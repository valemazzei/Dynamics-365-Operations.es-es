---
title: Elegir entre Modern POS (MPOS) y PDV en la nube
description: Este tema explica las diferencias entre Modern POS y PDV en la nube. También se describen los distintos factores que los minoristas que están implementando Dynamics 365 Commerce deben considerar para ayudar a tomar las mejores decisiones para sus requisitos.
author: jblucher
manager: AnnBe
ms.date: 10/13/2017
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
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1fffc7141c041873f39f716aaf1a775984ef499c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023882"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="91578-104">Elegir entre Modern POS (MPOS) y PDV en la nube</span><span class="sxs-lookup"><span data-stu-id="91578-104">Choose between Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91578-105">Este tema proporciona a los implementadores antecedentes, sugerencias, y directrices adicionales para los factores que deben tener en cuenta al implementar Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91578-105">This topic gives implementers additional background, tips, and guidance for factors that they should consider when they deploy Dynamics 365 Commerce.</span></span> <span data-ttu-id="91578-106">Revisando y siguiendo esta orientación como parte del proceso de implementación, los implementadores podrán evitar problemas que podrían afectar a la satisfacción del usuario o al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="91578-106">By reviewing and following this guidance as part of the deployment process, implementers can avoid issues that might affect user satisfaction or performance.</span></span>

## <a name="insights"></a><span data-ttu-id="91578-107">Información</span><span class="sxs-lookup"><span data-stu-id="91578-107">Insights</span></span>

<span data-ttu-id="91578-108">Commerce proporciona una gran variedad de opciones de implementación y topología.</span><span class="sxs-lookup"><span data-stu-id="91578-108">Commerce provides a wide range of deployment and topology options.</span></span> <span data-ttu-id="91578-109">Por lo tanto, los minoristas pueden elegir los componentes y la configuración que mejor cumplan sus requisitos empresariales y de tecnología.</span><span class="sxs-lookup"><span data-stu-id="91578-109">Therefore, retailers can choose the components and configuration that best meet their business and technology requirements.</span></span> <span data-ttu-id="91578-110">Un aspecto de la implementación que requiere una consideración cuidadosa es la elección de una plataforma y un factor de forma para el componente de punto de venta (PDV).</span><span class="sxs-lookup"><span data-stu-id="91578-110">One aspect of implementation that requires careful consideration is the choice of a platform and form factor for the point of sale (POS) component.</span></span>

### <a name="pos-platform-and-form-factor-considerations"></a><span data-ttu-id="91578-111">Consideraciones de la plataforma y el factor de forma de PDV</span><span class="sxs-lookup"><span data-stu-id="91578-111">POS platform and form factor considerations</span></span>

<span data-ttu-id="91578-112">Commerce admite las siguientes opciones de PDV:</span><span class="sxs-lookup"><span data-stu-id="91578-112">Commerce supports the following POS options:</span></span>

- <span data-ttu-id="91578-113">Modern POS (MPOS) para Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="91578-113">Modern POS (MPOS) for Microsoft Windows</span></span>
- <span data-ttu-id="91578-114">MPOS para Microsoft Windows Phone</span><span class="sxs-lookup"><span data-stu-id="91578-114">MPOS for Microsoft Windows Phone</span></span>
- <span data-ttu-id="91578-115">MPOS para el Apple iPad o tableta de Google Android</span><span class="sxs-lookup"><span data-stu-id="91578-115">MPOS for Apple iPad or Google Android tablet</span></span>
- <span data-ttu-id="91578-116">Cloud POS (CPOS), que admite Microsoft Edge, Internet Explorer, y los exploradores de Google Chrome</span><span class="sxs-lookup"><span data-stu-id="91578-116">Cloud POS (CPOS), which supports the Microsoft Edge, Internet Explorer, and Google Chrome browsers</span></span>

