---
title: Límites de existencias de la ubicación
description: Este tema describe la funcionalidad para los límites de existencias de ubicaciones.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 208662f38b06b1f230bdde5247946a9fefd57cea
ms.sourcegitcommit: d2dea9ce480f35d0c0b10615c18862695e107d55
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2020
ms.locfileid: "4607288"
---
# <a name="location-stocking-limits"></a><span data-ttu-id="ecc31-103">Límites de existencias de la ubicación</span><span class="sxs-lookup"><span data-stu-id="ecc31-103">Location stocking limits</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecc31-104">Puede usar la página **Límites de almacenamiento de ubicación** (**Gestion de almacenes \> Preparar \> Almacén \> Límites de almacenamiento de ubicación**) para controlar la capacidad de carga en las ubicaciones de los almacenes sin tener que utilizar los procesos más avanzados para cálculos volumétricos de productos físicos.</span><span class="sxs-lookup"><span data-stu-id="ecc31-104">You can use the **Location stocking limits** page (**Warehouse management \> Setup \> Warehouse \> Location stocking limits**) to control the load capacity at warehouse locations without having to use the more advanced processes for volumetric calculations of physical products.</span></span>

<span data-ttu-id="ecc31-105">El propósito de los límites de existencias de una ubicación es evaluar la cantidad máxima que puede contener una ubicación.</span><span class="sxs-lookup"><span data-stu-id="ecc31-105">The purpose of location stocking limits is to evaluate the maximum quantity that a location can contain.</span></span> <span data-ttu-id="ecc31-106">Puede configurar la función en cualquiera de los tres niveles, cada uno de los cuales tiene su propia pestaña en la página **Límites de almacenamiento de ubicación**:</span><span class="sxs-lookup"><span data-stu-id="ecc31-106">You can set up the feature on any of three levels, each of which has its own tab on the **Location stocking limits** page:</span></span>

- <span data-ttu-id="ecc31-107">Productos</span><span class="sxs-lookup"><span data-stu-id="ecc31-107">Products</span></span>
- <span data-ttu-id="ecc31-108">Variantes del producto</span><span class="sxs-lookup"><span data-stu-id="ecc31-108">Product variants</span></span>
- <span data-ttu-id="ecc31-109">Tipos de contenedor</span><span class="sxs-lookup"><span data-stu-id="ecc31-109">Container types</span></span>

<span data-ttu-id="ecc31-110">Para cada nivel, puede definir diferentes valores de campo.</span><span class="sxs-lookup"><span data-stu-id="ecc31-110">For each level, you can define different field values.</span></span> <span data-ttu-id="ecc31-111">A continuación, el sistema evaluará la capacidad de una ubicación específica, en función de los valores **Cantidad** y **Unidad** para cada fila.</span><span class="sxs-lookup"><span data-stu-id="ecc31-111">The system will then evaluate the capacity of a specific location, based on the **Quantity** and **Unit** values for each row.</span></span> <span data-ttu-id="ecc31-112">Primero seleccionará el registro coincidente más detallado.</span><span class="sxs-lookup"><span data-stu-id="ecc31-112">It will select the most detailed matching record first.</span></span> <span data-ttu-id="ecc31-113">Por ejemplo, una fila que tiene un valor en el campo **ID de perfil de ubicación** se evaluará antes de una fila que tenga un valor solo en el campo **Almacén**.</span><span class="sxs-lookup"><span data-stu-id="ecc31-113">For example, a row that has a value in the **Location profile ID** field will be evaluated before a row that has a value only in the **Warehouse** field.</span></span> <span data-ttu-id="ecc31-114">También se evaluará la capacidad restante, en función del valor **Cantidad** para el registro de límite de existencias de la ubicación que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ecc31-114">The remaining capacity will also be evaluated, based on the **Quantity** value for the location stocking limit record that is used.</span></span>

<span data-ttu-id="ecc31-115">En la sección **Productos** de la página, puede definir los siguientes valores de campo para la búsqueda de límites de almacenamiento de ubicación:</span><span class="sxs-lookup"><span data-stu-id="ecc31-115">In the **Products** section of the page, you can define the following field values for the search for location stocking limits:</span></span>

