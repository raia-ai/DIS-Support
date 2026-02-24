---
title: "Determine why Demand is Not Recorded for Sold Part – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Determine why Demand is Not Recorded for Sold Part – Ag Internal."
long_description: "This document provides internal system administration information about Determine why Demand is Not Recorded for Sold Part – Ag Internal."
---

_This article helps troubleshoot why Demand is not displaying for parts that were sold through POS Invoicing_

Issue 

 A part does not show any demand or calls over a given time period when the customer knows the part was sold during that time frame. One reason may be that the No Demand check box on the Invoicing Detail screen was selected when generating the invoice 

 

 When an invoice is closed, the No Demand checkbox will appear unselected even if it was selected when creating the invoice. 

  

 Solution 

 Check the SAM file to see if the No Demand check box was selected when the invoice was generated. 

 Select AS/400 Command Line (System | AS/400 Command Line) or press the Alt and A keys on your keyboard at the same time. 

 

 Type DSPPFM u .SAM where u = the File Set letter. 

 

 In the Find line, type the invoice number and click the Shift + F4 keys to scroll through the lines.  Keep pressing Shift + F4 until you find the specific part detail line.  

 With the specific line highlighted, press F10 on your keyboard. The information displays similar to the following. 

 

 Press F11 on your keyboard. The information displays similar to the following: 

 

 If an N displays in position 105 for the specified detail line, the No Demand checkbox WAS selected when the invoice was generated.