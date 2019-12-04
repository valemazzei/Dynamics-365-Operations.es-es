---
title: Configurar liquidación
description: Cómo y cuándo se liquidan las transacciones puede ser temas complejos, lo que es fundamental que entienda y defina correctamente los parámetros para satisfacer sus requisitos empresariales. Este tema describe los parámetros que se usan para la liquidación tanto para Proveedores como Clientes.
author: kweekley
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 094b8876b3b10b6dcbc0ce399a1a9915271459ed
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188381"
---
# <a name="configure-settlement"></a><span data-ttu-id="f94de-104">Configurar liquidación</span><span class="sxs-lookup"><span data-stu-id="f94de-104">Configure settlement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f94de-105">Cómo y cuándo se liquidan las transacciones puede ser temas complejos, lo que es fundamental que entienda y defina correctamente los parámetros para satisfacer sus requisitos empresariales.</span><span class="sxs-lookup"><span data-stu-id="f94de-105">How and when transactions are settled can be complex subjects, so it's essential that you understand and correctly define the parameters to meet your business requirements.</span></span> <span data-ttu-id="f94de-106">Este tema describe los parámetros que se usan para la liquidación tanto para Proveedores como Clientes.</span><span class="sxs-lookup"><span data-stu-id="f94de-106">This topic describes the parameters that are used for settlement for both Accounts payable and Accounts receivable.</span></span> 

<span data-ttu-id="f94de-107">Los siguientes parámetros afectan al procesamiento de las liquidaciones en Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f94de-107">The following parameters affect how settlements are processed in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="f94de-108">La liquidación es el proceso de liquidar una factura con un pago o una nota de abono.</span><span class="sxs-lookup"><span data-stu-id="f94de-108">Settlement is the process of settling an invoice against a payment or credit note.</span></span> <span data-ttu-id="f94de-109">Estos parámetros se encuentran en el área **Liquidación** de las páginas **Parámetros de clientes** y **Parámetros de proveedores**.</span><span class="sxs-lookup"><span data-stu-id="f94de-109">These parameters are located in the **Settlement** area of the **Accounts receivable parameters** and **Accounts payable parameters** pages.</span></span>

- <span data-ttu-id="f94de-110">**Liquidación automática**: establezca esta opción en **Sí** si se debe liquidar una transacción automáticamente con otras transacciones abiertas cuando se registre.</span><span class="sxs-lookup"><span data-stu-id="f94de-110">**Automatic settlement** – Set this option to **Yes** if a transaction should be settled automatically against other open transactions when it is posted.</span></span> <span data-ttu-id="f94de-111">Si esta opción se establece en **No**, los usuarios pueden liquidar transacciones manualmente al especificar pagos, o más adelante, mediante la página **Liquidar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="f94de-111">If this option is set to **No**, users can manually settle transactions when they enter payments, or later, by using the **Settle transactions** page.</span></span>
- <span data-ttu-id="f94de-112">**Administración del descuento por pronto pago**: especifique cómo [se controla un descuento por pronto pago cuando se sobrepaga una factura](cash-discount-handling-overpayments.md).</span><span class="sxs-lookup"><span data-stu-id="f94de-112">**Cash discount administration** – Specify how a [cash discount is handled when an invoice is overpaid](cash-discount-handling-overpayments.md).</span></span> <span data-ttu-id="f94de-113">Para un sobrepago, el descuento por pronto pago se puede reducir, se puede tratar como diferencia o puede quedar a cuenta para el proveedor o el cliente.</span><span class="sxs-lookup"><span data-stu-id="f94de-113">For an overpayment, the cash discount can be reduced, it can be treated as a difference, or it can remain on account for the vendor or customer.</span></span>
  -   <span data-ttu-id="f94de-114">**No específico**: el importe del descuento por pronto pago se reduce por el importe del sobrepago.</span><span class="sxs-lookup"><span data-stu-id="f94de-114">**Unspecific** – The cash discount amount is reduced by the overpayment amount.</span></span> <span data-ttu-id="f94de-115">Este funcionamiento se usa siempre, independientemente de si el importe del sobrepago es superior o inferior al importe que se especifica en el campo **Máximo de sobrepago/pago insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="f94de-115">This behavior is always used, regardless of whether the overpayment amount is more than or less than the amount that is entered in the **Maximum overpayment or underpayment** field.</span></span>
  -   <span data-ttu-id="f94de-116">**Específico**: el importe del sobrepago se registra en una cuenta contable de diferencia de descuento por pronto pago o permanece como saldo en la cuenta del cliente o del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f94de-116">**Specific** – The overpayment amount either is posted to a cash discount difference ledger account, or remains a balance on the customer’s or vendor's account.</span></span> <span data-ttu-id="f94de-117">El funcionamiento específico depende de si el importe del sobrepago se encuentra entre 0,00 y el importe especificado en el campo **Sobrepago o pago insuficiente máximo**, o si el importe del sobrepago es superior al importe de **Sobrepago o pago insuficiente máximo**.</span><span class="sxs-lookup"><span data-stu-id="f94de-117">The specific behavior depends on whether the overpayment amount is between 0.00 and the amount that is entered in the **Maximum overpayment or underpayment** field, or whether the overpayment amount is more than the **Maximum overpayment or underpayment** amount.</span></span>
