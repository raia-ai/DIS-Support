---
title: "Verify ECCService Host can Open SFTP Connection to Syncron – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Verify ECCService Host can Open SFTP Connection to Syncron – Ag Internal."
long_description: "This document provides internal system administration information about Verify ECCService Host can Open SFTP Connection to Syncron – Ag Internal."
---

The ECC service application is attempting to connect on port 22 using the SFTP protocol to host transfer.us.ints.syncroncloud.com 

 Use Powershell to test if the port is reachable. 

 Test-NetConnection -ComputerName transfer.us.ints.syncroncloud.com -Port 22 

  

 Use Putty to connect. 

 If a prompt is visible, the host can connect to the SFTP host. 

  

 If a black screen is produced, the host is unable to connect to the SFTP host. 

  

 Filezilla can be used to test the functionality of the .pfx file 
 Create a new site using host transfer.us.ints.syncroncloud.com and configure for key authentication using kubotaprod005 as the user and the .pfx key file. 

  

 C:\ProgramData\dis\im\data\syncronKubotaProd.pfx 

  

 The completed connection to synchron with key authentication should look like the following: 

  

 If the connection fails it appears as a timeout. 

  

 Hosts and ports to be added to a whitelist 

 34.239.232.179 100.24.143.118 

 transfer.us.ints.syncroncloud.com 

 SFTP Port 22