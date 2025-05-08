---
sidebar_position: 1
---

# Tenant Management

This section provides guidance on managing tenant-specific configurations, handling subscriptions and billing, and monitoring tenant usage within the system. It covers the key functionalities and steps to perform common administrative tasks related to tenant management.

## Managing Tenant Settings

Tenant settings allow administrators to configure tenant-specific parameters that tailor the environment to individual tenant needs. This includes setting organizational details, contact information, and feature toggles.

### How to update tenant settings

1. Log in as an administrator with tenant management privileges.
2. Navigate to the Tenant Management section in the admin dashboard.
3. Select the tenant you wish to configure.
4. Click on the "Edit" button to open the tenant settings form.
5. Update the desired fields:
   - Organization name
   - Country code
   - Web address
   - Phone number
   - Email addresses (e.g., contact, support)
   - Feature toggles (e.g., enable/disable specific features)
6. Save the changes by clicking "Update" or "Save".
7. Confirm that the tenant's configuration reflects the new settings.

### Important considerations
- Ensure all contact details are accurate for proper communication.
- Feature toggles should be tested in a staging environment before enabling in production.
- Changes may require tenant re-login or cache clearing to take effect.

## Subscription Management

Handling subscription details involves managing billing plans, payment methods, and subscription statuses. This ensures tenants are billed correctly and have access to appropriate features.

### How to manage subscriptions

1. Access the tenant's profile via the Tenant Management dashboard.
2. Navigate to the "Subscription" tab or section.
3. Review current subscription details:
   - Plan type (e.g., Basic, Premium)
   - Billing cycle (monthly, yearly)
   - Payment method (credit card, invoice)
   - Subscription status (active, canceled, pending)
4. To update billing details:
   - Click "Edit" or "Update Payment".
   - Enter new payment information.
   - Save changes.
5. To change the subscription plan:
   - Select the desired plan from available options.
   - Confirm the change.
   - The system may prompt for billing confirmation or additional verification.
6. To cancel or suspend a subscription:
   - Click "Cancel" or "Suspend".
   - Confirm the action.
   - Note that cancellation may take effect at the end of the billing cycle.

### Important considerations
- Billing changes may trigger proration or additional charges.
- Ensure payment methods are valid and up-to-date to avoid service interruptions.
- Review cancellation policies before terminating subscriptions.

## Tracking Usage Metrics

Monitoring tenant usage helps administrators understand resource consumption, feature utilization, and compliance with plan limits.

### How to monitor tenant usage

1. Access the Tenant Management section.
2. Select the tenant for which you want to view usage.
3. Navigate to the "Usage Monitoring" tab or section.
4. Review key metrics:
   - Number of active users
   - Test runs executed
   - Storage used for attachments and reports
   - API call counts
   - Feature usage statistics
5. Use available filters to analyze usage over specific periods or features.
6. Export usage reports if needed for auditing or billing purposes.

### Important considerations
- Regularly review usage to prevent exceeding plan limits.
- Set alerts or notifications for high usage thresholds.
- Use insights to optimize resource allocation or upgrade plans accordingly.

## Additional Tips

- Always back up tenant configurations before making bulk changes.
- Communicate planned updates or billing changes to tenants in advance.
- Use audit logs to track changes made to tenant settings and subscriptions.
- Leverage tenant usage data to inform future feature development and capacity planning.

This guide provides the essential steps and considerations for effective tenant management, ensuring smooth operation and customer satisfaction within the platform.