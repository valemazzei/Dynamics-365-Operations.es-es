--- 
title: "Designar un formato para usar intervalos horizontalmente ensanchables para añadir de forma dinámica columnas en informes de Excel para informes electrónicos (ER)"
description: "En los pasos siguientes se explica cómo un usuario asignado al administrador del sistema o al rol de desarrollador de informes electrónicos, puede configurar un formato electrónico (ER) para generar informes mientras que los archivos de las hojas de cálculo de Excel (OPENXML) en los que las columnas necesarias se pueden crear de forma dinámica como intervalos horizontalmente ensanchables."
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
ms.openlocfilehash: 0cd1de95630d0f7c40c3b9948015892623a93686
ms.contentlocale: es-es
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="c4e20-103">Designar un formato para usar intervalos horizontalmente ensanchables para añadir de forma dinámica columnas en informes de Excel para informes electrónicos (ER)</span><span class="sxs-lookup"><span data-stu-id="c4e20-103">Design a format to use horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4e20-104">En los pasos siguientes se explica cómo un usuario asignado al administrador del sistema o al rol de desarrollador de informes electrónicos, puede configurar un formato electrónico (ER) para generar informes mientras que los archivos de las hojas de cálculo de Excel (OPENXML) en los que las columnas necesarias se pueden crear de forma dinámica como intervalos horizontalmente ensanchables.</span><span class="sxs-lookup"><span data-stu-id="c4e20-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="c4e20-105">Estos pasos se pueden llevar a cabo en cualquier empresa.</span><span class="sxs-lookup"><span data-stu-id="c4e20-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c4e20-106">Para completar estos pasos, primero debe completar estas tres guías de tarea:</span><span class="sxs-lookup"><span data-stu-id="c4e20-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="c4e20-107">"ER Creación y activación de un proveedor de configuraciones"</span><span class="sxs-lookup"><span data-stu-id="c4e20-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="c4e20-108">"ER Usar dimensiones financieras como origen de datos (Parte 1: Modelo de datos de diseño)"</span><span class="sxs-lookup"><span data-stu-id="c4e20-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="c4e20-109">"ER Usar dimensiones financieras como origen de datos (Parte 2: Asignación de modelo)"</span><span class="sxs-lookup"><span data-stu-id="c4e20-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="c4e20-110">También debe descargar y guardar una copia local de la plantilla con un informe de ejemplo que se encuentra aquí: http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="c4e20-110">You must also download and save a local copy of the template with a sample report found here: http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx</span></span>

<span data-ttu-id="c4e20-111">Este procedimiento es para una función que se ha añadido en la versión 1611 de Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="c4e20-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="c4e20-112">Cree una nueva configuración del informe.</span><span class="sxs-lookup"><span data-stu-id="c4e20-112">Create a new report configuration</span></span>
1. <span data-ttu-id="c4e20-113">Vaya a Administración de la organización > Informes electrónicos > Configuraciones.</span><span class="sxs-lookup"><span data-stu-id="c4e20-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c4e20-114">En el árbol, seleccione "Modelo de ejemplo de las dimensiones financieras".</span><span class="sxs-lookup"><span data-stu-id="c4e20-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c4e20-115">Haga clic en Crear configuración para abrir el cuadro de diálogo desplegable.</span><span class="sxs-lookup"><span data-stu-id="c4e20-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="c4e20-116">En el campo Nuevo, especifique "Formato basado en modelo de datos Modelo de ejemplo de las dimensiones financieras".</span><span class="sxs-lookup"><span data-stu-id="c4e20-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="c4e20-117">Use el modelo creado por adelantado como el origen de los datos para su nuevo informe.</span><span class="sxs-lookup"><span data-stu-id="c4e20-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="c4e20-118">En el campo Nombre, inrtoduzca "Informe de ejemplo con intervalos ensanchables horizontalmente". </span><span class="sxs-lookup"><span data-stu-id="c4e20-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="c4e20-119">Informe de ejemplo con intervalos ensanchables horizontalmente </span><span class="sxs-lookup"><span data-stu-id="c4e20-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="c4e20-120">En el campo Descripción, instroduzca “Para crear un resultado en formato Excel con columnas agregadas dinámicamente".</span><span class="sxs-lookup"><span data-stu-id="c4e20-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="c4e20-121">Para generar un resultado en formato Excel con columnas agregadas dinámicamente </span><span class="sxs-lookup"><span data-stu-id="c4e20-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="c4e20-122">En el campo Definición del modelo de datos, seleccione Entrada.</span><span class="sxs-lookup"><span data-stu-id="c4e20-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="c4e20-123">Haga clic en Crear configuración.</span><span class="sxs-lookup"><span data-stu-id="c4e20-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="c4e20-124">Diseñe el formato del informe.</span><span class="sxs-lookup"><span data-stu-id="c4e20-124">Design the report format</span></span>
1. <span data-ttu-id="c4e20-125">Haga clic en Diseñador.</span><span class="sxs-lookup"><span data-stu-id="c4e20-125">Click Designer.</span></span>
2. <span data-ttu-id="c4e20-126">Encienda el botón de alternancia “Detalles de la presentación”.</span><span class="sxs-lookup"><span data-stu-id="c4e20-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="c4e20-127">En el panel de acciones, haga clic en Importar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="c4e20-128">Haga clic en Importar desde Excel.</span><span class="sxs-lookup"><span data-stu-id="c4e20-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="c4e20-129">Haga clic en Archivos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c4e20-129">Click Attachments.</span></span>
    * <span data-ttu-id="c4e20-130">Importe la plantilla del informe.</span><span class="sxs-lookup"><span data-stu-id="c4e20-130">Import the report’s template.</span></span> <span data-ttu-id="c4e20-131">Use el archivo de Excel que haya descargado para ello.</span><span class="sxs-lookup"><span data-stu-id="c4e20-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="c4e20-132">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="c4e20-132">Click New.</span></span>
