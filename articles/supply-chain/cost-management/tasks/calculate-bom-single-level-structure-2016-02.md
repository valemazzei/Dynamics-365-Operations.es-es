---
title: Calcular un L.MAT mediante una estructura de un solo nivel (febrero de 2016)
description: Este procedimiento muestra cómo calcular el coste de un producto terminado mediante la expansión de un único nivel que se basa en la hoja de Gestión de costes.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83a62966e343a9b1c073c2d6ec1c1b69b1daddbb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436931"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Calcular un L.MAT mediante una estructura de un solo nivel (febrero de 2016)

[!include [banner](../../includes/banner.md)]

Este procedimiento muestra cómo calcular el coste de un producto terminado mediante la expansión de un único nivel que se basa en la hoja de Gestión de costes. Es la sexta tarea en las series de cálculo BOM. La empresa de datos de prueba utilizada para crear esta tarea es USMF.

1. Vaya a Productos emitidos.
2. En la lista, busque y seleccione el registro deseado.
    * Seleccione el producto BOM_1  
3. En el panel de acciones, haga clic en Gestionar costes.
4. Haga clic en Precio de artículo.
5. Haga clic en Calcular coste del artículo.
    * Es posible que tenga que hacer la elipsis (...) para ver esta opción en el menú superior.  
6. En el campo Versión de la gestión de costes, haga clic en el botón desplegable para abrir la búsqueda.
    * Para esta demostración, seleccione 10. Esta es la misma versión de gestión de costes utilizada para agregar el precio de coste a los componentes.  
7. Haga clic en Aceptar
8. Haga clic en Ver detalles de cálculo.
    * Es posible que tenga que hacer la elipsis (...) para ver esta opción en el menú superior.    A continuación se indica la composición del coste:  *    10 se deriva de ITEM_A, 10 de ITEM_B, 10 de BOM_2. En este caso no hay detalles para BOM_2, ya que se ha especificado como coste estándar de 10 pero no mediante el cálculo.  *    7 se deriva del tiempo de configuración, que es un coste constante, y el 7 adicional se deriva de la operación de tiempo de ejecución (Proceso).  *    También hay otros importes que corresponden a costes indirectos.  
9. @SysTaskRecorder: _RequestClose

