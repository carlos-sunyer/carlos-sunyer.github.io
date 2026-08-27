# Web académica personal

Sitio estático (HTML/CSS plano) para GitHub Pages.

## Estructura

- `index.html` — portada: foto, bio, afiliación y enlaces (CV, email, Scholar).
- `research.html` — publicaciones, working papers y capítulos de libro.
- `policy.html` — policy reports y divulgación.
- `photography.html` — galería de fotos (pendiente, el enlace en el menú está comentado).
- `css/style.css` — única hoja de estilos de todo el sitio.
- `files/` — PDFs: CV, papers, reports. Nombres en minúsculas y sin espacios (`cv.pdf`, `sunyer-2025-titulo.pdf`).
- `photos/` — imágenes optimizadas para web (JPG/WebP, ≤2000 px lado largo, ~300–500 KB). Los originales en alta resolución NO van al repo.

## Publicar

1. Crear en GitHub un repositorio llamado `<usuario>.github.io`.
2. `git remote add origin https://github.com/<usuario>/<usuario>.github.io.git`
3. `git push -u origin main`
4. En Settings → Pages, comprobar que sirve desde la rama `main` (raíz).

La web queda en `https://<usuario>.github.io`.

## Añadir un paper nuevo

Copiar un bloque `<article class="paper">…</article>` en `research.html`, editar título/coautores/enlaces, subir el PDF a `files/` y hacer commit + push.
