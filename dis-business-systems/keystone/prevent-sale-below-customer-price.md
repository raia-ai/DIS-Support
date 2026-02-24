---
title: "Prevent Sale Below Customer Price"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Prevent Sale Below Customer Price."
long_description: "This document provides information about Prevent Sale Below Customer Price from the DIS Keystone system."
---

## Introduction

Keystone allows you to set options that require salespeople to provide a password in order to sell a part below a price designated for a customer. This document covers how to set related options, set customer price, setup the password, and process a sale below customer price in Invoicing.

> **Note**: The Prevent Sales Below Cost option must be set in order to enable this option (Opt POS Menu 19).

## Set Option

This option requires salespeople to enter a password before selling a part/unit below the customer price, providing the customer price is greater than the part cost. If the price is less than the part cost, the Sale Below Item Cost gate will appear instead. The password is the same for both.

1.  Access **Point of Sale OPT Menu Sixteen** in Keystone (Security | OPT DIS Master Menu | Point of Sale | Click the Next Arrow until you reach Menu 16).

    

title: "Prevent Sales Below Cost"
source: "Prevent_Sales_Below_Cost.pdf"
tags: ["Keystone", "Point of Sale", "POS", "Sales", "Cost Control", "Password", "Security", "Reporting", "Invoicing"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "A guide for Keystone users on configuring options to prevent sales of parts or units below their cost. It covers setting up passwords, processing below-cost sales in invoicing, and generating related reports."
long_description: "This document provides detailed instructions for system administrators and managers using the Keystone software to manage sales pricing and prevent losses. It explains how to enable the 'Prevent Sale Below Cost' feature, which requires a password override for any transaction where the sale price is less than the dealer net cost. The guide walks through three key configuration areas: setting the primary prevention option, defining the scope (parts only, units only, or both), and establishing the override password. It includes step-by-step instructions for navigating to specific option menus (OPT Menu Nineteen and Twenty-Two) within the Point of Sale module. Additionally, it details how to set up override passwords in the Sales Margin Maintenance screen. The document also covers the practical application, showing a salesperson how to enter the password and authorizer name during invoicing when a below-cost sale is attempted. Finally, it explains how to configure automatic end-of-day reporting for below-cost sales and how to manually run the 'Sale Below Cost Report' at any time to audit these transactions."