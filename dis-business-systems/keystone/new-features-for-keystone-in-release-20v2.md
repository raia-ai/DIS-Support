---
title: "New Features for Keystone in Release 20v2"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about New Features for Keystone in Release 20v2."
long_description: "This document provides information about New Features for Keystone in Release 20v2 from the DIS Keystone system."
---

## INTRODUCTION

The following information is on the primary new features in R20v2. Complete step-by-step instructions for all new features will be added to Keystone-Online-Help, as soon as they are available.

If you are interested in purchasing Keystone or any of the other products, please call DIS at 1-800-426-8870.

## PARTS

### Select a Part Lists for Correct Stock Return or Correct Stock Phase-Out

We have added a Part Lists button to the Stock Return Correction and Stock Phase-out Correction screens that allows you to select an existing part list and include the parts on the return or phase-out. For phase-outs, the quantity of parts on the part list is ignored and replaced by the on-hand inventory quantities.

1.  Click the **Part Lists** button on the Stock Return Collection or Stock Phase-Out Correction screen (Parts | Stock Return/Phase-out | Correct Stock Return OR Correct Stock Phase-out).

    > **UI Screenshot: Stock Return and Phase-Out Correction Screens**
    > The images show the "STOCK RETURN CORRECTION - SCROLL AND CHANGE LINES" and "STOCK PHASE-OUT CORRECTION SCREEN - SCROLL AND DELETE LINES" screens. On both, a **Part Lists** button is now available.

2.  Select the part list from the table on the Part Lists screen that opens and click the **Select** button. A message appears at the bottom of the screen stating the Part list(s) have been selected.

    > **UI Screenshot: Part Lists Screen**
    > The image displays the "PART LISTS - Sorted By: List Name" screen. A list of available part lists is shown in a table. Buttons like "Return with Selections" and "Select" are visible. A message at the bottom confirms "Part list(s) selected."

3.  Click the **Return with Selections** button. The Stock Return Correction/Stock Phase-Out Correction screen re-opens with the parts listed in the table.

### Ability to Insert a Decimal in Bulk Quantity
*(Parts | Parts Posting & Maintenance)*

You can now insert a decimal point into the Bulk amount for a part in Parts Posting & Maintenance. If you do not insert a decimal point, a decimal point and two zeros are added to the number you provide on the Change Bulk Field Warning screen that opens.

> **UI Screenshot: Parts Posting and Maintenance - Part Information**
> The image shows the "Parts Posting and Maintenance" screen with a "Change Bulk Field Warning" dialog box open. The dialog allows the user to input a "New Bulk amount", which is shown as `325.00`, demonstrating the ability to use decimals.

### Price Book Import Error Notification (Purchasable Product)

If you create a price book from a CSV file and there are records that are incorrectly formatted in the file that prevent their insertion into the price book, the problem records are automatically printed on an exception report.

### Added Print/Finalize button to Stock Order Correction - Scroll and Change Lines Screen

We have added a Print/Finalize button to the Correct Stock Order/Create Manual Order – Scroll and Change Lines screen. After creating/correcting the order, you can print and finalize the order by clicking this button rather than having to go through the Print/Finalize Order menu option.

> **UI Screenshot: Stock Order Correction Screen**
> The image displays the "STOCK ORDER CORRECTION - SCROLL AND CHANGE LINES" screen. A new **Print/Finalize** button is visible next to the "Pre-Edit" button.

### New Stihl Bryan Order Download

A Stihl Bryan order download is now available for purchase. It allows you to download your stock order to your local PC as a text file, access it, and upload into the manufacturer's website.

### New Kinze Order Download

A Kinze order download is now available for purchase. It allows you to download your stock order to your local PC as a text file, access it, and upload into the manufacturer's website.

### Kobelco Parts Locator

Files listing Kobelco part inventory have been added and will be updated nightly. This allows you to search for Kobelco parts and find the location(s) closest to your dealership that have the parts available for sale.

## POINT OF SALE

### New “Remit to” Address for Productivity Plus (For U.S. Customers Only)

The "Remit to" address printed on the invoice has been changed to the new address for Citibank/Productivity Plus.

> **UI Screenshot: Invoice Snippet**
> The image shows the bottom portion of an invoice. The "Remit to" section has been updated to:
> **Remit to: Productivity Plus Account**
> **Regular Mail:** P.O. Box 78004 Phoenix, AZ 85062-8004
> **Express Mail:** 1820 E. Sky Harbor Circle South STE 150 Phoenix, AZ 85034

### Warning Screen Appears when Sales Code Format Changed (Optional Security Gate Available)

We have added a warning screen that will display when you exit the Sales Code Maintenance screen after changing the format of an existing sales code. This screen allows you to verify and confirm that you want to make the change before it becomes final.

> **UI Screenshot: Warning Dialog**
> A "WARNING" dialog box is displayed with the message: "You are attempting to change the format of an existing Sales Code. This can cause errors on invoices where the sales code was used with the prior format." Options are "Continue" and "Cancel".

A security gate that users will have to pass through the first time they attempt a sales code format change has also been installed. You can change the gate to 00 in Step 5 below to remove the security gate if desired.

