---
title: "Determine if Printer is LAN or LPR – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Determine if Printer is LAN or LPR – Ag Internal."
long_description: "This document provides internal system administration information about Determine if Printer is LAN or LPR – Ag Internal."
---

Introduction 

 This article provides instruction for determining whether a printer is an LAN or LPR printer and why it is important for submitting effective support requests. 

  

 Access Printer in Work with Device Descriptions Screen 

 Whether the printer is an LAN or LPR may be included as part of its description in the Work with Device Descriptions screen.  

 Select AS/400 Command Line (System | AS/400 Command Line). 

 Type WRKDEVD *PRT and click OK . The Work with Device Descriptions screen displays and may include whether the printer is LAN or LPR in the Text box. 

 

 Sometimes, the information is not listed or the information that was entered may be wrong. 

  

 To Correctly Determine LAN/LPR Printer 

 Via Device Description screen 

 

 To objectively tell if a printer is LAN, type 5 in the Opt field for the printer and press Enter . The Display Device Description screen displays. 

 

 Page down 3 times. 

 

 If you see the IP address under the Remote location: line as shown above, then it is a LAN printer. 
 If you see the IP in the Text line at the bottom as shown below, then it is a LPR device. 

 

  

 Via the Work with All Output Queues screen 

 You can also determine whether a printer in LAN or LPR by looking at the printer description in the Work with All Output Queue. 

 Type WRKOUTQ in a command line and press Enter . 

 Note : To look at printers that start with a P, you can enter P* to the end of the command. 

 

 Type 8 in the Opt field for the device and press Enter . The Work with Output Queue Description screen displays. 

 

 Page down once. If you see an Internet Address line and an IP there as shown below, then it is LPR. 

 

  

 Why this Matters to Support 

 If a printer’s writer needs to be started again to get it working, then you need to know if the printer is a LAN or LPR to know what command to use. 

 If it is a LAN printer , use the command STRPRTWTR .  So, to start the writer for printer PE, run the STRPRTWTR PE command. 
 If it is a LPR printer , use the command STRRMTWTR .  So, to start the writer for printer P2 run the STRRMTWTR P2 command.