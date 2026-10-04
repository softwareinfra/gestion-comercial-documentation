# Contexto del proyecto — G5-Service (frontend)

> Documento de contexto consolidado. Reúne en un solo lugar lo que está repartido entre
> `doc/negocio/`, `doc/tecnico/`, `vault/` y el código. **No es fuente de verdad**: si algo acá
> contradice al contrato (`doc/negocio/Propuesta de proyecto.md`), a las decisiones de stack
> (`doc/tecnico/conclusiones_tecnologicas.md`) o al vault, mandan esos.
> Sirve para poner al día a alguien (persona o instancia de Claude Code) que llega al proyecto.

---

## 1. Qué es el proyecto

**G5-Service** — sistema de Gestión Comercial, Inventario, Garantías, Financiación y Tesorería para
una empresa colombiana de venta de equipos móviles (celulares Android/iPhone, tablets, computadores,
smartwatches, accesorios).

> El producto pasó a llamarse **G5-Service** el 2026-08-15. El nombre contractual del sistema en
> `doc/negocio/Propuesta de proyecto.md` **no se tocó**: ese documento es copia del backend y tiene
> gestión de cambios propia (§21). Los identificadores de infraestructura tampoco cambiaron todavía;
> el orden está en `vault/planes/despliegue/rename-a-g5-service.md` del repo backend.

Hoy la empresa opera con Excel y planillas manuales. El sistema reemplaza eso por una plataforma
web centralizada, multipunto, con control por IMEI y trazabilidad completa.

| Dato | Actual | Proyección |
|---|---|---|
| Puntos de venta | ~10 tiendas | ~50 ubicaciones |
| Ventas mensuales | ~350 | 700 – 1.000 |

**Este repo es solo el frontend**: la SPA en React + Vite + TypeScript. El backend
(`softwareinfra/gestion-comercial-backend`, Django + DRF) es un repo aparte. Ambos son componentes
de una misma app de DigitalOcean App Platform.

---

## 2. Estado actual

**Autenticación y andamiaje, sin ninguna pantalla de negocio todavía.** Lo que existe hoy:

- Proyecto Vite + React 19 + TypeScript en modo `strict`, compilando a `dist/`.
- **Sesión completa contra el backend**: login, logout, rehidratación al recargar y guard de rutas.
  El estado vive en `src/sesion/` (Context + `useReducer`, sin librería de estado).
- **Layout y navegación** de las 6 secciones. El menú se arma iterando `usuario.modules`, que
  devuelve `/auth/me/`: **no hay ninguna tabla rol → secciones en el frontend**, justamente porque
  la jerarquía Super Admin vs Admin sigue abierta con el cliente (contrato §20).
- Cliente HTTP en `src/api/client.ts`: `apiFetch<T>()`, `ApiError` (que lee el `detail` del cuerpo),
  CSRF y `getHealth()`.
- Tipos del contrato de auth en `src/api/types.ts`, verificados contra el backend real.
- 73 tests con Vitest + Testing Library, 87% de líneas cubiertas.
- CI/CD en GitHub Actions: `ci.yml` + 5 reusables (`_lint`, `_typecheck`, `_test`, `_build`,
  `_security`) con la puerta única `ci-ok`, más `cd.yml` y `_deploy-do.yml`.
- React Router ya entró (estaba en el stack fijo desde el principio). **Sin Bootstrap** — los
  estilos son CSS3 propio en `src/estilos/`. **Playwright entró el 2026-08-20** (también estaba en
  §16): `npm run e2e` corre la spec de humo (`e2e/humo.spec.ts`) contra el entorno local ya
  levantado con la skill `run-entorno-local`; sin etapa de CI mientras el CI siga apagado.

**No existe todavía**: ninguna pantalla de datos, ningún formulario de dominio, ningún listado
paginado, `Paginado<T>` (se crea con el primer listado), ni componente de negocio alguno. Las 6
secciones son destinos de navegación vacíos.

