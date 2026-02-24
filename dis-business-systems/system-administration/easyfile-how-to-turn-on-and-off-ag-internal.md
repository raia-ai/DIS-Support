---
title: "EasyFile - How to turn on and off - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about EasyFile - How to turn on and off - Ag Internal."
long_description: "This document provides internal system administration information about EasyFile - How to turn on and off - Ag Internal."
---

_EasyFile - How to turn on and off - AG Internal_

To Turn On 
 Bring up a 400 command line. 
 Type in INSTALL_EF and Press Enter (Note there is an "under bar" between Install and EF ). 
 This will bring up a lock & key screen. 
 Be sure to send the customer documentation about this feature. Articles to consider: 
   
 EasyFile Overview - Quantum 
 EasyFile Overview - Keystone Video Tutorial 
 EasyFile Overview - Quantum Video Tutorial 
 Accessing and Working with EasyFile Documents - Quantum 
 Creating, Naming, and Adding Files to EasyFile - Quantum 
 Enable SMB 1.0 on Windows 10 PCs to Access EasyFile - Keystone 

   
   
 To Turn Off   
 Bring up a 400 command line. 
 Type in CALL X000B6RP and press Enter .  The next screen has a list of the unlocked products from a 400-perspective.  If EasyFile is listed on this screen it means that INSTALL_EF previously unlocked it.       
 Highlight and click the Remove button to turn off.