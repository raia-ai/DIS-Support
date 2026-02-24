---
title: "SQL to Change Tax Code on Address - Standard Tax - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about SQL to Change Tax Code on Address - Standard Tax - Ag Internal."
long_description: "This document provides internal system administration information about SQL to Change Tax Code on Address - Standard Tax - Ag Internal."
---

_SQL to Change Tax Code on Address - Standard Tax - AG Internal_

Introduction 

 Sometimes it may be needed to change a tax code for customer addresses with a specific tax code. In this case, the customer has to prove they are tax exempt each year. So the dealer wanted to change the tax code for all address from and specific exempt tax code to a specific taxable code.  Then when the customer presents the necessary paperwork, they change the tax code to a nontaxable code in the maintenance screen. 

 The easiest way to do this is through SQL. The table that holds the tax code for Addresses is ADO.  (It used to be ADM but changed quite some time ago.) 

 In this case, the dealer was setup with Standard tax.  While the code is viewable on screen as a 1 character field, behind the scenes there is a second character that notes the division code.  

  

 Solution 

  

 1. Make a copy of ADO.  (suggested name of copy would be ADOmmddyy ex:ADO123022) 

  

 CPYF FROMFILE(FILE u /ADO) TOFILE(FILE u /ADO123022) MBROPT(*ADD) CRTFILE(*YES)  - where  u  is the Fileset. 

 Example :  CPYF FROMFILE(FILEW/ADO) TOFILE(FILEW/ADO123022) MBROPT(*ADD) CRTFILE(*YES) 

 Make sure both files have the same number of records. 

 To do this, at a command line, type: DSPPFM ADO and press enter. 

 Put an 8 next to the File and press enter.  

 In the Control field, type the letter B and press enter.  

 Note the number to the right of the 'Total records' field. 

 Do the same thing for the file you copied to and confirm that they have the same number of records.   

  

 2. Use the following SQL to see how many of the addresses are tied to the current tax code. For standard tax this will be the tax code and then the division in the field called AOTAXC . 

 Example: 

 DISSQL REQUEST('select * from ADO where AOTAXC like ''5%''')   

 This example looks at every address that starts with a tax 5.  The Tax code would be each tax 5 plus division. The SQL could be refined to sort or count if needed.  

 This is a good way to look at the data to see if there are multiple divisions involved.  

  

 3. Refine the SQL to select on just the tax code you want to affect. 

 Example: In this case we are selecting only addresses with the 5I tax code.  

 DISSQL REQUEST('select * from ADO where AOTAXC = ''5I''')   

 Take another look and make sure this is the right data to change. If all is good.  Proceed to step 4. 

  

 4. Use the following SQL to update the ADO file for the Tax code Change based on what the current tax code is. 

 Example: In this case, we are changing tax code 5I to 4I 

 DISSQL REQUEST('UPDATE ADO  SET AOTAXC = ''4I'' where AOTAXC = ''5I''') 

   

 Note : This will not change any existing lines on Open POS tickets.  These will need to be changed manually for each line that has the wrong tax code on them, by Dealer.