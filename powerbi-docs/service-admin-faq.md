---
title: 'Administración de Power BI: preguntas más frecuentes (P+F)'
description: Conozca las respuestas a las preguntas más frecuentes sobre Power BI, regístrese, administración de inquilinos y otras tareas administrativas.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 11/16/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: 2e51017333a940bd9d7838e6a903c1a66ce2e342
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "65100774"
---
# <a name="administering-power-bi---frequently-asked-questions-faq"></a>Administración de Power BI: preguntas más frecuentes (P+F)

En este artículo se tratan las preguntas más frecuentes para la administración de Power BI. Para obtener información general sobre la administración de Power BI, vea [¿Qué es la administración de Power BI?](service-admin-administering-power-bi-in-your-organization.md)

## <a name="whats-in-this-article"></a>Contenido de este artículo

### <a name="sign-up-for-power-bi-section"></a>Sección Suscribirse en Power BI

* [Uso de PowerShell](#using-powershell)
* [¿Cómo se suscriben los usuarios a Power BI?](#how-do-users-sign-up-for-power-bi)
* [¿Cómo se suscriben los usuarios individuales de mi organización?](#how-do-individual-users-in-my-organization-sign-up)
* [¿Cómo puedo impedir que los usuarios se unan a mi inquilino de Office 365 existente?](#how-can-i-prevent-users-from-joining-my-existing-office-365-tenant)
* [¿Cómo puedo permitir que los usuarios se unan a mi inquilino de Office 365 existente?](#how-can-i-allow-users-to-join-my-existing-office-365-tenant)
* [¿Cómo se puede comprobar si tengo el bloque activado en el inquilino?](#how-do-i-check-if-i-have-the-block-on-in-the-tenant)
* [¿Cómo puedo impedir que mis usuarios existentes comiencen a usar Power BI?](#how-can-i-prevent-my-existing-users-from-starting-to-use-power-bi)
* [¿Cómo puedo permitir a mis usuarios existentes que se suscriban a Power BI?](#how-can-i-allow-my-existing-users-to-sign-up-for-power-bi)

### <a name="administration-of-power-bi-section"></a>Sección Administración de Power BI

* [¿Cómo cambiará esto la manera de administrar identidades para usuarios de mi organización hoy?](#how-will-this-change-the-way-i-manage-identities-for-users-in-my-organization-today)
* [¿Cómo se administra Power BI?](#how-do-we-manage-power-bi)
* [¿Cuál es el proceso para administrar un inquilino creado por Microsoft para mis usuarios?](#what-is-the-process-to-manage-a-tenant-created-by-microsoft-for-my-users)
* [Si tengo varios dominios, ¿puedo controlar al inquilino de Office 365 que los usuarios se agregan a?](#if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-get-added-to)
* [¿Cómo quito Power BI para los usuarios que ya están suscritos?](#how-do-i-remove-power-bi-for-users-that-already-signed-up)
* [¿Cómo sé cuándo nuevos usuarios se han unido a mi inquilino?](#how-do-i-know-when-new-users-have-joined-my-tenant)
* [¿Hay aspectos adicionales para que debo prepararme?](#are-there-any-additional-things-i-should-prepare-for)
* [¿Dónde se encuentra mi inquilino de Power BI?](#where-is-my-power-bi-tenant-located)
* [¿Qué es el Acuerdo de Nivel de Servicio de Power BI?](#what-is-the-power-bi-sla)
* [¿Cómo controla Power BI la alta disponibilidad y la conmutación por error?](#how-does-power-bi-handle-high-availability-and-failover)

### <a name="security-in-power-bi-section"></a>Sección Seguridad en Power BI

* [¿Cumple Power BI los requisitos de cumplimiento nacionales, regionales y específicos del sector?](#does-power-bi-meet-national-regional-and-industry-specific-compliance-requirements)
* [¿Cómo funciona la seguridad en Power BI?](#how-does-security-work-in-power-bi)

## <a name="sign-up-for-power-bi"></a>Suscribirse en Power BI

### <a name="using-powershell"></a>Uso de PowerShell

Algunos de los procedimientos descritos en esta sección requieren los scripts de Windows PowerShell. Si no está familiarizado con PowerShell, se recomienda leer la [Guía de introducción de PowerShell](http://go.microsoft.com/fwlink/p/?LinkID=286814). Para ejecutar los scripts, instale primero la última versión de 64 bits de [PowerShell de Azure Active Directory para Graph](/powershell/azure/active-directory/).

### <a name="how-do-users-sign-up-for-power-bi"></a>¿Cómo se suscriben los usuarios a Power BI?

Como administrador, puede suscribirse a Power BI a través de la [sitio web de Power BI](https://powerbi.microsoft.com) o [comprar servicios](https://admin.microsoft.com/AdminPortal/Home#/catalog) página en el centro de administración de Microsoft 365. Cuando un administrador se suscribe a Power BI, pueden asignar licencias de usuario a los usuarios que deben tener acceso.

Además, los usuarios individuales de la organización pueden suscribirse a Power BI a través del [sitio web de Power BI](https://powerbi.microsoft.com). Cuando un usuario de la organización se suscribe a Power BI, el servicio asigna automáticamente una licencia de Power BI para el usuario. Para obtener más información, consulte [suscriban a Power BI como usuario individual](service-self-service-signup-for-power-bi.md) y [licencias de Power BI en su organización](service-admin-licensing-organization.md).

### <a name="how-do-individual-users-in-my-organization-sign-up"></a>¿Cómo se suscriben los usuarios individuales de mi organización?

Hay tres escenarios que se podrían aplicarse a los usuarios de su organización:

* **Escenario 1**: Su organización ya tiene un entorno de Office 365 existente y el usuario que se suscribe a Power BI ya tiene una cuenta de Office 365.
    En este escenario, si un usuario ya tiene un trabajo o cuenta educativa en el inquilino (por ejemplo, contoso.com) pero todavía no tiene Power BI, Microsoft activa simplemente el plan para esa cuenta. Automáticamente se notifica al usuario con información sobre cómo usar el servicio Power BI.

* **Escenario 2**: Su organización tiene un entorno de Office 365 existente, pero el usuario que se suscribe a Power BI no tiene una cuenta de Office 365.
    En este escenario, el usuario tiene una dirección de correo electrónico en el dominio de su organización (por ejemplo, contoso.com) pero todavía no tiene una cuenta de Office 365. En este caso, el usuario puede suscribirse a Power BI y automáticamente se le asigna una cuenta. Esta acción permite al usuario acceso el servicio Power BI. Por ejemplo, si una empleada llamada Nancy usa su trabajo dirección de correo electrónico (como nancy@contoso.com) para suscribirse, Microsoft agrega automáticamente Nancy como un usuario en el entorno de Office 365 de Contoso y activa de Power BI para esa cuenta.

* **Escenario 3**: Su organización no tiene un entorno de Office 365 conectado al dominio de correo electrónico.
    No hay ninguna acción administrativa que su organización necesita para aprovechar las ventajas de Power BI. El servicio agrega a los usuarios al directorio del usuario nuevo, en la nube. También puede tomar el control como el Administrador de inquilinos y administrarlos.

> [!IMPORTANT]
> Si su organización tiene varios dominios de correo y usted prefiere que todas las extensiones de dirección de correo estén en el mismo inquilino, agregue todos los dominios de dirección de correo a un inquilino de Azure Active Directory antes de suscribir ningún usuario. Una vez que ha creado usuarios, no hay ningún mecanismo automático para mover usuarios entre inquilinos. Para obtener más información sobre este proceso, consulte [si tengo varios dominios, ¿puedo controlar el inquilino de Office 365 que los usuarios se agregan a?](#if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-get-added-to) más adelante en este artículo y [agregar un dominio a Office 365](/office365/admin/setup/add-domain/).

### <a name="how-can-i-prevent-users-from-joining-my-existing-office-365-tenant"></a>¿Cómo puedo impedir que los usuarios se unan a mi inquilino de Office 365 existente?

Hay pasos que puede realizar, como administrador, para impedir que los usuarios se unan a su inquilino de Office 365 existente. Si se bloquea el acceso, los intentos de los usuarios a registrarse por error, y aparece un mensaje que dirija a ponerse en contacto con el Administrador de. su organización No es necesario repetir este proceso si ya ha deshabilitado la distribución automática de licencias (por ejemplo, a través de Office 365 para educación para estudiantes, profesores y personal).

Use el siguiente script de PowerShell para impedir que los nuevos usuarios se unan a un inquilino administrado. ([Más información sobre PowerShell][1].)

```powershell
$msolcred = get-credential
connect-msolservice -credential $msolcred

Set-MsolCompanySettings -AllowEmailVerifiedUsers $false
```

> [!NOTE]
> El bloqueo del acceso impide que los nuevos usuarios de su organización se suscriban a Power BI. Los usuarios que se suscriben a Power BI antes de deshabilitar nuevas suscripciones para su organización aún conservarán sus licencias. Para quitar un usuario, consulte [¿Cómo quito Power BI para los usuarios que ya están suscritos?](#how-do-i-remove-power-bi-for-users-that-already-signed-up) más adelante en este artículo.

### <a name="how-can-i-allow-users-to-join-my-existing-office-365-tenant"></a>¿Cómo puedo permitir que los usuarios se unan a mi inquilino de Office 365 existente?

Use el siguiente script de PowerShell para permitir que los usuarios nuevos unirse a un inquilino administrado. ([Más información sobre PowerShell][1].)

```powershell
$msolcred = get-credential
connect-msolservice -credential $msolcred

Set-MsolCompanySettings -AllowEmailVerifiedUsers $true
```

### <a name="how-do-i-check-if-i-have-the-block-on-in-the-tenant"></a>¿Cómo se puede comprobar si tengo el bloque activado en el inquilino?

Use el siguiente script de PowerShell para comprobar la configuración. *AllowEmailVerifiedUsers* debe ser false. ([Más información sobre PowerShell][1].)

```powershell
$msolcred = get-credential
connect-msolservice -credential $msolcred

Get-MsolCompanyInformation | fl allow*
```

### <a name="how-can-i-prevent-my-existing-users-from-starting-to-use-power-bi"></a>¿Cómo puedo impedir que mis usuarios existentes comiencen a utilizar Power BI?

La opción de configuración de Azure AD que controla esto es **AllowAdHocSubscriptions**. La mayoría de los inquilinos tienen establecido como true, lo que significa que está habilitada. Si ha adquirido Power BI a través de un asociado, se puede establecer en false, lo que significa que está deshabilitado.

Use el siguiente script de PowerShell para deshabilitar las suscripciones ad hoc. ([Más información sobre PowerShell][1].)

1. Inicie sesión en Azure Active Directory usando sus credenciales de Office 365. La primera línea del siguiente script de PowerShell le pide las credenciales. La segunda línea se conecta a Azure Active Directory.

    ```powershell
     $msolcred = get-credential
     connect-msolservice -credential $msolcred
    ```

   ![Inicio de sesión de captura de pantalla de Azure Active Directory a través de PowerShell](media/service-admin-licensing-organization/azure-ad-sign-in.png)

1. Una vez que inicie sesión, ejecute el siguiente comando para ver cómo el inquilino configurado actualmente.

    ```powershell
     Get-MsolCompanyInformation | fl AllowAdHocSubscriptions
    ```

1. Ejecute el siguiente comando para habilitar (`$true`) o deshabilitar (`$false`) **AllowAdHocSubscriptions**.

    ```powershell
     Set-MsolCompanySettings -AllowAdHocSubscriptions $false
    ```

> [!NOTE]
> Use la **AllowAdHocSubscriptions** marca para controlar varias funcionalidades de usuario de su organización, incluida la capacidad para los usuarios se registren para el servicio Azure Rights Management. El cambio de esta marca afecta a todas estas funcionalidades.

### <a name="how-can-i-allow-my-existing-users-to-sign-up-for-power-bi"></a>¿Cómo puedo permitir a mis usuarios existentes que se suscriban a Power BI?

Para permitir que los usuarios existentes registrarse en Power BI, ejecute el comando enumerado para la pregunta anterior, pero pase `$true` en lugar de `$false` en el último paso.

## <a name="administration-of-power-bi"></a>Administración de Power BI

### <a name="how-will-this-change-the-way-i-manage-identities-for-users-in-my-organization-today"></a>¿Cómo cambiará esto la manera de administrar identidades para usuarios de mi organización hoy?

Hay tres escenarios que se podrían aplicarse a los usuarios de su organización:

* **Escenario 1**: Si su organización ya tiene un entorno de Office 365 existente y todos los usuarios de su organización tienen cuentas de Office 365, no hay ningún cambio en cómo administrar la identidad.

* **Escenario 2**: Si su organización ya tiene un entorno de Office 365 existente pero no todos los usuarios de su organización tienen cuentas de Office 365, crearemos un usuario en el inquilino y asignaremos licencias basadas en correo electrónico escolar o de trabajo del usuario.

    Como resultado, el número de usuarios que se está administrando en cualquier momento determinado crece a medida que se suscriben los usuarios de su organización para el servicio.

* **Escenario 3**: Si su organización no tiene un entorno de Office 365 conectado al dominio de correo electrónico, no hay ningún cambio en cómo administrar la identidad.

    El servicio agrega a los usuarios al directorio del usuario nuevo, en la nube. Además, puede tomar el control como el Administrador de inquilinos y administrarlos.

### <a name="how-do-we-manage-power-bi"></a>¿Cómo se administra Power BI?

Power BI proporciona un portal de administración que le permite ver las estadísticas de uso, proporciona un vínculo al centro de administración de Microsoft 365 para administrar usuarios y grupos y proporciona la capacidad para controlar la configuración de los inquilinos.

Para usar el portal de administración de Power BI, debe marcar la cuenta como un **administrador Global** dentro de Office 365 o Azure Active Directory, o alguien debe asignar el rol de administrador del servicio Power BI a su cuenta de usuario. Para obtener más información, consulte [descripción del rol de administrador de Power BI](service-admin-role.md) y [Portal de administración de Power BI](service-admin-portal.md).

### <a name="what-is-the-process-to-manage-a-tenant-created-by-microsoft-for-my-users"></a>¿Cuál es el proceso para administrar un inquilino creado por Microsoft para mis usuarios?

Cuando un usuario de autoservicio se suscribe a un servicio en la nube que usa Azure AD, el servicio agrega a una instancia de Azure no administrado en función de directorio de AD de su dominio de correo electrónico. Puede reclamar y administrar el inquilino que haya creado alguien mediante un proceso conocido como un *la adquisición de administración*. El tipo de adquisición que realice depende de si hay una existente administrada asociado con el dominio del inquilino:

* Utilice una *adquisición interna* para crear otro inquilino administrado para el dominio.

* Utilice una *adquisición externa* para mover el dominio a un inquilino administrado existente.

Para obtener más información, consulte [adquirir un directorio no administrado como administrador en Azure Active Directory](/azure/active-directory/users-groups-roles/domains-admin-takeover).

Al realizar una adquisición externa, el servicio coloca contenido que se creó antes de la adquisición de Power BI un [área de trabajo de Power BI archivado](service-admin-power-bi-archived-workspace.md). Debe migrar manualmente cualquier contenido que quiera utilizar en el nuevo inquilino.

### <a name="if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-get-added-to"></a>Si tengo varios dominios, ¿puedo controlar al inquilino de Office 365 que los usuarios se agregan a?

Si no hace nada, el servicio crea a un inquilino para cada dominio de correo electrónico del usuario y el subdominio. Si desea que todos los usuarios se encuentren en el mismo inquilino independientemente de sus extensiones de dirección de correo electrónico: Crear a un inquilino de destino antes de tiempo, o usar a un inquilino existente. A continuación, agregue todos los dominios y subdominios existentes que desee consolidados dentro de ese inquilino. Todos los usuarios con direcciones de correo electrónico que terminen en esos dominios y subdominios automáticamente Únase al inquilino de destino cuando se registren.

> [!IMPORTANT]
> Una vez que ha creado usuarios, no hay ningún mecanismo automático admitido para mover usuarios entre inquilinos. Para obtener información sobre cómo agregar dominios a un solo inquilino de Office 365, consulte [Pasos para comprobar dominio en Office 365](/office365/admin/setup/add-domain/).

### <a name="how-do-i-remove-power-bi-for-users-that-already-signed-up"></a>¿Cómo quito Power BI para los usuarios que ya están suscritos?

Si un usuario se suscribió a Power BI, pero ya no desea que tenga acceso a Power BI, puede quitar la licencia de Power BI para ese usuario.

1. Vaya al [Centro de administración de Microsoft 365](https://admin.microsoft.com/AdminPortal/Home#/homepage).

1. En la barra de navegación izquierda, seleccione **Usuarios** > **Usuarios activos**.

1. Busque el usuario para el que desea quitar la licencia y seleccione su nombre.

    También puede realizar la administración masiva de licencias para los usuarios. Para ello, seleccione varios usuarios y luego **Editar licencias de productos**.

1. En la página de detalles del usuario, junto a **Licencias de productos**, seleccione **Editar**.

1. Dependiendo de qué licencia se aplica a su cuenta, establezca **Power BI (gratis)** o **Power BI Pro** a **desactivar**.

1. Seleccione **Guardar**.

### <a name="how-do-i-know-when-new-users-have-joined-my-tenant"></a>¿Cómo sé cuándo nuevos usuarios se han unido a mi inquilino?

Los usuarios que se han unido al inquilino como parte de este programa se asignen una licencia única que puede filtrar en el panel de usuarios activos en el panel de administración. Para crear esta vista, siga estos pasos.

1. Vaya al [Centro de administración de Microsoft 365](https://admin.microsoft.com/AdminPortal/Home#/homepage).

1. En la barra de navegación izquierda, seleccione **Usuarios** > **Usuarios activos**.

1. En el menú **Vistas**, seleccione **Agregar vista personalizada**.

1. Asigne un nombre a la nueva vista y, en **Licencia de producto asignada**, seleccione **Power BI (gratis)** o **Power BI Pro**.

    Solo puede tener una licencia seleccionada por vista. Si tiene tanto la licencia **Power BI (gratis)** como la licencia **Power BI Pro** en su organización, puede crear dos vistas.

1. Escriba cualquier otra condición que desee y después seleccione **Agregar**.

1. Después de crear la nueva vista, está disponible en el **vistas** menú.

### <a name="are-there-any-additional-things-i-should-prepare-for"></a>¿Hay aspectos adicionales para que debo prepararme?

Es posible que experimente un aumento en las solicitudes de restablecimiento de contraseña. Para obtener información acerca de este proceso, consulte [restablecer una contraseña de usuario](/office365/admin/add-users/reset-passwords).

Puede quitar un usuario del inquilino mediante el proceso estándar en el Centro de administración de Microsoft 365. Sin embargo, si el usuario todavía tiene una dirección de correo electrónico activa de su organización, puede volver a unirse a menos que bloquee todos los usuarios para impedirles que se unan.

### <a name="where-is-my-power-bi-tenant-located"></a>¿Dónde se encuentra mi inquilino de Power BI?

Para obtener información acerca de qué región de datos de su inquilino de Power BI está en, consulte [donde se encuentra mi inquilino de Power BI?](service-admin-where-is-my-tenant-located.md).

### <a name="what-is-the-power-bi-sla"></a>¿Qué es el Acuerdo de Nivel de Servicio?

Para obtener información sobre el SLA de Power BI (contrato de nivel de servicio), consulte el [términos de licencia y la documentación](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37) el artículo en el **Licensing** sección del sitio Web de Microsoft Licensing.

### <a name="how-does-power-bi-handle-high-availability-and-failover"></a>¿Cómo controla Power BI la alta disponibilidad y la conmutación por error?

Para obtener información sobre la alta disponibilidad y conmutación por error, consulte [Power BI alta disponibilidad, conmutación por error y recuperación de desastres preguntas más frecuentes sobre](service-admin-failover.md).

## <a name="security-in-power-bi"></a>Seguridad en Power BI

### <a name="does-power-bi-meet-national-regional-and-industry-specific-compliance-requirements"></a>¿Cumple Power BI los requisitos de cumplimiento nacionales, regionales y específicos del sector?

Para obtener más información acerca de la compatibilidad de Power BI, consulte el [Centro de confianza de Microsoft](https://www.microsoft.com/TrustCenter/CloudServices/business-application-platform/default.aspx).

### <a name="how-does-security-work-in-power-bi"></a>¿Cómo funciona la seguridad en Power BI?

Microsoft creó Power BI en la base de Office 365, que a su vez se basa en servicios de Azure como Azure Active Directory. Para obtener información general de la arquitectura de Power BI, vea [Seguridad de Power BI](service-admin-power-bi-security.md).

## <a name="next-steps"></a>Pasos siguientes

[Portal de administración de Power BI](service-admin-portal.md)  
[Descripción del rol de administrador de Power BI](service-admin-role.md)  
[Registro de autoservicio para Power BI](service-self-service-signup-for-power-bi.md)  
[Adquisición de Power BI Pro](service-admin-purchasing-power-bi-pro.md)  
[¿Qué es Power BI Premium?](service-premium-what-is.md)  
[Cómo comprar Power BI Premium](service-admin-premium-purchase.md)  
[Notas del producto de Power BI Premium](https://aka.ms/pbipremiumwhitepaper)  
[Administración del grupo en Power BI y Office 365](service-manage-app-workspace-in-power-bi-and-office-365.md)  
[Administración de cuentas de usuario de Office 365](/office365/servicedescriptions/office-365-platform-service-description/user-account-management/)  
[Administración de grupos de Office 365](/office365/admin/email/create-edit-or-delete-a-security-group/)  

¿Tiene más preguntas? [Pruebe a preguntar a la comunidad de Power BI](http://community.powerbi.com/)

[1]: https://docs.microsoft.com/powershell/scripting/overview