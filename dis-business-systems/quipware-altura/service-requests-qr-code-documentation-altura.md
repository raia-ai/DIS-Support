---
title: "Service Requests (QR Code) Documentation - Altura"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Service Requests (QR Code) Documentation - Altura."
long_description: "This document provides information about Service Requests (QR Code) Documentation - Altura from the DIS Salesforce Knowledge Base."
---

Introduction 

 The Service Requests QR Code feature allows you to present customers with a scannable QR code which opens an application to collect contact and authorization information when they bring their service vehicle for maintenance. The service request information is imported into Altura allowing you to quickly generate a work order with the information provided. This article details how to configure the Service Request feature in Altura once you have purchased the license and generate a work order from a service request in Altura. 

  

 Enable Service Request & QR Code Permissions 

 The Service Request and QR Code permissions must be enabled to use this feature. 

 Access Altura . 

 

 Select Roles and Permissions (Admin Settings | Staff Users | Roles & Permissions) . 

 

 Scroll down the page and enable the Service Request options. 

 

 Scroll down and select the Tools caret, then enable the QR Configuration Service Request options. 

 Add Service Request Statements 

 Select Service (Admin Settings | Configuration | Service). 

 

 Select Service Requests. 
 In the Approval Limit Text field, enter a repair dollar limit statement like the following to allow work to be completed below a specific dollar amount if the customer approves: 

 Select Yes below if you approve repairs under 1500.00 to be completed without contact and require an estimate and approval for repairs over $1500.00. 

 In the Authorization/Disclaimer Text field, enter an authorization statement like the following which will display above where the customer signs: 

 I hereby authorize repairs under $1500.00 to be completed without contact. 

 Click Save . 

 Generate QR Code 

 Select QR Code (Tools | Communication | QR Code). 

 

 Click on the drop-down arrows and select: 

 Service Request 
 The Sub Type 
 The File set or Company providing the service 
 The Division or Branch providing the service 

 Click the Create button. The QR code displays. 

 

 Click the Download button, print out the QR code, and post it where customers can easily locate it when dropping off service vehicles. 

 When the customer scans the QR code, they will be presented with the Service Request form shown below. 

 Note : The Service Request screen is broken down into multiple screenshots below, but it is a single scrolling screen in the application. 

      

 When the customer provides their information and clicks the Submit button: 

 A Success message displays if the request is successfully submitted 
 A Service Request is created in Altura 
 The customer receives a confirmation email 

 Process Service Request / Generate Work Order in Altura 

 

 Select Service Request (Service | Service Request). 
 New service requests have an OPEN status. Click anywhere on the service request line. 

 The Create Work Order screen displays the information provided by the customer listed on the left side and the generated work order which needs to be completed on the right side of the screen. 

 

 Enter the work order details in the fields provided. You must enter information in fields with an asterisk*. Where applicable, click the drop-down arrows to select from available options. 
 Click the Create WO button. 

 The Service Request is processed, the work order is generated, and the provided details display on the screen that opens. The status changes from OPEN to COMPLETE signaling the work order has been successfully generated. 

 

 Click the hyperlinked Work Order Number to access the work order details screen. 

 

 Click the View Details button to access the work order.