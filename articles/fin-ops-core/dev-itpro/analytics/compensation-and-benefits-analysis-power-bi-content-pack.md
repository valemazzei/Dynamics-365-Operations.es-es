---
title: Contenido de compensaciones y prestaciones de Power BI
description: Este tema describe el contenido de compensaciones y prestaciones de Power BI.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 96932c4ab32c004afb08fc9db2bf87bd5d5542d5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174291"
---
# <a name="compensation-and-benefits-power-bi-content"></a><span data-ttu-id="4b9b0-103">Contenido de compensaciones y prestaciones de Power BI</span><span class="sxs-lookup"><span data-stu-id="4b9b0-103">Compensation and Benefits Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b9b0-104">Este tema describe el contenido de compensaciones y prestaciones de Power BI.</span><span class="sxs-lookup"><span data-stu-id="4b9b0-104">This topic describes the Compensation and Benefits Power BI content.</span></span> 

## <a name="reports-that-are-included-in-the-content-pack"></a><span data-ttu-id="4b9b0-105">Informes que se incluyen en el paquete de contenido</span><span class="sxs-lookup"><span data-stu-id="4b9b0-105">Reports that are included in the content pack</span></span>
<span data-ttu-id="4b9b0-106">Tras conectar el paquete de contenido con sus datos, los informes muestran los datos de su organización.</span><span class="sxs-lookup"><span data-stu-id="4b9b0-106">After you've connected the content pack to your data, the reports show your organization's data.</span></span> <span data-ttu-id="4b9b0-107">Si nunca antes ha utilizado Microsoft Power BI, consulte [Aprendizaje dirigido para Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData) para obtener más información acerca de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b9b0-107">If you've never used Microsoft Power BI before, you can learn more about it on the [Guided Learning page for Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData).</span></span> <span data-ttu-id="4b9b0-108">Los informes incluidos en el paquete de contenido tienen gráficos y tablas que contienen información adicional.</span><span class="sxs-lookup"><span data-stu-id="4b9b0-108">The reports that are included in the content pack have both charts and tables that contain additional information.</span></span> <span data-ttu-id="4b9b0-109">En la siguiente tabla se describen los informes.</span><span class="sxs-lookup"><span data-stu-id="4b9b0-109">The following table describes the reports.</span></span>

| <span data-ttu-id="4b9b0-110">Informe</span><span class="sxs-lookup"><span data-stu-id="4b9b0-110">Report</span></span>                     | <span data-ttu-id="4b9b0-111">Contenido</span><span class="sxs-lookup"><span data-stu-id="4b9b0-111">Contents</span></span>                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9b0-112">Análisis de compensaciones y prestaciones</span><span class="sxs-lookup"><span data-stu-id="4b9b0-112">Comp and Benefits Analysis</span></span> | <span data-ttu-id="4b9b0-113">Empleados por hora y asalariados por empresa, sueldo por hora medio, sueldo medio de asalariado, empleados por tipo de empleo e inscripción del plan</span><span class="sxs-lookup"><span data-stu-id="4b9b0-113">Hourly and salaried employees by company, average hourly pay, average salaried pay, employees by employment type, and plan enrollment</span></span> |
| <span data-ttu-id="4b9b0-114">Prestaciones del empleado</span><span class="sxs-lookup"><span data-stu-id="4b9b0-114">Employee Benefits</span></span>          | <span data-ttu-id="4b9b0-115">Inscripción del empleado por prestación seleccionada</span><span class="sxs-lookup"><span data-stu-id="4b9b0-115">Employee enrollment by selected benefit</span></span>                                                                                               |

