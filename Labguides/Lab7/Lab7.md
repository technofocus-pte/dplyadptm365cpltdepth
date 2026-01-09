# Lab 6 – Crear un agente declarativo poético utilizando Microsoft 365 Agents Toolkit

**Objetivo  
**Un agente declarativo es una versión personalizada de Microsoft 365
Copilot que permite a los usuarios crear experiencias personalizadas
mediante la declaración de instrucciones, acciones y conocimientos
específicos. Esta guía proporciona información sobre cómo construir un
agente declarativo utilizando **Microsoft 365 Agents Toolkit** (una
evolución de Teams Toolkit).  
  
En este laboratorio, se creará un agente declarativo poético.

## Ejercicio 1: Crear un agente declarativo

En este ejercicio, se iniciará la creación de un agente declarativo
básico desde **Visual Studio Code**.

1.  Desde la máquina virtual, abra **Visual Studio Code**.

2.  Seleccione **Extensions** en el panel izquierdo y escriba
    +++Microsoft 365 Agents Toolkit+++.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.png)

3.  Seleccione **Microsoft 365 Agents Toolkit** y haga clic en
    **Install** para instalar la extensión.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.png)

4.  Seleccione la **extensión instalada**, haga clic en **Create a New
    Agent/App** y luego seleccione **Declarative Agent** de las opciones
    listadas.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.png)

5.  Seleccione **No Action** para crear un agente declarativo básico.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.png)

6.  Seleccione **Default folder** para almacenar la carpeta raíz del
    proyecto en la ubicación predeterminada.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.png)

7.  Ingrese +++**My Agent**+++ como nombre de la aplicación y presione
    **Enter**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.png)

8.  En la nueva ventana de Visual Studio Code que se abre, seleccione
    **Microsoft 365 Agents Toolkit**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.png)

9.  En el panel **Lifecycle**, seleccione **Provision** y luego haga
    clic en **Sign in** en el cuadro emergente para iniciar sesión en la
    cuenta de **Microsoft 365**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.png)

10. **Inicie sesión** utilizando las credenciales proporcionadas en la
    pestaña **Resources** y cierre la ventana una vez completado.

![A black background with white text AI-generated content may be
incorrect.](./media/image9.png)

11. En Visual Studio Code, verifique que la **provisión** se haya
    **completado correctamente.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.png)

12. El agente declarativo básico ha sido creado con éxito.

Tarea 1: Probar el agente  
En esta tarea se evaluará el funcionamiento del agente declarativo
creado.

1.  Navegue a la aplicación **Copilot** mediante la
    URL +++<https://m365.cloud.microsoft/chat+++>.

2.  En la esquina superior izquierda, **seleccione** el ícono del
    **conversation drawer**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.png)

3.  Seleccione el agente declarativo **My Agent**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.png)

4.  Ingrese la pregunta +++Hello! How can you help me?+++ y verifique
    que el agente responda: "Thanks for using Microsoft 365 Agents
    Toolkit to create your declarative agent!"

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image13.png)

En este ejercicio, se ha creado un agente declarativo básico y se ha
probado su funcionalidad.

Ejercicio 2: Agregar instrucciones  
En este ejercicio, se agregarán instrucciones al agente declarativo
creado y se mejorará su funcionalidad.

1.  Desde **Visual Studio Code**, abra el archivo
    **appPackage/instructions.txt** y reemplace su contenido por el
    siguiente texto:

> You are a declarative agent and were created with Microsoft 365 Agents
> Toolkit. You are an expert at creating poems.
>
> Every time a user asks a question, you must turn the answer into a
>
> poem. The poem must not use the quote markdown and use regular
>
> text.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.png)

(El contenido de este archivo se insertará en la propiedad instructions
del manifiesto del agente durante la provisión.).

2.  Seleccione **Provision** en el panel **Lifecycle** del **Agents
    Toolkit.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.png)

3.  Verifique que la **provisión** se haya completado **correctamente**
    (aparecerá un mensaje en la esquina inferior derecha de Visual
    Studio Code).

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.png)

4.  El agente declarativo utilizará las instrucciones actualizadas
    después de recargar la página.

5.  Actualice la página de chat, seleccione **My Agent** e ingrese:
    +++Do we have chocolate in our food catalog?+++.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image17.png)

6.  Observe que el agente genera una respuesta poética.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image18.png)

7.  Agregue iniciadores de conversación.

8.  Abra el archivo **appPackage/declarativeAgent.json** y, justo
    después del nodo **instructions**, agregue una coma, presione
    **Enter** y pegue el siguiente código:

> "conversation_starters": \[
>
> {
>
> "title": "Getting Started",
>
> "text": "How can I get started with Agents Toolkit?"
>
> },
>
> {
>
> "title": "Getting Help",
>
> "text": "How can I get help with Agents Toolkit?"
>
> }
>
> \]

![A screen shot of a computer AI-generated content may be
incorrect.](./media/image19.png)

9.  Seleccione **Provision** en el panel **Lifecycle** del **Microsoft
    365 Agents Toolkit** y verifique que la provisión se complete
    correctamente.

10. Los iniciadores de conversación actualizados estarán disponibles en
    su agente declarativo después de **recargar** la página.

11. **Recargue** la página de chat para confirmar la disponibilidad.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.png)

## Ejercicio 3: Agregar contenido web

En este ejercicio, se habilitará que el agente pueda buscar contenido
web.

1.  Abra el archivo **appPackage/declarativeAgent.json** y agregue el
    arreglo **capabilities** con el siguiente contenido:

> "capabilities": \[
>
> {
>
> "name": "WebSearch"
>
> }
>
> \]

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image21.png)

2.  Seleccione **Provision** en el panel **Lifecycle** del **Microsoft
    365 Agents Toolkit** y asegúrese de que la provisión se complete
    correctamente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image22.png)

El agente declarativo tendrá acceso a contenido web para generar sus
respuestas después de recargar la página.

3.  Pregunte al agente: +++How can I build a declarative agent?+++ y
    observe que el agente responde utilizando información web.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image23.png)

**Resumen**

En este laboratorio, usted ha aprendido a:

- Crear un agente declarativo para Microsoft 365 Copilot.

- Mejorar el agente con instrucciones personalizadas y contenido web.

- Probar la funcionalidad del agente en cada etapa de su creación.
