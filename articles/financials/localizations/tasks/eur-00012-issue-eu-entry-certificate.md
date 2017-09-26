--- 
title: Emitir un certificado de entrada de la UE
description: "Este procedimiento le muestra cómo habilitar un certificado de entrada de la UE, cómo configurar una cuenta de cliente para usar certificados de entrada y emitir un certificado."
author: mrolecki
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1eca89c0588b3611cdd3ac5a62b5ac95c83c8e62
ms.contentlocale: es-es
ms.lasthandoff: 07/27/2017

---
# <a name="issue-an-eu-entry-certificate"></a>Emitir un certificado de entrada de la UE

[!include[task guide banner](../../includes/task-guide-banner.md)]

Este procedimiento le muestra cómo habilitar un certificado de entrada de la UE, cómo configurar una cuenta de cliente para usar certificados de entrada y emitir un certificado. Este procedimiento se creó con los datos de demostración de la empresa DEMF.


## <a name="enable-entry-certificate-management"></a>Habilitar administración de certificados de entrada
1. Vaya a Clientes > Configuración > Parámetros de clientes.
2. Haga clic en la ficha Envíos.
3. Expanda la sección Certificado de entrada.
4. Seleccione Sí en el campo Habilitar administración de certificados de entrada.
5. Seleccione Sí en el campo Habilitar emisión de certificados de entrada.
6. Haga clic en la ficha Secuencias numéricas.
7. En la lista, busque y seleccione Fila de certificado de entrada.
8. En el campo Código de secuencia numérica, especifique o seleccione un valor.

## <a name="set-up-a-customer"></a>Configuración de un cliente
1. Vaya a Clientes > Clientes > Todos los clientes.
2. Use el filtro rápido para buscar registros. Por ejemplo, filtre por el campo Cuenta, por el valor "DE-015".
3. Abra los detalles de la cuenta del cliente.
4. Haga clic en Editar.
5. Expanda la sección Factura y entrega.
6. Seleccione Sí en el campo Se necesita certificado de entrada.
7. Seleccione Sí en el campo Emitir certificado de entrada.
8. Haga clic en Guardar.

## <a name="create-an-eu-entry-certificate-automatically"></a>Creación automática de un certificado de entrada de la UE
1. Vaya a Clientes > Pedidos > Todos los pedidos de venta.
2. Haga clic en Nuevo.
3. En el campo Cuenta de cliente, especifique o seleccione un valor.
4. Haga clic en Aceptar
5. En el campo Número de artículo, especifique o seleccione un valor.
6. Haga clic en Guardar.
7. En el panel de acciones, haga clic en Seleccionar y empaquetar.
8. Haga clic en Registrar albarán.
9. Expanda la sección Parámetros.
10. En el campo Cantidad, seleccione 'Todo'.
11. Quite la marca de la casilla Emitir certificado de entrada.
    * Un certificado de entrada se puede emitir al registrar un albarán o al facturar un pedido. Deje la casilla Emitir certificado de entrada sin marcar para emitirlo más adelante.  
12. Haga clic en Aceptar
13. Haga clic en Aceptar
14. En el panel de acciones, haga clic en Factura.
15. Haga clic en Factura.
    * Compruebe que las casillas Se necesita certificado de entrada y Emitir certificado de entrada en la sección Visión general estén marcadas.  También puede seleccionar la casilla Imprimir certificado de entrada para permitir imprimir el certificado.  
16. Haga clic en Aceptar
17. Haga clic en Aceptar
18. En el panel de acciones, haga clic en Factura.
19. Haga clic en Factura.
20. En el panel de acciones, haga clic en Factura.
21. Haga clic en Ver certificados de entrada emitidos.
22. Haga clic en Imprimir.
23. Cierre la página.
24. Haga clic en Cambiar estado.
25. En el campo Nuevo estado, seleccione una opción.
26. Haga clic en Aceptar
27. Cierre la página.

## <a name="create-an-eu-entry-certificate-manually"></a>Creación manual de un certificado de entrada de la UE
1. En el panel de acciones, haga clic en Factura.
2. Haga clic en Crear certificado de entrada.
3. Haga clic en Aceptar
4. En el panel de acciones, haga clic en Factura.
5. Haga clic en Ver certificados de entrada emitidos.

