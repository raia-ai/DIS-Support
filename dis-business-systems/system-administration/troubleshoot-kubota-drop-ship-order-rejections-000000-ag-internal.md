---
title: "Troubleshoot Kubota Drop Ship Order rejections - 000000 - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Troubleshoot Kubota Drop Ship Order rejections - 000000 - AG Internal."
long_description: "This document provides internal system administration information about Troubleshoot Kubota Drop Ship Order rejections - 000000 - AG Internal."
---

_How to troubleshoot Kubota Drop Ship Order rejections - 000000 - AG Internal_

Troubleshoot Kubota Drop Ship Order rejections - 000000 - AG Internal 

  

  

 From the PC running the ECCService.

 Browse out to the C:\ProgramData\dis\im\temp\kub folder 

 You will need to look at the MFGxxxx.txt file associated with the order validation request.

 What I do is sort the files by Date modified then look for the one that corresponds to the time when the order validation request was sent and returned with 0000000 supplemental order number.

  

 

  

 Display the file and scroll to the bottom

  

 

  

 Another thing to look at is what they have for the ship to address on the POS invoice to make sure they have valid address information there. In this example the dealer should have changed the address to 1056 S WASHINGTON or 1056 S WASHINGTON ST and then it would have validated.

  

 

  

 You can also use the USPS address verificaion tool to check an address

 https://tools.usps.com/zip-code-lookup.htm 

  

  

 

  

  

 ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 

 -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 

 ---