---
title: "Financial Statement Out of Balance - Troubleshooting Processes - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Financial Statement Out of Balance - Troubleshooting Processes - Ag Internal."
long_description: "This document provides internal system administration information about Financial Statement Out of Balance - Troubleshooting Processes - Ag Internal."
---

_This article has combined existing articles on troubleshooting why the Financial Statement is out of balance OOB_

Introduction 

 This article provides multiple troubleshooting suggestions to determine why a Financial Statement is out of balance. This article is a working document and will be added to as additional information becomes available. 

 Click on each option to display the associated trouble shooting procedure: 

  

 
 Use TRW to Find OOB Financial Statement 
  

 Summary TRW’s can be done on the GL month, division, and the sort by the transaction date to see the date it went out.  Next, a TRW can be done on the date and divisions sorted by document number also summary. 

 In this example Nov of 2024 is out of balance, H division. 

 

 01 - general ledger, 01- subtotal desired, Y to summary 

 

 13 (GL month) = N for November, 05 (GL account) = H!!!!!!!) 

 

 Press Enter to save changes, then Cmd2 to continue to sort specification 
 02 (post date) = 111111 (wildcard) 

 

 Press Enter to save changes, then Cmd1 to run report. 
 Review the report and find day difference. In this case 11/8/2024 is the day the report is out of balance 

 

 Create another TRW 
 01 - general ledger, 01- subtotal desired, Y to summary 

 

 (02) Post date = to date of out of balance 
 (05) Account = H!!!!!!! (wildcard) 

 

 Press Enter to save changes, then Cmd2 to sort specification 

 

 Sorted by document number (03) = 1111111111 (wild card) 
 Look at the report to find the out of balance document number, in this case 4633 
 Confirm the document number with the user/dealership and proceed with a resolution. 

 
  

  

 
 Trial Balance and Financial Statement out of Balance (Use SQLs to Locate Accounts that were Deleted or Don’t Exist) 
 Issue            

 This might be a result of a transaction in CUA assigned to a General Ledger Maintenance account that has been deleted or doesn’t exist. 

  

 Solution     

 Use these SQL's to find the issue: 

 To locate deleted accounts: Type DISSQL in a command line and click OK . Copy the SQL request below and paste it on the screen that opens, then click Enter . 

 select cudiv, cuacc7 from cua where cudiv||cuacc7 in (select gldiv||glacwo from glm where gldel = '*') 

 If an account number displays, access it through Account Maintenance (Accounting | General Ledger | Account Maintenance) and re-instate it. 

  

 To identify accounts that don’t exist: Type DISSQL in a command line and click OK . Copy the SQL request below and paste it on the screen that opens, then click Enter .                    

 s elect cudiv, cuacc7 from cua where cudiv||cuacc7 not in (select gldiv||glacwo from glm) 

 If an account number displays, add it through Account Maintenance (Accounting | General Ledger | Account Maintenance). 

 Rerun the Trial Balance and Financial Statement and confirm that they are  are now correct. 

 
  

  

 
 Look for Issues with Cost of Sales Configuration 
  

 COS Sales Accounts need to be assigned to a Sale Account to show on the Financial Statement. They should only be assigned to 1 Sale account 

 Select Account Maintenance (Accounting | General Ledger | Account Maintenance) . 
 Click Link Divisions . 
 Click Exception Report . 

 

 Enter group number in provided fields to choose the division you want to print. 
 Click Submit Report . 
 Access the file labeled as X14802. The following reports are listed at the bottom if applicable: 

 COS Accounts not assigned to Sales Accounts 
 COS Accounts assigned to more that one Sales Account 
 COS Accounts Tied to Deleted Sales Account 

 Work with the customer to resolve all issues on this report.