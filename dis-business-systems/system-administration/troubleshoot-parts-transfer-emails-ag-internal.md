---
title: "Troubleshoot Parts Transfer Emails - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Troubleshoot Parts Transfer Emails - Ag Internal."
long_description: "This document provides internal system administration information about Troubleshoot Parts Transfer Emails - Ag Internal."
---

Issue 

 The emails that are sent after each step during divisional transfer as detailed below have issues or are missing.   

  

 Transfer Steps and Emails that Should be Sent 

 When Division A opens a request for a parts transfer, two Emails are sent: 

 Division A  - Receives email that says they requested parts from Division B. 

 Division B – Receives an email that Division A is requesting part(s). 

 These emails are put in a queue and the Utilservlet moves the emails to the MailGun server to send. This can take up to 15 or more minutes. 

 Division B accepts or denies the parts transfer request.  

 Division A – Receives an email with the accept or deny message. 

 These emails are put in a queue and the Utilservlet moves the emails to the MailGun server to send. This can take up to 15 or more minutes. 

 If Division B transfers the part, they mark the transfer as shipped.  

 Division A – Receives email with the Shipped message 

 These emails are put in a queue and the Utilservlet moves the emails to the MailGun server to send. This can take up to 15 or more minutes. 

 If the 3 steps above are not followed and shortcuts are taken, then some or all the emails WILL NOT be sent.  If Division A makes a request and Division B checks the parts transfer queue and accepts the transfer before the request, then the 2 request emails WILL NOT be sent as MailGun will believe that the emails were sent already.  If Division B marks the parts transfer as Shipped before any of the other emails were delivered, then MailGun WILL ONLY send the Shipped email as it thinks the others were already sent. 

 Solution 

 Select Configure Parts Daily Transfer (Parts | Parts Configuration | Configure Parts Daily Transfer) and record the email addresses assigned to both divisions involved with the part transfer. 
 Login to MailGun and search Logs for the email addresses. 
 Advise dealer what needs to be done. 

 Related Support: 

 Ken Guy supports the MailGun server 
 Dave Willingham can support questions about some of the errors you may see in MailGun logs relating to SPF or DMARC or DKIM records on the DIS side. 

  

 Related Articles: 

 https://perseus.my.site.com/DISSupportPortal/s/article/Configure-System-for-Parts-Transfer-Quantum 

 https://perseus.my.site.com/DISSupportPortal/s/article/Transfer-Parts-from-Another-Division-in-POS-Quantum 

 https://perseus.my.site.com/DISSupportPortal/s/article/Processes-to-Complete-After-Adding-a-New-Division-Quantum