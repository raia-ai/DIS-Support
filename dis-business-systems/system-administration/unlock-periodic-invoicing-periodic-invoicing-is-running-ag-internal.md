---
title: "Unlock Periodic Invoicing (Periodic Invoicing is Running)- AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Unlock Periodic Invoicing (Periodic Invoicing is Running)- AG Internal."
long_description: "This document provides internal system administration information about Unlock Periodic Invoicing (Periodic Invoicing is Running)- AG Internal."
---

_Unlock Periodic Invoicing - AG Internal_

Issue 

 Periodic Invoicing will not run (becomes locked) due to a temporary file and the following message displays: 

 Periodic invoicing is already running for this division 

   

 Resolve Issue - Unlock Periodic Invoicing  

 If there isn’t actually a user in Periodic Invoicing, a dangling temporary file may need to be deleted. 

 Make sure there is no one else in Periodic Invoicing. 

 Open a Command line ( Alt + A ). 

 

 Type WRKF U .@* (where U is the File Set and there is a space between WRKF and U .@*). 

 Click OK . The Work the Files screen displays. 

 Search for a U . D 5530 file (where U is the File Set and D is the Division). In the example below the 5530 temp file is for File Set H and Division D. 

 

 Select the file and click Display physical file member .  

 IF the file is empty return to the Work With Files screen and delete the U . D 5530 temp file. 

 Run Periodic Invoicing again.