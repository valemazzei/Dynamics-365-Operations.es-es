---
title: Crear y actualizar una directiva de devoluciones y reembolsos para un canal
description: Este tema explica cómo configurar una directiva de devoluciones y reembolsos para un canal.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415635"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Crear y actualizar una directiva de devoluciones y reembolsos para un canal

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Visión general

La directiva de devoluciones del canal en Dynamics 365 Commerce permite a los minoristas establecer medidas de cumplimiento sobre las cuales se pueden permitir formas de pago para procesar una devolución en un dispositivo de punto de venta (PDV).  

Este tema describe los pasos para configurar una directiva de devoluciones y reembolsos para un canal.

El alcance de la directiva se limita actualmente a establecer las formas de pago que se pueden permitir para un canal. La lista "permitidos" se basa en los métodos de pago utilizados para realizar la compra. Por ejemplo:

- Si una compra se realizó con una tarjeta regalo, la directiva de la tienda es procesar los reembolsos solo a una nueva tarjeta de regalo o dar crédito de la tienda. 
- Si una venta se realiza en efectivo, las opciones permitidas para reembolso son efectivo, tarjeta de regalo y cuenta del cliente, pero no tarjeta de crédito. 


## <a name="enable-return-policy"></a>Habilitar directiva de devolución

Para habilitar la funcionalidad de directiva de devolución del canal, haga lo siguiente:

1. Vaya al espacio de trabajo **Administración de características** en Dynamics 365 Commerce.
2. Busque la característica **Habilitar directiva de devoluciones del canal** en la lista de nombres de características.
3. Seleccione **Habilitar ahora**. 

## <a name="configure-return-policy"></a>Configurar directiva de devoluciones

Siga estos pasos para configurar una política de devoluciones para una tienda minorista o un canal minorista en línea.

1. Vaya a **Retail y Commerce** \> **Configuración de canal** \> **Devoluciones** \> **Directiva de devoluciones del canal**.

2. Seleccione **Nueva** para crear una nueva plantilla de directiva de devoluciones. Para usar una plantilla existente, seleccione la plantilla en el panel izquierdo. Para nuevas plantillas, agregue un nombre y una descripción que le ayudará a identificar la directiva cuando se aplique al canal.

   ![Agregar nueva directiva de devoluciones](media/Return-policy-page1.png "Agregar nueva directiva de devoluciones")
     
   
3. En la sección **Métodos de pago de devoluciones permitidos**, defina las formas de pago de devolución **permitidas** que son específicas para cada método de pago.
   ![Agregar métodos de pago](media/Return-policy-page2.PNG "Establecer métodos de pago permitidos por tipo de pago")
   
    > [!IMPORTANT]
    > - Los métodos de pago se derivan de los métodos de pago establecidos para la organización.
    > - La adición de un tipo de forma de pago de devolución permitida para cada método de pago mostrado garantizará que las devoluciones se puedan realizar al tipo de forma de pago de devolución permitido.
    
4. Asocie la plantilla de directiva de devoluciones a las tiendas en la que se usará. Seleccione **Agregar** en la pestaña **Canales minoristas** y asocie los canales disponibles. 

    - En el cuadro de diálogo **Elegir nodos organizativos**, seleccione las tiendas, regiones y organizaciones a las que debe asociarse la plantilla.
    - Solo se puede asociar una plantilla de directiva de devoluciones a cada tienda.
    - Use los botones de flecha para seleccionar tiendas, regiones u organizaciones.
    - La fecha de vigencia de la directiva será la fecha en que las directivas se aplican a los canales y se ejecuten los trabajos del canal. 

    ![Cuadro de diálogo Elegir nodos organizativos](media/Return-policy-page3.PNG "Cuadro de diálogo Elegir nodos organizativos")

5. En la página **Programación de distribución**, ejecute el trabajo **1070** para que la directiva de devoluciones del canal esté disponible para el PDV.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Vista previa de la directiva de devolución del canal en el PDV

Siga los pasos en cualquiera de los siguientes ejemplos para ver los tipos de formas de pago de devolución permitidos en PDV.

1. Inicie sesión en el PDV como cajero o director.
2. Debajo de **Turnos y caja registradora**, seleccione **Mostrar diario**.
3. Seleccione la transacción que forma parte de la devolución. 
4. Seleccione los artículos de los que se hará la devolución y elija el método de pago.  
- Si la forma de pago seleccionada aparece en la lista permitida de tipos de forma de pago de devolución, el cajero puede completar la transacción.
- Si la forma de pago seleccionada no está permitida, se muestra un mensaje de error.
- Seleccione **Importe vencido** para mostrar una lista de todos los tipos de formas de pago de devolución permitidos.

– O bien –

1. Inicie sesión en el PDV como cajero o director.
2. Seleccione **Transacción de devolución** e introduzca el id. de recibo que usa un análisis de código de barras o introdúzcalo manualmente. 
3. Seleccione la transacción que forma parte de la devolución. 
4. Seleccione los artículos de los que se hará la devolución y elija el método de pago.  
- Si la forma de pago seleccionada aparece en la lista permitida de tipos de forma de pago de devolución, el cajero puede completar la transacción.
- Si la forma de pago seleccionada no está permitida, se muestra un mensaje de error.
- Seleccione **Importe vencido** para mostrar una lista de todos los tipos de formas de pago de devolución permitidos.

![Devolución no permitida](media/Return-policy-page6.png "Tipo de devolución no permitido")



![Lista de métodos de pago](media/Return-policy-page5.PNG "Tipos de devolución permitidos")
