# Lab 6 - Build a poetic declarative agent using Microsoft 365 Agents Toolkit

**Scenario**

An organization wants to explore how **Microsoft 365 Copilot** can be customized using **declarative agents** to deliver unique, branded, and personality-driven experiences. As a proof of concept, the team decides to build a creative agent that responds to user questions in a **poetic form**, while still leveraging Microsoft 365 Copilot’s core intelligence and web knowledge.

Using **Microsoft 365 Agents Toolkit** in Visual Studio Code, the team will create a declarative agent, **define** its **behavior** through **instructions**, enhance the user experience with **conversation starters**, and enable **web search** capabilities—all while testing the agent directly within **Microsoft 365 Copilot Chat**.

**Objective**

By completing this lab, you will learn how to:

-    **Create a declarative agent** using Microsoft 365 Agents Toolkit in Visual Studio Code.

-    **Provision** and **test** the declarative agent within Microsoft 365 Copilot Chat.

-    **Define agent behavior** using **instruction prompts** in the agent manifest.

-    **Customize** the agent’s personality by enforcing poetic responses.

-   **Add conversation starters** to guide user interaction.

-    **Enable web search** capabilities for the agent.

-    **Validate agent behavior** after each enhancement through live testing.

## Exercise 1: Create a declarative agent

In this exercise, you will start with creating a basic declarative agent
from the Visual Studio Code.

1.  From the VM desktop, open **Visual Studio Code**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im39.png)

3.  Select **Extensions** from the left pane and type +++Microsoft 365 Agents Toolkit+++

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image1.png)

4.  Select the **Microsoft 365 Agents Toolkit** and select **Install**
    to install the extension.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image2.png)

5.  Select **Create a New Agent/App** on the left panel, then select **Declarative Agent**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image3.png)

6.  Select **No Action** to create a basic declarative agent.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image4.png)

7.  Select **Default folder** to store your project root folder in the
    default location.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image5.png)

8.  Enter +++My Agent+++ as the **Application Name** and press **Enter**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image6.png)

9.  Select **Yes, I trust the authors** in the Do you trust the authors pop up.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im29.png)

9.  In the new Visual Studio Code window that opens, select **Microsoft 365 Agents Toolkit**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image7.png)

10. Select **Provision** in the **Lifecycle** pane and then select **Sign in** in the pop up that appears, to sign in to the Microsoft 365 account.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image8.png)

    >[!Alert] If provisioning fails and VSC gives an option to **resolve with @m365agents**, select to resolve. Provisioning should complete after selecting to resolve.

11. **Sign in** using the below credentials and close the window once done.

    - Username - +++@lab.CloudPortalCredential(User1).Username+++
      
    - TAP - +++@lab.CloudPortalCredential(User1).TAP+++

    ![A black background with white text AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image9.png)

12. Ensure that the provisioning is successful. You can see the success message at the bottom right corner of VS code. Now, the basic declarative agent creation is done.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im31.png)

### Task 1: Test the agent

In this task, we will test the declarative agent that we have created.

1.  Navigate to the Copilot application with the
    URL +++https://m365.cloud.microsoft/chat+++.

2.  In the top left, **select** the **conversation drawer icon**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image10.png)

3.  Select the declarative agent **My Agentdev** (It can also be **My Agent**. Select based on the name that gets listed.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im32.png)

4.  Enter a question +++Hello! How can you help me?+++ for your
    declarative agent and ensure that it replies with "Thanks for using
    Microsoft 365 Agents Toolkit to create your declarative agent!"

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im33.png)

    ![A screenshot of a chat AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image12.png)

    In this exercise, we have created a basic declarative agent and tested its functionality.

## Exercise 2: Add instructions

In this exercise, we will start adding instructions to the declarative
agent that we created in the previous exercise and enhance it

1.  From the Visual Studio Code, open
    the **appPackage/instructions.txt** file and replace its contents
    with the following text.

    ```
    You are a declarative agent and were created with Microsoft 365 Agents Toolkit. You are an expert at creating poems.
    
    Every time a user asks a question, you **must** turn the answer into a
    poem. The poem **must** not use the quote markdown and use regular
    text.
    ```

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image13.png)

    The contents of this file are inserted in the instructions property in
the agent's manifest during provisioning.

2.  Select **Provision** in the **Lifecycle** pane of the Agents
    Toolkit.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image14.png)

3.  Check that the **provisioning** is completed **successfully**. You
    can see a message at the bottom right of the Visual Studio Code.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image15.png)

4.  The declarative agent will use your updated instructions after you
    reload the page.

5.  Refresh the chat page, select **My Agentdev** and type +++Do we have chocolate in our food catalog?+++

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im34.png)

6.  Observe that the agent gives a poetic answer.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im35.png)

7.  Now, add conversation starters to the agent.

8.  Open the **appPackage/declarativeAgent.json** file and right after
    the instructions node add a **comma** press enter, and paste below
    code.

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
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image18.png)

9.  Select **Provision** in the Lifecycle pane of the **Microsoft 365 Agents Toolkit** and ensure that the provisioning gets completed successfully.

10. The updated conversation starters will be available in your
    declarative agent after you **refresh** the page.

11. **Refresh** the chat page to check the same.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im36.png)

## Exercise 3: Add web content

In this exercise, you will add the ability to the agent to search the
web content.

1.  Open the **appPackage/declarativeAgent.json** file, right after
    the end of the conversation_Starters, add a **comma** press enter, and paste the below capabilities array.

    ```
    "capabilities": [
            {
                "name": "WebSearch"
            }
        ]
    ```

    ![A screenshot of a computer program AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image20.png)

2.  Select **Provision** in the Lifecycle pane of the **Microsoft 365
    Agents Toolkit** and ensure that the provisioning gets completed
    successfully.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab7/media/image21.png)

    The declarative agent will have access to web content to generate its answers after you reload the page.

3.  Ask the agent, +++How can I build a declarative agent?+++ and
    observe that the agent replies from the web.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im37.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im38.png)

## Summary

In this lab, you successfully **built** a **poetic declarative agent** using **Microsoft 365 Agents Toolkit**. You created and provisioned a basic declarative agent, tested its integration with Microsoft 365 Copilot Chat, and enhanced it by adding custom instructions that transform every response into a poem.

You further improved the agent experience by adding conversation starters and enabling web search capabilities, allowing the agent to retrieve external information while maintaining its poetic style. This lab demonstrates how declarative agents can be customized through configuration and instructions—without writing code—to deliver creative, controlled, and engaging Copilot experiences within Microsoft 365.


===
