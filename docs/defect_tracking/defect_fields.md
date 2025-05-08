---
sidebar_position: 3
---

# Defect Fields

This section explains how to manage and utilize defect fields within the defect tracking system, focusing on both standard and custom fields used to capture defect-related information. It guides developers on configuring defect data models, customizing defect fields, and integrating defect data into workflows.

## Overview of Defect Fields

Defect fields are data attributes associated with defect records, capturing essential information such as defect status, priority, severity, description, and custom attributes tailored to project needs. These fields enable precise defect tracking, filtering, reporting, and integration with external tools.

## Standard Defect Fields

Standard defect fields are predefined attributes that are commonly used across projects. Typical standard fields include:

- **ID**: Unique identifier for each defect.
- **Title/Summary**: Brief description of the defect.
- **Description**: Detailed defect information.
- **Status**: Current state (e.g., Open, In Progress, Resolved, Closed).
- **Priority**: Urgency level (e.g., Low, Medium, High).
- **Severity**: Impact level (e.g., Minor, Major, Critical).
- **Reported By**: User who reported the defect.
- **Assigned To**: User responsible for fixing.
- **Created Date / Last Modified Date**: Timestamps for record tracking.
- **Attachments**: Files or screenshots related to the defect.

These fields are typically configured in the defect entity model and database schema, ensuring consistent data capture.

## Custom Defect Fields

Custom fields allow projects to extend defect records with additional attributes tailored to specific workflows or reporting needs. Examples include:

- **Test Case Reference**: Link to the related test case.
- **Component**: Part of the system affected.
- **Reproducibility**: How easily the defect can be reproduced.
- **Environment**: Hardware/software environment details.
- **Steps to Reproduce**: Sequential steps to recreate the defect.
- **Root Cause**: Underlying cause analysis.
- **Resolution Notes**: Details on how the defect was fixed.

### Configuring Custom Fields

1. **Define Custom Attributes**: Extend the defect entity class to include new properties.
2. **Update Database Schema**: Create migration scripts to add new columns for custom fields.
3. **Modify Data Models**: Adjust data transfer objects (DTOs) and API contracts to include custom fields.
4. **Update UI Forms**: Add input controls for custom fields in defect creation/edit forms.
5. **Validation and Business Logic**: Implement validation rules and logic to handle custom data.

### Example: Adding a Custom Field

Suppose you want to add a "Component" field:

- **Entity Model**:
  ```csharp
  public class Defect
  {
      public int Id { get; set; }
      public string Title { get; set; }
      public string Description { get; set; }
      public string Status { get; set; }
      public string Priority { get; set; }
      public string Severity { get; set; }
      public string ReportedBy { get; set; }
      public string AssignedTo { get; set; }
      public DateTime CreatedDate { get; set; }
      public DateTime LastModifiedDate { get; set; }
      public string Component { get; set; } // Custom field
  }
  ```

- **Migration Script**:
  ```csharp
  migrationBuilder.AddColumn<string>(
      name: "Component",
      table: "Defects",
      type: "nvarchar(100)",
      nullable: true);
  ```

- **UI Form**:
  Add a dropdown or textbox for "Component" in defect creation/edit pages.

## Using Defect Fields

### Filtering and Reporting

- Use defect fields to filter defect lists (e.g., show all high-priority, open defects in a specific component).
- Generate reports based on custom fields (e.g., defect counts per component or environment).

### Integration with External Tools

- Map defect fields to external bug tracking systems like Jira, TestRail, or Azure DevOps.
- Synchronize defect data, ensuring custom fields are correctly transferred.

### Best Practices

- Maintain consistency in field naming and data types.
- Use enumerations or lookup tables for fields like Status, Priority, and Severity.
- Document custom fields clearly for team understanding.
- Validate custom fields to prevent invalid data entry.

## Summary

Managing defect fields involves configuring both standard and custom attributes within defect records to suit project requirements. Proper setup ensures accurate defect tracking, effective filtering, comprehensive reporting, and seamless integration with external tools. Developers should extend the defect data model thoughtfully, update the database schema via migrations, and adapt UI components to support custom fields for a flexible defect management process.