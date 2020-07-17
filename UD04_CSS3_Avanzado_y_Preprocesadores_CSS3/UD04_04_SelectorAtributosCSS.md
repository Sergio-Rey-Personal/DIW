# 4. **Selector de atributos en CSS**

Tabla de contenidos

- [4. **Selector de atributos en CSS**](#4-selector-de-atributos-en-css)
      - [Ejemplo](#ejemplo)
- [Ejercicios propuestos](#ejercicios-propuestos)


En la unidad anterior vimos [pseudo-clases](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_30_PseudoClasesPsaudoElementosCSS.md) de CSS que nos permitían realizar una selección más específica de los elementos a los que queremos aplicar un cierto estilo. Por ejemplo, utilizábamos la jerarquía de los elementos para especificar la selección. En esta sección vamos a ver los selectores de atributos que nos permitirán también realizar una selección más específica de los elementos a los que queremos aplicar un cierto estilo en función de los atributos o valores que tengan asignados.

Los **selectores de atributos** permiten elegir elementos HTML en función de sus atributos y/o **valores** de esos atributos.

Los tipos de selectores de atributos son los siguientes:

-   [**nombre_atributo**], selecciona los elementos que tienen establecido el atributo llamado nombre_atributo independientemente de su valor. 

-   [**nombre_atributo=valor**], selecciona los elementos que tienen establecido un atributo llamado nombre_atributo con un valor igual a valor.

-   [**nombre_atributo~=valor**], selecciona los elementos que tienen establecido un atributo llamado nombre_atributo y al menos uno de los valores del atributo es valor.

-   [**nombre_atributo|=valor**], selecciona los elementos que tienen establecido un atributo llamado nombre_atributo, cuyo valor es una lista de valores, donde alguno comienza por valor.

-   [**nombre_atributo$=valor**] Selecciona aquellas etiquetas cuyo atributo acabe en ese valor.

-   [**nombre_atributo^=valor**] Selecciona aquellas etiquetas cuyo atributo comience por ese valor.

-   [**nombre_atributo\*=valor**] El atributo nombre_atributo existe y contiene valor.

#### Ejemplo

A continuación se muestran algunos ejemplos de estos tipos de selectores:

| Atributo | Descripción |
| --- | --- |
| `[href]` | El atributo `href` existe en la etiqueta. |
| `[href="#"]` | El atributo `href` existe y su valor es igual al texto `#`. |
| `[href\*="eniun"]` | El atributo `href` existe y su valor contiene el texto `eniun`. |
| `[href^="https://"]` | El atributo `href` existe y su valor comienza por `https://`. |
| `[href$=".pdf"]` | El atributo `href` existe y su valor termina por `.pdf` (es un enlace a un PDF). |
| `[class~="eniun"]` | El atributo `class` contiene una lista de valores, que contiene `eniun`. |
| `[lang|="es"]` | El atributo `lang` contiene una lista de valores, donde alguno empieza por `es-`. |

* Selecciona aquellas imágenes con extensión png:

```css
img[src=$png]						
```

* Se muestran de color azul todos los enlaces que tengan un atributo "class", independientemente de su valor:

```css
a[class] { color: blue; }
```

* Se muestran de color azul todos los enlaces que tengan un atributo "class" con el valor "externo":

```css
a[class="externo"] { color: blue; }
```

* Se muestran de color azul todos los enlaces que apunten al sitio "http://www.ejemplo.com".

```css
a[href="http://www.ejemplo.com"] { color: blue; }
```

* Se muestran de color azul todos los enlaces que tengan un atributo "class" en el que al menos uno de sus valores sea "externo". 

```css
a[class~="externo"] { color: blue; }
```

* Selecciona todos los elementos de la página cuyo atributo "lang" sea igual a "en", es decir, todos los elementos en inglés 

```css
*[lang=en] { ... }
```

* Selecciona todos los elementos de la página cuyo atributo "lang" empiece por "es", es decir, "es", "es-ES", "es-AR", etc. 

```css
[lang|="es"] { color : red }
```

# Ejercicios propuestos

-   Utiliza los selectores de atributos, la pseudo-clase :not y tus conocimientos de CSS para dibujar un borde rojo (border: 3px solid red;) a todas las imágenes que no tengan el atributo "alt". De esta forma nunca se te olvidará ponerlo.
-   Utiliza los selectores de atributos y el [pseudo-elemento](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_30_PseudoClasesPsaudoElementosCSS.md) after para añadir un icono de la imagen de pdf justo detrás de todos los enlaces que apunten a un pdf .