<span data-ttu-id="91578-117">En todos los casos, el sistema POS (MPOS y CPOS) comparte el mismo código de aplicación básica.</span><span class="sxs-lookup"><span data-stu-id="91578-117">In all cases, the POS (MPOS and CPOS) shares the same core application code.</span></span> <span data-ttu-id="91578-118">Este punto es importante por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="91578-118">This point is important for the following reasons:</span></span>

- <span data-ttu-id="91578-119">La interfaz de usuario (IU) es coherente, independientemente de la plataforma o factor de forma.</span><span class="sxs-lookup"><span data-stu-id="91578-119">The user interface (UI) is consistent, regardless of the platform or form factor.</span></span>
- <span data-ttu-id="91578-120">La mayoría de las capacidades funcionales son iguales, independientemente de la plataforma o factor de forma.</span><span class="sxs-lookup"><span data-stu-id="91578-120">Most of the functional capabilities are the same, regardless of the platform or form factor.</span></span> <span data-ttu-id="91578-121">Sin embargo, existen algunas diferencias importantes.</span><span class="sxs-lookup"><span data-stu-id="91578-121">However, there are some important differences.</span></span> <span data-ttu-id="91578-122">Estas diferencias se indican en este tema.</span><span class="sxs-lookup"><span data-stu-id="91578-122">These differences are noted in this topic.</span></span>
- <span data-ttu-id="91578-123">En un almacén determinado, las variaciones de POS se pueden combinar y se pueden ejecutar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="91578-123">In a given store, the POS variations can be combined and can run concurrently.</span></span> <span data-ttu-id="91578-124">Por ejemplo, para sus registros principales, un minorista puede usar MPOS en equipos que ejecutan Windows.</span><span class="sxs-lookup"><span data-stu-id="91578-124">For example, for its main registers, a retailer can use MPOS on computers that run Windows.</span></span> <span data-ttu-id="91578-125">Sin embargo, el minorista puede complementar dichos registros con terminales basados en el explorador o dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="91578-125">However, the retailer can supplement those registers with browser-based terminals or mobile devices.</span></span>
- <span data-ttu-id="91578-126">Las personalizaciones y extensiones se pueden utilizar con facilidad a través de varias plataformas y factores de forma.</span><span class="sxs-lookup"><span data-stu-id="91578-126">Customizations and extensions can easily be used across platforms and form factors.</span></span> <span data-ttu-id="91578-127">Dado que el código de aplicación básica se comparte, la mayoría de las personalizaciones se pueden implementar una vez en lugar de varias veces.</span><span class="sxs-lookup"><span data-stu-id="91578-127">Because the core application code is shared, most customizations can be implemented one time instead of multiple times.</span></span>

### <a name="mpos-vs-cpos"></a><span data-ttu-id="91578-128">MPOS y CPOS</span><span class="sxs-lookup"><span data-stu-id="91578-128">MPOS vs. CPOS</span></span>

<span data-ttu-id="91578-129">Aunque los MPOS y los CPOS son prácticamente iguales, existen algunas diferencias importantes que debe comprender.</span><span class="sxs-lookup"><span data-stu-id="91578-129">Although MPOS and CPOS are largely the same, there are some important differences that you must understand.</span></span>

#### <a name="mpos"></a><span data-ttu-id="91578-130">MPOS</span><span class="sxs-lookup"><span data-stu-id="91578-130">MPOS</span></span>

<span data-ttu-id="91578-131">MPOS en un dispositivo Windows, iOS, o Android es una aplicación que se empaqueta, se instala y se mantiene en dicho dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91578-131">MPOS on a Windows, iOS, or Android device is an application that is packaged, installed, and serviced on that device.</span></span>

