---
title: Almacenar configuraciones para los extractos de Retail
description: Este procedimiento muestra las configuraciones para la tienda que afectan a la manera en que se crean y se registran los extractos de Commerce.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e255c58997ed1c0ad5614b15867f14714a8bcfc8
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/24/2020
ms.locfileid: "4415688"
---
# <a name="store-configurations-for-retail-statements"></a>Almacenar configuraciones para los extractos de Retail

[!include [banner](../includes/banner.md)]

Este procedimiento muestra las configuraciones para la tienda que afectan a la manera en que se crean y se registran los extractos de Commerce. Las dimensiones financieras en tiendas se cubren en otro procedimiento. Este procedimiento usa la empresa de prueba USRT.

1. En el **Panel de navegación**, vaya **Módulos > Retail y Commerce > Canales > Tiendas > Todas las tiendas**.
2. En la lista, busque y seleccione el registro deseado.
3. En la lista, haga clic en el vínculo de la fila seleccionada.
4. Haga clic en **Editar**.
5. La configuración de la ficha desplegable **Extracto/cierre** afecta a la creación, la validación y al registro de extractos para el almacén. Expanda la ficha desplegable **Extracto/cierre**.  
6. En el campo **Método de extracto**, seleccione el método que desea usar para agrupar las líneas de extracto.  
7. Seleccione "Sí" en **Un extracto al día** si solo se debería crear un extracto al día al crear extractos del trabajo por lotes de la creación de extractos.  
8. El campo **Cálculo de declaración por forma de pago** define si las declaraciones por forma de pago se deben agregar juntas o si se debe usar la última.  
9. En el campo **Redondeo**, seleccione la cuenta contable en la que registrar diferencias de redondeo.  
10. En el campo **Diferencia de redondeo máxima**, especifique la diferencia de redondeo máxima permitida.
11. En el campo **Registro**, introduzca la diferencia de registro total máxima permitida para un extracto.
12. En el campo **Turno**, especifique la diferencia total máxima dentro de un turno en un extracto.  
13. En el campo **Transacción**, introduzca la diferencia total máxima en una línea de extracto.  
14. En el campo **Método de cierre**, defina si las transacciones que se incluirán en un extracto deben parte de un turno cerrado o si puede haber algunas transacciones dentro del intervalo definido de fecha o hora.  
15. En el campo **Final del día laboral**, especifique una hora si las transacciones que se producen después de medianoche se deben registrar con el día anterior.  
16. Seleccione "Sí" en **Registrar como día laboral** si las transacciones que se producen después de medianoche se deben registrar como parte del día anterior.  
17. Seleccione "Sí" en **Dividir por método de extracto** para que se creen extractos para cada método de extracto definido. Esta acción puede resultar útil si el rendimiento del registro se debe mejorar para almacenes con volúmenes altos de transacción puesto que creará muchos extractos más pequeños que se pueden procesar en paralelo.  
18. En la ficha desplegable **General**, en el campo **Cliente predeterminado**, puede seleccionar la cuenta de cliente que se usará para ventas a los clientes que entran.  

