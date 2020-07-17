# How to send reminder emails from ProCampaign

## 1. What this solutions will do for you

Some of your chat bots aim to get your customers to return to the chat bot after a certain time. Loyalty experiences or the advent calendar in particular are use cases where your customers ideally return to the chatbot. You can offer to remind your customer via emails to ensure that they return to your chat experience. To do this, you need to ask them to confirm. This article describes **how you can use ProCampaign** to send reminder emails to your customers with your unique sender address and branding. LoyJoy will automatically transfer your reminder email data to ProCampaign.

## 2. What you need for this solution

To start transfer the participants from LoyJoy to ProCampaign you will need two things - **your ProCampaign admin will help you out** with this:

 - The **Reminder list name** in ProCampaign
 - The **Reminder transaction name** in ProCampaign
 - The **API key that has the needed rights** to send the transaction

## 3. Add particular process block to your chat flow

Create or copy an new experience and add the **`Reminder Opt-in`** process block to your chatflow. Also add the **`Sign In`** process block if your chat flow does not have it yet. The sign up process block collects the email adresses from your customers as a registration for the individual customer. In case of an Advent Calender chatbot, the `Reminder Opt-in` process block requires a `Sign in` to identify the customer and with his consent send him reminders in the future. 

<p align="center">
  <img src="PIN/reminder_optin_processbrick.png" alt="reminder optin process block in LoyJoy" title="Sign In Process Block in LoyJoy" width="600"/>
</p>

Close the process editor and go to the `Reminder opt-in` process brick. Here you can edit the texts displayed in the chat. Only the `Ask your customers if they opt-in for the reminder`field is required.

<p align="center">
  <img src="PIN/reminder_main.png" alt="reminder optin process block in LoyJoy" title="Sign In Process Block in LoyJoy" width="600"/>
</p>

In the `Reminder double opt-in email` section, you can configure the email which will be send to your customers as a reminder email for your chat experience. Because we want to send our reminder emails from ProCampaign, we will activate the button `Do not send double opt-in email` in order to deactivate the LoyJoy build-in email service.

<p align="center">
  <img src="PIN/reminder_double.png" alt="reminder optin process block in LoyJoy" title="Sign In Process Block in LoyJoy" width="600"/>
</p>
<p align="center">
  <img src="PIN/reminder_double_off.png" alt="reminder optin process block in LoyJoy" title="Sign In Process Block in LoyJoy" width="600"/>
</p>

Scroll down to `Other texts` and edit the field `If the customer is not yet logged in` to configure the message which will ask your customer to enter his email to be reminded via email.

<p align="center">
  <img src="PIN/reminder_othertexts.png" alt="reminder optin process block in LoyJoy" title="Sign In Process Block in LoyJoy" width="600"/>
</p>

Cool! :tada: You just created your reminder email option in the LoyJoy chat. Congrats!

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

Scroll down to the section 'Cases where only the transaction name to be sent can be set'. Now enter the **Reminder list name** and the **Reminder transaction name** in the corresponding fields in LoyJoy. This will trigger the associated action in ProCampaign and send the requested reminder email to your customer. Optionally, you can also enter the name of the attribute where the reminder agreement text from the chat is written in the **Reminder consent** field.

<p align="center">
  <img src="PIN/api_reminder.png" alt="API PIN Email" title="API PIN Email in LoyJoy" width="800"/>
</p>

Scroll down and activate the integration for your bot in the field "Choose on which bots the integration should be active". Click on "Add a mapping" to create a mapping for the email field. Then choose `process variable` and type in **customer_email** to refer to your data field in your chat flow. Now just type in the source name of the data field in ProCampaign **Email**.

<p align="center">
  <img src="newsletter/procampaign_newsletter_customer_email_api.png" alt="LoyJoy to ProCampaign API newsletter section mapping" title="LoyJoy to ProCampaign API newsletter mapping" width="800"/>
</p>

Congratulations! You just have successfully connected your LoyJoy chatbot with ProCampaign and from now on all reminder emails will be automatically send by ProCampaign. Good job! :tada:
