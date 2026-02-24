---
title: "Generate Product Keys for Quantum – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Generate Product Keys for Quantum – Ag Internal."
long_description: "This document provides internal system administration information about Generate Product Keys for Quantum – Ag Internal."
---

Access and log in to the internal AS/400 called “THEBORG” - http://10.255.4.14/webclient/ for Quantum and 10.255.5.8 for the IBM server. 

 Note : Visit 1Password for connection and password information. 

 Once signed in, open a command line ( ALT + A on your keyboard) or ( System | AS/400 Command Line ). 
 Type CHGCURLIB PMSDIS in the command line and click OK . 
 Open a command line again ( Alt + A ). 
 Type GETPRD in the command line and click OK . 
 Fill in the DIS Group Code and Product fields and press Enter on your keyboard. 

 Note : The Group Code and Product can be found in through ( Security | DIS Product Key Setup). 

 The product key is automatically generated and displayed in the Product Key field. Insert this value into the Key field in ( Security | DIS Product Key Setup) in the system on which you are adding the new product.