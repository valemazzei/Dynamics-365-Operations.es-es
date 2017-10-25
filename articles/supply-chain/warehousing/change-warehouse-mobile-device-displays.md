---
title: "Configuración de visualización del dispositivo móvil del almacén"
description: "Este artículo describe cómo configurar el aspecto de una visualización del dispositivo móvil y cómo asignar teclas de método abreviado a controles, como botones."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 799cd4a940813e39f8be6b4c127b9efabc88e909
ms.contentlocale: es-es
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-mobile-device-display-settings"></a><span data-ttu-id="009ad-103">Configuración de visualización del dispositivo móvil del almacén</span><span class="sxs-lookup"><span data-stu-id="009ad-103">Warehouse mobile device display settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="009ad-104">Este artículo describe cómo configurar el aspecto de una visualización del dispositivo móvil y cómo asignar teclas de método abreviado a controles, como botones.</span><span class="sxs-lookup"><span data-stu-id="009ad-104">This article describes how to set up the appearance of a mobile device display and map keyboard shortcuts to controls such as buttons.</span></span> 

<span data-ttu-id="009ad-105">Este artículo se aplica a las características "almacenamiento avanzado" en gestión de almacenes.</span><span class="sxs-lookup"><span data-stu-id="009ad-105">This article applies to "advanced warehousing" features in Warehouse management.</span></span> <span data-ttu-id="009ad-106">Los dispositivos móviles se pueden usar para muchas de las tareas que los trabajadores de almacén realizan.</span><span class="sxs-lookup"><span data-stu-id="009ad-106">Mobile devices can be used for many of the tasks that warehouse workers perform.</span></span>

## <a name="specify-styles-and-map-keyboard-shortcuts"></a><span data-ttu-id="009ad-107">Especificar los estilos y asignar los métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="009ad-107">Specify styles and map keyboard shortcuts</span></span>
<span data-ttu-id="009ad-108">Como parte de la configuración del dispositivo móvil, puede definir diseños diferentes para los dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="009ad-108">As part of the mobile device configuration, you can define different layouts for mobile devices.</span></span> <span data-ttu-id="009ad-109">Para ello, debe conocer el nombre del archivo de hojas de estilo CSS y el archivo de extensión de página Active server (ASPX).</span><span class="sxs-lookup"><span data-stu-id="009ad-109">To do this, you must know the name of the Cascading Style Sheets (CSS) file and the Active Server Page Extension (ASPX) file.</span></span> <span data-ttu-id="009ad-110">Los archivos predeterminados se instalan como parte de la instalación del portal de los dispositivos móviles de almacén.</span><span class="sxs-lookup"><span data-stu-id="009ad-110">Default files are installed as part of the Warehouse Mobile Devices Portal installation.</span></span> <span data-ttu-id="009ad-111">Si no conoce los nombres de archivo, pregunte al administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="009ad-111">If you don’t know the file names, ask your system administrator.</span></span> <span data-ttu-id="009ad-112">Puede definir un nuevo estilo en la página **Configuración de visualización del dispositivo móvil**:</span><span class="sxs-lookup"><span data-stu-id="009ad-112">You can define a new style on the **Mobile device display settings** page:</span></span>

-    <span data-ttu-id="009ad-113">En el campo **archivo CSS**, escriba el nombre del archivo CSS.</span><span class="sxs-lookup"><span data-stu-id="009ad-113">In the **CSS file** field, enter the name of your CSS file.</span></span> <span data-ttu-id="009ad-114">Incluya la extensión del nombre del archivo .css.</span><span class="sxs-lookup"><span data-stu-id="009ad-114">Include the .css file name extension.</span></span>
-   <span data-ttu-id="009ad-115">En el campo **Vista de los valores de visualización del dispositivo móvil**, especifique el archivo ASPX.</span><span class="sxs-lookup"><span data-stu-id="009ad-115">In the **Mobile device display settings view** field, specify the ASPX file.</span></span> <span data-ttu-id="009ad-116">**No** incluya la extensión de nombre del archivo .aspx.</span><span class="sxs-lookup"><span data-stu-id="009ad-116">Do **not** include the .aspx file name extension.</span></span>

