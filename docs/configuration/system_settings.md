---
sidebar_position: 1
---

# System Settings

This section explains how to access and modify the global system configuration options within TestWorthy, a test management platform. These settings control core behaviors, integrations, and environment-specific parameters that affect the entire application.

## Accessing System Settings

1. Log in to the TestWorthy admin dashboard with appropriate permissions.
2. Navigate to the **Settings** menu from the main sidebar.
3. Click on **System Settings** to open the configuration page.

## Modifying Global Configuration Options

The system settings page provides various configurable options grouped into categories such as environment parameters, integrations, notifications, and feature toggles.

### Step-by-step configuration process:

### 1. Environment Parameters

- **Tenant ID**: Set the identifier for multi-tenant support.
- **Default Language**: Choose the default language for the platform.
- **Timezone**: Select the timezone for timestamp consistency.
- **Date Format**: Define the date display format (e.g., MM/DD/YYYY).

*To modify:*
- Locate the environment section.
- Select or input the desired values.
- Click **Save** to apply.

### 2. External Integrations

- **Jira Settings**:
  - API URL: Enter your Jira server URL.
  - Username & API Token: Provide credentials for API access.
  - Enable Jira Integration: Toggle to activate.

- **TestRail Settings**:
  - API URL and credentials.
  - Enable TestRail sync.

- **Stripe Payment Gateway**:
  - API keys for live or test mode.
  - Enable/Disable payment processing.

*To modify:*
- Fill in the required fields.
- Toggle the respective switches.
- Save changes.

### 3. Notification Settings

- **Email Server Configuration**:
  - SMTP Host, Port, Username, Password.
  - Enable email notifications.

- **Notification Triggers**:
  - On test case creation, update, or failure.
  - On milestone completion.
  - On system errors.

*To modify:*
- Enter SMTP details.
- Select notification triggers.
- Save.

### 4. Feature Toggles

- Enable or disable features such as:
  - Test case automation.
  - External integrations.
  - User activity logging.
  - Multi-language support.

*To modify:*
- Use toggle switches.
- Confirm by clicking **Save**.

## Important Considerations

- **Permissions**: Only users with admin privileges can modify system settings.
- **Validation**: Fields like API URLs and credentials are validated upon saving.
- **Impact**: Changes may affect system behavior immediately or after a restart, depending on the setting.
- **Backup**: Always back up current configurations before making significant changes.

## Example: Configuring Jira Integration

1. Enter your Jira instance URL, e.g., `https://yourcompany.atlassian.net`.
2. Provide your Jira username and API token.
3. Toggle **Enable Jira Integration** to **On**.
4. Click **Save**.
5. Test the connection by clicking **Test Connection** (if available).

## Summary

Configuring system settings involves navigating to the **System Settings** page, selecting the desired options across environment, integrations, notifications, and features, and saving your changes. Proper configuration ensures seamless operation, external integrations, and tailored user experience across your test management environment.