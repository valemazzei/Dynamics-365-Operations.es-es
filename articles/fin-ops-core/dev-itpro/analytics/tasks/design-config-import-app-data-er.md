---
title: Diseñar configuraciones de ER para analizar documentos entrantes
description: Este procedimiento muestra cómo diseñar las configuraciones de los informes electrónicos (ER) para analizar un documento electrónico entrante.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 446a4676ad00c93d691d3048408c32d7ad373d2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682102"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Diseñar configuraciones de ER para analizar documentos entrantes

[!include [banner](../../includes/banner.md)]

Este procedimiento muestra cómo diseñar las configuraciones de los informes electrónicos (ER) para analizar un documento electrónico entrante. En este procedimiento, importará las configuraciones de ER necesarias que se han creado para la empresa de ejemplo, Litware, Inc. y las usará para analizar documentos electrónicos entrantes. Para completar los pasos de este procedimiento, primero debe completar los pasos del procedimiento, "ER: Crear un proveedor de configuraciones y marcarlo como activo".

Este procedimiento se ha creado para los usuarios con los roles Administrador del sistema o Desarrollador de informes electrónicos asignados.

Estos pasos se pueden completar mediante cualquier conjunto de datos. Antes de comenzar, descargue y guarde los archivos enumerados en el tema "Analizar documentos de entrada para actualizar datos de aplicación" ([Analizar documentos entrantes](../parse-incoming-electronic-documents.md)). Los archivos son: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Vaya a Administración de la organización > Espacios de trabajo > Informes electrónicos.
    * Asegúrese de que el proveedor de configuración de la empresa de ejemplo “Litware, Inc.” está disponible y marcado como Activo. Si no ve a este proveedor de configuración, complete los pasos del procedimiento "Creación de un proveedor de configuración y marcarlo como activo".
