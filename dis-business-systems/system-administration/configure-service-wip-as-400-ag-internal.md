---
title: "Configure Service WIP: AS/400 - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Service WIP: AS/400 - Ag Internal."
long_description: "This document provides internal system administration information about Configure Service WIP: AS/400 - Ag Internal."
---

_Configure Service WIP: AS/400 - AG Internal_

Introduction 

 Set up for the Service WIP KPI will depend upon whether or not the dealer has been set up with Spectrum. When a dealer has already been set up for Spectrum, the configuration screen that controls which document types are set up, and what the labor threshold is set to is likely already set up. The following steps could be done before or after the Quantum server is configured for the Service WIP KPI, but please be aware that no figures will show in the KPI until that step is complete. 

 Note: When the request is sent to Network Services to configure the Quantum server for Service WIP, please make sure to include the file set(s) on which Service WIP should query.  

   

 Unlocking Service WIP 

 To unlock Service WIP, sign on as SUPPORT, then bring up a command line on the AS400 and type INSTALL_P2. You will be brought to the Receivables screen. If it is locked, press <F1> to move passed it (or click Cancel if on Keystone/Quantum). If it’s unlocked, press <F2> to move passed it (or click the Continue button if on Keystone/Quantum). 

 The next screen will be the Payables screen. If it’s locked, press <F1> to move passed it (or click Cancel if on Keystone/Quantum). If it’s unlocked, press <F2> to move passed it (or click the Continue button if on Keystone/Quantum). 

 The next screen will be the Service WIP screen. If it is locked, go onto SC/400 (D1D), type LOCK on a command line, and paste in the permanent key. Once unlocked, you will be able to configure the threshold and document types. 

   

 Setting the Threshold and Document Types 

 By default, the threshold is 14 days. You may type in a new interval, and click Enter to save. Each time a change has been made and Enter is pressed to save the changes, a message displays at the bottom of the screen that says, “Global settings updated.” 

 If the dealer has had Spectrum at one point, certain document types may already be configured for Service WIP. Because new document types may have been added in the business system since the last time the configuration was updated, it’s a good idea to go through the list of document types with the dealer to make sure the setting is what they want. Only W (work order type) documents may be configured in Service WIP. If you click the Add All button, all W type documents within all divisions under the current file set will be added to the configuration. Alternatively, you may click the Add button to set up each document type separately. On this screen, type in the division code and document code, and press Enter to save the changes. 

 If a document type needs to be deleted from the configuration, type 4 into the Opt field next to the document type, and press Enter. Click Enter on the confirmation screen (or click the Confirm button if in Keystone/Quantum). You may set up all divisions within the current file set on this screen. If a dealer has multiple file sets, you need to ENV to the other file set(s) and go through this install process again. 

   

 Setting the Timing and Completing Configuration 

 Service WIP is designed to run every two hours, indicated by the 120 (minutes) value set as a default in the Timing: Default interval field. Please leave this setting as is unless a dealer has specifically requested to have the job run on a lesser interval. If this value needs to be updated, type in a new value into the field, in minutes, and press Enter to save the changes. 

 The Last Date/Time field indicates the last date and time the Service WIP job was run. The Next Date and Next Time fields indicate the next date and time the Service WIP job will run. These values may be manipulated if you want the job to run sooner than the next date/time indicates. (Note: You can use the command DSPSYSVAL QTIME on a command line to see the current system time.) Input a new date and/or time and click Enter to save your changes. 

 When configuration is complete, press <F2> (or click Continue if on Keystone/Quantum) to move on. The last page, containing the Prism Server, User, Password, etc. should be left as is. Press <F2> (or click the Forward arrow/button if in Keystone/Quantum), and you will be brought to a master menu. Once INSTALL_P2 is complete, a checkbox for Service WIP will appear in the Security Maintenance settings for Management 360 set up.  

 See Configuring Service WIP: Quantum Server for Quantum server configuration instructions. 

 

 Configure Service WIP to Include 0$ Work Orders 

 Users may call in to configure Service WIP to include 0$ work orders using the WIPZERO option . Potential settings include: