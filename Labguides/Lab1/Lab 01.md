# **Get Started with Workflows in Microsoft 365 Copilot**

## **What is Workflows Agent?**

Workflows is an agent in Microsoft 365 Copilot that helps you automate
work across Microsoft 365 using natural language. Instead of manually
configuring steps or connectors, you simply describe what you want, and
Workflows generates a working workflow using supported Microsoft 365
services. 

## **What you will build in this exercise**

You will create a workflow that:

- Runs **every weekday morning**

- Reviews **unread emails from the last 24 hours**

- Identifies **important or actionable emails**

- Organizes them into clear sections

- Sends a **summary to you in Microsoft Teams**

## **Prerequisites (Important – Check Before You Start)**

### **Licensing & Access**

Make sure:

- You have a **Microsoft 365 Copilot license**

- You are part of the **Frontier program**

- Workflows Agent (Frontier) is available in your tenant

**Note**: Workflows is **English-only** at the moment.

### **DLP & Connector Requirements (Admin setup)**

Your organization’s **DLP policy must allow**:

- **AI actions** (Power Platform connector)

- **Dataverse (AI prompt)**

- Microsoft 365 connectors:

  - Outlook

  - Teams

  - SharePoint

  - Planner

  - Approvals

These are required so Workflows can read emails, post to Teams, and
summarize content.

## Exercise 1: Add Workflows Agent to Copilot

1.  Sign in to **Microsoft 365 Copilot**

&nbsp;

1.  **Sign in with your Microsoft 365 Copilot account**

![](./media/4ad5a4ad6d6c6b84f471ea900a689ba5e1ea248d.png)

2.  Click **Yes,** to stay signed in.

![](./media/a610296599c1f2181c95a5860d341f03f18aa4eb.png)

3.  After successful login, you will see **Copilot Chat** home page.

![](./media/92400451e9de39ccd7f544f4beab4ca5e43f4207.png)

2.  In the **left navigation**, select **All Agents**

![](./media/b0e69ae705d99ce8880aa9719a128e48bad23cb0.png)

3.  Explore **Agent Store**

![](./media/9afcbf76689888f49e8d52daa80c11eda6d41459.png)

4.  Search for **Workflows (Frontier),** Select **Add**

![](./media/85d11ee9343169932c044530d7e6400ad10e738c.png)

![](./media/f25bd0390a5059a456584d38ee5f76f0bfad5bf4.png)

5.  You should now see **Workflows** (Frontier) under **Agents** in the
    left pane.

![](./media/6cc7c2bd9406f4973e9829e14c365370d300301f.png)

## **Exercise 2: Step-by-Step: Build Your First Workflow**

### Step 1: Open Workflows Agent

1.  Go to **Microsoft 365 Copilot**

2.  In the left navigation, select:  
    **Agents → Workflows Agent (Frontier)**

![](./media/6cc7c2bd9406f4973e9829e14c365370d300301f.png)

- You will see a chat interface of **Workflows (Frontier).**

![](./media/38872484c68cf1f6168270424a10308d7bc1e599.png)

### Step 2: Describe Your Workflow in Natural Language

1.  Copy and paste the following **example prompt in the prompt box of
    Workflows Frontier,** and click **Send**

*“Each weekday morning, review all unread emails from default inbox from
the last 24 hours, and identify anything important I may have missed.
Focus on messages that are high priority, time-sensitive, or require
action. Organize the results into three sections: Needs Response, For
Your Information, and Other Important Emails. For each message, include
the sender, subject, a brief summary, any due dates or deadlines, and
next steps. Send to myself on Teams”*

![](./media/5789886267f0293f8c3ae3dad534be3b0fcccd51.png "A prompt for workflows")

### Step 3: Understand What Copilot Just Did

Behind the scenes, Workflows automatically:

- Creates a **time-based trigger** (weekday mornings)

- Connects to:

  - **Outlook** (read unread emails)

  - **Dataverse AI prompt** (summarization & grouping)

  - **Teams** (send the output)

- Builds the workflow logic for you

You **did not** configure connectors manually—Copilot did it.

![](./media/ab601e06b9b95dd112325aa4a867ea79deac644e.png)

![](./media/55dbce3d1f52f0cbaba8af9bb1a4a4283cbc1961.png)

### Step 4: Review the Generated Workflow

1.  After processing your prompt, you’ll see:

- Trigger (Schedule)

- Actions (Read emails → AI summarize → Send Teams message)

- A **visual workflow designer**

