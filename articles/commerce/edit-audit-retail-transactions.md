---
title: Editar y auditar transacciones de tienda
description: En este tema se describe la funcionalidad de editar y auditar transacciones de tienda.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004398"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="7e996-103">Editar y auditar transacciones de tienda</span><span class="sxs-lookup"><span data-stu-id="7e996-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="7e996-104">Los clientes de Dynamics 365 Commerce usan aplicaciones de punto de venta (PDV) de primera entidad así como de terceros.</span><span class="sxs-lookup"><span data-stu-id="7e996-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="7e996-105">Con la aplicación de PDV de primera entidad, las transacciones de tienda se incluyen en Headquarters desde los canales a través de un proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="7e996-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="7e996-106">Con aplicaciones de terceros, las transacciones se incluyen en Headquarters mediante la integración.</span><span class="sxs-lookup"><span data-stu-id="7e996-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="7e996-107">En ambos casos, después de que las transacciones se incluyan en Headquarters, se debe ejecutar un proceso de comprobación de coherencia que ejecute varias validaciones en las transacciones para que solo las transacciones validadas correctamente se incluyan en el extracto que se registrará en Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7e996-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="7e996-108">Las transacciones de Commerce producen un error en la validación por varios motivos.</span><span class="sxs-lookup"><span data-stu-id="7e996-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="7e996-109">Por ejemplo, un error en el código de integración o un error en la aplicación de PDV puede producir datos incoherentes, o un error de usuario, como la eliminación de un producto después de sincronizarse al canal o el cierre de un período fiscal sin registrar las transacciones para ese período puede producir datos incoherentes.</span><span class="sxs-lookup"><span data-stu-id="7e996-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="7e996-110">Aunque estas transacciones se marcan y excluyen de los extractos, las transacciones pueden interrumpir el proceso diario de un cliente de registrar las ventas diarias en las operaciones financieras.</span><span class="sxs-lookup"><span data-stu-id="7e996-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="7e996-111">En Commerce, podrá editar las transacciones comerciales específicas que causaron un error en la validación durante el mantenimiento de la auditoría de todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="7e996-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="7e996-112">Edición y auditar transacciones</span><span class="sxs-lookup"><span data-stu-id="7e996-112">Edit and audit transactions</span></span>

