---
title: "Configurar un catálogo externo para la adquisición electrónica de marcaje de salida"
description: "Este tema describe el uso de un catálogo externo o del catálogo de marcaje de salida para recopilar información de presupuestos de un proveedor y añadirla a una solicitud."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 2d853cb963471f81d7a2a09a0f7913722de8a417
ms.contentlocale: es-es
ms.lasthandoff: 06/20/2017


---

# Configurar un catálogo externo para la adquisición electrónica de marcaje de salida
<a id="set-up-an-external-catalog-for-punchout-eprocurement" class="xliff"></a>

Usando el catálogo externo, puede asegurarse de que la información del producto y de precios que procese posteriormente en Dynamics 365 for Finance and Operations, Edición Enterprise de julio de 2017 sea precisa y actualizada. La solicitud puede aprobarse y convertirse en un pedido de compra y se puede presentar el pedido al proveedor.

Cuando el catálogo externo se configura y un empleado está preparando una solicitud, habrá una opción para redirigir a un sitio externo, el catálogo externo, y devolver la cesta de la compra que se creó en el sitio externo. Esta comunicación se basa en el protocolo cXML y tiene que configurarse entre los sistemas de la organización que compra y la que vende.

Para establecer la comunicación, el proveedor tiene que proporcionar datos que usted utilizará en la configuración del catálogo externo, como identidad, dominio de la empresa del comprador, por ejemplo, “DUNS” y “número DUNS”, credenciales y el URL para acceder al catálogo de proveedores.

## Configuración de un catálogo externo
<a id="setting-up-an-external-catalog" class="xliff"></a>

El catálogo externo debe habilitar que un empleado que especifique una solicitud de compra sea redirigido a un sitio externo para seleccionar productos. Los productos que el empleado seleccione en el catálogo externo se devuelven a Dynamics 365 for Finance and Operations con información de precio actualizada y de aquí se pueden agregar a la solicitud de compra. La intención no es permitir a los empleados realizar un pedido en el sitio externo. Cuando configure el catálogo externo, debe asegurarse de que el propósito del sitio al que se puede acceder por el catálogo externo sea recopilar información de presupuestos y no realizar un pedido real.

### Para configurar un catálogo de proveedores externos, complete estas tareas:
<a id="to-set-up-an-external-vendor-catalog-complete-the-following-tasks" class="xliff"></a>

