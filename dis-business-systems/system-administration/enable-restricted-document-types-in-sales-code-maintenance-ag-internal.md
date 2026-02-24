---
title: "Enable Restricted Document Types in Sales Code Maintenance – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Enable Restricted Document Types in Sales Code Maintenance – Ag Internal."
long_description: "This document provides internal system administration information about Enable Restricted Document Types in Sales Code Maintenance – Ag Internal."
---

Issue 

 The user can’t restrict document types in Sales Code Maintenance because the option is not enabled / the Restricted Docs Type field does not display. 

  

 Solution 

 Select AS/400 Command Line (System | AS/400 Command Line). 

 

 Type X00081 POSSCDOC,1 in the command line and click OK . The Restricted Doc Types field now displays in Sales Code Maintenance allowing the user to create sales code restrictions. 

 

 To disable this option, enter X00081 POSSCDOC,0 in a command line.