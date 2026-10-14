# Spec de desarrollo — [Nombre del emprendimiento]

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML y CSS, la estructura de archivos y la navegación definidas,
las variables de :root con los valores de DESIGN.md y la estructura
semántica de cada página. Usa el código de Stitch solo como referencia
visual. Al terminar, revisa cada criterio de aceptación y dime cuáles
se cumplen y cuáles no.
```

## 1. Estructura de archivos

```rockys-garage/
├── DESIGN.md
├── index.html
├── tienda.html
├── servicio-scanner.html
├── servicio-embrague.html
├── servicio-mantencion.html
├── servicio-frenos.html
├── carrito.html
├── agendar.html
├── confirmacion.html
├── blog.html
├── articulo-check-engine.html
├── articulo-embrague.html
├── articulo-mantencion.html
├── nosotros.html
├── contacto.html
├── preguntas-frecuentes.html
├── terminos.html
├── privacidad.html
├── 404.html
├── css/
│   └── styles.css
├── img/
├── stitch/
└── docs/
```

## 2. Páginas y navegación

| Desde | Elemento | Lleva a |
|---|---|---|
| Todas las páginas | Logo "Rocky's Garage" | index.html |
| Todas las páginas | Menú: Servicios | tienda.html |
| Todas las páginas | Menú: Blog | blog.html |
| Todas las páginas | Menú: Nosotros | nosotros.html |
| Todas las páginas | Menú: Contacto | contacto.html |
| Todas las páginas | Botón WhatsApp | wa.me con mensaje prellenado (número real por definir) |
| Pie de página | Preguntas frecuentes | preguntas-frecuentes.html |
| Pie de página | Términos | terminos.html |
| Pie de página | Privacidad | privacidad.html |
| Pie de página | Instagram | https://www.instagram.com/rg.automotriz_/ |
| index.html | Botón "Agendar hora" | agendar.html |
| index.html | Botón "Ver precio" | tienda.html |
| index.html | Tarjetas de servicio ("Ver") | servicio-scanner.html, servicio-embrague.html, servicio-mantencion.html y servicio-frenos.html |
| index.html | Tarjetas del blog | articulo-check-engine.html y articulo-embrague.html |
| index.html | Formulario de cotización | Prototipo visual: no envía datos |
| tienda.html | Categorías | Anclas dentro de la misma página (#diagnostico, #embrague, #mantencion, #frenos) |
| tienda.html | "Ver servicio" | Ficha de su categoría (scanner y check engine a servicio-scanner.html; embrague a servicio-embrague.html; aceite a servicio-mantencion.html; pastillas y amortiguadores a servicio-frenos.html) |
| tienda.html | "Pide tu cotización" | contacto.html#cotizacion |
| servicio-*.html | Ruta de navegación "Tienda" | tienda.html |
| servicio-*.html | "Agregar y agendar" | carrito.html |
| servicio-*.html | "Consultar por WhatsApp" | wa.me con mensaje prellenado |
| carrito.html | "Agendar hora" | agendar.html |
| carrito.html | "Seguir viendo servicios" | tienda.html |
| agendar.html | "Confirmar hora" | confirmacion.html |
| confirmacion.html | "Volver al inicio" | index.html |
| blog.html | Categorías | Anclas dentro de la misma página (#diagnostico, #embrague, #mantencion) |
| blog.html | "Leer artículo" | articulo-check-engine.html, articulo-embrague.html o articulo-mantencion.html |
| blog.html | "Agendar hora" | servicio-scanner.html |
| articulo-*.html | Ruta de navegación "Blog" | blog.html |
| articulo-*.html | Botón de servicio relacionado | servicio-scanner.html, servicio-embrague.html o servicio-mantencion.html, según el artículo |
| articulo-*.html | Compartir | Enlaces de WhatsApp, X y correo con el título del artículo |
| 404.html | "Volver al inicio" | index.html |

## 3. Estructura semántica

```html
<body>
  <a class="saltar" href="#contenido">Saltar al contenido</a>
  <header>
    <nav aria-label="Principal"> logo, menú y botón WhatsApp </nav>
  </header>
  <main id="contenido"> ... </main>
  <footer> contacto, ubicación, enlaces legales e Instagram </footer>
