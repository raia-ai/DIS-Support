---
title: "Manually “Reclaim” a Batch of Purchase Orders that were Cancelled out of a Batch for an Entire Date - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Manually “Reclaim” a Batch of Purchase Orders that were Cancelled out of a Batch for an Entire Date - AG Internal."
long_description: "This document provides internal system administration information about Manually “Reclaim” a Batch of Purchase Orders that were Cancelled out of a Batch for an Entire Date - AG Internal."
---

_Manually “Reclaim” a Batch of Purchase Orders that were Cancelled out of a Batch for an Entire Date - AG Internal_

Issue 

 A customer cancelled their Point of Sale Posting batch that included Purchase Orders and want to “Reclaim” it. 

  

 Solution 

 Use this SQL to find/verify the documents: 

  ===> DISSQL REQUEST('select distinct bapo# from baa where bapdat = yymmdd and badiv = ''d'' order by bapo#') OUTPUT(*PRINT) 

 Where yymmdd = the posting date and d = their division letter. 

 Confirm these are all of the only documents that need to be reclaimed and there aren’t any additional. 
 Make backup copies of BAA and BAM 
 Type DISSQL enter and then paste in the following: 

 update baa set bapost = ' ' where badiv = 'd' and bapdat = yymmdd 

    

 Type DISSQL enter and then paste in the following: 

 update bam set bmpost = ' ' where bmpost = 'Y' and bmpdat = yymmdd and bmdiv = 'd' 

   

 Important! Do not 'blank out' the BAPDAT or BMPDAT fields as it is not necessary & they could be used as a marker should you need to change something. 

 If you get SQL errors, you may need to run these SQL's first:     

 DISSQL REQUEST('update baa set bapdat = 0 where hex(bapdat) = ''404040404040''') 
 DISSQL REQUEST('update bam set bmpdat = 0 where hex(bmpdat) = ''404040404040''') 

  

 SC400 Solution Record A03417