1. Configure una jerarquía de categorías de compras. Para obtener más información, consulte [Configurar directivas para jerarquías de categorías de compras](/https://ax.help.dynamics.com/en/wiki/set-up-policies-for-procurement-category-hierarchies/).
2. Registre el proveedor en Finance and Operations. Para poder configurar las opciones de acceso al catálogo externo del proveedor, debe configurar el proveedor y el contacto del proveedor en Microsoft Dynamics 365. También debe agregar el proveedor del catálogo externo a la categoría de compras seleccionada. Para obtener más información acerca del registro de proveedores en Microsoft Dynamics 365, consulte [Gestionar usuarios de colaboración de proveedor](/procurement/manage-vendor-collaboration-users.md). Para obtener información sobre cómo asignar a un proveedor a una categoría de compras, consulte [Aprobar proveedores para categorías de compras específicas](/https://ax.help.dynamics.com/en/wiki/approve-vendors-for-specific-procurement-categories/).
3. Asegúrese de que las unidades de medida y la divisa que usa el proveedor se han configurado. Para obtener información sobre cómo crear una unidad de medida, consulte [Crear unidades de medida](/https://ax.help.dynamics.com/en/wiki/manage-unit-of-measure/).
4. Configure el catálogo de proveedores externos con los requisitos del sitio del catálogo externo de su proveedor. Para obtener más información acerca de esta tarea, consulte la sección siguiente.
5. Pruebe la configuración del catálogo externo del proveedor para comprobar que sea válida y que se puede acceder al catálogo externo del proveedor. Use la acción **Validar la configuración** para validar el mensaje de configuración de la solicitud que haya definido. Este mensaje debería hacer que se abra el sitio de catálogo externo del proveedor en una ventana del navegador. Durante la validación, no podrá pedir artículos y servicios del proveedor. Para pedir artículos y servicios, debe acceder al catálogo del proveedor a través de una solicitud de compra.
6. Active el catálogo externo mediante el botón **Activar catálogo** en la página **Catálogos externos** . El catálogo externo deberá activarse antes de que los empleados puedan usarlo. Puede desactivar el catálogo externo en cualquier momento.


## (4) Configurar el catálogo de proveedores externos
<a id="4-configure-the-external-vendor-catalog" class="xliff"></a>

Esta sección proporciona más detalles sobre la tarea 4 de la sección anterior.

1. Escriba un nombre y una descripción para el catálogo externo del proveedor. El nombre que escriba aparecerá en el carro que representa el catálogo externo que se muestra a los empleados que crean una solicitud. Los empleados pueden hacer clic en el carro para abrir el catálogo en el sitio del catálogo externo del proveedor.
2. Agregue una imagen mediante la acción **Imagen del catálogo externo** . La imagen aparecerá en el carro que representa el catálogo externo que se muestra a los empleados que crean una solicitud. Tenga en cuenta que la anchura y la altura de la imagen deben ser iguales. De lo contrario, la imagen no se muestra correctamente.
3. Seleccione si la página web del catálogo externo del proveedor debe aparecer en la misma ventana de explorador en la que el empleado ha creado la solicitud, o abrirse en una ventana nueva.
4. Seleccione el proveedor para el catálogo. En el lista **Entidades jurídicas** existe una fila para cada entidad jurídica donde el proveedor está configurado. Para permitir que los usuarios soliciten productos directamente del catálogo del proveedor en algunas personas jurídicas pero no otras, puede usar el botón **Impedir acceso** o **Permitir acceso** para cada entidad jurídica donde desea que el catálogo esté o no disponible.
5. En el campo **Caducidad predeterminada (días)**, escriba el número de días durante el cual un presupuesto recibido del catálogo externo es válido y se puede usar para comprar al proveedor externo. Cuando se crea un presupuesto y se recupera del sitio del catálogo externo del proveedor; el presupuesto será válido a partir de la fecha del sistema actual y seguirá siendo válido durante el número de días que escriba en este campo.
6. Haga clic en el botón **Añadir** para empezar a asignar las categorías de compras al catálogo externo. A continuación, en la lista de nombre de categoría, seleccione una categoría. La lista de categorías es un superconjunto de categorías de compras a las que se ha asignado al proveedor en todas las entidades jurídicas configuradas para dicho proveedor.
[!NOTE]
Las directivas de compra se utilizan para permitir o restringir el acceso a las categorías para la entidad jurídica compradora o unidad operativa receptora. El marcaje de salida a un catálogo externo requiere que se permita el acceso al menos a una de las categorías de compras asignada al catálogo.
7. Configure el mensaje de solicitud de configuración de cXML que se enviará al proveedor. El formato del mensaje generado automáticamente es la plantilla mínima que se requiere para iniciar una sesión. Rellene los valores de las etiquetas.

En cualquier momento, puede recargar la plantilla de mensajes generada por el sistema haciendo clic en **Restaurar formato de mensaje**. Tenga en cuenta que si restaura el formato del mensaje, el mensaje actual se sustituye por el formato de mensaje generado automáticamente, que tiene etiquetas vacías.

### Mensaje de configuración de cXML
<a id="cxml-setup-message" class="xliff"></a>
A continuación verá una descripción de las etiquetas que se incluyen en la plantilla:

| Campo | Descripción | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|El dominio de la empresa del comprador.|
|< Header >< From >< Credential>< Identity >< /Identity > | La identidad de la empresa del comprador.|
|< Header >< To >< Credential domain=”” > | El dominio de la empresa del proveedor.|
|< Header >< To >< Credential>< Identity >< /Identity> | La identidad de la empresa del proveedor.|
|< Header >< Sender >< Credential domain=”” > | El dominio de la empresa del comprador.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | La identidad de la empresa del comprador.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|El secreto compartido para la empresa del comprador.|
|< Request deploymentMode=”” >|La implementación de prueba o en producción.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|El URL del extremo de marcaje de salida del proveedor.|

### Elementos extrínsecos
<a id="extrinsic-elements" class="xliff"></a>

Un elemento extrínseco es información adicional, como un nombre de usuario basado en un usuario que hace un marcaje de salida. Se establece el elemento extrínseco cuando se produce el marcaje de salida y se puede enviar en el mensaje de configuración de la solicitud.
Su proveedor puede tener un requisito para recibir un elemento extrínseco en la solicitud de configuración. En ese caso, debe agregar el elemento extrínseco a la lista de elementos extrínsecos en la sección **Formato de mensaje** de la página **Catálogo externo**. Especifique un nombre para el elemento extrínseco que el proveedor pueda reconocer y asignar a un valor. Las opciones de valores son: nombre de usuario, correo electrónico del usuario o valor aleatorio.
Para obtener más información acerca del protocolo de cXML, consulte: http://cxml.org/

## Mensaje de confirmación
<a id="post-back-message" class="xliff"></a>
El mensaje de confirmación es el mensaje que se recibe del proveedor cuando el usuario completa la compra en el sitio externo y vuelve a Finance and Operations. Los mensajes de confirmación no se pueden configurar. Los mensajes se basan en la definición del protocolo cXML. A continuación se indica la información que puede formar parte del mensaje de confirmación que se recibe en una línea de solicitud:

| Mensaje recibido del proveedor | Se copia a la línea de solicitud en Finance and Operations|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Cantidad|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Identificador de artículo externo|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Divisa|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Precio unitario|
|< ItemDetail >< Description ShortName=”” >|Nombre del producto|
|< ItemDetail >< Description >< /Description >|Incluido en la descripción del artículo; nombre del producto si ShortName no se especifica.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Unidad|
|< ItemDetail >< Classification >< /Classification >|Incluido en la descripción del artículo|
|< ItemDetail >< Classification domain=”” >|Incluido en la descripción del artículo|

## Eliminar un catálogo externo
<a id="delete-an-external-catalog" class="xliff"></a>
Eliminar un catálogo externo con la acción Eliminar en la página.

Si se ha solicitado un producto del catálogo de proveedores externo, no se podrá eliminar el catálogo de proveedores externo. En su lugar, el estado del catálogo de proveedor externo se establece como inactivo. Si desea impedir el acceso al sitio del catálogo del proveedor externo, pero no eliminarlo, cambie el estado del catálogo externo a Inactivo.

