---
title: Función REVERSE de ER
description: Este tema proporciona información general sobre cómo usar la función REVERSE de informes electrónicos (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917244"
---
# <a name="REVERSE">Función REVERSE de ER</a>

[!include [banner](../includes/banner.md)]

La función `REVERSE` devuelve la lista especificada como un valor *Lista de registros* en orden inverso.

## <a name="syntax"></a>Sintaxis

```
REVERSE (list)
```

## <a name="arguments"></a>Argumentos

`list`: *Lista de registros*

La ruta válida de un origen de datos del tipo de datos *Lista de registros*.

## <a name="return-values"></a>Valores de retorno

*Lista de registros*

La lista de registros resultante.

## <a name="example-1"></a>Ejemplo 1

Si especifica el origen de datos **DS** del tipo *Campo calculado* y contiene la expresión `SPLIT ("C|B|A", "|")`, la expresión `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` devuelve el valor de texto **"C"**.

## <a name="example-2"></a>Ejemplo 2

Cuando **Proveedor** se configura como origen de datos de ER que hace referencia a la tabla VendTable, la expresión `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` devuelva la lista de proveedores que se clasifica por nombre en orden descendente.

## <a name="additional-resources"></a>Recursos adicionales

[Funciones de lista](er-functions-category-list.md)