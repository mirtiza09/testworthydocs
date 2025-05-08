---
sidebar_position: 5
---

# Project Dashboard

This section provides detailed instructions on how to understand, access, and customize the project dashboard within the application. The project dashboard serves as the central hub for viewing project summaries, test statuses, milestones, recent activity, and other key metrics. Customization allows tailoring the dashboard to specific project needs, user roles, or organizational preferences.

## Accessing the Project Dashboard

1. **Login to the Application**
   - Navigate to the application's login page.
   - Enter your credentials and authenticate.
   
2. **Navigate to the Projects Section**
   - From the main menu, click on **Projects**.
   - Select the desired project from the list.

3. **Open the Project Dashboard**
   - Once inside a project, locate the **Dashboard** tab or button.
   - Click on **Dashboard** to load the project overview.

## Understanding the Default Dashboard Layout

The default dashboard typically includes:

- **Project Summary Cards**: Visual summaries of test cases, test runs, milestones, and recent activity.
- **Test Status Charts**: Pie or bar charts showing pass/fail/blocked ratios.
- **Milestone Progress**: Visual indicators of milestone completion.
- **Recent Activity Feed**: Log of recent test executions, updates, or comments.
- **Quick Links**: Shortcuts to test cases, test plans, or reports.

The layout is built using a combination of Bootstrap grid system, cards, and chart components (e.g., Chart.js).

## Customizing the Dashboard

### 1. Modifying Layout and Components

**Step-by-step:**

- **Locate the Dashboard Template**
  - The dashboard layout is defined in the HTML template files, often named `dashboard.html` or similar.
  - These files are located in the `views` or `templates` directory.

- **Edit the Layout**
  - Use your preferred code editor to open the template.
  - Adjust the Bootstrap grid classes (`col-*`, `row`) to change the layout.
  - Add or remove dashboard widgets (cards, charts, activity feeds).

- **Add Custom Widgets**
  - Create new Bootstrap cards or panels within the grid.
  - For example, to add a new test coverage widget:
    ```html
    <div class="col-md-4">
      <div class="card">
        <div class="card-header">Test Coverage</div>
        <div class="card-body">
          <canvas id="coverageChart"></canvas>
        </div>
      </div>
    </div>
    ```
  - Ensure to include corresponding JavaScript to populate the chart.

### 2. Updating Data Sources

- **Identify Data Endpoints**
  - Dashboard data is fetched via API calls or embedded in the page.
  - Look for AJAX calls in scripts like `dashboard.js` or similar.

- **Modify Data Retrieval**
  - To change the data displayed, update the API endpoints or data processing logic.
  - For example, in JavaScript:
    ```js
    $.ajax({
      url: '/api/projects/{projectId}/dashboard-data',
      method: 'GET',
      success: function(data) {
        // Update charts and widgets
      }
    });
    ```

- **Inject Custom Data**
  - For static data, embed JSON objects directly into the template.
  - For dynamic data, modify server-side controllers to supply additional metrics.

### 3. Customizing Charts and Visuals

- **Adjust Chart Types and Options**
  - Locate chart initialization code, often in `dashboard.js`.
  - Example:
    ```js
    var ctx = document.getElementById('statusChart').getContext('2d');
    var statusChart = new Chart(ctx, {
      type: 'pie',
      data: {...},
      options: {...}
    });
    ```
  - Change `type` to `bar`, `line`, or other supported types.
  - Modify `data` and `options` to customize appearance.

- **Add New Charts**
  - Create new `<canvas>` elements in the HTML.
  - Initialize charts with your data and options.

### 4. Styling and Theming

- **Update CSS**
  - Modify styles in `style.css` or theme-specific CSS files.
  - Change colors, fonts, spacing to match organizational branding.

- **Use Custom CSS Classes**
  - Add classes to dashboard components for targeted styling.
  - Example:
    ```html
    <div class="card custom-card-style">
      ...
    </div>
    ```
  - In CSS:
    ```css
    .custom-card-style {
      border-color: #4CAF50;
      background-color: #f0f4f8;
    }
    ```

### 5. Role-Based Customization

- **Control Widget Visibility**
  - Use server-side logic or JavaScript to show/hide components based on user roles.
  - Example:
    ```js
    if (userRole !== 'Admin') {
      $('#adminWidget').hide();
    }
    ```

- **Configure Permissions**
  - Adjust backend permissions to restrict or grant access to certain dashboard features.

### 6. Automating Dashboard Updates

- **Set Up Periodic Refresh**
  - Use JavaScript `setInterval` to refresh data periodically.
  - Example:
    ```js
    setInterval(function() {
      refreshDashboardData();
    }, 300000); // Refresh every 5 minutes
    ```

- **Implement Real-Time Updates**
  - Integrate WebSocket or SignalR for live updates if supported.

## Best Practices

- **Backup Templates Before Editing**
- **Use Version Control** for all layout and code changes.
- **Test Responsiveness** on different devices.
- **Maintain Consistent Styling** with theme variables.
- **Document Customizations** for future reference.

## Summary

Customizing the project dashboard involves editing layout templates, updating data sources, modifying visualizations, and adjusting styles. By understanding the existing structure and following the step-by-step instructions, you can tailor the dashboard to meet project-specific metrics, organizational branding, and user role requirements, enhancing the overall project management experience.