- <span data-ttu-id="f94de-118">**Diferencia máxima de decimales**: especifique la diferencia máxima de decimales permitida para las transacciones liquidadas.</span><span class="sxs-lookup"><span data-stu-id="f94de-118">**Maximum penny difference** – Enter the maximum permitted penny difference for the settled transactions.</span></span> <span data-ttu-id="f94de-119">Si la diferencia es igual o menor que la diferencia de decimales especificada en este campo, la diferencia se registrará en la cuenta contable de diferencia de decimales que se especifica en la página **Cuentas para transacciones automáticas**.</span><span class="sxs-lookup"><span data-stu-id="f94de-119">If the difference is equal to or less than the penny difference that is specified in this field, the difference will be posted to the penny difference ledger account that is specified on the **Accounts for automatic transactions** page.</span></span>
- <span data-ttu-id="f94de-120">**Máximo de sobrepago/pago insuficiente**: especifique el importe que se acepta para el sobrepago o pago insuficiente.</span><span class="sxs-lookup"><span data-stu-id="f94de-120">**Maximum overpayment or underpayment** – Enter the amount that is accepted for overpayment and underpayment.</span></span> <span data-ttu-id="f94de-121">Para calcular los impuestos sobre pagos insuficientes o sobrepagos, en la página **Parámetros de Contabilidad general**, haga clic en **Impuestos** y, a continuación, seleccione la opción **Impuestos de sobrepago/pago insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="f94de-121">To calculate tax on overpayments or underpayments, on the **General ledger parameters** page, click **Sales tax**, and then select the **Sales tax on overpayment or underpayment** option.</span></span>
  -   <span data-ttu-id="f94de-122">Si el sobrepago o el pago insuficiente produce una diferencia menor que la diferencia definida en el campo **Diferencia máxima de decimales**, la diferencia de decimales se registra en la cuenta de diferencias de pago.</span><span class="sxs-lookup"><span data-stu-id="f94de-122">If the overpayment or underpayment produces a difference that is less than the difference that is defined in the **Maximum penny difference** field, the penny difference amount is posted to the penny difference account.</span></span>
  -   <span data-ttu-id="f94de-123">Si el sobrepago o el pago insuficiente produce una diferencia de decimales mayor que la diferencia definida en el campo **Diferencia máxima de decimales**, el importe de la diferencia se registra en la cuenta de diferencia seleccionada para el tipo de registro **Descuento por pronto pago del cliente** o el tipo de registro **Descuento por pronto pago del proveedor** de la página **Cuentas para transacciones automáticas**.</span><span class="sxs-lookup"><span data-stu-id="f94de-123">If the overpayment or underpayment produces a difference that is more than the difference that is defined in the **Maximum penny difference** field, the difference amount is posted to the difference account that is selected for the **Customer cash discount** or **Vendor cash discount** posting type on the **Accounts for automatic transactions** page.</span></span>
