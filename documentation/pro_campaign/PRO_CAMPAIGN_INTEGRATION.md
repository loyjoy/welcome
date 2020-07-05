# How to transfer data from LoyJoy to ProCampaign

## 1. What this solution will do for you

Basically, all kinds of data can be flexibly sent from LoyJoy to ProCampaign as attributes.

In this article you'll learn how transfer the following data from LoyJoy to ProCampaign:

  - Newsletter subscribers ([check out our separate article](https://github.com/loyjoy/welcome/blob/master/documentation/pro_campaign/PRO_CAMPAIGN_INTEGRATION.md)).
  - Reminder email subscribers (single-opt-in is sent to ProCampaign, double-opt-in email sent via ProCampaign)
  - Giveaway (raffle) participations
  - Advent calendar winners
  - Postal addresses
  - PIN emails

## 2. What you need for the data transfer

You need an API key for ProCampaign that must be set up to **allow writing of the data fields that you want to transfer**. Your ProCampaign admin will be able to help you.

## 3. Configure the data transfer

In LoyJoy, go to settings, then choose integration. Choose ProCampaign and click on "Add now".

![settings](pro_campaign_integration/image6.png)

Scroll down until you see the "ProCampaign Integration". In the fields you can configure the data transfer.
  
![integration](pro_campaign_integration/image1.png)
  
The following screenshot shows an example for newsletter settings.
  
![integrationfield](pro_campaign_integration/image4.png)

## 4. Define custom data points (variables) in LoyJoy

As you know, in LoyJoy you can create custom variables and store them in the customer database. You can pick any customer variable that is stored in LoyJoy and send them to ProCampaign. Variables can be set for example via the "Variable" process building block or in a "Questionnaire".

Here is an example for a variable created in a questionnaire.

![variable](pro_campaign_integration/image2.png)

Here is an example for a variable set with the "Variable" process brick.

![questionnaire](pro_campaign_integration/image3.png)

## 5. Transfer your data to ProCampaign

1. As mentioned above, some transactions in LoyJoy send data to ProCampaign automatically based the mappings in settings > integration
2. Additionally, you can trigger to send data to a ProCampaign transaction with the "ProCampaign" building brick

![procampaign](pro_campaign_integration/image5.png)
  
## List of default variables in LoyJoy

The following customer data fields (called variables in LoyJoy) are *always* available in LoyJoy:

- customer_country
- customer_email
- customer_firstname
- customer_gender
- customer_id
- customer_language_iso_6391
- customer_lastname
- customer_locality
- customer_phone
- customer_region_iso_31662
- customer_street
- customer_surrogate_id
- customer_zipcode

