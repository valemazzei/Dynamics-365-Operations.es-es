---
title: Configurar libros de arrendamiento
description: Este tema describe la información que se mantiene en los libros de arrendamiento. Los libros de arrendamiento contienen las directivas contables que determinan cómo se contabiliza un arrendamiento en el sistema.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4447803"
---
# <a name="set-up-lease-books"></a>Configurar libros de arrendamiento

[!include [banner](../includes/banner.md)]

Los libros de arrendamiento contienen las directivas contables que determinan cómo se contabiliza un arrendamiento en el sistema. Además de la contabilidad basada en efectivo, Arrendamiento de activos admite los siguientes estándares:

- Principios Contables Generalmente Aceptados en los Estados Unidos (US GAAP)
- Tema 842 de Codificación de Normas de Contabilidad (ASC 842)
- ASC 840
- Norma Internacional de Información Financiera 16 (IFRS 16)
- Norma Internacional de Contabilidad 17 (IAS 17)

Para crear un nuevo libro de arrendamiento, siga estos pasos.

1. Vaya a **Arrendamiento de activos \> Configuración \> Libros de arrendamiento**.
2. Seleccione **Nuevo** para agregar un libro.
3. Establezca los campos siguientes.

    | Nombre                                     | Descripción |
    |------------------------------------------|-------------|
    | Capa de registro                            | Seleccione una capa de registro a utilizar. Cada libro adjunto a un arrendamiento se configura para una capa de publicación específica. Cada capa de registro tiene diferentes propósitos de registro. |
    | Tipo de arrendamiento                               | Seleccione si el arrendamiento debe clasificarse automáticamente o si debe estar predefinido como arrendamiento financiero u operativo. |
    | Marco de contabilidad                     | Seleccione el marco asociado con el libro. |
    | Configuración del plazo del arrendamiento/vida útil          | El sistema clasificará el arrendamiento como financiero si el tipo de arrendamiento se establece en **Automático** y si el plazo del arrendamiento durante la vida útil del activo es mayor o igual al porcentaje introducido en este campo.  |
    | Configuración del valor actual/valor razonable del activo   | Introduzca un número entero para definir el umbral que determinará el tipo de arrendamiento. Si el valor presente de los futuros pagos mínimos de arrendamiento es mayor que el valor definido por el usuario de la configuración del libro, y si la clasificación del arrendamiento del libro se establece en automática, el sistema clasificará el arrendamiento como arrendamiento financiero. |
    | Umbral a corto plazo                     | Introduzca el número de meses que se utilizará como umbral para los arrendamientos a corto plazo. Si el plazo del arrendamiento es menor o igual al número de meses que introduce aquí, el sistema clasificará el arrendamiento como arrendamiento a corto plazo y se aplicará el tratamiento de arrendamiento diferido. |
    | Umbral de valor bajo                      | Introduzca una cantidad para usarla como umbral de arrendamientos de bajo valor. Si el valor razonable del activo es menor o igual al valor que introduce aquí, el sistema clasificará el arrendamiento como arrendamiento de bajo valor y se aplicará el tratamiento de arrendamiento diferido. |
    | Pagar a proveedor                            | Establezca esta opción en **Sí** para permitir que los pagos del arrendamiento se registren, como una factura, en la cuenta del proveedor que se especifica en cada arrendamiento. Cuando se registra un pago de arrendamiento, se abona en la cuenta del proveedor. Si esta opción se establece en **No**, será la cuenta que se especifica para el tipo de registro **Pago de arrendamiento** en la página **Parámetros de registro de arrendamiento** la que se acreditará en su lugar. |
