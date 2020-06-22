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

All other customer variables saved in during the chat can also be sent to ProCampaign. Variables can be set via the Variable process building block or a questionnaire.

![variable](procampaign_integration/image2.png)

![questionnaire](procampaign_integration/image3.png)

### Sending the data to ProCampaign
- The data will be sent in all transactions to ProCampaign
- ProCampaign transactions can be triggered manually using a ProCampaign process block
- Also ProCampaign transactions are triggered automatically e.g. on newsletter single-opt-ins
  - For automatic transactions you only have to fill out the transaction fields in the integration:
  ![integrationfield](procampaign_integration/image4.png)
  - These automatic transactions are implemented:
    - Newsletter single-opt-in
    - Reminder single-opt-in
    - Giveaway participation
    - Instant win participation
    - Postal address entered
    - PIN 
    - Advent calendar winner drawn

### Things to consider
- The API key for ProCampaign must be set up to allow writing of the attributes you want to send
