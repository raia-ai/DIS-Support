---
title: "Error Message CPF4101 Appeared During OPEN for File PIEH - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Error Message CPF4101 Appeared During OPEN for File PIEH - AG Internal."
long_description: "This document provides internal system administration information about Error Message CPF4101 Appeared During OPEN for File PIEH - AG Internal."
---

STOP! DO NOT COMPLETE THIS PROCESS   i f the dealership that received this error uses two-step purchase orders. Contact Mike S or Ruth K for assistance. 

 Important! This is NOT a batch recovery process. The batch in the temp files being deleted will need to manually re-entered. 

  

 

 Issue 

 A user receives the error message when they select Invoice Entry (Accounting | Payables | Invoice Entry) and cannot access the screen to create a new batch. 

 

 

   

 Solution 

 Have the user complete the following steps: 

 Enter a C for the response on the first error screen. The second error screen displays. 

 Enter a 3 for this response. The main Quantum/Keystone screen displays. 

 Select Take Workstation ID (System | Accounting Only | Take Workstation ID ).  Note the session ID currently running the Payables Invoice Entry job. 

 Select AS/400 Command Line (System | AS/400 Command Line). Enter the command WRKF u .@* where u is the File Set and click OK . 

 Delete all of the temp files for the session ID receiving the error. In the second screenshot above, the session ID is A6, so all of the u .@A6 temp files would be deleted. 

 Exit the temp files screen. 

 Select AS/400 Command Line (System | AS/400 Command Line). Enter the command UPDDTA CTL and click OK . 

 Page down on the screen that opens until you locate a file with the session ID in the CTL Session ID field and 5 in the CTL Option Number field. Delete those values and click Enter . 

 The Payables Invoice Entry job is ended for that session ID and the user can access Payables Invoice Enter and create a new batch.