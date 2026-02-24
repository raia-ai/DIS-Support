---
title: "EasyFile Documents WILL NOT Transfer with Reassign Option - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about EasyFile Documents WILL NOT Transfer with Reassign Option - Ag Internal."
long_description: "This document provides internal system administration information about EasyFile Documents WILL NOT Transfer with Reassign Option - Ag Internal."
---

_EasyFile Documents WILL NOT Transfer with Reassign Option - AG Internal_

Issue 

 Customer wants to know if there is a way to recover easy file documents that were on a POS document but has since been reassigned. 

  

 Solution 

 The reassign function intentionally does not copy that information over. The choice to not copy that information over was done in an attempt to alleviate accidentally transferring incorrect information. The logic is that a work order could be accidentally opened up to the wrong account and the unit information or Easy File information could then be incorrect as well.