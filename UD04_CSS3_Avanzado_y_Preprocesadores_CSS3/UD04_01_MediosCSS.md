# 1. **Estilos para diferentes medios en CSSS**

Tabla de contenidos

- [1. **Estilos para diferentes medios en CSSS**](#1-estilos-para-diferentes-medios-en-csss)
  - [1.1. Medios definidos con `<link>`](#11-medios-definidos-con-link)
  - [1.2. Medios definidos con @media](#12-medios-definidos-con-media)
  - [1.3. Medios definidos con `@import`](#13-medios-definidos-con-import)
  - [1.4. Hojas de estilo auditivas, CSS Speech Module](#14-hojas-de-estilo-auditivas-css-speech-module)
- [Ejercicios propuestos](#ejercicios-propuestos)
    - [Actividad Extra](#actividad-extra)


Las hojas de estilos CSS permiten **definir diferentes estilos para diferentes medios** o dispositivos: pantallas, impresoras, proyectores, televisores, etc. La tabla siguiente muestra el nombre que se utiliza en CSS para identificar cada medio:

| Medio | Descripción |
| --- | --- |
| `all` | Todos los dispositivos |
| `print` | Para documentos paginados y mostrados en vista de impresión |
| `screen` | Pantallas de ordenador |
| `speech` | Sintetizadores para navegadores de voz utilizados por personas discapacitadas |

Una de las ventajas de CSS es que nos permite modificar los estilos de una página en función del medio en el que se visualiza. Hay tres formas diferentes de indicar el medio en el que se deben aplicar los estilos CSS. Veamos cada una de ellas.

## 1.1. Medios definidos con `<link>`

Se puede utilizar la etiqueta `<link>` en el código html **para enlazar los archivos CSS externos**. Para ello utilizaremos el atributo media para indicar el `medio` en el que se aplica el estilo de cada archivo mencionado en el atributo `href`.

```html
<link rel="stylesheet" type="text/css" media="screen" href="style.css" />
<link rel="stylesheet" type="text/css" media="print" href="especialStyle.css" />
```

## 1.2. Medios definidos con @media

Mediante la **regla**`**@media**` podemos **indicar de forma directa el medio o medios en los que se aplicarán los estilos**. Para especificar el medio en el que se aplican los estilos, se incluye su nombre después de `@media`. Si los estilos se aplican a varios medios, se incluyen los nombres separados mediante comas.

En el siguiente ejemplo se define que el tamaño de letra de la página visualizada en una pantalla será de 12 píxeles. Sin embargo, cuando se impriman los contenidos de la página, su tamaño de letra será de 11 puntos. En cualquier caso el texto de la letra será de color azul.

```css
@media print  { body { font-size: 11pt; } }
@media screen { body { font-size: 12px; } }
@media { body { color: blue; } } /* Se aplica a todo */
```

* * * * *

## 1.3. Medios definidos con `@import`

Gracias a las reglas de tipo `@import` se pueden **enlazar archivos CSS externos para indicar los estilos que se aplican en cada medio**. Este método viene muy bien para no tener todos los estilos en una misma hoja.

En el ejemplo siguiente se carga el archivo "estilosPantalla.css" cuando la página se visualiza por pantalla. Cuando la página se imprime se carga el archivo "estilosImpresora.css". El archivo estilos.css se cargará en ambos medios.

```css
@import url("estilosPantalla.css") screen;
@import url("estilosImpresora.css") print;
@import url("estilos.css"); /* Se aplica a todo por defecto*/
```
* * * * *

## 1.4. Hojas de estilo auditivas, CSS Speech Module

Las hojas de estilo auditivas proporcionan información para usuarios invidentes y de navegadores de voz de manera parecida a la que se proporciona visualmente.

> Las propiedades CSS definidas en el módulo del habla (CSS Speech Module) permiten a los autores controlar de forma declarativa la presentación de un documento en la versión auditiva.\
>\
> El procesamiento auditivo de un documento combina la síntesis de voz (también conocido como "**TTS", el acrónimo de "Text to Speech**") y los iconos auditivos ("audio cues" en esta especificación).\
>\
> Las propiedades CSS del habla proporcionan la **capacidad de controlar el tono del habla y velocidad, el volumen, voces TTS utilizadas**, etc.\
>\
> Estas propiedades CSS **pueden ser utilizadas junto con las propiedades visuales** (medios mixtos), o **como una alternativa completa fonética a una presentación visual**.
>
> *W3C*

[Leer más en el siguiente artículo recomendado](https://escss.blogspot.com/2012/06/css-speech-module-css-hablado.html)

# Ejercicios propuestos

Cuando se imprime una página web normalmente lo que queremos es el contenido, no la presentación visual de la página como logotipos e imágenes decorativas. Además, los elementos de la interfaz como menús, listas desplegables y botones no tiene sentido imprimirlos porque no se puede interactuar con ellos.

Por ejemplo, al imprimir una página web puede interesar no imprimir la cabecera (`<header>`), el pie de página (`<footer>`), el menú de navegación principal (`<nav>`) e información adicional al contenido (`<aside>`).

- Añade una nueva hoja de estilo utilizando medios definidos con `<link>` para que no se imprima el `<header>`), el `<footer>`), el `<nav>` y el `<aside>`
- Crea un fichero HTML como el de la actividad anterior pero ahora agrega los estilos utilizando la opción `@import`

### Actividad Extra

Interpreta el siguiente código y explica las diferentes propiedades y sus valores.

```css
h1, h2, h3, h4 {
  voice-family: male;
  richness: 80;
  cue-before: url("beep.au")
}
```