# Connect a LoyJoy bot to Facebook Messenger

Every chatbot on the Facebook platform is manually checked by Facebook and only then is it activated. The steps required to set up and submit a chatbot are explained below. Some steps may have already been completed, so you can simply skip them. Setup is not always self-explanatory. LoyJoy has no influence on this procedure.

1. You need a Facebook page for your chatbot. Copy the page ID of your page, you will enter the ID afterwards at LoyJoy.

![image3](facebook_integration/image3.png)


2. Create a Facebook app for your chat bot that goes here. Skip the quick start by clicking the "skip and create app ID" button.

![image9](facebook_integration/image9.png)


3. Give your app a name (this will later be the name in Facebook Messenger) and choose a contact email address where you can be reached

![image5](facebook_integration/image5.png)


4. Now you can select a "scenario" on Facebook. This is not necessary, scroll to the bottom of the page and click "skip"

![image4](facebook_integration/image4.png)


5. Now set up your app for Facebook Messenger by selecting the Messenger tile and clicking "Set up"

![image10](facebook_integration/image10.png)


6. Your app needs the pages_messaging feature to send and receive messages on Facebook. Add this to your submission.

![image6](facebook_integration/image6.png)


7. If you want to submit pages_messaging, you need to add some details, click "Add details".

![image17](facebook_integration/image17.png)


8. On the following page, you need to make four settings. Not visible in the screenshot is the commercial use setting located under the logo upload.

![image11](facebook_integration/image11.png)


9. Then go to Messenger > Settings in the left menu. Here go to the Access Key section. Select the page you want to connect to the chatbot. Then click on the button "Edit permissions".

![image7](facebook_integration/image7.png)


10. A new window will open, here you have to perform several steps. The prerequisite for this is that your company and you as a person / administrator have been personally verified on Facebook. If not already done, please perform the verifications. Then you can read on here.

![image18](facebook_integration/image18.png)
![image12](facebook_integration/image12.png)
![image13](facebook_integration/image13.png)


11. After the verification (which is under review first) you will receive your page access key. Please copy it. Just like the App-ID shown above.

![image2](facebook_integration/image2.png)


12. Now you can copy the three information from Facebook (page ID, app ID and page access key) into your LoyJoy bot. To do this, go to the "Integration" tab in the Bot (really in the Bot, not in an Experience!) and expand the "Facebook" area. Put the three pieces of information in the right place. Then copy the "Webhook URL" from LoyJoy.

![image16](facebook_integration/image16.png)
![image1](facebook_integration/image1.png)


13. You can now paste the webhook URL you just copied from LoyJoy into the "Callback URL" field on Facebook. Under Confirm token you can enter a random character string. Then hook the four options messages, message_deliveries, messaging_postbacks and message_reads. Then click "Confirm and save".

![image15](facebook_integration/image15.png)


14. Your Facebook app is still in development mode, which you can only test internally. Customers are not yet able to access it. The app (i.e. your chatbot) still has to be activated. A team from Facebook will test the chat.


15. Scroll down to "Current submission". Click on "Add details".

![image14](facebook_integration/image14.png)


16. Here you must first accept that you will not send any promotional messages via Messenger. You must also describe your chatbot experience in detail and create a screencast if necessary. You will find all information about this there. Please read the information on the Facebook page carefully.

![image8](facebook_integration/image8.png)
![image19](facebook_integration/image19.png)
