---
sidebar_position: 1
---

# User Roles and Permissions

This section explains the different user roles within the system and their associated permissions. Understanding these roles is crucial for managing access control, ensuring users have appropriate permissions for their responsibilities, and maintaining system security.

## Overview of User Roles

The system supports multiple user roles, each with specific permissions that determine what actions a user can perform. Common roles include:

- **Admin**: Has full access to all system features, including user management, project configuration, and permission settings.
- **Project Manager (PM)**: Responsible for overseeing projects, managing test plans, and assigning tasks. Typically has permissions to create, update, and delete project-related entities.
- **Quality Assurance (QA)**: Focused on testing activities, including creating test cases, executing tests, and reporting defects.
- **Developer**: May have permissions related to code integration, defect fixing, and sometimes test case creation.
- **Guest / Viewer**: Limited access, primarily for viewing reports, dashboards, or test results without modification rights.

*Note: The exact roles and their permissions can be customized based on organizational needs.*

## Permissions and Access Control

Permissions are granular actions assigned to roles, such as:

- **Create**: Ability to add new entities (e.g., test cases, projects).
- **Read/View**: Ability to view data and reports.
- **Update/Edit**: Modify existing entities.
- **Delete**: Remove entities from the system.
- **Manage Users**: Add or remove users, assign roles.
- **Configure Settings**: Modify system or project configurations.

Permissions are typically enforced via role-based access control (RBAC), where each user is assigned one or more roles, and each role has a set of permissions.

## Managing Roles and Permissions

### Viewing Roles and Permissions

- Navigate to the **User Management** section.
- Select **Roles** to view existing roles.
- Each role displays associated permissions, which can be viewed or edited.

### Assigning Roles to Users

- Go to **User List**.
- Select a user to modify.
- Assign or remove roles via checkboxes or dropdowns.
- Save changes to update user permissions.

### Editing Role Permissions

- Access the **Roles** management page.
- Choose a role to edit.
- Select or deselect permissions as needed.
- Save to apply changes.

### Best Practices

- Assign the **least privilege** necessary for each role.
- Regularly review role permissions to ensure they align with current responsibilities.
- Use descriptive role names to clarify permissions scope.
- Avoid assigning multiple high-privilege roles unless necessary.

## Example: Typical Role Permissions

| Role             | Can Create | Can Read | Can Update | Can Delete | Manage Users | Configure Settings |
|------------------|--------------|----------|------------|------------|----------------|--------------------|
| Admin            | Yes          | Yes      | Yes        | Yes        | Yes            | Yes                |
| Project Manager  | Yes          | Yes      | Yes        | No         | No             | Limited            |
| QA               | No           | Yes      | Yes        | No         | No             | No                 |
| Developer        | No           | Yes      | Limited    | No         | No             | No                 |
| Guest / Viewer   | No           | Yes      | No         | No         | No             | No                 |

*Note: Actual permissions may vary based on system configuration.*

## Summary

- User roles define access levels and permissions.
- Permissions include creating, viewing, updating, deleting, and managing system entities.
- Proper role assignment and permission management are essential for security and operational efficiency.
- Regular review and adherence to the principle of least privilege help maintain system integrity.

For detailed configuration, consult the system's role management interface or administrator documentation.