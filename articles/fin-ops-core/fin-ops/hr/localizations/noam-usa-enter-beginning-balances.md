---
title: Especificar saldos iniciales de nómina
description: El tema se describen los pasos para especificar los saldos iniciales para los códigos de ganancias, las deducciones, las prestaciones y los impuestos. Esta información tiene valor para que los socios migren o transfieran los datos para una nueva implementación de nóminas desde otro sistema.
author: kherr75
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cab844e190140d2c3b605c9a1490d33a6f383ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179896"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="55dfd-104">Especificar saldos iniciales de nómina</span><span class="sxs-lookup"><span data-stu-id="55dfd-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55dfd-105">El tema se describen los pasos para especificar los saldos iniciales para los códigos de ganancias, las deducciones, las prestaciones y los impuestos.</span><span class="sxs-lookup"><span data-stu-id="55dfd-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="55dfd-106">Esta información tiene valor para que los socios que transfieran los datos para una nueva implementación de nóminas desde otro sistema.</span><span class="sxs-lookup"><span data-stu-id="55dfd-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="55dfd-107">Para prepararse para especificar los saldos iniciales de nóminas, comprobamos la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="55dfd-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="55dfd-108">Los registros de empleados se especificaron y están disponibles en el sistema</span><span class="sxs-lookup"><span data-stu-id="55dfd-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="55dfd-109">Los siguientes datos se configuraron y asignaron a los empleados:</span><span class="sxs-lookup"><span data-stu-id="55dfd-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="55dfd-110">Ciclos y períodos de pago</span><span class="sxs-lookup"><span data-stu-id="55dfd-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="55dfd-111">Códigos de ganancia</span><span class="sxs-lookup"><span data-stu-id="55dfd-111">Earning codes</span></span>
    - <span data-ttu-id="55dfd-112">Impuestos</span><span class="sxs-lookup"><span data-stu-id="55dfd-112">Taxes</span></span>
    - <span data-ttu-id="55dfd-113">Beneficios y deducciones</span><span class="sxs-lookup"><span data-stu-id="55dfd-113">Benefits and deductions</span></span>

