---
title: "Hidden OPTs and other OPIs #3 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #3 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #3 – AG Internal."
---

_Hidden OPTs and other OPIs #3 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 ARWEB01

 
 future

 
 Menu

 
 0

 
 If a customer is set to not print invoices, all electronic forms copies are printed except for the cust copy.

 
       
 1

 
 if a customer is set to not print invoices, no copies are printed.

 
           
 
 AUTOPRIC

 
 2.1

 
 Menu

 
 0

 
 Do not automatically reprice changed part from Price Book

 
       
 1

 
 Automatically reprice changed part from Price Book

 
           
 
 AVGINSTL

 
 V8L4

 
 Menu

 
 0

 
 Average costing for parts inventory is not installed

 
       
 1

 
 Average costing for parts inventory is installed

 
           
 
 BFCREDIT

 
 V8L0

 
 Menu

 
 0

 
 posting will apply BF credits 120, 90, 60, 30, sc, current

 
       
 1

 
 posting will apply BF credits sc, 120, 90, 60, 30, current

 
           
 
 BFMERGE

 
 future

 
 Menu

 
 0

 
 Do not run balance forward merge automatically

 
       
 1

 
 Run balance forward merge automatically during scheduled backup

 
           
 
 BILLSTMT

 
 V7L3

 
 Menu

 
 0

 
 print short form bill statements

 
       
 1

 
 print long form billing statements

 
   
 V8L5

   
 2

 
 print long statements without titles

 
           
 
 BILLZERO

 
 V8L4B

 
 Menu

 
 0

 
 Do not print a statement for customers with a total balance of zero

 
       
 1

 
 Print a statement for customers with a total balance of zero if they had activity in the period.

 
   
 2.2

   
 2

 
 Print all Zero Balance Statements

 
           
 
 BKUPJOBQ

 
 future

 
 phone

 
 0

 
 Backup Job Queue is not installed

 
       
 1

 
 Backup Job Queue is installed (Henderson CC)

 
           
 
 BULKRPT

 
 future

 
 Menu

 
 0

 
 Receive Order Report: Always show Quick Code on received parts 

 
       
 1

 
 Receive Order Report: Always show Bulk equivalent on received parts

 
           
 
 C3270SON

 
 future

 
 phone

 
 0

 
 Do not automatically estab a connection to Case when going into 3270 emulation

 
       
 1

 
 Automatically estab a connection to Case when going into 3270 emulation

 
           
 
 CANCHK

 
 future

 
 Menu

 
 0

 
 Do not use eForm Canadian Imageable Checks

 
       
 1

 
 Use eForm Canadian Imageable Checks

 
           
 
 CANCHKSG

 
 future

 
 Menu

 
 0

 
 Do not print Sig Text on Canadian Imageable Cheques

 
       
 1

 
 Print Sig Text on Canadian Imageable Cheques

 
           
 
 CASADV01

 
 2.3

 
 Menu

 
 0

 
 Report part numbers with errors only, on CASE response to orders and returns.

 
       
 1

 
 Report all parts on CASE response to orders & returns.

 
           
 
 CASCODUP

 
 future

 
 phone

 
 0

 
 Request a Ship Code update from CASE every 14 days

 
       
 1

 
 Force a Ship Code update from CASE every time an order is finalized.

 
           
 
 CASDBOPT

 
 future

 
 phone

 
 0

 
 CSPS pre-edit – will send a price & availability transactions in order to show more types of errors.  Will slow down response.

 
       
 1

 
 CSPS pre-edit – will send availability transaction only and provide faster results.

 
       
  

 
  

 
 
 CASEAFTP

 
 future

 
 Menu

 
 0

 
 Case Order Fulfillment uses SNA

 
       
 1

 
 Case Order Fulfillment uses FTP