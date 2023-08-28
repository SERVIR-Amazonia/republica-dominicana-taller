---
layout: page
title: Interpolaciones Espaciales
parent: ArcGIS Pro Análisis Espaciales
nav_order: 1
---

# Interpolaciones Espaciales

<sup>Este material de enseñanza está basado en ArcGIS Pro 3.1.</sup>

La interpolación es un método que ayuda a predecir valores de píxel (ráster) entre un número limitado de puntos. Es un método muy útil para predecir valores desconocidos de algún parámetro dentro de una zona geográfica entre puntos de muestreo, por ejemplo datos de elevación, precipitación, concentraciones químicas, niveles de ruido, entre otros.

<p align="center">
<img src="../images/arcgis-spatial/01_fig1.jpg" vspace="10" width="400">
</p>

Hay una variedad de formas de predecir datos espaciales, cada método es conocido como un *modelo*. Para cada modelo existen diferentes presunciones de acuerdo al tipo de datos; por ejemplo un modelo puede estimar la variación local mejor que otro. Cada modelo produce predicciones usando diferentes cálculos. Las herramientas de interpolación estan divididas en métodos determinísticos y geoestadísticos.

* Los métodos determinísticos asignan valores (predecidos) alrededor de los valores medidos y en fórmulas matemáticas específicas que determinan la suavidad de la capa resultante. Entre estos se encuentran los métodos IDW (Inverse Distance Weighting - Distancia Inversa Ponderada), Natural Neighbor, Trend, y Spline.
* Los métodos geoestadísticos predicen valores basados en modelos estadísticos como la autocorrelación espacial (relación estadística entre puntos medidos). Debido a esto las técnicas geoestadísticas no solo tienen la capacidad de producir una capa o superficie de predicción, sino que también produce algunas medidas de precisión de las predicciones. Entre estos podemos encontrar el método Kriging.

Los métodos de interpolación disponibles en la herramienta Spatial Analysis de ArcGIS Pro son:

|   Método             |                       Descripción                                                                  |
|:--------------------:|:--------------------------------------------------------------------------------------------------:|
| IDW                  | El IDW estima valores de celda (o píxel) promediando los valores de muestra cercanos a cada celda a predecir. |
| Kriging              | Este es un método geoestadístico avanzado que produce interpolaciones basadas en valores o mediciones de un conjunto de puntos dispersos espacialmente. Adicionalmente, esta herramiento ofrece diversos modelos de semi-variogramas a usar: esférico, circular, gaussiano, lineal. Es importante conocer el 'comportamiento' u origen de los datos para seleccionar el método a usar.  |
| Natural Neighbor     | Este método toma el conjunto de datos o puntos más cercanos al punto a predecir y pondera esos valores.  |
| Spline               | Este método estima valores usando una función matemática que suaviza la interpolación entre los puntos de muestreo.  |
| Spline with Barriers | Similar al método Spline, pero puede usar tanto los valores de muestreo como barreras entre estos que genera cierta discontinuidad.  |
| Topo to Raster       | Este método es específico para crear una interpolación que represente una cuenca natural y que preserve mejor los contornos de los datos.  |
| Trend                | Esta es una interpolación polinómica global que suaviza los datos aplicando una función polinómica a las muestras. Esta interpolación ayuda a capturar patrones en escalas grandes o no tan finas.  |
