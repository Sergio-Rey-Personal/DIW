# 24. **Unidades de medida en CSS**

Tabla de contenidos

- [24. **Unidades de medida en CSS**](#24-unidades-de-medida-en-css)
  - [24.1. Utilización de píxeles](#241-utilización-de-píxeles)
  - [24.2. Utilización de ems](#242-utilización-de-ems)
  - [24.3. Convertidor Pixel a Ems](#243-convertidor-pixel-a-ems)

Los valores de las propiedades se pueden expresar en **longitudes absolutas y longitudes relativas.** Veamos las diferentes opciones en la siguiente tabla.

| | Longitudes relativas |
| --- | --- |
| `px` | Píxeles (relativo al dispositivo) |
| `em` | Relativo al tamaño de la fuente del elemento ( 2em significa 2 veces el tamaño de la fuente actual) |
| `%` | Porcentaje (relativo al elemento padre) |
| `vh y vw` | Medidas relativas de acuerdo al viewport: *1vh = 1% de la altura del viewport* y *100vh = altura del viewport* |

| | Longitudes absolutas |
| --- | --- |
| `in` | Pulgadas (1pulgada = 2.54 cm) |
| `cm` | Centímetros |
| `mm` | Milímetros |
| `pt` | Puntos (1pt = 1/72 pulgadas) |
| `pc` | Picas (1pica = 12 puntos) |

> Normalmente es recomendable usar unidades relativas en la medida de lo posible, ya que mejora la accesibilidad de la página web y permite que los documentos se adapten fácilmente a cualquier medio. En concreto, el organismo W3C, recomienda el uso de la unidad `em` para indicar el tamaño del texto.

## 24.1. Utilización de píxeles

El único inconveniente que puede darnos trabajar con píxeles es que no todas las pantallas son iguales y que un píxel no es igual en todas las pantallas. Este inconveniente se soluciona fácilmente siempre que se pueda redimensionar el texto en la pantallas.

## 24.2. Utilización de ems

El tamaño de los ems se establece en base al tamaño que tenga definido el navegador. El único problema es que el usuario haya modificado ese tamaño base, aunque los navegadores permiten ajustar estos parámetros nuevamente.

## 24.3. Convertidor Pixel a Ems

Normalmente el tamaño de una fuente por defecto en los navegadores es de 16px ( 16px = 1em). Por lo que tendríamos la siguiente conversión:

| px | em | % |
| -- | -- | -: |
| 12 | 0,7500 | 75 |
| 14 | 0,8750 | 87,50 |
| 16 | 1,0000 | 100,00 |
| 18 | 1,1250 | 112,50 |
| 20 | 1,2500 | 125 |

Puedes ver la conversión de pixel a ems en el [siguiente enlace](https://www.w3schools.com/tags/ref_pxtoemconversion.asp).

En las próximas secciones veremos con detalle las medidas de las propiedades más utilizadas.