# 6. Niveles de prioridad  y puntos de verificación 

Tabla de contenidos

- [6. Niveles de prioridad  y puntos de verificación](#6-niveles-de-prioridad-y-puntos-de-verificación)
  - [6.1. Niveles de prioridad](#61-niveles-de-prioridad)
  - [6.2. Logos de conformidad](#62-logos-de-conformidad)
  - [6.3. Cómo usar los logos](#63-cómo-usar-los-logos)
    - [6.3.1. Nivel A de Conformidad](#631-nivel-a-de-conformidad)
    - [6.3.3. Nivel Doble-A de Conformidad](#633-nivel-doble-a-de-conformidad)
    - [6.3.3. Nivel Triple-A de Conformidad](#633-nivel-triple-a-de-conformidad)
  - [6.4. Alcance de la declaración](#64-alcance-de-la-declaración)
  - [6.5. Responsabilidad en cuanto a la exactitud de las declaraciones](#65-responsabilidad-en-cuanto-a-la-exactitud-de-las-declaraciones)


## 6.1. Niveles de prioridad

La **WCAG** ofrece varios **niveles de prioridades** a la hora de aplicar las pautas de accesibilidad. De esta forma podemos saber cuáles son las acciones más importantes que debemos realizar. Son tres niveles de prioridades:

-   **Prioridad 1:** Nivel mínimo exigible y requisito esencial que se debe satisfacer. De otra forma, uno o más grupos de usuarios encontrarán imposible acceder a la información. 
-   **Prioridad 2:** Satisfacer este punto de verificación eliminará importantes barreras de acceso a la información Web.
-   **Prioridad 3:** Satisfacer este punto de verificación mejorará la accesibilidad a la información web a usuarios que tengan dificultades para utilizar la interfaz.

Si se cumplen los niveles de prioridades se establecen varios niveles de conformidad que sirven de sello de accesibilidad.

-   **Nivel A** de Conformidad: Se han satisfecho todos los puntos de verificación de Prioridad 1.
-   **Nivel AA** de Conformidad: Se han satisfecho todos los puntos de verificación de Prioridad 1 y 2.
-   **Nivel AAA:** de Conformidad: Se han satisfecho todos los puntos de verificación de Prioridad 1, 2 y 3.

## 6.2. Logos de conformidad 

| nivel A | Doble-A | Triple-A |
| --- | --- | --- |
| ![Icono del  Nivel A de conformidad con las Directrices de Accesibilidad para el Contenido Web 2.1 del W3C-WAI](https://www.w3.org/WAI/wcag21/wcag2.1A-v.png) | ![Icono del Nivel Doble-A de conformidad con las Directrices de Accesibilidad para el Contenido Web 2.1. del W3C-WAI](https://www.w3.org/WAI/wcag21/wcag2.1AA-v.png) | ![Icono del Nivel Triple-A de conformidad con las Directrices de Accesibilidad para el Contenido Web 2.1 del W3C-WAI](https://www.w3.org/WAI/wcag21/wcag2.1AAA-v.png) |

## 6.3. Cómo usar los logos

Para la inclusión de los logotipos de conformidad, una vez decidida la conformidad que alcanza nuestra web se especifica de la forma siguiente según se indica en la publicacion de la W3C [Adding WCAG Conformance Logos](https://www.w3.org/WAI/standards-guidelines/wcag/conformance-logos/)


### 6.3.1. Nivel A de Conformidad

Poner en la página web el siguiente código HTML:

```html
<a href="https://www.w3.org/WAI/WCAG2A-Conformance"
   title="Explanation of WCAG 2 Level A Conformance">
  <img height="32" width="88"
       src=" https://www.w3.org/WAI/WCAG21/wcag2.1A-v"
       alt="Level A conformance,
            W3C WAI Web Content Accessibility Guidelines 2.1">
</a>

```
Si se quiere utilizar la insignia azul, añadir "-blue" al src de la imagen. De la misma forma estan disponible los logitipos para la version 2.0 y 1.0.

### 6.3.3. Nivel Doble-A de Conformidad

Poner en la página web el siguiente código HTML:

```html
<a href="https://www.w3.org/WAI/WCAG2AA-Conformance"
   title="Explanation of WCAG 2 Level AA conformance">
  <img height="32" width="88"
       src=" https://www.w3.org/WAI/WCAG21/wcag2.1AA-v"
       alt="Level AA conformance,
            W3C WAI Web Content Accessibility Guidelines 2.1">
</a>

```

Si se quiere utilizar la insignia azul, añadir "-blue" al src de la imagen.De la misma forma estan disponible los logitipos para la version 2.0 y 1.0.

### 6.3.3. Nivel Triple-A de Conformidad

Poner en la página web el siguiente código HTML:

```html
<a href="https://www.w3.org/WAI/WCAG2AAA-Conformance"
   title="Explanation of WCAG 2 Level AAA conformance">
  <img height="32" width="88"
       src=" https://www.w3.org/WAI/WCAG21/wcag2.1AA-v"
       alt="Level AAA conformance,
            W3C WAI Web Content Accessibility Guidelines 2.1">
</a>

```
Si se quiere utilizar la insignia azul, añadir "-blue" al src de la imagen.De la misma forma estan disponible los logitipos para la version 2.0 y 1.0.

## 6.4. Alcance de la declaración

Por omisión, un icono de conformidad se refiere a una única página. Si la declaración pretende aplicarse o incluir más de una página, el icono de conformidad debe ir acompañado de información explícita del alcance, explicando qué páginas cubre la declaración.

## 6.5. Responsabilidad en cuanto a la exactitud de las declaraciones

Los proveedores de contenidos son los únicos responsables del uso de estos logos. Se recomienda que el proveedor de Contenidos se familiarice con las [Directrices de Accesibilidad para el Contenido Web 2.1](https://www.w3.org/WAI/standards-guidelines/wcag/es), antes de utilizar estos logos como parte de una declaración de conformidad y que, utilicen varios métodos de revisión para garantizar que cualquier página en la que se usen realmente alcanza el nivel de conformidad declarado. Los proveedores deben también asegurarse de que cualquiera que mantenga o actualice el sitio está familiarizado con el uso de los logos, y de que nadie repasa la página o elimina el logo de la página si no está seguro de que sigue alcanzando el nivel de conformidad especificado.

Hay  que tener en cuenta que el uso de este logo no depende de una revisión automática. No existe aún ninguna herramienta que pueda hacer una revisión completa de todos los puntos de verificación que hay en las directrices, y una revisión automática completa en el futuro puede seguir siendo difícil o imposible. Por ejemplo, algunos puntos de verificación se basan en una interpretación de qué información es "importante" o en si el texto equivalente para un elemento no textual es exacto.

También es posible que un revisor de la accesibilidad automático presente "falsos negativos" o "falsos positivos" debido al tipo de marcado en una página. Por estas razones, los logos de esta página se usan sólo para indicar una declaración de conformidad hecha por el autor de la página, no una conformidad conseguida mediante un validador automático.