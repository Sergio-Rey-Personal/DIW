## 5. Técnicas para satisfacer los requisitos definidos en las WCAG 

Tabla de contenidos

- [5. Técnicas para satisfacer los requisitos definidos en las WCAG](#5-técnicas-para-satisfacer-los-requisitos-definidos-en-las-wcag)
  - [5.1. Técnicas fundamentales](#51-técnicas-fundamentales)
  - [5.2. Técnicas HTML](#52-técnicas-html)
  - [5.3. Técnicas CSS](#53-técnicas-css)
  - [5.4. Javascript](#54-javascript)
  - [5.5. Técnicas para servidor](#55-técnicas-para-servidor)
  - [5.6. Técnicas WAI-ARIA](#56-técnicas-wai-aria)
  - [5.7. Otras técnicas](#57-otras-técnicas)
    - [Ejercicios](#ejercicios)
    - [Actividad 4.3](#actividad-43)
    - [Actividad 4.4](#actividad-44)


Las técnicas para satisfacer los requisitos definidos en las WCAG están recogidas en la siguiente web: <https://www.w3.org/WAI/GL/WCAG20-TECHS/>

Como puedes ver, hay más de 400 técnicas para satisfacer todos los requisitos definidos en las WCAG, a continuación se mencionan las más destacadas:

### 5.1. Técnicas fundamentales

- Incluir alternativas de texto al contenido multimedia.
- Permitir pausar el contenido multimedia.
- Incluir alternativas legibles cuando la lectura dependa del contraste de colores.
- Ordenación coherente del contenido.
- Incluir glosarios, mapa del sitio, tabla de contenidos.
- Incluir títulos descriptivos.
- Añadir enlaces para ir al principio de la página.
- Identificar la localización del usuario dentro de la web (breadcrumbs).
- Evitar parpadeos.
- Alinear los textos de manera similar.
- Ofrecer feedback de confirmación o negación al realizar una operación, etc.

### 5.2. Técnicas HTML

- Utilizar elemento title para dar un título coherente a la página.
- Incluir la etiqueta meta description.
- Incluir el botón de submit en los formularios.
- Definir el idioma correspondiente con el atributo lang.
- Incluir el atributo alt en las imágenes.
- Utilizar el atributo caption y summary en las tablas.
- Maquetación sin tablas.
- Utilizar los encabezados h1-h6.
- Crear un orden de tabulación coherente en formularios y enlaces.
- Utilizar [etiquetas estructurales o elementos semánticos](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_02_HTML5.md).

### 5.3. Técnicas CSS

- Facilitar mecanismos para que se pueda modificar la hoja de estilos CSS: colores, fuentes, etc.
- [Separar la estructura de los estilos y no utilizar estilos en línea](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_22_ComoAplicarEstilosCSS.md).
- Utilizar tamaño de letra con [medidas relativas: unidades em](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_24_UnidadesDeMedidaCSS.md).
- Incluir el foco en los elementos mediante la [clase :focus](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_37_ResumenCSS.md#pseudo-clases-para-los-estados-de-un-elemento).
- Utilizar CSS para presentar el texto, controlar el espaciado, etc.

### 5.4. Javascript

- Aumentar los tiempos de acción.
- Soporte para utilizar tanto ratón como teclado.
- Validación de datos con alertas.
- Usar el DOM para manipular la página.
- Utilizar scripts para modificar el aspecto de la página, como el fondo.
- Utilizar scripts para hacer scroll por la página y que se pueda controlar.

### 5.5. Técnicas para servidor

- Aplicar redirecciones en lado del servidor (.htaccess)  y no en el cliente.

### 5.6. Técnicas WAI-ARIA

Las técnicas **WAI-ARIA (Web Accessibility Initiative -- Accessible Rich Internet Applications)** proporcionan semántica, de tal forma que se pueden transmitir comportamientos de la interfaz de usuario e información estructural a las tecnologías de apoyo (por ejemplo, lectores de pantalla). La especificación de ARIA establece componentes que definen r**oles, estados y propiedades de los elementos de la interfaz de usuario.**

Algunas de las técnicas que se especifican consisten en utilizar los **atributos** que definen los componentes:

- **aria-label**: etiquetar objetos.
- **aria-describedly**: controles de la interfaz de usuario.
- **aria-required:** campos requeridos.
- **aria-role:** indicar el rol de un control y agrupar los controles de grupos.
- **state y property** para mostrar los estados de los componentes.
- **aria landmarks** para establecer las regiones de una página.

> [Ver ejemplos de ARIA en HTML](https://www.w3.org/TR/aria-in-html/)

> [Ver ejemplos atributo semántico "role"](https://www.ediciones-eni.com/open/mediabook.aspx?idR=82bf10a975d8defafd64bdcf2b089ea6)

### 5.7. Otras técnicas

Puedes ver más técnicas relacionadas con el uso de PDF, Flash, Silverlight, etc. en la web oficial: <https://www.w3.org/WAI/GL/WCAG20-TECHS/>

> [Ver guía breve y consejos de accesibilidad web](http://accesibilidadweb.dlsi.ua.es/?menu=guiabreve-1)

> [Ver más técnicas y ejemplos de accesibilidad](http://www.codexexempla.org/curso/curso_2_6.php)

#### Ejercicios

#### Actividad 4.3

Analiza la accesibilidad de tu sitio web mediante la herramienta [Cynthiasays](http://www.cynthiasays.com/). Explica los errores encontrados, su posible solución y adjunta capturas de pantalla, si fuese necesario.

#### Actividad 4.4

Como hemos visto, Bootstrap nos ayuda a que nuestros sitios web sean accesibles incluyendo en los ejemplos de código los elementos y atributos HTML recomendados para conseguir aplicaciones accesibles. Analiza la página web que creaste en la práctica de Bootstrap y encuentra los atributos WAI-ARIA utilizados. Fíjate, por ejemplo, en los atributos role y aria-hidden. Explica por qué se han utilizado esos atributos.