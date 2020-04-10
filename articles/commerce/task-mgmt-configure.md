---
title: Configurar la administración de tareas
description: Este tema describe cómo configurar las funciones de administración de tareas en Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036864"
---
# <a name="configure-task-management"></a><span data-ttu-id="d780d-103">Configurar la administración de tareas</span><span class="sxs-lookup"><span data-stu-id="d780d-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d780d-104">Este tema describe cómo configurar las funciones de administración de tareas en Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d780d-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d780d-105">Visión general</span><span class="sxs-lookup"><span data-stu-id="d780d-105">Overview</span></span>

<span data-ttu-id="d780d-106">Antes de que los gerentes y empleados en Dynamics 365 Commerce puedan usar las funciones de administración de tareas en Commerce, la administración de tareas debe estar configurada.</span><span class="sxs-lookup"><span data-stu-id="d780d-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="d780d-107">Los pasos de configuración incluyen otorgar permisos a gerentes y empleados, distribuir permisos a clientes de puntos de venta (PDV), configurar notificaciones de PDV y configurar el mosaico **Tareas** en la página de inicio de una aplicación PDV.</span><span class="sxs-lookup"><span data-stu-id="d780d-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="d780d-108">Configurar permisos para gerentes de tienda</span><span class="sxs-lookup"><span data-stu-id="d780d-108">Configure permissions for store managers</span></span>

