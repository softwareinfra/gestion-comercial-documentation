# Conclusiones tecnológicas del desarrollo

**Fecha de referencia:** 8 de agosto de 2026  
**Objetivo:** definir exclusivamente las tecnologías, arquitectura técnica, infraestructura, despliegue, seguridad, observabilidad y costos base del desarrollo.

> Este documento no define módulos funcionales, reglas de negocio, procesos comerciales ni requerimientos del sistema.

## 1. Arquitectura tecnológica seleccionada

El desarrollo utilizará una arquitectura desacoplada entre frontend, backend y base de datos.

```text
                    Internet
                       |
                       v
             DigitalOcean App Platform
                       |
            +----------+----------+
            |                     |
            v                     v
       Frontend SPA          Backend REST API
    React + Vite + TS        Django + DRF
      Static Site            Web Service
            |                     |
            |      HTTPS/JSON     |
            +---------->----------+
                                  |
                                  v
                       Managed PostgreSQL

                    Archivos estáticos
                           |
                           v
                  DigitalOcean Spaces
```

Principios técnicos:

- frontend y backend desacoplados;
- comunicación mediante HTTPS y JSON;
- API REST como interfaz de acceso al backend;
- PostgreSQL no expuesto directamente a los clientes;
- archivos persistentes almacenados fuera del contenedor de aplicación;
- infraestructura administrada como servicio, evitando servidores gestionados manualmente;
- despliegues automatizados desde GitHub;
- posibilidad de sustituir o agregar clientes sin modificar la base de datos.

## 2. Frontend

### Tecnologías

| Elemento | Tecnología |
|---|---|
| Framework | React |
| Build tool | Vite |
| Lenguaje | TypeScript |
| Marcado | HTML5 |
| Estilos | CSS3 |
| Navegación | React Router |
| Consumo HTTP | Fetch API o Axios |
| Componentes visuales | Bootstrap o librería equivalente |

### Modelo de ejecución

El frontend será una **Single Page Application, SPA**.

Vite compilará el proyecto a archivos estáticos:

```text
dist/
  index.html
  assets/
    *.js
    *.css
    imágenes
```

En producción no será necesario mantener un servidor Node.js ejecutándose para servir el frontend.

### Hosting

El frontend se publicará como **Static Site** dentro de DigitalOcean App Platform.

Costo de cómputo adicional estimado dentro de una App paga:

**US$0/mes**

Esto permite mantener frontend y backend como componentes independientes dentro de la misma App de DigitalOcean.

## 3. Backend

### Tecnologías

| Elemento | Tecnología |
|---|---|
| Lenguaje | Python 3.13 |
| Framework web | Django 5.2 LTS |
| API REST | Django REST Framework |
| Servidor WSGI | Gunicorn |
| ORM | Django ORM |
| Documentación API | OpenAPI / Swagger |
| Testing | pytest + pytest-django |
| Linting y formato | Ruff |

Django 5.2 se selecciona por ser una versión LTS, priorizando estabilidad y mantenimiento prolongado.

### Modelo de exposición

El backend será REST-first y publicará una API versionada.

Ruta base:

```text
/api/v1/
```

La API utilizará los métodos HTTP estándar:

```text
GET
POST
PUT
PATCH
DELETE
```

También se expondrá documentación técnica automática:

```text
/api/schema/
/api/docs/
```

Esto permitirá probar y consumir la API desde:

- frontend web;
- Postman;
- Insomnia;
- scripts de automatización;
- integraciones futuras;
- aplicaciones móviles;
- otros clientes HTTP autorizados.

## 4. Base de datos

### Tecnología

**PostgreSQL**

### Servicio

**DigitalOcean Managed PostgreSQL**

### Configuración inicial

| Recurso | Configuración |
|---|---:|
| vCPU | 1 |
| RAM | 1 GiB |
| Almacenamiento inicial | desde 10 GiB |
| Tipo | nodo único / Shared CPU |
| Precio base | **US$15.15/mes** |

### Decisiones técnicas

- PostgreSQL estará separado del backend.
- No se utilizará SQLite en producción.
- La aplicación accederá mediante Django ORM y conexiones PostgreSQL.
- Los consumidores externos no recibirán credenciales directas de PostgreSQL.
- El acceso externo se realizará mediante la API REST.
- La base de datos será un servicio administrado por DigitalOcean.

