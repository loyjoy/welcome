## Salesforce Service Cloud

Integrate Salesforce Service Cloud (SFSC) into the process.

You can create new objects in SFSC or update existing ones. Use mappings to configure which data should be written to which object:

![grafik](https://user-images.githubusercontent.com/8091176/125075484-f8f2c580-e0be-11eb-85c6-14d386ed146f.png)


### Configuration

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
