---
title: "Set Default Price Level for New Customers in P.O.S. - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Set Default Price Level for New Customers in P.O.S. - AG Internal."
long_description: "This document provides internal system administration information about Set Default Price Level for New Customers in P.O.S. - AG Internal."
---

_Set Default Price Level for New Customers in P.O.S. - AG Internal_

Issue 

 Dealership want to change default price level. Beginning in version 11.1, an Option is available that allows the default price level to be set in Point of Sale for all new customers. The price level is 4 by default. 

  

 Solution  

 Open a command line by simultaneously pressing the Alt and A keys on your keyboard. 

 Enter the command X00081 CUST0156,* substituting the asterisk with the number that represents the price level you want to set as the default. 

 
 Price Level 

 
 Correlating Option Number 

 
 
 Dealer Net 

 
 3 

 
 
 Internal 

 
 2 

 
 
 Suggested List 

 
 1 

 
 
 Dealer List 

 
 0 

 
 

  

 For Instance : To set the default Price Level to Suggested List, you would enter X00081 CUST0156,1.