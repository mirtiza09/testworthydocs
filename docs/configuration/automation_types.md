---
sidebar_position: 6
---

# Automation Types

This section explains how to set up and manage automation types within your test management system. Automation types categorize your test cases based on the automation framework or method used, enabling better organization, filtering, and reporting.

## Step-by-step instructions

### 1. Access the Automation Types Configuration

- Log in to your test management platform with appropriate permissions.
- Navigate to the **Configuration** section from the main menu.
- Select **Automation Types** from the submenu.

### 2. View Existing Automation Types

- The page displays a list of predefined automation types such as "Manual," "Selenium," "Appium," etc.
- Review the existing entries to understand current classifications.

### 3. Add a New Automation Type

- Click the **Add New** button (usually located at the top or bottom of the list).
- Fill in the required fields:
  - **Name**: Enter a descriptive name for the automation type (e.g., "Robot Framework").
  - **Description**: Optionally, provide details about this automation type.
- Save the new entry by clicking **Save** or **Add**.

### 4. Edit an Existing Automation Type

- Locate the automation type you wish to modify.
- Click the **Edit** icon (pencil) next to it.
- Update the **Name** or **Description** as needed.
- Confirm changes by clicking **Save**.

### 5. Delete or Disable an Automation Type

- To remove an automation type, click the **Delete** icon (trash bin).
- Confirm the deletion if prompted.
- Alternatively, disable it (if the system supports soft deletion or deactivation) by toggling an **Active/Inactive** switch.

### 6. Assign Automation Types to Test Cases

- When creating or editing a test case:
  - Locate the **Automation Type** dropdown or selector.
  - Choose the appropriate automation type from the list.
  - Save the test case to associate it with the selected automation framework.

### 7. Use Automation Types for Filtering and Reporting

- Use the **Filter** options in test case lists or reports:
  - Select specific automation types to narrow down your view.
- Generate reports based on automation types to analyze automation coverage or effectiveness.

## Implementation details

- The configuration interface is typically built with a form-based UI, backed by a database table (e.g., `AutomationTypes`).
- CRUD operations are performed via API calls or direct database access, depending on your system architecture.
- Validation ensures that names are unique and non-empty.
- Changes are reflected immediately in dropdowns and filters across the platform.

## Important considerations

- Maintain consistent naming conventions for clarity.
- Use descriptive names to facilitate filtering and reporting.
- Regularly review and update automation types as your testing frameworks evolve.
- Ensure proper permissions are set to prevent unauthorized modifications.

## Example

Suppose you want to add a new automation type called "Cypress":

- Click **Add New**.
- Enter **Name**: "Cypress".
- Enter **Description**: "End-to-end testing with Cypress framework".
- Save the entry.
- When creating a new test case, select "Cypress" from the **Automation Type** dropdown.
- Filter test cases by "Cypress" to analyze all tests using this framework.

By following these steps, you can effectively categorize and manage your automation types, streamlining your testing workflows and reporting.