<span data-ttu-id="009ad-117">Los archivos CSS y ASPX deben estar situados en un directorio específico, de modo que la solicitud de los servicios de información de Internet (IIS) puedan cargarlos.</span><span class="sxs-lookup"><span data-stu-id="009ad-117">The CSS and ASPX files must be located in a specific directory, so that the Internet Information Services (IIS) application can load them.</span></span> <span data-ttu-id="009ad-118">Puede ser útil definir distintos archivos CSS si está ejecutando la función del dispositivo móvil en diferentes exploradores o en diferentes tipos de hardware que requieren varios controles de diseño.</span><span class="sxs-lookup"><span data-stu-id="009ad-118">It might be useful to define different CSS files if you're running the mobile device functionality in different browsers or on different kinds of hardware that require different layout control.</span></span> <span data-ttu-id="009ad-119">Ajustes simples como el color de fondo, la fuente y el tamaño de fuente para el texto, y el ancho y el comportamiento de los botones, se pueden controlar fácilmente usando de manera diferente los archivos CSS.</span><span class="sxs-lookup"><span data-stu-id="009ad-119">Simple settings such as the background color, the font and font size for text, and the width and behavior of buttons, can easily be controlled by different use of CSS files.</span></span> <span data-ttu-id="009ad-120">El archivo ASPX se utiliza para mostrar el sitio móvil en la solicitud del servidor ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="009ad-120">The ASPX file is used to display the mobile site on the server-side ASP.NET application.</span></span> <span data-ttu-id="009ad-121">El archivo controla la manera en que se diseña la estructura general del HTML. Conviene personalizar esta funcionalidad solo si tiene problemas estructurales serios con HTML y JavaScript, y debe cambiar este código para los dispositivos específicos.</span><span class="sxs-lookup"><span data-stu-id="009ad-121">The file controls how the overall structure of the HTML is laid out. It's a good idea to customize this functionality only if you have serious structural issues with the HTML and JavaScript, and must change this code for your specific devices.</span></span> <span data-ttu-id="009ad-122">Para asignar los controles de HTML en la página del dispositivo móvil a los métodos abreviados de teclado, en la página **Valores de visualización del dispositivo móvil**, en el campo **Métodos abreviados de teclado**, asigne códigos numéricos para las claves.</span><span class="sxs-lookup"><span data-stu-id="009ad-122">To map the HTML controls on the mobile device page to keyboard shortcuts, on the **Mobile device display settings** page, in the **Keyboard shortcut** field, assign the numeric codes for the keys.</span></span> <span data-ttu-id="009ad-123">Puede usar el menú **Ver códigos para los métodos abreviados de teclado** en el dispositivo móvil para encontrar los códigos de carácter numérico.</span><span class="sxs-lookup"><span data-stu-id="009ad-123">You can use the **View codes for keyboard shortcuts** menu on the mobile device to find the numeric character codes.</span></span> <span data-ttu-id="009ad-124">Tenga en cuenta que las asignaciones pueden variar, en función del hardware que se usa.</span><span class="sxs-lookup"><span data-stu-id="009ad-124">Note that the mappings might differ, depending on the hardware that is used.</span></span> <span data-ttu-id="009ad-125">Debe usar la siguiente sintaxis para crear la asignación:</span><span class="sxs-lookup"><span data-stu-id="009ad-125">You must use the following syntax to create the mapping:</span></span>

<span data-ttu-id="009ad-126">&lt;nombre de control&gt;(&lt;nombre de tecla&gt;)=&lt;código de tecla&gt;;</span><span class="sxs-lookup"><span data-stu-id="009ad-126">&lt;control name&gt;(&lt;key name&gt;)=&lt;key code&gt;;</span></span>

<span data-ttu-id="009ad-127">Aquí hay una explicación de las partes de la sintaxis:</span><span class="sxs-lookup"><span data-stu-id="009ad-127">Here is an explanation of the parts of the syntax:</span></span>

-   <span data-ttu-id="009ad-128">**&lt;nombre de control&gt;**: el nombre del control (por ejemplo, un botón) que se representa en HTML.</span><span class="sxs-lookup"><span data-stu-id="009ad-128">**&lt;control name&gt;** – The name of the control (for example, a button) that is rendered in HTML.</span></span>
-   <span data-ttu-id="009ad-129">**(&lt;nombre de tecla&gt;)**: el nombre de la tecla de teclado para la que está creando el método abreviado.</span><span class="sxs-lookup"><span data-stu-id="009ad-129">**(&lt;key name&gt;)** – The name of the keyboard key that you’re creating the shortcut for.</span></span>
-   <span data-ttu-id="009ad-130">**&lt;Código de tecla&gt;**: el código de carácter numérico para la clave que desea utilizar como la tecla de método abreviado.</span><span class="sxs-lookup"><span data-stu-id="009ad-130">**&lt;Key code&gt;** – The numeric character code for the key to use as the shortcut key.</span></span>

