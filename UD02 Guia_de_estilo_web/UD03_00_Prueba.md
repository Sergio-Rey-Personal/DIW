# **Propiedades de texto en CSS**

Tabla de contenidos

-   [6\. Propiedades de texto](#6-Propiedades-de-texto)
    -   [6.1. Text-indent](#61-Text-indent)
    -   [6.2. Text-align](#62-Text-align)
    -   [6.3. Text-decoration](#63-Text-decoration)
    -   [6.4. Letter-spacing](#64-Letter-spacing)
    -   [6.5. Word-spacing](#65-Word-spacing)
    -   [6.6. Text-transform](#66-Text-transform)
    -   [6.7. Line-height](#67-Line-height)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

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


