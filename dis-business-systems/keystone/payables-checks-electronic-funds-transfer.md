---
title: "Payables Checks Electronic Funds Transfer"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Payables Checks Electronic Funds Transfer."
long_description: "This document provides information about Payables Checks Electronic Funds Transfer from the DIS Keystone system."
---

## Introduction

The DIS Payables Checks application allows Keystone dealers to create a file when printing checks that can be uploaded through a secure Internet portal to an Electronic Funds Transfer (EFT) processing vendor, such as FreedomWare (http://www.freedomware.net). (FreedomWare is only available to U.S. dealers.) An Automated Clearing House (ACH) transfer from the dealership's bank account will be made to each payable vendor's bank account and an email will automatically be sent to the vendor with check stub information attached in the form of a PDF file.

This feature requires:
- Laser Payable Checks (Electronic Forms)
- EasyFile
- Archiving
- iSeries on V5R2 or above

## EFT Configuration

EFT Configuration is available in both Vendor Maintenance and Vendor Inquiry.

1.  Select Vendor Maintenance (`Accounting | Payables | Vendor Maintenance`) or Vendor Inquiry (`Accounting | Payables | Vendor Inquiry`) from the Keystone main menu.

2.  Provide a vendor address and click **Enter**. One of the following screens opens, where you will find the **EFT Configuration** button.

    - **VENDOR MAINTENANCE - Screen #1**
    - **VENDOR INQUIRY - General Information**

3.  Click the **EFT Configuration** button. After passing through the security gate, the Vendor Maintenance – EFT Configuration screen opens.

    *[Image: VENDOR MAINTENANCE - EFT Configuration screen showing fields for bank details and email addresses.]*

    A payables check created for this vendor will print as usual if the Active check box is unselected. A record in the Payables EFT upload file will be transferred to an EFT processing vendor or bank if the Active check box is selected. If you select the Active check box, you must also supply the Bank Name, Name on Bank Account, Routing Number, Account Number, Checking or Savings.

4.  Select the **Active** check box to activate EFT check transactions for this vendor.

5.  Type the bank name for this vendor's Payables EFT transactions in the **Bank Name** field.

6.  Type the vendor's name as it appears on the bank's records in the **Name on Bank Account** field.

7.  Type the vendor's bank routing number for EFT check transactions in the **Routing Number** field.

8.  Type the vendor's bank account number to use for EFT checks in the **Account Number** field.

9.  Select **Checking** or **Savings** to designate the account type for EFT transactions.
    > **Note:** All bank account information is encrypted.

10. Supply a **From Email** address and up to five **To Email** addresses.

11. Click **Enter** to save.

## EFT Check Box in Print Payable Checks

On the Adjust Vendors screen reached through Print Payable Checks (`Accounting | Payables | Print Payable Checks`), you will notice the EFT check box in the last column of the table.

*[Image: PRINT PAYABLE CHECKS - Adjust Vendors - Include screen, with the EFT column highlighted, showing checkboxes for vendors AGCO CORP and AL'S MACHINE SHOP.]*

The EFT check box is automatically marked for vendors that have provided bank information and selected the Active check box in EFT Configuration. You can remove the vendor from receiving EFT transactions by unselecting the EFT check box. This will result in the vendor having a check printed for them instead of depositing the funds in their bank account. If you try to Select the EFT check box on this screen and the vendor DOES NOT have bank information listed or the Active check box selected in EFT configuration, an error message appears and the system will not allow you to continue until EFT is unselected.

### Printing Payable Checks

A batch of checks can include both those that are set for EFT transactions and those that are not. The first time a vendor is paid through an EFT transaction, the check will process as a normal check so that the EFT account information can be verified. This initial EFT transaction is considered a pre-notification transaction. After the information has been verified by the EFT processor, the next EFT check that is processed for that vendor will go through as an EFT transaction. Any time EFT account information is changed for a payables vendor, that vendor will have to conduct another pre-notification transaction.

For each EFT check that is processed, a transaction will be created in a temporary file that will include the appropriate EFT bank information. The amount will be the net amount.

## PDF File and Email Attachment

For each EFT transaction, a PDF file is created. The file contains the same information that would print on a check stub for a normal payables check. The PDF file is attached to an email sent to each “To Email" address set up in EFT Configuration, as well as the "From Email” address. The email will let the recipients know an EFT transaction from your dealership has been processed for them and refers them to the PDF file attachment.

The PDF file will automatically be added to the EasyFile directory under each vendor's address number. If the email is not sent for some reason, a copy of the PDF file with the check stub information is saved and can be manually attached and sent in an email, or printed and sent to the vendor through the mail.

The path where the PDF file is stored is:
```
\\keystone\keystone\mypictures\filesetX\AP\addr#\CHECK\EF999999 (where filesetX = user's fileset, addr# = vendor address number, EF999999 = check#).
```

The name for the PDF file will be in the following format:
```
EF999999_20130501.pdf (yyyymmdd).
```

To have the email delivered automatically, the iSeries server must be properly configured to generate emails. Contact the DIS PC/Net Response Line for assistance with configuration.

A sample PDF email attachment is displayed below.

```
05/09/13                          EFT Payment Information                         Page: 1

Payer: BELLINGHAM TRACTOR
       1234 MAIN STREET
       PO BOX 1234
       BELLINGHAM, WA 98225

Payee: AGRO MARKET CORP
       PO BOX 4321
       TACOMA, WA 98328

Inv Date   Invoice#   Unit #      Amount      Discount    Net Amount
----------------------------------------------------------------------
5/01/13    IV00003                25.00                   25.00

           Totals :               25.00                   25.00


AGRO MARKET CORP             Customer account number: ADAMSAL
```

## Enter Manual Checks

The option to process a manual check as an EFT transaction is also available in Enter Manual Checks.

1.  On the Check Information screen reached through `Accounting | Payables | Enter Manual Checks`, unselect the **Print Check?** check box and select the **EFT check?** check box.
    > **Note:** You must have the vendor setup in EFT Configuration in order to select the EFT Check? check box.

    *[Image: ENTER MANUAL CHECK - Check Information screen with the EFT Check? checkbox selected and a message "EFT information is not configured or is not active for this vendor." displayed at the bottom.]*

2.  When you unselect the **Print Check?** check box, the **Check Number** field allows you to provide a number for the check.
    > **Note:** When a manual EFT transaction is processed, the check number entered in this field will be used as the reference number. The EF999999 sequencing number used for Print Payable Checks will not be used in Enter Manual Checks.

3.  Type the amount for the check in the **Check Amount** field. Process the manual check as normal. After you have selected invoices to be paid by this check, you are returned to the Vendor Selection screen.

A 'Y' appears in the EFT configuration column for each vendor who has the EFT Check box selected on the **ENTER MANUAL CHECKS - Vendor Selection** screen. When the manual checks are posted, the PDF file is created and sent to the emails setup in EFT Configuration. The file contains the same information that would print on a check stub for a normal payables check. The PDF file will automatically be added to the EasyFile directory under each vendor's address number. If the email is not sent for some reason, a copy of the PDF file with the check stub information is saved and can be manually attached and sent in an email, or printed and sent to the vendor through the mail.

## EFT Check Register Report

The EFT Check Register report is generated with detail information for the EFT vendors that are processed. The report is created in the archiving files for later review and retrieval.

## EFT Transaction File Processing

After payables checks have been processed, if any EFT transactions have been added to the temporary file, this file will be copied to the IFS as a CSV (comma separated value) data file named `X127_EFT.csv` for Print Payable Checks and `X128_EFT.csv` for Manual Checks.

This file will be saved to the following path:
```
\\keystone\Keystone\Export\"as400 user signon"\
```
If the file already exists, it will be replaced with the current file.

> **WARNING:** The CSV file is not secured. It must be manually copied from the IFS to your local PC. It must be deleted manually from the IFS directory to ensure that only those with authorization access the file. This can be done through Windows Explorer.

You are then able to log onto the Internet portal provided by your ACH processing vendor, and upload the file to be processed by that vendor for the EFT transactions to be created and transferred. The specifics of this process will be dictated by the EFT processing vendor or bank. In some cases, the EFT processing vendor can request to have this file emailed to them or given to them directly on a form of media.

## Verification Reports

Your ACH provider should give your dealership a verification report indicating which transactions were processed with each EFT batch. This report should include a list of those vendors whose transactions could not be processed or verified because of faulty routing or account numbers.

If routing or account numbers could not be verified, you will need to go back into Vendor Maintenance and correct the information. By changing the information on the EFT Configuration screen, the Verification flag will be set off, and the vendor will be set up to be added to the next payable checks EFT batch as a pre-notification transaction again.

## DIS Keystone Payables Checks EFT Export File Layout

The information below is available for you to pass on to your bank or ACH provider as the file specifications necessary to process payables EFT checks.

The following is a description of the ASCII text file that can be used to export transactions from the DIS Keystone Payables Checks application.

ASCII Comma Separated Values (CSV). Each field will be enclosed in double quotes (“) to allow commas and other characters if applicable and still be separated with the comma delimiter.

| Field | Title | Max Character | Format |
| :--- | :--- | :--- | :--- |
| 1 | **Payables Vendor ID** | 15 | Alpha Numeric |
| | *This is the Vendor ID field used to identify the vendor in Payables Applications.* | | |
| 2 | **Name on Bank Account** | 20 | Alpha Numeric |
| | *This is the name the vendor uses on their bank account.* | | |
| 3 | **Routing Number** | 9 | Numeric |
| | *Routing Number - Valid 9 digit long bank routing number.* | | |
| 4 | **Account Number** | 17 | Numeric (No spaces or dashes) |
| | *The bank account number associated with the Routing Number.* | | |
| 5 | **Amount** | 11 (including decimal) | Numeric (99999999.99) |
| | *The amount of the transaction. Include cents with a decimal.* | | |
| 6 | **Checking or Savings** | 2 | 22 for checking / 32 for savings |
| | *This field designates whether the account number is for checking or savings.* | | |

A pre-notification transaction may be sent for 0.00 dollars to verify the routing number and account numbers specified. In this case, the amount field must be 0.00 and the Checking or Savings field will have a 23 for Checking (instead of 22) or 33 for Savings (instead of 32).

Each transaction in the CSV file will end with one carriage return (OD) and one line feed (OA). These ASCII characters are typically included by most accounting CSV export programs.

### Sample File

```csv
"RODRIG","ALEX RODRIGUEZ","325180184","78738748987349874","0.00","33"
"SLESK2","BILLY SLESCK","325170631","88873888838788887","0.00","23"
"CASE01","CNH CORPORATION","325180113","8009896083","999.99","32"
"FORD01","FORD TRACTORS","325180142","8734536733","1500.23","22"
```


title: "Perform a Complete System Save"
source: "Perform_a_Complete_System_Save.pdf"
tags: ["System Save", "System Backup", "AS/400", "iSeries", "DIS", "Keystone", "Data Backup", "Disaster Recovery", "INZTAP", "INZOPT"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "A procedural guide on how to perform a complete system save (backup) for DIS/Keystone systems running on AS/400 or iSeries. It covers preparation, tape/optical media initialization, and the step-by-step save process."
long_description: "This document provides detailed, step-by-step instructions for performing a Complete System Save, also known as a System Backup, for DIS (Dealer Information Systems Corporation) and Keystone systems. A complete save is a critical procedure for disaster recovery, backing up all business data, queries, user profiles, hardware configurations, business system programs, and the operating system. The guide outlines the importance of performing this backup before and after major hardware or software changes and recommends a schedule of at least every six months for routine maintenance. It covers initial preparation steps like deleting old backups, calculating the required number of tapes by analyzing system storage, and initializing media for both tape drives and optical drives using commands like INZTAP and INZOPT. The main procedure involves using the system console, navigating AS/400 menus (GO SAVE), and configuring command defaults for single-tape, multi-tape, and optical drive scenarios. Finally, it provides instructions for verifying the save and important best practices for handling and storing backup tapes to prevent data loss and ensure data integrity."