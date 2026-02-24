---
title: "CPF5152 I/O Error Detected in X3SIBOKL - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about CPF5152 I/O Error Detected in X3SIBOKL - Ag Internal."
long_description: "This document provides internal system administration information about CPF5152 I/O Error Detected in X3SIBOKL - Ag Internal."
---

_CPF5152 I/O Error Detected in X3SIBOKL - AG Internal_

Issue 

 Receiving the  CPF5152 I/O Error Detected in X3SIBOKL error message when trying to add parts to a quote or POS Sale ticket. This is typically related to one specific vendor and indicates that there is an issue with the download of the price book for that vendor.   

  

 Solution 

 Open a command line, enter CALL PGM(X3740H) PARM(xxxxxx) where the (xxxxxx) is the name of the price book tied to that vendor code, and click OK . 

 Note : If this doesn’t work, the price book will need to be deleted from the IFS and also from the vendor assignment in Configure Vendor/Class. Once deleted from these locations, download the price book again from the web locker, create a new price book, and assign it to the vendor code.