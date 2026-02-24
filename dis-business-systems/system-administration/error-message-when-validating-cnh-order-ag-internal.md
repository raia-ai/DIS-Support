---
title: "Error Message When Validating CNH Order - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Error Message When Validating CNH Order - AG Internal."
long_description: "This document provides internal system administration information about Error Message When Validating CNH Order - AG Internal."
---

_Error Message When Validating CNH Order - AG Internal_

Issue 

 Receive error message 'java.lang.RuntimeException: Unexpected error: java.security.InvalidAlg'  when trying to validate a CNH order. 

  

 Solution 

 PC must have updated Java. 

 Access Environment Variables (Control Panel | All Control Panel Items | System>Advanced System Settings>Environment Variables) and look for bin in path. 

 Check C:\Program Files (x86)\Java\jre1.8.0_181 for bin folder. 

 Is there a 191 version that has the bin folder? updated the path to C:\Program Files (x86)\Java\jre1.8.0_191\bin