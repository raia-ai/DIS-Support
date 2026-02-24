---
title: "CLAAS Parts Inventory Management"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about CLAAS Parts Inventory Management."
long_description: "This document provides information about CLAAS Parts Inventory Management from the DIS Quantum system."
---

## Introduction

CLAAS Parts Inventory Management (PIM) allows you to maintain a consistent inventory level for CLAAS parts through part file transfers between your dealership's system and CLAAS. (Click here for a breakdown of files sent to and received from CLAAS.)

This document provides details on configuration, how to view the status of orders and resend if necessary, work with suggested transfers, and generate the Suggested Stock Orders Report.

## Configure CLAAS Communications

In order to enable PIM communications, a Warehouse Group Code and a Warehouse Code must be provided. There is also an option that can be selected to download the CLAAS files every Sunday at 10:15 p.m. if you do not normally schedule backup on Sundays. Setup will be completed with DIS assistance.

1.  Select **Electronic Commerce Configuration** (`Security | Electronic Commerce | Electronic Commerce Communication`). The Electronic Commerce Communication screen opens.
2.  Click the **Add** button. The Add Vendor/Comm Package screen opens.
3.  Provide information in the available fields and click **OK**. The CLAAS Communications – Configure screen opens.
4.  Type the Dealer Number supplied by CLAAS in the **Inventory Dealer Number** field. This is for the current inventory download.
5.  Type the Warehouse Group Code provided by CLAAS into the **Warehouse Group Code** field. There is only one code per file set. Once it has been entered in one division, the number supplied will be verified for a match when new divisions are configured in the same file set.
6.  Type the Warehouse Code provided by CLAAS into the **Warehouse Code** field. Each individual division will have its own unique warehouse code.
7.  The **Sales History** field is the number of days of sales history considered when generating the Transactional Demand file. This field defaults to 1095 and cannot be changed until you have been using the system for a while and only with CLAAS authorization.
    > **Note:** This field only displays for the first division that is configured and is controlled by that division. For that division, the warehouse code will match the last portion of the Warehouse Group Code.
8.  Select the **Set Sunday job?** check box and click **Enter**. The CLAAS Sunday Download is configured.
    > **Note:** This field only displays for the first division that is configured and is controlled by that division. For that division, the warehouse code will match the last portion of the Warehouse Group Code.

## Configure Vendor Maintenance - Inventory

This is standard Vendor Maintenance configuration where Vendor/Class combinations are entered to identify the part classes to be considered when generating and sending CLAAS part inventory files.

1.  Select **Vendor Maintenance-Inventory** (`Manufacturers | CLAAS | Vendor Maintenance-Inventory`). The Vendor Maintenance screen opens.
2.  Do one of the following:
    *   Click the **Add** button. The Add/Vendor Class screen opens.
        *   Either enter just a Vendor code to consider all parts from that vendor when generating part files or enter a specific Class to only consider parts from that class when generating part files. You can only do one or the other for each vendor.
    *   Select a Vendor/Class from the table and click the **Delete** button. The Confirm Delete screen opens.
        *   Click **Yes** to remove the class from the table.

## Configure Vendor Maintenance - PIM

Vendor Maintenance – PIM allows you to designate the vendor that the parts are ordered from and the expected time between ordering and receiving parts from the vendor.

1.  Select **Vendor Maintenance - PIM** (`Manufacturers | CLAAS | Vendor Maintenance - PIM`). The Vendor Maintenance screen opens showing the existing vendor maintenance entries.
2.  Do one of the following:
    *   Click the **Add** button. The Add/Vendor Class screen opens.
        *   Any vendor can be added. Multiple classes can be added for a given vendor. Leaving the class field blank will add all classes. The program will not allow adding a vendor with a class if that vendor has already been added with the class field left blank. It also does not allow the same vendor/class combination to be added twice.
        *   Enter C in the **Order From Code** field to designate the parts are ordered from CLAAS.
        *   The **lead time** is the expected time (in days) between ordering and receiving parts from the vendor. CLAAS usually uses a default of 7 days.
    *   Select a Vendor entry from the table and click the **Delete** button. The Confirm Delete screen opens displaying the Vendor/Class entry that you are about to remove.
        *   Click **Yes** to remove the entry from the table.

## View Status of Submitted Part Inventory Files

Part Inventory files are automatically generated and sent after every scheduled backup. You can check the status of each submission and resend it if it failed. (Click here for a breakdown of files sent to CLAAS.)

