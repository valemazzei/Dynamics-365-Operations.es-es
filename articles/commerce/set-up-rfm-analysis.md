---
title: Configurar análisis de novedad, frecuencia y monetario (RFM)
description: Este tema explica cómo configurar un análisis de novedad, frecuencia y monetario (RFM) de los clientes.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c7cb79fa82b579bee01e51cb635597cc5f711a98
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023952"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a><span data-ttu-id="e708a-103">Configurar análisis de novedad, frecuencia y monetario (RFM)</span><span class="sxs-lookup"><span data-stu-id="e708a-103">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e708a-104">Este tema explica cómo configurar un análisis de novedad, frecuencia y monetario (RFM) de los clientes.</span><span class="sxs-lookup"><span data-stu-id="e708a-104">This topic explains how to set up a Recency, Frequency, and Monetary (RFM) analysis of your customers.</span></span>

<span data-ttu-id="e708a-105">El análisis de RFM es una herramienta de marketing que su organización puede usar para evaluar los datos que se generan mediante las compras del cliente.</span><span class="sxs-lookup"><span data-stu-id="e708a-105">Recency, frequency, and monetary (RFM) analysis is a marketing tool that your organization can use to evaluate the data that is generated by customer purchases.</span></span> <span data-ttu-id="e708a-106">Después de configurar un análisis de RFM, a los clientes se les asigna una puntuación calculada de RFM mientras realizan compras.</span><span class="sxs-lookup"><span data-stu-id="e708a-106">After you set up RFM analysis, customers are assigned a calculated RFM score as they make purchases.</span></span> <span data-ttu-id="e708a-107">La puntuación de RFM puede ser una calificación de tres dígitos o un número global, en función de cómo haya configurado el análisis de RFM su organización.</span><span class="sxs-lookup"><span data-stu-id="e708a-107">The RFM score can be a three-digit rating or an aggregate number, depending on how your organization has configured RFM analysis.</span></span> <span data-ttu-id="e708a-108">Así es cómo funciona la calificación si su organización usa una calificación de tres dígitos para la puntuación:</span><span class="sxs-lookup"><span data-stu-id="e708a-108">Here's how the rating works if your organization uses a three-digit rating for the score:</span></span>

- <span data-ttu-id="e708a-109">El primer dígito es la grado de recencia del cliente, que se refiere a la última vez que un cliente hizo una compra en su organización.</span><span class="sxs-lookup"><span data-stu-id="e708a-109">The first digit is the customer's recency rating, which is how recently the customer made a purchase from your organization.</span></span>
- <span data-ttu-id="e708a-110">El segundo dígito es el grado de frecuencia del cliente, que se refiere a con qué frecuencia el cliente realiza compras en su organización.</span><span class="sxs-lookup"><span data-stu-id="e708a-110">The second digit is the customer's frequency rating, which is how often the customer makes purchases from your organization.</span></span>
- <span data-ttu-id="e708a-111">El tercer dígito es el grado del importe monetario del cliente, que se refiere a cuánto gasta el cliente cuando realiza compras en su organización.</span><span class="sxs-lookup"><span data-stu-id="e708a-111">The third digit is the customer's monetary rating, which is how much the customer spends when he makes purchases from your organization.</span></span>

<span data-ttu-id="e708a-112">Por ejemplo, su organización ha configurado las clasificaciones en una escala de 1 a 5, donde 5 es el grado más alto.</span><span class="sxs-lookup"><span data-stu-id="e708a-112">For example, your organization has set the ratings on a scale of 1 through 5, where 5 is the highest rating.</span></span> <span data-ttu-id="e708a-113">En este caso, una clasificación de cliente de 535 le indicará la siguiente información acerca del cliente:</span><span class="sxs-lookup"><span data-stu-id="e708a-113">In this case, a customer rating of 535 tells you the following information about the customer:</span></span>

- <span data-ttu-id="e708a-114">**Grado de proximidad de 5:** el cliente ha comprado recientemente.</span><span class="sxs-lookup"><span data-stu-id="e708a-114">**Recency rating of 5** – The customer recently made a purchase.</span></span>
- <span data-ttu-id="e708a-115">**Grado de frecuencia de 3:** el cliente compra productos de la organización con una frecuencia moderada.</span><span class="sxs-lookup"><span data-stu-id="e708a-115">**Frequency rating of 3** – The customer purchases products from your organization moderately often.</span></span>
- <span data-ttu-id="e708a-116">**Grado monetario de 5**: cuando el cliente realiza una compra, gasta un importe significativo de dinero.</span><span class="sxs-lookup"><span data-stu-id="e708a-116">**Monetary rating of 5** – When the customer makes a purchase, he spends a significant amount of money.</span></span>

