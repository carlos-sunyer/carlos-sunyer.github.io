# Web academica personal

Sitio estatico de una sola pagina (HTML/CSS plano) para GitHub Pages.

## Estructura

- `index.html`: toda la web en una pagina, con secciones ancladas: About (#about), Research (#research), Policy & Outreach (#policy) y Contact (#contact). Photography (#photography) esta prevista y comentada en el menu.
- `css/style.css`: unica hoja de estilos.
- `files/`: PDFs (cv.pdf). Nombres en minusculas y sin espacios.
- `photos/`: imagenes optimizadas para web (JPG, <=2000 px de lado largo). Los originales en alta resolucion van en `photos/originals/`, excluida del repo.

## Publicar

1. Crear en GitHub el repositorio `carlos-sunyer.github.io`.
2. `git push -u origin main` (el remote ya esta configurado).
3. En Settings > Pages, comprobar que sirve desde la rama `main` (raiz).

La web queda en https://carlos-sunyer.github.io

## Anadir un paper nuevo

Copiar un bloque `<article class="paper">...</article>` en la seccion correspondiente de `index.html`, editar titulo, coautores y enlaces, y hacer commit + push.
