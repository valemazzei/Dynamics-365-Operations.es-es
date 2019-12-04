---
title: Configurar los documentos de transferencia para el movimiento de mercancías dentro de una empresa
description: Este procedimiento muestra cómo crear documentos de transferencia para movimiento de mercancías dentro de una empresa.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe4dd04595c961e1c66178e6ac6955e945869ded
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185690"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="e9521-103">Configurar los documentos de transferencia para el movimiento de mercancías dentro de una empresa</span><span class="sxs-lookup"><span data-stu-id="e9521-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9521-104">Este procedimiento muestra cómo crear documentos de transferencia para movimiento de mercancías dentro de una empresa.</span><span class="sxs-lookup"><span data-stu-id="e9521-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="e9521-105">Este procedimiento sólo está disponible para entidades jurídicas con dirección principal en Lituania.</span><span class="sxs-lookup"><span data-stu-id="e9521-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="e9521-106">Este procedimiento se ha creado con los datos de demostración de la empresa DEMF, con una dirección principal en Lituania.</span><span class="sxs-lookup"><span data-stu-id="e9521-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="e9521-107">Antes de completar este procedimiento, deberá completar el procedimiento de “Configuración de los documentos de transferencia de mercancías dentro de una empresa”.</span><span class="sxs-lookup"><span data-stu-id="e9521-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="e9521-108">Este procedimiento está dirigido a contables de inventario.</span><span class="sxs-lookup"><span data-stu-id="e9521-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="e9521-109">Este procedimiento es para una función que se ha agregado en la versión 1611 de Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="e9521-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="e9521-110">Creación de un pedido de transferencia</span><span class="sxs-lookup"><span data-stu-id="e9521-110">Create a transfer order</span></span>
1. <span data-ttu-id="e9521-111">Vaya a Gestión del inventario > Pedidos de entrada > Orden de transferencia.</span><span class="sxs-lookup"><span data-stu-id="e9521-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="e9521-112">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="e9521-112">Click New.</span></span>
3. <span data-ttu-id="e9521-113">En el campo Desde almacén, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="e9521-114">En el campo Hasta almacén, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="e9521-115">Haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="e9521-115">Click Add.</span></span>
6. <span data-ttu-id="e9521-116">En la lista, marque la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="e9521-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="e9521-117">En el campo Número de artículo, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="e9521-118">Especificar los detalles de transporte para el pedido de transferencia</span><span class="sxs-lookup"><span data-stu-id="e9521-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="e9521-119">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="e9521-119">Click Save.</span></span>
2. <span data-ttu-id="e9521-120">En el panel de acciones, haga clic en Enviar.</span><span class="sxs-lookup"><span data-stu-id="e9521-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="e9521-121">Haga clic en Detalles de transporte.</span><span class="sxs-lookup"><span data-stu-id="e9521-121">Click Transportation details.</span></span>
4. <span data-ttu-id="e9521-122">Seleccione Sí en el campo Imprimir detalles de transporte.</span><span class="sxs-lookup"><span data-stu-id="e9521-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="e9521-123">En el campo Mercancías emitidas por, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="e9521-124">En el campo Paquete, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="e9521-125">En el campo Nivel de riesgo de la carga, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="e9521-126">En el campo Transportista, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="e9521-127">En el campo Modelo, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="e9521-128">En el campo Número de registro, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="e9521-129">En el campo Número de registro del tráiler, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="e9521-130">En el campo Conductor, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="e9521-131">En el campo Nombre de conductor, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="e9521-132">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="e9521-132">Click Save.</span></span>
15. <span data-ttu-id="e9521-133">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="e9521-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="e9521-134">Ver el albarán para el pedido de transferencia sin registrar</span><span class="sxs-lookup"><span data-stu-id="e9521-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="e9521-135">Haga clic en Albarán.</span><span class="sxs-lookup"><span data-stu-id="e9521-135">Click Packing slip.</span></span>
2. <span data-ttu-id="e9521-136">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="e9521-136">Click OK.</span></span>
3. <span data-ttu-id="e9521-137">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="e9521-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="e9521-138">Ver el albarán para el pedido de transferencia registrado</span><span class="sxs-lookup"><span data-stu-id="e9521-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="e9521-139">En el panel de acciones, haga clic Transferir pedido.</span><span class="sxs-lookup"><span data-stu-id="e9521-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="e9521-140">En el panel de acciones, haga clic en Enviar.</span><span class="sxs-lookup"><span data-stu-id="e9521-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="e9521-141">Haga clic en Enviar pedido de transferencia.</span><span class="sxs-lookup"><span data-stu-id="e9521-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="e9521-142">Haga clic en la pestaña General.</span><span class="sxs-lookup"><span data-stu-id="e9521-142">Click the General tab.</span></span>
5. <span data-ttu-id="e9521-143">En el campo Actualizar, seleccione una opción.</span><span class="sxs-lookup"><span data-stu-id="e9521-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="e9521-144">Haga clic en la ficha Visión general.</span><span class="sxs-lookup"><span data-stu-id="e9521-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="e9521-145">En el campo Albarán, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="e9521-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="e9521-146">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="e9521-146">Click OK.</span></span>
9. <span data-ttu-id="e9521-147">En el panel de acciones, haga clic en Enviar.</span><span class="sxs-lookup"><span data-stu-id="e9521-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="e9521-148">Haga clic en Albarán.</span><span class="sxs-lookup"><span data-stu-id="e9521-148">Click Packing slip.</span></span>
11. <span data-ttu-id="e9521-149">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="e9521-149">Click OK.</span></span>