- <span data-ttu-id="91578-132">**Windows**: el MPOS para la aplicación de Windows contiene todo el código de aplicación y el tiempo de ejecución de Commerce Runtime (CRT).</span><span class="sxs-lookup"><span data-stu-id="91578-132">**Windows** – The MPOS for Windows application contains all the application code and the embedded commerce runtime (CRT).</span></span> 
- <span data-ttu-id="91578-133">**iOS/Android** En estas plataformas, la aplicación actúa como host para el código de aplicación de los CPOS.</span><span class="sxs-lookup"><span data-stu-id="91578-133">**iOS/Android** – On these platforms, the application acts as a host for the CPOS application code.</span></span> <span data-ttu-id="91578-134">Es decir, el código de aplicación procede del servidor de los CPOS en Microsoft Azure o Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="91578-134">In other words, the application code comes from the CPOS server on Microsoft Azure or the Commerce Scale Unit.</span></span> <span data-ttu-id="91578-135">Para obtener más información, consulte [Vista general de Retail Store Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin)</span><span class="sxs-lookup"><span data-stu-id="91578-135">For more information, see [Retail Store Scale Unit overview](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).</span></span>

#### <a name="cpos"></a><span data-ttu-id="91578-136">CPOS</span><span class="sxs-lookup"><span data-stu-id="91578-136">CPOS</span></span>

<span data-ttu-id="91578-137">Dado que los CPOS se ejecutan en un explorador, la aplicación no se instala en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91578-137">Because CPOS runs in a browser, the application isn't installed on the device.</span></span> <span data-ttu-id="91578-138">En su lugar, el explorador tiene acceso al código de aplicación desde el servidor de los CPOS.</span><span class="sxs-lookup"><span data-stu-id="91578-138">Instead, the browser accesses the application code from the CPOS server.</span></span> <span data-ttu-id="91578-139">Por lo tanto, los CPOS no pueden tener acceso directamente al hardware ni trabajar sin conexión.</span><span class="sxs-lookup"><span data-stu-id="91578-139">Therefore, CPOS can't directly access POS hardware or work in an offline state.</span></span>

### <a name="store-deployment-considerations"></a><span data-ttu-id="91578-140">Consideraciones sobre la implementación de la tienda</span><span class="sxs-lookup"><span data-stu-id="91578-140">Store deployment considerations</span></span>

<span data-ttu-id="91578-141">Además de una plataforma y un factor de forma, los minoristas deben elegir también una opción de implementación en la tienda.</span><span class="sxs-lookup"><span data-stu-id="91578-141">In addition to a platform and form factor, retailers must also choose a deployment option at the store.</span></span> <span data-ttu-id="91578-142">En la siguiente tabla, se muestran las configuraciones que están disponibles para opción de POS.</span><span class="sxs-lookup"><span data-stu-id="91578-142">The following table shows the configurations that are available for each POS option.</span></span>

| <span data-ttu-id="91578-143">Solicitud de POS</span><span class="sxs-lookup"><span data-stu-id="91578-143">POS application</span></span>         | <span data-ttu-id="91578-144">Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="91578-144">Commerce Scale Unit</span></span> | <span data-ttu-id="91578-145">Disponible sin conexión</span><span class="sxs-lookup"><span data-stu-id="91578-145">Available offline</span></span> |
|-------------------------|---------------|-------------------|
| <span data-ttu-id="91578-146">MPOS para Windows</span><span class="sxs-lookup"><span data-stu-id="91578-146">MPOS for Windows</span></span>        | <span data-ttu-id="91578-147">Nube o RSSU</span><span class="sxs-lookup"><span data-stu-id="91578-147">Cloud or RSSU</span></span> | <span data-ttu-id="91578-148">Sí</span><span class="sxs-lookup"><span data-stu-id="91578-148">Yes</span></span>               |
| <span data-ttu-id="91578-149">MPOS para iOS o Android</span><span class="sxs-lookup"><span data-stu-id="91578-149">MPOS for iOS or Android</span></span> | <span data-ttu-id="91578-150">Nube o RSSU</span><span class="sxs-lookup"><span data-stu-id="91578-150">Cloud or RSSU</span></span> | <span data-ttu-id="91578-151">No</span><span class="sxs-lookup"><span data-stu-id="91578-151">No</span></span>                |
| <span data-ttu-id="91578-152">PDV en la nube</span><span class="sxs-lookup"><span data-stu-id="91578-152">Cloud POS</span></span>               | <span data-ttu-id="91578-153">Nube o RSSU</span><span class="sxs-lookup"><span data-stu-id="91578-153">Cloud or RSSU</span></span> | <span data-ttu-id="91578-154">No</span><span class="sxs-lookup"><span data-stu-id="91578-154">No</span></span>                |

