# Laboratorio 9: Implementar una acción de prompt para el tema de un agente generador de cuestionarios

**Objetivo:**
Las acciones de prompt son una de las formas de extender Microsoft
Copilots. Lo hacen creando acciones en lenguaje natural específicas del
negocio. Estas acciones son interpretadas por el modelo GPT para
realizar la acción necesaria según las instrucciones. Estas acciones se
encapsulan dentro de una definición de plugin de IA, que los copilots
pueden invocar en tiempo de ejecución cuando se detecta una intención o
expresión coincidente.

En este laboratorio, aprenderá a crear una acción de prompt para un tema
de generación de cuestionarios que generará preguntas basadas en un tema
determinado.

Duración estimada - 40 minutos

## Ejercicio 1: Utilizar lenguaje natural para crear un agente

1.  Abra un navegador e inicie sesión en
    +++<https://copilotstudio.microsoft.com/>+++ utilizando las
    siguientes credenciales.  
    - Username - +++@lab.CloudPortalCredential(User1).Username+++  
    - TAP - +++@lab.CloudPortalCredential(User1).TAP+++

2.  Desde la página **Home**, en el área de texto Start building by
    describing what your agent needs to do, introduzca +++I want you to
    be a question and answering assistant that can answer common
    questions from users using the content of a website+++ y haga clic
    en **Send**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image1.png)

3.  El agente se crea según los requisitos.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image2.png)

4.  Desplácese hacia abajo y seleccione **+ Add knowledge** en la
    sección Knowledge.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image3.png)

5.  Seleccione la opción **Public websites**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image4.png)

6.  Introduzca +++[www.microsoft.com](http://www.microsoft.com)+++ y
    seleccione **Add**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image5.png)

7.  Seleccione **Add to agent**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image6.png)

8.  El sitio web se agrega como fuente de conocimiento para el agente.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image7.png)

9.  Haga clic en el icono **Test** para probar el agente. Introduzca
    +++What is Copilot Studio?+++ y presione **Enter**.  
    ![A screenshot of a phone AI-generated content may be
    incorrect.](./media/image8.png)

10. Introduzca +++What is the latest xbox model?+++  
    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image9.png)

Para ambas preguntas, obtendrá una respuesta genérica del agente, ya que
utilizará su conocimiento general.

## Ejercicio 2: Crear una acción de prompt para un tema de respuestas generativas

Utilice **prompt** en **Copilot Studio** para crear acciones en lenguaje
natural como extensiones de copilot. Estas acciones utilizan modelos de
IA generativa de AI Builder y comprensión del lenguaje natural para
abordar escenarios específicos. Esto permite ampliar las capacidades de
sus copilots mediante la creación de acciones basadas en lenguaje
natural.

En este ejercicio, aprenderá a agregar una acción de prompt a un nodo de
tema.

1.  En su agente, seleccione la pestaña **Topics**, luego seleccione **+
    Add a topic** y elija **From blank**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image10.png)

2.  Introduzca el nombre del tema como +++Generate questions for a
    quiz+++. Introduzca los siguientes detalles en **Description**
    (seleccione **Copy** y pegue en el área **correspondiente**):

    ```
    create a number of questions for a quiz based on a topic and format the
    quiz based on the instruction provided

    creates a quiz with a number of questions based on the topic provided
    and formats the quiz

    generate a quiz with a number of questions using the topic provide and
    format the questions

    creates questions for a quiz on a specific topic and format

    format a quiz by a number of questions based on the topic provided
    ```

    Seleccione **Save** en la esquina superior derecha para guardar el tema.

3.  Haga clic en el símbolo **+** debajo del nodo Trigger. Seleccione la
    opción **Add a tool** y luego **New prompt**.  
    ![Screens screenshot of a quiz AI-generated content may be
    incorrect.](./media/image11.png)

4.  Aparecerá el cuadro de diálogo Prompt, y puede ver una guía
    emergente. Seleccione **Next** para continuar.

5.  Cree un prompt que genere preguntas para un cuestionario. Introduzca
    el nombre +++Quiz Generator+++.

6.  Pegue el siguiente contenido en el campo Prompt:  
    ```
    Generate a quiz with [number] questions to cover this [topic]. Decide on the format, such as multiple-choice questions or true/false statements. Use this [format]. Designate the correct answer within parentheses.
    ```

    Seleccione \[number\], expanda **+ Add context** y seleccione
    **Text**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image12.png)

7.  Introduzca el nombre +++number+++ e ingrese un valor de ejemplo como
    +++5+++. Seleccione **Close**.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image13.png)

8.  Seleccione \[**topic**\], expanda **+ Add context** y seleccione
    **Text**. Introduzca el nombre +++**topic**+++ y un valor de ejemplo
    como +++**Science**+++.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image14.png)

9.  Seleccione \[**format**\], expanda **+ Add context** y seleccione
    **Text**. Introduzca el nombre +++**format**+++ y un valor de
    ejemplo como +++bullet points+++. Seleccione **Save** en la ventana
    Prompt.  
    ![A screenshot of a test AI-generated content may be
    incorrect.](./media/image15.png)

10. El nodo de acción de prompt aparecerá en el lienzo. Defina los
    valores de entrada seleccionando el icono ….  
    ![A screenshot of a quiz AI-generated content may be
    incorrect.](./media/image16.png)

11. Seleccione la pestaña **System** y elija **Activity.Text** como
    valor de entrada para que la acción utilice la respuesta completa
    del usuario.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image17.png)

12. Repita el proceso para los demás parámetros de entrada.  
    ![A screenshot of a quiz AI-generated content may be
    incorrect.](./media/image18.png)

13. Defina la variable de salida seleccionando el icono \>. En la
    pestaña **Custom**, seleccione **Create new** y nombre la variable
    +++**VarQuizQuestionsResponse**+++.  
    ![A screenshot of a quiz AI-generated content may be
    incorrect.](./media/image19.png)  
    ![A screenshot of a browser window AI-generated content may be
    incorrect.](./media/image20.png)

14. Debajo de la acción de prompt, seleccione + y agregue un nodo **Send
    a message**. Seleccione el icono **{x}**.  
    ![A screenshot of a quiz AI-generated content may be
    incorrect.](./media/image21.png)

15. Seleccione la variable **VarQuizQuestionsResponse.text.** Seleccione
    **Save** para guardar el tema.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image22.png)

16. Actualice los detalles del tema en la sección **Details**:  
    - Display name - +++generate questions for a quiz+++  
    - Description - +++This topic creates questions for a quiz based on
    the number of questions, the topic and format provided by the
    user+++  
    Seleccione **Save**.  
    ![A screenshot of a quiz AI-generated content may be
    incorrect.](./media/image23.png)

17. Pruebe el agente. Abra el panel Test e introduzca:  
    +++Create 5 questions for a quiz based on geography and format the
    quiz as multi choice+++  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image24.png)  
    ![A screenshot of a cell phone AI-generated content may be
    incorrect.](./media/image25.png)

## Resumen 
En este laboratorio, aprendió a crear una acción de prompt para un tema
mediante la creación de un prompt personalizado y su validación mediante
pruebas.
