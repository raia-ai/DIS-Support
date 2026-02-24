---
title: "High Resource Usage | Multiple Session Issue - QW"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about High Resource Usage | Multiple Session Issue - QW."
long_description: "This document provides information about High Resource Usage | Multiple Session Issue - QW from the DIS Salesforce Knowledge Base."
---

_The executable QW_IS_RepCall.exe (referred to in Task Manager as “Quipware Executable File”) is being launched by various programs and fails to terminate properly. This leads to multiple instances running concurrently, which must be manually killed. The problem can become increasingly frequent—causing significant impact on user productivity and system resources.

Error Troubleshooting_

Problem 

 The executable QW_IS_RepCall.exe (referred to in Task Manager as “Quipware Executable File”) is being launched by various programs and fails to terminate properly. This leads to multiple instances running concurrently, which must be manually killed. The problem can become increasingly frequent—causing significant impact on user productivity and system resources.

 Scope of Impact 

 
 The issue appears specifically related to Parts operations.

 
 The executable hangs primarily during OE (Order Entry) invoice generation.

 
 Users can report no irregular actions—standard activities like invoicing, receiving, processing Direct Ships, or closing OE orders.

 Observed Symptoms 

 
 Multiple persistent QW_IS_RepCall.exe processes requiring manual termination.

 
 High system resource usage, especially during invoice generation.

 
 Frequent need to monitor and intervene via Task Manager (sometimes 8–10 hours/day).

 
 Use of “Print + Complete” and potential link to Direct Ships noted.

 
 Automated scripts deployed to kill long-running processes due to impracticality of manual intervention.

 
 No correlation to Billtrust PDF failure; resource issues persist independently.

 
 
 
 
 
  

  

 
 
 

  

  

 Troubleshooting Steps 

 
 Consultation with users and direct observation/confirmation of process hangs

 
 Printer registry cleaning to reduce potential printer entry bloat.

 
 Investigation of print spooler functionality and restart schedules.

 
 Review of Group Policy potential for printer creation and related warnings in Event Viewer.

 
 SQL Server review:

 
 Identified processes (e.g., ID 233 by user scover, ID 112 by user scyr) being blocked on the QuipWare server.

 
 Printer registry review:

 
 EXP: originally had 497 printers due to possible network RDP sessions; reduced to 67 after cleanup.

 
 Event logs repeat the same message; no UI/printer setup changes in ~1 year.

 
 Print spooler is restarted hourly on both terminals; spooler restart cycle in place since 04/22, but increase in issue frequency observed only in the past week.

 Solution 

 Root Cause of these persistent errors could caused by any one of the below issues. It is recommended to have documented policies & procedures in place for IT Team to review these on a regular cadence.

 
 Group Policy Review:

 
 Evaluate if Group Policy is auto-creating printers that contribute to registry bloat or process conflicts.

 
 Address any Group Policy-related warnings found in Event Viewer.

 
 Process/Resource Monitoring: monitor Task Manager and SQL activity for unusual or blocked processes, particularly under impacted user accounts.

 
 Printer Registry Maintenance | Provide End User Guidance

 
 Instruct all affected users to clear printers via QW Connect (Settings → Check Printer Reg option).

 
 Confirm if reducing printer entries improves process termination.

 
 Print Spooler: Although print spooler restarts do not align with the timing of the issue, continue to monitor for any potential influence.

 
 
  

 searchTags: High resource usage, troubleshooting, on-prem, AppHang81, QW_PO.exe, Error Number: 9, Error Source: Sti_printing