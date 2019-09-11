---
title: Control de horas de trabajo
description: Este tema explica el control de las horas de trabajo en la Administración de activos.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918381"
---
# <a name="work-hour-control"></a><span data-ttu-id="81283-103">Control de horas de trabajo</span><span class="sxs-lookup"><span data-stu-id="81283-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="81283-104">En Administración de activos, puede calcular las horas para obtener una visión general de las horas reales comparadas con las horas del presupuesto sobre los activos, ubicaciones técnicas y órdenes de trabajo.</span><span class="sxs-lookup"><span data-stu-id="81283-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="81283-105">Las horas reales se basan en las transacciones registradas.</span><span class="sxs-lookup"><span data-stu-id="81283-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="81283-106">Control de horas de trabajo para los activos, las ubicaciones técnicas y las órdenes de trabajo</span><span class="sxs-lookup"><span data-stu-id="81283-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="81283-107">Los cálculos realizados para los activos, las ubicaciones técnicas y las órdenes de trabajo son idénticos casi.</span><span class="sxs-lookup"><span data-stu-id="81283-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="81283-108">Únicamente la diferencia es que en los activos y las ubicaciones técnicas, también puede incluir subactivos y sububicaciones en el cálculo.</span><span class="sxs-lookup"><span data-stu-id="81283-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="81283-109">La fecha es la fecha de la transacción en la que el registro se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="81283-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="81283-110">Haga clic en **Administración de activos** > **Consultas** > **Activos** > **Control de horas de activos** o **Control de horas de ubicación técnica** o **Administración de activos** > **Consultas** > **Órdenes de trabajo** > **Control de horas de órdenes de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="81283-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="81283-111">En el cuadro de diálogo **Control de horas de activos**.</span><span class="sxs-lookup"><span data-stu-id="81283-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="81283-112">En el diálogo **Control de horas de activos** / **Control de horas de ubicación técnica** / **Control de horas de órdenes de trabajo**, seleccione un período que se calculará en los campos **Desde fecha** y **Hasta fecha**.</span><span class="sxs-lookup"><span data-stu-id="81283-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="81283-113">Si es necesario, seleccione un **conjunto de dimensiones financieras** que se incluirá en el cálculo.</span><span class="sxs-lookup"><span data-stu-id="81283-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="81283-114">Seleccione "Sí" en el botón de alternar **Omitir cero** si no desea mostrar los resultados que contengan el valor cero horas.</span><span class="sxs-lookup"><span data-stu-id="81283-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="81283-115">Puede usar el campo **Nivel** para indicar el nivel de detalle que desea para las líneas de control de horas con respecto a las ubicaciones técnicas.</span><span class="sxs-lookup"><span data-stu-id="81283-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> <span data-ttu-id="81283-116">Por ejemplo, si especifica el número "1 "en el campo, y tiene una jerarquía de ubicación técnica de varios niveles, todas las líneas de control de horas de defectos del activo para una ubicación técnica se mostrarán en el nivel superior, y por tanto, las horas en una línea se pueden agregar desde las ubicaciones técnicas ubicadas en un nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="81283-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="81283-117">Si especifica el número "0 "en el campo **Nivel**, verá un resultado detallado que muestra todas las líneas de control de horas en todo el nivel de la ubicación técnica con el que están relacionadas.</span><span class="sxs-lookup"><span data-stu-id="81283-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="81283-118">Seleccione "Sí" en el botón de alternar **Incluir subactivos** para mostrar costes relacionados con los activos secundaria como líneas independientes.</span><span class="sxs-lookup"><span data-stu-id="81283-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="81283-119">Si desea limitar la búsqueda, puede seleccionar activos específicos, fechas de ubicaciones técnicas y órdenes de trabajo en la ficha desplegable **Registros a incluir**.</span><span class="sxs-lookup"><span data-stu-id="81283-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="81283-120">Haga clic en **Aceptar** para iniciar el cálculo.</span><span class="sxs-lookup"><span data-stu-id="81283-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="81283-121">En la página **Control de horas de activos**, en los grupos del panel de acciones **Agrupar por...**, haga clic en los botones relevantes para mostrar el nivel de detalle necesario del cálculo.</span><span class="sxs-lookup"><span data-stu-id="81283-121">On the **Asset hour control** page, in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="81283-122">Se resaltarán los botones del panel de acciones seleccionados.</span><span class="sxs-lookup"><span data-stu-id="81283-122">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="81283-123">Haga clic en un botón para activarlo o desactivarlo.</span><span class="sxs-lookup"><span data-stu-id="81283-123">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="81283-124">La ilustración siguiente muestra un ejemplo de un cálculo de **Control de horas de activos**.</span><span class="sxs-lookup"><span data-stu-id="81283-124">The figure below shows an example of an **Asset hour control** calculation.</span></span>

![Figura 1](media/04-controlling-and-reporting.png)

<span data-ttu-id="81283-126">Otra forma de realizar un cálculo de horas es seleccionar múltiples activos en **Todos los activos** o **Activos activos**.</span><span class="sxs-lookup"><span data-stu-id="81283-126">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="81283-127">A continuación, haga clic en el botón **Control de horas** de la ficha desplegable **General**.</span><span class="sxs-lookup"><span data-stu-id="81283-127">Then, you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="81283-128">Los activos seleccionados se insertan automáticamente en el campo **Activo** en la ficha desplegable **Registros que incluir**.</span><span class="sxs-lookup"><span data-stu-id="81283-128">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="81283-129">Haga clic en **Aceptar** en el diálogo **Control de horas de activos**, y el cálculo de los activos seleccionados se mostrará.</span><span class="sxs-lookup"><span data-stu-id="81283-129">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="81283-130">El mismo procedimiento se puede realizar para las ubicaciones técnicas en **Todas las ubicaciones técnicas** o **Ubicaciones técnicas activas**, y para las órdenes de trabajo en **Todas las órdenes de trabajo** o **Órdenes de trabajo activas**.</span><span class="sxs-lookup"><span data-stu-id="81283-130">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="81283-131">El campo **Presupuesto original** muestra las horas del presupuesto según la previsión de órdenes de trabajo.</span><span class="sxs-lookup"><span data-stu-id="81283-131">The **Original budget** field shows budget hours from the work order forecast.</span></span> <span data-ttu-id="81283-132">El campo **Horas reales** muestra las horas registradas en órdenes de trabajo.</span><span class="sxs-lookup"><span data-stu-id="81283-132">The **Actual hours** field shows posted hours on work orders.</span></span> <span data-ttu-id="81283-133">El campo **Horas comprometidas** muestra el total de horas a las que se comprometió la empresa con respecto a las órdenes de trabajo.</span><span class="sxs-lookup"><span data-stu-id="81283-133">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>