<span data-ttu-id="e708a-117">Si su organización usa una calificación global de la puntuación, las puntuaciones se suman.</span><span class="sxs-lookup"><span data-stu-id="e708a-117">If your organization uses an aggregate number for the score, the individual ratings are added together.</span></span> <span data-ttu-id="e708a-118">Para el mismo ejemplo, el cliente tiene un puntuación de 13 (5 + 3 + 5).</span><span class="sxs-lookup"><span data-stu-id="e708a-118">For the same example, the customer has a rating of 13 (5 + 3 + 5).</span></span>

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a><span data-ttu-id="e708a-119">Configurar el análisis de RFM para clientes en su organización</span><span class="sxs-lookup"><span data-stu-id="e708a-119">Set up RFM analysis for the customers in your organization</span></span>

1. <span data-ttu-id="e708a-120">Vaya a **Centro de llamadas** \> **Periódico** \> **Análisis de RFM**.</span><span class="sxs-lookup"><span data-stu-id="e708a-120">Go to **Call center** \> **Periodic** \> **RFM analysis**.</span></span>
2. <span data-ttu-id="e708a-121">En la página **Análisis de RFM** , seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="e708a-121">On **RFM analysis** page, select **New**.</span></span> <span data-ttu-id="e708a-122">En el campo **Definición de RFM**, especifique un nombre para la definición del RFM.</span><span class="sxs-lookup"><span data-stu-id="e708a-122">In the **RFM definition** field, enter a name for the RFM definition.</span></span> <span data-ttu-id="e708a-123">Por ejemplo, podría llamar a la definición RFM-A.</span><span class="sxs-lookup"><span data-stu-id="e708a-123">For example, you could call the definition RFM-A.</span></span>
3. <span data-ttu-id="e708a-124">Escriba una fecha inicial y una fecha final para esta definición de RFM.</span><span class="sxs-lookup"><span data-stu-id="e708a-124">Enter a start date and end date for this RFM definition.</span></span>
4. <span data-ttu-id="e708a-125">En la ficha desplegable **General**, realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e708a-125">On the **General** FastTab, do the following:</span></span>

    - <span data-ttu-id="e708a-126">Si cada sección de la puntuación de RFM debe contener un recuento igual de clientes, seleccione la casilla **Distribución equitativa**.</span><span class="sxs-lookup"><span data-stu-id="e708a-126">If each section of the RFM score must contain an equal count of customers, select the **Even distribution** check box.</span></span>
    - <span data-ttu-id="e708a-127">Seleccione la casilla **Agregar puntuación** para agregar las tres puntuaciones.</span><span class="sxs-lookup"><span data-stu-id="e708a-127">Select the **Add scores** check box to aggregate the three scores.</span></span> <span data-ttu-id="e708a-128">Por ejemplo, esto daría al cliente una puntuación de RFM de 13 en lugar de 535.</span><span class="sxs-lookup"><span data-stu-id="e708a-128">For example, this would give a customer an RFM score of 13 instead of 535.</span></span>
    - <span data-ttu-id="e708a-129">Selecione la casilla **Guardar historial** para requerir que el sistema guarde los datos estadísticos de los clientes para poder utilizarlos para calcular la puntuación de RFM.</span><span class="sxs-lookup"><span data-stu-id="e708a-129">Select the **Save history** check box to require the system to save the statistical data for customers so that the data can be used to calculate the RFM score.</span></span>

