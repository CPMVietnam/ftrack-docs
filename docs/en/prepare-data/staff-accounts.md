---
title: Staff Accounts
description: How to create and manage field staff accounts in Ftrack
---

# Staff Accounts

How to create login accounts for field staff so they can use the Ftrack Mobile app.

## Access the Feature

<!-- TODO: screenshot - Navigation to Staff Accounts -->

**Step 1:** From the menu, go to **Prepare Data** → **Staff Accounts**

## Create a Single Account

<!-- TODO: screenshot - New account creation form -->

**Step 2:** Click **Add New** to create an account for one staff member

**Step 3:** Fill in the details:

| Field | Description | Required |
|-------|-------------|----------|
| Full Name | Staff member's full name | Yes |
| Email | Used for login | Yes |
| Phone Number | <!-- TODO: verify --> | No |
| Role | Staff / Supervisor / Admin | Yes |
| Territory | <!-- TODO: verify --> | No |

**Step 4:** Click **Save** — the system will send an activation email to the staff member

## Import Accounts in Bulk

<!-- TODO: screenshot - Template download for bulk import -->

**Step 2 (alternative):** Click **Download Template** → Fill in the staff list → **Upload & Import**

!!! tip "Tip"
    Use bulk import at the start of a project when creating many accounts at once.

## Roles and Permissions

<!-- TODO: screenshot - Role/permission settings screen -->

<!-- TODO: verify - detailed description of roles: Admin, Supervisor, Field Staff -->

Ftrack supports these roles:
- **Admin**: full system access
- **Supervisor**: view reports, manage staff in their territory
- **Field Staff**: use mobile app to complete visits

## Update and Deactivate Accounts

<!-- TODO: screenshot - Edit / deactivate account buttons -->

To **edit**: click the edit icon on the account row

To **deactivate**: click the lock icon — the staff member cannot log in, but historical data is preserved
