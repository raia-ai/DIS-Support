---
title: "Remove Asterisk Next to the Writer Name in WRKOUTQ - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Remove Asterisk Next to the Writer Name in WRKOUTQ - Ag Internal."
long_description: "This document provides internal system administration information about Remove Asterisk Next to the Writer Name in WRKOUTQ - Ag Internal."
---

_Remove Asterisk Next to the Writer Name in WRKOUTQ - AG Internal_

Issue 
 Sometimes when an LPR printer is created, an asterisk appears next to the writer. This seems to just happen with OS/400. 
  
 Solution 
 The printer still appears to work in every way, but here’s how to remove it. 
  
 Here’s the output queue of an LPR printer 
 
 If there is an * next to the writer, end the writer. In this example ENDWTR P2 and click Enter. 
 Refresh the screen and the output queue will look like this, with the writer named RMTW00000 x : 
 
 End that writer by typing ENDWTR RMTW00000X and clicking Enter 
 
 Restart the print writer as normal (STRRMTWTR P2 enter) and it should work fine from there.