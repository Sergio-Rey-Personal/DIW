# **Control de reproducción de vídeo y audio con JavaScript**

Tabla de contenidos

Como hemos visto en las secciones anteriores, los navegadores trabajan de forma diferente y algunos de los atributos de <audio> y <video> pueden estar o no habilitados por defecto.

# 9.1. Control de reproducción de vídeo y audio con JavaScript

Para poder controlar todos los elementos de nuestro reproductor podemos utilizar JavaScript y aprovechar los nuevos métodos, propiedades y eventos incorporados en HTML5.

## 9.1. Métodos

Para gestionar la reproducción de medios en HTML5 disponemos de una lista de métodos que se pueden llamar desde JavaScript. Los métodos más utilizados son los siguientes:

-   **play**(): comienza a reproducir el medio desde el inicio, siempre que el medio no haya sido pausado previamente.
-   **pause**(): pausa la reproducción.
-   **load**(): carga el archivo del medio. Es útil para cargar el medio anticipadamente.
-   **canPlayType(formato)**: para comprobar si el formato del archivo se soporta por el navegador.

Por ejemplo, si queremos iniciar la reproducción de un vídeo después de pulsar un botón haremos lo siguiente:

```html
 <video id="video" width="700" height="350">
    <source src="video.mp4">
    <source src="video.ogv">
</video>
<input type="button" id="boton" value="Reproducir">

<script>
function iniciar() {
   var boton=document.getElementById('boton');
   boton.addEventListener('click', presionar, false);
}
function presionar() {
   var video=document.getElementById('video');
   video.play();
}
window.addEventListener('load', iniciar, false);
</script>
```

## 9.2. Propiedades

Con HTML5 también disponemos de algunas propiedades que nos darán información sobre el medio, la mayoría de ellas son de lectura/escritura, por lo tanto, también podemos cambiar su valor. Las siguientes son las propiedades más utilizadas:

-   **paused**: tiene valor "true" si la reproducción del medio está actualmente pausada o no ha comenzado.
-   **ended**: tiene valor "true" si la reproducción del medio ha finalizado porque se llegó al final.
-   **duration**: contendrá la duración del medio en segundos.
-   **currentTime**: Esta propiedad de lectura/escritura contendrá un valor para informar sobre la posición en segundos en la cual el medio está siendo reproducido, o especifica una nueva posición donde continuar reproduciendo.
-   **error**: tiene el valor del error ocurrido.
-   **muted**: para desactivar (true) o activar (false) el sonido del vídeo.
-   **volume**: para indicar el volumen del vídeo. El valor del volumen debe ser un número entre 0 y 1, por ejemplo si indicamos medio.volume = 0.3 estaríamos configurando el volumen al 30%.

Por ejemplo, podemos cambiar la función presionar() del ejemplo anterior, para que se inicie la reproducción del vídeo al presionar el botón y se pause la reproducción si se vuelve a presionar. En el siguiente código, cambiamos también el texto del botón indicando la operación a realizar.

```javascript
function **presionar**() {
   if(!medio.paused && !medio.ended)   {
      medio.pause();
      reproducir.value='Reproducir';
   }
   else
   {
      medio.play();
      reproducir.value='Pausa';
   }
}
```

## 9.3. Eventos

También disponemos de diferentes eventos que nos permiten conocer la situación del medio. Los eventos más importantes son los siguientes:

-   **progress**: progreso de la descarga del medio. La información estará disponible a través del atributo buffered.
-   **canplaythrough**: se dispara cuando el medio completo puede ser reproducido sin interrupción.
-   **ended**: se dispara cuando el reproductor llega al final del medio.
-   **pause**: se dispara cuando el reproductor es pausado.
-   **play**: se dispara cuando el medio comienza a ser reproducido.
-   **error**: se dispara cuando ocurre un error.

[Más eventos JS](https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Media_events)