# Spec de diseño — [Rocky's Garage]

> Guía: [Spec de diseño](../evaluacion/guias/fase-2-specs/06-spec-de-diseno.md)

La spec de diseño tiene dos partes:

1. **[`DESIGN.md`](../DESIGN.md)** (en la raíz): tu design system, en el formato que Stitch importa.
2. **Este documento:** tus pantallas, escritas como prompts listos para pegar en Stitch.

**Wireframes en Whimsical:** https://whimsical.com/rocky-s-garage/E5piis7vAyGkH3htSjKHig

## Pantallas

### 1. Landing

```text
Pantalla: Landing de Rocky's Garage, versión desktop. Usa el design system del proyecto.
Objetivo: que quien llega entienda en segundos qué servicios ofrece el taller, vea el precio para su auto y pueda agendar una hora sin llamar.
Componentes, de arriba hacia abajo:
1. Navbar: fondo negro con logo RG y "Rocky's Garage", menú (Servicios, Blog, Nosotros, Contacto) y botón "WhatsApp" siempre visible.
2. Hero: título "Agenda tu hora sin llamar" en cursiva serif, una línea de apoyo, selector de marca, modelo y año, y botón rojo "Agendar hora".
3. Servicios: cuatro tarjetas (Diagnóstico con scanner, Embrague y transmisión, Mantención ligera, Frenos y suspensión) con ilustración, precio "desde" y botón "Ver servicio".
4. Cómo funciona: tres pasos (Elige el servicio, Agenda tu hora, Recibe tu presupuesto por escrito).
5. Trabajos reales: galería de fotos de antes y después.
6. Reseñas: tres reseñas de clientes con estrellas rojas.
7. Del blog: dos tarjetas de artículo, cada una con botón al servicio relacionado.
8. Formulario de cotización: nombre, WhatsApp, marca y modelo del auto, botón "Enviar" y enlace a la política de privacidad.
9. Footer: fondo negro con contacto, ubicación (Villa Alemana, V región), aviso de servicio a domicilio, Instagram, preguntas frecuentes, términos y privacidad.
```

### 2. Tienda

```text
Pantalla: Tienda de Rocky's Garage, versión desktop. Usa el design system del proyecto.
Objetivo: que el cliente encuentre el servicio que necesita, buscando por nombre o por síntoma o filtrando por categoría, y llegue a su ficha.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Título "Servicios" y buscador con el texto "Busca por servicio o síntoma, por ejemplo: el embrague patina".
3. Categorías como botones: Diagnóstico con scanner, Embrague y transmisión, Mantención ligera, Frenos y suspensión.
4. Filtros por rango de precio y duración.
5. Grilla de tarjetas de servicio en tres columnas: ilustración o foto, nombre, precio "desde", duración y botón "Ver servicio".
6. Bloque "¿No sabes qué necesita tu auto?" con botón "Pide tu cotización".
7. Footer.
```

### 3. Ficha de servicio

```text
Pantalla: Ficha de servicio de Rocky's Garage, versión desktop. Usa el design system del proyecto.
Objetivo: que el cliente entienda qué incluye el servicio, vea el precio estimado para su auto y confíe lo suficiente para agendar.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Ruta de navegación: Tienda, categoría y nombre del servicio.
3. Título del servicio y foto principal del trabajo.
4. Datos clave: precio "desde", duración y garantía.
5. Selector de marca, modelo y año, con el precio estimado para ese auto.
6. Qué incluye el servicio, en una lista corta.
7. Reseñas de clientes de este servicio.
8. Preguntas frecuentes en acordeón.
9. Botón rojo "Agregar y agendar", que queda fijo al bajar por la página.
10. Footer.
```

### 4. Carrito

```text
Pantalla: Carrito de Rocky's Garage, versión desktop. Usa el design system del proyecto.
Objetivo: que el cliente revise los servicios elegidos y el total, sepa que recibirá el presupuesto por escrito y pase a agendar su hora.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Título "Tu solicitud".
3. Lista de servicios agregados, cada uno con el auto elegido, el precio y un botón para quitarlo.
4. Resumen con el total y la duración estimada.
5. Aviso: "Recibirás el presupuesto por escrito antes de que intervengamos tu auto".
6. Botón rojo "Agendar hora" y enlace "Seguir viendo servicios".
7. Footer.
```

### 5. Blog

```text
Pantalla: Blog de Rocky's Garage, versión desktop. Usa el design system del proyecto.
Objetivo: que el cliente entienda qué le pasa a su auto con artículos simples y dé el paso hacia el servicio relacionado.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Título "Entiende tu auto" con una línea de apoyo.
3. Categorías: Diagnóstico y luces del tablero, Embrague y Mantención básica.
4. Artículo destacado con imagen grande, título y resumen.
5. Grilla de tarjetas de artículo: imagen, categoría, título, resumen y botón "Leer artículo".
6. Bloque "Agenda tu diagnóstico con scanner" con botón rojo.
7. Footer.
```

### 6. Artículo

```text
Pantalla: Artículo del blog de Rocky's Garage, versión desktop. Usa el design system del proyecto.
Objetivo: que el lector entienda su problema, pueda compartir el artículo o comentar, y siga hacia el servicio relacionado.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Ruta de navegación: Blog, categoría y título del artículo.
3. Título, categoría, fecha y autor.
4. Imagen principal.
5. Cuerpo del artículo con subtítulos y párrafos cortos.
6. Botones para compartir por WhatsApp, X y correo.
7. Bloque con botón rojo hacia el servicio relacionado, por ejemplo "Agenda tu diagnóstico con scanner".
8. Comentarios.
9. Artículos relacionados.
10. Footer.
```

## Versión mobile (para cada pantalla)

```text
Genera la versión mobile (375px de ancho) de esta pantalla siguiendo la sección Layout del design system: una sola columna, navbar con menú hamburguesa y botón de WhatsApp visible, botones a ancho completo, tarjetas en una columna (los servicios de la landing en dos columnas), títulos h1 de 36px, h2 de 28px y h3 de 22px, párrafo de 16px, y en la ficha de servicio el botón "Agregar y agendar" fijo en la parte inferior.
```
```
