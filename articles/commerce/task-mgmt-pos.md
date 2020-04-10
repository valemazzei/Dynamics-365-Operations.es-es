---
title: Administración de tareas en PDV
description: Este tema describe la gestión de tareas en la aplicación Microsoft Dynamics 365 Commerce de punto de venta (PDV).
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036795"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="41160-103">Administración de tareas en PDV</span><span class="sxs-lookup"><span data-stu-id="41160-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="41160-104">Este tema describe la gestión de tareas en la aplicación Microsoft Dynamics 365 Commerce de punto de venta (PDV).</span><span class="sxs-lookup"><span data-stu-id="41160-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="41160-105">Visión general</span><span class="sxs-lookup"><span data-stu-id="41160-105">Overview</span></span>

<span data-ttu-id="41160-106">La aplicación Dynamics 365 Commerce PDV tiene funciones de administración de tareas que permiten a los gerentes de tienda y trabajadores administrar tareas y actualizar el estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="41160-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="41160-107">Los trabajadores de la tienda pueden acceder a las tareas seleccionando el mosaico **Tareas** mosaico en la página de inicio de PDV o seleccionando notificaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="41160-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="41160-108">Por defecto, los trabajadores de la tienda son llevados a la pestaña **Mis tareas**, donde pueden ver las tareas que se les asignan.</span><span class="sxs-lookup"><span data-stu-id="41160-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="41160-109">Sin embargo, pueden cambiar fácilmente a las pestañas **Tareas atrasadas**, **Tareas abiertas** y **Listas de tareas**.</span><span class="sxs-lookup"><span data-stu-id="41160-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="41160-110">Operaciones de tareas para gerentes de tienda</span><span class="sxs-lookup"><span data-stu-id="41160-110">Task operations for store managers</span></span>

<span data-ttu-id="41160-111">Los gerentes de tienda pueden realizar las siguientes operaciones de tareas en la aplicación PDV utilizando los botones de la barra de comandos:</span><span class="sxs-lookup"><span data-stu-id="41160-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="41160-112">**Asignar** - Asignar tareas seleccionadas a un trabajador de la tienda.</span><span class="sxs-lookup"><span data-stu-id="41160-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="41160-113">**Estado de la tarea** - Cambia el estado de las tareas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="41160-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="41160-114">**Filtrar** - Por defecto, solo se muestran las tareas activas.</span><span class="sxs-lookup"><span data-stu-id="41160-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="41160-115">Sin embargo, al aplicar filtros, los gerentes pueden ver todas las tareas, incluso las tareas que se han completado o cancelado.</span><span class="sxs-lookup"><span data-stu-id="41160-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="41160-116">**Nueva tarea** - Crea una tarea en una lista de tareas existente o una tarea de un solo propósito.</span><span class="sxs-lookup"><span data-stu-id="41160-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="41160-117">Los trabajadores de la tienda pueden realizar las siguientes operaciones de tareas en la aplicación PDV utilizando los botones de la barra de comandos:</span><span class="sxs-lookup"><span data-stu-id="41160-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="41160-118">**Estado de la tarea** - Cambia el estado de las tareas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="41160-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="41160-119">**Filtrar** - Por defecto, solo se muestran las tareas activas.</span><span class="sxs-lookup"><span data-stu-id="41160-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="41160-120">Sin embargo, al aplicar filtros, los trabajadores pueden ver todas las tareas, incluso las tareas que se han completado o cancelado.</span><span class="sxs-lookup"><span data-stu-id="41160-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="41160-121">La siguiente ilustración muestra la pestaña **Mis tareas** en la aplicación PDV de Commerce.</span><span class="sxs-lookup"><span data-stu-id="41160-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Pestaña Mis tareas en la aplicación PDV de Commerce](media/POS-task-management.png)

<span data-ttu-id="41160-123">La ilustración siguiente muestra la pestaña **Lista de tareas**.</span><span class="sxs-lookup"><span data-stu-id="41160-123">The following illustration shows the **Task lists** tab.</span></span>

![Pestaña lista de tareas en la aplicación PDV de Commerce](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="41160-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="41160-125">Additional resources</span></span>

[<span data-ttu-id="41160-126">Visión general de la administración de tareas</span><span class="sxs-lookup"><span data-stu-id="41160-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="41160-127">Configurar la administración de tareas</span><span class="sxs-lookup"><span data-stu-id="41160-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="41160-128">Crear listas de tareas y agregar tareas</span><span class="sxs-lookup"><span data-stu-id="41160-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="41160-129">Asignar listas de tareas a tiendas o empleados</span><span class="sxs-lookup"><span data-stu-id="41160-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)