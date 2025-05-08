---
sidebar_position: 11
---

# Integrations

This section guides developers through setting up and utilizing the various third-party integrations supported by the platform, including Jira, Azure DevOps, GitHub, and TestRail migration tools, as well as the API interface for custom integrations.

## Jira Integration

### Setup and Configuration
- Navigate to the integrations settings page within the platform.
- Locate the Jira integration section.
- Enter your Jira instance URL, API token, and username in the provided fields.
- Save the configuration to establish the connection.
- Ensure that the Jira plugin is enabled and correctly configured.

### Issue Synchronization
- When creating or updating test cases and defects in the platform, they can be synchronized with Jira issues.
- To sync, select the test case or defect and choose the 'Sync with Jira' option.
- The system will automatically create or update the corresponding Jira issue.
- Changes made in Jira (status, comments) can be synced back to the platform via the 'Refresh' option.

### Field Mapping
- Access the Jira field mapping configuration.
- Map platform-specific fields (e.g., test case title, description, status) to Jira issue fields.
- Save the mappings.
- During synchronization, the system uses these mappings to align data correctly.

## Azure DevOps Integration

### Setup and Configuration
- Go to the integrations settings.
- Select Azure DevOps.
- Provide your Azure DevOps organization URL, project name, and access token.
- Save the configuration.
- Verify the connection by testing the API call.

### Work Item Synchronization
- Link test cases or defects to Azure DevOps work items.
- Use the 'Sync with Azure DevOps' option.
- The system will create or update work items in Azure DevOps accordingly.
- Changes in Azure DevOps (status, comments) can be pulled into the platform.

### Field Mapping
- Configure field mappings between platform entities and Azure DevOps work item fields.
- Map test case fields like title, description, state, and assigned to.
- Save the mappings to ensure proper data synchronization.

## GitHub Integration

### Setup and Configuration
- Access the GitHub integration section.
- Enter your repository URL, personal access token, and branch details.
- Save and test the connection.
- Enable the integration for relevant projects.

### Issue Synchronization
- Link GitHub issues with test cases or defects.
- Use the 'Sync with GitHub' feature.
- The system will create or update issues in GitHub based on platform data.
- Comments, status updates, and labels can be synchronized bidirectionally.

### Field Mapping
- Map platform fields such as title, description, labels, and assignee to GitHub issue fields.
- Save the mappings for consistent data exchange.

## TestRail Migration

### Tools and Processes
- Use the migration tool provided within the platform.
- Export your existing TestRail data (test cases, test runs, results).
- Import the data into the platform via the migration interface.
- Map TestRail fields to platform entities during import.
- Validate data integrity post-migration.
- Use the migration logs to troubleshoot issues.

## API Integration

### API Overview
- The platform exposes a RESTful API for custom integrations.
- Supports CRUD operations for test cases, test runs, defects, and projects.
- Uses JSON format for request and response payloads.

### Authentication
- Authenticate via API keys or OAuth tokens.
- Include the token in the `Authorization` header (`Bearer <token>`).

### Endpoints
- `/api/projects`: Manage projects.
- `/api/testcases`: Create, retrieve, update, delete test cases.
- `/api/testruns`: Manage test runs.
- `/api/defects`: Handle defect reports.
- `/api/auth`: Authentication endpoints.

### Examples
```bash
# Retrieve all test cases
curl -H "Authorization: Bearer <token>" https://yourdomain.com/api/testcases

# Create a new test case
curl -X POST -H "Content-Type: application/json" -H "Authorization: Bearer <token>" \
-d '{"title": "Login Test", "description": "Verify login functionality"}' \
https://yourdomain.com/api/testcases
```

This section provides the foundational steps for integrating external tools, enabling seamless synchronization, data consistency, and automation across your testing ecosystem. Proper configuration and field mapping are crucial for effective data exchange and maintaining traceability between platform entities and external systems.