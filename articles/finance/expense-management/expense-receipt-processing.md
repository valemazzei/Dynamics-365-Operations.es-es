---
title: Procesamiento de recibos de gastos
description: Este tema proporciona información sobre el procesamiento de recibos mediante reconocimiento óptico de caracteres (OCR). Esta característica está diseñada para mejorar la experiencia del usuario cuando se crean informes de gastos en Microsoft Dynamics 365 Finance.
author: stevensporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ead9039de63e2cf4f3a7faddd1702b9614d7f99
ms.sourcegitcommit: 6aceca43c53c4dde46954c0b6b855d488eb44ed2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027912"
---
# <a name="public-preview-expense-receipt-processing"></a><span data-ttu-id="bdf8c-104">Versión preliminar pública: procesamiento de recibos de gastos</span><span class="sxs-lookup"><span data-stu-id="bdf8c-104">Public Preview: Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="bdf8c-105">La entrada de gastos se ha mejorado mediante la introducción del procesamiento de reconocimiento óptico de caracteres (OCR) para los recibos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="bdf8c-106">Esta característica está diseñada para mejorar la experiencia del usuario cuando se crean informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="bdf8c-107">Funciones principales</span><span class="sxs-lookup"><span data-stu-id="bdf8c-107">Key features</span></span>

- <span data-ttu-id="bdf8c-108">El nombre del comerciante, la fecha y el importe total se extraen de los recibos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="bdf8c-109">La función intenta hacer coincidir los recibos no vinculados con las transacciones de gastos no vinculados.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="bdf8c-110">Los usuarios pueden crear transacciones de gastos ingresadas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="bdf8c-111">Ejemplos de uso</span><span class="sxs-lookup"><span data-stu-id="bdf8c-111">Usage examples</span></span>

- <span data-ttu-id="bdf8c-112">**Adjuntar automáticamente recibos que incluyan transacciones con tarjeta de crédito cuando se cree un informe de gastos**</span><span class="sxs-lookup"><span data-stu-id="bdf8c-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="bdf8c-113">Abra el espacio de trabajo **Administración de gastos**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="bdf8c-114">En la pestaña **Recibos**, verifique que haya recibos sin adjuntar.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="bdf8c-115">También puede cargar recibos en la pestaña **Ingresos**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="bdf8c-116">En la pestaña **Gastos**, verifique que haya gastos sin adjuntar.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="bdf8c-117">Por lo general, el administrador de gastos importa estos gastos del proveedor de la tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="bdf8c-118">Seleccione **Nuevo informe de gastos**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-118">Select **New expense report**.</span></span> <span data-ttu-id="bdf8c-119">Tenga en cuenta que ahora también puede incluir gastos y recibos cuando cree un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="bdf8c-120">Si agrega gastos y recibos, se activa la comparación automática de los recibos con los gastos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="bdf8c-121">**Crear un gasto o conciliar un gasto de un recibo**</span><span class="sxs-lookup"><span data-stu-id="bdf8c-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="bdf8c-122">En un informe de gastos, en la pestaña **Recibos**, adjunte un recibo seleccionando **Agregar recibos**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="bdf8c-123">Debajo de la imagen cargada del recibo, observe las opciones **Crear** y **Conciliar**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="bdf8c-124">Seleccione **Crear** para crear una transacción de gastos introducida manualmente y completar los valores que se extraen del recibo.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="bdf8c-125">Si selecciona **Conciliar**, el sistema intenta hacer coincidir un gasto existente con el recibo.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="bdf8c-126">Instalación</span><span class="sxs-lookup"><span data-stu-id="bdf8c-126">Installation</span></span>

<span data-ttu-id="bdf8c-127">Esta característica funciona en combinación con **Informes de gastos reinventados** para ayudar a simplificar la experiencia de los gastos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="bdf8c-128">Para usar estas capacidades avanzadas de gastos, instale el complemento del Servicio de administración de gastos para Microsoft Dynamics 365 Finance y active las funciones en su instancia.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="bdf8c-129">Puede acceder al complemento desde su proyecto en Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bdf8c-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="bdf8c-130">Inicie sesión en LCS y abra el entorno deseado.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="bdf8c-131">Vaya a **Detalles completos**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="bdf8c-132">Seleccione **Mantener** o descienda hasta la ficha desplegable **Complementos del entorno**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="bdf8c-133">Seleccione **Instalar un nuevo complemento**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="bdf8c-134">Seleccione **Servicio de administración de gastos**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="bdf8c-135">Siga la guía de instalación y acepte los términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="bdf8c-136">Seleccione **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-136">Select **Install**.</span></span>

<span data-ttu-id="bdf8c-137">En el espacio de trabajo **Administración de características**, active las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="bdf8c-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="bdf8c-138">Informes de gastos reinventados</span><span class="sxs-lookup"><span data-stu-id="bdf8c-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="bdf8c-139">Conciliar automáticamente y crear gasto del recibo</span><span class="sxs-lookup"><span data-stu-id="bdf8c-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="bdf8c-140">Al activar estas características, ocurren las acciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="bdf8c-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="bdf8c-141">El espacio de trabajo **Gestión de gastos** existente se reemplaza con el nuevo espacio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="bdf8c-142">Un nuevo elemento de menú para la visibilidad del campo de gastos se agrega.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="bdf8c-143">Todavía puedes abrir la antigua página **Informes de gastos** yendo a **Gestión de gastos > Mis gastos > Informes de gastos**.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="bdf8c-144">Los flujos de trabajo y la aprobación aún le llevan a la página existente de los informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="bdf8c-145">Los recibos serán procesados a través de Microsoft Azure Cognitive Services y los metadatos se extraerán y agregarán.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="bdf8c-146">Se agrega una opción que le permite crear un informe de gastos que incluye recibos no asociados coincidentes.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="bdf8c-147">Una opción que se agrega a los informes de gastos permite crear una línea de gastos a partir de un recibo o intenta conciliar un recibo existente con una línea de gastos existente.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="bdf8c-148">Para obtener más información sobre la función de informes de gastos reinventada, consulte [Informes de gastos reinventados](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="bdf8c-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="bdf8c-149">Preguntas frecuentes</span><span class="sxs-lookup"><span data-stu-id="bdf8c-149">Frequently asked questions</span></span>

<span data-ttu-id="bdf8c-150">**¿Microsoft usa mis datos para sus modelos?**</span><span class="sxs-lookup"><span data-stu-id="bdf8c-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="bdf8c-151">No, Microsoft ha creado un modelo general de aprendizaje automático para su servicio de procesamiento de recibos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="bdf8c-152">Este modelo no se basa en los recibos que carga.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="bdf8c-153">**¿Dónde está disponible y se procesa esta función?**</span><span class="sxs-lookup"><span data-stu-id="bdf8c-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="bdf8c-154">Actualmente, solo en los Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="bdf8c-155">**¿Dónde van mis recibos?**</span><span class="sxs-lookup"><span data-stu-id="bdf8c-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="bdf8c-156">Finance se pondrá en contacto con Cognitive Services para extraer los datos de campo.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="bdf8c-157">Cognitive Services retendrá una copia de su recibo por hasta 24 horas mientras se procesa.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="bdf8c-158">Una vez completado el procesamiento, Cognitive Services eliminará el recibo.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="bdf8c-159">Los recibos todavía se almacenan en Finanzas.</span><span class="sxs-lookup"><span data-stu-id="bdf8c-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="bdf8c-160">Para más información, vea [Habilitar la comprensión de los recibos con la nueva funcionalidad del reconocedor de formularios](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="bdf8c-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>