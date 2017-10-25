---
title: "Visión general del flujo de trabajo"
description: Este tema describe el sistema de flujo de trabajo en Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6622f0e5ed6c38bb8131d13aa02061968862678b
ms.contentlocale: es-es
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-overview"></a><span data-ttu-id="d35a8-103">Visión general del flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-103">Workflow overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d35a8-104">Este tema describe el sistema de flujo de trabajo en Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d35a8-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-workflow"></a><span data-ttu-id="d35a8-105">¿Qué significa flujo de trabajo?</span><span class="sxs-lookup"><span data-stu-id="d35a8-105">What is workflow?</span></span>
-----------------

<span data-ttu-id="d35a8-106">El término *flujo de trabajo* se puede definir de dos maneras: como sistema y como proceso empresarial.</span><span class="sxs-lookup"><span data-stu-id="d35a8-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>
### <a name="workflow-is-a-system"></a><span data-ttu-id="d35a8-107">Flujo de trabajo es un sistema</span><span class="sxs-lookup"><span data-stu-id="d35a8-107">Workflow is a system</span></span>

<span data-ttu-id="d35a8-108">El flujo de trabajo es un sistema que se instala junto con Dynamics 365 for Finance and Operations y se ejecuta en Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="d35a8-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="d35a8-109">El sistema de flujo de trabajo proporciona funciones que se pueden usar para crear flujos de trabajo individuales, o procesos empresariales.</span><span class="sxs-lookup"><span data-stu-id="d35a8-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="d35a8-110">Flujo de trabajo es un proceso empresarial</span><span class="sxs-lookup"><span data-stu-id="d35a8-110">Workflow is a business process</span></span>

<span data-ttu-id="d35a8-111">Un flujo de trabajo representa un proceso empresarial.</span><span class="sxs-lookup"><span data-stu-id="d35a8-111">A workflow represents a business process.</span></span> <span data-ttu-id="d35a8-112">El flujo de trabajo define el flujo o movimiento de un documento en el sistema al mostrar quién debe completar una tarea, tomar una decisión o aprobar un documento.</span><span class="sxs-lookup"><span data-stu-id="d35a8-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="d35a8-113">Por ejemplo, en la siguiente ilustración se muestra un flujo de trabajo de informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="d35a8-113">For example, the following illustration shows a workflow for expense reports.</span></span> 

![Flujo de trabajo con elementos que están asignados a usuarios](./media/workflow_user.gif) 

<span data-ttu-id="d35a8-115">Para comprender mejor este flujo de trabajo, supongamos que Sam envía un informe de gastos por un total de 7.000 USD.</span><span class="sxs-lookup"><span data-stu-id="d35a8-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="d35a8-116">En esta situación, Ivan debe revisar los recibos que Sam le envía.</span><span class="sxs-lookup"><span data-stu-id="d35a8-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="d35a8-117">A continuación, Frank y Sue deben aprobar el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="d35a8-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="d35a8-118">Ahora supongamos que Sam envía un informe de gastos por un total de 11.000 USD.</span><span class="sxs-lookup"><span data-stu-id="d35a8-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="d35a8-119">En esa situación, Ivan debe revisar los recibos y Frank, Sue y Ann deben aprobar el informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="d35a8-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="d35a8-120">Ventajas del uso del sistema de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="d35a8-121">El uso del sistema de flujo de trabajo en una organización ofrece varias ventajas:</span><span class="sxs-lookup"><span data-stu-id="d35a8-121">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="d35a8-122">**Procesos coherentes**: puede definir cómo determinados documentos —por ejemplo, solicitudes de compra e informes de gastos— se procesan.</span><span class="sxs-lookup"><span data-stu-id="d35a8-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="d35a8-123">Al usar el sistema de flujo de trabajo, puede asegurarse de que los documentos se procesarán y aprobarán de manera coherente y eficiente.</span><span class="sxs-lookup"><span data-stu-id="d35a8-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="d35a8-124">**Visibilidad de procesos**: puede realizar el seguimiento del estado, el historial y las medidas de rendimiento de las instancias de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d35a8-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="d35a8-125">De este modo, puede determinar si se deben realizar cambios en el flujo de trabajo para mejorar la eficiencia.</span><span class="sxs-lookup"><span data-stu-id="d35a8-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="d35a8-126">**Lista de trabajo centralizada**: los usuarios pueden ver una lista de trabajo centralizada con las tareas y aprobaciones de flujo de trabajo que tienen asignadas.</span><span class="sxs-lookup"><span data-stu-id="d35a8-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="d35a8-127">Contenido del flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-127">Workflow content</span></span>

+ [<span data-ttu-id="d35a8-128">Arquitectura del flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="d35a8-129">Elementos del flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="d35a8-130">Acciones de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="d35a8-131">Creación de un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="d35a8-132">Configuración de propiedades del flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="d35a8-133">Configuración de una tarea manual en un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="d35a8-134">Configuración de una tarea automatizada en un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="d35a8-135">Configuración de un proceso de aprobación en un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="d35a8-136">Configuración de un paso de aprobación en un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="d35a8-137">Configuración de una decisión manual en un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="d35a8-138">Configuración de una decisión condicional en un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="d35a8-139">Configuración de una actividad paralela en un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="d35a8-140">Configuración de rama paralela en un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d35a8-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="d35a8-141">Configuración de un flujo de trabajo de elementos</span><span class="sxs-lookup"><span data-stu-id="d35a8-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
