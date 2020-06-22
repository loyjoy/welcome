# ProCampaign Integration

All kinds of data can be flexibly sent to ProCampaign as attributes. The mapping from LoyJoy to ProCampaign is set up in the integration:

![integration](procampaign_integration/image1.png)

There are a number of customer fields that are always accessible:
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

All other customer variables saved in during the chat can also be sent to ProCampaign:

![variable](procampaign_integration/image2.png)
![questionnaire](procampaign_integration/image3.png)

Things to consider:
- The API key for ProCampaign must be set up to allow writing of the attributes you want to send
