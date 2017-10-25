--- 
title: "Registrar diarios periódicos"
description: "Los diarios periódicos a veces que se denominan diarios periódicos dado que el importe, el texto y otra información se repiten cada vez que se recupera el diario periódico."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8eae11e0501db78e467e517b29a2bc19f5765e75
ms.contentlocale: es-es
ms.lasthandoff: 09/29/2017

---
# <a name="post-periodic-journals"></a><span data-ttu-id="2e0a2-103">Registrar diarios periódicos</span><span class="sxs-lookup"><span data-stu-id="2e0a2-103">Post periodic journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e0a2-104">Los diarios periódicos a veces que se denominan diarios periódicos dado que el importe, el texto y otra información se repiten cada vez que se recupera el diario periódico.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="2e0a2-105">Al crear el diario periódico, se especifica el intervalo del período para la periodicidad, como días o meses.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="2e0a2-106">Esta guía de la tarea creará un diario periódico con una periodicidad mensual.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="2e0a2-107">Vaya a Contabilidad general > Tareas periódicas > Diarios periódicos.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="2e0a2-108">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-108">Click New.</span></span>
3. <span data-ttu-id="2e0a2-109">En el campo Nombre, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="2e0a2-110">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2e0a2-111">En el campo Descripción, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="2e0a2-112">La descripción será el nombre del diario periódico cuando se recupere más adelante, por lo que debe asegurarse de darle un nombre relevante.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="2e0a2-113">Haga clic en Líneas.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-113">Click Lines.</span></span>
    * <span data-ttu-id="2e0a2-114">Un diario periódico incluirá normalmente varias líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="2e0a2-115">En esta guía de tarea, no obstante, se agregará una sola línea.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="2e0a2-116">En el campo Fecha, escriba una fecha.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="2e0a2-117">El campo Fecha contiene la fecha de registro de la siguiente transferencia al diario.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="2e0a2-118">Para los diarios que se recuperarán cada mes, se recomienda usar la fecha del mes en que se registraron, normalmente la primera o última fecha del período.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="2e0a2-119">Es posible dejar en blanco el campo de fecha y ofrecer una fecha cuando se recupera el diario, mediante el campo Fecha vacía.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="2e0a2-120">El campo se actualiza automáticamente a la siguiente fecha que se repite cuando se recuperan las transacciones.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="2e0a2-121">En el campo Cuenta, especifique los valores deseados.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="2e0a2-122">En el campo Descripción, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="2e0a2-123">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-123">Close the page.</span></span>
11. <span data-ttu-id="2e0a2-124">En el campo Débito, escriba un número.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="2e0a2-125">En el campo Cuenta de contrapartida, especifique los valores deseados.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="2e0a2-126">En el campo Unidad, seleccione "Meses".</span><span class="sxs-lookup"><span data-stu-id="2e0a2-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="2e0a2-127">En el campo Número de unidades, escriba "1".</span><span class="sxs-lookup"><span data-stu-id="2e0a2-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="2e0a2-128">En el campo Última fecha, escriba una fecha.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="2e0a2-129">Especificar la última fecha del período anterior prevendrá que el diario periódico se cree por error en el período inicial incorrecto.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="2e0a2-130">La última fecha se actualizará después cada vez que se recupere el diario periódico.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="2e0a2-131">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-131">Click Save.</span></span>
17. <span data-ttu-id="2e0a2-132">Vaya al panel predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="2e0a2-133">Vaya a Contabilidad general > Movimientos de diario > Diarios generales.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="2e0a2-134">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-134">Click New.</span></span>
20. <span data-ttu-id="2e0a2-135">En el campo Nombre, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="2e0a2-136">En la lista, busque y seleccione el registro deseado.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="2e0a2-137">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="2e0a2-138">En el campo Descripción, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="2e0a2-139">Haga clic en Líneas.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-139">Click Lines.</span></span>
25. <span data-ttu-id="2e0a2-140">Haga clic en Diario del período.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-140">Click Period journal.</span></span>
26. <span data-ttu-id="2e0a2-141">Haga clic en Recuperar diario.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="2e0a2-142">Especifique una fecha en el campo Fecha final.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="2e0a2-143">La fecha final sirve como fecha de corte para las líneas periódicas del asiento.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="2e0a2-144">De acuerdo con la configuración de periodicidad, la última fecha y la fecha final para la misma línea se pueden incluir más de una vez en el diario resultante.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="2e0a2-145">La fecha final se actualiza automáticamente según la fecha de sesión de la última vez que la línea periódica se transfirió a un diario.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="2e0a2-146">En el campo Número de diario periódico, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="2e0a2-147">En la lista, haga clic en el vínculo de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="2e0a2-148">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="2e0a2-148">Click OK.</span></span>
    * <span data-ttu-id="2e0a2-149">El diario del período se puede revisar, aprobar o registrar ahora en función del requisito y la configuración.</span><span class="sxs-lookup"><span data-stu-id="2e0a2-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  