![](./media/55dbce3d1f52f0cbaba8af9bb1a4a4283cbc1961.png)

2.  Take a moment to:

- Review steps

- Confirm inbox and Teams destination

- Rename the workflow (optional)

### Step 5: Save the Workflow

1.  Select **Save** on the top right corner of **Workflow** window

- Your workflow is now created and ready to test

![](./media/fa4a0bd83f7b6cdc1a89febcc0419e165922ff77.png)

### Step 6: Test the Workflow 

After saving the workflow, you’ll be prompted to test.

1.  Select **Test** from the top menu.

![](./media/ed5f19ae1620e92a2e662d80c05f56c643c174de.png)

- Observe the test run generated in the Workflow window.

![](./media/e7cc1fa407a851b773427df48cdfa07f8051b57d.png)

### Step 7: Review Test Results

1.  After the test runs:

![](./media/7f059525a53555b58a03b433e71e3f97b6523a37.png)

2.  Check:

    1.  Emails detected

**Note:** I manually sent an email to my ODL account to verify that the
workflow triggers a notification in Microsoft Teams. If you don’t have
any new unread emails in your inbox, you’ll need to do the same to test
the workflow.

> ![](./media/49d9c762134b6eccc18052cf9d0a33d5d437ba91.png)

2.  Categorization accuracy

> ![](./media/2d10b0e295ba13f9a33f753c1c9106f37fc01304.png)

3.  Teams message format:

- Ensure that the Teams message format is matching the Outlook email
  details.

![](./media/92c28748c59c3ed14ab872bf7c6815c0830855f0.png)

3.  If something looks wrong:

    1.  Update the prompt

    2.  Re-test

**Note**: You can iterate just like chatting—no rebuild required.

4.  Simple **SharePoint Document Review Workflow** for user to explore
    more

**Example prompt:**

*“When a new document is uploaded to the “Project Documents” library in
my SharePoint site, review the document and generate a short summary.
Highlight key points, action items, and any risks or missing
information. Send the summary to me in Microsoft Teams for review.”*

### Step 8: Monitor Workflow Runs

To see how your workflow performs over time:

1.  Go to the **Activity** tab located at the centre of the workflow
    window.

![](./media/28df1b8574f50221f82bda6e54e9542160a8acd8.png)

2.  Select the workflow you want to manage. You may choose your most
    recent workflow or any other workflow as required.

![](./media/d63c998e91c799dbde31566e613ef0133d457588.png)

3.  View the following details:

&nbsp;

1.  **Trigger Time**  
    The exact date and time when the workflow was initiated.

2.  **Action Status (Success / Failed)**  
    The execution result of each action within the workflow, indicating
    whether the action completed successfully or encountered an error.

3.  **Output Details**  
    The response or data generated by each action, including inputs,
    outputs, and any error messages for troubleshooting.

![](./media/ef6da3f0774d811104763b1c6f5b8c24cad89922.png)

4.  Click any run to see **step-by-step execution details**.

&nbsp;

1.  **Review the execution status**

    1.  A green banner such as “Your workflow ran successfully”
        indicates the run completed without errors.

    2.  If the run failed, error indicators will be shown instead.

2.  **View trigger details**

    1.  At the top of the run details, expand the Trigger section (for
        example, Get Unread Emails).

    2.  This shows when and how the workflow was triggered.

### Step 9: Manage Your Workflows

From the **Workflows (Frontier) home page**, you can:

1.  **View** all workflows you created under **My workflows** section of
    **Workflows (Frontier)** page.

![](./media/cdbac86ac3f34777e0077b74d3a369c946d33403.png)

2.  Turn workflows on or off using the **ellipses (...).** Turning off a
    workflow pauses its automation.

&nbsp;

1.  Navigate to the **ellipsis** (three dots) on the right-hand side of
    the selected workflow, then click **Turn off** to pause the
    automation.

![](./media/95723f84cdeb60baf970814170af6379601570f2.png)![](./aa88133a0c2c55a8dfce07d4a825cecbd142e2b4.png)

2.  Click on **Delete** to delete workflows permanently.

**Note**: Deleting a workflow removes it entirely and can’t be undone.

![](./media/862df5f928b9c982256f86629542fa87c130230f.png)

## **What You Learned in This Exercise**

By completing this beginner workflow, you learned how to:

- Use natural language to automate tasks

- Connect Outlook, Teams, and AI summarization automatically

- Test and monitor workflows

- Manage automations without Power Automate knowledge
