---
title: "Error Message RPG9036 - Duplicate Keys Found While Adding Record to File REAUF - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Error Message RPG9036 - Duplicate Keys Found While Adding Record to File REAUF - Ag Internal."
long_description: "This document provides internal system administration information about Error Message RPG9036 - Duplicate Keys Found While Adding Record to File REAUF - Ag Internal."
---

_Error Message RPG9036 - Duplicate Keys Found While Adding Record to File REAUF - AG Internal_

Issue 

 A batch is not posted and has an error message on the WRKACTJOB or DD screen: 

 RPG9036 - Duplicate keys were found while adding a record to file REAUF 

 This message is a result of another batch job using the AR address  in which a randomizer in the REA file has been allocated to the same number.  This can happen when the customer is trying to post several batches around the exact same time.   

   

  

 Solution 

 Take option 3 and then recover the batch.  

 Do not take an option 0 is taken, the system will just move on and it doesn’t put the line it’s working on in the REA file.  

 In other words, it will post to the GL but be missing from the Receivables customer.