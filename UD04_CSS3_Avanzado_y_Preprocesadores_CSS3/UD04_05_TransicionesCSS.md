# **Transiciones en CSS, estilos diferentes entre estados**

# 5. Transiciones en CSS

Las transiciones nos permiten aplicar un **cambio de estilo gradual a los elementos**. Además, nos ofrecen la ventaja de poder **especificar el tiempo** para que se produzca la transformación entre estilos, de esta forma podríamos utilizarlas para dar un **efecto de animación**.

Todos los parámetros para aplicar las transiciones se pueden establecer en una sola línea y también mediante propiedades por separado. Veamos como se implementa en una sola línea:

- **transition:**[propiedad a modificar] [Duración] [Tipo de animación] [Retardo];

- **transition:** width 2s ease-out 0.5s;

- **[Propiedades a modificar]:** Algunas de las propiedades que podemos modificar utilizando transiciones son las que se muestran en la siguiente lista:

| Propiedades | 
| --- | 
| all |
| background-color |
| border |
| border-radius |
| color |
| top |
| bottom |
| left |
| right |
| box-shadow |
| width |
| height |
| line-height |
| margin |
| opacity |
| word-spacing |
| letter-spacing |
| fill |
| padding |
| stroke |
| text-shadow |
| vertical-align |
| visibility |
| z-index |

