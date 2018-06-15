---
title: "Usar códigos de motivo de etapa"
description: "El código de motivo se usa para indicar por qué se canceló un contrato de nivel de servicio (SLA) o por qué se superó el límite de tiempo de un pedido de servicio establecido en el SLA."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAParameters
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
ms.openlocfilehash: e42172fe1b484b91e9a3e3d05d438e7e9b0b0eb4
ms.contentlocale: es-es
ms.lasthandoff: 05/08/2018

---


# <a name="use-stage-reason-codes"></a><span data-ttu-id="885bf-103">Usar códigos de motivo de etapa</span><span class="sxs-lookup"><span data-stu-id="885bf-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="885bf-104">El código de motivo se usa para indicar por qué se canceló un contrato de nivel de servicio (SLA) o por qué se superó el límite de tiempo de un pedido de servicio establecido en el SLA.</span><span class="sxs-lookup"><span data-stu-id="885bf-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="885bf-105">También puede especificar que es necesario especificar un código de motivo cuando un SLA se cancela o cuando el límite de tiempo supera el tiempo que se especifica en el SLA para el pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="885bf-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="885bf-106">Si indicó que es necesario especificar un código de motivo, debe especificar un código de motivo en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="885bf-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="885bf-107">Cuando un pedido de servicio se traslada a una etapa que detiene el registro de tiempo en comparación con el SLA para el pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="885bf-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="885bf-108">Cuando se realiza la aprobación final del pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="885bf-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="885bf-109">Cuando el registro de tiempo se detiene manualmente.</span><span class="sxs-lookup"><span data-stu-id="885bf-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="885bf-110">Configurar códigos de motivos</span><span class="sxs-lookup"><span data-stu-id="885bf-110">Set up reason codes</span></span>

1.  <span data-ttu-id="885bf-111">Haga clic en **Gestión de servicio** \> **Configuración** \> **Pedidos de servicio** \> **Códigos de motivo de etapa**.</span><span class="sxs-lookup"><span data-stu-id="885bf-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="885bf-112">En el formulario **Códigos de motivo de etapa**, haga clic en **Nuevo** para crear un nuevo código de motivo.</span><span class="sxs-lookup"><span data-stu-id="885bf-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="885bf-113">En el campo **Código de motivo de etapa**, especifique un código de motivo de etapa única.</span><span class="sxs-lookup"><span data-stu-id="885bf-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="885bf-114">En el campo **Descripción**, especifique una descripción para el código de motivo de etapa.</span><span class="sxs-lookup"><span data-stu-id="885bf-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="885bf-115">Cierre el formulario para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="885bf-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="885bf-116">Exigir códigos de motivo cuando se cancele un acuerdo de nivel de servicio</span><span class="sxs-lookup"><span data-stu-id="885bf-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="885bf-117">Haga clic en **Gestión de servicio** \> **Configuración** \> **Parámetros de la gestión de servicio**.</span><span class="sxs-lookup"><span data-stu-id="885bf-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="885bf-118">En el formulario **Parámetros de gestión de servicio**, haga clic en el vínculo **General** y seleccione la casilla de verificación **Código de motivo al cancelar** .</span><span class="sxs-lookup"><span data-stu-id="885bf-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="885bf-119">Exigir códigos de motivo cuando un pedido de servicio supere el tiempo límite establecido en un contrato de nivel de servicio</span><span class="sxs-lookup"><span data-stu-id="885bf-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="885bf-120">Haga clic en **Gestión de servicio** \> **Configuración** \> **Parámetros de la gestión de servicio**.</span><span class="sxs-lookup"><span data-stu-id="885bf-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="885bf-121">En el formulario **Parámetros de gestión de servicio**, haga clic en el vínculo **General** y seleccione la casilla de verificación **Código de motivo al superar el tiempo** .</span><span class="sxs-lookup"><span data-stu-id="885bf-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="885bf-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="885bf-122">See also</span></span>

[<span data-ttu-id="885bf-123">Iniciar y detener registro de horas en un pedido de servicio</span><span class="sxs-lookup"><span data-stu-id="885bf-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


