---
title: "Add Cross reference to Kubota parts with out the dash to be used for UPC barcode readers - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Add Cross reference to Kubota parts with out the dash to be used for UPC barcode readers - AG Internal."
long_description: "This document provides internal system administration information about Add Cross reference to Kubota parts with out the dash to be used for UPC barcode readers - AG Internal."
---

_How to add Cross reference to Kubota parts with out the dash to be used for UPC barcode readers - AG Internal_

UPC codes wrong on Kubota parts, needs to update them.  - bar code scanners
 ***This should be added to the checklist of setting up bar code scanning, If the dealership is a Kubota dealer this should be done at the time of install so they do not have to call later saying it doesn’t work***
  
 Parts from Kubota come with a UPC barcode on them but they do not include the dash in them like the price book has. We have a utility job that we can set up to add the part numbers without the dash into the cross reference on the part.
  
 We'll need to set up a scheduled job like this 
   
 Job name . . . . . . . . . . . . > KUBXREF       Name                  
Command to run . . . . . . . . .   STRS36PRC PRC(KUBXRF) CURLIB(LIBRARY)
PARM('KUB,BATCH')                      
  
 Go to wrkjobscde entry – select add
 **Make sure the job name and the vendor code matches the users vendor code**
 Once this is scheduled enter this command on the command line as well to “run immediately.”
  
 ***Make sure the Schedule Time is run prior to the backup job starting***