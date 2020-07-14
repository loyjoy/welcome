# How to transfer ratings and reviews from LoyJoy to ProCampaign

## What this solution will do

Customers will be able to rate a product within the chat. The rating will then automatically be transferred to ProCampaign.

There are only three requirements:

1. Variables have to be set in the process
2. ProCampaign process brick with ratings configuration
3. Configuration of the ProCampaign integration

## 1. Set variables in process

You can simply copy the ratings & review process from the toolbox. See below for a detailed explanation.

All the data we send to ProCampaign for the review must first be present as variables in the LoyJoy process.

We can create such variables using the `Variable` process brick or using a `Questionnaire`. A `Variable` process
brick should be used when the data is not influenced by the user, but set e.g. by the website the chatbot is on.
A `Questionnaire` should be used for all instances where user input is needed.

These are the variables required to send a full review:
  - procampaign_rating_product - `Variable` / `Questionnaire`
  - procampaign_rating_url - `Variable` / `Questionnaire`
  - procampaign_rating_is_recommended -`Questionnaire` 
  - procampaign_rating_text - `Questionnaire`
  - procampaign_rating_title - `Questionnaire`
  - procampaign_rating_value - `Questionnaire`

## 2. Set up ProCampaign process brick

This is also already present in the toolbox process.

For this step, you simply add a `ProCampaign` process brick and select `Send review` in its settings.

## 3. Configure ProCampaign integration

In the ProCampaign integration, you only have to add the API key (see below) and a basic mapping, mapping `customer_email` to `Email`.

The requirement for the API keys is different, depending on whether reviews are only allowed for logged in users or for all users:

  - if reviews are open (NIVEA X): Only normal API key is needed
  - if only logged-in users can send reviews: Add alternative API key (for cookie requests) -> should have more rights in ProCampaign
  
  
