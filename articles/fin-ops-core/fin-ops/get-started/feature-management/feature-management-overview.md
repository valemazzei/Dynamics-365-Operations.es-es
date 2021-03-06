---
title: Vista previa de Administración de características
description: Este tema describe la función de Administración de características y cómo puede utilizarla.
author: ChrisGarty
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 82c8172958f819735ea3f29fc331272f80b3a25a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692975"
---
# <a name="feature-management-overview"></a>Visión general de la administración de características

[!include [banner](../../includes/banner.md)]

Las características se suman y se actualizan en cada versión. La experiencia de administración de la característica proporciona un espacio de trabajo en el que puede ver una lista de características que se han entregado en cada versión. De forma predeterminada, las nuevas características están desactivadas. Puede usar el espacio de trabajo para activarlas y ver su documentación.

## <a name="the-feature-management-workspace"></a>El espacio de trabajo Administración de características.

Puede abrir el espacio de trabajo **Administración de características** seleccionando el mosaico adecuado en el panel de información. Verá una página que muestra una lista de características para todos las versiones que son compatibles con la experiencia de Administración de características. Con el tiempo, Microsoft ampliará la experiencia de la Administración de características de modo que incluya funcionalidad adicional para ayudarle a gestionar características.

La lista de características incluye la información siguiente:

- **Nombre de la característica** - Una descripción de la función que se ha agregado.
- **Estado habilitado** - Un símbolo indica si se ha activado una característica (marca de verificación), no está activada (en blanco), se ha programado para ser activada (reloj), es obligatorio activarla (candado), requiere atención antes de activarla (advertencia) o no se puede habilitar (X). El valor que se muestra se usa para todas las entidades jurídicas. Tenga en cuenta que incluso cuando se ha activado, una característica aún se controla mediante la seguridad. Por lo tanto, la característica sólo estará disponible para los usuarios que tengan acceso a ella, en función de su rol de seguridad. También estará disponible solo en las entidades jurídicas a las que tiene acceso el usuario.
- **Fecha de habilitación** - La fecha en que la característica se ha activado o está programado que lo haga.
- **Característica agregada** - La fecha en que la característica se ha agregado al entorno. Esta fecha se introduce automáticamente durante la actualización del entorno durante los ciclos de lanzamiento mensuales.
- **Módulo** - El módulo afectado por la nueva característica.

Al seleccionar una característica, información adicional aparece en el panel de información a la derecha de la lista de la función. En la parte superior del panel podrá ver el nombre de la función, la fecha en la que la característica se ha agregado, el módulo afectado por la función, y un vínculo a **Más información** . Seleccione este vínculo para ver la documentación para la característica. Si la documentación no está disponible, le llevarán a una página temporal. El panel de detalles también incluye un campo **Comentarios** donde puede agregar sus propios comentarios acerca de la característica.

El espacio de trabajo **Administración de características** también tiene varias pestañas y cada una muestra una lista de funciones de ella.

- **Nuevo** - Esta pestaña muestra todas las características que se han agregado desde la última actualización de mensual. Si ha omitido cualquier actualización mensual, la ficha muestra todas las nuevas características que se han agregado desde la última vez que se actualizó. Las características más nuevas aparecen en la parte superior de la lista. El número total de nuevas características también se muestra en un mosaico en la parte superior de la página.
- **No habilitado** - La ficha muestra todas las funciones que no se han activado. Las características más nuevas aparecen en la parte superior de la lista. El número total de nuevas características que no se han activado también se muestra en un mosaico en la parte superior de la página.
- **Programado** - Esta pestaña muestra todas las características que se han programado para ser habilitadas en el futuro. Las características que tienen la fecha programada más próxima aparecen en la parte superior de la lista. El número total de nuevas características programadas también se muestra en un mosaico en la parte superior de la página.
- **Todas** - La ficha muestra todas las funciones. Las características más nuevas aparecen en la parte superior de la lista.

## <a name="turn-on-a-feature"></a>Activar una característica

Si una característica no se ha activado, un botón **Habilitar ahora** aparece en el panel de detalles. Puede usar este botón para activar la característica.

- Seleccione la característica que desea activar y, a continuación, en el panel de detalles, seleccione **Habilitar ahora**. Se activa la función.

Algunas funciones no se pueden desactivar tras activarlas. Si la función que intenta activar no se puede desactivar, se mostrará una advertencia. En este punto, puede seleccionar **Cancelar** para cancelar la operación y para dejar la característica desactivada. Sin embargo, si se selecciona **Habilitar** y activa la característica, no podrá desactivarla posteriormente.

