---
sidebar_position: 2
---

# Defect Workflow

This section explains how defects (bugs or issues) progress through their lifecycle within the defect tracking system. It provides a step-by-step guide for developers to understand how defects are created, updated, assigned, resolved, and closed, including the key states, transitions, and actions involved.

## Accessing the defect workflow

1. Log into the defect tracking module of the application.
2. Navigate to the "Defects" or "Issues" section from the main menu.
3. Select an existing defect or create a new defect to observe the workflow.

## Creating a new defect

- Click on the "Create Defect" button.
- Fill in the required fields such as title, description, severity, priority, and assign it to a responsible team member.
- Set the initial status to **Open**.
- Save the defect to initiate its lifecycle.

## Defect lifecycle stages

The defect progresses through the following primary states:

### 1. Open

- The defect has been reported but not yet reviewed or assigned.
- Actions:
  - Assign the defect to a developer or team member.
  - Change severity or priority if needed.
  - Add comments or attachments for additional context.

### 2. In Progress / Assigned

- The defect has been acknowledged and work has started.
- Actions:
  - Update status to **In Progress**.
  - Log work hours or notes.
  - Communicate with testers or stakeholders about progress.

### 3. Resolved / Fixed

- The developer has fixed the defect.
- Actions:
  - Mark the defect as **Resolved** or **Fixed**.
  - Attach relevant fix details or code references.
  - Notify testers for verification.

### 4. Verified / Closed

- The QA team verifies the fix.
- Actions:
  - Test the defect fix.
  - If verified, change status to **Closed**.
  - If not fixed, revert to **Reopened**.

### 5. Reopened

- The defect reappears or the fix is inadequate.
- Actions:
  - Change status back to **Reopened**.
  - Assign to the appropriate developer.
  - Repeat the cycle as necessary.

## Transition actions

- Moving between states involves specific actions:
  - **Assign**: Allocate defect to a team member.
  - **Resolve**: Mark as fixed after developer action.
  - **Verify**: QA confirms whether the defect is fixed.
  - **Close**: Finalize the defect after successful verification.
  - **Reopen**: Revert to an earlier state if defect persists.

## Additional actions and considerations

- Add comments at any stage to document findings, progress, or reasons for status changes.
- Attach logs, screenshots, or files to provide evidence or details.
- Change severity or priority as the defect's impact evolves.
- Use filters and dashboards to track defect statuses and lifecycle progress.

## Summary flowchart

```plaintext
[Open] --> [In Progress] --> [Resolved] --> [Verified] --> [Closed]
   |                                              ^
   |                                              |
   +---------------------------------------------- [Reopened]
```

## Tips for managing defect lifecycle

- Always update the defect status promptly to reflect current progress.
- Maintain clear and detailed comments for transparency.
- Reassign defects as needed to ensure timely resolution.
- Use the defect history to review past actions and decisions.

By understanding and properly managing each stage of the defect lifecycle, developers can ensure efficient resolution, clear communication, and high-quality software delivery.