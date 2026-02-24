---
title: "Turn on Journaling for Time Clock U.SAM & TCD - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Turn on Journaling for Time Clock U.SAM & TCD - AG Internal."
long_description: "This document provides internal system administration information about Turn on Journaling for Time Clock U.SAM & TCD - AG Internal."
---

_Turn on Journaling for Time Clock U.SAM & TCD - AG Internal_

Introduction 

 These journals can help to diagnose and monitor issues with Time Clock and Point of Sale Tickets. 

 (This information would be used by our technical department.) 

                              

 Turn it On 

 Manually                                                                   

 1. Turn the TCLCKJRN opt 'on' using the following command X00081 TCLCKJRN,1 

 2. Ensure there are no locks on u.SAM & TCD for the file set that you want to start journaling using the following commands 

     PRJOBS SUSPEND  (This will pause the DISPRISM jobs) 

      WRKOBJLCK OBJ( u .SAM) OBJTYPE(*FILE)   (Where u = file set) End all jobs holding locks on the file

      WRKOBJLCK OBJ(TCD) OBJTYPE(*FILE)  End all jobs holding locks on the file 

  

 3. E nsure you are in the environment (ENV to file set) that you want to start journaling. Stop and restart the current TCD journal using the following commands     

     Type CALL ENDTCLKJRN PARM(‘ u ’) (Where u = file set) and press Enter . 

     Type CALL STRTCLKJRN PARM(‘ u ’) (Where u = file set) and press Enter .  

     PRJOBS RESUME (This command will restart the DISPRISM jobs) 

     

 OR 

  

 Automatically                                                              

 Turn the TCLCKJRN opt 'on'  using the following command X00081 TCLCKJRN,1                                                     

 Run POS End of Month.                                                      

  

 Turn it Off 

 Manually                                                                

 1. Turn the TCLCKJRN opt 'off' (X00081 TCLCKJRN,0). 

 2. Ensure there are no locks on u.SAM & TCD for the file set that you want to start journaling using the following commands 

     PRJOBS SUSPEND  (This will pause the DISPRISM jobs) 

      WRKOBJLCK OBJ( u .SAM) OBJTYPE(*FILE)   (Where u = file set) End all jobs holding locks on the file

      WRKOBJLCK OBJ(TCD) OBJTYPE(*FILE)  End all jobs holding locks on the file

  

 3. E nsure you are in the environment (ENV to file set) that you want to start journaling. Stop and restart the current TCD journal using the following commands   

     Type CALL ENDTCLKJRN PARM(‘ u ’) (Where u = file set) and press Enter . 

     PRJOBS RESUME (This command will restart the DISPRISM jobs) 

  

 OR 

  

 Automatically                                                            

 Turn the TCLCKJRN opt 'off' using the following command X00081 TCLCKJRN,0                       

 Run POS End of Month.      

                                              

 SC/400 solution record A03426 

 0……………