---
sidebar_position: 3
---

# Test Statuses

This section explains how to interpret, modify, and extend the test status definitions within the test management system. Test statuses are critical for tracking the progress and outcome of test cases, test runs, and overall project health. Customizing test statuses allows tailoring the workflow to fit specific project requirements or organizational standards.

## Overview of Test Statuses

Test statuses are predefined categories that represent the current state of a test case or test run. Common statuses include "Passed," "Failed," "Blocked," "In Progress," and "Not Executed." These statuses are stored as entities in the database and are used throughout the application to filter, report, and visualize testing progress.

## How to View Existing Test Statuses

1. **Navigate to the Test Status Management Page:**
   - Log into the application with appropriate permissions.
   - Access the "Test Settings" or "Test Statuses" section from the main menu.
   - This page displays a list of all current statuses, their labels, colors, and descriptions.

2. **Review Status Details:**
   - Each status entry includes:
     - Status Name (e.g., "Passed")
     - Status Color (used in UI indicators)
     - Description or notes
     - Active/Inactive toggle

## How to Customize Test Statuses

### Adding a New Status

1. **Open the Test Statuses Management Page:**
   - Follow the steps above to reach the status list.

2. **Click "Add New Status":**
   - Locate the "Add" button or link.

3. **Fill in the Status Details:**
   - Enter a unique name (e.g., "Retest Needed").
   - Choose an associated color for visual identification.
   - Provide a description if necessary.

4. **Save the New Status:**
   - Click "Save" or "Create."
   - The new status will appear in the list and be available for assignment.

### Editing an Existing Status

1. **Select the Status to Edit:**
   - Click on the status entry in the list.

2. **Modify the Details:**
   - Change the name, color, description, or activation state.

3. **Save Changes:**
   - Confirm by clicking "Update" or "Save."

### Removing or Deactivating a Status

- To prevent new test cases from using a status, deactivate it.
- To delete permanently, select the status and click "Delete," if supported.
- **Tip:** Deactivation is safer to preserve historical data.

## How to Use Custom Test Statuses

- When creating or updating test cases and test runs, select the desired status from the dropdown.
- Use filters to generate reports based on custom statuses.
- Visual indicators (colors) help quickly assess test progress in dashboards.

## Technical Details for Developers

### Modifying Test Status Entities

Test statuses are stored in the database table, typically named `Statuses`. The entity class may look like:

```csharp
public class Status
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string ColorHex { get; set; }
    public string Description { get; set; }
    public bool IsActive { get; set; }
}
```

### Extending Statuses Programmatically

To add or modify statuses via code:

1. **Create a migration:**

```bash
Add-Migration AddCustomTestStatus
```

2. **Update the migration code:**

```csharp
migrationBuilder.InsertData(
    table: "Statuses",
    columns: new[] { "Name", "ColorHex", "Description", "IsActive" },
    values: new object[] { "Retest Needed", "#FFA500", "Test requires retesting", true }
);
```

3. **Apply the migration:**

```bash
Update-Database
```

### Customizing Statuses at Runtime

- Use the API endpoints or admin UI to add, edit, or deactivate statuses.
- Ensure that test cases and runs reference the correct status IDs or names.

## Best Practices

- Use consistent naming conventions.
- Assign meaningful colors for quick visual recognition.
- Keep descriptions clear to aid understanding.
- Deactivate obsolete statuses instead of deleting to maintain data integrity.
- Document custom statuses in project guidelines.

## Summary

Customizing test statuses involves managing the status entities through the application's UI or programmatically via code and migrations. Proper configuration ensures accurate tracking, reporting, and visualization of testing activities aligned with your project workflows. Always test changes in a staging environment before deploying to production to prevent data inconsistencies.

---

*Tip:* For advanced customization, consider extending the status entity with additional properties such as severity, priority, or custom flags, depending on your testing process needs.