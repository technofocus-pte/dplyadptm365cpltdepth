# Laboratorio 6 - Crear un agente declarativo poético utilizando Microsoft 365 Agents Toolkit

## Escenario  
Una organización desea explorar cómo **Microsoft 365 Copilot** puede
personalizarse utilizando **agentes declarativos** para ofrecer
experiencias únicas, con marca y orientadas a la personalidad. Como
prueba de concepto, el equipo decide crear un agente creativo que
responda a las preguntas de los usuarios en **forma poética**,
aprovechando al mismo tiempo la inteligencia central y el conocimiento
web de Microsoft 365 Copilot.

Utilizando **Microsoft 365 Agents Toolkit** en Visual Studio Code, el
equipo creará un agente declarativo, **definirá** su **comportamiento**
mediante **instrucciones**, mejorará la experiencia del usuario con
**conversation starters** y habilitará capacidades de **búsqueda web**,
todo mientras prueba el agente directamente en **Microsoft 365 Copilot
Chat**.

**Objetivo**  
Al completar este laboratorio, aprenderá a:  
- **Crear un agente declarativo utilizando Microsoft 365 Agents
Toolkit** en Visual Studio Code.  
- **Aprovisionar** y **probar** el agente **declarativo** dentro de
Microsoft 365 Copilot Chat.  
- **Definir el comportamiento del agente** mediante **prompts de
instrucciones** en el manifiesto del agente.  
- **Personalizar** la personalidad del agente aplicando respuestas en
formato poético.  
- **Agregar conversation starters** para guiar la interacción del
usuario.  
- **Habilitar capacidades de búsqueda web** para el agente.  
- **Validar el comportamiento del agente** después de cada mejora
mediante pruebas en tiempo real.

## Ejercicio 1: Crear un agente declarativo

En este ejercicio, comenzará creando un agente declarativo básico desde
Visual Studio Code.

1.  Desde el escritorio de la máquina virtual, abra **Visual Studio
    Code**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image1.png)

2.  Seleccione **Extensions** en el panel izquierdo y escriba
    +++Microsoft 365 Agents Toolkit+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image2.png)

3.  Seleccione **Microsoft 365 Agents Toolkit** y haga clic en
    **Install** para instalar la extensión.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image3.png)

4.  Seleccione **Create a New Agent/App** en el panel izquierdo y luego
    seleccione **Declarative Agent**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image4.png)

5.  Seleccione **No Action** para crear un agente declarativo básico.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image5.png)

6.  Seleccione **Default folder** para almacenar la carpeta raíz del
    proyecto en la ubicación predeterminada.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image6.png)

7.  Introduzca +++My Agent+++ como **Application Name** y presione
    **Enter**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image7.png)

8.  Seleccione **Yes, I trust the authors** en la ventana emergente.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image8.png)

9.  En la nueva ventana de **Visual Studio Code**, seleccione
    **Microsoft 365 Agents Toolkit**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image9.png)

10. Seleccione **Provision** en el panel **Lifecycle** y luego
    seleccione **Sign in** en la ventana emergente para iniciar sesión
    en la cuenta de **Microsoft 365**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image10.png)

    Si el aprovisionamiento falla y Visual Studio Code ofrece la opción
    **resolve with @m365agents**, selecciónela. El aprovisionamiento debería
    completarse correctamente.

11. **Inicie sesión** con las siguientes credenciales y cierre la
    ventana cuando finalice:  
    - Username - +++@lab.CloudPortalCredential(User1).Username+++  
    - TAP - +++@lab.CloudPortalCredential(User1).TAP+++  
    ![A black background with white text AI-generated content may be
    incorrect.](./media/image11.png)

12. Asegúrese de que el aprovisionamiento se haya completado
    correctamente. Puede ver el mensaje de éxito en la esquina inferior
    derecha de Visual Studio Code.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image12.png)

Tarea 1: Probar el agente

En esta tarea, probará el agente declarativo creado.

1.  Navegue a la aplicación Copilot con la URL
    +++<https://m365.cloud.microsoft/chat+++>

2.  En la parte superior izquierda, **seleccione** el **icono de
    conversation drawer**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image13.png)