En el [siguiente enlace](https://developer.mozilla.org/es/docs/Web/CSS/Transiciones_de_CSS#Propiedades_que_pueden_ser_animadas) podemos encontrar más propiedades que se pueden utilizar en las transiciones.

- **[Duración en segundos]**: Se debe especificar el número de segundos que va a durar la animación. Primero se escribe un valor numérico (los segundos) y seguido la "s" (ejemplo: 3s).\
- **[Tipo de animación]**: Esta propiedad es opcional. Aquí tenemos la posibilidad de indicar un tipo de *easing*, es decir, si la animación empezará suavemente e irá acelerándose progresivamente, si pasará todo lo contrario o si el movimiento tendrá una velocidad uniforme durante todo su recorrido entre otras. Algunas de las posibilidades son las siguientes:
  -   linear: La velocidad de la animación es uniforme en todo el recorrido.
  -   ease: La velocidad se acelera al inicio, luego se retarda un poco y se acelera al final de nuevo.
  -   ease-in: La animación empieza lentamente y va aumentando progresivamente.
  -   ease-out: La animación empieza muy rápida y va descendiendo progresivamente.
  -   ease-in-out: La animación empieza y acaba lentamente, y es en la parte central del recorrido donde la velocidad es más rápida.

- **[Retardo]:** En este apartado podemos especificar un tiempo (en segundos) que el navegador esperará antes de poner en marcha la animación. Se especifica el número de segundos a esperar seguido de la "s" (ejemplo: 1s).

[Recuerda utilizar la extensión que te facilita la tarea de crear los prefijos para navegadores.](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_31_PrefijosNavegadoresCSS.md)

## Ejemplo

**Transiciones para algunas propiedades:**

```css
.container{
    position: relative;
}
.caja{
  width: 180px;
  height: 180px;
  background-color: #30B037;
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
  -webkit-transition: background-color 1s linear;
  transition: background-color 1s linear;
}
.caja1:hover{
  background-color: #3F51B5;
}
.caja2{
  background-color: #9B59B6;
  -webkit-transition: font-size 1s ease;
  transition: font-size 1s ease;
}
.caja2:hover{
  font-size: 28px;
}
.caja3{
  background-color: #2980B9;
  -webkit-transition: color 1s linear;
  transition: color 1s linear;
}
.caja3:hover{
  color: yellow;
}
.caja4{
  background-color: #3498DB;
  -webkit-transition: 1s linear;
  transition: 1s linear;
}
.caja4:hover{
  line-height: 300px;
}
.caja5{
  border-radius: 0px;
  background-color: #17A589;
  -webkit-transition: 1s linear;
  transition: 1s linear
}
.caja5:hover{
  border-radius: 20px;
}
.caja6{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: #F1C40F;
}
.caja6:hover{
  -webkit-box-shadow: 10px 10px 14px 2px rgba(0,0,0,0.47);
  box-shadow: 10px 10px 14px 2px rgba(0,0,0,0.47);
}
.caja7{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: #E67E22;
}
.caja7:hover{
  opacity: 0.3;
}
.caja8{

  -webkit-transition: 1s linear;

  transition: 1s linear;
  background-color: #95A5A6;
}
.caja8:hover{
  border-style: solid;
  border-color: #95A5A6;
  border-color: #000;
}
.caja9{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: #2C3E50;
}
.caja9:hover{
  margin: 80px;
}
.caja10{
  -webkit-transition: 1s linear;
  transition: 1s linear;
  background-color: black;
}
.caja10:hover{
  padding: 30px;
}
```

```html
<div class="container">
  <div class="caja caja1">Background</div>
  <div class="caja caja2">Font-size</div>
  <div class="caja caja3">Color</div>
  <div class="caja caja4">Line-height</div>
  <div class="caja caja5">Border-radius</div>
  <div class="caja caja6">Box-shadow</div>
  <div class="caja caja7">Opacity</div>
  <div class="caja caja8">Border</div>
  <div class="caja caja9">Margin</div>
  <div class="caja caja10">Padding</div>
</div>
```

> [Transiciones en CSS (Codesite)](https://codepen.io/sergio-rey-personal/pen/xxZraNQ)


**Menú con transiciones:**

```css
/* Menú horizontal con transiciones */

/* Formato general de cada item */

.menu {
  display: block;
  position: relative;
  height: 76px;
  width: 120px;
  margin: 0;
  overflow: hidden;
}

/* Bordes superiores */

.menu.servicios {
  border-top: #ffc000 0.3em solid;
}

.menu.recursos {
  border-top: #b81800 0.3em solid;
}

.menu.proyectos {
  border-top: #00a53c 0.3em solid;
}

.menu.contacto {
  border-top: #9600b4 0.3em solid;
}

/* Atributos y transición */

.menu > span {
  display: block;
  position: absolute;
  overflow: hidden;
  left: 0;
  top: 0;
  width: 100%;
  height: 0%;
  transition: 0.5s ease-in-out;
  -webkit-transition: 0.5s ease-in-out;
}

.menu:after, .menu > span > span {
  display: block;
  text-align: center;
  border-radius: 0em;
  padding: 2em 0 1.5em;
}

.menu:after {
  content: attr(data-title);
  width: 100%;
  background: #000;
  color: #fff; 
}

.menu > span > span {
  width: 120px;
  color: #fff;
}

.menu.servicios > span > span {
  background: #ffc000;
}

.menu.proyectos > span > span {
  background: #00a53c;
}

.menu.recursos > span > span {
  background: #b81800;
}

.menu.contacto > span > span {
    background: #9600b4;
}

/* Lo que pasa con hover */

.menu:hover > span {
    height: 100%; 
}

/* Dando formato a lista */ 

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

li a {
  display: inline;
  float: left;
  text-decoration: none;
  font-family: sans;
}
```

```html
<ul>
<li><a class="menu servicios" href="#" data-title="Servicios"><span>
    <span>Servicios</span>
  </span></a></li>
<li><a class="menu proyectos" href="#" data-title="Proyectos">
  <span>
    <span>Proyectos</span>
  </span>
  </a></li>
  <li><a class="menu recursos" href="#" data-title="Recursos">
  <span>
    <span>Recursos</span>
  </span>
  </a></li>
    <li><a class="menu contacto" href="#" data-title="Contacto">
  <span>
    <span>Contacto</span>
  </span>
  </a></li>
</ul>
```

> [Menú transiciones (Codesite)](https://codepen.io/sergio-rey-personal/pen/ZEQyqJq)

# Ejercicios propuestos

Utiliza transiciones para algunos de los botones de tu proyecto web o para otro elemento en el que te parezca adecuado el uso de transiciones.