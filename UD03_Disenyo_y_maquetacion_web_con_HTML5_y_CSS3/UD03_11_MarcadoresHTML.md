# **Marcadores en HTML. Enlaces locales para movernos fácilmente en una página**

Tabla de contenidos

-   [11. Marcadores en HTML](#11-Marcadores_en-HTML)
    -   [11.1. HTML <a> atributo target ](#111_HTML-ltaatributo-target)
-   [Ejercicios propuestos](#Ejercicios-propuestos)

# 11. Marcadores en HTML
-----------------------

Al crear una página web muy larga y con muchos apartados, es útil crear ciertos enlaces que nos permitan saltar directamente a la parte de la página que nos interesa. Este tipo de hipervínculos se llaman marcadores o enlaces locales.

Además, puede ser especialmente útil utilizar marcadores cuando al principio de una página colocamos una especie de índice y queremos que se pueda acceder a los distintos capítulos desde ahí mismo.

La estructura de los marcadores es básicamente la misma que al crear un [hiperenlace o hipervínculo a otra página](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_03_EtiquetasHTMLDeContenidoyTexto.md). Lo primero que hay que hacer es definir con un nombre cada parte de la página a la que queremos enlazar.

```html
<a name="nombre_marcador">Título</a>
```

Esta etiqueta puede contener en su interior un texto, una imagen o incluso podemos dejarla en blanco.

La etiqueta para crear un enlace a esa sección de la página es la siguiente:

```html
<a href="#nombre_marcador">Ir al título</a>
```

#### Ejemplo
```html
<html>
<head>
   <meta charset="utf-8"> 
   <title>Marcadores</title>  
</head>
<body>  
    <a href="#nombre_marcador1">Titulo 1</a> | 
    <a href="#nombre_marcador2">Titulo 2</a> | 
    <a href="#nombre_marcador3">Titulo 3</a> | 
    <a href="#nombre_marcador3">Titulo 4</a>

    <a name="nombre_marcador"></a>
    <h3>Marcadores en HTML</h3>
  
    <a name="nombre_marcador1"></a>
    <h4>Titulo 1</h4>
    <p>	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. </p>
  <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae.</p>
  
    <a name="nombre_marcador2"></a>
    <h4>Titulo 2</h4>
    <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae.</p>
  
    <a name="nombre_marcador3"></a>
    <h4>Titulo 3</h4>
    <p>	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. </p>
  <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae.</p>
  
  <a name="nombre_marcador4"></a>
  <h4>Titulo 4</h4>
    <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae.</p>
  <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. 	Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam amet inventore nesciunt ea architecto distinctio, officiis provident error tempora suscipit iure fugit libero aspernatur vitae assumenda. Repellat officiis ex vitae.</p>
  
<a href="#nombre_marcador">Ir arriba</a>
</body>
</html>
```

[Marcadores HTML (Codepen)](https://codepen.io/sergio-rey-personal/pen/yLeaZZg)

### 11.1. HTML `<a>` atributo target 

Ya que hemos profundizado un poco más en los enlaces y dado que ya hemos visto qué son los *[frames o framesets](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_14_MarcosFramesHTML.md)*, vamos a recordar el atributo *target* y sus diferentes valores.

```html
<a target=" _blank | _self | _parent | _top | *framename* ">
```

| Value | Description |
| ------|-------------|
| **_blank** | Abre la página en otra ventana. |
| **_self** | Abre el documento en el mismo frame. |
| **_parent** | Abre el documento en el frame padre. |
| **_top** | Abre el documento en el cuerpo de la página. |
| **framename** | Abre el documento en un frame concreto (se especifica su nombre). |

# Ejercicios propuestos

- Crea enlaces locales en el *aside* de tu blog para mostrar todas las entradas. Incluye 4 entradas y rellena el contenido con *Lorem ipsum*.

- Cuando el usuario se desplaza por tu página web, la acción puede ser diseñada para desencadenar una variedad de opciones de animación. En el caso de los marcadores, quedaría más adecuado un efecto de animación del recorrido desde una parte de la página hacia la otra. ¿Cómo se te ocurre que puede implementarse esa animación?