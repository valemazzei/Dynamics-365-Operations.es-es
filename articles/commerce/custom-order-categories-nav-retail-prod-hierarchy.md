---
title: Cambiar el orden de clasificación de entidades de comercialización
description: Este tema explica los conceptos relacionados con el control el orden de visualización para diversas entidades relacionadas con la comercialización en Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415542"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Cambiar el orden de clasificación de entidades de comercialización


[!include [banner](includes/banner.md)]

Los minoristas consideran el descubrimiento de productos una herramienta principal para la interacción de clientes en todos los canales. La funcionalidad Varios puede ayudar a los clientes a detectar fácilmente productos. Por ejemplo, pueden examinar categorías, buscar y filtrar.

Este tema explica los conceptos relacionados con el control el orden de visualización para diversas entidades relacionadas con la comercialización. También explica cómo cambiar el orden de clasificación.

## <a name="overview"></a>Información general

La compatibilidad para clasificar diversas entidades relacionadas con la comercialización se ha ampliado. Esta compatibilidad está ahora mejor alineada con los escenarios existentes de clientes, que requerían anteriormente extensiones por parte de socios de implementación.

En las versiones de Retail anteriores a la versión 10.0.5, el criterio de clasificación para las categorías de la jerarquía de navegación era alfabético. La nueva funcionalidad personalizada del orden de clasificación permite a los encargados de comercialización configurar el orden de clasificación para diversas entidades relacionadas con la comercialización en todos los clientes de usuario final. Estos clientes incluyen sedes empresariales y centros de llamadas.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Configurar el orden de visualización para las categorías de la jerarquía de productos

Antes de poder completar este procedimiento, los datos de prueba se deben instalar en el entorno.

1. Vaya a **Retail y Commerce \> Productos y categorías \> Jerarquía de productos de Commerce**.
2. Haga clic en **Editar jerarquía de categoría**.
3. Haga clic en **Editar**.
4. En el árbol, expanda **ALL \> Action Sports**.
5. En el árbol, expanda **ALL \> Team Sports**.
6. En el campo **Orden de visualización**, escriba un número. (El número puede ser negativo).
7. Repita los pasos del 4 al 6 para todas las categorías adicionales para las que desee cambiar el orden.

El orden de visualización para la jerarquía de navegación de canal se reflejará en la sede para la jerarquía de productos comerciales y productos liberados por categoría.

![Jerarquía de productos ordenada de forma personalizada con valores negativos](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Productos liberados por categoría ordenados de forma personalizada en función de la jerarquía de productos](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Configurar el orden de visualización para las categorías de la jerarquía de navegación de canales

Antes de poder completar este procedimiento, los datos de prueba se deben instalar en el entorno.

1. Vaya a **Retail y Commerce \> Productos y categorías \> Categorías de navegación de canales**.
2. En la lista, seleccione la jerarquía **Navegación de moda** .
3. Haga clic en **Editar jerarquía de categoría**.
4. Haga clic en **Editar**.
5. En el árbol seleccione, **Fashion \> Womenswear \> Womens Shoes**.
6. En el campo **Orden de visualización**, escriba un número.
7. En el árbol seleccione, **Fashion \> Womenswear \> Tops**.

    Del mismo modo, puede definir el orden de clasificación para las categorías secundarias.

8. En el árbol seleccione, **Fashion \> Menswear \> Casual Shirts**.
9. En el campo **Orden de visualización**, escriba un número.
10. En el árbol seleccione, **Fashion \> Menswear \> Coats & Jackets**.
11. En el campo **Orden de visualización**, escriba un número.
12. Repita los pasos para todas las categorías adicionales para las que desee cambiar el orden.

El orden de visualización para la jerarquía de navegación de canales se refleja en la sede, el catálogo y los canales.

![Jerarquía de navegación de canales ordenada de forma personalizada](./media/ChannelNavCustomSorted.png)

![Jerarquía de navegación de catálogos ordenada de forma personalizada en función de la jerarquía de navegación de canales](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![PDV con categorías ordenadas de forma personalizada](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> De forma predeterminada, la característica de orden de clasificación personalizado está desactivada. Para obtener información sobre cómo activar esta característica y otras, consulte [Administración de características](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).
