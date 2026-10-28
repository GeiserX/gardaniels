# Propuesta 3 · «Jardín y agua»

Plan de diseño. El sujeto: un jardinero de Cartagena que también cuida piscinas. Su público: vecinos de casas y chalés de la costa de Murcia que buscan a alguien de confianza y quieren llamarle ya. El trabajo de la página: que llamen o escriban por WhatsApp.

## Idea

Los dos oficios de Dani son la estructura de la página. Una costura vertical separa jardín y agua en la portada: a la izquierda palmeras contra el cielo, a la derecha el agua de una piscina. Esa misma costura vuelve en los servicios (seis de jardín, uno de piscina, cada mundo con su color) y en el contacto (llamar a un lado, escribir al otro). Mucho aire, luz de cal blanca, nada de decoración que no diga algo.

## Color

| Nombre | Claro | Oscuro | Uso |
|---|---|---|---|
| Cal | `#F6F7F4` | `#0F1C19` | Fondo. Blanco frío de pared encalada, no crema. |
| Pino | `#17302A` | `#E6EDE9` | Texto. Verde casi negro, sale del negro del logo. |
| Hoja | `#3D7520` | `#9BD067` | Mundo jardín: enlaces, botón de llamar, títulos de jardín. Derivado del verde del mandala (`#7DB53A`), oscurecido para AA. |
| Agua | `#0B6874` | `#62CDD8` | Mundo piscina: botón de WhatsApp, banda de piscina, enlaces de agua. |
| Agua clara | `#DDF1F2` | `#123A3E` | Superficie de la banda de piscina y del contacto. |
| Grava | `#E2E5E0` | `#1B2B27` | Bordes y fondos neutros (grava, piedra). |

El verde vivo del logo (`#7DB53A`) solo aparece en el propio logo y en la costura; nunca en texto.

## Tipografía

Una sola familia, **Archivo** (variable, ejes de peso y anchura, OFL, autoalojada). La anchura es la herramienta expresiva: titulares en Archivo expandido (`wdth 125`, peso 640), anchos y bajos como un horizonte o la lámina de agua; cuerpo en anchura normal (`wdth 100`, peso 400). Sin cursivas de acento, sin mayúsculas de etiqueta.

Escala de tercera mayor (1,25) sobre 18 px: 14,4 · 18 · 22,5 · 28 · 35 · 44 · 55 · 69 px. Cuerpo 18/1,6, línea máxima 62 caracteres.

## Maquetación

Alineación a la izquierda en todo; solo los números de teléfono grandes y los pasos se alinean a su columna. Retícula de 12 columnas, márgenes laterales amplios (`clamp(20px, 5vw, 72px)`).

```
ESCRITORIO
┌──────────────────────────────────────────────────────┐
│ (mandala) Gardaniel's      Servicios Trabajos Contacto│
│                                     [Llamar]          │
├──────────────────────────┬┬──────────────────────────┤
│                          ││                          │
│   palmeras (jardín)      ││    agua (piscina)        │  ← costura verde de 6 px
│                          ││                          │
│ Jardín                   ││                 Piscina  │
├──────────────────────────┴┴──────────────────────────┤
│ Tu jardín, nuestro compromiso.   (expandido, 69 px)  │
│ párrafo de portada            [Llamar][WhatsApp][Ver]│
├──────────────────────────────────────────────────────┤
│ Servicios                                            │
│ En el jardín                                         │
│  Podas en altura          Trasplantes                │
│  texto + 3 ventajas       texto + 3 ventajas   (×6)  │
│ ┌──────────── banda agua clara ───────────────────┐ │
│ │ En la piscina                                    │ │
│ │ Mantenimiento de piscinas      [foto piscina]    │ │
│ └──────────────────────────────────────────────────┘ │
├──────────────────────────────────────────────────────┤
│ Conócenos: texto  |  mandala grande + 4 valores      │
├──────────────────────────────────────────────────────┤
│ Cómo trabajamos  1 ── 2 ── 3 ── 4   (línea de agua)  │
├──────────────────────────────────────────────────────┤
│ Opiniones: tres citas en columnas                    │
├──────────────────────────────────────────────────────┤
│ Trabajos: mosaico de 5 fotos de tamaños distintos    │
├──────────────────────────┬┬──────────────────────────┤
│ Llámanos                 ││ Escríbenos               │
│ 677 768 231 (grande)     ││ WhatsApp · correo        │
├──────────────────────────┴┴──────────────────────────┤
│ pie: © Gardaniel's, avisos legales                   │
└──────────────────────────────────────────────────────┘

MÓVIL (360–760 px)
┌────────────────┐
│ (m) Gardaniel's│
├───────┬┬───────┤  las dos fotos siguen lado a lado, más bajas
│ palm. ││ agua  │
├───────┴┴───────┤
│ Titular        │
│ párrafo        │
│ [Ver servicios]│
│ …secciones…    │
╞════════════════╡
│[Llamar][WhatsApp]  barra fija abajo, siempre visible
└────────────────┘
```

## Principios

1. **Dos mundos, una costura.** Verde = jardín, agua = piscina, siempre con el mismo significado. Ningún color se usa de adorno.
2. **El gesto memorable es la portada partida.** Todo lo demás es tranquilo: texto bien compuesto, reglas finas, fotos sin marcos ni sombras.
3. **Contactar está a un toque.** Llamar y WhatsApp en la portada, en el contacto y en una barra fija en móvil.
4. **Un solo movimiento.** Al cargar, las dos fotos se abren desde la costura hacia fuera (0,9 s). Con `prefers-reduced-motion` no se mueve nada.
5. **Contenido real.** Todos los textos salen de `content/contenido.md`; sin cifras, premios ni precios inventados.

## Revisión frente al brief y a los patrones por defecto

Primer borrador y lo que cambié:

- **Serif de titular (Fraunces) sobre crema.** Es el patrón por defecto número 1. Lo cambié por Archivo expandido sobre cal fría: más mediterráneo moderno (rótulo, horizonte) y una sola familia.
- **Siete tarjetas iguales con icono para los servicios.** Kit SaaS. Lo cambié por la división real del negocio: seis servicios de jardín como texto en dos columnas con regla verde, y la piscina en su propia banda de agua con foto. La estructura dice algo: qué es jardín y qué es agua.
- **Separadores de ola en SVG entre secciones.** Cliché de web de piscinas y decoración pura. Eliminados; la única «línea de agua» es la que une los cuatro pasos, porque esos pasos sí son una secuencia.
- **Etiquetas en mayúsculas encima de cada título («SERVICIOS», «OPINIONES»).** Eliminadas; el título basta. Las únicas etiquetas que quedan son «Jardín» y «Piscina» sobre las fotos de portada, porque dicen qué es cada mitad.
- **Contadores («+10 años», «+500 clientes»).** Fuera: el brief los prohíbe y el «más de 10 años» ya está en el texto.
- **Animaciones de entrada en cada sección.** Fuera; solo queda la apertura de la portada.

## Revisión tras ver las capturas

- La portada dejaba un hueco grande a la derecha del titular: ahora el titular va a la izquierda y la entrada con los botones a la derecha.
- Las ventajas de cada servicio se partían en 2 + 1 de forma torpe: ahora van en columna.
- En «Cómo trabajamos» el texto tras la negrita empezaba con una coma en otra línea: la negrita va en línea con el resto de la frase.
- Las reglas entre secciones se salían del margen: ahora se dibujan dentro de la retícula. Menos espacio vertical entre secciones.
- Los valores alternaban verde y agua sin significado: ahora todos en verde hoja.
