---
title: "Change GST Method to 0 for All Customers - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Change GST Method to 0 for All Customers - Ag Internal."
long_description: "This document provides internal system administration information about Change GST Method to 0 for All Customers - Ag Internal."
---

_Change GST Method to 0 for All Customers - AG Internal_

Issue 

 If a dealership decides they want to start collecting GST, they will need to assign each of the customers one of the four available GST Methods. This document provides instruction on how to assign all customers the base GST Calculation Method 0 (Not Calculated) and then update individual customers with the appropriate GST Method. 

 

 Prior to adding GST information to sales codes, it didn’t matter what GST method was associated with the customer address since it wasn’t calculated. 

  

 Solution 

 Make a Copy of the ADM. Open a Command Line and run the following command to see all addresses in the ADM that are NOT currently set to Method 0: 

 DISSQL REQUEST('select * from adm where aba2nb <> ''0''') 

 A screen similar to the following displays: 

 

 Open a Command Line and run the following command to assign all addresses to Method 0 : 

 DISSQL REQUEST('UPDATE adm SET aba2nb = ''0''') 

 Update the GST Method assignment for individual customers through Receivables Maintenance. 

 Note Consider changing the default GST Method assigned to new addresses to Method 0 using the Default Canadian GST Method Option .