Algunas funciones mostrarán un mensaje con información adicional antes de activarlas. Estas funciones están marcadas con un símbolo amarillo de advertencia. Debe leer la información adicional cuidadosamente para averiguar qué sucederá cuando se habilite la función. No obstante, aún podrá seleccionar **Habilitar** para activar la función.

Algunas funciones mostrarán un mensaje de que la característica no puede habilitarse hasta que se tomen medidas. Estas funciones se indican con un símbolo de una X roja. Debe realizar los pasos que se describen en la descripción antes de que se habilite la función. Por ejemplo, si no puede usar una característica hasta que se deshabilite una clave de configuración, debe deshabilitar la clave de configuración primero y después volver a la administración de características para habilitar la función.

Después de que se active la característica, aparece un mensaje bajo el vínculo **Más información** en el panel de detalles. Este mensaje confirma que la característica se ha activado o indica la fecha futura en la que está programada que se active. Aparecerá cada vez que seleccione la característica en la lista de la función.

Las características programadas para activarse en el futuro aparecen en la pestaña **Programado**. Un proceso por lotes las activará a medianoche en la fecha especificada, en función de la zona horaria que se representa por la fecha del sistema.

## <a name="reschedule-a-feature"></a>Reprogramar una característica

Si una característica se ha programado para activarse en el futuro, un botón **Programar** aparece en el panel de detalles. Puede usar este botón para cambiar el valor de **Fecha de habilitación** a otra distinta.

1. Seleccione la característica programada que desea reprogramar y, a continuación, en el panel de detalles, seleccione **Programar**.
2. En el cuadro de diálogo que aparece, en el campo **Fecha de habilitación**, especifique la nueva fecha en que la característica se debe activar.
3. Seleccione **Habilitar** para volver a programar la característica o **Deshabilitar** para cancelar la programación.

## <a name="turn-off-a-feature"></a>Desactivar una característica

Si una característica ya se ha habilitado, un botón **Deshabilitar** aparece en el panel de detalles. Puede usar este botón para desactivar la característica. El botón **Deshabilitar** no está disponible si la característica no se puede desactivar después de que se active.

- Seleccione la característica que desea desactivar y, a continuación, en el panel de detalles, seleccione **Deshabilitar**. Se desactiva la característica, y se borra el campo **Fecha de habilitación**.

Después de que se desactive la característica, aparece un mensaje bajo el vínculo **Más información** en el panel de detalles. Este mensaje afirma que la característica aún no se ha activado. Aparecerá cada vez que seleccione la característica en la lista de la función. Las funciones que no se han activado aparecen en la pestaña **No activado**.

## <a name="features-that-must-be-turned-on"></a>Características que deben activarse

A veces se lanza una característica crítica que se activará automáticamente cuando se actualice. Estas características se activan automáticamente en la fecha especificada en el campo **Fecha de habilitación**. Para estas características, aparece un mensaje bajo el vínculo **Más información** en el panel de detalles. Este mensaje confirma que la característica se ha activado o indica la fecha futura en la que está programada que se activará. Aparecerá cada vez que seleccione la característica en la lista de la función.

## <a name="enable-all-features"></a>Habilitar todas las características

De forma predeterminada todas las características que se añaden a su entorno se desactivan. Puede habilitar todas las funciones seleccionando el botón **Habilitar todo**. 

Cuando selecciona **Habilitar todo**, aparece una opción para proporcionar la siguiente información:
- Una lista de todas las características que requieren confirmación antes de que puedan habilitarse. Si desea habilitar las características de la lista, seleccione **Sí** para el botón **Habilitar las características que requieren confirmación**.
- Se mostrará una lista de todas las características que no se pueden habilitar. Estas características no se habilitarán.

Todas las funciones que se pueden habilitar se habilitarán. Si una característica ya está programada para ser habilitada en el futuro, la programación no cambiará. 

## <a name="turn-on-all-features-automatically"></a>Activar todas las funciones automáticamente

De forma predeterminada todas las características que se añaden a su entorno se desactivan a menos que sean características obligatorias. Sin embargo, si se desea activar automáticamente todas las nuevas características, puede usar la lista desplegable bajo al título del espacio de trabajo para cambiar qué ocurre cuando se agregan las nuevas características.

- Seleccione **Habilitar nuevas características automáticamente** para activar automáticamente todas las nuevas características cuando se añaden al entorno.
- Seleccione **No habilitar nuevas características automáticamente** para que todas las nuevas características estén desactivadas de forma predeterminada cuando se añadan al entorno.


