---
title: "Configure Text to Pay for Dealerships - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Text to Pay for Dealerships - Ag Internal."
long_description: "This document provides internal system administration information about Configure Text to Pay for Dealerships - Ag Internal."
---

Introduction 

 This article details how to configure a dealership for (Gravity Specific) Text to Pay, including how to: 

 Enable Licenses 
 Configure Payment Provider 
 Configure Text to Pay Settings 
 Configure Secret Key 
 Customer Gravity Configuration Process 
 Generate Text to Pay API Key 
 Configure Deploy Tool 
 Enable Text to Pay in Quantum 

 Version Requirement! Dealerships must be at release DIS_N124 to use Text to Pay. 

 Enable Licenses 

 Important! These instructions are written with the assumption that the Dealer already has Notify enabled. 

 Access Support Manager . 

 

 Select License Management . The Select Dealership screen displays. 

 

 Type the Dealership Enterprise ID in the Dealership field. The Licenses screen displays. 

 

 Select the Messaging Base License option on the left-side of the screen. 

 

 Enable the following options: 

 Prism License Altura Notify Text to Pay 
 Prism License Altura Text to Pay Configuration 

 Configure Payment Provider 

 Access the Altura environment for the dealership being configured. 

 

 Select Applications (Admin Settings | Configuration | Applications) . The Applications screen displays. 

 

 Select Credit Card . 
 Click the Credit Card accordion to expand the pane. 
 Ensure you are working with the correct File Set. 
 Select the Gravity option for all divisions/branches that need to be enabled. 
 Click the Back button in the upper left corner to return to the Altura home page. 

 Configure Text to Pay Settings 

 Important! The following steps should be completed with the Dealership as their input is necessary. 

 

 Select Accounting (Admin Settings | Configurations | Accounting). The Accounting screen displays. 
 Select Text to Pay. 
 Set the Default Page Expiration days. This determines the number of days the Text to Pay link is active. It is 90 days by default with 99 being the maximum number of days. 
 Set the # of days to resend after non payment days. This determines how many days can pass without customer payment until the customer is resent the request for payment. As of 1/16/26, an entry must be made, but this issue is in the process of being resolved. 
 Set the # of attempts before escalation days. This determines the number of times a request for payment is sent before an email is sent to the email address provided in the Email settings on this screen. 
 In the Email Subject field, specify what the escalation email subject line should say when the customer has passed the # of attempts before escalation threshold. 
 In the Email Text field, enter the information to provide in the escalation email. 
 Click the Default Email Addresses accordion to expand the pane and provide an email address at the File Set level OR provide specific email addresses for each division/branch in the File Set. 

 Note : Multiple email addresses can be added for a File Set or Division/Branch. Enter a semi colon after each email address. 

 Scroll down and select the Text To Pay accordion to expand the pane. 
 Enable the entire File Set or specific branches/divisions by sliding the associated option. All associated divisions/branches must be configured with a Notify number. 

 Configure Secret Key 

 Go to Random.org                

 

 Generate 1 password that is 20 characters long and click Get Passwords. 
 Copy the password that is generated and return to the Altura homepage. The password will be used in the next step and MUST be provided to the dealer that you are working with so they can enter it in their Gravity Portal. 

 

 Select Gravity (Admin Settings | Configurations | Gravity) . The Gravity screen displays. 

 

 Select DMS Connection . 
 Paste the generated password in the Text to Pay Secret Key field. 
 Click Save Changes . 

 Customer Gravity Configuration Process 

 The customer must perform the following setup on their system from their Gravity Dashboard. Their dashboard may be different than the screenshots below, but the process is the same. 

 Important! If the dealership dashboard does not display any of the options or tabs mentioned in these instructions, they need to reach out to Gravity for assistance with enabling the missing option. 

 

 Select Settings from the options on the left side of the screen. The Settings page displays. 

 

 Select the Locations tab. The Locations screen displays with each division/branch location represented in a box  as shown below. 

 

 Click the Configure option. 

 

 Click the emergepay tab. 

 

 Scroll down to the bottom of the screen to the Postback Configuration section and click Edit . 
 Select the URL Page checkbox. 
 Enter the following URL in Postback URL field: 

 https://payments.disprism.com/api/public/gravity/transaction/textToPay 

 Enter the secret key (Passphrase) generated in Altura in the Secret Passphrase field. 

 At this point the dealership can start generating text to pay links from Altura. 

 Generate Text to Pay API Key 

 Go to the Online UUID Generator . The following screen displays with an UUID already generated. 

 

 Copy and Record the UUID. It will be entered in Step 8 below and the Deployment section that follows. 
 Access Support Manager . 

 

 Select License Management . The Select Dealership screen displays. 

 

 Type the Dealership Enterprise ID in the Dealership field. 
 Select Authentication Keys . 

 

 Select the Add API Key button. 

 

 Enter the UUID that was generated in Step 1 . 
 Click the Consumer Name drop-down arrow and select Text to Pay (Gravity) . 
 Click Save . 

 Configure Deploy Tool 

 Important! The instructions in this section should be done after hours when the dealer is off of their system to prevent connections from being dropped if the dealership processing operation with the util servlet. 

 Important! Expanded View  must be configured in order for this process to work.  See the Enabling Expanded View in Quantum document for instructions. If Expanded View is not already enabled, the process can be completed when completing Step 2 below. 

 Navigate to the Deploy Tool. 

 

 Select the Setup Dealer Env for a Docker Stack option. 

 

 Enter the dealership number in the search field. Options will display as you type. Select the correct dealership number from the options that display. 
 Click the Dealer Stack File drop-down arrow and select quantum_util_servlet . 
 Scroll down to the bottom of the screen and click the Add button. 
 On the new line that displays, enter the following in the Name field: 

 UTIL_SERVLET_TEXT_TO_PAY_API_KEY 

 Enter the UUID generated in the previous section . 
 Click Save . 
 Click Home in the upper left corner. 

 

 Select the Deploy Docker Stack for Dealer option. 

 

 Select the Dealership again. 
 Select the Quantum_util_servlet option. 
 Click the Deploy button at the bottom of the screen. 

 Enable Text to Pay in Quantum 

 Open a Command Line in Quantum ( Alt + A ). 

 

 Enter X00081 TXTTOPAY,1 and click OK . The servlet checks the option every 15 minutes on the hour, so the Text to Pay buttons feature may not display right away. 

  

 Click here to view the customer facing Text to Pay documentation.