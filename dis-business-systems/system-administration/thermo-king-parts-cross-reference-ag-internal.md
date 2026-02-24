---
title: "Thermo King Parts Cross Reference - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Thermo King Parts Cross Reference - AG Internal."
long_description: "This document provides internal system administration information about Thermo King Parts Cross Reference - AG Internal."
---

_Thermo King Parts Cross Reference - AG Internal_

Introduction 

 Some Thermo King dealers use an older parts numbering system that includes dashes in the part number. The Thermo King bar code does not typically include the dashes, so DIS created a cross reference utility. This will make it possible for scanning of TK bar codes. 

   

 Steps to add Thermo King Cross Reference information. 

 Sample part number 40-1001 does not have any cross reference information. 

 

  

 Select AS/400 Command Line (System | AS/400 Command Line) or click the ALT and A keys on the keyboard at the same time.  

 

 Type TKXREF in the command line and click OK . The utility will run. This job does not require a dedicated system. 

 

 Once the job is complete, you’ll see a cross reference record that allows scanning of these parts.