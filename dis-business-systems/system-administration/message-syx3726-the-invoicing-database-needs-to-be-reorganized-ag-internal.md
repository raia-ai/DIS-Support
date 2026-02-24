---
title: "Message SYX3726 – The invoicing database needs to be reorganized - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Message SYX3726 – The invoicing database needs to be reorganized - Ag Internal."
long_description: "This document provides internal system administration information about Message SYX3726 – The invoicing database needs to be reorganized - Ag Internal."
---

_Message SYX3726 – The invoicing database needs to be reorganized - Ag Internal_

Issue 

 This message comes up when the u.SAM triggers are not attached.  It can display in Point of Sale (X5-1), Time Clock (X5B-1), Review By Technician (X5B-4) & Review By Work Order (X5B-5).   If the triggers are not attached then information will not go to the Document Ledger. This causes an auditing, specifically with CNH when they perform warranty audits. 

 These triggers could be missing because POS EOM is running or just missing for some other reason. 

  

 Solution 

 If you see the message above:        

 Check to see if POS EOM is running 

 If POS EOM is running you can check to see if there is a lock on u.SAM.  (other than the POS EOM job - i.e. Time Clock jobs) - if there is end the job(s) just be careful that you don't end the POS EOM job. The command to view if there are locks on u.SAM is: WRKOBJLCK OBJ(QS36F/u.SAM) OBJTYPE(*FILE). (Note ‘u’ = fileset)              

 If POS EOM is not on the user board, check to see if u.@5400 exists 

 You can run Security | Initial File Setup (X6-7) to reattach the triggers, but it’s much quicker to manually attach them with the following command: CALL ADDSAMTRG PARM(‘u’ ‘0000’) (Note ‘u’ = fileset) This must be done with a dedicated u.SAM file. Once it has completed you should check to be sure the triggers are attached by typing DSPFD u.SAM , then press enter.  If you search on the word "trigger" it will take you to that section of the screen and it should look like this.      

 Number of triggers :                3