#### <a name="commerce-scale-unit"></a><span data-ttu-id="91578-155">Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="91578-155">Commerce Scale Unit</span></span>

<span data-ttu-id="91578-156">Commerce Scale Unit es un componente que hospeda el CRT.</span><span class="sxs-lookup"><span data-stu-id="91578-156">The Commerce Scale Unit is a component that hosts the CRT.</span></span> <span data-ttu-id="91578-157">CRT contiene toda la lógica de negocios que utiliza PDV, y proporciona acceso a la base de datos del canal.</span><span class="sxs-lookup"><span data-stu-id="91578-157">The CRT contains all the business logic that the POS uses, and it provides access to the channel database.</span></span> <span data-ttu-id="91578-158">Mientras están en línea, todos los clientes de PDV de la tienda utilizan Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="91578-158">While they are online, all POS clients in the store use the Commerce Scale Unit.</span></span> <span data-ttu-id="91578-159">Commerce Scale Unit se puede implementar en la nube o en la tienda.</span><span class="sxs-lookup"><span data-stu-id="91578-159">The Commerce Scale Unit can be deployed either in the cloud or in the store.</span></span>

#### <a name="offline-mode"></a><span data-ttu-id="91578-160">Modo sin conexión</span><span class="sxs-lookup"><span data-stu-id="91578-160">Offline mode</span></span>

<span data-ttu-id="91578-161">MPOS para Windows admite el modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="91578-161">MPOS for Windows supports offline mode.</span></span> <span data-ttu-id="91578-162">En el modo desconectado, POS puede seguir procesando ventas incluso si se ha desconectado de Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="91578-162">In offline mode, the POS can continue to process sales even if it's disconnected from the Commerce Scale Unit.</span></span> <span data-ttu-id="91578-163">Se puede sincronizar con la base de datos del canal al restablecer la conectividad.</span><span class="sxs-lookup"><span data-stu-id="91578-163">It can then be synchronized with the channel database when connectivity is restored.</span></span> <span data-ttu-id="91578-164">MPOS utiliza su propia instancia incrustada de CRT y utiliza temporalmente su propio origen de datos locales (base de datos de SQL Server sin conexión).</span><span class="sxs-lookup"><span data-stu-id="91578-164">MPOS uses its own embedded instance of the CRT and temporarily uses its own local data source (offline SQL Server database).</span></span> <span data-ttu-id="91578-165">Para obtener más información sobre la funcionalidad sin conexión, consulte [Funcionalidad sin conexión de PDV](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality).</span><span class="sxs-lookup"><span data-stu-id="91578-165">For more information about offline functionality, see [POS offline functionality](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality).</span></span>

### <a name="pos-peripheralhardware-considerations"></a><span data-ttu-id="91578-166">Consideraciones sobre los periféricos/hardware del PDV</span><span class="sxs-lookup"><span data-stu-id="91578-166">POS peripheral/hardware considerations</span></span>

