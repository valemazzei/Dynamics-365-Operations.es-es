---
title: Pedidos de cliente en Modern POS (MPOS)
description: Este tema proporciona información acerca de los pedidos de cliente en Modern POS (MPOS). Los pedidos de cliente también se conocen como pedidos especiales. El tema incluye una discusión de parámetros y flujos de transacción relacionados.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b8ea8339c2ad25ceed2415eb5ccf5e2048c612fa
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023896"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="dba56-105">Pedidos de cliente en Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="dba56-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dba56-106">Este tema proporciona información acerca de los pedidos de cliente en Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="dba56-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="dba56-107">Los pedidos de cliente también se conocen como pedidos especiales.</span><span class="sxs-lookup"><span data-stu-id="dba56-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="dba56-108">El tema incluye una discusión de parámetros y flujos de transacción relacionados.</span><span class="sxs-lookup"><span data-stu-id="dba56-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="dba56-109">En un mundo de comercio onmicanal, muchos minoristas ofrecen la opción de pedidos de cliente, o pedidos especiales, para cumplir diferentes requisitos de producto y de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="dba56-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="dba56-110">Aquí hay algunas situaciones habituales:</span><span class="sxs-lookup"><span data-stu-id="dba56-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="dba56-111">Un cliente desea que los productos se entreguen en una dirección específica en una fecha específica.</span><span class="sxs-lookup"><span data-stu-id="dba56-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="dba56-112">Un cliente desea elegir productos de una tienda o de una ubicación diferente de la tienda o de la ubicación donde el cliente compró los productos.</span><span class="sxs-lookup"><span data-stu-id="dba56-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="dba56-113">Un cliente desea que otra persona recoja los productos que el cliente compró.</span><span class="sxs-lookup"><span data-stu-id="dba56-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="dba56-114">Los minoristas también utilizan pedidos de cliente para minimizar las ventas perdidas que, de no ser así, la falta de existencias podría provocar; la mercancía se puede entregar o recoger en una hora o un lugar distintos.</span><span class="sxs-lookup"><span data-stu-id="dba56-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="dba56-115">Configurar pedidos de cliente</span><span class="sxs-lookup"><span data-stu-id="dba56-115">Set up customer orders</span></span>

