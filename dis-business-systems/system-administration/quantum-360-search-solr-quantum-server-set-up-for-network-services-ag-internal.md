---
title: "Quantum 360 Search - Solr - Quantum server set up - for Network Services - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Quantum 360 Search - Solr - Quantum server set up - for Network Services - Ag Internal."
long_description: "This document provides internal system administration information about Quantum 360 Search - Solr - Quantum server set up - for Network Services - Ag Internal."
---

_Quantum 360 Search - Solr - Quantum server set up - for Network Services - AG Internal_

Activate C360 Search Feature 

  

 Note : This article deals with Quantum Server Setup. Click here to view an article detailing the changes and steps for enabling on the Business System Side. 

  

 Business system releases 

 DIS_NR63 and above 

 23v2 + JN01698 and above 

 Enable OPT on business system (per file set) 

 X00081 CUST0345,1 

 Enable Solr service on the Quantum Server . 

                 

 The service will sync on startup. 

 

 Do a solr sync by going to their URL and remove webclient and add solr. 

 Slide bar to pull latest image version, then update. 

  

 Example: 

 https://woodstockeq.dis.us /webclient/ 

 useà https://woodstockeq.dis.us/solr/#/ 

 Select Core and select the fileset you need to sync.  If they have multiple filesets this will need to be done for each one. 

 

 Select Data Import. 

 Check ‘Optimize’. 

 Check Auto Refresh Status 

 Select Execute. 

 This will take a few minutes depending on how much data they have. 

 

 

 You should get a message when complete.