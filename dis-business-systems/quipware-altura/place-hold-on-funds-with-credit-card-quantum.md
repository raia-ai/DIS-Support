---
title: "Place Hold on Funds with Credit Card - Quantum"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Place Hold on Funds with Credit Card - Quantum."
long_description: "This document provides information about Place Hold on Funds with Credit Card - Quantum from the DIS Salesforce Knowledge Base."
---

_Place Hold on Funds with Credit Card - Quantum_

Introduction 

 You can place a temporary hold on a customer’s credit card for a specific dollar amount using a credit card pre-authorization (pre-auth) with card is EDC (Electronic Data Capture) capable. The hold ensures that funds remain available, but the card is not charged until the ticket is actually closed. The hold lasts for about a week with most cards, but varies based on the issuing credit card company. 

 When a pre-auth is performed: 

 The ticket is authorized and the authorization number appears in Altura as a CreditAuth. 
 The ticket remains open in Quantum. 

 Pre-auths are useful for guaranteeing payment when the final amount may change. If the ticket total changes, the pre-auth can be adjusted to reflect the final amount. The pre-auth can also be cancelled if another form of payment is to be used. 

  

 Pre-Authorize a Card 

 Create the invoice in Point of Sale, select the Navigation button, and click the Prt & Cls button. 
 On the Credit Card Authorization screen, select the Pre-authorize checkbox. 

 

 Click Enter . This procedure places a hold on the funds without charging the card and the ticket remains open in Quantum. The pre-authorization number appears in Altura as a  CreditAuth as shown below, confirming that the card has been pre-authorized. 

 

   

 Close a Ticket with a Previously Authorized Card 

 Open the ticket in Point of Sale. 
 Review the ticket total. If it differs from the pre-authorized amount, the system shows both the previously authorized amount and the new total to authorize. 

 

 Press Enter to capture the pre-auth for the final amount. The previously entered card information is used to process the transaction. 

 

 The transaction appears in Altura as a tokenizedForce entry as shown above, indicating the pre-auth was captured and the card charged. 
 If the customer is paying with a different method, you can cancel the pre-auth before closing the ticket using the Cancel Pre-Auth option on the left side of the screen (see below). 

 

 This ensures that the card is only charged for the correct final amount and avoids declined transactions due to mismatched amounts.