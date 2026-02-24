---
title: "Remove Dealer Access to Service Logistics - Internal"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Remove Dealer Access to Service Logistics - Internal."
long_description: "This document provides information about Remove Dealer Access to Service Logistics - Internal from the DIS Salesforce Knowledge Base."
---

Follow the steps of this document in the order presented to ensure the dealership wants to be removed and that it is done correctly. 

  

 Confirm Dealer Offboarding 

 If there is a Service Cloud case labeled “Remove SL Access”: 

 Check for attachments and case comments: 

 Is the dealer requesting historic access? 
 Or are they requesting complete removal? 

 Internal Case Handling: 

 Treat this as an internal case. 
 Set Type and Resolution Category to Account Management . 
 This ensures the case stays off the customer portal and a survey is NOT triggered. 

 Verify Effective Date: 

 Do NOT remove access before the agreed-upon date. 
 If the case lacks clear direction, reach out to Tammy Mitchell in Accounting to confirm whether historic access is needed or if access should be completely removed. 

 Remove SL Access 

 Remove SL Tech Roles: 

 Use SLOR or Altura to remove the tech role from each user. 

 Adjust License Count: 

 Go to Setup UI:  Setup > License Count 
 Change the license count to: 
 1 if the dealer requires historic access 
 0 if access should be fully removed 

 Finalize the Case 

 Document all actions in the case comments. 
 Close the case.