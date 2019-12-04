---
title: Espacio de trabajo de pagos de proveedor
description: Este tema proporciona información acerca del espacio de trabajo Pagos a proveedores. El espacio de trabajo Pagos a proveedores muestra la información relacionada con el procesamiento de pagos a proveedores.
author: abruer
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 89ba0d68bd52413328dd583e87b09b01fd523d6f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179857"
---
# <a name="vendor-payments-workspace"></a><span data-ttu-id="03e46-104">Espacio de trabajo de pagos de proveedor</span><span class="sxs-lookup"><span data-stu-id="03e46-104">Vendor payments workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03e46-105">El espacio de trabajo **Pagos a proveedores** muestra la información relacionada con el procesamiento de pagos a proveedores.</span><span class="sxs-lookup"><span data-stu-id="03e46-105">The **Vendor payments** workspace shows information that is related to the processing of vendor payments.</span></span> <span data-ttu-id="03e46-106">Este espacio de trabajo incluye un vista **Mi trabajo** y una página **Análisis** .</span><span class="sxs-lookup"><span data-stu-id="03e46-106">This workspace includes a **My work** view and an **Analytics** page.</span></span> <span data-ttu-id="03e46-107">La vista **Mi trabajo** muestra mosaicos de resumen, cuadrículas de transacciones con proveedores y la información de proveedor relacionada.</span><span class="sxs-lookup"><span data-stu-id="03e46-107">The **My work** view shows summary tiles, vendor transaction grids, and related vendor information.</span></span> <span data-ttu-id="03e46-108">La página **Análisis** utiliza las capacidades de Microsoft Power BI para mostrar las representaciones visuales relacionados con pagos a proveedores.</span><span class="sxs-lookup"><span data-stu-id="03e46-108">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to vendor payments.</span></span>

## <a name="setup-needed-to-view-power-bi-content"></a><span data-ttu-id="03e46-109">Configuración necesaria para ver el contenido de Power BI</span><span class="sxs-lookup"><span data-stu-id="03e46-109">Setup needed to view Power BI content</span></span>

<span data-ttu-id="03e46-110">Es necesario completar la siguiente configuración para que los datos se muestren en los elementos visuales de Power BI **Pagos a proveedores**.</span><span class="sxs-lookup"><span data-stu-id="03e46-110">The following setup needs to be completed for data to display in **Vendor payments** Power BI visuals.</span></span>
1. <span data-ttu-id="03e46-111">Vaya a **Administración del sistema > Configuración > Parámetros del sistema** para establecer **Divisa del sistema** y **Tipo de cambio del sistema**.</span><span class="sxs-lookup"><span data-stu-id="03e46-111">Go to **System administration > Setup > System Parameters** to set **System currency** and **System Exchange Rate**.</span></span>
2. <span data-ttu-id="03e46-112">Vaya a **Contabilidad general > Configuración > Libro mayor** para establecer **Divisa de contabilidad** y **Tipo de cambio**.</span><span class="sxs-lookup"><span data-stu-id="03e46-112">Go to **General Ledger > Setup > Ledger**  to set **Accounting Currency** and **Exchange Rate Type**.</span></span> 
2. <span data-ttu-id="03e46-113">Defina los tipos de cambio entre las Divisas de transacción y la Divisa de contabilidad, la Divisa de contabilidad y la Divisa del sistema.</span><span class="sxs-lookup"><span data-stu-id="03e46-113">Define exchange rates between Transaction currencies and Accounting currency, Accounting currency and System currency.</span></span> <span data-ttu-id="03e46-114">Para ello, vaya a **Contabilidad general > Divisas > Tipos de cambio de divisas**.</span><span class="sxs-lookup"><span data-stu-id="03e46-114">To do this, go to **General Ledger > Currencies > Currency exchange rates**.</span></span>
3. <span data-ttu-id="03e46-115">Vaya a **Administración del sistema > Configuración > Almacén de entidades** para actualizar la medida agregada **VendPaymentBIMeasure**.</span><span class="sxs-lookup"><span data-stu-id="03e46-115">Go to **System administration > Setup > Entity Store** to refresh the **VendPaymentBIMeasure** aggregate measurement.</span></span> 

