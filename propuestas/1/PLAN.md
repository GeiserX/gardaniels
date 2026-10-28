# Propuesta 1: «Cuaderno de campo»

La web como un cuaderno de campo de un técnico forestal: fichas precisas, papel de herbario, tinta de pino. El mandala es lo único que se permite lucirse.

## Paleta

| Nombre | Hex | Uso |
|---|---|---|
| Pinar | `#13301F` | Tinta principal, bandas oscuras (portada, contacto, pie) |
| Herbario | `#EFF3E8` | Fondo de página: papel verdoso de pliego de herbario, no crema |
| Pliego | `#E2EAD6` | Superficie de las fichas y del bloque «Conócenos» |
| Mandala | `#76B42D` | El verde del logo, solo en marcas y sobre Pinar (nunca texto sobre claro) |
| Musgo | `#2F5D1E` | Enlaces y acentos sobre claro (6,9:1 sobre Herbario) |
| Agua | `#1D5E6B` | Solo la ficha de piscinas: la única entrada que no es planta |

Modo oscuro: fondo `#0E1F14`, superficie `#16291C`, texto `#E6ECDD`, acento `#9CCB5A`, agua `#7CC3CF`. El mandala cambia la tinta negra por `#E6ECDD` (SVG con `currentColor`).

## Tipografía

- **Alegreya** (Huerta Tipográfica, OFL), variable, para titulares, nombres de servicio, citas y el teléfono grande. Es una romana caligráfica pensada para textos literarios largos: tiene trazo de pluma, encaja con un cuaderno escrito a mano sin caer en una «fuente manuscrita».
- **Alegreya Sans** 400/700 para el texto corrido, botones y datos. Misma familia, contraste claro serif/sans.
- Escala 1,25: 16 · 20 · 25 · 31 · 39 · 49 · 61 px. Titulares en peso 500, no negrita. Texto a 17-18 px, interlineado 1,55, medida máxima 64 caracteres.

## Maquetación

```
┌──────────────────────────────────────────────────────────┐
│ (m) Gardaniel's      Servicios Conócenos Opiniones  [Llamar]│  cabecera fina, Herbario
├──────────────────────────────────────────────────────────┤
│ PINAR                                                     │
│  Tu jardín,                               .-~~~-.         │
│  nuestro compromiso.                    (  MANDALA )      │  mandala grande en tinta clara,
│  texto de portada                         '-~~~-'  ←sale  │  se sale por la derecha
│  [Llamar] [Escribir por WhatsApp] Ver servicios           │
│  nota al margen: Daniel Baños · Técnico Sup. Gestión Forestal │
├──────────────────────────────────────────────────────────┤
│ Servicios                                                 │
│ índice de 7 entradas (enlaces)                            │
│ ┌ficha──────────────────────────────────────────────────┐ │
│ │ [glifo] Podas en altura   │ texto                      │ │  nombre a la izquierda,
│ │                           │ ✿ ventaja ✿ ventaja ✿ ...  │ │  texto y ventajas a la derecha
│ └───────────────────────────────────────────────────────┘ │
│  ... ×7 (piscinas en Agua)                                │
├──────────────────────────────────────────────────────────┤
│ Conócenos: texto  │ ficha técnica <dl> (titular, formación,│
│                   │ oficio desde, zona, horario) + valores │
├──────────────────────────────────────────────────────────┤
│ Cómo trabajamos  1 ── 2 ── 3 ── 4   (sí es una secuencia)  │
├──────────────────────────────────────────────────────────┤
│ Opiniones: tres citas en Alegreya cursiva                 │
├──────────────────────────────────────────────────────────┤
│ Trabajos: láminas (rejilla de 6 fotos con pie)            │
├──────────────────────────────────────────────────────────┤
│ PINAR  Contacto: 677 768 231 enorme, [Llamar] [WhatsApp] [Correo] │
│ Pie: mandala pequeño, ©, enlaces legales                  │
└──────────────────────────────────────────────────────────┘
 móvil: barra fija inferior [Llamar | WhatsApp]
```

Alineación a la izquierda en todo; nada centrado salvo el mandala. Las fichas usan una columna estrecha para el nombre y una ancha para el texto, como una entrada de guía de campo.

## Principios

1. El mandala es el gesto: grande en la portada, pequeño como sello en cabecera, pie y firma de cada opinión. Las ventajas llevan una hoja, no el mandala: a 18 px el mandala se vuelve una mancha. Un único movimiento: gira y se abre una vez al cargar.
2. La estructura dice algo: un índice porque son siete entradas consultables; números solo en «Cómo trabajamos», que sí es un orden; un `<dl>` para los datos de Dani porque son pares dato-valor.
3. Llamar está siempre a un toque: cabecera, portada, contacto y barra fija en móvil.
4. Nada que Dani no haya dicho: ni cifras inventadas ni contadores. Fotos de banco solo en «Trabajos», hasta que haya fotos reales.

## Revisión contra el brief y los defaults

- **Antes:** portada con foto de jardín a sangre y titular encima. **Ahora:** portada sin foto, el mandala como protagonista. La foto de banco es lo genérico; el mandala es lo único que es de Gardaniel's.
- **Antes:** servicios numerados 01-07 con etiqueta en mayúsculas encima de cada sección. **Ahora:** sin numeración (no es una secuencia) y sin etiquetas sobre los titulares; un índice enlazado y un glifo dibujado por servicio.
- **Antes:** tarjetas iguales con sombra para los servicios. **Ahora:** fichas a todo el ancho con columna de nombre, sin sombras; la de piscinas cambia a Agua para marcar que es otro oficio.
- **Antes:** fondo crema. **Ahora:** Herbario `#EFF3E8`, un papel con tinte verde, y bandas Pinar para portada y contacto.
- Evitados: puntos medios entre metadatos (el pie es una lista), flechas en botones, monoespaciada, versalitas de adorno.
- **Tras la primera captura:** el titular llevaba «nuestro compromiso.» en cursiva verde. Es el tic de resaltar media frase; ahora el titular va en un solo color y el verde se queda en el mandala.
- **Tras la primera captura:** el contorno de foco en verde Mandala no llegaba a 3:1 sobre Herbario; ahora es Musgo sobre claro y Mandala sobre las bandas oscuras.
