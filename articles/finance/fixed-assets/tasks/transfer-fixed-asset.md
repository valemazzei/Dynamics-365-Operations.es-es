---
title: Transferir un activo fijo
description: Esta guía de tareas transferirá la Información financiera de un libro de activo fijo desde un conjunto de dimensiones financieras a un nuevo conjunto de dimensiones financieras.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb38483d3ac61acb4513e87d8c36ddd0f8863a10
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447617"
---
# <a name="transfer-a-fixed-asset"></a>Transferir un activo fijo

[!include [banner](../../includes/banner.md)]

Esta guía de tareas transferirá la Información financiera de un libro de activo fijo desde un conjunto de dimensiones financieras a un nuevo conjunto de dimensiones financieras.  Usa el rol de contable y los datos de prueba de la entidad jurídica USMF.

1. En el panel de navegación, vaya a **Módulos > activos fijos > activos fijos > activos fijos**.
2. En la lista, busque y seleccione el activo fijo para transferir.
3. En el panel de acciones, haga clic en **Activo fijo.**
4. Haga clic en **Transferir activos fijos**.
5. En el campo **Fecha de transferencia**, especifique una fecha.
6. Escriba comentarios para describir la transferencia.
    
    Esta lista muestra todos los libros para el activo fijo.  
7. Marque los libros que desea transferir a un nuevo conjunto de dimensiones financieras.
    * Esta lista muestra los valores de dimensión financiera existentes para el libro seleccionado.  
    * seleccione la dimensión financiera que desee actualizar para el libro de activo fijo seleccionado.  
8. En el campo **Dimensión financiera**, haga clic en el botón desplegable para abrir la búsqueda.
    * Defina otros valores de la dimensión financiera si procede.  
    * Todos los valores de la dimensión financiera cambiarán cuando se produzca una transferencia, tanto si se ha especificado un valor como si se ha dejado en blanco. Por ejemplo, si se ha especificado un valor para BusinessUnit y se han dejado en blanco las dimensiones financieras CostCenter y Departamento. Si la estructura de cuentas permite valores en blanco para CostCenter y Departamento, la transferencia haría que cada modelo de valor tenga el nuevo valor para BusinessUnit y un valor en blanco para CostCenter y Departamento.  
9. Haga clic en **Actualizar**.
    * Tiene la oportunidad de ver los cambios de requisito previo antes de finalizar la transferencia.  
    * Revise los resultados antes de transferir los libros de activo fijo.  
10. Haga clic en **Transferir**.

