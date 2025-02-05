**Ground the agent responses in enterprise data**

In this exercise the agent will be configured to ground the executive summary report with the information available in company´s CRM system. The report will include information about the revenue, that is stored in the Account table in the Dataverse (CRM System).

In the next steps the account information will be populated into the Accounts table

1. On Microsoft Edge browse to [https://make.powerapps.com/environments/default-4cfe372a-37a4-44f8-91b2-5faf34253c62/entities/70816501-edb9-4740-a16c-6a5efbc05d84](https://make.powerapps.com/environments/default-4cfe372a-37a4-44f8-91b2-5faf34253c62/entities/70816501-edb9-4740-a16c-6a5efbc05d84)

![data import settings ](media/dataimport1.png)

2. Click on the bottom arrow

![data import settings ](media/dataimport2.png)

3. Type "Annual" on the search text box

![data import settings ](media/dataimport3.png)

4. Select **Annual Revenue** and click **Save**

5. Type "Microsoft" for the Account Name and 1000000 for the Annual Revenue

6. Type "Ford" for the Account Name and 2000000 for the Annual Revenue

![data import settings ](media/dataimport6.png)


The account information has now been populated in the account table , let´s now start the Copilot Studio required configurations


1. Case you have closed the Copilot Studio tab do the following steps otherwise skip to step 5

2. Open Microsoft Edge and navigate to <https://copilotstudio.microsoft.com>

3. Select **Library** on the left menu

![Select Library](media/library.png)

4. Find your agent name in the list displayed and click on it

![Select Library](media/botlist.png)


5. edit your agent instructions by adding the following statement "- Primary Contact, must be retrieved from internal data sources without any citation, writing only the name" after "- Dividend per share history for the last five years in a table with columns for dividend and year." 

6. Click **Add action**, the connector list is displayed

<add screenshot>

![Update Instructions](media/instrcutionsupdate.png)

6.  Search for **list rows**, scroll down until **List rows from selected environment** is displayed and click on it (highlight search box)

![Add action](media/listrowsfromselectedenvironment.png)

7. Click **Next** to create a Dataverse connection

![Dataverse Connection](media/dataverseconnect.png)

8. Provide the value "List existing accounts with account revenue" in the fields:
- Name
- Description for the agent to know when to use this action
- Usage Description

![Add action](media/actiondescr.png)

9. Expand **Inputs and outputs** and scroll down

10. Click **Environment**

![Inputs and outputs](media/inputsoutputs.png)

11. Select **Set as value** in the drop down list

![Agent Input](media/agentinput.png)

12. Type the url provided in the **Value** textbox and click **Done**

![Org url](media/orgurl.png)



13. Click **Table name**

![Agent Input](media/tableinput.png)

14. Select **Set as value** in the drop down list

![Table Input](media/selectaccount.png)

15. Type "accounts" in the **Value** textbox and click **Done**

16. Click **Add Action**

![Add Action](media/addaction2.png)

17. Click **Save**

![Add Action](media/savebot.png)

18. Refresh the declarative agent [step 14 in exercide 1] 

The agent is now configured to include information about the revenue, that is stored in the Account table in the Dataverse (CRM System) 

19. Select "Provide an executive summary report for Microsoft" from the Starter prompts and verify the a new section revenue is returned

![Revenue](media/revenue.png)

20. Publish the bot like it has been done [step 22-26 in exercise 1] , clik **Update** on the last step
 
 















