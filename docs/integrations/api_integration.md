---
sidebar_position: 5
---

# API Integration

This section provides a comprehensive overview of how to utilize the TestWorthy API for integrating external systems, automating test management workflows, and extending platform capabilities. It covers authentication procedures, available API endpoints, and practical code examples to facilitate seamless integration.

## API Overview

The TestWorthy API offers a RESTful interface to interact programmatically with the test management platform. It enables external applications to create, read, update, and delete test cases, test runs, projects, and other entities. The API supports data retrieval for reporting, automation of test workflows, and integration with third-party tools such as CI/CD pipelines, issue trackers, and test automation frameworks.

## Authentication

To securely access the API, authentication is required via API tokens. Follow these steps:

1. **Obtain API Token:**
   - Log into your TestWorthy account.
   - Navigate to your user profile settings.
   - Generate a new API token or use an existing one.
   - Copy the token; it will be used in the `Authorization` header.

2. **Include Token in Requests:**
   - Use the `Authorization` header with the `Bearer` scheme:
   
```http
Authorization: Bearer YOUR_API_TOKEN
```

3. **Sample cURL Request:**

```bash
curl -H "Authorization: Bearer YOUR_API_TOKEN" \
     -H "Content-Type: application/json" \
     -X GET https://api.testworthy.com/v1/projects
```

**Important:** Keep your API token secure. Do not expose it in client-side code or public repositories.

## Endpoints

Below are the key API endpoints categorized by functionality. All endpoints follow the base URL:

```
https://api.testworthy.com/v1/
```

### Projects

- **GET /projects**: Retrieve list of projects.
- **POST /projects**: Create a new project.
- **GET /projects/`{id}`**: Get details of a specific project.
- **PUT /projects/`{id}`**: Update project information.
- **DELETE /projects/`{id}`**: Remove a project.

### Test Cases

- **GET /projects/`{projectId}`/cases**: List test cases within a project.
- **POST /projects/`{projectId}`/cases**: Create a new test case.
- **GET /cases/`{caseId}`**: Retrieve details of a test case.
- **PUT /cases/`{caseId}`**: Update test case details.
- **DELETE /cases/`{caseId}`**: Delete a test case.

### Test Runs

- **GET /projects/`{projectId}`/runs**: List test runs.
- **POST /projects/`{projectId}`/runs**: Create a new test run.
- **GET /runs/`{runId}`**: Get details of a test run.
- **PUT /runs/`{runId}`**: Update test run status or details.
- **DELETE /runs/`{runId}`**: Remove a test run.

### Test Results & Reports

- **GET /projects/`{projectId}`/results**: Fetch test results.
- **POST /results**: Submit test results.
- **GET /reports/`{reportId}`**: Download or view report.

### Users & Permissions

- **GET /users**: List users.
- **POST /users**: Create a user.
- **GET /users/`{userId}`**: Get user details.
- **PUT /users/`{userId}`**: Update user info.
- **DELETE /users/`{userId}`**: Remove user.

### External Integrations

- **GET /integrations/jira**: Fetch Jira configuration.
- **POST /integrations/jira**: Set Jira integration.
- **GET /integrations/testrail**: Fetch TestRail configuration.
- **POST /integrations/testrail**: Set TestRail integration.

## Examples

### 1. List all projects

```bash
curl -H "Authorization: Bearer YOUR_API_TOKEN" \
     https://api.testworthy.com/v1/projects
```

### 2. Create a new test case

```json
POST /projects/123/cases
Content-Type: application/json

{
  "title": "Login Functionality",
  "description": "Verify login with valid credentials",
  "steps": [
    "Navigate to login page",
    "Enter username and password",
    "Click login button"
  ],
  "expectedResult": "User is redirected to dashboard"
}
```

### 3. Submit test results for a run

```json
POST /results
Content-Type: application/json

{
  "runId": 456,
  "caseId": 789,
  "status": "Passed",
  "comments": "Test executed successfully"
}
```

### 4. Fetch Jira configuration

```bash
curl -H "Authorization: Bearer YOUR_API_TOKEN" \
     https://api.testworthy.com/v1/integrations/jira
```

### 5. Update project details

```json
PUT /projects/123
Content-Type: application/json

{
  "name": "Updated Project Name",
  "description": "Updated description for the project"
}
```

## Best Practices

- Always authenticate requests with your API token.
- Use HTTPS to secure data in transit.
- Handle API responses appropriately, checking for success status codes.
- Implement rate limiting and retries to handle API throttling.
- Store API tokens securely; avoid hardcoding in client-side code.
- Use pagination parameters (`page`, `limit`) for endpoints returning large datasets.

This guide provides the foundational knowledge to integrate with the TestWorthy API effectively. For detailed documentation on each endpoint, request/response schemas, and error handling, refer to the official API documentation portal or contact support.

---

*End of Documentation*