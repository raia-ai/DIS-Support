---
title: "Set OPT for ZIP/Postal Code Lookup - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Set OPT for ZIP/Postal Code Lookup - Ag Internal."
long_description: "This document provides internal system administration information about Set OPT for ZIP/Postal Code Lookup - Ag Internal."
---

_Set OPT for ZIP/Postal Code Lookup - AG Internal_

Issue 

 Dealership would like to skip or enable the postal/zip Code validation process. 

 
 Solution 

 Use the Zip/Postal Lookup OPT to configure this feature. Options are: 

 CUST0341,0 to skip the ZIP/Postal validation procedure. 
 CUST0341,1 to automatically validate the ZIP/Postal code with the supplied City, Province/State. 

 Note : Clicking the ZIP/Postal prompt button will take the user to the Selection screen regardless of the OPT setting.