# VarMonitor — sitio público (Astro + MkDocs)

> **No confundir con esta página:** en GitHub, la vista **Código** del repo muestra este `README.md` en Markdown. **Eso no es la web desplegada.**  
> **Landing Astro (la que buscas):** **https://lorenzoadr.github.io/VarMonitor/** (con el segmento `/VarMonitor/`).  
> Si abres solo `https://lorenzoadr.github.io/` verás el sitio del repo **LorenzoAdr.github.io**, que es otro proyecto.

Este repositorio contiene la **landing** en [Astro](https://astro.build/), la documentación en Markdown procesada con [MkDocs](https://www.mkdocs.org/) (ES + EN) y el workflow de **GitHub Pages**.

El código de la aplicación (C++, Python, plugins) sigue en **[RealTimeMonitor](https://github.com/LorenzoAdr/RealTimeMonitor)**.

## URL publicada

Tras configurar Pages con **Source: GitHub Actions** (no «Deploy from a branch»): **https://lorenzoadr.github.io/VarMonitor/** (ajusta `base` en `astro/astro.config.mjs` si el nombre del repo en GitHub es otro).

## Build local

```bash
pip install mkdocs mkdocs-material pymdown-extensions
./scripts/build_docs_for_astro.sh
cd astro && npm ci && npm run build
```

Vista previa: `(cd astro && npm run preview)`.

## CI

Ver `.github/workflows/deploy-astro.yml` y la guía en `astro/DEPLOY.md`.
