---
title: Estados de administración de transporte
description: Este tema explica cómo crear un estado de transporte y asignar ese estado a un estado de transportista.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/29/2020
ms.locfileid: "4437316"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="073ca-103">Estados de administración de transporte</span><span class="sxs-lookup"><span data-stu-id="073ca-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="073ca-104">Configure códigos maestros de estados de transporte para interpretar códigos proporcionados por sus transportistas de envío.</span><span class="sxs-lookup"><span data-stu-id="073ca-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="073ca-105">Esto le permite integrarse con los transportistas de envío para proporcionar un estado.</span><span class="sxs-lookup"><span data-stu-id="073ca-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="073ca-106">El estado del transporte que proporciona para un código de estado maestro de transporte puede ayudarle a realizar un seguimiento del estado de una carga, de un envío o de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="073ca-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="073ca-107">El estado de transporte específico para una carga, envío o contenedor solo se puede actualizar mediante la integración de datos y no manualmente a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="073ca-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="073ca-108">Crear un estado de transporte</span><span class="sxs-lookup"><span data-stu-id="073ca-108">Create a transportation status</span></span>

<span data-ttu-id="073ca-109">Para crear un estado de transporte, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="073ca-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="073ca-110">Vaya a **Administración de transporte \> Configuración \> Maestros de estado de transporte**.</span><span class="sxs-lookup"><span data-stu-id="073ca-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="073ca-111">Seleccione **Nuevo** para crear un nuevo estado maestro de transporte.</span><span class="sxs-lookup"><span data-stu-id="073ca-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="073ca-112">En el campo **Maestro de estado de transporte**, escriba un código único para el código de transporte.</span><span class="sxs-lookup"><span data-stu-id="073ca-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="073ca-113">En el campo **Tipo de transporte**, seleccione ya sea *Transportista de envío* o *Cubo* como el tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="073ca-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="073ca-114">Ingrese un nombre y estado de transporte.</span><span class="sxs-lookup"><span data-stu-id="073ca-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="073ca-115">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="073ca-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="073ca-116">Asignar un estado de transporte a un estado de transportista</span><span class="sxs-lookup"><span data-stu-id="073ca-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="073ca-117">Para asignar un estado de transporte a un estado de transportista, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="073ca-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="073ca-118">Vaya a **Administración de transporte \> Configuración \> Transportistas \> Maestros de estado de transporte**.</span><span class="sxs-lookup"><span data-stu-id="073ca-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="073ca-119">Seleccione **Nuevo** para asignar un código de un transportista de envío a un código maestro de estado de transporte.</span><span class="sxs-lookup"><span data-stu-id="073ca-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="073ca-120">Seleccione la identificación única para el transportista de envío y el servicio de transportista.</span><span class="sxs-lookup"><span data-stu-id="073ca-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="073ca-121">Seleccione el código de estado del transporte que desea asignar al código del transportista de envío seleccionado.</span><span class="sxs-lookup"><span data-stu-id="073ca-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="073ca-122">Especifique el código externo que usa el transportista de envío.</span><span class="sxs-lookup"><span data-stu-id="073ca-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="073ca-123">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="073ca-123">Close the page.</span></span>