---
sidebar_position: 5
---

# Test Case Management

This section provides a detailed guide for managing test cases within the platform, covering the structure, creation, fields, versioning, importing/exporting, bulk operations, and templating. Follow these step-by-step instructions to effectively utilize and extend test case functionalities.

## Understanding the Test Case Structure

Test cases are organized entities that encapsulate all necessary information for testing a feature or requirement. Each test case typically includes:

- **Identification**: Unique ID, name, and description.
- **Fields**: Standard fields such as preconditions, steps, expected results, status, priority, and custom fields.
- **Versioning**: Multiple versions to track changes over time.
- **Attachments**: Supporting files like screenshots or logs.
- **Relations**: Links to test runs, defects, or related test cases.

Understanding this structure helps in designing comprehensive and maintainable test cases.

## Creating Test Cases

To create effective test cases, follow these steps:

1. **Navigate to the Test Cases Section**:
   - Click on the "Test Cases" menu item in the main navigation.
   - Select the relevant project or suite.

2. **Initiate Creation**:
   - Click on the "Add New" or "Create Test Case" button.
   - Choose a template if available for consistency.

3. **Fill in Required Fields**:
   - Enter a descriptive **Test Case Name**.
   - Provide detailed **Description** and **Preconditions**.
   - Define **Test Steps** with clear, actionable instructions.
   - Specify **Expected Results** for each step.
   - Set **Priority**, **Status**, and other relevant fields.

4. **Attach Supporting Files**:
   - Upload screenshots, logs, or other relevant documents.

5. **Save the Test Case**:
   - Click "Save" or "Create" to finalize.

*Tip:* Use templates for common test case types to ensure consistency.

## Test Case Fields

Test cases include a mix of standard and custom fields:

- **Standard Fields**:
  - Name
  - Description
  - Preconditions
  - Test Steps
  - Expected Results
  - Status (Passed, Failed, Blocked, etc.)
  - Priority (High, Medium, Low)
  - Assigned To
  - Tags

- **Custom Fields**:
  - Test Data
  - Environment
  - Automation Status
  - Custom Attributes defined by your organization

*Note:* Custom fields can be configured in the system settings to tailor test cases to your process.

## Test Case Versioning

Version control allows tracking changes over time:

1. **Automatic Versioning**:
   - Each update to a test case creates a new version.
   - Previous versions are retained for audit and rollback.

2. **Manual Versioning**:
   - When editing, select "Create New Version" if you want to preserve the current state before changes.
   - Use version history to compare or revert to earlier versions.

3. **Viewing Versions**:
   - Access the version history from the test case detail page.
   - Review differences and restore if necessary.

*Tip:* Use versioning to document iterative improvements or corrections.

## Importing and Exporting Test Cases

### CSV Import/Export

- **Export**:
  1. Navigate to the Test Cases list.
  2. Click on "Export" and select CSV format.
  3. Save the file locally.

- **Import**:
  1. Prepare a CSV file with test case data matching the system fields.
  2. Click on "Import" and upload the CSV.
  3. Map columns if prompted.
  4. Confirm and import.

*Tip:* Use templates to structure CSV files correctly.

### Excel Import/Export

- Similar to CSV, but with XLSX files:
  - Export test cases to Excel for editing.
  - Import edited Excel files back into the system.

### TestRail Import

- For migrating from TestRail:
  1. Use the dedicated import feature.
  2. Provide TestRail export files or API credentials.
  3. Map test case fields accordingly.
  4. Initiate import and verify data.

*Note:* Ensure field mappings are correct to preserve data integrity.

## Bulk Operations

Perform actions on multiple test cases simultaneously:

1. **Select Multiple Test Cases**:
   - Use checkboxes in the list view.
   - Use "Select All" for bulk actions.

2. **Choose Action**:
   - Click on bulk action buttons such as:
     - Change Status
     - Assign To
     - Move to Suite
     - Delete

3. **Configure and Confirm**:
   - Set parameters for the action.
   - Confirm to apply changes.

*Tip:* Use bulk operations to update statuses after a test run or assign multiple cases to a tester.

## Test Case Templates

Create and use templates for consistent test case creation:

1. **Create a Template**:
   - Design a test case with common fields filled.
   - Save as a template for reuse.

2. **Apply Template**:
   - When creating a new test case, select the template.
   - Modify fields as needed.

3. **Manage Templates**:
   - Edit or delete existing templates from the templates management section.

*Tip:* Use templates for recurring test scenarios to save time and ensure uniformity.

---

This guide equips you with the essential steps and best practices for managing test cases effectively within the platform. Proper use of versioning, bulk operations, and templates ensures maintainability and consistency across your testing efforts.