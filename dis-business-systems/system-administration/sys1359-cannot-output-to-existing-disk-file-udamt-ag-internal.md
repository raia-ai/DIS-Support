---
title: "SYS1359 - Cannot output to existing disk file u.@@DAMT - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about SYS1359 - Cannot output to existing disk file u.@@DAMT - Ag Internal."
long_description: "This document provides internal system administration information about SYS1359 - Cannot output to existing disk file u.@@DAMT - Ag Internal."
---

_SYS1359 - Cannot output to existing disk file u.@@DAMT - Ag Internal_

Issue 

 Backup getting an error SYS1359 Cannot output to existing file u.@@DAMT. 

 This is a temp file that gets created during Accounting EOD jobs and relates to the reorg of the Daily Maintenance Log files. 

   

 Solution 

 Answer the message with a 3 and end backup off the user board. 

 Release the QBATCH and ECM like normal. 

 WRKDTAARA EPCLOCK* and delete any EPCLOCK data areas if they show. 

 You then want to delete the u.@@DAMT file so backup can complete normally the next time it runs.