---
title: Función VALUEINLARGE ER
description: Este tema proporciona información general sobre cómo usar la función VALUEINLARGE de informes electrónicos (ER).
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 26a7148a4caa80a191688145bac625bdf0bf83b2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686915"
---
# <a name="valueinlarge-er-function"></a>Función VALUEINLARGE ER

[!include [banner](../includes/banner.md)]

La función `VALUEINLARGE` determina si la entrada especificada del tipo *Int64* o *Entero* coincide con algún valor de un elemento específico de la lista especificada. La función devuelve un valor *booleano* de **VERDADERO** si la entrada especificada coincide con el resultado de ejecutar la expresión especificada para al menos un registro de la lista especificada. De lo contrario, la expresión devuelve un valor *Booleano* de **FALSE**. Para entender la diferencia con la función `VALUEIN`, consulte la sección [Nota de uso](#usage_note) posterior de este tema.

## <a name="syntax"></a>Sintaxis

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumentos

`input`: *Campo*

La ruta válida de un elemento de origen de datos del tipo *Lista de registros*. El valor de este elemento se conciliará.

`list`: *Lista de registros*

La ruta válida de un origen de datos del tipo de datos *Lista de registros*.

`list item expression`: *Expresión*

Un expresión condicional válida que señala o contiene un único campo de la lista especificada que se debe usar para la asignación.

## <a name="return-values"></a>Valores de retorno

*Booleano*

El valor *Booleano* resultante.

## <a name=""></a><a name="usage_note">Notas de uso</a>

Cuando la entrada especificada representa un tipo *Int64* o *Entero* de un elemento de origen de datos, cuya llamada se puede traducir a una declaración SQL directa, la lista especificada se convierte en una tabla SQL temporal y la coincidencia se realiza en la base de datos mediante la ejecución de una única consulta `EXISTS JOIN`. De lo contrario, esta función actúa como la función [`VALUEIN`](er-functions-logical-valuein.md).

Cuando la entrada especificada representa un elemento de origen de datos diseñado como un elemento distinto del tipo *Int64* y *Entero*, se produce un error en el momento del diseño, informándole que la función `VALUEINLARGE` no es aplicable para la expresión ER configurada.

Cuando la expresión de función `VALUEINLARGE` se ejecuta y se usa más de una tabla temporal en el ámbito de esta ejecución, se produce un error de tiempo de ejecución.

## <a name="example"></a>Ejemplo

Defina los siguientes orígenes de datos en la asignación de su modelo:

- El origen de datos **En** del tipo *Registros de la tabla*.
    - Este origen de datos se refiere a la tabla **Intrastat**.
    - La opción **Entre empresas** está configurada en **No**.
- El origen de datos **InMemory** del tipo *Campo calculado*.
    - Este origen de datos contiene la expresión `WHERE (In, In.Port <> "")`.
- El origen de datos **InFiltered** del tipo *Campo calculado*.
    - Este origen de datos contiene la expresión `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Cuando el origen de datos **InFiltered** se llama en el contexto de la empresa **DEMF**, se crea una nueva tabla temporal en la base de datos de la aplicación, la lista de códigos de identificación de registros recopilada en la memoria se inserta en esta tabla y se genera la siguiente declaración SQL para devolver los registros filtrados de la tabla **Intrastat**.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Recursos adicionales

[Funciones lógicas](er-functions-category-logical.md)

[Funciones VALUEIN](er-functions-logical-valuein.md)
