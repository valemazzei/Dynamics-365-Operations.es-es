---
title: Diseñar configuraciones de ER para generar informes en formato Word
description: En los pasos siguientes se explica cómo un usuario con rol de administrador del Sistema o de desarrollador de informes electrónicos puede configurar formatos de informes electrónicos para generar archivos de informes en Microsoft Word.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 327f03435ab55551953fd998dd89c831c76c4c26
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182609"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="16db3-103">Diseñar configuraciones de ER para generar informes en formato Word</span><span class="sxs-lookup"><span data-stu-id="16db3-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16db3-104">En los pasos siguientes se explica cómo un usuario con rol de administrador del Sistema o de desarrollador de informes electrónicos puede configurar formatos de informes electrónicos (ER) para generar archivos de informes en Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="16db3-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="16db3-105">Estos pasos se pueden llevar a cabo en la empresa GBSI.</span><span class="sxs-lookup"><span data-stu-id="16db3-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="16db3-106">Para completar estos pasos, primero debe completar los pasos en la guía de tarea "Crear una configuración de ER para generar informes en formato OPENXML”.</span><span class="sxs-lookup"><span data-stu-id="16db3-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="16db3-107">Previamente deberá descargar y guardar también las plantillas siguientes localmente para el informe de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="16db3-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="16db3-108">Plantilla de informe de pago</span><span class="sxs-lookup"><span data-stu-id="16db3-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="16db3-109">Plantilla enlazada de informe de pago</span><span class="sxs-lookup"><span data-stu-id="16db3-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="16db3-110">Este procedimiento es para una función que se ha agregado en la versión 1611 de Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="16db3-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="16db3-111">Seleccione la configuración existente del informe ER</span><span class="sxs-lookup"><span data-stu-id="16db3-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="16db3-112">En el **Panel de exploración, vaya a Módulos > Administración de la organización > Espacios de trabajo > Informes electrónicos**.</span><span class="sxs-lookup"><span data-stu-id="16db3-112">In the **Navigation pane, go to Modules > Organization administration > Workspaces > Electronic reporting**.</span></span> <span data-ttu-id="16db3-113">Asegúrese de que el proveedor de la configuración "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="16db3-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="16db3-114">está seleccionado como activo.</span><span class="sxs-lookup"><span data-stu-id="16db3-114">is selected as active.</span></span>  
2. <span data-ttu-id="16db3-115">Haga clic en **Configuraciones de informes**.</span><span class="sxs-lookup"><span data-stu-id="16db3-115">Click **Reporting configurations**.</span></span> <span data-ttu-id="16db3-116">Reutilizaremos la configuración actual de ER que se ha diseñado originalmente para generar la salida de informes en formato de OPENXML.</span><span class="sxs-lookup"><span data-stu-id="16db3-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="16db3-117">En el árbol, expanda "Modelo de pago".</span><span class="sxs-lookup"><span data-stu-id="16db3-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="16db3-118">En el árbol, seleccione "Modelo de pago\Informe de hoja de cálculo de muestra".</span><span class="sxs-lookup"><span data-stu-id="16db3-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="16db3-119">Haga clic en Diseñador.</span><span class="sxs-lookup"><span data-stu-id="16db3-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="16db3-120">Sustituya la plantilla de Excel con la plantilla de Word</span><span class="sxs-lookup"><span data-stu-id="16db3-120">Replace the Excel template with the Word template</span></span>

<span data-ttu-id="16db3-121">Actualmente, el documento de Excel se utiliza como plantilla para producir un resultado en formato de OPENXML.</span><span class="sxs-lookup"><span data-stu-id="16db3-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="16db3-122">Importaremos la plantilla del informe en formato de Word.</span><span class="sxs-lookup"><span data-stu-id="16db3-122">We will import the report’s template in Word format.</span></span>

