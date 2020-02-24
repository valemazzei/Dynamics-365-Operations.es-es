---
title: Administración de artículos que se prestan a trabajadores
description: Los artículos de préstamo son registros que ayudan a los gerentes a realizar un seguimiento de los artículos físicos que su empresa presta a los trabajadores.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5fe1caf7e1854fd59a957ec75f3e4760d5b01837
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010433"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="e0a67-103">Administración de artículos que se prestan a trabajadores</span><span class="sxs-lookup"><span data-stu-id="e0a67-103">Manage items that are lent to workers</span></span>

<span data-ttu-id="e0a67-104">Los artículos de préstamo son registros que ayudan a los gerentes a realizar un seguimiento de los artículos físicos que su empresa presta a los trabajadores.</span><span class="sxs-lookup"><span data-stu-id="e0a67-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="e0a67-105">Los siguientes son ejemplos de artículos que las compañías pueden prestar a los trabajadores:</span><span class="sxs-lookup"><span data-stu-id="e0a67-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="e0a67-106">Teléfonos móviles</span><span class="sxs-lookup"><span data-stu-id="e0a67-106">Mobile telephones</span></span>
-   <span data-ttu-id="e0a67-107">Automóviles</span><span class="sxs-lookup"><span data-stu-id="e0a67-107">Automobiles</span></span>
-   <span data-ttu-id="e0a67-108">Equipo informático</span><span class="sxs-lookup"><span data-stu-id="e0a67-108">Computer equipment</span></span>

<span data-ttu-id="e0a67-109">Cada artículo físico debe tener un artículo correspondiente de préstamo.</span><span class="sxs-lookup"><span data-stu-id="e0a67-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="e0a67-110">Cada registro de artículo de préstamo debe describir lo que se está prestando, la persona responsable del préstamo y el número de días que se puede prestar el artículo a un trabajador.</span><span class="sxs-lookup"><span data-stu-id="e0a67-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="e0a67-111">Puede crear varios artículos en préstamo al mismo tiempo, como llaves, tarjetas de acceso o uniformes.</span><span class="sxs-lookup"><span data-stu-id="e0a67-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="e0a67-112">Al prestar un artículo, introduzca la fecha del préstamo y la fecha de devolución planificada.</span><span class="sxs-lookup"><span data-stu-id="e0a67-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="e0a67-113">Una vez devuelto el artículo, introduzca la fecha de devolución real.</span><span class="sxs-lookup"><span data-stu-id="e0a67-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="e0a67-114">Los empleados pueden ver los registros de los artículos que se han prestado mediante el espacio de trabajo Autoservicio para empleados.</span><span class="sxs-lookup"><span data-stu-id="e0a67-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="e0a67-115">También pueden corregir los registros existentes o especificar nuevos artículos de préstamo si se han recibido artículos físicos adicionales.</span><span class="sxs-lookup"><span data-stu-id="e0a67-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="e0a67-116">El flujo de trabajo se puede configurar para dirigir cambios hacia artículos de préstamo nuevos o existentes por medio de un proceso de aprobación.</span><span class="sxs-lookup"><span data-stu-id="e0a67-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="e0a67-117">Los gerentes pueden ver los artículos prestados para sus informes directos.</span><span class="sxs-lookup"><span data-stu-id="e0a67-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="e0a67-118">También pueden disponer de permiso para agregar nuevos artículos de préstamo en nombre de sus empleados.</span><span class="sxs-lookup"><span data-stu-id="e0a67-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="e0a67-119">Cuenta para los artículos de préstamos perdidos o mal colocados</span><span class="sxs-lookup"><span data-stu-id="e0a67-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="e0a67-120">Si un elemento se daña o se extravía, introduzca un registro de devolución ficticio.</span><span class="sxs-lookup"><span data-stu-id="e0a67-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="e0a67-121">A continuación, elimine el artículo o manténgalo en la visión general y cambie la descripción para indicar que el artículo no está disponible.</span><span class="sxs-lookup"><span data-stu-id="e0a67-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="e0a67-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e0a67-122">Additional resources</span></span>
--------

[<span data-ttu-id="e0a67-123">Recursos humanos</span><span class="sxs-lookup"><span data-stu-id="e0a67-123">Human resources</span></span>](index.yml)