**Próximo paso**: el módulo Administración del backend ya está mergeado y expone 12 recursos REST,
así que la primera pantalla de datos ya tiene contra qué construirse.

---

## 3. Stack tecnológico

Fijado en `doc/tecnico/conclusiones_tecnologicas.md`. No se cambia sin pasar por
`/plan-cto-review`.

| Elemento | Tecnología |
|---|---|
| Framework | React 19 |
| Build tool | Vite 7 |
| Lenguaje | TypeScript 5.9, `strict: true` |
| Runtime de desarrollo | Node ≥ 22 (declarado en `engines`) |
| Gestor de paquetes | **npm** + `package-lock.json` committeado |
| Navegación | React Router *(previsto, aún no instalado)* |
| Estilos | Bootstrap o equivalente *(previsto, aún no instalado)* |
| HTTP | `fetch` nativo, envuelto en `src/api/client.ts` |
| Lint | ESLint 9 (flat config) + typescript-eslint |
| Tipos | `tsc --noEmit` como etapa de CI separada |
| Tests | Vitest 3 + Testing Library + jsdom |
| Cobertura | `@vitest/coverage-v8`, umbral 70% de líneas en CI |
| Seguridad de deps | `npm audit --omit=dev` + Dependabot |

### Infraestructura

Una sola app de DigitalOcean App Platform con dos componentes en repos distintos:

```
App: gestion-comercial (región nyc)
  ├─ frontend  Static Site  (este repo)              US$0/mes
  ├─ backend   Web Service  (repo backend)           US$10/mes
  ├─ job migrate  PRE_DEPLOY (repo backend)
  ├─ Managed PostgreSQL 17  gestion-comercial-db     US$15.15/mes
  └─ Spaces  250 GiB + CDN                           US$5/mes
```

**Routing por rutas bajo un único dominio** — es lo que elimina CORS. Reglas de ingress en orden:
`/api` → backend, `/admin` → backend, `/static` → backend, `/` (catch-all) → **este SPA**.
`catchall_document: index.html` en el app spec es lo que evita el 404 al recargar una ruta del SPA.

**El app spec no vive acá**: está en `.do/app.yaml` del repo backend, única fuente de verdad de la
infraestructura. El CD de este repo redespliega la app existente por nombre, sin copia local del spec.

> **Rename en curso.** `cd.yml` ya dice `app-name: g5-service`, pero la app en DigitalOcean todavía
> se llama `gestion-comercial`. El deploy de este repo está apagado (`DEPLOY_ENABLED` no existe), así
> que hoy no rompe nada. Antes de encenderlo hay que renombrar la app **en el panel de DO** y recién
> después alinear el `name:` del app spec del backend — nunca al revés: cambiar solo el spec **crea
> una segunda app** con su propia base vacía. `gestion-comercial-db` no se toca nunca: es la mitad
> izquierda de las referencias `${gestion-comercial-db.DATABASE_URL}`.

---

## 4. Los 6 módulos del negocio

El contrato define 6 módulos (§3). El backend los implementa como apps Django; acá se traducen a
secciones de navegación y pantallas. Ver `vault/arquitectura/modulos.md` para el detalle.

1. **Administración** — usuarios, roles, sucursales/bodegas, proveedores, entidades financieras,
   catálogos. Todo lo demás depende de esto.
2. **Inventario** — equipos por IMEI, traslados.
3. **Ventas** — incluye caja y movimientos de dinero.
4. **Garantías y Devoluciones**.
5. **Metas Comerciales**.
6. **Dashboard e Informes** — capa de agregación, se construye al final.

El frontend **no puede adelantarse** a los endpoints del backend: una pantalla sin API detrás no es
entregable. El orden de construcción sigue al del backend.

---

## 5. Reglas de negocio que impactan la UI

Estas aplican a todo el sistema y son las que revisan `/arquitecto`, `/plan-eng-review`, `/review`
y el subagent `developer`:

