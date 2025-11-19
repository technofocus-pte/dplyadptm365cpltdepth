# Lab 9 - Streamlining IT Support Operations with Autonomous Copilot Agent using Copilot Studio

**Estimate Time: 60 mins**

**Objective**

The objective of this lab is to enable participants to streamline IT
support operations at Contoso Solutions by creating an autonomous
Copilot agent. Participants will learn to set up Microsoft Copilot
Studio, configure the IT Support Agent, integrate Power Apps and
Dataverse, enhance the bot’s capabilities with a knowledge base, and
automate ticket creation using Power Automate. This hands-on lab will
equip users with the skills to improve IT workflows, reduce manual
effort, and enhance support efficiency.

**Solution**

Participants will create a customized Contoso IT Support Agent using
Microsoft Copilot Studio, configure it to handle common IT issues, and
integrate it with Dataverse for storing support data. They will set up a
development environment, add knowledge sources, and refine the bot's
conversation flows for better user interaction. By leveraging Power
Apps, participants will create a Dataverse table to manage IT support
records. Using Power Automate, they will automate ticket creation and
email notifications for unresolved issues. Finally, participants will
test the agent to validate its troubleshooting accuracy and workflow
automation, ensuring seamless IT support operations.

## Exercise 1: Getting Started with Power Apps

This exercise introduces participants to Power Apps and Dataverse. The
goal is to log in to Power Apps, set up a working environment, and
create a Dataverse table by importing data from an Excel file.
Participants will learn essential skills for working with data-driven
applications.

### Task 1: Logging into Power Apps

1.  Navigate to power apps website +++https://www.microsoft.com/en-us/power-platform/products/power-apps+++ and click on the **Try for Free** button.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/im1.png)

2.  Enter the **Username**, +++@lab.CloudPortalCredential(User1).Username+++. **select** the **checkbox** and click on the **Start free** button. Select country of origin.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image2.png)

### Task 2: Update the Developer environment settings

1.  Login to the Power Platform admin center at
    +++https://admin.powerplatform.microsoft.com/home+++ using your
    login credentials.
	
	- +++@lab.CloudPortalCredential(User1).Username+++
	- +++@lab.CloudPortalCredential(User1).AccessToken+++

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image3.png)

2.  Select **Manage** from the left pane and select **+ New** under
    **Environments**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image4.png)

3.  Provide the environment name as +++Dev One+++ and select the
    Type as **Developer** and select **Next**.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image5.png)

4.  Select **Save** in the **Add Dataverse** dialog.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image6.png)

5.  Once the environment is **Ready**, select the created **Dev One**
    environment.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image7.png)

6.  Click on **Edit** to edit the Settings.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image8.png)

7.  In the Edit pane, toggle **Administration mode** to **ON** and
    select **Save**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image9.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image10.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image11.png)

8.  Once the edited changes are saved, select **Settings**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image12.png)

9.  Select **Product - Features**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image13.png)

10. Under the **Features**, toggle on **Dataverse search**, select **save**, then toggle **Single table search** option to On and select **Save**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image14.png)

### Task 3: Setting Up a Dataverse Table

1.  From the Admin PowerPlatform page, select the **Manage** on the left side panel, **Environments**, **Dev One** environment and open the **Environment URL**. 

1. Select the **Power Platform Environment**. Under **Customizations** select **Solutions**. 

2.  From the left navigation bar select **Tables.** In the tables
    section top bar click on the **+ New table** and then
    select **Create new tables**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image16.png)

3.  Select **Import an Excel file or CSV** option to create a new table.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image17.png)

4.  Click on the **Select form device** option and select **Support
    Ticket** excel file from **C:\Autonomous agent\LabFiles** folder.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image18.png)

5.  Select **Import** in the next screen.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image19.png)

6.  Select the table and click on **View data** to see the table.

    >[!Note] **Note:** In this case, the table is named *Employee Support Ticket*. The name may vary with each execution. Please save the
table name for future reference. The column name may also vary in the execution. 

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image20.png)

7.  Go to table data, select the drop down next to the **Issue
    Description** field, select **Edit column**, Set the data type
    as **Text** 🡪 **Multiple line** 🡪 **Plain Text** and click on
    the **Update**. The column name may be different in each case.

    >[!Note] The **column name might be slightly different**, but
it will be something similar to the issue description since it is
Copilot generated.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image21.png)

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image22.png)

8.  Select drop down next to the **Ticket Status** field, select **Edit
    column**, Set the Choices as +++Unresolved+++,
    +++Resolved+++, +++Processing+++. Set Default choice
    as **Unresolved** and click on the **Update**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image23.png)

9.  From top right side click on **Save and exit** to save the table.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image24.png)

### Task 4: Add a file to the OneDrive

1.  From the top left of the Power Apps page, select the menu and select
    OneDrive.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image25.png)

2.  Select **My files** - **+ Add new**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image26.png)

3.  Select **Files upload**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image27.png)

4.  Choose **IT Support.xlsx** from **C:\LabFiles**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image28.png)

5.  This file will be used in a later exercise.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image29.png)

    **Conclusion**

    By completing this exercise, participants will learn:

    - How to access and navigate Power Apps using office 365 admin tenant
    credentials.

    - Steps to create and configure a Dataverse table by importing data.

    - Practical knowledge of setting up an environment to support app
    development workflows.

## Exercise 2: Creating the Contoso IT Support Agent

This exercise focuses on logging into Microsoft Copilot Studio and
creating a customized Copilot agent tailored for IT support operations
at Contoso. Participants will gain hands-on experience navigating
Copilot Studio, configuring environments, and building an AI-powered
agent to streamline IT workflows.

### Task 1: Creating and Configuring Contoso IT Support Agent

1.  Login to +++https://copilotstudio.microsoft.com+++ using your loding credentials.

2.  In Copilot Studio home section from top right, select the **environment** and choose **DevOne** environment.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image30.png)

    >[!Alert] **Important:** If the Copilot Studio and does not show up the option to select **Environment** as in the below screenshot, then follow the below steps.
    >
    >![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/im5.png)
    >
    >Open +++https://admin.powerplatform.microsoft.com/+++. Select **Manage** -> **Environments** -> **Dev env** and select the value of the **Environment ID**.
    >
    >![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/im6.png)
    >
    >Navigate back to the Copilot Studio tab and open +++https://copilotstudio.microsoft.com/environments/< EnvironmentID >+++ (Replacing **< EnvironmentID >** with the value fetched above)

3.  On welcome copilot studio tab, click on the **Skip** to move forward.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image31.png)

1. Select **Create**, **+ new agent** and switch the toggle from describe to **Configure**.

4.  Select the **Configure** tab.

5.  Enter **Name, Description and Instruction** of the agent as given
    below and click on **Create** button.

    **Name:** +++Contoso IT Support Agent+++
    
    **Description**: +++Create a Contoso IT Support Agent which transforms IT support at Contoso Solutions by providing instant troubleshooting for common issues, automating ticket creation for unresolved problems, and storing all interactions in Dataverse. This solution enhances response times, reduces manual workloads, and boosts employee productivity.+++
    
    **Instruction**: +++Create the Copilot Agent and configure it to handle IT support operations. Add a knowledge source containing solutions for common IT issues like hardware troubleshooting, connectivity, and software glitches. Set up a trigger to detect updates to a OneDrive file describing unresolved issues. Create an action to save these technical issues into a Dataverse table, ensuring all details are stored for tracking and reporting. Test the agent to validate its troubleshooting accuracy and ticket automation workflow before deployment.+++

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image34.png)

7.  On the overview page of Contoso IT Support Agent, **Enable** the
    orchestrator for the agent.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image35.png)

8.  From top right corner of the agent, click on
    the **Settings** button.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image36.png)

9.  Then go to **Generative AI** section, ensure that **Yes** is selected under **Use generative AI orchestration for your agent's responses?** Scroll down and disable the **Use general knowledge** option and then click on **Save**.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/im1.png)

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/im2.png)

11. Once **saved**, **close** the Settings pane.

    **Conclusion**

    By completing this exercise, participants will learn:

    - How to access and set up Microsoft Copilot Studio.

    - Steps to create and configure a custom Copilot agent.

    - Practical skills in enabling generative AI and orchestrator settings
    for the agent.

    - Ways to enhance IT operations by automating ticket creation and
    leveraging AI for troubleshooting.

## Exercise 3: Enhancing Bot Capabilities

This exercise focuses on enhancing the capabilities of the Contoso IT
Support Agent by adding a knowledge base and customizing bot topics for
improved interaction. Participants will refine the bot's responses and
ensure it effectively assists users in troubleshooting and escalation.

### Task 1: Add Knowledge Base

1.  On the Contoso agent overview page, scroll down and click on **+ Add
    Knowledge** button.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image39.png)

2.  Select **Upload file** to add the lab file **Contoso Common IT
    Issue.docx** from **C:\Autonomous agent\LabFiles** folder and then click
    on **Add** to save the file.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image40.png)

    ![image](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image41.png)

3.  Again, go to agent overview page, scroll down and click on **+ Add
    knowledge.**

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image42.png)

4.  Select **Dataverse (preview)** option as data source.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image43.png)

5.  In top right corner search bar, enter and search for +++Employee+++ and select **Employee Support Ticket** table. Then click on the **Next** and **Add** button to add the knowledge source.

    >[!Note] The **table name might be different** in your case since it is
a Copilot generated one. Try searching for +++Support Ticket+++ if needed.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image44.png)

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image45.png)

    >[!Alert] **Important:** From the Knowledge page, ensure that the added knowledge source has been successfully uploaded. This will generally take 15 to 30 minutes to complete.

### Task 2: Customize the Conversation Start Topic

1.  From the top bar option click on **Topics**, select **System** and then click and open **Conversation Start** topic.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image46.png)

2.  Scroll down and go to message node. Update the message after bot
    name as given below:

    Hello. I’m Bot Name, a virtual assistant. +++How can I help you?+++

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image47.png)

3.  From top click on the **Save** to save the topic.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image48.png)

### Task 3: Update the Fallback Topic

1.  From the top bar option click on **Topics** and then open
    the **Fallback** topic.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image49.png)

2.  Scroll down and go to message node. Update the message as given
    below:

    +++I’m sorry. This information is not available in my system. You can
raise the support ticket via mail for this issue.+++

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image50.png)

3.  From top right side click on the **Save** button to save the topic.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image51.png)

    **Conclusion**

    By completing this exercise, participants will learn:

    - How to upload and integrate a knowledge base to enhance the bot's
    functionality.

    - Steps to customize conversation start messages for a more engaging
    user experience.

    - Techniques to update fallback responses for better handling of
    unsupported queries.

## Exercise 4: Test the agent

This exercise guides participants through testing the Contoso IT Support
Agent to validate its functionality. Participants will check how the bot
handles prompts using the knowledge base and fallback topics to ensure
seamless interaction and escalation.

1.  From top right corner click on the **Test** button. Then in test
    section click on **Map** turn it **On** and then click **Refresh**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image52.png)

2.  Enter the prompt +++My printer is not working how to fix it+++ .
    It gives the solution as per knowledge source.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image53.png)

3.  Again, give the prompt +++Two factor Authentication (2FA)
    issue+++ .

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image54.png)

4.  The 2FA issue and solution is not available in the knowledge source
    so it will go to fallback topic and return prompt related to Raise
    Ticket.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image55.png)

**Conclusion**

By completing this exercise, participants will learn:

- How to test and activate an AI agent for troubleshooting.

- Validation of the bot’s ability to respond using its knowledge base.

- How fallback topics handle unsupported queries and redirect users
  effectively.

## Exercise 5: Automating Support Ticket Creation with Power Automate

This exercise demonstrates how to automate support ticket creation using
AgentFlow and integrate it with the Contoso IT Support Agent.
Participants will create a flow to streamline issue reporting and record
data in Dataverse.

1.  Select **Flows** from the left menu bar of the agent.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image56.png)

2.  Select **+ New agent flow**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image57.png)

3.  Verify the **Designer** tab is selected. Select **Add a trigger** and then select **When an agent calls the
    flow** trigger.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image58.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image59.png)

4.  Select the added trigger, **When an agent calls the flow** and then
    select **Add an Input**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image60.png)

5.  Select **Text** as data type of input and rename the input as
    +++Name+++.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image61.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image62.png)

6.  With same procedure create more input as per given below details.

    | **Input Name**  |  **Data Type** |
    |:------|:---------|
    |  +++ID+++ | Text  |
    |  +++Email+++ |  Text |
    |  +++Details+++ |  Text |

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image63.png)

7.  Below **When an agent calls the flow**, click on **(+)** sign and
    select **Add an action**.

    ![](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image64.png)

