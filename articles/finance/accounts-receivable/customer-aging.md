---
title: Informe de vencimiento de clientes
description: El informe de vencimiento de clientes muestra los saldos ordenados por intervalo de fechas o período de vencimiento.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 062e8972c879d770cc4106c2811cd4c16fff0446
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974870"
---
# <a name="customer-aging-report"></a><span data-ttu-id="c0859-103">Informe de vencimiento de clientes</span><span class="sxs-lookup"><span data-stu-id="c0859-103">Customer aging report</span></span> 

<span data-ttu-id="c0859-104">El informe **Vencimiento de clientes** muestra los saldos ordenados por intervalo de fechas o período de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="c0859-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="c0859-105">Cuando genere este informe, se mostrarán los siguientes parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c0859-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="c0859-106">Puede usar estos parámetros para filtrar los datos que se mostrarán en el informe.</span><span class="sxs-lookup"><span data-stu-id="c0859-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="c0859-107">Para obtener más información, consulte [Configurar cobros](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="c0859-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0859-108">Campo</span><span class="sxs-lookup"><span data-stu-id="c0859-108">Field</span></span></p></th>
<th><p><span data-ttu-id="c0859-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0859-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0859-110"><strong>Clasificación de la facturación</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-111">Seleccione una o varias clasificaciones de la facturación para incluirlas en el informe.</span><span class="sxs-lookup"><span data-stu-id="c0859-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="c0859-112">**Nota**: Este control solo está disponible si está seleccionada la clave de configuración del <STRONG>Sector público</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c0859-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0859-113"><strong>Incluir transacciones sin una clasificación de la facturación</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-114">Si esta casilla está activada, todas las transacciones que no tengan una clasificación de la facturación asignada se mostrarán en el informe.</span><span class="sxs-lookup"><span data-stu-id="c0859-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="c0859-115">**Nota**: Este control solo está disponible si está seleccionada la clave de configuración del <STRONG>Sector público</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c0859-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0859-116"><strong>Vencimiento a partir de</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-117">Ingrese la fecha utilizada en el depósito de antigüedad actual.</span><span class="sxs-lookup"><span data-stu-id="c0859-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0859-118"><strong>Saldo a partir de</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-119">Especifique la fecha para la que desea consultar los saldos de cliente.</span><span class="sxs-lookup"><span data-stu-id="c0859-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="c0859-120">Esta fecha también se conoce como una fecha límite para transacciones.</span><span class="sxs-lookup"><span data-stu-id="c0859-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0859-121"><strong>Fecha inicial</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-122">Especifique una fecha que se encuentra en el primer intervalo de períodos o período de vencimiento para incluirla en el informe.</span><span class="sxs-lookup"><span data-stu-id="c0859-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0859-123"><strong>Criterios</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-124">Seleccione el tipo de fecha en la que se basa el informe.</span><span class="sxs-lookup"><span data-stu-id="c0859-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="c0859-125"><strong>Fecha de transacción</strong> - La fecha de registro de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="c0859-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="c0859-126">Por ejemplo, podría ser una fecha de factura que es la base del cálculo de la fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="c0859-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="c0859-127"><strong>Fecha de vencimiento</strong> - La fecha de vencimiento de las transacciones, de acuerdo con las condiciones de pago.</span><span class="sxs-lookup"><span data-stu-id="c0859-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="c0859-128"><strong>Fecha de documento</strong> – Una fecha de documento definida por el usuario que es la base para el cálculo de la fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="c0859-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0859-129"><strong>Definición de período de vencimiento</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-130">Seleccione una definición de período de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="c0859-130">Select an aging period definition.</span></span> <span data-ttu-id="c0859-131">El campo <strong>Intervalo</strong> no se usa si se selecciona una definición de período de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="c0859-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="c0859-132">Las definiciones del período de vencimiento que tienen más de seis períodos de vencimiento no se pueden usar en el informe impreso.</span><span class="sxs-lookup"><span data-stu-id="c0859-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="c0859-133">**Nota:** Puede configurar períodos de envejecimiento en la página <STRONG>Definiciones del período de envejecimiento</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c0859-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0859-134"><strong>Imprimir descripción de período de vencimiento</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-135">Seleccione <strong>Sí</strong> para incluir descripciones del depósito de vencimiento al principio de cada columna de período de vencimiento en el informe.</span><span class="sxs-lookup"><span data-stu-id="c0859-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="c0859-136">Seleccione <strong>No</strong> para imprimir el informe sin encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="c0859-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0859-137"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-138">Defina el período que se usará especificando el número de unidades de días o meses en cada período.</span><span class="sxs-lookup"><span data-stu-id="c0859-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="c0859-139">Por ejemplo, para ver la información de vencimiento por semana, escriba 7 en este campo y seleccione <strong>Día</strong> en el campo <strong>Día/Mes</strong>.</span><span class="sxs-lookup"><span data-stu-id="c0859-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="c0859-140">**Nota**: La información que se especifica en este campo solo se usa si no se ha seleccionado ninguna definición de período de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="c0859-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="c0859-141">De lo contrario, la dirección de impresión se define en la definición del período de envejecimiento.</span><span class="sxs-lookup"><span data-stu-id="c0859-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0859-142"><strong>Día/Mes</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-143">Seleccione la unidad, <strong>Día</strong> o <strong>Mes</strong>, que se usa para definir el período en el campo <strong>Intervalo</strong>.</span><span class="sxs-lookup"><span data-stu-id="c0859-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0859-144"><strong>Dirección de impresión</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-145">Seleccione si desea calcular saldos e imprimir el informe de vencimiento para los períodos pasados o futuros.</span><span class="sxs-lookup"><span data-stu-id="c0859-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="c0859-146">La fechas se evalúan con relación a la fecha seleccionada en el campo <strong>Saldo según</strong>.</span><span class="sxs-lookup"><span data-stu-id="c0859-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="c0859-147">Seleccione <strong>Regresivo</strong> para mostrar la información de períodos pasados.</span><span class="sxs-lookup"><span data-stu-id="c0859-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="c0859-148">Seleccione <strong>Adelante</strong> para mostrar la información de períodos futuros.</span><span class="sxs-lookup"><span data-stu-id="c0859-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>

<span data-ttu-id="c0859-149">**Nota**: La información que se especifica en este campo solo se usa si no se ha seleccionado ninguna definición de período de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="c0859-149">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0859-150"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-151">Se selecciona para mostrar las transacciones que están comprendidas en los saldos que se muestran en el informe.</span><span class="sxs-lookup"><span data-stu-id="c0859-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0859-152"><strong>Incluir importes en la divisa de la transacción</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-153">Se selecciona para incluir importes en la divisa de transacción además de importes en la divisa de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="c0859-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="c0859-154">Si no se activa esta casilla, los importes del informe solo se muestra en la divisa de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="c0859-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0859-155"><strong>Saldo negativo</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-156">Se selecciona para incluir las cuentas de cliente con saldos negativos.</span><span class="sxs-lookup"><span data-stu-id="c0859-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0859-157"><strong>Excluir cuentas de saldo cero</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-158">Se selecciona para excluir las cuentas de cliente con saldo cero.</span><span class="sxs-lookup"><span data-stu-id="c0859-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0859-159"><strong>Ubicación del pago</strong></span><span class="sxs-lookup"><span data-stu-id="c0859-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="c0859-160">Se selecciona para mostrar los pagos que no se han liquidado.</span><span class="sxs-lookup"><span data-stu-id="c0859-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="c0859-161">Se muestran en la primera columna del informe.</span><span class="sxs-lookup"><span data-stu-id="c0859-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>
