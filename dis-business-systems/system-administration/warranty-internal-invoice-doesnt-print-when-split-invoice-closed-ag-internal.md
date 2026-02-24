---
title: "Warranty / Internal Invoice Doesn’t Print when Split Invoice Closed - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Warranty / Internal Invoice Doesn’t Print when Split Invoice Closed - Ag Internal."
long_description: "This document provides internal system administration information about Warranty / Internal Invoice Doesn’t Print when Split Invoice Closed - Ag Internal."
---

Issue 

 Warranty or Internal ticket isn’t created / doesn’t print when a split invoice is closed. This can happen for a variety of reasons. 

  

 Solution 

 Make a copy of the u.SAM file. 

 Run a DISFU on the u.SAM for the second line of the header record for the invoice. 

 Change the digit in position 81 from 1 to 0. 

 Reclaim the invoice. 

 Return to header record and change position 81 from 0 to 1. (to original entry). 

 Re-open the invoice in Invoicing (P.O.S. | Invoicing). 

 Close the invoice to create the split correctly. 

 Have the user create a batch and post the invoice. 

 Important! If there is a charge to the customer and it was previously posted, it must be deleted from the batch to prevent a double post. It is fine if the customer copy is $0.