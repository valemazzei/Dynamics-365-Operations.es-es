---
title: Informe de declaración DIOT
description: En este tema se proporciona información acerca del informe de declaración DIOT para México.
author: sndray
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DIOTDeclarationConcept_MX, DIOTDeclarationTaxCode_MX, VendTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 79334
ms.assetid: 0cdb4da3-dca8-4e31-8fd5-8a1f785b5104
ms.search.region: Mexico
ms.author: sndray
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df73d43214193f248b5c236b033640da23ff137e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183577"
---
# <a name="diot-declaration-statement"></a><span data-ttu-id="c7ab5-103">Informe de declaración DIOT</span><span class="sxs-lookup"><span data-stu-id="c7ab5-103">DIOT declaration statement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7ab5-104">En este tema se proporciona información acerca del informe de declaración DIOT para México.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-104">This topic provides information about the DIOT declaration statement for Mexico.</span></span>

<span data-ttu-id="c7ab5-105">El informe de la declaración DIOT (declaración informativa de operaciones con proveedores) se usa para informar de transacciones de proveedores a las autoridades fiscales mexicanas (Servicio de Administración Tributaria \[SAT\]).</span><span class="sxs-lookup"><span data-stu-id="c7ab5-105">The DIOT declaration statement (informative declaration of operation with vendors) is used to report vendor transactions to the Mexican tax authorities (Servicio de Administración Tributaria \[SAT\]).</span></span> <span data-ttu-id="c7ab5-106">Puede que tenga que hacerlo si está sujeto a impuestos sobre el valor añadido (IVA).</span><span class="sxs-lookup"><span data-stu-id="c7ab5-106">You might have to do this if you're subject to value-added tax (VAT).</span></span> <span data-ttu-id="c7ab5-107">El informe de la declaración DIOT es un archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-107">The DIOT declaration statement is a text file.</span></span> <span data-ttu-id="c7ab5-108">Puede generar este archivo en Dynamics 365 Finance y, a continuación, importarlo en la herramienta de validación y entrega del gobierno.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-108">You can generate this file in Dynamics 365 Finance, and then import it into the government validation and delivery tool.</span></span> <span data-ttu-id="c7ab5-109">Los informes consolidados y detallados también se generan para fines de control.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-109">Consolidated and detailed reports are also generated for control purposes.</span></span> <span data-ttu-id="c7ab5-110">El informe incluye transacciones que se generaron de los pedidos de compra, los diarios de registro de facturas, los diarios de aprobación de facturas y los diarios de facturas.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-110">The statement includes transactions that were generated from purchase orders, invoice register journals, invoice approval journals, invoice journals.</span></span> <span data-ttu-id="c7ab5-111">También incluye las transacciones de proveedor que se generaron del módulo **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-111">It also includes vendor transactions that were generated from the **Project** module.</span></span> <span data-ttu-id="c7ab5-112">Además, puede incluir transacciones abiertas o transacciones liquidadas.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-112">Additionally, you can include open transactions or settled transactions.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7ab5-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7ab5-113">Prerequisites</span></span>
<span data-ttu-id="c7ab5-114">Debe completar la configuración siguiente para poder generar el archivo de texto de DIOT o informes relacionados:</span><span class="sxs-lookup"><span data-stu-id="c7ab5-114">You must complete the following setup before you can generate the DIOT text file or related reports:</span></span>

1.  <span data-ttu-id="c7ab5-115">Especifique los números o los id. de registro de impuestos para la entidad jurídica.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-115">Enter tax registration IDs or numbers for your legal entity.</span></span>
2.  <span data-ttu-id="c7ab5-116">Permite especificar información de impuestos para proveedores.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-116">Enter tax information for vendors.</span></span>

