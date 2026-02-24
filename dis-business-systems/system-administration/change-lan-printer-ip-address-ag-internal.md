---
title: "Change *LAN Printer IP Address - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Change *LAN Printer IP Address - Ag Internal."
long_description: "This document provides internal system administration information about Change *LAN Printer IP Address - Ag Internal."
---

_Change *LAN Printer IP Address - AG Internal_

To Change *LAN Printer IP Address 

 

 Open a command line (Alt + A), type  WRKDEVD *PRT , and click  OK . The Work with Device Descriptions screen displays. 

 

 The JTEST printer is updated in this example. 

 Highlight the printer and click the Work with Status button. The Work with Configuration Status screen displays. 

 

 Note the current Status for the printer is ACTIVE/WRITER. The Print writer must be ended before any changes can be made. 

 Type ENDWTR JTEST in the Command line at the bottom of the screen and click Enter . 

 Press the F5 key to refresh the screen.  The Status should now be Varied On as shown below. 

 

 Highlight the printer and click the Vary off button. The status changes to Varied Off. 

 Click Enter to return to the Work with Device Descriptions screen: 

 

 Highlight the printer and click the Change button.  The Change Device screen displays. 

 Page down twice. 

 

 Change the IP address listed in the Remote Location field, then page down. 

 

 Change the Text Description to reflect the new IP address and click Enter to save the changes. 

 Highlight the printer and click the Work with Status button. 

 Highlight the printer and click the Vary on button. 

 Type STRPRTWTR JTEST in the command line at the bottom of the screen and click Enter to start the print writer.