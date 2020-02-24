---
title: Crear tipos de planes
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c12eecb38bd943a9c604f878644da289783d3f74
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010474"
---
# <a name="create-plan-types"></a><span data-ttu-id="948c2-102">Crear tipos de planes</span><span class="sxs-lookup"><span data-stu-id="948c2-102">Create plan types</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="948c2-103">Un tipo de plan en Microsoft Dynamics 365 Human Resources es una agrupación de alto nivel de tipos específicos de prestaciones.</span><span class="sxs-lookup"><span data-stu-id="948c2-103">A plan type in Microsoft Dynamics 365 Human Resources is a high-level grouping of specific types of benefits.</span></span> <span data-ttu-id="948c2-104">Cada tipo de plan tiene un código de tipo de plan que determina reglas para el tipo de plan.</span><span class="sxs-lookup"><span data-stu-id="948c2-104">Each plan type has a plan type code that determines rules for the plan type.</span></span> <span data-ttu-id="948c2-105">Por ejemplo, el tipo de plan Vida básica tendría el código de tipo de plan Vida porque es un tipo de plan de seguro de vida y debe cumplir las reglas establecidas para el código de tipo de plan de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-105">For example, the plan type Basic life would have the plan type code Life because it’s a kind of life insurance plan and must conform to rules established for the Life plan type code.</span></span> <span data-ttu-id="948c2-106">Otro tipo de plan podría ser vida complementaria, también con el código de tipo de plan Vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-106">Another plan type might be Supplemental life, also with plan type code Life.</span></span>

<span data-ttu-id="948c2-107">Cada tipo de plan indica si un empleado puede inscribirse en un plan de su tipo o en varios.</span><span class="sxs-lookup"><span data-stu-id="948c2-107">Each plan type indicates whether an employee can enroll in one plan of its type or multiple.</span></span> <span data-ttu-id="948c2-108">Por ejemplo, es probable que un empleado pueda inscribirse tanto en las directivas de vida básica como vida complementaria del tipo de plan Vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-108">For example, an employee would likely be able to enroll in both the Basic life and the Supplemental life policies of plan type Life.</span></span> <span data-ttu-id="948c2-109">Es probable que a un empleado se le permita inscribirse en una sola directiva de tipo médico.</span><span class="sxs-lookup"><span data-stu-id="948c2-109">An employee would likely be allowed to enroll in only one policy of type Medical.</span></span>

<span data-ttu-id="948c2-110">Si un tipo de plan implica contactos, el tipo de plan indica si los contactos son beneficiarios o dependientes.</span><span class="sxs-lookup"><span data-stu-id="948c2-110">If a plan type involves contacts, the plan type indicates whether contacts are beneficiaries or dependents.</span></span> <span data-ttu-id="948c2-111">Por ejemplo, un tipo de plan de vida básico tendría beneficiarios, mientras que un tipo de plan médico básico tendría dependientes.</span><span class="sxs-lookup"><span data-stu-id="948c2-111">For example, a Basic life plan type would have beneficiaries, while a Basic medical plan type would have dependents.</span></span> <span data-ttu-id="948c2-112">En algunos casos, es posible que un plan no tenga contactos personales.</span><span class="sxs-lookup"><span data-stu-id="948c2-112">In some cases, a plan may not have any personal contacts.</span></span> <span data-ttu-id="948c2-113">Por ejemplo, una cuenta de gastos flexible o una concesión de aparcamiento.</span><span class="sxs-lookup"><span data-stu-id="948c2-113">For example, a Flexible Spending Account or Parking allowance.</span></span>

