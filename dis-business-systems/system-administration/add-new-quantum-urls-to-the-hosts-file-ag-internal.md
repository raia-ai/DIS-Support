---
title: "Add new Quantum urls to the hosts file - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Add new Quantum urls to the hosts file - Ag Internal."
long_description: "This document provides internal system administration information about Add new Quantum urls to the hosts file - Ag Internal."
---

_How to add new Quantum urls to the hosts file - Ag Internal_

How to add new Quantum urls to the hosts file. 
  
 Introduction:
 Some customers have a different setup (QRA or Dealer IT changes) that makes it so you can not just copy and paste the url and gain access to their Quantum system as a DIS Support Rep. 
 You may find notes like the following in stafflink that indicates this is the case. 
 Dealer IT made changes that disabled Quantum connection if not using a Host file / VPN.  
 QRA Access is blocked. need a hosts file entry to access the server. 

 Solution: 
 Click the Windows icon in lower left corner.
 Start typing Notepad. When you see the Notepad App right click and click run as administrator.
 Click Yes to "Do you want to allow this app to make changes to you device?"
 Click File and choose Open.
 Click Windows(C:)
 Then Windows, System 32, drivers, etc
 Then change the file extension from Text Documents (*txt) to All files (*.*)
  
 Select hosts
 Add urls and notes about the customer they are for.
 Click File then Save.
    
  
 Here are examples of some of the customers that are in my hosts file.
 10.255.250.132 champlainvalley.dis.us
10.255.238.180 townlineequipment.dis.us
10.255.233.196 erbhenry.dis.us
10.255.251.212 mitchelltractor.dis.us
10.255.242.148 wichitatractor.dis.us
10.255.235.100 farmersimp.dis.us
10.255.252.221 lmtractor.dis.us
10.255.233.116 trieboldimplement.dis.us
10.255.238.164 northstarag.dis.us
10.1.144.19 stateequipment.dis.us
10.255.247.20 greinerimpco.dis.us
10.255.249.4 mountainfarm.dis.us
10.255.252.229 hodgemh.dis.us
10.255.254.13 thermokingofeasterncanada.dis.us
10.255.238.196 demotttractor.dis.us
10.255.232.100 jaycoximplement.dis.us
10.255.255.172 linkimplement.dis.us
10.255.242.180 keimfarm.dis.us
10.255.248.52 sandbergimp.dis.us
10.255.243.20 minnesotaag.dis.us
10.255.255.172 linkimplement.dis.us
10.255.245.180 ginopsales.dis.us
10.1.245.19 stateequipment.dis.us
10.255.246.212 odessatrading.dis.us
10.255.231.180 oxfordkubota.dis.us
10.255.246.164 amarillothermoking.dis.us
10.255.230.164 wallingford.dis.us
10.255.252.172 abellandson.dis.us
10.255.249.164 chwaltzsons.dis.us
10.255.228.228 cnypowersports.dis.us
10.255.229.148 fourmequip.dis.us
10.255.228.180 clbenningereq.dis.us
10.255.252.109 atlanticsupply.dis.us
10.255.252.164 genevaimplement.dis.us
10.255.227.68 beelertractor.dis.us
10.255.246.68 mpgtractor.dis.us
10.255.238.244 kubotathunderbay.dis.us
10.255.235.228 northwestforklift.dis.us
10.255.240.52 centraleqcomedford.dis.us
10.255.231.228 eastonsales.dis.us
10.255.240.116 mandsimplement.dis.us