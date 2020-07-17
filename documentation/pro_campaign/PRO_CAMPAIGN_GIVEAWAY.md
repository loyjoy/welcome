# How to transfer giveaway participants from LoyJoy to ProCampaign

## 1. What this solutions will do for you

LoyJoy lets you create a giveaway for your customers within the chat experience. Your customers will be asked to enter their email address in order to participate. 
In addition you can draw the winners on the platform and export them.

You can **automatically transfer your new giveaway participants to your ProCampaign database**. LoyJoy will transfer your participants' email addresses to ProCampaign.

## 2. What you need for this solution

To start transfer the participants from LoyJoy to ProCampaign you will need three things - your ProCampaign admin will help you out with this:

 - The **Participation transaction name** in ProCampaign.
 - The **Participation list name** in ProCampaign.
 - The **API key that has the needed rights** to send the transaction.

## 3. Add the `Giveaway participation` process block to your chat flow

Create or copy an new experience and add the `Giveaway participation` process block. 

<p align="center">
  <img src="giveaway/giveaway_process_block.png" alt="giveaway process block in LoyJoy" title="Giveaway Process Block in LoyJoy" width="600"/>
</p>

Turn off the double-opt-in email in LoyJoy (as this email will be sent by ProCampaign).

<p align="center">
  <img src="pro_campaign_integration/procampaign_email_off.png" alt="Switch off double opt-in" width="800"/>
</p>

## 4. Configure the data transfer

You completed all the configurations within the chat. Now you have to set up the data transfer.

On the LoyJoy platform, go to settings, then choose integration. Choose ProCampaign and click on "Add now".

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration.png" alt="LoyJoy to ProCampaign" title="LoyJoy to ProCampaign" width="800"/>
</p>

This will add a new tab with the name "ProCampaign" below the cards.

Scroll down to "General settings".

Set a name for your integration (since you can have several integrations this will help you keep an overview).
Enter **your API key** that you got from your ProCampaign admin.

<p align="center">
  <img src="pro_campaign_integration/procampaign_api_key.png" alt="LoyJoy to ProCampaign API key section" title="LoyJoy to ProCampaign API key" width="800"/>
</p>  

Scroll down to the section `Fields for newsletter single opt-in`. Now fill in the `Newsletter list name` and the `Newsletter transaction name` into the according fields in LoyJoy. 

<p align="center">
  <img src="newsletter/procampaign_api_newsletter.png" alt="LoyJoy to ProCampaign API newsletter section" title="LoyJoy to ProCampaign API newsletter" width="800"/>
</p>

The following fields are optional:
- `Newsletter consent`: If set, the text that the user confirmed to subscribe in the chat will be sent as an attribute to ProCampaign.
- `Newsletter Ident_long`: Ident_long transaction parameter (Defaults to "Newsletter Subscription")


Scroll down and activate the integration for your bot in the field "Choose on which bots the integration should be active". Click on "Add a mapping" to create a mapping for the email field. Then choose `process variable` and type in `customer_email` to refer to your data field in your chat flow. Now just type in the source name of the data field in ProCampaign `Email`.

<p align="center">
  <img src="newsletter/procampaign_newsletter_customer_email_api.png" alt="LoyJoy to ProCampaign API newsletter section mapping" title="LoyJoy to ProCampaign API newsletter mapping" width="800"/>
</p>

Congratulations! You just have successfully connected your LoyJoy chatbot with ProCampaign and all Newsletter Opt-ins within the chat will automatically tranferred to ProCampaign.:tada:
