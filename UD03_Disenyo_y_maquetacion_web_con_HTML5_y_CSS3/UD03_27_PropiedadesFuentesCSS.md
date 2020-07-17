# 27. **Propiedades de las fuentes en CSS**

Tabla de contenidos

- [27. **Propiedades de las fuentes en CSS**](#27-propiedades-de-las-fuentes-en-css)
  - [27.1. Font-family](#271-font-family)
  - [27.2. Font-style](#272-font-style)
  - [27.3. Font-variant](#273-font-variant)
  - [27.4. Font-weight](#274-font-weight)
  - [27.5. Font-size](#275-font-size)
- [Ejercicios propuestos](#ejercicios-propuestos)

Las propiedades CSS de las fuentes son las que permiten controlar el tamaño, el tipo, el grosor o el estilo de las letras entre otras cosas.

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `**font-family**` | Familias de fuentes | nombre-familia|nombre-familia-genérica| * |
| `**font-style**` | Estilo de la fuente | normal | italic | oblique |
| `**font-variant**` | Convierte a mayúsculas manteniendo un tamaño inferior | normal | small-caps |
| `**font-weight**` | Anchura de los caracteres. Normal = 400, Negrita = 700 | normal | bold | bolder | lighter | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 |
| `**font-size**` | Tamaño de la fuente | xx-small | x-small | small | medium | large | x-large | xx-large | larger | smaller | longitud | porcentaje |
Tabla 7.1: Propiedades de las fuentes

* * * * *

## 27.1. Font-family

```css
.a  { font-family: "Times New Roman", Times, serif; }
.b  { font-family: Arial, Helvetica, sans-serif; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad font-family</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad font-family</h3>
    <p class="a">Texto con propiedad font-family: "Times New Roman", Times, serif; </p>
    <p class="b">Texto con propiedad font-family: Arial, Helvetica, sans-serif;</p>
    <p class="negrita">Párrrafo en negrita</p>
</body>
</html>
```

[CSS3. Propiedad font-family](https://codepen.io/sergio-rey-personal/pen/NWxbaaZ)


* * * * *

## 27.2. Font-style

```css
.a  { font-style: normal; }
.b  { font-style: italic; }
.c  { font-style: oblique; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad font-style</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad font-style</h3>
    <p class="a">Párrrafo con estilo normal </p>
    <p class="b">Párrafo en italic</p>
    <p class="c">Párrrafo en oblique</p>
</body>
</html>
```

[CSS3. Propiedad font-style](https://codepen.io/sergio-rey-personal/pen/qBbqPpV)

* * * * *

## 27.3. Font-variant

```css
.a  { font-variant: normal; }
.b  { font-variant: small-caps; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad font-variant</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad font-variant</h3>
    <p class="a">Párrrafo con estilo normal </p>
    <p class="b">Párrafo con estilo small-caps</p>
    <h2 class="b">Cabecera con estilo small-caps</h2>
</body>
</html>
```

[CSS3. Propiedad font-variant](https://codepen.io/sergio-rey-personal/pen/oNbYGqq)

* * * * *

## 27.4. Font-weight

```css
.a  { font-weight: normal; }
.b  { font-weight: bold; }
.c  { font-weight: 400; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad font-weight</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad font-weight</h3>
    <p class="a">Párrrafo con estilo normal </p>
    <p class="b">Párrafo en negrita</p>
    <p class="c">Párrrafo en negrita</p>
</body>
</html>
```
[CSS3. Propiedad font-weight](https://codepen.io/sergio-rey-personal/pen/rNxWGKj)

* * * * *

## 27.5. Font-size

```css
.a  { font-size: 20px; }
.b  { font-size: 2em; }
.c  { font-size: xx-small; }
.d  { font-size: small; }
.e  { font-size: 250%; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad font-size</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad font-size</h3>
    <p class="a">Párrrafo con font-size: 20px </p>
    <p class="b">Párrafo con font-size: 2em</p>
    <p class="c">Párrrafo con font-size: xx-small </p>
    <p class="d">Párrafo con font-size: small</p>
    <p class="e">Párrafo con font-size: 250%</p>
</body>
</html>
```

[CSS3. Propiedad font-size](https://codepen.io/sergio-rey-personal/pen/abdBLjL)

# Ejercicios propuestos

Dale estilo a tu proyecto web partiendo de la guía de estilo creada en la unidad 1. Define las propiedades de las fuentes de todas las etiquetas de tipo sección, contenido, texto, formularios y tablas de contenido.