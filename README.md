# VA Billing Hub — Supabase-connected prototype

This version uses Supabase for cloud data and authentication instead of browser localStorage.

## Supabase project
- Project URL is configured in `index.html`.
- Browser-safe Supabase publishable key is configured in `index.html`.
- Never put a Supabase secret/service-role key in this file.

## Tables used
- organizations
- organization_members
- clients
- vas
- payment_profiles
- va_services
- recurring_schedules
- invoices
- invoice_items
- invoice_events

## Notes
- Sign in with the Supabase Auth user created for the project.
- The user must be a member of an organization. The current setup links the owner account to VA Billing Hub.
- RLS policies protect organization data.
- The app does not store card numbers.
- Approve & Send marks the invoice as sent and prepares it for emailing; actual email delivery is intentionally not wired yet.
- Recurring schedules are stored; automatic future invoice generation/reminders are the next backend feature.
