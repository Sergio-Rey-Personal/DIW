# 7. **Propiedad CSS `overflow`, excedente de contenido**

Tabla de contenidos
- [7. **Propiedad CSS `overflow`, excedente de contenido**](#7-propiedad-css-overflow-excedente-de-contenido)
  - [7.1. Valores de **`overflow`**](#71-valores-de-overflow)
- [Ejercicios propuestos](#ejercicios-propuestos)


En la unidad anterior vimos el [comportamiento de los contenedores en CSS](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD04_CSS3_Avanzado_y_Preprocesadores_CSS3/UD04_06_TransformacionesCSS.md), veamos ahora cómo controlar el **comportamiento del contenido** que se encuentra en esos contenedores.

La propiedad ***overflow*** (desbordamiento o excedente) nos permite controlar el **comportamiento del contenido que se encuentra en una caja o contenedor**. Por lo tanto, mediante esta propiedad podremos especificar si queremos recortar un contenido, mostrar barras de desplazamiento o mostrar el contenido que excede de un elemento a nivel de bloque.

## 7.1. Valores de **`overflow`**

La propiedad *overflow* solo funciona sobre elementos de tipo bloque con una altura definida. Sus valores son los siguientes:

**overflow: visible|hidden|scroll|auto;**

-   **Overflow: visible (default).** Por defecto la propiedad *overflow* es visible y lo que hace es que los contenidos se salgan del elemento y sean completamente visibles.

-   **Overflow: hidden.** Los contenidos que se salen del contenedor padre se ocultan y no se muestran barras de *scroll*. De esta forma se puede controlar el tamaño del elemento y su contenido.

-   **Overflow: scroll**. Se muestra una barra de *scroll* (horizontal y vertical) cuando los contenidos no caben en el contenedor o caja.

-   **Overflow: auto**. El navegador es el que decide si se muestran las barras de *scroll* o si se extiende el contenedor. En cualquier caso, gracias a este valor nunca se permite que el contenido desborde al contenedor. Este valor es muy interesante ya que si el contenido se sale por un lado (horizontal o vertical), sólo se muestra la barra de *scroll* de ese lado.

Puede interesarte conocer también las propiedades [overflow-x](https://developer.mozilla.org/es/docs/Web/CSS/overflow-x) y [overflow-y](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow-y).

**Ejemplo**

```css
.scroll {
  background-color: lightgreen;
  width: 150px;
  height: 150px;
  overflow: scroll;
}

.hidden {
  background-color: lightblue;
  width: 150px;
  height: 150px;
  overflow: hidden;
}

.auto {
  background-color: lightgrey;
  width: 150px;
  height: 150px;
  overflow: auto;
}
.visible {
  background-color: lightyellow;
  width: 150px;
  height: 150px;
  overflow: visible;
}
.auto-img {
  background-color: lightgrey;
  overflow: auto;
}
.auto-img img{
 float: left;
 max-height: 300px;
}
```

```html
<h1>Propiedad overflow</h1>

<h2>overflow: visible (default):</h2>
<div class="visible">
  Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
  nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Lorem
  ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
  euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
</div>
<br /><br /><br /><br /><br /><br />
<h2>overflow: scroll</h2>
<div class="scroll">
  Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
  nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Lorem
  ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
  euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
</div>

<h2>overflow: hidden</h2>
<div class="hidden">
  Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
  nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Lorem
  ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
  euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
</div>

<h2>overflow: auto con scroll</h2>
<div class="auto">
  Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
  nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Lorem
  ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
  euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
</div>
<h2>overflow: auto sin scroll</h2>
<p>
  En este caso la imagen excede el contenedor. Al establecer la propiedad
  overflow: auto conseguimos que el contenido no desborde el contenedor.
</p>
<div class="auto-img">
  <img src="https://www.gva.es/portal-gva-theme/images/GVA/logo_gva.png" alt="logo"/>
  Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
  nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Lorem
  ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
  euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
</div>
```

> [Propiedad overflow (Codepen)](https://codepen.io/sergio-rey-personal/pen/pogwxxx)

# Ejercicios propuestos

Utiliza la propiedad `overflow` con el valor `hidden` o `auto` para mostrar el texto de los artículos de la página del blog de tu proyecto web.