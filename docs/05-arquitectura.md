# Arquitectura de la información — [Rocky´s Garage]

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

<!-- Incluye landing, blog, tienda y las páginas obligatorias:
contacto, preguntas frecuentes, términos, privacidad y 404. -->

```text
Inicio (landing)
├── Tienda
│   ├── Categoría: Diagnóstico con scanner
│   ├── Categoría: Embrague y transmisión
│   ├── Categoría: Mantención ligera
│   ├── Categoría: Frenos y suspensión
│   ├── Ficha de servicio
│   ├── Carrito
│   ├── Agendar hora
│   └── Confirmación y presupuesto
├── Blog
│   ├── Categoría: Diagnóstico y luces del tablero
│   ├── Categoría: Embrague
│   ├── Categoría: Mantención básica
│   └── Artículo
├── Nosotros (taller, equipo y trabajos realizados)
├── Estado de mi auto (Futuro)
├── Contacto
├── Preguntas frecuentes
├── Términos y condiciones
├── Política de privacidad
└── 404
```

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: compra

```compra

```text
Felipe busca "taller mecánico cerca" en Google o ve un video del taller en Instagram
        ↓
Inicio (landing)
        ↓
Tienda  →  busca por síntoma ("el embrague patina") o filtra por categoría
        ↓
Ficha de servicio
        ↓
Elige marca, modelo y año de su auto  →  ve el precio estimado
        ↓
¿Le sirve el precio?
   ├── No  →  vuelve a la Tienda o consulta por WhatsApp
   └── Sí  →  "Agregar" al Carrito
                    ↓
               Carrito (resumen y total)
                    ↓
               Agendar hora (elige día y horario)
                    ↓
               Confirmación y presupuesto
               (recibe el presupuesto por escrito en WhatsApp o correo)

```

### Flujo 2: contenido

```contenido

```text
Felipe ve una luz encendida en el tablero y busca en Google "luz check engine parpadea"
        ↓
Artículo del blog: "Qué significa la luz check engine y cuándo es urgente"
        ↓
Lee y entiende qué le pasa a su auto
        ↓
¿Qué hace después?
   ├── Comparte el artículo por WhatsApp
   ├── Deja un comentario con su duda
   └── Hace clic en "Agenda tu diagnóstico con scanner"
                    ↓
               Ficha de servicio (Diagnóstico con scanner)
                    ↓
               Carrito  →  Agendar hora  →  Confirmación y presupuesto
```

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

| Categoría | Productos |
|---|---|
| Diagnóstico con scanner | Diagnóstico computarizado con scanner, revisión de luz check engine, revisión antes de comprar un auto usado |
| Embrague y transmisión | Cambio de kit de embrague, revisión de embrague (patina o pedal duro), cambio de aceite de caja |
| Mantención ligera | Cambio de aceite y filtros, cambio de bujías, revisión de niveles y batería |
| Frenos y suspensión | Cambio de pastillas de freno, cambio de discos, revisión de amortiguadores |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de la proto-persona | Producto relacionado |
|---|---|---|---|
| Diagnóstico y luces del tablero | Qué significa la luz check engine y cuándo es urgente | Entender qué le pasa al auto y evitar quedar botado | Diagnóstico con scanner |
| Diagnóstico y luces del tablero | Qué es un diagnóstico con scanner y qué debe entregarte el taller | Confiar en que no le cobren de más por no saber de autos | Diagnóstico con scanner |
| Embrague | 5 señales de que tu embrague está fallando | Detectar el problema antes de quedar botado en plena ruta | Revisión de embrague |
| Embrague | Cuánto cuesta cambiar el embrague y de qué depende el precio | Saber cuánto le va a costar y pagar un precio justo | Cambio de kit de embrague |
| Mantención básica | Cada cuántos kilómetros cambiar el aceite y los filtros | Cuidar el auto que usa para trabajar y no gastar de más | Cambio de aceite y filtros |
| Mantención básica | Qué revisar en tu auto antes de salir a ruta | Evitar un imprevisto frente a un cliente o en un viaje | Revisión de niveles y batería |
