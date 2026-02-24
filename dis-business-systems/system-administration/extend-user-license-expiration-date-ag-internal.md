---
title: "Extend User License Expiration Date – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Extend User License Expiration Date – Ag Internal."
long_description: "This document provides internal system administration information about Extend User License Expiration Date – Ag Internal."
---

Issue 

 User License expiration date has passed, and user can no longer sign in. 

  

 Solution 

 Connect to the customer’s system using Mocha.  

 

 Enter the bolded information below in the listed field: 

 User : SUPPORT 
 Password : PUGET 
 Program/procedure : *none 
 Menu : Main 

 Open a Command Line ( Alt + A ), type addlible disfiles , and press Enter . 

 Open another Command Line ( Alt + A ), type clibaslic , and press Enter . 

 

 Press F17 . 

 

 On this screen change LED (License End Date) to a later date.  

 Press Enter to save, F2 to continue, and F3 to exit.