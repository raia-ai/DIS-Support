---
title: "Units G/L Period or Inventory/Flooring Report Totals Don't Match G/L Totals - Things to check - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Units G/L Period or Inventory/Flooring Report Totals Don't Match G/L Totals - Things to check - Ag Internal."
long_description: "This document provides internal system administration information about Units G/L Period or Inventory/Flooring Report Totals Don't Match G/L Totals - Things to check - Ag Internal."
---

_Units G/L Period or Inventory/Flooring Report Totals Don't Match G/L Totals - Things to check - AG Internal_

Units G/L Period or Inventory/Flooring Report Totals Don't Match  G/L Totals - Things to check 

  

 Typically the customer is running these reports for past months so it's a good idea to see where they are at in the current month to try to hone in on exactly where the issue is. 

 Run a Current Inventory Report and an Units GL Period Report for the current month.   

 Note : The Current Inventory Repo rt Looks at the current cost amount on each unit in the WGI file for non-sold units.  This is the amount you see in the cost field when you look at the unit in Inquire/Update Units.  

 Note : The Units GL Period and Inventory Flooring Reports looks at the figures in the WHT file. 

   

 Do the totals match for each Inventory account? 

 No , you may have an issue with an improper total in the WHT file.  To find this, we will need a list of all non-Sold units in a specific inventory account.  Sorted by units number.  Then compare these figures to the Units GL Inventory Report figures for each unit t to see which unit(s) is/are causing an issue. When you find a unit with an issue.  Compare the Inventory entries on the unit to the totals in WHT to see what the issue is and correct accordingly.  

 Yes , check the prior months Units GL Period Reports to see where the totals start to get out of balance.  Looking for sales that happened during those months that may have attributed to the difference.  

                           

 Run a  Subledger Balance Report . Is it out of balance for any unit Inventory accounts? 

 If there is an out of balance: 

 - Check for overrides to the account that may have caused this.  This can be done by looking at the account in General Ledger Account Inquiry in either Keystone or Quantum and looking at the Override field in the transactions screen or you could run a datamine report to look for overrides.  

 - Check archived Subledger Balance Reports in the Accounting end of day section. Look month by month to see if you can hone in on when the subledger when out of balance. 

  

 ***This document is a work in process. As you find more items to check or corrections to this document please let Ruth know. ***