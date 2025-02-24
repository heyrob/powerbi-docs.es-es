---
title: Gráficos de dispersión de alta densidad en Power BI
description: Gráficos de dispersión de alta densidad en Power BI
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 928e93c724a47f48aff1f87ee51f9a8c907774d6
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "65454277"
---
# <a name="high-density-sampling-in-power-bi-scatter-charts"></a>Muestreo de alta densidad en los gráficos de dispersión de Power BI
Desde la versión de septiembre de 2017 de **Power BI Desktop** y las actualizaciones del **servicio Power BI**, hay disponible un nuevo algoritmo de muestreo que mejora cómo se representan los datos de alta densidad en los gráficos de dispersión.

Por ejemplo, podría crear un gráfico de dispersión de la actividad de ventas de la organización, cada almacén con decenas de miles de puntos de datos de cada año. Un gráfico de dispersión de dicha información realizará un muestreo de los datos (seleccionando una representación significativa de los datos para ilustrar cómo se producen las ventas a través del tiempo) a partir de los datos disponibles y creará un gráfico de dispersión que representa los datos subyacentes. Esta es una práctica habitual en los gráficos de dispersión de alta densidad. Power BI ha mejorado el muestreo de datos de alta densidad, cuyos detalles se describen en este artículo.

![](media/desktop-high-density-scatter-charts/high-density-scatter-charts_01.png)

> [!NOTE]
> El algoritmo de **muestreo de alta densidad** que se describe en este artículo está disponible en los gráficos de dispersión, tanto para **Power BI Desktop** como para el **servicio Power BI**.
> 
> 

## <a name="how-high-density-scatter-charts-work"></a>Modo de funcionamiento de los gráficos de dispersión de alta densidad
Anteriormente, **Power BI** seleccionaba una colección de puntos de datos de muestra en el intervalo completo de datos subyacentes de manera determinista para crear un gráfico de dispersión. En concreto, Power BI seleccionaría la primera y última fila de datos de la serie del gráfico de dispersión y a continuación dividiría las filas restantes uniformemente para representar un total de 3500 puntos de datos en el gráfico de dispersión. Por ejemplo, si la muestra tiene 35 000 filas, se seleccionan la primera y la última fila para trazar, y se traza cada décima fila (35 000/10 = cada décima fila = 3500 puntos de datos). Anteriormente, los valores NULL o los puntos que no se podían trazar (por ejemplo, los valores de texto) de la serie de datos no se mostraban y, por tanto, no se tenían en cuenta al generar el objeto visual. Con este tipo de muestreo, la densidad percibida del gráfico de dispersión también se basaba en los puntos de datos representativos y, por tanto, la densidad visual implícita era una circunstancia de los puntos de la muestra y no de la colección completa de los datos subyacentes.

Al habilitar **muestreo de alta densidad**, Power BI implementa un algoritmo que elimina los puntos que se superponen y se asegura de que se pueden acceder los puntos en el objeto visual al interactuar con el objeto visual. El algoritmo también garantiza que todos los puntos del conjunto de datos se representan en el objeto visual, lo que proporciona contexto para el significado de los puntos seleccionados, en lugar de simplemente trazar una muestra representativa.

Por definición, se muestrean los datos de alta densidad para crear visualizaciones de forma razonablemente rápida que responden a interactividad. Si hay demasiados puntos de datos en un objeto visual pueden provocar que se ralentice y disminuya la visibilidad de las tendencias. Por eso, la forma en la que se muestrean los datos es lo que impulsa la creación del algoritmo de muestreo, para proporcionar la mejor experiencia de visualización y asegurarse de que todos los datos están representados. En Power BI, el algoritmo se ha mejorado para proporcionar la mejor combinación de capacidad de respuesta, representación y conservación de los puntos importantes en el conjunto de datos.

> [!NOTE]
> Los gráficos de dispersión que usan el algoritmo de **muestreo de alta densidad** se trazan mejor en objetos visuales cuadrados, al igual que ocurre con todos los gráficos de dispersión.
> 
> 

## <a name="how-the-new-scatter-chart-sampling-algorithm-works"></a>Modo de funcionamiento del nuevo algoritmo de muestreo de gráficos de dispersión
El nuevo algoritmo para **muestreo de alta densidad** para gráficos de dispersión emplea métodos que capturan y representan los datos subyacentes de forma más eficaz y elimina los puntos superpuestos. Lo hace comenzando con un radio pequeño para cada punto de datos (el tamaño del círculo visual de un punto dado en la visualización). A continuación, aumenta el radio de todos los puntos de datos; cuando se superponen dos (o más) puntos de datos, un círculo único (con el tamaño del radio aumentado) representa los puntos de datos superpuestos. El algoritmo continúa aumentando el radio de los puntos de datos hasta que dicho valor del radio da como resultado un número razonable de puntos de datos (3500) para mostrar en el gráfico de dispersión.

