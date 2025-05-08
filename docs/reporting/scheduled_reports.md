---
sidebar_position: 7
---

# Scheduled Reports

This section explains how to set up and manage scheduled reports within the application. It covers configuring automated report generation, scheduling their distribution, and ensuring timely delivery to stakeholders.

## Setting Up Automated Report Generation and Distribution

Follow these step-by-step instructions to configure scheduled reports:

### 1. Access the Reports Configuration

- Log in to the application with appropriate permissions.
- Navigate to the **Reports** section from the main menu.
- Locate the **Scheduled Reports** subsection or tab.

### 2. Create a New Scheduled Report

- Click on the **Create New Schedule** button.
- Fill in the required details:
  - **Report Name**: Enter a descriptive name for the report.
  - **Report Type**: Select the type of report (e.g., Test Summary, Milestone Report).
  - **Frequency**: Choose how often the report should run (daily, weekly, monthly).
  - **Time**: Specify the exact time for report generation.
  - **Recipients**: Add email addresses or user groups to receive the report.

### 3. Configure Report Parameters

- Define filters and parameters:
  - Select specific projects, milestones, or test suites.
  - Set date ranges or other relevant filters.
- Save the parameters to customize the report content.

### 4. Schedule and Enable

- Review the schedule details.
- Enable the report by toggling the **Active** switch.
- Confirm by clicking **Save** or **Activate**.

### 5. Verify Scheduled Jobs

- Navigate to the **Scheduled Jobs** or **Task Scheduler** section.
- Ensure the report job appears in the list.
- Check the next scheduled run time.

### 6. Monitor Report Delivery

- After the scheduled time, verify email delivery:
  - Check inboxes of recipients.
  - Confirm the report content matches expectations.
- Review logs or job status for any errors.

### 7. Manage Existing Reports

- To modify a scheduled report:
  - Locate it in the list.
  - Click **Edit**.
  - Adjust parameters, frequency, or recipients.
  - Save changes.
- To disable or delete:
  - Toggle **Active** off or select **Delete**.

## Important Tips

- Ensure email addresses are correct and verified.
- Test the schedule with a dummy recipient before full deployment.
- Regularly review scheduled reports for relevance and accuracy.
- Use the **Report Preview** feature (if available) to verify content before scheduling.

## Additional Notes

- Reports are generated asynchronously; large datasets may take longer.
- The system supports multiple concurrent scheduled reports.
- For troubleshooting, check the **Job Logs** or **Report History** for errors or delivery issues.

By following these steps, you can automate report generation and ensure stakeholders receive timely insights into testing progress and project status.