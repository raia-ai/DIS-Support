---
title: "Install Scheduled Price Updates - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Install Scheduled Price Updates - AG Internal."
long_description: "This document provides internal system administration information about Install Scheduled Price Updates - AG Internal."
---

_Install Scheduled Price Updates - AG Internal_

To Install Scheduled Price Updates 

 Set DIS Product Key DISGL 
 Set opt X00081D CUST0285,1 (Note it’s a “D” opt. There are two OPT file settings one in FILEu and one in DISFILES OPT. The file name in DISFILES is DOPT.) 
 Configure Electronic Commerce Configuration for Vendor DIS. 

 
 PBF          

 
 PB Get  File 

 
 CHALL24 

 
 
 PBL          

 
 PB List 

 
 CHALL24 

 
 
 PBT                   

 
 PB Get Table 

 
 CHALL24 

 
 

 Configure the Interface Manager. 
 Check the SC/400 to see what books the dealer subscribes to. 

   

 Run a configuration report to see what vendors and price books are currently loaded. 

   

   

 Click Manual Update to get a master list of Price Books. 

   

 The master list of all available price files displays. 

   

 Add books and associate them with the book currently tied to the vendor. 

   

 Run the manual update again to download the price files. 

   

 *EOD Update* displays as part of the description for all price books that were updated.