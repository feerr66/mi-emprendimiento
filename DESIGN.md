---
version: alpha
name: "[Rocky´s Garage]"
description: "[Design system de Rocky's Garage, taller de mecánica ligera, scanner y embrague, en blanco, rojo y negro, con títulos en cursiva serif y textos en sans condensada.
colors:"
# Guía: evaluacion/guias/fase-2-specs/06-spec-de-diseno.md
# Reemplaza TODOS los valores de ejemplo por los de tu paleta y tipografía
# (docs/08-color-tipografia.md). Los HEX van siempre entre comillas.
# Valida con: npx @google/design.md lint DESIGN.md
colors:
  primary: "#BE282B"
  primary-hover: "#9E1F23"
  on-primary: "#FFFFFF"
  secondary: "#000000"
  on-secondary: "#FFFFFF"
  tertiary: "#595959"
  on-tertiary: "#FFFFFF"
  neutral: "#FFFFFF"
  surface: "#F2F2F2"
  on-surface: "#333333"
  success: "#1E7B3A"
  error: "#8C1C20"
typography:
  headline-display:
    fontFamily: Playfair Display
    fontSize: 56px
    fontWeight: 900
    lineHeight: 1.1
  headline-lg:
    fontFamily: Barlow Condensed
    fontSize: 40px
    fontWeight: 700
    lineHeight: 1.15
  headline-md:
    fontFamily: Barlow Condensed
    fontSize: 28px
    fontWeight: 700
    lineHeight: 1.2
  body-lg:
    fontFamily: Barlow
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.6
  body-md:
    fontFamily: Barlow
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-md:
    fontFamily: Barlow Condensed
    fontSize: 18px
    fontWeight: 700
    lineHeight: 1.2
rounded:
  sm: 4px
  md: 6px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 12px 24px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 12px 24px
  button-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.secondary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 12px 24px
  card:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.md}"
    padding: 16px
  input:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 16px
  navbar:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    typography: "{typography.label-md}"
    padding: 16px 24px
  tag:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 4px 12px
---

# Rocky's Garage — Design system

## Overview

Rocky's Garage es un taller de mecánica ligera, scanner y embrague en Villa Alemana, con servicio a domicilio. El sistema parte de la identidad que ya existe en su Instagram (@rg.automotriz_): logo RG en rojo sobre fondo blanco, títulos en cursiva serif roja y textos en sans condensada negra.

La personalidad es clara, confiable y cercana: un taller que explica lo que hace, muestra precios y trabajos reales, y se deja contactar por WhatsApp. El diseño es mobile primero, porque el cliente típico busca y reserva desde el celular. La base es blanca, el negro ordena (encabezado, pie y títulos de apoyo) y el rojo se reserva para lo que debe llamar la atención: botones principales, logo y títulos destacados.

## Colors

| Rol | Nombre | HEX | Uso |
|---|---|---|---|
| primary | Rojo Rocky | #BE282B | Botones principales ("Agendar hora"), logo, títulos destacados y enlaces |
| primary-hover | Rojo oscuro | #9E1F23 | Estado hover y presionado del botón principal |
| on-primary | Blanco | #FFFFFF | Texto sobre rojo (contraste 5,95:1) |
| secondary | Negro | #000000 | Encabezado, pie de página, botones secundarios y texto de titulares oscuros |
| on-secondary | Blanco | #FFFFFF | Texto sobre negro (contraste 21:1) |
| tertiary | Gris acero | #595959 | Iconos, bordes, textos de apoyo y detalles (contraste 7:1 sobre blanco) |
| on-tertiary | Blanco | #FFFFFF | Texto sobre gris acero |
| neutral | Blanco | #FFFFFF | Fondo de las páginas y de las tarjetas |
| surface | Gris claro | #F2F2F2 | Secciones alternas, etiquetas y fondos de apoyo |
| on-surface | Gris carbón | #333333 | Párrafos y textos largos (contraste 12,6:1 sobre blanco) |
| success | Verde | #1E7B3A | Confirmación de hora agendada y mensajes de envío correcto |
| error | Burdeos | #8C1C20 | Errores de formulario, siempre con icono y texto |

El rojo sobre negro tiene un contraste de 3,5:1, por lo que solo se usa en texto grande. El rojo sobre blanco tiene 5,95:1 y cumple AA en cualquier tamaño.

## Typography

