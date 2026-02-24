---
title: "Close a Z Clone Document (DIS-5523 Error) – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Close a Z Clone Document (DIS-5523 Error) – AG Internal."
long_description: "This document provides internal system administration information about Close a Z Clone Document (DIS-5523 Error) – AG Internal."
---

_Close a Z Clone Document (DIS-5523 Error) – AG Internal_

Issue 

 The error message DIS-5523 You can't close a Z cloned document; copy to a new document displays w hen closing a Z clone document generated from an Equipment Rentals Contract:  

     

 This errors occurs when an invoice has used all of the letters of the alphabet. The document needs to be manually closed in the background. Use the Solution below to resolve the issue. 

 Important!   Do this using Greenscreen. 

  

 Solution                                                                         

 Manually close the Z clone document by editing the SAM header record and changing the status  IF  there aren’t parts on it that need updating when closed. The document will remain attached to the EQR contract. Once closed, nothing more needs to be done because EQR will start over with a new invoice number sequence. 

 Be sure to create a duplicate of the file in case of an error when completing this process, then delete the file after successfully completing this process. 

  

 Access the main menu in Greenscreen. 

 

 On the main menu, type DSPPFM U . SAM (‘ U ’ stands for the file set) and press Enter . 

 

 Type the invoice number in the Find field and press F16 ( Shift + F4 ) to display the header line (highlighted in white). 

 Write down the record number listed in the white text at the bottom of the screen (2552521 in the example above).  

 Press F3 to return to the main menu. 

 

 Type DISFU and press Enter . 

 

 Type U . SAM where U is the file set.  Press Enter . 

 

 Under the next missing parameter, type QS36F and press Enter . 

 

 Leave the final parameter blank and press Enter . 

 

 Type that record number you previously wrote down in the Record line and press Enter . 

 

 The O value shown above means the invoice is Open and needs to be changed to a C to close it.  

 Notice that the two yellow digits below the O are D and 6 and that D6 creates the O value according to the glossary at the bottom of the screen. 

 To change the O value to a C, use the tab and arrow keys on your keyboard to move your cursor to those yellow digits below the O.  Move the cursor over the D and change it to a C, then move the cursor to the 6 and change it to a 3 as shown below. 

  

   

 Press Enter . T he value changes to C and the document is closed.                                                                                       

 

 Important! Be sure NOT to press f4 in the next step as it will delete the file. 

 Press F3 to exit this screen.