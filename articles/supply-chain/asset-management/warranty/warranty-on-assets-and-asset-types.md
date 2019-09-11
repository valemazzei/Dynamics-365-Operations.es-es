---
title: Garantías de activos y tipos de activos
description: Este tema explica cómo configurar garantías de activos y tipos de activos en Administración de activos.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874610"
---
# <a name="warranty-on-assets-and-asset-types"></a><span data-ttu-id="1f12b-103">Garantía de activos y tipos de activos</span><span class="sxs-lookup"><span data-stu-id="1f12b-103">Warranty on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="1f12b-104">Este tema explica cómo configurar garantías de activos y tipos de activos en Administración de activos.</span><span class="sxs-lookup"><span data-stu-id="1f12b-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="1f12b-105">Configuración de una garantía de un tipo de activo</span><span class="sxs-lookup"><span data-stu-id="1f12b-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="1f12b-106">Seleccione **Administración de activos** \> **Configuración** \> **Tipos de activos** \> **Tipos de activos**.</span><span class="sxs-lookup"><span data-stu-id="1f12b-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="1f12b-107">En el panel izquierdo, seleccione el tipo de activo al que vincular un acuerdo de la garantía de proveedor y, a continuación seleccione **Valores predeterminados de tipo de activo**.</span><span class="sxs-lookup"><span data-stu-id="1f12b-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="1f12b-108">En la ficha desplegable **General**, en el campo **Garantía de proveedor**, seleccione el acuerdo.</span><span class="sxs-lookup"><span data-stu-id="1f12b-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="1f12b-109">Configuración de una garantía de un activo</span><span class="sxs-lookup"><span data-stu-id="1f12b-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="1f12b-110">Seleccione **Administración de activos** \> **Común** \> **Activos** \> **Todos los activos**.</span><span class="sxs-lookup"><span data-stu-id="1f12b-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="1f12b-111">Seleccione el activo y, a continuación, seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="1f12b-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="1f12b-112">En la ficha desplegable **Proveedor**, en la sección **Garantía del proveedor**, en el campo **Garantía**, seleccione el contrato de la garantía.</span><span class="sxs-lookup"><span data-stu-id="1f12b-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="1f12b-113">En los campos **Inicio de la garantía** y **Fin de la garantía**, seleccione las fechas inicial y final.</span><span class="sxs-lookup"><span data-stu-id="1f12b-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1f12b-114">Si una fecha se selecciona en el campo **Inicio de la garantía** en un pedido de trabajo, la garantía empezará a ser válida para la orden de trabajo en esa fecha.</span><span class="sxs-lookup"><span data-stu-id="1f12b-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="1f12b-115">Al crear un pedido de trabajo, el campo **Inicio de la garantía** se establece automáticamente en la fecha de creación.</span><span class="sxs-lookup"><span data-stu-id="1f12b-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="1f12b-116">Sin embargo, puede cambiar la fecha de modo que corresponda a, por ejemplo, la fecha inicial de un acuerdo de la garantía.</span><span class="sxs-lookup"><span data-stu-id="1f12b-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Figura 1](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="1f12b-118">Al crear un pedido de trabajo para un activo cubierto por una garantía del proveedor, si la orden de trabajo tiene una fecha de inicio prevista durante el período de garantía, usted recibirá una notificación sobre el acuerdo de la garantía.</span><span class="sxs-lookup"><span data-stu-id="1f12b-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="1f12b-119">En ese momento podrás cancelar la orden de trabajo, como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="1f12b-119">You can then cancel the work order, as you require.</span></span>