1.  Select **Resend/Review Log** (`Manufacturers | CLAAS | Resend/Review Log`). The Send List screen opens displaying the files that have been sent.
2.  Review the statuses of the submitted inventory files in the table. If a submission did not go through for any reason, it will have a **Failed** status. The file will automatically be sent again at 9 a.m. the next morning.
3.  To manually resubmit the file, highlight it and click the **Resend** button to submit the inventory file again.

## View Files Received from CLAAS

You can view when part inventory files were sent to your dealership from CLAAS and whether or not the submission was successful. (Click here for a breakdown of files sent to CLAAS.)

1.  Select **Resend/Review Log** (`Manufacturers | CLAAS | Resend/Review Log`). The Send List screen opens.
2.  Click the **Receive List** button. The Receive List screen opens showing when you received the files and whether or not the submission was successful. This screen is informational only.

## Suggested Stock Orders

Parts for suggested stock orders are selected on the CLAAS/Syncron website. You will then download the parts to Quantum in an Order Export File. Downloaded parts will continue to be added to the order until the order is finalized or deleted. Stock orders are accessed, edited, and finalized as per normal processes.

Orders created by the system will begin with CLA, then the division code, then a four-digit number.
**For Example:** CLAD0081

## Suggested Transfers

The Work with Suggested Transfers option allows you to view, print, change, delete, or complete an outgoing transfer. You can also view the parts on an incoming transfer and change the quantity if desired. Transfers created by the system from the Order Export file will start with CLT, then the division code, then a four-digit number.
**For Example:** CLTA0017

### Outgoing Transfers

1.  Select **Work with Suggested Transfers** (`Manufacturers | CLAAS | Work with Suggested Transfers`). The Manufacturer Suggested Transfers screen opens displaying suggested transfers for select manufactures.
2.  Select the transfer from the table that you would like to work with and do one of the following:
    *   Click the **Display** or **Change** button. A screen opens listing the parts on the transfer.
        *   If you want to change the quantity of parts to be transferred, click on the current quantity, type in the correct quantity, and click **Enter**.
    *   Click the **Transfer** button to process the suggested transfer. The Confirm processing of Transfer Parts screen opens.
        *   Verify this is the transfer that you want to complete and click the **OK** button.
    *   Click the **Delete** button to remove the transfer from the system. The Confirm Deletion of Parts Transfer screen opens.
        *   Click the **OK** button to confirm the deletion. If you press Enter on your keyboard, the deletion process will be cancelled.
    *   Click the **Print** button, then click **OK** on the screen that opens to print the suggested transfer.

### Incoming Transfers

1.  Click **View Incoming Parts** on the Manufacturer Suggested Transfers screen.
2.  The View Incoming Parts screen opens displaying the parts on incoming transfers.
3.  Do one of the following:
    *   To change the quantity of a part being transferred to your dealership, select the part line in the table and click the **Change Qty** button. On the screen that opens, type the new part quantity over the old part quantity and click **Enter**.
    *   Click **Print** to print out the parts on the incoming divisional transfer.

## Print Suggested Orders Report

The Suggested Order Report lists suggested stock orders uploaded to a single division or all divisions on the date you specify. It also lists any parts that were provided by CLASS as part of a suggested stock order that were not included in an automatically generated order.

1.  Select **Print Suggested Orders Report** (`Manufacturers | CLAAS | Print Suggested Orders Report`).
2.  Enter a code in the **Division** field or leave it blank to run the report for all divisions that have PIM enabled.
3.  Enter the **Date** that you want to consider when generating the report.
4.  Click **Enter**. The report is printed if the **Hold Print?** check box was not selected. Otherwise it will be generated into the Report Center in Systems.

The report shows the division, the upload date you requested, the orders that were generated with the number of lines, the CLAAS Order description, and any items that were sent but not put in an order.

*   The CLAAS order description is included for reference as CLAAS breaks down their order types differently than Quantum.
*   Parts that were not ordered are listed at the bottom of that specific order, as well as the reason they were not shipped.
*   Parts that are not included in the order have a reference number (Vendor CLAAS Document ID) listed on the same line to be used for reference if you need to contact CLAAS about the order.
*   If there were no suggested orders on the date you specified, a message displays stating **"Nothing Uploaded on date selected."**
*   If CLAAS sends suggested orders or transfers to a division not configured in ECC, that division will be listed on a separate page with a blank division field. It will state "Items Not Ordered" and provide the reason as **"Supplier Warehouse 00000xxxxx not configured."** Additionally, items to be transferred to that division will show as Items Not Ordered under the transferring division with the same reason provided.

