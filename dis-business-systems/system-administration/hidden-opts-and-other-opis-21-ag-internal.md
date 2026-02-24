---
title: "Hidden OPTs and other OPIs #21 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #21 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #21 – AG Internal."
---

_Hidden OPTs and other OPIs #21 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 KEYDMREG

 
 future

 
 phone

 
 0

 
 Data Mine Payable Check Register query is not active

 
       
 1

 
 Data Mine Payable Check Register query is active

 
       
 2

 
 Data Mine Custom Check Register query is active

 
           
 
 KEYDMSLC

 
 future

 
 phone

 
 0

 
 Keystone Data Mine adds a comma between Unit Spec Lines.

 
       
 1

 
 Keystone Data Mine does NOT use a comma between Unit Spec Lines.

 
           
 
 KUBINV

 
 future

 
 phone

 
 0

 
 Kubota Invoices download is not enabled

 
       
 1

 
 Kubota Invoices download is enabled in Payables Invoice Entry

 
           
 
 KUBORDFN

 
 future

 
 phone

 
 0

 
 Finalize Kubota order upon exit whether submitted or not (default)

 
       
 1

 
 Only finalize Kubota order when submitted

 
           
 
 LABORJOB

 
 2.2

 
 Phone

 
 0

 
 The Job code field does not display in POS on a labor line. ( unless TKDLR=1 )

 
       
 1

 
 Job code field displays at POS labor line. Also used by Labor analysis report. ( see opt LARBYJOB )

 
           
 
 LARBYJOB

 
 2.2

 
 Phone

 
 0

 
 Labor Analysis Report does not break by job code.

 
       
 1

 
 Labor Analysis Report breaks by job code.  Part of Orton's CC roll in.  Also used by TK dealers.

 
           
 
 LSRSIGO

 
 Future

 
 Phone

 
 0

 
 2nd signature line on laser checks will print in the new location

 
       
 1

 
 2nd signature line on laser checks will print in the old location

 
           
 
 LETTERWR

 
 V8L0

 
 Menu

 
 0

 
 print name and salutation

 
       
 1

 
 print no name and no salutation

 
       
 2

 
 print name and no salutation

 
           
 
 LOGINSTL

 
 V8L4

 
 Menu

 
 0

 
 log printer is not installed

 
       
 1

 
 log printer is installed

 
           
 
 MAKMODAD

 
 future

 
 Phone

 
 0

 
 Allow F6 Add on Make Model Selection Screen

 
       
 1

 
 Do not allow F6 Add on Make Model Selection Screen

 
           
 
 MFG400

 
 2.1

 
 Menu

 
 0

 
 Electronic Commerce Communications is not installed.

 
       
 1

 
 Electronic Commerce Communications is installed.

 
           
 
 MICR8

 
 11.0 V.1

 
 Phone

 
 0

 
 Micr line on checks is limited to 6 digits

 
       
 1

 
 Micr line on checks is 8 digits

 
           
 
 MICRTSTC

 
 11.2 V1

 
 Phone

 
 0

 
 print test MICR check with test number of 123456 and print as Non-Negotiable

 
       
 1

 
 print test MICR check with the next real check number for the bank account and negotiable

 
           
 
 MRTLOG

 
 future

 
 phone

 
 0

 
 Logging Unit Meter changes is not turned on

 
       
 1

 
 Logging Unit Meter changes is turned on

 
           
 
 NEWCAS1

 
 future

 
 phone

 
 0

 
 Initial load of CSPS table files has not been completed

 
       
 1

 
 initial load of CSPS table files has been completed

 
           
 
 NEWSMS

 
 V8L4A

 
 Tape

 
 0

 
 SMS module is not installed - disallow hooks from POS

 
       
 1

 
 SMS module is installed.  Cmd key access from POS okay

 
           
 
 NITESHFT

 
 2.3

 
 Phone

 
 0

 
 TK Eastern CC is not installed.

 
       
 1

 
 TK Eastern CC is installed - Night shift jobq prompt for many reports.

 
       
 2

 
 Night shift job queue available for only the DOC X157 report

 
           
 
 NOEXTADR

 
 future

 
 menu

 
 0

 
 Print EXT Name and ADR on PR Check Stub

 
       
 1

 
 Do not print EXT Name and ADR on PR Check Stub

 
           
 
 NOSCTAX

 
 future

 
 Phone

 
 0

 
 sales code tax code will override tax code from rental contract just like POS

 
       
 1

 
 Do not override the tax code on rental contract from the sales code

 
       
 2

 
 Do not override the tax code on rental contract from the sales code, except for Damage Waiver sales code

 
           
 
 NOSHORTM 

 
 21.2

 
 phone

 
 0

 
 Short model is not generated automatically when adding a new model

 
       
 1

 
 Short model is generated automatically when adding a new model

 
           
 
 NOWGMEOD

 
 future

 
 Phone

 
 0

 
 print changes to WGM from Inquire/Update Units on the Acct EOD Report

 
       
 1

 
 Do not print changes to WGM from Inquire/Update Units on the Acct EOD Report

 
           
 
 NOZEROES

 
 10.1

 
 Phone

 
 0

 
 $0.00 Equipment Rental attachments will not show up in Periodic Invoicing.

 
       
 1

 
 $0.00 Equipment Rental attachments will show up in Periodic Invoicing.

 
           
 
 OMITBACK

 
 11.2 V1

 
 Menu

 
 0

 
 File backup will be included in the normal Backup/End of Day routines

 
       
 1

 
 File backup will not be included in the normal Backup/End of Day routines

 
           
 
 OPENDOC

 
 2.1

 
 Menu

 
 0

 
 Previous Open Document Message is not displayed.

 
       
 1

 
 Previous Open Document Message is displayed.

 
           
 
 PARLOG

 
 PRE23

 
 Menu

 
 0

 
 Parts Transaction Log is not installed

 
       
 1

 
 Parts Transaction Log is installed

 
           
 
 PLJRNCHK

 
 future

 
 Phone

 
 0

 
 Parts Log journaled files will be checked prior to POS, PPM, Rec Order, Corr Ord B4 Rec

 
       
 1

 
 Parts Log journaled files will not be checked prior to POS, PPM, Rec Order, Corr Ord B4 Rec

 
           
 
 PARTHIDE

 
 future

 
 phone

 
 0

 
 Show pricing from the pricebook in Parts Inquiry and Parts Posting and Maintenance

 
       
 1

 
 Hide pricing from the pricebook in Parts Inquiry and Parts Posting and Maintenance

 
           
 
 PARTTAX

   
 Menu

 
 0

 
 Don't allow parts to have an override tax code

 
       
 1

 
 Allow parts to have an override tax code

 
           
 
 PAYAMSG

 
 V8L5

 
 Menu

 
 0

 
 Prompt for Alignment message

 
       
 1

 
 Avoid Prompt for Alignment messages