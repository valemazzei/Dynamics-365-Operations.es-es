---
title: Tarjetas de fidelización de clientes y puntos de recompensa
description: Este tema describe la integración de datos sobre tarjetas de fidelización de clientes y puntos de recompensa entre aplicaciones en escritura dual.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683507"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Tarjetas de fidelización de clientes y puntos de recompensa

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Las empresas clasifican a los clientes y brindan servicios sofisticados, basados en los patrones de compras y gastos de los clientes. Por ejemplo, Dynamics 365 Commerce, tiene la infraestructura y las funciones para facilitar y gestionar tarjetas de fidelización de clientes, puntos de recompensa, precios basados en lealtad y experiencias de compra basadas en recompensas. Cuando los datos sobre tarjetas de fidelización de clientes y puntos de recompensa en Commerce se sincronizan con Dataverse, las aplicaciones Customer Engagement pueden usar esos datos. Por ejemplo, los usuarios de Dynamics 365 Customer Service pueden usar los datos para proporcionar los mismos servicios sofisticados a través del servicio de asistencia.

## <a name="templates"></a>Plantillas

| Aplicaciones de Finance and Operations | Aplicaciones basadas en modelos en Dynamics 365 | Descripción |
|-----------------------------|-----------------------------------|-------------|
| Tarjeta de fidelización                | msdyn\_loyaltycards               | Esta plantilla sincroniza información sobre las tarjetas de fidelización del cliente. |
| Puntos de recompensa de fidelización       | msdyn\_loyaltyrewardpoints        | Esta plantilla sincroniza información sobre los puntos de recompensa del cliente. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
