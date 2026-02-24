---
title: "Hidden OPTs and other OPIs #4 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #4 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #4 – AG Internal."
---

_Hidden OPTs and other OPIs #4 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 CASEAFXR

 
 future

 
 phone

 
 0

 
 AMAX transfer files will be added as usual

 
   
  

   
 1

 
 AMAX transfer files will not be added

 
           
 
 CASEALRD

 
 future

 
 phone

 
 0

 
 AMAX - Do not send the last reciept date instead of the add date on the inventory file

 
       
 1

 
 AMAX - Send the last reciept date instead of the add date on the inventory file

 
           
 
 CASEAPR

 
 2.2

 
 Menu

 
 0

 
 Case Order Fulfillment is not installed

 
       
 1

 
 Case Order Fulfillment is installed

 
           
 
 CASEAPUL

 
 future

 
 phone

 
 0

 
 AMAX files will not be pulled using Interface Manager instead of pushing to the IFS

 
       
 1

 
 AMAX files will be pulled using Interface Manager instead of pushing to the IFS

 
           
 
 CASE56

 
 V8L5A

 
 Phone

 
 0

 
 Use Logical Unit 3 and 4 devices for CASE communications.  ( Normal )

 
       
 1

 
 Use Logical Unit 5 and 5 devices for CASE Communications.  ( Dual File Set Dealers )

 
         
 (This opt should only be turned on for the second file set.  Not the Primary.)

 
           
 
 CASLOADd

 
 2.2

 
 System

 
 0

 
 Order Fulfillment:  Daily activity status

 
       
 1

 
 Order Fulfillment:  Daily activity status

 
       
 2

 
 Order Fulfillment:  Daily activity status

 
           
 
 CASLOGTR

 
 future

 
 phone

 
 0

 
 Only show a subset of Case transactions in the Outbound log

 
       
 1

 
 Show all Case transactions in the Outbound log

 
           
 
 CASLZROd

 
 current

 
 phone

 
 0

 
 Parts Mass Load is not scheduled for Backup

 
       
 1

 
 Parts Mass Load is scheduled for Backup  - for SNA,  – Send Inventory and History information – FTP only

 
       
 2

 
 Parts Mass Load is scheduled for Backup – Send only Inventory information – FTP only

 
       
 3

 
 Parts Mass Load is scheduled for Backup – Send only History information – FTP only

 
           
 
 CASNHD

 
 future

 
 phone

 
 0

 
 CNH All Brands Warning will not display

 
       
 1

 
 CNH All Brands Warning will display

 
           
 
 CCAUTSET

 
 2.2

 
 Phone

 
 0

 
 Credit Card - Datatran Communications is not installed

 
       
 1

 
 Credit Card - Datatran Communications is installed

 
           
 
 CCINST

 
 2.1

 
 Menu

 
 0

 
 Case Credit Communications is not installed.

 
       
 1

 
 Case Credit Communications is installed.

 
           
 
 CCMASK

 
 10.2

 
 Menu

 
 0

 
 mask both public and private cards          

 
     
  

 
 1

 
 mask public cards but unmask private cards  

 
       
 2

 
 unmask public cards but mask private cards  

 
       
 3

 
 public and priunmask both vate cards        

 
           
 
 CCPREAMT

 
 future

 
 phone

 
 0

 
 Don't issue a hard error if the new invoice amount is greater than the Pre-Auth amount.

 
       
 1

 
 Issue a hard error if the new invoice amount is greater than the Pre-Auth amount.

 
           
 
 CCPRMLOG

 
 future

 
 phone

 
 0

 
 Allow the date in the CCLOGO data area to control how long credit card logging takes place.

 
       
 1

 
 Ignore the date in the CCLOGO data area and always log credit card transactions.

 
       
  

   
 
 CCTEXT

 
 2.2

 
 Menu

 
 0

 
 Print legal text at the bottom of credit card invoice.

 
       
 1

 
 Do not print the legal txt at the bottom of a credit card invoice.