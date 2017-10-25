--- 
title: "Ejecutar el formato para realizar recuentos y sumas para informes electrónicos (ER)"
description: "Los pasos siguientes explican cómo un usuario asignado al administrador del sistema o al rol de desarrollador de informes electrónicos puede configurar un formato de informe electrónico (ER) para que realice el recuento y calcule en función de los datos de la salida de texto ya generada."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9f5520dc4e1eddc2fc52a05e5dc386b982d8f5ad
ms.contentlocale: es-es
ms.lasthandoff: 09/29/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="67f97-103">Ejecutar el formato para realizar recuentos y sumas para informes electrónicos (ER)</span><span class="sxs-lookup"><span data-stu-id="67f97-103">Run the format to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67f97-104">Los pasos siguientes explican cómo un usuario asignado al administrador del sistema o al rol de desarrollador de informes electrónicos puede configurar un formato de informe electrónico (ER) para que realice el recuento y calcule en función de los datos de la salida de texto ya generada.</span><span class="sxs-lookup"><span data-stu-id="67f97-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="67f97-105">Estos pasos se pueden llevar a cabo en la empresa DEMF.</span><span class="sxs-lookup"><span data-stu-id="67f97-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="67f97-106">Para completar estos pasos, primero debe completar los pasos del procedimiento "ER Configurar el formato para contar y sumar (Parte 3: Uso de los cálculos para crear la salida)".</span><span class="sxs-lookup"><span data-stu-id="67f97-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="67f97-107">Este procedimiento es para una función que se ha añadido en la versión 1611 de Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="67f97-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="67f97-108">Pruebe esta configuración para la generación de los informes Intrastat</span><span class="sxs-lookup"><span data-stu-id="67f97-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="67f97-109">Vaya a Administración de la organización > Espacios de trabajo > Informes electrónicos.</span><span class="sxs-lookup"><span data-stu-id="67f97-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="67f97-110">Haga clic en Configuraciones de informes.</span><span class="sxs-lookup"><span data-stu-id="67f97-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="67f97-111">En el árbol, expanda "Intrastat modelo".</span><span class="sxs-lookup"><span data-stu-id="67f97-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="67f97-112">En el árbol, expanda "Modelo de Intrastat\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="67f97-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="67f97-113">En el árbol, seleccione "Modelo de Intrastat\Intrastat (DE)\Intrastat (DE) con recuento & suma".</span><span class="sxs-lookup"><span data-stu-id="67f97-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="67f97-114">En el panel de acciones, haga clic en Configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67f97-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="67f97-115">Haga clic en Parámetros de usuario.</span><span class="sxs-lookup"><span data-stu-id="67f97-115">Click User parameters.</span></span>
8. <span data-ttu-id="67f97-116">Seleccione Sí en el campo Parámetros de ejecución.</span><span class="sxs-lookup"><span data-stu-id="67f97-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="67f97-117">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="67f97-117">Click OK.</span></span>
10. <span data-ttu-id="67f97-118">Haga clic en Editar.</span><span class="sxs-lookup"><span data-stu-id="67f97-118">Click Edit.</span></span>
11. <span data-ttu-id="67f97-119">Seleccione Sí en el campo Borrador de ejecución.</span><span class="sxs-lookup"><span data-stu-id="67f97-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="67f97-120">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="67f97-120">Click Save.</span></span>
13. <span data-ttu-id="67f97-121">Vaya a Impuestos > Configuración > Comercio exterior > Parámetros de comercio exterior.</span><span class="sxs-lookup"><span data-stu-id="67f97-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="67f97-122">Expanda la sección Informes electrónicos.</span><span class="sxs-lookup"><span data-stu-id="67f97-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="67f97-123">Seleccione la configuración "Intrastat (DE) con recuento & suma".</span><span class="sxs-lookup"><span data-stu-id="67f97-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="67f97-124">Seleccione la configuración "Intrastat (DE) con recuento & suma".</span><span class="sxs-lookup"><span data-stu-id="67f97-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="67f97-125">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="67f97-125">Click Save.</span></span>
18. <span data-ttu-id="67f97-126">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="67f97-126">Close the page.</span></span>
19. <span data-ttu-id="67f97-127">Vaya a Impuestos > Declaraciones > Comercio exterior > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="67f97-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="67f97-128">Haga clic en Salida.</span><span class="sxs-lookup"><span data-stu-id="67f97-128">Click Output.</span></span>
21. <span data-ttu-id="67f97-129">Haga clic en Informe.</span><span class="sxs-lookup"><span data-stu-id="67f97-129">Click Report.</span></span>
    * <span data-ttu-id="67f97-130">Ejecute el proceso de generación de informes de Intrastat.</span><span class="sxs-lookup"><span data-stu-id="67f97-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="67f97-131">En el campo Fecha inicial, defina la fecha en "2000-01-01".</span><span class="sxs-lookup"><span data-stu-id="67f97-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="67f97-132">Defina las fechas de inicio y fin del período de informes que incluye las existentes en las transacciones del formulario.</span><span class="sxs-lookup"><span data-stu-id="67f97-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="67f97-133">En el campo Fecha final, defina la fecha en "2022-12-31".</span><span class="sxs-lookup"><span data-stu-id="67f97-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="67f97-134">Defina las fechas de inicio y fin del período de informes que incluye las existentes en las transacciones del formulario.</span><span class="sxs-lookup"><span data-stu-id="67f97-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="67f97-135">En el campo Dirección, seleccione "Llegadas".</span><span class="sxs-lookup"><span data-stu-id="67f97-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="67f97-136">Seleccione Sí en el campo Generar archivo.</span><span class="sxs-lookup"><span data-stu-id="67f97-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="67f97-137">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="67f97-137">Click OK.</span></span>
    * <span data-ttu-id="67f97-138">Revise la salida creada con las líneas de resumen al final.</span><span class="sxs-lookup"><span data-stu-id="67f97-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="67f97-139">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="67f97-139">Click New.</span></span>