5. <span data-ttu-id="e708a-130">En la ficha desplegable **Recencia**, realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e708a-130">On the **Recency** FastTab, do the following:</span></span>

    - <span data-ttu-id="e708a-131">En el campo **Divisiones**, especifique el número de divisiones o grupos, que se usarán para calcular la puntuación de recencia de los clientes.</span><span class="sxs-lookup"><span data-stu-id="e708a-131">In the **Divisions** field, enter the number of divisions, or groups, which will be used to calculate the recency score for customers.</span></span> <span data-ttu-id="e708a-132">Por ejemplo, si tiene 100 clientes, una división de 5 significa que hay 20 clientes para cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="e708a-132">For example, if you have 100 customers, a division of 5 means that there are 20 customers for each score.</span></span> <span data-ttu-id="e708a-133">Los 20 clientes que han realizado compras más recientemente tienen una puntuación de recencia de 5.</span><span class="sxs-lookup"><span data-stu-id="e708a-133">The 20 customers who have made purchases most recently have a recency score of 5.</span></span> <span data-ttu-id="e708a-134">Los siguientes 20 clientes tienen una puntuación de recencia de 4, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="e708a-134">The next 20 customers have a recency score of 4, and so on.</span></span> <span data-ttu-id="e708a-135">Si tiene 50 clientes, 10 clientes tienen una puntuación de novedad de 5, 10 tienen una puntuación de novedad de 4, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="e708a-135">If you have 50 customers, 10 customers have a recency score of 5, 10 have a recency score of 4, and so on.</span></span>
    - <span data-ttu-id="e708a-136">En el campo **Prioridad**, seleccione qué peso dar al parámetro de recencia en relación con los otros parámetros cuando se calcula la puntuación de RFM para un cliente.</span><span class="sxs-lookup"><span data-stu-id="e708a-136">In the **Priority** field, select how much weight to give the recency parameter in relation to the other parameters when the RFM score is calculated for a customer.</span></span> <span data-ttu-id="e708a-137">Por ejemplo, puede configurar más valor de la puntuación de novedad que para la puntuación monetaria.</span><span class="sxs-lookup"><span data-stu-id="e708a-137">For example, you might place more value on the recency score than the monetary score.</span></span>
    - <span data-ttu-id="e708a-138">En el campo **Multiplicador**, especifique el valor por el que multiplicar la puntuación de recencia.</span><span class="sxs-lookup"><span data-stu-id="e708a-138">In the **Multiplier** field, enter the value by which to multiply the recency score.</span></span> <span data-ttu-id="e708a-139">Si no escribe ningún valor, la puntuación no se multiplica.</span><span class="sxs-lookup"><span data-stu-id="e708a-139">If you do not enter a value, the score will not be multiplied.</span></span>
    - <span data-ttu-id="e708a-140">En el campo **Periodo**, seleccione el período de tiempo durante en el que se calcula la puntuación de recencia.</span><span class="sxs-lookup"><span data-stu-id="e708a-140">In the **Period** field, select the time period by which the recency score is calculated.</span></span> <span data-ttu-id="e708a-141">Por ejemplo, por semana o por mes.</span><span class="sxs-lookup"><span data-stu-id="e708a-141">For example, by week or by month.</span></span>

6. <span data-ttu-id="e708a-142">En la ficha desplegable **Frecuencia**, realice los siguiente:</span><span class="sxs-lookup"><span data-stu-id="e708a-142">On the **Frequency** FastTab, do the following:</span></span>

    - <span data-ttu-id="e708a-143">En el campo **Divisiones**, especifique el número de divisiones o grupos, que se usarán para calcular la puntuación de frecuencia de los clientes.</span><span class="sxs-lookup"><span data-stu-id="e708a-143">In the **Divisions** field, enter the number of divisions, or groups, which will be used to calculate the frequency score for customers.</span></span>
    - <span data-ttu-id="e708a-144">En el campo **Prioridad**, seleccione qué peso dar al parámetro de frecuencia en relación con los otros parámetros cuando se calcula la puntuación de RFM para un cliente.</span><span class="sxs-lookup"><span data-stu-id="e708a-144">In the **Priority** field, select how much weight to give the frequency parameter in relation to the others when the RFM score is calculated for a customer.</span></span>
    - <span data-ttu-id="e708a-145">En el campo **Multiplicador**, especifique el valor por el que multiplicar la puntuación de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="e708a-145">In the **Multiplier** field, enter the value by which to multiply the frequency score.</span></span> <span data-ttu-id="e708a-146">Si no escribe ningún valor, la puntuación no se multiplica.</span><span class="sxs-lookup"><span data-stu-id="e708a-146">If you do not enter a value, the score will not be multiplied.</span></span>

