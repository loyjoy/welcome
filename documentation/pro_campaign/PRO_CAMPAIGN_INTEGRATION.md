# How to transfer data from LoyJoy to ProCampaign

## 1. What this solution will do for you

This article explains how to generally transfer a custom data field from LoyJoy to ProCampaign. For this example, we will use the "Favourite Colour" field.

## 2 What you need to make this solution work

You will need an API key for ProCampaign, which must be set up to **allow writing the data fields you want to transfer**. Your ProCampaign administrator will be able to help you with this.

## 3. Configure the data transfer

In LoyJoy, go to settings, then choose integration. Choose ProCampaign and click on "Add now".

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration.png" alt="LoyJoy to ProCampaign" title="LoyJoy to ProCampaign" width="800"/>
</p>

This will add a new tab with the name "ProCampaign" below the cards.

Scroll down to "General settings".

- Set a name for your integration (since you can have several integrations this will help you keeping track of)
- Enter your API key that you got from your ProCampaign admin

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_api_key.png" alt="API key for ProCampaign" title="API key for ProCampaign" width="800"/>
</p>

You might also want to set a Source for the data, so that you can identify where the data originated in ProCampain. This is also a field in general settings, just a bit below the API key setting.

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_source.png" alt="Set a source for ProCampaign" title="Set a source for ProCampaign" width="800"/>
</p>

Now scroll down until you see a tab called "Add mapping". A mapping maps field names from LoyJoy to field names in ProCampaign.

- Choose the LoyJoy bot(s) that you want to use the integration in (here: "MyBot")
- Click "Add mapping" to add a new mapping
- Choose "Process variable" from the Source dropdown
- Enter the variable name from LoyJoy that you want to transfer as Source (here: "favorite_color")
- Enter the target name of the data field that you store in ProCampaign (here: "Color")

<p align="center">  
  <img src="pro_campaign_integration/pro_campaign_integration_mapping.png" alt="Mapping settings LoyJoy to ProCampaign" title="Mapping settings LoyJoy to ProCampaign" width="800"/>
</p>

## 4. How to set the custom data fields (variables) in LoyJoy

In LoyJoy you can create custom data fiels, we call them **`variables`**, and store them in the LoyJoy customer database. You can pick any customer variable that is stored in LoyJoy and send it to ProCampaign. Variables can be set for example via the `Variable` process building block or in a `Questionnaire`.

We will create a variable "favorite color" in a questionnaire.

Let's build a small process that contains a `Questionnaire` and a `ProCampaign` process block.

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_process_bpmn.png" alt="Build a BPMN process in LoyJoy" title="Build a BPMN process in LoyJoy" width="800"/>
</p>

In the `questionnaire` we ask for the favorite color and offer three options (red, blue, green). We store the answers in a new variable called "favorite color".

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_questionnaire.png" alt="Create a questionnaire in LoyJoy" title="Create a questionnaire in LoyJoy" width="800"/>
</p>

In each answer (red, blue, green), we set the value of the variable. Here: red.

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_variable.png" alt="Create a variable in a questionnaire in LoyJoy" title="Create a variable in a questionnaire in LoyJoy" width="800"/>
</p>

## 5. Configure the transfer of your data to ProCampaign

Now we configure our process block `ProCampaign` to transfer the data from LoyJoy to a corresponding transaction and data field in ProCampaign.

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_transaction.png" alt="Configure a ProCampaign transaction" title="Configure a ProCampaign transaction" width="800"/>
</p>

Now you can test the data transfer and you are ready to go! :tada:

## 6. Typical obstacles

If you run into problems, here are some typical solutions:
- Have you selected the right bot(s) in the integration settings?
- Are the field names in ProCampaign written correctly?
- Has your API key the necessary rights? (check out the log in LoyJoy for error messages, you find it at the bottom of the page settings > integrations)

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_log.png" alt="Integration log in LoyJoy" title="Integration log in LoyJoy" width="800"/>
</p>



