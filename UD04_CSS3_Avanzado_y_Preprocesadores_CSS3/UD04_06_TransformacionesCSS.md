# 6. **Transformaciones en CSS: rotar, torcer, escalar o desplazar**

Tabla de contenidos

- [6. **Transformaciones en CSS: rotar, torcer, escalar o desplazar**](#6-transformaciones-en-css-rotar-torcer-escalar-o-desplazar)
  - [6.1. Tipos de transformaciones](#61-tipos-de-transformaciones)
- [Ejercicios propuestos](#ejercicios-propuestos)

Las **transformaciones CSS** nos permiten **rotar, torcer, escalar o desplazar** los elementos de nuestra página web. Este tipo de propiedades de CSS3 son muy interesantes para convertir el lenguaje de hojas de estilo en un sistema capaz de realizar todo tipo de **efectos visuales**. Las dos propiedades que nos sirven para definir las transformaciones son `**transform**`y `**transform-origin**`.

-   `transform-origin`La posición de origen que se utilizará para la transformación es por defecto el lado superior izquierdo del elemento.
-   `transform`La posición de origen para realizar la transformación es el eje central del elemento.

## 6.1. Tipos de transformaciones

Las transformaciones que podemos aplicar son las siguientes:

-   **Scale**: modifica el tamaño de los elementos.
-   **Translate**: cambia la posición del elemento. Izquierda, derecha, arriba o abajo.
-   **Rotate**: gira o rota los elementos en grados.
-   **Skew**: distorsiona los elementos.
-   **Matrix**: mueve o transforma los elementos con precisión de píxel.

La propiedad transform se usa junto con la propiedad [transition](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD04_CSS3_Avanzado_y_Preprocesadores_CSS3/UD04_05_TransicionesCSS.md) vista en el apartado anterior:

```css
.caja1{
   background-color: #C0392B;
   -webkit-transition: 1s linear;
   transition: 1s linear;
 }
 .caja1:hover{
   -webkit-transform: scale(.5);
   transform: scale(.5);
 }

```
[Recuerda utilizar la extensión que te facilita la tarea de crear los prefijos para navegadores.](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_31_PrefijosNavegadoresCSS.md)

**Ejemplo**

Transformaciones y transiciones sobre elementos:

```css
.container{
  position: relative;
}
.caja{
  width: 180px;
  height: 180px;
  color: #FFF;
  text-align: center;
  line-height: 180px;
  margin: 15px;
  float: left;
  font-size: 18px;
  font-family: Arial;
}
.caja1{
  background-color: #C0392B;
  -webkit-transition: 1s linear;
  transition: 1s linear;
}
.caja1:hover{
  -webkit-transform: scale(.5);
  transform: scale(.5);
}
.caja2{
  background-color: #9B59B6;
  -webkit-transition: 1s linear;
  transition: 1s linear;
}
.caja2:hover{
  -webkit-transform: rotate(360deg);
  transform: rotate(360deg);
}
.caja3{
  background-color: #2980B9;
  -webkit-transition: 1s linear;
  transition: 1s linear;
}
.caja3:hover{
  -webkit-transform: skew(5deg, 5deg);
  transform: skew(5deg, 5deg);
}
.caja4{
  background-color: #3498DB;
  -webkit-transition: 1s linear;
  transition: 1s linear;
}
.caja4:hover{
  -webkit-transform: skewX(-10deg);
  transform: skewX(-10deg);
}
.caja5{
  background-color: #17A589;
  -webkit-transition: 1s linear;
  transition: 1s linear;
}
.caja5:hover{
  -webkit-transform: skewY(10deg);
  transform: skewY(10deg);
}
.caja6{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: #F1C40F;
}
.caja6:hover{
  -webkit-transform: translate(10%);
  transform: translate(10%);
}
.caja7{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: #E67E22;
}
.caja7:hover{
  -webkit-transform: translateX(20px);
  transform: translateX(20px);
}
.caja8{

  -webkit-transition: 1s linear;

  transition: 1s linear;
  background-color: #95A5A6;
}
.caja8:hover{
  -webkit-transform: translateY(20px);
  transform: translateY(20px);
}
.caja9{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: #2C3E50;
}
.caja9:hover{
  -webkit-transform: perspective(150px) rotateX(45deg);
  transform: perspective(150px) rotateX(45deg);
}
.caja10{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: grey;
}
.caja10:hover{
  -webkit-transform: perspective(150px) rotateY(45deg);
  transform: perspective(150px) rotateY(45deg);
}
.caja11{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: black;
}
.caja11:hover{
  -webkit-transform: matrix(0.5, 0.1, 0.5,1,10, -2);
  transform: matrix(0.5, 0.1, 0.5,1,10, -2);
}
```

```html
<div class="container">
  <div class="caja caja1">Scale</div>
  <div class="caja caja2">Rotate</div>
  <div class="caja caja3">Skew</div>
  <div class="caja caja4">SkewX</div>
  <div class="caja caja5">SkewY</div>
  <div class="caja caja6">Translate</div>
  <div class="caja caja7">TranslateX</div>
  <div class="caja caja8">TranslateY</div>
  <div class="caja caja9">Perspective rotate</div>
  <div class="caja caja10">Perspective rotate</div>
  <div class="caja caja11">Matrix</div>
</div>
```

> [Transformaciones y transiciones en CSS (Codesite)](https://codepen.io/sergio-rey-personal/pen/rNxwqKR)

# Ejercicios propuestos

Utiliza algún tipo de transformación en uno de los elementos de tu proyecto web.