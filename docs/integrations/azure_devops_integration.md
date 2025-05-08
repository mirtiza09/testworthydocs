---
sidebar_position: 2
---

# Azure DevOps Integration

This section guides developers through setting up and utilizing the Azure DevOps integration within the TestWorthy platform. It covers connecting the platform to Azure DevOps, synchronizing work items, and mapping fields between TestWorthy and Azure DevOps.

## Setup and Configuration: Connecting TestWorthy to Azure DevOps

To establish a connection between TestWorthy and your Azure DevOps account, follow these steps:

1. **Obtain Azure DevOps Personal Access Token (PAT):**
   - Log into your Azure DevOps portal.
   - Navigate to your user profile > Personal Access Tokens.
   - Create a new token with appropriate scopes (e.g., Work Items Read/Write).
   - Copy the generated token; you'll need it for configuration.

2. **Configure Azure DevOps Settings in TestWorthy:**
   - Log into TestWorthy as an administrator.
   - Navigate to **Settings** > **Integrations** > **Azure DevOps**.
   - Click on **Add New Configuration**.
   - Enter the following details:
     - **Organization URL:** Your Azure DevOps organization URL (e.g., `https://dev.azure.com/yourorganization`)
     - **Personal Access Token:** Paste the PAT obtained earlier.
     - **Project Name:** Select or enter the Azure DevOps project to link.
   - Save the configuration.

3. **Test the Connection:**
   - Use the **Test Connection** button to verify connectivity.
   - If successful, the platform will authenticate and store the connection details.

*Tip:* Ensure your PAT has sufficient permissions and that network firewalls allow outbound connections to Azure DevOps.

## Work Item Synchronization: Syncing with Azure DevOps Work Items

Once connected, you can synchronize work items between TestWorthy and Azure DevOps:

1. **Initiate Sync:**
   - Go to **Test Cases** or **Test Runs**.
   - Select the option **Sync with Azure DevOps**.
   - Choose the scope:
     - **Single Work Item:** Sync a specific test case or defect.
     - **Batch Sync:** Sync multiple items or entire test suites.

2. **Configure Sync Settings:**
   - Map TestWorthy test cases to Azure DevOps work items.
   - Decide on sync direction:
     - **One-way:** From TestWorthy to Azure DevOps or vice versa.
     - **Two-way:** Keep both in sync with conflict resolution rules.

3. **Execute Sync:**
   - Click **Start Sync**.
   - Monitor progress in the sync status window.
   - Upon completion, the linked work items will reflect the latest data.

4. **Automate Sync (Optional):**
   - Set up scheduled sync jobs for ongoing synchronization.
   - Configure webhook triggers for real-time updates.

*Note:* Be cautious with conflicts; define rules for overwriting or merging data.

## Field Mapping: Mapping TestWorthy Fields to Azure DevOps Fields

To ensure data consistency, map custom fields between TestWorthy and Azure DevOps:

1. **Access Field Mapping Settings:**
   - Navigate to **Settings** > **Integrations** > **Azure DevOps**.
   - Select your existing configuration.
   - Click **Edit Field Mappings**.

2. **Define Mappings:**
   - For each TestWorthy field (e.g., Test Case Title, Description, Status, Priority):
     - Select the corresponding Azure DevOps field.
     - Use dropdowns to pick from available fields.
   - Map custom fields if needed:
     - For example, map TestWorthy's "Test Data" to Azure DevOps custom fields.

3. **Save and Validate:**
   - Save the mappings.
   - Run a test sync to verify correct data transfer.
   - Adjust mappings as necessary based on test results.

4. **Maintain Mappings:**
   - Update mappings when new fields are added.
   - Document custom field mappings for team reference.

*Tip:* Use consistent naming conventions and ensure custom fields exist in Azure DevOps before mapping.

---

By following these steps, you can seamlessly connect TestWorthy to Azure DevOps, synchronize work items, and customize field mappings to streamline your testing and development workflows.