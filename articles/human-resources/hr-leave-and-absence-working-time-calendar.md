---
title: Crear un calendario de horas de trabajo
description: Defina un calendario de horas de trabajo, días festivos y horas no laborables en Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 641f66c75875cfba51af3753223a070d7cb7dc50
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010505"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="14fe3-103">Crear un calendario de horas de trabajo</span><span class="sxs-lookup"><span data-stu-id="14fe3-103">Create a working time calendar</span></span>

<span data-ttu-id="14fe3-104">Un calendario de horas de trabajo en Dynamics 365 Human Resources muestra los días y las horas en que trabajan los empleados en su organización.</span><span class="sxs-lookup"><span data-stu-id="14fe3-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="14fe3-105">Cuando un empleado envía una solicitud de tiempo libre, no tiene que preocuparse de días festivos y cierres.</span><span class="sxs-lookup"><span data-stu-id="14fe3-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="14fe3-106">Para agilizar las solicitudes de tiempo libre, configure estos elementos para su organización:</span><span class="sxs-lookup"><span data-stu-id="14fe3-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="14fe3-107">Calendario de horario de trabajo</span><span class="sxs-lookup"><span data-stu-id="14fe3-107">Working time calendar</span></span>
- <span data-ttu-id="14fe3-108">Días festivos y cierres</span><span class="sxs-lookup"><span data-stu-id="14fe3-108">Holidays and closures</span></span>
- <span data-ttu-id="14fe3-109">Tiempo no laborable</span><span class="sxs-lookup"><span data-stu-id="14fe3-109">Non-work time</span></span>

<span data-ttu-id="14fe3-110">Puede agregar los dos últimos elementos mientras configura un calendario de horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="14fe3-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="14fe3-111">También puede configurarlos o actualizarlos por separado.</span><span class="sxs-lookup"><span data-stu-id="14fe3-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="14fe3-112">Configurar un calendario de horas de trabajo</span><span class="sxs-lookup"><span data-stu-id="14fe3-112">Set up a working time calendar</span></span>

<span data-ttu-id="14fe3-113">Configure al menos un calendario de tiempo laborable que muestre sus días y horas de operación.</span><span class="sxs-lookup"><span data-stu-id="14fe3-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="14fe3-114">Si tiene ubicaciones en varios países y regiones, es posible que desee configurar un calendario de tiempo de trabajo para cada área.</span><span class="sxs-lookup"><span data-stu-id="14fe3-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="14fe3-115">En la página **Administración de la organización**, seleccione **Calendarios**.</span><span class="sxs-lookup"><span data-stu-id="14fe3-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="14fe3-116">Seleccione **Nuevo** y especifique un nombre y una descripción para su calendario.</span><span class="sxs-lookup"><span data-stu-id="14fe3-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="14fe3-117">En **Opciones de generación**, seleccione los días laborales para su organización e introduzca las horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="14fe3-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="14fe3-118">Para agregar un día festivo o un cierre, seleccione el botón **Agregar** junto a **Días festivos y cierres**.</span><span class="sxs-lookup"><span data-stu-id="14fe3-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="14fe3-119">Para agregar tiempo no laborable, como almuerzos o descansos, seleccione **Agregar** debajo de **TIEMPO NO LABORABLE** e introduzca el nombre y el intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="14fe3-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="14fe3-120">En **Días**, seleccione **Generar** para generar los días en el calendario.</span><span class="sxs-lookup"><span data-stu-id="14fe3-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="14fe3-121">Introduzca el intervalo de fechas para su calendario y luego seleccione **Generar días**.</span><span class="sxs-lookup"><span data-stu-id="14fe3-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="14fe3-122">Para agregar horarios de trabajo, en **Programación de trabajos**, seleccione **Agregar** y luego introduzca las horas para cada horario de trabajo.</span><span class="sxs-lookup"><span data-stu-id="14fe3-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="14fe3-123">Configurar días festivos y cierres</span><span class="sxs-lookup"><span data-stu-id="14fe3-123">Configure holidays and closures</span></span>

<span data-ttu-id="14fe3-124">Puede agregar o cambiar días festivos y cierres por separado desde un calendario de horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="14fe3-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="14fe3-125">En la página **Administración de la organización**, seleccione **Días festivos y cierres**.</span><span class="sxs-lookup"><span data-stu-id="14fe3-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="14fe3-126">Seleccione **Nuevo** y especifique un nombre y una fecha para el día festivo o el cierre.</span><span class="sxs-lookup"><span data-stu-id="14fe3-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="14fe3-127">Configurar tiempo no laborable</span><span class="sxs-lookup"><span data-stu-id="14fe3-127">Configure non-work time</span></span>

<span data-ttu-id="14fe3-128">Puede agregar o cambiar horas no laborables por separado desde un calendario de horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="14fe3-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="14fe3-129">En la página **Administración de la organización**, seleccione **Tiempo no laborable**.</span><span class="sxs-lookup"><span data-stu-id="14fe3-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="14fe3-130">Seleccione **Nuevo** y especifique un nombre e intervalo de tiempo para el tiempo no laborable.</span><span class="sxs-lookup"><span data-stu-id="14fe3-130">Select **New** and enter a name and time range for the non-work time.</span></span>

## <a name="leave-and-absence-preview-feature"></a><span data-ttu-id="14fe3-131">Características de vista previa para permisos y ausencias</span><span class="sxs-lookup"><span data-stu-id="14fe3-131">Leave and absence preview feature</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

<span data-ttu-id="14fe3-132">Si ha habilitado la característica de vista previa de correcciones de días festivos de permisos y ausencias, Human Resources usa los días festivos y las fechas de cierre para determinar el número de días para ajustar para los empleados inscritos en el calendario.</span><span class="sxs-lookup"><span data-stu-id="14fe3-132">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="14fe3-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="14fe3-133">See also</span></span>

- [<span data-ttu-id="14fe3-134">Visión general de bajas y ausencias</span><span class="sxs-lookup"><span data-stu-id="14fe3-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="14fe3-135">Configurar tipos de permisos y ausencias</span><span class="sxs-lookup"><span data-stu-id="14fe3-135">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)