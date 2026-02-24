---
title: "Work with DIS Report Printers – ENVP - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Work with DIS Report Printers – ENVP - AG Internal."
long_description: "This document provides internal system administration information about Work with DIS Report Printers – ENVP - AG Internal."
---

_Work with DIS Report Printers – ENVP - AG Internal_

Work with DIS Report Printers – ENVP 

 There are two variable settings in ENVP that determine printer assignments for users:

 User
 User/Device

   

 The rules that are common to both settings: 

 Any user who has not accessed ENVP to select a printer will by default be assigned to the ‘System printer’. 
 The selections on this screen do not affect Point of Sale printer assignments. 

 Option 1, U ser  Each user goes to ENVP one time and selects a report printer.  No matter where they sign on, their assigned printer remains the same.

 This is by far the cleanest, easiest setting, at least when to comes to troubleshooting.  The question “Which printer is my default” is quickly and easily answered: 

  

 

  

 Option 2, User/Device .  This allows each user to select a different printer for each combination of user and device that is created:

 

  

 With the User/Device setting the answer to the question “Which printer is my default” is “It depends.”

 For example:

 User SUPPORT is signed onto a session named HANSOJIM1A.  In ENVP this combo of User/Device has selected printer NP.

 User SUPPORT is also signed onto a session named HANSOJIM1B and in ENVP selected printer JZ for this user/device combo.

 If user SUPPORT then starts a new session, named HANSOJIM1C, and does not access ENVP to select a printer for this combination of user/device, by default that user/device combo will be assigned to the ‘System printer’… NP in the screen shot above.