- <span data-ttu-id="f94de-124">**Calcular descuento por pronto pago para pagos parciales**: establezca esta opción en **Sí** para permitir que los descuentos por pronto pago se calculen automáticamente para pagos parciales.</span><span class="sxs-lookup"><span data-stu-id="f94de-124">**Calculate cash discounts for partial payments** – Set this option to **Yes** to enable cash discounts to be automatically calculated for partial payments.</span></span>
  -   <span data-ttu-id="f94de-125">El efecto de esta opción depende del valor del campo **Utilizar descuento por pronto pago** en la página **Liquidar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="f94de-125">The effect of this option depends on the value of the **Use cash discount** field on the **Settle transactions** page.</span></span> <span data-ttu-id="f94de-126">Si esta opción se establece en **Sí**, el descuento se toma cuando el campo **Utilizar descuento por pronto pago** se establece en **Normal**.</span><span class="sxs-lookup"><span data-stu-id="f94de-126">If this option is set to **Yes**, the discount is taken when the **Use cash discount** field is set to **Normal**.</span></span> <span data-ttu-id="f94de-127">Cuando el campo **Utilizar descuento por pronto pago** se establece en **Siempre**, siempre se obtiene el descuento por pronto pago, independientemente de la configuración de este campo.</span><span class="sxs-lookup"><span data-stu-id="f94de-127">When the **Use cash discount** field is set to **Always**, the cash discount is always taken, regardless of the setting of this field.</span></span> <span data-ttu-id="f94de-128">Cuando el campo **Utilizar descuento por pronto pago** se establece en **Nunca**, nunca se obtiene el descuento por pronto pago, independientemente de la configuración de este campo.</span><span class="sxs-lookup"><span data-stu-id="f94de-128">When the **Use cash discount** field is set to **Never**, the cash discount is never taken, regardless of the setting of this field.</span></span>
  -   <span data-ttu-id="f94de-129">Si esta opción se establece en **Sí**, y un usuario cambia el valor del campo **Importe para liquidar** en la página **Liquidar transacciones**, el descuento se calcula automáticamente y se muestra como entrada predeterminada en el campo **Importe de descuento por pronto pago para aplicar**.</span><span class="sxs-lookup"><span data-stu-id="f94de-129">If this option is set to **Yes**, and a user changes the value in the **Amount to settle** field on the **Settle transactions** page, the discount is automatically calculated and displayed as the default entry in the **Cash discount amount to take** field.</span></span>
  -   <span data-ttu-id="f94de-130">Si esta opción se establece en **No**, y un usuario cambia el valor del campo **Importe para liquidar** en la página **Liquidar transacciones**, la entrada predeterminada del campo **Importe de descuento por pronto pago para aplicar** es **0** (cero).</span><span class="sxs-lookup"><span data-stu-id="f94de-130">If this option is set to **No**, and a user changes the value in the **Amount to settle** field on the **Settle transactions** page, the default entry in the **Cash discount amount to take** field is **0** (zero).</span></span>
- <span data-ttu-id="f94de-131">**Calcular descuentos por pronto pago para notas de abono**: establezca esta opción en **Sí** para calcular automáticamente un descuento por pronto pago para notas de abono.</span><span class="sxs-lookup"><span data-stu-id="f94de-131">**Calculate cash discounts for credit notes** – Set this option to **Yes** to automatically calculate a cash discount for credit notes.</span></span> <span data-ttu-id="f94de-132">En Clientes, una transacción de nota de abono es una transacción negativa que tiene un valor en el campo **Factura** de la página **Factura de servicios** o una devolución en la página **Pedido de ventas**.</span><span class="sxs-lookup"><span data-stu-id="f94de-132">In Accounts receivable, a credit note transaction is a negative transaction that has a value in the **Invoice** field on the **Free text invoice** page, or a return on the **Sales order** page.</span></span>
  - <span data-ttu-id="f94de-133">El efecto de esta opción depende del valor del campo <strong>Utilizar descuento por pronto pago</strong> en la página <strong>Liquidar transacciones</strong>.</span><span class="sxs-lookup"><span data-stu-id="f94de-133">The effect of this option depends on the value of the <strong>Use cash discount</strong> field on the <strong>Settle transactions</strong> page.</span></span> <span data-ttu-id="f94de-134">Si esta opción se establece en <strong>Sí</strong>, el descuento se toma cuando el campo *<strong><em>Utilizar descuento por pronto pago</em></strong>* se establece en <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="f94de-134">If this option is set to <strong>Yes</strong>, the discount is taken when the *<strong><em>Use cash discount</em></strong>* field is set to <strong>Normal</strong>.</span></span> <span data-ttu-id="f94de-135">Cuando el campo *<strong><em>Utilizar descuento por pronto pago</em></strong>* se establece en <strong>Siempre</strong>, siempre se obtiene el descuento por pronto pago, independientemente de la configuración de este campo.</span><span class="sxs-lookup"><span data-stu-id="f94de-135">When the *<strong><em>Use cash discount</em></strong>* field is set to <strong>Always</strong>, the cash discount is always taken, regardless of the setting of this field.</span></span> <span data-ttu-id="f94de-136">Cuando el campo *<strong><em>Utilizar descuento por pronto pago</em></strong>* se establece en <strong>Nunca</strong>, nunca se obtiene el descuento por pronto pago, independientemente de la configuración de este campo.</span><span class="sxs-lookup"><span data-stu-id="f94de-136">When the *<strong><em>Use cash discount</em></strong>* field is set to <strong>Never</strong>, the cash discount is never taken, regardless of the setting of this field.</span></span>
  - <span data-ttu-id="f94de-137">Si esta opción se establece en **Sí**, y se marca una nota de abono en la página **Liquidar transacciones**, el descuento se calcula automáticamente y se muestra como entrada predeterminada en el campo **Importe de descuento por pronto pago para aplicar**.</span><span class="sxs-lookup"><span data-stu-id="f94de-137">If this option is set to **Yes**, and a credit note is marked on the **Settle transactions** page, the discount is automatically calculated and is displayed as the default entry in the **Cash discount amount to take** field.</span></span>
  - <span data-ttu-id="f94de-138">Si esta opción se establece en **No**, y se marca una nota de abono en la página **Liquidar transacciones**, la entrada predeterminada en el campo **Importe de descuento por pronto pago para aplicar** es **0** (cero).</span><span class="sxs-lookup"><span data-stu-id="f94de-138">If this option is set to **No**, and a credit note is marked on the **Settle transactions** page, the default entry in the **Cash discount amount to take** field is **0** (zero).</span></span>

