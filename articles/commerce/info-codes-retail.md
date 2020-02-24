---
title: Códigos de información y grupos de códigos de información
description: Este artículo proporciona información general acerca de códigos de información, grupos de códigos de información y acerca de cómo usarlos.
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 046204d36e2fc7a69129aaf7fe027b2abc7e8dd9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024005"
---
# <a name="info-codes-and-info-code-groups"></a><span data-ttu-id="8fd78-103">Códigos de información y grupos de códigos de información</span><span class="sxs-lookup"><span data-stu-id="8fd78-103">Info codes and info code groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8fd78-104">Este artículo proporciona información general acerca de códigos de información, grupos de códigos de información y acerca de cómo usarlos.</span><span class="sxs-lookup"><span data-stu-id="8fd78-104">This article provides an overview about info codes, info code groups, and how to use them.</span></span>

<span data-ttu-id="8fd78-105">Los códigos de la información proporcionan una forma de capturar datos en un registro del punto de venta (PDV).</span><span class="sxs-lookup"><span data-stu-id="8fd78-105">Info codes provide a way for you to capture data at a point-of-sale (POS) register.</span></span> <span data-ttu-id="8fd78-106">Puede utilizar los códigos de información para solicitar al cajero que especifique información durante varias acciones en el PDV, como las ventas del artículo, las devoluciones de artículos o la selección de clientes.</span><span class="sxs-lookup"><span data-stu-id="8fd78-106">You can use info codes to prompt the cashier to enter information during various actions at the POS, such as item sales, item returns, or selecting customers.</span></span> <span data-ttu-id="8fd78-107">Los cajeros pueden seleccionar la entrada de una lista o escribirla como un código, un número, una fecha o texto.</span><span class="sxs-lookup"><span data-stu-id="8fd78-107">Cashiers can select input from a list or enter it as a code, number, date, or text.</span></span> <span data-ttu-id="8fd78-108">Puede asignar códigos de información a acciones de tienda predefinidas, artículos comerciales, métodos de pago, clientes o actividades de punto de venta específicas.</span><span class="sxs-lookup"><span data-stu-id="8fd78-108">You can assign info codes to predefined store actions, retail items, payment methods, customers, or specific point-of-sale activities.</span></span> <span data-ttu-id="8fd78-109">Puede usar códigos de información para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8fd78-109">You can use info codes to do the following:</span></span>

- <span data-ttu-id="8fd78-110">Obtener información adicional en el momento de la transacción, tal como un número de vuelo o el motivo de una devolución.</span><span class="sxs-lookup"><span data-stu-id="8fd78-110">Capture additional information at transaction time, such as a flight number or the reason for a return.</span></span>
- <span data-ttu-id="8fd78-111">Solicitar al cajero de la caja registradora que seleccione productos específicos de una lista de precios.</span><span class="sxs-lookup"><span data-stu-id="8fd78-111">Prompt the register cashier to select from a list of prices for specific products.</span></span>
- <span data-ttu-id="8fd78-112">Vincular un subcódigo a un código de información que solicite al cajero de la caja registradora una respuesta cuando lleve a cabo una actividad específica.</span><span class="sxs-lookup"><span data-stu-id="8fd78-112">Link a subcode to an info code to prompt the cashier for input when performing a specific activity.</span></span> <span data-ttu-id="8fd78-113">Por ejemplo, cuando un cliente devuelve un producto, puede solicitar al cajero consultar por qué se devuelve el producto.</span><span class="sxs-lookup"><span data-stu-id="8fd78-113">For example, when a customer returns a product, you can prompt the cashier to ask why the product is being returned.</span></span> <span data-ttu-id="8fd78-114">A continuación puede usar subcódigos para mostrar una lista de motivos entre los que el cajero pueda elegir.</span><span class="sxs-lookup"><span data-stu-id="8fd78-114">Then you can use subcodes to display a list of reasons that the cashier can choose from.</span></span>
- <span data-ttu-id="8fd78-115">Vender un producto como una venta regular, venta con descuento o producto gratuito.</span><span class="sxs-lookup"><span data-stu-id="8fd78-115">Sell a product as a regular sale, discounted sale, or free product.</span></span>
- <span data-ttu-id="8fd78-116">Solicitar al cajero que especifique un valor o seleccione uno de una lista de subcódigos al abrir la caja registradora sin realizar una operación de ventas.</span><span class="sxs-lookup"><span data-stu-id="8fd78-116">Prompt the cashier to enter a value or select from a list of subcodes when the register drawer is opened without performing a sales operation.</span></span>

## <a name="info-codes-group"></a><span data-ttu-id="8fd78-117">Grupo de códigos de información</span><span class="sxs-lookup"><span data-stu-id="8fd78-117">Info codes group</span></span>

<span data-ttu-id="8fd78-118">En Commerce, puede crear grupos de códigos de información.</span><span class="sxs-lookup"><span data-stu-id="8fd78-118">In Commerce, you can create groups of info codes.</span></span> <span data-ttu-id="8fd78-119">Los grupos de códigos de información agregan flexibilidad al permitirle definir menos códigos de información y después usarlos de maneras más versátiles.</span><span class="sxs-lookup"><span data-stu-id="8fd78-119">Info code groups add flexibility by enabling you to define fewer info codes and then use them in more versatile ways.</span></span> <span data-ttu-id="8fd78-120">Puede usar los grupos de códigos de información de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="8fd78-120">You can use info code groups in the following ways:</span></span>

