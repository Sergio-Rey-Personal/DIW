# 2. **Barreras de accesibilidad web**

Tabla de contenidos

- [2. **Barreras de accesibilidad web**](#2-barreras-de-accesibilidad-web)
  - [2.1. Barreras derivadas del entorno](#21-barreras-derivadas-del-entorno)
  - [2.2. Barreras por tipo de perfil](#22-barreras-por-tipo-de-perfil)
    - [2.2.1. Ceguera:](#221-ceguera)
    - [2.2.2. Baja visión:](#222-baja-visión)
    - [2.2.3. Daltonismo:](#223-daltonismo)
    - [2.2.4. Auditivas:](#224-auditivas)
    - [2.2.5. Motrices:](#225-motrices)
    - [2.2.6. Neurológicas o cognitivas (dislexia, trastornos de atención, falta de memoria...):](#226-neurológicas-o-cognitivas-dislexia-trastornos-de-atención-falta-de-memoria)
  - [2.3. Ayudas técnicas y productos de apoyo](#23-ayudas-técnicas-y-productos-de-apoyo)
    - [2.3.1. Línea braille](#231-línea-braille)
    - [2.3.2. Lectores de pantalla](#232-lectores-de-pantalla)
    - [2.3.3. Licornio](#233-licornio)
    - [2.3.4. Ratones especiales](#234-ratones-especiales)
    - [2.3.5. Navegadores de voz](#235-navegadores-de-voz)
    - [2.3.6. Webcams para seguimiento de ojos o cara](#236-webcams-para-seguimiento-de-ojos-o-cara)

La **accesibilidad web** consiste en desarrollar **aplicaciones web** que puedan ser **utilizadas** por el mayor número de **usuarios con necesidades específicas**. Estas necesidades pueden ser debidas a **limitaciones derivadas del entorno** o **derivadas de problemas visuales, auditivos, motrices y neurológicos** (dislexia, trastornos de atención, falta de memoria...).

## 2.1. Barreras derivadas del entorno 

- **Navegadores antiguos**: Proporcionar alternativas cuando se utilizan elementos que no tienen soporte en tecnologías antiguas. Si usamos Javascript para mostrar un menú, este debe funcionar igualmente aunque la tecnología no esté disponible. 
- **Navegadores de texto**: Incluir un equivalente textual para todos los elementos no textuales(imágenes, vídeos o sonidos)
- **Conexiones lentas**: minimizar el tiempo de carga de los elementos de la web.
- **Pantallas pequeñas o muy grandes:** diseño web responsive.
- **Monitores monocromos**: evitar funcionalidades que se interpretan por su color, etc.

## 2.2. Barreras por tipo de perfil

### 2.2.1. Ceguera:

- Las **imágenes sin texto alternativo** no pueden ser leídas por los lectores de pantalla.
- Las **imágenes que incluyen gráficos que representan datos** o **textos insertados mediante imágenes** tampoco son leídos por los lectores de pantalla.
- **Elementos multimedia** sin descripción textual.
- **Tablas en las que el contenido es incomprensible** cuando se lee de forma secuencial.
- Falta de independencia de dispositivo, la **web** debe ser **funcional** cuando no se utilice **ratón**.
- **Formatos no accesibles de documentos** que pueden dar **problemas a los lectores** de pantalla si no cumplen las normas de accesibilidad (por ejemplo en documentos pdf que no cumplen las normas).

### 2.2.2. Baja visión:

- **Tamaño de letra con medidas absolutas** que no permiten su cambio.
- **Maquetación desajustada** al modificar los tamaños de la fuente y que complican la navegabilidad.
- **Poco contraste** entre textos, fondos e imágenes.
- **Texto insertado mediante imágenes**.

### 2.2.3. Daltonismo:

- **Color para el resaltado** de los textos sin utilizar otro formato adicional como la cursiva, la negrita o el subrayado.
- **Poco contraste** entre textos, fondos e imágenes.

### 2.2.4. Auditivas: 

- **Falta de subtítulos o transcripciones** de los contenidos.
- **Obligatoriedad del uso de micrófono** sin posibilidad de desactivación.

### 2.2.5. Motrices:

- **Elementos** de interacción **muy pequeños**: botones, enlaces, etc.
- **Falta de independencia de dispositivo**, la web debe ser funcional cuando no se utilice ratón.

### 2.2.6. Neurológicas o cognitivas (dislexia, trastornos de atención, falta de memoria...):

- **Tamaño de letra fijo** que no se puede cambiar.
- **Elementos sonoros o visuales que no se pueden desactivar.**
- **Falta de estructuración y organización** del contenido que impide entenderlo correctamente.
- **Lenguaje muy enrevesado** y frases muy complejas.
- **Destellos o parpadeos** frecuentes que pueden provocar ataques de epilepsia.

    [**Víctimas de epilepsia televisiva:** "Más de 700 niños tienen que ser hospitalizados en Japón tras ver una serie de dibujos animados." Ver noticia en el Diario Información](https://elpais.com/diario/1997/12/18/ultima/882399601_850215.html)

    #### Qué es la epilepsia fotosensitiva

    **La epilepsia fotosensitiva es un problema causado por una respuesta anormal del cerebro a las luces intermitentes** (tipo flash). Se debe a que el mecanismo cerebral que controla la reacción a la información visual "es defectuosa o está ausente".

    **Además de las luces parpadeantes o relampagueantes rápidas**, especialmente si son rojas, los ataques **pueden ser causados, a veces, por ciertas formas y patrones geométricos**. La frecuencia del parpadeo de luz que provoca estos ataques varía de persona a persona.** Generalmente se da en frecuencias que oscilan entre los 5 y los 30 parpadeos por segundo (hertz)**. 

    [Ver más ejemplos sobre ataques fotosensibles](https://olgacarreras.blogspot.com/2007/11/como-evitar-causar-ataques.html)

> [Ver más desafíos y soluciones de diseño web accesible](http://accesibilidadweb.dlsi.ua.es/?menu=persona-discapacitada-web)

## 2.3. Ayudas técnicas y productos de apoyo

Gracias a la combinación de herramientas hardware y software, muchos usuarios disponen de herramientas para acceder de una manera eficaz a los contenidos de una web. Veamos algunos de los dispositivos utilizados.

### 2.3.1. Línea braille

En un periférico que dispone de unas celdas que permiten representar caracteres braille y ser leídos por personas ciegas mediante los dedos.

### 2.3.2. Lectores de pantalla

Son aplicaciones software que leen el texto de la pantalla en voz alta mediante un sintetizador de voz. También pueden enviar el texto a una línea braille para que el usuario lo lea con los dedos.

La aplicación software más famosa es JAWS y se maneja con las teclas del teclado. Estos son algunos de sus comandos:

- INSERT+FLECHA ABAJO: leer todo.
- ESC: detener la lectura.
- FLECHA IZQUIERDA: carácter anterior.
- TAB: se mueve al siguiente enlace.
- SHIFT+TAB: se mueve al enlace anterior.
- V: se mueve al siguiente enlace visitado, etc.

>[Ver cómo funcionan los lectores de pantalla JAWS y NVDA](https://rua.ua.es/dspace/bitstream/10045/55406/1/Lectores%20de%20pantalla%20JAWS%20y%20NVDA.pdf)

### 2.3.3. Licornio

Casco con varilla incorporada que permite utilizar un teclado tradicional mediante los movimientos de la cabeza.

### 2.3.4. Ratones especiales

Ratones especiales: ratones de cabeza, ratones de pie o apuntadores de boca, ratón de mirada, ratón de palanca, [ver todos los tipos de ratones](https://tecnoaccesible.net/content/ratones).

### 2.3.5. Navegadores de voz

Permiten, mediante un sintetizador de sonido de voz incorporado, leer en voz alta el contenido de la pantalla.

### 2.3.6. Webcams para seguimiento de ojos o cara

Transforman el movimiento de los ojos o la cara en movimientos del puntero del ratón en la pantalla simulando las pulsaciones del ratón con un parpadeo o con un gesto concreto de la cara. Estos dispositivos son adecuados para aquellas personas que tienen una discapacidad motriz severa de las extremidades y además tienen dificultad en el habla.

> [Ver más productos de apoyo y ayudas técnicas](http://accesibilidadweb.dlsi.ua.es/?menu=hardware)
