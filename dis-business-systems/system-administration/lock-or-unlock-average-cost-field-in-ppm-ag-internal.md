---
title: "Lock or Unlock Average Cost Field in PP&M - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Lock or Unlock Average Cost Field in PP&M - Ag Internal."
long_description: "This document provides internal system administration information about Lock or Unlock Average Cost Field in PP&M - Ag Internal."
---

_Lock or Unlock Average Cost Field in PP&M - AG Internal_

Issue 

 A parts manager complains because someone accidently wiped out the average cost amount set in PP&M or complains that they can’t change the average cost amount. 

 

 Solution 

 These hidden OPTs allow you to lock or unlock the Average Cost field. 

 Note : If someone enters the wrong receipt cost on a part the only way to correct it is to temporarily turn the opt off. 

 X00081 CUST0104,1 locks the field. With the opt set, the field is grayed out and can’t be selected. 
 X00081 CUST0104,0 unlocks the field. The field can now be selected and edited.