28. <span data-ttu-id="67f97-140">En la lista, marque la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="67f97-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="67f97-141">En el campo Dirección, seleccione "Distribuciones".</span><span class="sxs-lookup"><span data-stu-id="67f97-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="67f97-142">En el campo Número de artículo, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="67f97-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="67f97-143">En el campo Código Intrastat de la mercancía, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="67f97-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="67f97-144">Establezca un Peso de "10".</span><span class="sxs-lookup"><span data-stu-id="67f97-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="67f97-145">establezca un importe de Factura de "10000"</span><span class="sxs-lookup"><span data-stu-id="67f97-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="67f97-146">Establezca un Importe estadístico de "10000"</span><span class="sxs-lookup"><span data-stu-id="67f97-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="67f97-147">Haga clic en Salida.</span><span class="sxs-lookup"><span data-stu-id="67f97-147">Click Output.</span></span>
36. <span data-ttu-id="67f97-148">Haga clic en Informe.</span><span class="sxs-lookup"><span data-stu-id="67f97-148">Click Report.</span></span>
37. <span data-ttu-id="67f97-149">En el campo Dirección, seleccione "Distribuciones".</span><span class="sxs-lookup"><span data-stu-id="67f97-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="67f97-150">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="67f97-150">Click OK.</span></span>
    * <span data-ttu-id="67f97-151">Revise la salida creada con las líneas de resumen al final.</span><span class="sxs-lookup"><span data-stu-id="67f97-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="67f97-152">Observe que se ha cambiado en comparación con la primera ejecución.</span><span class="sxs-lookup"><span data-stu-id="67f97-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="67f97-153">Ejecute esta configuración en modo depuración para revisar los datos recogidos de suma & recuento</span><span class="sxs-lookup"><span data-stu-id="67f97-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="67f97-154">Vaya a Administración de la organización > Informes electrónicos > Configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67f97-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="67f97-155">En el árbol, expanda "Intrastat modelo".</span><span class="sxs-lookup"><span data-stu-id="67f97-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="67f97-156">En el árbol, expanda "Modelo de Intrastat\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="67f97-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="67f97-157">En el árbol, seleccione "Modelo de Intrastat\Intrastat (DE)\Intrastat (DE) con recuento & suma".</span><span class="sxs-lookup"><span data-stu-id="67f97-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="67f97-158">En el panel de acciones, haga clic en Configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67f97-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="67f97-159">Haga clic en Parámetros de usuario.</span><span class="sxs-lookup"><span data-stu-id="67f97-159">Click User parameters.</span></span>
7. <span data-ttu-id="67f97-160">Seleccione Sí en el campo Ejecutar en modo depuración.</span><span class="sxs-lookup"><span data-stu-id="67f97-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="67f97-161">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="67f97-161">Click OK.</span></span>
9. <span data-ttu-id="67f97-162">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="67f97-162">Close the page.</span></span>
10. <span data-ttu-id="67f97-163">Vaya a Impuestos > Declaraciones > Comercio exterior > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="67f97-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="67f97-164">Haga clic en Salida.</span><span class="sxs-lookup"><span data-stu-id="67f97-164">Click Output.</span></span>
12. <span data-ttu-id="67f97-165">Haga clic en Informe.</span><span class="sxs-lookup"><span data-stu-id="67f97-165">Click Report.</span></span>
13. <span data-ttu-id="67f97-166">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="67f97-166">Click OK.</span></span>
14. <span data-ttu-id="67f97-167">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="67f97-167">Close the page.</span></span>
15. <span data-ttu-id="67f97-168">Vaya a Administración de la organización > Informes electrónicos > Configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67f97-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="67f97-169">En el árbol, expanda "Intrastat modelo".</span><span class="sxs-lookup"><span data-stu-id="67f97-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="67f97-170">En el árbol, expanda "Modelo de Intrastat\Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="67f97-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="67f97-171">En el árbol, seleccione "Modelo de Intrastat\Intrastat (DE)\Intrastat (DE) con recuento & suma".</span><span class="sxs-lookup"><span data-stu-id="67f97-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="67f97-172">Haga clic en los registros de Depuración.</span><span class="sxs-lookup"><span data-stu-id="67f97-172">Click Debug logs.</span></span>
    * <span data-ttu-id="67f97-173">Tenga en cuenta que se ha creado un registro de depuración para el proceso de ejecución de la configuración seleccionada.</span><span class="sxs-lookup"><span data-stu-id="67f97-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="67f97-174">Haga clic en Vincular.</span><span class="sxs-lookup"><span data-stu-id="67f97-174">Click Attach.</span></span>
21. <span data-ttu-id="67f97-175">Haga clic en Abrir.</span><span class="sxs-lookup"><span data-stu-id="67f97-175">Click Open.</span></span>
    * <span data-ttu-id="67f97-176">Revise el archivo XML creado que contiene los detalles de recuento y suma obtenidos durante la ejecución de la configuración seleccionada.</span><span class="sxs-lookup"><span data-stu-id="67f97-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

