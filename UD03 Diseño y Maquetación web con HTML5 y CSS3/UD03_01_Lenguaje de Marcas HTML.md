Lenguaje de marcas HTML
=======================

Tabla de contenidos

-   [1\. Lenguaje de marcas HTML](#1-Lenguaje-de-marcas-HTML)
-   [1.1. Breve historia HTML](#11-Breve-historia-HTML)
-   [1.2. Estructura HTML](#12-Estructura-HTML)
-   [1.3. Organización de elementos HTML](#13-Organización-de-elementos-HTML)


*En la unidad anterior vimos los componentes y elementos principales necesarios en la **planificación de interfaces web**. En este punto, veremos el **lenguaje de marcado** que emplearemos para la creación o inserción de todos esos elementos.*

# 1\. Lenguaje de marcas HTML

El **lenguaje de marcas o lenguaje de marcado** es un tipo de lenguaje de programación que no tiene funciones aritméticas o variables. En este tipo de lenguaje se combina el texto con etiquetas que contienen información adicional sobre la estructura del texto o su presentación. Algunos ejemplos de este lenguaje son HTML, XML o RDF.

**HTML (HyperText Markup Language) es el lenguaje de marcado utilizado para la creación de páginas web**. Básicamente, se trata de un **conjunto de etiquetas que especifican los textos, las líneas, las imágenes, los enlaces a otras páginas y otros elementos** que pueda contener una página web.

El número de etiquetas en HTML es limitado y siguen unas reglas bastante estrictas. Todas las etiquetas disponen de los símbolos mayor que y menor que ( < > ), y normalmente se utilizarán en parejas. Una al principio y otra al final del texto al que afectan. Por ejemplo:

```html
<h1>Encabezado principal</h1>
```

Observa que la etiqueta de cierre del final incluye una barra inclinada.

El lenguaje HTML es un estándar reconocido en todo el mundo y sus normas están definidas por un organismo sin ánimo de lucro llamado [World Wide Web Consortium](https://www.w3.org/), conocido como **W3C**. 

## 1.1. Breve historia HTML

En el siguiente vídeo puedes conocer de forma breve la **historia de HTML**.

[Historia de HTML (youtube)](https://www.youtube.com/embed/EEttUcYhv30)

El vídeo que acabas de ver forma parte de un [curso de Google Actívate realizado por la Universidad de Alicante](https://learndigital.withgoogle.com/activate/course/web-development-I) que te recomendamos realizar.

## 1.2. Estructura HTML

Las páginas web tienen una estructura general que explicaremos en los siguientes apartados.

```html
<!DOCTYPE html>
<html lang="es">  
  <head>    
    <title>Título de la WEB</title>       
  </head>  
  <body>    
    Estructura básica HTML
  </body>  
</html>
```
[Estructura básica HTML (Codepen)](https://codepen.io/sergio-rey-personal/pen/xxZVBRv)

## 1.3. Organización de elementos HTML

A la hora de desarrollar un sitio web es recomendable llevar a cabo una estructura lógica de carpetas para facilitar la programación y posterior mantenimiento del sitio.

![Organización de carpetas en el desarrollo web](img/estructura-de-carpetas-desarrollo-web.png)


# Actividad

Crea una carpeta llamada “www.web.com” y dentro de ella una carpeta llamada “assets” tal y como se indica en el esquema anterior. 

Crea también un documento index.html y escribe la estructura básica que hemos visto en esta sección.

