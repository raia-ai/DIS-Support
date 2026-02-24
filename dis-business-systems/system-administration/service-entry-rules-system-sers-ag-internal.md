---
title: "Service Entry Rules System SERS - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Service Entry Rules System SERS - Ag Internal."
long_description: "This document provides internal system administration information about Service Entry Rules System SERS - Ag Internal."
---

_Service Entry Rules System SERS - AG Internal_

Introduction 

 Service Entry Rules System or SERS allows dealers to define specific parameters for setting fields on their labor lines. This tool was developed because of the limitations of Service Logistics regarding what fields the technicians can supply. It streamlines the input process for dealers by automatically configuring the correct field values on labor lines or part lines based on predefined rules. SERS rules apply to all labor and part lines added from outside of Point of Sale, such as Service Logistics, Time Clock, or an API. 

   

 Rule Example 

 One rule might be: 

 "If the Segment Title contains 'Trucking,' then set the Sales Code to LT, the Work Type code to 5 and the Status Code to 07". 

 The dealer would submit the following template 

 
 Segment Title 

 
 Sales Code 

 
 Work Type Code 

 
 Status Code 

 
 
 Trucking 

 
 LT 

 
 5 

 
 07 

 
 
 Warranty 

     
 05 

 
 
 Internal 

     
 04 

 
 

 We would then create the rule in the SERS file (fileu/SERS) 

 
 SERS _DIV 

 
 SERS_RULEN 

 
 SERS_CLAUS 

 
 SERS_FUNCT 

 
 SERS_LEFT 

 
 SERS_OPER 

 
 SERS_RIGHT 

 
 SERS_SAND1 

 
 SERS_SAND2 

 
 
 A 

 
 1 

 
 1 

 
 IF 

 
 I002 

 
 EQ 

 
 CL 

 
 - 

 
 - 

 
 
 A 

 
 1 

 
 2 

 
 AND 

 
 F003 

 
 CO 

 
 CTRUCKING 

 
 - 

 
 - 

 
 
 A 

 
 1 

 
 3 

 
 THEN 

 
 O004 

 
 EQ 

 
 C07 

 
 - 

 
 - 

 
 
 A 

 
 1 

 
 4 

 
 THEN 

 
 O005 

 
 EQ 

 
 C5 

 
 - 

 
 - 

 
 
 A 

 
 1 

 
 5 

 
 THEN 

 
 O002 

 
 EQ 

 
 CLT 

 
 - 

 
 - 

 
 

 Note : Quantum development handles any modifications or additions to a dealer's SERS Table. If a dealer requests an addition or change, please create a Jira QSUP ticket.