---
sidebar_position: 1
---

# Test Runs

This section provides detailed instructions on how to create, assign, and configure test runs within the testing platform. It guides developers through the process of setting up test executions, assigning specific tests to testers, and customizing test run options to suit project needs.

## Creating Test Runs

To set up a new test run for execution:

1. Navigate to the **Test Runs** section in the application dashboard.
2. Click on the **Create New Test Run** button, typically labeled as "Add Test Run" or similar.
3. Fill in the required details:
   - **Test Plan**: Select an existing test plan or create a new one.
   - **Project**: Choose the relevant project associated with the test run.
   - **Milestone** (optional): Assign a milestone if applicable.
   - **Test Suite**: Select the suite containing the tests to be executed.
   - **Test Cases**: Select specific test cases or opt to include all.
4. Configure additional options:
   - **Execution Mode**: Choose between manual or automated.
   - **Start Date / End Date**: Set the schedule for the test run.
   - **Environment**: Specify the testing environment (e.g., staging, production).
5. Click **Save** or **Create** to finalize the test run setup.

*Tip:* You can also clone existing test runs to quickly set up similar executions by selecting the clone option and modifying details as needed.

## Assigning Tests

Once a test run is created, assign individual tests or groups of tests to testers:

1. Open the specific test run from the list.
2. Navigate to the **Tests** tab within the test run details.
3. Select the tests you want to assign:
   - Use checkboxes to select multiple tests.
   - Or select all tests in a suite.
4. Click on **Assign Testers** or similar button.
5. Choose testers from the list:
   - Assign each test to a specific user.
   - Optionally, assign multiple testers to the same test for collaborative testing.
6. Confirm the assignment by clicking **Assign**.

*Note:* You can also assign tests in bulk by selecting multiple tests and assigning them simultaneously.

## Test Run Settings

Configure options to customize how the test run behaves:

1. Access the **Settings** or **Options** tab within the test run configuration.
2. Adjust the following parameters:
   - **Notification Preferences**: Enable or disable email notifications for testers upon assignment or completion.
   - **Test Execution Mode**:
     - **Sequential**: Tests are executed in order.
     - **Parallel**: Tests run simultaneously across testers.
   - **Retesting Options**: Define whether failed tests should be retested automatically.
   - **Reporting Settings**:
     - Enable detailed logging.
     - Set report generation frequency.
3. Save the settings to apply them to the current test run.

*Tip:* Use the **Test Run Templates** feature to reuse common configurations across multiple test runs, ensuring consistency and saving setup time.

---

By following these steps, developers can efficiently set up and manage test runs, assign tests to appropriate testers, and tailor execution options to fit project workflows. Proper configuration ensures smooth testing cycles and accurate tracking of test progress and results.