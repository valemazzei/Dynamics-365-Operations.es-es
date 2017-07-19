---
title: "Contenido en Power BI sobre rendimiento de la producción"
description: "Este tema describe lo que se incluye en el contenido de Power BI sobre Rendimiento de la producción. Explica cómo obtener acceso a los informes de Power BI y proporciona información acerca del modelo de datos y las entidades que se utilizan para generar el contenido."
author: sericks
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 915ff93edff0f68f52a536ad169c8f0f917ac9b2
ms.contentlocale: es-es
ms.lasthandoff: 06/20/2017

---

# Contenido en Power BI sobre rendimiento de la producción
<a id="production-performance-power-bi-content" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Este tema describe lo que se incluye en el contenido de Microsoft Power BI sobre **Rendimiento de la producción**. Explica cómo obtener acceso a los informes de Power BI y proporciona información acerca del modelo de datos y las entidades que se utilizan para generar el contenido.

## Información general
<a id="overview" class="xliff"></a>

El contenido de Power BI sobre **Rendimiento de la producción** es para directores de producción o personas de la organización responsables del control de producción.

Los informes que se incluyen le permiten usar Power BI para controlar el rendimiento de las operaciones de fabricación en relación con la ejecución, la calidad y el coste oportunos. Los informes utilizan datos transaccionales de pedidos de producción y de lotes, y proporcionan tanto una vista global de medidas empresariales de la producción y un desglose de medidas por producto y recurso.

El contenido de Power BI destaca la capacidad de la organización para completar la producción a tiempo y completamente. El rendimiento futuro se proyecta en función de los planes de producción. Los informes completos proporcionan conocimientos detallados de los defectos de los productos causados por la producción, así como del índice de defectos para recursos y operaciones.

Este contenido de Power BI también le permite analizar las desviaciones de producción. Las desviaciones de producción se calculan como la diferencia entre el coste estimado y el coste realizado. Las desviaciones de producción se calculan cuando los pedidos de producción o los pedidos de lote alcanzan el estado **Terminado** .

El contenido de Power BI sobre **Rendimiento de la producción** incluye datos procedentes de pedidos de producción y de pedidos de lote. Los informes no incluyen datos relacionados con las producciones de kanban.

## Acceso al contenido de Power BI
<a id="accessing-the-power-bi-content" class="xliff"></a>
Si está usando la actualización de julio de 2017 de Microsoft Dynamics 365 for Finance and Operations, Enterprise Editions , el contenido de Power BI sobre **Rendimiento de la producción** se muestra en la página **Rendimiento de la producción** (**Control de la producción** > **Consultas e informes** > **Análisis del rendimiento de la producción** > **Rendimiento de la producción**). 

## Métricas que se incluyen en el contenido de Power BI
<a id="metrics-that-are-included-in-the-power-bi-content" class="xliff"></a>

El contenido de Power BI sobre **Rendimiento de la producción** incluye un conjunto de páginas de informes. Cada página consta de un conjunto de métricas que se visualizan como gráficos, mosaicos y tablas.

La tabla siguiente proporciona información general de las visualizaciones que se incluyen.

| Página de informes                                | Gráficos                                               | Mosaicos |
|--------------------------------------------|------------------------------------------------------|-------|
| Rendimiento de producción                     | <ul><li>Número de producción por fecha</li><li>Número de producciones por producto y grupo de artículos</li><li>Número de producciones planificadas por fecha</li><li>10 últimos productos por puntualidad y completitud</li></ul> | <ul><li>Total de pedidos</li><li>Porcentaje de puntuales y completados</li><li>Porcentaje de incompletos</li><li>Porcentaje de finalizados con antelación</li><li>Porcentaje de finalizados con retraso</li></ul> |
| Defectos por producto                         | <ul><li>Tasa de defectos (ppm) por fecha</li><li>Tasa de defectos (ppm) por producto y grupo de artículos</li><li>Cantidad producida por fecha</li><li>10 primeros productos por tasa de defectos</li></ul> | <ul><li>Tasa de defectos (ppm)</li><li>Cantidad defectuosa</li><li>Cantidad total</li></ul> |
| Tendencia de defectos por producto                   | Tasa de defectos (ppm) por cantidad producida | Tasa de defectos (ppm) |
| Defectos por recurso                        | <ul><li>Tasa de defectos (ppm) por fecha</li><li>Tasa de defectos (ppm) por recurso y ubicación</li><li>Tasa de defectos (ppm) por operación</li><li>10 primeros recursos por tasa de defectos</li></ul> | Cantidad defectuosa |
| Tendencia de defectos por recurso                  | Tasa de defectos (ppm) por cantidad procesada | |
| Desviaciones de producción para gestión de costes de órdenes de producción | <ul><li>Desviación de producción por fecha y tipo de grupo de costes</li><li>Desviación de producción por ubicación y tipo de grupo de costes</li><li>10 primeros productos con desviación de producción desfavorable</li><li>10 primeros con desviación de producción desfavorable por recurso</li></ul> | <ul><li>Coste realizado</li><li>Desviación de producción</li><li>Porcentaje de desviación de producción</li></ul> |

