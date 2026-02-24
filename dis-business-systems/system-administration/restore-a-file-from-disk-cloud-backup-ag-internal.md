---
title: "Restore a file from Disk - Cloud Backup - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Restore a file from Disk - Cloud Backup - Ag Internal."
long_description: "This document provides internal system administration information about Restore a file from Disk - Cloud Backup - Ag Internal."
---

_Restore a file from Disk - Cloud Backup - AG Internal_

Introduction 

 This document provides instructions on the process of restoring a file from the previous night's disk backup. 

 Note: This is for dealers who have Cloud Backup. With Cloud Backup we only keep one backup on disk. Restoring files moved to the cloud is a different process. 

   

 To Restore a File 

 Step 1:  Go into Backup History Log 

 

 Step 2: Display the Library that contains the file you want to restore. In this example we are restring PEM so we will display FILES 

 

 Step 3: Copy the FTP Filename for the Library 

 

 Step 4: Create a Library (CRTLIB) to restore the file into. Ex. CRTLIB DISTEST 

 

 Step 5: Retore Object (RSTOBJ) into the library 

 
 Object – PEM 
 Saved Library – FILES 
 Device - *SAVF 
 Save File – FILES15626 (see above) 
 Library DISBACKUP 

 

 Page down for additional information 

         Restore to library – DISTEST 

 

 Press ENTER 

 

 WRKF *ALL/PEM