## <a name="tax-information-for-unmanaged-vendors"></a><span data-ttu-id="c7ab5-117">Información de impuestos para proveedores no administrados</span><span class="sxs-lookup"><span data-stu-id="c7ab5-117">Tax information for unmanaged vendors</span></span>
<span data-ttu-id="c7ab5-118">Los proveedores no administrados son proveedores que no tienen sus detalles registrados como cuentas de proveedor en Finance.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-118">Unmanaged vendors are vendors that don't have their details registered as vendor accounts in Finance.</span></span> <span data-ttu-id="c7ab5-119">Cuando se registra una transacción de compra para este tipo de proveedor, puede seleccionar cualquier cuenta contable diferente de la cuenta de proveedor.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-119">When a purchase transaction is registered for this type of vendor, you can select any ledger account other than the vendor account.</span></span> <span data-ttu-id="c7ab5-120">Dado que todas las transacciones de compras se incluyen en el informe de la declaración DIOT, las transacciones de compras para los proveedores no administrados también requieren los id. de impuestos (RFC o CURP), el tipo de operación y otra información adicional.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-120">Because all purchase transactions are included in the DIOT declaration statement, purchase transactions for unmanaged vendors also require tax registration IDs (RFC or CURP), the type of operation, and other additional information.</span></span> <span data-ttu-id="c7ab5-121">Para los proveedores habituales, puede definir información adicional en la página **Proveedores**.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-121">For regular vendors, you can define additional information on the **Vendors** page.</span></span> <span data-ttu-id="c7ab5-122">Sin embargo, no puede hacerlo para proveedores no administrados.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-122">However, you can't do this for unmanaged vendors.</span></span> <span data-ttu-id="c7ab5-123">Para capturar la información fiscal necesaria para proveedores no administrados, puede especificar información adicional en el nivel de la transacción en las siguientes transacciones de diario cuando no se identifique la cuenta de proveedor:</span><span class="sxs-lookup"><span data-stu-id="c7ab5-123">To capture the required tax information for unmanaged vendors, you can enter additional information at the transaction level in the following journal transactions when the vendor account isn't identified:</span></span>

-   <span data-ttu-id="c7ab5-124">Diario de facturas</span><span class="sxs-lookup"><span data-stu-id="c7ab5-124">Invoice journal</span></span>
-   <span data-ttu-id="c7ab5-125">Registro de facturas</span><span class="sxs-lookup"><span data-stu-id="c7ab5-125">Invoice register</span></span>
-   <span data-ttu-id="c7ab5-126">Diario de gastos</span><span class="sxs-lookup"><span data-stu-id="c7ab5-126">Expense journal</span></span>

<span data-ttu-id="c7ab5-127">Para definir códigos de impuestos para que los campos de información adicional estén disponibles para un proveedor no administrados en transacciones de diario, debe especificar un código de impuestos que se ha configurado para permitir información adicional en el diario.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-127">To define sales tax codes to make additional information fields available for an unmanaged vendor in journal transactions, you must specify a sales tax code that was set up to allow for additional information in the journal.</span></span>

## <a name="diot-report-configuration"></a><span data-ttu-id="c7ab5-128">Configuración de informe DIOT</span><span class="sxs-lookup"><span data-stu-id="c7ab5-128">DIOT report configuration</span></span>
<span data-ttu-id="c7ab5-129">En esta sección se describe cómo definir los conceptos y vincular los códigos de impuestos que se requieren para generar el informe de la declaración DIOT.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-129">This section describes how to define the concepts and attach the sales tax codes that are required to generate the DIOT declaration statement.</span></span> <span data-ttu-id="c7ab5-130">En Finance, un concepto representa los importes de transacción de compras que se agrupan en distintos porcentajes de IVA, según lo especificado por las autoridades fiscales de México.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-130">In Finance, a concept represents purchase transaction amounts that are grouped under different VAT percentages, as specified by the tax authorities in Mexico.</span></span> <span data-ttu-id="c7ab5-131">En el archivo de texto de DIOT, los importes totales se agrupan para cada proveedor, en función de los conceptos definidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-131">In the DIOT text file, the total amounts are grouped for each vendor, based on the concepts that were previously defined.</span></span> <span data-ttu-id="c7ab5-132">Estos conceptos se notifican en las columnas 8 al 22 del formato de diseño de DIOT.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-132">These concepts are reported in columns 8 through 22 of the DIOT layout format.</span></span> <span data-ttu-id="c7ab5-133">Las demás columnas del informe se rellenan automáticamente en función de la información del proveedor como RFC, tipo de operación y otros datos relacionados.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-133">The other columns of the report are automatically filled in based on vendor information such as the RFC, type of operation, and other related data.</span></span>

### <a name="example-of-concepts"></a><span data-ttu-id="c7ab5-134">Ejemplo de conceptos</span><span class="sxs-lookup"><span data-stu-id="c7ab5-134">Example of concepts</span></span>

