---
title: "Print due date at the bottom of an invoice based on a set number of days from the close date (Custom opt ) - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Print due date at the bottom of an invoice based on a set number of days from the close date (Custom opt ) - Ag Internal."
long_description: "This document provides internal system administration information about Print due date at the bottom of an invoice based on a set number of days from the close date (Custom opt ) - Ag Internal."
---

_Print due date at the bottom of an invoice based on a set number of days from the close date (Custom opt ) - AG Internal_

We wrote a custom opt for a dealer called Next Lift in March of 2021.  

 It allows for an extra line at the bottom of an invoice that would print a due date calculated off the close date.  

 You can choose the Division, Document Classification code and Number of days to calculate the due date.  

  

 To set the OPT on: 

 At a menu, type X00081 CUST0344,1 and press enter.  

  

 Use UPDDTA to update the FILEu/X5DOCDUE file. 

   

 The 3 items to fill in: 

 DUEDIV - the division code 
 DUEDOCCLS - the POS document classification code 
 DUEDAYS - the number of days from the close date when the document becomes due  ( 15=15, 30=30, etc) 

  

  

 

  

 The rules: 

 It is available in Floor 57 

 This is a custom OPT and will need to be set by request – it is NOT in the OPT menu 

 This OPT is set by document type.  

 It’s very simple in the requirements, you simply tell it a # of days.  If you tell it you want “I” documents to have a due date 15 days out, it will calculate the due date 15 days out from the CLOSED date. 

 If you re-open a ticket and re-close, the due date will recalculate from the new close date, and there will be no record of the previous close date. 

 This will print on ALL tickets – regardless of payment type.  Even tickets flipped to CASH (or opened to CASH). 

 If they don’t like that, an option would be a new document type for Cash tickets 

  

 Here is the Jira ticket associated with the option.  

 https://jira-new.disdev.net/browse/QU-1172