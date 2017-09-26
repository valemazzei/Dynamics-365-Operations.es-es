--- 
title: Configurar permisos para pedir productos en nombre de otro usuario
description: "Este procedimiento muestra cómo conceder a los trabajadores permiso para preparar solicitudes de la compra en nombre de otros trabajadores."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8f12f9eb949034f9bef91d93f31a0f3373e39e98
ms.contentlocale: es-es
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Configurar permisos para pedir productos en nombre de otro usuario

[!include[task guide banner](../../includes/task-guide-banner.md)]

Este procedimiento muestra cómo conceder a los trabajadores permiso para preparar solicitudes de la compra en nombre de otros trabajadores. Es decir, un “preparador” de una solicitud de compra puede crear una solicitud para otro “solicitante.” El procedimiento también muestra cómo conceder permisos a un trabajador para que pida los artículos y los servicios en diferentes entidades jurídicas o unidades operativas. Normalmente, estas tareas las realiza el administrador de compras. Puede utilizar este procedimiento en los datos para la empresa de demostración USMF o en sus propios datos.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Conceder permiso para especificar solicitudes de compra en nombre de otro trabajador
1. Vaya a Adquisición y abastecimiento > Configuración > Directivas > Permisos de solicitud de compra.
    * Asegúrese de que el campo Vista actual está establecido en Por preparador.  La lista del panel izquierdo muestra a la gente a quien se le puede conceder permiso para preparar solicitudes en nombre de otras personas.  
2. Seleccione la persona a la que le concederá el permiso (el preparador).
3. Haga clic en Agregar.
4. Encuentre y seleccione la persona para agregarla como solicitante.
    * El solicitante es la persona en nombre de la cual el preparador puede crear solicitudes.  
    * En el campo Autorización, seleccione Específico si el preparador debe poder crear solicitudes de compra en nombre del trabajador seleccionado. Seleccione Notificación si el preparador debe poder crear solicitudes de compra en nombre de todos los trabajadores que informen a ese trabajador.  
5. En el campo Vigente, especifique una fecha.
6. En el campo Caducidad, especifique una fecha.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Ver preparadores que tienen permiso para crear solicitudes de compra para un trabajador seleccionado
1. En el campo Vista actual, seleccione “Por solicitante”.
    * Esta lista muestra una lista de preparadores a los que se le han concedido permiso para crear solicitudes de compra en nombre de un trabajador seleccionado.  
2. Utilice el Filtro rápido para encontrar el trabajador que acaba de agregar como solicitante.
3. Seleccione el solicitante.
    * La lista Preparador muestra las personas con permiso para pedir artículos en nombre del solicitante seleccionado en el panel izquierdo.   Puede agregar preparadores adicionales aquí.   Esta vista también le permite conceder el permiso de solicitante para crear solicitudes en entidades jurídicas y unidades operativas que no son la entidad jurídica principal o unidad operativa de esa persona.  

