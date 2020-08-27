# 1. **Tipos de diseño web ¿cuál utilizo?**

Tabla de contenidos

- [1. **Tipos de diseño web ¿cuál utilizo?**](#1-tipos-de-diseño-web-cuál-utilizo)
  - [1.1. Diseño fijo](#11-diseño-fijo)
  - [1.2. Diseño elástico](#12-diseño-elástico)
  - [1.3. Diseño líquido o fluido](#13-diseño-líquido-o-fluido)
  - [1.4. Diseño web responsivo o adaptable](#14-diseño-web-responsivo-o-adaptable)
  - [1.5. Diseño flexible](#15-diseño-flexible)
  - [1.6. ¿Qué tipo de diseño utilizo?](#16-qué-tipo-de-diseño-utilizo)

A la hora de crear una interfaz web existen **diferentes tipos de diseño**: diseño con tamaño fijo, diseño con unidades «em», diseño mediante porcentajes, diseño que se adapta mediante puntos de ruptura o diseño definido dentro de unos márgenes predefinidos. Es importante mencionar que  estos métodos **se pueden utilizar de forma combinada**. Veamos cada uno de estos métodos mediante un ejemplo.

## 1.1. Diseño fijo

El **diseño fijo** dispone de **medidas fijas** que no son modificadas para los distintos dispositivos. Por lo tanto, se trata de un diseño que **no cumple las normas de un diseño web responsivo o r*****esponsive web design***.


```css
body {
  width: 960px;
  margin: 0 auto;
}

h1 {
  text-align: center;
}

#datos, #principal {
  float: left;
  padding: 0;
  margin: 0;
}

#datos {
 width: 260px;
}

#principal {
  width: 700px;
}

#contenido {
  list-style-type: none;
  padding: 0;
}

#contenido li {
  float: left;
  width: 33%;
}
```

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>HTML & CSS: Curso práctico avanzado</title>
  </head>
  <body>
    <h1>HTML & CSS: Curso práctico avanzado</h1>

    <div id="datos">
      <h2>Datos del libro</h2>

      <ul>
        <li>Título: HTML & CSS: Curso práctico avanzado</li>
        <li>Autor: Sergio Luján Mora</li>
        <li>Editorial: Publicaciones Altaria</li>
        <li>Año de publicación: 2015</li>
        <li>ISBN: 978-84-944049-4-8</li>
      </ul>
    </div>

    <div id="principal">
      <h2>Descripción del libro</h2>

      <p>
        Aunque los inicios de Internet se remontan a los años sesenta, no ha
        sido hasta los años noventa cuando, gracias a la Web, se ha extendido su
        uso por todo el mundo. En pocos años, la Web ha evolucionado
        enormemente: se ha pasado de páginas sencillas, con pocas imágenes y
        contenidos estáticos que eran visitadas por unos pocos usuarios a
        páginas complejas, con contenidos dinámicos que provienen de bases de
        datos y que son visitadas por miles de usuarios al mismo tiempo.
      </p>

      <p>
        Todas las páginas están internamente construidas con la misma
        tecnología, con el Lenguaje de marcas de hipertexto (Hypertext Markup
        Language, HTML) y con las Hojas de estilo en cascada (Cascading Style
        Sheets, CSS).
      </p>

      <p>
        Este libro es adecuado para cualquiera que tenga interés en aprender a
        desarrollar sus propias páginas web. No son necesarios conocimientos
        previos para aprender con este libro, lo único que es necesario es saber
        utilizar un ordenador y saber navegar por la Web.
      </p>

      <h2>Contenido del libro</h2>

      <p>
        El contenido de este libro se estructura en tres apartados bien
        diferenciados:
      </p>

      <ul id="contenido">
        <li>
          En la primera parte del libro se trabajan conceptos generales que son
          necesarios para poder desarrollar páginas web; se explican conceptos
          de estructura física y estructura lógica (o estructura de navegación)
          de un sitio web. Se detalla cómo influye la estructura física en las
          URL o direcciones que se emplean a la hora de crear los enlaces de un
          sitio web. Pasando por el concepto de "estándar web", un término
          general que se emplea para refererirse a los estándares que define su
          funcionamiento como HTML y CSS, empleados para el desarrollo de las
          páginas web en el lado del cliente.
        </li>

        <li>
          En la segunda parte se trabaja HTML. Partiendo de la estructura básica
          de una página web, se explican las etiquetas de HTML que se utilizan
          para definir el texto, los enlaces, las listas, las tablas, los
          formularios y los elementos multimedia.
        </li>

        <li>
          En la tercera y última parte se explica CSS, el lenguaje que se emplea
          para definir el formato y la presentación de una página web. Se
          explica cómo utilizar el color, cómo definir la presentación del
          texto, de las tablas y de los formularios; cómo realizar
          transformaciones y transiciones con el fin de diseñar una página web.
        </li>
      </ul>
    </div>
  </body>
</html>
```

[Diseño fijo (Codepen)](https://codepen.io/sergio-rey-personal/pen/xxZrJgO)

## 1.2. Diseño elástico

En el diseño elástico se definen las **dimensiones** de la página **con unidades «em»**. De esta forma el diseño **se adaptará cuando el visitante del sitio cambie el tamaño del texto**, pero **no se adaptará en función de los cambios de tamaño de la ventana del navegador**.

Tal y como vimos en el apartado "[Unidades de medida en CSS](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_24_UnidadesDeMedidaCSS.md)" de la unidad 3, el «em» es una unidad relativa y su valor depende del tamaño de fuente definido en el navegador.

El «em» es una unidad de tipografía que mide exactamente el ancho de la letra «M» mayúscula de una tipografía dada y a un tamaño dado. Por tanto, un «em» no mide siempre lo mismo. Actualmente, el tamaño de fuente por defecto en todos los navegadores suele ser de 16 píxeles.

```css
/* styles.css */
body {
  width: 60em;
  margin: 0 auto;
}

h1 {
  text-align: center;
}

#datos, #principal {
  float: left;
  padding: 0;
  margin: 0;
}

#datos {
 width: 16em;
}

#principal {
  width: 44em;
}

#contenido {
  list-style-type: none;
  padding: 0;
}

#contenido li {
  float: left;
  width: 33%;
}
```

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>HTML & CSS: Curso práctico avanzado</title>
  </head>
  <body>
    <h1>HTML & CSS: Curso práctico avanzado</h1>

    <div id="datos">
      <h2>Datos del libro</h2>

      <ul>
        <li>Título: HTML & CSS: Curso práctico avanzado</li>
        <li>Autor: Sergio Luján Mora</li>
        <li>Editorial: Publicaciones Altaria</li>
        <li>Año de publicación: 2015</li>
        <li>ISBN: 978-84-944049-4-8</li>
      </ul>
    </div>

    <div id="principal">
      <h2>Descripción del libro</h2>

      <p>
        Aunque los inicios de Internet se remontan a los años sesenta, no ha
        sido hasta los años noventa cuando, gracias a la Web, se ha extendido su
        uso por todo el mundo. En pocos años, la Web ha evolucionado
        enormemente: se ha pasado de páginas sencillas, con pocas imágenes y
        contenidos estáticos que eran visitadas por unos pocos usuarios a
        páginas complejas, con contenidos dinámicos que provienen de bases de
        datos y que son visitadas por miles de usuarios al mismo tiempo.
      </p>

      <p>
        Todas las páginas están internamente construidas con la misma
        tecnología, con el Lenguaje de marcas de hipertexto (Hypertext Markup
        Language, HTML) y con las Hojas de estilo en cascada (Cascading Style
        Sheets, CSS).
      </p>

      <p>
        Este libro es adecuado para cualquiera que tenga interés en aprender a
        desarrollar sus propias páginas web. No son necesarios conocimientos
        previos para aprender con este libro, lo único que es necesario es saber
        utilizar un ordenador y saber navegar por la Web.
      </p>

      <h2>Contenido del libro</h2>

      <p>
        El contenido de este libro se estructura en tres apartados bien
        diferenciados:
      </p>

      <ul id="contenido">
        <li>
          En la primera parte del libro se trabajan conceptos generales que son
          necesarios para poder desarrollar páginas web; se explican conceptos
          de estructura física y estructura lógica (o estructura de navegación)
          de un sitio web. Se detalla cómo influye la estructura física en las
          URL o direcciones que se emplean a la hora de crear los enlaces de un
          sitio web. Pasando por el concepto de "estándar web", un término
          general que se emplea para refererirse a los estándares que define su
          funcionamiento como HTML y CSS, empleados para el desarrollo de las
          páginas web en el lado del cliente.
        </li>

        <li>
          En la segunda parte se trabaja HTML. Partiendo de la estructura básica
          de una página web, se explican las etiquetas de HTML que se utilizan
          para definir el texto, los enlaces, las listas, las tablas, los
          formularios y los elementos multimedia.
        </li>

        <li>
          En la tercera y última parte se explica CSS, el lenguaje que se emplea
          para definir el formato y la presentación de una página web. Se
          explica cómo utilizar el color, cómo definir la presentación del
          texto, de las tablas y de los formularios; cómo realizar
          transformaciones y transiciones con el fin de diseñar una página web.
        </li>
      </ul>
    </div>
  </body>
</html>
```

[Diseño elastico](https://codepen.io/sergio-rey-personal/pen/JjGJBLW)

## 1.3. Diseño líquido o fluido

El diseño líquido se adapta a la ventana del dispositivo, normalmente definiendo los tamaños mediante **porcentajes**. Sin embargo, este método perjudica la experiencia de usuario y no permite controlar el diseño ( el diseño varía constantemente según el tamaño del dispositivo y no se puede diseñar al píxel para todos los tamaños).

```css
/* styles.css */
body {
  width: 80%;
  margin: 0 auto;
}

h1 {
  text-align: center;
}

#datos, #principal {
  float: left;
  padding: 0;
  margin: 0;
}

#datos {
 width: 25%;
}

#principal {
  width: 75%;
}

#contenido {
  list-style-type: none;
  padding: 0;
}

#contenido li {
  float: left;
  width: 33%;
}
```

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>HTML & CSS: Curso práctico avanzado</title>
  </head>
  <body>
    <h1>HTML & CSS: Curso práctico avanzado</h1>

    <div id="datos">
      <h2>Datos del libro</h2>

      <ul>
        <li>Título: HTML & CSS: Curso práctico avanzado</li>
        <li>Autor: Sergio Luján Mora</li>
        <li>Editorial: Publicaciones Altaria</li>
        <li>Año de publicación: 2015</li>
        <li>ISBN: 978-84-944049-4-8</li>
      </ul>
    </div>

    <div id="principal">
      <h2>Descripción del libro</h2>

      <p>
        Aunque los inicios de Internet se remontan a los años sesenta, no ha
        sido hasta los años noventa cuando, gracias a la Web, se ha extendido su
        uso por todo el mundo. En pocos años, la Web ha evolucionado
        enormemente: se ha pasado de páginas sencillas, con pocas imágenes y
        contenidos estáticos que eran visitadas por unos pocos usuarios a
        páginas complejas, con contenidos dinámicos que provienen de bases de
        datos y que son visitadas por miles de usuarios al mismo tiempo.
      </p>

      <p>
        Todas las páginas están internamente construidas con la misma
        tecnología, con el Lenguaje de marcas de hipertexto (Hypertext Markup
        Language, HTML) y con las Hojas de estilo en cascada (Cascading Style
        Sheets, CSS).
      </p>

      <p>
        Este libro es adecuado para cualquiera que tenga interés en aprender a
        desarrollar sus propias páginas web. No son necesarios conocimientos
        previos para aprender con este libro, lo único que es necesario es saber
        utilizar un ordenador y saber navegar por la Web.
      </p>

      <h2>Contenido del libro</h2>

      <p>
        El contenido de este libro se estructura en tres apartados bien
        diferenciados:
      </p>

      <ul id="contenido">
        <li>
          En la primera parte del libro se trabajan conceptos generales que son
          necesarios para poder desarrollar páginas web; se explican conceptos
          de estructura física y estructura lógica (o estructura de navegación)
          de un sitio web. Se detalla cómo influye la estructura física en las
          URL o direcciones que se emplean a la hora de crear los enlaces de un
          sitio web. Pasando por el concepto de "estándar web", un término
          general que se emplea para refererirse a los estándares que define su
          funcionamiento como HTML y CSS, empleados para el desarrollo de las
          páginas web en el lado del cliente.
        </li>

        <li>
          En la segunda parte se trabaja HTML. Partiendo de la estructura básica
          de una página web, se explican las etiquetas de HTML que se utilizan
          para definir el texto, los enlaces, las listas, las tablas, los
          formularios y los elementos multimedia.
        </li>

        <li>
          En la tercera y última parte se explica CSS, el lenguaje que se emplea
          para definir el formato y la presentación de una página web. Se
          explica cómo utilizar el color, cómo definir la presentación del
          texto, de las tablas y de los formularios; cómo realizar
          transformaciones y transiciones con el fin de diseñar una página web.
        </li>
      </ul>
    </div>
    <a
      href="http://desarrolloweb.dlsi.ua.es/libros/html-css/ejercicio-maquetacion-diseno-fijo"
      >Acceso</a
    >
  </body>
</html>
```

[Diseño líquido](https://codepen.io/sergio-rey-personal/pen/QWygBrX)

## 1.4. Diseño web responsivo o adaptable

El diseño web r**esponsivo o** ***responsive web design*** (también llamado **adaptable o** ***adaptative***) se basa en el uso de *[**media queries**](https://www.eniun.com/media-queries-css-diseno-web-responsive/)*. Gracias a esta técnica podemos **definir estilos condicionales con puntos de ruptura o puntos de interrupción, aplicables únicamente en determinadas situaciones.**

Supongamos que queremos aplicar un estilo diferente en pantallas de ancho superior a 1200px, inferior a 1200px, e inferior a 600px, tendríamos las siguientes media queries para definir los estilos del ejemplo que hemos estado viendo:

```css
/* styles.css */ 
body {
  width: 80%;
  margin: 0 auto;
}

@media (min-width: 1201px) {
  h1 {
    text-align: center;
  }

  #datos, #descripcion, #contenido {
    float: left;
    padding: 0;
    margin: 0;
  }

  #datos {
   width: 33%;
  }

  #descripcion {
   width: 33%;
  }

  #contenido {
   width: 33%;
  }  
}

