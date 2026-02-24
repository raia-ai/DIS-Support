---
title: "KPS Registry Fix – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about KPS Registry Fix – Ag Internal."
long_description: "This document provides internal system administration information about KPS Registry Fix – Ag Internal."
---

Issue 

 Can’t get into the KPS icon in the system tray. 

  

 Solution 

 Type “regedit” in the search field and go into it. If you’re not comfortable with the registry, ask someone to do it. 

 

 Make sure Keystone is closed and delete the “Legasuite Printer Client”. 

 Re-open Keystone and it should be fixed.