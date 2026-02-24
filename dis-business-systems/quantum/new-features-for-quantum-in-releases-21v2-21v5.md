---
title: "New Features for Quantum in Releases 21v2 – 21v5"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about New Features for Quantum in Releases 21v2 – 21v5."
long_description: "This document provides information about New Features for Quantum in Releases 21v2 – 21v5 from the DIS Quantum system."
---

## INTRODUCTION

- The following information is on the primary new features in Quantum R21v2 - R21v5. If you are interested in purchasing Quantum or any other products, please call DIS at 1-800-426-8870.

## Resolution Upgrade

We have enhanced the resolution in Quantum to improve the layout of screen content. Objects and Fonts will adjust appropriately when re-sizing a browser window, remaining proportioned and legible in all window sizes.

## Customer 360

### Excel Export Button Available

The data associated with the Ranking option in Customer 360 as well as the Equipment, Parts, Documents and Rental graphs can now be exported to a spreadsheet with the click of a button.

The interface for this feature includes a table with an `>Excel` button.

| Sale Date | Division | Document | Purchase Order | Parts Total | Service Total | Units Total | Rentals Total |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 4/28/2016 | A | RN00271Y | | $0.00 | $0.00 | $0.00 | $4,500.00 |
| 4/28/2016 | A | RN00271Z | | $0.00 | $0.00 | $0.00 | $4,500.00 |
| 4/28/2016 | A | RN00352B | | $0.00 | $0.00 | $0.00 | $45.00 |
| 4/28/2016 | A | RN00352C | | $0.00 | $0.00 | $0.00 | $45.00 |
| 4/28/2016 | A | RN00352D | | $0.00 | $0.00 | $0.00 | $45.00 |
| 4/28/2016 | A | RN00352E | | $0.00 | $0.00 | $0.00 | $45.00 |
| 4/28/2016 | A | RN00363 | | $0.00 | $0.00 | $0.00 | $4,500.00 |
| 4/28/2016 | A | RN00363A | | $0.00 | $0.00 | $0.00 | $4,500.00 |

- Though the button specifies Excel, you can export the data into most spreadsheet software such as Google Docs.
- The exported data maintains the same format (column order, sort order, etc.) as the screen from which it is being exported. If the data column is hidden, it will not display in the spreadsheet.

## Management 360

### General Ledger Sales Summary Enhancement

There have been two significant changes to Management 360 regarding the General Ledger Sales Summary.

**UI Enhancements:**
- **Toggle Figures:** Buttons are available to toggle between monthly figures.
- **Graph Data:** The graph reflects MTD and YTD figures for the selected month.
- **Date Options:** A new option can be set to display the amount of transactions from a specific day (Dated) or the amount of transactions posted on a specific day (Posted).
- **Month Selection:** Figures are displayed for the current or previous month, with buttons to toggle between them.

1.  You can now toggle between the current Month-to-Date/Year-to-Date figures and those from the previous month. The graph and the MTD/YTD figures at the bottom of the screen will either reflect the G/L sales figures at the close of the previous month or the current figures.
2.  You can set an Opt to view sales amounts according to the day that they were posted or the day of the transaction. Contact DIS to set the Option.

## Units

### Import Unit Information

A new feature is available **for purchase** that allows you to use an Excel spreadsheet to add new unit information in Quantum. Rather than having to add unit information on multiple screens, you can enter the information in one Excel Spreadsheet and import it into the system.

This feature can also be used to update unit information. If the unit make/model that you import does not already exist in the system, it will automatically be added to the make/model table as the long make/model version.

Additionally, a new report titled **Units Not Imported** will automatically print after every Import attempt. If a Unit was not successfully imported, it will be listed on the report.

## Parts

### Bin Location Range Report

A second bin location has been added to the Bin Location Range Report and will display as shown below.

| Vendor Part # | Description | Class | Order Code | Min | Max | Qty On Hand | Qty Available | Bin |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| MAS 016779X | BALL TRA | T | C | | | | | A1 9 1 |
| MAS 151257M1 | SPACER COM | C | C | | | | | A1 9 2 |
| CAS AA10245 | 0 | C | | 31 | | 1- | | A10 |
| CAS AA2903 | FILTER | Y | C | | | 9 | 9- | A101-1 |
| ACN ACN114 | FRAMING NAILER | A | A | | | 50 | 49 | A1051 |
| CAS AA2094 | 0 | C | | 27 | | 14 | | A11 |
| CAS AF1600 | FILTER | 0 | C | | | 4 | 21- | A111 / B222 |
| ACN ACN125 | PRECISION PLIERS | A | A | | | 17 | 16 | A1156 |
| CAS AC187623 | ALTERNATOR | 0 | c | | | 13 | 8- | A12 |
| FOR ABNN12250B | RESTR | A | C | | | 3 | 3 | A12 |
| FOR APN582A | KIT | A | C | | | 24 | 6 | A15 |
| FOR B2NN12200A | ROTOR | A | C | | | 5 | 5 | A16 |
| FOR ABNN12250A | RESTR | A | C | | | 6 | 6 | A18 |
| CAS AA2900 | FILTER | Y | C | | | 10482 | 2 | A2 / A2XTRA |
| CAS A24314 | MUFFLER | 0 | C | | | 54 | 52 | A2 |
| CUM 127184 | WSH, PLA | S | A | | | 55 | 55 | A2 |
| MAS 022810X | SEAL TRA | T | C | | | | | A2 |

