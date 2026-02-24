---
title: "Fix POS Print Job Errors - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Fix POS Print Job Errors - AG Internal."
long_description: "This document provides internal system administration information about Fix POS Print Job Errors - AG Internal."
---

_Fix POS Print Job Errors - AG Internal_

Issue  

 User who starts a POS print job doesn’t have all the proper user authorities and a system operator message such as the following displays: 

 Message . . . . :   SYS3827 Options (0  3)     

                  Error occurred on a CL command 

  

 Solution 

 Display the message and press F9 to find the user ID that caused the issue. 

 Answer message with a 3. 

 Check the user set up by entering WRKUSRPF *all (or user id instead of *all) on a command line and clicking OK . Each user ID should have at least these 5 set up: 

 *ALLOBJ 
 *IOSYSCFG 
 *JOBCTL 
 *SAVSYS 
 *SPLCTL 

 The *JOBCTL and *SPLCTL options cause POS print job issues if the user ID doesn’t have them. 

 Add authority that is missing on the user ID. 

 Open a command line and separately enter the following to generate reports and view any lines on POS tickets that need to be fixed: 

 BIGP 
 BIGS 
 BIGD 
 BIGN 

 If information similar to below displays on the reports, the customer will need to go into the POS ticket, select to edit the line that has the part #’s with an issue, and click Enter so the background process can record correctly.