1. **No-borrado-físico** (§6.3). La UI **no ofrece** botones de "Eliminar" sobre ventas, garantías,
   traslados, movimientos de caja, equipos, usuarios ni sucursales. Las acciones son: crear,
   consultar, editar cuando corresponda, deshabilitar, anular, archivar. **La única excepción de
   todo el SPA es borrar un filtro guardado del tablero** (cambio 2.8b): es una preferencia del
   usuario y no un registro operativo, y el usuario la ratificó por escrito el 2026-09-19. No es un
   precedente — ver `vault/decisiones/filtros-guardados-con-nombre.md`.
2. **Aislamiento por sucursal** (§6.1). Un Vendedor no ve inventario de otros puntos. El frontend
   **no es la barrera de seguridad** — filtra el backend — pero tampoco debe mostrar selectores de
   sucursal ni vistas consolidadas a roles que no las tienen.
3. **Trazabilidad** (§6.4). Los campos de auditoría (usuario, fecha/hora, sucursal, aprobador) los
   deriva el backend del request autenticado: **nunca se envían desde el cliente**.
4. **Visibilidad por rol** (§7.9). Costo y ganancia pueden ocultarse a determinados roles. La UI
   debe soportar que un campo simplemente no venga en la respuesta, sin romperse.
5. **Flujo de aprobación de ventas** (§9.11/9.12). Modificar o anular una venta confirmada abre una
   *solicitud* con justificación obligatoria — nunca un formulario de edición directa.
6. **Fórmulas de precios** (§8.11). Se calculan en el backend a partir de parámetros administrables.
   El frontend las **muestra**, no las recalcula: nada de `0.03`, `100000`, `0.11` ni `0.19` en el
   código del SPA.
7. **Medios de pago combinados** (§9.8). La suma de medios + valor financiado debe coincidir con el
   total. La validación en el cliente es de conveniencia; la autoritativa es la del backend.
8. **IMEI único** (§8.10) y estados del equipo coherentes.

### Roles iniciales

| Rol | Alcance |
|---|---|
| **Super Administrador** | Acceso completo |
| **Administrador** | Gestión administrativa autorizada, aprueba modificaciones y anulaciones |
| **Administrador de Punto** | Su sucursal |
| **Vendedor** | Inventario de su punto, registro de ventas, impresión, inicio de garantías |
| **Bodeguero** (§21, aprobado el 2026-09-29) | Solo Inventario, en su sede (bodega, punto o ambos), con lo mismo que hace ahí el Administrador de Punto: consultar equipos con costo y proveedor, historial, cambiar estados, ingresos, traslados y parámetros de precio. No edita fichas ni precios |

Además de lo que trae su rol, un Administrador de Punto, un Vendedor o un Bodeguero puede tener **permisos
extra** que le otorga el Super Administrador desde su ficha (Administración → Usuarios), por módulo y por acción.
Un extra nunca amplía el alcance: sigue siendo su sede. El SPA abre pantallas y acciones por el código de
`me.permissions`, nunca por el nombre del rol (`vault/decisiones/permisos-extra-en-el-spa.md`).

### Compatibilidad con dispositivos (§5)

Diseño **desktop first**. Tablet y celular deben permitir login, consulta y operaciones básicas,
con formularios adaptados al ancho; las tablas amplias pueden requerir scroll horizontal. **No** se
promete experiencia equivalente a app nativa, ni reorganización especializada de dashboards para
celular, ni funcionamiento offline, ni instalación desde App Store / Play Store. El criterio de
aceptación es la visualización desde computador.

### Impresión (§7.8, §9.13)

Los formatos imprimibles se generan desde los datos guardados y se imprimen o guardan como PDF
**desde el navegador** — el sistema no almacena PDF automáticamente. Firma y huella son manuales
sobre papel: no hay captura digital ni biométrica en el alcance base.

---

## 6. Estructura del repositorio

