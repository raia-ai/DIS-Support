---
title: "Copy Files from QS36F and/or FILEu Libraries – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Copy Files from QS36F and/or FILEu Libraries – Ag Internal."
long_description: "This document provides internal system administration information about Copy Files from QS36F and/or FILEu Libraries – Ag Internal."
---

Introduction 

 This article details how to copy files from the QS36F and FILEu Libraries. 

  

 Files in QS36F Library 

 Files in the QS36F library are files like IVT, SAM, etc. 

 Access Command Entry screen. 

 

 Type the command CPYF u . FILENAME where u is the File set.  

 Example : If copying an IVT file from file set P , the command is CPYF P.IVT as shown in the screenshot above and press Enter . 

 

 Enter a name for the copy being created in the To File field that starts with the file set letter - P.IVTG0723 in the example above. 
 Enter QS36F in the Library field. 
 Type *YES in the Create File field. 
 Press Enter . 

  

  

 Files in FILEu Library 

 Examples of files in FILEu are OAA, PAA, ADM, etc. 

 

 Access the Master Menu 

 

 Type CPYF FILENAME in the Command line and click Enter .  

 Example : If copying the OAA file, type CPYF OAA as shown in the example above. 

 

 Enter a name for the copy being created in the To File field. 
 Enter FILE u in the Library field where u is the file set.  Z is the file set in the example above. 
 Type *YES in the Create File field. 
 Press Enter .