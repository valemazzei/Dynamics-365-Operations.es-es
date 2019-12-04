---
title: Espacio de trabajo móvil de entrada de tiempo de proyecto
description: Este tema proporciona información acerca del espacio de trabajo móvil de entrada de horas del proyecto. Este espacio de trabajo permite a los usuarios especificar y guardar la hora en un proyecto mediante el dispositivo móvil.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250378"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="8cf93-104">Espacio de trabajo móvil de entrada de tiempo de proyecto</span><span class="sxs-lookup"><span data-stu-id="8cf93-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cf93-105">Este tema proporciona información acerca del espacio de trabajo móvil **Entrada de tiempo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="8cf93-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="8cf93-106">Este espacio de trabajo permite a los usuarios especificar y guardar la hora en un proyecto mediante el dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="8cf93-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="8cf93-107">Este espacio de trabajo móvil se debe usar con la aplicación Dynamics 365 Unified Operations mobile.</span><span class="sxs-lookup"><span data-stu-id="8cf93-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="8cf93-108">Visión general</span><span class="sxs-lookup"><span data-stu-id="8cf93-108">Overview</span></span>
<span data-ttu-id="8cf93-109">Como parte de su trabajo diario, los recursos de proyecto están a menudo in situ o de viaje.</span><span class="sxs-lookup"><span data-stu-id="8cf93-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="8cf93-110">El espacio de trabajo móvil **Entrada de horas del proyecto** permite a los usuarios especificar su tiempo facturable o no facturable relativo a un proyecto, en el dispositivo móvil de su elección.</span><span class="sxs-lookup"><span data-stu-id="8cf93-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="8cf93-111">Por lo tanto, los recursos de proyecto pueden registrar las entradas de horas en cualquier momento y cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="8cf93-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="8cf93-112">También se pueden ver las entradas de horas que ya se han registrado.</span><span class="sxs-lookup"><span data-stu-id="8cf93-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="8cf93-113">Específicamente, en el espacio de trabajo móvil **Entrada de tiempo del proyecto**, los usuarios pueden realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="8cf93-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="8cf93-114">Para cualquier fecha seleccionada, especifique el número de horas empleadas en una tarea específica.</span><span class="sxs-lookup"><span data-stu-id="8cf93-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="8cf93-115">Busque por nombre del proyecto o el cliente para encontrar el proyecto para el que debe especificar las horas.</span><span class="sxs-lookup"><span data-stu-id="8cf93-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="8cf93-116">Especifique la categoría y la actividad de las horas empleadas.</span><span class="sxs-lookup"><span data-stu-id="8cf93-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="8cf93-117">Registre la hora como facturable o no facturable para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="8cf93-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="8cf93-118">También puede especificar cualquier comentario externo o interno.</span><span class="sxs-lookup"><span data-stu-id="8cf93-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8cf93-119">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8cf93-119">Prerequisites</span></span>
<span data-ttu-id="8cf93-120">Los requisitos previos varían, en función de la versión de Microsoft Dynamics 365 que se ha implementado para su organización.</span><span class="sxs-lookup"><span data-stu-id="8cf93-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="8cf93-121">Requisitos previos si usa Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="8cf93-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="8cf93-122">Si Finance se ha implementado para su organización, el administrador del sistema debe publicar el espacio de trabajo móvil **Entrada de tiempo del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="8cf93-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="8cf93-123">Para obtener instrucciones, consulte [Publicar un espacio de trabajo móvil](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="8cf93-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="8cf93-124">Los requisitos previos si usa la versión 1611 con la actualización de plataforma 3 o posterior</span><span class="sxs-lookup"><span data-stu-id="8cf93-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="8cf93-125">Si se ha implementado la versión 1611 con actualización de plataforma 3 o posterior en su organización, el administrador del sistema debe cumplir los requisitos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8cf93-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8cf93-126">Requisito previo</span><span class="sxs-lookup"><span data-stu-id="8cf93-126">Prerequisite</span></span></th>
<th><span data-ttu-id="8cf93-127">Función</span><span class="sxs-lookup"><span data-stu-id="8cf93-127">Role</span></span></th>
<th><span data-ttu-id="8cf93-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cf93-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="8cf93-129">Implementar 4018050 KB.</span><span class="sxs-lookup"><span data-stu-id="8cf93-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="8cf93-130">Administrador del sistema</span><span class="sxs-lookup"><span data-stu-id="8cf93-130">System administrator</span></span></td>
<td><span data-ttu-id="8cf93-131">KB 4018050 es una sustitución de actualización o de metadatos X++ que contiene el espacio de trabajo móvil <strong>Entrada de horas del proyecto</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cf93-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="8cf93-132">Para implementar KB 4018050, el administrador del sistema debe seguir estos pasos.</span><span class="sxs-lookup"><span data-stu-id="8cf93-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="8cf93-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Descargar la revisión de metadatos de Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="8cf93-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="8cf93-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Instalar la revisión de metadatos</a>.</span><span class="sxs-lookup"><span data-stu-id="8cf93-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="8cf93-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Crear un paquete desplegable</a> que contenga los modelos <strong>ApplicationSuite</strong> y <strong>ProjectMobile</strong> y luego cargar el paquete desplegable en LCS.</span><span class="sxs-lookup"><span data-stu-id="8cf93-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="8cf93-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Aplicar el paquete implementable</a>.</span><span class="sxs-lookup"><span data-stu-id="8cf93-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cf93-137">Publique el espacio de trabajo móvil <strong>Entrada de tiempo del proyecto</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cf93-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="8cf93-138">Administrador del sistema</span><span class="sxs-lookup"><span data-stu-id="8cf93-138">System administrator</span></span></td>
<td><span data-ttu-id="8cf93-139">Consulte <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publicar un espacio de trabajo móvil</a>.</span><span class="sxs-lookup"><span data-stu-id="8cf93-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="8cf93-140">Descargar e instalar la aplicación móvil</span><span class="sxs-lookup"><span data-stu-id="8cf93-140">Download and install the mobile app</span></span>

