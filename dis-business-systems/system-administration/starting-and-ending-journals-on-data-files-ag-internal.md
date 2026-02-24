---
title: "Starting and Ending Journals on Data files - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Starting and Ending Journals on Data files - Ag Internal."
long_description: "This document provides internal system administration information about Starting and Ending Journals on Data files - Ag Internal."
---

_Starting and Ending Journals on Data files - AG Internal_

There are times when there are issues on the system and journaling a file can help find who and what program are making the change to the data.
  
 Journals takes up space and continue to grow so it is important to keep a reminder ticket and reminder in Outlook to come back at a later date an remove the journal. 
  
 Steps to start journaling for a file to trap a problem. Sample for WGI:    
 
CRTLIB LIB(DISJOURN1)                                                      
CRTJRNRCV JRNRCV(DISJOURN1/WGI)                                            
CRTJRN JRN(DISJOURN1/WGI) JRNRCV(DISJOURN1/WGI)                            
STRJRNPF FILE(FILEu/WGI) JRN(DISJOURN1/WGI) IMAGES(*BOTH) OMTJRNE(*OPNCLO) 
 
 To display the journal file        
                                        
DSPJRN JRN(DISJOURN1/WGI) OUTPUT(*OUTFILE) OUTFILFMT(*TYPE2)               
OUTFILE(QTEMP/RK1) ENTDTALEN(*CALC)                                        
Then DSPPFM QTEMP/RK1                                                      
To stop the journal                                                        
ENDJRNPF FILE(Fileu/WGI)
                                                   
 Then delete the DISJOURN1 library.       **This requires a dedicated file. 
  
 ENDJRNPF FILE(Fileu/WGI)  JRN(DISJOURN1/WGI)        
Then delete the DISJOURN1 library.              
  
 From SC400 A03346