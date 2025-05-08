---
sidebar_position: 1
---

# Jira Integration

This section guides developers through setting up and managing Jira integration within the application. It covers connecting TestWorthy to Jira, synchronizing test cases and defects, and mapping fields between TestWorthy and Jira.

## Setup and Configuration

To connect TestWorthy to Jira:

1. **Create a Jira Application Link (OAuth or Basic Auth):**
   - Log into your Jira instance.
   - Navigate to **Administration > Applications > Application Links**.
   - Enter the URL of your Jira instance and create a new link.
   - Configure the link with appropriate authentication (OAuth or Basic Auth).
   
2. **Configure Jira Integration in TestWorthy:**
   - Access the **Integration Settings** in TestWorthy.
   - Locate the **Jira Configuration** section.
   - Enter your Jira API URL, username, and API token or password.
   - Save the configuration.
   
3. **Activate Jira Integration:**
   - Ensure the **IsJiraConfigurationActive** flag is set to true.
   - Test the connection to verify proper setup.

*Tip:* Use the `JiraConfiguration` entity to store API credentials and URLs. This entity is linked to your project and can be managed via the admin panel.

## Issue Synchronization

TestWorthy supports syncing test cases and defects with Jira issues:

1. **Sync Test Cases:**
   - When creating or updating test cases in TestWorthy:
     - Use the **Sync with Jira** option.
     - The system will create or update corresponding Jira issues.
   
2. **Sync Defects:**
   - When a defect is logged in TestWorthy:
     - Use the **Create Jira Issue** button.
     - The defect details are pushed to Jira as an issue.
   
3. **Automated Sync:**
   - Enable scheduled synchronization:
     - Configure sync intervals in the integration settings.
     - The system will periodically sync test cases and defects with Jira.

*Important:* The synchronization relies on the `JiraConfiguration` entity and the API credentials stored therein.

## Field Mapping

Mapping TestWorthy fields to Jira fields ensures data consistency:

1. **Open Field Mapping Settings:**
   - Navigate to **Integration > Jira Field Mapping**.
   
2. **Configure Mappings:**
   - Map TestWorthy test case fields to Jira issue fields:
     - Example:
       - TestWorthy 'Test Case Title' → Jira 'Summary'
       - TestWorthy 'Test Steps' → Jira 'Description'
       - TestWorthy 'Priority' → Jira 'Priority'
   - Map defect fields similarly.
   
3. **Save Mappings:**
   - Confirm and save the field mappings.
   - These mappings are stored in the `FieldMapping` entity.
   
4. **Test Mappings:**
   - Use the **Test Mapping** button to verify correct data transfer.
   - Adjust mappings as needed for accuracy.

*Tip:* Use the **Field Mapping** interface to customize field correspondence, ensuring that critical data flows correctly between systems.

---

This guide provides the essential steps to establish, synchronize, and map fields between TestWorthy and Jira, enabling seamless issue tracking and test management integration.