8.  In Add an action search bar, enter +++Add a new row+++ . Then select **Add a new row** from Microsoft Dataverse section.

    ![A screenshot of a computer program AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image65.png)

    >[!note] **Note:** Sometimes, a Dataverse connection is not created automatically. You may need to **sign in** again with your
 credentials **OAuth** authentication. If a connection name is required, name it +++connect1+++. The browser may also block the initial pop up window, please allow it in the right corner of the URL bar.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image66.png)

9.  In **Table Name** section search and select +++Employee Support Ticket+++ (or your corresponding table name created).

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image67.png)

10. Below table name select **Show all**, then click on the particular field and add **input** with the help of **dynamic content** button
 (**Thunder bolt**) as per the below table.

    Set the **Current Status** field to **Unresolved**.

    |  **Section** |  **Input Variable** |
    |:------|:-------|
    | Employee Name  | Name (Dynamic Input)  |
    | Email Address | Email (Dynamic Input)  |
    | Employee ID  | ID (Dynamic Input)  |
    |  Technical Issue Description | Details (Dynamic Input)  |

    ![A blue line on a white background AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image68.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image69.png)

11. From the top bar click on **Save draft** and then
    click **Publish**. **Close** the Power automate tab.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image70.png)

12. Select **Flows** from the left menu bar and then select the
    **Untitled** flow(the one that we just created).

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image71.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image72.png)

13. Select **Edit** in the flow.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image73.png)

14. Name the flow as +++Create an Employee Support Ticket+++ and
    select **Save**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image74.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image75.png)

15. From the **Contoso IT Support Agent** **Overview** page, select **+ Add tool**, search for **employee**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image76.png)

16. Select the **Create an Employee Support Ticket** Agent flow.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image77.png)

17. Click on **Add tool** button to add a flow.

    ![A screenshot of a computer screen AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image78.png)

18. From the **Overview** page of the agent, select **inputs** to Edit the **Inputs** section.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image79.png)

    ![A screenshot of a support ticket AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image80.png)

19. Enter the given description in the respected input field by selecting **customize** next to each field, after entering the description click on **Save** button.

    | **Section**  | **Details**  |
    |:------|:-------|
    | Name -- Description  | +++Enter the name of the employee.+++  |
    | ID -- Description  | +++Enter the employee ID in the field.+++  |
    | Email -- Description  | +++Enter the email address of the employee from whom the email is received.+++  |
    |  Details -- Description |  +++Enter the email details of the employee.+++ |

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image81.png)

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image82.png)

    *Conclusion**
    
    By completing this exercise, participants will learn:

    - How to integrate Agent flows with a Copilot agent for ticket creation.

    - Steps to collect and map input data dynamically from user
    interactions.

    - Techniques to automate email notifications for technical issue
    escalation.

    - The ability to configure workflows for efficient support ticket
    management.

## Exercise 6: Configuring a trigger for Automated Actions

This continuation of automating support ticket creation focuses on
setting up a trigger in the Contoso IT Support Agent to a file creation
in the OneDrive with the automated Power Automate flow. Participants
will configure triggers and finalize the agent for deployment.

1.  Go to overview page of the agent, scroll down and click on **+ Add
    trigger**.

    ![A screenshot of a web page AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image83.png)

2.  Select **When a file is created** trigger and click **Next**.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image84.png)

3.  Once the connection establishment is successful, select **Next**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image85.png)

4.  Select **Root** for **Folder**, **Yes** for **Include Subfolders**
    and then click on **Create trigger**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image86.png)

5.  **Close** the Time to test your trigger dialog.

    ![A screenshot of a computer error AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image87.png)

6.  From the Overview page of the agent, select the three dots next to
    the added trigger – **When a file is created** and select **Edit in
    Power Automate**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image88.png)

7.  Select the + symbol below the When a file is created node to add an
    action. In the Action pane, search for +++Get a row+++ and select
    **Get a row** under **Excel Online (Business)**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image89.png)

8.  Once the action is added, add the below details in it.

    - Location – Select OneDrive for Business

    - Document Library – OneDrive

    - File – ITSupport.xlsx

    - Table – Table1

    - Key Column – ID

    - Key Value – +++ID1234+++

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image90.png)

9.  Select the **Sends a prompt to the specified copilot for
    processing** node.

    Under Body/message, enter +++Run the flow Create an Employee Support
    Ticket+++ then add the dynamic values, Name, ID, Email ID, Description
    and Status. Then add +++along with a message "New record added to the
    Employee Support table"+++

    It should look similar to the one in the screenshot below.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image91.png)

