---
title: Política de reserva de dimensión de nivel de almacén flexible
description: Este tema describe la política de reserva de inventario que permite a las empresas que venden productos con seguimiento por lotes y ejecutan su logística como operaciones habilitadas para WMS reservar lotes específicos para pedidos de clientes, a pesar de que la jerarquía de reservas asociada con los productos no permite la reserva de lotes específicos.
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c0baf96315dd9fe6bc1984d337fd1c50ae47016a
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031052"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="ec9ea-103">Política de reserva de dimensión de nivel de almacén flexible</span><span class="sxs-lookup"><span data-stu-id="ec9ea-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec9ea-104">Cuando una jerarquía de reserva de inventario de tipo "Batch-below\[ubicación\]" está asociada con productos, las empresas que venden productos con seguimiento de lotes y ejecutan su logística como operaciones habilitadas para Microsoft Dynamics 365 Warehouse Management System (WMS) no pueden reservar lotes específicos de esos productos para pedidos de clientes.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="ec9ea-105">Este tema describe la política de reserva de inventario que permite a estas empresas reservar lotes específicos, incluso cuando los productos están asociados con una jerarquía de reservas "Batch-below\[ubicación\]".</span><span class="sxs-lookup"><span data-stu-id="ec9ea-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="ec9ea-106">Jerarquía de reservas de inventario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="ec9ea-107">Esta sección resume la jerarquía de reservas de inventario existente.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="ec9ea-108">Se centra en la forma en que se manejan los artículos seguidos por lotes y seguidos en serie.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="ec9ea-109">La jerarquía de reservas de inventario dicta que, en lo que respecta a las dimensiones de almacenamiento, la orden de demanda lleva las dimensiones obligatorias de sitio, almacén y estado del inventario, mientras que la lógica de almacén es responsable de asignar una ubicación a las cantidades solicitadas y reservar la ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="ec9ea-110">En otras palabras, en las interacciones entre el pedido de demanda y las operaciones de almacén, se espera que el pedido de demanda indique de dónde debe enviarse el pedido (es decir, qué sitio y almacén).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="ec9ea-111">El almacén se basa en su lógica para encontrar la cantidad requerida en las instalaciones del almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="ec9ea-112">Sin embargo, para reflejar el modelo operativo de la empresa, las dimensiones de seguimiento (números de serie y de lote) están sujetas a una mayor flexibilidad.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="ec9ea-113">Una jerarquía de reserva de inventario puede acomodar escenarios donde se aplican las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="ec9ea-114">El negocio se basa en sus operaciones de almacén para gestionar la recolección de cantidades que tienen números de lote o de serie después de que las cantidades se hayan encontrado en el espacio de almacenamiento de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="ec9ea-115">Este modelo a menudo se conoce como *Batch-below\[ubicación\]*.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="ec9ea-116">Por lo general, se usa cuando la identificación de un lote o número de serie de un producto no es importante para los clientes que colocan la demanda en la empresa vendedora.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="ec9ea-117">Si los números de lote o de serie son parte de la especificación de pedido de un cliente y se registran en el pedido de demanda, las operaciones de almacén que encuentran las cantidades en el almacén están restringidas por los números solicitados específicos y no se les permite cambiarlos.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="ec9ea-118">Este modelo a menudo se conoce como *Batch-above\[ubicación\]*.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="ec9ea-119">En estos escenarios, el desafío es que solo se puede asignar una jerarquía de reserva de inventario a cada producto lanzado.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="ec9ea-120">Por lo tanto, para que el WMS maneje los artículos rastreados, una vez que la asignación de la jerarquía determina cuándo se debe reservar el lote o el número de serie (cuando se toma la orden de demanda o durante el trabajo de selección de almacén), este momento no se puede cambiar ad hoc.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="ec9ea-121">Reserva flexible para artículos con seguimiento por lotes</span><span class="sxs-lookup"><span data-stu-id="ec9ea-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="ec9ea-122">Escenario empresarial</span><span class="sxs-lookup"><span data-stu-id="ec9ea-122">Business scenario</span></span>