2. Seleccione Configuraciones de informes.
    * El escenario siguiente se usará para mostrar las capacidades de analizar documentos electrónicos entrantes en formato XML: la aplicación ERP solicita datos del servicio Web (como servicio fiscal [EFSTA](http://efsta.org/)) y analiza las respuestas de entrada para actualizar los datos de la aplicación en consecuencia. Para la forma más eficaz de analizar, se usa un único formato de ER a pesar de la estructura diferente de los documentos de entrada previstos en formato XML.

## <a name="import-and-review-er-configurations"></a>Importar y revisar configuraciones de ER

Importe la configuración del modelo de ER que contiene el modelo de datos de ejemplo diseñado para almacenar los detalles del archivo de entrada.

1. Seleccione Intercambiar.
2. Seleccione Cargar desde un archivo XML.
    * Seleccione Examinar y seleccione el archivo model.xml de EFSTA.
3. Seleccione Aceptar.
4. En el árbol, seleccione 'EFSTA model'.
5. Seleccione Diseñador.
    * Revisar la estructura del modelo de datos importado. La enumeración enumType se define para reconocer los siguientes tipos de respuestas de servicio: para obtener la confirmación del envío de la transacción, para obtener información acerca de la última transacción registrada, y para reconocer tipos de respuesta no admitidos.
6. En el árbol, expanda 'Response'.
    * El elemento raíz “respuesta” se define para especificar el tipo de datos que se debe tomar de una respuesta de servicio no admitida para actualizar los datos de la aplicación en consecuencia.
7. Cierre la página.
    * Se importará la configuración del formato de ER que especifica cómo los documentos de entrada se analizarán para almacenar datos en el modelo de datos de ER.
8. Seleccione Intercambiar.
9. Seleccione Cargar desde un archivo XML.
    * Seleccione Examinar y seleccione el archivo format.xml de EFSTA.
10. Seleccione Aceptar.
11. En el árbol, expanda 'EFSTA model'.
12. En el árbol, seleccione 'EFSTA model\EFSTA format'.
13. Seleccione Diseñador.
14. Seleccione Expandir/Contraer.
    * El elemento de formato CASE se usa como la raíz y contiene tres elementos anidados FILE, lo que significa que este formato se ha diseñado para analizar los archivos entrantes de varios formatos.
15. En el árbol, seleccione 'Responses\Transaction completion\TraC'.
    * La respuesta sobre la transacción enviada comienza desde el elemento raíz de "TraC".
16. En el árbol, seleccione 'Responses\Last transaction request\Tra'.
    * La respuesta sobre la última transacción enviada comienza desde el elemento raíz de "Era".
17. En el árbol, seleccione 'Responses\Unexpected response\Text'.
    * El tercer elemento FILE con el elemento TEXT anidado se ha agregado para reconocer cualquier otro tipo de respuestas que difiera de la respuesta mencionada anteriormente.
18. Seleccione Asignar formato a modelo.
    * Esta asignación de modelo contiene la definición del flujo de datos para almacenar los detalles del documento de entrada analizado con el uso de los elementos del modelo de datos.
19. Seleccione Diseñador.
20. En el árbol, expanda "formato".
21. En el árbol, expanda 'format\Responses: Case(Responses)'.
    * Revisar la estructura del origen de datos "format". Los tres tipos de respuesta se ofrecen por separado.
22. En el árbol, seleccione 'format\Responses: Case(Responses)\aType'.
    * El elemento de origen de datos “aType” se ha agregado para indicar el tipo de respuesta y está enlazado al elemento de modelo de datos “Type”.
23. Seleccione la pestaña Validaciones.
24. En el árbol, seleccione 'Type = format.Responses.aType'.
    * La validación de ER se ha configurado para informar al usuario sobre la situación cuando la estructura de respuesta no coincide con la confirmación tras el envío de la transacción o la información sobre la última transacción enviada (caso de respuesta no admitido).
25. Cierre la página.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Ejecución de la asignación de modelos del formato de ER configurado para analizar archivos entrantes

Se ejecutará la asignación de modelo creado para objetivos de prueba, para ver cómo el formato de ER configurado analizará las respuestas de servicio de entrada. Este paso usa distintos archivos XML para simular distintos tipos de respuestas de servicios Web.

1. Abre el archivo Response1.xml en un lector de xml como un explorador web. Este archivo contiene los detalles de la confirmación sobre la transacción completada (“TraC” es el elemento raíz).
2. Seleccione Ejecutar.
    * Seleccione Examinar y seleccione el archivo Response1.xml.
3. Seleccione Aceptar.
    * Revise la salida generada. El tipo de respuesta se ha reconocido y analizado correctamente (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` significa caso de finalización de la transacción).
    * Abre el archivo Response2.xml en un lector de XML. Este archivo contiene información sobre la última transacción enviada (`Tra` es el elemento raíz).
4. Seleccione Ejecutar.
    * Seleccione Examinar y seleccione el archivo Response2.xml.
5. Seleccione Aceptar.
    * Revise la salida generada. El tipo de respuesta se ha reconocido y analizado correctamente (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` significa caso de reinicio del sistema).
    * Abre el archivo Response3.xml en un lector de XML. Este archivo comienza desde el elemento de raíz TraZ y que esta estructura no se ha configurado con el formato de ER.
6. Seleccione Ejecutar.
    * Seleccione Examinar y seleccione el archivo Response3.xml.
7. Seleccione Aceptar.
    * Revise la salida generada. El tipo de respuesta se ha reconocido correctamente como no admitido (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). El mensaje correspondiente se ha puesto en el Registro de información (según el valor de la validación de ER), y la mayor parte del modelo de datos no se ha completado.
    * Abre el archivo Response4.xml en un lector de XML. La estructura de este archivo casi es la misma que el archivo Response1.xml analizado correctamente, excepto la secuencia de elementos anidados del elemento raíz “TraC”.
8. Seleccione Ejecutar.
    * Seleccione Examinar y seleccione el archivo Response4.xml.
9. Seleccione Aceptar.
    * Revise la salida generada. El tipo de respuesta se ha reconocido correctamente como no admitido (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`)). El mensaje correspondiente se ha puesto en el Registro de información y la mayor parte del modelo de datos no se ha completado. Este comportamiento se debe a que la configuración actual de este formato de ER presupone una determinada secuencia de elementos anidados del elemento raíz del archivo de entrada.
10. Cierre la página.
11. En el árbol, seleccione 'Responses\Transaction completion\TraC'.
12. En el campo de orden de análisis de elementos anidados seleccione “Cualquiera”.
    * Seleccione Cualquiera en el campo "Orden de análisis de los elementos anidados" para permitir cualquier secuencia de elementos anidados para este elemento de XML de la raíz.
13. Seleccione Guardar.
14. Seleccione Asignar formato a modelo.
15. Seleccione Ejecutar.
    * Seleccione Examinar y seleccione el archivo Response4.xml.
16. Seleccione Aceptar.
    * Revise la salida generada. El tipo de respuesta ha sido reconocido correctamente como igual para el archivo Response1.xml.
