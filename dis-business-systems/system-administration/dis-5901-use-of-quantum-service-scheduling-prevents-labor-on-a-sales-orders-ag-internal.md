---
title: "DIS-5901 Use of Quantum Service Scheduling prevents labor on a sales orders - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DIS-5901 Use of Quantum Service Scheduling prevents labor on a sales orders - Ag Internal."
long_description: "This document provides internal system administration information about DIS-5901 Use of Quantum Service Scheduling prevents labor on a sales orders - Ag Internal."
---

_DIS-5901 Use of Quantum Service Scheduling prevents labor on a sales orders - Ag Internal_

Issue 

 Getting an error DIS-5901 Use of Quantum Service Scheduling prevents labor on a sales orders when trying to add labor to a document. 

  

 Solution 

 This error comes up when Service Scheduling is turned on and you are trying to add labor to a document type that is formatted as a Sales Order. What you will need to do is use an actual work order format Document type or you can go to POS|TABLE MAINTENANCE|DOCUMENT CLASSIFICATION and pull up that document type and change the format to Work Order and then continue to use this document type to add labor. Note: Prior to changing the Document Classification code, make sure the Document type is not used for Rentals. Changing documents types on tickets produced by periodic billing should not be changed as it can cause errors if the prior format and current format do not match.   You will also need to go into SECURITY|LASER FORMS CONFIGURATION and then enable the document type that will now be under the Work Order category so that it will print like you expect.