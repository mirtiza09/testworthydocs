---
sidebar_position: 5
---

# Data Migration

This section provides detailed instructions on how to perform data migration tasks within the TestWorthy platform, including tools, techniques, and best practices for importing, transforming, and integrating data into the system. It covers the use of migration scripts, configuration files, and external utilities to ensure a smooth transition of data from legacy systems or external sources into the TestWorthy database.

## Overview of Data Migration in TestWorthy

Data migration involves transferring existing data—such as test cases, test runs, user information, project details, and configurations—from external sources or older systems into the TestWorthy environment. This process ensures data consistency, integrity, and compatibility with the current schema, enabling seamless continuation of testing activities and reporting.

Migration is typically performed using predefined scripts, configuration files, and migration tools that automate schema updates and data transformations. Proper planning and execution are critical to prevent data loss and ensure system stability.

## Prerequisites

- Access to the database server hosting TestWorthy.
- Migration scripts and configuration files tailored to your source data.
- Backup of the current database before migration.
- Necessary permissions to execute migration scripts and modify the database.
- Familiarity with SQL, Entity Framework migrations, or custom migration tools.

## Step-by-Step Migration Process

### 1. Prepare Your Environment

- Ensure the database server is accessible.
- Verify that the migration scripts are compatible with your database version.
- Backup the current database to prevent data loss.
- Review the migration scripts for any environment-specific configurations.

### 2. Configure Migration Settings

- Locate the migration configuration files, such as `appsettings.json` or custom migration configs.
- Set the connection string to point to your target database.
- Adjust migration parameters if needed, such as schema prefixes or data transformation options.

### 3. Import External Data Sources

- If migrating from external systems (e.g., Jira, TestRail), prepare data export files (CSV, JSON, XML).
- Use provided import utilities or custom scripts to load data into staging tables.
- Validate imported data for completeness and correctness.

### 4. Run Migration Scripts

- Execute migration scripts in the correct order, respecting dependencies.
- Use Entity Framework CLI commands or SQL scripts, e.g.:

```bash
dotnet ef database update
```

or run SQL scripts directly via SQL Server Management Studio or command-line tools.

- Monitor execution for errors or warnings.

### 5. Transform and Map Data

- Apply data transformations as specified in migration scripts:
  - Convert data types (e.g., date formats, IDs).
  - Map legacy values to new schema enums or lookup tables.
  - Populate new columns (e.g., `Priority`, `TestData`, `Designation`).

- Use custom scripts or ETL tools if complex transformations are needed.

### 6. Verify Data Integrity

- Run validation queries to ensure data has been migrated correctly.
- Check key tables such as `TestCases`, `TestRuns`, `Users`, `Projects`, and `Milestones`.
- Confirm foreign key relationships are intact and consistent.

### 7. Finalize Migration

- Remove or archive staging tables if used.
- Rebuild indexes and update statistics for optimal performance.
- Run application tests to verify data correctness and system stability.

### 8. Post-Migration Tasks

- Update configuration files with new environment-specific settings.
- Notify stakeholders of migration completion.
- Schedule regular backups and monitoring.

## Migration Scripts and Techniques

### Schema Alterations

Migration scripts handle schema updates such as:

- Adding new columns (e.g., `Designation`, `LastLoginAt`, `PasswordSalt`).
- Changing data types (e.g., from `int` to `DateTime`).
- Creating or dropping tables (e.g., `Payment`, `PaymentLog`).
- Updating foreign key constraints and indexes.

Example snippet for adding a column:

```sql
ALTER TABLE [dbo].[Users] ADD [Designation] NVARCHAR(100) NULL;
```

### Data Transformation

Scripts may include data conversion logic, such as:

- Converting date integers to `DATETIME`.
- Mapping legacy status codes to new enum values.
- Populating default roles and permissions.

### Seed Data

Migration scripts often seed essential data, such as:

- Default roles (`PM`, `QA`, `SE`).
- Designations and user types.
- Default configurations and settings.

### Handling Data Consistency

- Use transactions to ensure atomicity.
- Validate data after each migration step.
- Log errors and roll back if necessary.

## Best Practices

- Always perform a full backup before migration.
- Test migration scripts in a staging environment.
- Document each step and script execution.
- Validate data thoroughly post-migration.
- Communicate with stakeholders about migration timelines and impacts.
- Automate repetitive tasks using scripts or migration tools.

## Additional Resources

- Entity Framework Core Migration Commands:
  - `dotnet ef migrations add <Name>`
  - `dotnet ef database update`
- SQL Server Management Studio for manual script execution.
- ETL tools for complex data transformations.
- External utilities for data export/import (CSV, JSON, XML).

## Summary

Performing data migration in TestWorthy requires careful planning, preparation, and execution of scripts and tools to ensure data integrity and system stability. By following the outlined steps—preparing environment, configuring settings, importing data, executing scripts, transforming data, verifying integrity, and finalizing—you can successfully migrate data from legacy systems or external sources into the platform. Always adhere to best practices and validate thoroughly to maintain data quality and system reliability.