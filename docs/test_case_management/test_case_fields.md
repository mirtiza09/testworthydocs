---
sidebar_position: 3
---

# Test Case Fields

This section explains the standard and custom fields used within test cases in the test management platform. It guides developers on how to handle, extend, and utilize test case fields effectively during development and customization.

## Overview

Test cases are central entities in the test management system, capturing individual test scenarios, steps, expected results, and associated metadata. Fields within test cases can be standard (predefined) or custom (user-defined), allowing flexibility to adapt to various testing needs.

## Standard Test Case Fields

These are the core fields typically present in every test case:

- **ID**: Unique identifier for the test case.
- **Title**: The name or brief description of the test case.
- **Description**: Detailed information about what the test case covers.
- **Preconditions**: Conditions that must be met before executing the test.
- **Steps**: Sequential steps to perform during testing.
- **Expected Result**: The anticipated outcome if the test passes.
- **Actual Result**: The observed outcome after execution.
- **Status**: Current state (e.g., Passed, Failed, Blocked).
- **Priority**: Importance level (e.g., High, Medium, Low).
- **Type**: Categorization (e.g., Functional, Regression).
- **Tested By**: User who executed the test.
- **Tested Date**: When the test was executed.
- **Attachments**: Files or screenshots linked to the test case.

These fields are stored in the database with corresponding properties in the data model, typically defined in the `TestCase` entity class.

## Custom Fields

To meet specific project requirements, custom fields can be added to extend the test case data model:

- **Test Data**: Additional data inputs used during testing.
- **Regression**: Boolean indicating if the test is part of regression suite.
- **Reviewed by PM/QALead/QAManager**: Flags indicating review status.
- **Smoke**: Boolean flag for smoke test inclusion.
- **To Automate**: Indicator whether the test case should be automated.
- **Test Data**: String for additional test data inputs.

Custom fields are stored in a flexible schema, often via a JSON column or a dedicated custom fields table, allowing dynamic addition without altering core schema.

## Usage Instructions

### Viewing Test Case Fields

1. Navigate to the test case detail page.
2. Review the standard fields displayed in the overview section.
3. For custom fields:
   - If using a JSON or dynamic schema, locate the "Custom Fields" section.
   - Use the UI to view, edit, or add custom fields as needed.

### Adding or Editing Fields

1. To add a custom field:
   - Access the test case edit form.
   - Locate the "Custom Fields" section.
   - Enter the field name and value.
   - Save changes; the system will store the data accordingly.
2. To modify existing fields:
   - Edit the test case.
   - Update the desired fields.
   - Save to persist changes.

### Extending Test Case Fields

- Developers can extend the data model by:
  - Adding new properties to the `TestCase` entity class.
  - Updating the database schema via migrations.
  - Modifying the UI to display new fields.
  - Ensuring validation and data binding are handled appropriately.

### Example: Adding a "Reviewed by" Custom Field

1. Update the `TestCase` entity to include a new property:
```csharp
public string ReviewedBy { get; set; }
```
2. Create a migration to add this column to the database.
3. Update the UI form to include an input for "Reviewed by".
4. Handle data binding and validation.
5. Save and display the new field in test case details.

## Implementation Details

- **Data Model**: Test cases are represented by the `TestCase` class, which includes properties for each field.
- **Database Schema**: Fields are mapped via Entity Framework migrations, with support for nullable or required constraints.
- **UI Components**: Forms and detail views are built using Razor views or frontend frameworks, binding to the model properties.
- **Custom Fields Storage**: For dynamic fields, a JSON column or related table stores key-value pairs, enabling flexible extension without schema changes.

## Important Interactions

- **Test Runs**: When executing test cases, fields like "Tested By" and "Tested Date" are populated.
- **Reporting**: Fields such as "Priority", "Status", and custom flags are used in reports and dashboards.
- **Automation**: The "To Automate" flag guides automation scripts to identify candidate test cases.
- **Attachments**: Files linked to test cases are stored and retrieved based on the "Attachments" field.

## Notable Implementation Tips

- Use migrations to add or modify fields to maintain schema consistency.
- For custom fields, prefer a flexible storage (JSON or key-value table) to avoid frequent schema changes.
- Ensure UI forms are updated to handle new fields with proper validation.
- Maintain data integrity by validating required fields and data types.
- Leverage existing data annotations and validation frameworks for consistency.

## Summary

Understanding and managing test case fields—both standard and custom—is crucial for effective test management and reporting. Developers should follow the outlined procedures for extending and utilizing these fields, ensuring data consistency and UI coherence.

---

*Tip:* Always back up your database before applying schema changes, and test UI updates thoroughly to prevent data loss or UI inconsistencies.