- <span data-ttu-id="ecc31-116">Almacén</span><span class="sxs-lookup"><span data-stu-id="ecc31-116">Warehouse</span></span>
- <span data-ttu-id="ecc31-117">Id. de perfil de ubicación</span><span class="sxs-lookup"><span data-stu-id="ecc31-117">Location profile ID</span></span>
- <span data-ttu-id="ecc31-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ecc31-118">Location</span></span>
- <span data-ttu-id="ecc31-119">Id. de categoría de tamaño de paquete</span><span class="sxs-lookup"><span data-stu-id="ecc31-119">Pack size category ID</span></span>
- <span data-ttu-id="ecc31-120">Número de artículo</span><span class="sxs-lookup"><span data-stu-id="ecc31-120">Item number</span></span>
- <span data-ttu-id="ecc31-121">Unidad</span><span class="sxs-lookup"><span data-stu-id="ecc31-121">Unit</span></span>

> [!NOTE]
> <span data-ttu-id="ecc31-122">No tiene que definir un valor de **Unidad** para cada registro de límite de existencias de ubicación.</span><span class="sxs-lookup"><span data-stu-id="ecc31-122">You don't have to define a **Unit** value for each location stocking limit record.</span></span> <span data-ttu-id="ecc31-123">Los cálculos de capacidad de ubicación se basarán en las cantidades de unidades de inventario.</span><span class="sxs-lookup"><span data-stu-id="ecc31-123">The location capacity calculations will be based on the inventory unit quantities.</span></span> <span data-ttu-id="ecc31-124">Si no se define una conversión de unidad para un valor que se utiliza, se omitirá el registro de límite de existencias de la ubicación, como si otro valor de **Número de artículo** está definido para ello.</span><span class="sxs-lookup"><span data-stu-id="ecc31-124">If no unit conversion is defined for a value that is used, the location stocking limit record will be skipped, as if another **Item number** value is defined for it.</span></span>

## <a name="example--purchase-order-receiving"></a><span data-ttu-id="ecc31-125">Ejemplo: recepción de pedido de compra</span><span class="sxs-lookup"><span data-stu-id="ecc31-125">Example – Purchase order receiving</span></span>

<span data-ttu-id="ecc31-126">Este ejemplo se basa en un conjunto de datos de demostración limpio de *USMF*, donde se establecen los siguientes valores en la pestaña **Variantes de producto** de la página **Límites de almacenamiento de ubicación**.</span><span class="sxs-lookup"><span data-stu-id="ecc31-126">This example is based on a clean *USMF* demo data set, where the following values are set on the **Product variants** tab of the **Location stocking limits** page.</span></span>

| <span data-ttu-id="ecc31-127">Almacén</span><span class="sxs-lookup"><span data-stu-id="ecc31-127">Warehouse</span></span> | <span data-ttu-id="ecc31-128">Id. de perfil de ubicación</span><span class="sxs-lookup"><span data-stu-id="ecc31-128">Location profile ID</span></span> | <span data-ttu-id="ecc31-129">Número de artículo</span><span class="sxs-lookup"><span data-stu-id="ecc31-129">Item number</span></span> | <span data-ttu-id="ecc31-130">Talla</span><span class="sxs-lookup"><span data-stu-id="ecc31-130">Size</span></span> | <span data-ttu-id="ecc31-131">Cantidad</span><span class="sxs-lookup"><span data-stu-id="ecc31-131">Quantity</span></span> | <span data-ttu-id="ecc31-132">Unidad</span><span class="sxs-lookup"><span data-stu-id="ecc31-132">Unit</span></span> |
|-----------|---------------------|-------------|------|----------|------|
| <span data-ttu-id="ecc31-133">24</span><span class="sxs-lookup"><span data-stu-id="ecc31-133">24</span></span>        | <span data-ttu-id="ecc31-134">FLOOR</span><span class="sxs-lookup"><span data-stu-id="ecc31-134">FLOOR</span></span>               | <span data-ttu-id="ecc31-135">D0013</span><span class="sxs-lookup"><span data-stu-id="ecc31-135">D0013</span></span>       | <span data-ttu-id="ecc31-136">L</span><span class="sxs-lookup"><span data-stu-id="ecc31-136">M</span></span>    | <span data-ttu-id="ecc31-137">300</span><span class="sxs-lookup"><span data-stu-id="ecc31-137">300</span></span>      | <span data-ttu-id="ecc31-138">c/u</span><span class="sxs-lookup"><span data-stu-id="ecc31-138">Ea</span></span>   |
| <span data-ttu-id="ecc31-139">24</span><span class="sxs-lookup"><span data-stu-id="ecc31-139">24</span></span>        | <span data-ttu-id="ecc31-140">FLOOR</span><span class="sxs-lookup"><span data-stu-id="ecc31-140">FLOOR</span></span>               | <span data-ttu-id="ecc31-141">D0013</span><span class="sxs-lookup"><span data-stu-id="ecc31-141">D0013</span></span>       | <span data-ttu-id="ecc31-142">L</span><span class="sxs-lookup"><span data-stu-id="ecc31-142">L</span></span>    | <span data-ttu-id="ecc31-143">240</span><span class="sxs-lookup"><span data-stu-id="ecc31-143">240</span></span>      | <span data-ttu-id="ecc31-144">c/u</span><span class="sxs-lookup"><span data-stu-id="ecc31-144">Ea</span></span>   |
| <span data-ttu-id="ecc31-145">24</span><span class="sxs-lookup"><span data-stu-id="ecc31-145">24</span></span>        | <span data-ttu-id="ecc31-146">FLOOR</span><span class="sxs-lookup"><span data-stu-id="ecc31-146">FLOOR</span></span>               | <span data-ttu-id="ecc31-147">D0013</span><span class="sxs-lookup"><span data-stu-id="ecc31-147">D0013</span></span>       | <span data-ttu-id="ecc31-148">S</span><span class="sxs-lookup"><span data-stu-id="ecc31-148">S</span></span>    | <span data-ttu-id="ecc31-149">360</span><span class="sxs-lookup"><span data-stu-id="ecc31-149">360</span></span>      | <span data-ttu-id="ecc31-150">c/u</span><span class="sxs-lookup"><span data-stu-id="ecc31-150">Ea</span></span>   |

