---
sidebar_position: 4
---

# Test Statuses

This section explains how to modify and tailor test statuses within the test management system. Test statuses represent different states a test case or test run can be in, such as "Passed," "Failed," "Blocked," etc. Customizing these statuses allows you to align the system with your specific workflow, reporting needs, and project requirements.

## Accessing Test Status Configuration

1. **Navigate to the Settings Menu**  
   - Log into the application with an administrator or user with configuration privileges.  
   - Locate the main menu or sidebar, and click on **Configuration**.  
   - From the dropdown or submenu, select **Test Statuses**.

2. **Open the Test Statuses Page**  
   - The page displays a list of existing statuses, their labels, colors, and behaviors.  
   - You will see options to add, edit, or delete statuses.

## Customizing Existing Test Statuses

1. **Select a Status to Edit**  
   - Click on the status name or the edit icon (usually a pencil) next to the status you want to modify.

2. **Modify Status Properties**  
   - **Label**: Change the display name (e.g., "Passed" to "Success").  
   - **Color**: Choose a color that visually represents the status (e.g., green for success).  
   - **Behavior**: Define what happens when this status is assigned, such as triggering notifications or updating related fields.

3. **Configure Status Behavior**  
   - Some statuses may have associated behaviors, such as automatically moving to another status after a certain period, or triggering a workflow step.  
   - Adjust these settings as needed, often via checkboxes or dropdowns.

4. **Save Changes**  
   - Click **Save** or **Update** to apply modifications.

## Adding a New Test Status

1. **Click on the Add New Status Button**  
   - Usually labeled **Add Status** or **New Status**.

2. **Fill in Status Details**  
   - **Label**: Enter a descriptive name (e.g., "In Review").  
   - **Color**: Select an appropriate color.  
   - **Behavior**: Define any specific behaviors or triggers associated with this status.

3. **Set Priority or Order** (Optional)  
   - Arrange the status in the desired sequence or priority level, if the system supports ordering.

4. **Confirm and Save**  
   - Click **Create** or **Save** to add the new status to the list.

## Configuring Test Status Behaviors

1. **Define Transition Rules**  
   - Access the **Status Transition** settings, often found under **Workflow** or **Behavior** tab.  
   - Specify allowed transitions between statuses (e.g., "Failed" can move to "Retest" but not directly to "Passed").  
   - Use drag-and-drop or dropdowns to set these rules.

2. **Set Automated Actions**  
   - For each status, define actions such as sending notifications, updating fields, or triggering scripts.  
   - These are configured via checkboxes, dropdowns, or custom scripts depending on the system.

3. **Enable or Disable Behaviors**  
   - Toggle behaviors like auto-assign, notifications, or status locking.

## Important Tips

- **Consistency**: Use clear, descriptive labels to avoid confusion.  
- **Colors**: Choose intuitive colors that match common conventions (e.g., green for success, red for failure).  
- **Workflow**: Map out your testing process to ensure status transitions reflect your actual workflow.  
- **Testing**: After customizing, perform test runs to verify that statuses behave as expected.

## Summary

Customizing test statuses involves editing existing entries or creating new ones through the **Test Statuses** configuration page. You can define labels, colors, behaviors, and transition rules to tailor the testing workflow to your project's needs. Proper configuration ensures clear reporting, efficient workflows, and accurate status tracking.

> **Tip:** Always document your custom statuses and transitions for team clarity and future maintenance.