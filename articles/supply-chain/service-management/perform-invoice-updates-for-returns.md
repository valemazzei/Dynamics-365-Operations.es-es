---
title: Actualizaciones de facturas para devoluciones
description: Esta funcionalidad también admite los procesos empresariales de muchas organizaciones que deciden que la misma persona facture pedidos de devolución y de ventas a la vez.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d60e29aec1ebdec939aaafc978ee4de04b96136
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436621"
---
# <a name="perform-invoice-updates-for-returns"></a>Actualizaciones de facturas para devoluciones 

[!include [banner](../includes/banner.md)]


Un pedido de devolución es un tipo de pedido de ventas marcado como artículo devuelto. Por lo tanto, la página de lista **Todos los pedidos de venta** se usa para generar facturas para los pedidos de devolución en lugar del formulario **Pedidos de devolución**. Esta funcionalidad también admite los procesos empresariales de muchas organizaciones que deciden que la misma persona facture pedidos de devolución y de ventas a la vez.

Dado que la factura para un artículo devuelto es para un importe negativo, se denomina nota de abono.

Al configurar la actualización de factura para el procesamiento por lotes, el pedido de ventas del tipo **Pedido devuelto** debe tener un estado de línea de devolución de **Recibido**, lo que indica que el albarán del pedido se ha actualizado.

## <a name="post-an-invoice-for-a-return-order"></a>Registrar una factura para un pedido de devolución

1.  Haga clic en **Clientes** \> **Común** \> **Pedidos de ventas** \> **Todos los pedidos de ventas**.

2.  Seleccione un pedido de ventas para el que se muestra **Pedido devuelto** en el campo **Tipo de pedido**.

3.  En el panel de acciones, en la ficha **Factura**, en el grupo **Generar**, haga clic en **Factura**.

4.  En la pestaña **Parámetros**, seleccione la casilla de verificación **Registrar**.

5.  Revise la información del formulario y realice los cambios pertinentes.

6.  Haga clic en **Aceptar**. La nota de abono se ha registrado.

## <a name="see-also"></a>Consulte también

[Actualizaciones de albaranes para devoluciones](packing-slip-updates-returns.md)

  


