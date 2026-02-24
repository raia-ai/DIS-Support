---
title: "DISTEMP Library Maximum Capacity Error Message - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DISTEMP Library Maximum Capacity Error Message - AG Internal."
long_description: "This document provides internal system administration information about DISTEMP Library Maximum Capacity Error Message - AG Internal."
---

_DISTEMP Library Maximum Capacity Error Message - AG Internal_

Issue 

 When the DISTEMP library has reached its maximum capacity, the File XXXXX not created in library DISTEMP error message will display. This can present in the following scenarios: 

  

 System operator messages on manufacturer part order submissions. The example below is an error for a Kubota order request. 

 CPF7302 received by KUB500INX0 at 3800. (C D I R) 

 Message . . . . :   CPF7302 received by KUB500INX0 at 3800. (C D I R)         

 Cause . . . . . . :    Control language (CL) program KUB500INX0 in library       

 LIBRARY detected an error at statement number 3800. Message text for CPF7302 

 is: File M2659020 not created in library DISTEMP.                           

 Recovery  . . . :    This inquiry message can be avoided by changing the       

 program. Monitor for the error (MONMSG command) and perform error recovery  

 within the program. To continue, choose a reply value.                      

  

 Error on parts communication with a manufacturer. The example below is an error for a part communication via CSPS with CNH. 

 Message . . . . :    CPF7302 received by CAS500IQX0 at 4500. (C D I R)         

 Cause . . . . . . :    Control language (CL) program CAS500IQX0 in library       

 LIBRARY detected an error at statement number 4500. Message text for CPF7302 is: 

 File M2659794 not created in library DISTEMP.                           

  

 Solution   

 Do one of the following to delete files from DISTEMP Library: 

 Delete some files manually using the DLTF command 
 Run Parts EOM – this process automatically deletes old files