---
title: "Summary of New Features in Release 15v1-16v4"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Summary of New Features in Release 15v1-16v4."
long_description: "This document provides information about Summary of New Features in Release 15v1-16v4 from the DIS Keystone system."
---

## INTRODUCTION

Following is overview information on the primary new features in R15v1-16v4. Step-by-step instructions for all new features will be added to the Keystone documentation, as soon as they are available.

If you are interested in purchasing Keystone or any of the other purchasable products, please call DIS at 1-800-426-8870.

## ACCOUNTING

### Receivables Maintenance – MyAccount

Use MyAccount (available for purchase, Keystone only) to help make it easier for your customers to do business with you. Customers can receive invoices and statements via email automatically, as well as download them from your website. The MyAccount application is hosted by DIS and integrated into your existing website, making it easier for your customers to access their account information, without having to call you.

As Point of Sale batches are created, invoices will automatically be emailed to designated customers. The invoices will appear as 'Documents' in MyAccount. As non-POS batches are posted to receivable accounts, they are immediately available online on the transaction screen. This includes journal entries, manual adjustments, received on account, and all documents.

In Receivables Maintenance, the new MyAccount option allows you to set up the customers you would like to be able to receive their invoices and statements via email. A separate administration site is used to enter user ID and password that will allow your customers access to their accounts online. Customers will login with their email address and a password selected by you.

### Financial Reports – Manufacturer Financial Reporting

CNH has made a number of changes to their BMS financial statement for 2013. They have changed their standard chart of account table, the structure of the sales and cost of sale accounts, other income and deduction accounts, and departmentalized all of their expense accounts, which has added many new account numbers for mapping.

### Payables – Purchase Order Entry 'Position To'

In Purchase Order Entry (Accounting | Payables | Purchase Order), a `Position To` field has been added to the rolodex within this option.

## UNITS

### Inquire/Update Units - Unit Attachments

> **Note:** A tutorial for Unit Attachments can be found on the DIS Corp website.

A new way to attach units to primary units is now available. The new Unit Attachment Configuration screen, in Inquire/Update Units, will allow you to create special pricing for the entire configuration of units that are attached together.

Point of Sale will allow the selling of the primary unit on a unit sale line and all attachments will be added to the invoice automatically with the special sale price that was built into the configuration. All units will print on the sale invoice together, to show that they are a configuration of units. You can choose to print only the overall configuration price or the individual price of the attachments.

*Figure: The 'Inquire/Update Units - Unit Information' screen, where a new 'Attachment Config' navigation button is available to configure units and their attachments.*

After a unit is configured, attached unit information will display in Inquire/Update Units. On the top of the Unit Information screen, red text will display either 'Primary Unit' or 'Attached to XYZ'. Configured amounts display in red on the lower right of the screen.

*Figure: The 'Inquire/Update Units - Unit Attachment Configuration' screen, showing the costs and prices for a configured unit and its attachments.*

*Figure: The 'Unit Information' screen displaying 'Primary Unit' status in red text at the top and the configured amounts (Dealer Lists, Costs, etc.) in red on the lower right.*

### Units Reports - Units Commission Report

The new Units Commission Report provides information for you to use in preparing unit sales commissions. The report presents revenue and costs for unit 'deals', including cost adjustments to traded-in units.

The new report option is located on the Units Reports menu.
(Menu Path: `Units` > `Units Reports` > `Units Commission Report`)

*Figure: The menu path to access the new 'Units Commission Report'.*

Use the selection criteria on the Units Commission Report - Selection screen to produce a report. You can then export the report data to Excel and apply your own commission calculations that pertain to your dealership.

*Figure: The 'UNITS COMMISSION REPORT - Selection' screen, allowing users to filter the report by salesperson, date range, and other criteria.*

*Figure: A sample of the 'UNITS COMMISSION REPORT' output, showing details of new sales and cost adjustments.*

