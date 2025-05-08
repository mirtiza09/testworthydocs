---
sidebar_position: 5
---

# Custom Reports

This section guides developers through the process of creating, customizing, and saving reports within the application. It covers the steps to define report parameters, generate reports based on user selections, and persist custom report configurations for future use.

## Step 1: Access the Reports Module

- Navigate to the Reports section via the main menu.
- Click on the "Create New Report" button to initiate a new report setup.

## Step 2: Define Report Parameters

- Select the report type from available options (e.g., Test Summary, Milestone Report, Test Run Details).
- Configure filters:
  - Choose relevant projects, milestones, test suites, or test cases.
  - Set date ranges or specific criteria.
- Customize columns:
  - Select which data fields to include in the report.
  - Arrange column order via drag-and-drop if supported.

## Step 3: Generate the Report

- Click the "Generate" or "Run Report" button.
- The system processes the parameters and displays the report preview.
- Review the report for accuracy and completeness.

## Step 4: Save the Custom Report

- Click the "Save" button within the report preview window.
- Enter a descriptive name for the report.
- Optionally, add tags or categories for easier retrieval.
- Confirm saving to persist the report configuration.

## Step 5: Access Saved Reports

- Return to the Reports dashboard.
- Locate your saved report in the list.
- Use the "Edit" option to modify parameters or "Run" to regenerate.
- Use the "Export" options (PDF, Excel, CSV) to download the report.

## Additional Tips

- Use the "Duplicate" feature to create similar reports with minor modifications.
- Set permissions if available, to restrict report access to specific user roles.
- Schedule automatic generation if the system supports report scheduling.

## Implementation Details

- Reports are stored as configurations in the database, capturing all filter, column, and layout settings.
- When a saved report is run, the system retrieves the configuration, applies filters, and renders the report dynamically.
- Export functions generate PDF or Excel files based on the current report view, utilizing server-side or client-side rendering techniques.

## Summary

Creating and saving custom reports involves selecting report types, configuring filters and columns, generating the report preview, and persisting the configuration for future access. This process enables users to tailor reports to their specific needs and streamline recurring reporting tasks.

> **Tip:** Utilize the "Save as Template" feature (if available) to reuse report layouts across different projects or time periods.