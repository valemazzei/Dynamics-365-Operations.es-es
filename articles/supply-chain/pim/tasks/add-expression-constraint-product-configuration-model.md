---
title: Agregar una restricción de expresión a un modelo de configuración de producto
description: Este procedimiento muestra cómo puede agregar una nueva expresión de restricción a un modelo de configuración de productos.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c43d7f768069c5ef201a2823a9aa626b38220073
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436867"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Agregar una restricción de expresión a un modelo de configuración de producto

[!include [banner](../../includes/banner.md)]

Este procedimiento muestra cómo puede agregar una nueva expresión de restricción a un modelo de configuración de productos. Muestra cómo puede ordenar que la protección de la esquina se aplique a un altavoz si el usuario ha seleccionado una parrilla delantera metálica. El procedimiento usa el componente Altavoz superior en la empresa de demostración USMF.


## <a name="create-an-expression-constraint"></a>Crear una restricción de expresión
1. Haga clic en Definición de modelo de variante del producto.
2. Haga clic en Modelos de configuración del producto.
3. En la lista, busque y seleccione el registro deseado.
    * Este ejemplo usa el modelo de altavoz superior.  
4. En la lista, haga clic en el vínculo de la fila seleccionada.
5. Expanda la sección Restricciones.
6. Haga clic en Agregar.
7. Haga clic en Crear.
8. En el campo Nombre, escriba un valor.

## <a name="enter-expression"></a>Introducir expresión
1. Haga clic en Editar expresión.
    * Si desbloquea la interfaz del usuario en la grabación de tareas en esta fase, puede usar IntelliSense y la lista de símbolos para crear la expresión de la restricción.  
2. En el campo ConstraintBody, especifique "Implies[FrontGrill=="Metal", CornerProtection]".
    * Esta lógica de la expresión indica: Si la parrilla delantera es metálica, se debe seleccionar la opción de protección de la esquina.  
3. Haga clic en Validar.
    * La función validar se ejecuta a través de la expresión de restricción y comprueba los errores de sintaxis.  
4. Haga clic en Cerrar.
5. Haga clic en Aceptar