> **Note:** New with Release 16v4 is the `Not Paid=n` column to the left of the document number. This displays next to unit sales or reversals where the document exists as unpaid in receivables.

## PARTS

### Parts-Bulk Items

> **Note:** A tutorial for Bulk Items can be found on the DIS Corp website.

A new option for 'bulk items' will allow you to order parts in one quantity and sell at another. You can also track the sales history of individual items sold, but order items in bulk. For example, bulk items will allow you to order 100 foot rolls of chain, but sell it by the foot.

Use Parts Posting and Maintenance to add bulk information by supplying the bulk quantity in the 'Bulk' field.

*Figure: The 'Parts Posting and Maintenance - Part Information' screen, with a red arrow pointing to the new 'Bulk' field where the bulk quantity (e.g., 100) is entered.*

A warning appears when entering into the Bulk field, to prevent errors. If the changes are correct, select 'Change Qty & Prices as shown above?', then click OK.

> **Note:** If a part is on an order or a return, you will be restricted from changing it.

*Figure: A warning dialog appears when changing the bulk field, confirming the automatic adjustment of on-hand quantity and prices.*

On the Part Information, bulk and itemized quantities and prices will now display.

> **Note:** In the description field, you can add a note as to the bulk description (feet, gallons, etc), this note will display in POS when the part is sold.

*Figure: The Part Information screen after setting up a bulk item, showing both the total on-hand quantity and the per-item prices.*

**Additional screens displaying Bulk Items**

Bulk information will display in Parts Inquiry, as illustrated below. On the Part Inquiry - Information screen, bulk pricing and quantity, as well as individual pricing and quantity, will display.

> **Note:** Prior to this feature, the Bulk field was MULT.

*Figure: The 'Parts Inquiry' screen showing bulk information on the 'Order Information' and 'Inventory' tabs.*

Bulk information will also display in Correct Stock Order. When in Correct Stock Order, bulk items are indicated with a blue arrow.

*Figure: The 'Stock Return Correction' screen showing a 'Bulk Items' button and an arrow indicating a bulk item in the list.*

Correct Orders Before Receiving also shows when an item is bulk. From this screen you can toggle between Bulk Qty Ordered and Qty Ordered, by using the Quick Code/Receipt Cost navigation button.

*Figure: The 'Correct Order Before Receiving' screen displaying columns for 'Bulk Ordered' and 'Qty Ordered'.*

A warning will display when attempting to correct a stock order and entering a quantity that is not a multiple of the bulk amount.

*Figure: A 'Bulk Warning' dialog that appears when the quantity entered is not a multiple of the bulk amount, providing options to proceed.*

### Bulk Items Report

A new report allows you to run a list of bulk items. From the Keystone main menu, go to Bulk Items Report (`Parts` | `Parts Reports`).

*Figure: The menu path to the new 'Bulk Items Report'.*

The new Bulk Items Reports – Selection screen appears. This new report can be run to list bulk items by vendor, class or All.

> **Note:** All changes to bulk items will display on the Parts EOD report.

*Figure: The 'Bulk Items Report - Selections' screen, allowing filtering by division, vendor, or class.*

### Parts Transaction-Move History

In Parts Posting and Maintenance, a new transaction type of 'Move History' is now available.

*Figure: The new 'Move History' option in the Transaction type dropdown menu in 'Parts Posting and Maintenance'.*

You can use Move History to transfer the sales history from one part to another. This will help when setting up Bulk Items (described earlier). Example: In the past, you may have had a part number set up to sell a portion of an OEM (Original Equipment Manufacturer) part. This option gives you the ability to move history back to the OEM, since the bulk project allows you to break down the quantity within the OEM part.

### Cycle Count Process – Validation Report

With Release 15v2, in Cycle Count Process (Export and Count Validation) (`Parts` | `Parts Inventory Adjustment` | `Parts Inventory Cycle Count`) the validation report has been enhanced to include a change in quantity, cost of the part (or average cost), and extended amount of change for each part adjusted. A total change in inventory dollar value (total of the extended amount of change) has been added at the end of the report, as well.