### CNH CSPS Interface

A new CSPS interface is now available that allows you to immediately access information on parts through communication with the manufacturer. You can also view availability and pricing, promotions, supersession information, notes about the part, and other general information. You can finalize and submit orders, view open and submitted orders, cancel orders, process returns (buybacks), and view the backorder inquiry. Click `here`, then (Quantum |CNH CSPS Training) for an overview of all that is possible with the new CSPS interface.

#### Create CNH Suggested Stock Order from Promotion IDs (New in 21v5)

A suggested stock order can now be generated based on promotion IDs up to 10 characters in length. Enter up to 4 promotion IDs to use when creating a suggested stock order.

1.  Select **Create Suggested Stock Order** from the main menu (`Parts | Stock Order | Create Stock Order | Create Suggested Stock Order`).
2.  The Create Suggested Stock Order screen opens. Provide the vendor code for CHN and any other desired information. Click **Enter**.
3.  The Create Suggested Stock Order screen opens.
4.  Click the **Select by CNH Codes** button.
5.  The **Select Parts by CNH Codes** screen opens allowing you to enter 4 promotion IDs up to 10 characters in length.
6.  Click **Verify Codes** to ensure the correct codes were entered and are valid.
7.  Click **Return with Selections**. The Create Suggested Stock Order screen opens. Click **OK**. A suggested stock order is generated listing parts based on the promotion IDs you provided.

## P.O.S.

### P.O.S. Document Ledger Priority Code (New in 21v5)

A priority code has been added to the document ledger to track changes.

### Flat Rate Adjustment Change

The method by which flat rate labor is adjusted has been changed to ensure technician data in the Service Recovery and Efficiency Report is more accurate. As a result, the last adjustment line on an invoice will now list billed hours as either .01 or .01- and the rate as 100 times the absolute value of the adjustment (see screenshot below).

**Example of Adjustment Line:**

| Qty | Vnd | Part Number | Description | Ext Price |
| :--- | :--- | :--- | :--- | :--- |
| TA | 0102 | LC | HAL | 6/08/17 .00 | .01- | .68- |

## P.O.S. & Service

### Spell Check Now in Work Order/Service Notes

Spell Check is now active when creating Work Order Notes in Invoicing or Service Notes in Service. When a spelling error is made in a note, the misspelled word will be underlined in red. Right-clicking on a misspelled word will allow you to select the correct spelling or add the word to your Quantum dictionary. This is available in screens such as "Point of Sale - Work with Notes" and "Inquire/Update Service Units - View/Update".

## Archiving

### EOM Financial Report (New in 21v5)

When Accounting End of Month is run for a division, an all department financial report is automatically generated and archived as an Accounting Report. If Combined End of month procedures are ran, then a report for each specified division is generated and archived.

Reports can be viewed through the **Work with Archived Documents** option in Archiving.

### Search Part Reports by Order Number (New in 21V5)

Recently archived parts reports can now be searched for by entering an associated order number.

- Select **Work with Archived Documents** in Archiving.
- Select **Parts Reports** and click **OK**.
- Click the **Search by Fields** button.
- Select the **Order Number** option and click **OK**.
- Enter the order number in the Search For field and click **OK**.

Contact DIS for assistance in enabling this search process in parts reports that were previously archived.

### Cancelled Order Report (New in 21v5)

A Cancelled Order Report is now automatically generated and archived whenever a stock order, return, or phase-out is cancelled. It is archived as a Parts Report and includes the order number, parts, and the user who completed the cancellation.


title: "New Features Guide for Quantum R22v1 - 22v3"
source: "New_Features_Guide_for_Quantum_R22v1_-_22v3.pdf"
tags: ["Quantum", "Software Release", "New Features", "22v3", "22v2", "22v1", "DIS", "Dealer Management System", "Technical Guide", "ERP"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "An overview of new features and enhancements in Quantum software releases R22v3, R22v2, and R22v1. This guide covers general UI updates, accounting improvements, P.O.S. functionality, manufacturer integrations, and 360 program upgrades."
long_description: "This comprehensive technical document details the primary new features introduced in the Quantum Dealer Management System across releases 22v1, 22v2, and 22v3. The guide is structured to provide users with a clear understanding of the updates, enhancing their ability to leverage the new functionalities. Key areas covered include the 'Quantum Refacing' project, which modernizes the user interface with symbolic icons and improved layouts. It outlines significant enhancements in Accounting, such as the GL Power Add and Copy feature and Receivable Payment Batch Recovery. The guide also introduces new Point of Sale (P.O.S.) tools like Service Scheduling and improved invoicing options. Furthermore, it details new and updated manufacturer interfaces for Kubota, CLAAS, JCB, and Polaris, streamlining parts and service management. Upgrades to the Sales 360 and Management 360 programs are also explained, offering new KPIs and improved data presentation. The document serves as an essential reference for dealerships to understand, purchase, and implement these new capabilities within their operations."