# VarMonitor — sitio público (Astro + MkDocs)

Este repositorio contiene la **landing** en [Astro](https://astro.build/), la documentación en Markdown procesada con [MkDocs](https://www.mkdocs.org/) (ES + EN) y el workflow de **GitHub Pages**.

El código de la aplicación (C++, Python, plugins) sigue en **[RealTimeMonitor](https://github.com/LorenzoAdr/RealTimeMonitor)**.

## URL publicada

Tras configurar Pages con GitHub Actions: `https://lorenzoadr.github.io/VarMonitor/` (ajusta `base` en `astro/astro.config.mjs` si el nombre del repo en GitHub es otro).

## Build local

```bash
pip install mkdocs mkdocs-material pymdown-extensions
./scripts/build_docs_for_astro.sh
cd astro && npm ci && npm run build
```

Vista previa: `(cd astro && npm run preview)`.

## CI

Ver `.github/workflows/deploy-astro.yml` y la guía en `astro/DEPLOY.md`.
