---
title: "Remove Sold Units from the Inventory/Flooring Report – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Remove Sold Units from the Inventory/Flooring Report – AG Internal."
long_description: "This document provides internal system administration information about Remove Sold Units from the Inventory/Flooring Report – AG Internal."
---

_Remove Sold Units from the Inventory/Flooring Report – AG Internal_

Issue 

 A unit that was sold still appears on the Inventory/Flooring Report ( Units | Units Reports | Inventory/Flooring ). 

 

 This is probably a result of the Sale 1: field being empty in Units G/L History Entry ( Security | Initial Data Entry | Units G/L History Entry) as shown below. 

 

   

 Solution 

 Enter the sale date for the unit in the Sale 1: field using a YYMM format as shown below and click Enter to remove the unit from the Inventory/Flooring report. 

 

 The unit’s sale date can be viewed by selecting the Unit in Inquire/Update (Units | Inquire/Update) and clicking the Unit Trans tab. 

 

 Once the sale date has been provided the unit should be removed from the Inventory/Flooring Report as shown below.