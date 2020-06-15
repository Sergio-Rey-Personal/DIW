# **Etiquetas html de contenido y texto**

Tabla de contenidos

-   [3\. Contenido y texto](https://www.eniun.com/etiquetas-contenido-texto-html/#3_Contenido_y_texto)
-   [3.1. Etiquetas de contenido](https://www.eniun.com/etiquetas-contenido-texto-html/#31_Etiquetas_de_contenido)
-   [3.2. Etiquetas de texto](https://www.eniun.com/etiquetas-contenido-texto-html/#32_Etiquetas_de_texto)
    -   [3.2.1. Hiperenlaces](https://www.eniun.com/etiquetas-contenido-texto-html/#321_Hiperenlaces)
-   [Comprueba tu aprendizaje](https://www.eniun.com/etiquetas-contenido-texto-html/#Comprueba_tu_aprendizaje)
-   [Ejercicios propuestos](https://www.eniun.com/etiquetas-contenido-texto-html/#Ejercicios_propuestos)

# 3. Contenido y texto

En este apartado vamos a ver dos tipos de **etiquetas HTML**: las etiquetas que agrupan el **contenido** y las etiquetas que contienen fragmentos de **texto** (dan significado a esas palabras o fragmentos). Veamos cada una de ellas.

## 3.1. Etiquetas de contenido

| Elemento | Descripción |
| --- | --- |
| `<p>` | Define una parte que debe mostrarse como un párrafo. |
| `<hr>` | Representa un cambio temático entre párrafos. |
| `<pre>` | Indica que su contenido esta preformateado y que este formato debe ser preservado. |
| `<blockquote>` | Representa un contenido citado desde otra fuente. |
| `<ol>` | Define una lista ordenada de artículos. |
| `<ul>` | Define una lista de artículos sin orden. |
| `<li>` | Define un artículo de una lista ennumerada. |
| `<dl>` | Define una lista de definiciones, es decir, una lista de términos y sus definiciones asociadas. |
| `<dt>` | Representa un término definido por el siguiente `<dd>`. |
| `<dd>` | Representa la definición de los terminos listados antes que él. |
| `<figure>` | Representa una figura ilustrada como parte  del documento. |
| `<figcaption>` | Representa la leyenda de una figura. |
| `<div>` | Representa un contenedor genérico sin ningún significado especial. |
Tabla 3.1: Etiquetas de contenido

#### Ejemplo

```html
<!DOCTYPE html>
<html lang="es">  
  <head>    
    <title>Ejemplos Etiquetas de contenido</title>      
  </head>  
  <body>
        <h3>Etiqueta &lt;p&gt;</h3>
        <p>Párrafo Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia beatae aliquam non natus aut id sint ea? Natus tempore hic reprehenderit temporibus minima nisi, quia, magnam omnis, officiis molestiae earum.</p>
        
        <h3>Etiqueta &lt;hr&gt;</h3>
        <hr>
        
        <h3>Etiqueta &lt;pre&gt;</h3>
        <pre>Contenido preformateado       Conserva los espacios,
            los saltos de línea y los tabuladores del texto original.
        </pre>
        
        <h3>Etiqueta &lt;blockquote&gt;</h3>
        <blockquote>Con blockquote representamos un contenido citado desde otra fuente.</blockquote>
        
        <h3>Etiqueta &lt;ul&gt;</h3>
        <ul>
            <li>Lista sin orden</li>
            <li>Lista sin orden</li>
            <li>Lista sin orden</li>
        </ul>
        
        <h3>Etiqueta &lt;ol&gt;</h3>
        <ol>
            <li>Lista ordenada</li>
            <li>Lista ordenada</li>
            <li>Lista ordenada</li>
        </ol>
        
        <h3>Etiquetas &lt;dl&gt; &lt;dt&gt; &lt;dd&gt;</h3>
        <dl>
            <dt>Término 1</dt>
            <dd>Definición del término 1.</dd>
        
            <dt>Término 2</dt>
            <dd>Definición del término 2.</dd>
        
            <dt>Término 3</dt>
            <dd>Definición del término 3.</dd>
        </dl>
        
        <h3>Etiqueta &lt;figure&gt;</h3>
        <figure>
            <img src="https://www.eniun.com/wp-content/uploads/eniun-icon-user-experience.svg"
                 alt="Usabilidad">
            <figcaption>Esto es un figcaption</figcaption>
        </figure>
        
        <h3>Etiqueta &lt;div&gt;</h3>
        <div>Contenedor tipo div</div>     
    </body>  
</html>
```



3.2. Etiquetas de texto
-----------------------

Tabla 3.2: Etiquetas de texto
| Elemento | Descripción |
| --- | --- |
| `<a>` | Representa un *hiperenlace*. |
| `<em>` | Representa un texto *enfatizado*. |
| `<strong>` | Representa un texto importante. |
| `<small>` | Representa un comentario aparte, es decir, textos de políticas de responsabilidad o una nota de derechos de autoría, que no son esenciales para la comprensión del documento. |
| `<s>` | Representa contenido que no es exacto, tiene el estilo tachado. |
| `<cite>` | Representa el título de una obra. |
| `<q>` | Representa una cita textual entre comillas. |
| `<dfn>` | Sirve para marcar el término que se quiere definir. |
| `<abbr>` | Representa una abreviación o un acrónimo; mediante el atributo `title` se puede describir la abreviatura. El texto es usualmente representado como tooltip cuando se pasa el puntero sobre el elemento. |
| `<time>` | Representa un valor de fecha y hora. |
| `<code>` | Representa un código de programación. |
| `<var>` | Representa a una variable, es decir, una expresión matemática o una variable de un programa o similar. |
| `<samp>` | Representa la salida de un programa. |
| `<kbd>` | Representa el texto que debe introducir o la tecla que debe pulsar el usuario. |
| `<sub>``<sup>` | Representan un subíndice y un superíndice respectivamente. |
| `<i>` | Muestra el texto marcado con un estilo en cursiva o italica. |
| `<b>` | Muestra el texto marcado con un estilo en negrita. |
| `<u>` | Muestra el texto subrayado. |
| `<mark>` | Representa un texto marcado o resaltado como referencia o anotación, debido a su relevancia o importancia. |
| `<span>` | Representa texto en línea. Sirve para aplicar estilo al texto o agrupar elementos en línea. |
| `<br>` | Representa un salto de línea. |
| `<wbr>` | Representa una oportunidad de salto de línea, es decir, un punto sugerido donde el texto puede ser dividido para mejorar su legibilidad. |

#### Ejemplo

### 3.2.1. Hiperenlaces

#### Valores del atributo href

Vamos a ver cómo crear un enlace para llamar por teléfono con `tel` y para enviar un correo con `mailto`

#### Ejemplo

#### Valores del atributo target

Vamos a abrir un enlace en una página aparte mediante el atributo `target` y el valor `_blank`:

#### Ejemplo