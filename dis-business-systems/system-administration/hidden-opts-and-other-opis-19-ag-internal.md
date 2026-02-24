---
title: "Hidden OPTs and other OPIs #19 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #19 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #19 – AG Internal."
---

_Hidden OPTs and other OPIs #19 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 DISNETMS

 
 11.1

 
 Phone

 
 0

 
 Multiple dealer numbers are not being used.

 
 
  

     
 1

 
 Multiple dealer numbers are being used.

 
           
 
 DISNETIS

 
 11.1

 
 Phone

 
 0

 
 DISNETIS has not been run.

 
 
  

     
 1

 
 DISNETIS has been run.

 
           
 
 DISOPC

 
 future

 
 phone

 
 0

 
 Online Parts Catalogs will work with IM 20903P

 
 
  

     
 1

 
 Online Parts Catalogs will work with IM 20909P

 
           
 
 DIVPYN

 
 future

 
 Menu

 
 0

 
 Default "Print All Divisions" prompt on Security Gate to Y

 
 
  

     
 1

 
 Default "Print All Divisions" prompt on Security Gate to N

 
           
 
 DOCCNT#*

 
 2.1

 
 Menu

 
 0

 
 Count sale documents being posted ONLY IF pos. 9-10 of Document# = '#*'.

 
 
  

     
 1

 
 Count all source documents to sale accounts

 
           
 
 DROPCOST

 
 Menu

 
 Phone

 
 0

 
 Dropship parts will be costed with Average Cost if that opt is on, otherwise Dealer Net

 
       
 1

 
 Dropship parts will be costed with Dealer Net even if the Average Cost opt is on

 
         
  

 
 
 DROPOPEN

 
 2.2

 
 Menu

 
 0

 
 Drop ship 'D' priority parts are included on priority orders if ticket is open or closed.

 
 
  

     
 1

 
 Drop ship 'D' priority parts are only included on priority orders if ticket is closed.

 
         
  

 
 
 DTRLOG

 
 11.0 V.2

 
 Phone

 
 0

 
 Credit Card background program will not automatically log

 
 
  

     
 1

 
 Credit Card background program will automatically log

 
           
 
 EGL1COSD

 
 2.2

 
 Phone

 
 0

 
 Eagle 1 Cost of Sales Distr. is deactivated.

 
 
  

     
 1

 
 Eagle 1 Cost of Sales Distr. is activated.

 
           
 
 EGL1FS

 
 2.2

 
 Phone

 
 0

 
 Eagle 1 Financial Statement is deactivated.

 
       
 1

 
 Eagle 1 Financial Statement is activated.

 
           
 
 EGL1GLT

 
 2.2

 
 Phone

 
 0

 
 Eagle 1 General Ledger Transmission is deactivated.

 
       
 1

 
 Eagle 1 General Ledger Transmission is activated.

 
           
 
 EGL1ODA

 
 2.2

 
 Phone

 
 0

 
 Eagle 1 Override Debit Account is deactivated.

 
       
 1

 
 Eagle 1 Override Debit Account is activated.

 
           
 
 EGL1TCLK

 
 V8L5A

 
 Phone

 
 0

 
 Eagle 1 Time Clock is deactivated.  (See TMCLK for base package switch.)

 
       
 1

 
 Eagle 1 Time Clock is activated.

 
           
 
 ENDODAY1

 
 V8L4

 
 Menu

 
 0

 
 print the subledger balance report during acct eod

 
       
 1

 
 don't print the subledger balance report during eod

 
           
 
 ENDODAY2

 
 2.1

 
 Menu

 
 0

 
 Run Receivables Aging Program.

 
       
 1

 
 Don't run Receivables Aging Program.

 
 
 EPCPORDR

         
   
 future

 
 Menu

 
 0

 
 On Order in EPC will only show quantity on Stock Orders

 
       
 1

 
 On Order in EPC will show Stock and Priority Orders

 
           
 
 ERPROBYP

 
 future

 
 phone

 
 0

 
 Do not bypass printer options window when printing a rental contract

 
       
 1

 
 Bypass printer options window when printing a rental contract

 
           
 
 EFPROBYP

 
 future

 
 phone

 
 0

 
 Do not bypass POS printer options when going into POS from Equip Rentals

 
       
 1

 
 Bypass POS printer options when going into POS from Equip Rentals

 
           
 
 EXCHANGE

 
 2.1

 
 Phone

 
 0

 
 Inter-division exchange rates disabled.

 
       
 1

 
 Inter-division exchange rates enabled.

 
           
 
 F&IINSTL

 
 V8L4

 
 Menu

 
 0

 
 F&I is not installed

 
       
 1

 
 F&I is installed (nothing to download)

 
       
 2

 
 F&I is installed (ready to download)

 
           
 
 FFR nn 

 
 V8L5

 
 Phone

 
 0

 
 Ask for forms change for the FFR report.

 
       
 1

 
 Do not ask for forms change for the FFR report.

 
         
 (The ' nn ' in the switch name is the format number of the report being run.  This way

 
         
   the switch can be set for individual formats rather than for all formats.)

 
           
 
 FIDISLTD

 
 V8L5

 
 Menu

 
 0

 
 DIS Limited F&I is not installed

 
       
 1

 
 DIS Limited F&I is installed

 
           
 
 FLRNCOLR

 
 V8L0

 
 Menu

 
 0

 
 'Color' appears as heading on Flooring/Inventory Rpt

 
       
 1

 
 'Mfg#' appears as heading on Flooring/Inventory Rpt

 
           
 
 FLTMGT

 
 2.3

 
 Phone

 
 0

 
 Fleet Management is not installed.

 
       
 1

 
 Old Fleet Management is installed. ( No longer used - but probably needs to be listed )

 
       
 2

 
 New Fleet Management has been installed.

 
           
 
 FORDAUTO

 
 Future 

 
 Menu

 
 0

 
 Ford Auto Comm. is not installed.  CHKOBJ FORD *SBSD -> MONMSG CPF9801 

 
       
 1

 
 Ford Auto Comm. is installed.

 
           
 
 FPDIVN

 
 10.1

 
 Menu

 
 0

 
 Farm Plan transactions will be grouped according to the GL Account division.

 
       
 1

 
 Farm Plan transactions will be grouped according to the editing division code.

 
           
 
 FPINST

 
 V8L5

 
 Menu

 
 0

 
 Farm Plan Communications is not installed.

 
       
 1

 
 Farm Plan Communications is installed.

 
   
 2.3

   
 2

 
 FarmPlan 95 communications is installed.

 
       
 3

 
 Farm Plan Communications is through Connect2

 
           
 
 FPTOTTRN

 
 2.2

 
 Menu

 
 0

 
 Farm Plan Offsetting Transactions are Accumulated.

 
       
 1

 
 Farm Plan Offsetting Transactions are created individually.