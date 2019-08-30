---
title: Tipos de importancia de los activos
description: En este tema se explican los tipos de importancia de los activos en Administración de activos.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660038060826ade9301e50143e49b53ba3fcd3ab
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783577"
---
# <a name="asset-criticalities"></a>Importancia de activos

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

En este tema se explican los tipos de importancia de los activos en Administración de activos. La importancia de los activos está relacionada con los activos y se transfiere a las órdenes de trabajo. No se puede modificar en una orden de trabajo. La importancia de los activos se usa para calcular la importancia de la orden de trabajo durante la programación de esta. Es decir, se usa para calcular hasta qué grado un trabajo de mantenimiento de un activo afecta a la programación de producción y la productividad de la empresa. Para obtener más información sobre la configuración relacionada con el cálculo de puntuaciones para la programación de órdenes de trabajo, consulte [Parámetros de administración de activos](../setup-for-objects/enterprise-asset-management-parameters.md).

Para configurar la importancia, primero se crean los tipos de importancia que se usarán en la configuración del activo. A continuación se configuran las imporatncias de los activos.

## <a name="set-up-criticality-types"></a>Configurar tipos de importancia

1. Seleccione **Administración de activos** \> **Configuración** \> **Activos** \> **Tipos de importancia**.
2. Seleccione **Nuevo** para crear un registro.
3. En el campo **Importancia** especifique un número que indique la importancia.
4. En el campo **Nombre**, especifique un nombre para el tipo de importancia.
5. En el campo **Factor**, escriba un factor. Este factor se utiliza durante el cálculo de la programación de órdenes de trabajo para determinar el registro de importancia que se debe utilizar. (Siempre se usa el registro que tiene el factor más alto). Este valor es relevante si, como se muestra en la siguiente ilustración, se crean líneas de importancia con el mismo valor de criticalidad.

    ![Figura 1](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Configurar importancias de activos

1. Seleccione **Administración de activos** \> **Configuración** \> **Importancias de activos**.
2. Seleccione **Nuevo** para crear un registro.
3. En función del nivel de detalle necesario para la importancia de activo, realice las selecciones relevantes en **Ubicación funcional**, **Tipo de activo**, **Fabricante**, **Modelo**, **Activo**, **Categoría del tipo de trabajo**, **Tipo de trabajo**, **Variante del tipo de trabajo** y **Requisito de trabajo**.

    > [!NOTE]
    > Si se selecciona una importancia de activo, Administración de activos recorre todos los registros de importancia de activo para comprobar si hay una coincidencia posible. Comprueba siempre primero la combinación más específica. Es decir, Administración de activos comprueba en primer lugar **Requisito de trabajo**. Si no se encuentra ninguna coincidencia, comprueba **Variante del tipo de trabajo**. Si no se encuentra ninguna coincidencia, comprueba **Tipo de trabajo**, y así sucesivamente. Como puede ver en el diseño de la página, este comportamiento significa que, para encontrar la combinación más específica, Administración de activos comprueba cada registro de derecha a izquierda en busca de una coincidencia. Si no se encuentra ninguna coincidencia, se utiliza el registro "predeterminado" que no tiene ninguna selección.

4. En el campo **Importancia**, seleccione uno de los valores de importancia que creó en el procedimiento anterior.

### <a name="notes-about-criticality-setup"></a>Notas sobre la configuración de la importancia

- Si modifica una importancia de activo en esta configuración después de utilizarla en una orden de trabajo, la importancia de la orden de trabajo no se actualiza como corresponde.
- La importancia de una orden de trabajo se actualiza cada vez que se agrega o se elimina una línea de la orden de trabajo.
- Si una orden de trabajo contiene varios trabajos, siempre se usará la importancia más alta, según el campo **Factor** de la página **Tipos de importancia**, en la orden de trabajo.
- Normalmente, la importancia de activo puede cambiar durante un período. La importancia se puede ver afectada por la compra de nuevo equipo, restauraciones y así sucesivamente. Considere reevaluar las importancias de los activos a intervalos regulares (por ejemplo, una vez al año o cada dos años) para asegurarse de que las definiciones de importancia coinciden con la configuración de la producción actual.