@media (min-width: 601px) and (max-width: 1200px) {
  h1 {
    text-align: center;
  }

  #datos, #principal {
    float: left;
    padding: 0;
    margin: 0;
  }

  #datos {
   width: 30%;
  }

  #principal {
    width: 70%;
  }

  #apartados {
    list-style-type: none;
    padding: 0;
  }

  #apartados li {
    float: left;
    width: 33%;
  }
}

@media (max-width: 600px) {
  #datos ul {
    padding-left: 0;
  }

  #datos li {
    display: inline;
  }
  
  #datos li:after {
    content: "; ";
  }
}
```

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />
    <title>HTML & CSS: Curso práctico avanzado</title>
  </head>
  <body>
    <h1>HTML & CSS: Curso práctico avanzado</h1>

    <div id="datos">
      <h2>Datos del libro</h2>

      <ul>
        <li>Título: HTML & CSS: Curso práctico avanzado</li>
        <li>Autor: Sergio Luján Mora</li>
        <li>Editorial: Publicaciones Altaria</li>
        <li>Año de publicación: 2015</li>
        <li>ISBN: 978-84-944049-4-8</li>
      </ul>
    </div>

    <div id="principal">
      <div id="descripcion">
        <h2>Descripción del libro</h2>

        <p>
          Aunque los inicios de Internet se remontan a los años sesenta, no ha
          sido hasta los años noventa cuando, gracias a la Web, se ha extendido
          su uso por todo el mundo. En pocos años, la Web ha evolucionado
          enormemente: se ha pasado de páginas sencillas, con pocas imágenes y
          contenidos estáticos que eran visitadas por unos pocos usuarios a
          páginas complejas, con contenidos dinámicos que provienen de bases de
          datos y que son visitadas por miles de usuarios al mismo tiempo.
        </p>

        <p>
          Todas las páginas están internamente construidas con la misma
          tecnología, con el Lenguaje de marcas de hipertexto (Hypertext Markup
          Language, HTML) y con las Hojas de estilo en cascada (Cascading Style
          Sheets, CSS).
        </p>

        <p>
          Este libro es adecuado para cualquiera que tenga interés en aprender a
          desarrollar sus propias páginas web. No son necesarios conocimientos
          previos para aprender con este libro, lo único que es necesario es
          saber utilizar un ordenador y saber navegar por la Web.
        </p>
      </div>

      <div id="contenido">
        <h2>Contenido del libro</h2>

        <p>
          El contenido de este libro se estructura en tres apartados bien
          diferenciados:
        </p>

        <ul id="apartados">
          <li>
            En la primera parte del libro se trabajan conceptos generales que
            son necesarios para poder desarrollar páginas web; se explican
            conceptos de estructura física y estructura lógica (o estructura de
            navegación) de un sitio web. Se detalla cómo influye la estructura
            física en las URL o direcciones que se emplean a la hora de crear
            los enlaces de un sitio web. Pasando por el concepto de "estándar
            web", un término general que se emplea para refererirse a los
            estándares que define su funcionamiento como HTML y CSS, empleados
            para el desarrollo de las páginas web en el lado del cliente.
          </li>

          <li>
            En la segunda parte se trabaja HTML. Partiendo de la estructura
            básica de una página web, se explican las etiquetas de HTML que se
            utilizan para definir el texto, los enlaces, las listas, las tablas,
            los formularios y los elementos multimedia.
          </li>

          <li>
            En la tercera y última parte se explica CSS, el lenguaje que se
            emplea para definir el formato y la presentación de una página web.
            Se explica cómo utilizar el color, cómo definir la presentación del
            texto, de las tablas y de los formularios; cómo realizar
            transformaciones y transiciones con el fin de diseñar una página
            web.
          </li>
        </ul>
      </div>
    </div>
  </body>
</html>
```

[Diseño adaptable](https://codepen.io/sergio-rey-personal/pen/YzwQjje)

## 1.5. Diseño flexible

Consiste en utilizar las propiedades CSS "**min-width**" y "**max-width**" para que las anchuras de los bloques puedan adaptarse dentro de unos mínimos y máximos.


## 1.6. ¿Qué tipo de diseño utilizo?

Qué tipo de método utilizar para nuestros proyectos es un tema muy debatido en la red porque crear un sitio web adaptable exige, en muchos casos, **combinar algunas de las técnicas que hemos estudiado**. Lo más habitual es declarar más de una *media query* para adaptar el diseño a múltiples dispositivos. Pero el número de puntos de interrupción y cómo se implementan estas técnicas **depende del diseño de nuestro sitio web**.

Así pues, lo ideal es utilizar un diseño web responsivo, preferentemente no elástico y con mezcla de diseño flexible y líquido según el contenedor. De este modo ofreceremos la **mejor experiencia de usuario** y podremos **considerar las distintas medidas de los dispositivos** utilizando tan solo HTML y CSS