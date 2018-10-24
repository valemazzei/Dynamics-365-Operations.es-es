---
title: Novedades y cambios en Dynamics 365 for Talent Core HR (17 de septiembre de 2018)
description: "Este tema describe las características que son nuevas o que se han cambiado en Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: c4428613441424c81f4fd7dd92bbf842c62ce860
ms.openlocfilehash: 6586761fc62c13c701e8a8f61e15eedc66e2f751
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a><span data-ttu-id="3883d-103">Novedades y cambios en Dynamics 365 for Talent Core HR (17 de septiembre de 2018)</span><span class="sxs-lookup"><span data-stu-id="3883d-103">What's new or changed in Dynamics 365 for Talent Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3883d-104">**Compilación 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="3883d-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="3883d-105">Este tema describe las características que son nuevas o que se han cambiado en Core HR.</span><span class="sxs-lookup"><span data-stu-id="3883d-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="3883d-106">Baja y ausencias – tiempo acumulado basado en horas trabajadas</span><span class="sxs-lookup"><span data-stu-id="3883d-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="3883d-107">Se ha agregado un nuevo tipo de acumulación a los planes de licencias.</span><span class="sxs-lookup"><span data-stu-id="3883d-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="3883d-108">Ahora la programación de acumulaciones se podrá basar en los meses de servicio o las horas trabajadas.</span><span class="sxs-lookup"><span data-stu-id="3883d-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="3883d-109">Para obtener más información, consulte [Acumulación de licencias basada en las horas trabajadas](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="3883d-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18"></a><span data-ttu-id="3883d-110">Actualización de la plataforma 18</span><span class="sxs-lookup"><span data-stu-id="3883d-110">Platform update 18</span></span>

<span data-ttu-id="3883d-111">La actualización 18 de la plataforma es ahora parte de la versión de Talent.</span><span class="sxs-lookup"><span data-stu-id="3883d-111">Platform update 18 is now part of the Talent release.</span></span> 

-   <span data-ttu-id="3883d-112">Los campos obligatorios y otros se pueden ocultar a través de la personalización.</span><span class="sxs-lookup"><span data-stu-id="3883d-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="3883d-113">Esto le permite a un usuario crear una experiencia simplificada donde los campos obligatorios que son establecidos como valor predeterminado por la lógica de negocios no se muestran.</span><span class="sxs-lookup"><span data-stu-id="3883d-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="3883d-114">Los campos obligatorios ocultos también se muestran temporalmente si están vacíos cuando se intenta guardar.</span><span class="sxs-lookup"><span data-stu-id="3883d-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="3883d-115">En la plataforma actualizada 18, el cliente Web de Talent ahora adapta sus representaciones visuales al diseño fluido de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3883d-115">In Platform update 18, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="3883d-116">Cuando los campos se encuentran en “modo de lectura”, solo tiene que seleccionar la opción de edición de los campos para cambiar el formulario al modo edición.</span><span class="sxs-lookup"><span data-stu-id="3883d-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="3883d-117">Cambios en cómo los campos se muestran en modo de lectura.</span><span class="sxs-lookup"><span data-stu-id="3883d-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="3883d-118">Los encabezados en espacios de trabajo y las páginas están en negrita.</span><span class="sxs-lookup"><span data-stu-id="3883d-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="3883d-119">El comportamiento de las búsquedas que no reemplazan se han mejorado.</span><span class="sxs-lookup"><span data-stu-id="3883d-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="3883d-120">Para obtener más información, consulte [Comportamiento mejorado de las búsquedas que no sustituyen](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="3883d-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="3883d-121">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="3883d-121">Bug fixes</span></span>

<span data-ttu-id="3883d-122">Este lanzamiento incluye varias correcciones de errores adicionales, incluso las referencias a ACA, ADA, y I9 ahora solo están habilitadas en empresas estadounidenses.</span><span class="sxs-lookup"><span data-stu-id="3883d-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
