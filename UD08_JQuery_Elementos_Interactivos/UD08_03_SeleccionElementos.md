# 3. **Selección de elementos**

Tabla de contenidos

- [3. **Selección de elementos**](#3-selección-de-elementos)
  - [3.1. Técnicas de selección.](#31-técnicas-de-selección)
    - [3.1.1. Selección de elementos en base a su `id`](#311-selección-de-elementos-en-base-a-su-id)
    - [3.1.2. Selección de elementos en base al ***nombre de clase***](#312-selección-de-elementos-en-base-al-nombre-de-clase)
    - [3.1.3. Selección de elementos ***por su atributo***](#313-selección-de-elementos-por-su-atributo)
    - [3.1.4. Selección de elementos en forma de ***selector CSS***](#314-selección-de-elementos-en-forma-de-selector-css)
    - [3.1.5. Pseudo-selectores](#315-pseudo-selectores)
    - [3.1.6. Elección de selectores](#316-elección-de-selectores)
    - [3.2. Comprobar selecciones](#32-comprobar-selecciones)
    - [3.3. Guardar selecciones](#33-guardar-selecciones)
  - [3.4. Refinamiento y filtrado de selecciones](#34-refinamiento-y-filtrado-de-selecciones)
  - [3.5. Selección de elementos de un formulario](#35-selección-de-elementos-de-un-formulario)
  - [3.6. Trabajar con selecciones](#36-trabajar-con-selecciones)
    - [3.6.1. Encadenamiento](#361-encadenamiento)
    - [3.6.2. Obtenedores (*getters*) y establecedores (*setters*)](#362-obtenedores-getters-y-establecedores-setters)

El concepto más básico de jQuery es el de *"seleccionar algunos elementos y realizar acciones con ellos"*. La biblioteca soporta gran parte de los selectores CSS3 y varios más no estandarizados. En [api.jquery.com/category/selectors](https://api.jquery.com/category/selectors/) se puede encontrar una completa referencia sobre los selectores de la biblioteca.

## 3.1. Técnicas de selección.

A continuación se muestran algunas técnicas comunes para la selección de elementos:

### 3.1.1. Selección de elementos en base a su `id`

```javascript
$('#myId'); // notar que los IDs deben ser únicos por página
```

### 3.1.2. Selección de elementos en base al ***nombre de clase***

```javascript
$('div.myClass'); // si se especifica el tipo de elemento,
                  // se mejora el rendimiento de la selección
```

### 3.1.3. Selección de elementos ***por su atributo***

```javascript
$('input[name=first_name]'); // cuidado, que puede ser muy lento
```

### 3.1.4. Selección de elementos en forma de ***selector CSS***

```javascript
$('#contents ul.people li');
```

### 3.1.5. Pseudo-selectores

```javascript
// selecciona el primer elemento <a> con la clase 'external'
$('a.external:first');

// selecciona todos los elementos <tr> impares de una tabla
$('tr:odd');

// selecciona todos los elementos del tipo input dentro del formulario #myForm
$('#myForm:input');

// selecciona todos los divs visibles
$('div:visible');

// selecciona todos los divs excepto los tres primeros
$('div:gt(2)');

// selecciona todos los divs actualmente animados
$('div:animated');
```

> **Nota**: Cuando se utilizan los pseudo-selectores `:visible` y `:hidden`, jQuery comprueba la visibilidad actual del elemento pero no si éste posee asignados los estilos CSS `visibility` o `display` --- en otras palabras, verifica si el alto y ancho físico del elemento es mayor a cero. Sin embargo, esta comprobación no funciona con los elementos `<tr>`; en este caso, jQuery comprueba si se está aplicando el estilo `display` y va a considerar al elemento como oculto si posee asignado el valor `none`. Además, los elementos que aún no fueron añadidos al DOM serán tratados como ocultos, incluso si tienen aplicados estilos indicando que deben ser visibles (En la sección Manipulación de este manual, se explica como crear y añadir elementos al DOM).

Como referencia, este es el fragmento de código que utiliza jQuery para determinar cuando un elemento es visible o no. Se incorporaron los comentarios para que quede más claro su entendimiento:

```javascript
jQuery.expr.filters.hidden = function( elem ) {
    var width = elem.offsetWidth, height = elem.offsetHeight,
        skip = elem.nodeName.toLowerCase() === "tr";

    // ¿el elemento posee alto 0, ancho 0 y no es un <tr>?
    return width === 0 && height === 0 && !skip ?

        // entonces debe estar oculto (hidden)
        true :

        // pero si posee ancho y alto y no es un <tr>
        width > 0 && height > 0 && !skip ?

            // entonces debe estar visible
            false :

            // si nos encontramos aquí, es porque el elemento posee ancho
            // y alto, pero además es un <tr>,
            // entonces se verifica el valor del estilo display
            // aplicado a través de CSS
            // para decidir si está oculto o no
            jQuery.curCSS(elem, "display") === "none";
};

jQuery.expr.filters.visible = function( elem ) {
    return !jQuery.expr.filters.hidden( elem );
};
``` 

### 3.1.6. Elección de selectores

La elección de buenos selectores es un punto importante cuando se desea mejorar el rendimiento del código. Una pequeña especificidad --- por ejemplo, incluir el tipo de elemento (como `div`) cuando se realiza una selección por el nombre de clase --- puede ayudar bastante. Por eso, es recomendable darle algunas "pistas" a jQuery sobre en que lugar del documento puede encontrar lo que desea seleccionar. Por otro lado, demasiada especificidad puede ser perjudicial. Un selector como `#miTabla thead tr th.especial` es un exceso, lo mejor sería utilizar `#miTabla th.especial`.

JQuery ofrece muchos selectores basados en atributos, que permiten realizar selecciones basadas en el contenido de los atributos utilizando simplificaciones de expresiones regulares.

```javascript
// encontrar todos los <a> cuyo atributo rel terminan en "thinger"
$("a[rel$='thinger']");
```

Estos tipos de selectores pueden resultar útiles pero también ser muy lentos. Cuando sea posible, es recomendable realizar la selección utilizando IDs, nombres de clases y nombres de etiquetas.

### 3.2. Comprobar selecciones

Una vez realizada la selección de los elementos, querrá conocer si dicha selección entregó algún resultado. Para ello, pueda que escriba algo así:

```javascript
if ($('div.foo')) { ... }
```

Sin embargo esta forma no funcionará. Cuando se realiza una selección utilizando `$()`, siempre es devuelto un objeto, y si se lo evalúa, éste siempre devolverá true. Incluso si la selección no contiene ningún elemento, el código dentro del bloque `if` se ejecutará.

En lugar de utilizar el código mostrado, lo que se debe hacer es preguntar por la cantidad de elementos que posee la selección que se ejecutó. Esto es posible realizarlo utilizando la propiedad JavaScript `length`. Si la respuesta es `0`, la condición evaluará falso, caso contrario (más de `0` elementos), la condición será verdadera.

```javascript
if ($('div.foo').length) { ... }
```

### 3.3. Guardar selecciones

Cada vez que se hace una selección, una gran cantidad de código es ejecutado. jQuery no guarda el resultado por si solo, por lo tanto, si va a realizar una selección que luego se hará de nuevo, deberá salvar la selección en una variable.

```javascript
var $divs = $('div');
```

> **Nota**: En el ejemplo "Guardar selecciones en una variable", la variable comienza con el signo de dólar. Contrariamente a otros lenguajes de programación, en JavaScript este signo no posee ningún significado especial --- es solamente otro carácter. Sin embargo aquí se utilizará para indicar que dicha variable posee un objeto jQuery. Esta práctica --- una especie de [Notación Húngara](https://es.wikipedia.org/wiki/Notaci%C3%B3n_h%C3%BAngara) --- es solo una convención y no es obligatoria.

Una vez que la selección es guardada en la variable, se la puede utilizar en conjunto con los métodos de jQuery y el resultado será igual que utilizando la selección original.

La selección obtiene sólo los elementos que están en la página cuando se realizó dicha acción. Si luego se añaden elementos al documento, será necesario repetir la selección o añadir los elementos nuevos a la selección guardada en la variable. En otras palabras, las selecciones guardadas no se actualizan *mágicamente* cuando el DOM se modifica.

## 3.4. Refinamiento y filtrado de selecciones

A veces, puede obtener una selección que contiene más de lo que necesita; en este caso, es necesario refinar dicha selección. jQuery ofrece varios métodos para poder obtener exactamente lo que desea.

```javascript
$('div.foo').has('p');          // el elemento div.foo contiene elementos <p>
$('h1').not('.bar');            // el elemento h1 no posse la clase 'bar'
$('ul li').filter('.current');  // un item de una lista desordenada
                                // que posse la clase 'current'
$('ul li').first();             // el primer item de una lista desordenada
$('ul li').eq(5);               // el sexto item de una lista desordenada
``` 

## 3.5. Selección de elementos de un formulario

jQuery ofrece varios pseudo-selectores que ayudan a encontrar elementos dentro de los formularios, éstos son especialmente útiles ya que dependiendo de los estados de cada elemento o su tipo, puede ser difícil distinguirlos utilizando selectores CSS estándar.

-   `:button` Selecciona elementos `<button>` y con el atributo `type='button'`
-   `:checkbox` Selecciona elementos `<input>` con el atributo `type='checkbox'`
-   `:checked` Selecciona elementos `<input>` del tipo checkbox seleccionados
-   `:disabled` Selecciona elementos del formulario que están deshabitados
-   `:enabled` Selecciona elementos del formulario que están habilitados
-   `:file` Selecciona elementos `<input>` con el atributo `type='file'`
-   `:image` Selecciona elementos `<input>` con el atributo `type='image'`
-   `:input` Selecciona elementos `<input>`, `<textarea>` y `<select>`
-   `:password` Selecciona elementos `<input>` con el atributo `type='password'`
-   `:radio` Selecciona elementos `<input>` con el atributo `type='radio'`
-   `:reset` Selecciona elementos `<input>` con el atributo `type='reset'`
-   `:selected` Selecciona elementos `<options>` que están seleccionados
-   `:submit` Selecciona elementos `<input>` con el atributo `type='submit'`
-   `:text` Selecciona elementos `<input>` con el atributo `type='text'`

```javascript
// obtiene todos los elementos inputs dentro del formulario #myForm
$('#myForm :input');
```

## 3.6. Trabajar con selecciones

Una vez realizada la selección de los elementos, es posible utilizarlos en conjunto con diferentes métodos. éstos, generalmente, son de dos tipos: obtenedores (en inglés *getters*) y establecedores (en inglés *setters*). Los métodos obtenedores devuelven una propiedad del elemento seleccionado; mientras que los métodos establecedores fijan una propiedad a todos los elementos seleccionados.

### 3.6.1. Encadenamiento

Si en una selección se realiza una llamada a un método, y éste devuelve un objeto jQuery, es posible seguir un "encadenado" de métodos en el objeto.

```javascript
$('#content').find('h3').eq(2).html('nuevo texto para el tercer elemento h3');
```

Por otro lado, si se está escribiendo un encadenamiento de métodos que incluyen muchos pasos, es posible escribirlos línea por línea, haciendo que el código luzca más agradable para leer.

```javascript
$('#content')
    .find('h3')
    .eq(2)
    .html('nuevo texto para el tercer elemento h3');
```

Si deseas volver a la selección original en el medio del encadenado, jQuery ofrece el método `$(elem).end` para poder hacerlo.

```javascript
$('#content')
    .find('h3')
    .eq(2)
        .html('nuevo texto para el tercer elemento h3')
    .end() // reestablece la selección a todos los elementos h3 en #content
    .eq(0)
        .html('nuevo texto para el primer elemento h3');
```

> **Nota**; El encadenamiento es muy poderoso y es una característica que muchas bibliotecas JavaScript han adoptado desde que jQuery se hizo popular. Sin embargo, debe ser utilizado con cuidado. Un encadenamiento de métodos extensivo pueden hacer un código extremadamente difícil de modificar y depurar. No existe una regla que indique que tan largo o corto debe ser el encadenado --- pero es recomendable que tenga en cuenta este consejo.

### 3.6.2. Obtenedores (*getters*) y establecedores (*setters*)

jQuery "sobrecarga" sus métodos, en otras palabras, el método para establecer un valor posee el mismo nombre que el método para obtener un valor. Cuando un método es utilizado para establecer un valor, es llamado método establecedor (en inglés *setter*). En cambio, cuando un método es utilizado para obtener (o leer) un valor, es llamado obtenedor (en inglés *getter*).

```javascript
/*El método $(elem).html utilizado como establecedor*/
$('h1').html('hello world');

/*El método html utilizado como obtenedor*/
var textoHTML = $('h1').html();
```

Los métodos establecedores devuelven un objeto jQuery, permitiendo continuar con la llamada de más métodos en la misma selección, mientras que los métodos obtenedores devuelven el valor por el cual se consultó, pero no permiten seguir llamando a más métodos en dicho valor.

