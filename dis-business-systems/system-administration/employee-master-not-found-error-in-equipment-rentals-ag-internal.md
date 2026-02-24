---
title: "Employee Master Not Found Error in Equipment Rentals - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Employee Master Not Found Error in Equipment Rentals - Ag Internal."
long_description: "This document provides internal system administration information about Employee Master Not Found Error in Equipment Rentals - Ag Internal."
---

_Employee Master Not Found Error in Equipment Rentals - AG Internal_

Issue 

 User is trying to close a rental contract and an error comes up stating: 

 The Employee Master Not Found 

 This is a result of the current sold by on the contract no longer being in Payroll. 

  

 Solution 

 If the employee is still active they will need to add the address back to payroll. If not, DISFU on the LQHP and change position 24-29 to a current employee address.