```
gestion-comercial-frontend/
├── src/
│   ├── App.tsx            mapa de rutas; las 6 secciones salen del mismo mapa que el menú.
│   │                      Las 35 pantallas entran por React.lazy — ver
│   │                      vault/decisiones/carga-diferida-por-modulo.md.
│   │                      Al estrenar pantallas, un módulo tiene que sumarse a
│   │                      MODULOS_CON_PANTALLAS **y** llevar su <RutaProtegida> escrita a
│   │                      mano: sale del bloque generado que se la daba gratis
│   ├── main.tsx           punto de entrada: createRoot + BrowserRouter + SesionProvider
│   ├── api/               capa transversal, NO un módulo de negocio
│   │   ├── client.ts      apiFetch, ApiError (con errores DRF por campo), CSRF por cookie. Un 204
│   │   │                  resuelve sin leer el cuerpo: antes de 2.8b CUALQUIER éxito sin cuerpo
│   │   │                  reventaba en response.json(), después de que el servidor ya había actuado
│   │   ├── auth.ts        iniciarSesion, cerrarSesion, obtenerSesion, asegurarCsrf
│   │   ├── recursos.ts    factoría CRUD genérica (listarPagina, obtener, crear, actualizar,
│   │   │                  accionCicloDeVida) que comparten los cuatro módulos. `borrar` es el
│   │   │                  ÚNICO DELETE del SPA y existe solo para los filtros guardados
│   │   ├── filtrosGuardados.ts  crear y borrar un favorito del tablero (/saved-filters/). No
│   │   │                  importa nada de src/dashboard/: api/ no depende de una feature
│   │   ├── administracion.ts / inventario.ts / ventas.ts / metas.ts / dashboard.ts / garantias.ts
│   │   │                  por módulo: sus rutas, su lista de filtros y su
│   │   │                  clavesDeFiltrosSeguras con las FKs propias
│   │   ├── descargas.ts   descargarArchivo: la única descarga al navegador (Blob + ancla) de
│   │   │                  los libros de Excel que arma el backend (pedirArchivo pide SOLO
│   │   │                  SpreadsheetML), y el texto de sus errores — ver vault/decisiones/descarga-de-archivos.md
│   │   ├── types.ts       tipos del contrato (Sesion, Paginado<T>, y los recursos de los
│   │   │                  cuatro módulos construidos)
│   │   └── expiracion.ts  aviso de 401: la frontera de red transporta, el reducer decide
│   ├── administracion/    módulo de Administración: 15 pantallas en paginas/
│   ├── inventario/        módulo de Inventario: equipos por IMEI, ingresos, traslados
│   ├── ventas/            módulo de Ventas: historial, alta, solicitudes de cambio, caja y cuadre de caja
│   ├── metas/             módulo de Metas: listado, ficha e imprimible, más alcance.ts y
│   │                      avance.ts (lógica pura) — ver vault/planes/plan-modulo-metas.md
│   ├── dashboard/         módulo de Dashboard e Informes: cuatro tableros de lectura y formato.ts
│   │                      (relleno de la serie y rótulos); los libros de Excel del tablero los
│   │                      arma el backend (series/export/ y by/export/).
│   │                      Dos features sobre los filtros, que conviven: useFiltrosRecordados
│   │                      (RECUERDA los últimos, en localStorage) y FiltrosGuardados (favoritos
│   │                      CON NOMBRE, en el servidor). Las dos pasan por consultaDeFiltros.ts
│   │                      —depurar, paraGuardar, normalizar—, UNA sola implementación a propósito:
│   │                      ver vault/decisiones/filtros-guardados-con-nombre.md
│   ├── garantias/         módulo de Garantías: /garantias (equipos en garantía y cambio de
│   │                      estado con motivo); la mitad del reemplazo de IMEI espera al backend
│   ├── hooks/             hooks de datos compartidos: usePaginado, useRecurso,
│   │                      useCatalogoCompleto (acepta filtros, que entran SERIALIZADOS a las
│   │                      dependencias del efecto: con el objeto, un literal inline lo pone en un
│   │                      bucle que no da test rojo sino que mata al worker de Vitest),
│   │                      useBusqueda, useTrampaDeFoco y useValorDemorado
│   │                      (demora genérica; la usa la cotización de Ventas, que cuenta contra el
│   │                      tope horario de toda la API — ver vault/decisiones/precio-editable-e-intermediacion.md)
│   ├── sesion/            Context + useReducer, useSesion, RutaProtegida
│   ├── layout/            Layout (menú lateral oscuro + barra con la miga), Navegacion, el mapa
│   │                      Modulo -> {ruta, etiqueta, icono} y pantallas.ts, el mapa de pantallas
│   │                      por módulo que comparten el acordeón del menú y la miga
│   ├── paginas/           Login, Inicio, Seccion, NoEncontrado
│   ├── componentes/       transversales: estados (Cargando, ErrorDeCarga, SinDatos), los
│   │                      controles del sistema visual (Icono, Desplegable, BuscadorAvanzado,
│   │                      Insignia, Paginador), TarjetaDeFiltros, la tarjeta de filtros de las
│   │                      16 pantallas que filtran (rótulos, secciones plegables y pie con
│   │                      «Limpiar filtros»), DialogoDeFormulario, que hospeda TODOS los
│   │                      formularios de alta/edición, y Dato, la pareja rótulo-valor de una
│   │                      ficha: un <dt>/<dd> suelto dentro de <dl className="ficha"> rompe la
│   │                      rejilla con un número impar de columnas — ver
│   │                      vault/decisiones/sistema-visual-crimson.md,
│   │                      vault/decisiones/filtros-en-secciones.md y
│   │                      vault/decisiones/formularios-en-dialogo.md
│   ├── estilos/           tokens.css, layout.css, componentes.css, administracion.css e
│   │                      impresion.css (CSS3 propio, sin framework). Se importan EN ESE ORDEN
│   │                      desde main.tsx, y el orden decide los empates de especificidad: un
│   │                      modificador tiene que vivir en el mismo archivo que su base
│   ├── catalogos.ts / vigencia.ts / fechas.ts / moneda.ts / porcentaje.ts
│   │                      lógica pura compartida: helpers de catálogo,
│   │                      versión vigente, fechas, pesos y fracción → porcentaje (sobre el texto,
│   │                      sin punto flotante). Al lado, filtrosAplicados.ts: el conteo de
│   │                      filtros aplicados que muestra el pie de la tarjeta de filtros
│   ├── pruebas/           andamiaje de tests compartido: stubDeRed, controles, sesion,
│   │                      tarjetaDeFiltros, pausaDeTipeo y rutasDiferidas (todo test que monte
│   │                      <App /> la llama: las rutas lazy() necesitan más margen que el segundo
│   │                      por defecto de Testing Library)
│   ├── setupTests.ts      jest-dom para Vitest
│   └── vite-env.d.ts
├── doc/                   documentación de origen (contrato + stack)
│   ├── negocio/           Propuesta de proyecto.md  ← copia; canónica en el backend
│   ├── tecnico/           conclusiones_tecnologicas.md ← copia; canónica en el backend
│   └── desarrollo/        documentación técnica viva de este repo (este archivo)
├── vault/                 decisiones de ingeniería tomadas durante el desarrollo (Obsidian)
│   └── referencias/       material de referencia versionado (las capturas del sistema visual)
├── scripts/               verificaciones del build que no son tests: verificar-chunks.mjs
│                          corre despues de `vite build` y falla si el arranque baja un
│                          chunk de módulo
├── graphify-out/          grafo de conocimiento del código (committeado a propósito)
├── pruebas-manuales/      planes de prueba para el evaluador humano (.xlsx + su plan-*.json)
│                          los genera la skill plan-de-pruebas-manuales; .fuentes/ va ignorado
├── .claude/               comandos, agentes y skills del proyecto
├── .github/
│   ├── workflows/         ci.yml, cd.yml y 6 reusables
│   └── dependabot.yml
├── index.html             plantilla de Vite, lang="es"
├── vite.config.ts         build y su manualChunks por módulo, proxy /api -> :8000 (dev en
│                          :5173 y preview del build en :4173), config de Vitest
├── tsconfig.json          strict, noUnusedLocals, noUnusedParameters
├── eslint.config.js       flat config
└── package.json / package-lock.json
```

