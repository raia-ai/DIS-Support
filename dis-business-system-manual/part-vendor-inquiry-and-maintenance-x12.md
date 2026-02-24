---
title: "PART: VENDOR INQUIRY AND MAINTENANCE (X12)"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about PART: VENDOR INQUIRY AND MAINTENANCE (X12)."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on PART: VENDOR INQUIRY AND MAINTENANCE (X12)."
---

---

## Page 1

## CHAPTER X12-1

VENDOR INQUIRY

### Introduction

Vendor Inquiry allows you to review vendor information including current
and history transactions. Vendor information is set up in Vendor
Maintenance (X12-2). Transactions are posted by Invoice Entry (X12-5),
Cancel Invoices (X12-6), Print Payable Checks (X12-7), Enter Manual
Checks (X12-8), Create Source Documents (X1-7), or Post Point of Sale
Documents (X55-2).

Fields displayed on the Inquiry and Maintenance screens are described in

## CHAPTER X12-2

## , VENDOR MAINTENANCE.

### How To Run

From the Vendor Menu (X1-2), select option 1, Vendor Inquiry. The
selection screen prompts you for an address number or last name.

## X12-1 VENDOR INQUIRY

A & R EQUIPMENT SALES ‘VENDOR INQUIRY x12101-01
Division A General Information
Name
Total Balance...
Date Entered,
Last Invoice....
Address (ext)... Invoice #.
City, State. : Amount...
Zip Code... : Last Check......
Telephone #. . Cheek #..,
Work Phone #..... . Amount. .
Customer # .
1234567890 Terms.... & Days (

Sort Codes... Net Days

Edit Codes... : Number Days/Due Days
Cmdl-End Cmd2-General md3-Miscellaneous Cmd4-G/L Dist md5-Summary History
Cad6-Note Cmd?~Current Transactions Cmi8-Transaction History

  

By Address Number

O Enter the address number in the Address # field. Press Enter. The
vendor's receivable information is displayed. To change vendors, type
over the current address number and press [Enter]. Or, to select by last
name, press {Field Exit] to erase the current address number and type a
few characters of the last name in the Name field. See below.

RELEASE 2.1 LO


By Name

 

 

 

Enter the first few letters of the vendor's name in the Name field. Press
Enter. The vendor index is displayed.

 

Vendor Index

A & R EQUIPMENT SALES ‘VENDOR INQUIRY X12101-14
Division: A Vendor Index

Address # © Edit Codes

12345678901

APLUOL v

ALLBOL

ALLEO1

HONDO

AMERICAN MUTUAL INSURANCE INSUOL
BATTERY SHOPPE BATTOL
BLUDGET? MANAGEMENT BLUDOL
BLYTHE STATE BANK PENSOL
CARL D CURRY CURROL
CASCADE UPHOLSTERER‘S caSscoL
CHARLI8'S TRACTOR COMPANY CHAROL
COTES ABRASIVES cOreo1
CUSTOMER DEPOSITS cUSTOL
FORD MOTOR COMPANY FORDO2
FORD MOTOR CREDIT COMPANY FORDO1

v
v
v
v
v
v
v
v
v
v
v
v
v

ee ed

Cmd3-Return Roll -Page

 

The vendor index starts at the closest match to your request, and lists
names in alphabetical order. If the vendor's name does not appear, press


[+] X12-1 VENDOR INQUIRY .
r
{

[PgDn]/[PgUp] to roll to the next/previous screen.

O To select a vendor, place any character next to the vendor's name. Do
not press [Enter]; the vendor's information is displayed automatically.
Or, you can position the cursor beside the vendor's name and go
directly to one of the screens listed below by pressing the appropriate
command key, such as [Cmd4] to display the G/L Distribution Table.
To change vendors, [Field Exit] through the address number. Type a
new address number or press [Tab] and type a few characters of a
vendor's name.

 

 

 

 

### General Information Screen

O Press [Cmd2] to look at the General Information screen, which is
illustrated below:

RELEASE 2.1 LU


A & R EQUIPMENT SALES VENDOR INQUIRY X12101-01
Division A General Information

‘Name

SEMB01 SEMENOW UPHOLSTERING SERVICE A2400
. SEMENOW UPHOLSTERING SERVICE Total Balance.

Address. . 2128 MAPLE DR
Address (ext).... P.O. BOX 49
City, State. . BELLINGHAM WA
Zip Code. . - 98225

Telephone #. + 206 715 3844
Work Phone #..... 206 350 5700 Ext. 4571
Fax #... 206 647 4921

Tax Number - SEMIN70027~-AN812
customer # .

GST Method .

1234567890
Sort Codes
Edit Codes. . zB

Date Entered. 9/21/98
Last Invoice.... 10/03/94
Invoice #. 980-341100
Amount... 124.66
Last Check...... 10/05/94
Check #... 125701
Amount... 371.97-
1099 YID Purch . 537.97 2
G/L Account #... -
Text Account #..
Tax2 Account #..

Texms.... 10.00 & 10 Days
Net 15 Days
Number Days/Due 30 Days

(mdi-mnd Cmd2-General Cmd3-miscellaneous Cmd4-G/L Dist Cmd5-Summary History
(md6-Note Cmd7-Current Transactions Cmd8-Transaction History

 

### Miscellaneous Information Screen

Press [Cmd3] to look at the Miscellaneous Information screen, which is

illustrated below:


6 | X12-1 VENDOR INQUIRY

A & R EQUIPMENT SALES VENDOR INQUIRY
Division A Miscellaneous Info

Alpha
SEMEO1 SEMENOW UPHOLSTERING SERVICE A2400

Include Discount Amount in Taxi.. N (Y/N)
Include Discount Amount in Tax2.. N (¥/N)
Hold Payments Nm)

 

B J LIGHTNER

%12101-02

Cmal-End Cmd2-General Crd3-Miscellaneous Cmd4-G/L Dist Cmd5-Summary History
Cma6-Note Cma7-Current Transactions Cmnd8-Transaction History

GENERAL LEDGER DISTRIBUTION TABLE

 

0 Press [(Cmd4] to look at the G/L Distribution Table, which is illustrated

below:
LL


A & R EQUIPMENT SALES VENDOR INQUIRY ¥12101-03
Division A G/L Distribution

Alpha
SEMEQ1 SEMENOW UPHOLSTERING SERVICE A2400
Invoice Debit Distribution
G/L Acct Fixed Amt & addr t G/L Acct Fixed amt

6670 75.00 we
6590 25.00 12.
13-
14-
1s-
16-
7
18-
19-
20-
Total Fixed Amounts.
Total Pexcentages..... 100.00

Cmil-End Cma2-General Cmd3-Miscellaneous Cmdd-G/L Dist Cmd5-Summary History
Gmd6-Note Cmd?-Current Transactions Omd8-Transaction History


8 | X12-1 VENDOR INQUIRY C .

SUMMARY HISTORY SCREEN

0 Press [Cmd6] to look at the Summary History screen, which is
illustrated below:

A & R EQUIPMENT SALES VENDOR INQUIRY ¥12101-04
Division A Summary History

Alpha
SEMEQ1 SEMENOW UPHOLSTERING SERVICE A2400
~-1994-— Invoices Checks Discounts
Number Amount Number Amount Number Amount,
January. .
February.
March.

Totals... 5 537.97 1 371.97- 1 41.34-
(mdl-End Cmd2-General cmd3-Miscellaneous Cmd4-G/L Dist cmd5-Summary History
(nd7-Current Transactions Cm@§-Transaction History Roll-Page

 

This screen totals the number and amounts of all invoices, checks, and
discounts by month for a particular year. [Roll] up and down to see these
summaries for additional years.

RELEASE 2.1 LO


X12-1 VENDOR INQUIRY [2]

### Current Transactions Screen

Note: Prior to the release of DIS software, "999999" was used to
indicate that a payables transaction had an "undefined" due date.
Most often, this was used with an invoice associated with a floored
unit. Once the unit was sold, the system automatically changed the
due date field from '999999"' to the current system date.

In V8LSA, all information in the date field must be in the form of a
valid date, not '999999."" To project a transaction as far in the future
as possible, enter 123150" or December 31, 2050. This is the most
distant date possible in the DIS system. Dates after December 31,
2050 will be interpreted by the computer as taking place in the 1900's.
Thus, "010151" would be treated by the computer as January 1, 1951.

A more convenient solution to manually typing in 123150" every
time your purchase a floored unit can be found in entering ''999" (the
largest number possible) in the "Number of Days/Due" field for the
floored vendor in Vendor Maintenance (X12-2). When the due date
field is left blank, this field will automatically be filled in with a date
999 days in the future, probably enough time for the unit to be sold.
[When the unit is sold, the due date field, regardless of what it is, will
be filled in with the current system date. At this point, it will be
treated by the system as a normal payables invoice.

 

Page 1—By Due Date

O Press [Cmd7] to look at page 1 of Current Transactions, which is
illustrated below.


A & R EQUIPMENT SALES VENDOR INQUIRY x12101-05
Division Page 1 Current Transactions By Due Date

Print.....
Start.... SEME91 SEMENOW UPHOLSTERING SERVICEA2400 124.66
Inv Date Invoice # Description Due Date Unit # Discount Amount
10/03/94 980-341100 CLEANING 41/02/94 12.47 124.66
** END

Gmdl-End md2-General Omd3-Miscellaneous Cmi4-G/L Dist Cmd5-Summary History
Cmd6-Page 2 Cmd7-Current Tm Cmd8-Trn Hist Cmd9-Invoice Number Roll-Page

 

 

To see the same screen with invoices listed by invoice number, press
[Cmd9].

 

 

 

}

RELEASE 2.1 \


Page 1—By Invoice Number

A & R EQUIPMENT SALES VENDOR INQUIRY x12101-05
Division Page 1 Current Transactions By Invoice Number

Alpha Print....

DOROO1 DOROTHY'S HEAVY HAULING 2,956.08
Inv Date Invoice # Description Due Date Unit # Amount
10/05/94 10022 MISC. WORK 10/30/94 500.32
10/05/94 10689 MISC. WORK 20/20/94 1000.66
10/04/94 129-99 DITCH 10/30/94 259.40
09/12/94 49-19740 = KEN'S TRUCK 10/08/94 466 .23
09/01/94 89-4500 KEN'S TRUCK 9/27/94 86.74
09/03/94 89-5409 KEN'S TRUCK 9/29/94 288.41
09/03/94 69-5410 KEN‘S TRUCK 9/29/94 34.56
07/06/94 984-00761 JO-BREAKDOWN 8/31/94 349.76

### ‘++ End +*

Cmdi-End Cmd2-General Cnd3~-Miscellaneous cmd4-G/L Dist Cmd5-summary History
(md6-Page 2 Ond?-Current Trn cmd8-Trn Hist Cmd9-Due Date Roll-Page

 

Page 2—By Due Date

 

 

 

From page 1 of current transactions, press [Cmd6] to look at page 2,
which is illustrated below.

 


 

X12101-06

A & R EQUIPMENT SALES VENDOR INQUIRY
By Due Date

Division Page 2 Current Transactions

Alpha
Start... SEMEC1] SEMENOW UPHOLSTERING SERVICE
Inv Date Invoice # Id Trn Date G/L Mth
20/03/94 980-341100 10/05/94 10/94
++ END +

cmdi-End Cmd2-General Cmd3-Miscellaneous Cnd4-G/L Dist cmd5-Summary History
Cmds-Page 3 Cmd7-Current Tr cCmd8-Trn Hist cm9-Invoice Number Roll-Page

 

 

To see the same screen with invoices listed by invoice number, press
[Cmd9}.

 

 

 

RELEASE 2.1 CO


Page 2—By Invoice Number

### A & R Equipment Sales Vendor Inquiry *12101-06

Division Page 2 Current Transactions By Invoice Number


Address #.... DOROOl == Alpha Print.....

Start... DOROO1 DOROTHY'S HEAVY HAULING 2,956.08
Inv Date Invoice # Id Trn Date G/L Mth Amount TX1 Amount TX2 amount
20/05/94 10022 10/05/94 10/94 88.02 66.01 500.32
10/05/94 10689 10/05/94 10/94 122.24 89.94 1000.66
10/04/94 129-99 10/04s92 10/94 259.40
09/12/94 49-19740 10/05/94 20/94 466.23
09/01/94 89-4500 10/05/94 20/94 56.74
09/03/94 89-5409 10/05/94 10/94 288.41
09/03/94 89-5410 10/05/96 20/94 34.56
07/06/94 984-00762 9/23/94 9/94 349.76

### ** End +

Cmdl-End Cnd2-General Cmd3-Miscellaneous Cmd4-G/L Dist Cmd5-Summary History
cmd6~Page 3 Cmd7-Curxent Trn Cmd8-Trn Hist Omd9-Due Date Roll-Page

 

Page 3—By Due Date

O From page 2 of current transactions, press [Cmd6] to look at page 3,
which is illustrated below.


1a | X12-1 VENDOR INQUIRY co

A & R EQUIPMENT SALES VENDOR INQUIRY x12101-07
Division Page 3 Current Transactions By Due Date

Alpha
SEMEO1 SEMENOW UPHOLSTERING SERVICE
Inv Date Invoice # Date/Mth/Merge © Check No. Batch No.
10/03/94 980-341100 100594-002
«+ END

Cmdl-End Cmd2-General Cmd3-Miscellaneous Gmd4-G/L Dist Cmd5-Summary History
Crd6-Page 1 Cmd7-Current Trn cmd8-Trn Hist Cmi9-Invoice Number Roll-Page

 

OD To see the same screen with invoices listed by invoice number, press

[Cmd9}.
The type field can be one of four values.
Cc Transaction came from a check
T Transaction came from an invoice

P Transaction came from a partial payment
blank Transaction came from Create Source Documents, not
payables

J
RELEASE 2.1 NW


Page 3—By Invoice Number

A & R EQUIPMENT SALES VENDOR INQUIRY x12101-07

Division Page 3 Current Transactions By Invoice Number

Address # + DOROOL = Alpha Print.

Start.... DOROO1 DOROTHY'S HEAVY HAULING 2,956.08
Inv Date Invoice # Date/Mth/Merge © Check No. Batch No. Type Amount
10/05/94 10022 1 v 500.
10/05/94 10689 1 v 1000.
10/04/94 129-99 100494-001 259.
09/12/94 49-19740 100594-001 7 466.
09/01/94 89-4500 100594-001 7 56.
09/03/94 89-5409 100594-001 T 288.
09/03/94 89-5410 100594-001 7 34.
07/06/94 984-00761 o92494-01 T 349.

** END «+

cmdl-End cmd2-General ¢md3-Miscellaneous Ond4-G/L Dist Cmd5-Summary History
cma6-Page 1 Cmd7-Current Tr Cmd@-Trm Hist Cmd9~pue Date Roll-Page

 

The type field can be one of four values.

Cc Transaction came from a check

T Transaction came from an invoice

P Transaction came from a partial payment

blank Transaction came from Create Source Documents, not
payables


16 X12-1 VENDOR INQUIRY C

TRANSACTION HISTORY

Page 1—By Due Date

C Press [Cmd8] to look at page 1 of Transaction History, which is
illustrated below.

A & R EQUIPMENT SALES VENDOR INQUIRY 12101-05
Division Page 1 History Transactions By Due Date

Address # Print.....
Start.... SEMEQ] SEMENOW UPHOLSTERING SERVICEA2400 124.66
Inv Date Invoice # Description Due Date Unit # Discount Amount,
10/05/94 125701 Check x12-7 10/05/94 41.34- 413.31-
09/14/94 901-8847 = VINYL 10/14/94 3.49 34.88 (
08/10/94 909-8847 BURLAP 10/24/94 5.98 59.75
08/05/94 928-8847 BURLAP 20/14/94 5.98 59.75
08/28/94 369400-018 J.0.'S CHATR 10/28/94 25.89 258.93
** END +*

Cmdl-End Crd2-General Cmd3-Miscellaneous Crd4-G/L Dist Cmd5-Summary History
Cmd6-Page 2 Cmd7-Current Tx Cmd8-Trn Hist Cmd9-Invoice Number Roll-Page

 

O To see the same screen with invoices listed by invoice number, press
[Cmd9].

RELEASE 2.1 LL


Page 1—By Invoice Number

### A & R Equipment Sales Vendor Inquiry *12101-05

Division Page 1 History Transactions By Invoice Number

Address #. - SEMEOL = Alpha Print.
Start.... SEMEO1 SEMENOW UPHOLSTERING SERVICEA2400

Inv Date Invoice # Description Due Date Unit # Discount Amount

10/05/94 125702 Check X12-7 10/05/94 41.34-

09/28/94 369400-018 J.0.'S CHAIR 10/28/94 25.89

09/14/94 901-8847 9 VINYL 10/14/94 3.49

09/10/94 909-8847 BURLAP 10/14/94 5.98

09/05/94 928-8847 BURLAP 10/14/94 5.98

### ++ End

Qmdi-End cm2-General md3-Miscellaneous Cmdé-G/L Dist Cmd5-Summary History
cndé-Page 2 Cmd7-Current Trn cmd8-Trn Hist cmd9-Due Date Roll-Page

 


18 | X12-1 VENDOR INQUIRY Cc

Page 2—By Due Date

O From page | of transaction history, press [Cmd6] to look at page 2,
which is illustrated below.

A & R EQUIPMENT SALES ‘VENDOR INQUIRY 12101-06
Division Page 2 Eistory Transactions By Due Date

Alpha
SEMEO] SEMENOW UPHOLSTERING SERVICE
Inv Date Invoice # Id Tn Date G/L Mth Amount TX1 Amount 7X2 Amount
10/05/94 128702 0 10/05/94 los94 413.31-
09/14/94 901-8847 10/05/94 10/94 34.88
09/10/94 909-8847 10/05/94 10/94 59.75
09/05/94 928-8847 10/05/94 10/94 59.75
09/28/94 369400-018 10/03/94 10/94 258.93
++ END ** (

(mal-End Cmd2~General Cmd3-Miscellancous Cmd4-G/L Dist CmaS-Summary History
(ma6-Page 3 Cmd?-Current Trn Cmd§-Trm Hist Cmd9-Invoice Number Roll-Page

 

O To see the same screen with invoices listed by invoice number, press
[Cmd9].

RELEASE 2.1 C °


Page 2—By Invoice Number

A & R EQUIPMENT SALES VENDOR INQUIRY x12101-06
Division Page 2 History Transactions By Invoice Number

Address #. 1. SEME01 Alpha
Start.... SEME01 SEMENOW UFHOLSTERING SERVICE
Inv Date Invoice # Td Ten Date G/L Mth Amount [TX1 Amount TR2 Amount
10/05/94 125701 0 10/05/94 «10/84 413.31-
09/28/94 369400-018 10/03/94 10/94 258.93
09/14/94 901-8847 10/05/94 10/94 34.88
09/10/94 909-8847 10/08/94 10/94 59.78 :
09/05/94 928-8847 10/05/94 10/94 59.75
** END **

cmai-Fnd Cwi2-General nd3-Miscellaneous Cmd4-G/L Dist Cmd5-Summary History
cma6-Page 3 Cm7-Current Trn Cmd8-Trn Hist Cmd9-Due Date Roll-Page


20 X12-1 VENDOR INQUIRY

Page 3—By Due Date

O From page 2 of history transactions, press [Cmd6] to look at page 3,
which is illustrated below.

A & R BOQUIPMENT SALES VENDOR INQUIRY x12101-07
Division Page 3 History Transactions By Due Date

Address #, SEMEO1 © Alpha
Start.... SEMEO1 SEMENOW UPHOLSTERING SERVICE

inv Date Invoice # Date/Mth/Merge © Check No. Batch No. Type

10/05/94 125701 10/05/84 10/94 125702 ¢

09/14/94 901-8847 40/05/94 10/94 125701 100594~001

09/20/94 309-8847 10/05/94 10/94 125702 100594~001

09/05/94 928-8847 10/05/94 10/94 125702 100594-001

09/28/94 369400-018 10/05/94 10/94 125701 092094-001 : (

++ END wt

Gadi-End Cmd2-General Cmd3-Miscellaneous Cndd-G/L Dist ndS-Sumary History
Cmdé-Page 1 Cmd7-current Tr Cma8-Trn Hist Grd9-Invoice Number Roll-Page

 

 

 

 

 

To see the same screen with invoices listed by invoice number, press
[Cma9}.

 

RELEASE 2.1 Ne


x12-4 VENDOR INQUIRY

The type field can be one of four values.
Cc Transaction came from a check
T Transaction came from an invoice
P Transaction came from a partial payment
plank Transaction came from Create Source Documents, not
payables.

Page 3—By Invoice Number

  
  
  

 

 

    
    
  
    
     
     
  
      
  
 
 

 

 

 

A & R EQUIPMENT SALES \yenpoR INQUIRY x22101-07

pivision page 3 wistory Transactions py invoice Number

nadress Beecetce gamed: © Alpha print..+++

start. .- SEMEO: SEMENOW yeHOLSTERING SERVICE 124.66
‘Tnv Date invoice * pate/Mth/Merge check No. Batch Nov ctype Amount
40/05/94 125702 4o/os/ga 10/94 1257021 c 413.31-
99/20/94 369400-028 40/05/94 10/94 125702 992094-001 T 258-93
99/14/94 901-8847 10/05/94 10/94 125702 100594-002 T 34.88
98/10/94 909-8847 10/05/94 10/94 125701 yoose4-001 T 59.75
09/05/94 928-8847 40/08/94 10/94 128702 400594-001 T $9.75

+e esp’?

 
 
  

-Genezal cnd3-Miscellaneous cmds-G/L DESE omiS-Summary History

cmdi-End cmd?
emas-Page 3 cma7-Current TP cmag-Trn Hist cma9-Due Date Roll-Page

     
  

  

 


[2] X12-1 VENDOR INQUIRY c

Payables
PRINTING TRANSACTIONS

You can Print current and history transactions for 1 or more vendors by
typing "Y" at the "Print" Prompt, which appears in the Upper right corner
of Vendor Inquiry Screens, You can Tequest several vendors during the

RELEASE 21 a


x12-1 VENDOR INQUIRY

vgs if you want te print

Enter
gransactions «++

Bistoxy

Due Date

p = Print by
ice Number

Enter +
Ne Print by inv

98 colums)
¢ (132 Columns)

= complete Report (1!
abbreviated Report


 


 

MEM AWD, co: & rae 9,
Pivteten: 2

SEBO) Lim's orrace surecaes (tm 205-676 26
be 06 340 122) er Lo4g
249 conan FAS 206-659 1064
mam sae

bearer
3 aers3/0 sosie4s

3 INOS cobain, Cros re,
7 12705706 ses-e06 Sua eme

Feead Hiacary Pane secon
‘Current traceectione
5 Mrtr180 sescatcee 32 am

TEAL Correct Take Actions

  
 

sane savers
aarora4 arenes
Br20/98 22707006
saraoree hyena

4 Mreections

aarrziag rss

1 Teansacriocs

tum
aye


 

Vader taastry

2 Du bane

050 cote :

Wek Adatory

CM ME «52150 cate racers, saveri94

Decesnemecge

3707394 2/34
34707784 96
Bro ae
aver aise

Tt 5.008 a8 ee

Bet 90 De

Mater ef Dare owe 65 tere
SARK BRED No. ee hae
su0s © taneae
aap Hovecean p740-33
fae HMO pe
seo ue pa?

 
     

some

se2.m

  

Patance .. 302,76

Phare ee Asean

 

tase Bear
ea,

nis 29

a 109.96

 


  
 
    
  
  
 

     
       
  

   

    

 

 

 

 

 

 

 

 

 

 

 

 

 

   

 

 

 

 

 

 

 

 

 

 

 
 

otal Current Transactions

 
 

 
  

A & R EQUIPMENT SALES
Division: A
‘CURRO1 CARL D CURRY

  
   
 
  
 

2092 TIMBER LANE

 

ra
GREENSBORO NC 27408

trans. Inv Pate Invoice # Description

History Transactions

pistory Transactions

1 24/08/94 690-2023 VAN SEAT

2 29/09/34 100000 Check 412-8
gotal History Transactions

  
 
  
 
   
  
  

 
 

current Transactions
current Pransactions
3 29/09/94 9OL-KK675 NEW DESCRIPT

  
 

      

otal Current Transactions

 


1 pransactions

pue Date Unit ¢ 1D Date Trn G/L Mt Merge Check No~

9/23/94
9729/94

By Due Date
aun 910 362 8993
awk 910 364 1128 EXT 4570 Taxi Acct
FAX 910 39¢ 1128


vender Inquiry

G/L Account:

‘Taxd Acct.
Grovpt Code +
Dare Entered:

9/20/94 9/94
9/29/98 9/94

2 Transactions

6/10/97

ipsossse 9/98

1 Transactions

 

Wich History

az400

124.66

tems

 

A & R EQUIPMENT SALES Vendor inquizy aovosy9s Page 2
Division: A ay Due Date Wich History 1240-48,
SENEO1 SEMENOW UPHOLSTERING SERVICE HH 206 725 3864 Gb account: az400 Terms -:10,00 § 10 Hays Balance 128.65
4nx 206 350 5700 ExT 4572 Text Acct. Net 15 Days
2128 MAPLE DR FAX 206 647 4921 Tax2 acct.. Numbex Days Due 20 Days
P.O. BOX 49 xt Groupt Code =
BELLINGRAM WA 96225 pate Entered: 9/21/34
rans, Inv pate tavoice # Description Dun Dare Unie ¥ XD Pate Sm 6/H Me Merge Chack No. Amount Discount Net Aount,
History Transactions
History Transactions
5 5/10/94 125701 Check 12-7 10/05/94 0 10/05/94 10/94 20/94 125703 413.31- 4n.34- 371.97-
2 44/09/96 902-0847 VINYL 10/24/96 10/05/94 10/94 10/94 125701 34.28 3.49 34.39
3 10/09/94 909-8847 BURLAP 30/24/96 10/05/96 10/94 10/96 325702 59.75 3.98 53.77
4 5/09/94 928-0847 BORLAP aosaasse 10/08/94 10/94 10/94 225702 59.75 5.98 33.77
1 28/09/94 369400-028 J.0.'S CHAIR 10/28/94 10/03/94 20/94 10/94 125702 258.93 25.99 233.04
qoral Ristory Transactions § Transactions
curzent Transactions
curvent Transactions
6 28/09/94 980-342100 CLEANING = 12/02/94 sovos/94 20/94 10/58 124.66 32.67 112.19

 
  

32.47 422.28

norosye4 Page 3
1240-40,

99.99 & 123 nays Balanced04,040, 438.27

Net 12¢ Days

numbes Days Que 999 Days

9/20/94

3/94 100000
5/94 190000

9194

Agount Discount ‘Net Anount
346.82 346.89
346.09- 346.89-

  
 

34.23 -50 33.73

250 33.73


Notes:
LO

## CHAPTER X12-2

VENDOR MAINTENANCE

### Introduction

Use Vendor Maintenance to:

= Set up and maintain a vendor's master record (3 screens)

= Specify a general ledger account (credit entry) for the vendor

= Establish a distribution table of fixed amounts or percentages for one or
more general ledger accounts (debit entry)

= Record notes pertaining to the vendor, which can be seen in Vendor

Inquiry

### How To Run

From the Payables Menu (X1-2), select option 2, Vendor Maintenance.
The Entrance screen prompts you for an address or name, as illustrated
below:

A & R EQUIPMENT SALES *12201-91
Division: A

Address 4

## X12-2 VENDOR MAINTENANCE

### Adding A New Vendor

To add a new vendor, type an address (up to 6 characters), and press
[Enter]. The first screen of a new master record is displayed. The screen
below shows the first screen of a master record after the fields have been
filled in. While you are adding a vendor, you can cancel the entire process

at any time by pressing [Cmd3].

Screen 1

A & R EQUIPMENT SALES
Division: A

Address #

Name... . PARKER'S PAINT & BODY SHOP

Name (ext)

Address... 1709 NOBLE ST
Address (ext)... PO BOX 981
city, State BELLINGHAM WA
2ip code. 98225
Telephone #...... 206 715 4300

Work Phone #..... 206 733 7610 Ext. 4570

206 647 6921

. PARKEO93-2390

249549912

1234567890

Bait Codes.

cmd3-Return Cmd6-Note Enter-Next Page

‘VENDOR MAINTENANCE ¥12201-02

Total Balance...
Date Entered...
Last Invoice...
Invoice #-
Amount.
Last Check.
Check #

Amount... .

G/L Account #... a2400

verms.... 10% 10 Days

Net 15 Days

Number Days/Due 30 Days
fo Cancel Enter 'Y'

 

Note that the "V" edit code in position 2 is not yet on the master record.

NN

### X12-2 Vendor Maintenance [2]

Also, the Total Balance and Date Entered are blank. These are assigned
after the record is complete and can be seen only when the record is
recalled. Until then, [Cmd6] to add payables notes does not work.

O Press [Enter] to go to the next screen.
To cancel the record, press [Cmd3] or type Y at the prompt, "To Cancel
Enter 'Y".

 

 

 

 

   

  

Note: Prior to the release of DIS software, "999999" was used to
indicate that a payables transaction had an "undefined" due date.
Most often, this was used with an invoice associated with a floored
unit. Once the unit was sold, the system automatically changed the
due date field from ''999999"' to the current system date.

In V8LS5A, all information in the date field must be in the form of a
valid date, not "999999." To project a transaction as far in the future
as possible, enter 123150" or December 31, 2050. This is the most
distant date possible in the DIS system. Dates after December 31,
2050 will be interpreted by the computer as taking place in the 1900's.
Thus, "010151" would be treated by the computer as January 1, 1951.

A more convenient solution to manually typing in "123150" every
time your purchase a floored unit can be found in entering "999" (the
largest number possible) in the "Number of Days/Due" field for the
floored vendor in Vendor Maintenance (X12-2). When the due date
field is left blank, this field will automatically be filled in with a date
999 days in the future, probably enough time for the unit to be sold.
When the unit is sold, the due date field, regardless of what it is, will
be filled in with the current system date. At this point, it will be
treated by the system as a normal payables invoice.

    
   
  
  

     
 
       
      
 

     
 
 
 
      
   
   
   
        


Screen 2

A & R EQUIPMENT SALES ‘VENDOR MAINTENANCE, 12201-03
Division: A Screen #2
PARKO2 PARKER'S PAINT & BODY SHOP

Hold Payments
Group Code.

Salesperson

Accounts Receivable Clerk
Telephone (

(nd3-Return Cmd5-Previous Page © Cmd6-Note Enter-Next Page

 

O Press [Enter] to go to the next screen.

RELEASE 2.1 to


X12-2_ VENDOR MAINTENANCE [=]

Screen 3

This table furnishes the defaults that appear when you are entering
invoices for the vendor. The accounts, fixed amounts or percentages, and
address numbers can be changed temporarily in Invoice Entry (X12-5);
however, permanent changes must be made on the screen illustrated
below.

A & R EQUIPMENT SALES VENDOR MAINTENANCE *12201-04
Division: A Sereen #3
PARKO2 PARKER'S PAINT & BODY SHOP

Invoice Distriburion
G/L Acct Fixed Amt %.. Addr # G/L Acct Fixed Amt &% Addr #

1+ A6670 6000
2- 46590 4000
3


19-
20-

Total Fixed Amounts...
Total Percentages

Cmd3-Return Cmd5-Prev Page Cmd6-Note Cmd8-G/L Index Enter-Update

 

This screen can be left blank, or you can specify a fixed dollar amount,
percentages that add up to 100%, or both. If fixed amounts and
percentages are used together, the fixed amounts will be subtracted first
and then the percentages applied to the balance.


—~

[«] X12-2 VENDOR MAINTENANCE a

Normally, transactions created by distribution do not require an address.
However, in special cases (such as posting to a receivable account) an
address will be required.

O When the record is complete, press [Enter] to create the master record
and return to the Entrance screen prompt, where the vendor's address
will be displayed. If you want to add payables notes, simply press
[Enter] at this time. See Adding Payables Notes.

### Adding A Vendor For Miscellaneous Checks

A unique vendor address can be used to write miscellaneous checks. The
recipient and account associated with these checks can be chosen at the

time when each check is written. This is useful for one-time purchases |
that need to be made quickly and easily. \

Follow the procedure detailed above in adding a miscellanous vendor. Set
it up under the ddd999 address, where d is the division associated with the
account (division A's miscellaneous vendor would be AAA999, for
example). While setting up this account enter something like "misc.
vendor" under the description field and a default account in the G/L.
Account # field. When each check is written, you will have the ability to
choose the name and address of the check's recepient and the account that
the check will draw on in writing the check.

G/L Index

If you need help with general ledger account numbers for the distribution
table, press [Cmd8] to see a list of accounts.

i
RELEASE 2.1 LL


X12-2 VENDOR MAINTENANCE 7 |

A & R EQUIPMENT SALES VENDOR MAINTENANCE x12201-04
Division: A Screen #3
PARKO G/L Account Index
8
Inv G/L acct
G/L Acct Fixed amt %.. - A6400 © ADVERTISING
- 46420 WARRANTY
1- A6670 6000 = - A6500 —-COMPENSATION-SALESMEN
2- RES90 4000 - A6S20  - COMPENSATION-OFF EMPLOYEE
3a- - 6530  COMPENSATION-OTHERS
- A6540 — COMPENSATION-PARTSMEN
5 6560 EMPLOYEE BENEFITS-TAXES
A580 = FRETGHT.
a6590 SHOP EXPENSE
6600 TOOLS & SHOP SUPPLIES
A6640 RENT & LEASE EXPENSE
6670 REPAIR & MAINTENANCE

v
E
g
E
E
z
z
2
z
E
E
E

Position to.. . AS

Cnd3-Return Roll-Page

Grd3-Return Cmd5-Prev Page

 

O Press [Shift]+[Tab] to go to the "Position to" prompt. Type a partial or
whole account number, such as “A6" above, and press [Enter]. _ first
account that matches your request appears at the top of the list.

Place a character beside the G/L account. You don't need to press
[Enter]. The account is placed on the next blank line in the table. To
exit without selecting an account, press (Cmd3].

 

 

 

 

Adding Payables Notes

Payables notes cannot be viewed in any application other than Payables.
Notes cannot be added until the record has actually been created, which


happens only after you have pressed [Enter] on screen 3. At that time the
6-character address is still displayed, and you can simply press [Enter] to
recall the vendor's record.

C From any of the 3 screens, press [Cmd6] to enter notes. Six lines of
payables notes are available, as illustrated below.

‘A & R EQUIPMENT SALES
Division: A

x12201-02

. PARKER'S PAINT & BODY SHOP Total Balance...

Date Entered.... 9/21/94
- 1709 NOBLE sT Last Invoice....
+ FO BOX 982 Invoice #.

tee wo ne tee {

PAY THIS BILL ON TIME EVERY TIME

tes PAYABLES trt

Qma3-Return Enter-Update

 

 

 

 

Press [Enter] to record the notes and to back to the original screen, or

to return to the original screen without recording the notes, press
[Cmd3].

 

RELEASE 2.1 to


X12-2 VENDOR MAINTENANCE |

CHANGING A VENDOR'S MASTER RECORD

1 To change information on a vendor's master record, recall it by entering
the vendor's address number at the entrance prompt or selecting the
name from the index. See Client Index.

0 Press [Enter] to go to the next screen or, from screens 2 and 3, press

[Cmd5] to retum to the previous screen.

After the record has been changed on screen, press [Enter] to update it

in the computer.

Press [Cmd3] to return to the entrance prompt.

Press [Cmd1] to end the job.

 

 

 

 

 

 

 

 

Client Index

 

 

 

 

To select a name from the Client Index, field exit through the Address
## field, if any, on the Entrance screen.

O Type a few characters of the last name or company name at the "Name"
prompt, and press [Enter]. An example of the Client Index is displayed
below.


| 10 | X12-2 VENDOR MAINTENANCE

‘A & R EQUIPMENT SALES

VENDOR MAINTENANCE

Client Index

A-1 PLUMBING
ALLERIGHT COMPANY

ALLKINDS INSURANCE COMPANY
AMERICAN HONDA MOTOR COMPANY
AMERICAN MUTUAL INSURANCE
BATTERY SHOPPE

BLUDGETT MANAGEMENT

BLYTHE STATE BANK

CARL D CURRY

CASCADE UPHOLSTERER'S
CHARLIE’S TRACTOR COMPANY
COTES ABRASIVES

CUSTOMER DEPOSITS

FORD MOTOR COMPANY

FORD MOTOR CREDIT COMPANY

Qmd3-Return Roll ~Page

DELETING A VENDOR

Address #

APLUOL
ALLBOL
ALLEOL
HONDOL
INSUO1
BATTOL
BLUDOL
PENSO1
CURRO
cASCO1
CHAROL
corso1
cusTo1
FORDO2
FORDO1

Edit Codes


eseedegeeegege

wo

12345678901

a ee ne)

x12201-06

Telephone

325 8907

325 7666

346 8932

362 8993
389 6500
259 7890
213 8907

357 3200

 

A vendor's master record can be deleted only if there is no active balance.
Even after the record is deleted, it can be reinstated until you run Payables
File Maintenance (X1.12-6) when it is actually removed from the system.

O Recall the vendor's record.
CO


A & R EQUIPMENT SALES
Division: A

X12-2. VENDOR MAINTENANCE ["]

x12201-02

SEMINOW UPHOLSTERING SERVICE Total Balance...

2128 MAPLE DR
P.O. BOX 49
BELLINGHAM WA
98225

206 715 3844

City, state.
Zip Code..

‘Telephone

Work Phone #

206 350 5700 Ext. 4571

Date Entered.... 9/21/94
Last Invoice...
Invoice #.
Amount... .
Last Check.
Check #
Amount... .

206 647 4921
‘SEMIN70027-AN812
983

G/L Account #...
Taxi Account #..
Tax2 Account #..

A2400

GST Method .

1234567890 Terms..., 10% 10 Days
Net 15 Days
Number Days/Due 30 Days

To Delete Enter '¥' _

Sort Codes..
Edit Codes. . v A

Cmd3-Return Cmd6-Note Enter-Next Page

 

O To delete a vendor, place a "Y" at the prompt "To Delete Enter "Y',"
which appears in the bottom right corner of screen 1. This prompt is not
displayed when there is an active balance.

7] we a)
ae SJb Wace | fen fo

- 6S>

ACCOUNTING Or

lay Qe Pst


| X12-2 VENDOR MAINTENANCE

### Fields & Descriptions

Fields on the Vendor Inquiry and Maintenance screens are described in
alphabetical order.
Accounts Receivable Clerk 28 characters.
Telephone 3-3-4 digits.
Fax 3-3-4 digits.
Address 20 characters. Recommended. Street
address or post office box.
Address (ext) 20 characters. Optional. Extended
street address or post office box.
Address # 6 characters. Required. ID number

Address # (distribution screen)

City, State
Customer #

Date Entered

Fax #
GAL Account #

assigned to this vendor.

6 characters. Optional. Normally,
transactions created by distribution
do not require an address. However,
in special cases (such as posting to a
receivable account), an address will
be required..

20 characters. Recommended.

12 characters. Optional. The
customer number assigned to your
dealership by the vendor.

No input allowed. System date
assigned by the system when the
record is created.

3-3-4 digits.

8 characters. Required. Credit
general ledger account. Cannot be
changed while there is an active
balance.


X12-2 VENDOR MAINTENANCE |

GIL Acct 8 characters. Optional. Debit account
for distribution.
Fixed Amt 9.2 digits. Optional. Default on Enter

Invoices screen where it can be
changed. Enter $100.00 as 10000 and
press [Field Exit]. Use either fixed.
amounts, percentages, or both.

% 4.2 digits. Optional. Default on Enter
Invoices screen where it can be
changed. Enter 75% as 7500 and.
press [Field Exit].

Addr # 6 characters. Required if the debit
account is a receivables account.

Group Code 5 characters. Optional.

GST Method I digit (1-3). Required. Canada only.
Method for calculating Goods and
Services Tax. See DIS OPT Library
in the Appendix.

Hold Payments (Y/N) i character. Required. If "Y",
transactions will not be displayed for
selection when printing checks. At
the selection screen for the Payables
Due Report, there is a prompt that
allows you to include these vendors,
if desired (they are excluded by

default).
Include Discount Amount in
Tax1 (Y/N) 1 character. Required.
Include Discount Amount in
Tax2 (Y/N) 1 character. Required.
Last Check No input allowed. Date of the most

recent check to the vendor. Manual


Check #

Amount

Last Invoice

Invoice Number
Amount
Name

Name (ext)
Number Days/Due

Position to

checks are entered in Enter Manual
Checks (X12-8). System checks are
printed in Print Payables Checks
(X12-7).

No input allowed. Check number of
the most recent check to the vendor.

No input allowed. Amount of the
most recent check to the vendor.

No input allowed. Date of the most
recent invoice from the vendor.
Invoices are entered in Invoice Entry
(X12-5).

No input allowed. Number of the
most recent invoice from the vendor.
No input allowed. Amount of the
most recent invoice from the vendor.
28 characters.

15 characters. Extended name.
Optional. The number days due, if
any, will be added to the invoice date
to determine the due date for an
invoice. However, a due date
entered by the user will override a
due date calculated in this way. See
the note on page 3 regarding flooring
vendors. Also, see Invoice Entry
(12-5) for more information.

8 characters. In the G/L Index this
prompt allows you to skip directly to
an account or to the one closest to
your request.


X12-2 VENDOR MAINTENANCE |

Salesperson 28 characters. Optional.
Telephone 3-3-4 digits. Optional.
Fax 3-3-4 digits. Optional.

Sort Codes 10 positions. User-defined, primarily
for Marketing. See SORT CODES in
the Appendix.

Tax # for Tax1 20 characters. Optional.

Tax Id Number 20 characters. Optional.

Tax1 Account # 8 characters. Optional. General
ledger account number for Tax 1.

Tax2 Account # 8 characters. Optional. General
Jedger account number for Tax 2.

Telephone # 3-3-4 digits. Recommended, This

number is used where a telephone
number is displayed or printed on a
report.

Terms % 4.2 digits. Optional. Type 10% as
1000 and press [Field Exit]. This is
the discount rate allowed when the
invoice is paid in the specified

number of days.
Days 3 digits. Optional. Number of days
during which discount can be taken.
Net Days 3 digits. Optional. Number of days

after which the net amount should be
paid. This number must be greater
than the number of days during
which the discount can be taken.

To Cancel (Delete) Enter 'Y' 1 character (Y/N). "Cancel" is
displayed for brand new records only
(Cmd3 does the same thing).
"Delete" is displayed for vendors


[=] X12-2 VENDOR MAINTENANCE

Total Balance

Total Percentages

Total Fixed Amounts

Work Phone #
Zip Code

who have no active balance.

No input allowed. The system
calculates and displays the total of all
unpaid invoices.

No input allowed. The system
provides a running total of the
percentages allocated to G/L
accounts. The final total must be
100%.

No input allowed. System calculates
and displays a running total of fixed
amounts.

3-3-4 digits. Optional.

9 characters. Recommended.
Lo

## CHAPTER X12-3

GROUP CODE MAINTENANCE

### Introduction

Group Cede Maintenance allows you to create or modify groups to which
vendors can be assigned. Checks and reports may be printed according to
what group (if any) vendors are assigned.

### How To Run

From the Payables Menu (X1-2), select option 3, Group Code
Maintenance. The following screen appears.

ABC-AG, AUTO,CONS & TRUCK CO. GROUP CODE MAINTENANCE *12301-02
Division A

 

0 To add a new group, type in the name of the new group and press
[Enter].
O To change the description of an existing group, enter that group's name


X12-3 GROUP CODE MAINTENANCE _

 

 

and press [Enter].

ABC-AG,AUTO,CONS & TRUCK CO. GROUP CODE MAINTENANCE x12302-02
Division A

Group Code

Description .

Enter '¥' to Cancel

cmd3-Return Enter-Update

 


Use [Tab] to position the cursor in the description field to enter a
description of your group.

To accept the new group, press [Enter]; to cancel, put a "Y" in the
"Cancel" field and press [Enter].

CO Enter another group name, or, if you are finished, press [Cmd1] to
leave. The following prompt appears:


Enter 'Y' for Group Code List............. N

(
RELEASE 2.1 Xe


X12-3 GROUP CODE MAINTENANCE [=]

O To print out a list of all groups, type a "Y" and press [Enter].
Otherwise, press [Enter] to return to the payables menu.

Uses for Group Codes

Group codes can be used for many purposes. Here is a list of possible
uses:

Q Vendors which will receive 1099's could be assigned to a specific
group.

Q Vendors whose invoices are due on the 10th, 15th, or 20th of each
month could be assigned to different groups.

Q Vendors whose invoices come in COD or with terms could be assigned
to different groups.


Notes:
\

## CHAPTER X12-4

CORRECT DUE DATES & DISCOUNTS

### Introduction

Use this job to change posted invoices. You may change discounts and due
dates (Cmd2-Change), merge transactions (Cmd3-Merge), or split a
transaction (Cmd4-Split). “Change," "Merge," and “Split” are referred to
as “modes.” You can search for (position to) a specific transaction by
Invoice Number or Due Date. By pressing [F9], you can display
transactions sorted in order by Due Dates, Invoice Numbers, or Unit
Numbers.

### How To Run

From the Payables Menu (X1-2), select option 4, Correct Due Dates and
Discounts. The Vendor Selection Screen is displayed in Change
Discount/Due Date mode (see center of 2nd line) as illustrated below:


[2] X12-4 CORRECT DUE DATES & DISCOUNTS

Vendor Selection Screen

NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS x12402-01
Division A Change Discount/Due Date By Due Date
Address # yame Transaction ..
Discount
G/L Account Due Date

Position to :

Gmdi-End Cmd2~Change Cmd3-Merge cmdd-split cma9-Invoice Number Roll-Page

 

By Address Number

O Enter the address number in the Address # field. Press [Enter]. The
vendor's information is displayed. To change vendors, type over the
current address number and press [Enter]. Or, to select by last name,
press [Field Exit] to erase the current address number and type a few
characters of the last name in the Name field. See below.


X12-4 CORRECT DUE DATES & DISCOUNTS [2]

By Last Name
O Enter the first few letters of the vendor's last name in the Name field.
Press Enter. The vendor index is displayed.

Vendor Index

 
 

  
  
 
   
  
       
  
   

  

WW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS
Division: A Vendor Index

x12401-03

  

       

   

 

Name---

 
 

 

Edit Codes
12345678901

Telephone

       

© & & RADIATORS INC v A 715 3122
CASCADE UPHOLSTERER'S v A 389 6500 -
_ CHARLIE'S TRACTOR COMPANY CHAROL v B 259 7890
_ COTES ABRASIVES COTEOL v A 213 8907
_ CUSTOMER DEPOSITS cUsTOL v A
_ FORD MOTOR COMPANY FORDO2 v A
— FORD MOTOR CREDIT COMPANY FORDO3 v A 357 3200
_ GREATNORTHERN STATE BANK GREAO1 v A 345 8808
— TH, CASE CASEOL v A .
. TH, CASE cASEO2 v A
_ ITEM, INC ITEMOL v A
_ JIM BELL'S RADIATORS JIMBO v A 324 7893
— JOHN DEERE TRACTOR COMPANY JOHNO2 v A 378 7990
_ MASSEY-FERGUSON MASSO2 v A
— MASSEY-FERGUSON MASSO2 v A

  

Roll-Page

 

 

 

To select a vendor, place any character next to the vendor's name. Do
not press {Enter]; the vendor's current transactions are displayed
automatically,

 

### [+] X12-4 Correct Due Dates & Discounts

O To change vendors, press [Cmd3]-Return to go back to the address and
name prompts.

RELEASE 2.1 CO


X12-4 CORRECT DUE DATES & DISCOUNTS [=]

CHANGE DISCOUNT/DUE DATE

On the second line of the screen below, note the mode, which is Correct
Discount/Due Date (same as Cmd2-Change). Also on the second line, note
the sort order, which is "By Due Date." Change mode is characterized by
the prompts: Transaction, Discount, and Due Date.

  

 
 
     
     
  

Note: Prior to the release of DIS software, "999999" was used to
indicate that a payables transaction had an "undefined" due date.
Most often, this was used with an invoice associated with a floored
unit. Once the unit was sold, the system automatically changed the
due date field from "999999" to the current system date.

In V8L5A, all information in the date field must be in the form of a
valid date, not '"999999."" To project a transaction as far in the future
as possible, enter "123150" or December 31, 2050. This is the most
distant date possible in the DIS system. Dates after December 31,
2050 will be interpreted by the computer as taking place in the 1900's.
‘Thus, ''010151" would be treated by the computer as January 1, 1951.

A more convenient solution to manually typing in "123150" every
time you purchase a floored unit can be found in entering "999" (the
largest number possible) in the "Number of Days/Due" field for the
floored vendor in Vendor Maintenance (X12-2). When the due date
field is left blank, this field will automatically be filled in with a date
999 days in the future, probably enough time for the unit to be sold.
'When the unit is sold, the due date field, regardiess of what it is, will
be filled in with the current system date. At this point, it will be
treated by the system as 2 normal payables invoice.

 
 
       
     
  

      
 
 
      
   
   
   
       

## X12-4 CORRECT DUE DATES & DISCOUNTS

 

 

 

To change the sort order, press [Cmd9]. Transactions can be displayed
in order of: Due Date, Invoice Number, and Unit Number.

 

NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS %12401-01
Division A Change Discount/Due Date By Due Date
Address # C&LRO1 Name ‘Transaction 1

C & L RADIATORS INC Discount .

G/u Account A2400 Balance 170.33 Due Date - 102395

Trans Date Inv # Invoice Description Due Date Unit # Discount Amount
1 10/20/95 PS9023-510 LP TOYOTA 10/30/95 8.34 166.87
2 10/05/95 NDO0S1-356 LP TOYOTA 10/15/95 3.46
++ ND t*

Position to :
Cmd1-End Cmd2-Change Cmé3-Merge Cmd4-split Cmd9-Invoice Number Roll-Page

 

 

 

Find the invoice you want to change. You can use the "Position to"
prompt at the bottom of the screen, where you can enter an invoice
number or a due date.

Type its transaction number (far left column) at the "Transaction"
prompt and press [Field Exit].

O Type the new discount, if any, at the "Discount" prompt, and press

 

 

 

 

RELEASE 2.1 KO


 

[Field Exit]. Leave this field blank if you don't want to change the
current discount.

11 Type the new due date, if any, at the "Due Date" prompt, and press
[Field Exit]. Leave this field blank if you don't want to change the
current due date.

O Press {Enter]. The transaction is displayed at the top of the list. A
message is displayed at the bottom of the screen:

 

NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS x12401-01
Division A Change Discount/Due Date By Due Date
Address # C&LRO] Name Transaction .. 2

© & L RADIATORS INC Discount .

G/L Account A2400 Balance 170.33 Due Date ...., 102395

1 30/20/85 Ps9023-510 LP TOYOTA 10/30/95 8.34

Position to :
(md1-End Cmd2-Change Cmd3-Merge Cmd4-Split Cmd9-Invoice Number Roll-Page
DIS-1184 You can stop this change by pressing Cmd2, Cmd3 or Roll.

 


 

0 If you want to cancel the change, press [Cmd2], [Cmd3], or a roll key;
otherwise, press [Enter] to make the change. Check the result carefully.
The screen below shows the same transaction (still #1, with a zero
discount and due date of Oct. 23, 1995.

x12401-01

NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS
Change Discount/Due Date By Due Date

Division A
Address # C&LRO1 Name Transaction .-
C & L RADIATORS INC
G/L Account 2400 Balance 170.33 Due Date
Trans Date Inv # invoice Description Due Date Unit # Discount
1 10/20/95 PS9023-510 LP TOYOTA = 10/23/95
2 10/05/95 ND005i-355 LP TOYOTA 10/15/95
A* END #*

Position to :

(mdi-End cmd2-change Cmd3-Nerge Cmdd-split cmd9-Invoice Number  Roll-Page

 

O Repeat for other transactions for the current vendor.
O To select another vendor, type another address, or field exit through the

address, type a few characters of the name, press [Enter] and select

from the index.
O If you are done, press [Cmd1] to end the job.

RELEASE 2.1 CO


X12-4 CORRECT DUE DATES & DISCOUNTS [2]

MERGE

You can merge the following transactions:

= Debit with Credit
When a debit and credit are merged, the resulting transaction will have
the same transaction number, transaction date, invoice number,
discount, and due date as the transaction with the highest value. If the
transactions were posted to 2 different general ledger months, the
resulting transaction will be assigned to the later of the 2 months.

= Debit with Debit
When debits are merged, transaction #2 is merged into transaction #1, a
new transaction number is assigned with the same transaction date,
invoice number, etc. as the transaction entered as transaction #1. If the
transactions were posted to 2 different general ledger months, the
resulting transaction will be assigned to the later of the 2 months.

= Credit with Credit
When credits are merged, transaction #2 is merged into transaction #1,
a new transaction number is assigned with the same transaction date,
invoice number, etc. as the transaction entered as transaction #1. If the
transactions were posted to 2 different general ledger months, the
resulting transaction will be assigned to the later of the 2 months.

On the second line of the screen below, note the mode, which is Merge
(same as Cmd3-Merge). Also on the second line, note the sort order,
which is "By Due Date." Merge mode is characterized by the prompts:
Transaction #1 and Transaction #2.

O To change the sort order, press [Cmd9]. Transactions can be displayed
in order by: Due Date, Invoice Number, and Unit Number.


10 | X12-4 CORRECT DUE DATES & DISCOUNTS

NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS x12401-02
Division A Merge By Due Date
Address # C&LRO] Name Transaction #1 1

C & L RADIATORS INC Transaction #2 2

G/L Account A2400 Balance 170.33

Trans Date Inv # Invoice Description Due Date Unit # Discount
1 10/20/95 PS9023-510 LP TOYOTA 10/23/95
2 10/05/95 NDOOS1-356 LP TOYOTA 10/15/95
++ END **

Position to :
Qndl-End Cmd2-Change cmd3-Merge Cmd4-Split Cmd9-Invoice Number Roll-Page

 

 

 

 

 

Find the transactions you want to merge.

O Type their transaction numbers (far left column) at the prompts labeled
“Transaction 1" and "Transaction 2" and press [Field Exit].

O Press [Enter]. The following message is displayed at the bottom of the

screen:


NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS

x42401-02

Division A uerge By Due Date

Address # C&LRO1 Name Transaction #1
© & L RADIATORS INC Transaction #2
G/L Account A2400 Balance 170.33

1 10/20/95 PS9023-510 LP TOYOTA 10/23/95
2 10/05/95 NDO0S1-356 LP TOYOTA 10/15/95

Position to :
Cmdl-End Cmd2-Change Cmd3-Merge Cmd4-Split ¢mé9-Invoice Number
DIS-1185 You can stop this merge by pressing Cmd2, Cmd3 or Roll.


Rell-Page

 

O If you want to cancel the request, press [Cmd2], [Cmd3], or a roll key;
otherwise, press [Enter] to merge the transactions. Check the result

carefully.


‘NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS %12401-02

Division A Merge By Due Date
Address # C&LRO1 Name Transaction #1

© & L RADIATORS INC Transaction #2
G/L Account A2400 —- Balance 170.33

Trans Date Inv # Invoice Description Due Date Unit # Discount
4 10/20/95 PS9023-510 LP TOYOTA = 10/23/95
** END **

Position to :
mdi-End omd2-Change Cmd3-Merge Cmd4-Split Cmi9-Invoice Number Roll-Page

 

In this example, 2 debits were merged. Note the new transaction number.
Also note that the transaction date, invoice number, etc. is the same as the
transaction entered as transaction #1.

O Repeat for other transactions for the current vendor.
O To select another vendor, type another address, or field exit through the

address, type a few characters of the name, press [Enter] and select
from the index.

O Ef you are done, press [Cmd1] to end the job.

RELEASE 2.1 Lo


X12-4 CORRECT DUE DATES & DISCOUNTS [=]

SPLIT

You can split any transaction into 2 separate transactions and assign a new
discount and due date to the new transaction. A debit can be split into 2
debits, a credit into 2 credits. The discount of the new transaction must be
equal to or less than the original discount.

On the second line of the screen below, note the mode, which is Split
(same as Cmd4-Split). Also on the second line, note the sort order, which
is "By Due Date." Split mode is characterized by the prompts: New
Amount, New Discount, and New Due Date.

 

 

 

To change the sort order, press [Cmd9]. Transactions can be displayed
in order by: Due Date, Invoice Number, and Unit Number.

 


 

NW BQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS *12401-05
Division A Split. By Due Date
Address # GREAQ] Name Transaction .. z

GREATNORTHERN STATE BANK New Amount ... 25000

G/L Account A2400 Balance 5,000.00 New Discount .

New Due Date . 110195

Trans Date Inv # Invoice Description Due Date Unit # Discount Amount

1 10/23/95 3456988842 LOAN 10/23/98 5000.00

4* END **

Position to :
cmdi-End md2-Change Cmd3-Merge Cmd9-Invoice Number  Roll-Page

 

O Find the transaction you want to split.

OC Type its transaction number (far left column) at the prompt labeled
“Transaction" and press [Field Exit].

O Type the amount of the new transaction you are creating. It must be less
than the original transaction and it must be the same type (debit or
credit).

O Type the discount associated with the new transaction, if any. The new
discount must be less than or equal to the original discount.

O Type the due date of the new transaction. If the due date is the same as

 


the original transaction, you may leave this field blank.
Press [Enter]. The following message is displayed at the bottom of the
screen:

 

 

 

 

NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS %12401-05
Division A split By Due Date
Address # GREAQ] Name ‘Transaction .. 1
GREATNORTHERN STATE BANK New Amount... 25000
G/L Account A2400 Balance §,000.00 New Discount .
New Due Date . 110195
1 10/23/95 3456988842 LOAN 10/23/98 $000.00

 

Position to :
cmdl-End ¢md2-Change Cmd3-Merge Cm9-Invoice Number Roll-Page
DIS-1184 You can stop this change by pressing Cmd2, Cmd3 or Roll.

 

C If you want to cancel the request, press [Cmd2], [Cmd3], or a roll key;
otherwise, press [Enter] to merge the transactions. The new transaction
is displayed.


a6 | 12-4 CORRECT DUE DATES & DISCOUNTS

NW EQUIPMENT SALES & RENTALS CORRECT DUE DATES AND DISCOUNTS ¥12401-95
Division A split By Due Date
Address # GREAOl Name Transaction ..
GREATNORTHERN STATE BANK New Amount .
G/L Account A2400 Balance 5,000.00 New Discount .
New Due Date .
Trans Date Inv # Invoice Description Due Date Unit # Discount Amount,
1 10/23/95 3456988842 LOAN 10/23/98 4750.00
2 10/23/95 3456988842 LOAN 11/01/95 250.00
** END t*

Position to ;
Cadi-End Cmd2-Change Cmd}-Merge Cmd9-Invoice Number Roll-Page

 

O Check the result carefully.

O Repeat for other transactions for the current vendor.

To select another vendor, type another address, or field exit through the
address, type a few characters of the name, press [Enter] and select
from the index.

O If you are done, press [Cmd1] to end the job.

 

 

 

 

RELEASE 2.1 LO

## CHAPTER X12-5

INVOICE ENTRY

### Introduction

Invoice Entry is a version of Create Source Documents, similar to
Receivables Payment Entry. It is specifically designed to enter vendor
invoices quickly. The batch is not posted until you press [Cmd12]=Post
Invoices. This job is both interactive and recoverable.

Invoice Entry batches are workstation specific and retain the same batch
ID until they are posted. A new batch ID is requested only when there is
no batch for the workstation. There is no limit to the number of times you
can go in to work on a batch after it has been created; however, it must
always be at the same workstation. Individual invoices can be deleted from
a batch or the entire batch can be canceled.

Invoice Entry credits the vendor's account, which is assigned in Vendor
Maintenance (X12-2), and the corresponding debit(s), which may be to
one or more expense accounts. The system uses the allocation accounts
entered in Vendor Maintenance (X12-2) as defaults; however, they can be
changed invoice-by-invoice in the batch.

   

  

Note: If the system is interrupted because of a power failure or
similar disaster while the batch is being posted, your data is not

corrupted. Once the system is running again, simply return to the job
that was interrupted and the posting will continue as before.


[2] X12-5 INVOICE ENTRY .

COMMAND KEYS

Vendor Selection Screen

Cmd1-End Ends the job and returns to the
Payables Menu. The batch, which
has not been posted, remains "in
process" at the same workstation and
will be displayed the next time

Invoices Entry is selected.
Cmd10-Totals Displays a summary of batch totals
(amount and number of invoices).
See Totals.
Cmd12-Post Invoices Initiates the posting process and

prints the final register (edit list),
which is sorted by vendor address
number. The 9 job steps are
announced on screen and the screen
is not released until they are
complete. See Post Invoices.

Cmd14-Print Register Prints the edit list, but does not post
the batch. See Print Register.

Cmd19-Delete Batch Deletes all invoices in the batch and
cancels the batch after a confirmation
message.

Roll Displays the next screen of invoices
in the current batch.

Home-Top of List Returns to the top of the list of
invoices in the current batch.

Enter Saves and returns to select another
vendor.

i
RELEASE 2.1 AL


X12-5 INVOICE ENTRY [=]

Invoice Information & Allocation Sections

Cmd3-Retum Retums to the previous section or
screen without saving.
Cmd5-Save & Return to ADD Saves the original invoice you're

working on and stays in the Invoice
Information section so you can enter
another invoice for the same vendor.
Invoice Number, Date, Amount,
Description, Discount, and Due Date
are repeated for the next entry. When
you revise an invoice, press [Enter].
[Cmd5] is not allowed on updates.

Cmd6-Configuration Displays allocation from the current
vendor's master record.
Cmd8-G/L Account Index Displays the Chart of Accounts and

allows you to select an account for
the Allocation section.
Cmd10-G/L Account Description Displays the description of the
general ledger accounts selected in
the Allocation section.
Cmd19-Cancel Invoice Cancels the current invoice and
deletes it from the batch after a
confirmation message.


[+] X12-5 INVOICE ENTRY cee
{

### How To Run

From the Payables Menu (X1-2), select option 5, Invoice Entry. Prompts
for the transaction date and general ledger posting month follow.

 
 

### Warning!

  
     

The transaction date is used as the default for each invoice or check;

however, it can be changed on the Invoice Entry screen, making it

possible to assign different transaction dates to each invoice. Al
invoices are posted to the same general ledger month.

    
   

 

Your selection is confirmed, and the Batch Number Selection screen is
displayed.

RELEASE 2.1 LL


X12-5 INVOICE ENTRY [=]

### Batch Number Selection Screen

This screen is displayed only when there is not an active batch at the
workstation.

A & R EQUIPMENT SALES INVOICE ENTRY #12501~01
Division A Batch Number Selection

Enter Batch Number + 092094-003

 

 

 

 

Enter up to 10 characters as the Batch Total. You may want to
standardize on a format such as the date and batch number for the
current day.

 

## X12-5 INVOICE ENTRY

### Vendor Selection Screen

The Vendor Selection screen is used for 2 purposes:

= To select a vendor in order to enter an invoice, which is illustrated in

this section.
= To select an invoice that was entered previously in order to review or

change it, which is illustrated in the section, List of Invoices..

A & R EQUIPMENT SALES INVOICE ENTRY *12502-01

Division A Batch 092094-001

Name

- Invoice # Inv Date unit #

Cndl-End Cmd10-Totals  Cmd12-Post Invoices
CmdLd-Print Register cmdi9-Delete Batch

Roll-Page © Home—Top of List

 

RELEASE 2.1 C.


X12-5 INVOICE ENTRY [7]

By Address Number

O Enter the address number in the Address # field. Press [Enter]. The
vendor's information is displayed. To change vendors, type over the
current address number and press [Enter]. Or, to select by last name,
press [Field Exit] to erase the current address number and type a few
characters of the last name in the Name field. See below.

By Name

Q Enter the first few letters of the vendor's name in the Name field. Press
Enter. The vendor index is displayed.


a | X12-5 INVOICE ENTRY

VENDOR INDEX

A & R BQUIPMENT SALES INVOICE ENTRY
Division: A Vendor Index

X SEMENOW UPHOLSTERING SERVICE
— SHINE & CLEAN

SKAGIT COUNTY MEDICAL

— SMALLS

_ SMYTHE TRACTOR

STAG BAG

— STARBUCK'S COFFEE

— STARNES,ERWIN $

— SUNFLOWER TRACTOR COMPANY
— TAMA COUNTY STATE BANK

— THANK YOU FOR YOUR BUSINESS
— TRI COUNTY UTILITIES

— VAROOM INDUSTRIES

— WE TOW COMPANY

— WEST COAST GRAPHICS

Qnd3-Return Roll -Page

Address #

SEMIOL
SHINOL
MEDIOL
SMALO
SMYTOL
STAGOL
STAROL
STAROZ
SUNFO1
TAMAOL

CASHA
‘TRICOL
‘VAROOL
WETOOL
WESTOS

Edit Codes


eqeegeee¢eeegeae

™

12345678901

PP UP eee yD DY DO DD

*22502-11

 

O To select a vendor, place any character next to the vendor's name. Do
not press [Enter]; the vendor's information is displayed automatically.
O To change vendors, press Cmd3=Return to go back to the address and

name prompts.

### Invoice Information Section

The Add/Update Invoices screen displays data from the vendor's master
record along with the Invoice Information section.

ADD/UPDATE INVOICES

SEMEO1 SEMENOW UPHOLSTERING SERVICE
Terms .: 10.00 % 10 Days
Net 15 Days
Number Days Due 30 Days
Credit G/L Account : A2400

Discount for Tax!
INVOICE INFORMATION

: 369400-018
Invoice Date , 092894
Invoice Amount ..: 25893

Description 7.0.18 CHAIR
Discount -

Due Date «

Unit Number

Help-Command Keys

 


X12-5 INVOICE ENTRY co

Fields in the Invoice Information section correspond to fields on the
Create Source Documents (X1-7) screen. For details on how to post
various transactions, please refer to CHAPTER X1-7 and the Quick
Reference Guide.

ID 1 character,

Invoice Number 10 characters. If the same invoice number has
already been posted for the vendor, a warning
message is displayed. When you press [Cmd5] to
Save & Return to ADD, the contents of this field
remain.

Invoice Date Date (MMDDYY). Repeats with [Cmd5].

Taxl Amount 9 digits, including 2 decimal digits. Amount of Tax
1, if any. An amount can be posted in this field only
if there is an account for Tax 1 on the vendor's {
master record. This field is only valid for Canadian
dealerships.

Tax2 Amount 9 digits, including 2 decimal digits. Amount of Tax
2, if any. An amount can be posted in this field only
if there is an account for Tax 2 on the vendor's
master record. This field is only valid for Canadian

dealerships.
Description 12 characters. Repeats with [Cmd5].
Discount Leave this field blank to use the system's

calculations. Note: The system doesn't remove the
discount even if it is no longer valid. It must be
removed manually. Repeats with (Cmd5].

Due Date 6 digits. If this field is left blank, the due date will
be calculated by adding the Invoice date to the
Number Days/Due (assigned in Vendor
Maintenance (X12-2)). Repeats with [Cmd5].

Unit Number 6 characters.

RELEASE 2.1 A


Note: Prior to the release of DIS software, 999999" was used to
indicate that a payables transaction had an "undefined" due date.
Most often, this was used with an invoice associated with a floored
unit. Once the unit was sold, the system automatically changed the
due date field from ''999999"' to the current system date.

In V8L5A, all information in the date field must be in the form of a
valid date, not 999999." To project a transaction as far in the future
as possible, enter 123150" or December 31, 2050. This is the most
distant date possible in the DIS system. Dates after December 31,
2050 will be interpreted by the computer as taking place in the 1900's.
Thus, "010151" would be treated by the computer as January 1, 1951.

A more convenient solution to manually typing in "123150" every
time your purchase a floored unit can be found in entering '999"' (the
largest number possible) in the "Number of Days/Due" field for the
floored vendor in Vendor Maintenance (X12-2). When the due date
field is left blank, this field will automatically be filled in with a date
999 days in the future, probably enough time for the unit to be sold.
‘When the unit is sold, the due date field, regardless of what it is, will
be filled in with the current system date. At this point, it will be
treated by the system as a normal payables invoice,

 

O When the fields in the Invoice Information section are complete, press
[Enter] to allow the system to do its calculations and proceed to the
Allocation section.

### Allocation Section

Note that on the screen below, the discount has been calculated, and the
due date has been set 30 days after the number of days due. In addition,
the total amount has been allocated to 2 general ledger accounts according
to instructions in the vendor's master record. The accounts and the


amounts can be changed on this screen; however, to make permanent
changes to the defaults, use Vendor Maintenance (X12-2).

Normally, transactions created by distribution do not require an address or
unit number. However, in special cases (such as posting to a receivable
account), these fields might be required.

ADD/UFDATE INVOICES

SEME01 SEMENOW UPHOLSTERING SERVICE

Terms .: 10.00 % 10 Days
Net 15 Days
Number Days Due 30 Days
Credit G/L Account ; A2400
Taxl .
fax2 .
Discount for Taxl: N Tax2: N
INVOICE INFORMATION

Invoice Number
Invoice Pate ..

369400-018
9/28/94
258.93

Invoice Amount ..:
Taxl Amount...
Tax2 Amount
Description .
Discount ..
Due Date ..
Unit Number .

: J.0.'S CHAIR
25.89
10/28/94

 

ALLOCATION
G/L Acct Amount Addr # Unit #
6670 19420
6590 6473

Help-Command Keys

When the Allocation section is OK, press [Enter] to return to the Vendor
Selection screen, or press [Cmd5] to save this invoice and return to the
Invoice Information screen to add another invoice for the same vendor.

RELEASE 2.1 ae

### Help-Command Keys

While you are working on the Invoice Information and Allocation
sections, you can press [Help] at any time to see a summary of available
command keys, as illustrated below:

ADD/UPDATE INVOICES ALLOCATION
G/L Acct amount Addr # Unit @
SEMEQi SEMENOW UPHOLSTERING SERVICE a- A6670 19420
Terms .: 10.00 & 10 Days 2- A6590 6473
Net 15 Days
Number Days Due 30 Days
Credit G/L Account : A200

Discount for Taxl: N Tax2:
INVOICE INFORMATION

Invoice Number ..: 369400-018
Command Keys

crd3-Return

OmdS~Save & Return to ADD
Crd6-Configuration

Cnd8-G/L Account Index
CmdL0-G/L Account Description
Qmd19-Cancel Invoice

Enter-End Help Help-Command Keys

 

Screens are illustrated on the following pages.

0 To exit help, press [Enter].


Cmd6-Configuration

SEMENOW EQUIPMENT INVOICE ENTRY x12502-08
Division A vender Configuration
DOROO] DOROTHY'S HEAVY HAULING

Invoice Distribution
G/L Acct Fixed Amt Ader # G/L Acct Fixed Amt % Addr #

1- A6580 1i-
12-
13-
u4-
is-
16-
1i-
18- (
1s-
20-

 

Tota? Fixed Amounts .:
Total Percentages ...:

Press any character to continue

 

RELEASE 2.1 LO


Cmd8-G/L Account Index

ADD/UPDATE INVOICES ALLOCATION
G/b Acct Amount Addr # Unit #
G/L ACCOUNT INDEX A6590 37883

G/L Acct Deseription----~----.
6400 ADVERTISING

6420 WARRANTY

6500 © COMPENSATION-SALESMEN
6520 COMPENSATION-OFF EMPLOYEE
A6530 © COMPENSATION-OTHERS
6540“ COMPENSATION-PARTSMEN
A6S60 EMPLOYEE BENEFITS-TAXES
6580 = FREIGHT

6590 SHOP EXPENSE.

A6600 — TOOLS_& SHOP SUPPLIES
AG640 - RENT & LEASE EXPENSE
6670 REPAIR & MAINTENANCE

First Page Follows ..: A6

omd3-Return Foll-Page

Help-Command Keys

 


Cmd10-G/L Account Description

DESCRIPTION OF GENERAL LEDGER DISTRIBUTION ACCOUNTS
G/L Acct Description-- * Amount Addr #

1- A6590 SHOP EXPENSE 323.83

2- 6600 TOOLS & SHOP SUPPLIES 55.00

‘**" Press any character to continue ***

x12502-07
Unit #

 


X12-5 INVOICE ENTRY [7]

Cmd19-Cancel Invoice

You can cancel an individual invoice from a batch by pressing [Cmd19].
The following confirmation message is displayed:

INVOICE ENTRY *12502-10
Cancel an Invoice

: DORQO] DOROTHY'S HEAVY HAULING INVOICE: 129-99

confirm .; N (Y/N)

omd3-Return,

 


| X12-5 INVOICE ENTRY

### Totals

On the Vendor Selection screen, press [{Cmd10] to see totals for the batch.

ABC-AG,AUTO,CONS & TRUCK CO. INVOICE ENTRY x212502-02
Division A ‘Totals

Number of Invoices. :

‘"* Press any character to continue ***

 

‘
RELEASE 2.1 AW


X12-5 INVOICE ENTRY [=]

### Post Invoices

When the batch is complete, press [Cmd12] to post the transactions to the
general ledger. A confirmation message is displayed, as illustrated below.

AG R EQUIPMENT INVOICE ENTRY x12502-13
Division A Post Invoice Batch M

BATCH # 100594-00
Post Invoice Batch

Confirm ... ¥ (Y/N)

cmi3-Return - Enter-Confizm

 

As posting proceeds, messages inform you about each step. In addition,
the register (edit list) is printed (see the section, Print Register). When
posting is done, press [Enter] to return to the Payables Menu. The next
time Invoice Entry is selected, the Batch Number Selection screen is
displayed.


20 | X12-5 INVOICE ENTRY

### Print Register

At any time when you are on the Vendor Selection screen, you can press
[Cmd14] to print the invoice register, which is the same as the Edit List for
Create Source Documents. A final register is printed automatically
whenever a batch is posted. Sample registers are illustrated below.

Interim Invoice Register

This is how the register looks when it is the result of [Cmd14].

A&R RQOIPEENT Invoice Register Batch #: 10594-9001 10/05/94 Page|
Division: & i250-32

Yd Invoice # Date crediz Anount Description Discount Due Date unit
## adar +

49-19740 9/12/94 azeno 466.23 KEN'S TRUCK 45.62 20/08/94 TR1000 PORODL
Allecation : A6s60 456.23
e9-4500 9/01/94 azgoe 86.74 EX'S TRUCK $.€7 9/27/94 TRI000 DOROOL
Allocation : AG580 56.74
a9-5409 9/03/94 22400 280.41 XEN'S TRUCK 9/25/94 7R1000 DoROCT
Allocation + a6se0 29a.e1
89-5410 9/03/94 A240 : EWS TRUCK M6 9/29/94 7R1000 DORODL
Allocation ; A6560
7905, 3/23/94 a2400 : g/21-9/20 3/23/94 RALPOL
Allocation + a6670
901-9847 9/14/94 a2dca : vn 3.49 10/24/94
Allocation + 26670
309-8847 9/10/94 A240 . ‘BURLAP 5.98 10/24/94
2 A6670
9/05/94 azaao - BURLAP 5.98 10/14/94
Allocatien : A670

Number of Invoices + : 2,002.07

 


Final Invoice Register

This is how the register looks when it is printed at the time the batch is
posted. Note that it is marked "Final."

A & R BOUTPMENT : Inveice Register Bateh #: 100594-001 1oes/s¢ Page = 2
Division: A Transaction Date ; 10/05/94 Pinal Posting Month: 20 ¥1250-30

a Invoice # Date credir Amount Description Due Date Unit # addr #
49-19740 9/12/94 azdoo 486.23, KEN'S TRUCK 10/08/54 TR1090 DOROO?
Allocation : A6580 486.23
ao-4500 © 9/01/94 A240 56.74 EWS TRUCK 9/27/94 TR1000 DORCOL
Allocation + A65a0 36.74
89-5409 9/03/94 a2aoe 228.02 Kaw’ TRUCK 9/29/94 7R1000 DORODL
Allocation + A6580 288.42
9-540 9/03/94 azdoc 34.56 KBW'S TRUCK 9/29/34 781000 DOROOL
allocation : A6580 34.56
7908 9/23/94 a2200 82.55 8/21-9/20 9723/94 RALPOL
Allocation + 46670 82.55
01-8847 9/14/94 A2400 34.88 vow, 20/14/94 SEMEOL
Allocation + A6670 26.16
909-8847 9/10/94 A2400 59.75 BURLAP 10/14/96 ‘SEMEOL
Allocation : A6570 24.82
928-8847 9/05/94 a2400 59.75 BURLAP 10/14/96 smMeo1
Allocation 1 A670 44.82

Number of Invoices 8 Tocal : 1,082.87

 

### List Of Invoices

 

 

 

 

To change an invoice that you have already entered, place any character
beside the invoice in the list of invoices on the Vendor Selection
screen.

A & R EQUIPMENT INVOICE ENTRY x12502-01
Division a Batch 100594-001

Address # RALPO1 Name

Name ~~~: Invoice # Inv Date Unit #
DOROTHY'S HEAVY HAULING 49-19740 9/12/94 TRI000
RALPH'S SEWER SERVICE 7905 9/23/94
SEMENOW UPHOLSTERING SERVICE 901-8847 9/14/94
SEMENOW UPHOLSTERING SERVICE 909-8847 9/10/94 (
SEMENOW UPHOLSTERING SERVICE 928-8847 9/05/94
ees END tet

crdi-nd Qmdid-Totals  Cmd12-Fost Invoices
Ondid-Print Register Cmdi9-Delete Batch = Roll-Page = Hame-Top of List

 

The Invoice Information section of the invoice is displayed.

O Make changes, if necessary, and press [Enter] to proceed to the
Allocation section.

From the Allocation section, press [Enter] to return to the list of
invoices.

 

 

 

 

RELEASE 2.1 QO

## CHAPTER X12-6

CANCEL INVOICES

### Introduction

Cancel invoices allows you to completely undo any number of invoices
created and posted with Invoice Entry (X12-5).

### How To Run

From the Payables Menu (X1-2), select option 6, Cancel Invoices. Enter
your division at the security gate.

Prompts for the transaction date and general ledger posting month follow.
You can change the date and month for posting. Press [Enter].

Once a general ledger month is closed, you can not post that closed month.
If you enter a month that is closed, you will see on the verification screen
that you are posting to a future month. You will be posting to that month
for the next year..

The next screen requests verification of the information just entered. If the
posting date and month are correct, press [Enter]. If not, press [Cmd3] to
go back to the previous screen and make nay changes you want. When the
date and month are correct, press [Enter]. The Vendor Selection appears.

 
     

Note: If the system is interrupted because of a power failure or
similar disaster while the batch is being posted, your data is not

corrupted. Once the system is running again, simply return to the job
that was interrupted and the posting will continue as before.


[2] X12-6 CANCEL INVOICES -

VENDOR SELECTION SCREEN

A & R EQUIPMENT SALES CANCEL INVOICES %12601-02

Division A Select Invoices
Name

- Invoice # Inv Date Unit #

cmdi-End cmdl0-Totals  Cmd12-Post Cancelled Batch
Roll-Page © Home-Top of List

 

O This screen displays all of the invoices that are in the batch of checks to
be cancelled. Since no invoices have been chosen for cancellation, the
batch is empty. To include an check on the batch, first select the
vendor that the check was written to..

RELEASE 2.1 LO


X12-6 CANCEL INVOICES [2]

By Vendor Address

Enter the address of the vendor in the "Address #" field. The Current
Transactions Detail Screen appears.

By Name

Enter the first few characters of the vendor's name in the "Name" field.
The Vendor Index appears.

Vendor Index

To select a vendor, position the cursor next to it and type any character.
The Current Transactions Detail Screen appears.

Once you have invoices are the cancellation batch, you can remove
individual invoices from the batch by positioning the cursor next to the
invoice you want to remove, typing a 'D', and pressing [Enter].

To post a cancellation batch, press [Cmd19]. A confirmation screen will
appear. Once the batch has been cancelled, press [Enter] to return to the
Payables Menu (X1-2).

Commands Available

[Cmd1} Returns you to the Payables Menu (X1-2). Note that
invoices you selected for cancellation, if any, will not
reappear when you return to Cancel Invoices.

[Cmd10] Displays the number of invoices on the cancellation batch

## X12-6 CANCEL INVOICES

and totals their amounts.
[Cmd12] Post cancelled batch.

CURRENT TRANSACTIONS DETAIL SCREEN - PAGE 1

A & R EQUIPMENT SALES CANCEL INVOICES *12601-05
Division A Page 1 Current Transactions By Due Date

ALBEQL ALBERT'S MACHINE SHOP 2400 1,245.28
Inv Date Invoice # Description Due Date Unit # Discount Amount
09/20/94 20001 WELDER REPAI 10/20/94 1 122.02
09/20/94 23042 MISC. MAIN 10/20/94 38 523.12
10/07/94 1 MISC MAINT — 10/20/94 10 100.02
10/07/94 51244 RETOOLING 10/20/94 -40 400.12
++ END (

cma3-Return Crd6-Page 2 cmd9-Invoice Number Roll-Page

 

RELEASE 2.1 LO


X12-6 CANCEL INVOICES [=]

Note: Prior to the release of DIS software, ''999999" was used to
indicate that a payables transaction had an "undefined" due date.
Most often, this was used with an invoice associated with a floored
unit. Once the unit was sold, the system automatically changed the
due date field from "999999" to the current system date.

In V8LSA, all information in the date field must be in the form of a
valid date, not "999999." To project a transaction as far in the future
as possible, enter 123150" or December 31, 2050. This is the most
distant date possible in the DIS system. Dates after December 31,
2050 will be interpreted by the computer as taking place in the 1900's.
‘Thus, ''010151" would be treated by the computer as January 1, 1951.

A more convenient solution to manually typing in "123150" every
time your purchase a floored unit can be found in entering "999" (the
largest number possible) in the "Number of Days/Due" field for the
floored vendor in Vendor Maintenance (X12-2). When the due date
field is left blank, this field will automatically be filled in with a date
999 days in the future, probably enough time for the unit to be sold.
When the unit is sold, the due date field, regardless of what it is, will
be filled in with the current system date. At this point, it will be
treated by the system as a normal payables invoice.

 

Q Position the cursor next to an invoice you want cancelled, type any
character, and press [Enter]. See the Transaction Detail Screen section
following this section for more information.

Commands Available

{Cmd3] Return to the entrance screen.
[Cmd6] Toggles between page 1, page 2, and page 3 of the
Transaction Detail Screen. These screens are illustrated


Le] X12-6 CANCEL INVOICES

[Cmd9]

co

below.

Toggles sorting method between due date and invoice
number. The sorting method appears in the upper-right
comer of the screen.

To review invoices with a particular due date, set the
sorting method to date and enter a due date in the "Start"
field below in the form of MMDDYY. Invoices with a due
date equal or later than the one you specified wili appear.

To view invoices with a particular invoice number, set the
sorting method to invoice number, enter an invoice number
in the "Start" field below. Invoices with an invoice number
equal or later than the one you specified will appear.

RELEASE 2.1 LO


X12-6 CANCEL INVOICES [7 |

CURRENT TRANSACTIONS DETAIL SCREEN - PAGE 2

A & R BQUIPMENT SALES CANCEL INVOICES x12601-06
Division A Page 2 Current Transactions By Due Date
F
ALBEQ1 ALBERT'S MACHINE SHOP A2400 1,145.28
Inv Date Invoice # Id Tn Date G/L Mth Amount Taxl Amount Tax2 amount
09/20/94 20001 10/05/94 = 10/94 10.01 5.87 122.02
09/20/94 23042 10/05/94 10/94 88.12 55.01 523.12
10/07/94 1 10/07/94 10/94 100.02
10/07/94 51244 10/07/94 = 10/94 400.12
** END **

Start ..:

md3-Return Cmd6~Page 3 Cmd9-Invoice Number Roll-Page

 

This screen displays each invoice's date, number, transaction date, G/L
month, Tax] amount, Tax2 amounts, and total.

Press [Cmd6] to toggle between each of the three Current Transactions
Detail Screens.


 

CURRENT TRANSACTIONS DETAIL SCREEN - PAGE 3

A & R EQUIPMENT SALES CANCEL INVOICES *12601-07
Division A Page 3 Current Transactions By Due Date

ALBEO] ALBERT'S MACHINE SHOP 2400 1,145.28
Inv Date Invoice # Date/Mth/Merge Check No Batch No. Type
09/20/94 20002 7021 .
09/20/94 23042 9921 T
20/07/94 40245 9922 v
10/07/94 51244 10022 v
** END

Start ..:

Cmd3-Return Cmd$-Page 1 Cmd9-invoice Number Roll-Page

 

This page displays the each invoice's date, number, merging date, check
number, batch number, invoice or credit flag, and amount.

Press [Cmd6] to toggle between each of the three Current Transactions
Detail Screens.

The type field can be one of four values.
Cc Transaction came from a check
T Transaction came from an invoice

RELEASE 2.1 CO


P Transaction came from a partial payment
blank Transaction came from Create Source Documents, not
payables.

INVOICE DETAIL SCREEN

A & R EQUIPMENT SALES CANCEL INVOICES x12601-09
Division A
ALBEO1 ALBERT’S MACHINE SHOP 2400 1,145.28
G/L Transactions for Invoice : 20001

Id Date Mth Document D/C Acct # E Amount Description Addr # Unit #
10/05/94 10 20002 c aaaoo OP 122.02 WELDER REPAI ALBEO2
10/05/94 10 20002 A2760 10.01 WELDER REPAI ALBEOL
10/05/94 10 20001 A270 5.87 WELDER REPAI ALBEOL
10/08/94 10 20002 AG600 90.22 WELDER REPAT
10/05/94 10 20001 6590 15.92 WELDER REPAI

w+ END t*

Cma3-Return Omd6-More Fields  Gmdi9-Cancel Inv. Rolll-Page

 

O Having selected an invoice, review the G/L transactions associated with
it. Use [Roll], if necessary, to view additional pages of transactions.

O To cancel the transaction, press [Cmd19]. When the confirmation


X12-6 CANCEL INVOICES eo

screen appears, type "Y" and [Enter]. You will return to the Vendor
Selection Screen.

COMMANDS AVAILABLE
[Cmd3] Retum to the Current Transactions Detail Screen. Use this
option if you do not want to cancel this receipt.
[Cmd6] Toggles between two pages of displayed information. The

second page displays the transaction's address number,
unite number, vendor name, due date, and discount.
[Cmd19] Cancel the invoice.

RELEASE 2.1 Lo

## CHAPTER X12-7

PRINT PAYABLE CHECKS

### Introduction

While Print Payable Checks is running, no other payables jobs are
available.

Print Payable Checks is selectable by:
= Due date

= Including or Excluding (bypassing) vendors

= G/L account, or

= Group code, or

= Vendor address number

Up to 3 lines of comments can be printed on each check. Comments can
be the same for all vendors (global) or different for each vendor.
Transactions can be displayed by due date or invoice number for any
vendor who has been included. Discounts can be removed for all vendors
or for an individual vendor, and they can be restored for individual
vendors.

The Check Register is printed before checks. In this chapter, you'll find
examples of both. For information about answering messages associated
with checks and check alignment, please see the instructions regarding
your printer, which can be found in the APPENDIX of the User Manual.

      

Note: If the system is interrupted because of a power failure or
similar disaster while the batch is being posted, your data is not

corrupted. Once the system is ranning again, simply return to the job
that was interrupted and the posting will continue as before.


[2] X12-7 PRINT PAYABLE CHECKS C

### How To Run

From the Payables Menu (X1-2), select option 7, Print Payable Checks.
Prompts for the transaction date and general ledger posting month follow.
You may change the date and month for posting. Press [Enter].

Once a general ledger month is closed, you can not post to that closed
month. If you enter a month that is closed, you will see on the verification
screen that you are posting to a future month. You will be posting to that
month for the next year.

The next screen requests verification of the information just entered. If the

posting date and month are correct, press [Enter]. If not, press [Cmd3] to

go back to the previous screen and make any changes you want. When the (
date and month are correct, press [Enter]. The Select Transactions screen

appears.

RELEASE 2.1 LL


X12-7 PRINT PAYABLE CHECKS [2]

SELECT TRANSACTIONS SCREEN

A & R EQUIPMENT SALES CHECK ENTRY x12701-01
Division a Select Transactions

Invoices Due On or Before -
Check Date .

First Check er.
Include or Bypass Vendors .

Print Detail on Check Stub
Print $0.00 Checks

Select by 2 1-G/L Account

2-Group Code
3-Address Number

Comment on Amount (Currency Type)

Comments for Stub

 

 

 

 

 

Enier the due date you want to include in this check run. Enter March
21, 1995 as 032195 and press [Field Exit].

O Enter the date you want to print on the checks. This date can be
changed for individual checks.

All vendors who meet the selection criteria will be listed in the
following screen. If "I" is entered in the Include or Bypass field, you
will have to select the vendors to be included in the batch with an "I."
If "B" is entered in the Include or Bypass field, you will have to select
the vendors to be bypassed (excluded) in the batch with a"B." If you
have chosen to bypass vendors, checks for all vendors will be printed

 

 

 

 

 


[+] X12-7 PRINT PAYABLE CHECKS c

except for those you selected.

O1 If you want invoice details printed on the check stub, accept the default

of "Y"; otherwise, key in "N."

You can choose to print zero balance checks or not. If you select '"N"

not to print balance checks, no check will be printed and the check

register will list "NO CHK” for that check number and no transaction
will be posted. If you select "Y"' to print zero balance checks, the
system will issue a check number in sequence and post to all
transaction files exactly like non-zero balance checks.

O Key in the first check number. The first check is printed will be the
number you enter here incremented by one (the system assumes that
one check is used to align the printer)..

O Indicate whether you want to select checks to print by:

1 = General ledger account (ALL, Trade, Flooring, or individual G/L

accounts. The next screen will allow you to select ALL, Trade, (
Flooring, or up to 10 general ledger accounts. See SELECT BY G/L
ACCOUNT SCREEN.

2 = Group code, in which case, the next screen will allow you to select

up to 10. See SELECT BY GROUP CODE SCREEN.

3 = Individual vendor addresses. The next screen will allow you to

select up to 10. See SELECT BY ADDRESS NUMBER SCREEN.

O Enter up to 5 characters to describe the type of currency, such as "U.S."
or "Can." (Optional) This code can be changed for individual checks.

Qi Type up to 3 lines of comments, which will apply to all vendors
(global) unless changed (Vendor Parameters). Each line holds 60
characters. These comments can be changed for individual checks.

 

 

 

 

 

 

An example of a completed Select Transactions screen follows:

i
RELEASE 2.1 Ne

## X12-7 PRINT PAYABLE CHECKS

A & R EQUIPMENT SALES CHECK ENTRY x12701-01
Division A Select Transactions

Invoices Due On or Before ... 103194
Check Race 102894
20086

Include or Bypass Vendors

Print Detail on Check Stub .
Print $0.00 Checks.

Select by 2 1-G/L Account
2-Group Code
3~Addxess Number

 

 

Comment on Amount (Currency Type) . -S. -
Comments for Stub

THERE ARE 3 LINES OF 60 CHARACTERS EACH AVAILABLE FOR YOUR

COMMENTS WHICH WILL BE PRINTED ON THE CHECK STUB, SUCH AS:

WE ARE PAYING WHAT WE CAN THIS MONTH, MORE WILL COME LATER.

omdl-End

 

O If you want to end the job and cancel the entries on this screen, press
[Cmd1]; otherwise, press [Enter] to continue. Depending on how you
want to select the vendors, you will be taken to one of the following
screens: Select by G/L Account, Select by Group Code, or Select by
Vendor Address. Ali 3 screens are described on the following pages.


Ls] X12-7 PRINT PAYABLE CHECKS

SELECT BY G/L ACCOUNT SCREEN

 
  

  

A & R EQUIPMENT SALES CHECK ENTRY
Division A Selection by General Ledger Account

x12701-02

   
     
  
  
  
  
   

Enter : ALL = All Payable Vendors ......... eet
T = Only Trade Payable Vendors
F = Only Flooring Payable vendors

or
Specific General Ledger Accounts .....-.--..-...-- :

 
      

Cmdi-End  Cma3-Previous Screen

  

Q) To print checks for all general ledger accounts with edit codes “P" or
"F," enter "ALL."

Oi To print checks for all trade payables accounts (edit code=P), enter "T."
O To print checks for all flooring accounts (edit code=F), enter "F."

Oj To print checks for any combination of trade payables and flooring
accounts, key in up to 10 specific account numbers in the spaces
provided. Press [Enter]. The Adjust Vendors screen displays the
selected vendors.

 
LC


X12-7 PRINT PAYABLE CHECKS [7]

SELECT BY GROUP CODE SCREEN

A & R EQUIPMENT SALES CHECK ENTRY X12701-03
Division A Selection by Group Code

Enter Group Codes _.

€méi-End  Cmd3~Previous Screen

 

O To print checks for any combination group codes, key in up to 10
specific group codes in the spaces provided. Press [Enter]. The Adjust
Vendors screen displays the selected vendors.


 

SELECTION BY ADDRESS NUMBER SCREEN

A & R EQUIPMENT SALES CHECK ENTRY *212701-04
Division a Selection by Address Number

Enter Address Numbers

Cmdl-End  Cmd3-Previous Sereen

 

 

 

 

 

 

To print checks for any combination of vendors, who may be attached
to various general ledger accounts, key in up to 10 specific vendor
system addresses in the spaces provided. Press [Enter]. The Adjust
Vendors screen displays the selected vendors.

RELEASE 2.1 C


ADJUST VENDORS SCREEN

A & R EQUIPMENT SALES CHECK ENTRY x12703-01
Division a Adjust Vendors Include

Enter address # for which to display transactions ...: DOROOL

Rame --~ amount Discount check,
ALBERT'S MACHINE SHOP ALBEOL 5433.36 5.29 5428.07
ALLKINDS INSURANCE COMPANY  ALLKO1 100.44 100.44
BLUDGETT MANAGEMENT BLUDOL 100.

DOROTHY'S HEAVY HAULING DOROO1 : 220.90 2200.30
LEE‘S PLUMBING & HEATING LEESO1 980. 4.20 976.06
RALPH'S SEWER SERVICE RALPOL 82. 82.55
STARBUCK'S COFFEE STAROL 56. 56.88
SUNFLOWER TRACTOR COMPANY © SUNFO1

WEST COAST GRAPHICS WESTOS

tee END «=

Gmdl-End Cmd8-Global Parameters Cm 10-Totals (md12-Post Checks
Cmdi9-Remove Discounts = Roll-Page Home-Top of List

 

O In the top right comer, you'll see either "Include" or “Bypass”
depending on your choice on the entrance screen. If you are
“Including,” mark the vendors you want to include by typing "I" beside
their names. The rest of the vendors will be excluded. If you are in
"Bypass" mode, mark the vendors you want to bypass by typing "B".
The rest of the vendors will be included.

O To display transactions for a particular vendor or change the detail that
will appear on the stub, type the system address number at the prompt:
“Enter address # for which to display transactions." See UPDATE

X12-7 PRINT PAYABLE CHECKS _
co

TRANSACTIONS.
O To change what will appear on the stub for all vendors included in this
check run, press Cmd8-Global Parameters. See Global Parameters.
To see totals of all checks that are included in this check run, press
Cmd10-Totals. See Totals.
O To proceed with posting and printing checks, press Crmd12-Post
Checks. See Post Checks.
To remove all discounts displayed on this screen, press
Cmd19-Remove Discounts. Discounts can be recalled for individual
dealers and specific invoices from the Display Transactions screen. See
UPDATE TRANSACTIONS.

 

 

 

 

 

 

RELEASE 2.1 LO


Global Transactions: Update Check Parameters

O From the Adjust Vendors screen, press [Cmd8] to change the same
items that appeared on the entrance screen (except due date selection)
for all vendors included in the current check run. The Update Check
Parameters screen displays the choices made on the entrance screen.

 
     
 
   
    
 
 
 
   
  

  

   

A & R EQUIPMENT SALES CHECK ENTRY x12703-02
Division A Update Check Parameters

Type of Currency 6.0.62... cece eee eee
Stub Comments ....

THERE ARE 3 LINES OF 60 CHARACTERS FACH AVAILABLE FOR YOUR
COMMENTS WHICH WILL BE PRINTED ON THE CHECK STUB. SUCH AS:
WE ARE PAYING WHAT WE CAN THIS MONTH, MORE WILL COME LATER.

      
 
   

Invoices Due on or Before ........: 10/31/94

   

Cmd3-Return  Enter-Update

 

 

 

Make changes as necessary, and press [Enter] to update and return to
the Adjust Vendor screen; otherwise, press [Cmd3} to return without
making changes.

 


[2] X12-7 PRINT PAYABLE CHECKS

Totals

From the Adjust Vendors screen, press {Cmd10] to see totals for the
vendors included in the current check run.

A & R EQUIPMENT SALES 12703-09
Division &

Number of Checks
Total amount : 9,074.69
Total Discount ! 230.39

Check Total : 8,844.30

*** Press any character to continue ***

 

 

 

No changes can be made on this screen. Press any key to return to the
Adjust Vendor screen.

 
Co


X12-7 PRINT PAYABLE CHECKS [2]

Post Checks

CO) When you are ready to post and print checks, press [Cmd12]. The
following verification message is displayed:

 
      

   
  
   
  
    

A & R EQUIPMENT SALES CHECK ENTRY
Division A Post Checks

*12703-05

 

Post Cheeks

Confirm ..: N (Y/N)

 

Cnd3-Return — Enter-Confirm

 

 

 

 

To return to the Adjust Vendor screen, press [Cmd3].

O To proceed with posting and printing type "Y" and press [Enter].
Posting begins. Progress can be monitored as the 10 job steps are
displayed. The screen is released at the end when you are prompted to
press [Enter]. You will return to the Payables Menu.


X12-7 PRINT PAYABLE CHECKS.

Check Register

‘A & R EQUIPUENT SALES Check Register 19/10/94 Page
Division: & G/u Month: 16/94 Transaction Data: 10/20/94 1270-08

check # vender wame- * Addr § G/L Account Check Date stub Amount comments?
Inv Date Invoice # Rescription Due Date Unit 4 Anoune Discount

ALBERT'S MACHINE SHOP ALREOL A240 aorsssa oy :
520/94 12422 REPAIR 9727/94 10.00 : 5.99

5026094 22082 Isc. MAIN 16/20/94 $23.12 . 3922.74

1oo7/34 si24e RETOOLING 19/26/96 400.12 : 399.72

3ovoe/9g 513245, REPAIR 15/25/94 4,800.12 : 4,495.62

tot check Totals : 5,433.36 - 5,428.07

DoHOTHH'S HEAVY HAULING ronorn azeoo = araseoe ous.
Troeise saeceaves so-smsatonm 6/31/24 empeas 349.76 nats
drosist ancesco.” anes sauce, Syztreu teenga S494 0?
syairse ga-oase kava omic S/a9/36 Thies «260 eh : 29.57
barat ta-tamwy ars Tauck rovcerad tases 466.28 foe
vorociss nas Guten doves amos seacag nace

LEE'S PLUMBING & HEATING LeEsoL azace ores oy
9705/94 SA-1GC475 ORIN CLEAN 19/95/96
920194 soat2 MISC. WORK 16/16/96
19/05/94 $6123 HEATER NST 16/26/96
st) check Totals

RALPH'S SEWER SERVICE RALPOL A2406 aorzaree
9/23/94 7905 8721-9720 923794
“s+ Shock Totals
STAREUCE'S COFFEE STAROL a2400 1or2gres vs.
2/20/24 GSK-2846 — SPRPF COFFEE 3/20/94 55.58 56.28
‘t+ Check Totals 20062 + 36.88 56.88

s+ Grand Totals : 9,074.69 5,344.30

General Ledger Summary

G/L Account. Ceseription- Debits credits
020 CASH IN BANK, 8,844.36
2400 PAYABLES 9,074.69
asaa0 CASH DISCOUNTS EARNED 230.39

9,974.69 9,678.68

 


MO3HO BNILISOdIa IUO4TE SNLS SIHL HOVIaG

id reas jaded ay} uo pL UM Uoljesopad 1Yysy UBIY

 

SE IXG PILO-T2s (00g) aus TOL YO ELEZ-EfZ INOHd (GR-Z) £890 # WHOS NOLVYOdOD SWHLSAS NOLVAMOINI Y3TV3C

PRINTED IN U.S.A.


 

 

 

 

t
a)


16 | X12-7 PRINT PAYABLE CHECKS

### Update Transactions

 

 

 

At the "Enter address # for which to display transactions" prompt on
the Adjust Vendors screen, type the system address number of a vendor
who is included in this check run. The Update Transactions screen
displays current invoices in order by due date.

 

A & R EQUIPMENT SALES CBECK ENTRY ¥12703-03
Division A Update Transactions By Due Date

DOROTHY 'S HEAVY HAULING DOROOL =. 2421.20 220.90 2200.30
Invoice # Inv Date Description Due Date Unit # amount Discount
984-G076i 7/06/94 JO-BREAKDOWN 8/31/94 UTOO7S 34976 3498
89-4500 9/01/94 KEN'S TRUCK 9/27/94 TR1000 5674 567
89-5409 9/03/94 KEN'S TRUCK 9/29/94 TR1000 28841 2884 (
49-19740 «9/12/94 KEN'S TRUCK 10/08/94 TR1000 46623 4662
10689 10/05/94 MISC. WORK 10/20/94 100066 7885
128-99 10/04/94 DITCH 10/30/94 TR1000 25940 2594
jee END tHe

Cmd3-Return Cmd8-Vendor Parameters Cmd9-Invoice Number
Cmdl6-Recall Cmd19-Remove Discounts  Roll-Page — Home-Top of List

 

O To change check date, print detail (Y/N), type of currency, or stub
comments for this check, press Cmd8-Vendor Parameters. See Vendor
Parameters.

To display invoices by invoice number, press [Cmd9}.

 

 

 

 

RELEASE 2.1 CC


 

 

 

To recall discounts and transaction balances for all invoices for this
vendor, press Cmd16-Recall. You might use this command key if all
discounts were removed on the Adjust Vendors screen or if you used
Cmd19-Remove Discounts on the current screen. Also, it is used to
recall original amounts, which may have been removed or reduced as
you decided what to pay in this check run.

O To remove discounts from all invoices for this vendor, press
Cmd19-Remove Discounts. A confirmation message is presented.

 

Vendor Parameters: Update Vendor Parameters

O On the Update Transactions screen, press [Cmd8] to change the
parameters displayed below for the current vendor only.


| 18 | X12-7 PRINT PAYABLE CHECKS a

A & R EQUIPMENT SALES CHECK ENTRY x212703-04
Division A Update Vendor Parameters

» 102594

Type of Currency

Stub Comments

COMMENTS CAN BE DIFFERENT FOR EACH VENDOR

Cmd3-Return  Enter-Update

 

 

To return to the Update Transactions screen without making any
changes, press [Cmd3].

Change any of the items for this vendor only, then press [Enter] to
update and return to the Update Transactions screen.

 

 

 

 

 

RELEASE 2.1 WS

## CHAPTER X12-8

ENTER MANUAL CHECKS

### Introduction

### Preparation

Enter Manual Checks allows you to process checks for transactions for
one-time payables customers who will not have a payables address. These

O From the Payables Menu (X12) select option 2, Vendor Maintenance,

© For the payables address, enter "ddd999," where dis your division. For
example, division A's payables address for manual checks would be
"AAA999"; division B's would be "BBB999."

Press [Enter]. The vendor maintenance screen appears.

## X12-8 ENTER MANUAL CHECKS

   
    

LEE'S RENTAL COMPANY: ‘VENDOR MAINTENANCE x12201-02 2
Division: A SCREEN #1

   
  
    

gotal Balance. .-
pate Entered.
Last Invoice

   
 
     
   

 

Invoice #.

 
 
  

    

city,
Zip code.
Telephone #..
Work Phone #.

Amount
Last Check.

check

Ext. Amount. .

   
 

     
    
 

 

   

  

G/L Account #...
Taxi Account #.-
Tax2 Account #..

  
      
  
    
   

1234567890 Terms. .-+

seeeeee v A

cmd3-Return cmdé-Note Enter-Next Page

 
 

1 Complete the name and G/L account fields. Note: the G/L account
you enter in this screen is only a default. It can be changed at the time
when each manual check is written. Once you have finished, press
[Enter] three times and [Cmd1] to return to Payables menu.

O For more information on posting a manual check, see the Posting
Manual Check section at the end of this chapter.

 


X12-8 ENTER MANUAL CHECKS [=]

### How To Run

From the Payables Menu (X1-2), select option 8, Enter Manual Checks.
Enter your division and password at the security gate.

Prompts for the transaction date and general ledger posting month follow.
‘You can change the date and month for posting. Press [Enter].

Once a general ledger month is closed, you can not post that closed month.
If you enter a month that is closed, you will see on the verification screen
that you are posting to a future month. You will be posting to that month
for the next year.

The next screen requests verification of the information just entered. If the
posting date and month are correct, press [Enter]. If not, press [Cmd3] to
go back to the previous screen and make any changes you want. When the
date and month are correct, press [Enter]. The Vendor Selection Screen
appears.

      

Note: If the system is interrupted because of a power failure or
similar disaster while the batch is being posted, your data is not

corrupted. Once the system is running again, simply return to the job
that was interrupted and the posting will continue as before.

 
     


[+] X12-8 ENTER MANUAL CHECKS a
(

### Vendor Selection Screen

A & R EQUIPMENT SALES ENTER MANUAL CHECKS x12802-01
Division A vendor Selection

Cmil-End = Gmi0-Totals © Cmd12-Fost Checks
Roll-Page Home-Top of List

 

O This screen displays the batch of checks that are ready to be processed.
Since no checks have been generated yet, the batch is empty. To
include a check on this batch, you must select the vendor who will
receive the check. There are two ways of doing this.

RELEASE 2.1 LO


By Address

X12-8 ENTER MANUAL CHECKS [=]

Enter the vendor address in the "Address #" field. The Check Information
Screen, detailed below, appears.

By Name

Vendor Index

Enter the vendor name in the "Name" field. The Vendor Index will be
displayed, starting with the closest match of the name you chose.

To select a vendor, place any character next to the vendor's name. Do not
press [Enter], The vendor's current transactions are displayed

automatically.

Command Options

[Cmd1]

[Cmd10]

[Cmd12]

[Roll]
[Home]

Returns you to the Payables Menu (X1-2) without
processing the checks.

Displays statistics on the batch of checks, including check
number (number of checks), total amount (of invoices),
total discounts, and total of checks. Press [Enter] to return
to the Vendor Selection Screen.

Post the batch of checks. Type "Y" and [Enter] at the
confirmation screen. Wait until the checks are processed
and press [Enter] to return to the Payables Menu (X1-2).
Scroll up and down the batch of processed checks.

Return to the beginning of the batch of processed checks.


L*] X12-8 ENTER MANUAL CHECKS co

### Check Information Screen

A & R EQUIPMENT SALES ENTER MANUAL CHECKS %12801-01
Division A Vendor Selection
AA & R EQUIPMENT SALES ENTER MANUAL CHECK
12801-02
Division A Check Information
B
Check Number
Date of Check .
Check Amount ....
Print Check ...

Address # : ALBEOL

Address (Ext)
City, State .., Zip -:

Transaction Description
Print Stub Detail ..
Type of Currency

Stub Comments ...

md3-Return Cmd19-Delete Check

 

OC Complete as many fields as you can. The "Check Number," "Date of
Check," and "Check Amount" fields must be completed, though "Date
of Check" and "Check Amount” can be changed at a later time. Enter
the "Date of Check" field in the form of MMDDYY.

O Key in another description to override the default “Check X12-8" in the
“Transcription Information" field, if desired. The contents of this field

{
RELEASE 2.1 Ve


X12-8 ENTER MANUAL CHECKS [7]

will become the "Description" field for G/L postings associated with
the check.

O If you want a invoice details printed on the check stub, accept the
default of "Y" in the "Print Detail on Check Stub Vendors." Otherwise,
key ina "N."

1 Enter up to 5 characters to describe the type of currency, such as "U.S."
or "Can." (Optional). This code can be changed for individual checks.

O Type up to 3 lines of comments, if desired.
Press [Enter]. The Check Detail Screen appears.

Command Options

{Cmd3] Return to the Vendor Selection Screen. Check detail totals
and check amounts must equal one another to return to this
screen.

[Cmd19] Delete the check. To delete it, type "Y" at the confirmation
and press [Enter].


 

### Check Detail Screen

A & R EQUIPMENT SALES ENTER MANUAL CHECKS x12801-03
Division A Check Detail

Check # 600100 WEST COAST GRAPHICS

Vendor Amounts Included
Invoice # Inv Date Unit #
** END

Total of Check Detail:
cmd3-Return cmd5-Check Information Cmd6-Add Invoices
cmd?-Vendor Transactions Cmdl9-Delete © Roli-Page Home-Top of List

 

The text highlighted at the top of the screen refers to the check you are
now generating. The dollar amount at the far left of this line refers to the
current amount of that check. This value is taken from the "Amount" field
you entered in the Check Information Screen until you add a new invoice
in Add/Update Invoices ot pay existing invoices in Vendor Transactions.

Before Add/Update Invoices or Vendor Transactions:

Check amount= "Amount" field in the Check Information Screen

RELEASE 2.1 C


X12-8 ENTER MANUAL CHECKS [e]

After Add/Update Invoices or Vendor Transactions:

Check amount = Total of new invoices in Add/Update Invoices +
Total of existing invoices in Vendor Transactions

The "Vendor Accounts Included" field located near the top of the screen is
the total of ali Open payable invoices that are included in the check. It
does not include any invoices you might have created with Add/Update
Invoices.

Below the "Vendor Accounts Included" field is a list of all the invoices
you have created with "Add/Update Invoices." To change or delete an
invoice, use [Tab] and [Shift}-[Tab] to Position the cursor next to the
appropriate invoice and type a character. Refer to the Add/Update Invoice
Section following for information on this screen..

If the check you are writing is full or partial payment of an open
payable transaction press [Cmd7] or a full payment of an invoice you
have not yet added to the system press [Cmd6]. Note that a manual
check can be a Payment of both new and existing invoices.

Commands Available
[Cmd3} Return to the Vendor Selection Screen, In order to do this
check detail totals and check amounts must equal one
another.
[Cmd5] Displays the Check Information Screen detailed above.
[Cmd6] Displays the Add/Update Invoices Screen detailed below.
[Cmd7] Displays the Vendor Transactions Screen detailed below.


{Cmdi9} Deletes the current check. To delete the check, type "Y"
and press [Enter] at the confirmation screen. You will


 

ro
'
return to the Vendor Selection Screen.
[Roll] Scrolls up or down the list of new invoices.
[Home] Displays the beginning of the list of new invoices.
ADD/UPDATE INVOICES SCREEN - PAGE 1
ADD/UPDATE INVOICES
WESTOS WEST COAST GRAPHICS
Terms: 2
Net
Number Days Due
Credit G/L Account =:
Taxl..:
Tax2..
Discount on Taxl.: N Tax2: N (

INVOICE INFORMATION

Invoice Number
Invoice Date
Invoice Amount
Taxl Amount -
Tax2 Amount .
Description -
Discount .

Due Date -
Unit Number

Help-Command Keys

 

RELEASE 2.1 Le


X12-8 ENTER MANUAL CHECKS [J

  
     

   
 

"999999" was used to
indicate that a payables transaction had an "undefined" due date.
Most often, this was used with an invoice associated with a floored
unit. Once the unit was sold, the system automatically changed the
due date field from "999999" to the current system date,

In V8LSA, all information in the date field must be in the form of a
valid date, not "999999." To project a transaction as far in the future
as possible, enter "123150" or December 31, 2050. This is the most
distant date possible in the DIS system. Dates after December 31,
2050 will be interpreted by the computer as taking place in the 1900's.
‘Thus, 010151" would be treated by the computer as Janua

A more convenient solution to manually typing in ''123150" every
time your purchase a floored unit can be found in entering "999" (the
largest number Possible) in the "Number of Days/Due" field for the
floored vendor in Vendor Maintenance (X12-2). When the due date
field is left blank, this field will automatically be filled in with a date
999 days in the future, probably enough time for the unit to be sold.
When the unit is sold, the due date field, regardless of what it is, will
i late. At this point, it will be
payables invoice.

  
  

  
     
  
  
  

   
   
   
   

 
   
   
    
   
    
    

   
 
 
      
    
 
 
  
 

 
 
  

O Use [Tab] and {Shift]-[Tab] to move through the displayed fields. The
“Invoice#," "Date" and "Amount" fields must be completed. Fill in the
date in the form of MMDDYY and press [Field Exit] to right Justify the
field. Fill in the "Amount" field without a decimal and Press [Field
Exit] to right justify the field.

Fill in as many of the other fields as you can and press [Enter]. The
following screen appears,

COMMANDS AVAILABLE


[2] X12-8 ENTER MANUAL CHECKS _
(

[Cmd3] Return to the Check Information Screen.

(Cmd6] Display the Configuration Screen. This screen displays the
default G/L distribution for the selected vendor.

[Cmd19] Cancel the invoice.

ADD/UPDATE INVOICES SCREEN - PAGE 2

ADD/UPDATE INVOICES ALLOCATION F
G/L Acct Amount: Addy # Unit #
ALBEO] ALBERT'S MACHINE SHOP 1- A6600 54910
Texms : .i0 % 10 Days 2-
Net 15 Days 3-
Number Days Due 30 Days 4
Credit G/L Account = Se
=
_
Discount on Taxl.: N Tax2: N 8-
INVOICE INFORMATION o-
2 Q 10-
Invoice Number ..: 10 le
Invoice Date 10/10/94 12-
Invoice Amount ~ 549.10 13-
‘axl Amount - 14-
Tax2 Amount . 15-
Description - 16-
Discount .. 17-
Due Date .. 48-
‘Unit Number - i9-
20-
Help-Command Keys

  

1 Fill out the G/L distribution for the new invoice. Default G/L accounts
are taken from the distribution list in Payables Maintenance (X12-2). If
necessary, use [Tab] or [Shift]-[Tab] to position the cursor in the
appropriate field. Remember to fill in the "Amount" field without a
decimal and to press [Field Exit] to right justify the fields contents

RELEASE 2.1 CU


X12-8 ENTER MANUAL CHECKS Ls]

when you have filled it in. Press {Enter} when you are done. You will
return to the Check Detail Screen.

Commands Available


[Cmd3]} Return to Add/Modify Invoices Screen - Page 1.
[Cmd6] Display default G/L distribution for the selected vendor.
[Cmd8] Display G/L Account Index.

[Cmd10] Display the description fields for ail the G/L accounts in the
distribution list.

[Cmd19] Delete the current invoice. The invoice must exist to be
deleted. Press [Cmd3] twice to return to the Check Detail
Screen without saving the current invoice.

This screen displays an index to all of your G/L accounts. Each account's
edit code (if any) and type is also displayed.

O Use [Tab] and [Shift]-[Tab] to position the cursor at a G/L account you
want to include in your distribution list. Type any character.

Use [Roll] to scroll the index up or down. To display another page of
the index, [Tab] over to the "Next Page Starts" and type ina G/L
account and press [Enter]. This will let you move very quickly through
the index.

If you do not want to include an additional G/L account in the
distribution list, press [Cmd3] to return to Add/Modify Invoice Screen -
Page 2.


[J X12-8 ENTER MANUAL CHECKS Cc

### Vendor Transactions Screen

A & R EQUIPMENT SALES ENTER MANUAL CHECKS x12801-04
Division A Transaction Selections By Due Date

Check # 10012 BLIDGETT MANAGEMENT But 504.99

vendor Amounts Included
Invoice # Due Date Unit # Amount Discount
24500 9708/54 100.40
27002 9/20/94 213,22
27150 9/21/94 55.12

++ END **
Position to :
(mi3-Return Cmé9-Inveice Number -- Roll-Page Home-Top of List

 

CO If unpaid invoices exist for this vendor, they will appear on this screen.
Fill in the amounts and discounts that will be paid with the manual
check. Enter all amounts without a decimal and be sure to press [Field
Exit] when finished with each field. When you are finished press
{Cmd3].

Press [Cmd9] to toggle between two sorting methods: by due date or
by invoice number. The current sorting method is displayed in inverse

RELEASE 2.1 LL


X12-8 ENTER MANUAL CHECKS [=]

text in the upper-right comer of the screen.

To review invoices by a specific invoice number, set the sorting
method to "By Invoice Number" with [Cmd9]. Enter an invoice
number in the "Position to" field. Invoices with an invoice number
equal or greater than the number you entered will be displayed on
screen.

To review invoices by a specific due date, set the sorting method to "By
Due Date" with [Cmd9]. Fill in the “Position to" field with a date in
the form of MMDDYY. Invoices with a due date equal or greater than
date you entered will be displayed on screen.

### Posting A Manual Check

This section describes the procedure for Posting a manual check, Refer to
the previous section for Specific information about any of tthe screens or
fields used in this procedure.

O From the Payables Menu (X12) select option 8, Enter Manual Checks.
Pass through the security gate. The Vendor Selection screen appears.


| 12-8 ENTER MANUAL CHECKS c

  
   
 
     
 
 

 
  

ENTER MANUAL CHECKS x12801-01

vendor Selection

 
 
 
  
      

UBE'S RENTAL COMPANY
Division A

- Addr # I Chk Date Discount

  

cqrdt-Ena Cd 0-Totals —Cmsi12-Post Checks
Roll-Page Home-Top of List

CO Enter the address of the payables vendor you prepared for manual
checks. See the "Preparation" section at the beginning of this chapter
for more information. The payable address will be in the form of
ddd999, with d being your division. Division A's payable vendor for
manual checks would be AAA999. Press [Enter]. The following

screen appears.

{
RELEASE 2.1 Ke


 

    
 
 

 
 
   

  

LEE'S RENTAL COMPANY
Division a

ENTER MANUAL CHECK
Check Information

*12801-02

  
  

Check Number .,
Date of Check |
Check Amount
Print Check ...

 
      
  
  

   
 

Address 4: AAA999 Name...
Name (Ext)
Address ....
Address (Ext)
City, State .., zip |

Bank Account ..,..... |

Transaction Description

Print Stub Detail ...

Type of currency

Stub Comments .__,,

 
 

    
 

    

 
    
     
  

  

Cna3-Return cmd19-Delete check

  

O Complete all the appropriate fields on this Screen. The Check Number,
Date of Check, Check Amount, Name, and Bank Account fields must
be completed. Other fields are optional. Press {Enter}. The Check
Detail screen appears.


    
         
 

LEE'S RENTAL COMPANY ENTER MANUAL CHECKS x12801-03

Check Detail

   

Division A

 

 
 

BAAG99 100.25

 
 

check # 109900 HAROLD UNLAND

  
     
   

  
 

vendor Amounts Included

Invoice # Inv Date Unit # Amount Discount

se END **

 
 
   

total of Check Detail:
end3-Return md5-Check Information cmd6-Aad 1:
nransactions Cmal9-Pelete Roll -Page Home-Top of List

mvoices cmd7-Vendor

  
 
     

C Now, add an invoice for the check you just entered. Press (Cmd6].
The add/update invoices screen appears.

RELEASE 2.1 CO


 

  

ADD/OPDATE INVOICES

 
    
   

 
    

AAAS99 MISCELLANEOUS

Terms: & Days
Net,
Number Days Due Days
Credit G/L Account ; a2400

Taxl..:

Tax2
Discount on Taxl.: N Tax2: Ny

INVOICE INFORMATION

   
   
   

    
     
    
  

 
  

 
 
 
 

Invoice Number
Tavoice pate
Tnvoice Amount .

 

Description
Discount
Due Date

 
   
     
  
 

© Fill out as many fields as are appropriate. The Invoice Number,
Invoice Date, Invoice Amount fields must be completed, Press {Enter}

    
  

   
 

Note: If there is a discrepency between the check amount and the
invoice amount, the amount of the check will be adjusted to equal the
amount of the invoice,


20 | X12-8 ENTER MANUAL CHECKS

  

  
 

ADD/UPDATE INVOICES

  
     

(RAAI99 MISCELLANEOUS VENDOR

   
      

Terms: % Days

Net Days
Number Days Due Days
credit G/L Account + A2400

 
 

 
 

 
 

‘Taxh
Tax2.

 
    
     

INVOICE INFORMATION
TD ceeeeeeeeee :

invoice Number .
Invoice Date

 
 

 

9999
3/20/95
100.25

 
 
 
 

 

 
 
 
 

Invoice Amount
axl Amount -
Tax2 Amount .

 
 

  
 
 
 
 
 

   
     
  
 

Description - CLEANING

  
 
 
  

Discount -
Due Date +
unit Number

  
  

3/20/98

  
  
  

{Enter}.

O At the Check Detail screen, press [Cmd3} to return
[Cmd12] to post the
invoice. Once the check is through posting, press

Selection Screen. Then press

the Payables Menu.

Discount on Taxt.: N Tax2:

10-
ne
12-
ae
1
as-
16-
1
18-
19-
20-

Help-Command Keys

 

G/L Acct.

ALLOCATION F

Amount
10025

Adde # unit #

U Enter all the accounts that the invoice will be distributed to. Press

to the Vendor
new check and
[Enter] to return to


X12-8 ENTER MANUAL CHECKS [=]

PRINTING CHECKS ON A DEDICATED PRINTER

S$/36

The first time you print checks on your dedicated printer after an IPL, you
will see the following message:

Sys 1404 Options (012)
On printer Pl, change to forms number CHKS ... (Pl = your
printer ID)

O Answer with a "J" to signal the computer that forms have been changed
to checks. The first line of the check will be printed and the following
message will appear.

Sys 5825 Options (012)
Align the forms in printer P11... (Pl = your printer
ID}

O if the first line is correctly printed, answer this Message with a "2" to
signal the printer to continue to print. Otherwise, realign the printer and
answer with a0." Continue answering with a "0" until the checks are
correctly aligned.

For more information on answering printing messages, consult the
appendix chapter appropriate for your printer.


[2] X12-8 ENTER MANUAL CHECKS —
(

AS/400

The first time you use your dedicated printer after an IPL, bring up the
print spool. The following message will be sent to your dedicated printer:

Message... + ? Lead form type 'STAT' device Pl. . «
(P1 = your printer ID {H C GI R)

O Answer this message with a "G" to indicate that the checks have been
loaded. The first line of the check will be printed and the following
message will be sent to your dedicated printer:

Message ..-. 3? Verify alignment on printer PRTO1. (I ¢
GN R)
O If the check is correctly aligned, answer this message with an “I" to {

signal the printer to continue printing without creating any more
messages. Otherwise, answer with a "G" to print move to print out the
same line on the preceding check. Continue answering with a "G" until
the checks are correctly aligned.

For more information on printing checks, consult the appendix chapter
appropriate for your printer.

ft
RELEASE 2.1 NY

## CHAPTER X12-9

CANCEL CHECKS

### Introduction

Cancel Checks allows you to delete any check and all of the G/L
transaction resulting from it. Checks and transactions posted prior to the
conversion to V8L5 cannot be cancelled.

### How To Run

From the Payables Menu (X1-2), select option 9, Cancel Checks. Enter
your division at the security gate and press [Enter]. Prompts for the
transaction date and general ledger posting month follow. You may
change the date and month for posting. Press [Enter].

Once a general ledger month is closed, you can not post to that closed
month. If you enter a month that is closed, you will see on the verification
screen that you are posting to a future month. You will be posting to that
month for the next year.

The next screen requests verification of the information just entered. If the
posting date and month are correct, press [Enter]. If not, press [Cmd3] to
go back to the previous screen and make any changes you want, When the
date and month are correct, press [Enter], The Select Vendor screen
appears.

 
    
      

  

Note: If the system is interrupted because of a power failure or
similar disaster while the batch is being posted, your data is not

corrupted. Once the system is running again, simply return to the job
that was interrupted and the posting will continue as before.


[2] X12-9 CANCEL CHECKS

 

SELECT VENDORS SCREEN

A & R EQUIPMENT SALES CANCEL CHECKS
Division A vendor Selection

x12901-02

D Check # * Addr # Chk Date Discount

cmdl-End cmdl0-Totals (md12-Post Cancelled Batch
Roli-Page Home-Top of Page

 

This screen displays the cancellation batch--a list of all checks that the
user has selected for cancellation. When the screen is first opened the
cancellation batch is empty. To add checks onto the cancellation batch,
select the vendor who was the recipient of the checks you want cancelled.

{
RELEASE 2.1 NY


X12-9 CANCEL CHECKS [2]

By Address Number

Enter the address number in the Address # field. Press [Enter]. The
Transaction History screen appears.

By Name

Enter the first few letters of the vendor's name in the Name field. Press
{Enter]. The vendor index is displayed.

Vendor Index

You can type all or part of the name to display an index of vendors starting
at the closest match to your request. The vendor index contains all the
names of all vendors in alphabetical order. Vendors are automatically
added to this index when they are added at Vendor Maintenance (X12-2).

To select a vendor, position the cursor next to a vendor's name and type a
character. The Transaction History screen appears.

Command Keys

[Cmd1t] Return to the Payables Menu (X1-2) without posting the
cancellation batch. The cancellation batch is erased.

{Cmd10] Displays totals of the cancellation batch. This will display
number of checks, total amount (before discounts), total
discounts, total of checks. Press any key to return to this
screen.

{Cmd12] Post cancellation batch. To post, type a “Y" at the
confirmation screen and press [Enter].

## X12-9 CANCEL CHECKS

TRANSACTION HISTORY SCREEN - PAGE 1

### A & R Equipment Sales Cancel Checks ¥12901-05

Division A = Page 1 Transaction History By Due Date

### Albeo1 Albert'S Machine Shop 42400

Inv Date Invoice # Description Due Date Unit # Discount Amount,
09/20/94 12422 REPAIR 9/27/94 -04 10.00
10/10/94 13002 Check X12-8 10/10/94 -01-
09/20/94 20001 WELDER REPAI 10/20/94 122.02
09/20/94 23042 MIsc. MAIN 10/20/94 : 523.12
10/07/94 24001 MIsc MAINT 10/20/94 100.02
10/07/94 51244 RETOOLING 10/20/94 : 400.32
09/20/94 20001 Cancel X12-6 10/20/94 122.02- {
10/07/94 24002 Cancel Ki2-6 10/20/94 100.02
10/09/94 513245 REPAIR 10/25/94 4.50 4500.12
10/28/96 20057 Check 12-7 10/28/94 5.29-  5433.36-
10/10/94 24001 11/09/94 +02
++ END

cmé3-Return cmd6-Page 2 cmd9-Invoice Number Roll-Page

 

This screen displays the transaction history for the selected vendor. To
cancel a check, position the cursor next to it and type any character. The
Check Detail Screen appears. See that section for more information.

The transaction history can be sorted in one of two ways: by due date and

RELEASE 2.1 or


X12-9 CANCEL CHECKS |

by invoice number. Press [Cmd9] to toggle between sorting methods.

The sorting method determines how the "Position to" field is interpreted.
If transaction history is sorted by due date, the "Position to" field will only
accept dates in the form of MMDDYY. This will display invoices and
checks with a due date equal or greater than the date you entered be
displayed. If transaction history is sorted by invoice number, the "Position
to" field will only accept invoice numbers.

Press [Cmd6] to circulate among the 3 Transaction History Pages. Page 2
and Page 3 are illustrated below.

Commands
{Cmd3] Returns to the Vendor Selection Screen detailed above.
[Cmd6] "Turns” to the next page of the Transaction History Screen.
Pages 2 and 3 are shown below.
[Cmd9] Toggles between two sorting methods: by due date and by

invoice number.


 

TRANSACTION HISTORY - PAGE 2

A & R EQUIPMENT SALES CANCEL CHECKS *12901-06
Division A Page 2 Transaction History By Due Date

### Albeo1 Albert'S Machine Shop 2400

Inv Date Invoice # Id Trn Date G/L Mth Amount Tax] Amount Tax2 Amount
09/20/94 12422 10/10/94 10/94 10.00
10/20/94 13002 10/13/94 10/94 -O1-
09/20/94 20001 10/05/94 10/94 122.02
99/20/94 23062 10/05/94 10/94 523.12
10/07/94 24002 10/07/94 10/94 200.02
10/07/94 51244 10/07/94 10/94 400.12
09/20/94 20001 10/07/94 10/94 122.02-
10/07/94 24001 10/10/94 10/96 100.02-
10/09/94 513245 10/10/94 10/94 4500.12
10/28/94 20057 20/10/94 10/94 5433 .36-
10/10/94 24001 1osi1/94 10/94 +01

** END +

Start,

Crd3-Return Omdé-Page 3 Cnd9-Invoice Number Roll-Page

 


TRANSACTION HISTORY - PAGE 3

‘A & R EQUIPMENT SALES CANCEL CHECKS ‘%12901-07
Division A Page 3 ‘Transaction History By Due Date

### Albeol Albert'S Machine Shop A2400

Inv Date Invoice # Date/Mth/Merge © Check No. Batch No. Type Amount,
09/20/94 12422 10/10/84 10/94 620057 4 10.00
10/10/94 13002 10/11/94 10/94 013002 -01-
09/20/94 20003 10/07/94 10/94 12-6 cance 122.02
09/20/94 23042 10/10/94 10/94 020087 523.12
10/07/94 24001 10/10/94 10/94 12-6 Cane 100.02
10/07/94 51244 20/10/94 10/94 020057 400.12
09/20/94 20001 20/07/94 10/94 X12-€ Canc 122.02-
10/07/94 24001 10/10/94 10/94 -x12-6 Cane 100,02-
10/09/94 513245 20/10/94 10/94 020057 4500.12
10/28/94 20057 10/10/94 10/94 020057 5433.36-
10/10/96 24002 10/1iss4 10/94 000666 02.

4” END **

Start

cmd3-Return Cmd6-Page 1 cmd9-Invoice Number Roll-Page

 


re | X12-9 CANCEL CHECKS _
{

CHECK DETAIL SCREEN

A & R EQUIPMENT SALES CANCEL CHECKS x12901-11
Division a Page 1 Check Detail By Due Date
ALBEQ] ALBERT'S MACHINE SHOP 2400
Invoices Paid hy this Check ..: 20057

Inv Date Invoice # Description Due Date Unit # Discount Amount,

10/26/94 20057 Check X12-7 10/28/94 5.29-  §433.36-
09/20/94 12422 REPAIR 9/27/94 01 10.00
09/20/94 23042 MISC. MAIN 10/20/94 38 523.12
10/07/94 51244 RETOOLING 10/20/94 +40 400.12
10/09/94 513245 REPAIR 20/25/94 4.50 4500.12

### ** End **

Cmd3-Return  Crd6-Page 2 Cmd8-G/L Transactions md19-Cancel Chk Roll-Page

 

The check detail screen displays all of the invoices paid with the check
you selected in the Transaction History Screen detailed above. To cancel
the check, press [Cmd19].

Commands
{Cmd3] Return to the Transaction History Screen detailed above.
{Cmd6] "Turns" to the next page of the Check Detail Screen. The 3

RELEASE 2.1 LO


pages available are identical to the 3 pages available from
the Transaction History Screen detailed above.

{Cmd8] Displays the G/L transactions associated with this check.
The 2 screens detailing these transactions are illustrated in
the General Ledger Screen section below.

GENERAL LEDGER SCREEN - PAGE 1

A & R EQUIPMENT SALES CANCEL CHECKS ¥12901-09
Division A
ALBEO] ALBERT'S MACHINE SHOP
G/L Transactions for Check : 20057

Id Date Mth Document D/c Acct # Amount Description addr # Unit #
10/10/94 10 20087 D Az400 5433.36 Check X12-7 ALBEO2
10/10/94 10 20057 ¢ 41030 5428.07 Check 12-7 ALBEOI
10/10/94 10 20057 c sooo 5.25 Check x12-7 ALBEO2

40s END tee

Gmd3-Return Cmd6-More Pages Cmd8-Invoices Cmd19-Cancel Chk Roll-Page

 


GENERAL LEDGER SCREEN - PAGE 2

A & R EQUIPMENT SALES

Division A

CANCEL CHECKS

ALBEO] ALEERT'S MACHINE SHOP 2400
G/L Transactions for Check : 20057

Description Addr # Unit # Name--. --* Due Date

Check 12-7 ALBEOL
Check 12-7 ALBEOL
Check X12-7 ALBEOL
ae END te

ALBERT’S MACHINE SHOP 10/28/94
ALBERT'S MACHINE SHOP
ALBERT’S MACHINE SHOP

x12901-10

Cmd3-Return Cmdé-More Pages Cmd8-Invoices Cmdil9-Cancel Chk Rol l-Page

 

## CHAPTER X12-10

LIST OF VENDORS (SUMMARY)

### Introduction

The List of Vendors produces a report that includes a summarized list of
selected vendors, including each vendor's G/L account, terms, home and.
work phone number, fax number, and work group.

### How To Run

From the Payables Menu (X1-2), select option 10, List of Vendors
(Summary).

C At the security gate, enter your division. To print vendors from all
divisions, press [Enter]. To print vendors from only the division you
selected, [Tab] to the "Print All Divisions" field and enter a "N." Press

[Enter]. The following screen will appear.

### X12A01-02

ABC-AG,AUTO,CONS & TRUCK CO. LIST OF VENDORS-SUMMARY

Division *

: 1-Vender Name
2-Vendor Address Number

: 1-General Ledger Account
2-Group Code
3-Address Number

### X12-10 List Of Vendors (Summary)

 

O To sort the report by address number, type a '"2" in the "Sort by" field.
To sort the report by vendor address, leave this field unchanged. Press
[Tab] to move onto the next field.

O To include vendors who are associated with general ledger account(s)
in the report, leave the "Select by" field unchanged To include vendors
belonging to a group code(s), enter a "2." To include vendors by
address, enter a "3." Press [Enter]. Depending on your choice, one of
three screens will appear.

Select by General Ledger Account Number

ABC-AG,AUTO, CONS & TRUCK CO. LIST OF VENDORS-SUMMARY *12A01-02
Division * Selection by G/L Account

Enter : ALL = All Payable Accounts
T = Only trade Payable Accounts
F = Only Flooring Payable Accounts

or
Specific General Ledger Account Numbers

Cmdi-End, Cnd3-Previous Screen
oe

### X12-10 List Of Vendors (Summary)

 

O To include all payables in the report type "ALL." Type "T" to include
only trade payable accounts in the report; type "F" to include only
flooring payable accounts in the report. Otherwise, to include specific
general ledger account number(s) in the report, [Tab] to the next field
and enter an account number. Continue pressing [Tab] and entering
more account numbers if desired.

O Press [Enter]. The report is generated and printed on the system
printer.

Select by Group Code

ABC-AG, AUTO, CONS & TRUCK CO. LIST OF VENDORS-SUMMARY 1201-03
Division * Selection by Group Codes

   

Enter Group Codes

Cndi-End, cnd3-Previous Screen

### X12-10 List Of Vendors (Summary)

 

 

O To include a group in the report, enter its code in this field. To move
onto the next field, press [Tab]. When you are finished entering group
codes press [Enter]. A report will be generated and printed. If this
screen is left blank, [Enter] will return you to the Payables Menu
without generating a report.

i
RELEASE 2.1 i


X12-10 LIST OF VENDORS (SUMMARY)

 

Select by Vendor Address

ABC-AG,AUTO,CONS & TRUCK CO. LIST OF VENDORS-SUMMARY X12A01-04
Division * Selection by Address Numbers

   

Enter Address Numbers

Qmdi-mnd, Cmd3-Previous Screen

© Enter a vendor address in this field. To add more vendors, use [Tab] to
move to the next field and key in the next vendor address. When you are
finished entering group addresses press [Enter]. A report is generated and
printed on the system printer. If this screen is left blank, [Enter] will take
you back to the Payables Menu without generating a report.

A printout is illustrated below.


X12-10 LIST OF VENDORS (SUMMARY)

 

180-40. A10, C088 & TRUK co. Tae ot venocs (any) ete
Selection by o/Aecoue © A

nase t mae i hse tecceetampescceceect Dhve/Bue Hom tone och Mone Het. Fok miter ten

tevin wet mown nate ae om

Ainon Albera's facnINe sfOP —«A240D. 3B YStpay net 50a soonys fae fe nied 266350 512 6517 206-25 082

witzes nuaenscnz cone tan

feuntt Asnincs noms coma szte ave 5 nee

tame, ARIMA wetOn er 2220

costes AERICAK wevom maser sen

cxests momer sere mu

ives amen waneoeaz gaat

oases suits store wa oe

cnuces engchbe WOLenEnSn's aA

Guise: inmie's macron cone; Aan

coresi cores nemstes mas

cornea owzoen btoers tens

bononh name's HEAT EATIINZ at 30.00 8 Snape et sam soe Ger czas ast0 206 547652

renbta sonoworon come aut ote tars ae ean

fenteh ono yofon cert COMPane he

feaond ono faita 39.00 6 ays et sans

root rove nase

ronoes ses es

ofene? ceznorinm sine mux aor (

fovtes cnexwonen Sse bulk”

creer tach wave

cant test nase

tree te ae ‘otto

aan omc Sears mscang aa nn

Zones som bene tacron Comey att tose

vasatsaaasbvrenae Rte

soca Manb-rahoe Sue

vot xo mooe's aus sees

feat soca cabin cont Neo

Tantei wine's macton connor

sane or noc wane

mun) mianiou, Cone: nico oes

DIREOz THRWGR's nin? & REY BMGH hb .20'¥ aéays net soups soneye 206 15 GHD 206 7297610 &570. 406 617 om

preon pean oan most

Caves Panic temovres crept eran

tisnea unis town szwiee sat

tonreg soolar Docs ee

yootet oven enor mito

fonons canton tors basco sn

Sines Sear ¢ ecm See cies

vores sot7 comer mmmem, tse

fun: cus sais ras

free: bec Zacron mato we

‘thot Stn ase og

 

RELEASE 2.1 CO

## CHAPTER X12-11

LIST OF VENDORS (DETAIL)

### Introduction

The List of Vendors (Detail) produces a customized report that lists
information about each vendor, including

™ ~=home, work and fax numbers and address
™ ~=©G/L and tax accounts, including G/L distribution
™ phone and fax numbers for salespeople and A/R clerks

### How To Run

From the Payables Menu (X1-2), select option 12, List of Vendors
(Detail). The following screen appears.

ABC-AG, AUTO,CONS & TRUCK CO. LIST OF VENDORS-DETAIL x12B01-01
Division * Selection

1-vendor Name ..
2-Vendor Address

Select by : 1-General Ledger Account
2-Group Code
3-Address Number

Print Salesman Information (Y/N)

Print A/R Clerk Information (¥/N)

Print G/L Distribution {¥/N)


[2] X12-11 LIST OF VENDORS (DETAIL) we

O Type a "2" in the "Sort by" field to sort the report by vendor address.
To sort the report by vendor name, leave this field unchanged. Press
[Tab] to move to the next field.

O To include vendors who are associated with general ledger account(s)
in the report, leave the "Select by” field unchanged. To include
vendors belonging to a group code(s), type a "2" in this field. To
include vendors by address, type a "3." Press [Tab] to move to the next
field.

0 To include salesperson information, A/R clerk information, or G/L
account distribution in the report, [Tab] over to the appropriate field(s)
and type a "Y."

D Press [Enter]. Depending on the method of selection you chose, one of
three screens will appear.

RELEASE 2.1 (OU


X12-11 LIST OF VENDORS (DETAIL) Le]

Select by General Ledger Account Number

ABC-AG, AUTO, CONS & TRUCK CO,
Division a

 
  
  

       
 

LIST OF VENDORS-DETATL X12E01-02
Selection by G/L Accounts

 
  
  

Enter .: ALL = All Payable Accounts
T = Only Trade Payable Accounts
= Only Flooring Payable Accounts

    
  
 

or
Specific General Ledger Accounts

 
   

  

Cmdl-End, Cmd3~Previous screen

  

Payable accounts in the report type "ALL." Type "T" to
include only trade payable accounts in the Teport; type "F" to include

entering more account numbers if desired,

O Press [Enter]. The Teport is generated and Printed on the system
printer.


[«] 42-11 LIST OF VENDORS (DETAIL) .

|| LEST OF VENDORS-DETAIL
selection by Group Codes

cmdi-2nd, Cmda3-Previous Screen

 

(1 To include a group in the report, enter its code in this field. To move
onto the next field, press [Tab]. When you are finished entering group
codes press [Enter]. A report is generated and printed on the system
printer. If this screen is left blank, [Enter] will retum you to the
Payables Menu without generating a report.

RELEASE 2.1 C


X12-11 LIST OF VENDORS (DETAIL) Le]

Select by Vendor Address

ABC-AG, AUTO, CONS & TRUCK CO. LIST oF VENDORS-DETATL, x12B01-04
Division * Selection by Address Numbers

        
         
   
 

Enter Address Numbers

“End, Cmd3-Previous Screen

A sample report follows,

### X12-11 List Of Vendors (Detail)

 

ABC-AG, AUTO, CONS & TRUCK CO. bist of Vendors (Detail) 9/29/94 Page
Division: * galesean: ¥ A/R Clerk: ¥ G/L Dist: ¥ Fick by: Vendoy Nane 1280-3
selection by G/L Account + AL
APLUOL A-L PLUMBING tomy 206 325 8907 Gru Account: A200 TERMS + & Days Disc Ine Taxt..+
fax 206 627 6094 Ext axl Acct. Net ‘Days Disc inc Tax2,
Box 32 FAX 206 325 6910 tax2 Acct. number Days Due «Days Payments on Hold : N
m1 pate Entered: 3/01/86 Group Codes +
Ma .VERNON, HA.
salesporson.--.++ +++ LAUREN rel. : 206 325 8909 Fax : 206 325 8930
AJR Clark : HOMPRREY tel. 1 206 325 3908 206 225 8910
MENO: ALWAYS ASK FOR DAN
G/L mise. +
ALBEAT'S NACHINE SHOP 206 734 2282 a/b account: A2s00 0 Terms: 108 20 Disc Inc Taxl..
20g 350 4511 Ext 4573 Taxi Acct..+ Not 15 Dige Inc Tax2.. +
3852 GRIFFITH AVE 206 725 7882 tax2 Acct Number Days Due 30 Payments on Hold : N
pate Hatered: 9/21/94 Group Codes +
‘BELLINGHAM WA

salesperson... ..+++! REBECCA gel. : 206 734 2182 Fax ; 206 734 2188
MR Clerk + RALPH M ger. 1 206 736 2162

yewo; ASK ABOUT MONTHLY SPECIAL
G/b Dist. +
ng609

 

RELEASE 2.1 LO

## CHAPTER X12-12

LIST OF PURCHASES SUBJ TO TAX1

### Introduction

List of Purchases Subj to Tax] lists and totals invoices that were entered
with non-zero amounts in the Tax! field. The Tax1 and Tax2 fields are
ideal for Canadian dealers who wish to record GST and PST.

### How To Run

From the Payables Menu (X1-2), select option 12, List of Purchases Subj
to Tax1. The following screen appears.

A & R EQUIPMENT SALES List of Purchases Subject to Taxl

x12¢01-01
Division A

Selection

: From General Ledger Month .
To General Ledger Month ...

: i-General Ledger Account
2-Group Code
3-Address Number

For Summary only Enter ‘¥'

 

O Enter the range of months you want included in the report. Using the
form MMYY, key in the beginning of the range of months included in
the report. In this form, for example, September 1994 would be keyed
in as "0994" not "994." Press [Tab] to move to the next field.

O Enter the final month that the report will include in the form MMYY.


X12-12 LIST OF VENDORS SUBJ TO TAX1

 

Press [Tab] to move to the next field.

O To include purchases who are associated with general ledger account(s)
in the report, leave the "1" in the "Select by" field unchanged. To
include purchases from vendors belonging to a group code(s), enter a
"2" in this field. To include purchases from specific vendors, enter a
"3." Press [Tab] to move to the next field

O A summarized report lists the total amounts of purchases made from
selected vendors but does not include detail lines on individual
invoices. To generate a summarized report, type a "Y" in the "For
summary only" field and press [Enter]. Otherwise, leave this field
unchanged and press [Enter]. Depending on the method of selection
you chose, one of three screens will appear.

RELEASE 2.1 oe °


X12-12 LIST OF PURCHASES SUBJ TO TAX1

 

 

Select by General Ledger Account Number

A & R EQUIPMENT SALES List of Purchases Subject to Taxi x12C01-02
Division A Selection by G/L Account

       

Enter : ALL = All Payable Accounts ............+:
@ = Only Trade Payable Accounts
F = Only Flooring Payable Accounts

or
Specific General Ledger Account

Endl-End, Cnd3-Previous Screen

O To include all payables accounts in the report type "ALL." Type "T" to
include only trade payable accounts in the report; type "F" to include
only flooring payable accounts in the report. Otherwise, to include
specific general ledger account number(s) in the report, [Tab] to the
next field and enter a G/L account number. Continue pressing [Tab]
and entering more accounts if desired.

O Press [Enter]. The report will be generated and printed.


X12-12 LIST OF VENDORS SUBJ TO TAX1

 

Select by Group Code

   

List of Purchases Subject to Taxi 1201-03
Selection by Group Code

cndi-End, cmd3-Previous Screen

O To include purchases made from vendors belonging to a specific
group(s), enter a group code in this field. Press [Tab] to move to the
next field. When you are finished entering group codes press [Enter].
A report will be generated and printed. If this screen is left blank,
[Enter] will return you to the Payables Menu without generating a

report.

(
RELEASE 2.1 Ne


X12-12 LIST OF PURCHASES SUBJ TO TAX1

 

Select by Vendor Address

A & R EQUIPMENT SALES List of Purchases Subject to Tax1 x12¢01-04
Division a Selection by Address Number

   

Enter Address Numbers..........: ~----

Cmd1-End, Cmd3-Previous Screen

© To include purchases made from a specific vendor, type in its address
in this field. To add more vendor(s), [Tab] to the next field and key in
its address. When you are finished, press [Enter]. A report will be
generated and printed. If this screen is left blank, [Enter] will return
you to the Payables Menu without generating a report.

A sample report follows.

### X12-12 List Of Vendors Subj To Tax1

   

A @ R EQUIPMENT SALES List of Purchases Subject to Taxi 20/05/94 Page.

Division: a Period fron 7/94 to 10/94 x12¢0-3A
Summary: 5
Selection by G/L Account : ALL

frm Date G/t Mth invoice # Inv Date Description Addr # Unit Amount, Net Amount,
10/05/94 10/94 20002, 9/20/94 WELDER REPAY ALBEOL 322.02 106.14
10/05/94 10/94 23042 9/20/94 MISC. MAIN ALBEQL 523.22 379,99
10/05/94 10794 10022 20/05/94 MISC. WORK —_DOROO1 500.32 346.29
20/05/94 10/94 10689, 20/05/94 MISC. WORK DORCOL 1,000.66 798.48
10/05/94 20/94 so002 9/20/94 MISC. WORK LEESOL 240.02 189.78
10/05/94 10/94 56123 10/05/94 HEATER INST LEESOL 656.12 565.08
Rumber of Transactions 6 Totals 20/56 + 3,042.25 2,376.56
Wunber of Transactions: 6 Grane Totals + 3,082.26 2,376.56

  

RELEASE 2.1 \

## CHAPTER X12-13

LIST OF PURCHASES SUBJ TO TAX2

### Introduction

List of Purchases Subj to Tax2 lists and totals invoices that were entered
with non-zero amounts in the Tax2 field. The Taxi and Tax2 fields are
ideal for Canadian dealers who wish to record GST and PST.

### How To Run

From the Payables Menu (X1-2), select option 12, List of Purchases Subj
to Taxl. The following screen appears.

A&R EQUIPMENT SRLES List of Purchases Subject to Tax? yazpo1~02
Division » selection

+ From General Ledger Month
To General Ledger Month

A-Generai Ledger Account .-..---.---2
2-Group cede

3-Adéress Number

 

Q Enter the range of months you want included in the report. Using the
form MMYY, key in the beginning of the range of months included in
the report. In this form, for example, September 1994 would be keyed
in as "0994" not "994." Press [Tab] to move to the next field.

O Enter the final month that the report will include in the form MMYY.
Press [Tab] to move to the next field.

O To include purchases who are associated with general ledger account(s)
in the report, leave the "1" in the "Select by" field unchanged. To
include purchases from vendors belonging to a group code(s), enter a


[2] X12-13 LIST OF PURCHASES SUBJ TO TAX2 _

"2" in this field. To include purchases from specific vendors, enter a
"3." Press [Tab] to move to the next field

O Asummarized report lists the total amounts of purchases made from
selected vendors but does not include detail lines on individual
invoices. To generate a summarized report, type a "Y" in the "For
summary only" field and press [Enter]. Otherwise, leave this field
unchanged and press [Enter]. Depending on the method of selection
you chose, one of‘three screens will appear.

RELEASE 2.1 om


X12-13 LIST OF PURCHASES SUBJ TO TAX2 [=]

Select by General Ledger Account Number

A & R EQUIPMENT SALES List of Purchases Subject to Tax2 x12D01-02
Division A Selection by G/L Account

       

Enter .: ALL = All Payable Accounts .............:
? = Only Trade Payable Accounts
F = Only Flooring Payable Accounts

or
Specific General Ledger Account

cmdi-End, Cma3-Previous Screen

O To include all payables accounts in the report type "ALL." Type "T" to
include only trade payable accounts in the report; type "F" to include
only flooring payable accounts in the report. Otherwise, to include
specific general ledger account number(s) in the report, [Tab] to the
next field and enter a G/L account number. Continue pressing [Tab]
and entering more accounts if desired.

O Press [Enter]. The report will be generated and printed.


[+] X12-13 LIST OF PURCHASES SUBJ TO TAX2

Select by Group Code

A & R EQUIPMENT SALES List of Purchases Subject to Tax2 412D01-03
Division A Selection by Group Code

   

Enter Group Codes ............:

Qmai-End, Cmd3-Previous Screen

To include purchases made from vendors belonging to a specific
group(s), enter a group code in this field. Press [Tab] to move to the
next field. When you are finished entering group codes press [Enter].
A report will be generated and printed. If this screen is left blank,
[Enter] will return you to the Payables Menu without generating a
report.

c


X12-13 LIST OF PURCHASES SUBJ TO TAX2 [=]

Select by Vendor Address

A & R EQUIPMENT SALES List of Purchases Subject to Tax2 12D01-04
Division A Selection by Address Number

   

Enter Address Numbers .......-:

 

 

(mdl-End, Cnd3-Previous Screen

O To include purchases made from a specific vendor, type in its address
in this field. To add more vendor(s), [Tab] to the next field and key in
its address. When you are finished, press [Enter]. A report will be
generated and printed. If this screen is left blank, [Enter] will return
you to the Payables Menu without generating a report.

A sample report follows.

### X12-13 List Of Purchases Subj To Tax2

 

A & R EQUIPMEN? SALES List of Purchases subject to Taxz 10/05/94 Page
Division: a Period from 94/07 co 94/10 1200-38,
Summary:

Selection by G/L Account ; ALL
‘em Date G/L Mth Invoice # Inv Date Description Addr # Unite Amount, Net Amount
10/05/94 10/9 20001 9/20/98 WELDER REPAL ALEGOL 122.02 106.24
10/0s/94 10/94 23042 9/20/94 MrSC. MAIN ALBEOL 523.12 379.98

20/05/94 10/94 10022 10/05/94 MISC. WORK DOROOL 500.32 346.25
10/05/94 10/9¢ 29689 10/05/94 MISC. WORK —_DOROOL 1,000.66 708.48
10/05/94 30/94 50002 9/20/94 MISC. WORK —LEPSOL 240.02 199.78
10/05/94 10/94 56123 20/05/94 HEATER INST LEESOL 656.12 565
Number of Transactions: 6 Totals 20/94 + 3,042.26 2,376.56
Number of Transactions 6 Grand Totals + 3,042.26 2,376.56

  

 

## CHAPTER X12-14

AGED PAYABLES SUMMARY REPORT

### Introduction

The Aged Payables Summary Report contains two sections. The first
projects amounts due, by vendor, over user-specified intervals of days.
The second projects amounts due, by G/L account, over user-specified
intervals of days.

Note: This report will include vendors with unmerged transactions even
when the totals are negative or zero.

### How To Run

From the Payables Menu (X1-2), select option 14, Aged Payables
Summary Report. The following screen will appear.

ABC-AG,AUTO,CONS & TRUCK CO. AGED PAYABLES-SUMMARY *12801-01
Division A Selection

Enter General Ledger Period
{Leave period blank for current period)

Enter column interval for ageing
(Ex.: 30 = 1-30, 31-60, 61-90, 91-120, 120+)

3 1-Complete Report (198 Columns)
2-Abbreviated Report (132 Columns)

A-Vendor Name ..
2-Vendor Address

Select by : 1-General Ledger Account
2-Group Code
3-adéxess Number

### [2] X12-14 Aged Payables Summary Report

C Enter the month and year you want the aged payables report to project
from. Make this entry in the form of MMYY, using the first two digits
for the month and the second two for the year. Example: September
1994 would be "0994." To project from the current month leave this
field blank. The month you select must be the purge month or later
(see X6-6, Security and Maintenance). Press [Tab] to move to the next
field.

O Enter the interval you want the report to use for its projection in the
"Enter Column Interval for Aging" field. A choice of 30 days would
generate a report that would list all the payables due in the next 1-30
days, 31-60 days, etc. This interval must be between 1 and 99 days.
Press [Tab] to move to the next field.

O Type a "2" in the "Enter" field to generate an abbreviated report. To (
print a complete report, leave this field unchanged. A complete report
includes the G/L account associated with each vendor and projects two
more intervals forward than the abbreviated report does. In every other
respect, the two reports are identical. Press [Tab] to move to the next
field.

C Type a"2" in the "Sort by" field to sort the report by vendor address.
To sort the report by vendor name, leave this field unchanged. Press
[Tab] to move to the next field.

O To include vendors who are associated with general ledger account(s)
in the report, leave the "Select by" field unchanged. To include
vendors belonging to a group code(s), enter a "2" in this field. To
include vendors by address, enter a "3."

© Press [Enter]. Depending on the method of selection you chose, one of
three screens will appear.

RELEASE 2.1 LU


X12-14 AGED PAYABLES SUMMARY REPORT [:]

Select by General Ledger Account Number

ABC-AG,AIITO, CONS & TRUCK CO. AGED PAYABLES-SUMMARY x12801-02
Division A Selection by G/L Accounts

ater .: ALL = All Payable Accounts
T = Only Trade Payable Accounts
F = Only Flooring Payable Accounts

or
Specific General Ledger Accounts

Cmdl-End, Cnd3-Previous Screen

 

O To include ali payable accounts in the report type "ALL." Type "T" to
include only trade payable accounts in the report; type "F" to include
only flooring payable accounts in the report. Otherwise, to include
specific general ledger account number(s) in the report, [Tab] to the
next field and enter an account number. Continue pressing [Tab] and
entering more account numbers if desired.

O Press [Enter]. The report will be generated and printed.


[+] X12-14 AGED PAYABLES SUMMARY REPORT a

Select by Group Code

ABC-AG, AUTO, CONS & TRUCK CO. AGED PAYABLES-SUMMARY *12E01-03
Division * Selection by Group Codes

       

Enter Selection Codes ........: -----

Cmdl-End, Cmd3-Previous Screen

O To include a group in the report, enter its code in this field. To move
onto the next field, press [Tab]. When you are finished entering group
codes press [Enter]. A report will be generated and printed. If this
screen is left blank, [Enter] will return you to the Payables Menu
without generating a report.

RELEASE 2.1 NW


X12-14 AGED PAYABLES SUMMARY REPORT [=]

Select by Vendor Address

ABC-AG, AUTO, CONS & TRUCK CO. AGED PAYABLES-SUMMARY X12E01-04
Division * Selection by Address Numbers

   

Enter Address Numbers ........: -----

cmdi-End, Cmd3-Previous Screen

O To include a vendor in the report, enter its address in this field. To
move onto the next field, press [Tab]. When you are finished entering
addresses press [Enter]. A report will be generated and printed. If this
screen is left blank, [Enter] will return you to the Payables Menu
without generating a report.

A sample report follows.

## X12-14 AGED PAYABLES SUMMARY REPORT

ged Payables Summary Report (abbreviated

AEC-NG,AVTO, CONS & TRUCK CO. ‘Aged Payables Summary 9/29/94 zage
Division: A Sorted by Vendor Name xI2E0-5A
Pericd: Current Interval: 20
Selection by G/L Account : ALL
4 adr, Nom, -* Past Due after 1-30 bays 32-60 Days 61-90 Days eral
DOROO] DOROTHY’S HEAVY BAULING 349.76 29 349.76
FORDOZ FORD MOTOR COMPANY 4,514.00 4,814.00
EBSCO] LEE'S PLUMBING & HEATING 94.12
NEWHC1 NEW HOLLAND 1,850.00 1,880,00
‘CASHA TRANK YOU FOR YOUR BUSINESS 50.06 80.00
WESTCS WEST COAST GRAPRICS 219.58 219.58
‘Totals + 28 203.70 6,414.09 7,067.46
ABC-AG,AUTO,CONS & TRUCK CO. aged payables Sumary 9/23/94 Page
Division: A Sorted by Vendor Name xa2B0-5A,
Poriod: Current interval: 30

 

Selection by G/L Account : ALL
Ledger Account Summary

1-30 Days «31-60 Days 62-90 Days + Total
NOTES PAYABLE-FORD 4,514.00 4,514.00
‘(NOTES PAYABLE-NEW HOLLAND 2,850.00 2,850.00 (
PAYABLES 653.46
CUSTOMER DEPCSTTS 50-00 50.00

TOTALS + 6,414.00 7,087.46

 

 

RELEASE 2.1 L

## CHAPTER X12-15

AGED PAYABLES DETAIL REPORT

### Introduction

The Aged Payables Detail Report contains two sections. The first projects
the amounts due, by vendor, over user-specified intervals of days and a
listing of all unpaid invoices. The second projects the amount due, by G/L
account, over user-specified intervals of days and a listing of all unpaid
invoices..

### How To Run

From the Payables Menu (X1-2), select option 15, Aged Payables Detail
Report. The following screen will appear.

ABC-AG,AUTO,CONS & TRUCK CO. AGED PAYABLES-DETAIL X12F01-01
Division A Selection

Enter General Ledger Period
(Leave period blank for current period)

Enter column interval for ageing

(Ex.: 30 = 1-30, 31-60, 61-90, 91-120, 120+)

: 1-Complete Report (198 Colums)

2-abbreviated Report (132 columns)

2-Vendor Address Number

: 1-Transactions by Due Date
2-Transactions by Invoice Number

+ L-General Ledger Account .
2-Group Code
3-Address Number

## X12-15 AGED PAYABLES DETAIL REPORT

 

O Enter the month and year you want the aged payables report to project
from, Make this entry in the form of MMYY, using the first two digits
for the month and the second two for the year. Example: September
1994 would be "0994." To project from the current month leave this
field blank. The month you select must be the purge month or later
(see X6-6, Security and Maintenance). Press [Tab] to move to the next
field.

O Enter the interval you want the report to use for its projection in the
"Enter Column Interval for Aging" field. A choice of 30 days would
generate a report that would list all the payables due in the next 1-30
days, 31-60 days, etc. This interval must be between 1 and 99 days.
Press [Tab] to move to the next field.

O Type a "2" in the "Enter" field to generate an abbreviated report. To
print a complete report, leave this field unchanged. A complete report (
includes the G/L account associated with each vendor and projects two :
more intervals forward than the abbreviated report does. In every other
respect, the two reports are identical. Press [Tab] to move to the next
field.

DO Type a"2" in the "Sort by” field to sort the report by vendor address.
To sort the report by vendor name, leave this field unchanged. Press
[Tab] to move to the next field.

O Type a"2” in the "Print" field to print transactions in order or invoice
number. To print transaction in order of due date, leave this field
unchanged. Press [Tab] to move to the next field.

O To include vendors who are associated with general ledger account(s)
in the report, leave the "Select by" field unchanged. To include
vendors belonging to a group code(s), type a "2" in this field. To
include vendors by address, type a "3."

O Press [Enter]. Depending on the method of selection you chose, one of
three screens will appear.

RELEASE 2.1 oe


 

Select by General Ledger Account Number

ABC-AG,AUTO,CONS & TRUCK CO. AGED PAYABLES-SUMMARY x12F01-02
Division A Selection by G/L Accounts

   

Enter .: ALL = All Payable Accounts ............-:
T = Only Trade Payable Accounts
F = Only Flooring Payable Accounts

or
Specific General Ledger Accounts

Cmdl-End, cmd3-Previous screen

© To include all payable accounts in the report type "ALL." Type "T" to
include only trade payable accounts in the report; type "F" to include
only flooring payable accounts in the report. Otherwise, to include
specific general ledger account number(s) in the report, [Tab] to the
next field and enter an account number. Continue pressing [Tab] and
entering more account numbers if desired.

O Press [Enter]. The report is generated and printed on the system
printer.


 

Select by Group Code

AEC-AG,AUTO,CONS & TRUCK CO. AGED PAYABLES-DETAIL x12F01-03
Division * Selection by Group Codes

   

Enter Selection Codes ........:

Cmdl-End, Cnd3-Previcus Screen

O To include a group in the report, enter its code in this field. To move
onto the next field, press [Tab]. When you are finished entering group
codes press [Enter]. A report will be generated and printed. If this
screen is left blank, [Enter] will return you to the Payables Menu
without generating a report.
WO


 

Select by Vendor Address

ABC-AG,AUTO,CONS & TRUCK CO. AGED PAYABLES-DETAIL X12F01-06
Division * Selection by Address Numbers

   

Enter Address Numbers

(mdi-mnd, Cnd3-Previous Screen

CO To include a vendor in the report, enter its address in this field. To
move onto the next field, press [Tab]. When you are finished entering
group addresses press [Enter]. A report will be generated and printed.
If this screen is left blank, [Enter} will return you to the Payables Menu
without generating a report.

A sample report follows.


Aged Payables Detail Report (abbreviated)

ABC-AG,ADT0,CONS & TRICK CO,
Division: A

Aged Payables Summary
Sorted by Vendor Name

& Transnetions by Due Date

Period: Current Interval: 30

Selection by G/L Account : ALL

DOROOL DOROTHY*S HEAVY HAULING im 206 734 0525,

4m 206 647 4229 Exc 4570

2426 MUSTANG WAY FAX 206 647 6921
P.O, BOX 5381 ma
BELLINGHAN WA 98225
Invoice # Inv Date M G/L ait 4 Tue Date
984-0761 7/06/94 9/94 UTODTS 8/31/94
Number of Invoices: 1 Totals +
FORDO2 FORD MOTOR COMPANY ex
we
2500 MAPLE AD FAK
ra
‘TROY, MI ae048
Invoice # Inv Dare ¥ G/L Unit # Due Date
17953 1/01/86 2/95 725798 99/99/99
621269 © 1/01/86 2/95 FTO7E1 99/99/99
642972 1/01/86 2/95 FroBes 99/99/99
ROA 2/01/86 3/95 PESBEG 99/93/99
Number of Invoices; 4 Totals +
LEESO1 LEE’S PLOWAING & HEATING tim 206 734 6440

MS ROOTER Awe 800 339 7318 Exe

3073 AIRPORT WAY FAX 206 738 1010
om
BELLINGHAM HA 98225
Invoice # Inv pate MG/L Unit | Due Date Past fue
SR-100478 9/09/96 9/94 10/05/94

Number of Invoices Totals +

Runber of invoices 9 Grend Totals : 249.76
‘ABC-AG,AUTO, CONS & TRUCK OC.
Division: a

Selection by G/L Account + ALL

Sorted by Vendor Nare
Peri:

G/L Accoune: 2400 Terms + 10.00 8
taxi acct... Nee.
Taxd nec... Nusber Days Due
Date Entard: 9/23/95 Group Code :
a 30 pays

31-60 Days 61-90 Days 81+

G/L Account: A2200 Terms 10% 20
Tax acct wet 30
Tax2 Acct. Number Days Due ¢5
Pate Bnterd: 1/01/86 Group Code
1-30 Days 31-60 Days GI- 90 Days B+
1,837.00
22, 462.00
23,225.00
42, 000.00-

4,514.00
G/L Account: 42400 Tems : 50% 10
‘Taxl Acct. Met 25
axd Acet..2 Namber Days Due 26
Pate Enterd: §/23/94 Group code :

A+ 30 nays 31-60 Days 61+ 90 Days «92+

6,414.00
‘aged Payables Summary
& Transactions by Due Date
Current Interval: 30

Generel Ledger Account Sumary

NOTES PAYABLE-FORD
NOTES PAYABLE-NEW HOLLAND
‘PRYABLES
‘CUSTOMER DEPOSITS

TOTALS :

1-30 Days 31-60 Days = G1- 90 Days «9+
4,524.00

1,850.00

50.00
6,414.00

 

9/29/94 Page

x12P0-54

349.76
Days
Days
Days

#21000.08- (
bays
ave
bere

84.12

7,067.46

9/29/98 Page 2

XA2P0-58

total
4,514.00
2,850.00
653.46
50.00
7,067.46

RELEASE 2.1 Lo

## CHAPTER X12-16

PAYABLES DUE REPORT

### Introduction

The Payables Due Report lists all invoices that are due on or before a
specified date. Invoices included in the report can be selected by general
ledger account, group code, or vendor address. Within each vendor,
invoices can be sorted by invoice number or due date. A total of all
payables due by the specified date concludes the report.

### How To Run

From the Payables Menu (X1-2), select option 16, Payables Due Report.
The following screen will appear.

= & L EQUIP. SALES & RENTALS PAYABLES DUE REPORT. x12G01-01
Division A Transaction Selection

Invoices Due On or Before : 10897  (MMDDYY)
(For all invoices use 123250)

Sort Invoices by : 1-Due Date
2-Invoice Number

Selection by ....; I+General Ledger Account. :
2-Group Code
3-Address Number

Include Vendors with Held Payments (¥,N) ...:

cmdl-End


[2] X12-16 PAYABLES DUE REPORT we
(

C The report will print invoices due on or before a date you select. Enter
that date in the form of MMDDYY in the "Invoices Due On or Before"
field. Example: February 1*, 1994 would be keyed in as "020194" not
as "2194."

Q The report lists invoices within each vendor. To sort these invoices by
due date, leave the "1" in the “Sort Invoices by” field unchanged. To
sort invoices by invoice number type a "2" in this field. Press [Tab] to
move to the next field.

O To generate this report using payables from vendors associated with a
general ledger account(s), leave the "1" in this field unchanged. To
include payables from vendors belonging to a group code(s), enter a
"2." To include payables from specific vendors, enter a"3." Press
[Enter]. Depending on your choice, one of three screens will appear.

O To include vendors whose master records (X12-2) are marked "Hold {
Payments=Y," change the default on "Include Vendors with Held
Payments" to “Y"; otherwise, these vendors will not be included on the
report. The selection screen defaults to “N" the first time, afterwards it
will remember your selection and use it as the default until it is
changed.

RELEASE 2.1 Co


X12-16 PAYABLES DUE REPORT [2]

Select by General Ledger Account Number

A & R EQUIPMENT SALES PAYABLES DUE TODAY x12602-02
Division A Selection by G/L Account

Enter : ALL = All Payable Accounts
? = Only Trade Payable Accounts
F = Only Flooring Payable Accounts

or
Specific General Ledger Accounts

(mdi-End, Cmd3-Previous Screen

 

O To include payables associated with all G/L accounts in the report type
“ALL.” Type “T" to include only payables associated with trade
payable accounts; type "F" to include only payables associated with
flooring payable accounts. Otherwise, to include payables associated
with specific general ledger account number(s), [Tab] to the next field
and enter an account number. Continue pressing [Tab] and entering
more account numbers if desired.

O Press [Enter]. The report is generated and printed on the system
printer.


[+] X12-16 PAYABLES DUE REPORT

Select by Group Code

A & R EQUIPMENT SALZS PRYABLES DUE TODAY x12601-03
Division A Selection by Group Code

   

Enter Group Codes ...

{

Cmdl-End, Cmd3-Previous screen

O To include payables from a specific group in the report, enter its code
in this field. To move onto the next field, press [Tab]. When you are
finished entering group codes press [Enter]. A report will be generated
and printed. If this screen is left blank, [Enter] will return you to the
Payables Menu without generating a report. .


X12-16 PAYABLES DUE REPORT [=]

Select by Vendor Address

ABC-AG, AUTO, CONS & TRUCK CO. PAYABLES DUB TODAY x12601-04
Division * Selection by Address Numbers

   

Enter Address Numbers

Cmdl-End, Cmd3-Previous Screen

O To include payables from a specific vendor in the report, enter its
address in this field. To move onto the next field, press [Tab]. When
you are finished entering group addresses press [Enter]. A report will
be generated and printed. If this screen is left blank, [Enter] will return
you to the Payables Menu without generating a report.

A sample report follows.

## X12-16 PAYABLES DUE REPORT

 

2 & R EQUIPMENT SALES Aged Payables for Specific pate 10/06/94 Page
Division: a Due on ox Zefore ...: 12/35/94 1260-38
Soct Order by Envcices & Bue Date
Seleccion by G/L Account: 7
ALBEO1 ALBERT’S MACHINE SHOP nim 206 734 2122 Gf. Account ; A200 Terms: 10 4 10 Days Balance:
WK 206 389 4512 Ex:4573 Setection cede: Net 15 Days
3882 orFerrt AVE PAX 206 715 7882 Dace Entered ; 9/21/94 number Days Ove 39 Days.
BEGLINGHAG WA 9e225
Invoice 4 Inv Date Description one Date unit Amount, Discount, Net Amoune,
9/20/94 WEODER REPAT 10/20/94 122.02 an a2i.sa
920/98 MISC. MAIN 26/29/95 $23.12 38 922.74
‘Totals 605.16 49 684.65
DORCTHY*S HEAVY HAULING emt 206 734 9525 fu account : A200 Terms :19.09 8 10 Days Balance: 2290.20
fu 266 647 4225 Pxr457% selection Code: Net 15 Days
2426 NOSTANS way FAK 266 647 5927 Bate Entered : 9/23/94 Nunbor Days Due 26 Days
P.O, 20x 5881
BELLINGHAM Wa e225
Invoice # Inv Date Deseriptiea Due Dace Unit F Amount, Discoune,
984-00761 7/06/94 JG-BREAKDOWN §— 8/31/94 -UTOOTS 343.78 34.58
39-4509, 9/0/94 MEN'S TRUCK = 9/27/99 © TRI000 56.78 3.87
a9-s403 5/93/94 KEN'S TRUCK 929/94 TRIO0D 288.43 28.04
48-19740, 5/3294 XEN'S TRUCK 10/98/94 -TRIODD 486.23 46.62
30689 id/0$/96 MISC. WORK = 15/29/44 4.990.66 78.88 (
328-93 Aoso4/94 DITCH 46030/%4  TRIBCO 289.45 25.98

Totals + 2,421.20 220.99 2,200.35
LEESO1 LEE‘S PLUMBING & HEATING HM 206 734 6440 G/L Recount : a2409 Terms: ,50 % 10 Days Balance:
MS ROOTER wan 800 339 7318, Selecticn Code: Net 15 Bays
3673 AIRPORT MAY FAX 206 738 1010, Date Entered : 9/23/94 Number Days ove 26 oays
BELLINGHAM UA 99228
invoice $ inv Date Description ue Dare unit # Amount Discount, Nez Amoune
SA-199675 9/38/94 DRAIN CLEAR 10/95/95, ga.22 42 83.70
soccz Srcr3e MISC. WORE 10/16/91 246.02 “95 239.07
56223 16/05/94 HEATER INST 19/29/34 656.22 653.29

 

rorals +

 

 

RELEASE 2.1 U

## CHAPTER X12-17

VENDOR TOTALS

### Introduction

For American dealers, this job will appear on the payables menu as
"Vendor Totals for 1099 Preparation." Vendor Totals lists selected
vendor's tax numbers and year to date sales. Vendors can be selected by
G/L account, group code, or address.

### How To Run

From the Payables Menu (X1-2), select option 17, 1099 Report. Enter
your division at the security gate and specify if you want the report to
include all divisions. The following screen appears.

### Selection Screen

A & R EQUIPMENT SALES PAYABLES 1099 REPORT x12H01-01
Division A Selection

: 1-Vendor Name
2-Vendor Address Nunber

: 1-General Ledger Account
2-Group Code
3-Address Number

 

O Choose how you want to sort the 1099 report by placing a'"1" or "2" in

## X12-17 VENDOR TOTALS

 

the "Sort by" field,

O Choose what vendors will be included in the report by placing a "1,"
"2," or "3" in the “Select by” field. Depending on your choice one of

three screen will appear.

SELECT BY G/L ACCOUNT

‘A & R EQUIPMENT SALES LIST OF VENDORS-SUMMARY
Division A Selection by G/L Account

Enter : ALL = All Payable Accounts
T = Only Trade Payable Accounts
F = Only Flooring payable Accounts

or
Specific General Ledger Account Numbers ...

Qndi-End, Cmd3-Previous Screen

### X12Ho1-02

 

O Decide if you want the report to include trade payable accounts,
flooring payable accounts, or all accounts. Type “All,” “T,” or “F” in

the field at the top of the screen.
Cc

CC


 

Or, if you want the report to include specific G/L accounts, enter those
account numbers in the ten fields at the bottom of the screen.

O Press [Enter] when done. The report is generated and sent to the
system printer.

### Select By Group Code

A & R EQUIPMENT SALES LIST OF VENDORS-SUMMARY x12H01-03
Division A Selection by Group Codes

Enter Group Codes

Qmdl-End, Cmd3-Previous Screen

 

O Enter the group codes for all the group(s) you want to include the
report.
O Press [Enter] and the report is generated and sent to the system printer.


 

### Select By Address Numbers

A & R EQUIPMENT SALES LIST OF VENDORS-SUMMARY x12H01-04
Division A Selection by Address Numbers

Enter Address Numbers ..

cmdl-znd, cmd3-Previous Screen

 

O Enter the address numbers of all the vendors you want included in the
report.
O Press {Enter] when finished. A report will be generated and sent to the

system printer.

RELEASE 2.1 CO


A sample report is shown below.

A&R BQUIPMENT SALES
Division: a

adds #

‘xLBEOL
cuako1
poRood

Selection by Address Numbers

Name:
ALBERT'S MACHINE SHOP
CARL D CORY

DOROTHY'S HEAVY HAULING
Numbex of Vendors :


1059 Report,
Sozted by Vendor Name
‘ALBEOL CURROI POROOI
tax number
ALBERMAI33D
CURR783-B348
DOROHHI2559

 


20/23/94

Page
xA280-38


Notes:

RELEASE 2.1 LO

## CHAPTER X12-18

PURCHASE ORDER MENU

### Introduction

‘The options on the Purchase Order Menu provide a system for creating
and tracking purchase orders that is similar to Point of Sale Tnyoicing and
Rental/Leasing Invoicing. Purchase Order Entry generates the payables
transactions and can optionally place part lines on a customer's work
order at a markup. Parts for resale and for internal use can be combined
on the same purchase order.

Purchase Orders have a unique document type, "P." Purchase codes are
used in Purchase Order Entry in the same way sales codes are used in
Point of Sale Invoicing. Purchase codes direct the payables accounting
transactions while corresponding sales codes direct the P.O.S. accounting
transactions. Since purchase orders can be held in the system, they are
usually not closed until you have the vendor's invoice number. The ~
vendor invoice number that is entered on the purchase order is used as the
document number, making it easy to track later on. The Due Date is also
established in Purchase Order Entry.

Individual lines on a purchase order can be closed and posted or a
purchase order can be closed in its entirety. Unless a purchase order has
been posted, it can always be reopened, and then modified, voided, or
transferred to another vendor. Orders are posted through the Post P.O.S.
Document Menu (X5-5). Regardless of their status, all purchase orders
maintained on one list. Closed and posted purchase orders can be moved
to a history file with Point of Sale End of Month (X5-4).

 
    
  

WARNING: When installing the Purchase Order System for the
first time, be sure that all closed purchase orders are posted. It is
OK to have open purchase orders during installation.

## X12-18 PURCHASE ORDER MENU

 

SUMMARY OF V9L0/ 1.4 ENHANCEMENTS

Individual lines within purchase orders can now be closed and posted.
You can also mark selected lines as closed without creating any
corresponding general ledger postings in case they have already been
posted manually.

Purchase Orders can be associated with a customer without being linked
to a point of sale invoice. In this case, the customer's name and address
are used as a reference only.

Individual lines within purchase orders can be split to multiple customers
or to different accounts.

Anew *PROMPT debit code enables you to distribute the debit amount
to multiple accounts. You can also specify a customer address, unit
number, and due date for each debit entry.

When you process an existing purchase order for a vendor, the list of
purchase orders displayed is now sorted in order of newest to oldest.
‘Additional fields make it easier to pinpoint the right purchase order and to
know its status (closed, posted, voided, etc.).

Anew parts line purchase code now exists. A search is performed on the
parts records every time the user adds or changes a parts line. When parts
lines are closed and posted, parts inventory will be modified accordingly.

An option now exists that allows you to print purchase orders on 7" or

11” invoices. As purchase orders do not print headings, you must use
preprinted forms for headings to appear on the invoices.

RELEASE 2.1 CU

### Overview

From the Payables Menu, select option 18, Purchase Order Menu. The
Purchase Order Menu is illustrated below:

‘COMMAND
(ce) DIS Corp.

. Purchase Order Entry
. Open Purchase Orders Report
. Purchases Today Report.

. Purchases MID Report.

. Purchase Order Profile

: Purchase Code Maintenance

. Return To Payables Menu

Ready for option number or command

 

A brief description of each option on the Purchase Order Menu follows:


 

X12.18-1 Purchase Order Entry
Purchase Order Entry is used to create, update, close, reopen,
and void purchase orders. It works like Point of Sale
Invoicing (X5-1) and Rental/Leasing Invoicing (X9-1), and
allows full access to old and new purchase orders.

X12.18-2 Open Purchase Orders Report
This report lists all open purchase orders in the system
regardless of date. The report can be printed in order by
vendor address or by purchase order number.

X12.18-3 Purchases Today Report
This report lists purchase orders that were created within a
range of selected dates. The report can include all purchase
orders, or it can be restricted to open (or closed) purchase {
orders only. On the Purchases Today Report you'll find: the
PO#, vendor address, vendor name, gross and.discounted
amounts, employee address, billing customer, and billing
document number and amount. It can be printed in order by
vendor address or by purchase order number.

X12.18-4 Purchases MTD Report
This report lists all open and closed purchase orders that were
created in the selected month and year. It includes the same
information as the Purchases Today Report.

RELEASE 2.1 CO


 

X12.18-5 Purchase Order Profile
Use Purchase Order Profile to set up and maintain a
divisional profile where default information for the Purchase
Orders system is stored. This profile is similar to the
Divisional Profile in Rental/Leasing (X9-5).

X12.18-6 Purchase Code Maintenance’
Purchase codes direct the payables accounting transactions.
Use Purchase Code Maintenance to specify the General
Ledger accounts that will be debited (usually inventory or
expense) and credited (usually accounts payable) for each
code. Each code is set up with a corresponding sales code
that is used as the default for customer work orders or counter
tickets. There are also default tax and discount codes both of
which pertain to the purchase order. The default tax and
discount codes assigned to the customer in Receivables
Maintenance are used on lines transferred to a P.O.S.
document.

### Purchase Orders & Point Of Sale Options

Although there is a unique Purchase Order Entry job, the purchase orders
system is integrated with Point of Sale. The Point of Sale options that are
used for purchase orders are described on the following pages.


 

X5-1 Point of Sale Invoicing

When a customer and their P.O.S. document number are
specified in Purchase Order Entry, the part lines marked for
resale can be automatically transferred to the appropriate
work order or counter ticket. You have full control from
Purchase Order Entry on the selling price. You can use a
percentage markup or enter a price and the system will
calculate the percentage for you. Sales transactions appear in
the Point of Sale Posting Batch as usual when the P.O.S.
document is closed.

X52-2 Document Classification Maintenance

A purchase order is defined as a document type "P."
Document type is set up in Document Classification
Maintenance (X52-2).

From the Point of Sale Menu, select option 2, Table
Maintenance Menu. From the Table Maintenance Menu,
select option 2, Document Classification Maintenance. The.
Document Classification prompt appears. Enter the character
you want to use for Purchase Orders, such as "P" or "O." This
is not the same as the document type and can be any letter that
is not being used for Point of Sale or Rental Invoices.

When you press [Enter], the Document Classification screen
is displayed.

RELEASE 2.1 Lo


ABC-AG,AUTO,CONS & TRUCK CO. DOCUMENT CLASSIFICATION x5220-101
Maintenance
Enter classification code 0

Description PURCHASE ORDER
Valid document types:
> Document type P For Point of Sale: For Rental/Leasing:

"g' ~ quote "U' = quote
'g' - sales order ‘R' ~ reservation
‘W' = work order ‘C* = contract
*p - purchase order

Posting option A Valid options:
‘A ~ automatic posting
‘Mw’ = manual posting
+ + ~ quote

Pricing detail ¥ valid options:
‘Y¥' - pricing om each line
‘N' - pricing on final total’ only

Sequence + Po 00001
NEW Classification code:
Enter ¥ to CANCEL

 

Make sure to select Document Type = "P" as illustrated.
Documents whose type is "P" are processed through Purchase
Order Entry only. Type "P" documents are not be allowed at
Point of Sale or Rental Invoicing.

X5-4 Point of Sale End of Month

When you run Point of Sale End of Month, the following
maintenance is done for purchase orders:


1) The Purchases MTD Report is automatically printed.

2) Posted purchase orders that were closed prior to the
specified purge date are moved to history. These orders will
not appear in the index and cannot be changed, but will
appear in reports.

3) Purchase orders that were voided prior to the specified
purge date are moved to history. These orders will appear in
reports, but can not be changed.

4) Purchase Orders are removed once they have been kept in
history for the number of months specified in Purchase Order
Profile (X12.18-5).

5) Purchase Order files are re-organized (cleaned up).

X55-1 Create Point of Sale Posting Batch
You can create a batch of Point of Sale documents only,
Purchase Orders only, or both. Payables accounting
transactions generated by Purchase Order Entry are included
in a Purchase Order batch. When a customer and P.O.S.
document number are specified on a purchase order, the
transactions generated by the part line on the work order (or
counter ticket) appear in a Point of Sale posting batch.

X55-2 Review & Post Point of Sale Documents
The vendor invoice number that is entered on the Purchase
Order Heading screen or on the Purchase Order Closing
screen is used as the document number on the payables
transactions. If a flooring vendor was used in Purchase Order
Entry, you can expect to see an error in the batch because of
the missing unit number.

NL


Accounting Transactions

To illustrate the accounting transactions that may be generated by a
purchase order, consider the following example:

Austin Parker brings his tractor in for repair. The morning he is to pick it
up, something goes wrong with a belt. You happen to be out of the belt
yourself, and there is no time to place a priority order. You know that
Gundie's Auto & Truck Supply carries the same belts; therefore, you
open a purchase order to Gundie's and put the belt on it. You will specify
that the belt is for Mr. Parker's work order. At this point you don’t know
the vendor's (Gundie's) invoice number, the due date, or how much
Gundie's is going to charge you, so it's OK to leave them blank for now.
You'll press {Cmd4] to print and hold the purchase order.

You'll give one copy of the purchase order to the GoFer at your
dealership who'll jump into a truck and run down to Gundie's. When the
GoFer gets back, there will be an invoice number, a due date, and the
actual cost to you which can be entered into the system.

The purchase order can be closed. Payables transactions are generated.
The part line with its corresponding sales code is placed on Mr. Parker's
work order. The cost of the part is your actual cost. Its selling price is
your cost plus the markup you designated in Purchase Order Entry.


 

Assuming that you owe Gundie's exactly $10.00 for the belt, the
transactions you can expect in the Purchase Order Posting Batch are:

Debit A1320 PARTS INVENTORY 10.00
Credit A2400 TRADE PAYABLES 10.00 GUNDIE -

Because the markup percentage is 125% these are the transactions you
can expect in the P.O.S. Posting Batch:

Debit A1110 ACCOUNTS RECEIVABLE 13.47

Credit A3320 PART SALES 12.50
Credit A2700 STATE SALES TAX : 97

There will also be some costing automatic transactions in the P.O.S.
batch, such as:

Debit A4320 PARTS COST OF SALE 10.00

Credit A1320 PARTS INVENTORY 10.00
LL

## CHAPTER X12.18-1

PURCHASE ORDER ENTRY

### Introduction

Purchase Order Entry is used to create, update, close, reopen, and void
purchase orders. It works like Point of Sale Invoicing (X5-1) and
Rental/Leasing Invoicing (X9-1), and allows full access to open, closed,
and posted purchase orders. For an overview of the Purchase Order
system and related accounting transactions, see Chapter X12-18, Purchase
Order Entry Menu.

The screens used for purchase order entry are presented in order:

1) Entrance Screen

2) Heading Screen

3) Detail Screen

4) Recap Screen

5) Closing Screen

6) Partial Closing Screen

### How To Run

From the Purchase Order Menu, select option 1, Purchase Order Entry.
The printer options are displayed.

## X12.18-1 PURCHASE ORDER ENTRY

   

ARC-AG,AUTO,CONS & TRUCK CO. Purchase Order Entry 1291-001
Division: A Option Screen

Enter printer ID for printing Purchase Orders:

Enter the number of heading lines to print (0-12):

For the Okidata printer, use 8.

For the IBM $256 printer, use 9.
For the IBM 4214 printer, use 12.
For the IBM PRO printer, use 12,

Enter the mumber of spaces left of normal to print (0,5):

For PC printers, use 5. (
For §/36 printers, use 0.

Fi-cancel ,

 

Change the defaults if necessary, and press [Enter]. The Purchase
Order Entry--Entrance Screen appears.

RELEASE 2.1 ae


X12,18-1 PURCHASE ORDER ENTRY

### Purchase Order Entry--Entrance Screen

ABC-AG,AUTO,CONS & TRUCK CO. Purchase Order Entry 1291-101 A
Division: A Entrance Screen

If a new purchase order, enter purchase order type:

Enter vendor name
or address number

Document #:

Fl-Cancel

 

New Purchase Order

To open a new purchase order, type the document classification code
for a"P" type document. Type a few characters of the vendor's last
name. Press [Enter]. The vendor index appears. Type any character
beside the name you want. The Heading Screen displays the vendor's
name and address.


X12,18-1 PURCHASE ORDER ENTRY

 

Existing Purchase Order

To recall a purchase order that is on hold, or to reopen a purchase
order that has been partially or entirely closed but not posted, do not
type a document classification code. Type a few characters of the
vendor's last name and press [Enter]. The vendor index appears.
Type any character beside the name you want. A list of the purchase
orders is displayed.

ABC-AG,AUTO,CONS & TRUCK CO Purchase Order Entry
x12T1-102 8 .
Division: S P.O. List - Vendor# DELOO1

9/08/95 © BES855 / BELMONT EQUIPMENT, INC. Not Posted

9/06/95 ¢ ANDERSON Posted

8/30/95 C FOR CASE POWER (CANADA) Posted (
8/28/95 P VERMEER Part posted

8/23/95 C.GREMILLION Posted

8/18/95 C FOR NETWORKS Posted

8/25/95 C KUENS Posted

8/02/95 C FOR KEY Posted,

7/31/95 P FOR FRITZ Part posted

Ts27195
7/26/95
7424195
7/24/95
7/12/95
7/10/95
7/07/95

LM Posted
FOR STRAUB Posted
FOR TK PITTSBURGH Posted
NUECES, TORRENCE, ZERA, DODGE, GOODRICH, HAZE Net Posted
FOR SNOW, WHITE, HOPF Posted
FOR NETWORKS Posted
BURNIPS Posted

¢
c
PB
c
c
c
c
>
7/27/95 © EMPIRE Posted
c
¢
c
°
¢
c

FlsExit F4=Return Enter=Paye forward

 

Each new purchase order is assigned a purchase order number. This
number is incremented by one each time a new purchase order is

f
RELEASE21  \_-


made. In other words, the higher the number, the more recent the
purchase order. This list displays the latest purchase orders first.

The date field to the right of the purchase order number indicates
when that purchase order was opened, closed, or posted.

The field to the right of the date indicates the status of the order. “O"
denotes an open document, "C" a closed document, "P" a partially
closed document, and "V" a voided document.

The field to the right of the status field is a description field. If an
order is open to a customer, the customer's number and name will
appear in this field. Otherwise, the description of the order's first part
line that has a price of zero will be used. These lines are usually
intended to be comment lines.

The field to the far right indicates whether or not the document has
been posted. Documents can be posted, not posted, or partially
posted. Once a document becomes posted it cannot be modified.

To select an order, place a character next to it and press [Enter].
Alternately, this screen can be bypassed altogether by typing a
document number at the Entrance Screen. °


 

### Purchase Order Heading Screen

DEALER INFORMATION SYSTEM Purchase Order Entry X12T1-103 ¢
Division: S . Heading Screen

PURCHASE ORDER # PO 20400 Open 9/08/95

Vendor: MAXO01 Telephone . . (821) 411-8220
MAX COMMUNICATIONS Work telephone: (811) 410-4421
Fax... (811) 410-4421

1621 NORTH WILSON .

LEWISTON, ID

Employee: PECKOZ

Vendor Inv#: . {
Due Date: o00000

Ship By:

Resale information:

Customer/stock#: E1013 Use custemer as reference only: Y
Customer Name:

POS Document:

F3=Print/Hold F4=Hold F9=Reopen Fl0=void Fll=Transfer EntersContinue

 

Type the employee's address number (required), the vendor's invoice
number if you know it now, and shipping information. The “Ship By"
field provides instructions for the vendor and is not used by the system. If
the purchase does not concern a customer's Point of Sale document, press
(Enter] to continue. The detail screen appears.

RELEASE 2.1 tO


 

NOTE: The Vendor Invoice number is used as the document number for
the payables accounting transactions. The same field is available for input
on the Closing Screen.

Resale Options

To create a link between the purchase order and a customer's Point of Sale
document, fill in the "Customer/unit#" field and set the "Use customer as
reference only" field to no. Once you press [Enter], a list of the
customer's P.O.S. documents is displayed. Type any character beside the
open document to which the purchase order line(s) will be transferred.
Lines that are marked for resale (with an R in the resale field) created on
this purchase order will automatically be copied into the P.O.S. document
you select on this screen when the purchase order is closed. Press [Enter].
The detail screen appears. Resale information, the customer's name and
the P.O.S. document number are displayed at the top.

Alternately, if "Use customer as reference only" is set to yes, the
customer's number and name will only be used as the description for that
purchase order and lines created on it will not be copied to that customer's
invoice. If this flag is set, pressing [Enter] takes you directly to the detail
screen. The default value of this flag is set in Purchase Order Profile
(X12.18-5).


 

### Options

[Enter] Continue to the detail screen.

[F3] Print and hold. See the Printing Options section
below for information about printing invoices of -
different sizes. :

[F4] Hold without printing or closing.

[F9] Reopen a closed document. A document that has
been posted cannot be reopened.

[FLO] Void the current document. If the document is
partially closed, only open lines will be voided.

[Fil] Transfers the document to a different vendor. Only

open documents can be transferred.

Note: Any action can be performed on a document that has not been
posted. Some actions may require more than one step. For example, to
transfer a document that has been partially closed, you would need to
reopen it before being transferred.

Printing Options

An option now exists that allows you to print purchase orders on 7" or 11"
invoices. As purchase orders do not print headings, you must use
preprinted forms for headings to appear on the invoices.

RELEASE 2.1 Lo


 

PURCHASE ORDER DETAIL SCREEN

ABC-AG,AUTO,CONS & TRUCK CO Purchase Order Entry
Division: $ Detail Screen
PURCHASE ORDER # PO 20484 Vendor: DELOO1 Open. 10/11/95
Resale: * Customer:
TOR Line C, Qty Description
R 10 PUR 2 WIDGETS

“1271-104

Ext Price Disc
4.00


WORK IN PROCESS

TDR Line PC. Qty Description
0020 PUR

 

F2=Print/Close F3=Print/Hold FdsHold F7=Return F2d=More keys Roll

This screen works like the Point of Sale detail screen except that a
purchase code is used instead of a sales code.

An additional field between "Description" and "Ext Price" will display a

*S, *C, or be blank. A line with a *C is closed. A line with an *S is split.
Once a split line is closed, it will be marked with a *C. See below for


 

more information on splitting lines.

The "TDR" on the far left stands for: Tax, Discount, and Resale.

The Tax and Discount apply to the purchase order, not to the customer's .
P.O.S. document, if any. Lines from purchase orders that are transferred
to a P.O.S. document use the tax and discount codes assigned to the
customer in Receivables Maintenance. Lines marked Resale are displayed
on the Closing Screen.

Items marked for Resale are taxed unless you use a blank tax code or a tax

code defined as zero in Tax Configuration Maintenance. The tax code for

a purchase code is taken from Purchase Code Maintenance (X12.18-6).

tems marked for resale will be copied into a Point of Sale invoice. Hence, {
this field will only be available to purchase orders that are opened to a

customer with the "Use customer as reference only" field set to no. See

the discussion of the Header Screen above for more information.

Purchase Order Entry Uses Point of Sale tax codes WITH THE

EXCEPTION OF THE BLANK TAX CODE. Purchase Order Entry
considers a blank tax code to be zero.

 

You can change the purchase code by typing over the one that is displayed.
Enter the information for the merchandise you are ordering. Press [Enter]
to place the line on the document.

You can combine taxable and non-taxable items on the same purchase
order. Likewise, you may receive discounts on some parts but not others.
By changing the Tax and Discount codes, you can control them line-by-
line. Remember Tax and Discount codes pertain to the purchase order.

RELEASE 2.1 LO


 

NOTE: You can combine merchandise for internal use and parts for resale
on the same purchase order. Just remove the "R" for resale for
merchandise purchased for internal use. Parts not flagged for resale do not
appear on the Closing Screen; however, they are printed on the purchase
order. If you forget to remove the "R" (or think it's too much trouble), you
can do it on the Closing Screen.

### Correct Or Delete Lines

To correct a line, replace the current line number and purchase code with
the line number and purchase code on the incorrect line, and press [Enter].
The line comes "down" for correction. The original line is still displayed
on the document, but it is replaced with the corrected line as soon as you
press [Enter]. To delete a line, bring it "down" for correction and press
[Fé].

### Split Lines

To split a line between multiple customers, press [F9] while editing it. A
window appears that will allow you to distribute quantities of an item to
different customers. Only Parts or Misc. Quantity lines can be split. See
Purchase Code Maintenance (X12.18-6) for more information.

Lines that use a Purchase Order code with a DEBIT setting of *PROMPT
cannot be split.


 

### Parts Purchase Order Code

When lines that use the Parts Purchase Order Code are added to the
invoice, the contents of the description field are used to perform a parts
search. If there is an exact match between the description field and a part
number that is supplied by a single vendor, pricing information from that
part is automatically copied into the line. If the description field matches
the part number for multiple vendors or if an exact match is not found, a
list of part numbers appears. The part you select from this list will
automatically be copied onto the purchase order.

When a line that uses the Parts Purchase Order Code is posted, a stock
order for that part is created and received so that the part's quantity and
order history will be accurate.

Press [Fi3] to see the Recap screen.

RELEASE 2.1 tO


 

### Purchase Order Recap Screen

ABC-AG,AUTO,CONS & TRUCK CO. Purchase Order Entry ‘X1291-107 G
Division: A Recap Screen .

PURCHASE ORDER # FO 00004 Vendor: ‘GUNDIE 7424/90
Resale: COUNTER TICKET # CT 00106 Customer: BOULOL

Purchase Order Amount
Discount/surcharge
Subtotal ©

Tax

Purchase Total

Billing Amount

Non-taxable lines
Taxable lines
Total

Enter-Previous screen

 

Taxable lines are those with a tax code other than blank on the detail screen.
Items marked for resale are taxed unless you give them a blank tax code or
a tax code defined as zero in Tax Configuration Maintenance.

Purchase Order Entry Uses Point of Sale tax codes WITH THE
EXCEPTION OF THE BLANK TAX CODE. Purchase Order Entry


considers a blank tax code to be zero.

To return to the detail screen, press [Enter]. To close and print the purchase
order, press [F2]. The Closing Screen appears.

### Options

{F2] Print and close.

{F3] Print and hold.

[F4] Hold without printing or closing.

[F5] Refresh the screen (useful if the screen becomes
garbled).

[F6] Delete line.

[F7] Return to the heading screen.

[F9] Split line.

(Fi3] Dispiay Purchase Order Recap screen.
CC


X12,18-1 PURCHASE ORDER ENTRY

 

### Purchase Order Closing Screen

ABC-AG,AUTO,CONS & TRUCK CO. Purchase Order Entry ‘¥i291-105 E
Division: A Closing screen
PURCHASE ORDER # PO 00004 Vendor: GUNDIE Open 7/24/90
Resale: COUNTER TICKET # CT 00106 Customer: BOULO1

RSC Line Qty Description Price/Dise % Resale

RMP 10 1 ELEMENT . 13.00 1250 1813
RMP 20 5 GASKET 18.09 1250 2244

Vendor Invoicek: V-INV 9058 Bue Dace

Cmd2-Close entire order Cmd7-Return Cmdl0-Close Selected Lines Roll-Page

 

This screen displays open lines only. You can change the sales code or the
customer's price of any line. To change the price, [Field Exit] through the
percentage markup, and enter the new selling price. The system calculates
the corresponding percentage of the markup. To change the markup
percentage, type over the old one. Press [Field Exit] and [Enter]. The
system calculates the new selling price.


 

If you have not entered the vendor's invoice number and due date, do so
now. The invoice number will be used as the document number in the
purchase order batch. To close and print the document, press [F2] again.

NOTE: If you forgot to remove the "R" for resale on some parts for internal

use, remove it here. After you press [Enter] the part(s) will no longer
appear on this screen.

### Closing Individual Lines

To close individual lines on the purchase order, press [F10]. The Partial
Posting Screen appears.

RELEASE21 \_-


ABCAG,AUTO,CONS & TRUCK CO Purchase Order Entry x12T1-106 F
Division: § Partial Posting Screen
PURCHASE ORDER # 20 20179 Vendor: © DELOOL 5/31/95
Resale: * Customer:
X=Close only, already posted ¥=Close and post
Line # Qty Description Price/Disc Invoice D/Date
10 1 DRAPES 525.00 100441 112495
20 1 CARPET 1380.00 100441 = 122495
30 1 RENOVATION :00 100441111495,

1905.00

F2eClose lines F7=Return Roll

 

To mark a line as closed without including it in the posting match, mark it
with an "X." To mark a line as closed and include it in the posting bate!
mark it with a “Y." :

The invoice and due dates for each line will default to what was entered on
the Closing Screen. These fields can be changed on a line by line basis..

Press [F2] to close lines marked with an "X" or "Y." The Closing Screen
reappears. The lines are now closed and the purchase order is posted. The
Heading Screen reappears.


 

### The *Prompt Debit Code

The *PROMPT debit code allows you to distribute the debited amount of a
purchase order line to multiple accounts. Whenever you close a line that
has a Purchase Order Code with *PROMPT in the debit field, the following

window appears.

ABC-AG, AUTO, CONS & TRUCK CO Purchase Order Entry x1271-105
E
Division: S Closing Screen
PURCHASE ORDER # PO 20489 Vendor: DELOO1 Open 10/12/95
Resale: * Customer:

RSC Line# Qty Description Price/Dise
1e WIDGET

: Postings for: S/DELOO1/PO20489/MAX/0010  X12T1B :

1 Must sum to: 100.00

: Account Amount Address Stock Due Date
10/10/95
10/10/95
20/20/95
10/10/95
10/10/95:

: Bottom

: Fl-Exit/Update F4ePrompt Account/Address Roll

: EntersValidate ~

Vendor Invoice#: L240

Purchase order number S/DEL001/P020489 is being updated.


 

Complete all appropriate fields, making sure that the total of the new
postings equals the amount specified at the top of the window. Press [F4]
to view a list of accounts (see example below).

DEALER INFORMATION SYSTEM Purchase Order Entry X1221-105 &
Division: $ Closing Screen

: Select G/L Account
: 1sSelect

: Opt Account Ed Deseription Acct. #1
: cise W GOODWILL. 530
cies X AMORTIZATION ~ GOODWILL
201 CREDIT LINE
: 220 BANK NOTES
— : c240 TRADE PAYABLES

: F3eExit Roll

F3=Exit/Update Fa=Prompt Account/Address
. : Enterevalidate
Vendor Invoicet: 1000

 

Press [Enter] followed by [F3] when finished.


X12,18-1 PURCHASE ORDER ENTRY

 

OPTIONS FOR THE CLOSING SCREEN

{F2} Close and print.

(F4] Provides prompt for searching for an account
or address.

{F7] Return to the detail screen.

{Page Down] Display the next page of purchase order lines.

RELEASE21 |.

## CHAPTER X12.18-2

OPEN PURCHASE ORDERS REPORT

### Introduction

Use this job to print all open purchase orders currently in the system,
regardless of date. The report can be printed in order by vendor address or
by purchase order number.

### How To Run

From the Purchase Order Menu, select option 2, Open Purchase Orders
Report. The print options are displayed.

Open Purchase Orders Report x12920-001

Report by Vendor Address Number, enter "Y*....  ¥

Report by Purchase Order Number, enter "Y"....

Fi-cancel

### X12,18-2 Purchases Mtd Report

Select either vendor address number or purchase order number, and press
{Enter]. The report is placed on the job queue.

An example of the Open Purchase Orders Report follows.

ABC=AG, AUTO, CONS & TRUCK CO. OFEN PURCHASE ORDERS Date 5/23/90 Page 1
DIVISION: A VENDOR ORDER Time 10.56.53 xiz920
Pocunent open. address

Resale
Number ‘Date =simp. # Number Vendor Nane

Purchase Amt. Dec. # Cust # Name
25.68

Resale Ant.

7000002 © 6/28/90 STAROL UNAUTO UNITED AUTO ELECTRIC
1 LISTED
LL

## CHAPTER X12.18-3

PURCHASE ORDER REPORT

### Introduction

Use this job to print a list of open and closed purchase orders that were
created on any date within the history period selected for the current
division in the Purchase Order Profile. The report can be printed in order
by vendor address number or by purchase order number, and there is an
option to include closed purchase orders that have not been posted. The
Purchase Order Report includes:

- Purchase order number

- Vendor's address number

- Vendor's name

- Purchase amount (cost to the dealership)
- Employee address number

- Customer's address number

- Customer's P.O.S. document number

- Resale price (selling price to customer)

### How To Run

From the Purchase Order Menu, select option 3, Purchase Order Report.
The print options are displayed. Note that the starting and ending dates
default to the current date, but they can be changed.


[| X12.18-3 PURCHASE ORDER REPORT co

Purchase Order Report X12930-002
Report by Vendor Address Number, enter “Y"....
Report by Purchase Order Number, enter "Y"....
Include Closed or Open status..." "/"C*/*0"...

Note: blank equals list all

Starting date to include.... 081398

Ending date to include. 081398

Fl-cancel

 

To list both open and closed purchase orders, field exit through the
"Include Closed or Open status" field to leave it blank. Otherwise, use "C"
to restrict the report to Closed purchase orders only, or use “O" if you want
Open purchase orders only.

Make your selections and press [Enter]. The report is placed on the job
queue.

RELEASE 2.2 LO

## X12.18-3 PURCHASE ORDER REPORT

An example of the Purchase Order Report follows.

ABE-AG,AUTO.CONS & TRUCK CO. PURCHASE ORDER REPORT
Dace 7/24/93 Page 1

Divisron: & VENDOR GR0ER
ime 11.27.37 212930
Pocumens, address Resale

Numker Date Ep. & Number Vendor Name Purchase Ant. Doc. # Cust # Name esale Amt.
POO0GO4 © 7/24/92 STARZ GUNDIE GUNDIE'S AUTO & TRUCK SUPPLY 34.09 ¢T02106 BOULO? Stim BOULDERMAN,
FOUGG03 0 7/24/98 STAROX UNAUTO UNITED AUTO ELECTRIC 29.13

2 Posted and Closed Listed.

 


Notes:

## CHAPTER X12.18-4

PURCHASES MTD REPORT

### Introduction

The Purchases MTD (Month-To-Date) Report lists all purchase orders for
the selected month; otherwise, it includes the same information as the
Open Purchase Orders Report. The report can be printed in order by
vendor address number or by purchase order number, and there is an
option to include closed purchase orders that have not been posted. The
Purchases MTD Report includes:

- Purchase order number

- Vendor's address number

- Vendor's name

- Purchase amount (cost to the dealership)
- Employee address number

- Customer's address number

- Customer's P.O.S. document number

- Resale price (selling price to customer)

### How To Run

From the Purchase Order Menu, select option 4, Purchases MTD Report.
The print options are displayed. Note that the month and year default to
the current month and year, but they can be changed.

## X12.18-4 PURCHASES MTD REPORT

 

Purchases Month-To-Date Report x12940-001

Report by Vendor Address Number, enter "Y*....

Report by Purchase Order Number, enter “Y"....

Include Closed purchase orders even though
they are not yet posted (if any), enter "¥*...

Month to report

Year to report

F1-Cancel

 

Make your selections and press [Enter]. The report is placed on the job
queue.

An example of the Purchases MTD Report follows.

 


 

ABC-AG,AUTO,CONS & TRUCK CO. PURCHASES M-T-D REPORT Date 7/24/90 Page 1
DIVISION: A \VENDGR CRDER ‘Time 11.39.27 x12940
Document address Resale

Number Date Pup. # Number Vendor Name Purchase Amt. Doc. # Cust # Name Resale Ant.

PoD0004 «7/24/90 STAROI “GUNDIE GUNDIE‘S AUTO & TRUCK SUPPLY 34.09 CT00106 BOULC, SLIM BOULDERMAN 38.37
pov0003 © 7/24/90 STAROL UNAUTO NITED AUTO ELECTRIC 20.33
2 Posted and Closed listed.

 

MAACCOUNTING


Notes:

## CHAPTER X12.18-5

PURCHASE ORDER PROFILE

### Introduction

Set up the Purchase Order Profile before you attempt to use the Purchase
Order system. :

In this job you will supply default information to be used during Purchase

Order Entry. Furnish this information for each division in which Purchase
Orders are used.

### How To Run

From the Purchase Order Menu, select option 5, Purchase Order Profile.
The Purchase Order Divisional Profile screen appears.

## X12.18-5 PURCHASE ORDER PROFILE

 

Purchase Order Divisional Profile X12950-1

Division. ABC-AG, AUTO,CONS & TRUCK CO.

Enter printer ID for printing purchase orders

Enter number of heading lines to print (0-12)

Enter number of spaces left of normal to print (0,5):

default billing percentage (33% as 1330)

default purchase sales code..

default billing sales code for point of sale..: MISC PARTS

number of months to store in histoxy file.....: (
Enter Resale number to print on purchase order......:

Use customer number as reference only (¥.N).

cmdi-cancel

 

Respond to the prompts on the screen. Enter printer ID
for printing purchase orders. The printer you'll use most
often for purchase orders.

Enter number of heading lines to print (0-12).
Okidata: 8
_ IBM 5256: 9

i
RELEASE21 0


X12.18-5 PURCHASE ORDER PROFILE [=]

IBM 4214: 12
IBM PRO: 12

Enter number of spaces left of normal to print (0,5)
PC printers: 5
S$/36 printers: 0

Enter default billing percentage
Enter the markup percentage you use most often
(percent over your cost charged to the customer). Type
133% as 1330. The system uses this markup to
calculate the selling price of parts that are transferred to
a customer work order or counter ticket. The
percentage and the selling price can be changed in
Purchase Order Entry.

Enter default purchase sales code
Enter the 3-character purchase code (set up in Purchase
Code Maintenance, X159-6) that you use most often.

Enter default billing sales code for P.O.S,
Enter the 2-character P.O.S. sales code (set up in Sales
Code Maintenance, X52-3) you use most often for
purchase orders. The sales code and the purchase code
must have the same format (both "M" or both "D").

Enter Resale number to print on purchase order
20 digits. Tax Number issued by the state for resale

items.

Enter number of months to store in history file:

MAACCOUNTING


 

Enter the number of months of purchase orders you
want to keep in the history files. Valid entries are 001-
999. Purchase orders are moved to history through
Point of Sale End of Month (X5-4). Purchase orders in
the history file can only be used to generate reports and
cannot be changed.

User customer number as a reference only
YorN. This sets the default for a field of the same
name that appears in the Purchase Order Heading
Screen. Refer to Purchase Order Entry (X12.18-1) for
more information about this field.

t
RELEASE2.1  \_-

## CHAPTER X12.18-6

PURCHASE CODE MAINTENANCE

### Introduction

Use Purchase Code Maintenance to set up codes that are used in Purchase
Order Entry. Purchase codes use miscellaneous ("M"), parts ("P"), or
descriptive ("D") formats and include defaults for the following items (all
of which can be changed on the purchase order).

- Tax Code

- Discount Code

- Sales Code

- Default Markup percent

### How To Run

From the Purchase Order Menu, select option 6, Purchase Code
Maintenance. The Purchase Code Maintenance screen appears.

ABC~AG,AUTO,CONS & TRUCK CO, PURCHASE CODE MAINTENANCE 1296-101
Division: A

Purchase Code

 

Enter the code you want to add or change, and press [Enter]. The remainder
of the screen is displayed.

## X12.18-6 PURCHASE CODE MAINTENANCE

ABC-AG, AUTO, CONS & TRUCK CO.

Division: A
Purchase Code PUR
Description

PARTS P.O.

Format

Debit

Purchase 1320

Defaults
Tax Code T
Discount Code

Sales Code PC
Markup $ 1250

Fl-End job F3-Go back

2400

(333 as 1330)

PURCHASE CODE MAINTENANCE 1296-102

New Sales Code

‘D's Misc. Description, ‘M'= Misc, Quantity, 'P’= Part

Credit

*PROMPT Prompt in debit only
*AUTO ‘Wild Card in credit only

F19-Delete this purchase code

 

The fields on the Purchase Code Maintenance screen are described below
in the order in which they appear on screen.

Description

15 characters. Short description of the purchase code

which is printed on the purchase order.

Format

Purchase order codes can be in formats "M" (Misc.
Quantity), "D" (Misc. Description), or "

 

(Parts)
io


Purchase
Debit

X12.18-6 PURCHASE CODE MAINTENANCE [2]

only. The miscellaneous format allows a quantity
and description. The descriptive format allows a
description only. The parts format is like the
miscellaneous format except it includes a parts
search. When lines that use the parts format are
added to an invoice, the parts files are searched for
records that match the description you entered. If no
exact match is found (or if multiple vendors have
parts that match), you will be prompted to select the
correct part. Once the part is selected, pricing
information and will automatically be copied into the
purchase order.

When a purchase order with a part line on it is posted
a stock order for that part is created and received so
that part's quantity and order history will be accurate.

Lines that use Sales codes and purchase codes must
have the same format, both "M" or both "D" or both
"pt

Only lines in an "M" or "P" format can be split. For
more information on splitting refer to Purchase Order
Entry (X12.18-1).

The General Ledger account that is debited, usually
an inventory account or an expense account, such as
PARTS INVENTORY or SHOP SUPPLIES
EXPENSE.


[ «| X12.18-6 PURCHASE CODE MAINTENANCE

When this field is set to *PROMPT, the user can
distribute the debited amount to multiple accounts.
The distribution list includes entries for the address
and stock number. See the Closing Screen in
Purchase Order Entry for more information.

Lines that use the *PROMPT debit code cannot be
split.

Credit The General Ledger account that is credited for the
purchase order, such as TRADE PAYABLES.
"* AUTO" will use the General Ledger account
attached to the vendor on the purchase order.

Default Tax Code — The tax code used most often for this purchase code.
Tax codes are set up in Tax Code Maintenance
(X52-7). The tax code can be changed on the
purchase order. This tax code pertains to the
purchase order only. Part lines that are transferred to
a P.O.S. document use the default tax code assigned
to the customer in Receivables Maintenance.

‘Purchase Order Entry uses Point of Sale tax codes WITH THE

EXCEPTION OF THE BLANK TAX CODE. Purchase Order Entry
considers a blank tax code to be zero.

 

Default Discount The discount code used most often for this purchase

Code code. Discount codes are set up in Discount
Maintenance (52-6). The discount code can be
changed on the purchase order. This discount code

RELEASE 2.1 CO


Default Sales Code

Default Markup
percent

### Options

Cmd1-End job
Cmd3-Go back

Cmd19-Delete

X12.18-6 PURCHASE CODE MAINTENANCE [=]

pertains to the purchase order only. Part lines that
are transferred to a P.O.S. document use the default
discount code assigned to the customer in
Receivables Maintenance.

The sales code used most often for this purchase
code. Sales codes are set up in Sales Code
Maintenance (X52-3). The sales code can be
changed on the purchase order. The sales code and
the purchase code must have the same format--both
“M", both "D", or both "P".

The markup percentage used most often for this
purchase code. Type 133% as 1330. The system
multiplies this percentage by your cost for a part to
calculate the selling price that is transferred to the
customer's P.O.S. document. You can change the
markup percentage and/or the selling price on the
purchase order. A part that is sold on a POS
document with a selling price that does not match
base 4 will appear on the Price Override Report
(X56-11).

Ends the Purchase Code Maintenance job and returns
to the Purchase Order Menu.

Cancels changes and returns to the purchase code
prompt.

Delete purchase code.


Notes:

## CHAPTER X14-1

ACCOUNT INQUIRY

### Introduction

Account Inquiry allows you to:

= view the balance and characteristics of a general ledger account.

"= request a print of the inquiry which contains all debit and credit
information for selected months.

= view transactions for the general ledger account.

### How To Run

From the General Ledger Menu (X1-4), select option 1, Account Inquiry.
The Balance Information Screen appears.

## X14-1 ACCOUNT INQUIRY

BALANCE INFORMATION SCREEN

‘A & R EQUIPMENT SALES
Division: A Balance Information
Account #:

Open Months Balance
Year to Date Balance

Quantity 0
Month to Date
94
Title 94
Edit Code 94
Debit Code 94
Account #1 93
Account #2 93
Factor 93
‘Type 93
93
93
93
93

Year End Adjustments

cmdi-End Job

cmd3~Transactions

GENERAL LEDGER ACCOUNT INQUIRY

K14101-01 1

Enter ¥ for printout

Qty Year te Date

cmd8-Index  Cmd1¢-Totals

 

Select the number of the account for inquiry. Key it into the "Account #

field.

If you do not know the number, press [Cmd8j to display the index.
Position the cursor next to the account for inquiry and press any character.
You do not need to press [Enter]. The account you selected will be

displayed on the Balance Information Screen.

Ne


X14-1 ACCOUNT INQUIRY [=]

Account information is displayed at the left of the screen. The Account #,
Title, Edit Code, Debit Code, Account #1, Account #2, Factor and Type
are filled in with information that has been entered at Account
Maintenance (X14-2).

Tf something looks strange in the information that's presented on this
screen, you could print out the general ledger register for this month. Put
a"Y" in the "Enter Y for printout" field. A sample printout is shown in
the "Printout of General Ledger Information" in this chapter.

### Field Definitions

Open month balance The figure is comprises of all debit and
credit entries to the general ledger during all
open months.

Year to date balance This figure is updated every time an entry is

made to the account. It is a total of all debits
and credits for the fiscal year.

On the right of the screen is the breakdown
for all closed months. Twelve months of
history are listed on the screen. The most
recent closed months appears at the top of
the list. The oldest closed month is on the
bottom.

Month to date The figures represent the total of all debits
and credits posted to the account during the
month.


[ «| X14-1 ACCOUNT INQUIRY
{

Year to date The total of all debit and credit entries for
the fiscal year at the time the month was
closed.

Year end adjustments The total of all adjustments in the thirteenth
month.

Commands Available

[Cmd1] End. Return to the General Ledger Menu. :
[Cmd3] Displays the Transaction Display Screen, detailed below.
[Cmd8] Displays the General Ledger Index.

[Cmd10] Displays the Open Month Balance Screen, detailed below.

RELEASE 2.1 ae

### Transaction Display Screen

A & R EQUIPMENT SALES GENERAL LEDGER ACCOUNT INQUIRY x14101-02 2
Division: a Transaction Display

Account #: A1000 CASH ON HAND
Open Months Balance 28,178.37 Year to Date Balance 29,178.37

Posting

Decument# Date D/C Amount Description addr#  stock#

cR7813 10/06/94 $00.32 CORRECTION — DOROO1

110004 Bs/1isga 5.00

Z10005 8/08/94 5.00

uso0104 #* 8/03/94 215.60 :

z00000002 8/08/94 3.33

ro000e002 = 8/08/94 3.00

rooo0co02 = 8/08/94 7.00

invoocoo, = 8/08/94 5.00

Invooooo2 =—-8/08/94 5.00

1v00027 #* 5/01/86 50.00 P, ORLOWSK

£800203 5/01/86 18000.00

ch#12345 5/30/86 499.76 WARRANTY

cKeo21 5/01/86 3500.00 ROA SEREOL
Gmdl-End Job Cm2-Balance Info Cmdd-History Cmd8-Index cmd10-Total :
Home-Top Roll~Page

   

This screen displays the G/L transactions to this account during all open
months. To display G/L transactions during closed months, press [Cmd4].

Commands Available

[Cmd1] End. Return to the General Ledger Menu.
[Cmd2] Displays the Balance Information Screen, detailed above.


[Cmd4] History. Toggles between displaying open and closed
month transactions.
[Cmd8] Displays the General Ledger Index.

[Cmd10] Displays the Open Month Balance Screen, detailed below.

### Open Month Balance Screen

A & R EQUIPMENT SALES GENERAL LEDGER ACCOUNT INQUIRY X1d101-04 4
Division: A Open Months Balance

1000 CASH ON HAND ‘Type A

Bal-- april on: 140,000.00

Debits Credits Balance

$17 128449.75 422 68413.25 939 100036.

600 9234.12 $122 80130.11 2112 iliac.

429 63556.55 315 29449.76 734 145248.
145248.
145248.
145248.
14524e.
145248.
145248.
145248.
145248.
145248.


md1-End Job Cmd3-Return

 

This screen displays (from left to right) the total number of debit
transactions, total debits, the total number of credit transactions, total

RELEASE 2.1 Lo


credits, the total number of transactions, and the balance. These totals are
displayed for all open months.

Press [Cmd1] to return to the Payables menu; [Cmd3] to return to the
Transaction Detail Screen.

### Printout Of General Ledger Information

If you were looking at the balance and something did not look right, you
could print out the general ledger register for the account. This report lists
all transactions for all open months.

‘You may request a printout of account information and transactions by
entering Y in the "Enter Y for printout" field. Press Enter. Inquire on the
next account. Request a printout. When ail the printouts are chosen, press
[Cmd1] to end the job. A printout is illustrated below.

Note:

The running balance and subtotals in the example are not accurate:
ll lines have been deleted from the report in order to illustrate its format
on this page.


A @ R EQUIPMENT
BELLINGHAM, WA L
1240 PAYABLES

oath
Year to Date

Month
Year to Date

ocr
22152.23-
69504.71
APR
2216.66
164028.90

GEVERAL LEDGER REGISTER

se?
15982.33,
90656.94
MAR
8e67.08,
162922.28

MP 1102
auG
49010.83-
74874.61.

FEB

42491.06
isaces.16

L300
mn
556¢4_a0:
123685.44

m0
= 17108.36-
169330.24

gan pec

39837.41
105954.10

4 58965.75-
70136.66

Date $/16/94 Page

1410-30

mae
42409.70
206438.50
Nov
17708.76
129102.41


 

Beginning Balance 69504,71

ALLE!
BOUNDARY
BOUNDARY
BURL FN
URL FH
cascanE,
cee 16881
cee 16852
cK 16858
Ke 16359
cKE 16860

04 CHK 23333
04 ocwo
04 i

21/11/93
31/14/93
31/24/93

11706793

31/06/93

aiy9sa3

11/21/93 ALLIED
11/12/93 ALLIED
20/23/93 BURL FINE
21/05/93 BOSHAN
10/23/93 oT

4/17/93 PD FLY BILL
4/20/93 FLYERS
4/17/93 FLYERS

802306
200219
300219
304852
504852,
couse
02366
02346
B04851
06471
00298

w02240
07203
wo2240

22/20/93
21/10/93
11s20/93
11/10/93
1/10/93
12/10/93
aas30/93
11/30/93
12/10/93
3110/93
3110/93

4n753
4722053
4/19/93

Open Months Total

442018.87

147.00
142165.87

Year co Date

6.66
4.72
87.95
27.89
6.58
226.55

26487.48

100003.64

2.00-
26.99
100.09
197,09
1o0198.62
26537-48

26537.48
42967.23-
Ke

### X14-1 Account Inquiry [2]

The account number and name of the account print at the top of the report.

Twelve months of history are provided. The most recent closed month is
listed first and the oldest closed month is listed last. You are provided with
the total of all debits and credits to the account for that month in the
"Month" field. The "Year to Date" field contains the year to date total
balance at the time the month was closed.

The BEGINNING BALANCE field on the report will contain the year to
date total balance of the month most recently closed.

All debits and credits will be listed for each open month. The transactions
will be separated by posting month.

The transaction from the example on page 3 reads:

J 07 CK#3426 7/07/86 JULY RENT D_ 750.00

i What was entered in the ID field at Create Source
Documents (X1-7).

07: Equals the posting month from Create Source Documents
(1-7).

CK#3426: What was entered in the Document field at Create Source
Documents (X1-7).

T07/86: Posting date from Create Source Documents (X1-7).

JULY RENT: Information from the Description field at Create Source
Documents (X1-7).


X14-1 ACCOUNT INQUIRY a
if

D: Debit or credit code from Create Source Documents.

750.00: Amount of the debit transaction. The credit transactions
will be listed on the right side of the column. Both columns
will be subtotaled by open month.

You will see other numbers you recognize. If you entered something in a
field at Create Source Documents, the information will appear on the
General Ledger Register. If a stock number was entered, the stock number
will appear on the transaction line.

At the bottom of the General Ledger Register is a debit and credit total for
all open months. The BEGINNING BALANCE plus the OPEN MONTHS
TOTAL equals YEAR TO DATE.

### Sales Transactions Counters

Sales Transactions Counters are a feature designed expressly for former
ADMS Dealers. The ADMS system maintained on-going counts of
invoices posted to various ledger sales accounts. When ADMS dealers
convert to DIS/400, DIS stores up to 24 months of these counts in the file
u.GLC.

In the DIS system, counts are accumulated from POS batches (X55-2) and
from Create Source Documents (X1-7). Transactions are counted for sales
accounts only; furthermore, transactions are counted by invoice, regardless
of amount, positive or negative. In other words, each time a document
includes a credit or debit to a sales account, the counter for the account is
increased by one. No attempt is made to ascertain how many or which

fl
RELEASE 2.1 Ne


X14-1 ACCOUNT INQUIRY [~]

parts may be represented by the transactions or whether it is a sale or a
return.

Sales transaction counters are displayed for in Account Inquiry (X14-1),
where a "Quantity" field appears for sales accounts only. The system
stores counts for each sales account for 24 months. The oldest month is
purged when Accounting End of Month runs.

Preparation

To take advantage of the sales transaction counters, the following
conditions must exist:

= The dealer must be an automobile dealer: the PRODINSTL, OPT
switch must be on. At any menu, type: PRODINST, OPT switch
must be on. At any menu, type: X00081 PRODINST, 1 [Enter].

™ The file u.GLC (u-User ID associated with the dealer's files) must exist.
To create u.GLC, run Initial File Setup (X6-7).


Account Inquiry Screen

ABC-AG,AUTO,CONS & TRUCK CO, GENERAL LEDGER ACCOUNT INQUIRY x1410-101 1
Division: A Balance Information

Account #: 3320 Enter ¥ fer printout
Open Months Balance 19,748.14 Quantity 0
Year to fate Balance 36,368.82 Month to Date Qty = Year ro Date
APR 94 16,135.42 aa 16,620.68
Title PARTS-COUNTER MAR 94 3,642.41- 12 485.26
Edit Code A FEB 94 13,240.19- 34 4,127.67
Debit Code P JAN 94 17,367.86 12 17,367.86
Account #2 DEC 93
Account #2 Nov 93
Factor ocr 93
Type 93
93
93 (
93
93

Year End Adjustments

Grdi-End job Cmd3-Display transactions

 

The current month's quantity appears to the right of its balance. Quantities
for prior months are for the month only-not year-to-date.

RELEASE 2.1 Lo

## CHAPTER X14-2

ACCOUNT MAINTENANCE

### Introduction

Account Maintenance is used to set up all general ledger accounts. It is
also used to make changes to general ledger accounts that already exist. If
you are setting up a new division or installing your first general ledger,
refer to General Ledger Menu (X1-4) and the Accounting Manager's
Handbook for more information. In these 2 manuals, you'll find more
information about numbering G/L accounts and how to set them up, a
discussion of departmentalization, and examples of each kind of account.
A summary of the information required for each type of account can be
found at the end of Chapter X1-4.

When you have finished with the maintenance that is necessary, run a
chart of accounts (X14-3). Check it carefully to make sure that all the
accounts are the way you want them.

### Restricting General Ledger Accounts

General ledger accounts can be restricted to prohibit posting. You may
want to stop posting to an account because you plan to delete it at end of
year. When an account has been restricted:

Posting. Further posting to it is prohibited, but reporting is available.

Index. It is not listed in the general ledger index except in Account Inquiry
(X14-1) and Account Maintenance (X14-2).

Chart of Accounts. It may or may not be included on the chart of accounts
depending on the setting of OPT switch, “Restricted Accounts,” which is
located on the OPT General Ledger Menu Two (X6312). The default
setting is not to print restricted accounts. If you want restricted accounts to
be listed in the chart of accounts, set the switch “on.”

Financial Statement. Asset and liability accounts are not printed on the
financial statement if they are restricted with no year-to-date balances.
Income and expense accounts are not printed if they are restricted with no


[2] X14-2 ACCOUNT MAINTENANCE c

month-to-date or year-to-date balances. Sales accounts are not printed if:
both the sales and cost of sales accounts are restricted, and they are
restricted with no month-to-date or year-to-date balances.

Removing a Restriction

It may occasionally be necessary to remove the restriction from an
account. Example: An invoice has been posted to a payables account. One
of the accounts involved is restricted after the invoice has been posted.
Later, the voice is canceled. When you try to cancel it, a message will
inform you that the account is invalid or restricted. At that time, you will
need to unrestrict the account temporarily in order to complete the
cancellation of the invoice.

## X14-2 ACCOUNT MAINTENANCE

### How To Run

From the General Ledger Menu (X1-4), select option 2, Account
Maintenance. The "Account #" prompt appears. Type the general ledger
account number you want to add or change. Press [Enter].

Account Index Screen

If you have forgotten the account number you want to modify, you can
view the index by pressing [Cmd8]. Place any character to the left of an
account number to select it.

E & L EQUIP. SALES & RENTALS GENERAL LEDGER ACCOUNT MAINTENANCE x14201-03 3
Division: A Index of G/L Accounts

Account Description Acct #1 Acct #2 Fac

ALO60 ‘MY HOME TOWN BANK

A1100 WHOLE GOODS RECEIVABLES

al110 ACCOUNTS RECEIVABLE

ALLZ0 WARRANTY RECEIVABLE

AL130 CONTRACTS IN TRANSIT

a11g90 DOUBTFUL RECEIVABLES

1200 NEW TRACTORS

al240 NEW EQUIPMENT

a1250 USED TRACTORS & EQUIPMENT

a1260 NEW AUTOS

1270 USED AUTOS

a1273 ‘TRUCKS

a1275 MOTORCYCLES

a1280 RENTAL INVENTORY

1320 PARTS & ACCESSORIES

a1350 ‘TIRES & TUBES

a1420 PREPAID INSURANCE

Position to G/L Account: A1060

Qmdi-Znd Job, Cmi3-Return, Roll-Page

ZEEE REZ ZY Ay

 


 

Zero Balance Account

B & L EQUIP. SALES & RENTALS GENERAL LEDGER ACCOUNT MAINTENANCE x14201-01
Division: A

Account 4; a1060

Title: MY HOME TOWN BANK
Edit Code: B
Account #1
Account #2:

 

Factor: __
‘Type: A
Cash account? (¥}: ¥
Quantity:

 

Delete account: This account has a zero balance and zero history.

You may key "R" to restrict the account in which
case further posting is prohibited but reporting (
features are available; or “D" to completely
General Schedule: delete the account.
Months to keep: 00

cmd3-Return without Save, Enter-Continue

 

d
RELEASE 2.1 QU


Account with Balance

E & L EQUIP. SALES & RENTALS GENERAL LEDGER ACCOUNT MATNTENANCE x14201-01
Division: A

Account #: A1030
Title: FIRST NATIONAL BANK
Edit Code: B
Account #1:
Account #2:
Factor: __
Type: A
Cash account? (¥): ¥

You may key "R" to place the account in a restricted
Restrict account: R state. Further posting is prohibited but account
balances will be reported. Restricted accounts do not
appear on the rolodex; switch GLPRTRES determines
appearance on the chart.
General Schedule:
Months to keep: 6

cma3~Return without Save, Enter-Continue


[«] %14-2. ACCOUNT MAINTENANCE

### Fields & Descriptions

Edit Code

1 character. This is the code that is used to tie the
subsidiary ledger to the particular general ledger. When a
line is posted, an edit code makes sure that all the necessary
information is present for both the general ledger and the
subsidiary ledger. The line is edited for errors.

Some general ledger accounts have edit codes and some do
not. If there is a subsidiary ledger for a general ledger
balance, there will be an edit code. The edit code is the
bridge from the general ledger to the subsidiary. The
subsidiary is a breakdown of information such as:

Account Edit Code Information Required

Receivables A Who owes how much

Units Inventory WwW How much was paid
for what

Trade Payables P How much you owe
to whom

Notes Payable (flooring) F How much you owe
whom on what

employees

Accumulated Depreciation X How much on what
The above are examples of accounts that may need edit
codes. You do not need an edit if there is no subsidiary
ledger. For example, if you have a payable account with a
jump sum and want no detail, do not use an edit code.

In addition, you may use an edit code of “B” for bank
LO


X14-2 ACCOUNT MAINTENANCE [7]

accounts if you want to use the reconciliation feature. See

## CHAPTER X14-6

## , CHECK RECONCILIATION. Or, you

can use a schedule code—see CHAPTERS X14-7 through
X147-5 to learn more about scheduled accounts.

Account 8 characters.

1&2 These fields are filled in with general ledger numbers that
instruct the computer to debit or credit the account
depending on what type of account it is and the edit code
used.

Look at receivables for example. A receivables account has
an A edit code. When posting to an account with an A edit
code, the address number of the person owing the money
will be entered. The general ledger and subsidiary (who)
are posted at the same time. This keeps them in balance.

Also, the A edit code triggers monthly billing to produce
statements. If interest is to be charged, account 1 will hold
the account number of the income account to be credited
with the interest.

Factor 3 digits: Percentage. Type 70% as 070. Percentage
attributed to cost. See explanation below:

When a part is sold at Point of Sale, inventory is
automatically credited and cost of sale is automatically
debited for the cost of the part. This assumes that the parts
inventory account is in the account 1 field and the parts cost
of sales account is the account 2 field.

If a part is not in inventory, there is no way for the


computer to “know” what the cost of the part was. A factor
is the percentage of the sale that should be cost of sales.
The factor is only used if the part is not in inventory.

You can also use a factor for rentals. When a factor of 70 is
used on a rental sales account, inventory will be credited
for 70 percent of the sale and cost of sales will be debited
for 70 percent of the sale. This assumes that the rental
inventory account is in the account 1 field and the rental
cost of sale account is in the account 2 field. See

## CHAPTER X1-4

## , GENERAL LEDGER MENU for

examples of automatic costing and examples of how the
factor works.

1 character. This is a code to identify the type of account
the general ledger will be. The types are defined below:

Asset =
Liability
Sale

Cost of Sale
income
Expense =

 

mAHOMoOP

Every general ledger account with the same type will sort
together in numeric order on the financial statement.

Cash acct?(Y) 1 character.

Quantity

If the general ledger account being added is a cash account
enter Y, If the account is designated as a cash account,
debits and credits are kept track of on a Daily Operating
Control report for review.

This field will only appear on sale accounts for auto


X14-2, ACCOUNT MAINTENANCE [>]

dealers. It indicates the number of invoices posted to the
account for the current month. The system will increment
this field every time a sale is posted. See the Sales
Transactions Counters section below for more information.

The next field varies depending on the status of the account:

Restrict Account Account has a balance. Place an “R” in this field to
restrict the account from further posting.

Abandon Restriction Account is currently restricted. Place an “R” in this
field to make the account eligible for posting.

Delete Account The account has a zero balance and no history. You
may choose to restrict it to keep reporting features,
but it is safe to delete the account. Type “R” to
restrict, “D” to delete.

General Schedule

Months to Keep 2 digits. Saves transaction detail for the specified
number of months (maximum=24). Normally,
transaction detail is removed from the DIS Business
System when a general ledger month is closed;
otherwise, disk space would be a real problem. If
you use General Schedule (X14-7), you may want
to keep transaction detail on selected accounts for
several months.

To Cancel accti 1 character (Y or blank). New or no balance
accounts only. If you want to cancel the account,
enter Y in the "To Cancel acct# enter ¥ field. This
option will only be available if there is no balance
in the account.


[| X14-2 ACCOUNT MAINTENANCE

### System Editing

The general ledger is tied to the subledgers by edit codes. Edit codes may
require the Account 1 and 2 fields to be filled in with other general ledger
account numbers. For example, a W edit code is used for units inventory.
With a W edit code, you are required to type in an account 2, cost of sale.
The Account 1 field should be filled in with the sale account. For either
field to be filled in with an account number, the general ledger account
must be opened.

The procedure is:

O) Open the units inventory account. Do not enter the account 1 or account
2. The accounts are not yet open. Do not enter the edit code, you will be
required to enter an account 2. Fill in all other information and press
Enter. {

O Open the unit sales account. Enter the account 1, unit inventory. Do not

enter the account 2, cost of sale. It is not open yet. Do not enter the S

edit code. You will be required to enter an account 1 and 2. Account 2

is not yet open. Fill in all other information and press Enter.

Open the unit cost of sales account. You may fill in all the required

information. The edit code is W, which will require an inventory

account in the account | field. The inventory account is open. Press

Enter.

O Bring the unit inventory and sale accounts back up and fill in the edit
codes and account 1 and 2 fields. Press Enter.

 

 

 

 

### Warning!

Don't forget to go back and add edit codes to the account numbers.
Your system will not work correctly without them,

 

RELEASE 2.1 Lo


X14-2 ACCOUNT MAINTENANCE [*]

### Sales Transactions Counters

Sales Transactions Counters are a feature designed expressly for former
ADMS Dealers. The ADMS system maintained on-going counts of
invoices posted to various ledger sales accounts. When ADMS dealers
convert to DIS/400, DIS stores up to 24 months of these counts in the file
u.GLC.

In the DIS system, counts are accumulated from POS batches (X55-2) and
from Create Source Documents (X1-7). Transactions are counted for sales
accounts only; furthermore, transactions are counted by invoice, regardless
of amount, positive or negative. In other words, each time a document
includes a credit or debit to a sales account, the counter for the account is
increased by one. No attempt is made to ascertain how many or which
parts may be represented by the transactions or whether it is a sale or a
return.

The counter is available for sales accounts only through Account
Maintenance (X14-2) where it can only be changed for the current month.
It may be necessary to change the counter from time-to-time since no
distinction is made between sales and returns, both of which cause the
counter to go up by one. The system stores counts for each sales account
for 24 months. The oldest month is purged when Accounting End of
Month runs.


[| X14-2 ACCOUNT MAINTENANCE ces

Preparation

To take advantage of the sales transaction counters, the following
conditions must exist:

© The dealer must be an automobile dealer: the PRODINSTL, OPT
switch must be on. At any menu, type: K00081 PRODINST, 1
[Enter].

= The file u.GLC (u-User ID associated with the dealer's files) must exist.
To create u.GLC, run Initial File Setup (X6-7).

O To change "Quantity" simply type the amount and press [Field Exit].

## CHAPTER X14-3

CHART OF ACCOUNTS

### Introduction

The Chart of Accounts lists your general ledger accounts in order by
account number. As new accounts are added, run a copy of the new chart
and keep it handy for quick reference during posting.

At the end of the chart of accounts, you'll find a summary of formatting for
the Financial Statement, which indicates totaling levels as set up in

Financial Statement Format Maintenance (X68-5). For more information,
see CHAPTER X68-5).

### How To Run

From the General Ledger Menu (X1-4), select option 3, Chart of
Accounts. The following security gate is presented:

x0001~001

Enter Division Code . . .

Print all divisions (¥/N) . . .

 

Enter the division code. If you want a chart on the division only, enter
N(No). Y(Yes) is the default. If you leave the Y, all the charts of
accounts for all divisions will print. Press Enter. The chart is printed. An
example follows.

## X14-3 CHART OF ACCOUNTS

   

ABC COMPANY CHART OF ACCOUNTS Date 5/14/92 Paget

BELLINGHAM, WA u Time 10.52.39 x3430-10,

acer Title Edit Debic account Account Factor Type. Title code
cote Code et ”

zea ASH ON HAKD

1102 (CASH IN BANK - PSH

1103 CANCELED DoctxmNTS

Los PETTY CASH - CHANGE FUND

L104 PETTY CASH - TRAVEL aAGs

uit ACCOUNTS. RECETVAILE

Linz TOTAL RENTAL LEASE

Ln ISK, MASTER CHARGE, COD

Laie WH WARRANTY

L120 FORD TRACTORS & EQUIPMENT

Liza MASSEY FERGUSON TRACTORS

123 NON-FORD EQUIPMENT

waza NEW HOLLAND

Laizs USED TRACTORS & ZQULPMENT

a7 ‘BOFORD

132 PARTS & ACCESSORIES

1136 REBUILT ENGINES

240 SUSPENSE,

naa PREPAID - OTHER

nasa SHOP EQUIPMENT

Liss ACCUM, DEER. - sHOP sQUZ:

Las PURNITURE & PIXTURES.

Las? ACCUM. DER. - FURNITURE

Lise CARS, TRUCKS & TRAILERS

nase ACCUM, DEPR.-CARS, TRUCKS

160 URASEROLD IMPROVEMENTS

n62 ACCUM DEPR.-LEASEHOLD IMP

362 RENTAL EQUIPMENT

63 ACCUM. DEPR.-RENTAL EQUIP

bi70a PIMANCE RESERVE - NH

1220 NOTES PAYABLE - FORD

12208 NOTES PAYABLE - LEASES

221 NOTES PAYABLE-0F

1223 NOTES PAYABLE - OTHER

na24 FLOORING-NEW HOLCAND

1238 NOTES PAYABLE - PSE

238m, NOTES PAYABLE - CONTRACTS

1239 EMPLOYEE SAVINGS ACCOUNTS

L240 PAYABLES



1262 ACCRUED BONUS

1262a, ACCRUED BONUS DEDUCTION

1263 ACCRUED FICA

La6a ACCRUED WITHHOLDING-PED.

1267 ACCRUED UNEMPLOYMENT-PED.

SER 4 2a >0 >>

 

=

ARE ERR ERE ER
PRP RE ROR ROE ee >

 

RELEASE 2.1 LL


 

ABC Company CHART OF ACCOUNTS pate 5/14/92 Pege 2

ELLINGHAM, WA L Time 10.52.39 1430-18

acct € title dit Debit Account Account F Title code
code code 2

26a ACCRUED CHEMPLOYMENT-STAT

L269 ACCRUED MED ATD-7ND TNS

L270 ACCRUED SALES TAX

270A, SALES TAX - LEASE

1276 MEDICAL INSURANCE

2308, NOTE - PSB REAL ESTATE

L230 CAPITAL STOCK

Last ‘TREASURY STOCK

1292 RETAINED EARNINGS

1233 CAPITAL SURPLUS

L320 FORD TRACTORS & EQUIPMENT

aan MBSS2Y FERGUSON TRACTORS

1322 PARTS CLEARING ACCT

1223 NON-FORD EQUIPMENT

1224 NEW HOLLAND

1325 USED TRACTORS & EQUIPMENT

4327 BOMPORD

u328 RENTAL EQUIPMENT REVENUE

1329 RENTAL EQUIPMENT SALES

1332 PARTS - INTERNAL

1332 PARTS - COUNTER RETAIL

1333 PARTS - SHOP RETAIL

1336 REBUILT ENGINES

4337 CUSTOMER LABOR-OTHER

L307F CUSTOMER LABOR-FORD

1334 CUSTOMER LABOR-ME

1337 CUSTOMER LABOR-NH

1338 SERVICE LABOR - INTSRKAL

1345 DATA SERVICES

Lass VEHICLE MANAGEMENT

nye eee ee bane
DMMB HOHaHnnHoheanonrooeeeneee

 


   

AEC COMPANY CARRT OF ACCOUNTS Dare 5/14/92 Penge 3

BELLINGHAM, WA ‘Time 10.52.39 2439-14,

acct # Edit Debit Account Accounts Factor Type. Ticle cede
code Code 2 a

FORD TRACTORS & EQUIPHENT ize
MASSEY FERGUSON TRACTORS Lizt
NON-FORD EQUIPMENT 1123
NEW HOLLAND ize
USED TRACTORS & EQUIPUENT L125
BOMFORD Lz?
RENTAL EQUIPMENT REVENUE

RENTAL EQUIPMENT SALES 162
PARTS - INTERNAL

PARTS - COUNTER RETAIL

PAR?S - SHOP RETAIL

REBUILT ENGINES

CUSTOMER LABOR-oTHeR

CUSTOMER LABOR-FORD

CUSTOMER LABOR-MF

CUSTOMER LAEOR-NA

SERVICE LABOR - INTERNAL

DATA SERVICES

VEEICLE MANAGEMENT

DISCOUNTS EARNED

OTHER INCOME

INTEREST INCOME

GAIN/LOSS ~ FIXED ASSETS

DISCOUNTS GIVEN

ADVERTISING

SRLES PROMOTION

WARRANTY — NEW

SHOP LABOR REWORK

BABCR-ROB & REBUILD PARTS

SHOP TIME-MECHANICS

SHOP TIME-SHOP MANAGERS:

COMPENSATION - SALESMEN

COMPENSATION - MANAGER

COMPENSATION - OFFICE

‘COVERALLS

COMPENSATION - FARTSHEN

EMPLOYER TAXES

EMPLOYEE MEDICAL

FREIGHT

TOOLS & SHOP SUPPLIES

EQUIPMENT RENTAL

BUILDING LEASE

BUILDING MAINTENANCE

TEUEPHONE ~ TELEGRAPH

UTILITIES

EQUIPMENT DEPRECIATION

 

IMME MH HOR ANnAeHANnAMAAoBAAAHO

Rm mm

 

 

RELEASE 2.1 LL


ABC COMPANY
BELLINGHAM, WA L

Rect #

L674
1675
675A,
1676
1630
682
2682
3683
16838
1683¢
684
1685
uses
687
688
629
1690
691
698
1699

ritle

EQUIPMENT REPAIR
\VERICLE EXPENSE - GAS
VEHICLE 2XPENSE - DIESEL
INSURANCE

INTEREST - FLOORING
INTEREST - OTHER
PRAINING.

TAXES & LICENSES

TAXES - STATE EXCISE
TAXES - PERSONAL PROPERTY
OFFICE SUPPLIES & POSTAGE
TRAVEL & ENTERTAINMENT
AUDIT, LEGAL & COLLECTION
‘BAD DEBTS

DUBS & SUBSCRIPTIONS
contataorr0Ns

DATA PROCESSING

DATA PROCESSING SUPPLIES
MONETARY EXCHANGE
MISCELLANEOUS

CHART OF AccomInS:

Fait Debit Account Account Factor
code code

®
P
P
P
Pp
Pe
2
Pe
P
Pe
Pe
P
eB
Pe
Pe
P
P
Pe
Pe

P
1044
19
136
136
19
155,
357
189
152,
263
180
180
239
246
276
26
280K
238
327
328
333
339,
239
360
539
639

n
sat

 

TOTAL CASH trererrreese
TOTAL RECEIVABLES ****+
TOTAL INVENTORIES **+7"
CURRENT ASSETS *tss40+5
PREPAID EXPENSE tessere

FIXED ASSETS tees"
OTHER ASSETS treeresers
TOTAL ASSETS reteeseees
NOTES PAYABLE *#++seees
ACCOUNTS PAYABLE teeee*
ACCRUED LIABILITIES ***
CURRENT LIABILITIES ***
LONG TERM LIABILITY *#*
NET WORTH <*+erssrenenn
TOTAL NEW & USED vere
TOTAL RENTALS *#+terre
TOTAL PARTS ***+e*:

TOTAL SERVICE seeeees®
TOTAL MISC SERVICES **
GRAND TOTAL SALES +++
NED OTHER INCOME +1
TOTAL EXPENSES t#+ee+*

  

 

 


 

pate $/14/32 Page «
Time 10.52.39 x14a0-1a
‘Type ticle code

 

HUAN NANO

 

ee ee ee ee


Bais
code

CHART OF accouNTS

Debit Account account
code aa n

Factor

Type

Date 5/24/92 Page 5
‘Time 10.52.39 x1a20-2a,
Title code

5S 1 OPERATING PROFIT ++

6 °* OTHER INCOME seeeeee 1
‘7+ NET PROFIT BEFORE TAX 1
@ PROFIT OR LOSS CURRENT YR 3
9 * TOTAL LIA a NET WORTH ¢

 

## CHAPTER X14-4

MONTHLY GENERAL LEDGER REPORT

### Introduction

The Monthly General Ledger Report is a listing of all debit and credit
transactions posted to all general ledger accounts. It runs automatically
when a month is closed; however, you can use this job to run the report at
other times. You can request the report for all open months or restrict it to
the oldest open month only.

If you wish to run a report on an individual general ledger account, go to
Account Inquiry (X14- 1), You may choose to run this report before
closing the month to make sure that all the required transactions for the
month are posted. Once a month is closed, you can not post to that month.
Tf you do, you will be posting to future month. For example, if June 1986
is closed and you post to June, the transactions will be posted into June
1987.

## X14-4 MONTHLY GENERAL LEDGER REPORT

 

### How To Run

From the General Ledger Menu (X1-4), select option 4 for the Monthly
General Ledger Report. A selection screen follows the security gate.

 

AUSTIN'S EQUIPMENT CO. MONTHLY GENERAL LEDGER REPORT 1440-001

Division: A Report Options

Month Selection:

i, Include all open months
2. Only include the eldest open month

Enter option: 1

mdi-End job Enter-Continue

 


An example of the Monthly General Ledger Report follows.

GENERAL LEDGER REGISTER Date 7/10/86 page 3
1410-20,
P
oun
750.00
2280.00

pec
-00 . : : 00

-00 : : -00

2250.00

J 07 cKesa2s 7707/96 su RENT >
OPEN MONTHS TOTAL : 750.00

3000.00,

 

The account number and name of the account print at the top of the report.

Twelve months of history are provided on the report. The most recent
closed month is listed first and the oldest closed month is listed last. You
are provided with the total of all debits and credits to the account for that
month in the "Month" field. The "Year to Date" field contains the year to
date total balance at the time the month was closed.

The BEGINNING BALANCE field will contain the year to date total
balance of the month most recently closed.


 

All debits and credits will be listed for each open month. The transactions
will be separated by posting month.

The transaction from the above example reads:
J 07 CK#3426 7/07/86 JULYRENT D_ 750.00

J: What was entered in the ID field at Create Source
Documents (X1-7).

07: Equals the posting month from Create Source Documents
(X1-7).
CK#3426: What was entered in the Document field at Create Source
Documents (X1-7). {
T107/86: Posting date from Create Source Documents (X1-7).

JULY RENT: Information from the Description field at Create Source
Documents (X1-7).

D: Debit or credit code from Create Source Documents.

750.00: Amount of the debit transaction. The credit transactions
will be listed on the right side of the column. Both columns
will be subtotaled by open month.

You will view other numbers your recognize. If you entered something in
a field at Create Source Documents, the information will appear on the
General Ledger Register. If a stock number was entered, the stock number
will appear on the transaction line.

RELEASE 2.1 CO


 

At the bottom of the General Ledger Register is a debit and credit total for
all open months. The BEGINNING BALANCE plus the OPEN MONTHS
TOTAL equals YEAR TO DATE.


Notes:

f
RELEASE 2.1 Ue

## CHAPTER X14-5

SUBLEDGER BALANCE REPORT

### Introduction

The Subledger Balance Report prints a list of General Ledger accounts
that have edit codes of A (Receivables), F Flooring), P (Payables), and W
(Units). Asset and liability accounts that have schedule edit codes are also
included.

The report shows the balance in the General Ledger account and compares
it with the sum of the subledger balances. This report saves you the time of
running the individual subledger reports, such as the Aged Receivables
Report, and comparing them to the General Ledger. The difference, which
should be zero, is reported. If there are discrepancies, you should clear
them up as soon as possible.

An option is available in the DIS OPT Library to print this report at
Accounting End of Day.

### How To Run

From the General Ledger Menu (X1-4), select option 5, Subledger Balance
Report. Following the Accounting security gate, the report is placed on the
job queue.


X14-5 SUBLEDGER BALANCE REPORT a

 

An example of a Subledger Balance Report follows:

hem xouteMmrT ses subledger satance Repore uae: 4/21/92 Page +
Division £ tine: 14:58:05 x1es0-24
Accoutt ite enecet Ledges subledser Yariasion

Lint AccouNESs RECEWVASLE Maiaase 262,123.53

saa gona RENT. LENSE e300. 8, 300.72-

23s Vash, JOETER CHARGE, CoD mai.as aaiias

eke Re wR pases 23,315.95

310° FORD TRACTORS & BXUIPAT sanisea ss 393,562059

ti21—_wassEy FERGUSON THACTORS ema 6 7en.et

12a Nov-ronp squImanT saaunss 93,131.98

hea Naw #otaN as.oo0.a1 246,372.22 2027.33

2225 UseD TRACTORS BOUIPAENT joviaes a) 207,404.99 16.56-

tay BowonD nimi. 11,722.98

nie RERUILT ExrmEs “eo

re. RENTAL SQUID? “oo

i220 Novas pavanie + FORD wana 328,457.42

20s NovEE PAYABLE ~ LineaE “eo “oe

Gani Norey mavnnuesur seesoles 8.480088

Liza oonaha-w NOEL 136,495.65 236,222.45 ar.20

tac payanies ws.7st28 78,754.28 {
ean Betmis :2,029/626.77 —2,027,468.14 nase:

 

 

RELEASE 2.1 LO

## CHAPTER X14-6

CHECK RECONCILIATION

### Introduction

Use this job to reconcile your bank statement with the balance of one or
more general ledger accounts. Only transactions associated with an
account with a "B" edit code are available.

If you are adding the "B" edit code to an existing account, you can add
uncleared transactions using the B=GL Bypass feature, which creates
transactions for later reconciliation but does not post to the general ledger.


[| X14-6 CHECK RECONCILIATION co

### How To Run

From the General Ledger Menu (X1-4), select option 6, Check
Reconciliation. The Select Bank Account Screen is displayed.

Select Bank Account Screen

A & R EQUIPMENT SALES, INC. CHECK RECONCILIATION 1460-201
Division A Select Bank Account

lsSelect 8=GL Bypass
Account# Title

NORTASTATE BANK
CASH IN BANK

Cmil-End job Roll-Page

 

The options on this screen are:
1=Select Used to reconcile transactions and post interest and service

RELEASE 2.1 LO

## X14-6 CHECK RECONCILIATION

charges, if any. However, the system will prevent automatic
posting of service and interest charges to restricted
accounts.

B=GL Bypass Used on a new bank account to enter uncleared transactions
without posting to the general ledger. Screen flow is the
same as 1=Select. In particular, see ADD
TRANSACTIONS on page 6.

1=Select
O Select a bank account by typing | beside it, and press [Enter]. The
Reconcile Register Screen appears, as illustrated below.

A & R EQUICMENT SALES, INC. CHECK RECONCILIATION x1460-301
Division A Reconcile Register

Account: A1030
CASH IN BANK

Bank Statement Opening Balance: 678206
Bank Statement Ending Balance : 128878

Transaction ID.:
Service Charge. : Offset Account:
Interest Earned: Offset Account: A2770

Cmdl-En@ job Cmd2-Add Trans Cmé3-Select Account Enter-Verity


[«| X14-6 CHECK RECONCILIATION co

Type the opening balance on your statement, and press [Field Exit].
Type the ending balance on your statement, and press [Field Exit].
Fill in a transaction ID. Press [Tab] or [Field Exit].

If there was a service charge or interest during the month, type them at
the appropriate prompt, and press [Field Exit]. Type the account
number you want to use for the offsetting entry. When you press
[Enter], a verification screen is displayed.

© To return to the Reconcile Register Screen, press [Cmd3]; otherwise,
press [Enter]. The service charge and interest, if any, are posted. The
following message is displayed: "Posting Transactions to General
Ledger."

goog

After the transactions have been posted, the Reconcile Register Screen
displays the list of transactions that have not been reconciled for the
selected bank account. An illustration follows: (

f
RELEASE 2.1 \


a
a
a
a


4 & R EQUIPMENT SALES, INC. CHECK RECONCILIATION ‘*1460-501
Division A Reconcile Register
Account: A1030 Cleared Balance: 4688.39
CASH IN BANX Bank Ending Balance: 1288.78
Difference: 3399.61
Clear Checkf Payment Amt Deposit Amt Date Description

1isios9a

10/25/94 Al TRANSMISSION SERVICE
2380 : 10/25/94 COTES ABRASIVES
2381 : 10/25/94 CURRY TOWING CO
2382 - 40/25/54 CASE IK
2383 : 10/25/94 MOTOR WELD INC
2384 : 10/25/94 NEW HOLLAND
2385 : 10/25/94 RAINDANCE ROOFCARE & PAIN
2386 : 10/25/94 REALTY WORLD ACTION PLUS
2387 : 10/25/94 SULLIVAN PLUMBING & HEATT
2388 : 10/25/94 WESTERN SUPPLY CO
2389 : 10/25/94 WILLIAMS STATIONERY STORE
98-03445 18009.43 11/10/94 SATURDAY

Qmdi-End job Cmd2-Add Trans Cmd3-Adj Bank Bal Cmd5-Reports Cmd12-Done

Place a character beside each item that has cleared.

Press [Enter] to recalculate the Difference.

To add transactions, press Cmd2-Add Trans. See Add Transactions.
To adjust the bank balance press [Cmd3]. See Adjust Bank Balance.
To print reports, press Cmd6-Reports. See Reports.

If you have finished reconciliation, press [Cmd12]-Done. The Print
Reports window appears. See Reports.


[<| X14-6 CHECK RECONCILIATION co

ADD TRANSACTIONS

0 If you need to add transactions that have not yet been posted, press
Cmd2-Add Trans. If you began with 1=Select, these transactions will
be posted. If, however, you began with B=GL Bypass, they will not be
posted but will be available for reconciliation later.

A & R EQUIPMENT SALES, INC. CHECK RECONCILIATION x1460-401
Add Transactions
Account: A1030
CASH IN BANK G/L Month.: 11

ID Date Check# Payment Amt Deposit Amt Description Offset Acct

111094

Last Added Transaction:
Ez 111094 = 98-03445 18009.43 SATURDAY 1000

Cmdl~End Job Cmd3-Return Cmd12-Post Added Trans Enter-verify

 

O To post the added transaction(s), press [Enter]. A verification screen is
displayed.

0 If the transactions are satisfactory, press [Enter] to confirm. The
transactions are posted. The following message is displayed: “Posting

(.


X14-6 CHECK RECONCILIATION 7 |

Transactions to General Ledger." You return to the list of transactions.
The list of transactions will be redisplayed, the new one will be
included, and the difference recalculated.

### Adjust Bank Balance

To adjust the bank balance, press Cmd3-Adj Bank Bal. The Reconcile
Register Screen, as illustrated earlier, is displayed.

A & R EQUIPMENT SALES, INC. CHECK RECONCILIATION x1460-301
Division a Reconcile Register

Account: AL030
CASA IN BANK

Bank Statement Opening Balance: 678206
Bank Statement Ending Balance = 428878

G/L Month

Transaction 1D.:
Service Charge.: Offset Account:
Interest Earned: Offset Account:

Cmdi-End job Cnd2-add Trans ¢md3-select Account  Enter-Verify

 


 

### Reports

Although the Reconciliation Reports are printed automatically when you
press Cmd12-Done, they can be printed at any time by pressing
Cmd6-Reports. The Print Reports Screen allows you to select the
Reconciliation Report, the Check Register Report, and whether you want
transactions in order by date or by check number. The selection screen is
illustrated below.

RELEASE 2.1 LO


Print Reports Screen

A & R EQUIPMENT SALES, INC. CHECK RECONCILIATION 1460-502
Division A print Reports

Account; 1030
CASH IN BANK

Reconciliation Summary Report: ¥

Check Register Report ...
Sort Order for Printing .

1+ Sort by Date
2 - Sort by Check#

Cmdl-End Jos Cmd3-Return  Enter-Continue


10 | X14-6 CHECK RECONCILIATION

Reconciliation Complete

When the process is complete, the following screen is displayed:

A & R EQUIPMENT SALES, INC. CHECK RECONCILIATION x1460-504
Division a Reconcile Register

Account: A1020
CASH IN BANK

Cleared Balance: 4288.74

Bank Ending Balance: 4288.74
Difference: 00

Reconciliation is complete. (

Cleared transactions have been removed from the check register.

Enter-Continue

 

RELEASE 2.1 LO


X%14-6 CHECK RECONCILIATION

Reconciliation Summary Report

An example of a Reconciliation Summary Report is shown below:

A & R RQUIPHENT SALES, INC. Reconciliation Summary Report s1nsios9@ Page sk
Division & PISES25  XLAGO-6A
Account: 42630

CASH IN SANK
Bank Stetenenc Opening Balance: 6,782.06
Cleared Checks end Paynents: 22 Irems

Cleared Deposits and cher Payments:

Cleared Balance: 4,288.74
Uncleared Checks and Payments: 90
Uncleared Deposics and Other Paymence: 09

Register Balance: 4,288.74

 


oof,

Check Register Report

An example of a Check Register Report, sorted by date, is shown below.

A R pgurmenr sates, ono ace | 11/18/94 age :
Division 8 Tine | 15:89:28 xt4son6s
Account: 42020
casi oH BAN
pate checks
Geevine anuance :
worsise 2079 AL TRANENEISSION stxvicE . la3s.a9,
yoas/ss 2389 comes agtastves : lass 74
10/25/98 2381 cuaRY TeHtNs 9
erasise 2383 GASE 3H : sloetss-
wrasse 2383 WOTER WELD 2H sisia.es-
10/28/96 2344 et HOLLAND : wel3an.se
10/25/96 3388 AINDANCE KODECARE & PAIS : hs20 aie
0125/9238 BEAUTY WoRLD aCrreH outs : 12 1968.32-
woras9e 338 SULLIVAS PLUNBING 4 aT: anlzei.as-
or2sioe 2388 wesvER® suPeLY co 13301. 10- {
oras/oe 3388 wELLIAMS STATIONERY STORE wasss:
Liners xt BARKED veut raat.
nanovs4 2390 evosi 14,120.42
ui/ig/e4$80-223 REN? nCVD na9.65 13320089.
nina/e4 98ee34as ——saTunaKe saess)— a.2ae.re

 

 

RELEASE 2.1 Lu

## CHAPTER X14-7

SCHEDULES MENU

### Introduction

Scheduling allows you to track individual postings to some accounts for a
longer period of time than the system normally allows. There are three
types of scheduling in the DIS system: general schedules, unit schedules,
and account schedules.

The Schedule Menu contains the following options:

X147-1 General Schedule
A General Schedule can be printed for up to 7 General Ledger
accounts. You can specify the sort order you prefer, and a date range
for the report. Only transactions for open months are available;
however, General Ledger Maintenance (X14-2) allows you to specify a
number of "Months to Keep" if you need to print general schedules
pertaining to closed G/L months.

X147-2 Unit Schedule
The Unit Schedule summarizes transactions for sold units from General
Ledger accounts related specifically to units: Units Inventory, Units
Cost of Sale, and Flooring accounts ("W" and "F" edit codes). The
schedule may include up to 7 different accounts for a particular
month/year.

147-3 Scheduled Account Reporting
Scheduled Account Reporting allows you to record transactions posted
to accounts marked with aN, U, T, V or L edit code. Transactions are
recorded after the edit code has been entered. See the section below for
more information about scheduled accounts.

147-4 Scheduled Account Purge
Scheduled Account Purge allows you to purge debit and credit
transactions associated with a scheduled account and write off amounts
that are not within the range specified by the user. This job then creates
the offsetting entry to a write-off account.


[2] X14-7 SCHEDULES OVERVIEW c

X147-5 Scheduled Account Inquiry
Scheduled Account Inquiry allows you to examine individual
transactions posted to a scheduled account.

### Using Scheduled Accounts In Reports

The primary use for scheduled accounts is generating reports. To make a
scheduled account, go into Account Maintenance (X14-2) and add one of
the following edit codes to an account with no edit code.

N Schedule by Address#

U Schedule by Unit#

T Schedule by Description (
Vv Schedule by VIN#

L Schedule by DOC#

Do not replace an edit code of an existing account with one of the above
codes!

Once one of these codes has been added to an account, all of the
transactions posted to that account are saved and can be viewed in queries
or used for generating reports. In addition, all transactions posted to that
account require the completion of one additional field (Address#, Uniti,
Description, VIN#, or DOC#) depending on that account's edit code.

Scheduled Account Reporting (X147-3) will generate reports that sort
selected accounts according to they way they are scheduled. For example,
an account scheduled by Address# will sort all of the transactions by
Address#, grouping all transactions that share a common address together.

i
RELEASE 2.1 Ne

### X14-7 Schedules Overview [2]

These reports could be used in a wide variety of ways. For example, a
warranty receivable account scheduled by Document# would generate
reports that would allow you to easily match the debit and credit amounts
for each unit. A leasing account scheduled by Unit# would allow you to
generate a report that would group the payments you have received for
each unit together.

For the purposes of report generating, scheduling can be used in any
number of ways. The general procedure would be: if you have an account
that you want to track closely and that does ot have an edit code, decide
how you would want it organized in a report (by Address#, Unit#, etc.)
and add the appropriate edit code to the account. If none of the other
fields would work, you could always schedule by description and
construct your own record-sorting scheme using that field.

Purging Scheduled Accounts

As more and more transactions are added to the schedules you use, you
may find it necessary to clean them up from time to time. There are two
ways of doing this:

First, an option exists for purging zero balances in Scheduled Account
Reporting (X147-3). If this option is chosen, all groups of transactions
associated with a particular Address#, Unit#, Description, VIN#, or DOC#
(depending on the edit code you used) that have a zero balance will be
deleted from the schedule. As this job purges debit and credit transactions
that are equal to one another, it is good for merging invoices and
payments. These change only affects scheduling, it does not interfere with
the rest of the system.


[+] X14-7 SCHEDULES OVERVIEW vo
{

Second, in Scheduled Account Purge (X147-4), there is the option for
purging transactions that have a balance between zero and a value you
specify. The purged transactions are moved to another account. Purged
transactions can be viewed in Scheduled Account Inquiry (X147-5).

RELEASE 2.1 \O

## CHAPTER X15-1

SALES ANALYSIS REPORT

### Introduction

The Sales Analysis Report provides sales and profit analyses and a quick
cash flow assessment.

= Totals and profit margins for each sales account for the month
selected:
-  Month-to-date
- Year-to-date
- Same month last year
- Year-to-date for last year

= Summary of aged receivables and payables.
= Income and expense account detail or summary only.

### How To Run

From the Financial Report Menu (X15-1), select option 1, Sales Analysis
Report. The following security gate is presented:

x0001-001 1

Enter Division Code
Print all divisions (y/M)

 

Enter Security Code

 

OU Enter the Division Code.

O Type a ¥ (Yes) if you want to print all divisions, or type a N (No) if you
do not.

O Type the Financial Security Code.


[| X15-1 SALES ANALYSIS REPORT yo
(

O Press Enter. The selection screen appears.

BRIGHAM IMPLEMENT Co. Sales Analysis Report x1510-001
Division: *

Print detail income and expense accounts? (¥/N)
Would you like this report for a past closed month? (Y/N) .
If closed month selected, enter desired month (1-12)

Cmdi-End job Cmd2-Select by Department

 

For a Sales Analysis Report with a summary of income and expense
accounts (no detail) type N. For detail listing of every income and expense
account, type Y (Yes). If you want totals from a past closed month instead
of open months, enter Y on the second line. Then enter the month you
want on the third line. The month selected will print at the top of the
report.

The report can be selected by department. Press [Cmd2] to use the

Department Selection screen (same as Financial Statement) as illustrated
below .

RELEASE 2.2 tO

## X15-1 SALES ANALYSIS REPORT

BRIGHAM IMPLEMENT CO. Financial Statement x1519-002
Division: * Department Selection

Department selection mask: XxXXXHX

To select ali departments and print all accounts, the mask must be all ‘x’.
To select all departments and summarize on a major portion of the account
number, enter a '*' in the mask where the minor (department) portion of the

account numbers begin

To select a specific department, enter the character(s) that identify that

department. Be sure to place them in the mask exactly where they appear in
the account numbers.

Examples:
Assume general ledger accounts ALO0A and A100B which represent cash accounts
for departments ‘A‘ and ‘B' respectively.

All accounts AXXXXKKRX

Summarized ORR

Specific department SKA

Cmdé-return to Month Selection screen

 

Press [Cmd6] to return to the Month Selection screen.
From the Sales Analysis screen, press [Enter].
The Sales Analysis Report will be placed on the job queue.

The fields on the Sales Analysis Report are defined below.


[+] X15-1 SALES ANALYSIS REPORT

 

Note:

Header Lines contain Division information or * for all Divisions.

B= Sales _-
Sales

Cost

Subtotals on Sales Accounts correspond to Financial Statement format.

### Current Year

MONTH Sales posted for the current month through report
date.
YEAR TO DATE Sales posted for the current year through report
date.
LAST YEAR
MONTH Total sales for the entire month last year.
YEAR TODATE Total year-to-date through end of the same month
last year.
RECEIVABLES
TITLE Description of the Receivables account.
ACCOUNT Receivables account number.
BALANCE Current total balance due.
CURRENT Current balance, including service charge.
30 DAYS Amount 30 days past due.
60 DAYS Amount 60 days past due.

90 DAYS & OVER Amount 90 days and over past due.
Lu


X15-1 SALES ANALYSIS REPORT [=]

PAYABLES
TITLE Description of the Payables account.
ACCOUNT Payables account number.
TOTAL DUE Total balance owed on account.
DUE TODAY Balance owed as of report date.
10 DAYS Balance owed in 10 days.
30 DAYS Balance owed in 30 days.

FUTURE Balance owed in over 30 days.

Note:

     

Choice of detail gives information on each income and expense
account.

Choice of summary only gives total balance posted to all income
| accounts and all expense accounts as of report date.

INCOME

TITLE Description of Income account.

ACCOUNT Income account number.

BALANCE Balance posted to the account through report date.

EXPENSES

TITLE Description of Expense account.

ACCOUNT Expense account number.

BALANCE Balance posted to the account through report date.


BELLINGHAW CAR & TRUCK CO.
BELLINGHAM, WA a
current Year 32/29/87
Month , Year to pace & Tele
35,618.00 100.09 143,271.00 24.73 NEW TRACTORS
8,214.00 62.56 12,464.00 73,55 NeW EQUIEHENT
1,200.00 16.86 1,209.09 16.66 USED TRACTORS-ECUIP
9,990.90 100.00 NEw AUTGS
USED auToS
‘TRUCKS
MOTORCYCLES

Sales analysis

45,632.09 90.59

22,995.00 39.22 RENTAL EQUIP SALES

Report,

Account, Month y
aaz06

Date 12/28/97 Page 3
‘Pima 19.23.08 1510-20

Last Year

Year to Dare 8

201.111.22 100.00 213,484.67 100.00

agzan

3250
3260
2270
a2273
ag27s

466,905.05 41.40 **T0TAL NEW & USED SALES"
665.20 60.90 RENTAL EQUI? REVENUE

204,121.22 100.99 213,484.67 190.00

al2e6

A290

39.660.20 39.85 **TOTAL RENTALS SALESY+++

PARTS-HHOLESALE 30a
363.22 PARTS-INTERNAL
54,613.39 43,57 PARTS-COUNTER
89.38 50.87 PAATS-SHOP
55,266.39 43.14 *TOTAG PARTS SALES*®
3,425.00 25.02. TIRES AND TUBES
1,901.26 100.00 MISC SALES

54,613.00 84.10 SERVICE LABOR-CUSTOMER
69.63 200.00 SERVICE LABOR- INTERNAL

SUBLET REPAIRS
$9,128.83 80.87 **TOTAL SERVICE SALES~
FREIGHT SALES

BELLINGHAM CAR & TRUCK CO,
BELLINGHAM, WA a

Sales Anelysis

Receivables

alae

300.00 234,58 100.90

3320

2330

234.55 100.00

an3s0

53360
83370
53380
43390

Asano

Report

Title aceount, Balance Corcent

ACCOUNTS RECEIVABLE atiia

WARRANTY RECEIVABLE aii20

CONTRACTS IN TRANSIT AL130
otal 36,865.17

BELLINGHAM CAR & TRUCK CO.

BEULINGHAM, WA a

36,865.17 22,031.29

22,031.29
Sales analysis

Payables
Due Today
99,070.59

Title account, Total pue
NOTES PAYABLE-FORD 2200 103, 584.59)
NOTES PAYABLE-NEW HOLLAND 42210 6,871.70
NOTES PAYABLE-CASE 2260 25,236,00 16,226.00
PAYABLES 22406 12,352.53 32,352.53
COSTOMER DEPOSITS a2aig 56.09

‘Total 139,874.82 128,639.12

Report,

 

Dace 12/29/97 Fage 2
Time 10.23.06 2510-20

39 Days 60 Days
9,462.28 2,371.60 3,000.09,

90 Days & over

9,462.28 2,372.60 3.009.090
Date 12/29/97 Page 3
‘Pime 10.2305 1519-28

Future
4,514.00
6,674.70

50.00
21,235.70

See the next page for a sample Sales Analysis Report.

RELEASE 2.2 LO


BELLINGHAM CAR & TRUCK CO. Sales analysis Repore sace 12/29/97 Page 4
BELLINGHAM. WA a Tine 10.23.06 1520-28
current vear

Meath Year to dace
352.47
96,669.99

  


Notes:

RELEASE 2.2 ow

## CHAPTER X15-2

FINANCIAL STATEMENT

### Introduction

The Financial Statement provides a balance sheet and operating statement
for any month you choose. The computer maintains 12 months of
financial statement history for the current fiscal year and 12 months for the
prior fiscal year plus a thirteenth month for end-of-year adjustments.

You can run a Financial Statement on a single division or on any
combination of divisions you choose. If you have departmentalized your
financial statement, you can run a Financial Statement on the departments
to see the profit/loss of each department.

The Financial Statement is designed to give you a clear picture of the
business for submission to necessary agencies. This will save time and
work for the accounting department.


[| X15-2 FINANCIAL STATEMENT co

### How To Run

From the Financial Report Menu (X15), select option 2. After passing the
security gate, the following screen is displayed:

AUSTIN TRACTOR & EQUIPMENT Financial Statement X1520-801 1
Division: A Summary Option 11/13790

Enter ‘Y' for summarized financial statement: N

cmdl-End job

 

You have the opportunity to either print a complete Financial Statement or
a summary of the totaling accounts. For example, you have three Case
New Equipment general ledger accounts:

A130 New Case Tractors
Al40 New Case Implements
A150 New Case Other

In Financial Statement Format Maintenance, (X68-4), you have set up a
totaling account:

151 Total New Case Equipment

RELEASE 2.2 LU

## X18-2 FINANCIAL STATEMENT

On the above screen, the default is N. Left unchanged, a complete
Financial Statement will print. If you change the N to Y, a Financial
Statement containing only the totaling accounts will print. For a list of the
account numbers to be included in this type of Financial Statement, look at
the last page of your Chart of Accounts (X14-3). There is a list of the
totaling accounts.

When you have made the decision on summarized financial statement,
press Enter.

The Financial Statement Month Selection screen appears:

 

AUSTIN TRACTOR & EQUIPMENT Financial Statement *2520-101 1

Division: A Month Selection -

Enter the month fer which a Financial Statement is desired (2-13):
Is this statement for an open or closed month? Enter ‘O' or 'C' :
Select either current or previous year Enter ‘C' or 'Pt =
Enter the number of statement copies to be printed (1-99)

Examples: Month Open/Closed
1. Statement for most recently closed month 8 c
Statement for current month 10

2 °
3. Statement for oldest open month 9 °
4. Statement for the “thirteenth" month* 13 c

The “thirteenth month statement is your fiscal year end month plus
adjusting entries.

Gmdi-End job Cmd2-Select by department Cnd3-Select by division

 


[ «| X15-2 FINANCIAL STATEMENT co

The defaults will be for the oldest closed month.

Select the month by the calendar year, such as August = 8, September = 9,
and October = 10 in the example above. Figures on the Financial
Statement are based on the fiscal year-to-date. If your fiscal year begins
April 1, and you request a statement for month 8, you will get year-to-date
figures for April - August.

Enter the month for the financial statement. If the month is open, enter O.
If the month is closed, enter C. On the next line enter C if you want the
statement for the current year or P if you want it for the prior year.
Type the number of copies you want.
Note the Cmd keys at the bottom of the screen: (
Cmd2 Select by department. If you have departmentalized your
Sales, Cost of Sales, Income and Expense accounts as
explained in General Ledger (X1-4), you may select the
department by pressing Cmd2.
Cmd3 Select by division. If you have more than one division and
have similar account numbers, you can combine the

divisions for a financial statement containing all divisions.

Let's look at cach of these selections individually:

RELEASE 2.2 LO


X15-2 FINANCIAL STATEMENT [=]

Cmd2 SELECT BY DEPARTMENT

We will assume you have departmentalized all Sales, Cost of Sales,
Income and Expense accounts. If you have not or have questions
regarding departmentalization, refer to the section General Ledger (X1-4).
For example, we will say the departments have been defined as:

Department Code
Parts 1
Service 2
Sales 3
Administration 4

When setting up your General Ledger account numbers, the last position
of the account number was reserved for the department code. Also, we will
say our goal was to have each department receive credit for the sales they
made. This will help the shop offset their high expenses for electricity
with income generated by parts sales for equipment they are working on.
See a sample chart below:

 

PARTS -WHOLESALE A33001
PARTS-INTERNAL A33103
PARTS-COUNTER A33201
PARTS- SHOP A33302

OTHER INCOME-PARTS AS50501
OTHER INCOME-SERVICE A50502
OTHER INCOME-SALES A50503
OTHER INCOME-ADMIN. A50504

TELEPHONE EXP.-PARTS A67101
TELEPHONE EXP.-SERV. A67102
TELEPHONE EXP.-SALES A67103
TELEPHONE EXP.-ADMIN. A67104

## X15-2 FINANCIAL STATEMENT

To find out if the goal has been reached, we want to run a
departmentalized financial statement for the service department. The
department code is 2.

Press Cmd 2 and the following screen will appear:

AUSTIN TRACTOR & EQUIPMENT Financial Statement x1520-102 2

Division: A Department Selection

Department selection mask: XXXXXXXX
To select all departments and print ali accounts, the mask must be all ‘x'.

To select all departments and summarize en a major portion of the account
number, enter a '*' in the mask where the minor (department) portion of the
account numbers begin.

To select a specific department, enter the character(s) that identify that
Gepartment. Be sure tc place them in the mask exactly where they appear in
the account numbers.

Examples:
Assume general ledger accounts A100A and A100B which represent cash accounts
for departments ‘A’ and ‘B‘ respectively.

2. All accounts Bicie valve

2. Summarized 2OOKK 20K

3. Specific department OCKKAIOOK

cmdé-return te Month Selection screen


 

Refer to the line on the previous screen:

Department selection mask:  XXXXXXXX

The "XXXXXXXX" represent the eight possible characters in a General
Ledger account number. Select the character representing the department
you want and enter it in over the "X" that is in that position. For example,
Parts Shop has an account number of A33302. The 2 in the last position
of the account number is the department code. It is in the sixth position of
the account number.

On the above screen, we have entered a "2" in the sixth position of the
“mask”. This tells the computer to search all General Ledger account
numbers and report those that have a "2" in the sixth position of the
General Ledger account number. In this way, a financial statement is
created for the service department, department 2.

If you want to see a financial statement containing a list of all
departments, enter "*" in the sixth position of the "mask". This telis the
computer include al] accounts with anything in the sixth position of the
General Ledger account number on the Financial Statement.

‘When the department selection is made, press Cmd6 to return to the
Month Selection screen.

Cmd3 SELECT BY DIVISION

If you have more than one division, you can select any of or all of the
divisions and combine them on one financial statement. For the
comparison to be valid, you would want to have the same General Ledger
numbers in all divisions.

Press Cmd3. The following screen appears:


| 3 | X15-2 FINANCIAL STATEMENT

AUSTIN TRACTOR & EQUIPMENT Financial Statement x1520-103 3

Division: A Division Selection
To include other divisions in a composite Financial Statement, place any
character beside the divisions to include.

B DEALER SALES & SERVICE, LTD D ABC COMPANY

E ABC COMPANY M MOTORCYCLE CITY
‘T THERMOKING

md6-return to Month Selection screen
Place any character next to the divisions to be included on the Financial
Statement.

When the selection is made, press Cmd6 to go back to the Month
Selection screen. On the Financial Statement Month Selection screen,
press Enter. The final verification screen will be displayed:
LU


AUSTIN TRACTOR & EQUIPMENT Financial Statement x1§20-104 ¢
Division: a Final verification

IE you have completed making your selections, press Enter to continue.

However, if you want to change your month, department or division selection,
press cmaé.

You have selected:
Month 8
Open/Closed 0

Year CURRENT
Department — XXKKK2xx
Division B

copies 02

Cmdi-End job Cmd6-return to Month Selection sereen Enter to continue

 

In the above example, the choice is for 2 copies of the Financial
Statement for the open 8th fiscal month, for the current year, which will
include department 2, service, for divisions A and B.

If the choices displayed are not the ones you want, press Cmd6 to return to
the Financial Statement Month Selection screen. You can begin the
selection process again.


[| X15-2 FINANCIAL STATEMENT c

Verify the choices made, and if they are correct, press Enter. The
Financial Statement will be placed on the job queue. The entrance screen
with the Summary Option prompt retums. Request another financial
statement, or press {Cmd1] to end the job and return to the Financial
Report Menu.

A sample of the Financial Statement is displayed on the next page.

RELEASE 2.2 LL


‘BELLIIGHAM CAR & TRUCK

P.O, BOX 7a54e
1295 sar ROAD
BELLINGHAM, WA
‘Signed by:

(CASH on HAND
ASH INV BAEK

(CASH TH BARK-PAYROUL
PETTY CASR-CRANCE FOND
+ TOTAL cA ©

[WHOLE Goous RECEIVABLES
[ACCOUNTS RECEIVABLE
DOUBTFUL, RECEIVARLES

+ TOURL RECEIVASLES ©

es TRACTORS
‘NE EporeeET

SED TRACTORS & EQUIPMENT
PARTS & ACCESSORIES

tL & GREASE

“TOTAL TIVENTORIES ©

CURRENT ASSETS **++

SEPAID INSURANCE
PREPAID OTHER
- PREPAID EXPERSE +

SHOP BQUzPREIT
[ACCUM DEPR-SHCP ZQUIP
FURNITURE & FIXTURES
ACCUM DEPR-FURNITURE
‘CARS, TRUCKS & TRAILERS
[AGOUM DEPR-CARS, TAUCKS
LEASEHOLD IMPROVEMENTS
[ACCUM DEPR-LEASEHOLD INP
RENTAL BQUIP

[ACCUM DEPR-RENTAL EQUIP
- FUMED ASSETS «1

FIMANCE RESERVE-HOLDBACKS A170
- OTHER ASSETS *+4eereee

826,956.31 * TOTAL ASSETS


1s, 896,
62.208

362,817.
42,762
126,638.
58,092
2393

152.967,
2,86?

FRIANCIAL STATEMENT
BALANCE SuEET
PECEMBER 15, 1997

‘TRIAL

38,288.72

207,205.01

378,702.54

624,008.27

158,099.
201,457.

BALANCE


ate 12/15/97
Tame 8.06.25
Department mask:

Minbilicves

+ NOTES PAYABLE-HEW TRACTOR A220
WOTES PAYABLE-HEW EQUIP A224
NOTES PAYABLE-BANKS ane
+ NOTES PAYABLE *re9*!

PAYABLES
CUSTOMER OEPOSITS-W.c.
CUSTOMER DEPOSITS-CTHER
+ ACCOUNTS PRYABLE +1

ACCRUED PAYROLe
(ACCRGED PAYROGL MOWTHLY
ACCRUED FIC

ACCRUED WITHHOLDING-FED
ACCRUED UNEMPLOYMET-FED
ACCRUED SALES TAX
ACCRUED PROPERTY-TAXES
CORP IBCCHE TAK

STATE & LocAL INCOME TAX
ACCRUED 8 & 0 TAX
ACCRUED TETEREST

+ ACCRUED LIABILITIES **+

+ CURREND LiaaIuITiEs ++

INOTES-LONG TERM
+ ose Tee Ltastiary +++

CAPITAL STOCK
RETAINED EARNINGS
NET voRTH +

PROFIT OR LOSS CURRENT YR
453.00 *

188,050.00
60,621.00

49,089.66
51,531.45
48,000.00

14,954.76
10,385.00,

4148.56
10,635.00

192,000.00

30,000.00
286,958.66

Paget
1520-63,
200K.

215, 671.00

25,621.41

40,100.30

27,392.41

282, 000.05,

150,359.66

315,204.26

- * TOTAL LIA & NET WORTH *
826,956.31 *


[2] X15-2 FINANCIAL STATEMENT C

### Fields And Descriptions

Fields found on the Financial Statement Balance Sheet are described
below in the order in which they appear from left to right:

 

Each is listed as an Asset or Liability with a debit or credit total.

Account Names Each of your entered accounts is listed.

Account # The General Ledger account number. (
Account Totals The total debit or credit for account groupings.

Totals Totals including Net Worth, P/L Current Year,

Liabilities and Net Worth, and Assets.

RELEASE 2.2 CO

### X15-2 Financial Statement [3]

Below is a sample of a Financial Statement Income Statement:

mere 12/15/97 Page
Depercewat mann: XCD

cone aesin

danger amaseno.e5stsar.ze rasta
nugs.9lwer.3e 07.62 maser Suess eases aoaze.e
swe 5s 695014 Gazv es ” . woers2 Mee s69906.59

453.05 es.80 1657.17 36058 ABAD eptte UES FDO? L40ees.26weeNSn)52222.85
seed 2904 30 30.32 ++ TOTAL ROMTAL saues ==> poasz.as | 1s700.25 75852182

ones 1S 19.00 paRIS-OOLESALe aasoes—usssseansa.es2eas.a
anes eee an36.82

2609.99 0 a2. : name gymis.es ceesees 33058.
307-82 3 : nose a2saits Lessee 1080.82
per.te . aesee aes aT 88.78

woans.ce 6996.07 we . anesoos.ae asianzs.or s3ans76.1s

 

Fields found on the Financial Statement Income Statement are described
below in the order in which they appear from left to right:

Sales Total sales for the month on each sales account.

Cost Total cost for the month on each cost account.

Margin Margin of profit on sales for the month by amount.

Percent Percent of profit on sales this month.

Account Title of the account.

Account Sales Sales General Ledger Account Number posted to.

Number Cost Cost General Ledger Account Number posted to.

Sales Year to date dollar amount of sales.

Cost Year to date dollar amount of cost.

Margin Dollar amount of margin of profit this year to date.
Can accommodate up to $99 million.

Percent Percent of profit this year to date.


[| X15-2 FINANCIAL STATEMENT Cc

| If cost figures are carrying down from one account number to the next,
check that each sales account is set up in General Ledger Maintenance

| with the appropriate cost of sales account listed in Account2. The
table in General Ledger Maintenance shows the appropriate accounts
| to enter in Accounts | and 2.

 

If you requested a summary only, your printout lists the sub-totals you
have set up on your regular financial statement, for example, Total (
Receivables, Total Inventory, Total Assets.

RELEASE 2.2 CO

## CHAPTER X15-3

TRIAL BALANCE

### Introduction

You can print a Trial Balance for any month, open or closed, or for the
13th month. The Trial Balance prints the year-to-date balance posted to
each General Ledger account at the end of the selected month.

Tf Journals are installed, you can request the Trial Balance by Journal IDs
if desired. Journal totals for the month of the report will be printed. In
addition, when Journals are installed, a Trial Balance by Journal ID is
printed automatically at Accounting End of Month.


[2] X15-3 TRIAL BALANCE C

### How To Run

From the Financial Report Menu, select option 3, Trial Balance. After the
Financial security gate, the selection screen appears:

 
 

  
  
  

1535-01 1

  

A & R SALES & LEASING

  

Division :

 

 
   
    
  
 

12-23)

Month Close or Open : ¢ (C = CLOSE 0 = OPEN}
By journals 1D : ON (Y/N)
Spaces between lines : 1 (1,2 or 3)

No. of copies a 2 (2-9)

   
 

(mdi-End job Cmd2-Change Division

 

 

 

Make your selections and press [Enter] to request the report, which is
placed on the job queue. You return to the Financial Report Menu.

O To change divisions from the selection screen, press [Cmd2] to return
to the security gate.

 

RELEASE 2.1 We

## X15-3 TRIAL BALANCE

A portion of a Trial Balance is illustrated below:

piviston & Month of + NOVEMBER 1991 Dime : 14:23:30 X1530-5a,
Account Ticle Debit, credit
110d CASH ON HAND.

1202 CASH IM BARK - PSB 36,702.24
1103 CANCELED pacuMENTS

110 PETTY CASH — CHANGE FUND 550.00

Y10A PETTY CASH - TRAVEL BACS 300.00

L121 ACCOUNTS RECEIVABLE 240, 205.54

1112 TOTAL RENTAL LEASE

LIS VISA, MASTER CHARGE, COD 3,189.39

E16 FNM WARRANTY 23,825.44

4120 FORD TRACTORS & EQUIPMENT 478,217.26
3121 MASSEY FRAGUSON TRACTORS 48,511.50

2123 NON-FORD EQUIPMENT. 103,905.39

1124 NEW HOLLAND 245,339.14

1125 USED TRACTORS & SQUIPHENT 285,410.29

2127 ROMFORD 53,425.14

132 PARTS § ACCESSORIES 443,097.15

136 REBUILT ENGINES 944.52

z140 SUSPENSE: 32,215.79

EM§ PREPAID - OTHER. 352.25,

asd sHop EQUIPMENT 34,427.96

LISS ACCUM. DEDR. - SHOP POUIP 23,465.63
Z1S$ FURNITURE & FIXTURES 98,774.58

L157 ACCUM. DEPR. - FURNITURE 86,700.20
L198 CARS, TRUCKS & TRAILERS 302,928.12

L189 ACCUM. DEPR,-CARS, TRUCKS 62,958.46
E160 «LEASEHOLD IMPROVEMENTS 72,028.00

L161 ACCUM DEPR,-LEASEHOLD IMP 46,819.97
1262 RENTAL EQUIPMENT

162 ACCUM. DEPR,-RENTAL EQUIP

170A PINANCE RESERVE - Wit 2,318.20

1220 © NOTES PAYARLE - FORD 590,695.36
L220R NOTES PAYABLE ~ LEASES 32,428.52
3221 NOTES PAYABLE-MF 36,639.10
1223 NOTES PAYASLE - OTHER

224 PLOORING-NEW HOLLAND 183.130.79
1238 NOTES PAYABLE ~ PSB 98,503.40
239R NOTES PAYABLE - CONTRACTS 17,174.73
1239 EMPLOYEE SAVINGS ACCOUNTS 341,476.23
nad) PAVARLES 328,102.42

ABR EQUIPMENT SALES. Trial Balance Bate; 4/20/92 Pasa:

 

 

 

 

- ACCOUNTING


Notes:

## CHAPTER X15-4

BUDGET MAINTENANCE

### Introduction

A budget is used to help predict the operations of a business for the current
operating year. Budget Maintenance allows you to set up a budget for the
current year. When performing Budget Maintenance, you will be provided
with figures from the current and previous year. You can use the figures as
a base for your budget.

### Financial Statement

Your Financial Statement is divided into two sections, Balance Sheet and
Operating Statement.

BALANCE SHEET

Assets = Liabilities

+
Equity or Capital

 

OPERATING STATEMENT

Sales ~ Cost of Sales
+ Income

- Expenses

= NET PROFIT

## X15-4 BUDGET MAINTENANCE

 

### Budget Methods

Budget Maintenance is performed general ledger account by general
ledger account. When you enter an account at Budget Maintenance, you
will see the following screen.

BELLINGHAM CAR & TRUCK CO. Budget Maintenance x1540-102
Division: A (Updating current year)

Account &

Current Year Previous Year ---~

Budget General Ledger Budget General Ledger

(General Ledger figures rounded to nearest dollar)

Jamary 197002- 18346
February 48500 $3147 (

March 24709 32468

April 21347

18000 34265

53425

49878- 7638

9700 76345

110208 $43213

121108- 65456

9997 6543

201222 123458

Enter ‘Y* to delete

Cmd2-Apply factor Cmd3-Mamual entry Cm&5S-Update Current
(md6-Copy current budget to previous year

 

Budget Maintenance is a fiscal year job. The first month displayed will be
the month your fiscal year begins. If your fiscal year begins in March, the
first month displayed would be March. The above screen is a picture of
Bellingham Car & Truck's New Tractors Sales account. The fiscal year for
this company begins in January.

RELEASE 2.1 LO


 

There are two ways to budget your general ledger accounts:
Manual Entries

Manual entry involves entering manually the budget figure next to the
month under the Budget column. Cmd3-Manual entry is used to make this
type of entry.

If the trend of the business is high sales during harvest season and very
low sales in the winter, manually enter these figures to show the trends.

Manual entries can be made on both balance sheet and operating statement
accounts.

Apply factor

A factor is a percentage. If you want to budget an increase in sales of 3%,
a factor can be applied. The factor is typed as 10300 or 103%. If
management predicts a slump in the sales, a factor to decrease sales by 3%
can be applied. The factor is typed as 9700 or 97%. If a factor is selected,
the previous year's general ledger balance for the month is multiplied by
the factor. The result is the budget.

General ledger balance X factor= Budget
Again, look at the New Tractors Sales example for Bellingham Car &
Truck. In February of last year, sales for the month were $48,500. If they
elect to factor Customer Labor Sales by 103%, the result would be:

General ledger balance X factor= Budget
48500 10300 49440


 

Balance sheet accounts provide a picture of asset, liability and capital
accounts on the date a financial statement is requested. The balances in
these accounts are directly dependent on the performance of the operating
statement accounts. For this reason, it is customary to budget operating
statement accounts only.

There are important differences in the way balance sheet accounts and

operating statement accounts are budgeted. Step-by-step instructions are
provided in this chapter.

RELEASE 2.1 tO


 

### When To Budget

Decide what period you are creating a budget for. What displays on the
screen is the last twelve months’ activity. Often time constraints determine
at what point in the fiscal year the budget for the next fiscal year is
prepared. The budget may need to be approved either by a major
manufacturer or a board of directors.

Bellingham Car & Truck makes its budget in October. Today is October 1,
1986 and the company is preparing the budget for 1987. The fiscal year for
Bellingham Car & Truck runs from January 1 to December 31.

On the screen, we are looking at the last twenty-four months' activity in
New Tractor sales. There are 2 sections: Current Year and Previous Year.
It is currently October 1, 1986. The current year for the months January
through September is 1986, and the previous year is 1985. For the months
October through December, the current year is 1985, and the previous year
is 1984.

Today's date is October 1, 1986. What you'll see on the screen is
illustrated below. The line, the years and arrows have been added to help
clarify exactly what year the figures are for.


BELLINGHAM CAR & TRUCK CO.
Division: A

Budget Maintenance
(Updating current year)

Account #

-- Previous Year ----

Budget General Ledger Budget

General Ledger

(General Ledger figures rounded to nearest dollar)

1986 =e2=> 197002-
4a500

24700

January 1985 ====>
February

March

April
may 18000
June

ouly 49878-
August 9700

Septenber 110208

 

October > 121108- 1984 ss==>
November 9997
December 201111

Enter ‘Y' to delete

15346
$3147
32468
21347
34265
53425
7638
76345
343213

63466
6543
123458

x1540-102

Cmdl-End job Cmd2-Apply factor Cma3-Manual entry cmdS-Update Current

Cmd6-Copy current budget to previous year

 

Budgeting will be for the remainder of the current fiscal year, 1986, for
months October through December. To budget the last three months for
1987, Bellingham Car & Truck will go back into the job in January of
1987 and budget, October, November and December.

C


 

### How To Run

From the Financial Menu, select option 4, Budget Maintenance.
Select the Division

Budget Maintenance is divisional. If the beginning fiscal month is the
same in all divisions, you can perform budget maintenance for all
divisions by selecting any division. If the fiscal year does not start in the
same month for all divisions, perform Budget Maintenance only for the
division selected at the security gate.

Same Fiscal Year

Bellingham Car & Truck has two divisions A and B. The fiscal year
begins in January for both divisions. Budget Maintenance can be
performed for both divisions in either division. At the security gate, either
the A or B division can be selected.

Different Fiscal Year

Bellingham Car & Truck has a third division, the S division. The fiscal
year begins in March. Budget Maintenance for the S division must be
performed separately. To perform Budget Maintenance on division S,
division S must be selected at the security gate.

Budget Maintenance is performed on each General Ledger Number
separately. After passing the security gate, enter the general ledger account
number you wish to budget.

The Manual Entry mode (Cmd3) will display.


 

### Balance Sheet Accounts

Below is a sample of the Accounts Receivable account for Bellingham Car
& Truck:

BELLINGHAM CAR & TRUCK CO. Budget Maintenance x1540-102 2
Division: A (Updating current year)
Account # ALLO ACCOUNTS RECEIVABLE

Current Year Previous Year ----
Budget General Ledger Budget General Ledger
(General Ledger figures rounded to nearest dollar)
7803 3246
February 13240- 643
march 3642- 2346
April 16135 3548
May 19748 7547
dune 342
duly 5090 4327
August 2412 543
September 116034 5424
October 108253- 5469
November 15000- 7653
December gaan 2548
Enter 'Y' to delete

Cmdl-End job Cmd2-Apply factor Cnd3-Manual entry cmd5-Update current
cmd6-Copy current budget to previous year

The General Ledger column displays the change from the previous month.
For example, Bellingham Car & Truck's Accounts Receivable had a
balance of $7900 on December 31, 1985. The balance displays on the
December 1985 Financial Statement. In January, 1986 there was a change
of $7,603. The January,1986 financial statement shows a balance of
$15,503.
Lo


 

Financial Statement Change
December 1985 7,900
January 1986 15,503 7,603

When budgeting balance sheet accounts, use Manual Entries. Apply factor
(Cmd2) is not applicable. Since you're dealing with the net change from
one month to another, you would not want to apply the same percentage to
all the months.

The screen is divided into five columns:

Month

The months are listed on the left hand of the screen. They display in fiscal
order. If the fiscal year begins in March, March wiil be the first month
displayed. At Bellingham Car & Truck, the fiscal year begins in January.

Budget columns

If Budget figures have been entered, they will display in the Budget
columns for the current and previous years. If the columns are blank,
Budget figures may be entered or existing figures may be updated. The
message below the screen title tells whether you are updating current or
previous year's figures. Cmd5 will switch you back and forth between the
two years. Your cursor will be placed in the correct column when you take
Cmd5.

The General Ledger columns
The change from the previous month is displayed for the current year and
the previous year.


15-4 BUDGET MAINTENANCE

 

Entering the budget

Balance sheet account balances are directly affected by the operations of
the business. For this reason, you may not wish to budget balance sheet
accounts. If you do, follow the steps below:

O Determine what the general ledger balances should be for each month.
This can be determined by examining the 12 financial statements from
the previous year. The financial statements will show the total of the
balance sheet accounts on the last date of the month.

Take a print screen of the Budget Maintenance screen for balance sheet
accounts.

Below is a chart created by Bellingham Car & Truck. It shows what the (
total balance will be in Accounts Receivable account if the budget is

teached.
Month G/L Budget
January 8,500
February 7,500
March 10,069
April 8,569
May 12,569
June 13,669
July 12,669
August 7,669
September 6,669
October 15,669
November 21,269
December 19,269

RELEASE 2.1 CO


The exact budget figure for the first fiscal month will be entered in

the Budget column.

To budget the months 2 - 12, enter the Change for the month. The
Change is the amount of change to the general ledger budget figure for
the previous fiscal month. Use the print screen taken in the previous
step to determine the trend of changes. Below is the chart Bellingham
Car & Truck put together for Accounts Receivable. It now includes the
Change for the months February through December:

Month G/L Budget

January
February
March
April

May

June

July
August
September
October
November
December

Change

8,500
7,500
10,069
8,569
12,569
13,669
12,669
7,669
6,669
15,669
21,269
19,269

1,000-
2,569
1,500-
4,000
1,100
1,000-
5,000-
1,000-
9,000
5,600
2,000-

Fill in the screen for the balance sheet account. Enter the exact budget
figure for the first month. For months 2 - 12, enter the amount of the
difference. Below is the completed Accounts Receivable screen:


 

BELLINGHAM CAR & TRUCK CO. Budget Maintenance 1540-102
Division: & (Updating previous year)

Account # ACCOUNTS RECEIVABLE

Previous Year ----

Budget General Ledger Budget General Ledger

{General Ledger figures rounded to nearest dollar)
January aso0 7603 3246
February 1000- 43240~ 643
March 2569 3642- 2346
april 15900- 36135 3548
May 4000 ig7ag 7847
dene 1100 342
galy 1000- 5090 4327
August s0¢0- 2211 543
September 1000- 116034 2000 5424
October eco 108253- 1000+ 5469
November 5600 15900- 3000 7653
December 2000-~ 9441 1500- 2548 {

Enter '¥’ to delete

(md1-End job Cmd2-Apply factor Cma3-Manual entry CmdS-Update current
emdé-Copy current budget to previous year

 

If the Change must be subtracted from the account balance to achieve
new general ledger budget, use the Field Minus key to make the
number negative.

For Bellingham Car & Truck, January's budget of Accounts Receivable
is $8,500. The budget for February is $7,500. The balance of the
general ledger must go down $1,000 to achieve the budget for the
month. Type 1000 and press Field Minus.

If the Change must be added to the account balance to achieve the new

RELEASE 2.1 Co


 

general ledger budget, use the Field Exit key to make the number
positive.

For Bellingham Car & Truck, the April budget is $8,569. The
management believes that the balance in the account will be $12,569 in
May. The balance in the account must increase by $4,000 to reach the
budget. The change is a positive number. Type 4000 and press Field
Exit.

When the screen is filled in, press Enter. Enter the next general ledger
account number to be budgeted.


 

### Operating Statement Accounts

After passing the security gate, enter the first operating statement general
ledger to be budgeted.

For operating statement accounts, you may manually enter budget figures
or apply a factor.

Below is the New Tractors sales account for Bellingham Car & Truck. The
figure displayed under General Ledger is the balance of the operating
account for the last twelve fiscal months. Use this figure as a base for the
budget.

RELEASE 2.1 LO


 

BELLINGHAM CAR & TRUCK CO. Budget Maintenance X1540-102 2
Division: A (Updating previous year)

Account #

current Year Previous Year ----

Budset © General Ledger Budget General Ledger

(General Ledger figures rounded to nearest dollar)
January 197002- 15346
February 48500 s3147
March 24700 32468
April 21347
May 18000 34265
June 53425,
guly 49878- 7638
August 9700 76345
September 120208 $43213 h
October 121108- 65466
Novenber 9997 6543
December 201111 123458

Enter '¥' to delete

Cmdi-End job Cmd2-Apply factor ¢md3-Manval entry cmd5-Update Curreat
emdé-Cory current budget to previous year

 

 

The screen is divided into five columns:

Month

The months are listed on the left hand of the screen. They display in fiscal
order. If the fiscal year begins in March, March will be the first month
displayed. At Bellingham Car & Truck, the fiscal year begins in January.

Budget columns
If Budget figures have been entered, they will display in the Budget


 

columns for the current and previous years. If the columns are blank,
Budget figures may be entered or existing figures may be updated. The
message below the screen title tells whether you are updating current or
previous year's figures. Cmd5 will switch you back and forth between the
two years. Your cursor will be placed in the correct column when you take
Cmd5.

The General Ledger columns

The general ledger balance for the month is displayed for both the current
and the previous year. You can use this figure as a reference for budgeting
the current year.

There are two ways to budget operating statement accounts. Manually and
by applying a factor.

Manual Entry

Operating statement accounts can be manually budgeted. When an account
number is entered, Manual entry mode (Cmd3) is displayed.

Below is a sample of the New Tractors Sales account for Bellingham Car
& Truck.

RELEASE 2.1 Lu


BELLINGHAM CAR & TRUCK CO, Budget Maintenance x1540-102 2
Division: A (Updating previous year}

Budget General Ledger Genexal Ledger
(General Ledger figures rounded to nearest dollar)
January 197002- 15346
February 48500 53147
March 24700 32468
April 21347
May 18000 34265
June 53425

49878- 7638

3700 76345

110208 543213

121108- 65466

9997 6543

201111 123458
Enter 'Y' to delete

cmd2-Apply factor Cmd@3-Manual entry Cmd5-Update Current
end6-Copy current budget to previous year

Use the exact budget figure for each month. Type the figure in the Budget
column next to the month. At Bellingham Car & Truck, new tractor sales
should increase in January to around $50,000. To indicate the budget of
$50,000, type 50000 in the Budget column next to January. Press Field
Exit. Following is Bellingham Car & Truck's budget for Customer Labor
sales:

### 15-4 Budget Maintenance

 

BELLINGHAM CAR & TRUCK CO. © Budget Maintenance 1540-102 2
Division: A (Updating previous year)

Account # NEW TRACTORS

- --- Previous Year ----
Budget General Ledger Budget General Ledger
(General Ledger figures rounded to nearest dollar)
January 50000 197902- 15346
February 55000 48500 53147
March 30000 24700 32468
April 20000 21347
May 20000 148000 34265
dene 30900 53425
50000 49878- 50000 7638
30000 9700 30000 76345
12000 110208 40000 543213
30000 121108- 20000 65466
40000 9987 40000 6543 {
20000 201111 30000 123458
Factor Enter 'Y' to delete

Cmdi-End job Cmd2-Apply factor Cmd3-Manual entry cmd5-Updace Current
Cmdé-Copy current budget to previous year

 

When the screen is filled in, press Enter. Budget the next operating
statement account.

Apply factor

Cmd72 is used to apply a percentage factor to all the months for the
operating statement general ledger accounts. The result will display in the
Budget column next to the month.

When Cmd2 is pressed, the following screen displays:

RELEASE 2.1 CO


BELLINGHAM CAR & TRUCK CO. © Budget Maintenance x1540-102
Division: A (Updating previous year)

Current Year Previous Year ---~
Budget General Ledger Budget General Ledger
(General Ledger figures rounded to nearest dollar)
January 309 457
February 390- 214
March sor 544
April 44ai- 765
350
gune
ouly
August
September
October
November
December
Factor Enter 'Y' to delete

(mdi-End job Cmd2-Apply factor Cmd3-Manual entry Cmd5-Update Current
Cmd6-Copy current budget to previous year

The above screen is the Parts Internal sales account for Bellingham Car &
Truck. The goal at this company is to increase parts internal sales by 3%
next year. In the field Factor, type 10300. Press Field Exit. Press Enter.


 

The following screen is displayed:

BELLINGHAM CAR & TRUCK CO. = Budget. Maintenance X1540-102
Division: A (Updating previous year)

Account # .. + A3310 PARTS-INTERNAL

Previous Year ----
General Ledger Budget General Ledger
(General Ledger figures rounded to nearest dollar)
January 318 309 457
February 402~ 390- 214
March 516 sol 544
april 454- 4ai- 765
361 350 246
643
July 520- 543
August 650 631 133
September 622- 766 {
October 105 102 433 .
November 321 312 533
December 321- 312- 253
Factor 20300 Enter ‘¥' to delete
mdi-End job Cmd2-Apply factor ¢md3-Manual entry  Cma5-Update Current
cmdé~Copy current budget to previous year

 

If the figures are acceptable, press Enter.

If Bellingham Car & Truck was predicting a decrease in sales of 3%, the
factor entered would be 9700. Press Field Exit. Press Enter. If the figures
are acceptable, press Enter.

Type the next general ledger account number to be budgeted. Repeat the
process.

RELEASE 2.1 LO


 

Cmdi1 End job

When the budget is complete, press Cmd1 io end the job. The following
screen will display:

Budget Maintenance 1549-001

Do you want to print the Verification Report (¥/N)? +

 

To get the verification report, type Y and press Enter. If you do not want
the report, type N. Press Enter.

If Y was entered, the Budget Maintenance Verification Report will print. :

BELLINGHAM CAR & TRUCK CO. BUDGET MAINTENANCE Date 12/15/89 Page 2
BELLINGHAM, HA a VERIFICATION REPORT Time 14.33.29 1540-28
vanuazy February March April way gune July August Septenber October November Cecenber

aiooo CASH ON HAND ++ current Year ---
4608 3420 esse- 29308

 

seat) ACCOUNTS RECEIVABLE
so> Previous Year ~~~

1000-3000,

- Current Year
o-> Previous Year
soo0n = 30000» 49000 © 20088 © cona0
PARTS-INTERNAL, c++ Current year ---
402- 516 36 536- 650 sa1- 205 32a
wos Previous Year --~

 


 

### Summary

In summary, there is a difference in the way balance sheet accounts and
operating statement accounts are budgeted. When budgeting follow the

rules below:
Balance Sheet Accounts Operating Statement Accounts
Use the actual budget amount for _—_ Use the actual budget amount

the first fiscal month. for all 24 months.
Use the Difference necessary to Use a factor to increase or

achieve the budget for months decrease operating accounts

2 through 24. for the year based on last

year's figures. {
CHANGE A BUDGET FIGURE

You can change any budget figure. From the Financial Report Menu,
select option 4, Budget Maintenance. After passing the security gate, type
the general ledger account number to reflect the change. Move the cursor
to the field and type over the figure.

RELEASE 2.1 KO

## CHAPTER X15-5

BUDGET REVIEW

### Introduction

Budget Review allows you to run a Financial Statement which displays

the budget information for the month chosen. The report will be in the .
form of the Financial Statement. You will be able to view the budget, the
actual figures, and the variance in doilars and percent.

### How To Run

Before Budget Review can be run, Budget Maintenance must be
performed. Refer to CHAPTER X15-4 for information.

After passing the security gate, the following screen will display:

BELLINGHAM CAR & TRUCK x1520-802
Division: A 9/22/86

Enter 'Y' for summarized financial statement: N

eméi-cancel job.

### K15-5 Budget Review

 

You have the opportunity to either print a complete Budget Review
Financial Statement or a summary of the totaling accounts. For example,
you have three Case New Equipment general ledger accounts:

A130. New Case Tractors
Al40 New Case Implements
A150 New Case Other

In Financial Statement Format Maintenance, (X68-4), you have set upa
totaling account:

151. Total New Case Equipment

On the above screen, the default is N. Left unchanged, a complete Budget
Review Financial Statement will print. If you change the N to Y, a Budget (
Review Financial Statement containing only the totaling accounts will °
print. For a list of the account numbers to be included in this type of

Budget Review Financial Statement, look at the last page of your Chart of
Accounts (X14-3). There is a list of the totaling accounts.

Decide which type of statement you want. Press Enter.

RELEASE 2.1 tC

## X15-5 BUDGET REVIEW

 

The Budget Review Month Selection screen will display:

Budget Review x1550-1011
Division: Month Selection

Enter the month for which a Budget Review is desired (1 - 12)
Select either current or previous year Enter ‘C* or 'P*
Is this review for an open or closed month? Enter '0' or 'C'
is this review for a single month or YTD? Enter 'M' or '¥*

Examples : Month Open/Closed. :
1. Statement for most recently closed month - 6 c L
2. Statement for current month - 22 °
3. Statement for oldest open month - 7 °

(mdl-End job Cmd2-Select by department cmd3-Select by division

The defaults will be the oldest closed month. i

Select the month by the calendar year, such as August = 8, September = 9,
and October = 10 in the example above. Figures on the Budget Review
Financial Statement are based on the fiscal year-to-date. If your fiscal year
begins April 1, and you request a statement for month 8, you will get
year-to-date figures for April - August.

Enter the month for the Budget Review Financial Statement. If the month
is open, enter O. If the month is closed, enter C.


 

On the next line, enter C if you want the report for the current year or P if
you want it for the previous year.

Choose either Y for year-to-date information or M for month-to-date
information. Month-to-date will contain the totals for the chosen month.

Balance Sheet Accounts - The figures will be the same whether a Y or M is
chosen for balance sheet accounts. The program looks at the month
selected, takes the beginning fiscal year figure and adds or subtracts the
variance totals used in Budget Maintenance. See X15-4 Budget
Maintenance. The figure will always be fiscal year-to-date.

Operating Statement Accounts - These figures are displayed for the
month if M is selected. If Y is selected, the figures will be fiscal
year-to-date. (
Note the Cmd keys at the bottom of the screen.
Cmd2 Select by department. If you have departmentalized your Sales,
Cost of Sales, Income and Expense accounts as explained in
General Ledger (X1-4), you may select the department by pressing
Cmd2.
Cmd3 Select by division. If you have more than one division and have
similar account numbers, you can combine the divisions for a

financial statement containing all divisions.

The selections are discussed below:
Cmd2 SELECT BY DEPARTMENT

We will assume you have departmentalized all Sales, Cost of Sales,

RELEASE 2.1 LO


 

Income and Expense accounts. If you have not or have questions regarding
departmentalization, refer to the section General Ledger (X1-4).

For example, we will say the departments have been defined as:

Department Code
Parts 1
Service 2
Sales 3
Administration 4

When setting up your General Ledger account numbers, the last position
of the account number was reserved for the department code.

Also, the goal was to have each department receive credit for the sales
they made. This will help the shop offset their high expenses for electricity
with income generated by parts sales for equipment they are working on.
We have budgeted the figures for the service department with the income
built in.

See a sample chart below:

PARTS-WHOLESALE A33001
PARTS-INTERNAL A33103
PARTS-COUNTER A33201
PARTS-SHOP A33302

OTHER INCOME-PARTS AS50501
OTHER INCOME-SERVICE A50502
OTHER INCOME-SALES AS50503
OTHER INCOME-ADMIN. AS0504

TELEPHONE EXP.-PARTS A67101


 

TELEPHONE EXP.-SERV. A67102
TELEPHONE EXP.-SALES A67103
TELEPHONE EXP.-ADMIN. 67104

To find out if the goal has been reached, we want to run a
departmentalized budget statement for the service department. The
department code is 2.

Press Cmd 2 and the following screen will display:

BELLINGHAM CAR & TRUCK BUDGET REVIEW x1520-102
Division: A DEPARTMENT SELECTION

Department selection mask: XKXKK2xX

fo select ail departments and print all accounts, the mask must be all "x",

To select all departments and summarize on a major portion of the account number,

enter a "*" in the mask where the minor (department) portion of the account
numbers begin.

To select a specific department, enter the characteris) that identify chat
department. Be sure to place them in the mask exactly where they appear in the
account numbers.

Examples:
Assume general ledger accounts A100A and Al00B which represent cash accounts for
departments "A" and "B* respectively.

1. All accounts sequacao.

2. Summarized OOO OOK

3. Specific department KAI

Cmdé-return to Month Selection screen.

Refer to the line on the previous screen:


 

Department selection mask: XXXXXXXXK

The "XXXXXXXX" represent the eight possible characters in a General
Ledger account number. Select the character representing the department
you want and type it in over the "X" that is in that position. For example,
Parts Shop has an account number of A33302. The 2 in the last position of
the account number is the department code. It is in the sixth position of the
account number.

On the above screen, we have entered a "2" in the sixth position of
the"mask". This tells the computer to search all General Ledger account
numbers and report those that have a "2" in the sixth position of the
General Ledger account number. In this way, a financial statement is
created for the service department, department 2.

Tf you want to see a Budget Review statement containing a summary of all
departments, enter "*" in the sixth position of the "mask". This tells the
computer include all accounts with anything in the sixth position of the
General Ledger account number on the Budget Review Statement.

When the department selection is made, press Cmd6 to return to the
Month Selection screen.

Cmd3 SELECT BY DIVISION

If you have more than one division, you can select any of or all of the
divisions and combine them on one Budget Review Financial Statement.
For the comparison to be valid, you would want to have the same General
Ledger numbers in all divisions.

Press Cmd3. The following screen displays:


 

BELLINGHAM CAR & TRUCK BUDGET REVIEW 1520-103
Division: A DIVISION SELECTION

To include other divisions in a composite Budget Review, place any
character beside the divisions to include.

X B EVER AVAILABLE RENTAL

Press Cmd6 to return to Month Selection screen.

 

Place any character next to the divisions to be included on the Budget
Review Statement.

When the selection is made, Cmd6 back to the Month Selection screen.

On the Budget Review Financial Statement Month Selection screen, press
Enter. The final verification screen will display:

RELEASE 2.1 LC


 

BELLINGHAM CAR & TRUCK CO. Budget Review X1550-104 4
Division: A Final Verification

If you have completed making your selections, press Enter to continue.
However, if you want to change your any of your selections, press CmdS

You have selected:
Month 06

Year CURRENT
Open/Closed ¢
Month/¥TD ™
Department

Division

Cmdl-End job Cmd6-return to Menth Selection screen Enter to continue

 

Verify the choices made, if they are correct, press Enter. The Budget
Review Financial Statement will be placed on the job queue.

In the above example, the choice of Budget Review Statement is for the
closed 6th fiscal month, for the current year and will include department 2,
service, displaying month-to-date figures, for divisions A and B.

Tf the choices displayed are not the ones you want, press Cmd6 to return to
the Budget Review Month Selection screen. You can begin the selection

process again.

The Balance sheet will print first.


 

The Income Statement will print next. Below is an example of ABC
Company's Budget Review Income Statement:

BUDGET REVIEW Dace 12/25/85 Page 3
INCOME. STATEMENT ‘Tima 28.03.39 1550-7A
SALES FOR 12 MONTHS ENDING DECEMBER 15, 1985 Department mask: ouuoGGR

sales Account Title cose Profit Margin
Actual Budget. -Varfance Percent Actual Budget «Variance Percent Actual Budget Var,
10256¢0  900000»=«125640 12.28 NEW TRACTORS stises —«783000«SzB52 14.31 21.22 13.00. BB+
263495 -2sc000 13495 5.12 NBW EOOTPMENT 217858 217500 38500616 17.32 13,004.32
548s3 ssoce 147-.27- USED TRACTORS-EQUIP 44574 47980 3276- 7.38- 18.74 13.00 8.74
1343983 «1205000, «132988 10.34 ** TOTAL NEW & USED teres 3174030 «1048350 «125680 10.72 12,65 13.00 35>

92563 100000 7437- 8,03- RENTAL EQUIP REVENUE 68906 e000 19096-27.72- 25.56 12.00 13,56
140629 160000, 40589 28.92 RENTAL BQUIP SALES eeaes 88000 4650530037032 12.00 25.42
233282 200000 33252 14.26 ** TOTAL RENTALS *+° 157362 176000 16631- 22.B4- 32.53 12,09 20.53

noise aseea genie .26- emnssmccesos ee eee
ne santa) Soe eatio-ooman mone bas “eis pee sees
sist si000= nian eauoccumemn nomi, © erege= peste Enos ands anos hase
eas eroen=2489 3.99. puMmoe BEEN fain fone aa dese ganar
qs “sea tases muscu fr hs deat ass gute ante alees (
sot bee asa trey ons onmaoe mmo saavledgheis ane are
sree nese ta ay te ataar ams seeeeessontsge assests hae nas Ee

gorna gs000 4714 4.93 SERVICE LABOR-CUSTOMER 665559 66500 159-24 33,18 30.00.18.
12641 an000 2641 12,98 SERVICE LASOR-INTERNAL 10856 700 3156 29.07 14.12 30.00 5.88-
7873 ecoe 227-  1.61+ SUBLET REPAIRS 6228 5600 6189.94 12.02 30,00 47.98:

x2o22at1ag00 6228 «49.28 ** TOTAL SERVICE *esreess 83733 79800 3933 4.70 30.35 30.00 38

18g5095 1706500788888. 1543729 1428775113554

 

RELEASE 2.1 LU

## CHAPTER X15-7

DAILY OPERATING CONTROL REPORT

### Introduction

The Daily Operating Control (DOC) Report has been designed to give you
maximum flexibility. You may run a fully detailed Daily Operating
Control Report for one division or you may design special reports
(profiles) to meet your particular needs. The special reports may include
more than one division and any combination of the segments which appear
on the full report:

= Sales

= Cash

= Receivables

= Payables


= Work-in-Process
= Expenses

Special Features:
® Run the fully detailed report which is provided.
= Design your own Daily Operating Control (DOC) Reports:
- choose the segments you want
- specify full detail or summary only
- include other divisions
- customize a descriptive legend
= Run all reports quickly and easily from a report selection screen.
= Organize sales and expenses accounts by departments.
= Unit information included in the Sales segment:
- number of units in inventory
- value of units in inventory
- exclude units below your specified cost
- number of units sold
~ gross profit on each unit
= Compare sales to your budget for sales, or gross profit to your budget
for gross profit.


[=| X15-7 DAILY OPERATING CONTROL REPORT

### How To Run

Report Selection Screen

From the Financial Report Menu (X1-5), select option 7, Daily Operating
Control Report. The selection screen is illustrated below:

ABC COMPANY Daily Operating control x1570-101
Division: K Select DOC Reports

Select DOC Report Profile Ending Date (010197 to 052197)
Basic Report 51997

ALLSALES Sales Analysis: All Divs 51997

CASE Cash only, all divs (
CASKMAIN Cash only, main div.

Quick Totais only, all divs

UNITS units & Cash, DivA & L

Enter any character beside each desired report, and press Enter.

Cm@i-End job Cmd8~Maintenance Options

 

The Basic Report will have all detail for all accounts in all segments of the
Daily Operating Control Report for the division selected at the security
gate. If you have not designed other reports, it will be the only one
available.

RELEASE 2.2 CO


X15-7 DAILY OPERATING CONTROL REPORT [2]

‘You must provide an Ending Date for any report which includes the Sales
or Cash segments. The range of Ending Dates (from your open general
ledger months) is provided in the top right hand corner.

If you have more than one page of profiles, press Enter without making
selections to see the next page.

You may select as many reports at one time as you wish. They will be
placed on the job queue automatically. Then you will be able to select
others if you wish. These reports access many files and may take several
minutes to run. As each report finishes, you will receive a message at the
work station.

 

 

To design your own report, press Cmd8 for Maintenance Options.


[ «| X15-7 DAILY OPERATING CONTROL REPORT

Cmd8-Maintenance Options

When you press Cmd8-Maintenance Options, you will see this screen:

ABC COMPANY Daily Operating Control x1570-102
Division: x Maintenance Options

. Maintain DOC Profiles
. Assign Accounts to DOC Departments
. Maintain DOC Departments

. Maintain DOC Legends (

Option:

Cmdi-End job  Cmd3-Go back

 

Option 1, Maintain DOC Profiles, allows you to set up any number of
profiles for reports. The reports can then be run from the report selection
screen.

RELEASE 2.2 LU


X15-7 DAILY OPERATING CONTROL REPORT [=]

If you plan to departmentalize the Sales or Work-in-Process segments in
your report profiles, set up the DOC departments first. Choose option 3, to
Maintain DOC Departments. After the departments have been set up,
choose option 2 to Assign Accounts to DOC Departments. Then choose
option 1 to define your DOC Report Profile.

Options are discussed in the order in which they appear on screen.

Cmd1-End job

Cmd1 will end the job. You will return to the Financial Report Menu.
Cmd3-Go back

Cmd3 will take you back one screen.

Cmd19-Delete this profile

Cmd19 will delete a report profile.

The Command keys are only valid when displayed on the screen.

Maintain DOC Profiles

You may define as many profiles as you need. The name and description
of each profile will be displayed on the report selection screen. The reports
may be run from the selection screen as often as necessary. You will not
have to return to maintenance unless you want to change a profile or add a
new one.

If you choose the Sales or Work-in-Process segments, you will be able to
specify the departments you want on the next screen.

If you have more than one division, the last screen will allow you to
specify which divisions you want to include.


[ «| X15-7 DAILY OPERATING CONTROL REPORT

First, fill in the name of the profile as illustrated below:

ABC COMPANY Daily Operating Control x1570-103
Division: kK Maintain DOC Profiles

DOC Profile Name: UNITS

 

Press Enter. The report profile screen is illustrated on the next page.


X15-7 DAILY OPERATING CONTROL REPORT | 7 |

Report Profile Screen
This is an example of the report profile screen:

A & R EQUIPMENT Daily Operating Control K1570-104 4
Division: L Maintain DOC Profiles New Profile

boc Profile Name: UNITS
Description: Units and Cash, Div E & L

Segments to include: x Sales
fany character) X Cash
~ Receivables 5
~ Payables
— Payroll
~ Work in Process
X Expenses

Show by accounts
or departments? {A/D): A (Sales Segment)

Show by accounts
or departments? (A/D): A (Expenses Sesment)

 

omdl-End Job Cmd}-Go Back Cmd19-Delete this profile

 

Put any character beside the segment(s) you want to include. Press Enter
after making changes on any screen.

Show by accounts or departments? (Sales and Expenses Segments)

When you have chosen the segments you want, specify whether you want
detail for each account. "A" means that each department will be listed

## X15-7 DAILY OPERATING CONTROL REPORT

 

separately on the report. In the department section, account detail will be
displayed in account number order. The department totals appear at the
bottom of each section.

“D" means that only segment and department totals will be printed.

Press Enter. If you did choose the Sales or Work-in-Process segment, you
will go to the department selection screen. The 2 character DOC
department codes must be set up using Maintenance Option 3, Maintain
DOC Departments. If you have not set up your codes, Cmd3 to go back to
the Maintenance Options screen and choose Option 3.

RELEASE 2.2 LO


Department Selection Screen

The DOC profile illustrated below contains the Sales segment. The
department selection screen illustrated below follows the report profile
screen. If the Sales or Work-in- Process segment is not selected, you will
not see this screen.

A & R EQUIPMENT Daily Operating Control 1570-105 5
Division: L Maintain DOC Profiles Current Profile

Doc Profile Name: UNITS
Description: Units and Cash, DivA & L
Departments to D 01 New Vehicles D 02 Used Vehicles
include: D 03 Service D 04 Rental and Leasing

(amy character} 05 Parts Counter 06 Body Shop
07 Service 08 Chemicals

Minimm unit cost
to show as inventory: 100

Budget for Sales or
Gross Profit? .(S/G): §

(mdl-End Job Cmd3-Go Back Cmd19-Delete this profile

 

Put any character by the departments you want to include on this report.
Press Enter after making changes on any screen. The following fields are
required only if this profile includes the Sales segment.


 

Minimum unit cost to show as inventory

If you are choosing departments which include units sales, the Daily
Operating Control Report will show the number of units currently
available in inventory.

For correct unit counts, there must be a valid sales account number in the
“Account 1" field of each Unit Inventory Account in General Ledger
Maintenance (X14-2). You may specify a minimum cost. Units which
have a cost less than the minimum cost will not appear on the report. This
feature allows you to exclude units which have been taken in trade or
which have been accepted for sale on consignment and entered into the
system. If the field is left blank, all unsold units will be counted.

Budget for Sales or Gross Profit

The last choice is whether you want the department totals on the report to (
be compared to your budget for sales or to your budget for gross profit. If

the Gross Profit method is selected, the system calculates your budget for

gross profit by adding budget figures for sales and subtracting budget

figures for cost of sales.


Division Selection Screen

You will see the division selection screen, illustrated below, if you have
more than one division.

The division selection screen looks like this:

A & R EQUIPMENT Daily Operating Control X1570-106 6
Division: L Maintain DOC Profiles Current Profile

DOC Profile Name: UNITS
Description: Units and Cash, Div A & L
Divisions to include (any character}:

Xx A A DIVSION xX L A & R EQUIPMENT

Cmdi-End Job Cmd3-Go Back © Cmd19-Delete this profile

 

Put any character beside the division(s) you want to include.

Press Enter after making changes on any screen.


Assign Accounts to DOC Departments

The 2-character DOC department codes must be set up using Maintenance
Option 3, Maintain DOC Departments. If you have not set up your codes,
Cmd3 to go back to the Maintenance Options screen and choose Option 3.

Account Assignment Screen

ABC COMPANY
Division: K

Daily Operating Control x1570-108

Assign Accounts to DOC Departments

Account # Title

£3200
3202
3202
3203
x3204
K3250
K3260
3280
3290
3310
R311
K3312
K3313
13314

Begin next screen with Account # K3320

NEW EQUIPMENT SALES
SALES NEW WFE

SALES NEW MASSEY COMB
SALES NEW MASSEY FERG
SALES NEW OUTDOOR POWER
USED EQUIPMENT SALES
INVENTORY ADJUSTMENT
RENTAL-EQ REVENUE,
RENTAL EQ SALES

INT PARTS-OTHER

INT PARTS-WHITE

INT PARTS-COMBINE

INT PARTS~TRACTOR

INT PARTS-OUTDOOR

Cmdi-End job cmd3-Go Back

02,
o1
o1
o1
on
02
o1

Dept # Title

New Vebicles
New Vehicles
New Vehicles
New Vehicles
New Vehicles
Used Vehicies
New Vehicles

 

All of the general ledger sales accounts for all divisions will be displayed.
Fill in the department code for each account. To see the next page of
CC


X15-7 DAILY OPERATING CONTROL REPORT [=]

accounts, press Enter.
After making changes on any page, press Enter to record your changes.

To skip to a certain account, change the account number at the bottom of
the screen: "Begin next screen with Account #

Unassigned Accounts

The system will assign accounts without department codes to a
"Miscellaneous Account” department when the profile selection is by
department. If the profile selection is by account, then unassigned accounts
will always print. It is best to assign all your accounts to departments.

To Change an Account Assignment
Type over the existing code. To delete a code, field exit through it.

Cmd3 to go back to the Maintenance Options screen.

 


[| X15-7 DAILY OPERATING CONTROL REPORT

Maintain DOC Departments

The DOC departments which you set up here are used by the Daily
Operating Control Report only.

Department Maintenance Screen

ABC COMPANY Daily Operating Control X1570-107
Division: K Maintain DOC Departments

Title

New Vehicles

Used Vehicles
Service

Rental and Leasing
Parts Counter
Body Shop

Service

Chemicals

Cmél-End job cmd3-Go back

 

You may have up to 15 different departments. Fill in the department code
(2 characters) and the department title. Press Enter, The departments will
arrange themselves in order by code.


X15-7 DAILY OPERATING CONTROL REPORT [=]

Changing a Code
Type over the existing code and title. To delete a code, field exit through
the information.

Make a print screen of the DOC department codes before you take option
2 to Assign Accounts to DOC Departments. Cmd3 to go back to the
Maintenance Options screen.


[«] X15-7 DAILY OPERATING CONTROL REPORT

Maintain DOC Legends

Ten lines of 80 characters are available for a customized, descriptive
legend, which can be printed on your own Daily Operating Control
Reports, if desired. Legends are not available for the Basic Report.

D From the Maintenance Options Menu, select option 4, Maintain DOC
Legends.

AGR EQUIPMENT SALES Daily Operating Control 170-103
Division: A Maintain Legends
DOC Profile Name: _____ Enter name or select from list
Current Profiles (

Select (any character)

— BANKDOC «NW Bank DOC - Paula

Customized legends are not
available for the Basic Report

Cmd1-End Job Cmd3-Go Back

 

 

 

 

To maintain a legend for a profile, enter any character beside it. You
don't need to press [Enter].

 

RELEASE 2.2 LO


A&R EQUIPMENT SALES Daily Operating Control x1570-109
Division: A Maintain Legends

DOC Profile Name: BANKDOC
Description: NW Bank DOC - Paula
begend:

12345678901234567890123456789012345678901234567890123456789012345678901234567890

 

 

 

 

 

 

 

 

 

Cmdi-End Job cmd3-Go Back

 

O Type a legend that will help people understand your Daily Operating
Control Report.

CO Press [Enter] to record your changes. You will return to the Maintain
Legends selection screen. Press Cmd3-Go Back until you return to the
entrance screen, where you'll find a prompt to print the legend on the
selected report(s), if desired. The entrance screen is illustrated below.


AGR EQUIPMENT SALES Daily Operating Control 1570-102
Division: A Select DOC Reports

Select DOC Report Profile Ending Date (090197 To 012998)

— Basic Report 12998

— -BANKDOC NW Bank Doc - Paula 12998

Legends to print on reports chosen (except Basic Report): ¥
Enter any character beside each desired report, and press ENTER.

(md1-End Job  Cma8-Maintenance Options

0 Change the default on "Legends to print on reports chosen (except
Basic Report)" from"N" to "Y". The legend is printed at the bottom of
the report.

Note:
The customized legends are not available for the Basic Report.

The following is a sample Daily Operating Control Report illustrating the
Legend at the bottom:
LU


ARR EQUIPMENT SALES DAILY OPERATING CONTROL Date 1/29/98 age S
Bivigson: & Profile: | BANKDOC Time 16.53.58 1570-9

+ Expenses as of 1/29/98
Title Account Balance Gross Budget Budget &
AUDITING, LEGAL 5 COLLECT AGRE

75.00
DATA PROCESSING

57.08-

51505
MISCELLANEOUS

21.74-
Wiscellaneous accounts 97-02

17235194
aaigai az :

+ Total sxpenses terree+ 97.02
37235.94
31298142

 

MA aNITa Aaa asta ata taIAaTIaAI ATA MaaLaagAIaa da
22332302292222279222292222222222922272222222222222292222720222222222222222222222 :
5553353333 3333333325333339933953915333395333331939533332933333393335329399999333
1 Soc ga C0T ROOT 00 TG UTDUTSU OTC O TOURIST TOTO TTI TIOOI II
eR ACCRA ARNE ARN IRIN EOM SETAE
PPPPEPERPEBDeCPPPPPPPEDEPPOPECPPEPPERPEPPEPPPPPDEDSERDEPPEPPPDDEPPPEEPPPDOEDPEDS

 

‘TEEEECESETEVEE¢FSS0 E0000 20 0EE EEE UEEYYYESEYS PPYEEYYEEEEEEE EL PYTE PETE EEEEEEEESEE

 

 

Se ACCOUNTING


SAMPLE REPORT

ARC COMPARY
Division: &

ore sales
Title
NEW HONDA SALES
a7 Unses
176836 value
NEN OTRER SALES

23 Unite i

98874 valve
wrNew sales

30 vaite

275310 Value
SERVICE SALES

This is a sample section from the Daily Operating Control Report:

as of

siigya7 eee
Period
Teday

Recount
53200
Inventory
Inventory y79
3202
Inventory
Inventory
wa
Inventory
tnventory
¥3203

DAILY OPERATING CONTROL

sales
27090.09
120050.80
575020.99
576.09
12040.50
24050.00
2068.00
132091.30
599970.90
385.00
10875.90
25789.85
985.00
10675.90
26739.85

Basic Report,

Gross
2609.00
13205.58
7502.09

500.00
ing0.09
1493.70
3308.00
14285 .58
9945.72

197.00
2135.18
5157.57

157.08
2135.18
26789.e5

Gross 4
10.6
1.e
10.0
23.8
2.
6.
ae
10.
°
20
20.
20

vaizs Gross/unic
2 1040.50
22 1200.50
60 958.36
500.00

216.00

240.61

1103.00

840.29

393.41

pace

20000

130000.
sooen0.


12000.
25000.
250.
7506.

36003

3/39/97
Time 15.14.38

sales Budget
4563.
136800.
560900.
1900.
30000.
59000.


60.

co
60
co
20
00
99
29
20

Pege 1
1870-88

Budget ©
593.6
87.6
192.8
97.8
40.
40.
ne
an
96.
246.
a8.
203.

 

Below is a sample Totaling section from the Daily Operating Report:

 

+ Total sales
4 Unite in Inventory

31830.00
347242.20
679842.35

3783.00 11.9 3
18825.76 12.8 27
$3206.76 41.81

3261.00
695.08
728.77

6296.68
188500 .09
730000.09

296810 value of Inventory

 

CC

 


Below are samples of other sections on the Daily Operating Report:

1 cash as of 5/16/97 r+
Title Account, Balance
CASH ON HAND x2990 31,262.02
CASH IN BANK x10920 33,772.90
"Total Cash +»: 25,153.02

cTt Recoivables as of 5/20/97 +="
Tine Account Balance

ACCOUNTS: RECETVABLE xan19 31,280.70
WARRANTY & SUPPLIER REC K1160 2,660.95
+ Toral Receivables +++ 33,913.65

se payables as of §/20/57 ++
nitle Account: Balance
NOTES PAYABLE NEW EQUIP K2200, 182,991.35
- Total Ficored Payables 182,991.35
TRADE PAYABLES x2210 37,074.87
+ Total Other Payables * 37,076.87
- Total Payables . 700,065.22

ser payeoll as of 5/20/97 +++

Tile account Balance
+ Total Payroll s+s+rese

Current
6,574.30
8,160.95

25,235.25

Due Today
29,195.70
29,195.70
47,074.82
17,074.87
46,250.57


30 pays
10,309.50

$00.00
40,809.50

10 vays

60 Days
453.17

453.17

50 Days & Over
23,913.73

33,913.73

Future
153,379.48
242,770.88

365,150.36


w0t Work-in-precess as of
tele
PARTS SALES-COUNTER
PARTS SALES-SHOP
MISC PARTS SALES
GAS SALES
arts
SHOP LABOR
sn=Service
+ otal Sales *s1eeseeen
+ Total Discounts *tere*
+ Total Work-in-Process

FREIGHT

FELEPHONE - TELEGRAPH

urtnariss

EQUIPMENT REPAIR

5420/97 +6

Account,
3320
3340
3369
3362
PR
3370

5149/97 +8

Account
1853

Balance
573.26
1122.76
208.65
921.96
2926.55
827.00
827.00
3,987.10

3,987.10

‘Today

wr
ym

wero
yD

erp
yoo

4027.23

9925.99

oo2r.17

2319.90

‘Today
vp
yD

13665.34

389871.14

Gross Budget

Budget &

See the next page for field definitions.

 
CC


X15-7 DAILY OPERATING CONTROL REPORT [=]

### Fields & Descriptions

Sales Segment
Sales as of (Ending Date}. ...

Title Title of General Ledger account or
department.

Account/Department Account number (if not departmentalized) or
Department number.

Period

Today Today's totals.

MTD Month-to-date totals.

YTD ‘Year-to-date totals.

Sales The total sales.

Gross Sales minus cost of sales.

Gross % The percent of gross margin for the sales.

Units Number of Units sold.

Gross/Unit Gross divided by the units sold.

Sales Budget The budget as defined by the user in
Budget Maintenance (X15-4). Today's
budget is calculated by dividing the MTD
budget by 20 days. YTD budget is
calculated beginning with the month
your fiscal year starts. See Security
Maintenance (X6-6).

Budget % Sales or Gross Profit divided by the budget.

This depends on the selection made on the
Maintain DOC Profiles screen. See the
section titled Department Selection Screen.


[=| X15-7 DAILY OPERATING CONTROL REPORT

Units in Inventory Number of units in each inventory account.
For the unit count to be correct, there must
be a valid sale account in the “Account 1” of
the inventory account at General Ledger
Maintenance (X14- 2).

Value of Inventory Total cost of the inventory. There must be a
valid sale account in the "Account 1" field
of the inventory account at General Ledger

Maintenance (X14-2).
Cash Segment
Cash as of (Ending Date)... .
Title Title of General Ledger account.
Account Account number.
Balance Balance of cash on hand. (
Total Cash Cash balance for Sales Analysis period.
Receivables Segment
Receivables as of (today's date) .. .
Title Title of General Ledger account.
Account Account number.
Balance Balance of Receivables.
Current Current amount owing.
30 Days Charges 30 days past.
60 Days Charges 60 days past.
90 Days And Over Charges 90 days and over.

RELEASE 2.2 Cu


X15-7 DAILY OPERATING CONTROL REPORT [=]

Payables Segment
Payables as of (today's date)...
Title Title of General Ledger account.
Account Account number.
Balance Balance of Payables.
Due Today Balance of Payables due today.
10 Days Balance of Payables in 10 days.
30 Days Balance of Payables in 30 days.
Future Balance of Payables beyond 30 days,
Payroll Segment
Title Title of General Ledger account.
Account Account number.

Work-In-Process Segment
Work-In-Process as of (today's date)...

 

Title Title of General Ledger account or
department.

Account/Department Account number (if not departmentalized) or
department number.

Balance Balance of today's Work-In-Process.

Total Sales Balance of total sales.

Total Discounts Balance of total discounts.

Total Work-In-Process _ Balance of total Work-In-Process.

Expenses Segment
Expenses as of (Ending Date) .. .
Title Title of General Ledger account or
department.
Account/Department Account number (if not departmentalized) or


[=| X15-7 DAILY OPERATING CONTROL REPORT

Period

Today

MTD

YTD
Balance
Gross Budget

Budget %


Department number.

Today's totals.

Month-to-date totals.

Year-to-date totals.

The total expenses.

Amount allocated in Budget Maintenance
(X14-4)

Expenses or Gross Profit divided by the
budget. This depends on the selection made
on the Maintain DOC Profiles screen. See
the section titled Department Selection
Screen.

LC

## CHAPTER X15-8

COMPARATIVE INCOME STATEMENT

### Introduction

The Comparative Income Statement is both an expansion and a refinement
of the Sales Analysis Report (X15-1). The statement may be run for
Month-to-Date or Year-to-Date, by department, for single or combined
divisions. Budgeting information can be included. Year-to-Date figures
are for the current fiscal year. Balances are taken from u.CUA, which
stores current transactions; therefore, it is for open months only.

### How To Run

From Menu X15 select option 8 for the Comparative Income Statement.
The financial security code is required.

The entrance screen looks like this:

## X15-8 COMPARATIVE INCOME STATEMENT

NW EQUIPMENT SALES & RENTALS
Division: A

Month-to-Date or Year-to-Date
Department Mask

Other divisions (Y/N)
Compared with Budget (Y/3)

Select one open month:
Novenber
December
January
February
March
april
May
dune
July
August

October

Month-to-Date or Year-to-Date (M/Y) : M

Comparative Income Statement

1995 +
1995 +
3996 :
1996 :
1996 :
1996 +
1996 :
1996 :
1996 ;
1996 :
September 1996 :
1996 :

1580-101

 

The default is M4 for Month-to-Date. If you want Year-to-Date, type Y.

Department Mask

: XXXXXXXX

The 8 X's represent the 8 possible characters in a general ledger account.
Replace the "X" in the same position as the department code with a "*" for
a summary or the department code if you want only one department.

Example: The 6th position of the general ledger account number is
reserved for a department code. For a summary of all accounts with a
Co


X15-8 COMPARATIVE INCOME STATEMENT [2]

character in the 6th position, the mask would be: XXXXX*XX. For all
service accounts, the department code is a "2" in the 6th position. To run a
Comparative Income Statement for the service department, the mask
would be: XXXXX2XX.

Other divisions (Y/N) : N
The default is N (No). If you want to include one or more other divisions,
type Y (Yes).


[| X15-8 COMPARATIVE INCOME STATEMENT

Compared with Budget (Y/N) : N
The default is N. If you want budget information to appear on the report,
type Y.

Select one open month:
All open months are displayed, starting with the oldest month. The oldest
month is selected by default.

If you typed Y to include other divisions, the Division Selection Screen
will appear. It looks like this:

Bellingham Car & Truck Comparative Income Statement 1580-102
Division: A DIVISION SELECTION

To incluge other divisions in a Comparative Income Statement, {
place any character beside the divisions to include.

X AB BURKINS, INC. © CARLSON EQUIPMENT
X A E ELISABETH'S TINY STORE X F FRANKLIN & SONS

Omdi-Ené Omd3-Go back

 

Type any character beside the divisions you want to include on the
Comparative Income Statement. In this example, divisions B, E, and F

RELEASE 2.1 LU


X15-8 COMPARATIVE INCOME STATEMENT |

have been selected.

Do this: Press Cmd3 to go back to the entrance screen.

Or this: Press Cmd1 to end the job and return to the Financial
Menu.

Or this: When you have selected the divisions, press Enter.


[ «| X15-8 COMPARATIVE INCOME STATEMENT

The Final Verification screen will appear. It looks like this:

BELLINGHAM CAR & TRUCK CO. Comparative Income Statement X1580-103 3
Division: A FINAL VERIFICATION

You have selected:

MrD/YTD M
Department spOCCOK
Division(s) A
Budget comparison? 8

Cmdi-End Cmd3-Go back Enter-Continue

 

Do this: Press Cmd3 to go back to the entrance screen.

Or this: Press Cmd1 to end the job and return to the Financial
Menu.

Or this: Press Enter to continue. The Comparative Income

Statement will be placed on the job queue.

RELEASE 2.1 LU


BELLINGHAM CAR & TRUCK CO.
BELLINGHAM, WA A

x1580-:

an

XXX,

Acct #

23200
an240
3250
A2310
3320
83330
53350
az6o

rele

NEW TRACTORS
neg egorPMENT

USED TRACTORS-B0UTP
‘PARTS-INTERNAL
PARTS-COURTER
PARTS-SHOP

‘TIRES ANO TURES
MISC SALES

+) TOTAL SALES **
NEW TRACTORS
NEW EQUIPHENT
USED TRACTORS-EQUIP
PARTS-COUNER
‘PARTS-SHOP
‘TIRES & TUBES cos
misc. sanes


This is an example of a Comparative Income Statement without budget
figures:

Comparative Income Stacarent. Date 12/29/89 Pace
For Peried Ending 12/29/89 Time 7.52.01
Selected: Month-to-nete Department mask:
without auégeted Figures
Current Year - Month Prior Year - Month variance
dollars 8 eotal dollars 4 total —«$ variance % variance
zoiiii.22 100.16 201111.22- —100.09-
814.00 88.02 aeie.09
1200.90 21.98 1200.06
322.79- 322.75

 

 

20014..00 200799.43 190788.43-

3292.00 3791.00
3000.00 1900.00

SERVICE LAEOR-CUSTONER

+7 cost oF Goons SLD ** 4291.00 4281.00

GROSS MARGIN +++
ADVERTISING
WARRANTY

5723.00 200799.43 195076.43-

 

COMPENSATION-SALESMEN


BELLO

INGHAM CAR & TRUCK 00.

BELLINGHRY, WA a
X1S80-42

xeGGOUR

acct,

5520
6530
6540
6560
6580
agseo

4 tele

COMPENSATION-OFF SMPLOVEE
COMPENSAPION-OTHERS
(COMPENSATZON-PARTSHEN
EMPLOYEE BENEFITS-TAXES
PREIGHT

SHOP EXPENSE

+ TORAL Expenses ++
OPERATING PROFIT +++
CASH DISCOUNTS EARNED
INTEREST INCOME
FINANCE RESERVE INCOME
GAIN LoSs-FIXED ASSETS

"> OTRER INCOME *+

NET INCOME BEFORE TAXES + +++

Comparative Income Statement
For Period anding 12/29/89

Selected: Month-to-pate

Date 12/23/85 Page
Tine 7.52.01
Department Mask:

without Budgeted Figures
Brier Year - Month Variance
totals variance & varience

arrens Year ~ Month
dollars & total,

5723.00 200799.43

3723.00, 200799.43

dollars

195076.43-

195075.43~

 
Co


And an example of the report with budget figures:

BELLINGHAM CAR & TRUCK CO. Conparacive Income Statement Dace 12/29/89 page 1
BELLINGHAM, WA a For Period Ending 12/29/89 Pima 9.32.01, X2580-40

Selected: Month-ro-Date Department mask:
SERKERK
With Budgeted Figures
current year ~ sm ~ Prior Year = MTD - variance -

Ticle Actual Budgeved —@ var. Actual Budgeted =H var. Actual Budgeted

NEW TRACTORS 202111.22 100..00-

NEW EQUIPMENT: 3814.00,

USED TRACTORS-EQUIP 1200.00,

PARTS-INTERNAL 321.00- 100.00-

PARTS-COUNTER,

PARTS-SHO?

‘TIRES AND TUBES

MISC SALES

### Service Labor-Customer

 

TOTAL SALES ** 30014..00 321,00- 219.60- 200799.43 . :
NEW TRACTORS

NEW EQUIPMENT 3291.00

USED TAACTORS-80U1P 1900.00 -
PARTS-WHOLESALE

PARTS-INTERNAL

PARTS-COUNTER

PARTS-SHOP

‘TIRES & TUBES Cos

MISC. SALES :
SERVICE LAZOR-CUSTOPER

 

"+ cost OF coops soup ** 4291.00

GROSS MARGIN +++ 3723.06 200799.43
ADVERTESING E
WARRANTY :
‘COMPENSATION-SALESHEN

 


co

 

BELLINGHAM CAR § TRUCK CO. Comparative income Stacenent Date 12/29/89 Page 2
BELLINGHAM, WA a For Period Eading 12/25/89 Time 9.32.01 11520-4a,
Selected: Month-to-Date Department Mask: — XRXKKXXK

With Budgeted Figures
current Year - Price Year -

Variance ---

acct # Title Actual Budgered Budgeted var. Actual Budgeted

A6S20COMPENSATION-OFF EMPLOYEE

6530 COMPENSATION-OTHERS

6540 COMPENSATION PARTSMEN

ASS60 EMPLOYEE BENEPITS-TAxes

ASS80 0 FREIGHT

AS590—-SHOP_ EXPENSE

+ TOTAL EXPENSES ++

vet OPERATING PROFIT #++ 5723.00 200799.43
DISCOUNTS EARNED

AS210 “INTEREST INCOME

AS220 PENANCE RESERVE IKCOME

S280 GATN LoSS-FIKED ASSETS

OTHER INCOME ++

s+ NET INCOME BEFORE TAKES **++ . 200799.43

 

The titles of the total lines are provided by the system.
Title: Description:

** TOTAL SALES ** Total of all accounts of type = S
(Sales).

** COST OF GOODS SOLD ** Total of all accounts of type = C

(Cost).

*#* GROSS MARGIN *** TOTAL SALES minus COST OF
GOODS SOLD.

** TOTAL EXPENSES ** Total of all accounts of type = E

RELEASE 2.1 LO


X15-8 COMPARATIVE INCOME STATEMENT [J

** TOTAL EXPENSES ** Total of all accounts of type = E
(Expense).

*** OPERATING PROFIT *** GROSS MARGIN minus TOTAL
EXPENSES

** OTHER INCOME ** Total of all accounts of type =I
(income).

*** NET INCOME BEFORE OPERATING PROFIT plus

TAXES #** OTHER INCOME.

Session Date

The session date is the current system date unless you have changed the
date at your terminal.

To change the session date: at a DIS menu, type: DATE mmddyy

(Enter)(mm = month, dd = day, yy = year). If the month has been closed,
the totals will be for the entire month.


[=] X15-8 COMPARATIVE INCOME STATEMENT

The statement is divided into 3 sections, Current, Last Year, and Budget.
The figures in each section depend on whether the statement was
requested for Month-to-Date (MTD) or Year-to-Date (YTD).

For:
MTD

Section:
Current

Last Year

Budget

Current

Last Year

Budget

Includes:

Actual dollar amounts of all transactions
which have been posted from the 1st of the
session month through and including the
session date.

Total of all transactions which were posted
for the entire session month during the
previous year.

Actual dollar amounts budgeted for the
entire session month for the current and
previous years.

Actual dollar amounts of all transactions
which have been posted from the first of the
fiscal year through and including the session
date.

Total of all transactions which were posted
for the previous fiscal year through and
including the end of the session month as of
last year.

Total budget for all months from the first of
the fiscal year through and including the end
of the session month for the current and
previous years.
CU


X15-8 COMPARATIVE INCOME STATEMENT |

Calculations

The percentages and variances are calculated as follows:

 

Without Budget Figures
dollars

% total = --------- x 100
total dollars

$ variance = current year dollars - prior year dollars

$ variance
% variance = ---------------------- x 100
prior year dollars

With Budget Figures

Budget $ variance
% variance = ------------------- x 100
Budget dollars

curr.yr. $ - prior yr. $

actual % variance = -------------------------- x 100 (rounded to
prior year $ nearest 10th of
percent)


Notes:

## CHAPTER X15-9

FORMATTED FINANCIAL STATEMENT MENU

### Introduction

Some vendors require financial information to be submitted in a certain
format. Previously, this required running a financial statement and writing
the information manually on the form provided by the vendor. All general
ledger figures would be placed in the proper general ledger block on the
form provided by the vendor.

With the Formatted Financial Statement feature, you can apply the
Financial Format diskette and assign your general ledger accounts to the
proper block of the form provided by the vendor. When the assignments
are made, you can run a financial statement in the format that the vendor
requires,

If financial information is required in one format for the main line vendor
and another format when reporting to a short line vendor, format scan be
set up for both vendors.

Check with DIS for a list of currently available financial formats.

## X15-9 FORMATTED FINANCIAL STATEMENT MENU

OVERVIEW OF THE FORMATTED FINANCIAL
STATEMENT MENU OPTIONS

The Formatted Financial Statement Menu contains four options:

X159-1

X159-2

X159-3

159-4

Formatted Financial Statement:

Certain vendors require that financial information be
submitted to them in specific formats. Formatted Financial
Statement allows you to run a financial statement in the
format required by the vendor.

Account Assignment Maintenance:

In this job, you will assign your general ledger account
numbers to standard account numbers matching the
standard account numbers provided by the vendor on the
required form. Account assignments must be made before a
Formatted Financial Statement (X159-1) can be run.

Apply Financial Statement Format:

The form required by the vendor has been placed on
diskette. In this job, you apply the financial format on the
diskette or tape to your files. This is the first step in the
process.

Remove Financial Statement Format:
This job removes a financial statement format.

## CHAPTER X15-10

GENERAL LEDGER ANALYSIS REPORT

### Introduction

The General Ledger Analysis Report provides an unadjusted trial balance
for the oldest open General Ledger month. It also lists a summary of
month-to-date and year-to-date information for every General Ledger
account for the past 24 closed months. It can be run for one division at a
time.

Note:

On the report, negative balances are underlined. Using this convention
allowed more information to be placed on the report than if minus
signs or parentheses had been used.

 

To run the General Ledger Analysis Report go to Menu X15 and take
Option 10.

COMMAND
{e) DIS Corp.

. Sales Analysis Report
, Financial Statement

. Departmental Personnel analysis Report
. Budget Maintenance

. Budget Review

- Daily Operating Control Report,
8. Comparative Income Statement
Formatted Financial Statement Menu
. General Ledger Analysis Report

. Return To Accounting Menu

Ready for option number or command,

## X15-10 GENERAL LEDGER ANALYSIS REPORT

 

Since the report is always based on the oldest open month, it will not be
necessary to select a specific month for the report. After you pass through
the security gate, the following screen will appear.

ABC-AG,AUTO,CONS & TRUCK CO. GL Analysis Report X2S§A0-102 1
Division A Parameter Screen

Show period totals as MID or YID amounts

Use 13th month adjustments to calculate 12th month... .

¢ndi-Cancel Job

 

Press ENTER after you have filled out the screen. The report will have a
different section for each account type. The sections will print in the
following order: Assets, Liabilities, Sales, Cost of Sales, Income, and
Expenses. There is a recap of the section totals at the end of the report. See
below for an example of the Income section of the report and the Recap
for all the sections.

RELEASE 2.1 LO


 

ABC-AG,AITO,CONS & TRUCK CO. Genera} Ledger analysis Report. DATE 12/10/89 PAGE 1

BELLINGHAM, WA a MID Ending May, 1969 wimz 8.40.48 x15A0-401
‘other Income:

05/89 Account, 03/89 02/83 O1yes «12/88 «11/88 oyeR 03/88 a8B O78 veR 0568

03788 02/88 «= OLveE 12/87 2/87 10787 09/87 03/87 1/8768? se7

® . ‘ ‘
+00 AsoOD

CASE DISCOUNTS EARYED

+00 AS210
INTEREST INCOME

00 AS220 :
GAIN LOSS-PIXED ASSETS

‘Total Other Income:

Recap Totals

Assets 104885.94

Liapilitit 34988.16
Sales 99761.27
Cost of Sales 36677.46

Other income -00 ~
Expenses: 9478.62

 

Grand Totals 161042.23, 94749.63,

 


Notes:

RELEASE 2.1 oe


SOURCE DOCUMENT INQUIRY

### Introduction

Source Document Inquiry allows you to display all information included

on any source document entered for:

= any open General Ledger month.

= any closed General Ledger month for which months of history are kept.
See Months to Keep in General Ledger Account Maintenance (X14-2).

### How To Run

## CHAPTER X16-1

From the TRANSACTION MENU (X1-6), select option 1, Source
Document Inquiry. The Source Document Inquiry screen displays
transactions:

A & R EQUIPMENT

Division L

ID Date
qiy14ss1
aiytasst
11/06/91
14/06/81
11/06/91
11/06/92
11/21/91
qyaayst
11/05/91,
11/05/92,
21/05/81
11/05/91
41/05/91
11/08/91
14/06/91
11/06/91

Mth
aw
1
nh
1
re
12
at
a
a.
a.
i
a
a
at
a.
12

Start Next Page With: Document
(mdi-End job, Cmd6-Nore Fields, Roli-Page

Document D/C

BOUNDARY
BOUNDARY

BUSH HOS
c-F
CF
cr
cr
CARLSON
CARLSON

¢

c
D
c
>
c
D
c
D
c
D
c
D
c

SOURCE DOCUMENT INQUIRY

Account
1240
4132
L240
1132
£240
1132
1240
1132
1240
2132
2240
L658
L240
L658
1240
1427

Amount Description Addr# vunit#
87.
a7.
27.
27,

6.
6.
ao.
10.
22.
22.
31
147.
134,
+90
56.
00


a7
17
35
35


X16101-01

00219

04851

BO4B51

Bo4aes1

801936

01955

co19s5

06447

## X16-1 SOURCE DOCUMENT INQUIRY

Note that at the bottom of the screen you can request a specific document

number.

You can press [Cmd6] to see more fields.

® & R EQUIPMENT
Division L

SOURCE DOCUMENT INQUIRY

Description addr # Unit# Name Due Date

B00219

BO48S1

BO4851

Bo4aeS2

BOL936

cO19ss

cO19s5

06447
BA6037

BOUNDARY AUTO PARTS 2/10/92

BURLINGTON FORD NEW HOLLAND 11/10/92

BURLINGTON FORD NEW HOLLAND 11/10/91

BURLINGTON FORD NEW HOLLAND 12/10/91

BUSH HOG ALLIED PROD CORP, 11/30/92

CONSOLIDATED FREIGHTWAYS 11/10/92

CONSOLIDATED FREIGHTWAYS 11/10/91

CARLSON STEEL & FENCE SUPPLY 11/10/91

Start Next Page With: Document
Cmdl-End job, Cmdé-More Fields, Roll-Page

x16101-02

Discount

 
Lo


 

### Fields & Descriptions

ID Document classification code, set up in
Point of Sale Document Classification
Maintenance, X522, or entered at Create
Source Documents.

Date Date of the transaction.

Acct# D (debit) or C (credit) to the General Ledger
Account number.

Amount Dollars and cents involved in the
transaction.

Description Description of the transaction.

Addr# Address # of the customer in Receivables.
Address # of the vendor in Payables.
Traded-on stock# for a Units inventory
account #.

Due Date Date the amount is due in Payables.

Warranty expiration date in a Units sale.
Date of sale in Flooring transaction, if sold
before the due date entered originally.
Discount Discount on the transaction, in Payables.
No decimal displays. EX: 500 = $5.00
Warranty code for Units sale.
EX: 4 hours 15 minutes = 425
Uniti# Unit stock number.

Notes:

RELEASE 2.1 a

## CHAPTER X16-2

TRANSACTION REPORT WRITER

### Introduction

Transaction Report Writer allows you to:

= request a report of different types of transactions for open months, and
in some instances, closed General Ledger months.

= create and request a report according to your specifications.

Note:

To set up your report specifications, you will want to know which files
to use. Check Chapter X1-6 for the Transaction Report Writer
specifications and example before proceeding.

## X16-2 TRANSACTION REPORT WRITER

### How To Run

From Menu X16 select option 2 to run Transaction Report Writer. You
will see the first screen as shown below:

### Generate Report From A Transaction File

To produce an existing report, enter the report name

fo create a new set of report specifications, press enter/rec adv

MD 1 to end job

FOR A NEW REPORT: Don't type anything, leave the field blank. If you
are requesting a new report, you will receive 2 message, "File Build
Procedure Executing." It will take a few seconds for the next screen to
appear.

FOR AN EXISTING REPORT: To change an existing report, refill in the
parameters, select and sort screens. The report name may stay the same. If
you requested an existing report, it will be generated and the menu return.
The job is complete.


 

The example screens in this chapter can be used to produce a Sales Tax
Report for your own company.

The report name used below is ST12. This is the report specification to
produce a listing of transactions for the month of December. If you wish to

use this report, recreate the report specifications for each of the twelve
months.

The Specify Parameters screen appears. See the example below:

ABC COMPANY GENERATE REPORT FROM TRANSACTION FILE
BELLINGHAM, WA *Specify Parameters*

Report name ST22
Entex report title FOS SALES TAX - DEC.
Select the transaction file
To report:
01 General ledger
Enter no. 01 Payables
05 Receivables
Receivable hist
07 Whole goods
08 Whole goods sld

Enter number of subtotals desired 02

Enter ¥ for a summary report (only subtotals and final totals)

cmdl to end job

 


 

‘When your selections are complete, press [Enter]. The fields are described

below:
Field: Definition: Limits:
Report Name Identifying number or name for

report. 4 characters

Note:

You must use 4 characters, no more, no less.

 

Enter Report Title Identifying description of the report 50 characters

Select the The number of the file listed on the
Transaction File screen that you want to access, 2 digits
Enter number of Number of subtotals you wanton —2. digits

Subtotals Desired _the report.

Enter Y fora Type a Y for a summary report. Y only
Summary Report (No detail transactions will print, only
totals.)

RELEASE 2.1 Lo


The Field Selections screen is displayed. See below:

ABC COMPANY GENERATE REPORT FROM TRANSACTION FILE
BELLINGHAM, WA E *Field Selections*

Field No. Operator Constant Field Table- ------ *
123456789012345 Mumber Name Length
D 01 IDortype 2
3 02 Post date 6
03 Document # 10
04 DorCcode 1
05 Account #

06 Amount

07 Description

08 Address &

09 Due date

10 Discount

11 Stock #

12 Delete code

13. G/L month

os
03

 

EQ
EQ
EQ
zQ
EQ
2
zQ
EO
EQ
EQ
EQ
EQ
EQ
BO
EQ

123456788012345 cmd? to continue to sort specification
Use | as a ‘wild card’ character Cmdl to start report
Possible operators are EQ,NE,LT,GT,LE, and GE

 

### Fields & Descriptions

Field: Definition: Limits:
Field No. One of the Numbers in the field table 2 digits
on the right hand side of the screen.
Press FIELD EXIT.

Operator Either press FIELD ADVANCE to leave
the OPERATOR at EQ, or type in the
operator of your choice. Possible
operators listed at bottom of screen. 2 characters


 

Constant Type in the constant for the chosen 1 character
field. Check the APPENDIX if you need each
more information for these selections.

In our example, we have selected Field 13 equal to D. This specifies that
we wish only transactions from the open month of December.

We also selected Field 05 equal to !3!!!111!. This specifies that we
wish to include only transactions from G/L account numbers that have a 3
in the second digit. In our sample company, accounts with the number 3 in
their second position are sales accounts.

those transactions which have a #* in the ninth and tenth position of the
document number. These document numbers are generated automatically (
by Point of Sale invoice numbers. :

The exclamation marks used in the two fields above are wild card
identifiers. When used in the document number field, the wild cards will
allow acceptance of all transactions with #* in the ninth and tenth position
regardless of what characters come before it. If we had left the
exclamation marks off, we would get transactions that only have #* in the
document number. If there were any other characters in the document
number, the transaction would not be included on the Teport.

### Options

O Press FIELD EXIT. Type in another FIELD NO., OPERATOR, and
CONSTANT to make another condition to be met.

O Press ENTER. The condition(s) you enter must all be met for a
transaction to be included on the report. When you press ENTER, the

RELEASE 2.1 LO


 

screen clears but remains at the Field Selection screen. If you enter
conditions on this "second" screen, the report will look for all
conditions on the first screen OR all conditions on the second screen.
‘You may use as many screens as you need.

O Press CMD 2 at an empty Field Selection screen to advance to setup
sorting guidelines.
OR
Press CMD 1 to start the report.

If you pressed CMD 2, the Specify Sorting Order screen appears. See
below:

ARC COMPANY GENERATE REPORT FROM TRANSACTION FILE
BELLINGHAM, WA *Specify Sorting Order*

Field No. Sort order----* Field Table-
123455789012345 Number Name
07 1 0 ID or type
as 22222222 02 Post date
03 3333333333 03° Document #
04 Dor ¢ code
05 Account #
06 Amount
07 Description 1
08 Address #
09 Due date
10 Discount
121 Stock #
12 Delete code
13° G/L month

123456789012345

Gmdl to start report

 


 

### Fields & Descriptions

Field Number Type in the field number you want sorted.
Use one of the numbers listed on the right
side of the screen.

Sort Order Type the order you want to sort by. For
example, if you want to sort by description
first, put 1 in the sort order field. You will
need as many 1's as the are characters in the
field you are sorting.

In our example above, we are sorting first by the third character in the
description field. Transactions from Point of Sale generate descriptions (
starting with the sales code in the first two positions, tax code in the third
position, and discount code in the fourth position. By sorting first by tax

code, we will have all similar tax code transactions grouped together on

our report with subtotals given for each code.

Our sample report will next sort by G/L account number. Since we
specified two subtotals on our parameter screen, we will get subtotals for
each G/L account within each tax code,

Within each G/L account, we will next have our transactions sorted by
Document number. Since we specified only two subtotals on our
parameter screen, we will not get subtotals for each document number.

When you have set up your sort order, press ENTER. A blank sort screen
displays. Then press CMD | to begin the report.

If you would like to see another example of how a report is set up, see

RELEASE 2.1 CU

### How To List Existing Report Specifications

O At the bottom of a menu, type in the LISTLIBR command:
LISTLIBR RS,ALL, PROC, dislibr, USER, NOPAGE, , DIRINFO

dislibr represents the name of your DIS library - usually LIBRARY.
O Press Enter. A report will print listing all Transaction Report

Specifications currently on your system. If you wish to delete any
Report Specifications, follow the instructions below.


 

### How To Delete A Report Specification

Note:

This delete process is used to delete an existing report specification
which is no longer used.

 

At the bottom of a menu, type in the REMOVE command:

REMOVE RSname, LIBRARY, dislibr

(name represents the name of the report to delete and

dislibr represents the name of your library to delete.) (

For example, to delete a report named STAX from the library called

LIBRARY, you would type in:
REMOVE RSSTAX, LIBRARY, LIBRARY [Enter]

RELEASE 2.1 Lo

## CHAPTER X16-3

SALES TAX REPORT

### Introduction

The Sales Tax Report includes the detail and summary (or summary only) of all
transactions that originated in Point of Sale or Create Source Documents that
involve sales accounts plus selected non-sale accounts selected as “Use in Tax
Report” in Account Maintenance (X14-2). You can optionally exclude up to 20
sales codes. Selection is by general ledger month: you can specify one open
month or a range of open months.

This option was enhanced for Release 2.3. If you want to run a tax report for any
month prior to the date when you installed Release 2.3, type: OLDTAX [Enter] at
any menu to display the original selection screen.

Tax transactions are retained for the number of months specified in Security
Maintenance (X6-6) and they are purged during Accounting End of Month.

### Contents

OVERVIEW......ccsssssssesssccsssssesssnssntssneescesnssssneesnsussesanseneneatssanssenesastensesseesse 2
ENTRANCE SCREEN.

 
 
 
  
 
  
   
 
 

SAMPLE REPORT...
Point of Sale Section
Non-Point of Sale Section.
Recap Section.

OLD SALES TAX REPORT.
Old Sales Tax Report: Point of Sale Section
Old Sales Tax Report: Non Point of Sale Section
Old Sales Tax Report: Recap


2 X16-3 e SALES TAX REPORT RELEASE 2.3

 

### Overview

The information on the Sales Tax Report is presented in 3 sections:
1. Point of Sale Information

2. Non Point of Sale Information

3. Recap, which can be printed independently

To understand how the system divides the information, remember that a document
number can be up to 10 characters. In Point of Sale, the sequence number is 2
characters followed by 5 digits. The 8th position is reserved for the alphabetic
character used for cloned documents. The system generates a "#*" in positions 9
and 10. Typical Point of Sale document numbers are CT00107 #* and
CT00107A#* (clone).

All document numbers with "#*" in the 9th and 10th positions are included in the
Point of Sale Information section.

All other document numbers that include a debit or credit to a sales account are
included in the Non Point of Sale section. These transactions originate in Create
Source Documents (X1-7). To make sure the tax report is accurate and not off by
the amount of last month’s taxes, use a vendor address to pay taxes instead of
making a journal entry.

 

 

### Important

If you deliberately enter "#*" in the 9th and 10th positions of the document
number from Create Source Documents, the transaction will be included in the
Point of Sale section. If you want it to be totaled correctly, observe the Point of
Sale conventions for sales codes and tax codes also. The sales code should be
entered into positions 1 and 2 of the description, the tax code in positions 3-5.

 

 

 

Unless you specify "Sort by Tax Code Description," transactions in the Point of
Sale detail section are listed in order by:

1. State or Province

2. Tax Code

3. Sales Code

4. Document Number

5. General Ledger Sales Account

Transactions in the Non Point of Sale detail section are listed in order by:
1. State or Province
2. General ledger Sales Account

The information that appears in the Recap (Summary) is also organized in 2
sections: Point of Sale and Non Point of Sale. In addition, there is a recap by tax


ACCOUNTING X16-3 ¢ SALES TAX REPORT 3

 

accrual account, which compares the sales tax amount collected at Point of Sale
for the sales codes you selected at the Entrance screen with the total amount in the
G/L account. The difference, if any, is shown as "Variance." When you exclude
sales codes, the Recap will show a variance between the amount collected, which
represents the sales codes reported and the total posted to the G/L account, which
represents all sales codes that post to it.

### Entrance Screen

From the Transaction Menu (X1-6), select option 3, Sales Tax Report. The
Accounting security gate appears, followed by the Sales Tax Report Selection
screen.

      

NW EQUIPMENT SALES SALES TAX REPORT
Division: A Selection

X1630~10

  
   
    
 
    
       
       
       
       
   
   
   
 
  

Starting general ledger Month/Year... 598

Ending general ledger Month/Year... 598

Print STATE (2 char or 'ALL') . 2... ALL

Print Recap only (Y/N)... ... 2.0 N
Note: when you Print Tax Rate detail (Y/N) .. 2... Y <q Applies
exclude sales codes, to Point
the Recap will show a of Sale
variance between the If you would like to exclude sales codes from section
amount collected, the report, enter them below, The previous only.

which represents the selection is shown:

sales codes reported
and the total posted to
the G/L account, which
represents all sales
codes that post to it.

Sort by Tax Code Description (Y/N)...
Starting Description:
Ending Description:

     

Cmdi-Cancel _Enter-Continue

 

Q) To print the report for one general ledger month, use the same month as
beginning and ending months.

Q Key in any sales codes you want to be excluded in the report. When you have
made your selections, press [Enter]. The job is placed on the job queue. A
sample Sales Tax Report is illustrated below.


4 X16-3 « SALES TAX REPORT RELEASE 2.3

 

SAMPLE REPORT

Point of Sale Section

KW EQUIPMENT SALES Sales Tax Report Date 1/28/99 Page 21
BELLINGHAM, WA G/L Month: 05/2998 - 05/1958 Time 16.34.15 ¥16302-02
Point of Sale Information By: Prov/tax/Sales cede

Sales Codes Omitted:
Returns
Account Sales /Trades Dare Addr} Unit#
SHOP SUPPLIES
Ro10S69 #r A3228 261.05 5/29/98 BAS31T
ROLOSB2 H+ A3225 227.03, $/19/98 Pst T4247
RO1603 4+ A3228 74.18 : 5/04/98 PST FEZ§86
RO10609 #* A3225 937,54 5/04/98 PST REPAIR
RO10615 # A3228 26.52 5/02/98 PST REPAIR
RO1O621 4+ 83225 21.40 5/09/98 PST cRgses
RO10623 #* 03228 203.29 5/07/98 PST REPAIR
ROLO626 4° A3223 23.02 5/23/98 PST GE7428
ROLO627 #* 43225 35,52 5/04/98 PST REPAIR
ROLOE32 H+ A328 e935 5/04/98 PST VEas0s
ROLOEIS d+ A3228 16.56 S/2s/9a PST SHEOMA
ROLDE4O #* 43228 64.32 8/30/98 PST wreo1s
ROLOGSS + 43223 357,27 5/19/98 PST REPAIR
ROLOGES a 83225 216.74 5/30/38 PST REPAIR
ROLOG67 #* 83223 €1,06 : 5/23/98 PST REPAIR
ROLOSTO #* A2225 S.22 5/27/98 PST woo4ais
Sales Code PS. | 2552.49 Net Sales 2551.49
RO10S93 H+ A323B +30 §/05/98 PHT coz2a1
Sales Code PH. +30 Net Sales

RO20329 H+ A335C 9/26/98 421023
ROLOS3S H+ Aa35C 5/02/98 REPAIR
ROLO6O9 #* A335C 5/04/98 REPAIR
ROLO654 #* A335C 5/20/88 REPAIR
RoL0663 H+ A335C : 5/16/38 REPAIR
ROLOGEA FY A335C : 5/30/58 REPAIR
ROLO667 f= A33SC 57/23/38 REPAIR
Sales cede ss. | Net Sales SS-SUBLET SALES GST
ROL0Sé4 H+ A336C 5/11/98 STT REPAIR
ROIO594 BY A335C 5/05/98 sTT REPAIR
RO106S3 H+ A336C 5/19/98 STT REPAIR
ROLOGE7 HY A336C 5/23/98 STT REPAIR
sales Code St. - : Net Sales ST-SERVICE CALL
ROLOS3S H+ AS34c . 4.20 $/02/98 TRE REPAIR
RO10S64 4+ A334c : 1.05 $/13/98 TRE REPAIR
RO10623 4+ A334C : 3.18 5/07/98 TRT REPAIR
Sales code TR... : : €.40 Net Sales ‘TR-TRUCKING

Total Tax Code 7. . - +00" 1635.61 Net Sales 23363.94 Total Sales 23363.94 GST
Tax Prev 1296.24 County 30.33 188.90 Dist 243.14 Other +00
Taxable 23704.22 23704 .22 23704.22 23704.22 +09
Rate 2 =98120 00230 : +01040 00000
Linit 500,00 =00 00 09
-90000 -oocge

 

POTAL PROV: BC...  23934.08 170.14 12780759 1635.61 Net Sales 233€3.94 Total Sales 151171.53 cSt 8636.87
TOTAL PROV: BC... — 23534.08 «170.14 -127807.59 1635.61 Net Sales 23363.94 Total Sales 151171.53 cst 8636.67
Tax Prov 1196.24 County 30.33 city 165.90 Dist 243.14 Other

Taxable 23704.22 2370422 23704 ,22 23708.22

The fields in the Point of Sale Information section are described below.

Tax Code 3-character tax code.
Document 8-character document number. Any document with
“#*" in positions 9 and 10 of the document number

 

LO


Account

Sales
Returns/Trades
Exempt

Tax Collected

Date
Description

Addr#
Unit#

X16-3 e SALES TAX REPORT

is included in the Point of Sale section. For more
information, see the INTRODUCTION.

General ledger sales account.

Total amount of sales on this document.

Total amount of returns or trades on this document.

Amount of document total that was exempt from
this sales tax.

Amount of tax collected on the document for this
tax code.

Transaction date (mm/dd/yy).

12-character description. For Point of Sale
documents, the system places the 2- character sales
code in positions 1 and 2, followed by the 1-
character tax code in positions 3-5.

6-character address number of the customer.
Stock number of the unit, if any.


é X16-3 « SALES TAX REPORT
Non-Point of Sale Section

SW EQUIEMENT SALES
BELLINGHAM, #A

Sales Tax Report
G/L Month: 05/1996 - 05/1998
Non Point of Sale Information

Prov : BC
Account? Docum

Sales

Returns Date

Desc

Date 7/15/99
Time 14.34.28

Fage 1
16302-02

Adér# unitw

ASIA
ALIA
AMLLA

#aa3eas
#013699
863730

20000,¢0
2188000
37900.00

5/11/98
5/19/98
5/30/98

WO TRADE. OLS9C4 NE-773
NO TRADE MAL226 NE-741
TRADE UE-606 BAE377 NE-720

 

79450,.09

: ce Net Sales
HewG3E40
#oHG3 672,
#wg3672
Frwg36es
Bracsces
kowG3696
wowG3698
#1163700
4sW8G3707
aswe3714
#0g3729

1250.00
2800.00
$5800.00
1750.00
600.00
1798.00
1090.00
1750.00
3650.00,
4250.00
499.00

3/02/98 NO TRADE
5/27/98 NO TRADE
9/27/98 NO TRADE
5/11/98 NO TRADE
5/13/98 NO TRADE
5/06/98 No TRADE
5/07/98 NO TRADE
5/07/98 TRADE UE~5e6
5/13/98 NO TRADE
5/27/98 NO TRADE
5/30/98 DAVID REID
fae 86234.00 Net sales
Hewe3672
H-NG2672
#2863685

27909.00
36200.90
3286800

8/27/98
5/27/98
5/11/98

NO TRADE
NO TRADE
NO TRADE

79450.00

camco2 961298
JAN181 082332
JAN381 061333
obs904 061255
BEAG4S 061340
FRAO?0 01295
0092 061324
DEB440 0£1293
THIT76 OE102
BAAG72 OE1344
WGS'98 OF1058

6234.09

ANLEL CE-266
ANL81 CE-267
OLs904 c8-271

#onG2688
aenc3eae
aenG3es1
#nG3699

#oweaeaz
#enC3 682
#NG3684
#7063687
#HG3 688
#9863692
#raG3693
#9HG3694
#4963695
#8163702
#4G3703
#9463706
#63708,
#raG3710
#raG3 71S
aenGa718
aeng3718
#9853720
#99G3721,
fewca724
#+8G3732

246700.00
2800.90
8670.00
30094.00

5/04/98 TRADE VE-84 BARG72 CE-265
5/04/98 TRADE YE-5@4 BAAG72 CE-270
$/04/98 NO TRADE REML62 CE-261
5/19/98 NO TRADE WAL226 CE-216
aos. 376892.06 Net Sales 376532.00
8000.00
7000.00
3625.90
1390.90
15000.00
13800.00

5/03/98 NO TRADE
5/09/98 KO TRADE
5/07/98 NO TRADE
5/23/88 NO TRADE
5/04/98 TRADE UE-S84
5/13/88 NO TRADE
59/13/98 REV. WG3628
5/05/98 KO TRADE
5/05/98 NO TRADE
5/03/98 NO TRADE
5/12/98 NO TRADE GRESO® UE~538
5/24/98 NO TRADE DIC616 VE-S28
5/14/98 SOUTHWAY FRM WGS"9S UE-555
5/23/98 NO TRADE WIS617 UE-395
5/27/98 NO TRADE 600999 UE-S7e
3/23/98 NO TRADE DOTSEs UE-59S
5/23/98 NO TRADE DOTSEs VE-S98
5/23/98 NO TRADE SAH7$1 UE-564
5/25/98 NO TRADE HALS39 UE-592
5/26/98 TRADE VE-602 KNAZ61 UE-S00
5/30/98 NO TRADE MANTL? VE-536

Net Sales 103832.3¢

LEN337 UT-358
LIN337 UE-530
DAH285 UB-579
MELG13 UE-S4B
BRAA72 VE-S14
MiD235 UE-580
MED235 UE-S40
MAR285 UE-570
WEDI2T UE-586
cROO7 Co-401

1500.00
4200.00
22000.00
1000.00
9252.34
1050.00
$00.00
3995.00
3600.00
1450.00
1450.00
1438.00
1200.00
4940.00
1178.06

115332,34

11800.00

 

The fields in the Non-Point of Sale section are described below.

Account
Document

General ledger sales account.

10-character document number entered in Create
Source Documents (any document involving this
sale account that does not have "#*" in positions 9
and 10).

Sales Total amount of sales posted to this account.

Returns Total amount of returns posted to account.
Date Transaction date (mm/dd/yy).
Dese 12-character description entered in Create Source

Documents.

 


ACCOUNTING X16-3 « SALES TAX REPORT 7

 

Addr# 6-character address number of the customer.
Unit# 6-character stock number of the unit, if any.

Recap Section

NW EQUIPMENT SALES SALES TAK REPORT Daze 1/18/99 Page 1
BELLINGHAM, WA. G/L Month: 08/1998 - 08/1998 Time 14.34.34 K16306-01
Recap

Tax Code

670977,34 1245800 68a818.34

B -00 -00  127607.58 00 +00

? 23934.08 170.14 +00 -23363.94 «1635.61 azE70 42670 A2670 42670
1196.24 30.33 265.90 283.16

Total BC 694811.42 —«-12628.14 —«127807.59 681882.28 «1535.61 GST: 636.87

691862.28

we Point of Sale Non-Pos
Posted Posted Posted

 

The fields in the Recap section are described below.

Tax Code 3-character tax code.
Sales Total amount of sales for this tax code.
Returns/Trades Total amount of returns or trades for this tax code.
Exempt Amount of document total that was exempt from

’ this sales tax.
Net Sales Sales minus Returns.
Collected Amount of tax collected for this G/L account for

this sales code.

State (or Prov) — County — City — District - Other
General ledger tax accrual account.
Amount of sales tax posted to this G/L account broken out by taxing authority.

Tax Account Information
The fields in the Tax Account Information section are described below.

Account General ledger tax accrual account.
Title Title of the general ledger tax accrual account.


8 X16-3 « SALES TAX REPORT
Point of Sale Section
Collected

Posted
Variance

Non-POS Collected

Total Collected

Dollar total of sales tax collected at Point of Sale for
the sales codes represented on the current report.
Dollar amount posted to this G/L account.
Difference between what was posted to the G/L
account and what was collected for the sales codes
represented on this report. In other words, there will
be a variance only if you excluded sales codes that
accrued tax to this G/L account.

Total amount posted to the general ledger tax
accrual account where the document number did not
have "#*" in the 9th and 10th positions.

Point of Sale Collected + Non-POS Collected.

Cc


ACCOUNTING X16-3 « SALES TAX REPORT 9

 

### Old Sales Tax Report

If you'd like to run the old version of the Sales Tax Report, it's still available. At a
command line, type: OLDTAX [Enter]. The following screen is displayed.

NW EQUIPMENT SALES SALES TAX REPORT %1630-101
Division: A Selection

Beginning general ledger month
Ending general ledger month

Print recap only (¥/N)

If you would like to include sales codes
that do not affect sales accounts, you may
enter up to 10 below:

 

Cmdl-Cancel _Enter-Continue

Q Key in any additional sales codes to be included in the report. When you have
made your selections, press [Enter]. The job is placed on the job queue. An
example of the old Sales Tax Report is illustrated below.


X16-3 e SALES TAX REPORT

Old Sales Tax Report: Point of Sale Section

Ni EQUIPMENT SALES
BELLINGHAM, WA

Tax Code

07200

Total Tax

NW EQUIPMENT SALES
BELLINGHAM, BA

aA

Sales Code
MS MISC SALES ROOOLO7 +
Total Sales Code MS. .

Document

PC PARTS CUSTOME cTo0100
700101
cr00102
T0003
croo10s
700205
cr00206
croei07
rv00025
000100
Rocole1
ROCO1OT
Total Sales Code PC
PI PARTS INTERNA RCOO103
Total Sales Code PI. .
RO00LO2
900103
000107
Totel Seles Code PS...

PS PARTS SHOP

rvo002s
rvo0029
Total Sales Code RE. .

TC LABOR CUSTOME R000102
0003.07
Sales Code TC.

woo0008

A
Account Document
43200 2500203
Total Account A3200
3260 ES00631

Total Account A3250
43290 Bs00812

Total Account A320

3310 32258

Total Account A3310

woo008s
Total Account 23390

0952
Total Account A380

Total Non Point of Sale

SALES TAX REPORT
G/L Month: 91 - 09
Point of Sale Information
Account Sales Returns
43360 1.76
1:76

pate
Tine

Bate

5/21/97

Description

MS

12.84
48.85
32.61
7
2.95
41.81
22,23
37.18
72.82
3.22
17.96
46.19

347.13,

6/20/97
6/20/37
6/20/97
6/20/97
6/20/97
6/20/97
6/20/97
6/20/97
8/01/96
£/20/97
6/20/97
5/21/97

53.50
53.50

5/20/97

109.55
48.09
18.59
176.23

5/20/97
5/20/97
5/21/87

212.00
313.60
625,60

5/03/96
5/03/96

334.63
49.65,
iga_2e

3/20/97
5/21/97

1388.50

A3310 498.22
tee 498.22

498,22

2086.72

SALES TAX REPORT
G/L Month: 01 - 03

Non Poiat of Sale Information

Sales Returns Date Description

$/01/96 7600

Bate
Time

Addeh

Bom%01

nite

28000,00 FTS803

TwOsO1

9990.00 4aitys
2950.00
2995.00
2995.00

5/01/96 440 BACKHOE GRADOA 8H1000

5/01/96 BATTERY

5/01/96 TIRES

5/01/96 PREP

$8564.63
oes AE

9/25/37
7.50.08

Adar#

WILL02
coRROL
BURKOZ
wILLer
WILLo4
cURROZ
WIELO2
WILLO3
ADAMO}
SHAWOI
CURROL
BURKOL

9/25/97
7.50.25

unite

TALOOG
rAz000

Page 1
1602-01

Page ot
¥16302-01


ACCOUNTING X16-3 e SALES TAX REPORT 11

Old Sales Tax Report: Recap

NW EQUIPMENT SALES SALES TAX REPORT Date 9/25/97 Page ot
BELLINGHAM, RA G/L Month: 01 - 09 Tine 7.51,00 x2 6306-01,
Recap

masons Tex Information meses
Sales Type Returns Net Account ‘Rate Calculased

-07800 1388.80 1388.50 42700 o7ace 308.30
Hon Point of Sale 98564.63 59564,63

Tax Account Information:

Non-P08 Total
Variance Collected Collected

42700 ACCRUED SALES 13.93


X16-3 # SALES TAX REPORT

Notes:

## CHAPTER X16-3

SALES TAX REPORT

### Introduction

The Sales Tax Report is based on general ledger transactions for open
months. It is similar to transactions Teports that can be printed using
TRANSACTION REPORT WRITER (X16-2). It includes the detail and
summary (or summary only) of all transactions that originated in Point of
Sale or Create Source Documents and involve sales accounts. You can
optionally include up to ten sales codes that do not affect sales accounts in
the report. Selection is by general ledger month: you can specify one open
month or a range of open months. If desired, you can also choose to reduce
net sales by unit returns and trade-ins.

Suggestion: Since you may close general ledger months before tax reports
are due, it is important to run the Sales Tax Report before you run
Accounting End of Month. Sales tax transactions are not available after a
general ledger month is closed.

The information on the Sales Tax Report is presented in 2 sections:
QO Point of Sale Information
Non Point of Sale Information

To understand how the system divides the information, remember that a
document number can be up to 10 characters. In Point of Sale, the
sequence number is 2 characters followed by 5 digits. The 8th position is
reserved for the alphabetic character used for cloned documents. The
system generates a "#*" in positions 9 and 10. Typical Point of Sale
document numbers are CTO0107 #* and CT00107A#* (clone).

All document numbers with "#*" in the 9th and 10th positions are
included in the Point of Sale Information section.

All other document numbers that include a debit or credit to a sales
account are included in the Non Point of Sale section. These transactions
originate in Create Source Documents (X1-7).


[| X16-3 SALES TAX REPORT Cc

### Important

If you deliberately enter “#*" in the 9th and 10th positions of the
document number from Create Source Documents, the transaction will

be included in the Point of Sale section. If you want it to be totaled
correctly, observe the Point of Sale conventions for sales codes and tax
codes also. The sales code should be entered into positions 1 and 2 of
the description, the tax code in position 3.

 

Transactions in the Point of Sale detail section are listed in order by:
O Tax Code
Sales Code
O Document Number
O General Ledger Sales Account (

 

 

 

 

Transactions in the Non Point of Sale detail section are listed in order by
general ledger sales account. The information that appears in the Recap
(Summary) is also organized in 2 sections: Point of Sale and Non Point of
Sale. In addition, there is a recap by tax accrual account, which compares
the sales tax amount calculated by the Sales Tax Report to the amount
actually collected at Point of Sale. The difference, if any, is shown as
"Variance."

You can expect some variance due to rounding. At Point of Sale, sales tax
for each tax code is calculated, rounded, and collected at the end of each
document. On the Sales Tax Report, all sales for a particular tax code are
totaled first, which means that there is only one calculation and rounding.
In most cases, the tax collected at Point of Sale will be more than the
amount calculated by the Sales Tax Repost.

RELEASE 2.2 LL


X16-3 SALES TAX REPORT [2]

### How To Run

From the Transaction Menu (X1-6), select option 3, Sales Tax Report. The
Accounting security gate appears, followed by the Sales Tax Report
Selection screen.

AGR EQUIPMENT SALES SALES TAX REPORT *1630-102
Division: a Selection

Beginning general ledger month
Ending general ledger month

Print recap only (¥/N)

If you would like to include sales
that do not affect sales accounts, you may
enter up to 10 below

Cmdi-cancel Enter-continue

 

To print the report for one general ledger month, use the same month as
beginning and ending months. To reduce net sales by returns and trade-ins,
type "Y".

Key in any additional sales codes to be included in the report. When you

have made your selections, press [Enter]. The job is placed on the job
queue. An example of a Sales Tax Report is illustrated below.

## X16-3 SALES TAX REPORT

Point of Sale Section

usatn SQUSPHENT COMPAL SaceS THX REPORT pote 3728/97 mage
BECLINGRA WA 5 crt Wenths 2-08 fine 7.30.08 2622-01
point of sate informacion
sex code sates cove Account Sales Returns boseziption Adare units
we mise sabe REOOLaT #43369 pais?
ota Sales Code MS. s+
de FARTS cUBTONE €700309 sa0i9) vwac2
cronies ey20i39 canna
enesiea erase? porno
erosie: eres sac
craoiee e037 wre
craoios eras? corno2
crn0i06 ena amo.
excors7 220/97 rua
3100025 52/36 —
ro00t02 pneis? aot
mo0ct01 saci cunno
r000367 593 sunk
goeol Sates code Fee (

Pr PARTS INTERNA ROOOLO3 5726/97
otal sales Code Pz «

FS PARTS SHOP -RODOLO2 5/20/97
090103 5/20/97
090107 5/21/97
Total Sales Code PS. -
rvoco23 5703/96
xv0c029 5/02/95
Total Sales Code RE
‘De uABOR CUSTOME RO00102 5/20/97 cURROL
Rog0107 5/28/97 BURKOL
Total Sales Code TC .

oral Tax Code vee 3BRB.S9

00000 wooeses z 70196
Total Sales cade WO. -

Total Tax Code R

‘otal Point of Sale

 

RELEASE 2.2 LU

## X16-3 SALES TAX REPORT LJ

### Fields & Descriptions

Tax Code l-character tax code found in position 3 of
the description field,

Sales Code 2-character sales code found in Positions 1
and 2 of the description field.

Document 8-character document number. Any

document with "¥*" in positions 9 and 10 of
the document number is included in the
Point of Sale section. For more information,

see the INTRODUCTION,
Account General ledger sales account.
Sales Total amount of sales on this document.
Returns Total amount of returns on this document,
Date Transaction date (mm/dd/yy).
Description 12-character description. For Point of Sale

documents, the system places the 2-
character sales code in positions 1 and 2,
followed by the 1- character tax code in

Position 3.
Addr# 6-character address number of the customer,
Unit# Stock number of the unit, if any.

co

Non-Point of Sale Section

     
     
 

  
 
  
 

AUSTIN EOULPHENT COMPANY SALES TAK REPORT pare 9/25/97 page 2
BELLINGHAM, WA a Git Monch: 91 > OF ime 7-30.25 x16302-02,

non Posat of Sale Internation
Dare

   
 
   
 

     

account, Document

 

    
 

  

 
   

 

200 #300203 15000 .00 5701/96
‘otal account A320 e000. 00

  

5/02/96

     

 

  
      

 

13290 E500512
motal account 43290

  

5/02/96 £40 BACKHOE

   
 
 
  

   

 
 

 

5/01/96 BRTTERY

 

 

   
 
  
  

5/01/95

   

1 account A3380

 

ine syoni3e PREP (
qovei Account M3309

    
      

   

    

  

Toual Non point of Sate 8564.62

 

### Fields & Descriptions

The fields in the Non-Point of Sale section are described below.

Account General ledger sales account.
Document 10-character document number entered in
Create Source Documents (any document
involving this sale account that does not
have "#*" in positions 9 and 10).
Sales Total amount of sales posted to this account.
Returns Total amount of returns posted to account.

RELEASE 2.2 os


Date Transaction date (mm/dd/yy),

Description 12-character description entered in Create
Source Documents.

Addr# 6-character address number of the customer.

Unit# 6-character stock number of the unit, if any.

Recap Section

AUSTIN EQUIPMENT COMPANY SALES TAX REPORT Pace 9725/37 Page
BELLINGHAM, WA B G/L Month: 02 - 03 Time 7.51.99 x16306-01
Reeap

Won Point of sale 59564.63, $8864.63,

Tax Account rn a

ss Point of Sale « =
Account Tire ated Collected Variance

A270 ACeRUED SALES tax

 

### Fields & Descriptions

The fields in the Recap section are described below,

Sales Type Sales tax code and its associated rate (total).
Sales Total amount of sales at this rate.
Returns Total amount of returns at this rate.
Net Sales minus Returns,
Tax Information
Account General ledger tax accrual account.
Rate Sales tax rate for this account.


Calculated

Tax Account Information

### Fields & Descriptions

Amount of sales tax calculated by the Sales
Tax Report. Note: This figure would be used
only in the most simple tax situation. Most
dealerships handle more complex returns
involving multiple taxing entities.

The fields in the Tax Account Information section are described below.

Account
Title

Point of Sale Calculated

Collected

Variance

Non-POS Collected

Total Collected

General ledger tax accrual account.

Title of the general ledger tax accrual
account.

Dollar total of sales tax calculated by the
Sales Tax Report. Note: This figure would
be used only in the most simple tax
situation. Most dealerships handle more
complex retums involving multiple taxing
entities.

Dollar amount actually collected at Point of
Sale.

Amount Calculated minus Amount
Collected. A negative amount indicates that
more tax was collected than may be due on
your sales tax return.

Total amount posted to the general ledger
tax accrual account where the document
number did not have "#*" in the 9th and
10th positions.

Point of Sale Collected + Non-POS
Collected.
CC

## CHAPTER X16-4

SALES TAX REPORT BY STATE/COUNTY

### Introduction

The Sales Tax Report by State/County is prepared from the same data as the Sales
Tax Report (X16-3). If you use the same selection criteria, the totals will be the
same, but the reports are sorted differently. Sorting by county is handled by
adding the county to the Tax Rule Table through Tax Rule Maintenance (X527-
3). A county must be linked to a zip code range; otherwise, all cities will be
reported under a blank county within each state.

ENTRANCE SCREEN

 

SAMPLE DEALER TEST FILES SALES TAX REPORT X1630-10
Division: A Selection

Starting general ledger Month/Year... 598
Ending general ledger Month/Year... 598

Print STATE (2 char or 'ALL') ...., ALL
Print Recap only (Y/N)... 2... N

if you would like to exclude sales codes from
the report, enter them below. The previous
selection is shown:

Sort by Tax Rule Report code (Y/N)... W

Starting Report code: . 7 Ky

Ending Report code:

Cmdl~Cancel _Enter-Continue

 

X164.doc 7/29/99 1


2 X16-4 « SALES TAX REPORT BY STATE/COUNTY RELEASE 2.3

 

 

### Sample Report

SAMPLE DEALER TEST FILES Sales Tax Report Date 7/18/99 Page 2
ABBOTSFORD, BC R G/t Month: 05/1998 - 05/2998 Time 14.27.23 26402-02
Point of Sale Information By: Prev/County/csty/Tax

Prov : BC Sales Codes Cnitted:
‘tax Tax
Code Document Acco! Exempt Collected Date
07000 TEST CHG TAX
ROLOESS Hr A330C 6.30 5/19/98 CLT REPAIR
craas76 Hy A3208 1,99 5/02/98 PCT CASHA
cr4a577 4+ A320B 5184 5/26/98 BCT CASHA
749590 #+ AZZ0B 2.37 $/04/98 BCT CASHA
74627 Be A3Z0B 6.05 5/21/98 PCT SASHA
crag629 H+ A3208 2.52 5/05/38 PCT. cASRA
cT4g6e7 §* A320B 14.40 $/07/88 pcr cASHA
crae6s3 fF A3208 +53 $/07/88 PCT CASHA
cragecs > A320B S.01 5/11/38 PCT cASBA
cr4e708 > A320B 1.27 5/08/38 PCr CASHA
348780 A320B 2.43- 5/11/38 PCT CASHA
erae776 Be A3Z0B 2.28 5/21/98 PCT CASHA ws
¢748779 # A320B 1.16 5/12/98 PCT CASHA 2s
cr4ea07 #* A320B 6.05 5/13/98 PCT CASHA
eraseos #* A320B g.e4 $/23/98 pcr cASHA yor
cragess #* A320B 2.08 5/16/98 PCT CASHA vas
798837 #* A320B 35.49 §/19/98 PCT CASHA ves
cT488ge #+ A320B 4.15 $/19/38 PCT CASHA vay
cr4gesi #* 23208 4.79 §/23/98 FCT CASHA va
¢r4as02 a= A3203 4.98 §/20/98 PCT CASHA ves
eraasog a* A3203 263 5/20/98 PCT CASEA vas
craaoi2 #¢ A3208 3.48 $/23/98 PCT caz7it ves
erag913 d+ 43208 : 2.79 5/20/98 PCT CASHA var
eragezs #* A2218 : 3.36 5/21/98 PCT cASHA vex
gragad7 #+ A320B : +54 5/23/98 PCT CASHA v3
e74a948 4+ A3208 : 2.62 5/26/98 PCT CASHA vas
er4e9e¢ a+ 23208 : 4.39 5/25/98 BCT cASHA 2s.
ergsose #* 43203 2.77 5/30/98 PCT CASHA ves
149067 4+ A3203 1.46 5/20/98 PCT asta vas
RO10659 4° A322 1.01 $/19/98 PST REPAIR van
RO1O659 #* A336 4,05 5/19/98 STT REPAIR yaw
tax Code: TO. eee -00 123.47 Net Seles 1763.41 Total sales 1763.41 GST
Tax Prov 90.28 city 12.49 Dist 19.44 Other +00
Taxeble 1832.92 2032.91 3032.92, +00
Rate 1 08120 -00749 -01040 90500

Limit S00.00 -00 -00 +00
00000 00060 +20000 -90009

1798.16 34.75 7599.67 «123.47 Net Sales 1763.41 Total Sales 9363.08
Prov 99.28 County 2.26 city 12.49 Dist 18.44 Other +00)
Taxable 3832-91 1832.91 1832.91 1832.91 +00

## CHAPTER X22-4

UNIT INVENTORY ACCOUNT TABLE

### Introduction

If you use F&I, this non-divisional job assigns general ledger accounts to
trade-ins by make and model. It is similar to Vendor/Class Maintenance
(X52-4).

When Unit Sales Entry is started, trade-ins are automatically entered into

inventory according to the account assignments made in this job.

Printing Unit Inventory Account Table.

If you simply want a printout of current assignments, you can enter this
job and then press [Cmd1] to end and answer Y to the following message:

Wild Card Used in Unit Inventory Account Table

*nnnnonn General ledger account


[| X22-4 UNIT INVENTORY ACCOUNT TABLE

### How To Run

From the Unit Sales Entry Menu, select option 4, F&I Trade-In
Assignments,

A & R SALES & LEASING CO UNIT INVENTORY ACCOUNT TABLE 2240-102 1
Division: *

Enter-Continue Cmd1-End job

 

 

 

 

Furnish both make and model and specify new or used and press
[Enter]. A prompt for the general ledger account is displayed.

 

RELEASE 2.1 CC


X22-4 UNIT INVENTORY ACCOUNT TABLE [=]

A & R SALES & LEASING CO UNIT INVENTORY ACCOUNT TABLE x2240-102 2
Division: *

G/L Account . *1230

Enter-Continue Cmd19-Delete

 

Oi To delete an assignment, press Cmd19-Delete on this screen.

(1 Furnish an account and press [Enter] to return to the entrance screen.
The “wild card" form where an asterisk (*) is used in place of a division
code is valid.

When you are done, press [Cmd1] to end the job. The following
message is displayed:

Oo

Print Unit Inventory Account Table? .....Y¥

 

 

 

Leave the default of Y if you want a printout; otherwise, change it to N
and press [Enter].

 

UNITS


[+] X22-4 UNIT INVENTORY ACCOUNT TABLE

SAMPLE PRINTOUT OF UNIT INVENTORY ACCOUNT
TABLE

An example of a printout of Unit Inventory Account Table is illustrated
below:

AE R SALES & LEASING CO. pate 3/25/94 Page 1

BELLINGHAM, WA ime 14.22.55 22402-01

 

## CHAPTER X22-7

UNIT SALES BUDGETING

### Introduction

Unit Sales Budgeting allows you to compare the actual number of unit
sales posted to a G/L account against a budgeted number specified by you.
Unit sales are automatically incremented with Point of Sale (X5-1) and
Unit Sales Entry (X22-1), and Create Source Documents (X1-7).

### Preparation

Point of Sale (X5=1) and Unit Sales Entry (X22-1) will automatically
increment the number of unit sales posted to each sales account. Create
Source Documents (X1-7), however, requires that you enter a "#*" at the
beginning of the Doc# field to increment the sales counter.

### How To Run

From the Unit Sales Entry Menu (X1-2), select option 7, Unit Sales
Budgeting. Enter your division and password at the security gate and
press [Enter]. The following screen appears.


[J X22-7 UNIT SALES BUDGETING Cc

ABC-AG,AUTO,CONS & TRUCK CO UNIT SALES BUDGETING 2270-101 1
Division: *

Account##:-

Enter-Continue Cmdl-End job

 

O Enter a unit sales account number and press [Enter]. The following
screen appears.

RELEASE 2.1 ae


UNITS

## X22-7 UNIT SALES BUDGETING

‘ABC-AG, AUTO, CONS & TRUCK CO UNIT SALES BUDGETING X2270-102 2

Division: *

Account#: 23260

Decenber 1994
January 1995
February 1995
March 1995
April 1995
May 1995

June 1995
duly 1995
August 1995
September 1995
October 1995
November 1995
December 1995
January 1996
February 1996

cmd3-Return Gmd5-Later cmd6-Earlier

Decerber 1993
January 1994
February 1994
March 1994
April 1994
May 1994

dune 1994
July 1954
August 1994
September 1994
Cctober 1994
November 1994
December 1994
January 1995
February 1995

 

O Fill out as many months of budgeted sales as you want, using [Cmd5]
and [Cmd6} to select earlier or later months if necessary.

O When you are finished, press [Cmd3} to return to the previous screen.
You may continue to budget unit sales for other accounts. When

finished, press [Cmd1].

O A prompt will appear asking if you want to print a Unit Sales
Budgeting Report. If you answer Y, the following screen will appear.


[+] X22-7 UNIT SALES BUDGETING co

ABC-AG, AUTO, CONS & TRUCK CO. UNIT SALES BUDGETING X22702-01 4
Division: A

 

O Enter the account and the range of months you want to be included in
the report. Press [Enter]. A report will be generated and sent to the
system printer. A sample report follows.

RELEASE 2.1 tO


ABC-AS, AUTO, CONS & TRUCK CO. UNIT SALES BUDGETING REFORT Date 12/07/94 Page 1

BELLINGHAM, WA B Time 8.53.15 2270-20
ACCOUNT: 43200

New TRACTORS
Decenber "94 - Maren “$6

Budgeted actual Actual as a
sales Sates 2 of Bugger

 

UNITS


Notes:

RELEASE 2.1 LL

## CHAPTER X22-8

UNIT ORDER PROCESSING

### Introduction

Unit Order Processing allows you to view and maintain a list of ordered
units. Entries in this list may be changed, deleted, or received.

### How To Run

From the Unit Sales Entry Menu (X1-2), select option 8, Unit Order
Processing. Enter your division and password at the security gate. The
following screen appears.

ABC-AG, AUTO, CONS & TRUCK CO UNIT ORDER PROCESSING ¥2280-002 1
Division A Review Unit orders
(options: i=Create 2=Change 4=Delete 9sReceive)
opt Order # ord Date Year Make Model color

ORDH201 «12/02/94 = «1995 FORD F129 BLUE

Cmdi-End job Roll-Page Home-Top of list

 

Each entry in this list represents an ordered unit that has not been received.


[2] X22-8 UNIT ORDER PROCESSING Cc .

0 To change an order, select it with 2=Change; to delete an order, select it
with 4=Delete. Creating and receiving orders are illustrated below.

Q To create a new order put a "1" next to the blank line on the top and
enter an Order# in the field next to it. Press [Enter].

### Create A New Ordered Unit

ABC-AG,AUITO,CONS & TRUCK CO UNIT ORDER PROCESSING x22810-01 1
Division & Create Unit Order

Order Number  ORD#201 Order Date

Specifications:

 

C Furnish the Order Date, Year, Make, and Model of the unit. The Color
field is optional. Enter T=Truck or C=Car. Press [Enter]. The unit you
just entered will appear on the Review Unit Orders screen above.

RELEASE 2.1 LO


X22-8 UNIT ORDER PROCESSING [=]

### Receive A Unit On Order

O To receive a unit, put a "9" next to it on the Review Unit Orders screen.
The following screen appears.

ABC-AG, AUTO, CONS & TRUCK CO UNIT ORDER PROCESSING %22890-01 1
Division A Receive Unit Order

Order Number  ORD#123 order Date 120294

Serial @.
Dese...

G/L acct.
Stock #..:

Specifications:

cmd3~Cancel

 

O Fumish the received unit's Serial#, Description, G/L Account, and
Stock#, The Serial# and Description fields are optional. Once you are
finished, press [Enter]. The Review Unit Orders screen appears and

UNITS


[+] X22-8 UNIT ORDER PROCESSING -
(

you can continue adding, changing, or receiving orders. Once you are
finished, press [Cmd1] to return to the Unit Sales Entry menu.

RELEASE 2.1 LL

## CHAPTER X22-9

UNIT ORDER REPORT

### Introduction

Unit Order Report produces a list of units that are currently on order. The
user can choose to select units included in the report on the basis of make
and model. An option exists to include all available units already in
inventory (as compared with those on order) in the report.

### How To Run

From the Unit Sales Entry Menu (X1-2), select option 9, Unit Order
Report. Enter your division and password at the security gate. Decide if

you want the report to include all divisions and press [Enter]. The
following screen appears.

ABC-AG, AUTO, CONS & TRUCK CO. UNIT ORDER REPORT
Select Units

2290-101 i

Select a combination of the following:

¢mdl-End job Entex-continue


[2] X22-9 UNIT ORDER REPORT Co

O If you want the report to include units of a particular make or model,
enter that information on this screen. If these fields are left blank, the
report will include all makes and models.

O Decide if you want a detailed or summarized report. A detailed report
includes all the information entered in Unit Order Processing, X22-7.
A summarized report lists each unit's Order#, Order date, Year, Color,
and Division.

O Decide if you want the report to include only ordered units or units that
are both on order and available. Press [Enter] when done. A report
will be generated and sent to the system printer. A sample report
follows. (

RELEASE 2.1 LU.


ABC-AG,AUTO,CONS & TRUCK CO.
DIVISTON +

ORDER DETAIL,

### Report

ervic
Year Color W/U Div

saenys 86 ”

> Total Available: HONDA CIVIC
Make/Moge! on Order : HONDA CIVIC
order # Year Color C/T
ORDHLOL 12/03/94 1995 CREAK =
ompe201 12/09/94 1995 GREEK ©

- Total on Order : HONDA

Make/Model Available: HONEA

onit # In Date

ord Date

Make/Model Available: HONDA CRX
Unit # In Date Year Color N/U

o97cKH 86
se98* Totel Available: HONDA CRX
ww09" No units are on order +t

Make/Model Available: HONDA FLISOR
unit # In Date Year Color N/U Div
7a0123, 86 MRITE ™

terse Total Available: HONDA FLOSOR,

Make/Model Available: HONDA NIGHTHAWK
Unit # year Color NAJ Div

sHi896 56 RED
e8* qoral available: HONDA NIGHTHAWK
"* No unics are on order ttt

In Date

Make/Model avai lab)
onic

HONDA VFSOOF
Year color N/J Div

Peogs2 26
‘Total Available: HONDA
No units are on order

an Dare

Make/Model Available: HONDA
Unit # In Date
PC06s8 86 BLUE
Total Available: HONDA VF7O0F
No units are on order **++
‘ORDER DETAIL
REPORT
Make/Model Availabla: YONDA VES MAGNA
Unit # In Date Year Color N/Y Div

VET0OF
Year Color N/U iv

ABC-AC,AUTO,CONS & TRUCK CO.
DIVISION *

UNITS

Location

+ Subtotal,

Eecation

recation

 

## X22-9 UNIT ORDER REPORT

DATE
Time

wero7ss4
8:53:55

PAGE 1
2290-202

DATE 12/07/94
TIME 0:53:55

PAGE 2
2290-201


[+] X22-9 UNIT ORDER REPORT

### Fields And Definitions

Two sections occur for each type of vehicle included in the report,

Available and On Order.

On Order

Unit# 6 characters.

In date 6 digits. Date received.

Year 2 digits.

Color 5 characters.

N/U I character. New or Used.

Div 1 character.

Location 6 characters.

On Order

Ord# 6 characters.

Ord Date 6 digits.

Year 4 digits.

Color 5 characters

c/T 1 character. Car or truck. Equipment dealers will always
have an "E” in this field.

Div 1 character.

## CHAPTER X27-1

CREATE DEPRECIATION POSTING BATCH

### Introduction

Use Create Depreciation Posting Batch to generate depreciation
transactions and create a posting batch from them. After the batch has
been created, use Review & Post Depreciation Batch (X27-2) to review
the transactions.

### Create A Batch

From the Units Depreciation Menu (X2-7), select option 1. Press Enter.
After the security gate, the Create Depreciation Posting Batch screen

appears.

Create Depreciation *22221-004
Posting Batch

Division: a

A Depreciation posting batch will be created for the month of July.

Gdl-End Job  Cmd2-Continue

## X27-1 CREATE DEPRECIATION POSTING BATCH

 

Press Cmd2 to continue.

It takes a few minutes to generate the transactions and create the batch.
You may proceed with other work. A message will be sent to your work
station when it is created.

Message Display

From-B WsID-** Date-12/11/89 Time- 11:39:21
Depreciation batch has been created for division A.

 

Press Enter to continue. Proceed to Review and Post Depreciation
Transactions (X27-2). (


RELEASE 2.1 WS

## CHAPTER X27-2

REVIEW AND POST DEPRECIATION POSTING BATCH

### Introduction

This job is Step 2 for depreciation transactions. Use Create Automatic
Depreciation Posting Batch (X27-1) to generate the transactions and create
the batch from them. After you receive the message at your workstation
that the batch has been created, use Review and Post Depreciation Posting
Batch.

### Post A Batch

From the Units Depreciation Menu (X2-7), select option 2. Press Enter.
After the security gate, the Post Source Documents Check for Errors
screen displays.

For information on editing and posting a batch, see Chapter X1-7, Create
Source Documents.


Notes:

## CHAPTER X27-3

DEPRECIATION REPORT

### Introduction

The Depreciation Report lists:

= all units with depreciation.

= figures for the last closed month or the end of the oldest open month
(for example, if the oldest open month is January, as of the 31st of
January).

= prints the items with sub-totals by account and final totals.

The Depreciation Report does not show depreciation which has been
posted manually.

NO OTHER USER UNITS JOBS CAN BE RUNNING. IF THERE IS A
UNITS JOB ON THE USER BOARD, WAIT FOR IT TO CLEAR.

### How To Run

From Menu X27, select option 3 to run the Depreciation Report.

At the Depreciation Report screen, type Y to include figures for your
oldest open month. Type N to report only the last closed month's figures.


X27-3_ DEPRECIATION REPORT

See the screen example below:

DEPRECIATION REPORT

N Enter ¥ if you want figures
as of the end of AUGUST

Otherwise the report will reflect.

your last closed month's figures.

Press cmdl to cancel

 

RESULT: The Depreciation Report will be placed on the job queue.

RELEASE 2.1 Lo


X27-3 DEPRECIATION REPORT [=]

WROEVER TRACTOR CO. ASCOUNTING END OF MONTH Dace 10/02/86 Page 1
BELLINGHAM, WA AUTOMATIC DEPRECIATION REGISTER FOR 21/85 ‘Time 17.00.26 IA90-ca,
pars, TOTAL ADDITIONAL PAS? YEARS THIS MONTH YEAR TO DATE
STOCKE MODEL «DESCRIPTION ACQUIRED COST FIRST YEAR SALVAGE LIFE METHOD —DEPR DEPR EPR
FA0642 5500 AATRACTOR —§/20/81 16826.29 20.0 SUN 149.22 441.3
PAO7S2 6600 A-TRACTOR 6/01/81 19562.70 10.0 SUN 163.02 978.12
PASTSR 720-5 M+ LOADER 6/10/81 1289.36 5.0 19.34 318.06
PRQIL sun 9701e1 2000.00 2000.00 5.0, 6199.80 133.33 1466.43
FA6215 useD 30/01/81 10000.00 5.0 Bon0.09 372.63 1722.63
FAGSAS ACRS USED 11/01/81 10000.00 5.0 Ba09.00 +20 1598.80

WHOEVER ‘TRACTOR CO. ACCOUNTING END OP wONTH Date 20/02/86 Page
BELLINGHAM, WA. A RECAP OF AUTOMATIC DEPRECIATION ‘Time 27,00,20 XLA00-HA

ACCUM DEPR EQ at2ia ‘CREDIT 3an.st

 

ACCIM DEPR RENT A122 cesorr 305.6

ACCUM DEPR-RENTAL EQUIP A163 CREDIT 322.58

EQUIP DEPR EXP A621 caeprt

RENT DEPR EXP. 622 cReDIT

DEPRECIATION EXP CREDIT

 

UNITS


[+] X27-3 DEPRECIATION REPORT

### Fields & Descriptions

The fields on the report are described below:

Stock# Unit identifying number.

Make Manufacturer of unit.

Model Manufacturer's model number for unit.

Description Brief description of the unit.

Date acquired Beginning date for fixed asset depreciation.

Cost Cost of unit to dealership.

First year Deprec. Dollar amount of the 1st year depreciation.
ff you see 25000, it is $250.00.)

Salvage The value in $ of an asset at end of its life

Bal. for regular Deprec.

Cost minus the Ist year depreciation and
salvage.

Prior years deprec. Dollar amount, past accumulated
depreciation.

Balance beginning Balance for regular depreciation

this year minus prior year's depreciation.

Current year Deprec. Dollar amount of current year's depreciation.

Life/Method LIFE is the expected lifetime of an item.
Enter 10 in LIFE so the monthly
depreciation will be figured correctly.
METHOD is the Depreciation Code, one of:
ACR for Accelerated Cost Recovery, SLN
for Straight Line, % for Declining balance,
or MAN for Manual.

Totals Totals by Account Number, Name of
Account, and Dollar Amount.

Grand Totals Dollar amount totals for each field.
Nat

## CHAPTER X28-1

SALES PRICE BOOK

### Introduction

The Sales Price Book lists:

= all units in inventory with useful information for sales personnel,
including:
= stock number, make, model, serial number
= description, specifications, in-date
= location and warranty codes
® special and list prices
= and optional cost of item.
= and allows you to select the following options when printing:
= print COST or not.
™ normal or compressed print at 6 or 8 LPI on 8 1/2" or 11" paper.
= print Fixed Assets and/or Rentals.
® print the Price Book for one specific account number.

This report can be printed in order by General Ledger account, by
description, by Horsepower, Location, or Make. In addition, units with
blank horsepower can be excluded, if desired. If it is in order by General
Ledger account, all units in a General Ledger account are listed together,
and they are in order by description. If it is in order by description, all
units appear in order by description, regardless of the General Ledger
account,

Since the description of the Sales Book item lists in alphabetical order, all
the AXLES sort together. AXLES will sort before BATTERIES. You may
deliberately choose to precede some descriptions with an "A" so that they
will appear first in the Sales Price Book, such as A - TRACTOR. Please
note that the system is very particular about the description, and it must be
exactly the same for each item you want in a certain category. If A -
TRACTOR, A - TRACTER, and A-TRACTOR is used on 3 different
units, they will appear in 3 different sections. Be very careful with
spelling, punctuation, and spaces. If there are errors, correct them in
Inquire/Update Units.

## X28-1 SALES PRICE BOOK

 

### How To Run

From Menu X28 select option | to run the Sales Price Book. At the
security gate, type Y to include all divisions on the report or N to include
only one division. The Sales Price Book selection screen appears.

 
  

           
  
  
  
   
  
   
  
   
  
 
 
   
   

ABC COMPANY
Division ALL

SALES PRICE BCOK X2810-101 1

Report by ¢ (6)

/% account #

iD) escription

(4) orsspower

{L) ocation

iM} ake

Enter "Y" if wanted {

Print cost column? N
Prompt to change forms? N
Print fixed assets? N
Print rentals? N

Exclude units with blank horsepower? N

Number of copies (1-9)? 1
CPI (10 or 15)? 10
LPI (6 or 8)? 6
LPP (51, 66, 68, or 88)? Sz

For a price book including units from
only a single account, enter account number:

 

cmdi-cancel job

Specify the order in which the Sales Price Book will be printed. Type G
for General Ledger account, D for description, H for horsepower, L for
location or M for make.

RELEASE 2.2 LU


X28-1 SALES PRICE BOOK [=]

### Fields & Descriptions

Print cost column? Y will print a COST column.
(You may prefer NOT to see COST figures
in your Sales Price Book; if so, accept the
default of N).

Prompt to change forms? Y causes system to generate a message when
it is time to change forms.

Print fixed assets? Y includes fixed assets on the price book.

Print rentals? Y includes rentals on the price book.

Exclude units with Y excludes units with blank horsepower.

blank horsepower?

Number of copies (1-9) 1 digit. Type the number of copies you want.

CPI (10 or 15)? Characters Per Inch. Normal type‘is 10 CPI.
Compressed print is 15 CPI.

LPI (6 or 8)? Lines Per Inch. See table below.

LPP (51, 66, 68, or 88)? Lines Per Page.

Set LPI and LPP according to the table

below:
Paper Length Lines Per Inch (LPI) Lines Per Page (LPP)
8 1/2" 6 51
8 1/2" 8 68
1" 6 66
11" 8 88

For a price book including units from

only a single account, enter account number:
8 characters. Typing in the specific account
number here will generate a price book for

UNITS


AGR EQUIPMENT SALES
LYNDEN, WA

Stock# Make
Specifications

sees BeRAKE:

NHO720 NEW HOLLA 855

penpaneees CoRAYBINE,

NH0224 NEW HOLA 439

D-ROTAVATOR

OWSS94 HOWARD HN-40
OWS604 HOWARD HN-4¢

FA-HEAD

HOLLA 770-1
HOLLA 770-4

G-FLAIL

HOLLA 36
HOLLA 32

‘J-SPREADER

NASTI3. NEW HOLLA 519

ce aeetenee ROBLADE

owses9 KRAUSE

dseseeneee LOROTARY HOW ttre

owsés6 Woops = MaPC

NEW EQUIPMENT

that account only.
RESULT: The Sales Price Book will be placed on the job queue.

An example of a Sales Price Book follows.

SALES PRICE SOOK - NEW EQUIPMENT Date 1/27/96 Page
Fixed Assets-No  Rentals-No Account- ALL Al) #P-Yes Time 16.15.46 w2ano-3a

PC Yr Color N/ Serial # Le Date dis War Price

2159.69

sagaza 6929.00

1195.90
1195.00

206326 1683.00
406690 1584.00

369052 4750.09 4376.00
9219 4750.09 4576.00

so7ese

oo ceossca

 

NEW EQUTPMERT
2

 

LO


UNITS

### Fields & Descriptions

Stock#
Make
Model
HP
Specs
Extended specs
Serial #
Le
Date
Dis
War
Special
Price
Cost

X28-1 SALES PRICE BOOK |

Unit identifying number.

Manufacturer of the unit.
Manufacturer's model number for item.
Horsepower of the unit.

Features of the unit.

Extra space for the features on the unit.
Serial number of the unit.

Location of the unit in your dealership.
Date the unit was entered into inventory.
Permitted discount on sale.
User-defined code for type of warranty.
Price if a special is offered.

Suggested list price.

Cost of unit to your dealership.


Notes:

## CHAPTER X28-2

SOLD UNITS REPORT

### Introduction

The Sold Units Report can be selected by:

™ transaction date range, or

® make, or

= make and model, or

" partial or complete serial number,

and includes:

= all sold units and the customer to whom they were sold,

= complete information about the unit,

™ customer information including customer name and address #.

The report can be sorted in order by transaction date with the most recent
date first or by unit number.

### How To Run

0 From Menu X28 select option 2 to run the Sold Units Report.

O At the security gate, type ¥ to include all divisions on the report or N to
include only one division.

The selection screen appears.

## X28-2 SOLD UNITS REPORT

 

 
 
 

       

AUSTIN EQUIPMENT COMPANY
Division: *

Sold Units Report
Selection Screen

2820-001 1

    
  
 

 

Enter the following information to select units for the xeport.

  
 
 
   
 
    
 
 
 

- If all of the fields are left blank, all units will be included.

~ A partial serial number can be entered to select all serial numbers
that begin with the same characters.

Transaction date (mmddyy): From 51094 To 51094

Make: FORD Model:

Serial:

    
 
 

- Sort report by transaction date (D) or unit# (U): D

    
 

Cmdl-End job Enter-contimue

 

C1 Leave the fields blank to include all dates and all units, or enter one or
more of the following selection criteria:
= Transaction date range, "From" and "To"
To request transactions for one day, use the same date "From" and
"To" as illustrated on the screen above.
Make

Model
Make & Model
Partial or complete serial number

#
RELEASE 2.1 Nw


 

 

 

 

If you prefer to have the report sorted in order by unit number, type U
at the prompt, "Sort report by transaction date (D) or unit# (U).

Press [Enter].

The Sold Units Report will be placed on the job queue.

 

oO

An example of the Sold Units Report, which is sorted by transaction date,
follows:

LEE'S RENTAL COMPANY ‘SOLD UNITS REPORT Date 12/11/96 Page
LYNDEN, WA A ‘Dime 10.32.36 2820-12,

From: 0/00/00 Te: 12/11/96 : : Serialt: Sort Method: DATE

Invoice warranty
Stock # Year Make Medel sre Description addr ¢ customer pate number Date code

BH1000 00 CASE 440 266099423 O-BACKHOZ GRADO. LEROY GRADY 5/01/86 BS00512 9/01/86
PTS803 00 FORD 7600 0637578 A-TRACTOR BOUL SLIM SOULDERMAN 5/01/86 2500203 5/02/86
@31LVS 86 HONDA ACCORD = -1LHGBAS€32GR002947 4D Lt ‘Twosda AMY TwosHoES 5/01/86 500631 5/02/87
T0542 00 FORD 6600 002462 A-TRACTOR BOUL SLIM BCULDERMAN 3/15/86 MAR UNTT 3/25/87
FESB6e 00 FORD 758 Boces 0-BACKHOB GRADO LEROY GRADY 2/01/86 INvOL 2/01/87
75768 00 FORD 1500 902627 A-TRACTOR —_HOOKO1 CARL HOOKER 1/15/86 rvo002 1s/e7
$8281 90 NEW HOL 707 288264 FCHOPPER © TEXAQ] TEXAS NATURAL GAS 1/05/86 TKoOGr 1/05/87
T3492 00 FORD 1700 700982 A-TRACTOR —TWOSO1 AMY TWOSKOES 1/93/86 rvoo01 103/87 -

  

An example of the Sold Units Report, which is sorted by unit number,
follows:

UNITS


   

UEE"S RENTAL COMPANY Pate 12/11/96 Page 2
IANDEN, WA a Tine 32.17.28 2820-18

From: 6/00/00 To: 12/12/96 : 2 Serial: Sort Method: UNITE

Invoice Warranty
Stock 1 Year make Model sha Description addr 1 customer Date Nusber Date Code

BHIg00 00 CASE 440 266899F423 O-BACKHOE = GRADO1 LEROY GRADY 5/01/86 eso0517 903/86

FES#62 00 FORD 758 aag62 O-BACKHOE GRADO LEROY GRADY 2/01/86 INVOL 2401/87
PTOS¢2 00 FORD és00 coozase A-TRACTOR —-BOULOI SLIM BOULDERMAN 3/15/86 MAR UNIT 2/15/87
FTS492 00 FORD ©3700 ‘u700982 ASTRACTOR —TWOSO1 AMY ‘THOSHOES 1/03/86 rvooo2 1703/87
T5768 CO FORD 2500 0502617 A-TRACTOR — HOOKO2 CARL HOOKER 115/e6 rvaca2 1/15/87
P5509 90 FORD 7600 637578 ASTRACTOR —-BOULO1 SLIM BOULDERMAN 5/01/86 ES0Gz03 5701/86
SNH281 00 NEW HOD 707 228366 F-CHOPPER TEXAO1 TEXAS NATURAL GAS 1/05/86 INO001 1/05/67
432LV5 96 HONDA ACCORD 1 HGHAS432GA003947 4D LX TWOSO1 AMY TWoSHOES 5/01/86 2s00633, 5/01/87

 

### Fields & Descriptions (

The fields on the Sold Units Report are described below.

Stock No. Number of the stock unit sold.
Year Last 2 digits of the model year.
Make Manufacturer of unit.
Model Manufacturer's model number for unit.
Serial Number Manufacturer's serial number for item.
Description Brief description of the unit.
Address No. Address number of the customer who
purchased item.
Customer Name of the customer who bought the unit.
Invoice date Date of the invoice and sale.
number Number of the invoice.
Warranty date Expiration of the warranty on the item.
code Warranty code, set up by the dealer.

RELEASE 2.1 —

## CHAPTER X28-3

UNITS SALES REPORT

### Introduction

Units Sales Report lists:

= all units sold during a specific time period, for example, a day, week,

month, or year of sales.
= any month or year in file for the past 5 years.
= all sales for a specified salesperson identification, if requested.

### How To Run

From Menu Name:
Units Sales Report

Type in:
General Ledger Month
and Year

OR

Transaction From/To
Dates

Salesperson ID
(as entered SOLD BY at POS.)

Press:

FIELD EXIT

ENTER


[2] X28-3 UNITS SALES REPORT

Note:
The General Ledger Month and Year must be blank if Transaction
From/To Dates and Salesperson ID are entered. The possible
combinations to enter are:
1. G/L Month & Year
OR

2. Transaction From/To Dates and Salesperson ID

Do NOT enter all three:
1. G/L Ledger Month & Year
2. Transaction From/To Dates
3. Salesperson ID

 

The Units Sales Report screen is illustrated below.

## X28-3 UNITS SALES REPORT

ABC COMPANY UNITS SALES REPORT 2830-101,

To generate report by general
ledger month and year select

To generate report for a specified
time period select the following
transaction dates

To generate report by Salesperson
ID select i

Selection of Salesperson 1D will only list sales
since the last Point of Sale End of Month was run.

Press CMD i to end job.

 

RESULT: :
The Units Sales Report will be placed on the job queue.

 

UNITS


‘3 UNITS SALES REPORT

An example of the Unit Sales Report follows.

AGR_QUIPMENT UNITS SALES REPORT Date $/24/97 Page 1
LYNDEN, WA Selected Units Report Time 9.29.18  x2100-48

options: GL nate....
From pate’ | | 95/01/97
To pace . : > | 98/31/97
Salesperson 1D
Salesperson

Unie make Mode Ye MU Se PC Color ice Engine # 0 Sug List Dir list
FES793, 775-5 06 3 6 37.00 1,932.00
Serial Description _Indate Warr Trade G/L ect. ise
17653 N-LOADER, oi2aer 8 A324g
~-Sale wation==

Sold Dace Document # sold by Sold for Gr Profit Margin § Warr Date Wi
LEROY GRADY 6/38/97 TESTSALE 3 3000.00 863.00 28-77 8/17/39
>-Unit Trans--

Month ID Dace Invoice # —-Descripti GyL acct amount Type addr ¥ code

aug * 8/18/97 usas78 SALEDH/0 34240 2037.00 Wf CASHA

aug 2/18/57 use576 SALE>W/0 31240 2037.00- Ww a

gan 1/86 «17853 LoAt i240 183700, w


"

 

Ww
bug 12/97 FEST W/O.1 STUFF F 1240 200.00 Ww
TEST W/O 2 AFTER SALE W

AGR EQUIPMENT SAL UNITS SALES REPORT Date 9/26/97 Page
LYNDEN, Wa, Selected Units Report Time 9.29.20 x2100-SE

Options tee Model 2. G/L pate...
y. New/Used Code’ (xu) From Date  05/01/97
Product code . (PC) To Dace. |. | 08/31/97
: Serial Nurber . Salesperscn 15 |
Leeation . Bivis. ted Salespersen
Description

sale
anounc
Make/Model:

020.00

++ wake:

 

 


X28-3 UNITS SALES REPORT [=]

### Fields & Descriptions

The Units Sales Report fields are described below:

Stock# Unit's identifying number.
Make Manufacturer of unit.
Model Manufacturer's mode] number.
Description Brief description of the item.
Specs Features of the unit.
SR# Serial number issued from the manufacturer.
Eng# The engine number of the unit.
ID Sold identification.
Loc Location of the unit in your dealership.
Date Date the unit was entered into inventory.
Disc Allowable discount on item.
War Dealer-defined code for type of warranty on
item.
Special Price if a special is being offered on this
item.
Price The suggested list price.
Sold... Information about the sale of the unit.
Sold to Customer who purchased this unit.
Sale date Date the unit was sold.
Document Document number of sale.
Traded on Ttem taken in trade on this sale.
Ware date Date warranty expires.
War code Code for type of warranty.
Sold for Dollar amount of sale.
Gross Profit Total amount of profit on sale.
Margin % Percentage of profit on sale.
Trans Transactions on the unit.

UNITS


[ «| X28-3 UNITS SALES REPORT

Subtotal

Washout

Stock#
Inv. days

Date sold
Sold for
Cost

Margin
Trade on
Washout tree

Washout totals

Includes Transaction ID (* is system
automatically generated; others are your
codes), Posting Date, Invoice or Document
Number, and D=Debit, C=Credit.

Dollar amount of cost transaction. Listed
above SUBTOTAL are amounts for
corresponding transactions

Includes profit margin for sales and
trade-ins.

Unit's identifying number.

Number of days the unit has been in
inventory.

Date of unit sale.

Dollar amount of sale.

Cost of unit. (
Margin of profit on sale.

Item stock number traded in on this sale.
Lists the item stock number traded in.
Lists the stock number sold.

Dollar totals on cost and price, and profit
margin.

(
RELEASE 2.1 MS

## CHAPTER X28-4

SALES HISTORY ANALYSIS

### Introduction

Sales History Analysis reports on:
= each unit sold by make, model, and description.
™ customer who purchased the unit.

### How To Run

From Menu X28 select option 4 to run Sales History Analysis. At the
security gate, type Y to include all divisions on the report or N to include
only one division.

RESULT:

The report will be placed on the job queue.

## X28-4 SALES HISTORY ANALYSIS

   

ABC COMPANY SALES HISTORY ANALYSTS Pate 20/02/86 Page 1
wmumnon, co ALL ‘Time 12.37.05 2840-28,
24 MONTHS HISTORY SEGINNING WITH THE CURRENT MONTH

MAKE, ‘MODEL DESCRIPTION ocr SEP AUG) ssUL,s MN. MAY. «APR MAR FEB JAN DEC ROW.
case. R90 s-souD

ocr sep AUG), UN MAY. «APR MAR FEB AN DEC NOV.


stock # SERIAL 1 DESCRIPTION NEW/USED PRODUCT CODE YEAR COLOR soup TO
SPECIFICATIONS
00287 s-soxb BELLINGS BODY SHOP
SOLD 70 BELLINGS BODY
00258 s-Soun LLIN NORTE
SOLD TO ELLEN MoRTY
MAKE ope. DESCRIPTION ocr SEP AUG) UL, JUN MAY APR HAR PE JAN DEC ROW.
case 1594 ASTRACTOR

ocr SEP AUG, UL. UN. MAY APR MAR PER JAN (DEC KOV.


smock # SERIAL 4 BESCREPTION NEW/USED PRODUCT CODE YEAR COLOR
SOLD TO SPECIFICATIONS
43027 A-TRACTOR CLARENCE LONGE
15450. O/a

WAKE woos, DESCRI?TION ocr SEP AUG) oUL JUN MAY. «APR MAR OFER JAN DEC NOV.

case 4690 A-TRACTOR

oct SEP AUG «UL, sou MAY. APR MAR FEB JAN DEC (NOV.
1
STOCK # SERIAL # DESCRIPTION NEW/USED PRODUCT CCDE YEAR COLOR SOLD TO
SPECIFICATIONS
430238861746 A-TRASTOR RONALD SU2ER
43500. 97a
MAKE MODEL DESCRIPTION ocr SEP) AUG) oUL JUN, MAY. APR MAR) FEB JAN
case au s-NISC
oct SEP AUG «UL. JUN, MAY. APR) MAR FEB JAN
4
STOCK 4 SERIAL # DESCRIPTION NEW/USED PRODUCT CODE YEAR COLOR sou TO
SPECIFICATIONS
43033 a-MIsc, ‘CLEON LANGE
CELON ZAG

 

RELEASE 2.1 QL


 

### Fields & Descriptions

The fields on the Sales History Analysis report are described below:

Make Manufacturer of unit.

Model Manufacturer's model number.

Description Brief description of the unit.

24 Months listed Sales history with # of sales under month of
sale.

Stock # Unit identifying number.

Serial # Manufacturer's serial number for unit.

Specs Features on item.

Sold to Name of customer who purchased item.

Note:

This report lists Units sold in the last 24 months. If you desire history
on a sale before then, consult the Sold Units Inquiry (X2-3).

 

UNITS


Notes:

RELEASE 2.1 NW.

## CHAPTER X28-5

UNITS MASTER REPORT

### Introduction

Units Master Report lists:
- all information on units in inventory, including
" unit specs
™ prices & costs
™ vendors
" all invoices & work orders
= accumulated costs & rental revenues
® rental rate key
® traded information

### How To Run

From Menu X28 select option 5 to run Units Master Report.
RESULT:

The screen will note that the report has been placed on the job queue. The
report will print.

### Units Master Report

ABC COMPANY UNITS MASTER REPORT Date 10/02/86 vage i
wHENOT, 09 ” ‘time 0.00.00 2880- 1A
STOCKY MAKE MODEL DESCRIPTION NEW/USED PRODUCT CODE YEAR COLOR «= SR #/ ENG # LOC DATE DISC SPECIAL PRICE
SPECIFICATIONS

00323 oF o-MTsC
CORN KIT F/759-850
cOST..... 339.77 RENTAL REVENUE... RENTAL RATE...
L 10/18/84 CHANCE miz0 339.77
TOTAL
00322 MF 1143 C-CORMHEAD 83227 21-81 19717,09 $13300.50
1438-802,918,919
COST..... 9324.25 RENTAL REVENUE... RENTAL cos. RENTAL RATE, RADED ON.
% 10/18/84 CHANGE niz0 9326.15
Tora 9224.18
90323 MF 3142 (C-CORNEEAD 53422 Od-m1 1722.00 §12720.25
1438-802

COST..... 10398,14 RENTAL REVENUE... RENTAL RATE. TRADED ON.

1B 10/18/84 CHANGE 220 10398.44
TOTAL 10298.14

00325 MF 520 G-TILLAGE 19365 02-81 7890.00 $8576.00
21 DESC HARROW, 333-219, 324, 481, 1867-725. 784,890,922

cosT..... 7049.07 RENTAL REVEWUE..... REIAL COST..... REVTAL RATE, ‘TRADED ON.
L osievea cmANGE = ob N20 6603.76 L 2/19/85 Ro 03686 D120
AJE WIS 405.33

‘TOTAL, 7949.07

00335 MF 298 AsTRACTOR 702763 91-61 23122.00  §28164.00
MP, STD. CL.

cosT..... RENTAL REVENUE... RENTAL COST. RENTAL RATE... ‘TRADED on,

4/15/86 312994 e120 F298 19486.28-

20/18/84 CHANGE =D N120 novieyed 19486.28

32/32/84 00335 D Niz0 Rr 629.00

4/22/86 AJB W/G C120 FREIGHT 629.00-


UNITS

### Fields & Descriptions

## X28-5 UNITS MASTER REPORT

The fields on the Units Master Report are described below.

Stock#
Make
Model
Description
Specs

SR#

Eng#

Loc

Date

Disc
Special
Price

Cost
Rental revenue

Rental cost

Rental rate
Traded on

Unit's identifying number.

Manufacturer's name.

Manufacturer's model number.

Brief description of unit.

Features of the unit.

Serial number of the item.

The engine number of the unit.

Location of item in your dealership.

Date the unit was entered into inventory.
Permitted discount on item (070=7%).
Price if a special is being offered.
Suggested list price for this item.

Cost of item to dealership.

Amount to-date accumulated for rental on
this item.

Amount to-date accumulated rental cost on
item.

Rate for the rental of the item.

Stock number this unit was traded on.

Next you'll see the transactions for each item listed, in this order:

Transaction ID

Posting Date
Document #

- is a system- automatically-generated
transaction. Other transaction IDs are
dealer-defined.

Date the transaction was posted.

Number of sale document (invoice number).


 

Debit/Credit Action on the general ledger account
number.

Account # General Ledger Account Number affected.

Description Description of the transaction.

Total Total dollar amounts of transaction(s).

‘

RELEASE 2.1 Nw

## CHAPTER X28-6

UNITS G/L PERIOD REPORT

### Introduction

The Units G/L Period Report lists:

= all available units with an inventory balance in the month selected for
the report

™ units specifications if requested

™ report recap of inventory account totals

Note:

The Units G/L Period Report does not necessarily list all units in
inventory. It lists only those units that have cost posted to them for the

month requested. It is a summary of the inventory subledger, just as

the Aged Receivables Report is a summary of the Accounts Receivable ]}
subledger and reflects only those customers who had active balances i
the month requested.


X28-6 UNITS G/L PERIOD REPORT

 

### How To Run

From Menu X28 select option 6 to run the Units G/L Period Report. The
following screen appears:

AUSTIN EQUIPMENT COMPANY Units G/L Period Report *2860-101
Division A Selection Screen

Enter month for units g/l pericd report

Open or closed month? (0 or C)

Print extended specifications for each unit? {¥ or N) . .

 

Type the number of the month you want (1-12). The report will give you
inventory balances as of the month you request. Type O if the month you
requested is open or C if it is closed. Type Y if you want the unit
specifications to print. The default is N. Press Enter. The Units G/L Period
Report will be placed on the job queue.

An example of the Units G/L Period Report follows.

RELEASE 2.1 ~


X28-6 UNITS G/L PERIOD REPORT

 

LEE'$ RENTAL COHPANY units G/t Period Report Date 12/21/96 Page 1.
LYNDEN, WA DETAIL: 9/56 vine 12.17.52 2860-30

Stock! YR make Description >
1200 (NEW TRACTORS

‘e* a1200 NEW TRACTORS

FTO762 00 FORD 6600 ceai2es 21462.00

Frosgs 60 PoRD 7700 3642972 23215.00

PPS852 09 FoRD wo 2629362 27686.94

TOTAL 2200 72363.94

se) a1240 New EQUIPMENT b
A1240 NEW EQUIPMENT :

25798 CO FORD 770-5 17853 1637.00
NHO224 00 NEW HOIIA 283 489828 5319.92 :
WHS714 00 NEW HOLLA $19 507836 3291.00
NHS822. 00 NEW HOLLA 770-W 206690 1850.09

1 TOTAL A2240 12297.92

L250 USED TRACTORS & EQUIPMENT
+ AL250 —_US2D ‘TRACTORS & EQUIPMENT

FE2228 76 FORD Lena RIDING MOWER 1000.90
seee* roman A1250 2000.00

vee n1260 MEW AUTOS :
81260 NEW AUTOS

419LVS 86 HONDA ‘ance JHMARS52xGC004118 8100.00
weeee pom A1260 8100.00

81270 USED AUTOS
s**/A1270 USED AUTOS

UNIT?3. 73 CORVETTE HOT NgWi9S0 5000.00
732EAR 84 HONDA ‘ACCORD ‘149A 743182998948 4090.00

TOTAL 1270 3009.00

s** 31620 USED RENTAL EQUIPMENT
s** 21620 USED RENTAL EQUIPMENT

FAO6@2 00 FORD 5600 coozasga 18425.00
7R1000 00 CASE 580c ses4nEsee3, 124.60-
R2000 86 CASE s80c 2essa3r2¢5, 4898.56

 

UNITS


X28-6 UNITS G/L PERIOD REPORT

 

### Fields & Descriptions

You will see the following fields on the report:

Stocki# Unit's identifying number.
Year Last 2 digits of the model year.
Make Manufacturer's name.
Model Manufacturer's model number.
Description Brief description of the unit.
Specs Features of the unit.
Extended specs Extended space for features.
SR# Serial number of the unit. (
ID Sold identification. .
Loc Location of the unit in your dealership.
Date Date the unit was entered into inventory.
Cost Cost of the unit to your dealership.
Whole goods or units recap
Account Includes the account title and G/L account
number.
Cost Dollar amount of cost to each vendor
account.
Flooring Dollar amount of flooring to each vendor
account.
Grand totals Total of current inventory in dollar amount.

RELEASE 2.1 Ne?


LEE‘S RENTAL COMPANY

LYNDEN, WA,
Account

1200
1240
1250
A260
1270
as20

#2 TOTAL

UNITS.

cost-$

72363.94
1297.92
1000.00
8200.00
9900.00
103298.76

205960.62

 

X28-6 UNITS G/L PERIOD REPORT

 

 
   
  
   

Note:

  

This report sorts by General Ledger Accounts. The recap at the end of
the report provides the inventory account totals. These totals may be
used to reconcile General Ledger inventory account totals.

   

Units G/L Pexiod Report Pate 12/11/96

Page 2
RECAP: 9/96

‘vine 21.17.52 2860-38


Notes:

RELEASE 2.1 LL

## CHAPTER X28-7

FLOORED UNITS REPORT

### Introduction

Floored Units Report lists:

= all units that have been floored.

= whether the item is sold, indicated by a * to the left of due date.
= subtotals by vendor for appropriate accounts.

### How To Run

From Menu X28, select option 7 to run the Floored Units Report. At the

security gate, type Y to include all divisions on the report or N to include
only one division.

RESULT: The Floored Units Report will be placed on the job queue.

## X28-7 FLOORED UNITS REPORT

   

This is a sample floored units report.

LEE'S RENTAL COMPANY FLOORED UNITS REPORT pate 12/11/95
LYNDEN, WA ‘Time 11.17.54

CASEO2 caSE 1H Date Entered 86/01/01
RACINE, WI Phone #

Unit # Yr. Make Model SRE Date Doc # acct Desc Gross Net Due
BH1000 00 case 440 266999"423 1/20/96 TRODD4 =—-a2260 BACKROE 18216.00 1e216.00 * 5/01/86

v7" vendor Subtotals 18216.00 119216.00

FORD MOTOR COMPANY Date Entered 96/01/01
2500 MAPLE RD
‘TROY, Mr 42048 Phone #

Yr. Make Model SR # Pate Doc # Acces Dese cress wet, ue
00 FORD 770-5 37853 1/01/86 17653 32200 LoaDen 1937.00 1e37.00 99/99/99

09 FORD 758 80063 2/04/86 ROR 42200 SETTLEMEN —42000.00- 42000.00-499/99/99
00 FORD 758 80062 1/01/86 80063 182200 BACKHOE 4200.00 2000.00 * 2/01/86
7 Stock Subtotals t**

00 FoRD 6600 © co02460 1/03/86 CC02468 2200 TRACTOR 22462.00 2462.00 + 3/15/86
00 FORD 6600 © co02468 3/15/86 MAR ROR UN A200 21482.00- 21462.00-* 3/25/86
‘t* Scock Subtotals +++
00 ForD ©6600 cz249 1/01/86 C621249 2200 TRACTOR 22462.00 21462.00 99/99/99

00 FORD «7700 «0642972 1/01/86 0642972 2200 TRACTOR 23215.00 23215.00 99/99/99
00 FoRD «1709700982 3/01/86 U700982 42200 TRACTOR 7428.00 7428.00 * 1/02/85
00 FORD = 150002617 2/01/86 US02617 42200 TRACTOR 6875.00 6875.00 » 1/15/86

00 7600 © 9637878 5/02/86 C627578 42200 7600 25235.28 15235.28 * 5/01/86

00 Tmo 639362 5/01/86 629362 42200 THLO 27532.31 22832.31 6/01/86

s** Vendor Subtotals *** — 10388¢.59 103584.59

= daca deleted here ===:

1 Report Totals *** — 126472.29 122672.29

 

RELEASE 2.1 —


LES'S RENTAL COMPANY
LYNDEN, WA

Agcount
NOTES PAYABLE-FORD 02200

NOTES PAYABLE-NEW HOLLAND 42210

NOTES PAYABLE-CASE 2260

Grand Totals

UNITS


FLOORED UNITS REPORT pate 12/11/36 Page 1.
RECAP BY GENSRAL LEDGER ACCOUNT ‘Time 11.17.57 2879-28,

Flooring
103584.59

6671.70

18216.00

128472.29


Notes:

RELEASE 2.1 a

## CHAPTER X28-8

INVENTORY/FLOORING REPORT

### Introduction

Inventory/Flooring Report lists:

= all current inventory and specifications

report recap of inventory account totals

all units that have been floored

whether the item is sold, indicated by a * to the left of due date
subtotals by vendor for appropriate accounts

This report summarizes the Current Inventory Report (X28-6) and the
Floored Units Report (X28-7).

### How To Run

From Menu X28, select option 8 to run the Inventory/Flooring Report. At
the security gate, type Y to include all divisions on the report or N to
include only one division.

RESULT: The Inventory/Flooring Report will be placed on the job queue.


X28-8 INVENTORY/FLOORING REPORT

 

This is a sample Inventory/Flooring Report:

LEE’S RENTAL COMPANY INVENTORY/FLOORING DATE 12/11/96 = PACE 1
LYNDEN, WA REPORT TIME 11:18:10 X2880-201

G/L Inventory Account: A1200 NEW TRACTORS

Unit# Color Yr. Mcke Medel Description Serio Id Loc Date Cost. Flooring Due Vendor
Fr0781 00 FORD 6600 A-TRACTOR == 621249 LO $-81 21,462.00 21,462.00 99/99/99 FORDOZ
FTO888 QO FORD = 7700 A-TRACTOR == 642972 LO 1-81 25,215.00 23,215.00 99/99/99 FORDOZ

FTS492 CO FORD = 1700 A-TRACTOR = U70882 MO 1-81 ++ SOLD + 7,428.00 1/03/86 FORDO2
FTS539 OO FORD = TWI0 A-TRACTOR C6 16601 LO 1~81 0 + NONE ++ (
FTS768 00 FORD 1500 A-TRACTOR —- 502617 MO 1-81 + SOLD x 6,875.00 1/15/86 FORDO2
#715809 OO FORD = 7600 A-TRACTOR (637578 NO 1-81 #2 SOLD ++ 15,255.28 5/01/86 FORDOZ
£15854 CO FORD = TWI0 A-TRACTOR = —C639362 MO 1-81 27,686.94 27,532.31 6/01/86 FORDO2

» Subtotal A1200 72,363.94 101,747.59

 

t
RELEASE 2.1 NL


X28-8 INVENTORY/FLOORING REPORT

 

### Fields & Descriptions

You will see the following fields on the report:

Unit# Unit's identifying number.

Color Color of the unit.

Year Last 2 digits of the model year.

Make Manufacturer of the unit.

Model Model of the unit.

Description Brief description of the unit.

Serial# Serial number of the unit.

Id Sold identification.

Loc Location of the unit in your dealership.
Date Date the unit was entered into inventory.
Cost Cost of the unit to your dealership.
Flooring Amount owing on the unit.

Due Date the flooring is due.

Vendor Name of the flooring company.
Subtotal Total cost of the units listed on this report.

UNITS


Notes:

RELEASE 2.1 Ke

## CHAPTER X28-9

UNITS ON WARRANTY REPORT

### Introduction

Units on Warranty Report lists:

= all of the units still under warranty.

= the unit information, customer name, address #, invoice number and
date, warranty type and expiration date.

### How To Run

From Menu X28 select option 9 to run the Units On Warranty Report. At
the security gate, type Y to include all divisions on the report or N to
include only one division.

RESULT:

The report will be placed on the job queue.

 

ABC COMPANY Date 12/02/90 Page 3
wayNor, co Time 9.54.13 2890-18

Stock¥ YR Make sR Description addr # customer pate pate cade
DIXAZ4 89 DIXON 42427R 26772 +0 FOQ065 ORRREYN ENGLISH 6/30/89 ENGKOLM 0 10/25/30
90200 90 SNAPPER COMET r-0RE, 100330 HARV MERDT 4/23/50 MATDL x 42/93
00316 580 6126 W00080 GILBERT WENBERGER 11/20/89 WENDINGER 10/21/30
90324 1183 212008 00240 RICHARD & ROBERT GOLAND 10/21/91 GRONAD R 10/03/32
00336 3505, 0K290206 ‘00102 WILLIAM ADAKS 2725/90 us4se7 9725/25
20335 224 2000572 ‘A00L02 WILLIAM ADAMS 9/25/85 usass7 9/25/90
00355 340 1734 600275 JaFF GRIFFIN 5/14/88 GRIBBEL J 12/31/90
43804 1018 143 HODOS6 DARYS D. HARTED 12/30/89 HELCET D 12/28/90
43808 115 1042 ‘800102 WILLIAM ADAMS 8/15/90 Yss578 8/15/91
43812 1018 3499 A00102 WELLIAM ADAMS Briss91 usE578 Briss92
43817 1919 41365 500115 LEROY GRADY 8/18/89 uses79 8/15/90
43826 1060 40230 00058 DARYL, D. ARNOLD 12/30/90 HELGE? D 12/28/91
42921 90 LINDSAY 8 68774973 900260 SARNEY HOLTZNEX 12/30/90 HOLTMANN 3 12/13/92

## X28-9 UNITS ON WARRANTY REPORT

 

### Fields & Descriptions

The fields on the Units on Warranty Report are described below.

Stock No. Unit stock number.

Year Last 2 digits of the model year.

Make Manufacturer of unit.

Model Manufacturer's model number.

Serial Number Manufacturer's serial number.

Description Brief description of the unit.

Address No. Address number of the customer who
purchased item.

Customer Name of customer who purchased the unit.

Invoice date Date of the invoice or selling document. {

Number Number of the invoice.

Warranty date ‘Warranty expiration date.

Code Warranty code, dealer- defined.

RELEASE 2.1 NS

## CHAPTER X28-10

RENTAL STATUS REPORT

### Introduction

The Rental Status Report replaces the Rental Availability Report. You can
select units by:

= make/model ™ serial number
™ rental status code ™ description
= location © year

or any combination of these items. You can choose to print only those
units whose status has changed since the last time the report was printed,
and you can choose to include or omit comments 7-9 (1-6 always print).
The information listed on the report includes:

= unit # ™ serial number
= make = location
= model ™ product code
= year " hour meter
= description = current rental status & related
fields
= color = comments 1-6, comments 7-9
optional
The units are listed in order by make/model/unit number with a blank line
between different models.

### How To Run

From the Rental Report Menu (X28), select option 10, Rental Status
Report. The Select Units screen appears.

## X28-10 RENTAL STATUS REPORT

   

Select Units Screen

ABC COMPANY RENTAL STATUS REPORT x2A10-201 1
Select Units

Select a combination of the following:

Make . - + + CASE
Model. » . DS2642
Rental Status Code . .
Location... .
Serial number
Description

 

print only changed units (¥/N) ? N
Include comments 7 - 9 (Y/N)? ¥

Gmdl-End job Enter-Continue

 

Type your request, and press [Enter] to continue. The report is placed on
the job queue.

RELEASE 2.1 NN


UNITS


 

Note:

Make and model must be requested together. You can use a partial
serial number; however, all other fields must be complete and exact
matches.

 

The list of valid status codes follows:

Null Status *
Available AV
Rented RE
Waiting for delivery WD
Waiting for pickup WP

Waiting for light service WL
Waiting for major service WM

Light Service LS

Major Service MS

Sold so

Demo DE

### Options

{Cmd1] End this job. Return to the Units Menu.
{Enter] Completes your request. The system locates

the units and prints the report.


 

An example of the Rental Status Report follows.

Deve 8/30/90 Page 1
‘rime 10.32.19 2K102-01

aA

Unité Description Serialt Coler Yr FC LC

5070A2 CE-BOCKET
5316A3 CB-BUCKET

5316A4 C2-BUCKET

5316A5 CS-BUCKET

SS79A2 CE-BUCKET

 

RELEASE 2.1 LO


UNITS

### Fields & Descriptions

 

The fields on the Rental Status Report are described below.

Make
Model
Unit#
Description
Seriali#
Color

Yr

PC

Lc

Meter

RS

9-characters. Manufacturer of the unit.
9-character model number.

5-character unit number assigned in
Inquire/Update units (X2-1)

11-character description of the unit from the
unit's master record (Inquire/Update Units,
X2-1).

Serial number of the unit.

5-characters. May be used for color of the
unit.

2-digits representing the year of
manufacture. 1990 is represented as "90."
2-character product code.

2-characters. Location of the unit.

7.1 digits. The number of hours on the hour
meter.

2-character rental status code. See the list of
rental status codes above.


Notes:

!
RELEASE 2.1 NS

## CHAPTER X28-11

RENTAL STATUS HISTORY ANALYSIS

### Introduction

The Rental Status History Analysis allows you to select units by:
= make/model ™ serial number
= rental status code = description
© location = year

or any combination of these items. The information listed on the detail

Teport includes:
" unit # «color
= make ® serial number
= model = location
™ year = hour meter
= description = Year-To-Date days &
percentage for each status
code (YTD)
= Life-To-Date days &
percentage for each status
code (LTD)
You can choose to print a summary by make and model instead of the
detailed report.

### How To Run

From the Rental Report Menu (X28), select option 11, Rental Status
History Analysis. The Select Units screen appears.

## X28-11 RENTAL STATUS HISTORY ANALYSIS

Select Units Screen

RENTAL STATUS HISTORY ANALYSTS
Select Units

Select a combination of the following:
Rental Status Code . .
Location

Serial number
Deseription -

Make/modei summary only (¥/N) ? ¥

Qrdi-End job Bnter-Contime

 

Type your request, and press [Enter] to continue. The report is placed on
the job queue.


UNITS


 

Note:

Make and model must be requested together. You can use a partial
|| serial number; however, all other fields must be complete and exact
| matches.

 

The list of valid status codes follows:

Null Status +
Available AV
Rented RE
Waiting for delivery WD
Waiting for pickup WP

Waiting for light service WL
Waiting for major service WM

Light Service LS

Major Service MS

Sold so

Demo DE

### Options

[Cmd1] End this job. Return to the Units Menu.

[Enter] Completes your request. The system locates
the units and prints the report.


 

An example of the Rental Status History Analysis Report follows.

ARC COMPANY RENTAL STATUS HISTORY ANALYSIS Date 8/30/90 Page 1
R ‘Time 10.35.06 1x2A202-01
make Model
Unit# Description serialt Ye LC Meter RentDt RS HEADER HEAPER2 READER? HEADER HEADERS HEADERS HEADER? HEADER@ HEADERS
Total 88 RE ot owe ot wD oS om 8 om 8 Is 8 oOUS so

CASE ps26¢2

‘3064A3 CE-BUCKET 20598 RE JAMES ¢ 8/30/90
yr 241 18 6: : :
uD soa: : Bo oo 38 6
SO70A2 CE-BUCKET 42088 RE
YrD 242 242 100
LD a54 954 100
531603 CE-BUCKET 121288 RE
2a 242 400 :
€26 626 100 :

 

SS16A5 CR-BUCKET 101388 RE
ym 241241 100

LID 686 686 100

5579R2 CE-BUCKET 51389 RE
vm 241

umm 478

‘Subtotal
yD 1445 (754 52: 31L
UMD 4336 2187 50 : 1139

 

RELEASE 2.1 LL


 

### Fields & Descriptions

The fields on the Rental Status History Analysis Report are described

below.
Make 9-characters, Manufacturer of the unit.
Model 9-character model number.
Unit# 5-character unit number assigned in
Inguire/Update units (X2-1)
Description 11-character description of the unit from the
unit's master record (Inquire/Update Units,
X2-1).
Serial# Serial number of the unit.
Yr 2-digits representing the year of
manufacture. 1990 is represented as "90."
LC 2-characters. Location of the unit.
Meter 7.1 digits. The number of hours on the hour
Meter.
ReatDt Rental start date.
RS 2-character rental status code. See the list of
rental status codes above
Title 1 - Title 9 Headers for Comment 1 - Comment 9
Rental Status Codes See list of rental status codes above.
YTD Year-To-Date. The number of days this year
that the unit has held this status.
% Percentage of time this year that unit has
held this status. The formula is:
= + days at this status this year
total # days from beginning of year
LTD Life-To-Date. The total number of days that

the unit has held this status since its rental

UNITS


BBC COMPANY
a
Make Model
Unite Description Serialé
Total *

CASE ps26d2

rs

Subtotal,
ym 241
uD

start date.
% Percentage of time that the unit has held this
Status since its rental start date. The formula

Is:
B= total # days at this status
total # days since rental start date

An example of a Rental Status History Analysis Report, Summary Only,
follows:

RENTAL STATUS HISTORY ANALYSIS Dace 9/30/90 Page ot
‘Time 10.38.25 2a202-01

Ye LC Meter RentDt RS HEADER] HEAPER2 HEADER3 HEADERG HEADERS MEADERS HEADER? READERB READER
Rea OPS MS a 80 8 OTE OR

 
LL

## CHAPTER X28-12

RENTAL UTILIZATION REPORT

### Introduction

The Rental Utilization Report can be printed for one division or for all
divisions. It lists, by unit, the amount of revenue a unit generates and
compares this with the cost of renting the unit. This report is helpful when
determining the profitability of specific units. It can also help you decide
whether to discontinue certain units or purchase more cost effective units.

Like other rental reports, the Rental Utilization Report is sorted in order by
Make, then Model. Subtotals are calculated for each Make/Model group.

### How To Run

From the Rental Report Menu (X28), select option 12, Rentals Utilization
Report. After the security gate, the Select Units screen appears,


[2 | X28-12 RENTAL UTILIZATION REPORT co

Selection Screen

RENTAL UTILIZATION REPORT X28C0-101 4
Select Units

Select a combination of the following:

Rental Status Code
Location... .
Serial number
Description

Make/model summary only (¥/N) ? N

Gmdi-End job Enter-Continue

 

Type your request, and press [Enter] to continue. The report is placed on
the job queue.

RELEASE 2.1 Ne


X28-12 RENTAL UTILIZATION REPORT [2]

Note:

Make and model must be requested together. You can use a partial
serial number; however, ali other fields must be complete and exact
matches.

 

The list of valid status codes follows:

Null Status *
Available AV
Rented RE
Waiting for delivery WD
Waiting for pickup WP

Waiting for light service WL
Waiting for major service WM

Light Service LS
Major Service MS
Sold so
Demo DE

UNITS


[ «| X28-12 RENTAL UTILIZATION REPORT

 

An example of the Rentals Utilization Report follows:

 

ABC COMPANY
BELLINGHAM, WA A
¥28002-01 Hake Model
Unit# Description Seriale Ye ic Meter Deprec. Rent Dr. Days ays.
(eacctees Life-to-pate “yt Year-to-Date. -- (escene Average Monthly ~

(Rent Rev. Rent Cost Margin) (Rent Rov, Rent Cost Margin) (Rent Rev. Rent Cost Mazgin)

case 440

RENTAL UTILIZATION REPORT

BH1G00 0-EACKEOE —-266899F423 1823284 asaosag
35.60 25.94 60.0 126

Subtotal 16231.54
15-84 60.0

TR1000 O-BACKAOE == 46S¢RESG41. 1/10/86
312.00 124.80 60.9 2.01

R000 O-BACKHCE ©—-266589F245 eaass.56 arr0 786
2.02

subtotal 8477.76
625.60 250.24 60.0

FAS796 M-LORDER 278538, 480.00- 3/20/86
1200.00 480.09 60.0 200.00 60.0, 1B

Subtotal i688 1032
1200.00 400.00 60.0 : 73, 60.0

FORD 700
PTOGBE A-TRACTOR 642972 23215.00

23215.00

532-35

92243 GRADALL
5000.00 2000.00 60.0 5000-00 2000.00 60.0 2136.75
subtotal 318750.00
3000.00 2000.00 60.0 3000.00 2090.00 60.0 2136.75

CANE 4/0166070 91 BL 5863 119750.00

Dace 3/13/91,
‘Time 8.03. 59
‘Total Rental

 
LC


X28-12 RENTAL UTILIZATION REPORT [=]

### Fields & Descriptions

The fields found on the Rental Utilization Report are described below in
the order in which they appear from left to right:

LINE 1:
Make
Model
LINE 2:
Unit# Unit identification number.
Description
Serial# Serial number.
Yr Year.
Lc Location.
Meter Hourmeter reading.
Cost Cost of the unit.
Deprec Depreciation accumulated on the unit.
Rent Dt. Rental Start Date.
Total Days Days from Rental Start Date to date of the
report.
Rental Days Number of days that Rental Status=REnted
Rent/Total Percentage of total days that unit has been
rented, Rental Days divided by Total Days.
LINE 3:
Life-To-Date
Rent Rev. LTD Rental Revenue generated by this unit.
Rent Cost LTD Cost attributed to this unit. Does not
include purchase price or depreciation.
Margin LTD Margin. LTD Rental Revenue divided
by LTD Rental Cost.

UNITS


[ «| X28-12 RENTAL UTILIZATION REPORT

Year-To-Date
Rent Rev.
Rent Cost
Margin

Average Monthly
Rent Rev.

Rent Cost

Margin

‘YTD Rental Revenue generated by this unit.
YTD Cost attributed to this unit. Does not
include purchase price or depreciation.
YTD Margin. YTD Rental Revenue divided
by YTD Rental Cost.

Average monthly Rental Revenue generated
by this unit.

Average monthly cost attributed to this unit.
Does not include purchase price or
depreciation.

Average monthly Margin. Average Rental
Revenue divided by Average Rental Cost.
LL

## CHAPTER X28-13

TRADED UNITS REPORT

### Introduction

For units sold through Point of Sale, the Traded Units Report furnishes the
information needed to claim notional Input Tax Credits (ITCs). It tracks
revenue from new unit sales and the amounts that were debited to used
inventory for trade-ins. The report, requested by date range, lists all "W"
edit code transactions for each unit, which, incidentally, provides a rough
washout tree.

   

    

 

Note:

 
 
 

| Only units sold at Point of Sale are listed on this report. If the GST
Method is "0" (zero), this report is not available.

 

 

### How To Run

Q To run the Unit Transaction Report, select option 12 from the Units
Menu (X2). A selection screen follows the security gate.


[2] X28-13 TRADED UNITS REPORT Co

TRADED UNITS REPORT 200-101 2
Select Units

Select unit sale information based upon a transaction date range:

Beginning transaction date
Ending transaction date 121090

Cmai-md job Enter-Continue

 

O Type the beginning transaction date. Type March 21, 1991 as 032191
and press [Field Exit]. The system uses the current session date as the
ending transaction date,

O Change the ending transaction date if desired, and press [Enter]. An
example of the report appears on the next page.

An example of the Unit Transaction Report is illustrated below.

RELEASE 2.1 \

## X28-13 TRADED UNITS REPORT

ABC-AG,AUTO,CONS & TRUCK CO. TRADED UNITS REPORT DATE 22/10/99, PAGE 2
BELLINGHAM, WA a From: 1/02/81 fo: §/15/51 Tame 15.27.45 x2c00-201

Deseription warranty

5/01/91 EsoDs12 29995.00 9701/31 1
s/o1/st es0si2 3000.00
2/01/91 rNvOL 48500.00 2/01/87
3/15/91 MAR UNIT 24700..00 3/15/87
1703/91 rvo002 8322.00 1703/87
1/03/91 zvoo01 1500.00
1/03/92 R901 00.00-

Prs76a 4/15/92 1v9002 8222.00 2/15/87

Frseos 5/02/91 8800203 18000,00 5/02/91

swuze1 2/05/91 road, 3630.00 1/05/87

aainvs 5/01/92 300631 9590.00 5/01/87

 

The report incidentally furnishes a rough washout tree: note the 4th deal
where the trade and its overallowance are listed.

UNITS


Notes:

i
RELEASE 2.1 Mee

## CHAPTER X28-14

CURRENT INVENTORY REPORT

### Introduction

Current Inventory Report lists:
= all current inventory and specifications,
™ report recap of inventory account totals.

### How To Run

From Menu X28 select option 14 to run the Current Inventory Report. At
the security gate, type Y to include all divisions on the report or N to
include only one division. The Current Inventory Report is placed on the
job queue.

LBE'S RENTAL COMPANY Date 12/12/96 Page 8
LYNDEN, MA ‘Tine 11.38.07 X2BR0-28,

Stock# YR Make Beseription Flooring Date vendor
Specifications

BU2010 95 THOR 98565639
302020 95 THOR 9903020

Bu2030 95 ‘THOR 9903030

Bu300 95 THOR 9903040

BU30S0 95 THOR 9903050,

3BU3060 95 cHOR 9903069,

303070 95 THOR 9903070,

303080 95 THOR 9903080

BUI090 95 THOR 9903080

Bx0100 95 xaro 29KB916S7H24093
Bx0200 $5 Karo 23K0200,

BxO200 95 KATO 2345240300
EXOG00 95 KATO 24K54993508782
EXOSOD 95 KATO 23K5240986A88787
BKOEO0 95 KATO 23K9576¢6uN88787
XO70C 95 KATO S9GRTKIa78798D12
Ex0g00 95 KATO 34K8734BN330034
EXOSO0 95 KATO 2397765347587

## X28-14 CURRENT INVENTORY REPORT

 

### Fields & Descriptions

The fields on the Current Inventory Report are described below:

Stock# Unit's identifying number.

Year Last 2 digits of the model year.

Make Manufacturer's name.

Model Manufacturer's model number.

Description Brief description of the unit.

Specs Features of the unit.

Extended specs Extended space for features.

SR# Serial number of the unit.

ID Sold identification.

Loc Location of the unit in your dealership. (

Date Date the unit was entered into inventory.

Cost Cost of the unit to your dealership.

Vendor Name of the flooring company.

Flooring Amount of flooring.

Date Date of flooring transaction.

Whole goods or Units recap

Account Includes the account title and G/L account
number.

Cost Dollar amount of cost to each vendor
account.

Flooring Dollar amount of flooring to each vendor
account.

Grand Totals Total of current inventory in dollar amount.

RELEASE 2.1 LO


LEE'S RENTAL COMPANY
LYNDEN, WA

Account,
NEW TRACTORS

NEW EQUIPMENT

28-14 CURRENT INVENTORY REPORT

 

 
   
 
 

Note:

  

This report sorts by General Ledger Account. The recap at the end of
the report provides the inventory account totals. These totals can be
used to reconcile General Ledger inventory account totals.

 
 

 

 

(CURRENT INVENTORY REPORT Dare 12/11/96 Page 2
RECAP BY GENERAL LEDGER ACCOUNT ‘Time 11.35.09 2850-28,

cost, Pleoring
aiz00 72363.9¢ 7209.32

a1240 2297.92 8508.70

USED TRACTORS & EQUIPMENT A1250 1000.00

Nea AUTOS

usep Auros

USED RENTAL S0UrPHENT

UNITS

1260 8100.00

1270 9000.00

A120 103198.76

205960.62 go7ze.o2


Notes:


RELEASE21 9 \~"

## CHAPTER X28-16

AGED INVENTORY REPORT

### Introduction

This new report offers a lot of flexibility in how it is printed. It can be
sorted by:

® a. Days-In-Stock, b. Year, then c. Unit#

= a. Year, b. Model, c. Days-In-Stock, then d. Unit#

= a. Model, b. Year, then c. Unit#

= a. Division, b. Days-In-Stock, then c. Unit#

You can request new or used units, or both, for 1 or all product codes.
If requested, summary statistics are added to the end of the report to
include the following calculations:

.™ Average days-in-stock
" Percentage of new units that have been in stock over 60 days
= Percentage of used units that have been in stock over 60 days
= Percentage of units that are the current year's model


X%28-16 AGED INVENTORY REPORT

   

### How To Run

From the Units Report Menu (X2-8), select option 16, Aged Inventory
Report. The selection screen is illustrated below.

Selection Screen

BOB‘S TRACTOR COMPANY AGED INVENTORY REPORT x28G01
Division: A Selection Scxeen 8/12/96

How would you like the report SORTED?
Please select one of the sort codes listed below...

1+ Days-In-Stock, Year, Unité (
2- Year, Model, Days~In-Stock, Unit#

3+ Model, Year, Unité
4
1

Division, Days-In-Stock, Unit#
Sort Option:

Selections: (New, [U)sed or (B)oth (N/U/B) : B
Product Code : (Blank for ALL)

Print ALL Divisions? (Y/N)
Summary statistics required? (¥/N): N

Printer Output Queue (F4 to Select) : PRTOL

(mdi-End Job Cmd4-Select Printer Press ENTER to continue

 

When summary statistics are requested, they added to the end of the
report. The same report detail is printed regardless of whether you ask for
sumunary statistics or not.


RELEASE 2.1 NN

## X28-16 AGED INVENTORY REPORT

 

Sample Report with Summary Statistics

 
   

         
        
      
        
   
 

   
   
         
  

 

 
 
    
  
        
   
   

   
   
  
       
          
   

         
      
       
      
   

BOB'S TRACTOR COMPANY Aged Inventory Reporte Date 2/12/96 Page 4
LYNDEN, WA a *** USED Vehicles += ‘Tine 13:37:28 xzeco2

Selection Criteria: Soxt-codes? Summay=¥ New/Used=B 0. Al1L-Div.2n .
stock DAYS In ORIGINAL, ADDED. Toran

NUMBER YEAR MAKE MODEL DESCRIPFICN COLOR SERIAL NUMBER ODOMETER 700K cost cost VALUE

E2220 76 FORD e725 RIDING MOWER 16063 589 1000.00 2,090.00 *
FE2228 76 FORD LeT125 RIDING HOWER 16063 $89 2,000.00 1,000.09

7322AR 64 RONDA. accoRD 4D LX WITTE 1HGAD7431eA0989¢8 207 4,000.00 4,008.00

TB2ERR 84 HONDA ACCORD 4D Lx. WHITE 1NGAD7¢a1EA0909¢8 7 4,000.00 4,000.90

869EAR 84 HONDA, ACCORD HB Lx. GRAY — 1nGAD73302A102825 307

S69EAR 6 RONDA ACCORD oe xx SRAY  1HGADT3302R101825 307

887EAR 85 HONDA civic ke. REO gHRH3329¢S029889 307

SB72AR 85 HONDA ervic Ha RED JHMAN3329FS029899 307 -
UNIT73 73 CORVETTE nor 73 VETTE RED NIWi950, 275 3,000.00 5, 000,00,

ONTT73 73° CORVETTE HOT 73 verre RED Ngwi950 25 5,000.00 5,009.00

cHevol 79° cuEy ces ‘Tuck RED ccessovi37810 244

cHEvel 79° curv css ‘TRUCK RED cezssovag7810 246

BOB'S TRACTOR COMPANY Aged Inventory Report bate 9/12/96 Page 5

LYNDEN, WA, a ** REPORT SUMMARY STATISTICS +++ ‘Time 13:37:28 28602

  
  

     

Salection Criteria: Sort-codes1 summary-¥ _New/ts.

 

Pe. AlL-piv. =

 
  
  

AVERAGE AGE | tare cars)

 
 

8 ovER 60 DAYS-NEW ...  an5
8 OVER 60 DAYS-USED .. 66,2

   

‘4 OF CURREWD-YEAR HODELS 2.2.7

  

 

“BND OF REPORT +

   

UNITS


Notes:


---