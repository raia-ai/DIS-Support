---
title: "Hidden OPTs and other OPIs #25 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #25 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #25 – AG Internal."
---

_Hidden OPTs and other OPIs #25 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 POSTAXRL

 
 10.1

 
 Menu

 
 0

 
 Only use sales tax rules when customer's division is diff from selling division

 
     
 X9

 
 1

 
 Use tax rules when customer's division is same as selling division

 
           
 
 POSTAXSO

 
 11.0

 
 Phone

 
 0

 
 Use customer tax code if ship to zip code doesn't find a match

 
       
 1

 
 If ship to zip code doesn't find a match use selling division zip code  to match

 
           
 
 POSTAXST

 
 future

 
 Phone

 
 0

 
 Forge Welkin Code is not installed

 
 
  

     
 1

 
 Forge Welkin Code to not use the tax code from a recv shipping record (ADS file)

 
           
 
 POSTAXVE

 
 future

 
 Phone

 
 0

 
 Custom Vetter Tax Code Override of an Exempt Customer is not installed

 
       
 1

 
 Custom Vetter Tax Code Override of an Exempt Customer is installed

 
           
 
 POSTNTX

 
 future

 
 phone

 
 0

 
 Special Tennesee tax calculation is not installed

 
       
 1

 
 Special Tennesee tax calculation is installed

 
           
 
 POSTSLDU

 
 future

 
 Menu

 
 0

 
 COS transactions allowed for Sold Units

 
       
 1

 
 COS transactions not allowed for Sold Units if it is POS document

 
       
 2

 
 COS transactions not allowed for Sold Units on any document

 
           
 
 POSTX128

 
 V8L3

 
 Menu

 
 0

 
 X12-8 do not adjust extended name and extended address.

 
       
 1

 
 X12-8 do adjust extended name and extended address.

 
           
 
 POSTX44

 
 V8L3

 
 Menu

 
 0

 
 X4-4 do not adjust extended name and extended address.

 
       
 1

 
 X4-4 do adjust extended name and extended address.

 
           
 
 POSTX51

 
 V8L3

 
 Menu

 
 0

 
 X5-1 do not adjust extended name and extended address.

 
       
 1

 
 X5-1 do adjust extended name and extended address.

 
           
 
 POSTXEDd

 
 future

 
 phone

 
 0

 
 Tax Exempt 2nd Signature is not installed for this division

 
       
 1

 
 Tax Exempt 2nd Signature is installed for this division

 
           
 
 POSTXMO

 
 future

 
 Menu

 
 0

 
 Don't allow different GL months in other divisions

 
       
 1

 
 Allow different GL months in other divisions

 
           
 
 POSVDCLD

 
 V8L5

 
 Menu

 
 0

 
 Print POS Document when Cmd10 selected

 
       
 1

 
 Do not Print POS Document when Cmd10 selected

 
           
 
 POSTWILD

 
 future

 
 phone

 
 0

 
 does not use div code of credit acct of sale code when tax code has an * in 1st pos

 
       
 1

 
 uses div code of credit acct of sale code when tax code has an * in 1st pos

 
           
 
 POSWIPIW

 
 future

 
 Menu

 
 0

 
 WIP Report does not calculate tax on I or W lines

 
       
 1

 
 WIP Report does calculate tax on I and W lines

 
           
 
 POSXCODE

 
 V8L5

 
 Menu

 
 0

 
 Default the priority code to P at POS and PA

 
       
 1

 
 Default the priority code to X at POS and PA

 
       
 2

 
 Default the priority code to X at POS only

 
       
 3

 
 Default the priority code to X at POS and PA

 
           
 
 POS11X32

 
 V8L1

 
 Menu

 
 0

 
 Display a security gate when cmd11 X32 is chosen

 
       
 1

 
 Do not display a security gate when cmd11 X32 is chosen

 
           
 
 PRINTGST

 
 V8L2

 
 Menu

 
 0

 
 Do not print GST registration number on POS invoice

 
       
 1

 
 Print GST registration number on POS invoice

 
           
 
 PRODINST

 
 V8L0

 
 Phone

 
 0

 
 Ag/CE Base Product

 
       
 1

 
 Automobile Dealership (TACTICS)

 
           
 
 PRTLCDEV

 
 V8L5

 
 System

 
 0

 
 Assume part file will be saved to tape.

 
       
 1

 
 Part file will be saved to diskette.

 
       
 2

 
 Part file will be saved to tape.

 
           
 
 PRTPAYAL

 
 V8L5

 
 Menu

 
 0

 
 Do not Print Alignment Check for Payables

 
       
 1

 
 Print Alignment Check for Payables

 
           
 
 PRTPAYCK

 
 V8L5

 
 Menu

 
 0

 
 Print Dates on Payables Check : MMDDMM

 
       
 1

 
 : YYMMDD

 
       
 2

 
 : DDMMYY

 
           
 
 PSHDSPLY

 
 11.2 V1

 
 Menu

 
 0

 
 Single line trans display at Parts Sales History

 
       
 1

 
 Double line trans display at Parts Sales History

 
           
 
 PSHINSTL

 
 V8L4

 
 Menu

 
 0

 
 Part Sales History is not installed

 
       
 1

 
 Part Sales History is installed

 
           
 
 PSPRTCMT

 
 future

 
 phone

 
 0

 
 Long Part Comment will not print on POS Invoices and Work Orders

 
       
 1

 
 Long Part Comment will print on POS Invoices and Work Orders

 
           
 
 PURPRE

 
 Future 

 
 Phone

 
 0

 
 Purchase order Remit-To is not preprinted

 
       
 1

 
 Purchase order Remit-To is preprinted

 
           
 
 PURPRINT

 
 1.4

 
 Menu

 
 0

 
 Purchase orders will print at 56 LPI.

 
       
 1

 
 Purchase orders will print at 88 LPI.

 
           
 
 PYDTLTRN

 
 V7L3

 
 Menu

 
 0

 

 
       
 1

 

 
           
 
 PYPRRATE

 
 V8L0

 
 Menu

 
 0

 

 
       
 1