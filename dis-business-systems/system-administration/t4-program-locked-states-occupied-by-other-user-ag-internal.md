---
title: "T4 Program Locked / States Occupied by Other User - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about T4 Program Locked / States Occupied by Other User - AG Internal."
long_description: "This document provides internal system administration information about T4 Program Locked / States Occupied by Other User - AG Internal."
---

_T4 Program Locked / States Occupied by Other User - AG Internal_

Issue 

 T4 Program Locked / States Occupied by Other User. 

  

 Solution 

 Access AS/400 and locate file u .AA1c91 in the QS36F library ( u represents the dealership division code) using command - DSPPFM     U .@@1C91. 

 After the file has been located, do one of the following: 

 Delete it using the command WRKF U .@@1C91 and entering the number 4 in Green screen or clicking Delete in Quantum/Keystone. 
 Enter the command DLTF U .@@1C91.