| <span data-ttu-id="c7ab5-135">Id. de concepto</span><span class="sxs-lookup"><span data-stu-id="c7ab5-135">Concept ID</span></span> | <span data-ttu-id="c7ab5-136">Descripción del concepto</span><span class="sxs-lookup"><span data-stu-id="c7ab5-136">Concept description</span></span>                               | <span data-ttu-id="c7ab5-137">Posición de columna en el archivo de texto (número de pedido)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-137">Column position in the text file (Order number)</span></span> |
|------------|---------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="c7ab5-138">1</span><span class="sxs-lookup"><span data-stu-id="c7ab5-138">1</span></span>          | <span data-ttu-id="c7ab5-139">El importe base de las compras con el 16 % de IVA (liquidado)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-139">The base amount of purchases at VAT 16% (settled)</span></span> | <span data-ttu-id="c7ab5-140">8</span><span class="sxs-lookup"><span data-stu-id="c7ab5-140">8</span></span>                                               |
| <span data-ttu-id="c7ab5-141">2</span><span class="sxs-lookup"><span data-stu-id="c7ab5-141">2</span></span>          | <span data-ttu-id="c7ab5-142">El importe base de las compras con el 15 % de IVA (liquidado)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-142">The base amount of purchases at VAT 15% (settled)</span></span> | <span data-ttu-id="c7ab5-143">9</span><span class="sxs-lookup"><span data-stu-id="c7ab5-143">9</span></span>                                               |
| <span data-ttu-id="c7ab5-144">3</span><span class="sxs-lookup"><span data-stu-id="c7ab5-144">3</span></span>          | <span data-ttu-id="c7ab5-145">Importe de IVA no recuperable del 16 % o el 15 %</span><span class="sxs-lookup"><span data-stu-id="c7ab5-145">VAT amount non recoverable at 16% or 15%</span></span>          | <span data-ttu-id="c7ab5-146">10</span><span class="sxs-lookup"><span data-stu-id="c7ab5-146">10</span></span>                                              |

<span data-ttu-id="c7ab5-147">Puede crear nuevos conceptos en la página **Declaración DIOT**.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-147">You can create new concepts on the **DIOT declaration** page.</span></span> <span data-ttu-id="c7ab5-148">Sin embargo, solo puede crear 15 conceptos.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-148">However, you can create only 15 concepts.</span></span> <span data-ttu-id="c7ab5-149">El primer concepto debe ser el número de pedido 8 y el último debe ser el número de pedido 22.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-149">The first concept should be order number 8 and the last should be order number 22.</span></span> <span data-ttu-id="c7ab5-150">Puede empezar a crear los conceptos con otro pedido, pero debe completar todos (del 8 al 22) para evitar incoherencias en la herramienta de validación del gobierno.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-150">You can start to create the concepts in a different order, but you must complete all of them (8 through 22) to prevent inconsistencies in the government validation tool.</span></span> <span data-ttu-id="c7ab5-151">Para cada concepto, debe especificar un tipo de columna.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-151">For each concept, you must specify a column type.</span></span> <span data-ttu-id="c7ab5-152">Especifique un tipo de columna de **Ninguno** si se ha quedado en desuso la columna.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-152">Specify a column type of **None** if the column has been deprecated.</span></span> <span data-ttu-id="c7ab5-153">Algunas columnas ya no se aplican y se deben notifica con un importe **0,00**.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-153">Some columns no longer apply and must be reported with a **0,00** amount.</span></span> <span data-ttu-id="c7ab5-154">Si la casilla no está activada, el informe de declaración DIOT muestra el importe neto completo o el importe de impuestos.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-154">If the check box isn't selected, the DIOT declaration statement shows the complete net amount or the tax amount.</span></span> <span data-ttu-id="c7ab5-155">Además, para cada columna, puede indicar el porcentaje no deducible del importe neto o el importe de impuestos que se muestra en el informe de declaración DIOT.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-155">Additionally, for each column, you can indicate the non-deductible percentage of the net amount or tax amount that is shown in the DIOT declaration statement.</span></span>

#### <a name="example"></a><span data-ttu-id="c7ab5-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ab5-156">Example</span></span>

<span data-ttu-id="c7ab5-157">Si el importe neto o el importe de impuestos es 10000.00 pesos, y el porcentaje del importe no deducible es el 30 por ciento, el informe muestra solo el 30 por ciento de 10.000,00 pesos, o 3.000,00 pesos.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-157">If the net amount or tax amount is 10000.00 pesos, and the percentage of the non-deductible amount is 30 percent, the report displays only 30 percent of 10,000.00 pesos, or 3,000.00 pesos.</span></span> <span data-ttu-id="c7ab5-158">Use el botón **Código de impuestos** para vincular uno o más códigos de impuestos a un concepto.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-158">Use the **Sales tax code** button to attach one or more sales tax codes to a concept.</span></span>

