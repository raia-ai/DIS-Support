---
title: "Database needs to be reorganized Error code Indicators - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Database needs to be reorganized Error code Indicators - Ag Internal."
long_description: "This document provides internal system administration information about Database needs to be reorganized Error code Indicators - Ag Internal."
---

_Database needs to be reorganized Error code Indicators - AG Internal_

New indicators were added to the various “database needs to be reorganized” messages in release NR94. This document outlines the various messages and resolution steps to take for each. 
  
 Error code E001 = SAM triggers not attached
 
 Resolution:
 Check to see if POS EOM is running and needs to complete. Check for EOM @ temp files before determining next steps.
 If EOM is not running check to make sure all SAM logical files exist. Use the DSPDBR u.SAM command (you will want to check it against another system that is on the same version of the software as the customer). If any of the logical files are missing run X67, this will create the logical files and attach the triggers.
 If EOM is not running and SAM logical files exist you can quickly attach triggers using this command CALL ADDSAMTRG PARM(‘u’ ‘0000’)  with dedicated access to SAM (NOTE: ‘u’ = file set value) - use the WRKOBJLCK OBJ(u.SAM) OBJTYPE(*FILE) command to check  for locks before running the command to attach triggers.

  
  
 Error code E002 = Parts log journals not attached
 
 Resolution
 Check to see if EOD or EOM is running and needs to complete. Check EOM @ temp files before determining next steps.
 If EOD or EOM are not running check to make sure IAM and IBM logical files exist using the DSPDBR IAM and DSPDBR u.IBM commands. If not, run X67.
 Manually attach the journals using this command CALL STRDISJRN PARM(‘u’ ‘ALL’) 

 with dedicated access to the files (NOTE: ‘u’ = file set value) – use the WRKOBJLCK OBJ(u.IBM) OBJTYPE(*FILE) command to check for locks before running the command.
 Use the DSPFD IAM and/or DSPFD u.IBM and/or DSPFD PARPOS command to check to see if the journals are attached. Page down util you see the ‘ File is currently journaled attribute ’.

 
  
  
 Error code E003 = there is an IBM file that has over 9 million records. This one prevents any user from signing on to the system until corrective action is taken by the RL. This is a new message as of NR91 .
 
 Resolution:
 Sign on using a Mocha session as Support without calling the DISSIGNON program

 
  
 From the command line create the data area to bypass the check at sign on using the command below. This will allow users to sign on.

 CRTDTAARA DTAARA(DISSYSOBJ/X0CLBALI36) TYPE(*CHAR) LEN(1) 
   
 WRKF QS36F/*ALL to find all u.IBM files on the system then display the file description to find the file that has over 9 million records. The customer will need to run Part Phase Outs for the file set and then Parts EOM to remove part records. After this has been done and u.IBM has less than 9 million records we should delete the data area created in step 2 using the command

 DLTDTAARA DISSYSOBJ/X0CLBALI36 
  
  
 Error code E004 = IBM triggers are not attached. This is a new message as of NR94 to prevent problems with the Parts Subledger data.
 
 Resolution
 Check to see if Parts EOM is running and needs to complete. Check for EOM @ temp files before determing next steps.
 Check to see if IBM logical files exist using the DSPDBR u.IBM and/or DSPDBR IAM command, IBM should have 2 logical files and IAM should have 6 logical files. If not, run X67 to create logical files and attach triggers.
 If EOM is not running and logical files exist you can attach triggers manually using these commands (NOTE: ‘u’ = file set value) CALL ADDIBMTRG PARM(‘u’ ‘0000’) and CALL ADDIAMTRG PARM(‘u’ ‘0000’)   with dedicated file access – use the WRKOBJLCK OBJ(u.IBM) OBJTYPE(*FILE) or WRKOBJLCK OBJ(IAM) OBJTYPE(*FILE) command to check for locks before running the command to attach the triggers - or run Parts EOM.