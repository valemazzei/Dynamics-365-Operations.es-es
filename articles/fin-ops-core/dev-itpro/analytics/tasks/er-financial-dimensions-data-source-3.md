---
title: 'ER Usar dimensiones financieras como origen de datos (Parte 3: Diseño del informe)'
description: En los pasos siguientes se explica cómo un usuario asignado al rol de administrador del sistema o desarrollador de informes electrónicos puede configurar un modelo de informes electrónicos (ER) para que use las dimensiones financieras como origen de datos de informes ER.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77f1f2d6390a1d99b22d6eab9f0cae30f9760cc8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550588"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="c0b93-103">ER Usar dimensiones financieras como origen de datos (Parte 3: Diseño del informe)</span><span class="sxs-lookup"><span data-stu-id="c0b93-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0b93-104">En los pasos siguientes se explica cómo un usuario asignado al rol de administrador del sistema o desarrollador de informes electrónicos puede configurar un modelo de informes electrónicos (ER) para que use las dimensiones financieras como origen de datos de informes ER.</span><span class="sxs-lookup"><span data-stu-id="c0b93-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="c0b93-105">Estos pasos se pueden llevar a cabo en cualquier empresa.</span><span class="sxs-lookup"><span data-stu-id="c0b93-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c0b93-106">Para completar estos pasos, primero debe completar los pasos del procedimiento "ER Usar dimensiones financieras como origen de datos (Parte 2: Asignación de modelo)".</span><span class="sxs-lookup"><span data-stu-id="c0b93-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="c0b93-107">Diseñar un informe para mostrar las dimensiones financieras</span><span class="sxs-lookup"><span data-stu-id="c0b93-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="c0b93-108">Vaya a Administración de la organización > Informes electrónicos > Configuraciones.</span><span class="sxs-lookup"><span data-stu-id="c0b93-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c0b93-109">En el árbol, seleccione "Modelo de ejemplo de las dimensiones financieras".</span><span class="sxs-lookup"><span data-stu-id="c0b93-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c0b93-110">Haga clic en Crear configuración para abrir el cuadro de diálogo desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="c0b93-111">En el campo Nuevo, especifique "Formato basado en modelo de datos Modelo de ejemplo de las dimensiones financieras".</span><span class="sxs-lookup"><span data-stu-id="c0b93-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="c0b93-112">Usar el modelo que se ha creado por adelantado como origen de datos para su nuevo informe.</span><span class="sxs-lookup"><span data-stu-id="c0b93-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="c0b93-113">En el campo Nombre, escriba "Informe del diario contable".</span><span class="sxs-lookup"><span data-stu-id="c0b93-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="c0b93-114">En el campo Definición del modelo de datos, seleccione Entrada.</span><span class="sxs-lookup"><span data-stu-id="c0b93-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="c0b93-115">Haga clic en Crear configuración.</span><span class="sxs-lookup"><span data-stu-id="c0b93-115">Click Create configuration.</span></span>
8. <span data-ttu-id="c0b93-116">Haga clic en Diseñador.</span><span class="sxs-lookup"><span data-stu-id="c0b93-116">Click Designer.</span></span>
9. <span data-ttu-id="c0b93-117">Haga clic en Agregar raíz para abrir el cuadro de diálogo desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="c0b93-118">En el árbol, seleccione XML\Elemento.</span><span class="sxs-lookup"><span data-stu-id="c0b93-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="c0b93-119">Escriba "Raíz" en el campo Nombre.</span><span class="sxs-lookup"><span data-stu-id="c0b93-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="c0b93-120">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-120">Click OK.</span></span>
13. <span data-ttu-id="c0b93-121">Haga clic en Agregar para abrir el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="c0b93-122">En el árbol, seleccione XML\Atributo.</span><span class="sxs-lookup"><span data-stu-id="c0b93-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="c0b93-123">Escriba "Empresa" en el campo Nombre.</span><span class="sxs-lookup"><span data-stu-id="c0b93-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="c0b93-124">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-124">Click OK.</span></span>
17. <span data-ttu-id="c0b93-125">Haga clic en Agregar para abrir el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="c0b93-126">En el árbol, seleccione XML\Elemento.</span><span class="sxs-lookup"><span data-stu-id="c0b93-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="c0b93-127">En el campo Nombre, escriba "Diario".</span><span class="sxs-lookup"><span data-stu-id="c0b93-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="c0b93-128">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-128">Click OK.</span></span>
21. <span data-ttu-id="c0b93-129">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="c0b93-130">Haga clic en Agregar para abrir el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="c0b93-131">En el árbol, seleccione XML\Atributo.</span><span class="sxs-lookup"><span data-stu-id="c0b93-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="c0b93-132">En el campo Nombre, escriba "Lote".</span><span class="sxs-lookup"><span data-stu-id="c0b93-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="c0b93-133">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-133">Click OK.</span></span>
26. <span data-ttu-id="c0b93-134">Haga clic en Agregar para abrir el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="c0b93-135">En el árbol, seleccione XML\Elemento.</span><span class="sxs-lookup"><span data-stu-id="c0b93-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="c0b93-136">En el campo Nombre, escriba "Transacción".</span><span class="sxs-lookup"><span data-stu-id="c0b93-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="c0b93-137">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-137">Click OK.</span></span>
30. <span data-ttu-id="c0b93-138">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="c0b93-139">Haga clic en Agregar para abrir el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="c0b93-140">En el árbol, seleccione XML\Atributo.</span><span class="sxs-lookup"><span data-stu-id="c0b93-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="c0b93-141">En el campo Nombre, escriba "Asiento".</span><span class="sxs-lookup"><span data-stu-id="c0b93-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="c0b93-142">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-142">Click OK.</span></span>
35. <span data-ttu-id="c0b93-143">Haga clic en Agregar atributos.</span><span class="sxs-lookup"><span data-stu-id="c0b93-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="c0b93-144">En el campo Nombre, escriba "Fecha".</span><span class="sxs-lookup"><span data-stu-id="c0b93-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="c0b93-145">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-145">Click OK.</span></span>
38. <span data-ttu-id="c0b93-146">Haga clic en Agregar atributos.</span><span class="sxs-lookup"><span data-stu-id="c0b93-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="c0b93-147">En el campo Nombre, escriba "Divisa".</span><span class="sxs-lookup"><span data-stu-id="c0b93-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="c0b93-148">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-148">Click OK.</span></span>
41. <span data-ttu-id="c0b93-149">Haga clic en Agregar atributos.</span><span class="sxs-lookup"><span data-stu-id="c0b93-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="c0b93-150">En el campo Nombre, escriba "Dt".</span><span class="sxs-lookup"><span data-stu-id="c0b93-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="c0b93-151">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-151">Click OK.</span></span>
44. <span data-ttu-id="c0b93-152">Haga clic en Agregar atributos.</span><span class="sxs-lookup"><span data-stu-id="c0b93-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="c0b93-153">En el campo Nombre, escriba "Ct".</span><span class="sxs-lookup"><span data-stu-id="c0b93-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="c0b93-154">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-154">Click OK.</span></span>
47. <span data-ttu-id="c0b93-155">Haga clic en Agregar para abrir el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="c0b93-156">En el árbol, seleccione XML\Elemento.</span><span class="sxs-lookup"><span data-stu-id="c0b93-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="c0b93-157">En el campo Nombre, escriba "Dimensiones".</span><span class="sxs-lookup"><span data-stu-id="c0b93-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="c0b93-158">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-158">Click OK.</span></span>
51. <span data-ttu-id="c0b93-159">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Dimensiones: Elemento XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="c0b93-160">Haga clic en Agregar para abrir el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="c0b93-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="c0b93-161">En el árbol, seleccione XML\Atributo.</span><span class="sxs-lookup"><span data-stu-id="c0b93-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="c0b93-162">En el campo Nombre, escriba "Código".</span><span class="sxs-lookup"><span data-stu-id="c0b93-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="c0b93-163">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-163">Click OK.</span></span>
56. <span data-ttu-id="c0b93-164">Haga clic en Agregar atributos.</span><span class="sxs-lookup"><span data-stu-id="c0b93-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="c0b93-165">En el campo Nombre, escriba "Valor".</span><span class="sxs-lookup"><span data-stu-id="c0b93-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="c0b93-166">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-166">Click OK.</span></span>
59. <span data-ttu-id="c0b93-167">Haga clic en Agregar atributos.</span><span class="sxs-lookup"><span data-stu-id="c0b93-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="c0b93-168">En el campo Nombre, escriba "Desc".</span><span class="sxs-lookup"><span data-stu-id="c0b93-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="c0b93-169">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0b93-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="c0b93-170">Asignar elementos del informe a orígenes de datos</span><span class="sxs-lookup"><span data-stu-id="c0b93-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="c0b93-171">Haga clic en la ficha Asignación.</span><span class="sxs-lookup"><span data-stu-id="c0b93-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c0b93-172">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras".</span><span class="sxs-lookup"><span data-stu-id="c0b93-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c0b93-173">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c0b93-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="c0b93-174">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c0b93-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="c0b93-175">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Datos de dimensiones: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c0b93-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="c0b93-176">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Dimensiones: Elemento XML\Desc: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="c0b93-177">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Datos de dimensiones: Lista de registros\Descripción: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c0b93-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="c0b93-178">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-178">Click Bind.</span></span>
9. <span data-ttu-id="c0b93-179">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Dimensiones: Elemento XML\Valor: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="c0b93-180">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Datos de dimensiones: Lista de registros\Código: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c0b93-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="c0b93-181">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-181">Click Bind.</span></span>
12. <span data-ttu-id="c0b93-182">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Dimensiones: Elemento XML\Código: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="c0b93-183">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Datos de dimensiones: Lista de registros\Nombre: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c0b93-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="c0b93-184">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-184">Click Bind.</span></span>
15. <span data-ttu-id="c0b93-185">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Datos de dimensiones: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c0b93-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="c0b93-186">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Dimensiones: Elemento XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="c0b93-187">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-187">Click Bind.</span></span>
18. <span data-ttu-id="c0b93-188">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Ct: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="c0b93-189">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Crédito: Real".</span><span class="sxs-lookup"><span data-stu-id="c0b93-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="c0b93-190">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-190">Click Bind.</span></span>
21. <span data-ttu-id="c0b93-191">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Dt: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="c0b93-192">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Débito: Real".</span><span class="sxs-lookup"><span data-stu-id="c0b93-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="c0b93-193">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-193">Click Bind.</span></span>
24. <span data-ttu-id="c0b93-194">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Divisa: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="c0b93-195">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Divisa: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c0b93-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="c0b93-196">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-196">Click Bind.</span></span>
27. <span data-ttu-id="c0b93-197">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Fecha: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="c0b93-198">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Fecha: Fecha".</span><span class="sxs-lookup"><span data-stu-id="c0b93-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="c0b93-199">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-199">Click Bind.</span></span>
30. <span data-ttu-id="c0b93-200">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML\Asiento: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="c0b93-201">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Asiento: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c0b93-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="c0b93-202">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-202">Click Bind.</span></span>
33. <span data-ttu-id="c0b93-203">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Transacción: Elemento XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="c0b93-204">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c0b93-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="c0b93-205">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-205">Click Bind.</span></span>
36. <span data-ttu-id="c0b93-206">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML\Lote: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="c0b93-207">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Lote: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c0b93-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="c0b93-208">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-208">Click Bind.</span></span>
39. <span data-ttu-id="c0b93-209">En el árbol, seleccione "Raíz: Elemento XML\Diario: Elemento XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="c0b93-210">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c0b93-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="c0b93-211">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-211">Click Bind.</span></span>
42. <span data-ttu-id="c0b93-212">En el árbol, seleccione "Raíz: Elemento XML\Empresa: Atributo XML".</span><span class="sxs-lookup"><span data-stu-id="c0b93-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="c0b93-213">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Empresa: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c0b93-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="c0b93-214">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-214">Click Bind.</span></span>
45. <span data-ttu-id="c0b93-215">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="c0b93-215">Click Save.</span></span>
46. <span data-ttu-id="c0b93-216">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="c0b93-216">Close the page.</span></span>