<span data-ttu-id="4b9b0-116">Puede filtrar los gráficos e iconos en estos informes y anclar los gráficos e iconos al panel de información.</span><span class="sxs-lookup"><span data-stu-id="4b9b0-116">You can filter the charts and tiles on these reports, and pin the charts and tiles to the dashboard.</span></span> <span data-ttu-id="4b9b0-117">Para obtener más información acerca de cómo filtrar y anclar en Power BI, consulte [Crear y configurar un panel de información](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span><span class="sxs-lookup"><span data-stu-id="4b9b0-117">For more information about how to filter and pin in Power BI, see [Create and Configure A Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="4b9b0-118">Comprensión del modelo de datos y de las entidades</span><span class="sxs-lookup"><span data-stu-id="4b9b0-118">Understanding the data model and entities</span></span>
<span data-ttu-id="4b9b0-119">Los datos de la aplicación se utilizan para rellenar los informes del paquete de contenido sobre compensaciones y prestaciones.</span><span class="sxs-lookup"><span data-stu-id="4b9b0-119">The application data is used to populate the reports in the Compensation and Benefits content pack.</span></span> <span data-ttu-id="4b9b0-120">En la tabla siguiente se muestran las entidades en las que se basaba el paquete de contenido.</span><span class="sxs-lookup"><span data-stu-id="4b9b0-120">The following table shows the entities that the content pack was based on.</span></span>

| <span data-ttu-id="4b9b0-121">Entidad</span><span class="sxs-lookup"><span data-stu-id="4b9b0-121">Entity</span></span>                            | <span data-ttu-id="4b9b0-122">Contenido</span><span class="sxs-lookup"><span data-stu-id="4b9b0-122">Contents</span></span>                                                                                                   | <span data-ttu-id="4b9b0-123">Relaciones con otras entidades</span><span class="sxs-lookup"><span data-stu-id="4b9b0-123">Relationships with other entities</span></span> |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="4b9b0-124">Workforce\_CalendarOffset</span><span class="sxs-lookup"><span data-stu-id="4b9b0-124">Workforce\_CalendarOffset</span></span>         | <span data-ttu-id="4b9b0-125">Desplazamientos del calendario para dividir informes</span><span class="sxs-lookup"><span data-stu-id="4b9b0-125">Calendar offsets to slice reports</span></span>                                                                          | <span data-ttu-id="4b9b0-126">Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_WorkerTrend, Workforce\_TerminatedWorker</span><span class="sxs-lookup"><span data-stu-id="4b9b0-126">Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_WorkerTrend, Workforce\_TerminatedWorker</span></span> |
| <span data-ttu-id="4b9b0-127">Workforce\_Company</span><span class="sxs-lookup"><span data-stu-id="4b9b0-127">Workforce\_Company</span></span>                | <span data-ttu-id="4b9b0-128">Empresas para filtrar informes por</span><span class="sxs-lookup"><span data-stu-id="4b9b0-128">Companies to filter reports by</span></span>                                                                             | <span data-ttu-id="4b9b0-129">Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-129">Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-130">Workforce\_Compensation</span><span class="sxs-lookup"><span data-stu-id="4b9b0-130">Workforce\_Compensation</span></span>           | <span data-ttu-id="4b9b0-131">Índice salaria y frecuencia a lo largo del tiempo</span><span class="sxs-lookup"><span data-stu-id="4b9b0-131">Pay rate and frequency over time</span></span>                                                                           | <span data-ttu-id="4b9b0-132">Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-132">Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-133">Workforce\_CurrentCompensation</span><span class="sxs-lookup"><span data-stu-id="4b9b0-133">Workforce\_CurrentCompensation</span></span>    | <span data-ttu-id="4b9b0-134">Índice salarial y frecuencia a partir de la fecha actual</span><span class="sxs-lookup"><span data-stu-id="4b9b0-134">Pay rate and frequency as of the current date</span></span>                                                              | <span data-ttu-id="4b9b0-135">Workforce\_Company, Workforce\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position</span><span class="sxs-lookup"><span data-stu-id="4b9b0-135">Workforce\_Company, Workforce\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position</span></span> |
| <span data-ttu-id="4b9b0-136">Workforce\_CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="4b9b0-136">Workforce\_CurrentPosition</span></span>        | <span data-ttu-id="4b9b0-137">Puestos a partir de la fecha actual, equivalentes a tiempo completo (FTE), vacantes y puestos vacantes a ocupados</span><span class="sxs-lookup"><span data-stu-id="4b9b0-137">Positions as of the current date, full-time equivalent (FTE), open positions, and open-to-filled positions</span></span> | <span data-ttu-id="4b9b0-138">Workforce\_Job, Workforce\_Position</span><span class="sxs-lookup"><span data-stu-id="4b9b0-138">Workforce\_Job, Workforce\_Position</span></span> |
| <span data-ttu-id="4b9b0-139">Workforce\_CurrentWorker</span><span class="sxs-lookup"><span data-stu-id="4b9b0-139">Workforce\_CurrentWorker</span></span>          | <span data-ttu-id="4b9b0-140">Trabajadores a partir de la fecha actual, edad y plantilla</span><span class="sxs-lookup"><span data-stu-id="4b9b0-140">Workers as of the current date, age, and headcount</span></span>                                                         | <span data-ttu-id="4b9b0-141">Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit</span><span class="sxs-lookup"><span data-stu-id="4b9b0-141">Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit</span></span> |
| <span data-ttu-id="4b9b0-142">Workforce\_Date</span><span class="sxs-lookup"><span data-stu-id="4b9b0-142">Workforce\_Date</span></span>                   | <span data-ttu-id="4b9b0-143">Días, semanas, meses y años</span><span class="sxs-lookup"><span data-stu-id="4b9b0-143">Days, weeks, months, and years</span></span>                                                                             | <span data-ttu-id="4b9b0-144">Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-144">Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-145">Workforce\_Demographics</span><span class="sxs-lookup"><span data-stu-id="4b9b0-145">Workforce\_Demographics</span></span>           | <span data-ttu-id="4b9b0-146">Fecha de nacimiento, género, origen étnico y estado civil</span><span class="sxs-lookup"><span data-stu-id="4b9b0-146">Date of birth, gender, ethnic origin, and marital status</span></span>                                                   | <span data-ttu-id="4b9b0-147">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-147">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-148">Workforce\_Employment</span><span class="sxs-lookup"><span data-stu-id="4b9b0-148">Workforce\_Employment</span></span>             | <span data-ttu-id="4b9b0-149">Fecha de inicio, fecha final y fecha de transición</span><span class="sxs-lookup"><span data-stu-id="4b9b0-149">Start date, end date, and transition date</span></span>                                                                  | <span data-ttu-id="4b9b0-150">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-150">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-151">Workforce\_GeographicLocation</span><span class="sxs-lookup"><span data-stu-id="4b9b0-151">Workforce\_GeographicLocation</span></span>     | <span data-ttu-id="4b9b0-152">Ciudad, provincia, código postal y comunidad autónoma</span><span class="sxs-lookup"><span data-stu-id="4b9b0-152">City, county, postal code, and state or province</span></span>                                                           | <span data-ttu-id="4b9b0-153">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-153">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-154">Workforce\_Job</span><span class="sxs-lookup"><span data-stu-id="4b9b0-154">Workforce\_Job</span></span>                    | <span data-ttu-id="4b9b0-155">Función tipo y cargo</span><span class="sxs-lookup"><span data-stu-id="4b9b0-155">Function, type, and title</span></span>                                                                                  | <span data-ttu-id="4b9b0-156">Workforce\_CurrentPosition, Workforce\_CurrentWorker</span><span class="sxs-lookup"><span data-stu-id="4b9b0-156">Workforce\_CurrentPosition, Workforce\_CurrentWorker</span></span> |
| <span data-ttu-id="4b9b0-157">Workforce\_PastPositionAssignment</span><span class="sxs-lookup"><span data-stu-id="4b9b0-157">Workforce\_PastPositionAssignment</span></span> | <span data-ttu-id="4b9b0-158">Motivo de la asignación, fecha de inicio, fecha final y trabajo</span><span class="sxs-lookup"><span data-stu-id="4b9b0-158">Assignment reason, start date, end date, and job</span></span>                                                           | <span data-ttu-id="4b9b0-159">Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position</span><span class="sxs-lookup"><span data-stu-id="4b9b0-159">Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position</span></span> |
| <span data-ttu-id="4b9b0-160">Workforce\_Performance</span><span class="sxs-lookup"><span data-stu-id="4b9b0-160">Workforce\_Performance</span></span>            | <span data-ttu-id="4b9b0-161">Calificación, descripción y modelo de calificación</span><span class="sxs-lookup"><span data-stu-id="4b9b0-161">Rating, description, and rating model</span></span>                                                                      | <span data-ttu-id="4b9b0-162">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-162">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-163">Workforce\_Position</span><span class="sxs-lookup"><span data-stu-id="4b9b0-163">Workforce\_Position</span></span>               | <span data-ttu-id="4b9b0-164">Departamento, FTE, puesto, tipo de puesto y cargo</span><span class="sxs-lookup"><span data-stu-id="4b9b0-164">Department, FTE, position, position type, and title</span></span>                                                        | <span data-ttu-id="4b9b0-165">Workforce\_CurrentPosition, Workforce\_CurrentWorker</span><span class="sxs-lookup"><span data-stu-id="4b9b0-165">Workforce\_CurrentPosition, Workforce\_CurrentWorker</span></span> |
| <span data-ttu-id="4b9b0-166">Workforce\_PositionTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-166">Workforce\_PositionTrend</span></span>          | <span data-ttu-id="4b9b0-167">Puestos a lo largo del tiempo, FTE y trabajo</span><span class="sxs-lookup"><span data-stu-id="4b9b0-167">Positions over time, FTE, and job</span></span>                                                                          | <span data-ttu-id="4b9b0-168">Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position</span><span class="sxs-lookup"><span data-stu-id="4b9b0-168">Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position</span></span> |
| <span data-ttu-id="4b9b0-169">Workforce\_ReportsToWorkerName</span><span class="sxs-lookup"><span data-stu-id="4b9b0-169">Workforce\_ReportsToWorkerName</span></span>    | <span data-ttu-id="4b9b0-170">Nombre, apellido y nombre completo</span><span class="sxs-lookup"><span data-stu-id="4b9b0-170">First name, last name, and full name</span></span>                                                                       | <span data-ttu-id="4b9b0-171">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-171">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-172">Workforce\_Skill</span><span class="sxs-lookup"><span data-stu-id="4b9b0-172">Workforce\_Skill</span></span>                  | <span data-ttu-id="4b9b0-173">Aptitudes, tipo de aptitud y calificación</span><span class="sxs-lookup"><span data-stu-id="4b9b0-173">Skill, skill type, and rating</span></span>                                                                              | |
| <span data-ttu-id="4b9b0-174">Workforce\_TerminatedWorker</span><span class="sxs-lookup"><span data-stu-id="4b9b0-174">Workforce\_TerminatedWorker</span></span>       | <span data-ttu-id="4b9b0-175">Trabajadores terminados, fecha de finalización, cargo, puesto y trabajo</span><span class="sxs-lookup"><span data-stu-id="4b9b0-175">Terminated workers, termination date, title, position, and job</span></span>                                             | <span data-ttu-id="4b9b0-176">Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit</span><span class="sxs-lookup"><span data-stu-id="4b9b0-176">Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit</span></span> |
| <span data-ttu-id="4b9b0-177">Workforce\_WorkerBenefit</span><span class="sxs-lookup"><span data-stu-id="4b9b0-177">Workforce\_WorkerBenefit</span></span>          | <span data-ttu-id="4b9b0-178">Fecha de vigencia, opción de prestación, plan de prestaciones y tipo de prestación</span><span class="sxs-lookup"><span data-stu-id="4b9b0-178">Effective date, benefit option, benefit plan, and benefit type</span></span>                                             | <span data-ttu-id="4b9b0-179">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-179">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-180">Workforce\_WorkerName</span><span class="sxs-lookup"><span data-stu-id="4b9b0-180">Workforce\_WorkerName</span></span>             | <span data-ttu-id="4b9b0-181">Nombre, apellido y nombre completo</span><span class="sxs-lookup"><span data-stu-id="4b9b0-181">First name, last name, and full name</span></span>                                                                       | <span data-ttu-id="4b9b0-182">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-182">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-183">Workforce\_WorkerTitle</span><span class="sxs-lookup"><span data-stu-id="4b9b0-183">Workforce\_WorkerTitle</span></span>            | <span data-ttu-id="4b9b0-184">Cargo y fecha de antigüedad</span><span class="sxs-lookup"><span data-stu-id="4b9b0-184">Title and seniority date</span></span>                                                                                   | <span data-ttu-id="4b9b0-185">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-185">Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend</span></span> |
| <span data-ttu-id="4b9b0-186">Workforce\_WorkerTrend</span><span class="sxs-lookup"><span data-stu-id="4b9b0-186">Workforce\_WorkerTrend</span></span>            | <span data-ttu-id="4b9b0-187">Trabajadores a lo largo del tiempo, plantilla, empresa y puesto</span><span class="sxs-lookup"><span data-stu-id="4b9b0-187">Workers over time, headcount, company, and position</span></span>                                                        | <span data-ttu-id="4b9b0-188">Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit</span><span class="sxs-lookup"><span data-stu-id="4b9b0-188">Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit</span></span> |