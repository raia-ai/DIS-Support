---
title: "EMV Credit Card Instructions"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about EMV Credit Card Instructions."
long_description: "This document provides information about EMV Credit Card Instructions from the DIS Keystone system."
---

## INTRODUCTION

This document provides instructions for the processes involving EMV credit cards, including how to:

- Create Tokens for EMV credit cards in Receivables Maintenance or Address Maintenance
- Process EMV credit cards in P.O.S. and capture a Token
- Use a Token to pay for a transaction
- Pre-Authorize available funds
- Process a refund for a return
- Get a manual authorization for a transaction

## Create EMV Credit Card Tokens

Credit Card numbers are no longer going to be stored on your system. Instead, tokens will be created and saved that can be used for processing transactions at a later time. Tokens can be created and saved using Receivables/Address Maintenance.

1.  Select Receivables Maintenance (Accounting | Receivables Maintenance) or Address Maintenance (Marketing | Address Maintenance) from the Keystone main menu.
2.  Click the **Credit Cards** button. The Credit Cards screen opens.
3.  Click in the **Card** column and type your dealership defined code for the credit card.
4.  Click **Enter**. A screen opens prompting "When prompted, enter the card number on the pinpad device."
5.  When prompted on the card reader, manually type the credit card number into the card reader and press **Enter** on the keypad.
6.  When the token has been added, a message will appear at the bottom of the credit cards screen stating that the Token has been added.

## Process a Purchase and Create a Token with a New Card (Card Present or Not Present)

1.  When you have added all of the goods and services to an invoice and clicked the **Print and Close** button on the Document Detail screen in Invoicing, the Credit Card Authorization screen opens if there are not any tokens saved for the customer.
2.  Select the **Card present** (If the card is present) and **Capture card token** check boxes and click **Enter** on the Keystone tool bar. If the card is not present, leave the Card present check box unselected.
3.  The "Authorizing. Please wait..." screen opens.
4.  Slide the card into the card reader (if it is on hand) or type the number into the card reader using the keypad (if the card is not on hand) and press **Enter** on the keypad.
5.  When providing the card for the first time, the card reader may display a "Select application" screen.
    -   Select **Visa Debit** to run the card through as a credit card.
    -   Select **US Debit** to run the card through as a debit card. A pin number will be required.
6.  The Authorization screen opens displaying the Authorization Number.
7.  Click the **Continue** button. If configured to do so, the Signature Capture screen opens.
8.  Click the **Capture** button to capture the signature. The signature is archived with a copy of the invoice. The DIS Signature Capture screen opens displaying the customer signature and verifying the customer has accepted.
9.  Click the **Accept** button. The transaction is completed and a token for the credit card has been saved and will be available to use on the customer's next purchase.

## Process Transaction with Token

Once you have created and saved a token for a customer's credit card, you can use it to process customer transactions. Though the credit card number is no longer stored in the system, the last four numbers of the card that the token represents is displayed. You can verify this is the card the customer wants to use by asking if the numbers on the screen match the card.

1.  When you have added all of the goods and services to the invoice and clicked the **Print and Close** button on the Document Detail screen in Invoicing, the Credit Card Authorization screen below opens if a token for the card exists. The screen will state "This transaction will be using the token for the card displayed" and show the card number as `****************1234`.
2.  Ensure the numbers displayed on the screen match the card the customer wants to use and click **Enter** on the Keystone tool bar.
3.  The "Authorizing. Please wait..." screen displays momentarily.
4.  Then the following screen opens displaying the authorization number.
5.  Click the **Continue** button. If configured, the Signature Capture screen opens.
6.  Click the **Capture** button to capture the signature. A copy of the signature is archived along with a copy of the invoice. The DIS Signature Capture screen opens displaying the customer signature and verifying the customer has accepted.
7.  Click the **Accept** button. The transaction is completed.

## Pre-Authorize Funds Required for Payment/Future Purchase

If you want to ensure a customer can cover the cost of goods and services or pre-authorize funds for a future purchase, you can create a pre-authorization. If the pre-authorization of funds is granted, a hold will be placed on the money. American Express holds pre-authorization funds for 7 days and all other credit cards hold the funds for 30 days. As long as the invoice remains open, you can cancel the pre-authorization and remove the hold at any time. Pre-Authorization of funds can be established in person or over the phone.

1.  When you have added all of the goods and services to the invoice and clicked the **Print and Hold** button on the Document Detail screen in Invoicing, the Credit Card Authorization screen opens if a token for the card does not exist. (If a token for a card is on file only the Pre-Authorize? check box will display.)
2.  Ensure the amount you would like to pre-authorize is displayed in the amount field and select the **Pre-Authorize?** check box.
    > **Note:** The Card present check box cannot be selected when doing a pre-authorization. You can capture a token for the card by selecting the Capture card token check box.
3.  Click **Enter** on the Keystone tool bar.
4.  The following screen opens if the Card present check box was not selected, prompting you to "Enter the billing address of the card being used."
5.  Verify with the customer that the street address and zip/postal code are correct, then click **Continue**.
6.  The "Authorizing. Please wait..." screen opens.
7.  Punch the credit card number into the card reader and click **Enter** on the keypad.
8.  The following screen opens displaying the Authorization number.

## Process a Refund for a Return

When providing a refund for a return, a transaction is processed for a negative amount equal to the original charge on the card.

1.  After you have created an invoice for a negative amount that is equal to the refund amount on the Document Detail screen and clicked the **Print and Close** button, the Credit Card Authorization screen opens.
2.  Ensure the amount displayed is the amount that you would like to refund to the customer and that the last four digits of the card number match the card they want to credit. Click **Enter** on the Keystone tool bar.
3.  The "Authorizing. Please wait..." screen opens momentarily.
4.  Then the Authorization screen opens displaying the Authorization Number.

## Get a Manual Authorization

In the event of a power failure or any other instance where you cannot use your card reader to get an authorization number for an EMV card transaction, you can contact Gravity Customer Service for a manual authorization.

1.  Contact Gravity Customer Service at 866-701-4700 and select Option 1 to receive an authorization code.
2.  Click the **Auto/Manual Auth** button on the Credit Card Authorization screen and type the authorization code you received from Gravity in the **Auth Code** field that appears. Click **Enter**.