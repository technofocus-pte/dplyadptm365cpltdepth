# Creación y administración de agentes en Microsoft 365 Copilot

## Introducción

Este laboratorio se centra en la creación y configuración de un agente
de Copilot en Microsoft 365 Copilot Chat utilizando Copilot Studio Agent
Builder. Aprenderá a crear un agente mediante las pestañas Describe y
Configure, personalizar sus instrucciones y fuentes de conocimiento,
probar su funcionalidad y administrar el uso compartido dentro de su
organización.

## Objetivo

En este laboratorio creará y configurará un agente de Copilot utilizando
las pestañas Describe y Configure.  
Utilizará Copilot Studio Agent Builder:

- Crear un agente utilizando las pestañas Describe y Configure en
  Copilot Studio Agent Builder

> **Importante:** La pestaña Describe está disponible solo cuando el
> idioma de Microsoft 365 está configurado en uno de los idiomas
> compatibles. Si su idioma preferido no admite la pestaña Describe, aún
> puede crear su agente utilizando la pestaña **Configure**.

- Personalizar las instrucciones del agente, la fuente de conocimiento y
  los prompts iniciales.

- Probar y editar su agente.

- Administrar y compartir su agente dentro de su organización..

## Aprendizajes clave

- Comprender cómo crear un agente utilizando la pestaña Describe
  proporcionando una descripción en lenguaje natural de su propósito.

- Aprender a ajustar la configuración del agente, las instrucciones, el
  tono y las fuentes de conocimiento mediante la pestaña Configure.

- Probar y validar las respuestas del agente utilizando la funcionalidad
  Try it antes de publicar.

- Explorar opciones de administración como Share, Edit y Uninstall para
  controlar la accesibilidad y mejorar la funcionalidad.

- Establecer permisos para compartir agentes (en toda la organización,
  usuarios específicos o solo usted) y generar enlaces compartibles para
  la colaboración. 

# Ejecución paso a paso

## Ejercicio 1: Crear un agente de Copilot utilizando la pestaña Describe

En este ejercicio utilizará la pestaña Describe en Copilot Studio para
crear un agente básico.

1.  Abra un navegador Microsoft Edge e introduzca la siguiente URL:
    +++[https://m365.cloud.microsoft](https://m365.cloud.microsoft)+++ para
    ir a la página principal de la aplicación **Microsoft 365 Copilot**
    (anteriormente Office).

    **Nota:** Debe iniciar sesión (si se le solicita) utilizando las
    credenciales proporcionadas en la pestaña **Resources en el lado
    derecho**.

    ![](./media/image1.png)

    ![](./media/image2.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image3.png)

    - Haga clic en **Yes** para mantener la sesión iniciada.

        ![A screenshot of a computer AI-generated content may be
        incorrect.](./media/image4.png)

2.  Se abrirá la página de **Copilot Chat**.

    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image5.png)

3.  En el panel de navegación izquierdo de **Copilot Chat**, vaya a la
    sección **Agents** y haga clic en la pestaña **New Agent.**

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image6.png)

4.  Verá la página principal de **Copilot Studio Agent Builder** con
    tres botones en la parte superior:

    **• Describe:** Esta pestaña le permite crear un agente simplemente
    describiendo su propósito en lenguaje natural. Genera automáticamente
    configuraciones iniciales basadas en su descripción.
    
    **• Configure:** Esta pestaña le permite ajustar la configuración del
    agente, como instrucciones, tono y fuentes de conocimiento, para un
    comportamiento más preciso.
    
    **• Try it:** Esta opción le permite probar las respuestas del agente
    frente a sus prompts y verificar su funcionalidad antes de publicarlo.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image7.png)

5.  En la pestaña **Describe**, introduzca la descripción del propósito
    del agente en lenguaje natural y haga clic en **Send.**

    **“An agent that assists users in finding popular learning paths and modules from Microsoft**”

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image8.png)

