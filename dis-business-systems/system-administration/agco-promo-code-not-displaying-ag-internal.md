---
title: "AGCO+ Promo Code Not Displaying - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about AGCO+ Promo Code Not Displaying - Ag Internal."
long_description: "This document provides internal system administration information about AGCO+ Promo Code Not Displaying - Ag Internal."
---

_AGCO+ Promo Code Not Displaying - AG Internal_

Introduction 

 If a customer calls in because they are not seeing an expected Promo for AGCO+, it might be because they have something other than AGC assigned as their AGCO vendor code. When a customer does a promo look-up, AGCO requires a certain percentage of the parts on the ticket be Agco parts assigned the AGC vendor code. To resolve this issue, customers will need to map the “Non-AGC” vendor code in Credit Card maintenance to the AGC vendor code. 

  

 To Map Non-AGC Vendor Code 

 Select Credit Card (POS | Table Maintenance | Credit Card) . The Card List Screen displays. 

 

 Select the card code and click the Promo Codes/Configure button. The Configuration screen displays. 

 

 Click the Assign Parts Source button. The Assign Part Source screen displays. 

 

 Locate the vendor in the table, change the Part Source vendor code to AGC, and click Enter to save.