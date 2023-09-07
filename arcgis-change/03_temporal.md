---
layout: page
title: Análisis Temporal
parent: ArcGIS Pro Análisis Temporales
nav_order: 3
---

# Análisis Espacio-Temporal

<sup>Este material de enseñanza está basado en ArcGIS Pro 3.1.</sup>



Crear nuevo proyecto e importar datos administrativos a nivel de provincia (*DOM_adm1*). En la tabla de atributos podremos observar que la columna que tienen el nombre de las provincias es llamada *NAME_1*. Debrían encontrarse 32 polígonos de provincias.

<p align="center">
<img src="../images/arcgis-change/03_fig1.jpg" vspace="10" width="800">
</p>

Procedemos a importar los datos con los promedios mensuales de temperatura por provincia durante 2002-2022, derivados de datos satelitales (*RepDom_TempAnualProvincias.csv*). Estos datos no tienen coordenadas, así que se cargaran como una tabla dentro de ArcGIS Pro. Al explorar sus tabla de atributos podremos observar el tipo de datos y su estructura.

<p align="center">
<img src="../images/arcgis-change/03_fig2.jpg" vspace="10" width="800">
</p>

Estos datos tiene una columna que indica el año correspondiente de cada dato, sin embargo es necesario convertir ese año numerico en un año tipo fecha que pueda ser legible más fácilmente por la aplicación. Para editar la tabla es necesario exportarla, ya que la tabla original no se puede sobreescribir. Hacer click derecho sobre la tabla original en el panel **Contents**, seleccionamos **Data**, luego **Export Table**, ponemos un nombre y hacemos click en **OK**. Ahora, vamos a editar la fecha de la nueva tabla. Vamos al panel de **Toolbox** y búscamos la herramienta **Convert Time Field**. En el nuevo panel que se abrirá seleccionamos la tabla respectiva en el campo **Input Table**, seleccionamos la columna con el año en **Input Time Field**, el formato de fecha deseado en **Input Time Format** será *yyyy*, el nombre de la columna nueva donde se alojarán las fechas puede renombrarse si se desea, y nos aseguramos que el formato de la columna sea *Date* en **Output Time Field Type**. La nueva columna mostrará fechas como *1/1/2002*.

<p align="center">
<img src="../images/arcgis-change/03_fig3.jpg" vspace="10" width="800">
</p>
