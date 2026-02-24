---
title: "MyAccount - Internal Troubleshooting - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about MyAccount - Internal Troubleshooting - AG Internal."
long_description: "This document provides internal system administration information about MyAccount - Internal Troubleshooting - AG Internal."
---

_My Account - Internal Troubleshooting - AG Internal_

Welcome to MyAccount 
 MyAccount makes it easier for Dealers to email out Invoices and Statements automatically.
 With the ability to embed MyAccount into your website, customers will have access to their history of payments and charges and be able to download copies of invoices/statements.
 FAQs 
 Who will be able to use MyAccount? 
 Dealers will decide which customers will have emails automatically sent to them. This is done in receivables maintenance.
  Additionally, you can control which customers will be able to see their account online. This is done in Prism.
 They will login with their email address and password selected by you. Customers who have invoices/statements emailed to them are not required to have online access. 
 What information will be available in My Account? 
 ✓ Outstanding and paid invoices, statements, charges, and payments will be visible.
 ✓ Invoices and statements may be viewed online or downloaded directly from the site.
 ✓ Emails may be sent from the site.
 ✓ Inquiries to the dealership may be sent from the site.
 How does information get from the business system to the website?
 ✓ As Point-of-Sale batches are created, invoices will automatically be emailed to designated customers and sent to DIS web servers. The invoices will appear as Documents in MyAccount.
 ✓ When monthly billing statements are generated, they will automatically be emailed to designated customers and sent to DIS web servers.
 ✓ As transactions are posted to receivable accounts, they are sent to DIS web servers, and are immediately available online on the Transaction screen. This includes journal entries, manual adjustments, received on account, and all documents.
   
   
 How are customers set up to use MyAccount? 
 Email addresses are added to customers in Receivables Maintenance and may be marked to receive invoices and/or statements via email. Access to MyAccount online is set up and maintained on the Prism Admin website.
 How current is the information on MyAccount?
 Information is available as soon as batches are posted.
   
 Business System Setup 
 Any customer who wants to have invoices/statements emailed to them needs to be set up in the business system. To do this, go to Accounting | Receivables | Receivables Maintenance. Bring up a customer, either by typing in the Address #, or clicking Name and using the rolodex to search. When the customer’s Receivables Maintenance screen has been pulled up, click the MyAccount button.
   
 Prism Admin Site Setup 
 The Prism Admin site is used to set up customer access to MyAccount online.
 Customers DO NOT need to be setup on Prism admin site to receive emailed invoices and/or statements. 
 Within the Prism Admin site, you can also set up staff members to be able to manage/add customer accounts, manage/add staff member logins, and view a list of invoices/statements that were emailed out.
 To get to the Prism Admin site just change the Dealer number to whomever you are working with.
 https://www.disprism.com/admin/DEALER #
 Username: dis@DEALER#.com
 Password: puget
 Or
  click the colored triangle icon at the top of any Keystone session.
  
 Or on the left-hand side in Quantum.
  
  
 Once logged in, click on the Administration tab, which is the tab with the Gear icon. (Note: depending upon which Prism products you have, the Administration tab may already be selected upon logging in.)
  
 
 To set up a new staff or customer account, click on the menu on the left side of the screen. This will open the tab.
  
  
 Click the Add button.
 Fill in the Email Address, Name, and Password. The enabled should be checked by default, but make sure it is checked. (Note: The website does not verify the email address, so double check the entry to ensure it’s a legitimate email address.)
   
 Adding a Staff or Customer, click the Add button .
 Type in the customer’s address number within the system. After you type in the address, wait a few seconds, and the results will load. If you have typed in a partial address, all addresses that begin with the string of characters you entered will display. Click the result that matches. Adding an account here links the Staff or customers’ MyAccount online account with their account in the business system. 
  
 If the staff or customer has more than one account on the business system, click Add and repeat the above process. Once all information has been entered, and all accounts have been added for the customer, click the Save button.
 The password does not display and can be left alone if it does not need to be changed. Make whatever changes are necessary, then click the Save button. 
  
 Any changes to a staff member login account will also be made on this page. If a staff member needs a password changed, a name updated, an additional business system account added, etc., click on the staff member and then click the Edit button.
  
  
  
  
  
  * Note* Prism can get cranky with changes and as a result you will see a SQL error: 
  
 This will require a JIRA ticket for Ken to fix. 
   
 Prism Admin Site: (Setup Staff and Customers for My Account and Sales Logistics.) 
 https://www.disprism.com/admin/DEALER #
 Username: dis@DEALER#.com 
 Password: puget
   
 Customer site: Dealers can embed this link into their website. 
 *not an option with My Portal* 
 https://www.disprism.com/webar/DEALER #
 Username & Password: -? Whatever was setup in Prism admin.
  
  
  
  
 Troubleshooting PRISM Jobs:
 1) How to check if PRISM jobs are running in AS400
 At a command line type WRKACTJOB and then page down.
  
 Don’t see them running? Type PRJOBS START. Still don’t see them running.
 Check to see if there is an EPC lock WRKDTAARA EPCLOCK$ and delete it.
 Then enter PRJOBS START
  
  
 2) Check PRISM job log to Middle Tier
 At a command line and enter CHKJLOG.
  
 Take a 5 and press enter on the upload.log
 Take a B and hit enter to go to the bottom. This is the latest data.
  
 Look to the right. Status codes in 200’s are correct.
 500’s, 404’s we have an issue
  
 How to see what URLS are being sent to MT
 At a command line enter DSPPFM ARWEBCFG1
  
 Most should be in the format in screen shot https://lowercasedealer#.disprism.com/webservices/2.0/ 
  
 How to update/modify URLs in 400 
 At a command line enter INSTALL_MA
 Press enter, through this screen.
  
 Here is where you would modify URL’s 
   
 And enter again to the next set of URLS. 
   
 Dealer ID sent to Middle Tier
  
 Hit Enter through the next screens.
  
  
  
 You will always see this message that MA is installed.
  
 To see what products are installed enter CALL X000B6RP at a command line.
  
 If a dealer calls in about seeing this message when logging into the Prism admin page. 
 Most likely, have them hit enter and it will go through, this is a bug web development is aware of.