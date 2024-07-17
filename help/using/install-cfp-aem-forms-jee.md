---
title: Instalación de paquetes de correcciones acumulativas en AEM Forms JEE
description: Resumen de los pasos para instalar y configurar el Fix Pack acumulativo (CFP) en AEM Forms JEE.
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: ht
source-wordcount: '905'
ht-degree: 100%

---

# Instalación de paquetes de correcciones acumulativas en AEM [!DNL  Forms] JEE {#installing-cumulative-fix-packs-on-aem-forms-jee}

## Instalación del CFP en AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Para instalar el Fix Pack acumulativo en AEM 6.3 [!DNL Forms JEE], realice la siguiente secuencia de pasos.

1. Para obtener el programa de instalación de AEM 6.3 [!DNL Forms JEE] para CFP, póngase en contacto con [Soporte de Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home&amp;lang=es#support).
1. Ejecute el instalador del CFP y configure AEM [!DNL Forms JEE] como se describe en [Instalar y configurar AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Instale el último CFP de AEM 6.3.3.x
1. Instale el paquete de complemento de [!DNL Forms] para el CFP de AEM [6.3.3.x](aem-forms-releases.md)

### Instale los paquetes de AEM [!DNL Forms JEE] {#install-aem-forms-jee-bundles-package}

El paquete de AEM [!DNL  Forms JEE] (aemfd-jee-bundles-package-6.3CFP1; versión 1.0.2) proporciona al usuario de [!DNL Forms] en AEM [!DNL Forms JEE] los mismos derechos y funcionalidades que en AEM [!DNL Forms OSGi]. Compruebe los paquetes instalados en el Administrador de paquetes e instale el paquete si aún no está instalado.

### Más instrucciones para CQ-4208044 {#additional-instructions-for-cq}

Si utiliza el servidor AEM 6.3 [!DNL Forms JEE] con base de datos de Oracle, configure las siguientes opciones después de la implementación del CFP1, es decir, después de ejecutar el Administrador de configuración. Esta configuración es necesaria para sincronizar usuarios, grupos y abonados del grupo cuando se ejecuta la sincronización de dominios de empresa.

1. Inicie sesión en la IU de **Administración**.
1. Vaya a **[!UICONTROL Settings]** > **[!UICONTROL User Management]** > **[!UICONTROL Configuration]** > **[!UICONTROL Import and Export Configuration File]**
1. Exporte el archivo config.xml.
1. Modifique la entrada para “`groupMemberDBQueryBatchSize`” en las configuraciones de dominio en *config.xml*. Entrada de muestra:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. Vuelva a importar el archivo modificado y, a continuación, vuelva a ejecutar la sincronización.

## Instalación del CFP en AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Para instalar el Fix Pack acumulativo en AEM 6.2 [!DNL Forms JEE], realice la siguiente secuencia de pasos.

1. Para obtener el programa de instalación de AEM 6.2 [!DNL Forms JEE] para CFP, póngase en contacto con [Soporte de Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home&amp;lang=es#support).
1. Ejecute el instalador del CFP y configure AEM [!DNL Forms JEE] como se describe en [Instalar y configurar AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Instale la revisión 12785 de AEM versión 7.0.
1. Instale el paquete de servicio 1 de AEM 6.2.
1. Instale la última versión -notes-aem-6-2-cumulative-fix-pack.md.
1. Instale el paquete de complemento de [!DNL Forms] para el CFP del paquete de servicio 1 de AEM 6.2.

### Instale los paquetes de AEM [!DNL Forms JEE] {#install-aem-forms-jee-bundles-package-1}

El paquete AEM Forms JEE (aemfd-jee-bundles-package-6.2CFP5; versión 1.0.2) proporciona al usuario de [!DNL Forms] en AEM [!DNL Forms JEE] los mismos derechos y funcionalidades que en AEM [!DNL Forms OSGi]. Compruebe los paquetes instalados en el Administrador de paquetes e instale el paquete si aún no está instalado.

### Configuración del tiempo de espera para operaciones en el nivel de componente (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Después del CFP4 de AEM 6.2, puede utilizar las siguientes instrucciones para configurar el tiempo de espera de las operaciones de DSC en caso de que tenga problemas debido al tiempo de espera durante el proceso de actualización.

La implementación de DSC tarda un tiempo variable debido al cual puede fallar. Para cambiar el tiempo de espera de las operaciones de DSC como Instalar, Cargar, Iniciar y Detener, debe configurar `adobe.component.registry.timeout` mediante el argumento JVM con la opción -D.

Especifique el valor de la clave en segundos. Por ejemplo: `-Dadobe.component.registry.timeout=300`

También puede cambiar los tiempos de espera en el nivel de componente utilizando las siguientes tres propiedades:

1. `adobe.all-component.timeout`: sobrescribe los tiempos de espera de todos los servicios del producto.
1. `adobe.<serviceName>.timeout`: sobrescribe el tiempo de espera solo para el servicio (&lt;serviceName>) mencionado en la clave. Si se establece el valor en el nivel de servicio, el uso de este comando solo sobrescribe el valor de tiempo de espera del servicio especificado si se establece en el nivel de aplicación.
1. `adobe.<serviceName>.<operationName>.timeout`: solo sobrescribe el tiempo de espera para la operación del servicio específico(&lt;serviceName>.&lt;operationName>) mencionado en la clave. Si el valor se establece en el nivel Operación, el uso de este comando solo sobrescribe el valor de tiempo de espera del servicio especificado si se establece en el nivel de aplicación o nivel de servicio.

**Ejemplos:**

Utilice los siguientes comandos para establecer el tiempo de espera en el nivel de componente:

1. Para establecer el tiempo de espera de todas las operaciones de servicio en 600 segundos:

   conjunto “`JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`”

1. Para establecer el tiempo de espera de los valores de operación `DesigntimeService` en 500 segundos, utilice lo siguiente:

   conjunto “`JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`”

1. Para establecer el tiempo de espera de los valores de operación `DesigntimeService's previewLCA` en 700 segundos, utilice lo siguiente:

   conjunto “`JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`”

1. Para establecer `DSC operations`, como carga e instalación, en 600 segundos, utilice lo siguiente:

   conjunto “`JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`”

## Instalación y configuración de AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Realice una copia de seguridad de la carpeta /deploy. Es necesaria si decide desinstalar la corrección rápida.
1. Detenga el servidor de aplicaciones.
1. Extraiga el archivo del programa de instalación del parche en el disco duro.
1. En el directorio denominado según el sistema operativo que esté utilizando:

   **Windows**

   Vaya al directorio correspondiente del medio de instalación o a la carpeta del disco duro donde copió el programa de instalación.

   * (`Windows 32-bit`): `Disk1\InstData\Windows\VM`
   * (`Windows 64-bit`): `Disk1\InstData\Windows_64bit\VM`

   A continuación, haga doble clic en el archivo denominado:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux®, Solaris™, AIX®**

   Vaya al directorio adecuado:

   * (Linux®): Disk1/InstData/Linux/NoVM
   * (Solaris™): Disk1/InstData/Solaris/NoVM
   * (AIX®): Disk1/InstData/AIX/VM

   Desde un símbolo del sistema, escriba:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Se inicia el asistente de instalación para guiarle a través de la instalación.

1. En el panel Introducción, haga clic en **[!UICONTROL Siguiente]**.
1. En la pantalla Elegir carpeta de instalación, compruebe que la ubicación predeterminada que se muestra es correcta para la instalación existente. También puede hacer clic en **[!UICONTROL Examinar]** para seleccionar la carpeta alternativa en la que AEM [!DNL Forms] está instalado y, luego, hacer clic en **[!UICONTROL Siguiente]**.
1. Lea la información de resumen de parches de corrección rápida y haga clic en **[!UICONTROL Siguiente]**.
1. Lea la información del resumen previo a la instalación y haga clic en **[!UICONTROL Instalar]**.
1. Una vez finalizada la instalación, haga clic en **[!UICONTROL Siguiente]** para aplicar las actualizaciones de correcciones rápidas a los archivos instalados.
1. La casilla de verificación de Inicio del Administrador de configuración está seleccionada de forma predeterminada. Haga clic en **[!UICONTROL Listo]** para ejecutar el Administrador de configuración.

   Para ejecutar el Administrador de configuración más adelante, anule la selección de la opción **[!UICONTROL Inicio del Administrador de configuración]** antes de hacer clic en **[!UICONTROL Listo]**. Puede iniciar el Administrador de configuración más adelante utilizando el script adecuado en el directorio *`[AEM_forms_root]`/configurationManager/bin*.

1. Según el servidor de aplicaciones, elija uno de los siguientes documentos y siga las instrucciones de la sección *Configuración e implementación de AEM [!DNL Forms]*.

   Para AEM [!DNL Forms] 6.3, consulte:

   * Instalación e implementación de AEM [!DNL Forms] para JBoss®
   * Instalación e implementación de AEM [!DNL Forms] para WebSphere®
   * Instalación e implementación de AEM [!DNL Forms] para WebLogic

1. Reinicie AEM [!DNL Forms] servidor JEE.
