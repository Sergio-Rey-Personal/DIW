# Colores y fondo en CSS, atributos y propiedades

Tabla de contenidos

-   [5. Colores y fondo](#5-Colores-y-fondo)
    -   [5.1. Tabla de colores básicos](#51-Tabla-de-colores-básicos)
    -   [5.2. Propiedades más utilizadas](#52-Propiedades-más-utilizadas)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

# 5. Colores y fondo

Los valores de los colores se pueden definir mediante su nombre, en hexadecimal o mediante los valores RGB (Red, Green, Blue) , HSL (Hue, Saturation, Lightness), RGBA (Red, Green, Blue, Alpha) y HSLA (Hue, Saturation, Lightness, Alpha).

## 5.1. Tabla de colores básicos

Html soporta alrededor de 140 nombres de colores diferentes. Entre ellos puedes encontrar los siguientes colores básicos:

| Color | HEX | RGB |
| ----- | --- | --- |
| black | #000000 | 0,0,0 |
| white | #ffffff | 255,255,255 |
| red | #ff0000 | 255,0,0 |
| blue | #0000ff | 0,0,255 |
| yellow | #ffff00 | 255,255,0 |
| gray | #808080 | 128,128,128 |
| green | #008000 | 0,128,0 |
Table 5.1. Colores básicos

[Ver lista completa de colores expresados por nombre, hexadecimal y en RGB](https://www.w3schools.com/cssref/css_colors.asp)

# 5.2. Propiedades más utilizadas

Algunas de las propiedades relacionadas con el color y el fondo más utilizadas son las siguientes:

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `color` | Color del texto | RGB | HSL | HEX | nombre del color | RGBA | HSLA |
| `background-color` | Color de fondo | url(...) | none |
| `background-image` | Imagen de fondo | none | underline | overline | line-through | * |
| `background-repeat` | Repetición de la imagen de fondo | repeat | repeat-x | repeat-y | no-repeat |
| `background-attachment` | Desplazamiento de la imagen de fondo | scroll | fixed |
| `background-position` | Posición de la imagen de fondo | percentage | length | left | center | right |
| `Opacity` | Transparencia de un elemento | [ 0 -- 1 ] |
Tabla 5.2: Propiedades colores y fondo

***`ejemplo`***

```css
/* style.css */
h1   { background-color: red; }
h2   { background-color: #FF0000; }
h3   { background-color: RGB(255,0,0); }
p    { background-color: HSL(0,100%,50%) }
body { background-image: url("https://bit.ly/2slA7jo"); }
```

```html
<html>
<head>
   <meta charset="utf-8"> 
   <title>Colores en CSS</title> 
   <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <p class="a">Rojo con su nombre</p>
    <p class="b">Rojo con Hexadecimal<p/>
    <p class="c">Rojo con RGB</p>
    <p class="d">Rojo con HSL</p>
</body>
</html>
```

[Colores en CSS (Codepen)](https://codepen.io/sergio-rey-personal/pen/JjGbyeK)


# Ejercicios propuestos
Dale estilo a tu proyecto web partiendo de la guía de estilo creada en la unidad 1.

-   Define los colores y fondos de las etiquetas de tipo sección: h1, h2, h3, h4... , nav, body, footer, a, header, aside, address, section,etc.
-   Define los colores y fondos de las etiquetas de contenido y texto.
-   Define los colores y fondos de las etiquetas para formularios.
-   Define los colores y fondos de las etiquetas de las tablas de contenido