7. <span data-ttu-id="c4e20-133">Haga clic en Archivo.</span><span class="sxs-lookup"><span data-stu-id="c4e20-133">Click File.</span></span>
8. <span data-ttu-id="c4e20-134">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="c4e20-134">Close the page.</span></span>
9. <span data-ttu-id="c4e20-135">En el campo Plantilla, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="c4e20-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="c4e20-136">Seleccione la plantilla descargada.</span><span class="sxs-lookup"><span data-stu-id="c4e20-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="c4e20-137">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c4e20-137">Click OK.</span></span>
    * <span data-ttu-id="c4e20-138">Agregue un nuevo intervalo para crear dinámicamente un resultado en formato Excel con tantas columnas como haya seleccionado (en el formulario del cuadro de diálogo de usuario) para dimensiones financieras.</span><span class="sxs-lookup"><span data-stu-id="c4e20-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="c4e20-139">Cada celda para cada columna representará un nombre de una sola dimensión financiera.</span><span class="sxs-lookup"><span data-stu-id="c4e20-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="c4e20-140">Haga clic en Agregar para abrir el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="c4e20-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="c4e20-141">En el árbol, seleccione "Excel\Intervalo"...</span><span class="sxs-lookup"><span data-stu-id="c4e20-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="c4e20-142">En el campo intervalo de Excel, introduzca “DimNames”.</span><span class="sxs-lookup"><span data-stu-id="c4e20-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="c4e20-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="c4e20-143">DimNames</span></span>  
