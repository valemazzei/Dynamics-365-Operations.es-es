---
title: Recomendaciones de productos en PDV
description: Este tema describe el uso de las recomendaciones de productos en un dispositivo de punto de venta (PDV).
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af0273ca1553d5fb371a20b8c96fd9a101f34815
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023980"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="33c84-103">Recomendaciones de producto en PDV</span><span class="sxs-lookup"><span data-stu-id="33c84-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33c84-104">En su base, las recomendaciones de productos son una aplicación empresarial de transformación que abarcan entre todos los aspectos de ventas al por menor para experiencias de detección de productos completas, atractivas y personalizadas.</span><span class="sxs-lookup"><span data-stu-id="33c84-104">At its core, product recommendations are a transformative business application that span across all retail spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="33c84-105">Para implementar esta característica en PDV, siga los pasos en [cómo agregar recomendaciones a los dispositivos de PDV.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="33c84-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="33c84-106">Para obtener más información sobre las características de recomendaciones de productos, lea la [información general sobre recomendaciones de productos.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="33c84-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="33c84-107">Situaciones</span><span class="sxs-lookup"><span data-stu-id="33c84-107">Scenarios</span></span>

<span data-ttu-id="33c84-108">Las recomendaciones de productos se habilitan para los siguientes escenarios de PDV.</span><span class="sxs-lookup"><span data-stu-id="33c84-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="33c84-109">Están disponibles en PDV en la nube o en PDV moderno (MPOS).</span><span class="sxs-lookup"><span data-stu-id="33c84-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="33c84-110">En la página **Detalles del producto**:</span><span class="sxs-lookup"><span data-stu-id="33c84-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="33c84-111">Si un empleado de tienda visita una página de **Detalles del producto** a la hora de buscar transacciones anteriores a través de distintos canales, el servicio de recomendación sugiere artículos adicionales que es probable que se adquieran de forma conjunta.</span><span class="sxs-lookup"><span data-stu-id="33c84-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="33c84-112">[![Recomendaciones en la página Detalles de producto](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="33c84-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="33c84-113">En la página **Transacción**:</span><span class="sxs-lookup"><span data-stu-id="33c84-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="33c84-114">El motor de recomendación sugiere artículos basados en la lista completa de artículos en la cesta que con frecuencia se adquieren conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="33c84-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="33c84-115">Para mostrar recomendaciones en la página **Transacción**, el minorista tiene que actualizar el diseño de la pantalla en Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="33c84-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="33c84-116">El control **Recomendaciones** debe quitarse de la página **Transacción**.</span><span class="sxs-lookup"><span data-stu-id="33c84-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="33c84-117">[![Recomendaciones de la página de la transacción](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="33c84-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="33c84-118">Configure Commerce para habilitar las recomendaciones de PDV</span><span class="sxs-lookup"><span data-stu-id="33c84-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="33c84-119">Siga estos pasos para configurar recomendaciones de productos:</span><span class="sxs-lookup"><span data-stu-id="33c84-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="33c84-120">Asegúrese de que el servicio se ha actualizado a la **compilación 10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="33c84-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="33c84-121">Siga las instrucciones de cómo [habilitar recomendaciones de productos](../commerce/enable-product-recommendations.md) para su negocio.</span><span class="sxs-lookup"><span data-stu-id="33c84-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="33c84-122">Opcional: para mostrar recomendaciones en la pantalla de transacción, vaya a **Diseño de pantalla**, elija su diseño de pantalla, inicie el **Diseñador de pantalla** y quite el control de **recomendaciones** cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="33c84-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="33c84-123">Vaya a **Parámetros de Commerce** seleccione **Aprendizaje automático** y seleccione **Sí** en **Habilitar recomendaciones de PDV**.</span><span class="sxs-lookup"><span data-stu-id="33c84-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="33c84-124">Para ver recomendaciones sobre el PDV, ejecute el trabajo de configuración global **1110**.</span><span class="sxs-lookup"><span data-stu-id="33c84-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="33c84-125">Para reflejar los cambios realizados en el diseñador de pantalla del PVD, ejecute el trabajo de configuración de canal **1070**.</span><span class="sxs-lookup"><span data-stu-id="33c84-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="33c84-126">Solucionar problemas donde tiene recomendaciones de productos ya habilitadas</span><span class="sxs-lookup"><span data-stu-id="33c84-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="33c84-127">Vaya a **Parámetros de Commerce** \> **Listas de recomendaciones** \> **Deshabilitar recomendaciones de productos** y ejecute **Trabajo de configuración global \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="33c84-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="33c84-128">Si agregó el **Control de recomendaciones** a su pantalla de transacción mediante el **Diseñador de pantalla**, quítelo también.</span><span class="sxs-lookup"><span data-stu-id="33c84-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="33c84-129">Si tiene preguntas adicionales, consulte [Preguntas más frecuentes sobre las recomendaciones del producto](../commerce/faq-recommendations.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="33c84-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33c84-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="33c84-130">Additional resources</span></span>

[<span data-ttu-id="33c84-131">Agregue un control de recomendaciones a la pantalla de transacción en dispositivos de PDV</span><span class="sxs-lookup"><span data-stu-id="33c84-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="33c84-132">Visión general de recomendaciones de producto</span><span class="sxs-lookup"><span data-stu-id="33c84-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="33c84-133">Habilitar recomendaciones de producto</span><span class="sxs-lookup"><span data-stu-id="33c84-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 