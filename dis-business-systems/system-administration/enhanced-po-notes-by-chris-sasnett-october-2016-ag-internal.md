---
title: "Enhanced PO Notes by Chris Sasnett October 2016 - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Enhanced PO Notes by Chris Sasnett October 2016 - Ag Internal."
long_description: "This document provides internal system administration information about Enhanced PO Notes by Chris Sasnett October 2016 - Ag Internal."
---

_Enhanced PO Notes by Chris Sasnett October 2016 - Ag Internal_

This document was written by Chris Sasnett in (October of 2016) 
 It was written to help understand the behind the scenes information about Purchase orders.
  
  
  
 Notes concerning Part receipts for Stock Orders and Purchase Orders: 
  
 Three Opt switches control the interaction between Stock Orders and Part Receipts . . .
  
 Menu X6343 
   1. Post PO's with a single posting process
 POAPOST               2. Post PO's with a double posting process            
                                                                            
   3. PO numbers are not linked to inventory orders
 POALINK               4. PO numbers are linked to inventory orders          
                                                                            
   5. Parts on PO's are NOT received if also Stock Ordered
 POAPART              6. Parts on PO's WILL be received if also Stock Ordered
  
  
  
 For the PO application, the "P" format purchase code was originally intended for adding parts onto a PO and then receive part quantities into inventory when the PO is posted.
  
 With Enhanced Purchase Orders (PO), Stock Orders (SO) may be linked to PO’s (POALINK). 
 When the SO is finalized it auto-creates a PO.
 The SO is renamed to have the same Order number as the newly created PO.
 A single (misc.) line item is added onto the PO with the total cost of the SO.

  
 When the parts order is received, the SO is processed and adds the part quantities into inventory.  Then the PO is closed/ posted which updates the G/L for part receipt cost.  
  
 However, a few customers insisted on using these applications in alternative ways. 
 They create and finalize an SO, which auto-generates a PO.
 Then they update the PO. They delete the Misc line.
 Then they manually re-enter the part lines (with a “P” format Purchase Code).

 
 They receive the SO and then close and post the PO.
 This was creating a double receipt of the parts (SO + PO).

  
 Another scenario that caused issues resulted from increasing the quantities for parts on a finalized SO, by adding these parts onto the PO too (i.e. SO qty 3 + PO qty 2 = 5).
  
 Therefore, this program must delineate between folks who...      
 Create a SO + PO but only have parts to receive on the SO.
 Create a PO (no SO), with multiple part lines. Where the same part# may be on the PO as separate line items.  This happens because each of the lines may be setup as resale to separate POS invoices (i.e. The same part being ordered for different customers). 
 Create a SO + PO where the parts are present on both, and the receipt should only occur based on the SO (not the PO).
 Create a SO + PO where additional parts are added to the PO (which are NOT on the SO), and the customer wishes both to receive their relative part quantities.

  
 The process is to check the Opt switches (above) against the part lines on the PO to be received against OAA/OAM and OAH/OAMH. 
  
 Note: Parts on a PO may be processed before (OAA/OAM), or after (OAH/OAMH) the SO receipt.
  
  
  
  
   
 Tars that relate to the development and evolution of the current solution : 
  
 Tar: SC400 844367
      ------                                                                        
 Stock Orders "Linked" to PO's...                                             
 -----------------------------                                                
 The concept of a linkage between these two applications is more "Virtual" than
 "Real".  If you create a Stock Order (or Priority Order) and Finalize it, the
 original Order number (in OAM, OAA and u.IBM) is renamed to the next PO#. Then
 an open PO (for that number) is created and one detail line is added that will
 include the current Cost of the Order.  At this juncture, the only "Linkage" 
 is that they both share the same PO#. That's it!  You must process the PO and
 the Stock Order as separate activities, although the receipt of Parts is done
 by the SO and the posting of Cost to the G/L is supposed to be done by the PO.
 .                                                                            
 Receiving PO's with "P" format Purchase Code line items (aka: Parts)...      
 --------------------------------------------------------------------         
 Here are my notes from the X55116 posting program that handles the PO:       
   *  The "P" format purchase code was originally intended for receiving      
   *  parts into inventory. With the release of Enhanced PO's another         
   *  solution was created so that stock orders could auto-create a PO        
   *  with a single line (misc.) to represent the total cost of receipt.      
   *  However, a few customers insisted on doing both!  They create a         
   *  stock order that generates a PO, then they alter the PO to manually     
   *  add part lines.  This was creating a double receipt (SO + PO).          
   *                                                                          
   *  This section is intended to delineate between folks who...              
   *  1) Create a SO + PO but only want to receive the parts on the SO        
   *  2) No SO, but they create a PO with part lines and receive during X55.1 
   *  3) POAPART=1 ... allow parts to be received regardless.                 
 .                                                                             
 It's complicated, but let me try to break it down...                         
  
  > POALINK opt = PO numbers are linked to inventory orders                 3-4
  > POAPART opt = PO part lines will NOT be received if also on Stock Order 3-5
                                                                             
 The 2nd Opt (POAPART) only comes into play if the 1st Opt (POALINK) is seton.
              -------                                       -------                                                                               
  
 The PO posting routine (X55116) is trying to add PO part lines to OAM and OAA.
 Later in this process, the stock order receipt programs will be called to do 
 the actual receipt to inventory.  Therefore we need to assess whether these PO
 part lines should be added into OAM/OAA or not!  We don't want this process to
 double receive parts if they are on a Stock Order AND a PO, etc.             
 .                                                                             
 Note that the only time we SUPPRESS receiving the PO Part lines is when:     
   POALINK = 1 and POAPART = 0 and the Order# + Part# are in OAA or OAH.      
 .                                                                            
 In this case, where the part is on the PO twice, the first part would get Rcvd
 and the 2nd line for this part will get skipped, because the first line had  
 already just been added to OAA.  Sheesh!                                     
 .                                                                            
 If they are going to continue with their current practice of using PO's to add
 Part Lines for Receipt, I suggest they set the POAPART Option ON.  This will 
 force the PO posting routine to receive the Parts REGARDLESS whether the Order
 exists as an OLD order, or the Part is listed more than once on the PO itself.
  
 Note :
 Ultimately, the program responsible for this process is:  DIS28202/QRPGLESRC/ X55116 
  
  
   
 Notes on the processing of transactions in the POT file : 
  
 When a PO is closed and posted the detail lines being processed are consolidated in the CSD batch (much like a POS batch). The resulting lines are captured in the POT file.
  
 The “Stmt#” column (field: PSTMT) is assigned as the POT entries are created (i.e. They do NOT specifically relate to the PO line number). 
  
 The “ATE” column (field: PFLAG) represents a flag for the entries where . . .
 “A” is the Accrual entry (comes from the PO purchase code credit account)
 “T” is the Tax transactions based on the Tax code used on the PO
 “E” if the Exchange Opt is seton (POAEXCH) and configured in PO Divisional Profile
  
 The “F” column (field: PPOST#) reflects the status of the PO where . . .
       “1” POT entries where the Accrual still has an Unapplied balance > 0
       “A” POT entries where the Accrual has an Unapplied balance = 0
       “B” POT entries for invoice allocations applied against the original entries
  
 Note: If a PO is partially closed, intial entries for the PO are added to POT. 
 If additional lines are closed for the same PO, and the POT file Accrual entry is
 still “active” (i.e. PPOST# = 1), then the additional PO entries are ADDED to the current POT entries (and the Accrual line is updated with the new Unapplied balance.
 Notice the transaction dates between Stmt# 20 and 30 bleow reflects this scenario.
  
 If the original POT entries are fully applied (PPOST# = A), when the second close occurs for this PO, then a brand new set of entries are created in POT and the original entries remain intact. 
  
 F ATE Stmt# Document#  Vendor  Date  D/C Account  Description      Amount     Applied   Unapplied 
 1  A  00010 PO00079 $% BATT01 062916  C  A2100                      46.50         .00       46.50 
 1     00020 PO00079 $% BATT01 062916  D  A6590    PMS               21.00         .00       21.00 
 1     00030 PO00079 $% BATT01 070916  D  A6710    PMS               10.00         .00       10.00 
 1     00040 PO00079 $% BATT01 070916  D  A6720    PMS               12.00         .00       12.00 
 1  T   00050 PO00079 $% BATT01 070916  D  A2705    PMS                3.50         .00        3.50 
  
  
  
  
 In Payable Invoice Entry, when a Vendor Invoice is entered (INV-79) the user may press the “F6” key to list PO’s available for selection.  POT file PO’s for this vendor, where the Accrual entry has an Unapplied balance will be listed.  All of the POT entries for the PO are represented on the PO allocation screen, EXCEPT for the “Accrual” (where ATE = A). 
 Whatever is entered onto the PO Allocation screen is captured and added to the PO file with a PFLAG = “B”.  The vendor invoice number is captured in the desceription field.  Any of the original PO entries which are applied against the invoice, as well as the “Accrual” entry are updated with changed values for “Applied” & “Unapplied” balances.
  
   
  
  
 One vendor invoice may not resolve the balance of a PO.  In this case the PO may be applied against a second vendor invoice (or more).  The process is repeated, where the applied lines create PFLAG = “B” entries and the Applied/Unapplied balances for the original POT entries are updated.  Until the PO is eventually fully applied (Unapplied = $0 on the Accrual).
 Once the original PO entries are fully applied the PFLAG is changed from “1” to “A”.
  
 F ATE Stmt# Document#  Vendor  Date  D/C Account  Description      Amount     Applied   Unapplied 
 A  A  00010 PO00079 $% BATT01 062916  C  A2100                       46.50       51.75          .00 
 A     00020 PO00079 $% BATT01 062916  D  A6590    PMS               21.00       25.00         .00 
 A     00030 PO00079 $% BATT01 070916  D  A6710    PMS               10.00        6.00         .00 
 A     00040 PO00079 $% BATT01 070916  D  A6720    PMS               12.00       16.00         .00 
 A  T   00050 PO00079 $% BATT01 070916  D  A2705    PMS                3.50        4.75         .00 
  
 B     00000 PO00079 $% BATT01 071216  D  A6710    INV-79             6.00         .00         .00 
 B     00000 PO00079 $% BATT01 071216  D  A6720    INV-79            11.00         .00         .00 
 B     00000 PO00079 $% BATT01 071216  D  A2705    INV-79             2.00         .00         .00 
  
 B     00000 PO00079 $% BATT01 080316  D  A6590    INV-82            25.00         .00         .00 
 B     00000 PO00079 $% BATT01 080316  D  A6720    INV-82             5.00         .00         .00 
 B     00000 PO00079 $% BATT01 080316  D  A2705    INV-82             2.00         .00         .00 
  
  
 Enhanced PO – SQL statements that may be helpful . . . 
  
 Display records for one PO:
 --------------------------
 DISSQL REQUEST('SELECT PFLAG AS A, PPOST# AS P, PSTMT AS LINE, PPO# AS
 DOCUMENT, PPOVEN AS VENDOR, DIGITS(PTRDT) AS DATE, PDORC AS DC, PACCT AS
 ACCOUNT, PNET AS POSTED, PAPPL AS APPLIED, PUNAP AS UNAPPLIED, PDESC AS
 DESCRIPTION FROM FILEx/POT WHERE PPO# = ''BS00256 '' ORDER BY 2, 3')
  
 A  P     LINE  DOCUMENT  VENDOR  DATE    DC  ACCOUNT          POSTED        APPLIED      UNAPPLIED  DESCRIPTION 
 -  -  -------  --------  ------  ------  --  --------  -------------  -------------  -------------  ------------ 
 A  1      10   BS00256   007416  021210  C   K2103S          445.52          93.08         352.44               
    1      20   BS00256   007416  021210  D   K13015          445.52          93.08         352.44   STK         
    B       0   BS00256   007416  021610  D   K13015           93.08            .00            .00   1743599     
  
 Display records for all unposted PO’s with calculated NET and VARIANCE:
 ----------------------------------------------------------------------
 DISSQL REQUEST('SELECT PPO# AS DOCUMENT, PPOVEN AS VENDOR, DIGITS(PTRDT) AS
 DATE, PACCT AS ACCOUNT, PNET AS POSTED, PAPPL AS APPLIED, (PNET-PAPPL) AS NET,
 PUNAP AS UNAPPLIED, (PNET-PAPPL-PUNAP) AS VARIANCE FROM FILEx/POT WHERE
 PFLAG = ''A'' AND PPOST# = ''1'' ORDER BY 1') 
  
 DOCUMENT  VENDOR  DATE    ACCOUNT          POSTED        APPLIED             NET      UNAPPLIED         VARIANCE 
 --------  ------  ------  --------  -------------  -------------  --------------  -------------  --------------- 
 BG00183   001683  012510  K2103G           13.51            .00           13.51          13.51              .00 
 BG00202   001683  020210  K2103G           97.00            .00           97.00          97.00              .00 
 BG00293   001683  040910  K2103G          222.64            .00          222.64         222.64              .00 
 BG00326   001683  032410  K2103G          808.09         587.09          221.00         221.00              .00 
 BG00334   002216  032510  K2103G           37.52            .00           37.52          37.52              .00 
 BG00335   001683  032610  K2103G          599.21          39.95          559.26         559.26              .00 
  
 Display records for one PO from BAA:
 -----------------------------------
 DISSQL REQUEST('SELECT BAPO# AS PO#, BAPSC AS PSC, BAFRMT AS FMT, BALINE AS
 LINE, BABILL AS R, BAPVEN AS VEN, BAQTY AS QTY, BADESC AS PART#, BAGDOL AS
 EXTPRICE, BABSC AS SC, BAPDAT AS PDATE FROM FILEx/BAA WHERE BAPO# = ''PK00478 ''')                                                   
  
 Display records for Unapplied PO’s joining POT and BAM:
 ------------------------------------------------------
 DISSQL REQUEST('SELECT PDIV AS DIV, PPO# AS DOCUMENT, PPOVEN AS POTVEN,  
 DIGITS(PTRDT) AS DATE, PNET AS POST$$, BMVEND AS BAMVEN, BMPOST AS OCP,
 BMSTAT AS STATUS, DIGITS(BMPDAT) AS POSTED FROM FILEx/POT LEFT JOIN
 FILEx/BAM ON PPO# = BMPO# WHERE PFLAG = ''A'' AND PPOST# = ''1'' ORDER BY 2')