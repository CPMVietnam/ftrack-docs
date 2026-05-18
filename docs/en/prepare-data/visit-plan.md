---
title: Visit Plan
description: How to create and manage visit plans for field staff in Ftrack
---

# Visit Plan

How to schedule and assign visit plans to field staff. A Visit Plan defines which staff member visits which store, on which date, and which survey program to complete.

!!! warning "Prerequisites"
    Complete [Store List](store-list.md) and [Staff Accounts](staff-accounts.md) before creating a Visit Plan.

## Access the Feature

<!-- TODO: screenshot - Navigation to Visit Plan -->

**Step 1:** From the menu, go to **Prepare Data** → **Visit Plan**

## Create a New Visit Plan

<!-- TODO: screenshot - New Visit Plan creation form -->

**Step 2:** Click **Create New Visit Plan**

**Step 3:** Fill in the details:

| Field | Description |
|-------|-------------|
| Plan Name | Identifier for this visit plan |
| Program | Select the linked survey program |
| Staff | Select the staff member |
| Stores | Select one or more stores |
| Visit Date | Planned visit date |
| Frequency | One-time / Weekly / Monthly |

## Import Visit Plans in Bulk

<!-- TODO: screenshot - Import Visit Plan from Excel -->

**Step 2 (alternative):** Use the **Import** feature to create multiple Visit Plans at once from an Excel file

See [Settings → Import Visit](../settings/import-visit.md) for instructions.

## View and Manage Visit Plans

<!-- TODO: screenshot - Visit Plan list in the system -->

**Step 4:** After creation, Visit Plans appear in the list with these statuses:
- **Pending**: staff hasn't started yet
- **In Progress**: staff has checked in
- **Completed**: staff has checked out
- **Overdue**: not completed by the planned date

## Edit and Delete Visit Plans

<!-- TODO: screenshot - Edit / delete Visit Plan buttons -->

Click the **Edit** icon to update a plan, or **Delete** to cancel a plan that hasn't started yet.

!!! tip "Tip"
    Use filters by staff member, date, and region to manage large Visit Plan lists more efficiently.
