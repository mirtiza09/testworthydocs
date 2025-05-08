---
sidebar_position: 2
---

# Access Control

This section explains how to control user access to various features and data within the TestWorthy platform. Proper access control ensures that users can only view or modify data and functionalities permitted by their roles and permissions.

## Overview of Access Control

Access control in TestWorthy is managed through a combination of user roles, permissions, and feature toggles. Users are assigned roles such as Administrator, Project Manager, QA Lead, or Tester, each with predefined access levels. Permissions specify what actions a role can perform, such as creating test cases, viewing reports, or modifying configurations.

## How to Manage User Roles and Permissions

1. **Assigning Roles to Users**
   - Navigate to the User Management section.
   - Select a user or create a new user.
   - Assign a role from the available options (e.g., Admin, QA Lead, Tester).
   - Save changes to update the user's role.

2. **Configuring Role Permissions**
   - Go to the Roles & Permissions settings.
   - Select a role to modify.
   - Enable or disable specific permissions such as:
     - View Test Cases
     - Create Test Cases
     - Edit Test Cases
     - Delete Test Cases
     - View Reports
     - Manage Projects
     - Configure Settings
   - Save the role configuration.

3. **Feature Toggles**
   - Some features can be enabled or disabled globally or per project.
   - Access the Feature Management panel.
   - Toggle features like Test Data Management, Integration Settings, or Advanced Reporting.
   - Save to apply changes.

## Managing Access to Specific Data

1. **Project-Level Access**
   - Assign users to projects with specific roles.
   - Use the Project Access Control panel to restrict or grant access.
   - Users with limited access can only view or modify data within assigned projects.

2. **Test Case and Test Run Restrictions**
   - Use permissions to restrict who can create, edit, or delete test cases and runs.
   - For sensitive test data, assign read-only permissions to certain users.

3. **Audit Trails and Logs**
   - Maintain logs of user actions for compliance and review.
   - Access logs via the Audit Trail feature to monitor data access and modifications.

## Best Practices for Access Control

- Always assign the least privilege necessary for a user's role.
- Regularly review user roles and permissions.
- Use project-level access controls to isolate sensitive data.
- Enable audit logging for critical actions.
- Use feature toggles to gradually roll out new features or restrict access during maintenance.

## Summary

Managing access to features and data in TestWorthy involves assigning appropriate roles, configuring permissions, and controlling project-level access. Regular reviews and audits help maintain security and ensure users only access what they are authorized to. Proper access control safeguards sensitive information and maintains the integrity of your testing environment.