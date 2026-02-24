---
title: "Rebuild Parts Data Mine Files When There Are Duplicate Keys - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Rebuild Parts Data Mine Files When There Are Duplicate Keys - AG Internal."
long_description: "This document provides internal system administration information about Rebuild Parts Data Mine Files When There Are Duplicate Keys - AG Internal."
---

_Rebuild Parts Data Mine Files When There Are Duplicate Keys - AG Internal_

Issue 

 Backup doesn’t complete and there is a message such as Records in member DMPIMI have duplicate keys . 

  

 Solution 

 Rebuild the Data Mine files or it will continue to happen, and nightly backup will continue to fail. 

 End the QDISDMPIM u job where the u = file set. 
 Check for any locks on the two data mine files using by typing these commands on a command line and ending any jobs holding locks
WRKOBJLCK OBJ(DMPIMI) OBJTYPE(*FILE)
WRKOBJLCK OBJ(DMPIOI) OBJTYPE(*FILE)  
 Use CLRPFM on the DMPIMI, DMPIOI files. 
 CLRPFM DMPIMI 
 CLRPFM DMPIOI 

 Enter PFDMPALL on a command line to rebuild the DM files.