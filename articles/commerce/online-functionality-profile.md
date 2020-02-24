---
title: Crear un perfil de funcionalidad en línea
description: Este tema describe cómo crear un perfil de funcionalidad en línea en Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003381"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="6e2bc-103">Crear un perfil de funcionalidad en línea</span><span class="sxs-lookup"><span data-stu-id="6e2bc-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6e2bc-104">Este tema presenta una visión general de la configuración de un perfil de funcionalidad en línea para Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6e2bc-105">Visión general</span><span class="sxs-lookup"><span data-stu-id="6e2bc-105">Overview</span></span>

<span data-ttu-id="6e2bc-106">El perfil de funcionalidad en línea proporciona varias configuraciones utilizadas para los canales en línea.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="6e2bc-107">Cada canal en línea debe especificar un perfil de funcionalidad en línea.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="6e2bc-108">Crear un perfil de funcionalidad en línea</span><span class="sxs-lookup"><span data-stu-id="6e2bc-108">Create an online functionality profile</span></span>

<span data-ttu-id="6e2bc-109">El siguiente procedimiento explica cómo crear un perfil de funcionalidad en línea desde la aplicación Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="6e2bc-110">En el panel de navegación, vaya a **Módulos \> Configuración de canal \> Configuración de la tienda en línea \> Perfiles de funcionalidad**.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="6e2bc-111">En el panel de acciones, seleccione **Nueva**.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6e2bc-112">En el campo **Perfil**, introduzca un id. para el perfil.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="6e2bc-113">En el campo **Descripción**, introduzca un valor ("Perfil de Adventure Works" en la imagen de ejemplo que se muestra a continuación).</span><span class="sxs-lookup"><span data-stu-id="6e2bc-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="6e2bc-114">En la sección **Funciones**, modifique la configuración de **CARRO**, **CLIENTES COMERCIALES** o **FINALIZAR COMPRA**, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="6e2bc-115">En el panel de acciones, seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6e2bc-116">La siguiente imagen muestra un perfil de funcionalidad en línea de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-116">The following image shows an example online functionality profile.</span></span>
  
![Ejemplo de perfil de funcionalidad en línea](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="6e2bc-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="6e2bc-118">Functions</span></span>

- <span data-ttu-id="6e2bc-119">**Productos agregados**: cuando está habilitada, esta función permite que el carro actualice la cantidad cuando se agrega el mismo artículo varias veces.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="6e2bc-120">**Permitir finalizar compra sin pagos**: cuando está habilitada, esta función maneja el escenario cuando los artículos agregados al carro tienen un precio 0,00 $.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="6e2bc-121">**Crear cliente en modo asincrónico**: esta es una configuración heredada aplicable a canales de comercio electrónico de terceros y no es aplicable al sitio de comercio electrónico de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e2bc-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6e2bc-122">Additional resources</span></span>

[<span data-ttu-id="6e2bc-123">Resumen de canales</span><span class="sxs-lookup"><span data-stu-id="6e2bc-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6e2bc-124">Requisitos previos de configuración de canales</span><span class="sxs-lookup"><span data-stu-id="6e2bc-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6e2bc-125">Configurar un canal en línea</span><span class="sxs-lookup"><span data-stu-id="6e2bc-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="6e2bc-126">Configurar un canal comercial</span><span class="sxs-lookup"><span data-stu-id="6e2bc-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="6e2bc-127">Configurar un canal de centro de llamadas</span><span class="sxs-lookup"><span data-stu-id="6e2bc-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)