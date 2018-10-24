---
title: Flujo de trabajo de proveedor
description: "Modifique la información del proveedor y use el flujo de trabajo para aprobarla."
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Vendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 950a1852acf9f3e4747ce2d55738c0eb3a646897
ms.contentlocale: es-es
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-workflow"></a><span data-ttu-id="7e14f-103">Flujo de trabajo de proveedor</span><span class="sxs-lookup"><span data-stu-id="7e14f-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e14f-104">Cuando se usa el flujo de trabajo de proveedor, los cambios que se realizan a campos específicos se envían al flujo de trabajo para su aprobación antes de que se agreguen al proveedor.</span><span class="sxs-lookup"><span data-stu-id="7e14f-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="7e14f-105">Configurar el flujo de trabajo del proveedor</span><span class="sxs-lookup"><span data-stu-id="7e14f-105">Set up the vendor workflow</span></span>

<span data-ttu-id="7e14f-106">Para poder utilizar la funcionalidad de flujo de trabajo debe activarla.</span><span class="sxs-lookup"><span data-stu-id="7e14f-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="7e14f-107">Vaya a **Proveedores \> Configuración \> Parámetros de proveedores**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="7e14f-108">En la pestaña **General**, en la ficha desplegable **Aprobación del proveedor**, establezca la opción **Habilitar aprobaciones de proveedor** en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="7e14f-109">En el campo **Comportamiento de entidad de datos**, seleccione el comportamiento que se debe usar cuando se importan datos:</span><span class="sxs-lookup"><span data-stu-id="7e14f-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="7e14f-110">**Permitir cambios sin aprobación** La entidad de datos puede actualizar el registro de proveedor sin procesarlo con el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7e14f-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="7e14f-111">**Rechazar cambios** – Los cambios no se pueden introducir en el registro de proveedor.</span><span class="sxs-lookup"><span data-stu-id="7e14f-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="7e14f-112">La importación fallará para los campos habilitados para el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7e14f-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="7e14f-113">**Crear propuestas de cambio** – Todos los campos se cambiarán excepto los campos habilitados para el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7e14f-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="7e14f-114">Los nuevos valores para estos campos se agregarán al proveedor como cambios propuestos y el flujo de trabajo se iniciará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7e14f-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="7e14f-115">En la lista de campos de proveedor, seleccione la casilla de verificación **Habilitar** para cada campo que debe aprobarse antes de que los cambios se puedan realizar.</span><span class="sxs-lookup"><span data-stu-id="7e14f-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="7e14f-116">Vaya a **Proveedores \> Configuración \> Flujos de trabajo de proveedores**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="7e14f-117">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-117">Select **New**.</span></span>
7. <span data-ttu-id="7e14f-118">Seleccione **Flujo de trabajo de cambios de proveedor propuestos**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="7e14f-119">Configure el flujo de trabajo para que coincida con el proceso de aprobación.</span><span class="sxs-lookup"><span data-stu-id="7e14f-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="7e14f-120">El elemento de aprobación del flujo de trabajo **Aprobación de flujo de trabajo para el cambio del proveedor propuesto** aplicará los cambios al proveedor.</span><span class="sxs-lookup"><span data-stu-id="7e14f-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="7e14f-121">Cambie la información del proveedor y registre los cambios en el flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="7e14f-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="7e14f-122">Cuando se cambia un campo que está habilitado para el flujo de trabajo, la página **Cambios propuestos** aparece.</span><span class="sxs-lookup"><span data-stu-id="7e14f-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="7e14f-123">Esta página muestra el valor original del campo y el nuevo valor que ha especificado.</span><span class="sxs-lookup"><span data-stu-id="7e14f-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="7e14f-124">El campo que ha cambiado se revierte a su valor original.</span><span class="sxs-lookup"><span data-stu-id="7e14f-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="7e14f-125">Un mensaje de estado también le informa de que los cambios no se han enviado.</span><span class="sxs-lookup"><span data-stu-id="7e14f-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="7e14f-126">Cada vez que se cambia un campo que está habilitado para el flujo de trabajo, dicho campo se agrega a la lista en la página **Cambios propuestos**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="7e14f-127">Para descartar el valor propuesto para un campo, use el botón **Descartar** junto al campo de la lista.</span><span class="sxs-lookup"><span data-stu-id="7e14f-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="7e14f-128">Para descartar todos los cambios, use el botón **Descartar todos los cambios** en la parte inferior de la página.</span><span class="sxs-lookup"><span data-stu-id="7e14f-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="7e14f-129">Seleccione **Aceptar** para cerrar la página.</span><span class="sxs-lookup"><span data-stu-id="7e14f-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="7e14f-130">Tras tener al menos un cambio propuesto, dos fichas adicionales aparecen en el panel de acciones: **Cambios propuestos** y **Flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="7e14f-131">Seleccione **Cambios propuestos** para abrir la página **Cambios propuestos** y revisar los cambios.</span><span class="sxs-lookup"><span data-stu-id="7e14f-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="7e14f-132">Seleccione **Flujo de trabajo \> Enviar para enviar los cambios al flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="7e14f-133">El estado que se muestra en la página cambia a **Cambios pendientes de aprobación**.</span><span class="sxs-lookup"><span data-stu-id="7e14f-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="7e14f-134">El flujo de trabajo sigue el proceso de flujo de trabajo estándar en Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7e14f-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="7e14f-135">Dirige al aprobador a la página **Proveedor**, donde puede revisar los cambios en la página **Cambios propuestos** y después seleccionar **Flujo de trabajo \> Aprobar** para aprobar el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7e14f-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="7e14f-136">Después de completar todas las aprobaciones, los campos se actualizan con los valores que se proponen.</span><span class="sxs-lookup"><span data-stu-id="7e14f-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
