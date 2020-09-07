---
title: Módulo de mapa
description: En este tema se tratan los módulos de mapa y se describe cómo configurarlos en Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/31/2020
ms.locfileid: "3647040"
---
# <a name="map-module"></a>Módulo de mapa

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

En este tema se tratan los módulos de mapa y se describe cómo configurarlos en Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Información general

Un módulo de mapa muestra las ubicaciones de las tiendas en un mapa interactivo que se representa utilizando el [Control web de Bing Maps V8](https://docs.microsoft.com/bingmaps/v8-web-control/). Se requiere una clave de la API de Bing Maps, y debe agregarse a la página de parámetros compartidos en la Central de Commerce. Los módulos de mapa proporcionan diferentes vistas, como Carretera, Aérea y A pie de calle, que los usuarios pueden seleccionar para ver las ubicaciones de los mapas. También permiten interacciones como hacer zoom y usar la ubicación del usuario.

Un módulo de mapa funciona junto con el módulo selector de tiendas para determinar las ubicaciones geográficas de las tiendas que deben representarse en un mapa. El selector de tienda y los módulos de mapa interactúan cuando un usuario selecciona una tienda en uno de esos módulos en una página del sitio. Los módulos de mapas se pueden ampliar para otros escenarios, más allá de la interacción con los módulos de selector de tienda. Sin embargo, se requiere la personalización del módulo.

El módulo de mapa se incorporó en Commerce, versión 10.0.13.

La siguiente imagen muestra un ejemplo de un módulo de mapa utilizado en una página ubicación de tiendas.

![Ejemplo de un módulo selector de tienda](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Propiedades del módulo

| Nombre de la propiedad             | Valor                 | Descripción |
|---------------------------|-----------------------|-------------|
| Cabecera | Texto | El encabezado del módulo. |
| Opciones de chincheta: icono predeterminado | Imagen | La imagen del símbolo de chincheta, que se usará para las tiendas que se aparecen en un mapa. |
| Opciones de chincheta: icono activo | Imagen | La imagen del símbolo de chincheta, que se usará para las tiendas seleccionadas en un mapa. |
| Opciones de chincheta: color de icono predeterminado | Cadena de caracteres | El texto o valor hexadecimal para el color de los símbolos de chincheta en un mapa. |
| Opciones de chincheta: color icono activo | Cadena de caracteres | El texto o valor hexadecimal para el color de los símbolos de chincheta seleccionados en un mapa. |
| Mostrar índice | **Verdadero** o **Falso** | Si esta propiedad se establece en **True**, cada símbolo de chincheta que indica una tienda mostrará un índice. Este índice coincidirá con el índice en la vista de lista que muestra el módulo selector de tienda. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Agregar direcciones URL de asignación permitidas a las directivas de política de seguridad de contenido de un sitio

Para que el módulo de mapas interactúe con Bing Maps, debe asegurarse de que las siguientes direcciones URL de asignación estén permitidas (también conocidas como "pertenecientes a la lista blanca") según la directiva de seguridad de contenido (CSP) de su sitio. Esta configuración se realiza en el creador de sitios de Commerce, agregando las direcciones URL permitidas a varias directivas CSP del sitio (por ejemplo, **img-src**). Para más información, consulte [Directiva de seguridad de contenido](manage-csp.md). 

- Para la directiva **connect-src**, agregue **&#42;.bing.com**.
- Para la directiva **img-src**, agregue **&#42;.virtualearth.net**.
- A la directiva **script-src**, agregue **&#42;.bing.com, &#42;.virtualearth.net**.
- Para la directiva **script style-src**, agregue **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Agregar un módulo de mapa a una página

Para obtener información detallada sobre cómo configurar un módulo de mapa en una página, vea [Módulo selector de tienda](store-selector.md). 
 
## <a name="additional-resources"></a>Recursos adicionales

[Visión general del kit de inicio](starter-kit-overview.md)

[Módulo de cuadro de compra](add-buy-box.md)

[Módulo de carro](add-cart-module.md)

[Módulo de selector de tienda](store-selector.md)

[Administrar Mapas de Bing para su organización](./dev-itpro/manage-bing-maps.md)

[Control web de Bing Maps V8](https://docs.microsoft.com/bingmaps/v8-web-control/)