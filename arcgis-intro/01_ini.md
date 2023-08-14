---
layout: page
title: Introducción
parent: ArcGIS Pro Introducción
nav_order: 1
---

# Introducción

Este material está basado en ArcGIS Pro 3.1 y usa algunos recursos de la [guía rápida](https://pro.arcgis.com/en/pro-app/latest/get-started/get-started.htm) a ArcGIS Pro de ESRI.

ArcGIS Pro es una aplicación profesional de SIG (Sistemas de Información Geográfica) propiedad de ESRI. Con ArcGIS Pro se puede explorar, visualizar, analizar datos, crear mapas 2D y 3D, compartir proyectos con ArcGIS Online
o su portal de ArcGIS Enterprise. En las siguientes secciones se introducirá el proceso de ingreso, la página de inicio, ArcGIS Pro projects, y la interfaz de usuario.

## Ingresar / Registro

La primera vez que use ArcGIS Pro, se requerirá ingresar con su credencial de ArcGIS Online, ArcGIS Enterprise, o ESRI. Si aún no tiene una cuenta puede crear una [aquí](https://goto.arcgis.com/production-esri-signup) gratuitamente usando la opción de prueba de 21 días. Si posee una licencia de uso puede registrarla al momento de usar el programa por primera vez.

<p align="center">
<img src="../images/intro-arcgis/01_fig1.png" vspace="10" width="600">
</p>

## Página de inicio

### Pestaña Home

Por defecto, ArcGIS Pro abre en la página de inicio. La página de inicio tiene una pestaña de "**Home**", una pestaña de "**Learning Resources**", y una pestaña de "**Settings**". En la pestaña **Home** se pueden encontrar las siguientes opciones para empezar un nuevo proyecto:

<p align="center">
<img src="../images/intro-arcgis/01_fig2.png" vspace="10" width="1000">
</p>

|    Elemento   |                       Descripción                                                                  |
|:-------------:|:--------------------------------------------------------------------------------------------------:|
| 1             | Plantillas predeterminadas para empezar un nuevo proyecto                                          |
| 2             | Proyectos recientes. Para abrir un proyecto que no esta en la lista, haga click en "**Open another project**" |
| 3             | Haga click en vista tipo **List** o **Tile** para mostrar proyectos de acuerdo a sus preferencias  |
| 4             | Haga click para cargar una plantilla reciente y empezar un nuevo proyecto desde esa plantilla predeterminada. Para empezar un proyecto desde una plantilla que no este en la lista, haga click en **Start with another template** |


### Recursos de aprendizaje

En la pestaña de **Learning Resources** puede encontrar recursos que le ayudaran a desarrollar habilidades, resolver problemas, y responder preguntas. Los recursos de aprendizaje también se pueden acceder desde una pestaña lateral en la página de **Settings** o desde el botón **Learning Resources** en la pestaña de **Help** en la barra de herramientas.

<p align="center">
<img src="../images/intro-arcgis/01_fig3.png" vspace="10" width="1000">
</p>

|    Elemento   |                       Descripción                                                                  |
|:-------------:|:--------------------------------------------------------------------------------------------------:|
| 1             | Tutoriales rápidos para aprender las funciones y procesos básicos de ArcGIS Pro                    |
| 2             | Acceder a la documentación del producto, materiales de aprendizaje, entrenamientos, noticias, y el sitio de la *Comunidad Esri* |
| 3             | Serie de tutoriales que presentan materiales de aprendizaje relacionados con un área de práctica  |
| 4             | Recursos disponibles para ayudar los usuarios de ArcMap a aprender ArcGIS Pro |


### Configuraciones

En la pestaña **Settings** se puede configurar y manejar la aplicación. En un proyecto abierto, las configuraciones son accesibles desde la pestaña **Project** en la barra de herramientas.

<p align="center">
<img src="../images/intro-arcgis/01_fig4.png" vspace="10" width="800">
</p>

|    Pestaña        |                       Descripción                                                                  |
|:-----------------:|:--------------------------------------------------------------------------------------------------:|
| New               | Crea un proyecto                    |
| Open              | Abre un proyecto existente |
| Info              | Ver información del proyecto actual  |
| Save Project      | Guardar proyecto actual |
| Save Project As   | Guardar una copia del archivo de proyecto actual (.aprx) |
| Portals           | Manejar la conexión a un portal y activar portal |
| Licensing         | Ver información de licencia, autorizar a ArcGIS Pro trabajar offline, y cambiar tipo de licencia |
| Options           | Acceder a un proyecto y opciones para configurar ArcGIS Pro |
| Package Manager   | Manejar paquetes y ambientes de Python, R, y librerías del sistema |
| Add-In Manager    | Instalar "add-ins" o complementos para personalizar la aplicación |
| Help              | Abrir la ayuda online u offline del sistema |
| About             | Ver información sobre su versión de ArcGIS Pro y actualizar a la última versión |
| Learning Resources| Acceder a los tutoriales rápidos, series de tutoriales, y otros recursos de aprendizaje |
| Exit              | Cerrar la aplicación |


## Proyectos

En ArcGIS Pro , un proyecto es una estructura de trabajo relacionada con mapas, escenas, capas, y otros recursos conectados como bases de datos y carpetas de sistema. Los archivos de proyecto tiene la extension **.aprx**. Por defecto, un proyecto es almacenado en su propia carpeta junto con archivos de geodatabase asociados y barras de herramientas. 

<p align="center">
<img src="../images/intro-arcgis/01_fig5.png" vspace="10" width="800">
</p>

## Interfaz de Usuario

Las partes principales de la interfaz de ArcGIS Pro son la barra de herramientas (o Ribbon), vistas, y paneles. A continuación veremos una descripción de cada una de estas partes.

### Barra de Herramientas (*Ribbon*)

Esta es una cinta horizontal en la parte superior de la ventana de trabajo dentro de la aplicación, la cual presenta una serie de pestañas con diferentes opciones y funciones. Algunas pestañas (pestañas base) estan siempre presentes. Otras (pestañas contextuales) aparecen cuando la aplicación esta en un estado particular. Por ejemplo, la pestaña contextual **Feature Layer** aparece cuando una capa es seleccionada en los contenidos del panel de un mapa. 

<p align="center">
<img src="../images/intro-arcgis/01_fig6.png" vspace="10" width="800">
</p>

|    Elemento       |                       Descripción                                                                  |
|:-----------------:|:--------------------------------------------------------------------------------------------------:|
| 1                 | La *barra de acceso rápido* tiene comandos que se usan a menudo.         |
| 2                 | Nombre de proyecto en la parte superior de la aplicación       |
| 3                 | El comando de búsqueda *Search* ayuda a encontrar y correr comandos  |
| 4                 | Pestañas base, tales como la pestaña **Map**. Cuando es seleccionada muestra sus botones y funciones asociados |
| 5                 | Pestañas contextuales, como la pestaña **Tile Layer**, las cuales aparecen en momentos apropiados para su uso |
| 6                 | Botones y herramientas para correr comandos. Por ejemplo, la herramienta **Explore** sirve para navegar en mapas e identificar objetos en mapas.  |
| 7                 | Caja de diálogo que abre paneles o cajas de diálogos con más funciones |
| 8                 | Agrupación de comandos relacionados y organizados en la barra  |


### Vistas

### Paneles

## Organización de la Interfaz de Usuario
