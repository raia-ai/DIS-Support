---
title: "Uninstall AGCO API in a Single Division-AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Uninstall AGCO API in a Single Division-AG Internal."
long_description: "This document provides internal system administration information about Uninstall AGCO API in a Single Division-AG Internal."
---

Introduction 

 This article details how to uninstall AGCO API 

  

 Set OPT to stop Uploads for the Division 

 Disable the AGCLOADd option for the division you want to stop uploading. 

 Remove API Workstation Parameters 

 Select Electronic Commerce Configuration (Security Electronic Commerce | Electronic Commerce Configuration). 
 Select the AGCO vendor and open Parameters. 

 

 Delete the Workstation name from the API transaction codes used to interface with Interface Manager ECC: 

 AGCOFTP 
 EOD 
 RESENDA 
 UPLOAD 

 Delete Vendors 

 Select Vendor Maintenance (AGCO Communications | Vendor Maintenance) . 
 Delete any vendors listed.  

 

 Remove Install Keys 

 Run X000B6RP to remove the install keys for each division you want to turn off.