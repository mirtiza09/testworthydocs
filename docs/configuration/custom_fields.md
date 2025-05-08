---
sidebar_position: 3
---

# Custom Fields

This section provides a detailed guide for developers on how to create, configure, and manage custom fields within the application. Custom fields allow extending existing entities with additional data points tailored to specific business needs, enabling flexible data modeling without altering core database schemas directly.

## Overview

Custom fields are user-defined data points that can be attached to various entities such as test cases, projects, milestones, or user profiles. They are managed through a dedicated configuration system that supports defining field types, labels, validation rules, and visibility.

## Accessing Custom Fields Management

1. **Navigate to the Configuration Section**  
   - Log into the application with appropriate permissions.  
   - From the main menu, go to **Settings** or **Configuration** (depending on your role).  
   - Locate the subsection labeled **Custom Fields**.

2. **Open the Custom Fields Management Page**  
   - Click on **Custom Fields** to open the management interface.  
   - You will see a list of existing custom fields, their associated entities, types, and statuses.

## Creating a New Custom Field

1. **Click on 'Add New' or 'Create Custom Field'**  
   - Usually represented by a button labeled **Add**, **New**, or a plus icon.

2. **Select the Entity**  
   - Choose the entity to which this custom field will be attached (e.g., Test Case, Project, Milestone).  
   - This determines where the custom field will appear and be available for data entry.

3. **Configure Basic Details**  
   - **Field Name/Label**: Enter a descriptive name for the custom field.  
   - **Field Type**: Select the data type (e.g., Text, Number, Date, Dropdown, Checkbox, Multiselect).  
   - **Description**: Optionally, provide a help text or description for users.

4. **Set Validation and Rules**  
   - Define whether the field is **Mandatory** or optional.  
   - Set validation rules such as max length, regex patterns, or value ranges.  
   - For dropdowns or multiselects, specify the list of options.

5. **Visibility and Access Control**  
   - Determine whether the field is **Visible** to all users or restricted based on roles or permissions.  
   - Configure read-only or editable states as needed.

6. **Save the Custom Field**  
   - Click **Save** or **Create** to persist the new custom field.  
   - The system will validate inputs and add the field to the configuration list.

## Managing Existing Custom Fields

- **Edit**:  
  - Select a custom field from the list.  
  - Click **Edit** to modify label, type, validation rules, or visibility.  
  - Save changes to update the configuration.

- **Deactivate/Enable**:  
  - Toggle the active status to temporarily disable or enable the field without deleting it.

- **Delete**:  
  - Remove a custom field if it is no longer needed.  
  - Be cautious: deletion may remove associated data.

## Applying Custom Fields to Entities

- Once created, custom fields automatically appear on the entity forms or views where they are configured.  
- For example, a custom field attached to **Test Cases** will be available when creating or editing test cases.

## Additional Tips

- **Bulk Operations**:  
  - Some systems support bulk editing or cloning of custom fields for multiple entities.

- **Field Templates**:  
  - Use predefined templates or copy existing custom fields to streamline setup.

- **Validation and Data Integrity**:  
  - Always define validation rules to ensure data consistency.

- **Localization**:  
  - If the application supports multiple languages, provide localized labels for custom fields.

## Dependencies and Interactions

- Custom fields are stored in dedicated configuration tables, often linked via foreign keys to the main entities.  
- They interact with data entry forms, validation routines, and reporting modules to include user-defined data points.

## Implementation Details

- Custom fields are managed via a configuration UI that updates the underlying data models.  
- The system dynamically renders input controls based on the field type during entity creation or editing.  
- Validation rules are enforced both client-side (via JavaScript) and server-side to ensure data integrity.

## Summary

Creating and managing custom fields involves selecting the target entity, defining field properties, validation rules, and visibility, then saving configurations. These fields extend the core data model flexibly, enabling tailored data collection without modifying the core schema. Proper management ensures data consistency, usability, and effective reporting.

---

*Tip:* Always review the list of custom fields periodically to remove obsolete or redundant entries, maintaining a clean configuration environment.