<span data-ttu-id="ecc31-151">Se configuran diferentes variantes de producto de unidad de medida para los productos.</span><span class="sxs-lookup"><span data-stu-id="ecc31-151">Different unit of measure product variants are set up for the products.</span></span> <span data-ttu-id="ecc31-152">Estas variantes están alineadas con los límites de almacenamiento de ubicación para tres paletas (PL):</span><span class="sxs-lookup"><span data-stu-id="ecc31-152">These variants are aligned with the location stocking limits for three pallets (PL):</span></span>

- <span data-ttu-id="ecc31-153">**Talla M:** 1 PL = 100 cada uno (Ea)</span><span class="sxs-lookup"><span data-stu-id="ecc31-153">**Size M:** 1 PL = 100 each (Ea)</span></span>
- <span data-ttu-id="ecc31-154">**Talla L:** 1 PL = 80 Ea</span><span class="sxs-lookup"><span data-stu-id="ecc31-154">**Size L:** 1 PL = 80 Ea</span></span>
- <span data-ttu-id="ecc31-155">**Talla S:** 1 PL = 120 Ea</span><span class="sxs-lookup"><span data-stu-id="ecc31-155">**Size S:** 1 PL = 120 Ea</span></span>

<span data-ttu-id="ecc31-156">Por lo tanto, cada lugar donde el valor de **ID de perfil de ubicación** está establecido en *FLOOR* puede llevar *3* *PL* del número de artículo *D0013*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-156">Therefore, each location where the **Location profile ID** value is set to *FLOOR* can carry *3* *PL* of item number *D0013*.</span></span>

### <a name="prepare-for-the-example"></a><span data-ttu-id="ecc31-157">Prepapar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ecc31-157">Prepare for the example</span></span>

<span data-ttu-id="ecc31-158">En este ejemplo, ejecutará un flujo de recepción de órdenes de compra para dos líneas.</span><span class="sxs-lookup"><span data-stu-id="ecc31-158">In this example, you will run a purchase order receiving flow for two lines.</span></span> <span data-ttu-id="ecc31-159">Sin embargo, primero debe actualizar los datos de demostración de la siguiente manera para asegurarse de que las ubicaciones permitan el transporte de artículos mixtos, solo se utilizan las ubicaciones vacías *FL-002* a *FL-004* y no hay trabajo entrante abierto.</span><span class="sxs-lookup"><span data-stu-id="ecc31-159">However, you must first update the demo data in the following way to ensure that the locations allow mixed items to be carried, only the empty locations *FL-002* through *FL-004* are used, and there is no open inbound work.</span></span>

