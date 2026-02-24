---
title: "Summary of New Features in Release 17v1 - 17v10"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Summary of New Features in Release 17v1 - 17v10."
long_description: "This document provides information about Summary of New Features in Release 17v1 - 17v10 from the DIS Keystone system."
---

## INTRODUCTION

Following is overview information on the primary new features in R17v1 – 17v10. Step-by-step instructions for all new features will be added to the Keystone documentation, as soon as they are available.

If you are interested in purchasing Keystone or any of the other purchasable products, please call DIS at 1-800-426-8870.

## ACCOUNTING

### Receivables Inquiry/Maintenance - CNH Gateway Customer Inquiry

CNH customer credit card information is now accessible in Receivables Inquiry/Maintenance. This option allows you to view a customer's account information, such as current balance, last payment date, current payment amount due, etc., from within the business system. Note: This requires the latest version of Interface Manager. This feature is also available in Address Maintenance and POS Invoicing.

### Payables Invoice Entry (Double-Post) – Position to P.O. Number

With Release 17v10, when requesting the list of PO's to select and apply to an invoice, a new `Position To` field has been added for the PO number.

### Payable Checks – Electronic Funds Transfer (EFT) Checks

The DIS Payables Checks applications now allow Keystone dealers to create a file during the printing of checks that can be uploaded through a secure Internet portal to an Electronic Funds Transfer (EFT) processing vendor, such as FreedomWare. This will then create Automated Clearing House (ACH) transfers made from the dealership's specified bank account to each payable vendor's bank account, and an email will be produced and automatically sent to the vendor with check stub information attached in the form of a PDF file. For more information, click here.

## PARTS

### Parts Posting and Maintenance and Correct Order Before Receiving - Prevent Supersession Circular Chain

Changes have been made in both Parts Posting and Maintenance and Correct Order Before Receiving to prevent the manual creation of a circular supersession chain.

