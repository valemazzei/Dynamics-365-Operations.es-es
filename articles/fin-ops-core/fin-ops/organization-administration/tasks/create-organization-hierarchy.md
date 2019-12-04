---
title: Crear una jerarquía organizativa
description: Realice el procedimiento siguiente para crear una jerarquía organizativa.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48c8564694b22a5110341d853a79096fbe805c91
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179864"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="ad504-103">Crear una jerarquía organizativa</span><span class="sxs-lookup"><span data-stu-id="ad504-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad504-104">Realice el procedimiento siguiente para crear una jerarquía organizativa.</span><span class="sxs-lookup"><span data-stu-id="ad504-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="ad504-105">Puede usar jerarquías organizativas para ver e informar de su negocio de diferentes perspectivas.</span><span class="sxs-lookup"><span data-stu-id="ad504-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="ad504-106">Por ejemplo, puede configurar una jerarquía para informes estatutarios, legales o de impuestos.</span><span class="sxs-lookup"><span data-stu-id="ad504-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="ad504-107">A continuación, puede configurar otra jerarquía para elaborar información financiera que no sea legalmente necesaria pero que se use para informes internos.</span><span class="sxs-lookup"><span data-stu-id="ad504-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="ad504-108">Antes de crear una jerarquía organizativa, debe crear organizaciones.</span><span class="sxs-lookup"><span data-stu-id="ad504-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="ad504-109">Para obtener más información, consulte las tareas "Crear una entidad jurídica" o "Crear una unidad operativa”.</span><span class="sxs-lookup"><span data-stu-id="ad504-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="ad504-110">También puede crear departamentos y equipos.</span><span class="sxs-lookup"><span data-stu-id="ad504-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="ad504-111">La empresa de datos de prueba utilizada para crear este procedimiento es USMF.</span><span class="sxs-lookup"><span data-stu-id="ad504-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="ad504-112">Crear una jerarquía</span><span class="sxs-lookup"><span data-stu-id="ad504-112">Create a hierarchy</span></span>
1. <span data-ttu-id="ad504-113">Vaya a **Panel de exploración > Módulos > Administración de la organización > Organizaciones > Jerarquías organizativas**.</span><span class="sxs-lookup"><span data-stu-id="ad504-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="ad504-114">En el **panel de acciones**, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ad504-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="ad504-115">En el campo **Nombre**, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="ad504-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="ad504-116">En la sección **Propósito**, haga clic en **Propósito de la asignación**.</span><span class="sxs-lookup"><span data-stu-id="ad504-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="ad504-117">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="ad504-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="ad504-118">Seleccione un propósito para asignar a su jerarquía organizativa.</span><span class="sxs-lookup"><span data-stu-id="ad504-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="ad504-119">En el sección **Jerarquías asignadas**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ad504-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="ad504-120">En la lista, marque la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ad504-120">In the list, mark the selected row.</span></span> <span data-ttu-id="ad504-121">Busque la jerarquía que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="ad504-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="ad504-122">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ad504-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="ad504-123">Agregar organizaciones a la jerarquía</span><span class="sxs-lookup"><span data-stu-id="ad504-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="ad504-124">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="ad504-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="ad504-125">Seleccione su jerarquía.</span><span class="sxs-lookup"><span data-stu-id="ad504-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="ad504-126">En la sección **Jerarquías asignadas**, haga clic en **Ver jerarquía**.</span><span class="sxs-lookup"><span data-stu-id="ad504-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="ad504-127">Agregue organizaciones según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ad504-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="ad504-128">Para agregar una organización, haga clic en **Editar** y, a continuación, en **Insertar** para agregar la organización.</span><span class="sxs-lookup"><span data-stu-id="ad504-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="ad504-129">Cuando haya terminado de realiza cambios, puede **guardar** un borrador y/o **publicar** los cambios.</span><span class="sxs-lookup"><span data-stu-id="ad504-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  
