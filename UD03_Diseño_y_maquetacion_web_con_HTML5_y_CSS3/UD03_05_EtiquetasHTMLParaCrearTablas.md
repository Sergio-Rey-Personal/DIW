# Etiquetas html para crear tablas de contenido

Tabla de contenidos

-   [5\. Tablas de contenido](#5-Tablas-de-contenido)
-   [5.1. Etiquetas para la creación de tablas de contenido](#51-Etiquetas-para-la-creacion-de-tablas-de-contenido)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

# 5. Tablas de contenido

Las tablas de contenido nos permiten almacenar los datos de forma ordenada.

## 5.1. Etiquetas para la creación de tablas de contenido

El principio y final de una tabla se define con las etiquetas `<table>` y `</table>`. Las filas se engloban con las etiquetas `<tr>` `</tr>` y las columnas estarán dentro de la etiquetas `<td>` `</td>`.

La etiqueta `<table>` puede incluir diferentes opciones, como puedes ver en la siguiente tabla.

| Elemento | Descripción |
| --- | --- |
| `<table>` | Representa datos con más de una dimensión. |
| `<caption>` | Representa el título de una tabla. |
| `<tr>` | Representa una fila de celdas en una tabla. |
| `<td>` | Representa una celda de datos en una tabla. |
| `<th>` | Representa una celda encabezado en una tabla. |
| `<colgroup>` | Representa un conjunto de una o más columnas de una tabla. |
| `<col>` | Representa una columna de una tabla. |
| `<tbody>` | Representa el bloque de filas que describen los datos concretos de una tabla. |
| `<thead>` | Representa el bloque de filas que describen las etiquetas de columna de una tabla. |
| `<tfoot>` | Representa los bloques de filas que describen los resúmenes de columna de una tabla. |
Tabla 5.1: Tablas de contenido

#### Ejemplo

```html
<!DOCTYPE html>
<html lang="es">  
  <head>    
    <title>Ejemplos Tabla de contenido</title>      
  </head>  
    <body>  
        <table>
        <caption>Tabla I: Ejemplo de tabla de contenido</caption>
          <tr>
            <th>Nombre</th>
            <th>Apellidos</th> 
            <th>Edad</th>
          </tr>
          <tr>
            <td>Jorge</td>
            <td>Oliva</td>
            <td>35</td>
          </tr>
          <tr>
            <td>Raquel</td>
            <td>Gimenez</td>
            <td>34</td>
          </tr>
          <tr>
            <td>María</td>
            <td>Ruiz</td>
            <td>87</td>
          </tr>
        </table>
    </body>  
</html>
```

[HTML. Etiquetas formularios (Codepen)](https://codepen.io/sergio-rey-personal/pen/dyGpwaz)
# Ejercicios propuestos

En la página Servicios crea una tabla que incluya un mínimo de 3 columnas y 5 filas. Debe disponer de etiqueta de encabezado `<th>` y de etiqueta de título `<caption>`. Describe los servicios que ofreces o utiliza *lorem ipsum* para rellenar los datos de la tabla.