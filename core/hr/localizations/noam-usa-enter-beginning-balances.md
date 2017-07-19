---
title: "Especificar saldos iniciales de nómina"
description: "El tema se describen los pasos para especificar los saldos iniciales para los códigos de ganancias, las deducciones, las prestaciones y los impuestos. Esta información tiene valor para que los socios migren o transfieran los datos para una nueva implementación de nóminas desde otro sistema."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 911a51e2498800e7ee7b1562b66c56967eef0505
ms.openlocfilehash: e6213d2e01445b78c6d8f98fc6a55f7c551231b5
ms.contentlocale: es-es
ms.lasthandoff: 06/19/2017


---

# Especificar saldos iniciales de nómina
<a id="enter-payroll-beginning-balances" class="xliff"></a>

[!include[banner](../../includes/banner.md)]]

El tema se describen los pasos para especificar los saldos iniciales para los códigos de ganancias, las deducciones, las prestaciones y los impuestos. Esta información tiene valor para que los socios que transfieran los datos para una nueva implementación de nóminas desde otro sistema. Para prepararse para especificar los saldos iniciales de nóminas, comprobamos la siguiente información:

> * Los registros de empleados se especificaron y están disponibles en el sistema
> * Los siguientes datos se configuraron y asignaron a los empleados:

> > * Ciclos y períodos de pago
> > * Códigos de ganancia
> > * Impuestos
> > * Beneficios y deducciones

> * La empresa debe haber elegido una fecha en la que saldos iniciales de nóminas se pueden configurar.

> * La información recopilada se en todas las ganancias, las prestaciones/deducciones, las contribuciones de prestación, los impuestos del empleado y los impuestos del empresario y los importes del año hasta la fecha del sistema heredado.

Cuando vaya a especificar saldos iniciales, considere cómo lo detallados que deben estar los datos. La mayoría de las empresas especifican un importe único, consolidado del año hasta la fecha. Sin embargo, si se necesita más información detallada, los saldos se pueden especificar en incrementos trimestrales. Decidir el nivel de detalle que sea necesario determina cuántos extractos de pago manuales se deben crear para cada trabajador. Para un solo importe del año hasta la fecha, solo una instrucción manual es necesaria para cada empleado. Para hacer esto utilice importes de año hasta la fecha desde el extracto de pago final del sistema anterior como el importe especificado en el nuevo sistema de nóminas.

El siguiente ejemplo muestra cómo puede especificar saldos iniciales de nómina de empleados, incluidos los códigos de ganancias, las prestaciones/deducciones y los impuestos. En un ejemplo del mundo real sólo recibiría un artículo de línea para cada código de ganancias, deducción de prestaciones, contribución de prestaciones impuesto de empleado e impuesto de empresario con el importe especificado siendo el importe del año hasta la fecha. Mediante esta lista de códigos e importes, siga los pasos para crear una ganancia manual y extracto de pago con la contabilidad deshabilitada para traer saldos iniciales para fines de nómina.  Se deshabilita la contabilidad ya que no se recomienda registrar este extracto de pago de saldo inicial en la contabilidad general. Esto se ha realizado en el sistema heredado y pasará al nuevo sistema cuando configure los saldos iniciales en la contabilidad general.

> [!NOTE] 
> Si desea reproducir los mismos pasos de más abajo, puede usar los datos de prueba. Los datos de prueba se pueden descargar en PartnerSource

### A. Cómo configurar los códigos de ganancias que se utilizarán en los saldos iniciales de nóminas
<a id="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances" class="xliff"></a>
Al especificar los saldos iniciales de nómina, asegúrese de que los códigos de ganancias que usará están configurados con la opción “Permitir edición de tasas de extracto de ganancias” habilitada. Esto le permitirá especificar manualmente el importe del sistema heredado. 

### B. Crear el extracto de ganancias para que un empleado con saldo inicial
<a id="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance" class="xliff"></a>
Este paso crea manualmente una instrucción de ganancias para cada trabajador para el último período salarial del sistema heredado, lo que crea las líneas de extracto de ganancias en el nuevo sistema de nóminas. Especifique una línea por código de ganancias y el importe y las horas de del año hasta la fecha. Los pasos de ejemplo son los siguientes:

1. Abra la página **Todos los extractos de ganancias** y haga clic en **Nuevo**.  

Especifique la información siguiente: 

| Campo      | Valor                 |
|------------|-----------------------|
| Trabajador     | Michael Redmond       |
| Ciclo de pago  | Se                    |
| Período de pago | 16/6/2017 - 30/6/2017 |

2. En la pestaña **Línea de extracto de ganancias**, especifique lo siguiente:

Línea 1: Pestaña **Línea de extracto de ganancias**

| Campo            | Valor       |
|------------------|-------------|
| Código de ganancias    | Pago regular |
| Cantidad         | 1,00        |
| Índice             | 30.000      |
| Pestaña Detalles de línea |             |
| Manual           | (marcado)    |

Línea 2: Pestaña **Línea de extracto de ganancias**

| Campo            | Valor    |
|------------------|----------|
| Código de ganancias    | Bonificación    |
| Cantidad         | 1.0000   |
| Índice             | 4250.00  |
| Pestaña Detalles de línea |          |
| Manual           | (marcado) |

Línea 3: Pestaña **Línea de extracto de ganancias**

| Campo           | Valor      |
|-----------------|------------|
| Código de ganancias   | Comisión |
| Cantidad        | 1.0000     |
| Índice            | 1299,00   |
| Índice            | 1,299.00   |
| Pestaña Detalles de línea |            |
| Manual          | (Marcado)   |

