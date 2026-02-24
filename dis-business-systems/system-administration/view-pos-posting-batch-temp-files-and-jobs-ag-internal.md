---
title: "View POS Posting Batch Temp Files and Jobs - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about View POS Posting Batch Temp Files and Jobs - AG Internal."
long_description: "This document provides internal system administration information about View POS Posting Batch Temp Files and Jobs - AG Internal."
---

Introduction 

 This article provides a list of the Files and Jobs created when a POS posting batch is created and posted. 

  

 View Files/Jobs Generated with Batch Creation 

 Open a command line, type WRKF u.@* (where u is the file set letter), and click OK . The Work with Files screen displays. 

 

 When Create Point of Sale Posting Batch is run (P.O.S. | Post P.O.S. Documents | Create Point of Sale Posting Batch) , it creates the SAE and SA7 temp files shown above. The first letter in the file name is the file set and the letter after the @ symbol is the division.  So, in the example below, these files show a batch created in file set Z, division K. 

 Nothing will show in Take Workstation ID.  

 View Files/Jobs Generated with Batch Posting 

 When the batch is posted (P.O.S | Post P.O.S. Documents | Review and Post Point of Sale Documents) , it generates the Create Source Documents temp files shown below in the Take Workstation screen. 

 

 

 The SAE and SA7 temp files on the Work with Files screen are replaced with the temp files shown above. 

 The one that ends in the A is the header, the one that ends in the B is the detail.  If a user is not currently looking at the batch, you can display the physical file member for the B file to see the detail in it. 

 If delayed batch is created in Create Point of Sale Posting Batch, it can be viewed by typing the DD command in an AS/400 Command Line and locating the X00082 job at the bottom of the screen.  The time the delayed batch is scheduled to run is also listed.