1. <span data-ttu-id="ecc31-160">Para la ubicación *FL-001*, cambie el valor del campo **Perfil de ubicación** de *FLOOR* a *FLOOR-05*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-160">For location *FL-001*, change the value of the **Location profile** field from *FLOOR* to *FLOOR-05*.</span></span>
1. <span data-ttu-id="ecc31-161">Para el perfil de ubicación *FLOOR*, configure la opción **Permitir elementos mixtos** en *Sí*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-161">For the *FLOOR* location profile, set the **Allow mixed items** option to *Yes*.</span></span>
1. <span data-ttu-id="ecc31-162">Cree un pedido de compra con las dos líneas siguientes.</span><span class="sxs-lookup"><span data-stu-id="ecc31-162">Create a purchase order that has the following two lines.</span></span>

    | <span data-ttu-id="ecc31-163">Almacén</span><span class="sxs-lookup"><span data-stu-id="ecc31-163">Warehouse</span></span> | <span data-ttu-id="ecc31-164">Número de artículo</span><span class="sxs-lookup"><span data-stu-id="ecc31-164">Item number</span></span> | <span data-ttu-id="ecc31-165">Talla</span><span class="sxs-lookup"><span data-stu-id="ecc31-165">Size</span></span> | <span data-ttu-id="ecc31-166">Cantidad</span><span class="sxs-lookup"><span data-stu-id="ecc31-166">Quantity</span></span> | <span data-ttu-id="ecc31-167">Unidad</span><span class="sxs-lookup"><span data-stu-id="ecc31-167">Unit</span></span> |
    |-----------|-------------|------|----------|------|
    | <span data-ttu-id="ecc31-168">24</span><span class="sxs-lookup"><span data-stu-id="ecc31-168">24</span></span>        | <span data-ttu-id="ecc31-169">D0013</span><span class="sxs-lookup"><span data-stu-id="ecc31-169">D0013</span></span>       | <span data-ttu-id="ecc31-170">S</span><span class="sxs-lookup"><span data-stu-id="ecc31-170">S</span></span>    | <span data-ttu-id="ecc31-171">4</span><span class="sxs-lookup"><span data-stu-id="ecc31-171">4</span></span>        | <span data-ttu-id="ecc31-172">PL</span><span class="sxs-lookup"><span data-stu-id="ecc31-172">PL</span></span>   |
    | <span data-ttu-id="ecc31-173">24</span><span class="sxs-lookup"><span data-stu-id="ecc31-173">24</span></span>        | <span data-ttu-id="ecc31-174">D0013</span><span class="sxs-lookup"><span data-stu-id="ecc31-174">D0013</span></span>       | <span data-ttu-id="ecc31-175">L</span><span class="sxs-lookup"><span data-stu-id="ecc31-175">L</span></span>    | <span data-ttu-id="ecc31-176">4</span><span class="sxs-lookup"><span data-stu-id="ecc31-176">4</span></span>        | <span data-ttu-id="ecc31-177">PL</span><span class="sxs-lookup"><span data-stu-id="ecc31-177">PL</span></span>   |

### <a name="process-the-example"></a><span data-ttu-id="ecc31-178">Procesar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ecc31-178">Process the example</span></span>

<span data-ttu-id="ecc31-179">Primero recibirá una cantidad de *4* de la unidad *PL* en tamaño *S* y revisará las ubicaciones de las líneas de colocación para el trabajo que se crea.</span><span class="sxs-lookup"><span data-stu-id="ecc31-179">You will first receive a quantity of *4* of unit *PL* in size *S*, and review the put line locations for the work that is created.</span></span> <span data-ttu-id="ecc31-180">Después recibirá una cantidad de *4* de la unidad *PL* en tamaño *L* y revisará las ubicaciones de las líneas de colocación para el trabajo que se crea.</span><span class="sxs-lookup"><span data-stu-id="ecc31-180">You will then receive a quantity of *4* of unit *PL* in size *L*, and review the put line locations for the work that is created.</span></span>

1. <span data-ttu-id="ecc31-181">En la aplicación de almacén, inicie sesión utilizando *24* como el Id. de usuario y *1* como la contraseña.</span><span class="sxs-lookup"><span data-stu-id="ecc31-181">In the warehouse app, sign in by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="ecc31-182">Seleccione **Entrante** \> **Recepción de compra**.</span><span class="sxs-lookup"><span data-stu-id="ecc31-182">Select **Inbound** \> **Purchase Receive**.</span></span>
1. <span data-ttu-id="ecc31-183">Reciba *4* *PL* del número de artículo *D0013* en tamaño *S*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-183">Receive *4* *PL* of item number *D0013* in size *S*.</span></span>
1. <span data-ttu-id="ecc31-184">Revise el trabajo de ubicación que se creó.</span><span class="sxs-lookup"><span data-stu-id="ecc31-184">Review the putaway work that was created.</span></span> <span data-ttu-id="ecc31-185">Debería ver el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="ecc31-185">You should see the following result:</span></span>

    - <span data-ttu-id="ecc31-186">3 PL -\> FL-002</span><span class="sxs-lookup"><span data-stu-id="ecc31-186">3 PL -\> FL-002</span></span>
    - <span data-ttu-id="ecc31-187">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="ecc31-187">1 PL -\> FL-003</span></span>

1. <span data-ttu-id="ecc31-188">Reciba *4* *PL* del número de artículo *D0013* en tamaño *L*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-188">Receive *4* *PL* of item number *D0013* in size *L*.</span></span>
1. <span data-ttu-id="ecc31-189">Revise el trabajo de ubicación que se creó.</span><span class="sxs-lookup"><span data-stu-id="ecc31-189">Review the putaway work that was created.</span></span> <span data-ttu-id="ecc31-190">Debería ver el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="ecc31-190">You should see the following result:</span></span>

    - <span data-ttu-id="ecc31-191">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="ecc31-191">1 PL -\> FL-003</span></span>
    - <span data-ttu-id="ecc31-192">3 PL -\> FL-004</span><span class="sxs-lookup"><span data-stu-id="ecc31-192">3 PL -\> FL-004</span></span>

<span data-ttu-id="ecc31-193">Según los resultados, puede concluir que el sistema no pudo asignar las ubicaciones correctas de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="ecc31-193">Based on the results, you might conclude that the system failed to allocate the correct putaway locations.</span></span> <span data-ttu-id="ecc31-194">De lo contrario, ¿por qué el sistema agregó solo *1* *PL* de tamaño *L* a la ubicación *FL-003* en el ultimo paso, no *2* *PL*?</span><span class="sxs-lookup"><span data-stu-id="ecc31-194">Otherwise, why did the system add only *1* *PL* of size *L* to location *FL-003* in the last step, not *2* *PL*?</span></span> <span data-ttu-id="ecc31-195">Es decir, ¿por qué no hay un total de *3* *PL* para el almacenamiento en esa ubicación?</span><span class="sxs-lookup"><span data-stu-id="ecc31-195">That is, why isn't there is a total of *3* *PL* for putaway to that location?</span></span>

<span data-ttu-id="ecc31-196">Para explicar esta aparente falla, debe comprender los criterios de selección para los límites de existencias de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="ecc31-196">To explain this apparent failure, you must understand the selection criteria for the location stocking limits.</span></span> <span data-ttu-id="ecc31-197">El sistema selecciona el registro coincidente más detallado.</span><span class="sxs-lookup"><span data-stu-id="ecc31-197">The system selects the most detailed matching record.</span></span> <span data-ttu-id="ecc31-198">En este ejemplo, el registro coincidente más detallado es la línea donde el valor **Tamaño** es *L*, el valor **Cantidad** es *240* y el valor **Unidad** es *Ea*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-198">In this example, the most detailed matching record is the line where the **Size** value is *L*, the **Quantity** value is *240*, and the **Unit** value is *Ea*.</span></span> <span data-ttu-id="ecc31-199">Porque ya tiene trabajo abierto desde la recepción anterior de una cantidad de *120* *Ea* de tamaño *S*, la capacidad restante se calcula como *240* - *120* = *120* *Ea*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-199">Because you already have open work from the previous receipt of a quantity of *120* *Ea* of size *S*, the remaining capacity is calculated as *240* – *120* = *120* *Ea*.</span></span> <span data-ttu-id="ecc31-200">Por lo tanto, la capacidad restante solo puede transportar *1* *PL* de *80* *Ea*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-200">Therefore, the remaining capacity can carry only *1* *PL* of *80* *Ea*.</span></span>

> [!NOTE]
> <span data-ttu-id="ecc31-201">No puede utilizar los límites de existencias de la ubicación para controlar, por ejemplo, el reabastecimiento de artículos que tienen diferentes cantidades en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="ecc31-201">You can't use location stocking limits to control, for example, the replenishment of items that have different quantities in the same location.</span></span> <span data-ttu-id="ecc31-202">En este caso, utilice una *plantilla de reposición*.</span><span class="sxs-lookup"><span data-stu-id="ecc31-202">In this case, use a *replenishment template*.</span></span>