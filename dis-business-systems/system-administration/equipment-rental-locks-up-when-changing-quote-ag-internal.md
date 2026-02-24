---
title: "Equipment Rental Locks Up when Changing Quote - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Equipment Rental Locks Up when Changing Quote - Ag Internal."
long_description: "This document provides internal system administration information about Equipment Rental Locks Up when Changing Quote - Ag Internal."
---

_Equipment Rental Locks Up when Changing Quote - AG Internal_

Issue 

 Equipment Rental quotes lock up 

 EQ rentals, rent by units, click on contracts, and then enter the Q type, highlight a line and click on change and it locks up 

 Typically this is caused by a blank class in the detail of the contract. 

  

 Solution 

 Find record in LQHP and then pull them up in UPDDTA and change the Active flag from Y to N