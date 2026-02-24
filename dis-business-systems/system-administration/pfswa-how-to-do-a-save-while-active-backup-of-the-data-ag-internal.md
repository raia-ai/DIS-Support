---
title: "PFSWA - How to do a Save While Active backup of the data - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about PFSWA - How to do a Save While Active backup of the data - Ag Internal."
long_description: "This document provides internal system administration information about PFSWA - How to do a Save While Active backup of the data - Ag Internal."
---

_PFSWA - How to do a Save While Active backup of the data - Ag Internal_

Introduction 

 Occasionally we have a situation with a customer where they are having an issue on the system and it's a good idea to backup the files before we take an action to resolve their issue.  A key example if Parts End of Month.  With parts end of month we have several temporary files at play and it is important to keep the correct files in sync for a successful recovery.  A command was created to get a full data backup of the system while people are still on the system.  aka: Save While Active. 

  

 Solution 

 At a command line, type: CALL PFSWA and press enter.  

 This command runs 3 processes that backup all 3 data libraries. 

 QS36F 

 FILEu (Where 'u' equals the fileset) 

 DISFILES 

  

 This process usually takes 3-5 minutes but we have seen it take as much as 30 minutes at a very large dealership. 

  

 These backup save files will be help in a library called DISSWA. 

 To view the objects in this library type: WRKF DISSWA/*ALL and press enter 

 0 

 File name = First letter is the fileset, followed by MMDD then HHMM and finally the sequence number. (Sequence 0 = QS36F, 1=FILEu and 2 = DISFILES) 

  

 It is very important that we go back and remove these libraries before we fully close out ticket with the customer.  

 These backup files take up space and we want to make we are keeping things clean.  

  

 To remove files. 

 Type: WRKF DISSWA/*ALL and press enter.   

 Put a 4 on each line you want to Delete and press enter.  Then enter to confirm.  

  

 If you are needed to use these files.  Please ask for help from Mike, Ruth or development. 

 A RSTOBJ command it necessary to restore specific file to put them in a prescribed location.