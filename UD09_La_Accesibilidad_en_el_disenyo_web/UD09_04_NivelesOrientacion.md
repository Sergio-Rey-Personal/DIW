# 4. **Niveles de orientación**

Tabla de contenidos

- [4. **Niveles de orientación**](#4-niveles-de-orientación)
  - [4.1. Principios generales](#41-principios-generales)
    - [4.1.1. Principio 1: Perceptible](#411-principio-1-perceptible)
      - [4.1.1.1. Pauta 1.1 Alternativas textuales](#4111-pauta-11-alternativas-textuales)
      - [4.1.1.2. Pauta 1.2 Medios tempodependientes](#4112-pauta-12-medios-tempodependientes)
      - [4.1.1.3. Pauta 1.3 Adaptable](#4113-pauta-13-adaptable)
      - [4.1.1.4. Pauta 1.4 Distinguible](#4114-pauta-14-distinguible)
  - [> Comprender 1.4.13](#blockquotecomprender-1413blockquote)
    - [4.1.2. Principio 2: Operable](#412-principio-2-operable)
      - [4.1.2.1. Pauta 2.1 Accesible por teclado](#4121-pauta-21-accesible-por-teclado)
      - [4.1.2.2. Pauta 2.2 Tiempo suficiente](#4122-pauta-22-tiempo-suficiente)
      - [4.1.2.3. Pauta 2.3 Convulsiones](#4123-pauta-23-convulsiones)
      - [4.1.2.4. Pauta 2.4 Navegable](#4124-pauta-24-navegable)
      - [4.1.2.5. Pauta 2.5 Modalidades de entrada](#4125-pauta-25-modalidades-de-entrada)
  - [> Comprender 2.5.6](#blockquotecomprender-256blockquote)
    - [4.1.3. Principio 3: Comprensible](#413-principio-3-comprensible)
      - [4.1.3.1. Pauta 3.1 Legible](#4131-pauta-31-legible)
      - [4.1.3.2. Pauta 3.2 Predecible](#4132-pauta-32-predecible)
      - [4.1.3.3. Pauta 3.3 Entrada de datos asistida](#4133-pauta-33-entrada-de-datos-asistida)
    - [4.1.4. Principio 4: Robusto](#414-principio-4-robusto)
      - [4.1.4.1. Pauta 4.1 Compatible](#4141-pauta-41-compatible)
  - [4.2. Conformidad](#42-conformidad)
    - [4.2.1. Requisitos de conformidad](#421-requisitos-de-conformidad)
    - [4.2.2. Declaraciones de conformidad (opcional)](#422-declaraciones-de-conformidad-opcional)
      - [4.2.2.1. Componentes exigidos en la declaración de conformidad](#4221-componentes-exigidos-en-la-declaración-de-conformidad)
      - [4.2.2.2. Componentes opcionales de la declaración de conformidad](#4222-componentes-opcionales-de-la-declaración-de-conformidad)
    - [4.2.3. Enunciado de conformidad parcial - Contenido de terceras partes](#423-enunciado-de-conformidad-parcial---contenido-de-terceras-partes)
    - [4.2.4. Enunciado de conformidad parcial - Lenguaje](#424-enunciado-de-conformidad-parcial---lenguaje)

Los **niveles de orientación nos orientan sobre cómo crear un contenido más accesible y están destinados a una audiencia muy variada**: diseñadores de sitios web, organizaciones que quieren verificar la accesibilidad de las webs existentes, profesionales interesados en que las webs sean accesibles por personas con discapacidades, etc.

Dentro de los niveles de orientación encontramos: principios generales, pautas generales, criterios de conformidad verificables y una amplia colección de técnicas suficientes, técnicas recomendables y fallos comunes documentados con ejemplos, enlaces a recursos adicionales y código.

- **Principios generales**: En el nivel más alto se sitúan los cuatro principios que proporcionan los fundamentos de la accesibilidad web: *perceptible, operable, comprensible y robusto*. 
- **Pautas generales**: Por debajo de los principios están las pautas. Las doce pautas proporcionan los objetivos básicos que los autores deben lograr con el fin de crear un contenido más accesible para los usuarios con distintas discapacidades. 
- **Criterios de Conformidad**: Para cada pauta se proporcionan los criterios de conformidad verificables. Se definen tres niveles de conformidad: A (el más bajo), AA y AAA (el más alto).
- **Técnicas suficientes y recomendables:** Para cada una de las *pautas* y *criterios de conformidad* se proporcionan técnicas que nos permiten hacer una evaluación correcta.

Todos estos niveles de orientación (principios, pautas, criterios de conformidad y técnicas suficientes y recomendables) actúan en conjunto para proporcionar una **orientación sobre cómo crear un contenido más accesible**. 

## 4.1. Principios generales

Como se ha dicho anteriormente, los **principios generales que debe cumplir una web para que su contenido sea accesible** son: **Perceptible, Operable, Comprensible, Robusto**.

---

### 4.1.1. Principio 1: Perceptible 

> **La información y los componentes de la interfaz de usuario deben ser presentados a los usuarios de modo que ellos puedan percibirlos.**

#### 4.1.1.1. Pauta 1.1 Alternativas textuales

 Proporcionar alternativas textuales para todo contenido no textual de modo que se pueda convertir a otros formatos que las personas necesiten, tales como textos ampliados, braille, voz, símbolos o en un lenguaje más simple.

> [Comprender la Pauta 1.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/text-equiv.html)

- **1.1.1 Contenido no textual:** Todo [contenido no textual](http://sidar.org/traducciones/wcag20/es/#non-text-contentdef "definición: contenido no textual") que se presenta al usuario tiene una [alternativa textual](http://sidar.org/traducciones/wcag20/es/#text-altdef "definición: alternativa textual") que cumple el mismo propósito, excepto en las situaciones enumeradas a continuación. (Nivel A)

  - **Controles, Entrada de datos:** Si el contenido no textual es un control o acepta datos introducidos por el usuario, entonces tiene un [nombre](http://sidar.org/traducciones/wcag20/es/#namedef "definición: nombre") que describe su propósito. (Véase la [Pauta 4.1](http://sidar.org/traducciones/wcag20/es/#ensure-compat) para requisitos adicionales sobre los controles y el contenido que aceptan entrada de datos).

  - **Contenido multimedia tempodependiente:** Si el contenido no textual es una presentación multimedia con desarrollo temporal, entonces las alternativas textuales proporcionan al menos una identificación descriptiva del contenido no textual. (Véase la [Pauta 1.2](http://sidar.org/traducciones/wcag20/es/#media-equiv) para requisitos adicionales sobre contenido multimedia).

  - **Pruebas:** Si el contenido no textual es una prueba o un ejercicio que no sería válido si se presentara en forma de [texto](http://sidar.org/traducciones/wcag20/es/#textdef "definición: texto"), entonces las alternativas textuales proporcionan al menos una identificación descriptiva del contenido no textual.

  - **Sensorial:** Si el contenido no textual tiene como objetivo principal el crear una [experiencia sensorial específica](http://sidar.org/traducciones/wcag20/es/#sensoryexpdef "definición: experiencia sensorial específica"), entonces las alternativas textuales proporcionan al menos una identificación descriptiva del contenido no textual.

  - **[CAPTCHA](http://sidar.org/traducciones/wcag20/es/#CAPTCHAdef "definición: CAPTCHA"):** Si el propósito del contenido no textual es confirmar que quien está accediendo al contenido es una persona y no una computadora, entonces se proporcionan alternativas textuales que identifican y describen el propósito del contenido no textual y se proporcionan formas alternativas de CAPTCHA con modos de salida para distintos tipos de percepciones sensoriales, con el fin de acomodarse a las diferentes discapacidades.

  - **Decoración, Formato, Invisible:** Si el contenido no textual es [simple decoración](http://sidar.org/traducciones/wcag20/es/#puredecdef "definición: simple decoración"), se utiliza únicamente para definir el formato visual o no se presenta a los usuarios, entonces se implementa de forma que pueda ser ignorado por las [ayudas técnicas](http://sidar.org/traducciones/wcag20/es/#atdef "definición: ayudas técnicas").

  > [Cómo cumplir 1.1.1](http://www.w3.org/WAI/WCAG21/quickref/#qr-text-equiv-all "Cómo satisfacer el Criterio de Conformidad 1.1.1") 

  > [Comprender 1.1.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/text-equiv-all.html "Comprender el Criterio de Conformidad 1.1.1")

#### 4.1.1.2. Pauta 1.2 Medios tempodependientes

  Proporcionar alternativas para los medios tempodependientes.

> [Comprender la Pauta 1.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv.html)

- **1.2.1 Sólo audio y sólo vídeo (grabado):** Para contenido [sólo audio](http://sidar.org/traducciones/wcag20/es/#audio-onlydef "definición: sólo audio") [grabado](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado") y contenido [sólo vídeo](http://sidar.org/traducciones/wcag20/es/#video-onlydef "definición: sólo vídeo") [grabado](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado"), se cumple lo siguiente, excepto cuando el audio o el vídeo es un [contenido multimedia alternativo al texto](http://sidar.org/traducciones/wcag20/es/#multimedia-alt-textdef "definición: contenido multimedia alternativo al texto") y está claramente identificado como tal: (Nivel A)

  - **Sólo audio grabado:** Se proporciona una [alternativa para los medios tempodependientes](http://sidar.org/traducciones/wcag20/es/#alt-time-based-mediadef "alternativa para los medios tempodependientes") que presenta información equivalente para el contenido sólo audio grabado.

  - **Sólo vídeo grabado:** Se proporciona una alternativa para los medios tempodependientes o se proporciona una pista sonora que presenta información equivalente al contenido del medio de sólo vídeo grabado.

  > [Cómo cumplir 1.2.1](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-av-only-alt "Cómo satisfacer el Criterio de Conformidad 1.2.1")

  > [Comprender 1.2.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-av-only-alt.html "Comprender el Criterio de Conformidad 1.2.1")

- **1.2.2 Subtítulos (grabados):** Se proporcionan [subtítulos](http://sidar.org/traducciones/wcag20/es/#captionsdef "definición: subtítulos") para el contenido de [audio](http://sidar.org/traducciones/wcag20/es/#audiodef "definición: audio") [grabado](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado") dentro de contenido [multimedia sincronizado](http://sidar.org/traducciones/wcag20/es/#synchronizedmediadef "definición: multimedia sincronizado"), excepto cuando la presentación es un [contenido multimedia alternativo al texto](http://sidar.org/traducciones/wcag20/es/#multimedia-alt-textdef "definición: contenido multimedia alternativo al texto") y está claramente identificado como tal. (Nivel A)

  > [Cómo cumplir 1.2.2](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-captions "Cómo satisfacer el Criterio de Conformidad 1.2.2")

  > [Comprender 1.2.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-captions.html "Comprender el Criterio de Conformidad 1.2.2")

- **1.2.3 Audiodescripción o Medio Alternativo (grabado):** Se proporciona una [alternativa para los medios tempodependientes](http://sidar.org/traducciones/wcag20/es/#alt-time-based-mediadef "definición: alternativa para los medios tempodependientes") o una [audiodescripción](http://sidar.org/traducciones/wcag20/es/#audiodescdef "definición: audiodescripción") para el contenido de [vídeo](http://sidar.org/traducciones/wcag20/es/#videodef "definición: vídeo") [grabado](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado") en los [multimedia sincronizados](http://sidar.org/traducciones/wcag20/es/#synchronizedmediadef "definición: multimedia sincronizados"), excepto cuando ese contenido es un [contenido multimedia alternativo al texto](http://sidar.org/traducciones/wcag20/es/#multimedia-alt-textdef "definición: contenido multimedia alternativo al texto") y está claramente identificado como tal. (Nivel A)

  > [Cómo cumplir 1.2.3](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-audio-desc "Cómo satisfacer el Criterio de Conformidad 1.2.3")

  > [Comprender 1.2.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-audio-desc.html "Comprender el Criterio de Conformidad 1.2.3")

- **1.2.4 Subtítulos (en directo):** Se proporcionan [subtítulos](http://sidar.org/traducciones/wcag20/es/#captionsdef "definición: subtítulos") para todo el contenido de [audio](http://sidar.org/traducciones/wcag20/es/#audiodef "definición: audio") [en directo](http://sidar.org/traducciones/wcag20/es/#livedef "definición: en directo") de los [multimedia sincronizados](http://sidar.org/traducciones/wcag20/es/#synchronizedmediadef "definición: multimedia sincronizados"). (Nivel AA)

  > [Cómo cumplir 1.2.4](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-real-time-captions "Cómo satisfacer el Criterio de Conformidad 1.2.4")

  > [Comprender 1.2.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-real-time-captions.html "Comprender el Criterio de Conformidad 1.2.4")

- **1.2.5 Audiodescripción (grabado):** Se proporciona una [audiodescripción](http://sidar.org/traducciones/wcag20/es/#audiodescdef "definición: audiodescripción") para todo el contenido de [vídeo](http://sidar.org/traducciones/wcag20/es/#videodef "definición: vídeo") [grabado](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado") dentro de contenido [multimedia sincronizado](http://sidar.org/traducciones/wcag20/es/#synchronizedmediadef "definición: multimedia sincronizado"). (Nivel AA)

  > [Cómo cumplir 1.2.5](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-audio-desc-only "Cómo satisfacer el Criterio de Conformidad 1.2.5")

  > [Comprender 1.2.5](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-audio-desc-only.html "Comprender el Criterio de Conformidad 1.2.5")

- **1.2.6 Lengua de señas (grabado):** Se proporciona una [interpretación en lengua de señas](http://sidar.org/traducciones/wcag20/es/#sign-languageinterpdef "definición: interpretación en lengua de señas") para todo el contenido de [audio](http://sidar.org/traducciones/wcag20/es/#audiodef "definición: audio") [grabado](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado") dentro de contenido [multimedia sincronizado](http://sidar.org/traducciones/wcag20/es/#synchronizedmediadef "definición: multimedia sincronizado"). (Nivel AAA)

  > [Cómo cumplir 1.2.6](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-sign "Cómo satisfacer el Criterio de Conformidad 1.2.6")

  > [Comprender 1.2.6](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-sign.html "Comprender el Criterio de Conformidad 1.2.6")

- **1.2.7 Audiodescripción ampliada (grabada):** Cuando las pausas en el audio de primer plano son insuficientes para permitir que la [audiodescripción](http://sidar.org/traducciones/wcag20/es/#audiodescdef "definición: audiodescripción") comunique el significado del vídeo, se proporciona una [audiodescripción ampliada](http://sidar.org/traducciones/wcag20/es/#extended-addef "definición: audiodescripción ampliada") para todos los contenidos de [vídeo](http://sidar.org/traducciones/wcag20/es/#videodef "definición: vídeo") [grabado](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado") dentro de contenido [multimedia sincronizado](http://sidar.org/traducciones/wcag20/es/#synchronizedmediadef "definición: multimedia sincronizado"). (Nivel AAA)

  > [Cómo cumplir 1.2.7](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-extended-ad "Cómo satisfacer el Criterio de Conformidad 1.2.7")

  > [Comprender 1.2.7](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-extended-ad.html "Comprender el Criterio de Conformidad 1.2.7")

- **1.2.8 Medio alternativo (grabado):** Se proporciona una [alternativa para los medios tempodependientes](http://sidar.org/traducciones/wcag20/es/#alt-time-based-mediadef "definición: alternativa para los medios tempodependientes"), tanto para todos los contenidos [multimedia sincronizados](http://sidar.org/traducciones/wcag20/es/#synchronizedmediadef "definición: multimedia sincronizados") [grabados](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado") como para todos los medios de [sólo vídeo](http://sidar.org/traducciones/wcag20/es/#video-onlydef "definición: sólo vídeo") grabado. (Nivel AAA)

  > [Cómo cumplir 1.2.8](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-text-doc "Cómo satisfacer el Criterio de Conformidad 1.2.8")

  > [Comprender 1.2.8](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-text-doc.html "Comprender el Criterio de Conformidad 1.2.8")

- **1.2.9 Sólo audio (en directo):** Se proporciona una [alternativa para los medios tempodependientes](http://sidar.org/traducciones/wcag20/es/#alt-time-based-mediadef "definición: alternativa para los medios tempodependientes") que presenta información equivalente para el contenido de [sólo audio](http://sidar.org/traducciones/wcag20/es/#audio-onlydef "definición: sólo audio") [en directo](http://sidar.org/traducciones/wcag20/es/#livedef "definición: en directo"). (Nivel AAA)

  > [Cómo cumplir 1.2.9](http://www.w3.org/WAI/WCAG21/quickref/#qr-media-equiv-live-audio-only "Cómo satisfacer el Criterio de Conformidad 1.2.9")

  > [Comprender 1.2.9](http://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-live-audio-only.html "Comprender el Criterio de Conformidad 1.2.9")

#### 4.1.1.3. Pauta 1.3 Adaptable

  Crear contenido que pueda presentarse de diferentes formas (por ejemplo, con una disposición más simple) sin perder información o estructura.

> [Comprender la Pauta 1.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation.html)

- **1.3.1 Información y relaciones:** La información, [estructura](http://sidar.org/traducciones/wcag20/es/#structuredef "definición: estructura") y [relaciones](http://sidar.org/traducciones/wcag20/es/#relationshipsdef "dfinición: relaciones") comunicadas a través de la [presentación](http://sidar.org/traducciones/wcag20/es/#presentationdef "definición: presentación") pueden ser [determinadas por software](http://sidar.org/traducciones/wcag20/es/#programmaticallydetermineddef "definición: determinado por software") o están disponibles como texto. (Nivel A)

  > [Cómo cumplir 1.3.1](http://www.w3.org/WAI/WCAG21/quickref/#qr-content-structure-separation-programmatic "Cómo satisfacer el Criterio de Conformidad 1.3.1")

  > [Comprender 1.3.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-programmatic.html "Comprender el Criterio de Conformidad 1.3.1")

- **1.3.2 Secuencia significativa:** Cuando la secuencia en que se presenta el contenido afecta a su significado, se puede [determinar por software](http://sidar.org/traducciones/wcag20/es/#programmaticallydetermineddef "definición: determinado por software") la [secuencia correcta de lectura](http://sidar.org/traducciones/wcag20/es/#correct-reading-sequencedef "definición: secuencia correcta de lectura"). (Nivel A)

  > [Cómo cumplir 1.3.2](http://www.w3.org/WAI/WCAG21/quickref/#qr-content-structure-separation-sequence "Cómo satisfacer el Criterio de Conformidad 1.3.2")

  > [Comprender 1.3.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-sequence.html "Comprender el Criterio de Conformidad 1.3.2")

- **1.3.3 Características sensoriales:** Las instrucciones proporcionadas para entender y operar el contenido no dependen exclusivamente en las características sensoriales de los componentes como su forma, tamaño, ubicación visual, orientación o sonido. (Nivel A)

> *Nota:* Para los requisitos relacionados con el color, véase la [Pauta 1.4](http://sidar.org/traducciones/wcag20/es/#visual-audio-contrast).

  > [Cómo cumplir 1.3.3](http://www.w3.org/WAI/WCAG21/quickref/#qr-content-structure-separation-understanding "Cómo satisfacer el Criterio de Conformidad 1.3.3")

  > [Comprender 1.3.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-understanding.html "Comprender el Criterio de Conformidad 1.3.3")
  
- **1.3.4 Orientacion (nuevo en 2.1):** El contenido no restringe su visualización y funcionamiento a una única orientación de pantalla, como vertical u horizontal, a menos que sea esencial una orientación de pantalla específica. (Nivel AA)

  > [Cómo cumplir 1.3.4](https://www.w3.org/WAI/WCAG21/quickref/#orientation "Cómo satisfacer el Criterio de Conformidad 1.3.4")

  > [Comprender 1.3.4](https://www.w3.org/WAI/WCAG21/Understanding/orientation.html "Comprender el Criterio de Conformidad 1.3.4")
  
- **1.3.5 Identificar el propósito de la entrada (nuevo en 2.1):** El propósito de cada campo de entrada que recopila información sobre el usuario se puede determinar mediante programación cuando:

    - El campo de entrada tiene un propósito identificado en la sección Propósitos de entrada para componentes de interfaz de usuario; y

    -  El contenido se implementa utilizando tecnologías con soporte para identificar el significado esperado para los datos de entrada del formulario. (Nivel AA)

  > [Cómo cumplir 1.3.5](https://www.w3.org/WAI/WCAG21/quickref/#identify-input-purpose "Cómo satisfacer el Criterio de Conformidad 1.3.5")

  > [Comprender 1.3.5](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html "Comprender el Criterio de Conformidad 1.3.5")

  
- **1.3.6 Identificar propósitos (nuevo en 2.1):** En el contenido implementado mediante lenguajes de marcado, el propósito de los componentes de la interfaz de usuario, los iconos y las regiones se puede determinar mediante programación. (Nivel AA)

  > [Cómo cumplir 1.3.6](https://www.w3.org/WAI/WCAG21/quickref/#identify-purpose "Cómo satisfacer el Criterio de Conformidad 1.3.6")

  > [Comprender 1.3.6](https://www.w3.org/WAI/WCAG21/Understanding/identify-purpose.html "Comprender el Criterio de Conformidad 1.3.6")

#### 4.1.1.4. Pauta 1.4 Distinguible

  Facilitar a los usuarios ver y oír el contenido, incluyendo la separación entre el primer plano y el fondo.

  > [Comprender la Pauta 1.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast.html)

- **1.4.1 Uso del color:** El color no se usa como único medio visual para transmitir la información, indicar una acción, solicitar una respuesta o distinguir un elemento visual. (Nivel A)

> *Nota:* Este criterio de conformidad trata específicamente acerca de la percepción del color. En la [Pauta 1.3](http://sidar.org/traducciones/wcag20/es/#content-structure-separation) se recogen otras formas de percepción, incluyendo el acceso por software al color y a otros códigos de presentación visual.

  > [Cómo cumplir 1.4.1](http://www.w3.org/WAI/WCAG21/quickref/#qr-visual-audio-contrast-without-color "Cómo satisfacer el Criterio de Conformidad 1.4.1")

  > [Comprender 1.4.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-without-color.html "Comprender el Criterio de Conformidad 1.4.1")

- **1.4.2 Control del audio:** Si el audio de una página web suena automáticamente durante más de 3 segundos, se proporciona ya sea un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "dfinición: mecanismo") para pausar o detener el audio, o un mecanismo para controlar el volumen del sonido que es independiente del nivel de volumen global del sistema. (Nivel A)

> *Nota:* En la medida en que cualquier contenido que no satisfaga este criterio puede interferir con la capacidad del usuario de emplear la página en su conjunto, todo contenido de la página web (tanto si satisface o no otros criterios de conformidad) debe satisfacer este criterio. Véase [Requisito de Conformidad 5: Sin interferencia](http://sidar.org/traducciones/wcag20/es/#cc5).

  > [Cómo cumplir 1.4.2](http://www.w3.org/WAI/WCAG21/quickref/#qr-visual-audio-contrast-dis-audio "Cómo satisfacer el Criterio de Conformidad 1.4.2")

  > [Comprender 1.4.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-dis-audio.html "Comprender el Criterio de Conformidad 1.4.2")

- **1.4.3 Contraste (mínimo):** La presentación visual de [texto](http://sidar.org/traducciones/wcag20/es/#textdef "definición: texto") e [imágenes de texto](http://sidar.org/traducciones/wcag20/es/#images-of-textdef "definición: imágenes de texto") tiene una [relación de contraste](http://sidar.org/traducciones/wcag20/es/#contrast-ratiodef "definición: relación de contraste") de, al menos, 4.5:1, excepto en los siguientes casos: (Nivel AA)

  - **Textos grandes:** Los textos de [gran tamaño](http://sidar.org/traducciones/wcag20/es/#larger-scaledef "definición: gran tamaño (texto)") y las imágenes de texto de gran tamaño tienen una relación de contraste de, al menos, 3:1.

  - **Incidental:** Los textos o imágenes de texto que forman parte de un [componente inactivo de la interfaz de usuario](http://sidar.org/traducciones/wcag20/es/#user-interface-componentdef "definición: componente de la interfaz de usuario"), que son [simple decoración](http://sidar.org/traducciones/wcag20/es/#puredecdef "definición: simple decoración"), que no resultan visibles para nadie o forman parte de una imagen que contiene otros elementos visuales significativos, no tienen requisitos de contraste.

  - **Logotipos:** El texto que forma parte de un logo o nombre de marca no tiene requisitos de contraste mínimo.

  > [Cómo cumplir 1.4.3](http://www.w3.org/WAI/WCAG21/quickref/#qr-visual-audio-contrast-contrast "Cómo satisfacer el Criterio de Conformidad 1.4.3")

  > [Comprender 1.4.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-contrast.html "Comprender el Criterio de Conformidad 1.4.3")

- **1.4.4 Cambio de tamaño del texto:** A excepción de los [subtítulos](http://sidar.org/traducciones/wcag20/es/#captionsdef "definición: subtítulos") y las [imágenes de texto](http://sidar.org/traducciones/wcag20/es/#images-of-textdef "definición: imágenes de texto"), todo el [texto](http://sidar.org/traducciones/wcag20/es/#textdef "definición: texto") puede ser ajustado sin [ayudas técnicas](http://sidar.org/traducciones/wcag20/es/#atdef "definición: ayudas técnicas") hasta un 200 por ciento sin que se pierdan el contenido o la funcionalidad. (Nivel AA)

  > [Cómo cumplir 1.4.4](http://www.w3.org/WAI/WCAG21/quickref/#qr-visual-audio-contrast-scale "Cómo satisfacer el Criterio de Conformidad 1.4.4")

  > [Comprender 1.4.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-scale.html "Comprender el Criterio de Conformidad 1.4.4")

- **1.4.5 Imágenes de texto:** Si con las tecnologías que se están utilizando se puede conseguir la presentación visual deseada, se utiliza [texto](http://sidar.org/traducciones/wcag20/es/#textdef "definición: texto") para transmitir la información en vez de [imágenes de texto](http://sidar.org/traducciones/wcag20/es/#images-of-textdef "definición: imágenes de texto"), excepto en los siguientes casos. (Nivel AA)

  - **Configurable:** La imagen de texto es [visualmente configurable](http://sidar.org/traducciones/wcag20/es/#visually-customizeddef "definición: visualmente configurable") según los requisitos del usuario.

  - **Esencial:** Una forma particular de presentación del texto resulta [esencial](http://sidar.org/traducciones/wcag20/es/#essentialdef "definición: esencial") para la información que se transmite.

  > *Nota:* Los logotipos (textos que son parte de un logo o de un nombre de marca) se consideran esenciales.
 
  > [Cómo cumplir 1.4.5](http://www.w3.org/WAI/WCAG21/quickref/#qr-visual-audio-contrast-text-presentation "Cómo satisfacer el Criterio de Conformidad 1.4.5")

  > [Comprender 1.4.5](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-text-presentation.html "Comprender el Criterio de Conformidad 1.4.5")

- **1.4.6 Contraste (mejorado):** La presentación visual de [texto](http://sidar.org/traducciones/wcag20/es/#textdef "definición: texto") e [imágenes de texto](http://sidar.org/traducciones/wcag20/es/#images-of-textdef "definición: imágenes de texto") tiene una [relación de contraste](http://sidar.org/traducciones/wcag20/es/#contrast-ratiodef "definición: relación de contraste") de, al menos, 7:1, excepto en los siguientes casos. (Nivel AAA)

- **1.4.7 Sonido de fondo bajo o ausente:** Para el contenido de [sólo audio](http://sidar.org/traducciones/wcag20/es/#audio-onlydef "definición: sólo audio") [grabado](http://sidar.org/traducciones/wcag20/es/#prerecordeddef "definición: grabado") que (1) contiene habla en primer plano, (2) no es un [CAPTCHA](http://sidar.org/traducciones/wcag20/es/#CAPTCHAdef "definición: CAPTCHA") sonoro o un audiologo, y (3) que no es una vocalización cuya intención principal es servir como expresión musical (como el canto o el rap), se cumple al menos uno de los siguientes casos: (Nivel AAA)

  - **Ningún sonido de fondo:** El audio no contiene sonidos de fondo.

  - **Apagar:** Los sonidos de fondo pueden ser apagados.

  - **20 dB:** Los sonidos de fondo son, al menos, 20 decibelios más bajos que el discurso en primer plano, con la excepción de sonidos ocasionales que duran solamente uno o dos segundos.

      *Nota:* Por la definición de "decibelio", el sonido de fondo que cumple con este requisito es aproximadamente cuatro veces más silencioso que la locución principal.

  > [Cómo cumplir 1.4.7](http://www.w3.org/WAI/WCAG21/quickref/#qr-visual-audio-contrast-noaudio "Cómo satisfacer el Criterio de Conformidad 1.4.7")

  > [Comprender 1.4.7](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-noaudio.html "Comprender el Criterio de Conformidad 1.4.7")

- **1.4.8 Presentación visual:** En la presentación visual de [bloques de texto](http://sidar.org/traducciones/wcag20/es/#blockstextdef "definición: bloques de texto"), se proporciona algún [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") para lograr lo siguiente: (Nivel AAA)

  1.  Los colores de fondo y primer plano pueden ser elegidos por el usuario.

  2.  El ancho no es mayor de 80 caracteres o signos (40 si es CJK).

  3.  El texto no está justificado (alineado a los márgenes izquierdo y derecho a la vez).

  4.  El espacio entre líneas (interlineado) es de, al menos, un espacio y medio dentro de los párrafos y el espacio entre párrafos es, al menos, 1.5 veces mayor que el espacio entre líneas.

  5.  El texto se ajusta sin ayudas técnicas hasta un 200 por ciento de modo tal que no requiere un desplazamiento horizontal para leer una línea de texto [en una ventana a pantalla completa](http://sidar.org/traducciones/wcag20/es/#fullscreenwindowdef "definición: en una ventana a pantalla completo").

  > [Cómo cumplir 1.4.8](http://www.w3.org/WAI/WCAG21/quickref/#qr-visual-audio-contrast-visual-presentation "Cómo satisfacer el Criterio de Conformidad 1.4.8")

  > [Comprender 1.4.8](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-visual-presentation.html "Comprender el Criterio de Conformidad 1.4.8")

- **1.4.9 Imágenes de texto (sin excepciones):** Las [imágenes de texto](http://sidar.org/traducciones/wcag20/es/#images-of-textdef "definición: imágenes de texto") sólo se utilizan como [simple decoración](http://sidar.org/traducciones/wcag20/es/#puredecdef "definición: simple decoración") o cuando una forma de presentación particular del [texto](http://sidar.org/traducciones/wcag20/es/#textdef "definición: texto") resulta [esencial](http://sidar.org/traducciones/wcag20/es/#essentialdef "definición: esencial") para la información transmitida. (Nivel AAA)

*Nota:* Los logotipos (textos que son parte de un logo o de un nombre de marca) se consideran esenciales.

  > [Cómo cumplir 1.4.9](http://www.w3.org/WAI/WCAG21/quickref/#qr-visual-audio-contrast-text-images "Cómo satisfacer el Criterio de Conformidad 1.4.9")

  > [Comprender 1.4.9](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-text-images.html "Comprender el Criterio de Conformidad 1.4.9")

- **1.4.10 Reflujo (nuevo en 2.1):** El contenido se puede presentar sin pérdida de información o funcionalidad, y sin necesidad de desplazarse en dos dimensiones para:

    - Contenido de desplazamiento vertical con un ancho equivalente a 320 píxeles CSS;

    - Contenido de desplazamiento horizontal a una altura equivalente a 256 píxeles CSS;

Excepto por partes del contenido que requieren un diseño bidimensional para su uso o significado. (Nivel AA)

  > [Cómo cumplir 1.4.10](https://www.w3.org/WAI/WCAG21/quickref/#reflow "Cómo satisfacer el Criterio de Conformidad 1.4.10")

  > [Comprender 1.4.10](https://www.w3.org/WAI/WCAG21/Understanding/reflow.html "Comprender el Criterio de Conformidad 1.4.10")

- **1.4.11 No-Texto contraste (nuevo en 2.1):** La presentación visual de lo siguiente tiene una relación de contraste de al menos 3: 1 frente a los colores adyacentes:

    - **Componentes de la interfaz de usuario**: información visual necesaria para identificar los componentes y estados de la interfaz de usuario, excepto los componentes inactivos o cuando la apariencia del componente la determina el agente de usuario y el autor no la modifica;

    - **Objetos gráficos**: partes de los gráficos necesarios para comprender el contenido, excepto cuando una presentación particular de los gráficos es esencial para la información que se transmite. (Nivel AA)

  > [Cómo cumplir 1.4.11](https://www.w3.org/WAI/WCAG21/quickref/#non-text-contrast "Cómo satisfacer el Criterio de Conformidad 1.4.11")

  > [Comprender 1.4.11](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html "Comprender el Criterio de Conformidad 1.4.11")

- **1.4.12 Espaciado del texto (nuevo en 2.1):** En el contenido implementado con lenguajes de marcado que admiten las siguientes propiedades de estilo de texto, no se produce pérdida de contenido o funcionalidad al configurar todo lo siguiente y al no cambiar ninguna otra propiedad de estilo:

    - Altura de línea (interlineado) hasta al menos 1,5 veces el tamaño de la fuente;

    - Espaciar los párrafos siguientes a al menos 2 veces el tamaño de la fuente;

    - Espaciado entre letras (seguimiento) al menos 0,12 veces el tamaño de la fuente;

    - Espaciado entre palabras al menos 0,16 veces el tamaño de fuente.

  Excepción: los lenguajes humanos y las escrituras que no hacen uso de una o más de estas propiedades de estilo de texto en el texto escrito pueden ajustarse utilizando solo las propiedades que existen para esa combinación de lengua y escritura. (Nivel AA)

  > [Cómo cumplir 1.4.12](https://www.w3.org/WAI/WCAG21/quickref/#text-spacing "Cómo satisfacer el Criterio de Conformidad 1.4.12")

  > [Comprender 1.4.12](https://www.w3.org/WAI/WCAG21/Understanding/text-spacing.html "Comprender el Criterio de Conformidad 1.4.12")
  
- **1.4.13 Contenidos en Hover y Focus (nuevo en 2.1):** Cuando recibir y luego quitar el cursor del puntero o el enfoque del teclado activa contenido adicional para que se vuelva visible y luego se oculte, lo siguiente es cierto:

    - **Descartable**: hay un mecanismo disponible para descartar el contenido adicional sin mover el puntero o el foco del teclado, a menos que el contenido adicional comunique un error de entrada o no oculte o reemplace otro contenido;

    - **Posible**: si el puntero puede activar el contenido adicional, entonces el puntero se puede mover sobre el contenido adicional sin que el contenido adicional desaparezca;

    - **Persistente**: el contenido adicional permanece visible hasta que se elimina el activador de desplazamiento o enfoque, el usuario lo descarta o su información ya no es válida.

  Excepción: la presentación visual del contenido adicional está controlada por el agente de usuario y no es modificada por el autor. (Nivel AA)

  > [Cómo cumplir 1.4.13](https://www.w3.org/WAI/WCAG21/quickref/#content-on-hover-or-focus "Cómo satisfacer el Criterio de Conformidad 1.4.13")

  > [Comprender 1.4.13](https://www.w3.org/WAI/WCAG21/Understanding/content-on-hover-or-focus.html "Comprender el Criterio de Conformidad 1.4.13")
---

### 4.1.2. Principio 2: Operable

> **Los componentes de la interfaz de usuario y la navegación deben ser operables.**

#### 4.1.2.1. Pauta 2.1 Accesible por teclado

  Proporcionar acceso a toda la funcionalidad mediante el teclado.

  > [Comprender la Pauta 2.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/keyboard-operation.html)

- **2.1.1 Teclado:** Toda la [funcionalidad](http://sidar.org/traducciones/wcag20/es/#functiondef "definición: funcionalidad") del contenido es operable a través de una [interfaz de teclado](http://sidar.org/traducciones/wcag20/es/#keybrd-interfacedef "definición: interfaz de teclado") sin que se requiera una determinada velocidad para cada pulsación individual de las teclas, excepto cuando la función interna requiere de una entrada que depende del trayecto de los movimientos del usuario y no sólo de los puntos inicial y final. (Nivel A)

*Nota 1:* Esta excepción se refiere a la función subyacente, no a la técnica de entrada de datos. Por ejemplo, si la entrada de texto se hace por medio de escritura a mano, la técnica de entrada (escritura a mano) depende del trazo (ruta trazada) pero la función interna (introducir texto) no.

*Nota 2:* Esto no prohíbe ni debería desanimar a los autores a proporcionar entrada de ratón u otros métodos de entrada de datos adicionales a la operabilidad a través del teclado.

  > [Cómo cumplir 2.1.1](http://www.w3.org/WAI/WCAG21/quickref/#qr-keyboard-operation-keyboard-operable "Cómo satisfacer el Criterio de Conformidad 2.1.1")

  > [Comprender 2.1.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/keyboard-operation-keyboard-operable.html "Comprender el Criterio de Conformidad 2.1.1")

- **2.1.2 Sin trampas para el foco del teclado:** Si es posible mover el foco a un componente de la página usando una [interfaz de teclado](http://sidar.org/traducciones/wcag20/es/#keybrd-interfacedef "definición: interfaz de teclado"), entonces el foco se puede quitar de ese componente usando sólo la interfaz de teclado y, si se requiere algo más que las teclas de dirección o de tabulación, se informa al usuario el método apropiado para mover el foco. (Nivel A)

*Nota:* En la medida en que cualquier contenido que no satisfaga este criterio puede interferir con la capacidad del usuario para emplear la página por completo, todo contenido de la página web (tanto si satisface o no otros criterios de conformidad) debe satisfacer este criterio. Véase [Requisito de Conformidad 5: Sin interferencia](http://sidar.org/traducciones/wcag20/es/#cc5).

  > [Cómo cumplir 2.1.2](http://www..org/WAI/WCAG21/quickref/#qr-keyboard-operation-trapping "Cómo satisfacer el Criterio de Conformidad 2.1.2")

  > [Comprender 2.1.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/keyboard-operation-trapping.html "Comprender el Criterio de Conformidad 2.1.2")

- **2.1.3 Teclado (sin excepciones):** Toda la [funcionalidad](http://sidar.org/traducciones/wcag20/es/#functiondef "definición: funcionalidad") del contenido se puede operar a través de una [interfaz de teclado](http://sidar.org/traducciones/wcag20/es/#keybrd-interfacedef "definición: interfaz de teclado") sin requerir una determinada velocidad en la pulsación de las teclas. (Nivel AAA)

  > [Cómo cumplir 2.1.3](http://www.w3.org/WAI/WCAG21/quickref/#qr-keyboard-operation-all-funcs "Cómo satisfacer el Criterio de Conformidad 2.1.3")

  > [Comprender 2.1.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/keyboard-operation-all-funcs.html "Comprender el Criterio de Conformidad 2.1.3")

  - **2.1.4 Atajos de teclado (nuevo en 2.1):** Si se implementa un método abreviado de teclado en el contenido utilizando solo letras (incluidas letras mayúsculas y minúsculas), signos de puntuación, números o símbolos, al menos una de las siguientes condiciones es verdadera:

    - Apagar: hay un mecanismo disponible para apagar el atajo;

    - Reasignación: hay un mecanismo disponible para reasignar el atajo para incluir una o más teclas de teclado no imprimibles (por ejemplo, Ctrl, Alt);

    - Activo solo en el foco: el método abreviado de teclado para un componente de la interfaz de usuario solo está activo cuando ese componente tiene el foco. (Nivel A)

  > [Cómo cumplir 2.1.4](https://www.w3.org/WAI/WCAG21/quickref/#character-key-shortcutss "Cómo satisfacer el Criterio de Conformidad 2.1.4")

  > [Comprender 2.1.4](https://www.w3.org/WAI/WCAG21/Understanding/character-key-shortcuts.html "Comprender el Criterio de Conformidad 2.1.4")

#### 4.1.2.2. Pauta 2.2 Tiempo suficiente

  Proporcionar a los usuarios el tiempo suficiente para leer y usar el contenido.

  > [Comprender la Pauta 2.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits.html)

- **2.2.1 Tiempo ajustable:** Para cada límite de tiempo impuesto por el contenido, se cumple al menos uno de los siguientes casos: (Nivel A)

  - **Apagar:** El usuario puede detener el límite de tiempo antes de alcanzar el límite de tiempo; o

  - **Ajustar:** El usuario puede ajustar el límite de tiempo antes de alcanzar dicho límite en un rango amplio que es, al menos, diez veces mayor al tiempo fijado originalmente; o

  - **Extender:** Se advierte al usuario antes de que el tiempo expire y se le conceden al menos 20 segundos para extender el límite temporal con una acción simple (por ejemplo, "presione la barra de espacio") y el usuario puede extender ese límite de tiempo al menos diez veces; o

  - **Excepción de tiempo real:** El límite de tiempo es un requisito que forma parte de un evento en tiempo real (por ejemplo, una subasta) y no resulta posible ofrecer una alternativa al límite de tiempo; o

  - **Excepción por ser esencial:** El límite de tiempo es [esencial](http://sidar.org/traducciones/wcag20/es/#essentialdef "definición: esencial") y, si se extendiera, invalidaría la actividad; o

  - **Excepción de 20 horas:** El límite de tiempo es mayor a 20 horas.

  *Nota:* Este criterio de conformidad ayuda a asegurarse de que los usuarios puedan completar una tarea sin cambios inesperados en el contenido o contexto que sean el resultado de un límite de tiempo. Este criterio de conformidad debe considerarse en combinación con el [Criterio de Conformidad 3.2.1](http://sidar.org/traducciones/wcag20/es/#consistent-behavior-receive-focus), que impone límites a los cambios de contenido o contexto como resultado de una acción del usuario.

  > [Cómo cumplir 2.2.1](http://www.w3.org/WAI/WCAG21/quickref/#qr-time-limits-required-behaviors "Cómo satisfacer el Criterio de Conformidad 2.2.1")
  
  > [Comprender 2.2.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-required-behaviors.html "Comprender el Criterio de Conformidad 2.2.1")

- **2.2.2 Poner en pausa, detener, ocultar:** Para la información que tiene movimiento, [parpadeo](http://sidar.org/traducciones/wcag20/es/#blinksdef "definición: parpadeo"), se desplaza o se actualiza automáticamente, se cumplen todos los casos siguientes: (Nivel A)

  - **Movimiento, parpadeo, desplazamiento:** Para toda información que se mueve, parpadea o se desplaza, que (1) comienza automáticamente, (2) dura más de cinco segundos y (3) se presenta en paralelo con otro contenido, existe un mecanismo para que el usuario la pueda poner en [pausa](http://sidar.org/traducciones/wcag20/es/#pauseddef "definición: pausar"), detener u ocultar, a menos que el movimiento, parpadeo o desplazamiento sea parte [esencial](http://sidar.org/traducciones/wcag20/es/#essentialdef "definición: esencial") de una actividad; y

  - **Actualización automática:** Para toda información que se actualiza automáticamente, que (1) se inicia automáticamente y (2) se presenta en paralelo con otro contenido, existe un mecanismo para que el usuario la pueda poner en pausa, detener u ocultar, o controlar la frecuencia de actualización a menos que la actualización automática sea parte esencial de una actividad.

  *Nota 1:* Para los requisitos relacionados con el parpadeo o el destello de contenido, véase la [Pauta 2.3](http://sidar.org/traducciones/wcag20/es/#seizure).

  *Nota 2:* En la medida en que cualquier contenido que no satisfaga este criterio puede interferir con la capacidad del usuario para emplear la página como un todo, todo contenido de la página web (tanto si satisface o no otros criterios de conformidad) debe satisfacer este criterio. Véase [Requisito de Conformidad 5: Sin interferencia](http://sidar.org/traducciones/wcag20/es/#cc5).

  *Nota 3:* Para el contenido que es actualizado periódicamente por medio de un software, o que se sirve a la aplicación de usuario por medio de streaming, no hay obligación de preservar o presentar la información que ha sido generada o recibida entre el inicio de la pausa y el reinicio de la presentación; no sólo podría no ser técnicamente posible, sino que además en muchas ocasiones podría ser erróneo o engañoso hacerlo.

  *Nota 4:* Una animación que ocurre como parte de una fase de precarga de un contenido o una situación similar puede ser considerada esencial si no se permite interacción a ningún usuario durante esa fase, y si el hecho de no indicar el progreso pudiera confundir a los usuarios y hacerles creer que ha habido un fallo en el contenido.

  > [Cómo cumplir 2.2.2](http://w3.org/WAI/WCAG21/quickref/#qr-time-limits-pause "Cómo satisfacer el Criterio de Conformidad 2.2.2")
  
  > [Comprender 2.2.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-pause.html "Comprender el Criterio de Conformidad 2.2.2")

- **2.2.3 Sin tiempo:** El tiempo no es parte [esencial](http://sidar.org/traducciones/wcag20/es/#essentialdef "definición: esencial") del evento o actividad presentada por el contenido, exceptuando los [multimedia sincronizados](http://sidar.org/traducciones/wcag20/es/#synchronizedmediadef "definición: multimedia sincronizados") no interactivos y los [eventos en tiempo real](http://sidar.org/traducciones/wcag20/es/#real-time-eventsdef "definición: evento en tiempo real"). (Nivel AAA)

  > [Cómo cumplir 2.2.3](http://www.rg/WAI/WCAG21/quickref/#qr-time-limits-no-exceptions "Cómo satisfacer el Criterio de Conformidad 2.2.3")
  
  > [Comprender 2.2.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-no-exceptions.html "Comprender el Criterio de Conformidad 2.2.3")

- **2.2.4 Interrupciones:** El usuario puede postergar o suprimir las interrupciones, excepto cuando las interrupciones implican una [emergencia](http://sidar.org/traducciones/wcag20/es/#emergencydef "definición: emergencia"). (Nivel AAA)

  > [Cómo cumplir 2.2.4](http://w3.org/WAI/WCAG21/quickref/#qr-time-limits-postponed "Cómo satisfacer el Criterio de Conformidad 2.2.4")
  
  > [Comprender 2.2.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-postponed.html "Comprender el Criterio de Conformidad 2.2.4")

- **2.2.5 Re-autentificación:** Cuando expira una sesión autentificada, el usuario puede continuar la actividad sin pérdida de datos tras volver a identificarse. (Nivel AAA)

  > [Cómo cumplir 2.2.5](http://www..org/WAI/WCAG21/quickref/#qr-time-limits-server-timeout "Cómo satisfacer el Criterio de Conformidad 2.2.5")
  
  > [Comprender 2.2.5](http://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-server-timeout.html "Comprender el Criterio de Conformidad 2.2.5")

- **2.2.6 Timeouts (nuevo en 2.1):** Se advierte a los usuarios sobre la duración de la inactividad del usuario que podría causar la pérdida de datos, a menos que los datos se conserven durante más de 20 horas cuando el usuario no realiza ninguna acción.. (Nivel AAA)

  > [Cómo cumplir 2.2.6]([http://www..org/WAI/WCAG21/quickref/#qr-time-limits-server-timeout](https://www.w3.org/WAI/WCAG21/quickref/#timeouts) "Cómo satisfacer el Criterio de Conformidad 2.2.6")
  
  > [Comprender 2.2.6](https://www.w3.org/WAI/WCAG21/Understanding/timeouts.html "Comprender el Criterio de Conformidad 2.2.6")

#### 4.1.2.3. Pauta 2.3 Convulsiones

  No diseñar contenido de un modo que se sepa podría provocar ataques, espasmos o convulsiones.

  > [Comprender la Pauta 2.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure.html)

- **2.3.1 Umbral de tres destellos o menos:** Las [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") no contienen nada que destelle más de tres veces en un segundo, o el [destello](http://sidar.org/traducciones/wcag20/es/#flash-def "definición: destello") está por debajo del [umbral de destello general y de destello rojo](http://sidar.org/traducciones/wcag20/es/#general-thresholddef "definición: umbral de destello general y de destello rojo"). (Nivel A)

*Nota:* En la medida en que cualquier contenido que no satisfaga este criterio puede interferir con la capacidad del usuario para emplear la página como un todo, todo contenido de la página web (tanto si satisface o no otros criterios de conformidad) debe satisfacer este criterio. Véase [Requisito de Conformidad 5: Sin interferencia](http://sidar.org/traducciones/wcag20/es/#cc5).

  > [Cómo cumplir 2.3.1](http://w..org/WAI/WCAG21/quickref/#qr-seizure-does-not-violate "Cómo satisfacer el Criterio de Conformidad 2.3.1")
  
  > [Comprender 2.3.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure-does-not-violate.html "Comprender el Criterio de Conformidad 2.3.1")

- **2.3.2 Tres destellos:** Las [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") no contienen nada que [destelle](http://sidar.org/traducciones/wcag20/es/#flash-def "definición: destello") más de tres veces por segundo. (Nivel AAA)

  > [Cómo cumplir 2.3.2](http://w3.org/WAI/WCAG21/quickref/#qr-seizure-three-times "Cómo satisfacer el Criterio de Conformidad 2.3.2")
  
  > [Comprender 2.3.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure-three-times.html "Comprender el Criterio de Conformidad 2.3.2")


- **2.3.3 Interacción en animaciones (nuevo en 2.1):** La animación de movimiento desencadenada por la interacción se puede desactivar, a menos que la animación sea esencial para la funcionalidad o la información que se transmite. (Nivel AAA)

  > [Cómo cumplir 2.3.3](https://www.w3.org/WAI/WCAG21/quickref/#animation-from-interactions "Cómo satisfacer el Criterio de Conformidad 2.3.3")
  
  > [Comprender 2.3.3](https://www.w3.org/WAI/WCAG21/Understanding/animation-from-interactions.html "Comprender el Criterio de Conformidad 2.3.3")
  
#### 4.1.2.4. Pauta 2.4 Navegable

  Proporcionar medios para ayudar a los usuarios a navegar, encontrar contenido y determinar dónde se encuentran.

  > [Comprender la Pauta 2.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms.html)

- **2.4.1 Evitar bloques:** Existe un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") para evitar los bloques de contenido que se repiten en múltiples [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web"). (Nivel A)

  > [Cómo cumplir 2.4.1](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-skip "Cómo satisfacer el Criterio de Conformidad 2.4.1")
  
  > [Comprender 2.4.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-skip.html "Comprender el Criterio de Conformidad 2.4.1")

- **2.4.2 Titulado de páginas:** Las [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") tienen títulos que describen su temática o propósito. (Nivel A)

  > [Cómo cumplir 2.4.2](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-title "Cómo satisfacer el Criterio de Conformidad 2.4.2")
  
  > [Comprender 2.4.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-title.html "Comprender el Criterio de Conformidad 2.4.2")

- **2.4.3 Orden del foco:** Si se puede [navegar secuencialmente](http://sidar.org/traducciones/wcag20/es/#nav-seqdef "definición: navegada secuencialmente") por una [página web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") y la secuencia de navegación afecta su significado o su operación, los componentes que pueden recibir el foco lo hacen en un orden que preserva su significado y operabilidad. (Nivel A)

  > [Cómo cumplir 2.4.3](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-focus-order "Cómo satisfacer el Criterio de Conformidad 2.4.3")
  
  > [Comprender 2.4.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-focus-order.html "Comprender el Criterio de Conformidad 2.4.3")

- **2.4.4 Propósito de los enlaces (en contexto):** El [propósito de cada enlace](http://sidar.org/traducciones/wcag20/es/#linkpurposedef "definición: propósito de cada enlace") puede ser determinado con sólo el texto del enlace o a través del texto del enlace sumado al [contexto del enlace determinado por software](http://sidar.org/traducciones/wcag20/es/#pdlinkcontextdef "definición: contexto del enlace determinado por software"), excepto cuando el propósito del enlace resultara [ambiguo para los usuarios en general](http://sidar.org/traducciones/wcag20/es/#ambiguouslinkdef "definición: ambiguo para los usuarios en general"). (Nivel A)

  > [Cómo cumplir 2.4.4](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-refs "Cómo satisfacer el Criterio de Conformidad 2.4.4")
  
  > [Comprender 2.4.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-refs.html "Comprender el Criterio de Conformidad 2.4.4")

- **2.4.5 Múltiples vías:** Se proporciona más de un camino para localizar una [página web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") dentro de un [conjunto de páginas web](http://sidar.org/traducciones/wcag20/es/#set-of-web-pagesdef "definición: conjunto de páginas web"), excepto cuando la página es el resultado, o un paso intermedio, de un [proceso](http://sidar.org/traducciones/wcag20/es/#processdef "definición: proceso"). (Nivel AA)

  > [Cómo cumplir 2.4.5](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-mult-loc "Cómo satisfacer el Criterio de Conformidad 2.4.5")
  
  > [Comprender 2.4.5](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-mult-loc.html "Comprender el Criterio de Conformidad 2.4.5")

- **2.4.6 Encabezados y etiquetas:** Los encabezados y [etiquetas](http://sidar.org/traducciones/wcag20/es/#labeldef "definición: etiquetas") describen el tema o propósito. (Nivel AA)

  > [Cómo cumplir 2.4.6](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-descriptive "Cómo satisfacer el Criterio de Conformidad 2.4.6")
  
  > [Comprender 2.4.6](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-descriptive.html "Comprender el Criterio de Conformidad 2.4.6")

- **2.4.7 Foco visible:** Cualquier interfaz de usuario operable por teclado tiene una forma de operar en la cuál el indicador del foco del teclado resulta visible. (Nivel AA)

  > [Cómo cumplir 2.4.7](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-focus-visible "Cómo satisfacer el Criterio de Conformidad 2.4.7")
  
  > [Comprender 2.4.7](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-focus-visible.html "Comprender el Criterio de Conformidad 2.4.7")

- **2.4.8 Ubicación:** Se proporciona información acerca de la ubicación del usuario dentro de un [conjunto de páginas web](http://sidar.org/traducciones/wcag20/es/#set-of-web-pagesdef "definición: conjunto de páginas web"). (Nivel AAA)

  > [Cómo cumplir 2.4.8](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-location "Cómo satisfacer el Criterio de Conformidad 2.4.8")
  
  > [Comprender 2.4.8](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-location.html "Comprender el Criterio de Conformidad 2.4.8")

- **2.4.9 Propósito de los enlaces (sólo enlaces):** Se proporciona un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") que permite identificar el propósito de cada enlace con sólo el texto del enlace, excepto cuando el propósito del enlace resultara [ambiguo para los usuarios en general](http://sidar.org/traducciones/wcag20/es/#ambiguouslinkdef "definición: ambiguo para los usuarios en general"). (Nivel AAA)

  > [Cómo cumplir 2.4.9](http://www..org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-link "Cómo satisfacer el Criterio de Conformidad 2.4.9")
  
  > [Comprender 2.4.9](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-link.html "Comprender el Criterio de Conformidad 2.4.9")

- **2.4.10 Encabezados de sección:** Se usan encabezados de [sección](http://sidar.org/traducciones/wcag20/es/#sectiondef "definición: sección") para organizar el contenido. (Nivel AAA)

*Nota 1:* "Encabezados" se usa en sentido general e incluye los títulos y otras formas de agregar encabezados a las distintos tipos de contenido.

*Nota 2:* Este criterio de conformidad se refiere al contenido propiamente dicho, no a los [componentes de la interfaz de usuario](http://sidar.org/traducciones/wcag20/es/#user-interface-componentdef "definición: componentes de la interfaz de usuario"). Los componentes de la interfaz de usuario se tratan en el [Criterio de Conformidad 4.1.2](http://www.w3.org/TR/2008/REC-WCAG20-20081211/#ensure-compat-rsv).

  > [Cómo cumplir 2.4.10](http://www.w3.org/WAI/WCAG21/quickref/#qr-navigation-mechanisms-headings "Cómo satisfacer el Criterio de Conformidad 2.4.10")
  
  > [Comprender 2.4.10](http://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-headings.html "Comprender el Criterio de Conformidad 2.4.10")

#### 4.1.2.5. Pauta 2.5 Modalidades de entrada

  Facilitar a los usuarios operar la funcionalidad a través de varias entradas más allá del teclado.

  > [Comprender la Pauta 2.5](http://www.w3.org/TR/UNDERSTANDING-WCAG21/navigation-mechanisms.html)

- **2.5.1 Gestos de puntero (nuevo en 2.1) :** Toda la funcionalidad que utiliza gestos multipunto o basados en ruta para la operación se puede operar con un solo puntero sin un gesto basado en ruta, a menos que sea esencial un gesto multipunto o basado en ruta. (Nivel A)

  > [Cómo cumplir 2.5.1](https://www.w3.org/WAI/WCAG21/quickref/#pointer-gestures "Cómo satisfacer el Criterio de Conformidad 2.5.1")
  
  > [Comprender 2.5.1](https://www.w3.org/WAI/WCAG21/Understanding/pointer-gestures.htmll "Comprender el Criterio de Conformidad 2.5.1")

- **2.5.2 Cancelación de puntero (nuevo en 2.1) :** Para la funcionalidad que se puede operar con un solo puntero, al menos uno de los siguientes es verdadero:

    - **Sin evento de bajada**: el evento de bajada del puntero no se utiliza para ejecutar ninguna parte de la función;

    - **Abortar o Deshacer**: La finalización de la función está en el evento up, y hay un mecanismo disponible para abortar la función antes de la finalización o para deshacer la función después de la finalización;

    - **Inversión ascendente**: el evento ascendente invierte cualquier resultado del evento descendente anterior;

    - **Esencial**: completar la función en el evento de caída es esencial.(Nivel A)

  > [Cómo cumplir 2.5.2](https://www.w3.org/WAI/WCAG21/quickref/#pointer-cancellation "Cómo satisfacer el Criterio de Conformidad 2.5.2")
  
  > [Comprender 2.5.2](https://www.w3.org/WAI/WCAG21/Understanding/pointer-cancellation.html "Comprender el Criterio de Conformidad 2.5.2")
  
- **2.5.3 Etiqueta en nombre (nuevo en 2.1) :** Para los componentes de la interfaz de usuario con etiquetas que incluyen texto o imágenes de texto, el nombre contiene el texto que se presenta visualmente. (Nivel A)

  > [Cómo cumplir 2.5.3](https://www.w3.org/WAI/WCAG21/quickref/#label-in-name "Cómo satisfacer el Criterio de Conformidad 2.5.3")
  
  > [Comprender 2.5.3](https://www.w3.org/WAI/WCAG21/Understanding/label-in-name.html "Comprender el Criterio de Conformidad 2.5.3")
  
- **2.5.4 Actuación por movimiento (nuevo en 2.1) :** La funcionalidad que puede ser operada por el movimiento del dispositivo o el movimiento del usuario también puede ser operada por los componentes de la interfaz de usuario y la respuesta al movimiento puede desactivarse para evitar una actuación accidental, excepto cuando:

    - **Interfaz compatible**: el movimiento se utiliza para operar la funcionalidad a través de una interfaz compatible con la accesibilidad;

    - **Esencial**: el movimiento es esencial para la función y hacerlo invalidaría la actividad. (Nivel A)

  > [Cómo cumplir 2.5.4](https://www.w3.org/WAI/WCAG21/quickref/#motion-actuation "Cómo satisfacer el Criterio de Conformidad 2.5.4")
  
  > [Comprender 2.5.4](https://www.w3.org/WAI/WCAG21/Understanding/motion-actuation.html "Comprender el Criterio de Conformidad 2.5.4")
  
- **2.5.5 Tamaño del objetivo (nuevo en 2.1) :** El tamaño del objetivo para las entradas del puntero es de al menos 44 por 44 píxeles CSS, excepto cuando:

    - **Equivalente**: el destino está disponible a través de un enlace o control equivalente en la misma página que tiene al menos 44 por 44 píxeles CSS;

    - **Inline**: el objetivo está en una oración o bloque de texto;

    - **Control de agente de usuario**: el agente de usuario determina el tamaño del objetivo y el autor no lo modifica;

    - **Esencial**: una presentación particular del objetivo es esencial para la información que se transmite.. (Nivel AAA)

  > [Cómo cumplir 2.5.5](https://www.w3.org/WAI/WCAG21/quickref/#target-size "Cómo satisfacer el Criterio de Conformidad 2.5.5")
  
  > [Comprender 2.5.5](https://www.w3.org/WAI/WCAG21/Understanding/target-size.html "Comprender el Criterio de Conformidad 2.5.5")
  
- **2.5.6 Mecanismos de entrada concurrentes (nuevo en 2.1) :** El contenido web no restringe el uso de las modalidades de entrada disponibles en una plataforma, excepto cuando la restricción es esencial, requerida para garantizar la seguridad del contenido o requerida para respetar la configuración del usuario. (Nivel AAA)

  > [Cómo cumplir 2.5.6](https://www.w3.org/WAI/WCAG21/quickref/#concurrent-input-mechanisms "Cómo satisfacer el Criterio de Conformidad 2.5.6")
  
  > [Comprender 2.5.6](https://www.w3.org/WAI/WCAG21/Understanding/concurrent-input-mechanisms.html "Comprender el Criterio de Conformidad 2.5.6")
---

### 4.1.3. Principio 3: Comprensible 

> **La información y el manejo de la interfaz de usuario deben ser comprensibles.**

#### 4.1.3.1. Pauta 3.1 Legible

  Hacer que los contenidos textuales resulten legibles y comprensibles.

  > [Comprender la Pauta 3.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning.html)

- **3.1.1 Idioma de la página:** El [idioma](http://sidar.org/traducciones/wcag20/es/#human-langdef "definición: idioma") predeterminado de cada [página web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") puede ser [determinado por software](http://sidar.org/traducciones/wcag20/es/#programmaticallydetermineddef "definición: determinado por software"). (Nivel A)

  > [Cómo cumplir 3.1.1](http://w3.org/WAI/WCAG21/quickref/#qr-meaning-doc-lang-id "Cómo satisfacer el Criterio de Conformidad 3.1.1")
  
  > [Comprender 3.1.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning-doc-lang-id.html "Comprender el Criterio de Conformidad 3.1.1")

- **3.1.2 Idioma de las partes:** El [idioma](http://sidar.org/traducciones/wcag20/es/#human-langdef "definición: idioma") de cada pasaje o frase en el contenido puede ser [determinado por software](http://sidar.org/traducciones/wcag20/es/#programmaticallydetermineddef "definición: determinado por software"), excepto los nombres propios, términos técnicos, palabras en un idioma indeterminado y palabras o frases que se hayan convertido en parte natural del texto que las rodea. (Nivel AA)

  > [Cómo cumplir 3.1.2](http://w3.org/WAI/WCAG21/quickref/#qr-meaning-other-lang-id "Cómo satisfacer el Criterio de Conformidad 3.1.2")
  
  > [Comprender 3.1.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning-other-lang-id.html "Comprender el Criterio de Conformidad 3.1.2")

- **3.1.3 Palabras inusuales:** Se proporciona un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") para identificar las definiciones específicas de palabras o frases [usadas de modo inusual o restringido](http://sidar.org/traducciones/wcag20/es/#unusual-restricteddef "definición: usadas de modo inusual o restringido"), incluyendo [expresiones idiomáticas](http://sidar.org/traducciones/wcag20/es/#idiomsdef "definición: expresiones idiomáticas") y [jerga](http://sidar.org/traducciones/wcag20/es/#jargondef "definición: jergas"). (Nivel AAA)

  > [Cómo cumplir 3.1.3](http://www.w3.org/WAI/WCAG21/quickref/#qr-meaning-idioms "Cómo satisfacer el Criterio de Conformidad 3.1.3")
  
  > [Comprender 3.1.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning-idioms.html "Comprender el Criterio de Conformidad 3.1.3")

- **3.1.4 Abreviaturas:** Se proporciona un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") para identificar la forma expandida o el significado de las [abreviaturas](http://sidar.org/traducciones/wcag20/es/#abbreviationsdef "definición: abreviaturas"). (Nivel AAA)

  > [Cómo cumplir 3.1.4]ttp://www.w3.org/WAI/WCAG21/quickref/#qr-meaning-located "Cómo satisfacer el Criterio de Conformidad 3.1.4")
  
  > [Comprender 3.1.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning-located.html "Comprender el Criterio de Conformidad 3.1.4")

- **3.1.5 Nivel de lectura:** Cuando un texto requiere un nivel de lectura más avanzado que el [nivel mínimo de educación secundaria](http://sidar.org/traducciones/wcag20/es/#lowseceddef "definición: nivel mínimo de educación secundaria") una vez que se han eliminado nombres propios y títulos, se proporciona un [contenido suplementario](http://sidar.org/traducciones/wcag20/es/#suppcontentdef "definición: contenido suplementario") o una versión que no requiere un nivel de lectura mayor a ese nivel educativo. (Nivel AAA)

  > [Cómo cumplir 3.1.5](http://w3.org/WAI/WCAG21/quickref/#qr-meaning-supplements "Cómo satisfacer el Criterio de Conformidad 3.1.5")
  
  > [Comprender 3.1.5](http://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning-supplements.html "Comprender el Criterio de Conformidad 3.1.5")

**3.1.6 Pronunciación:** Se proporciona un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") para identificar la pronunciación específica de las palabras cuando el significado de esas palabras, dentro del contexto, resulta ambiguo si no se conoce su pronunciación. (Nivel AAA)

  > [Cómo cumplir 3.1.6](http://w3.org/WAI/WCAG21/quickref/#qr-meaning-pronunciation "Cómo satisfacer el Criterio de Conformidad 3.1.6")
  
  > [Comprender 3.1.6](http://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning-pronunciation.html "Comprender el Criterio de Conformidad 3.1.6")

#### 4.1.3.2. Pauta 3.2 Predecible

  Hacer que las páginas web aparezcan y operen de manera predecible.

  > [Comprender la Pauta 3.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior.html)

- **3.2.1 Al recibir el foco:** Cuando cualquier componente recibe el foco, no inicia ningún [cambio en el contexto](http://sidar.org/traducciones/wcag20/es/#context-changedef "definición: cambio en el contexto"). (Nivel A)

  > [Cómo cumplir 3.2.1](http://www.w3.org/WAI/20/quickref/#qr-consistent-behavior-receive-focus "Cómo satisfacer el Criterio de Conformidad 3.2.1")
  
  > [Comprender 3.2.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-receive-focus.html "Comprender el Criterio de Conformidad 3.2.1")

- **3.2.2 Al recibir entradas:** El cambio de estado en cualquier [componente de la interfaz de usuario](http://sidar.org/traducciones/wcag20/es/#user-interface-componentdef "definición: componente de la interfaz de usuario") no provoca automáticamente un [cambio en el contexto](http://sidar.org/traducciones/wcag20/es/#context-changedef "definición: cambio en el contexto") a menos que el usuario haya sido advertido de ese comportamiento antes de usar el componente. (Nivel A)

  > [Cómo cumplir 3.2.2](http://www.w3.org/WAI/WCAG20/quickref/#qr-consistent-behavior-unpredictable-change "Cómo satisfacer el Criterio de Conformidad 3.2.2")
  > [Comprender 3.2.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-unpredictable-change.html "Comprender el Criterio de Conformidad 3.2.2")

- **3.2.3 Navegación coherente:** Los mecanismos de navegación que se repiten en múltiples [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") dentro de un [conjunto de páginas web](http://sidar.org/traducciones/wcag20/es/#set-of-web-pagesdef "definición: conjunto de páginas web") aparecen siempre en el [mismo orden relativo](http://sidar.org/traducciones/wcag20/es/#samerelorderdef "definición: mismo orden relativo") cada vez que se repiten, a menos que el cambio sea provocado por el propio usuario. (Nivel AA)

  > [Cómo cumplir 3.2.3](http://www.w3.org/WAI/WCAG20/quickref/#qr-consistent-behavior-consistent-locations "Cómo satisfacer el Criterio de Conformidad 3.2.3")
  
  > [Comprender 3.2.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-consistent-locations.html "Comprender el Criterio de Conformidad 3.2.3")

- **3.2.4 Identificación coherente:** Los componentes que tienen la [misma funcionalidad](http://sidar.org/traducciones/wcag20/es/#samefunctionalitydef "definición: misma funcionalidad") dentro de un conjunto de [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") son identificados de manera coherente. (Nivel AA)

  > [Cómo cumplir 3.2.4](http://www.w3.org/WAI/WCAG20/quickre#qr-consistent-behavior-consistent-functionality "Cómo satisfacer el Criterio de Conformidad 3.2.4")
  
  > [Comprender 3.2.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-consistent-functionality.html "Comprender el Criterio de Conformidad 3.2.4")

- **3.2.5 Cambios a petición:** Los [cambios en el contexto](http://sidar.org/traducciones/wcag20/es/#context-changedef "definición: cambios en el contexto") son iniciados únicamente a solicitud del usuario o se proporciona un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") para detener tales cambios. (Nivel AAA)

  > [Cómo cumplir 3.2.5](http://www.w3.org/WAI/WCAG20/quickre#qr-consistent-behavior-no-extreme-changes-context "Cómo satisfacer el Criterio de Conformidad 3.2.5")
  
  > [Comprender 3.2.5](http://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-no-extreme-changes-context.html "Comprender el Criterio de Conformidad 3.2.5")

#### 4.1.3.3. Pauta 3.3 Entrada de datos asistida

  Ayudar a los usuarios a evitar y corregir los errores.

  > [Comprender la Pauta 3.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error.html)

- **3.3.1 Identificación de errores:** Si se detecta automáticamente un [error en la entrada de datos](http://sidar.org/traducciones/wcag20/es/#input-errordef "definición: error en la entrada de datos"), el elemento erróneo es identificado y el error se describe al usuario mediante un texto. (Nivel A)

  > [Cómo cumplir 3.3.1](http://www.w3.org/WAI/WCAG21/quickref/#qr-minimize-error-identified "Cómo satisfacer el Criterio de Conformidad 3.3.1")
  
  > [Comprender 3.3.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-identified.html "Comprender el Criterio de Conformidad 3.3.1")

- **3.3.2 Etiquetas o instrucciones:** Se proporcionan [etiquetas](http://sidar.org/traducciones/wcag20/es/#labeldef "definición: etiquetas") o instrucciones cuando el contenido requiere la introducción de datos por parte del usuario. (Nivel A)

  > [Cómo cumplir 3.3.2](http://w3.org/WAI/WCAG21/quickref/#qr-minimize-error-cues "Cómo satisfacer el Criterio de Conformidad 3.3.2")
  
  > [Comprender 3.3.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-cues.html "Comprender el Criterio de Conformidad 3.3.2")

- **3.3.3 Sugerencias ante errores:** Si se detecta automáticamente un [error en la entrada de datos](http://sidar.org/traducciones/wcag20/es/#input-errordef "definición: error en la entrada de datos") y se dispone de sugerencias para hacer la corrección, entonces se presentan las sugerencias al usuario, a menos que esto ponga en riesgo la seguridad o el propósito del contenido. (Nivel AA)

  > [Cómo cumplir 3.3.3](http://www.w3.org/WAI/WCAG21/quickref/#qr-minimize-error-suggestions "Cómo satisfacer el Criterio de Conformidad 3.3.3")
  
  > [Comprender 3.3.3](http://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-suggestions.html "Comprender el Criterio de Conformidad 3.3.3")

- **3.3.4 Prevención de errores (legales, financieros, datos):** Para las [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: páginas web") que representan para el usuario [compromisos legales](http://sidar.org/traducciones/wcag20/es/#legalcommitmentsdef "definición: compromisos legales") o transacciones financieras; que modifican o eliminan datos [controlables por el usuario](http://sidar.org/traducciones/wcag20/es/#user-controllabledef "definición: controlables por el usuario") en sistemas de almacenamiento de datos; o que envían las respuestas del usuario a una prueba, se cumple al menos uno de los siguientes casos. (Nivel AA)

  1.  **Reversible:** El envío es reversible.

  2.  **Revisado:** Se verifica la información para detectar [errores en la entrada de datos](http://sidar.org/traducciones/wcag20/es/#input-errordef "definición: errores en la entrada de datos") y se proporciona al usuario una oportunidad de corregirlos.

  3.  **Confirmado:** Se proporciona un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") para revisar, confirmar y corregir la información antes de finalizar el envío de los datos.

  > [Cómo cumplir 3.3.4](http://www.w3.org/WAI/WCAG21/quickref/#qr-minimize-error-reversible "Cómo satisfacer el Criterio de Conformidad 3.3.4")
  
  > [Comprender 3.3.4](http://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-reversible.html "Comprender el Criterio de Conformidad 3.3.4")

- **3.3.5 Ayuda:** Se proporciona [ayuda dependiente del contexto](http://sidar.org/traducciones/wcag20/es/#context-sensitivehelpdef "definición: ayuda dependiente del contexto") . (Nivel AAA)

  > [Cómo cumplir 3.3.5](http://www.w3.org/WAI/WCAG21/quickref/#qr-minimize-error-context-help "Cómo satisfacer el Criterio de Conformidad 3.3.5")
  
  > [Comprender 3.3.5](http://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-context-help.html "Comprender el Criterio de Conformidad 3.3.5")

- **3.3.6 Prevención de errores (todos):** Para las [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") que requieren al usuario el envío de información, se cumple al menos uno de los siguientes casos. (Nivel AAA)

  1.  **Reversible:** El envío es reversible.

  2.  **Revisado:** Se verifica la información para detectar [errores en la entrada de datos](http://sidar.org/traducciones/wcag20/es/#input-errordef "definición: errores en la entrada de datos") y se proporciona al usuario una oportunidad de corregirlos.

  3.  **Confirmado:** Se proporciona un [mecanismo](http://sidar.org/traducciones/wcag20/es/#mechanismdef "definición: mecanismo") para revisar, confirmar y corregir la información antes de finalizar el envío de los datos.

  > [Cómo cumplir 3.3.6](http://www.w3.org/WAI/WCAG21/quickref/#qr-minimize-error-reversible-all "Cómo satisfacer el Criterio de Conformidad 3.3.6")
  
  > [Comprender 3.3.6](http://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-reversible-all.html "Comprender el Criterio de Conformidad 3.3.6")

---

### 4.1.4. Principio 4: Robusto 

> **El contenido debe ser suficientemente robusto como para ser interpretado de forma fiable por una amplia variedad de aplicaciones de usuario, incluyendo las ayudas técnicas.**

#### 4.1.4.1. Pauta 4.1 Compatible

  Maximizar la compatibilidad con las aplicaciones de usuario actuales y futuras, incluyendo las ayudas técnicas.

  > [Comprender la Pauta 4.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat.html)

- **4.1.1 Procesamiento:** En los contenidos implementados mediante el uso de lenguajes de marcas, los elementos tienen las etiquetas de apertura y cierre completas; los elementos están anidados de acuerdo a sus especificaciones; los elementos no contienen atributos duplicados y los ID son únicos, excepto cuando las especificaciones permitan estas características. (Nivel A)

*Nota:* Las etiquetas de apertura y cierre a las que les falte un carácter crítico para su formación, como un signo de "mayor qué", o en las que falten las comillas de apertura o cierre en el valor de un atributo, no se consideran completas.

  > [Cómo cumplir 4.1.1](http://w3.org/WAI/WCAG21/quickref/#qr-ensure-compat-parses "Cómo satisfacer el Criterio de Conformidad 4.1.1")
  
  > [Comprender 4.1.1](http://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-parses.html "Comprender el Criterio de Conformidad 4.1.1")

- **4.1.2 Nombre, función, valor:** Para todos los [componentes de la interfaz de usuario](http://sidar.org/traducciones/wcag20/es/#user-interface-componentdef "definición: componente de la interfaz de usuario") (incluyendo pero no limitado a: elementos de formulario, enlaces y componentes generados por scripts), el [nombre](http://sidar.org/traducciones/wcag20/es/#namedef "definición: nombre") y la [función](http://sidar.org/traducciones/wcag20/es/#roledef "definición: función") pueden ser [determinados por software](http://sidar.org/traducciones/wcag20/es/#programmaticallydetermineddef "definición: determinado por software"); los estados, propiedades y valores que pueden ser asignados por el usuario pueden ser [especificados por software](http://sidar.org/traducciones/wcag20/es/#programmaticallysetdef "definición: especificado por software"); y los cambios en estos elementos se encuentran disponibles para su consulta por las [aplicaciones de usuario](http://sidar.org/traducciones/wcag20/es/#useragentdef "definición: aplicaciones de usuario"), incluyendo las [ayudas técnicas](http://sidar.org/traducciones/wcag20/es/#atdef "definición: ayudas técnicas"). (Nivel A)

*Nota:* Este criterio de conformidad se dirige principalmente a los autores web que desarrollan o programan sus propios componentes de interfaz de usuario. Por ejemplo, los controles estándar de HTML satisfacen automáticamente este criterio cuando se emplean de acuerdo con su especificación.

  > [Cómo cumplir 4.1.2](http://www.w3.org/WAI/WCAG21/quickref/#qr-ensure-compat-rsv "Cómo satisfacer el Criterio de Conformidad 4.1.2")
  
  > [Comprender 4.1.2](http://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html "Comprender el Criterio de Conformidad 4.1.2")

- **4.1.3 Mensajes de estado (nueva en 2.1):** En el contenido implementado mediante lenguajes de marcado, los mensajes de estado se pueden determinar mediante programación a través de funciones o propiedades, de modo que se puedan presentar al usuario mediante tecnologías de asistencia sin recibir atención.. (Nivel AA)

  > [Cómo cumplir 4.1.3](https://www.w3.org/WAI/WCAG21/quickref/#status-messages "Cómo satisfacer el Criterio de Conformidad 4.1.3")
  
  > [Comprender 4.1.3](https://www.w3.org/WAI/WCAG21/Understanding/name-role-value.html "Comprender el Criterio de Conformidad 4.1.2")


## 4.2. Conformidad

En esta sección se presentan los requisitos de [conformidad](http://sidar.org/traducciones/wcag20/es/#conformancedef "definición: conformidad") con las WCAG 2.0. 

También se proporciona información acerca de cómo realizar declaraciones de conformidad, las cuales son opcionales. Finalmente, se describe el significado de [compatible con la accesibilidad](http://sidar.org/traducciones/wcag20/es/#accessibility-supporteddef "definición: compatible con la accesibilidad"), ya que sólo se puede [depender](http://sidar.org/traducciones/wcag20/es/#reliedupondef "definición: depender") de las tecnologías que se usan de un modo compatible con la accesibilidad para satisfacer la conformidad. 

En [Comprender la Conformidad](http://www.w3.org/TR/UNDERSTANDING-WCAG20/conformance.html) se incluye más información acerca del concepto de compatible con la accesibilidad.

### 4.2.1. Requisitos de conformidad

Para que una página web sea conforme con las WCAG 2.0, deben satisfacerse todos los requisitos de conformidad siguientes:

1. **Nivel de conformidad:** Uno de los siguientes niveles de conformidad se satisface por completo.

  - **Nivel A:** Para lograr conformidad con el Nivel A (el mínimo), la [página web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") [satisface](http://sidar.org/traducciones/wcag20/es/#satisfiesdef "definición: satisfacer un criterio de conformidad") todos los Criterios de Conformidad del Nivel A, o proporciona una [versión alternativa conforme](http://sidar.org/traducciones/wcag20/es/#conforming-alternate-versiondef "definición: versión alternativa conforme").

  - **Nivel AA:** Para lograr conformidad con el Nivel AA, la página web satisface todos los Criterios de Conformidad de los Niveles A y AA, o se proporciona una versión alternativa conforme al Nivel AA.

  - **Nivel AAA:** Para lograr conformidad con el Nivel AAA, la página web satisface todos los Criterios de Conformidad de los Niveles A, AA y AAA, o proporciona una versión alternativa conforme al Nivel AAA.

*Nota 1:* Aunque la conformidad sólo puede alcanzarse en los niveles mencionados, se alienta a los autores a notificar en sus declaraciones cualquier avance que hayan realizado para satisfacer los criterios de conformidad de un nivel de conformidad mayor al que hayan alcanzado.

*Nota 2:* No se recomienda que el Nivel de Conformidad AAA sea requerido como política general para la totalidad de un sitio web, ya que en algunos contenidos no es posible satisfacer todos los Criterios de Conformidad de Nivel AAA.

2. **Páginas completas:** La [conformidad](http://sidar.org/traducciones/wcag20/es/#conformancedef "definición: conformidad") (y el nivel de conformidad) se aplica a [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") completas, y no se puede alcanzar si se excluye una parte de la página.

*Nota 1:* Con el fin de determinar el nivel de conformidad, se considera que las alternativas a parte del contenido de una página son parte de esa página si se puede acceder a ellas directamente desde la página, por ejemplo, en el caso de una descripción extensa o la presentación alternativa de un vídeo.

*Nota 2:* Los autores de las páginas web que no cumplen con los requisitos debido a que parte del contenido está fuera de su control, pueden considerar la opción de una [Declaración de Conformidad Parcial](http://www.w3.org/TR/2008/REC-WCAG20-20081211/#conformance-partial).

3. **Procesos completos:** Cuando una [página web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") es parte de una serie de páginas web que presentan un [proceso](http://sidar.org/traducciones/wcag20/es/#processdef "definición: proceso") (es decir, una secuencia de pasos que es necesario completar para realizar una actividad), todas las páginas en ese proceso deben ser conformes con el nivel especificado o uno superior. (No es posible lograr conformidad con un nivel en particular si una de las páginas del proceso no cumple con ese nivel o uno superior).

*Ejemplo:* Una tienda en línea tiene una serie de páginas en las que se pueden seleccionar y comprar productos. Todas y cada una de las páginas de la serie de páginas de principio a fin (el pago) deben cumplir con los requisitos de conformidad para que se considere que cada una de ellas es también conforme.

4. **Uso de tecnologías exclusivamente según métodos que sean compatibles con la accesibilidad:** Para satisfacer los criterios de conformidad sólo se [depende](http://sidar.org/traducciones/wcag20/es/#reliedupondef "definición: depender") de aquellos usos de las [tecnologías](http://sidar.org/traducciones/wcag20/es/#technologydef "definición: tecnologías") que sean [compatibles con la accesibilidad](http://sidar.org/traducciones/wcag20/es/#accessibility-supporteddef "definición: compatible con la accesibilidad"). Toda información o funcionalidad que se proporcione de una forma que no sea compatible con la accesibilidad debe estar disponible de una forma que sí sea compatible con la accesibilidad. (Véase [Comprender Compatible con la Accesibilidad](http://www.w3.org/TR/UNDERSTANDING-WCAG20/conformance.html#uc-accessibility-support-head).)

5. **Sin interferencia:** Si las [tecnologías](http://sidar.org/traducciones/wcag20/es/#technologydef "definición: tecnologías (contenido web)") se usan de una forma que no es [compatible con la accesibilidad](http://sidar.org/traducciones/wcag20/es/#accessibility-supporteddef "definición: compatible con la accesibilidad"), o está usada de una forma que no cumple los requisitos de conformidad, no debe impedir a los usuarios acceder al contenido del resto de la página. Además, es necesario que la [página web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web") como un todo siga cumpliendo con los requisitos de conformidad en las siguientes circunstancias:

  1.  cuando cualquier tecnología de la que no se [depende](http://sidar.org/traducciones/wcag20/es/#reliedupondef "definición: depender") está activada en una aplicación de usuario,

  2.  cuando cualquier tecnología de la que no se depende está desactivada en una aplicación de usuario, y

  3.  cuando cualquier tecnología de la que no se depende no es soportada por una aplicación de usuario

Además, los siguientes criterios de conformidad se aplican a todo el contenido de la página, incluyendo el contenido del que, de todos modos, no se depende para alcanzar la conformidad, ya que su incumplimiento puede interferir con el uso de la página:

- ***1.4.2 - Control del audio***,

- ***2.1.2 - Sin trampas para el foco del teclado***,

- ***2.3.1 - Umbral de tres destellos o menos***, y

- ***2.2.2 - Poner en pausa, detener, ocultar***.

*Nota:* Si una página no puede cumplir con los requisitos (por ejemplo, una página de prueba de conformidad o una página de ejemplo), no puede ser incluida en el ámbito de la conformidad ni en la declaración de conformidad.

Para más información, ejemplos incluidos, véase [Comprender los Requisitos de Conformidad](http://www.w3.org/TR/UNDERSTANDING-WCAG20/conformance.html#uc-conformance-requirements-head).

### 4.2.2. Declaraciones de conformidad (opcional)

La conformidad se aplica sólo a las [páginas web](http://sidar.org/traducciones/wcag20/es/#webpagedef "definición: página web"). Sin embargo, la declaración de conformidad puede cubrir una sola página, una serie de páginas o múltiples páginas web relacionadas.

#### 4.2.2.1. Componentes exigidos en la declaración de conformidad

Las declaraciones de conformidad **no son obligatorias**. Los autores pueden cumplir con los requisitos de las WCAG 2.0 sin realizar la declaración. Sin embargo, si se realiza la declaración, ésta **debe** contener la siguiente información:

1. **Fecha** de la declaración

2. **Título de las pautas, versión y URI** "Web Content Accessibility Guidelines 2.0 en <http://www.w3.org/TR/2008/REC-WCAG20-20081211/>"

3. **Nivel de conformidad** satisfecho: (Nivel A, AA o AAA)

4. **Una breve descripción de las páginas web**, como por ejemplo una lista de sus URI para las que se hace la declaración, incluyendo si los subdominios están incluidos en la declaración.

    *Nota 1:* Las páginas web pueden ser descritas por medio de una lista o de una expresión que describa todas las URI incluidas en la declaración.

    *Nota 2:* El autor puede declarar que, para los productos basados en web que no tienen un URI antes de su instalación en el sitio web del cliente, el producto será conforme cuando se instale.

5. Una lista de las **[tecnologías de contenido web](http://sidar.org/traducciones/wcag20/es/#technologydef "definición: tecnologías (contenido web)") de las que se [depende](http://sidar.org/traducciones/wcag20/es/#reliedupondef "definición: depender")**.

*Nota:* Si se emplea un logo de conformidad, éste constituye una declaración y debe estar acompañado de todos los componentes requeridos para una declaración de conformidad declarados anteriormente.

#### 4.2.2.2. Componentes opcionales de la declaración de conformidad

Además de los componentes exigidos arriba para una declaración de conformidad, considere incluir información adicional para ayudar a los usuarios. La información adicional recomendada incluye:

- Una lista de los criterios de conformidad satisfechos más allá del nivel de conformidad declarado. Esta información debería proporcionarse de forma tal que el usuario pueda emplearla, preferiblemente en forma de metadatos legibles por máquinas.

- Una lista de las tecnologías específicas que "*se emplean pero de las que no se [depende](http://sidar.org/traducciones/wcag20/es/#reliedupondef "definición: depender")*."

- Una lista de las aplicaciones de usuario, incluyendo las ayudas técnicas que se han empleado para probar los contenidos.

- Información sobre cualquier paso adicional que se haya dado para mejorar la accesibilidad más allá de los criterios de conformidad.

- Una versión de metadatos legible por máquinas de la lista de tecnologías específicas de las que se [depende](http://sidar.org/traducciones/wcag20/es/#reliedupondef "definición: depender").

- Una versión de metadatos legibles por máquinas de la declaración de conformidad.

*Nota 1:* Véase [Comprender las Declaraciones de Conformidad](http://www.w3.org/TR/UNDERSTANDING-WCAG20/conformance.html#uc-conformance-claims-head) para más información y ejemplos de declaraciones de conformidad.

*Nota 2:* Véase [Comprender los Metadatos](http://www.w3.org/TR/UNDERSTANDING-WCAG20/appendixC.html#understanding-metadata) para más información sobre el uso de metadatos en las declaraciones de conformidad.

### 4.2.3. Enunciado de conformidad parcial - Contenido de terceras partes

En ocasiones se crean páginas web que recibirán luego contenido adicional. Es el caso, por ejemplo, de un programa de correo electrónico, un blog, un artículo que permita a los usuarios agregar comentarios o las aplicaciones que permiten a los usuarios aportar contenido. Otro ejemplo sería una página, como un portal o un sitio de noticias, que esté compuesto por contenido generado por múltiples usuarios, o los sitios que, a lo largo del tiempo, insertan contenido automáticamente desde otras fuentes, como cuando se inserta publicidad dinámicamente.

En estos casos, no es posible saber en el momento de la creación de la página cómo será este contenido sobre el cual el autor no tiene control. Es importante destacar que el contenido sobre el cual no se tiene control también puede afectar a la accesibilidad del contenido controlado. Ante esta situación hay dos opciones posibles:

1. Se puede redactar una resolución de conformidad basada en un conocimiento óptimo. Si una página es constantemente revisada y reparada (el contenido no conforme se elimina o se hace conforme) en el periodo de dos días laborales, puede hacerse una resolución o declaración de conformidad, ya que a excepción de los errores en el contenido aportado externamente, que son corregidos o eliminados cuando son detectados, la página cumple con los requisitos de conformidad. No se puede hacer una declaración de conformidad si no es posible controlar o corregir el contenido no conforme.

    **O**

2. Se puede redactar un "enunciado de conformidad parcial" que indique que la página no es conforme, pero que lo sería si ciertas partes fueran eliminadas. La forma de este enunciado podría ser "Esta página no cumple con los requisitos de conformidad de las WCAG 2.0, pero sería conforme al nivel X si las siguientes partes provenientes de fuentes no controladas fueran eliminadas". Además, las siguientes condiciones deberían ser verdaderas para el contenido no controlado descrito en el enunciado de conformidad parcial:

    1. No es un contenido que esté bajo el control del autor.

    2. El contenido se describe de manera tal que los usuarios puedan identificarlo (por ejemplo, no puede ser descrito como "todas las partes sobre las cuales no tenemos control", a menos que estén claramente etiquetadas como tales).

### 4.2.4. Enunciado de conformidad parcial - Lenguaje

Se puede hacer un "enunciado de conformidad parcial debido al lenguaje" en caso de que la página no sea conforme pero que podría serlo de existir [compatibilidad con la accesibilidad](http://sidar.org/traducciones/wcag20/es/#accessibility-supporteddef "definición: compatible con la accesibilidad") para el lenguaje (o todos los lenguajes) empleado en la página. La forma de este enunciado podría ser: "Esta página no es conforme, pero podría ser conforme con el nivel X si existiera soporte accesible para el/los siguiente/s lenguaje/s:"




  *Fuente:* [Web Content Accessibility Guidelines (WCAG) 2.0](http://sidar.org/traducciones/wcag20/es/#guidelines)
