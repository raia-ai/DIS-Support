---
title: "Reprint POS Posting Edit List Report - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Reprint POS Posting Edit List Report - AG Internal."
long_description: "This document provides internal system administration information about Reprint POS Posting Edit List Report - AG Internal."
---

_Reprint POS Posting Edit List Report - AG Internal_

Issue 

 The printer failed while the POS Posting Edit List was printing, and the print job was lost. 

  

 Solution 

 Use Transaction Report Writer to reproduce the report. 

 Note : This works best from a green-screen session. 

   

 Create a Detailed Report 

 Select Transaction Report Writer (Accounting | Transaction Menu | Transaction Report Writer) . 

   

 Press Enter to advance to the next screen. 

   

 Type 01 (General Ledger) in the Enter no. and Enter number of subtotals desired fields, then press Enter . 

   

 Type 02 (Post Date) on the first line of the Field No . column and the posting date in the Constant column using the MMDDYY format. 

 Tab to the next line and enter 03 (Document #) in the Filed No. column and 8 wild cards (exclamation points) followed by #* (Automatic POS postings) in the Constant column as shown above. 

  

 To Print Report for Single Division 

 Tab to the third line and type 05 (Account #) in the Field No. column and the Division code followed by 7 wild cards (exclamation points) in the Constant column. 

   

 Press Enter to save the settings, then press F2 to continue to the Sort specifications screen. 

 Type 03 (Document #) on the first line of the Field No. column and ten 1’s in the Sort Order column as shown above. 

 Press Enter , then F1 to run the report. 

  

 Print a Summary Report 

 On the Specify Parameters screen Type Y in the Enter Y for a summary report field at the bottom of the screen. 

   

 Press Enter . Provide the following information on the Field Selection screen. 

   

 Pres Enter , then F2 to set sort opts. 

   

 Type 05 (Account #) on the first line of the Field No. column and eight 1 ’s in the Sort Order column as shown in the screen shot above. 

 Press Enter to save the settings, then press F1 to run the report.