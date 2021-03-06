---
title: Enviar facturas al sistema de flujo de trabajo y conciliar líneas de recepción de productos (versión preliminar)
description: Este tema explica el proceso de enviar facturas de proveedores al sistema de flujo de trabajo y hacer coincidir automáticamente las líneas de recepción de productos registradas con las facturas de proveedores.
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cde164ee89b542d769d81d8d483049fb7ca001c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447447"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines-preview"></a>Enviar facturas al sistema de flujo de trabajo y conciliar líneas de recepción de productos (versión preliminar)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Este tema explica el proceso de enviar facturas de proveedores al sistema de flujo de trabajo y hacer coincidir automáticamente las líneas de recepción de productos registradas con las facturas de proveedores.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Enviar facturas de proveedores importadas al sistema de flujo de trabajo y hacer coincidir las líneas de recepción de productos registradas con las líneas de facturas de proveedores pendientes

Como parte de un proceso de facturación de Cuentas por pagar sin contacto, puede hacer que el sistema envíe automáticamente una factura importada al sistema de flujo de trabajo. Puede configurar el proceso de envío de facturas importadas al sistema de flujo de trabajo en la pestaña **Automatización de facturas de proveedores** de la página **Parámetros de cuentas por pagar** (**Cuentas por pagar \> Preparar \> Parámetros de cuentas por pagar**). El proceso de envío al flujo de trabajo se ejecutará en segundo plano, con la frecuencia que especifique (ya sea por hora o por día).

Cuando envía facturas automáticamente al sistema de flujo de trabajo, debe comenzar con una factura importada. Para asegurarse de que la factura se pueda procesar de principio a fin sin intervención manual, debe incluir una tarea de registro automatizado en la configuración del flujo de trabajo. Las facturas relacionadas con las órdenes de compra (PO) y las facturas que contienen una categoría de aprovisionamiento sin orden de compra y líneas no almacenadas se pueden enviar automáticamente al sistema de flujo de trabajo. Las facturas que se ingresan manualmente deben enviarse manualmente al sistema de flujo de trabajo.

El valor **Presentado por** en el flujo de trabajo es el ID de usuario que se ingresó para la tarea en segundo plano **Enviar las facturas del proveedor al flujo de trabajo** en la página **Automatización de procesos**. El usuario que tenga esa identificación de usuario podrá recuperar la factura del sistema de flujo de trabajo según sea necesario.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Hacer coincidir los recibos de productos registrados con las líneas de factura que tienen una política de coincidencia de tres vías

Como parte de un proceso de facturación de Cuentas por pagar sin contacto, el sistema puede hacer coincidir automáticamente los recibos de productos registrados con las líneas de facturación. Se debe definir una política de coincidencia de tres vías para esta tarea. Esta función está disponible si la función **Automatización de facturas de proveedores** se ha habilitado en la página **Gestión de funciones**.

El proceso se ejecutará hasta que la cantidad recibida del producto coincidente sea igual a la cantidad de la factura. Como parte de este proceso, puede especificar el número máximo de veces que el sistema debe intentar hacer coincidir los recibos de productos con una línea de factura antes de concluir que el proceso falló. El proceso se ejecutará en segundo plano, ya sea cada hora o diariamente. Puede ejecutar el proceso de comparación automatizado como parte del proceso para enviar facturas al sistema de flujo de trabajo. Alternativamente, puede ejecutarlo como un proceso independiente. Los ajustes del proceso match-product-receipts-to-invoice-lines se configuran en la pestaña **Automatización de facturas de proveedores** de la página **Parámetros de cuentas por pagar** (**Cuentas por pagar \> Preparar \> Parámetros de cuentas por pagar**).

Las líneas de factura que tienen una política de coincidencia de tres vías, donde la cantidad de recibo coincidente es menor que la cantidad de la factura, se incluirán en el proceso automatizado de coincidencia de recepción de producto.

Para ver el estado de la **última conciliación** de facturas que no forman parte del proceso automatizado de envío al flujo de trabajo, abra la factura en la página **Facturas de proveedores**. Cuando ve la factura, se actualiza la información de validación coincidente.

Una línea de factura se excluirá del procesamiento automatizado si se cumple alguna de las siguientes condiciones:

- El valor **Estado de coincidencia de recibo automatizado** de la línea de la factura es **Error**.
- Se está utilizando la factura.
- La factura está en el sistema de flujo de trabajo.
