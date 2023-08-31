---
layout: page
title: Cálculos Ráster
parent: ArcGIS Pro Análisis Espaciales
nav_order: 2
---
# Operaciones, Funciones, y Estadísticas

<sup>Este material de enseñanza está basado en ArcGIS Pro 3.1.</sup>

En esta sección exploraremos las diferentes formas de trabajar con los valores numericos de los datos ráster. Estos datos, como cualquier otro tipo de dato, pueden ser procesados para hacer cálculos, aplicar funciones, y obtener estadísticas para hacer análisis espaciales más avanzados.

## Calculadora Ráster

La calculadora ráster es una herramienta que nos ayuda a aplicar expresiones matemáticas a datos ráster. Sin embargo, si todas las entradas son números, el resultado será número. Los operadores que se encuentran en la calculadora ráster son:

|   Operador             |                       Descripción                      |   Ilustración     |
|:----------------------:|:------------------------------------------------------|:-----------------:|
| +                      | [Adición](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/arithmetic-plus-operator.htm): Suma los valores de dos rásters pixel por pixel  | <img src="../images/arcgis-spatial/0_adicion.png" vspace="10" width="500"> |
| -                      | [Substracción](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/arithmetic-minus-operator.htm) o [Negativo](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/arithmetic-negate-operator.htm): Resta el valor del segundo ráster al primer ráster  | <img src="../images/arcgis-spatial/0_resta.png" vspace="10" width="500"> |
| *                      | [Multiplicación](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/arithmetic-times-operator.htm): Multiplica los valores de dos ráster  | <img src="../images/arcgis-spatial/0_multiplicacion.png" vspace="10" width="500"> |
| /                      | [División](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/arithmetic-divide-operator.htm): Divide los valores de dos ráster  | <img src="../images/arcgis-spatial/0_division.png" vspace="10" width="500"> |
| ==                     | [Igual a](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/relational-equal-to-operator.htm): Retorna píxeles con valor a 1 cuando el valor del primer y segundo ráster son iguales. Este es 0 cuando no son iguales. | <img src="../images/arcgis-spatial/0_igual-a.png" vspace="10" width="300"> |
| >                      | [Mayor a](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/relational-greater-than-operator.htm): Retorna píxeles con valor a 1 cuando el valor del primer ráster es mayor al del segundo. Este es 0 cuando no es mayor. | <img src="../images/arcgis-spatial/0_mayor-a.png" vspace="10" width="300"> |
| <                      | [Menor a](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/relational-less-than-operator.htm): Retorna píxeles con valor a 1 cuando el valor del primer ráster es menor al del segundo. Este es 0 cuando no es menor. | <img src="../images/arcgis-spatial/0_menor-a.png" vspace="10" width="300"> |
| <=                     | [Menor o igual a](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/relational-less-than-equal-operator.htm): Retorna píxeles con valor a 1 cuando el valor del primer ráster es menor o igual al del segundo. Este es 0 cuando no es menor o igual. | <img src="../images/arcgis-spatial/0_menor-igual-a.png" vspace="10" width="300"> |
| >=                     | [Mayor o igual a](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/relational-greater-than-equal-operator.htm): Retorna píxeles con valor a 1 cuando el valor del primer ráster es mayor o igual al del segundo. Este es 0 cuando no es mayor o igual. | <img src="../images/arcgis-spatial/0_mayor-igual-a.png" vspace="10" width="300"> |
| !=                     | [No es igual a](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/relational-not-equal-operator.htm): Retorna píxeles con valor a 1 cuando el valor del primer y segundo ráster no son iguales. Este es 0 cuando son iguales. | <img src="../images/arcgis-spatial/0_no-igual-a.png" vspace="10" width="300"> |
| &                      | [Y booleano](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/boolean-and-operator.htm): Realiza una operación Y booleana en los valores de dos rásters. | <img src="../images/arcgis-spatial/0_y-booleano.png" vspace="10" width="300"> |
| <p>&VerticalLine;</p>  | [O booleano](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/boolean-or-operator.htm): Realiza una operación O booleana en los valores de dos rásters. | <img src="../images/arcgis-spatial/0_o-booleano.png" vspace="10" width="300"> |
| ^                      | [O exclusión booleano](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/boolean-xor-operator.htm): Realiza una operación O booleana de exclusión en los valores de dos rásters. | <img src="../images/arcgis-spatial/0_xor-booleano.png" vspace="10" width="300"> |
| ~                      | [No booleano](https://pro.arcgis.com/es/pro-app/latest/arcpy/image-analyst/boolean-not-operator.htm): Realiza una operación No booleana en los valores de dos rásters. | <img src="../images/arcgis-spatial/0_no-booleano.png" vspace="10" width="300"> |

## Funciones Ráster

Las funciones ráster permite trabajar con datos ráster y sus diferentes bandas. Estas están disponibles al seleccionar una capa ráster, pestaña **Analysis** de la barra de herramientas, dentro del grupo **Raster**, se encuentra **Raster Functions**. Dentro del panel de **Raster Functions**, en la pestaña **System** encontamos una lista de aplicaciones para procesar datos ráster. En esta lista encontramos la opción desplegable **Math**, en la cual encontramos **Band Arithmetic**.

<p align="center">
<img src="../images/arcgis-spatial/02_fig4.jpg" vspace="10" width="300">
</p>

En el panel de **Band Arithmetic Properties**, en la pestaña **Parameters**, se puede seleccionar la capa ráster a procesar, en el campo **Method** hay algunas funciones comunes disponibles, y en el campo **Band Indexes** se puede introducir la expresión o las bandas correspondientes para aplicar una función. Algunos de los métodos o formas de introducir funciones con bandas se puede encontrar [aquí](https://pro.arcgis.com/en/pro-app/latest/help/analysis/raster-functions/band-arithmetic-function.htm).

<p align="center">
<img src="../images/arcgis-spatial/02_fig5.jpg" vspace="10" width="300">
</p>

## Estadísticas Ráster

## Práctica

### Aplicaciones de calculadora ráster

Tiempo estimado: 45 min.

Datos: Elevación, Temperatura, Multiespectral.

## 1. Importar datos

Importaremos las tres capas ráster: elevación (*DOM_alt*), temperatura (*RepDom_LST_Jul2023.tif*), y mosaico multiespectral (*RepDom_Mosaico_2021_L8*). El mosaico se compone de varias bandas multiespectrales las cuales deben ser combinadas correctamente para visualizar en color real o RGB. La combinación RGB será en este caso R: B4, G: B3, B: B2.

<p align="center">
<img src="../images/arcgis-spatial/02_fig1.jpg" vspace="10" width="900">
</p>

## 2. Seleccionar pixeles específicos

Usaremos la calculadora ráster para seleccionar áreas menores a 100 m de altitud de la capa *DOM_alt*. La calculadora ráster se puede encontrar desde la barra de herramientas en la pestaña **Analysis**, grupo **Geoprocessing**, opción **Tools**. Luego desde el panel **Geoprocessing**, pestaña **Toolboxes**, desplegamos la extensión de **Spatial Analyst Tools**, desplegamos **Map Algebra**, y hacemos click en **Raster Calculator**.

En el panel de **Raster Calculator** observaremos un cuadro con las capas ráster disponibles a un lado, y del otro lado un cuadro con los operadorooes disponibles. En el cuadro inferior escribiremos la operación que deseamos aplicar a un ráster específico. Escribiremos `"DOM_alt" <= 100`, lo cual significa que tomaremos todos los valores menores o iguales a 100 del ráster *DOM_alt*. El campo **Output raster** nos permite cambiar el nombre y la ruta de guardado de la nueva capa ráster que se producirá.

<p align="center">
<img src="../images/arcgis-spatial/02_fig2.jpg" vspace="10" width="900">
</p>

La nueva capa ráster producida será una máscara con valores igual a 1 en esos píxeles que cumplieron con la condición requerida, y valores de 0 en los pixeles que no la cumplieron. En la imagen de referencia observamos los áreas menores a 100 m en azul, y las áreas mayores a 100 m en blanco.

## 3. Aplicar máscara

La máscara de elevación la podemos usar para visualizar los datos de temperatura en solo las áreas menores a 100 m de altitud. Para esto escribiremos en la **Calculadora Ráster** la siguiente expresión: `"RepDom_LST_Jul2023" * "dom_al_rast"`, en donde multiplicamos la capa que contiene los datos temperatura con la máscara de elevación. Como resultado obtendremos una nueva capa ráster con valores de temperatura válidos en aquellas áreas menores a 100 m.

<p align="center">
<img src="../images/arcgis-spatial/02_fig3.jpg" vspace="10" width="900">
</p>

Se podrá observar que los valores de temperatura varían alrededor de 26-40 °C. Las zonas más calientes durante Julio de 2023 en áreas menores a 100 m de altitud se observaron en el lado occidente del país.

### Funciones ráster

## 4. Calcular NDVI

El índice de diferencia de vegetación normalizada (NDVI) tiene un rango de valores entre -1 a +1. Típicamente, cuando hay valores negativos existe alta probabilidad que se trate de un cuerpo de agua. Por otro lado, si los valores son cercanos a +1 es probable que se trate de vegetación muy densa. Cuando el NDVI es cercano a cero es probable que se trate de un área urbana.

Para calcular el NDVI usamos la siguiente fórmula:

$$\frac{(NIR-Rojo)}{(NIR+Rojo)}$$

La relación entre las bandas NIR (infrarrojo cercano o Near-Infrared) y Rojo van a proporcionar un índice de vegetación.

<p align="center">
<img src="../images/arcgis-spatial/02_fig6.jpg" vspace="10" width="400">
</p>

Ahora, aplicaremos la función NDVI al ráster *RepDom_Mosaico_2021_L8**. En el panel de **Band Arithmetic Properties** seleccionamos esta capa, en el campo **Method** escogemos **User Defined**, a pesar de que la función NDVI ya está disponible vamos a aplicarla desde cero. Este ráster tiene siete bandas nombradas como B1, B2, B3, etc, las cules corresponden a diferentes longitudes de onda del sensor satelital Landsat-8. Por lo tanto, en el campo **Band Indexes** escribimos la expresión: `(B5 - B4) / (B5 + B4)`, donde B5 es el NIR y B4 es el rojo. Hacemos click en **Create new layer**.

<p align="center">
<img src="../images/arcgis-spatial/02_fig7.jpg" vspace="10" width="900">
</p>

En la imagen de referencia observamos los valores más altos de NDVI en verde más oscuro, y los valores más bajos en verde más claro.

## 5. Estadisticas
Estadisticas: promedio, maximo y minimo.
Relación entre temperaturas y elevaciones.