### Configure Vendor/Class - Parts Synch

> **Note:** A tutorial for Parts Synchronization can be found on the DIS Corp website.

This new feature in Configure Vendor/Class (`Parts` | `Parts Configuration`) allows you to link vendors by division (into a Parent/Child structure) with the option to keep classes synchronized, as well as other part information such as prices, class codes, etc. This job can be scheduled to run during backup, or other dates/times can be defined.

*Figure: The 'Parts Vendor/Class Configuration' screen for a 'Parent Division'.*

*Figure: The 'Parts Vendor/Class Configuration' screen for a 'Child Division', where classes are synchronized and locked from changes.*

If the vendor code is a child vendor in this division, and classes are synchronized, classes will be locked down from changes.

Use the new 'Link Divisions' navigation button to access the following screen. From the Link Divisions screen, you can specify the Parent division, link fields, submit and schedule synching (similar to scheduling backup, but should not run at the same time as backup).

*Figure: The 'Link Divisions' screen for specifying the parent division and linking child divisions.*

The 'Link Fields' navigation button will take you to the following screen, displaying pricing options. Select the 'Continue To Other Fields' navigation button to access the Link Fields - Defaults For All Vendors screen. This screen displays a list of other fields that can be kept synchronized.

*Figure: The 'Link Fields' screen to define synchronization rules for classes and prices.*

*Figure: The 'Link Fields - Defaults For All Vendors' screen showing a list of part fields that can be synchronized.*

From the Link Divisions screen, use the 'Scheduling and Other' navigation button to access the Other Options screen. From this screen you can schedule the job to run at backup, or select a time to run on specified days. If scheduled for backup, the job will actually run after the backup of files has taken place, but before Parts EOD, so that changes will display on EOD reports.

> **Note:** The default number of days to keep logged information is 30 days.

*Figure: The 'Other Options' screen for scheduling the synchronization job and setting data retention.*

### Part Lists - Part Kits

With Release 16v1, in Part Lists (`Parts` | `Part Update/Part Lists`), the Select button now lets you choose a part list 'kit', allowing a single 'part kit' on the list to be copied to the document, but the history and on-hand amounts will be processed for all of the parts in the list. The kit can be created by the parts department either prior to an invoice or at the time an invoice is created and all of the parts will be pulled from their bins and collected for the kit. All of the parts will be included in the kit, but the customer will view the kit as a single entity, with a special price on their invoice.

When in Part Lists, on the 'Select Part List Type' pop-up screen, when the Select button is pressed, a number of things will happen behind the scenes if the Part List contains a part flagged as a 'Kit Part'.

*   Only the part on the list that is designated as the Kit Part will be put on the clipboard designated as the part to be copied to the invoice. The other parts will also go on the clipboard, but will be designated as part of the kit and not the Kit Part.
*   The Kit Part is assumed to be a legitimate part found in inventory (so please make sure it is set up).
*   At the time the Kit Part is copied from the clipboard, a quantity of one is received to inventory for this part. This function will work just as if you were to add one to that part in Parts Posting and Maintenance with the Inventory/Receive transaction code.
*   At the time the Kit Part is copied, the other parts on the list will be adjusted with quantity and demand in their respective histories. This function will work just like if you were to adjust these parts with the Sale transaction code in Parts Posting and Maintenance.

From the Keystone main menu, select Part Lists. (`Parts` > `Price Update / Part Lists` > `Part Lists`)

The Type column will display part lists designated as kit parts. To add kit parts, select the Add New Part List navigation button. In the 'Type of List' drop-down menu, the new type 'Kit: Special P.O.S. Processing' is available.

*Figure: The 'Part Lists' screen showing a 'Kit' type in the list.*

*Figure: The 'Select Part List Type' dialog with the new 'Kit: Special P.O.S. Processing' option.*

