---
title: "NOSHORTM Hidden OPT - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about NOSHORTM Hidden OPT - Ag Internal."
long_description: "This document provides internal system administration information about NOSHORTM Hidden OPT - Ag Internal."
---

_NOSHORTM Hidden OPT - AG Internal_

Introduction 

 NOSHORTM is a hidden OPT that controls whether the Short Model is automatically generated. 

 X00081 NOSHORTM,0 - Short Model is not automatically generated when adding a new model. 
 X00081 NOSHORTM,1 - Short Model is automatically generated when adding a new model. 

 This article details how the Short Model name is determined if the OPT is set. 

  

 How the Short Model is Generated 

 If the Long Model is less than or equal to 9 characters, it will use the Long Model as the Short Model (NW- MS70D in the example below). 

 

 If the Long Model is 10 or longer (to 16), then the first 9 characters of the Long Model are used (MZ-E40263 in the example below). 

 

 If that Short Model is already in use, then the last character of the Short Model is replaced with a number. The first number will be one and increment by one, replacing characters from right to left as necessary until an un-used Short Model is found (MZ-E40261 in the example below, providing that Short Model does not already exist - if that Short Model is already in use, then MZ-E40261 is used). 

 

 The automatically generated described in the examples above are shown below.