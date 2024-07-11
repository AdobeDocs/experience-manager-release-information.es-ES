---
title: Fix Pack acumulativo de AEM 6.2
description: AEM Obtenga más información acerca de las notas de la versión del paquete de correcciones acumulativas de 6.2.
exl-id: f1c2d4ff-590b-46b5-b2b1-e2b5141f7cc0
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '21082'
ht-degree: 72%

---

# AEM Notas de la versión del paquete de correcciones acumulativas de.2{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived by way of UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Información de la versión {#release-information}

| **Producto** | Adobe Experience Manager |
|---|---|
| **Versión** | 6.2 |
| **Versión** | Paquete de correcciones acumulativas 6.2 SP1-CFP20 |
| **Requisitos previos** | [Paquete de servicio 1 de AEM 6.2](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) |
| **Disponibilidad general** | 6 de junio de 2019 |

### Paquete de correcciones acumulativas {#cumulative-fix-pack}

Adobe presentó un modelo de entrega única para la publicación de correcciones. En lugar de lanzar correcciones urgentes para problemas individuales, Adobe ahora publica un paquete de correcciones acumulativas (CFP) todos los meses (sujeto a la aprobación de comprobaciones de calidad). Un CFP es un paquete de contenido agregado para varias correcciones. Los CFP incluyen principalmente correcciones de errores, pero también pueden incluir paquetes de funciones. Tienen las siguientes ventajas con respecto a las versiones de revisiones individuales:

* De naturaleza acumulativa (por ejemplo, un CFP contiene correcciones entregadas a través de CFP anteriores)
* Mayor control de calidad
* Instalación simplificada (el usuario instala un CFP como paquete único que no tiene dependencias, excepto el último Service Pack)

