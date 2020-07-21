# How to transfer newsletter subscribers from LoyJoy to ProCampaign

## 1. What this solutions will do for you

LoyJoy can acquire newsletter subscribers within every chat flow that contains the `Newsletter opt-in` process brick. 

It's easy to **automatically transfer new newsletter subscribers to your ProCampaign database**. LoyJoy will transfer the single opt-ins to ProCampaign, and ProCampaign will then send the double opt-in email to the new subscribers. In LoyJoy you will only see the single opt-ins, while ProCampaign also stores the double opt-ins. This is a one-way integration, meaning the subscribers and their consents will be managed in ProCampaign only.

## 2. What you need for this solution

To start sending newsletter subscribers from LoyJoy to ProCampaign you will need three things - your ProCampaign admin will help you out with this:

 - The name of your **newsletter transaction** in ProCampaign.
 - The name of your **newsletter list** in ProCampaign.
 - An **API key that has the needed rights** to modify the attributes / send the transaction.

## 3. Add the newsletter opt-in process block to your chat flow

Create or copy an new experience and add the `Newsletter opt-in` process block. Please add the `sign in` process block as well as the `ProCampaign` process block.

<p align="center">
  <img src="newsletter/add_newsletter-block.png" alt="newsletter opt-in in LoyJoy" title="LoyJoy Newsletter Process Block" width="800"/>
</p>

Turn off the double-opt-in email in LoyJoy (as this email will be sent by ProCampaign).

<p align="center">
  <img src="pro_campaign_integration/procampaign_email_off.png" alt="Switch off double opt-in" width="800"/>
</p>

Now we configure our process block `ProCampaign` to transfer the data from LoyJoy to a corresponding transaction and data field in ProCampaign.

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration_transaction.png" alt="Configure a ProCampaign transaction" title="Configure a ProCampaign transaction" width="800"/>
</p>

Now you can test the data transfer and you are ready to go!

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


Scroll down and activate the integration for your bot in the field "Choose on which bots the integration should be active". Click on "Add a mapping" to create a mapping for the email field. Then choose `process variable` and type in **customer_email** to refer to your data field in your chat flow. Now just type in the source name of the data field in ProCampaign **Email**.

<p align="center">
  <img src="newsletter/procampaign_newsletter_customer_email_api.png" alt="LoyJoy to ProCampaign API newsletter section mapping" title="LoyJoy to ProCampaign API newsletter mapping" width="800"/>
</p>

Congratulations! You just have successfully connected your LoyJoy chatbot with ProCampaign and all Newsletter Opt-ins within the chat will automatically tranferred to ProCampaign.:tada:
