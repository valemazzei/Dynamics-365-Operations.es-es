---
title: Establecer programas de crédito flexible
description: Puede usar programas de crédito flexible en Microsoft Dynamics 365 Human Resources para inscribir a los empleados en prestaciones de acuerdo con un número predeterminado de créditos flexibles.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 157984479a041f0bf4555aa96ed3f7e62e415d81
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420372"
---
# <a name="set-up-flex-credit-programs"></a>Establecer programas de crédito flexible

Puede usar programas de crédito flexible en Microsoft Dynamics 365 Human Resources para inscribir a los empleados en prestaciones de acuerdo con un número predeterminado de créditos flexibles. Los empleados pueden elegir cómo asignar sus créditos flexibles. Por ejemplo, si un empleado está cubierto por el plan de seguro de salud de su cónyuge, es posible que desee utilizar los créditos que de otro modo habrían utilizado en la cobertura de salud para otras prestaciones. 

1. En el espacio de trabajo **Administración de prestaciones**, en **Planes**, seleccione **Programas de crédito flexible**.

2. Seleccione **Nuevo**.

3. Especifique los valores para los siguientes campos:

   | Campo | Descripción |
   | --- | --- |
   | **Id. de crédito de prestación** | El identificador único del programa de crédito flexible. |
   | **Descripción** | Una descripción del programa de crédito flexible. | 
   | **A partir de la fecha** | La fecha en que se activa el programa de crédito flexible. |
   | **Hasta fecha** | La fecha en que finaliza el programa de crédito flexible. Puede dejar el valor predeterminado (31/12/2154) para indicar que el programa de crédito flexible no tiene un vencimiento programado. |
   | **Valor total del crédito** | La cantidad de créditos que cada empleado tendrá que usar para sus prestaciones. |
   | **Regla de prorrateo** | La regla a utilizar para prorratear los créditos flexibles cuando se contrata a un empleado en la mitad del periodo de crédito flexible. </br></br><ul><li>**Ninguno**: el empleado no recibe créditos flexibles si son contratados después de que comience el periodo del programa de crédito flexible.</li><li>**Crédito total**: el empleado recibe el importe total de créditos flexibles, independientemente de cuándo sean contratados.</li><li>**Prorrateo**: el empleado recibe un importe prorrateado de créditos flexibles en función de su fecha de inicio.</li></ul> |
   | **Fórmula de prorrateo de crédito flexible** | La regla a utilizar para prorratear los créditos flexibles para los empleados que se contratan en mitad de un periodo de prestaciones del programa de crédito flexible. El prorrateo se basa en la fecha de inicio del empleo. Este campo únicamente se usa si selecciona **Prorrateo** o **Regla de prorrateo** en el campo . </br></br><ul><li>**Diario**: se prorratea el número de créditos flexibles que recibe un empleado de forma diaria. El número total de créditos flexibles se divide por el número de días en el periodo. Por ejemplo, si su periodo de prestaciones es de 400 días, el sistema dividirá la cantidad total de créditos flexibles por 400 para calcular la cantidad de créditos flexibles que reciben los empleados por día.</li><li>**Mes actual**: se prorratea el número de créditos flexibles que recibe un empleado de forma mensual, redondeado al mes actual. El número total de créditos flexibles se divide por el número de meses en el periodo. Por ejemplo, si su periodo de prestaciones es de 15 meses, el sistema dividirá la cantidad total de créditos flexibles por 15 para calcular la cantidad de créditos flexibles que reciben los empleados por mes.</li><li>**Mes siguiente**: se prorratea el número de créditos flexibles que recibe un empleado de forma mensual, redondeado al mes siguiente. El número total de créditos flexibles se divide por el número de meses en el periodo. Por ejemplo, si su periodo de prestaciones es de 15 meses, el sistema divide la cantidad total de créditos flexibles por 15 para calcular la cantidad de créditos flexibles que reciben los empleados por mes.</li></ul> |
   
