# **Imágenes y figuras en Bootstrap 4**

Tabla de contenido

# 5. Imágenes y figuras en Bootstrap 4

Para aquellos que no tengan claro la diferencia entre imágenes y figuras podemos resumirlo de la siguiente manera:

- Una **imagen** es únicamente el elemento gráfico el cual hemos añadido mediante las etiquetas `img` o `picture`.

```html
<img src="ejemplo.png">
````

- Una **figura** (etiqueta `figure`) es un conjunto compuesto de una imagen (etiqueta `img`) y de un texto descriptivo sobre la imagen (etiqueta `caption`). Esta etiqueta es una de las novedades en HTML5.Tradicionalmente es lo que se usa en libros para hacer posteriormente un índice de figuras.

```html
<figure>
  <img src="ejemplo.png">
  <figcaption>Texto descriptivo de la imagen</figcation>
</figure>
```

BootStrap 4, por supuesto, nos proporciona una serie de clases para tratar y dar estilos a este tipo de contenidos.

## 5.1. Imágenes

En relación a las imágenes las clases de interés son:

### 5.1.1. Imagen responsive

Bootstrap 4 nos ofrece la clase **`.img-fluid`** para que las imágenes se adapten correctamente a los distintos dispositivos.

Ejemplo:

```html
< img src="eniun.jpg" class="**img-fluid**" alt="Imagen Responsive">
```

2\. Imagen con esquinas redondeadas
-----------------------------------

La clase .**rounded** agrega esquinas redondeadas a una imagen:

Ejemplo:

<img src="eniun.jpg" class="**rounded**" alt="Eniun">

3\. Imagen con forma de círculo
-------------------------------

La clase **.rounded-circle** da forma de círculo a la imagen:

Ejemplo:

<img src="eniun.jpg" class="**rounded-circle**" alt="Eniun">

4\. Imagen tipo miniatura
-------------------------

La clase **.img-thumbnail** da forma de miniatura a la imagen:

Ejemplo:

<img src="eniun.jpg" class="**img-thumbnail**" alt="Eniun">

5\. Alineación de imágenes
--------------------------

Desplace una imagen hacia la derecha con la clase **.float-right** o hacia la izquierda con .**float-left**:

Ejemplo:

<img src="eniun.jpg" class="**float-left**" alt="Eniun">
<img src="eniun.jpg" class="**float-right**" alt="Eniun">

#### Ejemplo