- <span data-ttu-id="f94de-139">**Cuentas de contrapartida para descuentos (solo Proveedores)**: defina la cuenta contable de descuento por pronto pago predeterminada que se debe usar para el asiento contable para descuentos por pronto pago.</span><span class="sxs-lookup"><span data-stu-id="f94de-139">**Discount offset accounts (AP only)** – Define the default cash discount ledger account that should be used for the accounting entry for cash discounts.</span></span>
  -   <span data-ttu-id="f94de-140">**Usar cuenta principal para descuentos de proveedor**: el descuento por pronto pago se registra en la cuenta principal definida en la página **Configuración de descuento por pronto pago**.</span><span class="sxs-lookup"><span data-stu-id="f94de-140">**Use Main account for vendor discounts** – The cash discount is posted to the main account that is defined on the **Cash discount setup** page.</span></span>
  -   <span data-ttu-id="f94de-141">**Cuentas en las líneas de factura**: el descuento por pronto pago se registra en las cuentas contables en la factura original.</span><span class="sxs-lookup"><span data-stu-id="f94de-141">**Accounts on the invoice lines** – The cash discount is posted to the ledger accounts on the original invoice.</span></span>
- <span data-ttu-id="f94de-142">**Marcar líneas en notas de interés y facturas de servicios (solo Proveedores)**: establezca esta opción en **Sí** para habilitar el botón **Marcar líneas de factura** de las páginas **Introducir pagos de cliente**, **Asiento del diario de pagos** y **Liquidar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="f94de-142">**Mark lines on free text invoices and interest notes (AR only)** – Set this option to **Yes** to enable the **Mark invoice lines** button on the **Enter customer payments**, **Payment journal voucher**, and **Settle transactions** pages.</span></span> <span data-ttu-id="f94de-143">Este botón le permite a los usuarios marcar líneas individuales para la liquidación.</span><span class="sxs-lookup"><span data-stu-id="f94de-143">This button lets users mark individual lines for settlement.</span></span>
- <span data-ttu-id="f94de-144">**Priorizar liquidación (solo Proveedores)**: establezca esta opción en **Sí** para habilitar el botón **Marcar por prioridad** en las páginas **Introducir pagos de cliente** y **Liquidar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="f94de-144">**Prioritize settlement (AR only)** – Set this option to **Yes** to enable the **Mark by priority** button on the **Enter customer payments** and **Settle transactions** pages.</span></span> <span data-ttu-id="f94de-145">Este botón permite a los usuarios asignar el orden de liquidación predeterminado a las transacciones.</span><span class="sxs-lookup"><span data-stu-id="f94de-145">This button lets users assign the predetermined settlement order to transactions.</span></span>  <span data-ttu-id="f94de-146">Después de que el pedido de liquidación se haya aplicado a una transacción, el pedido y la asignación de pago se puede modificar antes del registro.</span><span class="sxs-lookup"><span data-stu-id="f94de-146">After the settlement order has been applied to a transaction, the order and the payment allocation can be modified before posting.</span></span>
- <span data-ttu-id="f94de-147">**Use la prioridad para las liquidaciones automáticas**: establezca esta opción en **Sí** para usar el orden de prioridad definido cuando las transacciones se liquidan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f94de-147">**Use priority for automatic settlements** – Set this option to **Yes** to use the defined priority order when transactions are automatically settled.</span></span> <span data-ttu-id="f94de-148">Este campo sólo está disponible si **Priorizar liquidación** y **Liquidación automática** se establecen en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="f94de-148">This field is available only if the **Prioritize settlement** and **Automatic settlement** options are set to **Yes**.</span></span>

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a><span data-ttu-id="f94de-149">Dimensiones fijas en cuentas principales de clientes/proveedores</span><span class="sxs-lookup"><span data-stu-id="f94de-149">Fixed dimensions on accounts receivable/accounts payable main accounts</span></span>

