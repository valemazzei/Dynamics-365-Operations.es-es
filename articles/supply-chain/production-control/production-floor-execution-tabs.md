---
title: Diseñar la interfaz de ejecución de la planta de producción
description: Este tema describe cómo diseñar el contenido de la interfaz de usuario para cada configuración.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664281"
---
# <a name="design-the-production-floor-execution-interface"></a>Diseñar la interfaz de ejecución de la planta de producción

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Puede diseñar el contenido de la interfaz de usuario para cada configuración utilizada por la interfaz de ejecución de la planta de producción. Por ejemplo, es posible que los trabajadores de una celda de trabajo necesiten poder abrir las instrucciones de trabajo en el piso de producción, mientras que en otra celda de trabajo, las instrucciones no son necesarias. En ese caso, se deben crear dos configuraciones, una con un botón para abrir documentos adjuntos y otra sin este botón.

## <a name="design-a-tab"></a>Diseñar una pestaña

En la página **Configurar la ejecución del piso de producción**, puede crear y configurar pestañas seleccionando **Fichas de diseño** en el Panel de acciones.

Cada pestaña está dividida en cuatro secciones, como se muestra en la siguiente ilustración.

![Diseño de pestaña](media/pfe-tab-layout.png "Diseño de pestaña")

Los siguientes elementos se muestran en la ilustración:

1. Barra de herramientas principal
1. Barra de herramientas secundaria
1. Vista principal
1. Vista detallada

Para crear y configurar una nueva pestaña, siga estos pasos:

1. Vaya a **Control de producción &gt; Ejecución de fabricación &gt; Dispositivo de tarjetas de trabajo**.

1. Seleccione **Fichas de diseño** en el Panel de acciones para abrir la página **Fichas de diseño**.

    ![Página de fichas de diseño](media/pfe-design-tabs.png "Página de fichas de diseño")

1. En el panel Acciones, seleccione **Nuevo**.

1. Realice los siguientes ajustes en el encabezado de la página:

    - **Nombre de la pestaña** - Especifique un nombre para la pestaña.
    - **Vista principal** - Seleccione entre las dos listas de trabajos predefinidas (*Trabajos activos* o *Todos los trabajos*).
    - **Vista de detalles** - Seleccione entre un valor en blanco o **Detalles del trabajo**. Si selecciona el valor en blanco, no habrá una vista detallada en la pestaña. Si selecciona **Detalles del trabajo**, la vista detallada contendrá una descripción detallada del trabajo seleccionado en la lista de trabajos en la vista principal.

1. En la sección **Barra de herramientas principal**, elija qué botones deben estar disponibles en la barra de herramientas principal. La columna **Acciones disponibles** muestra una lista de todos los botones que se pueden agregar. Las columnas **Acciones seleccionadas** muestran una lista de todos los botones que están incluidos en la configuración actual. Utilice los botones entre las columnas para mover los elementos seleccionados entre las columnas según sea necesario. Utilice los botones arriba y abajo junto a la columna **Acciones seleccionadas** para controlar el orden en que se presentan los botones en la interfaz de usuario.

1. En la sección **Barra de herramientas** **secundaria**, elija qué botones deben estar disponibles en la barra de herramientas secundaria. La columna **Acciones disponibles** muestra una lista de todos los botones que se pueden agregar. Las columnas **Acciones seleccionadas** muestran una lista de todos los botones que están incluidos en la configuración actual. Utilice los botones entre las columnas para mover los elementos seleccionados entre las columnas según sea necesario. Utilice los botones arriba y abajo junto a la columna **Acciones seleccionadas** para controlar el orden en que se presentan los botones en la interfaz de usuario.

## <a name="associate-a-tab-with-a-configuration"></a>Asociar una pestaña a una configuración

Una vez que haya diseñado todas las pestañas que necesita, puede asociarlas con una configuración.

1. Vaya a **Control de producción &gt; Configuración &gt; Configurar ejecución de planta de producción**.

    ![Configurar la ejecución de planta de producción](media/pfe-config-prod-floor-execution.png "Configurar la ejecución de planta de producción")

1. En la ficha desplegable **Selección de ficha**, seleccione **Agregar**.

1. Se agrega una nueva fila a la cuadrícula. Para esta nueva fila, seleccione el nombre de una pestaña que desea agregar a la configuración.

1. Continúe agregando pestañas adicionales según sea necesario.

1. Utilice los botones **Subir** y **Bajar** de la barra de herramientas para organizar las pestañas según sea necesario. Las pestañas se mostrarán de izquierda a derecha en el orden que se muestra en la captura de pantalla anterior (la pestaña en la parte superior se muestra a la izquierda).
