---
title: ER Configurar destinos
description: Este procedimiento muestra cómo configurar y usar diferentes destinos para componentes de salida de informes electrónicos, como una carpeta o un archivo.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbef5410d0e6f15fbb5025f3831486d55cd06216
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185069"
---
# <a name="er-configure-destinations"></a><span data-ttu-id="fcf8c-103">ER Configurar destinos</span><span class="sxs-lookup"><span data-stu-id="fcf8c-103">ER Configure destinations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fcf8c-104">Este procedimiento muestra cómo configurar y usar diferentes destinos para componentes de salida de informes electrónicos, como una carpeta o un archivo.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-104">This procedure demonstrates how to set up and use different destinations for Electronic reporting (ER) output components, such as a folder or a file.</span></span> <span data-ttu-id="fcf8c-105">La empresa de datos de demostración utilizada para crear este procedimiento es DEMF.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-105">The demo data company used to create this procedure is DEMF.</span></span> <span data-ttu-id="fcf8c-106">Alemania es el país o región de la dirección principal de la entidad jurídica. Sin embargo, puede usar cualquier entidad jurídica para este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-106">Germany is the country\region of the legal entity’s primary address, however you can use any legal entity for this procedure.</span></span> 

<span data-ttu-id="fcf8c-107">El formato que se usa en este ejemplo es ISO20022 Transferencia de crédito, pero puede usar cualquier formato que ya haya importado.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-107">The format used in this example is ISO20022 Credit transfer, but you can use any format that you have already imported.</span></span> <span data-ttu-id="fcf8c-108">Tenga en cuenta que este procedimiento es un ejemplo de una configuración de destino y archivo único.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-108">Note, this procedure is an example of a single file and a single destination setup.</span></span> <span data-ttu-id="fcf8c-109">Encontrará más información acerca de la gestión de destinos de informes electrónicos en la Ayuda de Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-109">More information about Electronic reporting destination management can be found in the Dynamics 365 Finance Help.</span></span>

1. <span data-ttu-id="fcf8c-110">Vaya a Administración de la organización > Informes electrónicos > Destino de informes electrónicos.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-110">Go to Organization administration > Electronic reporting > Electronic reporting destination.</span></span>
2. <span data-ttu-id="fcf8c-111">Haga clic en Nuevo para crear un nuevo conjunto de destinos para un formato.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-111">Click New to create a new set of destinations for a format.</span></span>
3. <span data-ttu-id="fcf8c-112">En el campo Referencia, seleccione un formato para el que desea configurar destinos.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-112">In the Reference field, select a format for which you want to configure destinations.</span></span>
    * <span data-ttu-id="fcf8c-113">Si no tiene un valor para seleccionarlo, significa que no ha importado ninguna configuración de formato de informes electrónicos.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-113">If you don't have a value to select, it means that you have not imported any Electronic reporting format configurations.</span></span> <span data-ttu-id="fcf8c-114">Debe importar una configuración de formato antes de configurar destinos.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-114">You must import a format configuration before setting up destinations.</span></span>  
4. <span data-ttu-id="fcf8c-115">Haga clic en Nuevo para crear un nuevo destino de archivo.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-115">Click New to create a new file destination.</span></span>
    * <span data-ttu-id="fcf8c-116">Tenga en cuenta que puede crear un destino de archivo para cada componente de salida del mismo formato, como una carpeta o un archivo.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-116">Note, you can create one file destination for each output component of the same format, such as a folder or a file.</span></span> <span data-ttu-id="fcf8c-117">Podrá habilitar y deshabilitar destinos de forma independiente en los ajustes.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-117">You will be able to enable and disable destinations separately in the settings.</span></span>  
5. <span data-ttu-id="fcf8c-118">En el campo Nombre, especifique el nombre sencillo del componente de salida.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-118">In the Name field, enter the user-friendly name of output component.</span></span>
    * <span data-ttu-id="fcf8c-119">Se recomienda usar nombres significativos, como "Archivo de pago" o "Informe de control".</span><span class="sxs-lookup"><span data-stu-id="fcf8c-119">We recommend that you use meaningful names, such as "Payment file" or "Control report".</span></span> <span data-ttu-id="fcf8c-120">Estos nombres se presentarán a los usuarios en tiempo de ejecución de la configuración junto con la configuración del destino.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-120">These names will be presented to users at configuration runtime along with the destination settings.</span></span>  
6. <span data-ttu-id="fcf8c-121">En el Nombre de archivo, seleccione un archivo o una carpeta específicos para el formato.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-121">In the File name, select a file or folder that is specific to the format.</span></span>
7. <span data-ttu-id="fcf8c-122">Haga clic en Configuración.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-122">Click Settings.</span></span>
8. <span data-ttu-id="fcf8c-123">Seleccione Sí en el campo Habilitado.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-123">Select Yes in the Enabled field.</span></span>
    * <span data-ttu-id="fcf8c-124">La casilla Habilitada de cada ficha habilita y deshabilita cada destino por separado.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-124">The Enabled check box on each tab enables and disables each destination separately.</span></span> <span data-ttu-id="fcf8c-125">En este ejemplo, habilitará el envío de un archivo de salida a un destinatario de correo cuando se genere el archivo.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-125">In this example, you'll enable sending an output file to a mail recipient when the file is generated.</span></span>  
