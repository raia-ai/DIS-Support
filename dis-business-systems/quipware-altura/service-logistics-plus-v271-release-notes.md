---
title: "Service Logistics Plus -  V2.7.1 Release Notes"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Service Logistics Plus -  V2.7.1 Release Notes."
long_description: "This document provides information about Service Logistics Plus -  V2.7.1 Release Notes from the DIS Salesforce Knowledge Base."
---

Enhancements & Bug Fixes 

  

 Improved Image Handling in PDFs and Logs 

 Resolved an issue where cached images were incorrectly reused, causing duplicate or ambiguous images (e.g., checklists or equipment photos) to appear in PDFs during work order reviews. This fix ensures accurate and consistent image rendering for technician and customer documents in review process. 

 Reliable Customer Signature Persistence 

 Fixed a problem where customer signatures were occasionally missing from order segments during the batch review process. This issue, observed in version 2.7, caused certain work orders to become stuck in the verification stage. Signature linkage is now more stable and consistent. 

  

 User Activity and Network Monitoring Instrumentation 

 Introduced tracking for user activity and device network status across time intervals. This provides better visibility into usage patterns and helps diagnose connectivity-related issues. Future updates will expand this functionality for deeper diagnostics and performance insights. 

  

 Close-Out Day Dialog Logging 

 Added detailed logs to detect and analyze when the "Close-Out Day" dialog appears. Some technicians reported this dialog repeatedly interrupting workflow. Logging enables better investigation and resolution of this repetitive behavior. 

  

 Email Persistence Improvements 

 Enhanced email recipient data is saved during batch review. Previously, email recipients could be overwritten or lost due to incorrect handling, particularly in versions prior to 2.6.3. This fix ensures that customer emails are saved accurately and reliably. 

  

 Prevent Recursive Technician Clocking API Calls 

 Addressed an edge case where technicians working offline could trigger repeated clocking sync calls upon reconnecting. These recursive calls strained server resources. A new mechanism ensures sync operations are now performed in a controlled and efficient way. 

  

 Real-Time Customer Data Fetch on Work Order Screen 

 Customer recipient data now updates dynamically when a technician opens the work order detail screen. This ensures visibility of customer contact details as configured in Altura, improving communication accuracy and workflow reliability.