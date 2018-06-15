---
title: "Crear pedidos de servicio automáticamente"
description: Es posible crear pedidos de servicio para un acuerdo de servicio o para varios.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c39e5b5eb79859b0a76c357edfee953ca90c0c4a
ms.contentlocale: es-es
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-automatically"></a><span data-ttu-id="014cb-103">Crear pedidos de servicio automáticamente</span><span class="sxs-lookup"><span data-stu-id="014cb-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="014cb-104">Es posible crear pedidos de servicio para un acuerdo de servicio o para varios.</span><span class="sxs-lookup"><span data-stu-id="014cb-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="014cb-105">Cuando se creen, podrá verlos en el formulario **Pedidos de servicio**.</span><span class="sxs-lookup"><span data-stu-id="014cb-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="014cb-106">Los pedidos de servicio sólo se crean para el período válido del acuerdo de servicio.</span><span class="sxs-lookup"><span data-stu-id="014cb-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="014cb-107">Si el intervalo que especifique en el formulario **Crear pedidos de servicio** empieza antes de la fecha de inicio o termina después de la fecha de finalización del acuerdo de servicio, sólo se crearán para la parte del intervalo que se encuentre dentro de las fechas del acuerdo de servicio.</span><span class="sxs-lookup"><span data-stu-id="014cb-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="014cb-108">Al crear pedidos de servicio de forma manual o automática desde la línea del acuerdo de servicio, el pedido de servicio debe estar dentro del intervalo de tiempo definido por las fechas inicial y final para la línea, a menos que no especifique una fecha final en la línea.</span><span class="sxs-lookup"><span data-stu-id="014cb-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="014cb-109">Crear pedidos de servicio automáticamente para un acuerdo de servicio</span><span class="sxs-lookup"><span data-stu-id="014cb-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="014cb-110">Haga clic en **Gestión de servicio** \> **Común** \> **Contratos de servicio** \> **Contratos de servicio**.</span><span class="sxs-lookup"><span data-stu-id="014cb-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="014cb-111">Seleccione un acuerdo de servicio.</span><span class="sxs-lookup"><span data-stu-id="014cb-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="014cb-112">Haga clic en la ficha **Entregar** y, a continuación, haga clic en **Pedidos de servicio planificados**.</span><span class="sxs-lookup"><span data-stu-id="014cb-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="014cb-113">Especifique las fechas en los campos **Desde fecha** y **Hasta fecha** para definir el período de servicio.</span><span class="sxs-lookup"><span data-stu-id="014cb-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="014cb-114">Active la casilla de verificación **Mostrar el registro de información** para que aparezca una lista de los pedidos de servicio que se han creado.</span><span class="sxs-lookup"><span data-stu-id="014cb-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="014cb-115">Seleccione tipos de transacción en el grupo de campos **Incluir los tipos de transacción** .</span><span class="sxs-lookup"><span data-stu-id="014cb-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="014cb-116">Estos tipos de transacciones representan las líneas que se crean en el acuerdo de servicio y cada tipo de transacción que seleccione genera varios pedidos de servicio según el intervalo de servicio especificado en la línea del acuerdo de servicio.</span><span class="sxs-lookup"><span data-stu-id="014cb-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="014cb-117">Para crear cualquier pedido de servicio que falta en una serie continua de pedidos de servicio, active la casilla de verificación **Continuo**.</span><span class="sxs-lookup"><span data-stu-id="014cb-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="014cb-118">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="014cb-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="014cb-119">Crear pedidos de servicio automáticamente para varios acuerdos de servicio</span><span class="sxs-lookup"><span data-stu-id="014cb-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="014cb-120">Haga clic en **Gestión de servicio** \> **Periódico** \> **Pedidos de servicio** \> **Crear pedidos de servicio**.</span><span class="sxs-lookup"><span data-stu-id="014cb-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="014cb-121">Haga clic en **Seleccionar** para efectuar selecciones de adición o eliminación de los criterios que se van a utilizar para crear pedidos de servicio.</span><span class="sxs-lookup"><span data-stu-id="014cb-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="014cb-122">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="014cb-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="014cb-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="014cb-123">See also</span></span>

[<span data-ttu-id="014cb-124">Pedidos de servicio</span><span class="sxs-lookup"><span data-stu-id="014cb-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="014cb-125">Crear pedidos de servicio automáticamente</span><span class="sxs-lookup"><span data-stu-id="014cb-125">Automatically creating service orders</span></span>](auto-create-service-orders.md)

  


