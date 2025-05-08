---
sidebar_position: 5
---

# User Profiles

This section provides a detailed guide for developers on how to implement, customize, and extend user profile management features within the application. It covers the core functionalities related to managing user data, preferences, and settings, along with the necessary interactions, UI components, and data handling techniques.

## Overview

User profiles are central to personalizing the user experience, controlling access, and storing user-specific configurations. The system supports CRUD operations for user data, preferences, roles, and settings, ensuring data integrity, security, and flexibility.

## Accessing User Profiles

1. **Retrieving User Data:**
   - Use the user repository interface (e.g., `IUsersRepository`) to fetch user data.
   - Example:
     ```csharp
     var user = await _usersRepository.GetByIdAsync(userId);
     ```
   - Ensure that user data includes core fields such as `UserName`, `Email`, `Designation`, `LastLoginAt`, and preferences.

2. **Displaying User Profiles:**
   - Create a user profile view model that encapsulates all necessary fields.
   - Bind the view model to the UI, typically a profile page or modal.
   - Example:
     ```csharp
     public class UserProfileViewModel
     {
         public string UserName { get; set; }
         public string Email { get; set; }
         public string Designation { get; set; }
         public DateTime LastLoginAt { get; set; }
         public UserPreferences Preferences { get; set; }
     }
     ```

## Managing User Information

1. **Updating User Details:**
   - Provide an API or controller endpoint to update user info.
   - Validate input data before saving.
   - Example:
     ```csharp
     public async Task<IActionResult> UpdateUserProfile(UserProfileUpdateModel model)
     {
         var user = await _usersRepository.GetByIdAsync(model.UserId);
         if (user == null) return NotFound();

         user.UserName = model.UserName;
         user.Email = model.Email;
         user.Designation = model.Designation;
         await _usersRepository.UpdateAsync(user);
         return Ok();
     }
     ```

2. **Changing Password:**
   - Implement a secure password update flow.
   - Validate current password, enforce password policies.
   - Example:
     ```csharp
     public async Task<IActionResult> ChangePassword(ChangePasswordModel model)
     {
         var user = await _usersRepository.GetByIdAsync(model.UserId);
         if (user == null || !VerifyPassword(user, model.CurrentPassword))
             return BadRequest("Invalid current password");

         user.PasswordHash = HashPassword(model.NewPassword);
         await _usersRepository.UpdateAsync(user);
         return Ok();
     }
     ```

## Managing User Preferences and Settings

1. **User Preferences Storage:**
   - Preferences are stored as a JSON object or dedicated table (e.g., `UserPreferences`).
   - Example:
     ```csharp
     public class UserPreferences
     {
         public bool ReceiveEmailNotifications { get; set; }
         public string Theme { get; set; }
         public string Language { get; set; }
         // Additional preferences
     }
     ```
   - Save preferences via API:
     ```csharp
     public async Task<IActionResult> SavePreferences(Guid userId, UserPreferences preferences)
     {
         var user = await _usersRepository.GetByIdAsync(userId);
         if (user == null) return NotFound();

         user.PreferencesJson = JsonConvert.SerializeObject(preferences);
         await _usersRepository.UpdateAsync(user);
         return Ok();
     }
     ```

2. **Loading Preferences:**
   - When loading the profile page, deserialize preferences:
     ```csharp
     var preferences = JsonConvert.DeserializeObject<UserPreferences>(user.PreferencesJson);
     ```

3. **Applying Preferences:**
   - Use preferences to customize UI elements, notifications, language, and themes.
   - Example:
     ```csharp
     if (preferences.Theme == "Dark")
     {
         ApplyDarkTheme();
     }
     ```

## Role and Access Management

- Users are associated with roles (e.g., Admin, User, Viewer).
- Role assignments are managed via the `Roles` and `UserRoles` tables.
- To update roles:
  ```csharp
  var userRoles = await _userRolesRepository.GetByUserIdAsync(userId);
  // Add or remove roles as needed
  ```

## Security Considerations

- Always validate user input.
- Hash passwords securely using algorithms like bcrypt or PBKDF2.
- Restrict access to profile management endpoints based on user permissions.
- Store sensitive data securely, encrypting preferences if necessary.

## UI Components

- Use modal dialogs or dedicated pages for profile editing.
- Include form validation and user feedback.
- Provide options for:
  - Updating personal info (name, email, designation)
  - Changing password
  - Setting preferences (language, theme, notifications)
  - Uploading profile images

## Example Workflow

1. **Viewing Profile:**
   - User navigates to `/Profile`.
   - System fetches user data and preferences.
   - UI displays current info and preferences.

2. **Editing Profile:**
   - User clicks "Edit".
   - Modal opens with form pre-filled.
   - User updates info/preferences.
   - On submit, API validates and saves data.
   - UI updates with new info.

3. **Changing Password:**
   - User clicks "Change Password".
   - Form prompts for current and new password.
   - Validation occurs server-side.
   - Password hash updated securely.

## Summary

Implementing user profile management involves:

- Creating secure APIs for CRUD operations.
- Managing preferences via JSON or dedicated tables.
- Providing intuitive UI components for editing.
- Ensuring role-based access control.
- Applying security best practices for sensitive data.

By following these guidelines, developers can build a robust, flexible, and user-friendly profile management system tailored to the application's needs.