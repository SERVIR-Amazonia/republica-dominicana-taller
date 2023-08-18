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
<img src="../images/intro-arcgis/03_fig1.jpg" vspace="10" width="1000">
</p>

1.2. A continuación usted verá que crea un proyecto y se observara una vista de mapa. En el panel **Contents** se mostrarán dos capas predeterminadas que muestran el mapa mundial con detalles topográficos y administrativos. Estás capas nos ayudan a orientarnos espacialmente. Si usted no las desea utilizar en su proyecto las puede deseleccionar o remover.

<p align="center">
<img src="../images/intro-arcgis/03_fig2.jpg" vspace="10" width="1000">
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

2.3. Los archivos que importemos los veremos en el panel **Contents**. El nivel administrativo 0 es unicamente un polígono del área nacional, el nivel administrativo 1 son varios polígonos de las áreas provinciales, y el nivel administrativo 2 son más polígonos de las áreas municipales. Cada capa es cargada con un color de manera predeterminada, pero puede ser editada expandiendo las capas y dando click en el recuadro coloreado. Esto abrirá el panel **Simbology** donde se puede editar el color de relleno, color de línea, y ancho de línea desde la pestaña **Properties**. Recuerde que para ver las otras capas en la vista de mapa debe deseleccionar otras que se encuentran por encima de la que desea visualizar.

<p align="center">
<img src="../images/intro-arcgis/03_fig5.jpg" vspace="10" width="1000">
</p>

2.4. Es importante verificar la información asociada a nuestros datos, especialmente el sistema de coordenadas que maneja. Si damos click derecho sobre una de las capas y damos clcik en **Properties** se abrirá la ventana de propiedades. En la pestaña **Source** podremos observar información sobre qué tipo de datos son, en este caso es uns hapefile que contiene geometrías de tipo polígono en la pestaña **Data Source**. La pestaña **Spatial Reference** nos da la información detallada sobre el tipo de coordenadas, en este caso es WGS84 EPSG:4326, la cual esta en un sistema ampliamente usado y deseado. Si usamos datos con otro tipo de coordenas tendriamos que hacer una conversión para trabajar todos los datos en un solo sistema. La pestaña **Extent** nos muestra los limites geográficos de nuestros datos y **Domain, Resolution, and Tolerance** nos brinda información sobre las extensiones máximas y mínimas que puede tener, junto con las resoluciones.

<p align="center">
<img src="../images/intro-arcgis/03_fig6.jpg" vspace="10" width="600">
</p>

## 3. Insertar plantilla de diseño (*Layout*)

3.1. Vamos a la barra de herramientas, en la pestaña **Insert**, dentro del grupo **Project**, damos click en **New Layout**. Se desplegará una lista de formatos de hoja y orientaciones. Usaremos el tamaño carta estandar en sentido horizontal, para ello seleccionamos el formato **Letter** dentro del grupo **ANSI - Landscape**.

<p align="center">
<img src="../images/intro-arcgis/03_fig7.jpg" vspace="10" width="900">
</p>

3.2. Ahora tendremos otra vista o pestaña disponible llamada *Layout*. Si no tenemos disponibles la regla y las guías, podemos activarlas dando click derecho en *Layout* dentro del panel **Contents**, y activamos las opciones **Guides** y **Rulers**. Estas serán de ayuda para ubicar correctamente los objetos y mapas en nuestro diseño.

<p align="center">
<img src="../images/intro-arcgis/03_fig8.jpg" vspace="10" width="500">
</p>

3.3. Podremos agregar las guías dando click derecho sobre la regla que está visible dentro de la vista *Layout*. La opción **Add Guide** colocará una guía sobre la posición que hicimos click. Sin embargo, vamos poner diversas guías horizontales y verticales espaciadas equitativamente. Damos click en **Add Guides...**. En el panel que se abrirá seleccionamos la orientación **Both**, la colocación será **Evenly spaced**, y el intervalo de separación será **1 in**. Hacemos click en OK y veremos que ahora tenemos una grilla en nuestra plantilla de diseño que nos ayudará a posicionar los objetos. Si se desea remover las guías, damos click derecho sobre la regla 

<p align="center">
<img src="../images/intro-arcgis/03_fig9.jpg" vspace="10" width="600">
</p>

## 4. Insertar mapa

4.1. En la pestaña **Insert** de la barra de herramientas, damos click en **Map Frame**, ubicado dentro del grupo **Map Frames**. Se abrirá un vista desplegable, y seleccionamos el mapa que tiene nuestars capas visibles.

<p align="center">
<img src="../images/intro-arcgis/03_fig10.jpg" vspace="10" width="400">
</p>

4.2. Ahora podremos crear un recuadro hacinedo click sobre la plantilla y arrastrandolo hasta el tamaño que deseamos tener. Este marco se puede cambiar de tamaño posteriormente.

<p align="center">
<img src="../images/intro-arcgis/03_fig11.jpg" vspace="10" width="1000">
</p>

4.3. Sin embargo puede notar que la extensión del mapa puede no mostrarse como se desea, e incluso no se muestra la capa que deseamos. Primero nos aseguramos de seleccionar unicamente la capa que nos interesa mostrar en este marco, la cual será la capa *DOM_adm0*. Ahora, para cambiar la escala o extension del mapa dentro del marco, debemos seleccionar el marco haciendo click dentro de él. Nos dirigimos a la pestaña **Layout** de la barra de herramientas, y dentro del grupo **Map** damos click en **Activate**. Podremos observar que el marco se seleccionará y podremos cambiar la escala del mapa dentro del marco. Para cerrar la activación, nos dirigimos a la pestaña **Layout** de la barra de herramientas, y damos click en **Close Activation**.

<p align="center">
<img src="../images/intro-arcgis/03_fig12.jpg" vspace="10" width="1000">
</p>

4.4. En este primer marco vamos a seleccionar también la capa *DOM_adm1* que muestra las provincias de República Dominicana. Nos enfocaremos en la provincia de Santo Domingo y Distrito Nacional. Vamos a filtrarla para dejar que estas sean las unicas visibles y se superpongan a la capa *DOM_adm0*.

<p align="center">
<img src="../images/intro-arcgis/03_fig13.jpg" vspace="10" width="800">
</p>

4.5. Al explorar la tabla de atributos de la capa *DOM_adm1*, veremos que los nombres de las provincias están dentro del atributo o columna llamada *NAME_1*. Este atributo será el que usaremos para filtrar las provincias de interés. Con la capa *DOM_adm1* seleccionada, damos click en la pestaña **Feature Layer** de la barra de herramientas, desplegamos la flecha de **Simbology**, y escogemos la opción **Unique Values**.

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
