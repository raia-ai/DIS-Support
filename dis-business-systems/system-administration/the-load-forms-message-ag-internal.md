---
title: "The Load Forms Message - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about The Load Forms Message - Ag Internal."
long_description: "This document provides internal system administration information about The Load Forms Message - Ag Internal."
---

Introduction 

 Every print job created in the AS/400 operating system has a specific ‘Form type’ assigned.  The Load Forms message is generated to remind the user to load the correct paper into the printer as different print jobs are created. 

 Reports aren’t printed on check stock, and checks aren’t printed on plain paper. 

 Here are examples of the different form types and how they are used. 

 *STD (Standard) 

 All user reports (accounting, parts, units…) 
 All POS jobs (Sales Orders, Work Orders, Purchase Orders, Quotes, Rental Contracts, Rental Agreements) 

 CHK_LASER (Checks / Laser format) 

 All checks processed through Payables 

 CHK_LSR (Checks / Laser format) 

 All checks reprinted from Archiving.  Notice the slight differences between the form type when printing from Payables vs printing from Archiving. 

 CHKS (Checks / Dot matrix format) – rarely (if ever) used 

 All checks directed to a dot matrix printer through Payables 

 STMT_LASER 

 All Statements and Interim Statements printed through Receivables. 

 STMT_LSR 

 All Statement jobs reprinted from Archiving.  Notice the slight differences between the form type when printing from Receivables vs printing from Archiving. 

 Labels 

 Labels 

   

 There are two reasons why the Load Forms message is generated: 

 The business system was started or restarted.  In either case, each initial job sent to a specific printer is the handled as the First Job Ever Sent To That Printer.  The system gives the user the opportunity to verify / load the correct paper before that report is sent to the printer. 
 A job was sent to the printer using a different form type than the previous job sent to that printer, with that ‘previous jobs’ load forms message being answered with a G .  

 Possible responses to the Load Forms message are: 

 G - Begin processing the current file after loading the form type. 

 This tells the system that the requested form type has been loaded.  The system will attempt to print that job, and any other jobs that are sent to that printer that also require that form type. 

 B - Begin processing the current file after loading and aligning the form type. 

 Very much like ‘G’ but designed more for the S/36 OS. 

 I - Ignore the request to load the form type.  Print the file on the current form type. 

 This tells the system that you don’t care what type of paper is in the printer, print the job on whatever paper is loaded.  The system will print ONLY that ONE job. 

 H - Hold the file and print the next file on the output queue. 

 This holds the print job.  Not usually a desirable option, since the goal is typically to print the job, not hold the job. 

 R - IBMs explanation for this is very long.  The short version is this: We Don’t Take an R . 
 C - Cancel the writer. 

 This will end the print writer.   This is not a good response, as it ends the print writer and results in a call to the DIS Response Line – “Help, I can’t print”.  We Don’t Take a C . 

  

 The response to the message determines what happens with subsequent print jobs. 

 The two responses generally used by DIS customers are G and I . 

 Scenario 

 Printer P1 is in the accounting office.  It’s used to print Reports, Invoices, Checks, and Statements. 

 A user sends an invoice or a report to P1.  When the job hits the output queue the message reads: 

 “Load form type '*STD' device P1 writer P1.” 

 The user will verify the printer has plain paper loaded, then answer the message with a ‘G’. 
 The first job will print. 
 If there are additional print jobs that also have a form type of *STD, those jobs will also print. 
 If there are no additional print jobs waiting, the next job that is sent will print without prompting, provided it also has a form type of *STD.  Invoices and Reports both have a form type of *STD so those jobs will continue to print without prompting. 

  

 Then let’s say a while later the user sends a check from Accounting / Print Payable Checks to P1.  When the job hits the output queue the message will read: 

 “Load form type 'CHK_LASER' device P1 writer P1.” 

 The user will load check stock into P1, then answer the message with a ‘G’. 
 The check(s) will print.  1 check or 101 checks, it’s all one print job so the message will only need to be answered once. 
 If the user sends another check job to P1 that job will print without prompting, due to the answer of ‘G’ on the previous check job. 
 When a Report or Invoice is sent to P1 the Load Forms message for *STD will be generated yet again.  The user will verify the check paper has been removed from the printer and will answer the message with a ‘G’. 

 Statements 

 When Statements are created, a load forms message for STAT_LASER is generated.  If the user prints statements on plain paper, as most DIS customers do, the user can choose one of these two options: 

 Answer the message with a ‘G’.   This tells the system the printer now has STAT_LASER paper loaded and the statement job will print. 

 When the next Report or Invoice is sent to that same printer another load forms message will be generated, this one for *STD paper.   The user will need to answer that with a ‘G’. 

 Answer the STAT_LASER load forms message with an ‘I’.  This tells the system that the user is not changing paper but chooses to print the job on the paper that’s currently in the printer.  The statement job will print. 

 Because the message was answered with an ‘I’, when a report or invoice is sent the user will not have to answer another message – the report/invoice will print. 

 In simple terms, the most common answer to the load forms message for Statements is ‘I’, and that is the only message that will need to be answered.