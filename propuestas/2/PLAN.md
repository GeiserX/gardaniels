# Propuesta 2: «Directo al móvil»

Quien busca a Dani lo hace con el móvil en la mano, delante de una palmera que ha crecido demasiado o de una piscina verde. La página tiene un solo trabajo: que llame o escriba por WhatsApp en segundos, y que antes de hacerlo vea que es de fiar.

## Color

| Nombre | Hex | Uso |
|---|---|---|
| Pinar | `#183F2C` | Fondo del hero y del contacto, titulares sobre claro |
| Limón | `#F5C518` | Solo el botón de llamar y la barra fija del móvil |
| Cal | `#F6F7F2` | Fondo general (blanco de pared encalada, frío, no crema) |
| Pizarra | `#25322B` | Texto corrido |
| Salvia | `#DDE6DA` | Separadores de la lista de servicios, fondo de opiniones |

Oscuro: fondo `#0F271C` (pino de noche, verde claro, no negro), texto `#E8EEE7`, Salvia pasa a `#1C3B2D`; Limón no cambia.

El amarillo limón sale de la huerta murciana y es el único color que grita: si algo es amarillo, es para llamar.

## Tipografía

Una sola familia, Archivo (variable, OFL), usada en dos anchos muy distintos:

- Titulares y el número de teléfono: Archivo a 900 de peso y 68 % de ancho, compacta como un rótulo de furgoneta de trabajo. Interlineado 0,92.
- Texto corrido: Archivo a 400, ancho 100 %, 17-18 px, interlineado 1,55, líneas de menos de 70 caracteres.

Escala aproximada 1,25 en móvil y 1,333 en escritorio. Sin mayúsculas sostenidas, sin etiquetas encima de los titulares.

## Maquetación

Móvil (el diseño de referencia):

```
+-----------------------------+
| (logo) Gardaniel's   Llamar |  cabecera fina
+-----------------------------+
| foto: poda de palmera       |
|                             |
| Tu jardín,                  |  titular condensado, enorme
| nuestro compromiso.         |
| texto breve                 |
| [ Llamar  677 768 231 ]     |  limón, ancho completo
| [ Escribir por WhatsApp ]   |  blanco
|   Ver servicios             |
+-----------------------------+
| Servicios                   |
| Podas en altura          +  |  lista desplegable (<details>)
|   ventajas en una línea     |
| Trasplantes              +  |
| ...                         |
+-----------------------------+
| «Gran profesional...»       |  opiniones, citas grandes
|  Antonia                    |
+-----------------------------+
| Conócenos / Cómo trabajamos |  1-4 es una secuencia real
| Trabajos: tira deslizable   |
| Contacto: 677 768 231 gigante
+-----------------------------+
[ Llamar ][ WhatsApp ]           barra fija abajo
```

Escritorio: el hero se parte en dos, texto sobre Pinar a la izquierda y la foto vertical a sangre a la derecha. Servicios con el titular fijo a la izquierda y la lista a la derecha. Todo alineado a la izquierda; nada centrado salvo la barra fija.

## Principios

1. Una sola cosa memorable: el número de teléfono escrito en grande con la letra condensada, en el botón del hero y como titular del contacto. Se puede leer, recordar y tocar.
2. Los servicios son una lista para escanear, no tarjetas: el nombre, sus tres ventajas en una línea y el texto completo al desplegar.
3. Las opiniones suben justo después de los servicios: son la prueba de confianza antes de llamar.
4. Sin animaciones de entrada. Solo se mueve lo que la persona toca (el signo + al desplegar un servicio).
5. Botones de 56 px de alto como mínimo; la barra fija del móvil siempre a un pulgar de distancia.

## Revisión contra el brief y los «tics» por defecto

- Primer borrador: tarjetas redondeadas para los siete servicios con iconos. Es el kit SaaS que el brief prohíbe y obliga a hacer scroll largo en el móvil. Cambiado por la lista desplegable.
- Primer borrador: verde casi negro con acento verde lima. Es justo el par prohibido. Cambiado a un verde pino medio (Pinar) con amarillo limón.
- Primer borrador: etiquetas en mayúsculas («SERVICIOS», «OPINIONES») encima de cada titular. Quitadas: el titular ya dice qué es la sección.
- Primer borrador: pasos de «cómo trabajamos» y servicios numerados por igual. Ahora solo los pasos llevan número, porque son lo único que es una secuencia.
- El pie del contenido usa puntos medios entre enlaces; se maqueta como una lista de enlaces normal.
- Orden: las opiniones van antes de «Conócenos» para que la confianza llegue pronto. El resto sigue el orden del contenido.
