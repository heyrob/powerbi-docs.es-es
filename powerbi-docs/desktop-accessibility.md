---
title: Accesibilidad a informes de Power BI Desktop
description: Características y sugerencias para crear informes accesibles de Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 01/11/2019
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 54c842a91684eec1cf60eca4442592500d1bcb11
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "64770417"
---
# <a name="accessibility-in-power-bi-desktop-reports"></a>Accesibilidad a informes de Power BI Desktop
Power BI presenta características que permiten a las personas con discapacidades usar los informes de Power BI e interactuar con ellos con más facilidad. Estas características incluyen la capacidad de interactuar con el informe mediante el teclado o un lector de pantalla, la tabulación para centrar la atención en varios objetos de una página y el uso apropiado de marcadores en las visualizaciones.

![Uso de marcadores diferentes para gráficos de líneas y de áreas para mejorar la accesibilidad](media/desktop-accessibility/accessibility_01.png)

## <a name="consuming-a-power-bi-desktop-report-with-a-keyboard-or-screen-reader"></a>Interactuación con un informe de Power BI Desktop mediante un teclado o un lector de pantalla
A partir de la versión de septiembre de 2017 de **Power BI Desktop**, puede presionar la tecla **?** para mostrar una ventana que describe los métodos abreviados de teclado de accesibilidad disponibles en **Power BI Desktop**.

![Presione la tecla ? en Power BI Desktop para mostrar los métodos abreviados de teclado de accesibilidad](media/desktop-accessibility/accessibility_03.png)

Con las mejoras de accesibilidad, puede usar un informe de Power BI con un teclado o un lector de pantalla mediante las siguientes técnicas:

Al ver un informe, normalmente el modo de examen debería estar desactivado.

Puede cambiar el enfoque entre las pestañas de las páginas del informe o los objetos de la página de un informe determinada con las teclas **Ctrl+F6**.

* Cuando el enfoque recae en las *pestañas de páginas de informes*, use el *tabulador* o las teclas de *dirección* para cambiar el enfoque de la página de un informe a la siguiente. El lector de pantalla lee el título de la página del informe e identifica si dicha página está seleccionada actualmente. Para cargar la página del informe en la que recae el enfoque actualmente, use la tecla *ENTRAR* o la *barra espaciadora*.
* Si el enfoque recae en una *página del informe* cargada, use el *tabulador* para cambiar el enfoque a cada objeto de la página, que incluye todos los cuadros de texto, imágenes, formas y gráficos. El lector de pantalla lee el tipo de objeto, su título, si lo tiene, y una descripción de ese objeto, si el autor del informe la ha proporcionado. 

Al desplazarse entre objetos visuales puede presionar **Alt + Mayús + F10** para mover el foco al encabezado visual, que contiene distintas opciones, como ordenar, exportar los datos del gráfico y el modo de enfoque. 

![Presione Alt+Mayús+F10 en Power BI Desktop para mover el foco al encabezado del objeto visual](media/desktop-accessibility/accessibility_08.png)

Puede presionar **Alt + Mayús + F11** para presentar una versión accesible de la ventana *Mostrar datos*. Esto le permite explorar los datos usados en el objeto visual de una tabla HTML con los mismos métodos abreviados de teclado que se usan normalmente con el lector de pantalla. 

![Presione Alt + Mayús + F11 en Power BI Desktop para mostrar una ventana accesible Ver datos en un objeto visual](media/desktop-accessibility/accessibility_04.png)

> [!NOTE]
> La característica Mostrar datos solo es accesible mediante un lector de pantalla con este método abreviado de teclado. Si abre Mostrar datos con la opción del encabezado visual, no será accesible mediante un lector de pantalla. Al usar Mostrar datos, active el modo de examen para aprovechar las teclas de acceso rápido que proporciona el lector de pantalla.

A partir de la versión de **Power BI Desktop** de julio de 2018, las segmentaciones también tienen integrada la funcionalidad de accesibilidad. Cuando seleccione una segmentación, use CTRL+flecha derecha (tecla Control más la tecla de flecha derecha) para moverse por los distintos controles dentro de la segmentación. Por ejemplo, cuando presiona inicialmente CTRL+flecha derecha, el foco está en el borrador y presionar la barra espaciadora equivale a hacer clic en el botón del borrador, con lo que se borran todos los valores de la segmentación. 

