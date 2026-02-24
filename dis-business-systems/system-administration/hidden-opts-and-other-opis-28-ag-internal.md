---
title: "Hidden OPTs and other OPIs #28 – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #28 – Ag Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #28 – Ag Internal."
---

_Hidden OPTs and other OPIs #28 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
  

 
 
 SNDUNTIL

 
 future

 
 phone

 
 0

 
 DISNET - Initial send has not occurred

 
       
 1

 
 DISNET - Initial send has occurred.

 
           
 
 SRALLOW

 
 future

 
 Phone

 
 0

 
 Use the System Request exit program

 
       
 1

 
 Bypass the System Request exit program

 
           
 
 STARTUP1

 
 V8L0

 
 Menu

 
 0

 
 Do run startup programs

 
       
 1

 
 Do not run startup programs

 
   
 V8L1

   
 2

 
 Do run startup programs including Cache

 
           
 
 STATALIG

 
 10801

 
 Menu

 
 0

 
 Print an Aligment Statement.

 
       
 1

 
 Do not Print an Alignment Statement.

 
           
 
 STATFORM

 
 10801

 
 Menu

 
 0

 
 Print Old (DIS) Statement Form.

 
       
 1

 
 Print New (SERTI) Statement Form.

 
       
 2

 
 Alternate New Style Forms

 
           
 
 STATHPHO

 
 10801

 
 Menu

 
 0

 
 Do Not Print Home Phone on Statement.

 
       
 1

 
 Print Home Phone on Statement.

 
           
 
 STATPCIE

 
 10801

 
 Menu

 
 0

 
 Do Not Print Company Information on Statement.

 
       
 1

 
 Print Company Information on Statement.

 
           
 
 STATSELD

 
 future 

 
 Menu

 
 0

 
 Print future-dated transactions as well.

 
       
 1

 
 Do not include future-dated transactions.

 
           
 
 STATPGST

 
 10801

 
 Menu

 
 0

 
 Do Not Print Monthly GST on Statement.

 
       
 1

 
 Print Monthly GST on Statement.

 
           
 
 STATPPST

 
 10801

 
 Menu

 
 0

 
 Do Not Print Monthly PST on Statement.

 
       
 1

 
 Print Monthly PST on Statement.

 
           
 
 STATWPHO

 
 10801

 
 Menu

 
 0

 
 Do Not Print Work Phone on Statement.

 
       
 1

 
 Print Work Phone on Statement.

 
           
 
 STDJOBPG

 
 2.1

 
 Menu

 
 0

 
 Standard Job Report does not start a new page with each new standard job.

 
       
 1

 
 Standard Job Report does start a new page with each new standard job.

 
           
 
 STRIPSGL

 
 11.1

 
 Menu

 
 0

 
 Do not print credit card signature line

 
       
 1

 
 Print credit card signature line  

 
       
 2

 
 Print credit card signature line on two copies

 
           
 
 SUBIAM1

 
 V8L4A

 
 Menu

 
 0

 
 In POS when searching for supersession information, check the price book first and then IBM.

 
       
 1

 
 In POS when searching for supersession information, check IBM first before the price book.

 
           
 
 SUPERX51

 
 11.0

 
 Menu

 
 0

 
 Look forward through supersession chain       

 
       
 1

 
 Look backward and forward through supersession chain

 
           
 
 SUPER341

 
 V8L1

 
 Menu

 
 0

 
 Do not include superseded parts on a suggested order

 
       
 1

 
 Include superseded parts on a suggested order

 
   
 V8L5

   
 2

 
 Process supersession chain on a suggested order

 
           
 
 SUPER342

 
 V8L3

 
 Menu

 
 0

 
 Do not fill reservations from superseded parts

 
       
 1

 
 Fill reservations from superseded parts

 
       
 2

 
 Order last part in the supersession chain

 
           
 
 TARGCNV   ** NOT LONGER USED AFTER 10.2  **

     
  

 
 
  

 
 V8L5A

 
 Menu

 
 0

 
 Target Marketing file conversion is not done.

 
       
 1

 
 Target Marketing file conversion is done.

 
           
 
 TARGET   ** NOT LONGER USED AFTER 10.2  **

     
  

 
 
  

 
 V8L5

 
 Menu

 
 0

 
 Do not Update Target Marketing Files.

 
       
 1

 
 Update Target Marketing Files.

 
           
 
 TAXRPCSD

 
 future

 
 phone

 
 0

 
 do not allow manually entered documents with a '#*' to be treated like POS documents for tax report reasons

 
       
 1

 
 allow manually entered documents with a '#*' to be treated like POS documents for tax report reasons

 
           
 
 TAXRPTAC

 
 future

 
 phone

 
 0

 
 Do no read accounts from tax codes besides reading TAXACCT when DBST is on and printing tax report

 
       
 1

 
 Read accounts from tax codes besides reading TAXACCT when DBST is on and printing tax report

 
           
 
 TAXRPTAP

 
 11.0

 
 Menu

 
 0

 
 Sales Tax Rpt exclude AP transactions from the posted amount on report

 
       
 1

 
 Sales Tax Rpt include AP transactions in the posted amount on the report

 
           
 
 TAXRPTST

 
 future

 
 Menu

 
 0

 
 Use Ship to address on Sales Tax Report

 
       
 1

 
 Do no use Ship to address on Sales Tax Report

 
           
 
 TAXSPLIT

 
 future

 
 Menu

 
 0

 
 Use ship to address on split documents

 
       
 1

 
 Do not use ship to address on split documents

 
           
 
 TCLCKJRN

 
 future

 
 phone

 
 0

 
 Journaling of TCD and u.SAM, and keystroke tracing in X5B - 1,4, & 5 is off.

 
       
 1

 
 Journaling of TCD and u.SAM, and keystroke tracing in X5B - 1,4, & 5 will start after STRTCLKJRN is run.

 
       
 2

 
 Journaling of TCD and u.SAM, and keystroke tracing in X5B - 1,4, & 5 is on.

 
           
 
 TCNWOd

 
 future

 
 Menu

 
 0

 
 Time Clock Now Working On  option is not installed for this division (d=div)

 
       
 1

 
 Time Clock Now Working On  option is installed for this division (d=div)

 
           
 
 TCVOID

 
 future

 
 Menu

 
 0

 
 existing time clock punches do not prevent open document from being voided

 
       
 1

 
 existing time clock punches prevent open document from being voided

 
           
 
 TCWODV

 
 11.1

 
 Menu

 
 0

 
 Work Order Default Value screen will not be displayed

 
       
 1

 
 Work Order Default Value screen will display if document is a work order

 
       
 2

 
 Work Order Default Value screen will display for sales order or work order documents