Los métodos de este algoritmo garantizan que los valores atípicos se representarán en el objeto visual resultante. El algoritmo también respeta la escala a la hora de determinar la superposición, de modo que se visualicen las escalas exponenciales con fidelidad en los puntos visualizados subyacentes.

El algoritmo también conserva la forma general del gráfico de dispersión.

> [!NOTE]
> Cuando se usa el algoritmo de **muestreo de alta densidad** para gráficos de dispersión, la *distribución precisa* de los datos es el objetivo y la densidad visual implícita *no* es el objetivo. Por ejemplo, podría ver un gráfico de dispersión con una gran cantidad de círculos que se superponen (densidad) en un área concreta e imaginar que muchos puntos de datos deben estar agrupados ahí; puesto que el algoritmo de **muestreo de alta densidad** puede usar un círculo para representar muchos puntos de datos, tal densidad visual implícita (o "agrupación") no se mostrará. Para obtener más detalles de una zona determinada, puede utilizar controles deslizantes para acercar la vista.
> 
> 

Además, se omiten los puntos de datos que no se pueden trazar (por ejemplo, los valores NULL o valores de texto), por lo que se selecciona otro valor que se puede trazar para garantizar aún más que la forma real del gráfico de dispersión se mantenga.

### <a name="when-the-standard-algorithm-for-scatter-charts-is-used"></a>Cuándo se usa el algoritmo estándar para los gráficos de dispersión
Hay circunstancias en las que **muestreo de alta densidad** no puede aplicarse a un gráfico de dispersión y el original se usa el algoritmo. Dichas circunstancias son las siguientes:

* Si hace clic con el botón derecho en un valor en **Detalles** y lo establece en **Mostrar elementos sin datos** en el menú, el gráfico de dispersión volverá al algoritmo original.
  
  ![](media/desktop-high-density-scatter-charts/high-density-scatter-charts_02.png)
* Cualquier valor en el eje **Reproducir** dará como resultado que el gráfico de dispersión vuelva al algoritmo original.
* Si faltan los ejes X e Y en un gráfico de dispersión, el gráfico vuelve al algoritmo original.
* El uso de una **línea de relación** en el panel **Análisis** hace que el gráfico se revierte al algoritmo original.
  
  ![](media/desktop-high-density-scatter-charts/high-density-scatter-charts_03.png)

## <a name="how-to-turn-on-high-density-sampling-for-a-scatter-chart"></a>Activación del muestreo de alta densidad para un gráfico de dispersión
Para activar **muestreo de alta densidad**, seleccione un gráfico de dispersión, vaya a la **formato** panel, expanda el **General** tarjeta y la parte inferior de la tarjeta, deslice el **Muestreo de alta densidad** activar o desactivar el control deslizante para **en**.

![](media/desktop-high-density-scatter-charts/high-density-scatter-charts_04.png)

> [!NOTE]
> Una vez que el control deslizante está activado, Power BI intentará usar el algoritmo de **muestreo de alta densidad** siempre que sea posible. Cuando el algoritmo no se puede usar (por ejemplo, si se coloca un valor en el eje *Reproducir*), el control deslizante permanece en la posición **Activado** aunque el gráfico se haya revertido al algoritmo estándar. Si después quita un valor del eje *Reproducir* (o cambian las condiciones para habilitar el uso del algoritmo de muestreo de alta densidad), el gráfico usará automáticamente el muestreo de alta densidad para ese gráfico porque la característica está activa.
> 
> [!NOTE]
> Los puntos de datos se agrupan o se seleccionan por el índice. Tener una leyenda no afecta al muestreo para el algoritmo, solo afecta a la ordenación del objeto visual.
> 
> 

## <a name="considerations-and-limitations"></a>Consideraciones y limitaciones
El algoritmo de muestreo de alta densidad es una mejora importante en Power BI, pero hay algunas consideraciones que debe conocer a la hora de trabajar con valores de alta densidad y gráficos de dispersión.

* El **muestreo de alta densidad** algoritmo solo funciona con conexiones dinámicas a modelos basados en servicios de Power BI, modelos importados o DirectQuery.

## <a name="next-steps"></a>Pasos siguientes
Para más información sobre el muestreo de alta densidad en otros tipos de gráficos, vea el artículo siguiente.

* [Muestreo de líneas de alta densidad en Power BI](desktop-high-density-sampling.md)

