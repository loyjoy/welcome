## Sign in

Customers enter their email addresses to sign in. Stored in CRM. Customers can log in again later and access their profile. If they log in on a different device or another channel (WhatsApp, Facebook, WeChat, Alexa, Google) they receive a PIN to verify their identity.

This process module is necessary for every process module that collects personal information like first name or birth date.

![sign_in_demo](https://raw.githubusercontent.com/loyjoy/welcome/master/help/bots/processes/subprocesses/sign_in_demo.png)

### Code email

An email containing a verification code is sent when a user that has registered in the chat comes back and enters the same email address again. 

Then this UI element appears and asks that user to enter the code that they received via email:

![grafik](https://user-images.githubusercontent.com/8091176/125278223-bf19fd00-e312-11eb-896a-76e1f9315c6a.png)

This email verification step is important so that no data can leaked or settings can be changed for a previously registered user. If we would not verify the users on their second log in, anyone could log in with any email address.

By applying the setting `Verify email with code on first use` you can also instruct LoyJoy to verify every log-in.
