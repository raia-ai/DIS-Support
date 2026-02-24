---
title: "Kubota Invoice Entry - Setting it up - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Kubota Invoice Entry - Setting it up - AG Internal."
long_description: "This document provides internal system administration information about Kubota Invoice Entry - Setting it up - AG Internal."
---

_Kubota Invoice Entry - Setting it up - AG Internal_

Introduction 

 Kubota Invoice Entry in a method of importing invoices from the Kubota website so our customers can view a PDF of the Kubota Payables invoice, copy invoice information into Quantum Payables Invoice Entry,  and save a PDF copy in Easyfile when posted.  

  

 Solution 

 There are 2 steps to set this up.  

 1st, it needs to be configured on the Quantum Server.  (See below for more details) This step should be performed by someone in Network Services.)  
 2nd, an opt needs to be turned on the business system.  At a command line type: X00081 KUBINV,1 and press enter.  

  

  

 Here are more details for the Quantum service setup. 

 Login to Portainer and navigate to the ‘quantum_util_servlet’ stack. 

 

  

 Choose the Editor tab and add the following environment variable. 

  

 

 Click ‘Update the stack’ 

 

  

  

 Import Kubota Invoicing