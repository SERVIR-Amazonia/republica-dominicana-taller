---
layout: page
title: Crear Mapa
parent: ArcGIS Pro Introducción
nav_order: 3
---

# Crear Mapa

Para compartir algún proyecto ya sea mapa, poster, o archivo PDF, se requiere saber crear un diseño. El diseño es una composición de uno o más mapas, junto con los elementos que lo componen como título, leyenda, y texto. Algunos diseños pueden incluir más de un mapa. Para esta sección se creará un nuevo proyecto, se descargarán y utilizaran algunos datos vectoriales, se creará un mapa, y se exportará.

<p align="center">
<img src="../images/intro-arcgis/03_mapa.jpg" vspace="10" width="300">
</p>

Este material de enseñanza está basado en ArcGIS Pro 3.1, y usa algunos recursos de la [guía rápida](https://pro.arcgis.com/en/pro-app/latest/get-started/add-maps-to-a-layout.htm) a ArcGIS Pro de ESRI<sup>TM</sup>.

Tiempo estimado: 60-90 min.

## Material

Se usará material descargado del portal [Diva-GIS](http://www.diva-gis.org/gdata) y [Natural Earth](https://www.naturalearthdata.com/), correspondiente a República Dominicana en formatos vectoriales:
* Administrative areas (Diva GIS) (*DOM_adm*)
* Inland water (Diva GIS) (*DOM_wat*)
* Roads (Diva GIS) (*DOM_rds*)
* Airports (Natural Earth) (*ne_10m_airports*)
* Ports (Natural Earth) (*ne_10m_ports*)

Descargar material [AQUÍ](https://drive.google.com/drive/u/1/folders/1x6qXRMHdH3iVh2Fc1znJyarl101YlDvC).

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

2.3. Los archivos que importemos los veremos en el panel **Contents**. El nivel administrativo 0 es unicamente un polígono del área nacional, el nivel administrativo 1 son varios polígonos de las áreas provinciales, y el nivel administrativo 2 son más polígonos de las áreas municipales. Cada capa es cargada con un color de manera predeterminada, pero puede ser editada expandiendo las capas y dando click en el recuadro coloreado. Esto abrirá el panel **Symbology** donde se puede editar el color de relleno, color de línea, y ancho de línea desde la pestaña **Properties**. Recuerde que para ver las otras capas en la vista de mapa debe deseleccionar otras que se encuentran por encima de la que desea visualizar.

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

4.1. En la pestaña **Insert** de la barra de herramientas, damos click en **Map Frame**, ubicado dentro del grupo **Map Frames**. Se abrirá un vista desplegable, y seleccionamos el mapa que tiene nuestras capas visibles.

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

4.5. Al explorar la tabla de atributos de la capa *DOM_adm1*, veremos que los nombres de las provincias están dentro del atributo o columna llamada *NAME_1*. Este atributo será el que usaremos para filtrar las provincias de interés. Con la capa *DOM_adm1* seleccionada, damos click en la pestaña **Feature Layer** de la barra de herramientas, desplegamos la flecha de **Symbology**, y escogemos la opción **Unique Values**. En el panel **Symbology**, seleccionas el campo *NAME_1* en la opción **Field 1**. Veremos una clasificación de colores automática para cada Provincia. Dentro del subpanel **Classes** veremos la lista de provincias, seleccionamos todas las que no nos interesan y presionamos la tecla *Supr* para eliminarlos de esta clasificación. Al final la lista deberá mostrar solo tres clases: Distrito Nacional, Santo Domingo, y otro clases que incluye todos los demas valores o provincias en **all other values**. Por ahora, vamos a editar la clase *all other values* dejandola invisible. Para ello damos click en el recuadro de color correspondiente, se abrirá otro panel de **Symbology**, en la pestaña **Properties**, damos click en el botón **Layers**. Deseleccionamos las opciones de **Solid stroke** y **Solid fill** para ocultar estos objetos, y damos click en **Apply**.

<p align="center">
<img src="../images/intro-arcgis/03_fig14.jpg" vspace="10" width="1000">
</p>

4.6. Para añadir un segundo marco con capas independientes del primer marco es necesario añadir un nuevo mapa. Vamos a la pestaña **Insert**, damos click en **New Map**, y agregamos en este mapa los datos que vamos a usar para el segundo marco. Por ahora vamos a añadir solo la capa *DOM_adm2* que contiene los municipios. Si agregamos un segundo marco usando la misma vista de mapa, estos no van a ser independientes y los cambios que hagamos en las capas se verán reflejados en los otros marcos.

4.7. Ahora agregamos un nuevo marco en la vista **Layout** o plantilla donde estamos creando el mapa. Nos aseguramos de seleccionar la vista del mapa correspondiente. Seleccionamos la capa *DOM_adm2* que contiene municipios y hacemos un procedimiento similar al del paso 4.5. Vamos a dejar únicamente visibles los municipios que estén en las provincias de Santo Domingo y Distrito Nacional. Es necesario usar dos campos para filtrar los municipios en el panel **Symbology**. En **Field 1** usamos el campo *NAME_1*, luego damos click en **Add field** para añadir nuevo campo, y en **Field 2** seleccionamos el campo *NAME_2*. Veremos que ahora las clases serán independientes por municipio y provincia (apróximadamente 159 clases), debemos únicamente remover las clases de los municipios que no pertenecen a Santo Domingo y Distrito Nacional. Otra forma de filtrar es hacerlo únicamente por el campo *NAME_1*, y obtendremos todos los municipios agrupados por provincia. Este segundo marco será nuesto mapa principal.

<p align="center">
<img src="../images/intro-arcgis/03_fig15.jpg" vspace="10" width="800">
</p>

## 5. Complementar y personalizar datos del mapa

5.1. Vamos a añadir datos de carreteras (*DOM_rds*), ríos (*DOM_water_lines_dcw*), aeropuertos (*ne_10m_airports*), y puertos (*ne_10m_ports*), a la más reciente vista de mapa creada. Activamos también la capa *DOM_adm0* en el segundo marco de mapa. En este momento tenemos datos vectoriales de todo tipo: polígonos, líneas, y puntos.

<p align="center">
<img src="../images/intro-arcgis/03_fig16.jpg" vspace="10" width="800">
</p>

5.2. En este paso vamos a cambiar los colores de cada una de las capas y objetos del mapa, cambiar grosor y tipos de lineas, y asignaremos símbolos a los aeropuertos y puertos. Todo esto lo haremos desde el panel **Symbology**. En el marco 1, pondremos los colores que nos parezcan para distinguir las provincias de interés e identificar su ubicación dentro de República Dominicana. El grosor de líneas puede ser de *1 pt*. En el marco 2, damos énfasis a los municipios de las provincias de interés asignando un color más oscuro y aumentando el grosor de líneas a *2 pt*. Las carreteras y ríos se han cambiado a líneas rayadas, de color rojo y azul respectivamente, y grosor de línea de *1.5 pt*. A los símbolos para aeropuertos y puertos se les aumento el símbolo a *20 pt* y el área circular a *22 pt*, y se les cambio el solo al símbolo.

<p align="center">
<img src="../images/intro-arcgis/03_fig17.jpg" vspace="10" width="800">
</p>

5.3. Adicionalmente, añadiremos un nuevo mapa y añadiremos un tercer marco que indicará la posición regional de República Dominicana, usando las capas predeterminadas de *World Topographic Map* y *World Hillshade*. Añadimos un punto sobre el tercer marco indicando la posición de República Dominicana. Vamos a la pestaña **Insert**, en el grupo **Graphics and Text**, seleccionamos un punto y lo ponemos sobre el marco. Veremos que que se añade este punto como un nuevo elemento en el panel **Contents**. Si lo deseamos, podemos personalizar este punto. Seleccionamos la capa **Point**, luego vamos a la pestaña **Graphic** en la barra de herramientas, dentro del grupo **Symbol** encontramos las opciones para cambiar la forma, tamañoy color de este símbolo. En este ejemplo se ha usado una estrella roja de tamaño 20 pt. En el primer marco (*Map Frame*) activamos la capa *World Topographic Map*.

<p align="center">
<img src="../images/intro-arcgis/03_fig18.jpg" vspace="10" width="800">
</p>

## 6. Agregar últimos detalles del mapa

6.1. Vamos a añadir etiquetas dentro de los marcos. Esto lo podemos hacer de dos formas: añadiendo elementos de texto manualmente o añadiendo etiquetas predeterminadas usando los atributos de cada capa. Para las estiquetas de los municipios, seleccionamos la capa *DOM_adm2*, damos click en la pestaña **Labeling** en la barra de herramientas, dentro del grupo **Label Class**, en **Field** seleccionamos el atributo *NAME_2*, y damos click en el botón **Label** para activar las etiquetas. Para agregar cuadros de texto adicional, dar click en la pestaña **Insert** de la barra de herramientas, en el grupo **Graphics and Text**, dar click en el ícono **Straight text** para insertar texto, luego dar click dentro de algún marco para escribir texto. El texto se puede editar dando click en el cuadro de texto, luego ir a la pestaña **Text** en la barra de herramientas, dentro del grupo **Text Symbol** se encuentran las opciones para cambiar tipo y tamaño de fuente. Es importante que el texto sea legible y tenga tamaño adecuado.

<p align="center">
<img src="../images/intro-arcgis/03_fig19.jpg" vspace="10" width="800">
</p>

6.2. En el marco inicial que contiene la vista de República Dominicana (*Map Frame*), lo seleccionamos y damos click en **Insert**, dentro del grupo **Map Frames**, dar click en **Extent Indicator**, y seleccionamos el marco que tiene la vista detallada de municipios, río, y carreteras (*Map Frame 1*). Ahora podremos ver que se dibuja un rectangulo indicando la extensión de este mapa dentro del marco *Map Frame*. 

Ahora, procedemos a agregar una grilla al marco *Map Frame 1*, damos click en **Insert**, en el grupo **Map Frames** damos click en **Grid**. Se dibujará una grilla sobre el marco, y se añadirá un elemento nuevo dentro del grupo *Map Frame 1* en el panel **Contents**. Podemos editar la grilla haciendo click derecho en el elemento de grilla *Black Horizontal Label Graticule* en el panel **Contents**, hacemos click en **Properties**, y se abrirá el panel **Element**. Damos click en el botón **Components**, seleccionamos **Labels** de la lista, y en la pestaña **Visible** desmarcamos las casillas **North** y **East** para no hacerlas visibles. Adicionalmente, en la pestaña **Vertical** seleccionamos el recuadro **West**, para visualizar las etiquetas de coordenada de forma vertical.

Para editar el intervalo de la grilla nos dirijimos al botón **Options** del panel **Element**, y deseleccionamos la opción **Automatically adjust** dentro de la pestaña **Interval**. Luego, en el botón **Components** seleccionamos **Labels** y cambiamos el intervalo de latitud y longitud, en este ejemplo es cada 0 grados y 10 minutos (0°10'0"). En la lista de **Components** seleccionamos **Ticks 1**, y ponemos un intervalo de 0 grados y 5 minutos (0°5'0"), y en **Appearence** ajustamos la longitud de los marcadores en **Length** a 0.05 in. Por último, ajustamos el tamaño de fuente de las coordenadas. Esto se hace seleccionando **Labels** del desplegable en la esquina superior izquierda del panel **Element**, ahí seleccionamos un tamaño de 10 pt en la opción **Size**.

<p align="center">
<img src="../images/intro-arcgis/03_fig20.jpg" vspace="10" width="800">
</p>

6.3. El siguiente paso es agregar un leyenda al mapa. Vamos a seleccionar el marco *Map Frame 1* que contiene los municipios, carreteras y ríos, luego en la pestaña **Insert** en la barra de herramientas, dentro del grupo **Map Surrounds**, seleccionamos la flecha de **Legend** y escogemos la opción **Legend 4**. Luego dibujamos un recuadro dentro del marco de mapa. Esto agregará una leyenda con todos los elementos o capas usadas en este marco respectivo, y un elemento de leyenda se agregará en el panel **Contents**.

<p align="center">
<img src="../images/intro-arcgis/03_fig21.jpg" vspace="10" width="300">
</p>

Sin embargo, esta leyenda es todavia muy precaria, y muestra más elementos de los que debería. Así que vamos a ir al panel **Contents** y a desplegar la lista de elementos dentro de **Legend**. Deseleccionamos *DOM_adm0*, *DOM_adm1*, y *DOM_adm2*. Aún falta cambiar el nombre de las capas correctamente, así que vamos al *Map Frame 1* y desplegamos los elementos en el panel **Contents**, seleccionamos cada capa individualmente y cambiamos su nombre, ya sea haciendo un segundo click sobre el nombre de la capa o yendo a **Properties** de la capa, y cambiar el nombre desde el campo *Name* en la pestaña **General**. Luego, podemos aumentar el tamaño de fuente de la leyenda haciendo click derecho sobre el elemento *Legend** en el panel **Contents**, se abrirá el panel **Element**, y nos dirigimos a la pestaña **Text Symbol** y cambiamos el tamaño en **Size**, en este caso usamos 14 pt. Activamos el título de la leyenda en la pestaña **Legend** del panel **Element*, luego en la pestaña **Legend** activar el recuadro **Show** en la opción *Title*. Podemos poner un título adecuado a nuestra leyenda. Adicionalmente, podemos agregar un borde al cuadro de leyenda desde el botón **Display** en el panel **Element**, en la pestaña **Border**, seleccionamos en la opción **Symbol** un color y grosor de línea.

<p align="center">
<img src="../images/intro-arcgis/03_fig22.jpg" vspace="10" width="1000">
</p>

6.4. Los detalles finales del mapa incluyen una roseta de los vientos, la escala del mapa, y cuadros de texto incluyendo alguna descripción o créditos. El cuadro de descripción podemos agregarlo desde la pestaña **Insert**, grupo **Graphics and Text**, botón **Dynamic Text**, y seleccionamos **Description**. Luego dibujamos el recuadro sobre la plantilla de mapa, lo seleccionamos, y en el panel **Element** escribiremos la descripción del mapa en el recuadro de la opción **Text** de la pestaña **Options**. El texto no se ajusta automáticamente al tamaño del recuadro, por lo tanto hay que escribir en líneas diferentes las porciones de texto.

Para agregar la roseta o flecha de Norte, seleccionamos el marco *Map Frame 1*, y luego vamos a **Insert** de la barra de herramientas, en el grupo **Map Surrounds**, desplegamos la opción **North Arrow** y seleccionamos una figura adecuada. Normalmente se ubica en una de las esquinas superiores del mapa.

Por último, la barra de escala se agrega desde el mismo grupo **Map Surrounds**, seleccionando un diseño de los disponibles en la opción **Scale Bar**, usando las unidades métricas. Dibujamos la escala en el mapa, luego lo editamos desde el panel **Element**. En la pestaña **Scale Bar** del panel **Element**, en la sección **Map Units**, seleccionamos las unidades *Kilometers*, y definimos la etiqueta de unidad como *Km* en el campo de **Label Text**. Ahora, hacemos click en el botón **Properties**, en la sección **Fitting Strategy** seleccionamos **Adjust number of divisions**. Luego en la sección **Divisions**, en el campo **Division Value** escribimos 20, y en la opción **Subdivisions** seleccionamos 4. Esto significa que la longitud máxima de la barra de escala va a tener máximo 20 km y va a tener 4 subdivisiones, una cada 5 km. En la pestaña **Text Symbol** del panel **Element** están las opciones para cambiar tamaño y tipo de fuente.

<p align="center">
<img src="../images/intro-arcgis/03_fig23.jpg" vspace="10" width="1000">
</p>

## Exportar mapa

Teniendo nuestro mapa finalizado podemos exportarlo desde la pestaña **Share**, grupo **Output**, opción **Export Layout**. Allí veremos multiples formatos, incluyendo GeoTIFF y Web JPEG. Al seleccionar el formato, se abrirá el panel **Export**. Si hemos selecccionado Web JPEG, observaremos que podemos escoger el formato de imagen disponible en **File Type**. Otras opciones están disponibles, como directorio donde se desea exportar, compresión, resolución, y color. Por ultimo, dar click en el botón **Export**.

<p align="center">
<img src="../images/intro-arcgis/03_fig24.jpg" vspace="10" width="300">
</p>

El resultado será un mapa como este, con el cual finalizamos esta lección:

<p align="center">
<img src="../images/intro-arcgis/03_mapa.jpg" vspace="10" width="600">
</p>

# Recursos para descargar datos geoespaciales

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