## <a name="generate-the-diot-declaration-statement"></a><span data-ttu-id="c7ab5-159">Generar el informe de declaración DIOT</span><span class="sxs-lookup"><span data-stu-id="c7ab5-159">Generate the DIOT declaration statement</span></span>
<span data-ttu-id="c7ab5-160">Para generar el informe de declaración DIOT, haga clic en **Impuestos** &gt; **Declaraciones** &gt; **Impuestos** &gt; **Generar la DIOT**.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-160">To generate the DIOT declaration statement, click **Tax** &gt; **Declarations** &gt; **Sales tax** &gt; **Generate DIOT declaration**.</span></span> <span data-ttu-id="c7ab5-161">Debe especificar o seleccionar la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-161">You must specify or select the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7ab5-162">Campo</span><span class="sxs-lookup"><span data-stu-id="c7ab5-162">Field</span></span></th>
<th><span data-ttu-id="c7ab5-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7ab5-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7ab5-164">Periodo de liquidación no realizado</span><span class="sxs-lookup"><span data-stu-id="c7ab5-164">Unrealized settlement period</span></span></td>
<td><span data-ttu-id="c7ab5-165">Seleccione un período de liquidación no realizado.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-165">Select the unrealized settlement period.</span></span> <span data-ttu-id="c7ab5-166">Este es el período que se usa en la configuración de códigos de impuestos para impuestos condicionales.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-166">This is the period that is used in the configuration of sales tax codes for conditional taxes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7ab5-167">Periodo de liquidación realizado</span><span class="sxs-lookup"><span data-stu-id="c7ab5-167">Realized settlement period</span></span></td>
<td><span data-ttu-id="c7ab5-168">Seleccione el período de liquidación realizado.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-168">Select the realized settlement period.</span></span> <span data-ttu-id="c7ab5-169">Este es el período que se usa en la configuración de códigos de impuestos.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-169">This is the period that is used in the configuration of sales tax codes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7ab5-170">Fecha inicial</span><span class="sxs-lookup"><span data-stu-id="c7ab5-170">From date</span></span></td>
<td><span data-ttu-id="c7ab5-171">Seleccione el período.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-171">Select the period.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7ab5-172">Tipo de informe de DIOT</span><span class="sxs-lookup"><span data-stu-id="c7ab5-172">DIOT report type</span></span></td>
<td><span data-ttu-id="c7ab5-173">Seleccione <strong>Consolidado</strong> o <strong>Detallado</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-173">Select either <strong>Consolidated</strong> or <strong>Detailed</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7ab5-174">Incluir transacciones</span><span class="sxs-lookup"><span data-stu-id="c7ab5-174">Include transactions</span></span></td>
<td><span data-ttu-id="c7ab5-175">Seleccione las opciones disponibles:</span><span class="sxs-lookup"><span data-stu-id="c7ab5-175">Select the available options:</span></span>
<ul>
<li><span data-ttu-id="c7ab5-176"><strong>No realizado</strong>: incluya solo las transacciones de compras no realizadas (las transacciones que no se liquidaron ni crearon en el período).</span><span class="sxs-lookup"><span data-stu-id="c7ab5-176"><strong>Unrealized</strong> – Include only the unrealized purchase transactions (transactions that were not settled and created in the period).</span></span></li>
<li><span data-ttu-id="c7ab5-177"><strong>Realizado</strong>: incluya solo las transacciones de compras realizadas (las transacciones que se liquidaron en el período).</span><span class="sxs-lookup"><span data-stu-id="c7ab5-177"><strong>Realized</strong> – Include only the realized purchase transactions (transaction that were settled in the period).</span></span></li>
<li><span data-ttu-id="c7ab5-178">Ambos</span><span class="sxs-lookup"><span data-stu-id="c7ab5-178">Both</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7ab5-179">Generar archivo</span><span class="sxs-lookup"><span data-stu-id="c7ab5-179">Generate file</span></span></td>
<td><span data-ttu-id="c7ab5-180">Seleccione <strong>Sí</strong> para generar el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-180">Select <strong>Yes</strong> to generate the text file.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7ab5-181">Porcentaje de operaciones de proveedores globales</span><span class="sxs-lookup"><span data-stu-id="c7ab5-181">Percentage of global vendor operations</span></span></td>
<td><span data-ttu-id="c7ab5-182">Escriba un porcentaje del importe de la transacción de proveedor total, según el cual el proveedor se identifica como un proveedor <strong>Global</strong> o <strong>Local</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-182">Enter a percentage of the total vendor transaction amount, based on which the vendor is identified as a <strong>Global</strong> or <strong>Local</strong> vendor.</span></span> <span data-ttu-id="c7ab5-183">Sin embargo, en la página <strong>Proveedores</strong>, en la ficha desplegable <strong>Factura y entrega</strong>, se debe especificar <strong>15: proveedor nacional/global</strong> para el proveedor en el campo <strong>Tipo de proveedor</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-183">However, on the <strong>Vendors</strong> page, on the <strong>Invoice and delivery</strong> FastTab, <strong>15:domestic/global vendor</strong> must be specified for the vendor in the <strong>Type of vendor</strong> field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7ab5-184">Límite superior</span><span class="sxs-lookup"><span data-stu-id="c7ab5-184">Upper limit</span></span></td>
<td><span data-ttu-id="c7ab5-185">Especifique el importe del umbral superior para el proveedor global.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-185">Enter the upper threshold amount for the global vendor.</span></span> <span data-ttu-id="c7ab5-186">Para un proveedor global, el importe del pago total que se debe declarar es inferior o igual al valor de este campo.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-186">For a global vendor, the total payment amount that must be declared is less than or equal to the value in this field.</span></span> <span data-ttu-id="c7ab5-187">Para un proveedor nacional, el importe del pago total que se debe declarar es superior al valor de este campo.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-187">For a domestic vendor, the total payment amount that must be declared is more than the value in this field.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c7ab5-188">En el informe de declaración DIOT, los importes tienen signos positivos o negativas, en función del tipo de importe que se especifica para la transacción de compras.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-188">In the DIOT declaration statement, the amounts have either positive or negative signs, depending on the amount type that is entered for the purchase transaction.</span></span> <span data-ttu-id="c7ab5-189">Consulte la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7ab5-189">See the following table.</span></span>