## <a name="my-work-view"></a><span data-ttu-id="03e46-116">Vista Mi trabajo</span><span class="sxs-lookup"><span data-stu-id="03e46-116">My work view</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="03e46-117">Iconos de resumen</span><span class="sxs-lookup"><span data-stu-id="03e46-117">Summary tiles</span></span>

<span data-ttu-id="03e46-118">Los mosaicos en la sección **Resumen** ofrece una visión general del estado de la información de pago.</span><span class="sxs-lookup"><span data-stu-id="03e46-118">The tiles in the **Summary** section give an overview of the state of your payment information.</span></span> <span data-ttu-id="03e46-119">Puede ver los diarios de pagos que todavía no se han registrado, las facturas vencidas, todos los proveedores, y proveedores que están en espera.</span><span class="sxs-lookup"><span data-stu-id="03e46-119">You can see payment journals that aren't yet posted, invoices that are past due, all vendors, and vendors that are on hold.</span></span> <span data-ttu-id="03e46-120">En la sección **Resumen** , puede crear un nuevo período de pago.</span><span class="sxs-lookup"><span data-stu-id="03e46-120">From the **Summary** section, you can create a new pay run.</span></span>

<span data-ttu-id="03e46-121">La información de la sección **Resumen** es para la empresa con la que tiene firmado un contrato.</span><span class="sxs-lookup"><span data-stu-id="03e46-121">The information in the **Summary** section is for the company that you're signed in to.</span></span>

### <a name="vendor-transactions-grids"></a><span data-ttu-id="03e46-122">Cuadrículas de transacciones con proveedores</span><span class="sxs-lookup"><span data-stu-id="03e46-122">Vendor transactions grids</span></span>

<span data-ttu-id="03e46-123">La sección **Transacciones de proveedor** contiene las cuadrículas que muestran las facturas vencidas y los pagos que no se hayan liquidado.</span><span class="sxs-lookup"><span data-stu-id="03e46-123">The **Vendor transactions** section contains grids that show the invoices that are past due and payments that aren't settled.</span></span> <span data-ttu-id="03e46-124">En la cuadrícula **Factura vencidas** , puede ver el historial de liquidaciones de una factura seleccionada.</span><span class="sxs-lookup"><span data-stu-id="03e46-124">From the **Invoices past due** grid, you can view the settlement history for a selected invoice.</span></span> <span data-ttu-id="03e46-125">En la cuadrícula **Pagos no liquidados** , puede ver el historial de liquidaciones de una factura seleccionada y liquidarla.</span><span class="sxs-lookup"><span data-stu-id="03e46-125">From the **Payments not settled** grid, you can view the settlement history for a selected invoice and settle an invoice.</span></span>

<span data-ttu-id="03e46-126">Los empleados de pagos centralizados pueden utilizar un filtro que aparece en la parte superior de cada cuadrícula para seleccionar una empresa.</span><span class="sxs-lookup"><span data-stu-id="03e46-126">Centralized payment clerks can use a filter that appears at the top of each grid to select a company.</span></span> <span data-ttu-id="03e46-127">La cuadrícula se filtra a continuación de modo que muestre solo las empresas definidas en la jerarquía organizativa de pagos centralizada que el empleado de pagos centralizados tenga derecho a ver.</span><span class="sxs-lookup"><span data-stu-id="03e46-127">The grid is then filtered so that it shows only those companies that are defined in the centralized payment organizational hierarchy that the centralized payment clerk has rights to view.</span></span>

<span data-ttu-id="03e46-128">La ficha **Buscar transacciones** en la sección **Transacciones de proveedor** le permite buscar una transacción de proveedor.</span><span class="sxs-lookup"><span data-stu-id="03e46-128">The **Find transactions** tab in the **Vendor transactions** section lets you search for a vendor transaction.</span></span>

### <a name="related-information"></a><span data-ttu-id="03e46-129">Información relacionada</span><span class="sxs-lookup"><span data-stu-id="03e46-129">Related information</span></span>

<span data-ttu-id="03e46-130">Puede ver el informe **Antigüedad de proveedores** y el informe **Resumen de pago por fecha** mediante los vínculos de la sección **Información relacionada** del espacio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="03e46-130">You can view the **Vendor aging** report and the **Payment summary by date** report by using the links in the **Related information** section of the workspace.</span></span>

