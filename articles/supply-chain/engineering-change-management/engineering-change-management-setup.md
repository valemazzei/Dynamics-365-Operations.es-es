---
title: Establecer valores comunes para la gestión de cambios de ingeniería
description: Este tema describe cómo establecer valores comunes que se utilizan para los parámetros en varias partes de la gestión de cambios de ingeniería.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 86de050ef4110e3485a77099440f3402e46cc498
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/29/2020
ms.locfileid: "4437307"
---
# <a name="establish-common-values-for-engineering-change-management"></a><span data-ttu-id="84e90-103">Establecer valores comunes para la gestión de cambios de ingeniería</span><span class="sxs-lookup"><span data-stu-id="84e90-103">Establish common values for engineering change management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84e90-104">Cuando configura la administración de cambios de ingeniería, debe establecer varias colecciones de valores que se utilizarán para completar listas desplegables en otras partes de la interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="84e90-104">When you set up engineering change management, you must establish several collections of values that will be used to fill in drop-down lists in other parts of the user interface (UI).</span></span> <span data-ttu-id="84e90-105">Debe especificar estos valores de acuerdo con los tipos de productos que produce y sus necesidades comerciales específicas.</span><span class="sxs-lookup"><span data-stu-id="84e90-105">You should specify these values according to the types of products that you produce and your specific business needs.</span></span>

## <a name="engineering-change-categories"></a><span data-ttu-id="84e90-106">Categoría de cambio de ingeniería</span><span class="sxs-lookup"><span data-stu-id="84e90-106">Engineering change categories</span></span>

<span data-ttu-id="84e90-107">Utiliza categorías de cambio de ingeniería para organizar sus órdenes de cambio de ingeniería, de modo que sean más fáciles de administrar y revisar.</span><span class="sxs-lookup"><span data-stu-id="84e90-107">You use engineering change categories to organize your engineering change orders, so that they are easier to manage and review.</span></span> <span data-ttu-id="84e90-108">Por ejemplo, puede resultarle útil configurar un flujo de trabajo en el que, según la categoría, un departamento específico deba revisar los cambios propuestos.</span><span class="sxs-lookup"><span data-stu-id="84e90-108">For example, you might find it useful to set up a workflow where, depending on the category, a specific department must review the proposed changes.</span></span> <span data-ttu-id="84e90-109">Por lo tanto, la orden de cambio de ingeniería incluye un campo **Categoría**.</span><span class="sxs-lookup"><span data-stu-id="84e90-109">Therefore, the engineering change order includes a **Category** field.</span></span>

<span data-ttu-id="84e90-110">Para establecer la colección de categorías de cambios de ingeniería que se utilizan en su empresa, vaya a **Gestión de cambios de ingeniería \> Preparar \> Gestión de cambios de ingeniería \> Categorías de cambio de ingeniería**.</span><span class="sxs-lookup"><span data-stu-id="84e90-110">To establish the collection of engineering change categories that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change categories**.</span></span> <span data-ttu-id="84e90-111">Luego, puede usar los botones en el Panel de acciones para agregar, eliminar y editar valores, y para organizarlos en el orden en el que deben aparecer en las listas desplegables donde se muestran.</span><span class="sxs-lookup"><span data-stu-id="84e90-111">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-priorities"></a><span data-ttu-id="84e90-112">Prioridades de cambio de ingeniería</span><span class="sxs-lookup"><span data-stu-id="84e90-112">Engineering change priorities</span></span>

<span data-ttu-id="84e90-113">Utiliza las prioridades de cambio de ingeniería para indicar la importancia o urgencia de una orden de cambio de ingeniería.</span><span class="sxs-lookup"><span data-stu-id="84e90-113">You use engineering change priorities to indicate the importance or urgency of an engineering change order.</span></span> <span data-ttu-id="84e90-114">Pueden ayudarlo a realizar un seguimiento de la importancia de una orden de cambio de ingeniería, de modo que pueda identificar fácilmente qué órdenes deben procesarse primero y con qué rapidez.</span><span class="sxs-lookup"><span data-stu-id="84e90-114">They can help you keep track of the importance of an engineering change order, so that you can easily identify which orders should be processed first, and how quickly.</span></span>

<span data-ttu-id="84e90-115">Para establecer la colección de prioridades de cambios de ingeniería que se utilizan en su empresa, vaya a **Gestión de cambios de ingeniería \> Preparar \> Gestión de cambios de ingeniería \> Prioridades de cambio de ingeniería**.</span><span class="sxs-lookup"><span data-stu-id="84e90-115">To establish the collection of engineering change priorities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change priorities**.</span></span> <span data-ttu-id="84e90-116">Luego, puede usar los botones en el Panel de acciones para agregar, eliminar y editar valores, y para organizarlos en el orden en el que deben aparecer en las listas desplegables donde se muestran.</span><span class="sxs-lookup"><span data-stu-id="84e90-116">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-reasons"></a><span data-ttu-id="84e90-117">Motivos del cambio de ingeniería</span><span class="sxs-lookup"><span data-stu-id="84e90-117">Engineering change reasons</span></span>

