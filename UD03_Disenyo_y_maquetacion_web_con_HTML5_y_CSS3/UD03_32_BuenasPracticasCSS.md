# 32. **Buenas prácticas CSS**

Tabla de contenidos

- [32. **Buenas prácticas CSS**](#32-buenas-prácticas-css)
  - [32.1. Organiza la estructura de arriba hacia abajo](#321-organiza-la-estructura-de-arriba-hacia-abajo)
  - [32.º2. Nombra correctamente los selectores](#32º2-nombra-correctamente-los-selectores)
  - [32.º3. Separa las palabras mediante guiones o mediante mayúsculas](#32º3-separa-las-palabras-mediante-guiones-o-mediante-mayúsculas)
  - [32.º4. Haz legible el CSS](#32º4-haz-legible-el-css)
  - [32.º5. Combina elementos](#32º5-combina-elementos)
  - [32.º6. Utiliza selectores descendientes](#32º6-utiliza-selectores-descendientes)
  - [32.º7. Utiliza las propiedades abreviadas](#32º7-utiliza-las-propiedades-abreviadas)
  - [32.º8. Utiliza nombres descriptivos en los selectores](#32º8-utiliza-nombres-descriptivos-en-los-selectores)
  - [32.º9. No utilices como nombre de un selector una característica visual](#32º9-no-utilices-como-nombre-de-un-selector-una-característica-visual)
  - [32.º10. Prueba el diseño en los diferentes navegadores](#32º10-prueba-el-diseño-en-los-diferentes-navegadores)
  - [32.º11. Valida tu CSS](#32º11-valida-tu-css)
  - [32.º12. Agrega los prefijos de los navegadores en propiedades que no sean estables](#32º12-agrega-los-prefijos-de-los-navegadores-en-propiedades-que-no-sean-estables)

Seguir unas pautas a la hora de crear tus estilos CSS hace que tu código sea más claro y legible tanto para ti y tus compañeros de proyecto, como para futuros desarrolladores que deban trabajar con tus implementaciones. Aunque no hay definido ningún estándar al respecto, es recomendable que sigas las siguientes recomendaciones para conseguir un desarrollo lo más entendible posible.

## 32.1. Organiza la estructura de arriba hacia abajo

Con el fin de encontrar rápidamente cualquier parte de código, es recomendable organizar los estilos de arriba hacia abajo e incluir los correspondientes comentarios.

```css
/****** generic classes*******/
styles goes here...
/****** header *******/
styles goes here...
/****** nav menu *******/
styles goes here...
/****** main content *******/
styles goes here...
/****** footer *******/
```

## 32.º2. Nombra correctamente los selectores

Para conseguir más claridad en el código y soporte en todos los navegadores conviene no comenzar el nombre de los selectores con mayúsculas, números ni caracteres especiales.

- Evitar: #1div, .=div, DivContent 
- Mejor utilizar: #div1, .div, divContent

## 32.º3. Separa las palabras mediante guiones o mediante mayúsculas

Elige una única manera de escribir el nombre de los selectores. Además, no utilices guiones bajos "_" u otros caracteres especiales ya que algunos navegadores no los soportan. Es recomendable seguir alguna de las siguientes opciones:

```css
/* Opción 1: Palabras separadas por mayúsculas */
navMenu { padding: 2em; border: 2px solid green; }

/* Opción 2: Palabras separadas por guiones */
nav-menu { padding: 2em; border: 2px solid green; }
```

## 32.º4. Haz legible el CSS

Adopta una única forma de escribir tu código para que sea más fácil de mantener y de encontrar cualquier elemento.

```css
/* Opción 1: Estilos en una línea */
.nav-menu { padding: 2em; border: 2px solid green; }

/* Opción 2: Cada estilo en una línea */
.nav-menu { 
      padding: 2em; 
      border: 2px solid green; 
}
```

## 32.º5. Combina elementos

Cuando varios elementos comparten propiedades es recomendable compartir las propiedades en vez de volver a repetir el código. Puedes utilizar [selectores combinados](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_23_SelectoresCSS.md#36-combinaci%C3%B3n-de-selectores).

```css
h1, h2, h3 { font-family: Arial; font-weight: 700;  }
```

## 32.º6. Utiliza selectores descendientes

Utiliza [selectores descendientes](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_23_SelectoresCSS.md#35-selector-descendiente) siempre que puedas antes de crear un selector clase o un selector identificador. El código estará más limpio, dispondrá de menos selectores clase e identificador y se comprenderá mucho mejor.

```css
selector1 selector2 selectorN{
        propiedad: valor;
}
```

## 32.º7. Utiliza las propiedades abreviadas

Reduce tu código usando las propiedades CSS abreviadas.

```css
/* Propiedades margin-left, margin-right y margin-top */
.nav-menu {margin-left: 5px; margin-right: 5px; margin-top: 5px;}
/* Propiedad abreviada margin */
.nav-menu {margin: 5px 5px 0px 5px;}
```

## 32.º8. Utiliza nombres descriptivos en los selectores

Utiliza nombres que te permitan averiguar fácilmente a qué elemento le estás dando estilo.

```css
.nav-button { background: blue; } /* Estilo del botón de la navbar*/
```

## 32.º9. No utilices como nombre de un selector una característica visual

Al utilizar en el nombre de un selector una característica visual como el color, el tamaño o la posición, si posteriormente modificamos esa característica, también deberíamos cambiar el nombre del selector. Esto complica mucho el código ya que tendríamos que actualizar todas las referencias a ese selector en HTML.

```css
/* Selector con nombre que define la característica visual del color */
.menu-red { background: red; }
/* Utiliza mejor: */
.nav-menu { background: red; }
```

## 32.º10. Prueba el diseño en los diferentes navegadores

Para descubrir si se producen errores de visualización en los navegadores lo recomendable es instalarlos todos en tu equipo. Algunos de los más utilizados son los siguientes:

- [Chrome](https://www.google.com/intl/es/chrome/)
- [Firefox](http://www.mozilla.com/en-US/firefox/all.html)
- [Opera](http://www.opera.com/download/)
- [Safari](http://www.apple.com/es/safari/)
- [Internet Explorer](https://www.microsoft.com/es-es/download/internet-explorer.aspx)

También puedes hacer uso de la aplicación [browserling](https://www.browserling.com/) que te permite ver tu desarrollo en varias versiones diferentes de cada navegador.

![](img/browserling-logo-cross-browser-testing.png)

## 32.º11. Valida tu CSS

Detecta errores en tu código mediante un validador CSS. El W3C proporciona una [herramienta de validación de CSS](https://jigsaw.w3.org/css-validator/) gratuita para los documentos CSS.

![validador CSS](img/validador-CSS.png)

## 32.º12. Agrega los prefijos de los navegadores en propiedades que no sean estables

Para ahorrar tiempo y facilitarnos la tarea de incluir los prefijos de las propiedades CSS que todavía no son estables podemos hacer uso de la[**extensión "Autoprefixer" en Visual Studio Code**](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_31_PrefijosNavegadoresCSS.md).