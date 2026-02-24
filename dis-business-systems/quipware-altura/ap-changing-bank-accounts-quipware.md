---
title: "AP - Changing Bank Accounts - QuipWare"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about AP - Changing Bank Accounts - QuipWare."
long_description: "This document provides information about AP - Changing Bank Accounts - QuipWare from the DIS Salesforce Knowledge Base."
---

_AP - Changing Bank Accounts - QW_

Steps for Changing a Bank Account 

  

 These instructions are to change the QuipWare setup when a client moves their cash account to a new bank or a new account at the same bank. There are two main reasons why all new setup is required: 

 If the customer is using QW Bank Reconciliation, and the account is new at the same bank, or a new account at a new bank, a separate GL account is required to maintain the ability to reconcile. 
 If a check ever needs to be researched, or reprinted for any reason, you would want to see the original account information (bank name and address, account number, routing number, etc.) as it was originally printed. Using the existing GL account and bank account but changing any of those details means all old checks would display or reprint with the new account details. 

 These are the steps for setting up a new account: 

 Create a new general ledger account in the chart for the new bank's cash account. 
 If the bank name is changing, set up a new supplier record for the new bank. 
 Add the bank setup under Accounting > Setup > Setup > Bank Account, and select the general ledger account created in step 1, and the supplier ID created in step 2. 
 Find the accounting distribution record for accounts receivable cash receipts. Change the distribution to point to this new account if cash deposits are going here. 
 In Accounting > Setup > Ledger, for all of the AR, AP and PO Invoice ledgers, change the GL Account field there. (There is a field for the GL account, and one for the error account -- change the GL account.) 
 There is an SQL (see next two pages) to update several tables with the new bank account information: 
 ast for supplier sub account 
 spb for supplier branch record 
 gtd for the GL account to pay (gla_id_pay and gca_id_pay) 
 gtp for any checks that might be in progress (gla_id_pay and gca_id_pay). 

 When doing an AP check selection, select only that new bank (not [All]), then check the box underneath the list of banks that says "Select entries with no bank." 

  

 Note: This SQL file is also saved here: 

 \\Ndsts0_new\nds_doc\QuipWare\QWCSG\SQL Statements\AP-change bank account.sql 

  

 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 

 -- INSTRUCTIONS 

 -- The relationship between the bank setup and the GL account is in the crt table using the crt.gla_id field 

 -- The bank account for a specific AP invoice is driven by the gtd.gla_id_pay and gtd.gca_id_pay (not by the crt_id) 

  

 -- 1. First, run SQL for the new bank's GL cash account to verify what the gla.gca_id is (this is very important) 

  

 -- 2, 3. The next two SQL's look at the assigned bank on the supplier's sub account (ast) and branch bank account (spb) 

  

 -- 4. The next SQL is view and count the number of records on gtd where the entry is unpaid or partially paid, and the 

 --      the old cash account still exists. 

  

 -- 5. This SQL is to view and count the number of entries selected for payment in the gtp table, so those records can 

 --      be updated, also. 

  

 -- 6. This SQL is to view the bank setups, to ensure that the correct account number is selected for the updates 

 * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 

  

 -- 1. BE SURE TO VERIFY THE GCA_ID FOR THE NEW CASH ACCOUNT 

 select * from gla where gla_id = '1001' 

  

 -- 2, 3. VIEW BANK ACCOUNT ON SUPPLIER SUB ACCOUNT AND BRANCH RECORDS 

 select * From ast where crt_id <> '0033699017' ; 

 select * From spb where crt_id <> '0033699017' ; 

  

 -- 4. VIEW GL CASH ACCOUNT ON UNPAID OR PARTIALLY PAID ENTRIES 

 select * from gtd where gla_id_pay <> '1001' and gtr_id in (select gtr_id from gtr where spp_id is not null and gtr_mat_code < 3) and gtd_mat_code <> 3; 

  

 -- 5. VIEW GL CASH ACCOUNT ON ENTRIES SELECTED FOR PAYMENT 

 select * from gtp where gla_id_pay <> '1001' and gtp_status_act < 2 and gtp_void = 0; 

  

 -- 6. VIEW THE BANK SETUPS -- MAINLY TO ENSURE THAT THE CORRECT CRT_ID IS SELECTED TO UPDATE THE SUPPLIER AST AND SPB TABLES 

 select * from crt ; 

  

  

 -- UPDATE THE SUPPLIER SUB ACCOUNT AND BRANCH BANK ACCOUNTS 

 begin work; 

 update ast set crt_id = '0033699017' where crt_id <> '0033699017' ; 

 update spb set crt_id = '0033699017' where crt_id <> '0033699017' ; 

 -- commit; 

 -- rollback 

  

 -- DON'T FORGET TO CHECK THE GCA_ID (UPDATE GTD.GCA_ID_PAY IF NECESSARY) 

 begin work; 

 update gtd set gla_id_pay = '1001' where gla_id_pay <> '1001' and gtr_id in (select gtr_id from gtr where spp_id is not null and gtr_mat_code < 3) 

  

 -- commit; 

 -- rollback 

  

 -- DON'T FORGET TO CHECK THE GCA_ID (UPDATE GTP.GCA_ID_PAY IF NECESSARY) 

 begin work; 

 update gtp set gla_id_pay = '1001' where gla_id_pay <> '1001' and gtp_status_act < 2 and gtp_void = 0 

  

 -- commit; 

 -- rollback 

  

  

 **Documentation of Steps for Changing a Bank Account Attached in Files Box on the right side of the screen.