Si habilita todas las características automáticamente, se habilitan todas las funciones que se habilitarían al hacer clic en el botón **Habilitar todo**. No se habilitarán las características que requieren confirmación o las características que no se pueden habilitar hasta que se tomen medidas.

## <a name="check-for-updates"></a>Buscar actualizaciones

Las características se agregan al entorno después de cada actualización. Sin embargo, puede comprobar manualmente la existencia de actualizaciones haciendo clic en el botón **Buscar actualizaciones**. Cualquier función que fuera agregada al sistema tras la actualización se agregará a la lista de características. Por ejemplo, si se habilita una característica por tramos después de una versión, puede comprobar la existencia de actualizaciones y la función se agregará a la lista.

## <a name="assigning-roles"></a>Asignar roles

El espacio de trabajo **Administración de características** lo pueden abrir administraciones del sistema, y también usuarios que están asignados a roles de Administrador de características o Visores de características. Estos dos roles fueron creados para dar soporte a la experiencia de administración de características. Los usuarios del rol de Administrador de características pueden activar o desactivar cualquier característica. También pueden actualizar el campo **Comentarios** para la característica. Los usuarios en el rol de Visor de características solo pueden ver el espacio de trabajo **Administración de características** . No pueden activar o desactivar las características.

El rol de Administrador de características y el de Visor de características no anulan la seguridad existente que tiene un usuario. Simplemente controlan si el usuario puede activar y desactivar características. No proporciona acceso a las características en sí.

## <a name="features-that-use-configuration-keys"></a>Características que usan claves de configuración

Si una característica usa una clave de configuración, pero la clave de configuración no está activada, el espacio de trabajo **Administración de características** no muestra la función en la lista de características disponibles. Tras activar o desactivar la clave de configuración, debe actualizar la característica mediante el elemento de menú **Buscar actualización**. La característica aparece entonces en la lista de características.

Si desactiva la clave de configuración, la característica no se elimina de la lista de características.

## <a name="data-entities"></a>Entidades de datos

Una entidad de datos que se llama **Administración de las características** le permite exportar la configuración de la gestión de la característica desde un entorno y después importarla en otro entorno. Esta entidad solo actualiza características existentes. La lógica de negocios en la entidad también ayuda a garantizar que las mismas reglas que se usan en el espacio de trabajo **Administración de características** se aplicarán cuando se realiza la importación. Por ejemplo, no puede invalidar un valor obligatorio de la característica quitando la fecha durante la importación.

Los ejemplos siguientes describen lo que ocurre cuando utilice la entidad **Administración de características** para importar datos.

- Si cambia el valor del campo **Habilitado** a **Sí** la característica está activa y el campo **Fecha de habilitación** se establece en la fecha actual.
- Si cambia el valor del campo **Habilitado** a **No** o deja el campo **Fecha de habilitación** en blanco, la característica está desactivada y el campo **Fecha de habilitación** queda vacío. No puede desactivar una característica obligatoria o una función que no se puede desactivar después de que se haya activado.
- Si cambia el valor del campo **EnableDate** a una fecha futura, la característica se programa para esa fecha.
- Si cambia el valor del campo **Habilitado** a **Sí** y cambia el valor del campo **EnableDate** a una fecha futura, la característica se programa para esa fecha. 
- Si cambia el valor del campo **Habilitado** a **No** pero también cambia el valor del campo **EnableDate** a una fecha futura, la característica se programa para esa fecha.
- Si una característica está activada y se agrega un campo **EnableDate** que se establece en una fecha futura, la característica continuará activada. Para reprogramar la característica, debe cambiar el campo **Habilitado** a **No**.

## <a name="feature-management-and-flighting"></a>Administración de características y distribución de paquetes piloto

La Administración de características le permite controlar las características que se añaden en cada versión. La distribución de paquetes piloto permite a los Microsoft Teams presentar características a un número limitado de clientes para poder ser probadas y validarlas las características sin afectar a todos los clientes. La Administración de características no controla la distribución de paquetes piloto de cualquier característica.

## <a name="new-features-are-optional-for-12-months"></a>Las nuevas funciones son opcionales durante 12 meses

