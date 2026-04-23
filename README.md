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

## Sigues viendo el README en la web

1. Abre **`https://lorenzoadr.github.io/VarMonitor/`** (no la página del repo en github.com).
2. En **Settings → Pages**, desactiva cualquier **Deploy from a branch** / carpeta **`/(root)`** en `main`. Solo debe figurar **Source: GitHub Actions**.
3. En **Actions**, comprueba que **Deploy Astro to GitHub Pages** haya corrido tras tu último push (si solo tocabas `README.md`, antes el workflow podía no ejecutarse; ya está configurado para lanzarse en cualquier cambio en `main`).
4. Opcional: **Actions → Deploy Astro → Run workflow** para forzar un despliegue.
