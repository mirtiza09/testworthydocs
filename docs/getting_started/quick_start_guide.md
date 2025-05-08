---
sidebar_position: 5
---

# Quick Start Guide

This guide provides step-by-step instructions for setting up and running TestWorthy, a test management platform built with a modular architecture supporting multiple features such as project management, test case tracking, reporting, and integrations. Follow these instructions to get your environment up and running efficiently.

## Prerequisites

- Ensure you have Node.js and npm installed on your machine.
- Install a code editor (e.g., Visual Studio Code).
- Set up a database server (e.g., SQL Server, MySQL) compatible with your environment.
- Install Git for version control and cloning repositories.
- Optional: Docker if you prefer containerized deployment.

## Step 1: Clone the Repository

1. Open your terminal or command prompt.
2. Run the following command to clone the project repository:

```bash
git clone https://github.com/yourorganization/testworthy.git
```

3. Navigate into the project directory:

```bash
cd testworthy
```

## Step 2: Install Dependencies

1. Install project dependencies using npm:

```bash
npm install
```

*This will install all required packages, including Bootstrap, jQuery, Chart.js, and build tools.*

## Step 3: Configure Environment Settings

1. Locate the configuration files, typically in `config/` or root directory.
2. Set up your database connection string in `appsettings.json` or environment variables:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=YOUR_SERVER;Database=TestWorthyDB;User Id=YOUR_USER;Password=YOUR_PASSWORD;"
  }
}
```

3. Configure third-party API keys if needed (e.g., Google Analytics, external integrations).

## Step 4: Set Up the Database

1. Run database migrations or scripts:

- If using Entity Framework Core, run:

```bash
dotnet ef database update
```

- Or execute SQL scripts provided in the `sql/` folder to create schema and seed data.

2. Verify the database is correctly configured and accessible.

## Step 5: Build the Front-End Assets

1. Run Gulp tasks to compile SASS, minify scripts, and prepare assets:

```bash
gulp build
```

2. For development with live reload, run:

```bash
gulp watch
```

*This will watch source files for changes and automatically reload your local server.*

## Step 6: Run the Application

1. Start the server:

```bash
npm start
```

*This will launch the application on `http://localhost:3000` or the configured port.*

2. Open your browser and navigate to the URL.

## Step 7: Access the Application

- Register a new tenant or log in with existing credentials.
- Follow the onboarding steps to set up projects, test cases, and milestones.
- Use the UI components to manage test plans, execute tests, generate reports, and view dashboards.

## Additional Tips

- **Import Sample Data:** Use provided JSON files (e.g., rolesreadonlyviews.json) to seed roles and access controls.
- **Configure Email & External Services:** Update SMTP settings and API keys in configuration files for email notifications and integrations.
- **Customize Themes:** Modify CSS files (e.g., style.css) or apply themes to match your branding.
- **Extend Functionality:** Add new modules or plugins following the existing architecture.

## Troubleshooting

- **Database Connection Errors:** Verify connection strings and database server status.
- **Missing Dependencies:** Run `npm install` again or delete `node_modules` and reinstall.
- **Build Failures:** Check Gulp logs for errors; ensure Gulp is installed globally (`npm install -g gulp`).

## Summary

By following these steps, you will have a fully functional TestWorthy environment ready for managing your testing workflows. Leverage the modular architecture to customize and extend features as needed, and consult the documentation for advanced configurations and integrations.