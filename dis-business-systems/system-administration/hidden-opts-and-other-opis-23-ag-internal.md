---
title: "Hidden OPTs and other OPIs #23 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #23 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #23 – AG Internal."
---

_Hidden OPTs and other OPIs #23 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
   

 
   

 
   

 
   

 
   

 
 
 POSDVROL

 
 V8L5A

 
 Menu

 
 0

 
 Display all Divisions on the POS rolodex

 
       
 1

 
 Display only security gate division on the POS rolodex

 
           
 
 POSEDIT

 
 V8L5A

 
 Menu

 
 0

 
 Display only the division in the edit code column of the POS rolodex

 
       
 1

 
 Display all edit codes in the edit code column of the POS rolodex

 
   
 2.3

   
 2

 
 Display first 15 characters from ADM City/State field in the Edit code column of POS rolodex

 
           
 
 POSEMAIL

 
 future

 
 phone

 
 0

 
 MyAccount email will be sent even if customer charges on an invoice are equal to zero

 
       
 1

 
 MyAccount email will not be sent if customer charges on an invoice are equal to zero

 
           
 
 POSEOM

 
 future

 
 phone

 
 0

 
 The POS EOM purge date is restricted to one year prior

 
       
 1

 
 The POS EOM purge date restriction is NOT enforced

 
           
 
 POSFIND

 
 future

 
 phone

 
 0

 
 The POS Address Number Find feature to prevent duplicate cash addresses is not on

 
       
 1

 
 The POS Address Number Find feature to prevent duplicate cash addresses is on (requires POSCSHBP to be on)

 
           
 
 POSHIST

 
 1.4

 
 Phone

 
 0

 
 POS History (SAH) is not installed. ( Pioneer )

 
       
 1

 
 POS History (SAH) is installed.

 
           
 
 POSINVCE

 
 V7L4.

 
 Menu

 
 0

 
 Standard Short form: 56 lines, 6 footer lines

 
       
 1

 
 Standard Long form:  88 lines, 7 footer lines

 
       
 2

 
 Extra Long form:    112 lines, 7 footer lines

 
           
 
 POSINVSU

 
 11.0

 
 Phone

 
 0

 
 POS Invoice Laser Form Speed Up is not on

 
       
 1

 
 POS Invoice Laser Form Speed Up is on

 
           
 
 POSLABDT

 
 V7L4

 
 Menu

 
 0

 
 No labor detail lines on invoice

 
       
 1

 
 Print labor detail lines on invoice

 
   
 1.4

   
 2

 
 Thermo King Specific - Print labor detail lines on invoice but

 
         
 combine lines that have matching TK job codes and do not print the employee#.

 
   
 1.4

   
 3

 
 Same as opt=2 except only print freon#, job code, & job description.

 
   
 1.4

   
 4

 
 Same as opt=2 except only print job code & job description.

 
           
 
 POSLABHR

 
 V7L4

 
 Menu

 
 0

 
 Show labor hours on detail and total lines

 
       
 1

 
 No labor hours on detail or total lines

 
           
 
 POSLBCST

 
 V8L0

 
 Menu

 
 0

 
 Use reported hours

 
       
 1

 
 Use billed hours

 
           
 
 POSLOCK

 
 V8L4B

 
 Menu

 
 0

 
 Point of Sale Lockout is not installed

 
       
 1

 
 Point of Sale Lockout is installed (manual)

 
       
 2

 
 Point of Sale Lockout is installed (automatic)

 
   
 10809

   
 3

 
 POS Lockout/Automatic based on 30,60,90,120 day buckets

 
       
 4

 
 POS Lockout/Automatic based on both Credit Limit and REM Buckets.

 
   
 Bacon

 
 Phone

 
 5

 
 POS Lockout/Automatic based on both Credit Limit and REM Buckets.

 
           
 
 POSLOGPA

 
 V8L4

 
 Menu

 
 0

 
 print line additions on the security report

 
       
 1

 
 do not print line additions on the security report

 
           
 
 POSLOGPC

 
 future

 
 Menu

 
 0

 
 print closing of all documents on the security report

 
       
 1

 
 do not print closing of documents on the security report

 
           
 
 POSLOGPD

 
 V8L4

 
 Menu

 
 0

 
 print line deletions on the security report

 
       
 1

 
 do not print line deletions on the security report

 
           
 
 POSLOGPK

 
 V8L4

 
 Menu

 
 0

 
 print document cancellations on the security report

 
       
 1

 
 do not print document cancellations on the sec rpt

 
           
 
 POSLOGPM

 
 V8L4

 
 Menu

 
 0

 
 print line modifications on the security report

 
       
 1

 
 do not print line modifications on the security report

 
           
 
 POSLOGPO

 
 V8L4

 
 Menu

 
 0

 
 print document reopenings on the security report

 
       
 1

 
 do not print document reopenings on the security rpt

 
           
 
 POSBLCON

 
 future

 
 phone

 
 0

 
 Below cost check for parts and units

 
       
 1

 
 Below cost check for parts only

 
       
 2

 
 Below cost check for units only

 
           
 
 POSBLNET

 
 11.0

 
 Menu

 
 0

 
 Prevent Sale Below Cost is off

 
       
 1

 
 Prevent Sale Below Cost or Cost = 0 is on

 
       
 2

 
 Prevent Sale Below Cost Only is on

 
           
 
 POSBLRPT

 
 11.0

 
 Menu

 
 0

 
 Don't Print Below Cost Report at EOD

 
       
 1

 
 Print Below Cost Report with all transactions at EOD

 
       
 2

 
 Print Below Cost Report with only overrides at EOD

 
           
 
 POSBMRPT

 
 11.0

 
 Menu

 
 0

 
 Don't Print Below Margin Report at EOD

 
       
 1

 
 Print Below Margin Report with all transactions at EOD

 
       
 2

 
 Print Below Margin Report with only overrides at EOD

 
           
 
 POSMARGIN

 
 11.0

 
 Menu

 
 0

 
 Prevent Sale Below Margin is off

 
       
 1

 
 Prevent Sale Below Margin is on

 
           
 
 POSMDTX

 
 future

 
 phone

 
 0

 
 round sales tax per Maryland requirements is not installed

 
       
 1

 
 round sales tax per Maryland requirements is installed

 
           
 
 POSNOPDd

 
 future

 
 phone

 
 0

 
 CNH Gateway Promo Action defaults to L (Lookup) for the division code d

 
       
 1

 
  CNH Gateway Promo Action defaults to ‘ ‘ (blank-no promotion) for the division code d