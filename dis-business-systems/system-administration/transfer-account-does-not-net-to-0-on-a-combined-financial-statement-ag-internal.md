---
title: "Transfer Account does Not Net to 0 on a Combined Financial Statement – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Transfer Account does Not Net to 0 on a Combined Financial Statement – Ag Internal."
long_description: "This document provides internal system administration information about Transfer Account does Not Net to 0 on a Combined Financial Statement – Ag Internal."
---

_Transfer Account does Not Net to 0 on a Combined Financial Statement – Ag Internal_

Issue 

 A combined financial statement transfer account should always net to 0. If a transfer account does not net to 0 on a combined financial statement, it is likely a result of the dealership posting manual transactions to the account which is configured to only handle system generated transactions. 

  

 Solution 

 In this example D1800 is the dealership’s transfer account and the month of January is still open. 

 Select Transaction Report Writer and click OK to create a new report. The Specify Parameters screen displays. 

 

 Create a report to determine what day(s) the dealership posted manual transactions. 

 Click Forward . 

 

 Note the account has a “!” in place of the division code. Click Sort Specification . The Sort Order screen displays. 

 

 Select Posting Date for the field name and enter 111111 for the Sort Order. 

 Click Forward .  

 A summarized report is generated listing every posting day for the transfer account in the specified month.  Any day where the debits do not equal the credits are manual entries. 

 Run another TRW similar to above but do not select the Print Summary Report check box.  On the second screen add a third line for the specific transaction date(s) you identified on the first report and click Save & Start Report.  

 The second report provides the detailed transactions.  Display the document(s) in Source Document Inquiry to see the full transaction. Use the available information to help the dealership make correcting entries as appropriate.