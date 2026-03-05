## ADDED Requirements

### Requirement: Download entry is visible and actionable

The site SHALL provide a clear, clickable download entry (e.g., button or link) that allows users to obtain the Mac version of OpenSpecGUI.

#### Scenario: Visitor wants to download

- **WHEN** a user wants to install the app
- **THEN** the page SHALL show at least one prominent download control (button or link) that initiates or points to the Mac app download

#### Scenario: Download control is accessible

- **WHEN** a user loads the page
- **THEN** the download entry SHALL be visible without requiring horizontal scroll on a typical desktop viewport

### Requirement: Download target is the Mac app package

The download entry SHALL point to a valid Mac app artifact (e.g., .app in a zip, .dmg, or direct .app) so that users can install OpenSpecGUI on macOS.

#### Scenario: User completes download

- **WHEN** a user activates the download entry and the transfer completes
- **THEN** the obtained file(s) SHALL allow installation of OpenSpecGUI on a compatible Mac (e.g., opening a .dmg or unzipping and moving .app to Applications)

### Requirement: Version and system requirements may be displayed

The page MAY display the current app version and minimum system requirements (e.g., macOS version) so that users can confirm compatibility before downloading.

#### Scenario: Version info is shown

- **WHEN** the site chooses to show version or requirements
- **THEN** the page SHALL display the version and/or requirements in human-readable text (e.g., "macOS 12+" or "Version 1.0.0")
