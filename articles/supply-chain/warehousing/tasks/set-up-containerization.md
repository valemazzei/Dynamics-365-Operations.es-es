---
title: Configurar la creación de contenedores
description: Este tema describe cómo automatizar la creación de contenedores de cargas en Administración de almacenes.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f961dc379ceeeae9bbceec1baaa9b9be21316f3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4437184"
---
# <a name="set-up-containerization"></a>Configurar la creación de contenedores

[!include [banner](../../includes/banner.md)]

Este tema describe cómo automatizar la creación de contenedores de cargas en Administración de almacenes. La creación de contenedores automatizada crea contenedores y el trabajo de picking para envíos cuando se procesa una oleada y las líneas de trabajo se pueden dividir en cantidades que se ajusten a los contenedores. Esto ayuda a los trabajadores de almacén a seleccionar los artículos directamente en el contenedor elegido. En comparación con el proceso de embalaje manual, las tareas como la creación de contenedores, la asignación de artículos y el cierre de contenedores se automatizan por el sistema. Este procedimiento usa la empresa de demostración USM y lo lleva a cabo un director de almacén.


## <a name="set-up-a-wave-template"></a>Configurar una plantilla de oleada
1. En el panel de exploración, vaya a **Módulos > Gestión de almacenes > Configurar > Oleadas > Plantillas de oleada**.
2. Seleccione **Nuevo**.
3. En el campo **Nombre de la plantilla de oleada**, escriba un valor.
4. En el campo **Descripción de la plantilla de oleada**, escriba un valor.
5. En el campo **Sitio**, especifique o seleccione un valor.
6. En el campo **Almacén**, especifique o seleccione un valor.
7. Expanda la sección **Métodos**. En el panel **Métodos de selección** se muestran los métodos para el tipo de plantilla de oleada seleccionado. La plantilla de oleada debe incluir el método de creación de contenedores.  
8. En el campo **Código de paso de oleada**, escriba un valor. Especifique un código de paso de oleada para el método agregado, que puede ser cualquier código. Es posible agregar el método más de una vez y asignar diferentes códigos de paso de oleada. Para ello, seleccione **Repetible para este método** en la página **Métodos de procesamiento de oleada**.  
9. Seleccione **Guardar**.
10. Cierre la página.

## <a name="set-up-a-container-type"></a>Configure un tipo de contenedor.
1. En el panel de exploración, vaya a **Módulos > Gestión de almacenes > Configurar > Contenedores > Tipos de contenedor**. Puede definir sus contenedores en la página **Tipos de contenedor**. Puede configurar las dimensiones físicas de los contenedores, incluida la tara, el peso máximo, el volumen máximo, la longitud máxima, el ancho y el alto. En este ejemplo, tenemos tres tamaños diferentes de cajas.  
2. Seleccione **Nuevo**.
3. En el campo **Código de tipo de contenedor**, escriba un valor.
4. En el campo **Tara**, escriba un número.
5. Escriba un número en el campo **Peso máximo**.
6. En el campo **Volumen**, escriba un número.
7. En el campo **Longitud**, especifique un número.
8. En el campo **Ancho**, escriba un número.
9. En el campo **Alto**, escriba un número.
10. En el campo **Descripción**, escriba un valor.
11. Seleccione **Guardar**.
13. Repita los pasos 2-11 dos veces más para hacer tres tipos de contenedor en total.
14. Cierre la página.

## <a name="set-up-a-container-group"></a>Configurar un grupo de contenedores
1. En el panel de exploración, vaya a **Módulos > Gestión de almacenes > Configurar > Contenedores > Grpos de contenedor**.
2. En el panel de acciones, haga clic en **Nueva**. Puede configurar grupos lógicos de tipos de contenedores. Para cada grupo, puede especificar la secuencia en la que se deben empaquetar los contenedores y el porcentaje de relleno de los contenedores. Las dimensiones del artículo se usan para determinar si cabrá en el contenedor. Se usa el contenedor que se encuentra más cercano a las dimensiones de tamaño del artículo. Si tiene varios tipos de contenedor en un grupo, se recomienda que organice la secuencia por tamaños, de modo que el contenedor más grande sea el primero, número 1 en la secuencia, y el contenedor más pequeño el último.    
3. En el campo **Identificación del grupo de contenedor** , escriba un valor que creó anteriormente.
4. En el campo **Descripción**, escriba un valor.
5. Repita los pasos 2-4 para los tres tipos de contenedor que creó anteriormente.
6. Seleccione **Guardar**.
7. Cierre la página.

## <a name="set-up-a-container-build-template"></a>Configurar una plantilla de creación de contenedores
1. En el panel de exploración, vaya a **Módulos > Gestión de almacenes > Configurar > Contenedores > Plantillas de creación de contenedores**.
2. Seleccione **Nuevo**. La plantilla de creación de contenedores se basa en cuáles de los procesos de creación de contenedores se realizan. Cada plantilla de creación de contenedores define un proceso de creación de contenedores que se usará por una plantilla de oleada. La opción **Editar consulta** le permite definir las condiciones en las que se procesará la plantilla seleccionada. Por ejemplo, puede que desee ejecutar solo la creación de contenedores para clientes, productos o almacenes específicos, o puede agregar los intervalos de consultas correspondientes a la plantilla. El campo **Código de paso de oleada** es cómo una plantilla de creación de contenedores se vincula a los pasos de una plantilla de oleada. Cuando se ejecuta una oleada, determina qué plantilla de creación de contenedores se usan para iniciar la creación de contenedores. El campo Tipos de consulta base determina qué embalar y en qué se basará la consulta del filtro. 
3. En el campo **Id. de plantilla de contenedor**, escriba un valor.
4. En el campo **Id. de grupo de contenedores**, especifique o seleccione un valor.
5. En el campo **Código de paso de oleada**, escriba un valor.
6. Active la casilla **Permitir selecciones divididas**.
7. Seleccione **Guardar**.
8. Seleccione **Restricciones de combinación de contenedor**. Las interrupciones de lógica de combinación le permiten configurar reglas para embalar líneas de asignación en contenedores. Por ejemplo, si agrega el campo **Número de artículo**, cuando los artículos se asignen a los contenedores, se crearán un nuevo contenedor cuando haya un nuevo número de artículo. Esto evitará que los trabajadores embalen líneas de asignación para dos clientes diferentes en el mismo contenedor.  
9. Seleccione **Nuevo**.
10. En el campo **Tabla**, seleccione una opción.
11. En el campo **Selección de campo**, especifique o seleccione un valor.
12. Seleccione **Aceptar**.

