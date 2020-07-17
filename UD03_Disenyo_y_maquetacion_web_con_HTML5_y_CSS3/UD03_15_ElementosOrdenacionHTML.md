# 15. **Elementos de ordenación**

Tabla de contenidos

- [15. **Elementos de ordenación**](#15-elementos-de-ordenación)
  - [15.1. Elementos en bloque o *block*](#151-elementos-en-bloque-o-block)
  - [15.2. Elementos en línea o *inline*](#152-elementos-en-línea-o-inline)
  - [15.3. Elementos flotantes o *float*](#153-elementos-flotantes-o-float)
  - [15.4. Posicionamiento absoluto y relativo](#154-posicionamiento-absoluto-y-relativo)

En el proceso de **maquetación de una web** es necesario organizar **elementos tales como imágenes, textos o tablas**. Tal y como vimos en el punto de la [**evolución de la web**](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD01_Disenyo_web_Caractaristicas_elementos_basicos_y_etapas_para_su_desarrollo/UD01_01_EdicionDelDisenyoWeb.md), en un primer momento los elementos de una página web se organizaban en tablas. En ese momento no había ni [**hojas de estilo CSS**](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD02%20Guia_de_estilo_web/UD02_01_QueEsUnaGuiaDeEstilos.md) ni ninguna otra herramienta que nos permitiera poner varios elementos seguidos uno detrás del otro.

En la actualidad, gracias a las **hojas de estilo** podemos crear nuestros propios estilos para maquetar cualquier página web. Para ello, necesitaremos conocer **cómo se ordenan los elementos en un documento web**.

## 15.1. Elementos en bloque o *block*

En un documento web lo más normal es ir posicionando los elementos de izquierda a derecha y de arriba a abajo dentro de la etiqueta `<body>`. En el caso de elementos en bloque o *block* como `<div>`, `<table>`, `<list>`, etc., estos **ocupan todo el ancho del contenedor o elemento padre**.

![elemento bloque html](img/elemento-bloque-html.png)

Figura 15.1. Elementos en bloque

## 15.2. Elementos en línea o *inline*

Los elementos en línea o *inline* como `<span>`, `<a>`, `<img>`, etc., **ocupan sólo el espacio delimitado por las etiquetas que definen el elemento en línea.**

![elemento en linea html](img/elemento-en-linea-html.png)

Figura 15.2. Elementos en línea

## 15.3. Elementos flotantes o *float*

El comportamiento de los elementos se puede modificar haciendo que floten. Cuando a un elemento html se le aplica un estilo con la propiedad de flotar o *float*, el **elemento sale del flujo normal y aparece posicionado a la izquierda o a la derecha de su contenedor**, donde el resto de elementos de la página se posicionarán alrededor. Las propiedades de los elementos flotantes se verán a fondo en la siguiente unidad.

## 15.4. Posicionamiento absoluto y relativo

Los elementos pueden estar posicionados de forma absoluta o relativa.

-   **Posicionamiento absoluto**: el elemento siempre se encuentra en el mismo lugar.
-   **Posicionamiento relativo**: el elemento se posiciona según otros elementos.