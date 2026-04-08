# Laboratorio 5 - Extender Microsoft 365 Copilot Chat con un agente de RR.HH. creado con Microsoft Copilot Studio

**Escenario  
Zava** Ltd. es una **empresa** global de servicios profesionales y
soluciones tecnológicas con una **fuerza laboral distribuida**. La
organización utiliza Microsoft 365, SharePoint y Power Platform para
gestionar operaciones de RR. HH., aprendizaje de empleados y datos de
reclutamiento.

Zava busca **mejorar la experiencia del empleado permitiendo** acceso
rápido y conversacional a información **relacionada con RR. HH**.
directamente dentro de **Microsoft 365 Copilot Chat**. Los empleados
consultan con frecuencia sobre **políticas de RR. HH**., oportunidades
de crecimiento profesional, rutas de aprendizaje y datos de
reclutamiento almacenados en sitios de SharePoint.

Para abordar esto, los equipos de IT y RR. HH. de Zava deciden crear un
**agente de RR. HH. dedicado** utilizando **Microsoft Copilot Studio**.
Este agente será definido de forma declarativa, alojado dentro de
Microsoft 365 Copilot Chat y enriquecido con conocimiento organizacional
almacenado en SharePoint. La solución debe construirse en un entorno
seguro y aislado de Power Platform e integrarse de forma fluida en la
experiencia de Microsoft 365.

**Objetivos**  
Al completar este laboratorio, aprenderá a:  
- Crear y administrar un entorno dedicado de **Power Platform para el
desarrollo de agentes**.  
- Crear un agente declarativo utilizando **Microsoft Copilot Studio**
para **Microsoft 365 Copilot Chat.  **
- Definir el propósito, tono y comportamiento **del agente** mediante
prompts en lenguaje natural.  
- Publicar e implementar el agente en **Microsoft 365 Copilot Chat**  
- Crear y configurar un **sitio de comunicación de SharePoint** para
alojar datos de **RR. HH**.  
- Agregar fuentes de conocimiento basadas en SharePoint a un agente de
Copilot Studio.  
- Probar la capacidad del **agente para recuperar** y razonar sobre
datos organizacionales estructurados dentro de **Copilot Chat**.

Duración estimada - 45 minutos

## Ejercicio 1: Crear un entorno de Power Platform

Con Power Platform, puede crear diferentes entornos y cambiar fácilmente
entre ellos según sus necesidades. Un entorno almacena aplicaciones,
flujos, datos, agentes, etc., y cada entorno está completamente aislado
de los demás. En este ejercicio, creará un nuevo entorno dedicado en el
que realizará los ejercicios restantes.

1.  Abra un navegador, vaya a +++https://admin.powerplatform.com+++ e
    inicie sesión utilizando las siguientes credenciales.  
    - Username - +++@lab.CloudPortalCredential(User1).Username+++  
    - Temporary Access Password -
    +++@lab.CloudPortalCredential(User1).TAP+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image1.png)

2.  Seleccione **Manage** y luego seleccione **+ New en
    Environments**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image2.png)

3.  Proporcione el Name como +++**Dev env**+++, seleccione el **Type**
    como **Developer** y haga clic en **Next**. Seleccione **Save** en
    la pantalla **Add Dataverse**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image3.png)  
    ![A screenshot of a web page AI-generated content may be
    incorrect.](./media/image4.png)

4.  El nuevo entorno se creará y cambiará de estado **Preparing** a
    **Ready** una vez que esté listo.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image5.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image6.png)

**Importante:** La **creación del entorno** tarda aproximadamente **10
minutos**, hasta un máximo de **15 minutos**. Espere ese tiempo y luego
**actualice** la pantalla para ver el entorno creado en el **Admin
Center**.

## Ejercicio 2: Crear un agente para Microsoft 365 Copilot Chat

En este ejercicio creará un agente declarativo con Microsoft Copilot
Studio y lo alojará en Microsoft 365 Copilot Chat.

