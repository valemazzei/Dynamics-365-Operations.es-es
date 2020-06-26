---
title: Consolidar los envíos manualmente utilizando la página Consolidar envíos
description: Este tema presenta un escenario en el que se despachan múltiples pedidos al almacén en la misma carga y luego se consolidan usando la página Consolidar envíos.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: acc6e1d09894b57d2bb063bacbcddef239c1a8bd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383854"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="31ff0-103">Consolidar los envíos manualmente utilizando la página Consolidar envíos</span><span class="sxs-lookup"><span data-stu-id="31ff0-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31ff0-104">Este tema presenta un escenario en el que se despachan múltiples pedidos al almacén en la misma carga y luego se consolidan usando la página **Consolidar envíos**.</span><span class="sxs-lookup"><span data-stu-id="31ff0-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="31ff0-105">Hacer que los datos de demostración estén disponibles</span><span class="sxs-lookup"><span data-stu-id="31ff0-105">Make demo data available</span></span>

<span data-ttu-id="31ff0-106">El escenario de este tema hace referencia a valores y registros que se incluyen en los datos de demostración estándar que se proporcionan para Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="31ff0-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="31ff0-107">Si desea utilizar los valores que se proporcionan aquí mientras realiza los ejercicios, asegúrese de trabajar en un entorno donde estén instalados los datos de demostración y configure la entidad jurídica en **USMF** antes de empezar.</span><span class="sxs-lookup"><span data-stu-id="31ff0-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="31ff0-108">Configurar directivas de consolidación de envíos y filtros de productos</span><span class="sxs-lookup"><span data-stu-id="31ff0-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="31ff0-109">El escenario que se describe aquí supone que ya ha activado la función, realizado los ejercicios de [Configurar directivas de consolidación de envíos](configure-shipment-consolidation-policies.md) y creado las directivas y otros registros que se describen allí.</span><span class="sxs-lookup"><span data-stu-id="31ff0-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="31ff0-110">Asegúrese de hacer esos ejercicios antes de continuar con este escenario.</span><span class="sxs-lookup"><span data-stu-id="31ff0-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="31ff0-111">Crear los pedidos de ventas para este escenario</span><span class="sxs-lookup"><span data-stu-id="31ff0-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="31ff0-112">Comience creando una colección de pedidos de ventas con los que pueda trabajar.</span><span class="sxs-lookup"><span data-stu-id="31ff0-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="31ff0-113">Debe trabajar con un almacén habilitado para procesos de almacén avanzado (WMS).</span><span class="sxs-lookup"><span data-stu-id="31ff0-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="31ff0-114">A menos que se mencione explícitamente un almacén diferente, ese mismo almacén debe utilizarse para cada uno de los siguientes conjuntos de pedidos.</span><span class="sxs-lookup"><span data-stu-id="31ff0-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="31ff0-115">Vaya a **Clientes \> Pedidos \> Todos los pedidos de ventas** y cree una colección de pedidos de ventas que tengan la configuración que se describe en las siguientes subsecciones.</span><span class="sxs-lookup"><span data-stu-id="31ff0-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="31ff0-116">Crear pedidos de ventas 1 y 2</span><span class="sxs-lookup"><span data-stu-id="31ff0-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="31ff0-117">Cree dos pedidos de venta idénticos que tengan la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="31ff0-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="31ff0-118">**Cuenta de cliente:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="31ff0-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="31ff0-119">**Grupo:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="31ff0-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="31ff0-120">Agregue una línea de pedido que tenga la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="31ff0-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="31ff0-121">**Número de artículo:** *A0001* (un artículo al que no se ha asignado el filtro **Código 4**)</span><span class="sxs-lookup"><span data-stu-id="31ff0-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="31ff0-122">**Cantidad:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="31ff0-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="31ff0-123">Seleccione **Inventario \> Reserva** y luego, en el Panel de acciones, seleccione **Reservar lote interno** para reservar la línea de pedido.</span><span class="sxs-lookup"><span data-stu-id="31ff0-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="31ff0-124">Crear pedidos de ventas 3 y 4</span><span class="sxs-lookup"><span data-stu-id="31ff0-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="31ff0-125">Cree dos pedidos de venta idénticos que tengan la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="31ff0-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="31ff0-126">**Cuenta de cliente:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="31ff0-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="31ff0-127">**Grupo:** Deje este campo en blanco.</span><span class="sxs-lookup"><span data-stu-id="31ff0-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="31ff0-128">Agregue una línea de pedido que tenga la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="31ff0-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="31ff0-129">**Número de artículo:** *A0001* (un artículo al que no se ha asignado el filtro **Código 4**)</span><span class="sxs-lookup"><span data-stu-id="31ff0-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="31ff0-130">**Cantidad:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="31ff0-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="31ff0-131">Seleccione **Inventario \> Reserva** y luego, en el Panel de acciones, seleccione **Reservar lote interno** para reservar la línea de pedido.</span><span class="sxs-lookup"><span data-stu-id="31ff0-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="31ff0-132">Despachar los pedidos al almacén</span><span class="sxs-lookup"><span data-stu-id="31ff0-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="31ff0-133">Siga estos pasos para despachar cada pedido de ventas que creó para este escenario al almacén.</span><span class="sxs-lookup"><span data-stu-id="31ff0-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="31ff0-134">Vaya a **Clientes \> Pedidos \> Todos los pedidos de venta**.</span><span class="sxs-lookup"><span data-stu-id="31ff0-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="31ff0-135">Busque y seleccione el pedido de ventas a despachar.</span><span class="sxs-lookup"><span data-stu-id="31ff0-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="31ff0-136">En el panel Acciones, en la pestaña **Almacén**, seleccione **Acciones \> Liberar al almacén** para despachar el pedido de ventas seleccionado.</span><span class="sxs-lookup"><span data-stu-id="31ff0-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="31ff0-137">Repita este procedimiento para cada pedido de ventas restante que creó para este escenario.</span><span class="sxs-lookup"><span data-stu-id="31ff0-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="31ff0-138">Consolidar envíos</span><span class="sxs-lookup"><span data-stu-id="31ff0-138">Consolidate shipments</span></span>

