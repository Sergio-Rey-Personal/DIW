# 4. **Etiquetas para la creación de formularios HTML**


Tabla de contenidos

- [4. **Etiquetas para la creación de formularios HTML**](#4-etiquetas-para-la-creación-de-formularios-html)
  - [4.1. Etiquetas para la creación de formularios](#41-etiquetas-para-la-creación-de-formularios)
  - [4.2. Tipos de inputs](#42-tipos-de-inputs)
  - [4.3. Atributos para la validación de campos en los formularios](#43-atributos-para-la-validación-de-campos-en-los-formularios)
    - [4.3.1. Atributo *Pattern*](#431-atributo-pattern)
- [Ejercicios propuestos](#ejercicios-propuestos)

Los formularios son el soporte en el que se integran los botones y las áreas de texto que se utilizan para que los usuarios introduzcan sus datos o que puedan elegir entre varias opciones. En este apartado veremos las etiquetas que se utilizan para la **creación de formularios en *HTML5*.**

## 4.1. Etiquetas para la creación de formularios

El principio y final de un formulario se define con las etiquetas `<form>` y `</form>`. La etiqueta `<form>` puede incluir diferentes campos que son enviados para ser procesados por el servidor web. *HTML5* dispone de un gran número de campos como puedes ver en la siguiente tabla.


| Elemento | Descripción |
| --- | --- |
| `<form>` | Define un formulario. |
| `<fieldset>` | Permite organizar en grupos los campos de un formulario. |
| `<legend>` | Representa el título de un `<fieldset>`. |
| `<label>` | Representa el título de un elemento de control de un formulario. |
| `<input>` | Se usa para crear controles interactivos que reciben datos del usuario. [Ver atributos](https://developer.mozilla.org/es/docs/Web/HTML/Elemento/input) |
| `<button>` | Representa un botón. |
| `<option>` | Representa una opción en un elemento `<select>` o `<datalist>`. |
| `<select>` | Representa un elemento de control que permite la selección entre un conjunto de opciones `<option>`. |
| `<optgroup>` | Representa un conjunto de opciones, agrupadas lógicamente. |
| `<datalist>` | Representa un elemento de control que permite la selección entre un conjunto de opciones `<option>`. |
| `<textarea>` | Representa un elemento de control de edición de texto multi-línea. |
| `<output>` | Representa el resultado de un cálculo. |
Tabla 4.1: Etiquetas para la creación de formularios

[Ver atributos para formularios](https://developer.mozilla.org/es/docs/Web/HTML/Elemento/form)

**Ejemplo**

```html
<!DOCTYPE html>
<html lang="es">  
  <head>    
    <title>Ejemplos Etiquetas de texto</title>      
  </head>  
    <body>  
       <form>

       <fieldset>
          <legend>Datos personales</legend>
        
          <label>Nombre: </label><input name='nombre' type='text'/><br>
          <label>Apellidos: </label><input name='apellidos' type='text'/><br><br>
         
          <label>Sexo: </label>
          <select name="select">
            <option value="value1">Hombre</option> 
            <option value="value2" selected>Mujer</option>
          </select><br><br>
         
          <label>Edad</label>
          <input type='checkbox' name='edad' value='20-39' /> 20-39
          <input type='checkbox' name='edad' value='40-59' /> 40-59
          <input type='checkbox' name='edad' value='60-79' /> 60-79<br><br>
         
          <label>Email: </label><input name='nombre' type='email'/><br><br>
         <label>Estudios: </label>
         <select id="dino-select">
              <optgroup label="Estudios Universitarios">
                  <option>Doctorado</option>
                  <option>Máster</option>
                  <option>Grado</option>
              </optgroup>
              <optgroup label="Ciclo Formativo">
                  <option>Grado Superior</option>
                  <option>Grado Medio</option>
              </optgroup>
          </select>
       </fieldset>
         
       <fieldset>
             <legend>Escribe un mensaje</legend>
             <textarea name="textarea" rows="10" cols="50">Escribe aquí tu mensaje</textarea>
       </fieldset>  
        <input type="submit" value="Enviar" />
      </form><br><br>
      <form oninput="result.value=parseInt(a.value)+parseInt(b.value)">
        <input type="range" name="b" value="50" /> +
        <input type="number" name="a" value="10" /> =
        <output name="result">60</output>
      </form>
      <button name="boton">Ir a inicio</button>
    </body>  
</html>
```
[HTML Etiquetas formularios. (Codepen)](https://codepen.io/sergio-rey-personal/pen/MWKjZEd)

4.2. Tipos de inputs
--------------------

Algunos de los inputs más utilizados son los siguientes:

-   `<input type="button">`
-   `<input type="checkbox">`
-   `<input type="color">`
-   `<input type="date">`
-   `<input type="email">`
-   `<input type="file">`
-   `<input type="image">`
-   `<input type="month">`
-   `<input type="number">`
-   `<input type="password">`
-   `<input type="radio">`
-   `<input type="range">`
-   `<input type="search">`
-   `<input type="submit">`
-   `<input type="tel">`
-   `<input type="text">`
-   `<input type="time">`
-   `<input type="url">`
-   `<input type="week">`

[Ver ejemplos de los tipos de inputs](https://www.w3schools.com/html/html_form_input_types.asp)

4.3. Atributos para la validación de campos en los formularios
--------------------------------------------------------------

La validación de los datos introducidos por los usuarios en los campos de los formularios es esencial para ofrecer al usuario información sobre el tipo de datos que se están solicitando. Gracias a los nuevos atributos que se introdujeron en *HTML5* no es necesario utilizar *Javascript* ya que se validan de forma automática al pulsar en el botón de tipo *submit*. En la siguiente tabla se destacan los atributos más utilizados en los campos de los formularios.

Tabla 4.2: Atributos para la validación de campos en los formularios
| Atributo | Ejemplo |
| --- | --- |
| placeholder | placeholder="Indica tu nombre" |
| required | required="true" |
| pattern | pattern="[a-z]{1,5}" |
| min | min="1" |
| max | max="100" |
| step | step="2" (saltos en un rango de números: 0, 2, 4...) |
| disabled | disabled="true" |
| autofocus | autofocus="true" |
| autocomplete | autocomplete="true" |

### 4.3.1. Atributo *Pattern*

El atributo pattern se utiliza en los inputs y nos permite definir nuestras propias reglas para validar el valor de entrada usando [*RegExp*](https://www.w3schools.com/jsref/jsref_obj_regexp.asp).

Por ejemplo, vamos a definir una reglar usando el atributo *pattern*. En este caso, queremos que el nombre de usuario consista solo de letras minúsculas. Además, la longitud del nombre de usuario no debe ser mayor de 20 caracteres.

En *RegExp*, está regla puede ser expresada como ***pattern="[a-z]{1,15}"**.*

En la siguiente página web se pueden comprobar las Expresiones Regulares: [regexr.com](https://regexr.com/)

# Ejercicios propuestos

Crea un formulario de contacto que solicite los siguientes datos:

-   Nombre (30 caracteres como máximo y sólo permita letras y números).
-   Email.
-   Edad (entre 18 y 99 años).
-   Teléfono.
-   Campo de consulta.
-   Checkbox de aceptación de política de privacidad y cookies.

Además, todos los campos deben ser obligatorios, el foco debes ponerlo en el campo nombre y todos los inputs deben tener placeholder.

Incluye también una sección con los datos de contacto y el número de teléfono (con enlace funcional).

Escribe el formulario en un archivo contacto.html y enlázalo desde el menú principal.