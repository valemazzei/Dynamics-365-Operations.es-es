---
title: Crear acuerdos de servicios
description: Este tema describe cómo utilizar funciones en los módulos Gestión de servicio y Gestión de proyectos y contabilidad para crear contratos de servicio.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a1a47761869a4190eac6dc9e069a6b520bf7a1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4437043"
---
# <a name="create-service-agreements"></a>Crear acuerdos de servicios

[!include [banner](../includes/banner.md)]

Este tema describe cómo utilizar funciones en los módulos Gestión de servicio y Gestión de proyectos y contabilidad para crear contratos de servicio.

## <a name="create-a-service-agreement-from-service-management"></a>Crear un acuerdo de servicio a partir de la gestión de servicio

1. Vaya a **Gestión de servicio**.
2. Haga clic en **Contratos de servicio** para crear una nueva línea de contrato de servicio en el encabezado de la página. 
3. Haga clic en **Nuevo**. Introduzca una descripción, seleccione una referencia para un proyecto en el campo **Id. de proyecto** y rellene el resto de los campos y líneas del contrato de servicio. Haga clic en **Guardar**.
4. En la pestaña **Relaciones**, seleccione **Objetos de servicio** o **Tareas de servicio** para crear relaciones de objetos de servicio o relaciones de tareas de servicio para el contrato de servicio. Los objetos y las tareas de servicio para las que se crean relaciones pueden vincularse a las líneas del acuerdo de servicio.
5. En la mitad inferior de la página, puede crear las líneas del contrato de servicio copiando las líneas de una plantilla de servicio u otro acuerdo de servicio, o bien puede crear manualmente las líneas del acuerdo de servicio.

> [!NOTE]
> Si copia las líneas del contrato de servicio de otro contrato de servicio, puede indicar si desea copiar también las relaciones de objetos y tareas de servicio. Si copia estas relaciones, se añadirán a las relaciones existentes del acuerdo de servicio. Si copia las líneas del acuerdo de servicio de una plantilla de servicio, se copiarán automáticamente las relaciones de objetos y tareas de servicio como las relaciones de objetos y tareas de servicio de las nuevas líneas del acuerdo de servicio.

## <a name="create-service-agreement-lines-manually"></a>Crear líneas de contrato de servicio manualmente

1. En la página **Contratos de servicio**, agregue una línea de contrato de servicio en la cuadrícula de líneas. 
2. Especifique la información adecuada para la línea del contrato de servicio. 
3. Presione **CTRL+S** para guardar la línea y cierre la página.

## <a name="create-a-service-agreement-from-project"></a>Crear un acuerdo de servicio a partir de Proyecto

1. Haga clic en **Gestión de proyectos y contabilidad**.
2. Haga clic en **Todos los proyectos**.
3. Seleccione el proyecto de la lista.
4. En el **Panel de acciones**, haga clic en **Gestionar**. En el grupo de acción **Nuevo**, haga clic en **Servicio** y seleccione **Contrato de servicio**.
5. Siga los pasos en la sección titulada **Crear un contrato de servicio** según lo descrito anteriormente en este tema para introducir la referencia del proyecto.


## <a name="related-topics"></a>Temas relacionados

[Visión general del desarrollo y establecimiento de acuerdos de servicio](service-agreements.md)