Para obtener más información sobre el CFP y otros tipos de liberaciones, consulte [Vehículo de versiones de mantenimiento](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

## Información de la versión {#about-the-release}

El paquete de correcciones acumulativas 6.2 SP1-CFP20 de AEM es el último paquete de correcciones acumulativas para AEM 6.2 y es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de [AEM 6.2 SP1](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

>[!CAUTION]
>
>La aplicación de CFP sin validar la compatibilidad entre los paquetes de funciones instalados puede provocar errores en el sistema o la pérdida de las configuraciones personalizadas, lo que podría requerir la restauración desde la copia de seguridad.

>[!NOTE]
>
>* Se incluye un nuevo paquete Sling `discovery- api` Johnzon 1.0.0 con el paquete de correcciones acumulativas de AEM 6.2 SP1-CFP10. Además, se ha añadido un usuario de servicio sling-discovery con privilegios de lectura y escritura para el nodo */var/discovery* en el repositorio de CRX.
>
>* Se ha añadido un paquete de correo electrónico de Apache commons **org.apache.commons/commons-email/1.5** que reemplaza **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
>
>* Adobe recomienda implementar CFP mediante la carpeta de instalación para clientes con muchos usuarios en la instancia de AEM.
>

## Problemas incluidos {#issues-included}

Esta sección enumera todos los problemas y revisiones incluidos en la CFP actual.

Además, este CFP incluye revisiones entregadas en [paquetes anteriores de correcciones acumulativas](#previous).

### Integración {#integration}

* Backporting múltiple de Segmentación de campañas, mejoras en la personalización. NPR-29163: revisión para CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler entra en un bucle infinito y causa actualizaciones de nodos en instancias de publicación. NPR-28561: revisión para CQ-4263096

### DAM: General {#dam-general}

* No se puede mostrar ni ocultar el botón de replicación para usuarios que no son administradores en carpetas DAM específicas. NPR-29026: revisión para CQ-4265361

### Vulnerabilidad {#vulnerability}

* AEM El marco de protección CSRF no funciona con los formularios de base de datos de la. NPR-28612: revisión para GRANITE-22231

### Forms {#forms}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [Versiones de AEM Forms](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package}

>[!NOTE]
>
>Para los clientes de AEM Forms, es esencial instalar el paquete de complementos de AEM Forms AEM después de instalar cualquier paquete de servicio, paquete acumulativo o paquete de funciones de.

>[!NOTE]
>
>Los paquetes de complementos de AEM Forms ayudan a alinear la funcionalidad de los formularios con los paquetes de servicios de AEM y los paquetes de correcciones acumulativas. Por lo tanto, es esencial instalar el paquete de complementos de AEM Forms después de instalar cualquier paquete de servicio, paquete acumulativo o paquete de funciones de AEM.

#### Formularios adaptables {#adaptive-forms}

* Problemas de uso con el componente anotaciones para dispositivos iOS 12.1. NPR-29082: revisión para CQ-4261765

#### Forms: seguridad de documentos {#forms-document-security}

* La comprobación de todas las firmas en un PDF mediante firma electrónica avanzada en formato PDF (PAdES) inicia la excepción InvalidOperationException. NPR-27848: revisión para CQ-4244837

#### Forms: Correspondencia {#forms-correspondence}

* Al obtener una vista previa de la carta como PDF, el campo de texto colocado en la página principal no respeta el valor introducido desde la pestaña de datos o según el vínculo de datos especificado. NPR-29239: revisión para CQ-4266856.

#### Forms: comunicación interactiva {#forms-interactive-communication}

* Cuando se agrega un apóstrofe, los campos rellenados previamente en la letra aparecen como caracteres ASCII en lugar de alfabetos normales. NPR-28863: revisión para CQ-4262900

### Instalador JEE de Forms {#forms-jee-installer}

* No hay nuevas correcciones en el instalador JEE de AEM Forms.

## Revisiones y paquetes de funciones incluidos en los paquetes de correcciones acumulativas anteriores {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Paquete de correcciones acumulativas 19 {#cumulative-fix-pack-1}

El paquete de correcciones acumulativas 6.2 SP1-CFP19 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de [AEM 6.2 SP1](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha habilitado la compatibilidad de la API v3.0 de MS® Translator con AEM 6.2
* Se agregó un mensaje de registro tras la instalación correcta del paquete para todos los SP, CFP y HF.

### Recursos {#assets}

* No puede cambiar el nombre de una carpeta DAM si falta el permiso Editar ACL. NPR-27555: revisión para CQ-104652
* La herramienta de edición de ajustes preestablecidos de imagen no responde en la versión 6.2.1 del CFP 17 y posterior. NPR-28147: revisión para CQ-4261041

### Sites {#sites}

* El Verificador de vínculos no completa el trabajo, se queda bloqueado con vínculos que no responden. NPR-27373: revisión para CQ-4256030
* El archivo de segmento no se carga correctamente debido a una ruta raíz adicional que rompe la ruta del segmento. NPR-28014: revisión para CQ-4260332

### Integración {#integration-1}

* La cancelación heredada de LiveCopy no funciona correctamente en contenedores de destino. NPR-28129: revisión para CQ-4259813
* `cq:actions` no se toman en consideración para un componente específico. NPR-27616: revisión para CQ-4257497

* La visualización del icono para romper la herencia no es coherente. NPR-27671: revisión para CQ-4257779

### Felix {#felix}

* El detalle del componente de la consola web falla con el error 500 después de la instalación del CFP 18 en la instancia del paquete de servicio 1 de AEM 6.2. NPR-28350: revisión para CQ-4261095

### Traducción {#translation}

* Soporte habilitado con el servicio de MS® Translator en AEM 6.3 después de actualizar MS® Translator a la API v3.0. NPR-28123: revisión para CQ-4259096

### IU: bases {#ui-foundation}

* El calendario de sitios de OOTB muestra fechas incorrectas. NPR-28392

### Granite {#granite}

* El diccionario no se invalida para los paquetes de recursos que usan `sling:basename`. NPR-27624

### Soporte {#sustenance}

* Los registros de actividad del administrador de paquetes deben extraerse en un archivo de registro independiente. NPR-27323: revisión para Granite-14866
* Se mostrará una frase, redacción o línea de registro estandarizada en el error.log cuando se complete la instalación. NPR-27835
* El complemento del paquete Granite elige la dependencia de una versión inferior de org.apache.sling.i18n. Revisión para CQ-4263245
* El paquete com.adobe.cq.com.adobe.cq.ui.commons se elimina al instalar el último CFP después de 6.2SP1-CFP15. Revisión para CQ-4258808

### Forms {#forms-1}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [Versiones de AEM Forms](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-1}

#### Formularios adaptables {#adaptive-forms-1}

* Vulnerabilidad de la inyección de XML con AEM Forms. NPR-27843: revisión para CQ-4257315

### Instalador JEE de Forms {#forms-jee-installer-1}

* No hay nuevas correcciones en el instalador JEE de AEM Forms.

### Paquetes de contenido y paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included}

Los siguientes documentos de texto enumeran los paquetes OSGI y los paquetes de contenido incluidos en el CFP.

Lista de paquetes OSGi incluidos en el SP1-CFP19 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp19_osgi_bundles.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP19 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp19_content_packages.txt)

### Paquete de correcciones acumulativas 18 {#cumulative-fix-pack-2}

El paquete de correcciones acumulativas 6.2 SP1-CFP18 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de [AEM 6.2 SP1](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se añadió la compatibilidad en DAM CommandLineProcess para acabar con el proceso de larga ejecución.
* Se corrigió una fuga de sesión en ReplicationEventListener.
* Se ha añadido la compatibilidad de redireccionamiento al componente de página principal.

### Recursos {#assets-1}

* Los procesos `Camera RAW` se quedan atascados durante los períodos de ingesta masiva que eventualmente bloquean todo el procesamiento del flujo de trabajo. NPR-26990: revisión para NPR-23860
* La funcionalidad de descarga utiliza AEM Assets mediante un servlet de descarga de recursos que permite a los usuarios anónimos descargar todos los recursos. NPR-27054, revisión para CQ-4254732
* Los caracteres especiales aparecen desglosados en la línea de asunto de las plantillas de correo electrónico en AEM. NPR-26470: revisión para CQ-4252368

### Sites {#sites-1}

* Debido a un comportamiento incorrecto de la clase ConfigPostProcessor, al suspender la imagen principal se elimina el tipo de mezcla `cq:LiveRelationship` de la página secundaria. NPR-26745: revisión para CQ-4254163
* Añadir la compatibilidad de redireccionamiento al componente de página principal. NPR-26576: revisión para CQ-110529
* Migrar context hub a `jQuery` 3.  NPR-26956: revisión para CQ-4255472
* Los campos de entrada de anclaje aparecen fuera de la sección visible del explorador en el cuadro de diálogo hasta que se maximiza. NPR-26852: revisión para CQ-4255019
* Copiar y pegar el texto insertando no deseados &lt;br> en el fragmento de contenido. NPR-26660: revisión para CRTE-151
* El administrador del sitio clásico no muestra la lista en el panel derecho de algunas páginas. NPR-27247: revisión para CQ-4251621
* (IU clásica) Los intentos de mover o cambiar el nombre de las páginas generan un error: “Error al mover la página”. NPR-27179: revisión para CQ-4235907

### Integración {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever recorre todo el árbol para recopilar las marcas disponibles. NPR-27060: revisión para CQ-4255790

### WCM: componentes base {#wcm-foundation-components}

* Problema de funcionalidad de búsqueda con el componente de lista de Foundation. NPR-26817: revisión para CQ-4250324

### Plataforma {#platform}

* Debido al carácter especial guion largo, el publicador tiene problemas para vaciar la caché. NPR-27199: revisión para CQ-4242790

### Granite {#granite-1}

* El validador de paquetes no valida los paquetes incluidos en CFP/SP. NPR-26775: revisión para Granite-22825

### Replicación {#replication}

* Fuga de sesiones JCR en ReplicationListener. NPR-27063: revisión para CQ-4232088

### Forms {#forms-2}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [Versiones de AEM Forms](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-2}

* No hay nuevas correcciones en el paquete de complementos de AEM Forms.

### Instalador JEE de Forms {#forms-jee-installer-2}

* No hay nuevas correcciones en el instalador JEE de AEM Forms.

#### Paquetes de contenido y paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-1}

Lista de paquetes OSGi incluidos en el SP1-CFP18 de AEM 6.2

[Obtener archivo](assets/do-not-localize/62cfp18updated_bundles.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP18 de AEM 6.2

[Obtener archivo](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Paquete de correcciones acumulativas 17 {#cumulative-fix-pack-3}

El paquete de correcciones acumulativas 6.2 SP1-CFP17 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de [AEM 6.2 SP1](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Compatibilidad añadida en las direcciones URL sin extensión del sitio en at-integration.js
* Se ha eliminado el importador de encuestas S7 de la configuración del servicio en la nube S7.
* Cambios en la vista del público para admitir la estructura de carpetas para la implementación de varios inquilinos.
* Actualización a jqueryui clientlib v1.12.1.

### Recursos {#assets-2}

* Para iniciar flujos de trabajo desde la IU de recursos, el usuario debe tener permisos de escritura, eliminación o modificación. NPR-25688: revisión para CQ-4250140
* Los botones Publicar y Cancelar la publicación permanecen visibles incluso para los usuarios sin los permisos de “replicar”. NPR-25094
* (Flujo de trabajo) El flujo de trabajo de los recursos de etiquetas inteligentes no se procesa a través de la configuración del proxy AEM. NPR-25915: revisión para CQ-4248202
* Eliminar el importador de encuestas S7 de la configuración del servicio en la nube S7. NPR-25239: revisión para CQ-95236

### Sites {#sites-2}

* Los flujos de trabajo iniciados desde el Editor -> Información de página, contienen la ruta de contexto en la carga útil. NPR-26389: revisión para CQ-76804
* (Comprobador de vínculos externos) Los vínculos https no válidos aparecen como vínculos válidos. NPR-25541: revisión para CQ-4201333
* (IU clásica) Al crear una página independiente en una Live Copy, la página se crea como una Live Copy. NPR-25610: revisión para CQ-4249801
* Problemas con los recursos de publicación asociados con el componente de importación de diseños cuando se activa una página. NPR-25638: revisión para CQ-102532
* La barra de herramientas del Editor de texto enriquecido RTE cubre la lista de selección. NPR-25165: revisión para CQ-4248948
* Migración de context hub a jquery 3. NPR-25059: revisión para Granite-19902
* Para un componente Parsys anidado, siempre se aplica el primer diseño satisfactorio (con la ruta menos anidada) de varios componentes disponibles. Para obtener más información, consulte [Resolución de ruta de diseño](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-25250: revisión para CQ-4246276

### Integración {#integration-3}

* Con la integración de Target OOTB, la segmentación de un componente procesa toda la página en lugar de un componente de destino vacío. NPR-25273: revisión para CQ-4248003
* En el modo de segmentación, si se interrumpe la herencia el componente seguirá mostrándose como destino con la herencia no interrumpida en el modo de edición. NPR-25324: revisión para CQ-4248162
* Cuando se define una personalización en una página y se resuelve un público, la experiencia correspondiente se muestra en el modo de edición. NPR-25731: revisión para CQ-4249465
* URL de teaser errónea al usar AEM con una ruta de contexto no predeterminada. NPR-25971: revisión para CQ-4250953
* Representación en blanco al utilizar la exclusión. NPR-25295: revisión para CQ-4246792
* Las experiencias eliminadas del entorno de autor nunca se eliminan del sitio de publicación tras la activación de la página. NPR-24869: revisión para CQ-4247832

### DAM: Cliente DM {#dam-dm-client}

* (Chrome, Firefox) VideoPlayer ignora los clics del ratón en los dispositivos táctiles. Revisión para CQ-4247370

### Plataforma {#platform-1}

* Permite configurar el número máximo de reintentos al adquirir o liberar un paquete. NPR-25328: revisión para Granite-22376
* Registro incorrecto si hay errores de replicación. NPR-25308: revisión para CQ-4249402
* La instalación de Forms AEM 6.2 Forms CFP8 a CFP14 provoca que el POI de Apache falle. NPR-25053: revisión para Granite-21771

### Granite {#granite-2}

* El proceso de sincronización del usuario falla con la excepción OakConstraint0022. NPR-25729: revisión para Oak-7428

### Comunidades {#communities}

* El paquete cq-social-as-provider no inicia con las versiones 3.x del controlador Mongo. NPR-26271: revisión para CQ-4252710

### IU: bases {#ui-foundation-1}

* Actualización a jqueryui clientlib v1.12.1. NPR-25090: revisión para Granite-21981, CQ-4248897

* (Omnisearch): La propiedad “Title” es vulnerable a ejecución de scripts en sitios múltiples (XSS) en Sites. NPR-24994: revisión para Granite-19933

### Forms {#forms-3}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [Versiones de AEM Forms](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-3}

#### Formularios adaptables {#adaptive-forms-2}

* Codificación incorrecta al enviar datos desde el formulario adaptable. NPR-25539

#### Forms: administración {#forms-management}

* Los recursos de formulario no relacionados aparecen como referencias al publicar la página. NPR-26167: revisión para CQ-4251004

### Instalador JEE de Forms {#forms-jee-installer-3}

#### Document Security {#document-security}

* La variable se rellena como Lista de tipo de datos, el subtipo es de cadena, pero se produce el error &quot;no se puede forzar el objeto&quot;. NPR-26194: revisión para CQ-4252287
* No se puede acceder a las configuraciones de marca de agua después de instalar 6.2-SP1-CFP15. NPR-26130: revisión para CQ-4250984

### Paquetes de contenido y paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-2}

Lista de paquetes OSGi incluidos en el SP1-CFP17 de AEM 6.2

[Obtener archivo](assets/do-not-localize/62cfp17updated_bundles.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP17 de AEM 6.2

[Obtener archivo](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Paquete de correcciones acumulativas 16 {#cumulative-fix-pack-4}

El paquete de correcciones acumulativas 6.2 SP1-CFP16 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de [AEM 6.2 SP1](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha añadido la compatibilidad con STARTTLS en el servicio de correo de Day CQ.
* Se ha corregido la alineación de los iconos de ContextHub en la ventana emergente de perfil.
* Correcciones en la funcionalidad de mostrar u ocultar del componente desplegable.
* Actualice a la última versión de Jackson 2.8.11

### Recursos {#assets-3}

* No se puede iniciar un flujo de trabajo desde una vista de lista. NPR-24393: revisión para CQ-4245788
* (Firefox/Chrome) No se pueden descargar recursos en la página Uso compartido de recursos. NPR-24523: revisión para CQ-4224408
* Se ha aumentado la calidad predeterminada para la previsualización de vídeo en AEM. NPR-24148: revisión para CQ-4244310

### Integración {#integration-4}

* Cuando un componente está dirigido a una instancia de publicación, aparece un parpadeo que muestra la experiencia predeterminada antes de la experiencia de destino. NPR-23992: revisión para CQ-4242038
* Las experiencias eliminadas del entorno de autor nunca se eliminan del sitio de publicación tras la activación de la página. NPR-24869: revisión para CQ-4247832

### Plataforma {#platform-2}

* Parche jQuery 1.12.4 de clientlib para incluir una corrección de seguridad. NPR-24129: revisión para Granite-20058
* Se ha añadido la compatibilidad con STARTTLS en el servicio de correo de Day CQ. NPR-23941: revisión para CQ-4240397
* Elimine el valor predeterminado de MERGE_PRESERVE aclHandling. NPR-24593: revisión para Granite-21889
* LineChecker no puede externalizar vínculos cuando una solicitud contiene parámetros de consulta no válidos. NPR-24127: revisión para CQ-4241893

### Medios convencionales {#msm}

* Revisiones proactivas a ataques de scripts entre sitios (XSS). NPR-21893: revisión para CQ-4223385
* MSM LiveRelationship: RolloutConfig eficaz es incorrecto si BlueprintConfig está en la raíz. NPR-23999: revisión para CQ-4243000

### Sites {#sites-3}

* La creación de una experiencia en un área de Live Copy requiere que primero se rompa la herencia para poder configurarla. NPR-24995, revisión para CQ-4248209
* (IU táctil) Varios iconos de la barra de herramientas superior desaparecen al bloquear o desbloquear una página. NPR-23954: revisión para CQ-4243345
* Los campos no están correctamente alineados en el contexto. NPR-23958
* Acción de Publish en la creación de saltos de página bloqueados. NPR-23970: revisión para CQ-4243203
* Los informes OOTB en /etc/reports/ no funcionan correctamente y no muestran gráficos de datos históricos. NPR-20035: revisión para CQ-4220180
* La creación de inicios falla al iniciar el flujo de trabajo &quot;Solicitar inicio&quot; en un proyecto. NPR-24255: revisión para CQ-4245030
* Etiquetas y atributos HTML ignorados por los correos electrónicos tras la instalación de CFP10. NPR-24287: revisión para CQ-4240028
* TagPicker: sugerencia de etiquetas en el campo de etiqueta de esquema de metadatos de etiquetas consultas de nodos etiquetables, por lo tanto, tardan mucho tiempo en cargarse. NPR-24347: revisión para CQ-4244291
* La integración de Salesforce falla con las configuraciones de proxy. NPR-24418: revisión para CQ-4245300
* (WCM) PageManager deja la página protegida en excepción durante la creación de la revisión. NPR-24565: revisión para CQ-4246203
* El botón Emulador de dispositivos desaparece del modo de edición y previsualización después de aplicar CFP14. NPR-24566: revisión para CQ-4247060
* (IU clásica) Todas las etiquetas se muestran como vacías una vez creadas en el cuadro de diálogo. NPR-24688, revisión para CQ-4246407
* No se pudo crear una versión en el primer intento. NPR-24774: revisión para CQ-4232176
* Los informes OOTB en /etc/reports/ no funcionan correctamente y no muestran gráficos de datos históricos. NPR-24138: revisión para CQ-4220180

### Vulnerabilidad {#vulnerability-1}

* La integración de Salesforce es vulnerable a la falsificación de solicitudes del lado del servidor (SSRF). NPR-24289: revisión para CQ-4245277
* Vulnerabilidad de falsificación de solicitudes del lado del servidor (SSRF) en ReportingServicesProxyServlet. NPR-24657: revisión para CQ-4246880

### Granite {#granite-3}

* No se han completado las operaciones de lectura de metadatos. NPR-24240: revisión para Granite-19866
* Actualice Jetty a 9.4.11.v20180605 para corregir vulnerabilidades. NPR-25033: revisión para Granite-22120

### WCM: componentes base {#wcm-foundation-components-1}

* PageComparator está iniciando ClassCastException mientras se ordenan las páginas. NPR-24123: revisión para CQ-4244048
* La funcionalidad Mostrar/Ocultar del componente desplegable del formulario no funciona correctamente. NPR-24562: revisión para CQ-4222853

### Interfaz de usuario {#user-interface}

* Se observa un alto uso de la CPU debido a muchas solicitudes en la funcionalidad de búsqueda de administración. NPR-23588: revisión para Granite-21286
* (IU clásica) El componente muestra los valores predeterminados aunque el servicio del modelo de datos de formulario asociado se establezca en un campo vacío. NPR-21903: revisión para GRANITE-19744
* Varios campos lanzan NPE cuando no hay ningún FormData presente para la solicitud. NPR-24513: revisión para Granite-21055

## Forms {#forms-4}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [Versiones de AEM Forms](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-4}

#### Núcleo {#core}

* (OSGI) El OSGI de AEM Forms se vio afectado por la alerta de seguridad de enlace de datos de Jackson. NPR-24274: revisión para CQ-4230245

#### Rights Management {#rights-management}

* Apache POI falla tras la instalación de AEM 6.2 SP1-CFP14. NPR-25054, NPR-25052: revisión para CQ-4245898, CQ-4244778

#### Formularios HTML5 {#html-forms}

* Los datos no se rellenan con el prefijo de campos multilínea en la previsualización HTML. NPR-23357: revisión para CQ-4244212
* Cuando se obtiene una vista previa de una carta mediante una vista previa predeterminada, la asignación de fragmentos de diseño no se muestra, mientras que la misma aparece correctamente al hacer clic en Vista previa. NPR-22993: revisión para CQ-4237745
* Problema con la previsualización HTML de un campo de texto cuando se aplica un patrón de un número de la seguridad social a una plantilla. NPR-23205

#### Formularios adaptables {#adaptive-forms-3}

* Error “no se ha definido Guidelib” al agregar un formulario de AEM al componente Parsys.  NPR-24269: revisión para CQ-4244546

### Instalador JEE de Forms {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Los extremos de línea de ventana en archivos de script de Shell hacen que LCM no se ejecute en UNIX®.  NPR-22958

### Paquetes de contenido y paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-3}

Lista de paquetes OSGi incluidos en el SP1-CFP16 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP16 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Paquete de correcciones acumulativas 15 {#cumulative-fix-pack-5}

El paquete de correcciones acumulativas 6.2 SP1-CFP15 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de [AEM 6.2 SP1](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Correcciones de seguridad dinámicas en la tabla Foundation para mantener la coherencia del diseño.
* Se añadió la compatibilidad de typeHint para guardar valores como cadena.
* Proporciona seguridad mejorada para el servicio de cumplimentación previa de Forms
* Actualice al archivo adobe-reader-extensions-dsc.jar más reciente para ver las correcciones en la extensión de Reader.
* Se ha ajustado el gancho de validación para tener en cuenta los elementos `:invalid` para la entrada de número de ampliación.

### Recursos {#assets-4}

* Los datos EmbedXMP siempre se definen como &quot;activos&quot; para el proceso de generación de la Pirámide de TIFF. NPR-22776: revisión para CQ-4234498
* No se pueden establecer varios valores predeterminados en los campos de varios valores. NPR-22900: revisión para CQ-4239000
* (Dynamic Media) Al seleccionar la casilla de verificación Representaciones dinámicas, el archivo zip descargado genera la imagen original del TIFF con un archivo de cero bytes. NPR-22410: revisión para CQ-4198471
* (IU táctil) Ubicación de carga predeterminada para los recursos en la vista de columna. NPR-23475: revisión para CQ-4237057

### Integración {#integration-5}

* En el modo de destinatario, los autores pueden modificar un componente heredado del modelo sin cancelar la herencia. NPR-22751: revisión para CQ-4237907
* La variable de ruta no se codifica correctamente, lo que provoca ejecuciones de scripts en sitios múltiples (XSS) no persistentes. NPR-22851

### Medios convencionales {#msm-1}

* Durante el despliegue de un LiveCopy con varias configuraciones de despliegue, si se produce un ResourceNameConflict debajo de la raíz, el flujo de despliegue termina sin incluir todas las ramas. NPR-22842: revisión para CQ-4236188

### Plataforma {#platform-3}

* Implementar un límite de sondeo en una solicitud de aplicación inversa. NPR-23351: revisión para Granite-21135****
* El cambio del patrón de mensajes no se refleja en los registradores personalizados. NPR-23486: revisión para CQ-4241974

### Sites {#sites-4}

* No funciona la creación de un vínculo dentro de un texto de un editor de texto enriquecido en un documento con espacios u otros caracteres especiales. NPR-22289: revisión para CQ-4224321
* Al guardar el segmento con un valor enorme (10000000000), se establece el valor de ampliación en 0, lo que provoca un mensaje de error. NPR-22524: revisión para CQ-4237006
* No se puede hacer clic en Añadir elemento en el componente multicampo. NPR-22552: revisión para CQ-4237404
* La barra de desplazamiento horizontal no está visible cuando un segmento tiene un título largo. NPR-22615: revisión para CQ-4237001
* La carga de una audiencia vacía genera un código JavaScript incorrecto. NPR-22974: revisión para CQ-4238734
* Al programar una activación o desactivación, el título del flujo de trabajo es obligatorio, por lo que el título del flujo de trabajo personalizado no se traduce en la línea de tiempo. NPR-23121: revisión para CQ-4237552
* Solicitud de correcciones a problemas relacionados con segmentos de destinatario en sitios. NPR-23128
* (Firefox) La casilla de verificación de la persona seleccionada no es la correcta. NPR-23345
* Las etiquetas de los distintos modos se muestran junto con los iconos. NPR-23275
* Error “Valor del selector de recursión no válido” al migrar un componente de AEM 6.0 a AEM 6.2. NPR-23503: revisión para CQ-4241258

### Comunidades {#communities-1}

* Las notificaciones por correo y web no se activan debido a un error en los mensajes de los grupos. NPR-23447: revisión para CQ-4242880

### Traducción {#translation-1}

* Las copias de idioma de los recursos se crean cuando el recurso &quot;No traducir&quot; se establece en la configuración de traducción. NPR-22540: revisión para CQ-4237962

### Interfaz de usuario {#user-interface-1}

* El uso de Omnisearch con una consulta de guion devuelve un error de servidor. NPR-22999: revisión para Granite-19674
* DatePicker no admite establecer manualmente una sugerencia de tipo externo establecida por un campo oculto. Si se cambia la sugerencia de tipo, se producirá un error de conversión. NPR-23333: revisión para Granite-21194

### WCM: componentes base {#wcm-foundation-components-2}

* El componente CAPTCHA ya no se utiliza para mejorar la seguridad. Si utiliza el componente CAPTCHA, aparece el mensaje &quot;El componente Captcha está obsoleto y no debe utilizarse&quot; después de instalar la versión 6.2 SP2-CFP15 o posterior. El componente de AEM se puede personalizar para incluir reCAPTCHA para mejorar la seguridad NPR-22151: revisión para CQ-4220052
* La “tabla” de componente WCM Foundation es vulnerable a la ejecución almacenada de scripts en sitios múltiples. NPR-23206: revisión para CQ-4240760

### Vulnerabilidad {#vulnerability-2}

* Ejecuciones de scripts en sitios múltiples (XSS) en los vínculos del proyecto de la IU de administración. NPR-23272: revisión para CQ-4241795

## Forms {#forms-5}

### Paquete de complemento de Forms {#forms-add-on-package-5}

#### Administración de correspondencia {#correspondence-management}

* Cuando se obtiene una vista previa de una carta mediante una vista previa predeterminada, la asignación de fragmentos de diseño no se muestra, mientras que la misma aparece correctamente al hacer clic en el botón Vista previa. NPR-23335: revisión para CQ-4237745
* Los datos de la carta correspondientes a los enlaces definidos en XDP no se rellenan con la dirección URL de la carta directa. NPR-24145: revisión para CQ-4244290

#### Mobile Forms {#mobile-forms}

* (Administración de correspondencia) Desalineación de datos al cargar la carta con XML de destinatario. NPR-22993: revisión para CQ-4237663

#### Reader Extensions Service {#reader-extensions-service}

* No se puede aplicar la extensión de lector en Adobe PDF. NPR-23067

#### Administrador de Forms {#forms-manager}

* Los Forms incrustados en el sitio no se publican al volver a publicar la página del sitio. NPR-23014: revisión para CQ-4236566

#### Vulnerabilidad {#vulnerability-3}

* Revisiones proactivas para ejecución de scripts en sitios múltiples. NPR-20624: revisión para CQ-4206055
* Vulnerabilidad de la ejecución almacenada de scripts en sitios múltiples (XSS) en la pestaña Notas del Administrador de Forms. NPR-27157: revisión para CQ-4255556

#### Servicio de cifrado {#encryption-service}

* (OSGI) [JEE] Estado de firma incorrecto para el PDF con datos adjuntos mientras se verifica con &quot;Validar proceso de PDF&quot;. NPR-23269, NPR-23737

### Instalador JEE de Forms {#forms-jee-installer-5}

#### Núcleo {#core-1}

* Deben solucionarse los problemas notificados en el análisis del código estático de la extensión principal. NPR-13947

#### Servicio PDFG {#pdfg-service}

* El conversor de HTML a PDF no funciona. NPR-21545

### Paquetes de contenido y paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-4}

Los siguientes documentos de texto enumeran los paquetes OSGI y los paquetes de contenido incluidos en el CFP.

Lista de paquetes OSGi incluidos en el SP1-CFP15 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP15 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Paquete de correcciones acumulativas 14 {#cumulative-fix-pack-6}

El paquete de correcciones acumulativas 6.2 SP1-CFP14 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha mejorado la capacidad de edición de las propiedades de metadatos de los recursos.
* Se ha vuelto a configurar el trabajo Notificación de caducidad de contraseña para los recursos que ya están en caducados.
* Consola de IU táctil personalizada para ampliar configuraciones regionales adicionales.
* Se ha actualizado cq-msm-core para lograr una sincronización eficiente de Livecopyindex.
* Funcionalidad de replicación optimizada para varios lanzamientos.

### Recursos {#assets-5}

* Los usuarios no pueden descargar recursos con nombres de archivo largos y de renuncia de responsabilidad. NPR-22163: revisión para CQ-4235274
* Un carácter de comilla simple evita la actualización de metadatos en la vista masiva y la interfaz de usuario se interrumpe al abrir las propiedades de un recurso mediante las acciones rápidas de la barra de herramientas. NPR-22317, NPR-22353: revisión para CQ-4236990, CQ-4236469
* El trabajo de notificación de caducidad del recurso no desactiva los recursos caducados. NPR-22346: revisión para CQ-4237188
* La descarga de recursos falla al usar Digital Rights Management en Assets en Safari. NPR-22378: revisión para CQ-4236460
* La representación web para imágenes pequeñas tiene un tamaño de píxel impreciso. NPR-22435: revisión para CQ-4236742

### Sites {#sites-5}

* (IU táctil) La etiqueta desplazada aparece en ubicaciones antiguas y nuevas en las propiedades de la página. NPR-21921, revisión para CQ-4238598
* (IU táctil) El editor de texto enriquecido elimina todos los atributos que no sean el ID de la etiqueta &lt;a>. NPR-22045: revisión para CQ-4234133
* Al pegar contenido directamente en el Editor de texto enriquecido mediante CTRL+V se omiten los saltos de línea. NPR-22117: revisión para CUI-5881
* (IU táctil) No se pueden mostrar más de 40 etiquetas en un área de nombres. NPR-22290: revisión para CQ-99114
* Problemas con la fuente RSS, puerto -1 a AEM 6.2 NPR-22158: revisión para CQ-4233339
* (IE) Al crear cualquier carácter en el campo Texto enriquecido por primera vez, se agrega un espacio final al carácter. NPR-22443: revisión para CQ-4235343
* Al intentar hacer coincidir el nombre del paquete, el objeto Java™ Use congela SightlyJavaCompilerService debido a un carácter de espacio final en la declaración del paquete. NPR-22557: revisión para Granite-20836
* La consola de IU táctil no recoge nuevos idiomas para el etiquetado. NPR-22250: revisión para CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Tanto la fecha de publicación como la fecha de portada son campos obligatorios para las publicaciones antes de que se carguen en DPS. NPR-22484

### Comercio {#commerce}

* Varias ejecuciones de scripts en sitios múltiples (XSS) en el comercio Crear asistente de catálogos. NPR-22344: revisión para CQ-4237017

### Medios convencionales {#msm-2}

* La sincronización de LiveCopyIndex provoca congestión de subprocesos durante las actualizaciones de índice largas. NPR-22214: revisión para CQ-90667
* La propiedad `cq:cugEnabled` se desactiva cuando se edita otro campo de una Live Copy, por lo que la página queda desprotegida. NPR-22246: revisión para CQ-4236050
* La acción Despliegue de página no puede actualizar los elementos secundarios cuando se suspende una página. NPR-22483: revisión para CQ-4236956
* El despliegue de una estructura que se ha movido en una pista principal genera un error `cq:moveTarget`. NPR-22373: revisión para CQ-4232536

### Integración {#integration-6}

* Al intentar ordenar ofertas en la biblioteca del selector de ofertas, se produce un comportamiento errático. NPR-22208: revisión para CQ-4235439
* TargetContentImpl hace que AEM sea lento durante consultas de larga ejecución. NPR-22361: revisión para CQ-4236907
* El motor de Target (mbox.js, at.js) no utiliza direcciones URL estropeadas y utiliza direcciones URL que contienen dos puntos que pueden dar error en determinadas implementaciones. NPR-22366: revisión para CQ-4237854
* La personalización de la página requiere la publicación en el nodo de la marca. NPR-22370: revisión para CQ-4236895

### Foundation {#foundation}

* Los modelos de Apache Sling Scripting Sightly utilizan el Paquete de proveedores **org.apache.sling.scripting.sightly.models.provider/1.0.18**. NPR-22614: revisión para Sling-5944, Sling-6866

### Proyectos {#projects}

* Workflow Starter no puede aceptar el valor TypeHint de String. NPR-22436: revisión para CQ-4237855

### Traducción {#translation-2}

* Investigación de los problemas con la funcionalidad Vista previa. NPR-22201: revisión para CQ-4223753

### Interfaz de usuario {#user-interface-2}

* (IU clásica) El componente muestra los valores predeterminados aunque el servicio del modelo de datos de formulario asociado se establezca en un campo vacío. NPR-21903: revisión para GRANITE-19744

### WCM: componentes base {#wcm-foundation-components-3}

* Error al publicar una página de Live Copy que apunta a una página de importador en Adobe Campaign. NPR-22470: revisión para CQ-4237164
* Errores de JavaScript al abrir el Editor de fragmentos de experiencia. NPR-22598: revisión para CQ-4238415

### Flujo de trabajo {#workflow}

* El Servicio de notificación por correo electrónico del flujo de trabajo de CQ diario desencadena un mensaje de correo electrónico por nodo Mongo para las notificaciones WorkflowCompleted y WorkflowAborted. NPR-22486: revisión para CQ-4238172

## Forms {#forms-6}

### Paquete de complemento de Forms {#forms-add-on-package-6}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

#### Formularios adaptables {#adaptive-forms-4}

* Incoherencia en el valor del marcador de posición desplegable en el formulario adaptable en IE11 y Chrome. NPR-22405: revisión para CQ-4227096

### Instalador JEE de Forms {#forms-jee-installer-6}

#### Instalación de LCM {#install-lcm}

* Actualice Jsafe Jars a Cryptoj 6.1.3.1 en el instalador y LCM. NPR-22744

### Paquetes de funciones incluidos {#feature-packs-included}

#### Administración de procesos {#process-management}

* (HTML Workspace) Cuando un usuario reclama una tarea, el recuento de la cola se actualiza solo para ese usuario en particular. Es decir, a menos que se actualice la página. NPR-19778: revisión para CQ-4233665

### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}

Lista de paquetes OSGi incluidos en el SP1-CFP14 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP14 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
El paquete de correcciones acumulativas 6.2 SP1-CFP13 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha habilitado la configuración del campo Parámetro estático dentro de la Configuración del componente de destino al usar AT.js como biblioteca de cliente.
* Correcciones en la funcionalidad de mostrar u ocultar del componente desplegable.
* Correcciones para usar audiencias de sincronización de destinatarios.
* Se ha aumentado la versatilidad de la administración de correspondencia para admitir caracteres especiales.

### Recursos {#assets-6}

* La depuración de versiones no puede eliminar versiones antiguas de los recursos. NPR-21682: revisión para CQ-4212996
* La reordenación de carpetas en una carpeta reordenable no persiste. NPR-21964: revisión para CQ-4231761

### Sites {#sites-6}

* (IU táctil)(IU clásica) Varias ejecuciones de scripts en sitios múltiples (XSS) vulnerables en componentes principales y HTL. NPR-21532: revisión para CQ-4232305 y CQ-4232511
* La creación o el formato de contenido (por ejemplo, asignar o quitar nuevos estilos de lista) en un texto seleccionado no funcionan bien en Internet Explorer 11. NPR-21533: revisión para CQ-4230689
* (Safari) Los usuarios no pueden ver todos los recursos en el panel Buscador de recursos. NPR-21981: revisión para CQ-4213720
* Deformación de tiempo devuelve el error &quot;RecursionTooDeepException&quot; con una página con errores y no se crea ninguna nueva versión aunque se cambie la fecha. NPR-21707: revisión para CQ-4199536
* AEM Al cargar una página en el editor, WorkflowStatusProvider (pageinfo.json) se carga tres veces, lo que provoca que la instancia de la página funcione con lentitud. NPR-21778: revisión para CQ-59232

### Integración {#integration-7}

* La creación de audiencias de Tipo y Navegador móvil en el modo de creación de Destinatario no funciona en AEM. NPR-21676, NPR-21681: revisión para CQ-4232100
* Con una latencia alta durante la actualización de un componente de destino, es posible agregar otra oferta antes de que el componente se actualice por completo. NPR-21744: revisión para CQ-4233158/CQ-4234293
* Los usuarios no pueden ver los valores de Parámetro estático de prueba en la llamada de mbox, lo que se puede ver al realizar pruebas con AT.js como biblioteca de cliente en la configuración de la nube. NPR-21930: revisión para CQ-4234520

### Plataforma {#platform-4}

* Problemas de rendimiento con la sincronización de usuarios cuando el número de usuarios o grupos es grande. NPR-20431: revisión para CQ-4223282
* Los usuarios no pueden sincronizar con la sincronización de usuarios mediante Sling Distribution. NPR-21911: revisión para Granite-20404
* Impedir que las palabras dejen de resaltarse en extractos de búsqueda (en una página de Geometrixx). NPR-21835: revisión para Granite-21067
Nota: Esta corrección requiere el Oak CFP 1.4.20 o superior.

### Traducción {#translation-3}

* Falta la propiedad jcr para el Iniciador de ID de usuario al crear un proyecto de traducción. NPR-21715: revisión para CQ-4230713

### WCM: componentes base {#wcm-foundation-components-4}

* La funcionalidad Mostrar/Ocultar del componente desplegable del formulario no funciona correctamente. NPR-22164: revisión para CQ-4235288

## Forms {#forms-7}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms {#forms-add-on-package-7}

#### Formularios adaptables {#adaptive-forms-5}

* Inyección de entidad externa XML (XXE) en los formularios adaptables. NPR-21982: revisión para CQ-109878
* (iOS11) Al hacer clic en el componente de archivo adjunto, el archivo adjunto abre la cámara en lugar del explorador de archivos del dispositivo. NPR-21926: revisión para CQ-4214348
* Falta el título en la IU para la creación del tema, lo que provoca una excepción y un error en la representación del cuadro de diálogo. Revisión para CQ-4236143

#### Administración de correspondencia {#correspondence-management-1}

* Problemas de procesamiento con datos xml que contienen caracteres especiales. NPR-21712: revisión para CQ-4229137

### Instalador JEE de Forms {#forms-jee-installer-7}

#### Servicio del ensamblador {#assembler-service}

* El archivo PDF generado mediante `6.2.0-ASM-1017-003` está roto. NPR-21427: revisión para CQ-4228046

#### Servicio PDFG {#pdfg-service-1}

* Error de OCR debido a un tamaño de página (PDF) inesperado de archivos PNG, JPEG y TIFF. NPR-19489: revisión para CQ-4209079

## Los paquetes OSGI y los paquetes de contenido están incluidos en la versión CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

Lista de paquetes OSGi incluidos en el SP1-CFP13 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP13 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp13_contentpackage-list.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP12.1 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha mejorado la administración de metadatos para los campos multivalor.
* Compatibilidad con códigos de país de varios caracteres (más de dos) en los flujos de trabajo de traducción.
* Se ha mejorado la representación de páginas con varios componentes anidados.
* Se ha mejorado la sincronización de las fechas de publicación de los recursos entre AEM y Adobe Digital Publishing Suite.

### Recursos {#assets-7}

* AEM Demasiados caracteres en OmniSearch pueden provocar que el servidor de la se bloquee. NPR-21083: revisión para CQ-4223602
* Los valores especificados en la segunda opción de un campo multivalor en el esquema de metadatos no se anexan a los valores especificados anteriormente en CRX-de. NPR-21220: revisión para CQ-4224526
* La descarga de recursos falla al usar Digital Rights Management en Assets en Safari. NPR-21387: revisión para CQ-4230287

### Sites {#sites-7}

* (DAM) (IU clásica) Varias ejecuciones de scripts en sitios múltiples (XSS) en algunos archivos SWF en el inicio rápido de AEM CQ Author/Publish. NPR-21073, NPR-21074: revisión para NPR-20612
* El selector de etiquetas no traduce las etiquetas que están disponibles en varios idiomas. NPR-21221: revisión para CQ-78855
* Los problemas de representación con la consola de artículos de AEM, como el uso de varios componentes anidados, hacen que sea lenta. NPR-21271: revisión para CQ-4224158

### Integración {#integration-8}

* Al agregar un marco de trabajo de Target, el modo de Orientación no está disponible en la lista Seleccionar modo del editor. NPR-21047

### Mobile On-Demand {#mobile-on-demand-1}

* (Digital Publishing Suite) Las fechas de publicación de las publicaciones de AEM no coinciden con las fechas que aparecen en Folio Producer. NPR-21145

### Medios convencionales {#msm-3}

* El proceso de restablecimiento de Live Copy se detiene después de eliminar la primera página local en la LC. NPR-21276: revisión para CQ-4229743

### Plataforma {#platform-5}

* AEM La biblioteca de etiquetas personalizada que hace referencia a las etiquetas implementadas como un script no se encuentra después de actualizar a la versión 6.3 de. NPR-20149: revisión para Granite-18433

### Traducción {#translation-4}

* Los flujos de trabajo de traducción fallan con códigos lang_country superiores a dos caracteres. NPR-21088: revisión para CQ-4197439
* No vuelva a enviar una página de recursos a un proyecto de traducción hasta que se complete el proyecto. NPR-21219: revisión para CQ-4209908

### Interfaz de usuario {#user-interface-3}

* El componente Seleccionar no elimina la propiedad de destinatario durante el envío del formulario. NPR-21163: revisión para GRANITE-14125
* El doble de expansión HTTP.encodePathOfURI codifica el signo más &quot;+&quot;. NPR-21417: revisión para GRANITE-16340

### Vulnerabilidad {#vulnerability-4}

* Ejecuciones de scripts en sitios múltiples (XSS) en el editor de metadatos DAM. NPR-21434: revisión para CQ-83472
* Varios archivos de SWF son vulnerables a ejecuciones de scripts en sitios múltiples (XSS). NPR-20612: revisión para CQ-4213297

## Forms {#forms-8}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms {#forms-add-on-package-8}

#### Administración de correspondencia {#correspondence-management-2}

* (IE11) El procesamiento inicial del contenido HTML se produce solamente en el lado izquierdo, mientras que en el lado derecho se carga intermitentemente después de cargar la IU completa. NPR-21554
* AEM El botón de envío de previsualización de carta se desactiva después de instalar el SP1-CFP9 de la versión 6.2. NPR-21547
* Al seleccionar el tipo de vinculación de recursos, la ventana Selector de recursos no se abre en el asistente Editar enlace de datos de carta. NPR-21164: revisión para CQ-4194567
* Para editar un módulo de texto en línea o editable, toque el icono Editar correspondiente o haga doble clic en el módulo de texto correspondiente en la previsualización de carta. NPR-21402

#### Formularios adaptables {#adaptive-forms-6}

* El componente de botón de envío de AEM Forms muestra type=&quot;button&quot; en lugar de type=&quot;submit&quot;. NPR-21007
* Los datos se mantienen al agregar o eliminar nuevos paneles para los paneles repetitivos. NPR-21408

### Instalador JEE de Forms {#forms-jee-installer-8}

#### Núcleo {#core-2}

* La actualización a la última Actualización 131 de Java™ 8 genera una excepción: &quot;El proveedor JsafeJCE está deshabilitado, se ha producido un error en la comprobación de integridad de FIPS 140 necesaria&quot;. NPR-21355

**Nota:** Este NPR requiere más ajustes. Consulte la [Última actualización de Java™ 8](#latest-java-update-throws-an-exception-npr).

* Jsafe Jars se ha actualizado a CryptoJ 6.1.3.1 en Principal, Cifrado, Firma y Seguridad de los documentos. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Instalación de LCM {#install-lcm-1}

* Actualice Jsafe Jars a Cryptoj 6.1.3.1 en el programa de instalación y LCM. NPR-21362

#### Servicio PDFG {#pdfg-service-2}

* Actualice Jsafe Jars a Cryptoj 6.1.3.1 en PDFG. NPR-21359

#### Administración de procesos {#process-management-1}

* (Espacio de trabajo HTML) Habilitar el cambio de tamaño de la columna para que la categoría de nombre no aparezca truncada. NPR-19770: revisión para CQ-4233668

#### Reader Extensions Service {#reader-extensions-service-1}

* Jsafe Jars se ha actualizado a CryptoJ 6.1.3.1 en RE. NPR-21357

## Los paquetes OSGI y los paquetes de contenido están incluidos en la versión CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

Lista de paquetes OSGi incluidos en el SP1-CFP12.1 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP12.1 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp12_contentpackage-list.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP11 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha actualizado cq-msm-core para lograr una sincronización eficiente de Livecopyindex.
* Eficacia de edición mejorada para fragmentos de contenido.
* Proporciona una opción de validación en el Administrador de paquetes para detectar permisos ACL.
* Se ha introducido la capacidad de Campaign para incluir el ID de correo electrónico para la correspondencia de los clientes.
* Se han mejorado las capacidades de codificación de vídeo para archivos de Dynamic Media.
* Correcciones en el componente Sightly y LiveCopies.

### Recursos {#assets-8}

* La codificación de vídeo de Dynamic Media falla en los archivos que incluyen espacios en sus nombres. NPR-20818: revisión para CQ-102469
* Varias ejecuciones de scripts en sitios múltiples (XSS) en algunos archivos SWF en el inicio rápido de AEM CQ Author/Publish. NPR-21071, NPR-21072
* Los usuarios no pueden descargar recursos con nombres de archivo largos y de renuncia de responsabilidad. NPR-20255: revisión para CQ-4222139

### Sites {#sites-8}

* Integración de AEM y Campaign: los vínculos especiales se reescriben en Adobe Campaign para evitar que los clientes envíen mailto: hipervínculos en sus correos electrónicos. NPR-20787: revisión para CQ-4225760
* (IU táctil) Problemas de uso y de rendimiento de AEM cuando el idioma se establece en francés. NPR-20854: revisión para CQ-4227628
* La vinculación de un archivo de recurso codificado mediante un complemento de vínculo en RTE devuelve un vínculo vacío. NPR-20626, NPR-21059: revisión para CQ-4223011
* El editor de metadatos de Fragmento de contenido evita que los autores de contenido guarden cambios en los Fragmentos de contenido. NPR-20641: revisión para CQ-4224755
* El Alias de propiedad de página lleva a Solicitar publicación o Solicitar cancelación de la publicación. NPR-20731: revisión para CQ-4226227
* Problemas del componente de texto con la codificación del vínculo en el elemento RTE. NPR-20755: revisión para CQ-4224321

### Plataforma {#platform-6}

* ResourceResolverImpl.map() no invoca ResourceDecorator. NPR-20788: revisión para GRANITE-19718
* `org.apache.sling.i18n.DefaultLocaleResolver` no puede procesar solicitudes a través de org.apache.sling.engine.SlingRequestProcessor. NPR-20706: revisión para CQ-94880
* Solicite agregar una opción de validación en el Administrador de paquetes para detectar si se han cambiado los permisos o privilegios de ACL en un paquete en particular. Revisión para CQ-4229196

### Flujo de trabajo {#workflow-1}

* Problemas de estabilidad con la implementación del servidor de producción de AEM. NPR-20979: revisión para Granite-19104

### Proyectos {#projects-1}

* (IU táctil) No se pueden agregar miembros del equipo a un proyecto. NPR-20990: revisión para CQ-4205375

### WCM: componentes base {#wcm-foundation-components-5}

* El componente de imagen de Sightly &quot;vínculo a&quot; genera un error 403 debido a la falta de la extensión .html. NPR-20823: revisión para CQ-4195909
* En un sitio del modelo que utiliza LiveCopy, al intentar eliminar un componente de formulario, se genera una excepción NullPointerException y se vuelve a agregar el componente de formulario en lugar de eliminarlo. NPR-20855: revisión para CQ-4204628
* La sincronización de LiveCopyIndex provoca congestión de subprocesos durante las actualizaciones de índice largas. NPR-20634: revisión para CQ-90667

### Seguridad {#security}

* Actualización proactiva de la biblioteca XSS. NPR-21174
* Actualice a Apache Commons Email 1.5, que presenta una API simplificada para enviar correo electrónico. NPR-20509: revisión para Granite-18240
* Parche de seguridad aplicado a la API de protección Apache Sling XSS para eliminar la posibilidad de omitir XSS. NPR-21290: revisión para GRANITE-19924
* Omisión XSS en la función XSSAPI#getValidHref. NPR-21174: revisión para Granite-19924

### Aplicaciones móviles {#mobile-apps}

* Se han corregido problemas con las solicitudes de cabezal de curl para los recursos de OOTB en AEM. NPR-20511: revisión para CQ-4221520 y CQ-103024

## Forms {#forms-9}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

Los aspectos destacados de AEM Forms son:

* Autenticación de certificados para los usuarios de Workbench habilitada.
* Correcciones de uso para la administración de correspondencia, HTML5 Forms y espacio de trabajo de AEM Forms.

### Paquete de complemento de Forms {#forms-add-on-package-9}

#### Formularios HTML5 {#html-forms-1}

* Problemas de uso con el componente de anotaciones en dispositivos iOS 10 y 11. NPR-21092

#### Administración de correspondencia {#correspondence-management-3}

* (IU de correspondencia) Deshabilite el botón de envío después de un clic. NPR-21078

### Instalador JEE de Forms {#forms-jee-installer-9}

#### Servicio del ensamblador {#assembler-service-1}

* docConvertor falla al producir PDF/A con el error &quot;El prefijo &quot;stEvt&quot; para el elemento `stEvt:action` no está enlazado&quot;. NPR-21032: revisión para CQ-4222540
* Se produce una excepción con el nombre `java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE` al invocar el servicio OMPFSubmission/PDFA/PDFtoPDFA. Esta excepción evita que el proceso de verificación de firma de corta duración se complete hasta que se reinicie el servidor. NPR-20792

#### Workbench {#workbench}

* Autenticación de certificados para los usuarios de Workbench habilitada. NPR-17548: revisión para CQ-4214486

#### Administración de procesos {#process-management-2}

* El proceso de preparación de datos se invoca varias veces cuando se procesa un formulario móvil con parámetros de fuente de datos. NPR-19801: revisión para CQ-4230427: CQ-4230400

## Los paquetes OSGI y los paquetes de contenido están incluidos en la versión CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

Lista de paquetes OSGi incluidos en el SP1-CFP11 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP11 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp11_contentpackage-list.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP10 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha añadido una nueva función de utilidad en onDialogLoaded para hacer pruebas.
* Pruebas y configuraciones de unidades de front-end añadidas en ClientLibraryProxyServlet.
* Correcciones de rendimiento en el componente de editor de varias imágenes locales.
* Actualizaciones de configuración en Apache Sling JCR ResourceBundleProvider.

### Recursos {#assets-9}

* La previsualización de recursos no funciona si los flujos de trabajo de actualización de recursos están desactivados. NPR-20543: revisión para CQ-4204986
* Problemas de procesamiento con clase agregada en Granite: propiedad de clase (cq-damadmin-admin-assets-upload). NPR-20514: revisión para CQ-4219238
* Los recursos de miniaturas con caracteres especiales en el título muestran el objeto Java™ en el atributo alternativo de NPR-20347: revisión para CQ-4223620
* Reemplazar el código de comparación de versiones con el código propiedad de Adobe debido a problemas de licencias. NPR-20273: revisión para CQ-4223758
* Problemas de procesamiento al cargar archivos CMYK PSB con varias capas alfa. NPR-20251: revisión para CQ-4220869
* Los diccionarios de internacionalización funcionan si se reinicia el servidor en org.apache.sling.i18n 2.5.6. NPR-20525: revisión para Granite - 19490
* AEM No se generan volcados de procesos según el período de planificador con la configuración predeterminada del Recopilador de volcado de procesos (inicio predeterminado de la). NPR-20288: revisión para GRANITE-19488/GRANITE-12741 CQ-90647.

### Sites {#sites-9}

* Si el filtro de fecha modificado se cambia después de abrir la búsqueda guardada, no hay ningún efecto en los resultados. Y, los resultados mostrados son los mismos que el valor guardado anterior del filtro de fecha modificado. NPR-19739: revisión para CQ-4219425
* No se pudieron cargar las páginas con componentes anidados. NPR-20312
* El flujo de trabajo de solicitud de eliminación se activa al eliminar los paquetes de flujo de trabajo. NPR-20266: revisión para CQ-4221686
* (IU táctil) Problema con Copiar o Pegar con el portapapeles del sistema operativo y el portapapeles interno de AEM. NPR-20228: revisión para CQ-4220383
* AEM instancia se ralentiza con la vista de listas cuando se cargan varios recursos (más de 100). NPR-20034: revisión para CQ-4222695
* (IU táctil) La eliminación de lanzamientos mediante la consola de IU clásica hace que todas las páginas sean no editables. NPR-20520: revisión para CQ-4225074
* El menú desplegable de Target no funciona con varios componentes RTE en un cuadro de diálogo. NPR-20345: revisión para CQ-4220981

### Plataforma {#platform-7}

* Cuando se accede mediante una sesión anónima, ClientLibraryProxyServlet no realiza solicitudes proxy a bibliotecas de cliente en la instancia publicada y genera un error HTTP 404 no encontrado. NPR-20195: revisión para Granite-14409

### Integración {#integration-10}

* Si se selecciona el motor de destino como Adobe Target, se evita que el componente se cargue y se genera un error en el registro del servidor. NPR-20058: revisión para CQ-88071, CQ-109698, CQ-4201600

### Comercio {#commerce-1}

* No aparece ningún mensaje emergente de confirmación o redirección al crear productos desde la misma página. NPR-20257: revisión para CQ-4223414

### Interfaz de usuario {#user-interface-4}

* Cuando el Selector de fecha es un campo en un campo múltiple, los valores guardados en los campos de fecha no persisten al editar el componente. NPR-20077: revisión para GRANITE-19147
* Las consultas anteriores no se anulan en caso de que se activen consultas consecutivas que produzcan resultados incorrectos. NPR-20397: revisión para GRANITE-19306

### WCM: componentes base {#wcm-foundation-components-6}

* La propiedad ImageMap sigue existiendo incluso después de eliminar las imágenes del componente de editor de varias imágenes locales. NPR-20142: revisión para CQ-4222982

## Forms {#forms-10}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms {#forms-add-on-package-10}

#### Formularios adaptables {#adaptive-forms-7}

* El script valueCommit se ejecuta dos veces para DropDownList cuando se cambia a través de la interfaz de usuario. NPR-19989: revisión para CQ-110212

### Instalador JEE de Forms {#forms-jee-installer-10}

**Administración de procesos**

* El paquete CFP contiene AEM Forms HTML Workspace versión 2.2.26. NPR-20099
* El formulario precumplimentado no funciona cuando el formulario móvil está configurado para la vista como PDF. NPR-20566

**Rights Management**

* El cuadro de diálogo de selección de certificados de autenticación mutua o CAC debe mostrar los certificados con uso mejorado de claves (EKU) como inicio de sesión con autenticación de cliente o tarjeta inteligente. NPR-20708
* Forms JEE admite autenticación mutua PKCS#11. NPR-15001

## Los paquetes OSGI y los paquetes de contenido están incluidos en la versión CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

Lista de paquetes OSGi incluidos en el SP1-CFP10 del CFP de AEM 6.2

[Obtener archivo](assets/do-not-localize/bundle-list-cfp10.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP10 del CFP de AEM 6.2

[Obtener archivo](assets/do-not-localize/contentpackage-list-cfp10.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP9 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Configuración de la IU clásica de Analytics adaptada para entradas secretas.
* Correcciones para la caché de persistencia independiente para Context Hub.
* Cálculo preciso de las dimensiones de recursos.
* Se ha optimizado el rendimiento de AEM al publicar recursos en Brand Portal.
* Correcciones en el valor `Resourcetype` en el nodo de lienzo.
* Se ha habilitado la funcionalidad de búsqueda mediante caracteres especiales y distinguiendo entre mayúsculas y minúsculas del contenido de fragmento del documento.
* Formularios adaptables mejorados para adjuntar archivos PDF como archivos adjuntos en Safari.
Esta experiencia proporciona una nueva Dynamic Media que se conecta a la nueva infraestructura de publicación de Dynamic Media para una replicación más rápida y escalable.

### Recursos {#assets-10}

* AEM Assets no puede extraer referencias de subrecursos para recursos de InDesign que incluyen vínculos de duplicado al recurso. NPR-19006: revisión para CQ-4204186
* La opción Ordenar no funciona para los recursos de la colección en Comercio. NPR-19508: revisión para CQ-4213622
* Cuando un recurso con el mismo nombre que un recurso ya existente se mueve a la misma ubicación, el valor de `cq:lastReplicationAction` de los recursos se intercambia entre ellos, lo que causa la creación de metadatos incorrectos. NPR-19531
* Se muestra un mensaje de error al publicar un gran número de recursos, a pesar de que todos los recursos se han publicado correctamente. NPR-19629: revisión para CQ-4219611
* Las representaciones estáticas se muestran con dimensiones fijas y no reflejan el tamaño de la representación real. NPR-20004
* La instancia de AEM se vuelve lenta cuando se publican varios recursos (más de 4) en Brand Portal. NPR-20009

### Sites {#sites-10}

* AEM Muestra un comportamiento inesperado cuando un usuario intenta publicar `/unpublish/create` versión de una página bloqueada por otro usuario. NPR-19249; revisión para CQ-4215298 y CQ-4203856
* Al promocionar el lanzamiento anidado manualmente, la página secundaria se elimina. NPR-19704
* Problemas de persistencia cuando ContextHub almacena la sobrescritura de la capa de persistencia predeterminada durante la inicialización. NPR-19979: revisión para CQ-4218399
* Los fragmentos de contenido se superponen con otros botones. NPR-19980: revisión para CQ-4221519
* La página del sitio no se muestra cuando se ve usando un alias en SiteAdmin. NPR-20053: revisión para CQ-4221478
* Error al publicar una página de Live Copy que apunta a una página de importador en Adobe Campaign. NPR-20066: revisión para CQ-4220846

### Plataforma {#platform-8}

* Se ha actualizado Apache POI a la versión 3.16 para admitir la inclusión de imágenes de fondo de diapositivas PPT en las representaciones. NPR-18286
* Se han producido problemas de procesamiento con Internet Explorer 11 y Edge al cargar varios recursos en la misma carpeta. NPR-20062

### Integración {#integration-11}

* El archivo at.js personalizado no se publica cuando se accede con un usuario anónimo. NPR-19542: revisión para CQ-4219592
* Migración de las credenciales existentes de Analytics a la autenticación WSSE. NPR-19962

### Brand Portal {#brand-portal}

* AEM Habilitar las etiquetas de publicación desde la consola de administración de etiquetas/etiquetado a Brand Portal desde la de publicación. NPR-20271

## Forms {#forms-11}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms {#forms-add-on-package-11}

#### Administración de correspondencia {#correspondence-management-4}

* Funcionalidad habilitada para buscar texto actual en fragmentos del documento cuando se obtiene una vista previa de una carta. NPR-19712

#### Formularios adaptables {#adaptive-forms-8}

* Formularios adaptables mejorados para adjuntar archivos PDF como archivos adjuntos en Safari. Para admitir la misma capacidad en los formularios existentes, cambie la configuración en el widget de datos adjuntos y en &quot;Tipos de archivos compatibles&quot; y actualice el valor application/pdf en lugar de .pdf. NPR-19623

#### Administrador de Forms {#forms-manager-1}

* Si validationState es indefinido en un campo de formulario adaptable y se produce el evento elementFocusChanged, se devuelve un evento de error (errorState) al servidor de Adobe Analytics. NPR-19513

### Instalador JEE de Forms {#forms-jee-installer-11}

#### Núcleo {#core-3}

* El Administrador de conexiones no está disponible durante el apagado. JBoss® corta la dependencia de JDBC antes de que se cancele el despliegue del EAR del autor causando problemas de corrupción. NPR-19703

## Paquetes de funciones incluidos {#feature-packs-included-1}

* Corrección de miniaturas y mejoras de transparencia en Dynamic Media. NPR-15207

## Los paquetes OSGI y los paquetes de contenido están incluidos en la versión CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

Lista de paquetes de contenido incluidos en el SP1-CFP9 de AEM 6.2

[Obtener archivo](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Lista de paquetes OSGi incluidos en el SP1-CFP9 de AEM 6.2

[Obtener archivo](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP8 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Introducción de etiquetas a plantillas de usuario personalizadas en el servicio de plantillas de correo electrónico de Adobe.
* Mejoras en los botones de la IU táctil de la aplicación de escritorio.
* Se ha deshabilitado el botón de envío al hacer clic para evitar que se envíen varios formularios en una página de traducción.
* Se han configurado varios componentes RTE en un cuadro de diálogo.
* Se han reforzado ReferenceUpdates en Live Copy.
* Se ha habilitado la funcionalidad de búsqueda con distinción entre mayúsculas y minúsculas para el contenido de fragmento de documento.
* Se ha añadido una lista de las bibliotecas Linux® a la documentación de instalación de AEM Forms.

### Recursos {#assets-11}

* Problemas con la aplicación del filtro Omnisearch en colecciones inteligentes en el explorador Safari. NPR-19511
* Los metadatos de palabra clave de PDF no se extraen correctamente y se modifican incorrectamente cuando hay varias palabras clave asociadas a un recurso de PDF. Para resolver el problema, se ha eliminado la propiedad de metadatos del campo Asunto para los recursos de PDF. Sin embargo, puede editar el esquema de metadatos para agregar un campo de texto de varios valores para el campo Asunto. NPR-19126
* El servicio de notificación del flujo de trabajo no codifica los vínculos del correo electrónico, lo que impide que se carguen después de que los usuarios hagan clic en ellos. NPR-19490: revisión para CQ-4218055
* No se puede cargar una lista completa de páginas/recursos en la vista de columna mediante Chrome. NPR-19458: revisión para CQ-4214248
* AEM El icono Tiempo de inactividad incorrecto se muestra en la bandeja de entrada de la al activar el flujo de trabajo &quot;Solicitud de activación&quot;. NPR-19365: CQ-4216174
* Problemas con el orden en la vista de listas. NPR-19217: CQ-95602
* Al cambiar el título o la imagen en miniatura en la configuración de la carpeta de recursos, se anulan el grupo y los permisos originales de la carpeta. NPR-19283: revisión para CQ-4216080
* Las estaciones de trabajo de `Windows 10` cambian automáticamente al Modo táctil y desactivan el funcionamiento de algunos de los botones. NPR-19183

### Sites {#sites-11}

* Problemas con la presencia de varios componentes RTE en un cuadro de diálogo. NPR-19311: NPR-19587
* AEM La Depuración automática de versiones en vanilla 6.2 solo funciona después de que se inicialice VersionManagerImpl. NPR-19315: revisión para CQ-4217175
* La instancia de flujo de trabajo se queda atascada en el paso del flujo de trabajo &quot;Salesforce.com Export&quot;. NPR-19222: revisión para CQ-4212976
* Las páginas de copia de idioma creadas a partir de Live Copies no son editables. NPR-18967
* ReferencesUpdateAction no puede actualizar los vínculos en un LiveCopy anidado con cambio de jerarquía. NPR-18715: revisión para CQ-4214105

### Plataforma {#platform-9}

* El servicio de plantilla de correo electrónico Adobe agrega etiquetas a las plantillas de usuario personalizadas. NPR-19190: revisión para CQ-4217113

### Proyectos {#projects-2}

* Los editores de proyectos no pueden copiar/pegar recursos en la carpeta de recursos del proyecto. NPR-19619
* No se puede generar la previsualización para proyectos de traducción después de instalar 6.2 SP1-CFP1. NPR-16481: CQ-4204655

### Integración {#integration-12}

* Obtenga acceso a las propiedades de los artículos que se establecen incorrectamente en la solución de publicación digital de Adobe en la IU clásica. NPR-19366
* AEM Representación lenta de las miniaturas debido a artículos de tamaño completo en la consola de artículos de. NPR-19086: CQ-4217148
* Comportamiento incorrecto del plegado automático al personalizar las ofertas a través de Campaign si los usuarios tienen acceso a varias áreas. NPR-19290: revisión para CQ-4218029
* El cuadro de diálogo de destino no se muestra en el modo de destino cuando se edita un módulo de destino y se guarda más de una vez. NPR-19144: revisión para CQ-4216708

### Flujo de trabajo {#workflow-2}

* Los usuarios no pueden filtrar las notificaciones en la bandeja de entrada por usuario/grupo en la IU de Inbox Classic. NPR-19122: revisión para CQ-4215374
* El Mapa de imagen no conserva las coordenadas seleccionadas en el componente de imagen HTL. NPR-18911: CQ-4211584

## Forms {#forms-12}

* Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [Versiones de AEM Forms](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-12}

* Cuando el contenido se copia desde Microsoft® Word o un explorador web al Editor de texto de Correspondence Manager, el estilo se pierde. NPR-19530
* El contenido sin salto de línea del Editor de texto no se puede ajustar. NPR-19481
* Funcionalidad habilitada para buscar texto actual en fragmentos del documento cuando se obtiene una vista previa de una carta. NPR-17792: revisión para CQ-4214501

#### Administración de correspondencia {#correspondence-management-5}

>[!NOTE]
>
>Esta funcionalidad de búsqueda de fragmentos de texto tiene algunas restricciones:
>
>* El contenido de los fragmentos de documento distingue entre mayúsculas y minúsculas y los títulos no distinguen entre mayúsculas y minúsculas.
>* Los resultados de la búsqueda no se resaltan cuando parte de la palabra buscada tiene un estilo diferente o contiene un carácter especial como &quot;, &#39; o \.
>* La búsqueda no funciona para contenido dinámico (como valores de elementos del diccionario de datos o valores de variables) dentro del fragmento de documento.

#### Administrador de Forms {#forms-manager-2}

* Las propiedades del esquema XML de los formularios adaptables no se pueden editar después de aplicar el CFP6 en AEM 6.2. Revisión para CQ-4219684
* Todos los servicios del paquete principal de AEM Forms Manager no se inician al reiniciar el servidor. Revisión para CQ-4217014

### Instalador JEE de Forms {#forms-jee-installer-12}

#### Instalación de LCM {#install-lcm-2}

* La pantalla del administrador de Microsoft® Windows muestra la versión número 6.0 después de instalar el CFP6. Revisión para CQ-4217573

## Paquetes de funciones incluidos {#feature-packs-included-2}

* Mejoras en los botones de la IU táctil de la aplicación de escritorio. NPR-18676

## Paquetes OSGi incluidos en CFP8 {#osgi-bundles-included-in-cfp}

Lista de paquetes OSGi incluidos en el SP1-CFP8 de AEM 6.2

[Obtener archivo](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP8 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP7 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Cambio de comportamiento en la visualización de títulos en la tarjeta de imagen para una imagen que tiene la propiedad dc: title establecida en String (multifield).
* Correcciones en el problema de rendimiento con Cloud Service de Dynamic Media, IU táctil e IU de seguridad.
* Correcciones en Apache Felix Http Bridge 3.0.8
* Se ha resuelto la replicación sin binarios (BLR) entre el entorno de creación y publicación.
* Compatibilidad con el archivo de la biblioteca de Target AT.JS, una biblioteca de implementación para la integración del lado del cliente con Adobe Target, está diseñada tanto para implementaciones web típicas como para aplicaciones de una sola página.
* Se ha mejorado el rendimiento de AEM al introducir un período de tiempo de espera de conexión configurable por el usuario para Analytics, DTM y Target.

### Recursos {#assets-12}

* Al probar la ingestión de vídeo con AEM 6.3 configurado con Cloud Services de Dynamic Media, se produce la excepción “Demasiados archivos abiertos”. NPR-18734, revisión para CQ-4211407
* La configuración de URL de vanidad para los recursos de una página no funciona después de reiniciar la instancia de AEM. NPR-18634; revisión para Granite-18085
* En la IU táctil, el botón Publicar se muestra para los usuarios sin permiso para publicar recursos. NPR-18620, revisión para CQ-4214042
* La opción de representación dinámica no está presente en el cuadro de diálogo de descarga de un recurso una vez que el contrato de licencia se ha establecido para él. NPR-18607, revisión para CQ-4212342
* No se puede descargar la representación dinámica para los recursos que incluyen espacios en sus nombres. NPR-18571, revisión para CQ-4211738
* No se puede guardar más de un usuario al compartir la carpeta de recursos con Creative Cloud. NPR-18489, revisión para CQ-103297
* dc: title y dc: description no cambian a un valor de varios campos en crx/de. NPR-18474, revisión para CQ-4209086
* La operación de mover recursos causa una degradación del rendimiento. NPR-18346
* No se muestran elementos en la línea de tiempo cuando se abre con el conjunto de opciones predeterminado Mostrar todo. NPR-18302, revisión para CQ-4211957
* Se produce un error cuando se carga un archivo de texto con codificación ASCII/UTF-8 en AEM Assets y falla la generación de miniaturas. NPR-18006: CFP para CQ-4209345
* Los botones de acción de Publish están visibles incluso cuando el usuario no tiene acceso replicado. NPR-17353, revisión para CQ-4209269
* Tanto el administrador del sitio como el administrador Misc no funcionan cuando la minificación está habilitada usando min:gcc;obfuscate=true. NPR-18593, revisión para CQ-4209220
* Los elementos de menú personalizados no aparecen hasta que la pantalla se actualiza cada vez. NPR-18500, revisión para CQ-4213581
* Actualice moment.js a 2.10.6. NPR-18596; revisión de Granite-11881
* La aplicación de permisos para macros DM rompe la vista para el usuario Administrador. NPR-18544, revisión para CQ-4211729
* Publicar más tarde para recursos está generando ArgumentException de forma no válida. CQ-4214532

### Sites {#sites-12}

* En un clúster de autores activo-activo con MongoDB, ambos autores intentan almacenar en déclencheur la replicación para el mismo contenido cuando el tiempo alcanza el valor de tiempo de activación establecido para el contenido. NPR-18708, revisión para CQ-4210982
* NPE al mover un recurso con una referencia que no tiene jcr: nodo de contenido. NPR-18664
* Los marcadores de posición no están visibles en una página que contiene varios componentes Parsys. NPR-18645, revisión para CQ-110253
* Problemas de concurrencia en AbstractCopyMoveCommand. NPR-18591
* Al copiar texto en un componente Parsys desde otra instancia de AEM, Parsys se crea sin ningún resourceType establecido. NPR-18511, revisión para CQ-4212306

### Plataforma {#platform-10}

* El instalador JCR no actualiza la versión del paquete después de la instalación del paquete. NPR-18728; revisión para NPR-15135
* La replicación sin binarios (BLR) falla con entornos de creación y publicación de binarios. NPR-18704
* Solicitud de resolución de Apache Felix Http Bridge AEM en un entorno de. NPR-18297
* La replicación falla cuando varias páginas con una estructura similar se replican simultáneamente con Sling Content Distribution. NPR-18665; revisión para Granite-13712
* Los paquetes de distribución de Sling se acumulan y no se limpian automáticamente. NPR-18601; revisión para Granite-16183

### Integración {#integration-13}

* La visualización de ofertas publicadas desde carpetas de la biblioteca se produce en NPE. NPR-18732, revisión para CQ-4214593
* La fecha de inicio o finalización de una actividad no se actualiza en JCR y Destinatario cuando se cambia de una fecha específica a “Al activarse o desactivarse”. NPR-18612, revisión para CQ-104831
* La integración de Analytics con AEM no tiene tiempo de espera de conexión o de socket establecido para las conexiones httpclient. NPR-18497
* La integración de DTM con AEM no tiene tiempo de espera de conexión o de socket establecido para las conexiones httpclient. NPR-18495
* La integración de Target con AEM no tiene tiempo de espera de conexión o de socket establecido para las conexiones httpclient. NPR-18494
* La actividad de destinatario se desactiva después de añadir una experiencia adicional. NPR-18227, revisión para CQ-4201895

### WCM: componentes base {#wcm-foundation-components-7}

* Los mapas de imagen no conservan las coordenadas seleccionadas en el componente de imagen HTL. NPR-18530, revisión para CQ-4211584

### Traducción {#translation-5}

* Los resultados de la búsqueda de traducción no incluyen los nombres de proyectos de traducción. NPR-18224, revisión para CQ-4210658

### Brand Portal {#brand-portal-1}

* AEM Habilitar las etiquetas de publicación desde la consola de administración de etiquetas/etiquetado a Brand Portal desde la de publicación. CQ-4212165

## Forms {#forms-13}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [Versiones de AEM Forms](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-13}

#### Administración de correspondencia {#correspondence-management-6}

* Los datos correctos no se muestran en el panel de edición hasta que se guarda el fragmento. NPR-19092
* Añadir un fragmento de documento a una carta toma mucho tiempo. NPR-18958
* Si existe una declaración XML en un archivo XML de datos y la representación de la carta se inicia mediante una solicitud del POST, la carta correspondiente no muestra los datos. NPR-18870
* No se generan registros de auditoría para las acciones realizadas en los recursos de CM. NPR-16618

>[!NOTE]
>
>No instale este paquete añadido de CFP si tiene alguno en los dos problemas siguientes:
>
>* Copiar y pegar desde Word o desde la Web en el editor de texto de CM muestra el contenido de salto de línea. NPR-19530
>* El contenido sin salto de línea del Editor de texto de CM no se puede ajustar. NPR-19449
>

#### Formularios adaptables {#adaptive-forms-9}

* Al agregar un panel para paneles repetibles, se elimina el valor del campo desplegable del panel anterior. NPR-18772
* Los campos de formulario adaptables están marcados para aceptar solo enteros, y también aceptan algunos caracteres especiales del teclado numérico. NPR-18680
* No funciona ningún script para cambiar el título del botón en el evento de inicialización del panel raíz de la guía. NPR-18476
* La barra de desplazamiento no aparece en el panel derecho para las reglas creadas con el Editor de reglas. NPR-18716

#### Aplicación de AEM Forms {#aem-forms-app}

* Forms no se representa correctamente en la aplicación de AEM Forms cuando está en modo sin conexión o no conectado a la red. CQ-4218368

### Instalador JEE de Forms {#forms-jee-installer-13}

#### Servicio PDFG {#pdfg-service-3}

* PDF Generator no produce documentos PDF con los niveles de marcador especificados. Revisión para CQ-4211102

## Paquetes OSGi incluidos en CFP7 {#osgi-bundles-included-in-cfp-1}

Lista de paquetes OSGi incluidos en el SP1-CFP7 de AEM 6.2

[Obtener archivo](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP7 de AEM 6.2

[Obtener archivo](assets/do-not-localize/cfp7_content_packages.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP6 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Administración eficaz de los componentes ocultos en el modo de diseño en la tableta.
* Introducción de acciones rápidas en dispositivos híbridos.
* Resolución de problemas de sincronización a nivel de componente con Live Copies.

### Recursos {#assets-13}

* Un cliente se bloquea cuando un usuario que no tiene el permiso necesario intenta mover una operación en un recurso. NPR-18330, revisión para CQ-4212560
* La combinación de varias configuraciones de servicios de contenido inteligente causa problemas de uso. NPR-18273, revisión para CQ-4201557
* La acción de cierre de compra/flujos de trabajo no están disponibles en la consola Cronología una vez, aproximadamente, Se han añadido 80 fragmentos en la carpeta Assets. NPR-18257; revisión para CQ-4211214 y NPR-18251; revisión para CQ-4211216.
* El sistema se bloquea en Memoria insuficiente y carece de paginación durante los informes de Recursos. NPR-17865, revisión para CQ-4209759
* El vídeo publicado no se reproduce en un recurso de vídeo codificado. NPR-17849, revisión para CQ-4210739
* No se genera una miniatura para el PDF. NPR-17831, NPR-17750; revisión para CQ-4210547
* El trabajo de notificación de caducidad de Adobe CQ DAM no desactiva los recursos caducados. NPR-17666, revisión para CQ-107766
* Las actividades de caducidad de recursos se detienen si un recurso no tiene un propietario asignado. NPR-17665, revisión para CQ-4197946
* Se genera una excepción de puntero nulo cuando se mueve una carpeta de recursos con más de 150 referencias entrantes. CQ-4200981

### Sites {#sites-13}

* Personalization solo funciona para la primera IP cuando la regla de segmentación está establecida para un intervalo de IP. NPR-18121, revisión para CQ-83767
* El inicio de sesión falla debido a NumberFormatException cuando la propiedad historyShow está habilitada. NPR-18073, revisión para CQ-101965
* Las páginas eliminadas marcadas son visibles en la IU táctil. NPR-18025, revisión para CQ-86694
* Problemas de rendimiento al cargar una página con audiencias grandes (más de 2000). NPR-17884, revisión para CQ-4209567
* No puede seleccionar una imagen después de quitar otra imagen de la página. NPR-17711, revisión para CQ-4201323

### Plataforma {#platform-11}

* Los controles de la IU táctil están ocultos para los usuarios que tienen los permisos necesarios. NPR-17945, revisión para CQ-4211231
* Faltan etiquetas japonesas en el campo de selección de etiquetas. NPR-17768, revisión para CQ-4210456
* La consulta getsize() devuelve resultados incorrectos cuando FastQuerySize está habilitado. NPR-18018
* No se puede acceder a la consola web en la instancia de espera. NPR-17861; revisión para Granite-14582

### Comercio {#commerce-2}

* La inversión de consulta se produce cuando un modelo de catálogo no tiene ninguna condición definida para una sección. NPR-18229, revisión para CQ-4211924

### Comunidades {#communities-2}

* PollingImporterImpl. retrasa el cierre de AEM. NPR-18298, revisión para CQ-96133

### Integraciones {#integrations}

* Se han resuelto los errores de componentes de AEM Search que se pueden producir cuando el OSGI de AEM Day HTTP Client 3.1 se configura con un proxy que requiere autenticación implícita. NPR 18128
* Falta la casilla de verificación para poder revertir la herencia. NPR-17753: solicitud de revisión para CQ-4210139
* Los usuarios no pueden configurar la prioridad al destinar un componente con varias actividades. NPR-18658, revisión para CQ-4210727
* Los usuarios no pueden examinar la carpeta /etc/segmentation para seleccionar una audiencia creada en la carpeta /etc/segmentation/group1. NPR-18522

### Seguridad {#security-1}

* El asistente para mover recursos se bloquea si el usuario no tiene permiso de escritura en la carpeta destinatario. NPR-18300
* Solicite utilizar una versión actualizada del servlet org.apache.sling.servlets.post (2.3.22) en la API de Apache Sling para evitar una vulnerabilidad XSS. NPR-18963

### Traducción {#translation-6}

* El envío de la página de recursos no debe ser necesario de nuevo para un proyecto de traducción hasta que se complete el proyecto. NPR-18249, revisión para CQ-4209908

### WCM: componentes base {#wcm-foundation-components-8}

* No se puede usar el componente Iparsys de base de WCM en plantillas editables. NPR-18223, revisión para CQ-4210384
* El Mapa de imagen no conserva las coordenadas seleccionadas en el componente de imagen HTL. NPR-18032, revisión para CQ-4211584
* Cuando se procesa un componente de imagen HTL, se cambia el nombre del archivo en la dirección URL, lo que provoca que se interrumpa la dirección URL. NPR-17908, revisión para CQ-4211587
* No se puede salir de las propiedades de la página después de realizar los cambios. NPR-17832, revisión para CQ-96110

## Forms {#forms-14}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [Versiones de AEM Forms](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-14}

**Administración de correspondencia**

* El diccionario de datos se lee repetidamente durante la representación de cartas. NPR-18482, revisión para CQ-4210805
* Se ha añadido JavaDocs para la clase com.adobe.livecycle.content. NPR-18467
* Al crear una carta, no se guarda la descripción de la carta. NPR-18039
* Cuando se guarda un módulo de texto y una expresión del módulo de texto no contiene etiquetas de expresión de apertura o cierre, no se muestra ningún mensaje de error. El módulo de texto muestra un mensaje de error y no se puede procesar en la carta. NPR-17798
* Se observan errores inesperados en los registros de la instalación de un paquete de complementos. NPR-18295

**Administrador de Forms**

* La IU de AEM Forms enumera todos los recursos en el primer orden más antiguo. Los usuarios no pueden reordenar los recursos en el primer orden más reciente. NPR-18451

### Instalador JEE de Forms {#forms-jee-installer-14}

**Servicio de salida**

* Se ha mejorado el problema de rendimiento del Servicio de salida para AEM Forms 6.2. NPR-18033

**Servicio de firmas**

* No se puede firmar un documento de PDF con un Módulo de seguridad de hardware remoto. NPR-18017

## Paquetes OSGi incluidos en CFP6 {#osgi-bundles-included-in-cfp-2}

Lista de paquetes OSGi incluidos en el SP1-CFP6 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Lista de paquetes de contenido incluidos en el SP1-CFP6 de AEM 6.2

[Obtener archivo](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP5 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se han resuelto varios problemas de la interfaz de usuario con el uso compartido, el desplazamiento, la publicación y la descarga de recursos.
* Se ha aumentado la capacidad del cuadro de diálogo Mover para mostrar los recursos a los que se hace referencia.
* Se han resuelto varios problemas relacionados con los componentes y flujos de trabajo de Gestión de contenidos web (WCM), como Cancelar publicación y Depurar versión.
* Se ha mejorado la respuesta de la barra de acciones al mostrar las acciones de la barra de herramientas y los componentes de Coral.

### Recursos {#assets-14}

* Mejoras de rendimiento en la funcionalidad de publicación en Brand Portal. NPR-17189, revisión para CQ-4204150
* Al compartir un recurso mediante la opción Compartir vínculo, no se crea un archivo zip con una estructura de carpetas plana para la descarga. NPR-17513, revisión para CQ-4209381
* Al seleccionar un recurso en DAM y hacer clic en Publicar, no se muestra la opción Publicar en Brand Portal en la página Detalles del recurso. NPR-17351, revisión para CQ-94905
* En los pasos del flujo de trabajo de DAM, las secuencias binarias adquiridas desde Session o ResourceResolver deben cerrarse en un bloque final. Al hacerlo, se garantiza de que no se produzcan fugas de recursos. NPR-17385, revisión para CQ-4209452
* Al cargar un documento de Word en DAM, se produce una excepción de puntero nulo y la instancia del flujo de trabajo permanece atascada en el estado de ejecución. NPR-17160, revisión para CQ-4207358
* Los botones Compartir, Mover, Publicar y Descargar están visibles para los recursos caducados en la página del editor de metadatos para los usuarios no administradores. NPR-16903; revisión para CQ-101440/CQ-104535
* Las acciones como Compartir, Mover, Publicar y Copiar deben estar visibles para los usuarios administrativos en la consola Recursos. NPR-16902, revisión para CQ-4207111

### Sites {#sites-14}

* Al mover una página mediante la IU clásica y táctil, el cuadro de diálogo Mover no muestra referencias superiores a 150, lo que impide que los usuarios actualicen estas referencias y vuelvan a publicar la página. Este problema se ha corregido introduciendo una propiedad para la IU clásica: &#39;maxRefNo&#39; que se puede configurar en el nodo de administración del sitio: `'/libs/wcm/core/content/siteadmin'`. Esta propiedad especifica el número máximo de referencias (valor predeterminado 150) que se muestran antes de una operación de movimiento intensivo. Si una página tiene varias referencias, no se muestran en el cuadro de diálogo movePage. Esta configuración también funciona para la administración de DAM y otros administradores al aplicar la configuración en los nodos: `'/libs/wcm/core/content/damadmin'` y `'/libs/wcm/core/content/miscadmin'` respectivamente. NPR-17222, revisión para CQ-85878

* Al trabajar con componentes de WCM, los hipervínculos con espacios se eliminan en el Editor de texto enriquecido de la IU táctil. NPR-17698, NPR-17570; revisión para CQ-4206768
* Al activar el flujo de trabajo Solicitud de cancelación de publicación desde las propiedades de página, aparecen errores de JavaScript para los usuarios sin derechos de replicación. NPR-17294, revisión para CQ-102064
* Al procesar o exportar un componente de imagen HTL, la URL cambia a un número y se cambia el nombre del archivo, lo que provoca que se rompan los vínculos. NPR-17245, revisión para CQ-59616
* Al eliminar un lanzamiento en un lanzamiento anidado, los sublanzamientos quedan huérfanos. NPR-17228, revisión para CQ-4202639
* La ejecución de la depuración de versiones en AEM 6.2 con Oak 1.4.13 aplicado provoca una advertencia repetida constantemente en los registros. NPR-17391, revisión para CQ-4206870
* Después de instalar una revisión o una actualización para el componente ContextHub, el paquete de contenido sobrescribe todos los segmentos en /etc/segmentation/contexthub, lo que provoca una pérdida de todos los segmentos personalizados de ContextHub. NPR-17250, revisión para CQ-79958
* Al ejecutar un flujo de trabajo con grupos anidados como usuarios del flujo de trabajo, WorkflowStatusProvider (pageinfo.json) hace que la instancia del flujo de trabajo se bloquee. NPR-17555, revisión para CQ-4202056
* Al utilizar los componentes del editor de páginas WCM, existe una gran cantidad de espacio vacío al final de la página en el modo de edición de la IU táctil de la instancia de autor. NPR-17510, revisión para CQ-4205441
* Al procesar o exportar un componente de imagen HTL, la URL cambia a un número, lo que provoca que se rompan los vínculos. NPR-17245, revisión para CQ-59616

### IU {#ui}

* Al seleccionar un recurso y hacer clic en Herramientas de desarrollador, no siempre se muestran las acciones de la barra de acciones en conexiones lentas y la página debe volver a cargarse. NPR-17568, revisión para CQ-108365
* La barra de acciones debe actualizarse para utilizar dos contenedores: coral-actionbar-primary y coral-actionbar-secondary, en lugar de coral-actionbar-container. NPR-17591; revisión para GRANITE-15225

### Mobile On-Demand {#mobile-on-demand-2}

* Los usuarios con permisos de &quot;Solo lectura&quot; en la aplicación de AEM Mobile no pueden obtener una vista previa del contenido desde la página de Administración de contenido de AEM Mobile. NPR-17390, revisión para CQ-4209690

### Seguridad {#security-2}

* Vulnerabilidad XSS en la salida generada por HTMLRendererServlet. NPR-17136
* Solicitud para evitar que se divulgue la versión AEM en la página Fuentes de distribución web de AEM. NPR-16219

### Forms {#forms-15}

#### Paquete de complemento de Forms {#forms-add-on-package-15}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

**Formularios adaptables**

* Para un formulario adaptable con datos adjuntos, las entradas duplicadas para las etiquetas afSubmissionInfo se crean en el XML enviado cuando el formulario se envía por segunda vez. NPR-17364
* Cuando se utiliza el explorador Google Chrome, después de quitar un archivo adjunto de un formulario, al intentar volver a adjuntarlo se genera un error. NPR-17297
* En caso de que haya paneles anidados y repetitivos cargados a medida en los formularios adaptables basados en XSD o en modelo sin formulario, los valores rellenados en el formulario no se conservarán en el documento de registro (DOR). NPR-17176
* Los errores mostrados en el registro de errores del editor de reglas deben agregarse en el bloque catch de un código JavaScript de bloque try/catch. NPR-16757
* Al hacer clic en un archivo adjunto en un formulario, se produce un error en la consola del explorador y no se muestra la previsualización de datos adjuntos. NPR-17174

**Administración de correspondencia**

* La funcionalidad Crear interfaz de usuario de correspondencia se interrumpe en caso de que se añada texto en línea o una línea en blanco en la IU. NPR-17748
* El navegador parpadea cuando se abre una carta para editarla. NPR-17576
* Al agregar funciones remotas en elementos del diccionario de datos calculados, si el número de funciones es superior a la longitud de la pestaña que muestra funciones remotas, la barra de desplazamiento no aparece en la pestaña. NPR-17359
* El método de la API `com.adobe.icc.services.api.LetterInstanceService` para importar no funciona. NPR-17922, NPR-16008
* Una variable agregada en un módulo de texto no está visible en el panel Enlace de datos mientras se edita una carta. NPR-17940
* La IU de Administración de correspondencia no se inicia cuando una acción de envío del HTML utiliza el método de POST. NPR-17595

**Administrador de Forms**

* Con un formulario adaptable configurado para la prueba A/B, al hacer clic en Iniciar AB Testing no se inicia la prueba y se genera un error de consola del explorador. NPR-17838

**Servicio de Forms**

* Deben solucionarse los problemas notificados en el análisis del código estático de OSGI Forms. NPR-13951

#### Instalador JEE de Forms {#forms-jee-installer-15}

**Servicio de salida**

* AEM El uso del servicio de salida de Forms 6.2 para combinar un formulario específico con un XML de datos tarda 20 veces más tiempo. Ahora se corrige en entornos Windows y Linux®. NPR-17501

**Instalación de LCM**

* Después de instalar AEM Forms 6.2 GM y aplicar el CFP de AEM 6.2, al ejecutar Administrador de configuración de LiveCycle se muestra un punto y coma no deseado en la Información de la versión y la fecha de instalación del parche no se actualiza. NPR-14322

**Administración de procesos**

* La variable TaskContext no se rellena para los procesos de AEM Forms. CQ-4211857

#### Paquetes JEE de AEM Forms {#aem-forms-jee-bundles-package}

* Las capacidades de los usuarios de formularios, tanto si utilizan la consola de la IU de administración de JEE como la consola OSGi, deben ser las mismas. NPR-17670

### Paquetes de funciones incluidos en CFP5 {#feature-packs-included-in-cfp}

**Paquete JEE de Forms**

Administración de procesos - Espacio de trabajo HTML

* Al asignar un paso de espacio de trabajo, la pestaña archivos adjuntos del espacio de trabajo debe mostrar un contador para los datos adjuntos o las notas en caso de que haya más de un dato adjunto o nota. NPR-17771
* Solicite soporte técnico para Office 365 en AEM JEE Forms para funciones de correo electrónico en el flujo de trabajo del formulario. NPR-13866

**Paquete de complemento de Forms**

Administración de correspondencia

* Al editar fragmentos en el Editor de texto durante una vista previa de la carta, el texto procesado debe mostrarse para su edición en lugar de las condiciones en línea utilizadas en los fragmentos. NPR-15748, NPR-17504

### Paquetes OSGi incluidos en CFP5 {#osgi-bundles-included-in-cfp-3}

Lista de paquetes OSGi actualizados entre AEM 6.2 SP1-CFP5

[Obtener archivo](assets/do-not-localize/cfp5_osgi_bundles.txt)

Lista de paquetes de contenido actualizados entre AEM 6.2 SP1-CFP5

[Obtener archivo](assets/do-not-localize/content-package-cfp5.txt)

El paquete de correcciones acumulativas 6.2 SP1-CFP4 de AEM es una actualización importante que incluye correcciones clave del cliente publicadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Correcciones en los recursos para la representación de archivos Camera Raw, la vista de la línea de tiempo y la orientación de la imagen
* Mejora en

   * WCM se inicia en los sitios
   * Flujo de trabajo de proyectos
   * Componentes de ContextHub

* Correcciones de Campaign, Mobile On-Demand y Traducción
* Mejoras de uso en el editor de reglas de formularios adaptables
* Editor de condiciones en línea mejorado para la administración de correspondencia en formularios
* Correcciones de administración de procesos y servicios de salida para AEM Forms en JEE
* Corrección relacionada con Forms Designer para el Editor de Script

### Plataforma {#platform-12}

* Adición o personalización de columnas al **Assets OmniSearch** resultados al superponer en `/apps` no funciona. NPR-16737: revisión para CQ-4206785
* La página **Herramienta de diagnóstico** no funciona después de una actualización in-situ de AEM 6.1 SP2 a AEM 6.2 SP1. NPR-17121, revisión para CQ-4196786
* HTL: Al seleccionar un Foro, crear un Tema y una Publicación, `Sightly SightlyCompiledScript` añade la propiedad `addSelectors` incorrecta a `RequestDispatcherOption`. NPR-17008: revisión para GRANITE-16384

* Compatibilidad añadida para `CRON expressions` en `ManagedPollConfigs` utilizada por `ReportImporter`. NPR-16608: Solicitud de revisión para CQ-4206066

* Error al cargar una imagen de avatar para un usuario LDAP. NPR-16561; revisión para Granite-17013
* El número de resultados que se muestran en la pantalla Administración de usuarios es diferente en las vistas Tarjeta y Lista. NPR-16241; revisión para GRANITE-16914
* Las notificaciones de flujo de trabajo no se cargan de forma diferida mientras se visualizan en el navegador Google Chrome en Modo de pantalla completa. NPR-17013: revisión para CQ-4207567

### Recursos {#assets-15}

* La orientación de la imagen no se aplica correctamente al importar una imagen con una orientación definida. NPR-16750: revisión para CQ-4204356
* La vista de línea de tiempo de recursos no muestra ningún recurso aunque “Mostrar todo” esté definida de forma predeterminada. NPR-16957: revisión para CQ-98780
* Los archivos `Camera RAW` (incluidos ARW, CR2, NEF, DNG y EPS) cuando se añaden como representación en los recursos, no se pueden seleccionar ni eliminar. Estos archivos se descargan automáticamente cuando el usuario hace clic en ellos. NPR-16949: revisión para CQ-4206846
* La creación de un PDF dentro de otro PDF en la IU de Assets no muestra los PDF creados en la IU de DAM. Sin embargo, los PDF están visibles en el repositorio de CRX. NPR-16833: revisión para CQ-4206501
* La carga de un recurso como nodo secundario directo por sí mismo mediante la IU táctil provoca un problema. El recurso se carga como elemento secundario directo del recurso seleccionado anteriormente. NPR-16534: revisión para CQ-4204287
* En la IU de DAM, comentar un recurso y etiquetar a un usuario en el comentario no genera una notificación por correo electrónico. NPR-16589: revisión para CQ-102318

### Proyectos {#projects-3}

La consola de flujo de trabajo Proyectos muestra una NullPointerException en la página cuando se purgan flujos de trabajo. NPR-17017: revisión para CQ-4194269

### Sites {#sites-15}

* Los archivos de `ContextHub` no se minimizan en la instancia de autor. NPR-17022: revisión para CQ-79456
* La promoción de inicio de WCM-Launches tarda mucho tiempo en promocionar un lanzamiento que consta de un árbol grande de una página. NPR-16480: revisión para CQ-82731
* `ClientContext` El Procesador de condiciones de segmento se bloquea cuando se crea un segmento (o audiencia) con una regla que no funciona o que no ha terminado. NPR-16759: revisión para CQ-4205104
* En el Inicio de WCM, las páginas asociadas con un lanzamiento no se pueden cancelar cuando la acción se inicia desde las propiedades de la página en la IU táctil. NPR-16560: revisión para CQ-4204681
* Link Rewriter reescribe falsamente los valores href que contienen dos puntos suponiendo que el signo de dos puntos “:” define un área de nombres JCR. NPR-16753: revisión para CQ-4203762
* En WCM-Design Importer, abrir una página del importador de pruebas e intentar cargar un archivo zip provoca problemas si se ha cargado y eliminado anteriormente. NPR-16486: revisión para CQ-90962
* Navegación al **[!UICONTROL Navegación global]** El panel que utiliza los navegadores Firefox o Google Chrome ofrece una experiencia de usuario diferente. El navegador Firefox muestra el **[!UICONTROL Herramientas]** menú. El explorador Chrome de Google muestra la **[!UICONTROL Navegación]** menú. NPR-16770, revisión para CQ-4200456

### Campaign {#campaign}

* AEM Al probar plantillas de campaña de y modificar direcciones semilla para incluir &quot;Datos adicionales&quot;, la lista desplegable de Adobe Campaign desaparece en el Context Hub de la IU táctil. NPR-16771: revisión para CQ-105748

### Mobile On-Demand {#mobile-on-demand-3}

* AEM AEM Al comprobar previamente una publicación desde Autor de la prueba, una acción de verificación previa que dure más de cinco segundos provoca un pico inusual en el panel del fragmento de integración de AEMM - PECS con un número elevado de solicitudes de estado. NPR-16908: revisión para CQ-4207055
* El administrador de configuración de AEM Mobile falla después de instalar la actualización AEM-6.2-SP1-CFP1-1.0. NPR-16909: revisión para CQ-4204892

### Traducción {#translation-7}

* La vista previa de los trabajos de traducción no funciona después de instalar 6.2 SP1 - CFP1. NPR-16481, revisión para CQ-4204655
* La copia de idioma creada mediante la traducción apunta a la raíz principal en lugar de a la Live Copy del país local. NPR-17257, revisión para CQ-4208287

### Seguridad {#security-3}

* No se realiza ninguna validación de tipo MIME cuando se cargan archivos binarios en AEM. NPR-16617
* Problemas con la carga de imágenes de avatar para usuarios LDAP. NPR-16561

### Forms {#forms-16}

#### Paquete de complemento de Forms {#forms-add-on-package-16}

**Formularios adaptables**

* En el editor de Forms adaptable, el comentario Configuración de destinatario en head.jsp debe reemplazarse por la nueva instrucción context hub. NPR-17173
* En el Editor de reglas de Forms adaptable, la variable **[!UICONTROL Elegir un elemento]** muestra el evento como &quot;nulo&quot;. NPR-17139
* El formulario enviado se volverá a enviar navegando hacia delante mediante la flecha hacia delante (>). NPR-17080
* AJAX Al enviar un formulario adaptable mediante una llamada de retorno, la función de devolución de llamada &quot;error&quot; nunca se invoca si hubo un error. NPR-17034
* Al hacer clic en el botón **[!UICONTROL Guardar formulario]** en el Editor de reglas en tiempo de ejecución, no se guarda el formulario. NPR-16905
* El texto estático debe excluirse de la orden de tabulación en el formulario adaptable. NPR-16749
* El valor calculado de un campo decimal aparece incorrectamente. NPR-16596
* El icono para mostrar el contenido de ayuda debe incluirse en la orden de tabulación en los formularios adaptables. NPR-16484
* Compatibilidad con expresión regular de tipo `dataRef=C:/Users/`en el **[!UICONTROL Configuración predeterminada del servicio de relleno previo]**. Este tipo es para el relleno previo de datos para Forms adaptable. NPR-16425

* Las validaciones no se activan correctamente en todos los paneles si hay un escenario anidado con carga diferida. NPR-15821

**Administración de correspondencia**

* La representación de carta falla si una carta contiene un módulo de texto en blanco (uno sin texto). NPR-17054
* Los saltos de línea y los espacios de tabulación se eliminan del contenido después de pegarlos en el Editor de texto. NPR-17039
* La visualización de referencias de un módulo de texto tarda mucho tiempo si se hace referencia al módulo de texto en muchas cartas. NPR-17035
* Editar, guardar, eliminar y establecer referencias para fragmentos de documento lleva mucho tiempo. NPR-17033
* El texto justificado se representa con una fuente diferente al obtener una vista previa de la carta. NPR-16976
* La funcionalidad de búsqueda no funciona correctamente si el texto buscado tiene varias ocurrencias. NPR-16920
* La barra de herramientas del Editor de texto se muestra en el navegador de forma intermitente. NPR-16919
* La construcción **[!UICONTROL Guardar formulario]** del Editor de reglas no funciona. NPR-16905
* La lista desplegable Fuente no rellena la familia Fuente al crear un módulo de texto basado en un diccionario de datos mediante Internet Explorer. NPR-16944
* Después de crear un fragmento de texto, la fuente de la carta cambia al obtener una vista previa de la carta. NPR-16830
* Las cartas con espacios de tabulación al principio o entre expresiones en el fragmento de documento no se pueden procesar ni previsualizar. NPR-16769

**Mobile Forms**

* La previsualización de Mobile Form muestra contenido superpuesto, aunque el formulario se muestra correctamente para la representación en PDF. NPR-17105

**Forms Portal**

* Al hacer clic en el vínculo **[!UICONTROL Descargar]** para un formulario enviado, se abre una página HTML en lugar de un formulario PDF. NPR-17082

* `Upload Comments` para archivos adjuntos que no se muestran en la interfaz de usuario para instancias enviadas, aunque estén presentes en el XML almacenado en el repositorio de CRX. NPR-17075

**Reader Extensions Service**

* Un archivo específico no es Reader Extended en la instalación de OSGI en AEM Forms. NPR-16625

#### Instalador JEE de Forms {#forms-jee-installer-16}

**Núcleo**

* Durante el proceso de actualización, el Administrador de configuración falla con el tiempo de espera. NPR-16774 (Consulte [Configuración del tiempo de espera para operaciones a nivel de componente](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Administración de procesos - Espacio de trabajo HTML**

* El punto de partida de una Tarea de inicio no comienza con los datos enviados en el momento del envío del punto de inicio. NPR-16917
* Al hacer clic en el botón **[!UICONTROL Devolver]** para un formulario en el espacio de trabajo HTML, el formulario no se cierra, pero se devuelve a la Cola de grupo. 
NPR-16352

**Administración de procesos**

* Permite a los usuarios establecer el nombre para mostrar de tareas anteriores en cualquiera de las siguientes tareas de una instancia de proceso. NPR-15382

**Servicio de salida**

* El Servicio de salida no puede procesar un PDF modificado para incluir el campo adicional &quot;milisegundos&quot; en la `date-time format` metadatos. NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer Script Editor no respeta los valores predeterminados de Propiedades del formulario para `Calculate Event`y `Validate Event`. NPR-15921

### Paquetes de funciones incluidos en CFP4 {#feature-packs-included-in-cfp-1}

**Paquete de complemento de Forms**

* Mejora en el Editor de condiciones en línea para la Administración de correspondencia. NPR-10981

### Paquetes OSGi incluidos en CFP4 {#osgi-bundles-included-in-cfp-4}

Lista de paquetes OSGi actualizados entre AEM 6.2 SP1 y CFP4

Los puntos destacados de CFP3 son:

* Capacidad de búsqueda más eficaz para la IU clásica y para el componente de búsqueda de AEM mediante proxy con autenticación implícita
* Soluciona problemas al cargar recursos y mostrar metadatos de recursos
* Soluciona problemas al crear carpetas y mover páginas en caso de que el título tenga caracteres especiales.
* Correcciones para usar audiencias de sincronización de destinatarios, publicar campañas y seleccionar la Métrica de objetivos en la IU táctil
* Resuelve problemas de sincronización para trabajos de traducción
* Proporciona seguridad mejorada para el servicio de cumplimentación previa de Forms
* Mejoras en el componente de borrador y envío del portal de Forms y en el servicio de Forms con códigos de barras
* Mejoras de uso para formularios adaptables que contienen widgets de archivos adjuntos o fragmentos cargados de forma diferida.
* Mejoras de uso en la Administración de correspondencia, incluida la capacidad de búsqueda mejorada, el registro de recursos eliminados y la importación de diccionarios de datos.

### Plataforma {#platform-13}

* Una condición de carrera en **ModelAdapterFactory**, la cual es posible cuando dos subprocesos intentan inyectar el mismo campo, da como resultado un error al construir el modelo. NPR-16443: revisión para SLING-6584
* Opción de validación en el Administrador de paquetes para detectar cualquier conflicto entre el archivo superpuesto (JSP o archivo JavaScript) en `/apps` y el que contenía una revisión en `/libs`. La superposición afectada se puede volver a basar para incluir cambios del archivo en `/libs`. NPR-16216: revisión para CQ-81729
* El inicio de sesión en error.log a veces se detiene unos segundos después de iniciar el editor y debe borrarse para volverse a ejecutar. Solicite actualizar el marco de registro y proporcione el registro de Sling. NPR-15913: revisión para Granite-15452
* Solicitud para actualizar la API &quot; `use"` de JavaScript para evitar errores en la implementación de la API de uso de JavaScript de HTL. NPR-16461: revisión para SLING-6780

### Sites {#sites-16}

* Después de actualizar de AEM 6.0 a AEM 6.2, la IU clásica muestra un rendimiento lento al buscar etiquetas debido a numerosas consultas. Para resolver el problema, siga los pasos que se mencionan en [Deshabilitar el estado de replicación en la consola de etiquetado (IU clásica)](#disable-replication-status-in-tagging-console-classic-ui-npr) se puede seguir. NPR-15842: revisión para CQ-4201748.

* Al crear una página en la IU táctil, la Comprobación de entrada del campo &quot;nombre&quot; no comprueba el carácter especial &quot;Apóstrofo&quot; (el mismo que en la IU clásica). Por lo tanto, la página no se puede mover. NPR-16404: revisión para CQ-4205321.
* Al aplicar diferentes estilos en dos filas en el Editor de texto enriquecido y, a continuación, combinarlos, se elimina el estilo aplicado en la segunda fila. NPR-16389: revisión para CQ-4203835.
* En la pantalla Sitios de la IU táctil, al intentar pegar una página dentro de una página sin subpáginas, no se puede porque el botón Pegar no está disponible. NPR-15894: revisión para CQ-4201696.
* Al desplazarse por la pestaña Páginas del panel Buscador de contenido, algunos conjuntos de páginas se muestran indefinidamente en la IU clásica, mientras que la IU táctil muestra un conjunto limitado de pocas páginas no repetidas. NPR-16271: revisión para CQ-4202371
* Al abrir las propiedades de página de un LiveCopy en la IU táctil y hacer clic en Guardar sin ningún cambio, se escribe cualquier pestaña de LiveCopy y se crea un nodo de configuración de LiveSync. NPR-16327: revisión para CQ-108562
* La restricción de formulario no puede leer la propiedad `ConstraintMessage`. NPR-16388: revisión para CQ-101330
* El componente `wcm/foundation/components/parsys` no muestra el marcador de posición **[!UICONTROL “Arrastrar componentes aquí]**”. NPR: 16748: revisión para CQ-4205187

### Recursos {#assets-16}

* El rasterizador de PDF deja de funcionar y causa problemas de memoria insuficiente después de instalar 6.2 SP1 o la revisión 12430. NPR-15991
* Los metadatos de una propiedad de cadena, `documentNumber` se muestran como una fecha, mientras que debería ser un número. NPR-16134: revisión para GRANITE-16916
* Truncamientos de texto en el globo de evento de la línea de tiempo. NPR-16226: revisión para CQ-85226
* Cuando se crea una carpeta bajo la jerarquía de contenido con un título que contiene caracteres especiales, se muestra la versión codificada de esos caracteres. NPR-15935: revisión para CQ-4202987
* El usuario no puede cargar recursos ni crear carpetas mientras navega por los recursos debido a un comportamiento incoherente que se muestra al utilizar el botón Crear. NPR-16410: revisión para CQ-4204793
* Se han encontrado errores inesperados al cargar recursos HTML compartidos desde la vista de artículos en AEM Authoring. NPR-16133: revisión para AEMM-4155970

### Integración {#integration-14}

* AEM Al habilitar la autenticación proxy con Autenticación implícita, el componente Búsqueda en el código de tiempo de la aplicación emite una excepción ConcurrentModificationException. NPR-15309: revisión para CQ-4199191
* AEM Al crear una Actividad de prueba A/B de destinatario en la, la audiencia no se sincroniza con el Destinatario y muestra &quot;sin audiencias&quot;. NPR-16229: revisión para CQ-4204210
* Después de instalar SP1+NPR-11577 v1.2, al elegir “Usar una Métrica de análisis” para la Métrica de objetivo mientras se establece el objetivo en la IU táctil, la lista desplegable de métricas nunca se carga. NPR-16129: revisión para CQ-4204316
* Al utilizar la segmentación, la publicación de la campaña no publica automáticamente todo el árbol, incluidas la marca y la parte principal. NPR-15855: revisión para CQ-94630

### Traducción {#translation-8}

* AEM El trabajo de traducción de sincronización ahora se activa automáticamente y ahora se produce el sondeo de la sin bloquear los proyectos de traducción. NPR-15163: revisión para CQ-90856

### Forms {#forms-17}

#### Paquete de complemento de Forms {#forms-add-on-package-17}

**Formularios adaptables**

* Al guardar un formulario adaptable con un archivo adjunto, la ruta completa del archivo adjunto se agrega en la variable `fileAttachment` del XML generado, en lugar del nombre del archivo adjunto. NPR-16529
* En los formularios adaptables basados en XDP, el contenedor `afData/afBoundData` está presente en el XML enviado, aunque incluso el XML de relleno previo no tenga contenedores `afData/afBoundData`. NPR-16118

* Notación exponencial en el campo Número: cuando se utilizan formularios adaptables, si se introduce un número con una fracción decimal que supera los diez caracteres en total, el número se convierte en notación exponencial en el XML enviado. NPR-16106
* Para los formularios que contienen un componente de archivo adjunto y un fragmento cargado diferido, el xml de datos enviado no contiene la información del componente de archivo adjunto. NPR-16022
* Para un panel repetible con carga diferida que no tiene un antecesor repetible, los elementos secundarios repetitivos dentro de una segunda instancia del panel no se pueden repetir. NPR-15944
* Al intentar guardar un fragmento dentro de un fragmento en el editor de formularios, la raíz del modelo de fragmento no rellena el valor del fragmento secundario. NPR-15943
* Al crear una casilla de verificación con un solo elemento e intentar mostrar el título de la casilla de verificación manteniendo el título del elemento oculto, la acción Crear diccionario emite un `ArrayIndexOutOfBoundException` si el texto del elemento está vacío. El diccionario no se crea y no se genera ninguna respuesta de error en la pantalla. NPR-15816
* Para los formularios adaptables con widgets de archivos adjuntos, algunas partes del formulario se deshabilitan después de previsualizar el archivo adjunto.
NPR: 16611

* En el caso de los widgets de archivos adjuntos que permiten varios adjuntos, al enviar una nueva instancia de formulario con un adjunto en un widget que ya tiene un adjunto anterior, se muestra un código de error. Este error se produce al abrir el archivo adjunto agregado en lugar del contenido real. NPR-16258
* La seguridad del servicio de formularios permite rellenar automáticamente el servicio de acceso no autorizado a través de protocolos como `file://`, `http://` y `ftp://`. Consulte [Configurar el servicio de relleno previo mediante Configuration Manager](https://experienceleague.adobe.com/es_es/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15414

* Solicitud para procesar el formulario adaptable en formato de PDF en lugar de HTML en el paso de verificación y anexar todos los archivos adjuntos al PDF, de modo que la impresión muestre el formulario completo. NPR-9011

**Administración de correspondencia**

* Mientras se trabaja con fragmento de texto en una carta en modo Vista previa o Editar, si el texto se convierte en lista, se interrumpe toda la funcionalidad de la carta. Además, se genera un error de JavaScript. NPR-16460
* La importación de un archivo XSD para crear un diccionario de datos en el nodo Administración de correspondencia falla cuando el explorador no responde cada vez que se carga el XSD y se selecciona el nodo raíz. Este problema es independiente del explorador y no aparece en los registros del servidor. NPR-16452
* Al obtener una vista previa de una carta con el navegador Internet Explorer y al intentar editar el tamaño de fuente del contenido, los valores de duplicado se ven desde 8 a 72 en la lista desplegable de tamaño de fuente. NPR-16387
* Si un campo flotante aparece como un campo de entrada desde un fragmento XDP, el campo no se expande en la vista previa de la carta mientras se utiliza el explorador Internet Explorer. NPR-16367
* Al intentar enviar una carta directamente desde la previsualización, la ventana emergente del nombre de la carta no se muestra correctamente debido a que está oculta. NPR-16353
* Los espacios de línea agregados al editar una carta no se reflejan en la ventana de Previsualización. Para listas en fragmentos de texto, la salida PDF no muestra el espaciado correcto. NPR-16267
* Al trabajar en un fragmento de documento de texto con el explorador Internet Explorer, al intentar proporcionar sangría al texto se produce un error, ya que el cursor no permite la sangría del texto. NPR-16128
* Añadir o modificar un diccionario de datos en un fragmento de documento de texto existente lleva mucho tiempo y no siempre se notifica al usuario. NPR-16102
* Al obtener una vista previa de una carta con contenido desplazable mediante el explorador Internet Explorer, la barra de desplazamiento del explorador se superpone con la barra de desplazamiento de la carta. Como tal, no se puede ver todo el contenido de los fragmentos del lado derecho. NPR-16068
* Al crear o editar fragmentos de documento de texto con el navegador Google Chrome, la lista desplegable de selección de color aparece automáticamente y no se puede eliminar. El usuario debe seleccionar lista como tipo de entrada de datos para poder editar el fragmento. NPR-16067
* Al utilizar la API `Letterinstance`, el método `import com.adobe.icc.services.api.LetterInstanceService` no funciona. NPR-16008
* Cambiar los formatos de visualización de fecha a `locale=en_US; dateFormat=MMM dd,yyyy;` en la Configuración del compositor de recursos no funciona de la forma esperada y el formato de fecha se muestra como caracteres no deseados. NPR-16007
* El tipo de vinculación de datos en cartas mientras se vuelve a crear se muestra como &quot;Usuario&quot; aunque se haya configurado de forma diferente anteriormente. NPR-16619

**Forms Portal**

* Los escenarios de actualización para los componentes de borrador y envío no funcionan con la implementación de muestra de base de datos. NPR: 16752

**Servicio de Forms con códigos de barras (BCF)**

* El análisis de código estático del Servicio de Forms con códigos de barras (BCF) informa de problemas. NPR-13855

#### Instalador JEE de Forms {#forms-jee-installer-17}

**Administración de procesos - Espacio de trabajo HTML**

* La seguridad del servicio de formularios permite rellenar automáticamente el servicio de acceso no autorizado a través de protocolos como &quot;file://&quot;, &quot;http://&quot; y &quot;ftp://&quot;. Para obtener más información, consulte la [Configurar el servicio de relleno previo mediante Configuration Manager](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15434

**Administración de usuarios**

* La pantalla de inicio de sesión de SAML muestra una versión incorrecta (6.1.0) en el servidor AEM 6.2. NPR-13825
* Con AEM Forms configurado para la autenticación de Inicio de sesión único (Kerberos), si la autenticación falla al intentar iniciar sesión, se devuelve el código de error “404”. El usuario se redirige al sitio de inicio de sesión solo después de actualizar la página. NPR-15015

#### Forms Designer {#forms-designer-1}

* Cambiar la configuración regional del formulario a francés (Canadá) en la revisión ortográfica del diccionario no funciona en AEM Forms Designer.
NPR-15896

### Paquetes de funciones incluidos en CFP3 {#feature-packs-included-in-cfp-2}

**Paquete de complemento de Forms**

* Al eliminar cualquier recurso en Administración de correspondencia, se debe registrar un mensaje de advertencia en el archivo error.log. NPR-13225
* Mejore la funcionalidad de búsqueda mientras previsualiza una carta en Administración de correspondencia para habilitar la búsqueda de texto en el contenido del fragmento de texto, en lugar de buscar únicamente el título o la etiqueta de la carta. NPR-16103

### Paquetes OSGi incluidos en CFP3 {#osgi-bundles-included-in-cfp-5}

Lista de paquetes OSGi actualizados entre AEM 6.2 SP1 y CFP3

[Obtener archivo](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt).
Los aspectos destacados del paquete de correcciones acumulativas 2 son:

* AEM Correcciones de estabilidad y mejoras de rendimiento en la plataforma de, incluido el marco de trabajo y las operaciones de Sling
* Se ha mejorado la administración de recursos con varias correcciones para acceder, mover, buscar, cargar y publicar recursos
* Creación y administración mejoradas de sitios con correcciones en Fragmentos de contenido, Complementos de anclaje, Proyecciones de diapositivas y componentes de Context Hub
* Varias correcciones en la IU táctil, incluyendo el editor de texto, Omnisearch y el proceso de creación de variantes
* Se han mejorado los flujos de trabajo de traducción; se ha mejorado el conector de Microsoft® para usar nuevas API de traducción para el portal de Azure
* Correcciones en Proyectos y Campaign
* Creación y administración mejoradas con correcciones en formularios adaptables, administración de correspondencia y funciones del portal de formularios
* Correcciones en los Formularios principales de JEE, XTG y componentes de espacio de trabajo de HTML

### Plataforma {#platform-14}

* El `SlingPostProcessor` se activa si se edita la página que hace referencia directamente al marco de trabajo de Sling. NPR-15754: revisión para CQ-104153

* El valor de las etiquetas con `tagBasePath` La propiedad no se obtiene en el cuadro de diálogo IU clásica al desplazarse a un componente de página. NPR-15543: revisión para CQ-4199950

* Mientras realiza operaciones Sling, cuando tiene un fragmento llamado “chunk_n_n-1” `SlingFileUpload handler.getLastChunk` se ejecuta en un bucle interminable con fragmentos vacíos. NPR-15455: revisión para SLING-5701

* Cuando una interfaz amplía otra interfaz, los métodos inyectables en la superinterfaz no se insertan correctamente. NPR-15202: revisión para SLING- 5710
* No se impide una posible excepción de puntero nulo al utilizar la llamada a la función `com.adobe.granite.infocollector.impl.FilesTraversal`. NPR-15169 revisión para CQ-4197640
* El estado del flujo de trabajo no es coherente para algunos nodos secundarios y se muestra un error al enviar eventos de observación para ese nodo. NPR-15701: revisión para GRANITE-13786
* Un usuario selecciona un nodo en CRXDE (por ejemplo, `/content/dam/`). A continuación, hace clic en la ficha &#39;Control de acceso&#39;, asegurándose de que existe una Lista de control de acceso. Ahora, al arrastrar y soltar algunos elementos, se mueven los elementos, no el seleccionado. NPR-15696 revisión para GRANITE-16300
* Si se selecciona un usuario en la lista desplegable cuando se intenta suplantar, la ventana emergente del usuario desaparecerá. NPR-15774: revisión para CQ-4201738/GRANITE-11895
* En Omnisearch, la búsqueda por etiquetas con sugerencias rellenadas automáticamente no funciona. NPR-15088: revisión para GRANITE-14426.
Nota: Esta corrección requiere el Oak CFP 1.4.11 o superior.

### Mobile AEM Author {#mobile-aem-author}

* Al utilizar paquetes de AEM Mobile y ContentSync con una aplicación híbrida, AEM responde a una solicitud de captura (con marcas de hora) realizada por la aplicación con el paquete más antiguo, en lugar del solicitado por la aplicación. NPR-15749: revisión para CQ-104153

### Sites {#sites-17}

* El estado de modificación de la bandeja de entrada de flujo de trabajo en el WCM principal no cambia si un usuario modifica una página después de activar un flujo de trabajo. NPR-15684: revisión para CQ-4196974
* El complemento Anclaje del Editor de texto enriquecido para la IU táctil genera HTML5 no compatible cuando el usuario hace clic en el icono de anclaje y agrega un nombre. Debe agregar un atributo “id” en lugar del atributo “name” en la etiqueta HTML5 para el elemento de anclaje. NPR-15650: revisión para CQ-89782
* Cuando se crea un esquema de metadatos con numerosos campos y se aplica a los metadatos del fragmento de contenido, no se crea ninguna barra de desplazamiento en la pantalla de metadatos del fragmento de contenido, por lo que los campos no se pueden editar. NPR-15478: revisión para CQ-4202622
* La edición del componente de campo `TagInput` no muestra los valores configurados anteriormente en los campos del cuadro de diálogo. NPR-15464: revisión para CQ-4200360

* En la IU del editor de Fragmentos de contenido, cuando se crean variaciones de un Fragmento de contenido, el panel lateral no muestra la barra de desplazamiento para desplazarse por todas las variaciones. NPR-15445: revisión para CQ-4199444
* Cuando los usuarios se eliminan de los grupos directos, se agregan a los grupos heredados. NPR-15400: revisión para CQ-98758
* Creación de WCM: El autor de la IU táctil no permite la edición de páginas que tienen comas en el nombre. NPR-15396: revisión para CQ-4199723
* Al utilizar la IU táctil para la creación, la función `Granite.author.editableHelper.doSelectParent` pasa argumentos en un orden incorrecto que provoca un error de JavaScript. NPR-15349: revisión para CQ-4198594
* El segmento de ContextHub muestra la experiencia incluso si la cookie de exclusión está presente. NPR-15293: revisión para CQ-4198024
* El componente Presentación de diapositivas de la IU clásica no puede crear diapositivas ni arrastrar y soltar imágenes para crear diapositivas. NPR-15281: revisión para CQ-4194164
* A los usuarios, independientemente del permiso, se les muestran las opciones de “Crear”, como Crear página, Crear sitio, Crear Live Copy, Crear lanzamiento y Crear catálogo, en la Admin Console del sitio. NPR-15278: revisión para CQ-94436
* Después de instalar el paquete de servicio 1 de AEM 6.2, el control deslizante “Incluir subpáginas” deja de funcionar para inicios de página. NPR-15230: revisión para CQ-4198449
* Solicite mejorar la Depuración de versiones para recuperar y procesar versiones en bloques y poder utilizar una ruta especificada en una consulta XPath. NPR-15186: revisión para CQ-109205
* Falta el botón Borrar en la pestaña de miniaturas de las propiedades de página del componente Sitios. NPR-15143 revisión para CQ-4196997
* Para un sitio que utiliza Live Copies, al seleccionar la casilla &quot;Live Copy&quot; en el panel Columnas del Admin Console del sitio, el estado de Live Copy no se muestra correctamente y solo se muestra el marcado del HTML. NPR-15108: revisión para CQ-97086
* Al editar Fragmentos de contenido, si el usuario hace clic en hecho (“√”) para editar antes de obtener la respuesta de la Publicación, el contenido editado no se guarda correctamente. NPR-15014: revisión para CQ-4194095
* Si se cierra la página Editar durante el modo Deformación de tiempo y se intenta volver a abrirla desde el administrador del sitio, se produce un error con el estado `500`. NPR-14965: revisión para CQ-109647:
* En la IU del Digital Asset Manager (DAM), la Búsqueda del selector de usuarios autorizables busca las causas de una excepción “Memoria insuficiente”. NPR: 15307: revisión para CQ-98542

### Recursos {#assets-17}

* Después de buscar un recurso en Omnisearch, seleccione un recurso e intente editar las propiedades haciendo clic en **Ver propiedades** y, a continuación, el **Guardar** redirige a los usuarios a una página en blanco. NPR-15900: revisión para CQ-4202372
* La IU de recursos no responde a eventos. Si selecciona un recurso y hace clic en “Publicar” o “Representaciones”, no se producirá ninguna actividad. NPR-15828: revisión para CQ-4202247
* Al publicar un recurso desde la vista de tarjeta, la tarjeta no se actualiza para reflejar un estado publicado. En su lugar, se actualiza la página. NPR-15826: revisión para CQ-102732
* Revisión acumulativa que contiene Revisiones de recursos. NPR-15225
* Si se incluye un carácter et (&quot;&amp;&quot;) en el nombre de una carpeta de recursos, el nombre de la carpeta no se muestra correctamente al desplazarse al recurso. NPR-15775: revisión para CQ-4201735
* El uso de un carácter et (“&amp;”) en el nombre de un archivo de recurso provoca problemas al acceder a sus propiedades. NPR-15770: revisión para CQ-4201737
* Al navegar por Assets y utilizar el modo de visualización &quot;Vista de columna&quot;, si el usuario actualiza la página después de seleccionar y hacer clic en un recurso, se muestran los detalles del recurso en lugar del contenido actualizado. NPR-15768: revisión para CQ-4201727
* La ingestión de PDS absorbe el 100 % de utilización de CPU con un montón de bibliotecas para servicios PDF. NPR-15606 revisión para GRANITE-12929
* El acceso a la interfaz de usuario de &quot;Mi vínculo compartido&quot; mediante el navegador Firefox no muestra los elementos o usuarios compartidos y la pantalla no se puede utilizar. NPR-15539: revisión para CQ-4200992
* Al utilizar Digital Asset Manager, si una página está asociada a un conjunto de imágenes, al mover las imágenes a una nueva carpeta se interrumpe la asociación de páginas. Como tal, la página asociada omite algunas de las imágenes. NPR-15538: revisión para CQ-111479
* En el componente Dam Viewer, el uso del modo de ejecución “nosamplecontent” provoca errores con los medios dinámicos. NPR-15449: revisión para CQ-4195425
* Al crear perfiles de vídeo, si se elige un ajuste preestablecido de codificación de vídeo de alta calidad y de calidad media, los cambios realizados no se guardan. NPR-15447: revisión para CQ-4195482
* Aunque la carga de un recurso en Brand Portal falla debido a una respuesta de error del servidor, el estado se actualiza a “Publicado” en la IU de Brand Portal, lo que dificulta el seguimiento del archivo perdido. NPR-15442: revisión para CQ-4197968
* Al publicar una carpeta de recursos en Brand Portal, donde la publicación tarda más de una hora, algunos archivos no se pueden publicar. NPR-15441: revisión para CQ-4199493
* Al utilizar la consola de Buscador de recursos en la vista de columnas, al intentar crear una carpeta se produce un error una vez, aunque se logra al reintentar. NPR-15370: revisión para CQ-4199448
* Si un recurso o una carpeta seleccionados en la IU de DAM tiene una coma en el nombre, la pestaña Referencias no está disponible y muestra el mensaje &quot;La lista de referencias no está disponible para varias selecciones&quot;. NPR-15362: revisión para CQ-4199721
* La publicación de una carpeta en Brand Portal no cambia el estado publicado de la carpeta, aunque los recursos de la carpeta se hayan publicado correctamente. NPR-15292: revisión para CQ-4197667
* Durante la navegación a la consola Recursos en la IU táctil, se muestra una excepción al activar determinados recursos. NPR-15217: revisión para CQ-108779
* Publicación de un vídeo en YouTube cuando la conexión se realiza a través de un servidor proxy. NPR-15109: revisión para CQ-110332
* Uso de un recurso con un nombre que contenga un punto (.) en data-sly-resource no se resuelve en el mismo recurso y la ruta de salida termina en el punto. NPR-15069: revisión para CQ-4195914
* Tras actualizar AEM 6.2 al Service Pack 1, se produce un error en la sincronización de recursos en Scene7. La propiedad `dam:Scene7FileStatus` muestra el estado `UploadFailed` incluso para los recursos publicados. NPR-15269: revisión para CQ-4197708

### Interfaz de usuario {#user-interface-5}

* Entrada **[!UICONTROL IU táctil]**, la fecha guardada se muestra para los campos de fecha que ahora tienen type=&#39;datetime&#39; mientras se usa el explorador Internet Chrome versión 56.0.2924.87. NPR-15383: revisión para GRANITE-16481
* En **[!UICONTROL IU táctil]**, el Editor de texto enriquecido elimina el subproceso y los elementos de rótulo de las tablas HTML mientras los procesa. NPR-15267: revisión para CRTE-41
* `FileUpload Validator` no gestiona casos en los que el inicio automático es verdadero o cuando `uploadFile()` se solicita manualmente y genera un informe de validación no válido en estos casos. NPR-15295: revisión para GRANITE-13499

* Omnisearch no permite que los clientes utilicen `/apps` para agregar una fuente de datos de columna, ya que supone que la configuración de ubicación se enumera en */libs/granite/omnisearch/content/metadata/*. NPR-13188 revisión para GRANITE-16479
* Al utilizar la **[!UICONTROL IU táctil]**, las variantes de producto no se crean al mismo nivel que el producto. El usuario no está informado del estado del proceso de creación de variante. NPR-15345: revisión para CQ-4198948

**Scene7**

* La ejecución del flujo de trabajo de Scene7 da como resultado archivos abiertos que no se cierran. AEM Solicite mejorar el servicio-S7 para que mantenga y reutilice una sola instancia de HttpClient con la configuración de agrupación compartida. NPR-15357: revisión para CQ-109958

### Traducción {#translation-9}

* Al utilizar proyectos de traducción, la actualización de copias de idioma del idioma principal al inglés produce 11 lanzamientos independientes con el mismo nombre y la misma raíz de origen. Sin embargo, cada una tiene raíces de lanzamiento ligeramente diferentes, en caso de que el nombre de página siga un patrón definido. NPR-15605: revisión para CQ-4200699
* Los proyectos de traducción no se crean para páginas cuando las raíces del idioma tienen guiones y saltos en el nombre. NPR-15171: revisión para CQ-96286
* Solicitud de actualización del conector de Microsoft® para poder utilizar las API de Microsoft® Translator, que Microsoft® pone a disposición en el portal de Azure. NPR-15320: revisión para CQ-101010

### Proyectos {#projects-4}

* Solo 20 proyectos inactivos están visibles en la pantalla Proyectos, aunque existen más de 20 proyectos inactivos en el repositorio. NPR-15656: revisión para CQ-4200903

### Campaign {#campaign-1}

* Al utilizar la campaña: Segmentación y `MAC` : componentes de integración de Test and Target, la anulación de la publicación de actividades no actualiza el estado de actividad en la IU principal. NPR-15401: revisión para CQ-4199839
* Al mover un producto en AEM Commerce, el Asistente para mover el producto omite los valores precargados para el nombre del producto, el título, las páginas a las que se hace referencia, la creación del autor y la fecha de creación. NPR-15228: revisión para CQ-98617

### Seguridad {#security-4}

* Se ha agregado un parámetro de token CSRF a los formularios con un método de GET. NPR-15229

### Forms {#forms-18}

#### Paquete de complemento de Forms {#forms-add-on-package-18}

`**Adaptive Forms**`

* Los valores predeterminados se sustituyen por valores vacíos en xml al rellenar previamente el Formulario adaptable con XML de entrada. NPR-15721
* El `afData/afBoundData` El contenedor está presente en el XML enviado, aunque incluso el XML rellenado previamente no tenga `afData/afBoundData` contenedor en formularios adaptables basados en esquemas XML. NPR-15541

* Los títulos de la Barra de acordeón deben ser encabezados HTML “h2” editables en lugar de la etiqueta “a”. NPR-15475
* La presentación de acordeón de un panel de formulario no es accesible para los usuarios del lector de pantalla. Los usuarios no pueden desplazarse a la pestaña acordeón solo desde el teclado mediante un software de lector de pantalla como JAWS o NVDA. NPR-15474

`**Correspondence Management**`

* Guardar, eliminar y establecer referencias para un fragmento de documento requiere mucho tiempo. NPR-15939
* Alineación de tabulación definida en Administrar recursos en texto que contiene varios Saltos de encabezado en la IU de CCR. NPR-15818
* Las miniaturas de los Módulos de texto no muestran el contenido alineado, aunque el texto contiene contenido alineado creado con pestañas en Google Chrome. NPR-15819

`**Forms Portal**`

* El servicio de relleno previo no funciona para XDP Forms. NPR-15466
* Al almacenar los borradores de los formularios adaptables y los envíos a la base de datos, el estado del formulario adaptable se daña cuando la conectividad de la base de datos falla por cualquier motivo (por ejemplo, después de un largo tiempo de inactividad). NPR-15297

#### Instalador JEE de Forms {#forms-jee-installer-18}

`**Core**`

* Después de actualizar a la versión más reciente de Java™ 1.8.0_121-b13, la Interfaz de usuario del administrador no es accesible en AEM Forms. NPR-15330

`**XTG**`

* Al utilizar el servicio Output para combinar un formulario específico con un dataxml, el tiempo de respuesta es 20 veces mayor que el tiempo que tarda un servidor ES4 SP1. NPR-15283

#### Aplicación de AEM Forms {#aem-forms-app-1}

* Al recuperar tareas no guardadas, el mensaje que se muestra debe ser más claro para reducir el error del usuario. NPR-15377
* La aplicación de AEM Forms no procesa formularios creados a partir de plantillas personalizadas. NPR-15892
* Los usuarios no pueden iniciar sesión en la aplicación de AEM Forms. NPR-15891

Los aspectos destacados de AEM 6.2 SP2-CFP1 son:

* Optimiza la funcionalidad de replicación en Sites:

* Correcciones en varios Despliegues, LiveCopy y versiones de escritura erróneas

* Mejora la capacidad de respuesta de la IU táctil durante:

* Búsquedas de recursos
* clasificación basada en el tamaño

* Mejora la administración de etiquetas en colecciones inteligentes
* Controles de acceso más estrictos durante las operaciones de CRUD en carpetas

### Plataforma {#previous}

* Solicitud de eliminación de llamadas `ReplicationQueue#forceRetry` de API durante el inicio de los agentes de replicación porque dichas llamadas ralentizan considerablemente la instancia, especialmente cuando tiene muchos agentes de replicación. NPR-14032: revisión para GRANITE-13095
* Se solicita que la configuración de OSGi `DurboImportConfigurationProviderService` admita campos que puedan almacenar una matriz de valores. NPR-14570: revisión para CQ-108684
* El uso del componente Sightly en una página después de migrar a AEM 6.2 hace que el cuadro de diálogo Propiedades de la página deje de funcionar. NPR-14328: revisión para CQ-108355
* Al cancelar la programación de un trabajo programado anteriormente, no se elimina el nodo correspondiente por debajo de */var/eventing/schedule-job*. NPR-14253: revisión para SLING-5666
* Cuando un administrador intenta suplantar a un usuario eliminado, la interfaz de usuario no se actualiza. NPR-14247: revisión para CQ-107446
* La comprobación de la protección XSS produce una codificación incorrecta en el componente Sightly. NPR-14004: revisión para CQ-93821
* Solicite actualizar Jackrabbit File vault a 3.1.30 para resolver varios problemas. NPR-13454
* El error de caché se produce cuando Sling Distribution sincroniza los paquetes de distribución del autor a la publicación. NPR-13034: revisión para GRANITE-13970

### Sites {#sites-18}

* Problemas con VersionManagerImpl que purgan versiones incorrectas del historial de versiones. NPR-14372
* El componente Slightly Foundation Parsys de WCM ignora los nombres de etiquetas de declaración de componentes, `cq:htmlTag / cq:tagName`. NPR-14225
* Cuando se utiliza Sightly Parsys para procesar los componentes insertados mediante JavaScript en la IU táctil, la decoración personalizada se omite después de actualizar la página. NPR-14122
* Las listas desplegables de destino no funcionan en el cuadro de diálogo IU táctil cuando se crean varios campos de texto enriquecido, como vínculos. NPR-13911
* Al editar un campo de texto con varias propiedades del Editor de texto enriquecido (RTE) en un cuadro de diálogo (IU táctil), el enfoque cambia aleatoriamente a una propiedad RTE específica. NPR-13703
* El componente de vídeo predeterminado no procesa la miniatura de vídeo. NPR-14976
* La información se carga lentamente en la pestaña Live Usages del Editor de plantillas. NPR-14880: revisión para CQ-83417
* AEM La instalación de la revisión 10936 en una instancia de 6.2 deshabilita el componente Iparsys. NPR-14330: revisión para CQ-106982
* Varios problemas de componentes de Despliegue y un problema con Live Copy tras la migración a AEM 6.1 SP1. NPR-15256
* La acción Despliegue de página no puede crear elementos secundarios más allá del primer nivel, incluso para varias configuraciones de Despliegue. NPR-15055
* Al enviar el cuadro de diálogo Propiedades de página desde el Editor, se vuelven a escribir los datos sin modificar en las pestañas de LiveCopy. NPR-14693
* Cuando se envía el cuadro de diálogo Propiedades de página desde el Editor, el MSM Post Processor escribe algunos parámetros de la solicitud en lugar de los `msm:writeLiveCopyConfig` parámetro. NPR-14434
* Varios problemas relacionados con el componente de Despliegue, Live Copies y otros aspectos de MSM. NPR-12235

### Recursos {#assets-18}

* El flujo de trabajo de desempaquetado no puede gestionar imágenes con caracteres especiales en el nombre del archivo de imagen. NPR-15227: revisión para CQ-103887
* Los recursos que tienen la expresión Repetir con Condición no se muestran correctamente. Cuando el usuario previsualiza la plantilla de carta `*CDN3835RLCEN*`, no se muestra ningún recurso ubicado en el Área del cuerpo de destino. En el caso de los widgets de archivos adjuntos que permiten varios adjuntos, al enviar una nueva instancia de formulario con un adjunto en un widget que ya tiene un adjunto anterior, se muestra un código de error. NPR-14844

* Al crear una colección inteligente, la etiqueta de estilo no se conserva cuando se guarda la colección inteligente. NPR-15081: revisión para CQ-4195494
* Consultas de búsqueda de recursos que se ejecutan lentamente en la IU táctil durante búsquedas simultáneas de varios usuarios. NPR-15019: revisión para CQ-4195405
* Los metadatos extraídos para una propiedad de tipo `Long[]` se convierten en tipo `String[]` cuando el recurso original se vuelve a cargar en una ubicación diferente. NPR-15016: revisión de CQ-4195005

* Los usuarios no pueden eliminar una búsqueda guardada o una colección inteligente. NPR-14924: revisión para CQ-108494
* La edición masiva de metadatos para recursos (modo de anexado) mientras se utiliza un valor Booleano para TypeHint en un campo desplegable en el esquema de metadatos subyacente produce un error. NPR-14529: revisión para CQ-106876
* Los usuarios con derechos de Replicación ahora pueden eliminar carpetas de Recursos. NPR-14321: revisión para CQ-88271
* Al intentar editar los perfiles de vídeo para un vídeo en el Editor de Canales, el cuadro de diálogo de diseño no se abre y genera una excepción de puntero nulo en el registro de errores. NPR-14144: revisión para CQ-81101
* La propiedad de marca de tiempo &quot;Creada&quot; generada por el sistema que se muestra en la página de propiedades de un recurso es incorrecta. NPR-13992: revisión para CQ-95029
* Solicitud para habilitar la detección de recursos de duplicados para usuarios sin acceso de Lectura en AEM Assets NPR-13851: revisión para CQ-102281
* Los usuarios no pueden editar los metadatos de los recursos de forma masiva desde la página de propiedades. NPR-13721: revisión para CQ-100703
* Mensaje de error incorrecto en la IU clásica cuando se carga un recurso de duplicado. El mensaje de error no indica por qué falló la carga. NPR-13691: revisión para CQ-99272
* AEM Assets no puede ordenar más de 50 recursos por tamaño a la vez en la vista de Listas cuando esta contiene numerosos recursos. CQ-100588
* Si se seleccionan varios recursos, se produce un error con el Código de respuesta 414 (Solicitar URI demasiado largo) si el URI de recurso o carpeta es demasiado largo. NPR-13516: revisión para CQ-76076
* La página Informe de recursos deja de responder cuando el usuario selecciona todas las opciones en el cuadro de diálogo `Configure Columns`. NPR-13187: revisión para CQ-95589
* Comportamiento inesperado del selector de etiquetas en Safari e Internet Explorer. NPR-13134
* La edición de búsquedas guardadas desde el carril de Búsqueda de administración de recursos permite guardarlas como selecciones inteligentes anidadas, lo que provoca problemas de estabilidad en el entorno. NPR-13119: revisión para CQ-99460
* Tras mover un archivo (o carpeta) y cambiarle el nombre, los metadatos `cq:name` no reflejan el nuevo nombre de archivo (nombre de carpeta). NPR-13036: revisión para CQ-99141
* El recurso con nombres que incluyen caracteres especiales no se puede descargar del vínculo de descarga compartido por correo electrónico. NPR-12872: revisión para CQ-95795
* Los informes de Recursos predeterminados que se generan cuando hay un número sustancial de recursos provocan grandes recorridos donde la búsqueda no alcanza ningún índice y picos de uso de CPU. NPR-12811: revisión para CQ-84409
* Los usuarios de AMS pueden acceder a la instancia de autor de AEM Assets desde redes distintas, no se pueden cargar recursos mediante la carga de fragmentos sin privilegios de eliminación en carpetas. NPR-12768: revisión para CQ-82715
* En las búsquedas basadas en etiquetas de recursos que utilizan el carril de Búsqueda de recursos, la función Tipo delante no se limita a la ruta raíz y muestra las etiquetas de todas las áreas de nombres. NPR-12666
* El componente StaticRenditions genera una excepción de puntero nulo. NPR-12665
* Solicitud para deshabilitar MissingMetadataNotificationJob porque hace que la IU de Notificación de distintivos rompa la página con una excepción de tiempo de ejecución “No se puede analizar la entrada”. NPR-12500: revisión para CQ-93573
* La opción “Deshabilitar edición” para un campo de etiqueta no funciona en las páginas de propiedades de recursos en la IU táctil. NPR-12429: revisión para CQ-88835
* Correcciones de API en AEM Assets 6.2 para la implementación Companion App SMB. NPR-11099
* Dado que la variable `Jquery` , los usuarios no podrán seleccionar una colección de recursos y confirmar la selección en el panel Asociar contenido de un fragmento de contenido. NPR-14847: Backport para CQ-4194209
* A pesar de invocar la ordenación infinita en el lado del cliente, solo se ordenan los artículos, banners y colecciones que se muestran actualmente en la IU. NPR-14493: revisión para CQ-109926
* Solicitud para implementar la función Omnisearch para el servicio Mobile On-Demand de AEM. La búsqueda de palabras clave para cualquier artículo, colección o banner no devuelve ninguna coincidencia. NPR-14093: revisión para CQ-101394
* Cuando se utiliza el componente coral-select (*granite/ui/components/coral/foundation/form/select*) en un cuadro de diálogo, la inicialización de valores no funciona correctamente en Internet Explorer (exploradores IE11 o Edge) cuando el valor seleccionado contiene un solo elemento. NPR-13395: revisión para CQ-101013

### Proyectos {#projects-5}

* Al exportar un proyecto de traducción creado con el Método de traducción como &quot;humano&quot; y el proveedor de traducción como &quot;ninguno&quot;, no se genera ningún archivo ranslation_export_summary.xml porque falta el archivo de asignación GUID. NPR-13137: revisión para CQ-91976
* En Proyectos AEM, al crear un proyecto con la propiedad de fecha de vencimiento establecida, la conversión de fecha establece la hora de forma incorrecta debido a la diferencia de huso horario entre el servidor y el cliente. NPR-13003: revisión para CQ-98288
* La opción “Mostrar en sitios” se pierde del trabajo de traducción cuando se actualiza un proyecto de traducción. NPR-12966: revisión para CQ-93740
* Cuando se crea un proyecto de traducción para una página de sitio exportada, no se representa correctamente en la previsualización. NPR-12964: revisión para CQ-84627

### Flujo de trabajo {#workflow-3}

* El vínculo de carga útil de la pestaña Archivo de la consola Flujo de trabajo devuelve un error con el código de respuesta &quot;404&quot; al hacer clic en él. NPR-14993: revisión para CQ-4194977
* Cuando se utilizan flujos de trabajo predeterminados de AEM, CQ Mailer no envía una notificación por correo electrónico al grupo que omite la dirección de correo electrónico de un solo miembro. NPR-14804: Solicitud de revisión para CQ-91499
* Mejoras de rendimiento para la bandeja de entrada y el distintivo de notificación en la IU táctil. NPR-14145: revisión para CQ-101125
* Los usuarios no pueden previsualizar la carga útil desde la consola Bandeja de entrada de flujo de trabajo al iniciar flujos de trabajo. NPR-13226: revisión para CQ-100275
* La cookie &quot;saml_request_path&quot; configurada mediante el Controlador de autenticación SAML muestra la cookie configurada con un `?` carácter. Además, cuando se vuelve a publicar una respuesta SAML en AEM, la cookie de AEM &#39;saml_request_path&#39; devuelve un valor no válido debido a caracteres ya codificados. NPR-13517: revisión proactiva para GRANITE-11722 y GRANITE-14414

### Dynamic Media {#dynamic-media}

* Numerosos trabajos de Sling de `AEM-Scene7` que se crearon y cancelaron durante la activación de AEM se registran como trabajos de archivado durante la replicación. NPR-12835: revisión para CQ-86115

### Seguridad {#security-5}

* Solicitud para resolver el problema de validación de entrada en el filtro WCMDebug. NPR-12444: Solicitud de revisión para CQ-94890
* Solicitud proactiva para corregir el comportamiento de XSS al utilizar el Asistente para crear lanzamiento.
NPR-13062: Solicitud de revisión para CQ-99577

#### Paquete de complemento de Forms {#forms-add-on-package-19}

`Adaptive Forms`

* Al crear un panel repetible con formularios adaptables, el título del panel no se puede actualizar en el tiempo de ejecución. NPR-15325
* Si establece un valor predeterminado para un botón de opción y selecciona un valor diferente durante el guardado o el envío, el relleno previo no muestra el valor seleccionado. NPR-15304
* Google Chrome muestra un comportamiento incorrecto al utilizar el evento de opciones para rellenar dinámicamente la lista desplegable y enviar el valor del elemento seleccionado. NPR-15198
* Al crear un panel repetible con formularios adaptables, el título del panel no se puede actualizar en el tiempo de ejecución. NPR-15181
* Cuando se utiliza el modo de edición para formularios adaptables, se detectan errores de JavaScript como - &quot;El controlador del componente no es válido&quot; y &quot;la guía no está definida&quot;. NPR-15112
* El fragmento de Carga diferida dentro de un panel repetitivo no funciona correctamente. NPR-13916, NPR-14785

`Correspondence Management`

* Los recursos de Administración de correspondencia con expresión `'Repeat with condition'` establecida no se muestran correctamente. NPR-14844
* Al buscar un recurso de Administración de correspondencia (como una carta, un fragmento de documento o cualquier otro tipo), el icono de la cola de descarga no aparece en la barra de herramientas. NPR-14745
* Al crear un módulo de Lista, no funciona el alternado de las propiedades específicas del recurso (como editable y obligatorio). NPR-14689
* El panel Elementos de datos de la utilidad Generador de expresiones se sigue cargando en caso de que se cree un módulo de condición sin seleccionar un diccionario de datos. NPR-14688
* Al obtener una vista previa de una carta, los usuarios no pueden utilizar espacios de tabulación para alinear el contenido en formato de tabla. NPR-14481
* Al exportar recursos de Administración de correspondencia de forma masiva desde la interfaz de usuario, el servidor de AEM Forms genera registros innecesarios. NPR-15226
* Cuando se obtiene una vista previa de una carta, el texto justificado aparece en una fuente diferente. NPR-15468

`**Forms Portal**`

* Los archivos adjuntos de los formularios enviados en el portal de Forms no son visibles cuando se envía un nuevo borrador del envío al portal. NPR-13515

`**Forms Manager**`

* Mientras navega por el *Formularios y documentos* , el botón Pegar no se muestra cuando el usuario copia cualquier recurso y luego navega a una carpeta diferente. CQ-111327

#### Instalador JEE de Forms {#forms-jee-installer-19}

`Rights Management`

* El evento de auditoría relacionado con el inicio de sesión del usuario se registra con una hora no válida. No se puede rastrear la hora correcta para un evento de auditoría. NPR-13107
* Adobe Acrobat Reader y Microsoft® Office no pueden abrir documentos protegidos con autenticación ampliada. NPR-14482

`Process Management`

* Cuando se devuelve una tarea de borrador reenviada al usuario inicial en HTML Workspace, la tarea no aparece en la cola del usuario inicial. NPR-15178

`Assembler Service`

* AEM Forms no puede validar un PDF/A-2b con más de dos firmas. NPR-14101

`XTG`

* Al imprimir un documento con una bandeja de derivación de impresora, la función `GeneratePrintedOutput` no permite recuperar papel de la bandeja de derivación derecha. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer se bloquea cuando el usuario ejecuta la utilidad revisión de ortografía con el Formulario local seleccionado como francés (Canadá). NPR-13740
* Forms Designer se bloquea cuando el usuario selecciona calcular evento o validar evento para un campo de formulario y cambia el lenguaje a JavaScript e introduce `this.` en la ventana **[!UICONTROL Editor de secuencias de comandos]**. NPR-12974

### Paquetes de funciones incluidos en CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Paquete de complemento de Forms):

* Cuando se crea un formulario adaptable a partir de un archivo XDP, la tabulación para accesibilidad no sigue un patrón definido. NPR-12562

`Adaptive forms` (Paquete de complemento de Forms):

* El generador de reglas para formularios adaptables no da acceso basado en funciones. Los cambios realizados por un autor no se pueden rastrear. NPR-12840

`Core` (Instalador JEE de Forms):

* La funcionalidad del uso compartido de recursos de origen cruzado (CoreCross Origin Resource Sharing, CORS) como filtro servlet no está habilitada para JBoss®+.  NPR-13050

## Descargar instrucciones para CFP mediante distribución de software {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Para los clientes de AEM Forms AEM AEM, es esencial instalar el paquete de complementos de formularios de la aplicación después de instalar cualquier paquete de servicio, paquete acumulativo de servicio o paquete de funciones de la aplicación de la aplicación de la aplicación de la manera más adecuada.

Puede descargar el paquete CFP directamente desde la Distribución de software o realizar los siguientes pasos:

1. Abra [Distribución de software](https://experience.adobe.com/downloads). Necesitará un Adobe ID para iniciar sesión en la distribución de software.
1. Pulse **[!UICONTROL Adobe Experience Manager]**, disponible en el menú del encabezado.
1. Pulse el nombre del paquete, seleccione **[!UICONTROL Aceptar términos del EULA]** y pulse **[!UICONTROL Descargar]**.

## Instrucciones de instalación para el CFP {#installation-instructions-for-cfp}

Esta sección es una guía de los requisitos y pasos para instalar el CFP.

### Antes de realizar la instalación {#before-you-install}

>[!NOTE]
>
>Los paquetes de funciones opcionales proporcionados por Adobe dependen de la versión de la versión y del paquete de correcciones acumulativas. Si tiene instalado algún Feature Pack, póngase en contacto con el [equipo del Servicio de atención al cliente de AEM](https://experienceleague.adobe.com/?support-solution=General#support) para validar la compatibilidad con este Fix pack acumulativo para AEM 6.2.

>[!NOTE]
>
>Se recomienda ejecutar la validación en todos los paquetes de instalación nuevos antes de intentar instalar el paquete. La prevalidación analiza e informa de los errores encontrados antes de la instalación y avisa a los usuarios de dichos errores, superposiciones y permisos de forma proactiva.
>

* El Paquete de servicio 1 de AEM 6.2 es un requisito previo para el CFP. Para obtener instrucciones de instalación, consulte las notas de la versión de [AEM 6.2 Service Pack 1](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

* La descarga del Fix Pack acumulativo está disponible en [Distribución de software](https://experience.adobe.com/#/downloads/content/software-distribution/es/aem.html), a la que puede acceder directamente desde la instancia de AEM.
* Para una implementación de clúster mediante (RDBMK o MongoDB), el paquete CFP se puede instalar en cualquiera de las instancias de creación que utilizan el Administrador de paquetes.

* AEM Antes de instalar el paquete de correcciones acumulativas, asegúrese de tomar una instantánea o realizar una copia de seguridad de la instancia de la aplicación de la aplicación de correcciones acumulativas de la que dispone de una instancia de.
* No se admite la desinstalación del CFP.

### Instalación del CFP mediante distribución de software {#install-the-cfp-via-package-share}

Para instalar el Fix Pack acumulativo en una instancia de AEM 6.2 SP1 existente, siga estos pasos:

1. Para descargar el paquete, haga clic en [Distribución de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip).

1. Abra [Administrador de paquetes](http://localhost:4502/crx/packmgr/index.jsp) y haga clic en **[!UICONTROL Cargar paquete]** para cargar el paquete.

1. Seleccione el nombre del paquete y haga clic en **[!UICONTROL Instalar]**.

### Instalación automática {#automatic-installation}

CFP se puede instalar automáticamente en una instancia en ejecución de las siguientes maneras:

* Coloque el paquete en ../crx-quickstart/install mientras se ejecuta el servidor. El paquete se instala automáticamente.
* Utilice la [API de HTTP del Administrador de paquetes](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) (asegúrese de utilizar `cmd=install&recursive=true`) para que se instalen los paquetes anidados.

### Validar la instalación {#validate-installation}

1. La página Información del producto (/system/console/productinfo) debe mostrar ahora la cadena de la versión actualizada “Adobe Experience Manager, Versión 6.2.0.SP1-CFP20” en Productos instalados.
1. Todos los paquetes OSGI tienen el valor ACTIVO o FRAGMENTO en la consola OSGi (utilice la consola web: /system/console/bundles).

>[!NOTE]
>
>Al instalar correctamente el paquete, aparece un mensaje informativo que indica que el paquete de contenido se ha instalado correctamente, como “Paquete de contenido AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 instalado correctamente”.

>[!NOTE]
>
>Desde AEM 6.2 SP1-CFP1, el nivel de registro en Jackrabbit FileVault ha cambiado de INFO a DEPURACIÓN para la mayoría de los mensajes. Para obtener los registros de instalación de un paquete de contenido instalado en AEM 6.2 SP1-CFP1 o posterior, habilite el nivel de registro DEPURACIÓN para `org.apache.jackrabbit.vault.packaging.impl`.

### Instalación de AEM Forms {#install-forms}

>[!NOTE]
>
>Omita este paso si no utiliza AEM Forms.

#### Instale los complementos para AEM Forms {#install-aem-forms-add-on}

>[!NOTE]
>
>(**Únicamente AEM Forms en JEE**) El procedimiento para instalar un CFP en JEE de AEM Forms se describe en [Instalación de CFP en JEE de AEM Forms](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Asegúrese de que ha instalado el paquete CFP de AEM 6.2. SP1.
1. Descargue el paquete de complementos de Forms correspondiente que aparece en las [versiones de AEM Forms](aem-forms-releases.md) para su sistema operativo.
1. Instale el paquete de complementos para Forms tal como se describe en la [instalación de paquetes de complementos para AEM Forms](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

#### Instalación de paquetes JEE de AEM Forms {#install-aem-forms-jee-bundles-package}

Las correcciones en AEM Forms JEE se entregan mediante un instalador independiente. Para obtener información sobre la instalación de un CFP en AEM Forms en JEE, consulte [Instalación del CFP en AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Programa de instalación del diseñador Forms Designer {#designer-installer}

1. Para instalar la actualización, ejecute el archivo Designer 6.2.0_&lt;Language>_Cumulative_QF.msp.
1. En la pantalla de bienvenida, haga clic en **Actualizar**. Se inicia la instalación.
1. Una vez finalizada la instalación, haga clic en **terminar**.

## Parámetros de tiempo de espera configurables por el usuario para conexiones DTM, Analytics y Target {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Con el paquete de correcciones acumulativas 6.2 SP1-CFP7 de AEM y versiones posteriores, los períodos de tiempo de espera de conexión se pueden configurar en todas las conexiones anteriores, según los detalles siguientes:

| **Conexiones** | **Tiempo de espera de conexión&#42;** | **Tiempo de espera de socket&#42;&#42;** |
|---|---|---|
| DTM | 30000 milisegundos | 30000 milisegundos |
| Análisis | 30000 milisegundos | 30000 milisegundos |
| Target | 60000 milisegundos | 30000 milisegundos |

* **Tiempo de espera de conexión&#42;**: tiempo de espera en milisegundos hasta que se establece una conexión. Un valor de tiempo de espera de cero se interpreta como un tiempo de espera infinito.
* **Tiempo de espera de socket&#42;&#42;**: tiempo de espera en milisegundos de espera de datos o un período máximo de inactividad entre dos paquetes de datos consecutivos.

## Deshabilitar el estado de replicación en la consola de etiquetado (IU clásica) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Si utiliza CFP3 o posterior, siga estas instrucciones para deshabilitar el Estado de replicación en la consola de Etiquetado de la IU clásica:

* Superposición *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;* in *`/apps`*

* Añadir `replicationStateRequired`: “false” después de la Línea #416.

```js
415 baseParams: {
416 count: "false",
417 "replicationStateRequired": "false"
418 },
```

## La última actualización 131 de Java™ 8 genera una excepción (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Estas opciones de configuración son específicas para los clientes de AEM Forms que utilizan Document Security.

NPR-21355 está incluido en CFP12.1. Si va a instalar el CFP12.1 o posterior, realice el siguiente procedimiento para configurar NPR-21355 en el servidor de aplicaciones JBoss®. Si va a instalar CFP12.1 en el servidor de AEM Forms que se ejecuta en los servidores de aplicaciones de Oracle WebLogic o IBM® WebSphere, no se requiere ninguna configuración adicional:

1. Haga una copia de seguridad, elimine y cree un archivo module.xml. La ubicación predeterminada del archivo es [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. Abra el archivo module.xml recién creado para editarlo. Añada el siguiente código al archivo:

```xml
<module xmlns="urn:jboss:module:1.1"
name="com.adobe.livecycle">
<resources>
<resource-root path="cryptojcommon.jar"/>
<resource-root path="cryptojce.jar"/>
<resource-root path="jcmFIPS.jar"/>
<resource-root path="certj.jar"/>
<resource-root path="cglib.jar"/>
</resources>
<dependencies>
<module name="javax.api"/>
<module name="asm.asm"/>
</dependencies>
</module>
```

1. Cree una copia de seguridad del `jsafeFIPS.jar`, `jsafeJCEFIPS.jar`, y `certjFIPS.jar` archivos en [AEM_Forms_Installation_directory]`/jboss/modules/system/layers/base/com/adobe/livecycle/main/` y elimine los archivos del directorio mencionado anteriormente.

Póngase en contacto con el [soporte técnico de Adobe](https://experienceleague.adobe.com/?support-solution=General#support) para obtener nuevos archivos JAR. Coloque los archivos JAR obtenidos del [Soporte técnico de Adobe](https://experienceleague.adobe.com/?support-solution=General#support) en [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. (Solo Windows) Modifique los archivos de configuración `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` o `domain.conf.bat`:

* Para el servidor JBoss® en la configuración independiente, abra el archivo standalone.conf.bat para editarlo.
* Para el servidor JBoss® en la configuración de clúster, abra el archivo domain.conf.bat para editarlo.

  Añada las líneas siguientes al final y guarde el archivo:

  Establezca `JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true`

  Establezca `JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE`

1. (Solo SO basado en Linux) Modifique los archivos de configuración [AEM_Forms_Installation_directory]/jboss/standalone.conf o domain.conf

* Para el servidor JBoss® en la configuración independiente, abra el archivo standalone.conf para editarlo.
* Para el servidor JBoss® en la configuración de clúster, abra el archivo domain.conf para editarlo.

  Añada las líneas siguientes al final y guarde el archivo:

  `JAVA_OPTS="$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true"`

  `JAVA_OPTS="$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"`

## Ajustes de configuración necesarios para NPR-19778 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>El NPR-19778 es parte del CFP14.

El recuento de la cola compartida no se actualiza para otros usuarios cuando un usuario solicita una tarea. Como tal, el Adobe ha introducido una nueva propiedad. Siga los pasos a continuación para configurar esta propiedad en la instancia de AEM:

1. Vaya a la IU de Administración -> Services -> Workspace -> Global administration.
1. Exporte la configuración Global.
1. En el archivo XML descargado, agregue la etiqueta `<client_tasksPollingInterval>10</client_tasksPollingInterval>`. Ten es el valor de ejemplo en segundos. Puede modificarlo en consecuencia.
1. Guarde el archivo.
1. Vuelva a la IU de Administración -> Services -> Workspace -> Global administration.
1. Importe el archivo xml en la sección Importar configuración global.
1. Ahora puede cerrar la sesión del sistema y volver a iniciarla.
1. Recuento de inicios de cola compartidos que se actualizan para otros usuarios del espacio de trabajo.
1. Para desactivar la encuesta, cambie el valor a 0 y vuelva a importar el archivo XML.

## Cambios en la IU {#ui-changes}

* Cambio de comportamiento en la visualización de títulos en la tarjeta de imagen para una imagen que tiene la propiedad `dc:title` establecida en String [] (campo múltiple): solo se mostrará el último título modificado en la tarjeta de imagen en la IU, aunque todos los títulos se guardan en CRX. Revisión para CQ-4217165

## Problemas conocidos {#known-issues}

* Al actualizar AEM 6.2SP1-CFP19 y AEM 6.2SP1-CFP20 desde el CFP18, se cambia la redirección de la raíz a la página de bienvenida de la IU clásica en lugar de /sites.html/content. Es posible que tenga que corregir sling: Propiedad de destinatario de /welcome.html a /index.html con el Explorador de CRX. Este problema no se observa al actualizar desde CFP17 o una versión anterior.

Pueden producirse los siguientes errores transitorios al instalar AEM 6.2 SP1-CFPx. Sin embargo, no se requiere ninguna resolución para estos errores porque no afectan a la instancia de AEM y desaparecen después de instalar el CFP:

* Al actualizar AEM instancia 6.2SP1-CFP20 a AEM 6.5, es posible que algunas direcciones URL personales no funcionen como:

* */projects.html*
* */sites.html*

Sin embargo, la solución consiste en reiniciar la instancia de AEM después de una actualización.

* El error interno del servidor HTTP 500 aparece al abrir la página de detalles del componente de la consola web.
* Errores como **crear instancia de componente** y **La fábrica de servicios devolvió un valor nulo** se produce debido al reinicio del repositorio:

* com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Cannot create component instance due to failure to bind reference profileManager
* org.apache.sling.commons.scheduler FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Componente: com.day.cq.tagging.impl.TagGarbageCollector (1687))

* Error detectado en la instalación de CFP en Mongo y DB2®: **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Exception: java.lang.NullPointerException**.  Este error no se producirá después de instalar un CFP sobre CFP8.
* (Tarea de actualización del planificador de mantenimiento de Granite de Adobe) com.adobe.granite.maintenance.impl.TaskScheduler: No se ha encontrado ninguna tarea de mantenimiento con el nombre WorkflowPurgeTask para la ventana `granite:weekly`
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* AEM Al instalar el CFPx en la versión 6.2 SP1 de que incluye el paquete de funciones Etiquetas inteligentes, el paso de flujo de trabajo agregado anteriormente para Smart Tag Assets se elimina del flujo de trabajo de recursos de actualización de DAM.

## Uber Jar {#uber-jar}

Uber Jar para 6.2 SP1-CFP20 está disponible en el repositorio Maven público de Adobe.

Para usar Uber Jar en un proyecto de Maven, incluya la siguiente dependencia en el POM de su proyecto:

```XML
<dependency>
 <groupId>com.adobe.aem</groupId>
 <artifactId>uber-jar</artifactId>
 <version>6.2.SP1-CFP20</version>
 <classifier>apis</classifier>
 <scope>provided</scope>
</dependency>
```

## Paquetes de contenido y paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-5}

Los siguientes documentos de texto enumeran los paquetes OSGI y los paquetes de contenido incluidos en el CFP.

* [Lista de paquetes OSGi incluidos en el SP1-CFP20 de AEM 6.2](assets/do-not-localize/updated.txt)
* [Lista de paquetes de contenido incluidos en el SP1-CFP20 de AEM 6.2](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [Página de correcciones de AEM 6.2](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [Notas de la versión de AEM 6.2 SP1](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [Notas de la versión de AEM 6.2](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [Página de productos AEM](https://business.adobe.com/products/experience-manager/adobe-experience-manager.html?lang=es)
>* [Documentación de AEM 6.2](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [Actualizaciones prioritarias del producto de Adobe](https://experienceleague.adobe.com/en/docs/release-notes/experience-cloud/current)
