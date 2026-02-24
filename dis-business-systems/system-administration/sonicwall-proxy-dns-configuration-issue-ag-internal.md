---
title: "SonicWALL Proxy DNS Configuration Issue – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about SonicWALL Proxy DNS Configuration Issue – AG Internal."
long_description: "This document provides internal system administration information about SonicWALL Proxy DNS Configuration Issue – AG Internal."
---

_SonicWALL Proxy DNS Configuration Issue – AG Internal_

Issue 

 Network issues occurring as a result of unique Proxy DNS configurations. 

   

 Solution 

 Click here to view an article from SonicWall if you plan on adding this configuration. 

 Do not select the Enforce DNS Proxy For all DNS Requests check box as this will push all DNS queries to the firewall. We only want the networks with access to the hosted business system to have the static DNS for LAN quantum remote access. 

 

 Only DNS should be the LAN or WLAN default gateway.