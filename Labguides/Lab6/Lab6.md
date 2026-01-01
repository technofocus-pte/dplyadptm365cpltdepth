# Lab 6 - Extend Microsoft 365 Copilot Chat with a HR Agent built using Microsoft Copilot Studio

**Objective**

In this lab, you will learn how to extend Microsoft 365 Copilot Chat
with a Declarative Agent made using Microsoft Copilot Studio.  You will
also learn to add a custom action to the agent that you made.

Estimated duration – 45 minutes

## Exercise 1: Creating a Power Platform environment

With the Power Platform, you can create different environments and
easily switch between them accordingly to your needs. An environment
stores apps, flows, data, agents, etc. and each environment is
completely isolated from any other environment. In this exercise, you
will create a new dedicated environment in which you will perform the
remaining exercises and tasks.

1.  Open a browser, go to +++https://admin.powerplatform.com+++ and login using the below credentials.

    - Username - +++@lab.CloudPortalCredential(User1).Username+++
      
    - TAP - +++@lab.CloudPortalCredential(User1).TAP+++
   
    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image1.png)

2.  Select **Manage** and then select **+ New** under **Environments**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image2.png)

3.  Provide the Name as +++Dev env+++, select the **Type** as
    **Developer** and click on **Next**. Select **Save** in the **Add
    Dataverse** screen.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image3.png)

    ![A screenshot of a web page AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image4.png)

4.  The new environment gets created and changes from **Preparing** to
    **Ready** state once it is ready.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image5.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image6.png)

## Exercise 2 : Creating an agent for Microsoft 365 Copilot Chat

In this exercise you are going to create a declarative agent with
Microsoft Copilot Studio and host it in Microsoft 365 Copilot Chat.

1.  Login to +++https://copilotstudio.microsoft.com+++ using the login credentials below. (They are present in the  **Resources** tab as well).

    - Username - +++@lab.CloudPortalCredential(User1).Username+++
      
    - TAP - +++@lab.CloudPortalCredential(User1).TAP+++

2. Select **Get Started** in the **Welcome to Microsoft Copilot Studio** screen. 

   ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im14.png)

3.  Select **Skip** in the Welcome sreen.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im15.png)

5.  Select the **Dev env** environment that we created in the previous
    exercise.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image8.png)

    >[!Alert] **Important:** If the Copilot Studio and does not show up the option to select **Environment** as in the below screenshot, then follow the below steps.
    >
    >![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/im5.png)
    >
    >Open +++https://admin.powerplatform.microsoft.com/+++. Select **Manage** -> **Environments** -> **Dev env** and select the value of the **Environment ID**.
    >
    >![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/im6.png)
    >
    >Navigate back to the Copilot Studio tab and open +++https://copilotstudio.microsoft.com/environments/< EnvironmentID >+++ (Replacing **< EnvironmentID >** with the value fetched above)
    
6.  To create a declarative agent for Microsoft 365 Copilot Chat you
    need to first browse the list of agents in Copilot Studio and then
    select the agent with name **Microsoft 365 Copilot**. Select **Got it** in the version update pop up.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im16.png)

8.  Select **Agents** from the left navigation bar and select **Microsoft 365 Copilot** from the list.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im17.png)

9.  A new section of Microsoft Copilot Studio will open. From there,
    select the **+ Add** command to create a new agent for Microsoft 365
    Copilot Chat.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/img1.png)

10.  Copilot Studio asks you to describe in natural language what is the
    purpose of the agent. You can define your agent requirements. Paste
    the prompt below to do so

    +++You are an agent helping employees to find information about HR policies and procedures, about how to improve their career, and about how to define learning pathways.+++

   ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image11.png)

11.  When requested by Copilot Studio, give the name "Agentic HR" to your
    custom agent. Use the following prompt.

    +++Name it as Agentic HR+++

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image12.png)

11.  Then, instruct Copilot Studio to have specific tasks or goals with
    the following instruction:

    +++Emphasize everything that helps team building, inclusion, and the growth mindset+++

    ![A screenshot of a chat AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image13.png)

