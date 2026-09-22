# Web academica personal

Sitio estatico (HTML/CSS plano) para GitHub Pages.

## Estructura

- `index.html`: portada. Solo trabajo academico, con secciones ancladas About
  (#about), Research (#research) y Contact (#contact).
- `writing.html`: Other Writing. Policy reports, articles and blogposts y book
  reviews. Los titulos en castellano llevan la traduccion al ingles detras, en
  un `<span class="translation">[...]</span>`.
- `gallery.html`: galeria de fotos, con el lightbox en un `<script>` al final.
- `css/style.css`: unica hoja de estilos, compartida por las tres paginas.
- `files/`: PDFs (cv.pdf). Nombres en minusculas y sin espacios.
- `photos/`: imagenes optimizadas para web (JPG, <=2000 px de lado largo). Los
  originales en alta resolucion van en `photos/originals/`, excluida del repo.

La nav es identica en las tres paginas. Al anadir o quitar una entrada hay que
tocar las tres. La pagina activa lleva `class="active"` en su enlace.

## Publicar

1. Crear en GitHub el repositorio `carlos-sunyer.github.io`.
2. `git push -u origin main` (el remote ya esta configurado).
3. En Settings > Pages, comprobar que sirve desde la rama `main` (raiz).

La web queda en https://carlos-sunyer.github.io

## Anadir un paper nuevo

Copiar un bloque `<article class="paper">...</article>` en la seccion
correspondiente de `index.html`, editar titulo, coautores y enlaces, y hacer
commit + push. Para una entrada nueva en `writing.html`, mismo bloque mas la
linea de traduccion si el titulo esta en castellano.

## Ver en local

`py -m http.server 8000` en la raiz, y abrir http://localhost:8000
(configurado ya en `.claude/launch.json`). El servidor de Python es de un solo
hilo y suelta ERR_CONNECTION_RESET cuando la galeria pide las 13 fotos a la vez.
Es del servidor, no de la web.
