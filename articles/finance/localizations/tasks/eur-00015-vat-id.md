---
title: EUR-00015 Configurar Id. de IVA
description: Este procedimiento recorre los requisitos previos de registro del identificador de IVA, como configuración de un tipo de registro y asignación a la categoría del registro.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127e6caf6a6273df36f580b32fa81219b88b8a29
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183568"
---
# <a name="eur-00015-set-up-vat-id"></a><span data-ttu-id="34673-103">EUR-00015 Configurar Id. de IVA</span><span class="sxs-lookup"><span data-stu-id="34673-103">EUR-00015 Set up VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34673-104">Este procedimiento recorre los requisitos previos de registro del identificador de IVA, como configuración de un tipo de registro y asignación a la categoría del registro.</span><span class="sxs-lookup"><span data-stu-id="34673-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="34673-105">Puede obtener información adicional acerca del identificador de registro y el procesamiento del identificador de registro, incluidas requisitos previos necesarios, en el tema de ayuda Id. de registro.</span><span class="sxs-lookup"><span data-stu-id="34673-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="34673-106">Esta información se aplica a todos los países o regiones europeos.</span><span class="sxs-lookup"><span data-stu-id="34673-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="34673-107">La tarea se ha creado con los datos de demostración de la empresa DEMF y con una dirección principal de entidad jurídica en Alemania.</span><span class="sxs-lookup"><span data-stu-id="34673-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="34673-108">Esta tarea está destinada a administradores del sistema.</span><span class="sxs-lookup"><span data-stu-id="34673-108">This task is intended for system administrators.</span></span> <span data-ttu-id="34673-109">Este procedimiento es para una función que se ha agregado en la versión 1611 de Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="34673-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="34673-110">Vaya a Administración de la organización > Libreta de direcciones global > Tipos de registro > Tipos de registro.</span><span class="sxs-lookup"><span data-stu-id="34673-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="34673-111">Haga clic en Nueva para abrir el cuadro de diálogo desplegable.</span><span class="sxs-lookup"><span data-stu-id="34673-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="34673-112">En el campo Nombre, escriba "Id. de IVA".</span><span class="sxs-lookup"><span data-stu-id="34673-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="34673-113">En el campo Descripción, número de IVA.</span><span class="sxs-lookup"><span data-stu-id="34673-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="34673-114">En el campo País o región, especifique o seleccione un valor DEU</span><span class="sxs-lookup"><span data-stu-id="34673-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="34673-115">Seleccione Sí en el campo Único.</span><span class="sxs-lookup"><span data-stu-id="34673-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="34673-116">Seleccione esta casilla para comprobar si el Id. de IVA es único.</span><span class="sxs-lookup"><span data-stu-id="34673-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="34673-117">Seleccione Sí en el campo Principal para país.</span><span class="sxs-lookup"><span data-stu-id="34673-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="34673-118">Seleccione esta casilla si el Id. de IVA debe ser efectivo para todas las direcciones que pertenecen al país/región especificados.</span><span class="sxs-lookup"><span data-stu-id="34673-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="34673-119">Haga clic en Crear.</span><span class="sxs-lookup"><span data-stu-id="34673-119">Click Create.</span></span>
9. <span data-ttu-id="34673-120">Haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="34673-120">Click Add.</span></span>
10. <span data-ttu-id="34673-121">En el campo País o región, especifique o seleccione un valor ITA</span><span class="sxs-lookup"><span data-stu-id="34673-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="34673-122">En el campo Formato, escriba "###########".</span><span class="sxs-lookup"><span data-stu-id="34673-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="34673-123">Cuando se especifica un identificador de registro de este tipo para el país o la región seleccionada, el identificador de registro se comprueba según este formato.</span><span class="sxs-lookup"><span data-stu-id="34673-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="34673-124">Seleccione la casilla Único.</span><span class="sxs-lookup"><span data-stu-id="34673-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="34673-125">Seleccione esta casilla para comprobar si el Id. de IVA es único.</span><span class="sxs-lookup"><span data-stu-id="34673-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="34673-126">Seleccione la casilla Principal para país.</span><span class="sxs-lookup"><span data-stu-id="34673-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="34673-127">Seleccione esta casilla si el Id. de IVA debe ser efectivo para todas las direcciones que pertenecen al país/región especificados.</span><span class="sxs-lookup"><span data-stu-id="34673-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="34673-128">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="34673-128">Click Save.</span></span>
15. <span data-ttu-id="34673-129">Vaya a Administración de la organización > Libreta de direcciones global > Tipos de registro > Categorías de registro.</span><span class="sxs-lookup"><span data-stu-id="34673-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="34673-130">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="34673-130">Click New.</span></span>
17. <span data-ttu-id="34673-131">En el campo País o región, especifique o seleccione un valor Id. de IVA, DEU</span><span class="sxs-lookup"><span data-stu-id="34673-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="34673-132">En el campo Categoría de registro, seleccione "Id. de IVA".</span><span class="sxs-lookup"><span data-stu-id="34673-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="34673-133">Asigne el tipo de registro que ha creado anteriormente a una categoría de registro predefinida.</span><span class="sxs-lookup"><span data-stu-id="34673-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="34673-134">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="34673-134">Click New.</span></span>
20. <span data-ttu-id="34673-135">En el campo País o región, especifique o seleccione un valor Id. de IVA, ITA</span><span class="sxs-lookup"><span data-stu-id="34673-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="34673-136">En el campo Categoría de registro, seleccione "Id. de IVA".</span><span class="sxs-lookup"><span data-stu-id="34673-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="34673-137">Asigne el tipo de registro que ha creado a una categoría de registro predefinida.</span><span class="sxs-lookup"><span data-stu-id="34673-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="34673-138">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="34673-138">Click Save.</span></span>
