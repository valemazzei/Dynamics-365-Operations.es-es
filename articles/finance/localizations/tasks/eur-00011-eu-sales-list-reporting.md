---
title: EUR-00011 Configurar informes de listas de ventas de la UE
description: Esta tarea le guía por una visión general de los requisitos previos necesarios para los Informes de listas de ventas de la UE.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b44d439bf1e991380fb7273a70e1f69f807c8b25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175112"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="40e6c-103">EUR-00011 Configurar informes de listas de ventas de la UE</span><span class="sxs-lookup"><span data-stu-id="40e6c-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40e6c-104">Esta tarea le guía por una visión general de los requisitos previos necesarios para los Informes de listas de ventas de la UE.</span><span class="sxs-lookup"><span data-stu-id="40e6c-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="40e6c-105">Para obtener más información acerca de los informes de la lista de ventas de la UE, incluidos requisitos previos necesarios, remítase a la Ayuda.</span><span class="sxs-lookup"><span data-stu-id="40e6c-105">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="40e6c-106">Esta tarea se aplica a todos los países o regiones europeos.</span><span class="sxs-lookup"><span data-stu-id="40e6c-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="40e6c-107">La guía se ha creado con la empresa de datos de demostración DEMF y, por tanto, Alemania como país o región nacional de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="40e6c-108">La guía también utiliza Portugal como país o región de la UE de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="40e6c-109">Estas tareas están destinadas a administradores del sistema.</span><span class="sxs-lookup"><span data-stu-id="40e6c-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="40e6c-110">Importar las configuraciones de informes electrónicos para informes de listas de ventas de la UE</span><span class="sxs-lookup"><span data-stu-id="40e6c-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="40e6c-111">Vaya a Administración de la organización > Espacios de trabajo > Informes electrónicos.</span><span class="sxs-lookup"><span data-stu-id="40e6c-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="40e6c-112">Haga clic en Definir como activo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-112">Click Set active.</span></span>
3. <span data-ttu-id="40e6c-113">Haga clic en Repositorios.</span><span class="sxs-lookup"><span data-stu-id="40e6c-113">Click Repositories.</span></span>
4. <span data-ttu-id="40e6c-114">Haga clic en Abrir.</span><span class="sxs-lookup"><span data-stu-id="40e6c-114">Click Open.</span></span>
5. <span data-ttu-id="40e6c-115">En el panel de acciones, haga clic en Opciones.</span><span class="sxs-lookup"><span data-stu-id="40e6c-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="40e6c-116">Haga clic en Ordenación o filtro avanzado.</span><span class="sxs-lookup"><span data-stu-id="40e6c-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="40e6c-117">Haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="40e6c-117">Click Add.</span></span>
8. <span data-ttu-id="40e6c-118">En el campo Campo, seleccione "Nombre de configuración".</span><span class="sxs-lookup"><span data-stu-id="40e6c-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="40e6c-119">En el campo Criterios, escriba "Lista de ventas de la UE (DE)".</span><span class="sxs-lookup"><span data-stu-id="40e6c-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="40e6c-120">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="40e6c-120">Click OK.</span></span>
11. <span data-ttu-id="40e6c-121">Haga clic en Importar.</span><span class="sxs-lookup"><span data-stu-id="40e6c-121">Click Import.</span></span>
12. <span data-ttu-id="40e6c-122">Haga clic en Sí.</span><span class="sxs-lookup"><span data-stu-id="40e6c-122">Click Yes.</span></span>
13. <span data-ttu-id="40e6c-123">En el panel de acciones, haga clic en Opciones.</span><span class="sxs-lookup"><span data-stu-id="40e6c-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="40e6c-124">Haga clic en Ordenación o filtro avanzado.</span><span class="sxs-lookup"><span data-stu-id="40e6c-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="40e6c-125">Haga clic en Restablecer.</span><span class="sxs-lookup"><span data-stu-id="40e6c-125">Click Reset.</span></span>
16. <span data-ttu-id="40e6c-126">Haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="40e6c-126">Click Add.</span></span>
17. <span data-ttu-id="40e6c-127">En el campo Campo, seleccione "Nombre de configuración".</span><span class="sxs-lookup"><span data-stu-id="40e6c-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="40e6c-128">En el campo Criterios, escriba "Lista de ventas de la UE por informe de filas".</span><span class="sxs-lookup"><span data-stu-id="40e6c-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="40e6c-129">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="40e6c-129">Click OK.</span></span>
20. <span data-ttu-id="40e6c-130">Haga clic en Importar.</span><span class="sxs-lookup"><span data-stu-id="40e6c-130">Click Import.</span></span>
21. <span data-ttu-id="40e6c-131">Haga clic en Sí.</span><span class="sxs-lookup"><span data-stu-id="40e6c-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="40e6c-132">Configurar códigos de impuestos para informes de listas de ventas de la UE</span><span class="sxs-lookup"><span data-stu-id="40e6c-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="40e6c-133">Vaya a Impuestos > Impuestos indirectos > Impuestos > Códigos de impuestos.</span><span class="sxs-lookup"><span data-stu-id="40e6c-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="40e6c-134">Use un filtro rápido para filtrar el campo Código de impuestos con un valor de "VAT19".</span><span class="sxs-lookup"><span data-stu-id="40e6c-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="40e6c-135">Expanda la sección Configuración del informe.</span><span class="sxs-lookup"><span data-stu-id="40e6c-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="40e6c-136">Compruebe que la selección excluida se establece en No.</span><span class="sxs-lookup"><span data-stu-id="40e6c-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="40e6c-137">Es posible que tenga que desbloquear la guía de tareas para cambiar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="40e6c-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="40e6c-138">Configurar grupos de impuestos para informes de listas de ventas de la UE</span><span class="sxs-lookup"><span data-stu-id="40e6c-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="40e6c-139">Vaya a Impuestos > Impuestos indirectos > Impuestos > Grupos de impuestos.</span><span class="sxs-lookup"><span data-stu-id="40e6c-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="40e6c-140">Use un filtro rápido para filtrar el campo Grupo de impuestos sobre las ventas con un valor de "AR-DOM".</span><span class="sxs-lookup"><span data-stu-id="40e6c-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="40e6c-141">Haga clic en Editar.</span><span class="sxs-lookup"><span data-stu-id="40e6c-141">Click Edit.</span></span>
4. <span data-ttu-id="40e6c-142">Expanda la sección Configuración.</span><span class="sxs-lookup"><span data-stu-id="40e6c-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="40e6c-143">En la lista, seleccione la primera fila.</span><span class="sxs-lookup"><span data-stu-id="40e6c-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="40e6c-144">Active la casilla Exento.</span><span class="sxs-lookup"><span data-stu-id="40e6c-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="40e6c-145">En la lista, seleccione la segunda fila.</span><span class="sxs-lookup"><span data-stu-id="40e6c-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="40e6c-146">Active la casilla Exento.</span><span class="sxs-lookup"><span data-stu-id="40e6c-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="40e6c-147">En la lista, seleccione la tercera fila.</span><span class="sxs-lookup"><span data-stu-id="40e6c-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="40e6c-148">Active la casilla Exento.</span><span class="sxs-lookup"><span data-stu-id="40e6c-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="40e6c-149">Configurar grupos de impuestos de artículos para informes de listas de ventas de la UE</span><span class="sxs-lookup"><span data-stu-id="40e6c-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="40e6c-150">Vaya a Impuestos > Impuestos indirectos > Impuestos > Grupos de impuestos de artículos.</span><span class="sxs-lookup"><span data-stu-id="40e6c-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="40e6c-151">Use un filtro rápido para filtrar por el campo Grupo de impuestos de artículos con un valor de "FULL".</span><span class="sxs-lookup"><span data-stu-id="40e6c-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="40e6c-152">Compruebe que la selección Tipo de notificación se establece en "Artículo".</span><span class="sxs-lookup"><span data-stu-id="40e6c-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="40e6c-153">Es posible que tenga que desbloquear la guía de tareas para cambiar el valor en este campo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="40e6c-154">Use un filtro rápido para filtrar por el campo Grupo de impuestos de artículos con un valor de "RED".</span><span class="sxs-lookup"><span data-stu-id="40e6c-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="40e6c-155">Compruebe que la selección Tipo de notificación se establece en "Servicio".</span><span class="sxs-lookup"><span data-stu-id="40e6c-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="40e6c-156">Es posible que tenga que desbloquear la guía de tareas para cambiar el valor en este campo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="40e6c-157">Configurar parámetros de país o región para informes de listas de ventas de la UE</span><span class="sxs-lookup"><span data-stu-id="40e6c-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="40e6c-158">Vaya a Impuestos > Configuración > Impuestos > Parámetros por país o región.</span><span class="sxs-lookup"><span data-stu-id="40e6c-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="40e6c-159">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-159">Click New.</span></span>
3. <span data-ttu-id="40e6c-160">En el campo País/región, escriba "PRT".</span><span class="sxs-lookup"><span data-stu-id="40e6c-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="40e6c-161">En el campo Impuestos, escriba "PT".</span><span class="sxs-lookup"><span data-stu-id="40e6c-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="40e6c-162">Crear números de exención fiscal</span><span class="sxs-lookup"><span data-stu-id="40e6c-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="40e6c-163">Vaya a Impuestos > Configuración > Impuestos > Números de identificación fiscal.</span><span class="sxs-lookup"><span data-stu-id="40e6c-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="40e6c-164">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-164">Click New.</span></span>
3. <span data-ttu-id="40e6c-165">En el campo País/región, escriba "PRT".</span><span class="sxs-lookup"><span data-stu-id="40e6c-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="40e6c-166">En el campo NIF, escriba "PT12345".</span><span class="sxs-lookup"><span data-stu-id="40e6c-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="40e6c-167">Configurar parámetros de informes de listas de ventas de la UE</span><span class="sxs-lookup"><span data-stu-id="40e6c-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="40e6c-168">Vaya a Impuestos > Configuración > Comercio exterior > Parámetros de comercio exterior.</span><span class="sxs-lookup"><span data-stu-id="40e6c-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="40e6c-169">Haga clic en la ficha Lista de ventas de la UE.</span><span class="sxs-lookup"><span data-stu-id="40e6c-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="40e6c-170">Seleccione Sí en el campo Transferir compras.</span><span class="sxs-lookup"><span data-stu-id="40e6c-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="40e6c-171">Expanda la sección Reglas de redondeo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="40e6c-172">Establezca la regla de redondeo en "0,1".</span><span class="sxs-lookup"><span data-stu-id="40e6c-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="40e6c-173">Seleccione Sí en el campo Usar valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="40e6c-174">En el campo Número de decimales, escriba "2".</span><span class="sxs-lookup"><span data-stu-id="40e6c-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="40e6c-175">Expanda la sección Informes electrónicos.</span><span class="sxs-lookup"><span data-stu-id="40e6c-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="40e6c-176">En el campo Asignación de formato de archivo, seleccione "Lista de ventas de la UE (DE)".</span><span class="sxs-lookup"><span data-stu-id="40e6c-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="40e6c-177">En el campo Asignación de formato de informe, seleccione "Lista de ventas de la UE por informe de filas".</span><span class="sxs-lookup"><span data-stu-id="40e6c-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="40e6c-178">Haga clic en la ficha Propiedades de país/región.</span><span class="sxs-lookup"><span data-stu-id="40e6c-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="40e6c-179">Compruebe que el campo Tipo de país/región está establecido en "Nacional" para País o región DEU.</span><span class="sxs-lookup"><span data-stu-id="40e6c-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="40e6c-180">Es posible que tenga que desbloquear la guía de tareas para cambiar el valor en este campo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="40e6c-181">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-181">Click New.</span></span>
13. <span data-ttu-id="40e6c-182">En el campo País/región, escriba "PRT".</span><span class="sxs-lookup"><span data-stu-id="40e6c-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="40e6c-183">En el campo Código intrastat, escriba "PT".</span><span class="sxs-lookup"><span data-stu-id="40e6c-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="40e6c-184">En el campo Tipo de país/región, seleccione "UE".</span><span class="sxs-lookup"><span data-stu-id="40e6c-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="40e6c-185">Haga clic en la ficha Secuencias numéricas.</span><span class="sxs-lookup"><span data-stu-id="40e6c-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="40e6c-186">Compruebe que hay un Código de secuencia numérica especificado para la referencia "Lista de ventas de la UE".</span><span class="sxs-lookup"><span data-stu-id="40e6c-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="40e6c-187">Crear un cliente para fines de demostración de informes de lista de ventas de la UE</span><span class="sxs-lookup"><span data-stu-id="40e6c-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="40e6c-188">Vaya a Clientes > Clientes > Todos los clientes.</span><span class="sxs-lookup"><span data-stu-id="40e6c-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="40e6c-189">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="40e6c-189">Click New.</span></span>
3. <span data-ttu-id="40e6c-190">En el campo Cuenta de cliente, escriba "PRT-001".</span><span class="sxs-lookup"><span data-stu-id="40e6c-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="40e6c-191">En el campo Nombre, escriba "Un cliente de Portugal".</span><span class="sxs-lookup"><span data-stu-id="40e6c-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="40e6c-192">En el campo Grupo de clientes seleccione "10".</span><span class="sxs-lookup"><span data-stu-id="40e6c-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="40e6c-193">En el campo Grupo de impuestos, seleccione "AR-DOM".</span><span class="sxs-lookup"><span data-stu-id="40e6c-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="40e6c-194">En el campo NIF, seleccione "PT12345".</span><span class="sxs-lookup"><span data-stu-id="40e6c-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="40e6c-195">En el campo País/región, escriba "PRT".</span><span class="sxs-lookup"><span data-stu-id="40e6c-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="40e6c-196">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="40e6c-196">Click Save.</span></span>
