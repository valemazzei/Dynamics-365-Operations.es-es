---
title: Cancelar un trabajo de planificación maestro
description: Este tema explica cómo cancelar un trabajo activo de planificación que utilice la función planificación integrada.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6f5ce460cc2915d1d4d9b5699723a62ed7f94599
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4437102"
---
# <a name="cancel-a-master-planning-job"></a>Cancelar un trabajo de planificación maestro

[!include [banner](../includes/banner.md)]

En Microsoft Dynamics 365 Supply Chain Management, hay varias opciones para cancelar un trabajo de planificación maestro. Por ejemplo, es posible que desee cancelar un trabajo de planificación maestra si se inició por error o si se está ejecutando por más tiempo de lo esperado y desea finalizarlo. La mejor manera de cancelar un trabajo de planificación es desde la **Procesos de planificación inacabados** página. Las opciones alternativas de las páginas **Trabajos por lotes** y **Trabajos por lotes mejorados** solo deben usarse si cancelar el trabajo de planificación maestra desde la página **Procesos de planificación inacabados** no se completó en unos minutos.

## <a name="preferred-cancel-option"></a>Opción de cancelación preferida
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Cancelar el trabajo de planificación maestra desde la página **Procesos de planificación inacabados**
1. Vaya a **Planificación maestra > Consultas e informes > Planificación maestra > Procesos de planificación inacabados**.
2. Seleccione la línea con el proceso de planificación que quiera cancelar.
3. Haga clic en **Cancelar**.

## <a name="additional-cancel-options"></a>Opciones adicionales de cancelación
Estas solo deben usarse si la cancelación del trabajo de planificación maestra desde la página **Procesos de planificación inacabados** no se completó en unos minutos.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Eliminar el trabajo de planificación maestra de la página **Trabajos por lotes**
1. Vaya **Administración del sistema > Consultas > Trabajos por lotes**.
2. Seleccione la línea con el trabajo de planificación que quiera eliminar.
3. Haga clic **Eliminar**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Anular la tarea de planificación maestra desde la página **Trabajos por lotes mejorados**
1. Vaya **Administración del sistema > Consultas > Trabajos por lotes**.
2. Si la ID del trabajo no se muestra en la lista, haga clic en **Cambiar a forma mejorada**, de lo contrario, continúe con el siguiente paso.
3. Abra el trabajo por lotes. Haga clic en la **Identificación del trabajo** para el trabajo por lotes con tareas que desea finalizar.
4. En **Tareas por lotes**, seleccione las tareas para finalizar.
5. Haga clic en **Cambiar Estado**, elija **Cancelación** y haga clic en **Aceptar**.
6. En la ficha desplegable **Tareas por lotes**, haga clic en **Anular**.