### `doc/` vs `vault/` — no se duplican

- **`doc/`** = lo que se acordó **antes** de empezar. `negocio/` y `tecnico/` son copias del
  backend (ver `doc/README.md`); `desarrollo/` es propio de este repo.
- **`vault/`** = decisiones de ingeniería tomadas **durante** el desarrollo, en formato Obsidian
  con wikilinks. Empieza por `vault/README.md`.

---

## 7. Configuración y entornos

### Arranque local

```bash
npm ci
npm run dev     # http://localhost:5173
```

Requiere el backend corriendo en `localhost:8000` (ver el `README.md` del repo backend: Docker
Compose + `uv run python manage.py runserver`). El proxy de `vite.config.ts` reenvía `/api` hacia
allá, replicando el routing por rutas que en producción resuelve el ingress de App Platform. Por
eso `VITE_API_BASE_URL` es una ruta relativa en los dos entornos.

### Variables de entorno

Plantilla en `.env.example`; copiar a `.env.local` (nunca se sube a git).

| Variable | Uso |
|---|---|
| `VITE_API_BASE_URL` | Base de la API. `/api/v1` en desarrollo y producción. |

**Vite solo expone al navegador las variables con prefijo `VITE_` y las congela en tiempo de
build.** Nunca poner un secreto ahí: queda en el bundle público.

