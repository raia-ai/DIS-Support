---
title: "DIS-5059 The Employee Address Entered is not Valid Error Message - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DIS-5059 The Employee Address Entered is not Valid Error Message - Ag Internal."
long_description: "This document provides internal system administration information about DIS-5059 The Employee Address Entered is not Valid Error Message - Ag Internal."
---

_DIS-5059 The Employee Address Entered is not Valid Error Message - AG Internal_

Issue 

 The following Error Message displays when adding a labor line directly to a work order in P.O.S. Invoicing: 

 DIS-5059 The employee address entered is not valid. 

 When adding a labor line to a work order in P.O.S. Invoicing, the system looks at the Credit account assigned to the Labor Sales Code. If the credit account has a D edit code, the tech must be setup in payroll in order to add the labor line. 

  

 Solution 

 Either setup the tech ID in payroll or add the time using Review by Technician in time clock.