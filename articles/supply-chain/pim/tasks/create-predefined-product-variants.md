---
title: Crear variantes de productos predefinidas
description: Este procedimiento le guía por la creación de variantes de productos para un producto maestro mediante las combinaciones de dimensiones de productos.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fa9c6d4862a49bbf0b5ecbb8c0c3d573e0f49e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436853"
---
# <a name="create-predefined-product-variants"></a>Crear variantes de productos predefinidas

[!include [banner](../../includes/banner.md)]

Este procedimiento le guía por la creación de variantes de productos para un producto maestro mediante las combinaciones de dimensiones de productos. La empresa de demostración utilizada para crear este procedimiento es USMF.


## <a name="create-a-product-master"></a>Crear un producto maestro
1. Vaya a Gestión de información de productos > Productos > Productos maestros.
2. Haga clic en Nuevo.
3. En el campo Número de producto, escriba un valor.
    * Especificar un número de producto manualmente solo es obligatorio si no se ha establecido ninguna secuencia numérica para el campo del número de producto. En otras palabras, omita el paso si se ha establecido la secuencia numérica para el campo.  
4. En el campo Nombre de producto, escriba un valor.
5. En el campo Grupo de dimensiones de producto, especifique o seleccione un valor.
    * Seleccione el grupo de dimensiones de producto SizeCol (tamaño y color).  
6. Haga clic en Aceptar

## <a name="add-product-dimensions"></a>Agregar dimensiones de productos
1. Haga clic en Dimensiones de producto.
    * Este ejemplo muestra cómo especificar manualmente dimensiones de producto. También puede elegir seleccionar un grupo de tamaños, colores o estilos que incluya los valores de dimensiones de productos que desea usar.  
2. Haga clic en Nuevo.
3. En la lista, marque la fila seleccionada.
4. En el campo Tamaño, especifique o seleccione un valor.
5. En el campo Nombre, escriba un valor.
6. Haga clic en Nuevo.
7. En la lista, marque la fila seleccionada.
8. En el campo Tamaño, especifique o seleccione un valor.
9. En el campo Nombre, escriba un valor.
10. Haga clic en la ficha Colores.
11. Haga clic en Nuevo.
12. En la lista, marque la fila seleccionada.
13. En el campo Color, especifique o seleccione un valor.
14. En el campo Nombre, escriba un valor.
15. Haga clic en Nuevo.
16. En la lista, marque la fila seleccionada.
17. En el campo Color, especifique o seleccione un valor.
18. En el campo Nombre, escriba un valor.
19. Haga clic en Guardar.
20. Cierre la página.

## <a name="generate-product-variants"></a>Generar variantes de productos
1. Haga clic en Variantes del producto.
2. Haga clic en Sugerencias de variantes.
3. Haga clic en Seleccionar todo.
    * En este ejemplo, se seleccionan todas las variantes posibles. Si solo se usará un subconjunto de las combinaciones de dimensiones de productos posibles para crear variantes, puede seleccionar las entradas individuales.  
4. Haga clic en Crear.
    * Puede generar descripciones para todas sus variantes en función de la combinación de los valores de dimensiones de productos. Las descripciones son opcionales.  
5. Haga clic en Guardar.

