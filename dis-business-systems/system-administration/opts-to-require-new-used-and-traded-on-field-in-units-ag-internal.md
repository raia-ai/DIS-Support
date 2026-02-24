---
title: "OPTs to require New/Used and Traded On field in Units - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about OPTs to require New/Used and Traded On field in Units - Ag Internal."
long_description: "This document provides internal system administration information about OPTs to require New/Used and Traded On field in Units - Ag Internal."
---

_OPTs to require New/Used and Traded On field in Units - AG Internal_

**INTERNAL ONLY** 

 OPTs to require New/Used and Traded On field in Units 

 INTRODUCTION 

 This custom OPT will allow the Dealers to force New/Used to be checked when creating a Unit #.  They can take this one step further and also require the Traded On field to be required when creating used units. 

 Please make sure to review the customer facing document when advising a customer on how these options work and make sure the Dealer has considered all items in that document. 

 

 SETTING THE OPT 

 This custom OPT is a phone option and has 3 settings. 

  

 Opt:  UNITNU 

  

 Settings: 

 Default – New/Used flag can be left blank or set to N or U 
 New/Used flag must be selected to N or U 
 New/Used flag must be selected to N or U, AND if marked U, Traded On field must be filled with a valid unit # 

  

 To set OPT, at a command line type: 

 X00081 UNITNU,0 

 X00081 UNITNU,1 

 X00081 UNITNU,2 

  

  

 Click the following link to see the customer facing document related to the Opt.  

 https://perseus.my.site.com/DISSupportPortal/s/article/Require-Entries-in-NewUsed-and-Traded-on-Fields-when-Adding-Units-Quantum