7. <span data-ttu-id="e708a-147">En la ficha desplegable **Monetaria**, realice los siguiente:</span><span class="sxs-lookup"><span data-stu-id="e708a-147">On the **Monetary** FastTab, do the following:</span></span>

    - <span data-ttu-id="e708a-148">En el campo **Divisiones**, especifique el número de divisiones o grupos, que se usarán para calcular la puntuación monetaria de los clientes.</span><span class="sxs-lookup"><span data-stu-id="e708a-148">In the **Divisions** field, enter the number of divisions, or groups, which will be used to calculate the monetary score for customers.</span></span>
    - <span data-ttu-id="e708a-149">En el campo **Prioridad**, seleccione qué peso dar al parámetro monetario en relación con los otros parámetros cuando se calcula la puntuación de RFM para un cliente.</span><span class="sxs-lookup"><span data-stu-id="e708a-149">In the **Priority** field, select how much weight to give the monetary parameter in relation to the others when the RFM score is calculated for a customer.</span></span>
    - <span data-ttu-id="e708a-150">En el campo **Multiplicador**, especifique el valor por el que multiplicar la puntuación monetaria.</span><span class="sxs-lookup"><span data-stu-id="e708a-150">In the **Multiplier** field, enter the value by which to multiply the monetary score.</span></span> <span data-ttu-id="e708a-151">Si no escribe ningún valor, la puntuación no se multiplica.</span><span class="sxs-lookup"><span data-stu-id="e708a-151">If you do not enter a value, the score will not be multiplied.</span></span>
    - <span data-ttu-id="e708a-152">En el campo **Bruto/neto**, seleccione si la puntuación monetaria del cliente debe calcularse usando el importe bruto o neto de la factura.</span><span class="sxs-lookup"><span data-stu-id="e708a-152">In the **Gross/net** field, select whether the customer's monetary score should be calculated by using the gross or net invoice amount.</span></span>
    - <span data-ttu-id="e708a-153">Si los importes de devolución de un cliente deben restarse de un cálculo total de la factura del cliente, seleccione la casilla **Restar devoluciones**.</span><span class="sxs-lookup"><span data-stu-id="e708a-153">If a customer's return amounts should be subtracted from the customer's total invoice calculation, select the **Subtract returns** check box.</span></span>

## <a name="view-a-customers-rfm-score"></a><span data-ttu-id="e708a-154">Ver el índice de RFM de un cliente</span><span class="sxs-lookup"><span data-stu-id="e708a-154">View a customer's RFM score</span></span>

<span data-ttu-id="e708a-155">Use este procedimiento para ver el índice de RFM de un cliente.</span><span class="sxs-lookup"><span data-stu-id="e708a-155">Use this procedure to view a customer's RFM score.</span></span>

1. <span data-ttu-id="e708a-156">Vaya a **Centro de llamadas** \> **Diarios** \> **Servicio al cliente**.</span><span class="sxs-lookup"><span data-stu-id="e708a-156">Go to **Call center** \> **Journals** \> **Customer service**.</span></span>
2. <span data-ttu-id="e708a-157">En la página **Servicio al cliente**, en el panel **Servicio al cliente**, en los campos de búsqueda, seleccione el tipo de palabra clave por el que se dese buscar y escriba el texto de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e708a-157">On the **Customer service** page, in the **Customer service** pane, in the search fields, select the keyword type to search on and enter the search text.</span></span>
3. <span data-ttu-id="e708a-158">Selección **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="e708a-158">Select **Search**.</span></span>
4. <span data-ttu-id="e708a-159">En la página **Búsqueda de clientes**, seleccione el registro de cliente que desee y, a continuación haga click en **Seleccionar cliente**.</span><span class="sxs-lookup"><span data-stu-id="e708a-159">On the **Customer search** page, select the customer record that you want, and then click **Select customer**.</span></span>

<span data-ttu-id="e708a-160">El índice de RFM se muestra en el grupo **Historial de pedidos** a la derecha de la página **Servicio al cliente**.</span><span class="sxs-lookup"><span data-stu-id="e708a-160">The RFM score is displayed in the **Order history** group on the right side of the **Customer service** page.</span></span>

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a><span data-ttu-id="e708a-161">Ver o borrar el historial de un registro de análisis de RFM</span><span class="sxs-lookup"><span data-stu-id="e708a-161">View or clear the history of an RFM analysis record</span></span>

<span data-ttu-id="e708a-162">Use este procedimiento para ver o borrar el historial de un registro de análisis de RFM.</span><span class="sxs-lookup"><span data-stu-id="e708a-162">Use this procedure to view or clear the history of an RFM analysis record.</span></span>

1. <span data-ttu-id="e708a-163">Vaya a **Centro de llamadas** \> **Periódico** \> **Análisis de RFM**.</span><span class="sxs-lookup"><span data-stu-id="e708a-163">Go to **Call center** \> **Periodic** \> **RFM analysis**.</span></span>
2. <span data-ttu-id="e708a-164">En la página **Análisis de RFM**, seleccione el registro que desea ver.</span><span class="sxs-lookup"><span data-stu-id="e708a-164">On the **RFM analysis** page, select the record that you want to view.</span></span>
3. <span data-ttu-id="e708a-165">Para ver el historial de registros, seleccione la ficha desplegable **Historial**.</span><span class="sxs-lookup"><span data-stu-id="e708a-165">To view the record history, select the **History** FastTab.</span></span>
4. <span data-ttu-id="e708a-166">Para eliminar el historial de registros, seleccione la ficha desplegable **Eliminar Historial**.</span><span class="sxs-lookup"><span data-stu-id="e708a-166">To clear the history of the record, select **Clear history**.</span></span>