## <a name="analytics-page"></a><span data-ttu-id="03e46-131">Página Análisis</span><span class="sxs-lookup"><span data-stu-id="03e46-131">Analytics page</span></span>

<span data-ttu-id="03e46-132">La página **Análisis** proporciona medidas importantes, como facturas de proveedor vencidas y facturas de proveedor que venzan en el futuro.</span><span class="sxs-lookup"><span data-stu-id="03e46-132">The **Analytics** page provides important metrics, such as vendor invoices that are past due and vendor invoices that are due in the future.</span></span> <span data-ttu-id="03e46-133">Esta página contiene nueve páginas de informe.</span><span class="sxs-lookup"><span data-stu-id="03e46-133">This page contains nine report pages.</span></span> <span data-ttu-id="03e46-134">Una página ofrece una visión general, y las otras ocho proporcionan información detallada acerca de medidas de pago a proveedores.</span><span class="sxs-lookup"><span data-stu-id="03e46-134">One page provides an overview, and the other eight pages provide details about Accounts payable payment metrics.</span></span>

<span data-ttu-id="03e46-135">En la tabla siguiente se muestran las visualizaciones que se encuentran disponibles en cada página de informe.</span><span class="sxs-lookup"><span data-stu-id="03e46-135">The following table shows the visualizations that are available on each report page.</span></span>


