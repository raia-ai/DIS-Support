---
title: "Datamining Check Register Report - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Datamining Check Register Report - Ag Internal."
long_description: "This document provides internal system administration information about Datamining Check Register Report - Ag Internal."
---

_Datamining Check Register Report - AG Internal_

Datamining Check Register Report 
 If, for any reason, a user’s Check Register Report doesn’t print, they can do a data mine for the information they need.  This is how to build the query: 
 Category : Accounting 
 Subcategory : Payable Check Register Query 
 Fields : Division (if they have more than one) 
 Check: Date (CCYYMMDD) 
 Check: Number 
 Check: Amount 
 Check: Vendor# 
 Check: Vendor Name 
 GL Account: Payable 
 GL Account: Bank 

 
 Filters : Exact Division (If necessary) 
 Exact Check: Date (CCYYMMDD) 
 Any others you may need 

 

 If the Payable Check Register Query subcategory isn’t available, it can be turned on using a secret OPT. 
 Go to System > AS/400 Command Line or press Alt + A. 
 Put in this command: X00081 KEYDMREG,1   (Quantum Data Mine does not require that this opt be set.) 
 Press Enter 
 Log out of all sessions, then log back in 

 After that, Payable Check Register Query should be available as a subcategory.