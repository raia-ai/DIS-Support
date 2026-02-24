---
title: "POS Daily transfer requests getting added to closed document - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about POS Daily transfer requests getting added to closed document - Ag Internal."
long_description: "This document provides internal system administration information about POS Daily transfer requests getting added to closed document - Ag Internal."
---

_POS Daily transfer requests getting added to closed document - Ag Internal_

POS Daily transfer requests are added to an existing open transfer document or the program will create a new document if there isn't one already open. 

 Occasionally a record lock or some other glitch will result in transfer requests going to closed documents. 

 To fix this simply delete the division’s transfer document record out of the PDTD file. There will only be one record per division in PDTD. The program will create a new PDTD record the next time a transfer request is made. 

  

 Note : Any new lines that were added to the closed transfer will need to be re-requested.