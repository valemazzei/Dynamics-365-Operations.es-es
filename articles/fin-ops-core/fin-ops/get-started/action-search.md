---
title: Búsqueda de acción
description: Este artículo describe la funcionalidad de búsqueda de la acción. La búsqueda de acción le ayudará a encontrar y ejecutar acciones en una página.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d01247aa356625cb759306e5ead2afd3cdeb840f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191325"
---
# <a name="action-search"></a><span data-ttu-id="b7ebd-104">Búsqueda de acción</span><span class="sxs-lookup"><span data-stu-id="b7ebd-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7ebd-105">Este artículo describe la funcionalidad de búsqueda de la acción.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-105">This article describes the action search functionality.</span></span> <span data-ttu-id="b7ebd-106">La búsqueda de acción le ayudará a encontrar y ejecutar acciones en una página.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="b7ebd-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="b7ebd-107">Introduction</span></span>

<span data-ttu-id="b7ebd-108">Las páginas exponen principalmente comandos en los paneles de acciones, tanto el panel de acciones estándar que aparece en la parte superior de una página como las barras de herramientas que aparecen en las distintas secciones de la página.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-108">Pages primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="b7ebd-109">En versiones anteriores, una característica de las sugerencias de teclas le permite acceder rápidamente a cualquier botón de un panel de acciones presionando la tecla Alt y, a continuación, una serie de letras.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="b7ebd-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="b7ebd-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="b7ebd-111">Las sugerencias de teclas no estarán disponibles pero han sido sustituidas por la función de búsqueda de la acción.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-111">Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="b7ebd-112">Esta característica nueva le permite rápidamente buscar y ejecutar un botón del Panel de acciones visible.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="b7ebd-113">Usar búsqueda de acciones</span><span class="sxs-lookup"><span data-stu-id="b7ebd-113">Using action search</span></span>

<span data-ttu-id="b7ebd-114">Para usar la característica de búsqueda de acciones, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="b7ebd-115">En el panels de acciones, haga clic en el campo **búsqueda de acciones**.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="b7ebd-116">(El campo **búsqueda de acción** contiene un icono de lupa.)</span><span class="sxs-lookup"><span data-stu-id="b7ebd-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="b7ebd-117">Escriba todo o parte del nombre del botón que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="b7ebd-118">También puede buscar usando palabras de la "ruta" del botón.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="b7ebd-119">(Para obtener más información, consulte la siguiente sección del artículo). Normalmente, aparecerá un botón cerca de la parte superior de la lista de resultados una vez que haya escrito de dos a cuatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="b7ebd-120">Busque y ejecute el botón en la lista de resultados (mediante el ratón o el teclado).</span><span class="sxs-lookup"><span data-stu-id="b7ebd-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="b7ebd-121">Después de ejecutar el botón, el foco se devuelve a la última posición de la página, de manera que pueda continuar trabajando.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="b7ebd-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="b7ebd-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="b7ebd-123">También puede iniciar la búsqueda de acciones presionando Ctrl+/ or Alt+Q.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="b7ebd-124">Presione el método abreviado de teclado de nuevo para devolver el foco a su última posición en la página.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="b7ebd-125">Comprensión de la lista de los resultados</span><span class="sxs-lookup"><span data-stu-id="b7ebd-125">Understanding the results list</span></span>

<span data-ttu-id="b7ebd-126">A menudo, debe conocer la ubicación y el contexto de un botón para comprender completamente el propósito de dicho botón.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-126">Often, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="b7ebd-127">Por lo tanto, la información adicional se muestra para cada elemento en la lista de resultados, para ayudarle a comprender exactamente qué botones aparecen en la lista.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="b7ebd-128">Concretamente, se muestra la "ruta" del botón.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="b7ebd-129">Esta ruta puede incluir las etiquetas de los siguientes elementos de la IU, según corresponda:</span><span class="sxs-lookup"><span data-stu-id="b7ebd-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="b7ebd-130">Ficha Panel de acciones</span><span class="sxs-lookup"><span data-stu-id="b7ebd-130">Action Pane tab</span></span>
- <span data-ttu-id="b7ebd-131">Grupo de botones</span><span class="sxs-lookup"><span data-stu-id="b7ebd-131">Button group</span></span>
- <span data-ttu-id="b7ebd-132">Botón de menú (si el botón está dentro de un botón de menú)</span><span class="sxs-lookup"><span data-stu-id="b7ebd-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="b7ebd-133">Separador de menú (si el botón está dentro de un grupo con nombre dentro de un botón de menú)</span><span class="sxs-lookup"><span data-stu-id="b7ebd-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="b7ebd-134">Grupo o separador o en la página (por ejemplo, el nombre de una ficha Desplegable)</span><span class="sxs-lookup"><span data-stu-id="b7ebd-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="b7ebd-135">Por ejemplo, si escribió **bebé** en el campo **búsqueda de acciones** y ahora está examinando la lista de los resultados.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="b7ebd-136">La primera entrada destaca un botón que se llama **Totales**.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="b7ebd-137">También aparece una ruta de botón **Pedido de ventas** &gt; **Visualización**.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="b7ebd-138">La parte de **Pedido de ventas** de la ruta de acceso corresponde a la pestaña **Pedido de ventas** del panel Acciones, y la parte **Vista** de la ruta de acceso corresponde al grupo **Vista** de esa pestaña. Igualmente, la ruta de acceso del botón **Descuento total** (**Vender** &gt; **Calcular**) le informa que el botón se ubicó en el grupo **Calcular** de la pestaña **Vender** del panel Acciones.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="b7ebd-139">Por lo tanto, esta información le ayuda a entender exactamente qué botón se activará con la búsqueda de acciones (si selecciona ese botón en la lista de resultados).</span><span class="sxs-lookup"><span data-stu-id="b7ebd-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="b7ebd-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="b7ebd-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="b7ebd-141">En el ejemplo anterior, la búsqueda de acción muestra resultados del panel de acciones estándar en la parte superior de una página.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="b7ebd-142">Sin embargo, la búsqueda de acciones también muestra resultados de barra de herramientas visibles situadas en otros lugares en la página.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="b7ebd-143">Por ejemplo, si está buscando el botón de **Inventario disponible** ubicado en la pestaña desplegable **Líneas de pedidos de ventas**.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b7ebd-144">En este caso, la ruta del botón en la lista de resultados (**Líneas de pedidos de ventas** &gt; **Inventario** &gt; **Visualización**) le informa de que este botón se encuentra debajo del encabezado de **Visualización** en el botón de menú **Inventario** en la pestaña desplegable **Líneas de pedidos de ventas**.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="b7ebd-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="b7ebd-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="b7ebd-146">Búsqueda de acciones frente a búsqueda de navegación</span><span class="sxs-lookup"><span data-stu-id="b7ebd-146">Action search vs. Navigation search</span></span>

<span data-ttu-id="b7ebd-147">Mientras que la búsqueda de acciones se va a utilizar para encontrar y ejecutar acciones en una página, hay un mecanismo independiente de la búsqueda para encontrar y desplazarse a las páginas.</span><span class="sxs-lookup"><span data-stu-id="b7ebd-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages.</span></span> <span data-ttu-id="b7ebd-148">Para obtener más información sobre dicha característica, consulte el artículo [Búsqueda de navegación](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="b7ebd-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>