1.  Select Security Maintenance from the Keystone main menu (Security | Security Maintenance).
2.  Type your master security code in the Division Code field on the Security Maintenance screen and click **Enter**.
3.  Click the **Assign Gates to Menu Options** button.
4.  Type "change format” into the Position to field and click **Enter**. The Assign Gates to Menu Options screen opens.

| Menu Option Title | Gate | Always Show Gate |
| :--- | :--- | :--- |
| Point of Sale / Table Maintenance / Sales Code Change Format | 01 | ☐ |

5.  The default security gate for this event is 01 (Accounting) and users will need to pass through it if they have not passed through the Accounting gate before. If you would like to change the gate, click **Gate** and select a new gate from the list that appears. Select the **Always Show Gate** check box if you want users to pass through the security gate every time they change a sales code format.

### Reports Archived when you Create Point of Sale Batch
*(P.O.S. | Post P.O.S. Documents | Create Point of Sale Posting Batch)*

When you select Create Point of Sale Posting Batch, the following information is automatically archived in the P.O.S. Posting Summary Report:

*   Voided and Re-assigned Documents
*   Parts Sold with Zero Cost
*   Parts Costing Summary
*   Cash Tendering Summary (if the cash tendering opt is turned on)

These reports can be located by Selecting Work with Archived documents (Archive | Work with Archived Documents) and then selecting POS Batch Reports on the screen that appears.

### Security Gate Available in P.O.S. Invoicing

A security gate that employees will need to pass through prior to closing a Point of Sale invoice is now available.

1.  Select Security Maintenance from the Keystone main menu (Security | Security Maintenance).
2.  Type your master security code in the Division code field on the Security Maintenance screen and click **Enter**.
3.  Click the **Assign Gates to Menu Options** button.
4.  Type "close" into the Position to field and click **Enter**. The Assign Gates to Menu Options screen opens.

| Menu Option Title | Gate | Always Show Gate |
| :--- | :--- | :--- |
| Point of Sale Close | 00 | ☐ |

5.  The default security gate for this event is 00 (No Security Gate). Click **Gate** and select a different security gate if you want users to pass through a security gate the first time they close a POS invoice. Select the **Always Show Gate** check box if you want users to pass through the security gate every time they close a POS invoice.

When the Always Show Gate check box is selected, the security gate will display when the Prt & Cls button is clicked from any screen in P.O.S. Invoicing including the Part Availability screen.

## PARTS AND P.O.S.

### Added Second Bin Location for Parts

We have added a space to record a second bin location for parts in Parts Posting and Maintenance.

> **UI Screenshot: Parts Posting and Maintenance - Part Information**
> The image shows the "Parts Posting and Maintenance" screen. In the top right section, there are now two fields for "Location", allowing a primary and a secondary bin location to be recorded for a part.

After a second bin location is added, it will display on all screens and reports where bin locations are listed.

## SECURITY

### Reformatted the text “Pay to the Order of” on Checks

We have reformatted the “Pay to the Order of” text on checks and moved its placement so that it no longer shows in the envelope window.

> **UI Screenshot: Check Layout**
> The image shows a portion of a printed check, highlighting that the "Pay to the order of" text has been moved up and to the left, out of the typical envelope window area.

## FLEET MANAGEMENT

### Print Service Notes with Scheduled Maintenance Due Report
*(Service | Service Reports | Scheduled Maintenance Due)*

We have added a check box that when selected will print Unit Service Notes with the Scheduled Maintenance Due Report.

> **UI Screenshot: Fleet Management Report Dialog**
> The image displays the "Fleet Management Report - Schedule Maintenance Due" dialog box. A new checkbox labeled **Print Unit Service Notes** has been added.


title: "Kubota Interface Master - Keystone"
source: "Kubota_Interface_Master_-_Keystone.pdf"
tags: ["Kubota", "Keystone", "DIS", "Parts Order", "Part Availability", "Parts Locator", "Invoicing", "Stock Order", "Interface", "Technical Manual"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "A guide to using the Kubota Interface within the DIS Keystone system. It details functionalities such as viewing part availability, locating parts at other dealerships, placing and managing part orders, and using material groups to create suggested stock orders."
long_description: "This technical manual provides comprehensive instructions for dealership staff on utilizing the Kubota Interface integrated with the Dealer Information Systems (DIS) Keystone platform. The document serves as a step-by-step guide for various parts management tasks. Key features covered include: Kubota Part Availability, which allows users to check part information and stock levels at specific warehouses; Kubota Parts Locator, enabling dealers to find parts at other dealerships and submit their own inventory for posting; and Kubota Part Orders, which details the process of configuring shipments, placing, and tracking orders. The guide also explains how to work with Kubota Material Groups and Part Categories to generate suggested stock orders. It walks users through the entire order lifecycle, from viewing pre-edit options and making decisions on shipping methods, to finalizing and transmitting the order to Kubota, and finally, checking the order status and tracking shipments. The document is heavily illustrated with screenshots of the Keystone software interface to provide clear, visual guidance for each step."