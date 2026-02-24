---
title: "Restore File Message Received when Opening Archived Document – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Restore File Message Received when Opening Archived Document – AG Internal."
long_description: "This document provides internal system administration information about Restore File Message Received when Opening Archived Document – AG Internal."
---

Issue 

 Customer receives a message stating they need to restore a file when opening an Archived Document. This is often caused by a server migration where the files didn’t get moved over or have been moved over in preparation for the migration. 

 

  

 Solution 

 The Files are usually under a file name of RSG or RSG2. Confirm the file name using the WRKF command. 

 Once the name of the file where the archived documents are stored is located, run the RSTOBJ command to pull the files back to the customer’s system as shown in the screenshots below.