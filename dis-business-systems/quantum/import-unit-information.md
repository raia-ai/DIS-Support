---
title: "Import Unit Information"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Import Unit Information."
long_description: "This document provides information about Import Unit Information from the DIS Quantum system."
---

## INTRODUCTION

You can now use an Excel spreadsheet to add new unit information in Quantum. Rather than having to add unit information on multiple screens, you can enter the information in one Excel Spreadsheet and import it into the system. This feature can also be used to update unit information (see table below to view fields that can be updated). Additional information:

- If the unit make/model that you import does not already exist in the system, it will automatically be added to the make/model table as the long make/model version.
- When new makes/models are imported, a short make/model version made up of the first 9 characters of the long version will also automatically be added. If the short model already exists, the last character(s) of the short model being added will be changed to a number to indicate that it is a unique model - `CK3510SEH` would be changed to `CK3510SE1`.
- A report titled **Units Not Imported** will automatically print after every Import attempt. If a Unit was not successfully imported, it will be listed on the report.
- If you do not designate an imported unit as New or Used, the unit will be designated as **New** by default.

## INSTRUCTIONS

### Create Excel Spreadsheet

1. Create an Excel spreadsheet using the column headers listed in the table below. Do not use any characters other than letters and numbers or the import process will fail.

| Column | Header | Required | Maximum Character Length of Entry Field | Field Updatable |
| :--- | :--- | :--- | :--- | :--- |
| A | Unit Number | Required | 6 (Alpha - Numeric) | No |
| B | Description | | 12 (Alpha - Numeric) | Yes |
| C | Make | Required | 10 (Alpha - Numeric) | Yes |
| D | Model | | 16 (Alpha - Numeric) | Yes |
| E | Year (last two digits) | | 2 (Alpha - Numeric) | Yes |
| F | Product Code | | 2 (Alpha - Numeric) | Yes |
| G | Color | | 5 (Alpha - Numeric) | Yes |
| H | Horsepower | | 3 (Numeric) | If originally left blank |
| I | Serial Number | | 17 (Alpha - Numeric) | No |
| J | Engine Serial Number | | 12 (Alpha - Numeric) | Yes |
| K | Location | | 2 (Alpha - Numeric) | Yes |
| L | Sold By | | 6 (Alpha - Numeric) | If Sales Rep is in system |
| M | In Date | | 8 (MM/DD/YYYY - slashes required) | No |
| N | Dealer List | | 9 (Numeric) | Yes |
| O | GL Account | Required | 8 (Alpha - Numeric) | Yes |
| P | Long Description | | 77 (Alpha - Numeric) | No |
| Q | Internal Specifications | | 56 (Alpha - Numeric) | Yes |
| R-AP | External Specifications | | 56 (Alpha - Numeric) | Yes |
| AQ | New or Used Designation | | 1 (Alpha - N = New, U = Used) | Yes |
| AR | Retail Price | | 9 (Numeric) | Yes |
| AS | Suggested List | | 9 (Numeric) | Yes |

2. Enter the information that you are adding/updating for each unit. You must provide a Unit Number, Make, and a valid GL Account Number. If you do not provide a valid GL Account Number, the unit information will not be imported.
    > **Warning:** If you exceed the maximum character length for an entry field, the import process may fail. Additionally, the characters exceeding the maximum length will not be imported. For instance, if you enter 2016 as the Year, 20 would be listed as the manufacture year.

3. Name the spreadsheet `ImportUnits` with the file extension `.csv` and save it as a CSV file to the IFS as `/Keystone/Import/ImportUnits.csv`.

    **File name:** `ImportUnits.csv`
    **Save as type:** `CSV (Comma delimited) (*.csv)`

## Import

1. Select Import Units from the Quantum main menu (*Units | Import Units*). The Import Units screen opens.

    > **Import Units**
    >
    > This application allows you to import Unit information from an Excel spreadsheet.
    > You must save this spreadsheet in a ".csv" (comma separated values) file format, as file name: "ImportUnits.csv"
    >
    > The file must be copied to the IFS as: "/Keystone/Import/ImportUnits.csv"
    >
    > `[Continue]`
    > `[Cancel and Return]`

2. Click **Continue**. The unit information is imported, the Units Not Imported report prints, and the Quantum main menu re-opens.
    > **Note:** After the unit information has been successfully imported, it will be reflected on the Daily Maintenance Event Log.