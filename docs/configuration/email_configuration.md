---
sidebar_position: 2
---

# Email Configuration

This section guides developers through setting up email notifications and templates within the application, enabling automated email communication for various events such as user registration, password resets, notifications, and system alerts.

## Accessing Email Settings

1. Locate the email configuration section in the admin or system settings panel of the application dashboard.
2. Navigate to the "Email Configuration" subsection, which typically includes SMTP server details, email templates, and notification preferences.

## Setting Up SMTP Server

1. Enter the SMTP server address provided by your email service provider (e.g., smtp.gmail.com, smtp.sendgrid.net).
2. Specify the SMTP port number (commonly 587 for TLS, 465 for SSL).
3. Choose the security protocol (SSL/TLS) as required.
4. Provide authentication credentials:
   - Enter the email address that will send notifications.
   - Enter the corresponding password or app-specific password.
5. Save the SMTP settings.

*Tip:* Ensure that the SMTP credentials are valid and that the email account has permissions enabled for SMTP access.

## Configuring Email Templates

1. Access the "Templates" or "Email Templates" section within Email Configuration.
2. For each notification type (e.g., Welcome Email, Password Reset, Notification Alert):
   - Select the template to edit or create a new one.
   - Use the provided template editor to customize the email content.
   - Incorporate placeholders or variables (e.g., `{{UserName}}`, `{{ResetLink}}`) to dynamically insert user-specific data.
3. Preview the email template to verify layout and content.
4. Save each template after editing.

*Example:*  
```html
<h1>Welcome, `{{UserName}}`!</h1>
<p>Thank you for registering. Please verify your email by clicking <a href="{{VerificationLink}}">here</a>.</p>
```

## Enabling Email Notifications

1. Toggle the "Enable Email Notifications" switch to activate email sending.
2. Set notification preferences:
   - Choose which events trigger emails (e.g., user registration, password reset, test completion).
   - Define recipient groups or individual email addresses.
3. Save the notification settings.

## Testing Email Setup

1. Use the "Send Test Email" feature, if available.
2. Enter a recipient email address.
3. Send a test message to verify SMTP configuration and template rendering.
4. Check the recipient inbox for delivery and content correctness.

## Additional Tips

- Ensure your SMTP server allows relaying from your application's IP address.
- Use verified email addresses to prevent spam filtering.
- For production environments, consider using dedicated email services like SendGrid, Amazon SES, or Mailgun for higher deliverability.

## Summary

By correctly configuring SMTP settings and customizing email templates, the system will automatically send notifications for various events, improving communication and user engagement. Always test email delivery after setup to confirm proper operation.

---

*Note:* The exact UI labels and navigation steps may vary depending on your application's version and customization. Refer to the application's documentation or contact support if options are not visible.