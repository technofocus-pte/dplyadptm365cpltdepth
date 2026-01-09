# Laboratorio 7 - Creación de agentes impulsados por MCP en Microsoft Copilot Studio

## Escenario:

Zava, una organización de salud digital en rápido crecimiento, ha
formado recientemente un **Hub interno de innovación** con el objetivo
de experimentar con nuevas capacidades de IA que posteriormente podrían
adaptarse a soluciones sanitarias reguladas. Antes de conectar sistemas
médicos confidenciales, el equipo de innovación necesita un entorno de
**prueba seguro y de bajo riesgo** para aprender cómo integrar API
externas y fuentes de datos con **Microsoft Copilot Studio** mediante el
**Model Context Protocol (MCP).**

Para lograrlo, el equipo comenzó con un ejemplo simple e inofensivo: un
**servidor MCP** de chistes (**Jokes MCP Server**), que ilustra cómo
Copilot Studio puede invocar API en tiempo real mediante MCP. Este
prototipo ligero permite a ingenieros, científicos de datos y
arquitectos de soluciones de IA comprender cómo funciona la integración:

- Cómo se implementan los servidores MCP en Azure,

- cómo Copilot Studio puede detectar y consumir herramientas MCP, y

- cómo los datos externos en tiempo real pueden integrarse de forma
  segura en los agentes.

Al completar este laboratorio, el equipo de innovación de Zava establece
la base para conectar futuros servidores MCP a sistemas empresariales
reales, una vez que se apliquen las medidas de gobernanza y cumplimiento
correspondientes.

## Valor empresarial:

- Fomenta el aprendizaje práctico con la integración de MCP antes de
  aplicarla a dominios sensibles.

- Demuestra la implementación de extremo a extremo y el consumo de
  herramientas en un entorno seguro y preparado para Azure.

- Fortalece la preparación organizacional para flujos de trabajo de
  próxima generación impulsados por IA.

## Objetivos:

En este laboratorio se demostrará cómo el Hub de innovación de Zava
experimenta con el Model Context Protocol (MCP) para conectar API
externas y fuentes de conocimiento con Microsoft Copilot Studio. Se
aprenderá a implementar un servidor MCP en Azure, registrarlo como
herramienta en Copilot Studio e integrarlo en un agente conversacional.

Al completar este laboratorio, se podrá:

> • Comprender cómo MCP permite la integración segura y en tiempo real
> de datos para los agentes de Copilot Studio.
>
> • Aprender a implementar, configurar y conectar un servidor MCP
> utilizando Azure Developer CLI.
>
> • Explorar el flujo de trabajo de extremo a extremo para agregar una
> herramienta impulsada por MCP a un agente de Copilot Studio.

## Ejercicio 1: Implementar el servidor MCP en Azure

En este ejercicio se **implementará** el servidor **Microsoft MCP**
(Model Context Protocol) desde un entorno de desarrollo local en
**Azure** utilizando Azure Developer CLI (azd). Esto establecerá un
**punto de conexión alojado en la nube** que podrá ser **consumido** por
**Copilot Studio** u otras aplicaciones en ejercicios posteriores.

1.  Abra **Docker Desktop** desde la máquina virtual del laboratorio.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.png)

2.  Abra **Visual Studio Code** y seleccione **Open Folder**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.png)

3.  Seleccione la carpeta **mcsmcp** ubicada en **C:\LabFiles** y haga
    clic en **Select Folder.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.png)

4.  Seleccione **Yes, I trust the authors** para continuar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.png)

5.  En **VS Code**, seleccione **View → Terminal** para abrir la
    terminal.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.png)

6.  Ingrese **azd auth login** para iniciar sesión en **Azure**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.png)

7.  **Inicie** sesión utilizando las credenciales proporcionadas en la
    pestaña **Resources.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.png)

8.  Ingrese +++**azd up**+++ y presione **Enter** para generar la
    estructura del proyecto en Azure.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.png)

9.  Ingrese el nombre <+++mcsmcp@lab.LabInstance.Id>+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.png)

10. Presione **Enter** para aceptar la suscripción que se muestra en la
    lista.

![A screen shot of a computer AI-generated content may be
incorrect.](./media/image11.png)

11. Seleccione **@lab.CloudResourceGroup(ResourceGroup1).Location** como
    su ubicación.

12. Utilice las teclas de flecha para desplazarse hacia arriba o hacia
    abajo en la lista de **regiones**, seleccione la región identificada
    en el paso anterior y presione **Enter**. La región mostrada en la
    captura de pantalla y la asignada en la máquina virtual del
    laboratorio pueden variar.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image12.png)

