---
title: "DIS Pay FAQs - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DIS Pay FAQs - Ag Internal."
long_description: "This document provides internal system administration information about DIS Pay FAQs - Ag Internal."
---

Q: What happens in chargeback scenarios?   

 A:  As of 1/26/26, we do not need to manage a chargeback. Perseus Payments handles it from end to end.  

 Q: What do I do if the terminal won’t light up? 

 A:   Reset the terminal. 

 If the terminal still does not light up, there could be a problem in the back end with how it is attached to Altura and Quantum. Escalate to Todd’s Team for verification in the backend. 
 If Todd's team has confirmed there is no issue, escalate to Sean. Flag as urgent; client cannot transact. Provide screen captures of the incident and an accurate description of the issue. Check if other clients are experiencing this issue or if it is isolated to this client.  

 Q: Why is the Terminal check mark yellow? 

 A:   The terminal is inactive 

 

 Ensure it is plugged in and connected to Wi-Fi. 
 Reboot the terminal if all else fails. 
 If the terminal still doesn’t come back online, we need to check the integration while simultaneously notifying Perseus, as we may need a replacement terminal. 

 Q: Why is the Terminal check mark green? 

 A:   The terminal is active and connected to Altura.  

 Q: What do I enter for the CVV with an Amex Card (American Express)? 

 A:   For American Express cards, Enter the 4-digit CVV on the front of the card. 

 Q:  Manual cards, do the address fields matter?   

 A:   Yes.   

 DIS Pay does an AVS (Address Verification System) check on all cards. We look at the information provided to the issuing bank of the card and ensure that it matches what the dealer entered into the manual card section. If it does not match, the transaction will return failed. The reason code may be fraud or failed CVV. We advise that the dealer contact the cardholder to ensure the correct address was provided. The cardholder can call their issuing bank to verify the transaction.  

 Q: Does the postal code matter?   

 A: Yes, the postal code matters. Our system uses AVS (Address Verification System) to check postal codes to ensure they are accurate.  

 Q:  Does the name matter? 

 A:  No, the name is not checked and does not.  

 Q:  Does the card have to be saved? 

 A:  Prior to DIS_N126, the card had to be saved. After that release, there is a Capture Card Token checkbox on the credit card authorization screen that can be unselected. 

 Q:  How do we delete a saved card?   

 A:  It cannot be done at this time. This is being worked on. 

 Q: How do we save a card?   

 A:  Prior to DIS_N126, the card was automatically saved. After that release, there is a Capture Card Token checkbox on the credit card authorization screen that can be selected. 

 Q:  How do we use a saved card?   

 A:    Click Saved Card on the DIS Pay Expanded pane and select the check box for the desired saved credit card.   

 Create an invoice being sure to enter credit card code DP on the Sold-To screen. 
 Close the invoice. 
 Select Saved Card at the top of the expanded view  pane that opens. 
 Confirm the last 4 digits with the client, select the check box for the card, and press Pay. 

 Q:  What does transaction ID represent?   

 A:  The transaction ID has no meaning to DIS at this time. The Transaction ID is only relevant to Perseus Pay.  

 Q:  What is the Order ID.   

 A:  This has no relevance for DIS. We are working on getting the invoice number added, but we are not there yet.  

 Q:  What if I realize the amount is wrong while checking out?   

 A:  Select the Cancel Transaction button and correct the line items causing the issue on the Detail screen, then Print & Close the invoice 

 Q:  The transaction was successful, but the expanded view/pay window is not closing.    

 A:  This needs to be escalated to engineering to determine the problem. It is best to log in to the client's Quantum from our end and see if we can replicate the issue. If this is a new integration, check the whitelist on Perseus. (At this time, Contact Sean regarding how to create a ticket with engineering to get this investigated.  

 Q:  How many times should I try a card if it fails?   

 A:  If a card fails, it is best to check the reason code for why it failed. Then talk to the client to ensure the information provided is correct. If everything is correct, encourage the dealership to have the cardholder contact their issuing bank to determine if there is an issue on their end.  

 Q:  How often can I try a card if it is declined for insufficient funds?   

 A:  Work with the cardholder to determine when it is best to charge their card again. Explain to the client that the card was declined or there was an NSF, at which point have the client guide you on when to charge the card next.  

 Q:  How quickly can I process a refund after a payment?   

 A:  You can process a refund immediately after a successful transaction.  

 Q:  How do I process a refund?   

 A:  As of 1/26/26, refunds are processed in 2 steps for card not present and in 1 step for card present.  

 Card Not Present 

 In Quantum, create a negative invoice with the line items you would like to return. 
 Process it and take note of the final total. 
 Switch over to Altura, identify the transaction in the transaction tab, and slide over to “Void.” 
 Select full or partial void and enter the amount saved from Quantum. Click refund and it will be completed.  

 Card Present 

 Create a negative transaction to trigger a refund when processed using DP. The transaction can be completed using the terminal.  

 Q:  When doing a refund, the manual card option does not show up.   

 A:  This is because refunds are conducted in 2 stages for a card not present refund: 1 – you create a negative invoice in Quantum that will see the refund amount.  

 Q:  The DIS Pay window closed by itself, why?   

 A:  Answer pending investigation  

 Q:  How many computers can use one terminal?   

 A:  Answer pending  

 Q:  How many terminals can one computer use? 

 A:  One computer can use any of the terminals associated with that specific division. You can only use 1 terminal at a time.  

 Q:  How do I install a terminal?   

 A:  They are plug and play with a hard-wired connection; otherwise, you will need to connect them to Wi-Fi following the on-screen instructions.  

 Q:  Customer states their fees are too high and this is not what they signed up for.   

 A:  There are several fees that make up the amount taken out of your daily deposit: 

 Interchange 
 Assessment Fees 
 Processing Fees  

 Q:  I heard talk about cash discounting; what is it?   

 A:  Cash Discounting is a way of offsetting the fees by raising prices and providing a discount to clients who pay via cash.  

 Q:  Why do I have to log in to Altura when I process a credit card payment in Quantum?   

 A:  You shouldn't have to log in; if this issue is occurring, it most likely means there is a problem with their setup.  

 Q:  How do I save a card without running a transaction? 

 A:    Enter the customer's credit card in Receivables Maintenance 

 Go to Receivables Maintenance in Accounting 
 Enter the Customer Address number 
 Select Credit Cards from the Navigation fly-out menu 
 Add credit card and follow the on-screen instructions in the expanded view window.  

 Q:  How do I process a private card using DP?   

 A:  You cannot process a private card using DP.  

 Q:  Why does the address field not populate when I do a manual card transaction?   

 A:  The address field in Quantum is not tied to manual card in DIS Pay. The address entered in the manual card section must be the billing address associated with the credit card.  

 Q:  How do I get the address field to populate during a manual transaction?   

 A:  You cannot get the address field to populate with Quantum information during a manual transaction.  

 Q:  How do I create a token?   

 A :     Enter the customer's credit card in Receivables Maintenance 

 Go to Receivables Maintenance in Accounting 
 Enter the Customer Address number 
 Select Credit Cards from the Navigation fly-out menu 
 Add credit card and follow the on-screen instructions in the expanded view window.  

 Q:  How do I run a batch?   

 A:  Answer pending 

 Q:  How do I do a bulk payment?   

 A:  As of 1/26/26, it is not possible to process a bulk payment in Quantum.  

 Q:  How many people can process a payment at the same time?   

 A:  Everyone who has access to Quantum can process a manual payment simultaneously; the terminals are on a first-come, first-served basis and will not be able to receive a transaction while they are being used.  

 Q:  Error code 400.   

 A:  Answer pending 

 Q:  Moving total bar .  

 A:  The total bar moves as of 1/26/26; it is an issue we are aware of and are working on fixing 

 Q: I see pending transactions that won't go away, why? 

 A:  Once pending transactions are successful, a new line item is added for them.  

 Q:  I see aborted transactions, but I didn’t abort.   

 A:  Transactions timeout after 2 minutes and they will reflect in Altura as an aborted transaction.  

 Q:  I see failed transactions due to fraud.   

 A:  As of 1/26/26, a failed transaction due to fraud is usually because of a mismatch in postal codes.  

 Q:  What does the void button do?   

 A:  The Void button in Altura enables refunds of both partial and full amounts. This does not feedback into Quantum. A client needs to do an offsetting transaction to see it reflected in Quantum's accounting.  

 Q:  How can I get more info on a transaction?   

 A:  Access Altura and click on the transaction you want more information on. A pop-up on the right side of the screen will provide additional details as to the reason why the transaction failed.  

 Q:  Why is the cost in Altura not right?   

 A:  The cost in Altura is an estimate based on our processing fees and does not include interchange and assessment fees.  

 Q:  Why don’t I see the invoice number?   

 A:  The invoice number in Altura is coming. We are working hard to get this feature to you.  

 Q:  What is the order number?   

 A:  The order number and reference number are unique identifiers used by DIS in the backend and have no relevance to Quantum.  

 Q:  What is the reference number?   

 A:  The order number and reference number are unique identifiers used by DIS in the backend and have no relevance to Quantum.  

 Q:  Where can I get reports?   

 A:  Altura is the only place you can get daily, monthly, or yearly reports of your credit card transactions.  

 Q:  What is the difference between historical and deposits?   

 A:  Historical deposits are being phased out and will no longer be generated; this was an old format for daily deposits.  

 Q:  How do I sort transactions?   

 A:  Using the filters in Altura will enable you to sort transactions as needed.  

 Q:  How do I set the same date?   

 A:  When choosing the date range, you can select 1 date by clicking on it twice.  

 Q:  How do I download this list?   

 A:    The export button will allow you to download the data in Excel format.  

 Q:  How do I get an Excel of this list of transactions?   

 A:  The export button will download the list in an Excel format.  

 Q:  How do I reconcile transactions?   

 A:  The sale value will line up with the DP batch file (from Quantum) for that day. All deposits from DIS Pay are done as net deposits.  

 Q:  What is terminal setting?   

 A:  Terminal setting will allow you to change the name of each terminal.  

 Q:  How do I change terminal names?   

 A:  Log in to Altura, navigate to the DIS Pay window, select terminal setting, and then proceed to change the name.  

 Q:  How do I sort by terminal?   

 A:  Answer pending 

 Q:  Will a pending transaction go through?   

 A:  Pending transactions will have an associated successful, failed, or aborted transaction record.  

 Q:  If I have a hanging invoice, how do I close it?   

 A:  This invoice would need to be closed in the same way you would close a hanging invoice in Quantum.  

 Q:  How do I access Altura?   

 A:  You access Altura through Quantum or by using the link provided.  

 Q:  How do I give access to Altura?   

 A:  You can create users under user management in Altura; don’t forget to give users DIS Pay access.  

 Q:  Who needs access to Altura?   A:   

 A:  We recommend all users that will be processing credit card payments have access to Altura.  

 Q:  What permissions do I give to DIS Pay users?   

 A:  DIS Pay is the most important functionality to give to users.  

 Q:  Identifying sales opportunity.   

 A:  Any client that is not currently using DIS Pay.  

 Q:  What is Perseus Pay Outage?   A:   

 A:  This is when there is an issue on the Perseus pay side that is preventing our clients from transacting.  

 Q:  What is an Adyen Outage?   

 A:  This is an outage on the Adyen side that is preventing our clients from transacting.  

 Q:  What do we do if a client can't transact?   

 A:  Raise this issue with Sean immediately. Regardless of the time or the day, all non-transacting client issues need to be escalated.  

 Q:  Are Partial Payments/Partial Approvals taken in DIS Pay?   

 A:  NO. DIS Pay DOES NOT take Partial Approvals. The full transaction amount needs to be available on the card at the time of the transactions. Attempting a partial payment / partial approval will result in a return code for a failed transaction. 

 Q:  What should be done if PIN is requested for customer credit card and customer doesn't know PIN number?   

 A:  There is more than one option to resolve this issue at the current time: 

 Enter the card as a manual transaction.  
 If the transaction is under $250 dollars, the card has the option of Tap to Pay , and the customer has not already performed 3 Tap to Pay transactions on the current day, enter the transaction as a Tap to Pay transaction.