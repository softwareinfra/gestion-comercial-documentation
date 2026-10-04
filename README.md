# gestion-comercial-documentation

Documentación pública de G5-Service, publicada en GitHub Pages:
**https://softwareinfra.github.io/gestion-comercial-documentation/**

El contenido de `docs/` es una copia de la carpeta `doc/` del repositorio del frontend
(`softwareinfra/gestion-comercial-frontend`), que sigue siendo la fuente.

## Ver el sitio en local

```bash
pip install -r requirements.txt
mkdocs serve   # http://127.0.0.1:8000
```

Cada push a `main` lo publica el workflow `.github/workflows/publicar.yml`.
