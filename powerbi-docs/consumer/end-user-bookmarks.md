---
title: Información general de los marcadores en los informes del servicio de Power BI
description: Tema de información general de la documentación acerca de las consultas en lenguaje natural de Preguntas y respuestas de Power BI.
author: mihart
manager: kvivek
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 05/10/2019
ms.author: mihart
LocalizationGroup: Create reports
ms.openlocfilehash: 55fafb00135908dc4f82151b96ed04d2cf2568da
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "65608308"
---
# <a name="what-are-bookmarks"></a>¿Cuáles son los marcadores?
Marcadores capturan la vista configurada actualmente de una página del informe, incluidos los filtros, las segmentaciones de datos y el estado de los objetos visuales. Cuando se selecciona un marcador, Power BI le devuelve a esa vista. Hay dos tipos de marcadores: aquellos cree usted mismo y aquellos creados por el informe *diseñadores*.

## <a name="use-bookmarks-to-share-insights-and-build-stories-in-power-bi"></a>Uso de marcadores para compartir información detallada y crear historias en Power BI 
Hay muchos usos para marcadores. Supongamos que descubre información interesante y desea mantenerlos: crear un marcador para poder regresar más adelante. Debe dejar y desea conservar el trabajo actual, cree un marcador. Incluso puede crear un marcador en la vista predeterminada del informe, por lo que cada vez que se devuelven, que se abre en primer lugar la vista de página del informe. 

También puede crear una colección de marcadores, organizarlos en el orden que desee y, posteriormente, recorrer cada marcador en una presentación para resaltar una serie de informaciones que contar una historia.  

![Mostrar panel Marcadores seleccionándolo en la cinta de opciones.](media/end-user-bookmarks/power-bi-bookmarks-pane.png)

## <a name="using-bookmarks"></a>Uso de marcadores
Para abrir el panel marcadores, seleccione **marcadores** desde la barra de menús. Para volver a la vista original publicada del informe, seleccione **Restablecer valores predeterminados**.

### <a name="report-bookmarks"></a>Informar de marcadores
Si el informe *diseñador* incluye marcadores de informe, encontrará en el **notificar marcadores** encabezado. 

![Mostrar marcadores de informe.](media/end-user-bookmarks/power-bi-report-bookmark.png)

Seleccione un marcador para cambiar a esa vista de informe. 

![Vídeo que muestra el informe de marcadores que se selecciona.](media/end-user-bookmarks/power-bi-bookmarks.gif)

### <a name="personal-bookmarks"></a>Marcadores personales

Cuando crea un marcador, los siguientes elementos se guardan con él:

* La página actual
* Filtros
* Segmentaciones de datos, incluidos el tipo de segmentación de datos (por ejemplo, menú desplegable o lista) y el estado de la segmentación de datos
* Estado de selección del objeto visual (por ejemplo, los filtros de resaltado cruzado)
* Criterio de ordenación
* Ubicación de exploración
* Visibilidad (de un objeto, mediante el panel **Selección**)
* Los modos de enfoque o de **Destacados** de cualquier objeto visible

Configure una página de informe de la forma en que desee que aparezca en el marcador. Una vez que la página del informe y los objetos visuales estén organizados a su gusto, seleccione **Agregar** en el panel **Marcadores** para agregar un marcador. En este ejemplo, hemos agregado algunos filtros de fecha y región. 

![Agregar marcadores Personal.](media/end-user-bookmarks/power-bi-add-personal.png)

**Power BI** crea un marcador y le da un nombre genérico o un nombre que especifique. También puede *cambiar el nombre de*, *eliminar*, o *actualizar* un marcador, seleccione el botón de puntos suspensivos situado junto al nombre del marcador y luego seleccione una acción en el menú que aparece.

Una vez que tenga un marcador, puede mostrarlo simplemente seleccionando el marcador en el **marcadores** panel. 

![Agregar marcadores Personal.](media/end-user-bookmarks/power-bi-personal-bookmark.png)


<!--
## Arranging bookmarks
As you create bookmarks, you might find that the order in which you create them isn't necessarily the same order you'd like to present them to your audience. No problem, you can easily rearrange the order of bookmarks.

In the **Bookmarks** pane, simply drag-and-drop bookmarks to change their order, as shown in the following image. The yellow bar between bookmarks designates where the dragged bookmark will be placed.

![Change bookmark order by drag-and-drop](media/desktop-bookmarks/bookmarks_06.png)

The order of your bookmarks can become important when you use the **View** feature of bookmarks, as described in the next section. 

-->

## <a name="bookmarks-as-a-slide-show"></a>Marcadores como una presentación con diapositivas
Para presentar o ver los marcadores, en orden, seleccione **vista** desde el **marcadores** panel para empezar una presentación.

Cuando está en el modo **Vista**, hay algunas características a tener en cuenta:

1. El nombre del marcador aparece en la barra de título de este, la cual, a su vez, aparece en la parte inferior del lienzo.
2. La barra de título del marcador tiene flechas que le permiten moverse al marcador siguiente o al anterior.
3. Puede salir del modo **Vista** seleccionando **Salir** en el panel **Marcadores** o la **X** que se encuentra en la barra de título del marcador. 

