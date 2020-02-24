---
title: Configuración de la funcionalidad de inicio de sesión extendido para MPOS y Cloud POS
description: En este tema se abordan las opciones de configuración de inicio de sesión extendido para Cloud POS y Retail Modern POS (MPOS).
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 79878e2ffbf219f77f378997c277ced8bb41598c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023977"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="afa41-103">Configurar la funcionalidad de inicio de sesión extendido para MPOS y Cloud POS</span><span class="sxs-lookup"><span data-stu-id="afa41-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="afa41-104">En este tema se abordan las opciones de configuración de inicio de sesión extendido para Cloud POS y Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="afa41-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="afa41-105">Configuración del inicio de sesión extendido</span><span class="sxs-lookup"><span data-stu-id="afa41-105">Setting up extended logon</span></span>

<span data-ttu-id="afa41-106">Puede encontrar la configuración de las máscaras de código de barras en **Retail y Commerce** &gt; **Configuración del canal** &gt; **Configuración del PDV** &gt; **Perfiles del PDV** &gt; **Perfiles de funcionalidad**.</span><span class="sxs-lookup"><span data-stu-id="afa41-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="afa41-107">La ficha desplegable **Funciones** incluye las siguientes opciones que están relacionadas con el inicio de sesión extendido.</span><span class="sxs-lookup"><span data-stu-id="afa41-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="afa41-108">Inicio de sesión de código de barras de personal</span><span class="sxs-lookup"><span data-stu-id="afa41-108">Staff bar code logon</span></span>

<span data-ttu-id="afa41-109">Cuando la opción **Inicio de sesión de código de barras del personal** se activa, los trabajadores que tienen un inicio de sesión extendido asignado a sus credenciales del punto de venta (PDV) pueden iniciar sesión mediante un código de barras.</span><span class="sxs-lookup"><span data-stu-id="afa41-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="afa41-110">El inicio de sesión de código de barras de personal requiere contraseña</span><span class="sxs-lookup"><span data-stu-id="afa41-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="afa41-111">Cuando se activa la opción **El inicio de sesión de código de barras del personal necesita contraseña**, el inicio de sesión de código de barras del personal selecciona únicamente el trabajador al que se la asignado el inicio de sesión extendido que se presenta.</span><span class="sxs-lookup"><span data-stu-id="afa41-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="afa41-112">Los trabajadores aún tienen que especificar su contraseña cuando se activa esta opción.</span><span class="sxs-lookup"><span data-stu-id="afa41-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="afa41-113">Inicio de sesión de tarjeta de personal</span><span class="sxs-lookup"><span data-stu-id="afa41-113">Staff card logon</span></span>

<span data-ttu-id="afa41-114">Cuando la opción **Inicio de sesión de tarjeta del personal**, los trabajadores que tienen un inicio de sesión extendido asignado a sus credenciales del PDV pueden iniciar sesión mediante una barra magnética.</span><span class="sxs-lookup"><span data-stu-id="afa41-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="afa41-115">El inicio de sesión de tarjeta de personal requiere contraseña</span><span class="sxs-lookup"><span data-stu-id="afa41-115">Staff card logon requires password</span></span>

<span data-ttu-id="afa41-116">Cuando se activa la opción **El inicio de sesión de tarjeta del personal necesita contraseña**, el inicio de sesión de tarjeta del personal selecciona únicamente el trabajador al que se la asignado el inicio de sesión extendido que se presenta.</span><span class="sxs-lookup"><span data-stu-id="afa41-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="afa41-117">Los trabajadores aún tienen que especificar su contraseña cuando se activa esta opción.</span><span class="sxs-lookup"><span data-stu-id="afa41-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="afa41-118">Asignación de un inicio de sesión extendido</span><span class="sxs-lookup"><span data-stu-id="afa41-118">Assigning an extended logon</span></span>

<span data-ttu-id="afa41-119">De forma predeterminada, solo los directores pueden asignar el inicio de sesión extendido a los trabajadores.</span><span class="sxs-lookup"><span data-stu-id="afa41-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="afa41-120">Para asignar el inicio de sesión extendido, vaya a **Inicio de sesión extendido** en PDV.</span><span class="sxs-lookup"><span data-stu-id="afa41-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="afa41-121">A continuación, busque un trabajador introduciendo su id. de operador en el campo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="afa41-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="afa41-122">Seleccione el trabajador y, a continuación, haga clic en la pestaña **Asignar**.</span><span class="sxs-lookup"><span data-stu-id="afa41-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="afa41-123">En la siguiente página, pase o o escanee el inicio de sesión que desee asignar al trabajador.</span><span class="sxs-lookup"><span data-stu-id="afa41-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="afa41-124">Si se lee correctamente, el botón **Aceptar** estará disponible.</span><span class="sxs-lookup"><span data-stu-id="afa41-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="afa41-125">Haga clic en **Aceptar** para guardar el inicio de sesión extendido para dicho trabajador.</span><span class="sxs-lookup"><span data-stu-id="afa41-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="afa41-126">Eliminación de un inicio de sesión extendido</span><span class="sxs-lookup"><span data-stu-id="afa41-126">Deleting an extended logon</span></span>

<span data-ttu-id="afa41-127">Para eliminar el inicio de sesión extendido que se asigna a un trabajador, busque el trabajador mediante la operación **Inicio de sesión extendido**.</span><span class="sxs-lookup"><span data-stu-id="afa41-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="afa41-128">Seleccione el trabajador y, a continuación, haga clic en **Anular asignación**.</span><span class="sxs-lookup"><span data-stu-id="afa41-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="afa41-129">Se eliminarán todas las credenciales de inicio de sesión extendidas asociadas con dicho trabajador.</span><span class="sxs-lookup"><span data-stu-id="afa41-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="afa41-130">Extensión de inicio de sesión extendido</span><span class="sxs-lookup"><span data-stu-id="afa41-130">Extending extended logon</span></span>

<span data-ttu-id="afa41-131">El servicio del inicio de sesión puede ser extendido para admitir dispositivos de inicio de sesión extendidos adicionales, como escáneres de la palma.</span><span class="sxs-lookup"><span data-stu-id="afa41-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="afa41-132">Para obtener más información, consulte la documentación de extensibilidad del PDV.</span><span class="sxs-lookup"><span data-stu-id="afa41-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="afa41-133">Uso del inicio de sesión extendido</span><span class="sxs-lookup"><span data-stu-id="afa41-133">Using extended logon</span></span>

<span data-ttu-id="afa41-134">Cuando se configura el inicio de sesión extendido, y se le ha asignado a un trabajador un código de barras o una cinta magnética, el trabajador sólo tiene que pasar o escanear su tarjeta mientras se abre la página de inicio de sesión del PDV.</span><span class="sxs-lookup"><span data-stu-id="afa41-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="afa41-135">Si una contraseña también es necesaria para que el inicio de sesión pueda continuar, se le pedirá al trabajador que especifique su contraseña.</span><span class="sxs-lookup"><span data-stu-id="afa41-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>