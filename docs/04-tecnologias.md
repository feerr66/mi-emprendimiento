# Tecnologías del proyecto — [Rocky´s Garage]

> Guía: [Tecnologías del proyecto](../evaluacion/guias/fase-1-requerimientos/04-tecnologias.md)

## Stack

| Área | Herramienta | Para qué la uso |
|---|---|---|
| Construcción | HTML + CSS | Maquetar las páginas de Rocky's Garage (inicio, servicios, blog) sin depender de un gestor de contenido |
| Versionado | Git y GitHub | Guardar el avance del sitio con commits y tener el proyecto en la nube |
| Publicación | GitHub Pages | Publicar el sitio gratis con una URL pública para que los clientes lo vean |
| Diseño | Whimsical | Armar el moodboard del taller y los wireframes de la reserva de hora y de la ficha de servicio |
| Diseño | Google Stitch | Generar el prototipo en alta fidelidad a partir de las funcionalidades y de la proto-persona Felipe |
| IA | Claude | Definir la proto-persona, redactar las funcionalidades y revisar mis documentos |
| Editor | [tu editor] | Escribir el código del sitio |

## Qué es funcional y qué es prototipo

| Funcionalidad | Estado en esta versión |
|---|---|
| Navegación entre inicio, servicios y blog | Funcional |
| Ver detalle de un servicio (scanner, embrague, mecánica ligera) con duración y garantía | Funcional |
| Consultar por WhatsApp con mensaje prellenado ("Hola, quiero cotizar un cambio de embrague") | Funcional (enlace a wa.me) |
| Compartir un artículo (por ejemplo, "qué significa la luz check engine") | Funcional (enlaces para compartir) |
| Navegar artículos por categoría (embrague, scanner, mantención) | Funcional (una página por categoría) |
| Galería de trabajos reales del taller con fotos de antes y después | Funcional (imágenes estáticas) |
| Reseñas de clientes | Funcional (contenido fijo) |
| Formulario para dejar marca, modelo y WhatsApp y pedir cotización | Prototipo visual |
| Buscador y filtros de servicios por síntoma, categoría o precio | Prototipo visual |
| Elegir marca, modelo y año del auto y ver precio estimado | Prototipo visual |
| Agendar una hora eligiendo servicio, día y horario | Prototipo visual |
| Presupuesto por escrito antes de intervenir el auto | Prototipo visual |
| Comentarios del blog | Prototipo visual |
| Seguimiento del estado del auto en el taller | Prototipo visual |
## Integraciones para una versión real

- Agenda de horas: Calendly, Cal.com o Google Calendar, para que Felipe reserve sin llamar.
- Cotización: Formspree o Netlify Forms para recibir marca, modelo y WhatsApp del cliente en el correo del taller.
- Precio estimado: JavaScript con una tabla de precios por servicio, marca, modelo y año.
- Presupuesto y seguimiento: WhatsApp Business API para enviar el presupuesto por escrito y avisar cuando el auto esté listo para retirar.
- Pago de anticipo: Mercado Pago o Webpay para asegurar la hora.
- Reseñas: widget de Google Reviews con las opiniones reales de los clientes del taller.
- Comentarios del blog: Giscus o Disqus.

## Restricciones

- **Plazo:** 2 semanas para la entrega del prototipo o menos.
- **Marca:** Rocky's Garage: debe reflejar profesionalismo, confianza y transparencia.
- **Dispositivos:** El sitio debe ser responsive y funcionar correctamente en desktop, tablet y móvil.
