---
title: "Prevent Report Center Credential Request when Opening – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Prevent Report Center Credential Request when Opening – Ag Internal."
long_description: "This document provides internal system administration information about Prevent Report Center Credential Request when Opening – Ag Internal."
---

Issue 

 Invalid credentials repeatedly launch the IBM SIGNON prompt. The Credential Request keeps displaying when the IBM CAX application System i Navigator is incorrectly configured with invalid credentials. 

  

 Resolution 

 

 Open System i Navigator from the Desktop or the start menu. 

 

 Right-click on Keystone and select Properties . 

 

 Select the Connection tab , select the Use default user ID option and enter DISUSER in the text box. 
 Click OK and close System i Navigator. 
 Open a new Keystone session and select Keystone Report Center . 
 Use DISUSER for the username and the password. Credential requests should no longer happen.