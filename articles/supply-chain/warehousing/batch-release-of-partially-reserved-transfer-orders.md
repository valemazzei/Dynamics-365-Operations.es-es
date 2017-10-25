---
title: "Liberación por lotes de pedidos de transferencia parcialmente reservados"
description: "En este tema se describe cómo configurar y aplicar la opción de liberación por lotes de pedidos de transferencia parcialmente reservados desde un dispositivo móvil."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 273ced77a61d485426c0830556e4401e782e86c4
ms.openlocfilehash: 369afe3f4bae223c8d4f9fc55e9cd9744590b6d3
ms.contentlocale: es-es
ms.lasthandoff: 10/24/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="6e88e-103">Liberación por lotes de pedidos de transferencia parcialmente reservados</span><span class="sxs-lookup"><span data-stu-id="6e88e-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6e88e-104">La funcionalidad de la opción de liberación por lotes de pedidos de transferencia parcialmente reservados le permite liberar parcialmente pedidos de transferencia a un almacén mediante un trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="6e88e-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="6e88e-105">Dado que tiene la opción de liberar una cantidad parcial, no tiene que esperar a que la totalidad del pedido esté disponible en el almacén antes de poder liberar un pedido.</span><span class="sxs-lookup"><span data-stu-id="6e88e-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="6e88e-106">La liberación de pedidos en un almacén es un proceso de gestión avanzada de almacenes.</span><span class="sxs-lookup"><span data-stu-id="6e88e-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="6e88e-107">Este proceso implica actividades tales como la recogida, embalaje y envío que un trabajador del almacén puede efectuar usando un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="6e88e-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="6e88e-108">Dónde se aplica</span><span class="sxs-lookup"><span data-stu-id="6e88e-108">Where it applies</span></span>

<span data-ttu-id="6e88e-109">Para esta funcionalidad, los pedidos de transferencia se liberan en un almacén mediante un trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="6e88e-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="6e88e-110">Esta función resulta útil si no tiene suficiente inventario en el almacén, pero todavía quiere transferir artículos desde un almacén a otro.</span><span class="sxs-lookup"><span data-stu-id="6e88e-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="6e88e-111">Cómo se configura</span><span class="sxs-lookup"><span data-stu-id="6e88e-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="6e88e-112">Especifique los criterios que han de cumplir los pedidos de transferencia y los de ventas.</span><span class="sxs-lookup"><span data-stu-id="6e88e-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="6e88e-113">Antes de que el pedido se pueda liberar parcialmente en un almacén en forma de lote, se deben cumplir los criterios de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="6e88e-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="6e88e-114">Estos criterios de cumplimiento se determinan gracias a la directiva de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="6e88e-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="6e88e-115">Las directivas de cumplimiento de los pedidos de transferencia y ventas se especifican en el nivel de empresa.</span><span class="sxs-lookup"><span data-stu-id="6e88e-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="6e88e-116">Según la configuración de la directiva de cumplimiento, la liberación de pedidos en lote se puede aceptar o rechazar.</span><span class="sxs-lookup"><span data-stu-id="6e88e-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="6e88e-117">Será entonces cuando se procesen los pedidos en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="6e88e-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="6e88e-118">Para crear directivas de cumplimiento para pedidos de transferencia y ventas, haga clic en **Gestión de almacenes** \> **Configuración** \> **Liberar en almacén** \> **Directiva de cumplimiento** y. a continuación, escriba un nombre y una descripción para crear una directiva de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="6e88e-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="6e88e-119">Para especificar un índice de entrega, un tipo de valor y el mensaje que se muestra si se infringe la directiva de cumplimiento, haga clic en **Gestión de almacenes** \> **Configuración** \> **Liberar en almacén** \> **Directiva de cumplimiento** y, a continuación configure los campos del **índice de entrega**, el **tipo de valor** y el **mensaje de infracción de cumplimiento** .</span><span class="sxs-lookup"><span data-stu-id="6e88e-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="6e88e-120">Configurar las directivas de cumplimiento de los pedidos de transferencia y los de ventas</span><span class="sxs-lookup"><span data-stu-id="6e88e-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="6e88e-121">Para configurar las directivas de cumplimiento de los pedidos de transferencia, haga clic en **Gestión del inventario** \> **Configuración** \> **Parámetros de gestión de inventarios y almacenes** \> **Pedidos de transferencia** \> **Gestión del almacenes** y, a continuación, seleccione una directiva de cumplimiento del pedido de transferencia.</span><span class="sxs-lookup"><span data-stu-id="6e88e-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="6e88e-122">Para establecer las directivas de cumplimiento de los pedidos de ventas, haga clic en **Clientes** \> **Configuración** \> **Parámetros de clientes** \> **Gestión de almacenes** y seleccione una directiva de cumplimiento del pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="6e88e-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="6e88e-123">Permitir la liberación en lote y especificar la cantidad que se debe liberar en ese lote</span><span class="sxs-lookup"><span data-stu-id="6e88e-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="6e88e-124">Se usa un trabajo por lotes para liberar pedidos en lote en un almacén.</span><span class="sxs-lookup"><span data-stu-id="6e88e-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="6e88e-125">Los parámetros que distinguen los pedidos que se deben ejecutar en un trabajo por lotes se establecen en el mismo trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="6e88e-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="6e88e-126">El parámetro **Cantidad** especifica si la cantidad total o la cantidad reservada físicamente se debe liberar en el lote.</span><span class="sxs-lookup"><span data-stu-id="6e88e-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="6e88e-127">El parámetro **Permitir la liberación de pedidos liberados parcialmente** determina si los pedidos del lote se deben aceptar o rechazar si se hubieran liberado con anterioridad.</span><span class="sxs-lookup"><span data-stu-id="6e88e-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="6e88e-128">Para establecer los parámetros **Cantidad** y **Permitir la liberación de pedidos liberados parcialmente** de los pedidos de transferencia, haga clic en **Gestión de almacenes** \> **Liberar en almacén** \> **Liberación automática de pedidos de transferencia**.</span><span class="sxs-lookup"><span data-stu-id="6e88e-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="6e88e-129">Para establecer los parámetros **Cantidad** y **Permitir la liberación de pedidos liberados parcialmente** de los pedidos de ventas, haga clic en **Gestión de almacenes** \> **Liberar en almacén** \> **Liberación automática de pedidos de ventas**.</span><span class="sxs-lookup"><span data-stu-id="6e88e-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>
