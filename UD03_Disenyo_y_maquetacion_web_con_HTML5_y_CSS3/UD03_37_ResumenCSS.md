# 37. **Tabla resumen de propiedades CSS y sus valores**

Tabla de contenidos

- [37. **Tabla resumen de propiedades CSS y sus valores**](#37-tabla-resumen-de-propiedades-css-y-sus-valores)
  - [Sintaxis selector](#sintaxis-selector)
  - [Unidades de medida](#unidades-de-medida)
  - [Colores básicos](#colores-básicos)
  - [Color y fondo](#color-y-fondo)
  - [Texto](#texto)
  - [Fuentes](#fuentes)
  - [Listas](#listas)
  - [Tablas](#tablas)
  - [Modelo de cajas](#modelo-de-cajas)
  - [Pseudo-clases para selección de hijos o hermanos](#pseudo-clases-para-selección-de-hijos-o-hermanos)
  - [Pseudo-clases para los estados de un elemento](#pseudo-clases-para-los-estados-de-un-elemento)
  - [Pseudo-elementos](#pseudo-elementos)
  - [Prefijos para los navegadores](#prefijos-para-los-navegadores)

## Sintaxis selector

![Sintaxis CSS](img/Sintaxis-CSS-Selector-propiedad.png)

## Unidades de medida

|| **Longitudes relativas** |
| --- | --- |
| `px` | Píxeles (relativo al dispositivo) |
| `em` | Relativo al tamaño de la fuente del elemento ( 2em significa 2 veces el tamaño de la fuente actual) |
| `%` | Porcentaje (relativo al elemento padre) |
| `vh y vw` | Medidas relativas de acuerdo al viewport: `1vh = 1% de la altura del viewport`y `100vh = altura del viewport` |

|| **Longitudes absolutas** |
| --- | --- |
| `in` | Pulgadas (1pulgada = 2.54 cm) |
| `cm` | Centímetros |
| `mm` | Milímetros |
| `pt` | Puntos (1pt = 1/72 pulgadas) |
| `pc` | Picas (1pica = 12 puntos) |

## Colores básicos

| Color | HEX | RGB |
| ----- | --- | --- |
| `black` | #000000 | 0,0,0 |
| `white` | #ffffff | 255,255,255 |
| `red` | #ff0000 | 255,0,0 |
| `blue` | #0000ff | 0,0,255 |
| `yellow` | #ffff00 | 255,255,0 |
| `gray` | #808080 | 128,128,128 |
| `green` | #008000 | 0,128,0 |

[Ver lista completa de colores expresados por nombre, hexadecimal y en RGB](https://www.w3schools.com/cssref/css_colors.asp)

## Color y fondo

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `color` | Color del texto | RGB \| HSL \| HEX \| nombre del color \| RGBA \| HSLA |
| `background-color` | Color de fondo | url(...) \| none |
| `background-image` | Imagen de fondo | none \| underline \| overline \| line-through \| * |
| `background-repeat` | Repetición de la imagen de fondo | repeat \| repeat-x \| repeat-y \| no-repeat |
| `background-attachment` | Desplazamiento de la imagen de fondo | scroll \| fixed |
| `background-position` | Posición de la imagen de fondo | percentage \| length \| left \| center \| right |
| `Opacity**` | Transparencia de un elemento | [ 0 -- 1 ] |

## Texto

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `text-indent` | Desplazamiento de la primera línea del texto | longitud \| porcentaje |
| `text-align` | Alineamiento del texto | left \| right \| center \| justify |
| `text-decoration` | Efectos de subrayado, tachado, parpadeo | none \| underline \| overline \| line-through \| * |
| `letter-spacing` | Espacio entre caracteres | normal \| longitud |
| `word-spacing` | Espacio entre palabras | normal \| longitud |
| `text-transform` | Transformación a mayúsculas / minúsculas | capitalize \| uppercase \| lowercase \| none |
| `line-height` | Tamaño del espacio entre líneas | longitud \| porcentaje |

## Fuentes

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `font-family` | Familias de fuentes | nombre-familia \| nombre-familia-genérica \| * |
| `font-style` | Estilo de la fuente | normal \| italic \| oblique |
| `font-variant` | Convierte a mayúsculas manteniendo un tamaño inferior | normal \| small-caps |
| `font-weight` | Anchura de los caracteres. Normal = 400, Negrita = 700 | normal \| bold \| bolder \| lighter \| 100 \| 200 \| 300 \| 400 \| 500 \| 600 \| 700 \| 800 \| 900 |
| `font-size` | Tamaño de la fuente | xx-small \| x-small \| small \| medium \| large \| x-large \| xx-large \| larger \| smaller \| longitud \| porcentaje |

## Listas

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `list-style-type` | Estilo aplicable a los marcadores visuales de las listas | disc \| circle \| square \| decimal \| decimal-leading-zero \| lower-roman \| upper-roman \| lower-greek \| lower-latin \| upper-latin \| armenian \| georgian \| lower-alpha \| upper-alpha \| none |
| `list-style-image` | Imagen aplicable a los elementos de las listas | url("http://...") \| none |
| `list-style-position` | Posición dentro de la lista de los elementos marcadores de las listas | inside \| outside |
| `list-style` | Permite establecer el estilo de la lista, la imagen y/o la posición | list-style-type \| list-style-position \| list-style-image |

## Tablas

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `font-family` | Familias de fuentes | nombre-familia \| nombre-familia-genérica \| * |
| `font-style` | Estilo de la fuente | normal \| italic \| oblique |
| `font-variant` | Convierte a mayúsculas manteniendo un tamaño inferior | normal \| small-caps |
| `font-weight` | Anchura de los caracteres. Normal = 400, Negrita = 700 | normal \| bold \| bolder \| lighter \| 100 \| 200 \| 300 \| 400 \| 500 \| 600 \| 700 \| 800 \| 900 |
| `font-size` | Tamaño de la fuente | xx-small \| x-small \| small \| medium \| large \| x-large \| xx-large \| larger \| smaller \| longitud \| porcentaje |

## Modelo de cajas

![Propiedades CSS contenedores](img/Propiedades-cajas-y-contenedores-en-CSS.png)

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `padding-top` \| `padding-right` \| `padding-bottom` \| `padding-left` | Tamaño del relleno superior, derecho, inferior e izquierdo | longitud \| porcentaje |
| `padding` | Tamaño del relleno | longitud | porcentaje {1,4} |
| `margin-top` \| `margin-right` \| `margin-bottom` \| `margin-left` | Tamaño del margen superior, derecho, inferior e izquierdo | longitud \| porcentaje \| auto |
| `margin` | Ancho de los margenes | longitud \| porcentaje \| auto {1,4} |
| `border-top-width` \| `border-right-width` \| `border-bottom-width` \| `border-left-width` | Anchura del borde superior, derecho, inferior o izquierdo | thin \| medium \| thick \| longitud |
| `border-width` | Anchura del borde (reducida) | thin \| medium \| thick \| longitud {1,4} |
| `border-top-color` \| `border-right-color` \| `border-bottom-color` \| `border-left-color` | Color del borde superior, derecho, inferior e izquierdo | color \| transparent |
| `border-color` | Color del borde (reducida) | color \| transparent {1,4}|
| `border-top-style` \| `border-right-style` \| `border-bottom-style` \| `border-left-style` | Estilo del borde superior, derecho, inferior e izquierdo | none \| hidden \| dotted \| dashed \| solid \| double \| groove \| ridge \| inset \| outset |
| `border-style` | Estilo del borde (reducida) | none \| hidden \| dotted \| dashed \| solid \| double \| groove \| ridge \| inset \| outset {1,4} |
| `border-top` \| `border-right` \| `border-bottom` \| `border-left` | Ancho, estilo y color para el borde superior, derecho, inferior e izquierdo | border-top-width \| border-top-style \| border-top-color |
| `border` | Ancho, estilo y color para los bordes (reducida) | border-width \| border-style \| border-color |
| `border-radius` | Curvatura del borde | 1-4 length \| % |
| `display` | Comportamiento del contenedor | inline \| block \| list-item \| run-in \| inline-block \| table \| inline-table \| table-row-group \| table-header-group \| table-footer-group \| table-row \| table-column-group \| table-column \| table-cell \| table-caption \| none |
| `position` | Esquema de posicionamiento | static \| relative \| absolute \| fixed |
| `top` \| `right` \| `bottom` \| `left` | Desplazamiento de la caja respecto al borde superior, derecho, inferior o izquierdo | longitud \| porcentaje \| auto |
| `float` | Posicionamiento flotante | left \| right \| none |
| `clear` | Control de cajas adyacentes a las float | none \| left \| right \| both |
| `z-index` | Nivel de la capa | auto \| numero entero |
| `box-sizing` | Control de bordes y relleno en el comportamiento del contenedor | content-box \| border-box |

![Propiedad Z-index](img/Propiedad-Z-index.png)

## Pseudo-clases para selección de hijos o hermanos

| Pseudo-clase | Descripción |
| --- | --- |
| `:first-child` | Primer hijo |
| `:last-child` | Último hijo |
| `:first-of-type` | Primer hermano de su tipo |
| `:last-of-type` | Último hermano de su tipo |
| `:only-child` | Hijos únicos |
| `:only-of-type` | Únicos hermanos de su tipo |
| `:empty` | Elementos que no tienen hijos |
| `:nth-child(n)` | Enésimo elemento hijo |
| `:nth-last-child(n)` | Enésimo elemento hijo contando desde el útimo |
| `:nth-of-type(n)` | Enésimo hermano de su tipo |
| `:nth-last-of-type(n)` | Enésimo hermano de su tipo comenzando desde el último |

## Pseudo-clases para los estados de un elemento

| Pseudo-clase | Descripción |
| --- | --- |
| `:link` | No visitado por el usuario |
| `:visited` | Visitado por el usuario |
| `:hover` | Modifica el estilo cuando un elemento apuntador pasa por encima |
| `:active` | Se activa cuando el usuario pulsa el elemento |
| `:focus` | Se activa cuando tiene el foco sobre el elemento |

## Pseudo-elementos

| Pseudo-clase | Descripción |
| --- | --- |
| `:first-line` | Primera línea de texto de un elemento |
| `:first-letter` | Primera letra de la primera línea de texto de un elemento |
| `:before` | Añade contenido al principio del documento |
| `:after` | Añade contenido al final del documento |

## Prefijos para los navegadores

| **Prefijo** | **Navegador** |
| --- | --- |
| `-moz-` | Firefox |
| `-webkit-` | Safari y Chrome |
| `-o-` | Opera |
| `-khtml-` | Konqueror |
| `-ms-` | Internet Explorer |
| `-chrome-` | Google Chrome |
