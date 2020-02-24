---
title: Modificar las relaciones jerárquicas para un puesto
description: Este procedimiento muestra cómo cambiar la relación jerárquica para un empleado.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3285222b11905999f0eadb846ac785342c16aa38
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010496"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="b3e4c-103">Modificar las relaciones jerárquicas para un puesto</span><span class="sxs-lookup"><span data-stu-id="b3e4c-103">Modify reporting relationships for a position</span></span>



<span data-ttu-id="b3e4c-104">Este procedimiento muestra cómo cambiar la relación jerárquica para un empleado.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="b3e4c-105">La relación jerárquica se puede usar para enrutar documentos mediante el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="b3e4c-106">El procedimiento también muestra cómo asignar el empleado a jerarquías adicionales.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="b3e4c-107">Por ejemplo, un empleado puede formar parte de un equipo de proyecto con una relación jerárquica informal con un supervisor de proyecto.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="b3e4c-108">Las relaciones jerárquicas adicionales se pueden definir en el puesto para adaptar distintos escenarios de proyecto o matriz.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="b3e4c-109">La empresa de datos de prueba utilizada para crear este procedimiento es USMF.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b3e4c-110">Vaya a Recursos humanos > Puestos > Puestos.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="b3e4c-111">Use el filtro rápido para buscar registros.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b3e4c-112">Por ejemplo, filtre el campo Puesto según un valor de "000091".</span><span class="sxs-lookup"><span data-stu-id="b3e4c-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="b3e4c-113">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b3e4c-114">Expanda la sección Notifica al puesto.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="b3e4c-115">Haga clic en Nueva para abrir el cuadro de diálogo desplegable.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="b3e4c-116">En el campo Informa a, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="b3e4c-117">Haga clic en Crear.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-117">Click Create.</span></span>
8. <span data-ttu-id="b3e4c-118">Expanda la sección Relaciones.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="b3e4c-119">Haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-119">Click Add.</span></span>
10. <span data-ttu-id="b3e4c-120">Active la casilla de la izquierda de la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="b3e4c-121">En el campo Nombre de jerarquía, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="b3e4c-122">Ejemplo: Proyecto</span><span class="sxs-lookup"><span data-stu-id="b3e4c-122">Example: Project</span></span>  
12. <span data-ttu-id="b3e4c-123">En el campo Notifica al puesto, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="b3e4c-124">Ejemplo: 000437</span><span class="sxs-lookup"><span data-stu-id="b3e4c-124">Example:  000437</span></span>
13. <span data-ttu-id="b3e4c-125">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-125">Click Save.</span></span>
