---
title: "Hidden OPTs and other OPIs #24 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #24 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #24 – AG Internal."
---

_Hidden OPTs and other OPIs #24 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 POSNOPRO

 
 future

 
 phone

 
 0

 
 CNH Gateway Promo Action defaults to L (lookup) only if over $500

 
       
 1

 
 CNH Gateway Promo Action defaults to ' ' (blank-no promotion)

 
       
 2

 
 CNH Gateway Promo Action always defaults to L (Lookup)

 
           
 
 POSOFFIC

 
 V7L4

 
 Menu

 
 0

 
 Never print an office copy for labor

 
       
 1

 
 Always print an office copy for labor

 
       
 2

 
 Print office copy for labor if invoice is closed

 
           
 
 POSPBACK

 
 2.2

 
 Menu

 
 0

 
 display the "print backordered lines prompt"

 
       
 1

 
 suppress the "print backordered lines prompt"

 
           
 
 POSPCNTR

 
 V8L4

 
 Menu

 
 0

 
 do not print a counter on the invoice

 
       
 1

 
 print a counter on the invoice

 
           
 
 POSPDATE

 
 V8L4

 
 Menu

 
 0

 
 print session date if ticket is open, closed date if ticket is closed

 
       
 1

 
 always print creation date - regardless

 
           
 
 POSDISC

 
 future

 
 Menu

 
 0

 
 Ship To Discount will be used when present

 
       
 1

 
 Sales Code Discount will be used when present

 
           
 
 POSPHONE

 
 V8L2

 
 Menu

 
 0

 
 Print Phone Number on invoice

 
       
 1

 
 Never print Phone Number on invoice

 
       
 2

 
 Print Phone Number at TOP of invoice

 
           
 
 POSPRBN2

 
 future

 
 Phone

 
 0

 
 Do not print extra invoice part line for 2nd bin

 
       
 1

 
 Print extra invoice part line for 2nd bin

 
           
 
 POSPRTM4

 
 Future 

 
 Phone

 
 0

 
 Gregware Custom POS Invoice is not installed.

 
       
 1

 
 Gregware POS Invoice (4 sp to left) is installed.

 
           
 
 POSPSPEC

 
 future

 
 Menu

 
 0

 
 Do not print external specs on POS invoice for Unit Sale lines

 
       
 1

 
 Print external specs on POS invoice for Unit Sale lines

 
           
 
 POSPTAXR

 
 2.3

 
 Menu

 
 0

 
 Print the tax rate on each invoice line

 
       
 1

 
 Print the tax code on each invoice line

 
           
 
 POSPTIME

 
 V8L4

 
 Menu

 
 0

 
 do not print the time of day on the invoice

 
       
 1

 
 print the time of day on the invoice

 
           
 
 POSPWARR

 
 future

 
 Menu

 
 0

 
 Print warranty code and date on invoice for Unit Sale lines

 
       
 1

 
 Do not print warranty code and date on invoice for Unit Sale lines

 
           
 
 POSQTY1

 
 11.1

 
 Menu

 
 0

 
 Default quantity to 1 if after XREF it is still 0

 
       
 1

 
 Do not default quantity to 1 even if it is 0

 
           
 
 POSSCDOC

 
 11.1

 
 Phone

 
 0

 
 Do not limit Sales Codes in POS to certain Document Types (Restrict Doc types)

 
       
 1

 
 Limit Sales Codes in POS to certain Document Types

 
           
 
 POSSECUR

 
 V8L4

 
 Menu

 
 0

 
 POS security is not installed

 
       
 1

 
 POS security is installed and the end of day POS log will print

 
       
 2

 
 POS security is not installed but the end of day POS log will print

 
           
 
 POSSHAD

 
 11.1

 
 Phone

 
 0

 
 Electronic Forms POS - Use shading

 
       
 1

 
 Electronic Forms POS - Do not use shading

 
           
 
 POSSIGNA

 
 V7L4

 
 Menu

 
 0

 
 Print signature line on charge document

 
       
 1

 
 Print signature line on all documents

 
       
 2

 
 Never print signature line

 
           
 
 POSSRCHG

 
 V7L4

 
 Menu

 
 0

 
 "SURCHARGE " labels negative discount total line

 
       
 1

 
 "          " (blank)

 
       
 2

 
 "FED. TAX  "

 
       
 3

 
 "EXCISE TAX"

 
       
 4

 
 "COUNTY TAX"

 
       
 5

 
 "CITY TAX  "

 
       
 6

 
 "PROV. TAX "

 
       
 7

 
 "STATE TAX "

 
           
 
 POSSSI

 
 V8L5

 
 Menu

 
 0

 
 Self service invoicing is not installed  (Changed from CUST0006 - 12/09/94)

 
       
 1

 
 Self service invoicing is installed

 
           
 
 POSTAX#

 
 future

 
 Menu

 
 0

 
 Print the Receivable Tax # on the POS Invoice

 
       
 1

 
 Print "ON FILE" instead of the Tax# on the POS Invoice

 
           
 
 POSTAXEX

 
 future

 
 Phone

 
 0

 
 Exempt cash customers will not use tax rules

 
       
 1

 
 Exempt cash customers will use tax rules

 
           
 
 POSTAXIL

 
 future

 
 phone

 
 0

 
 does not calculate tax for City/Dist/Other even if the 'Inside xxx limit' field is set to 'N'

 
       
 1

 
 calculates tax for City/Dist/Other even if the 'Inside xxx limit' field is set to 'N'

 
           
 
 POSTAXMO

 
 future

 
 phone

 
 0

 
 Regular DBST tax rules applied                                

 
       
 1

 
  If selling in Missouri to locations inside Missouri, use selling store tax code - not dest based for in state sales

 
         
  

 
 
 POSTAXPE

 
 Future

 
 Menu

 
 0

 
 Part tax overrides an exempt customer

 
       
 1

 
 Part Tax does not override an exempt customer

 
       
 2

 
 Part Tax overrides an exempt customer except on Internal tickets

 
       
 3

 
 Part Tax overrides an exempt customer except on Warranty lines

 
       
 4

 
 Part Tax overrides an exempt customer except on Internal docs and Int/War lines