<span data-ttu-id="ec9ea-123">En este escenario, una compañía usa una estrategia de inventario donde se hace un seguimiento de los productos terminados por número de lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="ec9ea-124">Esta compañía también usa la carga de trabajo de WHS.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-124">This company also uses the WHS workload.</span></span> <span data-ttu-id="ec9ea-125">Debido a que esta carga de trabajo tiene una lógica bien equipada para planificar y ejecutar operaciones de picking y envío de almacén para artículos habilitados por lotes, la mayoría de los artículos terminados están asociados con una jerarquía de reservas de inventario "Batch-below\[ubicación\]".</span><span class="sxs-lookup"><span data-stu-id="ec9ea-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="ec9ea-126">La ventaja de este tipo de configuración operativa es que las decisiones (que son efectivamente decisiones de reserva) sobre qué lotes elegir y dónde colocarlas en el almacén se posponen hasta que comiencen las operaciones de selección del almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="ec9ea-127">No se toman cuando se realiza el pedido del cliente.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="ec9ea-128">Aunque la jerarquía de reservas "Batch-below\[ubicación\]" sirve bien a los objetivos comerciales de la compañía, muchos de los clientes establecidos de la compañía requieren el mismo lote que compraron previamente cuando reordenan productos.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="ec9ea-129">Por lo tanto, la compañía busca flexibilidad en la forma en que se manejan las reglas de reserva de lotes, de modo que, dependiendo de la demanda de los clientes por el mismo artículo, ocurran los siguientes comportamientos:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="ec9ea-130">Se puede registrar y reservar un número de lote cuando el procesador de ventas toma el pedido, y no se puede cambiar durante las operaciones de almacén ni otras demandas.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="ec9ea-131">Este comportamiento ayuda a garantizar que el número de lote que se solicitó se envíe al cliente.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="ec9ea-132">Si el número de lote no es importante para el cliente, las operaciones del almacén pueden determinar un número de lote durante el trabajo de recolección, después de que se haya realizado el registro y la reserva del pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="ec9ea-133">Permitir la reserva de un lote específico en el pedido de ventas</span><span class="sxs-lookup"><span data-stu-id="ec9ea-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="ec9ea-134">Para admitir la flexibilidad deseada en el comportamiento de reserva de lotes para artículos que están asociados con una jerarquía de reservas de inventario "Batch-below\[ubicación\]", los gerentes de inventario deben seleccionar la casilla **Permitir reserva bajo pedido** para el nivel de **Número de lote** en la página **Jerarquías de reservas de inventario**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Hacer que la jerarquía de reservas de inventario sea flexible](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="ec9ea-136">Cuando se selecciona en la jerarquía el nivel de **Número de lote**, todas las dimensiones por encima de ese nivel hasta el nivel **Ubicación** se seleccionarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="ec9ea-137">(Por defecto, todas las dimensiones por encima del nivel de **Ubicación** están preseleccionadas). Este comportamiento refleja la lógica en la que todas las dimensiones en el rango entre el número de lote y la ubicación también se reservan automáticamente después de reservar un número de lote específico en la línea de pedido.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="ec9ea-138">La casilla **Permitir reserva bajo pedido** se aplica solo a los niveles de jerarquía de reserva que están por debajo de la dimensión de ubicación del almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="ec9ea-139">**Número de lote** es el único nivel en la jerarquía que está abierto para la política de reserva flexible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="ec9ea-140">En otras palabras, no puede seleccionar la casilla **Permitir reserva bajo pedido** para el nivel **Ubicación**, **Matrícula de entidad de almacén** o **Número de serie**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="ec9ea-141">Si su jerarquía de reservas incluye la dimensión del número de serie (que siempre debe estar por debajo del nivel de **Número de lote**) y si ha activado la reserva específica de lote para el número de lote, el sistema continuará manejando las operaciones de reserva y selección de número de serie, de acuerdo con las reglas que se aplican a la política de reserva "Serial-below\[ubicación\]".</span><span class="sxs-lookup"><span data-stu-id="ec9ea-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="ec9ea-142">En cualquier momento, puede permitir una reserva específica de lote para la jerarquía de reservas "Batch-below\[ubicación\]" en su implementación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="ec9ea-143">Este cambio no afectará ninguna reserva ni el trabajo de almacén abierto que se creó antes de que ocurriera el cambio.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="ec9ea-144">Sin embargo, la casilla de verificación **Permitir reserva bajo pedido** no se puede desactivar si las transacciones de inventario de tipo de problema **Pedido reservado**, **Cantidad física reservada** o **Cantidad pedida** existen para uno o más elementos que están asociados con esa jerarquía de reservas.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="ec9ea-145">Si la jerarquía de reservas existente de un artículo no permite la especificación de lotes en el pedido, puede reasignarla a una jerarquía de reservas que sí permita la especificación de lotes, siempre que la estructura de nivel de jerarquía sea la misma en ambas jerarquías.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="ec9ea-146">Utilice la función **Cambiar jerarquía de reservas para artículos** para hacer la reasignación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="ec9ea-147">Este cambio puede ser pertinente cuando desea evitar la reserva flexible de lotes para un subconjunto de artículos rastreados por lotes, pero permitirlo para el resto de la cartera de productos.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="ec9ea-148">Independientemente de si ha seleccionado la casilla **Permitir reserva bajo pedido**, si no desea reservar un número de lote específico para el artículo en una línea de pedido, la lógica de operaciones de almacén predeterminada que es válida para una jerarquía de reservas "Batch-below\[ubicación\]" seguirá siendo aplicable.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="ec9ea-149">Reservar un número de lote específico para un pedido del cliente</span><span class="sxs-lookup"><span data-stu-id="ec9ea-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="ec9ea-150">Después de que la jerarquía de reservas de inventario "Batch-below\[ubicación\]" de un artículo con seguimiento por lotes está configurada para permitir la reserva de números de lote específicos en pedidos de venta, los procesadores de pedidos de venta pueden tomar pedidos de clientes para el mismo artículo de una de las siguientes maneras, dependiendo de la solicitud del cliente:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="ec9ea-151">**Introducir los detalles del pedido sin especificar un número de lote**: este enfoque debe usarse cuando la especificación de lote del producto no es importante para el cliente.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="ec9ea-152">Todos los procesos existentes que están asociados con el manejo de un pedido de este tipo del sistema permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="ec9ea-153">No se requieren consideraciones adicionales por parte de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="ec9ea-154">**Introducir los detalles del pedido y reservar un número de lote específico**: este enfoque debe usarse cuando el cliente solicita un lote específico.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="ec9ea-155">Por lo general, los clientes solicitarán un lote específico cuando reordenen un producto que compraron previamente.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="ec9ea-156">Este tipo de reserva específica de lote se conoce como *reserva comprometida con el pedido*.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="ec9ea-157">El siguiente conjunto de reglas es válido cuando se procesan cantidades y se confirma un número de lote para un pedido específico:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="ec9ea-158">Para permitir la reserva de un número de lote específico para un artículo bajo la política de reserva "Batch-below\[ubicación\]", el sistema debe reservar todas las dimensiones a través de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="ec9ea-159">Este rango generalmente incluye la dimensión de la matrícula de entidad de almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="ec9ea-160">Las directivas de ubicación no se utilizan cuando el trabajo de selección se crea para una línea de ventas que utiliza la reserva de lotes confirmada por pedido.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="ec9ea-161">Durante el procesamiento del trabajo en el almacén para lotes confirmados por pedido, ni el usuario ni el sistema pueden cambiar el número de lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="ec9ea-162">(Este procesamiento incluye el control de excepciones).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="ec9ea-163">El siguiente ejemplo muestra el flujo de extremo a extremo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="ec9ea-164">Supuesto de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec9ea-164">Example scenario</span></span>

