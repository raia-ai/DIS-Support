---
title: "Unable to Allocate a Record in File BKAUC - AG Internal - Quantum"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Unable to Allocate a Record in File BKAUC - AG Internal - Quantum."
long_description: "This document provides internal system administration information about Unable to Allocate a Record in File BKAUC - AG Internal - Quantum."
---

_Unable to Allocate a Record in File BKAUC_

Introduction 

 This article addresses a common batch-posting issue related to General Ledger processing. 

 Issue 

 Users may encounter an error message indicating that the previous batch is still being distributed, which prevents a batch from posting successfully. 

 

 Reason 

 In some cases, the previous batch may still appear to be in distribution because a system operator message is awaiting a response. This system operator message typically occurs when another user is accessing Check Reconciliation screen (Accounting | General Ledger | Check Reconciliation) at the time the batch is being posted, which temporarily locks the process and prevents the batch from completing. 

 Until this message is addressed, the batch process cannot be completed successfully. 

 

 

 

 Solution 

 To resolve the issue, follow these steps: 

 Navigate to AS/400 Command Line (System | AS/400 Command Line). 
 Enter the command DD to access the job display screen. 

 

 Review the Job Function column and look for a user with an entry beginning with X171.. which indicates active use of the Check Reconciliation screen. 
 Ask the identified user to exit the Check Reconciliation screen to release the file lock. 
 Once the screen is no longer in use, respond to the system operator message by entering R to clear it. 
 Retry posting the batch.