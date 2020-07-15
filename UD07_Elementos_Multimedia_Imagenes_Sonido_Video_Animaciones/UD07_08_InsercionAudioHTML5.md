# **Inserción de audio en HTML5**

Tabla de contenidos

- [8. Inserción de audio en HTML5](#8-inserción-de-audio-en-html5)
  - [8.1. Atributos elemento <audio>](#81-atributos-elemento-audio)
  - [8.2. Soporte navegadores](#82-soporte-navegadores)
  - [8.3. Tipos MIME](#83-tipos-mime)


# 8. Inserción de audio en HTML5

El elemento <audio> de HTML5 dispone de prácticamente los mismos atributos que el elemento <video> visto en la sección anterior:

## 8.1. Atributos elemento <audio>

El elemento <audio> dispone de varios atributos que nos permiten establecer sus diferentes valores de comportamiento.

| Attribute | Value | Description | 
| --- | --- | --- |
| [autoplay](https://www.w3schools.com/tags/att_audio_autoplay.asp) | autoplay | al incluir este atributo, el navegador reproduce el audio automáticamente. |
| [controls](https://www.w3schools.com/tags/att_audio_controls.asp) | controls | muestra los controles de audio que nos ofrece el navegador. Cuando se incluye el atributo el navegador activará su propia interface de control del audio. De esta forma el usuario podrá reproducir el audio, pararlo, etc. | 
| [loop](https://www.w3schools.com/tags/att_audio_loop.asp) | loop | al incluir este atributo, el navegador reproduce nuevamente el audio cuando llega a su fin | 
| [muted](https://www.w3schools.com/tags/att_audio_muted.asp) | muted | Indica que el audio será silenciado por defecto al cargar |
| [preload](https://www.w3schools.com/tags/att_audio_preload.asp) | auto | descarga el archivo lo más pronto posible |
| | metadata | recomienda al navegador que capture información acerca de la fuente (duración). | 
| | none | el audio no se cachea. |
| [src](https://www.w3schools.com/tags/att_audio_src.asp) | [URL] | indica la URL del archivo de audio. Este atributo puede ser reemplazado por el elemento <source> y su propio atributo src para declarar varias fuentes con diferentes formatos. En el siguiente ejemplo el navegador leerá la etiqueta <source> y decidirá qué archivo reproducir de acuerdo a los formatos que soporte. | 

## 8.2. Soporte navegadores

MP3 está bajo licencia comercial, así que no es soportado por navegadores como Firefox u Opera. OGG es soportado por estos navegadores, pero no por Safari e Internet Explorer. Por este motivo, es **necesario subir los dos tipos (OGG y MP3) de archivos en nuestras páginas web**.

## 8.3. Tipos MIME

**Conviene especificar el contenido de un audio para que el navegador sepa identificar el tipo de formatos de nuestros archivos y sepa cómo manejarlos**. En el siguiente ejemplo el navegador elegirá solamente un audio. Al especificar el atributo type (no obligatorio), permitimos que el navegador conozca el tipo MIME y los tipos de codecs que debe utilizar antes de descargar el audio. Si no indicamos dicho atributo, el navegador intentará averiguar, mediante prueba y error, cuál es el tipo adecuado.

```html
<audio id="medio" controls>
     <source src="cancion.mp3" type='audio/mpeg; codecs="mp3"'>
     <source src="cancion.ogg" type='audio/ogg; codecs="vorbis"' >
</audio>
```

