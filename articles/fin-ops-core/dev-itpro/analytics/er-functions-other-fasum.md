---
title: Función FA_SUM de ER
description: Este tema proporciona información general sobre cómo usar la función FA_SUM de informes electrónicos (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 32eb07689598a3b6c852f272b480106670b88cd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916991"
---
# <a name="FA_SUM">Función FA_SUM de ER</a>

[!include [banner](../includes/banner.md)]

La función `FA_SUM` devuelve un valor *Contenedor (registro)* que consiste en datos para las cantidades del activo fijo para el elemento del activo fijo especificado, el código del modelo de valor y un período de fechas.

## <a name="syntax"></a>Sintaxis

```
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumentos

`fixed asset code`: *Cadena*

Un valor *Cadena* que representa el código de un elemento de activo fijo para el que se calcula el saldo.

`value model code`: *Cadena*

Un valor *Cadena* que representa el código de un modelo de valor para el que se calcula el saldo.

`start date`: *Fecha*

Un valor *Fecha* que representa la fecha de inicio de un período para el que se calculan los importes de los activos fijos.

`end date`: *Fecha*

Un valor *Fecha* que representa la fecha final de un período para el que se calculan los importes de los activos fijos.

## <a name="return-values"></a>Valores de retorno

*Contenedor (registro)*

El valor de registro resultante.

## <a name="example"></a>Ejemplo

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` devuelve el contenedor de datos para activos fijos **COMP-000001** que se ha preparado para el modelo de valor **Actual** y por un período desde **Fecha1** a **Fecha2**.

## <a name="additional-resources"></a>Recursos adicionales

[Otras funciones (específicas de dominio empresarial)](er-functions-category-other.md)