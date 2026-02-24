---
title: "Resolve Display Program Message Issue / GHOST Output Queue – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Resolve Display Program Message Issue / GHOST Output Queue – Ag Internal."
long_description: "This document provides internal system administration information about Resolve Display Program Message Issue / GHOST Output Queue – Ag Internal."
---

_Fix GHOST Output Queue_

Issue 

 A user receives a Display Program Messages error similar to those that are shown in the following screenshots and is unable to complete a process as a result. 

 

 

 If a message stating Output queue Ghost in library QGPL not found displays at the bottom of the log for the specific session as shown below, that is the issue. 

 

  

 Solution 

 Select AS/400 Command Line (System | AS400 Command Line) or press the Alt and A keys on your keyboard at the same time. 

 

 Type WRKUSRPRF *ALL and click OK . 

 Select the file and click Change . 

 Press F10 to view additional options. 

 Page down until you see the Output Queue line with the value GHOST and a Library line below it with the value QGPL as shown below. 

 

 

 Change the Output Queue line to *WRKSTN . 

 Delete the QGPL value from the Library line. 

 Press Enter until the user list displays.  The issue is resolved.