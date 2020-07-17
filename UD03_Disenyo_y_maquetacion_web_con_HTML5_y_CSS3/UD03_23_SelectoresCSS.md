# 23. **Tipos de selectores en CSS**

Tabla de contenidos

- [23. **Tipos de selectores en CSS**](#23-tipos-de-selectores-en-css)
  - [23.1. Selector universal](#231-selector-universal)
  - [23.2. Selector etiqueta](#232-selector-etiqueta)
  - [23.3. Selector clase](#233-selector-clase)
  - [23.4. Selector identificador](#234-selector-identificador)
  - [23.5. Selector descendiente](#235-selector-descendiente)
  - [23.6. Combinación de selectores](#236-combinación-de-selectores)
  - [23.7. Selector de hijos](#237-selector-de-hijos)
  - [23.8. Selector adyacente](#238-selector-adyacente)
- [Ejercicios propuestos](#ejercicios-propuestos)

Veamos ahora cuáles son los selectores básicos que podemos utilizar en CSS.

## 23.1. Selector universal

**Sintaxis:** * { atributo:valor; }

**Ejemplo:**`* { color: grey; }`/* El estilo se aplicará a todos los elementos de la página*/

## 23.2. Selector etiqueta

**Sintaxis:** etiqueta { atributo:valor }

**Ejemplo:** `p {color: green;} ` /* El estilo se aplicará a todos los elementos <p>.*/

## 23.3. Selector clase

**Sintaxis:** .clase { atributo:valor }

**Ejemplo:** `.index {color: red;}` /* El estilo se aplicará a cualquier elemento que tenga la clase .index*/

## 23.4. Selector identificador

El **selector identificador** utiliza el atributo id para seleccionar un elemento. Solo puede haber un elemento con un id dado en un documento.

**Sintaxis:** #id { atributo:valor }

**Ejemplo:** `#cent {color: blue;}` /* El estilo se aplicará al elemento que tenga el id #cent */

## 23.5. Selector descendiente

Un elemento es descendiente de otro cuando se encuentra entre las etiquetas de apertura y de cierre del elemento padre. Su sintaxis es: selector1 selector2... slectorN. Siendo el selector N el elemento sobre el que se aplica el estilo.

```html
selector1 selector2 selectorN{
    propiedad: valor;
}
```

## 23.6. Combinación de selectores

La combinación de selectores nos permite dar un estilo a todos los selectores indicados.

```html
selector1, selector2, selector3{
    propiedad: valor;
}
```

## 23.7. Selector de hijos

Se usa para seleccionar un elemento que es *hijo* de otro elemento y se indica mediante el signo "mayor que" (`>`).

```
selector1 > selector2{
    propiedad: valor;
}
```

## 23.8. Selector adyacente

Se usa para seleccionar elementos que son *hermanos*, es decir, su elemento padre es el mismo y están seguidos en el código HTML. Se indica mediante el signo "más" (`+`).

```
selector1 + selector2{
    propiedad: valor;
}
```

[Ver lista completa de selectores](https://www.w3schools.com/cssref/css_selectors.asp)

* * * * *

**Ejemplos**

```css
/*style.css*/
p { background-color: grey; } /* Selector etiqueta */
.clase { color: red; } /* Selector clase */
#ident { color: green; } /* Selector identificador */
* { font-style: italic; } /* Selector universal */
p a{
  background-color: orange;
}
```
```html
<html>
<head>
    <meta charset="utf-8"> 
    <title>Selectores</title> 
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <h1 class="clase">Texto de color rojo</h1>
    <p id="ident">Texto de color verde</p>
  <h2>Selector descendiente</h2>
  <p>
      <a href="#">Enlace</a><br>
      <span>
            <a href="#">Enlace</a>
      </span>
  </p>
  
</body> 
</html>
```

# Ejercicios propuestos

Utiliza el selector universal para asegurarte de que todo elemento tenga un margen interno y externo de 0 píxeles. De esta forma proveerás de consistencia al diseño.