If the Parts OPT for Superseded Parts is set to 'Process supersession chain on a suggested stock order' (if you are not sure, you can run an OPT Report (Security | OPT Report), and you try to add a supersession reference which would otherwise create a circular supersession chain, a new screen will display to show all of the links in the existing chain.

In the following example, part number AA2094 has been added to supersede the same part number AA2094.

*(Image of the 'Parts Posting and Maintenance - Part Information' screen shows part AA2094 being superseded by itself, CAS AA2094, which would create a circular reference.)*

When Enter is pressed, the following screen will appear with a 'circular supersession error' message.

> **Circular Supersession Error**
>
> You have requested to supersede CAS AA2094 with CAS AA2094. Because of previously recorded supersession information this change would create a supersession chain with no ending point. To prevent this you will need to either modify the existing supersessions or receive CAS AA2094 with action code T (temporary replacement). Temporary replacements are not recorded as permanent supersessions in your parts database.
>
> CAS AA2094 -->
> CAS AA2094 -->

### Correct Order Before Receiving – New Order Code 'T'

When correcting the order before receiving, you can use order code 'T' to mark the superseding part as a temporary replacement. Temporary replacements are received similar to normal supersessions, except that the supersession link is not retained in the parts database after the receipt. The receive order report will show 'T' receipts as 'T/R:' instead of 'S/B:'.

## POINT OF SALE

### POS Invoicing – Reset Tax Code

You can now reassign/reset the tax code used on all lines on a POS document. This can be useful when a document has existing lines and the ship-to address is added or changed. The new Reset Tax navigation button displays on the sold-to screen, if you are using Advanced Tax or DBST.

*(Image of the 'COUNTER TICKET' screen shows a new 'Reset Tax' button on the left navigation panel.)*

If the Reset Tax code button is selected, the following warning screen appears.

> **Change Tax code on Detail lines**
>
> This program will reset the tax code on each detail line using the current customer and ship to address (incl part tax, I/W, etc)
>
> This can be helpful if you have just changed the ship to address. WARNING: Manual tax changes will NOT be retained.

### POS Invoicing – Work Order Default Values

In the past, within a POS Work Order, you would pass through the Work Order Default Values screen (if the OPT was set to display this screen). This screen would appear each time you went from the Sold-To screen to the Detail screen. With R17v5, this screen will only appear the first time you go into a Work Order, after which, the screen will no longer display (for Keystone only). To access the screen, a new navigation button “WO Def” will appear on the bottom left of the Sold-To screen. If the OPT is set to not show the Work Order Default Values screen, this new navigation button will act as if you had just pressed Enter.

*(Image of the 'COUNTER TICKET' screen shows a new 'WO Def' button on the bottom-left navigation panel.)*

### Point of Sale - Credit Card Connect2

In R17v5, with Connect2 credit cards, check amount and cash amount fields have been added to the authorization screen and both amounts will print on the invoice. It is a John Deere requirement that the amount paid in cash on Connect2 credit cards be transmitted to them.

### Point of Sale – Service Enhancements

Following is a list of new Point of Sale and Service enhancements that have been added to the DIS Business System.
*   Flat Rate Labor by Document or by Segment (for CNH and non-CNH dealers)
*   Note Sets
*   CNH Operation Codes and Preventive Maintenance Tables (subscription required)
*   Service Recovery and Efficiency Report
*   Print Labor Detail by Sales Code

These new features are briefly described in this document. In addition, some features have expanded tutorials on the DIS Corp website, for more in-depth information.

### POS Invoicing - Flat Rate Labor by Document or Segment

More and more service shops are implementing a system of flat rating in order to stay competitive. DIS provides a variety of ways to flat rate your service jobs, from a simple manual entry when closing a work order to a more comprehensive system with automatic adjustments. You can create service jobs with an estimate by establishing labor minimum and/or maximum charges or a flat rate labor charge for specific work orders or segments You can also create work orders with flat rates, either segmented or not, and save these jobs as Note Sets to use again and again.

For CNH dealers with a subscription, you can create flat rated jobs using the CNH Operation Codes (also known as job codes) and Preventive Maintenance tables, copy those jobs to work orders, and save them as Note Sets, as well.

Labor sales codes can now be set to print detail or not print detail. Flat rates for labor can be manually adjusted right before closing the work order. Just set the sales code to not print details, and then the customer will see only the total charge for Customer Labor. If labor adjustments are made on a work order, to be able to provide a flat rate, you may want to change your labor sales code.

Labor minimum and/or labor maximum can be set on the Service Info screen. A min/max can be used to provide an estimate (ex: between $500 min and $600 max). The min and max can also be used to establish a flat rate (ex: $500 min and $500 max).

*(Image of the 'DOCUMENTS-Service Info' screen shows fields for 'Labor Minimum Charge' and 'Labor Maximum Charge'.)*

All of these methods and more are described in detail in the Flat Rating tutorials on the DIS website. Click the following links if you would like to view tutorials:
*   [Flat Rating for CNH Dealers tutorial](http://)
*   [Flat Rating for non-CNH Dealers tutorial](http://)

### POS Invoicing – Note Sets

A detailed tutorial for Note Sets can be found on the DIS website. Click the following link to view the tutorial: [Note Sets tutorial](http://)

Note Sets (Keystone only) allow you to set up groups of related work order note lines which can be saved and recalled for later use. Since typical dealership repair jobs can consist of several individual jobs, a note set can be used to group related jobs, helping you maintain complete and consistent notes for any service job. Note Sets can be created for a particular division or made available for all divisions.

From a POS work order, on the Work with Notes screen, select the Note Sets navigation button.

*(Image of the 'Point of Sale - Work with Notes' screen shows the 'Note Sets' button being selected.)*

Supply work order notes and click Note Sets to save. The following screen appears.

*(Image of the 'Point of Sale - Note Sets' screen where a user can create a new set, search for existing sets, and view a list of saved note sets.)*

Supply a description for the Note Set and click Create (Divisional or All Divisions). The Note Set is added to the list. Lists can be positioned by description (default), user or date. Regardless of the sort order, you can also filter the list of note sets using a keyword.

To copy a Note Set to a work order, highlight the Note Set and click Select. If the user has indicated a work order segment before selecting a Note Set, the notes will be copied directly to a work order segment. Flat rates can be added to Note Sets, as well, to be used over again, for other jobs. CNH Operation Codes and Preventive Maintenance codes can also be grouped and saved as Note Sets.

### Point of Sale - CNH Operation Codes and Preventive Maintenance Tables (subscription required)

CNH Operation Codes (formerly job codes) and Preventive Maintenance tables (Keystone only, Service Management required) are used in Point of Sale and Inquire/Update Service Units and contain repair descriptions, standard repair times (SRT), and more for CNH equipment. These codes and tables are initially transferred from your DIS Weblocker to your business system and are then automatically updated during successful backups.

CNH Operation Codes and Preventive Maintenance tables can be accessed from the Point of Sale Additional Options screen and the Point of Sale Work with Notes screen, illustrated below.

*(Image of the 'Point of Sale - Work with Notes' screen shows the 'CNH Operations' and 'CNH Prevent. Maint.' buttons.)*

By selecting either the CNH Operations or the CNH Prevent. Maint. navigation button, the following Search Type selection screen appears. For these examples, we will look at CNH Operation Codes, however Preventive Maintenance tables work in much the same fashion.

*(Image of the 'CNH Operation Codes - Search Type' screen shows buttons for 'Search by Serial Number' and 'Search by Model'.)*

Select Search by Serial Number, and a screen similar to the following appears.

*(Image shows a list of equipment based on a serial number search.)*

Select Search by Model, and a screen similar to the following appears. Note: If you are in a work order, the serial number will auto-fill.

*(Image shows a list of equipment models to select from.)*

For this example, we will select a model and click Select. A screen similar to the following appears. All groups for the selected model display. Highlight the group and click Select. If sub-groups exist, you can drill down to find the one you need. Highlight the job code and click Select. A screen similar to the following appears.

*(Images show the process of drilling down from a model to a specific operation code: selecting a group, then a sub-group, then viewing the list of operations with their Standard Repair Times (SRT).)*

Each job contains the operation code, description of work to be performed and a standard repair time (SRT). From this screen you can: 'Copy' the job to a work order; display job 'Details'; or toggle between 'Display only CNH Description' or 'Dealer Description (if any)'. A sample of the Details screen is illustrated below.

*(Image of the 'Operation Code Details - CNH Description' screen shows the operation, SRT, rate, and extended cost.)*

Select as many jobs as you would like, by using the back arrow to return to the codes list. When selected and copied back to the Work with Notes screen, the SRT and the work descriptions are included. The SRT will not print on the closed customer copy of the work order.

*(Image shows the work order notes screen with the selected CNH operations and their SRTs added.)*

Select 'Return with changes' to continue. You can then select to calculate a labor flat rate, if desired.

*(Image of a dialog box asking 'Calculate Labor Flat Rates?' with options to 'Do Not Calculate' or 'Calculate'.)*

This screen can be used as a worksheet to help calculate a min and max. Standard Repair Times for each selected job shows along with a total at the bottom. Make changes to repair times or to the default labor rate, as needed. When you have established a min and max, click Return with Changes. Labor flat rates will be added to the work order.

*(Image of the 'Point of Sale - Calculate Labor Flat Rates' screen, showing standard and dealer repair times, totals, and fields for setting a Labor Flat Rate Minimum and Maximum.)*

A message displays on the bottom of the screen confirming flat rates have been created. Flat rate lines appear on the work order, but will not print on the closed customer copy.

*(Image of the 'REPAIR ORDER' screen shows FLATMIN and FLATMAX lines added to the work order details.)*

Preventive Maintenance tables work in the same fashion as Operation Codes. These repair jobs can be saved in order to be used with other work orders in Note Sets. (See Note Sets described earlier in this document.)

### Point of Sale – End of Month – POS Document Purge Date

The document purge date for POS End of Month has been changed to allow you to keep at least one year of POS document history, instead of the previous requirement of no less than five years.

### Point of Sale – POS Reports - Service Recovery and Efficiency Report

A detailed tutorial for the Service Recovery and Efficiency Report can be found on the DIS website. Click the following link if you would like to view the tutorial: [Service Recovery and Efficiency Report Tutorial](http://)

The new Service Recovery and Efficiency Report allows dealerships with Service Management to measure technician recovery rates and billing efficiency rates, provided that all technician paid hours (both revenue and non-revenue) are entered on Point of Sale labor lines.

The new report is listed on the POS Reports menu.

*(Image shows the P.O.S. Reports menu with 'Service Recovery and Efficiency' highlighted.)*

Select Service Recovery and Efficiency. The following Overview screen displays how recovery rate and efficiency are calculated.

> **SERVICE RECOVERY AND EFFICIENCY - Overview**
>
> The Service Recovery and Efficiency Report provides recovery and billing efficiency rates for selected technicians.
>
> **Recovery Rate** = Billed Hours / Total Hours Worked
> **Billing Efficiency** = Billed Hours / Total Revenue Hours
>
> **Example:** If a technician billed 5 hours of his 8 hour work day on customer work orders and also spent 1 hour of that same day cleaning the shop, his Recovery Rate for the day would be 62.5% (5/8) and his Billing Efficiency Rate would be 71.4% (5/7).
>
> In order for the information on the report to be accurate all technician payroll hours must be posted to Point of Sale work orders. Point of Sale work orders which are "Non-Revenue" must be flagged on the work order Service screen. Typically "Non-Revenue" work orders are opened to virtual "customers" which are tied to expense accounts. In the above example the cleaning time (1 hour) would have been posted to a "Non-Revenue" work order opened to "The Shop".

Click Continue. The following screen appears to select divisions.

Select a division or ALL and click Continue. Note: If only one division is selected, you will not see the following screen. Select the type of report you would like to run. For this example, we will select Technician Report.

*(Images show the report workflow: selecting divisions, then selecting the report type - Technician Report or Divisional Summary.)*

Make your selections. Note: In the date range field, if the system date is before the 16th of the month, the date range will default to the previous month. From this screen you can also select to print detail lines and how you would like the report to sort. Click Continue and the following screen appears.

*(Image shows the report criteria screen: date range, print detail option, and sort by options.)*

Only technicians with labor punches for the selected date range will be listed. Select technicians, or all, and click Continue. The report will print. A sample of a detailed technician report is illustrated below.

> **Sample Detailed Technician Report**
> The detailed report shows individual labor lines for each technician with totals below. Labor lines on revenue documents with reported hours of zero are listed with 'adjust' on the technician detail report. It includes columns for Revenue Reported, Revenue Billed, Non-Rev Reported, Total Reported, Recovery %, and Efficiency %.

> **Sample Technician Summary Report**
> A summary report showing total hours and recovery/efficiency percentages for each technician and a divisional total.

### Point of Sale – Sales Code Maintenance - Print Labor Detail by Sales Code

Now, in Point of Sale, when work orders are printed, the Sales Codes (POS | Table Maintenance) labor detail values will be used to determine how labor detail prints. In Sales Code Maintenance, a new field for Print Detail has been added to the labor sales code screen for this purpose.

*(Image of the 'SALES CODE MAINTENANCE' screen shows a new column 'Print Detail?' with a dropdown menu for Customer, Internal, and Warranty labor.)*

The 'Print Detail?' column is displayed when setting up a new sales code or changing an existing labor sales code. Each field (customer labor detail, internal labor detail, or warranty labor detail) must be set to one of the following (selected from dropdown menu):
1.  **No Detail:** No labor detail lines are printed.
2.  **Print detail:** Labor detail lines are printed.
3.  **TK job not tech#:** Combine labor lines with matching TK job codes and do not print employee#.
4.  **TK job not freon#:** Combine labor lines with matching TK job codes but print only freon#, job code, and description.
5.  **TK job and desc:** Combine labor lines with matching TK job codes but print only job code and description.

Opt Point of Sale Menu Thirteen (X636-D) can be used to set print detail defaults, if desired. The printed sales code table has been modified to include the new detail fields.

### Point of Sale – Voiding Documents Opts

Opt Point of Sale Menu Seven (X636-7), options 6 and 7 have been added to control whether documents can be voided which contain labor posted through Time Clock.
*   **Option 6:** Voiding allowed when Time Clock labor exists
*   **Option 7:** Voiding restricted when Time Clock labor exists

> **Note:** This opt defaults to #7: Voiding restricted when Time Clock labor exists.

## MANUFACTURERS

### Customer Sales History Report – Address and Phone

In CNH Customer Sales History (Manufacturers | CNH Communications | CNH Reports), the customer's street address and phone number are now included on the report.

*(Image of the 'CNH CUSTOMER SALES HISTORY' report shows new columns for Address, City, St, Zip, and Phone.)*

## SERVICE MANAGEMENT

### Inquire/Update Service Units – Security

A new security setting has been added to Inquire/Update Service Units associated with the Delete function. By default, the setting will be no security, but that can be changed in Security Maintenance, if a security setting is desired.

## SYSTEM

### Report Center - Template for Finalized Orders

With Release 17v10, Keystone Report Center has added an Excel template for finalized stock, priority and drop-ship orders.

## OTHER

### MyAccount - POS Invoicing

For dealers with MyAccount only. In the past, with MyAccount enabled, a notification screen displayed when a customer was configured to receive invoices via email and not have the invoice print. The following override field has been added with R17v6 to allow a copy of the invoice to be printed, if selected.

> **Email Invoice Only**
> This customer has been configured to receive invoices by email only. An email with the invoice attached will be sent once it has been posted. The invoice will not print unless specified below. It will be emailed regardless of your answer.
> [ ] Print this time only

### MyAccount - Document View

For dealers with MyAccount only. The ability to suppress certain document types from view in MyAccount is now available. The Document Classification screen (POS | Table Maintenance) now includes selection options to control how certain point of sale documents (ex: unit sales) are viewed in MyAccount.

Selection options are:
*   **Show All:** Displays both transactions and the PDF version of the invoice.
*   **Hide All:** Does not display transactions or PDF version of the invoice.
*   **Hide: HTML view only (for future use).**
*   **Hide: PDF view only:** Displays the transactions, but no PDF version of the invoice.
> **Note:** If any option other than Show All is selected, the customer will not receive an email version of the POS invoice.

### Destination Based Sales Tax (DBST) – Monthly Update Change Notice

A new process has been added to DBST monthly tax update. This process will automatically add sales code overrides for tax codes that are new or are missing overrides, within the same state. This makes it so you do not have to manually check overrides in any new tax codes created for states to which you subscribe. This will help in case, for example, a new jurisdiction is created because of tax requirements and goes unnoticed until your dealership runs a tax report and you are unable to figure out why the tax is wrong – or you have created an override for one particular tax code (perhaps the one where your store is located) and you have forgotten to copy that override to the rest of the state. Note: With this change, however, if you set up an override incorrectly in one tax code for the state, this process will copy it into all locations within the state.

### Standard Customer Name Index - Phone Number Added

With R17v8, the standard lookup screen for customer names has been enhanced to allow customer searches by secondary phone numbers (work phone, fax, and extra phone numbers entered in Contacts).

The standard lookup screen for customer names is currently tied to the following:
*   Electronic Bar Code Label Configuration
*   Split Charge Configuration
*   Receivables Inquiry
*   Receivables Maintenance
*   PO Variance Report
*   Payables Vendor Inquiry
*   Payables Vendor Maintenance
*   Correct Due Dates and Discounts
*   Payables Invoice Entry
*   Time Clock Maintain Employee Master
*   Inquire/Update Units
*   Unit Orders
*   Sold Units Inquiry
*   Finalize Stock Order with Enhanced PO's
*   Address Inquiry
*   Address Maintenance
*   Point of Sale
*   POS Document List
*   Part Sales History
*   Price Table Maintenance
*   Point of Sale Profitability Report
*   CNH Dollar Volume Summary Report

With this new feature, on the Point of Sale entrance screen, you can now supply a complete or partial phone number to access the lookup screen. In other applications, a partial name is used to access the lookup screen and then the complete or partial phone number is supplied at the top of the lookup screen to search by phone number.

When searching by phone number, the lookup screen will display the type of each phone (Phone #, Phone #2, Fax, or other Contact's label). Note: When the lookup screen is sorted by name and unfolded, only the primary phone and 'Phone #2' will display. When the lookup screen is sorted by phone and unfolded, only one of the phone numbers will display on the first line of each entry.

Customers will not display on the lookup screen if they are excluded because of other opts (cash customer opt, display other divisions opt).

This enhancement could impact performance on older systems. If you would prefer to search only by the primary phone number and forego the new enhancement, please contact the DIS Response Line.

*Updated 01/22/2014*


title: "Part Supersession"
source: "Part_Supersession.pdf"
tags: ["Part Supersession", "Inventory Management", "Keystone", "DIS", "Parts Posting & Maintenance", "Parts Inquiry", "POS Invoicing", "Supersession Chain", "Vendor Configuration"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "A technical guide on managing part supersessions within the DIS Keystone system. It covers how to manually enter, view, and configure the system to search for forward and backward supersession information."
long_description: "This document provides comprehensive instructions for handling part supersessions in the DIS Keystone software environment. Part supersession is the process of replacing a part with an interchangeable one, forming a supersession chain. This guide details the manual entry of supersession data through the 'Parts Posting & Maintenance' module. It explains how to view these supersession chains, including both backward (older parts) and forward (newer parts) replacements, using the 'Parts Inquiry' screen and directly within 'POS Invoicing'. A key focus is on system configuration; the document outlines the steps to set specific OPT (Option) settings in the 'Point of Sale Menu' to enable alerts for backward supersessions. Additionally, it instructs on how to configure vendor settings to allow the system to search for backward supersession information provided by a price book. The guide includes screenshots and step-by-step procedures to assist users in effectively managing their inventory by leveraging the full capabilities of the supersession functionality."