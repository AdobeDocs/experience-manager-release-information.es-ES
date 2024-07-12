---
title: Actualizar definiciones vehiculares de versiones
description: En este artículo se detallan los distintos tipos de versiones de  [!DNL Experience Manager] , incluidas las versiones completas, los paquetes de funciones y los Service Pack.
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 85%

---

# Actualizar definiciones vehiculares de versiones de [!DNL Experience Manager]  {#update-release-vehicle-definitions}

Este documento incluye detalles sobre los distintos tipos de versiones de [!DNL Adobe Experience Manager], incluidas versiones completas, paquetes de funciones y paquetes de servicio que [!DNL Adobe] ofrece a sus clientes.

>[!NOTE]
>
>Para consultar la programación de versiones de actualización de [!DNL Experience Manager], consulte el programa de actualizaciones de [[!DNL Experience Manager] ](update-releases-roadmap.md)

## Versión completa {#full-release}

| Elementos | Descripción |
|-------|------|
| Definición | <ul> <li> Versión programada </li> <li> Admite rutas de actualización para versiones específicas definidas en las notas de la versión </li> </ul> |
| Nombre | <ul> <li> Los números de versión de las versiones principales aumentan según la fórmula X+1.Y.Z. </li> <li> Los números de versión de versiones menores aumentan según la fórmula X.Y+1.Z </li> </ul> Si X es el número de versión principal, Y es el número de versión secundario y Z el número de parche. |
| Inclusiones | <ul> <li> Nuevas funciones </li> <li>  Mejoras </li> <li>  Corrección de errores </li> </ul> |
| Documentación | <ul> <li> Las notas de la versión están disponibles en el portal de documentación </li> <li> La documentación sobre funciones, mejoras y correcciones de errores está disponible en el portal de documentación </li> </ul> |
| Cadencia | Anual |
| Disponibilidad e instalación | <ul> <li> Se entrega como un instalador de producto independiente </li> <li>  Disponible en el sitio web de licencias y Servicios administrados </li> <li> El sitio web de licencias puede requerir la migración del repositorio de contenido </li> </ul> |
| Nivel de prueba | Totalmente validado por el control de calidad |

## Service Pack {#service-pack}

| Elemento | Descripción |
|-----|-----|
| Definición | <ul> <li> Versión programada </li> <li> Actualmente, no se puede revertir </li> </ul> |
| Nombre | <ul> <li> El número de revisión es un número de un solo dígito </li> <li> Después de la instalación, aumentará el dígito del parche del número de versión instalado, según la fórmula X.Y.Z.SPx </li> </ul> Si X es el número de versión principal, Y es el número de versión secundario y Z el número de parche. x es el número del paquete de servicio. |
| Inclusiones | <ul> <li> Nuevas funciones</li> <li>  Mejoras </li> <li> Corrección de errores </li> <li> Paquetes de funciones de interés común (si los hay) </li> </ul> |
| Documentación | <ul> <li> Las notas de la versión están disponibles en el portal de documentación </li> <li> Documentación sobre funciones, mejoras y correcciones de errores en el portal de documentación </li> </ul> |
| Cadencia | Trimestral |
| Disponibilidad e instalación | <ul> <li> Entregado como paquete </li> <li> Disponible en distribución de software</li> <li>  Requiere una instalación funcional existente </li> </ul> |
| Nivel de prueba | <ul> <li> Se validó el control de calidad de todas las correcciones </li> <li>  Sentido general del paquete con ejecuciones de automatización </li> </ul> |

## Fix Pack acumulativo {#cumulative-fix-pack-aem}

| Elemento | Descripción |
|-----|-----|
| Definición | <ul> <li> Modelo de envío único de correcciones de liberación </li> <li> Paquete de contenido agregado que contiene el paquete de contenido de componentes individuales </li> <li>  Los archivos CFP son la sustitución de las correcciones rápidas y no se incluyen mejoras.  </li> </ul> |
| Nombre | X.Y.Z.CFPx <br> Donde X es el número de versión principal, Y es el número de versión secundaria y Z el número de parche. x es el número acumulado del paquete de servicio. |
| Inclusiones | CFP es un paquete de correcciones acumulativo que contiene correcciones de todos los componentes en fechas especificadas. Por ejemplo, si un cliente aplica CFP3, entonces CFP3 = CFP1 + CFP2. |
| Documentación | Las notas de la versión están disponibles en el portal de documentación |
| Cadencia | Trimestral |
| Disponibilidad e instalación | <ul> <li> Entregado como paquete </li> <li>  Disponible en distribución de software </li> <li>  Depende del Service Pack más reciente lanzado </li> <li>  CFP es autodependiente. Los clientes no necesitan preocuparse por encontrar o resolver dependencias. CFP debe instalarse en el paquete de servicio más reciente. </li> <li>  CFP se puede instalar como un paquete único, lo que mejora la experiencia del cliente.  </li> </ul> |
| Nivel de prueba | Control de calidad validado a nivel de integración y pruebas de regresión |

## Superposición {#overlay}

| Elemento | Detalles |
|-------|--------|
| Nombre | overlay-&lt;ticket ID> |
| Inclusiones | Corrección de errores de un archivo JS o JSP |
| Documentación | Ninguna |
| Cadencia | Según sea necesario |
| Disponibilidad e instalación | <ul> <li> Entregado como paquete por el servicio de atención al cliente de [!DNL Experience Manager]  </li> <li> No necesariamente se incluye en los paquetes de servicio o en las versiones completas </li> </ul> |
| Nivel de prueba | Validado por el Servicio de atención al cliente |

## Feature Pack {#feature-pack}

| Elementos | Detalles |
|--------|-----|
| Definición | <ul> <li>Los paquetes de funciones son funcionalidades adicionales y se entregan a través de paquetes de servicio. Si una versión de [!DNL Experience Manager] ha lanzado su último paquete de servicio, Adobe no proporcionará ningún paquete de funciones para ella en el futuro. </li> <li> Los programas configurados contienen mejoras del producto, programadas para una versión posterior del producto, pero entregadas con antelación según la decisión de la administración de productos de [!DNL Adobe's].</li> <li>  Las funciones siempre se combinan con la siguiente versión principal. Luego se transfieren a la versión [!DNL Experience Manager] requerida por el cliente </li> <li>  Los paquetes de funciones de Interés común y GA se combinan en el siguiente paquete de servicio  </li> </ul> |
| Nombre | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inclusiones | <ul> <li> Nuevas funciones </li> <li> Mejoras </li> <li> Correcciones de errores (actualizaciones de productos incrementales) </li> </ul> |
| Documentación | La documentación está disponible en adobe.com. |
| Cadencia | Varía con el área de producto |
| Disponibilidad e instalación | <ul> <li>Entregado mediante paquetes de servicio </li> <li> Disponible en la distribución de software. Los clientes aceptan los términos y condiciones de [!DNL Adobe's] a través de la distribución de software. </li> </ul> |
| Nivel de prueba | Los paquetes de funciones de disponibilidad general están validados por el control de calidad. |

* 1: Las correcciones de Oak no se entregan como correcciones rápidas individuales. Sin embargo, se incluyen en la revisión para Cumulative Oak posterior. En caso necesario, se puede disponer de un diagnóstico basado en el último COFP. La condición previa es que el cliente tenga la última COFP en ejecución. Las compilaciones de diagnóstico solo proporcionan el mismo nivel de garantía de calidad que una revisión. Por lo tanto, no proporcionan el mismo nivel de garantía de calidad que un Fix Pack acumulativo, un Service Pack o una versión del producto. La corrección final se entrega con la siguiente CFP.
