---
title: "Change Unit Aging in M360 Unit Inventory KPI - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Change Unit Aging in M360 Unit Inventory KPI - Ag Internal."
long_description: "This document provides internal system administration information about Change Unit Aging in M360 Unit Inventory KPI - Ag Internal."
---

_Change Unit Aging in M360 Unit Inventory KPI - AG Internal_

Issue 

 The customer wants to edit the aging days in the Unit Inventory KPI for Management 360. 

  

 Solution 

 In this example, the customer would like their aging categories to be 

 0-120 
 121-365 
 365+ 

  

 Begin by entering the following in a command line where u in FILE u  is the file set and the value is the end days for the first two aging categories: 

 CRTDTAARA DTAARA(FILEu/XQCQS008) TYPE(*CHAR) LEN(6) VALUE('120365') 

 If you get an error that it is invalid or already exists, then you would use this command where u in FILE u  is the file set and the value is the end days for the first two aging categories: 

 CHGDTAARA DTAARA(FILEu/XQCQS008) VALUE('120365') 

  

 Important! Users will just need to sign off Quantum and back on to see the changes.