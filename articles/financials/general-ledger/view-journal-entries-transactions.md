---
title: Ver movimientos del diario y transacciones
description: "Este artículo explica las distintas maneras en las que puede ver entradas del diario y transacciones."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 91cf395f2245f85cb244c7532ea77a63da98fcd7
ms.contentlocale: es-es
ms.lasthandoff: 08/01/2017

---

# <a name="view-journal-entries-and-transactions"></a>Ver movimientos del diario y transacciones

[!include[banner](../includes/banner.md)]


Este artículo explica las distintas maneras en las que puede ver entradas del diario y transacciones. 

Los usuarios que desean ver diarios y transacciones tienen varias formas de tener acceso a los datos. Pueden aprovecharse de las páginas de consulta que proporcionan la capacidad de exploración en profundidad o bien, pueden usar varias opciones de informes en la contabilidad general.

## <a name="voucher-transactions"></a>Transacciones de asiento
**Transacciones de asiento** es una página de consulta donde puede seleccionar entre distintas tablas y campos para especificar criterios para el saldo o la transacción que busca. Por ejemplo, puede ver todas las transacciones para una fecha o cuenta concreta, o todas las transacciones del tipo **En proceso de desarrollo** que se encuentran en una capa de registro específica. De forma predeterminada, la página muestra el número de diario, el asiento, la fecha y la cuenta principal, pero puede agregar tablas, campos y criterios adicionales para restringir la búsqueda.

## <a name="audit-trail"></a>Traza de auditoría
**Traza de auditoría** es una página de consulta que muestra los tipos de transacciones, las descripciones, quiénes crearon las transacciones y cuándo se crearon. En la página de consulta **Traza de auditoría**, puede ver las transacciones de asiento.

## <a name="financial-reports"></a>Informes financieros
También puede explorar y analizar transacciones de contabilidad general ejecutando informes financieros. Dado que el diseño de los informes financieros se puede basar en cuentas, dimensiones, categorías de cuenta, o en una combinación de los tres, puede ver las transacciones explorando en profundidad de distintas maneras. Si necesita más información para transacciones de contabilidad general, también puede incluir varias propiedades de transacción como parte del diseño del informe. Además, si desea ver las transacciones que componen un saldo de contabilidad general, puede explorar en profundidad las transacciones de cuenta, tal como puede hacerlo en la página de lista **Saldo de comprobación**.

## <a name="ledger-reports"></a>Informes de contabilidad
Además de los informes financieros, puede usar los siguientes informes de contabilidad general para ver transacciones de contabilidad general:

-   **Extracto de dimensión**: este informe muestra transacciones por día y cuenta, y también hay opciones para mostrar transacciones por dimensión y período.
-   **Lista de transacciones contables**: este informe muestra transacciones en divisas de transacción, contabilidad e informes para una cuenta.
-   **Imprimir diario**: este informe muestra el resultado de un diario registrado. Puede ejecutar el informe por número de lote del diario o tipo de diario, o agregar campos adicionales.
-   **Transacciones registradas por diario**: este informe muestra las transacciones que se han registrado en un diario, agrupadas por asiento.
-   **Lista de transacciones por fecha**: este informe muestra todas las transacciones por fecha, junto con el número de diario, el asiento y la cuenta contable. También muestra las transacciones en las divisas de transacción, contabilidad e informes.
-   **Origen de la transacción**: este informe de transacciones muestra la cuenta por diario, y por divisa de transacción, contabilidad e informes. También muestra cada línea del diario que se usaba como contrapartida.


##<a name="see-also"></a>Consulte también
- [Saldos de cuentas de contabilidad](general-ledger-account-balances.md) 
- [Explorador de origen de contabilidad](..\accounts-payable\accounting-source-explorer.md)
- [Informes financieros](financial-reporting-getting-started.md)
- [Ver entradas del diario](tasks/view-journal-entries-or-transactions.md)



