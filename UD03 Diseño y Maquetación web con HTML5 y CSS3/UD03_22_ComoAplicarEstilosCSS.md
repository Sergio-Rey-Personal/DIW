# **¿Cómo aplicar estilos CSS en un documento HTML?**

Tabla de contenidos

-   [2. Estilos CSS en un documento HTML](#2-Estilos-CSS-en-un-documento-HTML)
    -   [2.1. CSS en línea](#21-CSS-en-línea)
    -   [2.2. CSS incrustado en la cabecera](#22-CSS-incrustado-en-la-cabecera)
    -   [2.3. CSS en hojas de estilo externas](#23-CSS-en-hojas-de-estilo-externas)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

# 2. Estilos CSS en un documento HTML

Hay tres formas de aplicar estilos CSS en un documento HTML, veamos cada una de ellas:

# 2.1. CSS en línea

Los estilos en línea son declaraciones CSS que se integran en las etiquetas HTML mediante el atributo `style`. Este método tan solo afecta al elemento en el que se integra el código.

El CSS en línea es complicado de entender y mantener ya que mezcla los estilos CSS con el código HTML.

# 2.2. CSS incrustado en la cabecera

Otra manera muy simple de añadir estilo con CSS es utilizando la etiqueta `<style>` en la cabecera `<head>` del fichero HTML del sitio.

La desventaja de este método es que a la hora de realizar cualquier cambio, se debe realizar en múltiples páginas diferentes y el código estará repetido. Su uso puede llegar a ser necesario en el caso de utilizar un gestor de contenido que no permita modificar el archivo CSS directamente.

# 2.3. CSS en hojas de estilo externas

Mediante hojas de estilo externas se consigue separar el archivo de estilos del fichero HTML. El archivo de estilos cuenta con la extensión .css y se referencia desde HTML mediante el elemento `<link>`. Este es el método recomendado para aplicar estilos a una página web.

style.css
`p { color: red; }`

Este es el método más eficiente y más sencillo de mantener ya que el código CSS se encuentra separado del fichero HTML.

# Ejercicios propuestos
---------------------

A partir del proyecto web HTML creado en la primera parte de una unidad, realiza las siguientes actividades:

-   Añade una carpeta llamada "css" dentro de la carpeta "assets".
-   Enlaza en el documento index.html una hoja de estilo externa "style.css" y ubícala en la carpeta de "css".