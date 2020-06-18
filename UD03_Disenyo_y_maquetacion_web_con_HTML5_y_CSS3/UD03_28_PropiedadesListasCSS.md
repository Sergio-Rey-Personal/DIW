# **Propiedades de las listas en CSS**

Tabla de contenidos

-   [8\. Propiedades de las listas](#8-Propiedades-de-las-listas)
    -   [8.1. List-style-type](#81-List-style-type)
    -   [8.2. List-style-image](#82-List-style-image)
    -   [8.3. List-style-position](#83-List-style-position)
    -   [8.4. List-style](#84-List-style)
    -   [8.5. Lista convertida en botonera horizontal](#85-Lista-convertida-en-botonera-horizontal)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

# 8. Propiedades de las listas

Las propiedades CSS de las listas son las que nos permiten controlar los estilos de los marcadores y la posición de los elementos dentro de las listas, entre otras. En la tabla 8.1 se muestran **las propiedades de las listas** más utilizadas.

Tabla 8.1: Propiedades de las listas
| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `**list-style-type**` | Estilo aplicable a los marcadores visuales de las listas | disc | circle | square | decimal | decimal-leading-zero | lower-roman | upper-roman | lower-greek | lower-latin | upper-latin | armenian | georgian | lower-alpha | upper-alpha | none |
| `**list-style-image**` | Imagen aplicable a los elementos de las listas | url("http://...") | none |
| `**list-style-position**` | Posición del marcador dentro de la lista | inside | outside |
| `**list-style**` | Permite establecer el estilo de la lista, la imagen y/o la posición | list-style-type | list-style-position | list-style-image |

* * * * *

## 8.1. List-style-type

```css
.a {list-style-type: circle;}
.b {list-style-type: square;}
.c {list-style-type: upper-roman;}
.d {list-style-type: lower-alpha;}
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad font-size</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad list-style-type</h3>
    <ul class="a">
      <li>Tipo círculo</li>
      <li>Tipo círculo</li>
      <li>Tipo círculo</li>
    </ul>
    <ul class="b">
      <li>Tipo cuadrado</li>
      <li>Tipo cuadrado</li>
      <li>Tipo cuadrado</li>
    </ul>
    <p>Listas ordenadas:</p>
    <ol class="c">
      <li>Uno</li>
      <li>Dos</li>
      <li>CTres</li>
    </ol>
    <ol class="d">
      <li>Uno</li>
      <li>Dos</li>
      <li>Tres</li>
    </ol>
</body>
</html>
```

[CSS3. Propiedad list-style-type](https://codepen.io/sergio-rey-personal/pen/QWyGqoj)

* * * * *

## 8.2. List-style-image

```css
ul.a { list-style-image: url('https://i.racjonalista.pl/img/em/lol.gif'); }
ul.b { list-style-image: url('https://media.giphy.com/media/tBik70kZOJKOk/giphy.gif'); }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad list-style-image</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad list-style-image</h3>
    <ul class="a">
      <li>Lista con imagen externa</li>
      <li>Lista con imagen externa</li>
      <li>Lista con imagen externa</li>
    </ul>
    <ul class="b">
      <li>Lista con imagen externa</li>
      <li>Lista con imagen externa</li>
      <li>Lista con imagen externa</li>
    </ul>
</body>
</html>
```
[CSS3. Propiedad list-style-image](https://codepen.io/sergio-rey-personal/pen/PoZbJLr)

* * * * *

## 8.3. List-style-position

```css
ul.a { list-style-position: outside; }
ul.b { list-style-position: inside; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad list-style-position</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad list-style-position</h3>
    <h4>list-style-position: outside</h4>
    <ul class="a">
      <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur./li>
      <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</li>
    </ul>
    <h4>list-style-position: inside</h4>
    <ul class="b">
      <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</li>
      <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</li>
    </ul>
</body>
</html>
```
[CSS3. Propiedad list-style-position](https://codepen.io/sergio-rey-personal/pen/JjGbrVL)

* * * * *

## 8.4. List-style

```css
ul.a { list-style: square inside; }
ul.b { list-style: circle inside; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad list-style</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad list-style</h3>
    <h4>list-style: outside</h4>
    <ul class="a">
     <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</li>
      <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</li>
    </ul>
    <h4>list-style: circle inside</h4>
    <ul class="b">
      <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</li>
      <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</li>
    </ul>
</body>
</html>
```

[CSS3. Propiedad list-style](https://codepen.io/sergio-rey-personal/pen/vYLyewv)
## 8.5. Lista convertida en botonera horizontal

Gracias a los estilos podemos convertir una lista `<ul>` en una botonera horizontal, en una galería de fotos u en otros elementos. En el siguiente ejemplo puedes ver una barra de navegación bastante típica que puedes encontrar en cualquier web.

Presta atención a que no se han utilizado clases, sólo se ha necesitado hacer uso de [selectores etiqueta](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_23_SelectoresCSS.md#32-selector-etiqueta) y [selectores descendientes](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_23_SelectoresCSS.md#35-selector-descendiente). Además fíjate que gracias al padding que se le ha incluido en los enlaces, serían perfectamente pulsables.

```css
*{
    margin: 0px;
    padding: 0 px;
    font-family: "Roboto", Arial, Tahoma, sans-serif;
}
/* Header and Nav */
header{
    position: fixed;
    width: 100%;
    height: 70px;  
    background-color: #F7F9FA;
}
nav{
    max-width: 1024px;
    margin: 0 auto;
}
header img{
    padding: 18px 10px;
}
nav ul{
    float: right;
    list-style: none;
    text-align: center;
    vertical-align: top;
}
nav li{
    list-style-type: none;
    padding: 0px;
    display: inline;
}
nav li a{
    font-size: 1em;
    text-decoration: none;
    line-height: 70px;
    padding: 15px 10px;
}
```

```html
 <header>
   <nav>
      <a href="index.html"><img src="http://www.gva.es/portal-gva-theme/images/GVA/logo_gva.png" alt="GVA Logo" width="74" height="33"></a>
      <ul>
          <li><a href="#">Inicio</a></li>
          <li><a href="#">Servicios</a></li>
          <li><a href="#">Contacto</a></li>
      </ul>
   </nav>
</header>
```
[CSS3. Menu](https://codepen.io/sergio-rey-personal/pen/yLeVPJb)

# Ejercicios propuestos

A partir de tu proyecto HTML realiza los siguiente:

-   Establece los estilos necesarios para convertir la lista que contiene la etiqueta `<nav>` en una botonera.
-   Dale estilo a las listas del `<aside>` de tu blog.