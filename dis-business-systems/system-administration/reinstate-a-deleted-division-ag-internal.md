---
title: "Reinstate a Deleted Division – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Reinstate a Deleted Division – AG Internal."
long_description: "This document provides internal system administration information about Reinstate a Deleted Division – AG Internal."
---

_Reinstate a Deleted Division – AG Internal_

Issue 

 If a dealer accidentally or intentionally deletes a division and wants to restore it, they can't just re-enter the lock and key like starting a new division. Reinstating the division requires an extra step in the setup process. 

 In this example, division T is the deleted division, as indicated by the '*' in MASP. 

 

  

 To Reinstate Division 

 Select Security Maintenance (Security | Security Maintenance) and input the master security code which is @ by default, but may have been changed. 

 

 Enter the division you want to reactivate using the same process as adding a new division and press Enter . 

 

 The Adding New Division Lock & Key screen displays like when adding a new division. Input the key number from the LOCK program in SC/400 and press F2 to continue. The next screen displays. 

 

 Change the Division code from @ (or whatever the master code is) to the division you intend to reactivate. In this case, division T . 

 Press Enter . The Security Maintenance screen displays. 

 

 Enter Y as directed, and press Enter to reinstate the division. 

  

 Once a division is reinstated, the data listed below needs to be manually re-added. Click here for instructions. 

 The branch name used by 360 pages.
 Security codes used by that division.
 Quantum 360 User Configuration.
 The Management 360 table used to cross reference a unit location to a division.
 The Parts Daily Transfer configuration.
 Which sales codes for the division are used by Service Logistics.