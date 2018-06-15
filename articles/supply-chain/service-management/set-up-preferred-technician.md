---
title: "Configuración de un técnico preferido"
description: "Puede seleccionar cualquier trabajador como técnico preferido para un acuerdo de servicio o un pedido de servicio."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable, SMADispatchBoard
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
ms.openlocfilehash: 390e436b63fdfe82e0b743e7f286cae3bb29be55
ms.contentlocale: es-es
ms.lasthandoff: 05/08/2018

---


# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="00baf-103">Configuración de un técnico preferido</span><span class="sxs-lookup"><span data-stu-id="00baf-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="00baf-104">Puede seleccionar cualquier trabajador como técnico preferido para un acuerdo de servicio o un pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="00baf-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="00baf-105">Sin embargo, es una buena idea agregar el trabajador al equipo de distribución apropiado de modo que el trabajador esté incluido en el **Panel de distribución**.</span><span class="sxs-lookup"><span data-stu-id="00baf-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="00baf-106">Asignar el empleado a un equipo de distribución</span><span class="sxs-lookup"><span data-stu-id="00baf-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="00baf-107">Haga clic en **Recursos humanos** \> **Común** \> **Trabajadores** \> **Trabajadores**.</span><span class="sxs-lookup"><span data-stu-id="00baf-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="00baf-108">Haga doble clic en un trabajador para abrir la página de detalles.</span><span class="sxs-lookup"><span data-stu-id="00baf-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="00baf-109">En el **Panel de acciones**, haga click en **Configuración** \>**Equipo de distribución** para abrir el formulario **Remitir trabajadores** .</span><span class="sxs-lookup"><span data-stu-id="00baf-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="00baf-110">En el campo **Equipo de distribución**, seleccione el equipo al que se va a asignar el trabajador.</span><span class="sxs-lookup"><span data-stu-id="00baf-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="00baf-111">Asignar un técnico preferido a un acuerdo de servicio</span><span class="sxs-lookup"><span data-stu-id="00baf-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="00baf-112">Haga clic en **Gestión de servicio** \> **Común** \> **Contratos de servicio** \> **Contratos de servicio**.</span><span class="sxs-lookup"><span data-stu-id="00baf-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="00baf-113">Haga doble clic en un acuerdo de servicio para abrir el formulario de detalles.</span><span class="sxs-lookup"><span data-stu-id="00baf-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="00baf-114">En la ficha **General**, seleccione el campo **Técnico preferido** y, a continuación, seleccione el miembro del equipo de distribución apropiado como técnico preferido para el acuerdo de servicio.</span><span class="sxs-lookup"><span data-stu-id="00baf-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="00baf-115">Asignar un técnico preferido a un pedido de servicio</span><span class="sxs-lookup"><span data-stu-id="00baf-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="00baf-116">Haga clic en **Gestión de servicios** \> **Periódico** \> **Panel de distribución**.</span><span class="sxs-lookup"><span data-stu-id="00baf-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="00baf-117">En el formulario <STRONG>Panel de distribución</STRONG>, especifique el intervalo de fechas de las actividades de distribución que desea ver.</span><span class="sxs-lookup"><span data-stu-id="00baf-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="00baf-118">Especifique también si desea ver las actividades cerradas y si se debe restringir la lista de actividades de distribución a los equipos a los que pertenece o los equipos que está autorizado a supervisar.</span><span class="sxs-lookup"><span data-stu-id="00baf-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="00baf-119">Haga clic en <STRONG>Aceptar</STRONG> para abrir el formulario <STRONG>Panel de distribución</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="00baf-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="00baf-120">Seleccione la línea de la actividad del servicio que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="00baf-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="00baf-121">En la ficha **Relacionado**, utilice la lista **Trabajador** para asignar un miembro del equipo de distribución apropiado como técnico preferido a la llamada de servicio.</span><span class="sxs-lookup"><span data-stu-id="00baf-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="00baf-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00baf-122">See also</span></span>

[<span data-ttu-id="00baf-123">Acuerdos de servicio </span><span class="sxs-lookup"><span data-stu-id="00baf-123">Service agreements</span></span>](service-agreements.md)

[<span data-ttu-id="00baf-124">Crear pedidos de servicio manualmente</span><span class="sxs-lookup"><span data-stu-id="00baf-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="00baf-125">[Acuerdos de servicio (formulario)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="00baf-125">[Service agreements (form)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))</span></span>
  


