---
title: "Display Printer OUTQ Messages to Troubleshoot Writer and Communication Issues - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Display Printer OUTQ Messages to Troubleshoot Writer and Communication Issues - Ag Internal."
long_description: "This document provides internal system administration information about Display Printer OUTQ Messages to Troubleshoot Writer and Communication Issues - Ag Internal."
---

From a Green Screen,  type WRKJOB <printer ID>.

  

 Enter a 1 for Option in the last message that has the status of OUTQ.

 

 Enter 4 to Work with spooled files.

  

 Enter 5 to display the JOBLOG.

  

 The diagnostic error message in this case was searchable on the Internet CPD337C

   https://www.ibm.com/support/pages/writer-hp-printer-ends-messae-cpd337c-andcpd337f 

  

 These were the steps that resolved the issue
 VRYCFG CFGOBJ(PrinterDeviceName) CFGTYPE(*DEV) STATUS(*OFF)
 CHGDEVPRT DEVD(PrinterDeviceName) USRDFNOPT(*IBMSHRCNN) SYSDRVPGM(*IBMSNMPDRV)
 VRYCFG CFGOBJ(PrinterDeviceName) CFGTYPE(*DEV) STATUS(*ON)
 STRPRTWTR DEV(PrinterDeviceName)