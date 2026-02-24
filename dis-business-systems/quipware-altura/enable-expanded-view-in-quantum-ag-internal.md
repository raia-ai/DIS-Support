---
title: "Enable Expanded View in Quantum - Ag Internal"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Enable Expanded View in Quantum - Ag Internal."
long_description: "This document provides information about Enable Expanded View in Quantum - Ag Internal from the DIS Salesforce Knowledge Base."
---

Introduction 

 This document describes the requirements for enabling Expanded View for a dealer.  Expanded view must be setup in Altura/MT first.  The information from this setup is needed to configure Quantum.  

  

 Requirements  

 On the License Manager, create the Expanded View user and API Key. 

 If you do not have a login to the License Manager, please open a ticket with the CloudOps team and request a login.  

 Use the keys provided in License Manager to populate the Quantum Util-Servlet keys.   

  

 Instructions 

   Access  License Manager . 

    

    Select Expanded View User from the left side of the screen. 

 

 Select the  Dealership , Company , and Default Branch (Division) .  The Default Branch is the main branch for the dealership.   
 Click Create . 

 

 The values in the API Key and User GUID fields display. The need to be used on the Quantum Util Servlet setup   

  

 Enable Expanded View – Quantum  

 To configure Quantum with the API-KEY and user id needed for the Expanded View, navigate to the Quantum deploy tool:  http://qdeploy.disdev.net/#/home . 

 

 Select  Setup Dealer Env for a Docker Stack . 

 

 Enter the dealer’s Enterprise Number in the top right corner and select the dealer from the Select Dealer drop down.  

 

 Click the Select Dealer Stack File drop-down and select the util-servlet stack . 

 

 

 Add the following two environment variables:   

 
 Name 

 
 Value 

 
 
 UTIL_SERVLET_EXPANDED_VIEW_API_KEY  

 
 API-KEY 

 
 
 UTIL_SERVLET_EXPANDED_VIEW_USER_KEY  

 
 user-id (likely a GUID) 

 
 

 Select Save . 
 Click Home in the Upper left corner of the screen. 

 

 Select Deploy Docker Stack for Dealer . 

 

 Important!   This restarts the dealer’s utilservlet. It should only be done after hours when the dealer is off the system.   

 Select the dealer utilservlet. 
 Select the stack file. 
 Click Deploy.