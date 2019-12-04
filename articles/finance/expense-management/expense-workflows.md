---
title: Configurar flujos de trabajo de los gastos
description: Puede configurar un proceso de flujo de trabajo que se usa para revisar y aprobar documentos de gastos y viajes.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179775"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="08f58-103">Configurar flujos de trabajo de los gastos</span><span class="sxs-lookup"><span data-stu-id="08f58-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08f58-104"> Puede configurar un proceso de flujo de trabajo que se usa para revisar y aprobar documentos de gastos y viajes.</span><span class="sxs-lookup"><span data-stu-id="08f58-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="08f58-105">Los documentos para los que pueden definirse los flujos de trabajo incluyen informes de gastos, pedidos de viaje y solicitudes de anticipo.</span><span class="sxs-lookup"><span data-stu-id="08f58-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="08f58-106">Un flujo de trabajo representa un proceso empresarial.</span><span class="sxs-lookup"><span data-stu-id="08f58-106">A workflow represents a business process.</span></span> <span data-ttu-id="08f58-107">El flujo de trabajo define cómo se gestiona un documento en el sistema e indica quién debe completar una tarea o aprobar un documento.</span><span class="sxs-lookup"><span data-stu-id="08f58-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="08f58-108">El uso del sistema de flujo de trabajo en su organización le ofrece varias ventajas:</span><span class="sxs-lookup"><span data-stu-id="08f58-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="08f58-109">**Procesos coherentes**: puede definir el proceso de aprobación para documentos específicos como, por ejemplo, solicitudes de compra e informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="08f58-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="08f58-110">El sistema de flujo de trabajo le ayuda a garantizar que los documentos se procesan y se aprueban de manera coherente y eficaz.</span><span class="sxs-lookup"><span data-stu-id="08f58-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="08f58-111">Visibilidad de procesos: puede realizar el seguimiento del estado, el historial y las medidas de rendimiento de una instancia de flujo de trabajo determinada.</span><span class="sxs-lookup"><span data-stu-id="08f58-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="08f58-112">De este modo puede determinar si los cambios deben realizarse en el flujo de trabajo para mejorar la eficacia.</span><span class="sxs-lookup"><span data-stu-id="08f58-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="08f58-113">Lista de trabajo centralizada: los usuarios pueden ver una lista de trabajo centralizada para ver las tareas y aprobaciones de flujo de trabajo que tienen asignadas.</span><span class="sxs-lookup"><span data-stu-id="08f58-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="08f58-114">**Tipos de flujo de trabajo que puede crear**</span><span class="sxs-lookup"><span data-stu-id="08f58-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="08f58-115">En la siguiente tabla se describen los tipos de flujo de trabajo que se pueden crear en **Gastos**.</span><span class="sxs-lookup"><span data-stu-id="08f58-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="08f58-116"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="08f58-117"><strong>Use este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="08f58-118"><strong>Informe de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="08f58-119">Cree flujos de trabajo de aprobación para los informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="08f58-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="08f58-120"><strong>Registro automático de informe de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="08f58-121">Cree flujos de trabajo del registro automático para los informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="08f58-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="08f58-122"><strong>Elemento de línea de gastos</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="08f58-123">Cree flujos de trabajo de aprobación para los artículos de línea en los informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="08f58-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="08f58-124"><strong>Registro automático de artículo de línea de gasto</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="08f58-125">Cree flujos de trabajo de registro automático para los artículos de línea en los informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="08f58-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="08f58-126"><strong>Pedido de viaje</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="08f58-127">Cree flujos de trabajo de aprobación para solicitudes de viaje.</span><span class="sxs-lookup"><span data-stu-id="08f58-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="08f58-128"><strong>Solicitud de anticipo</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="08f58-129">Cree flujos de aprobación para las solicitudes de anticipo.</span><span class="sxs-lookup"><span data-stu-id="08f58-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="08f58-130"><strong>Devolución de impuestos de IVA</strong></span><span class="sxs-lookup"><span data-stu-id="08f58-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="08f58-131">Cree flujos de trabajo de aprobación para la devolución del impuesto sobre el valor añadido (VAT).</span><span class="sxs-lookup"><span data-stu-id="08f58-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
