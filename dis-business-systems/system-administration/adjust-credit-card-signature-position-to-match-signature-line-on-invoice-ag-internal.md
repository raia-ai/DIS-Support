---
title: "Adjust Credit Card Signature Position to Match Signature Line on Invoice – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Adjust Credit Card Signature Position to Match Signature Line on Invoice – Ag Internal."
long_description: "This document provides internal system administration information about Adjust Credit Card Signature Position to Match Signature Line on Invoice – Ag Internal."
---

_Adjust Credit Card Signature Position to Match Signature Line on Invoice – Ag Internal_

Issue 

 The Credit Card signature is printing too high or too low in relation to the signature line on an invoice. 

  

 Solution 

 Adjust the Value assigned to the Signature Position so it matches the signature line on the invoice. 

 To find the current signature Value setting, enter the following in a Command Line: 

 DSPDTAARA DTAARA(DISFILES/SIGOFFV1) 

 The Current signature position is indicated by the Value. It is currently at the default Value / position ( .00 ) in the screenshot below. 

 

  

 To adjust the signature position DOWN ¼ inch, enter the following in a Command Line: 

 CHGDTAARA DTAARA(DISFILES/SIGOFFV1) VALUE(.25) 

   

 To adjust the signature position UP ¼ inch, enter the following in a Command Line (note the Value is entered as a negative): 

 CHGDTAARA DTAARA(DISFILES/SIGOFFV1) VALUE(-.25) 

  

  

 To reset the signature position to the default value / position, enter the following in a Command Line: 

 CHGDTAARA DTAARA(DISFILES/SIGOFFV1) VALUE(.00)