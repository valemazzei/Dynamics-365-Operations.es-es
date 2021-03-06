---
title: Corrección de información de seguimiento de inventario
description: Este procedimiento le muestra el proceso de crear y registrar un diario de transferencia de inventario para corregir la información de seguimiento de inventario.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4437121"
---
# <a name="correct-inventory-tracking-information"></a>Corrección de información de seguimiento de inventario

[!include [banner](../../includes/banner.md)]

Este procedimiento le muestra el proceso de crear y registrar un diario de transferencia de inventario para corregir la información de seguimiento de inventario. En este ejemplo, actualizaremos la información de un artículo controlado por lote cambiando un lote registrado incorrectamente por otro lote. Puede revisar este procedimiento con los datos de prueba de la empresa USPI o utilizar sus propios datos. Si utiliza sus propios datos, debe tener un artículo habilitado para lotes y no debe estar controlado por ubicación. También necesita tener configurado un nombre de diario de inventario para las transferencias de inventario. Estas tareas las realizará normalmente el empleado del almacén.


## <a name="create-an-inventory-transfer-journal"></a>Creación de un diario de transferencias de inventario
1. Vaya a Transferir.
2. Haga clic en Nuevo.
3. En el campo Nombre, especifique o seleccione un valor.
4. Haga clic en Aceptar

## <a name="create-journal-lines"></a>Creación de líneas de diario
1. Haga clic en Nuevo.
2. En el campo Número de artículo, especifique o seleccione un valor.
    * Si utiliza USPI, seleccione el artículo M5003.  
3. En el campo Cantidad, especifique un número.
4. Haga clic en la ficha Dimensiones de inventario.
5. En el campo Número de lote, especifique o seleccione un valor.
6. En el campo Sitio, especifique o seleccione un valor.
7. En el campo Almacén, especifique o seleccione un valor.
8. En el campo Número de lote, especifique o seleccione un valor.

## <a name="post-the-journal"></a>Registrar el diario
1. Haga clic en Registrar.
2. Haga clic en Aceptar

## <a name="check-tracing-information"></a>Comprobar la información de seguimiento
1. Haga clic en Inventario.
2. Haga clic en Seguimiento.
3. Haga clic en Aceptar
    * Con esta información de seguimiento puede rastrear desde qué lote corrigió el inventario.  También puede usar la página Seguimiento de artículos para ver esta información.  
4. Cierre la página.

## <a name="check-inventory-transactions"></a>Comprobar las transacciones del inventario
1. Haga clic en Inventario.
2. Haga clic en Transacciones.
    * Aquí puede ver las transacciones creadas al registrar el diario.   

