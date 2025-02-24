---
title: Supervisar las métricas de uso de paneles e informes
description: Cómo ver, guardar y utilizar las métricas de uso para los informes y paneles de Power BI.
author: maggiesMSFT
ms.author: maggies
manager: kfile
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 12/19/2018
LocalizationGroup: Dashboards
ms.openlocfilehash: 55415126ae4c87381f788729f6f4b23807ac6572
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "61401152"
---
# <a name="monitor-usage-metrics-for-power-bi-dashboards-and-reports"></a>Supervisar las métricas de uso de paneles e informes de Power BI

Si desea crear paneles e informes, las métricas de uso le ayudan a conocer su impacto. Al ejecutar métricas de uso de panel o métricas de uso de informe, verá cómo se usan estos paneles e informes en toda la organización; qué es lo que se está utilizando, por quién y con qué finalidad.  

> [!NOTE]
> Las métricas de uso hacen un seguimiento del uso de los informes que se insertan en SharePoint Online. Sin embargo, no hacen un seguimiento de los paneles e informes insertados mediante el flujo "el usuario posee las credenciales" o "la aplicación posee las credenciales". Las métricas de uso no hacen un seguimiento del uso de los informes insertados mediante [Publicar en la Web](service-publish-to-web.md).

Estos informes de métricas de uso son de solo lectura. Sin embargo, puede personalizar un informe de métricas de uso mediante la opción "Guardar como". Se crea un conjunto de datos y el informe de solo lectura se convierte en un informe de Power BI con todas las características, que puede editar. No solo el informe personalizado contiene métricas para el panel o el informe seleccionado, sino que al quitar el filtro predeterminado, ya tiene acceso a las métricas de uso para todos los paneles o informes en el área de trabajo seleccionada. Puede incluso ver los nombres de los usuarios finales.

![Informe de métricas de uso](media/service-usage-metrics/power-bi-dashboard-usage-metrics-update-3.png)

## <a name="why-are-usage-metrics-important-to-me"></a>¿Por qué son importantes para mí las métricas de uso?

Conocer cómo se usa el contenido le ayuda a demostrar su impacto y a priorizar sus esfuerzos. Las métricas de uso pueden mostrarle que un segmento considerable de la organización utiliza a diario uno de sus informes y también que un panel que creó no lo está viendo nadie. Este tipo de comentario es muy valioso a la hora de dirigir los esfuerzos de trabajo que realiza.

La ejecución de informes de métricas de uso solo está disponible en el servicio Power BI.  Sin embargo, si guarda un informe de métricas de uso o lo ancla a un panel, puede abrirlo e interactuar con ese informe en dispositivos móviles.

### <a name="prerequisites"></a>Requisitos previos

- La característica de métricas de uso permite capturar información de uso de todos los usuarios, sea cual sea la licencia que tengan asignada. Sin embargo, para ejecutar los datos de métricas de uso y acceder a ellos se necesita una licencia de Power BI Pro.
- Se proporcionan métricas de uso en paneles o informes en el área de trabajo seleccionada. Para obtener acceso a los datos de métricas de uso de un determinado panel o informe, debe:    
    • Tener acceso de edición a ese panel o informe • Contar con una licencia Pro

## <a name="about-the-usage-metrics-report"></a>Información acerca del informe de métricas de uso

Cuando se selecciona **Métricas de uso** o el icono de ![métricas de uso](media/service-usage-metrics/power-bi-usage-metrics-report-icon.png), Power BI genera un informe precompilado con métricas de uso del contenido para los últimos 90 días.  El informe es similar a los informes de Power BI con los que está familiarizado, pero está diseñado para que sea informativo y no interactivo. Podrá segmentarlo en función de cómo han obtenido acceso sus usuarios finales: si ha sido a través de la Web o de una aplicación móvil, etc. A medida que los paneles e informes evolucionen, evolucionará igualmente el informe de métricas de uso, que se actualiza a diario con nuevos datos.  