1.  Inicie sesión en +++<https://copilotstudio.microsoft.com+++>
    utilizando las siguientes credenciales (también disponibles en la
    pestaña **Resources)**.  
    - Username - +++@lab.CloudPortalCredential(User1).Username+++  
    - Temporary Access Password -
    +++@lab.CloudPortalCredential(User1).TAP+++

2.  Seleccione **Get Started** en la pantalla **Welcome to Microsoft
    Copilot Studio**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image7.png)

3.  Seleccione **Skip** en la pantalla de bienvenida.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image8.png)

4.  Seleccione el entorno **Dev env** creado en el ejercicio anterior.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image9.png)

**Importante:** Si Copilot Studio no muestra la opción de seleccionar
**Environment** como en la captura, siga estos pasos:  
![A screenshot of a chat AI-generated content may be
incorrect.](./media/image10.png)  
Abra +++<https://admin.powerplatform.microsoft.com/>+++. Seleccione
**Manage → Environments → Dev env** y copie el valor de **Environment
ID**.  
![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.png)

Vuelva a la pestaña de Copilot Studio y abra
+++<https://copilotstudio.microsoft.com/environments/>\<
**EnvironmentID** \>+++ reemplazando \< **EnvironmentID** \> con el
valor obtenido.

5.  Para crear un agente declarativo para Microsoft 365 Copilot Chat,
    primero debe examinar la lista de agentes en Copilot Studio y luego
    seleccionar el agente con nombre **Microsoft 365 Copilot**.
    Seleccione **Got it** en la ventana emergente de actualización de
    versión.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image12.png)

6.  Seleccione **Agents** en la barra de navegación izquierda.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image13.png)

7.  Seleccione **Microsoft 365 Copilot** de la lista.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image14.png)

8.  Se abrirá una nueva sección de Microsoft Copilot Studio. Desde allí,
    seleccione el comando **+ Add** para crear un nuevo agente para
    Microsoft 365 Copilot Chat.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image15.png)

9.  Copilot Studio le pedirá describir en lenguaje natural el propósito
    del agente. **Pegue el siguiente prompt** y haga clic en **Send**:  
    +++You are an agent helping employees to find information about HR
    policies and procedures, about how to improve their career, and
    about how to define learning pathways.+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image16.png)

10. Cuando se le solicite, asigne el nombre "Agentic HR" al agente
    utilizando el siguiente prompt:  
    +++Name it as Agentic HR+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image17.png)

11. Indique tareas u objetivos específicos con la siguiente
    instrucción:  
    +++Emphasize everything that helps team building, inclusion, and the
    growth mindset+++  
    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image18.png)

12. Defina un tono profesional con la siguiente entrada:  
    +++It should have a professional tone+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image19.png)

13. Una vez completada la descripción, seleccione **Create** para crear
    el agente.  
    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image20.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image21.png)

## Ejercicio 3: Publicar el agente en Microsoft 365 Copilot Chat

1.  Seleccione **Publish** en la página de resumen del agente.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image22.png)

2.  Seleccione **Publish** en la pantalla **Publish agent**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image23.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image24.png)

3.  Seleccione **Copy** en **Share link** para copiar el enlace y luego
    seleccione **Done**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image25.png)

4.  Abra una nueva pestaña, pegue la URL copiada y seleccione **Add**
    para agregar el agente **Agentic HR** a su lista de agentes.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image26.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image27.png)

5.  Seleccione **Skip** en la pantalla de introducción.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image28.png)

6.  El agente **Agentic HR** ahora está agregado. Selecciónelo en el
    panel de navegación izquierdo.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image29.png)

## Ejercicio 4: Crear un sitio de SharePoint

1.  En un nuevo navegador, vaya a
    +++<https://m365.cloud.microsoft/chat/>++ seleccione **Apps** en el
    panel izquierdo y luego seleccione **SharePoint** cuando se carguen
    las aplicaciones.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image30.png)

2.  Seleccione **+ Create site** en la página de SharePoint.  
    ![A screenshot of a browser AI-generated content may be
    incorrect.](./media/image31.png)

3.  Seleccione **Communication site** en la página **Select the site
    type**.  
    ![A screenshot of a web page AI-generated content may be
    incorrect.](./media/image32.png)

4.  Seleccione una **plantilla**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image33.png)

5.  Seleccione **Use template**.  
    ![A screenshot of a website AI-generated content may be
    incorrect.](./media/image34.png)

6.  Introduzca +++Contoso site2-@lab.LabInstance.Id+++ como **Site
    name** y seleccione **Next.**  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image35.png)

7.  En la siguiente pantalla, seleccione **Create site**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image36.png)

8.  Una vez creado, anote la **URL** del sitio.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image37.png)

9.  Seleccione **Documents** en la barra de menú. Seleccione **+ Create
    or upload → Files upload**
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image38.png)
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image39.png)
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image40.png)

10. Seleccione el archivo **Sample-list-of-candidates.xlsx** desde
    **C:\LabFiles** para cargarlo. Una vez cargado, haga clic en los
    tres puntos junto al documento, seleccione **Copy link** y guarde el
    enlace en un bloc de notas.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image41.png)

## Ejercicio 5: Agregar conocimiento al agente

En este ejercicio agregará conocimiento desde SharePoint al agente
creado.

1.  En Copilot Studio, desde la página principal **del agente**,
    seleccione **+ Add knowledge** en la sección Knowledge.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image42.png)

2.  Seleccione **SharePoint,** introduzca la **URL** del archivo cargado
    y seleccione **Add.  **
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image43.png)

3.  Seleccione **Add to agent** en la siguiente pantalla.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image44.png)

4.  Seleccione **Publish** para publicar el agente.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image45.png)

5.  Seleccione **Publish** nuevamente.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image46.png)

6.  Copie la **URL** y ábrala en un navegador.  
    ![A screenshot of a computer program AI-generated content may be
    incorrect.](./media/image47.png)

7.  Esta vez aparecerá la opción **Update now**. Selecciónela.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image48.png)

8.  Seleccione **Open** una vez actualizado.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image49.png)

**Alerta:** Puede que deba interactuar con el agente para obtener los
resultados esperados.

9.  En la pantalla del **agente Agentic HR**, envíe el siguiente
    mensaje:  
    +++Show me a list of candidates for HR with role "HR Director" or
    "HR Manager"+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image50.png)

    **Importante:** Si se solicita aprobación, realice los siguientes pasos.
    De lo contrario, puede omitirlos.  
    En el mensaje Data to be shared with Agentic HR, seleccione **Allow
    once** (si se solicita).  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image51.png)  
    Si se le pide iniciar sesión, seleccione **Sign in** **to Agentic HR** y
    luego **Connect** en la siguiente pantalla.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image52.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image53.png)

    Seleccione **Submit** una vez conectado.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image54.png)  
    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image55.png)

    Vuelva a enviar el mensaje:  
    +++Show me a list of candidates for HR with role "HR Director" or "HR
    Manager"+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image56.png)

10. Recibirá la lista solicitada  
    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image57.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image58.png)

**Resumen**  
En este laboratorio, extendió correctamente Microsoft 365 Copilot Chat
creando un agente declarativo Agentic HR con Microsoft Copilot Studio.
Configuró un entorno dedicado de Power Platform, diseñó y publicó un
agente enfocado en RR. HH. e integró la solución en la experiencia de
Microsoft 365.

También creó un sitio de comunicación de SharePoint, cargó contenido
relacionado con RR. HH. y lo conectó como fuente de conocimiento para el
agente. Finalmente, validó la solución consultando el agente en Copilot
Chat y obteniendo respuestas contextualizadas basadas en SharePoint.

Este laboratorio demuestra cómo Copilot Studio permite a las
organizaciones crear agentes específicos de dominio que aprovechan de
forma segura el conocimiento empresarial y mejoran la productividad
mediante IA conversacional en Microsoft 365.
