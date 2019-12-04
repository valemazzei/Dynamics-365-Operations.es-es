---
title: Visión general de pagos de cliente
description: Esta guía de tareas le muestra los distintos métodos para introducir pagos de cliente.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7777ba38e4bf41b17fae698200017b933fc9e876
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188174"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="e160b-103">Visión general de pagos de cliente</span><span class="sxs-lookup"><span data-stu-id="e160b-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e160b-104">Esta guía de tareas le muestra los distintos métodos para introducir pagos de cliente.</span><span class="sxs-lookup"><span data-stu-id="e160b-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="e160b-105">Esta tarea usa la empresa de demostración USMF.</span><span class="sxs-lookup"><span data-stu-id="e160b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e160b-106">Vaya a **Panel de exploración > Módulos > Clientes > Pagos > Diario de pagos**.</span><span class="sxs-lookup"><span data-stu-id="e160b-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="e160b-107">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="e160b-107">Click **New**.</span></span>
3. <span data-ttu-id="e160b-108">Seleccione el diario de pagos donde se van a guardar los pagos de cliente.</span><span class="sxs-lookup"><span data-stu-id="e160b-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="e160b-109">Seleccione el diario o especifíquelo manualmente.</span><span class="sxs-lookup"><span data-stu-id="e160b-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="e160b-110">En el **panel de acciones**, haga clic en **Introducir pagos de cliente**.</span><span class="sxs-lookup"><span data-stu-id="e160b-110">On **Action pane**, click **Enter customer payments**.</span></span> <span data-ttu-id="e160b-111">Introducir pagos de cliente se usa para registrar un pago de cliente cada vez.</span><span class="sxs-lookup"><span data-stu-id="e160b-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="e160b-112">Se especifica la información de pago en la parte superior y, a continuación, se pueden marcar las facturas pagadas con el pago, todo desde la misma página.</span><span class="sxs-lookup"><span data-stu-id="e160b-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="e160b-113">Especifique el cliente de quien recibió el pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-113">Enter the customer from whom you received the payment.</span></span> <span data-ttu-id="e160b-114">Si no conoce al cliente pero sabe que se pagó una transacción, puede usar el campo Transacción para especificar el pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="e160b-115">Especifique o seleccione la factura en el campo Transacción.</span><span class="sxs-lookup"><span data-stu-id="e160b-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="e160b-116">De forma predeterminada, el cliente se incluirá automáticamente al seleccionar la transacción.</span><span class="sxs-lookup"><span data-stu-id="e160b-116">The customer will automatically default after you select the transaction.</span></span>
7. <span data-ttu-id="e160b-117">En el campo **Referencia del pago**, especifique una referencia para el pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-117">In the **Payment reference** field, enter a payment reference.</span></span> <span data-ttu-id="e160b-118">La referencia de pago podría ser el número de cheque del cliente o una referencia del pago electrónico del cliente.</span><span class="sxs-lookup"><span data-stu-id="e160b-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="e160b-119">La referencia de pago solo es obligatoria si se especifica incluir el pago en un resguardo de depósito.</span><span class="sxs-lookup"><span data-stu-id="e160b-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="e160b-120">En el campo **Resguardo de depósito**, seleccione si el pago se incluirá en un resguardo de depósito.</span><span class="sxs-lookup"><span data-stu-id="e160b-120">In the **Deposit slip** field, select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="e160b-121">En el campo **Importe**, especifique el importe del pago al cliente.</span><span class="sxs-lookup"><span data-stu-id="e160b-121">In the **Amount** field, enter the amount of the customer payment.</span></span> <span data-ttu-id="e160b-122">El importe de pago no se especificará en un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e160b-122">The payment amount will not default.</span></span> <span data-ttu-id="e160b-123">Se debe especificar manualmente.</span><span class="sxs-lookup"><span data-stu-id="e160b-123">It must be manually entered.</span></span> 
10. <span data-ttu-id="e160b-124">Marque las facturas pagadas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="e160b-124">Mark the invoices that were paid by the customer.</span></span> <span data-ttu-id="e160b-125">Si el pago es un anticipo, no es necesario marcar ninguna factura para su liquidación.</span><span class="sxs-lookup"><span data-stu-id="e160b-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="e160b-126">El pago se puede guardar y registrar.</span><span class="sxs-lookup"><span data-stu-id="e160b-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="e160b-127">La liquidación de una factura puede producirse en otro momento.</span><span class="sxs-lookup"><span data-stu-id="e160b-127">Settlement to an invoice can happen at a later time.</span></span>
11. <span data-ttu-id="e160b-128">Especifique el importe del pago que se liquidará en la factura marcada.</span><span class="sxs-lookup"><span data-stu-id="e160b-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> <span data-ttu-id="e160b-129">Este campo se puede usar cuando el pago corresponde a un pago parcial.</span><span class="sxs-lookup"><span data-stu-id="e160b-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="e160b-130">Si no especifica un importe, el importe que liquidar se determina automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e160b-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>
12. <span data-ttu-id="e160b-131">Haga clic en **Guardar en diario**.</span><span class="sxs-lookup"><span data-stu-id="e160b-131">Click **Save in journal**.</span></span> <span data-ttu-id="e160b-132">Antes de guardar el pago en el diario, asegúrese de que se haya definido la cuenta de contrapartida.</span><span class="sxs-lookup"><span data-stu-id="e160b-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="e160b-133">**Guardar en diario** guardará el pago y lo pasará al diario.</span><span class="sxs-lookup"><span data-stu-id="e160b-133">Using **Save in journal** will save the payment and move it to the journal.</span></span> <span data-ttu-id="e160b-134">A continuación, podrá continuar especificando el siguiente pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-134">You can then continue entering the next payment.</span></span>
13. <span data-ttu-id="e160b-135">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="e160b-135">Close the page.</span></span>
14. <span data-ttu-id="e160b-136">En **Panel de acciones**, haga clic en Líneas.</span><span class="sxs-lookup"><span data-stu-id="e160b-136">On **Action pane**, click Lines.</span></span> <span data-ttu-id="e160b-137">Al abrir Líneas verá los pagos registrados en la página **Introducir pagos de cliente** y también almacenados en el diario.</span><span class="sxs-lookup"><span data-stu-id="e160b-137">When opening Lines, you will see any payments you recorded on the **Enter customer payments** page and saved into the journal.</span></span> <span data-ttu-id="e160b-138">También puede usar esta página para introducir nuevos pagos de clientes o editar pagos de clientes existentes antes de registrarlos.</span><span class="sxs-lookup"><span data-stu-id="e160b-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>
15. <span data-ttu-id="e160b-139">Haga clic en **Nuevo** para crear otro pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-139">Click **New** to create another payment.</span></span> 
16. <span data-ttu-id="e160b-140">Seleccione el cliente de quien recibió el pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-140">Select the customer from whom you received the payment.</span></span> <span data-ttu-id="e160b-141">Si no sabe quién es el cliente pero sabe qué factura desembolsa el pago, use el campo Factura para especificar o seleccionar manualmente la factura.</span><span class="sxs-lookup"><span data-stu-id="e160b-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="e160b-142">El cliente se incluirá de forma predeterminada una vez se seleccione la factura.</span><span class="sxs-lookup"><span data-stu-id="e160b-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="e160b-143">Haga clic en **Liquidar transacciones** para marcar las facturas pagadas.</span><span class="sxs-lookup"><span data-stu-id="e160b-143">Click **Settle transctions** to mark invoices that were paid.</span></span> <span data-ttu-id="e160b-144">No es necesario liquidar el pago en ninguna factura.</span><span class="sxs-lookup"><span data-stu-id="e160b-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="e160b-145">Si es un anticipo o si no sabe qué factura se ha pagado, puede introducir y registrar el pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="e160b-146">El pago se podrá liquidar en una factura más adelante.</span><span class="sxs-lookup"><span data-stu-id="e160b-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="e160b-147">Marque las facturas desembolsadas en el pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="e160b-148">En el campo **Importe**, especifique el importe del pago que se liquidará en la factura.</span><span class="sxs-lookup"><span data-stu-id="e160b-148">In the **Amount** field, enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="e160b-149">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e160b-149">Click **OK**.</span></span>
21. <span data-ttu-id="e160b-150">En el campo **Referencia del pago**, especifique una referencia para el pago.</span><span class="sxs-lookup"><span data-stu-id="e160b-150">In the **Payment reference** field, enter a payment reference.</span></span> <span data-ttu-id="e160b-151">La referencia de pago solo es obligatoria si se especifica incluir el pago en un resguardo de depósito.</span><span class="sxs-lookup"><span data-stu-id="e160b-151">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="e160b-152">En el **panel de acciones**, haga clic en **Registrar** para registrar los pagos del cliente.</span><span class="sxs-lookup"><span data-stu-id="e160b-152">On **Action pane**, click **Post** to post the customer payments.</span></span> 
