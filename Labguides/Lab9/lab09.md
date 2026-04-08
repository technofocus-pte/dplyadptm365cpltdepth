# Laboratorio 8 - Optimizar las operaciones de soporte de IT con un agente autónomo de Copilot usando Copilot Studio

**Tiempo estimado: 60 minutos**

**Objetivo  **
El objetivo de este laboratorio es permitir a los participantes
optimizar las operaciones de soporte de IT en Contoso Solutions mediante
la creación de un agente autónomo de Copilot. Los participantes
aprenderán a configurar Microsoft Copilot Studio, configurar el agente
de soporte de IT, integrar Power Apps y Dataverse, mejorar las
capacidades del bot con una base de conocimiento y automatizar la
creación de tickets utilizando Power Automate. Este laboratorio práctico
proporcionará a los usuarios las habilidades necesarias para mejorar los
flujos de trabajo de IT, reducir el esfuerzo manual y aumentar la
eficiencia del soporte.

**Solución**  
Los participantes crearán un agente de soporte de IT personalizado de
Contoso utilizando Microsoft Copilot Studio, lo configurarán para
manejar problemas comunes de IT y lo integrarán con Dataverse para
almacenar datos de soporte. Configurarán un entorno de desarrollo,
agregarán fuentes de conocimiento y refinarán los flujos de conversación
del bot para mejorar la interacción con el usuario. Aprovechando Power
Apps, los participantes crearán una tabla de Dataverse para gestionar
los registros de soporte de IT. Utilizando Power Automate, automatizarán
la creación de tickets y las notificaciones por correo electrónico para
problemas no resueltos. Finalmente, los participantes probarán el agente
para validar la precisión en la resolución de problemas y la
automatización del flujo de trabajo, garantizando operaciones de soporte
de IT sin interrupciones.

## Ejercicio 1: Introducción a Power Apps  
Este ejercicio introduce a los participantes en Power Apps y Dataverse.
El objetivo es iniciar sesión en Power Apps, configurar un entorno de
trabajo y crear una tabla de Dataverse importando datos desde un archivo
de Excel. Los participantes aprenderán habilidades esenciales para
trabajar con aplicaciones basadas en datos.

### Tarea 1: Iniciar sesión en Power Apps

1.  Navegue al sitio web de Power Apps
    +++<https://www.microsoft.com/en-us/power-platform/products/power-apps>+++
    y haga clic en el botón **Try for Free**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image1.png)

2.  Ingrese +++@lab.CloudPortalCredential(User1).Username+++. Seleccione
    la **casilla de verificación** y haga clic en el botón **Start
    free**. Seleccione el país de origen.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image2.png)

3.  Ingrese el Temporary Access Pass
    +++@lab.CloudPortalCredential(User1).TAP+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image3.png)

4.  Seleccione **Get Started**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image4.png)

### Tarea 2: Actualizar la configuración del entorno Developer

1.  Desde una nueva pestaña en el navegador, abra Power Platform admin
    center - +++<https://admin.powerplatform.microsoft.com/home>+++ e
    inicie sesión usando sus credenciales si se le solicita.  
    - +++@lab.CloudPortalCredential(User1).Username+++  
    - +++@lab.CloudPortalCredential(User1).AccessToken+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image5.png)

2.  Seleccione **Manage** en el panel izquierdo y seleccione **+ New**
    en **Environments**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image6.png)

3.  Proporcione el nombre del entorno como +++Dev One+++ y seleccione el
    tipo como **Developer** y seleccione **Next**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image7.png)

4.  Seleccione **Save** en el cuadro de diálogo **Add Dataverse**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image8.png)

5.  Una vez que el entorno esté **Ready**, seleccione el entorno creado
    **Dev One**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image9.png)

6.  Haga clic en **Edit** para editar la configuración.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image10.png)

7.  En el panel Edit, active **Administration mode** en **ON** y
    seleccione **Save**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image11.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image12.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image13.png)