11.  Then, define a professional tone for your agent, providing the
    following input:

    +++It should have a professional tone+++

   ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image14.png)

11. Once you are done describing your agent, select
    the **Create** command to create the actual agent. 

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image15.png)

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image16.png)

## Exercise 3: Publishing the agent in Microsoft 365 Copilot Chat

1.  Select **Publish** from the agent overview page.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im20.png)

2.  Select **Publish** in the **Publish agent** screen.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image18.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image19.png)

3.  Select **Copy** under **Share link** to copy the link and then
    select **Done**.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image20.png)

4.  Open a new tab and paste the copied url. Select **Add** to add the
    **Agentic HR** to your list agents.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image21.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image22.png)

5.  Select **Skip** in the introduction screen.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image23.png)

6.  The **Agentic HR** agent is now added. Select **Agentic HR** from the left navigation pane.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im21.png)

## Exercise 4: Create SharePoint site

1.  In a new browser, navigate to +++https://m365.cloud.microsoft/chat/+++ Select **Apps** from the left pane and then select **SharePoint** once the Apps are loaded.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image25.png)

2.  Select **+ Create site** from the SharePoint page.

    ![A screenshot of a browser AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image26.png)

3.  Select **Communication site** from the **Select the site type**
    page.

    ![A screenshot of a web page AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image27.png)

4.  Select a **template** to be used.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image28.png)

5.  Select **Use template**.

    ![A screenshot of a website AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image29.png)

6.  Enter +++Contoso site2-@lab.LabInstance.Id+++ as the **Site name** and select
    **Next.**

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image30.png)

7.  In the next screen, select **Create site**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image31.png)

8.  Once created, note down the **url** of this site.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im22.png)

9.  Select **Documents** from the menu bar. Select **+ Create or upload** -> **Files upload**

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im23.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im24.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im25.png)

11. Select **Sample-list-of-candidates.xlsx** file from **C:\LabFiles**
    to be uploaded. Once **uploaded**, click on the **3 dots** next to the **document**, select **Copy link** and save the link in a **notepad**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im26.png)

## Exercise 5: Adding knowledge to the agent

In this exercise you are going to add knowledge from the Sharepoint site, to the agent that
you created.

1. Back in Copilot studio, from the **Agent** home page, select **+ Add knowledge** under the Knowledge section.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/img11.png)

2. Select **SharePoint**, enter the **url** of the tracker uploaded in the earlier exercise and then select **Add**. 

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im27.png)

4. Select **Add to agent** in the next screen.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/img16.png)

5. Select **Publish** to publish the agent.

    ![A screenshot of a computer AI-generated content may be
incorrect.](./media/im28.png)

6. Select **Publish** again.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image51.png)

7. **Copy** the url and **open** it from a browser.

    ![A screenshot of a computer program AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image52.png)

8. This time, it will give an option to **Update now** since it is already added. Select it.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image53.png)

9. Select **Open** once it is updated.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image54.png)

    >[!Alert] you may have to engage in the copilot conversation to get the expected results.

10. In the **Agentic HR agent** screen, send the below message.

    +++Show me a list of candidates for HR with role "HR Director” or "HR Manager”+++
   
    ![A screenshot of a computer AI-generated content may be
   incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image55.png)

    >[!Alert] **Important:** If you are asked for approval, perform the below steps. Else you can ignore these and check for the result as in the last step in this lab guide.
    >
    >In the Data to be shared with Agentic HR message, select **Allow once** (if prompted) option.
    >![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image56.png)
    >
    >If it asks you to **sign in**, select the **Sign in to Agentic HR** option and then select **Connect** in the next screen.
    >![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image57.png)
    >
    >    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image58.png)
    >
    >Select **Submit** once connected.
    >![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image59.png)
    >
    >![A screenshot of a chat AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image60.png)
    >
    >Now, resend the below message to the agent.
    >
    >+++Show me a list of candidates for HR with role “HR Director” or ”HR Manager”+++
    >![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image61.png)


15. You will then receive the requested list

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image62.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab6/media/image63.png)


## Summary

In this lab, you have successfully learnt, how to use custom connectors
in Copilot Studio.




===