Los informes de métricas de uso no aparecen en **Recientes**, **Áreas de trabajo**, **Favoritos** ni otras listas de contenido. No se pueden agregar a una aplicación. Si ancla un icono desde un informe de métricas de uso a un panel, ese panel no se podrá agregar a una aplicación o paquete de contenido.

Para profundizar en los datos del informe, o para crear sus propios informes con el conjunto de datos, utilice **Guardar como** (consulte [Guardar el informe de métricas de uso como un informe con todas las características de Power BI](#save-the-usage-metrics-report-as-a-full-featured-power-bi-report-personalize)).

## <a name="open-a-usage-metrics-report-for-a-dashboard-or-report"></a>Abrir un informe de métricas de uso para un panel o informe

1. Comience en el área de trabajo que contiene el panel o el informe.
2. En la lista de contenido del área de trabajo o en el panel o el propio informe, seleccione el icono de **Métricas de uso** ![icono de métricas de uso](media/service-usage-metrics/power-bi-usage-metrics-report-icon.png).

    ![Pestaña de paneles](media/service-usage-metrics/power-bi-run-usage-metrics-report.png)

    ![Selección de Métricas de uso](media/service-usage-metrics/power-bi-run-usage-metrics-report2.png)
3. La primera vez que lo haga, Power BI creará el informe de métricas de uso y le informará cuando esté listo.

    ![Métricas listas](media/service-usage-metrics/power-bi-usage-metrics-ready.png)
4. Para abrir los resultados, seleccione **Ver métricas de uso**.

    Las métricas de uso son un eficaz aliado mientras se trabaja para implementar y mantener los informes y paneles de Power BI. ¿Se pregunta qué páginas del informe son las más útiles y cuáles se deben eliminar gradualmente? Puede segmentar por **página del informe** para averiguarlo. ¿Se pregunta si debe crear un diseño móvil para el panel? Puede segmentar por **Plataformas** para descubrir cuántos usuarios tienen acceso a su contenido a través de las aplicaciones móviles en comparación con los que acceden a través del explorador web.

5. Si lo desea, mantenga el puntero sobre una visualización y seleccione el icono de anclaje para agregar la visualización a un panel. O bien, en la barra de menús superior, seleccione la **página Anclar elemento activo** para agregar la página completa a un panel. Desde el panel puede supervisar las métricas de uso más fácilmente o compartirlas con otras personas.

    > [!NOTE]
    > Si ancla un icono desde un informe de métricas de uso a un panel, ese panel no se podrá agregar a una aplicación o paquete de contenido.

## <a name="which-metrics-are-reported"></a>¿Qué métricas se incluyen en el informe?

| Métrica | panel | Informe | Descripción |
| --- | --- | --- | --- |
| Segmentación por método de distribución |sí |sí |Modo de acceso de los usuarios al contenido. Hay 3 métodos posibles: los usuarios pueden tener acceso al panel o informe por ser miembros de un [área de trabajo de aplicación](consumer/end-user-experience.md), por tener el contenido [compartido con ellos](service-share-dashboards.md) o al instalar una aplicación o paquete de contenido.  Observe que las vistas realizadas mediante una aplicación cuentan como "paquete de contenido". |
| Segmentación por plataforma |sí |sí |¿Se tuvo acceso al panel o informe a través del servicio Power BI (powerbi.com) o mediante un dispositivo móvil? Los dispositivos móviles incluyen todas las aplicaciones iOS, Android y Windows. |
| Segmentación por páginas de informe |no |sí |Si el informe tiene más de una página, se segmenta el informe por las páginas que se han visto. Si ve una opción de lista de "En blanco", significa que recientemente se ha agregado una página del informe (en un plazo de 24 horas, aparece el nombre real de la nueva página en la lista de segmentación) o se han eliminado páginas del informe. "En blanco" captura estos tipos de situaciones. |
| Vistas por día |sí |sí |Número total de vistas por día: una vista se define como la carga de una página del informe o un panel por parte del usuario. |
| Vistas únicas por día |sí |sí |Número de usuarios *diferentes* que han visto el panel o informe (basado en la cuenta de usuario de AAD). |
| Vistas por usuario |sí |sí |Número de vistas en los últimos 90 días, desglosado por usuarios individuales. |
| Compartidos por día |sí |no |Número de veces que el panel se compartió con otro usuario o grupo. |
| Número total de vistas |sí |sí |Número de vistas en los últimos 90 días. |
| Número total de visualizadores |sí |sí |Número de visualizadores únicos en los últimos 90 días. |
| Número total de compartidos |sí |no |Número de veces que el panel o informe se compartió en los últimos 90 días. |
| Total en la organización |sí |sí |Recuento de todos los paneles o informes en toda la organización que han tenido al menos una vista en los últimos 90 días.  Se usa para calcular la clasificación. |
| Clasificación: Número total de vistas |sí |sí |Para el número total de vistas de todos los paneles e informes de la organización en los últimos 90 días, posición en la que se clasifica este panel o informe. |
| Clasificación: Número total de compartidos |sí |no |Para el número total de compartidos de todos los paneles e informes de la organización en los últimos 90 días, posición en la que se clasifica este panel o informe. |

### <a name="dashboard-usage-metrics-report"></a>Informe de métricas de uso del panel

![Informe de métricas de uso del panel](media/service-usage-metrics/power-bi-dashboard-usage-metrics-update-3.png)

### <a name="report-usage-metrics-report"></a>Informe de métricas de uso del informe

![Informe de métricas de uso del informe](media/service-usage-metrics/power-bi-report-usage-metrics-update.png)

## <a name="save-the-usage-metrics-report-as-a-full-featured-power-bi-report-personalize"></a>Guardar el informe de métricas de uso como un informe con todas las características de Power BI (personalizar)

![Guardar como](media/service-usage-metrics/power-bi-save-as.png)

Use **Guardar como** para convertir el informe de métricas de uso en un informe de Power BI con todas las características, que se puede personalizar y compartir. Después de crear una copia personalizada, obtendrá acceso completo al conjunto de datos subyacente, lo que le permite personalizar el informe de métricas de uso para sus necesidades específicas. Puede incluso usar Power BI Desktop para crear informes de métricas de uso personalizadas mediante la [conexión dinámica a la característica del servicio Power BI](https://powerbi.microsoft.com/blog/connecting-to-datasets-in-the-power-bi-service-from-desktop).

Más aún, el conjunto de datos subyacente incluye los detalles de uso para todos los paneles o informes en el área de trabajo. Esto ofrece un nuevo mundo de posibilidades. Por ejemplo, podría crear un informe que comparara todos los paneles en el área de trabajo basándose en el uso. O bien, podría crear un panel de métricas de uso para la aplicación Power BI agregando el uso a todo el contenido distribuido dentro de esa aplicación.  Consulte [Quitar el filtro para ver todos los datos de métricas de uso en el área de trabajo](#remove-the-filter-to-see-all-the-usage-metrics-data-in-the-workspace) a continuación.

### <a name="what-is-created-when-using-save-as"></a>¿Qué es lo que se crea cuando se usa "Guardar como"?

Cuando Power BI crea el informe completo, también crea un nuevo conjunto de datos **formado por todos los paneles e informes que se encuentran en el área de trabajo actual** a los que se ha tenido acceso en los últimos 90 días. Por ejemplo, supongamos que tiene un área de trabajo denominada "Sales" que contiene tres paneles y dos informes, y crea un informe de métricas de uso en el panel "Northeast". A continuación, usa **Guardar como** para personalizar y convertirlo en un informe completo. El conjunto de datos para ese nuevo informe contiene las métricas de uso *no solo para el panel con el nombre "Northeast"* sino para los tres paneles en el área de trabajo "Sales". El informe muestra de forma predeterminada datos del panel "Northeast" y deberá [quitar un filtro](#remove-the-filter-to-see-all-the-usage-metrics-data-in-the-workspace) (un solo clic) para mostrar los datos de los tres paneles.

### <a name="create-a-copy-of-the-usage-report-using-save-as"></a>Crear una copia del informe de uso con "Guardar como"

Cuando crea una copia con "Guardar como" (personalizar), Power BI convierte el informe de solo lectura pregenerado en un informe completo.  A primera vista, parece exactamente el mismo. Sin embargo, ya puede abrir el informe en vista de edición, agregar nuevas visualizaciones, filtros y páginas, modificar o eliminar visualizaciones existentes, y mucho más. Power BI guarda el nuevo informe y el conjunto de datos en el área de trabajo actual. En el ejemplo siguiente, el área de trabajo actual es **mihart**.

1. En el informe de métricas de uso pregenerado, seleccione **Archivo > Guardar como**. Power BI convierte el informe de métricas de uso en un informe con todas las características de Power BI. A esto se le denomina informe de métricas de uso *personalizado*. El informe de uso personalizado y el conjunto de datos se guardan en el área de trabajo actual, que se llama **mihart*.

    ![Guardar como](media/service-usage-metrics/power-bi-save-as.png)
2. Abra el informe en vista de edición e [interactúe con él como lo haría con cualquier otro informe de Power BI](service-interact-with-a-report-in-editing-view.md). Por ejemplo, agregar nuevas páginas y crear nuevas visualizaciones, agregar filtros, dar formato a las fuentes y colores, etc.

    ![Apertura de un informe en Vista de edición](media/service-usage-metrics/power-vi-editing-view.png)
3. O bien, comience con el nuevo conjunto de datos y genere un informe desde el principio.

    ![Pestaña Conjuntos de datos](media/service-usage-metrics/power-bi-new-dataset.png)
4. El nuevo informe se guarda en el área de trabajo actual (mihart) y se agrega también a la lista de contenido **Recientes**.

    ![Pestaña Informes](media/service-usage-metrics/power-bi-new-report.png)

### <a name="remove-the-filter-to-see-all-the-usage-metrics-data-in-the-workspace"></a>Elimine el filtro para ver ***todos*** los datos de métricas de uso del área de trabajo

Para ver las métricas de todos los paneles o informes en el área de trabajo, tendrá que quitar un filtro. De forma predeterminada, el informe personalizado se filtra para mostrar métricas solo del panel o informe que se usó para crearlo.

Si, por ejemplo, se utiliza el panel denominado "European sales" para crear este nuevo informe personalizado, se muestran solo los datos de uso del panel "European sales". Para quitar el filtro y los datos de todos los paneles en esa área de trabajo:

1. Abra el informe personalizado en la vista de edición.

    ![Selección de Editar informe](media/service-usage-metrics/power-bi-editing-view.png)
2. En el panel de filtros, busque el cubo **Filtros de nivel de informe** y quite el filtro seleccionando la "x".

    ![Eliminación del filtro](media/service-usage-metrics/power-bi-report-level-filter2.png)

    Ahora el informe personalizado muestra las métricas para toda el área de trabajo.

## <a name="admin-controls-for-usage-metrics---for-power-bi-administrators"></a>Controles de administración para métricas de uso: para administradores de Power BI

Los informes de métricas de uso son una característica que el administrador de Power BI u Office 365 puede activar o desactivar. Los administradores tienen control granular sobre qué usuarios tienen acceso a las métricas de uso. Estas están activas de manera predeterminada para todos los usuarios de la organización.

1. Abra el portal de administración con el icono de engranaje en la parte superior derecha del servicio Power BI y elija **Portal de administración**.

    ![Selección del icono de engranaje](media/service-usage-metrics/power-bi-admin-portal-new.png)
2. En el portal de administración, seleccione **Configuración de inquilino** y elija **Métricas de uso para los creadores de contenido**.

    ![Portal de administración](media/service-usage-metrics/power-bi-usage-settings.png)
3. Habilite (o deshabilite) las métricas de uso y seleccione **Aplicar**.

    ![Métricas de uso habilitadas](media/service-usage-metrics/power-bi-tenant-settings-updated.png)

Los datos por usuario están habilitados de forma predeterminada en las métricas de uso, mientras que el informe de métricas incluye información sobre la cuenta del creador de contenido. Si prefiere no incluir esta información de algunos los usuarios, incluso de ninguno de ellos, deshabilite la característica para los grupos de seguridad en cuestión o para toda la organización. En tal caso, la información de la cuenta aparece en el informe como *Sin nombre*.

Al deshabilitar las métricas de uso para toda la organización, los administradores pueden utilizar la opción **Elimine todo el contenido existente de las métricas de uso** para eliminar todos los iconos de informes y paneles existentes que se compilaron mediante los informes y conjuntos de datos de las métricas de uso. Esta opción permite eliminar todos los accesos a los datos de métricas de uso de todos los usuarios de la organización que ya los puedan estar usando. Tenga cuidado, ya que la eliminación del contenido de las métricas de uso existentes es irreversible.

## <a name="usage-metrics-in-national-clouds"></a>Métricas de uso en nubes nacionales

Power BI está disponible en nubes nacionales independientes. Dichas nubes ofrecen los mismos niveles de seguridad, privacidad, cumplimiento y transparencia como la versión global de Power BI, combinado con un modelo único para las regulaciones locales relativas prestación de servicios, residencia de datos, acceso y control. Dado que se trata de un modelo único para las regulaciones locales, las métricas de uso no están disponibles en las nubes nacionales. Para obtener más información, consulte el tema relativo a las [nubes nacionales](https://powerbi.microsoft.com/clouds/).

## <a name="considerations-and-limitations"></a>Consideraciones y limitaciones

Es importante comprender qué diferencias pueden producirse al comparar métricas de uso y registros de auditoría y por qué. Los *registros de auditoría* se recopilan mediante datos del servicio Power BI, y las *métricas de uso* se recopilan en el cliente. Debido a esa diferencia, los recuentos de agregados de las actividades en los registros de auditoría podrían no coincidir siempre con las métricas de uso por los siguientes motivos:

* En ocasiones, las métricas de uso pueden no contar actividades debido a conexiones de red desiguales, bloqueadores de anuncios y otros problemas que pueden interrumpir el envío de los eventos desde el cliente.
* Ciertos tipos de vistas no se incluyen en las métricas de uso, como se ha descrito anteriormente en este artículo.
* En ocasiones, las métricas de uso pueden no contar actividades en situaciones en las que el cliente se actualiza sin necesidad de devolver una solicitud al servicio Power BI.

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

Además de las posibles diferencias entre métricas de uso y registros de auditoría, las siguientes preguntas y respuestas sobre las métricas de uso pueden ser útiles para los usuarios y administradores:

**P:**    No puedo ejecutar métricas de uso en un panel o informe.

**R:**    R: Solo puede ver métricas de uso para el contenido del que es propietario o para el que tenga permisos de edición.

**P:**    ¿Las métricas de uso capturan vistas de los informes y paneles insertados?

**R:**    Actualmente, las métricas de uso no permiten capturar el uso de paneles insertados, informes y el flujo [publicar en web](service-publish-to-web.md).          En esos casos, se recomienda utilizar las plataformas de análisis web existentes para realizar un seguimiento del uso del portal o la aplicación de hospedaje.

**P:**    No puedo ejecutar métricas de uso en ningún contenido.

**R1:**    Los administradores pueden desactivar esta característica para su organización.  Póngase en contacto con su administrador para comprobar si este es el caso.

**R2:**    Las métricas de uso son una característica de Power BI Pro.

**P:**    Los datos no parecen actualizados. Por ejemplo, los métodos de distribución no aparecen, faltan de páginas del informe, etc.

**R:**    Los datos pueden tardar hasta 24 horas en actualizarse.

**P:**    Hay cuatro informes en el área de trabajo, pero el informe de métricas de uso solo muestra tres.

**R:**    El informe de métricas de uso solo incluye informes (o paneles) a los que se haya accedido en los últimos 90 días.  Si un informe (o un panel) no aparece, es probable que no se haya usado en más de 90 días.

## <a name="next-steps"></a>Pasos siguientes

[Paneles favoritos](consumer/end-user-favorite.md)

¿Tiene más preguntas? [Pruebe la comunidad de Power BI](http://community.powerbi.com/)
