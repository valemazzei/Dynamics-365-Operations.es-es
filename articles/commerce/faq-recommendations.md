---
title: Preguntas más frecuentes de recomendaciones de producto
description: Este tema proporciona información sobre los procesos y las herramientas que puede utilizar para solucionar los problemas relacionados con las recomendaciones de productos o sus resultados.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f4f053066ef9a10ca8a60e6eb081f73401760eb4
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770125"
---
# <a name="product-recommendations-faq"></a>Preguntas más frecuentes de recomendaciones de producto

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Este tema proporciona información sobre los procesos y las herramientas que puede utilizar para solucionar los problemas relacionados con las [recomendaciones de productos](product-recommendations.md) o sus resultados.

## <a name="best-practices"></a>Prácticas recomendadas
Es muy importante usar el concepto de productos maestros y variantes. La agrupación sensata de variantes a un maestro de producto principal ayuda a algoritmos y servicio de la lista a crear mejores modelos. Además, el servicio puede servir solo una instancia de un producto en lugar de colocar todas las variantes estrechamente relacionadas en una lista. Cuando se colocan todas las variantes estrechamente relacionadas en una lista, se pueden producir resultados duplicados o erróneos.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>¿Por qué faltan productos de mis listas de recomendación?

Normalmente, si falta un artículo de una lista de recomendaciones de productos, puede haber un problema de la configuración de productos. Por ejemplo, puede haber una fecha inicial o una fecha final incorrecta de producto, puede haber una dimensión mal configurada o puede que el producto se encuentre en el surtido del canal correcto, etc.

Si falta un artículo de una lista de recomendaciones que se basa en inteligencia artificial-aprendizaje automático (AI-ML), es posible que el artículo no se ajuste a los criterios de la lista de recomendaciones o que no tenga suficientes transacciones de compra para que la lista de recomendaciones lo muestre.

Se recomienda que compruebe estos pasos:
1. **Asegúrese de que las recomendaciones de producto se hayan habilitado en la sede.** Para obtener información sobre cómo habilitar este servicio, consulte [Habilitar recomendaciones de producto](enable-product-recommendations.md).
1. **Asegúrese de que las propiedades de productos clave están establecidas.** Por ejemplo, los surtidos de productos se deben establecer en **Incluir**.
1. **Para productos surtidos recientemente, se pueden tardar 3 horas antes de que el producto empiece a aparecer en la nueva lista.**
1. **Si un artículo sigue sin aparecer en Tendencias, Más vendidos, A la gente también le gustó o Los usuarios que compraron esto también compraron, es posible que ese producto no tenga suficientes transacciones.** En este caso, puede esperar que se produzcan más transacciones, actualizar los parámetros predeterminados de la lista de recomendaciones o utilizar la intervención manual para modificar los resultados de la lista de productos de recomendación. Para obtener más información acerca de los parámetros de recomendación, consulte [Administrar resultados de recomendaciones de producto basadas en AI-ML](modify-product-recommendation-results.md).
1. **Asegúrese de que el producto cumple los criterios de recomendación para la lista.** Para obtener más información acerca de los parámetros de recomendación de productos, consulte [Administrar resultados de recomendaciones de producto basadas en AI-ML](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>¿Cómo puedo evitar que vuelvan los malos resultados de recomendaciones?

Las listas de recomendación requieren un gran volumen de transacciones para producir resultados. Por lo tanto, es importante que los usuarios proporcionen datos de transacción históricos completos.

Además, los productos sin transacciones o pocas transacciones no suelen tener resultados **A la gente también le gustó** o **Los usuarios que compraron esto también compraron**, y no aparecen en las listas de recomendaciones **Tendencias** o **Más vendidos**. Esta situación puede surgir a menudo para productos muy nuevos, o para productos antiguos que tienen una cantidad pequeña de compras. Los nuevos artículos populares superarán este error fácilmente.

Se recomienda que siga estos pasos:
1. **Asegúrese de que el producto cumple los criterios de recomendación para esa lista.** Para obtener más información acerca de los parámetros de recomendación de productos, consulte Modificar resultados de recomendaciones de producto basadas en AI-ML.
1. **Si el producto es nuevo, piense en modificar una lista de recomendaciones hasta que el producto tenga más transacciones.** Para obtener más información acerca de cómo modificar los resultados de la lista de recomendaciones, consulte [Administrar resultados de recomendaciones de producto basadas en AI-ML](modify-product-recommendation-results.md).


- **Asegúrese de que el producto cumple los criterios de recomendación para esa lista.** Para obtener más información acerca de los parámetros de recomendación de productos, consulte [Administrar resultados de recomendaciones de producto basadas en AI-ML](modify-product-recommendation-results.md).
- **Si el producto es nuevo, piense en modificar una lista de recomendaciones hasta que el producto tenga más transacciones**. Para obtener más información acerca de cómo modificar los resultados de la lista de recomendaciones, consulte [Administrar resultados de recomendaciones de producto basadas en AI-ML](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>¿Puedo quitar un producto pero seguir viéndolo en la tienda?

Puede ajustar listas que se generen de manera algorítmica si surge una necesidad empresarial. Sin embargo, si se quita un producto de una lista de recomendaciones, el producto seguirá siendo detectable en la tienda. Para obtener más información acerca de cómo modificar los resultados de recomendaciones de productos, consulte [Administrar resultados de recomendaciones de producto basadas en AI-ML](modify-product-recommendation-results.md).

Si debe bloquear un artículo de ser detectado en la tienda, debe cambiar el valor **Surtidos de artículos** a **Excluir**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>¿Cómo agrego una lista a una página de comercio electrónico?

Para obtener información acerca de cómo agregar páginas de recomendaciones de productos a su sitio web de comercio electrónico, consulte [Agregar listas de recomendaciones de producto a las páginas de comercio electrónico](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>¿Cómo habilito recomendaciones sobre PDV?

Después de habilitar recomendaciones de productos, deberá agregar el panel de las recomendaciones a la pantalla de PDV de control. Consulte [esta documentación de características](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) para obtener más información sobre cómo hacer para agregar el panel de recomendaciones al diseño de dispositivo de PDV.

## <a name="additional-resources"></a>Recursos adicionales

[Visión general de recomendaciones de producto](product-recommendations.md)

[Habilitar recomendaciones de producto](enable-product-recommendations.md)

[Administrar resultados de recomendaciones de producto basadas en AI-ML](modify-product-recommendation-results.md)