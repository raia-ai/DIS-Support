---
title: "Start, Display, Stop - Journals - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Start, Display, Stop - Journals - Ag Internal."
long_description: "This document provides internal system administration information about Start, Display, Stop - Journals - Ag Internal."
---

_Start, Display, Stop - Journals - Ag Internal_

Issue 

 There are time when we are troubleshooting an issue that we need to journal a file to learn more about the cause of a problem. 

 For example: The unit rental status is AV when it should be RE.  

  

 Solution 

 It's always a good idea to make a copy of the file you are journaling as a reference point of the data before the journal was started.  

  

 Steps to start journaling for a file to trap a problem. Example for WGI: 

 At a command line, enter each command string an press enter.  

  

 CRTLIB LIB(DISJOURN1) 
 CRTJRNRCV JRNRCV(DISJOURN1/WGI) 
 CRTJRN JRN(DISJOURN1/WGI) JRNRCV(DISJOURN1/WGI) 
 STRJRNPF FILE(FILEu/WGI) JRN(DISJOURN1/WGI) IMAGES(*BOTH) OMTJRNE(*OPNCLO)                                                                                            (**replace the 'u' in FILEu with the appropriate fileset letter) 

 To display the journal file 

 At a command line, enter the following command string by typing or pasting each line separately and press enter. 

 
 DSPJRN JRN(DISJOURN1/WGI) OUTPUT(*OUTFILE) OUTFILFMT(*TYPE2) 
 OUTFILE(QTEMP/RK1) ENTDTALEN(*CALC) 

  

 Then DSPPFM QTEMP/RK1 

  

 Note: If the journal has been running for a while and the data you see in the file is more current then you need you may need to modify the command to get older data from the journal.  

 DSPJRN JRN(DISJOURN1/WGI) RCVRNG(*CURCHAIN) OUTPUT(*OUTFILE) OUTFILFMT(*TY  

 PE2) OUTFILE(QTEMP/RK1) ENTDTALEN(*CALC)   

 
 To stop the journal 

 At a command line, enter the following command. 

 
 ENDJRNPF FILE(FILEu/WGI)                                                                                                                                                                                              (**replace the 'u' in FILEu with the appropriate fileset letter)  

 
 Then delete the DISJOURN1 library.