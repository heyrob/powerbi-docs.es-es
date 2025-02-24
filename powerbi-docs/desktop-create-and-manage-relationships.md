---
title: Crear y administrar relaciones en Power BI Desktop
description: Crear y administrar relaciones en Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 04/19/2019
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: f2102ad654a056832f7890dc506acc99eb5ef26f
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "61312713"
---
# <a name="create-and-manage-relationships-in-power-bi-desktop"></a>Crear y administrar relaciones en Power BI Desktop
Al importar varias tablas, lo más probable es que vaya a realizar un análisis con los datos de todas esas tablas. Las relaciones entre esas tablas son necesarias para calcular los resultados de forma precisa y mostrar la información correcta en los informes. Power BI Desktop facilita la creación de esas relaciones. De hecho, en la mayoría de los casos no tendrá que hacer nada; la característica de detección automática lo puede hacer por usted. Sin embargo, en algunos casos tendrá que crear relaciones usted mismo o tal vez necesite realizar algunos cambios en una relación. En cualquier caso, es importante entender las relaciones en Power BI Desktop y cómo crearlas y editarlas.

## <a name="autodetect-during-load"></a>Detección automática durante la carga
Si consulta dos o más tablas al mismo tiempo, cuando se carguen los datos, Power BI Desktop intenta buscar y crear relaciones automáticamente. La cardinalidad, la dirección del filtro cruzado y las propiedades activas se establecen automáticamente. Power BI Desktop examina los nombres de columna en las tablas que está consultando para determinar si hay posibles relaciones. Si las hay, esas relaciones se crean automáticamente. Si Power BI Desktop no puede determinar con un alto nivel de confianza se encuentra una coincidencia, no crea automáticamente la relación. Todavía puede usar el cuadro de diálogo Administrar relaciones para crear o modificar las relaciones.

## <a name="create-a-relationship-by-using-autodetect"></a>Crear una relación mediante la detección automática
En la pestaña **Inicio**, haga clic en **Administrar relaciones** \> **Detección automática**.

![](media/desktop-create-and-manage-relationships/automaticrelationship.gif)

## <a name="create-a-relationship-manually"></a>Crear una relación de forma manual
1. En la pestaña **Inicio**, haga clic en **Administrar relaciones** \> **Nuevo**.
2. En el **Crear relación** cuadro de diálogo, en la primera lista desplegable de tabla, seleccione una tabla y, a continuación, seleccione la columna que desea usar en la relación.
3. En la segunda lista desplegable de tabla, seleccione la otra tabla que desea en la relación y, a continuación, seleccione la otra columna que desea usar y, a continuación, haga clic en **Aceptar**.

![](media/desktop-create-and-manage-relationships/manualrelationship2.gif)

De forma predeterminada, Power BI Desktop configura automáticamente la cardinalidad (dirección), entre la dirección del filtro y las propiedades activas para la nueva relación; Sin embargo, puede cambiar la configuración si es necesario. Para obtener más información, vea la sección de información sobre opciones adicionales más adelante en este artículo.

Verá un error que indica *una de las columnas debe tener valores únicos* si ninguna de las tablas seleccionadas para la relación tenga valores únicos. Al menos una tabla de una relación *debe* tener una lista distinta y única de valores de clave, que es un requisito común para todas las tecnologías de bases de datos relacionales. 

Si detecta ese error, hay un par de formas de corregir el problema:

* Usar "Quitar filas duplicadas" para crear una columna con valores únicos. El inconveniente de este enfoque es que perderá información cuando se quiten las filas duplicadas, y a menudo se duplica una clave (fila) por un buen motivo.
* Agregar una tabla intermedia hecha de la lista de valores de claves distintos en el modelo, que luego se vinculará a ambas columnas originales de la relación.

