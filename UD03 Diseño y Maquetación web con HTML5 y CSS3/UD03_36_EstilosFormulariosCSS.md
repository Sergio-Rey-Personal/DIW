# **Estilos en formularios CSS, propiedades necesarias**

Tabla de contenidos

- [16. Estilos CSS en formularios](#16-Estilos-CSS-en-formularios)
  - [1. Formulario básico en CSS](#1-Formulario-básico-en-CSS)
  - [2. Propiedad box-sizing](#2-Propiedad-box-sizing)
  - [3. Propiedad resize](#3-Propiedad-resize)
- [Ejercicios propuestos](#Ejercicios-propuestos)

En el tema anterior vimos las [etiquetas HTML para la creación de formularios](https://www.eniun.com/etiquetas-formularios-html5/). Vamos a ver ahora cómo podemos dar estilo a esas etiquetas mediante CSS.

# 16. Estilos CSS en formularios

Gracias a los estilos podemos romper el diseño gris con líneas negras de los formularios y convertirlos en una parte más que se integra perfectamente en nuestro diseño web.

Como sabemos, a la hora de crear nuestros formularios, seguiremos [buenas prácticas CSS](https://www.eniun.com/buenas-practicas-css-codigo/), no crearemos clases extra y utilizaremos, en la medida de lo posible, [selectores descendientes](https://www.eniun.com/selectores-css-tipos/#35_Selector_descendiente) y etiquetas predefinidas.

A las etiquetas de los formularios se les puede dar estilo CSS al igual que al resto de elementos de nuestro documento. Sin embargo, debemos conocer una serie de propiedades que nos ayuden a elaborar nuestros diseños de la forma más óptima posible.

## 1. Formulario básico en CSS

En el siguiente ejemplo puedes ver un formulario básico en CSS que permite ser visualizado en cualquier dispositivo:

```css
@import url(https://fonts.googleapis.com/css?family=Roboto:400);
form{
  padding: 60px;
  max-width: 400px;
  background-color: #E7E7E7;
  margin: 0 auto;
}

form input, form textarea{
  margin-bottom: 15px;
  font-family: "Roboto", sans-serif;
  width: 100%;
  padding: 10px;
  -webkit-box-sizing: border-box;
  box-sizing: border-box; 
  border: none; 
  color: #525c66; 
  font-size: 1em;
  resize: horizontal; 
}

form button {
	display: block;
	background-color: #0095eb;
	padding: 10px 45px 10px 45px;
	border: 0;
	font-size: 1em; 
	color: 	white;
  font-family: "Roboto", sans-serif;
}
form button: hover{
	background-color: #046193;
}
```

```html
<form action="formulario-contacto.php" method="post">	
				<input name="nombre" type="text" placeholder="Nombre" maxlength="30" pattern="[a-zA-Z0-9]+" required autofocus/>
				<input name="email" type="email" placeholder="Correo electrónico" required />	
				<textarea name="consulta" placeholder="¿Cuál es el motivo de tu consulta?" rows="6" required></textarea>
				<button id="enviar" name="enviar" type="submit" class="btn">ENVIAR</button>
</form>	
```

> [CSS3. Formulario básico (Codepen)](https://codepen.io/sergio-rey-personal/pen/KKVNQqK)

En este ejemplo se han utilizado muchas de las propiedades que hemos visto a lo largo del curso. Por ejemplo, se han quitado los bordes con la propiedad `"border:none"`, se le ha dado un padding a los inputs y textarea, y se han utilizado las propiedades "margin: 0 auto" para centrar el contenido y `"width: 100%"` para conseguir un diseño web responsive.

Vamos a ver ahora ciertas propiedades que aún no conocemos y que son de mucha utilidad en la creación de nuestros formularios.

## 2. Propiedad box-sizing

Por defecto en el [modelo de cajas de CSS](https://www.eniun.com/modelo-cajas-css-margenes-relleno-bordes/), el ancho y alto asignado a un elemento es aplicado solo al contenido de la caja del elemento. Si el elemento tiene algún borde (border) o relleno (padding), este es entonces añadido al ancho y alto del tamaño de la caja o contenedor. Esto significa que cuando se define el ancho y alto, se tiene que ajustar el valor para permitir cualquier borde o relleno que se pueda añadir.

La propiedad `box-sizing` puede ser usada para ajustar el siguiente comportamiento:

- `content-box` es el comportamiento CSS por defecto para el tamaño de la caja (box-sizing). Si se define el ancho de un elemento en 100 pixeles, la caja del contenido del elemento tendrá 100 pixeles de ancho, y el ancho de cualquier borde o relleno será añadido al ancho final desplegado.
- `border-box` toma en cuenta cualquier valor que se especifique de borde o de relleno para el ancho o alto de un elemento. Es decir, si se define un elemento con un ancho de 100 pixeles. Esos 100 pixeles incluirán cualquier borde o relleno que se añadan, y la caja de contenido se encogerá para absorber ese ancho extra. Esta propiedad es especialmente útil para redimensionar cualquier elemento.

Vamos a ver un ejemplo: en el caso de los inputs, normalmente les añadimos un padding para darle algo de aire. Sin embargo, si después centramos el contenido y le dotamos de un `"width:100%"`, este ancho no tendrá en cuenta el padding añadido al input y el elemento no se encontrará perfectamente redimensionado. Realiza la prueba quitando y añadiendo la propiedad "box-sizing: border-box" en el código del formulario básico creado en el punto 1.

Como puedes ver en el código, se han añadido los [prefijos para navegadores](https://www.eniun.com/prefijos-css-navegadores-propiedades/) necesarios para esta nueva propiedad.

```css
-webkit-box-sizing: border-box;
box-sizing: border-box;
```

## 3. Propiedad resize

Por defecto, los elementos `<textarea>` permiten cambiar el tamaño por el usuario. Podemos anular este comportamiento utilizando la propiedad "resize:none".

```css
/* Valores de la propiedad resize */
resize: none;
resize: both;
resize: horizontal;
resize: vertical;
```

| **Valores** | **Descripción** |
| --- | --- |
| `none` | El usuario no puede cambiar el tamaño del elemento |
| `horizontal` | El usuario puede cambiar el tamaño del elemento horizontalmente |
| `vertical` | El usuario puede cambiar el tamaño del elemento verticalmente |
| `both` | El usuario puede cambiar el tamaño del elemento en horizontal y vertical |

# Ejercicios propuestos

-   Incorpora los estilos necesarios para maquetar el formulario de tu proyecto web teniendo en cuenta todos los elementos estudiados.