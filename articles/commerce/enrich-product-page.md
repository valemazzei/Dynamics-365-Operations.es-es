---
title: Enriquecer una página de producto
description: En este tema se describe cómo enriquecer una página de producto en Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9c0f329d21cdda5c36a39a8c602d5925b720f52
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945752"
---
# <a name="enrich-a-product-page"></a>Enriquecer una página de producto

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

En este tema se describe cómo enriquecer una página de producto en Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Visión general

De forma predeterminada, el sitio utiliza una página genérica para mostrar los datos del producto. Esta página incluye la información básica acerca del producto y los controles que se requieren para venderlo. Sin embargo, puede complementar la información proveniente de Retail Server con texto o imágenes adicionales para un producto específico. Este proceso se conoce como enriquecimiento de la página del producto.

En muchos casos, deseará usar contenido adicional específico para sus productos. Cuando vaya a **Retail** en la herramienta de creación, verá una lista de productos del canal que se asigna al sitio. En esta lista, la columna **Enriquecido** indica si se ha enriquecido la página del producto para un producto. Si aparece una marca de verificación en la columna, existe una página enriquecida del producto para el producto. Si aparece ninguna marca de verificación, la página y el contenido predeterminados del producto se usan para el producto. Puede obtener una vista preliminar de las páginas tanto enriquecidas como no enriquecidas del producto seleccionando un nombre del producto en la lista.

## <a name="enrich-a-product-page"></a>Enriquecer una página de producto

Para enriquecer un página del producto, siga estos pasos.

1. En **Sitios**, seleccione **Fabrikam** (o el nombre del sitio).
1. En el panel de navegación de la izquierda, seleccione **Productos**.
1. Seleccione los productos que no tengan una página enriquecida del producto.
1. En el panel de acciones, seleccione **Enriquecer página de producto**.
1. Seleccione **Plantilla de PDP** y, a continuación, seleccione **Aceptar**.
1. En el árbol del esquema de página de la izquierda, expanda la franja **Principal**.
1. Seleccione el botón de puntos suspensivos (**...**) para la franja **Principal** y, a continuación, seleccione **Agregar módulo**.
1. Seleccione **Contenedor 2** y, a continuación, seleccione **Aceptar**.
1. Seleccione el botón de puntos suspensivos para **Contenedor 2** y **Agregar módulo**.
1. Seleccione **Característica** y, a continuación, seleccione **Aceptar**.
1. En el panel de propiedades de la derecha, en el campo **Texto enriquecido**, escriba la descripción actualizada de producto.
1. En el campo **Encabezado**, inserte el texto del encabezado y, a continuación, seleccione **Aceptar**.
1. Seleccione **Guardar** y, a continuación, seleccione **Proteger**.
1. En el campo **Comentarios**, especifique **Enriquecer** y, a continuación seleccione **Aceptar**.
1. Seleccione **Vista previa** para obtener una vista previa de la página enriquecida del producto. Cuando haya terminado, cierre la pestaña de vista previa para volver a la herramienta de creación.
1. Seleccione **Publicar**.

## <a name="additional-resources"></a>Recursos adicionales

[Modificar una página de sitio existente](modify-existing-page.md)

[Agregar una página de sitio nueva](add-new-page.md)

[Seleccionar diseños de página](select-page-layouts.md)

[Administrar metadatos de SEO](manage-seo-metadata.md)

[Guardar, obtener una vista previa y publicar una página](save-preview-publish-page.md)

[Enriquecer una página de aterrizaje de categoría](enrich-category-page.md)

[Verificar accesibilidad de contenido de página](verify-accessibility.md)