6.  Haga clic en **Send** para obtener una vista previa del agente en
    borrador.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image9.png)

7.  Un agente en borrador con configuraciones iniciales se guardará
    automáticamente. Revise los campos generados automáticamente y
    realice los ajustes necesarios. En este ejercicio utilizará los
    campos generados automáticamente tal como están.

8.  Se le pedirá confirmar o sugerir un nombre para el agente. En este
    ejercicio, asigne el nombre **LearnAssist Buddy**.

    ![](./media/image10.png)

9.  Agent Builder confirma que el nombre del agente se ha actualizado a
    LearnAssisst Buddy.

    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image11.png)

10. Ahora ha creado un agente con detalles básicos. Se le pedirá que
    refine las instrucciones del agente y realice los ajustes
    necesarios. En este ejercicio utilizará la configuración
    predeterminada para agilizar el proceso de creación.

    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image12.png)

## Ejercicio 2: Configurar los detalles del agente utilizando la pestaña Configure

En este ejercicio configurará los ajustes del agente para ajustar su
comportamiento mediante la pestaña **Configure**.

**Nota:** Si está creando un agente directamente desde la pestaña
Configure, deberá definir el nombre, la descripción y el propósito del
agente.

1.  Cambie a la pestaña **Configure** en la ventana de Agent Builder.

    ![](./media/image13.png)

2.  Puede configurar los ajustes de comportamiento del agente, incluido
    el tono de respuesta y el estilo de interacción. En este ejercicio
    continuará con las instrucciones predeterminadas.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image14.png)

3.  Ahora configurará las fuentes de conocimiento que utilizará el
    agente, como sitios específicos de SharePoint, bibliotecas de
    documentos y sitios web. En este ejercicio utilizará un sitio web
    como fuente de conocimiento para fundamentar las respuestas del
    agente.

    Introduzca +++<https://learn.microsoft.com/en-us/training>+++ y presione
    Enter.

    ![](./media/image15.png)

4.  Ahora habilitará la búsqueda web solo para las fuentes
    especificadas.

    ![](./media/image16.png)

    **Nota:** La URL del sitio web no puede tener más de dos niveles de
    profundidad. Además, el agente buscará en sitios web públicos si no
    agrega una URL y activa la búsqueda web.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image17.png)

5.  Los cambios de configuración se guardarán automáticamente.

6.  Ahora ha completado la configuración del agente con ajustes
    personalizados adaptados a las necesidades de su organización. A
    continuación, asegurará que el agente funcione según lo previsto y
    realizará los ajustes necesarios.

## Ejercicio 3: Probar y editar el agente

Ahora probará si el agente responde según la configuración establecida
en la ventana **Try it** de Agent Builder.

1.  Cambie a la pestaña **Try it** en la ventana de Agent Builder.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image18.png)

2.  Ahora introduzca el siguiente prompt para evaluar la respuesta del
    agente.

    **"List the popular learning paths and modules offered by Microsoft”**

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image19.png)

3.  Puede verificar la respuesta comparándola con la información
    disponible en la URL utilizada como fuente de conocimiento.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image20.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image21.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image22.png)

4.  También puede probar la respuesta introduciendo un prompt no
    relacionado.

    **"Help me with instructions for baking cakes"**

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image23.png)

    ![](./media/image24.png)

5.  El agente evitó proporcionar una respuesta basándose en la
    instrucción “Avoid discussing topics unrelated to Microsoft learning
    paths and modules”.

    **Nota:** El conjunto de instrucciones predeterminado en su caso puede
    ser diferente. Asegúrese de que las instrucciones estén configuradas
    correctamente para que el agente evite proporcionar la respuesta.

6.  **Opcional:** Vuelva a la pestaña **Configure** para editar la
    configuración, las instrucciones o las fuentes de conocimiento del
    agente según sea necesario.

