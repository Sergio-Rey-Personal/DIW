# 29. **Propiedades de las tablas en CSS**

Tabla de contenidos

- [29. **Propiedades de las tablas en CSS**](#29-propiedades-de-las-tablas-en-css)
  - [29.1. Caption-side](#291-caption-side)
  - [29.2. Table-layout](#292-table-layout)
  - [29.3. Border-collapse](#293-border-collapse)
  - [29.4. Border-spacing](#294-border-spacing)
- [Ejercicios propuestos](#ejercicios-propuestos)

Las propiedades CSS de las tablas son las que nos permiten controlar los estilos de los títulos de la tabla, el tamaño de las celdas, las filas y las columnas o espaciado entre los bordes, entre otras. En la tabla 9.1 se muestran **las propiedades de las tablas** más utilizadas.

| Propiedad | Descripción | Valores |
| --- | --- | --- |
| `**caption-side**` | Posición del título respecto la tabla | top | bottom |
| `**table-layout**` | Formato de las celdas, filas y columnas | auto | fixed |
| `**border-collapse**` | Selección del modelo de los bordes | collapse | separate |
| `**border-spacing**` | Espaciado entre los bordes de celdas adyacentes | longitud |
| `**empty-cells**` | Visibilidad de los bordes de celdas sin contenido | show | hide |

* * * * *

## 29.1. Caption-side

```css
.a { caption-side: bottom; }
.b { caption-side: top; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad caption-side</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h3>Propiedad caption-side</h3>
   <h4>caption-side: bottom</h4>
   <table class="a">
    <caption>Tabla 1: Propiedad caption-side</caption>
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
  <h4>caption-side: top</h4>
   <table class="b">
    <caption>Tabla 2: Propiedad caption-side</caption>
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
</body>
</html>
```

[CSS3. Propiedad caption-side](https://codepen.io/sergio-rey-personal/pen/abdBVwa)

* * * * *

## 29.2. Table-layout

```css
.a { table-layout: auto; width: 200px; }
.b { table-layout: auto; width: 100%; }
.c { table-layout: fixed; width: 200px; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad table-layout</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
   <h3>Propiedad table-layout</h3>
   <h4>Table-layout: auto, width: 200px</h4>
   <table class="a">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
  <h4>Table-layout: auto, width: 100%</h4>
   <table class="b">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
  <h4>Table-layout: fixed, width: 200px</h4>
   <table class="c">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
</body>
</html>
```

[CSS3. Propiedad table-layout](https://codepen.io/sergio-rey-personal/pen/mdVOqBd)

* * * * *

## 29.3. Border-collapse

```css
.a { border-collapse: separate; }
.b { border-collapse: collapse; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad border-collapse</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
   <h3>Propiedad table-layout</h3>
   <h4>Border-collapse: separate</h4>
   <table class="a">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
  <h4>Border-collapse: collapse</h4>
   <table class="b">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
</body>
</html>
```

[CSS3. Propiedad border-collapse](https://codepen.io/sergio-rey-personal/pen/GRoNOOg)

* * * * *

## 29.4. Border-spacing

```css
.a { border-collapse: separate; border-spacing: 50px 10px;}
.b { border-collapse: collapse; border-spacing: 40px;} /* Solo tiene efecto cuando border-collapse: separate; */
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad border-spacing</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
   <h3>Propiedad border-spacing</h3>
   <h4>Propiedad border-spacing: 50px 10px;</h4>
   <table class="a">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
  <h4>Propiedad border-spacing con border-collapse: collapse</h4>
   <table class="b">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td>Fila 1</td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td>Fila 3</td>
    </tr>
   </table>
</body>
</html>
```

[CSS3. Propiedad border-spacing](https://codepen.io/sergio-rey-personal/pen/xxZRPPQ)

9.5. Empty-cells

```css
.a { empty-cells: hide; }
.b { empty-cells: show; }
```

```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Propiedad empty-cells</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
   <h3>Propiedad empty-cells</h3>
   <h4>Propiedad empty-cells: hide</h4>
   <table class="a">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td></td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td></td>
    </tr>
   </table>
  <h4>Propiedad empty-cells: show</h4>
   <table class="b">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td></td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td></td>
    </tr>
   </table>
  <h4>Propiedad empty-cells: show</h4>
   <table class="c">
    <tr>
      <th>Columna 1</th>
      <th>Columna 2</th>
      <th>Columna 3</th>
    </tr>
    <tr>
      <td>Fila 1</td>
      <td>Fila 1</td>
      <td></td>
    </tr>
    <tr>
      <td>Fila 2</td>
      <td>Fila 2</td>
      <td>Fila 2</td>
    </tr>
    <tr>
      <td>Fila 3</td>
      <td>Fila 3</td>
      <td></td>
    </tr>
   </table>
</body>
</html>
```

[CSS3. Propiedad empty-cells](https://codepen.io/sergio-rey-personal/pen/PoZbOEZ)

* * * * *

# Ejercicios propuestos

- Dale estilo a la tabla de la primera entrada que creaste en tu blog. Utiliza alguna de las propiedades vistas en esta sección.

- En la página servicios de tu proyecto HTML establece los siguientes estilos a la tabla:
    - Un título en la parte de abajo.
    - La celda se debe ajustar según el texto introducido.
    - La tabla debe ocupar el 100% de su contenedor padre.
    - Utiliza la propiedad "border-collapse: collapse".
    - Dale estilo a los bordes de la tabla.