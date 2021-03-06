---
title: Contenido de formación organizativa de Power BI
description: Este tema describe el contenido de Finance and Operations - Formación organizativa de Power BI.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bbbb3069ffc43062e456721e189f671398514cfd
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685844"
---
# <a name="organizational-training-power-bi-content"></a>Contenido de formación organizativa de Power BI

[!include [banner](../includes/banner.md)]

Este tema describe el contenido de Finance and Operations - Formación organizativa de Power BI.

## <a name="reports-that-are-included-in-the-content-pack"></a>Informes que se incluyen en el paquete de contenido
Tras conectar el paquete de contenido con sus datos, los informes muestran los datos de su organización. Si nunca antes ha utilizado Microsoft Power BI, consulte [Aprendizaje dirigido para Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData) para obtener más información acerca de la aplicación. Los informes incluidos en el paquete de contenido tienen gráficos y tablas que contienen información adicional. En la siguiente tabla se describen los informes.

| Informe          | Contenido                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Análisis de curso | Registro por ubicación, asistentes del curso por estado y lista de registro |
| Tipos de cursos    | Tipo de curso por aptitud                                                       |

Puede filtrar los gráficos e iconos en estos informes y anclar los gráficos e iconos al panel de información. Para obtener más información acerca de cómo filtrar y anclar en Power BI, consulte [Crear y configurar un panel de información](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Comprensión del modelo de datos y de las entidades
Los datos de la aplicación se usan para rellenar los informes del paquete de contenido sobre formación organizativa. En la tabla siguiente se muestran las entidades en las que se basaba el paquete de contenido.

| Entidad                    | Contenido                                                         | Relaciones con otras entidades |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Training\_CalendarOffset  | Desplazamientos del calendario para dividir informes                                | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Company         | Empresas para filtrar informes por                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Course          | Curso, descripción, nombre del instructor, ubicación, sitio y estado | Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill |
| Training\_CourseAgenda    | Programa, curso, y horas de inicio y finalización                          | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Course |
| Training\_CourseAttendees | Nombre, estado, trabajo y fecha de registro                         | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position |
| Training\_CourseSkill     | Aptitudes, tipo de aptitud y nivel                                     | Training\_Course |
| Training\_Date            | Días, semanas, meses y años                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Demographics    | Fecha de nacimiento, género, origen étnico y estado civil         | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Employment      | Fecha de inicio, fecha final y fecha de transición                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Job             | Función tipo y cargo                                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Position        | Puesto, título y equivalente a jornada completa                  | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_WorkerName      | Nombre, apellido y nombre completo                             | Training\_CourseAttendees |
| Training\_WorkerTitle     | Cargo y fecha de antigüedad                                         | Training\_CourseAttendees |
