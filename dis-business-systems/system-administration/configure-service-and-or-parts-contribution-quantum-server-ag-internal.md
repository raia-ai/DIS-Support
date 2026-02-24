---
title: "Configure Service and/or Parts Contribution: Quantum Server - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Service and/or Parts Contribution: Quantum Server - Ag Internal."
long_description: "This document provides internal system administration information about Configure Service and/or Parts Contribution: Quantum Server - Ag Internal."
---

_Configure Service and/or Parts Contribution: Quantum Server - AG Internal_

If a dealer needs to be configured for Service and/or Parts Contribution, please send the dealer number (and Quantum IP address if available) to Jason Hack.  

 Note : once the dealer has been migrated, you can turn this feature off. (servicecontribution.migrate.accounts=false) 

 

 Use the Controller to load data 

 http://ip:8080/util-servlet-1.0.0/servicecontribution/glaccounts/{fileset}/{divisions} 

  

 See Configuring Service and/or Parts Contribution: AS/400  for AS/400 configuration instructions.