10. Now, save the flow by clicking **Save Draft** and then **Publish**
    it to Publish the flow.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image92.png)

11. Back in the Copilot Studio, **Publish** the agent.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image93.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image94.png)

## Exercise 7: Test the agent

1.  From the Power Automate flow, **When a file is created**, select
    **Test**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image95.png)

2.  Select the **Manually** option and select **Test**.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image96.png)

3.  Open your **OneDrive** page. Under **My files**, select **+ Add
    new** and select **Word document**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image97.png)

4.  Back in the Power Automate page, you can see that the flow has
    started execution and has passed.

    ![A screenshot of a computer AI-generated content may be incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image98.png)

5.  From the agent Overview page, select **Test Trigger** icon.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image99.png)

6.  Select the latest trigger and select **Start testing**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image100.png)

7.  It executes the flow, fetches the data from the Support tracker and
    update in the Dataverse table.

    ![A screenshot of a computer screen AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image101.png)

8.  In this case, there is one support ticket detail in the tracker,
    which gets added to the Dataverse table hence creating a support
    ticket for the user.

9.  An Email generation on receiving an email from a user regarding any
    issue will be more appropriate. The email configuration part could
    not be done here due to the tenant permission restrictions. Consider
    the next Task, if you have a tenant with the permissions.

## Task to be done in production environment

In a production environment, the support ticket generation will be
mainly mail based.
>[!Alert]
>
>This task is **not** meant to be performed in this test environment,
>since the tenant has restrictions on using the mail account. These steps
>can be added to the flow after the step 10 of the **Exercise 5:
>Automating Support Ticket Creation with Power Automate**, if you have a
>tenant which can send and receive mail.
>
>Ignore this task in this execution. This has been added purely for
>learning and understanding of the mail generation part and setting up
>the incoming mail as a trigger which will play a main part in the IT
>support operations and then testing the agent

1.  Below Add a new row action click on (+) and select **Add an
    action**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image102.png)

2.  In add an action section, enter +++Send an email+++ in the
    search bar and select **send an email (V2)** from office 365 outlook
    section.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image103.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image104.png)

3.  In send an email section, Enter the below given detail in the
    respected section:

    Replace the place holders for **Name**, **ID**, **Details** with the variables using dynamic content

    **To**

    ```
    Enter support engineer email (Use any email ID - It will be to this id, the mail will be sent by the agent to when Support Ticket is raised)
    ```
    **Subject**

    +++New Technical Support Ticket Raised+++

    **Body**

    ```
    A new technical support ticket has been raised and requires your attention. Please find details below:

    Employee Name: < Name >
    Employee ID: < ID > 
    Technical Issue: < Details >

    Thank you for your prompt attention to this matter.'

    Best Regards
    ```

    ![A screenshot of a email AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image105.png)

4.  From top left corner rename the flow as +++Create an Employee
    Support Ticket+++.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image106.png)

5.  Save and publish the flow

6.  Go to overview page of the agent, scroll down and click on **+ Add
    trigger**.

    ![A screenshot of a web page AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image83.png)

7.  Then from Add trigger window, select **When a new email arrives
    (V3)** trigger.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image107.png)

8.  After successful connection of copilot and outlook and green tick
    appears click on **Next** button.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image108.png)

9.  In folder field select folder icon and select **Inbox** folder and
    then select **Create trigger**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image109.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image110.png)

10. Close the **Time to test your trigger** prompt. On Support agent
    overview page scroll down, on trigger section click on three
    dots **(…)** and select **Edit in Power Automate.**

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image111.png)

11. Right click on When a new email arrives trigger and
    select **Delete**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image112.png)

12. Then click on Add a trigger, search for +++When new email
    arrives+++ and select **When a new email arrives** trigger
    from **Office 365 outlook** section.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image113.png)

13. Click on **Send a prompt to the specified copilot for processing**,
    in body/message section enter the prompt, +++Run Create an
    Employee Support Ticket flow and use content from Body From.+++
    Replace **Body** and **From** as dynamic content variable.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image114.png)

14. **Save** and **Publish** the flow, close power automate window and
    go back to copilot window.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image115.png)

