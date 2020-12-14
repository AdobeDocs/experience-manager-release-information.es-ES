---
title: Paquete de correcciones acumulativas de AEM 6.2
description: nulo
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '19954'
ht-degree: 19%

---


# Notas de la versión de AEM 6.2 Cumulative Fix Pack{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Información de la versión {#release-information}

| **Producto** | Adobe Experience Manager |
|---|---|
| **Versión** | 6.2 |
| **Versión** | [Paquete de correcciones acumulado 6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **Requisitos previos** | [Paquete de servicio 1 de AEM 6.2](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **Disponibilidad general** | 6 de junio de 2019 |

### Paquete de correcciones acumulativas {#cumulative-fix-pack}

Adobe presentó un modelo de entrega única para la publicación de correcciones. En lugar de lanzar correcciones urgentes para problemas individuales, Adobe ahora publica un paquete de correcciones acumulativas (CFP) todos los meses (sujeto a la aprobación de comprobaciones de calidad). Un CFP es un paquete de contenido agregado para varias correcciones. Los archivos CFP incluyen principalmente correcciones de errores, pero también pueden incluir paquetes de funciones. Tienen las siguientes ventajas con respecto a las versiones de revisiones individuales:

* Carácter acumulativo (por ejemplo, un CFP contiene correcciones enviadas a través de los CFP anteriores)
* Mayor control de calidad
* Instalación simplificada (el usuario instala un CFP como paquete único que no tiene dependencias, excepto el último paquete de servicio)

Para obtener más información sobre el CFP y otros tipos de liberaciones, consulte [Vehículo de versiones de mantenimiento](https://docs.adobe.com/content/docs/en/aem/6-2/deploy/maintenance-release-vehicle-definitions.html).

## Información de la versión {#about-the-release}

AEM paquete de correcciones acumulativas 6.2 SP1-CFP20 es el último paquete de correcciones acumulativas para AEM 6.2 y es una actualización importante que incluye correcciones clave de cliente publicadas tras la disponibilidad general de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

>[!CAUTION]
>
>La aplicación de CFP sin validar la compatibilidad entre los paquetes de funciones instalados puede provocar errores en el sistema o la pérdida de las configuraciones personalizadas, lo que podría necesitar la restauración desde la copia de seguridad.

>[!NOTE]
>
>* Se incluye un nuevo paquete Sling `discovery-  api` Johnzon 1.0.0 con AEM Cumulative Fix Pack 6.2 SP1-CFP10. Además, se agrega un usuario de servicio sling-discover con privilegios de lectura y escritura para el nodo */var/discover* en el repositorio de CRX.
   >
   >
* Se ha agregado un paquete de correo electrónico de apache commons **org.apache.commons/commons-email/1.5** para reemplazar a **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
   >
   >
* Adobe recomienda implementar CFP a través de la carpeta de instalación para los clientes que tengan un gran número de usuarios en AEM instancia.

>



## Problemas incluidos {#issues-included}

Esta sección enumera todos los problemas y revisiones incluidos en la CFP actual.

Además, este CFP incluye revisiones entregadas en [paquetes de correcciones acumulativas anteriores](#previous).

### Integración {#integration}

* Backporting multiple Campaña Targeting, mejoras en la personalización. NPR-29163: revisión para CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler entra en un bucle infinito y provoca actualizaciones en los nodos en instancias de publicación. NPR-28561: revisión para CQ-4263096

### DAM: General {#dam-general}

* No se puede mostrar u ocultar el botón de replicación para usuarios no administradores en carpetas de presas específicas. NPR-29026: revisión para CQ-4265361

###  Vulnerabilidad{#vulnerability}

* El marco de protección CSRF no funciona con los formularios de base de AEM. NPR-28612: revisión para GRANITE-22231

### Forms {#forms}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package}

>[!NOTE]
>
>Para los clientes de AEM Forms, es esencial instalar el paquete de complementos de AEM Forms después de instalar cualquier paquete de servicio, paquete acumulativo o paquete de funciones de AEM.

>[!NOTE]
>
>Los paquetes de complementos de AEM Forms ayudan a alinear la funcionalidad de los formularios con los paquetes de servicios de AEM y los paquetes de correcciones acumulativas. Por lo tanto, es imperativo instalar AEM paquete de complementos de formularios después de instalar cualquier Service Pack AEM, Cumulative Fix Pack o Feature Pack.

#### Formularios adaptables {#adaptive-forms}

* Problemas de uso con el componente garabatear para dispositivos iOS 12.1. NPR-29082: revisión para CQ-4261765

#### Forms: seguridad de documentos {#forms-document-security}

* La verificación de todas las firmas de un PDF mediante PDF Advanced Electronic Signatures (PAdES) genera InvalidOperationException. NPR-27848: revisión para CQ-4244837

#### Forms - Correspondencia {#forms-correspondence}

* Al obtener una vista previa de la carta como PDF, el campo de texto colocado en la página de formato no respeta el valor introducido desde la ficha de datos o según el vínculo de datos especificado. NPR-29239: revisión para CQ-4266856.

#### Forms: comunicación interactiva {#forms-interactive-communication}

* Cuando se agrega un carácter de apóstrofo, los campos rellenados previamente en la letra aparecen como caracteres ASCII en lugar de alfabetos normales. NPR-28863: revisión para CQ-4262900

### Instalador JEE de Forms {#forms-jee-installer}

* No hay nuevas correcciones de AEM Forms en el instalador JEE de Forms.

## Revisiones y paquetes de funciones incluidos en los paquetes de correcciones acumulativas anteriores {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Paquete de correcciones acumulativas 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha habilitado la compatibilidad con la API v3.0 de MS Translator para AEM 6.2
* Se agregó un mensaje de registro tras la instalación correcta del paquete para todos los SP, CFP y HF.

### Assets {#assets}

* No se puede cambiar el nombre de la carpeta DAM si falta el permiso Editar ACL. NPR-27555: revisión para CQ-104652
* La herramienta de edición de ajustes preestablecidos de imagen no responde en la versión 6.2.1 de CFP 17 y posterior. NPR-28147: revisión para CQ-4261041

### Sites {#sites}

* El Verificador de vínculos no completa el trabajo, se queda atascado con vínculos que no responden. NPR-27373: revisión para CQ-4256030
* El archivo de segmento no se carga correctamente debido a una ruta raíz adicional que rompe la ruta del segmento. NPR-28014: revisión para CQ-4260332

### Integración {#integration-1}

* La cancelación de herencia de LiveCopy no funciona correctamente en contenedores de destino. NPR-28129: revisión para CQ-4259813
* Las acciones cq:no se toman en consideración para un componente dirigido. NPR-27616: revisión para CQ-4257497

* La visualización del icono para romper la herencia no es coherente. NPR-27671: revisión para CQ-4257779

### Felix {#felix}

* El detalle del componente de la consola web falla con 500 después de la instalación de CFP 18 en AEM instancia 6.2 SP1. NPR-28350: revisión para CQ-4261095

### Traducción {#translation}

* Habilite la compatibilidad con el servicio MS Translator en AEM 6.3 después de actualizar MS Translator a la API v3.0. NPR-28123: Revisión para CQ-4259096

### IU: bases {#ui-foundation}

* El calendario de sitios de OOTB muestra fechas incorrectas. NPR-28392

### Granite {#granite}

* El diccionario no se invalida para los paquetes de recursos que usan sling:basename . NPR-27624

### Soporte {#sustenance}

* Los registros de actividades del administrador de paquetes deben extraerse en un archivo de registro independiente. NPR-27323: Revisión para Granite-14866
* Una frase/redacción/línea de registro estandarizada en error.log que se mostrará cuando se complete la instalación. NPR-27835
* El complemento de paquete Granite está eligiendo la dependencia de una versión inferior de org.apache.sling.i18n. Revisión para CQ-4263245
* El paquete com.adobe.cq.com.adobe.cq.ui.commons se elimina al instalar el último CFP después de 6.2SP1-CFP15. Revisión para CQ-4258808

### Forms {#forms-1}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-1}

#### Formularios adaptables {#adaptive-forms-1}

* Vulnerabilidad de la inyección de XML con AEM Forms. NPR-27843: revisión para CQ-4257315

### Instalador JEE de Forms {#forms-jee-installer-1}

* No hay nuevas correcciones de AEM Forms en el instalador JEE de Forms.

### Los paquetes de contenido y los paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included}

El siguiente texto documentos la lista de paquetes OSGI y paquetes de contenido incluidos en la CFP.

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP19

[Obtener archivo](assets/do-not-localize/cfp19_osgi_bundles.txt)

Lista de paquetes de contenido incluidos en AEM 6.2SP1-CFP19

[Obtener archivo](assets/do-not-localize/cfp19_content_packages.txt)

### Paquete de correcciones acumulativas 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se añadió la compatibilidad en DAM CommandLineProcess para acabar con el proceso de larga ejecución.
* Se corrigió una fuga de sesión en ReplicationEventListener.
* Se añadió la compatibilidad con la redirección al componente de página principal.

### Recursos {#assets-1}

* Los procesos Camera Raw se quedan atascados durante los períodos de ingestión masiva que eventualmente bloquean todo el procesamiento del flujo de trabajo. NPR-26990: revisión para NPR-23860
* La funcionalidad de descarga aprovecha AEM Assets mediante el servlet de descarga de recursos, lo que permite a los usuarios anónimos descargar todos los recursos. NPR-27054, revisión para CQ-4254732
* Los caracteres especiales aparecen desglosados en la línea de asunto de las plantillas de correo electrónico en AEM. NPR-26470: revisión para CQ-4252368

### Sitios {#sites-1}

* Debido a un comportamiento incorrecto de la clase ConfigPostProcessor, al suspender la imagen principal se elimina cq: Tipo de mezcla LiveRelationship de la página secundaria. NPR-26745: revisión para CQ-4254163
* Añada la compatibilidad con la redirección al componente de página principal. NPR-26576: revisión para CQ-110529
* Migrar context hub a jquery 3. NPR-26956: revisión para CQ-4255472
* Los campos de entrada de anclaje aparecen fuera de la sección visible del explorador en el cuadro de diálogo hasta que se maximiza. NPR-26852: revisión para CQ-4255019
* Copie y pegue texto insertando &lt;br> no deseados en el fragmento Contenido. NPR-26660: revisión para CRTE-151
* El administrador del sitio clásico no procesa la lista en el panel derecho de algunas páginas. NPR-27247: revisión para CQ-4251621
* (IU clásica) Los intentos de mover o cambiar el nombre de las páginas generan un error: &quot;Error al mover la página&quot;. NPR-27179: revisión para CQ-4235907

### Integración {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever recorre todo el árbol para recopilar las marcas disponibles. NPR-27060: revisión para CQ-4255790

### WCM: componentes base {#wcm-foundation-components}

* Problema de funcionalidad de búsqueda con el componente lista de Foundation. NPR-26817: revisión para CQ-4250324

### Plataforma {#platform}

* Debido a un guión largo de caracteres especiales, el Editor tiene problemas para vaciar la caché. NPR-27199: revisión para CQ-4242790

### Granito {#granite-1}

* El validador del paquete no valida los paquetes incluidos en CFP/SP. NPR-26775: Revisión para Granite-22825

### Replicación {#replication}

* Filtración de sesiones JCR en ReplicationListener. NPR-27063: revisión para CQ-4232088

### Forms {#forms-2}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-2}

* No hay nuevas correcciones de AEM Forms en el paquete complementario de Forms.

### Instalador JEE de Forms {#forms-jee-installer-2}

* No hay nuevas correcciones de AEM Forms en el instalador JEE de Forms.

#### Los paquetes de contenido y los paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-1}

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP18

[Obtener archivo](assets/do-not-localize/62cfp18updated_bundles.txt)

Lista de paquetes de contenido incluidos en AEM 6.2 SP1-CFP18

[Obtener archivo](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Paquete de correcciones acumulativas 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Compatibilidad añadida con las direcciones URL sin extensión del sitio en at-integration.js
* Se ha eliminado el importador de encuestas S7 de la configuración del servicio en la nube S7.
* Cambios en la vista de audiencias para admitir la estructura de carpetas para la implementación de varios usuarios.
* Actualización a jqueryui   clientlib v1.12.1.

### Recursos {#assets-2}

* Para iniciar flujos de trabajo desde la interfaz de usuario de recursos, el usuario debe tener permisos de escritura, eliminación o modificación. NPR-25688: revisión para CQ-4250140
* Los botones Publicar y Cancelar la publicación permanecen visibles incluso para los usuarios sin permisos &quot;replicar&quot;. NPR-25094
* (Flujo de trabajo) El flujo de trabajo de los recursos de etiquetas inteligentes no se procesa a través de la configuración del proxy AEM. NPR-25915: revisión para CQ-4248202
* Elimine el importador de encuestas S7 de la configuración del servicio en la nube S7. NPR-25239: revisión para CQ-95236

### Sitios {#sites-2}

* Los flujos de trabajo iniciados desde el Editor -> Información de página contienen la ruta de contexto en la carga útil. NPR-26389: revisión para CQ-76804
* (Comprobador de vínculos externos) Los vínculos https no válidos se muestran como vínculos válidos. NPR-25541: revisión para CQ-4201333
* (IU clásica) Al crear una página independiente en una Live Copy, la página se crea como una Live Copy. NPR-25610: revisión para CQ-4249801
* Problemas con los recursos de publicación asociados con el componente Importador de diseños cuando se activa una página. NPR-25638: revisión para CQ-102532
* La barra de herramientas de texto enriquecido RTE cubre la lista de selección. NPR-25165: revisión para CQ-4248948
* Migrar contexthub a jquery 3. NPR-25059: revisión para Granite-19902
* Para los componentes parsys anidados, siempre se aplica el primer diseño satisfactorio (con la ruta menos anidada) de varios componentes disponibles. Para obtener más información, consulte [Resolución de ruta de diseño](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/page-templates-static.html). NPR-25250: revisión para CQ-4246276

### Integración {#integration-3}

* Si se utiliza la integración de destinatario OOTB, la segmentación de un componente procesa toda la página en lugar de un componente de destino vacío. NPR-25273: revisión para CQ-4248003
* Si se interrumpe la herencia en el modo de destino, el componente seguirá mostrándose como destino con la herencia no dañada en el modo de edición. NPR-25324: revisión para CQ-4248162
* Cuando se define una personalización en una página y se resuelve una audiencia, la experiencia correspondiente se muestra en modo de edición. NPR-25731: revisión para CQ-4249465
* URL de teaser errónea al usar AEM con una ruta de contexto no predeterminada. NPR-25971: revisión para CQ-4250953
* Representación en blanco al utilizar optout. NPR-25295: revisión para CQ-4246792
* Las experiencias eliminadas del entorno de creación nunca se eliminan del sitio de publicación tras la activación de página. NPR-24869: revisión para CQ-4247832

### DAM: Cliente DM {#dam-dm-client}

* (Chrome, Firefox) VideoPlayer ignora los clics del ratón en los dispositivos táctiles. Revisión para CQ-4247370

### Plataforma {#platform-1}

* Permite configurar el número máximo de reintentos al adquirir o liberar un paquete. NPR-25328: revisión para Granite-22376
* Registro incorrecto en caso de errores de replicación. NPR-25308: revisión para CQ-4249402
* La instalación de Forms AEM 6.2 Forms CFP8 a CFP14 provoca que el POI de Apache falle. NPR-25053: revisión para Granite-21771

### Granito {#granite-2}

* El proceso de sincronización del usuario falla con la excepción OakConstraint0022. NPR-25729: Revisión para Oak-7428

### Communities {#communities}

* el paquete cq-social-as-provider no inicio con las versiones 3.x del controlador mongo. NPR-26271: revisión para CQ-4252710

### IU: bases {#ui-foundation-1}

* Actualización a jqueryui   clientlib v1.12.1. NPR-25090: Revisión para Granite-21981, CQ-4248897

* (Omnisearch): La propiedad &#39;Title&#39; es vulnerable a las secuencias de comandos entre sitios (XSS) en Sitios. NPR-24994: revisión para Granite-19933

### Forms {#forms-3}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-3}

#### Formularios adaptables {#adaptive-forms-2}

* Codificación incorrecta al enviar datos desde el formulario adaptable. NPR-25539

#### Forms: administración {#forms-management}

* Los recursos de formulario no relacionados aparecen como referencias al publicar la página. NPR-26167: revisión para CQ-4251004

### Instalador JEE de Forms {#forms-jee-installer-3}

#### :Seguridad de los documentos{#document-security}

* La variable se rellena como Lista de tipo de datos, el subtipo es cadena, pero se obtiene el error &quot;no se puede forzar el objeto&quot;. NPR-26194: revisión para CQ-4252287
* No se puede acceder a las configuraciones de marca de agua después de instalar 6.2-SP1-CFP15. NPR-26130: revisión para CQ-4250984

### Los paquetes de contenido y los paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-2}

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP17

[Obtener archivo](assets/do-not-localize/62cfp17updated_bundles.txt)

Lista de paquetes de contenido incluidos en AEM 6.2SP1-CFP17

[Obtener archivo](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Paquete de correcciones acumulativas 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha añadido la compatibilidad con STARTTLS en el servicio de correo de Day CQ.
* Se corrigió la alineación de los iconos de ContextHub en la ventana emergente de perfil.
* Correcciones en la funcionalidad de mostrar u ocultar del componente desplegable.
* Actualice a la última versión de Jackson 2.8.11

### Recursos {#assets-3}

* No se puede iniciar un flujo de trabajo desde una vista de lista. NPR-24393: revisión para CQ-4245788
* (Firefox/Chrome) No se pueden descargar recursos en la página Uso compartido de recursos. NPR-24523: revisión para CQ-4224408
* Se ha aumentado la calidad predeterminada para la previsualización de vídeo en AEM. NPR-24148: revisión para CQ-4244310

### Integración {#integration-4}

* Cuando un componente está dirigido a una instancia de publicación, aparece un parpadeo que muestra la experiencia predeterminada antes de la experiencia de destino. NPR-23992: revisión para CQ-4242038
* Las experiencias eliminadas del entorno de creación nunca se eliminan del sitio de publicación tras la activación de página. NPR-24869: revisión para CQ-4247832

### Plataforma {#platform-2}

* Parche jQuery 1.12.4 de clientlib para incluir una corrección de seguridad. NPR-24129: revisión para Granite-20058
* Se ha añadido la compatibilidad con STARTTLS en el servicio de correo de Day CQ. NPR-23941: revisión para CQ-4240397
* Elimine el valor predeterminado de MERGE_PRESERVE aclHandling. NPR-24593: revisión para Granite-21889
* LineChecker no puede externalizar vínculos cuando la solicitud contiene parámetros de consulta no válidos. NPR-24127: revisión para CQ-4241893

### Medios convencionales {#msm}

* Revisiones proactivas a ataques de secuencias de comandos entre sitios (XSS). NPR-21893: revisión para CQ-4223385
* MSM LiveRelationship: RolloutConfig eficaz incorrecto si BlueprintConfig está en la raíz. NPR-23999: revisión para CQ-4243000

### Sitios {#sites-3}

* La creación de una nueva experiencia en un área de Live Copy requiere que se rompa la herencia para configurarla. NPR-24995, revisión para CQ-4248209
* (IU táctil) Varios iconos de la barra de herramientas superior desaparecen al bloquear o desbloquear una página. NPR-23954: revisión para CQ-4243345
* Los campos no están correctamente alineados en el contexto. NPR-23958
* Acción de publicación en la creación de saltos de página bloqueados. NPR-23970: revisión para CQ-4243203
* Los informes OOTB en /etc/reports/ no funcionan correctamente y no muestran gráficos de datos históricos. NPR-20035: revisión para CQ-4220180
* La creación de inicios falla al iniciar el flujo de trabajo &#39;Solicitar inicio&#39; en un proyecto. NPR-24255: revisión para CQ-4245030
* Etiquetas y atributos HTML ignorados por los correos electrónicos tras la instalación de CFP10. NPR-24287: revisión para CQ-4240028
* TagPicker: Sugerencia de etiquetas en el campo de etiqueta de esquema de metadatos de etiquetas consultas de nodos etiquetables, por lo tanto, tardan mucho tiempo en cargarse. NPR-24347: revisión para CQ-4244291
* La integración de Salesforce falla con las configuraciones de proxy. NPR-24418: revisión para CQ-4245300
* (WCM) PageManager deja la página protegida en Excepción durante la creación de la revisión. NPR-24565: revisión para CQ-4246203
* El botón Emulador de dispositivos desaparece del modo de edición y previsualización después de aplicar CFP14. NPR-24566: revisión para CQ-4247060
* (IU clásica) Todas las etiquetas se muestran como vacías una vez creadas en el cuadro de diálogo. NPR-24688, revisión para CQ-4246407
* No se puede crear la versión en el primer intento. NPR-24774: revisión para CQ-4232176
* Los informes OOTB en /etc/reports/ no funcionan correctamente y no muestran gráficos de datos históricos. NPR-24138: revisión para CQ-4220180

###  Vulnerabilidad{#vulnerability-1}

* La integración de Salesforce es vulnerable a la falsificación de solicitudes del lado del servidor (SSRF). NPR-24289: revisión para CQ-4245277
* Vulnerabilidad de falsificación de solicitudes del lado del servidor (SSRF) en ReportingServicesProxyServlet. NPR-24657: revisión para CQ-4246880

### Granito {#granite-3}

* Las operaciones de lectura de metadatos no finalizan. NPR-24240: revisión para Granite-19866
* Actualice Jetty a 9.4.11.v20180605 para corregir vulnerabilidades. NPR-25033: revisión para Granite-22120

### WCM: componentes base {#wcm-foundation-components-1}

* PageComparator lanzando ClassCastException mientras se ordenan las páginas. NPR-24123: revisión para CQ-4244048
* La funcionalidad Mostrar/Ocultar del componente desplegable del formulario no funciona correctamente. NPR-24562: revisión para CQ-4222853

### Interfaz de usuario {#user-interface}

* Se observa un alto uso de la CPU debido a muchas solicitudes en la funcionalidad de búsqueda de administración. NPR-23588: revisión para Granite-21286
* (IU clásica) El componente muestra los valores predeterminados aunque el servicio del modelo de datos de formulario asociado esté establecido en un campo vacío. NPR-21903: revisión para GRANITE-19744
* Varios campos lanzan NPE cuando no hay ningún FormData presente para la solicitud. NPR-24513: revisión para Granite-21055

## Forms {#forms-4}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-4}

#### Núcleo {#core}

* (OSGI) El OSGI de AEM Forms se vio afectado por la alerta de seguridad de enlace de datos de Jackson. NPR-24274: revisión para CQ-4230245

#### Rights Management {#rights-management}

* Apache POI falla tras la instalación AEM 6.2 SP1-CFP14. NPR-25054, NPR-25052: revisión para CQ-4245898, CQ-4244778

#### HTML5 Forms {#html-forms}

* Los datos no se rellenan con el prefijo de campos multilínea en la previsualización HTML. NPR-23357: revisión para CQ-4244212
* Cuando se obtiene una vista previa de una carta mediante la previsualización predeterminada, la asignación de fragmentos de diseño no se muestra, mientras que la misma aparece correctamente cuando se hace clic en el botón previsualización. NPR-22993: revisión para CQ-4237745
* Problema con la previsualización HTML de un campo de texto cuando se aplica un patrón de número de seguridad social a una plantilla. NPR-23205

#### Formularios adaptables {#adaptive-forms-3}

* Error &quot;No se ha definido la guía&quot; al agregar AEM formulario al componente parsys. NPR-24269: revisión para CQ-4244546

### Instalador JEE de Forms {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Los extremos de línea de ventana en archivos de script de Shell hacen que LCM no se ejecute en UNIX. NPR-22958

### Los paquetes de contenido y los paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-3}

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP16

[Obtener archivo](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Lista de paquetes de contenido incluidos en AEM 6.2SP1-CFP16

[Obtener archivo](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Paquete de correcciones acumulativas 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Corrección de seguridad proactiva en la tabla Foundation para mantener la coherencia del diseño.
* Se añadió la compatibilidad de typeHint para guardar valores como cadena.
* Proporciona seguridad mejorada para el servicio de cumplimentación previa de Forms
* Actualice al archivo adobe-reader-extension-dsc.jar más reciente para obtener correcciones en Reader Extension.
* Se ha ajustado el gancho de validación para tener en cuenta los elementos &quot;:no válidos&quot; para la entrada de número de ampliación.

### Recursos {#assets-4}

* Los datos EmbedXMP siempre se definen como “activos” para el proceso de generación de Ptiff. NPR-22776: revisión para CQ-4234498
* No se pueden establecer varios valores predeterminados en los campos de varios valores. NPR-22900: revisión para CQ-4239000
* (Dynamic Media) Al seleccionar la casilla de verificación Representaciones dinámicas, el archivo zip descargado genera la imagen TIFF original con un archivo de byte cero. NPR-22410: revisión para CQ-4198471
* (IU táctil) Ubicación de carga predeterminada para los recursos en la vista de columnas. NPR-23475: revisión para CQ-4237057

### Integración {#integration-5}

* En el modo Destinatario, los autores pueden modificar un componente heredado del modelo sin cancelar la herencia. NPR-22751: revisión para CQ-4237907
* La variable de ruta no se codifica correctamente, lo que provoca secuencias de comandos de sitios cruzados (XSS) no persistentes. NPR-22851

### Medios convencionales {#msm-1}

* Durante la implementación de un LiveCopy con varias configuraciones de implementación, si se produce un ResourceNameConflict debajo de la raíz, el flujo de implementación termina sin incluir todas las ramas. NPR-22842: revisión para CQ-4236188

### Plataforma {#platform-3}

* Implementar un límite de sondeo en una solicitud de aplicación inversa. NPR-23351: revisión para Granite-21135****
* El cambio del patrón de mensajes no se refleja en los registradores personalizados. NPR-23486: revisión para CQ-4241974

### Sitios {#sites-4}

* No funciona la creación de un vínculo dentro de un texto de un editor de texto enriquecido en un documento con espacios u otros caracteres especiales. NPR-22289: revisión para CQ-4224321
* Al guardar el segmento con un valor enorme (10000000000), se establece el valor de ampliación en 0 que provoca el mensaje de error. NPR-22524: revisión para CQ-4237006
* No se puede hacer clic en Añadir elemento en el componente Multicampo. NPR-22552: revisión para CQ-4237404
* La barra de desplazamiento horizontal no está visible cuando el segmento tiene un título largo. NPR-22615: revisión para CQ-4237001
* La carga de una audiencia vacía genera un código JavaScript incorrecto. NPR-22974: revisión para CQ-4238734
* Al programar una activación o desactivación, el título del flujo de trabajo es obligatorio, por lo que el título del flujo de trabajo personalizado no se traduce en la línea de tiempo. NPR-23121: revisión para CQ-4237552
* Solicitud de correcciones a problemas relacionados con segmentos de Destinatario en Sitios. NPR-23128
* (Firefox) La casilla de verificación de la persona seleccionada no es la correcta. NPR-23345
* Las etiquetas de los distintos modos se muestran junto con los iconos. NPR-23275
* Error &#39;Valor del selector de recursión no válido&#39; al migrar un componente de AEM 6.0 a AEM 6.2. NPR-23503: Revisión para CQ-4241258

### Comunidades {#communities-1}

* Las notificaciones por correo y web no se activan debido a un error en los mensajes de los grupos. NPR-23447: revisión para CQ-4242880

### Traducción {#translation-1}

* Las copias de idioma de los recursos se crean cuando el recurso &quot;No traducir&quot; se configura en la configuración de traducción. NPR-22540: revisión para CQ-4237962

### Interfaz de usuario {#user-interface-1}

* El uso de Omniture con una consulta de guión devuelve un error de servidor. NPR-22999: revisión para Granite-19674
* DatePicker no admite la configuración manual de sugerencias de tipo externas establecidas por campo oculto. Si se cambia la sugerencia de tipo se obtiene un error de conversión. NPR-23333: revisión para Granite-21194

### WCM: componentes base {#wcm-foundation-components-2}

* El componente CAPTCHA ha quedado obsoleto para una mejor seguridad, si utiliza el componente CAPTCHA, entonces envíe el mensaje &quot;El componente Captcha está obsoleto y ya no debe usarse&quot;. se mostrará después de instalar 6.2 SP2-CFP15 o una versión posterior. AEM componente se puede personalizar para incluir reCAPTCHA para una mejor seguridad NPR-22151: Revisión para CQ-4220052
* El componente &#39;Tabla&#39; de WCM Foundation es vulnerable a las secuencias de comandos entre sitios almacenadas. NPR-23206: revisión para CQ-4240760

###  Vulnerabilidad{#vulnerability-2}

* Ejecución de scripts en sitios múltiples (XSS) en vínculos de proyectos de la interfaz de usuario de administración. NPR-23272: revisión para CQ-4241795

## Forms {#forms-5}

### Paquete de complemento de Forms {#forms-add-on-package-5}

#### Administración de correspondencia {#correspondence-management}

* Cuando se obtiene una vista previa de una carta mediante la previsualización predeterminada, la asignación de fragmentos de diseño no se muestra, mientras que la misma aparece correctamente cuando se hace clic en el botón previsualización. NPR-23335: revisión para CQ-4237745
* Los datos de la letra correspondientes a los enlaces definidos en XDP no se rellenan usando la dirección URL de la carta directa. NPR-24145: revisión para CQ-4244290

#### Forms móvil {#mobile-forms}

* (Administración de correspondencia) Desalineación de datos al cargar la carta con XML de destinatario. NPR-22993: revisión para CQ-4237663

#### Servicio de Extensiones de Reader {#reader-extensions-service}

* No se puede aplicar la extensión de lector en Adobe PDF. NPR-23067

#### Administrador de Forms {#forms-manager}

* Forms incrustado en el sitio no se publica al volver a publicar la página del sitio. NPR-23014: revisión para CQ-4236566

####  Vulnerabilidad{#vulnerability-3}

* Revisiones proactivas para secuencias de comandos entre sitios. NPR-20624: revisión para CQ-4206055
* Vulnerabilidad de la ejecución almacenada de scripts en sitios múltiples (XSS) en la ficha Notas del administrador de Forms. NPR-27157: revisión para CQ-4255556

#### Servicio de cifrado {#encryption-service}

* (OSGI) [JEE] Estado de firma incorrecto para PDF con datos adjuntos mientras se verifica con &quot;Validar proceso PDF&quot;. NPR-23269, NPR-23737

### Instalador JEE de Forms {#forms-jee-installer-5}

#### Núcleo {#core-1}

* Deben solucionarse los problemas notificados en la análisis de código estático de Core-ext. NPR-13947

#### Servicio PDFG {#pdfg-service}

* El conversor de HTML a PDF no funciona. NPR-21545

### Los paquetes de contenido y los paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-4}

El siguiente texto documentos la lista de paquetes OSGI y paquetes de contenido incluidos en la CFP.

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP15

[Obtener archivo](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Lista de paquetes de contenido incluidos en AEM 6.2SP1-CFP15

[Obtener archivo](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Paquete de correcciones acumulativas 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha mejorado la editabilidad de las propiedades de metadatos de los recursos.
* Se ha reconfigurado el trabajo Notificación de caducidad de contraseña para los recursos que ya están en estado caducado.
* Consola táctil personalizada para ampliar configuraciones regionales adicionales.
* Se ha actualizado cq-msm-core para lograr una sincronización eficiente de Livecopyindex.
* Funcionalidad de replicación optimizada para varios lanzamientos.

### Recursos {#assets-5}

* Los usuarios no pueden descargar recursos con nombres de archivo largos y de renuncia de responsabilidad. NPR-22163: revisión para CQ-4235274
* El carácter de comilla única evita la actualización de metadatos en la vista masiva y la interfaz de usuario se interrumpe completamente al abrir las propiedades de un recurso mediante las acciones rápidas de la barra de herramientas. NPR-22317, NPR-22353: revisión para CQ-4236990, CQ-4236469
* El trabajo de notificación de caducidad del recurso no desactiva los recursos caducados. NPR-22346: revisión para CQ-4237188
* La descarga de recursos falla al usar Digital Rights Management en Assets en Safari. NPR-22378: revisión para CQ-4236460
* La representación web para imágenes pequeñas tiene un tamaño de píxel impreciso. NPR-22435: revisión para CQ-4236742

### Sitios {#sites-5}

* (IU táctil) La etiqueta desplazada aparece en la ubicación antigua y en la nueva en las propiedades de la página. NPR-21921, revisión para CQ-4238598
* (IU táctil) El editor de texto enriquecido elimina todos los atributos que no sean id de la etiqueta &lt;a>. NPR-22045: revisión para CQ-4234133
* Al pegar contenido directamente en el Editor de texto enriquecido mediante CTRL+V se omiten los saltos de línea. NPR-22117: revisión para CUI-5881
* (IU táctil) No se pueden mostrar más de 40 etiquetas en la Área de nombres. NPR-22290: revisión para CQ-99114
* Problemas de fuentes RSS, puerto -1 a AEM 6.2 NPR-22158: Revisión para CQ-4233339
* (IE) Al crear cualquier carácter en un campo de texto enriquecido por primera vez, se agrega un espacio final al carácter. NPR-22443: revisión para CQ-4235343
* Al intentar hacer coincidir el nombre del paquete, el objeto Java Use congela SightlyJavaCompilerService debido a un carácter de espacio final en la declaración del paquete. NPR-22557: revisión para Granite-20836
* La consola de IU táctil no recoge nuevos idiomas para el etiquetado. NPR-22250: revisión para CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Tanto la fecha de publicación como la fecha de portada eran campos obligatorios que se debían definir para las publicaciones antes de que se cargaran en DPS. NPR-22484

### Comercio {#commerce}

* Varias vulnerabilidades de scripts entre sitios (XSS) en el comercio crean un asistente de catálogos. NPR-22344: revisión para CQ-4237017

### Medios convencionales {#msm-2}

* La sincronización de LiveCopyIndex provoca congestión de subprocesos durante las actualizaciones de índice largas. NPR-22214: revisión para CQ-90667
* la propiedad cq:cugEnabled se desactiva cuando se edita otro campo de una Live Copy, por lo que la página queda desprotegida. NPR-22246: revisión para CQ-4236050
* La acción Despliegue de página no puede actualizar los elementos secundarios cuando se suspende una página. NPR-22483: revisión para CQ-4236956
* El despliegue de una estructura que se ha movido en una página principal conduce a un cq:moveTarget incorrecto. NPR-22373: revisión para CQ-4232536

### Integración {#integration-6}

* Al intentar ordenar ofertas en la biblioteca del selector de ofertas, se produce un comportamiento errático. NPR-22208: revisión para CQ-4235439
* TargetContentImpl hace que AEM seo lenta durante consultas de larga duración. NPR-22361: revisión para CQ-4236907
* El motor de destino (mbox.js, at.js) no utiliza direcciones URL manipuladas y utiliza direcciones URL que contienen dos puntos, lo que puede provocar errores en determinadas implementaciones. NPR-22366: revisión para CQ-4237854
* La personalización de la página requiere publicación en el nodo de la marca. NPR-22370: revisión para CQ-4236895

### Foundation {#foundation}

* Los modelos de Apache Sling Scripting Sightly utilizan el paquete de proveedores **org.apache.sling.scripting.sightly.models.provider/1.0.18**. NPR-22614: Revisión para Sling-5944, Sling-6866

### Proyectos {#projects}

* Workflow Starter no puede aceptar el valor TypeHint de String. NPR-22436: revisión para CQ-4237855

### Traducción {#translation-2}

* Investigación de los problemas con la funcionalidad Vista previa. NPR-22201: revisión para CQ-4223753

### Interfaz de usuario {#user-interface-2}

* (IU clásica) El componente muestra los valores predeterminados aunque el servicio del modelo de datos de formulario asociado esté establecido en un campo vacío. NPR-21903: revisión para GRANITE-19744

### WCM: componentes base  {#wcm-foundation-components-3}

* Error al publicar una página de Live Copy que apunta a una página de importador en campañas de Adobe. NPR-22470: revisión para CQ-4237164
* Errores de JavaScript al abrir el Editor de fragmentos de experiencia. NPR-22598: revisión para CQ-4238415

### Flujo de trabajo {#workflow}

* El servicio de notificación por correo electrónico de flujo de trabajo de CQ por día desencadena un mensaje de correo electrónico por nodo Mongo para las notificaciones WorkflowCompleted y WorkflowAborted. NPR-22486: revisión para CQ-4238172

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

* (Espacio de trabajo HTML) Cuando un usuario reclama una tarea, el recuento de colas se actualiza para ese usuario en particular, pero no para otros usuarios a menos que se actualice la página. NPR-19778: revisión para CQ-4233665

### Paquetes y paquetes de contenido OSGI incluidos en CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP14

[Obtener archivo](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Lista de paquetes de contenido incluidos en AEM 6.2SP1-CFP14

[Get ](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
FileAEM Cumulative Fix Pack 6.2 SP1-CFP13 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se habilitó la configuración del campo Parámetro estático dentro de la configuración del componente de Destinatario al usar AT.js como biblioteca de cliente.
* Correcciones en la funcionalidad de mostrar u ocultar del componente desplegable.
* Correcciones para usar audiencias de sincronización de destinatarios.
* Se ha aumentado la versatilidad de la gestión de correspondencia para admitir caracteres especiales.

### Recursos {#assets-6}

* La depuración de versiones no puede eliminar versiones antiguas de los recursos. NPR-21682: revisión para CQ-4212996
* La reordenación de carpetas en una carpeta reordenable no persiste. NPR-21964: revisión para CQ-4231761

### Sitios {#sites-6}

* (TouchUI)(ClassicUI) Varias vulnerabilidades de scripts entre sitios (XSS) en componentes principales y HTL. NPR-21532: Revisión para CQ-4232305 y CQ-4232511
* La creación o el formato de contenido (por ejemplo, asignar o quitar nuevos estilos de lista) en un texto seleccionado no funcionan bien en Internet Explorer 11. NPR-21533: revisión para CQ-4230689
* (Safari) Los usuarios no pueden realizar la vista de todos los recursos en el panel del buscador de recursos. NPR-21981: revisión para CQ-4213720
* Deformación de tiempo devuelve el error &quot;RecursionTooDeepException&quot; con una página con errores y no se crea ninguna nueva versión aunque se cambie la fecha. NPR-21707: revisión para CQ-4199536
* Al cargar una página en el editor, WorkflowStatusProvider (pageinfo.json) se carga tres veces, lo que provoca que AEM instancia funcione con lentitud. NPR-21778: revisión para CQ-59232

### Integración {#integration-7}

* La creación de audiencias de tipo y navegador móvil en el modo de creación de Destinatario no funciona en AEM. NPR-21676, NPR-21681: revisión para CQ-4232100
* En una latencia alta durante la actualización de un componente de destino, es posible agregar otra oferta antes de que el componente se actualice por completo. NPR-21744: Revisión para CQ-4233158/CQ-4234293
* Los usuarios no pueden ver los valores de parámetro estático de prueba en la llamada de mbox, lo que se puede ver al realizar pruebas con AT.js como biblioteca de cliente en la configuración de nube. NPR-21930: revisión para CQ-4234520

### Plataforma {#platform-4}

* Problemas de rendimiento con la sincronización de usuarios cuando el número de usuarios o grupos es grande. NPR-20431: revisión para CQ-4223282
* Los usuarios no se sincronizan con la sincronización de usuarios mediante Sling Distribution. NPR-21911: revisión para Granite-20404
* Impedir que las palabras dejen de resaltarse en extractos de búsqueda (en una página de Geometrixx). NPR-21835: revisión para Granite-21067\
   Nota: Esta corrección requiere el Oak CFP 1.4.20 o superior.

### Traducción {#translation-3}

* falta la propiedad jcr para el identificador de usuario de iniciador al crear un proyecto de traducción. NPR-21715: revisión para CQ-4230713

### WCM: componentes base {#wcm-foundation-components-4}

* La funcionalidad Mostrar/Ocultar del componente desplegable del formulario no funciona correctamente. NPR-22164: revisión para CQ-4235288

## Forms {#forms-7}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms {#forms-add-on-package-7}

#### Formularios adaptables {#adaptive-forms-5}

* Inyección de entidad externa XML (XXE) en Forms adaptable. NPR-21982: revisión para CQ-109878
* (iOS11) Al hacer clic en el componente de archivo adjunto, el archivo adjunto se abre con la cámara en lugar del explorador de archivos del dispositivo. NPR-21926: revisión para CQ-4214348
* Falta el título en la interfaz de usuario para la creación del tema, lo que provoca una excepción y un error en la representación del cuadro de diálogo. Revisión para CQ-4236143

#### Administración de correspondencia {#correspondence-management-1}

* Problemas de procesamiento con datos xml que contienen caracteres especiales. NPR-21712: revisión para CQ-4229137

### Instalador JEE de Forms {#forms-jee-installer-7}

#### Servicio del ensamblador {#assembler-service}

* El archivo PDF generado con 6.2.0-ASM-1017-003 está dañado. NPR-21427: revisión para CQ-4228046

#### Servicio PDFG {#pdfg-service-1}

* Error de OCR debido a un tamaño de página (PDF) inesperado de archivos PNG, JPEG y TIFF. NPR-19489: revisión para CQ-4209079

## Paquetes y paquetes de contenido OSGI incluidos en CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP13

[Obtener archivo](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Lista de paquetes de contenido incluidos en AEM 6.2SP1-CFP13

[Obtener archivo](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha mejorado la administración de metadatos para campos multivalor.
* Compatibilidad con códigos de país de varios caracteres (más de dos) en flujos de trabajo de traducción.
* Se mejoró la representación de páginas con varios componentes anidados.
* Se ha mejorado la sincronización de las fechas de publicación de los recursos entre AEM y Adobe Digital Publishing Suite.

### Recursos {#assets-7}

* Demasiados caracteres en OmniSearch hacen que el servidor de AEM se bloquee. NPR-21083: revisión para CQ-4223602
* Los valores especificados en la segunda opción de un campo multivalor en el Esquema de metadatos no se anexan a los valores especificados anteriormente en CRX-de. NPR-21220: revisión para CQ-4224526
* La descarga de recursos falla al usar Digital Rights Management en Assets en Safari. NPR-21387: revisión para CQ-4230287

### Sitios {#sites-7}

* (DAM) (ClassicUI) Varias vulnerabilidades de scripts entre sitios (XSS) en algunos archivos SWF en AEM inicio rápido de CQ Author/Publish. NPR-21073, NPR-21074: Revisión para NPR-20612
* El selector de etiquetas no traduce las etiquetas que están disponibles en varios idiomas.NPR-21221: Revisión para CQ-78855
* Los problemas de representación con AEM consola de artículos como el uso de varios componentes anidados hacen que sea lenta. NPR-21271: revisión para CQ-4224158

### Integración {#integration-8}

* Al agregar un marco de Destinatario, el modo de objetivo no está disponible en la lista Seleccionar modo del editor. NPR-21047

### Móvil bajo demanda {#mobile-on-demand-1}

* (Digital Publishing Suite) Las fechas de publicación de las publicaciones de AEM no coinciden con las fechas que aparecen en Folio Producer. NPR-21145

### Medios convencionales {#msm-3}

* El proceso de restablecimiento de Live Copy se detiene después de eliminar la primera página local en la LC. NPR-21276: revisión para CQ-4229743

### Plataforma {#platform-5}

* Después de actualizar a AEM 6.3, no se encuentran etiquetas personalizadas que hagan referencia a etiquetas implementadas como secuencia de comandos. NPR-20149: Revisión de Granite-18433

### Traducción {#translation-4}

* Los flujos de trabajo de traducción fallan con códigos lang_country superiores a 2 caracteres. NPR-21088: revisión para CQ-4197439
* No se debe permitir que la página de recursos se vuelva a enviar a un proyecto de traducción hasta que se complete el proyecto. NPR-21219: revisión para CQ-4209908

### Interfaz de usuario {#user-interface-3}

* El componente Seleccionar no elimina la propiedad destinatario durante el envío del formulario. NPR-21163: revisión para GRANITE-14125
* El doble de expansión HTTP.encodePathOfURI codifica el signo más &#39;+&#39;. NPR-21417: revisión para GRANITE-16340

###  Vulnerabilidad{#vulnerability-4}

* Secuencias de comandos entre sitios (XSS) en el editor de metadatos DAM. NPR-21434: revisión para CQ-83472
* Varios archivos SWF vulnerables a secuencias de comandos entre sitios (XSS). NPR-20612: revisión para CQ-4213297

## Forms {#forms-8}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms  {#forms-add-on-package-8}

#### Administración de correspondencia {#correspondence-management-2}

* (IE11) El procesamiento inicial del contenido HTML se produce solamente en el lado izquierdo, mientras que el lado derecho se carga intermitentemente después de cargar la IU completa. NPR-21554
* El botón de envío de previsualización de carta se desactiva después de instalar AEM 6.2 SP1-CFP9. NPR-21547
* Al seleccionar el tipo de vinculación de recursos, la ventana Selector de recursos no se abre en el asistente Editar enlace de datos de carta. NPR-21164: revisión para CQ-4194567
* Para editar un módulo de texto en línea o editable, toque el icono Editar correspondiente o haga clic con el doble en el módulo de texto correspondiente en la previsualización de letras. NPR-21402

#### Formularios adaptables {#adaptive-forms-6}

* El componente de botón de envío de AEM Forms muestra type=&quot;button&quot; en lugar de type=&quot;submit&quot;. NPR-21007
* Los datos se mantienen al agregar o eliminar nuevos paneles para los paneles repetitivos. NPR-21408

### Instalador JEE de Forms {#forms-jee-installer-8}

#### Núcleo {#core-2}

* La actualización a la última actualización 131 de Java 8 genera una excepción: &quot;El proveedor JsafeJCE está deshabilitado, se ha producido un error en la comprobación de integridad de FIPS 140 necesaria&quot;. NPR-21355

   **Nota:** Este NPR requiere una configuración adicional; para obtener más información, consulte  [Última actualización](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr) de Java 8.

* Actualice los tarros seguros a cryptoj 6.1.3.1 en Core, Encryption, Signature &amp; Documento Security. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Instalación de LCM {#install-lcm-1}

* Actualice Jsafe Jars a Cryptoj 6.1.3.1 en el instalador y LCM. NPR-21362

#### Servicio PDFG {#pdfg-service-2}

* Actualice Jsafe Jars a Cryptoj 6.1.3.1 en PDFG. NPR-21359

#### Administración de procesos {#process-management-1}

* (Espacio de trabajo HTML) Al habilitar el cambio de tamaño de la columna para que la categoría de nombre no aparezca truncada. NPR-19770: revisión para CQ-4233668

#### Servicio de Extensiones de Reader {#reader-extensions-service-1}

* Actualice los tarros seguros a cryptoj 6.1.3.1 en RE. NPR-21357

## Paquetes y paquetes de contenido OSGI incluidos en CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP12.1

[Obtener archivo](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Lista de paquetes de contenido incluidos en AEM 6.2 SP1-CFP12.1

[Obtener archivo](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha actualizado cq-msm-core para lograr una sincronización eficiente de Livecopyindex.
* Se ha mejorado la eficacia de edición de los fragmentos de contenido.
* Proporciona una opción de validación en el administrador de paquetes para detectar permisos ACL.
* Se ha introducido la capacidad de Campaña para incluir ID de correo electrónico para la correspondencia de los clientes.
* Se han mejorado las capacidades de codificación de vídeo para archivos Dynamic Media.
* Correcciones en Sightly Component y LiveCopies.

### Recursos {#assets-8}

* La codificación de vídeo de Dynamic Media falla en los archivos que incluyen espacios en sus nombres. NPR-20818: revisión para CQ-102469
* Varias vulnerabilidades de secuencias de comandos entre sitios (XSS) en algunos archivos SWF en AEM inicio rápido de CQ Author/Publish. NPR-21071, NPR-21072
* Los usuarios no pueden descargar recursos con nombres de archivo largos y de renuncia de responsabilidad. NPR-20255: revisión para CQ-4222139

### Sitios {#sites-8}

* Integración de AEM y Campaña: Los vínculos especiales se reescriben en Adobe Campaign para evitar que los clientes envíen mailto: hipervínculos en sus correos electrónicos. NPR-20787: revisión para CQ-4225760
* (IU táctil) AEM problemas de uso y de rendimiento cuando el idioma se establece en francés. NPR-20854: revisión para CQ-4227628
* La vinculación de un archivo de recurso codificado mediante el complemento de vínculo en RTE devuelve un vínculo vacío. NPR-20626, NPR-21059: revisión para CQ-4223011
* El editor de metadatos de fragmento de contenido evita que los autores de contenido guarden cambios en los fragmentos de contenido. NPR-20641: revisión para CQ-4224755
* El alias de propiedad de página lleva a solicitar publicación/solicitar cancelación de publicación. NPR-20731: revisión para CQ-4226227
* Problemas del componente de texto con la codificación del vínculo en el elemento RTE. NPR-20755: revisión para CQ-4224321

### Plataforma {#platform-6}

* ResourceResolverImpl.map() no invoca ResourceDecorator. NPR-20788: revisión para GRANITE-19718
* org.apache.sling.i18n.DefaultLocaleResolver no puede procesar solicitudes a través de org.apache.sling.engine.SlingRequestProcessor. NPR-20706: revisión para CQ-94880
* Solicite agregar una opción de validación en el Administrador de paquetes para detectar si se han cambiado los permisos/privilegios de ACL en un paquete en particular. Revisión para CQ-4229196

### Integración {#integration-9}

* (Search&amp;Promote) La definición ambigua del filtro para el paquete de contenido lleva a rutas sobrescritas durante la instalación. NPR-20808: revisión para CQ-4227615

### Flujo de trabajo {#workflow-1}

* Problemas de estabilidad con la implementación del servidor de producción de AEM. NPR-20979: revisión para Granite-19104

### Proyectos {#projects-1}

* (IU táctil) No se pueden agregar miembros del equipo a un proyecto. NPR-20990: revisión para CQ-4205375

### WCM: componentes base {#wcm-foundation-components-5}

* Sightly Image Component &#39;link to&#39; genera un error 403 debido a la falta de la extensión .html. NPR-20823: revisión para CQ-4195909
* En un sitio de modelo que utiliza LiveCopy, al intentar eliminar un componente Formulario, se genera una excepción NullPointerException y se vuelve a agregar el componente Formulario en lugar de eliminarlo. NPR-20855: revisión para CQ-4204628
* La sincronización de LiveCopyIndex provoca congestión de subprocesos durante las actualizaciones de índice largas. NPR-20634: revisión para CQ-90667

### Seguridad {#security}

* Actualización proactiva de la biblioteca XSS. NPR-21174
* Actualice a Apache Commons Email 1.5, que presenta una API simplificada para enviar correo electrónico. NPR-20509: revisión para Granite-18240
* Parche de seguridad aplicado a la API de protección Apache Sling XSS para eliminar la posibilidad de omitir XSS. NPR-21290: revisión para GRANITE-19924
* Omisión XSS en la función XSSAPI#getVálidoHref. NPR-21174: revisión para Granite-19924

### Aplicaciones móviles {#mobile-apps}

* Se han corregido problemas con las solicitudes de cabezal de curl para los recursos de OOTB en AEM. NPR-20511: Revisión para CQ-4221520 y CQ-103024

## Forms {#forms-9}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

Los aspectos destacados de AEM Forms son:

* Autenticación de certificados para los usuarios de Workbench habilitada.
* Correcciones de uso para administración de correspondencia, formularios HTML5 y espacio de trabajo de AEM Forms.

### Paquete de complemento de Forms {#forms-add-on-package-9}

#### HTML5 Forms {#html-forms-1}

* Problemas de uso con el componente garabatear en dispositivos iOS 10 y 11. NPR-21092

#### Administración de correspondencia {#correspondence-management-3}

* (Interfaz de usuario de correspondencia) Deshabilite el botón de envío después de un clic. NPR-21078

### Instalador JEE de Forms {#forms-jee-installer-9}

#### Servicio del ensamblador {#assembler-service-1}

* docConvertor no produce PDF/A con el error &quot;El prefijo &quot;stEvt&quot; del elemento &quot;stEvt:action&quot; no está enlazado&quot;. NPR-21032: revisión para CQ-4222540
* Se genera una excepción con el nombre java.lang.IllegalArgumentException, mensaje:Ninguna constante enum com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE al invocar el servicio OMPFSubmission/PDFA/PDFtoPDFA. Esto evita que el proceso de verificación de firma de corta duración se complete hasta que se reinicie el servidor. NPR-20792

#### Workbench {#workbench}

* Habilite la autenticación de certificados para los usuarios de Workbench. NPR-17548: revisión para CQ-4214486

#### Administración de procesos {#process-management-2}

* El proceso de preparación de datos se invoca varias veces cuando el formulario móvil se procesa con parámetros de fuente de datos. NPR-19801: revisión para CQ-4230427: CQ-4230400

## Paquetes y paquetes de contenido OSGI incluidos en CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP11

[Obtener archivo](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Lista de paquetes de contenido incluidos en AEM 6.2 SP1-CFP11

[Obtener archivo](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se ha añadido una nueva función de utilidad en DialogLoaded para pruebas.
* Pruebas y configuraciones de unidades de front-end añadidas en ClientLibraryProxyServlet.
* Correcciones de rendimiento en el componente de editor de varias imágenes in situ.
* Actualizaciones de configuración en Apache Sling JCR ResourceBundleProvider.

### Recursos {#assets-9}

* La previsualización de recursos no funciona si los flujos de trabajo de actualización de recursos están desactivados. NPR-20543: revisión para CQ-4204986
* Problemas de procesamiento con clase agregada en el granito: propiedad class (cq-damadmin-admin-assets-upload). NPR-20514: revisión para CQ-4219238
* Los recursos de miniaturas con caracteres especiales en el título muestran el objeto java en el atributo alt de NPR-20347: Revisión para CQ-4223620
* Reemplazar el código de comparación de versiones con el código propiedad de Adobe debido a problemas de licencias. NPR-20273: revisión para CQ-4223758
* Problemas de procesamiento al cargar archivos PSB CMYK con varias capas alfa. NPR-20251: revisión para CQ-4220869
* Los diccionarios de internacionalización no funcionan a menos que se reinicie el servidor en org.apache.sling.i18n 2.5.6. NPR-20525: Revisión de Granite - 19490
* No se generan depósitos de subprocesos según el período de Planificador con la configuración predeterminada del recopilador de volcado de subprocesos (inicio AEM predeterminado). NPR-20288: Revisión para GRANITE-19488 / GRANITE-12741 / CQ-90647.

### Sitios {#sites-9}

* Si el filtro de fecha modificado se cambia después de abrir la búsqueda guardada, no hay ningún efecto en los resultados y los resultados mostrados son los mismos que el valor guardado anterior del filtro de fecha modificado. NPR-19739: revisión para CQ-4219425
* No se pudieron cargar las páginas con componentes anidados. NPR-20312
* El flujo de trabajo de solicitud de eliminación se activa al eliminar los paquetes de flujo de trabajo. NPR-20266: revisión para CQ-4221686
* (IU táctil) Problema con Copiar/Pegar con el portapapeles del sistema operativo y el portapapeles AEM interno. NPR-20228: revisión para CQ-4220383
* AEM instancia se ralentiza con la vista de listas cuando se cargan varios recursos (más de 100). NPR-20034: revisión para CQ-4222695
* (IU táctil) La eliminación de lanzamientos mediante la consola de IU clásica hace que todas las páginas sean no editables. NPR-20520: revisión para CQ-4225074
* El menú desplegable destinatario no funciona con varios componentes RTE en un cuadro de diálogo. NPR-20345: revisión para CQ-4220981

### Plataforma {#platform-7}

* Cuando se accede mediante una sesión anónima, ClientLibraryProxyServlet no realiza solicitudes proxy a bibliotecas de cliente en la instancia de publicación y genera un error HTTP 404 no encontrado. NPR-20195: revisión para Granite-14409

### Integración {#integration-10}

* Si se selecciona el motor de destinatario como Adobe Target, se evita que el componente se cargue y se genera un error en el registro del servidor. NPR-20058: revisión para CQ-88071, CQ-109698, CQ-4201600

### Comercio {#commerce-1}

* No aparece ningún mensaje emergente de confirmación o redirección al crear productos de la misma página. NPR-20257: revisión para CQ-4223414

### Interfaz de usuario {#user-interface-4}

* Cuando el Selector de fecha es un campo de un campo múltiple, los valores guardados en los campos de fecha no persisten al editar el componente. NPR-20077: revisión para GRANITE-19147
* Las consultas anteriores no se anulan en caso de que se activen consultas consecutivas que produzcan resultados incorrectos. NPR-20397: revisión para GRANITE-19306

### WCM: componentes base {#wcm-foundation-components-6}

* La propiedad ImageMap sigue existiendo incluso después de eliminar las imágenes del componente de editor de varias imágenes in situ. NPR-20142: revisión para CQ-4222982

## Forms {#forms-10}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms  {#forms-add-on-package-10}

#### Formularios adaptables {#adaptive-forms-7}

* la secuencia de comandos valueCommit se ejecuta dos veces para DropDownList cuando se cambia a través de la interfaz de usuario. NPR-19989: revisión para CQ-110212

### Instalador JEE de Forms {#forms-jee-installer-10}

**Administración de procesos**

* El paquete CFP contiene AEM Forms HTML Workspace versión 2.2.26. NPR-20099
* El formulario precumplimentado no funciona cuando el formulario móvil está configurado para la vista como PDF. NPR-20566

**Rights Management**

* El cuadro de diálogo de selección de certificados de autenticación mutua/CAC debe mostrar los certificados con Uso mejorado de claves (EKU) como inicio de sesión con autenticación de cliente o tarjeta inteligente. NPR-20708
* Forms JEE admite autenticación mutua PKCS#11. NPR-15001

## Paquetes y paquetes de contenido OSGI incluidos en CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

Lista de los paquetes OSGi incluidos en AEM CFP 6.2 SP1-CFP10

[Obtener archivo](assets/do-not-localize/bundle-list-cfp10.txt)

Lista de paquetes de contenido incluidos en AEM CFP 6.2 SP1-CFP10

[Obtener archivo](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Configuración de la IU de Analytics Classic adaptada para entradas secretas.
* Correcciones para la caché de persistencia independiente para Contexthub.
* Cálculo preciso de las dimensiones de activos.
* Se ha optimizado AEM rendimiento al publicar recursos en Brand Portal.
* Correcciones en el valor de Resourcetype en el nodo de lienzo.
* Se ha habilitado la funcionalidad de búsqueda de caracteres especiales y distinción entre mayúsculas y minúsculas para el contenido de fragmentos de documento.
* Forms adaptable mejorado para adjuntar archivos PDF como archivos adjuntos en Safari.\
   Proporciona un nuevo Dynamic Media que se conecta a la nueva Dynamic Media Publishing Infrastructure para una replicación más rápida y escalable.

### Recursos {#assets-10}

* AEM Assets no puede extraer referencias de subrecursos para recursos de InDesign que incluyen vínculos de duplicado al recurso. NPR-19006: revisión para CQ-4204186
* La opción Ordenar no funciona para los recursos dentro de la colección en Comercio. NPR-19508: revisión para CQ-4213622
* Cuando un recurso con el mismo nombre que un recurso preexistente se mueve a la misma ubicación, el valor de cq: lastReplicationAction para los recursos se intercambia entre ellos, lo que provoca la creación de metadatos incorrectos. NPR-19531
* Se muestra un mensaje de error al publicar un gran número de recursos, a pesar de que todos los recursos se hayan publicado correctamente. NPR-19629: revisión para CQ-4219611
* Las representaciones estáticas se muestran con dimensiones fijas y no reflejan el tamaño de la representación real. NPR-20004
* La instancia de AEM se vuelve lenta cuando se publican varios recursos (más de 4) en Brand Portal. NPR-20009

### Sitios {#sites-10}

* AEM muestra un comportamiento inesperado cuando un usuario intenta publicar /cancelar publicación/crear versión de una página bloqueada por otro usuario. NPR-19249; Revisión para CQ-4215298 y CQ-4203856
* Al promocionar el lanzamiento anidado manualmente, la página secundaria se está eliminando. NPR-19704
* Problemas de persistencia cuando ContextHub almacena la superposición de la capa de persistencia predeterminada durante la inicialización. NPR-19979: revisión para CQ-4218399
* Los fragmentos de contenido se superponen con otros botones. NPR-19980: revisión para CQ-4221519
* La página del sitio no se muestra cuando se ve con un alias en SiteAdmin. NPR-20053: revisión para CQ-4221478
* Error al publicar una página de Live Copy que apunta a una página de importador en campañas de Adobe. NPR-20066: revisión para CQ-4220846

### Plataforma {#platform-8}

* Se ha actualizado Apache POI a la versión 3.16 para admitir la inclusión de imágenes de fondo de diapositivas PPT en las representaciones. NPR-18286
* Se han producido problemas de procesamiento con Internet Browser 11 y Edge al cargar varios recursos en la misma carpeta. NPR-20062

### Integración {#integration-11}

* El archivo at.js personalizado no se publica cuando se accede al mismo con el usuario anónimo. NPR-19542: revisión para CQ-4219592
* Migración de las credenciales existentes de Analytics a la autenticación WSSE. NPR-19962

### Brand Portal {#brand-portal}

* Habilitar las etiquetas de publicación de AEM a Brand Portal desde la consola de administrador de etiquetas/etiquetado. NPR-20271

## Forms {#forms-11}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms  {#forms-add-on-package-11}

#### Administración de correspondencia {#correspondence-management-4}

* Funcionalidad habilitada para buscar texto real en fragmentos de documento cuando se obtiene una vista previa de una carta. NPR-19712

#### Formularios adaptables {#adaptive-forms-8}

* Forms adaptable mejorado para adjuntar archivos PDF como archivos adjuntos en Safari. Para admitir la misma capacidad en los formularios existentes, necesitamos realizar el cambio en la configuración en el widget de datos adjuntos y en &quot;Tipos de archivos admitidos&quot; actualizar el valor application/pdf en lugar de .pdf. NPR-19623

#### Administrador de Forms {#forms-manager-1}

* Si validationState es undefined en un campo de formulario adaptable y se produce el evento elementFocusChanged, se devuelve un evento de error (errorState) al servidor de Adobe Analytics. NPR-19513

### Instalador JEE de Forms {#forms-jee-installer-11}

#### Núcleo {#core-3}

* El administrador de conexiones no está disponible durante el apagado. Jleader corta la dependencia de JDBC antes de que el autor EAR sea desdesplegado causando problemas de corrupción. NPR-19703

## Paquetes de funciones incluidos {#feature-packs-included-1}

* Corrección de miniaturas y mejoras de transparencia en Dynamic Media. NPR-15207

## Paquetes OSGI y paquetes de contenido incluidos en CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

Lista de paquetes de contenido actualizados en AEM 6.2SP1-CFP9

[Obtener archivo](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Lista de paquetes OSGi actualizados en AEM 6.2SP1-CFP9

[Obtener archivo](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Introducción de etiquetas a plantillas de usuario personalizadas en el servicio de plantillas de correo electrónico de Adobe.
* Mejoras en los botones TouchUI de la aplicación de escritorio.
* Se ha deshabilitado el botón de envío al hacer clic para evitar que se envíen varios formularios en una página de traducción.
* Se configuraron varios componentes RTE en un cuadro de diálogo.
* Refuerzo de ReferenceUpdates en Live Copy.
* Se ha habilitado la funcionalidad de búsqueda que distingue entre mayúsculas y minúsculas para el contenido de fragmentos de documento.
* Lista añadida de las bibliotecas Linux a la documentación de instalación de AEM Forms.

### Recursos {#assets-11}

* Problemas con la aplicación del filtro Omnisearch en colecciones inteligentes en el navegador Safari. NPR-19511
* Los metadatos de palabra clave PDF no se extraen ni modifican correctamente cuando hay varias palabras clave asociadas a un recurso PDF. Para resolver el problema, se ha eliminado la propiedad de metadatos del campo Asunto de los recursos PDF. Sin embargo, puede editar el esquema de metadatos para agregar un campo de texto de varios valores para el campo Asunto. NPR-19126
* El servicio de notificación de flujo de trabajo no codifica los vínculos del correo electrónico, lo que impide que se carguen después de que los usuarios hagan clic en ellos. NPR-19490: revisión para CQ-4218055
* No se puede cargar la lista completa de páginas/recursos en la vista de columna al usar Chrome. NPR-19458: revisión para CQ-4214248
* El icono Tiempo de inactividad incorrecto se muestra en AEM bandeja de entrada al activar el flujo de trabajo &quot;Solicitud de Activación&quot;. NPR-19365: CQ-4216174
* Problemas con la ordenación en la vista de listas. NPR-19217: CQ-95602
* Al cambiar el título o la imagen en miniatura en la configuración de la carpeta de recursos, se anulan el grupo y los permisos originales de la carpeta. NPR-19283: revisión para CQ-4216080
* Las estaciones de trabajo de Windows 10 cambian automáticamente al modo de toque, desactivando el funcionamiento de algunos de los botones. NPR-19183

### Sitios {#sites-11}

* Problemas con la presencia de varios componentes RTE en un cuadro de diálogo. NPR-19311: NPR-19587.
* La depuración automática de versiones en vainilla AEM 6.2 solo funciona una vez después de que se inicialice VersionManagerImpl. NPR-19315: revisión para CQ-4217175
* La instancia de flujo de trabajo se queda atascada en el paso de flujo de trabajo &quot;Salesforce.com Export&quot;. NPR-19222: revisión para CQ-4212976
* Las páginas de copia de idioma creadas a partir de copias en vivo no son editables. NPR-18967
* ReferencesUpdateAction no puede actualizar los vínculos en un LiveCopy anidado con cambio de jerarquía. NPR-18715: revisión para CQ-4214105

### Plataforma {#platform-9}

* El servicio Plantilla de correo electrónico de Adobe agrega etiquetas a las plantillas de usuario personalizadas. NPR-19190: revisión para CQ-4217113

### Proyectos {#projects-2}

* Los editores de proyectos no pueden copiar/pegar recursos en la carpeta de recursos del proyecto. NPR-19619
* No se puede generar la previsualización para proyectos de traducción después de instalar 6.2 SP1-CFP1. NPR-16481: CQ-4204655

### Integración {#integration-12}

* Obtenga acceso a las propiedades de los artículos que se establecen incorrectamente en la solución de publicación digital de Adobe en la IU clásica. NPR-19366
* Representación lenta de las miniaturas debido a artículos de tamaño completo en AEM consola de artículos. NPR-19086: CQ-4217148
* Comportamiento incorrecto del plegado automático al personalizar las ofertas a través de Campaign si los usuarios tienen acceso a varias áreas. NPR-19290: revisión para CQ-4218029
* El cuadro de diálogo de destino no se muestra en el modo de segmentación cuando se edita un módulo de destino y se guarda más de una vez. NPR-19144: revisión para CQ-4216708

### Flujo de trabajo {#workflow-2}

* Los usuarios no pueden filtrar las notificaciones en la Bandeja de entrada por usuario o grupo en la interfaz de usuario de la Bandeja de entrada clásica. NPR-19122: revisión para CQ-4215374
* El mapa de imagen no conserva las coordenadas seleccionadas en el componente de imagen HTML. NPR-18911: CQ-4211584

## Forms {#forms-12}

* Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-12}

* Cuando el contenido se copia desde Microsoft Word o un explorador Web al editor de texto del administrador de correspondencia, el estilo se pierde. NPR-19530
* El contenido sin salto de línea del Editor de texto no se ajusta. NPR-19481
* Funcionalidad habilitada para buscar texto real en fragmentos de documento cuando se obtiene una vista previa de una carta. NPR-17792: revisión para CQ-4214501

#### Administración de correspondencia {#correspondence-management-5}

>[!NOTE]
>
>Esta funcionalidad de búsqueda de fragmentos de texto tiene algunas restricciones:-
>
>* El contenido de los fragmentos de documento distingue entre mayúsculas y minúsculas y los títulos no distinguen entre mayúsculas y minúsculas.
>* Los resultados de la búsqueda no se resaltan cuando parte de la palabra buscada tiene un estilo diferente o contiene caracteres especiales como &quot; o &#39; o \.
>* La búsqueda no funciona para contenido dinámico (como valores de elementos del diccionario de datos o valores de variables) dentro del fragmento de documento.


#### Administrador de Forms {#forms-manager-2}

* Las propiedades de Esquema XML de Forms adaptable no se pueden editar después de aplicar CFP6 en AEM 6.2. Revisión para CQ-4219684
* Todos los servicios del paquete principal de AEM Forms Manager no se inician al reiniciar el servidor. Revisión para CQ-4217014

### Instalador JEE de Forms {#forms-jee-installer-12}

#### Instalación de LCM {#install-lcm-2}

* La pantalla Administrador de Microsoft Windows muestra la versión número 6.0 después de instalar CFP6. Revisión para CQ-4217573

## Paquetes de funciones incluidos {#feature-packs-included-2}

* Mejoras en los botones TouchUI de la aplicación de escritorio. NPR-18676

## Paquetes OSGi incluidos en CFP8 {#osgi-bundles-included-in-cfp}

Lista de paquetes OSGi actualizados en AEM 6.2SP1-CFP8

[Obtener archivo](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Lista de paquetes de contenido actualizados en AEM 6.2SP1-CFP8

[Obtener archivo](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Cambio de comportamiento en la visualización de títulos en la tarjeta de imagen para una imagen que tiene dc: propiedad title establecida en String [] (multifield).
* Correcciones en el problema de rendimiento con Cloud Services de Dynamic Media, IU táctil e interfaces de usuario de seguridad.
* Correcciones en Apache Felix Http Bridge 3.0.8
* Se ha resuelto la replicación sin binarios (BLR) entre el entorno de creación y publicación.
* Compatibilidad con archivos de la biblioteca de destinatarios, AT.JS, una biblioteca de implementación para la integración del cliente con Adobe Target diseñada tanto para implementaciones web típicas como para aplicaciones de una sola página.
* Se ha mejorado el rendimiento AEM al introducir un período de tiempo de espera de conexión configurable por el usuario para las soluciones de Marketing Cloud (Analytics, DTM, Destinatario y S&amp;P).

### Recursos {#assets-12}

* Al probar la ingestión de vídeo con AEM 6.3 configurado con Cloud Services de Dynamic Media, se produce la excepción &quot;Demasiados archivos abiertos&quot;. NPR-18734; Revisión para CQ-4211407
* La configuración de URL de vanidad para los recursos de una página no funciona después de reiniciar la instancia de AEM. NPR-18634; Revisión de Granite-18085
* En TouchUI, el botón Publicar se muestra para los usuarios sin permiso para publicar recursos. NPR-18620; Revisión para CQ-4214042
* La opción de representación dinámica no está presente en el cuadro de diálogo de descarga de un recurso una vez que el contrato de licencia se ha establecido para él. NPR-18607; Revisión para CQ-4212342
* No se puede descargar la representación dinámica para los recursos que incluyen espacios en sus nombres. NPR-18571; Revisión para CQ-4211738
* No se puede guardar más de un usuario al compartir la carpeta de recursos con Creative Cloud. NPR-18489; Revisión para CQ-103297
* dc: title &amp; dc: description no cambia a un valor de varios campos en crx/de. NPR-18474; Revisión para CQ-4209086
* La operación de mover recursos causa una degradación del rendimiento. NPR-18346
* No se muestran elementos en la línea de tiempo cuando se abre con el conjunto de opciones predeterminado Mostrar todo. NPR-18302; Revisión para CQ-4211957
* Se produce un error cuando se carga un archivo de texto codificado ASCII/UTF-8 en AEM Assets y falla la generación de miniaturas. NPR-18006: CFP para CQ-4209345
* Los botones de acción Publicar están visibles incluso cuando el usuario no tiene acceso replicado. NPR-17353; Revisión para CQ-4209269
* Tanto Siteadmin como Miscadmin no funcionan cuando la minimización está habilitada usando min:gcc;obfuscate=true. NPR-18593; Revisión para CQ-4209220
* Los elementos de menú personalizados no aparecen hasta que la pantalla se actualiza cada vez. NPR-18500; Revisión para CQ-4213581
* Actualice time.js a 2.10.6. NPR-18596; Revisión de Granite-11881
* La aplicación de permisos para macros DM rompe la vista para el usuario administrador. NPR-18544; Revisión para CQ-4211729
* Publicar más tarde para recursos está generando una excepción ArgumentException no válida. CQ-4214532

### Sitios {#sites-12}

* En un clúster de autores activo-activo con MongoDB, ambos autores intentan activar la replicación para el mismo contenido, cuando el tiempo alcanza el valor de tiempo de activación establecido para el contenido. NPR-18708; Revisión para CQ-4210982
* NPE al mover un recurso con una referencia que no tiene jcr: nodo de contenido. NPR-18664
* Los marcadores de posición no están visibles en una página que contiene varios componentes parsys. NPR-18645; Revisión para CQ-110253
* Problemas de concurrencia en AbstractCopyMoveCommand. NPR-18591
* Al copiar texto a un componente parsys desde otra instancia de AEM, parsys se crea sin ningún resourceType establecido. NPR-18511; Revisión para CQ-4212306

### Plataforma {#platform-10}

* El instalador de JCR no actualiza la versión del paquete después de la instalación del paquete. NPR-18728; Revisión para NPR-15135
* La replicación sin binarios (BLR) falla con entornos de creación y publicación de binarios. NPR-18704
* Solicitud de resolución del puente HTTP Apache Felix en AEM entorno. NPR-18297
* La replicación falla cuando varias páginas con una estructura similar se replican simultáneamente con Sling Content Distribution. NPR-18665; Revisión de Granite-13712
* Paquetes de distribución Sling que se acumulan y no se limpian automáticamente. NPR-18601; Revisión de Granite-16183

### Integración {#integration-13}

* La visualización de ofertas publicadas desde carpetas de biblioteca resulta en NPE. NPR-18732; Revisión para CQ-4214593
* La fecha de inicio/finalización de una actividad no se actualiza en JCR y Destinatario cuando se cambia de una fecha específica a &quot;Al activarse/desactivarse&quot;. NPR-18612; Revisión para CQ-104831
* La integración de Analytics con AEM no tiene ningún tiempo de espera de conexión o de socket establecido para las conexiones httpclient. NPR-18497
* La integración de DTM con AEM no tiene ningún tiempo de espera de conexión o de socket establecido para las conexiones de httpclient. NPR-18495
* La integración de Destinatario con AEM no tiene ningún tiempo de espera de conexión o de socket establecido para las conexiones httpclient. NPR-18494
* La integración de Search &amp; Promote con AEM no tiene ningún tiempo de espera de conexión o de socket establecido para las conexiones de cliente httpclient. NPR-18493
* La actividad de destinatario se desactiva después de añadir una experiencia adicional. NPR-18227; Revisión para CQ-4201895

### WCM: componentes base {#wcm-foundation-components-7}

* Los mapas de imagen no conservan las coordenadas seleccionadas en el componente de imagen HTML. NPR-18530; Revisión para CQ-4211584

### Traducción {#translation-5}

* Los resultados de la búsqueda de traducción no incluyen nombres de proyectos de traducción. NPR-18224; Revisión para CQ-4210658

### Brand Portal {#brand-portal-1}

* Habilitar las etiquetas de publicación de AEM a Brand Portal desde la consola de administrador de etiquetas/etiquetado. CQ-4212165

## Forms {#forms-13}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-13}

#### Administración de correspondencia {#correspondence-management-6}

* Los datos correctos no se muestran en el panel de edición hasta que se guarda el fragmento. NPR-19092
* Añadir fragmento de documento en una carta lleva mucho tiempo. NPR-18958
* Si existe una declaración XML en un archivo XML de datos y la representación de letras se inicia mediante una solicitud de POST, la letra correspondiente no muestra los datos. NPR-18870
* No se generan registros de auditoría para las acciones realizadas en los recursos de CM. NPR-16618

>[!NOTE]
>
>No instale este paquete Añadido de CFP si tiene algún impacto en los dos problemas siguientes:
>
>* Copiar pegar desde Word/Web en el Editor de texto de CM muestra el contenido de salto de línea. NPR-19530
>* El contenido sin salto de línea en el Editor de texto de CM no se ajusta. NPR-19449

>
>
Estas cuestiones se abordarían en la futura política pesquera común.

#### Formularios adaptables {#adaptive-forms-9}

* Al agregar un nuevo panel para paneles repetitivos, se elimina el valor del campo desplegable del panel anterior. NPR-18772
* Los campos de formulario adaptables marcados para aceptar sólo enteros también aceptan algunos caracteres especiales del teclado numérico. NPR-18680
* La secuencia de comandos para cambiar el título del botón en el evento de inicialización del panel de guía no funciona. NPR-18476
* La barra de desplazamiento no se ve en el panel derecho para las reglas creadas con el editor de reglas. NPR-18716

#### Aplicación de AEM Forms {#aem-forms-app}

* Forms no se representa correctamente en la aplicación de AEM Forms cuando está en modo sin conexión o no conectado a la red. CQ-4218368

### Instalador JEE de Forms  {#forms-jee-installer-13}

#### Servicio PDFG {#pdfg-service-3}

* El generador de PDF no produce documentos PDF con niveles de marcadores especificados. Revisión para CQ-4211102

## Paquetes OSGi incluidos en CFP7 {#osgi-bundles-included-in-cfp-1}

Lista de paquetes OSGi actualizados en AEM 6.2SP1-CFP7

[Obtener archivo](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Lista de paquetes de contenido actualizados en AEM 6.2SP1-CFP7

[Obtener archivo](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Administración eficaz de los componentes ocultos en el modo de diseño en tabletas.
* Introducción a Quickactions en dispositivos híbridos.
* Resolución de problemas de sincronización a nivel de componente con copias en vivo.

### Recursos {#assets-13}

* El cliente se bloquea cuando un usuario que no tiene el permiso necesario intenta mover una operación en un recurso. NPR-18330; Revisión para CQ-4212560
* La combinación de varias configuraciones de servicios de contenido inteligente causa problemas de uso. NPR-18273; Revisión para CQ-4201557
* Las acciones o Flujos de trabajo de cierre de compra no están disponibles desde la consola Línea de tiempo una vez aproximadamente. Se añaden 80 fragmentos en la carpeta Recursos. NPR-18257; Revisión para CQ-4211214 y NPR-18251; Revisión para CQ-4211216.
* El sistema se bloquea en Memoria insuficiente y no se pagina durante los informes de Recursos. NPR-17865; Revisión para CQ-4209759
* El vídeo publicado no se reproduce en un recurso de vídeo codificado. NPR-17849; Revisión para CQ-4210739
* La miniatura para PDF no se genera. NPR-17831, NPR-17750; Revisión para CQ-4210547
* El trabajo de notificación de caducidad de Adobe CQ DAM no desactiva los recursos caducados. NPR-17666; Revisión para CQ-107766
* Las actividades de caducidad de recursos se detienen si un recurso no tiene un propietario asignado. NPR-17665; Revisión para CQ-4197946
* Se genera una excepción de puntero nulo cuando se mueve una carpeta de recursos con más de 150 referencias entrantes. CQ-4200981

### Sitios {#sites-13}

* La personalización solo funciona para la primera IP cuando la regla de segmentación está establecida para un intervalo de IP. NPR-18121; Revisión para CQ-83767
* El inicio de sesión falla debido a NumberFormatException cuando la propiedad historyShow está habilitada. NPR-18073; Revisión para CQ-101965
* Las páginas eliminadas marcadas son visibles en la IU táctil. NPR-18025; Revisión para CQ-86694
* Problemas de rendimiento al cargar una página con audiencias grandes (más de 2000). NPR-17884; Revisión para CQ-4209567
* No se puede seleccionar una imagen después de quitar otras imágenes de la página. NPR-17711; Revisión para CQ-4201323

### Plataforma {#platform-11}

* Los controles de IU táctil no están ocultos para los usuarios que no tienen los permisos necesarios. NPR-17945; Revisión para CQ-4211231
* Faltan etiquetas japonesas en el campo de selección de etiquetas. NPR-17768; Revisión para CQ-4210456
* La consulta getsize() devuelve resultados incorrectos cuando FastQuerySize está habilitado. NPR-18018
* No se puede acceder a la consola web en la instancia de espera. NPR-17861; Revisión para Granite-14582

### Comercio {#commerce-2}

* La inversión de consulta se produce cuando el modelo de catálogo no tiene ninguna condición definida para una sección. NPR-18229; Revisión para CQ-4211924

### Comunidades {#communities-2}

* PollingImporterImpl. retrasa AEM cierre. NPR-18298; Revisión para CQ-96133

### Integraciones {#integrations}

* Se han resuelto los errores de componentes de AEM Search que se pueden producir cuando el OSGI de AEM Day HTTP Client 3.1 se configura con un proxy que requiere autenticación implícita. NPR 18128
* Falta la casilla de verificación para revertir la herencia. NPR-17753; Solicitud de revisión para CQ-4210139
* Los usuarios no pueden configurar la prioridad al destinar un componente con varias actividades. NPR-18658; Revisión para CQ-4210727
* Los usuarios no pueden examinar la carpeta /etc/segmentation para seleccionar una audiencia creada en la carpeta /etc/segmentation/group1. NPR-18522

### Seguridad {#security-1}

* El Asistente para mover recursos se bloquea si el usuario no tiene permiso de escritura en la carpeta destinatario. NPR-18300
* Solicite utilizar una versión actualizada del servelet org.apache.sling.servlets.post (2.3.22) en la API de Apache Sling para evitar una vulnerabilidad XSS. NPR-18963

### Traducción {#translation-6}

* No se debe permitir que la página de recursos se vuelva a enviar a un proyecto de traducción hasta que se complete el proyecto. NPR-18249; Revisión para CQ-4209908

### WCM: componentes base {#wcm-foundation-components-8}

* No se puede usar el componente iparsys de base de WCM en plantillas editables. NPR-18223; Revisión para CQ-4210384
* El mapa de imagen no conserva las coordenadas seleccionadas en el componente de imagen HTML. NPR-18032; Revisión para CQ-4211584
* Cuando se procesa un componente de imagen HTL, se cambia el nombre del nombre del nombre del archivo en la dirección URL, lo que provoca que se rompan las direcciones URL. NPR-17908; Revisión para CQ-4211587
* No se puede salir de Propiedades de página después de realizar los cambios. NPR-17832; Revisión para CQ-96110

## Forms {#forms-14}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-14}

**Administración de correspondencia**

* El diccionario de datos se lee repetidamente durante la representación de letras. NPR-18482, revisión para CQ-4210805
* Se ha añadido JavaDocs para la clase com.adobe.livecycle.content. NPR-18467
* Al crear una carta, la descripción de la carta no se guarda. NPR-18039
* Cuando se guarda un módulo de texto y una expresión del módulo de texto no contiene etiquetas de expresión de apertura o de cierre, no se muestra ningún mensaje de error. El módulo de texto muestra un mensaje de error y no se procesa en la carta. NPR-17798
* Errores inesperados en los registros de la instalación del paquete de complemento. NPR-18295

**Administrador de Forms**

* La interfaz de usuario de AEM Forms muestra todos los recursos por orden de antigüedad. Los usuarios no pueden alterar el orden para colocar los recursos más recientes primero. NPR-18451

### Instalador JEE de Forms  {#forms-jee-installer-14}

**Servicio de salida**

* Se ha mejorado el problema de rendimiento del servicio Output para AEM formularios 6.2. NPR-18033

**Servicio de firmas**

* No se puede firmar un documento PDF con el módulo de seguridad de hardware remoto. NPR-18017

## Paquetes OSGi incluidos en CFP6 {#osgi-bundles-included-in-cfp-2}

Lista de paquetes OSGi actualizados en AEM 6.2SP1-CFP6

[Obtener archivo](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Lista de paquetes de contenido actualizados en AEM 6.2SP1-CFP6

[Obtener archivo](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Se han resuelto varios problemas de la interfaz de usuario con el uso compartido, el desplazamiento, la publicación y la descarga de recursos.
* Se ha aumentado la capacidad del cuadro de diálogo Mover para mostrar los recursos a los que se hace referencia.
* Se han resuelto varios problemas relacionados con los componentes y flujos de trabajo de WCM, como Cancelar publicación y Depurar versión.
* Se ha mejorado la capacidad de respuesta de la barra de acciones con respecto a la visualización de acciones de la barra de herramientas y componentes de Coral.

### Recursos {#assets-14}

* Mejoras de rendimiento en la funcionalidad de publicación en Brand Portal. NPR-17189; Revisión para CQ-4204150
* Al compartir un recurso mediante la opción Compartir vínculo, no se crea un archivo zip con una estructura de carpetas plana para la descarga. NPR-17513; Revisión para CQ-4209381
* Al seleccionar un recurso en DAM y hacer clic en Publicar, no se muestra la opción Publicar en Brand Portal en la página Detalles del recurso. NPR-17351; Revisión para CQ-94905
* En los pasos del flujo de trabajo de DAM, los flujos binarios adquiridos desde Session o ResourceResolver deben cerrarse en un bloque final para garantizar que no se produzcan fugas de recursos. NPR-17385; Revisión para CQ-4209452
* Al cargar un documento de Word en DAM, se produce una excepción de puntero nulo y la instancia de workflow permanece atascada en el estado de ejecución. NPR-17160; Revisión para CQ-4207358
* Los botones Compartir, Mover, Publicar y Descargar están visibles para los recursos caducados en la página Editor de metadatos para los usuarios no administradores. NPR-16903; Revisión para CQ-101440/CQ-104535
* Las acciones como Compartir, Mover, Publicar y Copiar deben estar visibles para los usuarios administrativos en la consola Recursos. NPR-16902; Revisión para CQ-4207111

### Sitios {#sites-14}

* Al mover una página mediante la IU clásica y táctil, el cuadro de diálogo Mover no muestra referencias superiores a 150, lo que impide que los usuarios actualicen estas referencias y vuelvan a publicar la página. Este problema se ha corregido introduciendo una propiedad para la IU clásica: &#39;maxRefNo&#39; que se puede configurar en el nodo siteadmin: &#39;/libs/wcm/core/content/siteadmin&#39;. Esta propiedad especifica el número máximo de referencias (valor predeterminado 150) que se muestran antes de una operación de movimiento intensivo y, si una página tiene más número de referencias, no se muestran en el cuadro de diálogo movePage. Esta configuración también funciona para damadmin y miscadmin mediante la aplicación de la configuración en los nodos: `'/libs/wcm/core/content/damadmin'` y `'/libs/wcm/core/content/miscadmin'` respectivamente. NPR-17222; Revisión para CQ-85878

* Al trabajar con componentes de WCM, los hipervínculos con espacios se eliminan en el Editor de texto enriquecido de la IU táctil. NPR-17698, NPR-17570; Revisión para CQ-4206768
* Al activar el flujo de trabajo Solicitud de cancelación de publicación desde las propiedades de página, aparecen errores de JavaScript para los usuarios sin derechos de replicación. NPR-17294; Revisión para CQ-102064
* Al procesar o exportar un componente de imagen HTL, la URL cambia a un número y se cambia el nombre del archivo, lo que provoca que se rompan los vínculos. NPR-17245; Revisión para CQ-59616
* Al eliminar un inicio en un lanzamiento anidado, los subinicios quedan huérfanos. NPR-17228; Revisión para CQ-4202639
* La ejecución de la depuración de versiones en AEM 6.2 con Oak 1.4.13 aplicado provoca una advertencia repetida constantemente en los registros. NPR-17391; Revisión para CQ-4206870
* Después de instalar una revisión o una actualización para el componente ContextHub, el paquete de contenido sobrescribe todos los segmentos en /etc/segmentation/contexthub, lo que resulta en una pérdida de todos los segmentos personalizados de ContextHub. NPR-17250; Revisión para CQ-79958
* Al ejecutar un flujo de trabajo con grupos anidados como usuarios del flujo de trabajo, WorkflowStatusProvider (pageinfo.json) hace que la instancia del flujo de trabajo se bloquee. NPR-17555; Revisión para CQ-4202056
* Al utilizar los componentes del editor de páginas WCM, existe una gran cantidad de espacio vacío al final de la página en el modo de edición de la IU táctil de la instancia de autor. NPR-17510; Revisión para CQ-4205441
* Al procesar o exportar un componente de imagen HTML, la URL cambia a un número, lo que provoca que se rompan los vínculos. NPR-17245; Revisión para CQ-59616

### IU {#ui}

* Al seleccionar un recurso y hacer clic en Herramientas de desarrollador, no siempre se muestran las acciones de la barra de acciones en conexiones lentas y la página debe volver a cargarse. NPR-17568; Revisión para CQ-108365
* La barra de acciones debe actualizarse para utilizar dos contenedores: coralino-bar-primario y coralino-bar-secundario, en lugar de coralino-bar-contenedor. NPR-17591; Revisión para GRANITE-15225

### Móvil bajo demanda {#mobile-on-demand-2}

* Los usuarios con permisos de &quot;solo lectura&quot; en la aplicación de AEM Mobile no pueden realizar previsualizaciones del contenido desde la página de AEM Mobile Gestor de contenido. NPR-17390; Revisión para CQ-4209690

### Seguridad {#security-2}

* Vulnerabilidad XSS en la salida generada por HTMLRendererServlet. NPR-17136
* Solicitud para evitar que se divulgue AEM versión en AEM página Fuentes de distribución web. NPR-16219

### Forms {#forms-15}

#### Paquete de complemento de Forms {#forms-add-on-package-15}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

**Formularios adaptables**

* Para un formulario adaptable con datos adjuntos, las entradas de duplicado para las etiquetas afSubmissionInfo se crean en el XML enviado cuando el formulario se envía por segunda vez. NPR-17364
* Cuando se utiliza el navegador Google Chrome, después de quitar un archivo adjunto de un formulario, al intentar volver a adjuntarlo se genera un error. NPR-17297
* En caso de que haya paneles anidados y repetitivos cargados a medida en Forms adaptable basado en XSD o en modelo sin formulario, los valores rellenados en el formulario no se conservarán en el Documento de registro (DOR). NPR-17176
* Los errores mostrados en el registro de errores del Editor de reglas deben agregarse en el bloque catch de un código JavaScript de bloque try/catch. NPR-16757
* Al hacer clic en un archivo adjunto en un formulario, se produce un error en la consola del explorador y no se muestra la previsualización de datos adjuntos. NPR-17174

**Administración de correspondencia**

* La funcionalidad Crear interfaz de usuario de correspondencia se interrumpe en caso de que se añada texto en línea o una línea en blanco en la interfaz de usuario. NPR-17748
* El navegador parpadea cuando se abre una carta para editarla. NPR-17576
* Al agregar funciones remotas en elementos del diccionario de datos calculados, si el número de funciones es superior a la longitud de la ficha que muestra funciones remotas, la barra de desplazamiento no aparece en la ficha. NPR-17359
* El método API, import com.adobe.icc.services.api.LetterInstanceService no funciona. NPR-17922, NPR-16008
* Una variable agregada en un módulo de texto no está visible en el panel Enlace de datos mientras se edita una letra. NPR-17940
* La interfaz de usuario de Correspondence Management no se inicia cuando la acción de envío HTML utiliza el método POST. NPR-17595

**Administrador de Forms**

* Con un formulario adaptable configurado para la prueba A/B, al hacer clic en Prueba A/B de Inicio no se inicio la prueba y se genera un error de consola del explorador. NPR-17838

**Servicio de Forms**

* Deben corregirse los problemas notificados en la análisis de código estático de los formularios OSGI. NPR-13951

#### Instalador JEE de Forms {#forms-jee-installer-15}

**Servicio de salida**

* El uso de AEM Forms 6.2 Output Service para combinar un formulario específico con un XML de datos tarda 20 veces más tiempo que el tiempo que tarda el servidor LiveCycle ES4 SP1 en la misma operación. Se corrige en entornos de Windows y Linux. NPR-17501

**Instalación de LCM**

* Después de instalar AEM Forms 6.2 GM y aplicar el CFP AEM 6.2, al ejecutar LiveCycle Configuration Manager se muestra un punto y coma no deseado en la Información de la versión y la fecha de instalación del parche no se actualiza. NPR-14322

**Administración de procesos**

* La variable TaskContext no se rellena para los procesos de AEM Forms. CQ-4211857

#### Paquete JEE de AEM Forms {#aem-forms-jee-bundles-package}

* Las capacidades de los usuarios de formularios, tanto si utilizan la consola de la interfaz de usuario de administración de JEE como la consola OSGi, deben ser las mismas. NPR-17670

### Paquetes de funciones incluidos en CFP5 {#feature-packs-included-in-cfp}

**Paquete Forms JEE**

Administración de procesos - Espacio de trabajo HTML

* Al asignar un paso de espacio de trabajo, la ficha Archivos adjuntos del espacio de trabajo debe mostrar un contador para los datos adjuntos o las notas en caso de que haya más de un adjunto o nota. NPR-17771
* Solicite soporte técnico para Office 365 en AEM JEE Forms para funciones de correo electrónico en el flujo de trabajo del formulario. NPR-13866

**Paquete Añada de Forms**

Administración de correspondencia

* Durante la edición de fragmentos en el editor de texto durante una previsualización de letras, el texto procesado debe mostrarse para su edición en lugar de las condiciones en línea utilizadas en los fragmentos. NPR-15748, NPR-17504

### Paquetes OSGi incluidos en CFP5 {#osgi-bundles-included-in-cfp-3}

Lista de paquetes OSGi actualizados entre AEM6.2 SP1-CFP5

[Obtener archivo](assets/do-not-localize/cfp5_osgi_bundles.txt)

Lista de paquetes de contenido actualizados entre AEM6.2 SP1-CFP5

[Obtener archivo](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 es una actualización importante que incluye correcciones clave de cliente realizadas tras la disponibilidad general de AEM 6.2 SP1.

Los aspectos destacados de este paquete de correcciones acumulativas son:

* Correcciones en los recursos para la representación Camera Raw de archivos, la vista de la línea de tiempo y la orientación de la imagen
* Mejora en

   * WCM se inicia en los sitios
   * Flujo de trabajo de proyectos
   * Componentes de ContextHub

* Correcciones de Campaña, Móvil a petición y Traducción
* Mejoras de uso en el Editor de reglas de formularios adaptables
* Editor de condiciones en línea mejorado para la administración de correspondencia en formularios
* Correcciones de administración de procesos y servicios de salida para formularios AEM en JEE
* Corrección relacionada con Forms Designer para el Editor de secuencias de comandos

### Plataforma {#platform-12}

* El formulario de búsqueda de Search&amp;Promote ignora la configuración `environment` cuando se configura el servicio en la nube, lo que hace que no se pueda utilizar en la instancia de creación. NPR-16594: revisión para CQ-4206076
* No funciona añadir o personalizar columnas en los **recursos que OmniSearch** genera al superponer en /apps. NPR-16737: revisión para CQ-4206785
* La **herramienta de diagnóstico **página no funciona después de una actualización in situ de AEM 6.1 SP2 a AEM 6.2 SP1. NPR-17121; Revisión para CQ-4196786
* HTL: Al seleccionar un foro, crear un tema y una publicación, la `Sightly SightlyCompiledScript` agrega una propiedad `addSelectors` incorrecta a `RequestDispatcherOption`. NPR-17008: revisión para GRANITE-16384

* Compatibilidad añadida para `CRON expressions` en `ManagedPollConfigs` utilizada por `ReportImporter`. NPR-16608: Solicitud de revisión para CQ-4206066

* Error al cargar una imagen de avatar para un usuario LDAP. NPR-16561; Revisión de Granite-17013
* El número de resultados mostrados en la pantalla Administración de usuarios es diferente en la vista de tarjetas y Listas. NPR-16241; Revisión para GRANITE-16914
* Las notificaciones de flujo de trabajo no se cargan de forma diferida mientras se visualizan en el navegador Google Chrome en modo de pantalla completa. NPR-17013: revisión para CQ-4207567

### Recursos {#assets-15}

* La orientación de la imagen no se aplica correctamente al importar una imagen con una orientación definida. NPR-16750: revisión para CQ-4204356
* La vista de línea de tiempo de recursos no muestra ningún recurso aunque &quot;Mostrar todo&quot; esté definida de forma predeterminada. NPR-16957: revisión para CQ-98780
* Los archivos sin procesar de cámara (incluidos ARW, CR2, NEF, DNG y EPS) cuando se agregan como representación en los recursos, no se pueden seleccionar ni eliminar. Estos archivos se descargan automáticamente cuando el usuario hace clic en ellos. NPR-16949: revisión para CQ-4206846
* La creación de un PDF dentro de otro PDF en la interfaz de usuario de Assets no muestra los archivos PDF creados en la interfaz de usuario de DAM, aunque estos están visibles en el repositorio crx. NPR-16833: revisión para CQ-4206501
* La carga de un recurso como nodo secundario directo por sí mismo mediante la IU táctil provoca un problema. El recurso se carga como elemento secundario directo del recurso seleccionado anteriormente. NPR-16534: revisión para CQ-4204287
* En la interfaz de usuario de DAM, comentar un recurso y etiquetar a un usuario en el comentario no genera una notificación por correo electrónico. NPR-16589: revisión para CQ-102318

### Proyectos {#projects-3}

La consola de flujo de trabajo de proyectos muestra una excepción NullPointerException en la página cuando se purgan flujos de trabajo. NPR-17017: revisión para CQ-4194269

### Sitios {#sites-15}

* Los archivos de `ContextHub` no se minimizan en la instancia de creación. NPR-17022: revisión para CQ-79456
* La promoción de inicio de WCM-Launches tarda mucho tiempo en promocionar un lanzamiento que consta de un árbol grande de una página. NPR-16480: revisión para CQ-82731
* `ClientContext` El procesador de condiciones de segmento se bloquea cuando se crea un segmento (o audiencia) con una regla que no funciona o que no ha terminado. NPR-16759: revisión para CQ-4205104
* En los inicios de WCM, las páginas asociadas con un lanzamiento no se cancelan de publicar cuando la acción se inicia desde las propiedades de la página en la IU táctil. NPR-16560: revisión para CQ-4204681
* Link Rewriter reescribe falsamente los valores href que contienen dos puntos suponiendo que el signo de dos puntos &quot;:&quot; define una Área de nombres JCR. NPR-16753: revisión para CQ-4203762
* En WCM-Design Importer, abrir una página del importador de pruebas e intentar cargar un archivo zip provoca problemas si se ha cargado y eliminado anteriormente. NPR-16486: revisión para CQ-90962
* El desplazamiento al panel **[!UICONTROL Navegación global]** mediante los navegadores Firefox Safari y Google Chrome proporciona una experiencia de usuario diferente. El navegador Firefox muestra el menú **[!UICONTROL Herramientas]** mientras que el navegador Google Chrome muestra el menú **[!UICONTROL Navegación]**. NPR-16770; Revisión para CQ-4200456

### Campaign {#campaign}

* Al probar plantillas de campaña AEM y modificar direcciones semilla para incluir &quot;Datos adicionales&quot;, la lista desplegable de Adobe Campaign desaparece en el Context Hub de la IU táctil. NPR-16771: revisión para CQ-105748

### Móvil a petición {#mobile-on-demand-3}

* Al comprobar previamente una publicación desde el entorno de creación de AEM, una acción de verificación previa que dure más de 5 segundos provoca un pico inusual en el panel del fragmento de integración de AEMM - AEM PECS con un número elevado de solicitudes de estado por segundo. NPR-16908: revisión para CQ-4207055
* La administración de la configuración de AEM Mobile falla después de instalar la actualización AEM-6.2-SP1-CFP1-1.0. NPR-16909: revisión para CQ-4204892

### Traducción {#translation-7}

* La vista previa de los trabajos de traducción no funciona después de instalar 6.2 SP1 - CFP1. NPR-16481; Revisión para CQ-4204655
* La copia de idioma creada mediante Traducción apunta al maestro raíz en lugar de a la Live Copy del país local. NPR-17257; Revisión para CQ-4208287

### Seguridad {#security-3}

* No se realiza ninguna validación de tipo MIME cuando se cargan archivos binarios en AEM. NPR-16617
* Problemas con la carga de imágenes de avatar para usuarios LDAP. NPR-16561

### Forms {#forms-16}

#### Paquete de complemento de Forms {#forms-add-on-package-16}

**Formularios adaptables**

* En el Editor de Forms adaptable, el comentario Configuración de Destinatario en head.jsp debe reemplazarse por la nueva instrucción Context Hub. NPR-17173
* En el Editor de reglas de Forms adaptable, **[!UICONTROL Elegir un elemento]** muestra el evento como &#39;nulo&#39;. NPR-17139
* El formulario enviado se vuelve a enviar al navegar hacia delante mediante la flecha hacia delante (>). NPR-17080
* Al enviar un formulario adaptable mediante AJAX, la función de devolución de llamada &#39;error&#39; nunca se invoca en caso de error. NPR-17034
* Al hacer clic en el botón **[!UICONTROL Guardar formulario]** en el Editor de reglas en tiempo de ejecución, no se guarda el formulario. NPR-16905
* El texto estático debe excluirse del orden de tabulación en formato adaptable. NPR-16749
* El valor calculado de un campo decimal aparece incorrectamente. NPR-16596
* El icono para mostrar el contenido de la Ayuda debe incluirse en el orden de tabulación en los formularios adaptables. NPR-16484
* Compatibilidad con el uso de expresión regular de tipo `dataRef=C:/Users/`en la &#39; **[!UICONTROL Configuración del servicio de relleno previo predeterminada]**&#39; para el relleno previo de datos para Forms adaptable. NPR-16425

* Las validaciones no se activan correctamente en todos los paneles si hay un escenario anidado cargado diferentemente. NPR-15821

**Administración de correspondencia**

* La representación de letras falla si una letra contiene un módulo de texto en blanco (uno sin texto). NPR-17054
* Los saltos de línea y los espacios de tabulación se eliminan del contenido después de pegarse en el Editor de texto. NPR-17039
* La visualización de referencias de un módulo de texto tarda mucho tiempo si se hace referencia al módulo de texto en muchas letras. NPR-17035
* Editar, guardar, eliminar y establecer referencias para fragmentos de documento lleva mucho tiempo. NPR-17033
* El texto justificado se representa con una fuente diferente al obtener una vista previa de la letra. NPR-16976
* La funcionalidad de búsqueda no funciona correctamente si el texto buscado tiene varias ocurrencias. NPR-16920
* La barra de herramientas del Editor de texto se muestra en el navegador de forma intermitente. NPR-16919
* La construcción **[!UICONTROL Guardar formulario]** del Editor de reglas no funciona. NPR-16905
* La lista desplegable Fuente no rellena la familia Fuente al crear un módulo de texto basado en el diccionario de datos mediante Internet Explorer. NPR-16944
* Después de crear un fragmento de texto, la fuente de la letra cambia al obtener una vista previa de la carta. NPR-16830
* Las letras con espacios de tabulación al principio o entre expresiones en el fragmento de documento no se pueden procesar ni previsualizar. NPR-16769

**Forms móvil**

* La previsualización de formulario móvil muestra contenido superpuesto, aunque el formulario se muestra correctamente para la representación en PDF. NPR-17105

**Forms Portal**

* Al hacer clic en el vínculo **[!UICONTROL Descargar]** para un formulario enviado, se abre una página HTML en lugar de un formulario PDF. NPR-17082

* `Upload Comments` para archivos adjuntos no se muestran en la interfaz de usuario para instancias enviadas, aunque están presentes en el XML almacenado en el repositorio crx. NPR-17075

**Servicio de extensiones de Reader**

* Un archivo específico no es Reader Extended en AEM instalación OSGI de formularios. NPR-16625

#### Instalador JEE de Forms  {#forms-jee-installer-16}

**Núcleo**

* Durante el proceso de actualización, Configuration Manager falla con el tiempo de espera. NPR-16774 (consulte [Configuración del tiempo de espera para operaciones a nivel de componente](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Administración de procesos - Espacio de trabajo HTML**

* El punto de partida de una Tarea de Inicio no comienza con los datos enviados en el momento del envío del punto de inicio. NPR-16917
* Al hacer clic en el botón **[!UICONTROL Devolver]** para un formulario en el área de trabajo HTML, el formulario no se cierra, pero se devuelve a la cola de grupo.\
   NPR-16352

**Administración de procesos**

* Permite a los usuarios establecer el nombre para mostrar de tareas anteriores en cualquiera de las siguientes tareas de una instancia de proceso. NPR-15382

**Servicio de salida**

* El servicio de salida no puede procesar un PDF que se ha modificado para incluir un campo adicional &#39;miliseg&#39; en los metadatos `date-time format`. NPR-16838

#### Forms Designer {#forms-designer}

* AEM Editor de secuencias de comandos de Designer no respeta los valores predeterminados de Propiedades del formulario para `Calculate Event`y `Validate Event`. NPR-15921

### Paquetes de funciones incluidos en CFP4 {#feature-packs-included-in-cfp-1}

**Paquete Añada de Forms**

* Mejora en el Editor de condiciones en línea para la administración de correspondencia. NPR-10981

### Paquetes OSGi incluidos en CFP4 {#osgi-bundles-included-in-cfp-4}

Lista de paquetes OSGi actualizados entre AEM 6.2 SP1 y CFP4

Los puntos destacados de CFP3 son:

* Capacidad de búsqueda más eficaz para la IU clásica y para el componente de búsqueda AEM mediante proxy con autenticación de compendio
* Soluciona problemas al cargar recursos y mostrar metadatos de recursos
* Soluciona problemas al crear carpetas y mover páginas en caso de que el título tenga caracteres especiales.
* Correcciones para usar audiencias de sincronización de objetivos, publicar campañas y seleccionar Métrica de objetivo en la IU táctil
* Resuelve problemas de sincronización para trabajos de traducción
* Proporciona seguridad mejorada para el servicio de cumplimentación previa de Forms
* Mejoras en el componente de borrador y envío del portal de formularios y en el servicio Forms con códigos de barras
* Mejoras de uso para formularios adaptables que contienen widgets de archivos adjuntos o fragmentos cargados diferentemente.
* Mejoras de uso en la administración de correspondencia, incluida la capacidad de búsqueda mejorada, el registro de recursos eliminados y la importación de diccionarios de datos.

### Plataforma {#platform-13}

* Una condición de carrera en **ModelAdapterFactory**, que es posible cuando dos subprocesos intentan inyectar el mismo campo, da como resultado un error al construir el modelo. NPR-16443: Revisión para SLING-6584
* Opción de validación en el administrador de paquetes para detectar cualquier conflicto entre el archivo superpuesto (JSP o JavaScript) en /apps y el que contiene una revisión en /libs. La superposición afectada se puede volver a basar para incluir cambios del archivo en /libs . NPR-16216: revisión para CQ-81729
* El inicio de sesión en error.log a veces se detiene unos segundos después de iniciar el editor y debe borrarse para volver a ejecutarse. Solicite actualizar el marco de registro y proporcione el registro de Sling. NPR-15913: revisión para Granite-15452
* Solicitud para actualizar la API &quot; `use"` de JavaScript para evitar errores en la implementación de la API de uso de JavaScript de HTL. NPR-16461: Revisión para SLING-6780

### Sitios {#sites-16}

* Después de actualizar de AEM 6.0 a AEM 6.2, la IU clásica muestra un rendimiento lento al buscar etiquetas debido a numerosas consultas. Para resolver el problema, se pueden seguir los pasos mencionados en [Deshabilitar el estado de replicación en la consola de etiquetado (IU clásica)](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr). NPR-15842: revisión para CQ-4201748.

* Al crear una página en la IU táctil, la comprobación de entrada del campo &#39;nombre&#39; no comprueba el carácter especial &#39;Apóstrofe&#39; (igual que en la IU clásica). Por lo tanto, la página no se puede mover. NPR-16404: revisión para CQ-4205321.
* Al aplicar diferentes estilos en dos filas en el Editor de texto enriquecido y, a continuación, combinarlos, se elimina el estilo aplicado en la segunda fila. NPR-16389: revisión para CQ-4203835.
* En la pantalla Sitios de la IU táctil, al intentar pegar una página dentro de una página sin subpáginas, no funciona porque no aparece el botón Pegar. NPR-15894: revisión para CQ-4201696.
* Al desplazarse por la ficha Páginas del panel Buscador de contenido, algunos conjuntos de páginas se muestran indefinidamente en la IU clásica, mientras que la IU táctil muestra un conjunto limitado de pocas páginas no repetidas. NPR-16271: revisión para CQ-4202371
* Al abrir las Propiedades de página de un LiveCopy en la IU táctil y hacer clic en Guardar sin ningún cambio, se escribe cualquier ficha de LiveCopy y se crea un nodo de configuración de LiveSync. NPR-16327: revisión para CQ-108562
* La restricción de formulario no puede leer la propiedad `ConstraintMessage`. NPR-16388: revisión para CQ-101330
* El componente `wcm/foundation/components/parsys` no muestra el marcador de posición **[!UICONTROL &#39;Arrastrar componentes aquí]**&#39;. NPR: 16748: Revisión para CQ-4205187

### Recursos {#assets-16}

* El rasterizador de PDF deja de funcionar y causa problemas de memoria insuficiente después de instalar 6.2 SP1 o la revisión 12430. NPR-15991
* Los metadatos de una propiedad de cadena, `documentNumber`, se muestran como una fecha, mientras que debería ser un número. NPR-16134: revisión para GRANITE-16916
* Trunca el texto en el globo de evento de la línea de tiempo. NPR-16226: revisión para CQ-85226
* Al crear una carpeta bajo la jerarquía de contenido con un título con caracteres especiales, se muestra la forma codificada del carácter especial. NPR-15935: revisión para CQ-4202987
* El usuario no puede cargar recursos ni crear carpetas mientras navega por los recursos debido a un comportamiento incoherente que se muestra al utilizar el botón &#39;Crear&#39;. NPR-16410: revisión para CQ-4204793
* Se han encontrado errores inesperados al cargar recursos HTML compartidos desde la vista de artículos en AEM creación. NPR-16133: Revisión para AEMM-4155970

### Integración {#integration-14}

* Al habilitar la autenticación proxy con autenticación implícita, el componente Búsqueda AEM genera una excepción ConcurrentModificationException. NPR-15309: revisión para CQ-4199191
* Al crear una Actividad de prueba A/B de Destinatario en AEM, la audiencia no se sincroniza con el Destinatario y muestra &#39;sin audiencias. NPR-16229: revisión para CQ-4204210
* Después de instalar SP1+NPR-11577 v1.2, al elegir &#39;Usar una métrica de Analytics&#39; para la métrica de objetivo mientras se establece el objetivo en la IU táctil, la lista desplegable de métricas nunca se carga. NPR-16129: revisión para CQ-4204316
* Al usar objetivos, la publicación de la campaña no publica automáticamente todo el árbol, incluidas la marca y el maestro. NPR-15855: revisión para CQ-94630

### Traducción {#translation-8}

* El trabajo de traducción de sincronización no se activa automáticamente y AEM sondeo no se produce sin bloquear los proyectos de traducción. NPR-15163: revisión para CQ-90856

### Forms {#forms-17}

#### Paquete de complemento de Forms {#forms-add-on-package-17}

**Formularios adaptables**

* Al guardar un formulario adaptable con un archivo adjunto, la ruta completa del archivo adjunto se agrega en la etiqueta `fileAttachment` del XML generado, en lugar del nombre del archivo adjunto. NPR-16529
* En los formularios adaptables basados en XDP, el contenedor `afData/afBoundData` está presente en el XML enviado, aunque incluso el XML de relleno previo no tenga contenedores `afData/afBoundData`. NPR-16118

* Notación exponencial en el campo Número: Cuando se utilizan formularios adaptables, si se introduce un número con una fracción decimal que supera los diez caracteres en total, el número se convierte en notación exponencial en el XML enviado. NPR-16106
* Para los formularios que contienen un componente de archivo adjunto y un fragmento cargado diferido, el xml de datos enviado no contiene la información del componente de archivo adjunto. NPR-16022
* Para un panel repetible con carga diferida que no tiene un antecesor repetible, los elementos secundarios repetitivos dentro de una segunda instancia del panel no se pueden repetir. NPR-15944
* Al intentar guardar un fragmento dentro de un fragmento en el editor de formularios, la raíz del modelo de fragmento no rellena el valor del fragmento secundario. NPR-15943
* Al crear una casilla de verificación con un solo elemento e intentar mostrar el título de la casilla de verificación manteniendo el título del elemento oculto, la acción crear diccionario emite un `ArrayIndexOutOfBoundException` si el texto del elemento está vacío. El diccionario no se crea y no se genera ninguna respuesta de error en la pantalla. NPR-15816
* Para los formularios adaptables con widgets de archivos adjuntos, algunas partes del formulario se desactivan después de previsualizar el archivo adjunto.\
   NPR: 16611

* En el caso de los widgets de archivos adjuntos en los que se permiten varios adjuntos, si se envía una instancia de formulario nueva con un adjunto en una utilidad que tenga un adjunto anterior, se muestra un código de error al abrir el adjunto agregado en lugar del contenido real. NPR-16258
* La seguridad del servicio de formularios permite precumplimentar el servicio de acceso no autorizado a través de protocolos como `file://`, `http://` y `ftp://`. Consulte &quot; [Configuración del servicio de relleno previo mediante Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754).&quot; NPR-15414

* Solicite procesar el formulario adaptable en formato PDF en lugar de HTML en el paso Verificar y anexe todos los archivos adjuntos al PDF, de modo que la impresión muestre el formulario completo. NPR-9011

**Administración de correspondencia**

* Mientras se trabaja con fragmento de texto en una letra en modo Previsualización/edición, si el texto se convierte en lista, se interrumpe toda la funcionalidad de la letra y se genera un error de JavaScript. NPR-16460
* La importación de un archivo XSD para crear un diccionario de datos en el nodo Administración de correspondencia falla cuando el explorador no responde cada vez que se carga el XSD y se selecciona el nodo raíz. Este problema es independiente del explorador y no aparece en los registros del servidor. NPR-16452
* Al obtener una vista previa de una carta con el navegador Internet Explorer y al intentar editar el tamaño de fuente del contenido, los valores de duplicado se ven de 8 a 72 en la lista desplegable de tamaño de fuente. NPR-16387
* Si un campo flotante aparece como un campo de entrada desde un fragmento XDP, el campo no se expande en la previsualización de letras mientras se utiliza el explorador Internet Explorer. NPR-16367
* Al intentar enviar una carta directamente desde la previsualización, la ventana emergente del nombre de la carta no se muestra correctamente debido a que está oculta. NPR-16353
* Los espacios de línea agregados al editar una letra no se reflejan en la ventana de Previsualización. Para listas en fragmentos de texto, la salida PDF no muestra el espaciado correcto. NPR-16267
* Al trabajar en un fragmento de documento de texto con el navegador Internet Explorer, al intentar proporcionar sangría al texto se produce un error, ya que el cursor no permite la sangría del texto. NPR-16128
* Añadir o modificar un diccionario de datos en un fragmento de documento de texto existente lleva mucho tiempo y no siempre se notifica al usuario. NPR-16102
* Al obtener una vista previa de una carta con contenido desplazable mediante el navegador Internet Explorer, la barra de desplazamiento del explorador se solapa con la barra de desplazamiento de la carta y no se puede ver todo el contenido de los fragmentos del lado derecho. NPR-16068
* Al crear o editar fragmentos de documento de texto con el navegador Google Chrome, la lista desplegable de selección de color aparece automáticamente y no se puede eliminar. El usuario debe seleccionar lista como tipo de entrada de datos para poder editar el fragmento. NPR-16067
* Al utilizar la API Letterinstance, el método `import com.adobe.icc.services.api.LetterInstanceService` no funciona. NPR-16008
* Cambiar los formatos de visualización de fecha a `locale=en_US; dateFormat=MMM dd,yyyy;` en la Configuración del Compositor de recursos no funciona de la forma esperada y el formato de fecha se muestra como caracteres no deseados. NPR-16007
* El tipo de vinculación de datos en letras mientras se vuelve a crear se muestra como &quot;Usuario&quot; aunque se haya configurado de forma diferente anteriormente. NPR-16619

**Forms Portal**

* Los escenarios de actualización para los componentes de borrador y envío no funcionan con la implementación de muestra de base de datos. NPR: 16752

**Servicio de Forms con códigos de barras (BCF)**

* La análisis de código estático del servicio Forms con códigos de barras (BCF) informa de problemas. NPR-13855

#### Instalador JEE de Forms  {#forms-jee-installer-17}

**Administración de procesos - Espacio de trabajo HTML**

* La seguridad del servicio de cumplimentación previa de formularios de acceso no autorizado mediante protocolos como &quot;file://&quot;, &quot;http://&quot; y ftp://. Para obtener más información, consulte [Configuración del servicio de relleno previo mediante Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754). NPR-15434

**Administración de usuarios **

* La pantalla de inicio de sesión de SAML muestra una versión incorrecta (6.1.0) en el servidor AEM 6.2. NPR-13825
* Con AEM Forms configurado para la autenticación de inicio de sesión único (Kerberos), si la autenticación de usuario falla al intentar iniciar sesión, se devuelve el código de error &#39;404&#39;. El usuario se redirige al sitio de inicio de sesión sólo después de actualizar la página. NPR-15015

#### Forms Designer {#forms-designer-1}

* Cambiar la configuración regional del formulario a francés (Canadá) en la revisión ortográfica del diccionario no funciona en AEM Forms Designer.\
   NPR-15896

### Paquetes de funciones incluidos en CFP3 {#feature-packs-included-in-cfp-2}

**Paquete Añada de Forms**

* Al eliminar cualquier recurso en la administración de correspondencia, se debe registrar un mensaje de advertencia en el archivo error.log. NPR-13225
* Mejore la funcionalidad de búsqueda mientras previsualiza una carta en la administración de correspondencia para habilitar la búsqueda de texto en el contenido del fragmento de texto, en lugar de buscar únicamente el título o la etiqueta de la letra. NPR-16103

### Paquetes OSGi incluidos en CFP3 {#osgi-bundles-included-in-cfp-5}

Lista de paquetes OSGi actualizados entre AEM 6.2 SP1 y CFP3

[Obtener ](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
archivoLos aspectos destacados del paquete 2 de correcciones acumulativas son:

* Correcciones de estabilidad y mejoras de rendimiento en AEM plataforma, incluido el marco y las operaciones de Sling
* Se ha mejorado la administración de recursos con varias correcciones para acceder, mover, buscar, cargar y publicar recursos
* Creación y administración mejoradas de sitios con correcciones en fragmentos de contenido, complementos de anclaje, proyecciones de diapositivas y componentes de Context Hub
* Varias correcciones en la IU táctil, incluyendo el editor de texto, Omniture y el proceso de creación de variantes
* Flujos de trabajo de traducción mejorados; conector de Microsoft mejorado para usar nuevas API de traducción para el portal de Azure
* Correcciones en proyectos y Campaña
* Creación y administración mejoradas con correcciones en formularios adaptables, administración de correspondencia y funciones del portal de formularios
* Correcciones en los componentes principales, XTG y HTML de Forms JEE

### Plataforma {#platform-14}

* El `SlingPostProcessor` se activa si se edita la página que hace referencia directamente al marco de trabajo de Sling. NPR-15754: revisión para CQ-104153

* El valor de las etiquetas con la propiedad `tagBasePath` no se recuperan en el cuadro de diálogo de la IU clásica al desplazarse a un componente de página. NPR-15543: revisión para CQ-4199950

* Mientras realiza operaciones Sling, cuando tiene un fragmento llamado &#39;chunk_n_n-1&#39; `SlingFileUpload handler.getLastChunk` se ejecuta en un bucle interminable con fragmentos vacíos. NPR-15455: Revisión para SLING-5701

* Cuando una interfaz amplía otra interfaz, los métodos inyectables en la superinterfaz no se insertan correctamente. NPR-15202: Revisión para SLING-5710
* No se impide una posible excepción de puntero nulo al utilizar la llamada a la función `com.adobe.granite.infocollector.impl.FilesTraversal`. Revisión de NPR-15169 para CQ-4197640
* El estado del flujo de trabajo no es coherente para algunos nodos secundarios y se muestra un error al enviar eventos de observación para ese nodo. NPR-15701: revisión para GRANITE-13786
* Cuando el usuario selecciona un nodo en CRXDE (por ejemplo, /content/dam/) y, a continuación, la ficha &#39;Control de acceso&#39;, asegurándose de que existe una Lista de Control de acceso, al arrastrar y soltar algunos elementos se mueven los elementos distintos del seleccionado. Revisión de NPR-15696 para GRANITE-16300
* Si se selecciona un usuario en la lista desplegable cuando se intenta suplantar, la ventana emergente del usuario desaparecerá. NPR-15774: HotFix para CQ-4201738/GRANITE-11895
* En Omniture, la búsqueda por etiquetas con sugerencias rellenadas automáticamente no funciona. NPR-15088: revisión para GRANITE-14426.\
   Nota: Esta corrección requiere el Oak CFP 1.4.11 o superior.

### AEM Author móvil {#mobile-aem-author}

* Al utilizar paquetes de AEM Mobile y ContentSync con una aplicación híbrida, AEM responde a una solicitud de captura (con marcas de hora) realizada por la aplicación con el paquete más antiguo, en lugar del solicitado por la aplicación. NPR-15749: revisión para CQ-104153

### Sitios {#sites-17}

* El estado de modificación de la bandeja de entrada de workflow en el núcleo de WCM no cambia si el usuario modifica una página después de activar un flujo de trabajo. NPR-15684: Corrección urgente para CQ-4196974
* El complemento Anclaje del Editor de texto enriquecido para la IU táctil genera HTML5 no compatible cuando el usuario hace clic en el icono de anclaje y agrega un nombre. Debe agregar un atributo &#39;id&#39; en lugar del atributo &#39;name&#39; en la etiqueta HTML5 para el elemento de anclaje. NPR-15650: revisión para CQ-89782
* Cuando se crea un esquema de metadatos con numerosos campos y se aplica a los metadatos del fragmento de contenido, no se crea ninguna barra de desplazamiento en la pantalla de metadatos del fragmento de contenido, por lo que los campos no se pueden editar. NPR-15478: revisión para CQ-4202622
* La edición del componente de campo `TagInput` no muestra los valores configurados anteriormente en los campos de diálogo. NPR-15464: HotFix para CQ-4200360

* En la interfaz de usuario del editor de fragmentos de contenido, en caso de que se creen muchas variaciones de un fragmento de contenido, el panel lateral no muestra la barra de desplazamiento para desplazarse por todas las variaciones. NPR-15445: HotFix para CQ-4199444
* Cuando los usuarios se eliminan de los grupos directos, se agregan a los grupos heredados. NPR-15400: revisión para CQ-98758
* Creación WCM: El autor de la IU táctil no permite la edición de páginas que tienen comas en el nombre. NPR-15396: revisión para CQ-4199723
* Al utilizar la IU táctil para la creación, la función `Granite.author.editableHelper.doSelectParent` pasa argumentos en un orden incorrecto que provoca un error de JavaScript. NPR-15349: revisión para CQ-4198594
* El segmento de ContextHub muestra la experiencia incluso si la cookie de exclusión está presente. NPR-15293: revisión para CQ-4198024
* El componente Presentación de diapositivas de la IU clásica no puede crear diapositivas ni arrastrar y soltar imágenes para crear nuevas diapositivas. NPR-15281: revisión para CQ-4194164
* Los usuarios, independientemente de su permiso, se muestran en los elementos de menú &quot;Crear&quot;, como Crear página, Crear sitio, Crear Live Copy, Crear lanzamiento y Crear catálogo, en la consola Administración del sitio. NPR-15278: revisión para CQ-94436
* Después de instalar AEM 6.2 Service Pack 1, el control deslizante &#39;Incluir subpáginas&#39; deja de funcionar para inicios de página. NPR-15230: revisión para CQ-4198449
* Solicite mejorar la depuración de versiones para recuperar y procesar versiones en bloques y también poder utilizar una ruta especificada en una consulta XPath. NPR-15186: revisión para CQ-109205
* Falta el botón Borrar en la ficha de miniaturas Propiedades de la página del componente Sitios. Revisión de NPR-15143 para CQ-4196997
* Para un sitio que utiliza Live Copy, al seleccionar la casilla &#39;Live Copy&#39; en el panel Columnas de la consola siteadmin no se muestra el estado de Live Copy correctamente y solo se muestra el código HTML. NPR-15108: revisión para CQ-97086
* Al editar fragmentos de contenido, si el usuario hace clic en hecho (&#39; retro&#39;) para editar antes de obtener la respuesta de la publicación, el contenido editado no se guarda correctamente. NPR-15014: revisión para CQ-4194095
* Si se cierra la página Editar durante el modo Deformación de tiempo y se intenta volver a abrirla desde SiteCatalyst, se producirá un error con el estado &#39;500&#39; en lugar de volver a abrir la página. NPR-14965: revisión para CQ-109647:
* En la interfaz de usuario de Digital Asset Manager (DAM), la búsqueda del selector de usuarios Buscar autorizables produce una excepción &#39;Memoria insuficiente&#39;. NPR: 15307: HotFix para CQ-98542

### Recursos {#assets-17}

* Después de buscar un recurso en Omniture, al seleccionar un recurso e intentar editar las propiedades, haga clic en &#39;Propiedades de la Vista&#39; y luego en el botón &#39;Guardar&#39; se redirige a los usuarios a una página en blanco. NPR-15900: revisión para CQ-4202372
* Recursos La interfaz de usuario no responde a eventos. Si selecciona un recurso y hace clic en &#39;Publicar&#39; o &#39;Representaciones&#39;, no se producirá ninguna actividad. NPR-15828: revisión para CQ-4202247
* Al publicar un recurso desde la vista de tarjetas, la tarjeta no se actualiza para reflejar un estado publicado a menos que se actualice la página. NPR-15826: HotFix para CQ-102732
* Revisión acumulativa que contiene revisiones de recursos. NPR-15225
* Si se incluye el carácter de símbolo de unión (&#39;&amp;&#39;) en el nombre de una carpeta de recursos, el nombre de la carpeta no se muestra correctamente al desplazarse al recurso. NPR-15775: revisión para CQ-4201735
* El uso de un carácter de símbolo &amp; en el nombre de un archivo de recurso provoca problemas al acceder a sus propiedades. NPR-15770: revisión para CQ-4201737
* Al navegar por Recursos y utilizar el modo de visualización &#39;vista de columna&#39;, si el usuario actualiza la página después de seleccionar y hacer clic en un recurso, se muestran los detalles del recurso en lugar del contenido actualizado. NPR-15768: revisión para CQ-4201727
* La ingestión de PDS absorbe el 100% de utilización de CPU con un montón de bibliotecas para servicios pdf. Corrección urgente NPR-15606 para GRANITE-12929
* El acceso a la interfaz de usuario de &#39;Mi vínculo compartido&#39; mediante el navegador Firefox no muestra los elementos o usuarios compartidos y la pantalla no se puede utilizar. NPR-15539: HotFix para CQ-4200992
* Al utilizar Digital Asset Manager, si una página está asociada a un conjunto de imágenes, al mover las imágenes a una nueva carpeta se interrumpe la asociación de páginas y la página asociada pasa por alto algunas de las imágenes. NPR-15538: revisión para CQ-111479
* En el componente Visor de presas, el uso del modo de ejecución &#39;nosamplecontent&#39; provoca errores con los medios dinámicos. NPR-15449: revisión para CQ-4195425
* Al crear perfiles de vídeo, si se elige un ajuste preestablecido de codificación de vídeo de alta calidad y de calidad media, los cambios realizados no se guardan. NPR-15447: revisión para CQ-4195482
* Aunque la carga de un recurso en Brand Portal falla debido a una respuesta de error del servidor, el estado se actualiza a &#39;Publicado&#39; en la interfaz de usuario del portal de marca, lo que dificulta el seguimiento del archivo perdido. NPR-15442: revisión para CQ-4197968
* Al publicar una carpeta de recursos en Brand Portal, donde la publicación tarda más de una hora, algunos archivos no se pueden publicar. NPR-15441: revisión para CQ-4199493
* Cuando se utiliza la consola de Buscador de recursos en la vista de columnas, al intentar crear una carpeta se produce un error una vez, aunque se logra reintentar. NPR-15370: revisión para CQ-4199448
* Si un recurso o una carpeta seleccionados en la interfaz de usuario de DAM tiene una coma en el nombre, la ficha Referencias no está disponible y muestra un mensaje &quot;La Lista de referencias no está disponible para varias selecciones&quot;. NPR-15362: revisión para CQ-4199721
* La publicación de una carpeta en Brand Portal no cambia el estado publicado de la carpeta, aunque los recursos de la carpeta se hayan publicado correctamente. NPR-15292: revisión para CQ-4197667
* Durante la navegación a la consola Recursos en la IU táctil, se muestra una excepción al activar determinados recursos. NPR-15217: HotFix para CQ-108779
* Publicación de un vídeo en YouTube cuando la conexión se realiza a través de un servidor proxy. NPR-15109: HotFix para CQ-110332
* Uso de un recurso con un nombre que contenga un punto o punto (.) en data-il-resource no se resuelve en el mismo recurso y la ruta de salida termina en el punto. NPR-15069: revisión para CQ-4195914
* Tras actualizar AEM 6.2 a Service Pack 1, se produce un error en la sincronización de recursos en Scene7. La propiedad dam:Scene7FileStatus muestra el estado &#39; `UploadFailed`&#39; incluso para los recursos publicados. NPR-15269: revisión para CQ-4197708

### Interfaz de usuario {#user-interface-5}

* En **[!UICONTROL IU táctil]**, la fecha guardada no se muestra para los campos de fecha que no tienen type=&#39;datetime&#39; mientras se usa el explorador Internet Chrome versión 56.0.2924.87. NPR-15383: Revisión para GRANITE-16481
* En **[!UICONTROL IU táctil]**, el Editor de texto enriquecido elimina el subproceso y los elementos de rótulo de las tablas HTML mientras los procesa. NPR-15267: revisión para CRTE-41
* `FileUpload Validator` no gestiona casos en los que el inicio automático es verdadero o cuando  `uploadFile()` se llama manualmente y genera un informe de validación no válido en estos casos. NPR-15295: revisión para GRANITE-13499

* Omniture no permite que los clientes que utilizan /apps agreguen una fuente de datos de columna, ya que supone que la configuración de ubicación se encuentra en */libs/granite/omnisearch/content/metadata/*. Revisión de NPR-13188 para GRANITE-16479
* Al utilizar la **[!UICONTROL IU táctil]**, las variantes de producto no se crean al mismo nivel que el producto. El usuario no está informado del estado del proceso de creación de variante. NPR-15345: HotFix para CQ-4198948

**Scene7**

* La ejecución del flujo de trabajo de Scene7 da como resultado archivos abiertos que no se cierran. Solicite mejorar el servicio AEM-S7 para que mantenga y reutilice una única instancia de HttpClient con la configuración de agrupación compartida. NPR-15357: HotFix para CQ-109958

### Traducción {#translation-9}

* Al utilizar proyectos de traducción, al actualizar las copias de idioma del maestro de inglés, se generan 11 inicios independientes con el mismo nombre y la misma raíz de origen, pero con raíces de inicio ligeramente diferentes, en caso de que el nombre de página siga un patrón definido. NPR-15605: revisión para CQ-4200699
* Los proyectos de traducción no se crean para páginas cuando las raíces del idioma tienen guiones y guiones en el nombre. NPR-15171: HotFix para CQ-96286
* Solicite actualizar el conector de Microsoft para poder usar las API de Microsoft Translator, que Microsoft pone a disposición en el portal de Azure. NPR-15320: revisión para CQ-101010

### Proyectos {#projects-4}

* Sólo 20 proyectos inactivos están visibles en la pantalla Proyectos, aunque existen más de 20 proyectos inactivos en el repositorio. NPR-15656: revisión para CQ-4200903

### Campaña {#campaign-1}

* Mientras se utilizan los componentes Campaña - Segmentación y MAC - Prueba e integración de Destinatario, la anulación de la publicación de actividades no actualiza el estado de actividad en la IU maestra. NPR-15401: HotFix para CQ-4199839
* Al mover un producto en AEM comercio, el Asistente para mover el producto omite los valores precargados para el nombre del producto, el título, las páginas a las que se hace referencia, la creación del autor y la fecha de creación. NPR-15228: revisión para CQ-98617

### Seguridad {#security-4}

* Se ha agregado un parámetro de token CSRF a los formularios con un método de GET. NPR-15229

### Forms {#forms-18}

#### Paquete de complemento de Forms {#forms-add-on-package-18}

`**Adaptive Forms**`

* Los valores predeterminados se sustituyen por valores vacíos en xml al rellenar previamente el formulario adaptable con XML de entrada. NPR-15721
* El contenedor `afData/afBoundData` está presente en XML enviado, aunque incluso el XML de relleno previo no tiene `afData/afBoundData` envoltorio en formularios adaptables basados en esquema XML. NPR-15541

* Los títulos de la barra de acordeón deben ser encabezados HTML &#39;h2&#39; editables en lugar de la etiqueta &#39;a&#39;. NPR-15475
* La presentación de acordeón de un panel de formulario no es accesible para los usuarios del lector de pantalla. Los usuarios no pueden desplazarse a la ficha acordeón solo mediante el teclado mediante el software de lector de pantalla como JAWS o NVDA. NPR-15474

`**Correspondence Management**`

* Guardar, eliminar y establecer referencias para un fragmento de documento lleva un tiempo considerable. NPR-15939
* Alineación de tabulación definida en Administrar recursos en texto que contiene varios saltos de Encabezado en la interfaz de usuario de CCR. NPR-15818
* Las miniaturas de los módulos de texto no muestran el contenido alineado, aunque el texto contiene contenido alineado creado con fichas en Google Chrome. NPR-15819

`**Forms Portal**`

* El servicio de relleno previo no funciona para XDP Forms. NPR-15466
* Al almacenar borradores de formularios adaptables y envíos a la base de datos, el estado del formulario adaptable se daña cuando la conectividad de la base de datos falla por cualquier motivo (por ejemplo, después de un largo tiempo de inactividad). NPR-15297

#### Instalador JEE de Forms  {#forms-jee-installer-18}

`**Core**`

* Después de actualizar a la versión más reciente de Java 1.8.0_121-b13, la interfaz de usuario del administrador no es accesible en AEM Forms. NPR-15330

`**XTG**`

* Al utilizar el servicio Output para combinar un formulario específico con un dataxml, el tiempo de respuesta es 20 veces mayor que el tiempo que tarda el servidor ES4 SP1 en la misma operación. NPR-15283

#### Aplicación de AEM Forms {#aem-forms-app-1}

* Al recuperar tareas no guardadas, el mensaje que se muestra al recuperar tareas no guardadas debe ser más claro para reducir el error del usuario. NPR-15377
* La aplicación de AEM Forms no procesa formularios creados a partir de plantillas personalizadas. NPR-15892
* Los usuarios no pueden iniciar sesión en la aplicación de AEM Forms. NPR-15891

Los aspectos destacados de AEM 6.2 SP2-CFP1 son:

* Optimiza la funcionalidad de replicación en Sitios:

   * Correcciones en varios problemas de publicación, LiveCopy y versiones de escritura erróneas

* Mejora la capacidad de respuesta de la IU táctil durante:

   * Búsquedas de recursos
   * clasificación basada en el tamaño

* Mejora la administración de etiquetas en colecciones inteligentes
* Controles de acceso más estrictos durante las operaciones de CRUD en carpetas

### Plataforma {#previous}

* Solicitud de eliminación de `ReplicationQueue#forceRetry` llamadas de API durante el inicio de los agentes de replicación porque dichas llamadas ralentizan considerablemente la instancia, especialmente cuando tiene muchos agentes de replicación. NPR-14032: revisión para GRANITE-13095
* Solicite la configuración de `DurboImportConfigurationProviderService` OSGi para admitir campos que pueden almacenar una matriz de valores. NPR-14570: revisión para CQ-108684
* El uso del componente Sightly en una página después de migrar a AEM 6.2 hace que el cuadro de diálogo Propiedades de la página deje de funcionar. NPR-14328: revisión para CQ-108355
* Al cancelar la programación de un trabajo programado anteriormente, no se elimina el nodo correspondiente por debajo de */var/eventing/schedule-job*. NPR-14253: Revisión para SLING-5666
* Cuando un administrador intenta suplantar a un usuario eliminado, la interfaz de usuario no se actualiza. NPR-14247: revisión para CQ-107446
* La comprobación de la protección XSS produce una codificación incorrecta en el componente Sightly. NPR-14004: revisión para CQ-93821
* Solicite actualizar Jackrabbit Filevault a 3.1.30 para resolver varios problemas. NPR-13454
* El error de caché se produce cuando la distribución de Sling sincroniza los paquetes de distribución del autor a la publicación. NPR-13034: revisión para GRANITE-13970

### Sitios {#sites-18}

* Problemas con VersionManagerImpl que purgan versiones incorrectas del historial de versiones. NPR-14372
* El componente parsys de WCM Sightly Foundation ignora los nombres de etiquetas de declaración de componentes, `cq:htmlTag / cq:tagName`. NPR-14225
* Cuando se utiliza Sightly Parsys para procesar los componentes insertados mediante JavaScript en la IU táctil, la decoración personalizada se omite después de actualizar la página. NPR-14122
* Las listas desplegables de destinatario no funcionan en el cuadro de diálogo IU táctil cuando se crean varios campos de Richtext, como vínculos. NPR-13911
* Al editar un campo de texto con varias propiedades del editor de texto enriquecido (RTE) en un cuadro de diálogo (IU táctil), el enfoque cambia aleatoriamente a una propiedad RTE específica. NPR-13703
* El componente de vídeo predeterminado fuera del cuadro no representa la miniatura de vídeo. NPR-14976
* La información se carga lentamente en la ficha Live Usages (Uso activo) del Editor de plantillas. NPR-14880: revisión para CQ-83417
* La instalación de la revisión 10936 en una instancia de AEM 6.2 deshabilita el componente iparsys. NPR-14330: revisión para CQ-106982
* Varios problemas de componentes de despliegue y un problema con Live Copy tras la migración a AEM 6.1 SP1. NPR-15256
* La acción Despliegue de página no puede crear elementos secundarios más allá del primer nivel, incluso para varias configuraciones de Despliegue. NPR-15055
* Al enviar el cuadro de diálogo Propiedades de página desde el Editor, se vuelven a escribir los datos sin modificar en las fichas de LiveCopy. NPR-14693
* Cuando se envía el cuadro de diálogo Propiedades de página desde el Editor, el postprocesador MSM escribe algunos parámetros de la solicitud en lugar del parámetro `msm:writeLiveCopyConfig`. NPR-14434
* Varios problemas relacionados con el componente de despliegue, Live Copies y otros aspectos de MSM. NPR-12235

### Recursos {#assets-18}

* UnPack Workflow no puede gestionar imágenes con caracteres especiales en el nombre del archivo de imagen. NPR-15227: revisión para CQ-103887
* Los recursos que tienen la expresión Repetir con condición no se muestran correctamente. Cuando el usuario previsualización la plantilla de `*CDN3835RLCEN*` letras, no se muestra ningún recurso ubicado en el área destinatario de trabajo. Cuando el recurso `*VIPReassement*`, que es un recurso opcional, está preseleccionado, no está seleccionado, los demás recursos preseleccionados se muestran en la letra. NPR-14844

* Al crear una colección inteligente, la etiqueta de estilo no se conserva cuando se guarda la colección inteligente. NPR-15081: revisión para CQ-4195494
* Consultas de búsqueda de recursos que se ejecutan lentamente en la IU táctil durante búsquedas simultáneas de varios usuarios. NPR-15019: Hotifx para CQ-4195405
* Los metadatos extraídos para una propiedad de tipo `Long[]` se convierten en tipo `String[]` cuando el recurso original se vuelve a cargar en una ubicación diferente. NPR-15016: Revisión de CQ-4195005

* Los usuarios no pueden eliminar una búsqueda guardada o una colección inteligente. NPR-14924: revisión para CQ-108494
* La edición masiva de metadatos para recursos (modo de anexado) mientras se utiliza un valor booleano para TypeHint en un campo desplegable en el esquema de metadatos subyacente produce un error. NPR-14529: revisión para CQ-106876
* Los usuarios sin derechos de replicación no pueden eliminar carpetas de recursos. NPR-14321: revisión para CQ-88271
* Al intentar editar los perfiles de vídeo para un vídeo en el Editor de Canales, el cuadro de diálogo de diseño no se abre y genera una excepción de puntero nulo en el registro de errores. NPR-14144: revisión para CQ-81101
* La propiedad de marca de tiempo &#39;Creada&#39; generada por el sistema que se muestra en la página de propiedades de un recurso es incorrecta. NPR-13992: revisión para CQ-95029
* Solicitud para habilitar la detección de recursos de duplicado para usuarios sin acceso de lectura en AEM Assets NPR-13851: Revisión para CQ-102281
* Los usuarios no pueden editar los metadatos de los recursos de forma masiva desde la página de propiedades. NPR-13721: revisión para CQ-100703
* Mensaje de error incorrecto en la IU clásica cuando se carga un recurso de duplicado. El mensaje de error no indica por qué falló la carga. NPR-13691: revisión para CQ-99272
* AEM Assets no puede ordenar más de 50 recursos por tamaño a la vez en la vista de Listas cuando ésta contiene numerosos recursos. CQ-100588
* Si se seleccionan varios recursos, se produce un error con el código de respuesta 414 (Solicitar URI demasiado largo) si el URI de recurso o carpeta es demasiado largo. NPR-13516: revisión para CQ-76076
* La página Informe de recursos deja de responder cuando el usuario selecciona todas las opciones en el cuadro de diálogo Configurar columnas. NPR-13187: revisión para CQ-95589
* Comportamiento inesperado del Selector de etiquetas en Safari e Internet Explorer. NPR-13134
* La edición de la búsqueda guardada desde el carril de búsqueda de administración de recursos permite guardarlas como selecciones inteligentes anidadas, lo que provoca problemas de estabilidad de entorno. NPR-13119: revisión para CQ-99460
* Después de mover un archivo (o carpeta) y cambiarle el nombre, los metadatos &#39;cq:name&#39; no reflejan el nuevo nombre de archivo (nombre de carpeta). NPR-13036: revisión para CQ-99141
* El recurso con nombres que incluyen caracteres especiales no se puede descargar del vínculo de descarga compartido por correo electrónico. NPR-12872: revisión para CQ-95795
* Los informes de recursos predeterminados que se generan cuando hay un número considerable de recursos provocan grandes recorridos donde la búsqueda no alcanza ningún índice y picos de uso de CPU. NPR-12811: revisión para CQ-84409
* Los usuarios de AMS pueden acceder a la instancia de creación de AEM Assets desde redes distintas que no pueden cargar recursos mediante la carga de fragmentos sin privilegios de eliminación en carpetas. NPR-12768: revisión para CQ-82715
* En las búsquedas basadas en etiquetas de recursos que utilizan el carril de búsqueda de recursos, la función Tipo delante no se limita a la ruta raíz y muestra las etiquetas de todas las Áreas de nombres. NPR-12666
* El componente StaticRenditions genera una excepción de puntero nulo. NPR-12665
* Solicitud para deshabilitar MissingMetadataNotificationJob porque hace que la interfaz de usuario de notificación de distintivos rompa la página con una excepción de tiempo de ejecución &quot;No se puede analizar la entrada&quot;. NPR-12500: revisión para CQ-93573
* La opción &#39;Deshabilitar edición&#39; para un campo de etiqueta no funciona en las páginas de propiedades de recursos en TouchUI. NPR-12429: revisión para CQ-88835
* Correcciones de API en AEM Assets 6.2 para la implementación Companion App SMB. NPR-11099
* Desde la actualización de Jquery, los usuarios no pueden seleccionar una colección de recursos y confirmar la selección en el panel Asociar contenido de un fragmento de contenido. NPR-14847: Puerto posterior para CQ-4194209
* A pesar de invocar la ordenación infinita en el lado del cliente, solo se ordenan los artículos, pancartas y colecciones que se muestran actualmente en la interfaz de usuario. NPR-14493: revisión para CQ-109926
* Solicitud para implementar la función omnisearch para AEM servicio móvil a petición. La búsqueda de palabras clave para cualquier artículo, colección o pancarta no devuelve ninguna coincidencia. NPR-14093: revisión para CQ-101394
* Cuando se utiliza el componente Selección de corales (*granito/ui/components/coral/foundation/form/select*) en un cuadro de diálogo, la inicialización de valores no funciona correctamente en Internet Explorer (exploradores IE11 o Edge) cuando el valor seleccionado contiene un solo elemento. NPR-13395: revisión para CQ-101013

### Proyectos {#projects-5}

* Al exportar un proyecto de traducción creado con el método de traducción como &#39;humano&#39; y el proveedor de traducción como &#39;ninguno&#39;, no se genera ningún archivo Translation_export_summary.xml porque falta el archivo de asignación GUID. NPR-13137: revisión para CQ-91976
* En los proyectos de AEM, al crear un proyecto con la propiedad de fecha de vencimiento establecida, la conversión de fecha establece la hora de forma incorrecta debido a la diferencia de huso horario entre el servidor y el cliente. NPR-13003: revisión para CQ-98288
* La opción &#39;Mostrar en sitios&#39; se pierde del trabajo de traducción cuando se actualiza un proyecto de traducción. NPR-12966: revisión para CQ-93740
* Cuando se crea un proyecto de traducción para una página de sitio exportada, no se representa correctamente en la previsualización. NPR-12964: revisión para CQ-84627

### Flujo de trabajo {#workflow-3}

* El vínculo Carga útil de la ficha Archivo de la consola Flujo de trabajo devuelve un error con el código de respuesta &#39;404&#39; al hacer clic en él. NPR-14993: revisión para CQ-4194977
* Cuando se utilizan AEM flujos de trabajo predeterminados, CQ Mailer no envía una notificación por correo electrónico al grupo que omite la dirección de correo electrónico de un solo miembro. NPR-14804: Solicitud de revisión para CQ-91499
* Mejoras de rendimiento para bandeja de entrada y distintivo de notificación en la IU táctil. NPR-14145: revisión para CQ-101125
* Los usuarios no pueden realizar la previsualización de la carga útil desde la consola Bandeja de entrada del flujo de trabajo mientras inician flujos de trabajo. NPR-13226: revisión para CQ-100275
* La cookie &#39;saml_request_path&#39; configurada mediante el controlador de autenticación SAML muestra la cookie configurada con un &#39;?&#39; extra carácter. Además, cuando se vuelve a publicar una respuesta SAML en AEM, la cookie AEM &#39;saml_request_path&#39; devuelve un valor no válido debido a caracteres ya codificados. NPR-13517: Revisión proactiva para GRANITE-11722 y GRANITE-14414

### Integración de soluciones {#solution-integration}

* Después de integrar AEM 6.2 con Search&amp;Promote, si un usuario busca un término que devuelve una pancarta, la funcionalidad de búsqueda no responde. NPR-14549: CFP para CQ-109631

### Dynamic Media {#dynamic-media}

* Numerosos trabajos de sling de AEM-Scene7 que se crearon y cancelaron durante AEM activación se registran como trabajos de archiving durante la replicación. NPR-12835: revisión para CQ-86115

### Seguridad {#security-5}

* Solicitud para resolver el problema de validación de entrada en el filtro WCMDebug. NPR-12444: Solicitud de revisión para CQ-94890
* Solicitud proactiva para corregir el comportamiento de XSS al utilizar el Asistente para crear inicio.\
   NPR-13062: Solicitud de revisión para CQ-99577

#### Paquete de complemento de Forms {#forms-add-on-package-19}

`Adaptive Forms`

* Al crear un panel repetible con formularios adaptables, el título del panel no se puede actualizar en tiempo de ejecución. NPR-15325
* Cuando se establece el valor predeterminado de un botón de radio y se selecciona un valor distinto del predeterminado al guardar o enviar, el valor no se muestra en el relleno previo. NPR-15304
* Google Chrome muestra un comportamiento incorrecto al utilizar el evento de opciones para rellenar dinámicamente la lista desplegable y enviar el valor del elemento seleccionado. NPR-15198
* Al crear un panel repetible con formularios adaptables, el título del panel no se puede actualizar en tiempo de ejecución. NPR-15181
* Cuando se utiliza el modo de edición para formularios adaptables, se detectan errores de JavaScript como - &#39;El controlador del componente no es válido&#39; y &#39;la guía no está definida&#39;. NPR-15112
* El fragmento de carga diferida dentro de un panel repetitivo no funciona correctamente. NPR-13916, NPR-14785

`Correspondence Management`

* Los recursos de Correspondence Management con `'Repeat with condition'`expresión establecida no se muestran correctamente. NPR-14844
* Al buscar un recurso de Gestión de correspondencia (como una carta, un fragmento de documento o cualquier otro tipo), el icono Cola de descarga no aparece en la barra de herramientas. NPR-14745
* Al crear un módulo de Lista, no funciona el alternado de las propiedades específicas del recurso (como editable y obligatorio). NPR-14689
* El panel Elementos de datos de la utilidad Expresión Builder se sigue cargando en caso de que se cree un módulo de condición sin seleccionar un diccionario de datos. NPR-14688
* Al obtener una vista previa de una carta, los usuarios no pueden utilizar espacios de tabulación para alinear el contenido en formato de tabla. NPR-14481
* Al exportar recursos de Correspondence Management de forma masiva desde la interfaz de usuario, el servidor de AEM Forms genera registros innecesarios. NPR-15226
* Cuando se obtiene una vista previa de una carta, el texto justificado aparece en una fuente diferente. NPR-15468

`**Forms Portal**`

* Los datos adjuntos de los formularios enviados en el portal de Forms no son visibles cuando se envía un nuevo borrador del envío al portal. NPR-13515

`**Forms Manager**`

* Al navegar en el directorio *FormsDocuments*, el botón Pegar no se muestra cuando el usuario copia cualquier recurso y luego navega a una carpeta diferente. CQ-111327

#### Instalador JEE de Forms {#forms-jee-installer-19}

`Rights Management`

* El evento de auditoría relacionado con el inicio de sesión del usuario se registra con una hora no válida. No se puede rastrear la hora correcta para el evento de auditoría. NPR-13107
* Adobe Acrobat Reader y Microsoft Office no pueden abrir documentos protegidos con autenticación extendida. NPR-14482

`Process Management`

* Cuando se devuelve una tarea de borrador reenviada al usuario inicial en el espacio de trabajo HTML, la tarea no aparece en la cola del usuario inicial. NPR-15178

`Assembler Service`

* AEM Forms no puede validar un PDF/A-2b con más de dos firmas. NPR-14101

`XTG`

* Al imprimir un documento con una bandeja de derivación de impresora, la función `GeneratePrintedOutput` no permite recuperar papel de la bandeja de derivación derecha. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer se bloquea cuando el usuario ejecuta la utilidad Revisión de ortografía con la configuración regional de formulario seleccionada como francés (Canadá). NPR-13740
* Forms Designer se bloquea cuando el usuario selecciona calcular evento o validar evento para un campo de formulario y cambia el lenguaje a JavaScript e introduce `this.` en la ventana **[!UICONTROL Editor de secuencias de comandos]**. NPR-12974

### Paquetes de funciones incluidos en CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Paquete Añada de Forms):

* Cuando se crea un formulario adaptable a partir de un archivo XDP, la tabulación para accesibilidad no sigue el patrón definido. NPR-12562

`Adaptive forms` (Paquete Añada de Forms):

* El Generador de reglas para formularios adaptables no proporciona acceso basado en roles. Los cambios realizados por un autor no se pueden rastrear. NPR-12840

`Core` (Instalador JEE de Forms):

* La funcionalidad de uso compartido de recursos de CoreCross Origen (CORS) como filtro servlet no está habilitada para Jjefe+. NPR-13050

## Descargar instrucciones para CFP mediante distribución de software {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Para los clientes de AEM Forms, es esencial instalar AEM paquete de complementos de formularios después de instalar cualquier AEM Service Pack, Cumulative Service Pack o Feature Pack.

Puede descargar el paquete CFP directamente desde Distribución de software o realizar los siguientes pasos:

1. Abra [Distribución de software](https://experience.adobe.com/downloads). Necesita un Adobe ID para iniciar sesión en la distribución de software.
1. Toque **[!UICONTROL Adobe Experience Manager]** disponible en el menú del encabezado.
1. Toque el nombre del paquete, seleccione **[!UICONTROL Aceptar términos del EULA]** y toque **[!UICONTROL Descargar]**.

## Instrucciones de instalación para CFP {#installation-instructions-for-cfp}

Esta sección es una guía de los requisitos y pasos para instalar el CFP.

### Antes de realizar la instalación  {#before-you-install}

>[!NOTE]
>
>Los paquetes de funciones opcionales proporcionados por Adobe dependen de la versión de la versión y del paquete de correcciones acumulativas. Si tiene instalado algún paquete de funciones, póngase en contacto con el [equipo de atención al cliente de AEM](https://helpx.adobe.com/es/marketing-cloud/contact-support.html) para validar la compatibilidad con este paquete de correcciones acumulativas para AEM 6.2.

>[!NOTE]
>
>Se recomienda ejecutar la validación en todos los paquetes de instalación nuevos antes de intentar instalar el paquete. La prevalidación analiza e informa de los errores encontrados antes de la instalación y avisa a los usuarios de dichos errores, superposiciones y permisos de forma proactiva.
>
>Puede acceder a la documentación de la opción Validar en [https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator)

* AEM 6.2 Service Pack 1 es un requisito previo para la PPC. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 1 de AEM 6.2](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).

* La descarga del paquete de correcciones acumulativas está disponible en [Distribución de software](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20), a la que puede acceder directamente desde la instancia de AEM.
* Para una implementación de clúster que utilice ( RDBMK o MongoDB), el paquete CFP se puede instalar en cualquiera de las instancias de creación que utilice el Administrador de paquetes.

* Antes de instalar el paquete de correcciones acumulativas, asegúrese de realizar una instantánea o una copia de seguridad de su instancia de AEM.
* No se admite la desinstalación de CFP.

### Instalar CFP mediante distribución de software {#install-the-cfp-via-package-share}

Realice los siguientes pasos para instalar el paquete de correcciones acumulativas en una instancia existente de AEM 6.2 SP1:

1. Haga clic en el vínculo [Distribución de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) para descargar el paquete.

1. Abra [Administrador de paquetes](http://localhost:4502/crx/packmgr/index.jsp) y haga clic en **[!UICONTROL Cargar paquete]** para cargar el paquete.

1. Seleccione el nombre del paquete y haga clic en **[!UICONTROL Instalar]**.

### Instalación automática {#automatic-installation}

CFP se puede instalar automáticamente en una instancia en ejecución de las siguientes maneras:

* Coloque el paquete en ../crx-quickstart/install mientras el servidor se está ejecutando. El paquete se instala automáticamente.
* Utilice la [API HTTP del Administrador de paquetes](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html); asegúrese de utilizar `cmd=install&recursive=true` para instalar el paquete anidado.

### Validar la instalación {#validate-installation}

1. La página Información del producto (/system/console/ productinfo ) debe mostrar ahora la cadena de versión actualizada &quot;Adobe Experience Manager, versión 6.2.0.SP1-CFP20&quot; en Productos instalados.
1. Todos los paquetes OSGI tienen el valor ACTIVO o FRAGMENTO en la consola OSGI (utilice la consola web:/system/console/bundles).

>[!NOTE]
>
>Al instalar correctamente el paquete, aparece un mensaje informativo que indica que el paquete de contenido se ha instalado correctamente, como &quot;Paquete de contenido AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 instalado correctamente&quot;.

>[!NOTE]
>
>Desde AEM 6.2 SP1-CFP1, el nivel de registro en Jackrabbit FileVault ha cambiado de INFO a DEBUG para la mayoría de los mensajes. Para obtener los registros de instalación de un paquete de contenido instalado en AEM 6.2 SP1-CFP1 o superior, habilite el nivel de registro DEBUG para `org.apache.jackrabbit.vault.packaging.impl`.

### Instalación de de AEM Forms {#install-forms}

>[!NOTE]
>
>Omita este paso si no utiliza AEM Forms.

#### Instale los complementos para AEM Forms  {#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms en JEE solamente**) El procedimiento para instalar un CFP en AEM Forms en JEE se describe en [Instalación de CFP en AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Asegúrese de que ha instalado el paquete CFP AEM 6.2 SP1.
1. Descargue el paquete adicional de Forms correspondiente en [AEM Forms releases](aem-forms-releases.md) para su sistema operativo.
1. Instale el paquete del complemento de Forms tal como se describe en [Instalación de paquetes del complemento de formularios AEM](https://helpx.adobe.com/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html).

#### Instalación de paquetes JEE de AEM Forms {#install-aem-forms-jee-bundles-package}

Las correcciones en el instalador JEE de AEM Forms se entregan mediante un instalador independiente. Para obtener información sobre la instalación de un CFP en AEM Forms en JEE, consulte [Instalación de CFP en el JEE de AEM Forms](install-cfp-aem-forms-jee.md).

#### Programa de instalación del diseñador Forms Designer  {#designer-installer}

1. Para instalar la actualización, ejecute el archivo Designer6.2.0_&lt;Language>_Cumulative_QF.msp.
1. En la pantalla de bienvenida, haga clic en **Actualizar**. Se inicia la instalación.
1. Una vez finalizada la instalación, haga clic en **Finalizar**.

## Parámetros de tiempo de espera configurables por el usuario para DTM, Analytics, Destinatario, Conexiones de Search &amp; Promote {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Con AEM paquete de correcciones acumulativas 6.2 SP1-CFP7 y versiones posteriores, los períodos de tiempo de espera de conexión se pueden configurar en todas las conexiones anteriores, según los detalles siguientes:

| **Conexiones** | **Tiempo de espera de la conexión*** | **Tiempo de espera de zócalo**** |
|---|---|---|
| DTM | 30000 ms | 30000 ms |
| Análisis | 30000 ms | 30000 ms |
| Destino | 60000 ms | 30000 ms |
| Search&amp;Promote | 30000 ms | 30000 ms |

* **Tiempo de espera de conexión***: tiempo de espera en milisegundos hasta que se establece una conexión. Un valor de tiempo de espera de cero se interpreta como un tiempo de espera infinito.
* **Tiempo de espera de socket****: tiempo de espera en milisegundos para esperar datos o un período máximo de inactividad entre dos paquetes de datos consecutivos.

>[!NOTE]
>
>Con AEM paquete de correcciones acumulativas 6.2 SP1-CFP6 y versiones posteriores, la configuración OSGi utilizada para la integración de Search &amp; Promote es la configuración proxy de componentes HTTP Apache. Ya no se utiliza la configuración proxy del cliente HTTP 3.1 de Day Commons.

## Deshabilitar el estado de replicación en la consola de etiquetado (IU clásica) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Si utiliza CFP3 o posterior, siga estas instrucciones para deshabilitar el estado de replicación en la consola Etiquetado de la IU clásica:

* Overlay *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;* en */apps*

* Añadir `replicationStateRequired`: &quot;false&quot; después de la línea 416.

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## La última actualización de Java 8 131 genera una excepción (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Estas opciones de configuración son específicas para los clientes de AEM Forms que utilizan la seguridad de Documento.

NPR-21355 está incluido en CFP12.1. Si va a instalar CFP12.1 o posterior, realice el siguiente procedimiento para configurar NPR-21355 en el servidor de aplicaciones JBoss. Si va a instalar CFP12.1 en el servidor AEM Forms que se ejecuta en servidores de aplicaciones Oracle WebLogic o IBM WebSpehere, no se requiere ninguna configuración adicional:

1. Haga una copia de seguridad, elimine y cree un nuevo archivo module.xml. La ubicación predeterminada del archivo es [directorio_de_instalación_de_Forms_AEM]/jjefe/módulos/sistema/capas/base/com/adobe/livecycle/main/

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

1. Cree una copia de seguridad de los archivos jsafeFIPS.jar, jsafeJCEFIPS.jar y certjFIPS.jar ubicados en [directorio_de_instalación_de_Forms]/jjefe/módulos/sistema/capas/base/com/adobe/livecycle/main/ y elimine los archivos del directorio mencionado.

   Póngase en contacto con [Soporte técnico de Adobe](https://helpx.adobe.com/marketing-cloud/contact-support.html) para obtener nuevos archivos JAR. Coloque los archivos JAR obtenidos de [Compatibilidad con Adobe](https://helpx.adobe.com/marketing-cloud/contact-support.html) en [AEM_Forms_Installation_directory]/jpatrón/módulos/system/ayers/base/com/adobe/livecycle/main/

1. (Solo Windows) Modifique los archivos de configuración `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` o `domain.conf.bat`:

   * Para el servidor JBoss en la configuración independiente, abra el archivo standalone.conf.bat para editarlo.
   * Para el servidor JBoss en la configuración de clúster, abra el archivo domain.conf.bat para editarlo.

   Añada las líneas siguientes al final y guarde el archivo:

   establezca &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   configure &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. (Solo SO basado en Linux) Modifique los archivos de configuración [AEM_Forms_Installation_directory]/jboss/standalone.conf o domain.conf:

   * Para el servidor JBoss en la configuración independiente, abra el archivo standalone.conf para editarlo.
   * Para el servidor JBoss en la configuración de clúster, abra el archivo domain.conf para editarlo.

   Añada las líneas siguientes al final y guarde el archivo:

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## Ajustes de configuración necesarios para NPR-19778 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>El NPR-19778 es parte del CFP14.

El recuento de la cola compartida no se actualiza, de forma predeterminada, para otros usuarios cuando un usuario solicita una tarea. Para ello, hemos introducido una nueva propiedad. Siga los pasos a continuación para configurar esta propiedad en la instancia de AEM:

1. Vaya a la IU de administración -> Servicios -> Espacio de trabajo -> Administración global.
1. Exportar configuración global.
1. En el archivo XML descargado, agregue la etiqueta `<client_tasksPollingInterval>10</client_tasksPollingInterval>` Aquí, 10 es el valor de ejemplo en segundos. Puede modificarlo en consecuencia.
1. Guarde el archivo.
1. Vuelva a la IU de administración -> Servicios -> Espacio de trabajo -> Administración global.
1. Importe el archivo xml en la sección Importar configuración global.
1. Ahora puede cerrar la sesión del sistema y volver a iniciarla.
1. Recuento de inicios de cola compartidos que se actualizan para otros usuarios del espacio de trabajo.
1. Para desactivar la encuesta, cambie el valor a 0 y vuelva a importar el archivo XML.

## Cambios en la interfaz de usuario {#ui-changes}

* Cambio de comportamiento en la visualización de títulos en la tarjeta de imagen para una imagen que tiene dc: propiedad title establecida en String [] ( multifield ): solo se mostrará el último título modificado en la tarjeta de imagen en la interfaz de usuario, aunque todos los títulos se guardarán en CRX. Revisión para CQ-4217165

## Problemas conocidos {#known-issues}

* Al actualizar AEM 6.2SP1-CFP19 y AEM 6.2SP1-CFP20 desde CFP18, se cambia la redirección raíz a la página de bienvenida de la IU clásica en lugar de /sites.html/content. Es posible que tenga que corregir sling: Propiedad de destinatario de /welcome.html a /index.html con el Explorador de CRX. Este problema no se observa al actualizar desde CFP17 o una versión anterior.

Pueden producirse los siguientes errores transitorios al instalar AEM 6.2 SP1-CFPx. Sin embargo, no se requiere resolución para estos errores porque no afectan a la instancia de AEM y desaparecen después de instalar CFP:

* Al actualizar AEM instancia 6.2SP1-CFP20 a AEM 6.5, es posible que algunas direcciones URL personales no funcionen como:

   * */projects.html*
   * */sites.html*

Sin embargo, la solución consiste en reiniciar la instancia de AEM después de una actualización.

* Error interno del servidor HTTP 500 al abrir la página de detalles del componente Webconsole.
* Se producen errores porque **crear instancia de componente** y **la fábrica de servicios devolvió null** debido al reinicio del repositorio:

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] No se puede crear una instancia de componente debido a un error al enlazar profileManager de referencia
   * org.apache.sling.commons.Planificador FrameworkEvent ERROR (org.osgi.framework.ServiceException: La fábrica de servicios devolvió un valor nulo. (Componente: com.day.cq.tagging.impl.TagGarbageCollector (1687))

* Error observado en la instalación de CFP en Mongo y DB2: **org.apache.sling.discover.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Excepción: java.lang.NullPointerException**. Este error no se producirá después de instalar un CFP sobre CFP8.
* (Tarea de actualización del Planificador de mantenimiento de Granite de Adobe) com.adobe.granite.mantenimiento.impl.TaskScheduler: No se encontró ninguna tarea de mantenimiento con el nombre WorkflowPurgeTask para el granito de ventana:semanal
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
* Al instalar CFPx en AEM 6.2 SP1 que incluye el paquete de funciones Etiquetas inteligentes, el paso de flujo de trabajo agregado anteriormente para Recursos de etiquetas inteligentes se elimina del flujo de trabajo de recursos de actualización de DAM.

Consulte lista de [Problemas conocidos en AEM 6.2 SP1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known Issues).

## Uber Jar {#uber-jar}

El Uber Jar para 6.2 SP1-CFP20 está disponible en [repositorio de Maven Público de Adobe](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/).

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

## Los paquetes de contenido y los paquetes OSGI incluidos {#osgi-bundles-and-content-packages-included-5}

El siguiente texto documentos la lista de paquetes OSGI y paquetes de contenido incluidos en la CFP.

* [Lista de los paquetes OSGi incluidos en AEM 6.2 SP1-CFP20](assets/do-not-localize/updated.txt)
* [Lista de paquetes de contenido incluidos en AEM 6.2SP1-CFP20](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [Página de correcciones de AEM 6.2](https://helpx.adobe.com/es/experience-manager/kb/aem62-available-hotfixes.html)
>* [Notas de la versión de AEM 6.2 SP1](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [Notas de la versión de AEM 6.2](https://docs.adobe.com/docs/es/aem/6-2/release-notes.html)
>* [Página de productos AEM](http://www.adobe.com/es/solutions/web-experience-management.html)
>* [Documentación de AEM 6.2](https://docs.adobe.com/content/docs/en/aem/6-2.html)
>* [Actualizaciones del producto ](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) Prioritarias de suscripción a  [Adobe](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)

