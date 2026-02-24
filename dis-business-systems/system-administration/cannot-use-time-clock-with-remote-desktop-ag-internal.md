---
title: "Cannot Use Time Clock with Remote Desktop - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Cannot Use Time Clock with Remote Desktop - AG Internal."
long_description: "This document provides internal system administration information about Cannot Use Time Clock with Remote Desktop - AG Internal."
---

_Cannot Use Time Clock with Remote Desktop - AG Internal_

Issue 

 User is unable to use Remote Desktop. 

  

 Solution 

 Adding this registry key will fix the problem 

 Pathway - HKEYCURRENTUSER\SOFTWARE\TERMINAL SERVER CLIENT 

 Add key - RDGClientTransport     

 Change value to - 0X00000001