<span data-ttu-id="009ad-131">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="009ad-131">Here is an example:</span></span>

<span data-ttu-id="009ad-132">Cancelar(Esc)=27; Full(F2)=113</span><span class="sxs-lookup"><span data-stu-id="009ad-132">Cancel(Esc)=27; Full(F2)=113</span></span>

<span data-ttu-id="009ad-133">En todas las páginas que incluyan el botón **Cancelar**, el botón tendrá este texto:</span><span class="sxs-lookup"><span data-stu-id="009ad-133">On all pages that include a **Cancel** button, the button will have this text:</span></span>

<span data-ttu-id="009ad-134">**(Esc) Cancelar**</span><span class="sxs-lookup"><span data-stu-id="009ad-134">**(Esc) Cancel**</span></span>

<span data-ttu-id="009ad-135">Al presionar la tecla ESC en el teclado, se activará el botón **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="009ad-135">Pressing the Esc key on the keyboard will activate the **Cancel** button.</span></span> <span data-ttu-id="009ad-136">Para aplicar los ajustes de estilo y métodos abreviados de teclado a un dispositivo específico, debe crear una asignación en el campo **Criterios**.</span><span class="sxs-lookup"><span data-stu-id="009ad-136">To apply the style and keyboard shortcut settings to a specific device, you must create a mapping in the **Criteria** field.</span></span> <span data-ttu-id="009ad-137">Debe usar una expresión regular de .NET para crear la asignación, y la expresión debe constar de tres seccionesseparadas por una barra vertical (|), como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="009ad-137">You must use a .NET regular expression to create the mapping, and the expression must consist of three sections that are separated by a vertical bar (|), as shown here:</span></span>

<span data-ttu-id="009ad-138">Request.UserHostAddress=&lt;dirección de host de usuario&gt;|HostName=&lt;nombre de host de usuario&gt;|Request.UserAgent=&lt;agente de usuario&gt;</span><span class="sxs-lookup"><span data-stu-id="009ad-138">Request.UserHostAddress=&lt;user host address&gt;|HostName=&lt;user host name&gt;|Request.UserAgent=&lt;user agent&gt;</span></span>

<span data-ttu-id="009ad-139">Aquí hay una explicación de las partes de la expresión:</span><span class="sxs-lookup"><span data-stu-id="009ad-139">Here is an explanation of the parts of the expression:</span></span>

-   <span data-ttu-id="009ad-140">**&lt;dirección de host de usuario&gt;**: una expresión regular de .NET que coincida con la dirección IP del solicitante.</span><span class="sxs-lookup"><span data-stu-id="009ad-140">**&lt;user host address&gt;** – A .NET regular expression that matches the requestor IP address.</span></span>
-   <span data-ttu-id="009ad-141">**&lt;nombre de host del usuario&gt;**: una expresión regular de .NET que coincida con el nombre de red del solicitante.</span><span class="sxs-lookup"><span data-stu-id="009ad-141">**&lt;user host name&gt;** – A .NET regular expression that matches the network name of the requestor.</span></span>
-   <span data-ttu-id="009ad-142">**&lt;agente de usuario&gt;**: una expresión regular de .NET que coincida con el identificador del explorador usada por el solicitante.</span><span class="sxs-lookup"><span data-stu-id="009ad-142">**&lt;user agent&gt;** – A .NET regular expression that matches the identifier of the browser that the requestor uses.</span></span>

<span data-ttu-id="009ad-143">En el siguiente ejemplo permite el uso de Internet Explorer 8:</span><span class="sxs-lookup"><span data-stu-id="009ad-143">The following example enables Internet Explorer 8 to be used:</span></span>

<span data-ttu-id="009ad-144">Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0</span><span class="sxs-lookup"><span data-stu-id="009ad-144">Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0</span></span>

<span data-ttu-id="009ad-145">Puede usar el menú **Configuración del servidor de visualización para los valores de visualización** en el dispositivo móvil para buscar información acerca de la configuración.</span><span class="sxs-lookup"><span data-stu-id="009ad-145">You can use the **View server configuration for display settings** menu on the mobile device to find the information about the setup.</span></span>

