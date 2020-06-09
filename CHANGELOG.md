
# Change Log

All notable changes to LoyJoy will be documented in this file.


## Unreleased

### Added

### Changed

### Fixed


## release-2020-06-09

### Added

- Integration mappings can read process variables.
  - allows sending e.g. customer variables to ProCampaign, Salesforce, Cleverreach etc.
- Historization of customer variables and process variables.
  - when adding a new variable, an existing variable of the same name will be archived
- ⏲️ Timer date change:
  - previously the timer was listening to a fixed minute interval
  - now it can be set to be active after a date change (on the next calendar day)
  - customers can chat at 23:50 and on 00:00 the timer will be active
  - allows synchronizing daily giveaways & timers
  - can be used in combination with minute threshold (timer should be active after at least 6 hours & a date change)
- 📅 Date picker for manager preview
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
