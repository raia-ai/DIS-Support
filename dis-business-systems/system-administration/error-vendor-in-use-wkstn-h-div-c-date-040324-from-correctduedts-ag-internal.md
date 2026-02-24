---
title: "Error: Vendor in use! (Wkstn: _H Div: C Date: 040324 from: CorrectDueDts) - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Error: Vendor in use! (Wkstn: _H Div: C Date: 040324 from: CorrectDueDts) - Ag Internal."
long_description: "This document provides internal system administration information about Error: Vendor in use! (Wkstn: _H Div: C Date: 040324 from: CorrectDueDts) - Ag Internal."
---

_Error: Vendor in use! (Wkstn: _H Div: C Date: 040324 from: CorrectDueDts) - AG Internal_

Issue 

 Trying to get in to Manual Checks for a specific vendor and getting a message at the bottom of the screen that says

 Error: Vendor in use! (Wkstn: _H Div: C Date: 040324 from: CorrectDueDts)

 In this case:

 Workstation ID = _H

 Division = C

 Date Lock was put in place = 04/03/2024

 Menu option = Correct Due Dates and Discounts. 

  

 Things to consider before removing the line from the LOCKVEN file: 

  

 Check TAKE screen

 In this case, you can see that the session _H is active because it's in red and in AP Correct Due Dates 

 

  

 Another option would be to look for temporary files related to the session noted in the Error message.  

 At a command line, type:  WRKF Z.@*    (where  Z is the fileset)

 Look for files that start with Z.@_H...

 In this situation, the key file to note for session _H in Correct Due Dates and Discounts is 

  

 The file that is holding the Lock information in called LOCKVEN and is in the FILEu library (where u = Fileset).

 This is what this particular lock looks like in the file. 

 

  

 Solution:

 In this case, we should get the person using vendor ALXC on session _H to complete their process in Correct Due Dates and discounts before proceeding with Manual Checks. 

  

 Why was the vendor lock created in the first place? 

 The Vendor lock was created to prevent multiple users from posting to the same vendor at the same time and potentially

 merging the same transactions more that once.

  

 Can the vendor lock be "eased" not not consider Payables Invoice Entry?  Yes

      SC400: 0676951 Notes:

      Payable Invoice Entry (Legacy version - X12.5):  This update 
     introduces a "hidden" opt which removes the restrictions to  
     post invoices to the same vendor from simultaneous batches.  
     However, the restriction that "locks" a vendor will remain   
     for Manual Checks and Correct Due Dates and Discounts.       

 The caution would still be the possibility of merging the same transactions in 2 different sessions.  It should be a thoughtful discussion with the customer before turning the below opt on. 
.                                                                 
Opt: CUST0225  (Note: applies to the X12.5 LEGACY version only)   
     0 = A/P Invoice Entry restricts Vendor use (LOCKVEN)         
     1 = A/P Invoice Entry does NOT restrict Vendor use (LOCKVEN) 

  

 ****This article is a work in process.  Please make suggestions for additions and changes to the article.  I wanted to get some thoughts down for this right away but I know there are more things to add/consider. - RK 04/03/2024

  

 Considerations to add:

 An example where the lock came from Manual Checks. 

 An example where the lock came from Payables Invoice Entry.