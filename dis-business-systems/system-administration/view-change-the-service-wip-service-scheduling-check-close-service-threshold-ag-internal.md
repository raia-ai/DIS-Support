---
title: "View/Change the Service WIP / Service scheduling 'Check Close' Service Threshold - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about View/Change the Service WIP / Service scheduling 'Check Close' Service Threshold - AG Internal."
long_description: "This document provides internal system administration information about View/Change the Service WIP / Service scheduling 'Check Close' Service Threshold - AG Internal."
---

_How to View/Change the Service WIP / Service scheduling 'Check Close' Service Threshold_

I n Service WIP open work orders with all labor lines dated older than the dealership defined Service Threshold are classified as "Check Close". 

 By default, the threshold is set to 14 days. There are two ways to view or change this threshold. Note: These same changes also change Service Scheduling. 

 Sign on as SUPPORT. At a command line type INSTALL_P2. The first screen you'll see is the Receivables KPI screen. If it is locked, press <F1> to move passed it, if it’s unlocked, press <F2> to move to the next KPI. 

 The next screen will be the Payables KPI screen. If it is locked, press <F1> to move passed it, if it’s unlocked, press <F2> to move to the next KPI. 

 The next screen will be the Service WIP screen. Here you can view or change the Service Threshold.            

   

 A quicker way to view or update the Service Threshold is to update the X0PR000038 file in the DISFILES library. 

 At a command line type UPDDTA X0PR000038 and page down. Change the X383ST value to new Service Threshold. 

  

 

 Configure Service WIP to Include 0$ Work Orders 

 Users may call in to configure Service WIP to include 0$ work orders using the WIPZERO option . Potential settings include: