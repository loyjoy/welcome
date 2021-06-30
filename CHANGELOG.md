
# Change Log

All notable changes to LoyJoy will be documented in this file.

## Unreleased

### Added

- Palette
  - Grouping of subprocesses, groups are ordered by priority
  - Filtering subprocesses by name, group, tags
  - Fullscreen palette shows subprocess messages


### release-2021-06-30

### Added

- Widgets in Home are now hidden if they do not contain content
- New process module: Salesforce Interaction Studio
- Web components are now available inside the chatflow
- Web components can now be used in footer
- Web components can now be parameterized
- Notifications in the home view notifications widget are now stacked if more than one
- Live chat messages are now stored either in database or in-memory. In-memory is for financial institution tenants such as banks, database for other tenants.

### Fixes
- Fixed a bug that caused web components to be included only once


### release-2021-06-16

### Added

- 📈 Analytics
  - New events are counted
    - Customer data entered (birthdate, name, ...; cf. [screenshot](changelog/2021-06-07-customer_data.png))
    - Opt-in rejected (cf. [screenshot](changelog/2021-06-07-opt_in_rejected.png))
    - Auto-jump (cf. [screenshot](changelog/2021-06-07-automatic_jump.png))
    - Questionnaire question answered (cf. [screenshot](changelog/2021-06-07-questionnaire.png))
    - Mail sent (cf. [screenshot](changelog/2021-06-07-email.png))
    - Proceed confirmed (cf. [screenshot](changelog/2021-06-07-proceed.png))
    - Intent matching (cf. [screenshot](changelog/2021-06-07-intents.png))
  - Heatmap showing how many of certain process blocks are reached (cf. [screenshot](changelog/2021-06-07-heatmap.png))
  - Optimizations
- List process brick
  - Added jump functionality to elements
- ChatUI
  - Inverted colors of header: The header of new processes has now a white background and the font color is the primary color
  - However, this can be inverted back to the traditional design under the `branding`-tab
  - Increased size of the header-title
- Audio recording
  - Customers can record and send an Audio in the Chat. (Not supported in `ie11`)
  - If the customer is logged in, the Audio will be saved in the history.
- Audio player: depending on the browser the following functionality is available
  - display of audio duration and progressbar (not supoprted in `safari`)
  - jump forwards and backwards in current playtime (`firefox`(all files), `chrome, edge-chromium, ie11`(for files approx. smaller than 3 MB), not supported in `safari`
  

### Fixes
- Questionnaire:
  - Placeholder for numerical inputs is now editable
- Image Gallery:
  - Indicator of the active item has color
- Added auto translation on bot level


## release-2021-05-25

### Added

- `External link` process module
  - Titles, descriptions and images are now loaded automatically based on og-tags of respective website
  - Link clicks are measured and displayed in analytics.
- `List process` module
  - List elements can now be conditioned
- `Mini program` process module
  - Can now be opened automatically
  - Footer for closing the mini program can now be hidden
  - An optional clickable teaser image can now be added
- `Notification` module
  - Notifications can now be sent via SMS with help of Twilio.
  - For this to work, customer must have given an SMS opt-in with `SMS opt-in` module and entered their phone number with `Phone number` module.
- `Product` module
  - Link clicks are measured and displayed in analytics.
- `Timer` process module
  - It is now possible to add absolute start and end dates
- 📈 Analytics
  - Process starts are measured and shown in analytics.
  - Link clicks are measured in the `External link` and `Product` modules.
- Callbacks added to JavaScript API
- Text inside draggable components is now selectable
- All CSV exports are provided as encrypted ZIP files


### Fixed

- `List` process module
  - Margin of elements while solely using titles


## release-2021-05-10

### Added

- `SMS opt-in` process module now supports Twilio
- Chat "send message" button icon can now be adjusted via image upload in branding.
- 📅 `Appointment` process module: Option to add a lead time
- 📈 Analytics
  - Analytics for decision jump process module
  - Analytics for live chats
  - Analytics for home view
- Policy user add
  - suitable greeting, if no first name known
  - new welcome email to the added user
- Animations
  - New animations: Autumn Leaves, Santa, Cheese, Christmas balls, Easter eggs, Gift boxes, Pine cones, Pumpkins, Raining stars
  - Animation subprocess
- `Questionnaire` process module
  - new question type: email

### Fixed

- Stochastic timeout on image upload in Firefox Android
- BPMN variable select popover
  - Underlying dialog no longer closes on any click
  - Resize to fit to screen

## release-2021-04-13

### Added
- `Mail` process module can now send attachments
- Added `Clipboard` process module
  - Show a text that your customers can copy


## release-2021-03-29

### Added

- New help bar on the right of LoyJoy manager with context information for all functionalities of LoyJoy.
- New Process module `List`
  - Show a list of generic elements to your customers and let them optionally react on it
- New process module `Salesforce Service Cloud`
- New process module `Clever Reach`
- In branding added option to disable `Restart chat`
- In branding added option to enable `Reset chat`
- In branding added option for fullscreen mode.
- Added event bus for ChatUI. When emitting event `route_home` with event process module, the ChatUI changes to home view.
- In process module `Appointment` added option to send event description via email as password encrypted PDF attachment.
- All surrounding micro-services for data storage etc. now can be disabled by super admins, allowing the LoyJoy runtime to be executed in-memory only, thus enabling the deployment of the LoyJoy runtime as an appliance in environments without any storage capabilities (e.g. embedded devices).


## release-2021-03-23

### Added

- New process module `Campaign Monitor`
- New process module `Scondoo`
- New process module `Google Pub/Sub`


## release-2021-03-22

### Added

- New process module `Password`
  - Ask your customers for a password which is stored encrypted in the session


## release-2021-03-19

### Added

- Radically simplified `ProCampaign` process module. Everything now is managed in the process module, not in the integration.


## release-2021-03-18

### Added

- User accounts can now be added to multiple tenants.
  - Simply add the user email address to multiple tenants in the tenant settings.
  - After sign in, the user can select a tenant with the tenant select control on top right beside the LoyJoy logo.


## release-2021-03-12

### Added

- Extended capability for locale `ar`. Also markdown can now be used everywhere in the chat UI.
- New analytics connector for pushing analytics fact and dimension table to BigQuery.
- Introduced Web components to enable 100% customization of home screen and chat bubbles, also by 3rd-party developers. With this release custom splash screen and home view widgets are possible, custom chat bubbles will follow.
- `Video` process modules now can autoplay the first video.

### Fixed

- Fixed seeding standard NLU intents, which where seeded multiple times before depending on the number of locales active on the bot.


## release-2021-03-04

### Added

- Added process module `Reset` for resetting the complete session, not only changing the process instance.


## release-2021-03-03

### Added

- Added Function `IsMobile` to check, if the customer is chatting from a mobile device.
- The imprint is only offered in the chatbot navigation bar, if it is configured.
- Chat UI
  - The chat can now have an avatar image, representing the bot/live agent.
- `Data collection` process module
  - Option to allow dynamic loading of dropdown options
- `Product` process module
  - Button to set variable
- `Phone number` process module
  - Similar to first name and last name now the phone number of the customer can be collected in the chat.
- `SMS opt-in` process module
  - Added process module to collect SMS opt-ins for phone numbers
- Birth date, first name, last name, phone number, gender, postal address can now be reasked, e.g. for building a customer settings chat process. These values before were only asked once.


## release-2021-02-17

### Added

- The local storage is now used tenant-wide, not bot-wide. Thus, the authentication context of a bot is shared with the other bots of that tenant, inducing less sign-ins for the customers.
- Added variable `loyalty_balance`, containing the loyalty point balance for a customer
- Added a new function `customer_age`.
- Separated storage for customer variables and process variables into a long-term storage and a transient store for more fine-granular control over variable life cycles.
- In the chat UI texts are now interpolated in the client, not on the server, enabling a more responsive reaction on variable changes in the UI.
- In case of a LoyJoy update the manager and chat now asks for a browser reload.


## release-2021-01-28

### Added

- `ProCampaign` process module: replaced hardcoded configuration properties for consent text and list
  - consent text is modeled in a mapping as `<consent text key> := Function I18nTranslate(<i18n_key as copied from texts table>)`
  - list is modeled in a mapping as `<list key> := 1`
- Sub processes can now be copied in the process editor


## release-2021-01-26

### Added

- Chat UI
  - Added option to disable user input field
  - Added option to lock process from modifications 🔒
- Redesigned the branding tab in manager
  - Branding now only contains options for styling the chat UI (i.e. no texts/content elements)
  - The branding can be inherited from the bot. This is practical for bots with many processes, which should have the same styling.
  - Some former branding settings such as SMTP settings, persistence quick replies and timezone now are configured below the list of process modules or in the respective process module
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
- `Live` process module: Agents configuration
  - Agents can now be defined on a `Live` process module.
  - Agents can declare themselves as online/offline in live view.
  - If there are no agents online when a user enters the `Live` process module, the process module is skipped.


## release-2021-01-11

### Added

- Upload option for BPMN XML files of bots and processes
- Intents additionally are matched rule-based against intent training data
- Added REST endpoints for programmatically downloading XML process definitions
- Added debug mode in manager that makes internal chat mechanics transparent


## release-2021-01-07

### Added

- New process module: `Appointment` 📅
  - You can use this module to let your customers schedule invididual appointments.
  - Appointments are stored as iCalendar events, which are sent by email and can be integrated as WebCal into calendar tools such as Google Calendar.
- New process module: `Live` 💬
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

- New Process module: Language selection
  - This enables you to ask your customer for her/his language.
  - Possible choices are derived from the languages of the BPMN process.
- Locales `de` and `de__formal` can now be active at the same time on the same process, enabling customers to choose between `Duzen` and `Siezen`.


## release-2020-11-02

### Added

- 📧 Process module `Mail`:
  - Sends email in the process flow to the current customer.
- Process module `Signal`.
  - Most process modules emit events. Now you can place a `Signal` process module in any process of the bot, which listens for such events in the bot. When an events occurs, the `Signal` process module is triggered in a background process execution. E.g. a use case is to listen for newsletter opt-in events in any process of the bot and trigger a background process, which writes the newsletter opt-in to Salesforce.
- Added the functions [`string_replace`](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html#replace(java.lang.CharSequence,%20java.lang.CharSequence)) and [`string_replace_all`](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html#replaceAll(java.lang.String,%20java.lang.String)), which can be used in expressions.


## release-2020-10-26

### Added

- `Reminder` process module
  - Schedule reminder notifications for Web push, email etc. individually for your customers, which have given a reminder opt-in.
  - Reminder schedules from menu item "Push" can now be found in the `Reminder` process module, which you can add to any process.
- Refactured campaigns
  - Campaigns now are more lightweight, focussing on Web push: Simply (1) enter a title, body and URL, (2) optionally select you target customer segment, (3) optionally precalculate the segment size and (4) finally trigger sending of Web push notifications to the selected customer segment. Web push notifications will be sent instantly, without planning overhead.
- `Salesforce` process module
  - Integrate Salesforce into experiences in form of a process module with the new `Salesforce` process module. You can map arbitrary customer variables to Salesforce data objects and attributes.
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

- 📋📋📋 New process module `Decision table` for central evaluation and exection of bpmn process variables and other conditions.
  - If your process tends to be too complicated with many branches this process module might help you in simplifying your process
  - It is an implementation of the open DMN standard by the [OMG group](https://www.omg.org/)
- When a new user message arrives, process information such as bot, experience and process module are now stored additionally.
  - This provides you with information about what a user has entered in which context and can be explored in the live menu.
- 🎞️ Image sharing via new `Image Sharing` process module:
  - Images sent via Snapshot are pre-selected for sharing
- 👶🧒👵 A minimum age can be set for the birthdate
  - In the LoyJoy chat UI only years in accordance with this minimum age can be selected

### Fixed

- 🔗 Links are parsed correctly in questionnaire answers


## release-2020-09-25

### Added

- Intent groups can now be scoped to a bot
  - This enables you to activate specific Intent groups for specific bots.
- ⭐⭐⭐⭐⭐ New process module for creating reviews in Yotpo
  - Including the ability to use the trusted vendors feature
- The coin image is now editable for Loyalty programs
- An image can now be used as a chat background

## release-2020-09-14

### Added

- `Mini program` process module:
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
- `Mini program` process module
  - Added action to close Mini-Program via API.
- 🎟️ `Coupon Codes` process module
  - Message, if no coupon codes left.
  - Number of uploaded / redeemed coupon codes in analytics.
  - Allow GS-1 Databar Expanded coupon codes.
- Updated names for sub-processes
  - Show both type and name of a process module together.
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
- `Sign in` process module reworked
  - Text before login can now be changed at sign in process module.
  - PIN-E-Mail reworked.
- `Rewards` process module
  - Message if reward is not available
  - Reward redemption counts in analytics
- `Web service` process module
  - Moved HTTP header authorization details to separate field, which can be configured in the Web service process module


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

- Moved coupon codes from experience to process module.

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

- 🏆 New `Loyalty` process module enabling loyalty programs.
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
- Unified jump process module.
- Variables in I18n messages and emails.
- `Timer` process module for timed push messages.
- Intro message in proceed process module.
