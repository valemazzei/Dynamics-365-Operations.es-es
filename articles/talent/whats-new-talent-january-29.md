---
title: Novedades y cambios en Dynamics 365 for Talent (31 de enero de 2019)
description: Este tema describe las características que son nuevas o que se han cambiado en Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 1/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c9449e2bdec8c17cc2cf659ed68ac1d713a26ad
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2019
ms.locfileid: "374743"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Novedades y cambios en Dynamics 365 for Talent (31 de enero de 2019)

[!include [banner](includes/banner.md)]

Este tema describe las características que son nuevas o que se han cambiado en Dynamics 365 for Talent.

**Compilación 8.1.2128**

## <a name="core-hr-changes"></a>Cambios en Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>El tiempo de licencia tomado en la tarjeta de las personas de la licencia no tiene en cuenta las fechas del plan de la licencia
Para aquellas personas que tienen planes de licencia que no se ejecuten en un año natural, ahora la una tarjeta **Procedente** muestra el tiempo de licencia que se ha tomado en el año de licencia definido en el plan. Por ejemplo, si el año de la licencia de una organización está incluido entre el 1 de junio y el 30 de mayo y un empleado ha tomado 3 días libres en diciembre, la tarjeta **Procedente** mostrará 3 días el 15 de enero. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Los importes de acumulación no coinciden con la base de fecha del nivel
Se han agregado nuevas opciones para licencias y ausencias (parámetros**Recursos humanos**) para habilitar a los clientes para que determinen cuándo los meses de servicio de los empleados entran en vigor. Para algunas organizaciones, la fecha es el final del mes, pero para otros puede ser el inicio del mes siguiente. Por ejemplo, una organización puede conceder tiempo libre el 31 de diciembre, mientras que otra puede concederlo el 1 de enero. Esta opción le permitirá decidir cuando debe realizarse la concesión de tiempo. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Las acciones de contratación del trabajador se bloquean en el estado “flujo de trabajo completo”
Se han realizado cambios para corregir un problema en el que una pequeña cantidad de flujos de trabajo terminaban con un estado “flujo de trabajo completo”. Los nuevos flujos de trabajo ahora pasan al estado “completado” cuando finaliza del flujo de trabajo. Cualquier flujo de trabajo que tenga un estado completado del flujo de trabajo se pasará al estado de error para permitir su actualización o eliminación si procede. 