# How to transfer data from LoyJoy to ProCampaign

## 1. What this solution will do for you

Basically, all kinds of data can be flexibly sent from LoyJoy to ProCampaign as attributes. In this article you'll learn how transfer data to ProCampaign.

This article has two sections (A and B). In **section A** you'll learn how to transfer the following data from LoyJoy to ProCampaign:

  - Newsletter subscribers ([check out our separate article](https://github.com/loyjoy/welcome/blob/master/documentation/pro_campaign/PRO_CAMPAIGN_INTEGRATION.md)).
  - Reminder email subscribers (single-opt-in is sent to ProCampaign, double-opt-in email sent via ProCampaign)
  - Giveaway (raffle) participations
  - Advent calendar winners
  - Postal addresses
  - PIN emails

In **section B** you'll learn how transfer other data to ProCampaign.

## 2. What you need for the data transfer

You need an API key for ProCampaign that must be set up to **allow writing of the data fields that you want to transfer**. Your ProCampaign admin will be able to help you.

## Section A

## A 1. Configure the data transfer

In LoyJoy, go to settings, then choose integration. Choose ProCampaign and click on "Add now".

![settings](pro_campaign_integration/image6.png)

Scroll down until you see the "ProCampaign Integration". In the fields you can configure the data transfer.
  
![integration](pro_campaign_integration/image1.png)
  
The following screenshot shows an example for newsletter settings.
  
![integrationfield](pro_campaign_integration/image4.png)

## Section B

## B 1. Define custom data points (variables) in LoyJoy

As you know, in LoyJoy you can create custom variables and store them in the customer database. You can pick any customer variable that is stored in LoyJoy and send them to ProCampaign. Variables can be set for example via the "Variable" process building block or in a "Questionnaire".

Here is an example for a variable created in a questionnaire.

![variable](pro_campaign_integration/image2.png)

Here is an example for a variable set with the "Variable" process brick.

![questionnaire](pro_campaign_integration/image3.png)

## B 2. Transfer your data to ProCampaign

You can trigger to send custom data to a ProCampaign transaction with the "ProCampaign" building brick. Add the brick to your process and configure it.

![procampaign](pro_campaign_integration/image5.png)
 