1. <span data-ttu-id="16db3-123">Haga clic en **Archivos adjuntos**.</span><span class="sxs-lookup"><span data-stu-id="16db3-123">Click **Attachments**.</span></span> <span data-ttu-id="16db3-124">Sustituya la plantilla de Excel actual con la plantilla de Word que ha descargado anteriormente, SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="16db3-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="16db3-125">Tenga en cuenta que esta plantilla solo contiene el diseño del documento que deseamos generar como ER de salida.</span><span class="sxs-lookup"><span data-stu-id="16db3-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="16db3-126">Haga clic **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-126">Click **Delete**.</span></span>
3. <span data-ttu-id="16db3-127">Haga clic en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="16db3-127">Click **Yes**.</span></span>
4. <span data-ttu-id="16db3-128">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="16db3-128">Click **New**.</span></span>
5. <span data-ttu-id="16db3-129">Haga clic en **Archivo**.</span><span class="sxs-lookup"><span data-stu-id="16db3-129">Click **File**.</span></span>
6. <span data-ttu-id="16db3-130">Haga clic en **Examinar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-130">Click **Browse**.</span></span> <span data-ttu-id="16db3-131">Desplácese y seleccione SampleVendPaymDocReport.docx que ha descargado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="16db3-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="16db3-132">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-132">Click **OK**.</span></span> <span data-ttu-id="16db3-133">Seleccione la plantilla que ha descargado en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="16db3-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="16db3-134">En el campo **Plantilla**, especifique o seleccione un valor.</span><span class="sxs-lookup"><span data-stu-id="16db3-134">In the **Template** field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="16db3-135">Aumente la plantilla de Word agregando una parte del XML personalizado</span><span class="sxs-lookup"><span data-stu-id="16db3-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="16db3-136">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-136">Click **Save**.</span></span> <span data-ttu-id="16db3-137">Además de almacenar cambios de configuración, la acción Guardar también actualiza la plantilla de Word adjunta.</span><span class="sxs-lookup"><span data-stu-id="16db3-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="16db3-138">La estructura del formato diseñado se traslada al documento de Word adjunto como una nueva parte del XML personalizado con el nombre “Informe”.</span><span class="sxs-lookup"><span data-stu-id="16db3-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="16db3-139">Tenga en cuenta que la plantilla de Word adjunta no sólo contiene el diseño del documento que deseamos para generar como salida de ER, sino que también contiene la estructura de datos que el ER rellenará en esta plantilla en el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="16db3-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="16db3-140">Haga clic en **Archivos adjuntos**.</span><span class="sxs-lookup"><span data-stu-id="16db3-140">Click **Attachments**.</span></span>
    + <span data-ttu-id="16db3-141">Ahora necesita vincular los elementos de la parte XML personalizada del “Informe” a las partes del documento en Word.</span><span class="sxs-lookup"><span data-stu-id="16db3-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    + <span data-ttu-id="16db3-142">Si está familiarizado con los documentos de Word que se pueden diseñar como formularios que contienen los controles de contenido limitados con elementos de partes de XML personalizado: reproduzca todos los pasos de la subtarea siguiente para crear tal documento.</span><span class="sxs-lookup"><span data-stu-id="16db3-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="16db3-143">Para obtener más detalles, consulte [Crear formularios que los usuarios pueden rellenar o imprimir en Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="16db3-143">For more details, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US).</span></span> <span data-ttu-id="16db3-144">Si no, omita todos los pasos de la subtarea siguiente.</span><span class="sxs-lookup"><span data-stu-id="16db3-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="16db3-145">Consiga Word con la parte XML personalizada para realizar vínculos de datos</span><span class="sxs-lookup"><span data-stu-id="16db3-145">Get Word with custom XML part to do data bindings</span></span>

