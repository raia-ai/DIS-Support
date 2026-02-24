---
title: "Quantity of Requested Unit Number isn’t Available Error Message - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Quantity of Requested Unit Number isn’t Available Error Message - AG Internal."
long_description: "This document provides internal system administration information about Quantity of Requested Unit Number isn’t Available Error Message - AG Internal."
---

_Quantity of Requested Unit Number isn’t Available Error Message - AG Internal_

Issue 

 Receiving an error message stating the quantity requested for this unit isn’t available when trying to add a unit to a rental contract. 

   

  

 Solution 

 The error is a result of the unit not having a serial number assigned to it. Do one of the following to resolve the issue: 

 Select Inquire/Update Units (Units | Inquire/Update Units) . Select the unit and click the Update Unit button . Ensure the Unit Information tab is selected on the screen that opens and assign a serial number to the unit in the Serial # field (see below). 

   

 Select Inquire/Update Units (Units | Inquire/Update Units). Select the unit and click the Update Unit button. Select the Rental tab and enter a positive quantity (1 or above) in the Non-Serialized field (see below).