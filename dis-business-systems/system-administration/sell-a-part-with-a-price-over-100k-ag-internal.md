---
title: "Sell a Part with a Price Over $100k - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Sell a Part with a Price Over $100k - AG Internal."
long_description: "This document provides internal system administration information about Sell a Part with a Price Over $100k - AG Internal."
---

_Sell a Part with a Price Over $100k - AG Internal_

Issue 

 Cannot sell a part that has a price over $100,000.00 (one hundred thousand dollars) since the parts price field only goes to $99999.99. 

  

 Solution 

 There are two recommended options: 

 The most popular method is to setup the part as a unit number since unit pricing allows price amounts over $100k to be entered. 
 The other option is to split the part into 2 separate part numbers and assign half of the whole price for the part to each created part number. Each part number could then be added to the invoice. 

 Alternatively, the part could be sold using a miscellaneous sales code and not a parts sales code. This will allow a price over $100k to be manually entered, HOWEVER, auto costing wouldn’t be applied and manual adjustments would need to be made to move the money from parts inventory to the parts cost of sale accounts.