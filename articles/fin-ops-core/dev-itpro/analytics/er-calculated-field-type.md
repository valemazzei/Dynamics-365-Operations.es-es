---
title: Admita las llamadas con parámetros de los orígenes de datos de ER del tipo de campo calculado
description: Este tema proporciona información sobre cómo usar el tipo de campo calculado para los orígenes de datos de ER.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f331401f8d191243f72961333e4f1dbe84d0be5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771338"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="5699e-103">Admita las llamadas con parámetros de los orígenes de datos de ER del tipo de campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5699e-104">Este tema explica cómo puede diseñar un origen de datos de informes electrónicos (ER) mediante el tipo **Campo calculado**.</span><span class="sxs-lookup"><span data-stu-id="5699e-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="5699e-105">Este origen de datos puede contener una expresión del ER que, cuando se ejecuta, se puede controlar mediante los valores de los argumentos de parámetros que se configuran en un enlace que llama a este origen de datos.</span><span class="sxs-lookup"><span data-stu-id="5699e-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="5699e-106">Al configurar llamadas con parámetros de este tipo de origen de datos, puede volver a usar un solo origen de datos en muchos enlaces, lo que reduce el número total de orígenes de datos que se deben configurar en distribuciones de modelos de ER o formatos de ER.</span><span class="sxs-lookup"><span data-stu-id="5699e-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="5699e-107">También simplifica el componente de ER configurado, que reduce los costes de mantenimiento y el coste de uso de otros consumidores.</span><span class="sxs-lookup"><span data-stu-id="5699e-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5699e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5699e-108">Prerequisites</span></span>
<span data-ttu-id="5699e-109">Para completar los ejemplos de este tema, debe tener el acceso siguiente:</span><span class="sxs-lookup"><span data-stu-id="5699e-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="5699e-110">Acceso a uno de estos roles:</span><span class="sxs-lookup"><span data-stu-id="5699e-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="5699e-111">Desarrollador de informes electrónicos</span><span class="sxs-lookup"><span data-stu-id="5699e-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="5699e-112">Consultor funcional de informes electrónicos</span><span class="sxs-lookup"><span data-stu-id="5699e-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5699e-113">Administrador del sistema</span><span class="sxs-lookup"><span data-stu-id="5699e-113">System administrator</span></span>

- <span data-ttu-id="5699e-114">Acceso a la instancia de los Regulatory Configuration Services (RCS) que se han aprovisionado para el mismo arrendatario que Finance and Operations, para uno de los roles siguientes:</span><span class="sxs-lookup"><span data-stu-id="5699e-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="5699e-115">Desarrollador de informes electrónicos</span><span class="sxs-lookup"><span data-stu-id="5699e-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="5699e-116">Consultor funcional de informes electrónicos</span><span class="sxs-lookup"><span data-stu-id="5699e-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5699e-117">Administrador del sistema</span><span class="sxs-lookup"><span data-stu-id="5699e-117">System administrator</span></span>

