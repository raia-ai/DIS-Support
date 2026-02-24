---
title: "Reclaim PO Batch from Specified Date - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Reclaim PO Batch from Specified Date - AG Internal."
long_description: "This document provides internal system administration information about Reclaim PO Batch from Specified Date - AG Internal."
---

_Reclaim PO Batch from Specified Date - AG Internal_

Introduction 

 If a PO batch gets deleted before posting, there is not a Keystone application to reclaim the PO's as there is with the POS documents. The batch can be reclaimed via SQL. 

  

 To Reclaim Batch 

 Run these two SQL's to clean up any bad data in BAA and BAM: 

 DISSQL REQUEST('update baa set bapdat = 0 where hex(bapdat) = ''404040404040''') 
 DISSQL REQUEST('update bam set bmpdat = 0 where hex(bmpdat) = ''404040404040''') 

  

 Use this SQL to find the documents: 

 DISSQL REQUEST('select distinct bapo# from baa where bapdat = yymmdd and badiv = ''d'' order by bapo#') OUTPUT(*PRINT) 

 Confirm these are all and the only documents that need to be reclaimed. If there are additional POs listed, they will need to be deleted from the batch to avoid double posting. 

  

 Make backup copies of BAA and BAM 

  

 Run these SQL's to reclaim the POs: 

 DISSQL REQUEST('update baa set bapost = '' '' where badiv = ''d'' and bapdat = yymmdd') 
 DISSQL REQUEST('update bam set bmpost = '' '' where bmpost = ''Y'' and bmpdat = yymmdd and bmdiv = ''d''') 

 Note : Do not 'blank' the BAPDAT or BMPDAT fields as it is not necessary & they could be used as a marker should you need to change something.