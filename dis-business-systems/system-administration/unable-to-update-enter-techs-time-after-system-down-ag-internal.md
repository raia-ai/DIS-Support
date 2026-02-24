---
title: "Unable to Update/Enter Tech's Time After System Down - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Unable to Update/Enter Tech's Time After System Down - AG Internal."
long_description: "This document provides internal system administration information about Unable to Update/Enter Tech's Time After System Down - AG Internal."
---

_Unable to Update/Enter Tech's Time After System Down - AG Internal_

Issue 

 Error message CPF4161 appeared during OPEN for file SATECL0. 

  

 Solution 

 A unique keyed access path for member SATECL0 was not built.                  

 Records in member SATECL0 have duplicate keys.                          

 Error message CPF4161 appeared during OPEN for file SATECL0.            

 Function check. RNX1216 unmonitored by X527RP at statement 0001000001,  

   instruction X'0000'.                                                   

 Error message CPF4161 appeared during OPEN for file SATECL0 (C S D F).  

 Error message CPF4161 appeared during OPEN for file SATECL0 (C S D F).  

 ************************** 

   

 Ran SQL                                                                      

  SELECT STCDIV, STCAOS, STCADR, STCDOC, STCTEC, count(*) as counter            

     FROM satecp GROUP BY STCDIV, STCAOS, STCADR, STCDOC, STCTEC HAVING         

     count(*) > 1                                                                

  .                                                                             

                                                            Display Report                                            

  Query . . . . .:   LIBRARY/DISSQLQM          Width . . .:       123                                                 

  Form  . . . . .:   *SYSDFT                   Column  . .:         1                                                 

  Control  . . . .                                                                                                     

  Line   ....+....1....+....2....+....3....+....4....+....5....+....6....+....7....+....8....+....9....+....0....+.... 

           Division  Address or Stock  Address_Stock  Document Number  Technician Code         COUNTER                

           --------  ----------------  -------------  ---------------  ---------------  --------------                

  000001   A         A                 BROO10         WO12969          GN00                         2                  

  ******  * * * * *  E N D  O F  D A T A  * * * * *        

 ***************************                                                                   

   

 Searched SATECP file for WO12969 and found two records.  Used STRDFU to remove all but one of the records.                                                                                                                        

  Deleted LF for SATEC* 

      SATECL0     FILEH       LF          Work Order / Technician: Update Index 

      SATECL1     FILEH       LF          Work Order / Technician: Retrieval In 

      SATECL2     FILEH       LF          Work Order / Technician: by Technicia 

      SATECP      FILEH       PF          Work Order / Technician Cross Referen 

 *************************** 

   

 Then ran X6-7 and cleared SAT file - CLRPFM SAT