---
title: "RPG9029 Options ( 123F) Cannot Allocate record to file GLC Error Message - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about RPG9029 Options ( 123F) Cannot Allocate record to file GLC Error Message - Ag Internal."
long_description: "This document provides internal system administration information about RPG9029 Options ( 123F) Cannot Allocate record to file GLC Error Message - Ag Internal."
---

_RPG9029 Options ( 123F) Cannot Allocate record to file GLC Error Message - AG Internal_

Issue 

 Document doesn’t show as posted even after posting in Create Source Documents or Point of Sale and a message displays under System Operator Messages stating RPG9029 Options (123F) Cannot Allocate record to file GLC . 

  

 Solution 

 If the error message is displayed under System Operator Messages, look in the temp files or select Take Workstation ID ( System | Accounting Only | Take  Workstation ID ) and see it there is a description of Post Source Documents for your session. If there is, answer the message with 3. 

 Select Create Source Documents , create an empty batch, and try to post it. A pop up option to RECOVER a previous batch should display. 

 Select the option to recover. The lost item should now be able to be posted.