<span data-ttu-id="91578-167">Los minoristas deben también considerar cómo los PDV tendrán acceso a los dispositivos y periféricos como impresoras, cajas registradoras, y terminales de pago.</span><span class="sxs-lookup"><span data-stu-id="91578-167">Retailers must also consider how the POS will access devices and peripherals such as printers, cash drawers, and payment terminals.</span></span> <span data-ttu-id="91578-168">Solo MPOS para Windows admite la comunicación directa con estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="91578-168">Only MPOS for Windows supports direct communication with these devices.</span></span> <span data-ttu-id="91578-169">MPOS para Windows Phone, iOS, o Android, y Cloud POS requieren una estación de hardware para obtener acceso a estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="91578-169">MPOS for Windows Phone, iOS, or Android, and Cloud POS require a hardware station in order to access these devices.</span></span> <span data-ttu-id="91578-170">Las estaciones de hardware se pueden dedicar a un registro de POS o compartir entre los registros de una tienda.</span><span class="sxs-lookup"><span data-stu-id="91578-170">Hardware stations can be dedicated to a POS register or shared among the registers in a store.</span></span> <span data-ttu-id="91578-171">Para obtener más información sobre estaciones de hardware, consulte [Instalar y configurar una estación de hardware de Retail](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="91578-171">For more information about hardware stations, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="91578-172">Consideraciones sobre la implementación</span><span class="sxs-lookup"><span data-stu-id="91578-172">Implementation considerations</span></span>

<span data-ttu-id="91578-173">Tenga en cuenta la siguiente información cuando planee su implementación de PDV en sus tiendas:</span><span class="sxs-lookup"><span data-stu-id="91578-173">Consider the following information as you plan your POS implementation in your stores:</span></span>

- <span data-ttu-id="91578-174">**Requisitos funcionales** – Los procesos y las capacidades de negocio principales son iguales, independientemente de la plataforma, factor de forma, o topología de implementación.</span><span class="sxs-lookup"><span data-stu-id="91578-174">**Functional requirements** – The core business processes and capabilities are the same, regardless of the platform, form factor, or deployment topology.</span></span> <span data-ttu-id="91578-175">Por lo tanto, la mayoría de los minoristas no tienen que tener en cuenta los requisitos funcionales cuando planifican su implementación.</span><span class="sxs-lookup"><span data-stu-id="91578-175">Therefore, most retailers don't have to consider functional requirements when they plan their implementation.</span></span>
- <span data-ttu-id="91578-176">**Conectividad** - La disponibilidad de la red (red de área extendida \[WAN\] y red de área local \[LAN\]) es un factor principal que requiere una consideración cuidadosa.</span><span class="sxs-lookup"><span data-stu-id="91578-176">**Connectivity** – Network availability (wide area network \[WAN\] and local area network \[LAN\]) is a major factor that requires careful consideration.</span></span> <span data-ttu-id="91578-177">Todos los beneficios que aporta una solución alojada en la nube de espacio cero en términos de coste y sencillez se pierden si el sistema no está disponible para los procesos de negocio indispensables.</span><span class="sxs-lookup"><span data-stu-id="91578-177">Any benefits that a zero-footprint, cloud-hosted solution brings in terms of cost and simplicity are lost if the system isn't available for business-critical processes.</span></span>

    <span data-ttu-id="91578-178">A menos que la conectividad para un dispositivo dado sea muy de confianza y resistente, o a menos que una determinada cantidad de tiempo de inactividad sea aceptable para el minorista, se recomienda una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="91578-178">Unless the connectivity for a given device is very dependable and resilient, or unless a certain amount of downtime is acceptable to the retailer, we recommend one of the following options:</span></span>

    - <span data-ttu-id="91578-179">Usar MPOS en Windows y habilitar el modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="91578-179">Use MPOS in Windows, and enable offline mode.</span></span>
    - <span data-ttu-id="91578-180">Implemente una Commerce Scale Unit local.</span><span class="sxs-lookup"><span data-stu-id="91578-180">Deploy an on-premises Commerce Scale Unit.</span></span>

    <span data-ttu-id="91578-181">Estas dos opciones no se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="91578-181">These two options aren't mutually exclusive.</span></span> <span data-ttu-id="91578-182">En la topología más fiable, los minoristas pueden implementar una RSSU local para reducir la dependencia de conectividad de Internet o la disponibilidad de Azure y también pueden implementar registros de PDV donde el modo sin conexión está habilitado si hay un problema con el servidor local o la red.</span><span class="sxs-lookup"><span data-stu-id="91578-182">For the most reliable topology, retailers can deploy a local RSSU to reduce the dependency on internet connectivity or Azure availability, and they can also deploy POS registers where offline mode is enabled if there is an issue with the local server or network.</span></span>

- <span data-ttu-id="91578-183">**Dispositivos de hardware/periféricos** – Un aspecto importante de un sistema Retail POS es su capacidad para usar periféricos de PDV como impresoras, cajas registradoras, y terminales de pago.</span><span class="sxs-lookup"><span data-stu-id="91578-183">**Hardware devices/peripherals** – One important aspect of a Retail POS system is its ability to use POS peripherals such as printers, cash drawers, and payment terminals.</span></span> <span data-ttu-id="91578-184">Aunque todas las opciones disponibles de POS puedan usar dispositivos periféricos, solo los MPOS para Windows los admiten directamente.</span><span class="sxs-lookup"><span data-stu-id="91578-184">Although all the available POS options can use peripheral devices, only MPOS for Windows supports them directly.</span></span> <span data-ttu-id="91578-185">Para el resto de solicitudes, se requieren una o más estaciones de hardware.</span><span class="sxs-lookup"><span data-stu-id="91578-185">For all other applications, one or more hardware stations are required.</span></span> <span data-ttu-id="91578-186">Aunque este planteamiento añade flexibilidad, deben implementarse, configurarse y mantener componentes adicionales.</span><span class="sxs-lookup"><span data-stu-id="91578-186">Although this approach adds flexibility, additional components must be deployed, configured, and serviced.</span></span>
- <span data-ttu-id="91578-187">**Requisitos del sistema** – Los requisitos del sistema para la aplicación de PDV varían.</span><span class="sxs-lookup"><span data-stu-id="91578-187">**System requirements** – The system requirements for the POS application vary.</span></span> <span data-ttu-id="91578-188">Asegúrese de verificar la información más reciente antes de tomar una decisión.</span><span class="sxs-lookup"><span data-stu-id="91578-188">Be sure to check the latest information before you make your choice.</span></span> <span data-ttu-id="91578-189">Por ejemplo, ya que los CPOS se ejecutan en un explorador, admiten una gama más amplia de sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="91578-189">For example, because CPOS runs in a browser, it supports a wider range of operating systems.</span></span> <span data-ttu-id="91578-190">Para obtener más información acerca de los requisitos del sistema, consulte los [Requisitos del sistema para implementaciones en la nube](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).</span><span class="sxs-lookup"><span data-stu-id="91578-190">For more information about system requirements, see [System requirements for cloud deployments](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).</span></span>
- <span data-ttu-id="91578-191">**Implementación y mantenimiento** La complejidad de los requisitos de implementación y mantenimiento puede variar, en función de las opciones de la aplicación y la implementación.</span><span class="sxs-lookup"><span data-stu-id="91578-191">**Deployment and servicing** – The complexity of the deployment and servicing requirements can vary, depending on the application and deployment choices.</span></span> <span data-ttu-id="91578-192">Por ejemplo, para una implementación de CPOS hospedada en la nube, no es necesario instalar y actualizar en cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91578-192">For example, for a cloud-hosted CPOS deployment, you don't have to install and update on every device.</span></span> <span data-ttu-id="91578-193">Por lo tanto, este planteamiento reduce significativamente la complejidad y el coste.</span><span class="sxs-lookup"><span data-stu-id="91578-193">Therefore, this approach greatly reduces complexity and cost.</span></span> <span data-ttu-id="91578-194">Sin embargo, si se implementan MPOS en cada registro y habilita el modo desconectado, y también implementa las estaciones compartidas de hardware, aumenta significativamente el número de extremos que deben administrarse.</span><span class="sxs-lookup"><span data-stu-id="91578-194">However, if you deploy MPOS on every register and enable offline mode, and you also deploy shared hardware stations, you greatly increase the number of endpoints that must be managed.</span></span>