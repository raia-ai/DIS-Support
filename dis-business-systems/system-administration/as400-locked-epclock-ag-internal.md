---
title: "AS400 Locked / EPCLOCK - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about AS400 Locked / EPCLOCK - Ag Internal."
long_description: "This document provides internal system administration information about AS400 Locked / EPCLOCK - Ag Internal."
---

_AS400 Locked / EPCLOCK - Ag Internal_

Issue :  

 AS400 Locked 

 This can result from failed backup, cancelling EOM jobs, etc. 

 Other applications that can be impacted by the presence of EPCLOCK data areas. 

 Management 360.          Symptom : Dashboard missing data. 
 Quantum Data Mine       Symptoms : No results or categories not displaying 
 POS Service Notes          Symptom : Reason code drop-down not responding. 
 Easy File                         Symptom : Documents not displaying 
 
 Sales360                        Symptom : Cannot display quote pdf.  Get blank page 

 Service360                        Symptom : Error Transmitting Work Order to Service 360 

  

 Solution: 

 1) WRKACTJOB command to check to see if the backup job has an error message needing a reply (Backup runs under the QCTL subsystem). This could be many things but most of the time it has to with someone getting signed on and into a program before the EOD jobs have run or completed. There are multiple error messages that could result from that. Note: It may be necessary to have someone from the software side take a look at the error to see what caused it before ending the job or answering the message. 

  

 2) Un-restrict ECM – RLSECM This will allow the interfaces to communicate and connect to the 400 again. 

  

 3) Check job for an IPL waiting – D J command will show the job queue status in the upper right hand corner. 

 Note: If the IPL is listed in the jobs there delete it prior to releasing the job queue.    

  

     

  

 4) Un-restrict the job queue – RLSJOBQ QBATCH command 

  

 5) Check for EPCLOCK data areas – WRKDTAARA EPCLOCK* 

 Delete any data areas that show up. EPCLOCKu will prevent part catalogs from connecting. EPCLOCK$, EPCLOCK#uU and EPCLOCK#uC data areas will prevent the 400 from sending data to the MT and the Quantum feeds from starting (aka - business system locked in the Quantum server jobs). We rarely see the EPCLOCK# data areas however. 

 The EPCKLOCKu data area gets created when the Backup and/or Parts EOM jobs run to prevent the catalogs from accessing the data files while the jobs are running. 
 The EPCLOCK$ data area gets created when backup runs and prevents the 400 from sending data to the MT and the Quantum feeds (Easy File and Report Center) 
 The EPCLOCK#uU data area gets created when a Units Reorgs runs. 
 The EPCLOCK#uC data area gets created when the Customer # rename/merge jobs run. 

     

  

  

 !!! DO NOT USE  the WRKOBJ EPCLOCK* command. 

 The WRKOBJ command will show you all objects, including the EPCLOCK programs that are needed for backups. If the programs are deleted it will cause the backup to error.