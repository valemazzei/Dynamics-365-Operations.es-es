---
title: Identificar una hipótesis y determinar métricas para un experimento
description: Este tema describe cómo identificar la hipótesis y las métricas de éxito para un experimento que ejecutará en un sitio web de comercio electrónico en Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 43358264a2107fb139c00ce617054be16a74f935
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/22/2020
ms.locfileid: "4415672"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Identificar una hipótesis y determinar métricas de éxito para un experimento
La primera fase del ciclo de vida de la experimentación incluye identificar la hipótesis para el experimento y determinar las métricas que rastreará para evaluar el éxito. El siguiente diagrama muestra todos los pasos necesarios para [configurar y ejecutar un experimento](experimentation-overview.md) en un sitio web de comercio electrónico en Dynamics 365 Commerce. Los pasos adicionales se tratan en temas separados. 

[ ![Recorrido del usuario de experimentación: identificar](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Una hipótesis es una declaración en la que predice el resultado del experimento. Muchos factores intervienen en la definición de una hipótesis, por ejemplo, la investigación sobre el comportamiento del usuario y los datos del sitio web que ha recopilado. Con la hipótesis, definirás la suposición o teoría que deseas validar con tu experimento. Un ejemplo de hipótesis para su experimento puede ser "*una imagen de una camiseta blanca en mi página de inicio generará una tasa de clics más alta que un suéter azul marino durante los meses de verano porque la gente quiere usar algo liviano y de colores claros en el verano*". En ese caso, creará variaciones que incluyen una camiseta blanca y un suéter azul marino, y publicará ambos al mismo tiempo.

Para validar una hipótesis, el éxito o el fracaso de un experimento debe estar directamente relacionado con las acciones del usuario; por ejemplo, si el usuario del sitio web hace clic en un vínculo o botón. Estas acciones deben corresponder con eventos que se informarán al servicio de terceros que realiza el seguimiento del experimento. Con el tiempo, el porcentaje de usuarios que realizan la acción se contabilizará como una métrica que puede utilizar para generar informes y realizar análisis. Para revisar todos los eventos y atributos disponibles, consulte [Diagnóstico y solución de problemas de eventos de componentes de Commerce](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).

## <a name="previous-step"></a>Paso anterior
[Experimentación en Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Paso siguiente
[Configurar un experimento](experimentation-setup.md)