Displaying the individual parts in Part Lists shows the new column designating Kit Part. The Kit Part can be select by putting a Y in the Kit Part column. **Only one part on a Part List can be designated as the Kit Part.** When you designate a part as the Kit Part, any other parts on this list that had previously been flagged as a Kit Part, will have the flag automatically removed.

*Figure: Displaying parts within a list, with a 'Y' in the 'Kit Part' column to designate the main part for the kit.*

### Kit Parts in POS

On the POS Detail screen, select the Part List navigation button. The Select button is visible in Part Lists from POS, or from Parts Orders. Highlight the Kit Part and click Select, then click Return With Selections. The following window displays a prompt for the quantity of this Kit that you want to sell. Verify kit quantity and click OK.

*Figure: Selecting a kit from the Part Lists screen within POS.*

*Figure: A prompt appears to confirm the quantity of kits to be sold.*

When you return to POS with a kit selected, only the Kit Part will be put on the invoice. Behind the scenes the quantity selected to sell will be added to inventory for the Kit Part, and subtracted from inventory from the other parts on the Kit. This action will process Parts EOD transactions just as if it had been done manually for each part in Parts Posting and Maintenance.

If a kit is deleted from an invoice, all of the behind the scenes work to inventory will be reversed.

> **Note:** If you drill into the individual parts on a Kit, you can select them individually, but they will not be processed as an entire list.

*Figure: A counter ticket showing only the single Kit Part line item on the invoice.*

## POINT OF SALE

### CNH Credit Cards

As of 16V3, U.S. Invoices paid with a CNH credit card which are CRA approved, will now print the following information at the end of the invoice.

> Remit to: CRA Payment Center P.O. Box 3900 Lancaster, PA 17604-3900
>
> By signing I certify that I am authorized to use this Account, to sign this receipt, and that I agree that the total amount of this invoice is repayable in accordance with the Credit Agreement applicable to the Account.

## MANUFACTURERS

### Manufacturers – AGCO API

AGCO API is now available (for purchase). This new feature allows you to automatically transmit your parts inventory to AGCO and have them help manage your inventory as far as producing suggested orders and returns which are automatically downloaded to the business system.

Each division is configured in ECM with the desired vendor(s) to include in these files. Periodically, Interface Manager will perform a search of any available orders and returns that are ready to download to your business system. A complete snapshot of your inventory and history will be transmitted each Friday with only daily changes being sent the rest of the week. Interface Manager 21202P or higher required.

### Manufacturers – Claas Partsfinder

A new automated process, Claas Partsfinder, has been created to upload your inventory to Claas each night. This will process each division during the End of Day backup procedure. This allows you to send a daily snapshot of your inventory to Claas which can be used for a parts locator application that the manufacturer provides. Setup for each division is done in ECM Configuration. If any files were created, but could not be transmitted, an automatic retry program will attempt to send them again at 9:00 AM the next morning. Interface Manager 21202P or higher is required.

### Manufacturers – John Deere Parts Locator

The new John Deere Parts Locator download feature (for purchase) allows you to automatically transmit inventory and history files to John Deere daily. With this feature, an initial load (Refresh) is sent first, then daily changes afterwards. Any parts locator files that fail during backup will automatically try to send again at 9:00 AM the following morning. Interface Manager 21202P or higher is required.

### Manufacturers – John Deere Parts Priority Orders

Release 15v2 now allows John Deere priority orders (as well as stock orders), as long as both types of orders are finalized for processing by going to the John Deere website. A change to your ECM configuration is required.

### Manufacturers – CNH NGPC Parts Catalog

With Release 16v2, the business system has added new manufacturer codes to work with the CNH NGPC parts catalog. Added, also, is the ability of the interface to find a part even if it is under a different vendor code or is out of stock in the current vendor. This new feature allows you to search other vendors that are configured in Part Catalog Configuration (Parts | Price Update/Parts Lists).