- <span data-ttu-id="55dfd-114">La empresa debe haber elegido una fecha en la que saldos iniciales de nóminas se pueden configurar.</span><span class="sxs-lookup"><span data-stu-id="55dfd-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="55dfd-115">La información recopilada se en todas las ganancias, las prestaciones/deducciones, las contribuciones de prestación, los impuestos del empleado y los impuestos del empresario y los importes del año hasta la fecha del sistema heredado.</span><span class="sxs-lookup"><span data-stu-id="55dfd-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="55dfd-116">Cuando vaya a especificar saldos iniciales, considere cómo lo detallados que deben estar los datos.</span><span class="sxs-lookup"><span data-stu-id="55dfd-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="55dfd-117">La mayoría de las empresas especifican un importe único, consolidado del año hasta la fecha.</span><span class="sxs-lookup"><span data-stu-id="55dfd-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="55dfd-118">Sin embargo, si se necesita más información detallada, los saldos se pueden especificar en incrementos trimestrales.</span><span class="sxs-lookup"><span data-stu-id="55dfd-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="55dfd-119">Decidir el nivel de detalle que sea necesario determina cuántos extractos de pago manuales se deben crear para cada trabajador.</span><span class="sxs-lookup"><span data-stu-id="55dfd-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="55dfd-120">Para un solo importe del año hasta la fecha, solo una instrucción manual es necesaria para cada empleado.</span><span class="sxs-lookup"><span data-stu-id="55dfd-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="55dfd-121">Para hacer esto utilice importes de año hasta la fecha desde el extracto de pago final del sistema anterior como el importe especificado en el nuevo sistema de nóminas.</span><span class="sxs-lookup"><span data-stu-id="55dfd-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="55dfd-122">El siguiente ejemplo muestra cómo puede especificar saldos iniciales de nómina de empleados, incluidos los códigos de ganancias, las prestaciones/deducciones y los impuestos.</span><span class="sxs-lookup"><span data-stu-id="55dfd-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="55dfd-123">En un ejemplo del mundo real sólo recibiría un artículo de línea para cada código de ganancias, deducción de prestaciones, contribución de prestaciones impuesto de empleado e impuesto de empresario con el importe especificado siendo el importe del año hasta la fecha.</span><span class="sxs-lookup"><span data-stu-id="55dfd-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="55dfd-124">Mediante esta lista de códigos e importes, siga los pasos para crear una ganancia manual y extracto de pago con la contabilidad deshabilitada para traer saldos iniciales para fines de nómina.</span><span class="sxs-lookup"><span data-stu-id="55dfd-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="55dfd-125">Se deshabilita la contabilidad ya que no se recomienda registrar este extracto de pago de saldo inicial en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="55dfd-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="55dfd-126">Esto se ha realizado en el sistema heredado y pasará al nuevo sistema cuando configure los saldos iniciales en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="55dfd-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="55dfd-127">A.</span><span class="sxs-lookup"><span data-stu-id="55dfd-127">A.</span></span> <span data-ttu-id="55dfd-128">Cómo configurar los códigos de ganancias que se utilizarán en los saldos iniciales de nóminas</span><span class="sxs-lookup"><span data-stu-id="55dfd-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="55dfd-129">Al especificar los saldos iniciales de nómina, asegúrese de que los códigos de ganancias que usará están configurados con la opción “Permitir edición de tasas de extracto de ganancias” habilitada.</span><span class="sxs-lookup"><span data-stu-id="55dfd-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="55dfd-130">Esto le permitirá especificar manualmente el importe del sistema heredado.</span><span class="sxs-lookup"><span data-stu-id="55dfd-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="55dfd-131">B.</span><span class="sxs-lookup"><span data-stu-id="55dfd-131">B.</span></span> <span data-ttu-id="55dfd-132">Crear el extracto de ganancias para que un empleado con saldo inicial</span><span class="sxs-lookup"><span data-stu-id="55dfd-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="55dfd-133">Este paso crea manualmente una instrucción de ganancias para cada trabajador para el último período salarial del sistema heredado, lo que crea las líneas de extracto de ganancias en el nuevo sistema de nóminas.</span><span class="sxs-lookup"><span data-stu-id="55dfd-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="55dfd-134">Especifique una línea por código de ganancias y el importe y las horas de del año hasta la fecha.</span><span class="sxs-lookup"><span data-stu-id="55dfd-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="55dfd-135">Los pasos de ejemplo son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="55dfd-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="55dfd-136">Abra la página **Todos los extractos de ganancias** y haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="55dfd-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="55dfd-137">Especifique la información siguiente:</span><span class="sxs-lookup"><span data-stu-id="55dfd-137">Enter the following:</span></span> 

    | <span data-ttu-id="55dfd-138">Campo</span><span class="sxs-lookup"><span data-stu-id="55dfd-138">Field</span></span>      | <span data-ttu-id="55dfd-139">Valor</span><span class="sxs-lookup"><span data-stu-id="55dfd-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="55dfd-140">Trabajador</span><span class="sxs-lookup"><span data-stu-id="55dfd-140">Worker</span></span>     | <span data-ttu-id="55dfd-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="55dfd-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="55dfd-142">Ciclo de pago</span><span class="sxs-lookup"><span data-stu-id="55dfd-142">Pay cycle</span></span>  | <span data-ttu-id="55dfd-143">Se</span><span class="sxs-lookup"><span data-stu-id="55dfd-143">sm</span></span>                    |
    | <span data-ttu-id="55dfd-144">Período de pago</span><span class="sxs-lookup"><span data-stu-id="55dfd-144">Pay period</span></span> | <span data-ttu-id="55dfd-145">16/6/2017 - 30/6/2017</span><span class="sxs-lookup"><span data-stu-id="55dfd-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="55dfd-146">En la pestaña **Línea de extracto de ganancias**, especifique lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55dfd-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="55dfd-147">Línea 1: Pestaña **Línea de extracto de ganancias**</span><span class="sxs-lookup"><span data-stu-id="55dfd-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="55dfd-148">Campo</span><span class="sxs-lookup"><span data-stu-id="55dfd-148">Field</span></span>            | <span data-ttu-id="55dfd-149">Valor</span><span class="sxs-lookup"><span data-stu-id="55dfd-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="55dfd-150">Código de ganancias</span><span class="sxs-lookup"><span data-stu-id="55dfd-150">Earnings code</span></span>    | <span data-ttu-id="55dfd-151">Pago regular</span><span class="sxs-lookup"><span data-stu-id="55dfd-151">Regular pay</span></span> |
    | <span data-ttu-id="55dfd-152">Cantidad</span><span class="sxs-lookup"><span data-stu-id="55dfd-152">Quantity</span></span>         | <span data-ttu-id="55dfd-153">1.00</span><span class="sxs-lookup"><span data-stu-id="55dfd-153">1.00</span></span>        |
    | <span data-ttu-id="55dfd-154">Índice</span><span class="sxs-lookup"><span data-stu-id="55dfd-154">Rate</span></span>             | <span data-ttu-id="55dfd-155">30,000</span><span class="sxs-lookup"><span data-stu-id="55dfd-155">30,000</span></span>      |
    | <span data-ttu-id="55dfd-156">Pestaña Detalles de línea</span><span class="sxs-lookup"><span data-stu-id="55dfd-156">Line details tab</span></span> |             |
    | <span data-ttu-id="55dfd-157">Manual</span><span class="sxs-lookup"><span data-stu-id="55dfd-157">Manual</span></span>           | <span data-ttu-id="55dfd-158">(marcado)</span><span class="sxs-lookup"><span data-stu-id="55dfd-158">(marked)</span></span>    |

    <span data-ttu-id="55dfd-159">Línea 2: Pestaña **Línea de extracto de ganancias**</span><span class="sxs-lookup"><span data-stu-id="55dfd-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="55dfd-160">Campo</span><span class="sxs-lookup"><span data-stu-id="55dfd-160">Field</span></span>            | <span data-ttu-id="55dfd-161">Valor</span><span class="sxs-lookup"><span data-stu-id="55dfd-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="55dfd-162">Código de ganancias</span><span class="sxs-lookup"><span data-stu-id="55dfd-162">Earnings code</span></span>    | <span data-ttu-id="55dfd-163">Bonificación</span><span class="sxs-lookup"><span data-stu-id="55dfd-163">Bonus</span></span>    |
    | <span data-ttu-id="55dfd-164">Cantidad</span><span class="sxs-lookup"><span data-stu-id="55dfd-164">Quantity</span></span>         | <span data-ttu-id="55dfd-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="55dfd-165">1.0000</span></span>   |
    | <span data-ttu-id="55dfd-166">Índice</span><span class="sxs-lookup"><span data-stu-id="55dfd-166">Rate</span></span>             | <span data-ttu-id="55dfd-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="55dfd-167">4250.00</span></span>  |
    | <span data-ttu-id="55dfd-168">Pestaña Detalles de línea</span><span class="sxs-lookup"><span data-stu-id="55dfd-168">Line details tab</span></span> |          |
    | <span data-ttu-id="55dfd-169">Manual</span><span class="sxs-lookup"><span data-stu-id="55dfd-169">Manual</span></span>           | <span data-ttu-id="55dfd-170">(marcado)</span><span class="sxs-lookup"><span data-stu-id="55dfd-170">(marked)</span></span> |

    <span data-ttu-id="55dfd-171">Línea 3: Pestaña **Línea de extracto de ganancias**</span><span class="sxs-lookup"><span data-stu-id="55dfd-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="55dfd-172">Campo</span><span class="sxs-lookup"><span data-stu-id="55dfd-172">Field</span></span>           | <span data-ttu-id="55dfd-173">Valor</span><span class="sxs-lookup"><span data-stu-id="55dfd-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="55dfd-174">Código de ganancias</span><span class="sxs-lookup"><span data-stu-id="55dfd-174">Earnings code</span></span>   | <span data-ttu-id="55dfd-175">Comisión</span><span class="sxs-lookup"><span data-stu-id="55dfd-175">Commission</span></span> |
    | <span data-ttu-id="55dfd-176">Cantidad</span><span class="sxs-lookup"><span data-stu-id="55dfd-176">Quantity</span></span>        | <span data-ttu-id="55dfd-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="55dfd-177">1.0000</span></span>     |
    | <span data-ttu-id="55dfd-178">Índice</span><span class="sxs-lookup"><span data-stu-id="55dfd-178">Rate</span></span>            | <span data-ttu-id="55dfd-179">1299,00</span><span class="sxs-lookup"><span data-stu-id="55dfd-179">!,299.00</span></span>   |
    | <span data-ttu-id="55dfd-180">Índice</span><span class="sxs-lookup"><span data-stu-id="55dfd-180">Rate</span></span>            | <span data-ttu-id="55dfd-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="55dfd-181">1,299.00</span></span>   |
    | <span data-ttu-id="55dfd-182">Pestaña Detalles de línea</span><span class="sxs-lookup"><span data-stu-id="55dfd-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="55dfd-183">Manual</span><span class="sxs-lookup"><span data-stu-id="55dfd-183">Manual</span></span>          | <span data-ttu-id="55dfd-184">(Marcado)</span><span class="sxs-lookup"><span data-stu-id="55dfd-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="55dfd-185">Establecer el control deslizante **Manual** en **Sí** en la pestaña **Detalles de línea** para cada línea de extracto de ganancias es fundamental para tener saldos iniciales de nómina especificados para cada trabajador.</span><span class="sxs-lookup"><span data-stu-id="55dfd-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="55dfd-186">En el panel **Acción**, haga clic en **Liberar extracto de ganancias** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="55dfd-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="55dfd-187">En el panel **Acción** haga clic en **Extracto de pago** para abrir la página **Generar extractos de pago** y establecer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55dfd-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="55dfd-188">Campo</span><span class="sxs-lookup"><span data-stu-id="55dfd-188">Field</span></span>              | <span data-ttu-id="55dfd-189">Valor</span><span class="sxs-lookup"><span data-stu-id="55dfd-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="55dfd-190">Fecha de pago</span><span class="sxs-lookup"><span data-stu-id="55dfd-190">Payment date</span></span>       | <span data-ttu-id="55dfd-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="55dfd-191">6/30/2017</span></span> |
    | <span data-ttu-id="55dfd-192">Tipo de ejecución de pago</span><span class="sxs-lookup"><span data-stu-id="55dfd-192">Payment run type</span></span>   | <span data-ttu-id="55dfd-193">Manual</span><span class="sxs-lookup"><span data-stu-id="55dfd-193">Manual</span></span>    |
    | <span data-ttu-id="55dfd-194">Deshabilitar contabilidad</span><span class="sxs-lookup"><span data-stu-id="55dfd-194">Disable accounting</span></span> |   <span data-ttu-id="55dfd-195">Sí</span><span class="sxs-lookup"><span data-stu-id="55dfd-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="55dfd-196">Esto solo está disponible cuando el tipo de procesamiento de pago es manual y si el usuario desea deshabilitar la contabilidad en el procesamiento de pagos.</span><span class="sxs-lookup"><span data-stu-id="55dfd-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="55dfd-197">Haga clic en **Aceptar** y cierre el **Registro de información**.</span><span class="sxs-lookup"><span data-stu-id="55dfd-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="55dfd-198">¿Por qué el control deslizante Deshabilitar contabilidad tiene que establecerse en Sí cuando se generan extractos de pago?</span><span class="sxs-lookup"><span data-stu-id="55dfd-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="55dfd-199">Establecer el control deslizante en **Sí** impide que las líneas de los extractos de pago se distribuya en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="55dfd-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="55dfd-200">Los importes de la contabilidad general se actualizaron con anterioridad cuando se introdujeron los saldos de cuenta desde el sistema heredado.</span><span class="sxs-lookup"><span data-stu-id="55dfd-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="55dfd-201">Introducir los saldos iniciales para la nómina le permite generar informes que contienen información de años anteriores, así como identificar límites para fines de prestaciones e impuestos.</span><span class="sxs-lookup"><span data-stu-id="55dfd-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="55dfd-202">C.</span><span class="sxs-lookup"><span data-stu-id="55dfd-202">C.</span></span> <span data-ttu-id="55dfd-203">Crear extractos de pago para empleados</span><span class="sxs-lookup"><span data-stu-id="55dfd-203">Create pay statements for employees</span></span>

