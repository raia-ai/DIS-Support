---
title: "Move Saved Documents to Another Output Queue while Deleting and Recreating a Printer - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Move Saved Documents to Another Output Queue while Deleting and Recreating a Printer - Ag Internal."
long_description: "This document provides internal system administration information about Move Saved Documents to Another Output Queue while Deleting and Recreating a Printer - Ag Internal."
---

_Move Saved Documents to Another Output Queue while Deleting and Recreating a Printer - AG Internal_

Issue 

 A customer needs a new printer setup because their previous printer has died. Their previous printer was a *LAN, but the replacement printer only works as an LPR. The customer has multiple reports saved on the previous printer’s outq as shown below and can’t lose them. 

 

  

 Solution 

 Create a temporary outq to put these in for safe keeping as shown below. 

 

 Once the outq is created, enter a 2 next to every job that needs to be kept, then issue the command shown below. 

 

 Hit Enter and all of the documents are moved to the newly created outq. 

 Now you can delete the printer and re-create it as an LPR. When the LPR device has been created, reverse the steps from above, moving all of the SAV files back to where they belong. 

 Delete the temporary outq by placing a 4 next to it and clicking Enter .