---
title: "Error Retrieving Gravity Transaction Message - Quantum"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Error Retrieving Gravity Transaction Message - Quantum."
long_description: "This document provides information about Error Retrieving Gravity Transaction Message - Quantum from the DIS Salesforce Knowledge Base."
---

_Error Retrieving Gravity Transaction Message - Quantum_

Introduction 

 When closing a Gravity Flex/eMerge Pay transaction, a network error message of Error Retrieving Gravity Transaction may appear immediately after attempting to connect to Altura as shown below. 

 

 This typically occurs when there is a non-alphanumeric character in either the customer address field or the ship-to field and not a Gravity credit card or communications issue. 

 

 R esolve Issue and Close Invoice 

 Remove any non-alphanumeric characters from any ship-to locations manually entered in the system. 

 Remove any non-alphanumeric characters from the address fields in either: 

 Receivable Maintenance (Accounting | Receivables | Receivables Maintenance) 
 Address Maintenance (Marketing | Address Maintenance) 

 Once the non-alphanumeric characters have been removed, you can successfully close and authorize the invoice.