</body>
```

Contenido de `<main>` por página, con un solo `<h1>` y los títulos de sección en `<h2>`:

- **index.html:** `<section>` hero con `<h1>` y selector de auto; Servicios (`<article>` por tarjeta); Cómo funciona (`<ol>`); Trabajos reales (`<figure>` con `<figcaption>`); Reseñas (`<blockquote>`); Del blog (`<article>`); Pide tu cotización (`<form>` con `<label>`).
- **tienda.html:** `<h1>` Servicios; buscador (`<form role="search">`); `<nav aria-label="Categorías">`; una `<section id>` por categoría con un `<article>` por servicio.
- **servicio-*.html:** ruta de navegación (`<nav aria-label="Ruta de navegación">` con `<ol>`); `<h1>`; `<figure>`; datos (precio, duración, garantía); `<form>` selector de auto; Qué incluye (`<ul>`); Reseñas; Preguntas frecuentes con `<details>` y `<summary>`.
- **carrito.html, agendar.html y confirmacion.html:** `<h1>`, `<section>` de resumen o formulario y botón principal.
- **blog.html:** `<h1>`, `<nav>` de categorías y `<article>` por tarjeta dentro de una `<section id>` por categoría.
- **articulo-*.html:** `<article>` con `<h1>`, `<time>`, `<figure>` y `<h2>` por subtítulo; enlaces de compartir; `<section>` de comentarios con `<form>`; artículos relacionados.
- **nosotros.html:** `<h1>`, texto del taller y galería de `<figure>`.
- **contacto.html:** `<h1>`, datos de contacto y `<form id="cotizacion">`.
- **preguntas-frecuentes.html:** `<h1>` y `<details>` con `<summary>` por pregunta.
- **terminos.html y privacidad.html:** `<h1>` y `<h2>` por apartado.
- **404.html:** `<h1>`, mensaje breve y enlaces para volver.

## 4. Organización del CSS

```css
:root {
  /* Colores (DESIGN.md) */
  --color-principal: #BE282B;
  --color-secundario: #000000;
  --color-acento: #595959;
  --color-fondo: #FFFFFF;
  --color-fondo-alterno: #F2F2F2;
  --color-texto: #333333;
  --color-exito: #1E7B3A;
  --color-error: #8C1C20;

  /* Tipografía */
  --fuente-titulos: 'Playfair Display', Georgia, serif;
  --fuente-subtitulos: 'Barlow Condensed', 'Arial Narrow', sans-serif;
  --fuente-texto: 'Barlow', Arial, sans-serif;

  /* Tamaños (mobile) */
  --tam-h1: 36px;
  --tam-h2: 28px;
  --tam-h3: 22px;
  --tam-parrafo: 16px;
  --tam-boton: 16px;

  /* Espaciado y forma */
  --espacio-s: 8px;
  --espacio-m: 16px;
  --espacio-l: 24px;
  --espacio-xl: 48px;
  --radio: 6px;
  --ancho-max: 1200px;
}

@media (min-width: 768px) {
  :root {
    --tam-h1: 56px;
    --tam-h2: 40px;
    --tam-h3: 28px;
    --tam-parrafo: 18px;
    --tam-boton: 18px;
  }
}
```

## 5. Criterios de aceptación

**Navegación**
- [ ] Existen las 19 páginas de la estructura de archivos y todas abren sin error.
- [ ] Todo enlace de la tabla de la sección 2 lleva a la página indicada.
- [ ] El menú y el pie son iguales en todas las páginas, y la página actual lleva `aria-current="page"`.
- [ ] Desde el inicio se llega a agendar hora en 1 clic, y a la confirmación en máximo 4 clics.
- [ ] Todos los enlaces internos usan rutas relativas, para que funcionen en GitHub Pages.
- [ ] 404.html está en la raíz y se muestra al entrar a una ruta que no existe.

**Funcionalidades**
- [ ] El botón de WhatsApp abre wa.me con un mensaje prellenado en todas las páginas.
- [ ] Los botones de compartir abren WhatsApp, X y correo con el título del artículo.
- [ ] Las categorías de la tienda y del blog saltan a su sección dentro de la misma página.
- [ ] Las preguntas frecuentes se abren y cierran con `<details>`, sin JavaScript.
- [ ] Cada ficha de servicio muestra precio "desde", duración, garantía y qué incluye.
- [ ] El formulario de cotización, el selector de auto, el carrito, la agenda y los comentarios se ven completos pero no envían datos (prototipo visual).
- [ ] El sitio no usa JavaScript propio, solo HTML y CSS.

**Diseño**
- [ ] Todos los colores, fuentes y tamaños salen de `:root`; no hay valores escritos directamente en otras partes del CSS.
- [ ] El rojo #BE282B se usa solo en el botón principal, el logo, los títulos destacados y los enlaces; el negro, en el encabezado y el pie.
- [ ] El h1 usa Playfair Display en negrita cursiva; h2, h3 y botones usan Barlow Condensed 700; los párrafos usan Barlow 400.
- [ ] Cada página sigue el orden de componentes de su pantalla de Stitch y de la spec de diseño.
- [ ] Las imágenes son fotos reales de Rocky's Garage, no recuadros vacíos.
**Responsive**
- [ ] Todas las páginas se ven bien a 375px y a 1440px, sin scroll horizontal.
- [ ] En mobile, el menú es una hamburguesa que abre y cierra sin JavaScript y el botón de WhatsApp sigue visible.
- [ ] Las grillas de tarjetas pasan a 1 columna (2 en los servicios de la landing) en mobile.
- [ ] Los botones principales ocupan todo el ancho en mobile.
- [ ] En mobile, "Agregar y agendar" queda fijo en la parte inferior de la ficha de servicio.
- [ ] Los tamaños de texto son 36/28/22/16 px en mobile y 56/40/28/18 px en desktop.
**Accesibilidad y publicación**
- [ ] Los textos cumplen contraste AA; el rojo sobre negro solo se usa en texto grande.
- [ ] Todas las imágenes tienen `alt` (vacío si son decorativas).
- [ ] Cada página tiene un solo `<h1>` y una jerarquía de títulos sin saltos.
- [ ] Todos los campos de formulario tienen `<label>`, el foco se ve y se puede navegar con teclado.
- [ ] Cada página tiene `lang="es"`, un `<title>` propio, `meta description` y `meta viewport`.
- [ ] Las fuentes de Google Fonts tienen fuente de respaldo.
- [ ] El sitio está publicado en GitHub Pages y se ve igual desde la URL pública, con el CSS y las imágenes cargando bien.
- [ ] La política de privacidad explica qué datos recogen los formularios y para qué.