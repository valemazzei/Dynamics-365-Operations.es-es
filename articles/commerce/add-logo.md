---
title: Agregar un logotipo
description: En este tema se describe cómo agregar un logotipo a su sitio en Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914634"
---
# <a name="add-a-logo"></a>Agregar un logotipo

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

En este tema se describe cómo agregar un logotipo a su sitio en Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Visión general

Cuando crea su sitio, una de las primeras cosas que probablemente hará es agregar el logotipo de su empresa o marca al encabezado del sitio. El kit de inicio en línea de Dynamics 365 Commerce proporciona un módulo que facilita esta tarea.

Puede agregar un logotipo directamente a una plantilla, diseño o página. De esta manera, puede cambiar fácilmente el logotipo que aparece en páginas específicas o grupos de páginas. Sin embargo, este tema cubre el escenario más frecuente, donde agrega su logotipo a un fragmento de encabezado que puede reutilizarse en todas las páginas de su sitio.

## <a name="prerequisites"></a>Requisitos previos

Antes de poder agregar un logotipo a todas las páginas de su sitio, debe completar estas tareas.

1. Suba su logotipo al administrador de activos digitales, al que puede acceder desde la página **Activos**.
1. Crear un fragmento de encabezado. Para obtener más información sobre cómo crear y usar fragmentos, vea [Trabajar con fragmentos](work-with-fragments.md).
1. Incluya el fragmento de encabezado en la plantilla que usan las páginas de su sitio para su diseño y opciones de módulo. Para obtener más información sobre las plantillas, vea [Trabajar con plantillas](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Agregar un logotipo a un fragmento de encabezado

Para agregar un logotipo al fragmento de encabezado de su sitio, siga estos pasos.

1. En el panel de navegación a la izquierda, seleccione **Fragmentos** y luego seleccione el fragmento de encabezado que creó.
2. Seleccione **Desproteger**.
3. Expanda el espacio **Encabezado** y el espacio **Logotipo**.
4. Seleccione el botón de puntos suspensivos (**...**) para el espacio **Logotipo** y, a continuación, seleccione **Agregar módulo**.
5. Seleccione el módulo de logotipo.
6. En el panel de propiedades de la derecha, configure el módulo logotipo para que muestre su logotipo.
7. Guarde el fragmento de encabezado, protéjalo y publíquelo.

Después de publicar el fragmento de encabezado actualizado, todas las páginas del sitio que usan la plantilla que contiene el fragmento de encabezado mostrarán su logotipo.

## <a name="additional-resources"></a>Recursos adicionales

[Seleccionar un tema de sitio](select-site-theme.md)

[Trabajar con archivos de invalidaciones CSS](css-override-files.md) 

[Agregar un icono de favoritos](add-favicon.md)

[Agregar un mensaje de bienvenida](add-welcome-message.md)

[Agregar un aviso de derechos de autor](add-copyright-notice.md)

[Agregar idiomas al sitio](add-languages-to-site.md)

[Agregar secuencia de comandos a páginas del sitio para admitir telemetría](add-telemetry.md)
