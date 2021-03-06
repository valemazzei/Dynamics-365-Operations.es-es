---
title: Introducción a la optimización de la planificación
description: Este tema explica cómo empezar a usar la función de optimización de la planificación.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/29/2020
ms.locfileid: "4437299"
---
# <a name="get-started-with-planning-optimization"></a>Introducción a la optimización de la planificación

[!include [banner](../../includes/banner.md)]

Como se [anunció previamente](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization está programado para reemplazar el motor de planificación maestro integrado existente.

Si actualmente utiliza el motor de planificación maestro integrado, debería comenzar a planificar su migración a Planning Optimization ahora. Es importante comenzar el proceso de migración de inmediato porque sus operaciones pueden verse afectadas cuando se aplica la obsolescencia. Para evitar problemas de última hora cuando se aplica la desactivación, le recomendamos encarecidamente que complete la migración antes del 1 de diciembre de 2020. 

La funcionalidad de optimización de la planificación no admite actualmente todas las características disponibles en el motor de planificación que se incorpora en Supply Chain Management. Por lo tanto, es importante que evalúe si la función que están disponible actualmente en la optimización de la planificación cumplirá sus requisitos. La funcionalidad de Planning Optimization no está activada actualmente de forma predeterminada en Dynamics Lifecycle Services (LCS), por lo que tiene la oportunidad de realizar su evaluación antes de que se active la función.

> [!NOTE]
> Debe solicitar una excepción de la migración a Planning Optimization si su proceso de planificación maestra no incluye la producción (la planificación maestra generó órdenes de producción planificadas) y necesita el motor de planificación maestra incorporado más allá de la versión 10.0.15. A partir de la versión 10.0.16, se mostrará un error en los entornos al ejecutar la planificación maestra incorporada sin la generación de órdenes de producción planificadas. La optimización de planificación debe utilizarse para todas las implementaciones nuevas que no generan órdenes de producción planificadas durante la planificación maestra. Los propietarios de entornos existentes que ejecutan el motor de planificación maestro incorporado sin generar órdenes de producción planificadas recibirán un correo con detalles sobre el proceso de excepción. Le recomendamos que trabaje con un socio para evaluar y planificar la migración a Planning Optimization.

Antes de activar o desactivar la planificación de optimización, se recomienda encarecidamente que evalúe los resultados del análisis de aptitud de optimización de la planificación. Para obtener más información, consulte [Análisis de aptitud de optimización de la planificación](planning-optimization-fit-analysis.md).

### <a name="availability"></a>Disponibilidad
Optimización de planificación está disponible actualmente en las siguientes geografías de Azure: Estados Unidos, Canadá, Europa, Reino Unido y Australia. Si intenta instalar el complemento desde otra región geográfica, LCS mostrará un mensaje que indica que esta ubicación geográfica no es compatible.

Tenga en cuenta que Optimización de planificación no admite implementaciones locales de Dynamics 365 Supply Chain Management.

### <a name="licensing"></a>Licencias

Si puede ejecutar con la planificación maestra con su licencia actual, no es necesario comprar una licencia adicional de empezar a usar la optimización de la planificación.

### <a name="install-the-add-in"></a>Instalar el complemento

Para usar la optimización de la planificación, instale el complemento de optimización de la planificación para Dynamics 365 Supply Chain Management. Puede obtener acceso al complemento desde su proyecto de LCS y activar la funcionalidad de optimización de la planificación desde la interfaz de usuario (IU) de Supply Chain Management.

> [!NOTE]
> El requisito para Optimización de la planificación es un entorno de alta disponibilidad habilitado para LCS, nivel 2 o superior (no un entorno OneBox), con Dynamics 365 Supply Chain Management, versión 10.0.7 o posterior. Si intenta instalar el complemento en un entorno OneBox, la instalación no se completará y deberá cancelarla.

1. Inicie sesión en LCS y abra el entorno deseado.
1. Vaya a **Detalles completos**.
1. Desplácese hacia abajo hasta la ficha desplegable **Complementos del entorno**.
1. Seleccione **Instalar un nuevo complemento**.
1. Seleccione **optimización de la planificación**.
1. Siga la guía de instalación y acepte los términos y condiciones.
1. Seleccione **Instalar**.
1. En la ficha desplegable **Complementos del entorno** debería ver que se está instalando Planning Optimization.
1. Después de unos minutos, **Instalando** debería cambiar a **Instalado** (es posible que deba actualizar la página). Cuando está instalado, está listo para activar la Optimización de planificación en Dynamics 365 Supply Chain Management.

El objetivo principal de instalar el complemento de Planning Optimization es conectar el servicio y el entorno. Por lo tanto, debe instalar el complemento por separado en cada entorno en el que utilizará Planning Optimization, independientemente de cualquier código movido entre los entornos.

### <a name="planning-optimization-integration"></a>Integración de la optimización de la planificación

Para configurar si el complemento de optimización de la planificación se debe usar para la planificación maestra, vaya **Planificación maestra** \> **Configuración** \> **Parámetros de optimización de la planificación**.

#### <a name="connection-status"></a>Estado de conexión

El estado de la conexión indica el estado actual de la conexión entre Supply Chain Management y el servicio de optimización de la planificación. La tabla siguiente muestra los posibles valores.

| Estado de conexión | Descripción | ¿Se puede usar optimización de la planificación? |
|---|---|---|
| Conectada | Una conexión se ha establecido entre el servicio de optimización de la planificación y Supply Chain Management. | Sí |
| Habilitando conexión | Una petición para activar la conexión al servicio de optimización de la planificación está actualmente en curso. | No |
| Desconectado | No hay conexión al servicio de optimización de la planificación. La conexión se puede cambiar desde LCS, según lo descrito antes en este tema. | No |
| Deshabilitando conexión | Una petición para desactivar la conexión al servicio de optimización de la planificación está actualmente en curso. | No |
| Obteniendo estado | El sistema está esperando por la información del estado del servicio de optimización de la planificación. | No |

#### <a name="the-use-planning-optimization-option"></a>La opción de optimización de la planificación de uso

Si se establece la opción **optimización de la planificación de uso** se determina el motor de planificación que se usa para la planificación maestra:

- **Sí**: la optimización de la planificación se utiliza para la planificación maestra.
- **No**: el motor de planificación de Supply Chain Management integrado se utiliza para la planificación maestra.

> [!NOTE]
> Si se activan los trabajos por lotes existentes de planificación creados para el motor de planificación de Supply Chain Management integrado se activan mientras que la opción **optimización de la planificación de uso** está establecida en **Sí**, estos trabajos fallarán.

### <a name="integration-with-the-setup"></a>Integración con la configuración

Si la vista previa de Optimización de la planificación está activada, la planificación maestra se realiza mediante el complemento de optimización de la planificación. En este caso, se ven afectados los resultados y las características de la planificación maestra.

## <a name="additional-resources"></a>Recursos adicionales

[Términos y condiciones de la vista previa](https://go.microsoft.com/fwlink/?linkid=2015274)

[Visión general de la optimización de la planificación](planning-optimization-overview.md)

[Análisis de aptitud de la optimización de la planificación](planning-optimization-fit-analysis.md)

[Ver el historial del plan y los registros de planificación](plan-history-logs.md)

[Aplicar filtros a un plan](plan-filters.md)

[Cancelar un trabajo de planificación](cancel-planning-job.md)
