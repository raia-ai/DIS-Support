---
title: "Load Laser Form Logos on Customer PC Via Logmein – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Load Laser Form Logos on Customer PC Via Logmein – AG Internal."
long_description: "This document provides internal system administration information about Load Laser Form Logos on Customer PC Via Logmein – AG Internal."
---

_Load Laser Form Logos on Customer PC Via Logmein – AG Internal_

Introduction 

 This article details how to load a Laser Form Logo created for a dealership to their system using Logmein. 

  

 To Load Laser Form Logos on Dealership PC 

 Connect to the customer’s PC using Logmein123.com. 

 Determine which logo image codes are currently being used by typing  WRFK LOGO* in a command line and clicking Enter . The Work with Files screen displays. 

 

 In the example above, LogoJ is the last file listed.  The new ‘batch’ of logos will begin with image code K . 

 Travis uses a process to create PCL versions of the logo files (supplied to him by the customer), and creates a file called UP.BAT similar to the following: 

 
 makeputcustpf.pl *.pcl keystone K > up.bat  (Where K is the beginning image code identified earlier) 

 Travis provides you the UP.BAT file and all the PCL files for the logos. 

 Copy those files into a folder on your PC, along with these two files: 

 
 EditV64.exe 
 putcustpfheadless.bat 

 Using Logmein’s remote file manager, create a temp directory on the customer’s PC (c:\temp) and transfer the following from your PC to the customer’s temp directory: 

 
 All the PCL files 
 up.bat 
 EditV64.exe 
 putcustpfheadless.bat 

 On the customer’s PC, go to the DOS prompt, run a cd\temp and execute go.bat. 

 Enter the SUPPORT username and password when prompted, then press Enter .  All the logos will be uploaded to the customers system. 

 Use WRKF LOGO* to verify the image codes loaded. 

  

 Print the Logos 

 Access Laser Forms to print the list of Logos. 

 Select a form type (Sales Order, Quote…) and click the Configure button. 

 Click the Logos button. 

 Click the Print Logos button. 

 Select a virtual printer (NP, VP, ZZ…) and set the Source to F (File). 

 Press Enter to generate the list of Logos and use Report Center to display the file.