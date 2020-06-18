# Etiquetas html para el contenido incrustado

Tabla de contenidos

-   [6\. Contenido incrustado](#6-Contenido-incrustado)
-   [6.1. Etiquetas para incrustar contenido](#61-Etiquetas-para-incrustar-contenido)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

# 6. Contenido incrustado

El contenido HTML incrustado se utiliza para mostrar recursos externos como, por ejemplo, mapas, previsiones meteorológicas, fórmulas matemáticas, vídeos y audios, entre otros. Este método permite utilizar un sitio de terceros como un servicio de alojamiento e interfaz de carga. 

# 6.1. Etiquetas para incrustar contenido

| Elemento | Descripción |
| --- | --- |
| `<img>` | Representa una imagen. |
| `<iframe>` | Representa un contexto anidado de navegación, es decir, un documento HTML embebido. |
| `<embed>` | Representa un punto de integración para una aplicación o contenido interactivo externo que por lo general no es HTML. |
| `<object>` | Representa un recurso externo, que será tratado como una imagen, un sub-documento HTML o un recurso externo a ser procesado por un plugin. |
| `<param>` | Define parámetros para el uso por los plugins invocados por los elementos `<object>`. |
| `<video>` | Representa un vídeo, y sus archivos de audio y canciones asociadas, con la interfaz necesaria para reproducirlos. |
| `<audio>` | Representa un sonido o *stream de audio.* |
| `<source>` | Permite a autores especificar recursos multimedia alternativos para los elementos multimedia como  `<video>` o `<audio>`. |
| `<track>` | Permite a autores especificar una pista de texto temporizado para elementos multimedia como `<video> `o  `<audio>`. |
| `<canvas>` | Representa un área de mapa de bits en el que se pueden utilizar scripts para renderizar gráficos. |
| `<map>` | En conjunto con `<area>`, define un mapa de imagen. |
| `<area>` | En conjunto con  `<map>`, define un mapa de imagen. |
| `<svg>` | Define una imagen vectorial embebida. |
| `<math>` | Define una fórmula matemática. |
Tabla 6.1: Contenido incrustado

#### Ejemplo

```html
<!DOCTYPE html>
<html lang="es">  
  <head>    
    <title>Ejemplos Etiquetas incrustar contenidos</title>      
  </head>  
    <body>  
       <h3>Etiqueta &lt;img&gt;</h3>
       <img src="https://www.gva.es/portal-gva-theme/images/GVA/logo_gva.png"
                 alt="Usabilidad">
      
       <h3>Etiqueta &lt;iframe&gt;</h3>
       <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d154214.5103364689!2d-0.5427351669515812!3d38.35795447718404!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xd6235da3b9dab4b%3A0x1d7da872ac0b81e3!2sAlicante+(Alacant)%2C+Alicante%2C+Espa%C3%B1a!5e1!3m2!1ses!2sus!4v1564299065614!5m2!1ses!2sus" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe><br><br>
      <h3>Etiqueta &lt;iframe&gt;</h3>
      <iframe width="600" height="400" src="https://www.youtube.com/embed/coy5h2w5xUg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </body>  
</html>
```

[HTML. Etiquetas incrustar contenidos (Codepen)](https://codepen.io/sergio-rey-personal/pen/WNrGLqW)

# Ejercicios propuestos

#### Actividad 6.1

Añade el logotipo de la empresa en la cabecera de tu blog, el logotipo debe contener un enlace que te lleve a la página de inicio. Recuerda ubicar las imágenes dentro de la carpeta adecuada.

#### Actividad 6.2

Incluye en el footer de tu blog los iconos de redes sociales con sus enlaces correspondientes. Incluye mínimo el icono de Whatsapp, Twitter y Facebook.

#### Actividad 6.3

Añade una nueva entrada en tu blog que contenga los siguientes elementos:

-   Un título *lorem ipsum*.
-   Una descripción con *lorem ipsum*.
-   Un mapa con la ubicación de la empresa.

#### Actividad 6.4

Añade una nueva entrada en tu blog que contenga los siguientes elementos:

-   Un título *lorem ipsum*.
-   Una descripción con *lorem ipsum*.
-   Un vídeo.