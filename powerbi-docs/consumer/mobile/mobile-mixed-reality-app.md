---
title: Aplicación Power BI for Mixed Reality (versión preliminar)
description: Vea los paneles e informes en la aplicación Power BI for Mixed Reality (versión preliminar), tanto si está inmerso en el mundo virtual como si se encuentra en el contexto de su entorno.
author: mshenhav
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 06/05/2018
ms.author: mshenhav
ms.openlocfilehash: 443615a64bee1f4723450c6c8cc3c49feb81989c
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "61374062"
---
# <a name="power-bi-for-mixed-reality-app-preview"></a>Aplicación Power BI for Mixed Reality (versión preliminar)
Vea los paneles e informes en la aplicación Power BI for Mixed Reality (versión preliminar), tanto si está inmerso en el mundo virtual como si los coloca en ubicaciones específicas en el contexto de su entorno. 

[Descargue la aplicación Power BI para Mixed Reality](https://www.microsoft.com/p/power-bi-mobile/9nblgggzlxn1?activetab=pivot%3aoverviewtab) de la Tienda Windows: En Windows Store, se llama "Power BI Mobile". Interactúe con sus paneles e informes en el mundo virtual y luego seleccione los que quiera aplicar. 

## <a name="two-views-windows-classic-and-holographic"></a>Dos vistas: clásica de Windows y holográfica

Power BI for Mixed Reality se basa en la aplicación móvil Power BI para Windows con capacidades adicionales únicas para realidad mixta. Cuando inicia Power BI for Mixed Reality, se encuentra en la vista "clásica" de Windows de Power BI. En esta vista, puede navegar entre los paneles y los informes a los que tiene acceso. Cuando encuentre uno que le interese, puede cambiar de la vista clásica de Windows a la experiencia holográfica. 


## <a name="windows-classic-view-basics"></a>Conceptos básicos de la vista clásica de Windows

Si no está familiarizado con la experiencia de realidad mixta, esta sección puede interesarle. Interactuar con una aplicación de realidad mixta es diferente de interactuar con un equipo o incluso con una tableta o teléfono. En la vista clásica de Windows, las aplicaciones de realidad mixta responden ante un conjunto de gestos y comandos de voz que reemplazan el teclado y el mouse tradicional, o las teclas del teléfono. 

**Pulsar en el aire**

El gesto de pulsación en el aire es el más básico que debe conocer para interactuar con casi cualquier aplicación de realidad mixta. Con la mano en alto, se pulsa con el dedo índice sobre el dedo pulgar, con un movimiento similar a un clic de mouse o una pulsación de tecla de teléfono.  

![Gesto de pulsación en el aire en realidad mixta](./media/mobile-mixed-reality-app/power-bi-hololens-airtap.png)

En Power BI, se usa la pulsación en el aire en la vista clásica de Windows para cualquier acción con la que haría clic con el mouse. Puede pulsar en el aire para abrir un panel o un informe en el área de trabajo o pulsar en el aire sobre una parte de un objeto visual para filtrarlo o resaltar de forma cruzada otros objetos visuales, etc.

![Pulsar en el aire con la mano en Power BI](./media/mobile-mixed-reality-app/power-bi-hololens-airtap-hand.png) 

Si quiere saber más, lea [Gestures](https://developer.microsoft.com/windows/mixed-reality/gestures) (Gestos).

**Anclar un elemento** 

Pulse en el aire sobre el icono **Anclar** ![icono de anclar](./media/mobile-mixed-reality-app/power-bi-hololens-pin.png) para anclar un panel o un informe de la vista clásica de Windows en la vista holográfica. Puede anclar varios elementos en la vista holográfica. 

**Cambiar a la vista holográfica**

Después de anclar elementos en la vista clásica de Windows, pulse en el aire en el icono **Pantalla completa** ![Icono de pantalla completa](./media/mobile-mixed-reality-app/power-bi-hololens-fullscreen.png) para cambiar a vista holográfica. 


## <a name="holographic-view-basics"></a>Conceptos básicos de la vista holográfica

Una vez que está en la vista holográfica, todos los artefactos que haya anclado se muestran en la cinta de acoplamiento. Puede colocar estos elementos anclados en ubicaciones específicas del espacio físico, como por ejemplo, junto a la pieza de equipo que el elemento está describiendo. En la vista holográfica, los comandos de voz complementan los gestos de mano. Estos son algunos comandos de voz habituales.

**"Follow me"** (Sígueme) 

Recoger un artefacto de Power BI para que permanezca en su campo de visión principal y seguir su mirada hasta que lo coloque en algún lugar.

**"Dock"** (Acoplar) 

Con este comando puede colocar un artefacto en la cinta de acoplamiento de Power BI, de modo que le seguirá, fuera de su campo de visión principal, para un acceso sencillo.

**"Place here"** (Colocar aquí)

Este comando coloca un panel o un informe en una pared o un objeto, o queda flotando en el espacio.

![Colocación de un panel en el espacio](./media/mobile-mixed-reality-app/power-bi-hololens-place-visuals.png)

**"Go home"** (Ir a inicio)

Este comando le lleva a la vista clásica de Windows de Power BI. 

**"Remove"** (Quitar)

Este comando quita un artefacto de la vista holográfica.

**"Remove all"** (Quitar todo) 

Use este comando para quitar todos los artefactos de la vista holográfica.


## <a name="scan-a-report-qr-code-in-holographic-view"></a>Escanear un código QR en la vista holográfica

Puede escanear el código QR para un informe en la vista holográfica, igual que cuando [escanea códigos QR con la aplicación móvil Power BI](mobile-apps-qr-code.md) para iPhone y Android.

- En la vista holográfica, mire un código QR. Power BI abre el informe asociado con ese código QR.

## <a name="limitations-and-considerations"></a>Limitaciones y consideraciones

Hay algunas limitaciones y consideraciones sobre la vista holográfica.

- No se ve el filtrado cruzado o el resaltado que haya podido establecer en la vista clásica de Windows.
- La vista de los informes y paneles anclados es privada. Actualmente no se admiten experiencias compartidas.
- Los paneles y los informes se actualizan cada 45 segundos, cuando los datos cambian.


## <a name="next-steps"></a>Pasos siguientes

- [Obtención de datos procedentes del mundo real con las aplicaciones móviles de Power BI](mobile-apps-data-in-real-world-context.md)

 