![Presentación de marcador](media/end-user-bookmarks/power-bi-bookmark-slideshow.png)

Cuando está en modo **Vista**, puede cerrar el panel **Marcadores** (haciendo clic en la X en ese panel) para proporcionar más espacio para la presentación. Siempre que esté en el modo **Vista**, todos los objetos visuales serán interactivos y estarán disponibles para realizar el resaltado cruzado, al igual que lo estarían en caso contrario si interactúa con ellos. 

<!--
## Visibility - using the Selection pane
With the release of bookmarks, the new **Selection** pane is also introduced. The **Selection** pane provides a list of all objects on the current page and allows you to select the object and specify whether a given object is visible. 

![Enable the Selection pane](media/desktop-bookmarks/bookmarks_08.png)

You can select an object using the **Selection** pane. Also, you can toggle whether the object is currently visible by clicking the eye icon to the right of the visual. 

![Selection pane](media/desktop-bookmarks/bookmarks_09.png)

When a bookmark is added, the visible status of each object is also saved based on its setting in the **Selection** pane. 

It's important to note that **slicers** continue to filter a report page, regardless of whether they are visible. As such, you can create many different bookmarks, with different slicer settings, and make a single report page appear very different (and highlight different insights) in various bookmarks.


## Bookmarks for shapes and images
You can also link shapes and images to bookmarks. With this feature, when you click on an object, it will show the bookmark associated with that object. This can be especially useful when working with buttons; you can learn more by reading the article about [using buttons in Power BI](desktop-buttons.md). 

To assign a bookmark to an object, select the object, then expand the **Action** section from the **Format Shape** pane, as shown in the following image.

![Add bookmark link to an object](media/desktop-bookmarks/bookmarks_10.png)

Once you turn the **Action** slider to **On** you can select whether the object is a back button, a bookmark, or a Q&A command. If you select bookmark, you can then select which of your bookmarks the object is linked to.

There are all sorts of interesting things you can do with object-linked bookmarking. You can create a visual table of contents on your report page, or you can provide different views (such as visual types) of the same information, just by clicking on an object.

When you are in editing mode you can use ctrl+click to follow the link, and when not in edit mode, simply click the object to follow the link. 


## Bookmark groups

Beginning with the August 2018 release of **Power BI Desktop**, you can create and use bookmark groups. A bookmark group is a collection of bookmarks that you specify, which can be shown and organized as a group. 

To create a bookmark group, hold down the CTRL key and select the bookmarks you want to include in the group, then click the ellipses beside any of the selected bookmarks, and select **Group** from the menu that appears.

![Create a bookmark group](media/desktop-bookmarks/bookmarks_15.png)

**Power BI Desktop** automatically names the group *Group 1*. Fortunately, you can just double-click on the name and rename it to whatever you want.

![Rename a bookmark group](media/desktop-bookmarks/bookmarks_16.png)

With any bookmark group, clicking on the bookmark group's name only expands or collapses the group of bookmarks, and does not represent a bookmark by itself. 

When using the **View** feature of bookmarks, the following applies:

* If the selected bookmark is in a group when you select **View** from bookmarks, only the bookmarks *in that group* are shown in the viewing session. 

* If the selected bookmark is not in a group, or is on the top level (such as the name of a bookmark group), then all bookmarks for the entire report are played, including bookmarks in any group. 

To ungroup bookmarks, just select any bookmark in a group, click the ellipses, and then select **Ungroup** from the menu that appears. 

![Ungroup a bookmark group](media/desktop-bookmarks/bookmarks_17.png)

Note that selecting **Ungroup** for any bookmark from a group takes all bookmarks out of the group (it deletes the group, but not the bookmarks themselves). So to remove a single bookmark from a group, you need to **Ungroup** any member from that group, which deletes the grouping, then select the members you want in the new group (using CTRL and clicking each bookmark), and select **Group** again. 
-->





## <a name="limitations-and-considerations"></a>Limitaciones y consideraciones
En esta versión de los **marcadores** hay algunas limitaciones y consideraciones que debe tener en cuenta.

* La mayoría de objetos visuales personalizados deben funcionar bien con marcadores. Si experimenta problemas con marcadores y un objeto visual personalizado, póngase en contacto con el creador de ese objeto visual personalizado y pídale que haga los marcadores compatibles con su objeto visual. 
* Si agrega un objeto visual en una página de informe después de crear un marcador, se mostrará el objeto visual en su estado predeterminado. Esto también significa que si se introduce una segmentación de datos en una página en la que previamente creó marcadores, la segmentación de datos se comportará según su estado predeterminado.
* Si se desplaza por los objetos visuales después de haber creado un marcador se reflejará en este. 
* Por lo general, los marcadores no se verán afectados si el informe *diseñador* actualiza o vuelve a publicar el informe. Sin embargo, si el diseñador realiza cambios significativos en el informe, como la eliminación de los campos que usa un marcador y, a continuación, recibirá un mensaje de error la próxima vez que intenta abrir ese marcador. 

<!--
## Next steps
spotlight?
-->
