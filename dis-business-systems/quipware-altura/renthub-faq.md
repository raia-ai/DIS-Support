---
title: "RentHub FAQ"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about RentHub FAQ."
long_description: "This document provides information about RentHub FAQ from the DIS Salesforce Knowledge Base."
---

Each invoice created from RentHub has note lines with the reservation # and Invoice date to cross reference to the RentHub. 

 Examples: 

 

 

 Credit Card transactions are processed on the RentHub side via Gravity. 

 Entries are NOT shown in Transactions (P.O.S. | Post P.O.S. Documents | Transmit EDC Credit Card Transactions). 

 Note : This might only be temporary due to a bug See: QSUP-3105 

 Credit Card transactions are not shown in Altura 

 Rent Hub Invoices are automatically created and closed in the Quantum system. 

 In the Document Ledger the programs are: 

 X000W006 - add the invoice 

 X000W018 - add lines & closing the ticket 

 CCSURCHG - used if a Gravity Credit Card Surcharge was charged 

 Quantum configuration is in Rent Hub Configuration (P.O.S | Table Maintenance | Rent Hub Configuration) and is divisional. 

 Document Class 
 Sales mode mapping 
 Misc. Unit# 
 Exempt tax code 

 RentHub invoices are added to the archiving database when they are pulled into the accounting batch as of DIS_N125.