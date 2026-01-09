# Laboratorio 3 - Automatizar la asistencia de conocimiento mediante Microsoft 365 Copilot Agents

**Duración: 20 minutos**

Objetivo:

En este laboratorio se creará y configurará un agente de Copilot
utilizando las pestañas **Describe** y **Configure**.

Se utilizará **Copilot Studio Agent Builder** para:

- Crear un agente mediante las pestañas **Describe** y **Configure** en
  **Copilot Studio Agent Builder**.

**Nota:** La disponibilidad de la pestaña **Describe** depende de la
**región geográfica y del idioma**. Si la pestaña **Describe** no está
disponible en su región o idioma preferido, puede crear el agente
manualmente mediante la pestaña **Configure**

- Personalizar las instrucciones del agente, la fuente de conocimiento y
  los starter prompts.

- Probar y editar el agente.

- Administrar y compartir el agente dentro de la organización.

Ejercicio 1: Crear un agente de Copilot usando la pestaña Describe  
En este ejercicio se utilizará la pestaña **Describe** en **Copilot
Studio** para crear un agente básico.

1.  Abra el navegador **Edge** y navegue a
    <https://m365.cloud.microsoft> para acceder a la página principal de
    **Microsoft 365 Copilot**, y luego haga clic en el botón **Sign
    in**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image1.png)
>
> **Nota:** Debe iniciar sesión (si se le solicita) utilizando las
> **credenciales** proporcionadas en la pestaña **Resources** ubicada en
> el lado derecho de la pantalla.

2.  Ingrese el **nombre de usuario** y la **contraseña** para abrir la
    página **Copilot Chat**.

![](./media/image2.png)

3.  La interfaz de **Copilot Chat** se abrirá.

> ![](./media/image3.png)
>
> **Nota:** Si aparece el mensaje **Something went wrong**, haga clic en
> **Refresh** para volver a abrir la aplicación **Copilot**

4.  Haga clic en **Create an agent** en el panel de navegación izquierdo
    de la página principal de **Copilot Chat**.

> ![A screenshot of a chat AI-generated content may be
> incorrect.](./media/image4.png)

5.  **Interfaz de Copilot Studio Agent Builder:**  
    Al abrir **Copilot Studio Agent Builder**, aparecerán **tres
    pestañas** en la parte superior de la pantalla:

- **Describe** – Define el propósito y la funcionalidad del agente.

- **Configure** – Personaliza el comportamiento, los desencadenadores
  (*triggers*) y las acciones del agente.

- **Try it** – Permite probar las respuestas del agente y refinar su
  rendimiento.

> **Nota:** Use estas pestañas de forma secuencial para diseñar,
> configurar y validar su agente de Copilot antes del despliegue.
>
> ![](./media/image5.png)

6.  En la pestaña **Describe**, ingrese la descripción del propósito del
    agente en lenguaje natural y luego haga clic en el botón
    **Ejecutar**.  
    Ingrese la siguiente descripción en el campo de chat: +++**An agent
    that assists users in finding popular learning paths and modules
    from Microsoft**+++.

> ![](./media/image6.png)

7.  Valide la respuesta del agente con respecto a la descripción
    proporcionada. El chat sugerirá un nombre para el agente y le pedirá
    confirmarlo. Para este laboratorio, escriba +++Use suggested name+++
    en el campo y luego haga clic en el **botón Ejecutar**.

> ![](./media/image7.png)

8.  Haga clic en el botón **Create** ubicado en la parte superior
    derecha de la ventana del generador de agentes para enviar el
    agente.

**Nota:** En este ejercicio se utilizan las configuraciones
predeterminadas para agilizar el proceso de creación.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.png)

9.  Una vez que el agente se haya creado correctamente, haga clic en el
    **botón Go to agent** para comenzar a interactuar con él. ![A
    screenshot of a computer AI-generated content may be
    incorrect.](./media/image9.png)

**Nota:** Si el nombre del agente no aparece actualizado en la
**interfaz de** **Copilot Chat**, pruebe los siguientes pasos:

- **Actualice** la página**,** o en el panel de navegación izquierdo,
  seleccione la pestaña **Agents** y elija su agente en la lista.

> ![](./media/image10.png)

10. Ahora se ha creado el agente **Learning Path Finder** con la
    configuración predeterminada.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image10.png)

### Probar su agente

A continuación, se verificará que el agente responda según la
configuración predeterminada.

1.  Ingrese el siguiente *prompt* en el campo de chat del agente para
    evaluar su respuesta y validarla:

> **Prompt:** +++List the popular learning paths and modules offered by
> Microsoft+++
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image11.png)
>
> ![](./media/image12.png)

2.  De manera similar, pruebe la respuesta del agente ingresando un
    *prompt* irrelevante en el campo de chat:

> Prompt: +++**Help me with instructions for baking cakes**+++

- De forma predeterminada, el agente evita proporcionar respuestas
  basadas en información ajena a los **Microsoft Learning** paths,
  demostrando precisión y confiabilidad en su comportamiento
  predeterminado.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image13.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image14.png)
>
> **Consejo:** Puede explorar más sobre los Microsoft learning paths
> haciendo clic en la **Prompt Gallery**. Seleccione el agente
> **Learning Path Finder**, desplácese hacia abajo, haga clic en **See
> more**, y luego en **Prompt Gallery** para ver los prompts sugeridos.
>
> ![](./media/image15.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image16.png)

Ejercicio 2: Configurar los detalles del agente usando la pestaña
Configure  
En este ejercicio se configurarán los ajustes del agente para refinar su
comportamiento.

**Nota:** Si crea un agente desde la pestaña **Configure**, deberá
definir el nombre, la descripción y el propósito del agente.

1.  En el panel de navegación izquierdo, seleccione el agente **Learning
    Path Finder** que se creó con la configuración predeterminada.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image17.png)

2.  Haga clic en el ícono **de tres puntos (⋯)** junto al nombre del
    agente y seleccione **Edit.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.png)

3.  Configure los ajustes de comportamiento del agente, incluido el tono
    de las respuestas y el estilo de interacción. En este ejercicio, se
    continuará con las instrucciones predeterminadas.

![](./media/image19.png)

4.  Cargue los archivos, carpetas o sitios recomendados por su
    organización como **Knowledge Source** del agente. Haga clic en el
    ícono de **Upload** para agregar archivos directamente desde su
    **OneDrive.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.png)

5.  Configure las fuentes de conocimiento que utilizará el agente, como
    sitios de **SharePoint**, bibliotecas de documentos o sitios web
    específicos. En este ejercicio, se utilizará un sitio web como
    fuente de conocimiento para fundamentar las respuestas del agente.

6.  Haga clic en el campo de búsqueda de **Knowledge source**, pegue el
    siguiente enlace y presione **Enter**:
    +++**https://learn.microsoft.com/en-us/training/**+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image21.png)

> **Nota:** La URL del sitio web no puede tener más de dos niveles de
> profundidad. Además, el agente buscará en sitios web públicos si no se
> agrega una URL y la búsqueda web está activada.
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image22.png)

7.  Los cambios de configuración se guardan automáticamente a medida que
    se editan. Para finalizar y aplicar todas las actualizaciones, haga
    clic en el botón **Update** ubicado en la esquina superior derecha.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image23.png)

**Nota:** Con esto, la configuración del agente queda completada y
adaptada a las necesidades de la organización.

8.  Haga clic en **Go to agent** para visualizar las actualizaciones en
    la ventana de **Copilot Chat**, verificar que el agente funcione
    según lo previsto y realizar los ajustes necesarios.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image24.png)

### Probar su agente personalizado 

Pruebe el agente personalizado para verificar que las configuraciones
aplicadas, las fuentes de conocimiento y los ajustes de comportamiento
funcionen correctamente.

1.  Ingrese el siguiente *prompt* en el campo de chat del agente
    **LearnAssistantBuddy** y evalúe la respuesta del agente: 

> +++**List the popular learning paths and modules offered by
> Microsoft**+++ 
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image25.png)
>
> ![](./media/image26.png)

2.  Verifique la respuesta comparándola con la información disponible en
    la URL utilizada como fuente de conocimiento. 

>  
>
> ![](./media/image27.png) 

3.  Ahora pruebe la respuesta del agente ingresando un prompt
    irrelevante: 

> **Prompt**: +++**Find out the top 10 tourist places in India**+++ 
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image28.png)
>
> **Nota:** El agente evita proporcionar respuestas basadas en la
> instrucción *“Avoid discussing topics unrelated to Microsoft learning
> paths and modules”*.
>
> ![](./media/image29.png)
>
> **Nota**: El conjunto de instrucciones predeterminado puede variar.
> Asegúrese de que las instrucciones estén correctamente configuradas
> para que el agente evite generar respuestas fuera del contexto. 

## Ejercicio 3: Administrar y compartir el agente

A continuación, se desplegará el agente dentro de la organización y se
gestionará su accesibilidad.

1.  Comparta el agente con usuarios o grupos específicos asignando los
    permisos adecuados.

2.  En el panel de navegación izquierdo, seleccione el agente
    **LearnAssistantBuddy**, haga clic en el menú de **tres puntos (⋯)**
    y elija **Share.**

> ![](./media/image30.png)

3.  En el cuadro de diálogo **Share agent**, seleccione cómo desea
    compartir el agente:

- Elija **Anyone in your organization** para que esté disponible para
  todos los usuarios.

- O bien, seleccione **Specific users in your organization** o **Only
  you**, según la preferencia de uso compartido.

- Haga clic en **Save** para confirmar la selección.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image31.png)

4.  Seleccione la primera opción, **Anyone in my organisation**, para
    que el agente esté disponible para todos los usuarios, y luego haga
    clic en **Save**.

![](./media/image32.png)

5.  Después de hacer clic en **Save**, copie el enlace generado y
    compártalo con los miembros de su equipo para que puedan acceder al
    agente.

![](./media/image33.png)

## Pruébelo usted mismo: 

1.  Cree un agente denominado Product Buddy para obtener detalles de
    productos.

2.  Asigne la fuente de conocimiento a la biblioteca de documentos
    creada en el *laboratorio 0 - Preparación para la ejecución del
    laboratorio*.

3.  Pruebe el agente solicitando prompts relacionados con productos para
    verificar su funcionamiento.

Resumen  
Al completar este laboratorio, se habrá adquirido experiencia práctica
en el diseño, personalización e implementación de **Copilot Agents** que
ofrecen asistencia contextual alineada con el conocimiento y los
objetivos organizacionales.
