---
title: "Lock and Key Instructions – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Lock and Key Instructions – Ag Internal."
long_description: "This document provides internal system administration information about Lock and Key Instructions – Ag Internal."
---

The lock and key isn’t always needed. If it is, you are presented with the screen below for whatever the product may be. 

 To use the lock and key method of activation of a product on the system you will initially see this for whatever product requires it. In this case barcoding. 

 

 As of version 23V2, You can type PFLOCK on any system to get the Lock & Key information. You must be logged on as either SUPPORT or QSECOFR. 

 

 Copy/paste the installation lock above. 

 

 Enter 

 Copy/paste the permanent key onto the customers server. That will activate the product. 

 

  

 Add a Product Key 

 Any new product that needs to be purchased will need a product key added. 

 On the customer server, again my example is on Mocha with a Vlink connection. Go to MENU X6 – Security and Configuration 

 Go into DIS Product Key Setup 

 Copy the DIS Group Code as in the example below. 

 

 Now you must go to the DIS system that generates the key. I’m using green screen on the server we call D1D (S1072D1D) The IP for that machine is 172.16.16.141. 

 Once you log in, type command GETPRD on the command line and hit enter. You will see this: 

 

 Copy in the group code from above.  It is different for every customer, the above is just an example. You will then need to type in the product code. An example would be “UPS” if you were installing the UPS interface. 

 You will be presented with a product key. Copy that into the product field on the customers server. In the bottom part of the screen hit F6 to add. 

 

 Make sure the product is present, if so, it has been added to their system.