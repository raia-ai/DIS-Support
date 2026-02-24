---
title: "GL DataMining Commands - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about GL DataMining Commands - Ag Internal."
long_description: "This document provides internal system administration information about GL DataMining Commands - Ag Internal."
---

_GL DataMining Commands - AG Internal_

Issue: 
 User is running GL based Datamines and information is missing or incorrect. 
  
  
 **Before running any GL Datamining commands make sure there are no Accounting batches being posted.  
  
 DISCFGDM - Configuration - Type: DISCFGDM OPT(*UPDATE)  then enter.
 Assign the Retained Earnings Account to each division you want to see in Datamining for GL information. 
 Bypass any divisions that the customer does not want to see in Datamining.
 Note: Adding a new division or one that hasn't been part of Datamining through DISCFGDM does not result in the loss of information from other divisions. It will simply add existing current data for new the division, including historical records based on GL months to keep. 
 PFDMCNV - Recalculates everything.
 Detail is created from the CUA and CUH transactions. 
 Summary information comes from the 12 current months plus 25 history months from GLM and GLH. 
 You may lose information from both Detail and Summary if you Recalculate.  (If you are unsure if this may be an issue for the customer, make copies of DMGLDET and DMGLSUM) 
 
 DMGLFIX – Recalculates the DMGLDET & DMGLSUM for 25 closed + current. Leaves older Summary totals as is.