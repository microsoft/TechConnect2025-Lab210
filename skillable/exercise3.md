## Ground the agent responses in enterprise data

In this exercise the agent will be configured to ground the executive summary report with the information available in company´s CRM system. The report will include information about the revenue, that is stored in the Account table in the Dataverse (CRM System).

### Populate Test Data

In the following steps, we populate the **Account** table in Dataverse with some test data:

1. Launch a new Microsoft Edge browser or tab, go to PowerApps Maker Portal at <https://make.powerapps.com>, and select **Tables** in the left menu

   ![data import settings ](media/dataimport1_1.png)

2. From the list of tables shown click on the **Account** table

   ![data import settings ](media/dataimport2_1.png)

3. Now, Click on the bottom arrow as shown below, type `Annual` on the search text box, select **Annual Revenue** from the list shown, and click **Save** button

   ![data import settings ](media/dataimport3_1.png)

4. In the **Account columns and data** section, add a new row with `Microsoft` as the Account Name and `1000000` as the Annual Revenue.

5. Also, add another row with `Ford` as the Account Name and `2000000` as the Annual Revenue. After these rows are added, you table should now have two new rows as shown below

   ![data import settings ](media/dataimport6.png)

The account information has now been populated in the account table, let's now start the Copilot Studio required configurations

### Grounding the Agent

1. In case you have closed the Copilot Studio tab, Launch Microsoft Edge, or open a new browser Tab and navigate to <https://copilotstudio.microsoft.com>

2. Select **Library** on the left menu, find your agent's name in the list displayed and click it

   ![Select Library](media/botlist_1.png)

3. Edit your agent instructions by adding the following statement `  - Account Revenue, must be retrieved from internal data sources WITHOUT any citation, writing only the name` after the statement `- Dividend per share history for the last five years in a table with columns for dividend and year.` and **Save**

4. Next, scroll down to **Actions** section and click **Add action** button.

   ![Add Action](media/addaction_1.png)

5. In the dialog box that opens up with the list of the actions, search for **list rows**, and select the **List rows from selected environment** action from the list of results

   ![Update Instructions](media/instrcutionsupdate.png)

6. Search for **list rows**, scroll down until **List rows from selected environment** is displayed and click on it

   ![Add action](media/listrowsfromselectedenvironment.png)

7. Click **Next** to create a Dataverse connection

   ![Dataverse Connection](media/dataverseconnect.png)

8. Provide the value `List existing accounts with account revenue` for the following fields:

   - Name
   - Description for the agent to know when to use this action
   - Usage Description

   ![Add action](media/actiondescr.png)

9. Expand **Inputs and outputs**, and scroll down to the **Environment** section

   ![Inputs and outputs](media/inputsoutputs.png)

10. Select **Set as value** in the drop down list

    ![Agent Input](media/agentinput.png)

11. Type the url of your Dataverse environment in the **Value** textbox and click **Done**

    ![Org url](media/orgurl.png)

    > You can get the environment url by selecting the **Settings** icon in the **CoPilot Studio** top bar, and selecting session details from the side bar that opens up, as shown below:
    >
    > ![Session Details](media/sessiondetails.png)
    >
    > From the dialog box that opens up, you can copy the highlighted url:
    >
    > ![Dataverse Environment URL](media/sessiondetails_1.png)

12. Click **Table name**

    ![Agent Input](media/tableinput.png)

13. Select **Set as value** in the drop down list

    ![Table Input](media/selectaccount.png)

14. Type "accounts" in the **Value** textbox and click **Done**

15. Click **Add Action**

    ![Add Action](media/addaction2.png)

16. Click **Save**

    ![Add Action](media/savebot.png)

17. Refresh the declarative agent [step 14 in exercise 1]

The agent is now configured to include information about the revenue, that is stored in the Account table in the Dataverse (CRM System)

19. Select "Provide an executive summary report for Microsoft" from the Starter prompts and verify the a new section **Account Revenue** is shown in the response

    ![Revenue](media/revenue.png)

20. Publish the bot like it has been done in Excerise 1 (steps 22 to 26), and click **Update** on the last step.
