---
title: Grupos de crédito del cliente
description: Este tema proporciona información sobre los grupos de crédito de cliente.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015386"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="f6730-103">Grupos de crédito del cliente</span><span class="sxs-lookup"><span data-stu-id="f6730-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f6730-104">Puede definir grupos de clientes que tienen el mismo límite de crédito.</span><span class="sxs-lookup"><span data-stu-id="f6730-104">You can define groups of customers who have the same credit limit.</span></span> <span data-ttu-id="f6730-105">También se considera el límite de crédito individual que se define en la cuenta de la factura del cliente.</span><span class="sxs-lookup"><span data-stu-id="f6730-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="f6730-106">Los miembros de un grupo de crédito de cliente pueden seleccionarse de diferentes entidades jurídicas.</span><span class="sxs-lookup"><span data-stu-id="f6730-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="f6730-107">Cuando agrega un cliente a la lista de clientes en el grupo de crédito de cliente, la fecha de vencimiento del límite de crédito para cada cliente cambia a la fecha de vencimiento que se asigna al grupo.</span><span class="sxs-lookup"><span data-stu-id="f6730-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="f6730-108">Puede configurar grupos de crédito de cliente en la página **Grupos de crédito de cliente** (**Administración de crédito \> Grupos de crédito de cliente \> Grupos de crédito de cliente**).</span><span class="sxs-lookup"><span data-stu-id="f6730-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="f6730-109">En los campos **Número de grupo** y **Descripción**, introduzca un identificador y una descripción para el grupo.</span><span class="sxs-lookup"><span data-stu-id="f6730-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="f6730-110">En los campos **Límite de crédito** y **Divisa**, introduzca el límite de crédito y la divida que se deben usar cuando el sistema comprueba el límite de crédito de cualquier miembro del grupo.</span><span class="sxs-lookup"><span data-stu-id="f6730-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="f6730-111">En el campo **Límite de crédito hasta la fecha**, introduzca la fecha en la que vence el límite de crédito.</span><span class="sxs-lookup"><span data-stu-id="f6730-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="f6730-112">Los grupos de crédito de cliente deben tener una fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="f6730-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="f6730-113">Una vez que haya terminado de configurar un grupo de crédito de cliente, puede agregar clientes especificado su entidad jurídica y su id. de cuenta de cliente.</span><span class="sxs-lookup"><span data-stu-id="f6730-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="f6730-114">Al agregar un nuevo cliente a un grupo de crédito de cliente, el sistema busca la misma cuenta de cliente en todas las entidades jurídicas y le solicita que la agregue al grupo de crédito de cliente.</span><span class="sxs-lookup"><span data-stu-id="f6730-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="f6730-115">Use el menú **Saldos vencidos** para ver los detalles de saldo vencido de todos los clientes de factura en un grupo de crédito de cliente.</span><span class="sxs-lookup"><span data-stu-id="f6730-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="f6730-116">La página **Saldo vencido** muestra un resumen de los saldos vencidos de las cuentas de cliente de factura.</span><span class="sxs-lookup"><span data-stu-id="f6730-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>