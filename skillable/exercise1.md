## Build M365 Declarative Agents & API Actions with Copilot Studio Workshop

In this lab you’ll first work with Microsoft Copilot Studio to build your first declarative agent, you’ll then publish this copilot to Microsoft 365 Copilot. Next, in the second half of this workshop, you'll extend your copilot with an out of the box connector.

> The green text with the **T** icon can be clicked on and will be typed automatically into the VM, For example, please click in the password text box and then click the password: **Passw0rd!**
>
> > **NOTE:** To ensure text is entered accurately avoid interacting or clicking in the VM until the text has finished being typed

### Build your first agent

To start you're going to build your very first copilot powered by Generative answers.

1. Open Microsoft Edge and navigate to <https://copilotstudio.microsoft.com>
2. Log in with

   - Username: +++@lab.CloudPortalCredential(User1).Username+++
   - Password: +++@lab.CloudPortalCredential(User1).Password+++

3. Click **Get Started**
![get started](media/getstarted.png)

4. Click **skip**
![skip](media/skip.png)

5. Click **Cancel agent creation**
![cancel](media/cancel.png)

6. Click **leave** 
![create agent](media/leave.png)

7. Click the Environment drop down to make sure you have the default environment selected.

8. In the left nav click **Agents** to start creating a new copilot

   ![create agent](media/create.png)

9. Click **Copilot for Microsoft 365**

   ![create agent](media/agents.png)

10. Click **Add** button on the section agents

   ![add button](media/AddAgent.png)

11. Describe your agent by providing the following statement (without the double quotes) and click on the arrow

   ```
   I would like to make an executive summary assistant. this assistant will take company name as user prompt and create a summary report highlighting key details about the company. the knowledge about the company can come from publicly available information or internal data sources
   ```

   ![description](media/description.png)

12. Give your agent a new neme or use the suggested one by typing `yes` and click on the arrow.
   ![agent name](media/agentname.png)

   ![agent name](media/instructons.png)

13. Describe your agent refined instructions by providing the following statement (without the double quotes) and click on the arrow

   ```
   Summary Report must include following sessions:
   - Company history
   - Number of employees
   - Recent news about the company
   - Any business done in the company in the last two years
   - Dividend per share history for the last five years in a table with columns for dividend and year.
   ```

   ![agent behavior](media/agentbehavior.png)

14. Define your agent response behavior by typing `formal and detailed` and click on the arrow.
    ![agent behavior](media/createbot.png)

15. Click **Create** to finish your agent
    ![agent behavior](media/createbotbutton.png)

16. Scroll down until the **Starter prompts** is displayed and click on the pencil icon
    ![start prompt creation](media/starterprompts.png)

17. Edit the first start prompt with the following values

- Title : `Executive Summary Report`
- Prompt : `Provide an executive summary report for Microsoft`, and click **Save** button

  ![start prompt creation](media/editstarterprompt.png)

18. Press the refresh icon, the start promtps will now be refreshed with the updated values
    ![refresh](media/refresh2.png)

19. The agent is now ready to be tested go ahead and type `Provide an executive summary report for Microsoft` or select it from the **Starter prompts**
    ![refresh](media/reply.png)

### Fine-tune your agent

In the previous steps the agent was not returning the most up to date values in the next steps the agent will be fine-tunned to:

- Display the most up to date values (LLM do not have the most recent information)
- Include the information about the board members of the company

Finally the changes will be tested and published to M365 Copilot so that is available on BizChat.

20. Enable the **Web browsing** toggle in the **Additional settings** section

    ![web browsing](media/webbrowsing.png)

21. Click on the arrow on the top to refresh the agent and type `Provide an executive summary report for Microsoft`, or select it from the **Starter prompts**

    ![agent refresh](media/refresh.png)

22. Verify that the agent is now returning more recent information.

    ![up to date information](media/uptodateinfo.png)

23. Now, On the left side of you editor, scroll to the top to display the **Details** section, and Click **Edit**

    ![edit agent](media/edit.png)

24. In the **Instructions** section text box add `- Board members` before `- Number of Employees` and click **Save**

    ![edit instructions](media/board.png)

25. Click on the Refresh button and type `Provide an executive summary report for Microsoft` and hit **Enter**. You should now see that Board members information is included in the output.

    ![agent refresh](media/board2.png)

### Publish the Agent

So far the agent has been only tested in Copilot Studio, in the next steps the agent will be published to M365 Copilot to be availabe in the Bizchat

26. Verify that the agent is now returning board information and click **Publish**

    ![publish agent](media/publish.png)

27. Define the agent properties and click **Publish**, leaving the pre populated fields as is

    ![publish agent](media/publish2.png)

28. The publishing process starts, and shows following dialog.

    ![publish agent](media/publish3.png)

    It can take a couple of minutes for the publishing process to finish, please wait and keep this dialog displayed until the publishing is complete.

29. Now, Click **Copy** button under the **Share link** section

    ![publish agent](media/publish4.png)

30. Launch a new Microsoft Edge (or a new tab), paste the copied URL and hit **Enter**

31. On the page that opens, click **Add** button to acess your new declerative agent in M365 BizChat.

    ![add agent to teams](media/addbottoteams.png)

32. Find you agent name on the right menu in BizChat and click it

    ![bizchat](media/bizchat.png)

33. Type `Provide an executive summary report for Ford` and hit **Enter** to see the output

    ![Ford Report](media/ford.png)
