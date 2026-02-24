---
title: "Error - Keystone failed to recognize you File Set and your Division. Please log off and log back in. - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Error - Keystone failed to recognize you File Set and your Division. Please log off and log back in. - Ag Internal."
long_description: "This document provides internal system administration information about Error - Keystone failed to recognize you File Set and your Division. Please log off and log back in. - Ag Internal."
---

_Error - Keystone failed to recognize you File Set and your Division. Please log off and log back in. - Ag Internal_

A quick way to resolve “Keystone failed to recognize your File Set...” message remotely  
 Introduction 
 User is getting the message, “Keystone failed to recognize your File Set and your Division. Please log off and log back in.”  This is typically because the user has used the ENV command and entered the division code in the company file group field. 
 
  
 Resolution: 
 A quick way to resolve the issue is to delete the username file from the QS36F library with the AS/400 command dltf qs36f/ username . 
 
  
  
 Have the user sign on again and they will be prompted to enter their company file group and division again.