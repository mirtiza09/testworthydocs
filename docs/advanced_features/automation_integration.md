---
sidebar_position: 1
---

# Automation Integration

This section provides a detailed, step-by-step guide for integrating TestWorthy with popular test automation tools. The goal is to enable seamless communication between your test automation frameworks and TestWorthy, allowing for automated test result reporting, test case management, and synchronization.

## Step 1: Understand the Integration Architecture

Before starting, familiarize yourself with the architecture:

- TestWorthy exposes RESTful APIs for external tools to send test results, update test cases, and fetch test data.
- Your automation tools (e.g., Selenium, TestComplete, Postman) will act as clients, making HTTP requests to TestWorthy's API endpoints.
- Authentication is typically handled via API keys or OAuth tokens.

## Step 2: Obtain API Access Credentials

- Log into your TestWorthy dashboard.
- Navigate to **Settings > API Keys**.
- Generate a new API key with appropriate permissions (read/write).
- Save the API key securely; you'll need it for authentication.

## Step 3: Identify the API Endpoints

TestWorthy provides endpoints such as:

- **Create Test Run:** `POST /api/test-runs`
- **Update Test Result:** `PUT /api/test-results/{id}`
- **Fetch Test Cases:** `GET /api/test-cases`
- **Upload Attachments:** `POST /api/attachments`

Refer to the official API documentation for detailed request/response schemas.

## Step 4: Configure Your Test Automation Framework

Depending on your tool, implement the following:

### For Selenium (Java Example):

- Use an HTTP client library (e.g., Apache HttpClient).

```java
// Example: Sending test result to TestWorthy
HttpPost post = new HttpPost("https://testworthy.example.com/api/test-results");
post.setHeader("Authorization", "Bearer YOUR_API_KEY");
post.setHeader("Content-Type", "application/json");

String jsonPayload = "{ \"testCaseId\": 123, \"status\": \"Passed\", \"executionTime\": 45 }";
post.setEntity(new StringEntity(jsonPayload));

HttpResponse response = httpClient.execute(post);
```

### For Postman:

- Create a new request.
- Set method to POST or PUT.
- Enter the API URL.
- Add Authorization header: `Bearer YOUR_API_KEY`.
- Use raw JSON body with test results or other data.
- Save and automate via Postman Collection Runner or Newman.

### For Other Tools:

- Use the HTTP request feature or scripting capabilities.
- Ensure headers include the API key/token.
- Format payloads according to API specifications.

## Step 5: Automate Test Result Reporting

- Integrate API calls into your test scripts:
  - At the end of each test, send the result (pass/fail, logs, screenshots).
  - Use environment variables or config files to store API keys and URLs.
- Example pseudocode:

```python
def report_result(test_case_id, status, logs, attachments=None):
    payload = {
        "testCaseId": test_case_id,
        "status": status,
        "logs": logs,
        "attachments": attachments or []
    }
    headers = {
        "Authorization": "Bearer YOUR_API_KEY",
        "Content-Type": "application/json"
    }
    response = requests.post("https://testworthy.example.com/api/test-results", json=payload, headers=headers)
    return response.status_code
```

## Step 6: Upload Attachments and Screenshots

- Capture screenshots during tests.
- Use the attachment upload endpoint:

```python
files = {'file': open('screenshot.png', 'rb')}
headers = {"Authorization": "Bearer YOUR_API_KEY"}
response = requests.post("https://testworthy.example.com/api/attachments", files=files, headers=headers)
attachment_id = response.json().get('id')
```

- Link attachment IDs with test results.

## Step 7: Fetch Test Data and Test Cases

- Use GET endpoints to retrieve test case details or test configurations.
- Automate test data synchronization:

```python
response = requests.get("https://testworthy.example.com/api/test-cases", headers=headers)
test_cases = response.json()
# Use test_cases to parameterize your tests
```

## Step 8: Handle Authentication and Security

- Store API keys securely (environment variables, secret vaults).
- Rotate keys periodically.
- Use HTTPS for all API communications.
- Implement error handling for failed API calls.

## Step 9: Validate Integration

- Run your automation suite.
- Verify that test results are correctly reflected in TestWorthy.
- Check logs and API responses for errors.
- Confirm attachments and logs are uploaded properly.

## Step 10: Maintain and Extend Integration

- Automate API token renewal.
- Add support for custom test result fields.
- Integrate with CI/CD pipelines for continuous reporting.
- Monitor API usage and handle rate limits.

---

**Tip:**  
Always test your API integration in a sandbox environment before deploying to production to prevent data inconsistencies.

---

By following these steps, you can establish a robust integration between your test automation tools and TestWorthy, enabling efficient test management, reporting, and traceability.