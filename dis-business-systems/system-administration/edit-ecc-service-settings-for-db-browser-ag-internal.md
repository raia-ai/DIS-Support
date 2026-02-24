---
title: "Edit ECC Service Settings for DB Browser - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Edit ECC Service Settings for DB Browser - Ag Internal."
long_description: "This document provides internal system administration information about Edit ECC Service Settings for DB Browser - Ag Internal."
---

Making changes to ECCService settings when the application hangs “Not Responding” The problem: Users are not able to make changes to settings such as file paths etc.. 

 Navigate to https://sqlitebrowser.org/ and download DB Browser for SQLite. 

  

 Unzip and run the DB Browser for SQLite.exe application as administrator by right clicking and select Run as administrator . 

 

 Select Open Database . 

  

 Navigate to the path C:\ProgramData\dis\im\data and open Meta.sqlite3 . 

  

 To edit the file path for any given manufacturer, select the Browse Data , then select Interface from the table dropdown. 

 All file paths for the manufacturers that have been added to the interface display. 

 To edit the path for AGCO ORD, click to highlight. 

  

 Edit in the edit database cell textbox and click the Apply button. 

 

 Now write the changes to the DB. When starting the interface and viewing the settings for AGCO you can see that change was made as shown below.