| <span data-ttu-id="c7ab5-190">Tipo de importe en la transacción de compra</span><span class="sxs-lookup"><span data-stu-id="c7ab5-190">Amount type in the purchase transaction</span></span>      | <span data-ttu-id="c7ab5-191">Signo mostrado en el DIOT</span><span class="sxs-lookup"><span data-stu-id="c7ab5-191">Sign displayed in the DIOT</span></span> |
|----------------------------------------------|----------------------------|
| <span data-ttu-id="c7ab5-192">Importe de crédito</span><span class="sxs-lookup"><span data-stu-id="c7ab5-192">Credit amount</span></span>                                | <span data-ttu-id="c7ab5-193">Signo más (+)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-193">Plus sign (+)</span></span>              |
| <span data-ttu-id="c7ab5-194">Importe de débito</span><span class="sxs-lookup"><span data-stu-id="c7ab5-194">Debit amount</span></span>                                 | <span data-ttu-id="c7ab5-195">Signo menos (–)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-195">Minus sign (–)</span></span>             |
| <span data-ttu-id="c7ab5-196">Importe de crédito con importe de impuestos positivo</span><span class="sxs-lookup"><span data-stu-id="c7ab5-196">Credit amount with positive-sales tax amount</span></span> | <span data-ttu-id="c7ab5-197">Signo más (+)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-197">Plus sign (+)</span></span>              |
| <span data-ttu-id="c7ab5-198">Importe de crédito con importe de impuestos negativo</span><span class="sxs-lookup"><span data-stu-id="c7ab5-198">Credit amount with negative-sales tax amount</span></span> | <span data-ttu-id="c7ab5-199">Signo menos (–)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-199">Minus sign (–)</span></span>             |
| <span data-ttu-id="c7ab5-200">Importe de débito con importe de impuestos positivo</span><span class="sxs-lookup"><span data-stu-id="c7ab5-200">Debit amount with positive-sales tax amount</span></span>  | <span data-ttu-id="c7ab5-201">Signo menos (–)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-201">Minus sign (–)</span></span>             |
| <span data-ttu-id="c7ab5-202">Importe de débito con importe de impuestos negativo</span><span class="sxs-lookup"><span data-stu-id="c7ab5-202">Debit amount with negative-sales tax amount</span></span>  | <span data-ttu-id="c7ab5-203">Signo más (+)</span><span class="sxs-lookup"><span data-stu-id="c7ab5-203">Plus sign (+)</span></span>              |




