---
title: "Purchase order batch - how to 'reclaim' entire posting date - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Purchase order batch - how to 'reclaim' entire posting date - Ag Internal."
long_description: "This document provides internal system administration information about Purchase order batch - how to 'reclaim' entire posting date - Ag Internal."
---

_Purchase order batch - how to "reclaim" entire posting date - Ag Internal_

Issue 

 Customer Cancelled POS batch containing Purchase orders or deleted Purchase order lines from a POS batch.  

 We do not have a reclaim option for purchase orders like we do with POS tickets.  

 Note:  

  

 Solution 

 1 ) Make a copy of BAA and BAM                                             
 2 ) DISSQL REQUEST('select distinct bapo# from baa where bapdat = yymmdd and  
 badiv = ''d'' order by bapo#') OUTPUT(*PRINT)      

  

 Change "yymmdd" to the actual posting date of the purchase orders that did not post. 

 Change "d" to the divisions of the purchase orders you are working with. 

  

 Note: If you get an error on this SQL run the following SQL's and then try again. 

 DISSQL REQUEST('update baa set bapdat = 0 where hex(bapdat) =  
 ''404040404040''')       

 - 

 DISSQL REQUEST('update bam set bmpdat = 0 where hex(bmpdat) = 
 ''404040404040''')   

 3 ) Review the report created in step 2 and confirm that this is the list of Purchase orders you would like to "reclaim".        

 4 ) DISSQL REQUEST('update baa set bapost = '' '' where badiv = ''d'' and  

       bapdat = yymmdd')    

 Change "yymmdd" to the actual posting date of the purchase orders that did not post. 

 Change "d" to the divisions of the purchase orders you are working with. 

  

 5 ) DISSQL REQUEST('update bam set bmpost = '' '' where bmpost = ''Y'' and   

     bmpdat = yymmdd and bmdiv = ''d''')       

 Change "yymmdd" to the actual posting date of the purchase orders that did not post. 

 Change "d" to the divisions of the purchase orders you are working with. 

                                          

 Important! Do not 'blank out' the BAPDAT or BMPDAT fields as it is not necessary & they could be used as a marker should you to nee change something. 

  

  

 from SC400 A03417