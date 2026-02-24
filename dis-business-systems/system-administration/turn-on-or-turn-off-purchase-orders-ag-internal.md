---
title: "Turn ON or Turn OFF Purchase Orders - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Turn ON or Turn OFF Purchase Orders - Ag Internal."
long_description: "This document provides internal system administration information about Turn ON or Turn OFF Purchase Orders - Ag Internal."
---

_Turn ON or Turn OFF Purchase Orders - AG Internal_

To Turn ON Purchase Order: 

 Go to the menu option for Purchase Orders and go through the Lock & Key 
Also set X00081 CUST0010,1                          
Then setup Divisional Profile                       
Set up Laser Forms                                  
Set up other codes.                                 
Send Tutorials and Documentation    

  

 To Turn OFF Purchase Order:       

  At a command line: Type: CALL X000B6RP and press enter. 

 Delete the Purchase order line. 

  At a command line: Type:  X00081 CUST0010,0 and press enter.