7.  Una vez que esté satisfecho, haga clic en **Create** en la esquina
    superior derecha para publicar el agente.

    ![](./media/image25.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image26.png)

8.  Su agente LearnAssist Buddy se ha creado correctamente.

    - Haga clic en el botón **Go to agent** para abrir el agente
    **LearnAssist Buddy** creado.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image27.png)

9.  La interfaz de chat de **LearnAssit Buddy** ahora está abierta para
    la interacción.

    ![](./media/image28.png)

## Ejercicio 4: Administrar y compartir el agente

Ahora implementará el agente dentro de su organización y administrará su
accesibilidad.

1.  Su agente **LearnAssist Buddy** ahora está disponible en el panel de
    navegación de Copilot Chat en la sección **Agents**.  
    Haga clic en los puntos suspensivos (….) junto al agente para ver
    las acciones disponibles. Puede:  
    • Share – Otorgar acceso a usuarios o grupos específicos mediante la
    configuración de permisos.  
    • Edit – Modificar el nombre del agente, las instrucciones o las
    fuentes de conocimiento para mejorar la funcionalidad.  
    • Uninstall – Eliminar el agente del entorno de Copilot Chat si ya
    no es necesario.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image29.png)

2.  Al seleccionar la opción **Share** en la interfaz de Copilot Chat,
    se abrirá la ventana “**Share your agent”**. En esta ventana, puede:

    **•** Generar un enlace compartible: Este enlace le permite proporcionar
    acceso al agente a usuarios o grupos específicos dentro de su
    organización.  
    • Establecer permisos: Puede definir quién puede ver o editar el agente
    asignando roles y niveles de acceso.  
    • Distribuir fácilmente: Una vez generado el enlace, puede copiarlo y
    compartirlo mediante correo electrónico, Teams u otros canales de
    comunicación para una colaboración rápida.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image30.png)

3.  Configure los permisos requeridos y haga clic en **Apply** para
    generar un enlace compartible. Puede elegir uno de los siguientes
    niveles de permisos:  
    **• Anyone in your organization:** Esta configuración hace que el
    agente sea accesible para todos los usuarios dentro de su
    organización. Es ideal para agentes de uso general que admiten
    tareas comunes o recursos de aprendizaje.  
    **• Specific users in your organization:** Esta opción le permite
    compartir el agente solo con individuos o grupos seleccionados. Es
    útil cuando el agente está diseñado para un equipo o departamento
    específico.  
    • **Only you: Esto restringe el acceso al agente para que solo usted
    pueda usarlo y administrarlo. Es ideal para agentes personales o
    experimentales que no están listos para una implementación más
    amplia.**

4.  He decidido compartir el agente LearnAssist Buddy con todos en mi
    organización.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image31.png)

5.  Ahora, copie el enlace generado para toda la organización y
    compártalo con su equipo.

    ![](./media/image32.png)

6.  Haga clic en el icono **Copy** para copiar el enlace generado en la
    ventana **Your agent was shared.**

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image33.png)

**Nota:** Realice mejoras iterativas basadas en los comentarios de los
usuarios y las métricas de rendimiento.

**Pruébelo usted mismo:**

- Cree un agente “Product Buddy” para obtener detalles de productos.

- Configure el agente con la Description, Instructions y las fuentes de
  conocimiento necesarias.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image34.png)

- Asigne las fuentes de conocimiento desde su biblioteca de documentos.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image35.png)

- Pruebe el agente realizando prompts relacionados con productos para
  verificar su funcionamiento.

# Resumen

Al completar este laboratorio, ha creado y configurado correctamente un
agente de Copilot, lo ha vinculado a fuentes de conocimiento relevantes,
ha probado su comportamiento y ha aprendido a administrarlo y
compartirlo dentro de su organización. Estos pasos garantizan que sus
agentes proporcionen respuestas precisas y contextualizadas y que puedan
implementarse de manera efectiva para uso en equipos u organizaciones.
