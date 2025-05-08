---
sidebar_position: 9
---

# Defect Tracking

This section provides detailed instructions on how to create, manage, and report defects within the testing platform. It covers the entire defect lifecycle, including recording defects, understanding their workflow, defining relevant fields, linking defects to test cases, and generating comprehensive defect reports.

## Creating Defects

To record a new defect:

1. **Navigate to the Defects Module:**
   - Log into the application.
   - From the main menu, select **Defects** or **Bug Tracking**.

2. **Open the 'Create New Defect' Form:**
   - Click on the **Add New Defect** button, typically located at the top right corner.
   - Alternatively, select a test case or test run, and choose **Report Defect** from the context menu.

3. **Fill in Defect Details:**
   - **Title/Summary:** Enter a concise description of the defect.
   - **Description:** Provide detailed information about the defect, steps to reproduce, expected vs. actual results.
   - **Defect Fields:** Populate standard fields such as severity, priority, status, assigned to, and defect type.
   - **Custom Fields:** Fill any custom fields configured for your project (e.g., environment, build version).

4. **Attach Evidence:**
   - Upload relevant screenshots, logs, or files by clicking the **Attach Files** button.

5. **Link to Test Cases:**
   - If applicable, associate the defect with specific test cases or test runs (see linking defects below).

6. **Save the Defect:**
   - Click **Save** or **Create**.
   - The defect will now be listed in the defect repository with a unique ID.

## Understanding the Defect Workflow

Defects progress through a predefined lifecycle:

1. **Open:** The defect is newly reported and awaiting triage.
2. **In Progress:** Assigned to a developer or responsible team member for investigation.
3. **Resolved:** The defect has been fixed and verified.
4. **Closed:** The defect has been verified and marked as resolved definitively.
5. **Reopened:** If the defect persists or reappears after resolution, it can be reopened for further investigation.

**Workflow Steps:**

- When creating a defect, set its initial status to **Open**.
- Transition between statuses is managed via the defect detail page, with options like **Start Progress**, **Resolve**, **Close**, or **Reopen**.
- Each transition may require comments or evidence, depending on project policies.

## Defect Fields

Defects include both standard and custom fields:

### Standard Fields:
- **ID:** Unique identifier.
- **Title/Summary:** Brief description.
- **Description:** Detailed defect info.
- **Severity:** Critical, High, Medium, Low.
- **Priority:** Urgent, High, Normal, Low.
- **Status:** Open, In Progress, Resolved, Closed, Reopened.
- **Assigned To:** Responsible team member.
- **Reported By:** User who reported.
- **Created Date:** Timestamp.
- **Last Updated:** Timestamp.
- **Type:** Bug, Enhancement, Task, etc.

### Custom Fields:
- **Environment:** e.g., staging, production.
- **Build Version:** Specific build where defect was found.
- **Module:** Part of the application affected.
- **Repro Steps:** Specific steps to reproduce.
- **Screenshots/Logs:** Attachments.

*Note:* Custom fields are configurable per project and can include any additional data relevant to defect tracking.

## Linking Defects to Test Cases

To associate defects with test cases:

1. **Open the Defect Details:**
   - From the defect list, click on the defect ID.

2. **Use the 'Link to Test Case' Feature:**
   - Locate the **Linked Test Cases** section.
   - Click **Add Link** or **Associate Test Case**.

3. **Select the Test Case:**
   - Search for the relevant test case by ID or name.
   - Select the test case from the list.

4. **Confirm the Link:**
   - Click **Save** or **Link**.
   - The defect is now linked to the test case, enabling traceability.

**Alternatively**, when viewing a test case, you can report a defect directly from the context menu or action buttons, which automatically links the defect to that test case.

## Generating Defect Reports

To analyze defect status and trends:

1. **Navigate to the Reports Module:**
   - Select **Defect Reports** or **Bug Trends**.

2. **Configure Report Parameters:**
   - Filter by:
     - Status (Open, Resolved, Closed)
     - Severity
     - Priority
     - Assigned To
     - Date Range
     - Project or Module

3. **Generate the Report:**
   - Click **Run Report**.
   - The system will compile data into charts, tables, or downloadable formats (PDF, Excel).

4. **Export or Share:**
   - Download the report for offline analysis.
   - Share via email or integrate with dashboards.

**Tip:** Use saved filters to quickly access common defect views and monitor defect trends over time.

---

This guide provides the essential steps to effectively create, manage, link, and report defects, ensuring comprehensive defect lifecycle management within your testing process.