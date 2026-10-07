---
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 3%
---
# Directrices para contribuir a la documentación de Adobe Experience Manager

## Filosofía de documentación

Los usuarios de Adobe Experience Manager trabajan en entornos altamente competitivos y se esfuerzan por crear experiencias digitales que los diferencien de su competencia. Por lo tanto, cuando Adobe introduce nuevas herramientas avanzadas en AEM, proporcionan una documentación precisa y clara. Este enfoque permite a los clientes utilizar inmediatamente su inversión en AEM y maximizar el retorno de la inversión.

El objetivo de la documentación de AEM es poner la documentación en manos de los usuarios de AEM lo antes posible. Por lo tanto, se crea una documentación precisa y útil, que se actualiza y mejora continuamente.

## Contribuciones de documentación

Para mejorar continuamente la documentación de AEM, contamos con la ayuda de toda la comunidad de usuarios de AEM. Ya sea a través de solicitudes de extracción o incidencias, las mejoras en la documentación pueden ser correcciones, aclaraciones, expansiones y más ejemplos.

## Normas de documentación

Adobe agradece las contribuciones a la documentación. Cualquier contribución a la documentación de AEM, ya sea una solicitud de extracción o un problema, debe ajustarse a las normas de contribución y documentación de Adobe.

Las contribuciones que no cumplan estas normas podrán ser rechazadas.

### Adobe escribe sobre casos de uso estándar.

La documentación de AEM abarca estos casos de uso estándar. Los casos de uso que exceden el ámbito de la instalación y el uso estándar del producto no forman parte de la documentación de AEM.

### Adobe no suele documentar errores ni sus soluciones alternativas.

La documentación de AEM abarca estos casos de uso estándar. Por este motivo, los errores, los efectos causados por errores y las soluciones alternativas para los errores no están documentados.

Las excepciones a esta regla se aplican a las notas de la versión, donde los problemas conocidos pueden enumerarse con posibles soluciones que apruebe el equipo de administración del producto de AEM.

### Las contribuciones a la documentación no sirven para responder preguntas técnicas.

Cualquier idea que tenga para mejorar la documentación de AEM es bienvenida como contribución. Sin embargo, los comentarios, problemas y solicitudes de extracción están destinados únicamente a *contribuciones*. No pretenden responder a sus preguntas sobre cómo utilizar AEM, implementar su proyecto de AEM ni solucionar problemas técnicos.

Informe de cualquier pregunta acerca del uso de AEM o de errores técnicos mediante el [Portal de soporte Enterprise de Experience Cloud](https://experienceleague.adobe.com/es/home?support-solution=General#support). O bien, use la [comunidad de Experience Manager](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community?profile.language=es).

***Las contribuciones a la documentación de AEM no sustituyen al servicio de atención al cliente de Adobe*** y se rechaza cualquier contribución de este tipo que busque respuestas a preguntas relacionadas con la asistencia.

### Las contribuciones deben hacer referencia claramente a las páginas de documentación afectadas.

Si crea un problema para sugerir mejoras en la documentación, incluya vínculos a las páginas afectadas. Si crea un problema usando el vínculo **Editar esta página** en una página de documentación, el problema se creará automáticamente con un vínculo a la página.

Este proceso no se aplica a las solicitudes de extracción, ya que las solicitudes de extracción, por su naturaleza, hacen referencia a la página o páginas afectadas.

## Directrices de documentación

Cualquier contribución a la documentación de debe seguir determinadas directrices de estilo.

Seguir estas directrices facilita la revisión de su contribución y, por lo tanto, la integración en la documentación de es más rápida.

### Idioma y estilo

#### Idioma

* La documentación de AEM se redacta y se actualiza en inglés estadounidense (originalmente).
* Utilice frases lo más simples posibles.
* Utilice un lenguaje claro y conciso.

Recuerde, los lectores de la documentación de AEM son de todo el mundo y no se puede esperar que hablen inglés de forma nativa o fluida. Evite los coloquialismos y utilice un lenguaje tan claro y simple como sea posible.

#### Siga el Manual de estilo de Microsoft®

[El Manual de estilo de Microsoft®](https://learn.microsoft.com/en-us/style-guide/welcome/) es una guía de estilo de documentación disponible libremente que se centra en documentación de software y la documentación de AEM sigue esta guía siempre que es posible.

### Formato

| Elemento | Estilo |
|---|---|
| Elemento u opción de la IU | **negrita** |
| Nombre de archivo, ruta, entrada de usuario, valores de parámetro | `monospaced` |
| Código, línea de comandos | ```Code Block``` |

### Capturas de pantalla

Las capturas de pantalla deben utilizarse con prudencia y solo cuando la descripción textual no sea suficiente.

No se deben utilizar marcadores u otras anotaciones en las capturas de pantalla (como marcos rojos, flechas o texto). De este modo, las capturas de pantalla son más fáciles de reutilizar o replicar en versiones localizadas de la documentación.

### Referencias específicas de la versión

Lo ideal es evitar cualquier referencia directa a una versión específica en todo el contenido de la documentación, siempre que sea posible. Este método hace que la documentación sea más flexible y extensible para futuras versiones.

### Uso de Day, AEM, CQ, CRX

Cuando mencione el producto por primera vez en un artículo, use siempre su nombre completo, **Adobe Experience Manager**. Después de eso, puede referirse a él como **AEM**.

No se deben utilizar Día, Software de día, CQ y CRX excepto cuando sea inevitable, como en nombres de clase o en referencia al historial de AEM.