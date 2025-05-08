---
sidebar_position: 3
---

# GitHub Integration

This section guides developers through the setup, configuration, and field mapping processes necessary to integrate TestWorthy with GitHub. It covers connecting the platform to GitHub repositories, syncing issues, and aligning custom fields between TestWorthy and GitHub.

## Setup and Configuration: Connecting TestWorthy to GitHub

To establish a connection between TestWorthy and your GitHub account, follow these steps:

1. **Create a GitHub Personal Access Token:**
   - Log in to your GitHub account.
   - Navigate to **Settings > Developer Settings > Personal Access Tokens**.
   - Click **Generate new token**.
   - Select the necessary scopes, typically:
     - `repo` (full control of private repositories)
     - `admin:repo_hook` (manage hooks)
     - `workflow` (if needed)
   - Generate the token and copy it securely.

2. **Configure GitHub Integration in TestWorthy:**
   - Log in to your TestWorthy admin panel.
   - Navigate to **Integrations > GitHub Integration**.
   - Enter your GitHub **API Token** in the provided field.
   - Specify the repositories or organizations you want to connect.
   - Save the configuration.

3. **Authorize TestWorthy Access (if OAuth is used):**
   - If your setup uses OAuth, click the authorization button.
   - Log in to GitHub and authorize the application.
   - Confirm the permissions granted.

4. **Test the Connection:**
   - Use the **Test Connection** button to verify connectivity.
   - Ensure that TestWorthy can fetch repositories and issues.

**Tip:** Keep your API token secure and rotate it periodically for security best practices.

## Issue Synchronization: Syncing with GitHub Issues

Once connected, you can synchronize issues between TestWorthy and GitHub:

1. **Initiate Issue Sync:**
   - Go to **Integrations > GitHub Issues**.
   - Click **Sync Issues**.
   - Choose the scope:
     - Sync all issues from selected repositories.
     - Sync issues for specific projects or test plans.

2. **Configure Sync Settings:**
   - Decide whether to:
     - Import GitHub issues into TestWorthy as test cases or defects.
     - Push TestWorthy issues back to GitHub.
   - Set synchronization frequency (manual or scheduled).

3. **Perform Manual Sync:**
   - Click **Sync Now** to fetch latest issues.
   - Review imported issues in TestWorthy, linked to corresponding GitHub issues.

4. **Automate Periodic Sync:**
   - Set up scheduled sync jobs if supported.
   - Ensure the sync process runs without conflicts.

**Note:** During sync, TestWorthy will match issues based on identifiers or titles. Conflicts or duplicates can be resolved via the UI.

## Field Mapping: Mapping TestWorthy Fields to GitHub Fields

Aligning custom fields ensures data consistency between platforms:

1. **Access Field Mapping Settings:**
   - Navigate to **Integrations > GitHub Field Mapping**.
   - Select the relevant repository or project.

2. **Map Custom Fields:**
   - For each TestWorthy field (e.g., Status, Priority, Assignee, Labels):
     - Choose the corresponding GitHub field.
     - For example:
       - TestWorthy **Status** → GitHub **Issue State** (Open/Closed)
       - TestWorthy **Priority** → GitHub **Labels** (High, Medium, Low)
       - TestWorthy **Assignee** → GitHub **Assignee**
       - TestWorthy **Tags** → GitHub **Labels**

3. **Configure Field Transformation Rules:**
   - Define how values are converted:
     - E.g., map "Critical" priority to GitHub label "Priority: Critical".
     - Use predefined options or custom scripts if supported.

4. **Save and Apply Mappings:**
   - Confirm the mappings.
   - Run a test sync to verify correct data transfer.

5. **Adjust Mappings as Needed:**
   - Fine-tune mappings based on sync results.
   - Use filters to exclude certain fields or issues.

**Tip:** Maintain a consistent naming convention for labels and statuses to simplify mapping.

---

By following these steps, you can seamlessly connect TestWorthy with GitHub, synchronize issues, and ensure that custom fields are accurately mapped, enabling efficient issue tracking and project management across both platforms.