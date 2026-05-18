---
title: Store List
description: How to import your list of stores and retail points into Ftrack
---

# Store List

How to import your list of stores (retail points, distributors, supermarkets, etc.) into Ftrack to support Visit Plans and survey programs.

## Access the Feature

<!-- TODO: screenshot - Navigation to Store List -->

**Step 1:** From the menu, go to **Prepare Data** → **Store List**

## Download the Template

<!-- TODO: screenshot - Download template button -->

**Step 2:** Click **Download Template** to get the Excel file

!!! info "Note"
    Always use the latest template downloaded from the system. Do not use old templates or custom files.

## Fill In the Data

<!-- TODO: screenshot - Sample filled-in Excel template -->

**Step 3:** Open the template and fill in each store:

| Column | Description | Required |
|--------|-------------|----------|
| Store Code | Unique identifier | Yes |
| Store Name | Store/outlet name | Yes |
| Address | Full address | Yes |
| Province/City | <!-- TODO: verify required columns --> | Yes |
| Region | Geographic zone | No |
| Latitude / Longitude | GPS coordinates | No |

!!! warning "Note"
    - Do not delete or modify the header row
    - Store codes must be unique across the entire file
    - Avoid special characters in data cells

## Upload the File

<!-- TODO: screenshot - File upload interface -->

**Step 4:** Go back to the system, click **Choose File**, and upload the completed Excel file

**Step 5:** Click **Import** to start the import process

## Review Import Results

<!-- TODO: screenshot - Import results screen (success/error counts) -->

**Step 6:** Review the results:
- **Success**: number of records added
- **Errors**: list of failed rows and reasons

!!! tip "Tip"
    If there are errors, download the error log, fix the issues in the template, and re-import only the failed rows.

## View Imported Stores

<!-- TODO: screenshot - Store list in the system after import -->

After a successful import, stores appear in the system and can be selected when creating a Visit Plan.
