# 11. Animaciones basadas en keyframes con la propiedad animation

Tabla de contenidos

- [11. Animaciones basadas en keyframes con la propiedad animation](#11-animaciones-basadas-en-keyframes-con-la-propiedad-animation)
  - [11.1. Propiedad `animation`](#111-propiedad-animation)
  - [11.2. Uso de `@keyframes`](#112-uso-de-keyframes)
  - [11.3. Ejemplo animación](#113-ejemplo-animación)

*En la unidad 4 vimos cómo hacer *[transformaciones](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD04_CSS3_Avanzado_y_Preprocesadores_CSS3/UD04_06_TransformacionesCSS.md) y [transiciones](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD04_CSS3_Avanzado_y_Preprocesadores_CSS3/UD04_05_TransicionesCSS.md)* CSS3 sobre los elementos de nuestra página web. De esta forma conseguíamos proporcionar a los elementos un efecto de animación sobre algunas propiedades básicas de CSS.*

En este apartado veremos c**ómo encadenar diferentes animaciones utilizando la propiedad animation y sus subpropiedades**. Para ello, **definiremos la propiedad animation sobre nuestros selectores y después definiremos nuestra secuencia de animación mediante `@keyframes`.**

## 11.1. Propiedad `animation`

Para crear una animación primero añadiremos al selector la propiedad `animation` y utilizaremos sus subpropiedades para configurar la duración o dirección, entre otras cosas. La sintaxis es la siguiente:

```css
selector{
     ** animation-name**: identifier;
      **subproperty**: value;
}
```

Las subpropiedades de `animation` son:

| Propiedad | Descripción | 
| --- | --- |
| `animation-name` | Especifica el nombre de la regla `@keyframes` que describe los fotogramas de la animación. |
| `animation-delay` | Tiempo de retardo entre el momento en que el elemento se carga y el comienzo de la secuencia de la animación. |
| `animation-direction`| Indica si la animación debe retroceder hasta el fotograma de inicio al finalizar la secuencia o si debe comenzar desde el principio al llegar al final. |
| `animation-duration` | Indica la cantidad de tiempo que la animación consume en completar su ciclo (duración). |
| `animation-iteration-count` | El número de veces que se repite. Podemos indicar `infinite` para repetir la animación indefinidamente. |
| `animation-play-state` | Permite pausar y reanudar la secuencia de la animación |
| `animation-timing-function` | Indica el ritmo de la animación, es decir, como se muestran los fotogramas de la animación, estableciendo curvas de aceleración. |
| `animation-fill-mode` | Especifica qué valores tendrán las propiedades después de finalizar la animación (los de antes de ejecutarla, los del último fotograma de la animación o ambos). |

## 11.2. Uso de `@keyframes`

Una vez añadida la propiedad animation a nuestro selector, haremos uso de los `@keyframes` para crear animaciones completas.

Los @**keyframes** son un conjunto de fotogramas clave que describen cómo se muestra cada elemento animado durante la secuencia de la animación. La sintaxis es la siguiente:

```css
@keyframes identifier {
  from {
      ...
  }
  percentage {
      ...
  }
  to {
      ...
  }
}
```

| Parámetro | Descripción |
| --- | --- |
| `identifier` | Nombre que identifica la lista de keyframe. Debe coincidir con animation-name. |
| `from` | Desde (por ejemplo: desde 0%). |
| `to` | Hasta (por ejemplo hasta 100%). |
| `percentage` | Porcentaje intermedio de las veces que va a ocurrir una animación. |

[Ver descripción completa de propiedades](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Animations/Usando_animaciones_CSS)

## 11.3. Ejemplo animación

Veamos mejor estos valores mediante un ejemplo.

Vamos a hacer una animación mediante **`@keyframes`** de nuestro logo, de forma que se encuentre rotando de forma indefinida. Para ello vamos a utilizar la propiedad **`transform`** y le daremos varios valores a su rotación: crearemos una animación con tres **`keyframes`**: uno inicial que tendrá rotación de 0 grados, otro en el 50% que tendrá una rotación sobre el eje y de 180 grados y uno final que volverá a tener una rotación de 0 grados.

```html
<!--Código html:-->
<img class="**animacionLogo**" src="logo.png">
```

```css
/*Código CSS:*/

.animacionLogo{
     animation-duration: 5s;
     animation-name: animLogo;
     animation-iteration-count: infinite;
   }
 @keyframes animLogo{
     from {
         -webkit-transform: rotate(0deg);
         transform: rotateY(0deg);
     }
     50%{
         -webkit-transform: rotate(180deg);
         transform: rotateY(180deg);
     } to {
         -webkit-transform: rotate(360deg);
         transform: rotateY(360deg);
         }
 }
 ```

Tenemos el siguiente resultado: 

![Animación con Animation y Keyframes](img/Animation-keyframes.gif)

> [Ejemplo completo en CodePen](https://codepen.io/sergio-rey-personal/pen/yLexEmR)

> [Más ejemplo de animaciones en Codepen](https://codepen.io/sergio-rey-personal/pen/pogOOry)


Ver más ejemplos de animaciones en [Web developer de Mozilla](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Animations/Usando_animaciones_CSS) y en [w3school](https://www.w3schools.com/css/css3_animations.asp)