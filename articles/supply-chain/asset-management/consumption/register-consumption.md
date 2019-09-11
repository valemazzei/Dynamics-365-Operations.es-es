---
title: Registrar consumo
description: En este tema se explica cómo registrar el consumo en Administración de activos.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f785b0935b952d6de68fd120a3639077ad124bd
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913107"
---
# <a name="register-consumption"></a><span data-ttu-id="4ec5c-103">Registrar consumo</span><span class="sxs-lookup"><span data-stu-id="4ec5c-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4ec5c-104">Cuando se haya completado un trabajo de mantenimiento en una orden de trabajo, el paso siguiente es hacer los registros de consumo y registrar los diarios.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="4ec5c-105">Puede hacer registros en los siguientes tipos de consumo: horas, artículos y gastos.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="4ec5c-106">Los distintos tipos de consumo se registran en la página **Diarios de órdenes de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="4ec5c-107">La configuración del diario en **Administración de activos** se utiliza para crear y registrar diarios independientes para horas, artículos y gastos en el módulo **Gestión y contabilidad de proyectos**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="4ec5c-108">Es posible que pueda agregar o eliminar líneas de previsión en una orden de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="4ec5c-109">La configuración del estado de ciclo de vida de una orden de trabajo, el tipo de proyecto relacionado y las reglas de etapa relacionadas con el tipo de proyecto determinan si puede agregar o editar líneas del diario.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="4ec5c-110">Obtenga más información sobre los estados de ciclo de vida de una orden de trabajo y las etapas de proyecto relacionadas en [Integración en la contabilidad y gestión de proyectos](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="4ec5c-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="4ec5c-111">Es posible configurar un registro automático de diarios en el estado de ciclo de vida de una orden de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="4ec5c-112">Consulte [Estados de ciclo de vida de orden de trabajo](../setup-for-work-orders/work-order-lifecycle-states.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="4ec5c-113">Haga clic en **Administración de activos** > **Común** > **Órdenes de trabajo** > **Todas las órdenes de trabajo** u **Órdenes de trabajo activas**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4ec5c-114">Seleccione la orden de trabajo y haga clic en **Diarios**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="4ec5c-115">Haga clic en **Copiar desde previsión** para transferir cualquier línea de previsión que pueda estar conectada con la orden de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="4ec5c-116">Puede seleccionar los tipos de consumo que desea transferir.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="4ec5c-117">Si es necesario, puede agregar más líneas de consumo en la ficha desplegable pertinente haciendo clic en **Agregar línea** y rellenando los datos de la línea.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="4ec5c-118">Haga clic en **Validar diarios** para validar las líneas de diario antes de registrarlo.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="4ec5c-119">Haga clic en **Registrar diarios** para registrar las líneas del diario.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="4ec5c-120">Después de haber registrado los diarios de consumo, puede actualizar el estado de ciclo de vida de la orden de trabajo, por ejemplo a "Terminado", para indicar que la orden de trabajo se ha completado.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="4ec5c-121">En el campo **Mostrar** situado en la parte superior de la página **Diarios de órdenes de trabajo**, seleccione las líneas del diario que desea ver: Todas, No registradas o Registradas.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="4ec5c-122">Los diarios registrados tienen una marca de verificación en la casilla **Registrado**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="4ec5c-123">Cuando se crean líneas de artículos en el diario de orden de trabajo, las dimensiones del producto y las dimensiones de seguimiento relacionadas con el artículo se transfieren automáticamente a la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="4ec5c-124">La siguiente captura de pantalla muestra un ejemplo de los registros de horas y artículos en una orden de trabajo en **Diarios de órdenes de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Figura 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="4ec5c-126">Horas divididas en órdenes de trabajo con varios trabajos de una orden trabajo</span><span class="sxs-lookup"><span data-stu-id="4ec5c-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="4ec5c-127">Si una orden de trabajo contiene varias tareas, puede registrar las horas de trabajo mediante la función **Horas divididas**, lo que significa que una línea de registro de horas se puede distribuir de forma equitativa en cada tarea de la orden de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="4ec5c-128">Haga clic en **Administración de activos** > **Común** > **Órdenes de trabajo** > **Todas las órdenes de trabajo** u **Órdenes de trabajo activas**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4ec5c-129">Seleccione la orden de trabajo y haga clic en **Diarios**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="4ec5c-130">Seleccione la línea de registro de horas que desea dividir y haga clic en **Horas divididas**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="4ec5c-131">En el diálogo **Horas divididas en trabajos de mantenimiento de órdenes de trabajo**, el nombre del trabajador que está registrado se muestra automáticamente en el campo **Trabajador**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="4ec5c-132">Si es necesario, puede seleccionar otro trabajador.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="4ec5c-133">Seleccione una categoría para el registro de horas en el campo **Categoría**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="4ec5c-134">Inserte el número de horas de trabajo que se van a dividir en el campo **Horas**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![Figura 2](media/02-consumption.png)

7. <span data-ttu-id="4ec5c-136">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-136">Click **OK**.</span></span>

<span data-ttu-id="4ec5c-137">*Ejemplo:* en la siguiente captura de pantalla se muestran las líneas de diario para una orden de trabajo que contiene tres tareas.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="4ec5c-138">La primera línea, que contiene tres horas de trabajo, se ha dividido, y una hora de trabajo se registra en cada tarea de la orden de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="4ec5c-139">Una vez creadas las tres líneas de registro de horas, decida qué hacer con la línea de registro de horas original (la primera línea del ejemplo).</span><span class="sxs-lookup"><span data-stu-id="4ec5c-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="4ec5c-140">Puede conservarla tal cual o eliminarla.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-140">You can keep it as is or delete it.</span></span> 

![Figura 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="4ec5c-142">Dimensiones financieras en los registros de consumo</span><span class="sxs-lookup"><span data-stu-id="4ec5c-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="4ec5c-143">Al hacer registros de consumo, las dimensiones financieras relacionadas con los distintos tipos de registro se agregan a los registros en una secuencia específica.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="4ec5c-144">*Registros de horas y gastos:* en primer lugar, se agregan las dimensiones financieras del encabezado del diario, si existen.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="4ec5c-145">A continuación, se agregan las dimensiones financieras del proyecto de orden de trabajo relacionado.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="4ec5c-146">Finalmente, se agregan las dimensiones financieras del recurso (trabajador).</span><span class="sxs-lookup"><span data-stu-id="4ec5c-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="4ec5c-147">*Registros de artículos:* en primer lugar, se agregan las dimensiones financieras del encabezado del diario, si existen.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="4ec5c-148">Después, se agregan las dimensiones financieras del proyecto de orden de trabajo relacionado.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="4ec5c-149">A continuación, se agregan las dimensiones financieras del sitio.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="4ec5c-150">Finalmente, se agregan las dimensiones financieras del artículo.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="4ec5c-151">Para los tres tipos de registro, se valida la combinación de dimensiones financieras y se dejan en blanco las combinaciones no válidas.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="4ec5c-152">Se trata de una configuración estándar en Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ec5c-152">This is standard setup in Dynamics 365 for Finance and Operations.</span></span>
