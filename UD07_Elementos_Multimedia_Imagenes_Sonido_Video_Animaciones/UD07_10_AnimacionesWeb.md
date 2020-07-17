# 10. **Introducción a las animaciones Web**

Tabla de contenidos

- [10. **Introducción a las animaciones Web**](#10-introducción-a-las-animaciones-web)

*Según la definición de la wikipedia: animación es un proceso utilizado para dar la sensación de movimiento a imágenes o dibujos. Los cuadros se pueden generar dibujando, pintando o fotografiando los minúsculos cambios hechos repetidamente a un modelo de la realidad o a un modelo tridimensional virtual.*

Tenemos varias formas de añadir animaciones en una web:

-   Usando diferentes **formatos** de **archivos** que permiten animar imágenes como GIF, SVG o SWF

-   Utilizar las nuevas características de **CSS3**
-   Usar lenguajes de programación dinámicos como **javascript.**

Ciñéndose a la definición anterior, solo se consideraría animación propiamente dicha a la primera de las opciones, las otras dos podrían ser consideradas parte de la interacción, no obstante aquí trataremos sobre todo la segunda parte ya que con las nuevas propiedades de las hojas de estilo es posible hacer multitud de efectos que no tienen que ver sólo con la interacción.

En cualquier **animación hay dos conceptos** clave: los **fotogramas** y las **capas.**

Un **fotograma** es una imagen estática, no obstante un conjunto de fotogramas visualizados secuencialmente a cierta velocidad provoca la sensación de movimiento. Existen varios tipos de fotogramas:

-   Fotograma clave. Representa un cambio en la escena con respecto al fotograma anterior
-   Fotograma de fin de secuencia. Es el último fotograma de una secuencia de fotogramas iguales.
-   Fotograma intermedio. Puede estar formado por una interpolación de forma o de movimiento o por una secuencia de fotogramas blancos o iguales.

Por su parte una capa añade un elemento virtual que permite que los objetos gráficos no interfieran entre sí. Es como si añadiéramos una fina lámina transparente. 

Una vez realizada una animación con un programa adecuado podemos añadirle audio o vídeo. En el caso de añadir audio debemos cargar el mismo en nuestro programa y añadirlo a la escena intentando sincronizarlo con la animación. Para el vídeo debemos incorporarlo igualmente, esta vez no hace falta sincronización.

En cuento a las animaciones derivadas de las propiedades CSS4, en la unidad 4, ya hemos [transformaciones](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD04_CSS3_Avanzado_y_Preprocesadores_CSS3/UD04_06_TransformacionesCSS.md) y [transiciones](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD04_CSS3_Avanzado_y_Preprocesadores_CSS3/UD04_05_TransicionesCSS.md), y a continuación veremos animaciones. 