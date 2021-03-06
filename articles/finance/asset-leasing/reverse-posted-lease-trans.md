---
title: Revertir transacciones de arrendamiento contabilizadas
description: Este tema explica cómo revertir una transacción de arrendamiento contabilizada. Cualquier transacción que se cree mediante Arrendamiento de activos se puede revertir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 259fd8f41eade1e873225f0d95c499c8cb8c1a6a
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4447805"
---
# <a name="reverse-posted-lease-transactions"></a>Revertir transacciones de arrendamiento contabilizadas

[!include [banner](../includes/banner.md)]

Cualquier transacción que se cree mediante Arrendamiento de activos se puede revertir. Las transacciones que se revierten mediante Arrendamiento de activos actualizan sus datos de arrendamiento. Por lo tanto, también actualizan los valores en libros del pasivo por arrendamiento y el activo por derecho de uso (ROU).

Para crear una transacción de reversión para un arrendamiento, siga estos pasos.

1. En la página **Transacciones de activos** o en la página **Transacciones de pasivo**, seleccione la transacción y luego seleccione **Revertir transacción**.
2. En el cuadro de diálogo que aparece, puede editar la fecha en la que se publicará la entrada inversa. Por defecto, el campo **Fecha** se establece en la fecha de registro de la transacción que seleccionó. La entrada de reversión no se puede publicar antes de la fecha de registro original de la transacción seleccionada.
3. Seleccione **Aceptar**. Se publica un movimiento de diario que invierte la entrada que seleccionó. La inversión se muestra en la página **Transacciones de activos** o **Transacciones de pasivo**, y se actualiza el total neto del saldo actual que se muestra en la página.

Cuando selecciona **Seguimiento inverso**, aparece un cuadro de diálogo que muestra tanto las transacciones originales como las transacciones revertidas, junto con un número vinculado que se conoce como *número de seguimiento*. Para que las reversiones sean más fáciles de entender y mejorar la visibilidad, también puede realizar un seguimiento de las reversiones mediante las programaciones de arrendamiento.

El campo **Último número de diario** de la página **Programación** muestra los números de diario de las transacciones. Cuando se invierte una transacción, este campo se actualiza con el número de diario de una transacción de reversión. Además, la casilla **Invertido** está seleccionada para indicar que la transacción se ha invertido y el campo **Registrado** está seleccionado.

## <a name="revoke-a-reversed-transaction"></a>Revocar una transacción revertida

Para revocar una transacción revertida, siga estos pasos.

1. En la página **Programación** o **Transacciones**, seleccione la transacción original.
2. Siga uno de estos pasos:

    - Si seleccionó la transacción en la página **Programación**, siga los pasos para crear un diario en [Crear movimientos de diario mensuales en un lote](create-monthly-journals-batch.md). Debe registrar manualmente el diario.
    - Si seleccionó la transacción en la página **Transacciones**, seleccione **Transacción inversa**. Recibirá un mensaje que indica que esta revocación es una revocación de una revocación anterior y que puede editar la fecha de registro de esta revocación. Sin embargo, las validaciones comerciales generales afectan las fechas que se pueden introducir en el campo **Fecha**. 

3. Seleccione **Aceptar**. Se publica un movimiento de diario que invierte la entrada que seleccionó. La inversión se muestra en la página **Transacciones**, y el saldo actual neto total se restaura a lo que era antes de la primera reversión. Por tanto, se niega el impacto que tuvo la reversión en los saldos.

Cuando selecciona **Seguimiento de reversiones**, aparece un cuadro de diálogo que muestra tanto las transacciones originales como las transacciones revertidas, junto con un número de seguimiento vinculado.

También puede realizar un seguimiento de las revocaciones mediante el uso de la página **Programaciones**. El campo **Revertir** se borra, mientras que el campo **Diario registrado** se selecciona. Además, el campo **Último número de diario** se actualiza con el número de diario de la transacción de revocación y el campo **Número de diario** se actualiza con el número de diario de reversión.
