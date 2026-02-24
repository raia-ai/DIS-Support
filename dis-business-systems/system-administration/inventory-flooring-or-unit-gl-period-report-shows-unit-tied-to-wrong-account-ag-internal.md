---
title: "Inventory/Flooring or Unit GL Period Report shows unit tied to wrong account - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Inventory/Flooring or Unit GL Period Report shows unit tied to wrong account - Ag Internal."
long_description: "This document provides internal system administration information about Inventory/Flooring or Unit GL Period Report shows unit tied to wrong account - Ag Internal."
---

_Inventory/Flooring or Unit GL Period Report shows unit tied to wrong account - Ag Internal_

Issue 

 Customer calls in saying they have units that they have changed the GL account for and moved them to an internal expense account but the unit still shows on the Inventory/Flooring or Units GL Period Report tied to the original GL account. This can happen when you move a unit out of an inventory account with a W edit code to an account without an edit code and the system keeps the record in the WCT file. 

  

 Solution 

 You may need to delete the record for the unit number in the WCT file. 

 ***UPDDTA WCT then type in the unit number and look for a record for that unit and delete it (F23) 

 Or you could also consider adding a new record to the WCT file for the new account.