---
title: Crear objetos de coste
description: Este procedimiento muestra cómo crear objetos de coste importando la dimensión financiera del centro de coste en la contabilidad de Costes a través de un conector de los datos.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f5f6e5048f70e744cb3dc82a2a279aae69b4af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447740"
---
# <a name="create-cost-objects"></a>Crear objetos de coste 

[!include [banner](../../includes/banner.md)]

Este procedimiento muestra cómo crear objetos de coste importando la dimensión financiera del centro de coste en la contabilidad de Costes a través de un conector de los datos. Se ha utilizado la empresa de demostración USMF para crear este procedimiento. 


## <a name="create-new-cost-objects"></a>Crea nuevos objetos de coste.
1. Vaya a contabilidad de Costes > Dimensiones > dimensiones del objeto de Coste.
2. Haga clic en Nuevo.
3. En el campo Nombre, escriba un valor.
4. En el conector de datos para el campo de miembros de dimensión, especifique o seleccione un valor.
5. En el campo Descripción, escriba un valor.
6. Haga clic en Guardar.

## <a name="configure-the-data-connector"></a>Configura el conector de datos
1. Haga clic en Configurar proveedor de miembros de dimensión.
    * Seleccione CostCenter para importar la dimensión de CostCenter en la contabilidad de Costes.  
2. En el campo Nombre de dimensión, seleccione el centro de coste.
3. Haga clic en Aceptar

## <a name="import-cost-centers"></a>Importar centros de coste
1. Haga clic en Importar miembros de dimensión.
2. Haga clic en Aceptar

## <a name="view-the-imported-cost-centers"></a>Ver los centros de coste importados
1. Haga clic en miembros de dimensión.

