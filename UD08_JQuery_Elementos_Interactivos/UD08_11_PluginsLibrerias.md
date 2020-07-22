# 11. **Plugins y librerías en JQuery**

Tabla de contenidos

- [11. **Plugins y librerías en JQuery**](#11-plugins-y-librerías-en-jquery)
  - [11.1. Plugins](#111-plugins)
    - [11.1.1. `Validate`: Validando un formulario](#1111-validate-validando-un-formulario)
    - [11.1.2. `slick`: slide de imágenes.](#1112-slick-slide-de-imágenes)
    - [11.1.3. `Skippr`: slide de imágenes.](#1113-skippr-slide-de-imágenes)
  - [11.2. Creación de plugins](#112-creación-de-plugins)
  - [11.3. Librerías jQuery](#113-librerías-jquery)

## 11.1. Plugins

Otro de los puntos fuertes de JQuery es la gran comunidad que gira en torno a dicho proyecto aportando cientos de **plugins** que podemos utilizar de forma totalmente gratuita.

Para descargarlos accede al repositorio oficial de plugins haciendo clic en [este enlace](http://plugins.jquery.com/) y navega entre los etiquetados como más populares (animaciones, AJAX, formularios, etc.) o utiliza el buscador que encontrarás en la parte superior de la página. También puedes encontrar otros muchos buscando en la web.

![Plugins](img/jquery-plugins.png)

A continuación mostraremos algunos ejemplos prácticos de cómo integrar plugins de JQuery en una página web.

### 11.1.1. `Validate`: Validando un formulario

En este punto vamos a ver cómo utilizar uno de los mejores plugins existentes para **validar formularios** con JQuery, Validate, el cual dispone de varias métodos para comprobar que los componentes requeridos han sido rellenados y/o que el formato de los datos es el esperado.

Para descargarlo haz clic en [este enlace](http://bassistance.de/jquery-plugins/jquery-plugin-validation/) y a continuación pulsa en Download

Una vez descomprimido el archivo descargado entra en la carpeta dist y copia los archivos jquery.validate.min.js y additional-methods.min.js a nuestro proyecto, para luego enlazarlos en nuestras páginas web.

El primero de dichos archivos contiene el plugin en sí, y el segundo incorpora más métodos aún para relizar la validación.

Por otro lado, podemos extender las funcionalidades del plugin escribiendo otros métodos propios (en tal caso es recomendable guardarlos en un archivo aparte).

Algunos de los métodos de validación más útiles que incluye son (para más información consulta el enlace a la documentación facilitado más abajo):

- `required()`: especifica que el campo debe contener un valor.
- `minlength()` / `maxlength()`: permite indicar un número mínimo/máximo de caracteres que ha de contener.
- `rangelength()`: indica que el número de caracteres que puede contener el componente ha estar entre un rango especificado.
- `min()` / `max()`: permite indicar el valor mínimo/máximo que ha de contener.
- `range()`: indica que el valor ha de estar entre un rango específico.
- `email()`: especifica que el valor introducido debe tener formato de dirección de correo electrónico.
- `url()`: especifica que el valor introducido debe tener formato de dirección URL válida (comenzando por 'http://', 'https://' o 'ftp://').
- `number()`: indica que el valor introducido deberá ser numérico (entero o decimal).
- `digits()`: indica que el valor introducido deberá ser numérico (entero).
- `creditcard()`: indica que el valor introducido deberá tener formato de número de tarjeta de crédito.
- `equalTo()`: permite especificar que el valor introducido tendrá que ser el mismo que contenga otro campo (útil por ejemplo cuando queramos que el usuario confirme la contraseña o dirección E-Mail).
- `accept()`: en caso de usar un componente de formulario para seleccionar un archivo y enviarlo al servidor (hacer upload) permite indicar los tipos de archivo MIME que serán admitidos.
- `extension()`: como la opción anterior, pero permite indicar las extensiones de archivo que serán admitidas.

Por otro lado, si enlazamos el archivo additional-methods.min.js dispondremos entre otros de los siguientes métodos:

- `dateITA()`: admite fechas con formato 'dd/mm/yyyy'.
- `time()`: admite una hora en formato de 24 horas, entre 00:00 y 23:59.
- `time12h()`: admite una hora en formato de 12 horas (ej: '5:30 pm', '05:30 PM').
- `stripHtml()`: elimina tags HTML.
- `minWords()` / `maxWords()`: indica que el componente deberá contener un número mínimo/máximo de palabras.
- `rangeWords()`: indica que el componente podrá contener un número de palabras entre el rango que especifiquemos.
- `letterswithbasicpunc()`: permite que un cuadro de texto contenga sólo letras y unos determinados caracteres (guión medio, punto, coma, paréntesis, comillas simples o dobles y espacio).
- `nowhitespace()`: no permite que hayan espacios.
- `lettersonly()`: pemite que hayan letras únicamente.
- `alphanumeric()`: permite sólo letras, números y guiones bajos.
- `integer()`: admite sólo números enteros (positivos o negativos).
- `ipv4()`: dirección IP en formato IPV4.
- `ipv6()`: dirección IP en formato IPV6.

En caso de que el formulario haya sido cumplimentado de forma correcta tenemos la posibilidad de usar el método submitHandler() para procesar una función callback.

Veamos ahora un ejemplo donde podemo ver junto este plugin y Bootstrap.

[Ejemplo de Plugin de valicación con JQuery usando Bootstrap](https://github.com/jquery-validation/jquery-validation/blob/master/demo/bootstrap/index.html)

Cabe destacar la forma en la que se validan los campos: 

```javascript 
$(document).ready(function () {
  $("#signupForm1").validate({
    rules: {
      firstname1: "required",
      lastname1: "required",
      username1: {
        required: true,
        minlength: 2
      },
      password1: {
        required: true,
        minlength: 5
      },
      confirm_password1: {
        required: true,
        minlength: 5,
        equalTo: "#password1"
      },
      email1: {
        required: true,
        email: true
      },
      agree1: "required"
    },
    messages: {
      firstname1: "Please enter your firstname",
      lastname1: "Please enter your lastname",
      username1: {
        required: "Please enter a username",
        minlength: "Your username must consist of at least 2 characters"
      },
      password1: {
        required: "Please provide a password",
        minlength: "Your password must be at least 5 characters long"
      },
      confirm_password1: {
        required: "Please provide a password",
        minlength: "Your password must be at least 5 characters long",
        equalTo: "Please enter the same password as above"
      },
      email1: "Please enter a valid email address",
      agree1: "Please accept our policy"
    },
    errorElement: "em",
    errorPlacement: function (error, element) {
      // Add the `help-block` class to the error element
      error.addClass("help-block");

      // Add `has-feedback` class to the parent div.form-group
      // in order to add icons to inputs
      element.parents(".col-sm-5").addClass("has-feedback");

      if (element.prop("type") === "checkbox") {
        error.insertAfter(element.parent("label"));
      } else {
        error.insertAfter(element);
      }

      // Add the span element, if doesn't exists, and apply the icon classes to it.
      if (!element.next("span")[0]) {
        $(
          "<span class='glyphicon glyphicon-remove form-control-feedback'></span>"
        ).insertAfter(element);
      }
    },
    success: function (label, element) {
      // Add the span element, if doesn't exists, and apply the icon classes to it.
      if (!$(element).next("span")[0]) {
        $(
          "<span class='glyphicon glyphicon-ok form-control-feedback'></span>"
        ).insertAfter($(element));
      }
    },
    highlight: function (element, errorClass, validClass) {
      $(element)
        .parents(".col-sm-5")
        .addClass("has-error")
        .removeClass("has-success");
      $(element)
        .next("span")
        .addClass("glyphicon-remove")
        .removeClass("glyphicon-ok");
    },
    unhighlight: function (element, errorClass, validClass) {
      $(element)
        .parents(".col-sm-5")
        .addClass("has-success")
        .removeClass("has-error");
      $(element)
        .next("span")
        .addClass("glyphicon-ok")
        .removeClass("glyphicon-remove");
    }
  });
});
```

![Ejemplo plugin validate con bootstrap](img/jquery-plugin-validate.png)
https://jqueryvalidation.org/files/demo/bootstrap/index.html

> [Ejemplo de validación de formularios con plugin de validación y Bootstrap](https://codepen.io/sergio-rey-personal/pen/QWyYvQw)

Observa que por cada opción de validación definida en `rules` definimos otra en `messages`, y que en caso de que un componente tenga definida una sola regla basa con especificar un mensaje entre comillas.

Fíjate también en que dentro de `messages` es posible incluir código HTML.

### 11.1.2. `slick`: slide de imágenes.

Este componente es muy versatil para poder realizar slides de imágenes.

En la página web del proyecto [slick](http://kenwheeler.github.io/slick/) puedes ver su funcionalidad.

### 11.1.3. `Skippr`: slide de imágenes.

Otro plugin JQuery para realización de slides muy sencillos y vistosos

Visita su web para ver sus capacidades [skippr](http://austenpayan.github.io/skippr/)

## 11.2. Creación de plugins

Los plugins en jQuery se crean asignando una función a la propiedad "fn" del objeto jQuery. A partir de entonces, esas funciones asignadas se podrán utilizar en cualquier objeto jQuery, como uno de los muchos métodos que dispone dicho objeto principal del framework.

La creación de plugins, para ampliar las funcionalidades de jQuery, es una cosa tan básica que la mayoría de las funciones con las que está dotado el propio framework están incluidas en el objeto jQuery por medio de plugins. Es decir, en la construcción del framework en muchas de las ocasiones simplemente se crean plugins para extenderlo. Así pues, esta técnica es usada, no sólo por terceros desarrolladores, para crear nuevos componentes, sino también por el propio equipo de jQuery para el diseño base de este framework.

Si lo deseamos, aparte de seguir los próximos artículos de este manual, podemos ver el código fuente del framework o cómo están hechos los plugins de otros desarrolladores, para tener una idea sobre cómo se utilizan.

A modo de ejemplo, podemos ver a continuación un código fuente de un plugin muy sencillo:

```javascript
jQuery.fn.desaparece = function() {
   this.each(function(){
      elem = $(this);
      elem.css("display", "none");
   });   
   return this;
};
```

Este plugin permitiría hacer desaparecer a los elementos de la página y podríamos invocarlo por ejemplo de la siguiente manera:

```javascript
$("h1").desaparece();
```

## 11.3. Librerías jQuery

Podemos enriquecer nuestras interfaces mediante diferentes librerías. Veamos algunas de ellas:

- jqueryui.com : con diversos componentes para realizar interacciones, efectos, elementos interactios de deseño... 
- jquerymobile.com : librería para la realización de páginas resonsives.
