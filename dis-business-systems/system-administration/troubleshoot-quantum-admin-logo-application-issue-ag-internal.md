---
title: "Troubleshoot Quantum Admin Logo Application Issue - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Troubleshoot Quantum Admin Logo Application Issue - Ag Internal."
long_description: "This document provides internal system administration information about Troubleshoot Quantum Admin Logo Application Issue - Ag Internal."
---

_Troubleshoot Quantum Admin Logo Application Issue - AG Internal_

Issue 

 The Customer updated their logo using the Theme option in Quantum Admin, but the old logo is still displaying on the Quantum Remote Access and Sign On screens despite showing the new logo when signed in. 

  

 Example 

   

   

 Once signed on, the logo is correct as shown below. 

   

  

 Solution 

 This issue may be the result of the logo not being assigned to all necessary options. 

 Access Quantum Admin through the User Authority and Quantum option in Master Security Maintenance. 

 Click the Theme tab. The Theme screen displays. 

   

 The new logo needs to be applied to each of the following options (located on the left side of the screen): 

 Enterprise - Assigns the logo to the Remote Access login screen. 
 Fileset - Assigns the logo to the Sign On screen. 
 Division - Assigns the logo to the Session once signed on.