<span data-ttu-id="55dfd-204">Tras generar los extractos de pago con saldos iniciales, debe comprobar que los extractos de pago reflejan exactamente los datos de la nómina.</span><span class="sxs-lookup"><span data-stu-id="55dfd-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="55dfd-205">También debe actualizar manualmente la información de prestaciones y de impuestos para que coincida con los valores del sistema de nóminas anterior.</span><span class="sxs-lookup"><span data-stu-id="55dfd-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="55dfd-206">Después de verificar que los importes del sistema de nóminas anterior se corresponden con los importes de los extractos de pago actuales, debe finalizar los extractos de pago.</span><span class="sxs-lookup"><span data-stu-id="55dfd-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="55dfd-207">Abre la página **Todos los extractos de pago**.</span><span class="sxs-lookup"><span data-stu-id="55dfd-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="55dfd-208">Resalte el último extracto de pago generado para Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="55dfd-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="55dfd-209">Haga clic en **Editar** para abrir la página **Extracto de pago**.</span><span class="sxs-lookup"><span data-stu-id="55dfd-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="55dfd-210">Abre la pestaña **Deducciones por prestaciones** y especifique lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55dfd-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="55dfd-211">Campo</span><span class="sxs-lookup"><span data-stu-id="55dfd-211">Field</span></span>             | <span data-ttu-id="55dfd-212">Valor</span><span class="sxs-lookup"><span data-stu-id="55dfd-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="55dfd-213">Prestación</span><span class="sxs-lookup"><span data-stu-id="55dfd-213">Benefit</span></span>           | <span data-ttu-id="55dfd-214">Importe de deducción</span><span class="sxs-lookup"><span data-stu-id="55dfd-214">Deduction amount</span></span> |
    | <span data-ttu-id="55dfd-215">401K</span><span class="sxs-lookup"><span data-stu-id="55dfd-215">401K</span></span>              | <span data-ttu-id="55dfd-216">Participar</span><span class="sxs-lookup"><span data-stu-id="55dfd-216">Participate</span></span>      |
    | <span data-ttu-id="55dfd-217">Dental</span><span class="sxs-lookup"><span data-stu-id="55dfd-217">Dental</span></span>            | <span data-ttu-id="55dfd-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="55dfd-218">SubSp</span></span>            |
    | <span data-ttu-id="55dfd-219">Gastos de atención del Dep</span><span class="sxs-lookup"><span data-stu-id="55dfd-219">Dep care spending</span></span> | <span data-ttu-id="55dfd-220">Participar</span><span class="sxs-lookup"><span data-stu-id="55dfd-220">Participate</span></span>      |
    | <span data-ttu-id="55dfd-221">Visión</span><span class="sxs-lookup"><span data-stu-id="55dfd-221">Vision</span></span>            | <span data-ttu-id="55dfd-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="55dfd-222">SupSp</span></span>            |