<span data-ttu-id="f94de-150">Cuando las dimensiones fijas se utilizan en la cuenta principal de clientes/proveedores, las entradas adicionales contables y dos transacciones de proveedor adicionales se enviarán por el proceso de liquidación.</span><span class="sxs-lookup"><span data-stu-id="f94de-150">When fixed dimensions are used on the accounts receivable/accounts payable main account, additional accounting entries and two additional vendor transactions will be posted by the settlement process.</span></span> <span data-ttu-id="f94de-151">La liquidación compara la cuenta contable de clientes/proveedores de la factura y el pago.</span><span class="sxs-lookup"><span data-stu-id="f94de-151">Settlement compares the accounts receivable/accounts payable ledger account from the invoice and payment.</span></span>  <span data-ttu-id="f94de-152">Una vez que se completan conjuntamente el pago y la liquidación, que es el escenario típico, el asiento contable del pago no se registra en la contabilidad general hasta después de que se complete también el proceso de liquidación.</span><span class="sxs-lookup"><span data-stu-id="f94de-152">When the payment and settlement are completed together, which is the typical scenario, the payment’s accounting entry isn’t posted to General ledger until after the settlement process is also complete.</span></span> <span data-ttu-id="f94de-153">Debido al orden de los eventos de procesamiento, la liquidación no puede determinar la cuenta contable real de clientes/proveedores del asiento contable del pago.</span><span class="sxs-lookup"><span data-stu-id="f94de-153">Due to the order of processing events, settlement is unable to determine the actual accounts receivable/accounts payable ledger account from the payment’s accounting entry.</span></span> <span data-ttu-id="f94de-154">La liquidación reconstruye cuál será la cuenta contable para el pago.</span><span class="sxs-lookup"><span data-stu-id="f94de-154">Settlement reconstructs what the ledger account will be for the payment.</span></span> <span data-ttu-id="f94de-155">Esto se convierte en un problema cuando se emplea una dimensión fija para la cuenta principal de clientes/proveedores.</span><span class="sxs-lookup"><span data-stu-id="f94de-155">This becomes an issue when a fixed dimension is used for the accounts receivable/accounts payable main account.</span></span>

