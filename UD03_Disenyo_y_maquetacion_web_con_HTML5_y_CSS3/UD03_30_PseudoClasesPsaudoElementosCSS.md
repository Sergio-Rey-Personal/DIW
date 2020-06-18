# **Pseudo-clases y pseudo-elementos en CSS**

Tabla de contenidos

-   [10. Pseudo-clases y pseudo-elementos en CSS](#10-Pseudo-clases-y-pseudo-elementos-en-CSS)
    -   [10.1. Pseudo-clases para selección de hijos o hermanos](#101-Pseudo-clases-para-seleccin-de-hijos-o-hermanos)
    -   [10.2. Pseudo-clases para los estados de un elemento](#102-Pseudo-clases-para-los-estados-de-un-elemento)
    -   [10.3. Pseudo-elementos](#103-Pseudo-elementos)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

# 10. Pseudo-clases y pseudo-elementos en CSS

Gracias a las pseudo-clases y los pseudo-elementos de CSS podemos realizar una selección más específica de los elementos a los que queremos aplicar un cierto estilo sin necesidad de crear una clase concreta.

## 10.1. Pseudo-clases para selección de hijos o hermanos

| Pseudo-clase | Descripción |
| --- | --- |
| :first-child | Primer hijo |
| :last-child | Último hijo |
| :first-of-type | Primer hermano de su tipo |
| :last-of-type | Último hermano de su tipo |
| :only-child | Hijos únicos |
| :only-of-type | Únicos hermanos de su tipo |
| :empty | Elementos que no tienen hijos |
| :nth-child(n) | Enésimo elemento hijo |
| :nth-last-child(n) | Enésimo elemento hijo contando desde el útimo |
| :nth-of-type(n) | Enésimo hermano de su tipo |
| :nth-last-of-type(n) | Enésimo hermano de su tipo comenzando desde el último |

```css
p:first-child{ color: red; } 
p:last-child{ color: green; } 
```

```html
<div>
    <p>Primer párrafo</p>
    <p>Segundo párrafo</p>
    <p>Tercer párrafo</p>
    <p>Cuarto párrafo</p>
</div>
<span>
    <p>Primer párrafo</p>
    <p>Segundo párrafo</p>
    <p>Tercer párrafo</p>
    <p>Cuarto párrafo</p>
</span>
<div>
    <h1>Título</h1>
    <p>Primer párrafo</p>
    <p>Segundo párrafo</p>
    <p>Tercer párrafo</p>
    <p>Cuarto párrafo</p>
</div>
```
[CSS3.  Pseudo-clases](https://codepen.io/sergio-rey-personal/pen/MWKbOXQ)

### Pseudo-clase nth-child

Veamos como funciona la pseudo-clase `nth-child` mediante un ejemplo en el que aprovechamos la jerarquía de los elementos para referenciar una etiqueta:

En el código siguiente tenemos cuatro elementos `<p>` que son hermanos entre sí e hijos del elemento `<div>`.

```html
<div>
    <p>Primer párrafo</p>
    <p>Segundo párrafo</p>
    <p>Tercer párrafo</p>
    <p>Cuarto párrafo</p>
</div>
```

Utilizando la pseudo-clase nth-child() podemos seleccionar un hijo específico. El número que indiquemos entre paréntesis será la posición del hijo.

En el siguiente código, seleccionaremos todos los párrafos que sean el primer hijo de un contenedor (div, span, etc.).

```css
p:nth-child(1){ color: red; }
```

### Valores *odd* (impar) y *even* (par)

Los valores *odd* y *even* son muy útiles para seleccionar elementos pares e impares. El valor *`even`* representa elementos en posición par y el valor *`odd`* representa los elementos en posición impar.

### Ejemplos:

`tr:nth-child(odd)` o `tr:nth-child(2n+1)`Selecciona las filas impares de una tabla.

`tr:nth-child(even)` o `tr:nth-child(2n)`Selecciona las filas pares de una tabla.

`:nth-child(7)`Selecciona el séptimo elemento.

`:nth-child(6n)`Selecciona los elementos 6, 12, 18, etc.

`:nth-child(3n+4)`Selecciona los elementos 4, 7, 10, 13, etc.

## 10.2. Pseudo-clases para los estados de un elemento

Podemos utilizar diferentes pseudo-clases para definir las propiedades de ciertos elementos con diferentes estados. Uno de los usos más comunes es en los enlaces `<a>` aunque se pueden aplicar en otros elementos.

| Pseudo-clase | Descripción |
| --- | --- |
| :link | No visitado por el usuario |
| :visited | Visitado por el usuario |
| :hover | Modifica el estilo cuando un elemento apuntador pasa por encima |
| :active | Se activa cuando el usuario pulsa el elemento |
| :focus | Se activa cuando tiene el foco sobre el elemento |

```css
a:hover{ /*Elemento apuntador pasa por encima*/
  text-decoration: overline;
}
a:active{ /*Se activa cuando el usuario pulsa el elemento*/
  background-color: yellow;
}
a:link{ /*No visitado por el usuario*/
  color: green;
}
```

```html
<a href="https://www.w3schools.com">w3schools.com</a>
<a href="https://www.wikipedia.org">wikipedia.org</a>
<a href="https://www.google.com">google.com</a>
```
[CSS3. Pseudo-clases 2](https://codepen.io/sergio-rey-personal/pen/YzwpEMX)

## 10.3. Pseudo-elementos

| Pseudo-elemento | Descripción |
| :first-line | Primera línea de texto de un elemento |
| :first-letter | Primera letra de la primera línea de texto de un elemento |
| :before | Añade contenido al principio del documento |
| :after | Añade contenido al final del documento |

```css
p:first-line{
  color: green;
}
h2:first-letter{
  color: blue;
}
p:after {
  content: " - Aloja more don";
  color: red;
}
p:before {
  content: "*. ";
}
```

```html
<h2>Ed ut perspiciatis unde omnis iste natus error sit voluptatem</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
<h2>Ut enim ad minima veniam, quis nostrum exercitationem</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
```

[CSS3. Pseudo-elementos](https://codepen.io/sergio-rey-personal/pen/GRoNOaq)

> [Ver más pseudo-clases](https://www.w3schools.com/css/css_pseudo_classes.asp)

# Ejercicios propuestos

-   Utiliza el pseudo-elemento ":first-child" para darle un color de fondo a la primera fila de cada tabla.
-   Utiliza la pseudo-clase ":nth-child(argumento)" con el argumento "odd" y "even" para poner el fondo de las filas impares de un color y el de las filas pares de otro color.
-   Define las siguientes pseudo-clases para los estados de los enlaces de tu proyecto :link, :visited, :hover, :active. Ten en cuenta que tienes enlaces en el `<aside>`, en el `<nav>`, en el `<footer>` y también cualquier enlace que se pueda incluir en una entrada. Recuerda utilizar [selectores descendientes](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03%20Dise%C3%B1o%20y%20Maquetaci%C3%B3n%20web%20con%20HTML5%20y%20CSS3/UD03_23_SelectoresCSS.md#35-selector-descendiente) y [combinación de selectores](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03%20Dise%C3%B1o%20y%20Maquetaci%C3%B3n%20web%20con%20HTML5%20y%20CSS3/UD03_23_SelectoresCSS.md#36-combinaci%C3%B3n-de-selectores) siempre que sea posible.