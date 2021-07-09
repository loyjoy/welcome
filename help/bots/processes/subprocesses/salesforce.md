## Salesforce Service Cloud

Integrate Salesforce Service Cloud (SFSC) into the process.

You can create new objects in SFSC or update existing ones. Use mappings to configure which data should be written to which object:

![grafik](https://user-images.githubusercontent.com/8091176/125075484-f8f2c580-e0be-11eb-85c6-14d386ed146f.png)


### SFSC Configuration

You will need to create a Connected App in SFSC for the connection to work.

LoyJoy needs the `api` and `refresh_token` OAuth Scopes. Additionally you need to set the Callback URL in the OAuth settings:
![grafik](https://user-images.githubusercontent.com/8091176/125076203-ec22a180-e0bf-11eb-981c-b8bd87df5211.png)

This is where you find the callback URL:
![grafik](https://user-images.githubusercontent.com/8091176/125075900-80403900-e0bf-11eb-8136-5d30add8d93f.png)

These are the required settings for the refreh token:
![grafik](https://user-images.githubusercontent.com/8091176/125075831-6bfc3c00-e0bf-11eb-8175-bba1c3512dea.png)

After you have adjusted the settings in SFSC you can authenticate LoyJoy by clicking this button:
![grafik](https://user-images.githubusercontent.com/8091176/125075972-964df980-e0bf-11eb-9ba5-1a25c6922ca1.png)

You should see a message like this, showing that everything worked:
![grafik](https://user-images.githubusercontent.com/8091176/125076050-b7164f00-e0bf-11eb-915f-5cf12c79eb66.png)

### Example

This is an example flow which first registers a customer, asks them for their first and last name and then creates / updates a contact in SFSC accordingly:
![grafik](https://user-images.githubusercontent.com/8091176/125079060-7ae4ed80-e0c3-11eb-96fe-ea0d99c12f5c.png)

The connection is configured as described above:
![grafik](https://user-images.githubusercontent.com/8091176/125079196-a071f700-e0c3-11eb-9db0-310cb6aef4b2.png)

There are three mappings: One for each of the fields to be mapped (email, first name, last name):
![Unbenannt](https://user-images.githubusercontent.com/8091176/125080004-90a6e280-e0c4-11eb-98de-6e0c6a2b1512.png)

Like mentioned above, the email field is configured here to act as primary key in the connection to SFSC. Before creating a new contact, SFSC is queried for a contact with this email address. If one exists, it is updated with the data from LoyJoy. If not, a new contact with the data from LoyJoy is created.

By removing the checkbox "Use field to check for existing record" we could instruct LoyJoy to always create new contact objects.



