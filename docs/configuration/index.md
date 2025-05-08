---
sidebar_position: 12
---

# Configuration

This section provides guidance on managing the system settings within the application, including global configurations, email setup, custom fields, test statuses, priorities, automation types, and UI customization. It details how to access, modify, and implement these configurations to tailor the system behavior and appearance.

## Accessing System Settings

1. Log into the application with administrator privileges.
2. Navigate to the main menu and select **Settings**.
3. Choose **System Settings** from the submenu.

## Configuring Global System Options

- **Purpose**: Set overarching parameters affecting the entire system.
- **Steps**:
  - Within **System Settings**, locate the **General** tab.
  - Adjust options such as default language, date/time formats, and system-wide features.
  - Save changes to apply globally.

## Setting Up Email Notifications

- **Purpose**: Enable email alerts and templates for system events.
- **Steps**:
  - Navigate to **Email Configuration** under **Settings**.
  - Input SMTP server details: host, port, username, password.
  - Configure email templates for notifications like test assignments, status updates, or alerts.
  - Test email delivery to ensure correctness.
  - Save configuration.

## Managing Custom Fields

- **Purpose**: Extend entities with additional data points.
- **Steps**:
  - Go to **Custom Fields** in **Settings**.
  - Select the entity to customize (e.g., Test Cases, Users).
  - Create new fields, specifying type (text, dropdown, date), label, and options.
  - Assign visibility and mandatory status.
  - Save and refresh entities to include new custom fields.

## Customizing Test Statuses

- **Purpose**: Define and modify statuses for test cases and runs.
- **Steps**:
  - Access **Test Statuses** in **Settings**.
  - Add new statuses or edit existing ones.
  - Set behaviors such as default status, color coding, and transition rules.
  - Save to update workflow.

## Setting Up Priorities

- **Purpose**: Manage priority levels for test cases.
- **Steps**:
  - Navigate to **Priorities** under **Settings**.
  - Add, edit, or delete priority levels (e.g., Low, Medium, High).
  - Assign color codes for visual identification.
  - Save changes.

## Configuring Automation Types

- **Purpose**: Define automation frameworks and types for test cases.
- **Steps**:
  - Go to **Automation Types** in **Settings**.
  - Create new types (e.g., Selenium, Appium).
  - Assign relevant parameters or scripts.
  - Save and associate with test cases as needed.

## UI Customization

- **Purpose**: Alter the appearance of the system.
- **Steps**:
  - Select **UI Customization** in **Settings**.
  - Choose themes, color schemes, or upload custom CSS.
  - Adjust layout options if available.
  - Preview changes and save.

## Tips

- Always back up configurations before making bulk changes.
- Use test environments to validate UI customizations.
- Leverage templates for email notifications to maintain consistency.
- Regularly review statuses and priorities to align with project workflows.

This guide enables systematic setup and modification of core system configurations to optimize the application's performance and user experience.