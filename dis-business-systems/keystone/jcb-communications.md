---
title: "JCB Communications"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about JCB Communications."
long_description: "This document provides information about JCB Communications from the DIS Keystone system."
---

## Introduction

JCB Communications allows you to maintain a consistent inventory level for JCB parts through part file transfers between your dealership's system and JCB. You can specify the vendor/code combinations to consider when generating the part files, submit files to generate suggested orders immediately or during nightly backup, resend files that failed during submission, and specify customers whose sales transactions you don't want to consider when generating suggested stock orders.

## Configure JCB Communications

In order for your system to communicate with JCB and transfer the files necessary to maintain desired part inventory, configuration will need to be completed. Setup will be completed with DIS assistance.

1.  Select **Electronic Commerce Configuration** (Security | Electronic Commerce | Electronic Commerce Communication). The Electronic Commerce Communication screen opens.
2.  Click the **Add** button. The Add Vendor/Comm Package screen opens.
3.  Provide information in the available fields and click **OK**. The JCB Communications - Configure screen opens.

    

title: "Keystone_EMV_Documentation"
source: "Keystone_EMV_Documentation.pdf"
tags: ["Keystone", "EMV", "Credit Card", "Tokenization", "Payment Processing", "Point of Sale", "POS", "Gravity Payments", "DIS"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "This document provides step-by-step instructions for handling EMV credit card transactions within the Keystone system. It covers creating tokens, processing purchases with new cards and existing tokens, pre-authorizing funds, processing refunds, and obtaining manual authorizations."
long_description: "This document is a user guide for the Keystone software, specifically detailing procedures for processing EMV credit card transactions. It addresses the shift from storing credit card numbers to using secure tokens for enhanced security. The guide provides step-by-step instructions for various common scenarios encountered by users. These scenarios include: 1) Creating and saving credit card tokens in Receivables or Address Maintenance without an immediate transaction. 2) Processing a purchase with a new card (whether the card is physically present or not) and simultaneously creating a token for future use. 3) Using a previously saved token to quickly and securely pay for a new transaction. 4) Pre-authorizing funds on a credit card to place a temporary hold for a future purchase or to ensure funds are available. 5) Processing a refund for a return transaction using a saved token. 6) Obtaining a manual authorization code from Gravity Customer Service in case of system or reader failure and applying it to a transaction. The instructions are accompanied by descriptions of the Keystone interface, guiding the user through each screen and action required to complete the processes successfully."