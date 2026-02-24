---
title: "Info Requiring Manual Entry If Division is Accidentally Deleted - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Info Requiring Manual Entry If Division is Accidentally Deleted - Ag Internal."
long_description: "This document provides internal system administration information about Info Requiring Manual Entry If Division is Accidentally Deleted - Ag Internal."
---

_Info Requiring Manual Entry If Division is Accidentally Deleted - AG Internal_

Issue 

 A division was accidentally deleted from X66 and there is unsurety about what things have been removed from the system that need to be manually re-added.  

 According to Jeff North (07/06/2020), the following data is deleted and won’t automatically “come back” by reinstating a division:

 The branch name used by 360 pages.
 Security codes used by that division.
 Quantum 360 User Configuration.
 The Management 360 table used to cross reference a unit location to a division.
 The Parts Daily Transfer configuration.
 Which sales codes for the division are used by Service Logistics.

  

 Solution 

 Reinstate the division at X66 and manually enter the following items:

 Select Security Maintenance (Security | Security Maintenance) and do the following:

 Enter the division code and provide the branch name used in the 360 pages in the field at the bottom of the screen when the Division tab is selected.

  

 Enter the division code, click Security Codes , and provide the security codes for the division.

  

 Enter the master security code ( @ ), then click User Authority & Quantum . Hold the Ctrl key, select each user, and click the Quantum 360 User Cnfg  button. Select the appropriate divisions for each KPI for the first user. When complete, click Back to move to the next user and select their divisions for each KPI. Repeat for the remaining users.

  

 Recreate the Management 360 table used to cross reference a unit location to a division through Quantum Unit Location Table (Units | Quantum Unit Location Table) .

 Recreate Configure Parts Daily Transfers setup (Parts | Parts Configuration | Configure Parts Daily Transfers) 

 Designate the sales codes used by the division for Service Logistics through the Sales Code menu (P.O.S | Table Maintenance | Sales Code) by entering the Parts Sales code for Service Logistics and clicking the Assign Service Logistics Part Assigned button.