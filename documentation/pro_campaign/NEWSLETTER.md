# How to add newsletter subscribers from LoyJoy to ProCampaign

## What this solutions will do for you

LoyJoy can acquire newsletter subscribers within every chat flow that contains the "newsletter opt-in" process brick. By default, new subscribers and their consents are stored in the LoyJoy database. It's also simple to transfer newsletter subscribers to your ProCampaign database automatically. LoyJoy will transfer the single opt-ins (SOI) to ProCampaign, and ProCampaign will then send the double opt-in email to the new subscribers. In LoyJoy you will only see the single opt-ins, while ProCampaign also stores the double opt-ins. Plase note: this is a one-way integration, meaning the subscribers and their consents will be managed in ProCampaign only.

## What you need for the data connection

To start sending newsletter subscribers from LoyJoy to ProCampaign you will need three things:

1. The name of your newsletter transaction in ProCampaign (your ProCampaign admin will know this)
2. The name of your newsletter list in ProCampaign  (your ProCampaign admin will know this)
3. An API key that has the needed rights to modify the attributes / send the transaction (your ProCampaign admin will know this)

## How to configure the connection

Three steps are necessary to configure the integration in LoyJoy:

1. Create or copy an experience that contains a "newsletter opt-in" process brick. 

![process](newsletter/process.png)

2. Turn off the double-opt-in email in LoyJoy (as this email will be sent by ProCampaign).

![email_off](newsletter/email_off.png)

3. Configure the ProCampaign integration in LoyJoy.
   1. Go to settings in the top menu, look for the ProCampaign card and click on "Add now".
   2. Scroll down to "Integrate ProCampaign".
   1. Fill in your API key, the list name, and the transaction name into the according fields in LoyJoy. There is a section "Fields for newsletter single opt-in".
   2. Activate this integration for the Bot you are using by choosing the bot from the list "Choose on which bots the integration should be active".
   3. Click on "Add a mapping" to create a mapping for the email field as pointed out below (you could add more fields of course, but here we are focusing on the email address).

![integration](newsletter/integration.png)


## Optional Fields in the Integration Settings
- Newsletter consent: If set, the text that the user confirmed to subscribe in the chat will be sent as an attribute to ProCampaign.
- Ident_long: Ident_long transaction parameter (Defaults to "Newsletter Subscription")
- Create Account: post data to `Account/Register` instead of `Consumer` endpoint

From the general settings:
- `Privacy policy` & `Privacy policy URL`: Content from the URL can be written to an attribute with the name given in the
  `Privacy policy` field
