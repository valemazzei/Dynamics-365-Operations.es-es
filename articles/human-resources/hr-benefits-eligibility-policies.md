---
title: Directivas de idoneidad para beneficio
description: Este artículo proporciona información acerca de las directivas de idoneidad de prestación, que le ayudan a definir quién es apto para las prestaciones específicas.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7b35d3f9a8afd3be44b648f6e138afd5f143ba55
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010541"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="5636b-103">Directivas de idoneidad para prestaciones</span><span class="sxs-lookup"><span data-stu-id="5636b-103">Benefit eligibility policies</span></span>

<span data-ttu-id="5636b-104">Este artículo proporciona información acerca de las directivas de idoneidad de prestación, que le ayudan a definir quién es apto para las prestaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="5636b-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="5636b-105">Cuando crea prestaciones, decide qué beneficios estarán disponibles para qué empleados.</span><span class="sxs-lookup"><span data-stu-id="5636b-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="5636b-106">En la tabla siguiente se muestran ejemplos de las prestaciones que puede poner a disposición de empleados específicos.</span><span class="sxs-lookup"><span data-stu-id="5636b-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="5636b-107">Prestación</span><span class="sxs-lookup"><span data-stu-id="5636b-107">Benefit</span></span>          | <span data-ttu-id="5636b-108">Para quién está disponible la prestación</span><span class="sxs-lookup"><span data-stu-id="5636b-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="5636b-109">Seguro médico</span><span class="sxs-lookup"><span data-stu-id="5636b-109">Health insurance</span></span> | <span data-ttu-id="5636b-110">Todos los empleados</span><span class="sxs-lookup"><span data-stu-id="5636b-110">All employees</span></span>                   |
| <span data-ttu-id="5636b-111">Teléfono móvil</span><span class="sxs-lookup"><span data-stu-id="5636b-111">Mobile phone</span></span>     | <span data-ttu-id="5636b-112">Personal de ventas, ejecutivos</span><span class="sxs-lookup"><span data-stu-id="5636b-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="5636b-113">Pases para aparcamiento</span><span class="sxs-lookup"><span data-stu-id="5636b-113">Parking passes</span></span>   | <span data-ttu-id="5636b-114">Ejecutivos</span><span class="sxs-lookup"><span data-stu-id="5636b-114">Executives</span></span>                      |

<span data-ttu-id="5636b-115">Se usan los siguientes componentes para crear directivas de idoneidad:</span><span class="sxs-lookup"><span data-stu-id="5636b-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="5636b-116">Tipos de reglas de directivas</span><span class="sxs-lookup"><span data-stu-id="5636b-116">Policy rule types</span></span>
-   <span data-ttu-id="5636b-117">Directivas de idoneidad para prestación</span><span class="sxs-lookup"><span data-stu-id="5636b-117">Benefit eligibility policies</span></span>

<span data-ttu-id="5636b-118">Los tipos de reglas de directivas definen los parámetros de consulta que se usan al desarrollar reglas de directivas específicas.</span><span class="sxs-lookup"><span data-stu-id="5636b-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="5636b-119">Tras crear tipos de reglas de directivas, puede crear directivas de idoneidad de prestación.</span><span class="sxs-lookup"><span data-stu-id="5636b-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="5636b-120">Las directivas le permiten crear una colección de reglas que se aplican a una o más entidades jurídicas.</span><span class="sxs-lookup"><span data-stu-id="5636b-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="5636b-121">Dentro de cada directiva, puede ver cualquiera de los tipos de reglas de directivas de idoneidad de prestación que haya creado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5636b-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="5636b-122">Define el ámbito de la regla dentro de la directiva.</span><span class="sxs-lookup"><span data-stu-id="5636b-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="5636b-123">Por ejemplo, si crea un tipo de regla de directivas de idoneidad de prestación que se llama **Ejecutivo**, puede especificar cuáles es la regla dentro de dicha directiva.</span><span class="sxs-lookup"><span data-stu-id="5636b-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="5636b-124">En este ejemplo, la regla podría indicar que se debe incluir en la regla cualquier título de trabajo que contenga la palabra "ejecutivo".</span><span class="sxs-lookup"><span data-stu-id="5636b-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="5636b-125">Una vez que haya definido los parámetros de la regla o las reglas que se incluyen en la directiva, puede asignar una regla específica a la prestación.</span><span class="sxs-lookup"><span data-stu-id="5636b-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>



