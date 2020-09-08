
# Change Log

All notable changes to LoyJoy will be documented in this file.

## Unreleased

### Added


## release-2020-09-07

### Added

- Complete switch to NoSQL database repositories for scalability.
- Timers are evaluated on all experiences, not only on default experiences.
- Support for Google Data Studio.
- Extended customer cleansing logic.
- 🎞️ Image sharing via new Image Sharing process block:
  - Images sent via Snapshot are pre-selected for sharing


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
