---
title: "Disable Shading on POS Invoices - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Disable Shading on POS Invoices - AG Internal."
long_description: "This document provides internal system administration information about Disable Shading on POS Invoices - AG Internal."
---

_Disable Shading on POS Invoices - AG Internal_

Introduction 

 This document provides instruction on removing the gray shaded areas on printed invoices. A check box in Laser Forms Configuration controls the shaded lines that alternate between part lines. 

 An option controls whether or not the gray Sold By/Ship By box above the parts lines and the Customer Phone Number box at the bottom of the invoice display. 

   

  

 To Remove Part Line Shading 

 Select Laser Forms Configuration (Security | Laser Forms Configuration) and select the Disable POS Documents Shading check box to stop shading alternating part lines. 

 Note : This only controls the setting for the current division in which the user is working. 

   

  

 To Remove Gray Boxes 

 An option exists that stops the printing of the gray boxes at the top and bottom of an invoice. 

 Note : This is a File set/Company wide setting that will affect invoices in all divisions. 

 Open a command line, enter X00081 CUST0250,1 and click OK  to stop printing the gray boxes as shown below. 

   

 Open a command line, enter X00081 CUST0250, 0 and click OK to begin printing the gray boxes again.