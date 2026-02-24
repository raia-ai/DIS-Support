---
title: "Stop Middle tier feeds - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Stop Middle tier feeds - Ag Internal."
long_description: "This document provides internal system administration information about Stop Middle tier feeds - Ag Internal."
---

_How to stop Middle tier feeds - Ag Internal_

If you want the XML jobs to run but just hold the uploads.
 Type: WRKACTJOB SBS(DISPRISM) enter and then put a 3 beside the QARWEBUPL job and press enter. 
  
 When you are ready to release it. Use the same instructions above but use a 6 instead to release. 
  
 If you want to shut the middle tier feeds down and prevent them from running. 
 Type: PRJOBS SUSPEND and press enter. 
  
 To start them back up.
 Type: PRJOBS RESUME and press enter.