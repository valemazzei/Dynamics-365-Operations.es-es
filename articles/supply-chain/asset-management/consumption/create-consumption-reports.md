---
title: Crear informes de consumo
description: En este tema se explica cómo crear informes de consumo en Administración de activos.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d28acbccc35b3f59f9cca7236dd721a1d9bdead8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436969"
---
# <a name="create-consumption-reports"></a>Crear informes de consumo

[!include [banner](../../includes/banner.md)]

 

Cuando haya creado y publicado registros de consumo en órdenes de trabajo en Administración de activos, estarán dos informes disponibles para mostrar los detalles de consumo.


## <a name="asset-consumption-report"></a>Informe de consumo de activos

Cuando haya registrado el consumo en las órdenes de trabajo, podrá imprimir un informe de consumo de activos. El informe muestra las horas, los costes por hora, los costes de artículo y los gastos registrados en los activos.

1. Haga clic en **Administración de activos** > **Informes** > **Activos** > **Consumo de activos**.

2. En el cuadro de diálogo **Consumo de activos**, seleccione los parámetros y el nivel de detalle que desea ver seleccionando **Sí** en los botones de alternar relevantes e insertando un nivel de ubicación técnica en la sección **Mostrar**.
    - Puede usar el campo **Niveles** para indicar el nivel de detalle que desea para las líneas de activos con respecto a las ubicaciones técnicas. 
    
        Por ejemplo, si introduce el número "1 "en el campo, y tiene una estructura de ubicación técnica de varios niveles, todos los activos para una ubicación técnica se mostrarán en el nivel superior, y por tanto, se puede agregar una línea desde las ubicaciones técnicas ubicadas en un nivel inferior. 
        
        Si introduce el número "0 "en el campo **Niveles** , verá un resultado detallado que muestra todos los activos en todos los niveles de la ubicación técnica con el que están relacionados. 
        
    - Seleccione **Sí** en el botón de alternar **Sumar en todos los activos secundarios** para ver las sumas para cada activo secundario en el informe.

3. Seleccione un intervalo de fechas en la sección **Fechas**.

4. En la ficha desplegable **Destino**, seleccione si desea visualizar el informe en la pantalla, imprímalo o guárdelo como archivo o correo electrónico.

5. Si es necesario, puede seleccionar activos específicos que se mostrarán en el informe. En la ficha desplegable **Registros que incluir**, haga clic en **Filtrar** y agregue los activos que desea incluir en el informe.

6. Haga clic en **Aceptar** para generar el informe.


## <a name="work-order-consumption-report"></a>Informe de consumo de orden de trabajo

Cuando haya registrado el consumo en las órdenes de trabajo, podrá imprimir un informe de consumo de orden de trabajo. El informe muestra las horas, los costes por hora, los costes de artículo y los gastos registrados en las órdenes de trabajo.

1. Haga clic en **Administración de activos** > **Informes** > **Órdenes de trabajo** > **Consumo de órdenes de trabajo**.

2. En el cuadro de diálogo **Consumo de órdenes de trabajo**, seleccione los parámetros que desea incluir en el informe seleccionando **Sí** en los botones de alternar relevantes en la sección **Mostrar**.

3. Seleccione un intervalo de fechas en la sección **Fechas**.

4. En la ficha desplegable **Destino**, seleccione si desea visualizar el informe en la pantalla, imprímalo o guárdelo como archivo o correo electrónico.

5. Si es necesario, puede seleccionar órdenes de trabajo específicas que se mostrarán en el informe. En la ficha desplegable **Registros que incluir**, haga clic en **Filtrar** y agregue las órdenes de trabajo que desea incluir en el informe.

6. Haga clic en **Aceptar** para generar el informe.


>[!NOTE]
>También puede generar un [informe de órdenes de trabajo](../work-orders/work-order-report.md), que contiene más detalles sobre la orden de trabajo.

