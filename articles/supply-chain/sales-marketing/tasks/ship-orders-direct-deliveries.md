--- 
title: Enviar pedidos como entregas directas
description: "En este procedimiento se demuestra cómo crear una entrega directa para un pedido de ventas."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f674de4877dd2d6e6f1ff02f16a68cb4805d9864
ms.contentlocale: es-es
ms.lasthandoff: 09/29/2017

---
# <a name="ship-orders-as-direct-deliveries"></a><span data-ttu-id="a73d5-103">Enviar pedidos como entregas directas</span><span class="sxs-lookup"><span data-stu-id="a73d5-103">Ship orders as direct deliveries</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a73d5-104">En este procedimiento se demuestra cómo crear una entrega directa para un pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="a73d5-104">This procedure demonstrates how to create a direct delivery for a sales order.</span></span> <span data-ttu-id="a73d5-105">La entrega directa se usa si desea enviar mercancías al cliente directamente desde el proveedor, en lugar de enviarlas a su propio almacén primero.</span><span class="sxs-lookup"><span data-stu-id="a73d5-105">You use direct delivery when you want to ship goods to the customer directly from your vendor, instead of shipping them to your own warehouse first.</span></span> <span data-ttu-id="a73d5-106">Puede ejecutar este procedimiento con los datos de la empresa de demostración USMF o utilizar sus propios datos.</span><span class="sxs-lookup"><span data-stu-id="a73d5-106">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a73d5-107">Para finalizar correctamente la segunda subtarea "Crear entregas directas desde el área de trabajo", asegúrese de que el artículo que elige en el pedido de ventas tiene un proveedor predeterminado especificado en la ficha desplegable Compra del productos maestro emitido.</span><span class="sxs-lookup"><span data-stu-id="a73d5-107">To successfully complete the second sub-task "Create direct deliveries from the workbench", make sure that the item that you choose on the sales order has a default Vendor specified on the Purchase FastTab of the Released product master.</span></span>


## <a name="set-an-individual-order-for-direct-delivery"></a><span data-ttu-id="a73d5-108">Definir un pedido individual para entrega directa</span><span class="sxs-lookup"><span data-stu-id="a73d5-108">Set an individual order for direct delivery</span></span>
1. <span data-ttu-id="a73d5-109">Vaya a Todos los pedidos de ventas.</span><span class="sxs-lookup"><span data-stu-id="a73d5-109">Go to All sales orders.</span></span>
2. <span data-ttu-id="a73d5-110">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="a73d5-110">Click New.</span></span>
3. <span data-ttu-id="a73d5-111">En el campo Cuenta de cliente, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="a73d5-111">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="a73d5-112">Si está usando USMF, puede seleccionar la cuenta US-001.</span><span class="sxs-lookup"><span data-stu-id="a73d5-112">If you’re using USMF, you can select account US-001.</span></span>  
4. <span data-ttu-id="a73d5-113">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="a73d5-113">Click OK.</span></span>
5. <span data-ttu-id="a73d5-114">En el campo Número de artículo, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="a73d5-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a73d5-115">Si está usando USMF, puede seleccionar el artículo T0020.</span><span class="sxs-lookup"><span data-stu-id="a73d5-115">If you’re using USMF, you can select item T0020.</span></span>  
6. <span data-ttu-id="a73d5-116">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="a73d5-116">Click Save.</span></span>
7. <span data-ttu-id="a73d5-117">En el panel de acciones, haga clic en Pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="a73d5-117">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="a73d5-118">Haga clic en Entrega directa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-118">Click Direct delivery.</span></span>
    * <span data-ttu-id="a73d5-119">La página Crear entrega muestra todas las líneas de pedidos de ventas abiertas según se copian del pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="a73d5-119">The Create delivery page lists all the open sales order lines as copied from the sales order.</span></span> <span data-ttu-id="a73d5-120">Puede revisar los detalles del pedido y, si es necesario, modificar los detalles como condiciones de precios y cantidad de compra antes de crear la entrega directa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-120">You can review the order details, and if required, you can modify details such purchase quantity and pricing terms before you create the direct delivery.</span></span>  
