---
sidebar_position: 1
---

# Creating Test Suites

This section explains how to organize test cases into test suites within the application. Test suites serve as containers to group related test cases, enabling better management, execution, and reporting of testing activities.

## Accessing the Test Suites Management

1. **Navigate to the Test Suites Section:**
   - Log into the application.
   - From the main dashboard, locate the sidebar or top menu.
   - Click on **Test Management** or **Test Suites** (depending on your UI layout).
   - Alternatively, access via URL if direct link is available, e.g., `/test-suites`.

2. **View Existing Test Suites:**
   - The list of test suites will display with options to create, edit, or delete.

## Creating a New Test Suite

1. **Click on "Add New" or "Create Test Suite":**
   - Usually represented by a button labeled **Add Test Suite** or a "+" icon.
   
2. **Fill in the Test Suite Details:**
   - Enter a **Name** for the suite.
   - Provide an optional **Description** to clarify its purpose.
   - Select a **Parent Suite** if nesting is supported (for hierarchical organization).
   - Configure additional settings if available (e.g., tags, priority).

3. **Save the Test Suite:**
   - Click **Save** or **Create**.
   - The new suite will appear in the list, ready to contain test cases.

## Organizing Test Cases into a Suite

1. **Open the Target Test Suite:**
   - Click on the suite name from the list.
   - You will see an interface to manage test cases within this suite.

2. **Add Existing Test Cases:**
   - Click on **Add Test Cases** or **Add Existing**.
   - Search or filter available test cases.
   - Select one or multiple test cases.
   - Confirm to add them to the suite.

3. **Create New Test Cases within the Suite:**
   - Use the **Add Test Case** button.
   - Fill in test case details such as:
     - Title
     - Description
     - Preconditions
     - Steps
     - Expected Results
   - Save to include in the suite.

4. **Arrange Test Cases:**
   - Drag and drop test cases to reorder within the suite if supported.
   - Use options like **Move Up/Down** or **Indent/Outdent** for hierarchical organization.

## Managing Test Suites

- **Edit a Suite:**
  - Click on the suite name.
  - Modify details such as name, description, or hierarchy.
  - Save changes.

- **Delete a Suite:**
  - Select the suite.
  - Click **Delete**.
  - Confirm deletion; note that deleting a suite may also remove or reassign contained test cases depending on system behavior.

- **Copy or Clone a Suite:**
  - Use the **Clone** option if available to duplicate a suite with its test cases.

## Best Practices for Organizing Test Suites

- Use meaningful names reflecting the test scope.
- Group related test cases logically (e.g., by feature, module, or test phase).
- Maintain a clear hierarchy for complex projects.
- Regularly review and clean up outdated or redundant suites.

## Summary

Organizing test cases into test suites involves creating suites, adding existing or new test cases, arranging their order, and managing their hierarchy. This structure enhances test management, execution efficiency, and reporting clarity.

---

**Tip:** Always ensure test cases are correctly linked to their suites before executing or generating reports to maintain traceability and coverage.