## Ampliar el contenido de Power BI
<a id="extending-the-power-bi-content" class="xliff"></a>
Mediante los paquetes de contenido disponibles en Microsoft Dynamics Lifecycle Services (LCS), puede ofrecer análisis muy buenos a las personas que no inician sesión en Microsoft Dynamics 365. Puede modificar estos paquetes de contenido para que incluyan otros informes o representaciones visuales y, a continuación, publicar los paquetes de contenidos en el inquilino de Power BI.com para su análisis.

Puede encontrar el contenido de Power BI sobre **Rendimiento de la producción** en la biblioteca de activos compartidos de LCS. Para obtener información sobre cómo descargar contenido e implementarlo en su organización, consulte [Contenido de Power BI en LCS en Microsoft y sus socios](power-bi-content-microsoft-partners.md). Para ver una demostración que muestra cómo implementar el contenido de Power BI, consulte [Contenido de Power BI de Microsoft y sus socios en Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Asegúrese de descargar el contenido sobre **Rendimiento de la producción** que se aplica a la versión de Dynamics 365 que esté usando.

> [!NOTE]
> Si utiliza Microsoft Dynamics 365 for Operations, versión 1611, KB 4011327 es un requisito para este contenido de Power BI. Tras iniciar sesión en LCS, puede acceder a KB en https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## Comprensión del modelo de datos y de las entidades
<a id="understanding-the-data-model-and-entities" class="xliff"></a>

Los datos siguientes se usan para las páginas de informes en el contenido de Power BI sobre **Rendimiento de la producción**. Estos datos se representan como medidas agregadas que se realizan en el almacén de la entidad. El almacén de la entidad es una base de datos de Microsoft SQL Server que se optimiza para el análisis. Para obtener más información acerca del almacén de entidades, consulte [Integración de Power BI con el almacén de entidades](power-bi-integration-entity-store.md).

La tabla siguiente muestra las medidas agregadas clave que se usan como base del contenido de Power BI.

| Entidad                   | Medidas agregadas clave  | Origen de datos para Finance and Operations | Campo              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Se usará la tabla siguiente para mostrar cómo se usan las medidas agregadas clave para crear varias medidas calculadas en el conjunto de datos del contenido.

| Medida                  | Cómo se calcula la medida |
|--------------------------|-------------------------------|
| Desviación de la producción, en %   | SUM('Desviación de la producción'[Desviación de la producción]) / SUM('Desviación de la producción'[Coste estimado]) |
| Todos los pedidos planificados       | COUNTROWS('Pedido de producción planificado') |
| Con antelación                    | COUNTROWS(FILTER('Pedido de producción planificado', 'Pedido de producción planificado'[Fecha final programada] \< 'Pedido de producción planificado'[Fecha de requisito])) |
| Con retraso                     | COUNTROWS(FILTER('Pedido de producción planificado', 'Pedido de producción planificado'[Fecha final programada] \> 'Pedido de producción planificado'[Fecha de requisito])) |
| Puntual                  | COUNTROWS(FILTER('Pedido de producción planificado', 'Pedido de producción planificado'[Fecha final programada] = 'Pedido de producción planificado'[Fecha de requisito])) |
| Porcentaje de puntuales                | IF ( 'Pedido de producción planificado'[Puntual] \<\> 0, 'Pedido de producción planificado'[Puntual], IF ('Pedido de producción planificado'[Todos los pedidos planificados] \<\> 0, 0, BLANK()) ) / 'Pedido de producción planificado'[Todos los pedidos planificados] |
| Finalizado                | COUNTROWS(FILTER('Pedido de producción', 'Pedido de producción'[Notificado como terminado] = TRUE)) |
| Tasa de defectos (ppm)     | SI( 'Pedido de producción'[Cantidad total] = 0, BLANK(), (SUM('Pedido de producción'[Cantidad defectuosa]) / 'Pedido de producción'[Cantidad total]) \* 1000000) |
| Tasa de producción retrasada  | 'Pedido de producción'[Retrasado \#] / 'Pedido de producción'[Completado] |
| Con antelación y completados          | COUNTROWS(FILTER('Pedido de producción', 'Pedido de producción'[Completado] = TRUE && 'Pedido de producción'[Con antelación] = TRUE)) |
| Con antelación \#                 | COUNTROWS(FILTER('Pedido de producción', 'Pedido de producción'[Con antelación] = TRUE)) |
| Porcentaje de finalizados con antelación                  | IFERROR( IF('Pedido de producción'[Con antelación \#] \<\> 0, 'Pedido de producción'[Con antelación \#], IF('Pedido de producción'[Total de pedidos] = 0, BLANK(), 0)) / 'Pedido de producción'[Total de pedidos], BLANK()) |
| Incompleto               | COUNTROWS(FILTER('Pedido de producción', 'Pedido de producción'[Completado] = FALSE && 'Pedido de producción'[Notificado como terminado] = TRUE)) |
| Porcentaje de incompletos             | IFERROR( IF('Pedido de producción'[Incompleto] \<\> 0, 'Pedido de producción'[Incompleto], IF('Pedido de producción'[Total de pedidos] = 0, BLANK(), 0)) / 'Pedido de producción'[Total de pedidos], BLANK()) |
| Se retrasa               | 'Pedido de producción'[Notificado como terminado] = TRUE && 'Pedido de producción'[Valor de retrasado] = 1 |
| Con antelación                 | 'Pedido de producción'[Notificado como terminado] = TRUE && 'Pedido de producción'[Días de retraso] \< 0 |
| Completado               | 'Pedido de producción'[Buena cantidad] \>= 'Pedido de producción'[Cantidad programada] |
| Notificado como terminado                | 'Pedido de producción'[Valor de estado de producción] = 5 \|\| 'Pedido de producción'[Valor de estado de producción] = 7 |
| Tarde y completo           | COUNTROWS(FILTER('Pedido de producción', 'Pedido de producción'[Completado] = TRUE && 'Pedido de producción'[Con retraso] = TRUE)) |
| Cetraso \#                  | COUNTROWS(FILTER('Pedido de producción', 'Pedido de producción'[Con retraso] = TRUE)) |
| Porcentaje de finalizados con retraso                   | IFERROR( IF('Pedido de producción'[Con retraso \#] \<\> 0, 'Pedido de producción'[Con retraso \#], IF('Pedido de producción'[Total de pedidos] = 0, BLANK(), 0)) / 'Pedido de producción'[Total de pedidos], BLANK()) |
| Puntuales y completados        | COUNTROWS(FILTER('Pedido de producción', 'Pedido de producción'[Completado] = TRUE && 'Pedido de producción'[Con retraso] = FALSE && 'Pedido de producción'[Con antelación] = FALSE)) |
| Porcentaje de puntuales y completados      | IFERROR( IF('Pedido de producción'[Puntual y completo] \<\> 0, 'Pedido de producción'[Puntual y completo], IF('Pedido de producción'[Completo] = 0, BLANK(), 0)) / 'Pedido de producción'[Completo], BLANK()) |
| Total de pedidos             | COUNTROWS('Pedido de producción') |
| Cantidad total           | SUM('Pedido de producción'[Cantidad sin errores]) + SUM('Pedido de producción'[Cantidad defectuosa]) |
| Tasa de defectos (ppm)        | IF( 'Transacciones de ruta'[Cantidad procesada] = 0, BLANK(), (SUM('Transacciones de ruta'[Cantidad defectuosa]) / 'Transacciones de ruta'[Cantidad procesada]) \* 1000000) |
| Proporción defectuosa mezclada (ppm) | IF( 'Transacciones de ruta'[Total de cantidad mezclada] = 0, BLANK(), (SUM('Transacciones de ruta'[Cantidad defectuosa]) / 'Transacciones de ruta'[Total de cantidad mezclada]) \* 1000000) |
| Cantidad procesada       | SUM('Transacciones de ruta'[Cantidad sin errores]) + SUM('Transacciones de ruta'[Cantidad defectuosa]) |
| Total de cantidad mezclada     | SUM('Pedido de producción'[Cantidad sin errores]) + SUM('Transacciones de ruta'[Cantidad defectuosa]) |

Las tabla siguiente muestra las dimensiones clave que se utilizan como filtros para cortar las medidas globales de forma que logre mayor granularidad y profundizar en la visión analítica.

| Entidad                    | Ejemplos de atributos                                        |
|---------------------------|---------------------------------------------------------------|
| Notificado como fecha finalizada | Fecha de finalización (notificada como terminada), contrapartida mensual y anual                 |
| Fecha de finalización                | Contrapartida mensual terminada y mes                                  |
| Fecha de requisito          | Contrapartida mensual de fecha de requisito y fecha de requisito            |
| Fecha de transacción de ruta    | Contrapartida mensual de transacción de ruta y fecha                       |
| Sitios                     | Identificador de sitios, nombre del sitio, estado y localidad                          |
| Entidades                  | Identificador y nombre                                                   |
| Recursos                 | Identificador de recurso, nombre de recurso, tipo de recurso y grupo de recursos |
| Productos                  | Número de producto, nombre de producto, identificador de artículo y grupo de artículos         |

## Recursos adicionales
<a id="additional-resources" class="xliff"></a>

Estos son algunos vínculos útiles relacionados con las entidades y la creación de contenido de Power BI:

- [Entidades de datos](https://ax.help.dynamics.com/en/wiki/data-entities/)
- [Creación de paquetes de contenido organizativo](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Modelado de datos con Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Adición de iconos de Power BI a espacios de trabajo](http://ax.help.dynamics.com/en/wiki/configuring-powerbi-integration/)
