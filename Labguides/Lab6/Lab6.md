# Laboratorio 5 - Extender Microsoft 365 Copilot Chat con un agente de RR. HH. creado mediante Microsoft Copilot Studio

**Objetivo**

En este laboratorio, se explicará cómo extender **Microsoft 365
Copilot** Chat mediante la creación e integración de un **agente
declarativo personalizado** utilizando **Microsoft Copilot Studio.** Se
configurará el entorno, se diseñará y publicará un nuevo agente de
**asistencia para RR. HH**., y se enriquecerá con conocimiento
organizacional desde **SharePoint**.

Al finalizar este laboratorio, se comprenderá cómo conectar agentes de
Copilot Studio con Microsoft 365 Copilot para ofrecer respuestas
contextuales, específicas de la organización, y automatizar consultas
relacionadas con RR. HH.

**Duración estimada** – 45 minutos

## Ejercicio 1: Crear un entorno de Power Platform

Con Power Platform, es posible crear distintos entornos y cambiar entre
ellos según sea necesario. Un entorno almacena aplicaciones, flujos,
datos, agentes, etc., y cada entorno es completamente independiente. En
este ejercicio, se creará un entorno dedicado en el que se completarán
los ejercicios restantes.

1.  Abra un explorador y, utilizando las credenciales del **Resources**
    tab, vaya
    a +++[https://admin.powerplatform.com+++](https://admin.powerplatform.com+++/).

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.png)

2.  Seleccione **Manage** y luego seleccione **+ New** en
    **Environments.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.png)

3.  Ingrese el **Name** como +++**Dev env**+++, seleccione **Type** como
    **Developer** y haga clic en **Next**. Seleccione **Save** en la
    pantalla **Add Dataverse.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.png)

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image4.png)

4.  El nuevo entorno se creará y cambiará de **Preparing** a **Ready**
    cuando esté disponible.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.png)

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image6.png)

## Ejercicio 2: Crear un agente para Microsoft 365 Copilot Chat

En este ejercicio, se creará un agente declarativo con Microsoft Copilot
Studio y se alojará en Microsoft 365 Copilot Chat.

1.  Inicie sesión en
    +++[https://copilotstudio.microsoft.com+++](https://copilotstudio.microsoft.com+++/) utilizando
    las credenciales de la pestaña **Resources**.

![](./media/image7.png)

2.  Seleccione **Get Started** en la pantalla **Welcome to Microsoft
    Copilot Studio**.

3.  Seleccione el entorno **Dev env** que fue creado en el ejercicio
    anterior.

![](./media/image8.png)

\[!Alerta\] **Importante:** Si Copilot Studio no muestra la opción para
seleccionar **Environment,** siga los pasos indicados:

> ![](./media/image9.png)

Abra +++<https://admin.powerplatform.microsoft.com/+++>. Seleccione
**Manage → Environments → Dev env** y copie el **Environment ID**.

![](./media/image10.png)

Regrese a la pestaña de Copilot Studio y abra:
+++<https://copilotstudio.microsoft.com/environments/>\< EnvironmentID
\>+++ (Reemplace \<**EnvironmentID**\> con el valor obtenido).

4.  Para crear un agente declarativo para Microsoft 365 Copilot Chat,
    primero revise la lista de agentes en Copilot Studio y seleccione
    **Microsoft 365 Copilot**.

5.  Seleccione **Agents** en la barra de navegación izquierda y
    seleccione **Microsoft 365 Copilot**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.png)

6.  Se abrirá una nueva sección de Microsoft Copilot Studio. Seleccione
    **+ Add** para crear un nuevo agente para **Microsoft 365 Copilot
    Chat**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.png)

7.  Copilot Studio solicita describir en lenguaje natural el propósito
    del agente. Es posible definir los requisitos del agente. Pegue el
    siguiente prompt para hacerlo:

**+++You are an agent helping employees to find information about HR
policies and procedures, about how to improve their career, and about
how to define learning pathways.+++**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.png)

8.  Cuando Copilot Studio lo solicite, asigne el nombre **Agentic HR**
    al agente personalizado. Use el siguiente prompt:

+++Name it as Agentic HR+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.png)

9.  Luego, indique tareas u objetivos específicos proporcionando la
    siguiente instrucción:

**+++Emphasize everything that helps team building, inclusion, and the
growth mindset+++**

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image15.png)

10. Defina un tono profesional para su agente con la siguiente entrada:

\*\*+++It should have a professional tone+++\*\*

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.png)

11. Una vez finalizada la descripción, seleccione **Create** para crear
    el agente. 

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image17.png)

> ![](./media/image18.png)

