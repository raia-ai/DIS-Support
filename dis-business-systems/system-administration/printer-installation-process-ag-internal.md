---
title: "Printer Installation Process - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Printer Installation Process - Ag Internal."
long_description: "This document provides internal system administration information about Printer Installation Process - Ag Internal."
---

_Printer Installation Process - AG Internal_

Introduction 

 This article details how to configure all printers using the same method, so that if one rep installs a printer, another rep can quickly/easily troubleshoot an issue with that printer. The process is as follows: 

 Create the device description 
 Add the printer to ENVP 
 Add the printer to POS Table Maintenance (x52-10) 
 Test the printer. 

  

 Create the Device Description 

 Create a KPS on the PC if the printer is connected via USB. 
 Use WRKDEVD to add a Text Description to the printer 

 OR 

 Use WRKDEVD *PRT if the printer is connected via ethernet and create the *LAN or LPR device as required by the printer make/model. 

 After creating the printer: 

 
 If *LAN , vary the printer on and start the print writer. 
 If LPR , turn off Separator Page: 

 
 
 On a command line type ENDWTR printer_name and press Enter . 
 On a command line type WRKOUTQ and press Enter . 
 Take the option to ‘Change’ the Output Queue. 
 Press F9 (all parameters), then page down twice. 
 Change ‘Print separator page’ from *YES to *NO and press Enter . 

 Note : There’s no need to restart the print writer for LPR devices as it automatically starts when enter is pressed after that last step. 

  

 Text Description 

 When troubleshooting printer issues, the Text Description provides the quickest and easiest way to gather info about how a printer is connected/configured and where it’s located.  You can use that info to quickly begin the troubleshooting process. 

 The Text Description should include the following: 

 The make/model of the printer 
 The location of the printer 
 The connection method: KPS, *LAN or LPR 
 The IP address if ethernet-connected 
 The letters NAT if a Network Address Translation table is in use 

 *NAT is a good description for *LAN devices that use NAT . 

  

 Examples 

 Lexmark b2422, Service Mgr - *LAN 10.3.123.21 (NAT) 

 OR 

 Lex b2422, Service Mgr, Baltimore - *NAT 10.3.123.21 

  

 Add the Printer to ENVP 

 This step allows users to select the printer for reports. 

 Click System / Work with DIS Report Printers . 
 Press F6 to add the printer. 

 The ‘text description’ field in ENVP is much shorter than the description field in WRKDEVD.  Because ENVP is for the User to select a printer, some of the info contained in the description isn’t 

 Note : If the AS/400 printer name is 2 digits, and the system assigns a S/36 name that does not match, change the S/36 name of the printer: 

 On a command line type CHGS36 and press Enter . 
 Take the option to change the S/36 printer IDs. 
 Page down – the printer you just added will be at the bottom of the list. 
 Change the S/36 name of the printer to match the AS/400 name. 
 Press Enter , then press Enter again to return to the main menu. 

  

 Add Printer to POS Table Maintenance (x52-10) 

 This step allows users to enter the printer in the Default Printer field of POS 

 Select Point of Sale Printers (POS | Table Maintenance | Point of Sale Printers). 
 Type the S/36 name of the printer and press Enter twice. 

 Important! If the printer is only used for checks, do not add the printer to ENVP or x52-10 because: 

 It does not need to be in ENVP because they don’t want users printing reports on check stock. 
 It will not be used for invoices so don’t add it to the POS Printers list. 
 Checks are assigned to a printer in e-forms and in Payables/Payroll by the user. 

  

 Test the Printer 

 After installing a printer, print an invoice from archiving to the new printer to: 

 Ensure the printer is configured correctly – correct IP address, device type, etc. 
 Start the printer writer and answer the load forms message so that the printer is active and ready for the customer to use. 
 Determine whether the printer is compatible.  Many printers will be compatible as ‘report’ printers, when plain text reports are being printed, but may not be able to handle the more advanced job that is a laser form doc. 

  

 The ACI to use: