---
title: "Don’t Print Either Signature Line on Laser Check - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Don’t Print Either Signature Line on Laser Check - Ag Internal."
long_description: "This document provides internal system administration information about Don’t Print Either Signature Line on Laser Check - Ag Internal."
---

_Don’t Print Either Signature Line on Laser Check - AG Internal_

Issue 

 Customer has laser checks that are pre-printed with both signature lines. 

 While there is a setting in Electronic Forms to disable the 2 nd signature line, one signature line will always print by default. 

  

 Solution 

 This procedure will disable both signature lines. 

 File LIBRARY/LSRPCLPF may need to be modified from release to release.  Note that not every release will replace this file. 

 UPDDTA FILE(LIBRARY/LSRPCLPF) 
 Type in the key as follows and press enter: 

 LPFRMC: CK******01 

 LPSEQ:  070 

 If the record is not found the file has not been replaced in this release so nothing else needs to be done. 
 If the record is found, press F23 twice to delete it. 
 Repeat the second and fourth bullet point for each of the following keys: 

 LPFRMC: CK******01 

 LPSEQ:  071 

 LPFRMC: CR******01 

 LPSEQ:  070 

 LPFRMC: CR******01 

 LPSEQ:  071