13. Esto implementará los recursos necesarios en el portal de Azure y
    mostrará un mensaje de confirmación de implementación exitosa.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.png)

14. La salida también proporcionará una **URL de Endpoint**.
    **Guárdela** en un **bloc de notas** para utilizarla en los próximos
    ejercicios.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.png)

15. Agregue **/mcp** al final de esa URL y ábrala en un navegador.
    Aparecerá un mensaje de error en formato JSON, lo cual es correcto,
    ya que indica que se ha establecido conexión con el servidor MCP.

![](./media/image15.png)

En este ejercicio se abrió el proyecto del servidor MCP en Visual Studio
Code, se autenticó en Azure utilizando Azure Developer CLI y se
implementó la solución en Azure mediante el comando azd up. La
implementación creó los recursos necesarios en Azure (como una Container
App y la infraestructura de soporte) y proporcionó una URL de endpoint
pública para el servidor MCP. La verificación del endpoint en un
navegador confirmó la implementación y conectividad exitosas,
estableciendo la base para integrar el servidor MCP con los componentes
posteriores en los próximos ejercicios.

## Ejercicio 2: Usar el servidor MCP de chistes (Jokes MCP Server) en Microsoft Copilot Studio

### Tarea 1: Importar el conector

**Objetivo**

Importar y configurar un **conector MCP personalizado** en **Power
Apps** para integrarlo con el servidor MCP implementado.

1.  Vaya a +++<https://make.preview.powerapps.com/customconnectors+++>

2.  Seleccione **+ New custom connector** -\> **Import from GitHub**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.png)

3.  Seleccione los siguientes detalles.

    - **Connector Type – Custom**

    - **Branch – dev**

    - \*\*Connector - MCP-Streamable-HTTP \*\*

Seleccione **Continue**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image17.png)

4.  Cambie el **nombre del conector** a **+++Jokes MCP+++**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image18.png)

5.  Pegue la URL raíz (la parte posterior a https://) de la dirección
    guardada anteriormente en el campo **Host**, y seleccione **Create
    connector**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.png)

\[!Alert\] **Advertencia**

Es posible que aparezcan una advertencia y un error durante la creación.
Este problema debería resolverse pronto, pero puede ignorarlo por ahora.

6.  **Cierre** el conector.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.png)

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image21.png)

En esta tarea se importó el conector **MCP-Streamable-HTTP** desde
GitHub a Power Apps, se le asignó el nombre **Jokes MCP** y se configuró
con la URL del servidor MCP alojado en Azure. Esto establece una
conexión entre Power Platform y el servidor MCP, lo que permite futuras
interacciones en las siguientes tareas.

### Tarea 2: Crear un agente y agregar el servidor MCP como una herramienta

En esta tarea se creará un agente personalizado llamado **Jokester** en
Microsoft Copilot Studio y se integrará con el **Jokes MCP Server**
utilizando el framework **Model Context Protocol (MCP)**, lo que
permitirá que el agente obtenga y entregue chistes dinámicos desde el
endpoint MCP conectado.

1.  Abra **Copilot Studio** desde un navegador mediante la URL,
    +++[https://copilotstudio.microsoft.com+++](https://copilotstudio.microsoft.com+++/) e
    inicie sesión con las credenciales proporcionadas en la pestaña
    **Resources**. Seleccione **Get Started** para habilitar la licencia
    de prueba.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image22.png)

2.  Seleccione **Create** -\> **+ New agent**.

![A screenshot of a phone AI-generated content may be
incorrect.](./media/image23.png)

3.  Seleccione la pestaña **Configure** para configurar su agente.

![A screenshot of a login page AI-generated content may be
incorrect.](./media/image24.png)

4.  Ingrese los siguientes detalles y seleccione **Create**.

- **Name** – +++Jokester+++

- **Description** –

> +++A humor-focused agent that delivers concise, engaging jokes only
> upon user request, adapting its style to match the user's tone and
> preferences. It remains in character, avoids repetition, and filters
> out offensive content to ensure a consistently appropriate and witty
> experience.+++

- **Instructions** –

> You are a joke-telling assistant. Your sole purpose is to deliver
> appropriate, clever, and engaging jokes upon request. Follow these
> rules:
>
> \* Respond only when the user asks for a joke or something related
> (e.g., "Tell me something funny").
>
> \* Match the tone and humor preference of the user based on their
> input—clean, dark, dry, pun-based, dad jokes, etc.
>
> \* Never break character or provide information unrelated to humor.
>
> \* Keep jokes concise and clearly formatted.
>
> \* Avoid offensive, discriminatory, or NSFW content.
>
> \* When unsure about humor preference, default to a clever and
> universally appropriate joke.
>
> \* Do not repeat jokes within the same session.
>
> \* Avoid explaining the joke unless explicitly asked.
>
> \* Be responsive, witty, and quick.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image25.png)