8.  Una vez guardados los cambios, seleccione **Settings**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image14.png)

9.  Seleccione **Product - Features**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image15.png)

10. En **Features**, active **Dataverse search**, seleccione **Save**,
    luego active la opción **Single table search** y seleccione
    **Save**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image16.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image17.png)

### Tarea 3: Configurar una tabla de Dataverse

1.  Navegue nuevamente a la **página de PowerApps** y seleccione el
    entorno **DevOne** de la lista de entornos.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image18.png)

2.  Desde la barra de navegación izquierda seleccione **Tables**. En la
    barra superior de la sección de tablas, haga clic en **+ New table**
    y luego seleccione **Create new tables**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image19.png)

3.  Seleccione la opción **Import an Excel file or CSV** para crear una
    nueva tabla.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image20.png)

4.  Haga clic en la opción **Select form device** y seleccione el
    archivo **Excel Support Ticket** desde
    **C:\LabFiles\Labfiles\Autonomous agent**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image21.png)

5.  Seleccione **Import** en la siguiente pantalla.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image22.png)

6.  Seleccione la tabla y haga clic en **View data** para ver los
    datos.  
    **Nota:** En este caso, la tabla se llama *Employee Support Ticket*.
    El nombre puede variar en cada ejecución. Guarde el nombre de la
    tabla para referencia futura. El nombre de las columnas también
    puede variar.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image23.png)

7.  Vaya a los datos de la tabla, seleccione el menú desplegable junto
    al campo **Issue Description**, seleccione **Edit column**,
    configure el tipo de dato como **Text** **Multiple line** **Plain
    Text** y haga clic en **Update**. El nombre de la columna puede
    variar.  
    El nombre de la **columna puede ser ligeramente diferente,** pero
    será similar a la descripción del problema, ya que es generado por
    Copilot.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image24.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image25.png)

8.  Seleccione el menú desplegable junto al campo **Ticket Status**,
    seleccione **Edit column**, configure Choices como +++Unresolved+++,
    +++Resolved+++, +++Processing+++. Configure Default choice como
    **Unresolved** y haga clic en **Update**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image26.png)

9.  En la parte superior derecha haga clic en **Save and exit** para
    guardar la tabla.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image27.png)

### Tarea 4: Agregar un archivo a OneDrive

1.  Desde la parte superior izquierda de la página de Power Apps,
    seleccione el menú y seleccione **OneDrive**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image28.png)

2.  Seleccione **My files - + Create or upload**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image29.png)

3.  Seleccione **Files upload**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image30.png)

4.  Elija **IT Support.xlsx** desde **C:\LabFiles\Labfiles**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image31.png)

5.  Este archivo se utilizará en un ejercicio posterior.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image32.png)

## Conclusión  
Al completar este ejercicio, los participantes aprenderán:  
- Cómo acceder y navegar en Power Apps utilizando credenciales de Office
365 admin tenant.  
- Los pasos para crear y configurar una tabla de Dataverse importando
datos.  
- Conocimiento práctico sobre la configuración de un entorno para
soportar flujos de desarrollo de aplicaciones.

## Ejercicio 2: Crear el agente de soporte de IT de Contoso  
Este ejercicio se centra en iniciar sesión en Microsoft Copilot Studio y
crear un agente de Copilot personalizado para operaciones de soporte de
IT en Contoso. Los participantes adquirirán experiencia práctica
navegando en Copilot Studio, configurando entornos y creando un agente
impulsado por IA para optimizar flujos de trabajo de IT.

### Tarea 1: Crear y configurar el agente de soporte de IT de Contoso

1.  Desde una nueva pestaña, inicie sesión en
    +++<https://copilotstudio.microsoft.com>+++ usando sus credenciales.
    Seleccione **Get Started**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image33.png)

2.  Seleccione **Skip** en la ventana emergente de bienvenida.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image34.png)

