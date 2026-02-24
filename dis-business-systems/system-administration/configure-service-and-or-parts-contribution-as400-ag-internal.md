---
title: "Configure Service and/or Parts Contribution: AS400 - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Service and/or Parts Contribution: AS400 - Ag Internal."
long_description: "This document provides internal system administration information about Configure Service and/or Parts Contribution: AS400 - Ag Internal."
---

_Configure Service and/or Parts Contribution: AS400 - AG Internal_

Introduction 
 Set up for the Contribution KPIs will depend upon whether or not the dealer has been set up with Spectrum. When a dealer has already been set up for Spectrum, the web team will import the general ledger account category settings into the business system. A dealer with Spectrum installed likely already has Sales Ranking configured, but this should still be reviewed. The following steps could be done before or after the Quantum server is configured for the Contribution KPIs, but please be aware that no figures will show in the KPIs until that step is complete. 
   
 Unlock Spectrum 
 Spectrum must be unlocked in order for the Contribution KPIs to function. For best results, use Green Screen for this portion of the install. The easiest way to tell if Spectrum is unlocked is by typing CALL X000B6RP on a command line. If Spectrum is not listed, it is not yet unlocked. Next, check to see if MyAccount is listed. If MyAccount is listed, jump down to the section " Unlocking Spectrum Manually ." If MyAccount is not listed, sign on as SUPPORT, then type INSTALL_MA on a command line. 
 Press <F1> on your keyboard to bypass the MyAccount lock and key. The lock for Spectrum should come up. Use SC/400 (type LOCK on a command line) and paste in the permanent key. Once unlocked, the Spectrum – Exclude Filesets screen will come up. Leave this blank and press Enter to continue. 
 The next screen that comes up is Spectrum – Web Service URLs. If the URLs for each entry do not begin with https(or http):// www.disprism.com , please copy them the URLs listed below. Press Enter to continue. A second screen of URLs displays, check that those also begin with https(or http):// www.disprism.com , then press Enter to continue. 
   
 URLs 
 Accounting URL  https://www.disprism.com/webservices/2.0/accounting 
 Auditing URL  https://www.disprism.com/webservices/2.0/auditing 
 Customer URL    https://www.disprism.com/webservices/2.0/customer    
 Document URL  https://www.disprism.com/webservices/2.0/document 
 Enterprise URL  https://www.disprism.com/webservices/2.0/enterprise 
 Equipment URL  https://www.disprism.com/webservices/2.0/equipment   
   
 The next screen that displays is Spectrum – DIS Dealer#/Dealer ID. The dealer’s customer number should automatically display, but check this for accuracy and adjust if needed. Press Enter to continue. 
 The next screen that displays is Spectrum – Number of days until due. Leave the settings as is and click Enter to continue. You should get a message that Spectrum is unlocked. Once Spectrum is unlocked, two checkboxes (one for Service Contribution and one for Parts Contribution) will appear in the Security Maintenance settings for Management 360 set up. 
   
 Unlocking Spectrum Manually 
 If MyAccount is already unlocked, Spectrum must be unlocked manually, since there is no way to get to the Spectrum lock and key through the normal command once MyAccount is unlocked. To do this, sign off and sign back on as QSECOFR. The password is likely PUGET, but you will need to check the Account Comments for the dealership if PUGET does not work. 
 On a command line, type: 
 addlible disfiles 
 On a command line, type: 
 chgcurlib library 
 On a command line, paste in the following lines separately, then press enter. (Please view the screenshot, as this step is very important to get right.) 
 CALL PGM(X000B1RP) PARM('SPECTRU1' ' ' 'Spectrum 
                      ' 'Y' '') 
 
 Once you press enter, the Spectrum lock should come up. If the lock does NOT come up, please see Aliese for assistance.  
 
 Use SC/400 (type LOCK on a command line) and paste in the permanent key. Sign off of your session and back on as SUPPORT. Once Spectrum is unlocked, two checkboxes (one for Service Contribution and one for Parts Contribution) will appear in the Security Maintenance settings for Management 360 set up. 
   
 Start the Prism Jobs 
 Once Spectrum is unlocked, the Prism jobs need to be running. If Spectrum (or MyAccount) was already unlocked, chances are the Prism jobs are already running. To verify, type WRKACTJOB SBS(DISPRISM) on a command line. You should see several QARWEBxxx jobs running under the DISPRISM subsystem. If the subsystem does not exist, type PRJOBS START on a command line. After a minute or two, type WRKACTJOB SBS(DISPRISM) to verify they are running. If the subsystem exists but no jobs are showing underneath, type PRJOBS RESUME on a command line. After a minute or two, type WRKACTJOB SBS(DISPRISM) to verify they are running. 
   
 Sales Ranking 
 The Sales Ranking report ( Marketing | Sales Ranking Report ) is what controls which sales codes map to each department. A sales code must be mapped to the Service department for the associated general ledger accounts to show in Service Contribution. A sales code must be mapped to the Parts department for the associated general ledger accounts to show in Parts Contribution. To begin, have the dealer print out their Sales Code table ( P.O.S. | Table Maintenance | Sales Code ). Next, have them identify which sale accounts they want mapped to the Service department, and which sale accounts they want mapped to the Parts department. Once these accounts are identified, print out the Sales Ranking sales code assignments ( Marketing | Sales Ranking Report . Click Assign Sales Codes. Click By Sales Code and Document Type. Click Print Assignments). Verify the sales codes they want mapped are on the Sales Ranking sales code assignment printout. If they are not mapped, or are mapped to the wrong department, go back into the Sales Ranking Report menu option and modify the assignments. Remember that each sales code should be mapped for each document type the sales code may be used on, and each division will need to be set up. Once you have one division set up, you can use the copy utility to quickly set up the other divisions. 
   
 Assign General Ledger Account Categories 
 Each general ledger account that is now mapped to one of the Contribution KPIs needs to be identified as a customer, internal, or warranty account. Within Quantum, go to Accounting | General Ledger | Account Maintenance . Type in a mapped general ledger account. Select Customer, Internal, or Warranty from the Contribution Category dropdown. If the dealer already had Spectrum set up, these categories should be pre-filled in, but may be modified. Repeat this for each mapped general ledger account. 
   
 Financial Data Mine Configuration 
 The financial Data Mine configuration must be done for any divisions the dealer wants set up in the Service and/or Parts Contribution KPI. To view what is already done, type DISCFGDM (*VIEW) on a command line. If a division or more is missing and this configuration needs to be updated, you will need a dedicated system. Once a dedicated system is obtained, type DISCFGDM (*UPDATE) on a command line. On the Data Mining Configuration screen, click Assign Accounts. Look to see which divisions do not have a Retained Earnings account in place, and do not say "Yes" under the Already Converted column. Fill in the Retained Earnings account for each division that needs to be configured. Put a B in the Bypass column for any division that does not need to be configured. When finished, click Enter, then either the Forward button at the top, or the Continue button on the left. The system will work to configure the financial Data Mining. When finished, you can type DISCFGDM (*VIEW) on a command line to take a look at the configuration again to ensure everything is in order.  
   
 Import/Edit Budget 
 The Contribution KPIs reach their full value when a budget for the year has been set up. If the dealer is not sure what budget figures they’d like to use, an easy option to start with would be to import the previous years’ sales figures as the budget for this year. There is a utility in Budget Maintenance that can be used for this. Go to Accounting | Financial Reports | Budget Maintenance . Click Copy. Under Source, select Copy from general ledger amounts. The ‘copy from’ year should be last year, and the ‘copy to’ year should be this year. For the Contribution KPIs, the range only needs to be Parts and Service sale accounts, but the General Ledger Sales Summary KPI in Management 360 also uses budgeting, so the entire range of sale accounts could be selected if the dealer is interested. Leave all other settings as is, and click Begin Copy. Because the previous years’ information also shows in the Contribution KPIs, they may want to modify these figures. When copying budget figures from last year, there is a setting option to adjust source amounts by a specific percentage. This is an easy way to modify last years’ figures without having to go to each account manually. 
  
 See Configuring Service and/or Parts Contribution: Quantum Server  for Quantum server configuration instructions.