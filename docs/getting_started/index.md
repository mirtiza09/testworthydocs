---
sidebar_position: 2
---

# Getting Started

This section provides a comprehensive guide to setting up, configuring, and beginning to use the TestWorthy platform, a robust test management system. It covers system requirements, installation procedures, initial setup steps, and key terminology to help developers quickly become productive.

## Introduction

TestWorthy is a full-featured test management platform designed to organize, execute, and track testing activities across multiple projects and teams. It offers test case management, execution tracking, reporting, and integrations with external tools, all built on a scalable, multi-tenant architecture.

## Key Features

- **Test Case Management:** Create, organize, and version test cases within projects and suites.
- **Test Execution:** Run tests, record results, and track progress.
- **Reporting & Analytics:** Generate detailed reports on test cycles, milestones, and project health.
- **Integrations:** Connect with Jira, TestRail, Azure DevOps, and other external tools.
- **User & Role Management:** Fine-grained access control with roles, permissions, and tenant segregation.
- **Content Management:** Support for blogs, documentation, and content publishing.
- **Multi-Tenant Support:** Isolated data for different organizations or departments.

## System Requirements

- **Hardware:**
  - Minimum 4 CPU cores
  - 8 GB RAM
  - 100 GB disk space (depending on data volume)
- **Software:**
  - Windows Server or Linux (Ubuntu 20.04+ recommended)
  - .NET Core 3.1 or later
  - SQL Server 2016+ or PostgreSQL
  - IIS or Linux-based web server (e.g., Nginx)
- **Additional:**
  - Browser: Chrome, Edge, Firefox, or Safari (latest versions)
  - Email server for notifications

## Installation Guide

### Cloud Deployment

1. **Provision Infrastructure:**
   - Set up a VM or cloud service (Azure, AWS, GCP) with the above hardware/software specs.
2. **Configure Database:**
   - Create a new SQL Server or PostgreSQL database.
3. **Deploy Application:**
   - Download the latest release package from the official repository or build from source.
   - Publish the application to your web server or cloud platform.
4. **Configure Environment:**
   - Set environment variables or appsettings.json with database connection strings, SMTP settings, and external API keys.
5. **Run Migrations:**
   - Execute database migrations to set up schema (`dotnet ef database update`).
6. **Start Services:**
   - Launch the application, configure IIS or reverse proxy as needed.
7. **Access Platform:**
   - Navigate to your deployment URL, complete initial setup via web UI.

### On-Premises Installation

1. **Prepare Server:**
   - Install Windows Server or Linux OS.
2. **Install Dependencies:**
   - .NET Core runtime
   - SQL Server or PostgreSQL
   - Web server (IIS/Nginx)
3. **Deploy Application:**
   - Download or clone the codebase.
   - Build and publish the application.
4. **Configure Database & Environment:**
   - Run migrations.
   - Update configuration files with database and SMTP details.
5. **Start Application:**
   - Set up as a Windows Service or systemd service.
6. **Access Platform:**
   - Open browser and navigate to the configured URL.

## Quick Start Guide

1. **Login:**
   - Use the default admin account or create a new tenant during initial setup.
2. **Create Projects:**
   - Navigate to Projects > Create New.
3. **Add Test Suites & Cases:**
   - Within a project, define test suites and add test cases.
4. **Execute Tests:**
   - Run test cases manually or via automated test runs.
5. **Generate Reports:**
   - Use the Reports module to review test results and progress.
6. **Invite Users:**
   - Assign roles and permissions to team members.
7. **Configure Integrations:**
   - Set up Jira, TestRail, or other tools under Settings.

## Glossary

- **Tenant:** An isolated organizational unit within the platform.
- **Test Case:** A documented set of steps to verify a feature.
- **Test Run:** An execution instance of one or more test cases.
- **Milestone:** A significant point or deadline in the testing schedule.
- **Suite:** A collection of related test cases.
- **Role:** Defines permissions and access levels for users.
- **Integration:** Connection with external tools like Jira or TestRail.
- **Dashboard:** Overview page showing project health and activity summaries.

---

This guide aims to help developers quickly set up and start using TestWorthy. For detailed configuration, API integration, and customization, refer to the official documentation or contact support.

