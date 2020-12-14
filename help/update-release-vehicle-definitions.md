---
title: Actualizar definiciones del vehículo de lanzamiento
description: Este artículo detalla los distintos tipos de versiones [!DNL Experience Manager] , incluidas las versiones completas, los paquetes de funciones y los paquetes de servicios.
contentOwner: AK
translation-type: tm+mt
source-git-commit: 11ff4f7d66038a80697afe5f104c560137e130f4
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 5%

---


# [!DNL Experience Manager] actualizar las definiciones de los vehículos de lanzamiento  {#update-release-vehicle-definitions}

Este documento incluye detalles sobre los distintos tipos de [!DNL Adobe Experience Manager] versiones, incluidas versiones completas, paquetes de funciones y paquetes de servicios que [!DNL Adobe] ofrece a sus clientes.

>[!NOTE]
>
>Para consultar la programación de versiones de [!DNL Experience Manager] actualizaciones, consulte [[!DNL Experience Manager] roadmap de versiones de actualización](update-releases-roadmap.md)

## Versión completa {#full-release}

| Elementos | Descripción |
|-------|------|
| Definición | <ul> <li> Versión programada </li> <li> Admite rutas de actualización para versiones específicas, que se define en las notas de la versión </li> </ul> |
| Asignación de nombres | <ul> <li> Los números de versión de las versiones principales aumentan según la fórmula X+1.Y.Z. </li> <li> Los números de versión de versiones menores aumentan según la fórmula X.Y+1.Z </li> </ul> Si X es el número de versión principal, Y es el número de versión secundario y Z el número de parche. |
| Inclusiones | <ul> <li> Nuevas funciones </li> <li>  Mejoras </li> <li>  Corrección de errores </li> </ul> |
| Documentación | <ul> <li> Las notas de la versión están disponibles en el portal de documentación </li> <li> La documentación sobre funciones, mejoras y correcciones de errores está disponible en el portal de documentación </li> </ul> |
| Cadence | Anual |
| Disponibilidad e instalación | <ul> <li> Se entrega como un instalador de producto independiente </li> <li>  Disponible en el sitio web de licencias y Managed Services </li> <li> El sitio web de licencias puede requerir la migración del repositorio de contenido </li> </ul> |
| Nivel de prueba | Totalmente validado por el control de calidad |

## Paquete de servicio {#service-pack}

| Elemento | Descripción |
|-----|-----|
| Definición | <ul> <li> Versión programada </li> <li> Actualmente, no se puede revertir </li> </ul> |
| Asignación de nombres | <ul> <li> El número de revisión es un número de un solo dígito </li> <li> Después de la instalación, aumentará el dígito del parche del número de versión instalado, según la fórmula X.Y.Z.SPx </li> </ul> Si X es el número de versión principal, Y es el número de versión secundario y Z el número de parche. x es el número del Service Pack. |
| Inclusiones | <ul> <li> Nuevas funciones</li> <li>  Mejoras </li> <li> Corrección de errores </li> <li> Paquetes de funciones de interés común (si los hay) </li> </ul> |
| Documentación | <ul> <li> Notas de la versión disponibles en el portal de documentación </li> <li> Documentación sobre funciones, mejoras y correcciones de errores en el portal de documentación </li> </ul> |
| Cadence | Trimestral |
| Disponibilidad e instalación | <ul> <li> Entregado como paquete </li> <li> Disponible en distribución de software</li> <li>  Requiere una instalación funcional existente </li> </ul> |
| Nivel de prueba | <ul> <li> Se validó el control de calidad de todas las correcciones </li> <li>  Sentido general del paquete con ejecuciones de automatización </li> </ul> |

## Paquete de correcciones acumulativas  {#cumulative-fix-pack-aem}

| Elemento | Descripción |
|-----|-----|
| Definición | <ul> <li> Modelo de envío único de correcciones de liberación </li> <li> Paquete de contenido agregado que contiene el paquete de contenido de componentes individuales </li> <li>  Los archivos CFP son la sustitución de las correcciones rápidas y no se incluyen mejoras.  </li> </ul> |
| Asignación de nombres | X.Y.Z.CFPx <br> Donde X es el número de versión principal, Y es el número de versión secundario y Z el número de parche. x es el número acumulado del Service Pack. |
| Inclusiones | CFP es un paquete de correcciones acumulativo que contiene correcciones de todos los componentes en fechas especificadas. Por ejemplo, si un cliente aplica CFP3, entonces CFP3 = CFP1 + CFP2. |
| Documentación | Notas de la versión disponibles en el portal de documentación |
| Cadence | Trimestral |
| Disponibilidad e instalación | <ul> <li> Entregado como paquete </li> <li>  Disponible en distribución de software </li> <li>  Depende del Service Pack más reciente lanzado </li> <li>  CFP es autodependiente. Los clientes no tienen por qué preocuparse por encontrar o resolver dependencias. CFP debe instalarse en el Service Pack más reciente. </li> <li>  CFP se puede instalar como un paquete único, lo que mejora la experiencia del cliente.  </li> </ul> |
| Nivel de prueba | Control de calidad validado a nivel de integración y pruebas de regresión |

## Superposición {#overlay}

| Elemento | Detalles |
|-------|--------|
| Asignación de nombres | superposición-&lt;ID del vale> |
| Inclusiones | Corrección de errores de un archivo JS o JSP |
| Documentación | Ninguna |
| Cadence | Según sea necesario |
| Disponibilidad e instalación | <ul> <li> Entregado como paquete por [!DNL Experience Manager] Servicio de atención al cliente  </li> <li> No necesariamente se incluye en los Service Packs o en las versiones completas </li> </ul> |
| Nivel de prueba | Validado por el Servicio de atención al cliente |

## Feature Pack {#feature-pack}

| Elementos | Detalles |
|--------|-----|
| Definición | <ul> <li>Los paquetes de funciones son funcionalidades adicionales y se entregan a través de Service Packs. Si una versión [!DNL Experience Manager] ha lanzado su último Service Pack, Adobe no proporcionará ningún paquete de funciones para ella en el futuro. </li> <li> Los programas programados contienen mejoras del producto, programadas para una versión posterior del producto, pero entregadas con antelación según la decisión de [!DNL Adobe's] Administración de productos.</li> <li>  Las funciones siempre se combinan con la siguiente versión principal y luego se adaptan a la versión [!DNL Experience Manager] requerida por el cliente </li> <li>  Los paquetes de funciones de Interés común y GA se combinan en el siguiente Service Pack  </li> </ul> |
| Asignación de nombres | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inclusiones | <ul> <li> Nuevas funciones </li> <li> Mejoras </li> <li> Correcciones de errores (actualizaciones de productos incrementales) </li> </ul> |
| Documentación | La documentación está disponible en adobe.com. |
| Cadence | Varía con el área de producto |
| Disponibilidad e instalación | <ul> <li>Entregado mediante Service Packs </li> <li> Disponible en Distribución de software. Los clientes aceptan [!DNL Adobe's] Términos y condiciones a través de la distribución de software. </li> </ul> |
| Nivel de prueba | Los paquetes de funciones de disponibilidad general están validados por el control de calidad. |

* 1: Las correcciones OAK no se entregan como correcciones rápidas individuales. Sin embargo, se incluyen en la corrección urgente Acumulative Oak posterior. Si es necesario, se puede poner a disposición una compilación de diagnóstico sobre el último COFP. La condición previa es que el cliente tenga la última COFP en ejecución. Las compilaciones de diagnóstico solo proporcionan el mismo nivel de garantía de calidad que una corrección urgente. Por lo tanto, no proporcionan el mismo nivel de garantía de calidad que un paquete de correcciones acumulativo, un Service Pack o una versión del producto. La corrección final se entrega con la siguiente CFP.
