---
title: Procesar tasas de cambios
description: Procesar cambios en la tasa de prestaciones en Microsoft Dynamics 365 Human Resources cuando un plan de prestaciones nuevo o existente tiene un cambio en la configuración de las reglas de idoneidad.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010425"
---
# <a name="process-rate-changes"></a><span data-ttu-id="9408c-103">Procesar tasas de cambios</span><span class="sxs-lookup"><span data-stu-id="9408c-103">Process rate changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="9408c-104">Procesar cambios en la tasa de prestaciones en Microsoft Dynamics 365 Human Resources cuando un plan de prestaciones nuevo o existente tiene un cambio en la configuración de las reglas de idoneidad.</span><span class="sxs-lookup"><span data-stu-id="9408c-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="9408c-105">Si se crea una nueva regla de idoneidad y se asigna al plan, esto lleva al sistema a volver a ejecutar la idoneidad de los trabajadores para verificar si los trabajadores ahora son idóneos para el plan en función de las nuevas opciones de idoneidad.</span><span class="sxs-lookup"><span data-stu-id="9408c-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to re-run worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="9408c-106">En el espacio de trabajo **Administración de prestaciones**, en **Procesamiento**, seleccione **Procesamiento de actualización de tasas de cambios**.</span><span class="sxs-lookup"><span data-stu-id="9408c-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="9408c-107">En el cuadro de diálogo **Ejecutar proceso de actualización de tasas de cambios**, especifique valores para los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="9408c-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="9408c-108">Campo</span><span class="sxs-lookup"><span data-stu-id="9408c-108">Field</span></span> | <span data-ttu-id="9408c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9408c-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9408c-110">Período de inscripción</span><span class="sxs-lookup"><span data-stu-id="9408c-110">Enrollment period</span></span> | <span data-ttu-id="9408c-111">El periodo de inscripción para procesar tasas de cambios.</span><span class="sxs-lookup"><span data-stu-id="9408c-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="9408c-112">Si desea ejecutar el proceso en segundo plano, seleccione **Ejecutar en segundo plano** y realice las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="9408c-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="9408c-113">Escriba información para proceso.</span><span class="sxs-lookup"><span data-stu-id="9408c-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="9408c-114">Para configurar un trabajo periódico, seleccione **Periodicidad**, introduzca la información de periodicidad y seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9408c-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="9408c-115">Para configurar una alerta de trabajo, seleccione **Alertas**, seleccione las alertas que quiera recibir y luego seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9408c-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="9408c-116">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9408c-116">Select **OK**.</span></span> <span data-ttu-id="9408c-117">El proceso se ejecutará con los parámetros que establezca.</span><span class="sxs-lookup"><span data-stu-id="9408c-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="9408c-118">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9408c-118">Select **OK**.</span></span>