- **Títulos principales (h1):** Playfair Display en negrita (900) y cursiva, por su parecido con la cursiva serif roja de las publicaciones.
- **Subtítulos (h2, h3) y botones:** Barlow Condensed en 700, por su parecido con los titulares condensados negros del Instagram.
- **Textos:** Barlow en 400, legible en celular.
- **Carga:** fuentes de Google Fonts con `font-display: swap` y respaldo (Georgia para Playfair Display, Arial Narrow para Barlow Condensed y Arial para Barlow).

| Elemento | Token | Desktop | Mobile |
|---|---|---|---|
| h1 | headline-display | 56px | 36px |
| h2 | headline-lg | 40px | 28px |
| h3 | headline-md | 28px | 22px |
| Párrafo | body-lg | 18px | 16px (body-md) |
| Botón | label-md | 18px | 16px |

El front matter guarda los valores de desktop; el cambio a mobile ocurre en el breakpoint de 768px. La cursiva del h1 no es una propiedad del front matter, así que se aplica en el CSS.

## Layout

- **Contenedor:** ancho máximo de 1200px, centrado, con 16px de margen lateral en mobile y 24px en desktop.
- **Breakpoint:** 768px (mobile primero). Se revisa a 375px y a 1440px.
- **Grillas:** servicios en 4 columnas en desktop y 2 en mobile; tarjetas de tienda y blog en 3 columnas en desktop y 1 en mobile; reseñas en 3 columnas y 1 en mobile.
- **Espaciado:** escala xs 4, sm 8, md 16, lg 24, xl 32, 2xl 48 y 3xl 64. Entre secciones se usa 2xl (48px) en desktop y xl (32px) en mobile; dentro de una tarjeta, md (16px).
- **Navegación:** navbar negro con logo, menú y botón de WhatsApp siempre visible; en mobile, menú hamburguesa.
- **Botones:** en mobile, los principales ocupan todo el ancho; en la ficha de servicio, "Agregar y agendar" queda fijo abajo.

## Elevation & Depth

El diseño es plano, sin sombras. La jerarquía se logra con contraste de color (bandas negras, fondos grises claros) y con bordes de 2px en negro o gris acero. La barra fija de la ficha de servicio se separa del contenido con un borde superior de 1px. El foco de teclado se muestra con un contorno de 3px en negro y 2px de separación, visible sobre blanco y sobre rojo.

## Shapes

- **Botones, tarjetas e inputs:** esquinas de 6px (`md`).
- **Etiquetas:** forma de píldora (`full`).
- **Imágenes:** esquinas de 6px (`md`).
- **Logo:** circular, como el avatar de Instagram.

## Components

- **Navbar:** fondo negro, logo "Rocky's Garage", enlaces Servicios, Blog, Nosotros y Contacto, y botón de WhatsApp con borde blanco.
- **Botón primario:** fondo rojo, texto blanco, 12px 24px; en hover, rojo oscuro.
- **Botón secundario:** fondo blanco, texto y borde negros de 2px; en hover, fondo gris claro.
- **Hero:** título h1 en cursiva, una línea de apoyo, selector de marca, modelo y año, y botón primario "Agendar hora".
- **Tarjeta de servicio:** foto o ilustración, nombre, precio "desde", duración, garantía y botón "Ver servicio".
- **Selector de auto:** tres campos (marca, modelo y año) con etiqueta visible y precio estimado debajo.
- **Reseña:** estrellas rojas, comentario, nombre del cliente y servicio realizado.
- **Antes y después:** dos fotos reales del mismo trabajo, con leyenda.
- **Preguntas frecuentes:** acordeón con `<details>` y `<summary>`, sin JavaScript.
- **Formulario:** cada campo con su etiqueta, mensaje de error en burdeos con icono y botón primario "Enviar".
- **Footer:** fondo negro con contacto, ubicación (Villa Alemana, V región), aviso de servicio a domicilio, Instagram y enlaces legales.

## Do's and Don'ts

**Do**

- Usa el rojo solo para la acción principal de cada pantalla y para los títulos destacados.
- Muestra fotos reales del taller, de las piezas y de los trabajos.
- Escribe títulos y botones con frases cortas y claras, como "Agendar hora".
- Mantén un solo botón primario por pantalla visible a la vez.
- Revisa el contraste de cada combinación nueva (mínimo AA).

**Don't**

- No uses texto rojo pequeño sobre fondo negro.
- No agregues colores nuevos ni gradientes; la marca es blanco, rojo y negro.
- No uses sombras ni esquinas muy redondeadas en botones y tarjetas.
- No dependas solo del color para indicar un error o un éxito; agrega icono y texto.
- No pongas párrafos largos en Barlow Condensed, que es solo para títulos, botones y etiquetas.