|            <span data-ttu-id="03e46-136">Página de informes</span><span class="sxs-lookup"><span data-stu-id="03e46-136">Report page</span></span>            |                                                                                                                                                                                <span data-ttu-id="03e46-137">Visualización</span><span class="sxs-lookup"><span data-stu-id="03e46-137">Visualization</span></span>                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     <span data-ttu-id="03e46-138">Visión general de pagos de proveedor</span><span class="sxs-lookup"><span data-stu-id="03e46-138">Vendor payments overview</span></span>      | <ul><li><span data-ttu-id="03e46-139">Facturas vencidas</span><span class="sxs-lookup"><span data-stu-id="03e46-139">Invoices past due</span></span></li><li><span data-ttu-id="03e46-140">Facturas que vencen hoy</span><span class="sxs-lookup"><span data-stu-id="03e46-140">Invoices due today</span></span></li><li><span data-ttu-id="03e46-141">Descuentos aplicados a descuentos perdidos</span><span class="sxs-lookup"><span data-stu-id="03e46-141">Discounts taken to discounts lost</span></span></li><li><span data-ttu-id="03e46-142">Facturas pendientes en el futuro por fecha de descuento por pronto pago</span><span class="sxs-lookup"><span data-stu-id="03e46-142">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="03e46-143">Facturas pendientes en el futuro por fecha de vencimiento</span><span class="sxs-lookup"><span data-stu-id="03e46-143">Invoices due in future by due date</span></span></li><li><span data-ttu-id="03e46-144">Facturas pagadas tarde a las facturas pagadas a tiempo</span><span class="sxs-lookup"><span data-stu-id="03e46-144">Invoices paid late to invoices paid on time</span></span></li><li><span data-ttu-id="03e46-145">Asignación de flujo de trabajo de pagos</span><span class="sxs-lookup"><span data-stu-id="03e46-145">Payment workflow assignment</span></span></li><li><span data-ttu-id="03e46-146">Saldo cliente/proveedor</span><span class="sxs-lookup"><span data-stu-id="03e46-146">Vendor to customer balance</span></span></li><li><span data-ttu-id="03e46-147">Facturas abiertas con el pago en espera</span><span class="sxs-lookup"><span data-stu-id="03e46-147">Open invoices with payment hold</span></span></li></ul> |
|         <span data-ttu-id="03e46-148">Facturas vencidas</span><span class="sxs-lookup"><span data-stu-id="03e46-148">Invoices past due</span></span>         |                                                                                             <ul><li><span data-ttu-id="03e46-149">Facturas vencidas</span><span class="sxs-lookup"><span data-stu-id="03e46-149">Invoices past due</span></span></li><li><span data-ttu-id="03e46-150">Detalles sobre facturas vencidas</span><span class="sxs-lookup"><span data-stu-id="03e46-150">Invoices past due details</span></span></li><li><span data-ttu-id="03e46-151">Total de facturas abiertas</span><span class="sxs-lookup"><span data-stu-id="03e46-151">Total open invoices</span></span></li><li><span data-ttu-id="03e46-152">Facturas vencidas por grupo de proveedores</span><span class="sxs-lookup"><span data-stu-id="03e46-152">Invoices past due per vendor group</span></span></li><li><span data-ttu-id="03e46-153">Facturas vencidas por empresa</span><span class="sxs-lookup"><span data-stu-id="03e46-153">Invoices past due per company</span></span></li></ul>                                                                                              |
|        <span data-ttu-id="03e46-154">Facturas que vencen hoy</span><span class="sxs-lookup"><span data-stu-id="03e46-154">Invoices due today</span></span>         |                                                                                                         <ul><li><span data-ttu-id="03e46-155">Facturas que vencen hoy</span><span class="sxs-lookup"><span data-stu-id="03e46-155">Invoices due today</span></span></li><li><span data-ttu-id="03e46-156">Detalles sobre facturas que vencen hoy</span><span class="sxs-lookup"><span data-stu-id="03e46-156">Invoices due today details</span></span></li><li><span data-ttu-id="03e46-157">Facturas que vencen hoy por empresa</span><span class="sxs-lookup"><span data-stu-id="03e46-157">Invoices due today per company</span></span></li><li><span data-ttu-id="03e46-158">Facturas que vencen hoy por grupo de proveedores</span><span class="sxs-lookup"><span data-stu-id="03e46-158">Invoices due today per vendor group</span></span></li></ul>                                                                                                          |
| <span data-ttu-id="03e46-159">Descuentos aplicados a descuentos perdidos</span><span class="sxs-lookup"><span data-stu-id="03e46-159">Discounts taken to discounts lost</span></span> |                                                                             <ul><li><span data-ttu-id="03e46-160">Descuentos aplicados a descuento perdido</span><span class="sxs-lookup"><span data-stu-id="03e46-160">Discounts taken to discount lost</span></span></li><li><span data-ttu-id="03e46-161">Detalles de descuentos aplicados a descuento perdido</span><span class="sxs-lookup"><span data-stu-id="03e46-161">Discounts taken to discount lost details</span></span></li><li><span data-ttu-id="03e46-162">Descuentos aplicados a descuento perdido por empresa</span><span class="sxs-lookup"><span data-stu-id="03e46-162">Discounts taken to discount lost per company</span></span></li><li><span data-ttu-id="03e46-163">Descuentos aplicados a descuento perdido por grupo de proveedores</span><span class="sxs-lookup"><span data-stu-id="03e46-163">Discounts taken to discount lost per vendor group</span></span></li></ul>                                                                              |
|      <span data-ttu-id="03e46-164">Facturas que vencen en el futuro</span><span class="sxs-lookup"><span data-stu-id="03e46-164">Invoices due in future</span></span>       |                                                 <ul><li><span data-ttu-id="03e46-165">Facturas que vencen en el futuro</span><span class="sxs-lookup"><span data-stu-id="03e46-165">Invoices due in future</span></span></li><li><span data-ttu-id="03e46-166">Detalles de facturas que vencen en el futuro</span><span class="sxs-lookup"><span data-stu-id="03e46-166">Invoices due in future details</span></span></li><li><span data-ttu-id="03e46-167">Facturas que vencen en el futuro por empresa</span><span class="sxs-lookup"><span data-stu-id="03e46-167">Invoices due in future per company</span></span></li><li><span data-ttu-id="03e46-168">Facturas que vencen en el futuro por grupo de proveedores</span><span class="sxs-lookup"><span data-stu-id="03e46-168">Invoices due in future per vendor group</span></span></li><li><span data-ttu-id="03e46-169">Facturas pendientes en el futuro por fecha de descuento por pronto pago</span><span class="sxs-lookup"><span data-stu-id="03e46-169">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="03e46-170">Facturas pendientes en el futuro por fecha de vencimiento</span><span class="sxs-lookup"><span data-stu-id="03e46-170">Invoices due in future by due date</span></span></li></ul>                                                  |
|        <span data-ttu-id="03e46-171">Facturas pagadas tarde</span><span class="sxs-lookup"><span data-stu-id="03e46-171">Invoices paid late</span></span>         |                                                         <ul><li><span data-ttu-id="03e46-172">Facturas pagadas después de vencimiento</span><span class="sxs-lookup"><span data-stu-id="03e46-172">Invoices paid after due date</span></span></li><li><span data-ttu-id="03e46-173">Detalles de facturas pagadas después de vencimiento</span><span class="sxs-lookup"><span data-stu-id="03e46-173">Invoices paid after due date details</span></span></li><li><span data-ttu-id="03e46-174">Facturas pagadas después de vencimiento por empresa</span><span class="sxs-lookup"><span data-stu-id="03e46-174">Invoices paid after due date per company</span></span></li><li><span data-ttu-id="03e46-175">Facturas pagadas después de vencimiento por grupo de proveedores</span><span class="sxs-lookup"><span data-stu-id="03e46-175">Invoices paid after due date per vendor group</span></span></li><li><span data-ttu-id="03e46-176">Facturas pagadas tarde frente a facturas pagadas a tiempo</span><span class="sxs-lookup"><span data-stu-id="03e46-176">Invoices paid late versus invoices paid on time</span></span></li></ul>                                                          |
|         <span data-ttu-id="03e46-177">Flujo de trabajo de pagos</span><span class="sxs-lookup"><span data-stu-id="03e46-177">Payment workflow</span></span>          |                                                                                <ul><li><span data-ttu-id="03e46-178">Instancias de flujo de trabajo de pago a proveedores</span><span class="sxs-lookup"><span data-stu-id="03e46-178">Vendor payment workflow instances</span></span></li><li><span data-ttu-id="03e46-179">Instancias de flujo de trabajo de pago a proveedores por responsable</span><span class="sxs-lookup"><span data-stu-id="03e46-179">Vendor payment workflow instances per approver</span></span></li><li><span data-ttu-id="03e46-180">Instancias de flujo de trabajo de pago a proveedores por empresa</span><span class="sxs-lookup"><span data-stu-id="03e46-180">Vendor payment workflow instances per company</span></span></li><li><span data-ttu-id="03e46-181">Promedio días en el flujo de trabajo por responsable</span><span class="sxs-lookup"><span data-stu-id="03e46-181">Average days in workflow by approver</span></span></li></ul>                                                                                |
|    <span data-ttu-id="03e46-182">Saldo cliente/proveedor</span><span class="sxs-lookup"><span data-stu-id="03e46-182">Vendor to customer balance</span></span>     |                                                                                                                   <ul><li><span data-ttu-id="03e46-183">Saldo cliente/proveedor</span><span class="sxs-lookup"><span data-stu-id="03e46-183">Vendor to customer balance</span></span></li><li><span data-ttu-id="03e46-184">Saldo cliente/proveedor por empresa</span><span class="sxs-lookup"><span data-stu-id="03e46-184">Vendor to customer balance per company</span></span></li><li><span data-ttu-id="03e46-185">Detalles del saldo cliente/proveedor</span><span class="sxs-lookup"><span data-stu-id="03e46-185">Vendor to customer balance details</span></span></li></ul>                                                                                                                    |
|    <span data-ttu-id="03e46-186">Facturas con el pago en espera</span><span class="sxs-lookup"><span data-stu-id="03e46-186">Invoices with payment hold</span></span>     |                                                                                         <ul><li><span data-ttu-id="03e46-187">Facturas con el pago en espera</span><span class="sxs-lookup"><span data-stu-id="03e46-187">Invoices with payment hold</span></span></li><li><span data-ttu-id="03e46-188">Detalles sobre facturas con el pago en espera</span><span class="sxs-lookup"><span data-stu-id="03e46-188">Invoices with payment hold details</span></span></li><li><span data-ttu-id="03e46-189">Facturas con el pago en espera por empresa</span><span class="sxs-lookup"><span data-stu-id="03e46-189">Invoices with payment hold per company</span></span></li><li><span data-ttu-id="03e46-190">Facturas con el pago en espera por grupo de proveedores</span><span class="sxs-lookup"><span data-stu-id="03e46-190">Invoices with payment hold per vendor group</span></span></li></ul>                                                                                          |
