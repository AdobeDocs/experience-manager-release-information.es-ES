---
title: Paquete de correcciones acumulativas de AEM 6.3
description: Notas de la versión de AEM 6.3 Cumulative Fix Pack
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '15916'
ht-degree: 79%

---


# Notas de la versión de AEM 6.3 Cumulative Fix Pack {#release-notes-aem-cumulative-fix-pack}

## Información de la versión {#release-information}

| **Producto** | Adobe Experience Manager |
|---|---|
| **Versión** | 6.3 |
| **Versión** | Paquete de correcciones acumulado 6.3.3.8 en [PackageShare](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8), [Distribución de software(Beta)](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) |
| **Requisitos previos** | [Paquete de servicio 3 de AEM 6.3 (6.3.3.0)](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **Disponibilidad general** | 05 de marzo de 2020 |

### Paquete de correcciones acumulativas {#cumulative-fix-pack}

Adobe presentó un modelo de entrega única para la publicación de correcciones. En lugar de lanzar correcciones urgentes para problemas individuales, Adobe ahora publica un paquete de correcciones acumulativas (CFP) todos los meses (sujeto a la aprobación de comprobaciones de calidad). Un CFP es un paquete de contenido agregado para varias correcciones. Los archivos CFP incluyen principalmente correcciones de errores, pero también pueden incluir paquetes de funciones. Tienen las siguientes ventajas con respecto a las versiones de revisiones individuales:

* Carácter acumulativo (por ejemplo, un CFP contiene correcciones enviadas a través de los CFP anteriores)
* Mayor control de calidad
* Instalación simplificada (el usuario instala un CFP como paquete único que no tiene dependencias, excepto el último paquete de servicio)

Para obtener más información sobre CFP y otros tipos de liberaciones, consulte [Definiciones de Vehículos de Liberación de Mantenimiento.](https://docs.adobe.com/content/docs/en/aem/6-3/deploy/maintenance-release-vehicle-definitions.html)

## Información de la versión {#about-the-release}

El paquete de correcciones acumulativas 6.3.3.8 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 3 (6.3.3.0) de AEM 6.3 en septiembre de 2018.

AEM Cumulative Fix Pack 6.3.3.8 depende de AEM 6.3 Service Pack 3. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.3.x después de instalar AEM 6.3 Service Pack 3. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 3 de AEM 6.3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Los aspectos destacados del **AEM paquete de correcciones acumulativas** son:

* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.20.

>[!CAUTION]
>
>La aplicación de CFP sin validar la compatibilidad entre los paquetes de funciones instalados puede provocar errores en el sistema o la pérdida de las configuraciones personalizadas, lo que podría necesitar la restauración desde la copia de seguridad.

>[!NOTE]
>
>En AEM casos con una versión inferior a 6.3.3.0, Adobe recomienda implementar ing SP/CFP a través de la carpeta de instalación para clientes con un gran número de usuarios en AEM instancia.

>[!NOTE]
>
>MongoDB Enterprise 3.6 se admite a partir de la versión 6.3.3.1 de AEM.

## Lista de problemas {#changes}

Esta sección enumera todos los problemas y revisiones incluidos en la CFP actual.

Además, este CFP incluye revisiones entregadas en [paquetes de correcciones acumulativas anteriores](#previous).

### Assets {#assets}

* La página Añadir a colección no muestra todas las colecciones disponibles en la Vista de tarjetas al agregar recursos a la colección (NPR-32537).

### Sites {#sites}

* Al seleccionar un parsys y un componente dentro de él y utilizar el método abreviado de teclado para eliminar los elementos seleccionados, la acción elimina tanto el componente como su parsys principal (NPR-32071).
* Cuando se guardan las propiedades de una página, se crea un nodo incorrecto (NPR-31774).

### Integraciones {#integrations}

* ReportSuitesServlet es vulnerable a SSRF (NPR-32162).

### Objetivo de campaña {#campaign-targeting}

* El contenido de un componente cambiado, en la instancia de Autor y luego activado, no se ve en la instancia de Publish hasta que se reinicia el componente **com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489 y NPR-32232).
* Las funciones de Contexthub se bloquean al publicar (NPR-31170).

### Brand Portal {#brand-portal}

* Adobe I/O no está integrado con Adobe Experience Manager 6.3 para Brand Portal (NPR-32056).

### Forms {#forms}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

#### Paquete de complemento de Forms {#forms-add-on-package}

>[!NOTE]
>
>Los paquetes de complementos de AEM Forms ayudan a alinear la funcionalidad de los formularios con los paquetes de servicios de AEM y los paquetes de correcciones acumulativas. Por lo tanto, es esencial instalar el paquete de complementos de AEM Forms después de instalar cualquier paquete de servicio, paquete acumulativo o paquete de funciones de AEM.

* Designer: Si la opción de etiquetado está activada, el borde del subformulario desaparece en la salida PDF generada (NPR-32324 y NPR-32545).
* Designer: Si hay celdas combinadas en una tabla, la prueba de accesibilidad falla para el archivo PDF de salida convertido desde un formulario XDP mediante el servicio de salida (NPR-32068).
* Seguridad de documento: Un archivo PDF protegido no se puede abrir sin conexión con la opción `DisableGlobalOfflineSynchronizationData` establecida en `True` (NPR-32080).

## Revisiones y paquetes de funciones incluidos en los paquetes de correcciones acumulativas anteriores {#previous}

### Paquete de correcciones acumulativas 6.3.3.7 {#cumulative-fix-pack-1}

El paquete de correcciones acumulativas 6.3.3.7 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 3 (6.3.3.0) de AEM 6.3 en septiembre de 2018.

AEM Cumulative Fix Pack 6.3.3.7 depende de AEM 6.3 Service Pack 3. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.3.x después de instalar AEM 6.3 Service Pack 3. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 3 de AEM 6.3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Recursos {#assets-1}

* Los recursos seleccionados (en la vista de columna en la IU táctil) antes de seleccionar la opción de filtro en la lista desplegable Solo contenido y, a continuación, seleccionar la opción de mover, hará que los recursos también se muevan (NPR-30693).
* La variable `${extension}` no se procesa en la instancia de autor durante el procesamiento del flujo de trabajo (NPR-31694).
* El valor de caducidad (tiempo de espera de caché del cliente) configurado para el modo híbrido de Dynamic Media no se replica en el entorno de entrega de Dynamic Media (NPR-31114).
* Los recursos se replican en la instancia Publicar de la instancia de Autor que se ejecuta en una implementación Dynamic Media - Scene7 incluso después de utilizar los filtros predeterminados (NPR-30856).

### Sitios {#sites-1}

* Las propiedades de una página principal no se pueden cargar y se devuelve una excepción NullPointerException. El problema se resuelve al agregar la propiedad cq:blueprint (NPR-30901).
* Las configuraciones de implementación no se recuperan correctamente de blueprintConfig en el nodo raíz. La desactivación sucede tanto para los modelos como para las copias en vivo. La desactivación solo debe iniciarse para el modelo (NPR-30866).
* Cuando un usuario despliega una página, el cuadro de diálogo de configuración muestra rutas de una copia activa duplicadas (NPR-30438).
* De forma predeterminada, la matriz del Editor de texto enriquecido (RTE) aplica el tamaño de fuente en línea a los elementos de forma inesperada (NPR-31283, NPR-30922).
* No se puede sincronizar la campaña de Adobe Campaign que contenga el componente de importador de diseños incorporado (NPR-30890).
* Editor de texto enriquecido (RTE). no permite insertar una tabla incrustada como elemento de una lista (NPR-30878).
* Cuando un usuario se centra en los campos del carril izquierdo y utiliza un método abreviado de teclado para pegar contenido, pega el contenido del portapapeles del editor de páginas en lugar del contenido copiado de los campos del carril izquierdo (NPR-31173).
* Cuando un usuario edita un fragmento de contenido, se restaura la variación ya eliminada del fragmento de contenido (NPR-31272).
* AEM Site no tiene la opción de crear una copia de idioma (NPR-30690).
* Las acciones del Editor de páginas no tienen los controles para desplegar copias activas (NPR-30613).

### Communities  {#communities}

* Los títulos de las actividades y las notificaciones son incoherentes (NPR-30940).
* Los informes de Analytics no se completan en el entorno de creación de AEM; aparece una página en blanco (NPR-30905).
* La paginación no funciona correctamente en los blogs de Communities (NPR-30827).

### Foundation {#foundation}

* Las actualizaciones en la configuración del tamaño del búfer para el servicio HTTP basado en Jetty no se guardan (NPR-30925).

### Forms {#forms-1}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-1}

>[!NOTE]
>
>Los paquetes de complementos de AEM Forms ayudan a alinear la funcionalidad de los formularios con los paquetes de servicios de AEM y los paquetes de correcciones acumulativas. Por lo tanto, es esencial instalar el paquete de complementos de AEM Forms después de instalar cualquier paquete de servicio, paquete acumulativo o paquete de funciones de AEM.

#### Formularios adaptables {#adaptive-forms}

* Los valores flotantes calculados con una secuencia de comandos no se muestran correctamente en un formulario que forme parte de un conjunto de formularios (NPR-30802).

#### Formularios HTML5  {#html-forms}

* Al generar la vista previa HTML5 de un formulario XDP, se muestra un parpadeo al agregar instancias de un subformulario (NPR-30908).

### Instalador JEE de Forms  {#forms-jee-installer}

#### Servicios de documento {#document-services}

* OutputService muestra una respuesta incorrecta después de aplicar un parche para corregir problemas de HTML a PDF (NPR-31504).

#### Servicio PDFG  {#pdfg-service}

* El recuento máximo de reutilización con la consola JMX no se muestra para el servicio HTML2PDF (NPR-30305).

#### Base JEE  {#foundation-jee}

* El recuento máximo de reutilización con la consola JMX no se muestra para el servicio HTML2PDF (NPR-30136).

### Paquete de correcciones acumulativas 6.3.3.6 {#cumulative-fix-pack-2}

El paquete de correcciones acumulativas 6.3.3.6 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 3 (6.3.3.0) de AEM 6.3 en septiembre de 2018.

AEM Cumulative Fix Pack 6.3.3.6 depende de AEM 6.3 Service Pack 3. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.3.x después de instalar AEM 6.3 Service Pack 3. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 3 de AEM 6.3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Recursos {#assets-2}

* Añadir el vídeo Dynamic Video solo devuelve los 100 elementos principales del conjunto de resultados. NPR-30441; revisión para CQ-4213561
* Problema de conectividad de etiquetas inteligentes de Adobe a través de Datapower. NPR-30026: revisión para CQ-4269457
* Si se descomprime un archivo con una carpeta que tenga un signo de porcentaje (%) en su nombre no se podrá abrir con la interfaz de recursos. NPR-29989: revisión para CQ-4270467
* El procesamiento de subrecursos de archivos PDF de gran tamaño provoca una excepción OutOfMemoryError (OOME). NPR-29851: revisión para CQ-4269574

### Sitios {#sites-2}

* Error de ContextHub durante la integración de AEM y Campaign. NPR-30624: revisión para CQ-4250790
* Las propiedades de metadatos “onTime” u “offTime” guardadas en los recursos no se recuperan si se reinicia el servidor de AEM. NPR-30412: revisión para CQ-4272784
* Al generar una exportación de CSV, agregar columnas personalizadas para la vista de lista rompe el informe. NPR-30208: revisión para CQ-4273344
* Los informes OOTB en /etc/reports/ no funcionan correctamente y no se muestra el gráfico de datos históricos. NPR-30016: revisión para CQ-4220180
* El valor del parámetro de solicitud resourceType se copia en el valor de un atributo de etiqueta HTML que se encapsula entre comillas dobles. NPR-29832: revisión para CQ-4255365

### Comunidades  {#communities-1}

* Problema de contenido duplicado con la consola de moderación de AEM Communities. NPR-30667: revisión para CQ-4276829

### Traducción  {#translation}

* Problema de traducción: solo unos pocos componentes se traducen mediante traducción automática. NPR-30079: revisión para CQ-4273764
* Al utilizar el marco de traducción, la adición de páginas a varios trabajos de traducción activa un error. NPR-29746: revisión para CQ-4270953

### Forms {#forms-2}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-2}

>[!NOTE]
>
>Los paquetes de complementos de AEM Forms ayudan a alinear la funcionalidad de los formularios con los paquetes de servicios de AEM y los paquetes de correcciones acumulativas. Por lo tanto, es esencial instalar el paquete de complementos de AEM Forms después de instalar cualquier paquete de servicio, paquete acumulativo o paquete de funciones de AEM.

#### HTML5 Forms {#html-forms-1}

* Cuando se utiliza la opción de acceso al escritorio no visual en el modo Examinar para leer un formulario de HTML5, el navegador Chrome lee el elemento &quot;gráfico&quot; antes que cada gráfico vectorial escalable (SVG) en el diseño de formulario. NPR-30451: revisión para CQ-4274732

#### Forms: integración back-end {#forms-backend-integration}

* No se puede ver el servicio o la fuente de datos para la conexión de la base de datos al crear el Modelo de datos de formulario (FDM). NPR-30108: revisión para CQ-4273359

### Instalador JEE de Forms  {#forms-jee-installer-1}

#### Forms: servicios de documentos {#forms-document-services}

* Cuando se hace una prueba de carga en el servicio HTML a PDF, se produce un error y se elimina la configuración del tipo de archivo del servidor de AEM Forms. NPR-30111, NPR-30086: revisión para CQ-4271495

### Paquete de correcciones acumulativas 6.3.3.5  {#cumulative-fix-pack-3}

El paquete de correcciones acumulativas 6.3.3.5 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 3 (6.3.3.0) de AEM 6.3 en septiembre de 2018.

AEM Cumulative Fix Pack 6.3.3.5 depende de AEM 6.3 Service Pack 3. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.3.x después de instalar AEM 6.3 Service Pack 3. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 3 de AEM 6.3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Los aspectos destacados del **AEM paquete de correcciones acumulativas** son:

* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.17.

### Recursos {#assets-3}

* Se ha actualizado la interfaz DAM DMGgateway para que sea compatible con varias partes de S3. NPR-29740: revisión para Q-4226303
* No se puede eliminar una representación de imagen en un recurso de vídeo desde la página de detalles del recurso. NPR-29417: revisión para CQ-4268675
* El propietario no puede crear una carpeta privada dentro de una carpeta privada. NPR-29397: revisión para CQ-4229830
* Al cargar un archivo de ilustraciones de Adobe Illustrator de más de 2 GB, se genera un error de espacio en la acumulación de Java. NPR-29265: revisión para CQ-4226217
* Los recursos se vuelven inutilizables después de que el servicio DAM CQ Mime Type aplique texto para m3u8. NPR-29259: revisión para CQ-4264052
* La opción Crear no funciona al intentar crear colecciones en Edge. NPR-29248: Revisión para CQ-4265699 y CQ-4265438
* La función compartida de vínculos de recursos muestra tarjetas grises en blanco para algunos recursos de la carpeta. NPR-29831: revisión para CQ-4270187
* Las nuevas etiquetas agregadas a los recursos no se pueden guardar ni pueden desaparecer de las propiedades. Revisión para CQ-4271931, CQ-4270476

### Sitios {#sites-3}

* Cuando se utiliza CoralUI con Multifield, se almacena el parámetro fileReferenceParameter en el nivel de componente en lugar de en el nivel de multicampo. NPR-29535: revisión para CQ-4266129
* Problema al intentar comparar la versión de página más reciente y la versión actual en AEM 6.3.3.3. NPR-29532: Revisión para CQ-4269639
* El campo de la ruta se abre en la ruta raíz independientemente de la ruta de acceso especificada para la búsqueda. NPR-29398: revisión para CQ-4268897
* (Fragmentos de experiencia) FacebookApplication#setUpApp utiliza una API obsoleta, que ya no funciona. NPR-29213: revisión para CQ-4266630
* Se genera una alerta de error al añadir componentes a la página WCM cuando la minimización está habilitada en la instancia. NPR-29476: revisión para CQ-4266197
* Las propiedades vacías y multiples no se propagan desde el modelo durante el despliegue. La restauración de la Copia activa con modelo no funciona para los componentes.NPR-29252: Revisión para CQ-4264928, CQ-4264926, CQ-4267722
* Minimizar el Editor de texto enriquecido desde la pantalla completa mientras se encuentra en el modo de edición de fuente provoca la pérdida del contenido. NPR-28838: revisión para CQ-4260584

### Comunidades  {#communities-2}

* Los visitantes y los miembros que no tengan privilegios de moderador pueden ver las publicaciones pendientes o no aprobadas pegando la dirección URL. NPR-29726: revisión para CQ-4271124
* Se observa un tiempo de respuesta alto de hasta 40-50 segundos cuando el usuario inicia sesión en la comunidad. NPR-29679: revisión para CQ-4269444
* No se puede restablecer la contraseña cuando se ha iniciado sesión con un nombre de usuario y un correo electrónico diferentes, ya que la clave parece generarse con un nombre de usuario y un correo electrónico intercambiados. NPR-29281: revisión para CQ-4268694

### Fragmentos de experiencias {#experience-fragments}

* No se pueden exportar fragmentos de experiencia para que sean objetivos cuando se utiliza una imagen inteligente. Revisión para CQ-4269606

### Replicación {#replication}

* El componente del agente de replicación es susceptible a una vulnerabilidad que revela información confidencial a usuarios no autorizados. NPR-29613: revisión para Granite-25070
* Los datos que proporcionó el usuario no se evitan en la salida del componente `cq/replication/components/agent`, lo que provoca una vulnerabilidad en la ejecución almacenada de scripts en sitios múltiples (XSS). NPR-29452: revisión para CQ-4266263

### Forms {#forms-3}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

### Paquete de complemento de Forms {#forms-add-on-package-3}

* No hay nuevas correcciones de AEM Forms en el paquete complementario de Forms.

### Instalador JEE de Forms  {#forms-jee-installer-2}

* No hay nuevas correcciones de AEM Forms en el instalador JEE de Forms.

### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión 6.3.3.5.  {#osgi-bundles-and-content-packages-included-in}

Lista de paquetes OSGi incluidos en AEM 6.3.3.5

[Obtener archivo](assets/do-not-localize/6_5-bundle-list.txt)

Lista de paquetes de contenido incluidos en AEM 6.3.3.5

[Obtener archivo](assets/do-not-localize/content_packages6335.txt)

### Paquete de correcciones acumulativas 6.3.3.4 {#cumulative-fix-pack-4}

El paquete de correcciones acumulativas 6.3.3.4 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 3 (6.3.3.0) de AEM 6.3 en septiembre de 2018.

AEM Cumulative Fix Pack 6.3.3.4 depende de AEM 6.3 Service Pack 3. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.3.x después de instalar AEM 6.3 Service Pack 3. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 3 de AEM 6.3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Los aspectos destacados del **AEM paquete de correcciones acumulativas** son:

* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.16.
* Se ha añadido tiempo de espera de conector y tiempo de espera de conexión en los agentes de replicación de Brand Portal.

### Recursos {#assets-4}

* Si se vuelve a cargar un archivo con el mismo nombre, no se generan representaciones para los nuevos recursos procesados. NPR-28643: revisión para CQ-4262286
* Error de CommandLineProcess del flujo de trabajo con un nombre de archivo con una sola comilla. NPR-28805: revisión para CQ-4262287
* Los valores son diferentes entre la página de recopilación y la página de recopilación cuando se usa el filtro. NPR-28642: revisión para CQ-4261405
* CommitFailedException activa la carga de los recursos de archivos zip grandes. NPR-28528: revisión para CQ-4260903
* Los metadatos de la carpeta no se pueden guardar al editar una carpeta que contiene caracteres especiales. NPR-28211: revisión para CQ-4260401
* No se pueden eliminar las representaciones de imágenes de un recurso de vídeo desde la página de detalles del recurso. NPR-29149: revisión para CQ-4266073
* La entrega del vídeo de escritorio DMS7 mediante DMComponent utiliza la descarga progresiva para reproducir el vídeo en modo de publicación y no se retransmite. NPR-28754: revisión para CQ-4263732
* No se pueden crear ni editar ajustes preestablecidos de imagen porque restringir el acceso a /etc/dam/video/dynamicmedia deshabilita las funciones de los administradores de imágenes. NPR-28662: revisión para CQ-4263022
* El uso compartido de vínculos con archivos de vídeo codificados de DMS7 genera carpetas vacías. NPR-28851: revisión para CQ-4206743
* La replicación de AEM a Brand Portal se queda atascada durante largos períodos de tiempo. NPR-28913: revisión para CQ-4254932

### Communities {#communities-3}

* No se pueden abrir los mensajes con datos adjuntos en las carpetas de la bandeja de entrada y de enviados de Outlook. NPR-28559: revisión para CQ-4217072

### Sitios {#sites-4}

* Ejecución de scripts en sitios múltiples (XSS) en SuggestionHandler para 6.3. NPR-28692: Revisión para CQ-4253821
* El despliegue profundo finaliza sin contener todas las ramas de la LiveCopy correspondiente. NPR-29175: revisión para CQ-4239472
* (MSM) Implemente LiveCopyIndex con oak-index. NPR-29198: revisión para CQ-4222472
* El archivo “coral.js” incluye una versión vulnerable de la biblioteca “handlebars.js”. NPR-26973: revisión para CQ-4255377
* El uso de un componente Destinatario con un Contenedor de diseño y un componente de texto anidados produce un error de JavaScript &quot;No se puede leer la propiedad currentPos de null&quot; al editar texto o hacer clic en el contenedor. NPR-29077: revisión para CQ-4246594
* (IU táctil) No se pueden actualizar de forma masiva las etiquetas de las páginas que ya están etiquetadas con etiquetas diferentes. NPR-28729: revisión para CQ-4262922
* Al abrir la variación en la vista de tarjeta, se produce un error 500. NPR-28611: revisión para CQ-4263571
* El despliegue de una estructura que se ha movido en una página principal conduce a un cq:moveTarget incorrecto. NPR-28968: revisión para CQ-4265280

### Integración  {#integration}

* (Configuraciones del Cloud Service) Se debe quitar la casilla &quot;Heredada de&quot; que aparece en el nivel raíz. NPR-28771: revisión para CQ-4259676
* com.day.cq.personalization.impl.TeaserResourceEventHandler entra en un bucle infinito y provoca actualizaciones en los nodos en instancias de publicación. NPR-28561: revisión para CQ-4263096
* Error de conexión al utilizar las credenciales de Brightedge. NPR-29167: revisión para CQ-4265872
* Problema de compilación en OfferproxyTandtProvider.java debido a que falta la instrucción de importación para la clase “Resource”: falta la instrucción import: import org.apache.sling.api.resource.Resource. NPR-28772

### Comercio {#commerce}

* La opción Ordenar no funciona para los recursos de la colección Commerce. NPR-28755: revisión para CQ-4213622

### Jetty {#jetty}

* Las excepciones de fragmento en error.log para cada redirección 302 después de instalar CFP2 sobre 6.3.3. NPR-28606: Backport para CQ-4262844

### IU: bases {#ui-foundation}

* Al hacer clic en la etiqueta, se elimina el evento global mouseup y el cuadro de diálogo se bloquea en el “modo arrastrable”. NPR-28641: revisión para CUI-7294

### WCM: administrador de varios sitios (MSM){#wcm-msm}

* El lanzamiento de PushOnModify para el movimiento de PageManager se confirma varias veces desde dos sesiones, lo que provoca una condición de carrera. NPR-28880: revisión para CQ-4266191

###  Vulnerabilidad  {#vulnerability}

* El marco de protección CSRF no funciona con los formularios de base de AEM. NPR-28612: revisión para GRANITE-22231

### Forms {#forms-4}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

Los aspectos destacados de AEM Forms son:

* Opción habilitada para seleccionar elementos por página en la página de vista Conjunto de directivas.
* Se ha agregado la funcionalidad de cola de Uso compartido para todos los exploradores.

### Paquete de complemento de Forms {#forms-add-on-package-4}

#### Forms: flujo de trabajo {#forms-workflow}

* La tarea de respuesta en cola compartida abre un elemento flash en el espacio de trabajo HTML5. NPR-29161: revisión para CQ-4266498
* No se puede enviar desde Workspace si el botón contiene el carácter Umlaut. NPR-29014: revisión para CQ-4263172

#### Forms: seguridad de documentos  {#forms-document-security}

* Opción habilitada para seleccionar elementos por página en la página de vista Conjunto de directivas. NPR-29243: Revisión para CQ-4268567 y CQ-4265132

#### Forms: servicios de documentos  {#forms-document-services-1}

* El ensamblador de formularios OSGi no funciona en los archivos de Acrobat. NPR-29049: revisión para CQ-4254426

#### HTML5 Forms {#html-forms-2}

* Se experimenta un comportamiento diferente al previsualizar un XDP como PDF frente al mismo XDP como HTML en Designer. NPR-28602: revisión para CQ-4260239

### Instalador JEE de Forms  {#forms-jee-installer-3}

* No hay nuevas correcciones de AEM Forms en el instalador JEE de Forms.

### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión 6.3.3.4.  {#osgi-bundles-and-content-packages-included-in-1}

Lista de paquetes OSGi incluidos en AEM 6.3.3.4

[Obtener archivo](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

Lista de paquetes de contenido incluidos en AEM 6.3.3.4

[Obtener archivo](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Paquete de correcciones acumulativas 6.3.3.3 {#cumulative-fix-pack-5}

El paquete de correcciones acumulativas 6.3.3.3 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 3 (6.3.3.0) de AEM 6.3 en septiembre de 2018.

AEM Cumulative Fix Pack 6.3.3.3 depende de AEM 6.3 Service Pack 3. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.3.x después de instalar AEM 6.3 Service Pack 3. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 3 de AEM 6.3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Los aspectos destacados del **AEM paquete de correcciones acumulativas** son:

* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.16.
* La paginación de la lista del conjunto de directivas cambia para limitarse a 50 registros por página.
* República añadida: almacenar en caché nodos ignorables en el escucha de sincronización de usuarios de AEM Communities en instancias de publicación.
* Etiqueta aria añadida para el botón de vista de lista y tarjeta.
* Se incluyó un carácter de escape para la coma cuando se realiza una búsqueda.
* Se ha habilitado la compatibilidad de recursos sintéticos para la política de contenido.

#### Recursos {#assets-5}

* No se pueden descargar varios archivos de tipo .jp2, .max, .oft, .msg. NPR-28002: revisión para CQ-4210856
* La configuración de publicación de ImageServer no se replica en envío híbrido. NPR-28329: revisión para CQ-4253030

#### Comunidades  {#communities-4}

* Se ha habilitado la navegación mediante el teclado para los componentes de habilitación de AEM Communities en la publicación. NPR-27739: revisión para CQ-4253856
* Se ha habilitado la navegación mediante el teclado para activar la reproducción de contenido. NPR-27738: revisión para CQ-4254026
* Etiqueta aria añadida para el botón de vista de lista y tarjeta. NPR-27736: revisión para CQ-4254027
* (Puerto posterior) República Añadida: almacenar en caché nodos ignorables en el escucha de sincronización de usuarios de AEM Communities en instancias de publicación. NPR-27841: revisión para CQ-4247234
* Los caracteres especiales llevan el prefijo de carácter de escape (\) en el cuadro de búsqueda en la interfaz de usuario. NPR-27839: revisión para CQ-4259757
* Error al buscar caracteres como ( , +,? en búsqueda rápida. NPR-28212: revisión para CQ-4260969
* No se pueden eliminar comentarios en el contenido generado por el usuario mediante API. NPR-28075: revisión para CQ-4260534
* Los comentarios publicados en la página siguiente se resaltan en amarillo cuando se publica un comentario nuevo. NPR-28148: revisión para CQ-4259681
* No se pueden abrir los mensajes con datos adjuntos en las carpetas de la bandeja de entrada y de enviados de Outlook. NPR-28559: revisión para CQ-4217072

#### Sitios {#sites-5}

* La ejecución de la depuración de versiones en AEM 6.3 provoca una advertencia repetida constantemente en los registros. NPR-27750; revisión para CQ-4206870
* El complemento de estilo no se admite en el modo de pantalla completa del editor de texto enriquecido. NPR-27622: revisión para CQ-4258674
* La lista &#39;loaderPromises&#39; no se borra después de cargar el marco de contenido en editor.js NPR-27768: Revisión para CQ-4205337
* No se puede establecer la directiva de plantilla en parsys anidado sin establecer el componente principal. NPR-27987: revisión para CQ-4246095
* El navegador de componentes no está eliminando los datos introducidos por el usuario y, por lo tanto, puede generar errores de JavaScript. NPR-27986: revisión para CQ-4247590
* La página aparece en blanco cuando el usuario intenta editar el fragmento de contenido. NPR-27669
* El resaltado de la anotación desaparece cuando el usuario hace clic en la anotación. BPR-27196: revisión para CQ-4254423

#### Integración  {#integration-1}

* ResourceResolver no resuelve varios dominios para el componente de Target. NPR-28265: revisión para CQ-107847
* La cancelación de herencia de LiveCopy no funciona correctamente en los contenedores objetivo, ya que no se muestra ninguna acción. NPR-28129: revisión para CQ-4259813

#### Replicación {#replication-1}

* DispatcherFlushRules interrumpe la replicación en 6.3.3.1 NPR-28150: Revisión para CQ-4261401

#### Campaign: Segmentación  {#campaign-targeting-1}

* NullPointerException en TargetedContentManager. Revisión para CQ-4263485

#### Social: SCORM  {#social-scorm}

* Elimine la referencia a la nube del Modelo de referencia de objetos de contenido compartido (SCORM) en el reproductor. Revisión para CQ-4260779

#### DAM: General {#dam-general}

* La descarga mediante correos electrónicos de recursos compartidos a través de vínculos devuelve un archivo comprimido vacío o dañado. Revisión para CQ-4259686

#### MAC: Integración de Test&amp;Target  {#mac-test-target-integration}

* La opción Configurar componente de Target no está disponible para las audiencias, excepto para la audiencia predeterminada. Revisión para CQ-4261370

#### Traducción {#translation-1}

* Habilite la compatibilidad con el servicio MS Translator en AEM 6.3 después de actualizar MS Translator a la API v3.0. NPR-28365: Revisión para CQ-4259096

### Forms {#forms-5}

### Paquete de complemento de Forms {#forms-add-on-package-5}

#### Forms: flujo de trabajo {#forms-workflow-1}

* No se pueden procesar formularios PDF en el espacio de trabajo HTML5. NPR-28059: revisión para CQ-4260373

#### Forms: servicios de documentos  {#forms-document-services-2}

* No se puede ver ningún conjunto de directivas más allá de los primeros 1000 enumerados en la vista Conjuntos de directivas de Admin Console. NPR-28060, NPR-26047: revisión para CQ-4249865
* Se genera una excepción con el nombre java.lang.IllegalArgumentException, mensaje:Ninguna constante enum com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE que impide que se complete el proceso de corta duración. NPR-28652

#### Forms: Formularios adaptables  {#forms-adaptive-forms}

* Añadir o eliminar elementos en la lista desplegable no se actualiza al marcar los elementos de casilla de verificación. NPR-28224: revisión para CQ-4252834

### Instalador JEE de Forms  {#forms-jee-installer-4}

* No hay nuevas correcciones de AEM Forms en el instalador JEE de Forms.

### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión 6.3.3.3.  {#osgi-bundles-and-content-packages-included-in-2}

Lista de paquetes OSGi incluidos en AEM 6.3.3.3

[Obtener archivo](assets/do-not-localize/6333_bundle_list.txt)

Lista de paquetes de contenido incluidos en AEM 6.3.3.3

[Obtener archivo](assets/do-not-localize/content_package_list_6333.txt)

### Paquete de correcciones acumulativas 6.3.3.2 {#cumulative-fix-pack-6}

El paquete de correcciones acumulativas 6.3.3.2 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 3 (6.3.3.0) de AEM 6.3 en septiembre de 2018.

AEM Cumulative Fix Pack 6.3.3.2 depende de AEM 6.3 Service Pack 3. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.3.x después de instalar AEM 6.3 Service Pack 3. Para obtener instrucciones de instalación, consulte las notas de la versión del paquete de servicio 3 de AEM 6.3.

Los aspectos destacados del paquete de correcciones acumulativas de AEM son:

* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.15.
* Se agregó compatibilidad con la pestaña Reglas y su aplicación en la carpeta de recursos en el esquema de metadatos de la carpeta.
* Se habilitó la compatibilidad de paginación para agrupar la página de listado en  instancias de publicación .
* Se ha habilitado la notificación unreadCount para que se configure con cualquier número. Valor predeterminado establecido en 20.
* Correcciones en el Comprobador de vínculos externos.

#### Recursos {#assets-6}

* La lista desplegable en cascada no es compatible con las listas desplegables dinámicas. NPR-27044; revisión para CQ-4252564
* Mejore la consulta para utilizar la función ExpiryNotification. NPR-26999: revisión para CQ-4251188
* Migración de reglas del esquema de metadatos al esquema de metadatos de la carpeta. NPR-27771: Backport para CQ-4257737, CQ-4257735, CQ-4259822
* El ajuste de referencia de recursos no puede actualizar las referencias de recursos que forman parte de Sling ResourceCollections. NPR-26759: revisión para CQ-4252605
* La descarga mediante el correo electrónico del recurso compartido de vínculos devuelve un archivo comprimido vacío o dañado. NPR-27997: revisión para CQ-4259686
* La codificación de vídeo híbrido no se completa y no se crea ninguna miniatura. NPR-27122: revisión para CQ-4255080

#### Sitios {#sites-6}

* La suspensión de la página principal elimina cq: Tipo de mezcla LiveRelationship de la página que falta. NPR-26996: revisión para CQ-4254113
* (Comprobador de vínculos externos) Los vínculos internos se muestran como rotos en páginas individuales, pero lo mismo no funciona para los vínculos externos. NPR-27481: revisión para CQ-4257780
* La herencia de la configuración de Cloud Service se interrumpe al editar otras propiedades de página. NPR-27311: revisión para CQ-4256785
* Excepción de puntero nulo al usar componentes principales  junto con un formulario base. NPR-27333: revisión para CQ-4249176
* El Editor de texto enriquecido elimina la etiqueta alt vacía. NPR-26938: revisión para CQ-4253267
* (IU clásica) Problemas de rendimiento con   selectionchanged   oyente en caso de que haya varias listas desplegables. NPR-27115: revisión para CQ-4237215
* Cuando el editor de texto enriquecido se combina con varios campos, se produce el error Uncaught TypeError: fieldAPI.getName is not a function at foundation.js. NPR-27146: revisión para CQ-4253155, CQ-4259967
* Enfoque/Cursor permanece en el Editor de texto enriquecido incluso cuando se hace clic en un botón de opción en el explorador Safari. NPR-27144: revisión para CQ-4249635
* La página aparece en blanco cuando el usuario intenta editar el fragmento de contenido. NPR-27669
* No se puede crear una versión para los fragmentos de experiencia. NPR-27689: revisión para CQ-4259009

#### Integración  {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever recorre todo el árbol para recopilar las marcas disponibles. NPR-27060: revisión para CQ-4255790
* El   cq : no se consideran acciones para un componente de destino. NPR-27616: revisión para CQ-4257497

#### Sling  {#sling}

* Cuando se utiliza el uso de datos de forma remota con clases con un nombre idéntico, se genera el código no compatible. NPR-27282: Revisión para Sling-7581

#### Comercio {#commerce-1}

* Actualización a Apache Felix Http Jetty 4.0.6. NPR-26472: Revisión de Granite-22916

#### DAM: Cliente DM  {#dam-dm-client}

* Una imagen no se muestra después de especificar puntos de interrupción en el componente de medios dinámicos. Revisión para CQ-4256168

#### DAM: DMServices  {#dam-dmservices}

* MixedMediaSet con vídeo relacionado no se sincroniza correctamente. Revisión para CQ-4251650
* El vídeo no se reproduce en el editor de ajustes preestablecidos de visor para conjuntos de medios mixtos. Revisión para CQ-4251442

#### DAM: General  {#dam-general-1}

* Falta el vínculo al modelo de fragmento de contenido después de aplicar el parche SP3. Revisión para CQ-4259029

#### DAM: IU  {#dam-ui}

* La interfaz de usuario del esquema de metadatos de la carpeta se corrompe tras instalar SP3. Revisión para CQ-4257737

#### Comunidades  {#communities-5}

* Al publicar, se agrega la compatibilidad con la paginación para la lista de grupos. NPR-26953: revisión para CQ-4246525
* La notificación de recuento sin leer no se puede establecer más allá de 21. NPR-27496: revisión para CQ-4252829
* El límite de suscripción de usuarios está establecido en 1000. NPR-27615: revisión para CQ-4254689
* Se ha observado un error al cargar un archivo adjunto que no sea una imagen (por ejemplo, .pdf) en el foro. NPR-27375: revisión para CQ-4257753
* El vínculo para respuestas no funciona al hacer clic en la fila. NPR-24556: revisión para CQ-4256138
* Las relaciones con UGC no se eliminan al eliminar UGC. NPR-27631: revisión para CQ-4258706
* No se puede buscar por valor de dirección en la búsqueda de palabras clave si la comunidad está configurada con el proveedor de recursos de almacenamiento de datos (DSRP). NPR-27652: revisión para CQ-4253261
* Al hacer clic en el icono de papelera de la imagen después de la confirmación de eliminación, se elimina el adjunto de forma permanente. NPR-27340: revisión para CQ-4255150
* Las publicaciones y las respuestas del foro se agregan al principio de la segunda página y, cuando se actualizan, la publicación se mueve a la ubicación correcta en la parte superior de la primera página. NPR-27341: revisión para CQ-4247338
* La etiqueta de estado de finalización de recursos de Puntuación de habilitación aparece vacía en la interfaz de usuario. NPR-27152: revisión para CQ-4249994
* Al habilitar “Permitir privilegiados”, los miembros privilegiados solo pueden componer para usuarios que son miembros de la comunidad. NPR-27901: revisión para CQ-4251235

#### Soporte  {#sustenance}

* Los registros de actividades del administrador de paquetes deben extraerse en un archivo de registro independiente. NPR-27323: Revisión para Granite-14866

#### Traducción  {#translation-2}

* La previsualización de traducción no funciona con el contenido de muestra we.retail. NPR-27170: revisión para CQ-4241179

* Correcciones proactivas de platform.login. NPR-26961
* Guardar y cerrar en las propiedades de la página no vuelve a la  página adecuada en AEM GUERRA con Tomcat. NPR-27567: Revisión para Granite-23671

* El texto introducido se pierde a través de la función sourceEdit una vez guardado. Revisión para CQ-4259273

### Forms {#forms-6}

### Paquete de complemento de Forms {#forms-add-on-package-6}

#### Forms: seguridad de documentos {#forms-document-security-1}

* Problema de concurrencia con el SDK del cliente de JEE. NPR-27572: revisión para CQ-4247156

#### Forms: servicios de documentos  {#forms-document-services-3}

* La creación de un modelo de datos de formulario basado en SOAP falla en WebSphere. NPR-27692: revisión para CQ-4253702

#### Forms: formularios adaptables  {#forms-adaptive-forms-1}

* Vulnerabilidad de la inyección de XML con AEM Forms. NPR-27863: revisión para CQ-4257315
* El componente Contenedor de AEM Forms se vuelve invisible cuando se configura el formulario incorrecto en la página Sitios y se selecciona la casilla de verificación “Los formularios cubren todo el ancho de la página”. NPR-25972: revisión para CQ-4239287, CQ-4249133

### Instalador JEE de Forms  {#forms-jee-installer-5}

#### Base JEE {#foundation-jee-1}

* La creación de un modelo de datos de formulario basado en SOAP falla en WebSphere. NPR-27692: revisión para CQ-4253702

#### Paquetes de contenido y paquetes OSGI incluidos  {#osgi-bundles-and-content-packages-included}

Lista de paquetes OSGi incluidos en AEM 6.3.3.2

[Obtener archivo](assets/do-not-localize/63332bundle_list.txt)

Lista de paquetes de contenido incluidos en AEM 6.3.3.2

[Obtener archivo](assets/do-not-localize/6332content_package.txt)

### Paquete de correcciones acumulativas 6.3.3.1 {#cumulative-fix-pack-7}

El paquete de correcciones acumulativas 6.3.3.1 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 3 (6.3.3.0) de AEM 6.3 en septiembre de 2018.

AEM Cumulative Fix Pack 6.3.3.1 depende de AEM 6.3 Service Pack 3. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.3.x después de instalar AEM 6.3 Service Pack 3. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 3 de AEM 6.3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Los aspectos destacados del **AEM paquete de correcciones acumulativas** son:

* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.14.
* Mejoras de rendimiento en predicados y búsquedas.
* Se corrigió un problema en el manejo de FormData para el valor predeterminado.
* Se ha actualizado FormBuilder a la versión más reciente de Handlebars.
* Se ha agregado el servlet de configuración para la configuración de edición de RTE en modo de cuadro de diálogo.
* Se agregó compatibilidad con campos compuestos.
* Elementos de la barra de herramientas habilitados o deshabilitados del Editor de texto enriquecido con una directiva de contenido para el cuadro de diálogo de edición.

#### Recursos {#assets-7}

* Con la desvinculación de IDS activada, el flujo de trabajo de recursos de actualización de DAM ya no vincula las referencias. NPR-26135: revisión para CQ-4250933
* No se abre la función de descomprimir un archivo creado por el paso del desarchivador con una carpeta con un % en su nombre. NPR-26275: revisión para CQ-4251482
* El carácter de comilla única evita la actualización de los metadatos. NPR-26808: revisión para CQ-4254305
* (Omnisearch) Problema de rendimiento al buscar dentro de una colección. NPR-26714: revisión para CQ-4253408
* El uso de GQLConverter con una búsqueda de texto completo que contiene la condición “OR” dentro del texto se procesa incorrectamente. NPR-26564: revisión para CQ-4247362
* El uso compartido de vínculos de recursos desde varios inquilinos antepone el ID de inquilino que forma una dirección URL no válida. NPR-26482: revisión para CQ-4253540
* Deshabilite &quot;Ruta de la carpeta raíz de la Compañía&quot; en la interfaz de usuario de configuración de Dynamic Media Cloud. NPR-26361: revisión para CQ-4249505
* Se prolonga la ingestión de archivos .mos RAW. NPR-26296: revisión para CQ-4250661
* El uso compartido de vínculos de recursos no permite agregar más de un usuario interno con un identificador de usuario numérico. NPR-26206: revisión para CQ-4251466
* Corrupción en archivos zip comprimidos con el algoritmo deflate64. NPR-26793: revisión para CQ-4253995
* El proceso de generación de miniaturas no funciona correctamente para archivos PDF complejos, lo que provoca la aparición de miniaturas en las que falta parte de la imagen. NPR-26057: revisión para CQ-4250944
* Problema de utilización de memoria de acumulación con la generación de miniaturas. NPR-25545: revisión para CQ-4246960
* La creación de un gran número de relaciones en un recurso provoca errores. NPR-26309: revisión para CQ-4250708
* La opción “Eliminar representación” no funciona y genera un error “nada que eliminar”. NPR-26007: revisión para CQ-4213414
* No se pueden eliminar los valores predeterminados de los campos multivalor. NPR-25116: revisión para CQ-4247856
* (DM Hybrid) La replicación de catálogos se interrumpe para AEM 6.3.2 con Dynamic Media. NPR-26406: revisión para CQ-4251306

#### Sitios {#sites-7}

* Correcciones proactivas del backport. NPR-26963
* Las etiquetas se crean dos veces cuando hay una diferencia en el tipo de caso Título y Nombre. NPR-26877: revisión para CQ-4254134
* Las funciones del editor de texto enriquecido del cuadro de diálogo de edición no están controladas por políticas. NPR-27059, NPR-26750: revisión para CQ-4241130
* Preguntas de almacenamiento en caché de ClientContext segment.js frente a preguntas que no están almacenadas en caché. NPR-26622: revisión para CQ-4253486
* La activación de la regla de segmentos (/etc/segmentation) para reglas secundarias en causas clásicas hace que la publicación se desactive. NPR-26601: revisión para CQ-4253588
* Al agregar un carácter especial, se desplaza al principio el cuadro de diálogo Editor de texto enriquecido. NPR-26435: revisión para CQ-4249869
* La barra de herramientas (IU táctil) no se puede utilizar con varios Editor de texto enriquecido al cambiar del cuadro de diálogo de pantalla completa a flotante. NPR-25652: revisión para CQ-4206008
* Al promocionar un lanzamiento de varias páginas, se crean varias versiones de cada página. NPR-26810: revisión para CQ-4254663
* Las operaciones de movimiento de etiquetas no se reflejan en  campos de etiqueta del modelo de fragmento de contenido estructurado. NPR-26801: revisión para CQ-4251805
* (IU táctil) La cancelación de la publicación de la página secundaria desde el editor de páginas no funciona después de cambiar el nombre de la página en el modelo. NPR-26774: revisión para CQ-4254175
* Una página sin publicar  no funciona con referencias. NPR-26749: revisión para CQ-4254372
* La creación de variaciones como Live Copy requiere que el usuario actualice la página para que se refleje. NPR-26663: revisión para CQ-4254328
* (IU clásica) Al volver a las propiedades de la página, la imagen en miniatura ya no utiliza la herencia y desaparece de la administración del sitio y de la barra de tareas, y la imagen se muestra en blanco. NPR-26562: revisión para CQ-4252346
* Cuando se crea una versión de una página y se activa una comparación, los nodos de /content/ versionshistory se enumeran en la lista de copias activas para el modelo. NPR-26506: revisión para CQ-4243957
* Las direcciones URL del Editor de administración de fragmentos de experiencia no permiten superposiciones. NPR-26318: revisión para CQ-4252156

#### Plataforma {#platform}

* Filtrado de sesiones en ReplicationEventListener con eventos de prueba. NPR-25937: revisión para CQ-4251090
* La replicación utiliza el token caducado para OAuth, lo que provoca varios errores. NPR-25894: revisión para GRANITE-22388

#### Integración  {#integration-3}

* El TSDK incrustado con AEM rompe con una actualización a Handlebars 4 debido al uso de plantillas incompatibles. NPR-26699: revisión para CQ-4248974
* Publicar una página con un nuevo recurso, desactiva la página secundaria de la instancia de publicación sin previo aviso. NPR-24869: revisión para CQ-4247832
* La replicación utiliza un token caducado para  oauth . NPR-25984: Revisión para Granite-22388

#### Replicación {#replication-2}

* El transporte HTTP puede provocar fugas en las sesiones abiertas. Revisión para Granite-17434
* Hay más de un agente de replicación que accede de manera simultánea a las excepciones en los registros mientras se accede al nodo del token de acceso. NPR-26964: Revisión para GRANITE-23276, Granite-23155

#### ContextHub {#contexthub}

* El archivo “coral.js” incluye una versión vulnerable de la biblioteca “handlebars.js”. Revisión para CQ-4255377

#### DAM: Cliente DM  {#dam-dm-client-1}

* Al eliminar una copia de un recurso de imagen, el recurso de imagen original queda inutilizable. Revisión para CQ-4251648
* Descarga redundante de contenido de imagen adicional de los servidores S7. Revisión para CQ-4248770

#### Granite  {#granite}

* El proveedor de AEM OAuth no realiza la búsqueda sin distinguir entre mayúsculas y minúsculas. NPR-26133: revisión para GRANITE-22650
* El validador del paquete no valida los paquetes incluidos en CFP/SP. NPR-26775: Revisión para Granite-22825

#### Comunidades  {#communities-6}

* Problema del delimitador con los resultados de búsqueda. NPR-27051: revisión para CQ-4248939
* Cambiar el valor desplegable de Dallas a Virginia en el proveedor de recursos de almacenamiento de Adobe. NPR-26936: revisión para CQ-4254434
* Habilite la compatibilidad para la búsqueda de títulos localizados en SocialTagManager. NPR-26932: revisión para CQ-4250276
* Al crear una publicación de foro, las imágenes de datos adjuntos no muestran miniaturas. NPR-26380: revisión para CQ-4253105
* Pegar desde el complemento de Word no permite cargar más de una imagen. NPR-26728: revisión para CQ-4253638
* No se puede filtrar el contenido en la página de moderación. NPR-26697: revisión para CQ-4213766
* (Vulnerabilidad de seguridad) Toma de cuentas debido a una configuración incorrecta de JWT. NPR-26440: revisión para CQ-4253314
* La recuperación de datos del proveedor de recursos de almacenamiento de Adobe es lenta. NPR-26237: revisión para NPR-24152
* La página de composición de mensajes privados se comporta de forma errática y lenta. NPR-26120: revisión para CQ-4250923
* La notificación “Marcar todo como leído” procesa solo los 10 primeros como no leídos sin actualizar la página. NPR-27036: revisión para CQ-4254058
* Comportamiento al hacer clic en la paginación de secciones de comentarios de Communities y comportamiento de carga de página NPR-27030: revisión para CQ-4251228
* (Búsqueda de foro) El botón Atrás omite la página y vuelve a forum.html. NPR-26949: revisión para CQ-4254804
* La notificación sin leer no aumenta más de 21. NPR-26947: revisión para CQ-4251251
* (Trabajo de SearchScheduledPosts) Añada el conmutador habilitar/deshabilitar en ConfigMgr. NPR-26924: revisión para CQ-4250463
* La ruta de contexto (/aempublish) de Tomcat se despliega al desplazarse por la página Asignaciones. NPR-26919: revisión para CQ-4254345
* NullPointerException al crear un grupo y un miembro. NPR-26778: revisión para CQ-4248095
* El contenido sin asignar y sin fijar del moderador no funciona con el Principio de responsabilidad única (SRP) de MySQL. NPR-26767: revisión para CQ-4251520
* Problemas de funcionalidad de búsqueda con determinados caracteres. NPR-26726: revisión para CQ-4247744
* Habilite los vínculos profundos para la interfaz de usuario de moderación y los recursos de habilitación. NPR-26705: revisión para CQ-4251381
* Problema de búsqueda en el componente del foro. NPR-26577: revisión para CQ-4251303
* La búsqueda conjunta del nombre y los apellidos en los mensajes de comunidades no devuelve los resultados esperados. NPR-26377: revisión para CQ-4253150
* La paginación no se actualiza al eliminar las respuestas. NPR-26327
* La eliminación de la publicación funciona, pero da un error en la consola y la publicación permanece visible en la interfaz de usuario. NPR-26292: revisión para CQ-4252803
* La paginación no se actualiza de forma dinámica y la lista de respuestas continúa aumentando. NPR-26145: revisión para CQ-4251586
* La configuración de grupo no se carga en un grupo que contiene entre 50 000 y 100 000 usuarios. NPR-25642: revisión para CQ-4238426
* Error del Reproductor de recursos del catálogo en las rutas de contexto. NPR-25640: revisión para CQ-4238426
* (Búsqueda de foro): los vínculos paginados a subprocesos con muchos anuncios no funcionan en las notificaciones. Revisión para CQ-4254202
* La consola de moderación solo muestra 5 entradas con Firefox. Revisión para CQ-4254128
* Los grupos no están visibles al crear un sitio. NPR-27148: revisión para CQ-4251788
* Excepción de puntero nulo al agregar grupos y miembros a la configuración de rol y al permitir que el miembro privilegiado se encuentre en la función de blog. NPR-21732, NPR-27176: revisión para CQ-4255909
* La edición del sitio y la adición de miembros en la configuración de funciones genera una excepción de puntero nulo. NPR-27132: revisión para CQ-4255909

#### Interfaz de usuario {#user-interface}

* Correcciones proactivas de inicio de sesión en la plataforma. NPR-26961
* (Varios campos) Permite que los elementos compuestos tengan nombres personalizados. NPR-26493: Revisión para Granite-20568
* La vista de columna no se actualiza después de pegar una página hasta que se actualiza. NPR-26030: revisión para CQ-4236346
* Correcciones proactivas de granite.ui.commons. NPR-26960
* granite.ui.coón proactiva. NPR-26959
* Correcciones proactivas del registro de CQ/experience. NPR-26943
* Backports de la interfaz de usuario de la base proactiva. NPR-26942
* (IE11) &quot;NaN&quot; se muestra en el campo de número al escribir un valor negativo. NPR-26701: revisión para CQ-100826
* (Coral. Varios campos) Los campos múltiples anidados utilizan la plantilla incorrecta para crear los elementos. NPR-25649: revisión para CUI-6743
* Actualice los clientlibs de granito coralui2 y coralui3 para quitar Handlebars de la compilación. NPR-25606: Revisión para Granite-22116

### Forms {#forms-7}

### Paquete de complemento de Forms {#forms-add-on-package-7}

#### Forms: seguridad de documentos {#forms-document-security-2}

* Excepciones de sustitución de clave principal en los registros del servidor para las claves en activo. NPR-26748: revisión para CQ-4253705
* No se puede crear ni modificar la configuración de marca de agua de la seguridad del documento. NPR-26267, NPR-26129: revisión para CQ-4250234

#### Forms: servicios de documentos  {#forms-document-services-4}

* La validación de PDF/A no muestra validez con “Validar PDF/A. NPR-25934: Revisión para CQ-4248558

#### Forms: comunicación interactiva  {#forms-interactive-communication}

* La vista previa en PDF y HTML de la carta es visible y funciona en la misma ventana cuando se edita, guarda y, a continuación, se abre/cierra una vista previa en PDF. NPR-26770: revisión para CQ-4253217

#### Forms: flujo de trabajo {#forms-workflow-2}

* El espacio de trabajo se bloquea de forma intermitente y muestra los puntos de inicio repetidamente. NPR-26461: revisión para CQ-4253439
* La excepción ESAPI se genera en los registros cuando se utilizan llaves en el nombre de la tarea. Revisión para CQ-4256627
* Se genera una excepción de puntero nulo cuando se abre un punto de inicio asociado de formulario o conjunto de formularios adaptable no rellenado previamente. Revisión para CQ-4256124
* No se puede enviar un correo electrónico con la configuración global. NPR-26163: revisión para CQ-111110
* No se puede abrir el espacio de trabajo después de aplicar el archivo axis.jar. NPR-26131: revisión para CQ-4251126
* El botón de actualización no puede sincronizar los datos más recientes del servidor con los formularios adaptables. Revisión para CQ-4255670
* La configuración de la plantilla de búsqueda desde la interfaz de usuario de administración y el uso del mismo para buscar la tarea en el espacio de trabajo de AEM Forms genera una excepción. Revisión para CQ-4255649
* Los detalles de seguimiento de los procesos en las aplicaciones con el símbolo entre paréntesis en el nombre no se muestran en el espacio de trabajo HTML. Revisión para CQ-4242101
* Al guardar los cambios en la pantalla de preferencias del espacio de trabajo HTML, se genera una excepción. Revisión para CQ-4241485
* La aprobación masiva se ha interrumpido en la última configuración de JEE. Revisión para CQ-4241486
* El borrador de la tarea/punto de inicio está fallando en el servidor 6.4 JEE más reciente. Revisión para CQ-4241484
* Establezca el parámetro Date().getTime().toString para inicializar la sesión en lugar de Date.toString(). Revisión para CQ-4241483
* Al abrir /lc/ws, se observa una excepción de caracteres vulnerable en el parámetro HTML. Revisión para CQ-4241481

####  Vulnerabilidad{#vulnerability-1}

* Vulnerabilidad de la ejecución almacenada de scripts en sitios múltiples (XSS) en la ficha Notas del administrador de Forms. NPR-27157: revisión para CQ-4255556

### Instalador JEE de Forms {#forms-jee-installer-6}

#### Base JEE {#foundation-jee-2}

* Revisión de código para la API de seguridad de Entreprise. Revisión para CQ-4255638
* No se pudo cargar esapi.properties como recurso del cargador de clases en WAS9. Revisión para CQ-4255631
* Al hacer clic en Agregar autenticación durante la configuración del dominio se genera un error. Revisión para CQ-4255634
* Forms JEE admite autenticación mutua PKCS#11. NPR-21372
* Se han corregido los problemas notificados en el análisis de código estático de Core. Revisión para CQ-104446
* La implementación de adobe.livecycle.weblogic.ear y adobe.livecycle.websphere.ear está fallando mientras se ejecuta LCM. Revisión para CQ-4255629, CQ-4255630
* Mensajes de error no válidos en Application Management. NPR-23289: revisión para CQ-4233163, CQ-4255636
* Al hacer clic en Agregar autenticación durante la configuración del dominio, se produce un error. Revisión para CQ-4255634

#### Forms: conector JEE {#forms-jee-connector}

* Se han corregido los problemas notificados en el análisis de código estático de Core. NPR-22260

#### Servicio PDFG  {#pdfg-service-1}

* org.jgroups.Message error en los registros después de actualizar de LiveCycle a formularios AEM 6.2. NPR-26795: revisión para CQ-4220415
* AEM Forms: error al migrar estilos. Revisión para CQ-4251969
* Se corrigieron los problemas notificados en el informe de análisis de código estático de PDFG. NPR-23251: revisión para CQ-4213930

#### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión 6.3.3.1.  {#osgi-bundles-and-content-packages-included-in-3}

Lista de paquetes OSGi incluidos en AEM 6.3.3.1

[Obtener archivo](assets/do-not-localize/63sp3cfp1bundlelist.txt)

Lista de paquetes de contenido incluidos en AEM 6.3.3.1

### Paquete de correcciones acumulativas 6.3.2.2  {#cumulative-fix-pack-8}

El paquete de correcciones acumulativas 6.3.2.2 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 2 (6.3.2.0) de AEM 6.3 en abril de 2018.

AEM Cumulative Fix Pack 6.3.2.2 depende de AEM 6.3 Service Pack 2. Por lo tanto, debe instalar el paquete AEM Cumulative Fix Pack 6.3.2.x después de instalar AEM 6.3 Service Pack 2. Para obtener instrucciones de instalación, consulte [las notas de la versión del paquete de servicio 2 de AEM 6.3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html).

Los aspectos destacados del **AEM paquete de correcciones acumulativas** son:

* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.11.
* Se han habilitado subrecursos y una vista de recursos de varias páginas en Brand Portal.
* Se ha cambiado la longitud del tipo de campo a 255 para admitir todos los tipos de MIME posibles para los diferentes tipos de datos adjuntos.
* Mensaje de error configurado del servidor cuando una imagen infringe los criterios de carga.
* Se ha añadido la compatibilidad con STARTTLS en el servicio de correo de Day CQ.
* Actualice a las versiones más recientes de cq-wcm-content y com.adobe.cq.launches.it.serverside.
* Actualice com.adobe.granite.ui.coralui3-rte a la versión más reciente publicada.
* La condición de procesamiento asegurada devuelve un resultado simulado si expresiónResolver es nulo.
* Coral.ColumnView: compatibilidad añadida con Mayús+clic.

### Recursos {#assets-8}

* El campo del grupo cerrado de usuarios de carpetas de recursos (CUG) no devuelve el grupo “todos”. NPR-23163: revisión para CQ-4239377
* Al buscar búsquedas guardadas de colecciones inteligentes no aparecen todos los resultados. NPR-23243: revisión para CQ-4240355
* (ExpiryNotificationJobImpl) Optimización de la consulta existente. NPR-23330: revisión para CQ-4205249
* (perfil de metadatos) Los valores de etiqueta estándar establecidos en el momento de la creación no están disponibles tras guardar. NPR-23370: revisión para CQ-4235458
* (IU táctil) No se pueden mover varios recursos debido a un error de JS. NPR-23395: revisión para CQ-4241279
* La falta de coincidencia en el tamaño de descarga con respecto a la información mostrada es incorrecta, lo que provoca confusión entre los usuarios. NPR-23418: revisión para CQ-4242774
* El mimetype extraído para la extensión de archivo LSR y SKETCH es incorrecto y dirige a una descarga de archivo no válida. NPR-23644: revisión para CQ-4243260
* (Firefox/Chrome) No se pueden descargar recursos en la página Uso compartido de recursos. NPR-23963: revisión para CQ-4244391
* Las facetas de búsqueda del administrador de recursos desaparecen en los paneles de búsqueda después de obtener la vista previa. NPR-23964: revisión para CQ-4244410
* La cancelación de la publicación del formulario de búsqueda elimina completamente el formulario de búsqueda predeterminado. NPR-23291: revisión para CQ-4241382
* (Brand Portal) La búsqueda en el predicado de directorios debe filtrarse en la replicación. NPR-23292: revisión para CQ-4241385
* La acción Publicar en la interfaz de usuario de Brand Portal no está disponible. NPR-23293: revisión para CQ-4241161
* El botón Publicar/Cancelar la publicación en Brand Portal no debe estar disponible para los fragmentos de contenido. NPR-23318: revisión para CQ-4245086
* (Brand Portal) Active la creación de subrecursos cuando se publique un recurso. NPR-23331: revisión para CQ-4242018
* Las solicitudes de Dynamic Media no usan un cliente común proxy/HTTP. NPR-10727: revisión para CQ-45695, CQ-88800
* No se puede anotar un recurso de vídeo MP4 de representación única en Dynamic Media S7 (DMS7). NPR-22046: revisión para CQ-4215912
* Los datos EmbedXMP siempre se definen como “activos” para el proceso de generación de Ptiff. NPR-22903: revisión para CQ-4234498
* Problemas de visualización y selección de representaciones dinámicas con un gran número de ajustes preestablecidos de imagen. NPR-23151: revisión para CQ-4217511
* Problema con el iniciador de codificación de vídeo de Dynamic Media: publicador de modificación/recarga. NPR-23237: revisión para CQ-4240260
* Corrección de la administración de proxy para el reenviador HTTP en Dynamic Media S7. NPR-24001: revisión para CQ-244140

### Sitios {#sites-8}

* Las discrepancias del generador de consultas que resultan en una traducción de xPath diferente entre 6.2 y 6.3. NPR-23245: Revisión para CQ-4240396
* La ficha Miniaturas de la propiedad de página no funciona para ampliar el cuadro de diálogo. NPR-22844: revisión para CQ-4241474
* Parsys rompe la anchura del marco del dispositivo emulador y recorta cualquier componente que se le agregue. NPR-22926: revisión para CQ-4238224
* Al ejecutar varios lanzamientos, el inicio se promociona en Author, pero los cambios no se replican en el servidor de publicación debido a la falta de permisos de replicación. NPR-22934: revisión para CQ-4234746
* Una página bloqueada por un usuario en la primera sesión puede ser modificada por otro usuario en otra sesión. NPR-23057; revisión para CQ-4199017
* Corregir la opción reordenable en la vista de lista. NPR-23065: revisión para CQ-4239321
* (Editor de páginas) La imagen de un componente de imagen desaparece al abrir de nuevo el cuadro de diálogo. NPR-23156: revisión para CQ-4239978
* El Editor de plantillas solo muestra 20 plantillas/carpetas y no carga las otras al desplazarse a la parte inferior de la página. NPR-23185: revisión para CQ-4238483
* (IU clásica) Se genera un error al mover o cambiar el nombre de las páginas. NPR-23213: revisión para CQ-4240971
* No se pueden editar ni crear segmentos de ContextHub. NPR-23218: revisión para CQ-4226948
* (Editor de texto enriquecido): la operación de reemplazo cambia el formato de una palabra. NPR-23271: revisión para CQ-4239677
* Falta el botón de despliegue en la pestaña de modelo para las variaciones XF. NPR-23320: revisión para CQ-4240404
* La IU clásica no funciona para editar CUG ya que ha quedado obsoleta. NPR-24122: Revisión para CQ4241823
* Corrección proactiva para protegerse de las promociones de contenido no deseado. NPR-24387: Revisión para CQ4244993
* Una vez añadidos aproximadamente 80 fragmentos en una carpeta en Assets, se producen errores al activar el flujo de trabajo desde la consola la cronología. NPR-23393; revisión para CQ-4211216
* No se pueden arrastrar y soltar imágenes en el cuadro de diálogo del Editor de texto enriquecido desde el buscador de contenido. NPR-23403: revisión para CQ-4242094
* Error &#39;Valor del selector de recursión no válido&#39; al migrar un componente de AEM 6.0 a AEM 6.2. NPR-23532: Revisión para CQ-4241258
* (Editor de texto enriquecido) La información sobre herramientas muestra el nombre variable del complemento en lugar del nombre legible del complemento. NPR-23550: revisión para CQ-4243269
* No se puede guardar el cuadro de diálogo con la lista desplegable de selección necesaria en la versión móvil o para tabletas. NPR-23904: revisión para CQ-4243096
* Las opciones del sistema de estilo aparecen en todas las páginas posteriores a la instalación de la versión 6.3.2.1. NPR-23972: revisión para CQ-4244394
* La IU clásica no funciona para editar CUG ya que ha quedado obsoleta. NPR-24122: Revisión para CQ4241823
* Corrección proactiva para protegerse de las promociones de contenido no deseado. NPR-24387: Revisión para CQ4244993
* Las referencias de recursos no se actualizan cuando se mueven recursos. NPR-23208: revisión para CQ-4239879

### Plataforma  {#platform-1}

* La colección inteligente no muestra los resultados después de guardarlos si se utilizan etiquetas predicadas en la faceta de búsqueda. NPR-23401: Revisión para Granite-21278
* Parche jQuery 1.12.4 de clientlib para incluir una corrección de seguridad. NPR-24128: Revisión para Granite-20058
* Las traducciones de internacionalización no se actualizan a menos que se reinicie el paquete. NPR-23193: Revisión para Sling-7190
* Resolución de recursos sin cerrar en ReplicationEventListener. NPR-23240: revisión para CQ-4241350
* Compatibilidad de STARTTLS en “Day CQ Mail Service”. NPR-23941: revisión para CQ-4240397
* El nombre de la etiqueta de queja JCR debe rellenarse automáticamente según el título de la etiqueta. NPR-24173: revisión para CQ-4199411

### Integración  {#integration-4}

* (Destinatario) Las Campañas no se activan cuando se utiliza el tipo de API como XML. NPR-23199: revisión para CQ-4240936****
* La replicación de referencia de configuración falla con la estructura de carpetas intermedias. NPR-23485: revisión para CQ-4242751

###  Vulnerabilidad  {#vulnerability-2}

* La integración de Salesforce es vulnerable a la falsificación de solicitudes del lado del servidor (SSRF). NPR-24289: revisión para CQ-424527
* Ejecución de scripts en sitios múltiples (XSS) en vínculos de proyectos de la interfaz de usuario de administración. NPR-23272: revisión para CQ-4241795

### WCM: componentes base  {#wcm-foundation-components}

* La tabla de base es vulnerable a la ejecución almacenada de scripts en sitios múltiples. NPR-23214: revisión para CQ-4240760

### Traducción  {#translation-3}

* No se eliminaron las propiedades de la Copia activa al crear copias de idioma. NPR-23123: revisión para CQ-4230641

### Interfaz de usuario {#user-interface-1}

* DatePicker no admite la configuración manual de sugerencias de tipo externas establecidas por campo oculto. Si se cambia la sugerencia de tipo se obtiene un error de conversión. NPR-23371: Revisión para Granite-21194
* Coral.ColumnView: Agrega compatibilidad con Mayús+clic. NPR-23404: Revisión para Granite-13338
* Seleccionar RT no valida cuando se selecciona un elemento con valor vacío. NPR-23405: Revisión para Granite-21283
* (OMEGA) Informe &quot;Función&quot; solo en inglés. NPR-23990: Revisión para Granite-21231
* Correcciones en la API de Coral.Autocomplete. NPR-23516

### Granito  {#granite-1}

* Las conexiones de seguimiento del cliente Apache Http y la alta utilización de acumulación hacen que el servidor de AEM se bloquee. NPR-23906: Revisión para Granite-21056

### Comercio {#commerce-2}

* La salida de json de Campaign no contiene la raíz de contexto del servlet. NPR-23733: revisión para CQ-4243827

### Comunidades  {#communities-7}

* La búsqueda en las comunidades está fallando por el reducido número de palabras. NPR-23256: revisión para CQ-4240717
* No se pueden asignar grupos para el problema de función de los administradores de la comunidad. NPR-23317: revisión para CQ-4241233: CQ-4221399
* Problemas en la creación de recursos con nombres de recursos similares. NPR-23319: revisión para CQ-4240700
* (ContextPath) Al romper la funcionalidad de mensajes, se producen errores y errores en las configuraciones de Jetty al buscar miembros del grupo en la lista de miembros del grupo de la comunidad. NPR-23336: revisión para CQ-4241519, CQ-4242080
* La carga de una imagen en un foro de Communities no aparece en el proveedor de recursos de almacenamiento de Adobe (ASRP). NPR-23397: revisión para CQ-4242497
* Las ideas eliminadas se muestran como vínculos activos en Actividades. NPR-23406
* imsmanifest.xml no se puede cargar con AEM al ejecutarse con la raíz de contexto. NPR-23483: revisión para CQ-4242193
* Vulnerabilidades de seguridad en una versión anterior de Handlebars. NPR-23518: revisión para CQ-4243055
* El servicio de túnel no funciona. NPR-23543: revisión para CQ-4242217
* Problemas con los componentes de Communities cuando se accede a ellos con Dispatcher y Sling Dynamic Include activados. NPR-23586: revisión para CQ-4242360, CQ-4241522
* Si se busca un término de búsqueda que produzca muchos resultados y, después, se introduce un nuevo término de búsqueda, la página no se restablece. NPR-23739: revisión para CQ-4222593
* Problemas durante la ejecución de la  buscar en el componente de foro. NPR-23838: revisión para CQ-4243770
* (Indicador de moderación de comunidades) La opción de permitir los mensajes marcados no funciona. NPR-23845: revisión para CQ-4243962
* El texto del botón Ordenar no muestra el valor predeterminado  inspección de valor   de selección del orden predeterminado. NPR-23881: revisión para CQ-4243375
* Las notificaciones por correo y web no se activan debido a un error en los mensajes de los grupos. NPR-23934: revisión para CQ-4242880
* No se muestran detalles sobre los usuarios del indicador ni motivos mediante la configuración de DSRP. NPR-23973: revisión para CQ-4243205
* Los motivos de marca de los usuarios que no están marcados permanecen visibles/ NPR-23974: Revisión para CQ-4243822
* Si se adjuntan dos archivos con el mismo nombre dos veces a la publicación de un formulario, se producirá un error de servidor. NPR-24166: revisión para CQ-4244367
* No se pueden almacenar datos adjuntos con tipos MIME superiores a 15 caracteres mediante el desarrollador de recursos de almacenamiento de la base de datos (DSRP). NPR-24174
* Cuando se arrastra una imagen que infringe los criterios de carga y se suelta en el texto de la publicación, se produce un error del servidor y se muestra un mensaje de error genérico al usuario. NPR-24243
* Correcciones en varios problemas del servidor de AEM Communities. NPR-23971: revisión para CQ-4243144, CQ-4242145, CQ-4243365, CQ-4244098
* Correcciones de varios problemas de Adobe Social. NPR-24242: revisión para CQ-4245054, CQ-4245120, CQ-4245296

### Campaign  {#campaign}

* La salida de json de Campaign no contiene la raíz de contexto del servlet. NPR-23733: revisión para CQ-4243827

### Medios convencionales  {#msm}

* Cuando se despliega la página, la Live Copy no muestra las propiedades de tiempo de activación y desactivación heredadas del patrón. NPR-23873: revisión para CQ-4243431
* La operación LiveCopy no ignora los nodos secundarios de los componentes eliminados. NPR-23058: revisión para CQ-4211662

### Descarga {#offloading}

* Solicitud de mecanismo para limpiar recursos de las instancias de trabajador después de procesarlos o de forma periódica. NPR-23638: Revisión para Granite-21337

## Forms {#forms-8}

### Paquete de complemento de Forms {#forms-add-on-package-8}

#### Formularios adaptables {#adaptive-forms-1}

* Mueva ReCaptchaConfigService al paquete interno. Revisión para CQ-4217459
* El campo numérico no respeta el valor mínimo. NPR-23967: revisión para CQ-4244830
* Compatibilidad con varios elementos compartidos en la integración de formularios adaptables con Adobe Sign. NPR-23383

#### Integración de back-end  {#backend-integration}

* (FDM) (WebService) Compatibilidad con la construcción de extensiones de WSDL en WSDL Parser. NPR-23640, NPR:23236: Revisión para 4205821
* Para incluir SDLInvokerParams en el SDK del cliente del complemento de Forms. NPR-23157

### Instalador JEE de Forms  {#forms-jee-installer-7}

#### Administración de procesos {#process-management}

* No se puede abrir el espacio de trabajo después de aplicar el nuevo archivo axis.jar. NPR-23316
* LiveCycle vulnerable a XSS en PMAdmin. NPR-23267
* Después de actualizar a AEM 6.1 Forms, el espacio de trabajo HTML se bloquea al acceder a la lista de tareas para usuarios específicos. NPR-23943

#### Núcleo {#core}

* Forms JEE admite autenticación mutua PKCS#11. NPR-21372

#### Servicio PDFG  {#pdfg-service-2}

* El servicio de captura de papel se está bloqueando mientras se procesan simultáneamente los archivos TIFF (con un tamaño aproximado de 50 KB). NPR-23556

#### Forms Designer {#forms-designer}

* Salida del servidor de AEM Forms: falta una descripción alternativa para las anotaciones. NPR-22207
* Agregue compatibilidad con PDF/UA a los formularios XML generados mediante Designer y el servicio de salida. NPR-23132

### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión 6.3.2.2.  {#osgi-bundles-and-content-packages-included-in-4}

Lista de paquetes OSGi incluidos en AEM 6.3.2.2

[Obtener archivo](assets/do-not-localize/6_3_2_2_bundle-list.txt)

Lista de paquetes de contenido incluidos en AEM 6.3.2.2

[Obtener archivo](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Paquete de correcciones acumulativas 6.3.2.1 {#cumulative-fix-pack-9}

El paquete de correcciones acumulativas 6.3.2.1 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 2 (6.3.2.0) de AEM 6.3 en abril de 2018.

Los aspectos destacados del **AEM paquete de correcciones acumulativas** son:

* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.10.
* Se ha mejorado el procesamiento de los componentes de Parsys en la interfaz de usuario clásica.
* Se han actualizado los paquetes de modelos de sling para incluir la corrección de conjuntos de caracteres.
* Se ha realizado la publicación en Brand Portal asincrónica para todos los tipos de recursos.
* Se ha actualizado coralui-component-richtexteditor.git de 0.1.15 a 0.1.16
* Correcciones en la funcionalidad de mostrar u ocultar del componente desplegable.
* Se habilitó el volteado de imagen para el componente de imagen principal.
* Actualizado  felix   Paquetes http para activar atributos de sesión.

* Se ha eliminado cache=true en los modelos Sling debido a problemas de consumo de memoria.

### Recursos {#assets-9}

* Al cambiar el título o la imagen en miniatura en la configuración de la carpeta de recursos, se anulan el grupo y los permisos originales de la carpeta. NPR-22171: revisión para CQ-4216080
* La interfaz de usuario genera el error “Error al publicar en Brand Portal”, mientras que el trabajo se agrega a la cola de replicación y los recursos se publican en Brand Portal. NPR-22179: revisión para CQ-4205273
* (IU táctil) Ubicación de carga predeterminada para los recursos en la vista de columnas. NPR-22465: revisión para CQ-4237057
* AEM emite un error StackOverflow al intentar copiar un esquema de recursos de /conf/global a /conf/ mytenant . NPR-22489: revisión para CQ-4235875
* Error al intentar descomprimir un archivo ZIP debido al espacio de seguimiento al final del nombre de la carpeta. NPR-22522: revisión para CQ-4238036
* La ordenación mediante la columna de título de recurso no funciona para los resultados de búsqueda. NPR-22908: revisión para CQ-4239076
* El vídeo de YouTube está etiquetado con la ruta completa en lugar del nombre de la etiqueta. NPR-22976: revisión para CQ-4238669
* La reordenación de carpetas en una carpeta reordenable no persiste. NPR-23125: revisión para CQ-4231761
* HTTP 504: Error de tiempo de espera de puerta de enlace al intentar compartir colecciones mediante el vínculo de uso compartido. NPR-21928: revisión para CQ-4234507
* Los metadatos de palabra clave PDF no se extraen ni modifican correctamente cuando hay varias palabras clave asociadas a un recurso PDF. Para resolver el problema, se ha eliminado la propiedad de metadatos del campo Asunto de los recursos PDF. Sin embargo, puede editar el esquema de metadatos para agregar un campo de texto de varios valores para el campo Asunto. NPR-21972: Revisión para 4215741****
* Los recursos incorrectos se eliminan si se cambia la carpeta seleccionada entre el momento en que se muestran las dos ventanas emergentes. NPR-21980: revisión para CQ-4233675
* (DAM) Varias vulnerabilidades de scripts entre sitios (XSS) al agregar al asistente de recopilación. NPR-22432: revisión para CQ-4327086
* La descarga de recursos falla al usar Digital Rights Management en Assets en Safari. Los usuarios no pueden descargar recursos con nombres de archivo largos y de renuncia de responsabilidad. NPR-22747: Revisión para CQ-4236460 y CQ-4235274
* Haga que el uso compartido sea público como opción predeterminada al publicar recursos en Brand Portal. NPR-21931: revisión para CQ-4218816

### Sitios {#sites-9}

* El nuevo elemento de la bandeja de entrada Flujo de trabajo muestra la ruta de la página en lugar del título de la página. NPR-21634: revisión para CQ-4230672
* Los componentes de estructura editables pierden los nombres de clase CSS necesarios para la cuadrícula adaptable al editarla. NPR-21741: revisión para CQ-4232374
* (TouchUI) Varias vulnerabilidades de scripts entre sitios (XSS) para componentes HTL. NPR-21899: revisión para CQ-4232511
* No se puede cambiar el tipo de recurso de imagen de medios mixtos de fragmento de contenido. NPR-21907: revisión para CQ-4233401
* La pantalla completa RTE para el cuadro de diálogo IU táctil oculta los complementos RTE. NPR-22034: revisión para CQ-4235457
* (IU táctil) El editor de texto enriquecido elimina todos los atributos que no sean id de la etiqueta &lt;a>. NPR-22044: revisión para CQ-4234133
* Varios parámetros apilados debido a consultas de larga duración (más de 6) hacen que AEM se ralentice. NPR-22134: revisión para CQ-4233904
* No se pueden cambiar los permisos en nodos que tengan dos puntos en el nombre. NPR-22136: revisión para CQ-4236221
* (IU clásica) El editor de texto enriquecido html agrega &#39;estilo de posición de lista: interior;&#39; como estilo en línea para la etiqueta &lt;ul>. NPR-22145: revisión para CRTE-114
* Hacer que TreeNode vuelva al atributo de nombre cuando el texto esté vacío. NPR-22146: Revisión para CQ-4234724/CQ-4236300
* Problemas con la fuente RSS, puerto -1 a AEM 6.3. NPR-22176: Revisión para CQ-4233339
* (IU clásica) El método abreviado de texto pegado (Ctrl+V) no funciona para el componente Texto OTB (texto enriquecido). NPR-22224: revisión para CQ-4236224
* El filtro de Tagfield  no funciona del modo esperado al escribir el texto. NPR-22236: revisión para CQ-4236655
* (Editor de páginas) Al pegar datos de texto en el componente de mapa de imágenes, el componente Texto también se pega al pegar datos de texto en el componente de mapa de imágenes. NPR-22264: revisión para CQ-4236230
* El campo exigido de Carga del cuadro de diálogo del archivo causa problemas en el envío del cuadro de diálogo. NPR-22464: revisión para CQ-4222192
* Mover los permisos sin replicación provoca que se inicie una solicitud para el flujo de trabajo de activación si no se puede activar la página movida o sus referentes. NPR-22467: revisión para CQ-4211765
* Problemas de rendimiento al cargar una página con audiencias grandes (más de 2000). NPR-22478; revisión para CQ-4209567
* Problemas de persistencia cuando ContextHub almacena la superposición de la capa de persistencia predeterminada durante la inicialización. NPR-22479: revisión para CQ-4218399
* El inicio con varias páginas no publica subpáginas en los servidores de publicación si “incluir subpáginas” no está marcado en  primera raíz de contenido. NPR-22482: revisión para CQ-4237818
* (IU táctil) La eliminación de lanzamientos mediante la consola de IU clásica hace que todas las páginas sean no editables. NPR-22491: revisión para CQ-4225074
* Problemas con el componente de Imagen debido a espacio adicional en  el cuadro de diálogo . NPR-22528: revisión para CQ-4238183
* Al abrir el componente mediante  en modo Inlide, los complementos cargados anteriormente no son visibles por segunda vez. NPR-22591: revisión para CQ-4236850
* Al eliminar un inicio en un lanzamiento anidado, los subinicios quedan huérfanos. NPR-22621; revisión para CQ-4202639
* (Barra de tareas de la IU clásica) La ficha Flujo de trabajo se desactiva cuando la página está en la etapa de bloqueo del flujo de trabajo. NPR-22722: revisión para CQ-4237557
* Después de voltear una imagen agregada en el componente de imagen de una página, los cambios no se guardan y  la imagen original se muestra en la página. Se ha agregado compatibilidad con el procesamiento al componente principal de la imagen mediante [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141). NPR-22801: revisión para CQ-4221539
* Cuando el usuario intenta eliminar el anclaje existente del menú de anclaje, la ventana del componente Editor de texto enriquecido se cierra y los cambios permanecen sin guardar. NPR-22802: revisión para CQ-4238167
* El filtro Omniture no muestra todas las acciones de la consola Sitios. NPR-22804: revisión para CQ-4239007
* Problema  con Copiar/Pegar en la IU táctil con el portapapeles del SO y el portapapeles interno de AEM. NPR-22807: revisión para CQ-4220383
* Incoherencia en el resaltado de extracto devuelto por la búsqueda de Lucene. NPR-22879: revisión para CQ-4238513
* La activación de una página con  la publicación de instancias da como resultado un estado verde en lugar de girar a ámbar. NPR-22927: revisión para CQ-4236310
* (StyleSystem) La posición de la pantalla salta al seleccionar estilo en la ventana emergente. NPR-23183: revisión para CQ-4238867
* (Administrar publicación) El paso al mes siguiente del calendario requiere varios clics. NPR-23508: revisión para CQ-4242732

### Plataforma  {#platform-2}

* El exportador Sling servlet no exporta correctamente los caracteres japoneses. NPR-22153: revisión para CQ-4228920
* Punto muerto del programador durante el inicio. NPR-22440: revisión para Sling-7004
* No se pueden sincronizar grupos entre dos instancias de publicación. NPR-21943: revisión para Granite-19564
* Problemas de rendimiento con org.apache.sling.i18n resolución de sesión/recurso compartido. NPR-23390: revisión para Sling-7543

### Integración  {#integration-5}

* ResourceResolver no cerrado en com.day.cq.analytics.sitecatalyst. NPR-22323: revisión para CQ-4236515
* TargetContentImpl hace que AEM seo lenta durante consultas de larga duración. NPR-22361: revisión para CQ-4236907
* El motor de destino (mbox.js, at.js) no utiliza direcciones URL manipuladas y utiliza direcciones URL que contienen dos puntos, lo que puede provocar errores en determinadas implementaciones. NPR-22366: revisión para CQ-4237854
* Al proporcionar un at.js o mbox.js personalizado, la secuencia de comandos de inclusión se escribe en la página como texto en lugar de etiquetas HTML. NPR-22441: revisión para CQ-4203691
* En el modo de Target, los autores pueden modificar un componente heredado del modelo sin cancelar la herencia. NPR-22751: revisión para CQ-4237907
* PersonalizationDataSource emite una excepción de puntero nulo debido a que falta  jcr : nodo de contenido. NPR-22850: revisión para CQ-4222122
* La segmentación AEM falla al   no inglés. NPR-22917: revisión para CQ-4218213
* A la publicación de una página con contenido de destino le faltan recursos relacionados. NPR-23064: revisión para CQ-4227119
* Los usuarios no pueden ver los valores de parámetro estático de prueba en la variable  llamada de mbox que se puede ver al probar con AT.js como la biblioteca del cliente en la configuración de la nube. NPR-21930: revisión para CQ-4234520

### WCM: componentes base  {#wcm-foundation-components-1}

* iParsys crea el cambio de posición después de desmarcar la casilla de verificación cancelar/desactivar herencia. NPR-21905: revisión para CQ-4230951
* La funcionalidad Mostrar/Ocultar del componente desplegable del formulario no funciona correctamente. NPR-22327: revisión para CQ-4222853
* El componente CAPTCHA ha quedado obsoleto para una mejor seguridad, si utiliza el componente CAPTCHA, entonces envíe el mensaje &quot;El componente Captcha está obsoleto y ya no debe usarse&quot;. después de instalar la versión 6.3.2.1 o una posterior. AEM componente se puede personalizar para incluir reCAPTCHA para una mejor seguridad NPR-22151: Revisión para CQ-4220052

### WCM: editor de páginas {#wcm-page-editor}

* Se ha reflejado el proceso de ejecución de scripts en sitios múltiples al utilizar un selector no válido. Revisión para CQ-4270397

### Traducción {#translation-4}

* Investigación de los problemas con la funcionalidad Vista previa. NPR-22114: revisión para CQ-4223753

### Interfaz de usuario {#user-interface-2}

* Problemas con el selector de mes del Calendario de Coral cuando se establece el intervalo de fechas “min” y “max”. NPR-22716: revisión para CUI-7187
* (IU clásica) El componente muestra los valores predeterminados aunque el servicio del modelo de datos de formulario asociado esté establecido en un campo vacío. NPR-22272: revisión para GRANITE-19744

### Granito  {#granite-2}

* Problemas de estabilidad con la instancia del editor de AEM de Asset Share provocados por una pérdida de memoria. NPR-22205, NPR-23178: revisión para Sling-5668, Sling-7292 y Sling-7470.
* No se debe usar la identificación de servicio inestable para los nombres de atributos de sesión. NPR-22821: revisión para Granite-21059
* Cuando  un http   la sesión administrada por la pizarra se invalida; la sesión de contenedor también se invalida si la sesión no tiene otros atributos de sesión. NPR-23059: revisión para FELIX-5819
* LogbackManager puede perder alguna configuración de OSGi en el momento del inicio. NPR-23060: revisión para Granite-19791

### Comercio {#commerce-3}

* Habilitar la creación de flujo de trabajo en el menú Fragmentos de experiencia. NPR-22347: revisión para CQ-4221661
* Errores de fragmentos de experiencia reproducibles en WeRetail. NPR-21958: revisión para CQ-4220061
* Al activar una página que contenga un fragmento de experiencia eliminado, se produce una excepción NullPointerException. NPR-23179: revisión para CQ-4239939

### Proyectos {#projects}

* (Proyecto en varios idiomas) Project no lista trabajos de traducción para más de 19 idiomas. NPR-22498: revisión para CQ-4229978

### Flujo de trabajo {#workflow}

* (IU clásica) La activación o desactivación de un iniciador de flujo de trabajo produce un comportamiento incorrecto. NPR-22907: revisión para CQ-4239153

## Forms {#forms-9}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

Los aspectos destacados de AEM Forms son:

* Compatibilidad añadida con el tipo de entrada HTML5.
* Corrección de la autenticación de encabezado SOAP básica.
* Compatibilidad añadida con el atributo del título para el hipervínculo.
* Identificador PDF/UA habilitado en el árbol de accesibilidad de Forms Designer.
* Autenticación de certificados para los usuarios de Workbench habilitada.
* Compatibilidad añadida para producir archivos PDF compatibles con PDF/A-2a o PDF/A-3a.

### Paquete de complemento de Forms  {#forms-add-on-package-9}

#### IU de Forms-Admin {#forms-admin-ui}

* La contraseña es visible en texto sin formato al inspeccionar el campo de contraseña para las páginas de configuración de Conectores de ECM. NPR-22508: revisión para CQ-4236065

#### Servicio de Forms {#forms-service}

* Cuando SSL está habilitado, los eventos Enviar y Abandonar no funcionan con Form Analytics. NPR-22637; Revisión para CQ-4237973

#### Administración de usuarios {#user-management}

* No se puede sincronizar LDAP debido a una versión cglib-nodep incorrecta. NPR-22493: revisión para CQ-4234099

#### Formularios adaptables  {#adaptive-forms-2}

* Las funciones personalizadas para el editor de reglas están agregando un extra; después de la llamada a la función, por lo tanto, se produce un error en la validación aunque la función personalizada devuelve true. NPR-22481: revisión para CQ-4235499
* Independientemente del patrón de fecha seleccionado, el componente selector de fechas no sigue el patrón al mostrar los mensajes de validación mínimo y máximo. NPR-22444: revisión para CQ-4236269
* El formato de fecha que se envía en la solicitud de envío debe coincidir con el patrón proporcionado en el componente de selección de fecha. NPR-22384
* El número máximo especificado de caracteres para un cuadro de texto del formulario adaptable no se acepta en los dispositivos Android 6.0 Samsung. NPR-22363, NPR-22364: revisión para CQ-4235205
* (Microsoft Edge) (IE11) El componente de campo de texto Formulario adaptable que tiene un campo multilínea muestra &#39;Null&#39; como valor predeterminado en lugar de en blanco. NPR-22284: revisión para CQ-69107
* La codificación de entrada SOAP UTF-8 en formularios adaptables devuelve errores en páginas de errores. NPR-20105: revisión para CQ-4222669
* El componente Contenedor de AEM Forms no está disponible para edición una vez configurado el formulario incorrecto en la página Sitios. Revisión para CQ-4237456
* Las pruebas de desarrollo fallan cuando se ejecutan en servidores JEE. Revisión para CQ-4222082
* Las pruebas AF fallan en servidores JEE debido a los problemas de minimización en el marco de Calvin. Revisión para CQ-4217220

#### Administrador de Forms {#forms-manager}

* (Firefox) No se pueden actualizar las propiedades de Esquema XML de Forms adaptable, ya que las opciones del Documento de registro (DOR) no se incluyen como preseleccionadas en la página de propiedades. NPR-22298: revisión para CQ-4237402
* Los formularios que se modifican después de publicar la página no se vuelven a publicar en el sitio. NPR-23013: revisión para CQ-4236566

#### Integración de back-end  {#backend-integration-1}

* La autenticación básica de OOTB para los servicios SOAP no funciona para la autenticación básica en la integración de FDM. NPR-23238: revisión para CQ-4241308

#### Administración de correspondencia  {#correspondence-management}

* Los XDP de OOTB, cuando se utilizan dentro de la carta y se previsualizan, muestran el contenido superpuesto con el pie de página. Revisión para CQ-4212414

#### Servicio del ensamblador {#assembler-service}

* Discrepancia entre Acrobat DC y AEM informes sobre el error de comprobación de compatibilidad con PDF/A-1b. NPR-22051, NPR-22050: revisión para CQ-4226128, CQ-4227671

### Instalador JEE de Forms  {#forms-jee-installer-8}

#### Workbench {#workbench}

* Autenticación de certificados para los usuarios de Workbench habilitada. NPR-20644: revisión para CQ-4214486
* La descarga del registro del servidor mediante Workbench solo funciona para un servidor, mientras que para el otro no funciona. NPR-21079: revisión para CQ-4229842

#### Administración de procesos  {#process-management-1}

* (Espacio de trabajo HTML) Problemas de tamaño de pantalla con las barras de desplazamiento. NPR-23288
* (Espacio de trabajo HTML) Los puntos de inicio del proceso no se ordenan en orden alfanumérico. NPR-22841 revisión para CQ-4238944
* (Espacio de trabajo HTML) La preparación de datos se activa al cerrar el formulario en el espacio de trabajo. NPR-21127: revisión para CQ-4224574
* (Espacio de trabajo HTML) Al invocar un proceso que requiere notas con descripciones largas, el botón de expansión Notas no funciona. Revisión para CQ-4241488

#### Núcleo  {#core-1}

* Error al iniciar cuando se pone en marcha el planificador. NPR-22990
* Impedir que los navegadores almacenen las credenciales introducidas en los formularios HTML. NPR-21762: revisión para CQ-4206543
* Deben solucionarse los problemas notificados en el análisis del código estático de Core. Revisión para CQ-104446

#### Servicio PDFG  {#pdfg-service-3}

* El generador de PDF no produce documentos PDF con niveles de marcadores especificados. NPR-22921, NPR-22285: revisión para CQ-4230562
* Compatibilidad añadida para producir archivos PDF compatibles con PDF/A-2a o PDF/A-3a. NPR-23021: revisión para CQ-4214172

#### Forms Designer {#forms-designer-1}

* Falta el identificador PDF/UA cuando se guarda como PDF desde Designer. NPR-23137
* Objetos de ruta, por ejemplo: los bordes, subrayados e hipervínculos no se etiquetan cuando se guardan como PDF desde Designer. NPR-23136
* El objeto de imagen no tiene ningún cuadro delimitador cuando se guarda como PDF desde Designer. NPR-23134
* Los hipervínculos en línea definidos en Designer no se etiquetan ni tienen texto alternativo cuando se guardan como PDF desde Designer. NPR-23133
* Al abrir el paquete de datos XML con AEM 6.3 Forms Designer, se quita el formato XHTML del origen XML. NPR-21178: revisión para LC-3917046

#### Instalación de LCM  {#install-lcm}

* Actualice Jsafe Jars a Cryptoj 6.1.3.1 en el instalador y LCM. NPR-21370

#### Servicio de firmas  {#signatures-service}

* Excepción al intentar firmar o certificar digitalmente un documento PDF mediante HSM. NPR-21154: revisión para CQ-4226978

### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión 6.3.2.1.  {#osgi-bundles-and-content-packages-included-in-5}

Lista de paquetes OSGi incluidos en AEM 6.3.2.1

[Obtener archivo](assets/do-not-localize/bundle-list_002_.txt)

Lista de paquetes de contenido incluidos en AEM 6.3.2.1

[Obtener archivo](assets/do-not-localize/content_package_comparison.txt)

El paquete de correcciones acumulativas 6.3.1.2 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde que está disponible de forma general el paquete de servicio 1 (6.3.1.0) de AEM 6.3 en octubre de 2017.

Los aspectos destacados del paquete de correcciones acumulativas de AEM son:

* Se ha modificado la interfaz de usuario para admitir la implementación de la funcionalidad CUG en AEM Assets.
* Se han corregido los problemas de la interfaz de usuario en la página de comprobación de licencias para obtener una mejor experiencia.
* Se ha habilitado la compatibilidad con tareas de flujo de trabajo de OSGi en la aplicación de AEM Forms.

### Recursos {#assets-10}

* Se ha modificado la interfaz de usuario para admitir la implementación de la funcionalidad CUG en AEM Assets. NPR-19485
* La carga de un recurso como nodo secundario directo por sí mismo mediante la IU táctil provoca un problema. El recurso se carga como elemento secundario directo del recurso seleccionado anteriormente. NPR-19736
* El predicado de intervalo de fechas y el predicado de intervalo no funcionan al cargar una búsqueda guardada o una colección inteligente. NPR-19844: revisión para CQ-4220808
* La instancia de AEM se vuelve lenta cuando se publican varios recursos (más de 4) en Brand Portal. NPR-20009: revisión para CQ-4213426
* No se pueden descargar recursos con espacios desde la página de comprobación de licencias. NPR-20067: revisión para CQ-4216557
* Problemas de procesamiento al cargar archivos PSB con varias capas alfa. NPR-20250: revisión para CQ-4220869
* Los usuarios no pueden descargar recursos con nombres de archivo largos y una exención de responsabilidad definida. NPR-20254
* ProductAssetsUploader deja los archivos temporales de la caché de JAVA en la carpeta TEMP de Java. NPR-20256: revisión para CQ-4221801
* Reemplazar el código de comparación de versiones con el código propiedad de Adobe debido a problemas de licencias. NPR-20272: revisión para CQ-4223758
* Los metadatos de una propiedad de cadena, documentNumber, se muestran como una fecha, mientras que debería ser un número. NPR-20291: revisión para CQ-4223991
* La extracción de texto se atasca para un PDF dañado. NPR-20416: revisión para CTG-4150375
* Los archivos comprimidos que incluyen recursos con nombres no compatibles con UTF-8 no se descargan correctamente. NPR-20420: revisión para CQ-4219961
* Demasiados caracteres en OmniSearch hacen que el servidor de AEM se bloquee. NPR-20434: revisión para CQ-4223602
* El defecto de metadatos de la API de recursos DAM rompe las API de xmp-write-back. NPR-20607: revisión para CQ-4220455
* Problemas de rendimiento al agregar usuarios a las colecciones. NPR-20699: revisión para CQ-4225733
* No se debe permitir la publicación en Brand Portal desde AEM para conjuntos de Dynamic Media. NPR-20320: revisión para CQ-4221147
* El vídeo con espacios y acentos no genera ningún vídeo para la página Representaciones. NPR-19961: revisión para CQ-4221014
* Se han resuelto varios problemas de gestión de carpetas con las API de Recursos. NPR-20569
* AEM Dynamic Media Classic (anteriormente Scene7) no puede sincronizar recursos del servidor AEM cuando la ruta de destino de la configuración del servicio en la nube apunta a una subcarpeta de la ruta raíz. CQ-4228265
* Se ha agregado el paquete de correo electrónico de apache commons `{org.apache.commons/commons-email/1.5}` reemplazando a `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`.

### Sitios {#sites-10}

* Problemas de permisos de administración: no se pueden quitar los miembros del grupo cerrado de usuarios de las propiedades de página. NPR-20631
* El nombre del flujo de trabajo escrito debe estar disponible en el cuadro Notificación al publicar una página mediante Administrar publicación. NPR-20046: revisión para CQ-4221586
* Al aplicar texto con estilo en dos filas en el Editor de texto enriquecido y, a continuación, combinarlas en un párrafo, se eliminan los espacios con estilo. NPR-20110: revisión para CQ-4223051
* Los cambios realizados en las propiedades de campo en varias pestañas del cuadro de diálogo de edición de propiedades a veces no se guardan. NPR-20286
* Etiqueta inesperada al final del contenido pegado en el fragmento de contenido. NPR-20413: revisión para CQ-4224014
* Se ha implementado un mecanismo en Adobe Campaign para recuperar la política de un recurso de contenido de un recurso de segmentación externo. NPR-20667
* El complemento Richtext no funciona ni para la barra en línea ni para la barra de pantalla completa en la IU táctil de varios campos. NPR-20973

### Campaign {#campaign-1}

* Los marcadores de posición no están visibles en una página que contiene varios componentes parsys. NPR-20436; revisión para CQ-4215000

### Comercio {#commerce-4}

* Los fragmentos de experiencia no se muestran correctamente en Internet Explorer 11. NPR-20161: revisión para CQ-4223319
* En los flujos de trabajo comerciales, se inserta automáticamente una imagen en blanco al crear una variante basada en un producto principal con varias imágenes. NPR-20068: revisión para CQ-4222048
* El filtrado mediante etiquetas en páginas de colección en la consola de productos no funciona. NPR-20292: revisión para CQ-4224023

### Comunidades  {#communities-8}

* Resultados de búsqueda incoherentes con el componente de resultados de búsqueda. NPR-20070: revisión para CQ-4220913
* Las notificaciones por correo electrónico no se activan para ninguna de las actividades relacionadas con moderadores en los componentes publicados. NPR-20122
* La paginación en blanco sin resultados se muestra para los usuarios anónimos de la comunidad. NPR-20136: revisión para CQ-4220738
* Configurar el activador de alertas cuando se detecta un UGC como correo no deseado o cuando un usuario publica en un sitio moderado previamente. NPR-20274: revisión para CQ-96850
* Varios problemas resueltos en las páginas del sitio de AEM Communities, incluidas las redirecciones incorrectas y los problemas de actualización de páginas. NPR-20344
* CommunityUserOperationExtension se ejecuta en una excepción de conversión de clase. NPR-20532: revisión para CQ-4224385
* Después de crear un sitio de Communities, los usuarios no pueden abrirlo desde el mapa del sitio porque la ruta de contexto no se antepone a la dirección URL. NPR-20730

### Integración {#integration-6}

* Migración de las credenciales existentes de Analytics a la autenticación WSSE. NPR-19962: revisión para CQ-4218071
* Reactivar el segmento tras cualquier modificación falla y genera un error. NPR-20054: revisión para CQ-4218401
* La configuración del servicio en la nube Search&amp;Promote ignora el método de recuperación de formularios, lo que hace que no se pueda utilizar en la instancia de creación. NPR-20447: revisión para CQ-4206076
* La definición ambigua del filtro en el paquete de contenido hace que las rutas se sobrescriban cuando se instala la función Search&amp;Promote. NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* Las propiedades de metadatos de recursos de tipo TXT se muestran en diferentes editores de metadatos cada vez que se muestran sus propiedades. NPR-20239

### Plataforma {#platform-3}

* Se ha resuelto una excepción de resolución de recursos sin cerrar. NPR-19749: revisión para Granite - 19143
* Solicitud para que se muestren las tarjetas personalizadas junto con las comprobaciones de estado predeterminadas en el panel de operaciones. NPR-20145
* La capa de anotación del editor de páginas no funciona correctamente en Internet Explorer 11. NPR-20222: revisión para CQ-4222818
* La sesión se filtra al configurar el agente de usuario como administrador en el agente de replicación. NPR-20578
* El parámetro requestAttributes no se desactiva para las demás instrucciones data-stir-resource. NPR-20639: Revisión para 4226206
* Se han corregido problemas con las solicitudes de cabezal de curl para los recursos de OOTB en AEM. NPR-20781: revisión para CQ-4221520

### Proyectos {#projects-1}

* El acceso a diferentes proyectos desde la consola Proyectos tarda más tiempo en cargarse. NPR-20314
* La instalación de AEM 6.3.0.1 elimina el almacén de claves del usuario de dam-update-service. NPR-20018
* En algunas implementaciones personalizadas, los usuarios que intentan seleccionar un usuario asignado en el módulo addTask tardan más en rellenar la lista en el selector de usuarios. NPR-20283: revisión para CQ-4224193

### Interfaz de usuario {#user-interface-3}

* El campo de color se configura como “siempre obligatorio” a pesar de los atributos del cuadro de diálogo. NPR-19702
* La barra de desplazamiento no se muestra para el componente de varios campos en la pantalla completa en Internet Explorer 11. NPR-20261: revisión para CQ-4219782
* Las consultas anteriores no se anulan en caso de que se activen consultas consecutivas que produzcan resultados incorrectos. NPR-20398: revisión para GRANITE-19306

### Flujo de trabajo {#workflow-1}

* Los usuarios no reciben notificaciones sobre las tareas de flujo de trabajo que reciben en su bandeja de entrada. NPR-20213: revisión para CQ-4221639
* El selector de usuarios de granito OOTB no carga ningún usuario cuando se hace clic en el menú desplegable en el paso del participante del cuadro de diálogo del modelo de flujo de trabajo. NPR-20236

## Forms {#forms-10}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms  {#forms-add-on-package-10}

#### Formularios adaptables {#adaptive-forms-3}

* Falta la compatibilidad con la expresión de agregación para paneles repetidos. NPR-20861
* El menú desplegable muestra el último valor almacenado aunque el servicio del modelo de datos de formulario asociado no devuelva ningún valor. NPR-20710
* No se pueden editar las reglas existentes con restricciones booleanas en el Editor de reglas. NPR-21128

#### Portal de formularios  {#form-portal}

* El perfil HTML se muestra para un formulario adaptable incluso cuando su tipo de recurso no es XDP. NPR-20079

#### Integración de back-end  {#backend-integration-2}

* No se puede establecer el valor del componente del componente entre verdadero/falso. NPR-21111

#### Flujo de trabajo de OSGI  {#osgi-workflow}

* Administre listas de envío de flujo de trabajo solo diez aplicaciones. CQ-4230193

#### Formularios HTML5  {#html-forms-3}

* El nombre de un objeto de formulario XDP como subformulario se muestra como información de objeto cuando no se define en las configuraciones de accesibilidad. NPR-20523

### Instalador JEE de Forms  {#forms-jee-installer-9}

#### Administración de procesos {#process-management-2}

* El punto de inicio de FormSetPrefillApp no rellena previamente los campos de conjunto de formularios en la aplicación de AEM Forms. NPR-20950

#### Forms - AEM (LiveCycle)  {#forms-aem-livecycle}

* Instale la última biblioteca CTJPEG2K para una vulnerabilidad de seguridad crítica. Esto afecta a los módulos XMLFM (AEM y IfBA), RM y PDFG. NPR-20625: NPR-21337.

### Paquetes de funciones incluidos {#feature-packs-included}

#### Aplicación de AEM Forms {#aem-forms-app}

* Se ha habilitado la compatibilidad con tareas de flujo de trabajo de OSGi en la aplicación de AEM Forms. CQ-4222638

### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión 6.3.1.2.  {#osgi-bundles-and-content-packages-included-in-6}

Lista de paquetes OSGi incluidos en AEM 6.3.1.2

[Obtener archivo](assets/do-not-localize/6_3_1_2-bundle-list.txt)

Lista de paquetes de contenido incluidos en AEM 6.3.1.2

[Get ](assets/do-not-localize/6_3_1_2-content-package-list.txt)
FileAEM Cumulative Fix Pack 6.3.1.1 es una actualización importante que incluye varias correcciones internas y de cliente desde la disponibilidad general de AEM 6.3 Service Pack 1 (6.3.1.0) en octubre de 2017.

Los aspectos destacados del paquete de correcciones acumulativas de AEM son:

* Se habilitó la acción Publicar en Brand Portal para el formulario de esquema de metadatos predeterminado.
* Cambio de comportamiento en la visualización de títulos en la tarjeta de imagen para una imagen que tiene dc: propiedad title establecida en String [] (multifield).
* Se ha sustituido la representación del tiempo en el lado del servidor por el componente de tiempo de base.
* Se habilitaron las etiquetas de publicación de AEM a Brand Portal desde la consola de tagadmin/tagging.
* Se ha publicado la API de JSON para consumir los fragmentos de contenido.
* El repositorio integrado (Apache Jackrabbit Oak) se ha actualizado a la versión 1.6.5.

### Recursos {#assets-11}

* La asignación de dos campos con la misma propiedad con diferentes tipos de campo de propiedad genera un error interno. NPR-19462: HF para CQ-4216828
* dc: title y dc: description no cambian a un valor de varios campos en  crx /de. NPR-19570: HF para CQ-4209086
* El visor dinámico carga la representación del vídeo de menor calidad para probar la reproducción del vídeo en modo de autor. NPR-19004
* No se puede descargar la representación dinámica para los recursos que incluyen espacios en sus nombres. NPR-19433: revisión para CQ-4211738
* No se puede cargar la lista completa de páginas/recursos en la vista de columna al usar Chrome. NPR-19566: revisión para CQ-4214248
* La opción Publicar en Brand Portal no está disponible al seleccionar un esquema o una faceta de búsqueda o ajuste preestablecido. NPR-19550
* Al seleccionar un recurso en la vista de columna y hacer clic en Editar, la página devuelve un error. NPR-20301: revisión para CQ-4224052
* La visualización Caducidad del recurso está desactivada cuando se cruzan zonas horarias positivas y negativas. NPR-20329: revisión para CQ-4219333

### Campaña {#campaign-2}

* Los componentes del deslizador de Campaign no aparecen cuando se elige la experiencia predeterminada para una campaña. NPR-19213

### Integración {#integration-7}

* El archivo at.js personalizado no se publica cuando se accede al mismo con el usuario anónimo. NPR-19542: revisión para CQ-4219592
* El campo de motor de destino en el asistente de configuración se establece en ContextHub (AEM) en lugar de en Adobe Target. NPR-19320: HF para CQ-4218465
* La sección Audiencia se daña al crear experiencia. NPR-19110
* El cuadro de diálogo de destino no se muestra en el modo de segmentación cuando se edita un módulo de destino y se guarda más de una vez. NPR-19144: revisión para CQ-4216708
* Obtenga acceso a las propiedades de los artículos que se establecen incorrectamente en la solución de publicación digital de Adobe en la IU clásica. NPR-19367
* Comportamiento incorrecto del plegado automático al personalizar las ofertas a través de Campaign si los usuarios tienen acceso a varias áreas. NPR-19290: revisión para CQ-4218029

### Sitios {#sites-11}

* Los valores desplegables de campos multicompuestos no se rellenan de nuevo debido al cambio de código en Sidekick.js después de actualizar la instancia a AEM 6.1SP2-CFP3. NPR-19450: HF para CQ-4194771
* WCMMode.EDIT no funciona para los componentes de destino en modo de creación. NPR-19387
* Se ha publicado la API de JSON para consumir los fragmentos de contenido. NPR-19500
* La funcionalidad negrita, cursiva y subrayado no se pueden usar en los campos del editor de texto enriquecido en el cuadro de diálogo de creación. NPR-19670: NPR-19718: revisión para CQ-4219088

### Móvil bajo demanda {#mobile-on-demand-1}

* El procesamiento de problemas con la consola de artículos de AEM al hacer uso de imágenes de tamaño completo hace que sea lento. NPR-19088

### Traducción {#translation-5}

* No se puede generar la vista previa de los proyectos de traducción. NPR-19289

### Seguridad {#security}

* Error de conexión SSL. No se puede establecer una conexión segura con el servidor. NPR-19628

### Comunidades  {#communities-9}

* El correo se activa en la publicación de contenido con sitios moderados previamente. NPR-20008
* Las notificaciones por correo electrónico no funcionan para ninguna de las actividades relacionadas con moderadores en los componentes publicados. NPR-19767: HF para CQ-4218060

### Plataforma  {#platform-4}

* Problemas de estabilidad con la implementación del servidor de producción de AEM. NPR-19707
* Las etiquetas personalizadas que hacen referencia a las etiquetas implementadas como un script no se encuentran tras actualizar a AEM 6.3. NPR-19087
* Correcciones de errores de HTL para AEM 6.3.1. NPR-19161
* El campo Richtext no se puede editar en los componentes de varios campos. NPR-19604: revisión para Granite-16755
* El servicio Plantilla de correo electrónico de Adobe agrega etiquetas a las plantillas de usuario personalizadas. NPR-19190
* Revisión para Oak 1.6.5. NPR-19148

### Comercio {#commerce-5}

* Iniciar el botón de flujo de trabajo después de seleccionar un editor de variaciones XF no tiene ningún efecto. NPR-19642: revisión para CQ-4207796

### Proyectos {#projects-2}

* Los editores de proyectos no pueden copiar/pegar recursos en la carpeta de recursos del proyecto. NPR-19619: revisión para CQ-4215321

### Administración de contenido web  {#web-content-management}

* En la pantalla Despliegue, las casillas de verificación correspondientes a las páginas de Copia activa no se pueden marcar ni desmarcar. NPR-19518
* La edición masiva de propiedades de página no se puede utilizar correctamente, ya que actualmente todas las pestañas y campos están disponibles para procesos de edición masiva. NPR-19451
* Las propiedades OOTB y las propiedades de alineación de imagen no aparecen al editar una imagen en la IU clásica. NPR-19488: HF para CQ-4217914

### Interfaz de usuario {#user-interface-4}

* Al utilizar el explorador Google Chrome, los usuarios no pueden cargar la lista completa de páginas o de recursos mediante la vista de columna en la IU táctil. NPR-19566: revisión para CQ-4214248

### Brand Portal  {#brand-portal-1}

* No se pueden publicar recursos de AEM con comentarios y anotaciones. NPR-19590: revisión para CQ-4218386
* Habilitar las etiquetas de publicación de AEM a Brand Portal desde la consola de administrador de etiquetas/etiquetado. NPR-20271: revisión para CQ-4223948
* Se corrigió el campo “habilitado” en la interfaz de usuario de la configuración de cloudservice de Brand Portal. Revisión para CQ-4211101
* Fallo en la replicación de formularios de búsqueda. Revisión para CQ-4220080

## Forms {#forms-11}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte Versiones de AEM Forms.

### Paquete de complemento de Forms  {#forms-add-on-package-11}

#### Formularios adaptables {#adaptive-forms-4}

* Enviar el flujo de trabajo a JEE no devuelve el parámetro de salida de JEE a AEM y emite el error “Ignorar porque el valor no es primitivo”. NPR-20265
* Los formularios adaptables no admiten PDF como datos adjuntos en Safari. NPR-19625
* RestoreGuideState sobrescribe el mapa de propiedades del contexto personalizado (customcontextproperty). CQ-4222877
* Al configurar Google reCaptcha mediante el servicio en la nube, en entornos que requieren la configuración de org.apache.http.proxyconfigurator para conexiones externas, las llamadas POST no parecen pasar por PROXY. NPR-20454
* Los formularios adaptables basados en esquemas XSD envían valores XML defectuosos para campos numéricos en instalaciones con configuraciones regionales que tienen un separador decimal distinto de “.” que genera errores. NPR-20444
* La configuración de proxy establecida para “Configuración proxy de componentes HTTP Apache” no se cumple al realizar una solicitud HTTP al servidor de terceros. Problemas de tiempo de espera de conexión mediante llamadas HTTP GET o POST. NPR-20457, NPR-20456, NPR-20455, NPR-20451

#### Integración de datos de Forms {#forms-data-integration}

* Los caracteres UTF-8 como resultado del servicio SOAP no se copian correctamente en los campos de formularios adaptables para las configuraciones regionales que no sean del inglés. NPR-20238: NPR-20103.

#### Administración de correspondencia  {#correspondence-management-1}

* Copiar y pegar el contenido del archivo de palabras provoca que se pierda el color y la fuente del contenido en el Editor de texto. NPR-19521

#### Servicio del ensamblador  {#assembler-services}

* Discrepancia entre los resultados de Acrobat y AEM durante la verificación de conformidad de un documento con el formato PDFA-1b. NPR-19280

#### Flujo de trabajo {#workflow-2}

* El paso de firma de flujo de trabajo para permitir que las llamadas http se conecten a través del proxy. NPR-20529

#### Formularios HTML5  {#html-forms-4}

* Se añadió la compatibilidad con el evento preSubmit. NPR-20604

### Instalador JEE de Forms  {#forms-jee-installer-10}

#### Administración de procesos {#process-management-3}

* Las fichas de datos adjuntos, notas y detalles del flujo de trabajo no funcionan en el espacio de trabajo cuando el formulario se maximiza/minimiza y se guarda como borrador o se reenvía. NPR-20243
* El campo de texto multilínea (TextArea) no conserva el carácter de nueva línea ni el salto de texto después de enviar datos en el espacio de trabajo HTML. NPR-20085

#### Informes de procesos  {#process-reporting}

* Los informes de procesos no recuperan los datos correctamente debido a la excepción de puntero nulo. NPR-19759

>[!NOTE]
>
>Instalar el paquete incrustado de LiveCycle que aparece en el artículo [Versiones de AEM Forms](aem-forms-releases.md) para solucionar el problema.

#### Servicios estándar  {#standard-services}

* docConvertor no admite el acoplamiento de transparencias en PDF y no puede producir un PDF/A. NPR-16228: revisión para CQ-4214488

#### Núcleo  {#core-2}

* Cuando se detiene el servidor de AEM Forms que se ejecuta en una configuración de clúster en la aplicación JBoss, el servidor de aplicaciones se desconecta de la base de datos. Puede provocar problemas de corrupción de datos. NPR-19724

### Paquetes de funciones incluidos  {#feature-packs-included-1}

* El campo de esquema de metadatos desplegable no se puede hacer obligatorio porque falta la validación de campo obligatoria para los recursos. NPR-17882: FP para CQ-4208373

### Los paquetes OSGI y los paquetes de contenido están incluidos en la versión 6.3.1.1.  {#osgi-bundles-and-content-packages-included-in-7}

Lista de paquetes OSGi incluidos en AEM CFP 6.3.1.1

[Obtener archivo](assets/do-not-localize/bundle-list.txt)

Lista de paquetes de contenido incluidos en AEM CFP 6.3.1.1

[Obtener archivo](assets/do-not-localize/content-package-list.txt)

El paquete de correcciones acumulativas 6.3.0.2 de AEM es una actualización importante que incluye varias correcciones internas y de cliente desde la publicación general de AEM 6.3 en abril de 2017.

Los aspectos destacados del paquete de correcciones acumulativas de AEM son:

* La auditabilidad del control de acceso de los usuarios
* incluye la versión 1.6.2 del repositorio integrado (Apache Jackrabbit Oak)
* Se han resuelto los problemas de resolución de recursos sin cerrar
* Configuración simplificada para servicios de contenido inteligente
* Problemas resueltos de validación de fragmentos de contenido
* Se ha mejorado la capacidad de edición de los esquemas de metadatos en dispositivos híbridos
* Se han resuelto los problemas de sincronización a nivel de componente en las copias en directo
* Uso mejorado de las páginas con mucho contenido en la vista de columna
* Compatibilidad mejorada con la convención de asignación de nombres a páginas para páginas con títulos largos
* Experiencia de personalización de campañas mejorada en la IU táctil
* Correcciones de varios problemas de superposición de proyectos

### Plataforma  {#platform-5}

* Revisión para Oak 1.6.2. NPR-16993
* Al abrir la búsqueda de contenido mediante un filtro, la ruta ya no está configurada. NPR-17398: revisión para CQ-4204870
* Requisito de auditabilidad de los cambios de permisos de usuario en AEM. NPR-17061
* Las conexiones de vinculación a los servicios en la nube de DM causan excepciones de “demasiados archivos abiertos”. CQ-4211407

### Recursos {#assets-12}

* Problemas de uso con la configuración de servicios de contenido inteligente mediante distintas opciones. NPR-18200: revisión para CQ-4201557
* Fuga de recursos en flujos binarios al almacén de datos S3. NPR-18041: revisión para CQ-4209506
* Se produce un error cuando se carga un archivo de texto codificado ASCII/UTF-8 en AEM Assets y falla la generación de miniaturas. NPR-18006: CFP para CQ-4209345
* El esquema de metadatos predeterminado provoca un error en la validación de fragmentos de contenido. NPR-17769: revisión para CQ-4211111
* Resolución de recursos sin cerrar en com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner. NPR-17598: CFP para CQ-4209018
* Solicite la creación de varios agentes de replicación para publicar recursos en Brand Portal. NPR-17189
* La tarea de revisión de recursos en la carpeta de idioma japonés no funciona. CQ-4204782
* La excepción de puntero nulo se produce cuando un recurso se mueve de su página de propiedades. CQ-4204251
* AEM no realiza el seguimiento de las referencias posteriores a un recurso en la página de propiedades si está vinculado a un documento de InDesign varias veces. CQ-4204186
* Problemas con la adición de nuevas pestañas en el formulario de esquema de metadatos cuando se edita en Chrome en dispositivos híbridos. CQ-4201810
* Cuando se cargan los recursos duplicados, la opción (eliminar/mantener) se aplica a todos los recursos aunque no esté seleccionada en el cuadro de diálogo detectado de duplicados. CQ-4201673
* Se genera una excepción de puntero nulo cuando se mueve una carpeta de recursos con más de 150 referencias entrantes. CQ-4200981
* Para una carpeta de recursos descargada, si se produce un conflicto al extraer el contenido del archivo ZIP, la opción predeterminada aparece como Crear versión en lugar de Mantener ambos. CQ-97800
* Los usuarios con permisos de solo lectura para la aplicación no pueden obtener una vista previa del contenido de la gestión de contenido de AEM Mobile. NPR-17486: CFP para CQ-4209690
* El botón Crear catálogo no funciona en la vista de columna de la consola Catálogo. CQ-4209952

### Sitios {#sites-12}

* Problemas con la incrustación de componentes de imagen/vídeo mediante el atributo data-sly-resource. NPR-18182: CFP para CQ-4212100
* Se han modificado los componentes localizados que no se restauran a su formulario original cuando se vuelve a aplicar la herencia en LiveCopy. NPR-18172: revisión para CQ-4211379
* Problemas con la navegación en una página con mucho contenido en la vista de columna en la IU táctil. NPR-17799: revisión para CQ-4199611
* Resolución de recursos sin cerrar en `com.day.cq.wcm.core.impl.VersionManagerImpl`. NPR-17789: CFP para CQ-4211152
* El nombre de la página no se genera según la convención para títulos de página largos. NPR-17633: revisión para CQ-4209056
* Problemas con la creación de páginas en la IU táctil en AEM 6.3 implementada en Jjefe EAP 6.4. NPR-17589: revisión de CQ-4210137
* El proveedor de estado de flujo de trabajo hace que la instancia se bloquee cuando hay grupos anidados. NPR-17556: solicitud de CFP para CQ-4202056
* Resolución de recursos sin cerrar en los siguientes objetos:

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497: CFP para CQ-4208673
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495: CFP para CQ-4208668
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494: CFP para CQ-4208669
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493: CFP para GRANITE-17404

### Integraciones {#integrations-1}

* Se han resuelto los errores de componentes de AEM Search que se pueden producir cuando el OSGI de AEM Day HTTP Client 3.1 se configura con un proxy que requiere autenticación implícita. NPR18128: revisión para NPR-18029
* Problemas con la personalización de campañas y experiencias asociadas mediante la IU clásica. NPR-18127: revisión para CQ-4211559
* Al configurar una marca o zona en una página raíz de un sitio, la herencia cancelada no se puede restaurar para las áreas de las subpáginas. NPR-17753: revisión para CQ-4210139

### Flujo de trabajo {#workflow-3}

* En un flujo de trabajo no transitorio, el historial de procesos y los cambios de metadatos realizados antes de un paso de proceso externo no se mantienen. NPR-17848: revisión para GRANITE-17757
* Los valores de los campos de diálogo de flujo de trabajo no persisten en el nodo del elemento de trabajo. NPR-17734: revisión para CQ-4210369
* Se produce un error de fecha incomparable al editar una tarea desde la bandeja de entrada. CQ-4208749

### Proyectos {#projects-3}

* Correcciones de varios problemas de superposición de proyectos NPR-17733
* La reestructuración de los pods en el módulo de proyectos hace que sea menos configurable. CQ-4209859
* La ruta de los recursos cambia a los sitios localizados respectivos cuando se agregan páginas al trabajo de traducción. CQ-4206007

### Seguridad {#security-1}

* Problemas con la carga de imágenes de avatar para usuarios LDAP. NPR-16561
* Solicite utilizar una versión actualizada del servlet org.apache.sling.servlets.post (2.3.22) en la API de Apache Sling para evitar una vulnerabilidad XSS. NPR-18963

## Forms {#forms-12}

Las correcciones de AEM Forms se entregan mediante paquetes de complementos de formularios y otros instaladores de parches que se proporcionan con la versión. Para obtener más información, consulte [AEM Forms Release](aem-forms-releases.md).

Los aspectos destacados de AEM Forms son:

* Las correcciones en los módulos de texto de administración de correspondencia, las vistas previas de las cartas y la interfaz de administración programada de creaciones de correspondencia.
* Correcciones para la validación de PDF/A-1b, conversión de archivos de imagen grandes a PDF y documentos PDF en japonés en PDF Generator.
* Correcciones de uso para administración de correspondencia, seguridad de documentos y flujo de trabajo de formularios.
* Se agregó la compatibilidad para capturar eventos de auditoría para el campo de firma de anotaciones.

### Paquete de complemento de Forms {#forms-add-on-package-12}

**Administración de correspondencia**

* Al editar un fragmento de gestión de correspondencia, el editor de texto muestra las condiciones en línea junto con el texto procesado. CQ-4211930
* Al crear una carta de administración de correspondencia, no se guarda la descripción de la carta. NPR-18089
* Los márgenes adicionales por encima y por debajo de una lista con viñetas están visibles en el editor de texto, pero no en la representación HTML y PDF. NPR-18126
* Cuando el envío HTML utiliza el método POST, la interfaz de usuario de creación de correspondencia no se puede iniciar. NPR-18202
* Cuando se guarda un módulo de texto y una expresión del módulo de texto no contiene etiquetas de expresión de apertura o de cierre, no se muestra ningún mensaje de error. El módulo de texto muestra un mensaje de error y no se procesa en la carta. NPR-18535
* Cuando se agrega contenido nuevo o se pulsa la tecla Intro, se agrega una etiqueta div al módulo de texto. NPR-18240

**Ensamblador**

* Al validar un documento PDF para que sea compatible con PDF/A-1b, AEM Forms devuelve un error de validación: PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED. El documento PDF no devuelve el error cuando se valida con Adobe Preflight y con software de terceros. NPR-18011
* Al validar documentos PDF para cumplir con PDF/A-1b, AEM Forms devuelve un error de validación: El campo del formulario tiene varias apariencias. Los documentos PDF son compatibles con PDF/A-1b. NPR-18013

**Carpeta de inspección**

* Al seleccionar el tratamiento de archivos mediante un flujo de trabajo cuando se crea una carpeta de inspección, la lista desplegable de selección de modelos de flujo de trabajo aparece truncada. NPR-17566

**HTML5 Forms**

* AEM Forms no captura eventos de auditoría para el campo de firma de anotaciones. NPR-15286

**Administrador de formularios**

* La interfaz de usuario de AEM Forms muestra todos los recursos por orden de antigüedad. Los usuarios no pueden alterar el orden para colocar los recursos más recientes primero. NPR-18450

**Referencia de API de Java**

Se ha añadido JavaDocs para la clase com.adobe.livecycle.content. NPR-18468

### Instalador JEE de Forms  {#forms-jee-installer-11}

**Generador de PDF**

* El servicio Generador de PDF no puede convertir imágenes de más de 100 MB en documentos PDF. Ref# CQ-4208628
* Al utilizar el servicio de Generador de PDF con un OCR en japonés, se crea un PDF invertido. NPR-17602

**Administración de procesos**

* La variable TaskContext no se rellena para los procesos de AEM Forms. NPR-18199

**:Seguridad de los documentos**

* Microsoft Excel y Microsoft PowerPoint tardan mucho más en abrir los documentos protegidos con la extensión de seguridad de documentos de AEM para Microsoft Office. CQ-4212358
* Cuando se crea una directiva nueva y una directiva con el mismo nombre que la existente, se produce un error interno del servidor. NPR-18247

## Paquetes de funciones incluidos  {#feature-packs-included-2}

* Requisito de auditabilidad de los cambios de permisos de usuario en AEM. NPR-17061

AEM Cumulative Fix Pack 6.3.0.1 es una actualización importante que incluye varias correcciones internas y de cliente desde la disponibilidad general de AEM 6.3 en abril de 2017. Los aspectos más destacados del AEM Cumulative Fix Pack son:

* Mejoras en la siguiente área:

   * Componentes de Fragmentos de contenido, Sitios y Editor de texto enriquecido, Editor de reglas y Editor de plantillas
   * Social Review e inicio de sesión en Facebook Social
   * Configuración e inicio de trabajos de traducción
   * Tiempo de respuesta para acceder a las notificaciones en las comunidades sociales
   * Visualización de tareas de revisión en el repositorio DAM

* Proporciona una opción de validación en el Administrador de paquetes para detectar conflictos entre superposiciones y CFP

## Descargar instrucciones para CFP mediante distribución de software {#download-instructions-for-cfp-via-package-share}

Puede descargar el paquete CFP directamente desde [Distribución de software](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8) o realizar los siguientes pasos:

1. Abra [Distribución de software](https://experience.adobe.com/downloads). Necesita un Adobe ID para iniciar sesión en la distribución de software.
1. Toque **[!UICONTROL Adobe Experience Manager]** disponible en el menú del encabezado.
1. Toque el nombre del paquete, seleccione **[!UICONTROL Aceptar términos del EULA]** y toque **[!UICONTROL Descargar]**.

## Instrucciones de instalación {#installation-instructions}

Esta sección es una guía de los requisitos y pasos para instalar el CFP.

### Antes de realizar la instalación  {#before-you-install}

>[!NOTE]
>
>Los paquetes de funciones opcionales proporcionados por Adobe dependen de la versión de la versión y del paquete de correcciones acumulativas. Si tiene instalado algún paquete de funciones, póngase en contacto con el [equipo de atención al cliente de AEM](https://helpx.adobe.com/es/marketing-cloud/contact-support.html) para validar la compatibilidad con este paquete de correcciones acumulativas para AEM 6.3.

>[!NOTE]
>
>Se recomienda ejecutar la validación en todos los paquetes de instalación nuevos antes de intentar instalar el paquete. La prevalidación analiza e informa de los errores encontrados antes de la instalación y avisa a los usuarios de dichos errores de forma proactiva.
>
>Puede acceder a la documentación de la opción Validar en [https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* AEM 6.3.3.0 es un requisito previo para el CFP. Visite la [documentación de actualización](https://docs.adobe.com/docs/es/aem/6-3/deploy/upgrade.html) para obtener instrucciones detalladas sobre cómo actualizar una instalación de AEM a AEM 6.3.
* Para una implementación de clúster mediante RDBMK o MongoDB, el paquete CFP se puede instalar en cualquiera de las instancias de creación que utilice el Administrador de paquetes.
* Antes de instalar el paquete de correcciones acumulativas, asegúrese de realizar una instantánea o una copia de seguridad de su instancia de AEM.
* No se admite la desinstalación de CFP.

### Adición de nuevos registros  {#adding-new-loggers}

Para configurar el registro de nivel de depuración y recuperar un registro de actividad durante la instalación de SP/CFP, puede seguir estos pasos:

* Puede agregar un nuevo registrador en la ubicación predeterminada [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) con las siguientes propiedades:

   * Nivel de registro: Depurar
   * Aditivo: falso
   * Archivo de registro: logs/activity.log
   * Registrador: org.apache.jackrabbit.vault.packl.ActivityLog

Actividad.log se creará en   crx -quickstart /logs.

### Instale el paquete de correcciones acumulativas mediante distribución de software {#install-the-cumulative-fix-pack-via-package-share}

Siga estos pasos para instalar el paquete de correcciones acumulativas en una instancia de AEM 6.3 existente:

1. Haga clic en el vínculo [Distribución de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) para descargar el paquete.

1. Abra [Administrador de paquetes](http://localhost:4502/crx/packmgr/index.jsp) y haga clic en **[!UICONTROL Cargar paquete]** para cargar el paquete.

1. Seleccione el nombre del paquete y haga clic en **[!UICONTROL Instalar]**.

### Instalación automática {#automatic-installation}

CFP se puede instalar automáticamente en una instancia en ejecución de las siguientes maneras:

* Coloque el paquete en `../crx-quickstart/install` mientras se ejecuta el servidor. El paquete se instala automáticamente.
* Utilice la [API HTTP del Administrador de paquetes](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/package-manager.html); asegúrese de utilizar `cmd=install&recursive=true` para instalar el paquete anidado.

### Validar la instalación {#validate-installation}

1. La página Información del producto ( `/system/console/  productinfo`) ahora debe mostrar la cadena de versión actualizada &quot;Adobe Experience Manager, versión 6.3.3.8&quot; en Productos instalados.
1. Todos los paquetes OSGI están ACTIVOS o FRAGMENTOS en la consola OSGI (utilice la consola web: `/system/console/bundles`).

>[!NOTE]
>
>Al instalar correctamente el paquete, aparece un mensaje informativo en los registros de errores que indica que el paquete de contenido se ha instalado correctamente, como &quot;Paquete de contenido **AEM-6.3.3-Cumulative-Fix-Pack-7** instalado correctamente&quot;.

>[!NOTE]
>
>Desde AEM 6.3.3.1, el nivel de registro en Jackrabbit FileVault ha cambiado de INFO a DEPURACIÓN para la mayoría de los mensajes. Para obtener los registros de instalación de un paquete de contenido instalado en AEM 6.3.3.1 o superior, habilite el nivel de registro DEBUG para org.apache.jackrabbit.vault.packl.

### Instalación de de AEM Forms {#install-aem-forms}

>[!NOTE]
>
>Omita este paso si no utiliza AEM Forms.

#### Instale los complementos para AEM Forms  {#install-forms}

1. Asegúrese de que ha instalado el paquete CFP de AEM 6.3.3.x.
1. Descargue el paquete adicional de Forms correspondiente en [AEM Forms releases](aem-forms-releases.md) para su sistema operativo.
1. Instale el paquete del complemento de Forms tal como se describe en [Instalación de paquetes del complemento de formularios AEM](https://helpx.adobe.com/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html).

#### Instalación de paquetes JEE de AEM Forms {#install-aem-forms-jee-bundles-package}

Las correcciones en el instalador JEE de AEM Forms se entregan mediante un instalador independiente. Para obtener información sobre la instalación de un CFP en AEM Forms en JEE, consulte [Instalación de CFP en el JEE de AEM Forms](install-cfp-aem-forms-jee.md).

#### Programa de instalación del diseñador Forms Designer  {#designer-installer}

1. Para instalar la actualización, ejecute el archivo Designer 6.2.0_&lt;Language>_Cumulative_QF.msp.
1. En la pantalla de bienvenida, haga clic en **Actualizar**. Se inicia la instalación.
1. Una vez finalizada la instalación, haga clic en **Finalizar**.

## Configuración del JEE de AEM Forms (JBoss EAP)  {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>Si va a instalar las versión 6.3.3.0 o una posterior, inicie el siguiente procedimiento para configurar los ajustes del servidor de aplicaciones JBoss. Si va a instalar 6.3.3.0 en el servidor de AEM Forms que se ejecuta en los servidores de aplicaciones Oracle WebLogic o IBM WebSphere, no se requiere ninguna configuración adicional. Para obtener más información, consulte [AEM 6.3.3.0 Notas de la versión](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

## Actualizaciones de configuración para la integración de Search&amp;Promote {#configuration-updates-for-search-promote-integration}

Con el paquete de correcciones acumulativas 6.3.0.2 de AEM y las versiones posteriores, la configuración OSGi utilizada para la integración de Search&amp;Promote es la **configuración proxy de componentes HTTP de Apache**. Ya no se utiliza la configuración proxy del cliente HTTP 3.1 de Day Commons.

## Problemas conocidos {#known-issues}

* Durante la instalación de AEM CFP 6.3.3.x pueden producirse los siguientes errores y advertencias, que se pueden ignorar sin problemas:

   * *WARN* [OsgiInstallerImpl] org.apache.jackrabbit.vault.package.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallhang-0.0.2-jar-with-dependencias.jar arrojó una excepción de tiempo de ejecución.
   * *ERROR* [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] Tiempo de espera de espera para que el cambio de reg finalice sin registrar. CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver, no se pueden atender las solicitudes y se envía el estado 503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource: no se puede comprobar el recurso [/bin/received], el administrador de páginas no está disponible
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver: La llamada al controlador de error generó un error
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver Error original nulo
   * org.apache.sling.engine.impl.DefaultErrorHandler El controlador de error falló:java.io.IOException
   * *ERROR* [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR (org.osgi.framework.ServiceException: La fábrica de servicios devolvió un valor nulo. (Componente: com.day.cq.dam.handler.standard.ps.PostScriptHandler))

**Brand Portal**

* A partir de la versión 6.3.1.2, se ha eliminado el botón Publicar en Brand Portal para colecciones inteligentes.

**Interfaz de usuario**

>[!NOTE]
>
>Si tiene algún problema, póngase en contacto con el [Servicio de atención al cliente de AEM](https://helpx.adobe.com/marketing-cloud/contact-support.html).

* Se observa un alto uso de la CPU debido a muchas solicitudes en la funcionalidad de búsqueda de administración. NPR-24229
* El campo de la ruta no está seleccionado en la ruta del navegador al volver a abrir el componente. NPR-24177

## Ajustes de configuración necesarios para NPR-27692  {#configuration-settings-required-for-npr}

>[!NOTE]
>
>Esta configuración se aplica a CFP 6.3.3.2 y versiones posteriores. Le indica que actualice las propiedades de delegación de inicio en el archivo `sling` .properties.

Para actualizar manualmente los cambios en adobe-livecycle - cq -author.ear/ cq.war, siga los pasos que se mencionan a continuación:

* Detenga el servidor AEM.
* Vaya a adobe-livecycle-cq-author.ear/cq.war
* Abra adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml para editar:

   * actualice el valor **sling.bootdelegate.ibm** param-name con:

      * com.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * Después del cambio anterior, init-param debería tener el siguiente aspecto:

      * &lt;init-param>\
         &lt;param-name>sling.bootdelegación.&lt;/param-name> &lt;param-value>ibmcom.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* Desinstale el archivo de almacenamiento empresarial (EAR) anterior del servidor de aplicaciones de la esfera web e instale el archivo EAR actualizado siguiendo los pasos de la sección 10.2 de [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
* Guarde el archivo y reinicie el servidor. [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## Ajustes de configuración necesarios para NPR-23208 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>Esta configuración se aplica a 6.3.2.2 y versiones posteriores. Le indica que actualice las directivas de Listas de Control de acceso (ACL) de forma manual a través de CRX-DE, ya que las ACL no se actualizan a través de la instalación de CFP debido a acHandling &quot;merge_preserve&quot;.

**Documentación para agregar políticas de ACL manualmente**

Para actualizar las directivas ACL, agregue los controles de acceso siguientes a través de CRX-DE:

`1)` En la ruta &quot;/content&quot;\
`a)` Principal: reference-Adjustment-service\
Tipo: Permitir\
Privilegios: jcr:read , jcr:modifyProperties\
Restricciones: rep:glob=&quot;/*/jcr:content&quot;\
`b)` Principal: reference-Adjustment-service\
Tipo: Permitir\
Privilegios: jcr:read , jcr:modifyProperties\
Restricciones: rep:glob=&quot;/*/jcr:content/*&quot;

`2)` En la ruta &quot;/content/usergenerate&quot;\
`a)` Principal: reference-Adjustment-service\
Tipo: Permitir\
Privilegios: jcr:write

`3)` En la ruta &quot;/etc.&quot;\
`a)` Principal: reference-Adjustment-service\
Tipo: Permitir\
Privilegios: jcr:read , jcr:modifyProperties\
Restricciones: rep:glob=&quot;/*/jcr:content&quot;\
`b)` Principal: reference-Adjustment-service\
Tipo: Permitir\
Privilegios: jcr:read , jcr:modifyProperties\
Restricciones: rep:glob=&quot;/*/jcr:content/*&quot;

## Ajustes de configuración necesarios para NPR-19450 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>Esta configuración se aplica a CFP 6.3.1.1 y posterior.

**Configure la propiedad CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL.**

La propiedad controla la profundidad máxima del subárbol de nodos bajo el nodo de página ` /  jcr   :content`, hasta la cual los nodos presentes en el repositorio se utilizarán para obtener las propiedades de página. Se ignora cualquier nodo que se encuentre por debajo de la profundidad especificada en esta propiedad.

El valor predeterminado es 1. El valor se puede  se sobrescribe superponiendo las constantes.js del archivo (`/libs/cq/ui/widgets/source/constants.js`) sin comentar la propiedad CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL y asignándole el valor requerido ( la profundidad máxima bajo la propiedad de la página / jcr:content hasta la cual se almacenan los datos de las propiedades de la página).

**Si el usuario necesita crear variantes de varias páginas para que el número de nodos bajo el nodo de contenido / jcr :de la página sea bueno a más de 1000, siga los pasos siguientes para realizar cambios en la configuración:**

* Configure la propiedad JSON Max resultados de Apache Sling
* Obtener servlet mediante `/system/console/  configMgr`
* Establezca su valor en un número >1000 (que es el valor predeterminado actual) de forma que este número sea bueno al número total de nodos en el subárbol / jcr :content hasta la profundidad configurada arriba.

Esto permite que el servlet de GET sling pueda devolver todos los nodos necesarios.

## Uber Jar {#uber-jar}

El Uber Jar para 6.3.3.8 está disponible en [repositorio de Maven público de Adobe](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/).

Para usar Uber Jar en un proyecto de Maven, consulte el artículo, [Cómo usar Uber jar](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/ht-projects-maven.html) e incluya la siguiente dependencia en el POM del proyecto:

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## Funciones eliminadas u obsoletas {#deprecated}

Esta sección enumera las funciones y capacidades que se han eliminado o dejado de utilizar en AEM 6.3.

| Área | Función | Reemplazo | Versión |
|----|-----|-----|-----|
| Integración de Assets y Adobe Creative Cloud | [AEM en el ](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/creative-cloud.html) uso compartido de carpetas de Creative Cloud se introdujo en AEM 6.2 como una forma de proporcionar a los usuarios creativos acceso a los recursos de AEM. Adobe Asset Link, la nueva capacidad de la aplicación Creative Cloud, proporciona experiencia de usuario mejorada y un acceso más eficaz a los recursos de AEM directamente desde Photoshop, InDesign e Illustrator.<br /> Adobe no realizará más mejoras en la funcionalidad de uso compartido de carpetas. Aunque la función se incluye en AEM, se recomienda a los clientes utilizar el remplazo. | Adobe Asset Link o Aplicación de escritorio. Para obtener más información, consulte el artículo sobre la [integración de AEM Creative Cloud](https://helpx.adobe.com/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html). | AEM 6.3.3.x |

## Paquetes de contenido y paquetes OSGi incluidos {#osgi-bundles-and-content-packages-included-1}

Los siguientes documentos de texto enumeran los paquetes OSGi y los paquetes de contenido incluidos en el CFP.

* [Lista de paquetes OSGi incluidos en AEM 6.3.3.8](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [Lista de paquetes de contenido incluidos en AEM 6.3.3.8](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [Versiones y actualizaciones de AEM](https://helpx.adobe.com/es/experience-manager/aem-releases-updates.html)
>* [Página de correcciones de AEM 6.3](https://helpx.adobe.com/es/experience-manager/kb/aem63-available-hotfixes.html)
>* [Notas de la versión de AEM 6.3](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [Página de productos AEM](http://www.adobe.com/es/solutions/web-experience-management.html)
>* [Documentación de AEM 6.3](https://docs.adobe.com/content/docs/en/aem/6-3.html)
>* Suscríbase a [actualizaciones de productos con prioridad de Adobe](https://www.adobe.com/subscription/priority-product-update.html)

