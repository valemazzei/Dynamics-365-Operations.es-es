---
title: Configurar la visualización de lotes más antiguos del almacén en un dispositivo móvil
description: Este tema describe cómo configurar un dispositivo móvil para mostrar una lista de ubicaciones con lotes más antiguos que la ubicación actual de una línea de trabajo.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b1c9452a811d662976a25993264be0617ac67fe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436836"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Configurar la visualización de lotes más antiguos del almacén en un dispositivo móvil

[!include [banner](../includes/banner.md)]

La configuración **Visualización de lotes más antiguos del almacén** permite mostrar una lista de ubicaciones con lotes más antiguos que la ubicación actual de la línea del trabajo. La lista de ubicaciones que aparece incluye información sobre los lotes más antiguos de la ubicación con la fecha de vencimiento y el inventario físico de cada lote. Puede elegir seleccionar en una nueva ubicación o continuar seleccionando en la ubicación actual. 
- Selección en una nueva ubicación - si selecciona una nueva ubicación para elegir, la línea del trabajo actual se actualizará para usar la nueva ubicación y el trabajo continuará como de costumbre con la nueva ubicación. Para que la nueva ubicación sea válida, debe tener cantidad suficiente disponible para toda la línea de trabajo. Si la cantidad requerida no está disponible, la línea del trabajo no se actualizará, y la lista se mostrará. 
- Continuar seleccionando en la ubicación actual - si continúa con la ubicación de la línea del trabajo actual, las cantidades de la línea de trabajo se continuarán seleccionando en la ubicación original.

## <a name="where-it-applies"></a>Dónde se aplica
Visualizar lotes más antiguos del almacén se configura en elementos de menú del dispositivo móvil y afecta a la selección de artículos del lote siguiente.

## <a name="set-up-display-older-batches-within-warehouse"></a>Configuración de la visualización de lotes más antiguos del almacén
La configuración de **Visualización de lotes más antiguos del almacén** está disponible en elementos de menú del dispositivo móvil cuando la opción **Seleccionar lote más antiguo** se establece en **Advertir**.

- En **Gestión de almacenes** > **Configuración** > **Dispositivo móvil** > **Elementos de menú del dispositivo móvil**, establezca **Usar trabajo existente** en **Sí** para el elemento de menú, y seleccione **Advertir** en el campo **Seleccionar lote más antiguo**. 