<span data-ttu-id="84e90-118">Las razones del cambio de ingeniería indican la causa o la naturaleza del cambio en la orden de cambio.</span><span class="sxs-lookup"><span data-stu-id="84e90-118">Engineering change reasons indicate the cause or nature of the change in the change order.</span></span>

<span data-ttu-id="84e90-119">Para establecer la colección de razones de cambios de ingeniería que se utilizan en su empresa, vaya a **Gestión de cambios de ingeniería \> Preparar \> Gestión de cambios de ingeniería \> Razones de cambio de ingeniería**.</span><span class="sxs-lookup"><span data-stu-id="84e90-119">To establish the collection of engineering change reasons that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change reasons**.</span></span> <span data-ttu-id="84e90-120">Luego, puede usar los botones en el Panel de acciones para agregar, eliminar y editar valores, y para organizarlos en el orden en el que deben aparecer en las listas desplegables donde se muestran.</span><span class="sxs-lookup"><span data-stu-id="84e90-120">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="material-disposal-codes"></a><span data-ttu-id="84e90-121">Códigos de eliminación de material</span><span class="sxs-lookup"><span data-stu-id="84e90-121">Material disposal codes</span></span>

<span data-ttu-id="84e90-122">Utiliza códigos de eliminación de materiales para clasificar los materiales que se utilizan en sus productos terminados o los componentes que deben eliminarse de una manera específica o que requieren algún tratamiento antes de que puedan agregarse a su basura habitual.</span><span class="sxs-lookup"><span data-stu-id="84e90-122">You use material disposal codes to categorize materials that are used in your finished goods, or components that must be disposed of in a specific way or require some treatment before they can be added to your regular trash.</span></span> <span data-ttu-id="84e90-123">Cuando agrega un producto relevante a una orden de cambio de ingeniería, puede asignar un código de eliminación como parte de los detalles del cambio.</span><span class="sxs-lookup"><span data-stu-id="84e90-123">When you add a relevant product to an engineering change order, you can assign a disposal code as part of the change details.</span></span>

<span data-ttu-id="84e90-124">Para establecer la colección de códigos de disposición de material que se utilizan en su empresa, vaya a **Gestión de cambios de ingeniería \> Preparar \> Gestión de cambios de ingeniería \> Códigos de disposición de material**.</span><span class="sxs-lookup"><span data-stu-id="84e90-124">To establish the collection of material disposal codes that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Material disposal codes**.</span></span> <span data-ttu-id="84e90-125">Luego, puede usar los botones en el Panel de acciones para agregar, eliminar y editar valores, y para organizarlos en el orden en el que deben aparecer en las listas desplegables donde se muestran.</span><span class="sxs-lookup"><span data-stu-id="84e90-125">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="received-customer-approval"></a><span data-ttu-id="84e90-126">Aprobación del cliente recibida</span><span class="sxs-lookup"><span data-stu-id="84e90-126">Received customer approval</span></span>

<span data-ttu-id="84e90-127">Cuando diseña productos para un cliente específico, el diseño y las especificaciones a menudo deben validarse antes de que el producto pueda configurarse como listo.</span><span class="sxs-lookup"><span data-stu-id="84e90-127">When you design products for a specific customer, the design and specifications often must be validated before the product can be set as ready.</span></span> <span data-ttu-id="84e90-128">El campo **Recibió la aprobación del cliente** le permite indicar qué tan avanzado se encuentra el producto en el proceso de aprobación del cliente y / o si se ha recibido la aprobación.</span><span class="sxs-lookup"><span data-stu-id="84e90-128">The **Received customer approval** field lets you indicate how far in the customer approval process the product is and/or whether the approval has been received.</span></span>

<span data-ttu-id="84e90-129">Para establecer la colección de valores de aprobación de cliente recibidos que se utilizan en su empresa, vaya a **Gestión de cambios de ingeniería \> Preparar \> Gestión de cambios de ingeniería \> Aprobación de cliente recibida**.</span><span class="sxs-lookup"><span data-stu-id="84e90-129">To establish the collection of received customer approval values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Received customer approval**.</span></span> <span data-ttu-id="84e90-130">Luego, puede usar los botones en el Panel de acciones para agregar, eliminar y editar valores, y para organizarlos en el orden en el que deben aparecer en las listas desplegables donde se muestran.</span><span class="sxs-lookup"><span data-stu-id="84e90-130">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change--environmental-health-and-safety-codes"></a><span data-ttu-id="84e90-131">Cambio de ingeniería: códigos de seguridad y salud ambiental</span><span class="sxs-lookup"><span data-stu-id="84e90-131">Engineering change – Environmental health and safety codes</span></span>