Para obtener más información, consulte el [entrada de blog](https://blogs.technet.microsoft.com/cansql/2016/12/19/relationships-in-power-bi-fixing-one-of-the-columns-must-have-unique-values-error-message/).


## <a name="edit-a-relationship"></a>Editar una relación
1. En la pestaña **Inicio** , haga clic en **Administrar relaciones**.
2. En el cuadro de diálogo **Administrar relaciones** , seleccione la relación y haga clic en **Editar**.

## <a name="configure-additional-options"></a>Configuración de opciones adicionales
Al crear o editar una relación, puede configurar opciones adicionales. De forma predeterminada, las opciones adicionales se configuran automáticamente en función de una mejor aproximación, que puede ser diferente para cada relación según los datos de las columnas.

## <a name="cardinality"></a>Cardinalidad
**Varios a uno (\*: 1)** : la mayoría común, el tipo predeterminado, lo que significa que la columna de una tabla puede tener más de una instancia de un valor y la otra tabla relacionada, a menudo conocida como tabla de búsqueda, solo tiene una instancia de un valor.

**Uno a uno (1:1)** : la columna de una tabla solo tiene una instancia de un valor determinado, y la otra tabla relacionada solo tiene una instancia de un valor determinado.

**Relaciones de varios a varios**: Con modelos compuestos, puede establecer relaciones de varios a varios entre tablas, lo que elimina los requisitos para valores únicos en tablas. También permite descartar las soluciones alternativas anteriores, como el hecho de presentar nuevas tablas solo para establecer relaciones. Para más información, vea [Relaciones con una cardinalidad de varios a varios](https://docs.microsoft.com/power-bi/desktop-many-to-many-relationships). 

Vea la sección Información sobre opciones adicionales más adelante en este artículo para obtener más detalles sobre cuándo se debe cambiar la cardinalidad.

## <a name="cross-filter-direction"></a>Dirección de filtro cruzado
**Ambos** : la más común, la dirección predeterminada, lo que significa para el filtrado con fines, ambas tablas se tratan como si fueran una sola tabla. **Ambos** funciona bien con una única tabla que tiene un número de tablas de búsqueda que lo rodean. Un ejemplo es una tabla de datos reales de ventas con una tabla de búsqueda de departamento. Esto se suele denominar una configuración de esquema de estrella (una tabla central con varias tablas de búsqueda). Sin embargo, si tiene dos o más tablas que también tengan tablas de búsqueda (con algo en común), no deseará usar la configuración de ambos. Para continuar con el ejemplo anterior, en este caso, también dispone de una tabla de ventas de presupuesto que registra el presupuesto de destino para cada departamento. Además, la tabla de departamento está conectada a la tabla de presupuesto y de ventas. Evite la configuración de ambos para este tipo de configuración.

**Solo** -las opciones de filtrado en tablas conectadas funcionan en la tabla donde se agregan valores. Si importa un modelo de datos de Power Pivot o anterior en Excel 2013, todas las relaciones tendrán una dirección única. 

Vea la sección Información sobre opciones adicionales más adelante en este artículo para obtener más detalles sobre cuándo se debe cambiar la dirección del filtro único.

## <a name="make-this-relationship-active"></a>Activar esta relación
Si se activa, significa que la relación actúa como la relación predeterminada y activa. En casos donde hay más de una relación entre dos tablas, la relación activa proporciona una manera para que Power BI Desktop cree automáticamente visualizaciones que incluyan las dos tablas.

Vea la sección Información sobre opciones adicionales más adelante en este artículo para obtener más detalles sobre cuándo activar determinada relación.

## <a name="understanding-relationships"></a>Descripción de las relaciones
Una vez que haya conectado dos tablas junto con una relación, puede trabajar con los datos en ambas tablas como si fueran una sola tabla, lo que le libera de tener que preocuparse sobre los detalles de la relación o lo que aplana esas tablas en una sola tabla antes de importarlas. En muchas situaciones, Power BI Desktop puede crear automáticamente relaciones para usted, por lo que es posible que no sea necesario que usted cree esas relaciones. Sin embargo, si Power BI Desktop no puede determinar con un alto grado de certeza que debe existir una relación entre dos tablas, crear automáticamente la relación. En ese caso, debe crear la relación. 

Analicemos un tutorial rápido, para mostrarle mejor cómo funcionan las relaciones en Power BI Desktop.

>[!TIP]
>Puede completar esta lección. Copie la tabla ProjectHours de abajo en una hoja de cálculo de Excel, seleccione todas las celdas, haga clic en **INSERTAR** \> **Tabla**. En el cuadro de diálogo **Crear tabla** , haga clic en **Aceptar**. A continuación, en **Nombre de tabla**, escriba **ProjectHours**. Haga lo mismo para la tabla CompanyProject. A continuación, puede importar los datos mediante **Obtener datos** en Power BI Desktop. Seleccione el libro y las tablas como origen de datos.

Esta primera tabla, ProjectHours, es un registro de los vales de trabajo que registran el número de horas que una persona ha trabajado en determinado proyecto. 

**ProjectHours**

| **Ticket** | **SubmittedBy** | **Hours** | **Project** | **DateSubmit** |
| ---:|:--- | ---:|:--- | ---:|
| 1001 |Brewer, Alan |22 |Azul |1/1/2013 |
| 1002 |Brewer, Alan |26 |Rojo |2/1/2013 |
| 1003 |Ito, Shu |34 |Amarillo |12/4/2012 |
| 1004 |Brewer, Alan |13 |Naranja |1/2/2012 |
| 1005 |Bowen, Eli |29 |Púrpura |10/1/2013 |
| 1006 |Bento, Nuno |35 |Verde |2/1/2013 |
| 1007 |Hamilton, David |10 |Amarillo |10/1/2013 |
| 1008 |Han, Mu |28 |Naranja |1/2/2012 |
| 1009 |Ito, Shu |22 |Púrpura |2/1/2013 |
| 1010 |Bowen, Eli |28 |Verde |10/1/2013 |
| 1011 |Bowen, Eli |9 |Azul |10/15/2013 |

Esta segunda tabla, CompanyProject, es una lista de proyectos con una prioridad asignada, A, B o C. 

**CompanyProject**

| **ProjName** | **Priority** |
| --- | --- |
| Azul |A |
| Rojo |B |
| Verde |C |
| Amarillo |C |
| Púrpura |B |
| Naranja |C |

Observe que cada tabla tenga una columna de proyecto. Cada una tiene un nombre ligeramente distinto, pero los valores parecen iguales. Eso es importante y volveremos a él en breve.

Ahora que tenemos nuestras dos tablas importadas en un modelo, vamos a crear un informe. Lo primero que queremos obtener es el número de horas presentadas por prioridad del proyecto, así que seleccionamos **Priority** y **Hours** en Campos.

 ![](media/desktop-create-and-manage-relationships/candmrel_reportfiltersnorel.png)

Si observamos nuestra tabla en el lienzo del informe, verá que el número de horas es **256,00** para cada proyecto y también el total. Claramente esto no es correcto. ¿Por qué? Porque no se puede calcular un suma total de valores de una tabla (Hours en la tabla Project), segmentada por valores en otra tabla (Priority en la tabla CompanyProject) sin una relación entre estas dos tablas.

Por lo tanto, vamos a crear una relación entre estas dos tablas.

¿Recuerda las columnas que vimos en ambas tablas, con un nombre de proyecto, pero con valores similares? Vamos a usar estas dos columnas para crear una relación entre las tablas.

¿Por qué estas columnas? Bueno, si miramos la columna Project en la tabla ProjectHours, veremos valores como Azul, Rojo, Amarillo, Naranja, etc. De hecho, veremos varias filas que tienen el mismo valor. En efecto, tenemos muchos valores de color para Project.

Si miramos la columna ProjName en la tabla CompanyProject, veremos que solo hay uno de cada uno de los valores de color para el proyecto. El valor de cada color en esta tabla es único y eso es importante, porque podemos crear una relación entre estas dos tablas. En este caso, una relación varios a uno. En una relación de varios a uno, al menos una columna en una de las tablas debe contener valores únicos. Existen algunas opciones adicionales para algunas relaciones que examinaremos más adelante, pero por ahora vamos a crear una relación entre las columnas Project en cada una de nuestras dos tablas.

### <a name="to-create-the-new-relationship"></a>Para crear la nueva relación
1. Haga clic en **Administrar relaciones**.
2. En **administrar relaciones**, haga clic en **New** para abrir el **Crear relación** cuadro de diálogo, donde podemos seleccionar las tablas, columnas y cualquier configuración adicional que queramos para nuestra relación.
3. En la primera tabla, seleccione **ProjectHours**y, a continuación, seleccione la columna **Project** . Se trata del lado varios de nuestra relación.
4. En la segunda tabla, seleccione **CompanyProject**y, a continuación, seleccione la columna **ProjName** . Se trata del lado uno de nuestra relación. 
5. Siga adelante y haga clic en **Aceptar** tanto en el cuadro de diálogo **Crear relación** como en el cuadro de diálogo **Administrar relaciones** .

![](media/desktop-create-and-manage-relationships/candmrel_create_compproj.png)

En aras de una divulgación completa, acaba de crear esta relación de las malas. Podría simplemente haber hecho clic en el botón detección automática en el cuadro de diálogo Administrar relaciones. De hecho, la detección automática lo habría hecho por usted al cargar los datos si las dos columnas tuvieran el mismo nombre. Pero, ¿cuál es el desafío?

Ahora, echemos un vistazo en la tabla del lienzo del informe una vez más.

 ![](media/desktop-create-and-manage-relationships/candmrel_reportfilterswithrel.png)

Ahora se ve mucho mejor, ¿verdad?

Cuando se suman horas por prioridad, Power BI Desktop busca todas las instancias de los valores de color únicos en la tabla de búsqueda CompanyProject y, a continuación, busque todas las instancias de cada uno de esos valores en la tabla CompanyProject y calculará una suma total para cada valor único .

Eso fue sencillo, de hecho, con la detección automática, es posible que no tiene incluso hacer esto mucho.

## <a name="understanding-additional-options"></a>Descripción de las opciones adicionales
Cuando se crea una relación, ya sea con detección automática o de que forma manual, Power BI Desktop configura automáticamente las opciones adicionales según los datos de las tablas. Puede configurar estas propiedades de relación adicionales en la parte inferior del cuadro de diálogo de creación y edición de relaciones.

 ![](media/desktop-create-and-manage-relationships/candmrel_advancedoptions2.png)

Como se ha explicado antes, normalmente se establecen automáticamente y no tendrá que trabajar con ellas. Sin embargo, hay varias situaciones donde tal vez quiera configurar opciones adicionales usted mismo.

## <a name="automatic-relationship-updates"></a>Actualizaciones automáticas de relación

Puede administrar cómo Power BI trata y ajusta automáticamente las relaciones en los informes y modelos. Para especificar cómo Power BI controla las opciones de las relaciones, seleccione **archivo > Opciones y configuración > opciones** desde Power BI Desktop, a continuación, seleccione **carga datos** en el panel izquierdo. A continuación, verá opciones para **relaciones**.

 ![Opciones de relaciones](media/desktop-create-and-manage-relationships/relationships-options-01.png)

Hay tres opciones que se pueden seleccionar y habilitadas. 

La primera opción es *importar las relaciones de orígenes de datos*, y se selecciona de forma predeterminada. Cuando se selecciona, Power BI comprueba si hay relaciones definidas en el origen de datos, como la clave externa y principal las relaciones en el almacenamiento de datos de clave. Si existen estas relaciones, se reflejan en el modelo de datos de Power BI al cargar datos inicialmente. Esta opción permite a rápidamente empezar a trabajar con el modelo, en lugar de necesidad de buscar o definir esas relaciones usted mismo.

La segunda opción es *actualizar o eliminar relaciones al actualizar datos*, y está desactivada de forma predeterminada. Si ha seleccionado (habilitado activando la casilla situada junto a la opción), Power BI comprueba si hay cambios en las relaciones del origen de datos cuando se actualiza el conjunto de datos. Si esas relaciones se cambian o se quitan, Power BI refleja los cambios en su propio modelo de datos, actualizándolas o eliminándolas para que coincida con.

> [!WARNING]
> Si usa seguridad de nivel de fila que se basa en las relaciones definidas, no se recomienda seleccionar la segunda opción, *actualizar o eliminar relaciones al actualizar datos*. Si se quita una relación que se basan en la configuración de RLS, el modelo puede volverse menos seguro. 

La tercera opción es *detectar automáticamente nuevas relaciones después de cargar datos*, que se describe en el [detección automática durante la carga](#autodetect-during-load) sección, que aparecía anteriormente en este artículo. 


## <a name="future-updates-to-the-data-require-a-different-cardinality"></a>Las futuras actualizaciones de datos requieren una cardinalidad diferente
Normalmente, Power BI Desktop puede determinar automáticamente la mejor cardinalidad para la relación. Si necesita reemplazar la configuración automática, porque sabe que los datos cambiarán en el futuro, puede seleccionarla en el control de cardinalidad. Veamos un ejemplo donde se debe seleccionar una cardinalidad diferente.

La siguiente tabla CompanyProjectPriority es una lista de todos los proyectos de la empresa y su prioridad. La tabla ProjectBudget es el conjunto de proyectos para los que se ha aprobado presupuesto.

**ProjectBudget**

| **Proyectos aprobados** | **BudgetAllocation** | **AllocationDate** |
|:--- | ---:| ---:|
| Azul |40,000 |12/1/2012 |
| Rojo |100,000 |12/1/2012 |
| Verde |50,000 |12/1/2012 |

**CompanyProjectPriority**

| **Project** | **Priority** |
| --- | --- |
| Azul |A |
| Rojo |B |
| Verde |C |
| Amarillo |C |
| Púrpura |B |
| Naranja |C |

Si creamos una relación entre la columna Project en la tabla CompanyProjectPriority y la columna ApprovedProjects en la tabla ProjectBudget, similar al siguiente:

 ![](media/desktop-create-and-manage-relationships/candmrel_create_compproj_appproj2.png)

Se establecerá automáticamente cardinalidad en uno a uno (1:1) y el filtrado cruzado para que sea Ambos (como se muestra). Esto es porque en el Power BI Desktop la mejor combinación de las dos tablas realmente tiene el siguiente aspecto:

| **Project** | **Priority** | **BudgetAllocation** | **AllocationDate** |
|:--- | --- | ---:| ---:|
| Azul |A |40,000 |12/1/2012 |
| Rojo |B |100,000 |12/1/2012 |
| Verde |C |50,000 |12/1/2012 |
| Amarillo |C |<br /> |<br /> |
| Púrpura |B |<br /> |<br /> |
| Naranja |C |<br /> |<br /> |

Hay una relación uno a uno entre nuestras dos tablas porque no hay ningún valor de repetición en la columna Project de la tabla combinada. La columna Project es única, porque cada valor se produce solo una vez, por lo que las filas de las dos tablas se pueden combinar directamente sin ninguna duplicación.

Sin embargo, supongamos que sabe que los datos cambiarán la próxima vez que los actualice. Ahora una versión actualizada de la tabla ProjectBudget tiene filas adicionales para Azul y Rojo:

**ProjectBudget**

| **Proyectos aprobados** | **BudgetAllocation** | **AllocationDate** |
| --- | ---:| ---:|
| Azul |40,000 |12/1/2012 |
| Rojo |100,000 |12/1/2012 |
| Verde |50,000 |12/1/2012 |
| Azul |80,000 |6/1/2013 |
| Rojo |90,000 |6/1/2013 |

 Esto significa que la mejor combinación de las dos tablas realmente tiene el siguiente aspecto: 

| **Project** | **Priority** | **BudgetAllocation** | **AllocationDate** |
| --- | --- | ---:| ---:|
| Azul |A |40,000 |12/1/2012 |
| Rojo |B |100,000 |12/1/2012 |
| Verde |C |50,000 |12/1/2012 |
| Amarillo |C |<br /> |<br /> |
| Púrpura |B |<br /> |<br /> |
| Naranja |C |<br /> |<br /> |
| Azul |A |80000 |6/1/2013 |
| Rojo |B |90000 |6/1/2013 |

En esta nueva tabla combinada, la columna Project tiene valores repetidos. Las dos tablas originales no tienen una relación uno a uno, una vez que se actualiza la tabla. En este caso, como sabemos que las actualizaciones futuras harán que la columna Project tenga duplicados, queremos establecer la Cardinalidad en Varios a uno (\*: 1), con Varios en el lado de ProjectBudget y Uno en el lado de CompanyProjectPriority.

## <a name="adjusting-cross-filter-direction-for-a-complex-set-of-tables-and-relationships"></a>Ajuste de la dirección del filtro cruzado para un conjunto complejo de tablas y relaciones
Para la mayoría de las relaciones, la dirección del filtro cruzado se establece en "Ambos". Sin embargo, hay algunas circunstancias poco comunes en las que tal vez necesite establecer esto de forma diferente del valor predeterminado, como si estuviera importando un modelo de una versión anterior de Power Pivot, donde cada relación se establece en una sola dirección. 

La opción Ambos permite que Power BI Desktop trate todos los aspectos de las tablas conectadas como si fueran una sola tabla. Existen algunas situaciones, sin embargo, en las que Power BI Desktop no puede establecer la dirección del filtro cruzado de una relación en "Ambos" y también mantener un conjunto ambiguo de valores predeterminados disponibles para fines de elaboración de informes. Si la dirección del filtro cruzado de una relación no se establece en Ambos, suele ser porque se crearía ambigüedad. Si el valor predeterminado del filtro cruzado no funciona para usted, intente configurarlo en una tabla determinada o en Ambos.

El filtro cruzado de una sola dirección funciona para muchas situaciones. De hecho, si ha importado un modelo de PowerPivot en Excel 2013 o versiones anteriores, todas las relaciones se establecerán en una dirección única. Una dirección única significa que las opciones de filtrado en tablas conectadas funcionan en la tabla donde sucede el trabajo de agregación. A veces, comprender el filtrado cruzado puede ser un poco complicado; veamos un ejemplo.

 ![](media/desktop-create-and-manage-relationships/candmrel_singledircrossfiltering.png)

Con el filtro cruzado de dirección única, si crea un informe que resuma las horas del proyecto, podrá optar por resumir (o filtrar) por los valores CompanyProject, Priority o CompanyEmployee, City. Sin embargo, si quiere contar el número de empleados por proyecto (una pregunta menos común), esto no funcionará. Obtendrá una columna de valores que son los mismos. En el ejemplo siguiente, la dirección de filtro cruzado de ambas relaciones se establece en una dirección única: hacia la tabla ProjectHours:

 ![](media/desktop-create-and-manage-relationships/candmrel_repcrossfiltersingle.png)

Especificación del filtro fluirá de CompanyProject a CompanyEmployee (como se muestra en la imagen siguiente), pero no fluirá hasta CompanyEmployee. Sin embargo, si establece la dirección del filtro cruzado en Ambos, sí funcionará. La opción Ambos permite que la especificación del filtro fluya hasta Employee.

 ![](media/desktop-create-and-manage-relationships/candmrel_bidircrossfiltering.png)

Con la dirección del filtro cruzado establecida en Ambos, nuestro informe ahora parece correcto:

 ![](media/desktop-create-and-manage-relationships/candmrel_repcrossfilterbi.png)

El filtro cruzado de ambas direcciones funciona bien para un modelo de relaciones de tablas que tengan un aspecto como el modelo anterior. Normalmente, esto se denomina esquema de estrella, similar al siguiente:

 ![](media/desktop-create-and-manage-relationships/candmrel_crossfilterstarschema.png)

La dirección del filtro cruzado no funciona bien con un patrón más general que se suele encontrarse en las bases de datos, como en este diagrama:

 ![](media/desktop-create-and-manage-relationships/candmrel_crossfilterwithloops.png)

Si tiene un patrón de tabla como este, con bucles, el filtro cruzado puede crear un conjunto ambiguo de relaciones. Por ejemplo, si suma un campo de Tabla X y después elige filtrar por un campo en la Tabla Y, no resulta claro cómo debe viajar el filtro, si a través de la tabla superior o la tabla inferior. Un ejemplo común de este tipo de modelo usa la Tabla X como tabla de ventas con los datos reales y la Tabla Y como tabla de datos de presupuesto. A continuación, las tablas en la parte central son tablas de búsqueda que utilizan las dos tablas, como la de división o de región. 

De igual modo que con las relaciones activas e inactivas, Power BI Desktop no permitirá que una relación se establezca en Ambos si creará ambigüedad en los informes. Hay varias maneras diferentes para tratar este asunto. Estas dos son las más comunes:

* Eliminar o marcar las relaciones como inactivas para reducir la ambigüedad. A continuación, puede establecer un filtro cruzado de relación en Ambos.
* Agregar una tabla dos veces (con un nombre diferente la segunda vez) para eliminar los bucles. Esto hace que el patrón de relaciones como un esquema de estrella. Con un esquema de estrella, todas las relaciones pueden establecerse en Ambos.

## <a name="wrong-active-relationship"></a>Relación activa incorrecta
Cuando Power BI Desktop crea automáticamente relaciones, a veces encuentra más de una relación entre dos tablas. Cuando esto sucede solo una de las relaciones se establece para estar activa. La relación activa actúa como la relación predeterminada para que al elegir los campos de dos tablas diferentes, Power BI Desktop pueda crear automáticamente una visualización para usted. Sin embargo, en algunos casos la relación seleccionada de forma automática puede ser incorrecta. Puede usar el cuadro de diálogo Administrar relaciones para establecer una relación como activa o inactiva, o bien puede establecer la relación activa en el cuadro de diálogo Editar relación. 

Para garantizar que haya una relación predeterminada, Power BI Desktop solo permite una relación única activa entre dos tablas en un momento dado. Por lo tanto, debe establecer primero la relación actual como inactiva y, a continuación, establecer la relación que desea que esté activa.

Veamos un ejemplo. Esta primera tabla es ProjectTickets y la tabla siguiente es EmployeeRole.

**ProjectTickets**

| **Ticket** | **OpenedBy** | **SubmittedBy** | **Hours** | **Project** | **DateSubmit** |
| ---:|:--- |:--- | ---:|:--- | ---:|
| 1001 |Perham, Tom |Brewer, Alan |22 |Azul |1/1/2013 |
| 1002 |Roman, Daniel |Brewer, Alan |26 |Rojo |2/1/2013 |
| 1003 |Roth, Daniel |Ito, Shu |34 |Amarillo |12/4/2012 |
| 1004 |Perham, Tom |Brewer, Alan |13 |Naranja |1/2/2012 |
| 1005 |Roman, Daniel |Bowen, Eli |29 |Púrpura |10/1/2013 |
| 1006 |Roth, Daniel |Bento, Nuno |35 |Verde |2/1/2013 |
| 1007 |Roth, Daniel |Hamilton, David |10 |Amarillo |10/1/2013 |
| 1008 |Perham, Tom |Han, Mu |28 |Naranja |1/2/2012 |
| 1009 |Roman, Daniel |Ito, Shu |22 |Púrpura |2/1/2013 |
| 1010 |Roth, Daniel |Bowen, Eli |28 |Verde |10/1/2013 |
| 1011 |Perham, Tom |Bowen, Eli |9 |Azul |10/15/2013 |

**EmployeeRole**

| **Employee** | **Role** |
| --- | --- |
| Bento, Nuno |Administrador del proyecto |
| Bowen, Eli |Responsable del proyecto |
| Brewer, Alan |Administrador del proyecto |
| Hamilton, David |Responsable del proyecto |
| Han, Mu |Responsable del proyecto |
| Ito, Shu |Responsable del proyecto |
| Perham, Tom |Patrocinador del proyecto |
| Roman, Daniel |Patrocinador del proyecto |
| Roth, Daniel |Patrocinador del proyecto |

En realidad hay dos relaciones aquí. Una entre SubmittedBy en la tabla ProjectTickets y Employee en la tabla EmployeeRole, y la otra entre OpenedBy en la tabla ProjectTickets y Employee en la tabla EmployeeRole.

 ![](media/desktop-create-and-manage-relationships/candmrel_activerelview.png)

Si agregamos ambas relaciones al modelo (OpenedBy primero), el cuadro de diálogo Administrar relaciones mostrará que OpenedBy está activo:

 ![](media/desktop-create-and-manage-relationships/candmrel_managerelactive.png)

Ahora, si creamos un informe que use campos Role y Employee de EmployeeRole y el campo Hours de ProjectTickets en una visualización de la tabla en el lienzo del informe, veremos patrocinadores del proyecto solo porque son los únicos que se puede abrir un vale del proyecto.

 ![](media/desktop-create-and-manage-relationships/candmrel_repcrossfilteractive.png)

Podemos cambiar la relación activa y obtener SubmittedBy en lugar de OpenedBy. En Administrar relaciones, desactivamos la relación ProjectTickets(OpenedBy) con EmployeeRole(Employee) y, a continuación, activamos la relación Project Tickets(SubmittedBy) con EmployeeRole(Employee).

![](media/desktop-create-and-manage-relationships/candmrel_managerelactivesubmittedby.png)

## <a name="see-all-of-your-relationships-in-relationship-view"></a>Vea todas las relaciones en la vista de relaciones
A veces, el modelo tiene varias tablas y relaciones complejas entre ellas. Vista de relaciones en Power BI Desktop muestra todas las relaciones en el modelo, su dirección y la cardinalidad en un diagrama personalizable y fácil de entender. Para más información, consulte [Vista de relaciones en Power BI Desktop](desktop-relationship-view.md).

