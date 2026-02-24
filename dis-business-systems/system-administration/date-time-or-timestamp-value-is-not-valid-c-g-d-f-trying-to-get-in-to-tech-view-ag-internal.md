---
title: "Date, Time or Timestamp value is not valid (C G D F) trying to get in to Tech View - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Date, Time or Timestamp value is not valid (C G D F) trying to get in to Tech View - Ag Internal."
long_description: "This document provides internal system administration information about Date, Time or Timestamp value is not valid (C G D F) trying to get in to Tech View - Ag Internal."
---

_Date, Time or Timestamp value is not valid (C G D F) trying to get in to Tech View - Ag Internal_

Issue 

 Tring to get in to Tech View and getting the following error 

   

  

 Solution 

 There is a date or time issue in the TCN file.  

 Use the DSPPFM TCN command and look for oddities in the date and/or time. 

 In this case, the line below with the red outline is missing the date and time. 

 Another scenario might be that the seconds are missing.   

 Note the TECH with the issue 

       

  

 Use UPDDTA TCN  

 put in the TECH and enter. 

 Either update the Date and/or Time or if appropriate remove the line.  

 If the seconds are missing, just edit the line to add the seconds. (01 would be a good choice) 

  

 Try Tech View again.  

  

  

 Here is an example of the missing seconds.