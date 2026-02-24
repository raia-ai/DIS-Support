---
title: "POS Document Ledger Programs - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about POS Document Ledger Programs - AG Internal."
long_description: "This document provides internal system administration information about POS Document Ledger Programs - AG Internal."
---

Introduction 

 This article explains the programs in Document Ledger and their definition 

 CCSURCHG : Gravity Credit Card Surcharge got charged 
 PSNTSE2R : Note detail line added or changed through the Work with Notes screen in POS | Invoicing 
 PSNTSE5R : The program that adds the FLATMIN and FLATMAX lines when setting up flat rating using the SRT code in the Work with Notes screen 
 X000W006 : Rent Hub program for adding the invoice 
 X000W018 : Rent Hub program for adding lines and closing the ticket 
 X34222 : Part received in Parts | Stock Order | Receive Order | Receive Order OR Correct Order Before Receiving and going from a ‘p’ priority code to an ‘a’ 
 X34273R : Part priority code going from ‘u’ to ‘a’ after being received in Parts | Stock Order | Receive Order | Receive Divisional Transfer 
 X5B101 : Time Clock labor punch added through TCLOCK login or POS | Time Clock | Time Clock Entry 
 X5B401 : Time Clock labor punch added through POS | Time Clock | Review by Technician 
 X5B501 : Time Clock labor punch change made through POS | Time Clock | Review by Work Order 
 X5BSVLG : Labor Detail punched into a WO from the Service Logistics app 
 X510ACR : A part going from a T priority code back to a P priority code when the transfer is rejected from the requestee document 
 X510A4R : Priority ordered part in requesting document getting a T priority code from the Parts Transfer screen 
 X510A7R : Part priority code going from T to ‘t’ when transfer request is accepted by requestee 
 X510AGR : Transferred Part priority code changed from ‘t’ to ‘u’ after requestee document is closed 
 X510AQ0002 : Labor lines added from Service Note configuration when clicking Auto Charge 
 X51007 : Standard program for most things done in the Detail screen of POS | Invoicing, like opening the document, closing the document, adding a Sold By address in the Sold To screen, adding a part to the Detail screen, deleting a part, etc 
 X51070 : Part added to Detail screen through Part Availability screen 
 X51080 : Document deleted by background program after being voided 
 X51094R : Detail lines added when clicking Auto Charge button 
 X51095R : Detail line segment changed 
 X53009 : Part going from ‘P’ priority code to ‘p’ priority code after being accepted in POS | Priority Orders 
 X55105 : Document reclaimed using POS | Post POS Documents | Reclaim Point of Sale Documents 
 X55112 : Document Batched and getting Posted Date through POS | Post POS Documents | Create Point of Sale Posting Batch