## <a name="define-text-colors-for-messages"></a><span data-ttu-id="009ad-146">Definir los colores de texto para los mensajes</span><span class="sxs-lookup"><span data-stu-id="009ad-146">Define text colors for messages</span></span>
<span data-ttu-id="009ad-147">Puede usar la página**Colores de texto del dispositivo móvil** para controlar los distintos los colores que se usan en los mensajes generados del sistema, como mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="009ad-147">You can use the **Mobile device text colors** page to control the various colors that are used in system-generated messages, such as error messages.</span></span> <span data-ttu-id="009ad-148">Por ejemplo, el color de texto puede indicar el propósito o la gravedad del mensaje.</span><span class="sxs-lookup"><span data-stu-id="009ad-148">For example, the text color can indicate the purpose or severity of the message.</span></span> <span data-ttu-id="009ad-149">Están disponibles los siguientes tipos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="009ad-149">The following types of messages are shown.</span></span>

| <span data-ttu-id="009ad-150">Tipo de mensaje</span><span class="sxs-lookup"><span data-stu-id="009ad-150">Message type</span></span> | <span data-ttu-id="009ad-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="009ad-151">Description</span></span>                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="009ad-152">Predeterminada</span><span class="sxs-lookup"><span data-stu-id="009ad-152">Default</span></span>      | <span data-ttu-id="009ad-153">Los mensajes predeterminados usan los ajustes de color predeterminados para todos los mensajes, según lo especificado por el archivo CSS para el portal del dispositivo móvil del almacén.</span><span class="sxs-lookup"><span data-stu-id="009ad-153">Default messages use the default color settings for all messages, as defined by the CSS file for the Warehouse Mobile Device Portal.</span></span>                                                   |
| <span data-ttu-id="009ad-154">Error</span><span class="sxs-lookup"><span data-stu-id="009ad-154">Error</span></span>        | <span data-ttu-id="009ad-155">Los mensajes de error indican un problema que el usuario debe resolver antes de que pueda continuar.</span><span class="sxs-lookup"><span data-stu-id="009ad-155">Error messages indicate an issue that the user must resolve before he or she can continue.</span></span>                                                                                             |
| <span data-ttu-id="009ad-156">Satisfactorio</span><span class="sxs-lookup"><span data-stu-id="009ad-156">Success</span></span>      | <span data-ttu-id="009ad-157">Los mensajes de éxito confirman que una acción es correcta.</span><span class="sxs-lookup"><span data-stu-id="009ad-157">Success messages confirm that an action was successful.</span></span>                                                                                                                                |
| <span data-ttu-id="009ad-158">Advertencia</span><span class="sxs-lookup"><span data-stu-id="009ad-158">Warning</span></span>      | <span data-ttu-id="009ad-159">Los mensajes de advertencia notifican al trabajador que hay un problema, o que podría haber un problema si el trabajador continúa.</span><span class="sxs-lookup"><span data-stu-id="009ad-159">Warning messages inform the worker that there is an issue, or that there could be an issue if the worker continues.</span></span> <span data-ttu-id="009ad-160">Sin embargo, el trabajador no tiene que resolver el problema para continuar.</span><span class="sxs-lookup"><span data-stu-id="009ad-160">However, the worker doesn't have to resolve the issue to continue.</span></span> |

<span data-ttu-id="009ad-161">Para seleccionar el color, en la página **Seleccionar color**, haga clic en la paleta o escriba un código de color hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="009ad-161">To select the color, on the **Select color** page, click in the palette or type a hexadecimal color code.</span></span>