Puede presionar la tecla TAB para desplazarse por los controles de una segmentación. Al presionar la tecla TAB cuando está en el borrador, se mueve al menú desplegable. Si vuelve a presionarla, pasa al primer valor de la segmentación (si hay varios valores para la segmentación, como un intervalo). 

![Presione CTRL+(tecla de flecha derecha) en Power BI Desktop para ajustar el elemento o los valores de una segmentación y presione ESPACIO para seleccionar el elemento y ajustar su valor.](media/desktop-accessibility/accessibility_07.png)

Estas incorporaciones de accesibilidad se han creado para que los usuarios puedan aprovechar en su totalidad los informes de Power BI mediante un lector de pantalla y la navegación con el teclado.

## <a name="tips-for-creating-accessible-reports"></a>Sugerencias para la creación de informes accesibles
Las siguientes sugerencias pueden ayudarlo a crear informes de **Power BI Desktop** que sean más accesibles.

### <a name="general-tips-for-accessible-reports"></a>Sugerencias generales para la creación de informes accesibles

* Para los objetos visuales de **línea**, **área** y **combinados**, al igual que para **Dispersión** y **Burbuja** active los marcadores y use una *forma de marcador* distinta para cada línea.
  
  * Para activar los *marcadores*, seleccione la sección **Formato** en el panel **Visualizaciones** y expanda la sección **Formas**; a continuación, desplácese hacia abajo para encontrar la opción de activación/desactivación de **Marcadores** y *actívela*.
  * A continuación, seleccione el nombre de cada línea (o de área, si usa un gráfico de **área**) en el cuadro de lista desplegable de la sección **Formas**. Debajo de la lista desplegable, puede ajustar muchos aspectos del marcador utilizado para la línea seleccionada, entre otros, su forma, color y tamaño.
  
  ![Uso de marcadores diferentes para gráficos de líneas y de áreas para mejorar la accesibilidad](media/desktop-accessibility/accessibility_01.png)
  
  * La utilización de una *forma de marcador* distinta para cada línea permite que los lectores del informe puedan diferenciar cada una de las líneas o áreas con más facilidad.
* Como continuación del punto anterior, no se base en el color para transmitir información. Además de usar formas en gráficos de líneas y de dispersión, no dependa del formato condicional para proporcionar información en tablas y matrices. 
* Elija un criterio de ordenación intencionado para cada objeto visual del informe. Cuando los usuarios de lectores de pantalla se desplacen por los datos del gráfico, elige el mismo criterio de ordenación que el del objeto visual.
* Seleccione un *tema* en la galería de temas con un alto contraste y un color apropiado para invidentes y, después, impórtelo en la [característica de versión preliminar **Temas**](desktop-report-themes.md).
* Proporcione *texto alternativo* para cada objeto de un informe. De esta forma, se asegura de que los usuarios del informe entienden lo que trata de comunicar con un objeto visual, incluso aunque ellos no puedan ver el objeto visual, la imagen, la forma o el cuadro de texto. Para proporcionar *texto alternativo* para cualquier objeto de un informe de **Power BI Desktop**, seleccione el objeto (como un objeto visual, una forma, etc.) y, en el panel **Visualizaciones**, seleccione la sección **Formato**, expanda **General**, desplácese hacia abajo y rellene el cuadro de texto **Texto alternativo**.
  
  ![El texto alternativo para cualquier objeto de un informe se puede agregar en Visualizaciones > Formato > General > cuadro Texto alternativo.](media/desktop-accessibility/accessibility_02.png)