<span data-ttu-id="ec9ea-165">Para este ejemplo, los datos de prueba deben estar instalados y debe usar los datos de la compañía de prueba **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="ec9ea-166">Configurar una jerarquía de reservas de inventario para permitir la reserva específica de lote</span><span class="sxs-lookup"><span data-stu-id="ec9ea-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="ec9ea-167">Vaya a **Gestión de almacenes** \> **Configurar** \> **Inventario \> Jerarquía de reservas**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="ec9ea-168">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-168">Select **New**.</span></span>
3. <span data-ttu-id="ec9ea-169">En el campo **Nombre**, escriba un nombre (por ejemplo, **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="ec9ea-170">En el campo **Descripción**, ingrese una descripción (por ejemplo, **Lote flexible**).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="ec9ea-171">En el campo **Seleccionado**, seleccione **Número de serie** y **Propietario**, y luego seleccione el botón de flecha izquierda para moverlos al campo **Disponible**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="ec9ea-172">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-172">Select **OK**.</span></span>
7. <span data-ttu-id="ec9ea-173">En la fila para el nivel de dimensión **Número de lote**, seleccione la casilla **Permitir reserva bajo pedido**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="ec9ea-174">Los niveles **Matrícula de entidad de almacén** y **Ubicación** se seleccionan automáticamente y no se pueden desactivar sus casillas de verificación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="ec9ea-175">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="ec9ea-176">Crear un nuevo producto liberado</span><span class="sxs-lookup"><span data-stu-id="ec9ea-176">Create a new released product</span></span>

1. <span data-ttu-id="ec9ea-177">Establezca los tres parámetros de datos maestros del producto utilizando estos valores:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="ec9ea-178">En el campo **Grupo de dimensiones de almacenamiento**, seleccione **Ware**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="ec9ea-179">En el campo **Grupo de dimensiones de seguimiento**, seleccione **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="ec9ea-180">En el campo **Jerarquía de reservas**, seleccione **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="ec9ea-181">Cree dos números de lote, como **B11** y **B22**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="ec9ea-182">Agregue cantidades de artículos al stock disponible utilizando los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="ec9ea-183">Almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-183">Warehouse</span></span> | <span data-ttu-id="ec9ea-184">Número de lote</span><span class="sxs-lookup"><span data-stu-id="ec9ea-184">Batch number</span></span> | <span data-ttu-id="ec9ea-185">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ec9ea-185">Location</span></span> | <span data-ttu-id="ec9ea-186">Matrícula de entidad de almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-186">License plate</span></span> | <span data-ttu-id="ec9ea-187">Cantidad</span><span class="sxs-lookup"><span data-stu-id="ec9ea-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="ec9ea-188">24</span><span class="sxs-lookup"><span data-stu-id="ec9ea-188">24</span></span>        | <span data-ttu-id="ec9ea-189">B11</span><span class="sxs-lookup"><span data-stu-id="ec9ea-189">B11</span></span>          | <span data-ttu-id="ec9ea-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="ec9ea-190">BULK-001</span></span> | <span data-ttu-id="ec9ea-191">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ec9ea-191">None</span></span>          | <span data-ttu-id="ec9ea-192">10</span><span class="sxs-lookup"><span data-stu-id="ec9ea-192">10</span></span>       |
    | <span data-ttu-id="ec9ea-193">24</span><span class="sxs-lookup"><span data-stu-id="ec9ea-193">24</span></span>        | <span data-ttu-id="ec9ea-194">B11</span><span class="sxs-lookup"><span data-stu-id="ec9ea-194">B11</span></span>          | <span data-ttu-id="ec9ea-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="ec9ea-195">FL-001</span></span>   | <span data-ttu-id="ec9ea-196">LP11</span><span class="sxs-lookup"><span data-stu-id="ec9ea-196">LP11</span></span>          | <span data-ttu-id="ec9ea-197">10</span><span class="sxs-lookup"><span data-stu-id="ec9ea-197">10</span></span>       |
    | <span data-ttu-id="ec9ea-198">24</span><span class="sxs-lookup"><span data-stu-id="ec9ea-198">24</span></span>        | <span data-ttu-id="ec9ea-199">B22</span><span class="sxs-lookup"><span data-stu-id="ec9ea-199">B22</span></span>          | <span data-ttu-id="ec9ea-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="ec9ea-200">FL-002</span></span>   | <span data-ttu-id="ec9ea-201">LP22</span><span class="sxs-lookup"><span data-stu-id="ec9ea-201">LP22</span></span>          | <span data-ttu-id="ec9ea-202">10</span><span class="sxs-lookup"><span data-stu-id="ec9ea-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="ec9ea-203">Introducir detalles del pedido de ventas</span><span class="sxs-lookup"><span data-stu-id="ec9ea-203">Enter sales order details</span></span>

1. <span data-ttu-id="ec9ea-204">Vaya a **Ventas y marketing** \> **Pedidos de ventas** \> **Todos los pedidos de ventas**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="ec9ea-205">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-205">Select **New**.</span></span>
3. <span data-ttu-id="ec9ea-206">En el encabezado del pedido de venta, en el campo **Cuenta de cliente**, ingrese **US-003**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="ec9ea-207">Agregue una línea para el nuevo artículo y escriba **10** como cantidad.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="ec9ea-208">Asegúrese de que el campo **Almacén** se haya definido como **24**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="ec9ea-209">En la ficha desplegable **Líneas de pedido de venta**, seleccione **Inventario** y, luego, en el grupo **Mantener**, seleccione **Reserva de lotes**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="ec9ea-210">La página **Reserva de lotes** muestra una lista de los lotes disponibles para la reserva para la línea de pedido.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="ec9ea-211">En este ejemplo, muestra una cantidad de **20** para el número de lote **B11** y una cantidad de **10** para el número de lote **B22**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="ec9ea-212">Tenga en cuenta que no se puede acceder a la página **Reserva de lotes** desde una línea si el elemento en esa línea está asociado con la jerarquía de reservas "Batch-below\[ubicación\]" a menos que esté configurado para permitir reservas específicas de lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec9ea-213">Para reservar un lote específico para un pedido de venta, debe utilizar la página **Reserva de lotes**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="ec9ea-214">Si introduce el número de lote directamente en la línea de pedido de venta, el sistema se comportará como si ingresara un valor de lote específico para un artículo que está sujeto a la política de reserva "Batch-below\[ubicación\]".</span><span class="sxs-lookup"><span data-stu-id="ec9ea-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="ec9ea-215">Cuando guarde la línea, recibirá un mensaje de advertencia.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="ec9ea-216">Si confirma que el número de lote debe especificarse directamente en la línea de pedido, la línea no será manejada por la lógica de administración de almacén regular.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="ec9ea-217">Si reserva la cantidad en la página **Reserva**, no se reservará ningún lote específico y la ejecución de las operaciones de almacén para la línea seguirá las reglas que se aplican en la política de reserva "Batch-below\[ubicación\]".</span><span class="sxs-lookup"><span data-stu-id="ec9ea-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="ec9ea-218">En general, esta página funciona y se interactúa de la misma manera que funciona y se interactúa con los elementos que tienen una jerarquía de reservas asociada del tipo "Batch-above\[ubicación\]".</span><span class="sxs-lookup"><span data-stu-id="ec9ea-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="ec9ea-219">Sin embargo, se aplican las siguientes excepciones:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="ec9ea-220">La ficha desplegable **Números de lote comprometidos con la línea de origen** muestra los números de lote que están reservados para la línea de pedido.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="ec9ea-221">Los valores del lote en la cuadrícula se mostrarán durante todo el ciclo de cumplimiento de la línea de pedido, incluidas las etapas de procesamiento del almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="ec9ea-222">Por el contrario, en la ficha desplegable **Visión general**, la reserva de línea de pedido regular (es decir, la reserva que se realiza para las dimensiones por encima del nivel **Ubicación**) se muestra en la cuadrícula hasta el punto en que se crea el trabajo de almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="ec9ea-223">La entidad de trabajo se hace cargo de la reserva de línea y la reserva de línea ya no aparece en la página.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="ec9ea-224">La ficha desplegable **Números de lote comprometidos con la línea de origen** ayuda a garantizar que el procesador de pedidos de ventas pueda ver los números de lote que se comprometieron con el pedido del cliente en cualquier momento durante su ciclo de vida, hasta la facturación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="ec9ea-225">Además de reservar un lote específico, un usuario puede seleccionar manualmente la ubicación y la placa específica del lote en lugar de permitir que el sistema las seleccione automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="ec9ea-226">Esta capacidad está relacionada con el diseño del mecanismo de reserva de lotes confirmado por pedido.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="ec9ea-227">Como se mencionó anteriormente, cuando se reserva un número de lote para un artículo bajo la política de reserva "Batch-below\[ubicación\]", el sistema debe reservar todas las dimensiones a través de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="ec9ea-228">Por lo tanto, el trabajo en el almacén tendrá las mismas dimensiones de almacenamiento que fueron reservadas por los usuarios que trabajaron con los pedidos, y puede que no siempre represente la ubicación de almacenamiento del artículo que sea conveniente, o incluso posible, para las operaciones de picking.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="ec9ea-229">Si los procesadores de pedidos conocen las restricciones del almacén, pueden querer seleccionar manualmente las ubicaciones específicas y las placas de matrícula cuando reservan un lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="ec9ea-230">En este caso, el usuario debe usar la funcionalidad de **Mostrar dimensiones** en el encabezado de la página y debe agregar la ubicación y la matrícula en la cuadrícula en la ficha desplegable **Visión general**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="ec9ea-231">En la página **Reserva de lotes**, seleccione la línea para el lote **B11** y luego seleccione **Reservar línea**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="ec9ea-232">No existe una lógica designada para asignar ubicaciones y placas durante la reserva automática.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="ec9ea-233">Puede introducir manualmente la cantidad en el campo **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="ec9ea-234">Tenga en cuenta que, en la ficha desplegable **Números de lote comprometidos con la línea de origen**, el lote **B11** se muestra como **Comprometido**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Confirmación de un número de lote específico en una línea de pedido de venta en la página de reserva de lote](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="ec9ea-236">La reserva de la cantidad en una línea de pedido de ventas se puede realizar en varios lotes.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="ec9ea-237">Del mismo modo, la reserva del mismo lote se puede realizar en múltiples ubicaciones y placas de matrícula (si las placas están habilitadas para las ubicaciones).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="ec9ea-238">La reserva de un lote específico para la cantidad en una línea de pedido de ventas también puede ser parcial.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="ec9ea-239">Por ejemplo, la cantidad total de 100 unidades se puede reservar para que un lote específico se comprometa a 20 unidades, mientras que 80 unidades se reservan en los niveles de sitio y almacén para cualquier lote disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="ec9ea-240">En este caso, el WMS se encargará de las operaciones de selección utilizando dos líneas de trabajo separadas.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="ec9ea-241">Vaya a **Gestión de información de productos** \> **Productos** \> **Productos emitidos**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="ec9ea-242">Seleccione su artículo y luego seleccione **Administrar inventario** \> **Ver** \> **Transacciones**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Reserva confirmada por pedido como un tipo de transacción de inventario](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="ec9ea-244">Revise las transacciones de inventario del artículo que están relacionadas con la reserva de línea de pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="ec9ea-245">Una transacción donde el campo **Referencia** se establece en **Pedido de venta** y el campo **Problema** se establece en **Cantidad física reservada** representa la reserva de línea de pedido para las dimensiones de inventario por encima del nivel **Ubicación**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="ec9ea-246">De acuerdo con la jerarquía de reserva de inventario del artículo, esas dimensiones son sitio, almacén y estado del inventario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="ec9ea-247">Una transacción donde el campo **Referencia** se establece en **Reserva comprometida con el pedido** y el campo **Problema** se establece en **Cantidad física reservada** representa la reserva de línea de pedido del lote específico y todas las dimensiones de inventario situadas por encima.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="ec9ea-248">De acuerdo con la jerarquía de reserva de inventario del artículo, esas dimensiones son número de lote y ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="ec9ea-249">En este ejemplo, la ubicación es **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="ec9ea-250">En el encabezado del pedido de ventas, seleccione **Almacén** \> **Acciones** \> **Liberar al almacén**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="ec9ea-251">La línea de pedido ahora se somete a oleada y se crean una carga y un trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="ec9ea-252">Revisar y procesar el trabajo de almacén que tiene números de lote confirmados por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="ec9ea-253">En la ficha desplegable **Líneas de pedido de venta**, seleccione **Almacén** \> **Detalles del trabajo**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="ec9ea-254">El trabajo que maneja la operación de picking para cantidades de lote que se comprometen con la línea de pedido de ventas tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="ec9ea-255">Para crear trabajo, el sistema usa plantillas de trabajo pero no directivas de ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="ec9ea-256">Todas las configuraciones estándar que se definen para las plantillas de trabajo, como un número máximo de líneas de selección o una unidad de medida específica, se aplicarán para determinar cuándo se debe crear un nuevo trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="ec9ea-257">Sin embargo, las reglas asociadas con las directivas de ubicación para identificar ubicaciones de selección no se tienen en cuenta, ya que la reserva confirmada por pedido ya especifica todas las dimensiones del inventario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="ec9ea-258">Esas dimensiones de inventario incluyen las dimensiones en el nivel de almacenamiento del almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="ec9ea-259">Por lo tanto, el trabajo hereda esas dimensiones sin tener que consultar las directivas de ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="ec9ea-260">El número de lote no se muestra en la línea de selección (como es el caso de la línea de trabajo que se crea para un artículo que tiene asociada una jerarquía de reservas "Batch-above\[ubicación\]"). En cambio, el número de lote "desde" y todas las demás dimensiones de almacenamiento se muestran en la transacción de inventario de trabajo de la línea de trabajo a la que se hace referencia desde las transacciones de inventario asociadas.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Transacción de inventario de almacén para el trabajo que se origina en la reserva comprometida con el pedido](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="ec9ea-262">Después de crear el trabajo, se elimina la transacción de inventario del artículo donde el campo **Referencia** se establece en **Reserva comprometida con el pedido**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="ec9ea-263">La transacción de inventario donde el campo **Referencia** se establece en **Trabajo** mantiene la reserva física en todas las dimensiones de inventario de la cantidad.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="ec9ea-264">Las operaciones de almacén pueden proceder a manejar la ejecución del trabajo de la manera habitual.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="ec9ea-265">Sin embargo, las instrucciones en el dispositivo móvil le indicarán al trabajador que elija un número de lote específico.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="ec9ea-266">En entornos de almacén donde las ubicaciones están controladas por matrículas, después de que un trabajador llega a una ubicación que almacena el mismo lote en varias placas, puede elegir cualquier placa que no esté reservada (por ejemplo, por otro pedido reserva comprometida o trabajo que se origina en una reserva de ese tipo).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="ec9ea-267">Si resulta poco práctico elegir desde la ubicación que se especifica en la línea de trabajo, los operadores del almacén pueden utilizar una de las siguientes acciones para redirigir la selección del lote específico desde una ubicación más conveniente:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="ec9ea-268">La acción estándar **Anular ubicación** en un dispositivo móvil (siempre que esté habilitada la configuración **Permitir anulación de ubicación de selección** para el trabajador del almacén).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="ec9ea-269">La acción **Cambiar ubicación** en la página **Detalles de la lista de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="ec9ea-270">En el dispositivo móvil, terminar la selección y colocar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="ec9ea-271">Ahora se selecciona la cantidad **10** del número de lote **B11** para la línea del pedido de venta y se coloca en la ubicación **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="ec9ea-272">En este punto, está listo para ser cargado en el camión y enviado a la dirección del cliente.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="ec9ea-273">Control de excepciones del trabajo de almacén que tiene números de lote confirmados por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="ec9ea-274">El trabajo de almacén para seleccionar los números de lote comprometidos con el pedido está sujeto a las mismas acciones y control de excepciones de almacén estándar que el trabajo normal.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="ec9ea-275">En general, el trabajo abierto o la línea de trabajo se pueden cancelar, se pueden interrumpir porque la ubicación de un usuario está llena, se puede seleccionar con picking corto y se puede actualizar debido a un movimiento.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="ec9ea-276">Del mismo modo, la cantidad de trabajo seleccionada que ya se ha completado se puede reducir, o bien se puede revertir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="ec9ea-277">La siguiente regla clave se aplica a todas estas acciones de manejo de excepciones: el número de lote que se reservó para el cliente nunca se puede reemplazar con un número de lote diferente, pero sus dimensiones de almacenamiento (ubicación y placa de matrícula) se pueden cambiar mediante una actualización manual por el usuario o una actualización automática por parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="ec9ea-278">La actualización automática se basa en la misma asignación aleatoria de dimensiones de almacenamiento que se aplicaba cuando un lote específico se reservaba automáticamente pero no se especificaban dimensiones de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="ec9ea-279">Supuesto de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec9ea-279">Example scenario</span></span>

<span data-ttu-id="ec9ea-280">Un ejemplo de este escenario es una situación en la que el trabajo completado anteriormente no se selecciona utilizando la función **Reducir cantidad seleccionada**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="ec9ea-281">Este ejemplo continúa el ejemplo anterior de este tema.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="ec9ea-282">Vaya a **Gestión de almacenes** \> **Cargas** \> **Cargas activas**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="ec9ea-283">Seleccione la carga que se creó en relación con el envío de su pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="ec9ea-284">En la ficha desplegable **Cargar líneas de pedido**, seleccione **Reducir cantidad seleccionada**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="ec9ea-285">En la página **Reducir cantidad seleccionada**, en el campo **Mover a la ubicación**, seleccione **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="ec9ea-286">En el campo **Mover a matrícula de entidad de almacén**, seleccione **LP33**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="ec9ea-287">En la cuadrícula, en el campo **Cantidad de inventario para anular selección**, introduzca **10**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="ec9ea-288">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-288">Select **OK**.</span></span>

<span data-ttu-id="ec9ea-289">Aquí están los resultados de la acción de anulación de selección:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="ec9ea-290">El estado del trabajo previamente cerrado se establece en **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="ec9ea-291">Se crea un nuevo trabajo de tipo **Movimiento de inventario** para la cantidad no seleccionada de **10** para el número de lote **B11**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="ec9ea-292">Este trabajo representa el movimiento de la ubicación **Baydoor** a la matrícula **LP33** en la ubicación **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="ec9ea-293">El estado se establece en **Cerrado**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="ec9ea-294">El sistema vuelve a reservar el número de lote que se ordenó originalmente y asigna la ubicación y los id. de las matrículas de entidad de almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="ec9ea-295">(Este proceso es equivalente a ejecutar la función **Reservar línea** para la línea de pedido de un número de lote dado).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="ec9ea-296">Como resultado, el lote **B11** se muestra como comprometido en la ficha desplegable **Números de lote comprometidos con la línea de origen** de la página **Reserva de lotes** y el campo **Reserva** contiene una cantidad de **10** para el número de lote **B11**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="ec9ea-297">Además, el campo **Ubicación** se establece en **FL-001** y el campo **Matrícula de entidad de almacén** se establece en **LP11**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="ec9ea-298">(Puede agregar estos campos a la cuadrícula si no están visibles).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="ec9ea-299">Las siguientes tablas proporcionan una descripción general que muestra cómo el sistema maneja la reserva de lotes confirmada por pedido para acciones específicas de almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="ec9ea-300">Para interpretar el contenido de las tablas, suponga que cada acción de almacén se ejecuta en el contexto del trabajo de almacén existente que se origina en una reserva de lote confirmada por pedido, o que la ejecución de cada acción de almacén afecta el trabajo de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="ec9ea-301">En estas tablas, la columna "Cantidad de lote está disponible" indica si hay una cantidad de lote disponible además de la cantidad que ya está reservada para las reservas actuales confirmadas por pedido o ya está reservada por el trabajo de almacén que se origina a partir de reservas de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="ec9ea-302">Reemplazar la ubicación de selección en el trabajo abierto</span><span class="sxs-lookup"><span data-stu-id="ec9ea-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec9ea-303">Parámetro de configuración clave</span><span class="sxs-lookup"><span data-stu-id="ec9ea-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="ec9ea-304">Cantidad de lote disponible</span><span class="sxs-lookup"><span data-stu-id="ec9ea-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ec9ea-305">Pasos clave del usuario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-305">Key user steps</span></span></th>
<th><span data-ttu-id="ec9ea-306">Trabajo de almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-306">Warehouse work</span></span></th>
<th><span data-ttu-id="ec9ea-307">Reserva de lote confirmada por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ec9ea-308">La opción <strong>Permitir anulación de ubicación de picking</strong> está habilitada en el trabajador.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ec9ea-309">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-310">Seleccione el elemento de menú <strong>Anular ubicación</strong> en la aplicación Warehouse Mmobile (WMA) cuando comience a seleccionar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-311">Seleccione <strong>Sugerir</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="ec9ea-312">Confirme la nueva ubicación que se sugiere según la disponibilidad de la cantidad de lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-313">En el trabajo actual, se producen las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="ec9ea-314">La ubicación en la línea de selección se actualiza a la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="ec9ea-315">(Si la ubicación está controlada por una placa de matrícula, se asigna una placa de matrícula aleatoria a la transacción del inventario de trabajo, y el trabajador puede elegir de cualquier placa que tenga una cantidad disponible).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="ec9ea-316">Si la cantidad se encuentra en más de una placa en la nueva ubicación, la línea de selección original se divide en varias líneas para que coincida con cada placa.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-317">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-318">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-319">Seleccione el elemento de menú <strong>Anular ubicación</strong> en la aplicación WMA cuando comience el trabajo de selección.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-320">Introduzca manualmente una ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-321">La acción <strong>Anular ubicación</strong> no es posible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="ec9ea-322">Falla y se produce un error.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="ec9ea-323">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="ec9ea-324">Botón completo: divide una línea de trabajo debido a un desbordamiento en la ubicación del usuario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec9ea-325">Parámetro de configuración clave</span><span class="sxs-lookup"><span data-stu-id="ec9ea-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="ec9ea-326">Cantidad de lote disponible</span><span class="sxs-lookup"><span data-stu-id="ec9ea-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ec9ea-327">Pasos clave del usuario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-327">Key user steps</span></span></th>
<th><span data-ttu-id="ec9ea-328">Trabajo de almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-328">Warehouse work</span></span></th>
<th><span data-ttu-id="ec9ea-329">Reserva de lote confirmada por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec9ea-330">La opción <strong>Permitir la división del trabajo</strong> está habilitada en el elemento de menú del dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="ec9ea-331">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-332">Seleccione el elemento de menú <strong>Completo</strong> en la aplicación WMA cuando procese el trabajo de selección.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-333">En el campo <strong>Cant. picking</strong>, introduzca una cantidad parcial de la selección requerida para indicar la capacidad total.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-334">En el trabajo actual, la cantidad se actualiza con la cantidad restante que debe seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="ec9ea-335">Se crea y cierra un nuevo trabajo para la cantidad seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="ec9ea-336">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="ec9ea-337">Reducir la cantidad seleccionada de trabajo completado (de una carga)</span><span class="sxs-lookup"><span data-stu-id="ec9ea-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec9ea-338">Parámetro de configuración clave</span><span class="sxs-lookup"><span data-stu-id="ec9ea-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="ec9ea-339">Cantidad de lote disponible</span><span class="sxs-lookup"><span data-stu-id="ec9ea-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ec9ea-340">Pasos clave del usuario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-340">Key user steps</span></span></th>
<th><span data-ttu-id="ec9ea-341">Trabajo de almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-341">Warehouse work</span></span></th>
<th><span data-ttu-id="ec9ea-342">Reserva de lote confirmada por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ec9ea-343">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-343">Not applicable</span></span></td>
<td><span data-ttu-id="ec9ea-344">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-345">Abra la página <strong>Reducir cantidad seleccionada</strong> en la línea de carga.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="ec9ea-346">Especifique la cantidad completa cuya selección se debe anular.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="ec9ea-347">Seleccione una ubicación/matrícula como destino del movimiento.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="ec9ea-348">El trabajo asociado con la línea de carga se cancela.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="ec9ea-349">Se crea y se cierra el nuevo trabajo de movimiento de inventario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-350">La cantidad se vuelve a reservar para el mismo lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ec9ea-351">El sistema asigna aleatoriamente una ubicación y una placa de matrícula (si la ubicación está controlada por la placa de matrícula) donde la cantidad está disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-352">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-352">No</span></span></td>
<td><span data-ttu-id="ec9ea-353">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-353">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-354">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-354">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-355">La cantidad se vuelve a reservar para el mismo lote y para la misma ubicación y matrícula (si la ubicación está controlada por la matrícula) que se ingresaron durante la eliminación.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="ec9ea-356">Mover un artículo dentro de un almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="ec9ea-357">Esta acción de almacén es aplicable solo al movimiento del tipo **Proceso de creación de trabajo**, no al movimiento por plantilla.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec9ea-358">Parámetro de configuración clave</span><span class="sxs-lookup"><span data-stu-id="ec9ea-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="ec9ea-359">Cantidad de lote disponible</span><span class="sxs-lookup"><span data-stu-id="ec9ea-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ec9ea-360">Pasos clave del usuario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-360">Key user steps</span></span></th>
<th><span data-ttu-id="ec9ea-361">Trabajo de almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-361">Warehouse work</span></span></th>
<th><span data-ttu-id="ec9ea-362">Reserva de lote confirmada por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ec9ea-363">La opción <strong>Permitir movimiento de inventario con trabajo asociado</strong> está habilitada en el trabajador.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ec9ea-364">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-365">Inicie un movimiento en la WMA.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="ec9ea-366">Especifique las ubicaciones de origen y destino.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-367">En todo el trabajo existente que se ve afectado por el movimiento, la ubicación de selección se actualiza con la nueva ubicación de destino.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="ec9ea-368">Se crea y se cierra el nuevo trabajo de movimiento de inventario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-369">Todas las reservas existentes que se ven afectadas por el movimiento de cantidad desde la ubicación dada se vuelven a reservar para el mismo lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="ec9ea-370">El sistema asigna aleatoriamente una ubicación y una placa de matrícula (si la ubicación está controlada por la placa de matrícula) donde la cantidad está disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-371">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-371">No</span></span></td>
<td><span data-ttu-id="ec9ea-372">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-372">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-373">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-373">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-374">Todas las reservas existentes que se ven afectadas por el movimiento de cantidad desde la ubicación dada se vuelven a reservar para el mismo lote y para la nueva ubicación y matrícula de destino (si la ubicación está controlada por la matrícula).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="ec9ea-375">Revertir la cantidad seleccionada de trabajo completado (de una carga u oleada)</span><span class="sxs-lookup"><span data-stu-id="ec9ea-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec9ea-376">Parámetro de configuración clave</span><span class="sxs-lookup"><span data-stu-id="ec9ea-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="ec9ea-377">Cantidad de lote disponible</span><span class="sxs-lookup"><span data-stu-id="ec9ea-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ec9ea-378">Pasos clave del usuario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-378">Key user steps</span></span></th>
<th><span data-ttu-id="ec9ea-379">Trabajo de almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-379">Warehouse work</span></span></th>
<th><span data-ttu-id="ec9ea-380">Reserva de lote confirmada por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="ec9ea-381">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-381">Not applicable</span></span></td>
<td><span data-ttu-id="ec9ea-382">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-383">Abra la página <strong>Invertir el trabajo</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="ec9ea-384">En la página solicitada, seleccione la opción <strong>Dejar los artículos en la ubicación actual</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-385">Todo el trabajo asociado con la carga se cancela.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="ec9ea-386">La cantidad se vuelve a reservar para el mismo lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ec9ea-387">El sistema asigna aleatoriamente una ubicación y una placa de matrícula (si la ubicación está controlada por la placa de matrícula) donde la cantidad está disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-388">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-388">No</span></span></td>
<td><span data-ttu-id="ec9ea-389">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-389">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-390">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-390">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-391">La cantidad se vuelve a reservar para el mismo lote, y para la ubicación y la placa donde se dejó la cantidad al revertirla.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-392">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-393">Abra la página <strong>Invertir el trabajo</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="ec9ea-394">En la página solicitada, seleccione la opción <strong>Asignar artículos a esta ubicación</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-395">El trabajo actual se cancela.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="ec9ea-396">Se crea y se cierra el nuevo trabajo de movimiento de inventario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-397">La cantidad se vuelve a reservar para el mismo lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ec9ea-398">El sistema asigna aleatoriamente una ubicación y una placa de matrícula (si la ubicación está controlada por la placa de matrícula) donde la cantidad está disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-399">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-399">No</span></span></td>
<td><span data-ttu-id="ec9ea-400">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-400">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-401">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-401">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-402">La cantidad se vuelve a reservar para el mismo lote y para la ubicación y la matrícula a las que estaba asignada la cantidad al revertirla.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-403">Sí/No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-404">Abra la página <strong>Invertir el trabajo</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="ec9ea-405">En la página solicitada, seleccione la opción <strong>Mover artículos a esta ubicación</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-406">No se admite la reversión.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="ec9ea-407">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-408">Sí/No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-409">Abra la página <strong>Invertir el trabajo</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="ec9ea-410">En la página solicitada, seleccione la opción <strong>Mover artículos según las directivas de ubicación</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-411">No se admite la reversión.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="ec9ea-412">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="ec9ea-413">Realizar la selección corta de una cantidad: registre la cantidad como físicamente no encontrada en la ubicación/matrícula mientras realiza el trabajo de selección</span><span class="sxs-lookup"><span data-stu-id="ec9ea-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec9ea-414">Parámetro de configuración clave</span><span class="sxs-lookup"><span data-stu-id="ec9ea-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="ec9ea-415">Cantidad de lote disponible</span><span class="sxs-lookup"><span data-stu-id="ec9ea-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ec9ea-416">Pasos clave del usuario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-416">Key user steps</span></span></th>
<th><span data-ttu-id="ec9ea-417">Trabajo de almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-417">Warehouse work</span></span></th>
<th><span data-ttu-id="ec9ea-418">Reserva de lote confirmada por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ec9ea-419">Se ha configurado una excepción de trabajo del tipo <strong>Selección corta</strong> donde <strong>Reasignación de artículos</strong> = <strong>Ninguna</strong>, <strong>Ajustar inventario</strong> = <strong>Sí</strong> y <strong>Eliminar reservas</strong> = <strong>No</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="ec9ea-420">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-421">Seleccione el elemento de menú <strong>ShortPick</strong> en la aplicación WMA cuando ejecute el trabajo de selección.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-422">En el campo <strong>Seleccionar cantidad</strong>, especifique <strong>0</strong> (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-423">En el campo <strong>Razón</strong>, introduzca <strong>Sin reasignación</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-424">El trabajo actual está cerrado y la cantidad seleccionada es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-425">Se crea una transacción de inventario de tipo <strong>Recuento</strong> y con el tipo de problema <strong>Vendido</strong> para representar el ajuste.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-426">La cantidad se vuelve a reservar para el mismo lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ec9ea-427">El sistema asigna aleatoriamente una ubicación y una placa de matrícula (si la ubicación está controlada por la placa de matrícula) donde la cantidad está disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-428">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-428">No</span></span></td>
<td><span data-ttu-id="ec9ea-429">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-430">La acción de selección corta falla y se genera un error.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="ec9ea-431">El trabajo actual permanece abierto.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-432">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="ec9ea-433">Se ha configurado una excepción de trabajo del tipo <strong>Selección corta</strong> donde <strong>Reasignación de artículos</strong> = <strong>Ninguna</strong>, <strong>Ajustar inventario</strong> = <strong>Sí</strong> y <strong>Eliminar reservas</strong> = <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="ec9ea-434">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-435">Seleccione el elemento de menú <strong>ShortPick</strong> en la aplicación WMA cuando ejecute el trabajo de selección.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-436">En el campo <strong>Seleccionar cantidad</strong>, especifique <strong>0</strong> (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-437">En el campo <strong>Razón</strong>, introduzca <strong>Sin reasignación</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-438">El trabajo actual está cerrado y la cantidad seleccionada es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-439">Se crea una transacción de inventario de tipo <strong>Recuento</strong> y con el tipo de problema <strong>Vendido</strong> para representar el ajuste.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-440">Todas las reservas existentes que se ven afectadas por el ajuste de la cantidad en la ubicación con selección corta se vuelven a reservar para el mismo lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="ec9ea-441">El sistema asigna aleatoriamente una ubicación y una placa de matrícula (si la ubicación está controlada por la placa de matrícula) donde la cantidad está disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-442">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-442">No</span></span></td>
<td><span data-ttu-id="ec9ea-443">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-443">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-444">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-444">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-445">Todas las reservas existentes que se ven afectadas por el ajuste de la cantidad en la ubicación con selección corta se eliminan.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-446">Se ha configurado una excepción de trabajo del tipo <strong>Selección corta</strong> donde <strong>Reasignación de artículos</strong> = <strong>Manual</strong>, <strong>Ajustar inventario</strong> = <strong>Sí</strong> y <strong>Eliminar reservas</strong> = <strong>No/Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="ec9ea-447">Además, la opción <strong>Permitir reasignación manual de artículos</strong> está habilitada en el trabajador.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ec9ea-448">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-449">Seleccione el elemento de menú <strong>ShortPick</strong> en la aplicación WMA cuando ejecute el trabajo de selección.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-450">En el campo <strong>Cantidad de selección corta</strong>, especifique <strong>0</strong> (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-451">En el campo <strong>Razón</strong>, seleccione <strong>Selección corta con reasignación manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="ec9ea-452">Seleccione la ubicación/matrícula en la lista.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-453">En el trabajo actual, se producen las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="ec9ea-454">La línea de selección se cierra y la cantidad seleccionada es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-455">La línea de venta se cancela.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="ec9ea-456">Se crea una línea de selección nueva.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-456">A new pick line is created.</span></span> <span data-ttu-id="ec9ea-457">Utiliza la ubicación/matrícula que seleccionó el usuario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="ec9ea-458">Se crea una línea de colocación nueva.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ec9ea-459">Se crea una transacción de inventario de tipo <strong>Recuento</strong> y con el tipo de problema <strong>Vendido</strong> para representar el ajuste.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-460">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-461">Se ha configurado una excepción de trabajo del tipo <strong>Selección corta</strong> donde <strong>Reasignación de artículos</strong> = <strong>Manual</strong>, <strong>Ajustar inventario</strong> = <strong>Sí</strong> y <strong>Eliminar reservas</strong> = <strong>No</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="ec9ea-462">Además, la opción <strong>Permitir reasignación manual de artículos</strong> está habilitada en el trabajador.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ec9ea-463">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-464">Seleccione el elemento de menú <strong>ShortPick</strong> en la aplicación WMA cuando ejecute el trabajo de selección.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-465">En el campo <strong>Cantidad de selección corta</strong>, especifique <strong>0</strong> (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-466">En el campo <strong>Razón</strong>, seleccione <strong>Selección corta con reasignación manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-467">La acción de selección corta falla y se genera un error.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="ec9ea-468">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-469">Se ha configurado una excepción de trabajo del tipo <strong>Selección corta</strong> donde <strong>Reasignación de artículos</strong> = <strong>Manual</strong>, <strong>Ajustar inventario</strong> = <strong>Sí</strong> y <strong>Eliminar reservas</strong> = <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="ec9ea-470">Además, la opción <strong>Permitir reasignación manual de artículos</strong> está habilitada en el trabajador.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="ec9ea-471">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-472">Seleccione el elemento de menú <strong>ShortPick</strong> en la aplicación WMA cuando ejecute el trabajo de selección.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-473">En el campo <strong>Cantidad de selección corta</strong>, especifique <strong>0</strong> (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-474">En el campo <strong>Razón</strong>, seleccione <strong>Selección corta con reasignación manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="ec9ea-475">Seleccione la ubicación/matrícula en la lista.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-476">En el trabajo actual, se producen las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="ec9ea-477">La línea de selección se cierra y la cantidad seleccionada es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-478">La línea de venta se cancela.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ec9ea-479">Se crea una transacción de inventario de tipo <strong>Recuento</strong> y con el tipo de problema <strong>Vendido</strong> para representar el ajuste.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ec9ea-480">Todas las reservas existentes que se ven afectadas por el ajuste de la cantidad en la ubicación/matrícula con selección corta se eliminan.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-481">Se ha configurado una excepción de trabajo del tipo <strong>Selección corta</strong> donde <strong>Reasignación de artículos</strong> = <strong>Automática</strong>, <strong>Ajustar inventario</strong> = <strong>Sí/No</strong> y <strong>Eliminar reservas</strong> = <strong>Sí/No</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="ec9ea-482">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ec9ea-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-483">Seleccione el elemento de menú <strong>ShortPick</strong> en la aplicación WMA cuando ejecute el trabajo de selección.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="ec9ea-484">En el campo <strong>Cantidad de selección corta</strong>, especifique <strong>0</strong> (cero).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="ec9ea-485">En el campo <strong>Razón</strong>, seleccione <strong>Selección corta con reasignación automática</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-486">La selección corta que implica reasignación automática no es compatible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="ec9ea-487">La selección corta que implica reasignación automática no es compatible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="ec9ea-488">Cambiar el estado de inventario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="ec9ea-489">Esta acción de almacén se puede realizar desde múltiples puntos de entrada.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="ec9ea-490">El ejemplo que se muestra aquí usa la acción **Cambio de estado de inventario** en la página **Disponible por ubicación**.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec9ea-491">Parámetro de configuración clave</span><span class="sxs-lookup"><span data-stu-id="ec9ea-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="ec9ea-492">Cantidad de lote disponible</span><span class="sxs-lookup"><span data-stu-id="ec9ea-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="ec9ea-493">Pasos clave del usuario</span><span class="sxs-lookup"><span data-stu-id="ec9ea-493">Key user steps</span></span></th>
<th><span data-ttu-id="ec9ea-494">Trabajo de almacén</span><span class="sxs-lookup"><span data-stu-id="ec9ea-494">Warehouse work</span></span></th>
<th><span data-ttu-id="ec9ea-495">Reserva de lote confirmada por pedido</span><span class="sxs-lookup"><span data-stu-id="ec9ea-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="ec9ea-496">En la pestaña <strong>Almacén</strong>, en el registro <strong>Almacén</strong>, el campo <strong>Eliminar reservas y marcas</strong> se establece en <strong>Reservas</strong> o <strong>Marcas y reservas</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="ec9ea-497">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-498">Seleccione una ubicación específica.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="ec9ea-499">Seleccione una línea que tenga un artículo, una ubicación y una matrícula específicos (si la ubicación está controlada por matrícula).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="ec9ea-500">Seleccione <strong>Cambio de estado de inventario</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="ec9ea-501">Establezca el campo <strong>Estado de inventario</strong> en <strong>Bloqueo</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-502">No se permiten cambios en el estado del inventario para cantidades reservadas para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-503">La cantidad se vuelve a reservar para el mismo lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ec9ea-504">El sistema asigna aleatoriamente una ubicación y una placa de matrícula (si la ubicación está controlada por la placa de matrícula) donde la cantidad está disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="ec9ea-505">Dos transacciones de inventario de tipo <strong>Cambio de estado de inventario</strong> se crean para representar el cambio en la dimensión de estado del inventario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="ec9ea-506">Se crea una transacción de inventario de tipo <strong>Bloqueo de inventario</strong> y tipo de problema <strong>Cantidad física reservada</strong> para representar la reserva de la cantidad bloqueada.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-507">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-507">No</span></span></td>
<td><span data-ttu-id="ec9ea-508">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-508">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-509">No se permiten cambios en el estado del inventario para cantidades reservadas para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ec9ea-510">Se elimina la reserva.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="ec9ea-511">Dos transacciones de inventario de tipo <strong>Cambio de estado de inventario</strong> se crean para representar el cambio en la dimensión de estado del inventario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="ec9ea-512">Se crea una transacción de inventario de tipo <strong>Bloqueo de inventario</strong> y tipo de problema <strong>Cantidad física reservada</strong> para representar la reserva de la cantidad bloqueada.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="ec9ea-513">En la pestaña <strong>Almacén</strong>, en el registro <strong>Almacén</strong>, el campo <strong>Eliminar reservas y marcas</strong> se establece en <strong>Ninguna</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="ec9ea-514">Sí</span><span class="sxs-lookup"><span data-stu-id="ec9ea-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ec9ea-515">Seleccione una ubicación específica.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="ec9ea-516">Seleccione una línea que tenga un artículo, una ubicación y una matrícula específicos (si la ubicación está controlada por matrícula).</span><span class="sxs-lookup"><span data-stu-id="ec9ea-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="ec9ea-517">Seleccione <strong>Cambio de estado de inventario</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="ec9ea-518">Establezca el campo <strong>Estado de inventario</strong> en <strong>Bloqueo</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="ec9ea-519">No se permiten cambios en el estado del inventario para cantidades reservadas para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="ec9ea-520">La cantidad se vuelve a reservar para el mismo lote.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="ec9ea-521">El sistema asigna aleatoriamente una ubicación y una placa de matrícula (si la ubicación está controlada por la placa de matrícula) donde la cantidad está disponible.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec9ea-522">No</span><span class="sxs-lookup"><span data-stu-id="ec9ea-522">No</span></span></td>
<td><span data-ttu-id="ec9ea-523">Vea la fila anterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-523">See the previous row.</span></span></td>
<td><span data-ttu-id="ec9ea-524">No se permiten cambios en el estado del inventario para cantidades reservadas para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="ec9ea-525">No se permiten cambios en el estado del inventario.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="ec9ea-526">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="ec9ea-526">Limitations</span></span>

- <span data-ttu-id="ec9ea-527">La funcionalidad flexible de reserva de dimensión a nivel de almacén no admite las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="ec9ea-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="ec9ea-528">Gestión del peso capturado</span><span class="sxs-lookup"><span data-stu-id="ec9ea-528">Catch weight management</span></span>
    - <span data-ttu-id="ec9ea-529">Inventario negativo físico</span><span class="sxs-lookup"><span data-stu-id="ec9ea-529">Physical negative inventory</span></span>
    - <span data-ttu-id="ec9ea-530">Reserva contra suministro solicitado</span><span class="sxs-lookup"><span data-stu-id="ec9ea-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="ec9ea-531">Órdenes de transferencia y selección de materia prima.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="ec9ea-532">La regla de consolidación de contenedores para el embalaje por unidad directiva tiene limitaciones.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="ec9ea-533">Para las reservas confirmadas por pedido, le recomendamos que no use plantillas de compilación de contenedores donde el campo **Unidad de directiva de empaque** esté habilitado.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="ec9ea-534">En el diseño actual, las directivas de ubicación no se utilizan cuando se crea el trabajo de almacén.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="ec9ea-535">Por lo tanto, solo la unidad más baja en el grupo de secuencia de unidades (la unidad de inventario) se aplica durante el paso de oleada de contenedorización.</span><span class="sxs-lookup"><span data-stu-id="ec9ea-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>