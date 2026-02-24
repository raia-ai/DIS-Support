---
title: "Opt to turn off 'Card Payment' and 'Cash Payment' entries in Receivables if they do not have My Account or MyPortal - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Opt to turn off 'Card Payment' and 'Cash Payment' entries in Receivables if they do not have My Account or MyPortal - Ag Internal."
long_description: "This document provides internal system administration information about Opt to turn off 'Card Payment' and 'Cash Payment' entries in Receivables if they do not have My Account or MyPortal - Ag Internal."
---

_Opt to turn off 'Card Payment' and 'Cash Payment' entries in Receivables if they do not have My Account or My Portal - Ag Internal_

As a part of the Prism or middle tier fields customers can get extra lines in Receivables for Cash tickets that are specified as just cash or credit card.  

 The idea was that customers with My Account or My Portal would have one place for their a customers to view all transactions online even if they didn't go to Receivables.  

 As more an more dealers are using add on products (Service 360, Altura, Kubota bundle, etc) the Prism/ Middle tier feed are getting turned on for more dealers so they can take advantage of these new offerings.  

  

 Some dealers have noticed this and prefer these extra transactions to not be created.   

  

 **It is very important the we make sure the customer does not have either My Account or My Portal prior to turn this opt off.** 

  

 CUST0347 future phone 0 Cash and Card payment transx in REA are included in X11-1 and statements 
       1 
 Cash and Card payment transx in REA are excluded in X11-1 and statements 

 
 

  

 Note: 

 X00081 CUST0347,1   will prevent new entries from being created.  It will not remove any entries that are already in the file.  

  

 Here is an example of what the transactions might look like with the opt setting 0 above.  The top 2 highlighted lines are auto created and merged as a part of the posting process.  

 In this case they were doing a Received on Account on a Cash ticket.  The bottom highlighted line is the regular line that would have posted no matter what.