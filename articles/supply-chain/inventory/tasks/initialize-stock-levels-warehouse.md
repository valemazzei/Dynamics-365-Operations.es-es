---
title: Inicializar los niveles de existencias en el almacén
description: Este procedimiento muestra cómo obtener el inventario disponible actualizado manualmente mediante un diario de movimientos de inventario.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03481ddc5bd12b3459b69d65b1cfaeb23c60dfd4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4437115"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Inicializar los niveles de existencias en el almacén

[!include [banner](../../includes/banner.md)]

Este procedimiento muestra cómo obtener el inventario disponible actualizado manualmente mediante un diario de movimientos de inventario. (También es posible actualizar el inventario disponible importando transacciones en entidades de datos). Puede ejecutar este procedimiento con los datos de la empresa de demostración USMF, donde todos los requisitos previos, como el nombre del diario, la configuración del artículo, los perfiles de contabilización y las cuentas, están disponibles. El procedimiento sugiere los valores específicos para el artículo y las dimensiones que se usan. Si elige un artículo diferente, es posible que tenga que especificar valores para distintas dimensiones.

1. Vaya a Gestión del inventario > Movimientos de diario > Artículos > Movimiento.
2. Haga clic en Nuevo.
3. En el campo Nombre, haga clic en el botón desplegable para abrir la búsqueda.
4. Seleccione IMov.
    * Es buena práctica utilizar distintas plantillas de nombre de diario para distintos fines empresariales.  
5. En la lista, haga clic en el vínculo de la fila seleccionada.
6. En el campo Cuenta de contrapartida, especifique los valores "140200".
    * Se trata de la cuenta de contrapartida que será la cuenta predeterminada en las líneas de diario. Es posible anular el valor predeterminado para asignar distintas cuentas de contrapartida por línea.  
7. Haga clic en Aceptar
8. Haga clic en Nuevo.
9. En el campo Código de artículo, haga clic en el botón desplegable para abrir la búsqueda.
10. Seleccione el artículo A0001.
11. En la lista, haga clic en el vínculo de la fila seleccionada.
12. Haga clic en la ficha Dimensiones de inventario.
13. En el campo Sitio, haga clic en el botón desplegable para abrir la búsqueda.
14. Seleccione el sitio 1.
15. En el campo Almacén, haga clic en el botón desplegable para abrir la búsqueda.
16. Seleccione el almacén 13.
17. En la lista, haga clic en el vínculo de la fila seleccionada.
18. En el campo Ubicación, haga clic en el botón desplegable para abrir la búsqueda.
19. Seleccione la ubicación 13.
20. En el campo Cantidad, especifique un número.
21. Haga clic en Guardar.
22. Haga clic en Registrar.
23. Active o desactive la casilla Transferir todos los errores de registro a un nuevo diario.
    * Si activa esta opción, cualquier línea que no pueda registrar se copiará a un nuevo diario. Puede usar la información del registro para corregir problemas y después volver a registrar las líneas.  
24. Haga clic en Aceptar
25. Cierre la página.
26. Cierre la página.

