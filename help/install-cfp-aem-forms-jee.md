---
title: Instalación de paquetes de correcciones acumuladas en AEM Forms JEE
description: Resumen de los pasos para instalar y configurar Cumulative Fix Pack (CFP) en AEM Forms JEE
contentOwner: AK
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 1%

---


# Instalación de paquetes de correcciones acumuladas en AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## Instalar CFP en AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Realice los siguientes pasos, en la secuencia especificada, para instalar el paquete de correcciones acumulativas en la AEM 6.3 [!DNL Forms JEE].

1. Póngase en contacto con [Soporte técnico de Adobe](https://www.adobe.com/account/sign-in.supportportal.html) para obtener el instalador AEM 6.3 [!DNL Forms JEE] para CFP.
1. Ejecute el instalador de CFP y configure AEM [!DNL Forms JEE] como se describe en [Instalar y configurar AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Instale la última AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. Instale el paquete Añadido [!DNL Forms] para AEM CFP [6.3.3.x](aem-forms-releases.md)

### Instalar el paquete de paquetes de AEM [!DNL Forms JEE] {#install-aem-forms-jee-bundles-package} paquetes de paquetes

[[!DNL  Forms JEE] AEMpackage](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-buncles-package-6.3CFP1; versión 1.0.2) proporciona al  [!DNL Forms] usuario AEM  [!DNL Forms JEE] los mismos derechos y capacidades que en AEM  [!DNL Forms OSGi]. Compruebe los paquetes instalados en el Administrador de paquetes e instale el paquete si aún no está instalado.

### Instrucciones adicionales para CQ-4208044 {#additional-instructions-for-cq}

Si utiliza AEM servidor 6.3 [!DNL Forms JEE] con la base de datos de Oracle, configure las siguientes opciones después de la implementación de CFP1, es decir, después de ejecutar Configuration Manager. Esta configuración es necesaria para sincronizar usuarios, grupos y miembros del grupo cuando se ejecuta la sincronización de dominios de empresa. Consulte el problema CQ-4208044 en [AEM notas de la versión 6.3](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205).

1. Inicie sesión en la interfaz de usuario **Administración**.
1. Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Administración de usuarios]** > **[!UICONTROL Configuración]** > **[!UICONTROL Importar y exportar archivo de configuración]**
1. Exporte el archivo config.xml.
1. Modifique la entrada para &quot; `groupMemberDBQueryBatchSize`&quot; en las configuraciones de dominio en *config.xml*. Entrada de muestra:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. Vuelva a importar el archivo modificado y, a continuación, vuelva a ejecutar la sincronización.

## Instalar CFP en AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Realice los siguientes pasos, en la secuencia especificada, para instalar el paquete de correcciones acumulativas en la AEM 6.2 [!DNL Forms JEE].

>[!NOTE]
>
>Si está en AEM 6.2 [!DNL Forms OSGi], siga las instrucciones de instalación que se encuentran en [AEM notas de la versión de CFP 6.2.](release-notes-aem-6-2-cumulative-fix-pack.md)

1. Póngase en contacto con [Soporte técnico de Adobe](https://www.adobe.com/account/sign-in.supportportal.html) para obtener el instalador AEM 6.2 [!DNL Forms JEE] para CFP.
1. Ejecute el instalador de CFP y configure AEM [!DNL Forms JEE] como se describe en [Instalar y configurar AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Instale [AEM revisión 12785 versión 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785).
1. Instale [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).
1. Instale la última [AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md).
1. Instale el paquete Añadido [!DNL Forms] para [AEM 6.2 Service Pack 1 CFP](aem-forms-releases.md).

### Instalar el paquete de paquetes de AEM [!DNL Forms JEE] {#install-aem-forms-jee-bundles-package-1} paquetes de paquetes

[Paquete](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24)  AEM Forms JEE(aemfd-jee-buncles-package-6.2CFP5; versión 1.0.2) proporciona al  [!DNL Forms] usuario AEM  [!DNL Forms JEE] los mismos derechos y capacidades que en AEM  [!DNL Forms OSGi]. Compruebe los paquetes instalados en el Administrador de paquetes e instale el paquete si aún no está instalado.

### Configuración del tiempo de espera para operaciones a nivel de componente (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Después de AEM 6.2 CFP4, puede utilizar las siguientes instrucciones para configurar el tiempo de espera de las operaciones de DSC en caso de que tenga problemas debido al tiempo de espera durante el proceso de actualización. (Consulte NPR-16774 en [AEM notas de la versión 6.2 CFP4](release-notes-aem-6-2-cumulative-fix-pack.md)).

La implementación de DSC tarda un tiempo variable debido al cual puede fallar. Para cambiar el tiempo de espera de las operaciones de DSC como Instalar, Cargar, Inicio y Detener, debe configurar el `adobe.component.registry.timeout` mediante el argumento JVM con la opción -D.

Especifique el valor de la clave en segundos. Por ejemplo: `-Dadobe.component.registry.timeout=300`

También puede cambiar los tiempos de espera en el nivel de componente con las tres propiedades siguientes:

1. `adobe.all-component.timeout`:: sobrescribe los tiempos de espera de todos los servicios del producto.
1. `adobe.<serviceName>.timeout`:: sobrescribe el tiempo de espera solo para el servicio (&lt;servicename>) mencionado en la clave. Si se establece el valor en el nivel de servicio, el uso de este comando solo sobrescribe el valor de tiempo de espera del servicio especificado si se establece en el nivel de aplicación.
1. `adobe.<serviceName>.<operationName>.timeout`:: Solo sobrescribe el tiempo de espera para la operación del servicio específico(&lt;servicename>.&lt;operationname>) en la clave. Si el valor se establece en el nivel Operación, el uso de este comando solo sobrescribe el valor de tiempo de espera del servicio especificado si se establece en el nivel de aplicación o de servicio.

**Ejemplos:**

Utilice los siguientes comandos para establecer el tiempo de espera en el nivel de componente:

1. Para establecer el tiempo de espera de todas las operaciones de servicio en 600 segundos:

   configurar &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Para establecer el tiempo de espera de los valores de operación `DesigntimeService` en 500 segundos, utilice:

   configurar &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Para establecer el tiempo de espera de los valores de operación `DesigntimeService's previewLCA` en 700 segundos, utilice:

   configurar `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Para establecer el `DSC operations` como carga, instalación, etc. en 600 segundos, utilice:

   configurar &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## Instalar y configurar AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Realice una copia de seguridad de la carpeta /deploy. Es necesario si decide desinstalar la corrección rápida.
1. Detenga el servidor de aplicaciones.
1. Extraiga el archivo de archivo del instalador de parches en el disco duro.
1. En el directorio denominado según el sistema operativo que esté utilizando:

   **Windows**

   Vaya al directorio correspondiente del medio de instalación o la carpeta del disco duro donde copió el instalador:

   * (Windows de 32 bits): Disk1\InstData\Windows\VM
   * (Windows de 64 bits): Disk1\InstData\Windows_64bit\VM

   A continuación, haga clic con el doble en el archivo denominado:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux, Solaris, AIX**

   Vaya al directorio correspondiente:

   * (Linux): Disk1/InstData/Linux/ NoVM
   * (Solaris): Disk1/InstData/Solaris/ NoVM
   * (AIX): Disk1/InstData/AIX/VM

   Desde un símbolo del sistema, escriba:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Esto inicia un asistente de instalación que lo guiará a través de la instalación.

1. En el panel Introducción, haga clic en **[!UICONTROL Siguiente]**.
1. En la pantalla Elegir carpeta de instalación, verifique que la ubicación predeterminada que se muestra es correcta para la instalación existente o haga clic en **[!UICONTROL Examinar]** para seleccionar la carpeta alternativa en la que AEM [!DNL Forms] está instalado actualmente y haga clic en **[!UICONTROL Siguiente]**.
1. Lea la información de Resumen de parches de Corrección rápida y haga clic en **[!UICONTROL Siguiente]**.
1. Lea la información del resumen previo a la instalación y haga clic en **[!UICONTROL Instalar]**.
1. Una vez finalizada la instalación, haga clic en **[!UICONTROL Siguiente]** para aplicar las actualizaciones de correcciones rápidas a los archivos instalados.
1. La casilla de verificación Administrador de configuración de Inicio está seleccionada de forma predeterminada. Haga clic en **[!UICONTROL Listo]** para ejecutar Configuration Manager.

   Para ejecutar Configuration Manager más adelante, anule la selección de la opción **[!UICONTROL Administrador de configuración de Inicio]** antes de hacer clic en **[!UICONTROL Listo]**. Puede inicio Configuration Manager más adelante utilizando la secuencia de comandos adecuada en el directorio *`[AEM_forms_root]`/configurationManager/bin*.

1. Según el servidor de aplicaciones, elija uno de los siguientes documentos y siga las instrucciones de la sección *Configuración e implementación de AEM[!DNL Forms]*.

   Para AEM [!DNL Forms] 6.3, consulte:

   * [Instalación e implementación de  [!DNL Forms] AEM para JBoss](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [Instalación e implementación de  [!DNL Forms] AEM para WebSphere](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [Instalación e implementación de  [!DNL Forms] AEMfor WebLogic](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   Para AEM [!DNL Forms] 6.2, consulte:

   * [Instalación e implementación de  [!DNL Forms] AEM para JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62)
   * [Instalación e implementación de  [!DNL Forms] AEM para WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62)
   * [Instalación e implementación de  [!DNL Forms] AEMfor WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62)

   Para AEM Forms 6.1, consulte:

   * [Instalación e implementación de  [!DNL Forms] AEM para JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [Instalación e implementación de  [!DNL Forms] AEM para WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [Instalación e implementación de  [!DNL Forms] AEMfor WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. Reinicie AEM [!DNL Forms] servidor JEE.
