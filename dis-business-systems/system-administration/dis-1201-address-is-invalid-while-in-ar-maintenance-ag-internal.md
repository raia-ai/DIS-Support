---
title: "DIS-1201 Address is Invalid while in AR Maintenance - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DIS-1201 Address is Invalid while in AR Maintenance - AG Internal."
long_description: "This document provides internal system administration information about DIS-1201 Address is Invalid while in AR Maintenance - AG Internal."
---

_DIS-1201 Address is Invalid while in AR Maintenance - AG Internal_

Issue 

  Getting an error of DIS-1201 Address is invalid when in the second screen of a customer address in AR Maintenance. 

  

 Solution 

 The error is coming from a salesman ID that is deactivated or no longer valid that is tied to this address. You can either update the REM file to remove, or find it in ADM and reactivate it to clear the error. There is also a hidden OPT (see call in SC400 1025189) RECSALMN where the salesman field can be hidden or displayed so if you don’t see this on the actual AR screen the OPT is off.