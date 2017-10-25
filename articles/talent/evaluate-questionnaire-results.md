---
title: Ver y evaluar los resultados de un cuestionario
description: "En este tema se explica cómo se pueden ver y evaluar los resultados de los cuestionarios que los encuestados completan."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 68dde5f6d67b48dad753e9f4c4123fb9e9e6b53a
ms.contentlocale: es-es
ms.lasthandoff: 09/29/2017

---

# <a name="view-and-evaluate-the-results-of-a-questionnaire"></a><span data-ttu-id="6b5d2-103">Ver y evaluar los resultados de un cuestionario</span><span class="sxs-lookup"><span data-stu-id="6b5d2-103">View and evaluate the results of a questionnaire</span></span>

<span data-ttu-id="6b5d2-104">En este tema se explica cómo se pueden ver y evaluar los resultados de los cuestionarios que los encuestados completan.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="6b5d2-105">Después de que los encuestados completen un cuestionario, puede ver y evaluar los resultados del mismo de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b5d2-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="6b5d2-106">**Sesiones de respuestas completadas**: ver los detalles sobre los cuestionarios que los encuestados han completado y generar informes para resumir respuestas y los puntos que se hayan obtenido.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="6b5d2-107">**Grupos de resultados**: ver los detalles y las estadísticas del grupo de resultados de los cuestionarios.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="6b5d2-108">Es posible generar estadísticas del grupo de resultados para una única sesión de respuestas de un cuestionario o todas las sesiones de respuestas.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="6b5d2-109">**Estadísticas de cuestionarios**: especificar los criterios para calcular las estadísticas de un grupo determinado de encuestados.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="6b5d2-110">También puede generar diversos informes para ver los resultados ordenados por persona, sesión de respuestas o grupo de resultados.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="6b5d2-111">Están disponibles los siguientes informes relacionados con cuestionarios completados:</span><span class="sxs-lookup"><span data-stu-id="6b5d2-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="6b5d2-112">Respuestas</span><span class="sxs-lookup"><span data-stu-id="6b5d2-112">Answers</span></span>
-   <span data-ttu-id="6b5d2-113">Respuestas por cuestionario</span><span class="sxs-lookup"><span data-stu-id="6b5d2-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="6b5d2-114">Respuestas por persona</span><span class="sxs-lookup"><span data-stu-id="6b5d2-114">Answers per person</span></span>
-   <span data-ttu-id="6b5d2-115">Análisis de realimentación</span><span class="sxs-lookup"><span data-stu-id="6b5d2-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="6b5d2-116">Resultados de la sesión de respuestas</span><span class="sxs-lookup"><span data-stu-id="6b5d2-116">Answer session results</span></span>
<span data-ttu-id="6b5d2-117">Cuando los encuestados completen un cuestionario, puede ver los resultados de las sesiones de respuestas completadas.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="6b5d2-118">Una sesión de respuestas es la respuesta de un usuario a un cuestionario.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="6b5d2-119">Puede ver los detalles acerca de las sesiones de respuestas completadas en la página **Respuestas**.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="6b5d2-120">Las sesiones de respuestas que se incluyen en la página **Respuestas** se filtran de diversas maneras, en función de cómo abra la página:</span><span class="sxs-lookup"><span data-stu-id="6b5d2-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="6b5d2-121">Todos los cuestionarios</span><span class="sxs-lookup"><span data-stu-id="6b5d2-121">All questionnaires</span></span>
-   <span data-ttu-id="6b5d2-122">Un cuestionario concreto</span><span class="sxs-lookup"><span data-stu-id="6b5d2-122">A specific questionnaire</span></span>
-   <span data-ttu-id="6b5d2-123">Una persona concreta</span><span class="sxs-lookup"><span data-stu-id="6b5d2-123">A specific person</span></span>

<span data-ttu-id="6b5d2-124">En la página **Respuestas**, puede ver los detalles sobre las respuestas, los puntos obtenidos, las respuestas de un encuestado en cada grupo de resultados y la jerarquía de preguntas que se usó en el cuestionario seleccionado, si se usó una jerarquía de preguntas.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="6b5d2-125">También puede generar e imprimir los informes siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b5d2-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="6b5d2-126">**Informe de resultados**: este informe muestra una representación gráfica de los puntos que se obtuvieron por grupo de resultados para la sesión de respuestas seleccionada.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="6b5d2-127">**Informe de respuestas**: este informe muestra las respuestas que el encuestado seleccionó para cada pregunta del cuestionario.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="6b5d2-128">**Respuestas incorrectas**: este informe muestra la información relacionada con las respuestas incorrectas que seleccionó el encuestado.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="6b5d2-129">**Nota:** el informe **Resultados** solo está disponible si usa grupos de resultados en el cuestionario y si seleccionó **Página de resultados** en la página **Cuestionarios**.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="6b5d2-130">Los informes **Respuesta** y **Respuestas incorrectas** solo están disponibles si seleccionó **Informe de respuestas** en la página**Cuestionarios**.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="6b5d2-131">Estadísticas de los cuestionarios</span><span class="sxs-lookup"><span data-stu-id="6b5d2-131">Questionnaire statistics</span></span>
<span data-ttu-id="6b5d2-132">Puede usar las estadísticas del cuestionario para analizar los resultados de un cuestionario completado sobre la base de cálculos que se definan.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="6b5d2-133">Para definir cálculos, debe completar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b5d2-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="6b5d2-134">Seleccionar un criterio para calcular y mostrar las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="6b5d2-135">Puede mostrar las estadísticas por cuestionario, preguntas, filas de preguntas o grupos de resultados.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="6b5d2-136">Seleccione el tipo de gráfico que se usará al ver resultados.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="6b5d2-137">Seleccionar el tipo de personas de la red, como empleados, personas de contacto o candidatos, para los que incluir respuestas.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="6b5d2-138">También puede incluir las respuestas de los cuestionarios que se completaron de manera anónima.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="6b5d2-139">Configurar intervalos sobre la base de edad o antigüedad para analizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="6b5d2-140">Seleccionar o comprobar la configuración que limita el sujeto de las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="6b5d2-141">Por ejemplo, al seleccionar un código postal, puede analizar los resultados para todos los encuestados dentro de un área geográfica específica.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="6b5d2-142">Seleccionar o comprobar los criterios para analizar los resultados según encuestado o según las características del cuestionario.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="6b5d2-143">Por ejemplo, al seleccionar un **código postal**, se puede analizar la correlación entre la ubicación del encuestado y las respuestas correctas.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="6b5d2-144">Los parámetros que defina se guardarán y se podrán usar para volver a calcular los resultados de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="6b5d2-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="see-also"></a><span data-ttu-id="6b5d2-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6b5d2-145">See also</span></span>
--------

[<span data-ttu-id="6b5d2-146">Diseñar cuestionarios</span><span class="sxs-lookup"><span data-stu-id="6b5d2-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="6b5d2-147">Uso de cuestionarios</span><span class="sxs-lookup"><span data-stu-id="6b5d2-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="6b5d2-148">Distribuir y completar cuestionarios</span><span class="sxs-lookup"><span data-stu-id="6b5d2-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

