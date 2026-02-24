---
title: "Kubota Trial Balance Troubleshooting - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Kubota Trial Balance Troubleshooting - Ag Internal."
long_description: "This document provides internal system administration information about Kubota Trial Balance Troubleshooting - Ag Internal."
---

_Kubota Trial Balance Troubleshooting - AG Internal_

Issue 
 An Out of Balance message similar to the following is received: 
 
   
 Solution 
 Perform the following troubleshooting steps to resolve the issue 
 Check the Financial Statement Balance in Quantum 

 Verify the financial statement is in balance 

   
 If Balanced, resend GL Data to Middle Tier 

 Resend the GL data to the Middle Tier if the financial statement is in balance. 
 Sign in as SUPPORT and execute the PR_SENDGL command from an AS/400 command line. 

 
   
 Monitor the Resending Process 

 Enter WRKACTJOB SBS(DISPRISM) in a command line to monitor the progress of the data resend. 

 Note : The resend process may take up to an hour. 
 
   
 If financial statement is still out of balance, recalculate the GL Data 

 If the financial statement is still out of balance, enter DMGLFIX in a command line. This command recalculates the DMGLDET & DMGLSUM files for the last 25 closed months as well as the current months, keeping older Summary totals unchanged. 

   
 Verify DMGLSUM data with SQL Queries 

 Confirm the recalculated data in the DMGLSUM file using SQL queries for different types. 

 The GSMYnn field depends on the fiscal start. In this case, with a fiscal start in January (the first month), December GL period is represented as the 12 th month. 
 Open the Excel spreadsheet attached at the bottom of this article and use the figures from the below SQL’s to help with the calculation described. 

   
 Assets 
 DISSQL REQUEST('select SUM(GSMY12) from dmglsum1 where GSYYYY = 2022 AND GSTYPE = ''A''') 
   
 Liabilities 
 DISSQL REQUEST('select SUM(GSMY12) from dmglsum1 where GSYYYY = 2022 AND GSTYPE = ''L''') 
   
 Sales & Income 
 DISSQL REQUEST('select SUM(GSMY12) from dmglsum1 where GSYYYY = 2022 AND GSTYPE = ''S'' or GSYYYY = 2022 AND GSTYPE = ''I''') 
   
 COS & Expense 
 DISSQL REQUEST('select SUM(GSMY12) from dmglsum1 where GSYYYY = 2022 AND GSTYPE = ''C'' or GSYYYY = 2022 AND GSTYPE = ''E''') 
   
 The net difference between Assets minus Liabilities should equal the difference of Sales & Income minus COGS & Expenses. 
 (Assets - Liabilities) = (Sales & Income) - (COGS & Expenses)