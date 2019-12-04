---
title: Perfiles de contabilización del proveedor
description: Los perfiles de contabilización controlan el registro de transacciones de proveedores en la contabilidad general.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43450c5f7ab8295b896b591880da9d0bddd955cf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189301"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="4d781-103">Perfiles de contabilización del proveedor</span><span class="sxs-lookup"><span data-stu-id="4d781-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d781-104">Los perfiles de contabilización controlan el registro de transacciones de proveedores en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="4d781-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="4d781-105">Perfiles de contabilización del proveedor</span><span class="sxs-lookup"><span data-stu-id="4d781-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="4d781-106">Los perfiles de contabilización de proveedor le permiten asignar cuentas de contabilidad general y configuración de documentos a todos los proveedores, un grupo de proveedores o un único proveedor.</span><span class="sxs-lookup"><span data-stu-id="4d781-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="4d781-107">Esta configuración se usará al crear pedidos de compra, facturas de proveedor y pagos en efectivo.</span><span class="sxs-lookup"><span data-stu-id="4d781-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="4d781-108">Para algunas transacciones, cuando seleccione un perfil de contabilización diferente de los perfiles de registro configurados para las transacciones de esta página y que tenga precedencia sobre los mismos.</span><span class="sxs-lookup"><span data-stu-id="4d781-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="4d781-109">El perfil de contabilización predeterminado se define en la ficha desplegable **Impuestos y contabilidad** en la página **Parámetros de proveedores**.</span><span class="sxs-lookup"><span data-stu-id="4d781-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="4d781-110">El perfil de contabilización predeterminado se incluye automáticamente en el encabezado de los documentos nuevos donde puede cambiarlo a otro perfil de contabilización, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="4d781-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="4d781-111">También puede asociar las definiciones de contabilización a los tipos de registro de transacción en la página **Definiciones de contabilización de transacción**.</span><span class="sxs-lookup"><span data-stu-id="4d781-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="4d781-112">Permite configurar los perfiles de registro que controlan el registro de transacciones de proveedores en la contabilidad general en vez de los perfiles de registro.</span><span class="sxs-lookup"><span data-stu-id="4d781-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="4d781-113">Creación de un perfil de registro</span><span class="sxs-lookup"><span data-stu-id="4d781-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="4d781-114">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="4d781-114">**Setup**</span></span>

<span data-ttu-id="4d781-115">Especifique las cuentas contables que se utilizan en el registro de las transacciones con el perfil de contabilización seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4d781-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="4d781-116">Seleccione un código de cuenta y, siempre que sea posible, una cuenta o número de grupo para el perfil de registro seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4d781-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="4d781-117">En el proceso de registro, para buscar el perfil de contabilización más adecuado para cada transacción busque el código de cuenta, el número de cuenta, o el grupo más específico, así como la combinación de números en el siguiente orden.</span><span class="sxs-lookup"><span data-stu-id="4d781-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="4d781-118">Valor del campo **Código de cuenta**</span><span class="sxs-lookup"><span data-stu-id="4d781-118">**Account code** field value</span></span> | <span data-ttu-id="4d781-119">Valor del campo **Número de grupo/cuenta**</span><span class="sxs-lookup"><span data-stu-id="4d781-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="4d781-120">Prioridad de búsqueda</span><span class="sxs-lookup"><span data-stu-id="4d781-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="4d781-121">**Tabla**</span><span class="sxs-lookup"><span data-stu-id="4d781-121">**Table**</span></span>                    | <span data-ttu-id="4d781-122">Cuenta específica del proveedor</span><span class="sxs-lookup"><span data-stu-id="4d781-122">Specific vendor account</span></span>                     | <span data-ttu-id="4d781-123">1</span><span class="sxs-lookup"><span data-stu-id="4d781-123">1</span></span>               |
| <span data-ttu-id="4d781-124">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="4d781-124">**Group**</span></span>                    | <span data-ttu-id="4d781-125">Grupo de proveedores asignado al proveedor</span><span class="sxs-lookup"><span data-stu-id="4d781-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="4d781-126">2</span><span class="sxs-lookup"><span data-stu-id="4d781-126">2</span></span>               |
| <span data-ttu-id="4d781-127">**Todas**</span><span class="sxs-lookup"><span data-stu-id="4d781-127">**All**</span></span>                      | <span data-ttu-id="4d781-128">En blanco</span><span class="sxs-lookup"><span data-stu-id="4d781-128">Blank</span></span>                                       | <span data-ttu-id="4d781-129">3</span><span class="sxs-lookup"><span data-stu-id="4d781-129">3</span></span>               |

