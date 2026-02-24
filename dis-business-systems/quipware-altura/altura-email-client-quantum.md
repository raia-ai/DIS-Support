---
title: "Altura Email Client - Quantum"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Altura Email Client - Quantum."
long_description: "This document provides information about Altura Email Client - Quantum from the DIS Salesforce Knowledge Base."
---

_This article details the process of configuring Altura users so they can instantly generate an email directly from POS Invoicing with the Subject, To, and From fields automatically populated and the Invoicing document attached._

Introduction 

 The new Altura Email Client feature allows you to generate emails directly from Quantum P.O.S. Invoicing with the subject, sender, and recipient automatically populated and the opened document attached. 

   

 This document details how to configure your email server in Altura and generate an email directly from Quantum P.O.S. Invoicing. The instructions should be completed after you have notified DIS that you are interested in this feature, and they have turned on the appropriate licenses. These instructions assume the user being configured is already entered in both Quantum and Altura. 

 Enabling this option impacts the entire File Set and the process associated with the E-mail button in Point of Sale is updated for all users. 

 The sent email will not be listed in the user’s personal sent folder, however, sent emails can be viewed in Altura. Based on their permissions, users can see all sent emails or just the emails they have sent. 

 Altura Configuration 

 Add DNS Records 

 

 Select Communication (Admin Settings | Configurations | Communication). 

 

 Select Email Client . 

 

 Provide the email domain name for your dealership. The Domain is the part of the email that comes after @. 

 For example: discorp.com is the domain name from the dislearn@discorp.com email. 

 Click Save . The DNS records are added as shown below and have a red circle with an X indicating they need to be validated. 

 

 Consult whoever manages your email server to have the DNS records added. It is suggested that you relay the Host and Data information using the Copy and Paste options to ensure accuracy. 
 Once the DNS records have been added, click the Validate button.  If configured correctly, the Valid icons should change to green circles with check marks as shown below. 

 

 Configure Dealer Default Email 

 Click the Dealer Email Configurations pane to expand it. 

 

 Enter the default Email address and user From Name in the fields provided. Anyone at your dealership can send emails using this email address. 
 Click Save . A verification email is sent to the provided email address. 
 Access the email that was sent and click the verification button/link. 

 Configure Individual User Email 

 Access your Altura dashboard. 

 

 Click on your profile icon in the upper-right corner of the screen and select My Account Settings from the drop-down menu. The My Account Settings screen displays. 

 

 Click the Email Configuration pane to expand it. 
 If the email being entered is the same as what is listed in the Altura Settings section at the top of the screen, select the Same as Altura check box. 
 If the email is different than what is listed in the Altura Settings section at the top of the screen, enter the email and the From Name in the fields provided. 
 If you would like to have signature information automatically added to the email, select the Show Signature switch so that it is blue as shown above and enter the text to display. 

 Adjust the size of the text by clicking the heading/paragraph option above the table to select from 3 different heading or a paragraph text size. 

 

 Add your authentic signature by taking a screenshot of it, saving it to your computer, and dragging the image file from the folder on your PC onto the Signature box as shown above. 

 Click Save . 

 Map Users through DMS User Section 

 Dealership users can be configured as the first step if desired. All Quantum users are listed under the DMS USERS tab and can be configured from that location. This prevents users from having to select the Sign in button and provide their credentials when they select the Email button from the Point of Sale Invoicing Navigation fly-out menu as detailed in the next section . 

 

 Select User Management (Admin Settings | Staff Users | Users Management). 
 Select the DMS USERS tab. The names of all of the users configured in Quantum display. 

 

 Locate the user to configure and click the ellipsis on their line. 
 Select Map User . The Map User screen displays listing the Quantum username in the lower field. 
 Click the User drop-down arrow and select associated Altura name/email. 
 Click Save . The Altura user is now mapped to the Quantum user. 
 Once you have configured users, contact DIS again so they can enable the option. 

  

 Generate and Send Email 

 From Invoicing 

 Create the Invoicing document as you normally would or access an existing invoice. 

 

 From the Sold-To or Detail screen, click the Navigation fly-out menu and select the E-mail button. One of the following happens: 

 If your Altura user has been mapped to your Quantum user following the instructions in the previous section , the Email View pane expands with your email address in the From field. 
 If your Altura user has NOT been mapped to your Quantum user, the Authentication Required screen shown above displays. Do one of the following: 
 Click Continue to send the email from the Default dealership email. 
 Click Sign in , to sign into Altura and map your Quantum user to your Altura user. This only needs to be completed the first time. 

 The Email View pane expands with the invoice attached and the subject, To, and From fields populated. 

 

 If desired, click the From drop-down arrow and select the email address to use as the sent from address. Once an individual user and default address are configured, the following options are available to be selected for the sent From email: 

 Individual user email address 
 Dealership default email address (if configured) 
 app@disprism.com – This is the fallback option 

 Enter any informational text you would like to send to the customer in the space provided and click the Send button. 

 From Management 360 – Aged Receivables KPI 

 Access Quantum and select Management 360 as shown below. 

 

 Select the Expansion icon on the Aged Receivables KPI. The Aged Receivables screen displays. 
 Select the account that with the transaction that you want to send via Altura Email. 
 Click the Details button. The next Aged Receivables screen displays listing the customers associated with that account. 

 

 Select the customer in the table whose transaction you would like to Email. 
 Click the Details button. The transactions for the selected account and customer display. 

 

 Select the Transaction in the table to attach in the Email. 
 Click  the Email button. The Email pane expands with the information attached and populated. 
 Provide a desired message and click Send .