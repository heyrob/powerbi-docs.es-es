---
title: Conexión a Planview Enterprise con Power BI
description: Planview Enterprise para Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 6095faca7fd0d7d42fd6b3871c9e45658a32a14f
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "61163130"
---
# <a name="connect-to-planview-enterprise-with-power-bi"></a>Conexión a Planview Enterprise con Power BI
El paquete de contenido de Planview Enterprise permite visualizar los datos de administración de recursos y del trabajo de una forma totalmente nueva directamente en Power BI. Utilice sus credenciales de inicio de sesión de Planview Enterprise para ver de forma interactiva el gasto de la inversión de cartera, comprender dónde supera el presupuesto y dónde no lo alcanza, y averiguar el grado de alineación de sus proyectos con las prioridades estratégicas corporativas. También puede ampliar el panel integrado y los informes para obtener la información más importante para usted.

Conéctese al [paquete de contenido de Planview Enterprise en Power BI](https://app.powerbi.com/getdata/services/planview-enterprise)

>[!NOTE]
>Para importar datos de Planview Enterprise en Power BI, debe ser un usuario de Planview Enterprise con la característica Visor del portal de informes habilitada en su rol. Consulte los requisitos adicionales siguientes.

## <a name="how-to-connect"></a>Cómo conectarse
1. Seleccione **Obtener datos** en la parte inferior del panel de navegación izquierdo.
   
    ![](media/service-connect-to-planview/get.png)
2. En el cuadro **Servicios** , seleccione **Obtener**.
   
    ![](media/service-connect-to-planview/services.png)
3. En la página de Power BI, seleccione **Planview Enterprise** y, después, seleccione **Obtener**:  
    ![](media/service-connect-to-planview/planview.png)
4. En el cuadro de texto Dirección URL de Planview Enterprise, escriba la dirección URL del servidor de Planview Enterprise que desea usar. En el cuadro de texto Base de datos de Planview Enterprise, escriba el nombre de la base de datos de Planview Enterprise y, después, haga clic en Siguiente.  
    ![](media/service-connect-to-planview/params.png)
5. En la lista Método de autenticación, seleccione la opción **Básico** si no está seleccionada. Escriba el **nombre de usuario** y la **contraseña** de su cuenta y seleccione **Iniciar sesión**.  
   ![](media/service-connect-to-planview/creds.png)
6. En el panel izquierdo, seleccione Planview Enterprise en la lista de paneles.  
     Power BI importa los datos de Planview Enterprise en el panel. Tenga en cuenta que los datos pueden tardar cierto tiempo en cargarse.  
    ![](media/service-connect-to-planview/dashboard.png)

**¿Qué más?**

* Pruebe a [hacer una pregunta en el cuadro de preguntas y respuestas](consumer/end-user-q-and-a.md), en la parte superior del panel.
* [Cambie los iconos](service-dashboard-edit-tile.md) en el panel.
* [Seleccione un icono](consumer/end-user-tiles.md) para abrir el informe subyacente.
* Aunque el conjunto de datos se programará para actualizarse diariamente, puede cambiar la programación de actualización o intentar actualizar a petición mediante **Actualizar ahora**

## <a name="system-requirements"></a>Requisitos del sistema
Para importar datos de Planview Enterprise en Power BI, debe ser un usuario de Planview Enterprise con la característica Visor del portal de informes habilitada en su rol. Consulte los requisitos adicionales siguientes.

En este procedimiento se supone que ya ha iniciado sesión en la página principal de Microsoft Power BI con una cuenta de Power BI. Si no tiene una cuenta de Power BI, vaya a [powerbi.com](https://powerbi.microsoft.com/get-started/) y, en **Power BI: Colaboración y uso compartido en la nube**, seleccione **Probar gratis**. A continuación, haga clic en **Obtener datos**.

## <a name="next-steps"></a>Pasos siguientes:

[¿Qué es Power BI?](power-bi-overview.md)

[Obtener datos para Power BI](service-get-data.md)