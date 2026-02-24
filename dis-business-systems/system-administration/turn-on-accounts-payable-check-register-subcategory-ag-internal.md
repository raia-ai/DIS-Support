---
title: "Turn on Accounts Payable Check Register Subcategory - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Turn on Accounts Payable Check Register Subcategory - AG Internal."
long_description: "This document provides internal system administration information about Turn on Accounts Payable Check Register Subcategory - AG Internal."
---

_Turn on Accounts Payable Check Register Subcategory - AG Internal_

Issue 

 The Accounts Payable Check Register Subcategory allows dealers to print their own check register which can be used to create a Positive Pay Register. 

 They could also create a file with this subcategory to upload, export, import, and/or email to their bank. 

  

 Solution 

 To Enable the Data mine Subcategory, 

 at a command line, type: X00081 KEYDMREG,1 and press enter.  (Quantum Data Mine does not require that this opt be set.) 

 Log completely off the the system and then log back on.  The Data mine Subcategory should now be available to use. It is under the Accounting Category. 

  

 This file, FILEu/PALOG, has data for Checks and Voids that includes the bank name, Account and Routing#, check amount, and the vendor name used when the check was printed (including misc. vendor ddd999). 

 Includes: Payable Checks (X12-7), Manual Checks (X12-8), and Cancel Checks (X12-9).