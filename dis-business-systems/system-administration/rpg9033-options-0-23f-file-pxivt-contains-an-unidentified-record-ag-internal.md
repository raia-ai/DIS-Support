---
title: "RPG9033 Options (0 23F) File PXIVT contains an unidentified record - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about RPG9033 Options (0 23F) File PXIVT contains an unidentified record - Ag Internal."
long_description: "This document provides internal system administration information about RPG9033 Options (0 23F) File PXIVT contains an unidentified record - Ag Internal."
---

_RPG9033 Options (0 23F) File PXIVT contains an unidentified record - AG Internal_

Issue 

 Parts orders are being held up and the error message RPG9033 Options (0 23F) File PXIVT Contains an Unidentified Record displays in System Operator Messages, there are parts on an order with blank class code assigned to them. 

   

  

 Solution 

 Simultaneously press the ALT + A keys on your keyboard, type X59A00 and click OK . A report prints listing parts that don’t have a class code assigned. 

 Select Parts Posting and Maintenance (Parts | Parts Posting and Maintenance) and assign a class code to each of the parts listed on the report. 

 Once class codes have been assigned, return to the error message and answer it with a 0. The orders should start releasing.