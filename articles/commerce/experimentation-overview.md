---
title: Experimentación en Dynamics 365 Commerce
description: La experimentación permite la creación, edición y gestión del diseño de página y tratamientos de contenido en el creador de sitios. El soporte de experimentación de un extremo a otro está habilitado para las páginas y entidades de comercio electrónico dentro de una página.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8b2e97167d12b8ceecf72af075ee0362101c4fa0
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930287"
---
# <a name="experimentation-in-dynamics-365-commerce"></a><span data-ttu-id="88eed-104">Experimentación en Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="88eed-104">Experimentation in Dynamics 365 Commerce</span></span>
<span data-ttu-id="88eed-105">Utilice la experimentación en Dynamics 365 Commerce para validar hipótesis sobre la eficacia de sus páginas de comercio electrónico y tomar decisiones con confianza basada en datos.</span><span class="sxs-lookup"><span data-stu-id="88eed-105">Use experimentation in Dynamics 365 Commerce to validate hypotheses about the effectiveness of your e-Commerce pages and make decisions with data-driven confidence.</span></span> <span data-ttu-id="88eed-106">Commerce admite pruebas A / B en páginas, módulos y fragmentos y le permite medir el impacto de los cambios propuestos en su sitio web.</span><span class="sxs-lookup"><span data-stu-id="88eed-106">Commerce supports A/B testing on pages, modules, and fragments and enables you to measure the impact of proposed changes to your website.</span></span>

<span data-ttu-id="88eed-107">Puede crear, editar y administrar tratamientos de contenido y página conocidos como **variaciones** en el creador de sitios.</span><span class="sxs-lookup"><span data-stu-id="88eed-107">You can create, edit, and manage page and content treatments known as **variations** in site builder.</span></span> <span data-ttu-id="88eed-108">Commerce se integra con servicios de terceros que puede utilizar para crear experimentos y asignaciones de tratamiento.</span><span class="sxs-lookup"><span data-stu-id="88eed-108">Commerce integrates with third-party services that you can use to create experiments and treatment assignments.</span></span> <span data-ttu-id="88eed-109">Los flujos de eventos en tiempo real capturados en Commerce habilitan los análisis que definen los resultados del experimento en el servicio de terceros.</span><span class="sxs-lookup"><span data-stu-id="88eed-109">Real-time event streams captured in Commerce enable the analytics that define the experiment results in the third-party service.</span></span> <span data-ttu-id="88eed-110">Luego, puede aprovechar estos análisis para ayudar a respaldar o refutar su hipótesis.</span><span class="sxs-lookup"><span data-stu-id="88eed-110">You can then leverage these analytics to help support or refute your hypothesis.</span></span>

