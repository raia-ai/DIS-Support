---
title: "Green screen fake out - to get in to X51, X111, X112, X121, X122, X42 post Address expansion - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Green screen fake out - to get in to X51, X111, X112, X121, X122, X42 post Address expansion - Ag Internal."
long_description: "This document provides internal system administration information about Green screen fake out - to get in to X51, X111, X112, X121, X122, X42 post Address expansion - Ag Internal."
---

_Green screen fake out - to get in to X51, X111, X112, X121, X122, X42 post Address expansion - AG Internal_

In a mocha session, make sure your screen is set to a wider screen. 
 At the top of the screen click on Settings
 Select Termtype
 Select IBM-3477-FC   :  27*132 color display  and click ok. 
 Disconnect and reconnect
  
  
 To fake the system into thinking you are really in a Keystone session use this: 
 CALL X00072CL 
  
 To fake the system into thinking you are really using a Quantum session use this:
 CALL PGM(LSJOBSR) PARM('S' 'B') 
  
 --
 This option is only available when using a Keystone or Quantum session. 
 Press  <Enter> to return to the previous menu. 
  
  
 aka: Green screen hack