<span data-ttu-id="dba56-116">A continuación se muestran algunos de los parámetros que se pueden configurar en la página **Parámetros de Commerce** para definir cómo se realizan los pedidos de cliente:</span><span class="sxs-lookup"><span data-stu-id="dba56-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="dba56-117">**Porcentaje de depósito predeterminado**: permite especificar el importe que el cliente debe pagar como depósito para que el pedido se pueda confirmar.</span><span class="sxs-lookup"><span data-stu-id="dba56-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="dba56-118">Se calcula el importe de depósito predeterminado como porcentaje del valor del pedido.</span><span class="sxs-lookup"><span data-stu-id="dba56-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="dba56-119">En función de los privilegios, un socio de la tienda puede anular el importe mediante **Anular depósito**.</span><span class="sxs-lookup"><span data-stu-id="dba56-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="dba56-120">**Porcentaje de cargo de cancelación**: si se aplica un cargo cuando un pedido de cliente se cancela, especifique el importe de dicho cargo.</span><span class="sxs-lookup"><span data-stu-id="dba56-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="dba56-121">**Código de cargo de cancelación**: si se aplica un cargo cuando un pedido de cliente se cancela, dicho cargo se reflejará mediante un código de cargo en el pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="dba56-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="dba56-122">Use este parámetro para definir el código del cargo de cancelación.</span><span class="sxs-lookup"><span data-stu-id="dba56-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="dba56-123">**Código de cargo de envío**: los minoristas pueden cargar una cuota adicional por enviar mercancía a un cliente.</span><span class="sxs-lookup"><span data-stu-id="dba56-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="dba56-124">El importe del cargo de envío se reflejará mediante un código codificado en el pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="dba56-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="dba56-125">Use este parámetro para asignar el código de cargo de envío a los cargos de envío en el pedido del cliente.</span><span class="sxs-lookup"><span data-stu-id="dba56-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="dba56-126">**Devolver los gastos de envío**: especifique si los gastos de envío que están asociados a un pedido de cliente son reembolsables.</span><span class="sxs-lookup"><span data-stu-id="dba56-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="dba56-127">**Importe máximo sin aprobación**: si los cargos de envío son reembolsables, especifique el importe máximo de las devoluciones de cargos de envío en los pedidos de devolución.</span><span class="sxs-lookup"><span data-stu-id="dba56-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="dba56-128">Si se supera este importe, la anulación de administrador se requiere para continuar con la devolución.</span><span class="sxs-lookup"><span data-stu-id="dba56-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="dba56-129">Para incluir los siguientes escenarios, una devolución de cargos de envío puede superar el importe que se pagó originalmente:</span><span class="sxs-lookup"><span data-stu-id="dba56-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="dba56-130">Los cargos se aplican en el nivel del encabezado del pedido de ventas, y cuando una cierta cantidad de una línea de productos se devuelve, la devolución máxima de cargos de envío permitida para los productos y la cantidad no se puede determinar por la forma en que funciona para todos los clientes.</span><span class="sxs-lookup"><span data-stu-id="dba56-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="dba56-131">Los cargos de envío se tienen por cada instancia de envío.</span><span class="sxs-lookup"><span data-stu-id="dba56-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="dba56-132">Si un cliente devuelve varias veces productos y la directiva del distribuidor especifica que el distribuidor se hará cargo de los cargos de devolución de envío, los cargos de devolución de envío serán más elevados que los cargos de envío reales.</span><span class="sxs-lookup"><span data-stu-id="dba56-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="dba56-133">Flujo de transacciones para pedidos de cliente</span><span class="sxs-lookup"><span data-stu-id="dba56-133">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="dba56-134">Crear un pedido de cliente en Modern POS</span><span class="sxs-lookup"><span data-stu-id="dba56-134">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="dba56-135">Agregue un cliente a la transacción.</span><span class="sxs-lookup"><span data-stu-id="dba56-135">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="dba56-136">Agregue productos al carro.</span><span class="sxs-lookup"><span data-stu-id="dba56-136">Add products to the cart.</span></span>
3. <span data-ttu-id="dba56-137">Haga clic en **Crear pedido de cliente** y después seleccione el tipo de pedido.</span><span class="sxs-lookup"><span data-stu-id="dba56-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="dba56-138">El tipo de pedido puede ser **Pedido de cliente** o **Presupuesto**.</span><span class="sxs-lookup"><span data-stu-id="dba56-138">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="dba56-139">Haga clic en **Envío seleccionado** o en **Enviar todo** para enviar los productos a una dirección de la cuenta de cliente, especifique la fecha de envío solicitada, y especifique los cargos de envío.</span><span class="sxs-lookup"><span data-stu-id="dba56-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="dba56-140">Haga clic en **Recoger la selección** o en **Recoger todo** para seleccionar los productos que se cogerán en la tienda actual o en otro almacén en una fecha específica.</span><span class="sxs-lookup"><span data-stu-id="dba56-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="dba56-141">Cobre el importe del depósito, si se requiere un depósito.</span><span class="sxs-lookup"><span data-stu-id="dba56-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="dba56-142">Edición de un pedido de cliente ya existente</span><span class="sxs-lookup"><span data-stu-id="dba56-142">Edit an existing customer order</span></span>

1. <span data-ttu-id="dba56-143">En la página principal, haga clic en **Encontrar un pedido**.</span><span class="sxs-lookup"><span data-stu-id="dba56-143">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="dba56-144">Busque y seleccione el pedido que desea editar.</span><span class="sxs-lookup"><span data-stu-id="dba56-144">Find and select the order to edit.</span></span> <span data-ttu-id="dba56-145">En la parte inferior de la página, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="dba56-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="dba56-146">Elegir pedido</span><span class="sxs-lookup"><span data-stu-id="dba56-146">Pick up an order</span></span>

