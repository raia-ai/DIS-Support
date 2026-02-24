---
title: "Text to Pay - Quantum"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Text to Pay - Quantum."
long_description: "This document provides information about Text to Pay - Quantum from the DIS Salesforce Knowledge Base."
---

Introduction 

 Text to Pay allows you to quickly send personalized texts to designated customer contacts requesting payment for an invoice from POS Invoicing, Receivables Inquiry, or directly from Notify. The customer contact can then click a link in the text and make a payment via Gravity Payments. 

 Text to Pay lets you specify the number of days to wait for payment before the text is automatically resent to the customer as well as the number of times the text is resent before notifying a designated recipient at your dealership company and/or branch that payment has not been received. 

 Dealerships must purchase Notify and be at NR_122 or higher to utilize this feature. Additionally, you must have an account with Gravity and complete some DIS assisted Gravity Dashboard configuration. This option is set at a divisional level. Methods used to track payments are determined and maintained by dealerships. 

 This document details how to configure Text to Pay and complete the associated processes. After you have notified DIS that you are interested in this feature, and they have turned on the appropriate options and licenses, use the following steps to send texts for payment. 

 Configure Text to Pay defaults in Altura 
 Add customer contacts to receive texts for payment 
 Create and send text for payment from POS Invoicing 
 Create and send text for payment from Receivables Inquiry 

 Altura Configuration 

 Configure Text to Pay Defaults 

 After you have contacted DIS and had them enable Text to Pay, configure the Text to Pay defaults and contact information in Altura. 

 

 Select Accounting (Admin Settings | Configurations | Accounting) . The Accounting screen displays. 

 

 Click the Text to Pay option on the left-side of the screen. 
 Enter the following information in the Default Settings pane fields: 

 Default page expiration - Enter the number of days before the link sent in the text becomes inactive (no longer functioning). 
 # of days to resend after nonpayment - Enter the number of days until the text is resent as a result of nonpayment in the # of days field 
 # of attempts before escalation – Enter the number of times the text is resent to the customer until an escalation email is sent to designated employees at a company and/or branch(es). 

 Click Save . 
 Enter the generic email subject line and message in the Email Settings pane fields to send to the designated company/branch recipients when the # of attempts before escalation threshold is met. 
 Click Save . 
 Scroll down the page and expand the Default Email Addresses pane. 

 

 In the File set pane field (C-C in the screenshot above), enter the email address for the company employees to receive the escalation email any time the threshold is met in any branch/division of the Company/File set. 
 In the Division/branch field (C – New Dundee in screenshot above), enter the email of the employee at that location who should receive the escalation email. 
 Click Save when you have finished providing escalation emails and scroll down to the bottom of the screen. 

 

 Click the Companies/File set panes under Text to Pay with branches/divisions you want to enable for Text to Pay and slide the option to green to enable as shown above. 
 Click Save when finished. 

 The Altura configuration process is complete. 

 Add New Contact for Customer 

 Customer contacts must be added to the system before texts for payment can be sent to them. Contacts can be setup for a customer in either Point of Sale or Receivables Inquiry. Once configured, they will be available for selection in both options. 

 Access the POS Document in Invoicing that you want to submit a text for payment and navigate to the Sold To screen. 

 

 Click the Text To Pay button under the Customer tab. The Text To Pay Expanded pane displays. 
 Click + Add Contact . The Add Customer Contacts pane displays. 

 

 The First Name, Last Name, and a cell phone number must be provided. Enter any other available information. 
 Click Save . The Add Contact screen closes, and the contact is now available for selection. 

 Send Text for Payment from Sold To Invoicing Screen 

 

 Access the Text to View pane for the customer from the Invoicing Sold To screen. The screen that displays when the Text to Pay button is selected depends on whether there is a current dialogue with a contact assigned to the customer. 

 If there IS NOT an existing dialogue, the screen above displays. Continue with Step 2 . 
 If there IS an existing dialogue, the Text to Pay screen opens with a contact already selected. Continue the instructions with Step 3 . 

 Select the contact(s) that you would like to send the text for payment and click the Add Selected Contacts button. 

 The Text to Pay pane displays the selected customer contact, amount of the invoice, and the associated document number. 

 The Text to Pay defaults that were setup in Altura display along with the Cashier ID which is the user mapped in Altura to the current user logged into this Quantum session. 

 

 If you want to change the contact set to receive the text request for payment, click the drop-down arrow (circled in green) and select the new contact. If the contact you want to send the text to has not been configured in the system, click the Create Contact button and Add the Contact . 
 Verify the amount listed and update if necessary. 
 Enter a message of up to 200 alphanumeric characters (no special characters allowed). This message displays in the both the text message the contact receives and the page that is accessed through the link included in the text. 
 Update any other information as necessary and click Send Transaction . The text is sent to the contact. 

  

  

 The customer contact selects the link and is taken to the Gravity payments page listing your dealership information, the invoice and amount associated with the payment request, and the text message. 

 After providing their billing address information and payment method with details, the customer contact selects the Pay $ button to process the payment. 

 Send Text for Payment from Transaction Screen in Receivables Inquiry 

 Before this process can be completed, the customer contact must be added to the system using the instructions in the Add Contact section of this document. 

 Select Receivables Inquiry (Accounting | Receivables Inquiry) . 

 

 Hover your cursor over the Navigation button and click the Transactions button. The Transactions screen displays. 

 

 Enter the Receivables Address and click Enter or click Name and select it from the index. 
 Select the transaction line from the table that you want to receive payment for and click the Text to Pay button. The Add Customer Contacts screen displays. 

 Note : If you click Text to Pay without selecting a transaction, the text for payment request will be for the customer’s entire balance 

 

 Select the Customer Contact(s) that you want to send a Text for Payment request and click the Add Selected Contacts button. The Text to Pay fields display. 

 

 Verify the amount listed and update if necessary. 
 Enter a message of up to 200 alphanumeric characters (no special characters allowed). This message displays in the both the text message the contact receives and the page that is accessed through the link included in the text. 
 Update any other information as necessary and click Send Transaction . The text is sent to the contact.