3.  En la sección principal de Copilot Studio, en la parte superior
    derecha, seleccione el **entorno** y elija **DevOne**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image35.png)

    **Importante:** Si Copilot Studio no muestra la opción para seleccionar
    **Environment** como en la captura, siga estos pasos.  
    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image36.png)

    Abra +++<https://admin.powerplatform.microsoft.com/>+++. Seleccione
    **Manage -\> Environments -\> Dev env** y seleccione el valor de
    **Environment ID**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image37.png)

    Regrese a la pestaña de Copilot Studio y abra
    +++<https://copilotstudio.microsoft.com/environments/>\< EnvironmentID
    \>+++ (reemplace \< **EnvironmentID** \> con el valor obtenido).

4.  Seleccione **Create an agent**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image38.png)

5.  Seleccione **Edit**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image39.png)

6.  Ingrese **Name** y **Description** como se indica y seleccione
    **Save**.  
    **Name**: +++Contoso IT Support Agent+++  
    **Description** (seleccione **Copy** y **pegue** en el campo
    **Description**):  
    Create a Contoso IT Support Agent which transforms IT support at
    Contoso Solutions by providing instant troubleshooting for common
    issues, automating ticket creation for unresolved problems, and
    storing all interactions in Dataverse. This solution enhances
    response times, reduces manual workloads, and boosts employee
    productivity.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image40.png)

7.  Seleccione **Edit** en Instructions para agregar instrucciones al
    agente.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image41.png)

8.  Ingrese la **instrucción** y seleccione **Save**.  
    **Instrucción** (seleccione **Copy** y **pegue** en el campo
    **Instruction**):  
    Create the Copilot Agent and configure it to handle IT support
    operations. Add a knowledge source containing solutions for common
    IT issues like hardware troubleshooting, connectivity, and software
    glitches. Set up a trigger to detect updates to a OneDrive file
    describing unresolved issues. Create an action to save these
    technical issues into a Dataverse table, ensuring all details are
    stored for tracking and reporting. Test the agent to validate its
    troubleshooting accuracy and ticket automation workflow
    before deployment.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image42.png)

9.  Desde la esquina superior derecha del agente, haga clic en
    **Settings**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image43.png)

10. Desplácese hacia abajo y desactive **Use general knowledge** en la
    sección **Knowledge** y luego haga clic en **Save**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image44.png)

11. Una vez **guardado**, cierre el panel **Settings**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image45.png)

## Conclusión 
Al completar este ejercicio, los participantes aprenderán:  
- Cómo acceder y configurar Microsoft Copilot Studio.  
- Los pasos para crear y configurar un agente de Copilot
personalizado.  
- Habilidades prácticas para habilitar IA generativa y configuraciones
de orquestador en el agente.  
-Formas de mejorar operaciones de IT automatizando la creación de
tickets y utilizando IA para la resolución de problemas.

## Ejercicio 3: Mejorar las capacidades del bot  
Este ejercicio se centra en mejorar las capacidades del agente de
soporte de IT de Contoso agregando una base de conocimiento y
personalizando los temas del bot para mejorar la interacción. Los
participantes refinarán las respuestas del bot y garantizarán que asista
eficazmente a los usuarios en la resolución de problemas y escalamiento.

### Tarea 1: Agregar base de conocimiento

1.  En la página de resumen del agente Contoso, desplácese hacia abajo y
    haga clic en **+ Add Knowledge**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image46.png)

2.  Seleccione **Upload file** para agregar el archivo **Contoso Common
    IT Issue.docx** desde **C:\LabFiles\Labfiles\Autonomous agent** y
    luego haga clic en **Add to agent**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image47.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image48.png)

3.  Nuevamente, vaya a la página de resumen del agente, desplácese hacia
    abajo y haga clic en **+ Add knowledge**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image49.png)

4.  Seleccione **Dataverse** como fuente de datos.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image50.png)

