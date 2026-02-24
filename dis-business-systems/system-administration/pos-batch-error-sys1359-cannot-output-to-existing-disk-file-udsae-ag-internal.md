---
title: "POS Batch Error - SYS1359 Cannot output to existing disk file u.@dSAE - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about POS Batch Error - SYS1359 Cannot output to existing disk file u.@dSAE - AG Internal."
long_description: "This document provides internal system administration information about POS Batch Error - SYS1359 Cannot output to existing disk file u.@dSAE - AG Internal."
---

_POS Batch Error - SYS1359 Cannot output to existing disk file u.@dSAE - AG Internal_

Issue 

  A system operator error message displays as a result of two POS batches colliding . 

  

 Solution 

 Answer the error message with a 3. 

 Access the temp files by entering WRKF u .@* ( u = File Set) in a command line and clicking OK . 

 Are there SAE, SA7, and 5510 files? If so, display the 5510 temp file and do one of the following: 

 If 5510 temp file is blank, delete it. They can then review and post the batch. 
 If 5510 temp file has tickets, display the SAE file. If SAE file is blank, have them go into Create POS Batch and take the option to Recover. They can create the batch now or at a delayed time. 
 If both SAE and 5510 files have tickets, do the following: