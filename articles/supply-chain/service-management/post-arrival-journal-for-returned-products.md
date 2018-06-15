---
title: Registrar diario de llegadas para productos devueltos
description: Registrar diario de llegadas para productos devueltos.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cbe60846f0a16b5061349d9960c49bb5310bd6f9
ms.contentlocale: es-es
ms.lasthandoff: 05/08/2018

---


# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="19904-103">Registrar diario de llegadas para productos devueltos</span><span class="sxs-lookup"><span data-stu-id="19904-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="19904-104">Para procesar una devolución, primero valide la cantidad de devolución y actualice el campo de cantidad en el diario de recepción de artículos.</span><span class="sxs-lookup"><span data-stu-id="19904-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="19904-105">A continuación, seleccione un código de disposición o indique que los artículos devueltos tienen que inspeccionarse.</span><span class="sxs-lookup"><span data-stu-id="19904-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="19904-106">Cuando haya completado estos pasos, puede registrar el diario de llegadas de artículos del pedido de devolución.</span><span class="sxs-lookup"><span data-stu-id="19904-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="19904-107">Haga clic en **Gestión del inventario** \> **Periódico** \> **Visión general de llegadas**.</span><span class="sxs-lookup"><span data-stu-id="19904-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="19904-108">En el filtro **Configurar nombre** , seleccione **Pedido de devolución**.</span><span class="sxs-lookup"><span data-stu-id="19904-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="19904-109">Si la lista de recepciones es larga, utilice los campos del área **Intervalo** para limitar la lista.</span><span class="sxs-lookup"><span data-stu-id="19904-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="19904-110">Localice la línea del pedido de devolución que desea registrar, seleccione el cuadro **Seleccionar para llegada** y, a continuación, haga clic en **Iniciar llegada**.</span><span class="sxs-lookup"><span data-stu-id="19904-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="19904-111">Haga clic en **Diarios** \> **Mostrar llegadas a partir de recepciones** para abrir el formulario **Diario de ubicaciones**.</span><span class="sxs-lookup"><span data-stu-id="19904-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="19904-112">Para ver información detallada, seleccione un diario y, a continuación, haga clic en <STRONG>Líneas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="19904-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="19904-113">Realice las actualizaciones necesarias y haga clic en **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="19904-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="19904-114">Una vez registrado el diario, se registran los artículos devueltos en el inventario y el formulario **Pedidos de devolución** indica que los artículos han llegado al almacén.</span><span class="sxs-lookup"><span data-stu-id="19904-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="19904-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="19904-115">See also</span></span>

<span data-ttu-id="19904-116">[Diario de ubicaciones (formulario)](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="19904-116">[Location journal (form)](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))</span></span>

  


