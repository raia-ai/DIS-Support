---
title: "New Features for Keystone in Releases 21v2 - 21v5"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about New Features for Keystone in Releases 21v2 - 21v5."
long_description: "This document provides information about New Features for Keystone in Releases 21v2 - 21v5 from the DIS Keystone system."
---

## INTRODUCTION
The following information is on the primary new features in R21v2 – R21v5. Complete step-by-step instructions for all new features will be added to Keystone-Online-Help, as soon as they are available.

If you are interested in purchasing Keystone or any of the other products, please call DIS at 1-800-426-8870.

## Units

### Import Unit Information
A new feature is available for purchase that allows you to use an Excel spreadsheet to add new unit information in Keystone. Rather than having to add unit information on multiple screens, you can enter the information in one Excel Spreadsheet and import it into the system. This feature can also be used to update unit information. If the unit make/model that you import does not already exist in the system, it will automatically be added to the make/model table as the long make/model version.

Additionally, a new report titled Units Not Imported will automatically print after every Import attempt. If a Unit was not successfully imported, it will be listed on the report.

## Parts

### Bin Location Range Report
A second bin location has been added to the Bin Location Range Report and will display as shown below.

[Image: Screenshot of the 'Bin Location Range Report' showing a table with part details. Red boxes highlight the 'Bin' column, which now displays primary and secondary bin locations (e.g., A111 /B222 and A2 /A2XTRA).]

| Vendor Part # | Description | Class | Order Code | Min | Max | Qty On Hand | Qty Available | Bin |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| MAS 016779X | BALL TRA | C | A | | 1 | | | A1 9 1 |
| MAS 151257M1 | SPACER COM | C | C | | | 3 | 1- | A1 9 2 |
| CAS AA10245 | | C | | | | 27 | 14 | A10 |
| CAS AA2903 | FILTER | C | Y | | | 9 | 9- | A101-1 |
| ACN ACN114 | FRAMING NAILER | A | A | | | 50 | 49 | A1051 |
| CAS AA2094 | | C | | | | 4 | 21- | A11 |
| CAS AF1600 | FILTER | C | | | | | | A111 /B222 |
| ACN ACN125 | PRECISION PLIERS | A | A | | | 17 | 16 | A1156 |
| CAS AC187623 | ALTERNATOR | C | | | | 13 | 8- | A12 |
| FOR ABNN12250B | RESTR | C | A | | | 3 | 3 | A12 |
| FOR APN582A | KIT | C | A | | | 24 | 6 | A15 |
| FOR B2NN12200A | ROTOR | C | A | | | 5 | 5 | A16 |
| FOR ABNN12250A | RESTR | C | A | | | 6 | 6 | A18 |
| CAS AA2900 | FILTER | C | Y | | | 10482 | 2 | A2 /A2XTRA |
| CAS A24314 | MUFFLER | C | | | | 54 | 52 | A2 |
| CUM 127184 | WSH, PLA | A | S | | | 55 | 55 | A2 |
| MAS 022810X | SEAL TRA | C | T | | | | | A2 |

## CNH CSPS Interface

> **LINK**
> A new CSPS interface is now available that allows you to immediately access information on parts through communication with the manufacturer. You can also view availability and pricing, promotions, supersession information, notes about the part, and other general information. You can finalize and submit orders, view open and submitted orders, cancel orders, process returns (buybacks), and view the backorder inquiry.
> Click here, then scroll to Parts and click **CSPS Interface** for an overview of all that is possible with the new CSPS interface.

### Create CNH Suggested Stock Order from Promotion IDs (New in 21v5)
A suggested stock order can now be generated based on promotion IDs up to 10 characters in length. Enter up to 4 promotion IDs to use when creating a suggested stock order.

- Select **Create Suggested Stock Order** from the main menu (Parts | Stock Order | Create Stock Order | Create Suggested Stock Order).

- The Create Suggested Stock Order screen opens. Provide the vendor code for CHN and any other desired information. Click **Enter**.

- The Create Suggested Stock Order screen opens.

    [Image: Screenshot of the 'Create Suggested Stock Order' screen with various options. The 'Select by CNH Codes' button is highlighted.]