9. <span data-ttu-id="fcf8c-126">Haga clic en Editar para configurar los destinatarios de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-126">Click Edit, to set up email recipients.</span></span>
10. <span data-ttu-id="fcf8c-127">Haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-127">Click Add.</span></span>
11. <span data-ttu-id="fcf8c-128">Haga clic en Correo electrónico de administración de impresión.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-128">Click Print Management email.</span></span>
12. <span data-ttu-id="fcf8c-129">En el campo Origen de correo electrónico, seleccione una opción.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-129">In the Email source  field, select an option.</span></span>
    * <span data-ttu-id="fcf8c-130">Puede seleccionar diferentes tipos de origen de correo electrónico, como un cliente o un tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-130">You can select different email source types, such as a customer or a vendor type.</span></span> <span data-ttu-id="fcf8c-131">Esto define el tipo de argumento que devolverá la fórmula de la cuenta de origen del correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-131">This defines the type of argument that will be returned by the Email source account formula.</span></span> <span data-ttu-id="fcf8c-132">La fórmula de la cuenta de origen del correo electrónico, descrita en el paso siguiente, es donde enlazará un origen de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-132">The Email source account formula, described in a following step, is the place where you bind an email source.</span></span> <span data-ttu-id="fcf8c-133">Seleccione Proveedor si la fórmula devolverá una cuenta de proveedor.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-133">Select Vendor if your formula will return a vendor account.</span></span> <span data-ttu-id="fcf8c-134">Use Proveedor si está usando el ejemplo de configuración ISO 20022 Transferencia de crédito.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-134">Use Vendor if you are using the ISO 20022 Credit Transfer configuration example.</span></span>  
13. <span data-ttu-id="fcf8c-135">Haga clic en el botón Enlazar origen de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-135">Click Email source bind button.</span></span>
14. <span data-ttu-id="fcf8c-136">En la Fórmula, especifique una referencia específica de documento para el tipo de parte que ha seleccionado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-136">In the Formula, enter a document-specific reference to a party type that you selected earlier.</span></span>
    * <span data-ttu-id="fcf8c-137">En lugar de escribir, puede encontrar un nodo del origen de datos que represente la cuenta de la parte y hacer clic en el botón Agregar origen de datos para actualizar la fórmula.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-137">Instead of typing, you can find a data source node that represents the party account, and click the Add data source button to update the formula.</span></span> <span data-ttu-id="fcf8c-138">Por ejemplo, si utiliza la configuración ISO 20022 Transferencia de crédito, el nodo que representa una cuenta de proveedor es "$PaymentsForCoveringLetter".Creditor.Identification.SourceID.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-138">For example, if you use the ISO 20022 Credit Transfer configuration, the node representing a vendor account is '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID.</span></span> <span data-ttu-id="fcf8c-139">De lo contrario, especifique cualquier valor de cadena, como "DE-001", para guardar una fórmula.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-139">Otherwise, enter any string value, such as "DE-001", to save a formula.</span></span>  
15. <span data-ttu-id="fcf8c-140">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-140">Click Save.</span></span>
16. <span data-ttu-id="fcf8c-141">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-141">Close the page.</span></span>
17. <span data-ttu-id="fcf8c-142">Haga clic en Editar para configurar los detalles de contacto de la parte.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-142">Click Edit to configure contact details for the party.</span></span>
18. <span data-ttu-id="fcf8c-143">Seleccione Sí en el campo Contacto principal.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-143">Select Yes in the Primary contact field.</span></span>
    * <span data-ttu-id="fcf8c-144">Puede usar diferentes opciones para indicar qué tipo de contacto de la parte se debe usar como dirección de correo electrónico para este destino.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-144">You may use different options to indicate what contact type of the party should be used as an email address for this destination.</span></span> <span data-ttu-id="fcf8c-145">En este ejemplo usaremos el contacto principal.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-145">We use primary contact in this example.</span></span>  
19. <span data-ttu-id="fcf8c-146">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="fcf8c-146">Click OK.</span></span>
20. <span data-ttu-id="fcf8c-147">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="fcf8c-147">Click OK.</span></span>
21. <span data-ttu-id="fcf8c-148">En el campo Asunto, escriba un valor.</span><span class="sxs-lookup"><span data-stu-id="fcf8c-148">In the Subject field, type a value.</span></span>
22. <span data-ttu-id="fcf8c-149">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="fcf8c-149">Click OK.</span></span>