### Limitación inicial

La configuración de US$15.15 utiliza un solo nodo y no proporciona alta disponibilidad de base de datos.

Será la configuración inicial para controlar costos y posteriormente se evaluará el escalamiento usando métricas reales.

## 5. Procesamiento del backend

### Servicio

**DigitalOcean App Platform**

### Configuración inicial

| Recurso | Configuración |
|---|---:|
| Tipo | Shared Fixed |
| vCPU | 1 compartida |
| RAM | 1 GiB |
| Instancias | 1 |
| Transferencia incluida | 100 GiB/mes |
| Precio | **US$10/mes** |

Esta instancia ejecutará:

```text
Python
Django
Django REST Framework
Gunicorn
```

### Consideración

Esta configuración está orientada al lanzamiento y no proporciona redundancia horizontal.

No se contratará inicialmente una segunda instancia mientras el consumo real no lo justifique.

## 6. Almacenamiento de archivos

### Servicio

**DigitalOcean Spaces**

### Configuración base

| Recurso | Incluido |
|---|---:|
| Almacenamiento | 250 GiB |
| Transferencia saliente | 1,024 GiB/mes |
| CDN | Incluido |
| Precio | **US$5/mes** |

### Uso técnico

Spaces será utilizado para almacenamiento persistente de objetos y archivos.

No se utilizará el filesystem local de App Platform para información que deba persistir entre despliegues.

El backend se conectará a Spaces mediante una interfaz compatible con S3.

## 7. Organización de repositorios

Se utilizarán dos repositorios GitHub independientes:

```text
proyecto-frontend
  React
  Vite
  TypeScript

proyecto-backend
  Python
  Django
  Django REST Framework
```

### Ventajas técnicas

- despliegues independientes;
- pipelines independientes;
- versionamiento separado;
- menor acoplamiento entre capas;
- posibilidad de reemplazar el frontend sin modificar el backend;
- API reutilizable por otros clientes;
- responsabilidades técnicas claramente separadas.

DigitalOcean App Platform permite asociar componentes diferentes de una misma App a repositorios distintos.

La cantidad de repositorios no determina directamente el costo de App Platform. El costo depende de los componentes que consumen recursos de cómputo.

## 8. Estructura en DigitalOcean App Platform

Se utilizará una sola App con dos componentes principales:

```text
DigitalOcean App Platform

App: proyecto
  |
  +-- frontend
  |    tipo: Static Site
  |    origen: repositorio frontend
  |    costo de cómputo: US$0
  |
  +-- backend
       tipo: Web Service
       origen: repositorio backend
       costo: US$10/mes
```

La base de datos y Spaces serán servicios separados conectados a la aplicación.

## 9. Routing

Se recomienda utilizar un único dominio con routing por rutas.

Ejemplo:

```text
https://app.dominio.com/          -> Frontend
https://app.dominio.com/api/v1/   -> Backend Django REST
https://app.dominio.com/api/docs/ -> Swagger
```

Ventajas:

- configuración más sencilla de CORS;
- menor complejidad de cookies y autenticación;
- un solo certificado y dominio principal;
- menor complejidad para el frontend;
- routing centralizado por App Platform.

## 10. CI/CD

### Plataforma

**GitHub Actions**

### Pipeline del backend

```text
Push / Pull Request
        |
        +-- instalar dependencias
        +-- lint
        +-- format check
        +-- Django system checks
        +-- validar migraciones
        +-- tests unitarios
        +-- tests API
        +-- análisis de dependencias
        +-- build
        +-- deploy
```

Herramientas:

- pytest;
- pytest-django;
- Ruff;
- Django system checks;
- Dependabot.

### Pipeline del frontend

```text
Push / Pull Request
        |
        +-- npm ci
        +-- ESLint
        +-- TypeScript type check
        +-- tests
        +-- build Vite
        +-- deploy
```

Herramientas:

- ESLint;
- TypeScript;
- Vitest;
- Playwright para pruebas E2E cuando sea necesario.

### Costo

**US$0 estimado mientras el consumo se mantenga dentro de la cuota incluida por GitHub.**