## <a name="define-the-date-format-to-use-on-mobile-devices"></a><span data-ttu-id="009ad-162">Definir el formato de fecha para usar en los dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="009ad-162">Define the date format to use on mobile devices</span></span>
<span data-ttu-id="009ad-163">Puede ampliar la lista de formatos de fecha aceptados para cada instalación.</span><span class="sxs-lookup"><span data-stu-id="009ad-163">You can extend the list of accepted date formats for each installation.</span></span> <span data-ttu-id="009ad-164">Esta capacidad puede resultar útil si, por ejemplo, desea proporcionar un formato que haga más fácil al trabajador la especificación de fechas en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="009ad-164">This capability can be useful if, for example, you want to provide a format that makes it easier for a worker to enter dates on a mobile device.</span></span> <span data-ttu-id="009ad-165">El formato predeterminado viene determinado por el idioma predeterminado del usuario, que se especifica en el campo **Opciones de usuario** de la página **Idioma**.</span><span class="sxs-lookup"><span data-stu-id="009ad-165">The default format is determined by the user's default language, which is specified in the **Language** field on the **User options** page.</span></span> <span data-ttu-id="009ad-166">(La misma página también se usa para asociar a un empleado con un usuario específico de trabajo de almacén). **Nota:** El portal de dispositivos móviles de almacén no usa el valor del campo **Formato de fecha y hora de número** en la página **Preferencia de idiomas y región**.</span><span class="sxs-lookup"><span data-stu-id="009ad-166">(The same page is also used to associate an employee with a specific warehouse work user.) **Note:** The Warehouse Mobile Devices Portal doesn't use the setting of the **Date time and number format** field on the **Language and region preferences** page.</span></span> <span data-ttu-id="009ad-167">Para cambiar un formato de fecha, debe estar familiarizado con expresiones regulares en .NET Framework de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="009ad-167">To change a date format, you must be familiar with regular expressions in the Microsoft .NET Framework.</span></span> <span data-ttu-id="009ad-168">Para obtener más información, consulte [Expresiones regulares de .Net Framework](http://go.microsoft.com/fwlink/?LinkId=391260).</span><span class="sxs-lookup"><span data-stu-id="009ad-168">For more information, see [.NET Framework Regular Expressions](http://go.microsoft.com/fwlink/?LinkId=391260).</span></span> <span data-ttu-id="009ad-169">Para definir formatos de fecha, edite el archivo Dates.ini que se encuentra en Content\\Settings\\Dates.ini en el servidor del portal de dispositivos móviles de almacén.</span><span class="sxs-lookup"><span data-stu-id="009ad-169">To define date formats, edit the Dates.ini file that is located at Content\\Settings\\Dates.ini on the Warehouse Mobile Devices Portal server.</span></span> <span data-ttu-id="009ad-170">Este archivo usa expresiones regulares de .NET para especificar el formato de fecha.</span><span class="sxs-lookup"><span data-stu-id="009ad-170">This file uses .NET regular expressions to specify the date format.</span></span> <span data-ttu-id="009ad-171">La expresión regular debe contener las subexpresiones que crean grupos denominados por día, mes y año (DDMMYY), tal y como se muestra en el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="009ad-171">The regular expression must contain subexpressions that create named groups for day, month, and year (DDMMYY), as shown in the following example:</span></span>

<span data-ttu-id="009ad-172">^(?&lt;día&gt;\\d{2})(?&lt;mes&gt;\\d{2})(?&lt;año&gt;\\d{2})$</span><span class="sxs-lookup"><span data-stu-id="009ad-172">^(?&lt;day&gt;\\d{2})(?&lt;month&gt;\\d{2})(?&lt;year&gt;\\d{2})$</span></span>

<span data-ttu-id="009ad-173">Cada subexpression requiere de uno a dos dígitos para el día y el mes, y de uno a cuatro dígitos para el año.</span><span class="sxs-lookup"><span data-stu-id="009ad-173">Each subexpression requires one to two digits for the day and month, and one to four digits for the year.</span></span> <span data-ttu-id="009ad-174">Por ejemplo, la siguiente subexpresión define un grupo denominado para un año, y requiere un mínimo de dos dígitos o un máximo de cuatro dígitos:</span><span class="sxs-lookup"><span data-stu-id="009ad-174">For example, the following subexpression defines a named group for a year, and requires a minimum of two digits or a maximum of four digits:</span></span>

<span data-ttu-id="009ad-175">(?&lt;año&gt;\\d{2,4})</span><span class="sxs-lookup"><span data-stu-id="009ad-175">(?&lt;year&gt;\\d{2,4})</span></span>

<span data-ttu-id="009ad-176">Puede especificar más de una expresión en el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="009ad-176">You can specify more than one expression in the same file.</span></span> <span data-ttu-id="009ad-177">Cada expresión debe estar en una línea independiente.</span><span class="sxs-lookup"><span data-stu-id="009ad-177">Each expression must be on a separate line.</span></span> <span data-ttu-id="009ad-178">La primera expresión que coincida se usa para analizar la fecha.</span><span class="sxs-lookup"><span data-stu-id="009ad-178">The first expression that is matched is used to parse the date.</span></span>

<a name="see-also"></a><span data-ttu-id="009ad-179">Consulte también</span><span class="sxs-lookup"><span data-stu-id="009ad-179">See also</span></span>
--------

[<span data-ttu-id="009ad-180">Configuración de dispositivos móviles del trabajo de almacén</span><span class="sxs-lookup"><span data-stu-id="009ad-180">Configuration of mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)



