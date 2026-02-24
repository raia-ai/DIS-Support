---
title: "Attempt to Write a Duplicate Record to File TOE / Duplicate Keys – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Attempt to Write a Duplicate Record to File TOE / Duplicate Keys – AG Internal."
long_description: "This document provides internal system administration information about Attempt to Write a Duplicate Record to File TOE / Duplicate Keys – AG Internal."
---

Issue 

 User encounters one of the following two errors: 

 When finalizing a parts phase-out (Parts | Stock Return/Phase-out | Print/Finalize Phase-out) , a user receives the following message and is unable to finalize the phase-out: 

 
 Attempt to write a duplicate record to file TOE 

 When working with a stock phase-out (Parts | Stock Return/Phase-out | Correct Stock Phase-out) , the user is unable to access or complete the phase-out and receives the following S/36 message: 

 
 Duplicate keys were found while adding record to file TOA 

  

 Cause 

 This is likely a result of a part number being in the detail of the phase out more than once.  The detail can be seen in Order Inquiry ( Parts | Stock Order | Order Inquiry) .  

 In the screenshot below, there are two instances of part number A-DOG in this phase-out with one of the parts has a blank space in the beginning.  Despite this difference, the system considers these parts duplicate records. 

 

  

 Solution 

 Remove one of those parts from the detail of the phase-out.  

 Select AS/400 Command Line ( System | AS/400 Command Line). 

 

 Type UPDDTA OAA and click OK . 

 

 Provide the order number, the vendor code, and the part you want to work with and click Enter . 

 

 Press F23 (Shift + F11) twice to delete this record. The part is deleted from the detail of the phase out.  

 Re-open the phase-out. The duplicate should be removed from the detail. 

 

 The phase-out should be able to be finalized.  The part that was removed from the phase out can be included in another phase out to be deleted or it can be deleted from Parts Posting & Maintenance.