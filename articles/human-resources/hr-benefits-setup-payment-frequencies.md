---
title: Configurar frecuencias de pago
description: ''
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
ms.openlocfilehash: e5fe0a16c4abbb9241fcdac88fd56e92bf04788c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010525"
---
# <a name="set-up-payment-frequencies"></a><span data-ttu-id="640e3-102">Configurar frecuencias de pago</span><span class="sxs-lookup"><span data-stu-id="640e3-102">Set up payment frequencies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="640e3-103">Microsoft Dynamics 365 Human Resources utiliza las frecuencias de pago para calcular el salario anual de prestaciones, determinar el importe de la prima de beneficios que un empleado paga en cada período de pago y definir la frecuencia con la que se realizan los pagos a los proveedores.</span><span class="sxs-lookup"><span data-stu-id="640e3-103">Microsoft Dynamics 365 Human Resources uses payment frequencies to calculate the annual benefit salary, determine the benefit premium amount an employee pays each pay period, and define the frequency payments are made to providers.</span></span>

<span data-ttu-id="640e3-104">Las frecuencias de pago de beneficios utilizan factores de conversión para convertir los períodos de pago de beneficios entre frecuencias de pago mensuales, semestrales, quincenales, semanales y diarias.</span><span class="sxs-lookup"><span data-stu-id="640e3-104">Benefit payment frequencies use conversion factors to convert benefit payment periods between monthly, semi-monthly, biweekly, weekly, and daily payment frequencies.</span></span> <span data-ttu-id="640e3-105">Esto permite a las empresas definir la interdependencia entre las frecuencias de pago dentro de un plan de beneficios.</span><span class="sxs-lookup"><span data-stu-id="640e3-105">This allows companies to define the interdependence between the payment frequencies within a benefit plan.</span></span>

<span data-ttu-id="640e3-106">Los campos de factores de conversión identifican el factor de conversión de la frecuencia de pago a los períodos de pago estándar y permiten que el sistema haga cálculos entre las frecuencias de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-106">The conversion factors fields identify the conversion factor from the payment frequency to the standard payment periods and allow the system to do calculations between payment frequencies.</span></span> <span data-ttu-id="640e3-107">La cantidad del factor de conversión también se usa para determinar la cantidad de la prima de beneficio que un empleado debe pagar cada frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-107">The conversion factor amount is also used to determine the benefit premium amount that an employee should pay each pay frequency.</span></span>

1. <span data-ttu-id="640e3-108">En el espacio de trabajo **Administración de prestaciones**, en **Configuración**, seleccione **Frecuencias de pago**.</span><span class="sxs-lookup"><span data-stu-id="640e3-108">In the **Benefits management** workspace, under **Setup**, select **Payment frequencies**.</span></span>

2. <span data-ttu-id="640e3-109">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="640e3-109">Select **New**.</span></span>

