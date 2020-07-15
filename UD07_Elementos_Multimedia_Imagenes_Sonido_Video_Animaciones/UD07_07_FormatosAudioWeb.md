# 7. **Formatos de archivos de audio y optimizaciones**

Tabla de contenidos

- [7. **Formatos de archivos de audio y optimizaciones**](#7-formatos-de-archivos-de-audio-y-optimizaciones)
  - [7.1. Formatos de archivos de audio](#71-formatos-de-archivos-de-audio)
    - [7.1.1. Formato WAV](#711-formato-wav)
    - [7.1.2. Formato MP3](#712-formato-mp3)
    - [7.1.3. Formato OGG](#713-formato-ogg)
    - [7.1.4. Formato MIDI](#714-formato-midi)
  - [7.2. Optimizaciones en archivos de audio para web](#72-optimizaciones-en-archivos-de-audio-para-web)
  - [7.3. Conversiones entre formatos](#73-conversiones-entre-formatos)
    - [7.3.1. Audacity](#731-audacity)
  - [7.4. Sitios web para la descarga de sonidos](#74-sitios-web-para-la-descarga-de-sonidos)

La incorporación de **audio digital** en una página web es una necesidad que surge en múltiples contextos: **grabación de locuciones, lecturas, entrevistas, debates, noticias, composiciones musicales, interpretaciones instrumentales, etc**.

Los audios digitales están disponibles en **distintos formatos** y disponen de una extensión de archivo específica. Existen muchos tipos de formatos de audio: mp3, wav, ogg, mp4, au... De todos estos formatos los que más se utilizan en la **web** son los formatos **mp3 y ogg**.

## 7.1. Formatos de archivos de audio

En esta sección vamos a tratar las características de algunos de los formatos y su optimización para la web.

### 7.1.1. Formato WAV

El formato **WAV** (WaveForm Audio File) es un archivo que desarrolló originalmente Microsoft para guardar audio. Los archivos tienen extensión `*.wav`.

-   Es ideal para guardar audios originales a partir de los cuales se puede comprimir y guardar en distintos tamaños de muestreo para publicar en la web.
-   Es un formato de excelente calidad de audio. Sin embargo produce archivos de un peso enorme.
-   Compresión: Los archivos WAV se pueden guardar con distintos tipos de compresión. Las más utilizadas son la compresión PCM y la compresión ADPCM. No obstante incluso definiendo un sistema de compresión, con un audio de cierta duración se genera un archivo excesivamente pesado.

### 7.1.2. Formato MP3

El formato **MP3** (MPEG 1 Layer 3) fue creado por el Instituto Fraunhofer y por su extraordinario grado de compresión y alta calidad ha monopolizando el mundo del audio digital. Los archivos tienen extensión `*.mp3`.

-   Es ideal para publicar audios en la web. Se puede escuchar desde la mayoría de reproductores.
-   La transformación de WAV a MP3 o la publicación directa de una grabación en formato MP3 es un proceso fácil y al alcance de los principales editores de audio.
-   Tiene un enorme nivel de compresión respecto al WAV. En igualdad del resto de condiciones reduciría el tamaño del archivo de un fragmento musical con un factor entre 1/10 y 1/12.
-   Presentan una mínima pérdida de calidad.

### 7.1.3. Formato OGG

El formato **OGG**, desarrollado por la fundación Xiph.org, ***es libre y de código abierto***, a diferencia del formato MP3. Los archivos tienen extensión `*.ogg`.

-   Muestra un grado de compresión similar al MP3 pero según los expertos en música la calidad de reproducción es ligeramente superior.
-   No todos los reproductores multimedia son capaces de leer por defecto este formato. En algunos casos es necesario instalar los códecs o filtros oportunos.
-   El formato OGG puede contener audio y vídeo.

### 7.1.4. Formato MIDI

El formato **MIDI** (Musical Instrument Digital Interface o Interface Digital para Instrumentos Digitales) en realidad no resulta de un proceso de digitalización de un sonido analógico y, por ello, no es un formato de audio propiamente dicho. Sus características son las siguientes.

-   Un archivo de extensión *.mid almacena secuencias de dispositivos MIDI (sintetizadores) donde se recoge qué instrumento interviene, en qué forma lo hace y cuándo.
-   Los archivos MIDI se pueden editar y manipular mediante programas especiales y distintos de los empleados para editar formatos WAV, MP3, etc. El manejo de estos programas suele conllevar ciertos conocimientos musicales.
-   Los archivos MIDI permiten audios de cierta duración con un reducido peso. Esto es debido a que no guardan el sonido sino la información o partitura necesaria para que el ordenador la componga y reproduzca a través de la tarjeta de sonido.
-   Se suelen utilizar en sonidos de fondo de páginas HTML o para escuchar composiciones musicales de carácter instrumental.

## 7.2. Optimizaciones en archivos de audio para web

Para optimizar el peso del archivo de audio que vamos a subir a nuestra web será necesario utilizar un editor para reducir alguno o algunos de los siguientes parámetros:

1.  **Tasa de muestreo**. Definir valores inferiores: 44100 Hz., 22050 Hz., 11025 Hz, etc.
2.  **Resolución**. Establecer resoluciones más pequeñas: 32-bits, 16-bits, 8-bits, 4-bits, etc.
3.  **Duración**. En ocasiones se puede utilizar un fragmento más corto que reproducido en bucle cubre el tiempo suficiente de acompañamiento musical. A éstos se les llama loops.
4.  **Calidad estéreo/mono**. La reducción a calidad "mono" reduce considerablemente el peso del archivo. Por otra lado la calidad de reproducción "mono" para la mayoría de audios y de público es apenas perceptible.
5.  **Formato**. Es preferible utilizar el formato MP3 u OGG en lugar del WAV por su potente factor de compresión y su aceptable calidad de audio.

## 7.3. Conversiones entre formatos

En el caso de necesitar insertar un audio en una web, es posible que sea necesario utilizar un **programa de edición** para cambiar su formato o recortar un trozo, entre otras adaptaciones.

Tal y como vimos en el apartado de [edición de vídeo](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD07_Elementos_Multimedia_Imagenes_Sonido_Video_Animaciones/UD07_05_FormatosVideoWeb.md), podemos utilizar herramientas útiles y gratuitas como el **reproductor VLC** para hacer algunos cambios básicos sobre un vídeo o un audio. Además, para realizar ediciones de audio más complejas disponemos de **Audacity**, un software libre y fácil de utilizar.

### 7.3.1. Audacity

**Audacity** es un programa **libre y de código abierto** para grabar y editar sonidos. Se puede descargar para **Windows, Linux o Mac** en la página oficial: [audacityteam.org](https://www.audacityteam.org/)

**Para cambiar el formato de un audio en Audacity:**

1.  Abrimos Audacity.
2.  Abrimos el archivo que queremos convertir.
3.  "Archivo" y "Exportar".
4.  Elegimos tipo de archivo (ejemplo: MP3) y aceptar.

[Más información sobre formatos de audio en ite.educacion.es](http://www.ite.educacion.es/)

## 7.4. Sitios web para la descarga de sonidos

A continuación se propone un listado de bancos para la descarga de audios gratuitos para utilizarlos en proyectos propios.

-   [elongsound.com](https://www.elongsound.com/)
-   [sshhtt.com](https://www.sshhtt.com/)
-   [recursostic.educacion.es/bancoimagenes/web/](http://recursostic.educacion.es/bancoimagenes/web/)
-   soundeffectsplus.com
-   es.audiomicro.com
-   soundsnap.com
-   findsounds.com