<span data-ttu-id="5699e-118">Desde [Centro de descarga de Microsoft](https://go.microsoft.com/fwlink/?linkid=874684), descarga el archivo comprimido **Admita las llamadas con parámetros de los orígenes de datos de ER del tipo de campo calculado**.</span><span class="sxs-lookup"><span data-stu-id="5699e-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="5699e-119">Contiene las siguientes configuraciones de ER que se deben extraer y almacenar localmente.</span><span class="sxs-lookup"><span data-stu-id="5699e-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="5699e-120">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="5699e-120">**Content**</span></span>                           | <span data-ttu-id="5699e-121">**Nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="5699e-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5699e-122">Configuración del modelo datos de ER de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5699e-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="5699e-123">Modelo para aprender llamadas con parámetros.versión.1.xml</span><span class="sxs-lookup"><span data-stu-id="5699e-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="5699e-124">Configuración de metadatos de ER de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5699e-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="5699e-125">Metadatos para aprender llamadas con parámetros.versión.1.xml</span><span class="sxs-lookup"><span data-stu-id="5699e-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="5699e-126">Configuración del modelo de mapeado de ER de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5699e-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="5699e-127">Asignación para aprender llamadas con parámetros.versión.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="5699e-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="5699e-128">Configuración de formato de ER de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5699e-128">Sample ER format configuration</span></span>        | <span data-ttu-id="5699e-129">Formato para aprender llamadas con parámetros.versión.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="5699e-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="5699e-130">Iniciar sesión en su instancia de RCS</span><span class="sxs-lookup"><span data-stu-id="5699e-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="5699e-131">En este ejemplo, creará una configuración para la empresa del ejemplo, Litware, Inc. First, en RCS, tiene que completar estos pasos, en el procedimiento [Crear proveedores de la configuración y marcarlos como activos](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="5699e-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="5699e-132">En el panel predeterminado, seleccione **Informes electrónicos**.</span><span class="sxs-lookup"><span data-stu-id="5699e-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="5699e-133">Seleccione **Configuraciones de informes**.</span><span class="sxs-lookup"><span data-stu-id="5699e-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="5699e-134">Importe las configuraciones descargadas al RCS en la siguiente secuencia: modelo de datos, metadatos, distribución de modelo, formato.</span><span class="sxs-lookup"><span data-stu-id="5699e-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="5699e-135">Realice los pasos siguientes para cada configuración de ER:</span><span class="sxs-lookup"><span data-stu-id="5699e-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="5699e-136">Seleccione **Intercambiar.**</span><span class="sxs-lookup"><span data-stu-id="5699e-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5699e-137">Seleccione **Cargar desde un archivo XML**.</span><span class="sxs-lookup"><span data-stu-id="5699e-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5699e-138">Seleccione **Examinar** y seleccione la configuración necesaria de ER en formato XML.</span><span class="sxs-lookup"><span data-stu-id="5699e-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="5699e-139">Seleccione **Aceptar.**</span><span class="sxs-lookup"><span data-stu-id="5699e-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="5699e-140">Revise la solución de ER proporcionada</span><span class="sxs-lookup"><span data-stu-id="5699e-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="5699e-141">Revisión de la distribución del modelo</span><span class="sxs-lookup"><span data-stu-id="5699e-141">Review model mapping</span></span>

1. <span data-ttu-id="5699e-142">En el árbol de configuración, expanda el contenido del elemento **Modele para aprender llamadas con parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5699e-143">Seleccione **Asignación para aprender llamadas con parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5699e-144">Seleccione **Diseñador**.</span><span class="sxs-lookup"><span data-stu-id="5699e-144">Select **Designer**.</span></span>
4. <span data-ttu-id="5699e-145">Seleccione **Diseñador**.</span><span class="sxs-lookup"><span data-stu-id="5699e-145">Select **Designer**.</span></span>  
   
    <span data-ttu-id="5699e-146">Esta distribución del modelo de ER está diseñada para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5699e-146">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="5699e-147">Obtener la lista de códigos de impuestos (origen de datos**Impuestos**) que residen en la tabla **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="5699e-147">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="5699e-148">Obtener la lista de transacciones de impuestos (origen de datos**Impuestos**) que residen en la tabla **TaxTable**:</span><span class="sxs-lookup"><span data-stu-id="5699e-148">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="5699e-149">Agrupar la lista de transacciones capturadas (origen de datos**Gr**) por código de impuestos.</span><span class="sxs-lookup"><span data-stu-id="5699e-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="5699e-150">Calcular las transacciones agrupadas que siguen valores agregados por código de impuestos:</span><span class="sxs-lookup"><span data-stu-id="5699e-150">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="5699e-151">Sumar los valores de la base fiscal.</span><span class="sxs-lookup"><span data-stu-id="5699e-151">Sum of tax base values.</span></span>
            - <span data-ttu-id="5699e-152">Sumar los valores de las tasas.</span><span class="sxs-lookup"><span data-stu-id="5699e-152">Sum of tax values.</span></span>
            - <span data-ttu-id="5699e-153">Sumar el valor mínimo del índice de impuestos.</span><span class="sxs-lookup"><span data-stu-id="5699e-153">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="5699e-154">La distribución de modelo en esta configuración implementa el modelo de datos base de todos los formatos ER creados para este modelo y ejecutados en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5699e-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="5699e-155">Como consecuencia, el contenido de los orígenes de datos **Impuesto** y **Gr** se expone para los formatos de ER como orígenes de datos abstractos.</span><span class="sxs-lookup"><span data-stu-id="5699e-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Página de diseñador de distribución de modelo que muestra los orígenes de datos Impuesto y Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="5699e-157">Cierre la página **Diseñador de distribución del modelo**.</span><span class="sxs-lookup"><span data-stu-id="5699e-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="5699e-158">Cierre la página **Distribución del modelo**.</span><span class="sxs-lookup"><span data-stu-id="5699e-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="5699e-159">Formato de revisión</span><span class="sxs-lookup"><span data-stu-id="5699e-159">Review format</span></span>

1. <span data-ttu-id="5699e-160">En el árbol de configuración, expanda el contenido del elemento **Modele para aprender llamadas con parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5699e-161">Seleccione **Formato para aprender llamadas con parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5699e-162">Seleccione **Diseñador**.</span><span class="sxs-lookup"><span data-stu-id="5699e-162">Select **Designer**.</span></span> <span data-ttu-id="5699e-163">Este formato de ER está diseñado para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5699e-163">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="5699e-164">Genere un extracto impositivo en formato XML.</span><span class="sxs-lookup"><span data-stu-id="5699e-164">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="5699e-165">Mostrar los siguientes niveles de impuestos en el extracto de impuestos: regular, reducido, y ninguno.</span><span class="sxs-lookup"><span data-stu-id="5699e-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="5699e-166">Actuales varois detalles en cada nivel de impuestos y tener un número distinto de detalles en cada nivel.</span><span class="sxs-lookup"><span data-stu-id="5699e-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Página de diseñador de formato](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="5699e-168">Seleccione **Asignación**.</span><span class="sxs-lookup"><span data-stu-id="5699e-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="5699e-169">Expanda las entradas **Modelo**, **Datos,** y **Resumen**.</span><span class="sxs-lookup"><span data-stu-id="5699e-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="5699e-170">El campo calculado **Model.Data.Summary.Level** contiene la expresión que devuelve el código del nivel de impuestos (**Regular**, **Reducido**, **Ninguno,** o **Otro**) como valor de texto para cualquier código de impuestos que se puede recuperar del origen de datos **Model.Data.Summary** en el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5699e-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![La página del diseñador del formato que muestra los detalles del modelo de datos Model para aprender las llamadas con parámetros](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="5699e-172">Expanda **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="5699e-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="5699e-173">Expanda **Model**.**Data2Summary2**.</span><span class="sxs-lookup"><span data-stu-id="5699e-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="5699e-174">El origen de datos **Model**.**Data2.Summary2** está configurado para agrupar los detalles de transacción del origen de datos **Model.Data.Summary** por el nivel de impuestos (devuelto por el campo calculado **Model.Data.Summary.Level** ) y calcular las agregaciones.</span><span class="sxs-lookup"><span data-stu-id="5699e-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Página del diseñador del formato que muestra los detalles del origen de datos Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="5699e-176">Revise los campos calculados **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, y **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="5699e-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="5699e-177">Estos campos calculados se usan para filtrar la lista de registros de **Model**.**Data2.Summary2** y devolver solamente los registros que representan un nivel determinado de los impuestos.</span><span class="sxs-lookup"><span data-stu-id="5699e-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="5699e-178">Cierre la página **Diseñador de formato**.</span><span class="sxs-lookup"><span data-stu-id="5699e-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="5699e-179">Crear un formato derivado</span><span class="sxs-lookup"><span data-stu-id="5699e-179">Create a derived format</span></span>
<span data-ttu-id="5699e-180">Puede mejorar el formato proporcionado agregando un campo calculado para filtrar el nivel impositivo requerido en lugar de utilizar los tres campos existentes: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** y **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="5699e-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="5699e-181">El nivel necesario de impuestos se puede especificar en la ubicación donde se llamará a este nuevo campo calculado.</span><span class="sxs-lookup"><span data-stu-id="5699e-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="5699e-182">En el árbol de configuración, expanda el contenido del elemento **Modele para aprender llamadas con parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5699e-183">Seleccione **Formato para aprender llamadas con parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5699e-184">Seleccionar **Crear configuración**.</span><span class="sxs-lookup"><span data-stu-id="5699e-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="5699e-185">Seleccione **Derivar de nombre: Formato para aprender las llamadas con parámetros, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="5699e-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="5699e-186">En el campo **Nombre**, introduzca **Formato para aprender llamadas con parámetros (personalizado)**.</span><span class="sxs-lookup"><span data-stu-id="5699e-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="5699e-187">Seleccione **Crear configuración.**</span><span class="sxs-lookup"><span data-stu-id="5699e-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="5699e-188">Configurar un campo calculado con parámetros que devuelve una lista de registros</span><span class="sxs-lookup"><span data-stu-id="5699e-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="5699e-189">Empezar a agregar un nuevo campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="5699e-190">Seleccione **Diseñador**.</span><span class="sxs-lookup"><span data-stu-id="5699e-190">Select **Designer**.</span></span>
2. <span data-ttu-id="5699e-191">Seleccione **Expandir o contraer/** para expandir todos los elementos de formato.</span><span class="sxs-lookup"><span data-stu-id="5699e-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="5699e-192">Seleccione **Asignación**.</span><span class="sxs-lookup"><span data-stu-id="5699e-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="5699e-193">Expanda el elemento **Model**.</span><span class="sxs-lookup"><span data-stu-id="5699e-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="5699e-194">Seleccione **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="5699e-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="5699e-195">Seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-195">Select **Add**.</span></span>
7. <span data-ttu-id="5699e-196">Seleccione **Funciones\\Campo calculado**.</span><span class="sxs-lookup"><span data-stu-id="5699e-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="5699e-197">En el campo **Nombre**, especifique **Niveles**.</span><span class="sxs-lookup"><span data-stu-id="5699e-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="5699e-198">Seleccione **Editar fórmula**.</span><span class="sxs-lookup"><span data-stu-id="5699e-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="5699e-199">Definir un parámetro para agregar un campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="5699e-200">Seleccione **Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="5699e-201">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="5699e-201">Select **New**.</span></span>
3. <span data-ttu-id="5699e-202">En el campo **Nombre**, introduzca **Nivel impositivo**.</span><span class="sxs-lookup"><span data-stu-id="5699e-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="5699e-203">En el campo **Tipo**, seleccione **Cadena**.</span><span class="sxs-lookup"><span data-stu-id="5699e-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="5699e-204">Solo los tipos de datos primitivos se pueden utilizar para especificar el tipo de argumento de parámetros.</span><span class="sxs-lookup"><span data-stu-id="5699e-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="5699e-205">Por lo tanto, los tipos **Lista de registro**, **registro**, y **Enumeración** no se pueden usar con este propósito.</span><span class="sxs-lookup"><span data-stu-id="5699e-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="5699e-206">El número máximo de parámetros que se pueden especificar para un solo campo calculado es 8.</span><span class="sxs-lookup"><span data-stu-id="5699e-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Lista de orígenes de datos de parámetros](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="5699e-208">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-208">Select **OK**.</span></span>

<span data-ttu-id="5699e-209">Si agrega este parámetro, especifica la condición que debe existir en lugar de llamar a este campo calculado.</span><span class="sxs-lookup"><span data-stu-id="5699e-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="5699e-210">Cuando llama a este campo calculado, debe especificar argumento del parámetro **Nivel impositivo** como valor con el formato **Cadena**.</span><span class="sxs-lookup"><span data-stu-id="5699e-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="5699e-211">Asegúrese de definir parámetros solo para los campos calculados que residen en un contenedor ( **Lista de registros**, **registro**, o **Contenedor**).</span><span class="sxs-lookup"><span data-stu-id="5699e-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="5699e-212">El parámetro configurado está disponible en la lista de orígenes de datos de este campo calculado.</span><span class="sxs-lookup"><span data-stu-id="5699e-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="5699e-213">Puede agregar el parámetro a la expresión configurada seleccionando **Agregar origen de datos**.</span><span class="sxs-lookup"><span data-stu-id="5699e-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Campo del origen de datos](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="5699e-215">Definir una expresión para agregar un campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="5699e-216">En el campo **Fórmula**, escriba:</span><span class="sxs-lookup"><span data-stu-id="5699e-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="5699e-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="5699e-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="5699e-218">Seleccione el parámetro **Nivel impositivo** en la lista de orígenes de datos.</span><span class="sxs-lookup"><span data-stu-id="5699e-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="5699e-219">Seleccione **Agregar origen de datos**.</span><span class="sxs-lookup"><span data-stu-id="5699e-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="5699e-220">En el campo **Fórmula**, finalice la expresión como:</span><span class="sxs-lookup"><span data-stu-id="5699e-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="5699e-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="5699e-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="5699e-222">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-222">Select **Save**.</span></span>

    ![Información del campo de origen de datos](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="5699e-224">Cierre la página **Diseñador de fórmula**.</span><span class="sxs-lookup"><span data-stu-id="5699e-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="5699e-225">Terminar de agregar un nuevo campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="5699e-226">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-226">Select **OK**.</span></span>

<span data-ttu-id="5699e-227">En la página **Diseñador de formato**, el campo calculado configurado con parámetros **Niveles** requiere un argumento **Cadena**.</span><span class="sxs-lookup"><span data-stu-id="5699e-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Lista ampliada de niveles del campo calculado](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="5699e-229">Use el campo calculado configurado para vincular elementos del formato</span><span class="sxs-lookup"><span data-stu-id="5699e-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="5699e-230">Seleccione **Model.Data2.Levels** para seleccionar el campo calculado configurado.</span><span class="sxs-lookup"><span data-stu-id="5699e-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="5699e-231">Seleccione el elemento de formato **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="5699e-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="5699e-232">Seleccione **Enlazar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-232">Select **Bind**.</span></span>
4. <span data-ttu-id="5699e-233">Seleccione **Sí** para confirmar la sustitución del origen de datos usado actualmente, **Level1**, para el nuevo origen de datos, **Niveles**, en todos los elementos del formato anidados del elemento del formato seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5699e-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="5699e-234">La vinculación aplicada se ha creado como una llamada del campo calculado con parámetros.</span><span class="sxs-lookup"><span data-stu-id="5699e-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="5699e-235">De forma predeterminada, el nombre del elemento de formato vinculado se usa como argumento para el campo calculado con parámetros en las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="5699e-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="5699e-236">El campo calculado se configura para usar un único parámetro.</span><span class="sxs-lookup"><span data-stu-id="5699e-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="5699e-237">El tipo de datos de este parámetro se define como **Cadena**.</span><span class="sxs-lookup"><span data-stu-id="5699e-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="5699e-238">Cuando el nombre del elemento de formato vinculado está en blanco, el nombre del origen de datos de este elemento se usa en el vínculo aplicado.</span><span class="sxs-lookup"><span data-stu-id="5699e-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="5699e-239">Seleccione el elemento de formato **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="5699e-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="5699e-240">Seleccione **Enlazar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-240">Select **Bind**.</span></span>
7. <span data-ttu-id="5699e-241">Seleccione **Sí** para confirmar la sustitución del origen de datos usado actualmente, **Level2**, para el nuevo origen de datos, **Niveles**, en todos los elementos del formato anidados en el elemento del formato seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5699e-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="5699e-242">Seleccione el elemento de formato **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="5699e-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="5699e-243">Seleccione **Enlazar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-243">Select **Bind**.</span></span>
10. <span data-ttu-id="5699e-244">Seleccione **Sí** para confirmar la sustitución del origen de datos usado actualmente, **Level3**, para el nuevo origen de datos, **Niveles**, en todos los elementos del formato anidados en el elemento del formato seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5699e-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="5699e-245">Cuando se especifica el argumento del campo calculado con parámetros para el elemento XML que representa el nivel de impuestos (por ejemplo, **Model.Data2.Levels ("Reduced")** como valor de texto), no es necesario hacer lo mismo para atributos XML anidados -sus vínculos heredarán automáticamente el valor del argumento definido en el nivel principal (**Model.Data2.Levels.aggregated.Base**, no **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="5699e-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="5699e-246">Las llamadas periódicas de cualquier campo calculado con parámetros no se admiten.</span><span class="sxs-lookup"><span data-stu-id="5699e-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="5699e-247">Puede seleccionar **Editar fórmula** y cambiar el argumento aplicado de forma predeterminada del campo calculado con parámetros del vínculo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5699e-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="5699e-248">Si falta este argumento, puede producir errores en tiempo de ejecución — se informa a los usuarios sobre esta situación cuando se valida el formato actual.</span><span class="sxs-lookup"><span data-stu-id="5699e-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Notificación de aviso de validación](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="5699e-250">Configurar un campo calculado con parámetros para devolver un registro</span><span class="sxs-lookup"><span data-stu-id="5699e-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="5699e-251">Cuando un campo calculado con parámetros devuelve un registro, necesita admitir el vínculo de campos individuales de este registro para dar formato a elementos.</span><span class="sxs-lookup"><span data-stu-id="5699e-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="5699e-252">En casos como éste no habrá vinculación principal que contenga el valor de un argumento para llamar a un campo calculado con parámetros —este valor debe definirse en la vinculación del campo de un único registro.</span><span class="sxs-lookup"><span data-stu-id="5699e-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="5699e-253">Empezar a agregar un nuevo campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="5699e-254">Seleccione **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="5699e-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="5699e-255">Seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-255">Select **Add**.</span></span>
3. <span data-ttu-id="5699e-256">Seleccione **Funciones\\Campo calculado**.</span><span class="sxs-lookup"><span data-stu-id="5699e-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="5699e-257">En el campo **Nombre**, especifique **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="5699e-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="5699e-258">Seleccione **Editar fórmula**.</span><span class="sxs-lookup"><span data-stu-id="5699e-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="5699e-259">Definir un parámetro para agregar un campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="5699e-260">Seleccione **Parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="5699e-261">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="5699e-261">Select **New**.</span></span>
3. <span data-ttu-id="5699e-262">En el campo **Nombre**, introduzca **Nivel impositivo**.</span><span class="sxs-lookup"><span data-stu-id="5699e-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="5699e-263">En el campo **Tipo**, seleccione **Cadena**.</span><span class="sxs-lookup"><span data-stu-id="5699e-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="5699e-264">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="5699e-265">Definir una expresión para agregar un campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="5699e-266">En el campo **Fórmula**, introduzca lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5699e-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="5699e-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="5699e-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="5699e-268">Seleccione el parámetro **Nivel impositivo**.</span><span class="sxs-lookup"><span data-stu-id="5699e-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="5699e-269">Seleccione **Agregar origen de datos**.</span><span class="sxs-lookup"><span data-stu-id="5699e-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="5699e-270">En el campo **Fórmula**, anexe **'Taxation Level'))** a lo que especificó en el paso 1 para finalizar la expresión a:</span><span class="sxs-lookup"><span data-stu-id="5699e-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="5699e-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="5699e-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="5699e-272">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-272">Select **Save**.</span></span>
6. <span data-ttu-id="5699e-273">Cierre la página **Diseñador de fórmula**.</span><span class="sxs-lookup"><span data-stu-id="5699e-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="5699e-274">Terminar de agregar un nuevo campo calculado</span><span class="sxs-lookup"><span data-stu-id="5699e-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="5699e-275">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="5699e-276">Use el campo calculado configurado para vincular elementos del formato</span><span class="sxs-lookup"><span data-stu-id="5699e-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="5699e-277">Expanda **Model.Data2.LevelRecord** para seleccionar el campo calculado configurado.</span><span class="sxs-lookup"><span data-stu-id="5699e-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="5699e-278">Expanda el contenedor **Model.Data2.LevelRecord.aggregated** del campo calculado configurado.</span><span class="sxs-lookup"><span data-stu-id="5699e-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="5699e-279">Seleccione el campo **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="5699e-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="5699e-280">Seleccione el elemento de formato **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="5699e-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="5699e-281">Seleccione **Desenlazar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="5699e-282">Seleccione el elemento de formato **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="5699e-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="5699e-283">Seleccione **Enlazar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-283">Select **Bind**.</span></span>
8. <span data-ttu-id="5699e-284">Seleccione **Editar fórmula**.</span><span class="sxs-lookup"><span data-stu-id="5699e-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="5699e-285">Cambie la expresión a **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="5699e-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Expresión actualizada](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="5699e-287">Quite los campos calculados que no se utilizan</span><span class="sxs-lookup"><span data-stu-id="5699e-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="5699e-288">Seleccione **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="5699e-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="5699e-289">Seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-289">Select **Delete**.</span></span>
3. <span data-ttu-id="5699e-290">Seleccione **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="5699e-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="5699e-291">Seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-291">Select **Delete**.</span></span>
5. <span data-ttu-id="5699e-292">Seleccione **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="5699e-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="5699e-293">Seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-293">Select **Delete**.</span></span>
7. <span data-ttu-id="5699e-294">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5699e-295">Se reusó el mismo campo calculado **Model.Data2.Levels** varias veces en vínculos de formato.</span><span class="sxs-lookup"><span data-stu-id="5699e-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="5699e-296">Es mucho más fácil utilizar y mantener un único campo calculado en lugar de hacerlo para varios campos similares.</span><span class="sxs-lookup"><span data-stu-id="5699e-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="5699e-297">Cierre la página **Diseñador de formato**.</span><span class="sxs-lookup"><span data-stu-id="5699e-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="5699e-298">Completar la versión ajustada de un formato derivado</span><span class="sxs-lookup"><span data-stu-id="5699e-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="5699e-299">En la ficha desplegable **Versiones**, seleccione **Cambiar estado**.</span><span class="sxs-lookup"><span data-stu-id="5699e-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="5699e-300">Seleccione **Completar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="5699e-301">Exportar la versión completada de un formato derivado</span><span class="sxs-lookup"><span data-stu-id="5699e-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="5699e-302">Seleccione el formato **Formato para aprender llamadas con parámetros (personalizado)** en el árbol de las configuraciones.</span><span class="sxs-lookup"><span data-stu-id="5699e-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="5699e-303">En la ficha desplegable **Versiones**, seleccione la versión 1.1.1 completa.</span><span class="sxs-lookup"><span data-stu-id="5699e-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="5699e-304">Seleccione **Intercambiar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="5699e-305">Seleccione **Exportar como archivo XML**.</span><span class="sxs-lookup"><span data-stu-id="5699e-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="5699e-306">Almacene la configuración descargada localmente, en formato XML.</span><span class="sxs-lookup"><span data-stu-id="5699e-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="5699e-307">Probar los formatos de ER</span><span class="sxs-lookup"><span data-stu-id="5699e-307">Test ER formats</span></span> 
<span data-ttu-id="5699e-308">Puede ejecutar los formatos de ER inicial y mejorado para asegurarse de que funcionan los campos calculados con parámetros configurados correctamente.</span><span class="sxs-lookup"><span data-stu-id="5699e-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="5699e-309">Importar configuraciones de ER</span><span class="sxs-lookup"><span data-stu-id="5699e-309">Import ER configurations</span></span>
<span data-ttu-id="5699e-310">Puede importar las configuraciones revisadas de RCS mediante el repositorio de ER del tipo **RCS**.</span><span class="sxs-lookup"><span data-stu-id="5699e-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="5699e-311">Si ya ha revisado los pasos en el tema, utilice el tema [Importar configuraciones de informes electrónicos (ER) desde Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use el repositorio de ER configurado para importar las configuraciones tratadas anteriormente en este tema a su entorno.</span><span class="sxs-lookup"><span data-stu-id="5699e-311">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="5699e-312">De lo contrario, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="5699e-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="5699e-313">Seleccione la empresa **DEMF** y en el panel predeterminado, seleccione **Informes electrónicos**.</span><span class="sxs-lookup"><span data-stu-id="5699e-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="5699e-314">Seleccione **Configuraciones de informes**.</span><span class="sxs-lookup"><span data-stu-id="5699e-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="5699e-315">Importe las configuraciones desde el Centro de descarga de Microsoft en la siguiente secuencia: modelo de datos, distribución de modelo, formato.</span><span class="sxs-lookup"><span data-stu-id="5699e-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="5699e-316">Realice los pasos siguientes para cada configuración de ER:</span><span class="sxs-lookup"><span data-stu-id="5699e-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="5699e-317">Seleccione **Intercambiar.**</span><span class="sxs-lookup"><span data-stu-id="5699e-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5699e-318">Seleccione **Cargar desde un archivo XML**.</span><span class="sxs-lookup"><span data-stu-id="5699e-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5699e-319">Seleccione **Examinar** para seleccionar la configuración necesaria de ER en formato XML.</span><span class="sxs-lookup"><span data-stu-id="5699e-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="5699e-320">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-320">Select **OK**.</span></span>

4. <span data-ttu-id="5699e-321">Importe la versión 1.1.1 completada de RCS de formato **Formato para aprender llamadas con parámetros (personalizado)**:</span><span class="sxs-lookup"><span data-stu-id="5699e-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="5699e-322">Seleccione **Intercambiar.**</span><span class="sxs-lookup"><span data-stu-id="5699e-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5699e-323">Seleccione **Cargar desde un archivo XML**.</span><span class="sxs-lookup"><span data-stu-id="5699e-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5699e-324">Seleccione **Examinar** para seleccionar el archivo almacenado localmente **Formato para aprender las llamadas con parámetros (personalizado)** en formato XML.</span><span class="sxs-lookup"><span data-stu-id="5699e-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="5699e-325">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5699e-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="5699e-326">Ejecutar los formatos de ER</span><span class="sxs-lookup"><span data-stu-id="5699e-326">Run ER formats</span></span>

1. <span data-ttu-id="5699e-327">En el árbol de configuración, expanda el contenido del elemento **Modele para aprender llamadas con parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5699e-328">Seleccione **Formato para aprender llamadas con parámetros**.</span><span class="sxs-lookup"><span data-stu-id="5699e-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5699e-329">Seleccione **Ejecutar** en la cinta de opciones superior.</span><span class="sxs-lookup"><span data-stu-id="5699e-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="5699e-330">Guarde la salida generada localmente.</span><span class="sxs-lookup"><span data-stu-id="5699e-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="5699e-331">Seleccione **Formato para aprender llamadas con parámetros (personalizado)**.</span><span class="sxs-lookup"><span data-stu-id="5699e-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="5699e-332">Seleccione **Ejecutar** en la cinta de opciones superior.</span><span class="sxs-lookup"><span data-stu-id="5699e-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="5699e-333">Guarde la salida generada localmente.</span><span class="sxs-lookup"><span data-stu-id="5699e-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="5699e-334">Compare el contenido de las salidas generadas.</span><span class="sxs-lookup"><span data-stu-id="5699e-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5699e-335">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5699e-335">Additional resources</span></span>
[<span data-ttu-id="5699e-336">Diseñador de fórmulas en los informes electrónicos (ER)</span><span class="sxs-lookup"><span data-stu-id="5699e-336">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)