5. <span data-ttu-id="55dfd-223">En la pestaña **Contribuciones por prestaciones**, especifique lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55dfd-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="55dfd-224">Campo</span><span class="sxs-lookup"><span data-stu-id="55dfd-224">Field</span></span>   | <span data-ttu-id="55dfd-225">Valor</span><span class="sxs-lookup"><span data-stu-id="55dfd-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="55dfd-226">Prestación</span><span class="sxs-lookup"><span data-stu-id="55dfd-226">Benefit</span></span> | <span data-ttu-id="55dfd-227">Importe de contribución</span><span class="sxs-lookup"><span data-stu-id="55dfd-227">Contribution amount</span></span> |
    | <span data-ttu-id="55dfd-228">401K</span><span class="sxs-lookup"><span data-stu-id="55dfd-228">401K</span></span>    | <span data-ttu-id="55dfd-229">Participar</span><span class="sxs-lookup"><span data-stu-id="55dfd-229">Participate</span></span>         |
    | <span data-ttu-id="55dfd-230">Dental</span><span class="sxs-lookup"><span data-stu-id="55dfd-230">Dental</span></span>  | <span data-ttu-id="55dfd-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="55dfd-231">SubSp</span></span>               |
    | <span data-ttu-id="55dfd-232">Visión</span><span class="sxs-lookup"><span data-stu-id="55dfd-232">Vision</span></span>  | <span data-ttu-id="55dfd-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="55dfd-233">SubSp</span></span>               |

