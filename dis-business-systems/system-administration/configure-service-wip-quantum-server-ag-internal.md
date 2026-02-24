---
title: "Configure Service WIP: Quantum Server - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Service WIP: Quantum Server - Ag Internal."
long_description: "This document provides internal system administration information about Configure Service WIP: Quantum Server - Ag Internal."
---

_Configure Service WIP: Quantum Server - AG Internal_

A script has been created that will: 
 Create the /srv/config folder on the Quantum server if it does not yet exist 
 Create the util.properties file in the above folder if it does not yet exist 
 Add an entry in the util.properties file for the Service WIP job 
 Add an entry in the util.properties file for the fileset(s) on which Service WIP should query . 

 Note: Before beginning, make sure you have been given the fileset(s) on which Service WIP should query.  
   
 Save the attached add_property.bash file into the /home/access folder on the dealer's Quantum server.  
 Open a session in PuTTY on the dealer's Quantum server.  
 Switch user to root.  
 Paste in the following command: chmod +x /home/access/add_property.bash 
 Paste in the following command: /home/access/add_property.bash 
 You will be asked, "What Service_WIP Filesets should be active? Enter with no spaces?" Type in the fileset(s) on which Service WIP should query, and press Enter.  
 You will be asked, "Confirm Limiting Service_WIP filesets to fileset(s) f? (where f = fileset(s) entered). Type Y and press Enter. 

 
 The contents of the util.properties file will display. Ensure the enableCron.servicewip entry is set to true, and the as400.servicewip.filesets value has the correct fileset(s) for the dealership.  
 Reboot the Quantum server for the changes to take effect.  

  
 See Configuring Service WIP: AS/400 for AS/400 configuration instructions.