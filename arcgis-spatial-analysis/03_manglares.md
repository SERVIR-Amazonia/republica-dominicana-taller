![image](https://github.com/SERVIR-Amazonia/republica-dominicana-taller/assets/49037033/33527e98-2660-48e8-aeb3-b162b994a900)---
layout: page
title: Mapeo de Manglares
parent: ArcGIS Pro Análisis Espaciales
nav_order: 3
---
# Mapeo de Manglares

<sup>Este material de enseñanza está basado en ArcGIS Pro 3.1.</sup>

Este material de mapeo de manglares es una adaptación del [mapeo de manglares en GEE](https://github.com/SERVIR-Amazonia/republica-dominicana-taller/blob/main/gee-mapeo-manglares/gee-mapeo-manglares.md).

El material necesario para esta práctica es:

* Imagen sin nubes construida con la colección Landsat-8 (*RepDom_MosaicoManglar_2021_L8.tif*).
* Datos de entrenamiento (*Datos_Manglar.shp*).

## Pasos
1. Crear proyecto e importar datos.
2. Entrenamiento
3. Clasificación
4. Validación

## 1. Crear proyecto e importar datos

En un nuevo proyecto importamos los datos requeridos: la imagen de Landsdat-8 y los datos de entrenamiento. Los datos de entrenamiento son polígonos con una propiedad llamada *clase*, la cual puede ser de valor 1 o de valor 2, lo cual indicaría si son datos de Manglar o No Manglar, respectivamente.

<p align="center">
<img src="../images/arcgis-spatial/03_fig1.jpg" vspace="10" width="900">
</p>

## 2. Entrenamiento

Es importante que los datos de entrenamiento tengan una estructura indexada, es decir una columna indicando un nombre de clase (texto) y valor de clase (numerico).

<p align="center">
<img src="../images/arcgis-spatial/03_fig2.jpg" vspace="10" width="300">
</p>

Los poligonos de entrenamiento pueden editarse o crearse desde cero usando la herramienta **Training Samples Manager**. Este estás disponible seleccionando un elemento ráster, luego desde la pestaña **Imagery** de la barra de herramientas, seleccionar **Classification Tools** y ahí estará la herramienta **Training Samples Manager**. Allí se puede crear un nuevo esquema donde se pueden añadir el número de clases requeridas y se pueden dibujar los polígonos. Por el momento esto no será necesario.

Ahora, dentro del panel **Toolboxes**, vamos a la extensión de **Image Analyst Tools** (o también **Spatial Analysis Tools**), desplegamos la opción **Classification and Pattern Recognition** y seleccionamos **Train Random Trees Classifier**. En el nuevo panel que se abrirá ingresamos el ráster a clasificar en **Input Raster**, datos de entrenamiento en **Input Training Sample File**, seleccionamos la columna con las clases en **Dimension Value Field**, y seleccionamos el destino donde se guardará el archivo de entrenamiento en **Output Classifier Definition File**. La configuración para el modelo es 10 **Max Number of Trees**, 5 **Max Tree Depth**, y 1000 **Max Number of Samples Per Class**. Hacer click en **Run**. Se guardará un archivo en formato **.ecd**.

<p align="center">
<img src="../images/arcgis-spatial/03_fig3.jpg" vspace="10" width="300">
</p>

## 3. Clasificación

Ahora procedemos a clasificar la imagen. Dentro del panel **Toolboxes**, vamos a la extensión de **Image Analyst Tools** (o también **Spatial Analysis Tools**), desplegamos la opción **Classification and Pattern Recognition** y seleccionamos **Classify Raster**. En el panel que se abrirá seleccionamos la imagen a clasificar en **Input Raster**, cargamos el archivo **.ecd** de entrenamiento en **Input Classifier Definition File**, y ponemos un nombre al archivo que se producirá en **Output Classified Raster**. Hacer click en **Run**. El proceso puede tardar unos segundos en terminar.

<p align="center">
<img src="../images/arcgis-spatial/03_fig4.jpg" vspace="10" width="300">
</p>

La imagen clasificada va a lucir como esta:

<p align="center">
<img src="../images/arcgis-spatial/03_fig5.jpg" vspace="10" width="800">
</p>

## 4. Validación

Podemos crear un conjunto de puntos para validar o estimar la precisión de la clasiicación. En este caso serán puntos derivados de los polígonos usado para el entrenamiento. Dentro del panel **Toolboxes**, vamos a la extensión de **Image Analyst Tools** (o también **Spatial Analysis Tools**), desplegamos la opción **Classification and Pattern Recognition** y seleccionamos **Create Accuracy Assessment Points**. En el nuevo panel que se abrirá seleccionamos los polígonos de entrenamiento en **Input Raster or Feature Class Data**, la columna de valores por clase en **Dimension Field for Feature Class**, ponemos un nombre al archivo resultante en **Output Accuracy Assessment Points**, escogemos *Classified* en **Target Field**, el numero de puntos puede ser 500, y la estrategia de muestreo puede ser **Stratified random**.

<p align="center">
<img src="../images/arcgis-spatial/03_fig6.jpg" vspace="10" width="1000">
</p>
