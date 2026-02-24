---
title: "Quantum Direct Access ( QDA ) connections FAQs & Troubleshooting - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Quantum Direct Access ( QDA ) connections FAQs & Troubleshooting - AG Internal."
long_description: "This document provides internal system administration information about Quantum Direct Access ( QDA ) connections FAQs & Troubleshooting - AG Internal."
---

_Quantum Direct Access ( QDA ) connections FAQs & Troubleshooting - AG Internal_

Quantum Direct Access ( QDA ) connections FAQs & Troubleshooting   

 
   

 
 What is Quantum Direct Access? 

 
 Quantum Direct Access capability allows customers to connect to Quantum over the Internet, not relying on the VPN tunnel for base functions.     

 
   

 
 Can you use the existing Quantum URL to connect? 

 
 Yes, The DNS record will be updated to point the existing URL at the new direct connect proxy in AWS.    

 
   

 
 Will reports print like normal? 

 
 Yes, if a VPN tunnel from the location where printers reside is open to the AS400.    

 
 If, for some reason, the VPN tunnel is down print spools will not be able to be transmitted to the printers via the IBM iSeries connection. There are some work arounds however for these situations. You can send the reports to a local network printer from Quantum Report Center. You could email an invoice directly from the POS Invoicing screen.   

 
   

 
 Will EZ File /Unit Pics/Display/etc. still work with QDA? 

 
 Yes.    

 
   

 
 Will ac cess to Altura still work with QDA? 

 
 Yes.