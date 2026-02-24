---
title: "Import Transactions in Create Source Document"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Import Transactions in Create Source Document."
long_description: "This document provides information about Import Transactions in Create Source Document from the DIS Keystone system."
---

## INTRODUCTION

This document describes the requirements and process of importing comma separated values files (.csv) containing general ledger transactions and posting them in Create Source Documents.

- The file to be imported must reside on the IBM iSeries Integrated File System.
- The feature requires a Keystone session environment since it uses the facility of the Keystone interface to communicate with its directories on the IFS.
- When the user takes the option to **Import Transactions**, the file to be imported must exist in the `\\Keystone\Keystone\Import\` directory path.
- The comma separated values file can be saved directly into this directory through PC applications such as Microsoft Excel if the PC has a mapped drive pointing to the `\\Keystone\Keystone` directory.
- The user must maintain the `\\Keystone\Keystone\Import` directory, deleting files that have been previously imported.

## Import File Layout

| Field | Title | Format | Description |
| :--- | :--- | :--- | :--- |
| 1 | ID | Text, 1 character | This field is optional. The ID field is typically used to document the source of the transaction, the id of the clerk who created/posted the transaction, or the subledger journal of the transaction. On most Keystone systems this field is not validated. |
| 2 | Transaction Date | MM/DD/YYYY | This field is optional. If no transaction date is supplied, the Keystone system will use the accounting batch date which is supplied by the user. If the transaction date is supplied it will be used instead of the accounting batch date. |
| 3 | Document | Text, 10 characters | This field is optional. The document field is typically used for invoice, purchase order, deposit, or check numbers. By default, the Keystone system will check that all transactions sharing the same document field balance with each other. |
| 4 | G/L Account | Text, 8 characters | This field is required. Keystone general ledger account numbers always begin with one character that designates the division (store or branch). Transactions with invalid general ledger account numbers will not be allowed to post. |
| 5 | Amount | Numeric, 9 characters plus decimal | The field is required. Debits should be submitted as positive numbers (without the leading negative sign) and credits should be submitted as negative numbers (with the leading negative sign.) The decimal point is optional. If the decimal point is not supplied then the value will be treated as a whole number. The maximum valid amount for each transaction is 9999999.99. |
| 6 | Description | Text, 12 characters | This field is optional. It serves as a memo line for each transaction. |
| 7 | Control Number | Text, 6 characters | This field may be required depending upon the G/L Account. It is typically used for the customer, vendor, or employee control number. If the G/L Account is not tied to a subledger or schedule, then this field is not controlled and is not required. However, if the G/L Account number is tied to a subledger or is scheduled, then this field is required and transactions with invalid entries will be rejected. Keystone users commonly refer to this as the "address number" field. |
| 8 | Due Date | MM/DD/YYYY | This field is optional in most cases. It is typically used for payable invoices to specify the date when payment is due or for equipment sales to specify when the equipment warranty will expire. |
| 9 | Discount | Numeric, 9 characters plus decimal | The rules and formatting for this field are the same as those for the Amount field. In most cases this field is optional. It is typically used for payable invoices to specify the discount amount that may be taken for early payment. |
| 10 | Unit Number | Text, 6 characters | This field may be required depending upon the G/L Account. It is used for the unit or stock number. If the G/L Account is not tied to a units subledger or schedule, then this field is not controlled and is not required. However, if the G/L Account number is tied to a units subledger or is scheduled by unit or serial number, then this field is required and transactions with invalid entries will be rejected. Common transactions that require the unit number are those posted to unit inventory, sales, and cost of sale accounts. Keystone users typically assign a unique unit number to each piece of equipment which is not the same as the manufacturer-assigned serial number. |

Each transaction line in the CSV file must end with one carriage return (0D) and one line feed (0A). These ASCII characters are typically included by most accounting CSV export programs.

## Sample Transaction Lines

```
ID,Transaction Date,Document,G/L Account,Amount,Description,Control Number,Due Date,Discount,Unit Number
P,1/6/2017,CK# 01434,A6400,800.00,Gross,Bert12,,,
P,1/6/2017,CK# 01435,A6400,-560.0,Net,Bert12,1/16/2017,200.00,DM0452,
```

## To Import a CSV File

1.  Select **Create Source Documents** (Accounting | Create Source Documents) and click **Continue**. The *G/L Transaction Date and Period* window appears.
    -   Enter the transaction date (e.g., `030917`).
    -   Enter the G/L posting month (e.g., `March`).
    -   Click **Continue**.

2.  The *Post Source Documents - Document Entry* screen opens. Click the **Recurrent Trans** button.

3.  The *Post Source Documents – Recurrent Transactions* screen opens. Click the **Add** button.

4.  The *Recurrent Transactions – Add New Group* screen opens. Click the **Import Transactions** button.

5.  The *Import Transactions* screen opens.
    -   Type the name of the file to import in the `Enter the name of the file to import` field (e.g., `NEWFILE.CSV`).
    -   Type the Group Name you would like to assign to the transactions in the `Enter a new Group Name to create with the imported transactions` field (e.g., `NEWGROUP`).
    -   **Note:**
        -   The full file name and extension must be entered. Only the file name should be entered and not the path name.
        -   The file name CANNOT contain any blanks and must exist in the `\\Keystone\Keystone\Import\` directory.
        -   The Group Name must be a new recurrent transaction group name.
    -   Click **OK**.

6.  Click **OK** to import the transactions. The *Post Source Documents – Recurrent Transactions* screen re-opens with the new group name listed in the table (e.g., `NEWGROUP`).

7.  Select the new group name and click the **Include** button. The imported transactions will be added to the current batch.

8.  The *Work/Due Date* screen opens. If you want to update the Work/Due date fields for each transaction, type the date in the field provided. Click **OK**.

9.  The *Post Source Documents – Recurrent Transactions* screen re-opens. Click the **Check for Errors** button.

10. The *Post Source Documents – Check for Errors* screen opens. Review the options and proceed.
    -   **Posting Month**: Confirms the posting month (e.g., `March`).
    -   **Editing Option**: Choose `Check Document Balancing` or `Do Not Check Document Balancing`.
    -   **Output Option**: Choose `Display Edit List` or `Print Edit List`.
    -   **Editing Division**: Set the division code.

11. Proceed with balancing the batch as you normally would, and post it to the general ledger.


title: "Import_Unit_Information_Keystone"
source: "Import_Unit_Information_Keystone.pdf"
tags: ["Keystone", "data import", "unit information", "inventory management", "CSV import", "Excel spreadsheet", "DIScorp"]
version: "1.0"
last_updated: "2024-05-21"
short_description: "This guide provides instructions on how to add or update unit information in the Keystone system by importing data from an Excel spreadsheet. It covers the required CSV file format, column specifications, and the import process within the Keystone application."
long_description: "This document details the process for importing unit information into the Keystone system using a specially formatted Excel spreadsheet. It eliminates the need for manual data entry across multiple screens by allowing bulk additions and updates. The guide outlines key system behaviors, such as the automatic creation of new make/model entries and the handling of duplicate short model names. It provides a comprehensive table specifying the required columns, headers, character limits, and data types for the import file. Mandatory fields like 'Unit Number', 'Make', and 'GL Account Number' are highlighted. The instructions walk the user through creating the Excel file, saving it as 'ImportUnits.csv', and placing it in the correct IFS directory. Finally, it explains how to initiate the import from the Keystone menu, what to expect during the process, and how to interpret the 'Units Not Imported' report that is generated."