9. <span data-ttu-id="a73d5-121">Seleccione Sí en el campo Incluir todos.</span><span class="sxs-lookup"><span data-stu-id="a73d5-121">Select Yes in the Include all field.</span></span>
    * <span data-ttu-id="a73d5-122">Si desea generar una entrega directa solo para un subconjunto de las líneas de pedidos de ventas, selecciónelas de manera individual.</span><span class="sxs-lookup"><span data-stu-id="a73d5-122">If you want to generate a direct delivery for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="a73d5-123">El campo Cuenta de proveedor puede o no rellenarse con un número de proveedor.</span><span class="sxs-lookup"><span data-stu-id="a73d5-123">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="a73d5-124">Si el proveedor predeterminado está configurado para el producto (en la cobertura de artículo asociada), este proveedor se copiará en la línea.</span><span class="sxs-lookup"><span data-stu-id="a73d5-124">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied to the line.</span></span> <span data-ttu-id="a73d5-125">De lo contrario, debe especificar un proveedor manualmente.</span><span class="sxs-lookup"><span data-stu-id="a73d5-125">Otherwise, you must enter a vendor manually.</span></span> <span data-ttu-id="a73d5-126">En este ejemplo, seleccionaremos un nuevo proveedor en el siguiente paso, incluso si ya hay uno rellenado.</span><span class="sxs-lookup"><span data-stu-id="a73d5-126">In this example, we’ll select a new vendor in the next step, even if one is already populated.</span></span>   
10. <span data-ttu-id="a73d5-127">En el campo Cuenta de proveedor, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="a73d5-127">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="a73d5-128">Si está usando USMF, puede seleccionar la cuenta 1001.</span><span class="sxs-lookup"><span data-stu-id="a73d5-128">If you’re using USMF, you can select account 1001.</span></span>  
11. <span data-ttu-id="a73d5-129">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="a73d5-129">Click OK.</span></span>
    * <span data-ttu-id="a73d5-130">El mensaje informa de que se ha creado el pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="a73d5-130">The message informs you that the purchase order has now been created.</span></span>   
12. <span data-ttu-id="a73d5-131">Expanda la sección Detalles de línea.</span><span class="sxs-lookup"><span data-stu-id="a73d5-131">Expand the Line details section.</span></span>
13. <span data-ttu-id="a73d5-132">Haga clic en la pestaña Entrega.</span><span class="sxs-lookup"><span data-stu-id="a73d5-132">Click the Delivery tab.</span></span>
    * <span data-ttu-id="a73d5-133">El campo Entrega directa está establecido ahora en Sí.</span><span class="sxs-lookup"><span data-stu-id="a73d5-133">The Direct delivery field is now set to Yes.</span></span>  
    * <span data-ttu-id="a73d5-134">El estado Entrega directa muestra el pedido de compra creado.</span><span class="sxs-lookup"><span data-stu-id="a73d5-134">The Direct delivery status shows the Purchase order created.</span></span>   
14. <span data-ttu-id="a73d5-135">En el panel de acciones, haga clic en General.</span><span class="sxs-lookup"><span data-stu-id="a73d5-135">On the Action Pane, click General.</span></span>
15. <span data-ttu-id="a73d5-136">Haga clic en Pedidos relacionados.</span><span class="sxs-lookup"><span data-stu-id="a73d5-136">Click Related orders.</span></span>
16. <span data-ttu-id="a73d5-137">Haga clic para seguir el vínculo en el campo Pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="a73d5-137">Click to follow the link in the Purchase order field.</span></span>
17. <span data-ttu-id="a73d5-138">Expanda la sección Detalles de línea.</span><span class="sxs-lookup"><span data-stu-id="a73d5-138">Expand the Line details section.</span></span>
18. <span data-ttu-id="a73d5-139">Haga clic en la ficha Dirección.</span><span class="sxs-lookup"><span data-stu-id="a73d5-139">Click the Address tab.</span></span>
    * <span data-ttu-id="a73d5-140">Tenga en cuenta que la dirección de entrega para esta línea de pedido de compra es la dirección de entrega del cliente y la no la dirección de su empresa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-140">Note that the delivery address for this purchase order line is the customer's delivery address and not your company's address.</span></span>  
    * <span data-ttu-id="a73d5-141">Si se modifica la dirección de entrega en la línea del pedido de ventas o la línea de pedido de ventas de origen, se actualizará automáticamente la dirección en la línea del pedido correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a73d5-141">If you change the delivery address on either the purchase order line or the originating sales order line, the address on the corresponding order line will be automatically updated.</span></span>  