<span data-ttu-id="948c2-114">Un tipo de plan puede definir opciones de cobertura.</span><span class="sxs-lookup"><span data-stu-id="948c2-114">A plan type may define coverage options.</span></span> <span data-ttu-id="948c2-115">Las opciones de cobertura se definen en el formulario de opción de cobertura.</span><span class="sxs-lookup"><span data-stu-id="948c2-115">The coverage options are defined in the Coverage option form.</span></span> <span data-ttu-id="948c2-116">Una opción de cobertura puede especificar el importe del beneficio o los contactos que son aptos para el tipo de plan.</span><span class="sxs-lookup"><span data-stu-id="948c2-116">A coverage option can specify the amount of the benefit or the contacts who are eligible for the plan type.</span></span> <span data-ttu-id="948c2-117">Por ejemplo, si el tipo de contacto es Beneficiario, la opción de cobertura debe definir los términos para lo que el beneficiario es elegible para recibir cuando se utiliza la prestación.</span><span class="sxs-lookup"><span data-stu-id="948c2-117">For example, if the contact type is Beneficiary, the coverage option should define the terms of what the beneficiary is eligible to receive when the benefit is utilized.</span></span> <span data-ttu-id="948c2-118">Si el tipo de contacto es Dependiente, la opción de cobertura debe definir la relación entre el dependiente y el empleado.</span><span class="sxs-lookup"><span data-stu-id="948c2-118">If the contact type is Dependent, the coverage option should define the relationship between the dependent and employee.</span></span> 

1. <span data-ttu-id="948c2-119">En el espacio de trabajo **Administración de prestaciones**, en **Configuración**, seleccione **Tipos de plan**.</span><span class="sxs-lookup"><span data-stu-id="948c2-119">In the **Benefits management** workspace, under **Setup**, select **Plan types**.</span></span>

2. <span data-ttu-id="948c2-120">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="948c2-120">Select **New**.</span></span>

3. <span data-ttu-id="948c2-121">Especifique los valores para los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="948c2-121">Specify values for the following fields:</span></span>

   | <span data-ttu-id="948c2-122">Campo</span><span class="sxs-lookup"><span data-stu-id="948c2-122">Field</span></span> | <span data-ttu-id="948c2-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="948c2-123">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="948c2-124">Tipo de plan</span><span class="sxs-lookup"><span data-stu-id="948c2-124">Plan type</span></span> | <span data-ttu-id="948c2-125">Un nombre único que identifica el tipo de plan.</span><span class="sxs-lookup"><span data-stu-id="948c2-125">A unique name that identifies the plan type.</span></span> |
   | <span data-ttu-id="948c2-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="948c2-126">Description</span></span> | <span data-ttu-id="948c2-127">Una descripción del tipo de plan.</span><span class="sxs-lookup"><span data-stu-id="948c2-127">A description of the plan type.</span></span> |
   | <span data-ttu-id="948c2-128">Código de tipo de plan</span><span class="sxs-lookup"><span data-stu-id="948c2-128">Plant type code</span></span> | <span data-ttu-id="948c2-129">Seleccione un código de tipo plan en la lista desplegable de valores.</span><span class="sxs-lookup"><span data-stu-id="948c2-129">Select a plan type code from the drop down list of values.</span></span> <span data-ttu-id="948c2-130">La lista de códigos de tipo de plan muestra todos los tipos de plan admitidos en la versión actual.</span><span class="sxs-lookup"><span data-stu-id="948c2-130">The plan type code list displays all the plan types that are supported in the current version.</span></span> |
   | <span data-ttu-id="948c2-131">Inscripción simultánea</span><span class="sxs-lookup"><span data-stu-id="948c2-131">Concurrent enrollment</span></span> | <span data-ttu-id="948c2-132">Especifica si un empleado puede inscribirse en varios planes de prestaciones del mismo tipo de plan o solo un plan de prestaciones por tipo de plan.</span><span class="sxs-lookup"><span data-stu-id="948c2-132">Specifies whether an employee can enroll in multiple benefit plans of the same plan type or only one benefit plan per plan type.</span></span> |
   | <span data-ttu-id="948c2-133">Tipo de contacto</span><span class="sxs-lookup"><span data-stu-id="948c2-133">Contact type</span></span> | <span data-ttu-id="948c2-134">Especifica el rol del contacto personal.</span><span class="sxs-lookup"><span data-stu-id="948c2-134">Specifies the role of the personal contact.</span></span> <span data-ttu-id="948c2-135">Los valores son en blanco, Dependiente y Beneficiario.</span><span class="sxs-lookup"><span data-stu-id="948c2-135">The values are blank, Dependent, and Beneficiary.</span></span> <span data-ttu-id="948c2-136">Puede dejar el Tipo de contacto en blanco si su tipo de plan no requiere un dependiente o beneficiario según la opción de cobertura.</span><span class="sxs-lookup"><span data-stu-id="948c2-136">You can leave Contact type blank if their plan type does not require a dependent or beneficiary based on the coverage option.</span></span> |

