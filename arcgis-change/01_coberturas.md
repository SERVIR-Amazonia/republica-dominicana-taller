---
layout: page
title: Cobertura Terrestre
parent: ArcGIS Pro Análisis Temporales
nav_order: 1
---

# Clasificación de cobertura terrestre

<sup>Este material de enseñanza está basado en ArcGIS Pro 3.1.</sup>

La clasificación de cobertura terrestre se procesa de manera similar a la aprendidada en la lección de Mapeo de Manglares. La diferencia con esta clasificación es el número de objetos a clasificar o clases. El número de clases depende de la imagen o localidad a clasificar. Algunos lugares pueden ser muy homogéneos, por ejemplo un bosque puede ser clasificado como solamente vegetación, o pueden incluirse clases más específicas como vegetación primaria y vegetación primaria, o palmas y manglares, todo depende del nivel de detalle que se desea obtener. Sin embargo, pueden existir limitaciones que dependen de la resolución espacial y espectral de las imágenes a usar. Las imágenes multiespectrales de amplio uso público vienen resoluciones espaciales que pueden ir desde los 500 m a 10 m por píxel (MODIS, Landsat, Sentinel-2). Las imágenes hiperespectrales pueden ayudar a obtener clasificaciones más detalladas pero normalmente estos datos suelen ser comerciales, limitados, o de difícil acceso.

<p align="center">
<img src="../images/arcgis-change/01_fig1.png" vspace="10" width="600">
</p>

Para esta lección usaremos dos imágenes multiespectrales de dos años y sensores diferentes. Una imagen compuesta del año 2000 construida con Landsat-7 y otra del año 2022 construida con Landsat-8. Estos dos sensores tienen resolución espacial de 30 m por píxel y tienen similares bandas espectrales, a excepción de la banda adicional de Landsa-8 en la región azul, también llamada banda ultra azul o aerosol. En estra lección nos enfocaremos en únicamente producir mapas de cobertura terrestre en estas dos imágenes con 20 años de diferencia.

<p align="center">
<img src="../images/arcgis-change/01_fig2.jpg" vspace="10" width="800">
</p>

### Datos requeridos:
* Mosaico compuesto de Landsat-8 año 2022 (*RepDom_MosaicoMineria_2022_L8.tif*)
* Mosaico compuesto de Landsat-7 año 2000 (*RepDom_MosaicoMineria_2000_L7.tif*)

## Pasos
1. Importar datos
2. Establecer categorías de cobertura
3. Recolectar datos de entrenamiento
4. Clasificar imágenes

## 1. Importar datos

Creamos un nuevo proyecto e importamos las dos imágenes de interés. La combinación de bandas RGB para Landsat-7 es B3/B2/B1 y para Landsat-8 es B4/B3/B2.

<p align="center">
<img src="../images/arcgis-change/01_fig3.jpg" vspace="10" width="1000">
</p>

## 2. Categorías de cobertura

Las categorías las estableceremos de acuerdo a las clases de fondos que podamos interpretar en ambas imágenes. Idealmente, estas clases deben ser las mismas en ambas imágenes.

Las clases comunes que podemos identificar son seis:

* Agua
* Vegetación densa
* Vegetación baja
* Agricultura
* Urbano
* Deforestado

<p align="center">
<img src="../images/arcgis-change/01_fig4.jpg" vspace="10" width="10600">
</p>
