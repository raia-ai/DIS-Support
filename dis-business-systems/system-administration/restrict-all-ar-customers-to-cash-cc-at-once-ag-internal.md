---
title: "Restrict ALL AR Customers to Cash/CC at Once - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Restrict ALL AR Customers to Cash/CC at Once - AG Internal."
long_description: "This document provides internal system administration information about Restrict ALL AR Customers to Cash/CC at Once - AG Internal."
---

_Simultaneously Restrict ALL AR Customers to Cash/CC - AG Internal_

Issue 

 Customer wants to update every Accounts Receivable address in all divisions so they are restricted to cash/credit card because they are either no longer doing AR or they were set up incorrectly. 

  

 Solution 

 Make a copy of the REO file, then use the following SQL to update all addresses: DISSQL REQUEST('update reo set rocash = ''Y''') 

 Manually remove the restrictions from the _CASHd address and then any warranty or internal AR addresses. 

 Use the following SQLs to update all addresses in a single division to cash only. Division G is being used in this example. 

  

 To display all REO records in Division G: 

 DISSQL REQUEST('select * from reo where roaddr in (select abaqcd from adm where abb7tx = ''G'')') 

  

 To update them to cash only: 

 DISSQL REQUEST('update reo set rocash = ''Y'' where roaddr in (select abaqcd from adm where abb7tx = ''G'')')