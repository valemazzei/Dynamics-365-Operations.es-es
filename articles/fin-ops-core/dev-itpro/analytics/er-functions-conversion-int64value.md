---
title: Función INT64VALUE ER
description: Este tema proporciona información general sobre cómo usar la función INT64VALUE de informes electrónicos (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686060"
---
# <a name="int64value-er-function"></a>Función INT64VALUE ER

[!include [banner](../includes/banner.md)]

La función `INT64VALUE` devuelve un valor *Int64* que representa la cadena especificada.

## <a name="syntax-1"></a>Sintaxis 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Sintaxis 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumentos

`text`: *Cadena*

Un valor de texto que debe convertirse en un número *Int64*.

`number`: *Real* o *Entero*

Un valor numérico *Real* o *Entero* que debe convertirse en un número *Int64*.

## <a name="return-values"></a>Valores de retorno

*Int64*

El valor numérico resultante.

## <a name="usage-notes"></a>Notas de uso

Se trunca cualquier posición decimal.

## <a name="example-1"></a>Ejemplo 1

`INT64VALUE ("22565422744")` devuelve el valor *Int64* **22565422744**.

## <a name="example-2"></a>Ejemplo 2

`INT64VALUE ( VALUE("22565422744.77"))` devuelve el valor *Int64* **22565422744**.

## <a name="additional-resources"></a>Recursos adicionales

[Funciones de conversión de tipos](er-functions-category-type-conversion.md)
