---
title: Crear reglas de configuración
description: Este procedimiento crea reglas de configuración que se pueden usar para que la configuración basada en dimensiones aplique o impida combinaciones de líneas de lista de materiales.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bc0af4d95e9430d0b5c8b7fc9a4ade076802044
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436857"
---
# <a name="create-configuration-rules"></a>Crear reglas de configuración

[!include [banner](../../includes/banner.md)]

Este procedimiento crea reglas de configuración que se pueden usar para que la configuración basada en dimensiones aplique o impida combinaciones de líneas de lista de materiales. La empresa de datos de prueba utilizada para crear este procedimiento es USMF. Este es el séptimo procedimiento de ocho que explica cómo crear combinaciones para la configuración basada en dimensiones.

1. Vaya a Gestión de información de productos > Listas de materiales y fórmulas > Listas de materiales.
2. En la lista, busque y seleccione el registro deseado.
    * Localice y seleccione la lista de materiales para la configuración basada en dimensiones.  
3. En el panel de acciones, haga clic en Opciones.
4. Haga clic en Cambiar vista.
5. Haga clic en Visualización de encabezado.
    * Abra la vista de encabezado para acceder a la ficha desplegable Ruta de configuración.  
6. Expanda o contraiga la sección Ruta de configuración.
    * La ficha desplegable Ruta de configuración debe estar en modo expandido.  
7. Haga clic en Reglas de configuración.
8. Haga clic en Nuevo.
9. En la lista, marque la fila seleccionada.
10. En el campo Código de artículo, haga clic en el botón desplegable para abrir la búsqueda.
    * Se muestran los elementos en el grupo de configuración actual. Seleccione el que representa la condición en la regla.  
11. En la lista, haga clic en el vínculo de la fila seleccionada.
12. En el campo Método, seleccione una opción.
    * Es posible hacer que se seleccione un elemento, o se anule su selección, de otro grupo de configuración.  
13. En el campo Grupo derivado, haga clic en el botón desplegable para abrir la búsqueda.
14. En la lista, busque y seleccione el registro deseado.
15. En la lista, haga clic en el vínculo de la fila seleccionada.
    * Seleccione el grupo de configuración que le interese.  
16. En el campo Código de artículo derivado, haga clic en el botón desplegable para abrir la búsqueda.
17. En la lista, haga clic en el vínculo de la fila seleccionada.
    * Seleccione el número de elemento que se seleccionará o dejará de seleccionarse, según el método elegido.  
18. Cierre la página.