5.  Busque +++Employee+++, seleccione la tabla **Employee Support
    Ticket** y luego haga clic en **Add to agent**.  
    El **nombre de la tabla puede ser diferente**. Intente buscar
    +++Support Ticket+++ si es necesario.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image51.png)

    **Importante:** Desde la página Knowledge, asegúrese de que la fuente de
    conocimiento se haya cargado correctamente. Esto puede tardar entre 10 y
    30 minutos.

## Tarea 2: Personalizar el tema Fallback

1.  En la barra superior seleccione **Topics**, luego **System** y abra
    **Fallback**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image52.png)

2.  Desplácese hacia abajo hasta el nodo de mensaje y actualice el
    mensaje como se indica:  
    +++I'm sorry. This information is not available in my system. You
    can raise the support ticket via mail for this issue. +++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image53.png)

3.  En la parte superior derecha haga clic en **Save** para guardar el
    tema.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image54.png)

## Conclusión

Al completar este ejercicio, los participantes aprenderán:  
- Cómo cargar e integrar una base de conocimiento para mejorar la
funcionalidad del bot.  
- Pasos para personalizar mensajes iniciales de conversación.  
- Técnicas para actualizar respuestas fallback para manejar consultas no
soportadas.

## Ejercicio 4: Probar el agente  
Este ejercicio guía a los participantes a través de la prueba del agente
de soporte de IT de Contoso para validar su funcionalidad. Los
participantes verificarán cómo el bot maneja los prompts utilizando la
base de conocimiento y los temas de fallback para garantizar una
interacción y escalamiento sin interrupciones.

1.  Desde la esquina superior derecha haga clic en **Test**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image55.png)

2.  Ingrese el prompt +++My printer is not working how to fix it+++ y
    observe la respuesta basada en la base de conocimiento.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image56.png)

## Conclusión 
Al completar este ejercicio, los participantes aprenderán:  
- Cómo probar y activar un agente de IA.  
- Validar la capacidad del bot para responder con base en conocimiento.

## Ejercicio 5: Automatizar la creación de tickets con Power Automate  
Este ejercicio demuestra cómo automatizar la creación de tickets de
soporte utilizando AgentFlow e integrarlo con el agente de soporte de IT
de Contoso. Los participantes crearán un flujo para optimizar el
registro de incidencias y almacenar datos en Dataverse.

1.  Seleccione **Flows** desde el menú izquierdo.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image57.png)

2.  Seleccione **+ New agent flow**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image58.png)

3.  Busque y seleccione +++**When an agent calls the flow**+++ en
    **Skills**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image59.png)

4.  Seleccione **Add an Input**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image60.png)

5.  Seleccione **Text** y nombre la entrada +++Name+++.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image61.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image62.png)

6.  Con el mismo procedimiento, cree más entradas según los detalles
    indicados a continuación:  
      
    **Introduzca el nombre** **Tipo de datos**  
    +++ID+++ (Text)  
    +++Email+++ (Text)  
    +++Details+++ (Text)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image63.png)

7.  Debajo de **When an agent calls the flow**, haga clic en el signo
    (**+**) para **Add an action**.  
    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image64.png)

8.  En la barra de búsqueda de Add an action, ingrese +++**Add a new
    row**+++. Luego seleccione Add a new row en la sección de Microsoft
    Dataverse.  
    ![A screenshot of a computer program AI-generated content may be
    incorrect.](./media/image65.png)

    **Nota:** En ocasiones, una conexión de Dataverse no se crea
    automáticamente. Es posible que necesite iniciar sesión nuevamente con
    sus credenciales mediante autenticación **OAuth**. Si se requiere un
    nombre de conexión, asígnelo como +++connect1+++. El navegador también
    puede bloquear la ventana emergente inicial; permita su ejecución desde
    la esquina derecha de la barra de direcciones.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image66.png)

9.  En la sección **Table Name**, busque y seleccione +++Employee
    Support Ticket+++ (o el nombre de tabla correspondiente que haya
    creado).  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image67.png)