<span data-ttu-id="8cf93-141">Descargue e instale la aplicación móvil Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="8cf93-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="8cf93-142">Para teléfonos Android</span><span class="sxs-lookup"><span data-stu-id="8cf93-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="8cf93-143">Para iPhones</span><span class="sxs-lookup"><span data-stu-id="8cf93-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="8cf93-144">Iniciar sesión en la aplicación móvil</span><span class="sxs-lookup"><span data-stu-id="8cf93-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="8cf93-145">Inicie la aplicación en su dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="8cf93-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="8cf93-146">Escriba la URL de Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8cf93-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="8cf93-147">La primera vez que se inicie sesión, se le solicitará su nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="8cf93-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="8cf93-148">Escriba sus credenciales.</span><span class="sxs-lookup"><span data-stu-id="8cf93-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="8cf93-149">Tras iniciar sesión, se mostrarán los espacios de trabajo disponibles para su empresa.</span><span class="sxs-lookup"><span data-stu-id="8cf93-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="8cf93-150">Tenga en cuenta que si el administrador del sistema publica un nuevo espacio de trabajo más tarde, tendrá que actualizar la lista de espacios de trabajo móviles.</span><span class="sxs-lookup"><span data-stu-id="8cf93-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="8cf93-151">[![Toque la pantalla para actualizar](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="8cf93-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="8cf93-152">Especifique las horas mediante el espacio de trabajo móvil de entrada de horas del proyecto</span><span class="sxs-lookup"><span data-stu-id="8cf93-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="8cf93-153">En el dispositivo móvil, seleccione el espacio de trabajo **Entrada de horas del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="8cf93-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="8cf93-154">Seleccione **Entrada de horas**</span><span class="sxs-lookup"><span data-stu-id="8cf93-154">Select **Time entry**.</span></span> <span data-ttu-id="8cf93-155">Se muestran las fechas de calendario de la semana actual.</span><span class="sxs-lookup"><span data-stu-id="8cf93-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="8cf93-156">Para una fecha seleccionada, seleccione **Acciones** &gt; **Nueva entrada**.</span><span class="sxs-lookup"><span data-stu-id="8cf93-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="8cf93-157">Escriba la cantidad de horas que deben registrarse.</span><span class="sxs-lookup"><span data-stu-id="8cf93-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="8cf93-158">Seleccione el proyecto de la entrada de horas.</span><span class="sxs-lookup"><span data-stu-id="8cf93-158">Select the project for the time entry.</span></span> <span data-ttu-id="8cf93-159">Una lista muestra los proyectos que están cargados en su aplicación para su uso sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8cf93-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="8cf93-160">Hay 50 artículos cargados de forma predeterminada, pero un desarrollador puede cambiar este número.</span><span class="sxs-lookup"><span data-stu-id="8cf93-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="8cf93-161">Para obtener más información, consulte [Plataforma móvil](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="8cf93-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="8cf93-162">Si el proyecto no está en la lista, seleccione **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="8cf93-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="8cf93-163">Busque por su nombre, o cambie a la búsqueda al nombre del proyecto o el cliente.</span><span class="sxs-lookup"><span data-stu-id="8cf93-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="8cf93-164">Permite seleccionar una categoría.</span><span class="sxs-lookup"><span data-stu-id="8cf93-164">Select a category.</span></span> <span data-ttu-id="8cf93-165">Una lista muestra las categorías que están cargadas en su aplicación para su uso sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8cf93-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="8cf93-166">Hay 50 artículos cargados de forma predeterminada, pero un desarrollador puede cambiar este número.</span><span class="sxs-lookup"><span data-stu-id="8cf93-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="8cf93-167">Para obtener más información, consulte [Plataforma móvil](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="8cf93-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="8cf93-168">Si la categoría no está en la lista, seleccione **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="8cf93-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="8cf93-169">Busque por categoría o cambie a buscar por nombre de categoría.</span><span class="sxs-lookup"><span data-stu-id="8cf93-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="8cf93-170">Seleccione una actividad.</span><span class="sxs-lookup"><span data-stu-id="8cf93-170">Select an activity.</span></span> <span data-ttu-id="8cf93-171">Una lista muestra las actividades que están cargadas en su aplicación para su uso sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8cf93-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="8cf93-172">Hay 50 artículos cargados de forma predeterminada, pero un desarrollador puede cambiar este número.</span><span class="sxs-lookup"><span data-stu-id="8cf93-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="8cf93-173">Para obtener más información, consulte [Plataforma móvil](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="8cf93-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="8cf93-174">Si la actividad no está en la lista, seleccione **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="8cf93-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="8cf93-175">Busque por número de actividad o cambie a buscar por propósito.</span><span class="sxs-lookup"><span data-stu-id="8cf93-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="8cf93-176">Seleccione la propiedad del línea.</span><span class="sxs-lookup"><span data-stu-id="8cf93-176">Select the line property.</span></span>
12. <span data-ttu-id="8cf93-177">Opcional: puede especificar cualquier comentario externo o interno.</span><span class="sxs-lookup"><span data-stu-id="8cf93-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="8cf93-178">Seleccione **Listo**.</span><span class="sxs-lookup"><span data-stu-id="8cf93-178">Select **Done**.</span></span>