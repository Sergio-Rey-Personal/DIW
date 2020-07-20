# 5. **Atributos**

Tabla de contenidos

- [5. **Atributos**](#5-atributos)
  - [5.1. Establecer y obtener atributos](#51-establecer-y-obtener-atributos)
  - [5.2. Ejemplo de uso de selectores, clases y atributos](#52-ejemplo-de-uso-de-selectores-clases-y-atributos)

Los atributos de los elementos HTML que conforman una aplicación pueden contener información útil, por eso es importante poder establecer y obtener esa información.

## 5.1. Establecer y obtener atributos

El método `$.fn.attr` actúa tanto como método establecedor como obtenedor. Además, al igual que el método `$.fn.css`, cuando se lo utiliza como método establecedor, puede aceptar un conjunto de palabra clave-valor o un objeto conteniendo más conjuntos.

```javascript
$('a').attr('href', 'allMyHrefsAreTheSameNow.html');
$('a').attr({
    'title' : 'all titles are the same too',
    'href' : 'somethingNew.html'
});
```

En el ejemplo, el objeto pasado como argumento está escrito en varias líneas. Como se explicó anteriormente, los espacios en blanco no importan en JavaScript, por lo cual, es libre de utilizarlos para hacer el código más legible. En entornos de producción, se pueden utilizar herramientas de minificación, los cuales quitan los espacios en blanco (entre otras cosas) y comprimen el archivo final.

```javascript
var enlace = $('a').attr('href');  // devuelve el atributo href perteneciente
                                   // al primer elemento <a> del documento
```

## 5.2. Ejemplo de uso de selectores, clases y atributos

> [Ha llegado el momento de probar todo lo visto en los puntos anteriores mediante el siguiente ejemplo (Codesite)](https://codepen.io/sergio-rey-personal/pen/NWxejGQ)

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>CDN jQuery</title>

    <!-- Estilos Bootstrap CDN -->
    <link
      rel="stylesheet"
      href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css"
      integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm"
      crossorigin="anonymous"
    />
  </head>
  <body>
    <div id="contenido" class="division">
      <h1 id="idh1" class="text-center">texto uno H1</h1>
      <h1 id="idh2" class="text-center">texto dos H1</h1>
      <img src="" alt="" />
      <img src="" alt="" />
      <img src="" alt="" />
    </div>
    <div class="division" id="divagregar">
      <h1 id="idagrega" class="text-center">Agregar Clase</h1>
      <h2 id="idquita" class="text-center">Quitar Clase</h2>
    </div>

    <div class="container my-5" id="ideven">
      <button class="btn btn-primary" id="boton1">Agregar</button>
      <button class="btn btn-danger" id="boton2">Quitar</button>
      <button class="btn btn-warning" id="boton3">Toggle</button>

      <div class="bg-dark text-white mt-5 p-2" id="idcont">
        <h2>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Magnam,
          numquam!
        </h2>
      </div>
    </div>

    <!-- Aquí esta incorporado jQuery a través de un CDN -->
    <script>
      src="https://code.jquery.com/jquery-3.5.0.min.js"
      integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8="
      crossorigin="anonymous"
    </script>
    <script src="js/Selectores.js"></script>
  </body>
</html>
```

```javascript
$(document).ready(function () {
  $('h1').html('texto modificado con etiqueta h1');
  $('#idh1').html('texto modificado con ID');
  $('.text-center').html('texto modificado con clase');

  //Forma con Javascript de h1
  //document.querySelector('h1').innerHTML = 'Texto con etiqueta JS';
  //document.querySelectorAll('h1').forEach(element => { element.innerHTML = 'Texto con etiqueta JS'});
  //document.querySelector('#idh1').innerHTML = 'Texto con ID JS';
  //document.querySelector('.text-center').innerHTML = 'Texto con clase JS';

  // cambia el texto en todos los h1 de la clase
  // $(".division h1").html("cambio de texto");
  // cambia el texto en el primer h1 de la clase
  // $(".division h1:first").html("cambio de texto --> .division h1:first");
  // cambia el texto en ultimo h1 de la clase
  // $(".division h1:last").html("cambio de texto  --> .division h1:last");

  // Agrengando Clase addClass
  // $('#idagrega').addClass('text-danger');
  // En JavaScript 2 formas de añadir
  //document.querySelector('#idagrega').className +=' text-danger'
  //document.querySelector('#idagrega').className ='text-center text-danger'

  // Quitando Clase removeClass
  //$('#idagrega').removeClass('text-center');

  //añadir un elemento append / prepend
  //$('#contenido').append('<h1 class="text-center mb-5">Esta es la línea 3</h1><br>');
  //$('#contenido').prepend('<h1 class="text-center">Esta es la línea 0</h1>');

  // función css
  //$('#idquita').css('color', 'blue');
  // para múltiples propiedades.
  $("#idquita").css({ color: "blue", background: "salmon", padding: "20px" });

  // función remove / hide
  //$('#contenido').remove(); // lo elimina incluso de la consola
  //$('#idquita').hide(); // únicamente lo oculta.
  //let quitar = document.querySelector('#idquita')
  //console.log(quitar)

  // funcion attr

  //$('img').attr('src','PBHP.png'); // mete la imagen en todos los img
  //$('img:first').attr("width","80")
  //$('img:last').attr("width","100")

  //Evento click Agregando clase

  var parrafo = $("#idcont h2");
  $("#boton1").click(function () {
    parrafo.addClass("display-4"); //cambiamos la clase para h2
  });

  /*Evento click Agregando estilo en css*/
  $("#boton2").click(function () {
    parrafo.removeClass("display-4");
  });

  /*Alternativa al evento click*/
  $("#boton3").on("click", function () {
    parrafo.toggleClass("display-4");
  });
});
```

Vamos a probar cada uno de los usos que se pueden dar a esta página, y veremos como van variando los elementos que se presentan en la misma:

![JQuery Selectores Ejemplo](img/jquery-selectores-ejemplo.png)