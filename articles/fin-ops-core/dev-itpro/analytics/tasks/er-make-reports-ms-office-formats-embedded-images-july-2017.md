---
title: Diseñar configuraciones para generar informes en los formatos de Office que tengan imágenes incrustadas
description: Los pasos de este tema proporcionan información sobre cómo diseñar las configuraciones de informes electrónicos (ER) que generen documentos electrónicos en formatos de Microsoft Office (Excel y Word) que contienen imágenes incrustadas.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143782413359d87f3d4c46940f9a699fbf0e8f90
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769818"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="33a47-103">Diseñar configuraciones para generar informes en los formatos de Office que tengan imágenes incrustadas</span><span class="sxs-lookup"><span data-stu-id="33a47-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33a47-104">Para completar los pasos de este procedimiento, primero complete el procedimiento, "ER: Crear un proveedor de configuraciones y marcarlo como activo".</span><span class="sxs-lookup"><span data-stu-id="33a47-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="33a47-105">Este procedimiento explica cómo diseñar las configuraciones de informes electrónicos (ER) para generar documentos de Microsoft Excel o Word que contienen imágenes incrustadas.</span><span class="sxs-lookup"><span data-stu-id="33a47-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="33a47-106">En este procedimiento, creará las configuraciones de ER necesarias para la empresa de ejemplo, Litware, Inc. Estos pasos se pueden completar mediante el conjunto de datos de USMF.</span><span class="sxs-lookup"><span data-stu-id="33a47-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="33a47-107">Este procedimiento se ha creado para los usuarios con los roles Administrador del sistema o Desarrollador de informes electrónicos asignados.</span><span class="sxs-lookup"><span data-stu-id="33a47-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="33a47-108">Antes de empezar, descargue y guarde los archivos que aparecen en el tema de Ayuda [Insertar imágenes y formas en documentos que genera mediante ER](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="33a47-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="33a47-109">Los archivos son: modelo Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png y Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="33a47-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="33a47-110">Comprobar los requisitos previos</span><span class="sxs-lookup"><span data-stu-id="33a47-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="33a47-111">Vaya a Administración de la organización > Espacios de trabajo > Informes electrónicos.</span><span class="sxs-lookup"><span data-stu-id="33a47-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="33a47-112">Asegúrese de que el proveedor de configuración de la empresa de ejemplo “Litware, Inc.” está disponible y marcado como Activo.</span><span class="sxs-lookup"><span data-stu-id="33a47-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="33a47-113">Si no ve a este proveedor de configuración, complete los pasos del procedimiento "Creación de un proveedor de configuración y marcarlo como activo".</span><span class="sxs-lookup"><span data-stu-id="33a47-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="33a47-114">Haga clic en Configuraciones de informes.</span><span class="sxs-lookup"><span data-stu-id="33a47-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="33a47-115">Añada una nueva configuración para el modelo ER</span><span class="sxs-lookup"><span data-stu-id="33a47-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="33a47-116">En lugar de crear un nuevo modelo, puede cargar el archivo de configuración del modelo de ER (modelo para cheques.xml) que se guardó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="33a47-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="33a47-117">Este archivo contiene el modelo de datos de ejemplo para los cheques de pago y la asignación de modelo de datos a los componentes de datos de la aplicación Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="33a47-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="33a47-118">En las versiones de ficha desplegable, haga clic en Exchange.</span><span class="sxs-lookup"><span data-stu-id="33a47-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="33a47-119">Haga clic en Cargar desde un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="33a47-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="33a47-120">Haga clic en Examinar, y seleccione el modelo para cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="33a47-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="33a47-121">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="33a47-121">Click OK.</span></span>  
 6. <span data-ttu-id="33a47-122">El modelo cargado se utilizará como origen de datos de la información para generar documentos que contengan imágenes en Excel y Word.</span><span class="sxs-lookup"><span data-stu-id="33a47-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="33a47-123">Añada una nueva configuración para el formato de ER</span><span class="sxs-lookup"><span data-stu-id="33a47-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="33a47-124">En lugar de crear un nuevo formato, puede cargar el archivo de configuración del formato de ER (formato de impresión de cheques .xml) que guardó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="33a47-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="33a47-125">Este archivo contiene el diseño de ejemplo de formato para imprimir cheques utilizando el formulario preimpreso y la asignación de este formato al modelo de datos “modelo para cheques”.</span><span class="sxs-lookup"><span data-stu-id="33a47-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="33a47-126">Haga clic en Intercambiar.</span><span class="sxs-lookup"><span data-stu-id="33a47-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="33a47-127">Haga clic en Cargar desde un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="33a47-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="33a47-128">Haga clic en Examinar y seleccione el archivo Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="33a47-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="33a47-129">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="33a47-129">Click OK.</span></span>  
 6. <span data-ttu-id="33a47-130">En el árbol, expanda "Modelo para cheques".</span><span class="sxs-lookup"><span data-stu-id="33a47-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="33a47-131">En el árbol, seleccione "Modelo para cheques\Formato de impresión de cheques".</span><span class="sxs-lookup"><span data-stu-id="33a47-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="33a47-132">El formato cargado se utilizará para generar documentos que contengan imágenes en Excel y Word.</span><span class="sxs-lookup"><span data-stu-id="33a47-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="33a47-133">Configurar los parámetros de usuario de ER</span><span class="sxs-lookup"><span data-stu-id="33a47-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="33a47-134">En el panel de acciones, haga clic en Configuraciones.</span><span class="sxs-lookup"><span data-stu-id="33a47-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="33a47-135">Haga clic en Parámetros de usuario.</span><span class="sxs-lookup"><span data-stu-id="33a47-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="33a47-136">Seleccione Sí en el campo Parámetros de ejecución.</span><span class="sxs-lookup"><span data-stu-id="33a47-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="33a47-137">Desconecte el indicador de ejecución de borrador para iniciar la versión de borrador del formato seleccionado en lugar del completado.</span><span class="sxs-lookup"><span data-stu-id="33a47-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="33a47-138">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="33a47-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="33a47-139">Configure los parámetros de administración de efectivo y bancos</span><span class="sxs-lookup"><span data-stu-id="33a47-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="33a47-140">Vaya a Gestión de efectivo y de banco > Cuentas bancarias > Cuentas bancarias.</span><span class="sxs-lookup"><span data-stu-id="33a47-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="33a47-141">Use un filtro rápido para filtrar por el campo Cuenta bancaria, por el valor ''USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="33a47-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="33a47-142">En el panel de acciones, haga clic en Configurar.</span><span class="sxs-lookup"><span data-stu-id="33a47-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="33a47-143">Haga clic en Comprobar.</span><span class="sxs-lookup"><span data-stu-id="33a47-143">Click Check.</span></span>  
 5. <span data-ttu-id="33a47-144">Expanda la sección Configuración.</span><span class="sxs-lookup"><span data-stu-id="33a47-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="33a47-145">Haga clic en Editar.</span><span class="sxs-lookup"><span data-stu-id="33a47-145">Click Edit.</span></span>  
 7. <span data-ttu-id="33a47-146">Seleccione Sí en el campo Logotipo de la empresa.</span><span class="sxs-lookup"><span data-stu-id="33a47-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="33a47-147">Haga clic en Logotipo de la empresa.</span><span class="sxs-lookup"><span data-stu-id="33a47-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="33a47-148">Haga clic en Cambiar.</span><span class="sxs-lookup"><span data-stu-id="33a47-148">Click Change.</span></span>  
 10. <span data-ttu-id="33a47-149">Haga clic Examinar y seleccione el archivo que ha descargado anteriormente, Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="33a47-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="33a47-150">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="33a47-150">Click Save.</span></span>  
 12. <span data-ttu-id="33a47-151">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="33a47-151">Close the page.</span></span>  
 13. <span data-ttu-id="33a47-152">Expanda la sección Firma.</span><span class="sxs-lookup"><span data-stu-id="33a47-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="33a47-153">Seleccione Sí en el campo Imprimir la primera firma.</span><span class="sxs-lookup"><span data-stu-id="33a47-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="33a47-154">Haga clic en Cambiar.</span><span class="sxs-lookup"><span data-stu-id="33a47-154">Click Change.</span></span>  
 16. <span data-ttu-id="33a47-155">Haga clic Examinar y seleccione el archivo que ha descargado anteriormente, Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="33a47-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="33a47-156">Expanda la sección Copias.</span><span class="sxs-lookup"><span data-stu-id="33a47-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="33a47-157">En el campo Marca de agua, seleccione una opción.</span><span class="sxs-lookup"><span data-stu-id="33a47-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="33a47-158">Seleccione Sí en el campo Formato de exportación electrónica genérica.</span><span class="sxs-lookup"><span data-stu-id="33a47-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="33a47-159">Seleccione la configuración "Cheques printing form".</span><span class="sxs-lookup"><span data-stu-id="33a47-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="33a47-160">Ahora el formato seleccionado de ER se usará para imprimir los cheques.</span><span class="sxs-lookup"><span data-stu-id="33a47-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="33a47-161">Haga clic en Vincular.</span><span class="sxs-lookup"><span data-stu-id="33a47-161">Click Attach.</span></span>  
 23. <span data-ttu-id="33a47-162">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="33a47-162">Click New.</span></span>  
 24. <span data-ttu-id="33a47-163">Haga clic en Archivo.</span><span class="sxs-lookup"><span data-stu-id="33a47-163">Click File.</span></span>  
 25. <span data-ttu-id="33a47-164">Haga clic Examinar y seleccione el archivo que ha descargado anteriormente, Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="33a47-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="33a47-165">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="33a47-165">Close the page.</span></span>  
 27. <span data-ttu-id="33a47-166">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="33a47-166">Close the page.</span></span>  
 28. <span data-ttu-id="33a47-167">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="33a47-167">Close the page.</span></span>  
 29. <span data-ttu-id="33a47-168">Vaya a Gestión de efectivo y bancos > Configurar > Parámetros de gestión de efectivo y bancos.</span><span class="sxs-lookup"><span data-stu-id="33a47-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="33a47-169">Seleccione Sí en el campo Permitir la creación de validaciones de cuenta en cuentas bancarias inactivas:.</span><span class="sxs-lookup"><span data-stu-id="33a47-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="33a47-170">Haga clic en Guardar.</span><span class="sxs-lookup"><span data-stu-id="33a47-170">Click Save.</span></span>  
 32. <span data-ttu-id="33a47-171">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="33a47-171">Close the page.</span></span>  