## <a name="set-up-prerequisites"></a><span data-ttu-id="88eed-111"> Requisitos previos de configuración</span><span class="sxs-lookup"><span data-stu-id="88eed-111">Set up prerequisites</span></span>
1. <span data-ttu-id="88eed-112">**Obtener la versión correcta de Commerce** - Actualice su biblioteca de módulos, el SDK de extensibilidad de canales en línea y Commerce Scale Unit a la versión 10.0.13 o posterior de Commerce.</span><span class="sxs-lookup"><span data-stu-id="88eed-112">**Get the correct version of Commerce** - Upgrade your module library, online channel extensibility SDK, and Commerce scale unit to Commerce version 10.0.13 or later.</span></span>
1. <span data-ttu-id="88eed-113">**Configurar un conector de experimentación** - Un conector de experimentación permite a Comercio conectarse con servicios de terceros para recuperar la lista de experimentos y determinar cuándo mostrar un experimento a un usuario.</span><span class="sxs-lookup"><span data-stu-id="88eed-113">**Set up an experimentation connector** - An experimentation connector allows Commerce to connect with third-party services to retrieve the list of experiments and determine when to show an experiment to a user.</span></span> <span data-ttu-id="88eed-114">Puede adquirir un conector de terceros en [AppSource](https://appsource.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="88eed-114">You can purchase a third-party connector from [AppSource](https://appsource.microsoft.com).</span></span> <span data-ttu-id="88eed-115">Siga las instrucciones de configuración proporcionadas por el editor.</span><span class="sxs-lookup"><span data-stu-id="88eed-115">Follow the setup instructions provided by the publisher.</span></span> <span data-ttu-id="88eed-116">Alternativamente, puede utilizar el conector de prueba de muestra de Commerce para probar el flujo de trabajo de experimentación sin necesidad de configurar un servicio externo.</span><span class="sxs-lookup"><span data-stu-id="88eed-116">You can alternatively use the sample test connector from Commerce to test the experimentation workflow without needing to configure an external service.</span></span> <span data-ttu-id="88eed-117">Para más información, vea [Configurar y habilitar conectores](e-commerce-extensibility/connectors.md).</span><span class="sxs-lookup"><span data-stu-id="88eed-117">For more information, see [Configure and enable connectors](e-commerce-extensibility/connectors.md).</span></span> 
1. <span data-ttu-id="88eed-118">**Activar las banderas de funciones de experimentación en Commerce** - Puede habilitar la experimentación a nivel de inquilino yendo a **Configuración de inquilinos > Funciones** o en el nivel de sitio en **Configuración del sitio > Funciones**.</span><span class="sxs-lookup"><span data-stu-id="88eed-118">**Turn on the experimentation feature flags in Commerce** - You can enable experimentation at the tenant level by going to **Tenant Settings > Features** or at the site level at **Site Settings > Features**.</span></span>
    - <span data-ttu-id="88eed-119">Habilite la marca **Experimentación** para crear variaciones experimentales de módulos dentro de una página sin afectar o copiar otro contenido que no es parte del experimento.</span><span class="sxs-lookup"><span data-stu-id="88eed-119">Enable the **Experimentation** flag to create experiment variations of modules within a page without affecting or copying other content that isn't part of the experiment.</span></span> <span data-ttu-id="88eed-120">Esto asegura que las actualizaciones de contenido en curso fuera del experimento permanezcan sincronizadas durante el ciclo de vida del experimento.</span><span class="sxs-lookup"><span data-stu-id="88eed-120">This ensures that ongoing content updates outside the experiment stay in sync during the experiment lifecycle.</span></span> <span data-ttu-id="88eed-121">La desactivación de esta marca impide que todos los experimentos se muestren a los usuarios y elimina todas las funciones de edición dentro del creador de sitios.</span><span class="sxs-lookup"><span data-stu-id="88eed-121">Disabling this flag stops all experiments from being shown to users and removes all editing functions within site builder.</span></span>
    - <span data-ttu-id="88eed-122">Habilite la marca **Experimente con páginas o fragmentos** para ejecutar experimentos en una página o fragmento.</span><span class="sxs-lookup"><span data-stu-id="88eed-122">Enable the **Experiment on pages or fragments** flag to run experiments on a page or fragment.</span></span> <span data-ttu-id="88eed-123">Esto crea una copia de instancia completa de toda la página o fragmento para todos los módulos dentro de la página o fragmento.</span><span class="sxs-lookup"><span data-stu-id="88eed-123">This creates a full instance copy of the entire page or fragment for all modules within the page or fragment.</span></span> <span data-ttu-id="88eed-124">Utilice este modo cuando desee probar cambios de contenido completos o cuando la sincronización de cambios de contenido en curso entre instancias no sea un problema.</span><span class="sxs-lookup"><span data-stu-id="88eed-124">Use this mode when you want to test comprehensive content changes, or where synchronizing ongoing content changes across instances isn't a concern.</span></span> <span data-ttu-id="88eed-125">La desactivación de esta marca evita la creación y edición de nuevos experimentos en páginas y fragmentos.</span><span class="sxs-lookup"><span data-stu-id="88eed-125">Disabling this flag prevents creation and editing of new experiments on pages and fragments.</span></span>
    > [!NOTE]
    > <span data-ttu-id="88eed-126">La marca **Experimentación** también debe estar habilitada para que la funcionalidad **Experimente con páginas o fragmentos** funcione.</span><span class="sxs-lookup"><span data-stu-id="88eed-126">The **Experimentation** flag must also be enabled for the **Experiment on pages or fragments** functionality to work.</span></span>
    
## <a name="experimentation-lifecycle"></a><span data-ttu-id="88eed-127">Ciclo de vida de experimentación</span><span class="sxs-lookup"><span data-stu-id="88eed-127">Experimentation lifecycle</span></span>
<span data-ttu-id="88eed-128">Configurar un experimento, crear variaciones y ejecutar un experimento es un proceso iterativo.</span><span class="sxs-lookup"><span data-stu-id="88eed-128">Setting up an experiment, creating variations, and running an experiment is an iterative process.</span></span> <span data-ttu-id="88eed-129">El siguiente diagrama ilustra el ciclo de vida de la experimentación en Commerce y el servicio de terceros.</span><span class="sxs-lookup"><span data-stu-id="88eed-129">The diagram below illustrates the experimentation lifecycle in Commerce and the third-party service.</span></span> 

<span data-ttu-id="88eed-130">[ ![Ciclo de vida de experimentación](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="88eed-130">[ ![Experimentation lifecycle](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)</span></span>

<span data-ttu-id="88eed-131">Para obtener más información sobre cada paso del proceso de experimentación, consulte los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="88eed-131">To learn more about each step in the experimentation process, refer to the following topics.</span></span>
- [<span data-ttu-id="88eed-132">Identificar una hipótesis y determinar métricas para un experimento</span><span class="sxs-lookup"><span data-stu-id="88eed-132">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md)
- [<span data-ttu-id="88eed-133">Configurar un experimento</span><span class="sxs-lookup"><span data-stu-id="88eed-133">Set up an experiment</span></span>](experimentation-setup.md)
- [<span data-ttu-id="88eed-134">Conectar y editar un experimento</span><span class="sxs-lookup"><span data-stu-id="88eed-134">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
- [<span data-ttu-id="88eed-135">Obtener una vista previa y publicar un experimento</span><span class="sxs-lookup"><span data-stu-id="88eed-135">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
- [<span data-ttu-id="88eed-136">Ejecutar y supervisar un experimento</span><span class="sxs-lookup"><span data-stu-id="88eed-136">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
- [<span data-ttu-id="88eed-137">Promover una variación y completar un experimento</span><span class="sxs-lookup"><span data-stu-id="88eed-137">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)

> [!NOTE]
> <span data-ttu-id="88eed-138">Para saber dónde se encuentra un experimento en el ciclo de vida, vaya a la pestaña **Experimentos** en el creador de sitios.</span><span class="sxs-lookup"><span data-stu-id="88eed-138">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="88eed-139">Se muestra una lista de experimentos con el estado de cada experimento tanto en Commerce como en el servicio de terceros.</span><span class="sxs-lookup"><span data-stu-id="88eed-139">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service.</span></span> <span data-ttu-id="88eed-140">Para más información, vea [Revisar el estado de un experimento](experimentation-status.md).</span><span class="sxs-lookup"><span data-stu-id="88eed-140">For more information, see [Review the status of an experiment](experimentation-status.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="88eed-141">Paso siguiente</span><span class="sxs-lookup"><span data-stu-id="88eed-141">Next step</span></span>
[<span data-ttu-id="88eed-142">Identificar una hipótesis y determinar métricas de éxito para un experimento</span><span class="sxs-lookup"><span data-stu-id="88eed-142">Identify a hypothesis and determine success metrics for an experiment</span></span>](experimentation-identify.md) 