<span data-ttu-id="7e996-113">En Retail versión 10.0.5, las transacciones de pago al contado sin entrega al domicilio como ventas y devoluciones son las únicas transacciones que se pueden editar.</span><span class="sxs-lookup"><span data-stu-id="7e996-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="7e996-114">No se admite la edición de pedidos de cliente o en línea.</span><span class="sxs-lookup"><span data-stu-id="7e996-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="7e996-115">En Retail versión 10.0.6 y posterior, también se admite la edición de transacciones de gestión de efectivo.</span><span class="sxs-lookup"><span data-stu-id="7e996-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="7e996-116">Instale el complemento de Excel de Dynamics.</span><span class="sxs-lookup"><span data-stu-id="7e996-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="7e996-117">Vaya al espacio de trabajo **Operaciones financieras de tienda**.</span><span class="sxs-lookup"><span data-stu-id="7e996-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="7e996-118">La ventana **Errores de validación de transacciones** ofrece una vista previamente filtrada del formulario de transacción que generó un error en una o más de las reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="7e996-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="7e996-119">Abra el formulario.</span><span class="sxs-lookup"><span data-stu-id="7e996-119">Open the form.</span></span> <span data-ttu-id="7e996-120">Haga clic en el registro que generó un error en la validación, haga clic en **Complemento de Office** y, a continuación, en **Editar transacción seleccionada**.</span><span class="sxs-lookup"><span data-stu-id="7e996-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="7e996-121">Se abre un archivo de Excel con los detalles de la transacción seleccionada, con las siguientes hojas de cálculo:</span><span class="sxs-lookup"><span data-stu-id="7e996-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="7e996-122">Líneas: esta hoja de cálculo tiene las líneas de productos y encabezado y los datos relacionados para la transacción.</span><span class="sxs-lookup"><span data-stu-id="7e996-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="7e996-123">Pagos: esta hoja de cálculo tiene los detalles de las líneas de pago para la transacción.</span><span class="sxs-lookup"><span data-stu-id="7e996-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="7e996-124">Descuentos: esta hoja de cálculo tiene los detalles relacionados con descuentos para la transacción.</span><span class="sxs-lookup"><span data-stu-id="7e996-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="7e996-125">Impuestos: esta hoja de cálculo tiene los detalles relacionados con impuestos para la transacción.</span><span class="sxs-lookup"><span data-stu-id="7e996-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="7e996-126">Gastos: esta hoja de cálculo tiene los detalles relacionados con gastos para la transacción.</span><span class="sxs-lookup"><span data-stu-id="7e996-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="7e996-127">En el archivo de Excel, modifique los campos adecuados y, a continuación, cargue los datos de nuevo en Headquarters usando la funcionalidad de publicación del complemento de Excel de Dynamics.</span><span class="sxs-lookup"><span data-stu-id="7e996-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="7e996-128">Una vez publicados, los cambios se reflejarán en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7e996-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="7e996-129">Durante la publicación, no se realizará ninguna validación en los cambios que hagan los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7e996-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="7e996-130">Para ver una traza de auditoría completa de los cambios, haga clic en **Ver traza de auditoría** en el encabezado **Transacción comercial** para los cambios de nivel de encabezado y en la sección y el registro pertinentes de la página de transacción adecuada.</span><span class="sxs-lookup"><span data-stu-id="7e996-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="7e996-131">Por ejemplo, todos los cambios relativos a las líneas de ventas serán visibles en la página **Transacciones de venta**, los cambios relativos a los pagos serán visibles en la página **Transacciones de pago**, etc. Los detalles de auditoría que se mantienen para los cambios son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e996-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="7e996-132">Fecha y hora de modificación</span><span class="sxs-lookup"><span data-stu-id="7e996-132">Modified date and time</span></span>
   - <span data-ttu-id="7e996-133">Campo</span><span class="sxs-lookup"><span data-stu-id="7e996-133">Field</span></span> 
   - <span data-ttu-id="7e996-134">Valor anterior</span><span class="sxs-lookup"><span data-stu-id="7e996-134">Old value</span></span>
   - <span data-ttu-id="7e996-135">Nuevo valor</span><span class="sxs-lookup"><span data-stu-id="7e996-135">New value</span></span>
   - <span data-ttu-id="7e996-136">Modificado por</span><span class="sxs-lookup"><span data-stu-id="7e996-136">Modified by</span></span>

6. <span data-ttu-id="7e996-137">Después de que se realicen y se publiquen los cambios, ejecute la opción **Validar transacciones de la tienda** de nuevo para validar que los cambios realizados son coherentes y válidos.</span><span class="sxs-lookup"><span data-stu-id="7e996-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="7e996-138">Solo puede editar las transacciones que generaron un error de validación.</span><span class="sxs-lookup"><span data-stu-id="7e996-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="7e996-139">Si desea editar las transacciones que pasaron la validación, cambie el estado de la validación de la transacción que desee cambiar a **Error** o **Ninguno** y, a continuación, podrá editarlo.</span><span class="sxs-lookup"><span data-stu-id="7e996-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="7e996-140">Edición en masa de transacciones</span><span class="sxs-lookup"><span data-stu-id="7e996-140">Bulk edit transactions</span></span>

