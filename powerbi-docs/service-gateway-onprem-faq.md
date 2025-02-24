---
title: Preguntas más frecuentes sobre la puerta de enlace de datos local
description: Estas son las preguntas más frecuentes sobre la puerta de enlace de datos local. Aquí se reúnen en un solo lugar las preguntas más frecuentes sobre la puerta de enlace.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: conceptual
ms.date: 01/24/2018
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: b1c74968365db59d51f7c0a7bdb356552cc75596
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/15/2019
ms.locfileid: "54283791"
---
# <a name="on-premises-data-gateway-faq"></a>Preguntas más frecuentes sobre la puerta de enlace de datos local
<!-- Shared FAQ shared Include -->
[!INCLUDE [gateway-onprem-faq-shared-include](./includes/gateway-onprem-faq-shared-include.md)]

## <a name="analysis-services"></a>Analysis Services
**Pregunta:** ¿Puedo usar msdmpump.dll para crear asignaciones personalizadas de nombres de usuario efectivos para Analysis Services?  
**Respuesta:** No. Esa capacidad no se admite en este momento.

**Pregunta:** ¿Puedo usar la puerta de enlace para la conexión a una instancia multidimensional (OLAP)?  
**Respuesta:** Sí. La puerta de enlace de datos local admite conexiones dinámicas a los modelos tabular y multidimensional de Analysis Services.

**Pregunta:** ¿Qué ocurre si instalo la puerta de enlace en un equipo en un dominio distinto del de mi servidor local que usa la autenticación de Windows?  
**Respuesta:** No hay nada seguro en este caso. Todo depende de la relación de confianza entre los dos dominios. Si los dos dominios diferentes están en un modelo de dominio de confianza, la puerta de enlace podría ser capaz de conectarse al servidor de Analysis Services y se podría resolver el nombre de usuario efectivo. Si no es así, se puede producir un error de inicio de sesión.

**Pregunta:** ¿Cómo puedo averiguar qué nombre de usuario efectivo se pasa a mi servidor de Analysis Services local?  
**Respuesta:** Respondemos en el [artículo de solución de problemas](service-gateway-onprem-tshoot.md).

**Pregunta:** Tengo 25 bases de datos en Analysis Services, ¿hay alguna forma de habilitarlas todas a la vez para la puerta de enlace?  
**Respuesta:** No. Está en el mapa de ruta pero no tenemos un margen de tiempo.

## <a name="administration"></a>Administración
**Pregunta:** ¿Puedo tener más de un administrador de una puerta de enlace?  
**Respuesta:** Sí. Al administrar una puerta de enlace, puede ir a la pestaña del administrador para agregar administradores adicionales.

**Pregunta:** ¿El administrador de la puerta de enlace debe ser un administrador en el equipo donde está instalada la puerta de enlace?  
**Respuesta:** No. El administrador de la puerta de enlace se usa para administrarla desde el servicio.

**Pregunta:** ¿Puedo evitar que los usuarios de mi organización creen una puerta de enlace?  
**Respuesta:** No. Está en el mapa de ruta pero no tenemos un margen de tiempo.

**Pregunta:** ¿Puedo obtener información de uso y estadísticas de las puertas de enlace de mi organización?  
**Respuesta:** No. Está en el mapa de ruta pero no tenemos un margen de tiempo.

## <a name="power-bi"></a>Power BI
**Pregunta:** ¿Necesito actualizar la puerta de enlace personal?
**Respuesta:** No, puede seguir usando la puerta de enlace personal para Power BI.

**Pregunta:** ¿Con qué frecuencia se actualizan los iconos de un panel de Power BI cuando se conecta a través de la puerta de enlace de datos local?  
**Respuesta:** Cada diez minutos aproximadamente. Es la frecuencia de las conexiones DirectQuery. Esto no significa que un icono emite una consulta en el servidor local y muestra datos nuevos cada diez minutos.

**Pregunta:** ¿Puedo cargar libros de Excel con modelos de datos de Power Pivot que se conectan a orígenes de datos locales? ¿Necesito una puerta de enlace para este escenario?  
**Respuesta:** Sí, puede cargar el libro. Y no, no necesita una puerta de enlace. Sin embargo, dado que los datos residen en el modelo de datos de Excel, los informes de Power BI basados en el libro de Excel no serán dinámicos. Para actualizar los informes de Power BI, deberá volver a cargar un libro actualizado cada vez. O bien, use la puerta de enlace con la actualización programada.

**Pregunta:** Si los usuarios comparten paneles con una conexión DirectQuery, ¿los otros usuarios podrán ver los datos aunque que no tengan los mismos permisos?  
**Respuesta:** Para un panel conectado a Analysis Services, los usuarios sólo verán los datos a los que tienen acceso. Si los usuarios no tienen los mismos permisos, no podrán ver ningún dato. Para otros orígenes de datos, todos los usuarios compartirán las credenciales especificadas por el administrador para ese origen de datos.

**Pregunta:** ¿Por qué no puedo conectarme a mi servidor de Oracle?  
**Respuesta:** Es posible que tenga que instalar el cliente de Oracle y configurar el archivo tnsnames.ora con la información correcta del servidor. Se trata de una instalación independiente fuera de la puerta de enlace. Para obtener más información, consulte [Instalación del cliente de Oracle](service-gateway-onprem-manage-oracle.md#installing-the-oracle-client).

**Pregunta:** ¿Funcionará la puerta de enlace con ExpressRoute?  
**Respuesta:** Sí. Para obtener más información acerca de ExpressRoute y Power BI, consulte [Power BI y ExpressRoute](service-admin-power-bi-expressroute.md).

**Pregunta:** Estoy usando scripts de R. ¿Está admitido?
**Respuesta:** Los scripts de R solo son compatibles con el modo personal.

## <a name="next-steps"></a>Pasos siguientes
[On-premises Data Gateway (Puerta de enlace de datos local)](service-gateway-onprem.md)  
[Detalles sobre la puerta de enlace de datos local](service-gateway-onprem-indepth.md)  
[Solución de problemas con la puerta de enlace de datos local](service-gateway-onprem-tshoot.md)  
¿Tiene más preguntas? [Pruebe la comunidad de Power BI](http://community.powerbi.com/)

