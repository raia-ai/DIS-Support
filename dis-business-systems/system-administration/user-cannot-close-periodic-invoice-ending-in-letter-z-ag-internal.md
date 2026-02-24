---
title: "User Cannot Close Periodic Invoice Ending in Letter Z - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about User Cannot Close Periodic Invoice Ending in Letter Z - AG Internal."
long_description: "This document provides internal system administration information about User Cannot Close Periodic Invoice Ending in Letter Z - AG Internal."
---

_User Cannot Close Periodic Invoice Ending in Letter Z - AG Internal_

Issue           

 The User has a periodic invoice automatically generated with a sequence ending in the letters A through Z, but the Z invoice cannot be closed through Point of Sale the regular way.    

 Invoice RI42471Z is used in this example. 

     

 Solution 

 Follow the solution based on the Invoice payment type  

 Credit Card Invoice – Copy the exact lines to a new ticket with the identical periodic information filled on the sold by screen. Void the Z ticket when finished.    
 Cash or Charge Ticket – Manually close the ticket using DISFU on the u.SAM file as shown below. There CANNOT be Parts on the ticket.  

 Search u.SAM for the record number of the ticket.   

   

 Type WRKF u.SAM and press Enter . 

   

 Type 5 and press Enter . 

   

 Press Enter . 

   

 Type the invoice number in the FIND field and press F16. 

   

 Write down the record number that appears at the bottom of the screen – 4396678 in the example above.   

   

 Type DISFU and press Enter . 

   

 Type u.SAM for the file name and press Enter . B is the file set in the example above. 

   

 Type QS36F for the library and press Enter . 

   

 Leave the Name of member field blank. Press Enter . 

   

 Type the record number you previously wrote down and verify it is the correct ticket number, then change position 27 of the record number to C as shown below. Press Enter . 

   

 Have the User Print and Close the invoice so it will be archived.