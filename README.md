# Coffea — Landing Page (HTML5 + CSS3)

- **Sitio publicado (Netlify):** `https://coffea-landing-page.netlify.app` ← *reemplazar por tu URL real tras el deploy*
- **Repositorio:** `https://github.com/<usuario>/coffea-landing` ← *reemplazar por tu repo*

Sin JavaScript, frameworks ni build. Capas: `@layer tokens, base, layout, components, utilities`.

## Ejecutar en local
**A) VS Code:** abrí `coffea-landing/` y usá *Live Server* sobre `index.html`.
**B) Python:**
```bash
cd coffea-landing
python3 -m http.server 8000   # http://localhost:8000
```
**C) Node:**
```bash
cd coffea-landing
npx serve .
```

## Despliegue
1. Subí el proyecto a GitHub/GitLab (rama `main`).
2. En Netlify: *Add new site → Import from Git*. Build command vacío, publish directory `.` (ya en `netlify.toml`).
3. Cada Pull Request genera un Deploy Preview. Medí Lighthouse sobre la URL de producción.

## Assets pendientes
Las imágenes de `assets/img/*.jpg` son **placeholders**. Exportá las reales desde Figma (a 2x, comprimidas, idealmente AVIF/WebP con `<picture>`) y confirmá la licencia de las fotos de stock. `--color-star` debe confirmarse contra el SVG 0:200.
Con caché `immutable`, renombrá con versión los archivos CSS/assets modificados (`main.v2.css`).

## Convenciones
BEM, mobile-first (768 / 1024 / 1440), sin valores sueltos fuera de `css/tokens.css`.
