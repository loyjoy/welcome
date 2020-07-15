# How to transfer data from LoyJoy to ProCampaign

## 1. What this solution will do for you

In this article you'll learn how to transfer the following data from LoyJoy to ProCampaign:

  - Newsletter subscribers
  - Reminder email subscribers
  - Giveaway (raffle) participations
  - Advent calendar winners
  - Postal addresses
  - PIN emails

## 2. What you need for the data transfer

You need an API key for ProCampaign that must be set up to **allow writing of the data fields that you want to transfer**. Your ProCampaign admin will be able to help you.

## 3. Configure the data transfer

In LoyJoy, go to settings, then choose integration. Choose ProCampaign and click on "Add now".

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration.png" alt="LoyJoy to ProCampaign" width="800"/>
</p>

This will add a new tab with the name "ProCampaign" below the cards.

Scroll down to "General settings".

- Set a name for your integration (since you can have several integrations this will help you keeping track of)
- Enter your API key that you got from your ProCampaign admin

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_general_settings.png" alt="LoyJoy to ProCampaign" width="600"/>
</p>

Scroll down until you see a tab called "Add mapping". A mapping maps field names from LoyJoy to field names in ProCampaign.

- Choose the LoyJoy bot(s) that you want to use the integration in
- Click "Add mapping" to add a new mapping
- Choose "Process variable" from the Source dropdown
- Enter the variable name from LoyJoy that you want to transfer as Source
- Enter the target name of the data field that you store in ProCampaign

<p align="center">  
  <img src="pro_campaign_integration/pro_campaign_mapping.png" alt="Mapping settings LoyJoy to ProCampaign" width="800"/>
</p>

## 4. How to set custom data points (variables) in LoyJoy

As you know, in LoyJoy you can create custom variables and store them in the customer database. You can pick any customer variable that is stored in LoyJoy and send them to ProCampaign. Variables can be set for example via the "Variable" process building block or in a "Questionnaire".

Here is an example for a variable created in a questionnaire.

<p align="center">
  <img src="pro_campaign_integration/questionnaire_set_variable.png" alt="Setting a variable in a questionnaire" width="800"/>
</p>

Here is an example for a variable set with the "Variable" process brick.

<p align="center">
  <img src="pro_campaign_integration/variable_set_variable.png" alt="Setting a variable with the 'variable' process brick" width="800"/>
</p>

## 5. Transfer your data to ProCampaign

You can trigger to send custom data to a ProCampaign transaction with the "ProCampaign" building brick. Add the brick to your process and configure it.

 <p align="center">
  <img src="pro_campaign_integration/pro_campaign_process_brick_transaction.png" alt="ProCampaign process brick in LoyJoy chat editor" width="800"/>
</p>
