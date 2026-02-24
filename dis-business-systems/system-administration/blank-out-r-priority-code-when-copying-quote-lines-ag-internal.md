---
title: "Blank out R Priority Code when Copying Quote Lines - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Blank out R Priority Code when Copying Quote Lines - Ag Internal."
long_description: "This document provides internal system administration information about Blank out R Priority Code when Copying Quote Lines - Ag Internal."
---

_Blank out R Priority Code when Copying Quote Lines - Ag Internal_

Issue 

 Customer wants to choose priority code as needed when copying quote lines. 

 When copying lines from a quote, there is an OPT to blank out the R priority code if desired. If you set the OPT to blank it out this allows the customer to choose the right priority code as needed when copying the lines. 

  

 Solution 

 Enter X00081 POSCOPYR and then a 0 on a command line if you want to blank out the R code. Enter X00081 POSCOPYR and then a 1 on a command line to not blank out the R code.