3. <span data-ttu-id="640e3-110">Especifique los valores para los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="640e3-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="640e3-111">Campo</span><span class="sxs-lookup"><span data-stu-id="640e3-111">Field</span></span> | <span data-ttu-id="640e3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="640e3-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="640e3-113">Frecuencia de pago</span><span class="sxs-lookup"><span data-stu-id="640e3-113">Payment frequency</span></span> | <span data-ttu-id="640e3-114">Un nombre de frecuencia de pago único.</span><span class="sxs-lookup"><span data-stu-id="640e3-114">A unique payment frequency name.</span></span> |
   | <span data-ttu-id="640e3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="640e3-115">Description</span></span> | <span data-ttu-id="640e3-116">Descripción de la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-116">A description of the payment frequency.</span></span> |
   | <span data-ttu-id="640e3-117">Período</span><span class="sxs-lookup"><span data-stu-id="640e3-117">Period</span></span> | <span data-ttu-id="640e3-118">El período adecuado que mejor se ajusta a la frecuencia de pago del proveedor de beneficios y del empleado.</span><span class="sxs-lookup"><span data-stu-id="640e3-118">The appropriate period that best matches the benefit provider’s and employee’s payment frequency.</span></span> <span data-ttu-id="640e3-119">La lista de períodos se compone de los períodos de pago estándar.</span><span class="sxs-lookup"><span data-stu-id="640e3-119">The period list is composed of the standard payment periods.</span></span> |
   | <span data-ttu-id="640e3-120">Número de períodos de pago</span><span class="sxs-lookup"><span data-stu-id="640e3-120">Number of pay periods</span></span> | <span data-ttu-id="640e3-121">El número de períodos de pago que representa la frecuencia con la que se paga al proveedor de beneficios o a los empleados.</span><span class="sxs-lookup"><span data-stu-id="640e3-121">The number of pay periods that represents how often the benefit provider or employees are paid.</span></span> <span data-ttu-id="640e3-122">Esta cantidad se utilizará para calcular el importe del salario de beneficio anual del empleado.</span><span class="sxs-lookup"><span data-stu-id="640e3-122">This amount will be used to calculate the employee‘s annual benefit salary amount.</span></span> |
   | <span data-ttu-id="640e3-123">Factor de conversión anual</span><span class="sxs-lookup"><span data-stu-id="640e3-123">Annual conversion factor</span></span> | <span data-ttu-id="640e3-124">El factor de conversión anual para la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-124">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="640e3-125">Por ejemplo, el factor de conversión anual para la frecuencia de pago mensual es:</span><span class="sxs-lookup"><span data-stu-id="640e3-125">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="640e3-126">(12 pagos mensuales / 1 año) = 12</span><span class="sxs-lookup"><span data-stu-id="640e3-126">(12 monthly payments / 1 year) = 12</span></span> |
   | <span data-ttu-id="640e3-127">Factor de conversión semestral</span><span class="sxs-lookup"><span data-stu-id="640e3-127">Semiannual conversion factor</span></span> | <span data-ttu-id="640e3-128">El factor de conversión semianual para la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-128">The semiannual conversion factor for the payment frequency.</span></span> <span data-ttu-id="640e3-129">Por ejemplo, el factor de conversión semianual para la frecuencia de pago mensual es:</span><span class="sxs-lookup"><span data-stu-id="640e3-129">For example, the semiannual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="640e3-130">(12 pagos mensuales / 2 veces al año) = 6</span><span class="sxs-lookup"><span data-stu-id="640e3-130">(12 monthly payments / 2 times a year) = 6</span></span> |
   | <span data-ttu-id="640e3-131">Factor de conversión trimestral</span><span class="sxs-lookup"><span data-stu-id="640e3-131">Quarterly conversion factor</span></span> | <span data-ttu-id="640e3-132">El factor de conversión trimestral para la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-132">The quarterly conversion factor for the payment frequency.</span></span> <span data-ttu-id="640e3-133">Por ejemplo, el factor de conversión trimestral para la frecuencia de pago mensual es:</span><span class="sxs-lookup"><span data-stu-id="640e3-133">For example, the quarterly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="640e3-134">(12 pagos mensuales / 4 trimestres) = 3</span><span class="sxs-lookup"><span data-stu-id="640e3-134">(12 monthly payments / 4 quarters) = 3</span></span> |
   | <span data-ttu-id="640e3-135">Factor de conversión mensual</span><span class="sxs-lookup"><span data-stu-id="640e3-135">Monthly conversion factor</span></span> | <span data-ttu-id="640e3-136">El factor de conversión mensual para la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-136">The monthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="640e3-137">Por ejemplo, el factor de conversión mensual para la frecuencia de pago mensual es:</span><span class="sxs-lookup"><span data-stu-id="640e3-137">For example, the monthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="640e3-138">(12 pagos mensuales / 12 meses) = 1</span><span class="sxs-lookup"><span data-stu-id="640e3-138">(12 monthly payments / 12 months) = 1</span></span> |
   | <span data-ttu-id="640e3-139">Factor de conversión bimensual</span><span class="sxs-lookup"><span data-stu-id="640e3-139">Semimonthly conversion factor</span></span> | <span data-ttu-id="640e3-140">El factor de conversión semimensual para la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-140">The semimonthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="640e3-141">Por ejemplo, el factor de conversión semimensual para la frecuencia de pago mensual es:</span><span class="sxs-lookup"><span data-stu-id="640e3-141">For example, the semimonthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="640e3-142">(12 pagos mensuales / 24 (2 veces al mes)) = 0,5</span><span class="sxs-lookup"><span data-stu-id="640e3-142">(12 monthly payments / 24 (2x a month)) = .5</span></span> | 
   | <span data-ttu-id="640e3-143">Factor de conversión quincenal</span><span class="sxs-lookup"><span data-stu-id="640e3-143">Biweekly conversion factor</span></span> | <span data-ttu-id="640e3-144">El factor de conversión anual para la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-144">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="640e3-145">Por ejemplo, el factor de conversión anual para la frecuencia de pago mensual es:</span><span class="sxs-lookup"><span data-stu-id="640e3-145">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="640e3-146">(12 pagos mensuales / 26 semanas) = 0,461538</span><span class="sxs-lookup"><span data-stu-id="640e3-146">(12 monthly payments / 26 weeks) = 0.461538</span></span> |
   | <span data-ttu-id="640e3-147">Factor de conversión semanal</span><span class="sxs-lookup"><span data-stu-id="640e3-147">Weekly conversion factor</span></span> | <span data-ttu-id="640e3-148">El factor de conversión anual para la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-148">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="640e3-149">Por ejemplo, el factor de conversión anual para la frecuencia de pago mensual es:</span><span class="sxs-lookup"><span data-stu-id="640e3-149">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="640e3-150">(12 pagos mensuales / 52 semanas) = 0,230769</span><span class="sxs-lookup"><span data-stu-id="640e3-150">(12 monthly payments / 52 weeks) = 0.230769</span></span> |
   | <span data-ttu-id="640e3-151">Factor de conversión diario</span><span class="sxs-lookup"><span data-stu-id="640e3-151">Daily conversion factor</span></span> | <span data-ttu-id="640e3-152">El factor de conversión anual para la frecuencia de pago.</span><span class="sxs-lookup"><span data-stu-id="640e3-152">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="640e3-153">Por ejemplo, el factor de conversión anual para la frecuencia de pago mensual es:</span><span class="sxs-lookup"><span data-stu-id="640e3-153">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="640e3-154">(12 pagos mensuales / 365 días) = 0,032877</span><span class="sxs-lookup"><span data-stu-id="640e3-154">(12 monthly payments / 365 days) = 0.032877</span></span> |

4. <span data-ttu-id="640e3-155">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="640e3-155">Select **Save**.</span></span> 