- <span data-ttu-id="8fd78-121">Defina menos códigos de información y reutilícelos fácilmente.</span><span class="sxs-lookup"><span data-stu-id="8fd78-121">Define fewer info codes and easily re-use them.</span></span> <span data-ttu-id="8fd78-122">Los códigos de información que se incluyen en grupos de códigos de información no tienen ninguna dependencia predefinida en otros códigos de información.</span><span class="sxs-lookup"><span data-stu-id="8fd78-122">Info codes that are included in info code groups have no predefined dependencies on other info codes.</span></span> <span data-ttu-id="8fd78-123">Puede incluir el mismo código de información de varios grupos de códigos de información y después usar la priorización para presentar los mismos códigos de información en el orden que tiene sentido en cualquier escenario concreto.</span><span class="sxs-lookup"><span data-stu-id="8fd78-123">You can include the same info code in multiple info code groups and then use prioritization to present the same info codes in the order that makes sense in any particular situation.</span></span>
- <span data-ttu-id="8fd78-124">Vincule códigos de información a otros códigos de información o grupos de códigos de información para recopilar información sobre un producto o una transacción sin tener que definir un código distinto de información o un código de información vinculado para cada situación.</span><span class="sxs-lookup"><span data-stu-id="8fd78-124">Link info codes to other info codes or info code groups to gather information about a product or transaction without having to define a separate info code or linked info code for each scenario.</span></span>

## <a name="info-code-examples"></a><span data-ttu-id="8fd78-125">Ejemplos de códigos de información</span><span class="sxs-lookup"><span data-stu-id="8fd78-125">Info code examples</span></span>

<span data-ttu-id="8fd78-126">**Ejemplo 1: reutilización de códigos de información**</span><span class="sxs-lookup"><span data-stu-id="8fd78-126">**Example 1: Reuse info codes**</span></span>

<span data-ttu-id="8fd78-127">Puede vincular códigos de información para que cuando se active un código de la información, se desencadene otro código de la información inmediatamente después de él.</span><span class="sxs-lookup"><span data-stu-id="8fd78-127">You can link info codes so that when one info code is triggered, another info code is triggered immediately after it.</span></span> <span data-ttu-id="8fd78-128">Por ejemplo, cuando vende determinados productos, puede solicitar al cajero que pregunte al cliente si desean comprar pilas y una garantía del producto.</span><span class="sxs-lookup"><span data-stu-id="8fd78-128">For example, when you sell certain products, you can prompt the cashier to ask the customer if they want to purchase batteries and a product warranty.</span></span> <span data-ttu-id="8fd78-129">Para otros productos, puede solicitar al cajero que pregunte al cliente si desean comprar pilas y si puede proporcionarles también su código postal.</span><span class="sxs-lookup"><span data-stu-id="8fd78-129">For other products, you can prompt the cashier to ask the customer if they want to purchase batteries and collect their postal code.</span></span> <span data-ttu-id="8fd78-130">Si crea códigos de información vinculados para estos casos, debe configurar cada variación del código de información para solicitar al cajero que pida la información correcta.</span><span class="sxs-lookup"><span data-stu-id="8fd78-130">If you create linked info codes for these scenarios, you must set up every variation of the info code so that the cashier is prompted to ask for the right information.</span></span> <span data-ttu-id="8fd78-131">Si usa grupos de códigos de información, los códigos de información comunes, como solicitar baterías, se pueden configurar una vez y después reutilizarlos en varios grupos de código de información.</span><span class="sxs-lookup"><span data-stu-id="8fd78-131">If you use info code groups, common info codes, such as asking for batteries, can be set up once and then reused in multiple info code groups.</span></span> <span data-ttu-id="8fd78-132">También puede usar la priorización en los grupos de códigos de información para identificar el orden en que se muestran los avisos.</span><span class="sxs-lookup"><span data-stu-id="8fd78-132">You can also use prioritization in the info code groups to identify the order in which the prompts are displayed.</span></span>

<span data-ttu-id="8fd78-133">**Ejemplo 2: Vincular códigos de información a grupos de códigos de información**</span><span class="sxs-lookup"><span data-stu-id="8fd78-133">**Example 2: Link info codes to info code groups**</span></span>

<span data-ttu-id="8fd78-134">Cuando vende determinados productos, por ejemplo, dispositivos móviles, desea siempre recopilar un conjunto específico de información, como el número de teléfono, el identificador móvil (IMEI) y el número de serie.</span><span class="sxs-lookup"><span data-stu-id="8fd78-134">When you sell certain products, for example mobile devices, you always want to collect a specific set of information, such as telephone number, mobile equipment identifier (MEID), and serial number.</span></span> <span data-ttu-id="8fd78-135">Sin embargo, también desea recopilar información distinta para una tableta en comparación con un teléfono móvil.</span><span class="sxs-lookup"><span data-stu-id="8fd78-135">However, you also want to collect different information for a tablet versus a mobile phone.</span></span> <span data-ttu-id="8fd78-136">Puede configurar un grupo del códigos de información que incluya los avisos para el número de teléfono, el IMEI y el número de serie, y después vincular el grupo de códigos de información a un código individual de información.</span><span class="sxs-lookup"><span data-stu-id="8fd78-136">You can set up an info code group that includes prompts for the telephone number, MEID, and the serial number, and then link the info code group to an individual info code.</span></span> <span data-ttu-id="8fd78-137">Cuando se activa el código de información específico del producto, el grupo de códigos de información puede activarse a continuación para permitirle recopilar los datos comunes sin tener que definir varios conjuntos de códigos de información vinculados para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8fd78-137">When the product-specific info code is triggered, the info code group can be triggered next to enable you to collect the common data without having to define multiple sets of linked info codes for each device.</span></span>