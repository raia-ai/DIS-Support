---
title: "Preventing Warranty Split document from being reopened - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Preventing Warranty Split document from being reopened - Ag Internal."
long_description: "This document provides internal system administration information about Preventing Warranty Split document from being reopened - Ag Internal."
---

_Preventing Warranty Split document from being reopened - AG Internal_

When there is a customer ticket with I/W lines and the ticket is closed, it creates split documents for the I and W designated lines.  

 If you want to recombine this documents, you must reopen the original customer ticket.  

 If you reopen the split ticket, you will sever the ties with the original ticket and they cannot be recombines.  

  

 How to prevent a Warranty Split document from being reopened.  

 If Fleet Management is turned on, you will get a message if you try to reopen the warranty ticket that says.  

 The customer document must be reopened instead of this split document. 

  

 There is also a phone opt that you can turn on to prevent this as well.  CUST0316  This opt was officially rolled in to version 22V1 per SC400 1129796 
 If you want to turn this one, at a command line, type: X00081 CUST0316,1   and press enter.