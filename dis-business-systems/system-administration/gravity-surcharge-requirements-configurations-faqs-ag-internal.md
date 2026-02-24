---
title: "Gravity Surcharge Requirements, Configurations, & FAQs – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Gravity Surcharge Requirements, Configurations, & FAQs – Ag Internal."
long_description: "This document provides internal system administration information about Gravity Surcharge Requirements, Configurations, & FAQs – Ag Internal."
---

Requirements  

 Dealerships interested in Gravity Surcharging should begin by contacting Gravity directly via this website to book a meeting with a Gravity representative: https://gravitypayments.com/lp/surcharging-dis/ .   

 Once the dealership has completed the meeting with a Gravity representative and completed the process provided Gravity, there is a 30-day registration period that begins at the start of a new month. They must register before the feature can be activated.   

 The surcharging feature is divisional. Gravity will inform DIS which dealership location(s) need to have the feature configured.   

 To qualify for Gravity Surcharging, the dealer must:  

 Be set up with Quantum  
 Be on business system version DIS_N114 or higher  
 Be set up with Gravity emergePay (surcharging is not compatible with Gravity 1.0)  

  

 Configurations  

 Create a new sales code for the Gravity surcharge and consider/complete the following: 

 The sales code is used to automatically add the Gravity surcharge onto Point of Sale documents and must be assigned the Miscellaneous Description format.   
 It is recommended to set the Debit for the Sales Code to *AUTO.  The Credit is usually set to a credit card fee expense account.  
 The dealer should consider setting up a sales code that will print at the bottom of the invoice since the detail lines on a Point of Sale document print in sales code order ( Example: 99). 
 The dealer needs to let DIS know what sales code(s) they set up so that it can be mapped appropriately to each division.   
 The mapping configuration is found in SAMSVCT. The SVCCCS field should be updated with the sales code. 

 Review the hierarchy the system uses to choose the appropriate tax code, and create a new tax code if needed. Note that: 

 The Gravity surcharge must be tax exempt. The following hierarchy is followed to decide the appropriate tax code:  

 Basic Tax  

 The system will first look for an override tax code on the mapped surcharge sales code  
 If there is not an override tax code on the sales code or the override tax code is not tax exempt, the system locates and uses an exempt tax code with the description of “CC SURCHARGE”. 
 If a tax code with the above description is not found, or the tax code with the above description is not tax exempt, the first exempt tax code (based on description) is used. 

 Advanced Tax and DBST  

 The system looks for the default tax code for the Point of Sale invoice first, and if there is a configured sales code override (on the sales code set up for the Gravity surcharge), the default tax code is used  
 If there is not a sales code override set up, or the sales code override is not a tax rate of 0, the system locates and uses an exempt tax code with the description of “CC SURCHARGE”  
 If a tax code with the above description is not found, or the tax code with the above description is not tax exempt, the first exempt tax code (based on description) is used. 

 Update Laser Forms to include a disclaimer stating the customer may incur a surcharge if paying by credit card. To ensure that the dealership is compliant with card brand guidelines for surcharging, they need to: 

 Add messaging to their Point of Sale Laser Forms that indicates that a surcharge of x % may be applied to credit card transactions, where x is a percentage value between 1 and 3.   

 For Example : “A surcharge of _% will be added if you elect to pay with a credit card, which we assess to cover our cost of acceptance. No surcharge will be added if you elect to pay with a debit card.”  

 Make the disclaimer clearly visible in the same font size as the detail lines on the Point of Sale document.   

 Any Automatic Point of Sale Charges have already been set up to calculate and charge a credit card surcharge should be removed prior to going live with Gravity Surcharges.  

  

 FAQs  

 Q : What should be done if a refund needs to be processed once surcharging is turned on?  

 A : Follow these guidelines for processing refunds:  

 The money must be returned using the same payment method as the original sale. (For example, if the customer originally paid cash, they must be given back cash. The refund cannot be put onto a credit card.)  
 If the original sale contained a surcharge, the surcharge must be refunded.   
 If the original sale did not contain a surcharge, the refund needs to be processed on the device itself. If the refund is processed via the device, the exact amount that is input will be refunded – it will not modify it and add a surcharge.   
 Only process refunds via the device if the original sale did not result in a surcharge.   

 Q : Can the surcharge percentage be modified?  

 A : Yes, the surcharge percentage can be modified (lowered). Contact your Gravity representative directly for any modification requests.   

 Q : Can surcharging be disabled for specific customers?  

 A : No. Card brand rules and “fair play” laws prevent this.   

 Q : The customer is using a debit card, but a surcharge was calculated. Why?  

 A : Every card has a Card Issue Type and a Card Subtype. The Card Issue Type takes priority and is identified within the first six digits of a card number. It is possible that a debit card has a credit Card Issue Type. If this is the case, a surcharge would be calculated. For any questions related to why a surcharge was calculated, contact Gravity Support ( support@gravitypayments.com ).   

 Q : The customer is using a credit card, but a surcharge was not calculated. Why?  

 A : There could be a few reasons why a credit card wouldn’t be eligible for a surcharge. Every card has a Card Issue Type and a Card Subtype. The Card Issue Type takes priority and is identified within the first six digits of a card number. It is possible that a credit card has a debit Card Issue Type. If this is the case, a surcharge would not be calculated. Additionally, some states/territories prohibit the practice of surcharging. If the cardholder’s billing address is from a state or territory that does not allow surcharging, the transaction will be processed without a surcharge. For any questions related to why a surcharge was not calculated, contact Gravity Support ( support@gravitypayments.com ).  

 Q : Can the surcharge be set to be taxable?  

 A : No, the surcharge must be tax exempt. The document total is already calculated by the time that total is sent to Gravity. The surcharge is then calculated and added onto the document, and the document is immediately closed. Additional tax on the surcharge line would result in a change to the document amount and cause the customer to need to process their card again, which would then cause a higher surcharge amount. This would cause a race condition – surcharge, tax, surcharge again, tax again, etc.    

 Q : Will the credit card reconciliation process change because of implementing surcharging?  

 A : Yes, the credit card reconciliation process changes once surcharging is turned on. This depends upon the surcharge sales code setup.   

 If the surcharge sales code is set to Credit a credit card fee expense account, a debit is posted to the same expense account for the surcharge amount once funding is received.   

 Review the example below:  

 An initial sale is $10. With a 3% surcharge, the total charged to the customer’s card is $10.30:  

 Initial Tota l:  $10.00  
 Surcharge :    $  0.30  
 Grand Total :  $10.30  

 If the initial sale was a charge ticket, the posting batch would include the following transactions:  

 

 Once the funding is received and the reconciliation is ready to be processed, the settlement posting batch would include the following transactions:  

 

 Important! This is just an example. DIS recommends consulting an accountant should any questions arise on the proper way to post credit card settlements with surcharging.