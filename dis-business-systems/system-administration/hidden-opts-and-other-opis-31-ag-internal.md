---
title: "Hidden OPTs and other OPIs #31 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #31 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #31 – AG Internal."
---

_Hidden OPTs and other OPIs #31 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 X21SNSEL

 
 future

 
 Menu

 
 0

 
 Serial Number Selection Window will appear at Inquire/Update Units

 
       
 1

 
 Serial Number Selection Window will not appear at Inquire/Update Units

 
           
 
 X21UPCSR

 
 2.3

 
 Menu

 
 0

 
 Position cursor at input field

 
       
 1

 
 Position cursor at the option field

 
           
 
 X23INDEX

 
 2.2

 
 Menu

 
 0

 
 Include only customers who have purchased units in the name index of Sold Units Inq.

 
       
 1

 
 Include all customers from the address master file in the name index of Sold Units Inq.

 
           
 
 X288PAGE

 
 future

 
 Menu

 
 0

 
 Do NOT start a new page for each GL Account#

 
       
 1

 
 Start a new page for each GL Account#

 
           
 
 X3APARTL

 
 2.1

 
 Menu

 
 0

 
 Do not prompt for parts voice data at end of month.

 
       
 1

 
 Prompt for parts voice data at end of month.

 
           
 
 X3BOBSLT

 
 2.2

 
 Menu

 
 0

 
 Do not allow selection of classes to be excluded from LIFO End of Year.

 
       
 1

 
 Allow up to 15 selected classes to be excluded from LIFO End of Year.

 
           
 
 X3CCALCA

 
 2.3

 
 Menu

 
 0

 
 During Transfer Parts (X3C1 not X3427) - Recalculate average cost using "from" average cost

 
       
 1

 
 During Transfer Parts (X3C1 not X3427) - Recalculate average cost using "from" dealer net

 
           
 
 X3HIDPRC

 
 11.0

 
 Menu

 
 0

 
 No customer view.  All prices are always shown.

 
       
 1

 
 Part Inquiry starts in business view.  All prices shown.  F21 toggles to/from customer view.

 
       
 2

 
 Part Inquiry starts in customer view.  Only list price is shown.  F21 tbbles to/from business view.

 
       
 3

 
 Parts Inquiry in business view with prices hidden

 
           
 
 X3VENSEL

 
 11.1

 
 Menu

 
 0

 
 The vendor selection window will display at X31, X32, POS detail, and PA

 
       
 1

 
 The vendor selection window will display at X31, X32, and POS detail, and not PA

 
       
 2

 
 The vendor selection window will not display

 
           
 
 X31GRP01

 
 future

 
 Menu

 
 0

 
 Remember the last group code used in Parts Inquiry and default to that group code

 
       
 1

 
 Always default to group code 01 in Parts Inquiry

 
           
 
 X32PTSEC

 
 V8L4

 
 Menu

 
 0

 
 do not use part transaction security code

 
       
 1

 
 use part tranx security code for X3-2: blank, -, M, P, R, and T; must enter each transaction

 
   
 V8L4B

   
 2

 
 use part tranx security code for X3-2 : blank, -, M, P, R, and T; must enter only for first transaction

 
           
 
 X32SOS

 
 2.2

 
 Menu

 
 0

 
 S.O.S. feature is enabled

 
       
 1

 
 S.O.S. feature is disabled

 
           
 
 X341MULT

 
 2.3

 
 Menu

 
 0

 
 Finalizing a Stock Order returns to the menu

 
       
 1

 
 Allows the Finalization of multiple orders by returning to Order prompt

 
           
 
 X34DISAN

 
 2.2

 
 Menu

 
 0

 
 Suggested Order: DIS method - if no sale in supply period last year prorate annual sales

 
       
 1

 
 Suggested Order: DIS method - if no sale in supply period last year do not prorate annual sales

 
           
 
 X34INCTR

 
 future

 
 menu

 
 0

 
 total incoming part transfers will not be added to "on order" total in X34 calculations

 
       
 1

 
 total incoming part transfers will be added to "on order" total in X34 calculations

 
           
 
 X36CNH

 
 11.0 V.2

 
 Menu

 
 0

 
 Do not display prompt for printing CNH marketing codes

 
       
 1

 
 Display prompt for printing CNH marketing codes

 
           
 
 X372BLNK

 
 V8L4A

 
 Menu

 
 0

 
 write over part information fields in IBM even if fields on price tape are blank

 
       
 1

 
 do not write over part information fields in IBM if fields on price tape are blank

 
           
 
 X379DUP

 
 future

 
 phone

 
 0

 
 Duplex Printing (*YES)

 
       
 1

 
 Duplex Printing (*NO)

 
           
 
 X39RPT

 
 V8L5A

 
 Menu

 
 0

 
 do not print the eod master file changes report. (originally mcfarlane c.c.)

 
       
 1

 
 print the eod master file changes report.

 
           
 
 X51CASDL 

 
 obsolete 

 
 obsolete 

 
 0

 
 Do not provide Dialup prompt at X3.1, or X5.1

 
         
 Provide prompt to Dialup at X3.1 and X5.1

 
           
 
 X5TRAD@C

 
 future

 
 Menu

 
 0

 
 Do not include @C at the end of desc field in *TRADE sc inventory trans

 
       
 1

 
 Include @C at the end of desc field in *TRADE sc inventory trans

 
           
 
 X51VANBN

 
 future

 
 Menu

 
 0

 
 Use main store bin locations on van documents

 
       
 1

 
 Use van code bin locations on van documents

 
           
 
 X563COST

 
 future 

 
 Menu

 
 0

 
 If labor cost = $0, use the payroll labor rate of the Soldby address to print cost on report.

 
       
 1

 
 If labor cost = $0, do NOT use payroll labor rate to report costing. Leave cost at zero $.

 
           
 
 X564OORC

 
 1.4

 
 Menu

 
 0

 
 Only include closed/posted SAM documents on the report and use the posted date to compare.

 
       
 1

 
 Include open, reopen, and closed documents on the report and use the work date on the detail

 
         
 labor line to compare

 
           
 
 X57DIVSC

 
 2.2

 
 Menu

 
 0

 
 Parts Sales History: Division change requires security

 
       
 1

 
 Parts Sales History: Division change does not require security

 
           
 
 X7PMPOPT

 
 Future

 
 Hidden

 
 0

 
 Case PMP reports are available to use

 
 
  

   
 Opt

 
 1

 
 Case PMP reports are disabled