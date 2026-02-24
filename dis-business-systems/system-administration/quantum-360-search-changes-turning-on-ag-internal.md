---
title: "Quantum 360 Search - changes/turning on - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Quantum 360 Search - changes/turning on - Ag Internal."
long_description: "This document provides internal system administration information about Quantum 360 Search - changes/turning on - Ag Internal."
---

_Quantum 360 Search - changes/turning on - Ag Internal_

Quantum 360 Search changes 

 AKA Customer 360, Cust 360, C360, Solr Search 

 Note: The Solr sync was turned off on the Quantum server for all ASP/LPAR dealers in response to a situation where this caused Quantum to go down. 

 Note : This article deals with the Business System Side. Click here to view an article on Quantum Server Setup. 

  

  

 New in DIS_NR63 and above or 23V2 with JN01695 and above 

 The Solr Quantum search option is dependent on the CUST0345 OPT being turned on - X00081 CUST0345,1 

 If this is set mid-day the Quantum server will need a restart to pick up the OPT to turn on the Service on the Quantum server. Create a ticket for the Network group for this. 

  

 By default the CUST0345 opt will be turned off so the C360 screen looks like this. 

 

   

 With the opt on, it will look like this. 

 Notice the new verbiage showing when the last time the data was sync’d under the Quantum Search box - ‘Quantum Search data last indexed: 9/23/2021, 9:05:46 AM’ 

 

   

 If the OPT is on and it has message like this -   (Quantum Search data is not accessible at this time) 

 Network Services will need to take a look at the set up on the Quantum server 

  

 

   

 If you want to resync/reindex the data, 

 Go to Security | Security Maintenance 

 Go through the security gate. 

 On the Division Code screen, enter your master security code.  Usually @ and press enter. 

 Click on User Authority & Quantum 

 On the top right click on Quantum Admin 

 Click Solr on the Left 

 Note: If you get a message like this Network Services will need to check the Quantum server 

 

 Click Start Solr Sync button 

 

 Screen will look like this while the sync is running.  

 Click Refresh Solr Sync Status button 

 

 Click Refresh Solr Syn Status 

 When done it will look like this. Notice the top line shows Indexing completed and the number of Added/Updated documents. Also, any Deleted documents. 

 

 Close Quantum Admin tab in your browser 

 Exit Security Maintenance by clicking enter and then click Exit. 

 Go back to Cust 360 to see the new updated indexed date and time.