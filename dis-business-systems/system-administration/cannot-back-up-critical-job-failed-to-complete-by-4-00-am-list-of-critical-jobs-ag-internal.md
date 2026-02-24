---
title: "Cannot Back up -- Critical Job Failed to complete by 4:00 am ! - List of Critical Jobs - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Cannot Back up -- Critical Job Failed to complete by 4:00 am ! - List of Critical Jobs - Ag Internal."
long_description: "This document provides internal system administration information about Cannot Back up -- Critical Job Failed to complete by 4:00 am ! - List of Critical Jobs - Ag Internal."
---

_Cannot Back up -- Critical Job Failed to complete by 4:00 am ! - List of Critical Jobs - Ag Internal_

Introduction 

 Occasionally the system does not backup due to a critical job running on the system.  The backup will keep trying until 4:00am and then the job will end itself. The following is an example of the message in the System Operator message queue.  

  

 Cannot Back up -- Critical Job failed to complete by 4:00 am ! 
     From . . : DISBACKM 06/24/21 04:03:24   

  

 How do we know what job caused the issue? 

  

 Solution 

 When backup ends it will print a list of jobs running on the system at that time. It may still be on the print spool under user DISBACKu (where 'u' is the fileset) or it may have printed. Review the printout against the list below to figure out which jobs caused the backup to not be able to run.  

  

 This is a list of the Critical jobs that will cause the backup not to run: 

 X1A001 - Accounting End Of Month 
 X1A201 - Combined End-of-month 
 X1A202 - Combined End-of-month 
 X1CA00 - Sold Units Purge 
 X1C400 - Depreciation End of Year 
 X1C500 - Receivables Files Maintenance 
 X1C600 - Payables Files Maintenance 
 X1C701 - General Ledger File Maintenance 
 X1C800 - Rentals End of Year 
 X13000 - Payroll Entry Screen 
 X3A001 - Parts End Of Month 
 X34110 - Create Stock Order 
 X34150 - Print Suggested Order   
 X34800 - Corporate Stock Order 
 X37200 - Automatic Price Update 
 X54001 - Point Of Sale End Of Month 
 X54201 - Combined POS End-of-month 
 X55100 - Post POS Documents 
 X55101 - Post POS Documents 
 X79100 - Restore Bearing Interchange 
 X00041CL - Mobile sync   

 This list was copied from SC400 solution record A03294 which was created 04/06/2009. 

 The procedure looking for the critical job is X60097.