---
title: Suspender y reanudar una transacción en el punto de venta (PDV)
description: Este tema explica cómo los usuarios pueden suspender transacciones en curso y reanudarlas después más tarde o en otro registro con Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f513e2d857908f2b95d27bf48ff1e826724d7cbf
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023989"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="77737-103">Suspender y reanudar una transacción en el punto de venta (PDV)</span><span class="sxs-lookup"><span data-stu-id="77737-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="77737-104">Los usuarios de punto de venta (PDV) pueden suspender transacciones en curso y después reanudarlas más tarde o en otro registro.</span><span class="sxs-lookup"><span data-stu-id="77737-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="77737-105">Las transacciones se suspenden a menudo para liberar rápidamente un registro para otra tarea sin perder ningún progreso con respecto a la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="77737-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="77737-106">Por ejemplo, un socio de la tienda empieza a procesar la transacción de un cliente en un dispositivo móvil, pero debe completarla en un registro con una caja registradora.</span><span class="sxs-lookup"><span data-stu-id="77737-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="77737-107">En este caso, el socio de la tienda puede suspender la transacción en el dispositivo móvil y, a continuación recuperarla y reanudarla en un registro.</span><span class="sxs-lookup"><span data-stu-id="77737-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="77737-108">Configurar la funcionalidad de suspender y reanudar</span><span class="sxs-lookup"><span data-stu-id="77737-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="77737-109">Operaciones de PDV</span><span class="sxs-lookup"><span data-stu-id="77737-109">POS operations</span></span>

<span data-ttu-id="77737-110">Dos [Operaciones de PDV](pos-operations.md) permiten que el soporte de PDV suspenda y reanude escenarios.</span><span class="sxs-lookup"><span data-stu-id="77737-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="77737-111">Puede asignar estas operaciones a [cuadrículas de botones](pos-screen-layouts.md) en la página de la transacción o a la página de inicio.</span><span class="sxs-lookup"><span data-stu-id="77737-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="77737-112">503: Suspender transacción</span><span class="sxs-lookup"><span data-stu-id="77737-112">503: Suspend transaction</span></span>
- <span data-ttu-id="77737-113">504: Recuperar transacción</span><span class="sxs-lookup"><span data-stu-id="77737-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="77737-114">Plantilla de recepción</span><span class="sxs-lookup"><span data-stu-id="77737-114">Receipt template</span></span>

<span data-ttu-id="77737-115">El PDV se puede configurar para generar un resguardo que se imprime cuando se suspende una transacción.</span><span class="sxs-lookup"><span data-stu-id="77737-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="77737-116">Dicho resguardo se puede utilizar para identificar y recuperar rápidamente la transacción más adelante.</span><span class="sxs-lookup"><span data-stu-id="77737-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="77737-117">Para permitir al PDV imprimir un resguardo, debe agregar el formato de recepción **Transacción suspendida** al perfil de recepción de la tienda.</span><span class="sxs-lookup"><span data-stu-id="77737-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="77737-118">Puede diseñar el formato de recepción de modo que incluya o excluya detalles específicos acerca de la transacción.</span><span class="sxs-lookup"><span data-stu-id="77737-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="77737-119">Por ejemplo, el formato puede incluir un código de barras para admitir la exploración.</span><span class="sxs-lookup"><span data-stu-id="77737-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="77737-120">Numeración del recibo</span><span class="sxs-lookup"><span data-stu-id="77737-120">Receipt numbering</span></span>

<span data-ttu-id="77737-121">Con respecto a otros tipos de la transacción PDV que generan un recibo impreso, puede definir una secuencia numérica para las transacciones suspendidas en la sección **Numeración del recibo** del perfil de funcionalidad de la tienda.</span><span class="sxs-lookup"><span data-stu-id="77737-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="77737-122">Anular al cerrar el turno</span><span class="sxs-lookup"><span data-stu-id="77737-122">Void when closing shift</span></span>

