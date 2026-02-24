---
title: "Dealership/User Locked Out of System for 9 Million Active Records - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Dealership/User Locked Out of System for 9 Million Active Records - Ag Internal."
long_description: "This document provides internal system administration information about Dealership/User Locked Out of System for 9 Million Active Records - Ag Internal."
---

_Dealership/User Locked Out of System for 9 Million Active Records - AG Internal_

Issue 

 A user receives a green-screen message stating they have too many (9 million) active records and need to contact DIS. They have been signed out/locked out of the system as a result. 

  

 Reason 

 Each time a user signs on, the system checks the number of active records used in each of the QS36F/u/IBM files which are stored in columns 2-8 of QS36F/u.IBM relative record 1. 

 If there are 9 million active records, they encounter the issue described above. The intention behind this is to resolve the issue and reclaim available space before the user reaches the serious/final limit of 10 million active records. 

  

 Solution 

 Unlock the user/Disable the 9 million check by completing the following steps: 

 Open a Command line ( Alt + A ). 

 

 Enter CRTDTAARA DTAARA , and click OK . The Create Data Area screen displays. 

 

 Enter *CHAR for the Type and 1 for the Length 

 Important! Ensure the user understands the importance of reclaiming space and the consequences if they do not.