---

## 8. CI/CD

### Integración continua (`ci.yml`)

Orquestador + 5 reusables. Se dispara en PR a `develop`/`main`, push a `develop`/`main`, y
`workflow_dispatch`. La versión de Node se declara en un solo lugar: `ci.yml`.

| Job | Qué hace |
|---|---|
| `lint` | `npm run lint` (ESLint) |
| `typecheck` | `tsc --noEmit` — etapa aparte porque `vite build` **no** comprueba tipos (esbuild solo borra las anotaciones) |
| `test` | Vitest con cobertura, umbral 70% de líneas, publica junit + coverage |
| `build` | `vite build` con `VITE_API_BASE_URL=/api/v1`; falla si no genera `dist/index.html` |
| `security` | `npm audit --omit=dev --audit-level=high` + verifica que no haya `.env` versionado |
| `ci-ok` | puerta única: es el único check que hay que marcar como obligatorio |

### Despliegue continuo (`cd.yml`)

Solo `main` despliega. Llama a `_deploy-do.yml`, que redespliega la app existente por nombre
(`g5-service`, ver el aviso de rename en §Infraestructura) y comprueba que el sitio responda 200.

**El deploy está apagado** hasta que exista la cuenta de DigitalOcean: el job se salta mientras la
variable de repositorio `DEPLOY_ENABLED` no valga `true`. Para activarlo, sin tocar archivos: crear
el secret `DIGITALOCEAN_ACCESS_TOKEN` y la variable `DEPLOY_ENABLED=true`.

### Deuda conocida del pipeline

Ver `vault/decisiones/deuda-del-pipeline.md`. En resumen, tres correcciones que el backend ya
aplicó y este repo todavía no:

1. `_deploy-do.yml` salta la comprobación del sitio cuando no hay `live_url`, dejando el job verde
   sin haber verificado nada.
2. `dependabot.yml` no tiene freno de majors.
3. `cd.yml` revalida solo con `_build.yml`, no con el CI completo.

---

## 9. Flujo de trabajo con Claude Code

La cadena completa (definida en `vault/decisiones/flujo-review-qa-ship.md`), en orden — cada paso
puede detener el flujo:

