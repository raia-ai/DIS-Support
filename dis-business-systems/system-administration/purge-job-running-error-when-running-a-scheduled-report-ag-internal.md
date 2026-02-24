---
title: "Purge Job Running Error When Running a Scheduled Report - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Purge Job Running Error When Running a Scheduled Report - AG Internal."
long_description: "This document provides internal system administration information about Purge Job Running Error When Running a Scheduled Report - AG Internal."
---

_Purge Job Running Error When Running a Scheduled Report - AG Internal_

Issue 

 User receives a Purge job is running message when they try to run a Schedule report. 

  

 Solution 

 Open a command line, type  WRKF ut@@ni , click OK . 

 Locate temp file u t.@@ni (where  u = File Set) and delete it.