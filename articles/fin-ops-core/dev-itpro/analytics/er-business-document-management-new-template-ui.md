---
title: Nueva interfaz de usuario de documentos en la gestión de documentos empresariales
description: Este tema proporciona información sobre cómo usar la nueva interfaz de usuario de documentos (UI) en la función de gestión de documentos comerciales del marco de informes electrónicos (ER).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681361"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Nueva interfaz de usuario de documentos en la gestión de documentos empresariales

[!include [banner](../includes/banner.md)]

La gestión de documentos empresariales aprovecha el marco de ER y permite a los usuarios empresariales editar plantillas de documentos empresariales mediante el servicio de Microsoft 365 o la aplicación de escritorio de Microsoft Office apropiada. Las ediciones pueden incluir cambios de diseño o nuevas implementaciones, o los usuarios pueden agregar marcadores de posición para incluir datos adicionales sin tener que cambiar el código fuente. Para obtener más información sobre cómo trabajar con la gestión de documentos empresariales, vea [Resumen de gestión de documentos comerciales](er-business-document-management.md).

La nueva interfaz de usuario del documento (UI) es más clara y más cómoda de usar. El área **Documento empresarial** muestra solo las plantillas que están disponibles para el proveedor actual.

El botón **Nuevo documento** permite a los usuarios crear y editar una plantilla en una configuración de formato de informes electrónicos (ER) proporcionada por otro proveedor. En el ejemplo de este tema, el proveedor es Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Poner a disposición la nueva interfaz de usuario de documentos en la gestión de documentos empresariales

Para comenzar a utilizar la nueva interfaz de usuario de documentos en la gestión de documentos empresariales, debe activar la característica **Experiencia de interfaz de usuario similar a oficina para la gestión de documentos empresariales** en el espacio de trabajo **Administración de características**.

Siga estos pasos para activar esta función para todas las entidades jurídicas.

1. En el espacio de trabajo **Administración de características**, en la pestaña **Nuevo**, seleccione la característica **Experiencia de IU similar a oficina para la gestión de documentos empresariales** en la lista.
2. Seleccione **Habilitar ahora** para activar la característica seleccionada.
3. Actualice la página para obtener acceso a la característica nueva.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Editar plantillas propiedad de otros proveedores

1. En el espacio de trabajo de **Gestión de documentos empresariales**, seleccione **Nuevo documento**.

    ![Espacio de trabajo de la gestión de documentos empresariales](./media/BDM_overview_new_template1.png)

2. En el cuadro de diálogo, seleccione el documento para usar como plantilla y luego seleccione **Crear documento**.

    ![Cuadro de diálogo Documentos empresariales](./media/BDM_overview_new_template2.png)

3. En el nuevo cuadro de diálogo, en el campo **Título**, cambie el título según lo requiera. El texto del título se usa para asignar un nombre a la nueva configuración del formato de ER que se crea automáticamente. La versión del borrador de esta configuración (**Copia de informe FTI de cliente (GER)**) incluirá la plantilla editada y se usará para ejecutar este formato de ER para el usuario actual. La plantilla original no modificada de la configuración del formato básico de ER se usará para ejecutar este formato de ER para los otros usuarios.
4. En el campo **Nombre**, cambie el nombre de la primera revisión de la plantilla editable que se creará automáticamente.
5. En el campo **Comentario**, actualice los comentarios para la revisión de la plantilla editable que se creará automáticamente.
6. Seleccione **Aceptar** para confirmar el inicio del proceso de edición.

    ![Cuadro de diálogo Creación de documentos](./media/BDM_overview_new_template3.png)

El botón **Nuevo documento** se usa para crear y editar una plantilla en una configuración de formato ER proporcionada por otro proveedor. En el ejemplo, el proveedor es Microsoft. Cuando seleccione **Nuevo documento**, verá todas las plantillas que poseen los proveedores actuales y otros proveedores. Después de seleccionar la plantilla, se abrirá para editarla. La plantilla editada se almacenará en una nueva configuración del formato de ER que se genera automáticamente.

Para más información, vea [Resumen de gestión de documentos empresariales](er-business-document-management.md).
