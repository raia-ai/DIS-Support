---
title: "CUST0117 custom code specifics - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about CUST0117 custom code specifics - Ag Internal."
long_description: "This document provides internal system administration information about CUST0117 custom code specifics - Ag Internal."
---

_CUST0117 custom code specifics_

GMFSMOD  Custom Code: Fin Stmt Expense Account Relocation @ 2.3/11033  
-----------------------------------------------------------------------
                                                                       
 PURPOSE                                                                 
                                                                       
In response to the request of Dealer's Truck and Process & Power,       
a means will be provided to change the standard Financial Report (X152)
by relocating certain expense accounts to a lower section in the       
report (e.g. after Operating Profit or after Net Profit).              
                                                                       
We will provide some flexibility by allowing the specific accounts to  
be input interactively.  However, in an attempt to also allow          
interactive specification of where to relocate the accounts, it        
became very difficult to provide sufficient safeguards and on-screen   
documentation such that R/L calls would not be generated.        

    

 So, it was decided to keep the parameter input an undisclosed option   
that only a developer or trained Cust Rep would use (for fee?).        
                                                                       
This code will be hidden-opted to restrict its use to paying customers.
                                                                       
 DESIGN                                                                  
                                                                       
The expense account relocation will apply to all divisions of the      
fileset, just as the fin stmt format (FIN file) does.                  
The parameter screen will be added to the first step of the            
Financial Statement process, right after the operator is asked if this 
will be a summary report or not.  Using the existing X152 screen       
format, the parameter screen will provide for up to 10 accounts to be  
relocated in each of 5 different locations:                            

  

                                                                         
div name                      FINANCIAL STATEMENT                 prgnm 
div code                   Expense Account Relocation              date 
                                                                        
                              Subt                                      
Cd Title                      Lvl  Accounts in New Locations            
5  *OPERATING PROFIT********  1                                         
                                   --------  -------  ------- ...       
                                   --------  -------  ------- ...       
                                   --------  ...5 accts/line...         
-  -------------------------  -                                         
                                   --------  -------  ------- ...       
                                   --------  -------  ------- ...       
6  *OTHER INCOME************  1                                         
                                   --------  -------  ------- ...       
                                   --------  -------  ------- ...

                                     --------  -------  ------- ...       
-  -------------------------  -                                         
                                   --------  -------  ------- ...       
                                   --------  -------  ------- ...       
7  *NET PROFIT**************  1                                         
                                   --------  -------  ------- ...       
                                   --------  -------  ------- ...       
-  -------------------------  -                                         
                                                                        
The initial screen fills in the default locations of the standard three 
subtotal lines (from FIN).  This project is limited to changes in this  
area of the fin stmt per the current custom code requests and to        
keep the project to a reasonable cost for the two requesting dealers.   
                                                                        
Any or all of the 5-7 subtotal lines can be moved to provide for        
more than 10 accounts to be inserted in one location.  Also, their

 more than 10 accounts to be inserted in one location.  Also, their     
descriptions can be changed here (no significant benefit over          
changing them in the FIN file, just happens to be possible).           
                                                                       
For further explanation of the meaning of the 5-7 subtotal lines and   
how they are used in the fin stmt process, refer to DIS documentation. 
                                                                       
Parameters:                                                            
  Cd         5,6,7 for the standard lines (each only occurring once)   
             *     for new subtotal line indicating the subtotal will  
                   be a replacement of the previous standard line      
                   (i.e. * after the Net Profit line will produce      
                   a new net profit figure to be used in the fin stmt).
             blank otherwise, such as a heading only (no accounts)     
                   or such as a new subtotal that does not replace

                    a standard (5-7) subtotal.                               

     Title      any text; if non-blank it will be printed                
                                                                      
  Subt Lvl   1-4   same meaning as FIN file: prints subtotal 1,2,3 or 
                   4 and clears that subtotal and all lower ones.     
                                                                      
  Accounts   up to 5 7-digit account numbers (no division) per        
             screen line.  The accounts will print in the order in    
             which they occur on the screen, thereby allowing accounts
             to be ordered any way desired.                           
                                                                      
Allowing maximum flexibility within these limitations resulted in     
a environment in which error checking became very difficult.  Either  
flexibility would be restricted or many hours of coding would be      
required to identify all possible problems that could oocur as a      
result of the operator's input.  Therefore, this custom code feature

 will not be changable by dealers.  If we receive additional requests   
for such changes, a developer or trained R/L person who understands    
the fin stmt format and process will be needed to set up the           
parameters.  If we consider making this a base package feature, or a   
widely used custom code option, this strategy can be reconsidered.     
                                                                       
   CUST0117 = 0  custom code not installed                             
   CUST0117 = 1  custom code installed, parameters can not be changed  
   CUST0117 = 2  custom code installed, parameter screen appears and   
                 changes allowed/saved                                 
                                                                       
Object      Type      Attribute   Comments re: object changes          
----------- --------- ----------- -------------------------------------
X15200      *OCL                  add FIN file to X15208               
X15201      *OCL                  add additional access to GLM         

  X15205      *PGM      RPG36       report prep program: call X15209CL & 
                                  effect acct relocations per parmeters
X15208      *PGM      RPG36       add new screen for parameter input & 
                                  call X15209CL.                       
X15208FM    *FILE     DSPF36      new parameter screen added           
X15208DTA   *DTAARA               new: storing parameters (600 bytes)  
 in FILEu                           1-10  X15208DTA hardcoded, not used
                                   11-16  6 1-char codes (Cd on screen)
                                   17-166 6 25-char titles             
                                  167-172 6 1-digit subtotal levels    
                                  173 522 50 7-digit account numbers   
X15209CL    *PGM      CLP         data area create/change/read         
                                                                       
*MEMBER LIST - TOP                                                     
QS36PRC                                                                 

 QS36PRC              
 X15200              
 X15201              
                     
QS36SRC              
 X15205              
 X15208              
 X15208FM            
                     
QCLSRC               
 X15209CL            
OBJECTS              
 X15208DTA           
*MEMBER LIST - BOTTOM
** end **            

  

 A003385 Solution record in SC400.