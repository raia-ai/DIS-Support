---
title: "Create Part List as Excel CSV File and Import"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Create Part List as Excel CSV File and Import."
long_description: "This document provides information about Create Part List as Excel CSV File and Import from the DIS Keystone system."
---

## INTRODUCTION
You can save an Excel spreadsheet as a .CSV file and then import it into the system using the Part List option. Only the part number and the quantity of the part need to be listed on the spreadsheet.

## INSTRUCTIONS

### Create and Save .CSV File
1.  Format the Excel spreadsheet as shown below, with the part number in the first column and quantity in the second column.

    | Part Number | Quantity |
    |-------------|----------|
    | A00922-2    | 2        |
    | A-5575565   | 13       |
    | A-800       | 22       |
    | A-803       | 15       |
    | A-80333     | 5        |
    | A-804       | 4        |
    | A804444     | 8        |
    | A-805       | 78       |
    | A805555     | 16       |
    | A-811       | 22       |

2.  Save the Excel spreadsheet as a .CSV file to your PC. In the "Save as type" dropdown, select `CSV (MS-DOS) (*.csv)`.

3.  Save the file to the `\\keystone\keystone\business_system_part_list_import` directory. After you have saved the .CSV file to the directory, you can import it into Parts Lists.

### Import .CSV File
1.  Select Part Lists (**Parts | Price Update/Part Lists | Part List**) from the Keystone main menu and click the **Import** button on the screen that opens.

    > **Note:** You can access this screen and import a Part List by clicking the **Part Lists** button on the Stock Return Correction, Stock Phase-out Correction, or Stock Order Correction screens.

2.  The **Part Lists – Select Part List File for Import** screen opens. Highlight the .CSV file that you created and click the **Select** button.

3.  The **Part Lists – Options** screen opens. Type the Code that you assigned to the vendor in the **Vendor** field, select whether you want to display and/or print the Part Lists Import Report, and click **Enter**.

4.  One of the following happens:
    *   If you selected to **display** the report, the report displays on the Display Spooled Files screen. Click **OK**. The **Part Lists – Sorted By** screen re-opens with the imported Part List displayed in the table.
    *   If you selected to **print** the report, the report automatically prints and the **Part Lists – Sorted By** screen re-opens with the imported Part List displayed in the table.


title: "Import Transactions in Create Source Documents"
source: "Import_Transactions_in_Create_Source_Documents.pdf"
tags: ["Keystone", "CSV Import", "General Ledger", "Source Documents", "Transactions", "Accounting", "Data Import", "IBM iSeries"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "This document provides instructions on importing comma-separated values (CSV) files containing general ledger transactions into the Keystone system's Create Source Documents module."
long_description: "This technical guide details the requirements and process for importing general ledger transactions from a CSV file into the Keystone software. It specifies the necessary system environment, including the file's location on the IBM iSeries Integrated File System (IFS) within the `\\Keystone\\Keystone\\Import\\` directory. The document provides a comprehensive layout for the CSV file, defining ten possible fields such as Transaction Date, Document, G/L Account, and Amount. For each field, it specifies the format, character limits, and whether it is optional or required, along with validation rules. The guide concludes with a detailed, step-by-step tutorial, complete with descriptions of the user interface screens, on how to execute the import process within the 'Create Source Documents' feature, from selecting the file to balancing and posting the transaction batch to the general ledger."