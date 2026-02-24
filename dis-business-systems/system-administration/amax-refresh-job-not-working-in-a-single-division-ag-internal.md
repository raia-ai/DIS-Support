---
title: "AMAX Refresh Job not Working in a Single Division - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about AMAX Refresh Job not Working in a Single Division - Ag Internal."
long_description: "This document provides internal system administration information about AMAX Refresh Job not Working in a Single Division - Ag Internal."
---

_AMAX Refresh Job not Working in a Single Division - AG Internal_

Issue 

 Communications acts as though dealership does not have parts in inventory and breath rating is 0. As a result, the division is having an issue with the AMAX nightly files submission. 

  

 Solution 

 Check the CASLOADd in the OPT file and make sure it is set to CASLOADH 2 and not CASLOADH 0 . If it is set to CASLOADH 0 , access the Send Part Refresh option and select Send Daily Files for this division during backup this evening. 

 

 This action should change the option from CASLOADH 0 to CASLOADH 2 .