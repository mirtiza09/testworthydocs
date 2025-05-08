---
sidebar_position: 1
---

# Testworthy 

This documentation provides detailed instructions and technical insights into the "Testworthy" project, focusing on its core functionalities, architecture, and how to build and extend the system. It covers the primary components, workflows, and configurations necessary for developers to understand and contribute effectively.

## Introduction

Testworthy is a comprehensive test management platform built with a layered architecture, supporting multi-tenant environments, extensive data models, and integrations. It leverages Entity Framework Core for data access, ASP.NET Core for web APIs, and a rich front-end built with Bootstrap, jQuery, Chart.js, and custom UI components. The system emphasizes modularity, scalability, and customization.

## Building the Project

### Prerequisites
- Install Node.js and npm
- Install .NET SDK (version compatible with the project, e.g., .NET Core 3.1 or later)
- Install Gulp CLI globally: `npm install -g gulp`
- Ensure SQL Server is available for database migrations
- Optional: Visual Studio or Visual Studio Code for development

### Steps
1. Clone the repository:
   ```
   git clone <repository-url>
   ```
2. Restore npm packages:
   ```
   npm install
   ```
3. Restore NuGet packages:
   ```
   dotnet restore
   ```
4. Build front-end assets:
   ```
   gulp build
   ```
5. Apply database migrations:
   ```
   dotnet ef database update
   ```
6. Run the application:
   ```
   dotnet run
   ```
7. Access the app at `https://localhost:5001` (or configured URL)

## Data Models and Schema

### Core Entities
- **Projects**: Manage test projects, including metadata, tenants, and configurations.
- **Test Cases**: Define individual test cases with properties like name, description, status, and associated test steps.
- **Test Runs**: Track execution instances, statuses, results, and logs.
- **Milestones & Schedules**: Organize test phases and deadlines.
- **Users & Roles**: Implement RBAC with multi-tenant support.
- **Attachments & Defects**: Attach files, bugs, and defect tracking.
- **Configurations & Settings**: Store system and project-specific configurations.

### Relationships
- Entities are linked via foreign keys, e.g., Test Cases belong to Projects, Test Runs relate to Test Cases, Users have roles, etc.
- Multi-tenant support is achieved via TenantId properties on key entities.

### Migration Scripts
- Use `dotnet ef migrations add <name>` to create new migrations.
- Migrations handle schema evolution, such as adding columns (`addPasswordInUser`), changing data types (`changeDateDataTypeInMigration`), and establishing foreign key constraints.
- Example: Adding a new `Designation` column to Users:
  ```
  migration.AddColumn("Users", "Designation", maxLength: 100, nullable: true);
  ```

## Data Access Layer

### Repositories
- Generic repositories (`Repository`, `AuditableRepository`) implement CRUD operations.
- Domain-specific repositories (`IProjectsRepository`, `ICasesRepository`, `ITestService`) provide tailored data access methods.
- Use dependency injection to inject repositories into services.

### Services
- Business logic resides in services (`IProjectService`, `ICaseService`, `ITestService`).
- Support bulk operations, complex queries, and data transformations.
- Example: Generating test reports or migrating data from external systems.

## Front-End Components

### Models
- Data transfer objects (DTOs) for API communication, e.g., `TestCaseDto`, `TestRunDto`.
- View models for UI binding, e.g., `AddCaseViewModel`, `EditTestRunModel`.

### UI Workflow
1. **Navigation**: Use the sidebar and top menu for project, suite, and test case navigation.
2. **Test Case Management**:
   - Create/Edit via forms bound to DTOs.
   - Attach files, add steps, and set statuses.
3. **Test Execution**:
   - Initiate test runs, monitor progress.
   - View logs, results, and defect links.
4. **Reporting**:
   - Generate PDFs, charts, and dashboards.
   - Export data as CSV or XLSX.

### Custom UI Components
- Use Bootstrap modals for dialogs (`ImageDialog`, `LinkDialog`).
- Use Chart.js for visualizations.
- Use jQuery for dynamic interactions (e.g., toggling test case details).

## Configuration & Environment

### appsettings.json
- Configure database connection strings.
- Set environment-specific variables (API keys, URLs).
- Enable/disable features like email, external integrations.

### Migrations & Seeding
- Seed default roles, designations, and initial data.
- Use `dotnet ef database update` to apply schema changes.

## External Integrations
- **Jira, TestRail, Azure DevOps**: Store API keys and URLs in configuration.
- **Stripe**: Manage payment plans and subscriptions.
- **Email**: SMTP settings for notifications.

## Extending the System

### Adding New Entities
- Define new models inheriting from base classes.
- Update DbContext with DbSet properties.
- Create migrations for schema updates.

### Customizing UI
- Modify Razor views or create new components.
- Extend existing models with additional properties.
- Use Bootstrap classes for styling consistency.

### Developing Plugins
- Implement new services or UI modules.
- Register via the `ModuleManager`.
- Use dependency injection for integration.

## Best Practices
- Use version control for all code changes.
- Write migration scripts for schema updates.
- Validate data inputs and handle exceptions gracefully.
- Maintain security best practices for user data and integrations.
- Regularly update dependencies and apply security patches.

## Summary

This overview provides the foundational knowledge for building, deploying, and extending the Testworthy platform. Developers should focus on understanding the data models, migration workflows, and front-end interactions. By leveraging the modular architecture, you can customize features, integrate new tools, and enhance the system's capabilities to meet evolving testing needs.

For detailed API references, code samples, and contribution guidelines, refer to the project's README and inline documentation.