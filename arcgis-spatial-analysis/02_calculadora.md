---
layout: page
title: Calculadora Ráster
parent: ArcGIS Pro Análisis Espaciales
nav_order: 2
---

# Calculadora Ráster

<sup>Este material de enseñanza está basado en ArcGIS Pro 3.1.</sup>

La calculadora ráster es una herramienta que nos ayuda a aplicar expresiones matemáticas a datos ráster. Sin embargo, si todas las entradas son números, el resultado será número. Los operadores qeu se encuentran en la calculadora ráster son:

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
| &                      | Y booleano  |
| <p>&VerticalLine;</p>  | O booleano  |
| ^                      | O exclusión booleano  |
| ~                      | No booleano  |




<p align="center">
<img src="../images/arcgis-spatial/02_fig1.jpg" vspace="10" width="400">
</p>
