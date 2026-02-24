---
title: "POS Invoice Document Class(es) Not Printing – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about POS Invoice Document Class(es) Not Printing – Ag Internal."
long_description: "This document provides internal system administration information about POS Invoice Document Class(es) Not Printing – Ag Internal."
---

Issue 

 Specific document classes are not printing in P.O.S. Invoicing. This may be the result of the Document Classes in Laser Form Configuration being assigned to a different printer than what is assigned in P.O.S. Invoicing. 

 In this example, the user has P5 on all printer options on the POS Printer Selection screen: 

 

 Doc classes II and IS print to P5, but Doc Class IR does not print. 

 This customer has the following Document Classes for Sales Orders: 

 Sales Orders 

 A - ROA CREDIT CARD 

 I - INVOICE 

 L – RENTAL/LEASING 

 The problem is that in Laser Forms Configuration the Sales Order form has P1 assigned to the Document Classes A and L as shown below. 

 

 With this configuration, ANY invoices that are Document Class A and L are sent to P1, regardless of the POS settings. 

 Notice that Document Class I does not have a printer assigned.  Those documents are sent to the printer assigned on the POS Printer Selection screen. 

 In some instances, the customer wants a specific printer assigned to a particular document class.  Show the customer the e-forms configuration and explain the details, then let them remove the printer name if that’s their desire. 

 Remove the Printer Assignment 

  

 Highlight the Electronic Form and click the Configure button. The Configure Form screen displays. 

 

 Highlight the Document Class and click the Configure button. 

 Remove the printer name from both fields and click Enter to save the changes.