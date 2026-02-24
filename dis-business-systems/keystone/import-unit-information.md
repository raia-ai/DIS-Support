---
title: "Import Unit Information"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Import Unit Information."
long_description: "This document provides information about Import Unit Information from the DIS Keystone system."
---

## INTRODUCTION

You can now use an Excel spreadsheet to add new unit information in Keystone. Rather than having to add unit information on multiple screens, you can enter the information in one Excel Spreadsheet and import it into the system. This feature can also be used to update unit information (see table below to view fields that can be updated). Additional information:

- If the unit make/model that you import does not already exist in the system, it will automatically be added to the make/model table as the long make/model version.
- When new makes/models are imported, a short make/model version made up of the first 9 characters of the long version will also automatically be added. If the short model already exists, the last character(s) of the short model being added will be changed to a number to indicate that it is a unique model - `CK3510SEH` would be changed to `CK3510SE1`.
- A report titled **Units Not Imported** will automatically print after every Import attempt. If a Unit was not successfully imported, it will be listed on the report.

## INSTRUCTIONS

### Create Excel Spreadsheet

1. Create an Excel spreadsheet using the column headers listed in the table below. Do not use any characters other than letters and numbers or the import process will fail.

| Column | Header | Required | Maximum Character Length of Entry Field | Field Updatable |
| :--- | :--- | :--- | :--- | :--- |
| A | Unit Number | **Yes** | 6 (Alpha - Numeric) | No |
| B | Description | No | 12 (Alpha - Numeric) | Yes |
| C | Make | **Yes** | 10 (Alpha - Numeric) | Yes |
| D | Model | No | 16 (Alpha - Numeric) | Yes |
| E | Year (last two digits) | No | 2 (Alpha - Numeric) | Yes |
| F | Product Code | No | 2 (Alpha - Numeric) | Yes |
| G | Color | No | 5 (Alpha - Numeric) | Yes |
| H | Horsepower | No | 3 (Numeric) | If originally left blank |
| I | Serial Number | No | 17 (Alpha - Numeric) | No |
| J | Engine Serial Number | No | 12 (Alpha - Numeric) | Yes |
| K | Location | No | 2 (Alpha - Numeric) | Yes |
| L | Sold By | No | 6 (Alpha - Numeric) | No |
| M | In Date | No | 8 (MM/DD/YYYY - slashes required) | No |
| N | Dealer List | No | 9 (Numeric) | Yes |
| O | GL Account | **Yes** | 8 (Alpha - Numeric) | Yes |
| P | Long Description | No | 77 (Alpha - Numeric) | No |
| Q | Internal Specifications | No | 56 (Alpha - Numeric) | Yes |
| R - AP | External Specifications | No | 56 (Alpha - Numeric) | Yes |

2. Enter the information that you are adding/updating for each unit. You must provide a Unit Number, Make, and a valid GL Account Number. If you do not provide a valid GL Account Number, the unit information will not be imported.

   > **Warning:** If you exceed the maximum character length for an entry field, the import process may fail. Additionally, the characters exceeding the maximum length will not be imported. For instance, if you enter `2016` as the Year, `20` would be listed as the manufacture year.

3. Name the spreadsheet `ImportUnits` with the file extension `.csv` and save it as a CSV file to the IFS as `/Keystone/Import/ImportUnits.csv`.

   ```
   File name: ImportUnits.csv
   Save as type: CSV (Comma delimited) (*.csv)
   ```

### Import into Keystone

1. Select Import Units from the Keystone main menu (`Units | Import Units`). The Import Units screen opens.

   > **Please note the following:**
   >
   > **Import Units**
   >
   > This application allows you to Import Unit information from an Excel spreadsheet.
   >
   > You must save this spreadsheet in a ".csv" (comma separated values) file format, as file name: "ImportUnits.csv"
   >
   > The file must be copied to the IFS as: "/Keystone/Import/ImportUnits.csv"
   >
   > `Continue` `Exit`

2. Click **Continue**. The unit information is imported, the Units Not Imported report prints, and the Keystone main menu re-opens.
   
   **Note:** After the unit information has been successfully imported, it will be reflected on the Daily Maintenance Event Log.


title: "JCB_Communications_-_Keystone"
source: "JCB_Communications_-_Keystone.pdf"
tags: ["JCB", "Keystone", "Inventory Management", "Part File Transfer", "Vendor Maintenance", "Electronic Commerce", "DIS", "Dealership System", "Configuration"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "A brief guide on configuring and using JCB Communications within the DIS Keystone system. It covers setting up electronic commerce for part file transfers, managing vendor and customer maintenance, and sending/reviewing inventory data with JCB."
long_description: "This document provides detailed, step-by-step instructions for dealerships using the DIS Keystone system to set up and manage JCB Communications. It allows for the maintenance of consistent JCB parts inventory levels through automated part file transfers. The guide covers the initial configuration of electronic commerce communications, including entering dealer-specific information provided by JCB. It details how to configure vendor maintenance to specify which part classes to include in inventory files. The document explains the process of sending part locator refreshes, offering options for immediate submission, nightly backups, or daily file transfers. It also outlines how to review the status of submitted files, resend failed transmissions, and view files received from JCB. Finally, it provides instructions on customer maintenance, allowing users to exclude specific customer sales from transaction demand files sent to JCB. This ensures accurate suggested stock orders based on relevant sales history."