---
title: Reglas de precios de categoría para crear acuerdos comerciales
description: Este procedimiento muestra cómo crear acuerdos comerciales de precios de venta con una regla de precios de categoría.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35c85e6e3bbdc913e9cd7aefdf6b143f3f03496f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023945"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="d0056-103">Reglas de precios de categoría para crear acuerdos comerciales</span><span class="sxs-lookup"><span data-stu-id="d0056-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d0056-104">Este procedimiento muestra cómo crear acuerdos comerciales de precios de venta con una regla de precios de categoría.</span><span class="sxs-lookup"><span data-stu-id="d0056-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="d0056-105">La empresa de datos de prueba utilizada para crear esta tarea es USRT.</span><span class="sxs-lookup"><span data-stu-id="d0056-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="d0056-106">Esta tarea está pensada para el rol de encargado de comercialización de Commerce.</span><span class="sxs-lookup"><span data-stu-id="d0056-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="d0056-107">Haga clic en Administración de precios y descuentos.</span><span class="sxs-lookup"><span data-stu-id="d0056-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="d0056-108">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="d0056-108">Click New.</span></span>
3. <span data-ttu-id="d0056-109">Haga clic en Regla de precios de categoría.</span><span class="sxs-lookup"><span data-stu-id="d0056-109">Click Category price rule.</span></span>
4. <span data-ttu-id="d0056-110">En la lista, marque la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="d0056-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d0056-111">En el campo Código de cuenta, seleccione una opción.</span><span class="sxs-lookup"><span data-stu-id="d0056-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="d0056-112">Se usa un código de cuenta de tipo "Grupo" para configurar los acuerdos comerciales de precio de ventas específicos para Canales, Programas de fidelización, Catálogos y Afiliaciones.</span><span class="sxs-lookup"><span data-stu-id="d0056-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="d0056-113">En el campo Selección de cuentas, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="d0056-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="d0056-114">En el campo Categoría, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="d0056-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="d0056-115">En el campo Importe/porcentaje, escriba un número.</span><span class="sxs-lookup"><span data-stu-id="d0056-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="d0056-116">En el campo Versión de redondeo, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="d0056-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="d0056-117">Haga clic en Generar acuerdos comerciales.</span><span class="sxs-lookup"><span data-stu-id="d0056-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="d0056-118">Haga clic en Siguiente.</span><span class="sxs-lookup"><span data-stu-id="d0056-118">Click Next.</span></span>
12. <span data-ttu-id="d0056-119">En el campo Fecha inicial, escriba una fecha.</span><span class="sxs-lookup"><span data-stu-id="d0056-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="d0056-120">Especifique una fecha en el campo Fecha final.</span><span class="sxs-lookup"><span data-stu-id="d0056-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="d0056-121">Seleccione Sí en el campo Buscar siguiente.</span><span class="sxs-lookup"><span data-stu-id="d0056-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="d0056-122">Haga clic en Siguiente.</span><span class="sxs-lookup"><span data-stu-id="d0056-122">Click Next.</span></span>
16. <span data-ttu-id="d0056-123">Haga clic en Finalizar.</span><span class="sxs-lookup"><span data-stu-id="d0056-123">Click Finish.</span></span>
    * <span data-ttu-id="d0056-124">Esto crea un Diario de acuerdos comerciales y lo abre para su revisión.</span><span class="sxs-lookup"><span data-stu-id="d0056-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="d0056-125">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="d0056-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d0056-126">No se registran los diarios de acuerdos comerciales creados a partir de reglas de precios de categoría.</span><span class="sxs-lookup"><span data-stu-id="d0056-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="d0056-127">Puede revisar y editar los precios generados antes de registrarlos.</span><span class="sxs-lookup"><span data-stu-id="d0056-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="d0056-128">Haga clic en Editar.</span><span class="sxs-lookup"><span data-stu-id="d0056-128">Click Edit.</span></span>
19. <span data-ttu-id="d0056-129">En el campo Importe en divisa, escriba un número.</span><span class="sxs-lookup"><span data-stu-id="d0056-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="d0056-130">Haga clic en Registrar.</span><span class="sxs-lookup"><span data-stu-id="d0056-130">Click Post.</span></span>
21. <span data-ttu-id="d0056-131">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="d0056-131">Click OK.</span></span>
22. <span data-ttu-id="d0056-132">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="d0056-132">Close the page.</span></span>
23. <span data-ttu-id="d0056-133">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="d0056-133">Close the page.</span></span>
24. <span data-ttu-id="d0056-134">Haga clic en la ficha Reglas de precios de categoría.</span><span class="sxs-lookup"><span data-stu-id="d0056-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="d0056-135">Las reglas de precios de categoría específicas de canal se mostrarán en esta lista.</span><span class="sxs-lookup"><span data-stu-id="d0056-135">Channel specific Category pricing rules will show in this list.</span></span>  
