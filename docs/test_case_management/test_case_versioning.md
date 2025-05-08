---
sidebar_position: 4
---

# Test Case Versioning

This section explains the mechanisms and processes involved in managing test case versions within the system. It covers how test case versions are created, stored, compared, and utilized during test management workflows.

## Overview

Test case versioning is a critical feature that allows tracking changes, maintaining historical records, and facilitating collaboration among testers and developers. Each test case can have multiple versions, enabling users to compare, revert, or audit modifications over time.

## Creating Test Case Versions

- **Automatic Versioning on Save:**  
  Every time a test case is modified and saved, the system automatically creates a new version. This process involves:
  1. Cloning the current state of the test case data.
  2. Incrementing the version number.
  3. Storing the previous version in the database for historical reference.

- **Manual Versioning:**  
  Users can also manually create a new version by selecting a "Create Version" option, which captures the current state without making further edits.

## Storage and Data Model

- **Version Records:**  
  Each test case version is stored as a separate record linked to the main test case entity via a foreign key. The record contains:
  - Version number
  - Change timestamp
  - Author of the change
  - Snapshot of all relevant fields (description, steps, expected results, attachments)

- **Version History:**  
  The system maintains a chronological list of versions, allowing users to browse or revert to previous states.

## Comparing Versions

- **Diff View:**  
  Users can select two versions to compare side-by-side or in a diff view. The system highlights differences in content, such as added, modified, or deleted steps and descriptions.

- **Change Highlights:**  
  The diff interface emphasizes:
  - Text differences
  - Attachment changes
  - Metadata updates (author, timestamp)

## Reverting to a Previous Version

- **Reversion Process:**  
  To revert:
  1. Select the desired previous version.
  2. Click the "Revert" button.
  3. The system copies the selected version's data into the current test case, creating a new version with the reversion timestamp and author.

- **Audit Trail:**  
  Reversion actions are logged, capturing who reverted and when.

## Version Management Best Practices

- **Regular Snapshots:**  
  Encourage frequent saving to capture incremental changes.

- **Clear Version Labels:**  
  Use descriptive comments or labels for each version to identify significant changes.

- **Access Control:**  
  Limit who can create or revert versions to maintain integrity.

- **Archiving Old Versions:**  
  Implement policies for archiving or purging outdated versions to optimize storage.

## Implementation Details

- **Data Model:**  
  The core entities involve:
  - `TestCase`: Main test case entity.
  - `TestCaseVersion`: Stores individual versions linked to `TestCase`.

- **Workflow:**
  1. On save, create a new `TestCaseVersion` record.
  2. Increment version number.
  3. Store change details and author info.
  4. Provide UI options for viewing, comparing, and reverting versions.

- **Dependencies:**
  - Versioning relies on the test case's primary key and version number.
  - Diff and revert functionalities are integrated into the test case detail view.

## Summary

Test case versioning ensures traceability, accountability, and flexibility in managing test artifacts. By automatically capturing changes, providing comparison tools, and enabling reversion, the system supports robust test management workflows that facilitate collaboration and quality assurance.

---

This concludes the overview of how versioning works for test cases in the system. For detailed implementation code, refer to the relevant modules handling `TestCase` and `TestCaseVersion` entities, as well as the UI components supporting version comparison and reversion actions.