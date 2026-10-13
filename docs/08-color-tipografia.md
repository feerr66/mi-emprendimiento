# Color y tipografía — [Rocky's Garage]

> Guía: [Color y tipografía](../evaluacion/guias/fase-2-specs/05-color-y-tipografia.md)

## Paleta

| Rol | Color | HEX | Uso |
|---|---|---|---|
| Principal | Rojo Rocky | #BE282B | Logo RG, botones principales ("Agendar hora"), títulos destacados y enlaces |
| Secundario | Negro | #000000 | Encabezado, pie de página, botones secundarios y titulares oscuros |
| Acento | Gris acero | #595959 | Iconos, bordes, textos de apoyo y detalles (tomado del gris de las bujías del logo) |
| Fondo | Blanco | #FFFFFF | Fondo de las páginas, como en las publicaciones de Instagram; gris claro #F2F2F2 para secciones alternas |
| Texto | Gris carbón | #333333 | Párrafos y textos largos |
| Éxito | Verde | #1E7B3A | Confirmación de hora agendada y mensajes de envío correcto |
| Error | Burdeos | #8C1C20 | Mensajes de error en formularios, siempre con icono y texto |
## Contraste

| Combinación | Ratio | Resultado |
|---|---|---|
| Negro #000000 sobre Blanco #FFFFFF | 21:1 | Cumple AAA |
| Gris carbón #333333 sobre Blanco #FFFFFF | 12,6:1 | Cumple AAA |
| Blanco sobre Rojo #BE282B (texto de botones) | 6,0:1 | Cumple AA |
| Rojo #BE282B sobre Blanco (títulos y enlaces) | 6,0:1 | Cumple AA |
| Blanco sobre Negro (encabezado y pie) | 21:1 | Cumple AAA |
| Gris acero #595959 sobre Blanco | 7,0:1 | Cumple AAA |
| Verde #1E7B3A sobre Blanco | 5,3:1 | Cumple AA |
| Burdeos #8C1C20 sobre Blanco | 9,1:1 | Cumple AAA |
| Rojo #BE282B sobre Negro | 3,5:1 | Solo texto grande; no usar en párrafos ni textos pequeños |

## Tipografía

- **Títulos:** Playfair Display en negrita cursiva (h1), por su parecido con la cursiva serif roja de "Servicios" en tus publicaciones; Barlow Condensed en negrita (h2, h3 y botones), por su parecido con los titulares condensados negros como "Mantenciones generales".
- **Textos:** Barlow en peso regular, legible en celular.
| Elemento | Desktop | Mobile | Peso |
|---|---|---|---|
| h1 | 56 px | 36 px | 900 cursiva (Playfair Display) |
| h2 | 40 px | 28 px | 700 (Barlow Condensed) |
| h3 | 28 px | 22 px | 700 (Barlow Condensed) |
| Párrafo | 18 px | 16 px | 400 (Barlow), interlineado 1,6 |
| Botón | 18 px | 16 px | 700 (Barlow Condensed) |

## Justificación
La paleta y el estilo salen del Instagram del taller (rg.automotriz_), para que quien llegue desde las redes reconozca de inmediato la misma marca en el sitio: el logo RG en rojo sobre fondo blanco, los títulos rojos en cursiva y los textos negros en letra condensada. El rojo se usa solo para lo que debe llamar la atención (botón "Agendar hora", logo y títulos principales), y el negro y el blanco dan orden y descanso visual, de modo que Felipe encuentre rápido el botón de reservar desde el celular. Todos los textos cumplen contraste AA o mejor, y el rojo sobre negro se limita a texto grande. Las dos familias (Playfair Display y Barlow) son gratuitas en Google Fonts, así que funcionan con HTML y CSS en GitHub Pages sin instalar nada. El error usa un burdeos distinto al rojo de la marca, y siempre va con icono y texto, para que no se confunda con un botón normal.