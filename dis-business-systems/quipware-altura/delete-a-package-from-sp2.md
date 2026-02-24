---
title: "Delete a Package from SP2"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Delete a Package from SP2."
long_description: "This document provides information about Delete a Package from SP2 from the DIS Salesforce Knowledge Base."
---

Introduction 

 This article explains how to delete a package from  SP2 by accessing the system through a secure shell (SSH) session. The procedure requires logging in with root credentials, navigating to the appropriate customer directory, and removing the specified package file from the outbox. These steps should be performed carefully to ensure that only the intended package is deleted. 

  

 Log into MT-Dev as Root.

 

 Enter  ssh qwftp put in y and enter again. 

 

 Change the directory to  u: cd /u/customer/cusDEALER#. 

 

 Run the command ls -l to list all the directories.

 

 Go to their outbox via cd outbox and then enter ls -l . A package named auth_MT.pkg.gz is returned. 

 

 Enter the command rm auth_MT.pkg.gz to remove the package . 
 Exit MT-Dev.