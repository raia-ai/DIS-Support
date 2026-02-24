---
title: "Clear All Parts from a Group Code: Step-by-Step Guide - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Clear All Parts from a Group Code: Step-by-Step Guide - AG Internal."
long_description: "This document provides internal system administration information about Clear All Parts from a Group Code: Step-by-Step Guide - AG Internal."
---

_How to Clear All Parts from a Group Code: Step-by-Step Guide - AG Internal_

Introduction 
 A dealer may want to clear all parts from a specific group. While there's no direct menu option, you can use SQL commands to update the Group Code file (IGA). Here's a step-by-step guide: 
   
 Step 1: Make a Backup of IGA 
 Use the following command to make a backup copy of IGA, replacing 'u' with the File Set: CPYF FROMFILE(FILEu/IGA) TOFILE(FILEu/IGA101723) CRTFILE(*YES) 
   
 Step 2: Display parts in the Group 
 Use the following SQL command, replacing 'd' with the Division code and 'xx' with the Group Code: SELECT * FROM IGA WHERE IGADIV = 'd' AND IGAGRP = 'xx' 
   
 Step 3: Delete Parts from the Group 
 Once you've verified the parts in the group, you can delete them using the following SQL command: DELETE FROM IGA WHERE IGADIV = 'd' AND IGAGRP = 'xx' 
   
 Step 4: Verify Deletion 
 Verify the parts in the group have been deleted using the following SQL command: SELECT * FROM IGA WHERE IGADIV = 'd' AND IGAGRP = 'xx' 
   
 Conclusion 
 By following these steps, you can clear all parts from a specific group, allowing a dealer to start over. Remember to always create a backup copy of the file before making any changes.