* Asegúrese de que los informes tengan suficiente contraste entre el texto y los colores de fondo. Hay varias herramientas, como [Colour Contrast Analyser](https://developer.paciellogroup.com/resources/contrastanalyser/), que se pueden usar para comprobar los colores del informe. 
* Use tamaños de texto y fuentes que sean fácilmente legibles. El texto o las fuentes de pequeño tamaño podrían ser difíciles de leer y poco prácticos de cara a la accesibilidad.
* Incluya un título, etiquetas de eje y etiquetas de datos en todos los objetos visuales.
* Use títulos significativos para todas las páginas del informe.
* Si es posible, evite formas e imágenes decorativas en el informe, ya que se incluyen en el orden de tabulación de este. Si necesita incluir objetos decorativos en el informe, actualice el texto alternativo de este para indicar a los usuarios de lectores de pantalla que tienen uso decorativo.

### <a name="arranging-items-in-field-buckets"></a>Organización de elementos en depósitos por Campo
A partir de la versión de octubre de 2018 de **Power BI Desktop**, el depósito **Campos** es accesible con un teclado e interactúa con los lectores de pantalla. 

Para mejorar el proceso de creación de informes con los lectores de pantalla, hay disponible un menú contextual para permitir el movimiento de los campos en el depósito hacia arriba o hacia abajo en la lista **Campos**, o el traslado del campo a otros depósitos, como **Leyenda**, **Valor** u otros.

![El menú contextual de Campos también le permite mover los campos hacia arriba, hacia abajo o a otra área.](media/desktop-accessibility/accessibility_09.png)

## <a name="high-contrast-support-for-reports"></a>Compatibilidad con el contraste alto en los informes

Al usar los modos de contraste alto en Windows, esta configuración y la paleta que seleccione también se aplicarán a los informes de **Power BI Desktop**. 

![Configuración de Windows de contraste alto](media/desktop-accessibility/accessibility_05.png)

**Power BI Desktop** detecta automáticamente el tema de contraste alto que se usa en Windows y aplica esta configuración a los informes. Los colores de contraste alto siguen el informe a la hora de publicarlo en el servicio Power BI o en otro lugar.

![Configuración de Windows de contraste alto](media/desktop-accessibility/accessibility_05b.png)

El servicio Power BI también intenta detectar la configuración de contraste alto seleccionada para Windows, pero el grado de eficacia y de precisión de esa detección dependerá del explorador usado en el servicio Power BI. Si quiere establecer el tema manualmente en el servicio Power BI, puede seleccionar **Vista > Colores de alto contraste** y, después, seleccionar el tema que quiere aplicar al informe.

![Configuración del contraste alto en el servicio Power BI](media/desktop-accessibility/accessibility_06.png)

Cuando esté en **Power BI Desktop** se percatará de que algunas áreas, como los campos **Visualizaciones** y **Campos**, no reflejan la selección de combinaciones de colores de contraste alto de Windows.


## <a name="considerations-and-limitations"></a>Consideraciones y limitaciones
Hay algunos problemas conocidos y limitaciones con las características de accesibilidad, que se describen en la lista siguiente:

* Cuando se usan lectores de pantalla con **Power BI Desktop**, se obtiene una experiencia óptima si se abre el lector de pantalla preferido antes de abrir cualquier archivo en Power BI Desktop.
* Si usa Narrador, existen algunas limitaciones en cuanto al desplazamiento por Mostrar datos como una tabla HTML.

## <a name="keyboard-shortcuts"></a>Métodos abreviados de teclado
Los métodos abreviados de teclado son útiles para desplazarse por los informes de Power BI mediante un teclado. En las tablas siguientes se describen los métodos abreviados disponibles en un informe de Power BI. Además de usar estos métodos abreviados de teclado en Power BI Desktop, también funcionan en las siguientes experiencias:

* Cuadro de diálogo del explorador de preguntas y respuestas
* Cuadro de diálogo de introducción
* Menú Archivo y cuadro de diálogo Acerca de
* Barra de advertencia
* Cuadro de diálogo Restauración de archivos
* Cuadro de diálogo de desaprobaciones

En nuestro continuo esfuerzo por mejorar la accesibilidad, la lista anterior de experiencias también admiten lectores de pantalla y configuración de contraste alto.


### <a name="frequently-used-shortcuts"></a>Métodos abreviados de uso frecuente
| Para hacerlo           | Presione                |
| :------------------- | :------------------- |
| Mover el foco entre secciones  | Ctrl + F6 |
| Mover el foco hacia adelante en la sección | Tab         |
| Mover el foco hacia atrás en la sección | Mayús + Tabulador |
| Seleccionar o anular la selección de un objeto | Entrar o Espacio |
| Seleccionar varios objetos | Ctrl + Espacio |

### <a name="on-visual"></a>Sobre el objeto visual
| Para hacerlo           | Presione                |
| :------------------- | :------------------- |
| Mover el foco al menú de objetos visuales | Alt + Mayús + F10 |
| Mostrar datos | Alt + Mayús + F11  |
| Especificar un objeto visual | Ctrl + flecha derecha |
| Especificar una capa | Especificar |
| Salir de una capa o un objeto visual | Esc |
| Seleccionar o anular la selección de un punto de datos | Entrar o Espacio |
| Selección múltiple | Ctrl + Entrar o Ctrl + Espacio |
| Clic con el botón derecho | <ul><li>Teclado de Windows: tecla de contexto de Windows + F10.  La clave de contexto de Windows está entre la tecla Alt de la izquierda y la tecla de flecha izquierda.</li><li>Otro teclado: Mayús+F10</li></ul> |
| Borrar selección | Control + Mayús + C |

### <a name="table--matrix-navigation"></a>Tabla de & navegación de la matriz
| Para hacerlo           | Presione                |
| :------------------- | :------------------- |
| Mover el foco arriba o hacia abajo una celda (a través de todas las celdas en todas las áreas)  | Flecha key / presionada la tecla de flecha arriba |
| Mover el foco hacia la izquierda / derecha de una celda (a través de todas las celdas en todas las áreas)  | Tecla de flecha izquierda / tecla de dirección derecha |

### <a name="pane-navigation"></a>Navegación por el panel
| Para hacerlo           | Presione                |
| :------------------- | :------------------- |
| Selección múltiple | Ctrl + Espacio |
| Contraer una sola tabla | Tecla Flecha izquierda |
| Expandir una sola tabla | Tecla Flecha derecha |
| Contraer todas las tablas | Alt + Mayús + 1 |
| Expandir todas las tablas | Alt + Mayús + 9 |
| Abrir un menú contextual | <ul><li>Teclado de Windows: tecla de contexto de Windows + F10.  La clave de contexto de Windows está entre la tecla Alt de la izquierda y la tecla de flecha izquierda.</li><li>Otro teclado: Mayús+F10</li></ul> |

### <a name="slicer"></a>Segmentación
| Para hacerlo           | Presione                |
| :------------------- | :------------------- |
| Interactuar con una segmentación | Ctrl + tecla de flecha derecha |

### <a name="selection-pane"></a>Panel Selección
| Para hacerlo           | Presione                |
| :------------------- | :------------------- |
| Activar panel de selección | F6 |
| Mover un objeto hacia arriba en la disposición en capas | Ctrl + Mayús + F |
| Mover un objeto hacia abajo en la disposición en capas | Ctrl + Mayús + B |
| Ocultar o mostrar (alternar) un objeto | Ctrl + Mayús + S |

### <a name="dax-editor"></a>Editor DAX
| Para hacerlo           | Presione                |
| :------------------- | :------------------- |
| Subir o bajar una línea | Alt + tecla de flecha arriba o abajo |
| Copiar línea arriba o abajo | Mayús + Alt + tecla de flecha arriba o abajo |
| Insertar línea debajo | Ctrl + Entrar |
| Insertar línea encima | Ctrl + Shift + Entrar |
| Saltar al corchete correspondiente | Ctrl + Mayús + \ |
| Aplicar sangría o anular la sangría de la línea | Ctrl + ] / [ |
| Insertar cursor | Alt + clic |
| Seleccionar la línea actual | Ctrl + I |
| Seleccionar todas las apariciones de la selección actual | Ctrl + Mayús + L |
| Seleccionar todas las apariciones de la palabra actual | Ctrl + F2 |

### <a name="enter-data"></a>Especificar datos
| Para hacerlo           | Presione                |
| :------------------- | :------------------- |
| Salir de la cuadrícula editable | Ctrl + Tab |


## <a name="next-steps"></a>Pasos siguientes
* [Uso de los temas para los informes en Power BI Desktop (versión preliminar)](desktop-report-themes.md)

