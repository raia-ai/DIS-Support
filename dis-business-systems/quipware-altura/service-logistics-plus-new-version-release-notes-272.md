---
title: "Service Logistics Plus - New Version Release Notes (2.7.2)"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Service Logistics Plus - New Version Release Notes (2.7.2)."
long_description: "This document provides information about Service Logistics Plus - New Version Release Notes (2.7.2) from the DIS Salesforce Knowledge Base."
---

Enhancements & Bug Fixes 

  

 Logout Issue / Additional Loggings 

 Resolved a persistent issue where technicians experienced unexpected logouts while using the application. The app will now attempt an automatic background re-login. If the server continues to return a 401 (Unauthorized) response, the app will proceed with a logout. Additional logging has been implemented in targeted areas to facilitate improved diagnostics and debugging, should issues arise. 

 Network Instrumentation Improvements  

 While network logging was already implemented, we have introduced further enhancements to capture more detailed statistics. These improvements will assist dealers and managers in identifying application-related details via Altura. 

 Image Viewer Compatibility Update 

 For iOS 18 the library which we were using for showing the images (enlarged view) was making problems for different technicians. We have updated the library and fixed the problem which will work on both old and new implementation. 

 Contacts disappearing from the work order 

 Customer was linking with invalid contacts due to the data in the work order. Technicians were reporting that when they open or complete a work order, sometimes contacts are not properly linking with customer, and it was causing issues in the work order detail screen. It is an edge case where sometimes data had problem while persisting. 

 Work order line notes disappearing during review process or work order status change 

 When a technician adds a notes order line in the Repair Work section, it works correctly the first time. However, if the technician reopens the workorder from the list to continue work and edit the added notes order lines, and then saves in repair work, during the review process, these notes order lines changes are overwritten by the application on change of workorder status/ on save changes in review process. 

 Instabug update for iOS 26 

 Instabug has reported that their library could cause crash on iOS 26. We have updated the library to support iOS 26 to avoid the crash in future.