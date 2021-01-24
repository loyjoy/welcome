
# Change Log

All notable changes to LoyJoy will be documented in this file.


## Unreleased

### Added

- Chat UI
  - The chat can now have an avatar image, representing the bot/live agent.
  - Added option to disable user input field
  - Added option to lock process from modifications 🔒
- Extended Live chat capabilities
  - Animation payload indicator in live view
  - Live view redesign
  - Splitted live and bot message sessions with tabs
  - Notifications with mute button
  - Added Emoji picker 
  - Switch for agents being online/offline
  - Option for fallback stratgy if agent does not reply


## release-2021-01-15

### Added

- Process module `Sign In` now triggers the sign in chat flow.
- Variables now have a store (Browser, Server) and scope (process-specific, process-independent).
- Live Process Brick: Agents configuration
  - Agents can now be defined on a Live Process Brick.
  - Agents can declare themselves as online/offline in live view.
  - If there are no agents online when a user enters the Live Process the building block is skipped.


## release-2021-01-11

### Added

- Upload option for BPMN XML files of bots and processes
- Intents additionally are matched rule-based against intent training data
- Added REST endpoints for programmatically downloading XML process definitions
- Added debug mode in manager that makes internal chat mechanics transparent


## release-2021-01-07

### Added

- New Process block: Appointment 📅
  - You can use this block to let your customers schedule invididual appointments.
  - Appointments are stored as iCalendar events, which are sent by email and can be integrated as WebCal into calendar tools such as Google Calendar.
- New Process block: Live chat 💬
  - This allows you to directly reply to customer requests
- New home screen widget: Icon widget
  - Add up to 5 icons linking to experiences.
- Migrated bots and experiences to BPMN XML files
  - Bots and experiences can be exported as XML files, providing overview over the complete configuration of bots and experiences including texts, variables collected etc.
  - All XML files are versioned and backed up internally, giving you the chance for rollbacks if needed. If you need a rollback, please contact our support and we can help you.


### Fixed

- Viber fixes

## release-2020-11-16

### Added

- Add option to request attributes from ProCampaign
- Add restart parameter for widget
- Add option to ask for Opt-Ins again in chat
- Add API servlet to start process flow
- Extended Salesforce integration
  - Allow upserting objects according to fields

## release-2020-11-09

### Added

- New Process block: Language selection
  - This enables you to ask your customer for her/his language. 
  - Possible choices are derived from the languages of the BPMN process.
- Locales `de` and `de__formal` can now be active at the same time on the same process, enabling customers to choose between `Duzen` and `Siezen`.


## release-2020-11-02

### Added

- 📧 Process module `mail`:
  - Sends email in the process flow to the current customer.
- Process module `signal`.
  - Most process modules emit events. Now you can place a `signal` process module in any process of the bot, which listens for such events in the bot. When an events occurs, the `signal` process module is triggered in a background process execution. E.g. a use case is to listen for newsletter opt-in events in any process of the bot and trigger a background process, which writes the newsletter opt-in to Salesforce.
- Added the functions [`string_replace`](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html#replace(java.lang.CharSequence,%20java.lang.CharSequence)) and [`string_replace_all`](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html#replaceAll(java.lang.String,%20java.lang.String)), which can be used in expressions.


## release-2020-10-26

### Added

- Reminder process module
  - Schedule reminder notifications for Web push, email etc. individually for your customers, which have given a reminder opt-in.
  - Reminder schedules from menu item "Push" can now be found in the reminder process module, which you can add to any process.
- Refactured campaigns
  - Campaigns now are more lightweight, focussing on Web push: Simply (1) enter a title, body and URL, (2) optionally select you target customer segment, (3) optionally precalculate the segment size and (4) finally trigger sending of Web push notifications to the selected customer segment. Web push notifications will be sent instantly, without planning overhead.
- Salesforce process module
  - Integrate Salesforce into experiences in form of a process module with the new Salesforce process module. You can map arbitrary customer variables to Salesforce data objects and attributes.
- Background BPMN processes
  - Some integrations can now trigger background BPMN processes. E.g. the Salesforce integration now can be configured with a specific BPMN process, which then can contain the new Salesforce process module.


## release-2020-10-14

### Added

- 🖼️ The carousel component got a rework
  - Video galleries, image galleries, product galleries, prizes, rewards etc. now are presented with a smooth slider
  - The slider teases successive elements of the gallery, giving the chat a horizontal dimension
- 📤 Add a catch-all subscription with whitelist for Pub/Sub
  - Allows all types of events to be sent to a Pub/Sub topic.
  - Event types to pusblish by Pub/Sub can be configured in integration settings.


## release-2020-10-06

### Added

- 💬 Refined Natural Language Processing (NLP) pipeline:
  - NLP models can now be trained by bot (before by tenant).
  - NLP models are stored in a storage after training.
  - NLP training can be canceled.


## release-2020-09-29

### Added

- 📋📋📋 New process block: 'Decision table' for central evaluation and exection of bpmn process variables and other conditions.
  - If your process tends to be too complicated with many branches this process block might help you in simplifying your process
  - It is an implementation of the open DMN standard by the [OMG group](https://www.omg.org/)
- When a new user message arrives, process information such as bot, experience and process module are now stored additionally.
  - This provides you with information about what a user has entered in which context and can be explored in the live menu.
- 🎞️ Image sharing via new Image Sharing process block:
  - Images sent via Snapshot are pre-selected for sharing
- 👶🧒👵 A minimum age can be set for the birthdate
  - In the LoyJoy chat UI only years in accordance with this minimum age can be selected

### Fixed

- 🔗 Links are parsed correctly in questionnaire answers


## release-2020-09-25

### Added

- Intent groups can now be scoped to a bot
  - This enables you to activate specific Intent groups for specific bots.
- ⭐⭐⭐⭐⭐ New process block for creating reviews in Yotpo
  - Including the ability to use the trusted vendors feature
- The coin image is now editable for Loyalty programs
- An image can now be used as a chat background 

## release-2020-09-14

### Added

- Mini program:
  - Allow for multiple variables to be set at the same time
  - Allow blocking process flow until variables are set from within the mini program

## release-2020-09-07

### Added

- Complete switch to NoSQL database repositories for scalability.
- Timers are evaluated on all experiences, not only on default experiences.
- Support for Google Data Studio.
- Extended customer cleansing logic.

## release-2020-08-26

### Added

- The home view is now based on widgets, which can be added flexibly:
  - Widget types to choose from are `hero`, `stories`, `groups`, `notifications`, `roster`. This list will grow in the future.
  - The widget type `stories` enables you to build AMP stories e.g. with https://makestories.io/ and publish them in the home view.
  - As customers can jump from stories into experiences, stories are an exciting way to engage your customers to start chats.
- ✨ Sparkle animation for quiz answer options.
- Mini-program
  - Added action to close Mini-Program via API.
- 🎟️ Coupon Codes
  - Message, if no coupon codes left.
  - Number of uploaded / redeemed coupon codes in analytics.
  - Allow GS-1 Databar Expanded coupon codes.
- Updated names for sub-processes
  - Show both type and name of a process building block together.
- Added copy option for i18n texts to copy texts of an BPMN process from one locale to another.
- Beta REST API for reading and writing customer variables and process variables programmatically.


## release-2020-08-10

### Added

- Extended process variable picker, providing process selection and information about variable declarations.
- Added support for SMS and WhatsApp via Twilio.
- Extended Web service integrations with URLs for process variables, customer variables and session variables. This enables you to listen for any changes to such variables via HTTP POST requests to an API provided by you.

### Changed

- Texts tab revised
  - Search updates only when search text changes.
  - Search also works on placeholder texts.
  - Adjusted layout.
- Sign in process building block reworked
  - Text before login can now be changed at sign in process building block.
  - PIN-E-Mail reworked.
- Rewards process building block
  - Message if reward is not available
  - Reward redemption counts in analytics
- Web service process building block
  - Moved HTTP header authorization details to separate field, which can be configured in the Web service process building block


## release-2020-07-28

### Added

- Replaced roster view of Web chat with new home view.
  - Content of home view is based on process groups
  - Home view can be themed according to multi-brand / multi-bot Web chat app.
  - Roster is now component in home view.
- 🔔 Push conditions.
  - Push can be made dependent on process & customer variables.
  - Customers can be targeted e.g. by entered data or giveaway participations.
  - Shows number of messages to be sent.
- ↩️ Restart button added to chat menu.

### Changed

- Unified database backend for campaign notifications and reminder notifications, preparing push capabilities for Web chat.

### Fixed

- Customer variables are updated before integration listeners are triggered


## release-2020-07-06

### Added

- Logging is accessible unter settings > log. Unsuccessful integration HTTP calls are logged and can be analyzed there.
- Enhanced Viber integration.
- ProCampaign consumer account assurance.
- New animations.

### Changed

- Switched from birthday to birthdate.

### Fixed

- Fixed CSV export encoding.


## release-2020-06-24

### Added

- Customer referrals.
  - Sharing with customer tokens.
  - Referring customers get loyalty points for new signups. 
- Added process groups for structuring processes into roster entries. Refactored the bots management UI around those process groups.
- Added intent groups for structuring intents. Intent groups can be copied between tenants.
- Integration of Viber REST API for Russian market.
- Integration of SMS.
- Barcode scanning for third-party messengers.
- Activated NoSQL database repositories.
- Version indicator in footer of management backend.

### Changed

- Moved coupon codes from experience to process building block.

### Fixed

- Multiple choice questions now work on third-party messengers.
- Fix for using LoyJoy inside cross-origin iframes.


## release-2020-06-09

### Added

- Integration mappings can read process variables.
  - Allows sending e.g. customer variables to ProCampaign, Salesforce, Cleverreach etc.
- Historization of customer variables and process variables.
  - When adding a new variable, an existing variable of the same name will be archived
- ⏲️ Timer date change.
  - Previously the timer was listening to a fixed minute interval
  - Now it can be set to be active after a date change (on the next calendar day)
  - Customers can chat at 23:50 and on 00:00 the timer will be active
  - Allows synchronizing daily giveaways & timers
  - Can be used in combination with minute threshold (timer should be active after at least 6 hours & a date change)
- 📅 Date picker for manager preview.
  - Now arbitrary dates can be selected in the manager when working on chat flow.
  - Useful for designing chat flows of time-dependent chat flows such as advent calendars and date-specific giveaways.
- Support for both SQL and NoSQL database repositories.
- Sub processes can be named in a model for better overview.
- CSV export for free-text messages.

### Changed

- Streamlined Web push subscription data model.


## release-2020-05-30

### Added

- 🏆 New loyalty process building block enabling loyalty programs.
- Chat can have width in interval XS, SM, MD, LG, XL.
- External links based on i18n entries, enabling language-specific and date-specific links.
- Variable picker and link picker in i18n text entry component.
- Loading indicator and animation for mini programs.
- Mini programs can set process variables via `parent.postMessage({ action: 'setVariable', key: 'somekey', value: 'somevalue' }, '*')`.
- Copy option for questionnaire questions and answer options.
- 🌤️ Integration for weather API.
- New animations.

### Changed

- Palette open by default.
- Bumped dependency versions.

### Fixed

- Fixes on questionnaire chat UI components.
- Fixes for WhatsApp integration.


## release-2020-05-03

### Added

- Persistent chat messages and roster view.
- Unified jump process building block.
- Variables in I18n messages and emails.
- Timer process building block for timed push messages.
- Intro message in proceed process building block.
