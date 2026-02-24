---
title: "Determine If a Dealer Is Actively Using Service Logistics - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Determine If a Dealer Is Actively Using Service Logistics - AG Internal."
long_description: "This document provides internal system administration information about Determine If a Dealer Is Actively Using Service Logistics - AG Internal."
---

_Determine If a Dealer Is Actively Using Service Logistics - AG Internal_

Introduction 

 Multiple dealers are configured for Service Logistics, but not all configured dealers are using it. Service Logistics Online Reports (SLOR) is most reliable method to determine if a dealer is actively using Service Logistics. 

   

 Access SLOR for a Specific Dealer 

 Access https:// xxxxxx .disprism.com/report-api/#/index (replace xxxxxx with the dealer number). 

 Login using the same credentials as Altura: 

 Username:  xxxxxx-admin@xxxxxx.com 
 Password:    $Upp0rt-xxxxxx. 

 Example : Accessing for H & R AGRI POWER (AG1350), you would enter 

 URL: https://ag1350.disprism.com/report/login#/index. 
 Username: AG1350-admin@AG1350.com 
 Password: $Upp0rt-ag1350. 

   

 View Active Service Logistics Users 

 The Service Logistics Online Reports screen displays once you’ve logged in. 

 

 select Technician Management . The Technician Management screen displays. 

 

 Click the Branch drop-down arrow and select the branch (division). 

 

 The technicians in the division and the timestamp of their last communication through Service Logistics display. The information in the Last Communicated column is the most reliable source of whether or not the dealer is actively using Service Logistics.