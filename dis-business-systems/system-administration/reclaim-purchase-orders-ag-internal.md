---
title: "Reclaim Purchase Orders - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Reclaim Purchase Orders - AG Internal."
long_description: "This document provides internal system administration information about Reclaim Purchase Orders - AG Internal."
---

_Reclaim Purchases Orders - AG Internal_

Issue 

 Purchase Orders were pulled into a Point of Sale batch, but not posted as the Point of Sale batch was cancelled. The tickets need to be unflagged as posted so they can be run through another batch. 

  

 Solution 

 Use this SQL to find the documents: 

 ===> DISSQL REQUEST('select distinct bapo# from baa where bapdat = yymmdd and badiv = ''d'' order by bapo#') OUTPUT(*PRINT) 

 Confirm these the only documents that need to be reclaimed. 

 Make backup copies of BAA and BAM files. 

 To reclaim individual PO’s where you already know the number use UPDDTA on the BAM file and change the Posted Flag from Y to blank. Next update the BAA Posting Flag from Y to blank. There will be a separate record for each line on the PO. 

  

 Run these SQL’s: 

 update baa set bapost = ' ' where badiv = 'd' and bapdat = yymmdd 

 update bam set bmpost = ' ' where bmpost = 'Y' and bmpdat = yymmdd and bmdiv ='d' 

 Do not ‘blank” the BAPDAT or BMPDAT fields as it is not necessary and could be used as a marker should you need to change something. 

  

 If you get SQL errors you many need to run these SQL’s first: 

 DISSQL REQUEST('update baa set bapdat = 0 where hex(bapdat) = ''404040404040''') 

 DISSQL REQUEST('update bam set bmpdat = 0 where hex(bmpdat) = ''404040404040''')