Los minutos adicionales pueden generar costo si se supera la cuota correspondiente al plan de GitHub.

## 11. Seguridad técnica

La configuración inicial deberá contemplar como mínimo:

- HTTPS obligatorio;
- secretos únicamente mediante variables de entorno o mecanismos equivalentes;
- credenciales fuera del código fuente;
- CORS restringido;
- configuración correcta de CSRF cuando aplique;
- cookies `HttpOnly` y `Secure` cuando se utilicen sesiones o tokens en cookies;
- autenticación de API;
- autorización basada en permisos;
- rate limiting para endpoints sensibles;
- validación de contenido y tamaño de archivos;
- protección de ramas principales en GitHub;
- revisión automática de dependencias;
- conexiones TLS hacia PostgreSQL;
- almacenamiento persistente fuera del contenedor;
- bloqueo del acceso directo público a PostgreSQL cuando no sea necesario.

## 12. Observabilidad

### App Platform

Monitorear:

- CPU;
- RAM;
- latencia;
- cantidad de solicitudes;
- errores HTTP 4xx;
- errores HTTP 5xx;
- reinicios del servicio;
- consumo de transferencia.

### PostgreSQL

Monitorear:

- CPU;
- memoria;
- conexiones;
- almacenamiento;
- queries lentas;
- latencia de consultas;
- crecimiento mensual de datos.

### Spaces

Monitorear:

- almacenamiento utilizado;
- transferencia utilizada;
- solicitudes y errores relevantes.

### GitHub Actions

Monitorear:

- minutos utilizados;
- duración de pipelines;
- frecuencia de fallos;
- errores de build o despliegue.

## 13. Estrategia de escalamiento

La infraestructura no se sobredimensionará desde el inicio.

Se aumentarán recursos únicamente a partir de métricas.

### Backend

Configuración inicial:

```text
1 vCPU compartida
1 GiB RAM
US$10/mes
```

Siguiente nivel relevante:

```text
1 vCPU compartida
2 GiB RAM
US$25/mes
```

Se evaluará el aumento cuando exista presión sostenida de CPU o memoria, degradación de latencia o reinicios por falta de recursos.

### PostgreSQL

Configuración inicial:

```text
1 vCPU
1 GiB RAM
>= 10 GiB almacenamiento
US$15.15/mes
```

Siguiente nivel de referencia:

```text
1 vCPU
2 GiB RAM
30 GiB almacenamiento inicial
US$30.45/mes
```

El escalamiento dependerá principalmente de memoria, conexiones, latencia, consultas y crecimiento del almacenamiento.

## 14. Alta disponibilidad

La configuración inicial no se considera de alta disponibilidad.

No se contratará inicialmente:

- segunda instancia del backend;
- nodo PostgreSQL standby;
- balanceadores adicionales dedicados;
- Kubernetes;
- Redis administrado;
- workers permanentes adicionales;
- servidores virtuales gestionados manualmente.

Estas capacidades se agregarán únicamente si las métricas o requisitos técnicos futuros justifican el costo y la complejidad.

## 15. Tecnologías descartadas inicialmente

### Django Templates como frontend principal

No se utilizará como frontend principal porque se decidió mantener una separación real entre cliente web y API REST.

### Next.js con SSR

No se utilizará inicialmente porque requeriría un runtime Node.js permanente y otro componente de cómputo.

Para este proyecto, React + Vite permite un frontend dedicado sin agregar un servidor de frontend en producción.

### Kubernetes

No se utilizará inicialmente porque aumenta significativamente la complejidad operativa sin aportar beneficios proporcionales al tamaño inicial de la plataforma.

### Droplets o máquinas virtuales administradas manualmente

No se utilizarán porque requieren gestionar sistema operativo, actualizaciones, firewall, runtime, despliegues y mantenimiento del servidor.

### PostgreSQL autogestionado

No se utilizará como opción principal de producción. Se prioriza Managed PostgreSQL para reducir trabajo de administración, backups, actualizaciones y mantenimiento.

### Go o FastAPI como backend principal

Son alternativas técnicamente válidas, pero no ofrecen una ventaja suficiente para justificar sustituir Django + DRF en esta arquitectura.

Django aporta ORM, migraciones, autenticación, administración, ecosistema maduro y una integración directa con Django REST Framework.

