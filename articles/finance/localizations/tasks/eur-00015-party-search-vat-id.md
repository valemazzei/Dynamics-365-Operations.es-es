---
title: EUR-00015 Búsqueda de la parte mediante el Id. de IVA
description: Este procedimiento muestra cómo realizar una búsqueda de parte mediante un identificador de registro.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0427b6e961173543f860ef6e098fc6248afd3aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183569"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="65497-103">EUR-00015 Búsqueda de la parte mediante el Id. de IVA</span><span class="sxs-lookup"><span data-stu-id="65497-103">EUR-00015 Party search using VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65497-104">Este procedimiento muestra cómo realizar una búsqueda de parte mediante un identificador de registro.</span><span class="sxs-lookup"><span data-stu-id="65497-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="65497-105">Antes de poder completar este procedimiento, debe configurar identificadores de IVA y especificar cualquier Id. de IVA para proveedores, clientes o entidades jurídicas.</span><span class="sxs-lookup"><span data-stu-id="65497-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="65497-106">Este procedimiento se aplica a todos los países o regiones europeos.</span><span class="sxs-lookup"><span data-stu-id="65497-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="65497-107">Este procedimiento se ha creado con los datos de demostración de la empresa DEMF y con una dirección principal en Alemania.</span><span class="sxs-lookup"><span data-stu-id="65497-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="65497-108">Este procedimiento se ha creado para un administrador de proveedores o un administrador de clientes.</span><span class="sxs-lookup"><span data-stu-id="65497-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="65497-109">Este procedimiento es para una función que se ha agregado en la versión 1611 de Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="65497-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="65497-110">Vaya a Administración de la organización > Libreta de direcciones global > Libreta de direcciones global.</span><span class="sxs-lookup"><span data-stu-id="65497-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="65497-111">Haga clic en Búsqueda de id. de registro.</span><span class="sxs-lookup"><span data-stu-id="65497-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="65497-112">Haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="65497-112">Click Add.</span></span>
4. <span data-ttu-id="65497-113">En el campo Tipo de registro, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="65497-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="65497-114">Por ejemplo, en el caso de que desee encontrar a las partes con un identificador de registro del tipo identificador de IVA, seleccione el identificador del IVA.</span><span class="sxs-lookup"><span data-stu-id="65497-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="65497-115">En el campo País o región, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="65497-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="65497-116">Por ejemplo, escriba DEU.</span><span class="sxs-lookup"><span data-stu-id="65497-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="65497-117">En el campo Número de registro, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="65497-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="65497-118">Haga clic en Buscar.</span><span class="sxs-lookup"><span data-stu-id="65497-118">Click Find.</span></span>
    * <span data-ttu-id="65497-119">Todas partes con ese identificador del registro se mostrará.</span><span class="sxs-lookup"><span data-stu-id="65497-119">All parties with that registration ID will be displayed.</span></span>  
