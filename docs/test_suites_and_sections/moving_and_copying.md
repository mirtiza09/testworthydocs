---
sidebar_position: 3
---

# Moving and Copying

This section provides detailed, step-by-step instructions for moving or copying test cases between different test suites and sections within the test management platform. It covers the user interface interactions, underlying processes, and considerations to ensure successful transfer of test cases.

## Accessing the Test Case Management Interface

1. Log into the test management platform with appropriate permissions.
2. Navigate to the **Test Suites** or **Test Cases** section from the main menu.
3. Locate the specific **Test Suite** or **Section** that contains the test cases you want to move or copy.

## Selecting Test Cases for Moving or Copying

1. Within the test suite or section, identify the list or grid of test cases.
2. Use the checkboxes or selection controls to select one or multiple test cases:
   - To select all test cases, click the **Select All** checkbox or button if available.
   - To select individual test cases, click their respective checkboxes.

## Initiating the Move or Copy Action

1. After selecting the desired test cases, look for the **Actions** menu or toolbar.
2. Click on the **Move** or **Copy** option:
   - The **Move** option will transfer the test cases from their current location to the target suite/section.
   - The **Copy** option will duplicate the test cases into the target location, leaving the originals intact.

## Choosing the Destination Suite or Section

1. A dialog or dropdown menu will appear prompting you to select the destination:
   - Choose the target **Test Suite** or **Section** from the list.
   - If applicable, select a specific subsection or category.
2. Confirm your selection:
   - Some platforms may allow you to select multiple destination locations if supported.
   - Ensure the destination is correct before proceeding.

## Confirming the Move or Copy Operation

1. Review the selected test cases and destination.
2. Click the **Confirm** or **OK** button to execute the operation.
3. The system will process the request:
   - For **Move**, the test cases will be relocated.
   - For **Copy**, duplicates will be created in the new location.

## Post-Operation Checks

1. Verify that the test cases appear in the target suite or section.
2. Confirm that the original test cases are removed (for move) or still present (for copy).
3. Check the test case details to ensure all relevant data has been transferred or duplicated correctly.

## Additional Tips

- **Bulk Operations**: Use filters or search to quickly locate large sets of test cases.
- **Undo/Cancel**: If available, use the undo or cancel options if you realize a mistake immediately.
- **Permissions**: Ensure you have the necessary permissions to move or copy test cases across suites or sections.
- **Dependencies**: Be aware of dependencies or linked test cases that might be affected by the move or copy.

## Implementation Notes

- The move and copy functionalities are typically implemented via backend APIs that handle database updates.
- The user interface triggers these APIs through AJAX calls upon confirmation.
- The system updates the test case relationships, hierarchy, and metadata accordingly.
- Proper validation ensures that test cases are not moved or copied into incompatible or restricted sections.

By following these steps, users can efficiently reorganize their test cases, maintain data integrity, and streamline test management workflows.

---