## 16. Stack tecnológico definitivo

```text
FRONTEND
React
Vite
TypeScript
HTML5
CSS3
React Router
Fetch API / Axios
Bootstrap o equivalente

BACKEND
Python 3.13
Django 5.2 LTS
Django REST Framework
Gunicorn
OpenAPI / Swagger

BASE DE DATOS
PostgreSQL
DigitalOcean Managed PostgreSQL

ALMACENAMIENTO
DigitalOcean Spaces
S3-compatible API
CDN

INFRAESTRUCTURA
DigitalOcean App Platform
Static Site para frontend
Web Service para backend

CONTROL DE VERSIONES
Git
GitHub
2 repositorios

CI/CD
GitHub Actions

CALIDAD BACKEND
pytest
pytest-django
Ruff
Django system checks
Dependabot

CALIDAD FRONTEND
ESLint
TypeScript
Vitest
Playwright
```

## 17. Costos tecnológicos iniciales

| Componente | Proveedor | Servicio | Configuración | Precio mensual |
|---|---|---|---|---:|
| Frontend | DigitalOcean | App Platform Static Site | React + Vite | **US$0.00** |
| Backend | DigitalOcean | App Platform Shared Fixed | 1 vCPU / 1 GiB | **US$10.00** |
| Base de datos | DigitalOcean | Managed PostgreSQL | 1 vCPU / 1 GiB | **US$15.15** |
| Archivos | DigitalOcean | Spaces | 250 GiB + CDN | **US$5.00** |
| CI/CD | GitHub | GitHub Actions | dentro de cuota | **US$0 estimado** |
| **TOTAL BASE** | | | | **US$30.15/mes** |

Costo anual de referencia:

```text
US$30.15 x 12 = US$361.80/año
```

No se consideran dentro del total base:

- dominio;
- impuestos;
- exceso de transferencia;
- almacenamiento adicional;
- exceso de minutos de GitHub Actions;
- escalamiento de CPU o RAM;
- alta disponibilidad;
- servicios adicionales que se incorporen posteriormente.

## 18. Resumen de proveedores seleccionados

| Área | Proveedor |
|---|---|
| Cloud principal | DigitalOcean |
| Frontend hosting | DigitalOcean App Platform |
| Backend hosting | DigitalOcean App Platform |
| PostgreSQL | DigitalOcean Managed Databases |
| Object Storage | DigitalOcean Spaces |
| Repositorios | GitHub |
| CI/CD | GitHub Actions |

## 19. Decisión tecnológica final

La plataforma se construirá con una arquitectura REST desacoplada y dos proyectos independientes.

```text
GitHub
  |
  +-- frontend
  |    React + Vite + TypeScript
  |
  +-- backend
       Python + Django + DRF

             |
             v
     DigitalOcean App Platform
             |
      +------+------+
      |             |
      v             v
 Static Site     Web Service
   US$0           US$10
                    |
                    v
          Managed PostgreSQL
               US$15.15

          DigitalOcean Spaces
                US$5
```

**Costo tecnológico base estimado: US$30.15/mes.**

La estrategia técnica será comenzar con esta capacidad, medir el comportamiento real de la aplicación y escalar únicamente cuando CPU, memoria, conexiones, latencia, almacenamiento o transferencia lo justifiquen.

## 20. Referencias técnicas y de precios

Precios y condiciones utilizados como referencia al 8 de agosto de 2026:

- DigitalOcean App Platform Pricing: https://www.digitalocean.com/pricing/app-platform
- DigitalOcean App Platform Pricing Documentation: https://docs.digitalocean.com/products/app-platform/details/pricing/
- DigitalOcean Managed Databases Pricing: https://www.digitalocean.com/pricing/managed-databases
- DigitalOcean Managed PostgreSQL: https://www.digitalocean.com/products/managed-databases-postgresql
- DigitalOcean Spaces Pricing: https://docs.digitalocean.com/products/spaces/details/pricing/
- GitHub Actions Billing: https://docs.github.com/en/billing/concepts/product-billing/github-actions
- Django 5.2 release information: https://docs.djangoproject.com/en/5.2/releases/5.2/
- Vite documentation: https://vite.dev/guide/
