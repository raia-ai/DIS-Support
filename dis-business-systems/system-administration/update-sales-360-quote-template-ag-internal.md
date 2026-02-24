---
title: "Update Sales 360 Quote Template - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Update Sales 360 Quote Template - Ag Internal."
long_description: "This document provides internal system administration information about Update Sales 360 Quote Template - Ag Internal."
---

_Update Sales 360 Quote Template - AG Internal_

Issue 

 The customer wants to add/change their logo or add an address to the header on their Sales 360 quote printouts. Any logo, image, or text to be added needs to be saved as a PNG file and then stored on the 400 IFS. 

   

  

 Solution 

 Create the PNG file by arranging the items as desired on a word document or similar program, then use the Snipping Tool to capture the image and save it as a PNG file. 

 Important! The file name MUST be location.png 

 Access the Dealer’s IFS \\400server\KEYSTONE\MyPictures\FilesetA\quotes\logos\divisionA. Note that the A in Fileset A is the actual file set and the A in division A is the division being changed. 

 Copy the updated PNG image into this file and replace the existing location.png file if there is already one there. 

 Note : Remember the file name HAS to be location.png for this to work and this only changes the header at the top of the document.