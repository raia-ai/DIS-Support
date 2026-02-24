---
title: "Manage California's Agriculture and Manufacturing Partial Exemptions with Tax Types - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Manage California's Agriculture and Manufacturing Partial Exemptions with Tax Types - Ag Internal."
long_description: "This document provides internal system administration information about Manage California's Agriculture and Manufacturing Partial Exemptions with Tax Types - Ag Internal."
---

_Manage California's Agriculture and Manufacturing Partial Exemptions with Tax Types - Ag Internal_

Introduction 

 California offers two specific partial tax exemptions that can be efficiently managed through DBST setup: 

 The Agriculture Exemption (Ag) 
 The Manufacturing Exemption (Mfg). 

 These exemptions apply a standard percentage reduction across the state, subtracted from the State Rate on the tax code. This setup eliminates the need to manually create and maintain new tax codes as dealers can handle standard, partial Ag, and partial Mfg exemptions with a single tax code. 

 

   

  

 Apply Partial Exemptions with Tax Types 

 Select Destination Tax Profile (POS | Table Maintenance | Tax Configuration | Destination Tax Profile). 

 

 In the California Specific section, enter the partial exemptions amount that will be subtracted from the State rate for Ag and Mfg (e.g., 5.25% is entered as 052500). Enter the current date as the effective date. 

 Create two new Tax Types: 

 A for the Ag exemption 
 M for the MFG exemption. 

 Select Tax Type Maintenance (POS | Table Maintenance | Tax Configuration | Tax Type Maintenance). 

 Click Add . 

 Provide the Tax Type Code and Description, then click Enter to create the Tax Type as shown below 

 

 Assign each tax type to at least one address associated with a California tax code to link the tax type with the state. 

 

 This can be done in Receivables Maintenance (Accounting | Receivables | Receivables Maintenance) or Address Maintenance (Marketing | Address Maintenance) as shown above . 

 Note : Tax types are set at the address level, not the Ship To level. The exemption will be applied to all Ship To addresses with CA tax codes. 

 With the next DBST update, a new tax code-tax type combination is added for each of the tax types to all California tax codes. 

 

 In the example below an address is assigned a default tax code of C¢ with a standard tax rate of 10.25% (.102500). When the M Tax Type is applied, the rate decreases by 3.9375% (039375) for a final tax rate of 6.312%. 

 

 The tax rate is followed by the Tax Type indicating it is a non-standard rate.