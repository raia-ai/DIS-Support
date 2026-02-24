---
title: "Login Process for SonicWALL with Multi-Factor Authentication – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Login Process for SonicWALL with Multi-Factor Authentication – AG Internal."
long_description: "This document provides internal system administration information about Login Process for SonicWALL with Multi-Factor Authentication – AG Internal."
---

_Login Process for SonicWALL with Multi-Factor Authentication – AG Internal_

To Login 

 Enter the login credentials for SonicWALL. 

 

 Click LOG IN. A screen displays prompting for a security code. 

 Follow the instructions to download an app and scan the QR code. 

 

 After the QR code is scanned you will get a code in the app. 

 Enter the code into the input box and click OK . 

 The next screen gives you a scratch code that should be saved, and the ability to unbind the TOTP key. 

 IMPORTANT! YOU MUST UNBIND THE KEY HERE, OR THIS WILL LOCK THE SONICWALL LOGIN TO THE MOBILE DEVICE THAT WAS USED. 

 

 Click UNBIND TOTP KEY . A popup message with the status of the request displays. 

 

 Click OK . 

 Once the TOTP key has been unbound you can login to the SonicWALL. 

 

 Select Click here to continue... .