6. <span data-ttu-id="55dfd-234">En la pestaña **Deducciones por impuestos**, especifique lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55dfd-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="55dfd-235">Campo</span><span class="sxs-lookup"><span data-stu-id="55dfd-235">Field</span></span>           | <span data-ttu-id="55dfd-236">Valor</span><span class="sxs-lookup"><span data-stu-id="55dfd-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="55dfd-237">Código de impuesto</span><span class="sxs-lookup"><span data-stu-id="55dfd-237">Tax code</span></span>        | <span data-ttu-id="55dfd-238">Importe de deducción</span><span class="sxs-lookup"><span data-stu-id="55dfd-238">Deduction amount</span></span> |
    | <span data-ttu-id="55dfd-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="55dfd-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="55dfd-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="55dfd-240">1600.00</span></span>          |
    | <span data-ttu-id="55dfd-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="55dfd-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="55dfd-242">825.75</span><span class="sxs-lookup"><span data-stu-id="55dfd-242">825.75</span></span>           |

7. <span data-ttu-id="55dfd-243">En la pestaña **Contribuciones por impuestos**, especifique lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55dfd-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="55dfd-244">Haga clic en **Calcular**.</span><span class="sxs-lookup"><span data-stu-id="55dfd-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="55dfd-245">Valide los totales del extracto de pago que coincidan con el año hasta la fecha del sistema heredado para el trabajador.</span><span class="sxs-lookup"><span data-stu-id="55dfd-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="55dfd-246">Es posible que desee retener la finalización en el paso siguiente para hacer una validación general de todos los extractos de pago en conjunto.</span><span class="sxs-lookup"><span data-stu-id="55dfd-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="55dfd-247">Una vez hecha la validación pase por todos los extractos de pago y complételos.</span><span class="sxs-lookup"><span data-stu-id="55dfd-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="55dfd-248">El mismo proceso se puede realizar en incrementos trimestres si fuera necesario para todos los trimestres anteriores de cada año.</span><span class="sxs-lookup"><span data-stu-id="55dfd-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="55dfd-249">Esto solo es necesario si el cliente necesita ver los datos por trimestre sin tener que volver al sistema heredado.</span><span class="sxs-lookup"><span data-stu-id="55dfd-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="55dfd-250">Si se equivoca especificando los saldos iniciales para un empleado</span><span class="sxs-lookup"><span data-stu-id="55dfd-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="55dfd-251">Es posible invertir y repetir las transacciones.</span><span class="sxs-lookup"><span data-stu-id="55dfd-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="55dfd-252">Para invertir la transacción, todo lo que debe hacer es completar los pasos siguientes en la página **Todos los extractos de pago**.</span><span class="sxs-lookup"><span data-stu-id="55dfd-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="55dfd-253">Haga clic en **Invertir**.</span><span class="sxs-lookup"><span data-stu-id="55dfd-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="55dfd-254">Haga clic en **Sí** cuando aparezca el mensaje “Cuando se invierte este extracto de pago, se crea un extracto de pago de inversión para compensarlo.</span><span class="sxs-lookup"><span data-stu-id="55dfd-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="55dfd-255">Ninguno de los extractos de pago se podrá modificar.</span><span class="sxs-lookup"><span data-stu-id="55dfd-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="55dfd-256">¿Quiere invertir este extracto de pago?</span><span class="sxs-lookup"><span data-stu-id="55dfd-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="55dfd-257">.</span><span class="sxs-lookup"><span data-stu-id="55dfd-257">displays.</span></span> 

<span data-ttu-id="55dfd-258">Una vez que revierta el extracto de pago, puede generar un nuevo extracto de pago para el trabajador desde el extracto de ganancias que creó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="55dfd-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="55dfd-259">Asegúrese de corregir las líneas incorrectas del extracto de ganancias antes de generar la nueva instrucción de pago, y luego genere nuevos extractos de sueldo con los importes correctos.</span><span class="sxs-lookup"><span data-stu-id="55dfd-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 