> [!NOTE]
> Marcar el valor de la casilla de verificación Manual en la pestaña **Detalles de línea** para cada línea de extracto de ganancias es fundamental para tener saldos iniciales de nómina especificados para cada trabajador.

3. En el panel **Acción**, haga clic en **Liberar extracto de ganancias** USA-FED-ER-FICA.

4. En el panel **Acción** haga clic en **Extracto de pago** para abrir la página **Generar extractos de pago** y establecer lo siguiente:

| Campo              | Valor     |
|--------------------|-----------|
| Fecha de pago       | 6/30/2017 |
| Tipo de ejecución de pago   | Manual    |
| Deshabilitar contabilidad | (marcado)  |

> [!NOTE] 
> Esto solo está disponible cuando el tipo de procesamiento de pago es manual y si el usuario desea deshabilitar la contabilidad en el procesamiento de pagos.

Haga clic en **Aceptar** y cierre el **Registro de información**.

#### ¿Por qué la casilla de verificación Contabilidad tiene que estar activada cuando se generan extractos de pago?
<a id="why-disable-accounting-checkbox-needs-to-be-turned-on-when-generating-pay-statements" class="xliff"></a>
Esto impide que cualquier línea de los extractos de pago se distribuya y se registrada en la contabilidad general. No se recomienda registrar este extracto de pago de saldo inicial mientras que sus valores estén en la contabilidad general a partir del sistema heredado. Esta carga de saldos se usa para fines de notificación y restricción.

### C. Crear extractos de pago para empleados
<a id="c-create-pay-statements-for-employees" class="xliff"></a>
Tras generar los extractos de pago con saldos iniciales, debe comprobar que los extractos de pago reflejan exactamente los datos de la nómina. También debe actualizar manualmente la información de prestaciones y de impuestos para que coincida con los valores del sistema de nóminas anterior. Después de verificar que los importes del sistema de nóminas anterior se corresponden con los importes de los extractos de pago actuales, debe finalizar los extractos de pago.

1. Abre la página **Todos los extractos de pago**.

2. Resalte el último extracto de pago generado para Michael Redmond

3. Haga clic en **Editar** para abrir la página **Extracto de pago**.

4. Abre la pestaña **Deducciones por prestaciones** y especifique lo siguiente:

| Campo                           | Valor            |
|---------------------------------|------------------|
| Beneficio                         | Importe de deducción |
| 401K | Participar              | 3000.00          |
| Dental | SubSp                  | 495,00           |
| Gastos de atención del Dep | Participar | 2500.00          |
| Visión | SupSp                  | 500,00           |

5. En la pestaña **Deducciones por prestaciones**, especifique lo siguiente: 

| Campo                           | Valor            |
|---------------------------------|------------------|
| Beneficio                         | Importe de deducción |
| 401K | Participar              | 3000.00          |
| Dental | SubSp                  | 495,00           |
| Gastos de atención del Dep | Participar | 2500.00          |
| Visión | SupSp                  | 500,00           |

6. En la pestaña **Contribuciones por prestaciones**, especifique lo siguiente:

| Campo              | Valor               |
|--------------------|---------------------|
| Beneficio            | Importe de contribución |
| 401K | Participar | 3000,00             |
| Dental | SubSp     | 495,00              |
| Visión | SubSp     | 500,00              |

7. En la pestaña **Deducciones por impuestos**, especifique lo siguiente:

| Campo           | Valor            |
|-----------------|------------------|
| Código de impuesto        | Importe de deducción |
| USA-FED-ER-FICA | 1600.00          |
| USA-FED-ER-MEDI | 825.75           |

8. En la pestaña **Contribuciones por impuestos**, especifique lo siguiente:

9. Haga clic en **Calcular**.
> [!IMPORTANT] 
> Valide los totales del extracto de pago que coincidan con el año hasta la fecha del sistema heredado para el trabajador. Es posible que desee retener la finalización en el paso siguiente para hacer una validación general de todos los extractos de pago en conjunto. Una vez hecha la validación pase por todos los extractos de pago y complételos.

El mismo proceso se puede realizar en incrementos trimestres si fuera necesario para todos los trimestres anteriores de cada año. Esto solo es necesario si el cliente necesita ver los datos por trimestre sin tener que volver al sistema heredado.

## Si se equivoca especificando los saldos iniciales para un empleado
<a id="if-you-make-a-mistake-entering-beginning-balances-for-an-employee" class="xliff"></a>
Es posible invertir y repetir las transacciones. Para invertir la transacción, todo lo que debe hacer es completar los pasos siguientes en la página **Todos los extractos de pago**.

1. Haga clic en **Invertir**.

2. Haga clic en **Sí** cuando aparezca el mensaje “Cuando se invierte este extracto de pago, se crea un extracto de pago de inversión para compensarlo. Ninguno de los extractos de pago se podrá modificar. ¿Quiere invertir este extracto de pago? . 

Después de invertir extracto de pago, puede generar un nuevo extracto de pago para el trabajador desde el extracto de ganancias que creó anteriormente en el procedimiento para generar extractos de ganancias y extractos de pago con saldos iniciales anteriormente en este tema. Asegúrese de corregir cualquier línea errónea en el extracto de ganancias antes de generar un nuevo extracto de pago y repita el procedimiento para actualizar extractos de pago con saldos iniciales para prestaciones e impuestos anteriormente en este tema.