- Click the **Select by CNH Codes** button. The Select Parts by CNH Codes screen opens allowing you to enter 4 promotion IDs up to 10 characters in length.

    [Image: Screenshot of the 'Select Parts by CNH Codes' screen, showing input fields for 'Product Line Codes' and 'Promo IDs'. The 'Promo IDs' section is highlighted.]

- Click **Verify Codes** to ensure the correct codes were entered and are valid.

- Click **Return with Selections**. The Create Suggested Stock Order screen opens. Click **OK**. A suggested stock order like the one below is generated listing parts based on the promotion IDs you provided.

    [Image: Screenshot of a 'SUGGESTED STOCK ORDER' report, showing parts filtered by the entered 'Promo Codes'. The 'Promo Codes' section in the report header is highlighted.]

## P.O.S.

### Flat Rate Adjustment Change
The method by which flat rate labor is adjusted has been changed to ensure technician data in the Service Recovery and Efficiency Report is more accurate. As a result, the last adjustment line on an invoice will now list billed hours as either .01 or .01- and the rate as 100 times the absolute value of the adjustment.

**Previous Final Adjustment Line**
[Image: A snippet of a previous invoice showing the final adjustment lines for labor, which includes a line with .00 hours and a rate of .28-.]

**New Final Adjustment Line**
[Image: A snippet of a new invoice showing the updated final adjustment lines for labor. The last line now shows .00 hours billed with a rate of .01- and a value of .68-.]

### P.O.S. Document Ledger Priority Code (New in 21v5)
A priority code has been added to the document ledger to track changes.

## Archiving

### EOM Financial Report (New in 21v5)
When Accounting End of Month is run for a division, an all department financial report is automatically generated and archived as an Accounting Report. If Combined End of month procedures are ran, then a report for each specified division is generated and archived.

Reports can be viewed through the Work with Archived Documents option in Archiving.

### Search Part Reports by Order Number (New in 21V5)
Recently archived parts reports can now be searched for by entering an associated order number.

- Select **Work with Archived Documents** in Archiving.
- Select **Parts Reports** and click **OK**.

    [Image: Screenshot of the 'Work with Archived Documents' screen. A red arrow shows the flow from clicking 'Search by Fields', selecting 'Order Number' in the 'Search Field Information' dialog, entering a number in the 'Search For' field, and the list of reports being filtered by that order number.]

- Click the **Search by Fields** button.
- Select the **Order Number** option and click **OK**.
- Enter the order number in the **Search For** field and click **OK**.

Contact DIS for assistance in enabling this search process in parts reports that were previously archived.

### Cancelled Order Report (New in 21v5)
A Cancelled Order Report is now automatically generated and archived whenever a stock order, return, or phase-out is cancelled. It is archived as a Parts Report and includes the order number, parts, and the user who completed the cancellation.


title: "New_Features_Guide_for_Keystone_R22v1_-_22v3"
source: "New_Features_Guide_for_Keystone_R22v1_-_22v3.pdf"
tags: ["Keystone", "DIS", "Dealer Information Systems", "R22v3", "R22v2", "R22v1", "Accounting", "POS", "Inventory Management", "Software Features"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "A guide detailing the new features and enhancements in Keystone software releases R22v1, R22v2, and R22v3. It covers updates across Accounting, P.O.S., Units, Inventory Management, and manufacturer interfaces like CLAAS, Kubota, Polaris, and JCB."
long_description: "This document serves as a comprehensive guide to the new features introduced in Keystone software, specifically for releases 22v1, 22v2, and 22v3. The guide is structured by release version, starting with the latest, 22v3, and then covering the combined features of 22v1 and 22v2. Key enhancements in R22v3 include the 'GL Power Add and Copy' for streamlined accounting across multiple divisions, 'Receivable Payment Batch Recovery' for data safety, and archiving for 'Check Reconciliation Reports.' It also details new unit import capabilities and P.O.S. printer setting enhancements. The section on releases 22v1-22v2 highlights major features such as the 'New Associated Addresses' for grouping customers, increased font size for better legibility in the contacts notebook, 'Extra Security for New P.O.S. Documents,' and new manufacturer interfaces. These interfaces include CLAAS Parts Inventory Management (PIM), a Canadian version of the Kubota Interface Master, a Polaris Service Plan viewer, and detailed instructions for configuring JCB Communications for inventory management. The document provides step-by-step instructions, including menu paths and screenshots, to help users configure and utilize these new functionalities effectively."