15. Go to overview section and from top right corner click
    on **Publish** and again click **Publish** to publish the copilot.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image116.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image117.png)

    **Conclusion**

    By completing this exercise, participants will learn:

    - Techniques to automate email notifications for technical issue
    escalation.

    - How to set up triggers in Copilot to automate workflows based on email
    inputs.

    - Steps to dynamically map email content to Power Automate flows.

    - The process of publishing and finalizing the AI agent for operational
    use.

    - Practical skills in linking communication tools like Outlook with
    automated workflows.

    **Test the agent**

    This exercise focuses on testing the integration of the Contoso IT
    Support Agent with Power Automate and Outlook. Participants will verify
    the agent's ability to process emails, create support tickets, and
    trigger automated workflows effectively.

1.  Go to overview page of agent, scroll down, click on **(…)** on
    trigger and select **Edit in power automate**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image118.png)

2.  It will navigate to power automate flow, from top bar click
    on **Test** button and then select **Manually** and again click
    on **Test**.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image119.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image120.png)

3.  **Send an email** to the 365 admin tenant mail id from any other
    mail box in order to **trigger the action**. The mail should be
    describing an issue and should have your details like employee id in
    it, similar to the one in the below screenshot. Example content is
    as below

    ```
    Hi Support Team,

    I hope this message finds you well.
    Iam Mark Brown, working as a Software Engineer at Contoso. My employee ID is CONTOSO099
    Issue: Monitor is completely balank and not functioning.
    Kindly raise a support ticket and assist in resolving this issue at the earlierst.
    Thank you for your support.

    Best Regards,
    Mark Brown
    ```

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image121.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image122.png)

4.  Navigate to copilot agent overview page, scroll down and
    select **Test trigger**.

    ![A screenshot of a web page AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image123.png)

5.  Click on **Start testing**, it will start testing.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image124.png)

6.  In test section click on the **Connect**, it will open the
    connection window.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image125.png)

7.  Click on the **Connect** again and then select **Submit.**

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image126.png)

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image127.png)

8.  Navigate to copilot studio window and re run the **Test**.

    ![A screenshot of a web page AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image123.png)

9.  The support request is automatically generated.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image128.png)

10. Navigate to power apps and go to Employee support ticket record
    table, and check the details.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image129.png)

11. Check the Support mail which we configure in power automate flow to
    send an email. The email is automatically sent to the support team.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image130.png)

12. Go to test window and writer query as user +++Mark Brown Ticket
    Current Status+++ . It gives the status of the issue as
    unresolved.

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image131.png)

13. As Support Engineer, write a prompt in the test section. +++I want
    to know about all Unresolved ticket+++ .

    ![A screenshot of a computer AI-generated content may be
incorrect.](https://raw.githubusercontent.com/LODSContent/DPCP-030-dplyadptm365cpltdepth/main/Labguides/Lab9/media/image132.png)

    **Conclusion**

    By completing this exercise, participants will learn:

    - How to test the agent's functionality by simulating real-world
    scenarios.

    - Steps to validate email-triggered workflows and ticket generation in
    Power Automate.

    - How to review generated records in Dataverse and ensure notifications
    are sent to the support team.

    - Practical insights into debugging and finalizing automation workflows.

**Final Conclusion of the Lab Guide**

This lab guide provided participants with a hands-on experience in
deploying an Autonomous Copilot Agent for Contoso Solutions' IT support
service desk. By following the step-by-step exercises, participants were
able to:

1.  **Set Up Copilot Studio**: Participants learned how to log into
    Copilot Studio, create and configure the IT support agent, and
    enable essential settings like generative AI and orchestrator for
    effective troubleshooting and ticket automation.

2.  **Navigate Power Apps**: Participants gained practical knowledge in
    logging into Power Apps, setting up a Dataverse table, and importing
    data from Excel to track and manage support tickets efficiently.

3.  **Enhance Bot Capabilities**: The exercises focused on adding a
    knowledge base to the bot, customizing the conversation start and
    fallback topics to improve user interaction, and ensuring the bot
    could handle a wide range of IT support scenarios.

4.  **Automate IT Support Tasks**: Participants also learned how to
    automate the creation of support tickets using Power Automate,
    enhancing the bot's capability to manage unresolved issues and
    improve IT team workflows.

By completing these exercises, participants were able to implement a
robust autonomous support system that improves response times, reduces
manual workload, and enhances overall productivity for IT support
operations. The integration of Copilot Studio, Power Apps, and Dataverse
ensures a seamless flow of information, automates routine tasks, and
optimizes support workflows, providing immediate troubleshooting
solutions to employees and automated ticket management for unresolved
issues.





===
