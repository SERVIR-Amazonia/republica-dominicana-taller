---
layout: page
title: Crear Mapa
parent: ArcGIS Pro Introducción
nav_order: 3
---

# Crear Mapa

Para compartir algún proyecto ya sea mapa, poster, o archivo PDF, se requiere saber crear un diseño. El diseño es una composición de uno o más mapas, junto con los elementos que lo componen como título, leyenda, y texto. Algunos diseños pueden incluir más de un mapa. Para esta sección se creará un nuevo proyecto, se descargarán y utilizaran algunos datos vectoriales, se creará un mapa, y se exportará.

Este material de enseñanza está basado en ArcGIS Pro 3.1, y usa algunos recursos de la [guía rápida](https://pro.arcgis.com/en/pro-app/latest/get-started/add-maps-to-a-layout.htm) a ArcGIS Pro de ESRI<sup>TM</sup>.

Tiempo estimado: 60 min.

## Material

Se usará material descargado del portal [Diva-GIS](http://www.diva-gis.org/gdata), correspondiente a República Dominicana, tanto en formatos vectorial como ráster:
* Administrative areas
* Inland water
* Roads
* Elevation
* Land cover
* Population

## 1. Nuevo Proyecto

1.1. Abra ArcGIS Pro y cree un nuevo proyecto. Si ha estado trabajando en otro proyecto puede ir a la pestaña **Project**, seleccionar **New**, y dar click en **Map**. Para esta práctica es recomendable que el proyecto se guarde en su computador local. Posteriormente aparecerá una ventana donde puede ingresar un nombre a su proyecto y decidir en donde lo va guardar.

<p align="center">
<img src="../images/intro-arcgis/03_fig1.jpg" vspace="10" width="800">
</p>

1.2. A continuación usted verá que crea un proyecto y se observara una vista de mapa. En el panel **Contents** se mostrarán dos capas predeterminadas que muestran el mapa mundial con detalles topográficos y administrativos. Estás capas nos ayudan a orientarnos espacialmente. Si usted no las desea utilizar en su proyecto las puede deseleccionar o remover.

<p align="center">
<img src="../images/intro-arcgis/03_fig2.jpg" vspace="10" width="800">
</p>

## 2. Importar datos vectoriales

2.1. Podemos importar o añadir datos al proyecto de dos formas: podemos arrastrar el archivo y soltarlo en el panel **Contents** o podemos ir a la pestaña **Map**, dentro del grupo **Layer**, dar click en **Add Data**. Se va a desplegar una lista con diversas acciones, vamos a dar click en **Data**.

<p align="center">
<img src="../images/intro-arcgis/03_fig3.jpg" vspace="10" width="600">
</p>

2.2. En la ventana que aparece vamos a buscar el directorio donde hemos guardado nuestros archivos. Vamos a cargar las capas administrativas de República Dominicana en la carpeta llamada *DOM_adm*. Dentro de esta carpeta veremos archivos en formato *.shp* y *.csv*, ambos formatos se pueden importar, pero en este caso vamos a trabajar con archivos .shp. Seleccionamos los tres archivos .shp disponibles, los cuales indican el nivel administrativo.

<p align="center">
<img src="../images/intro-arcgis/03_fig4.jpg" vspace="10" width="500">
</p>

2.3. Los archivos que importemos los veremos en el panel **Contents**. El nivel administrativo 0 es unicamente un polígono del área nacional, el nivel administrativo 1 son varios polígonos de las áreas provinciales, y el nivel administrativo 3 son más polígonos de las áreas municipales. Cada capa es cargada con un color de manera predeterminada, pero puede ser editada.

<p align="center">
<img src="../images/intro-arcgis/03_fig5.jpg" vspace="10" width="800">
</p>


## Descargar datos geoespaciales

* [The open data portal based on ArcGIS Hub technology](https://hub.arcgis.com/search): Portal con datos compartidos por usuarios Esri.
* [The Esri Living Atlas of the World](https://livingatlas.arcgis.com/en/home/): Portal con cientos de datos y mapas de diversos temas.
* [Protected Planet](https://www.protectedplanet.net/en): provee datos sobre las áreas terrestres y marinas protegidas a nivel global, y está en constante actualización. 
* [The European Space Agency’s Sentinel Online data portal](https://sentinel.esa.int/web/sentinel/sentinel-data-access): incluye información relacionada con temas relacionados a la tierra, oceano, atmófera, emergencia, y seguridad.
* [CIESIN](http://www.ciesin.org/sub_guide.html) de la Universidad de Columbia que durante más de 20 años ha proveído datos sobre clima, población, suelo, economía, uso del suelo, biodiversidad y otros temas.
* [Atlas of the Biosphere](https://sage.nelson.wisc.edu/) provee datos globales de impacto humano, uso del suelo, ecosistemas, y recursos acuáticos.
* [Natural Earth](https://www.naturalearthdata.com/) provee datos a escala pequeña de manera global, tanto en formato vectorial o ráster.
* [The World Resources Institute](https://www.wri.org/): datos geospaciales para sitios muy específicos como Kenya y Uganda.
* [The FAO GeoNetwork](https://data.apps.fao.org/map/catalog/srv/eng/catalog.search#/home): provee datos globales y regionales de las divisiones politico-administrativas, población, recursos acuáticos, uso del suelo.
* [OpenTopography](https://opentopography.org/): Datos relacionados con ciencias de la tierra, topográficos y batimétricos.
* [Diva-GIS](http://www.diva-gis.org/gdata): portal que ofrece datos de areas administrativas, fuentes de agua, elevación, carreteras, población, clima, entre otros, organizados por país.
* [TerraPopulus](https://terra.ipums.org/): Datos ambientales y poblacionales.