1. <span data-ttu-id="31ff0-139">Vaya a **Gestión de almacenes \> Envíos \> Todos los envíos**.</span><span class="sxs-lookup"><span data-stu-id="31ff0-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="31ff0-140">Busque y seleccione un envío que se creó cuando el pedido de ventas 1 se despachó al almacén.</span><span class="sxs-lookup"><span data-stu-id="31ff0-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="31ff0-141">(Su campo **Directiva de consolidación de envíos** debe establecerse en *Grupo de pedidos*).</span><span class="sxs-lookup"><span data-stu-id="31ff0-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="31ff0-142">En el panel Acciones, en la pestaña **Envíos**, seleccione **Envíos \> Consolidar envíos**.</span><span class="sxs-lookup"><span data-stu-id="31ff0-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="31ff0-143">Verifique los envíos que se sugieren para consolidación.</span><span class="sxs-lookup"><span data-stu-id="31ff0-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="31ff0-144">Solo se debe sugerir para consolidación un envío que tenga la misma directiva.</span><span class="sxs-lookup"><span data-stu-id="31ff0-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="31ff0-145">Cierre la página **Consolidación de envíos**.</span><span class="sxs-lookup"><span data-stu-id="31ff0-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="31ff0-146">Busque y seleccione un envío que se creó cuando el pedido de ventas 3 se despachó al almacén.</span><span class="sxs-lookup"><span data-stu-id="31ff0-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="31ff0-147">(Su campo **Directiva de consolidación de envíos** debe establecerse en *Predeterminada*).</span><span class="sxs-lookup"><span data-stu-id="31ff0-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="31ff0-148">En el panel Acciones, en la pestaña **Envíos**, seleccione **Envíos \> Consolidar envíos**.</span><span class="sxs-lookup"><span data-stu-id="31ff0-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="31ff0-149">Verifique lno se sugiere ningún envío para consolidación.</span><span class="sxs-lookup"><span data-stu-id="31ff0-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="31ff0-150">Seleccione **Mostrar filtros**.</span><span class="sxs-lookup"><span data-stu-id="31ff0-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="31ff0-151">En el panel **Filtros**, quite el filtro **Número de pedido** y luego seleccione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="31ff0-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="31ff0-152">Verifique los envíos que se sugieren para consolidación.</span><span class="sxs-lookup"><span data-stu-id="31ff0-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="31ff0-153">Solo se debe sugerir para consolidación un envío que tenga la misma directiva.</span><span class="sxs-lookup"><span data-stu-id="31ff0-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31ff0-154">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="31ff0-154">Additional resources</span></span>

- [<span data-ttu-id="31ff0-155">Directivas de consolidación de envíos</span><span class="sxs-lookup"><span data-stu-id="31ff0-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="31ff0-156">Configurar directivas de consolidación de envíos</span><span class="sxs-lookup"><span data-stu-id="31ff0-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)