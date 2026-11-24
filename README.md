# holajuanpablo — Juan Pablo Montalva Peroni

Segundo sitio, derivado de `montalva-sitio` con menos secciones.

Sitio estático (HTML + CSS + JS, sin compilación). Para verlo, abre `index.html` en el navegador
o usa la extensión **Live Server** de VS Code.

## Estructura

```
index.html            Página única, dividida en secciones (ver comentarios <!-- ... -->)
css/
  main.css            Estilos del sitio (índice numerado al inicio del archivo)
  lightbox.css        Diseño del visor de fotos y videos
  vendor/             Librerías externas — NO editar (los cambios van en main.css o lightbox.css)
js/
  main.js             Comportamiento del sitio (portada, animaciones, visores)
  vendor/             Librerías externas — NO editar
images/
  background/         28 portadas Cover_2026.001.jpeg … Cover_2026.028.jpeg
  gallery/            Fotos de la sección Gallery
```

## Secciones de index.html (en este orden)

| id                | Contenido                                     |
|-------------------|-----------------------------------------------|
| (portada)         | Cover: 29 imágenes que cambian con el mouse   |
| `bio`             | Biografía                                     |
| `exhibitions`     | Selected Exhibitions                          |
| `books`           | Books & Publications                          |
| `highlights`      | Additional Highlights                         |
| `gallery`         | Galería de fotos                              |
| `motion`          | The Chapters (Vimeo)                          |
| `narrative-films` | Stolen Summer, The Squat, The Cosmos’ Heart   |
| `contact`         | Footer con contacto                           |

## Cómo agregar…

**Una foto a un proyecto:** copia un bloque `<div class="wow fadeInUp col-md-…">` completo dentro
de la fila (`<div class="row">`) y cambia `href`, `src`, `alt`, `width` y `height`.
La foto se abre sola en el visor (clase `image-popup`).

**Un video:** copia un `<a data-src="https://vimeo.com/ID" …>` dentro de su galería
(`class="video-gallery js-video-gallery"`) y cambia el ID de Vimeo en `data-src` y en el `<iframe>`.

**Una sección nueva:** crea un `<section id="…" aria-label="…">` dentro de `<main>`, empezando con
una barra de título:

```html
<div class="section-bar">
  <h2 class="section-heading">Nombre</h2>
</div>
```

## Librerías

Bootstrap 3.3.6 · animate.css · WOW.js 1.0.2 · jQuery 2.2.3 · Magnific Popup 1.1.0
(visor de fotos y videos) · Vimeo Player 2.30
