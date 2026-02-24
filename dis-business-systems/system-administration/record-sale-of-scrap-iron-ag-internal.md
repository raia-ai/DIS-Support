---
title: "Record Sale of Scrap Iron – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Record Sale of Scrap Iron – AG Internal."
long_description: "This document provides internal system administration information about Record Sale of Scrap Iron – AG Internal."
---

_Record Sale of Scrap Iron – AG Internal_

Introduction 

 How a dealership records the sales of scrap iron depends on whether or not taxes need to be included in the sale. 

 If taxes NEED to be included, the sale should be made through P.O.S. as an invoice. 
 If taxes DO NOT NEED to be included, the sale can be recorded with a Receipt Type created through Configure Payments. 

  

 Create Receipt Type 

 Select Configure Payments (Accounting | Receivables | Configure Payments) then click Receipt Type . 

 Create a new receipt type. 

 

 Configure the Receipt Type so it: 

 Debits the bank (or cash if that check is going to be included in the dealership’s daily deposit with other checks and cash). 
 Credits where the dealer wants (for example an income account). 

 Once the Receipt type is created, use Enter Payments to record the check or cash payment for the scrap iron. 

 Important! Be sure to set the Receipt Type used in Enter Payments is the one created in this process. 

 For additional information on receiving a check for scrap iron through Enter Payments, see the Quantum Post Payments Video Tutorial .