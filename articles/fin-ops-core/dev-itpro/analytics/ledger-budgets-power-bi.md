---
title: Contenido Real frente a presupuesto de Power BI
description: Este tema describe el contenido en Power BI de Real frente a presupuesto Explica cómo tener acceso a los informes que se incluyen en el contenido, y proporciona información acerca del modelo de datos y las entidades que se utilizaron para generar el contenido.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184402"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="5c1f5-104">Contenido Real frente a presupuesto de Power BI</span><span class="sxs-lookup"><span data-stu-id="5c1f5-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c1f5-105">Este tema describe el contenido en Power BI de **Real frente a presupuesto**.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="5c1f5-106">Explica cómo obtener acceso a los informes Power BI y proporciona información acerca del modelo de datos y las entidades que se utilizan para generar el contenido.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="5c1f5-107">Información general</span><span class="sxs-lookup"><span data-stu-id="5c1f5-107">Overview</span></span>

<span data-ttu-id="5c1f5-108">El contenido en Power BI de **Real rente a presupuesto** se creó para aquellas personas que son responsables de supervisar los valores reales frente al presupuesto en su organización.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="5c1f5-109">El contenido en Power BI de **Real frente a presupuesto** proporciona visibilidad en las desviaciones de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="5c1f5-110">Puede analizar el presupuesto para el año actual por categoría de cuenta, código de presupuesto, cuenta principal, descripciones de la cuenta principal o período fiscal para obtener una mejor comprensión de los motivos que producen las desviaciones.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="5c1f5-111">Acceso al contenido de Power BI</span><span class="sxs-lookup"><span data-stu-id="5c1f5-111">Accessing the Power BI content</span></span>
<span data-ttu-id="5c1f5-112">Los informes del contenido de Power BI **Real frente a presupuesto** se muestran en los espacios de trabajo **Presupuestos y previsiones de libro mayor** y **CFO**.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="5c1f5-113">Informes que se incluyen en el contenido de Power BI</span><span class="sxs-lookup"><span data-stu-id="5c1f5-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="5c1f5-114">La siguiente tabla ofrece información sobre las métricas que se encuentran en cada página de informe en el contenido de Power BI de **Real frente a presupuesto**.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="5c1f5-115">Informe</span><span class="sxs-lookup"><span data-stu-id="5c1f5-115">Report</span></span>                      | <span data-ttu-id="5c1f5-116">Métricas</span><span class="sxs-lookup"><span data-stu-id="5c1f5-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c1f5-117">Gastos reales frente a gastos de presupuesto</span><span class="sxs-lookup"><span data-stu-id="5c1f5-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="5c1f5-118">Total de gastos este año</span><span class="sxs-lookup"><span data-stu-id="5c1f5-118">Total expenses this year</span></span></li><li><span data-ttu-id="5c1f5-119">Total de gastos de presupuesto este año</span><span class="sxs-lookup"><span data-stu-id="5c1f5-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="5c1f5-120">Ingresos reales frente a ingresos de presupuesto</span><span class="sxs-lookup"><span data-stu-id="5c1f5-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="5c1f5-121">Ingresos totales este año</span><span class="sxs-lookup"><span data-stu-id="5c1f5-121">Total revenue this year</span></span></li><li><span data-ttu-id="5c1f5-122">Total de ingresos de presupuesto este año</span><span class="sxs-lookup"><span data-stu-id="5c1f5-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="5c1f5-123">Gastos</span><span class="sxs-lookup"><span data-stu-id="5c1f5-123">Expense</span></span>                     | <ul><li><span data-ttu-id="5c1f5-124">Total de gastos este año</span><span class="sxs-lookup"><span data-stu-id="5c1f5-124">Total expenses this year</span></span></li><li><span data-ttu-id="5c1f5-125">Objetivo de gastos en función de presupuesto</span><span class="sxs-lookup"><span data-stu-id="5c1f5-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="5c1f5-126">Ingresos</span><span class="sxs-lookup"><span data-stu-id="5c1f5-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="5c1f5-127">Ingresos totales este año</span><span class="sxs-lookup"><span data-stu-id="5c1f5-127">Total revenue this year</span></span></li><li><span data-ttu-id="5c1f5-128">Objetivo de ingresos en función de presupuesto</span><span class="sxs-lookup"><span data-stu-id="5c1f5-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="5c1f5-129">Ingresos netos</span><span class="sxs-lookup"><span data-stu-id="5c1f5-129">Net income</span></span>                  | <ul><li><span data-ttu-id="5c1f5-130">Ingresos netos este año</span><span class="sxs-lookup"><span data-stu-id="5c1f5-130">Net income this year</span></span></li><li><span data-ttu-id="5c1f5-131">Objetivo de ingresos netos en función de presupuesto</span><span class="sxs-lookup"><span data-stu-id="5c1f5-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="5c1f5-132">Comprensión del modelo de datos y de las entidades</span><span class="sxs-lookup"><span data-stu-id="5c1f5-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="5c1f5-133">Entidad</span><span class="sxs-lookup"><span data-stu-id="5c1f5-133">Entity</span></span>                    | <span data-ttu-id="5c1f5-134">Contenido</span><span class="sxs-lookup"><span data-stu-id="5c1f5-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5c1f5-135">Actividades de contabilidad general</span><span class="sxs-lookup"><span data-stu-id="5c1f5-135">General Ledger Activities</span></span> | <span data-ttu-id="5c1f5-136">Importes de transacción de contabilidad general</span><span class="sxs-lookup"><span data-stu-id="5c1f5-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="5c1f5-137">Actividades de presupuesto</span><span class="sxs-lookup"><span data-stu-id="5c1f5-137">Budget Activities</span></span>         | <span data-ttu-id="5c1f5-138">Importes de transacción para el registro presupuestario</span><span class="sxs-lookup"><span data-stu-id="5c1f5-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="5c1f5-139">Cuentas principales</span><span class="sxs-lookup"><span data-stu-id="5c1f5-139">Main Accounts</span></span>             | <span data-ttu-id="5c1f5-140">Cuentas principales para filtrar informes</span><span class="sxs-lookup"><span data-stu-id="5c1f5-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="5c1f5-141">Calendarios fiscales</span><span class="sxs-lookup"><span data-stu-id="5c1f5-141">Fiscal Calendars</span></span>          | <span data-ttu-id="5c1f5-142">Calendarios fiscales para filtrar informes</span><span class="sxs-lookup"><span data-stu-id="5c1f5-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="5c1f5-143">Libros mayores</span><span class="sxs-lookup"><span data-stu-id="5c1f5-143">Ledgers</span></span>                   | <span data-ttu-id="5c1f5-144">Libros mayores que se pueden usar para filtrar el informe en la contabilidad actual</span><span class="sxs-lookup"><span data-stu-id="5c1f5-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="5c1f5-145">Códigos de presupuesto</span><span class="sxs-lookup"><span data-stu-id="5c1f5-145">Budget Codes</span></span>              | <span data-ttu-id="5c1f5-146">Códigos presupuestarios para filtrar informes</span><span class="sxs-lookup"><span data-stu-id="5c1f5-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="5c1f5-147">Entidades jurídicas</span><span class="sxs-lookup"><span data-stu-id="5c1f5-147">Legal Entities</span></span>            | <span data-ttu-id="5c1f5-148">Entidades jurídicas que se pueden usar para filtrar el informe para la entidad jurídica actual</span><span class="sxs-lookup"><span data-stu-id="5c1f5-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |