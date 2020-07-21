# 7. **Manipulación de elementos de DOM**

Tabla de contenidos

- [7. **Manipulación de elementos de DOM**](#7-manipulación-de-elementos-de-dom)
  - [7.1. Obtener y establecer información en elementos](#71-obtener-y-establecer-información-en-elementos)
  - [7.2. Mover, copiar y eliminar elementos](#72-mover-copiar-y-eliminar-elementos)
  - [7.3. Crear nuevos elementos](#73-crear-nuevos-elementos)
  - [7.4. Manipulación de atributos](#74-manipulación-de-atributos)


Una vez realizada la selección de los elementos que desea utilizar, *la diversión comienza*. Es posible cambiar, mover, eliminar y duplicar elementos. También crear nuevos a través de una sintaxis simple.

La documentación completa sobre los métodos de manipulación puede encontrarla en [la sección Manipulation](https://api.jquery.com/category/manipulation/).

## 7.1. Obtener y establecer información en elementos

Existen muchas formas por las cuales se puede modificar un elemento. Entre las tareas más comunes están las de cambiar el HTML interno o algún atributo del mismo. Para este tipo de tareas, jQuery ofrece métodos simples, funcionales en todos los navegadores modernos. Incluso es posible obtener información sobre los elementos utilizando los mismos métodos pero en su forma de método obtenedor.

> ***Nota***: Realizar cambios en los elementos, es un trabajo trivial, pero hay debe recordar que el cambio afectará a todos los elementos en la selección, por lo que, si desea modificar un sólo elemento, tiene que estar seguro de especificarlo en la selección antes de llamar al método establecedor.

> ***Nota***: Cuando los métodos actúan como obtenedores, por lo general, solamente trabajan con el primer elemento de la selección. Además no devuelven un objeto jQuery, por lo cual no es posible encadenar más métodos en el mismo. Una excepción es el método `$.fn.text`, el cual permite obtener el texto de los elementos de la selección.

- `$.fn.html` Obtiene o establece el contenido HTML de un elemento.
- `$.fn.text` Obtiene o establece el contenido en texto del elemento; en caso se pasarle como argumento código HTML, este es despojado.
- `$.fn.attr` Obtiene o establece el valor de un determinado atributo.
- `$.fn.width` Obtiene o establece el ancho en pixeles del primer elemento de la selección como un entero.
- `$.fn.height` Obtiene o establece el alto en pixeles del primer elemento de la selección como un entero.
- `$.fn.position` Obtiene un objeto con información sobre la posición del primer elemento de la selección, relativo al primer elemento padre posicionado. Este método es solo obtenedor.
- `$.fn.val` Obtiene o establece el valor (*value*) en elementos de formularios.

Veamos un ejemplo de cómo se cambiaria el HTML de un elemento

```javascript
$('#myDiv p:first').html('Nuevo <strong>primer</strong> párrafo');
```

## 7.2. Mover, copiar y eliminar elementos

Existen varias maneras para mover elementos a través del DOM; las cuales se pueden separar en dos enfoques:

- Querer colocar el/los elementos seleccionados de forma relativa a otro elemento
- Querer colocar un elemento relativo a el/los elementos seleccionados.

Por ejemplo, jQuery provee los métodos `$.fn.insertAfter` y `$.fn.after`. El método `$.fn.insertAfter` coloca a el/los elementos seleccionados después del elemento que se haya pasado como argumento; mientras que el método `$.fn.after` coloca al elemento pasado como argumento después del elemento seleccionado. Otros métodos también siguen este patrón: `$.fn.insertBefore` y `$.fn.before`; `$.fn.appendTo` y `$.fn.append`; y `$.fn.prependTo` y `$.fn.prepend`.

La utilización de uno u otro método dependerá de los elementos que tenga seleccionados y el tipo de referencia que se quiera guardar con respecto al elemento que se esta moviendo.

***Mover elementos utilizando diferentes enfoques***

```javascript
// hacer que el primer item de la lista sea el último
var $li = $('#myList li:first').appendTo('#myList');

// otro enfoque para el mismo problema
$('#myList').append($('#myList li:first'));

// debe tener en cuenta que no hay forma de acceder a la
// lista de items que se ha movido, ya que devuelve la lista en sí
```

***Clonar elementos***

Cuando se utiliza un método como `$.fn.appendTo`, lo que se está haciendo es mover al elemento; pero a veces en lugar de eso, se necesita mover un duplicado del mismo elemento. En este caso, es posible utilizar el método `$.fn.clone`.

***Obtener una copia del elemento***

```javascript
// copiar el primer elemento de la lista y moverlo al final de la misma
$('#myList li:first').clone().appendTo('#myList');
```

> ***Nota***: Si se necesita copiar información y eventos relacionados al elemento, se debe pasar `true` como argumento de `$.fn.clone`.

***Eliminar elementos***

Existen dos formas de eliminar elementos de una página: Utilizando `$.fn.remove` o `$.fn.detach`. Cuando desee eliminar de forma permanente al elemento, utilize el método `$.fn.remove`. Por otro lado, el método `$.fn.detach` también elimina el elemento, pero mantiene la información y eventos asociados al mismo, siendo útil en el caso que necesite reinsertar el elemento en el documento.

> ***Nota***: El método `$.fn.detach` es muy útil cuando se esta manipulando de forma severa un elemento, ya que es posible eliminar al elemento, trabajarlo en el código y luego restaurarlo en la página nuevamente. Esta forma tiene como beneficio no tocar el DOM mientras se está modificando la información y eventos del elemento.

Por otro lado, si se desea mantener al elemento pero se necesita eliminar su contenido, es posible utiliza el método `$.fn.empty`, el cual "vaciará" el contenido HTML del elemento.

## 7.3. Crear nuevos elementos

jQuery provee una forma fácil y elegante para crear nuevos elementos a través del mismo método `$()` que se utiliza para realizar selecciones.

***Crear nuevos elementos***

```javascript
$('<p>Un nuevo párrafo</p>');
$('<li class="new">nuevo item de la lista</li>');
```

***Crear un nuevo elemento con atributos utilizando un objeto***

```javascript
$('<a/>', {
    html : 'Un <strong>nuevo</strong> enlace',
    'class' : 'new',
    href : 'foo.html'
});
```

Puedes ver que en el objeto que se pasa como argumento, la propiedad `class` está entre comillas, mientras que la propiedad `href` y `html` no lo están. Por lo general, los nombres de propiedades no deben estar entre comillas, excepto en el caso que se utilice como nombre una palabra reservada (como es el caso de `class`).

Cuando se crea un elemento, éste no es añadido inmediatamente a la página, sino que se debe hacerlo en conjunto con un método.

***Crear un nuevo elemento en la página***

```javascript
var $myNewElement = $('<p>Nuevo elemento</p>');
$myNewElement.appendTo('#content');

// eliminará al elemento <p> existente en #content
$myNewElement.insertAfter('ul:last');

// clonar al elemento <p> para tener las dos versiones
$('ul').last().after($myNewElement.clone());
```

Estrictamente hablando, no es necesario guardar al elemento creado en una variable --- es posible llamar al método para añadir el elemento directamente después de `$()`. Sin embargo, la mayoría de las veces se deseará hacer referencia al elemento añadido, por lo cual, si se guarda en una variable no es necesario seleccionarlo después.

***Crear y añadir al mismo tiempo un elemento a la página***

```javascript
$('ul').append('<li>item de la lista</li>');
```

> ***Nota***:: La sintaxis para añadir nuevos elementos a la página es muy fácil de utilizar, pero es tentador olvidar que hay un costo enorme de rendimiento al agregar elementos al DOM de forma repetida. Si esta añadiendo muchos elementos al mismo contenedor, en lugar de añadir cada elemento uno por vez, lo mejor es concatenar todo el HTML en una única cadena de caracteres para luego anexarla al contenedor. Una posible solución es utilizar un array que posea todos los elementos, luego reunirlos utilizando `join` y finalmente anexarla.

```javascript
var myItems = [], $myList = $('#myList');

for (var i=0; i<100; i++) {
    myItems.push('<li>item ' + i + '</li>');
}

$myList.append(myItems.join(''));
```

## 7.4. Manipulación de atributos

Las capacidades para la manipulación de atributos que ofrece la biblioteca son extensos. La realización de cambios básicos son simples, sin embargo el método `$.fn.attr` permite manipulaciones más complejas.

***Manipular un simple atributo***

```javascript
$('#myDiv a:first').attr('href', 'newDestination.html');
```

***Manipular múltiples atributos***

```javascript
$('#myDiv a:first').attr({
    href : 'newDestination.html',
    rel : 'super-special'
});
```

***Utilizar una función para determinar el valor del nuevo atributo***

```javascript
$('#myDiv a:first').attr({
    rel : 'super-special',
    href : function(idx, href) {
        return '/new/' + href;
    }
});

$('#myDiv a:first').attr('href', function(idx, href) {
    return '/new/' + href;
});
```