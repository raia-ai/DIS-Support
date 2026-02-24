---
title: "Logos in Sales 360 - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Logos in Sales 360 - AG Internal."
long_description: "This document provides internal system administration information about Logos in Sales 360 - AG Internal."
---

Introduction 

 This article details logo placement on quotes in Sales 360. 

 When a user generates a quote in Sales 360 and clicks the PDF button located in the upper right-hand corner, the system displays the quote output along with the dealer’s logo at the top of the document. This logo is controlled by a specific image file stored within each client’s IFS folder structure. 

 

 This guide explains: 

 Where the quote logo comes from? 
 How dealers can update their own logo? 
 Why some quotes show more white space than others? 
 Recommended file size and image format 

 Where the Quote Logo Comes From 

 Sales 360 retrieves the quote header logo from a PNG file stored in the client’s \Keystone directory. 

 Although the initial portions of the file path (IP address, file set folder, or division folder) may differ between clients, the structure is generally similar. 

 

 Required File Name 

 The logo file must be named: 

 location.png 

 Sales 360 will only recognize the image if it uses this exact name. 

 Example 

 Clients typically find the file in an IFS folder like: 

 \\<Server or IP>\<FileSet>\IFS\<Division>\img\location.png 

 How Dealers Can Update their Own Logo 

 Dealers can update their logo themselves if they have access to the IFS folder and understand how to replace image files. 

 To Change the Logo: 

 Create or edit a PNG file using the required name: location.png. 
 Replace the existing file in the appropriate IFS folder. 

 Ensure that the image dimensions meet recommended guidelines (see Section Recommended File Size and Image Format ) 

 Why Some Quotes Show More White Space than Others 

 Users may notice that some Sales 360 quotes display more white space at the top. 

 This variation is caused by the pixel size (dimensions) of the logo file being used by each dealer. Changing the size of the logo only affects how high up that colored line with the date at the top gets pushed. 

 Larger logo image = less white space at the top of the PDF quote 
 Smaller logo image = more white space at the top 

 Example 

 Mason Machinery uses a larger logo thus there is minimal top white space. 

 

 Peak uses a smaller logo thus there is more top white space. 

 

 Recommended File Size and Image Format 

 To maintain consistent formatting and avoid excessive white space, the maximum recommended size for the logo is 1324 x 357 pixels. 

 How to Check the Logo’s Pixel Size 

 To verify the pixel dimensions of the existing logo: 

 Open location.png using the standard Photos application in Windows. 
 Look at the bottom-left corner of the window. 
 The pixel size (e.g., 1324 × 357) will appear there.