Cuando se instala una nueva característica no crítica, será opcional por un período de 12 meses. Esto le permite a usted y a su organización tiempo para planificar con anticipación cuándo utilizar una función y hacer que se pruebe en sus operaciones diarias. Para obtener más información, consulte [Preguntas frecuentes sobre actualizaciones del servicio de una versión](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/one-version#what-about-new-features).

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Usar la Administración de características para activar las características de ISV o las personalizadas

La administración de características no está actualmente disponible para las características de los fabricantes de software independientes (ISVs) y las características personalizadas. Sin embargo, Microsoft está añadiendo más funcionalidad para ampliar la administración de características. Después de que las mejoras hayan finalizado, Microsoft configurará la administración de características para todas las características y proporcionará instrucciones para actualizar sus características para usarla.

## <a name="frequently-asked-questions-faq"></a>Preguntas frecuentes

### <a name="when-are-features-added-removed-or-changed"></a>¿Cuándo se agregan, quitan o cambian características? 
Las características se agregan, eliminan y cambian mediante cambios en el código. Los entornos deben actualizarse para recibir esos cambios.

### <a name="does-a-feature-become-mandatory-automatically"></a>¿Una característica se vuelve obligatoria automáticamente? 
No, una función que se vuelve obligatoria no es una acción automática. Los equipos de producto necesitan hacer un cambio de código.

### <a name="when-do-features-become-mandatory"></a>¿Cuándo se vuelven obligatorias las características? 
La política es que todas las nuevas características se habiliten por un período de 12 meses y que no requieran ninguna gestión de cambios hasta que habilite la función. Los equipos de productos pueden elegir si hacer que una característica sea obligatoria una vez que finaliza ese período. 

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>¿Por qué no hay una "fecha habilitada obligatoria" específica? 
El tiempo de actualización es variable, el tiempo de actualización del entorno es variable y los clientes pueden optar por omitir algunas actualizaciones. Como resultado, las fechas específicas son difíciles de determinar. 

### <a name="wheres-the-documentation-for-features-that-are-being-made-mandatory"></a>¿Dónde está la documentación de las características que se hacen obligatorias? 
Esta documentación proviene de los equipos de aplicación. A menudo, estos se mencionarán en [Funciones eliminadas o en desuso](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>¿Hay una notificación en el producto o una señal de que una característica será obligatoriamente habilitada? 
Hoy en día no existe un mecanismo de notificación relacionado con hacer que una característica sea obligatoria.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>¿Se habilitan las características sin que el cliente lo sepa? 
Sí, si las características no tienen un impacto funcional, entonces pueden habilitarse de manera predeterminada.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>¿Qué es el paquete piloto de características y cómo se relaciona con la gestión de características? 
Los paquetes piloto de características son interruptores de encendido y apagado en tiempo real que controla Microsoft. Están fuera del control del cliente que proporciona Feature Management. 
- Las características de versión preliminar privada no aparecerán en Feature Management hasta que se activen en el paquete piloto. En el entorno de producción, el cliente debe aceptar ser parte de un programa especial para que eso se produzca.
- Las características de versión preliminar pública (generalmente disponibles) se enumerarán en Feature Management a menos que estén desactivadas. Desactivar una característica del paquete piloto se considera una opción de último recurso para los equipos de productos si se encuentra un problema crítico y, por lo general, sería una operación por cliente.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>¿Se deshabilitan características del paquete piloto sin que el cliente lo sepa? 
Sí, si una característica está afectando al funcionamiento de un entorno que no tiene un impacto funcional, entonces se pueden habilitar de forma predeterminada.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>¿Cómo se puede verificar la habilitación de funciones en el código?
Utilice el método **isFeatureEnabled** en la clase **FeatureStateProvider**, pasándole una instancia de la clase de entidad. Ejemplo: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>¿Cómo se puede verificar la habilitación de funciones en los metadatos?
La propiedad **FeatureClass** se puede utilizar para indicar que algunos metadatos están asociados con una característica. Se debe usar el nombre de clase utilizado para la característica, como **BatchContentionPreventionFeature**. Estos metadatos son visibles solo en esa función. La propiedad **Clase característica** está disponible en menús, elementos de menú, valores de enumeración y campos de tabla / vista.

### <a name="what-is-a-feature-class"></a>¿Qué es una clase de entidad?
Las funciones en la Gestión de funciones se definen como *clases de entidades*. Una clase de entidad **implementa IFeatureMetadata** y utiliza el atributo de clase de entidad para identificarse en el espacio de trabajo de Gestión de entidades. Hay numerosos ejemplos de clases de entidad disponibles que se pueden verificar para su habilitación en el código usando la API **FeatureStateProvider** y en metadatos usando la propiedad **FeatureClass**. Ejemplo: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>¿Qué es el IFeatureLifecycle implementado por algunas clases de entidad?
IFeatureLifecycle es un mecanismo interno de Microsoft para indicar la etapa del ciclo de vida de la característica. Las características pueden ser:
- PrivatePreview: necesita un vuelo para ser visible.
- PublicPreview: se muestra de forma predeterminada, pero con una advertencia de que la función está en vista previa.
- Lanzada: completamente publicada.

