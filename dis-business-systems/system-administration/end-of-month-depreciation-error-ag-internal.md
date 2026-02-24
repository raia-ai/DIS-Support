---
title: "End of Month Depreciation Error – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about End of Month Depreciation Error – Ag Internal."
long_description: "This document provides internal system administration information about End of Month Depreciation Error – Ag Internal."
---

Issue 

 Customer receives the following error when attempting to create depreciation: 

 A depreciation posting batch cannot be created for this division. Either a depreciation posting batch has already been posted to the oldest open general ledger month, or there are no units which need to be depreciated. 

 
 Solution 

 Select AS/400 Command Line (System | AS/400 Command Line). 

 

 Type WRKF MASP and click OK . 

 

 Type UPDDTA MAI in the command line at the bottom of the screen and click Enter . 

 Press the Page Down key on your keyboard until the correct MAI division is displayed. 

 

 Type 0 in the MAI Depreciation Switch field and click Enter to flip the switch.