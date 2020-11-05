---
title: Revisar el estado de un experimento
description: Este tema explica qué estado tiene un experimento en el ciclo de vida de la experimentación en Dynamics 365 Commerce.
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
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930281"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="ab589-103">Revisar el estado de un experimento</span><span class="sxs-lookup"><span data-stu-id="ab589-103">Review the status of an experiment</span></span>
<span data-ttu-id="ab589-104">Hay muchos pasos involucrados en la configuración y ejecución de un experimento en Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab589-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ab589-105">Para obtener información sobre el ciclo de vida de la experimentación, consulte [Experimentación en Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ab589-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="ab589-106">Para saber dónde se encuentra un experimento en el ciclo de vida, vaya a la pestaña **Experimentos** en el creador de sitios.</span><span class="sxs-lookup"><span data-stu-id="ab589-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="ab589-107">Se muestra una lista de experimentos con el estado de cada experimento tanto en Commerce como en el servicio de terceros que se está utilizando para permitir la creación de experimentos, asignar variaciones y analizar datos.</span><span class="sxs-lookup"><span data-stu-id="ab589-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="ab589-108">En la columna **Estado comercial**, se pueden mostrar los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="ab589-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="ab589-109">**Borrador** - El experimento está conectado a una página o fragmento en Commerce y se está editando.</span><span class="sxs-lookup"><span data-stu-id="ab589-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="ab589-110">**Publicado** - Las variaciones del experimento están listas para mostrarse en su sitio web.</span><span class="sxs-lookup"><span data-stu-id="ab589-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="ab589-111">Si el experimento se está ejecutando en el servicio de terceros, los usuarios del sitio web verán una variación de la página o el fragmento seleccionado por el servicio de terceros.</span><span class="sxs-lookup"><span data-stu-id="ab589-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="ab589-112">**Inédito** - El experimento ya no está disponible en su sitio web.</span><span class="sxs-lookup"><span data-stu-id="ab589-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="ab589-113">Los usuarios del sitio web solo verán la versión predeterminada de la página o el fragmento incluso si el experimento se está ejecutando en el servicio de terceros.</span><span class="sxs-lookup"><span data-stu-id="ab589-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="ab589-114">**Terminado** - El experimento ha seguido su curso y se promovió una variación para que esté disponible para todos los usuarios del sitio web.</span><span class="sxs-lookup"><span data-stu-id="ab589-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="ab589-115">Del mismo modo, en la columna **estado de terceros**, los siguientes valores pueden mostrarse para indicar en qué estado se encuentran los experimentos en el servicio de terceros.</span><span class="sxs-lookup"><span data-stu-id="ab589-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="ab589-116">**Borrador** - El experimento está configurado en el servicio de terceros, pero no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="ab589-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="ab589-117">**En ejecución** - El experimento se inició en el servicio de terceros y está recopilando datos.</span><span class="sxs-lookup"><span data-stu-id="ab589-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="ab589-118">**Pausado** - El experimento está en pausa y no se recopilan datos.</span><span class="sxs-lookup"><span data-stu-id="ab589-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="ab589-119">Debe reanudar el experimento para que vuelva a recopilar datos.</span><span class="sxs-lookup"><span data-stu-id="ab589-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="ab589-120">**Archivado** - El experimento ha seguido su curso y se ha catalogado en el servicio de terceros para futuras referencias.</span><span class="sxs-lookup"><span data-stu-id="ab589-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="ab589-121">El siguiente diagrama muestra ambos conjuntos de estados y cómo se relacionan entre sí.</span><span class="sxs-lookup"><span data-stu-id="ab589-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="ab589-122">[ ![Estados de experimentación](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ab589-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>