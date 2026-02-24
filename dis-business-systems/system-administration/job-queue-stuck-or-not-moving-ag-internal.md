---
title: "Job Queue stuck or not moving - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Job Queue stuck or not moving - Ag Internal."
long_description: "This document provides internal system administration information about Job Queue stuck or not moving - Ag Internal."
---

_Job Queue stuck or not moving - AG Internal_

SC400 Solution A02678 

 In order for jobs to come off the job queue, the status needs to be RLS/SBS.  
Remember some times it only appears that the job queue is stopped because     
there is a big "evoked" job (like create suggested order or DOC) that runs for
a long time since only one evoked job can typically run at once.      

        
1.  Check the user board for evoked jobs or ones with a stays of MSG Wait.   

 
2.  WRKJOB *ALL enter                                                         
    Look for QBATCH and QS36EVOKE make sure they have a status of RLS.        
    If status is held use opt 6 to release.                                   
    If status is stopped, at the cmd line type:                               
    STRSBS QBATCH enter      

                                                 
3.  Make sure these same two subsystems have the correct number of active jobs
    For QBATCH type CHGJOBQE (F4) fill in as follows:                         
 Subsystem description  . . . . .   qbatch        Name                        
   Library  . . . . . . . . . . .     *LIBL       Name, *LIBL, *CURLIB        
 Job queue  . . . . . . . . . . .   qbatch        Name                        
   Library  . . . . . . . . . . .     *LIBL       Name, *LIBL, *CURLIB        

   Maximum active jobs  . . . . . .   1             0-1000, *SAME, *NOMAX    
  Sequence number  . . . . . . . .   *SAME         1-9999, *SAME            
  Max active priority 1  . . . . .   1             0-99, *SAME, *NOMAX      
  Max active priority 2  . . . . .   1             0-99, *SAME, *NOMAX      
  Max active priority 3  . . . . .   1             0-99, *SAME, *NOMAX      
  Max active priority 4  . . . . .   1             0-99, *SAME, *NOMAX      
  Max active priority 5  . . . . .   1             0-99, *SAME, *NOMAX      
  Max active priority 6  . . . . .   1             0-99, *SAME, *NOMAX      
  Max active priority 7  . . . . .   1             0-99, *SAME, *NOMAX      
  Max active priority 8  . . . . .   1             0-99, *SAME, *NOMAX      
  Max active priority 9  . . . . .   1             0-99, *SAME, *NOMAX      

 
 4.  For QS36EVOKE type CHGJOBQE (F4) fill in as follows:                   
 Subsystem description  . . . . . > QBATCH        Name                      
   Library  . . . . . . . . . . .     *LIBL       Name, *LIBL, *CURLIB      
 Job queue  . . . . . . . . . . . > QS36EVOKE     Name                      

    Library  . . . . . . . . . . .     *LIBL       Name, *LIBL, *CURLIB   
 Maximum active jobs  . . . . . . > *nomax        0-1000, *SAME, *NOMAX  
 Sequence number  . . . . . . . .   *SAME         1-9999, *SAME          
 Max active priority 1  . . . . . > *nomax        0-99, *SAME, *NOMAX    
 Max active priority 2  . . . . . > *nomax        0-99, *SAME, *NOMAX    
 Max active priority 3  . . . . . > *nomax        0-99, *SAME, *NOMAX    
 Max active priority 4  . . . . . > *nomax        0-99, *SAME, *NOMAX    
 Max active priority 5  . . . . . > *nomax        0-99, *SAME, *NOMAX    
 Max active priority 6  . . . . . > *nomax        0-99, *SAME, *NOMAX    
 Max active priority 7  . . . . . > *nomax        0-99, *SAME, *NOMAX    
 Max active priority 8  . . . . . > *nomax        0-99, *SAME, *NOMAX    
 Max active priority 9  . . . . . > *nomax        0-99, *SAME, *NOMAX    

  

 SC400 Solution A00298 

 FROM THE JOBQ STATUS SCREEN (D J), TAKE A CMD21 (SUBSYSTEM) TO WORK WITH      
SUBSYSTEM DESCRIPTIONS.  TAKE OPTION 5 (DISPLAY) FOR 'QBATCH'. THEN TAKE      
TAKE OPTION 6 (JOB QUEUE ENTRIES) TO VIEW MAX ACTIVE - MAX ACTIVE FOR QBATCH  
SHOULD HAVE '1' IN ALL COLUMNS, IF NOT, USE 'CHGJOBQE' TO CHANGE.             
  SUBSYSTEM DESCRIPTION = QBATCH                                              
    LIBRARY             = QSYS                                                
  JOB QUEUE             = QBATCH                                              
    LIBRARY             = QGPL                                                
THEN SET MAX ACTIVE JOBS & MAX ACTIVE PRIORITY FOR ALL LEVELS TO '1'          
(or can set Priority levels on 1 thru 9 to *NOMAX)                            
******                                                                       

  

 Solution A01028 for other type of jobq problems .  

 Refer to solution #'s A00298 & A00917 first for regular job queue problems.
Type WRKJOBQ <e>                                                           
Place cursor next to the QBATCH subsystem & type a 6 to release it.        
Jobs should now be coming off.                                             
This could be caused by the new delayed backup not completing successfully. 
********                                                                   
Can also use: RLSJOBQ QBATCH <e>   (does same thing, faster to do!)