19. <span data-ttu-id="a73d5-142">Haga clic en la pestaña Entrega.</span><span class="sxs-lookup"><span data-stu-id="a73d5-142">Click the Delivery tab.</span></span>
    * <span data-ttu-id="a73d5-143">Como la línea de pedido de ventas, el tipo asociado de la línea de pedido de compra asociado también se establece en Entrega directa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-143">Like the sales order line, the associated purchase order line type is also set to Direct delivery.</span></span>  
    * <span data-ttu-id="a73d5-144">La Fecha de entrega y la Fecha de entrega confirmada de la línea del pedido de compra se establecen en la Fecha de recepción solicitada y la Fecha de recepción confirmada de la línea de pedido de ventas de origen respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a73d5-144">The purchase order line's Delivery  date and the Confirmed delivery date are set to the Requested receipt date and Confirmed receipt date of the originating sales order line respectively.</span></span>   
    * <span data-ttu-id="a73d5-145">Si actualiza cualquiera de estas fechas en la línea de compra o la línea de ventas, las fechas del pedido correspondiente se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a73d5-145">If you update any of these dates on either the purchase line or the sales line, the dates on the corresponding order will be automatically updated.</span></span>     
    * <span data-ttu-id="a73d5-146">El pedido de compra que se establece para entregar mercancías directamente al cliente está vinculado al pedido de ventas de origen mediante una asociación especial.</span><span class="sxs-lookup"><span data-stu-id="a73d5-146">The purchase order that is set to deliver goods directly the customer is linked to the originating sales order by means of a special association.</span></span> <span data-ttu-id="a73d5-147">Esta asociación impone la regla de que la actualización del albarán del pedido de ventas no se puede realizar desde el propio pedido de ventas y se debe realizar mediante el pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="a73d5-147">This association imposes the rule that the packing slip update of the sales order can't be done from the sales order itself and must be done by using the purchase order.</span></span> <span data-ttu-id="a73d5-148">Sin embargo, la facturación del cliente se debe llevar a cabo desde el pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="a73d5-148">However, customer invoicing must be carried out from the sales order.</span></span>  
20. <span data-ttu-id="a73d5-149">En el panel de acciones, haga clic en Compra.</span><span class="sxs-lookup"><span data-stu-id="a73d5-149">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="a73d5-150">Haga clic en Confirmación.</span><span class="sxs-lookup"><span data-stu-id="a73d5-150">Click Confirmation.</span></span>
22. <span data-ttu-id="a73d5-151">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="a73d5-151">Click OK.</span></span>
23. <span data-ttu-id="a73d5-152">En el panel de acciones, haga clic en Recibir.</span><span class="sxs-lookup"><span data-stu-id="a73d5-152">On the Action Pane, click Receive.</span></span>
24. <span data-ttu-id="a73d5-153">Haga clic en Recepción de producto.</span><span class="sxs-lookup"><span data-stu-id="a73d5-153">Click Product receipt.</span></span>
25. <span data-ttu-id="a73d5-154">En el campo Recepción de producto, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="a73d5-154">In the Product receipt field, type a value.</span></span>
26. <span data-ttu-id="a73d5-155">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="a73d5-155">Click OK.</span></span>
27. <span data-ttu-id="a73d5-156">En el panel de acciones, haga clic en General.</span><span class="sxs-lookup"><span data-stu-id="a73d5-156">On the Action Pane, click General.</span></span>
28. <span data-ttu-id="a73d5-157">Haga clic en Pedidos relacionados.</span><span class="sxs-lookup"><span data-stu-id="a73d5-157">Click Related orders.</span></span>
29. <span data-ttu-id="a73d5-158">En la lista, marque la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="a73d5-158">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a73d5-159">Después de que el pedido de compra se haya actualizado como recibido, es decir, después de que el proveedor haya enviado las mercancías a la dirección del cliente, el estado del pedido de ventas de origen se actualiza automáticamente a Entregado.</span><span class="sxs-lookup"><span data-stu-id="a73d5-159">After the purchase order has been updated as received, or in other words, after the vendor has shipped the goods to your customer's address, the status of the originating sales order is automatically updated to Delivered.</span></span>  
    * <span data-ttu-id="a73d5-160">El pedido de ventas se puede facturar ahora.</span><span class="sxs-lookup"><span data-stu-id="a73d5-160">The sales order can now be invoiced.</span></span>    
30. <span data-ttu-id="a73d5-161">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="a73d5-161">Click OK.</span></span>
31. <span data-ttu-id="a73d5-162">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="a73d5-162">Close the page.</span></span>
32. <span data-ttu-id="a73d5-163">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="a73d5-163">Click OK.</span></span>

