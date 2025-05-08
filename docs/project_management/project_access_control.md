---
sidebar_position: 3
---

# Project Access Control

This section explains how to control user access and permissions for projects within the system. It covers the steps to assign roles, set permissions, and manage project-level access to ensure proper security and collaboration.

## Step 1: Understand the Role and Permission Structure

- The system uses roles (e.g., Admin, User, Viewer) to define what actions a user can perform.
- Permissions are assigned at the project level, determining whether a user can view, edit, or administer a project.
- Roles are linked to users via a project access control list, which specifies the level of access per user per project.

## Step 2: Assign Users to Projects

- Navigate to the **Project Management** section in the admin dashboard.
- Select the specific project you want to manage access for.
- Click on **Manage Access** or **Project Access Control**.
- Add users by searching for their usernames or email addresses.
- For each user, assign a role (e.g., Viewer, Contributor, Administrator).

## Step 3: Configure Role-Based Permissions

- After adding users, configure their permissions:
  - **Viewer**: Can only view project details and test cases.
  - **Contributor**: Can modify test cases, create test runs, but cannot delete the project.
  - **Administrator**: Full access, including editing project settings and managing access control.

- To modify permissions:
  - Locate the user in the project access list.
  - Change their role using the dropdown menu.
  - Save changes to apply the new permissions.

## Step 4: Manage Project Access Control List (ACL)

- Use the **Access Control** interface to:
  - Remove users from the project.
  - Change their roles.
  - View current access levels for all users.

- Ensure that only authorized users have access to sensitive projects:
  - Remove users who no longer need access.
  - Assign higher roles only to trusted team members.

## Step 5: Verify Access Settings

- Test user access by logging in as different users:
  - Confirm that users can only perform actions permitted by their roles.
  - Check that restricted users cannot access admin settings or delete projects.

## Additional Tips

- Use the **Bulk Assign** feature to assign roles to multiple users at once.
- Regularly review project access lists to maintain security.
- For sensitive projects, restrict access to only essential team members.

## Summary

Managing project access control involves assigning roles to users, configuring permissions, and regularly reviewing access lists. By following these steps, you ensure that users have appropriate permissions, maintaining project security and integrity.

---

**Tip:** Always verify access rights after making changes to prevent unauthorized modifications or data leaks.