---
title: "P.O.S. Reassignment Error Regarding Service Logistics when SL is Not Enabled - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about P.O.S. Reassignment Error Regarding Service Logistics when SL is Not Enabled - AG Internal."
long_description: "This document provides internal system administration information about P.O.S. Reassignment Error Regarding Service Logistics when SL is Not Enabled - AG Internal."
---

_P.O.S. Reassignment Error Regarding Service Logistics when SL is Not Enabled - AG Internal_

Issue 

 If a customer receives the  Service Logistics: With new address number, document number may not be retained message when trying to reassign a P.O.S. document and they do not have Service Logistics, they may have inadvertently indicated a sales code as a Service Logistics Parts Sales Code in Sales code Maintenance. 

   

 Important!  If the customer Does Have Service Logistics, they will need to unselect the Retain document number check box under the Reassign Point of Sale Document option.  

  

 Solution 

 Important!   If the customer Does Have Service Logistics DO NOT do the following steps. 

 Display the SAMSVCT file to see which sales codes have a Service Logistics assignment by entering DSPPFM SAMSVCT in a command line ( Alt + A ).  

 Access the Sales Code in Sales Code Maintenance (P.O.S. | Table Maintenance | Sales Code). 

 

 Remove the assignment. The customer will be able to reassign the document and keep the document number.