5.  El **agente** se **crea** según las instrucciones proporcionadas.

![A logo of a company AI-generated content may be
incorrect.](./media/image26.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image27.png)

6.  Seleccione **Settings** en la esquina superior derecha de la página
    del agente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image28.png)

7.  En el panel de **Settings**, seleccione **No** en la opción **Use
    generative AI orchestration for your agent responses**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image29.png)

8.  Desplácese hacia abajo y desactive **Use general knowledge** y **Use
    information from the Web** en la sección **Knowledge**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image30.png)

9.  Desplácese hacia arriba y seleccione **Yes** en la opción **Use
    generative AI orchestration for your agent responses**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image31.png)

10. Seleccione **Save** y luego cierre la ventana de **Settings**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image32.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image33.png)

11. Desde la página **Overview** del agente, seleccione **Tools.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image34.png)

12. Seleccione **+ Add a tool** para agregar una nueva herramienta al
    agente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image35.png)

13. En la ventana **Add a tool**, seleccione la pestaña **Model Context
    Protocol**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image36.png)

14. Seleccione el **Jokes MCP Server** que creó anteriormente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image37.png)

15. Seleccione el **menú desplegable** junto a **Not connected** y luego
    haga clic en **Create new connection**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image38.png)

16. En la siguiente pantalla, seleccione **Create**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image39.png)

17. Una vez establecida la conexión, seleccione el botón **Add to
    agent** para agregar el servidor MCP al agente Jokester.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image40.png)

18. El **servidor MCP** ha sido agregado como herramienta al agente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image41.png)

19. Seleccione **Refresh** en el panel **Test** antes de comenzar a
    probar el comportamiento del agente.

![A screenshot of a phone AI-generated content may be
incorrect.](./media/image42.png)

20. Ingrese +++**Can I get a Chuck Norris joke?**+++ y seleccione
    **Send**.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image43.png)

21. Seleccione **Open connection manager**.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image44.png)

22. Seleccione **Connect** para establecer la conexión.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image45.png)

23. Una vez seleccionada la conexión **Jokes MCP**, haga clic en
    **Submit**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image46.png)

24. Ahora puede observar que, en la página **Manage your connections**,
    el **Jokes MCP Server** se encuentra en estado **connected**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image47.png)

25. Ahora que está conectado, regrese al panel **Test** y seleccione
    **Retry**.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image48.png)

26. Ahora puede observar que se está invocando el **servidor MCP** y que
    el agente intenta generar una respuesta desde el **Jokes MCP
    Server**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image49.png)

27. El agente utiliza el **servidor MCP**, genera una **respuesta** y la
    muestra en el panel **Test**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image50.png)

Y así es como funciona el **Jokes MCP Server** en **Microsoft Copilot
Studio**.

En esta tarea, se creó un nuevo agente llamado **Jokester** en **Copilot
Studio**, se configuraron su propósito e instrucciones de comportamiento
para la generación de humor y se habilitó **Generative AI
Orchestration** para respuestas inteligentes. Luego, se conectó el
**Jokes MCP Server** como herramienta mediante el **Model Context
Protocol**, se autenticó la conexión y se probó con éxito la integración
obteniendo chistes a través del panel de prueba del agente. Esto
confirmó que el **servidor MCP** estaba correctamente conectado y
funcionando dentro del entorno de **Copilot Studio**.

## Resumen

En este laboratorio, el **Hub de innovación de Zava** exploró con éxito
cómo el **Model Context Protocol (MCP)** puede ampliar **Microsoft
Copilot Studio** mediante la integración de datos externos en tiempo
real. Se inició con un ejemplo seguro y de bajo riesgo: el **Jokes MCP
Server**. Los participantes aprendieron a implementar un servidor MCP en
Azure utilizando **Azure Developer CLI**, configurarlo como un conector
personalizado y consumirlo dentro de un **agente de Copilot Studio**.

A través de los ejercicios, se creó un agente personalizado denominado
**Jokester**, conectado de forma segura al **Jokes MCP Server**,
demostrando cómo **Copilot Studio** puede realizar llamadas a API en
tiempo real mediante MCP. El laboratorio proporcionó experiencia
práctica en la configuración, autenticación y prueba de herramientas
basadas en MCP, estableciendo una base sólida para la futura integración
de servidores MCP críticos para el negocio con los sistemas de datos
empresariales.
