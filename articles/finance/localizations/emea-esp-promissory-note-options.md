---
title: Opciones de pagaré español
description: Este tema describe opciones y cambios en la funcionalidad básica de pagarés implementada en Microsoft Dynamics 365 Finance para las entidades jurídicas en España.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters, BankPromissoryNoteTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264624
ms.search.region: Spain
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 64cfd3185f16a5bf10d3780295fcf83ae37ee37e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175728"
---
# <a name="spanish-promissory-note-options"></a><span data-ttu-id="ec31d-103">Opciones de pagaré español</span><span class="sxs-lookup"><span data-stu-id="ec31d-103">Spanish promissory note options</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec31d-104">Este tema describe opciones y cambios en la funcionalidad básica de pagarés implementada en España.</span><span class="sxs-lookup"><span data-stu-id="ec31d-104">This topic describes options and changes for the basic promissory note functionality that is implemented for Spain.</span></span>

<span data-ttu-id="ec31d-105">Para las entidades jurídicas en España, la funcionalidad de pagaré tiene opciones adicionales:</span><span class="sxs-lookup"><span data-stu-id="ec31d-105">For legal entities in Spain, the promissory note functionality has additional options:</span></span>

-   <span data-ttu-id="ec31d-106">Validación de los diarios de pagarés</span><span class="sxs-lookup"><span data-stu-id="ec31d-106">Validation for promissory notes journals</span></span>
-   <span data-ttu-id="ec31d-107">Fechas en los diarios de pagarés</span><span class="sxs-lookup"><span data-stu-id="ec31d-107">Dates in promissory notes journals</span></span>
-   <span data-ttu-id="ec31d-108">Confirmación de facturas</span><span class="sxs-lookup"><span data-stu-id="ec31d-108">Invoice confirmation</span></span>

## <a name="accounts-payable-parameters-for-spanish-promissory-notes"></a><span data-ttu-id="ec31d-109">Parámetros de proveedor para pagarés españoles</span><span class="sxs-lookup"><span data-stu-id="ec31d-109">Accounts payable parameters for Spanish promissory notes</span></span>
<span data-ttu-id="ec31d-110">Para configurar los parámetros de los pagarés para las entidades jurídicas en España, vaya a **Parámetros de proveedores** &gt; **Pagarés ES**.</span><span class="sxs-lookup"><span data-stu-id="ec31d-110">To set up parameters for promissory notes for legal entities in Spain, go to **Accounts payable parameters** &gt; **Promissory notes ES**.</span></span>

## <a name="validation-for-promissory-notes-journals"></a><span data-ttu-id="ec31d-111">Validación de los diarios de pagarés</span><span class="sxs-lookup"><span data-stu-id="ec31d-111">Validation for promissory notes journals</span></span>
<span data-ttu-id="ec31d-112">Si el parámetro **Validación del diario de pagarés** se establece en **Sí**, el número de identificación fiscal del proveedor se valida al agregar líneas y rellenarlas en un diario de liquidación de pagarés.</span><span class="sxs-lookup"><span data-stu-id="ec31d-112">If the **Validation on promissory notes journal** parameter is set to **Yes**, the vendor's tax exempt number is validated when lines are added and fulfilled in a Promissory note settlement journal.</span></span> <span data-ttu-id="ec31d-113">Si este parámetro está establecido en **No**, y está activado **Nacional + estados miembros de la UE** en el campo **Requisito de NIF**, el número de identificación fiscal (NIF) no se valida.</span><span class="sxs-lookup"><span data-stu-id="ec31d-113">If this parameter is set to **No**, and if **Domestic + EU member states** is selected in the **Tax exempt number requirement** field, the tax exempt number isn't validated.</span></span>

## <a name="dates-in-promissory-notes-journals"></a><span data-ttu-id="ec31d-114">Fechas en los diarios de pagarés</span><span class="sxs-lookup"><span data-stu-id="ec31d-114">Dates in promissory notes journals</span></span>
<span data-ttu-id="ec31d-115">Si el parámetro **Tratamiento de datos (diarios de pagarés)** está establecido en **Sí**, el campo **Fecha mínima** se vacía al crear propuestas de pagos para Diarios de creación de pagarés y Diarios de remesa.</span><span class="sxs-lookup"><span data-stu-id="ec31d-115">If the **Date treatment (promissory notes journal)** parameter is set to **Yes**, the **Minimum date** field is cleared when you create payment proposals for Draw promissory note journals and Remittance journals.</span></span> <span data-ttu-id="ec31d-116">Por tanto, se usa la fecha de vencimiento como la fecha de transacción, aunque la fecha de vencimiento sea anterior a la del sistema.</span><span class="sxs-lookup"><span data-stu-id="ec31d-116">Therefore, the due date is used as the transaction date, even if the due date is before the system date.</span></span> <span data-ttu-id="ec31d-117">Si el parámetro **Tratamiento de datos (diarios de pagarés)** se establece en **No**, la fecha del sistema es la fecha predeterminada en el campo **Fecha mínima**.</span><span class="sxs-lookup"><span data-stu-id="ec31d-117">If the **Date treatment (promissory notes journal)** parameter is set to **No**, the system date is the default date in the **Minimum date** field.</span></span>

## <a name="invoice-confirmation"></a><span data-ttu-id="ec31d-118">Confirmación de facturas</span><span class="sxs-lookup"><span data-stu-id="ec31d-118">Invoice confirmation</span></span>
<span data-ttu-id="ec31d-119">Si el parámetro **Confirmando tratamiento de facturas** se establece en **Sí**, se crea una línea independiente para cada número de factura al crear propuestas de pago para diarios de remesa y diarios de liquidación de pagarés.</span><span class="sxs-lookup"><span data-stu-id="ec31d-119">If the **Confirming invoices treatment** parameter is set to **Yes**, a separate line is created for each invoice number when you create payment proposals for Remittance journals and Settle promissory note journals.</span></span> <span data-ttu-id="ec31d-120">Se crean líneas independientes, sea cual sea la selección en el campo **Periodo** para el método de pago.</span><span class="sxs-lookup"><span data-stu-id="ec31d-120">Separate lines are created, regardless of the selection in the **Period** field for the method of payment.</span></span> <span data-ttu-id="ec31d-121">Cada importe de factura puede comprobarse en el diario de remesas.</span><span class="sxs-lookup"><span data-stu-id="ec31d-121">Each invoice amount can be verified in the Remittance journal.</span></span> <span data-ttu-id="ec31d-122">Si el parámetro **Confirmando tratamiento de facturas** se establece en **No**, las líneas de diario pueden incluir importes para varias facturas, en función de la selección del campo **Período**.</span><span class="sxs-lookup"><span data-stu-id="ec31d-122">If the **Confirming invoices treatment** parameter is set to **No**, journal lines can include amounts for multiple invoices, depending on the selection in the **Period** field.</span></span>