4. <span data-ttu-id="948c2-137">Para configurar las opciones de eventos de vida, seleccione **Acciones** y luego seleccione **Opciones de eventos de vida**.</span><span class="sxs-lookup"><span data-stu-id="948c2-137">To configure life event options, select **Actions**, and then select **Life event options**.</span></span> <span data-ttu-id="948c2-138">Especifique los valores para los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="948c2-138">Specify values for the following fields:</span></span>

   | <span data-ttu-id="948c2-139">Campo</span><span class="sxs-lookup"><span data-stu-id="948c2-139">Field</span></span> | <span data-ttu-id="948c2-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="948c2-140">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="948c2-141">Tipo de plan</span><span class="sxs-lookup"><span data-stu-id="948c2-141">Plan type</span></span> | <span data-ttu-id="948c2-142">El tipo de plan para el que configurar opciones de eventos de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-142">The plan type to configure life event options for.</span></span> |
   | <span data-ttu-id="948c2-143">Id. del tipo de evento de vida</span><span class="sxs-lookup"><span data-stu-id="948c2-143">Life event type id</span></span> | <span data-ttu-id="948c2-144">El id. del tipo de evento de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-144">The ID of the life event type.</span></span> |
   | <span data-ttu-id="948c2-145">Permitir cancelación</span><span class="sxs-lookup"><span data-stu-id="948c2-145">Allow cancellation</span></span> | <span data-ttu-id="948c2-146">Especifica si un empleado puede cancelar un plan de prestaciones durante el evento de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-146">Specifies whether an employee can cancel a benefits plan during the life event.</span></span> |
   |<span data-ttu-id="948c2-147">Cambiar opción de cobertura</span><span class="sxs-lookup"><span data-stu-id="948c2-147">Change coverage option</span></span> | <span data-ttu-id="948c2-148">Especifica si un empleado puede cambiar opciones de cobertura durante el evento de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-148">Specifies whether an employee can change coverage options during the life event.</span></span> |
   | <span data-ttu-id="948c2-149">Cambiar a un nuevo plan</span><span class="sxs-lookup"><span data-stu-id="948c2-149">Change to a new plan</span></span> | <span data-ttu-id="948c2-150">Especifica si un empleado puede cambiar planes durante el evento de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-150">Specifies whether an employee can change plans during the life event.</span></span> |
   | <span data-ttu-id="948c2-151">Cancelar automáticamente el plan</span><span class="sxs-lookup"><span data-stu-id="948c2-151">Auto cancel plan</span></span> |<span data-ttu-id="948c2-152">Especifica si se cancelará automáticamente el plan durante el evento de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-152">Specifies whether to automatically cancel the plan during the life event.</span></span> |
   | <span data-ttu-id="948c2-153">Volver a abrir automáticamente la comprobación de idoneidad</span><span class="sxs-lookup"><span data-stu-id="948c2-153">Auto reopen eligibility check</span></span> | <span data-ttu-id="948c2-154">Especifica si la comprobación de idoneidad de la inscripción en prestaciones se debe volver a abrir automáticamente durante el evento de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-154">Specifies whether to automatically reopen the benefits enrollment eligibility check during the life event.</span></span> |
   | <span data-ttu-id="948c2-155">Ventana de notificación</span><span class="sxs-lookup"><span data-stu-id="948c2-155">Reporting window</span></span> | <span data-ttu-id="948c2-156">Especifica la ventana de notificación, en días, del evento de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-156">Specifies the reporting window, in days, of the life event.</span></span> <span data-ttu-id="948c2-157">**Nota**: Si no introduce un importe, el sistema supone que la ventana de informes es cero y no procesará el evento de vida.</span><span class="sxs-lookup"><span data-stu-id="948c2-157">**Note**: If you don't enter an amount, the system assumes the reporting window to be zero and won't process the life event.</span></span> |

5. <span data-ttu-id="948c2-158">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="948c2-158">Select **Save**.</span></span> 