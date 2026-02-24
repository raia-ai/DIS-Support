---
title: "DISABLE ENABLE command for use during backup or dedicated procedure - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DISABLE ENABLE command for use during backup or dedicated procedure - Ag Internal."
long_description: "This document provides internal system administration information about DISABLE ENABLE command for use during backup or dedicated procedure - Ag Internal."
---

_DISABLE ENABLE command for use during backup or dedicated procedure - AG Internal_

DIS has utility commands that could be used to Disable user profiles prior to backup and then Enable them based on scheduled jobs on the AS400.
 (These are not widely used by our customers and has not been widely shared.) 
 The utility does not end jobs on the 400 but rather prevents a user from signing on. It is not related to backup but could be strategically planned to prevent Users from signing on
 during a specified period of time.  The job relies on the set up of the user profile to determine that it is a DIS software specific profile.  It does this by looking at the “Initial program to call” field on the
 User profile.  If is it set to “DISSIGNON” or “X5B000CL” then it will be considered for the Disable and Enable commands.  This brings up and important point that needs to be addresses prior to considering this option.
 When your dealership disables user profiles on the AS400 what is the procedure used? If it is to only mark the status of the User Profile as *DISABLED then work will need to be done to change existing Disabled user profiles to remove the DISSIGNON or X5B000CL designation.  From a command line type the following.  PRTUSRPRF TYPE(*PWDINFO) for a list of user profiles you can work from.
 DISSIGNON and X5B000CL designation in the Initial Program to call so we do not Enable profiles that were not intended to be used any longer with this new proposed method of Locking down the system.  This also means a process change in general when the dealership
 Disables user profiles in the future.  I have included a screen shot from the CHGUSRPRF screen for reference.
  
 
  
 The person/user profile that initiate the command or creates the scheduled jobs for the DISABLE and ENABLE process along with the SUPPORT user profile will be the only DIS profiles that will be able to sign on while the system is DISABLED.
 QSECOFR would also be able to signon since it does not contain the Initial program to call that would indicate that this is a DIS specific user.
  
 The idea is you would schedule the special Disable job a few minutes before backup is scheduled to start and then schedule the special Enable job
 At reasonable amount of time later to allow for the finishing of backup.  This can be variable based on size files and the differential IFS backup option.
                             
 _____________________________________________________________________________________________________________________________________________________________________________________________
  
 Reference: SC400 921597
 When run by a DIS user interactively:                                  
 DISUSERS ACTION(*DISABLE) or                                           
 DISUSERS ACTION(*ENABLE)                                               
 This command will check security (new security event defaulted to master
 security) and then either enable or disable all user profiles which    
 are assigned to DIS (initial program DISSIGNON or X5B000CL) except for    
 SUPPORT, QSECOFR, and the user profile that is running the command.       
 .                                                                         
 If the command is scheduled we also need two more parameters              
 so that the system can check security in the background.  Here is an      
 example of adding a job schedule entry to disable all DIS users           
 at 8:00PM:                                                                
   ADDJOBSCDE JOB(RESTRICT)                                                
              CMD(LIBRARY/DISUSERS ACTION(*DISABLE) BSET(T) BDIV(W))       
              FRQ(*WEEKLY) SCDDATE(*NONE) SCDDAY(*ALL) SCDTIME('20:00:00') 
              JOBQ(QSYSNOMAX) USER(BRYCE)                                  
 .                                                                         
 Explanation:                                                               
 JOB = Can be named anything that makes sense to the system operator       
 BSET = This is the file set that should be used to check security.  It does   
        not control which user profiles will be disabled/enabled.              
 BDIV = This is the division within the file set that should be used to        
        check security.  It does not control which user profiles will be       
        disabled/enabled.                                                      
 JOBQ = QSYSNOMAX is a good choice as it is multi-threaded and is not held     
        by backup.                                                             
 USER = This is the user that is used to check security.                       
 .                                                                              
 When scheduled, if the file set or the division is not supplied, or either    
 value is incorrect, then the job will end without actually enabling or        
 disabling anything.  In addition, if the user profile used on the scheduler   
 has not previously passed security, then the job also ends without enabling or
 disabling. 
 .                                                                      
 If something goes wrong and all of the profiles need to be manually    
 re-enabled:                                                            
 1) The user who ran the disable command should not be disabled so the  
    dealership could sign on with that profile to the DIS menu and then 
    run the command to re-enable the profiles.                          
 2) Or, QSECOFR could be used by the system operator to re-enable one of
    the DIS profiles.  That profile could then be used to sign on to the
    DIS menu and the command could then be run to re-enable the profiles.