## Ejercicio 3: Publicar el agente en Microsoft 365 Copilot Chat

1.  Seleccione **Publish** desde la página de información general del
    agente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.png)

2.  Seleccione **Publish** nuevamente en la pantalla **Publish agent**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image20.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image21.png)

3.  Seleccione **Copy** en **Share link** para copiar el enlace y luego
    seleccione **Done**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image22.png)

4.  Abra una nueva pestaña, pegue la URL copiada y seleccione **Add**
    para agregar **Agentic HR** a su lista de agentes.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image23.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image24.png)

5.  Seleccione **Skip** en la pantalla de introducción.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image25.png)

6.  El agente **Agentic HR** queda agregado.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image26.png)

## Ejercicio 4: Crear un sitio de SharePoint

1.  En un nuevo explorador, navegue a
    +++<https://m365.cloud.microsoft/chat/+++> Seleccione **Apps** y
    luego seleccione **SharePoint** cuando carguen las aplicaciones.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image27.png)

2.  Seleccione **+ Create site**.

![A screenshot of a browser AI-generated content may be
incorrect.](./media/image28.png)

3.  En **Select the site type**, seleccione **Communication site**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image29.png)

4.  Seleccione una plantilla a utilizar.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image30.png)

5.  Seleccione **Use template**.

![A screenshot of a website AI-generated content may be
incorrect.](./media/image31.png)

6.  Ingrese +++**Contoso site**+++ como **Site name** y seleccione
    **Next.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image32.png)

7.  En la siguiente pantalla, seleccione **Create site**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image33.png)

8.  Una vez creado, anote la **URL** del sitio.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image34.png)

9.  Seleccione **Documents** en la barra de menú. Luego, seleccione
    **Upload → Files.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image35.png)

10. Seleccione el archivo **Sample-list-of-candidates.xlsx** desde
    **C:\LabFiles**. Copie y guarde la URL completa.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image36.png)

## Ejercicio 5: Agregar conocimiento al agente

En este ejercicio, se agregará al agente el conocimiento proveniente del
sitio de SharePoint creado.

1.  Desde la página principal del **agente**, seleccione **+ Add
    knowledge** en la sección **Knowledge.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image37.png)

2.  Seleccione **SharePoint** e ingrese la **URL** de la carpeta
    **Documents** guardada previamente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image38.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image39.png)

3.  Nómbrelo como +++**HR Document**+++ y seleccione **Add to agent.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image40.png)

4.  Ahora estará disponible en estado **Ready** en la sección
    **Knowledge**.

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image41.png)

5.  Seleccione **Publish** para publicar el agente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image42.png)

6.  Seleccione nuevamente **Publish**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image43.png)

7.  Copie la **URL** y ábrala en un **explorador**.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image44.png)

8.  En esta ocasión, se mostrará la opción **Update now** dado que ya se
    encuentra agregado. Selecciónela.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image45.png)

9.  Seleccione **Open** una vez actualizado.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image46.png)

10. En la pantalla del agente **Agentic HR**, envíe el siguiente
    mensaje:

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image47.png)

11. En el mensaje **Data to be shared with Agentic HR**, seleccione
    **Allow once** (si es solicitado).

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image48.png)

12. Si se requiere iniciar sesión, seleccione **Sign in to Agentic HR**
    y luego seleccione **Connect** en la siguiente pantalla.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image49.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image50.png)

13. Seleccione **Submit** una vez conectado.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image51.png)

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image52.png)

14. Vuelva a enviar el siguiente mensaje al agente:

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image53.png)

15. Recibirá la lista solicitada.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image54.png)

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image55.png)

**Resumen**

En este laboratorio, se extendió **Microsoft 365 Copilot Chat** mediante
un **agente personalizado de RR. HH**. creado en **Microsoft Copilot
Studio**. Se creó un entorno dedicado en Power Platform, se diseñó y
publicó un agente declarativo (*Agentic HR*) y se integró con Microsoft
365 Copilot Chat. También se agregó conocimiento desde un sitio de
SharePoint para enriquecer las respuestas del agente.

Durante este ejercicio, se aprendió a:

- Crear y administrar entornos de Power Platform.

- Diseñar y publicar agentes declarativos en Microsoft Copilot Studio.

- Integrar agentes con Microsoft 365 Copilot Chat.

- Extender capacidades del agente mediante la conexión a fuentes de
  datos organizacionales como SharePoint.

Este ejercicio fundamental demuestra cómo las organizaciones pueden
**personalizar la experiencia de Microsoft 365 Copilot** con
inteligencia específica del dominio y con integración de conocimiento
corporativo.
