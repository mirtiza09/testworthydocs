---
sidebar_position: 3
---

# User Management

This section provides detailed instructions for managing users within the application, including roles, permissions, user creation, groups, authentication methods, and user profiles. Follow these step-by-step guides to perform common user management tasks effectively.

## User Roles and Permissions

Understanding user roles and their associated permissions is crucial for controlling access levels.

- **Roles**: Define user categories such as Admin, Project Manager (PM), QA, Developer, etc.
- **Permissions**: Specify what actions each role can perform, such as creating projects, editing test cases, or managing users.

**How to view and assign roles:**

1. Navigate to the **User Management** section.
2. Select **Roles** from the menu.
3. To create a new role:
   - Click **Add Role**.
   - Enter the role name and select permissions.
   - Save changes.
4. To edit an existing role:
   - Click on the role name.
   - Modify permissions as needed.
   - Save.

**Important interactions:**

- When creating or editing a user, assign the appropriate role to control access.
- Permissions are enforced throughout the application based on assigned roles.

---

## Creating and Managing Users

Adding, editing, and deactivating users ensures proper access control.

**Steps to add a new user:**

1. Go to **User Management** > **Users**.
2. Click **Add User**.
3. Fill in user details:
   - User Name
   - Email
   - Role (select from available roles)
   - Status (Active/Inactive)
4. Set a password or generate one.
5. Save the user.

**To edit an existing user:**

1. Locate the user in the user list.
2. Click **Edit**.
3. Update details as necessary:
   - Change role or status.
   - Update email or profile info.
4. Save changes.

**To deactivate a user:**

1. Find the user.
2. Click **Edit**.
3. Set **Status** to Inactive.
4. Save.

**Note:** Deactivated users cannot log in but their data remains for audit purposes.

---

## User Groups

Creating user groups simplifies permission management for multiple users.

**How to create and manage groups:**

1. Navigate to **User Groups**.
2. Click **Create Group**.
3. Name the group and assign users:
   - Select users from the list.
   - Assign specific roles or permissions to the group.
4. Save the group.

**Usage:**

- Assign permissions at the group level.
- Add or remove users from groups as needed.
- Apply group permissions to streamline access control.

---

## Authentication

### Password Management

- **Setting Password Policies:**
  1. Go to **Settings** > **Authentication**.
  2. Define password complexity rules:
     - Minimum length
     - Special character requirements
     - Expiration policies
  3. Save policies.

- **Managing User Passwords:**
  1. Locate user.
  2. Click **Reset Password**.
  3. Generate or set a new password.
  4. Notify the user.

### Single Sign-On (SSO)

- **Configuring SSO:**
  1. Navigate to **Settings** > **SSO Configuration**.
  2. Select identity provider (e.g., Azure AD, Google, Okta).
  3. Enter required credentials:
     - Client ID
     - Client Secret
     - Redirect URLs
  4. Save configuration.
  5. Enable SSO for user login.

**Usage:**

- Users authenticate via the configured identity provider.
- Admins can assign SSO to specific user groups.

### Active Directory Integration

- **Setup:**
  1. Go to **Settings** > **Active Directory**.
  2. Enter AD server URL and credentials.
  3. Map AD groups to application roles.
  4. Save settings.

- **Usage:**
  - Users authenticate using AD credentials.
  - Permissions are assigned based on AD group mappings.

---

## User Profiles

Managing user information and preferences enhances personalization.

**How to update user profiles:**

1. Click on your profile picture or name.
2. Select **Profile**.
3. Update details:
   - Name
   - Contact information
   - Preferences (e.g., notification settings, language)
4. Save changes.

**Additional profile management:**

- Users can upload profile pictures.
- Set notification preferences for test updates, comments, etc.

---

By following these instructions, administrators and authorized users can effectively manage user access, roles, and profiles, ensuring secure and organized operation of the platform.