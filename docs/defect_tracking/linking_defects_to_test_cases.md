---
sidebar_position: 4
---

# Linking Defects to Test Cases

This section explains how to associate defects with specific test cases within the system. The process involves creating, viewing, and managing defect records linked to individual test cases to facilitate tracking, debugging, and quality assurance.

## Step-by-step Instructions

### 1. Access the Test Case Details

- Log into the system and navigate to the **Test Cases** module.
- Locate the specific test case you want to link a defect to, either through search, filtering, or browsing the test suite.
- Click on the test case to open its detailed view.

### 2. Open the Defects Section

- Within the test case detail page, scroll to or locate the **Defects** subsection or tab.
- This section displays existing defects linked to this test case, if any.

### 3. Add a New Defect

- Click on the **Add Defect** button or link.
- A form or modal window will appear, prompting for defect details:
  - Defect ID or number (if manually assigned)
  - Description or summary of the defect
  - Severity or priority level
  - Status (Open, In Progress, Resolved, etc.)
  - Additional fields such as assigned developer, defect type, or comments

### 4. Link Existing Defects

- If the defect already exists in the system:
  - Use the **Link Existing Defect** option.
  - Search for the defect by ID, title, or other attributes.
  - Select the defect from the search results.
  - Confirm to establish the link.

### 5. Save the Linkage

- After entering or selecting defect details, click **Save** or **Link**.
- The defect will now appear in the test case's defect list, indicating an association.

### 6. Verify the Link

- Refresh or revisit the test case detail page.
- Confirm that the defect appears under the **Defects** section.
- Check defect details for correctness.

### 7. Manage Linked Defects

- To update or change the defect linkage:
  - Use the **Edit** option next to the defect link.
  - Modify defect details or unlink the defect if necessary.
- To remove a defect link:
  - Click **Unlink** or **Remove Link**.
  - Confirm the removal.

## Additional Tips

- Ensure you have appropriate permissions to create or modify defect links.
- Use consistent defect IDs and descriptions for clarity.
- Link defects promptly after test execution to maintain accurate defect tracking.
- Use filters and search to quickly locate existing defects for linking.

## Important Interactions

- The defect linkage is typically stored as a relationship in the database, often via foreign keys or join tables.
- When viewing a defect, you can often see linked test cases, test runs, or related defects.
- Linking defects to test cases enables comprehensive traceability from requirements to defects.

## Summary

Linking defects to test cases is a straightforward process involving opening the test case details, accessing the defects section, and creating or associating existing defect records. Proper linkage ensures effective defect management, traceability, and quality control throughout the testing lifecycle.