<span data-ttu-id="77737-123">Puede usar la opción **Anular al cerrar el turno** para requerir que los usuarios completen o anulen cualquier transacción suspendida antes de que se cierre su cambio.</span><span class="sxs-lookup"><span data-stu-id="77737-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="77737-124">Durante la operación **Cerrar turno** , el PDV solicitará a los usuarios que vean o anulen todas las transacciones suspendidas pendientes.</span><span class="sxs-lookup"><span data-stu-id="77737-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="77737-125">Suspender y reanudar una transacción</span><span class="sxs-lookup"><span data-stu-id="77737-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="77737-126">Suspender una transacción</span><span class="sxs-lookup"><span data-stu-id="77737-126">Suspend a transaction</span></span>

<span data-ttu-id="77737-127">Los usuarios que tengan privilegios suficientes, y que tengan un diseño de pantalla que incluye la operación **Suspender transacción** , pueden suspender una transacción para que pueda recuperarse más adelante o en otro registro.</span><span class="sxs-lookup"><span data-stu-id="77737-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="77737-128">Las transacciones se pueden suspender solo si **no** contienen los siguientes tipos de líneas:</span><span class="sxs-lookup"><span data-stu-id="77737-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="77737-129">Líneas de pago activas</span><span class="sxs-lookup"><span data-stu-id="77737-129">Active payment lines</span></span>
- <span data-ttu-id="77737-130">Líneas de tarjeta regalo (para emitir una tarjeta regalo o agregar al saldo de la tarjeta regalo)</span><span class="sxs-lookup"><span data-stu-id="77737-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="77737-131">Una transacción suspendida no afecta a la información de ventas ni a la información de disponibilidad del inventario para la tienda.</span><span class="sxs-lookup"><span data-stu-id="77737-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="77737-132">Reanudar una transacción suspendida</span><span class="sxs-lookup"><span data-stu-id="77737-132">Resume a suspended transaction</span></span>

<span data-ttu-id="77737-133">Las transacciones suspendidas se pueden recuperar y reanudar en la misma tienda por cualquier usuario que tenga privilegios suficientes, y que también tenga un diseño que incluya la operación **Recuperar transacción**.</span><span class="sxs-lookup"><span data-stu-id="77737-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="77737-134">Para recuperar de forma rápida y sencilla una transacción suspendida, digitalice el código de barras del resguardo impreso mientras  visualiza la lista de transacciones de la operación **Recuperar transacción**.</span><span class="sxs-lookup"><span data-stu-id="77737-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="77737-135">Consideraciones para el modo sin conexión</span><span class="sxs-lookup"><span data-stu-id="77737-135">Considerations for offline mode</span></span>

- <span data-ttu-id="77737-136">Toda transacción que se haya suspendido mientras PDV se encuentra en el modo en línea no se puede reanudar en modo desconectado, ya que los datos no se sincronizan con la base de datos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="77737-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="77737-137">Si suspende una transacción mientras el PDV se encuentra en el modo desconectado, puede recuperarlo en modo desconectado, siempre y cuando no se haya devuelto al PDV al modo conectado en cualquier momento desde que suspendió la transacción.</span><span class="sxs-lookup"><span data-stu-id="77737-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="77737-138">Cuando se devuelve el PDV al estado anterior en modo conectado, los datos sobre transacciones suspendidas se pasan a la base de datos en línea y se quitan de la base de datos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="77737-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="77737-139">Por lo tanto, las transacciones se pueden reanudar solo en modo conectado.</span><span class="sxs-lookup"><span data-stu-id="77737-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="77737-140">Si devuelve el PDV al modo desconectado, no podrá reanudar las transacciones suspendidas, pues ya se han quitado de la base de datos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="77737-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="77737-141">Anular una transacción suspendida</span><span class="sxs-lookup"><span data-stu-id="77737-141">Void a suspended transaction</span></span>

<span data-ttu-id="77737-142">Puede anular transacciones suspendidas recuperando la transacción y después ejecutando la operación **Anular transacción** , o seleccionando la transacción en el lista **Recuperar transacción** y seleccionando **Anular** en la barra de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77737-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="77737-143">De manera alternativa, el almacén se puede configurar para solicitar a los usuarios que anulen las transacciones suspendidas cuando acaben su turno.</span><span class="sxs-lookup"><span data-stu-id="77737-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>