10. Debajo de **Table Name**, seleccione **Show all**, luego haga clic
    en el campo correspondiente y agregue input con la ayuda del botón
    **dynamic content**.  
      
    Configure el campo **Current Status** como **Unresolved**

    **Sección** **Variable de entrada**  
    Employee Name → Nombre (Entrada dinámica)  
    Email Address → Correo electrónico (Entrada dinámica)  
    Employee ID → ID (Entrada dinámica)  
    Descripción del problema técnico→ Detalles (Entrada dinámica)
    ![A blue
    line on a white background AI-generated content may be
    incorrect.](./media/image68.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image69.png)

11. Desde la barra superior, haga clic en **Save draft** y luego en
    **Publish. Cierre** la pestaña de Power Automate.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image70.png)

12. Vaya a **Overview**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image71.png)

13. Seleccione **Edit** en **Details**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image72.png)

14. Nombre el flujo +++Create an Employee Support Ticket+++ y seleccione
    **Save**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image73.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image74.png)

15. Desde la página **Overview del agente Contoso IT Support Agent**,
    **seleccione + Add tool**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image75.png)

16. Seleccione **Flows** y agregue **Create an Employee Support
    Ticket**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image76.png)

17. Seleccione **Add and configure**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image77.png)

18. Asegúrese de que la **tool** esté agregada **al agente**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image78.png)

## Conclusión  
Al completar este ejercicio, los participantes aprenderán:

- Cómo integrar Agent flows con un agente de Copilot para la creación de
  tickets.

- Pasos para recopilar y mapear datos de entrada dinámicamente a partir
  de interacciones de usuario.

- Técnicas para automatizar notificaciones por correo electrónico para
  la escalación de problemas técnicos.

- La capacidad de configurar flujos de trabajo para una gestión
  eficiente de tickets de soporte.

## Ejercicio 6: Configurar un trigger para acciones automáticas  
  
Esta continuación de la automatización de la creación de tickets de
soporte se centra en configurar un trigger en el agente de soporte de IT
de Contoso. Cree un Team y un Support Channel en MS Teams. Cuando se
publique un mensaje en el Support Channel, el trigger debe activarse.
Los participantes configurarán triggers y finalizarán el agente para su
implementación.

1.  Abra un navegador y abra Teams +++<https://teams.microsoft.com/>+++
    en él. Inicie sesión si se le solicita.

2.  Seleccione **New items → New Team**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image79.png)

3.  Ingrese los siguientes detalles y seleccione **Create:**  
    Team name: +++Support Team+++  
    Description: +++This is a team to post about support requests.+++  
    Channel: +++Support Channel+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image80.png)

4.  Seleccione **Skip** en la pantalla Add members.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image81.png)

5.  Desde la página Overview del agente en Copilot Studio, desplácese
    hacia abajo y haga clic en **+ Add trigger**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image82.png)

6.  Seleccione el **trigger When a new channel message is added** y haga
    clic en **Next**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image83.png)

7.  Una vez que el establecimiento de la conexión sea exitoso,
    seleccione **Next**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image84.png)

8.  Seleccione los siguientes valores y seleccione Create trigger.  
    Team - **Support Team** 
    Channel - **Support Channel**   
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image85.png)

9.  **Cierre** el cuadro de diálogo Time to test your trigger.  
    ![A screenshot of a computer error AI-generated content may be
    incorrect.](./media/image86.png)

10. **Publique** el agente seleccionando el botón **Publish** desde la
    esquina superior derecha.

11. Desde la página **Overview** del agente, seleccione los tres puntos
    junto al trigger agregado - **When a new channel message is added**
    y seleccione **Edit in Power Automate.**
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image87.png)

12. Seleccione el símbolo + debajo del nodo **When a new channel message
    is added** para agregar una acción. En el panel Action, busque
    +++**Get a row**+++ y seleccione **Get a row en Excel Online
    (Business).**  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image88.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image89.png)

