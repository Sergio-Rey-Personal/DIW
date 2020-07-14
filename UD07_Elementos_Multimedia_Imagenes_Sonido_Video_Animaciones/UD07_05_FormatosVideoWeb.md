# **Formatos de archivos de vídeo y conversiones**

- [5. Formatos de archivos de vídeo y conversiones](#5-formatos-de-archivos-de-vídeo-y-conversiones)
  - [5.1. Formatos de archivos de vídeo](#51-formatos-de-archivos-de-vídeo)
  - [5.2. Optimización de archivos de vídeo](#52-optimización-de-archivos-de-vídeo)
  - [5.3. Conversión y edición de vídeos](#53-conversión-y-edición-de-vídeos)
      - [VLC media player](#vlc-media-player)
  - [5.4. Sitios web para la descarga de vídeos](#54-sitios-web-para-la-descarga-de-vídeos)

# 5. Formatos de archivos de vídeo y conversiones
Gracias al avance en la velocidad de la conexión de datos, hoy en día es de lo más común descargar y ver vídeos dentro de cualquier página web. En la unidad 3 vimos cómo insertar un [vídeo incrustado en HTML](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_06_EtiquetasHTMLParaContenidoIncrustado.md) mediante la etiqueta `<iframe>`, en esta unidad vamos a ver cómo insertar un vídeo mediante la etiqueta `<video>` de HTML5 y cómo podemos mostrar y modificar sus controles.

Antes de conocer cómo podemos insertar un vídeo en HTML5 vamos a ver los distintos tipos de formatos de vídeo y sus conversiones.

## 5.1. Formatos de archivos de vídeo

Los vídeos digitales se pueden guardar en formatos diferentes con extensiones específicas. Los formatos de vídeo habituales para trabajar en la web son MP4, OGG y WebM.

-   **MP4** (ficheros con extensión .mp4 o .mov) ofrece un buen ratio de compresión/calidad. Es impulsado por Apple y Microsoft.
-   **OGG** (ficheros con extensión .ogv) está basado en un estándar libre y abierto. También es un formato de audio. Impulsado por Mozilla, Opera y Firefox.
-   **WebM** (ficheros con extensión .webm) es un formato creado especialmente para la web, también es gratuito e impulsado por los mismos que apoyan el formato OGG (Mozilla, Opera y Firefox).

## 5.2. Optimización de archivos de vídeo

Para optimizar el peso del archivo de vídeo será necesario editarlo para establecer algunos de los siguientes parámetros:

En el Audio:

1.  El **códec de compresión** de audio utilizado: MPEG Layer 1, MPEG Layer 2, MP3, etc.
2.  **Resolución**. Establecer resoluciones más pequeñas: 32-bits, 16-bits, 8-bits, 4-bits, etc.
3.  **Tasa de muestreo**. Definir valores inferiores: 44100 Hz., 22050 Hz., 11025 Hz, etc.
4.  **Velocidad de transmisión** (bitrate). Configurar bitrates más bajos: 128 Kbps, 96 Kbps, 64 Kbps, etc.
5.  **Calidad estéreo/mono**. Reducir la calidad de "stereo" a "mono".

En el Vídeo:

1.  El **códec de compresión** de vídeo utilizado.
2.  **Método de BitRate**. Utilizar un bitrate variable VBR puede optimizar la calidad del vídeo y repercutir en el peso final del archivo frente a un bitrate constante CBR.
3.  **Velocidad de transmisión** (bitrate). Configurar bitrates más bajos: 1000 Kbps, 768 kbps, 360 Kbps, etc.
4.  **Dimensiones**. Cuanto más pequeña sea la altura y anchura en píxeles de los fotogramas de un vídeo, menos tamaño ocupará su archivo.
5.  **Velocidad de fotogramas**. Se puede reducir el número de fotogramas por segundo que mostrará el vídeo: 30, 24, 20, 16, etc.
6.  **Fotogramas Clave**. Durante la compresión también se puede indicar cada cuánto se guardará un fotograma completo (fotograma clave): 24, 48, 96, 128, etc. Cuanto mayor sea esta cadencia más bajo será el peso del archivo resultante.

## 5.3. Conversión y edición de vídeos

Para reducir la calidad de cualquier vídeo o para convertir su formato no necesitamos hacer uso de programas profesionales como Final Cut Pro o Adobe Premier Pro. Podemos hacer uso de aplicaciones en la nube o de reproductores multimedia que nos ofrecen múltiples funcionalidades.

#### VLC media player

**VLC** es un reproductor multimedia libre y de código abierto multiplataforma y un «framework» que reproduce la mayoría de archivos multimedia. Puedes descargar el reproductor desde la página web [videolan.org](https://www.videolan.org/).

Algunas de las funcionalidades que nos ofrece este reproductor son las siguientes:

-   Conversión de formatos (vídeo y audio): Menú / Medio / Convertir o en Archivo / Convertir.
-   Controles avanzados: Menú / Ver / Controles avanzados.
-   Reproducción y guardado de vídeos online como Youtube.
-   Ventana / efectos de vídeo.

> [Cómo usar VLC para convertir archivos de audio y vídeo](https://www.genbeta.com/paso-a-paso/como-usar-vlc-para-convertir-archivos-de-audio-y-video)

## 5.4. Sitios web para la descarga de vídeos

A continuación se propone un listado de sitios web para la descarga de vídeos gratuitos libres de derechos de autor o con licencias Creative Commons para utilizarlos en proyectos propios.

-   [Coverr.co](https://coverr.co/)
-   [Pixabay.com](https://pixabay.com/es/)
-   videvo.net
-   es.videezy.com
-   lifeofvids.com
-   dareful.com
-   pexels.com
-   [Más sitios web para la descarga de vídeos](http://www.ite.educacion.es/formacion/materiales/107/cd/video/video0303.html)