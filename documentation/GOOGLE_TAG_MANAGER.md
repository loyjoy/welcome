# Integrate data from your LoyJoy chat into your tracking solution

With a LoyJoy chat on your site you can connect with your customers in a great way. You can watch how your customers use the chat in the LoyJoy backend. You can also extract a lot of data from LoyJoy and integrate it directly into your own website tracking solution to collect all analytics data in one place.

## Tracking integration

The tracking integration is based on the LoyJoy JavaScript API. Through the JavaScript API, events are triggered for various events in the chat:


| Event name          | Event description |
|---------------------|------------------|
| hide                | The chat window was not displayed when loading or hidden (hidden) after loading via JavaScript API. |
| load                | The chat was loaded. |
| open                | The chat was opened. |
| show                | The chat was displayed / no longer hidden. |
|-- |-- |
| advent_calendar_door_asked | A customer was asked whether to open an advent calendar door. |
| advent_calendar_door_opened | A customer has confirmed to open an advent calendar door. |
| appointment_created | An appointment was created in the appointment process brick. |
| audio_message_requested | A customer was asked to record an audio message in the audio message process brick. |
| audio_message_uploaded | A customer has uploaded an audio message in the audio message process brick. |
| birthdate_entered | A customer has entered their birthday in the birthdate process brick. |
| campaign_message_sent | A campaign message was sent. |
| code_entered | A customer has entered a code in the code process brick. |
| code_entered_correct | A customer has entered a correct code in the code process brick.  |
| code_entered_incorrect | A customer has entered an incorrect code in the code process brick. |
| code_registered | A code entered by a customer was registered. |
| coupon_code_issued | A coupon code was issued to a customer in the coupon code process brick. |
| coupon_code_uploaded | A coupon code was uploaded in the LoyJoy backend. |
| customer_created | A customer was created. |
| customer_deleted | A customer was deleted. |
| customer_purged | Customers were purged in the LoyJoy backend. |
| customer_updated | A customer was updated, e.g. by entering personal information such as name or birthdate. |
| data_collection_answer | A user has given a pre-defined answer in a questionnaire process brick (this includes e.g. quick reply type questions, but not text type). |
| data_collection_answer_idontknow | A user has clicked the "I don't know option" in an questionnaire. |
| data_collection_question | A question was asked in a questionnaire.  |
| data_collection_question_answered | A question was answered in a questionnaire (this includes all question types). |
| data_collection_variable_set | A variable was set in a questionnaire. |
| end | The end of a process / chat flow was reached. |
| firstname_entered | A customer has entered their first name in a firstname process brick. |
| gender_diverse | A customer has entered their gender as diverse in a gender process brick. |
| gender_entered | A customer has entered their gender in a gender process brick. |
| gender_female | A customer has entered their gender as female in a gender process brick. |
| gender_male | A customer has entered their gender as male in a gender process brick. |
| handover_email_sent | A handover email was sent. |
| home_view_opened | The home view was opened (non-unique). |
| home_view_screen_time | 15 seconds of screen time were reached in a home view (iterative). |
| intent_evaluated | An intent was evaluated (i.e. a user has entered free text). |
| intent_matched | A matching intent (above threshold) was found when evaluating intents. |
| interaction | A user has interacted for the first time in a process / experience. |
| jump_auto | An automatic jump process brick was executed. |
| jump_decision_question | The question where to jump was asked in a jump decision process brick. |
| lastname_entered | A customer has entered their last name in a lastname process brick. |
| link_clicked | A link was clicked in a external link or product gallery process brick. |
| live_chat_duration | A certain duration was reached during a live chat. |
| live_chat_ended | A live chat was ended. |
| live_chat_started | A live chat was started. |
| loyalty_first_received | A customer has received their first loyalty points. |
| loyalty_points_emitted | Loyalty points were emitted to a customer. |
| loyalty_points_spent | A customer has spent loyalty points. |
| loyalty_referral | A customer has signed up after being referred by another customer via the loyalty referral process brick. |
| loyalty_reward_redeemed | A customer has redeemed their loyalty points for a reward. |
| mail_sent | A mail was sent in the mail process brick. |
| mail_to_customer_sent | A mail was sent in a mail to customer process brick. |
| main_prize_sent | The main prize was shown in the main prize process brick. |
| newsletter_double_opt_in | A customer has given the newsletter double opt-in via clicking the link in a double opt-in email. |
| newsletter_opt_out | A customer has opted out to newsletter via clicking the unsubscribe link in an email or the settings menu in chat. |
| newsletter_single_opt_in | A customer has given the newsletter single opt-in by agreeing in the chat. |
| newsletter_single_opt_in_asked | A customer was asked in chat whether they want to receive a newsletter. |
| newsletter_single_opt_in_rejected | A customer did not agree to receive the newsletter in chat. |
| nps_survey_free_text_answered | A customer has answered the text question in the NPS process brick. |
| nps_survey_score_0 | A customer has given the score of 0 in the NPS process brick. |
| nps_survey_score_1 | A customer has given the score of 1 in the NPS process brick. |
| nps_survey_score_2 | A customer has given the score of 2 in the NPS process brick. |
| nps_survey_score_3 | A customer has given the score of 3 in the NPS process brick. |
| nps_survey_score_4 | A customer has given the score of 4 in the NPS process brick. |
| nps_survey_score_5 | A customer has given the score of 5 in the NPS process brick. |
| nps_survey_score_6 | A customer has given the score of 6 in the NPS process brick. |
| nps_survey_score_7 | A customer has given the score of 7 in the NPS process brick. |
| nps_survey_score_8 | A customer has given the score of 8 in the NPS process brick. |
| nps_survey_score_9 | A customer has given the score of 9 in the NPS process brick. |
| nps_survey_score_10 | A customer has given the score of 10 in the NPS process brick. |
| participant_bpmn_process | A customer has participated for the first time in process / experience. |
| participant_giveaway | A customer has participated for the first time in a giveaway. |
| participation | A customer has participated in a giveaway. |
| password_entered | A customer has entered a password in the password process brick. |
| phone_number_entered | A customer has entered their phone number in a phone number process brick. |
| platform_facebook | A customer has chatted via Facebook messenger. |
| platform_rest | A customer has chatted via the chat UI on the website. |
| platform_viber | A customer has chatted via Viber. |
| platform_wechat | A customer has chatted via WeChat. |
| platform_whatsapp | A customer has chatted via WhatsApp. |
| postal_address_confirmed | A customer has confirmed the postal address they entered. |
| postal_address_updated | A customer has entered their postal address in a postal address process brick. |
| prize_details_sent | A customer has requested the details for a prize in a prize process brick. |
| prize_sent | A prize was sent in a prize process brick. |
| proceed_confirmed | A customer has proceeded in a proceed process brick. |
| process_liked | A customer has liked a process. |
| profiling_double_opt_in | A customer has given the profiling double opt-in via clicking the link in a double opt-in email. |
| profiling_opt_out | A customer has opted out to profiling via clicking the unsubscribe link in an email or the settings menu in chat. |
| profiling_single_opt_in | A customer has given the profiling single opt-in by agreeing in the chat. |
| profiling_single_opt_in_asked | A customer was asked in chat whether they agree to profiling. |
| profiling_single_opt_in_rejected | A customer did not agree to profiling in chat. |
| pub_sub_failed | A message to Pub/Sub could not be posted. |
| pub_sub_published | A message was posted to Pub/Sub in a Pub/Sub process brick. |
| questionnaire_question | A question was asked in a questionnaire (legacy).  |
| quiz_answer | A customer has used a pre-defined answer in a quiz. |
| quiz_answer_correct | A customer has given a correct, pre-defined answer in a quiz. |
| quiz_answer_freetext | A customer has given a free text answer in a quiz. |
| quiz_answer_incorrect | A customer has given an incorrect, pre-defined answer in a quiz.  |
| quiz_answer_not_freetext | A customer has given a pre-defined answer in a quiz. |
| quiz_question | A question was asked in a quiz. |
| reminder_double_opt_in | A customer has given the reminder double opt-in via clicking the link in a double opt-in email. |
| reminder_opt_out | A customer has opted out to reminder via clicking the unsubscribe link in an email or the settings menu in chat. |
| reminder_single_opt_in | A customer has given the reminder single opt-in by agreeing in the chat. |
| reminder_single_opt_in_asked | A customer was asked in chat whether they agree to receive a reminder. |
| reminder_single_opt_in_rejected | A customer did not agree to receive a reminder in chat. |
| reset | A customer has triggered a chat reset. |
| restart | A customer has triggered a process re-start via the chat menu. |
| reward_redeemed | A customer has redeemed a reward in a rewards process brick. |
| screen_time | Screen time was recorded in a chat. |
| sign_in | A customer has signed in. |
| sign_in_email_address_blocked | An email address was blocked because it was found on the block list for one-time email hosters.  |
| sign_in_ip_address_blocked | A customer was blocked from signing up because there were already too many sign ups from their IP address. |
| sign_in_pin_failed | A customer has entered an incorrect PIN / code when signing up / signing in. |
| sign_in_pin_mail_sent | A customer was sent an email with their PIN / code. |
| sign_in_pin_succeeded | A customer has entered a correct PIN / code when signing up / signing in. |
| sign_out | A customer has signed out via the chat menu. |
| sign_up | A new customer has signed up. |
| sign_up_requested | A customer was asked to sign up via entering the email address. |
| sms_double_opt_in | A customer has confirmed the text message double opt-in via entering the code they received via text. |
| sms_opt_in_code_sent | A customer has received a code via text in the text opt-in process brick. |
| sms_single_opt_in | A customer has given the text single opt-in by agreeing in the chat. |
| sms_single_opt_in_asked | A customer was asked in chat whether they agree to receive text messages. |
| sms_single_opt_in_rejected | A customer did not agree to receive texts in chat. |
| snapshot_barcode_scanned | A customer has scanned a barcode in a snapshot process brick. |
| snapshot_image_uploaded | A customer has uploaded an image in a snapshot process brick. |
| start | A process was started. |
| story_read | A customer has read a story. |
| sub_process_visited | A sub process / process brick was shown to a customer. |
| terms_accepted | A customer has accepted the experience / process terms. |
| terms_rejected | A customer has rejected the experience / process terms. |
| user_agent_desktop | A customer on a dektop computer has chatted. |
| user_agent_mobile | A customer on a mobile device has chatted. |
| variable_set | A variable was set in a variable process module. |
| web_push_double_opt_in | A customer has given the web-push double opt-in via agreeing to the question shown by their browser. |
| web_push_opt_in_subscription_request | A request was sent to a customer's browser to ask for web-push opt-in. |
| web_push_single_opt_in | A customer has given the web-push single opt-in by agreeing in the chat. |
| web_push_single_opt_in_asked | A customer was asked in chat whether they agree to receive web-push messages. |
| web_push_single_opt_in_rejected | A customer did not agree to receive web-push messages in chat. |
| web_push_subscription_gone | A customer's web-push subscription (handled by the browser) could not be found (was likely deleted by user). |
| reminder_opt_out | A customer has opted out to reminder via clicking the unsubscribe link in an email or the settings menu in chat. |
| reminder_single_opt_in | A customer has given the reminder single opt-in by agreeing in the chat. |
| reminder_single_opt_in_asked | A customer was asked in chat whether they agree to receive a reminder. |
| reminder_single_opt_in_rejected | A customer did not agree to receive a reminder in chat. |
| welcome_sent | A welcome message was sent in a welcome process brick. |
| win_lost | A customer has not won in a win process brick. |
| win_participant_bpmn_process | A customer has participated for the first time in a process in a win process brick. |
| win_participant_bpmn_sub_process | A customer has participated for the first time in a win process brick. |
| win_participation | A customer has participated in a win process brick. |
| win_won | A customer has won in a win process brick. |


Using the following code to integrate a LoyJoy chat in your site, LoyJoy events can be pushed to an existing Google Tag Manager data layer:

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  eventListeners: [function (evt, obj) {
    dataLayer && dataLayer.push({ 'evt': evt, 'bot_id': obj && obj.bot_id, 'process_id': obj && obj.process_id, 'process_name': obj && obj.process_name })  
  }],
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```

