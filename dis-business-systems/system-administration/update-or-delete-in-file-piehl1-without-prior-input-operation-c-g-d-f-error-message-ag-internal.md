---
title: "Update or Delete in File PIEHL1 Without Prior input Operation (C G D F) Error Message - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Update or Delete in File PIEHL1 Without Prior input Operation (C G D F) Error Message - Ag Internal."
long_description: "This document provides internal system administration information about Update or Delete in File PIEHL1 Without Prior input Operation (C G D F) Error Message - Ag Internal."
---

_Update or Delete in File PIEHL1 Without Prior input Operation (C G D F) Error Message - AG Internal_

Issue 

 The user receives the following error message when trying to post a payables batch: 

  

 Update or delete in file PIEHL1 without prior input operation (C G D F) . 

  

 Solution 

 This is a result of an invoice in the batch having an N in the OK column. 

 Have the user answer the message with a C and then go back into their batch and remove the invoice with a N. They can then post the rest of the invoices and then process the invoice that was causing the error in a stand alone batch.