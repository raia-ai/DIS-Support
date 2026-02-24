---
title: "Convert a *LAN printer to a Virtual Printer - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Convert a *LAN printer to a Virtual Printer - AG Internal."
long_description: "This document provides internal system administration information about Convert a *LAN printer to a Virtual Printer - AG Internal."
---

_Convert a *LAN printer to a Virtual Printer - AG Internal_

Issue 

 A virtual printer was created as a *LAN device causing jobs that are sent to the virtual device to print on an actual printer. 

  

 Solution 

 Follow the instructions associated with each of the following steps to resolve the issue. 

 Note : In this document the original (incorrectly configured) virtual device is named ZZ, and the new temporary device will be called VP. 

 Note : If the ZZ output queue contains no files, you can simply delete ZZ and create a new virtual device of the same name instead of completing these instructions.  See the article titled Create Virtual Printer . 

  

 Create a temporary virtual device 

 Open a command line ( Alt + A ), type WRKDEVD *PRT, and click Enter / OK . 

 Press F6 to Create a new printer. The Create Device Description screen displays. 

   

 Type the name of the Virtual Printer (VP in this example) and click Enter / OK . Additional fields display. 

   

 Do the following: 

 Enter  *VRT  for the Device class 
 Enter  3812  for the Device type 
 Enter  1  for the Device model 

 Click  Enter / OK . Additional fields display. 

   

 Enter the number  11  in the Identifier field and click  Enter / OK . Additional fields display. 

   

 Click the down arrow to access the next screen. The Host Print transform field displays. 

 Click  OK . Additional fields display. Page down again using the down arrow. 

   

 Enter Virtual Printer for the description and click  OK  to save. 

  

 Move print jobs 

 In this step, the print jobs will be re-assigned from the original virtual devices output queue to the temporary virtual devices output queue created in the last step using report center. 

 Access the Report Center. 

   

 Set the filters to display ALL jobs for printer ZZ and click OK . 

    

 Highlight all the jobs listed under ZZ, then click the Move icon. Enter VP as the Move Output To printer and click OK . 

  

 Delete the original device/output queue 

 Open a command line ( Alt + A ), type WRKDEVD *PRT, and click Enter / OK . 

   

 Highlight the ZZ Device and click the Work with Status button. 

 If the device status displays as ACTIVE/WRITER, end the print writer by entering ENDWTR ZZ in a command line, and clicking OK . 

 Highlight the ZZ Device and click the Vary Off button. 

 Press enter to return to the Work with Device Descriptions screen. 

 Highlight the ZZ Device, click the Delete button and press enter on the Confirm screen. 

  

 Create a new virtual device 

 Repeat the first step and create a temporary virtual device named ZZ. 

  

 Move all jobs from the ‘temporary’ output queue to the ‘new’ virtual devices output queue 

 Repeat the process provided in the second step, this time moving all jobs from VP to ZZ in the report center. 

  

 Delete the temporary device / output queue 

 Open a command line ( Alt + A ), type WRKDEVD *PRT, and click Enter / OK . 

 Highlight the VP Device, click the Delete button, and press Enter on the Confirm screen.