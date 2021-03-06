---
title: Crear un estado de ciclo de vida del producto para excluir productos de planificación maestra
description: Este procedimiento muestra cómo crear un estado de ciclo de vida de producto nuevo que excluya los productos de cálculo de la planificación maestra y de nivel L. MAT.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9573fd220cd8b6a58f81e4d17ca65234f41beb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436712"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Crear un estado de ciclo de vida del producto para excluir productos de planificación maestra

[!include [banner](../../includes/banner.md)]

Este procedimiento muestra cómo crear un estado de ciclo de vida de producto nuevo que excluya los productos de cálculo de la planificación maestra y de nivel L. MAT.


## <a name="create-an-obsolete-state"></a>Crear un estado obsoleto
1. Vaya a Gestión de información de productos > Configuración > Estado de ciclo de vida de producto.
2. Haga clic en Nuevo.
3. En el campo Estado, escriba un valor.
4. Seleccione No en el campo Es activo para planificación.
5. En el campo Descripción, escriba un valor.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Asociar el estado obsoleto a un producto emitido
1. Cierre la página.
2. Vaya a Gestión de información de productos > Productos > Productos emitidos.
3. Use el filtro rápido para buscar registros. Por ejemplo, filtre el campo Nombre de búsqueda con el valor "M00".
4. Haga clic en Editar.
5. En la lista, marque la fila seleccionada.
6. En el campo Estado de ciclo de vida de producto, especifique o seleccione un valor.

