---
title: "Enable Technician View - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Enable Technician View - AG Internal."
long_description: "This document provides internal system administration information about Enable Technician View - AG Internal."
---

Introduction 

 This article details how to enable tech view. 

 Important! 

 Enabling tech view prevents Time Clock from working in Green Screen. 
 Tech view CANNOT be enabled if there is an employee currently punched into Time Clock. 
 This process needs to be completed in each division. 

  

 Enable Tech View 

 Open an AS/400 Command line (System | AS/400 Command Line). 

 

 Type X00081 TCNWO d ,1 (where d = the division code) and click OK .