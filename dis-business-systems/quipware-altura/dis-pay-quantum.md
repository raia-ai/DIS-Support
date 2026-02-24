---
title: "DIS Pay - Quantum"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DIS Pay - Quantum."
long_description: "This document provides information about DIS Pay - Quantum from the DIS Salesforce Knowledge Base."
---

_This article details how to:
•	Add DIS Pay Credit Card Code and Assign EDC Type
•	Process a DIS Pay transaction
•	View DIS Pay transactions in Altura
•	Rename integrated terminals through DIS Pay
•	View deposit reports
•	View DIS Pay posting batch 
•	Void DIS Pay transactions and issue refunds_

Introduction 

 DIS Pay offers integrated payment services for processing credit card payments . This document provides configuration instruction and details the available methods for processing a DIS payment in Quantum. It also details how to view and work with transactions through Altura 

 Important! To process payments by manually entering card numbers and not using terminals, the business system must be connected to a QRA or QDA server. 

 Dealerships must be at release DIS_NR122 or higher to use this feature. 

 Click on any BLUE text below proceeded by an ▶ to expand topic information. Click the BLUE text again to hide the topic information. 

  

 
 Add Credit Card Code and Assign EDC Type - Before a DIS Pay transaction can be completed, a card code for DIS Pay needs to be added to the system. 
  

 Select Credit Card (P.O.S. | Table Maintenance | Credit Card) . The Card List screen displays. Click the Add button if the screen displays in Change mode. 

 

 Enter the two character Card code, Name, and address number. 
 Assign 22 as the card EDC (Electronic Capture Device). 
 Click Enter to save the card information. 

 
  

 
 Process Payment - This section details how to process a DIS Pay transaction through an integrated terminal, manually without a card, and with a saved card token. 
 Select Invoicing (P.O.S. | Invoicing) and access Invoicing Sold-To screen. 

 

 Enter the sales representative’s address number and the credit card code added to system for DIS Pay (DP in the example above). 
 Click Enter . The Detail screen displays. 

 

  Add the transaction lines to the ticket. 
 Click the Navigation button and select the Print & Close option. The Credit Card Authorization screen displays. 

 

 Ensure the amount is correct and click Enter . If the customer’s billing information hasn’t already been added to the system, the Card Verification screen displays. 
 If you do not want to capture a token for the customer's credit card, unselect the Capture Card token checkbox. The checkbox is selected by default. 

 

 This information must be provided. Click Continue . 

 The DIS Pay pane displays prompting for payment. The payment can be taken by running a card through a terminal, entering card information manually, or using a saved card. 

 Click on one of the three payment methods below to display instructions on the process: 

  

 
 • Process Payment through Integrated Terminal - This process is used when the card is present. 
 The Terminal tab is selected by default when the DIS Pay pane displays allowing you to swipe or tap the card. 

 

 Select the Payment Terminal drop-down and select the terminal from those that have been configured by the dealership. 

 Note : The names assigned to terminals, such as M400-8062778 as shown above, can be modified to a more identifiable name such as Parts Counter 1 or Mac’s Terminal . See the Rename Integrated Terminals section for additional details.      

 Swipe or tap the card and click the Pay $0.00 button (where $ 0.00 = the listed price).    
 When the terminal lights up the customer can complete the transaction. 

 Note : The payment process resets after 2 minutes and the payment process will need to be restarted if the session expires. 

 
  

 
 • Manually Process DIS Pay Card - The card information can be entered manually if terminals are not available, or the customer is paying over the phone. 
  

 

 Select the Manual tab at the top of the screen. 
 Enter the card information. 

 Note : At this time, the customer’s name and address needs to be entered in both Quantum and the screen above when processing a manual transaction. 

 Important! If the customer card is an American Express, enter the 4 digit CVV on the front of the card in the Security Code field rather than the 3 digit code on the back of the card. 

 Click the Pay $0.00 button (where $ 0.00 = the amount). 

 
  

 
 • Process DIS Payment with Saved Card - At this time, all cards that are run through a terminal OR entered manually are saved in DIS Pay using Perseus Payments robust encryption protocols and are available to be used for payment. Once a credit card has been saved to the system, it will be associated with the customer. 
  

 The number of cards the customer has saved in the system is indicated by the number in the blue circle on the Saved Cards tab as shown below. 

 Note : To remove a saved credit card, access the customer in Receivables Maintenance, select the Navigation fly-out menu, click Credit Cards, and delete the saved DIS Pay credit card token. 

 

 Click the Saved Cards tab. Any cards saved for the customer display. 
 Select the check box for the credit card to use for payment. 
 Click the PROCESS PAYMENT $0.00 button. 

 
  

 Complete Payment Process 

 Regardless of which payment method is used, when the Pay $0.00 button is selected and the payment is successfully transmitted, the Status of the payment displays as Success and a green message displays indicating the payment Status as Authorized as shown below. 

 

 Other possible transactions status options are listed below (select the transaction to view more details). 

 Aborted – This option displays if the transaction times out or the Cancel Transaction button is selected. 
 Failed – Issues occurred during the transaction process or there was a problem with the card/card information. 
 Pending – The transaction is pending. This may indicate the transaction needs to be reprocessed. 
 Refunded – The transaction has been refunded in Altura. 
 Card Saved – The card token was saved without a transaction. 

 As detailed in the next section, the status is also listed in the Transaction Timeline and detailed reasoning may also be provided. 

 To prevent placing a freeze on the card, it is best practice not complete multiple attempts on a failed transaction. If a transaction fails, provide the customer the reasoning, and ask that they contact the card issuer for additional details. 

 
  

 
 View Transactions in Altura - DIS Pay transactions made through Quantum can be viewed in Altura and filtered by branch and/or specific dates. 
  

 

 

 Access Altura and select DIS Pay Transactions (Accounting | Payments | DIS Pay Transactions). The DIS Pay screen opens with the Dashboard selected. 

 

 Select the Transactions option. 
 Click the Locations drop-down arrow and select a specific Branch or All locations. 
 Click the date range / calendar icon and select a time period from those listed on the left of the screen that displays or customize the date range by selecting a beginning and ending date on the calendar. 

 

 Select the 3 vertical dots by any column header to Unsort the transaction detail in the table if it is currently sorted or in ascending or descending order based on that column’s content. You can also do this by clicking on the header itself. An arrow displays next to a column header if the contents are currently sorted by that column indicating the sort order. 
 Select the Filter option to display the filter screen which allows you to filter the table content based on the column/operator/value. 
 Click the Columns option above the table or the Show columns option to display the Find columns screen which allows you to click on column headers to display (blue) or hide them (white/faded). You can also click Hide from the column drop-down to hide that specific column. 
 Select the Refresh icon to update the transaction information listed in the table. 
 To set the number of transactions listed in the table, scroll down to the bottom of the screen. 

 

 Click the Rows per page drop-down option and select the number of transactions to list per page. 

 Select the Next and Previous carats to navigate between pages of transactions. 

 

 Click on any Transaction line to view the Transaction details and Timeline. 
 Click the Learn about it icon in the upper right corner of the Transaction Timeline pane to display a detailed description of each possible status. 

 
 

  

 
 Rename Integrated Terminals - Terminals can be assigned a specific name to help users readily identify and select the terminal they want to use. 
  

 Access the DIS Pay Dashboard. 

 

 Select the Terminal Settings option from the options on the left. The Terminal Setup table displays. 
 Click in the Terminal Alias field for the terminal that you want to rename and enter the new name. DIS suggests including the last 4 digits of the terminal Serial Number in the new name as shown above. If the dealership has multiple branches, include Branch defining details.  

 
  

 
 Deposit Reports - The Deposit Report provides a snapshot of amounts deposited into dealer bank accounts and can be exported to a spreadsheet. 
  

 The  Deposit Report  provides a snapshot of amounts deposited into dealer bank accounts and allows you to: 

 Reconcile settlements with actual bank payouts  
 Track deposits by date range or single day  
 Identify discrepancies due to fees, refunds, or chargebacks  
 Generate audit-ready records for finance/compliance  

 DIS Pay deposits are  net deposits (the processing fees are deducted).  

 Access Deposit Reports   

 Beginning December 31 st , 2025, daily deposit data will be stored under the Deposits option.  

 

 Select the  Reports  option on the left-side of the screen and click Deposits . The deposits display in order of the deposit date, NOT the transaction date. 
 Click  Export  to download the report. A spreadsheet with the following format is downloaded to your computer:  

 deposit_report_businessName_dateRange.xlsx  

 Report information details are listed in the table that follows: 

 Deposit Report Fields 

 
 Deposit Report Fields 

 
 
 Field 

 
 Description 

 
 Example 

 
 
 Batch Number  

 
 Unique settlement batch ID  

 
 387  

 
 
 Transaction Date  

 
 Date transaction was processed  

 
 8/25/2025  

 
 
 Payout Date  

 
 Date funds were deposited  

 
 8/26/2025  

 
 
 Transaction Type  

 
 Type of transaction (e.g., capture)  

 
 capture  

 
 
 PSP Reference  

 
 Processor-generated reference  

 
 P000PNTW3EDHHAA3  

 
 
 Merchant Reference  

 
 Unique transaction ID  

 
 10379-123456-12217-777E  

 
 
 Sale Amount  

 
 Gross amount before fees  

 
 46.77  

 
 
 Transactions  

 
 Total paid by customer  

 
 48.17  

 
 
 Refunds  

 
 Refunded amount  

 
 0  

 
 
 Chargeback  

 
 Chargeback amount  

 
 0  

 
 
 Transactions - Refunds  

 
 Net transaction amount  

 
 48.17  

 
 
 Fees  

 
 Processing fees  

 
 1.4  

 
 
 Total Payout Amount  

 
 Net payout (Transactions - Refunds - Fees)  

 
 46.77  

 
 Scheme Fees - Fees from the card brands. This changes based on the card type. 
 Interchange - Fee charged between banks for processing card payment 
 
 Fixed Fee - A fixed fee of $0.10 per transaction. 

 
 

  

 
  

 
 Work with DIS Pay Transaction Batch in Quantum - The current and closed DIS Pay EDC (Electronic Data Capture) batches can be viewed or have other options performed on them. 
 Select Transmit EDC Credit Card Transactions (P.O.S. | Post P.O.S. Documents | Transmit EDC Credit Card Transactions). 

 

 Highlight the DIS Pay option and click the Select button. The Batch List screen displays. 

 

 Select a specific transaction, then click one of the available options to work with that transaction. 

 

 
  

 
   Void and Refund Transactions - Successful DIS Pay transactions can be voided and refunds can be initiated prior to the transaction being posted. 
 Important! At this time, you must complete processes in both Quantum and Altura to void and refund transactions. 
 
  

 Create a Negative Invoice in Quantum 

 Create a negative invoice in Quantum for the transaction to be voided in Altura. 

 

 Enter DP as the credit card code on the Sold-To screen and Click Enter to access the Detail screen. 

 

 Create a negative transaction for the refund amount and click Enter to add it to the invoice. 
 Select the Navigation button and click Print & Close . 
 Press Enter twice to continue. The DIS Pay window opens. 

  

 

 Click the Cancel Transaction button in the DIS Pay window. 

 

 Select Auto/Manual Auth . 
 Type Refund in the authorization code field and click Enter . 
 The transaction is closed, and Quantum is offset.  

 Void Transaction and Issue Refund In Altura 

 Successful transactions can be voided, and partial or full refunds can be issued using the method detailed below if the card is not present. 

 Access DIS Pay in Altura, select Transactions , and use the filter options above the table to locate the successful transaction you want to void and refund. 

 

 Use the scroll bar to access the right side of the table. 
 Click the Void button. The Refund screen displays. 
 Select Full Refund or Partial Refund . If you select Partial Refund, the Refund Amount field displays. Enter the amount with a decimal point. 
 Click the Confirm button to void the transaction and submit the refund.