# **La sintaxis de SASS al detalle**

Tabla de contenidos

- [11. Sintaxis SASS](#11-Sintaxis-SASS)
  - [11.1. Variables](#111-Variables)
  - [11.2. Importar](#112-Importar) 
  - [11.3. Partials](#113-Partials)
  - [11.4. Mixins](#114-Mixins)
  - [11.5. Extend](#11-Extend)
  - [11.6. Anidamientos](#116-Anidamientos)
  - [11.7. Funciones](#117-Funciones)
  - [11.8. Bucles](#118-Bucles)
  - [11.9. Ramificación](#119-Ramificación)
  - [11.10. Comentarios](#1110-Comentarios)
  - [11.11. Error, warn y debug](#1111-Error-warn-y-debug)
- [Ejercicios propuestos](#Ejercicios-propuestos)

  
# 11. Sintaxis SASS

Como ya se ha mencionado, no hay solo una sintaxis en SASS. Hoy hay **dos formatos consolidados que compiten entre sí**. Originalmente, SASS se basaba en la sintaxis que hoy se conoce como *"indented syntax"*, en la que las indentaciones (o sangrías de texto) generan el anidamiento y cada salto de línea finaliza una línea de código. SCSS, en cambio, se orienta más al formato que conocemos por CSS y requiere, por lo tanto, corchetes y puntos y comas. A continuación, nos adentraremos en las peculiaridades de SASS.

> Si solo deseas probar el lenguaje de la hoja de estilo, puedes hacerlo en el navegador. Con [Sass.js Playground](http://sass.js.org/ "Editor online para SASS") o [SassMeister](https://www.sassmeister.com/ "Editor para SassMeister") el código fuente CSS se genera tras introducir el código.

## 11.1. Variables

La mayoría de los desarrolladores web aprecian el uso de variables en SASS porque con ellas puede **guardarse información con un alias** y reutilizarla más tarde. Su uso es muy popular, por ejemplo, en el contexto de los colores y las especificaciones de tamaño. En una variable se puede guardar el valor hexadecimal de un color o ajustar un tamaño fijo utilizando funciones matemáticas. Las variables se introducen en SASS con el símbolo del dólar (*$*):

```scss
$bg-color: #df0174
$size: 1em
```

*SCSS*

```scss
$bg-color: #df0174;
$size: 1em;
```

Estas variables se colocan entonces en los lugares apropiados del código:

*SASS*

```less
$bg-color: #df0174
$size: 1em
body
  background-color: $bg-color
  margin: $size * 2
```

*SCSS*

```scss
$bg-color: #df0174;
$size: 1em;
body {
  background-color: $bg-color;
  margin: $size * 2;
}
```

Al compilar, el compilador ajusta la sintaxis a CSS de nuevo y resuelve las variables:

*CSS*

```css
body {
  background-color: #df0174;
  margin: 2em;
}
```

> En la denominación de los valores cromáticos en la forma de variables se han consolidado dos principios diferentes. Para algunos desarrolladores es más práctico nombrar el color (*$pink*), mientras que otros prefieren especificar qué propósito debe servir (*$bg-color*). Con todo, en principio, los nombres de las variables pueden seleccionarse libremente.

Para ciertas variables, puede ser útil especificar un valor por defecto. A menos que se defina lo contrario, SASS recurre a esta información (si la variable se define de forma diferente, se ignora la información predefinida). Esto puede ser útil, por ejemplo, si un desarrollador presenta un producto inacabado a un cliente que aún desea realizar cambios o cuando un diseñador web utiliza su propia plantilla. Este valor predeterminado se puede lograr colocando una etiqueta ***!default***. Se pueden introducir tanto valores normales como variables ya definidas:

*SASS*

```less
$text-color: #000000 !default
$background-color: $bg-color !default
```

*SCSS*

```scss
$text-color: #000000 !default;
$background-color: $bg-color !default;
```

Los tipos de datos que tenemos son lo siguientes:

| Tipo | Ejemplo de uso |
| --- | --- |
| Booleanas | `$booleana: false;` |
| Numéricas | `$line-height: 1.5; $font-size: 1.2em;...` |
| Colores | `$color: purple; $borde: #333...` |
| Strings | `$header: “Helvetia Neue”; $str: Arial...` |
| Listas | `$usuarios: Pepe, Juan, Alicia, Luisa; $margin: 40px 5px 10px 20px;` |
| Mapas | `$btn-colors: ("error" : $color-error, "warning" : $color-warning, "accepted" : $color-accepted,"normal" : $color-normal);` - `$breakpoint: ( 'pequeño' : 576px, 'medio' : 768px, 'grande' : 992px );` |
| Null | `$nulo: null;` |

Ámbito:
- Las variables declaradas fuera de cualquier estilo son globales
- Las variables declaradas dentro de algún estilo son locales
- Las

### Ejemplos

```scss
// Variables de colores
$grey: #bbbbbb;
$header-background: $grey;
$link-normal: #111;
$link-hover: #f00;
$link-visited: #00f;
$link-active: #0f0;


/* **********************************************
    Elementos de la cabecera
*********************************************** */
.header {
    background-color: $header-background;
}


// ******************************************
// Tama?o de los iconos
// Listas
$sizes: ( 40px, 80px, 160px);

// Breakpoints para la p?gina
// Mapa
$breakpoints:( 
    "peque?o": 576px, 
    "medio": 768px,
    "grande": 992px
);

// ******************************************
//Interpolaci?n en selectores
$button-type: "error";
$btn-color: #f00;
.btn-#{$button-type} {
    background-color: $btn-color;
}

//Interpolaci?n en el uso de funciones
$fondo: "images/fondos/default.png";
.container {
    background-image: url('#{$fondo}');
}

//Interpolaci?n en comentarios
$autor: "Aqui tu nombre";

/* 
    Web desarrollada por #{$autor}
*/


// ******************************************
//Anidamiento b?sico para enlaces
a {
    color: $link-normal;
    text-decoration: none;
    &:hover {
        color: $link-hover;
    }
    &:visited {
        color: $link-visited;
    }
    &:active {
        color: $link-active;
    }
}
```

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Elementos Básicos</title>
</head>

<body>
    <h1 class="header">EJEMPLO SCSS VARIABLES - HEADER</h1>
    <h1 class="footer">EJEMPLO SCSS VARIABLES - FOOTER</h1>
</body>
```

[SCSS. Variables (Codepen)](https://codepen.io/sergio-rey-personal/pen/eYJEgzw)

* * * 

```scss
// Paletas de colores básica

//Colores generales
$color-background: #FFFFFF;
$color-base: #333333;


//Colores barra de menú
$navbar-background-color: rgb(155, 111, 145);
$navbar-color-hover: $color-background;

//Colores del borde 
$border-color: $color-base;

/*Estilos para el contenedor general de mi página*/
$main-container-width: 80%;

.container {
    width: $main-container-width;
    margin: 0 auto;
}


//Estilos para los bordes
$border-width: 0.1rem;
$border-style: "solid";

$border-radius-small: 0.2rem;
$border-radius: 1rem;
$boder-radius-big: 2rem;


/*Usando anidamiento crear la hoja de estilos para un menú */
nav {
    background-color: $navbar-background-color;
    padding: 0.2rem;

    ul {
        li {
            display: inline-block;
            padding-left: 1rem;
            padding-right: 1rem;

            &.active {
                color: $navbar-color-hover;
                font-weight: bolder;
            }

            &:hover {
                color: $navbar-color-hover;
            }


            a {
                text-decoration: none;
            }

        }
    }
}

/*Estructura de anidamiento para la figura (cards)*/
$figure-width: 25%;

figure.card {
    border: $border-width #{$border-style} $border-color;
    border-radius: $border-radius;
    display: inline-block;
    padding: 1rem;
    
    width: $figure-width;
     img {
        border-radius: $boder-radius-big; 
        width: 100%;
     }

     figcaption {
         font-size: 0.8rem;
         margin: 0.5rem;
         text-align: center;
     }

}
```

```html
<div class="container">
    <nav>
        <ul>
            <li class="active">
                <a>Inicio</a>
            </li>
            <li>
                <a>Productos</a>
            </li>
            <li>
                <a>Clientes</a>
            </li>
            <li>
                <a>Sobre nosotros</a>
            </li>
        </ul>
    </nav>
    <figure class="card">
        <img src="https://www.w3schools.com/w3css/img_fjords.jpg">
        <figcaption>Imagen 1</figcaption>
    </figure>
    <figure class="card">
        <img src="https://www.w3schools.com/w3css/img_lights.jpg">
        <figcaption>Imagen 2</figcaption>
    </figure>
</div>
```

[SCSS. Ejemplo Variables (Codepen)](https://codepen.io/sergio-rey-personal/pen/MWKvJON)

## 11.2. Importar

SASS tiene una directiva muy útil que permite **incorporar otros archivos en la hoja de estilos**, como podría hacerse creando e importando un archivo en el que se definan todas las variables (por ejemplo, todos los valores de color que se necesitan). La información del archivo importado se utiliza como si formara parte del código fuente. Esto mantiene la claridad en las hojas de estilo. Con *@import* puede importarse cualquier número de archivos, incluso desde subdirectorios. La función también puede importar varios archivos en un solo paso:

```scss
@import "variables";
@import "partials/styles";
@import "partials/test-a", "partials/test-b";
```

Si deseas incluir ficheros *.sass* o *.scss*, no necesitas especificar la extensión de fichero, porque el sistema asume automáticamente que se trata de estos tipos de fichero. Sin embargo, también es posible integrar **archivos CSS** y, para que el ordenador sepa exactamente lo que significa, en este caso sí hay que especificar la terminación. Al compilar, se invierte esta simplificación y el código CSS final ya no contiene la directiva, sino solo la información de los archivos.

## 11.3. Partials

En el trabajo con SASS, lo que se importa más a menudo son los llamados partials. Se trata de **fragmentos de código** con los que se crean módulos que se pueden instalar fácilmente una y otra vez. Al nombrar el archivo, es importante preceder el nombre real con un guion bajo, el cual informa al compilador de que este archivo no necesita una contrapartida en CSS. De lo contrario, el sistema convertiría todos los archivos SASS a CSS.

Al importar los parciales el **guion bajo** se omite. SASS también interpreta a qué archivo se refiere. Por lo tanto, es conveniente no crear archivos con el mismo nombre (con y sin guión): dos archivos llamados *ejemplo.sass* y *_ejemplo.sass* respectivamente llevarán a error. Esto también se aplica a las **extensiones de archivo**: *ejemplo.sass* y *ejemplo.scss* no deberían estar en el mismo directorio.

```scss
 _filename; 
 _filename.scss;
```

## 11.4. Mixins

Otra directiva importante la constituyen las llamadas `@mixin`, reglas fijas que pueden invocarse en la hoja de estilo cuando sea necesario sin tener que volver a insertar el código completo. Esto ayuda a **trabajar más rápido y a mantener el código más ligero**. Una `@mixin` puede contener todo lo que está permitido en SASS: reglas, parámetros o funciones, pero, incluso aunque tiene un espacio ilimitado, no conviene alojar en ella más de veinte líneas. Después de todo, el objetivo es incrementar la simplicidad, no complicarlo todo más.

Para trabajar eficazmente con mixins, solo se necesitan dos directivas: *`@mixin`* e *`@include`*: con la primera se crea el modelo, con la segunda se inserta el bloque de código:

```scss
@mixin big-blue-text {
  font-family: Arial;
  font-size: 25px;
  font-weight: bold;
  color:#0000ff;
}
```

Al crear la mezcla, se da un nombre a la plantilla (por ejemplo, *`hidden`*) que permite volver a integrar el bloque de código en la posición correspondiente.

```scss
@include big-blue-text;
```

En el código CSS final aparece el bloque completo de código fuente en lugar del mixin. Aquí, la definición de la mezcla en sí (*`@mixin`*) ya no aparece.

### Ejemplo Mixin

```scss
@mixin centrado {
  margin: 0px auto;
}

@mixin highlighted-link {
  a {
    background-color: yellow;
    font-style: italic;
    text-decoration: none;
  }
}

.header {
  @include centrado;

  background-color: black;
  color: white;
}

@include highlighted-link;

// Mixin con anidamiento
@mixin centrado_menu {
  @include centrado;

  background-color: #666;
  color: white;
  height: 3rem;
}

.main_menu {
  @include centrado_menu();
}

//Mixin con parámetro
@mixin girar($grados) {
  -webkit-transfrom: rotate(#{gradosdeg}deg);
  -ms-transform: rotate(#{gradosdeg}deg);
  transform: rotate(#{gradosdeg}deg);
}

.side_tile {
  @include girar(90);

  color: #f00;
}

@mixin logo($image, $radio: 10px) {
  background-image: url("#{$image}");
  background-position: center;
  border-radius: $radio;
}

.logo-cuadrado {
  @include logo("https://www.w3schools.com/w3css/img_fjords.jpg", 0px);
}

.logo-redondeado {
  @include logo("https://www.w3schools.com/w3css/img_lights.jpg");
}
```

```html
```

[SCSS Mixin (Codepen)](https://codepen.io/sergio-rey-personal/pen/qBbXRQm)

## 11.5. Extend

La regla extender permite ahorrar mucho trabajo. La directiva garantiza que todas las propiedades de una clase se transfieran a las de otra. Usando *`@extend`* se evita tener que redefinirlo todo. La directiva también funciona como una cadena. Una clase definida por *`@extend`* puede a su vez formar parte de una tercera clase:

```scss
.button-scope {
  margin: 5px;
  border-radius: 2px;
}
.home-button {
  @extend .button-scope;
  background-color: $black;
}
.back-button {
  @extend .home-button;
}
```

El compilador resuelve el código de la siguiente manera:


```scss
.button-scope, .home-button, .back-button {
  margin: 5px;
  border-radius: 2px;
}

.home-button, .back-button {
  background-color: #000000;
}
```

En algunas situaciones puede ser necesario especificar la apariencia de una clase que no se quiere aplicar en una página web, pero sí utilizar en forma de *`@extend`*. Esto ocurre sobre todo cuando se crea una biblioteca. SASS ofrece selectores de marcadores de posición (**placeholder selectors**) para tales situaciones. Se utiliza un signo de porcentaje (*`%`*) para identificar a una clase que se crea únicamente con el fin de utilizarla en otras clases. Si al diseñar el sitio web no se importa un selector de este tipo, SASS tampoco lo compilará en CSS:

```scss
%module {
  margin: 20px;
  padding: 10px;
  color: $bg-color;
}
.post {
  @extend %module;
  color: $grey;
}
```

En el código CSS final, la clase *module* ya no aparece. Sus propiedades se transfieren directamente a la clase *post*.

```css
.post {
  margin: 20px;
  padding: 10px;
  color: ...;
}

.post {
  color: #D3D3D3;
}
```

La etiqueta *`!optional`* también puede ser muy útil en *`@extend`*: si escribes una extensión de una clase que no existe, SASS generará un error durante la compilación. Con *`!optional`* se evita, porque SASS ignorará entonces el comando si no encuentra una clase adecuada.

>El modus operandi de los `@mixin` y de `@extend` se asemeja mucho y, en la mayoría de los casos, es mejor usar los primeros. Puedes encontrar un exhaustivo análisis de las diferencias entre ambos en [csswizardry.com](https://csswizardry.com/2014/11/when-to-use-extend-when-to-use-a-mixin/ "When to use @extend and when to use a mixin - csswizardry.com").

`@mixin` debe ser usado cuando definimos propiedades similares múltiples veces con pequeñas variaciones, por otro lado, `@extend` cuando tenemos propiedades que son exactamente iguales, es decir, declaraciones copiadas una y otra vez. En cambio, las funciones son operaciones que necesitamos usar muchas veces y que nos devuelven un valor.

Ejemplos `@mixin`: https://github.com/7ninjas/scss-mixins

##  11.6. Anidamientos

En HTML se asume que **el código se anida en una estructura jerárquica**. CSS, en cambio, ignora esta función y obliga al usuario a declarar las propiedades una y otra vez. SASS devuelve la anidación a las hojas de estilo al permitir que las subcategorías hereden las propiedades de la categoría superior. Esto también garantiza la ligereza del código y la reducción de la carga de trabajo para escribir y esperar. Por ejemplo, es posible definir la apariencia de los enlaces y especificar en una anidación cómo cambian de color cuando se pasa con el ratón por encima (*hover*) o cuando ya se han visitado.

Si se emplea el *nesting* en el código, se usa el símbolo *&* para reemplazar a una parte del selector por el superior.

```scss
a {
  color: $blue;
  &:visited {
    color: $red;
  }
  &:hover {
    color: $purple;
  }
}
```

En la compilación, el anidamiento debe disolverse de nuevo. En CSS cada estado aparece definido por separado.

```css
a {
  color: #0000FF;
}

a:visited {
  color: #FF0000;
}

a:hover {
  color: #551A8B;
}
```

Más ejemplos:

*SCSS*

```scss
// primero
a{
  &:hover{…}
}

// segundo
.btn {
  &_warning{…}
}

// tercero
nav {
  li {
    a {…}
  }
}
```

```css
/* primero */
a{...}
a:hover{...}

/* segundo */
.btn {...}
.btn_warning{...}


/* tercero */
nav {...}
nav li {...}
nav li a {...}
```

Además de la resolución del anidamiento, la compilación también asegura que las variables (cuya definición omitimos en el ejemplo) se conviertan de nuevo en valores hexadecimales.

> La anidación es una herramienta muy útil para mantener el código fuente de la hoja de estilo ligero y eficiente. Con todo, la tentación de hacer un uso excesivo de ella es muy fuerte, llevando así a invertir su efecto y crear estructuras muy complejas que pueden acarrear problemas a la hora de realizar cambios o labores de mantenimiento. Así, conviene no pasar de un tercer nivel.

El nesting también permite transferir las "**propiedades**". CSS conoce algunas propiedades que pertenecen a la misma familia. Por ejemplo, toda la información de formato de fuente pertenece a la misma familia (*font*), pero en CSS debe definirse como puntos individuales con sus nombres de propiedad completos. SASS permite anidar las propiedades bajo los nombres de las familias.

```scss
.example {
font: {
    family: serif;
    style: normal;
    size: medium;
  }
}
```

## 11.7. Funciones

SASS conoce numerosas funciones que facilitan el trabajo en la hoja de estilo. Se trata de *workflows* predefinidos que evitan tener que ejecutarlos manualmente. Las funciones pueden asignarse a diferentes categorías:

-   **Colores**: con estas funciones pueden ajustarse los valores de color, la saturación, la transparencia y muchas otras propiedades. Con *mix()*, p.ej., pueden mezclarse dos colores y crear uno nuevo.
-   **Listas**: en las listas (series de valores de propiedad CSS) las funciones sirven para leer el número de entradas o fusionar varias listas en una sola.
-   **Cadenas**: las strings son cadenas fijas de caracteres, como las que se utilizan en los textos. Las funciones de esta categoría pueden colocar una cadena de caracteres entre comillas o convertir un texto completo a mayúsculas.
-   **Selectores**: con las funciones de esta categoría se manipulan selectores completos. Con *selector**-unify()* puedes fusionar dos selectores en uno solo (ahorrando mucha escritura).
-   **Números**: dentro del tema de los números, valores o unidades, encontrarás funciones que pueden, entre otras cosas, redondear hacia arriba y hacia abajo, buscar el número más grande de un conjunto o entregar un número aleatorio.
-   **Mapas**: los mapas en SASS son estructuras de datos compuestas de claves y propiedades. Con las funciones adecuadas, estos conjuntos de datos pueden manipularse fusionando dos mapas o borrando una clave de un mapa.
-   **Introspección**: estas funciones permiten revisar el contenido de la hoja de estilo completa para comprobar, entre otras cosas, si en el código se encuentra una característica determinada, un mixin o una función en concreto.
-   **Miscellaneous**: en el punto miscelánea SASS también incluye la útil función *if()* --que no debe confundirse con la directiva del mismo nombre. La diferencia se explica más abajo en el punto "Ramificación".

> Una lista completa de las funciones SASS ya incluidas en el paquete de instalación se puede encontrar en la documentación oficial del lenguaje de la hoja de estilos. Allí también encontrarás una breve explicación de cada función.

Las funciones se insertan en el código **siguiendo siempre el mismo patrón**: cada función posee un nombre propio y ciertos parámetros que se encierran entre paréntesis separados por comas. Como resultado, la función entrega un valor individual. Explicaremos esta **sintaxis de SASS** usando el ejemplo de la simple pero útil función *mix()*:

```scss
***CODE***
$color-1: #ffff00;
$color-2: #0000ff;
body {
  background-color: mix($color-1, $color-2, 30%);
}
```

En esta función se mezclan los dos valores de color que se han definido previamente en las variables *$color-1* y *$color-2* (no es necesario guardar antes los valores de color en las variables; si se prefiere, los valores hexadecimales pueden incluirse directamente en la función). Como tercer parámetro, se especifica la proporción de la mezcla: en nuestro ejemplo, el resultado final contendrá un 30 por ciento de *$color-1*. Si dejas este último parámetro vacío, SASS interpreta que la mezcla ha de resultar 50/50. En el código CSS aparecerá un valor único (el valor hexadecimal del color resultante):

```css
body {
  background-color: #4d4db3;
}
```

Las funciones explicadas hasta ahora están incluidas por defecto en SASS, pero el lenguaje de hojas de estilo también permite **definir funciones específicas para un proyecto**, lo que agiliza las fases del trabajo que más se repiten. Con ello se asemejan a las mixins, con la diferencia de que, mientras estas entregan líneas de código como output, las funciones solo entregan un valor. Las funciones se crean con la directiva *@function*, aunque en realidad necesitan siempre dos directivas: además de la inicial *@function*, se necesita un *@return* anidado con el cual se define el valor de salida:

```scss
$column-count: 12;
@function column-width($num) {
  @return $num * 100% / $column-count;
}

.three-columns {
  width: column-width(3);
```

En este ejemplo de arriba hemos calculado el ancho de columna para una cuadrícula de diseño. Primero definimos 12 columnas. En el siguiente paso, se da nombre a la función y se define cuántos parámetros contiene (en nuestro ejemplo, un número). Además, determinamos qué debe hacer la función y, por lo tanto, qué valor entrega. En este caso, *column-width* multiplica el número que se introduce como parámetro por 100 % y divide el resultado por el número de columnas. Una vez definida la función, **se puede utilizar una y otra vez con parámetros distintos**. En el código final solo aparece el valor resultante:

```css
.three-columns {
  width: 25%;
}
```

> En la creación de funciones pueden utilizarse guiones o guiones bajos en los nombres. Cuando se llama a la función más tarde, esta distinción es irrelevante. Tanto *function-name* como *function_name* llaman a la misma función.

Para proteger tu privacidad, el vídeo se cargará tras hacer clic.

## 11.8. Bucles

Los bucles proporcionan al lenguaje de hojas de estilo el atractivo de un lenguaje de programación real. En SASS se utilizan para crear bloques de instrucciones que se repiten **hasta que tiene lugar una condición determinada**. Existen tres directivas diferentes para crear bucles:

-   *@for*
-   *@while*
-   *@each*

***@for*** es el ***loop* estándar en programación**: comienza al inicio y repite la orden hasta que se alcanza un estado de salida y con ello el final. En SASS, esta directiva se presenta en dos variantes diferentes: o bien el último ciclo se ejecuta una vez más cuando se alcanza el objetivo o se abandona el bucle antes.

```scss
@for $i from 1 through 4 {
	.width-#{$i} { width: 10em + $i; }
}
@for $i from 1 to 4 {
	.height-#{$i} { height: 25em * $i; }
}
```

Tras la directiva primero se especifica **una variable cualquiera** (*$i*) y luego se define el punto de inicio (*1*) y el de destino (*4*). Con *through* se indica que la cuarta repetición también debe realizarse, mientras que con *to* el bucle se detiene después de la tercera vuelta. Si para el inicio se define un valor superior al elegido para el final, SASS cuenta hacia atrás. Hay dos elementos integrados en el bucle: primero se elige la notación de CSS que obtendrá una cifra superior con *#{$i}:* la variable --y, por lo tanto, también la notación-- se incrementará en 1 con cada vuelta.

En SASS *#{}* es una interpolación. Con ella se puede combinar a una variable con un identificador que se ha asignado a sí mismo.

Seguidamente se escribe, bien entre corchetes o con sangría, lo que debe suceder. En nuestro ejemplo, cada vuelta hace aumentar la información de tamaño. En CSS aparecerá un valor para cada pasada:

```scss
.width-1 {
  width: 11em;
}
.width-2 {
  width: 12em;
}
.width-3 {
  width: 13em;
}
.width-4 {
  width: 14em;
}
.height-1 {
  height: 25em;
}
.height-2 {
  height: 50em;
}
.height-3 {
  height: 75em;
}
```

**La directiva*****@while*** tiene una mecánica muy similar a la de *@for* pero, mientras que este último tiene puntos fijos de inicio y final, un bucle ***@while*** contiene una consulta de tipo lógico: mientras un estado siga siendo verdadero, las órdenes deberán repetirse. Como se verá a continuación, con la función *@while* podemos lograr exactamente el mismo resultado:

```scss
$i: 1;
@while $i < 5 {
	.width-#{$i} { width: 10em + $i; }
	$i: $i + 1;
}
```

Con este tipo de bucle, primero se debe **asignar un valor a las variables**, ya que la directiva en sí no necesita un valor de inicio. En el ciclo se ha de especificar el estado hasta el que se realizan las repeticiones. En nuestro ejemplo, el bucle se ejecuta siempre que la variable sea inferior a 5. La instrucción dentro del bucle es inicialmente la misma que en el ejemplo de *@for*. De nuevo, haremos que se ajuste la designación del elemento de las variables y aumente el tamaño. También se ha de integrar un comando en el bucle que haga que *$i* aumente con cada vuelta, porque, de lo contrario, el bucle se ejecutaría hasta que el compilador SASS se detuviera. Al final se obtiene el mismo código CSS que en *@for*.

**La directiva *@each*** funciona de manera diferente. Este bucle se basa en una lista de datos especificada por el usuario que el bucle recorrerá en cada vuelta. Para cada entrada, *@each* hace una repetición diferente. De este modo, indicando una lista con los valores 1, 2, 3 y 4 sería posible generar el mismo resultado que con los otros bucles. La verdadera ventaja de este bucle, sin embargo, es que también puede introducirse otra información en la lista exceptuando valores numéricos (con *@each*, por ejemplo, se insertan varias imágenes diferentes en el diseño). Puedes introducir los datos directamente en la directiva o introducir la lista en una variable y luego llamarla.

```scss
$list: dog cat bird dolphin;
@each $i in $list {
	.image-#{$i} { background-image: url('/images/#{$i}.png'); }
}
```

Aquí, de nuevo, necesitas una variable. Esta asume el nombre de una de las entradas de la lista en cada vuelta. El nombre está integrado tanto en la denominación del bloque de código como en el nombre de archivo de la imagen. Para que el diseño funcione bien, las imágenes deben haber sido guardadas en la ruta especificada. El bucle se asegura de que la variable se haga cargo de la siguiente entrada.

```css
.image-dog {
  background-image: url("/images/dog.png");
}
.image-cat {
  background-image: url("/images/cat.png");
}
.image-bird {
  background-image: url("/images/bird.png");
}
.image-dolphin {
  background-image: url("/images/dolphin.png");
}
```

### Ejemplo estructuras de control y funciones

```scss
// @if / @else if / @else example
$light-theme: true;
$dark-theme: false;

header {
  @if $light-theme == true {
    background-color: #fff;
    color: #000;
  } @else if $dark-theme {
    background-color: #000;
    color: #fff;
  } @else {
    //Default theme
    background-color: #aaa;
    color: #444;
  }
}

// @while example
$num: 1;
$color-list: #0f0, #00f, orange, #ccc;

@while $num < 5 {
  td:nth-child(#{$num}) {
    color: #f00;
    background-color: nth($color-list, $num);
  }
  $num: $num + 1;
}
// @for example
@for $i from 1 to 5 {
  p:nth-of-type(#{$i}) {
    color: #f00;
    background-color: nth($color-list, $i);
  }
}

// @each example con lista
$usuarios: pepe, lola, manuel;

@each $u in $usuarios {
  .profile-#{$u} {
    background: image-url("img/#{$u}.png") no repeat;
  }
}

// @each example with maps
$mapa: (
  pepe: "pepe.png",
  lola: "lola.png",
  manuel: "manuel.png"
);

@each $u, $v in $mapa {
  .perfil-#{$u} {
    background: image-url("img/#{$v}") no repeat;
  }
}

//User defined function example
@function anchura-col($cols, $total) {
  @return percentage($cols/$total);
}

.sidebar {
  background-color: #00f;
  width: anchura-col(2, 10);
}

```

```html
  <header>
    <h1>Estructuras de Control y funciones</h1>
  </header>
  <table>
    <tbody>
      <tr>
        <td>UNO</td>
        <td>DOS</td>
        <td>TRES</td>
        <td>CUATRO</td>
      </tr>
    </tbody>
  </table>

  <p>PÁRRAFO UNO</p>
  <p>PÁRRAFO DOS</p>
  <p>PÁRRAFO TRES</p>
  <p>PÁRRAFO 4</p>
  <section class="sidebar">
    BARRA LATERAL
  </section>
```

[SCSS. Estructuras de control y funciones (Codepen)](https://codepen.io/sergio-rey-personal/pen/VwezPQz)

* * * 

```scss
// Sistema de botones

//Colores de base
$color-error: #ff0000;
$color-warning: rgb(239, 241, 120);
$color-accepted: rgb(55, 138, 0);
$color-normal: rgb(0, 110, 255);
$color-shadow: #888;

//Valor del radio para redondear los botones
$border-radius: 0.4rem;

//Mapa del que cogeremos los nombres para interpolarlos y los valores de los colores
$btn-colors: (
  "error": $color-error,
  "warning": $color-warning,
  "accepted": $color-accepted,
  "normal": $color-normal
);

//Elemento botón general
.btn {
  display: inline-block;
  text-align: center;
  text-decoration: none;
  border-radius: $border-radius;
  padding: 0.5rem;

  &:hover {
    box-shadow: $border-radius/2 $border-radius/2 $color-shadow;
  }

  &:active {
    background-color: orange;
    color: white;
  }
}

//Clase adicional que le da color
@each $k, $v in $btn-colors {
  .btn-#{$k} {
    background-color: $v;
  }
}

//Estilos genreales para la tabla
table {
  border-collapse: collapse;
}

th,
td {
  border: 1px solid black;
  padding: 1rem;
}

//Colores para los columnas
$color-col-pares: #cccccc;
$color-col-impares: #888888;

//Función que me devuelve el color de fondo de las columnas dependiendo
// de si es para o impar
@function colum-color($col-number) {
  @if ($col-number%2 == 0) {
    @return $color-col-pares;
  } @else {
    @return $color-col-impares;
  }
}

//Establezco el número máximo de columnas
$inicio: 1;
$fin: 10;


@for $num from $inicio to $fin {
  tbody tr td:nth-child(#{$num}) {
    background-color: colum-color($num);
  }
}

//Sistema de maquetación

//Padre de cada fila
.row {
  display: flex;
  flex-direction: row;
}

//Les doy un tamaño y un borde para distinguirlos
//Sólo válida para el ejemplo
.row > * {
  border: 1px solid black;
  height: 150px;
}

//Número de elementos máximos que voy a tener
$num_elementos: 8;

//Función que devuelve la anchura correspondiente al elemento
@function anchura_col($i) {
  @return (100 / $num_elementos)*$i ;
}


//Bucle para generar las clases
@for $i from 1 through $num_elementos {
.row > .col-#{$i} {
    padding: 1rem;
    width: #{anchura_col($i)}+ "%";
  }
}
```

```html
<span class="btn btn-error">Error</span>
<a class="btn btn-warning">Warning</a>
<!-- Esto no funcionaria si no reseteo los estilos que ponen los navegadores-->
<input type="button" class="btn btn-accepted" value="Accepted" />
<div class="btn btn-normal">Normal</div>

<p>Tabla</p>
<table>
    <thead>
        <tr>
            <th>Nombre</th>
            <th>Apellidos</th>
            <th>Dirección</th>
            <th>Email</th>
        </tr>                
    </thead>
    <tbody>
        <tr>
            <td>Pepe</td>
            <td>Pérez</td>
            <td>Aquí</td>
            <td>pepe@deaqui.es</td>
        </tr>        <tr>
            <td>Manuel</td>
            <td>López</td>
            <td>Allí</td>
            <td>manuel@dealli.es</td>
        </tr>                <tr>
            <td>Ana</td>
            <td>Martínez</td>
            <td>Lejos</td>
            <td>ana@delejos.es</td>
        </tr>                <tr>
            <td>Lola</td>
            <td>Fernández</td>
            <td>Cerca</td>
            <td>lola@decerca.es</td>
        </tr>                        
    </tbody>
</table>

<p>Sistema de columnas</p>

<section class="row">
    <div class="col-2"></div>
    <div class="col-4"></div>
    <div class="col-1"></div>
    <div class="col-1"></div>
</section>
```

[SCSS. Ejemplo de estructuras. (Codepen)](https://codepen.io/sergio-rey-personal/pen/YzwxNLr)

## 11.9. Ramificación

Además de los bucles, SASS ofrece aún otra herramienta más conocida en el entorno de la programación: las ramificaciones según el principio "si-entonces-si no". Con la directiva *@if* una orden solo se ejecuta si tiene lugar un cierto evento; en caso contrario, se ejecuta otro comando. Además de esta directiva, también hay una **función *if()***. No guardan relación, pero pueden aparecer juntas. La función es fácil de explicar. Contiene tres parámetros: la condición y dos salidas diferentes. La primera salida se emite si el primer parámetro es verdadero, de lo contrario la función reproduce el tercer parámetro.

```scss
$black: #000000;
$white: #ffffff;
$text-color: $black;
body {
	background-color: if($text-color == $black, $white, $black);
}
```

En nuestro ejemplo, la función verifica si la variable *$text-color* está configurada en negro (*black*). Si este es el caso (como en el ejemplo), el fondo se mostrará blanco. En cualquier otro caso, el CSS mostraría el fondo en negro. Como puede verse en este ejemplo, esta técnica no es quizá la más adecuada para el diseño de un sitio web completo. Tanto la directiva como la función son **útiles en primera línea en mixins o partials**. Esto permite a la plantilla reaccionar mejor a los valores que aparecen en el diseño final. A la inversa, si ya sabes que el color del texto es negro, no hace falta escribir una ramificación compleja para que el fondo sea blanco.

Las funciones tienen la particularidad de devolver un solo valor. Para requisitos más complejos, conviene emplear la **directiva *@if***, que cuenta con la ventaja de poder distinguir más de dos casos entre sí:

```scss
$black: #000000;
$white: #ffffff;
$lightgrey: #d3d3d3;
$darkgrey: #545454;
@mixin text-color($color) {
  @if ($color == $black) {
    background-color: $white;
  }
  @else if ($color == $white) {
    background-color: $black;
  }
  @else if ($color == $lightgrey) {
    background-color: $black;
  }
  @else {
    background-color: $white;
	}
}
p {
	@include text-color($lightgrey);
}
```

La sintaxis de la directiva permite teóricamente crear un caso para cada valor previsto, aunque es necesario **colocar la directiva *@else*** (que, en combinación con *if* puede invocarse tantas veces como se desee) **detrás de la *@if*** inicial. Solo el último *@else* permanece libre, cubriendo así a todos los demás casos.

## 11.10. Comentarios

Con SASS también **es útil añadir comentarios al código fuente**. Los comentarios contribuyen a que el código sea comprensible para cualquiera que lo lea en otro momento. Esto ocurre así especialmente cuando se crean plantillas para otros usuarios, porque los comentarios pueden serles útiles en la edición. Muchos diseñadores web también usan comentarios para estructurar el código con más claridad. La mayoría de los lenguajes de programación y marcado tienen la capacidad de insertar en el código texto que en la compilación o el análisis se ignora. Este texto está dirigido a las personas y no a las máquinas.

Los programadores y diseñadores web también usan esta función para "comentar" el código correcto, lo que se hace colocando un bloque de código, que no se necesita, pero que no se desea eliminar del código fuente, entre las etiquetas de comentarios.

Cada lenguaje tiene un método específico para comentar texto. En SASS, esto se hace de **dos maneras diferentes**. Por un lado, como en CSS, en SASS puedes utilizar */* */*. Con este método puedes comentar varias filas al mismo tiempo. A menudo se encuentran comentarios en CSS o SASS donde cada línea en el bloque de comentarios comienza con un asterisco. Sin embargo, esto es solo una convención y no una necesidad.

```scss
/* Esto es un comentario.
Todo lo escrito entre estas marcas
no se tendrá en cuenta. */
```

Cuando se comenta, no importa si se escribe el código en SCSS o en sintaxis sangrada. Los comentarios funcionan igual en ambas sintaxis.

Además de este conocido método de CSS, con *//* también puedes comentar líneas aisladas:

```scss 
// Esta línea es un comentario.
// Y esta línea también.
```

La diferencia entre los dos métodos también radica en que, si con la configuración por defecto la primera variante se copia en el CSS compilado, la segunda se pierde. De una forma u otra, un documento CSS con comentarios no puede lanzarse online como una versión productiva. Para ello se utiliza una versión minimizada que los navegadores pueden cargar más rápido.

## 11.11. Error, warn y debug

La directivas `@error`, `@warn` y `@debug` son directivas útiles cuando estamos depurando nuestro SCSS. Nos permiten mostrar mensajes y valores de variables, funciones etc..durante el proceso de generación del
CSS.

*SINTAXIS*

```scss
@error <expression>;
@warn <expression>;
@debug <expression>;
```

*Ejemplo*

```scss
$test: false;
body {
  @if $test {
    @error "Mensaje de error";
    @debug "Test tiene el siguiente valor: #{$test}";
  }
  else {
    @warn "Mensaje de warning";
  }
}
```

# Ejercicios propuestos

Vamos a modificar el fichero de estilos de nuestro proyecto y vamos a generarlo desde un scss. 
Para ello, debes definir al menos:
- Definir variables (colores y formas básicas)
- Define correctemente los anidamientos que tengas.
- Divide los estilos por zonas (menú, slide, resto) y crea un fichero para cada uno de ellos e integalos llamando a `@import`
- Definir al menos un `@mixin`
- Definir al menos un `@extend`
- Definir al menos una funcion.
- Inserta comentarios, y comprueba cono funcionan las directivas `@error`, `@warn` y `@debug` 