<span data-ttu-id="4d781-130">Si desea que todas las transacciones de proveedores tengan el mismo perfil de contabilización, configure solo un perfil de contabilización con valor **Todas** en el campo **Código de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="4d781-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="4d781-131">Especifique los valores siguientes para configurar su perfil de contabilización.</span><span class="sxs-lookup"><span data-stu-id="4d781-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4d781-132">Campo</span><span class="sxs-lookup"><span data-stu-id="4d781-132">Field</span></span></th>
<th><span data-ttu-id="4d781-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d781-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d781-134"><strong>Perfil de contabilización</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="4d781-135">Permite especificar un código para el perfil de contabilización.</span><span class="sxs-lookup"><span data-stu-id="4d781-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="4d781-136">Por ejemplo, podría crear dos perfiles de registro para obtener una cuenta para saldos de proveedores en la divisa nacional y otra para saldos de proveedores en una divisa extranjera.</span><span class="sxs-lookup"><span data-stu-id="4d781-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="4d781-137">Podría llamar a una cuenta Nacional y a otra Extranjera.</span><span class="sxs-lookup"><span data-stu-id="4d781-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d781-138"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="4d781-139">Permite especificar una descripción del perfil de registro.</span><span class="sxs-lookup"><span data-stu-id="4d781-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d781-140"><strong>Código de cuenta</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="4d781-141">Especificar si el perfil de contabilización se aplica a un proveedor específico, a un grupo de proveedores o a todos los proveedores:</span><span class="sxs-lookup"><span data-stu-id="4d781-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="4d781-142"><strong>Tabla</strong>: el perfil de registro se aplica a un único proveedor.</span><span class="sxs-lookup"><span data-stu-id="4d781-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="4d781-143">Seleccione la cuenta de proveedor en el campo <strong>Número de grupo/cuenta</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d781-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="4d781-144"><strong>Grupo</strong>: el perfil de registro se aplica a un grupo de proveedores.</span><span class="sxs-lookup"><span data-stu-id="4d781-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="4d781-145">Seleccione el grupo de proveedores en el campo <strong>Número de grupo/cuenta</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d781-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="4d781-146"><strong>Todos</strong>: el perfil de registro se aplica a todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="4d781-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="4d781-147">Deje en blanco el campo <strong>Número de grupo/cuenta</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d781-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d781-148"><strong>Número de grupo/cuenta</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="4d781-149">Si <strong>Tabla</strong> está seleccionada en el campo <strong>Código de cuenta</strong>, seleccione el número de cuenta del proveedor asociado al perfil de registro.</span><span class="sxs-lookup"><span data-stu-id="4d781-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="4d781-150">Si la opción <strong>Grupo</strong> está seleccionada, seleccione un grupo de proveedores.</span><span class="sxs-lookup"><span data-stu-id="4d781-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="4d781-151">Si <strong>Todos</strong> está seleccionado, deje este campo en blanco.</span><span class="sxs-lookup"><span data-stu-id="4d781-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d781-152"><strong>Extracto de cuenta</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="4d781-153">Seleccionar la cuenta contable que se usará como la cuenta de resumen para los proveedores con los que está relacionado el perfil de registro.</span><span class="sxs-lookup"><span data-stu-id="4d781-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="4d781-154">Se marcará el parámetro <strong>No permitir entrada manual</strong> para esta cuenta principal.</span><span class="sxs-lookup"><span data-stu-id="4d781-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="4d781-155">Si elimina posteriormente esta cuenta del perfil de contabilización, valide la configuración <strong>No permitir entrada manual</strong> en la página <strong>Cuentas principales</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d781-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="4d781-156"><strong>Nota:</strong> si la opción <strong>Usar definiciones de contabilización</strong> está seleccionada en la página <strong>Parámetros de contabilidad general</strong>, se usa la definición de registro de transacción para facturas de proveedor en lugar de la cuenta de resumen.</span><span class="sxs-lookup"><span data-stu-id="4d781-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d781-157"><strong>Liquidar cuenta</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="4d781-158">Permite seleccionar la cuenta contable de liquidez que se usa para previsiones de flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="4d781-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="4d781-159">Este campo solo está disponible si está habilitada la previsión de flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="4d781-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d781-160"><strong>Pagos de impuestos por adelantado</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="4d781-161">Seleccionar la cuenta para pagos de impuestos que se reciben por adelantado.</span><span class="sxs-lookup"><span data-stu-id="4d781-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="4d781-162"><strong>Nota:</strong> el perfil de contabilización que se usa cuando se marca el pago como un pago por adelantado está seleccionado en el campo Perfil de <strong>contabilización</strong> con el campo <strong>Asiento del diario de anticipos</strong> del área <strong>Impuestos y contabilidad</strong> de la página <strong>Parámetros de proveedores</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d781-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d781-163"><strong>Llegada</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="4d781-164">Seleccionar la cuenta contable en la que se registra la información sobre facturas de proveedores no aprobadas.</span><span class="sxs-lookup"><span data-stu-id="4d781-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="4d781-165">La información se indica en el Diario de registro de facturas.</span><span class="sxs-lookup"><span data-stu-id="4d781-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="4d781-166">Por ejemplo, un usuario escribe información muy básica acerca de las facturas de los proveedores cuando se reciben en el registro de facturas.</span><span class="sxs-lookup"><span data-stu-id="4d781-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="4d781-167">Cuando se registra el registro de facturas, las transacciones se registran en la cuenta especificada aquí y en el campo <strong>Cuenta de contrapartida</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d781-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="4d781-168">Cuando se aprueban las facturas, la deuda se transfiere desde la cuenta de llegadas a la cuenta de resumen del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4d781-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d781-169"><strong>Cuenta de contrapartida</strong></span><span class="sxs-lookup"><span data-stu-id="4d781-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="4d781-170">Seleccionar la cuenta contable que se usa para la compensación de facturas de proveedores no aprobadas actualizadas a través del registro de facturas.</span><span class="sxs-lookup"><span data-stu-id="4d781-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="4d781-171">La cuenta de contrapartida actúa como la cuenta de contrapartida para las transacciones que se registran en las cuentas de llegada.</span><span class="sxs-lookup"><span data-stu-id="4d781-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="4d781-172">Por tanto, la cuenta contiene compras de proveedor que aún no se han aprobado.</span><span class="sxs-lookup"><span data-stu-id="4d781-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="4d781-173">**Restricciones de tablas**</span><span class="sxs-lookup"><span data-stu-id="4d781-173">**Table restrictions**</span></span>

