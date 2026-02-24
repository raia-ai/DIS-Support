---
title: "Export SQL Command to CSV using System i Navigator - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Export SQL Command to CSV using System i Navigator - Ag Internal."
long_description: "This document provides internal system administration information about Export SQL Command to CSV using System i Navigator - Ag Internal."
---

_Export SQL Command to CSV using System i Navigator - Ag Internal_

Export SQL commands to CSV using System i Navigator 
 Steps to export SQL commands to CSV. 
 Click the Windows button and search for "System i Navigator." Open System i Navigator, and then click on the "Add Connection" button. 
 
 Enter the System IP and Description 
 
 The IP address can be found in the ASP/LPAR Server information in vLink 
 
 Click "Next" and change the "Use Default User ID" to "Support." 
 
 Click "Next," verify the connection, and then click "Finish." 
 
 You will now see the new connection listed in "My Connections." 
 
 Click on the plus sign next to the IP of the connection you just created and sign in using the user "Support" and the password "Puget." 
 
 Click on the plus sign next to "Databases," then expand the list by clicking on the plus sign next to the specific database. Right-click on the icon just below it and select "Run SQL Scripts." 
 
 Enter your SQL command, specifying both the library and file with a period (.) between the library and file name, as shown in this example: 
 SELECT F0AQCD, F0O3CD FROM FILEJ.RCC WHERE F0O3CD = 'MV' 
 
 Click “Options” then “Allow Save Results” 
 
 Click “Run” then “From Selected” 
 
 Right-click on the header of the first column in your results and select "Save Results." 
 
 Click "Browse" and save the file locally and assign it a name. Keep the file type as CSV and the Character set as ASCII. 
 
 You can then open and edit your files, assigning meaningful header names that make sense to your customers.