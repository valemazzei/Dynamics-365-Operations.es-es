---
title: Transacciones y estados del ciclo de vida de producto
description: Este tema explica cómo puede controlar qué transacciones están permitidas para cada estado del ciclo de vida a medida que un producto de ingeniería atraviesa su ciclo de vida.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 69ee39479424c1b629388c18e8bfefd023036d22
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/29/2020
ms.locfileid: "4437305"
---
# <a name="product-lifecycle-states-and-transactions"></a>Transacciones y estados del ciclo de vida de producto

[!include [banner](../includes/banner.md)]

A medida que un producto de ingeniería pasa por su ciclo de vida, es importante que pueda controlar qué transacciones están permitidas para cada estado del ciclo de vida. Por ejemplo, los productos que aún no están en un estado maduro no deben incluirse en un pedido de cliente. Alternativamente, si un producto está llegando al final de su vida útil, es posible que desee controlar la entrada de ese producto.

Para un producto de ingeniería, los cambios en el estado del ciclo de vida están conectados a las versiones de ingeniería del producto. Por lo tanto, el estado del ciclo de vida del producto también se puede conectar a sus versiones de ingeniería. Cuando el estado del ciclo de vida del producto está conectado a una versión de ingeniería, puede usar el estado del ciclo de vida para controlar qué transacciones están permitidas para la versión de ingeniería.

## <a name="create-and-manage-product-lifecycle-states"></a>Crear y administrar estados de ciclo de vida de producto

Para trabajar con estados del ciclo de vida del producto, vaya a **Gestión de cambios de ingeniería \> Preparar \> Estado del ciclo de vida del producto**. Luego siga uno de estos pasos.

- Para crear un nuevo estado de ciclo de vida, seleccione **Nuevo** en el Panel de acciones y luego configure los campos como se describe en las siguientes subsecciones.
- Para editar un estado de ciclo de vida existente, selecciónelo en el panel de lista, seleccione **Editar** en el Panel de acciones y luego configure los campos como se describe en las siguientes subsecciones.
- Para eliminar un estado de ciclo de vida existente, selecciónelo en el panel de lista y luego seleccione **Eliminar** en el Panel de acciones.

> [!NOTE]
> Los productos de ingeniería utilizan los mismos estados del ciclo de vida del producto que los productos estándar (que no son de ingeniería). También puede abrir la página **Estado del ciclo de vida del producto** que se describe en este tema yendo a **Gestión de información de producto \> Preparar \> Estado del ciclo de vida del producto**. Para obtener más información sobre los estados del ciclo de vida del producto, tanto para productos de ingeniería como para productos estándar, consulte [Descripción general del estado del ciclo de vida del producto](../pim/product-lifecycle.md).

### <a name="header"></a>Encabezado

Configure los siguientes campos en el encabezado del estado del ciclo de vida de un producto.

| Campo | Descripción |
|---|---|
| Estado o provincia | Permite especificar un nombre para el estado de ciclo de vida del producto. |
| Descripción | Escriba una descripción para el estado de ciclo de vida del producto. |

### <a name="general-fasttab"></a>Ficha desplegable General

Establezca los siguientes campos en la ficha rápida **General**:

| Campo | Descripción |
|---|---|
| Incumplimiento cuando se entrega a una entidad legal | Para productos estándar, establezca esta opción en *Sí* si este estado del ciclo de vida debe aplicarse a todos los productos de forma predeterminada cuando se lanzan por primera vez. Establézcalo en *No* si este estado del ciclo de vida se aplicará manualmente más tarde.<p>Esta configuración no se aplica a los productos de ingeniería. El estado del ciclo de vida de una versión de producto de ingeniería después de su creación en la empresa de ingeniería se especifica en su categoría de cambio de ingeniería. Cuando el producto se entrega a una empresa operativa, se copia el estado del ciclo de vida del producto. En otras palabras, cuando un producto de ingeniería se lanza a una empresa operativa, tiene el mismo estado de ciclo de vida que tenía en la empresa de ingeniería. El estado del ciclo de vida se puede sobrescribir en la empresa operativa.</p> |
| Es activo para planificación | Establezca esta opción en *Sí* para incluir productos que se encuentran en este estado de ciclo de vida en los cálculos en los niveles de planificación maestra y lista de materiales (BOM). Establézcala en *No* para excluir de los cálculos los productos que se encuentran en este estado de ciclo de vida. |

### <a name="enabled-business-processes-fasttab"></a>Ficha desplegable de procesos de negocio habilitados

Utilice la ficha desplegable **Procesos comerciales habilitados** para controlar cuál de los procesos de negocio disponibles se puede utilizar con productos en el estado del ciclo de vida actual. Los procesos que se enumeran en esta ficha desplegable se encuentran automáticamente de la siguiente manera:

- La primera vez que guarda un nuevo estado de ciclo de vida, la página carga los procesos comerciales que están disponibles actualmente.
- Si agrega nuevos procesos comerciales a su sistema, puede actualizar la lista en la ficha desplegable **Procesos comerciales habilitados** para un estado de ciclo de vida existente seleccionando **Buscar actualizaciones** en el Panel de acciones.

Los siguientes campos están disponibles para cada proceso que se enumera en la ficha desplegable **Procesos comerciales habilitados**.

| Campo | Descripción |
|---|---|
| Proceso | Este campo de solo lectura muestra el nombre de un proceso empresarial existente. |
| Área de proceso | Este campo de solo lectura muestra el nombre de un área de proceso existente. |
| Póliza | Seleccione uno de los siguientes valores para controlar si se permitirá el proceso actual para los productos que se encuentran en este estado de ciclo de vida y cómo:<ul><li>**Habilitado** - El proceso empresarial está permitido.</li><li>**Obstruido** - El proceso no está permitido. Si un usuario intenta utilizar el proceso en un producto que se encuentra en este estado de ciclo de vida, el sistema bloqueará el intento y mostrará un error. Por ejemplo, puede bloquear la compra de productos al final de su vida útil.</li><li>**Habilitado con advertencia** - El proceso está permitido, pero se mostrará una advertencia. Por ejemplo, es posible que desee que un producto prototipo se coloque en una orden de producción creada por el departamento de Investigación y Desarrollo. Sin embargo, otros departamentos deben tener en cuenta que aún no deben producir el producto.</li></ul> |

Si está agregando más reglas de estado del ciclo de vida como personalización, puede ver esas reglas en la interfaz de usuario (IU) seleccionando **Actualizar procesos** en el panel superior. El botón **Actualizar procesos** está disponible solo para administradores.
