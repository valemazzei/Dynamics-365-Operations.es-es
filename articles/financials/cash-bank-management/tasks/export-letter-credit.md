--- 
title: "Exportar una carta de crédito"
description: "Este procedimiento le muestra el proceso de la carta de crédito de exportación."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0fa4b57825bcf81778d91ee01484511bb40f6bd7
ms.contentlocale: es-es
ms.lasthandoff: 09/29/2017

---
# <a name="export-a-letter-of-credit"></a><span data-ttu-id="8a22d-103">Exportar una carta de crédito</span><span class="sxs-lookup"><span data-stu-id="8a22d-103">Export a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a22d-104">Este procedimiento le muestra el proceso de la carta de crédito de exportación.</span><span class="sxs-lookup"><span data-stu-id="8a22d-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="8a22d-105">Una carta de crédito es un contrato que emite un banco, por el cual el banco garantiza el pago en nombre del comprador, siempre que se cumplan las condiciones del contrato entre el comprador y el vendedor.</span><span class="sxs-lookup"><span data-stu-id="8a22d-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="8a22d-106">Ejecute los procedimientos "Configuración de instalaciones bancarias y perfiles de contabilización" y "Carta de crédito_Crear un acuerdo de instalaciones bancarias instalaciones bancarias" antes de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="8a22d-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="8a22d-107">Se debe seleccionar la empresa de demostración USMF para ejecutar este procedimiento correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a22d-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="8a22d-108">Crear un pedido de ventas para carta de crédito de exportación</span><span class="sxs-lookup"><span data-stu-id="8a22d-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="8a22d-109">Vaya a Clientes > Pedidos > Todos los pedidos de venta.</span><span class="sxs-lookup"><span data-stu-id="8a22d-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="8a22d-110">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="8a22d-110">Click New.</span></span>
3. <span data-ttu-id="8a22d-111">En el campo Cuenta de cliente, haga clic en el botón desplegable para abrir la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8a22d-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8a22d-112">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="8a22d-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8a22d-113">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8a22d-114">Expanda o contraiga la sección General.</span><span class="sxs-lookup"><span data-stu-id="8a22d-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="8a22d-115">En el campo Sitio, haga clic en el botón desplegable para abrir la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8a22d-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8a22d-116">Permite seleccionar el sitio en el que se mantiene en existencias el artículo que se va a emitir.</span><span class="sxs-lookup"><span data-stu-id="8a22d-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="8a22d-117">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8a22d-118">En el campo Almacén, haga clic en el botón desplegable para abrir la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8a22d-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8a22d-119">Permite seleccionar el Almacén en el que se mantiene en existencias el artículo que se va a emitir.</span><span class="sxs-lookup"><span data-stu-id="8a22d-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="8a22d-120">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8a22d-121">Nota: Se debe seleccionar el campo Tipo de documento bancario con el valor Crédito documentario.</span><span class="sxs-lookup"><span data-stu-id="8a22d-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="8a22d-122">En el campo Tipo de documento bancario, seleccione "Crédito documentario".</span><span class="sxs-lookup"><span data-stu-id="8a22d-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="8a22d-123">Expanda o contraiga la sección Entrega.</span><span class="sxs-lookup"><span data-stu-id="8a22d-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="8a22d-124">Seleccione Control de fecha de entrega = Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8a22d-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="8a22d-125">En el campo Fecha de recepción solicitada, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="8a22d-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="8a22d-126">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="8a22d-126">Click OK.</span></span>
15. <span data-ttu-id="8a22d-127">En el campo Código de artículo, haga clic en el botón desplegable para abrir la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8a22d-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8a22d-128">Seleccione el artículo requerido para su emisión o venta.</span><span class="sxs-lookup"><span data-stu-id="8a22d-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="8a22d-129">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="8a22d-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="8a22d-130">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="8a22d-131">En el campo Precio unitario, escriba un número.</span><span class="sxs-lookup"><span data-stu-id="8a22d-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="8a22d-132">Expanda o contraiga la sección Detalles de línea.</span><span class="sxs-lookup"><span data-stu-id="8a22d-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="8a22d-133">Haga clic en la ficha Entrega.</span><span class="sxs-lookup"><span data-stu-id="8a22d-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="8a22d-134">En el campo Fecha de envío solicitada, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="8a22d-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="8a22d-135">En el campo Fecha de envío confirmada, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="8a22d-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="8a22d-136">En el panel de acciones, haga clic en Gestionar.</span><span class="sxs-lookup"><span data-stu-id="8a22d-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="8a22d-137">Haga clic en Crédito documentario.</span><span class="sxs-lookup"><span data-stu-id="8a22d-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="8a22d-138">En el campo Número de documento bancario, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="8a22d-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="8a22d-139">En el campo Fecha de vencimiento, especifique una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="8a22d-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="8a22d-140">Expanda o contraiga la sección Detalles del banco.</span><span class="sxs-lookup"><span data-stu-id="8a22d-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="8a22d-141">En el campo Banco emisor, haga clic en el botón desplegable para abrir la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8a22d-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="8a22d-142">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="8a22d-143">En el campo Banco avisador, haga clic en el botón desplegable para abrir la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8a22d-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="8a22d-144">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="8a22d-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="8a22d-145">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="8a22d-146">Haga clic en Obtener envíos de pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="8a22d-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="8a22d-147">Haga clic en Emitir documento bancario.</span><span class="sxs-lookup"><span data-stu-id="8a22d-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="8a22d-148">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="8a22d-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="8a22d-149">Registrar albarán</span><span class="sxs-lookup"><span data-stu-id="8a22d-149">Post Packing slip</span></span>
1. <span data-ttu-id="8a22d-150">En el panel de acciones, haga clic en Seleccionar y empaquetar.</span><span class="sxs-lookup"><span data-stu-id="8a22d-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="8a22d-151">Haga clic en Registrar albarán.</span><span class="sxs-lookup"><span data-stu-id="8a22d-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="8a22d-152">Expanda o contraiga la sección Parámetros.</span><span class="sxs-lookup"><span data-stu-id="8a22d-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="8a22d-153">En el campo Cantidad, seleccione "Todo".</span><span class="sxs-lookup"><span data-stu-id="8a22d-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="8a22d-154">Expanda o contraiga la sección Configuración.</span><span class="sxs-lookup"><span data-stu-id="8a22d-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="8a22d-155">En el campo Fecha de entrega, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="8a22d-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="8a22d-156">Seleccione el Número de envío.</span><span class="sxs-lookup"><span data-stu-id="8a22d-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="8a22d-157">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8a22d-158">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="8a22d-158">Click OK.</span></span>
10. <span data-ttu-id="8a22d-159">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="8a22d-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="8a22d-160">Registrar factura de ventas</span><span class="sxs-lookup"><span data-stu-id="8a22d-160">Post sales invoice</span></span>
1. <span data-ttu-id="8a22d-161">En el panel de acciones, haga clic en Factura.</span><span class="sxs-lookup"><span data-stu-id="8a22d-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="8a22d-162">Haga clic en Factura.</span><span class="sxs-lookup"><span data-stu-id="8a22d-162">Click Invoice.</span></span>
3. <span data-ttu-id="8a22d-163">Expanda o contraiga la sección Visión general.</span><span class="sxs-lookup"><span data-stu-id="8a22d-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="8a22d-164">Seleccione el Número de envío.</span><span class="sxs-lookup"><span data-stu-id="8a22d-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="8a22d-165">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8a22d-166">Expanda o contraiga la sección Configuración.</span><span class="sxs-lookup"><span data-stu-id="8a22d-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="8a22d-167">En el campo Fecha de la factura, especifique una fecha.</span><span class="sxs-lookup"><span data-stu-id="8a22d-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="8a22d-168">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="8a22d-168">Click OK.</span></span>
9. <span data-ttu-id="8a22d-169">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="8a22d-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="8a22d-170">Estado enviado de documento de envío</span><span class="sxs-lookup"><span data-stu-id="8a22d-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="8a22d-171">En el panel de acciones, haga clic en Gestionar.</span><span class="sxs-lookup"><span data-stu-id="8a22d-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="8a22d-172">Haga clic en Crédito documentario.</span><span class="sxs-lookup"><span data-stu-id="8a22d-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="8a22d-173">Expanda o contraiga la sección Líneas.</span><span class="sxs-lookup"><span data-stu-id="8a22d-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="8a22d-174">Nota: El campo "Documento enviado" se debe establecer en "Sí".</span><span class="sxs-lookup"><span data-stu-id="8a22d-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="8a22d-175">Comprobar Exportar crédito documentario</span><span class="sxs-lookup"><span data-stu-id="8a22d-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="8a22d-176">Vaya a Gestión de efectivo y bancos > Carta de crédito > Exportar carta de crédito e importar cobro.</span><span class="sxs-lookup"><span data-stu-id="8a22d-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="8a22d-177">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="8a22d-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8a22d-178">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8a22d-179">Compruebe que la carta de crédito de exportación tienen un estado de envío de "Facturado".</span><span class="sxs-lookup"><span data-stu-id="8a22d-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="8a22d-180">Cobros</span><span class="sxs-lookup"><span data-stu-id="8a22d-180">Customer payment</span></span>
1. <span data-ttu-id="8a22d-181">Vaya a Clientes > Pagos > Diario de pagos.</span><span class="sxs-lookup"><span data-stu-id="8a22d-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8a22d-182">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="8a22d-182">Click New.</span></span>
3. <span data-ttu-id="8a22d-183">En la lista, marque la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8a22d-184">En el campo Nombre, haga clic en el botón desplegable para abrir la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8a22d-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8a22d-185">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8a22d-186">Haga clic en Líneas.</span><span class="sxs-lookup"><span data-stu-id="8a22d-186">Click Lines.</span></span>
7. <span data-ttu-id="8a22d-187">En el campo Fecha, escriba una fecha.</span><span class="sxs-lookup"><span data-stu-id="8a22d-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="8a22d-188">En el campo Cuenta, especifique los valores deseados.</span><span class="sxs-lookup"><span data-stu-id="8a22d-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="8a22d-189">Haga clic en Liquidación.</span><span class="sxs-lookup"><span data-stu-id="8a22d-189">Click Settlement.</span></span>
10. <span data-ttu-id="8a22d-190">Active la casilla en el encabezado de Totales.</span><span class="sxs-lookup"><span data-stu-id="8a22d-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="8a22d-191">Nota: Establezca el campo Mostrar en "Carta de crédito".</span><span class="sxs-lookup"><span data-stu-id="8a22d-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="8a22d-192">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="8a22d-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8a22d-193">Active o desactive la casilla Marcar.</span><span class="sxs-lookup"><span data-stu-id="8a22d-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="8a22d-194">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="8a22d-194">Click OK.</span></span>
14. <span data-ttu-id="8a22d-195">Haga clic en la ficha Pago.</span><span class="sxs-lookup"><span data-stu-id="8a22d-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="8a22d-196">Comprobar los detalles del Número de documento bancario y Número de envío</span><span class="sxs-lookup"><span data-stu-id="8a22d-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="8a22d-197">Haga clic en Registrar.</span><span class="sxs-lookup"><span data-stu-id="8a22d-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="8a22d-198">Comprobar Exportar crédito documentario después del pago</span><span class="sxs-lookup"><span data-stu-id="8a22d-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="8a22d-199">Vaya a Gestión de efectivo y bancos > Carta de crédito > Exportar carta de crédito e importar cobro.</span><span class="sxs-lookup"><span data-stu-id="8a22d-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="8a22d-200">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="8a22d-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8a22d-201">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8a22d-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8a22d-202">Compruebe Estado de envío = Pago recibido e importe de saldo = 0,00.</span><span class="sxs-lookup"><span data-stu-id="8a22d-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

