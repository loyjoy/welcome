1. Copy process from toolbox
  - basic rundown: set the variables (from website / questionnaire in chat) -> ProCampaign subprocess
  - variables have to be set:
    - procampaign_rating_product - from website
    - procampaign_rating_url - from website
    - procampaign_rating_is_recommended - questionnaire
    - procampaign_rating_text - questionnaire
    - procampaign_rating_title - questionnaire
    - procampaign_rating_value - questionnaire
2. Configure ProCampaign integration:
  - if reviews are open (NIVEA X): Only normal API key is needed
  - if only logged-in users can send reviews: Add alternative API key (for cookie requests) -> should have more rights in ProCampaign
