---
title: "Create a New Service Scheduling Group Queue for Dealers – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Create a New Service Scheduling Group Queue for Dealers – Ag Internal."
long_description: "This document provides internal system administration information about Create a New Service Scheduling Group Queue for Dealers – Ag Internal."
---

Scenario: Is there a way to create a Queue not assigned to a technician in the Queue view so the dealer can have WOs in there and can the dealer later drag those jobs into a techs queue when the dealer is ready to assign them? 

  Access Altura. 

 

 Select Scheduling (Service | Scheduling) . 

 

 Click on Groups , then click + New Group to create a New Queue 

 

 Enter the Group Name. 
 Assign a Branch if desired. 
 DO NOT assign a Technician. Assigning a Technician will result in jobs being assigned. 
 Click Save Group . 

 The new group displays in the table and the dealership can drag and drop work orders in that group. That group can then be drag and dropped into a Technician’s queue. 

 In the example below, Towline has created a Sales Group and dropped 5 work orders into the group. That group is then dragged and dropped into Tyler M’s queue.