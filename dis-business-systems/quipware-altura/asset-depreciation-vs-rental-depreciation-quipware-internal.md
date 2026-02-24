---
title: "Asset Depreciation vs Rental Depreciation - Quipware Internal"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Asset Depreciation vs Rental Depreciation - Quipware Internal."
long_description: "This document provides information about Asset Depreciation vs Rental Depreciation - Quipware Internal from the DIS Salesforce Knowledge Base."
---

Issue 

 Equipment was initially logged as Asset Depreciation, then changed to Rental Depreciation, causing negative depreciation. 

 There cannot be both Asset and Rental Depreciation – It must be one or the other as Rental Depreciation and Asset Depreciation do not write back to each other. 

  

 Solution 

 Make a GL entry for the total of all rental depreciation for this equipment or a GL entry for all Asset Depreciation for this equipment.