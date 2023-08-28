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
