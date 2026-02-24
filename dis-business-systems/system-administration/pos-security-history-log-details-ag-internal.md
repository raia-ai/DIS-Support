---
title: "POS Security History Log Details -Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about POS Security History Log Details -Ag Internal."
long_description: "This document provides internal system administration information about POS Security History Log Details -Ag Internal."
---

POS Security is controlled by an OPT.  Once turned on, a user ID and password field display on the Sold To screen and users must fill out the fields to access the POS Detail screen. 

 Certain actions are tracked and reported on the POS History Log. This report is generated at parts EOD and the report is automatically archived. 

 This report cannot be run from a menu. Data for this report is stored in the u.STL file which is purged each time end of day is run. 

 The Act (Action) column can contain the following codes: 

 A = Addition (line) 
 M = Modification (line) 
 D = Deletion (line) 
 O = Re-open (document) 
 K = Cancel (document) 
 CL = Closed (document) 
 CX = Void (document)