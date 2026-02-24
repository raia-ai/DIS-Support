---
title: "CPF4161 Error Message during OPEN for file DMPIMI – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about CPF4161 Error Message during OPEN for file DMPIMI – Ag Internal."
long_description: "This document provides internal system administration information about CPF4161 Error Message during OPEN for file DMPIMI – Ag Internal."
---

_CPF4161 Error Message during OPEN for file DMPIMI – Ag Internal_

Issue 

 Received the following Error Message:   

 Error message CPF4161 appeared during OPEN for file DMPIMI (C S D F).                                                                  

                                                                            

 Cause . . . . . :   RPG procedure X3900K in program LIBRARY/X3900K received the message CPF4161 while performing an implicit OPEN operation on file DMPIMI. 

 The actual file is DMPIMI. 

  

 Solution 

 This message occurs when the Parts Data Mine file contains duplicate keys and needs to be rebuilt. Complete these steps to resolve: 

 End the backup from the user board. 

 Release ECM and the jobq. 

 End the QDISDMPIMu job (where u = file set). 

 Use the WRKOBJLCK command to find any jobs holding locks on the DMPIMI file and end all jobs holding a lock. 

 Use CLRPFM on the DMPIMI and DMPIOI files. 

     CLRPFM DMPIMI 

     CLRPFM DMPIOI 

  

 Run the PFDMPALL command to rebuild the Data Mine files.