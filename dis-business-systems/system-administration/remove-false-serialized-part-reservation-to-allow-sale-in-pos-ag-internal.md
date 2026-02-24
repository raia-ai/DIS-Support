---
title: "Remove False Serialized Part Reservation to Allow Sale in P.O.S. - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Remove False Serialized Part Reservation to Allow Sale in P.O.S. - Ag Internal."
long_description: "This document provides internal system administration information about Remove False Serialized Part Reservation to Allow Sale in P.O.S. - Ag Internal."
---

Issue 

 A part cannot be added to an invoice in POS because it is currently reserved in the system, but the part isn’t actually reserved. In the example below, part number 102-1290 with Serial Number I15YD0430 appears to be reserved for ticket XW05431, though it is not, and cannot be added to the current invoice. 

 

  

 Solution 

 The incorrect part reservation needs to be cleared. 

 Select AS/400 Command Line (System | AS/400 Command Line). 

 

 Type DSPPFM SAMSER in the command line and click OK . The Display Physical File Member screen opens. 

 

 Type the part serial number in the Find field and press Shift + F4 on your keyboard to locate the file. The record number associated with the serial number is listed at the bottom of the screen (record 3053 in the example above). 

 Log the Record number. 

 Select AS/400 Command Line (System | AS/400 Command Line). 

 

 Type UPDDTA SAMSER in the command line and click OK . 

 

 Type the record number that was logged in the previous step (3053) in the *RECNBR field and click Enter . Additional fields display. 

 

 While holding down the Shift key, press F11 TWICE to delete the record.  The reservation for that part is removed and the part can now be added to the ticket.