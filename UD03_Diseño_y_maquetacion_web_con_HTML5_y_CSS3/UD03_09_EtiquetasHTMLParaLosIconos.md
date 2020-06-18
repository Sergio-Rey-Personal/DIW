# Etiquetas HTML para los iconos de acceso directo en Android, iPhone y otras aplicaciones

Tabla de contenidos

-   [9.1. Etiquetas HTML para los iconos de acceso directo en Android, iPhone y otras aplicaciones](#91-Etiquetas-HTML-para-los-iconos-de-acceso-directo-en-Android-iPhone-y-otras-aplicaciones)
    -   [9.1.1. Pasos a seguir para incluir los iconos de acceso directo a tu web en Android, iPhone u otros.](#911-Pasos-a-seguir-para-incluir-los-iconos-de-acceso-directo-a-tu-web-en-Android-iPhone-u-otros)
-   [9.2. ¿Cómo añadir el acceso directo de mi web al escritorio de mi Smartphone mediante Google Chrome? ](#92-¿Cómo-añadir-el-acceso-directo-de-mi-web-al-escritorio-de-mi-Smartphone-mediante-Google-Chrome?)
-   [9.3. ¿Cómo añadir el acceso directo de mi web al escritorio de mi Smartphone mediante Firefox? ](#93-¿Cómo-añadir-el-acceso-directo-de-mi-web-al-escritorio-de-mi-Smartphone-mediante-Firefox?)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

# 9.1. Etiquetas HTML para los iconos de acceso directo en Android, iPhone y otras aplicaciones

Insertar el a**cceso directo** a las webs que más utilizamos es extremadamente útil tanto en el "**escritorio**" de nuestro **smartphone** o **tablet**, como en la página principal de nuestros **navegadores** favoritos. De esta forma en un solo click conseguimos estar en la web o aplicación que deseemos.

Para incluir estos **accesos directos o iconos identificativos** en las pantallas de los smartphones, tablets o navegadores podemos insertar **etiquetas** especiales en nuestro **código HTML**. Lo que conseguiremos mediante estas etiquetas es incluir los **iconos tipo App** de nuestra web en **diferentes resoluciones** para que sean visibles y con buena calidad.

## 9.1.1. Pasos a seguir para incluir los iconos de acceso directo a tu web en Android, iPhone u otros.

1.  Crea el icono de tu web tipo App de un tamaño grande para no perder calidad (ejemplo **1024x1024px**).
2.  Crea los **diferentes tamaños exigidos** para cada tipo de dispositivo. Mediante esta [aplicación online gratuita](https://makeappicon.com/) puedes subir la imagen creada en el punto 1 y te llega un correo electrónico con todas las imágenes preparadas en un archivo comprimido.
3.  Guarda los diferentes tamaños que necesites en una **carpeta organizada en tu espacio web**.
4.  Añade las **etiquetas necesarias en tu código html**.

Para empezar está bien con incluir las siguientes etiquetas `<link>` en el `<head>` de tu código HTML:

< link href="http://www.tuweb.com/img/apple-touch-icon.png" rel="apple-touch-icon" />
< link href="http://www.tuweb.com/img/icon-hires.png" rel="icon" sizes="192x192" />
< link href="http://www.tuweb.com/img/icon-normal.png" rel="icon" sizes="128x128" />

Puedes encontrar más información sobre las etiquetas y sus usos en los siguientes enlaces:

-   [Etiquetas Opengraph](https://ogp.me/)
-   [Etiquetas iOS](https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.htm)

**Ejemplo de código o etiquetas que solemos utilizar en nuestros proyectos:**

```html
<!DOCTYPE html>
<html lang="es">  
  <head>    
    <title>Metaetiquetas útiles</title>  
    <link rel="shortcut icon" href="https://www.eniun.com/wp-content/uploads/favicon.png" type="image/x-icon">
    <link rel="apple-touch-icon" href="https://www.eniun.com/wp-content/uploads/emiun-apple.png">
    <meta name="description" content="Eniun. Diseño y desarrollo de webs corporativas. Servicios de marketing digital y social media. ¡Haz despegar tu negocio con nosotros! Consúltanos">
    <link rel="canonical" href="https://www.eniun.com/">
    <meta property="og:locale" content="es_ES">
    <meta property="og:type" content="website">
    <meta property="og:title" content="Inicio - Eniun">
    <meta property="og:description" content="Eniun. Diseño y desarrollo de webs corporativas. Servicios de marketing digital y social media. ¡Haz despegar tu negocio con nosotros! Consúltanos">
    <meta property="og:url" content="https://www.eniun.com/">
    <meta property="og:site_name" content="Eniun">
    <meta property="og:image" content="https://www.eniun.com/wp-content/uploads/eniun-background-first-home.jpg">
    <meta property="og:image:secure_url" content="https://www.eniun.com/wp-content/uploads/eniun-background-first-home.jpg">
    <meta property="og:image:width" content="1913">
    <meta property="og:image:height" content="911">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:description" content="Eniun. Diseño y desarrollo de webs corporativas. Servicios de marketing digital y social media. ¡Haz despegar tu negocio con nosotros! Consúltanos">
    <meta name="twitter:title" content="Inicio - Eniun">
    <meta name="twitter:site" content="@eniun_es">
    <meta name="twitter:image" content="https://www.eniun.com/wp-content/uploads/eniun-background-first-home.jpg">
    <meta name="twitter:creator" content="@eniun_es">
  </head>  
  <body>    
    Etiquetas útiles
  </body>  
</html>
```

[Etiquetas útiles (Codepen)]https://codepen.io/sergio-rey-personal/pen/OJMRdmG)

# 9.2. ¿Cómo añadir el acceso directo de mi web al escritorio de mi Smartphone mediante Google Chrome? 

-   Abre Google Chrome y carga la página que quieres añadir como acceso directo en tu smartphone.
-   Pulsa sobre el menú, los tres puntos de la esquina superior derecha.
-   Elige "Añadir a pantalla de inicio" y tendrás el acceso directo a la web en tu escritorio principal.

# 9.3. ¿Cómo añadir el acceso directo de mi web al escritorio de mi Smartphone mediante Firefox? 

-   Abre Firefox y carga la página que quieres añadir como acceso directo en tu smartphone.
-   Ve al menú superior derecho, el de los tres puntos, y selecciona "Página".
-   Desciende hasta "Añadir acceso directo a página" y selecciona "aquí".

# Ejercicios propuestos

Incluye las etiquetas de acceso directo a tu web para Android e iOS.