3.  Seleccione el agente declarativo **My Agentdev** (o **My Agent**,
    según el nombre que aparezca).  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image14.png)

4.  Introduzca la pregunta +++Hello! How can you help me?+++ y verifique
    que responda con “Thanks for using Microsoft 365 Agents Toolkit to
    create your declarative agent!”  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image15.png)  
    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image16.png)

En este ejercicio, ha creado un agente declarativo básico y ha validado
su funcionamiento.

## Ejercicio 2: Agregar instrucciones

En este ejercicio, agregará instrucciones al agente declarativo y
mejorará su comportamiento.

1.  En Visual Studio Code, abra el archivo
    **appPackage/instructions.txt** y reemplace su contenido con el
    siguiente texto:

    ```
    You are a declarative agent and were created with Microsoft 365 Agents
    Toolkit. You are an expert at creating poems.
    
    Every time a user asks a question, you must turn the answer into a poem.
    The poem must not use the quote markdown and use regular text.
    ``` 
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image17.png)
    
    El contenido de este archivo se inserta en la propiedad instructions del
    manifiesto del agente durante el aprovisionamiento.

2.  Seleccione **Provision** en el panel **Lifecycle** de Agents
    Toolkit.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image18.png)

3.  Verifique que el **aprovisionamiento se complete correctamente**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image19.png)

4.  El agente utilizará las instrucciones actualizadas después de
    recargar la página.

5.  Actualice la página de chat, seleccione **My Agentdev** y escriba
    +++Do we have chocolate in our food catalog?+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image20.png)

6.  Observe que el agente responde en formato poético.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image21.png)

7.  Ahora, agregue conversation starters al agente.

8.  Abra el archivo **appPackage/declarativeAgent.json** y, después del
    nodo instructions, agregue una coma, presione Enter y pegue el
    siguiente código:
    ```
    "conversation_starters": [  
        {  
            "title": "Getting Started",  
            "text": "How can I get started with Agents Toolkit?"  
        },  
        {  
            "title": "Getting Help",  
            "text": "How can I get help with Agents Toolkit?"  
        }  
    ]
    ```
    ![A screen shot of a computer AI-generated content may be
    incorrect.](./media/image22.png)

10.  Seleccione **Provision** en el panel Lifecycle de **Microsoft 365
    Agents Toolkit** y verifique que se complete correctamente.

11. Los conversation starters estarán disponibles después de
    **actualizar** la página.

12. **Actualice** la página de chat para comprobarlo.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image23.png)

## Ejercicio 3: Agregar contenido web

En este ejercicio, agregará la capacidad de búsqueda web al agente.

1.  Abra el archivo **appPackage/declarativeAgent.json** y, después de
    conversation_starters, agregue una **coma**, presione Enter y pegue
    el siguiente arreglo:
    ```
    "capabilities": [  
        {  
            "name": "WebSearch"  
        }  
    ]  
    ```
    ![A screenshot of a computer program AI-generated content may be
    incorrect.](./media/image24.png)

2.  Seleccione **Provision** en el panel Lifecycle de **Microsoft 365
    Agents Toolkit** y verifique que se complete correctamente.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image25.png)

    El agente tendrá acceso a contenido web después de recargar la página.

3.  Pregunte al agente +++How can I build a declarative agent?+++ y
    observe que responde utilizando información web.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image26.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image27.png)

## Resumen
En este laboratorio, **creó** correctamente un **agente declarativo
poético** utilizando **Microsoft 365 Agents Toolkit**. Creó y
aprovisionó un agente básico, validó su integración con Microsoft 365
Copilot Chat y mejoró su comportamiento mediante instrucciones
personalizadas que transforman cada respuesta en un poema.

Además, mejoró la experiencia agregando conversation starters y
habilitando la búsqueda web, permitiendo al agente recuperar información
externa mientras mantiene su estilo poético. Este laboratorio demuestra
cómo los agentes declarativos pueden personalizarse mediante
configuración e instrucciones, sin necesidad de escribir código, para
ofrecer experiencias creativas y controladas en Microsoft 365 Copilot.
