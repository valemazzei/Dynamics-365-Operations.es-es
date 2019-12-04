---
title: Crear elementos de coste
description: Existen varias maneras de crear elementos de coste en la contabilidad de costes.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187806"
---
# <a name="create-cost-elements"></a><span data-ttu-id="8aa11-103">Crear elementos de coste</span><span class="sxs-lookup"><span data-stu-id="8aa11-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8aa11-104">Existen varias maneras de crear elementos de coste en la contabilidad de costes.</span><span class="sxs-lookup"><span data-stu-id="8aa11-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="8aa11-105">Este procedimiento muestra cómo crear elementos de costes importando las cuentas principales mediante un conector de datos.</span><span class="sxs-lookup"><span data-stu-id="8aa11-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="8aa11-106">Se ha utilizado la empresa de demostración USMF para crear este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="8aa11-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="8aa11-107">Este procedimiento se utiliza para la función contabilidad de cuentas, que se ha añadido a Dynamics 365 for Operations, versión 1611.</span><span class="sxs-lookup"><span data-stu-id="8aa11-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="8aa11-108">Crea nuevos elementos de coste.</span><span class="sxs-lookup"><span data-stu-id="8aa11-108">Create new cost elements</span></span>
1. <span data-ttu-id="8aa11-109">Vaya a contabilidad de costes > Dimensiones > dimensiones del elemento de coste.</span><span class="sxs-lookup"><span data-stu-id="8aa11-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="8aa11-110">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="8aa11-110">Click New.</span></span>
3. <span data-ttu-id="8aa11-111">En el campo Nombre, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="8aa11-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8aa11-112">En el conector de datos para el campo de miembros de dimensión, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="8aa11-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="8aa11-113">En el campo Descripción, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="8aa11-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8aa11-114">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="8aa11-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="8aa11-115">Configura el conector de datos</span><span class="sxs-lookup"><span data-stu-id="8aa11-115">Configure the data connector</span></span>
1. <span data-ttu-id="8aa11-116">Haga clic en Configurar proveedor de miembros de dimensión.</span><span class="sxs-lookup"><span data-stu-id="8aa11-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="8aa11-117">En el campo Plan de cuentas, introduzca o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="8aa11-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="8aa11-118">Seleccione Compartido para usar el plan contable compartido.</span><span class="sxs-lookup"><span data-stu-id="8aa11-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="8aa11-119">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="8aa11-119">Click New.</span></span>
4. <span data-ttu-id="8aa11-120">En la lista, marque la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8aa11-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8aa11-121">Puede aplicar filtros a las cuentas para que cumplan sus criterios.</span><span class="sxs-lookup"><span data-stu-id="8aa11-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="8aa11-122">En el campo Desde cuenta principal, introduzca o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="8aa11-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="8aa11-123">En el campo A la cuenta principal, introduzca o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="8aa11-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="8aa11-124">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="8aa11-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="8aa11-125">Importar cuentas principales</span><span class="sxs-lookup"><span data-stu-id="8aa11-125">Import main accounts</span></span>
1. <span data-ttu-id="8aa11-126">Haga clic en Importar miembros de dimensión.</span><span class="sxs-lookup"><span data-stu-id="8aa11-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="8aa11-127">Las cuentas principales se importarán a la contabilidad de costes y se utilizarán como elementos de coste.</span><span class="sxs-lookup"><span data-stu-id="8aa11-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="8aa11-128">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="8aa11-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="8aa11-129">Ver las cuentas importadas como elementos de coste</span><span class="sxs-lookup"><span data-stu-id="8aa11-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="8aa11-130">Haga clic en miembros de dimensión.</span><span class="sxs-lookup"><span data-stu-id="8aa11-130">Click View dimension members.</span></span>
    * <span data-ttu-id="8aa11-131">Ver las cuentas contables importadas como elementos de coste en su negocio a los que se pueden derivar costes.</span><span class="sxs-lookup"><span data-stu-id="8aa11-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  