<span data-ttu-id="d780d-109">Todos los trabajadores de una tienda determinada pueden ver todas las tareas asignadas a esa tienda.</span><span class="sxs-lookup"><span data-stu-id="d780d-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="d780d-110">También pueden actualizar el estado de las tareas que se les asignan.</span><span class="sxs-lookup"><span data-stu-id="d780d-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="d780d-111">Sin embargo, personas como los gerentes de la tienda deben tener permisos de administración de tareas para administrar las tareas que se asignan a la tienda y crear tareas de un solo propósito.</span><span class="sxs-lookup"><span data-stu-id="d780d-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="d780d-112">Para configurar permisos de administración de tareas para gerentes de tienda, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d780d-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="d780d-113">Vaya a **Retail y Commerce \> Empleados \> Grupos de permiso**.</span><span class="sxs-lookup"><span data-stu-id="d780d-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="d780d-114">Seleccione un grupo de permisos específico (por ejemplo, **Gerente**) y luego seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="d780d-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="d780d-115">En la ficha desplegable **Permisos**, configure la opción **Permitir gestión de tareas** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="d780d-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="d780d-116">En la ficha desplegable **Notificaciones**, agregue la operación **Administración de tareas** e introduzca un valor en el campo **Orden de visualización**.</span><span class="sxs-lookup"><span data-stu-id="d780d-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="d780d-117">Por ejemplo, introduzca **2** si la operación **Cumplimiento de pedido** ya tiene un valor de **Orden de visualización** de **1**.</span><span class="sxs-lookup"><span data-stu-id="d780d-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d780d-118">Si una persona que no es gerente debe tener permisos de administración de tareas en el PDV, puede otorgar permiso a la persona.</span><span class="sxs-lookup"><span data-stu-id="d780d-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="d780d-119">Alternativamente, puede crear un nuevo grupo de permisos para los no administradores y establecer la opción **Permitir gestión de tareas** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="d780d-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="d780d-120">La siguiente ilustración muestra cómo configurar los permisos de gestión de tareas para gerentes de tienda.</span><span class="sxs-lookup"><span data-stu-id="d780d-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Configurar permisos de administración de tareas para gerentes de tienda](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="d780d-122">Configurar permisos para empleados</span><span class="sxs-lookup"><span data-stu-id="d780d-122">Configure permissions for employees</span></span>

<span data-ttu-id="d780d-123">Los empleados deben tener permisos para crear listas de tareas, administrar criterios de asignación y configurar la recurrencia de cualquier lista de tareas.</span><span class="sxs-lookup"><span data-stu-id="d780d-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="d780d-124">Para configurar estos permisos, asigne empleados el rol de **Gerente de tareas de Retail**.</span><span class="sxs-lookup"><span data-stu-id="d780d-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="d780d-125">Para configurar permisis para un empleado, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d780d-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="d780d-126">Vaya a **Retail y Commerce \> Empleados \> Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="d780d-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="d780d-127">Seleccione un empleado.</span><span class="sxs-lookup"><span data-stu-id="d780d-127">Select an employee.</span></span>
1. <span data-ttu-id="d780d-128">En la ficha desplegable **Roles de usuarios** seleccione **Asignar roles**.</span><span class="sxs-lookup"><span data-stu-id="d780d-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="d780d-129">En el cuadro de diálogo **Asignar roles al usuario**, seleccione el rol **Gerente de tareas de Retail**, y luego seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d780d-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="d780d-130">Distribuir permisos a clientes PDV</span><span class="sxs-lookup"><span data-stu-id="d780d-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="d780d-131">Antes de que los empleados puedan usar clientes PDV, los permisos deben distribuirse y sincronizarse con esos clientes.</span><span class="sxs-lookup"><span data-stu-id="d780d-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="d780d-132">Para distribuir permisos a los clientes PDV, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d780d-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="d780d-133">Vaya a **Retail y Commerce \> TI de Retail y Commerce \> Programación de distribución**.</span><span class="sxs-lookup"><span data-stu-id="d780d-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="d780d-134">Seleccione el calendario de distribución **1060** (**Personal**) y luego seleccione **Ejecutar ahora**.</span><span class="sxs-lookup"><span data-stu-id="d780d-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="d780d-135">Seleccione el calendario de distribución **1070** (**Configuración de canal**) y luego seleccione **Ejecutar ahora**.</span><span class="sxs-lookup"><span data-stu-id="d780d-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="d780d-136">Configurar notificaciones de PDV para tareas</span><span class="sxs-lookup"><span data-stu-id="d780d-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="d780d-137">La gestión de tareas debe configurarse de modo que las notificaciones estén disponibles en la aplicación PDV.</span><span class="sxs-lookup"><span data-stu-id="d780d-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="d780d-138">Para configurar las notificaciones PDV para tareas, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d780d-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="d780d-139">Vaya a **Retail y Commerce \> Configuración de canal \> Configuración de PDV \> PDV \> Operaciones PDV**.</span><span class="sxs-lookup"><span data-stu-id="d780d-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="d780d-140">Encuentre la operación **1400** (**Administración de tareas**) y seleccione la casilla **Permitir notificaciones** para ello.</span><span class="sxs-lookup"><span data-stu-id="d780d-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="d780d-141">La siguiente ilustración muestra la operación **Administración de tareas** en la página **Operaciones PDV**.</span><span class="sxs-lookup"><span data-stu-id="d780d-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Operación de gestión de tareas en la página de operaciones de PDV](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="d780d-143">Para obtener más información sobre cómo configurar las notificaciones de PDV, vea [Mostrar notificaciones de pedidos en el punto de venta (PDV)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="d780d-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="d780d-144">Configure el mosaico Tareas en la página de inicio de una aplicación PDV</span><span class="sxs-lookup"><span data-stu-id="d780d-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="d780d-145">Antes de configurar el mosaico **Tareas** en la página de inicio de una aplicación PDV, vea [Diseños de pantalla para el punto de venta (PDV)](pos-screen-layouts.md) para obtener información sobre cómo configurar y agregar nuevos botones a un diseño de pantalla PDV.</span><span class="sxs-lookup"><span data-stu-id="d780d-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="d780d-146">Para configurar el mosaico **Tareas** en la página de inicio de una aplicación PDV, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d780d-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="d780d-147">Vaya a **Retail y Commerce \> Configuración de canal \> Configuración de PDV \> PDV \> Diseños de pantalla**.</span><span class="sxs-lookup"><span data-stu-id="d780d-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="d780d-148">Seleccione un diseño de pantalla, seleccione un tamaño de diseño y seleccione una cuadrícula de botones.</span><span class="sxs-lookup"><span data-stu-id="d780d-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="d780d-149">En la ficha desplegable **Cuadrículas de botones**, seleccione **Diseñador** para editar la cuadrícula del botón seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d780d-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="d780d-150">Agregue un mosaico **Tareas** a la sección correspondiente de la página de inicio.</span><span class="sxs-lookup"><span data-stu-id="d780d-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="d780d-151">La ilustración siguiente muestra un ejemplo de un mosaico **Tareas** en una página principal PDV.</span><span class="sxs-lookup"><span data-stu-id="d780d-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Mosaico de tareas en una página de principal de PDV](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="d780d-153">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d780d-153">Additional resources</span></span>

[<span data-ttu-id="d780d-154">Visión general de la administración de tareas</span><span class="sxs-lookup"><span data-stu-id="d780d-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="d780d-155">Crear listas de tareas y agregar tareas</span><span class="sxs-lookup"><span data-stu-id="d780d-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="d780d-156">Asignar listas de tareas a tiendas o empleados</span><span class="sxs-lookup"><span data-stu-id="d780d-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="d780d-157">Administración de tareas en PDV</span><span class="sxs-lookup"><span data-stu-id="d780d-157">Task management in POS</span></span>](task-mgmt-POS.md)