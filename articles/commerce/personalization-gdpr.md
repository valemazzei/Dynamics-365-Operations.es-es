---
title: Cancelar recomendaciones personalizadas
description: Este tema explica cómo puede permitir que los clientes opten por no recibir recomendaciones personalizadas en Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8e7b800218f68167901d86d61ae483680a04cfab
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025279"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="c6c3f-103">Cancelar recomendaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="c6c3f-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6c3f-104">Este tema explica cómo puede permitir que los clientes opten por no recibir recomendaciones personalizadas en Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c6c3f-105">Visión general</span><span class="sxs-lookup"><span data-stu-id="c6c3f-105">Overview</span></span>

<span data-ttu-id="c6c3f-106">Durante la creación de la cuenta, los nuevos clientes se configuran automáticamente para recibir recomendaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="c6c3f-107">Sin embargo, Dynamics 365 Commerce proporciona diversas formas para que los minoristas permitan a los usuarios optar por no recibir estas recomendaciones y restringir el procesamiento de sus datos personales.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="c6c3f-108">Los usuarios autenticados que opten por no recibir recomendaciones personalizadas dejarán de ver inmediatamente listas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="c6c3f-109">Además, todos los datos personales que se recopilan para la personalización se eliminarán de los modelos de recomendaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="c6c3f-110">Para obtener más información acerca de las recomendaciones de producto personalizadas, consulte [Habilitar recomendaciones personalizadas](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="c6c3f-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="c6c3f-111">Maneras para que los minoristas implementen una experiencia de exclusión voluntaria</span><span class="sxs-lookup"><span data-stu-id="c6c3f-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="c6c3f-112">Los minoristas tienen tres maneras de implementar una experiencia de exclusión voluntaria.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="c6c3f-113">Optar por no recibir en nombre de los usuarios</span><span class="sxs-lookup"><span data-stu-id="c6c3f-113">Opting out on behalf of users</span></span>

<span data-ttu-id="c6c3f-114">En la gestión de cuentas de la oficina administrativa de Commerce, los minoristas pueden optar por no participar en nombre de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="c6c3f-115">Desde la página de inicio del área de operaciones, busque **todos los clientes**.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="c6c3f-116">Busque y seleccione un cliente, y luego seleccione la ficha desplegable **Retail**.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Ficha desplegable Retail](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="c6c3f-118">Debajo de **Privacidad**, establezca la opción **Deshabilitar personalización** en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Configuración de privacidad](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="c6c3f-120">Seleccione **Guardar** y cierre la página.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="c6c3f-121">Experiencia de exclusión voluntaria basada en módulos</span><span class="sxs-lookup"><span data-stu-id="c6c3f-121">Module-based opt-out experience</span></span>

<span data-ttu-id="c6c3f-122">Los minoristas pueden permitir a los usuarios autenticados optar por no recibir recomendaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="c6c3f-123">Para proporcionar esta experiencia de exclusión, agregue el módulo de exclusión del usuario a las páginas de perfil de la cuenta del cliente.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="c6c3f-124">Extensiones personalizadas</span><span class="sxs-lookup"><span data-stu-id="c6c3f-124">Custom extensions</span></span>

<span data-ttu-id="c6c3f-125">Los minoristas pueden crear sus propias extensiones para administrar la experiencia de exclusión voluntaria para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="c6c3f-126">Para más información, consulte [Llamar a las API de Retail Server](e-commerce-extensibility/call-retail-server-apis.md) y [Extensibilidad de canal en línea](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6c3f-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="c6c3f-127">Obtener una copia digital de datos de recomendaciones personalizadas en nombre de un usuario autenticado</span><span class="sxs-lookup"><span data-stu-id="c6c3f-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="c6c3f-128">Los clientes pueden querer obtener una copia digital de sus datos personales y también ver una vista exportada de los resultados de sus recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="c6c3f-129">Si un cliente solicita esta información, el minorista debe crear una extensión personalizada que llame a la interfaz de programación de aplicaciones (API) de Retail Server y solicite los resultados completos de la lista **Picking para usted**, en función del id. del cliente.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="c6c3f-130">Los resultados se pueden exportar en formato de valores separados por comas (CSV) y compartir con el cliente.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="c6c3f-131">El siguiente ejemplo muestra cómo un minorista puede realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="c6c3f-132">El minorista crea una extensión personalizada para extraer datos de recomendaciones personales en nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="c6c3f-133">Para obtener información acerca de cómo crear módulos, clonar módulos existentes, llamar a las API de Retail Server y llamar a acciones de datos, consulte [Extensibilidad de canal en línea](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6c3f-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="c6c3f-134">La extensión personalizada realiza una llamada a la acción de datos principal **get-recommendations** y le pasa la información requerida, de acuerdo con los requisitos de la lista.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="c6c3f-135">En el caso de la lista **Picking para usted**, la extensión debe pasar el nombre correcto de la lista y el id. del cliente a la acción de datos.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="c6c3f-136">Una forma de crear la extensión personalizada es clonar el módulo de colección de productos existente que se utiliza para devolver los resultados de las recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="c6c3f-137">Al clonar este módulo existente, un minorista puede modificar el código existente y agregar un nuevo botón que exporte los resultados de las recomendaciones a un archivo CSV.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="c6c3f-138">Para más información, consulte [Clonar un módulo de kit de inicio](e-commerce-extensibility/clone-starter-module.md) y [Módulos de colección de productos](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6c3f-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="c6c3f-139">Para obtener una vista completa de la biblioteca API de Retail Server, consulte [API de cliente y de consumidor de Retail Server](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="c6c3f-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="c6c3f-140">Después de crear la extensión personalizada, el minorista puede exportar un archivo CSV de todos los resultados de las recomendaciones, en función del id. de cliente único del usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="c6c3f-141">El minorista puede compartir el archivo CSV exportado que contiene la lista personalizada completa de productos recomendados con el usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="c6c3f-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6c3f-142">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c6c3f-142">Additional resources</span></span>

[<span data-ttu-id="c6c3f-143">Visión general de recomendaciones de producto</span><span class="sxs-lookup"><span data-stu-id="c6c3f-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c6c3f-144">Habilitar recomendaciones de producto</span><span class="sxs-lookup"><span data-stu-id="c6c3f-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c6c3f-145">Habilitar recomendaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="c6c3f-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="c6c3f-146">Agregar listas de recomendaciones a páginas</span><span class="sxs-lookup"><span data-stu-id="c6c3f-146">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="c6c3f-147">Para agregar el panel de recomendaciones a dispositivos de PDV</span><span class="sxs-lookup"><span data-stu-id="c6c3f-147">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="c6c3f-148">Visión general del módulo de colección de productos</span><span class="sxs-lookup"><span data-stu-id="c6c3f-148">Product collection module overview</span></span>](product-collection-module-overview.md)