<span data-ttu-id="16db3-146">Abra este documento en Word y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="16db3-146">Open this document in Word and do the following:</span></span>  
1. <span data-ttu-id="16db3-147">Abra la pestaña Desarrollador de Word (personalice la cinta de opciones si no está aún habilitada).</span><span class="sxs-lookup"><span data-stu-id="16db3-147">Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>
2. <span data-ttu-id="16db3-148">Seleccione el panel de asignación XML.</span><span class="sxs-lookup"><span data-stu-id="16db3-148">Select XML mapping pane.</span></span>
3. <span data-ttu-id="16db3-149">Seleccione el elemento XML personalizado del “Informe” en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="16db3-149">Select the ‘Report’ custom XML part in the lookup.</span></span>
4. <span data-ttu-id="16db3-150">Haga la asignación de los artículos de la parte XML seleccionada y de los controles de contenido del documento de Word.</span><span class="sxs-lookup"><span data-stu-id="16db3-150">Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="16db3-151">5.</span><span class="sxs-lookup"><span data-stu-id="16db3-151">5.</span></span> <span data-ttu-id="16db3-152">Guarde el documento de Word actualizado en una unidad local.</span><span class="sxs-lookup"><span data-stu-id="16db3-152">Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="16db3-153">Cargue la plantilla de Word con la parte XML personalizada para limitada a los controles de contenido</span><span class="sxs-lookup"><span data-stu-id="16db3-153">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="16db3-154">Haga clic **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-154">Click **Delete**.</span></span>
2. <span data-ttu-id="16db3-155">Haga clic en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="16db3-155">Click **Yes**.</span></span> <span data-ttu-id="16db3-156">Agregar una plantilla nueva.</span><span class="sxs-lookup"><span data-stu-id="16db3-156">Add a new template.</span></span> <span data-ttu-id="16db3-157">Si ha completado los pasos de la subtarea anterior, seleccione el documento de Word que ha preparado y guardado en una unidad local.</span><span class="sxs-lookup"><span data-stu-id="16db3-157">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="16db3-158">Si no, seleccione la plantilla de MS Word SampleVendPaymDocReportBounded.docx que había descargado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="16db3-158">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="16db3-159">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="16db3-159">Click **New**.</span></span>
4. <span data-ttu-id="16db3-160">Haga clic en **Archivo**.</span><span class="sxs-lookup"><span data-stu-id="16db3-160">Click **File**.</span></span>
5. <span data-ttu-id="16db3-161">Haga clic en **Examinar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-161">Click **Browse**.</span></span> <span data-ttu-id="16db3-162">Desplácese y seleccione el SampleVendPaymDocReportBounded.docx que ha descargado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="16db3-162">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="16db3-163">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-163">Click **OK**.</span></span>
6. <span data-ttu-id="16db3-164">En el campo **Plantilla**, seleccione el documento que ha descargado en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="16db3-164">In the **Template** field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="16db3-165">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-165">Click **Save**.</span></span>
8. <span data-ttu-id="16db3-166">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="16db3-166">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="16db3-167">Ejecute el formato para crear una salida en Word</span><span class="sxs-lookup"><span data-stu-id="16db3-167">Execute the format to create Word output</span></span>
1. <span data-ttu-id="16db3-168">En el **panel de acciones**, haga clic en **Configuraciones**.</span><span class="sxs-lookup"><span data-stu-id="16db3-168">On the **Action Pane**, click **Configurations**.</span></span>
2. <span data-ttu-id="16db3-169">Haga clic en **Parámetros de usuario**.</span><span class="sxs-lookup"><span data-stu-id="16db3-169">Click **User parameters**.</span></span>
3. <span data-ttu-id="16db3-170">Seleccione Sí en el campo **Parámetros de ejecución**.</span><span class="sxs-lookup"><span data-stu-id="16db3-170">Select Yes in the **Run settings** field.</span></span>
4. <span data-ttu-id="16db3-171">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-171">Click **OK**.</span></span>
5. <span data-ttu-id="16db3-172">Haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-172">Click **Edit**.</span></span>
6. <span data-ttu-id="16db3-173">Seleccione Sí en el campo **Borrador de ejecución**.</span><span class="sxs-lookup"><span data-stu-id="16db3-173">Select Yes in the **Run Draft** field.</span></span>
7. <span data-ttu-id="16db3-174">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-174">Click **Save**.</span></span>
8. <span data-ttu-id="16db3-175">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="16db3-175">Close the page.</span></span>
9. <span data-ttu-id="16db3-176">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="16db3-176">Close the page.</span></span>
10. <span data-ttu-id="16db3-177">En el **Panel de exploración**, vaya a **Módulos > Proveedores > Pagos > Diario de pagos**.</span><span class="sxs-lookup"><span data-stu-id="16db3-177">In the **Navigation pane**, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
11. <span data-ttu-id="16db3-178">Haga clic en **Líneas**.</span><span class="sxs-lookup"><span data-stu-id="16db3-178">Click **Lines**.</span></span>
12. <span data-ttu-id="16db3-179">En la lista, active o desactive todas las filas.</span><span class="sxs-lookup"><span data-stu-id="16db3-179">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="16db3-180">Haga clic en **Estado de pago**.</span><span class="sxs-lookup"><span data-stu-id="16db3-180">Click **Payment status**.</span></span>
14. <span data-ttu-id="16db3-181">Haga clic en **Ninguno**.</span><span class="sxs-lookup"><span data-stu-id="16db3-181">Click **None**.</span></span>
15. <span data-ttu-id="16db3-182">Haga clic en **Generar pagos**.</span><span class="sxs-lookup"><span data-stu-id="16db3-182">Click **Generate payments**.</span></span>
16. <span data-ttu-id="16db3-183">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-183">Click **OK**.</span></span>
17. <span data-ttu-id="16db3-184">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="16db3-184">Click **OK**.</span></span> <span data-ttu-id="16db3-185">Analice la salida generada.</span><span class="sxs-lookup"><span data-stu-id="16db3-185">Analyze the generated output.</span></span> <span data-ttu-id="16db3-186">Tenga en cuenta que la salida creada se presenta en formato de Word y contiene los detalles de los pagos procesados.</span><span class="sxs-lookup"><span data-stu-id="16db3-186">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  