> **Note:** The report is cumulative, so if the report is printed at 10 a.m. and 4 p.m., the report will include all of the data in the 10 a.m. report.

## View Relevant Items Report

The Relevant Items report is automatically generated and printed every Friday night on the default printer that you specify. The report lists parts in the Relevant Item file by CLAAS that are currently not in your divisions inventory. This allows you to decide whether or not to add them.

*   If a part on a suggested stock order from CLAAS is not in the divisions inventory, other divisions assigned to the CLAAS PIM, or the CLAAS Price Book, it is listed in the report with a message of "No Data Found".
*   If a part on a suggested stock order is listed in the inventory of another division or in the Price Book, it will be listed on the report with one of the following codes:
    *   **DVx** - x equals the division that has the part in its inventory.
    *   **PB** - indicates the part is currently listed in the Price Book.

## Overview of Files Exchanged in Process

### Files sent to CLAAS
These files are automatically generated and sent after every scheduled backup allowing CLAAS to generate an accurate stock order. Only data for parts from vendors that are added into CLAAS PIM in the vendor maintenance screens will be included.

*   **Purchase Order Files** – These files list the parts on open stock orders coming into your dealership and parts scheduled to be transferred from other dealerships. Parts from transfers will be listed until the transfer is complete or deleted.
    > **Note:** Open orders are stock or emergency orders that are finalized but not yet completely received as well as the CLAAS suggested stock orders that are not finalized.

*   **Transactional Demand Files** – These files list part sales over the last 3 years or those scheduled to be transferred to another dealership. Part transactions must be closed and posted to be listed. Parts on manually created transfers and those generated from inventory management continue to be listed until the transfer is closed or deleted.

*   **Dealer Item Files** – These files are used in sending part sales information and providing part sales forecasts. They provide your current stock information to CLAAS including:
    *   All parts with a stock quantity above zero, including reserved parts.
    *   All parts listed in the Transaction Demand file.
    *   All parts listed in the Purchase Order file.
    *   All parts listed in the Relevant Item file.

### Files Received from CLAAS
Your system receives 2 files from CLAAS that provide suggestions for parts well as a suggested stock order. The files are as follows:

*   **Relevant Item File** – These files contain items that CLAAS believes should be in your dealerships item file and is requested by your system every Friday night from 8 PM until 5AM Saturday morning. If you do not run the job or the job fails while running, the last time the file was run successfully continues to be used.
*   **Order Export File** – These are unfinalized suggested stock orders from CLAAS. The system checks for suggested parts and generates a new order if the vendor has been designated for PIM. Parts are grouped together by vendor and CLAAS order types. This file also includes suggested transfers between divisions which are treated as open orders and pending transfers when creating the open order file to send to CLAAS. If the suggested transfers are not sent in the Open Order file, CLAAS will resend the same suggested stock order every day.


title: "Clearing Your Browser Cache"
source: "Clearing_Your_Browser_Cache.pdf"
tags: ["Browser Cache", "Google Chrome", "Mozilla Firefox", "Internet Explorer", "Safari", "Troubleshooting", "Web Browsing", "Cache Clearing", "IT Support"]
version: "1.0"
last_updated: "2024-05-22"
short_description: "A technical guide providing step-by-step instructions for clearing the browser cache in Google Chrome, Mozilla Firefox, Internet Explorer, and Safari. The document explains why clearing the cache is necessary for resolving display and loading errors."
long_description: "This document, created by Dealer Information Systems (DIS) Corporation, serves as a comprehensive guide for users on how to clear their browser cache. It begins with an introduction explaining the purpose of a browser cache—to store code and images to speed up subsequent visits to websites. It then details the problem that can arise when cached files become corrupted, leading to incorrect loading of web pages. The guide provides clear, sequential instructions for the most common web browsers: Google Chrome, Mozilla Firefox, Internet Explorer, and Safari. Each section includes keyboard shortcuts (Ctrl+Shift+Delete) to access the relevant clearing menu, screenshots of the user interface to guide the user visually, and specific instructions on which checkboxes to select (e.g., 'Cached images and files,' 'Temporary Internet files') to ensure the cache is properly cleared. For Safari, it provides two distinct methods: deleting all browsing data and specifically clearing the cache via the Develop menu. The document is designed to be a user-friendly troubleshooting resource."