<span data-ttu-id="84e90-132">Si en la fabricación de un producto se debe tener en cuenta alguna reglamentación estándar de salud y seguridad ambiental, o reglamentación o procedimiento específico de la empresa, puede utilizar los códigos de salud y seguridad ambiental para definirla.</span><span class="sxs-lookup"><span data-stu-id="84e90-132">If any standard environmental health and safety regulations, or company-specific regulations or procedures, must be considered in the manufacture of a product, you can use the environmental health and safety codes to define them.</span></span> <span data-ttu-id="84e90-133">En la orden de cambio de ingeniería, puede indicar qué códigos se aplican a la fabricación de un producto mientras edita los detalles del producto afectado.</span><span class="sxs-lookup"><span data-stu-id="84e90-133">In the engineering change order, you can indicate which codes apply to the manufacture of a product while you edit the details of the affected product.</span></span>

<span data-ttu-id="84e90-134">Para establecer la colección de valores de salud y seguridad que se utilizan en su empresa, vaya a **Gestión de cambios de ingeniería \> Preparar \> Gestión de cambios de ingeniería \> Códigos de salud y seguridad medioambientales**.</span><span class="sxs-lookup"><span data-stu-id="84e90-134">To establish the collection of health and safety values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change - Environmental health and safety codes**.</span></span> <span data-ttu-id="84e90-135">Luego, puede usar los botones en el Panel de acciones para agregar, eliminar y editar valores, y para organizarlos en el orden en el que deben aparecer en las listas desplegables donde se muestran.</span><span class="sxs-lookup"><span data-stu-id="84e90-135">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-severities"></a><span data-ttu-id="84e90-136">Gravedad de los cambios de ingeniería</span><span class="sxs-lookup"><span data-stu-id="84e90-136">Engineering change severities</span></span>

<span data-ttu-id="84e90-137">Utiliza la gravedad de los cambios de ingeniería para indicar el nivel de impacto que se aplica a los productos en una orden de cambio de ingeniería.</span><span class="sxs-lookup"><span data-stu-id="84e90-137">You use engineering change severities to indicate the level of impact that applies to the products in an engineering change order.</span></span>

<span data-ttu-id="84e90-138">Para establecer la colección de gravedades de cambios de ingeniería que se utilizan en su empresa, vaya a **Gestión de cambios de ingeniería \> Preparar \> Gestión de cambios de ingeniería \> Gravedades de cambio de ingeniería**.</span><span class="sxs-lookup"><span data-stu-id="84e90-138">To establish the collection of engineering change severities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severities**.</span></span> <span data-ttu-id="84e90-139">Luego, puede usar los botones en el Panel de acciones para agregar, eliminar y editar valores, y para organizarlos en el orden en el que deben aparecer en las listas desplegables donde se muestran.</span><span class="sxs-lookup"><span data-stu-id="84e90-139">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

<span data-ttu-id="84e90-140">Puede establecer reglas que se apliquen a cada nivel de gravedad que cree.</span><span class="sxs-lookup"><span data-stu-id="84e90-140">You can establish rules that apply to each severity level that you create.</span></span> <span data-ttu-id="84e90-141">Para obtener más información sobre cómo asignar estas reglas, consulte la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="84e90-141">For more information about how to assign these rules, see the next section.</span></span>

## <a name="engineering-change-severity-rule-sets"></a><span data-ttu-id="84e90-142">Conjuntos de reglas de gravedad de cambio de ingeniería</span><span class="sxs-lookup"><span data-stu-id="84e90-142">Engineering change severity rule sets</span></span>

<span data-ttu-id="84e90-143">Utilice conjuntos de reglas de gravedad de cambios de ingeniería para establecer un grupo de reglas que puede utilizar para calcular automáticamente la gravedad de la orden de cambio, según el tipo de cambios en los productos afectados.</span><span class="sxs-lookup"><span data-stu-id="84e90-143">You use engineering change severity rule sets to establish a group of rules that you can use to automatically calculate the severity of the change order, based on the type of changes in the affected products.</span></span> <span data-ttu-id="84e90-144">Para usar las reglas de gravedad, abra la página **Parámetros de gestión de cambios de ingeniería** y establezca el campo **Regla de gravedad** en *Calcular* o *Calcular automáticamente*.</span><span class="sxs-lookup"><span data-stu-id="84e90-144">To use the severity rules, open the **Engineering change management parameters** page, and set the **Severity rule** field to *Calculate* or *Calculate automatically*.</span></span>