## <a name="create-direct-deliveries-from-the-workbench"></a><span data-ttu-id="a73d5-164">Crear entregas directas desde el área de trabajo</span><span class="sxs-lookup"><span data-stu-id="a73d5-164">Create direct deliveries from the workbench</span></span>
1. <span data-ttu-id="a73d5-165">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="a73d5-165">Close the page.</span></span>
2. <span data-ttu-id="a73d5-166">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="a73d5-166">Close the page.</span></span>
3. <span data-ttu-id="a73d5-167">Vaya a Todos los pedidos de ventas.</span><span class="sxs-lookup"><span data-stu-id="a73d5-167">Go to All sales orders.</span></span>
4. <span data-ttu-id="a73d5-168">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="a73d5-168">Click New.</span></span>
5. <span data-ttu-id="a73d5-169">En el campo Cuenta de cliente, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="a73d5-169">In the Customer account field, enter or select a value.</span></span>
6. <span data-ttu-id="a73d5-170">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="a73d5-170">Click OK.</span></span>
7. <span data-ttu-id="a73d5-171">En el campo Número de artículo, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="a73d5-171">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="a73d5-172">Expanda la sección Detalles de línea.</span><span class="sxs-lookup"><span data-stu-id="a73d5-172">Expand the Line details section.</span></span>
9. <span data-ttu-id="a73d5-173">Haga clic en la pestaña Entrega.</span><span class="sxs-lookup"><span data-stu-id="a73d5-173">Click the Delivery tab.</span></span>
    * <span data-ttu-id="a73d5-174">En lugar de crear una entrega directa como parte del procesamiento de pedidos de ventas en el procedimiento anterior, puede elegir entregar esta tarea a un profesional de compras.</span><span class="sxs-lookup"><span data-stu-id="a73d5-174">Instead of creating a direct delivery as part of the sales order processing as in the previous procedure, you can choose to hand over this task to a purchasing professional.</span></span> <span data-ttu-id="a73d5-175">Para incluir la línea de pedido de ventas en el proceso de control de entregas directas, debe marcar la línea para entrega directa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-175">To include the sales order line in the direct delivery handling process, you must mark the line for direct delivery.</span></span>  
10. <span data-ttu-id="a73d5-176">Seleccione Sí en el campo Entrega directa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-176">Select Yes in the Direct delivery field.</span></span>
    *   <span data-ttu-id="a73d5-177">Si el artículo ya se ha configurado para entrega directa de forma predeterminada, el campo se establecerá automáticamente a Sí en la entrada de la línea de pedido.</span><span class="sxs-lookup"><span data-stu-id="a73d5-177">If the item has already been set up for direct delivery by default, the field will automatically be set to Yes at the order line entry.</span></span> <span data-ttu-id="a73d5-178">Puede configurar un artículo para entrega directa en el maestro del Producto emitido estableciendo la opción Entrega directa en Sí y seleccionando un almacén de entrega directa predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a73d5-178">You can set up an item for direct delivery on the Released product's master by setting the Direct delivery option to Yes and selecting a default Direct delivery warehouse.</span></span>  
    * <span data-ttu-id="a73d5-179">Dado que el pedido de compra no se ha creado todavía, el estado de la entrega directa se establece en Realizar entrega directa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-179">Because the purchase order has not yet been created, the Direct delivery status is set to To be direct delivered.</span></span>   
11. <span data-ttu-id="a73d5-180">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="a73d5-180">Close the page.</span></span>
12. <span data-ttu-id="a73d5-181">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="a73d5-181">Close the page.</span></span>
13. <span data-ttu-id="a73d5-182">Vaya a Entrega directa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-182">Go to Direct delivery.</span></span>
    * <span data-ttu-id="a73d5-183">La página Entrega directa actúa como área de trabajo que proporciona al agente de compras una visión general de todas las líneas de pedidos de ventas que se procesarán por entrega directa y le permite crear los pedidos de compra respectivos.</span><span class="sxs-lookup"><span data-stu-id="a73d5-183">The Direct delivery page acts as a workbench that provides the purchasing agent with an overview of all the sales order lines that are to be direct delivered and it allows them to create the respective purchase orders.</span></span> <span data-ttu-id="a73d5-184">Además, puede ver los pedidos abiertos de entrega directa y los pedidos confirmados en las fichas Confirmación y Entrega.</span><span class="sxs-lookup"><span data-stu-id="a73d5-184">In addition, they can view the open direct delivery orders and the confirmed orders on the Confirmation and Delivery tabs.</span></span>   
14. <span data-ttu-id="a73d5-185">Haga clic en Crear entrega directa.</span><span class="sxs-lookup"><span data-stu-id="a73d5-185">Click Create direct delivery.</span></span>
15. <span data-ttu-id="a73d5-186">Haga clic en la ficha Confirmación.</span><span class="sxs-lookup"><span data-stu-id="a73d5-186">Click the Confirmation tab.</span></span>
    * <span data-ttu-id="a73d5-187">Después de crear un pedido de entrega directa, se desplazó automáticamente a la ficha de confirmación. Puede elegir confirmar el pedido directamente desde esta página.</span><span class="sxs-lookup"><span data-stu-id="a73d5-187">After you have created a direct delivery order, it automatically moved to the Confirmation tab. You can choose to confirm the order directly from this page.</span></span> <span data-ttu-id="a73d5-188">Cuando se confirme la compra, se moverá automáticamente a la ficha Entrega, desde la que puede registrar su recepción.</span><span class="sxs-lookup"><span data-stu-id="a73d5-188">When the purchase is confirmed, it will automatically move to the Delivery tab, from which you can registered its receipt.</span></span>  

