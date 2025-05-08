---
sidebar_position: 3
---

# Custom Scripting

This section explains how to utilize custom scripts within the TestWorthy platform to extend its core features and tailor its behavior to specific needs. It covers the process of integrating custom scripts, managing their lifecycle, and leveraging built-in APIs for customization.

## Step 1: Understanding the Custom Scripting Framework

TestWorthy supports custom scripting through a dedicated API that allows injecting JavaScript code to modify or extend default behaviors. These scripts can be used to:

- Add new test automation logic
- Customize UI components
- Implement additional validation rules
- Integrate with external systems

The scripting environment provides access to core objects such as `TestWorthy`, `TestCase`, `TestRun`, and UI elements.

## Step 2: Creating a Custom Script

To create a custom script:

1. Navigate to the **Custom Scripts** section in the admin panel.
2. Click **Add New Script**.
3. Provide a descriptive name and optional description.
4. Enter your JavaScript code in the editor.

**Example: Adding a custom validation before test execution**

```javascript
TestWorthy.on('beforeTestRun', function(testRun) {
  if (testRun.status === 'Failed') {
    alert('Test run cannot proceed because previous tests failed.');
    testRun.cancel();
  }
});
```

This script hooks into the `beforeTestRun` event, checks the status, and cancels the run if conditions are not met.

## Step 3: Managing Script Lifecycle

- **Enabling/Disabling Scripts:** Toggle the active state in the script list.
- **Editing Scripts:** Use the built-in editor to modify existing scripts.
- **Deleting Scripts:** Remove obsolete scripts to keep the environment clean.

**Tip:** Always test scripts in a staging environment before deploying to production.

## Step 4: Using APIs and Events

TestWorthy exposes several APIs and events for scripting:

- **Events:** `beforeTestRun`, `afterTestRun`, `onTestCaseStart`, `onTestCaseComplete`, etc.
- **Methods:** `TestWorthy.executeScript()`, `TestWorthy.getTestCases()`, `TestWorthy.log()`, etc.

**Example: Logging custom data during a test**

```javascript
TestWorthy.on('onTestCaseComplete', function(testCase) {
  TestWorthy.log('Test case completed: ' + testCase.name);
});
```

## Step 5: Best Practices

- Keep scripts modular and well-documented.
- Use unique event handlers to avoid conflicts.
- Handle exceptions gracefully to prevent script failures from affecting core functionality.
- Regularly review and update scripts to adapt to platform updates.

## Additional Tips

- Use the **Console** in the script editor for debugging.
- Leverage existing platform variables and objects for seamless integration.
- Store reusable functions in a shared namespace if supported.

## Summary

Custom scripting in TestWorthy empowers developers to extend and tailor the platform's capabilities efficiently. By creating, managing, and leveraging event hooks and APIs, you can implement complex automation, validation, and UI enhancements that align with your testing workflows.

Remember to test scripts thoroughly and document their purpose for maintainability.