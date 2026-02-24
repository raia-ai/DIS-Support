---
title: "Troubleshooting Download Errors for IP Based Quantum Sites - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Troubleshooting Download Errors for IP Based Quantum Sites - Ag Internal."
long_description: "This document provides internal system administration information about Troubleshooting Download Errors for IP Based Quantum Sites - Ag Internal."
---

Introduction 

 Dealers who are set up as IP based quantum log into the business system through a URL with the format, “ http://xx.xx.xx.xx/webclient ” , where http leads to the browsers marking the website and its content as not secure. This can lead to errors when trying to download a document/report/etc from the system. To troubleshoot this, try the following: 

 

   

 

 

  

 Update Browser S ettings | Google Chrome 

 Click the 3 dots in the upper right corner and select Settings. 

 Click P rivacy and s ecurity from the menu on the left side of the screen. 

 Select Site Settin gs, scroll down, and expand Additional content settings . 

 Click Insecure content . 

 Click Add in front of Allowed to show insecure content and put in the Dealer’s IP for Quantum. 

 Uncheck current session only. 

  

  

 Update Browser settings | Microsoft Edge 

 Click the 3 dots in the upper right corner and select Settings . 

 Click Cookies and site permissions from the menu on the left side of the screen. 

 Click All permissions . 

 Scroll down and click Insecure content . 

 Click Add in front of Allow and put in the Dealer’s IP for Quantum 

  

  

 Browser settings | Extensions (Chrome) 

 Click the 3 dots in the upper right corner and select Settings. 

 Click Extensions on the left side of the screen. 

 Check if there is an anti-virus/content blocker/pop-up blocker extension installed. 

 Based on the dealer’s preference, we can either remove the extension or update the settings of it (which varies from extension to extension). Some extensions do now allow updating settings and use defaults for all.