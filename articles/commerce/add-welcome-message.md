---
title: Agregar un mensaje de bienvenida
description: Este tema describe cómo agregar un mensaje de bienvenida en su sitio web de Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d2a125b4e71016ad620f128af2e3c9f29aa04f4c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415487"
---
# <a name="add-a-welcome-message"></a>Agregar un mensaje de bienvenida


[!include [banner](includes/banner.md)]

Este tema describe cómo agregar un mensaje de bienvenida en su sitio web de Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Visión general

Un mensaje de bienvenida en su sitio web de comercio electrónico puede informar a los visitantes acerca de las ventas continuas, las actualizaciones de sitio o la disponibilidad de colecciones de temporada. El mensaje de bienvenida se establece mediante el módulo de alerta.

El módulo de alerta se debe agregar al espacio **Mensajes de error o información** del fragmento de encabezado. El módulo de alerta le permite especificar el texto que se muestra, el color de texto y la alineación. También le permite especificar si los visitantes al sitio pueden descartar el mensaje.

Cuando se agrega un mensaje de bienvenida a un fragmento de encabezado compartido, se mostrará en todas las páginas que use la plantilla en la que se usa el fragmento de encabezado compartido.

Para agregar un mensaje de bienvenida al sitio, siga estos pasos.

1. En el generador de sitios de Commerce, vaya a su sitio.
1. Seleccione **Fragmentos**.
1. Seleccione el fragmento de encabezado al que agregar el mensaje.
1. En el árbol de esquema, expanda **Mensajes de error o información**.
1. Seleccione el módulo de alerta y, a continuación, seleccione **Aceptar**. Si no existe todavía un módulo de alerta, primero seleccione los puntos suspensivos (**...**) situados junto a **Mensajes de error o información** y, a continuación, seleccione **Agregar módulo**.
1. En el panel de propiedades de la derecha, en la pestaña **Datos**, seleccione **Agregar origen de datos** y, a continuación, **Contenido**.
1. En el campo **Texto de entrada**, escriba el texto del mensaje de bienvenida.
1. Seleccione **Guardar** y seleccione **Finalizar edición** para proteger el fragmento de encabezado y luego seleccione **Publicar** para publicarlo. 

El mensaje de bienvenida aparecerá ahora en la parte superior de cada página del sitio que usa el fragmento de encabezado seleccionado.

## <a name="additional-resources"></a>Recursos adicionales

[Agregar un logotipo](add-logo.md)

[Seleccionar un tema de sitio](select-site-theme.md)

[Trabajar con archivos de invalidaciones CSS](css-override-files.md)

[Agregar un icono de favoritos](add-favicon.md)

[Agregar un aviso de derechos de autor](add-copyright-notice.md)

[Agregar idiomas al sitio](add-languages-to-site.md)

[Agregar secuencia de comandos a páginas del sitio para admitir telemetría](add-telemetry.md)

