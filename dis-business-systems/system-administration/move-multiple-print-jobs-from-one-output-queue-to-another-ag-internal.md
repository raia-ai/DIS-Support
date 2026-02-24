---
title: "Move Multiple Print Jobs from One Output Queue to Another - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Move Multiple Print Jobs from One Output Queue to Another - Ag Internal."
long_description: "This document provides internal system administration information about Move Multiple Print Jobs from One Output Queue to Another - Ag Internal."
---

_Move Multiple Print Jobs from One Output Queue to Another - AG Internal_

Issue 

 A printer needs to be deleted and recreated but there are print jobs spooled to the existing printer name.  The following steps will allow the jobs to be moved, using one command, from one output queue to another. 

  

 Notes : 

 This works best from a green screen session. 
 Know which output queue into which you’re going to move the print jobs. For this example the queue to be used is SUPPORT. 

  

 Type WRKOUTQ and press enter. 
 Locate the output queue (the same name as the printer to be deleted). Take option 5, Work With and press enter. 
 Type a ‘2’ next to all the jobs in the queue. 
 Tab to the command line and type: 

 OUTQ(SUPPORT) and press enter 

 All the jobs in the existing output queue will be moved to the SUPPORT output queue. 

 Delete the old printer (which also deletes the output queue) and recreate the printer. 

 Use the same process to move the jobs from the SUPPORT output queue to the new printer name.