1. <span data-ttu-id="dba56-147">En la página principal, haga clic en **Encontrar un pedido**.</span><span class="sxs-lookup"><span data-stu-id="dba56-147">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="dba56-148">Seleccione el pedido que desea recoger.</span><span class="sxs-lookup"><span data-stu-id="dba56-148">Select the order to pick up.</span></span> <span data-ttu-id="dba56-149">En la parte inferior de la página, haga clic en **Picking y embalaje**.</span><span class="sxs-lookup"><span data-stu-id="dba56-149">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="dba56-150">Haga clic en **Recoger**.</span><span class="sxs-lookup"><span data-stu-id="dba56-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="dba56-151">Cancelar un pedido</span><span class="sxs-lookup"><span data-stu-id="dba56-151">Cancel an order</span></span>

1. <span data-ttu-id="dba56-152">En la página principal, haga clic en **Encontrar un pedido**.</span><span class="sxs-lookup"><span data-stu-id="dba56-152">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="dba56-153">Seleccione el pedido que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="dba56-153">Select the order to cancel.</span></span> <span data-ttu-id="dba56-154">En la parte inferior de la página, haga clic en **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="dba56-154">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="dba56-155">Crear un pedido de devolución</span><span class="sxs-lookup"><span data-stu-id="dba56-155">Create a return order</span></span>

1. <span data-ttu-id="dba56-156">En la página principal, haga clic en **Encontrar un pedido**.</span><span class="sxs-lookup"><span data-stu-id="dba56-156">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="dba56-157">Seleccione el pedido que se ha de devolver, seleccione la factura del pedido y seleccione la línea de productos para que la mercancía vuelva.</span><span class="sxs-lookup"><span data-stu-id="dba56-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="dba56-158">En la parte inferior de la página, haga clic en **Pedido de devolución**.</span><span class="sxs-lookup"><span data-stu-id="dba56-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="dba56-159">Flujo de transacciones asíncrono para pedidos de cliente</span><span class="sxs-lookup"><span data-stu-id="dba56-159">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="dba56-160">Los pedidos de cliente se pueden crear en el cliente de punto de venta (PDV) en modo sincrónico o modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="dba56-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="dba56-161">Habilite los pedidos de cliente que se crearán en modo asincrónico</span><span class="sxs-lookup"><span data-stu-id="dba56-161">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="dba56-162">Haga clic en **Retail y Commerce** &gt; **Configuración de canal** &gt; **Configuración de PDV** &gt; **Perfil de PDV** &gt; **Perfiles de funcionalidad**.</span><span class="sxs-lookup"><span data-stu-id="dba56-162">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="dba56-163">En la ficha desplegable **General**, establezca la opción **Crear pedido de cliente en modo asincrónico** en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="dba56-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="dba56-164">Cuando la opción **Crear pedido de cliente en modo asincrónico** está establecido en **Sí**, los pedidos de cliente se crean siempre en modo asincrónico, incluso si Retail Transaction Service (RTS) está disponible.</span><span class="sxs-lookup"><span data-stu-id="dba56-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="dba56-165">Si establece esta opción en **No**, los pedidos de cliente siempre se crean en modo sincrónico mediante RTS.</span><span class="sxs-lookup"><span data-stu-id="dba56-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="dba56-166">Cuando los pedidos de cliente se crean en modo asincrónico, se extraen y se insertan en Commerce mediante trabajos de extracción (P).</span><span class="sxs-lookup"><span data-stu-id="dba56-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="dba56-167">Los pedidos de ventas correspondientes se crean cuando **Sincronizar pedidos** se ejecuta manualmente o mediante un proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="dba56-167">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dba56-168">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="dba56-168">Additional resources</span></span>

[<span data-ttu-id="dba56-169">Pedidos de cliente híbridos</span><span class="sxs-lookup"><span data-stu-id="dba56-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)