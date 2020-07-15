# 2. **Inserción de imágenes en HTML5**

Tabla de contenidos

- [2. **Inserción de imágenes en HTML5**](#2-inserción-de-imágenes-en-html5)
  - [2.1. Etiquetas para imágenes](#21-etiquetas-para-imágenes)
  - [2.2. Nuevas etiquetas de imágenes](#22-nuevas-etiquetas-de-imágenes)
    - [2.2.1. Imágenes alternativas](#221-imágenes-alternativas)
    - [2.2.2. Imágenes responsive](#222-imágenes-responsive)
    - [2.2.3. Diferentes densidades](#223-diferentes-densidades)

Antes de colocar una imagen en una página web debemos tener claro en que clasificación se encuentra. Las imágenes utilizadas en una página web pueden ser de dos tipos: de **contenido** o de **decoración**. En el primer caso, si la imagen pertenece al contenido y tema tratado en esa página, debería incluirse mediante una etiqueta HTML `<img>`, pero si por el contrario pertenece a la decoración de la página, deberíamos incluirla como un fondo mediante la propiedad CSS `background-image`.

## 2.1. Etiquetas para imágenes

Para incluir imágenes en el contenido de una página utilizaremos la etiqueta `<img>`, que es una etiqueta muy sencilla, que dispone de varios atributos para modificar como se verá la imagen (***los atributos src y alt son siempre obligatorios***):

| Atributo | Descripción |
| --- | --- |
| `src` | Indica el nombre o la URL de la imagen a mostrar. |
| `alt` | Establece un texto alternativo para mostrar en el caso que la imagen no se pueda mostrar. |
| `width` | Indica el ancho de la imagen. No se debe indicar unidad. Se aconseja hacerlo desde CSS. |
| `height` | Indica el alto de la imagen. No se debe indicar unidad. Se aconseja hacerlo desde CSS. |

Un ejemplo básico para colocar una imagen sería el siguiente:

```html
<img src="https://github.com/Sergio-Rey-Personal/DIW/blob/master/img/logo-gva.png?raw=true"
     alt="Logotipo de HTML5"
     width="288" height="175" />
```

Nota que los atributos *`*width`** y **`height`** redimensionan la imagen al vuelo, esto es, la imagen tendrá unas dimensiones concretas y se descargará siempre a máxima resolución. Con estos atributos redimensionas la imagen al tamaño de ancho y alto indicado, pero la imagen realmente tiene su propio tamaño. Puedes omitir estos atributos siempre que quieras, ya que no son obligatorios, pero se consideran una buena práctica para evitar los molestos cambios repentinos de posición o tamaño en una página.

## 2.2. Nuevas etiquetas de imágenes

**HTML 5.1** incorporará un nuevo sistema para utilizar imágenes en nuestros documentos HTML de forma mucho más flexible que la antigua etiqueta `<img>` que nos permitirá mostrar imágenes dependiendo de nuestras necesidades. Para ello, utilizaremos las dos siguientes etiquetas:

| Etiqueta | Atributos | Descripción |
| --- | --- | --- |
| `<picture>` |  | Agrupa una serie de imágenes. Etiqueta contenedora. |
| `<source>` | srcset, sizes, media, type | Mostrará la imagen que cumpla una serie de criterios opcionales. |

Como podemos ver, lo interesante está en la etiqueta `<source>`, que tiene una serie de atributos disponibles para utilizar. Vamos a ver para que sirve cada uno:

| Atributo | Descripción |
| --- | --- |
| `srcset` | Serie de imágenes (*separadas por coma*) que se utilizarán. Obligatorio. |
| `sizes` | Tamaño específico de la imagen que finalmente se mostrará. |
| `media` | Condición que se debe cumplir para que muestre la imagen. Ver [media queries](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD05_Responsive_Web_Design_Maquetacion_CSS-Grid_FlexBox/UD05_04_MediaQueriesCSS.md). |
| `type` | Tipo de formato de imagen. Opcional. |

### 2.2.1. Imágenes alternativas

Una de las primeras ventajas que nos ofrecen estas etiquetas es la de utilizar formatos diferentes, dependiendo del soporte del navegador. Así pues, podríamos hacer algo como esto:

```html
<picture>
  <source srcset="imagen.webp" />
  <!-- Formato WebP -->
  <source srcset="imagen.png" />
  <!-- Formato PNG -->
  <img src="imagen.jpg" alt="Descripción de la imagen" />
  <!-- Fallback -->
</picture>

```

> [Seguir ejemplos en Codepen](https://codepen.io/sergio-rey-personal/pen/PoZdwMP?editors=1010)

En este caso, indicamos que el navegador utilice la imagen con el formato **WebP**. En caso de no soportarlo, lo intentará con el formato **PNG**. Si tampoco lo soporta, mostrará la imagen en formato **JPEG**, que es la que está soportada por todos los navegadores, y si utilizamos algún navegador de texto como Lynx u otro que no pueda mostrar imágenes, mostrará el texto alternativo.

### 2.2.2. Imágenes responsive

Otra ventaja interesante es que con `<picture>` podemos crear **imágenes responsive** que cambien dependiendo de características de las **media queries** (*[CSS](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD05_Responsive_Web_Design_Maquetacion_CSS-Grid_FlexBox/UD05_04_MediaQueriesCSS.md)*). Por ejemplo, utilicemos `min-width` (*tamaño mínimo de ancho de la pantalla*) en el siguiente ejemplo:

```html
<picture>
  <source media="(min-width: 600px)"
          srcset="html5-logo-xl.png" />
  <source media="(min-width: 300px) and (max-width: 600px)"
          srcset="html5-logo-large.png" />
  <source media="(max-width: 50px)"
          srcset="html5-logo-small.png" />
  <img src="html5-logo-medium.png" alt="HTML5 logo" />
</picture>

```

De esta forma, estamos indicando que se muestren diferentes imágenes dependiendo de la resolución de pantalla (*ancho*) del dispositivo:

-   **Dispositivos muy grandes** (más de 600px): Muestra la imagen `html5-logo-xl.png`
-   **Dispositivos grandes** (entre 300-600px): Muestra la imagen `html5-logo-large.png`
-   **Dispositivos pequeños** (menos de 50px): Muestra la imagen `html5-logo-small.png`
-   **Si no cumple las anteriores** (o no soporta HTML5.1): Muestra la imagen `html5-logo-medium.png`

Nótese que esto sólo hará cambio de imagen efectivo justo en los límites indicados (50, 300, 600). Si se desea que la imagen se adapte proporcionalmente, lo mejor es recurrir a tamaños máximos y mínimos de CSS.

### 2.2.3. Diferentes densidades

Además, este sistema también permite especificar diferentes imágenes dependiendo de la densidad de pantalla del dispositivo (*alto que varía actualmente en las diferentes gamas de smartphones*). Para ello, tenemos que usar un descriptor después del nombre de la imagen utilizado en el atributo **srcset** (*si no se incluye, por omisión es igual a 1x*):

```html
<picture>
  <source media="(min-width: 600px)"
    srcset="html5-logo-xl.png, html5-logo-xl-hd.png 2x, html5-logo-xl-fhd.png 3x" />
  <source media="(min-width: 300px) and (max-width: 600px)"
    srcset="html5-logo-large.png, html5-logo-large-hd.png 2x, html5-logo-large-fhd.png 3x" />
  <source media="(max-width: 50px)"
    srcset="html5-logo-small.png, html5-logo-small-hd.png 2x, html5-logo-small-fhd.png 3x" />
  <img srcset="html5-logo-medium.png, html5-logo-medium-hd.png 2x, html5-logo-medium-fhd.png 3x"
    alt="HTML5 logo" />
</picture>

```

Nótese que en cada etiqueta `<source>`, e incluso en la etiqueta `<img>`, se puede especificar el atributo **`srcset`** e indicar varias imágenes preparadas para pantallas de alta densidad.

Por último, recuerda que la etiqueta `<picture>` y la etiqueta `<source>` dentro de la anterior son características de HTML5.1 y aún no están soportadas en todos los navegadores. Se recomienda ser cuidadoso con este detalle.