| # | Comando | Pregunta que responde |
|---|---|---|
| 1 | `/plan-cto-review` | ¿Encaja en el stack/infraestructura ya decidido? |
| 2 | `/plan-ceo-review` | ¿Está dentro del alcance contratado? |
| 3 | `/arquitecto` | ¿El diseño respeta límites de módulo, visibilidad por rol, no-borrado, desktop-first? |
| 4 | `/plan-eng-review` | Plan técnico concreto: componentes, tipos, contrato de API, plan de pruebas |
| 5 | subagent `developer` | Implementación con **TDD obligatorio** (RED-GREEN-REFACTOR por pieza) |
| 6 | `/review` | Reglas de negocio sobre el diff + revisión genérica |
| 7 | `/qa` | lint + typecheck + tests + build contra criterios de aceptación |
| 8 | `/ship` | Réplica local del pipeline de CI antes de abrir PR |
| 9 | `/commit-push` | Commit + push, incluyendo el rebuild async de `graphify-out/` |
| 10 | `/pr` | PR rama → `develop`, y acompaña la promoción `develop` → `main` |

`/develop-feature` encadena los pasos 1–8 con gates de confirmación y ledger reanudable en
`.claude/flow-state/`. Termina en `/ship` a propósito: no automatiza push ni PR.

### Skills propias

`react-components`, `vitest-rtl-patterns`, `systematic-debugging`, `git-commit-push-seguro`.
Ver `.claude/SKILLS.md`.

### Convenciones de git — reglas duras

- **Nunca** se commitea ni se abre un PR estando parado en `develop` o `main`. Sin excepción por
  tamaño: ni un typo en un `.md`. Todo va por una rama `feature/*`.
- Flujo: `feature/*` → `develop` → `main`. `/pr` hardcodea `--base develop` (si confiara en el
  default branch reportado por GitHub abriría PRs directo a `main`).
- Preferir **squash and merge** para mantener el historial limpio.
- `/pr` verifica los merges de verdad (`gh pr view` + `git merge-base --is-ancestor`), no confía en
  la palabra del usuario. Borra ramas `feature/*` ya mergeadas; **nunca** `develop` ni `main`.

---

## 10. Incidentes y trampas ya conocidas

1. **`vite build` no comprueba tipos.** esbuild solo borra las anotaciones. Sin la etapa
   `typecheck` separada, un error de tipos compila y llega a producción.
2. **`VITE_API_BASE_URL` se congela en el build.** No es configurable en runtime: cambiarla exige
   recompilar y redesplegar.
3. **Sin `catchall_document: index.html` en el app spec, recargar una ruta del SPA da 404.** El
   enrutado lo resuelve el cliente, no el servidor. Está declarado en el spec del backend.
4. **`npm install` puede resolver versiones distintas a las del lockfile.** En CI siempre `npm ci`.
5. **`npm audit` sin `--omit=dev` rompe por vulnerabilidades que nunca llegan al bundle.** Solo se
   auditan las dependencias de producción.
6. **La cobertura excluye `main.tsx`, `setupTests.ts` y `vite-env.d.ts`**: son andamiaje sin lógica,
   medirlos daría un porcentaje engañoso.
7. **El repo tuvo `main` y `develop` vacíos** (solo `.gitignore` y `README.md`) mientras todo el
   scaffold vivía en una rama sin mergear. El app spec del backend apunta el static site a `main`
   con `build_command: npm ci && npm run build`: con `main` en ese estado, el primer despliegue de
   la app habría fallado en el build del frontend, y `validar_app_spec.py` del backend no puede
   detectarlo porque solo valida el servicio backend.
8. **Los indicadores de costo/ganancia pueden no venir en la respuesta** según el rol. Un
   componente que asuma que el campo siempre existe se rompe para Vendedor.
9. **`manualChunks` puede volver eager un chunk que se creía diferido, y no avisa.** Si algo que el
   arranque importa de forma estática termina dentro de un chunk de módulo, Rollup lo convierte en
   dependencia estática del `index`, Vite le pone un `modulepreload` y el navegador se lo baja
   igual: la carga diferida queda escrita y no difiere nada. Pasó el 2026-08-23 con React, alojado
   en `modulo-administracion`. El aviso de tamaño de Vite tampoco lo atrapa, porque mide un chunk
   a la vez. Lo vigila `scripts/verificar-chunks.mjs`, enganchado a `npm run build`.
