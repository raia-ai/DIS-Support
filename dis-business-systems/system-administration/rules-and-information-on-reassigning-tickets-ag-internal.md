---
title: "Rules and Information on Reassigning Tickets - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Rules and Information on Reassigning Tickets - AG Internal."
long_description: "This document provides internal system administration information about Rules and Information on Reassigning Tickets - AG Internal."
---

_Rules and Information on Reassigning Tickets - AG Internal_

Introduction 

 This article provides miscellaneous information regarding the Reassign button such as: 

 Why the Reassign button doesn’t display. 
 Requirements necessary to complete the procedure. 
 What can be accomplished through the procedure. 

   

 Reasons Reassign Button Won’t Display 

 The user has more than one POS session active. 
 The session has been toggled to history or standard job. 
 The session is processing a document list. 

  

 Documents Being Reassigned 

 Must be open or reopened. 
 Must be sales order or work order. 
 Can’t be a child of Internal or Warranty split ticket. 
 Can’t exist in the Parts Store. 
 Can’t be a Rental Contract invoice. 

  

 Additional Information 

 The New document type must not be restricted for any of the used sales codes. 
 Reassigning a document does not change the Ship-To information to the corrected customer address. 
 Sales tax is updated when customer changes. 
 The Reassign Option Allows Users to: 

  Change the address number or unit number associated with the document 
  Change the document number 
  Reprice the parts on the document 
  Reprice the labor on the document 
  Remove the discount codes from the document 

 If (c), (d), or (e), the changes appear in the document ledger as if they were changed manually by the user. 

 If (a) and/or (b), a new ledger is created for the document which will be associated with the new address number and/or document number. 

  

 The old ledger will have a final entry which indicates the reassignment and shows the new address number and/or document number in the PO# field. 
 The new ledger will show every line on the document that existed at the time of reassignment. 
 The new ledger will also show additional changes to the lines if the tax codes changed because of a change to the address number.