<span data-ttu-id="84e90-145">Cuando el sistema evalúa la gravedad, procesa las reglas en el orden en que aparecen en la página, de arriba a abajo.</span><span class="sxs-lookup"><span data-stu-id="84e90-145">When the system evaluates severity, it processes the rules in the order in which they appear on the page, from top to bottom.</span></span> <span data-ttu-id="84e90-146">Para que se seleccione una regla y se establezca su prioridad, se deben cumplir todas las reglas de un conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="84e90-146">For a rule to be selected and have its priority established, all the rules in a rule set must be met.</span></span>

<span data-ttu-id="84e90-147">Para configurar las reglas que se aplican a cada nivel de gravedad de cambio que haya definido, vaya a **Gestión de cambios de ingeniería \> Preparar \> Gestión de cambios de ingeniería \> Conjuntos de reglas de gravedad de cambios de ingeniería**.</span><span class="sxs-lookup"><span data-stu-id="84e90-147">To set up the rules that apply to each change severity level that you've defined, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severity rule sets**.</span></span> <span data-ttu-id="84e90-148">Luego siga uno de estos pasos.</span><span class="sxs-lookup"><span data-stu-id="84e90-148">Then follow one of these steps.</span></span>

- <span data-ttu-id="84e90-149">Para crear un nuevo conjunto de reglas, seleccione **Nuevo** en el Panel de acciones y luego configure los campos como se describe más adelante en esta sección.</span><span class="sxs-lookup"><span data-stu-id="84e90-149">To create a new rule set, select **New** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="84e90-150">Para editar un conjunto de reglas existente, selecciónelo en el panel de lista, seleccione **Editar** en el Panel de acciones y luego configure los campos como se describe más adelante en esta sección.</span><span class="sxs-lookup"><span data-stu-id="84e90-150">To edit an existing rule set, select it in the list pane, select **Edit** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="84e90-151">Para eliminar un conjunto de reglas existente, selecciónelo en el panel de lista y luego seleccione **Eliminar** en el Panel de acciones.</span><span class="sxs-lookup"><span data-stu-id="84e90-151">To delete an existing rule set, select it in the list pane, and then select **Delete** on the Action Pane.</span></span>
- <span data-ttu-id="84e90-152">Para reorganizar la lista de conjuntos de reglas, seleccione un conjunto de reglas en el panel de lista y luego use los botoones **Arriba** y **Abajo** del Panel de acciones para reposicionarlo.</span><span class="sxs-lookup"><span data-stu-id="84e90-152">To rearrange the list of rule sets, select a rule set in the list pane, and then use the **Up** and **Down** buttons on the Action Pane to reposition it.</span></span>

<span data-ttu-id="84e90-153">Para cada conjutno de reglas, establezca el siguiente campo:</span><span class="sxs-lookup"><span data-stu-id="84e90-153">For each rule set, set the following field:</span></span>

- <span data-ttu-id="84e90-154">**Gravedad** - Seleccione el nivel de gravedad para el que establecer reglas.</span><span class="sxs-lookup"><span data-stu-id="84e90-154">**Severity** – Select the severity level to establish rules for.</span></span> <span data-ttu-id="84e90-155">Use la página **Severidades de cambios de ingeniería** para crear y nombrar los niveles.</span><span class="sxs-lookup"><span data-stu-id="84e90-155">You use the **Engineering change severities** page to create and name the levels.</span></span> <span data-ttu-id="84e90-156">(Vea la sección anterior para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="84e90-156">(For more information, see the previous section.)</span></span>

<span data-ttu-id="84e90-157">Utilice los botones de la ficha desplegable **Reglas** para agregar o quitar una regla para la configuración de gravedad actual.</span><span class="sxs-lookup"><span data-stu-id="84e90-157">Use the buttons on the **Rules** FastTab to add or remove a rule for the current severity setting.</span></span> <span data-ttu-id="84e90-158">Cada regla tiene un campo **Regla** y un campo **Nombre**.</span><span class="sxs-lookup"><span data-stu-id="84e90-158">Each rule has a **Rule** field and a **Name** field.</span></span> <span data-ttu-id="84e90-159">Las reglas las establece el sistema e indican los tipos de cambios que puede tener un producto.</span><span class="sxs-lookup"><span data-stu-id="84e90-159">The rules are established by the system and indicate the types of changes that a product can have.</span></span> <span data-ttu-id="84e90-160">El nombre indica el tipo de modificación.</span><span class="sxs-lookup"><span data-stu-id="84e90-160">The name indicates the type of change.</span></span>