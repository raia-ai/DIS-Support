---
title: "Change LPR Printer IP Address - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Change LPR Printer IP Address - Ag Internal."
long_description: "This document provides internal system administration information about Change LPR Printer IP Address - Ag Internal."
---

_Change LPR Printer IP Address - AG Internal_

Introduction 

 LPR printers differ from *LAN printers in several ways, but the major difference is where the IP address of the printer is stored on the AS/400. 

 The IP address of a *LAN printer is contained within the printer’s device description. 
 The IP address of an LPR printer is contained in the output queue assigned to the printer. 

   

 To Change LPR Printer IP Address 

 

 Open a command line (Alt + A), type WRKOUTQ , and click OK . The Work with All Output Queues screen displays. 

 

 The BY Printer is updated in this example. 

 Type ENDWTR BY in the Command line at the bottom of the screen and click Enter . 

 

 Highlight the BY printer and click the Change button. 

 

 Press the F9 key to show all values, then press page down. 

 

 Click inside the Internet address field, type the new IP address, and click Enter to save the changes. 

 Note : There is no need to restart the print writer, that occurs automatically when the device is updated. 

 

 Open a command line (Alt + A), type WRKDEVD *PRT , and click OK . The Work with Device Descriptions screen displays. 

 

 Highlight the printer and click the Change button. 

 

 Page down to Text Description on the last page and update the IP address. Click Enter to save the changes.