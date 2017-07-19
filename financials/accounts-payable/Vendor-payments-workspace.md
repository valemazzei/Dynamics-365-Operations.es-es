---
title: Espacio de trabajo de pagos de proveedor
description: "Este tema proporciona información acerca del espacio de trabajo Pagos a proveedores. El espacio de trabajo Pagos a proveedores muestra la información relacionada con el procesamiento de pagos a proveedores."
author: twheeloc
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: 4011a2383fe4556b730fa0b6353ba0b9773a4eec
ms.contentlocale: es-es
ms.lasthandoff: 06/14/2017

---

# <a name="vendor-payments-workspace"></a>Espacio de trabajo de pagos de proveedor

[!include[banner](../includes/banner.md)]

El espacio de trabajo **Pagos a proveedores** muestra la información relacionada con el procesamiento de pagos a proveedores. Este espacio de trabajo incluye un vista **Mi trabajo** y una página **Análisis** . La vista **Mi trabajo** muestra mosaicos de resumen, cuadrículas de transacciones con proveedores y la información de proveedor relacionada. La página **Análisis** utiliza las capacidades de Microsoft Power BI para mostrar las representaciones visuales relacionados con pagos a proveedores.

## <a name="my-work-view"></a>Vista Mi trabajo

### <a name="summary-tiles"></a>Iconos de resumen

Los mosaicos en la sección **Resumen** ofrece una visión general del estado de la información de pago. Puede ver los diarios de pagos que todavía no se han registrado, las facturas vencidas, todos los proveedores, y proveedores que están en espera. En la sección **Resumen** , puede crear un nuevo período de pago.

La información de la sección **Resumen** es para la empresa con la que tiene firmado un contrato.

### <a name="vendor-transactions-grids"></a>Cuadrículas de transacciones con proveedores

La sección **Transacciones de proveedor** contiene las cuadrículas que muestran las facturas vencidas y los pagos que no se hayan liquidado. En la cuadrícula **Factura vencidas** , puede ver el historial de liquidaciones de una factura seleccionada. En la cuadrícula **Pagos no liquidados** , puede ver el historial de liquidaciones de una factura seleccionada y liquidarla.

Los empleados de pagos centralizados pueden utilizar un filtro que aparece en la parte superior de cada cuadrícula para seleccionar una empresa. La cuadrícula se filtra a continuación de modo que muestre solo las empresas definidas en la jerarquía organizativa de pagos centralizada que el empleado de pagos centralizados tenga derecho a ver.

La ficha **Buscar transacciones** en la sección **Transacciones de proveedor** le permite buscar una transacción de proveedor.

### <a name="related-information"></a>Información relacionada

Puede ver el informe **Antigüedad de proveedores** y el informe **Resumen de pago por fecha** mediante los vínculos de la sección **Información relacionada** del espacio de trabajo.

## <a name="analytics-page"></a>Página Análisis

La página **Análisis** proporciona medidas importantes, como facturas de proveedor vencidas y facturas de proveedor que venzan en el futuro. Esta página contiene nueve páginas de informe. Una página ofrece una visión general, y las otras ocho proporcionan información detallada acerca de medidas de pago a proveedores.

En la tabla siguiente se muestran las visualizaciones que se encuentran disponibles en cada página de informe.

| Página de informes | Visualización |
|-------------|---------------|
| Visión general de pagos de proveedor | <ul><li>Facturas vencidas</li><li>Facturas que vencen hoy</li><li>Descuentos aplicados a descuentos perdidos</li><li>Facturas pendientes en el futuro por fecha de descuento por pronto pago</li><li>Facturas pendientes en el futuro por fecha de vencimiento</li><li>Facturas pagadas tarde a las facturas pagadas a tiempo</li><li>Asignación de flujo de trabajo de pagos</li><li>Saldo cliente/proveedor</li><li>Facturas abiertas con el pago en espera</li></ul> |
| Facturas vencidas | <ul><li>Facturas vencidas</li><li>Detalles sobre facturas vencidas</li><li>Total de facturas abiertas</li><li>Facturas vencidas por grupo de proveedores</li><li>Facturas vencidas por empresa</li></ul> |
| Facturas que vencen hoy | <ul><li>Facturas que vencen hoy</li><li>Detalles sobre facturas que vencen hoy</li><li>Facturas que vencen hoy por empresa</li><li>Facturas que vencen hoy por grupo de proveedores</li></ul> |
| Descuentos aplicados a descuentos perdidos | <ul><li>Descuentos aplicados a descuento perdido</li><li>Detalles de descuentos aplicados a descuento perdido</li><li>Descuentos aplicados a descuento perdido por empresa</li><li>Descuentos aplicados a descuento perdido por grupo de proveedores</li></ul> |
| Facturas que vencen en el futuro | <ul><li>Facturas que vencen en el futuro</li><li>Detalles de facturas que vencen en el futuro</li><li>Facturas que vencen en el futuro por empresa</li><li>Facturas que vencen en el futuro por grupo de proveedores</li><li>Facturas pendientes en el futuro por fecha de descuento por pronto pago</li><li>Facturas pendientes en el futuro por fecha de vencimiento</li></ul> |
| Facturas pagadas tarde | <ul><li>Facturas pagadas después de vencimiento</li><li>Detalles de facturas pagadas después de vencimiento</li><li>Facturas pagadas después de vencimiento por empresa</li><li>Facturas pagadas después de vencimiento por grupo de proveedores</li><li>Facturas pagadas tarde frente a facturas pagadas a tiempo</li></ul> |
| Flujo de trabajo de pagos | <ul><li>Instancias de flujo de trabajo de pago a proveedores</li><li>Instancias de flujo de trabajo de pago a proveedores por responsable</li><li>Instancias de flujo de trabajo de pago a proveedores por empresa</li><li>Promedio días en el flujo de trabajo por responsable</li></ul> |
| Saldo cliente/proveedor | <ul><li>Saldo cliente/proveedor</li><li>Saldo cliente/proveedor por empresa</li><li>Detalles del saldo cliente/proveedor</li></ul> |
| Facturas con el pago en espera | <ul><li>Facturas con el pago en espera</li><li>Detalles sobre facturas con el pago en espera</li><li>Facturas con el pago en espera por empresa</li><li>Facturas con el pago en espera por grupo de proveedores</li></ul> |
