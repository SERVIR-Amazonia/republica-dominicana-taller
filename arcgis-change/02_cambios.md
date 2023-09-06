---
layout: page
title: Detección de Cambios
parent: ArcGIS Pro Análisis Temporales
nav_order: 2
---

# Detección de Cambios

<sup>Este material de enseñanza está basado en ArcGIS Pro 3.1.</sup>

Esta es la continuación de la lección anterior sobre clasificación de coberturas.

<p align="center">
<img src="../images/arcgis-change/01_fig6.jpg" vspace="10" width="800">
</p>

Para esta lección se cuantificarán las áreas por clase de cada imagen clasificada, y se detectarán los cambios por píxel de una de las clases entre las dos imágenes.

## Cuantificar áreas

Este es un procedimiento que toma en cuenta el número de píxeles por clase y el área de cada píxel. En este caso la imagen clasificada debe tener una resolución de píxel de 30 x 30 m, esto quiere decir que el área de cada píxel es 900 m2.

Para contar el número de píxels por clase podemos buscar la herramienta **Build Raster Attribute Table** en el panel de **Toolboxes**. En el panel que se abrirá escogemos el ráster clasificado en **Input Raster** y hacemos click en **Run**. Posteriormente, al hacer click derecho sobre el ráster procesado en el panel **Contents**, y seleccionamos la opción **Attribute Table**. En la tabla de atributos encontramos una columna llamada **Count** que indica el número de píxeles por clase.

Para calcular el área de cada clase (en kilometros cuadrados) debemos hacer el respectivo cálculo. Para esto hacemos click en el botón **Calculate** de la tabla de atributos, seleccionamos la imagen correspondiente en **Input Table**, ponemos un nombre para la columna donde se alojarán los nuevos datos en **Field Name (Existing or New)**, y en **Field Type** escogemos *Float*. En el campo que tendrá el nombre de la nueva columna, en este caso *Area_km2* (encima de **Code Block**) escribimos la expresión `(!Count!*900)/1000000`, la cual multiplica el número de píxeles de cada clase por 900 m2, y lo convierte a km2 al dividir por 1,000,000. Click en **OK**. Esto creará la nueva columna con los datos de área en la unidad correspondiente.

<p align="center">
<img src="../images/arcgis-change/02_fig1.jpg" vspace="10" width="600">
</p>

Realizamos el mismo procedimiento para la otra imagen y comparamos. Los resultados son:

|    Clase         |  Área (km2) 2000  |  Área (km2) 2022  |  Diferencia  |
|:----------------:|:-----------------:|:-----------------:|:------------:|
| Agua             |  33.7             |  32.1             |  -1.6        |
| Vegetación densa |  710.7            |  738.4            |  +27.7       |
| Vegetación baja  |  733.3            |  666.9            |  -66.4       |
| Agricultura      |  143.4            |  161.7            |  +18.3       |
| Urbano           |  57.0             |  52.4             |  -4.6        |
| Deforestado      |  58.2             |  84.7             |  +26.5       |

