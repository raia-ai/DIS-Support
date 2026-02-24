---
title: "Advanced Tax Conversion – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Advanced Tax Conversion – AG Internal."
long_description: "This document provides internal system administration information about Advanced Tax Conversion – AG Internal."
---

Conversion Timing & Requirement 

 There is no required date, such as the first or last day of the month, for switching to Advanced Tax. 
 Before running the conversion, all closed documents must be posted to the General Ledger (GL). 
 The command to run conversion from standard tax to advanced tax is STD2ADV . 

 Impact on Tax Reporting 

 If the switch to Advanced Tax occurs mid-month, the tax report will still generate correctly. 
 Key changes after conversion: 
 Tax codes will now include the division code as the second character (e.g., the previous 'T' code becomes 'TA', 'TB', etc.). 
 Transactions before the switch will display a single-character tax code in the tax report’s description field, while transactions after the switch will show a two-character code. 
 All divisions will have access to all tax codes in the system, not just those assigned to their division. 

 Handling Shared Tax Codes Across Divisions 

 If multiple divisions use the same tax code, the system will append a division-specific second character to distinguish them post-conversion. 
 All areas where tax codes were previously assigned (e.g., Receivables, Address Maintenance) will automatically update to reflect the two-character code. 
 No new tax code assignments are required—existing assignments will remain unchanged. 

 Pre-Conversion Setup & Considerations 

 The key preparation step is ensuring all closed POS documents are posted. 
 Verify that there are no delayed batches pending before proceeding with the conversion.