<span data-ttu-id="f94de-156">Para reconstruir la cuenta contable, la cuenta principal de clientes/proveedores se recupera del perfil de registro y las dimensiones financieras se recuperan del registro de transacciones del proveedor para el pago, como se define en el diario de pagos.</span><span class="sxs-lookup"><span data-stu-id="f94de-156">To reconstruct the ledger account, the accounts receivable/accounts payable main account is retrieved from the posting profile and the financial dimensions are retrieved from the vendor transaction record for the payment, as defined on the payment journal.</span></span> <span data-ttu-id="f94de-157">Las dimensiones fijas no se establecen de manera predeterminada en los diarios de pago, sino que por el contrario se aplican a la cuenta principal como el último paso del proceso de registro.</span><span class="sxs-lookup"><span data-stu-id="f94de-157">Fixed dimensions are not defaulted onto payment journals, but instead are applied to the main account as the last step of the posting process.</span></span> <span data-ttu-id="f94de-158">Como consecuencia, es probable que el valor de la dimensión fija no esté contenido en la transacción del proveedor, salvo que se establezca de manera predeterminada desde otro origen, como el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f94de-158">As a result, the fixed dimension value is likely not contained on the vendor transaction, unless it defaulted from another source, such as the vendor.</span></span> <span data-ttu-id="f94de-159">La cuenta reconstruida no incluirá la dimensión fija.</span><span class="sxs-lookup"><span data-stu-id="f94de-159">The reconstructed account will not include the fixed dimension.</span></span> <span data-ttu-id="f94de-160">El procesamiento de la liquidación determinará que debe crearse un asiento de ajuste, ya que la factura registrada con el valor de la dimensión fija y la cuenta de pago reconstruida no lo harán.</span><span class="sxs-lookup"><span data-stu-id="f94de-160">Settlement processing will determine that an adjusting entry must be created, because the invoice posted with the fixed dimension value and the reconstructed payment account did not.</span></span>  <span data-ttu-id="f94de-161">A medida que la liquidación continúa con el registro del asiento de ajuste, el último paso en el registro es que se aplique la dimensión fija.</span><span class="sxs-lookup"><span data-stu-id="f94de-161">As settlement continues with posting the adjusting entry, the last step in posting is for the fixed dimension to be applied.</span></span> <span data-ttu-id="f94de-162">Al agregar la dimensión fija al asiento de ajuste, se registra con un débito y un crédito en la misma cuenta contable.</span><span class="sxs-lookup"><span data-stu-id="f94de-162">By adding the fixed dimension to the adjusting entry, it is posted with a debit and credit to the same ledger account.</span></span> <span data-ttu-id="f94de-163">La liquidación no puede revertir el asiento contable.</span><span class="sxs-lookup"><span data-stu-id="f94de-163">Settlement cannot roll back the accounting entry.</span></span>

<span data-ttu-id="f94de-164">Para evitar los asientos contables adicionales, el débito y el crédito en la misma cuenta contable, deben considerarse las siguientes soluciones en función de sus requisitos empresariales.</span><span class="sxs-lookup"><span data-stu-id="f94de-164">To avoid the additional accounting entries, the debit and credit to the same ledger account, the following workarounds should be considered, depending on your business requirements.</span></span> 

-   <span data-ttu-id="f94de-165">Las organizaciones suelen usar dimensiones fijas para rellenar de ceros una dimensión financiera que no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="f94de-165">Organizations often use fixed dimensions to zero-fill a financial dimension that isn't required.</span></span> <span data-ttu-id="f94de-166">Este es habitualmente el caso para cuentas de balance de situación, como clientes/proveedores.</span><span class="sxs-lookup"><span data-stu-id="f94de-166">This is commonly the case for balance sheet accounts, such as accounts receivable/accounts payable.</span></span> <span data-ttu-id="f94de-167">Las estructuras contables se pueden utilizar para no realizar un seguimiento de las dimensiones financieras que suelen rellenarse de ceros.</span><span class="sxs-lookup"><span data-stu-id="f94de-167">Account structures can be used to not track financial dimensions that are typically zero-filled.</span></span>  <span data-ttu-id="f94de-168">Puede quitar la dimensión financiera para las cuentas de balance de situación eliminando la necesidad de usar dimensiones fijas.</span><span class="sxs-lookup"><span data-stu-id="f94de-168">You can remove the financial dimension for the Balance sheet accounts, eliminating the need to use fixed dimensions.</span></span>
-   <span data-ttu-id="f94de-169">Si su organización requiere dimensiones fijas en la cuenta principal de clientes/proveedores, encuentre una forma de establecer de manera predeterminada la dimensión fija en el pago, de manera que se el valor de la dimensión fija se almacene en la transacción de proveedor para el pago.</span><span class="sxs-lookup"><span data-stu-id="f94de-169">If your organization requires fixed dimensions on the accounts receivable/accounts payable main account, find a way to default the fixed dimension onto the payment, so that the fixed dimension value is stored  on the vendor transaction for the payment.</span></span> <span data-ttu-id="f94de-170">Esto permitirá al sistema reconstruir la cuenta principal de clientes/proveedores para incluir los valores de la dimensión fija.</span><span class="sxs-lookup"><span data-stu-id="f94de-170">This will allow the system to reconstruct the accounts receivable/accounts payable main account to include the fixed dimension values.</span></span> <span data-ttu-id="f94de-171">El valor de la dimensión fija se puede definir como predeterminado en los proveedores o en el nombre del diario para el diario de pagos.</span><span class="sxs-lookup"><span data-stu-id="f94de-171">The fixed dimension value can be defined as a default on either vendors or the journal name for the payment journal.</span></span>