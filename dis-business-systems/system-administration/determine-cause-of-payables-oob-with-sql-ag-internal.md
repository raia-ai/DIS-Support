---
title: "Determine Cause of Payables OOB with SQL - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Determine Cause of Payables OOB with SQL - Ag Internal."
long_description: "This document provides internal system administration information about Determine Cause of Payables OOB with SQL - Ag Internal."
---

This article provides a way to hone in on the cause of an OOB. 

  

 Is the History for the payables account OOB? 

 (The following SQL provides a 1 line total for the history on the specific GL account.) 

 === > DISSQL REQUEST('select Sum(PAAAMT) from paa where paaact = ''C2100000'' and paasta = ''H''')                        

 If yes, what address or addresses add up to that amount?   

 (The following SQL will give you a 1 line history total for each vendor with transactions for this GL account. Note all addresses that are not 0 and their total.  The totals for all not zero line will add up to the total in set 1 above.)    

 ===> DISSQL REQUEST('select PAAADR, Sum(PAAAMT) from paa where paaact = ''C2100000'' and paasta = ''H'' GROUP BY PAAADR')                                      

  

 Once we know an address or addresses run the following for each address number. 

 This SQL will hone in on which merge month is OOB for this address. 

 ===> DISSQL REQUEST('select PAAMFU, Sum(PAAAMT) from paa where paaact = ''C2100000'' and paasta = ''H'' AND PAAADR = ''BUE001'' GROUP BY PAAMFU')    

 From the merge month, can hone in on the Check number that OOB. 

 ===> DISSQL REQUEST('select PAACHK, Sum(PAAAMT) from paa where paaact = ''C2100000'' and paasta = ''H'' AND PAAADR = ''BUE001'' AND PAAMFU = ''202403’’ GROUP BY PAACHK')               

 Next, all list of transactions to figure out which transaction is the amount you are looking for to bring back to current.  

 ===> DISSQL REQUEST('select * from paa where paaact = ''C2100000'' and paasta = ''H'' AND PAAADR = ''BUE001'' AND PAAMFU = ''202403’’ AND PAACHK = ''X12-6 Canc''')                         

 Find the randomizer for the line for the line you want to bring back to current.  
 It’s in position 104-109 

 Search for the address number and randomizer in the PAA file to get the record number that needs to be moved to current. 

 Note :  You need to have a 6 character address followed by the randomizer which must be 6 digits.   (ABCDEF000001) 

 Addresses with less than 6 characters will have blank spaces and numbers that are less than 6 digits will have leading zero’s. 

 For example: 

 Address BUE001 randomizer 1963 would be BUE001 00 1963 
 Address GRAY randomizer 1963 it would be GRAY   00 1963   

 Make a copy of the PAA file. 

  Fix the records in PAA by changing them from current to history and removing the merge date and merge month.  

 Run the Payables reorg: X61005 to recalculate the Vendor totals.