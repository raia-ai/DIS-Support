---
title: "Delete Previously Saved Credit Cards - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Delete Previously Saved Credit Cards - AG Internal."
long_description: "This document provides internal system administration information about Delete Previously Saved Credit Cards - AG Internal."
---

Introduction 

 When customers switch to a new card processor, previously saved credit cards are no longer valid—even when moving from Gravity Legacy to Gravity eMerge. It's also best practice, for security reasons, not to save or retain old credit card information. 

 These SQLs will help identify and delete previously saved credit cards by card code. Refer to this article for instructions on how to pull a list of all customers with a credit card on file. 

 Note : Make a backup copy of RCC before deleting anything. 

 Display Saved Cards by Card Code 

 Use this SQL to display credit cards by card code (e.g., "AE" for American Express): 

 DISSQL REQUEST('select * from RCC where F0O3CD = ''AE''') 

 Delete Saved Cards by Card Code 

 Use this SQL to delete saved credit cards by card code: 

 DISSQL REQUEST('delete from RCC where F0O3CD = ''AE''') 

 After running the delete command, confirm the cards were removed by running the SELECT command again.