13. Una vez que la acción esté agregada, agregue los siguientes detalles
    en ella.

    - Location - Seleccione OneDrive for Business

    - Document Library – OneDrive

    - File - ITSupport.xlsx

    - Table - Table1

    - Key Column – ID

    - Key Value - +++ID1234+++

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image90.png)

14. Seleccione el nodo **Sends a prompt to the specified copilot for
    processing**.

    En Body/message, ingrese +++Run the flow Create an Employee Support
    Ticket+++ luego, agregue los valores dinámicos Name, ID, Email ID,
    Description y Status. Luego +++agregue junto con un mensaje "New record
    added to the Employee Support table"+++  
    Debe verse similar al que se muestra en la captura a continuación.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image91.png)

15. **Guarde** el flujo

## Ejercicio 7: Pruebe el agente

1.  Desde el flujo de Power Automate **When a new channel message is
    added**, seleccione **Test**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image92.png)

2.  Seleccione **Manually → Test**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image93.png)

3.  Abra Teams y seleccione **Post in channel** en el **team Support
    Channel**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image94.png)

4.  Ingrese un mensaje y seleccione **Post**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image95.png)

5.  De vuelta en la página de Power Automate, puede ver que el flujo ha
    iniciado su ejecución y se ha completado correctamente.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image96.png)

6.  Desde la página Overview del agente, seleccione el ícono **Test
    Trigger**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image97.png)

7.  Seleccione el trigger más reciente y seleccione **Start testing**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image98.png)

8.  Ejecuta el flujo, obtiene los datos del Support tracker y los
    actualiza en la tabla de Dataverse.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image99.png)  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image100.png)

9.  En este caso, hay un detalle de ticket de soporte en el tracker, el
    cual se agrega a la tabla de Dataverse, creando así un ticket de
    soporte para el usuario.

## Conclusión final de la guía del laboratorio

Esta guía de laboratorio proporcionó a los participantes una experiencia
práctica en la implementación de un agente autónomo de Copilot para la
mesa de servicio de soporte de IT de Contoso Solutions. Al seguir los
ejercicios paso a paso, los participantes pudieron:

1.  **Configurar Copilot Studio:** Los participantes aprendieron a
    iniciar sesión en Copilot Studio, crear y configurar el agente de
    soporte de IT, y habilitar configuraciones esenciales como IA
    generativa y orquestador para una resolución de problemas efectiva y
    automatización de tickets.

2.  **Navegar Power Apps:** Los participantes adquirieron conocimiento
    práctico al iniciar sesión en Power Apps, configurar una tabla de
    Dataverse e importar datos desde Excel para rastrear y gestionar
    tickets de soporte de manera eficiente.

3.  **Mejorar las capacidades del bot:** Los ejercicios se centraron en
    agregar una base de conocimiento al bot, personalizar el inicio de
    conversación y los temas de fallback para mejorar la interacción con
    el usuario, y garantizar que el bot pudiera manejar una amplia gama
    de escenarios de soporte de IT.

4.  **Automatizar tareas de soporte de IT:** Los participantes también
    aprendieron cómo automatizar la creación de tickets de soporte
    utilizando Power Automate, mejorando la capacidad del bot para
    gestionar problemas no resueltos y optimizar los flujos de trabajo
    del equipo de IT.

Al completar estos ejercicios, los participantes pudieron implementar un
sistema de soporte autónomo robusto que mejora los tiempos de respuesta,
reduce la carga de trabajo manual y aumenta la productividad general en
las operaciones de soporte de IT. La integración de Copilot Studio,
Power Apps y Dataverse garantiza un flujo de información sin
interrupciones, automatiza tareas rutinarias y optimiza los flujos de
trabajo de soporte, proporcionando soluciones inmediatas de resolución
de problemas a los empleados y gestión automatizada de tickets para
problemas no resueltos.
