---
layout: page
title: Práctica de Introducción
parent: ArcGIS Pro Introducción
nav_order: 2
---

# Práctica de Introducción

Este material de enseñanza está basado en ArcGIS Pro 3.1, y usa algunos recursos de la [guía rápida](https://pro.arcgis.com/en/pro-app/latest/get-started/introducing-arcgis-pro.htm) a ArcGIS Pro de ESRI<sup>TM</sup>.

En esta práctica se explorarán los componentes principales de la interfaz de ArcGIS Pro: la barra de herramientas, vistas, y paneles.

Se requiere descargar el proyecto **Introducing_ArcGIS_Pro.ppkx** disponible en este [enlace](https://www.arcgis.com/home/item.html?id=c25cf7226e3a48d48f0de9ac5a5a9122) (pestaña *Download*), y guardarlo en una carpeta específica de trabajo en su computador personal. Este proyecto contiene mapas 2D y 3D de Wellington, Nueva Zelanda.

Previamente, verifique que tiene ArcGIS Pro debidamente licenciado y listo para trabajar.

Tiempo estimado: 30 min.

## Abrir Proyecto

1. Inicie ArcGIS Pro. Si es necesario, haga click en **Sign in** en la esquina superior derecha, escriba su usuario y contraseña, y click en Sign in.
2. En la página de inicio, junto a la lista de proyectos recientes, haga click en **Open another project**. Si ya tiene un proyecto abierto, haga click en la pestaña **Project** de la barra de herramientas, haga click en **Open**, y posteriormente en **Open another project**.

<p align="center">
<img src="../images/intro-arcgis/02_fig1.jpg" vspace="10" width="800">
</p>

3. Aquí usted puede escoger si desea cargar un archivo o proyecto desde un portal o desde su computador local. En este caso vamos a cargar el proyecto previamente descargado en nuestro computador, buscamos la ubicación del archivo y lo cargamos. Alternativamente, si usa la opción portal, deberá conectar su cuenta con ArcGIS Online y activar este portal para tener acceso a los archivos tutoriales de Esri. Luego deberá usar la barra de búsqueda, buscar y cargar el proyecto *Introducing ArcGIS Pro*.

<p align="center">
<img src="../images/intro-arcgis/02_fig2.jpg" vspace="10" width="600">
</p>

4. Cuando el proyecto esté abierto, usted verá un mapa de Wellington, Nueva Zelanda. La ventana que contiene el mapa es la *vista de mapa*. La pestaña coloreada en la vista de mapa indica que esa pestaña está activa. El nombre de la vista es *Wellington City*.

    Hay otras vistas abiertas en el proyecto: el mapa de *Central Wellington*, la escena de *Central Wellington_3D*, y la capa *Central Wellington Layout*.

<p align="center">
<img src="../images/intro-arcgis/02_fig3.jpg" vspace="10" width="1000">
</p>

## Barra de herramientas

Arriba de la vista de mapa se encuentra la barra o cinta de herramientas (o *Ribbon*). Esta barra tiene un conjunto de pestañas base: **Maps**, **Insert**, **Analysis**, **View**, **Edit**, **Imagery**, **Share**, y **Help**, las cuales están siempre presentes cuando una vista de mapa esta activa. Cada pestaña tien su propio conjunto de herramientas, organizadas en grupos. La pestaña **Map** tiene herramientas para interactuar con el mapa. En la pestaña **Map**, la herrmienta **Explore** esta seleccionada dentro del grupo **Navigate**. 

En esta sección se usarán herramientas del grupo **Navigate**. La herramienta **Explore** permite mover y desplazarnos por el mapa, y leer información sobre los objectos de interés en el mapa.

<p align="center">
<img src="../images/intro-arcgis/02_fig4.png" vspace="10" width="700">
</p>

1. Seleccione la herramienta **Explore** y arrastre el mapa a un sitio diferente.

    Si arrastra el mapa muy rápido puede perder el sitio de partida. 

2. En la barra de herramientas, en la pestaña **Map**, haga click en **Bookmarks**. En la parte de **Wellington City Bookmarks** haga click en *Wellington*. Este le ayudará a volver a la vista de mapa inicial. Adicionalmente, puede crear un nuevo *bookmark* en otra posición del mapa si lo desea.

<p align="center">
<img src="../images/intro-arcgis/02_fig5.jpg" vspace="10" width="1000">
</p>

3. En el mapa, haga click dentro del área (*City Boundary*) de *Wellington* para obtener mas información acerca de este objeto. El área de la ciudad parpadeará y aparacerá una ventana con la información sobre la población de la ciudad.

<p align="center">
<img src="../images/intro-arcgis/02_fig6.png" vspace="10" width="700">
</p>

## Abrir y anclar paneles

A medida que se vaya trabajando en un proyecto veremos que a menudo se abriran y cerraran paneles que se necesitan para tareas específicas. Los paneles también se pueden minimizar con tal de dejar espacio disponible para trabajar con los mapas y otras vistas.

1. En la barra de herramientas, haga click en la pestaña **View**. En el grupo **Windows** haga click en **Reset Panes** y luego en **Reset Panes for Mapping (Default)**.

   Los paneles **Contents** y **Catalog** se abrirán (en caso de que hayan sido cerrados antes). Cualquier otro tipo de panel abierto será cerrado. Estos dos paneles pueden estar anclados en sitios opuestos de la ventana de la aplicación, lo cual es el diseño predeterminado.

<p align="center">
<img src="../images/intro-arcgis/02_fig7.jpg" vspace="10" width="1000">
</p>

Estos paneles pueden incluso ser colocados uno encima del otro, cada uno con una pestaña respectiva.
    
<p align="center">
<img src="../images/intro-arcgis/02_fig8.png" vspace="10" width="400">
</p>

2. Arrastre el panel **Catalog** de su barra sobre la vista de mapa. A medida que arrastre el panel (representado por una sombra azul), sitios de anclaje apareceran en el centro de la vista de mapa y en las orillas de la ventana de la aplicación. Cada sitio representa un area donde el panel puede ser posicionado.

<p align="center">
<img src="../images/intro-arcgis/02_fig9.png" vspace="10" width="400">
</p>

3. Posicione el panel en un sitio de anclaje sin soltar el click. Podrá observar como quedaría el panel posicionado, ya sea de manera horizontal o vertical, lo cual es representado con una sombra azul.

<p align="center">
<img src="../images/intro-arcgis/02_fig10.jpg" vspace="10" width="1000">
</p>

4. Suelte el panel en el sitio de anclaje. El panel mostrará su nueva posición. Si los paneles **Catalog** y **Contents** estaban agrupados antes, se mantendrán agrupados al intentar organizar o mover el panel a otro sitio.

<p align="center">
<img src="../images/intro-arcgis/02_fig11.jpg" vspace="11" width="1000">
</p>

5. Arrastre el panel **Catalog** a una nueva posición y sueltelo en cualquier otra parte de su pantalla que no sea una sitio de anclaje. Esto hará que el panel quede flotando. Puede re-ajustar su tamaño estirando una esquina o un lado del panel.

6. Si los paneles **Catalog** y **Contents** estan agrupados, haga click en la pestaña **Catalog** en la parte inferior del panel y arrastre el panel por su pestaña hacía una nueva posición. Ahora los paneles quedaran separados.

7. Suelte el panel **Contents** sobre el sitio de anclaje izquierdo. Suelte el panel **Catalog** sobre el sitio de anclaje derecho. Con esto los paneles estarán en posiciones opuestas. De manera predeterminada los paneles permanecerán abiertos mientras trabaja. Pero, se puede auto-esconder un panel para que no ocupe espacio en el area de trabajo que se este usando.

<p align="center">
<img src="../images/intro-arcgis/02_fig12.png" vspace="10" width="400">
</p>

8. Haga click en el panel **Contents** para tenerlo activo. Ahora, en la esquina superior derecha del panel, haga click en **Auto-Hide**. El panel se esconderá en el borde de la ventana de ArcGIS Pro donde el panel esta anclado.

<p align="center">
<img src="../images/intro-arcgis/02_fig13.png" vspace="10" width="400">
</p>

9. Haga click en el panel **Contents** que se encuentra escondido para restaurarlo. El panel se quedará abierto meintras usted est interactuando con él. Cuando seleccione otro panel, otra vista, o haga una acción diferente hará que el panel **Contents** se esconda nuevamente.

10. Haga click en **Auto-Hide** nuevamente para que el panel permanezca abierto.