<span data-ttu-id="4d781-174">Para las transacciones que tienen seleccionado el perfil de registro, especifique si las transacciones se liquidarán automáticamente, se calculará el interés y, las cartas de cobro se emitirán.</span><span class="sxs-lookup"><span data-stu-id="4d781-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="4d781-175">También puede seleccionar la cuenta que se usa al cerrar las transacciones que tienen el perfil de contabilización seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4d781-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="4d781-176">Especifique los valores siguientes para configurar su perfil de contabilización</span><span class="sxs-lookup"><span data-stu-id="4d781-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="4d781-177">Campo</span><span class="sxs-lookup"><span data-stu-id="4d781-177">Field</span></span>          | <span data-ttu-id="4d781-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d781-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d781-179">**Liquidación**</span><span class="sxs-lookup"><span data-stu-id="4d781-179">**Settlement**</span></span> | <span data-ttu-id="4d781-180">Seleccione esta opción para habilitar la liquidación automática de las transacciones que tienen este perfil de registro.</span><span class="sxs-lookup"><span data-stu-id="4d781-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="4d781-181">Si esta opción está desactivada, debe liquidar manualmente las transacciones mediante la página **Liquidar transacciones abiertas**.</span><span class="sxs-lookup"><span data-stu-id="4d781-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="4d781-182">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="4d781-182">**Cancel**</span></span>     | <span data-ttu-id="4d781-183">Seleccione esta opción si desea poder cancelar transacciones que tengan este perfil de registro.</span><span class="sxs-lookup"><span data-stu-id="4d781-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="4d781-184">**Cerrar**</span><span class="sxs-lookup"><span data-stu-id="4d781-184">**Close**</span></span>      | <span data-ttu-id="4d781-185">Seleccionar un perfil de registro al que desee cambiar cuando se cierren las transacciones con este perfil de registro.</span><span class="sxs-lookup"><span data-stu-id="4d781-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="4d781-186">Una transacción se considera como cerrada cuando se ha liquidado completamente.</span><span class="sxs-lookup"><span data-stu-id="4d781-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |