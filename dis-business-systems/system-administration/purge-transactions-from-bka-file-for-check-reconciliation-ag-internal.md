---
title: "Purge Transactions from BKA File for Check Reconciliation - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Purge Transactions from BKA File for Check Reconciliation - AG Internal."
long_description: "This document provides internal system administration information about Purge Transactions from BKA File for Check Reconciliation - AG Internal."
---

_Purge Transactions from BKA File for Check Reconciliation - AG Internal_

Issue 

 A customer wants to start using the check reconciliation program and they have multiple old transactions in the BKA file that need to be cleared out. 

  

 Solution   

 The option that you select depends on the transaction date that the user wants to begin reconciliation. Before performing either option, make a copy of the BKA file by entering following information in a command line and clicking OK : 

 CPYF FROMFILE(FILEu/BKA) TOFILE(FILE u /BKACPY) MBROPT(*ADD) CRTFILE(*YES) - where u is the Fileset. 

  

 To Clear Transactions 

 Type DISSQL in a command line and click OK . Copy the SQL request(s) below that reflect the dealers needs and paste on them screen that opens, then click Enter .  

 Note : Adjust the last two digits of the SQL(s) that you use to reflect the year or month that you want to begin reconciling.  

 Run this SQL if the customer wants to begin reconciling account A1010 starting on January 1, 2020: 

 Delete from bka where bkacct = ‘A1010’ and bkayy < '20' 

                       

 Run these SQLs if the customer wants to begin reconciling account A1010 starting on a specific month such as March 1, 2020: 

 Delete from bka where bkacct = ‘A1010’ and bkayy < '20' 

 Delete from bka where bkacct = ‘A1010’ and bkamm < '02'