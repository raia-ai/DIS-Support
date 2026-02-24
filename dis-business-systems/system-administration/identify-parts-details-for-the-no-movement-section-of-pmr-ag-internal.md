---
title: "Identify Parts Details for the No Movement Section of PMR – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Identify Parts Details for the No Movement Section of PMR – Ag Internal."
long_description: "This document provides internal system administration information about Identify Parts Details for the No Movement Section of PMR – Ag Internal."
---

Issue 

 Customer wants to see the part numbers that make up the various categories in the No Movement section of the PMR. The No Movement section is for parts that have no movement in the last 24 months – not necessarily parts that have never had any movement.

  

 Resolution 

 Run a Data Mine – see SC/400 A03327 or ticket 713020.
 The parts can also be identified using a suggested phase-out as the option can be run for months in Inventory, months with sales less than or equal to the previous # months.