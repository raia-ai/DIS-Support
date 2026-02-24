---
title: "How to get a list of Parts Sync divisions setup - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about How to get a list of Parts Sync divisions setup - Ag Internal."
long_description: "This document provides internal system administration information about How to get a list of Parts Sync divisions setup - Ag Internal."
---

_How to get a list of Parts Sync divisions setup - AG Internal_

Issue: 
 The dealer wants a list to see what vendor codes are set up for Parts Sync.
   
 Solution: 
There is not a specific report but you can use SQL to pull from the parts sync file IVSD.
 This SQL will show you this information: DISSQL REQUEST('select * from ivsd') output(*print)