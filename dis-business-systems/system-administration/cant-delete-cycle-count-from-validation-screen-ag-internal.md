---
title: "Can’t Delete Cycle Count from Validation Screen - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Can’t Delete Cycle Count from Validation Screen - AG Internal."
long_description: "This document provides internal system administration information about Can’t Delete Cycle Count from Validation Screen - AG Internal."
---

_Can’t Delete Cycle Count from Validation Screen - AG Internal_

Issue 

 If a value isn’t provided underneath the Parts column on the on the Validation screen, the cycle count cannot be deleted. 

  

 Solution 

 When there isn’t a value provided for the number of parts, the program thinks that the export/import is in process. In order to rectify, you will need to do the following: 

 Set the import dates back to null. 
 Change the date to 0001-01-01 
 Change the time to 00.00.00 
 Enter 1 in the Export Count field. 

 Once completed, you should be able to delete the record.