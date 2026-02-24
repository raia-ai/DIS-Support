---
title: "Refresh Warehouses (Facing Depots) for CSPS - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Refresh Warehouses (Facing Depots) for CSPS - AG Internal."
long_description: "This document provides internal system administration information about Refresh Warehouses (Facing Depots) for CSPS - AG Internal."
---

_Resolution for when closest warehouses are not displaying in CSPS_

Issue 

 The wrong Facing Depot displays in the Comments for Case parts on the Part Availability – Inquiry screen in Invoicing (P.O.S. | Invoicing) . 

 This also happens when looking at the Depot Availability column in the CSPS Communication – Availability screen accessed when pre-editing parts orders in Priority Orders (P.O.S. | Priority Orders).  The closest depot should be shown first, but may not display. 

  

 Resolution 

 Instruct the user to do the following: 

 Close any Availability screen(s) they are currently working on. 
 Select Refresh Configuration Data (Manufacturers | CSPS Communications | Refresh Configuration Data).  The CSPS Configuration Data screen displays. 

 

 Click Warehouses , then click Display . The CSPS Configuration Data – Warehouses screen displays.  

   

 Click the CNH Update button.  After a few moments, access the Availability screen and check for warehouses again. The closest warehouses should display.