---
title: "Split Charge - Split charge screen not coming up at Point of Sale - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Split Charge - Split charge screen not coming up at Point of Sale - Ag Internal."
long_description: "This document provides internal system administration information about Split Charge - Split charge screen not coming up at Point of Sale - Ag Internal."
---

_Split Charge - Split charge screen not coming up at Point of Sale - Ag Internal_

Issue 

 The customer is set up in Receivables to split a percentage of the ticket to another address or addresses and it's not bringing up the Split charge screen at Point of Sale. 

  

 Solution 

 If Journals are turned on: 

 All sales codes on the ticket must have the same Journal ID.  You can print a Sales Code Report to check 

 or look at each individual sales code in Point of Sale | Table Maintenance | Sales code .  

 or 

 A Parts transfer sales code has been used on the ticket. 

 Check Sales code table to see if any of the Sales codes used on the ticket have PTRAN in the Debit and/or Credit fields. 

 or 

 The debit account on one of the sales codes used on a ticket is not AUTO or *AUTO