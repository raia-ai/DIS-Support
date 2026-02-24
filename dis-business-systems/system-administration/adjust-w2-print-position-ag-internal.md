---
title: "Adjust W2 Print Position - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Adjust W2 Print Position - Ag Internal."
long_description: "This document provides internal system administration information about Adjust W2 Print Position - Ag Internal."
---

_Adjust W2 Print Position - Ag Internal_

Issue 

 W2’s are printing too high (or too low) on the page. The most common issue is the form is printing 1 line too high. 


  

 Solution 

 Open a command line. 

   

 Type WRKDTAARA W2LSRADJ and click OK . The work with Data Areas screen opens. 

   

 Take option 5 to display the file. 

   

 Make a note of the ‘Value’ (typically it’s .000) and press F12 to exit. 

 Next, take option 2 to change the file. 

 To move the print down about one line on the page set the ‘Value’ to .100 and press enter. 

   

 If the print is too low on the page (an uncommon occurrence) decrease the value: 

 If the current value is .200, decrease it to .100 to move the text up 1 line. 

 If the current value is .000, decrease it to -.100 to move the text up 1 line.