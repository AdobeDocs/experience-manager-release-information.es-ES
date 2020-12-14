---
source-git-commit: 65c8c0b9940f9d2e20234ccc65b1d819971ea52e
workflow-type: tm+mt
translation-type: tm+mt
source-wordcount: '752'
ht-degree: 5%

---
# Directrices para contribuir a la documentación de Adobe Experience Manager

## Filosofía de la documentación

Sabemos que los usuarios de Adobe Experience Manager están trabajando en entornos altamente competitivos, esforzándose por crear experiencias digitales que los diferencien de sus competidoras. Por lo tanto, es vital que cuando Adobe ofrece nuevas herramientas avanzadas en AEM, estas herramientas se complementen con una documentación precisa y clara que permita al cliente aprovechar inmediatamente su inversión AEM y maximizar el ROI.

El objetivo de la documentación AEM es poner la documentación en manos de los usuarios AEM lo antes posible. Por lo tanto, damos prioridad a la documentación precisa y utilizable y nos esforzamos por actualizarla y mejorarla continuamente.

## Contribuciones a la documentación

Para mejorar continuamente la documentación de AEM, es conveniente que toda la comunidad de usuarios AEM contribuya a la documentación. Ya sea a través de solicitudes o problemas, las mejoras en la documentación pueden ser correcciones, aclaraciones, expansiones y ejemplos adicionales.

## Normas de documentación

Si bien acogemos con beneplácito las contribuciones a nuestra documentación, toda contribución a la documentación de AEM, ya sea en forma de solicitud de retirada o de un problema, debe ajustarse a nuestras normas de contribución y documentación.

Las contribuciones que no cumplan estas normas podrán rechazarse.

### Documento casos de uso estándar.

AEM documentación abarca casos de uso estándar. Los casos de uso que exceden el ámbito de la instalación estándar y el uso del producto no forman parte de AEM documentación.

### Generalmente no se documento errores ni sus soluciones alternativas.

AEM documentación abarca casos de uso estándar. Por este motivo, los errores, los efectos causados por errores y las soluciones alternativas para los errores generalmente no están documentados.

Las excepciones a esta regla se aplican a las notas de la versión, donde los problemas conocidos pueden enumerarse con posibles soluciones aprobadas por AEM Administración de productos.

### Las contribuciones de documentación no sirven para responder preguntas técnicas.

Cualquier idea que tenga para mejorar la documentación de AEM es bienvenida como contribución. Sin embargo, los comentarios, los problemas y las solicitudes de extracción están destinados únicamente a *contribuciones*. No están pensados para utilizarse para responder a sus preguntas sobre cómo utilizar AEM, implementar su proyecto AEM o resolver problemas técnicos.

Cualquier pregunta sobre el uso de AEM o errores técnicos que pueda tener debe informarse a través del proceso de soporte normal a través del [portal de soporte empresarial de Experience Cloud](https://helpx.adobe.com/es/contact/enterprise-support.ec.html) o analizarse en la [comunidad de Experience Manager](https://forums.adobe.com/community/experience-cloud/marketing-cloud/experience-manager).

***AEM las contribuciones de documentación no sustituyen a la*** carrera de Adobe para los clientes, y cualquier contribución de este tipo que busque respuestas a preguntas relacionadas con la asistencia técnica será rechazada.

### Las contribuciones deben hacer referencia claramente a las páginas de documentación afectadas.

Si crea un problema para sugerir mejoras en la documentación, debe incluir vínculos a las páginas afectadas. Si crea un problema utilizando el vínculo **Editar esta página** en una página de documentación, el problema se creará automáticamente con un vínculo a la página.

Esto no se aplica a las solicitudes de extracción, ya que las solicitudes de extracción por su naturaleza hacen referencia a las páginas afectadas.

## Directrices de documentación

Pedimos que cualquier contribución a nuestra documentación siga ciertas pautas de estilo.

Seguir estas directrices facilita la revisión de su contribución y, por lo tanto, la integración en nuestra documentación es más rápida.

### Idioma y estilo

#### Idioma

* AEM documentación se crea y se mantiene en inglés estadounidense.
* Mantenga las oraciones tan simples como sea posible.
* Mantenga el lenguaje claro y conciso.

Recuerde, los lectores de AEM documentación son de todo el mundo y no se puede esperar que sean hablantes nativos o fluidos del inglés. Evite los coloquialismos y mantenga el lenguaje tan claro y simple como sea posible.

#### Seguir el Manual de estilo de Microsoft

[Microsoft Manual of ](https://docs.microsoft.com/en-us/style-guide/welcome/) Stylees es una guía de estilo de documentación disponible libremente que se centra en documentación de software y documentación de AEM sigue esta guía siempre que sea posible.

### Formato

| Elemento | Estilo |
|---|---|
| Elemento u opción de la interfaz de usuario | **negrita** |
| Nombre de archivo, ruta, entrada de usuario, valores de parámetro | `monospaced` |
| Código, línea de comandos | ```Code Block``` |

### Capturas de pantalla

Las capturas de pantalla deben utilizarse con prudencia y solo cuando la descripción textual no sea suficiente.

No se deben utilizar marcadores u otras anotaciones en las capturas de pantalla (como marcos rojos, flechas o texto). De este modo, las capturas de pantalla son más fáciles de reutilizar o replicar en versiones localizadas de la documentación.

### Referencias específicas de la versión

Intente evitar cualquier referencia directa a una versión específica en todo el contenido de la documentación siempre que sea posible. Esto hace que la documentación sea más flexible y extensible para futuras versiones.

### Uso de Día, AEM, CQ, CRX

El producto siempre debe ser referido por su nombre completo **Adobe Experience Manager** por primera vez en un artículo y luego puede ser referido como **AEM**.

No se deben utilizar Day, Day Software, CQ y CRX excepto cuando sea inevitable, como en nombres de clase o en referencia al historial de AEM.