<span data-ttu-id="7e996-141">En Retail versión 10.0.6 y posterior, se admite la opción de edición masiva de transacciones en un nivel de extracto.</span><span class="sxs-lookup"><span data-stu-id="7e996-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="7e996-142">Use el complemento de Excel para abrir un extracto que tenga transacciones que desee modificar con los pasos del 1 al 3 anteriores.</span><span class="sxs-lookup"><span data-stu-id="7e996-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="7e996-143">Elija una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e996-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="7e996-144">**Editar transacciones de pago al contado sin entrega a domicilio**.</span><span class="sxs-lookup"><span data-stu-id="7e996-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="7e996-145">Esta opción le permite editar todas las transacciones de pago al contado sin entrega a domicilio incluidas en el extracto.</span><span class="sxs-lookup"><span data-stu-id="7e996-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="7e996-146">Las siguientes hojas de cálculo Excel están disponibles.</span><span class="sxs-lookup"><span data-stu-id="7e996-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="7e996-147">**Transacción**: esta hoja de cálculo tiene toda la información de nivel de encabezado para las transacciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="7e996-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="7e996-148">**Transacción de venta**: esta hoja de cálculo tiene toda la información de nivel de líneas para las transacciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="7e996-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="7e996-149">**Transacciones de pago**: esta hoja de cálculo tiene toda la información de líneas de pago para las transacciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="7e996-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="7e996-150">**Transacciones de descuento**: esta hoja de cálculo tiene toda la información de líneas de pago para las transacciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="7e996-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="7e996-151">**Transacciones de impuestos**: esta hoja de cálculo tiene toda la información de líneas de impuestos para las transacciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="7e996-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="7e996-152">**Transacciones de gastos**: esta hoja de cálculo tiene toda la información de líneas de gastos para las transacciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="7e996-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="7e996-153">**Editar transacciones de administración de flujos de efectivo**.</span><span class="sxs-lookup"><span data-stu-id="7e996-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="7e996-154">Esta opción le permite editar todas las transacciones de administración de flujos de efectivo incluidas en el extracto.</span><span class="sxs-lookup"><span data-stu-id="7e996-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="7e996-155">Las siguientes hojas de cálculo Excel están disponibles.</span><span class="sxs-lookup"><span data-stu-id="7e996-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="7e996-156">**Transacción**: esta hoja de cálculo tiene toda la información de nivel de encabezado para las transacciones de administración de flujos de efectivo.</span><span class="sxs-lookup"><span data-stu-id="7e996-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="7e996-157">**Transacciones bancarias de forma de pago realizadas**: esta hoja de cálculo tiene todos los detalles de transacción de ingreso bancario.</span><span class="sxs-lookup"><span data-stu-id="7e996-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="7e996-158">**Transacciones de forma de pago en caja fuerte**: esta hoja de cálculo tiene todos los detalles de transacción de ingreso seguro.</span><span class="sxs-lookup"><span data-stu-id="7e996-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="7e996-159">**Declaración por forma de pago**: esta hoja de cálculo tiene todos los detalles de declaración por forma de pago.</span><span class="sxs-lookup"><span data-stu-id="7e996-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="7e996-160">**Transacción de ingresos y gastos**: esta hoja de cálculo tiene todos los detalles de línea de transacción de ingresos y gastos.</span><span class="sxs-lookup"><span data-stu-id="7e996-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="7e996-161">**Transacciones de pago**: esta hoja de cálculo tiene toda la información relacionada con pagos para la operación **Pagar factura** así como la transacción de ingresos y gastos.</span><span class="sxs-lookup"><span data-stu-id="7e996-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="7e996-162">Las validaciones no se realizan al publicar transacciones editadas de forma masiva.</span><span class="sxs-lookup"><span data-stu-id="7e996-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="7e996-163">Debe asegurarse que todas las ediciones son precisas y de que se mantiene la fidelidad de los datos en todas las hojas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7e996-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="7e996-164">Por ejemplo, si desea cambiar la fecha de transacción para administrar los escenarios donde el período fiscal o de inventario para las transacciones abiertas está cerrado, debe cambiar la fecha en todas las hojas de cálculo de Excel que tienen la columna **Fecha de negocio**.</span><span class="sxs-lookup"><span data-stu-id="7e996-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="7e996-165">Para validar transacciones después de que se hayan editado, puede usar la página **Revalidar transacciones** en la página **Extractos**.</span><span class="sxs-lookup"><span data-stu-id="7e996-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>