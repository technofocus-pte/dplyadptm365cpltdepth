# Lab 10: Implement prompt action for a quiz generation agent’s topic

**Objective :** 

Prompt actions are one of the ways to extend Microsoft Copilots. They do this by creating business specific natural language actions. The actions are interpreted by the GPT model to perform the necessary action as instructed. These actions are wrapped within a AI plugin definition, which copilots can invoke at runtime when a matching intent or utterance is encountered.

In this lab, you will learn to create a prompt action for a quiz generation topic which will generate quiz questions based on a given topic.

Estimated duration - 40 minutes

## Exercise 1: Use natural language to create an agent

1.  Open a browser and login to +++https://copilotstudio.microsoft.com/+++ and login with the
    credentials from the Resources tab if you are not in that page
    already.

    ![](./media/image1.png)

2.  If you are already on the Copilot Studio page, click on **Home** to
    go to the Home page.

    ![](./media/image2.png)

3.  On the Home page, in the text area under Describe your agent to
    create it, enter +++I want you to be a question and answering assistant that can answer common  questions from users using the content of a website+++ and click on **Send**.

   ![](./media/image3.png)
    
5.  It might suggest a name for the agent. Either accept it or provide
    your own name.
    
   ![](./media/img19.png)
    
7.  Give other details regarding the functions of the agent like below.

    +++help answer common product and support questions using the content of a website, and help answer HR questions from an uploaded file+++

   ![](./media/img20.png)
    
9.  Provide +++www.microsoft.com+++ for the website that will be used a
    sknowledge source.

   ![](./media/image4.png)

10. Once done with giving instructions, click on **Create** to create
     your agent.
  **Note**: Setting up the agent may take a few minutes. Once the setup is complete, click Skip to continue.
  ![](./media/img21.png)

11.  Select the agent gets created to view the agent details. Scroll through
    the page to understand that the agent has been created with the
    instructions you have provided for it.

    ![](./media/image6.png)

    ![](./media/image7.png)

11.  Click on **Test** icon to Test the agent. Enter +++What is Copilot Studio+++ and hit **Enter**.

    ![](./media/image8.png)

11. Enter +++What is the latest xbox model?+++

    ![](./media/image9.png)

For both the above steps, you will get an answer from the agent which
will be a generic one since the agent will be using its general
knowledge.

## Exercise 2: Create a Prompt action for a Topic for generative answers

Actions can be used to extend the capabilities of agents. You can add
multiple types of actions to your agents in Microsoft Copilot Studio:

- **Prebuilt connector action**, which use Power Platform connectors to
  access data from other systems, such as popular enterprise products
  like Salesforce, Zendesk, MailChimp, and GitHub.

- **Custom connector action**, where a connector can be built to access
  data from public or private APIs.

- **Power Automate cloud flow**, which use Power Automate cloud flows to
  perform actions, retrieve and work with data.

- **AI Builder prompts**, which use AI Builder and natural language
  understanding to target the specific scenarios and workflows within
  your business.

- **Bot Framework skill**, which use the skill manifest that outlines
  the actions the skill can perform, including its input and output
  parameters, the skill's endpoints, and dispatch models for the skill.

In this exercise, you will learn how to add a prompt to action to a
topic node

1.  In your agent select the **Topics** tab, select **+ Add a
    topic** and select **From blank**.

    ![](./media/image10.png)

2.  Enter the name for the Topic as +++Generate questions for a quiz+++. Enter the below details in the **Description**.

    +++create a number of questions for a quiz based on a topic and format the quiz based on the instruction provided+++

    +++creates a quiz with a number of questions based on the topic provided and formats the quiz+++

    +++generate a quiz with a number of questions using the topic provide and format the questions+++

    +++creates questions for a quiz on a specific topic and format+++

    +++format a quiz by a number of questions based on the topic provided+++

    Select **Save** on the top right to save the topic.

    ![](./media/img22.png)

3.  Click on the **+** symbol below the Trigger node. Select the **Add a tool** option and select **New prompt** option under that.

    ![](./media/img23.png)

5.  The Prompt dialog will appear, and you may see a flyout appear that
    will guide you on how to create your prompt. Select **Next** to go
    through the guide.

6.  We'll create prompt that will generate questions for a quiz. Enter
    the name for the prompt as +++Quiz Generator+++.

7.  Paste the below content in the Prompt field.

    +++Generate a quiz with [number] questions to cover this [topic].
Decide on the format, such as multiple-choice questions or true/false
statements. Use this [format]. Designate the correct answer within
parentheses.+++

    Select [number], expand **+ Add context** section and select **Text**.

    ![](./media/img26.png)

9.  Enter the name as +++number+++ and enter sample data such as
    +++5+++. Select **Close**.

    ![](./media/img27.png)

10. Select **[topic]**, expand **+ Add context** section and select **Text**. Enter the name as +++topic+++ and enter sample data such as
    +++Science+++.

    ![](./media/img28.png)

11. Select **[format]**, expand **+ Add context** section and select **Text**.Enter the name as +++format+++ and enter sample data such as
    +++bullet points+++. Select **Save** in the Prompt window

    ![](./media/img30.png)

16. The prompt action node will now appear in the authoring canvas of
    the Topic. Next, the values of the input parameter need to be
    defined in order for the agent to populate them. Select
    the **\>** icon

    ![](./media/image22.png)

17. Select the **System** tab and select the **Acivity.Text** as the
    input value for the action to use the user’s entire response and
    identify the format value.

    ![](./media/image23.png)

18. Repeat the same for the remaining input parameters of the prompt
    action.

    ![](./media/image24.png)

19. Next, we need to define the output variable of the prompt action.
    This is so that the response can be referenced downstream in the
    topic. Select the **\>** icon and in the **Custom** tab,
    select **Create new** and and name the variable as +++**VarQuizQuestionsResponse**+++. 

    ![](./media/image25.png)

    ![](./media/image26.png)

20. Below the Prompt action, select the **+** icon to add a new node and
    select **Send a message**. Select the **{x}** variable icon.

    ![](./media/image27.png)

21. Select the variable **VarQuizQuestionsResponse.text**. This will add
    the text property of the prompt action response to the send a
    message node. Select **Save** to save your topic.

    ![](./media/image28.png)

22. The Topic details needs to be updated next which will be used by
    your agent to associate the topic with the user's intent when
    Generative mode is enabled. Select **Details** and enter the following.

    - Display name - +++generate questions for a quiz+++

    - Description - +++This topic creates questions for a quiz based on the number of questions, the topic and format provided by the user+++

    Select **Save** to save your topic.

    ![](./media/image29.png)

25. Now we are ready to test the agent. In the test pane, select
    the **refresh** icon. Then enter the following question and observe
    the output.

    +++Create 5 questions for a quiz based on geography and format the quiz as multi choice+++

    ![](./media/image32.png)

    ![](./media/image33.png)

## Summary

In this lab, we have learnt how to create a prompt action for a topic by
creating a custom prompt and test it.

