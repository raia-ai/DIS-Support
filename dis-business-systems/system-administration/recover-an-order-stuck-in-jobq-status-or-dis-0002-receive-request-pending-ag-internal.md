---
title: "Recover an order stuck in JOBQ status or DIS-0002 Receive Request pending - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Recover an order stuck in JOBQ status or DIS-0002 Receive Request pending - AG Internal."
long_description: "This document provides internal system administration information about Recover an order stuck in JOBQ status or DIS-0002 Receive Request pending - AG Internal."
---

_Recovering an order stuck in JOBQ status or DIS-0002 Receive Request pending - AG Internal_

Introduction 

 Occasionally a job will get cancelled or the job queue will get cleared while an order receive is running. This leaves the order with a JOBQ status. 

 

  

 If the user tries to correct this order, they will get a message: DIS-0002 Order cannot be corrected because a receive request is pending. 

 

  

 Recovering an order stuck in JOBQ status. 

 Before you recover the order make sure there is nothing pending in the QBATCH or DISBATCH1 job queues. Recovering an order already in the queue will risk double receiving the order. 

 Type WRKJOBQ *ALL at a command line. 

 

  

 Once you’ve determined there are no other jobs pending go to Parts > Stock Order > Receive Order > Receive Order and enter the vendor and order number. 

 

 When you get the message that receipt is in progress (DIS-0002 Receipt is already in progress for  xxx.)  press F22 (Shift + F10) to kick start the order receipt process. 

 You’ll get a message: DIS-0001 Receive request for ‘order’ has been place on the job queue. 

 

  

 This will recover and receive your order.