---
title: "Find a Sales Tax Variance - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Find a Sales Tax Variance - AG Internal."
long_description: "This document provides internal system administration information about Find a Sales Tax Variance - AG Internal."
---

_How to Find a Sales Tax Variance - AG Internal_

Causes of Sales Tax Report Variance 
 Unit trade-in sales codes that credit a hardcoded inventory account will result in a variance if the inventory account is modified in batch. 
 Sales codes using the P Format with a credit to *SALE will trigger errors in the batch process if a new vendor is added in parts but not set up in vendor/class maintenance. 
 A sales code that credits a GL account, but the "Use on Tax Report" setting is set to "No" in GL maintenance. 

 Note: The following SQL command will display all GL accounts with a value not set to blank, which corresponds to "Determined by system automatically" in Quantum. 
 DISSQL REQUEST('SELECT GLTFLG, GLDIV, GLACWO, GLTITL FROM glm WHERE GLTFLG <> '' ''') 
  
 How to Find a Sales Tax Report Variance 
 Run the Sales Tax Report for the GL Period with the same parameters are the customer. 
 Then run the Sales Tax report with no exclusions if they have exclusions and check again to see if it is in balance. 
 Check the Sales Tax report for the variance.  Make a note of the variance. 
 Go to: POS | Table Maintenance | Tax Configuration | Tax Code Maintenance to see which tax codes are taxable and which tax codes are non-taxable. 
 Run PFVARTAX Are there any amounts that look like the out of balance amount that you noted in set 3? (There can be rounding error with tax so if it's within a few cents of the amount it's worth looking at.
 Look at the POS ticket and Source Document Inquiry on that ticket to see if the tax amounts match. 
 Make note of the report transactions.

 
 Run Sales Code report and check for any that are not tied to a sales account. Does the trade in account have *Trade (that helps if it does).
 If you find a Sales Codes that doesn't not hit a sale account, Go to Accounting | General Ledger |  Account Inquiry.  Enter the Credit Account GL Account Number from the Sales Code and got to the Transactions screen.  Look for transactions in the GL month in which your Sales Tax report is out of balance.  You can us the Filter option help with this.  Then, Look at the 3rd position of the description.  Look for any Tax code that is taxable.  Make note of the amounts to figure out the tax rate and the tax amount amount.  Note: Debit amount would be a negative tax amount, Credit would be a positive. 
 Look for P format Sales codes with the Credit account of *Sale. There can also be an issue if vendor/class assignment is missing for the Vendor/Class.

 
 Use Data Mine - Category = Accounting and SubCategory = Sales Tax History Query Filter on the division that is out of balance. Compare this to the GL for sales tax account (not everything is in the sales tax history file so you will need to compare to what actually posted. 
 Add formula left (doc description,2) to get sales codes.
 Compare these to the GL Account transactions for Tax Document that is not in the Sales tax report Datamine excel.
 Also, consider potential rounding issues if you are out a few cents. Take the rate/100*Document Total and compare that to the Total tax amount.  Add up the variances usually these are a few cents out altogether.

 

 ***This document is a work in process.  Please submit additions as you find more ways to hone in on and OOB.***