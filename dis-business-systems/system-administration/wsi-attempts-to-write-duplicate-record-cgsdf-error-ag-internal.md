---
title: "WSI Attempts to Write Duplicate Record (CGSDF) Error - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about WSI Attempts to Write Duplicate Record (CGSDF) Error - Ag Internal."
long_description: "This document provides internal system administration information about WSI Attempts to Write Duplicate Record (CGSDF) Error - Ag Internal."
---

Issue 

 When performing GL Import the customer receives the following WSI error: 

 WSI attempts to write duplicate record (C G S D F). 

 This occurs when a .csv file containing more than 999 lines is attempted to be imported. 

 Note : Each line increases by increments of 10. Line 9990 is actually line 999. 

  

 Solution 

 Cancel the Create Source Document. 

 Keep any necessary AUTO lines and reduce the .csv file to 999 lines or less. 

 Complete the import process again.