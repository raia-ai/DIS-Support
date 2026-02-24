---
title: "Summary of New Features for Quantum in Release 20v2"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Summary of New Features for Quantum in Release 20v2."
long_description: "This document provides information about Summary of New Features for Quantum in Release 20v2 from the DIS Quantum system."
---

## INTRODUCTION
The following information is on the primary new features in Quantum R20v2.

If you are interested in purchasing Quantum or any other products, please call DIS at 1-800-426-8870.

## QUANTUM

### Management 360 Feature
We have added the Management 360 feature in Quantum which provides Key Performance Indicators (KPI) that measure the success of a business by showing the performance levels for particular activities within the business. These measurements can illustrate progress towards a certain goal or indicate potential areas of improvement.

Setup is required to access this feature. Click `here` for setup instructions and additional information on Management 360.

*(An image displays the Quantum main screen, with a red arrow pointing to the new "Mgmt 360" button on the left-side menu, located below "Cust 360".)*

### Added Fields to Customer 360 Search Feature
We have added additional fields and buttons (box 1) to the already existing search feature in Customer 360 (box 2).

*(An image displays the "Customer 360 Search" screen. Box 1 highlights new fields for "Name", "Telephone", and "Address Number", along with "Search" and "Point of Sale" buttons. Box 2 highlights the existing general search text box.)*

The Search fields in Box 1 function like the customer lookup feature that already exists within Point of Sale. Provide a customer name or telephone number and click the **Search** button to display the customer's information on the Select Address screen or click the **Point of Sale** button to go directly to P.O.S. Invoicing.

> **Note:** You can enter a partial name or telephone number and click the **Search** button to display all customers with matching information on the Select Address screen.

*(An image shows the "Select Address" screen, displaying a list of customers matching the search criteria "JAMES", with columns for Name, Addr#, Div, Phone, and Type.)*

## PARTS

### Select a Part Lists for Correct Stock Return or Correct Stock Phase-Out
We have added a Part Lists button to the Stock Return Correction and Stock Phase-out Correction screens that allows you to select an existing part list and include the parts on the return or phase-out. For phase-outs, the quantity of parts on the part list is ignored and replaced by the on-hand inventory quantities.

1.  Click the **Part Lists** button on the Stock Return Collection or Stock Phase-Out Correction screen (Parts | Stock Return/Phase-out | Correct Stock Return OR Correct Stock Phase-out).

*(An image displays the "STOCK ORDER CORRECTION - SCROLL AND CHANGE LINES" screen, with the "Part Lists" button highlighted on the left-side menu.)*

*(A second image displays the "STOCK PHASE-OUT CORRECTION SCREEN - SCROLL AND DELETE" screen, also with the "Part Lists" button highlighted on the left-side menu.)*

2.  Select the part list from the table on the Part Lists screen that opens and click the **Select** button. A message appears at the bottom of the screen stating the Part list(s) have been selected.

*(An image displays the "PART LISTS" screen. The "Return With Selections" button is highlighted, which appears to be a mislabeling in the document for the "Select" button mentioned in the text. The table shows a list of available part lists.)*

3.  Click the **Return with Selections** button. The Stock Return Correction/Stock Phase-Out Correction screen re-opens with the parts listed in the table.

### Ability to Insert a Decimal in Bulk Quantity
(Parts | Parts Posting & Maintenance)
You can now insert a decimal point into the Bulk amount for a part in Parts Posting & Maintenance. If you do not insert a decimal point, a decimal point and two zeros are added to the number you provide on the Change Bulk Field Warning screen that opens.

*(An image displays the "Parts Posting and Maintenance - Part Information" screen with the "Change Bulk Field Warning" pop-up. The pop-up shows a "New Bulk amount" field where "325.00" has been entered, demonstrating the use of a decimal.)*

### Price Book Import Error Notification (Purchasable Product)
If you create a price book from a CSV file and there are records that are incorrectly formatted in the file that prevent their insertion into the price book, the problem records are automatically printed on an exception report.

### Added Print/Finalize button to Stock Order Correction - Scroll and Change Lines Screen
We have added a Print/Finalize button to the Correct Stock Order/Create Manual Order – Scroll and Change Lines screen. After creating/correcting the order, you can print and finalize the order by clicking this button rather than having to go through the Print/Finalize Order menu option.

*(An image displays the "STOCK ORDER CORRECTION - SCROLL AND CHANGE LINES" screen, with the new "Print/Finalize" button highlighted on the left-side menu.)*

### New Stihl Bryan Order Download
A Stihl Bryan order download is now available for purchase. It allows you to download your stock order to your local PC as a text file, access it, and upload into the manufacturer's website.

### New Kinze Order Download
A Kinze order download is now available for purchase. It allows you to download your stock order to your local PC as a text file, access it, and upload into the manufacturer's website.

### Kobelco Parts Locator
Files listing Kobelco part inventory have been added and will be updated nightly. This allows you to search for Kobelco parts and find the location(s) closest to your dealership that have the parts available for sale.

## Point of Sale

### New “Remit to” Address for Productivity Plus (For U.S. Customers Only)
The "Remit to" address printed on the invoice has been changed to the new address for Citibank/Productivity Plus.

*(An image shows a section of an invoice with a red box highlighting the new "Remit to" address: Productivity Plus Account, P.O. Box 78004, Phoenix, AZ 85062-8004 for Regular Mail and 1820 E. Sky Harbor Circle South STE 150, Phoenix, AZ 85034 for Express Mail.)*

### Warning Screen Appears when Sales Code Format Changed (Optional Security Gate Available)
We have added a warning screen that will display when you exit the Sales Code Maintenance screen after changing the format of an existing sales code. This screen allows you to verify and confirm that you want to make the change before it becomes final.

*(An image displays a "SALES CODE MAINTENANCE" warning pop-up: "WARNING: You are attempting to change the format of an existing Sales Code. This can cause errors on invoices where the sales code was used with the prior format." with "Continue" and "Cancel" buttons.)*

A security gate that users will have to pass through the first time they attempt a sales code format change has also been installed. You can change the gate to 00 in Step 5 below to remove the security gate if desired.

1.  Select Security Maintenance from the Quantum main menu (Security | Security Maintenance).
2.  Type your master security code in the Division Code field on the Security Maintenance screen and click **Enter**.
3.  Click the **Assign Gates to Menu Options** button.
4.  Type "change format” into the Position to field and click **Enter**. The Assign Gates to Menu Options screen opens.

| Menu Location / Menu Option Title | Gate | Always Show Gate |
| :--- | :---: | :---: |
| Point of Sale / Table Maintenance / Sales Code / Change Format | 01 | ☐ |

5.  The default security gate for this event is 01 (Accounting) and users will need to pass through it if they have not passed through the Accounting gate before. If you would like to change the gate, click **Gate** and select a new gate from the list that appears. Select the **Always Show Gate** check box if you want users to pass through the security gate every time they change a sales code format.

### Reports Archived when you Create Point of Sale Batch
(P.O.S. | Post P.O.S. Documents | Create Point of Sale Posting Batch)
When you select Create Point of Sale Posting Batch, the following information is automatically archived in the P.O.S. Posting Summary Report:
-   Voided and Re-assigned Documents
-   Parts Sold with Zero Cost
-   Parts Costing Summary
-   Cash Tendering Summary (if the cash tendering opt is turned on)

These reports can be located by Selecting Work with Archived documents (Archive | Work with Archived Documents) and then selecting POS Batch Reports on the screen that appears.

### Security Gate Available in P.O.S. Invoicing
A security gate that employees will need to pass through prior to closing a Point of Sale invoice is now available.

1.  Select Security Maintenance from the Quantum main menu (Security | Security Maintenance).
2.  Type your master security code in the Division code field on the Security Maintenance screen and click **Enter**.
3.  Click the **Assign Gates to Menu Options** button.
4.  Type "close" into the Position to field and click **Enter**. The Assign Gates to Menu Options screen opens.

| Menu Location / Menu Option Title | Gate | Always Show Gate |
| :--- | :---: | :---: |
| Point of Sale / Close | 00 | ☐ |

5.  The default security gate for this event is 00 (No Security Gate). Click **Gate** and select a different security gate if you want users to pass through a security gate the first time they close a POS invoice. Select the **Always Show Gate** check box if you want users to pass through the security gate every time they close a POS invoice.

When the Always Show Gate check box is selected, the security gate will display when the Prt & Cls button is clicked from any screen in P.O.S. Invoicing including the Part Availability screen.

## PARTS AND P.O.S.

### Added Second Bin Location for Parts
We have added a space to record a second bin location for parts in Parts Posting and Maintenance.

*(An image displays the "Parts Posting and Maintenance - Part Information" screen. A red box highlights a new, second "Location" field under the existing one.)*

After a second bin location is added, it will display on all screens and reports where bin locations are listed. Click `here` for a list of screens/reports with a second bin location.

## SECURITY

### Reformatted the text “Pay to the Order of” on Checks
We have reformatted the "Pay to the Order of" text on checks and moved its placement so that it no longer shows in the envelope window.

## FLEET MANAGEMENT

### Print Service Notes with Scheduled Maintenance Due Report
(Service | Service Reports | Scheduled Maintenance Due)
We have added a check box that when selected will print Unit Service Notes with the Scheduled Maintenance Due Report.

*(An image shows the "Fleet Management Report - Schedule Maintenance Due" pop-up. A red box highlights the new "Print Unit Service Notes" checkbox.)*


title: "Quantum_New_Features_Guide_21v1"
source: "Quantum_New_Features_Guide_21v1.pdf"
tags: ["Quantum", "Release Notes", "21v1", "DIS", "Dealer Information Systems", "Units", "P.O.S.", "Time Clock", "Data Mine", "Software Update"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "A guide detailing the new features and enhancements in Quantum Release 21v1. It covers updates to Units, Point of Sale (P.O.S.), the ability to add work order notes in Time Clock, and improvements to Quantum Data Mine."
long_description: "This document provides a comprehensive overview of the primary new features introduced in Quantum Release 21v1, a software product from Dealer Information Systems (DIS). The guide is intended to inform users about significant enhancements across various modules of the Quantum system. Key updates include the 'Units' section, which now supports longer Make/Model names, an increased capacity for storing up to 999 unit pictures, and more flexible search options. The 'P.O.S.' (Point of Sale) module has been improved with new options to print prices on invoices for priority order parts and to select different costing methods for dropship parts. A major new workflow allows technicians to create work order notes directly within the 'Time Clock' module; these notes can then be reviewed, edited, and added to the final customer invoice. The 'Quantum Data Mine' feature has also been updated to allow sharing of public reports between users and to import reports from Keystone. The document uses screenshots and step-by-step instructions to guide users through these new functionalities."