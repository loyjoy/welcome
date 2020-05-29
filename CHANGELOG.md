
# Change Log

All notable changes to LoyJoy will be documented in this file.


## Unreleased

### Added

- Integration mappings can use process variables
- Historization of customer variables and process variables

### Changed

### Fixed


## release-2020-05-17

### Added

- New loyalty process building block enabling loyalty programs
- Chat can have width in interval XS, SM, MD, LG, XL
- External links based on I18n entries, enabling language-specific and date-specific links
- Variable picker and link picker in I18n text entry component
- Loading indicator and animation for mini programs
- Mini programs can set process variables via `parent.postMessage({ action: 'setVariable', key: 'somekey', value: 'somevalue' }, '*')`
- Copy option for questionnaire questions and answer options

### Changed

- Palette open by default
- Bumped dependency versions

### Fixed

- Fixes on questionnaire chat UI components
