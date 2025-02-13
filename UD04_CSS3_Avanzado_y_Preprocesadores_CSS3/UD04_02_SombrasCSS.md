# 2. **Sombras CSS en texto y contenedores o cajas**

Tabla de contenidos

- [2. **Sombras CSS en texto y contenedores o cajas**](#2-sombras-css-en-texto-y-contenedores-o-cajas)
  - [2.1. Propiedades text-shadow y box-shadow](#21-propiedades-text-shadow-y-box-shadow)
      - [Ejemplo](#ejemplo)
  - [2.2. Generadores de sombra online](#22-generadores-de-sombra-online)
- [Ejercicios propuestos](#ejercicios-propuestos)

Gracias a las propiedades de CSS3 "**text-shado**w" y "**box-shadow**" podemos aplicar sombras en los textos y en los contenedores y así enriquecer nuestras interfaces.

## 2.1. Propiedades text-shadow y box-shadow

El formato es el mismo para las dos propiedades. Veamos por ejemplo qué significan los valores de la propiedad "text-shadow" que tenemos a continuación:

text-shadow: 3px 4px 0px #fff;
box-shadow: 10px 10px 14px 2px rgba(0,0,0,0.47);

-   3px: es el tamaño de la sombra que se aplica a la derecha del texto.
-   4px: es la sombra que se proyecta hacia abajo.
-   0px: es la cantidad de sombra borrosa que se aplica.
-   #fff: es el color de la sombra. Se puede aplicar también en RGBA y HSLA.

Para aplicar sombras arriba y a la izquierda se deben utilizar valores negativos.

Parta aplicar doble sombra se pueden poner dos valores separados con coma:

text-shadow: 3px 4px 0px #fff, 2px 2px 1px #ccc;

Recuerda que para este tipo de propiedades debemos incluir los [prefijos para navegadores](https://github.com/Sergio-Rey-Personal/DIW/blob/master/UD03_Disenyo_y_maquetacion_web_con_HTML5_y_CSS3/UD03_31_PrefijosNavegadoresCSS.md) correspondientes.

#### Ejemplo
```css
.shadow {
    padding: 20px;
    margin: 20px;
    text-shadow: 3px 3px 2px rgba(152, 150, 207, 0.7);
    -webkit-box-shadow: 10px 10px 14px 2px rgba(0,0,0,0.47);
    -moz-box-shadow: 10px 10px 14px 2px rgba(0,0,0,0.47);
    box-shadow: 10px 10px 14px 2px rgba(0,0,0,0.47);
  }
```

```html
<h1 class="shadow">Text & box shadow</h1>
```

[Text-shadow & box-shadow (Codepen)](https://codepen.io/sergio-rey-personal/pen/dyGRqVQ)

## 2.2. Generadores de sombra online

Para facilitarnos la tarea de la creación de sombras podemos utilizar un generador de sombras tanto para los textos como para las cajas o contenedores. Algunas herramientas online útiles son las siguientes:

**Generador de sombras en textos:** <https://css3gen.com/text-shadow/>

**Generador de sombras en cajas o contenedores:** <https://www.cssmatic.com/box-shadow>

# Ejercicios propuestos

Define una sombra inferior en el menú de tu proyecto web. Puedes elegir aplicar la sombra en otro lugar de tu sitio.