10. **El servidor de desarrollo no puede mostrar si el agrupado de chunks quedó bien**: entrega un
   módulo por archivo. Los chunks solo existen en el `dist/` compilado, así que verificar carga
   diferida exige `npm run build` + `npm run preview` (:4173, con su propio proxy a :8000), no
   `npm run dev`.
11. **Un diálogo montado DENTRO de un contenedor con reglas por descendiente las hereda, y ningún
   test lo ve.** Pasó el 2026-09-19: el diálogo de «Guardar filtros» quedaba dentro de la tarjeta
   `.filtros`, y `.filtros label` (mayúsculas, gris) le ganaba a `.campo label` por orden de
   import. Los diálogos los monta la PANTALLA; el que lo abre un componente metido en un contenedor
   así sale por `createPortal(…, document.body)`. Lo que sí se afirma en jsdom es la posición en el
   DOM. Ver `vault/decisiones/jsdom-no-ve-especificidad-css.md`.
12. **Un efecto de datos con un objeto literal en sus dependencias no falla: cuelga la corrida.**
   Satura los microtasks, el timeout de Vitest nunca dispara y a los ~2 minutos el worker cae con
   `ERR_IPC_CHANNEL_CLOSED`. Si una corrida se cuelga así después de tocar un hook de datos, es eso.
13. **jsdom enfoca un control escondido dentro de `[hidden]`, y el navegador no.** Una prueba que
   devuelve el foco a un filtro de una sección plegada pasa en verde, y en el navegador el foco cae
   al `body`. Las pruebas de la tarjeta de filtros usan `esperarFocoVisible`
   (`src/pruebas/controles.ts`), que además exige que ningún ancestro sea `[hidden]`. Ver
   `vault/decisiones/filtros-en-secciones.md`.
14. **El proyecto no tiene una regla global `[hidden] { display: none }`.** Un `display` propio
   (`grid`, `flex`) le gana al del navegador y el elemento con `hidden` se sigue viendo. Pasó el
   2026-09-28 con el cuerpo de las secciones plegables: cada componente que esconde con `hidden` y
   declara `display` necesita su propia regla `[hidden]`.

---

## 11. Pendientes de definición con el cliente (contrato §20)

Bloquean el diseño de las pantallas correspondientes:

- Aprobación del **único** formato imprimible de venta.
- Campos definitivos de garantía y cuál es la plataforma de garantías.
- Base exacta sobre la que se aplica el 3% de porcentaje adicional.
- Confirmación de qué valores son fijos y cuáles administrables.
- Reglas iniciales de corte y pago de las entidades financieras.
- Jerarquía final Super Administrador vs Administrador.
- Fórmulas definitivas del Dashboard, orden de indicadores, gráficos y **visibilidad por rol**.
- Decisión final sobre adjuntos e importación desde Excel — **opcionales cotizables**, no están en
  el alcance base.

---

## 12. Dónde buscar qué

| Pregunta | Fuente |
|---|---|
| ¿Qué se contrató? ¿Está esto en el alcance? | `doc/negocio/Propuesta de proyecto.md` |
| ¿Qué tecnología se decidió y por qué? | `doc/tecnico/conclusiones_tecnologicas.md` |
| ¿Por qué se hizo así durante el desarrollo? | `vault/decisiones/` |
| ¿Cómo se traducen los módulos a pantallas? | `vault/arquitectura/modulos.md` |
| ¿Qué pasó y cuándo? | `vault/avances/bitacora.md` |
| ¿Cómo arranco el proyecto? | `README.md` y la sección 7 de este documento |
| ¿Cómo está configurada la infraestructura? | `.do/app.yaml` **en el repo backend** |
| ¿Dónde está X en el código? | `graphify query "<pregunta>"` |
| ¿Cómo trabajo en este repo con Claude Code? | `CLAUDE.md` + `.claude/commands/` |