14. <span data-ttu-id="c4e20-144">En el campo de dirección Réplica, seleccione "Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="c4e20-145">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c4e20-145">Click OK.</span></span>
16. <span data-ttu-id="c4e20-146">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="c4e20-147">Haga clic en Subir.</span><span class="sxs-lookup"><span data-stu-id="c4e20-147">Click Move up.</span></span>
18. <span data-ttu-id="c4e20-148">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Cell<DimNames>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="c4e20-149">Haga clic en Cortar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-149">Click Cut.</span></span>
20. <span data-ttu-id="c4e20-150">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="c4e20-151">Haga clic en Pegar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-151">Click Paste.</span></span>
22. <span data-ttu-id="c4e20-152">En el árbol, expanda "Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="c4e20-153">En el árbol, expanda "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical".</span><span class="sxs-lookup"><span data-stu-id="c4e20-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="c4e20-154">En el árbol, expanda "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical".</span><span class="sxs-lookup"><span data-stu-id="c4e20-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="c4e20-155">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical".</span><span class="sxs-lookup"><span data-stu-id="c4e20-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="c4e20-156">Agregue un nuevo intervalo para crear dinámicamente un resultado en formato Excel con tantas columnas como haya seleccionado (en el formulario del cuadro de diálogo de usuario) para dimensiones financieras.</span><span class="sxs-lookup"><span data-stu-id="c4e20-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="c4e20-157">Cada celda para cada columna representará el valor de una sola dimensión financiera para cada transacción que se notifique.</span><span class="sxs-lookup"><span data-stu-id="c4e20-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="c4e20-158">Haga clic en Agregar Intervalo.</span><span class="sxs-lookup"><span data-stu-id="c4e20-158">Click Add Range.</span></span>
27. <span data-ttu-id="c4e20-159">En el campo de intervalo de Excel, introduzca “DimValues”.</span><span class="sxs-lookup"><span data-stu-id="c4e20-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="c4e20-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="c4e20-160">DimValues</span></span>  
28. <span data-ttu-id="c4e20-161">En el campo de dirección Réplica, seleccione "Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="c4e20-162">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="c4e20-162">Click OK.</span></span>
30. <span data-ttu-id="c4e20-163">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="c4e20-164">Haga clic en Cortar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-164">Click Cut.</span></span>
32. <span data-ttu-id="c4e20-165">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="c4e20-166">Haga clic en Pegar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-166">Click Paste.</span></span>
34. <span data-ttu-id="c4e20-167">En el árbol, expanda "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="c4e20-168">Asigne elementos de formato a orígenes de datos</span><span class="sxs-lookup"><span data-stu-id="c4e20-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="c4e20-169">Haga clic en la ficha Asignación.</span><span class="sxs-lookup"><span data-stu-id="c4e20-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c4e20-170">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras".</span><span class="sxs-lookup"><span data-stu-id="c4e20-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c4e20-171">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c4e20-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="c4e20-172">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c4e20-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="c4e20-173">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Datos de dimensiones: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c4e20-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="c4e20-174">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="c4e20-175">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Datos de dimensiones: Lista de registros\Código: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c4e20-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="c4e20-176">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-176">Click Bind.</span></span>
9. <span data-ttu-id="c4e20-177">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="c4e20-178">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Datos de dimensiones: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c4e20-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="c4e20-179">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-179">Click Bind.</span></span>
12. <span data-ttu-id="c4e20-180">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="c4e20-181">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Crédito: Real".</span><span class="sxs-lookup"><span data-stu-id="c4e20-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="c4e20-182">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-182">Click Bind.</span></span>
15. <span data-ttu-id="c4e20-183">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="c4e20-184">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Débito: Real".</span><span class="sxs-lookup"><span data-stu-id="c4e20-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="c4e20-185">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-185">Click Bind.</span></span>
18. <span data-ttu-id="c4e20-186">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="c4e20-187">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Divisa: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c4e20-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="c4e20-188">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-188">Click Bind.</span></span>
21. <span data-ttu-id="c4e20-189">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="c4e20-190">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Fecha: Fecha".</span><span class="sxs-lookup"><span data-stu-id="c4e20-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="c4e20-191">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-191">Click Bind.</span></span>
24. <span data-ttu-id="c4e20-192">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="c4e20-193">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros\Asiento: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c4e20-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="c4e20-194">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-194">Click Bind.</span></span>
27. <span data-ttu-id="c4e20-195">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="c4e20-196">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Lote: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c4e20-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="c4e20-197">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-197">Click Bind.</span></span>
30. <span data-ttu-id="c4e20-198">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical".</span><span class="sxs-lookup"><span data-stu-id="c4e20-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="c4e20-199">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Transacción: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c4e20-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="c4e20-200">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-200">Click Bind.</span></span>
33. <span data-ttu-id="c4e20-201">En el árbol, seleccione "Excel = 'SampleFinDimWsReport'\Range<JournalLine>Vertical\Cell<Batch></span><span class="sxs-lookup"><span data-stu-id="c4e20-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="c4e20-202">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros\Lote: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c4e20-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="c4e20-203">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-203">Click Bind.</span></span>
36. <span data-ttu-id="c4e20-204">En el árbol, seleccione "Excel = 'SampleFinDimWsReport'\RangeVertical\Cell<JournalLine>: Vertical</span><span class="sxs-lookup"><span data-stu-id="c4e20-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="c4e20-205">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Diario: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c4e20-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="c4e20-206">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-206">Click Bind.</span></span>
39. <span data-ttu-id="c4e20-207">En el árbol, expanda "modelo: Modelo de datos Modelo de ejemplo de dimensiones financierasl\Configuración de dimensiones: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c4e20-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="c4e20-208">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de dimensiones financieras\Configuración de dimensiones: Lista de registros\Código: Cadena'.</span><span class="sxs-lookup"><span data-stu-id="c4e20-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="c4e20-209">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range:<DimNames> Horizontal\Cell<DimNames>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="c4e20-210">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-210">Click Bind.</span></span>
43. <span data-ttu-id="c4e20-211">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de dimensiones financierasl\Configuración de dimensiones: Lista de registros".</span><span class="sxs-lookup"><span data-stu-id="c4e20-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="c4e20-212">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal".</span><span class="sxs-lookup"><span data-stu-id="c4e20-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="c4e20-213">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-213">Click Bind.</span></span>
46. <span data-ttu-id="c4e20-214">En el árbol, seleccione "Excel = "SampleFinDimWsReport"\Cell<CompanyName>".</span><span class="sxs-lookup"><span data-stu-id="c4e20-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="c4e20-215">En el árbol, seleccione "modelo: Modelo de datos Modelo de ejemplo de las dimensiones financieras\Empresa: Cadena".</span><span class="sxs-lookup"><span data-stu-id="c4e20-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="c4e20-216">Haga clic en Enlazar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-216">Click Bind.</span></span>
49. <span data-ttu-id="c4e20-217">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="c4e20-217">Click Save.</span></span>
50. <span data-ttu-id="c4e20-218">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="c4e20-218">Close the page.</span></span>

