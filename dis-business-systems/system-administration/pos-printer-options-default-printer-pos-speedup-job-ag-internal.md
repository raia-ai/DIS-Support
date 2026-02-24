---
title: "POS Printer Options Default Printer / P.O.S. Speedup Job - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about POS Printer Options Default Printer / P.O.S. Speedup Job - Ag Internal."
long_description: "This document provides internal system administration information about POS Printer Options Default Printer / P.O.S. Speedup Job - Ag Internal."
---

_POS Printer Options Default Printer / P.O.S. Speedup Job - AG Internal_

Introduction 

 This article provides an overview regarding assigning default printers on the P.O.S. Printer Options screen, the DISPSP xxx job process, and a solution to the issues arise when multiple users assign the same printer as their default printer. The Point of Sale Printer Options screen was originally set up to only configure dot matrix printers and just listed the Default printer field at the top of the screen. When laser printer use became more common, the Electronic Forms section was added to the bottom of the Printer Options screen for configuring Laser Printers as shown below. 

 

 If a dealership tries to print a Laser Form that has not been enabled in Laser Form Configuration (Security | Laser Form Configuration) as shown below, the system will send the document to the default dot matrix printer. 

 

 This often confuses the end user.  For instance, considering the first screen shot above, they may think My Default printer is set to P2.  Why are my invoices printing on P1?  with the answer being they have laser forms enabled and the Default Printer is not actually their default. 

  

 Issue 

 Regardless of whether laser forms are the default/enabled for a dealership, a default dot matrix printer must be assigned in order to start the DISPSP xxx job (P.O.S. speedup job) which controls the background process required for updating part reservations, removing parts from inventory, and printing. 

 Note : The last three characters of DISPSP xxx indicate the printer’s name and Fileset. For instance, DISPSP P2A indicates printer P2 and Fileset A. 

 The P.O.S speedup job starts when a user clicks Enter on the Printer Options screen in Invoicing, providing the (dot matrix) Default Printer assigned does not already have a P.O.S speedup job running.  When an end user (User A ) begins the P.O.S. speedup job, they own the job for that printer and any invoices sent by any other users to that printer will appear in the print spool under User A ’s name until the DISPSP xxx job ends. 

  The DISPSP xxx job automatically ends when: 

 A user manually ends the job 
 The EOD process begins (this ends all P.O.S. jobs). 

 While this doesn’t present an issue for User A as their invoice prints as normal, any other user’s who sends a print job will NOT have their invoice print and the job is listed under User A . 

 For Example: 

 User A is the first to click Enter on the Printer Options screen.  User A owns the P.O.S. job. 
 User B tries to print an invoice to the same printer, but nothing prints.  When User B goes to My Printer Output to look for the cause of the problem, there isn’t a print job listed because it’s under username A . 

  

 

 To Find the Print Job 

 Select My Printer OutPut (System | My Printer Output) and do one of the following: 

 Press F14 on your keyboard, or 
 In Keystone , click Functions , then click Select other printer output , or 
 In Quantum , click the Select other printer output button. 

 Type *ALL  in the User field, specify the printer name (P2 in this example), and click Enter . 

 

 You can also enter WRKOUTQ in a command line and click OK . 

   

 Highlight the printer, and click the Work with button.  All jobs sent to that printer are listed.  Respond to the printer status as required. 

 Using a virtual printer in POS further complicates the POS printing process. 

 Example :  User A assigns virtual printer ZZ as the dot matrix default printer. 

 A POS speedup job called DISPSPZZ x is started. 
 All invoices sent by User A spool to ZZ and don’t print. 
 If User B goes assigns ZZ as their default dot matrix printer, when they print an invoice those invoices also spool to ZZ, along with the invoices sent by User A. 

 When User B goes to D P they won’t see any invoices. 
 User B won’t see the invoices when they go to Report Center unless they set the filters to show *All users. 
 Because all the invoice jobs look the same, it’s difficult to tell which invoice is for which user. 

  

 Solution 

 Create a virtual printer for each user.  VJ for user Jim, VN for user Nancy, and so on. 

 Add each virtual printer to POS / Table Maintenance / POS Printers (x52-10) and ENVP. 

 Have each user assign their own virtual printer as the Default printer in Invoicing and as the e-forms printer. 

 Note : This becomes harder to implement in a larger dealership environment, due to the large number of virtual printers created. 

 In Plevna Implements system, they have 8 virtual printers created for specific individuals as well as the standard NP printer (see below). 

 

  

 To Add Dot Matrix Printer 

 Select Point of Sale Printers (P.O.S. | Table Maintenance | Point of Sale Printers) . 

 

 Provide the Printer name and click Enter . 

 

 No changes are required on this screen and these values don’t apply when using laser printing.  

 Click Enter to add the printer.