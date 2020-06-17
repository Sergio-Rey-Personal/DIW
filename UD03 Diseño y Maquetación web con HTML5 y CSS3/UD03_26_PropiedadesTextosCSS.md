# **Propiedades de texto en CSS**

Tabla de contenidos

-   [6\. Propiedades de texto](https://www.eniun.com/atributos-propiedades-textos-css/#6-Propiedades-de-texto)
    -   [6.1. Text-indent](https://www.eniun.com/atributos-propiedades-textos-css/#61-Text-indent)
    -   [6.2. Text-align](https://www.eniun.com/atributos-propiedades-textos-css/#62-Text-align)
    -   [6.3. Text-decoration](https://www.eniun.com/atributos-propiedades-textos-css/#63-Text-decoration)
    -   [6.4. Letter-spacing](https://www.eniun.com/atributos-propiedades-textos-css/#64-Letter-spacing)
    -   [6.5. Word-spacing](https://www.eniun.com/atributos-propiedades-textos-css/#65-Word-spacing)
    -   [6.6. Text-transform](https://www.eniun.com/atributos-propiedades-textos-css/#66-Text-transform)
    -   [6.7. Line-height](https://www.eniun.com/atributos-propiedades-textos-css/#67-Line-height)
-   [Ejercicios propuestos](https://www.eniun.com/atributos-propiedades-textos-css/#Ejercicios-propuestos)

# 6. Propiedades de texto

Las propiedades de texto son las que nos permiten controlar el texto como bloque, es decir, afectan al interlineado, a la separación entre palabras, al tabulado, etc. En la tabla 6.1 se muestran **las propiedades de texto** más utilizadas.

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `text-indent` | Desplazamiento de la primera línea del texto | longitud | porcentaje |
| `text-align` | Alineamiento del texto | left | right | center | justify |
| `text-decoration` | Efectos de subrayado, tachado | none | underline | overline | line-through | * |
| `letter-spacing` | Espacio entre caracteres | normal | longitud |
| `word-spacing` | Espacio entre palabras | normal | longitud |
| `text-transform` | Transformación a mayúsculas / minúsculas | capitalize | uppercase | lowercase | none |
| `line-height` | Tamaño del espacio entre líneas | longitud | porcentaje |
| `vertical-align` | Alineación vertical | top | middle | bottom |
Tabla 6.1: Propiedades de texto

* * * * *

## 6.1. Text-indent

```css
.a { text-indent: 50px; }
.b { text-indent: 3em; }
.c { text-indent: 30%; }
.d { text-indent: -50px; }
```

```html
<html>
<head>
   <meta charset="utf-8"> 
   <title>Propiedad text-indent</title> 
   <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad text-indent</h3>
    <p class="a">text-indent: 50px</p>
    <p class="b">text-indent: 3em</p>
    <p class="c">text-indent: 20%</p>
    <p class="d">text-indent: -50px</p>
</body>
</html>
``` 

[CSS3. Propiedad text-indent](https://codepen.io/sergio-rey-personal/pen/Yzwpxmr)

* * * * *

## 6.2. Text-align

```css
.a { text-align: center; }
.b { text-align: right; }
.c { text-align: left; }
.d { text-align: justify; }
```

```html
<html>
<head>
   <meta charset="utf-8"> 
   <title>Propiedad text-align</title> 
   <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad text-align</h3>
    <h4 class="a">text-align: center</h4>
    <p class="a">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. </p>
    <h4 class="b">text-align: right</h4>
    <p class="b">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. </p>
    <h4 class="c">text-align: left</h4>
    <p class="c">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. </p>
  <h4 class="d">text-align: justify</h4>
    <p class="d">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
</body>
</html>
```

* * * * *

## 6.3. Text-decoration

```css
.a { text-decoration: underline; }
.b { text-decoration: overline; }
.c { text-decoration: line-through; }
.d { text-decoration: underline line-through; } 
```
```html
<h3>Propiedad text-decoration</h3>
<p class="a">text-decoration: underline</p>
<p class="b">text-decoration: overline</p>
<p class="c">text-decoration: line-through</p>
<p class="d">text-decoration: underline line-through</p>
```

[CSS3. Propiedad text-align](https://codepen.io/sergio-rey-personal/pen/bGEBoGO)

* * * * *

6.4. Letter-spacing
-------------------

```css
.a { letter-spacing: 3px;  }
.b { letter-spacing: 10px; }
.c { letter-spacing: 15px; }
```

```html
<html>
<head>
   <meta charset="utf-8"> 
   <title>Propiedad letter-spacing</title> 
   <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad letter-spacing</h3>
    <p class="a">letter-spacing: 3px</p>
    <p class="b">letter-spacing: 10px</p>
    <p class="c">letter-spacing: 15px</p>
</body>
</html>
```

[CSS3. Propiedad letter-spacing](https://codepen.io/sergio-rey-personal/pen/GRoNMgd)

* * * * *

## 6.5. Word-spacing

```css
.a { word-spacing: 5px; }
.b { word-spacing: 20px; }
.c { word-spacing: 50px; }
```
```html
<html>
<head>
   <meta charset="utf-8"> 
   <title>Propiedad word-spacing</title> 
   <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad word-spacing</h3>
    <p class="a">word-spacing: 5px</p>
    <p class="b">word-spacing: 20px</p>
    <p class="c">word-spacing: 50px</p>
</body>
</html>
```

[CSS3. Propiedad word-spacing](https://codepen.io/sergio-rey-personal/pen/abdBLvB)

* * * * *

## 6.6. Text-transform

```css
.a { text-transform: capitalize; }
.b { text-transform: uppercase; }
.c { text-transform: lowercase; }
```
```html
<html>
<head>
   <meta charset="utf-8"> 
   <title>Propiedad text-transform</title> 
   <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad text-transform</h3>
    <p class="a">text-transform: capitalize</p>
    <p class="b">text-transform: uppercase</p>
    <p class="c">text-transform: LoWeRCASE</p>
</body>
</html>
```

[CSS3. Propiedad text-transform](https://codepen.io/sergio-rey-personal/pen/oNbYGbe)

* * * * *

## 6.7. Line-height

```css
.a { line-height: 50px; }
.b { line-height: 3em; }
.c { line-height: 30%; }
```

```html
<html>
<head>
   <meta charset="utf-8"> 
   <title>Propiedad line-height</title> 
   <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad text-indent</h3>
    <p class="a">line-height: 50px</p>
    <p class="b">line-height: 3em</p>
    <p class="c">line-height: 20%</p>
</body>
</html>
```

[CSS3. Propiedad line-height](https://codepen.io/sergio-rey-personal/pen/abdBLmp)

* * * * *

## Ejercicios propuestos
---------------------

Dale estilo a tu proyecto web partiendo de la guía de estilo creada en la unidad 1. Define las propiedades de texto de todas las etiquetas de tipo sección, contenido, texto, formularios y tablas de contenido.