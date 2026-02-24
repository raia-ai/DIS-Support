---
title: "Create a P.O. for Resale of Non-Inventory Parts - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Create a P.O. for Resale of Non-Inventory Parts - Ag Internal."
long_description: "This document provides internal system administration information about Create a P.O. for Resale of Non-Inventory Parts - Ag Internal."
---

_Create a P.O. for Resale of Non-Inventory Parts - AG Internal_

Issue 

 A dealer needs to create a PO for purchasing a part that they are reselling and do not want in inventory. 

  

 Solution 

 Create invoice to generate document number, but do not add parts. 

 Create the Purchase Order and add the invoice number. 

 

 Add the parts as a Miscellaneous Quantity PO Code format (tied to a Miscellaneous Quantity sales code for the invoice), to the Purchase order and R for resale. 

 

 

 Print and hold. Take the PO to the Vendor store to get the parts. When you receive the invoice#, go back into the PO header and place it in the Vendor# field. 

 Close the Purchase Order once the parts are received. It is automatically added to the POS invoice.