---
title: "PART: PARTS INVENTORY ADJUSTMENT (X33)"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about PART: PARTS INVENTORY ADJUSTMENT (X33)."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on PART: PARTS INVENTORY ADJUSTMENT (X33)."
---

---

## Page 1

## CHAPTER X33-1

PARTS INVENTORY ADJUSTMENT

### Introduction

Parts Inventory Adjustment allows you to:

= update the on-hand or available quantities to match your physical
count.

= update bin locations.

= update last count date (will be taken from the session date in effect at
the time the part is being counted).

= start with any vendor, part number, or bin location.

Note:

You will want to run X33-2 before this job if you haven't already built
the Parts Inventory Adjustment Report. If you have built the report,
you may proceed with this section. To check if you have the Teport,
[aS a catalog. You're looking for the file name u.1JMd. U = your

 

User Id, d = your division.

Parts Inventory Adjustment allows adjustment of either Available quantity
or On Hand quantity. Please refer to CHAPTER X3-3, PARTS
INVENTORY ADJUSTMENT MENU for more information.

## X33-1 PARTS INVENTORY ADJUSTMENT

 

### How To Run

From the Parts Inventory Adjustment Menu (X3-3), select option 1, Parts
Inventory Adjustment. The adjustment screen is illustrated:

A & R EQUIPMENT PARTS INVENTORY ADJUSTMENT 3310-102

Enter the location of the first part to be adjusted

Bin Location
vendor
Part #..

i-Show quantity available
a-Show quantity on hand (1/2) 1 (

cndi-End job

 

 

 

Type the first bin location, vendor, and part number if you know where
you want to start; otherwise, the first bin and part number in the report
will be displayed.

O) To adjust the available part quantity, press [Enter].

 

 

RELEASE 2.1 L


 

 

 

 

Type 2 to adjust the On hand quantities. Press [Enter]. The Parts
Inventory Adjustment screen appears, as illustrated below.

A & R EQUIPMENT PARTS INVENTORY ADJUSTMENT 3310-103

vendor Part Nutber Description Bin Location available

### Aar Ab33642B Insulator 1-

DIS-3140 This is the first part mumber on che parts exception report.
(mdi-End job, Cmd2-By pass part, Cmd3-Back up, Cmd4-start at new position


 

### Fields & Descriptions

Vendor Manufacturer of the part in this bin location.
Part Number Identifying number of this part.
Description Brief description of the part.
Bin Location Location of the part in your dealership.
Available Quantity now appearing on your records.
Or on Hand Enter the quantity deter mined by the recent

physical inventory count.

Locate the Available or On Hand field to adjust inventory. Type in the
quantity. Press [Field Exit] and then [Enter]. The next part will be
displayed.

Options:

Press [Enter]. The next part number will appear on the screen. Verify or
adjust the available quantity. If the available is correct, press [Enter].
(When you reach the last part number, the procedure will let you
know.)

Cl Press [Cmd1] to end the job.

Press [Cmd2] to by-pass the part. If you did not count the part and
therefore cannot adjust it, the part will appear on the Exception Report.
Press [Cmd3] to back up, so that you can check your adjustments.

Press [Cmd4] to start at a new bin location, vendor, or part number.

 

 

 

 

 

 

 

 

 

 

RELEASE 2.1 LU

## CHAPTER X33-2

PARTS INVENTORY ADJUSTMENT REPORT

### Introduction

Parts Inventory Adjustment Report allows you to:

request the report for inventory adjustment.
specifically select the parts for inventory adjustment, by bin location
or part number sequence.

= exclude parts with blank bin locations
= select manageable amounts of inventory to adjust, for example, bins

 
 

 
 
 

The Part Inventory Adjustment Report is printed by Bin Location or
Part Number -- not as two separate reports.
Da

AG.

perform a blind count or display the on hand or available inventory
quantities

exclude parts with no on hand quantity

select to print the report with single or double spacing.

select to start each bin location on a new page.

  
 

Note:

## X33-2 PARTS INVENTORY ADJUSTMENT REPORT

 

### How To Run

From the Parts Inventory Adjustment Menu (X3-3), select option 2, Parts
Inventory Adjustment Report. If there is already a parts inventory report
and inventory adjustment file for your division, the following message is
displayed:

***CAUTION‘** A Parts inventory Adjustment Report file exists. If you
wish to delete this report file and create a new Parts
Inventory Adjustment Report Enter “Y". If you do not wish
to delete the present report file Enter "N*.

Hither Enter "y" to delete the old report file and create a new
report file or Enter ‘N* to cancel the job and not delete
the report file.

 

If you want to use the report currently on the system, type N (No). The job
is cancelled. Use X33-1 Inventory Adjustment to adjust the quantities to
match your inventory count.

If you want to create a new report, type Y (Yes). The file u.JMd (u = your
User ID and d = your division) will be deleted. You may then request a

new report.

The first portion of the selection screen is displayed below:

RELEASE 2.1 CO


 

Selection Screen 1

LEE'S RENTAL COMPANY PARTS INVENTORY ADJUSTMENT REPORT %3320-201
IN BIN OR PART NUMBER ORDER

Sequence of report (B for bin, P for part) B
N-Print no quantity

1-Print quantity available

2-Print quantity on hand n/1/2) ow

Print double spaced (7m) oN

Number of copies (1-9)

(mdi-End job

 

O When your selections are complete, press [Enter] to go to the full
selection screen. The prompts on the first half are described below.

Sequence of report

Choose the best method for counting your inventory. The key is to keep
the inventory counting manageable. The system has been designed to
allow you to count inventory in sections. The Inventory Adjustment report
is a snapshot of what inventory is at the time the report is created. POS or


 

PPM activity will not change the report.

O To print a report that is in order by Bin Location, select B, or to print it
in order by part number, select P.

Displaying inventory quantities
‘There are three options for displaying quantities on the report.

N - Print no quantity
N - Print no quantity is the default. This is called a blind count. If
the inventory quantity is not included on the report, no estimation
based on quantities can be made by the counter.

1- Print quantity available
Use J if you want to display the "Avail able" quantity. The
available quantity is the quantity available (not reserved) for sale.
If you choose to display the available quantity, it is assumed that
all reserved parts have been pulled from the bins. See X3-3 Parts
Inventory Adjustment.

2- Print quantity on hand
Use 2 to print the On Hand quantity. The quantity on hand is how
many parts are in the dealership. It is not the amount of parts that
are for sale. No reservations are taken into account in the on hand
quantity. If the bin contains all parts whether reserved or not, you
are counting the on hand quantity. After you press [Enter], the
second half of the screen allows you to exclude parts with no on
hand quantity.

Print double spaced
If the report is double spaced, it is easier to read. However, more paper is
used,

0 Type Y (Yes) for double spacing, or N (No) for single spacing.


Number of copies (1-9)
How many counters do you have? You may print a copy for each of them
up to 9 copies. J is the default.

Full Bin Location Selection Screen

PARTS INVENTORY ADJUSTMENT REPORT 3320-201
IN BIN OR PART NUMBER ORDER

Sequence of report | (B for bin, F for part)
N-Print no quantity

i-print quantity available

2-Print quantity on hand n/1/2)

Print double spaced
Number of copies (1-9)
(For All leave From and To entries blank)
Bin Location

From .
To...

Omit Blank Bin Locations? (Y/N) ....
omit Parts with Oshand Qty. = 0 ? (¥/N)

New page after each bin (¥/N)

Bin sort sequence (C - Compress or E - Expand) ¢
Sort Seq: (1) Bin/Vendor/Part# (2) Bin/Part# ; 1

 

From/To
© If your selection is a report in bin order, type in Bin Location to start
FROM and Location TO stop physical count at. Smaller ranges will


 

limit the report to parts you can count in a single session.


Omit Blank Bin Locations? (Y/N)
If you have a lot of parts that have never been assigned a permanent bin
location, you may omit blank bin locations from the report.

Omit Parts with Onhand Qty. = 0? (Y/N)

If you have had a lot of special order parts, you may prefer not to print
parts with no on hand quantity. Omit them by typing Y; otherwise, leave
the default of N (No).

New page after each bin (Y/N)
O Type Y if you prefer to have each bin location start on a separate page.
Type N if you don't need a page break for every bin location.

Bin sort sequence (C - Compress or E - Expand)

Bin locations can be requested in compressed or expanded form. "Com
pressed," which is used most often, means left justified, dictionary order.
"Expanded" means that letters are placed on the left while numbers are
right justified and special characters are treated as blanks. "Expanded"
order makes sense only if your bin locations begin with letters and don't
contain special characters. For example:

Compressed Expanded
1) ABC256 A, 123
2) A123 A___ 1218
3) A4*2B AB__42
A) 12A18 ABC__256

Sort Seq: (1) Bin/Vendor/Part# (2) Bin/Part#

If you have bins where parts have been mixed without regard to vendor,
you will find it more convenient to have parts sorted by Bin and Part
Number. In that case, type 2; otherwise, leave the default of 1 and the
report will be sorted in order by Bin, then Vendor, then Part#.


Full Part Number Selection Screen

(For All leave From and To entries blank)

 

If your selection is a report in part order, type in VENDOR and PART
NUMBER to start from, VENDOR and PART NUMBER to stop at.

The report prints and the inventory adjustment file is built for your
division. Use the report to make a physical count of your parts before
proceeding with X33-1 - Parts Inventory Adjustment.

Below is a sample of the report. Part number order was requested, double
spaced, and no quantity available.
co

LO


ABC COMP:

waynor,

vondor
str

AY
co
code

PARTS INVENTOR

> BY PA

Part Number available Bin Loc

01-2089 7 oat
c1-z065

ba-2187

91-222292

01-2228

01-2334

01-2335,

#4 Bs


yY ADJUSTMENT

RT NUMBER
Description
BELT SET

Res C/T

FILTER

FILTER

caucE

eur

REPORT Date 10/01/86
Time 20.09.52
Last Count Package

32/85

Res 2/0

12785

a2res

12/85

12/85

12785

12785

Page 1
x3320- 3B
mult class

### Fields & Descriptions

Vendor
Code

Part Number
Available

Bin Loc
Description
Res C/t
Res R/o
Last Count

Package
Mult
Class

Deleting the Report

Vendor code for the part.

Quick code or Honda code.

Part identifying number.

On-hand minus the reservations from Point
of Sale.

You have the option to have this print or not.
If you chose not to have it print, asterisks
appear.

Bin location of the part.

Brief description of the part.

Amount of reservations on counter tickets.
Amount of reservations on repair orders.
Date of the last physical inventory. The
contents of this fields are taken from the
session date in effect during the last Parts
Inventory Adjustment (X33-1).

Amount in packaged quantity.

Amount in bulk, i.e. 55 for 55 gallons of oil.
Class code for the part.

When you no longer need the file, you can delete it:

O Ata menu, type: DELETE u.IJMd,F1 [Enter].
(u=the 1-character ID associated with your company files and

d=your division)

io

## CHAPTER X33-3

PARTS INVENTORY EXCEPTION REPORT

### Introduction

Parts Inventory Exception Report allows you to list the parts you missed in
taking inventory. These are parts with a bin location or on-hand quantity
that were skipped on the inventory adjustment screen.

### How To Run

The following screen is displayed:
PARTS INVENTORY EXCEPTION REPORT %3330-101,

05/96 is the most recent date for the "Last Count Date’ to
be included on the Parts Inventory Exception Report
Date Range Selection

From (MM/¥Y): 0596
To (M/Y¥Y): 0596

N-Print no quantity
1-print quantity available
2-Print quantity on hand (N/1/2)


[| X33-3 PARTS INVENTORY EXCEPTION REPORT

Last Count date

The Last Count date is used to determine what is on the Parts Inventory
Exception report. Last Count Date is a field displayed on the Part
Information screen at PPM (X3-2) and Parts Inquiry (X3-1). The Last
Count Date field on the Parts Information screen is updated from the
session date during Parts Inventory Adjustment (X33-1). The computer
looks at the Last Count Date field on the Part Information screen for
each part on the Parts Inventory Adjustment report.

If the Last Count Date on the Part Information screen does not fall
within the range of dates you enter on this screen, the part will display
on the Exception Report.

The current month and year display. If you did X33-1, Parts Inventory (
Adjustment in a prior month, change the Last Count date.

Displaying inventory quantities

There are three options for displaying quantities on the report.
N-Print no quantity
N - Print no quantity is the default. This is called a blind count. If the
inventory quantity is not included on the report, no estimation based on
quantities can be made by the counter.

1 - Print quantity available

Use J if you want to display the "Available" quantity. The available
quantity is the quantity available (not reserved) for sale. If you choose
to display the available quantity, it is assumed that all reserved parts
have been pulled from the bins. See X3-3 Parts Inventory Adjustment.

RELEASE 2.1 LL


X33-3 PARTS INVENTORY EXCEPTION REPORT [=]

2 - Print quantity on hand

Use 2 to print the On Hand quantity. The quantity on hand is how many
parts are in the dealership. It is not the amount of parts that are for sale.
No reservations are taken into account in the on hand quantity. If the
bin contains all parts whether reserved or not, you are counting the on
hand quantity.

When the screen is complete, press Enter.

### Inventory Adjustment Report

The Inventory Adjustment Report will print listing all parts by-passed or
not brought up during Parts Inventory Adjustment. You should check to
see if the parts on this report were missed in the physical inventory, or are
obsolete parts and should be deleted from parts inventory files.

PARTS INVENTORY EXCEPTION REPORT Date 20/01/86 Page 1
R BY PART NUMBER Time 11.01.25 xaz2e- 36
Coda Part Number Available Bin Loc Description Res C/T Res R/O Last Count Package Mult Class.
91-2059 7.8 Ha pee BELT SEP
01-2065 ‘HAAG prutee 12/85
01-2287 ‘ox1a  Frurae 1278s
01-222772 + RIES  caucE azsas
01-2228 son ac? BELT 12/85
01-2334 ‘ute | purer 12785

01-2335, ‘Ric | FruTER 12785
01-2336 3B FILTER 12785
01-2305, : * 83 EB swrTcH 12/65

 


[+] X33-3 PARTS INVENTORY EXCEPTION REPORT

### Fields & Descriptions

Vendor Manufacturer of the part.
Code Quick code or Honda code.
Part Number Identifying number of the part.
Available Quantity from last physical count.
or On Hand
Bin Loc Bin location of the part.
Description Description of the part.
Res C/T Amount of reservations on Counter Tickets.
Res R/O Amount of reservations on Repair Orders.
Last Count Date of the last count on each part.
Package Number of part per package.
Mult If the part comes in unit (55 gallons of oil). (
Class Class of the part.


X33-3 PARTS INVENTORY EXCEPTION REPORT [=]

### What Happens Next

Determine the count on any parts on the Exception Report.
Enter the count for each part using Parts Inventory Adjustment (X33-1).

Print the Parts Inventory Exception report again. Make sure there are no
parts on the report.

When all the inventory has been adjusted, delete the u.IJMd and u.IFZd
files (u = your User ID and d = your division).

At any menu type:

DELETE u.JJMd,F1 [Enter]
then:

DELETE u.IFZD,F1 [Enter}


Notes:


RELEASE 2.1 Ne

## CHAPTER X33-4

PARTS INVENTORY FREEZE

### Introduction

Use Parts Inventory Freeze to take a snapshot of your parts inventory files
prior to a major change, such as Inventory Adjustment or a Price Tape
Update. Following the change, select Parts Inventory Variation Report
(X33-5) to print a list of changes to on hand or available quantities and
cost.

### Warning!

No parts or point of sale jobs can be running when this job is
tequested.


[2] X33-4 PARTS INVENTORY FREEZE co

### How To Run

If a work file (the snapshot), is already on your disk, the following
message is displayed:

WARNING: A work file has already heen created
for this division on

03/10/92 11:06

1 you wish to delete this file to build a new
one type “¥" in the following field:

¥

 

If there is no Parts Inventory Freeze file, the job is placed directly on the
Job queue. When the file (u.IFZd) has been created, the system beeps and
issues the following message: "A Parts Inventory Freeze for division <d>
has completed on 03/10/92 11:06" where <d> is your division.

When you no longer need the freeze file, you can delete it:
O Ata menu, type: DELETE u.IFZd,F1 [Enter].

(u=the I-character ID associated with your company files and d=your
division code)

 

(
RELEASE 2.1 SN

## CHAPTER X33-5

PARTS INVENTORY VARIATION REPORT

### Introduction

Select Parts Inventory Variation Report to print a list of the differences
(variations) between the work file created by Parts Inventory Freeze
(X33-4) and your current parts inventory files.

### How To Run

A&R SALES & LEASING PARTS INVENTORY VARIATION REPORT %33501-01
Division: a

Vendor {Or ALL)

Class (Or ALL)

Available Quantity(1) or On Nand Quantity(2)..:

Print Variations Only? (¥/N)

Rurber Of Copies (1-9)

## X33-5 PARTS INVENTORY VARIATION REPORT

 

O To print Available Quantity, type: J. To print On Hand Quantity, type:
2.

O To print only the part lines that have changed, type Y at the prompt,
"Print Variations Only? (Y/N).”

Below is an example of an Inventory Variation Report that was limited to
variations only.

A & R EQUIPMENT SKLES Parts Inventory Variation Report pate 4/24/52 Page 1
Division: b Vendor: BBB Class: ALL Freeze Date: 6/22/52 9:45 ‘Time 14.30.20 23390-301

eases Inventory Freeze = Current Inventory ==== === variation
Pare F Description aw cost. Total = ay cost. Total Av Total
vi20448 GASKET a 2.86 2.56 2.74 8.22 2 5.66
00246 ROLLER 2.75 30.25 2.75 22.00 Be B.25- (

103244 IDLER SPROCKET 5.95 77.38, . 54.36 a 22.99-
aitod SPRING 32 3.52 . 2.48 296
121602 BEARING 14.63 146.30 : 231.67 14.63-

Class Totals: 259.98 220.73 39.25-
Vender Totals: 259.98 220.73 39.25-
Grand Totals: 259.98 220.73 39.28-

 

RELEASE 2.1 LU

## CHAPTER X34-2

RECEIVE ORDER MENU

### Introduction

Receive Order Menu allows you to correct before receiving system
generated stock orders, manual set up stock orders and priority orders
generated and accepted in Point of Sale. Once the orders have been
corrected, the orders can be received. When the order is received,
inventory is updated.

The Receive Order Menu includes the following jobs:

X342-1

X342-2

X342-3

X342-4

Correct Order Before Receiving

Sometimes when parts orders arrive at the dealership, there
are discrepancies between what was ordered and what was
shipped. If the inventory was received as ordered, the count
would be off. The orders must be corrected before they are
teceipted.

Receive Order

After all corrections have been made to the order, the order
is received to update on hand inventory. If the order is
received before corrections are made, corrections to
inventory will be made through Parts Posting and
Maintenance (X3-2).

Inquire/Update Reservation Priorities
Use this job to review or change the order in which
reservations will be filled.

Unclaimed Part Receipts Report

Print the Unclaimed Part Receipts Report to see a list of
parts that have been reserved, ordered, and received, but not
yet claimed: parts on open Point of Sale documents where
the priority code has changed to "a".


Notes:

## CHAPTER X34-3

CANCEL ORDER

### Introduction

Cancel Order allows you to:

- cancel an order that has previously been created either as a
- suggested order,
- final order,
- manual order,
- priority order, or
- special merchandising order.

DO NOT CANCEL AN ORDER WHICH IS BEING CREATED.
Check the user board to be sure that all X341___ procedures have
finished.

## X34-3 CANCEL ORDER

 

 

CANCELING ORDERS
From Menu Name: Type in: Press:
Cancel Order Vendor Code
Order Number ENTER
Note:
You may end the job at any time if Cmd1 is listed at the bottom of the
screen. This does not cancel the order; it returns you to the entrance
screen where you may enter another order number.
Da ns
(

RESULT: If you press ENTER, the order will be cancelled. Order
information for all parts on the order will be deleted for the cancelled
order. Type another order to be cancelled and repeat the process, or press
Cmd1 to cancel the job and return to the Stock Order Menu.

RELEASE 2.1 CO

## CHAPTER X34-4

ORDER INQUIRY

### Introduction

Order Inquiry allows you to:
" Look at any of the following as long as they are current:
— stock orders.
— priority orders.
- special merchandising orders.
— return orders and stock phase-outs.
= Look at part detail information for each order.
= Determine whether the orders are suggested or final orders.
= View responses from Case.

Note: Orders, returns, etc. remain current until they are fully receipted, posted, or

 

 

 
 

 

canceled.
CONTENTS
ENTRANCE SCREEN... aa 2
How to use this screen. wed
OPTIONS. ...cseresscsssossnsnccnacsnecentenssesacersesnsatavensnnesssserensnreresseananerenenereeseanarones 3
5=Display .. 3
R=Response... 4
P=PSO Inquiry . 5
HISTORY SCREEN.. ae 7

 

FIELDS ON THE ORDER INQUIRY SCREEN........ svserasensanenepessesenvenss: sree 8


2 X34-4 « ORDER INQUIRY RELEASE 2.3

 

### Entrance Screen (

From the Parts Inventory Menu (X3), select option 4, Stock Order Menu.
Select option 4, Order Inquiry. The Current Order Headers screen is displayed.

L&E EQUIPMENT SALES ORDER INQUIRY 34401
Division : T Current Order Headers

Order #

5=Display R=Response P=PSO Inquiry

 

Opt Order # Ven Src Order Date Type Status Lines Amount Suppl Ord#
R5809 0 CHE 11/19/98 Prty = Final 1 52.
RS813 ROS 11/30/88 Prty Final 2 136.
R5820 CAS 12/04/98 Prty Final 2 1607.
R5821 0 I/R 12/05/98 Prty Final 1849.
R5822 CHP 12/05/98 Prty Final 5055.
R5823 «ROS 12/07/98 Prty Final 108.
5M120398 CAS 12/02/98 Stock Final 9485. 6879696
80010216 Cas 2/16/99 Stock 5236.
0011023 10/23/98 Stock
S0061698 CAS 6/12/98 Stock 313. 6225822
80112498 11/23/98 1024. 6859041
80120898 12/07/98

Use these wieexit | . ;

. =Exi = = P S
function keys Order By: Fl4=Vendor = F15=Source suppiy Fl6=Type F17=Status
to change the F18=Supp1 ora# (
order of the
items on the
screen.

How to use this screen
To display the details of an item, select it with 5=Display.
To look at Case responses, select an item with R=Response.

= To do an Inquiry for the PSO #, select an item with P=PSO Inquiry. See page
5

= To see the next page, press [Page Down].
= To toggle to historical data (orders that have been fully posted), press
F20=Historical ([Shift]+{F8]).

Sorting the data in a different order

By default, the items are in order by Order #, and there is an order number
prompt, which allows you to locate the order you are looking for. The 2 lines at
the bottom of the screen indicate the different ways the data on the screen can be
sorted (put in order by). Simply press one of the command keys and the data will
be sorted in the corresponding order.


PARTS X34-4 e ORDER INQUIRY 3

### Options

5=Display
To display an item, select it with 5=Display.

AGR EQUIPMENT SALES ORDER INQUIRY 34402
Division : A Detail
Order #: R120898
Part Number Vendor : CAS
Source :

Part Number i Order Order Action
Cost Flag Code

A10094

A11190

11208

Bottom

F3=Exit F12=Previous PgUp/PgDn

 

To locate a particular part to see if it has been received or if it’s on backorder,
type the part number at the Part Number locator prompt, and press [Enter]. The
display will show the nearest match at the top of the list.

To return to the Entrance screen, press F12=Previous.

To return to the Stock Order Menu, press F3=Exit.

Fields on the detail screen

Order # Order number.

Vendor 3-character vendor code.

Source Source of supply vendor.

Part Number Part being ordered.

Quick Code Honda code.

Qty Order Number of parts ordered.

Qty Recvd Number of parts already received from order.

Order Cost Extended price (quantity orders * price).

Order Flag Back order indicator.

Action Code What action can be taken if ordered item could not be
eo] Valid action codes are:

   

[S| Substitution

iB Backorder

Cancel


4 X34-4 « ORDER INQUIRY

R=Response
To view a response from Case, select a Case item with R=Response.

A&R EQUIPMENT SALES
Division : A

CASE Response
Seq# : 00005

User-Id 0006
Main Dirt 22385800
Ordering Dlr# : 22385800

Seq# : 00006

User-Id : AO0G6
Main Dir# 22385800
Ordering Dir# : 22385800

PART DESCRIPTION
Al0094 BEARING B
A11190 TACHOMETER
411208 GASKET

ORDER INQUIRY 34403

View CASE Responses

Order +: R120898
Return Header
Dir Return#

Return Type
Pso#

: R120898
3-Monthly Re
: 6824283

 

Body

Dir order# 2 R120898
Return Type 3-Monthly Re
PSO# + 6824283

MESSAGE

INV- PART AND QUANTI
INVALID PART QUANTIT
INVALID PART QUANTIT

F3sExit Fl2=Previous F21=Print PgUp/PgDn

 

To print the response, press F21=Print.
To return to the Entrance screen, press F12=Previous.
To return to the Stock Order Menu, press F3=Exit.


PARTS X34-4 « ORDER INQUIRY


 

P=PSO Inquiry

From the Current Order Headers screen, select an item with P=PSO Inquiry.
A PSO Number prompt appears, as illustrated below:

L&E EQUIPMENT SALES CASE COMMUNICATIONS CASLOOPZQ0
Division : T PSO Order Inquiry

PSO Number
6879696

F3sExit FS=Header F6=Shipping F7=Paxt detail

To see the Headers screen, press F5=Header or press [Enter] to start the inquiry

 

with Case. Or, you can press F6=Shipping or F7=Part detail to go directly to those

screens instead.


6 X34-4 « ORDER INQUIRY

L&E EQUIPMENT SALES CASE COMMUNICATIONS
Division : T PSO Order Inquiry - Header

Pso. teeeeeee et 6875175 Sequence

Depot ID......... ceed Servicing
Ordered Through Dealer Syste: Depot
Indicators
. Customer Number....; 22385800
Order Cycle... wad
Customer Order No.
Customer Order Date:

Texms Code........... at Lines On PSO.
Order Type... : . Back Order Qty

Scheduled Ship Date..
Print Date.
CAS1OOPIQO

RSKLADPCMRTERISS //
ATCETLHOPEODGEDD //
CPYALSLLSGRMCWUC //

F3sExit FésShipping F7=Part detail F9=Print F12=Previous


X34-4 e ORDER INQUIRY 7

 

HISTORY SCREEN

‘When you press F20=Historical from the Current Order Headers screen, a list of
historical items is displayed. These items have been fully receipted or posted.

A&R EQUIPMENT SALES

ORDER INQUIRY

Division : A Historical Order Headers

Order #

S=Display R=Response P=PSO Inquiry
Type Status Lines

Opt Order # Ven Src Order Date
CASi202C CAS 12/02/98
c1207B cas 12/07/98
12084 = CAS. 12/08/98
JAMES2 CAS 6/22/98

F3=Exit F12=Previous

Order By: Fld=Vendor
F18=Suppl Ord#

Return Pinal
Prty Final
Prty Final
Return Final

F20=Current
F15=Source supply


 

34401

Suppl ord?
12345

oooss24ze1
0006824286

 

Bottom
PgUp/PgDn

Pl6é=Type Fi7=Status


8 X34-4 e ORDER INQUIRY

FIELDS ON THE ORDER INQUIRY SCREEN

Opt

Order #
Ven

Src

Order Date
Type

Status
Lines
Amount
Suppl Ord#

For selection, such as 5=Display.
Order number.

3-character vendor code.

Source of supply vendor.

Date that order was created.
Order Type. Valid order t

 

Rtn

 

 

  

StkOrd Stock Order

 

 

 

 

 

 

Emrg Emergency
Merch Merchandise
Order status (Final).

Number of lines in the order.
Total cost of item lines on the order.
Supplier’s order number.

## CHAPTER X34-4

ORDER INQUIRY

### Introduction

Order Inquiry allows you to:
= look at any order currently on the system, including:
- stock orders.
- priority orders.
- special merchandising orders.
- return orders and stock phase-outs.
= look at part detail information for each order.
= determine whether the orders are suggested or final orders.

The orders remain in the system until they are fully receipted or
deleted.

## X34-4 ORDER INQUIRY

### Running Stock Order Inquiry

After selecting the option to run Stock Order Inquiry, you will see the
screen as shown in Figure X3440-101. All the orders currently on the
system for your division will appear on the screen. Press Enter to scroll to

the next page.

‘ABC COMPANY
Division: E

order # Ven src Ord Date
80010830 wWDs 9/12/94
0010909 BEG 9709/94
0020911 8709/94
POSE 9/15/94
RAL2674 asiis94

Display detail: Order 4

ORDER INQUIRY

HEADER

Type = Status Lines

Stock
Stock Final
Stock Final
Prty Final
Return

endl -End Job Cmd16-Display order History

é
4

Amount
1621.32
377.84
952.96
117.36

3440-101

Suppl ordi

 
\

### Order History Screen

The order history screen displays information about orders that have been
finalized and received. Until an order is received, it will not appear on the
Order History Screen. Order History can be deleted with Parts End of
Month (X3-10). A sample screen is shown below.

To print a report of the selected order, put a "Y"in the “Print Y/N" field at
the top of the screen and press [Enter]. A report will be generated and sent
to the system printer.

ABC-AG,AUTO,CONS & TRUCK CO. ORDER INQUIRY 3440-103 3
Division : A BISTORY Print (Y/N):

Pare Part Rept Order Qty Oty OnHand = Receipt A
Number Dese Date Date Rev'd Ord Before cost C
Alaa BELT 10/17/94 05/01/86 2 2 6.99
12062 BUSHING 10/17/94 05/01/86 3 11.16
A2075 SEAL RING 10/17/94 05/01/86 62
16202 ORING 20/17/94 05/01/86 46
34543 BREATHER 10/17/94 05/01/86 -00
40035 BEARING 10/17/94 05/01/86 03
492082R91 BEARING 10/17/94 05/01/86 6.16
492853R91 SET 10/17/94 08/01/86 50
49385 O RING = 10/17/94 05/01/86 as
49S425R1 GEAR 10/17/94 05/01/86 68
495619R95 prise 20/17/94 05/01/86 -01
72773 GASKET — 10/17/94 05/01/86 we
760s SPRING 10/17/94 05/01/86

ga SPRING 10/17/84 05/01/86 38

Display History: order # $0010501 Vendor cas

Cmdi-End job © Cmd2-Return to Header screen

 

The column on the far right of the Order History Screen , A C, is referred


[| X34-4 ORDER INQUIRY C .

to as Action Code, There are three valid Action Codes:
Action Codes

B = Back Order. If the part is on back order with the vendor, type B. When
the order is received (X342-2), all parts with a B Action Code will be back
ordered. View all parts on back order by requesting a Back Order Parts
Report (X34-5). Back Order parts will not show on the report until the
order is received (X342-2).

C = Cancel. If you will not be receiving the part, cancel it off the order. To
cancel the part, type C in the Action Code field. When the order is
received, the part will be deleted from the order.

S = Supersession. If you order four parts, receive three of the ordered part
and one of a part superseding the ordered part, type a S in the Action Code
field.

LC


X34-4 ORDER INQUIRY [=]

### Fields & Descriptions

Order # Order identifying number.
Ven Vendor code of the manufacturer order is
for.
SRC Vendor code of source of supply.
Ord Date Date of the order.
Type Order type: Prty for Priority
Merch for Merchandising
Stock for Stock Order
Retn for Return
Status Final if final order; blank if suggested order;
or manual order not printed.
Lines Number of lines in the order.
Amount Cost to dealership for the order.
Vendor Ref Number of the part stock order supplied by
manufacturer via Communications.
OPTIONS

1. To review the detail! lines on the order, enter the order number and
vendor code in the spaces provided at the bottom of the screen. Press
ENTER. The detail lines will appear. Press ENTER to page through.
See Figure X3440-102 for an example of the screen.

A part number/Quick code can be typed in at the bottom of the screen

to begin the next page. If the lines fill more than one page, the last part
on the page appears in that field. It is also the first part on the next
page.

 


‘2AEC COMPANY ORDER INQUIRY 3440-102
Division: Er DETAIL

Order # $0010911 Vendor BHG Source

Part Number Quick Code  gty Quick Code Qty
spoo8

SPOLO

SPOSO

SPi05

SP172

SP188

Next page begins with part number

cmd2-Return to Header Screen Cmdl6-Display Order History

 

OPTIONS:

1. Press ENTER to scroll] through the Order Inquiry.
2. Press CMD 1 to end the job.

3. Press CMD 2 to return to the Order Inquiry Header.
4. Press CMD 16 to see the Order History Screen.

RELEASE 2.1 WL

## CHAPTER X34-5

BACK ORDER PARTS REPORT

### Introduction

Back Order Parts allows you to:
= request a report after a receipt of the stock order to show by single
vendor or all vendors the back orders.
= view the information on the report, which includes:
- order number,
- part number,
- quantity on back order,
- order type,
- unit cost,
- extended cost (number of parts X cost of part),
~ back order totals, including:
number of lines on the back order,
number of parts, and
total dollar amount.

### How To Run

 

 

 

From the Stock Order Menu, select option 5, Back Order Parts Report.
D At the selection screen:

 

Type in: Press:
Vendor Code or
ALL (all vendors) ENTER

You will receive a printout listing parts still on back order.

## X34-5 BACK ORDER PARTS REPORT

 

ABC COMPARY BACK ORDER PARTS REPORT 10/01/86 PAGE i.
waeNer, Co " MP + MASSEY-FERGUSCN 3450-208

ORDER # PART NUMBER QUANTITY ORDER TYPE STATUS. UNIT COST
0407860N ozs 8420, 3 stock B 3.13
o4o7960n 022 327% 2 06
oe07860N 021 726m

BACK ORDER TOTALS FOR MASSEY- FERGUSCN

OF LINES.

4 OF PARTS

 

FIELDS & DESCRIPTIONS (

Order # Order identifying number.

Part Number Identifying part numbers on the back order.

Quantity Number of the part on back order.

Order Type Kind of order: stock order or priority order.

Status Action code entered at Correct Order Before
Receiving (X3412-201). C for cancel the
order line from the order after receipting the
quantity entered or dealer-defined
informational field. Only C affects the order
line.

Unit Cost Cost of the part to the dealership.

Extended Cost Unit cost times the number of the part
ordered.

Back Order Totals Totals for the back order by vendor.

## of Lines Number of part lines on the back order.

!

RELEASE 2.1 Ne


 

## of Parts Number of parts on the back order.

Dollars Total dollar amount of the back order.
If you have a back order report for more than one vendor, the TOTALS for

the report reflect the TOTAL # of LINES and PARTS, and give the total
DOLLARS involved in the back order.


Notes:

RELEASE 2.1 LL

## CHAPTER X34-6

MOVE ORDER LINES

### Introduction

Move Order Lines allows you to:

™ move one, some or all order lines from one open order to another open
order.

™ move one, some or all order lines from one final order to another final
order.

= move order lines on:
~ stock orders (lines from a stock order may only be moved to other
stock orders)
- priority orders
- special merchandising orders.
- stock returns

When a part is not available at Point of Sale, the system assigns a priority
code = "P", assuring that you want to place it on a priority order. To place
it on a stock order instead, assign a priority code = "S". Likewise, in
Priority Orders (X5-3) you may change the priority code from "P" to "S".
The parts will be placed on a stock order, number POSd (d = division
code). This POSd order should never be finalized. To consolidate the Point
of Sale stock order with a larger open order, use Move Order Lines.

 
 

Note:

Lines can be moved only if both orders are open or both orders are

final. They cannot be moved if one order is open and the other is final.

   

  

      

 

### How To Run

See the Introduction for more on the Master Menu and Security Gates.


X34-6 MOVE ORDER LINES C .

 

From Menu Name: Move Order Lines

Type in: Press:
Vendor Code

Order Number

(or Return Number)

you want to move. ENTER

Note:

If you need to refer to the order numbers, check Order Inquiry X344.
Both orders must be open.

 

See Figure X3460-101 for an example of the Move Order Lines Screen.

RELEASE 2.1 CO

## X34-6 MOVE ORDER LINES

ABC COMPANY 3460-102
Division : A

Vendor: wD$
Order Number you want to move parts from: 0010912

The order you are moving to will be entered on the next screen.

cmdl-Ené job

The next screen is for identifying which order you want the order lines
moved to. See Figure X3460-201.


 

ABC COMPANY MOVE ORDER LINES 2460-201
Division: £ wDs 0010912

Move to order number: 0020830


14 (
15

Press Cmdl to end job

 

### Fields & Descriptions

Move to Order Number Order number you want the part(s) to
move to.

Part Number Identifying part numbers on the
order.

Quantity Number of the part on order.

Enter M to Move Type an M after the part(s) you want
to move another order.

Press ENTER.

RELEASE 2.1 LL


 

RESULT: The screen returns with the changes to the order. They are
moved to the order you specified.

### Options

O Move additional lines or change the order to move additional lines
to.

Press CMD 1 to end the job.


Notes:

RELEASE 2.1 Lo

## CHAPTER X34-7

PRINT ORDER LINES

### Introduction

Print Order Lines produces a list of parts that are currently on order and
the number of days they have been on order. It can be requested for all
vendors, all classes or restricted to a single vendor/class. The report can
list parts on all orders or it can be requested for priority orders only or
stock orders only.


X34-7 PRINT ORDER LINES _

 

### How To Run

From the Stock Order Menu (X3-4), select option 7, Print Order Lines.
Following the Parts security gate, the following selection screen is
displayed:

A & R SALES & LEASING PRINT ORDER LINES x34701-01
Division: A
Vendor (Or ALL)

Class (Or ALL)

Priority(P), Stock(S), (or ALL): ALL

 

O To print all parts on order, simply press [Enter] or change the defaults
as indicated below:
O) To request the report for one vendor, type the 3-character vendor code.
To request a single class, type the 1-character class code.
To request a list of parts on priority orders only, type P and press [Field
Exit].
To request a list of parts on stock orders only, type S and press
[Field Exit].

 

 

 

 

 

 

 

 

 

 

 

t
RELEASE 2.1 SN

## X34-7 PRINT ORDER LINES

 

A Print Order Lines report is illustrated below.

AG R SALES & LEASING Print Order Lines Pate §/04/32 Page 1
Division: a Vendor: ALL Class: ALL Order Type: ALL Bine 9.31.14 3470-301,
Totals
ven Part & Description type Date # Days Order # Steck total
AS ag4032R2 SPACER P syoiss2 3 0502920a, 12
48403382 RING sro1s92 95015208, 1
484038R2, WASHER sros92 osois20a, a
apaaeiR2 SPRING 5/01/82 POSA, a0
4es2s9n01 BEARING sro1rs2 POsa
490a75R3 BLADE 4730/52 50010430
49270983 4/30/92 50010430
492757R9L 4/30/82 50020430
49549283, 4730/32 30020430
495475R3 4/30/92 50010630

A & R SALES & LEASING Print Order Lines Dace $/04/92 2

Bivision: A Vendor: ALL Class: ALL Order Type: ALL. Time 9.31.14 3470-301
Order information sesssesse2==2ee: eneeeoa= Totals

Ven Part t Description cls Type Date 4 Days Order F Oty Pty Stock =Total

FOR BONNIO505A asH AS 4/30/92 4 0430920a 2 1 a

FOR BINN3537A BRG 4730/92 0430920a X x z

FOR CAPNS200A, xr 4130/92 0430920a 10 10

FOR CEPNII79q, xr 4/30/92 04309208 2 2

FOR CDPNSSOLA, PUMP 4730/92 0430920a 2 2

FOR CFPNGOOSB RIT 4030/92 92309208, 1 1 =

FOR CzN67213 FILTR 4430/92 0430920, 12 2

 

  


Notes:

RELEASE 2.1 oe

## CHAPTER X34-8

CORPORATE STOCK ORDER

### Introduction

Corporate Stock Order creates a multi-divisional stock order using one of
two methods. Method 1 combines separate stock orders created through
Create Suggested Stock Order (X34-1) or Create Manual Order (X34-2).
Method 2 combines quantities and histories from selected divisions and
generates a corporate order from the results. If you use method 2, an
option also exists to create a suggested stock transfer. Once a corporate
stock order is received, the user can freely distribute the parts included in
it among the divisions used in generating the order.

When a corporate order for Case is finalized, an Order Information screen
captures the necessary information before it is transmitted directly to the
Case host computer.

### How To Run

From the Stock Order Menu (X3-4), select option 8, Corporate Stock
Order. Enter your division and password at the security gate and press
{Enter]. The following screen appears.


[2] X34-8 CORPORATE STOCK ORDER Co

ABC-AG,AUTO,CONS & TRUCK CO CORPORATE STOCK ORDERS 3480-001 1
Division A Review Orders

(Opt: 1=Method #1 2="ethod #2 3=Review d=Delete S=Finalize 6=Print 7=Cor/Rev)

Opt. Corp Ord# Ord Date Order Method Status PSO #

(mdi-End job Roll-Page Home-Top of list

 

Each line on this screen represents a corporate stock order. Individual
orders can be created, reviewed, deleted, finalized, printed, or received.

O To perform one of these actions, type the appropriate number next to an
order and press [Enter]. Refer to the sections below for details on

creating, finalizing, and receiving a corporate stock order.

### Fields And Definitions

Corp. Order# 8 characters.

Order Date 6 digits.

Order Method "1" for method 1; "2" for method 2.
Status Either “Open” or "Finalized."

{
RELEASE 2.3 Ne


X34-8 CORPORATE STOCK ORDER [2]

PSO# 7 digits.

### Creating A Corporate Stock Order—Method 1

This is the general procedure used by Method | for creating a Corporate
Stock Order:

= The user selects individual stock orders created through Create
Suggested Stock Order (X34-1) or Create Manual Order (X34-2).
Selected stock orders have to be finalized.

a The individual stock orders are combined and used to generate a
single corporate stock order

= The user reviews and then finalizes the corporate stock order.
Once the corporate stock order is finalized, all the stock orders
included in it become finalized as well. The computer then
determines how the parts in the corporate stock order are
distributed to each division used to generate the order. If
necessary, the user modifies the parts distribution list of the order
and receives the order. Each division's parts inventory is changed
accordingly.

### How To Use Method 1

O From the Review Orders screen, enter a "1" in the field on the top-left.
In the field next to it, enter the Order Number of the new corporate
order. Press [Enter] The following screen appears.


[+] X34-8 CORPORATE STOCK ORDER C :

ABC-AG, AUTO, CONS & TRUCK CO CORPORATE STOCK ORDERS %3481-001 3
Division A Select Orders Method 1
ORDER # CRPORD1

(Options: 1=Select)
Vendor Order Date Division
cas 12/09/97 A

cAS 12/09/97
YAM 12/09/97 M

Cmd3-Return Roll-Page Home-Top of list

 

O Each entry on this list represents a stock order made through
Create Suggested Stock Order (X341-1) or Create Manual Order
(X341-2). Select all the stock orders you want to include in the
corporate stock order by placing a "1" in the opt field. Press
[Enter] when finished. Ali of the "1"'s you entered will disappear,
but otherwise the screen will appear the same. Press [Cmd3] to
return to the Review Orders screen.

O The order may now be reviewed, deleted, or received. Refer to the
sections below for more information on performing these tasks.

{
RELEASE23 9 ~~


X34-8 CORPORATE STOCK ORDER [=|

### Creating A Corporate Stock Order—Method 2

This is the general procedure that Method 2 uses in creating a Corporate
Stock Order.

= The user responds to a list of prompts about the corporate order,
specifying information such as vendor, class, and order number.
The user also has the option of creating a suggested stock transfer.
If this option is taken, this job will make a suggested stock transfer
and, in making the corporate order, assume that the stock transfer
has already taken place.
The user selects which divisions the corporate order will include.
The computer creates stock orders for each selected division.
These are combined and used to generate a corporate stock order.

= The order is reviewed and then finalized. Based on inventory and
sales history, the computer determines how many parts from the
corporate stock order are distributed to each division included in
the Stock Order. If necessary, the user modifies the order's
divisional distribution and then receives it. Each division's parts
inventory is changed accordingly.

= If the user opted to create a suggested stock transfer, the transfer is
then posted. See Suggested Stock Transfer (X34-9) for more
information.

= The user optionally assigns a time to generate the order.

### How To Use Method 2

O From the Review Orders screen, enter a "2" in the field on the top-left.
In the field next to it, enter the Order Number of the new corporate
order. Press [Enter] The following screen appears. The prompts are

## X34-8 CORPORATE STOCK ORDER

described below.

ABC-AG, AUTO, CONS & TRUCK CO. Create Corporate Order x3482-001 1
Division: A

From the given information a corporate stock order will be printed:

Class(es) or ALL ALL
Order Start Date 120997

Days Supply (1 to 365) . 120
Order Number 80152200
Create/Print Suggested Stock Transfer (¥/N) . N

Enter character to select by part category

Use available/on order quantities to calculate order (¥/N)

(Qmd-2 Select Divisions for Corporate Order cmd3-Return

 

Vendor Code 3 characters. Enter the vendor that will
receive the Corporate Stock Order.

Class(es) or ALL 3 characters. To request an order for more
than one class, but not all classes, type 1
class code on the first line and up to 13 more
on the next line.

Order Start Date 6 digits. Type in the beginning date of your
stocking period. A future start date will
change the sales history period the system

f
RELEASE 2.3 Ne


Days Supply

Order Number

Create Suggested Transfer

Enter character to select
by part category

Use available/on order
quantities to calculate
report.


 

considers when selecting parts for the order.

3 digits with a maximum value of 365. This
is the number of days supply this order will
cover.

8 characters. You may change it to an order
name or number of up to 8 characters. Order
number defaults to SOOLMMDD (MM is 2
digits for the month, DD is 2 digits for the
day).

If "Y," the corporate stock order will be
generated as if the suggested transfer has
already occurred. Post the transfer with
Suggested Stock Transfer (X34-9). See that
chapter for more information.

1 character. This prompt refers to the part
category field on the Parts Posting &
Maintenance screen. It is furnished by some
price tapes; otherwise, it is user-defined. If
you don't want to select a particular class
category, leave this prompt blank.

Enter a "Y" in this field.

O After you have completed specifying this information, press [Cmd2] to
select the divisions that will be included in the order. The following


 

screen appears.

ABC-AG, AUTO,CONS & TRUCK CO, Create Corporate Order x3411-102
Select. Divisions

A Corporate Stock Order will be created from the divisions
you select. The combined stock order will use demand
criteria from and will be shipped to Division aA

ABC-AG, AUTO, CONS & TRUCK CO.
DEALER SALES & SERVICE, LTD.
ABC COMPANY

ABC COMPANY

MOTORCYCLE CITY

### ‘Thermoking

Emd1-End Job Cmd2-Continue cma-12 Select All Divisions

 

O Select the divisions that will be included in the report by placing a
character next to them. Select all divisions by pressing [Cmd12]. Press
[Cmd2] when you are finished. The Create Corporate Order (Method
2) screen appears. Press [Cmd3] to return to the Review Orders screen.
As it may take some time for the new order to be generated, it will not
immediately be displayed on the screen. Quit this job and restart it
again to view the new entry.

RELEASE 2.3 LU

### Review Corporate Order

Select the order you want to review in the Review Corporate Order screen
(the entrance screen for this job), put a "3" next to it and press [Enter].
The following screen appears.

ABC-AG,AUTO,CONS & TRUCK CO CORPORATE STOCK ORDERS x3481-301 1
Division & Review Corp Order
ORDER # CRPORDL

(options: 3=Review 4=Remove)
Vendor Order Date Division
ORDE301 cas 12/09/97 A

ORDE302 cas 12/09/97 B
ORDE303 YAM 12/09/97 M

(md3-Return Roll-Page Home-Top of list

 

These are the individual stock orders that comprise the corporate stock
order you selected in the previous screen. To review an individual order
place a "3" next to it and press [Enter]. A screen like the following
appears.


 

ABC-AG, AUTO, CONS & TRUCK CO CORPORATE STOCK ORDERS ¥3480-301 1
Division A Review Orders

CORP # CRPORDL

ORDER ORD#302

Part Number Order Quantity

10731 00100

Cmd3-Return Roll-Page  Home~Top of list

 

O This screen displays the part number and quantity ordered for each part
included in the order you chose. When you are finished reviewing the
order press [Cmd3] to return to the Review Orders screen.

RELEASE 2.3 CC

## X34-8 CORPORATE STOCK ORDER J

### Remove Stock Order

C To remove one of the stock orders included in a corporate order, put a
"3" next to the corporate order on Review Orders screen (the entrance
screen for this job). Press [Enter]. The Corporate Order Review screen
appears. Put a "4" next to the stock order you want to remove and press
(Enter]. The following screen appears.

BRIM TRACTOR COMPANY, INC. CORPORATE STOCK ORDERS
Division L Review Corp order
Remove Divisional Order

x3481-302 2

order # Vendor order Date Division ‘Type
Order: 0630 BBB 06/30/98 L STOCK

Enter-Remove Order cmd3-Previous screen

 

Press [Enter] to confirm the removal of the selected stock order. The
Review Corporate Order screen reappears.


| X34-8 CORPORATE STOCK ORDER ro

### Delete Corporate Order

From the Review Order screen (entrance screen for this job), put a "4"
next to the order you want to delete, press [Enter]. The following screen

appears.

BRIM TRACTOR COMPANY, INC. CORPORATE STOCK ORDERS x3480-002 2
Division L Delete Corporate Order

order # Ord Date =‘ Method Status
ROBLI 12/06/97 1 FINALIZED

Delete Divisional Orders (¥/N)?

All Suggested Stock Transfers created by the
Corporate Stock Order will also be deleted.

Enter-Delete Order Cmd3-Previous screen

 

O To delete the divisional orders included with corporate order, type a
"Y" at the prompt and press [Enter]. All suggested stock transfers
associated with the corporate order will be deleted as well. Press
[Enter]. The Review Order screen appears. The deleted entry is still
displayed on screen, but it will disappear when this job is exited and
restarted from the Stock Order menu (X34-8),

RELEASE 2.3 Ne


X34-8 CORPORATE STOCK ORDER |

### Finalize Corporate Stock Order

O To finalize a corporate stock order, place a "5" next to it on the Review
Orders screen. If the order is for Case, an Order Information screen,
illustrated below, will prompt you for the information needed to
transmit the order to Case’s host computer.

PRINT/FINALIZE ORDER cAaS1000RD1
Order Information CAS CORPOOO2

R&R EQUIPMENT SALES
Division: A

Shipping information

Routin
Order fype ry

F2-Continue F4=Prompt

 

To select from a list of valid Order Types, place the cursor in the Order
Type field and press F4=Prompt. You will be able to choose from: 1=Unit

Down, Air; 2=Daily, Surface; 3=Supplemental; 4=Stock.

When you press F2=Continue on the Order Information screen, the order
will be transmitted to Case.


faa X34-8 CORPORATE STOCK ORDER
14

ABC-AG, AUTO, CONS & TRUCK CO CORPORATE STOCK ORDERS *3480-001 2
Division A Review Orders

(Opt: lsMethod #1 2=Method #2 3-Review 4=Delete S=Finalize S<Print 7=Cor/Rev)

Opt Corp Ord# Ord Date Order Method Status PSO #

CPORDHA2 = 12/12/97 1 FINALIZED

job Roll-Page Home-Top of list

 

After an order is finalized, its status changes to FINALIZED, and it cannot
be changed.


X34-8 CORPORATE STOCK ORDER [=]

### Print Corporate Stock Order

O To print a corporate stock order, put a “6' next to it and press [Enter].
A message saying the stock order is being printed will appear. A
sample printout of a stock order follows.

‘THERMO KING Corporate stock order 32/13/97 Page

Order ¥ cPR#233 3460-68
DIV A DIV B DIv
sos s015 so1s

ww 220k 2208 220M

‘cas arooo0

cas aigooa

cas aiocsa

cas 11268

cas anza

cas 425623

cas 586

cas 5886

  


X34-8 CORPORATE STOCK ORDER -

 

CORRECT/RECEIVE CORPORATE STOCK ORDER

O To correct or receive a corporate stock order, put a "7" next to it and
press [Enter]. Only finalized stock orders may be selected. The
following screen appears

ABC-AG,AUTO,CONS & TRUCK CO. CORPORATE STOCK ORDER X3487-201 1
Division: A CORRECT ORDER BEFORE RECEIVING
CRPORDL

Qty Qty PA Supersession

vendor Part number Ordered Revd BC Part Number
1 cas 10731 100 100
2 YAM 93402002600 10¢ 100

Gmdl-End job Cmd2-Scroll/change ¢mad4-Random cmd8-Backorder
Cmd9-Automatic divisional distribution Cmdl0-Mamial divisional distribution

 

0 Review the list of ordered parts and confirm that the order is correct.
When you are finished, either press [Cmd9] to automatically make
distributions from many divisions to one division or [Cmd10] to
distribute the order among the divisions included in the report. A
Divisional Distribution screen appears.

.

### Fields And Definitions

Vendor

Part Number
PB

Action Code

Supersession Part #
Supersession Qty

Other Commands
[Cmd2]

[Cmd4}

[Cmd8]
[Cmd9]

[Cmd10]


3 characters. Vendor code.

Identifying part number.

1 character. Print bar code label.

1 character. Either blank or "B," "C," or “S."
B=Back Order, C=Cancel, S=Supersession. See
X342-] for more information on action codes.
Identifying part number of superseding part.
Number of pieces of supersession part.

Enters scroll/change mode. Used for viewing
additional pages or modifying existing information.
Enters random mode. If the order is several pages
long and you only have to make a change to one or
two parts, this is the command you would use.
After pressing [Cmd4], enter the vendor, part
number, and number received.

Puts every entry on the list on backorder.

Makes distributions from many divisions to 1
division automatically.

Distributes orders to different divisions.

## X34-8 CORPORATE STOCK ORDER C

 

### Divisional Distribution

Parts on Corporate stock orders can be distributed automatically from
many divisions to one division by using [Cmd9]or manually to different
divisions using [Cmd10].

Cmd9

To automatically distribute orders from many divisions to one division,
press Cmd9-Automatic divisional distribution. The Automatic Divisional
Distribution screen is displayed.

‘ABC-AG,AUTO,CONS & TRUCK CO. © CORFORATE STOCK ORDERS 43487-801
Division: A Automatic Divisional Distribution

Corporate order: CRPORDL (
Involving divisions: ADT ~
Automatically distribute receipt quantities

From division(s}: A T

To division: D

Press [Enter] to validate the selections on this screen.
Press Cmd2 to begin the automatic distribution.

Cmdl-End job without automatic distribution Cmd2-Begin automatic distribution

 

1. Fill in the “From” divisions and the "To" division. The divisions that
were involved in the current Corporate order are noted at the top of the

LO


 

screen. Pressing [Enter] validates the "From" and "To" divisions for
this order. In the example above, all parts ordered by Divisions A and T
will be distributed to Division D.

2. If you want to stop without distributing parts, press [Cmd1]; otherwise,
press Cmd2-Begin automatic distribution.

Cmd10
To manually distribute orders to the different divisions, press Cmd10-
Manual divisional distribution. The following screen appears:

‘ABC-AG, AUTO, CONS & TRUCK CO. CORPORATE STOCK ORDER x3487-303 1
Division: A Divisional Distribution Page 1
CRPORD1
Start ¥AM93402002600
Tot ORDH301 A ORD#302 B ORDHI03
Ven Part number Red #0RD #RCV #ORD #RCV #ORD #RCV
cas 10731 100 100 100
YAM 93402002600 100 100 100

Cmdl-End md2-Return to Correct Screen Cmd3-Page Right  Cmd6-Receipt

 

0 This screen indicates the quantity of parts received and how they are
distributed by each division considered in making the report. To
change an entry, tab over to the appropriate field, type in the correct
information, and press enter. If more than four were divisions were


X34-8 CORPORATE STOCK ORDER co

included in the corporate report, you will have to use [Cmd3] to shift
the page right to see additional ones. Once you are satisfied that the
corporate order is correct, press [Cmd6] to receive it. The parts files for
all divisions included in the order are updated automatically. If a
suggested stock transfer was generated with the order, you will have to
post that as well. Refer to that chapter (X34-9) for more information.

You can retum to the Correct Order screen at any time by pressing
[Cmd2] or to the Review List by pressing [Cmd1].

LL

## CHAPTER X34-8

CORPORATE STOCK ORDER

### Introduction

Corporate Stock Order creates a multi-divisional stock order using one of
two methods. Method 1 combines separate stock orders created through
Create Suggested Stock Order (X34-1) or Create Manual Order (X34-2).
Method 2 combines quantities and histories from selected divisions and
generates a corporate order from the results. If you use method 2, an
option also exists to create a suggested stock transfer. Once a corporate
stock order is received, the user can freely distribute the parts included in
it among the divisions used in generating the order.

### How To Run

From the Stock Order Menu (X3-4), select option 8, Corporate Stock
Order. Enter your division and password at the security gate and press
[Enter]. The following screen appears.


ABC-AG,AUTO,CONS & TRUCK CO CORPORATE STOCK ORDERS *3480-001 1
Division A Review Orders

(Opt: lsMethod #1 2=Method #2 3=Review 4=Delete 5=Finalize 6=Print 7=Cor/Rev)

Opt Corp Ord# Ord Mate Order Method Status PSO #

(mai-Ené job Roll-Page Home-Top of list

 

Each line on this screen represents a corporate stock order. Individual
orders can be created, reviewed, deleted, finalized, printed, or received.

O To perform one of these actions, type the appropriate number next to an

order and press [Enter]. Refer to the sections below for details on
creating, finalizing, and receiving a corporate stock order.

RELEASE 2.2 LO


X34-8 CORPORATE STOCK ORDER [:]

### Fields And Definitions

Corp. Order# 8 characters.

Order Date 6 digits.

Order Method "1" for method 1; "2" for method 2.
Status Either “Open” or "Finalized."
PSO# 7 digits.

### Creating A Corporate Stock Order—Method 1

This is the general procedure used by Method 1 for creating a Corporate
Stock Order:

= The user selects individual stock orders created through Create
Suggested Stock Order (X34-1) or Create Manual Order (X34-2).
Selected stock orders have to be finalized.

= The individual stock orders are combined and used to generate a
single corporate stock order

= The user reviews and then finalizes the corporate stock order.
Once the corporate stock order is finalized, all the stock orders
included in it become finalized as well. The computer then
determines how the parts in the corporate stock order are
distributed to each division used to generate the order. If
necessary, the user modifies the parts distribution list of the order
and receives the order. Each division's parts inventory is changed
accordingly.


[+] X34-8 CORPORATE STOCK ORDER

### How To Use Method 1

O From the Review Orders screen, enter a "1" in the field on the top-left.

In the field next to it, enter the Order Number of the new corporate
order. Press [Enter] The following screen appears.

ABC-AG, AUTO, CONS & TRUCK CO CORPORATE STOCK ORDERS
Division A Select Orders Method 2
ORDER 4 CRPORDI

3481-001 1

(Options: 1=select)

order # = Vendor order Date Division

oRDH301 CAS 12/09/97 BR
ORD#302 CAS 12/09/97 B
ORD#303 AM 22/09/97 ™

cmd3-Return  Roll-Page Home-Top of list

QO Each entry on this list represents a stock order made through
Create Suggested Stock Order (X341-1) or Create Manual Order
(X341-2). Select all the stock orders you want to include in the
corporate stock order by placing a "1" in the opt field. Press
Lo


X34-8 CORPORATE STOCK ORDER |

[Enter] when finished. All of the "1"'s you entered will disappear,
but otherwise the screen will appear the same. Press [Cmd3] to
return to the Review Orders screen.

O The order may now be reviewed, deleted, or received. Refer to the
sections below for more information on performing these tasks.

### Creating A Corporate Stock Order—Method 2

This is the general procedure that Method 2 uses in creating a Corporate
Stock Order.

= The user responds to a list of prompts about the corporate order,
specifying information such as vendor, class, and order number.
The user also has the option of creating a suggested stock transfer.
If this option is taken, this job will make a suggested stock transfer
and, in making the corporate order, assume that the stock transfer
has already taken place.
The user selects which divisions the corporate order will include.
The computer creates stock orders for each selected division.
These are combined and used to generate a corporate stock order.

= The order is reviewed and then finalized. Based on inventory and
sales history, the computer determines how many parts from the
corporate stock order are distributed to each division included in
the Stock Order. If necessary, the user modifies the order's
divisional distribution and then receives it. Each division's parts
inventory is changed accordingly.

= Ifthe user opted to create a suggested stock transfer, the transfer is
then posted. See Suggested Stock Transfer (X34-9) for more
information.

«The user optionally assigns a time to generate the order.

### How To Use Method 2

O From the Review Orders screen, enter a "2" in the field on the top-left.
In the field next to it, enter the Order Number of the new corporate
order. Press [Enter] The following screen appears. The prompts are
described below.

ABC-AG,AUTO,CCNS & TRUCK CO. Create Corporate Order 3462-001 1
Division: A

From the given information a corporate stock order will be printed:

Classies) or ALL ALL
Order Start Date 120997

Days Supply (1 to 365) .. 120
: 80152200

Create/Print Suggested Stock Transfer (Y/N) . N
Enter character to select by part category
Use available/on order quantities to calculate order (Y/N) Y

cmd-2 Select Divisions for Corporate Order Cmd3-Return

Vendor Code 3 characters. Enter the vendor that will
receive the Corporate Stock Order.
LU


Class(es) or ALL

Order Start Date

Days Supply

Order Number

Create Suggested Transfer

Enter character to select
by part category


3 characters. To request an order for more
than one class, but not all classes, type 1
class code on the first line and up to 13 more
on the next line.

6 digits. Type in the beginning date of your
stocking period. A future start date will
change the sales history period the system
considers when selecting parts for the order.

3 digits with a maximum value of 365. This
is the number of days supply this order will
cover.

8 characters. You may change it to an order
name or number of up to 8 characters. Order
number defaults to S0O1MMDD (MM is 2
digits for the month, DD is 2 digits for the
day).

If "Y," the corporate stock order will be
generated as if the suggested transfer has
already occurred. Post the transfer with
Suggested Stock Transfer (X34-9). See that
chapter for more information.

1 character. This prompt refers to the part
category field on the Parts Posting &
Maintenance screen. It is furnished by some
price tapes; otherwise, it is user-defined. If
you don't want to select a particular class
category, leave this prompt blank.


|e | X34-8 CORPORATE STOCK ORDER

Use available/on order Enter a "Y" in this field.
quantities to calculate
report.

O After you have completed specifying this information, press [Cmd2] to
select the divisions that will be included in the order. The following
screen appears.

ABC-AG, AUTO, CONS & TRUCK CO. Create Corporate Order x3411-102
Select Divisions

A Corporate Stock Order will be created from the divisions
you select. The combined stock order will use demand (
criteria from and will be shipped to Division a

ABC-AG,AUTO,CONS & TRUCK CO.
DEALER SALES & SERVICE, LTD.
ABC COMPANY

ABC COMPANY

MOTORCYCLE CITY

### Teermoking

Emdi-End Job Cmd2-Continue cmd-12 Select All Divisions

 

O Select the divisions that will be included in the report by placing a
character next to them. Select all divisions by pressing [Cmd12]. Press

RELEASE 2.2 LU


X34-8 CORPORATE STOCK ORDER [>]

[Cmd2] when you are finished. The Create Corporate Order (Method
2) screen appears. Press [Cmd3] to retum to the Review Orders screen.
As it may take some time for the new order to be generated, it will not
immediately be displayed on the screen. Quit this job and restart it
again to view the new entry.

### Review Corporate Order

Select the order you want to review in the Review Corporate Order screen
(the entrance screen for this job), put a "3" next to it and press [Enter].
The following screen appears.

ABC-AG, AUTO, CONS & TRUCK CO CORPORATE STOCK ORDERS 3481-301 3
Division a Review Corp order
ORDER # CRPORDI

(Options: 3=Review 4=Remove)
Vendor order Date Division
12/08/97 A

12/08/97 B
12/09/97 M

Cm@3-Return Roll-Page Home-Top of list

 


 

These are the individual stock orders that comprise the corporate stock
order you selected in the previous screen. To review an individual order
place a "3" next to it and press [Enter]. A screen like the following
appears.

ABC-AG,AUTO,CONS & TRUCK CO CORPORATE STOCK ORDERS 3480-301 1
Division A Review Orders

CORP # CRPORDI

ORDER ORD#302

Part Number order quantity

10731 00100

 

(
ma3-Return Roll-Page Home-Top of list
O This screen displays the part number and quantity ordered for each part
included in the order you chose. When you are finished reviewing the
order press [Cmd3] to return to the Review Orders screen.
\

RELEASE 2.2 oa


X34-8 CORPORATE STOCK ORDER ["]

### Remove Stock Order

To remove one of the stock orders included in a corporate order, put a
"3" next to the corporate order on Review Orders screen (the entrance
sereen for this job). Press [Enter]. The Corporate Order Review screen
appears. Put a "4" next to the stock order you want to remove and press
[Enter]. The following screen appears.

BRIM TRACTOR COMPANY, INC. CORPORATE STOCK ORDERS 3481-302 2
Division L Review Corp Order
Remove Divisional order

order # vendor Order Date Division ‘Type
Order: 0630 BBB 06/30/98 L

Enter-Remove Order cmd3-Previous screen

 

Press [Enter] to confirm the removal of the selected stock order. The
Review Corporate Order screen reappears.


| X34-8 CORPORATE STOCK ORDER C

### Delete Corporate Order

From the Review Order screen (entrance screen for this job), put a'"4"
next to the order you want to delete, press [Enter]. The following screen
appears.

BRIM TRACTOR COMPANY, INC. CORPORATE STOCK ORDERS x3480-002 2
Division L Delete Corporate Order

Order # ord Date Method Status
Order; ROBI11 12/06/97 1 FINALIZED

Delete Divisional Orders (Y/N)? N i

All Suggested Stock Transfers created by the
Corporate Stock Order will also be deleted.

Enter-Delete Order Cmd3-Previcus screen

 

O To delete the divisional orders included with corporate order, type a
“Y" at the prompt and press [Enter]. All suggested stock transfers
associated with the corporate order will be deleted as well. Press
[Enter]. The Review Order screen appears. The deleted entry is still
displayed on screen, but it will disappear when this job is exited and

RELEASE 2.2 CO


X34-8 CORPORATE STOCK ORDER [=]

restarted from the Stock Order menu (X34-8).

### Finalize Corporate Stock Order

O To finalize a corporate stock order, place a "5" next to it on the Review
Orders screen. Its status will be changed from “Open” to
"FINALIZED." An example follows.

ABC-AG, AUTO, CONS & TRUCK CO CORPORATE STOCK ORDERS 3480-001 1
Division A Review Orders

(Opt: 1-Method #1 2=Method #2 3sReview 4=Delete 5-Finalize 6=Print 7=Cor/Rev)

Opt Corp Ord# Ord Date Order Method Status PSO F

CPORDE42 = 12/12/97 1 FINALIZED

Gmdl-End job Roll-Page  Home-Top of list

 

Once an order is finalized, all of the stock orders that it includes are also
finalized and are no longer subject to change.


[1 | X34-8 CORPORATE STOCK ORDER

### Print Corporate Stock Order

O To print a corporate stock order, put a "6' next to it and press [Enter].
A message saying the stock order is being printed will appear. A
sample printout of a stock order follows.

THERMO KING - BELLINGHAM Corperata Steck order 12/13/97 Page
order # CPRR233, 1480-6
DIV A Orv B DIV §
8015 S015 5015
wo 2208 2208 2204
cas Al9000

cas aiooo1 ‘

tae aiiats rs

tas atiats

one 386

ens doe6 rows (
feeate

 

RELEASE 2.2 LL


CORRECT/RECEIVE CORPORATE STOCK ORDER

O To correct or receive a corporate stock order, put a "7" next to it and

press [Enter]. Only finalized stock orders may be selected. The
following screen appears

ABC-AG, AUTO, CONS & TRUCK CO. CORPORATE STOCK ORDER 3487-202 1
Division: A CORRECT ORDER BEFORE RECEIVING
CRPORD1

Qty Qty PA Supersession

vendor Part number Ordered Revd BC Part Number
20731 tea 100
YAM — 93402002600 100-100

Cmdl-End job Cmd2-Scroll/change Cmd4-Random Cmd8-Backorder
Cmd9-Automatic divisional distribution Cmdl0-manual divisional distribution

 

O Review the list of ordered parts and confirm that the order is correct.
When you are finished, either press [Cmd9] to automatically make
distributions from many divisions to one division or [Cmd10] to
distribute the order among the divisions included in the report. A
Divisional Distribution screen appears.


co

Fieids and Definitions

Vendor 3 characters. Vendor code.
Part Number Identifying part number.
PB 1 character. Print bar code label.

Action Code
Supersession Part #
Supersession Qty

Other Commands
[Cmd2]

{Cmd4]

[Cma8}
[Cmd9]

[Cmd10]

1 character. Either blank or "B," "C," or "S."
B=Back Order, C=Cancel, S=Supersession. See
X342-1 for more information on action codes.
Identifying part number of superseding part.
Number of pieces of supersession part.

Enters scroll/change mode. Used for viewing
additional pages or modifying existing information.
Enters random mode. If the order is several pages (
long and you only have to make a change to one or
two parts, this is the command you would use.
After pressing [Cmd4], enter the vendor, part
number, and number received.

Puts every entry on the list on backorder.

Makes distributions from many divisions to 1
division automatically.

Distributes orders to different divisions.

{
RELEASE 2.2 Ne

### Divisional Distribution

Parts on Corporate stock orders can be distributed automatically from
many divisions to one division by using {Cmd9]ormanually to different
divisions [Cmd10]

Cmd9

To automatically distribute orders from many divisions to one division,
press Cmd9-Automatic divisional distribution. The Automatic Divisional
Distribution screen is displayed.

‘ABC-AG,AUTO,CONS & TRUCK CO. CORPORATE STOCK ORDERS 3487-801
Division: A Automatic Divisional Distribution

Corporate order: CRPORD]

Involving divisions: ADT

Automatically distribute receipt quantities
From division(s): AT

To division: D

Press [Enter] to validate the selections on this screen.

Press Cmd2 to begin the automatic distribution.

Cmd1-End job without automatic distribution Cmd2-Begin automatic distribution

 


18 X34-8 CORPORATE STOCK ORDER

™
}

1. Fill in the "From" divisions and the "To" division. The divisions that
were involved in the current Corporate order are noted at the top of the
screen. Pressing [Enter] validates the "From" and "To" divisions for
this order. In the example above, all parts ordered by Divisions A and T
will be distributed to Division D.

2. If you want to stop without distributing parts, press [Cmd1]; otherwise,
press Cmd2-Begin automatic distribution.

Cmal0

To manually distribute orders to the different divisions, press Cmd10-
Manual divisional distribution. The following screen appears:

‘ABC-AG, AUTO, CONS & TRUCK CO. © CORPORATE STOCK ORDER x3487-301 1
Division: A Divisional Distribution Page 1 (
CRPORDL
Start ¥AN93402002600
fot ORDH3O1 A ORD#302 -B ORDEO3  M
Ven Part number FORD FRCV #ORD ¥RCV #ORD #RCV
CAS 10731 100 100
YAM 93402002600 100 100

Cm@i-End Cma2-Return to Correct Screen Cmi3-Page Right Cmd6-Receipt

 

RELEASE 2.2 LU


X34-8 CORPORATE STOCK ORDER [=]

Q This screen indicates the quantity of parts received and how they are
distributed by each division considered in making the report. To
change an entry, tab over to the appropriate field, type in the correct
information, and press enter. If more than four were divisions were
included in the corporate report, you will have to use [Cmd3] to shift
the page right to see additional ones. Once you are satisfied that the
corporate order is correct, press [Cmd6] to receive it. The parts files for
all divisions included in the order are updated automatically. If a
suggested stock transfer was generated with the order, you will have to
post that as well. Refer to that chapter (X34-9) for more information.

You can return to the Correct Order screen at any time by pressing
[Cmd2] or to the Review List by pressing [Cmd1].


Notes:

## CHAPTER X34-9

SUGGESTED STOCK TRANSFER

### Introduction

Suggested Stock Transfer allows you to post stock transfers created by
Corporate Stock Order (X34-8). Individual stock transfers may be posted,
deleted, reviewed, or printed.

### How To Run

From the Stock Order menu, select option 9. Enter your division and
password at the security gate. The following screen appears.

THERMO KING - BELLINGHAM SUGGESTED STOCK TRANSFERS 3490-001 1
Division A Review Transfer
(Opt: 1=Post 3-Review 4=Delete 6=Print)
Opt Corp ord# ord Dat

CRPORD?6 = =—-12/13/94

Gmdi-End job Roll-Page Home-Top of list

 

Each entry on this list represents a suggested transfer report made by


[2] X34-9 SUGGESTED STOCK TRANSFER co

Corporate Stock Order (X34-8). Entries may be posted, reviewed, deleted,
or printed.

Posting a Suggested Stock Transfer

Q To post a suggested stock transfer, put a "1" next to the transfer and
press [Enter]. A message saying that the transfer is being posted will
be displayed.

{
RELEASE 2.1 NS


X34-9 SUGGESTED STOCK TRANSFER |

Reviewing a Suggested Stock Transfer

O To review a suggested stock transfer, put a "3" next to the transfer and
press [Enter]. A screen like the following appears.

THERMO KING - BELLINGHAM © SUGGESTED STOCK TRANSFERS *3491-301 1
Division A Review Transfers
‘TRANSFER# CRPORD42

Part Number Quantity From Div To Div

11208 ooo1g
11208 o0006
al1212 90003
55CO 90020

Cmd3-Return Roll-Page Home-Top of list,

 


[+] X34-9 SUGGESTED STOCK TRANSFER ( se

Deleting a Suggested Transfer Order

O To delete stock transfer orders, put a'"4" next to the orders you want to
delete and press [Enter]. A screen like the following appears.

THERMO KING - BELLINGHAM SUGGESTED STOCK TRANSFERS %3490-002 2
Division A Delete Suggested Transfers
order # ord Date

order: ORD#I44 12/13/9

Enter-Delete Order cmé3-Previous screen

 

O Confirm that you want these reports deleted by pressing [Enter]. The
Review Stock Transfer screen appears.

LL


X34-9 SUGGESTED STOCK TRANSFER [=|

Printing a Suggested Transfer Order

O To print a suggested transfer order, put a "6" next to it and press
[Enter]. A message saying that the order is printing will appear and a
report will be sent to the system printer. An example Suggested
Transfer Order follows:

THERMO KING - ELLINGEAM Suggested Stock Transfel2/13/94 Page 1
‘Transfer ¥ CRPEG2 3480-68,
part QUANTITY FROM DIV. TO DIV
11208 13 a

11208 6 4"
AMIaia 3 "
ssc0 20 a

 


Notes:

## CHAPTER X35-1

CREATE STOCK RETURN

### Introduction

The Create Stock Return job allows you to return the maximum number of
eligible obsolete or slow moving parts to a manufacturer. Parts are chosen
for the stock return based on the criteria you specify when setting up the
return. Selections include number of months without sale, manufacturers
return code and cost of the part. Returns are based on available quantities,
not on hand.

If you want to return unbroken packages only, the return quantity can be
adjusted according to the package quantity. For example, there are 11 of
Part A available, and a package is made up of 4 of Part A. Create Stock
Return divides the available quantity by the package quantity (11/4 =2
packages + 3 parts). It will suggest that you return 8 parts (2 packages).

A summary of the questions asked by the program to determine a part's
eligibility follows. An answer of "no" to any of the questions disqualifies
the part for the return.

CIs the part in the same vendor as the requested report?

CIs the part in the same division as the requested report?

Js the part in a class that is requested on the report?

C1 Is the on hand quantity greater than zero?

C7 Is the available quantity greater than zero?

O If return codes are selected, does the return code on the part match?

If you subtract the date added from the session date (counting in

months), is the result greater than the “Minimum Months Part in

Inventory" requested on the report?

CIs the on hand quantity greater than the last 12 months pieces sold?

Counting the months backward from the session date, find the first

piece or call recorded. ts the number of "blank" history months equal to

or greater than the "Minimum Months of No Sales” requested on the
report?

0 Subtract the number of pieces sold in the last 12 months from the on
hand quantity. Multiply this number by the cost of the part. Is the result
equal to or greater than the "Minimum Dollar Value per Line"
requested on the report.

## X35-1 CREATE STOCK RETURN

### How To Run

 

 

 

From the Parts Menu (X3), select Option 5, Stock Re turn/Phase Out
Menu.

 

O From the Stock Return/Phase Out Menu, select Option 1, Create Stock
Return. The selection screen appears.

 
  

    

### Agr Equipment Sales Create Stock Return X3510-101

     
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
 

Given the following information a suggested stock return will be printed

Vendor (Or ALL) .
Class (Or ALL) ..

 

Return Number 2.000.000.0020. ..c0e eee 2718
Selection of Manufacturer Return Codes

To Include or Exclude On Retura (1/E) .. E
Return Codes

{Enter ‘+' for a blank return code}

Minimum Months Part in Inventory .
Minimum Months of No Sales (Max. 24)
Minimum Dollar Value Per Line .......... 1
Maximum Dollar Total For fach Vendor ... 10000
Include parts already on a return (¥/N). ¥
Enter ‘¥' to print in bin location order N
Adjust by package gty (¥/N) ..... -N
Include superseded parts (¥/Ni.. iN

  

 

 
 

mdi -Cancel

 

 

 

Type a vendor code or "ALL."

C) Type the specific class or ALL.

O Type an identifying number for this return.

O Type J to include, or E to Exclude up to 10 return codes. Leave this

 

RELEASE 2.1 C “


X35-1 CREATE STOCK RETURN [2]

option blank to ignore return codes when selecting parts for this return.

Type the return codes to be included or excluded. If you want to

include or exclude a blank return code type +.

O Type the minimum number of months a part must be in inventory

before being considered for this return.

C Type the minimum number of months of "no sale" for a part. This
number can be no larger than 24.

Type the maximum total for each vendor. This amount must be entered

or the entire return will be excess. Refer to the Excess Returns report

section below for more information.

 

 

 

 

 
   
  

Note:

 
 
 
     
    

The date a part is added to inventory can be found in the “date added"
field in Parts Inquiry. For most parts the date added will be the date the
parts were entered into the computer. Some parts, added from
conversion tapes, will have the actual date the part was brought into
your physical inventory. Check your parts for the correct date.

 

If your parts have an add date of 2 months ago and you specify a

minimum of 6 months in inventory, you will get a blank suggested
return.

O Type minimum number of months of no sale. This information is taken
from the sales history (not Last Sale Date) on each part.

O Type a minimum dollar value for each line. Do not include decimal

places. The dealer net on each part must be greater than the minimum

for the part to be considered.

Type the maximum doilar total you can return to this vendor. No

decimal places here either.

O Type a ¥ to print the report in bin location order. Leave the N for part

 

 

 

 


[ «| X35-1 CREATE STOCK RETURN ( .

number order.

To return full packages only, type Y to adjust by package quantity.

©) You can choose to include superseded parts on the report or not. The
prompt will default to not include superseded parts, however, if you
choose to include them, type Y and they will appear on the return and
the supersession will print on the report as it does with a regular stock
order.

O Press ENTER. The report will be placed on the job queue. Press
ENTER to return to a menu.

 

 

 

 

Suggested Stock Returns vs. Excess Returns

The report prints in two parts, Suggested Stock Return and Excess

Returns, The Excess Returns Report is comprised of parts whose value

would exceed the vendor's Maximum Dollar Total. Parts included on the t
Excess Returns report do not have their Retums Qty field updated.

Instead, this return represents parts that could be manually added or

exchanged for parts on the Suggested Return Report. Parts on the

Suggested Return, on the other hand, do have their Return Qty fields

updated. This figure will match the Available Qty. These parts can be

accessed and edited in X3-5, Correct Stock Order.

### Move Lines Between Stock Returns

Move Order Lines (X34-6) can be used to move lines from one stock
return to another. Refer to that chapter for more information.

RELEASE 2.1 LU

### Suggested Stock Return Report

    
         
   

      

     
      
    
 
  

 

AGR EQUIPMENT SALES Excess Returns Minimum Months No Sales 3 9/26/97 Page 1

LYNDEN, WA A Vendor cASE/IH Minimum Line Value $i 23.26.35 x3510-5B
Maximum Return Value $10000

Part Number--. * Description Class Return Last Location Mths Last 12 ytd Pys Avail. Return Dealer

 

Extended

  

 

 

Oty Sale No Sale Mths Qty code Net

    
  

 

value

 

 

  

Total Excess Returns Fer CASE/IE Lines 00
Pieces

 
  
  
 

   

AGR EQUIPMENT SALES Excess Returns Grand Totais 9/26/97 Page 2
LYNDEN, WA A 13.26.35 X3510-5B

 

     
  

Grand Tota?

  


[<] X35-1 CREATE STOCK RETURN

### Fields & Descriptions

Part #
Description
Class
Return Qty

Last Sale
Location
Mths No Sale
Last 12 Mths
Ytd

Pys
Available Qty

Return Code
Dealer Net
Extended Value

Identifying number for the part.

Brief description of the part.

Class code of the part.

Quantity of this part number suggested for
return. (Equals available quantity minus
number sold in Jast 12 months. Adjusted by
package quantity, if requested.)

Last sale date of the part.

Bin location.

Number of months without a sale.
Number of sales in the last 12 months.
Number of sales in this calendar year.

Past year sales.

Quantity of the part that is available.

(On hand minus reservations).

Dealer or vendor defined return code.
Cost of one part to the dealer.

Dealer net multiplied by return quantity.

The Total suggested return and grand totals are printed at the end of the

order.
LC


X35-1 CREATE STOCK RETURN [7]

### Excess Returns Report

BELLINGHAM CAR & TRUCK CO. Bxcess Returns Minimum Months Ne Sales 3 67/12/97 page 5.
BELLINGHAM, WA a vendor SUMMING Minicum Line value sa 7.97.14 x3810-58

Mexinun Return Value $10000
Daseription Glass Return Last Lecation Mths Last 12 ed Pys Avail. Return Dealer sxtended
ay Sale No Sale Mths Qty coe = Net Value
Total Excess Returns For CUMMINS bines 08
Pieces

 

This report has the same fields as the Suggested Return report. Parts on
this report meet all criteria for return, but including them on the return
would cause the return to exceed the maximum dollar value allowed by
this vendor.

When all of the eligible parts will not fit on the Suggested Return, parts
are placed on the return in order of extended value. Sometimes the
suggested return will exceed the maximum value set by you. Let's say you
indicate a maximum return of $1000. The eligible part with the highest
extended value has a dealer net of $100 and you have 15 in inventory. This
part has no sales in the past year so 15 is the return quantity. All 15 parts
will be placed on the return even though the return value will be greater
than $1000.

 


Notes:

## CHAPTER X35-2

CORRECT STOCK RETURN

### Introduction

Correct Stock Return allows you to:
" correct a stock return, by

- adding,

- changing,

- deleting
"create a manual stock return

### How To Run

From Menu X35 select option 2 to Correct Stock Return. Type in your
desired Vendor Code, Return Number and either 'C’ to change an existing
Stock Return or ‘N' to create a manual Stock Return. Press Enter. The
Stock Return Correction screen appears.

## X35-2 CORRECT STOCK RETURN

 

### Abc Company Stock Return Correction 3412-201

Division: E Price book: BUSHHOG = BHG RA123456 Lines sere 4
Current mode: SCROLL AND CHANGE LINES Extended Amt 701.20
Quick Qty
Part Number Code ordered
SPO08 2
SPOSC 1
SP171 1
SP258 5


ts (

Press Cndl to end job cmd? to scroll and change lines Cmd3 to add lines
cmd4 to randomly change lines Cmd5 to add new parts

 

### Options

 

 

 

To scroll and change lines, press CMD 2.

15 lines will appear on the screen in sort sequence.

You may only change the QUANTITY in this mode. Press ENTER to
display the next 14 lines of the order.

 

{
RELEASE 2.1 NW


 

Note:

display if quantity is negative or greater than 100.

 

The last part will display as the first on the next screen. A message "|

O To add lines already in inventory to the order, press CMD 3. 15 blank
lines will become available for additions. Type in the part(s) and
quantities desired. If the parts are not in inventory, segment the part on
screen by typing a less than symbol between each segment and at the
end of the number. Press ENTER to add them to the order and to put
them in the vendor's default class. The part information will need to be
input aiso. (If you use CMD S instead of 3, you may add the part
information. Or go into Parts Posting and Maintenance when this job is
complete to add the part information.)

Note:

I If there are parts with errors, the screen will clear the parts up to the
part with error(s). If error-free, a new screen will be displayed.

 

 

 

 

To randomly change lines, press CMD 4.

15 lines are available on the screen at one time for changing. The
changes may be arranged in any order on the screen. Type in part
number and quantity.

 


 

Note:

If a part number does not exist in your inventory and you try to order
it, or you enter a part wrong, the message at the bottom of the screen
will say the new part number has an invalid format. In other words,

how the part is set up needs to be changed. Check how the vendor is
configured: how many segments or sections per part number. Then
create or change the format by typing a less than symbol between each
segment and at the end of the number. Press ENTER. This will add the
part to inventory with the default class code, order code, and base
codes.

 

O To DELETE a part from the order, enter a zero for the quantity. (
O To end the job, press CMD 1.

To add new parts to inventory and to the order, press CMD 5. Type a
less-than symbol between segments and at the end of the part number.

Be sure to type in an order quantity to add the part to the order. If you

leave the field blank, the part will be added to inventory, but will not be

added to the order.

 

 

 

 


For all of these operations, insure that you press ENTER before taking a
CMD 1 to end the job or change modes. Otherwise the changes or
additions will not be made.

After all changes, corrections, and/or deletions are complete, press CMD
1 to end the job.

Note:

The Current Mode is in the upper left corer of the screen. If you wish
to change to any of the above modes, those mode changes are reflected
here.

 

### Move Lines Between Stock Returns

Move Order Lines (X34-6) can be used to move lines from one stock
return to another. Refer to that chapter for more information.


Notes:

RELEASE 2.1 \

## CHAPTER X35-3

CANCEL STOCK RETURN

### Introduction

Use this job to cancel one or more stock returns.

Note:

### Do Not Cancel A Stock Return Which Is Being

CREATED. Check the user board to be sure that all X351__
procedures have completed.

 

### How To Run

From the Stock Return/Phase-out Menu (X3-5), select option 3 to Cancel
Stock Return. When prompted, type in the Vendor Code and Retum
Number of the return you want canceled. Press Enter.

Note:

If you press Cmd1, you will end this job without canceling the stock
return. You must complete the process by pressing ENTER.

## X35-3 CANCEL STOCK RETURN

 

RESULT: If you press ENTER, the return will be canceled. Stock return
information for all parts on this return will be deleted. Type another stock
return number to be canceled and repeat the process, or press Cmd1 to
cancel the job and return to the Stock Return/Phase Out

Menu.

RELEASE 2.1 LL

## CHAPTER X35-4

PRINT/FINALIZE RETURN

### Introduction

Print Stock Return allows you to finalize and print a final return when you
are ready to return stock to the manufacturer. This job does nof post your
stock return. Use option 5 from Menu X35 to post your retum after
printing.

Move Order Lines (X34-6) can be used to move lines from one stock
return to another. Refer to that chapter for more information.

When a return for a configured AGCO or New Holland vendor is
finalized, it is transferred to the PC where AGCO Solutions On-Line or
New Holland DCS is installed. When a return for Case is finalized, it is
sent directly to Case via the DIS Electronic Commerce Manager. To learn
more about DIS Electronic Commerce Manager and Client, see Chapters
X6-15 and X6.15-1, which include configuration and troubleshooting
instructions.

AGCO ™Returns

After you press [Enter] on the Print/Finalize Return screen, the return is
placed on the job queue. Press [Enter] again to return to the Stock
Return/Phase Out menu. If you are using DIS Electronic Commerce,
returns for configured AGCO vendors will be picked up within 10 minutes
(or the polling time you selected) and transferred to the appropriate
directory for AGCO Solutions On-Line.

Case Returns
An additional screen is presented after an order for Case is finalized. It is
described on page 5.

New Holiand Returns
An additional screen is presented after an order for a configured New
Holland vendor is finalized. It is described on page 6.


[=| X35-4 PRINT/FINALIZE RETURN

### How To Run

 

 

 

 

From Menu X35, select option 4 to Print/Finalize Return.

] When prompted, type in the Vendor Code and Return Number. Press

[Enter].

AGR EQUIPMENT SALES

(mdl-cancel job

 

PRINT/FINALIZE RETURN X3413-201

Vendor Code CAS
Return Number R120898

Finalize (¥/N) ¥ {

Dealer Number 0022385800

Special Shipping Instructions

FIRST LINE OF SHIPPING INSTRUCTIONS
1234567890123456789012345678901234567890

vendor Return
Authorization Number ERB

0 Type your Dealer Number, Special Shipping Instructions, and the
return authorization number from your vendor. Press (Enter). If the
return is for Case or New Holland, an additional screen will be
displayed; otherwise, the job is placed on the job queue. You return to

RELEASE 2.3 Lo


X35-4 PRINT/FINALIZE RETURN

the . The stock return will be printed on the system printer.

An example of a Printed stock return is illustrated below.

 
 

ABC COMPANY
STH SP AND vine

  
     

AEC company

 
  

S08 ST AND vine
winter, co 83208 wimor, co 83204

   
       
  
 

RETURN NUMBER 1234567 RETURN NUMBER 1234567
DEALER NUMBER MANI2345 DEALER NUMBER MANL2345
x -

   
 

 
 

SPECIAL SHIPPING INSTRUCTIONS: SPECIAL SHIPPING INSTRUCTIONS:
FIRST LINE OF INSTRUCTIONS FIRST LINE OP =NSTRUCETONS

 

 
  
  

 

‘Venpon RETURN
AUTHORIZATION NUMBER AMAI23¢

   
 

VENDOR RETURN
AUTHORIZATION SUMBER RMAIZ3¢

   
   
      

          
           
      
          
 
   
   
 

 
   

    

STEIGER yo/oa/97 PASE 1 STEIGER 10/03/97 page

ory paRT 4 * DESCRIPTION COST AMOUNT LOCATION PACK S-3 PART ¢ =" DESCRIPTION ory
3 02-2085 BELD spr 1751 ans ea a4 01-2059 BELT ser 2
1 01-2068 PILTER 6.23 6.2384 ae 02-2065 FILTER 2
2 01-2228 BELT 5.93 Saag ce 01-2228 Bau 2
46 01-7234 FILTER 7.61 123.76 818 01-2534 PUTER 1s
1 ot-z335 FILTER 10.57 aar.es Bac 01-2335 FILTER M
€ c1-2336 FILTER $81 S8eena 2 01-2336 FILTER 6

  

  
   

  
   

    
        
  
 

2 on-2367 came 54.99 S495 a 91-2867
1 oa-a332 oD evn 5.62 5.6143 pea 93-3332 Ror END 1
1 0t-36as cape 67.84 678k SA 03-3685 corse 1
2 oi-3as2 RELAY 9.66 9683 RS 01-3861 RELAY a
2 oi-eiss Sarre 20.88 10.86 #3 BF 01-4299 surree 1
2 ox-a22 SENDER 28.32 BS o1-4222

 
  

91-4458

 
  
  

  

oreea72 SWITCH 303 01-4072 sarten 1

 

1 oi-aee CABLE 4250 41.50 n 5a O1-¢4ar caBLe: 1
2 ¢1-61s0 suzteH

2 01-6252 swrtes

 
  
  


[+] X35-4 PRINT/FINALIZE RETURN

### Fields & Descriptions

Qty
Part #

Description
Dealer Net
Amount

Location
Pack/O-I

Part #

Description

Qty

Amount of the part being retumed.

Part identifying number.

Brief description of the part being returned.
Cost of the part to the dealership.

Quantity or number of the part returned
multiplied by the Cost.

Location of the part in your dealership.
Package quantity or original number for the
order-instead.

Identifying part number. Separate the order
here; keep one and send the other with the
return order.

Brief description of the part being returned.
Amount of the part being returned.


X35-4 PRINT/FINALIZE RETURN Le]

### Case Returns

On Case returns, after you press [Enter] on the Print/Finalize Return
screen, the following Return Information screen is displayed.

PRINT/FINALIZE RETURN CAS1OORTN1
Division: A Return Information cas R120898

Return Type 3
Return Type ID MONTHLYRET

 

Return Type must be equal to a 3

AND

to properly send a return to CASE.


| Return Type ID must equal MONTHLYRET
i
Il

 

F2eCentinue F4=Prompt

 

As of 12/8/98, the only valid entries in these fields are defaulted: Return
Type=3 and Return Type ID=MONTHL YRET. To select from a list of
valid return types or Ids, press F4=Prompt with the cursor in the
appropriate field. Press F2=Continue. The procedure will be placed on the
job queue. Press [Enter] to return to the Stock Return/Phase Out Menu.


[=] X35-4 PRINT/FINALIZE RETURN Co

NEW HOLLAND RETURN INFORMATION SCREEN

Returns cannot exceed 1,000 lines.

When you press [Enter] on the Print/Finalize Return screen, the New
Holland Return Information screen is displayed.

AGR EQUIPMENT SALES New Holland NHDLOORTNL

Division A Return Information FOR FORDRTN

order Class

F4=Prompt

 

1 Enter an Order Class or press F4=Prompt to select from a list of valid
return types, which are:

A=Annual

RELEASE 2.3 LL


X35-4 PRINT/FINALIZE RETURN

 

T=Initial
L=Leveling
T=Termination

Technical note: Parts return filenames are 8 characters plus a 3-character
extension, such as Nxxxxxxx.R$R, where N represents the type of return,
such as A=Annual, "R" signifies a parts return, and the last R=Ready to
Send. When the file has been successfully sent the extension is renamed to
R$S, which prevents the file from being sent again but retains it for future
use.

 

 

Press [Enter] to proceed. The job is placed on the job queue. Press
{Enter] to return to the Stock Return/Phase Out menu. The return file
will be placed in the appropriate directory for New Holland DCS.


Notes: CO

## CHAPTER X35-4

PRINT/FINALIZE RETURN

### Introduction

Print Stock Return allows you to finalize and print a final return when you
are ready to return stock to the manufacturer. This job does not post your
stock return. Use option 5 from Menu X35 to post your return after
printing.

Move Order Lines (X34-6) can be used to move lines from one stock
return to another. Refer to that chapter for more information.

When a return for a configured AGCO or New Holland vendor is
finalized, it is transferred to the PC where AGCO Solutions On-Line or
New Holland DCS is installed. To learn more about DIS Electronic
Manager and Client, see Chapters X6-15 and X6.15-1, which include
configuration and troubleshooting instructions.

AGCO Returns

After you press [Enter] on the Print/Finalize Return screen, the return is
placed on the job queue. Press [Enter] again to return to the Stock
Return/Phase Out menu. If you are using DIS Electronic Commerce,
returns for configured AGCO vendors will be picked up within 10 minutes
{or the polling time you selected) and transferred to the appropriate
directory for AGCO Solutions On-Line.

New Holland Returns
An additional screen is presented after an order for a configured New
Holland vendor is finalized. It is described on page 5.


[| X35-4 PRINT/FINALIZE RETURN co

### How To Run

 

 

 

From Menu X35, select option 4 to Print/Finalize Return.
O When prompted, type in the Vendor Code and Return Number. Press
[Enter].

 

ABC COMPANY PRINT/FINALIZE RETURN x3413-101

Vendor Code MAN
Return Number 1234567

Dealer Number MAN12345 (

Special Instructions

FIRST LINE OF INSTRUCTIONS
SECOND LINE

Vendor Return
Authorization Number  RMA1234

Cmdl-Cancel job

 

O Type your Dealer Number, Special Shipping Instructions, and the
return authorization number from your vendor. Press [Enter]. The job
is placed on the job queue. Press [Enter] again to return to the Stock
Return/Phase Out Menu. The stock return will be printed on the system
printer.

RELEASE 2.1 Ne


ABC COMPANY
STH ST AND VINE
wHYNOT, co.

X35-4 PRINT/FINALIZE RETURN

An example of a printed stock return is illustrated below.

53204

RETURN NUMBER 1234567
DEALER NUMBER MANI2245

SPECIAL SHIPFING INSTRUCTIONS:
FIRST LINE OF InsTRUCTIONS

VENCOR RETURN

ROTHORIZATION NOMBER RMAI2I4

STEIGER
PART @
91-2089
91-2065
04-2228
c1-2338
c1-2338
21-2336

2 03-2857
01-3232
01-3685
91-3862
01-4199
91-4222,

92-4458
01-2472
01-4482
01-6150
02-6152


20/01/97 PAGE
" DESCRIPTION
BELT SET
PILTER


cost
33.8t
6.23
$.93
161
16.87
9.82
54.98
61
84
88
86

AMOUNT LOCATION
1.51 #4 e-4
6.23 Be Add
5.93

321.78

147,98
s2.86

### Fields & Descriptions

Qu

Part #
Description
Dealer Net
Amount

ABC COMPANY
STH S? AND VINE
wRYNOT, co 83204
RETURN NUMBER 1234567
DEALER NUMBER MANIZ345
Kee.

SPECIAL SHIPPING INSTRUCTIONS

FIRST LINE OF INSTRUCTIONS

VENDOR RETURN
AUTHORIZATION NUMBER RMAIZ34
‘STEIGER 10/01/87 PAGE 1
PACK $+5 PART ¥-~. --* DESCRIPTION
01-2058 BELT ser
53-2065 FILTER
02-2228 BELT
01-2534 FILTER
02-2235 FILTER
c1-2336 PILTER

01-2867
01-3332
01-3685,
02-3861,
01-4199
91-4222

o2-44se
or-4472
Ones
01-6159
o1-sisz

 

Amount of the part being retumed.

Part identifying number.

Brief description of the part being returned.
Cost of the part to the dealership.

Quantity or number of the part returned
multiplied by the Cost.


[| X35-4 PRINT/FINALIZE RETURN Co

Location Location of the part in your dealership.
Pack/O-I Package quantity or original number for the
order-instead.

Part # Identifying part number. Separate the order

here; keep one and send the other with the
return order.
Description Brief description of the part being returned.
Qty Amount of the part being retumed.

(
RELEASE 2.1 NN


N,

X35-4 PRINT/FINALIZE RETURN [=]

NEW HOLLAND RETURN INFORMATION SCREEN

Returns cannot exceed 1,000 lines.

‘When you press [Enter] on the Print/Finalize Return screen, the New
Holland Return Information screen is displayed.

A&R EQUIPMENT SALES New Holland NHDLOORTNL
Division A Return Information FOR FORDRTN

order Class

 

© Enter an Order Class or press F4=Prompt to select from a list of valid
return types, which are:

A=Annual
T=Initial

L=Leveling


[ «| X35-4 PRINT/FINALIZE RETURN oon
(

T=Termination

Technical note: Parts return filenames are 8 characters plus a 3-character
extension, such as Nxxxxxxx.R$R, where N represents the type of return,
such as A=Annual, "R" signifies a parts return, and the last R=Ready to
Send. When the file has been successfully sent the extension is renamed to
R$S, which prevents the file from being sent again but retains it for future
use.

© Press [Enter] to proceed. The job is placed on the job queue. Press
[Enter] to retum to the Stock Return/Phase Out menu. The return file
will be placed in the appropriate directory for New Holland DCS.

RELEASE 2.1 oe

## CHAPTER X35-5

POST STOCK RETURN

### Introduction

Post Stock Return allows you to:

= Post a stock return after you have returned the parts to the vendor.
Posting adjusts the new on-hand totals in your parts files.

= Print a report which lists the returned parts.

### How To Run

From Menu X35 select option 5 to Post Stock Retum. When prompted,
type in the Vendor Code and Return Number of the Stock Return you wish
to post.

## X35-5 POST STOCK RETURN

### Result

The adjusted inventory will be reflected in ALL current reports and
inquiry screens. A report listing the parts on your stock return is printed.

ABC COMPANY POST STOCK RETURN REPORT 30/01/86 = PAGE ot
wanor, co w ST STEIGER 14.33.59 3850-20,
VENDOR AUTHORIZATION NUMBER 06245 RETURNE STr1
QUICK PART #-~.
DESCRIPTION LOCATION HAND AVAIL.
01-2058 BELT SET
01-2065 PYLTER
01-2228
01-2334
01-2335
01-2336
03-2867
01-3332
01-3685
01-3861
01-4299
01-4222
01-4456
o1-4a72
oi-aast
01-6150
01-6152
01-6153
o1-6154

The report lists the vendor and order return number at the top.


Part # alt ide; tifving Umber,
Description Nef description CH item
in Location Ocation of 10 Your de, ership
On Hang Wantity on hi ur dealership atte,
Teturn,
Avail Quantip Vailable after the Tet
turn Qty ‘uantit. etumeg to ‘endor,
Unit Cosy Cost of £0 your ¢, rship,
Xtendeg Cost Ost of eS the Qantity Teturneg
turn Totals ‘alculates e number Of LINES
TS,


Notes:

RELEASE 24

## CHAPTER X35-6

CREATE STOCK PHASE-OUT

### Introduction

Create Stock Phase-Out allows you to:

= review certain parts of your inventory to locate parts which have not
sold over a specified period of time.

" look at the stock phase-out teport and decide if you want to:
™ correct the phase-out in X357
= cancel the phase-out in X358
= print the phase-out in X359
"post it in X35A (this automatically removes the records of these
phase-out parts from your inventory)

This job differs from the stock return. These parts are parts you won't
return to the manufacturer, but haven't sold and simply aren't worth
stocking or parts which are one time Priority orders.


X35-6 CREATE STOCK PHASE-OUT an

### Creating A Stock Phase-Out

The Entrance Screen looks like this. You furnish the Vendor Code, Class,
a unique Phase-Out number and the sales criteria.

WHOEVER EQUIPMENT CO. CREATE STOCK PHASE-CUT x3560-101,
Division: L

vendor (Or ALL)

Class (Or AbL) sae
Phase-Out number coe ee + PHRSORIE

Parts meeting the following sales criteria:

have been in inventory over 4 months

with sales of less than or equal to i (
during the previous 12° months

will be included on the Suggested Phase-Out report.

Include parts with @ on hand only N
Include Superseded parts... (¥/N)? N

gnter ‘¥' to print in bin location order N
Otherwise, report will print
in sorted part number order

 

UL

RELEASE 2.2 *


X35-6 CREATE STOCK PHASE-oUT

      
    

  
 

 

     

### Abc Company

 

SuscesTED euase-ours Mininum months in inventory; Date 10/01/98 Page 2
wumnior, co x vENcoR AT muvee Sales less than er equal to: Time 15.52.24 xas60-55
PHASEW Months of history: 24

cost Deserizeion Class Phase-Our Lest Location sales ast 12 YTD PYS onhand Dealer Extended

   
 
 
 
 
 
 
 
 
 
 
 
  
   

     
  

 

oy sale Months oty

70% 901 233 ava Pp 2 9700 5k ° t
701 002 239 HEAD x 0706 ©

70% 002 22 BRACKET > arse on ¢

701 001 263 coven e ooo Be o

701 001 270 BUSHING P 4 oe r5n2 4 4
701 901 271 EINK e 1 0700 aR a 1
701 co1 273 ane > 1 Gro ae 0 i
702 001 274 BRACKET P 1 6/00 BR ° Q
201 002 275, BRACKET Pe 2 0/00 aR 9 1
701 00t 30¢ BRACKET > 3 5700 aR 5 1
701 092 306 EXTENsioN P 4 9s84 eR e 4
952 008 co6 BUSHING P 6 4/90 35-06 ° 5
954 001 a03 RIVED P 30 970 rs 05g 30

TOTAL SUGGESTED PRASE-OoT FOR AINIKER 64 Lines 414.90

 

A Suggested Phase-Outs Report will be printed. The fields on the report
are described below,

### Fields & Descriptions

Part Number Identifying part number.

Description Brief description of the part.

Class Classification code of the part.

Phaseout Qty Amount of the part in stock to be phased
out.

Location Bin location of the Part in your dealership,

Sales Total pieces sold,

Last 12 Months Amount sold in the last 12 months.

YTD Year to date sales,

PYS Past year sales,

Onhand qty Amount of part on hand.


X35-6 CREATE STOCK PHASE-OUT

### Error Report

If a part would be on the suggested stock phase-out but has a(n):
= reservation on it

= order or return on it

= no date added to inventory

The parts will list on the Phase-Out Error Report. This is a sample
Phase-Out Error Report.

     
  
 

 
 

WHORVER EQUIPMENT CO. phase-Out Frror Report Minimun sonehs in inventory: @ pace 9/09/38 Page 1
BELLINGHAM WA L Wendor HRD HOWARD ROTO. gales less than or equal tort Time 15.46.14 x3560- SB

    
 
       
 

 

   
    
       
     
  
 

phaset PHASOS96 Months of bistory: 12
part Nunber-------r--* pagerigtion Class PhagerGut [ase ZOcasior Seles Last 12 YTD PYS Onnand Dealer Extended
ay Sale vonehs. oy net Value
5953 w 0706 e -00 190
prs-3ide order, Recusn, oF Phase-Cut exists - cannot be phased- out.
18835 GEAR s 3/98 0D 5 99 -00
pis-3248 ordez, Return, oF Phase-Out exists » canner be phased- cut.
19841 ‘SEAL s esse BB 1 a a 2.24 09

 
 
   
 
 

 

 
 

 

prs-3148 order, Return, oF Phase-Oet exists , canner Be phased- out.
69667 BOLT 8 s 9788 ° we 8 152 2.60
prs-a1de orcer, Return, or Phase-out exists . cannot Be phased US:

  
     
  
    

  

otal Phase-Ouc Errors for HOWARD ROTO. 14 Lines: 115.58
14 Pieces

 

The fields are the same as are on the Suggested Stock Phase-out. After
each part line is a statement of why the part is on the error report, or in
other words cannot be phased-out.

You may correct the error, cancel this phase- out, and then create another
report with this phase-out part on it, or add it to this phase- out in correct
stock phase-out.

## CHAPTER X35-7

CORRECT STOCK PHASE-OUT

### Introduction

Correct Stock Phase-out allows you to:

™ correct a stock phase-out (quantity, add new parts, remove parts.)
create a new phase-out of specific parts.
process orders, returns, and phase-outs.

 
   
 
 
 

### Warning!

  

Do NOT change quantities of a phase-out part here. The purpose of
this job is to eliminate parts regardless of on hand quantities.


X35-7 CORRECT STOCK PHASE-OUT

 

### Correcting Phase-Outs

From Menu X35 select option 7 to Correct Stock Phase-Out. Type in your
desired Vendor code, Phase-out Number and either 'C' to change an
existing Stock Phase-Out or 'N' to create a manual Stock Phase-Out.

See Figure X3412-201 for the Stock Phase-Out Correction screen.

ABC COMPANY STOCK PHASE-OUT CORRECTION SCREEN 3570-101
Division: © BHG 123456 Lines
Current mode: SCROLL AND DELETE LINES Extended amt...

Quick
cede Quantity D = Delete

Press CHD 1 to end job: CMD 2 to scroll and delete lines; CMD 3 to add lines
CMD 4 to randomly delete lines

 

RELEASE 2.1 LO


X35-7 CORRECT STOCK PHASE-OUT

 

### Fields & Descriptions

Current Mode Notes your method of correcting, listed in
OPTIONS and at the bottom of the screen.

Lines Number of lines on the phase-out,
automatically updated.

Extended Amount Total cost of the phase- out, automatically
updated.

Part Number/ Part identifying number or manufacturer

Quick Code code used to access the part.

Quantity Quantity of the part in stock.

D= Delete To delete the part from the phase-out, use

CMD 2 or 4 and type a D in this field.

Press ENTER.


X35-7 CORRECT STOCK PHASE-OUT

 

### Options

 

Ci To scroll and delete lines, press CMD 2.
15 lines will appear on the screen in sort sequence. Type a D beside
part numbers to be deleted from the phase-out. To see more parts,
scroll using the Roll keys.

Press ENTER to display the next 14 lines.
An error will be displayed if a negative number is entered.

O To add lines to the phase-out, press CMD 3.

15 blank lines will become available for additions. Type in parts and
quantities. Press ENTER to add them to the phase-out.

Note:

If a part number does not exist in your inventory and you try to add it,
you will see a message at the bottom of the screen saying the new part
number has an invalid format.

 

 

 

 

 

To randomly delete lines, press CMD 4.

15 lines are available on the screen at one time to delete. Type D next
to the part to delete from the phase-out. Press ENTER. To verify
changes, use CMD 2 to scroll and edit.

0 Press CMD 1 to end the job.
C.

## CHAPTER X35-8

CANCEL STOCK PHASE-OUT

### Introduction

Cancel Stock Phase-out allows you to:
= cancel one or more stock phase-out numbers.

Note:

DO NOT CANCEL A PHASE-OUT WHICH IS BEING CREATED.
Check the user board to be sure that all X356___ procedures have
completed.


X35-8 CANCEL STOCK PHASE-OUT

CANCELING PHASE-OUTS

The Entrance Screen looks like this.

Phase-out Number ... BHASO9B6

 

1. Type the vendor code.
2. Type the Phase-out Number.

3. Press Enter. The procedure will be placed on the job queue.

Note:

If you press Cmd1, you will end this job without canceling the stock
phase-out. You must complete the process by pressing ENTER.

 

RESULT: If you press ENTER, the stock phase- out will be canceled.
Phase-out information for all parts on this stock phase-out number will be
deleted. Type another phase-out number to be canceled and repeat the
process, or press Cmd1 to cancel the job and return to the Stock
Return/Phase Out Menu.

## CHAPTER X35-9

PRINT/FINALIZE PHASE-OUT

### Introduction

Print/Finalize Phase-Out allows you to:

® print and finalize a stock phase-out.

### Printing A Stock Phase-Out

The Entrance Screen looks like this. You furnish the vendor code and
phase-out number.

Vendor code ‘BRD

Phase-out number PHASO986

 

 

Type the Vendor code.

 

 

 

 

Type the Phase-out number.

 

O Press Enter. The procedure will be placed on the job queue.


Notes:

## CHAPTER X35-10

POST STOCK PHASE-OUT

### Introduction

Post Stock Phase-out allows you to:

® post a stock phase-out which has been finalized. Phase-outs are
finalized in Print Final Phase-Out, X35-9.

= removes the records of the parts identified on the stock phase-out
report.

### Posting Stock Phase-Outs

The Entrance Screen looks like this. You furnish the vendor code and
phase-out number.

Vendor code BRD

Phase-out number PHASOS6

 

O Type the Vendor code.
O Type the Phase-out number.

O Press Enter. The procedure will be placed on the job queue.


Notes:
f
Qe

## CHAPTER X36-1

PARTS INVENTORY PAD

### Introduction

The Parts Inventory Pad gives a listing of your inventory by part number.
One division (or all), one vendor (or all) and one class (or all) may be
selected, and up to 6 core codes can be excluded. Dealer list, suggested
list, internal price, dealer net, or average cost may also be included in the
Pad. If multiple divisions are selected, a consolidated report that combines
the parts lists from selected divisions may be printed. If all vendors are
printed, each vendor's information will print separately in order of vendor
code. If a complete pad is not needed, a summary only may be requested.
A segmentation error report can also be printed which includes linkage
errors, as well. The Parts Inventory Pad prints all new parts, reman
(remanufactured ) parts and associated core information. To print core
parts only, see CHAPTER X36-20, CORE INVENTORY PAD.

Management Notes

The Parts Inventory Pad gives a listing of inventory by part number. One
of its uses is to provide inventory information when the system is down.
You can compare the parts pad summary before and after a price tape
update to get figures for adjustments to the general ledger.


[| X36-1 PARTS INVENTORY PAD —

### How To Run

From the Parts Reports Menu (X3-6), select option 1, Parts Inventory Pad.
The selection screen is illustrated below:

A&R EQUIPMENT SALES PARTS INVENTORY PAD xa610-001
SELEC?
Vendor (oz ALL)
Class (or ALL)

Core Codes to Exclude

Dealer List Price
Suggested List Price..
Internal Price

Dealer Net...

Average Cost.
Date Last Changed.

Gmdi-Cancel Cnd2-Select Divisions Enter-Continue

 

The Average Cost prompt appears if the Average Costing Enhancement
(X6332-7)OPT is on. If Average Cost is not installed, the Date Changed is
shown on the part line. If both Average Cost and Date Changed are
selected, a second line is printed for each part on the report. This
eliminates having a second line added for each part automatically.

## X36-1 PARTS INVENTORY PAD

 

 

 

When you have completed your selections, press [Enter].

 

D Select which prices you want printed in the Pad by placing a "Y" at the
end of the appropriate lines.

Q To include multiple divisions in the report, press [Cmd2]. The Select
Divisions Screen appears.

O When you are done, press [Enter]. The Report Type Screen appears.

SELECT DIVISIONS SCREEN

A&R EQUIPMENT SALES PARTS INVENTORY PAD x3610-002

Select Divisions

Listed below are all valid divisions. Place an 'X' next to the
Divisions you wish to include in the Parts Pad

Press Enter to retain selections before returning with Cmd3

x AGR EQUIPMENT SALES
DEALER SALES & SERVICE, LTD
ABC COMPANY
ASC COMPANY
MOTORCYCLE CITY
‘THERMOKING

Cmdi-Cancel Cmd3-Previous Screen Cmd-12 Select ALL


[ «| X36-1 PARTS INVENTORY PAD _

O Puta character besides all the divisions you want to include in the
report. Alternately, press [Cmd12] to include all the divisions in the
Teport.

O Press [Cmd3} when finished.

REPORT TYPE SCREEN

A & R EQUIPMENT SALES %3620-003

REPORT TYPE (

Print Detai
Consolidate

Print Summary.

Print on

Number of Copies

Cmdi-cancel Cmd3-Previous Screen ENTER-Continue

 

O Parts Pad Summary and Parts Pad Detail are actually two separate
reports. Decide which reports you want generated and select the

RELEASE 2.2 LO


X36-1 PARTS INVENTORY PAD [=]

appropriate fields.

Q A consolidated report will combine parts from all selected divisions.

An unconsolidated report will have separate records for identical parts
from different.divisions. If you want a consolidated report, enter a "Y"
in the "Consolidate Divs" field. There is no consolidated summary
report.

O Press [Enter]. The following screen appears.

NW EQUIPMENT SALES TIME DELAY 0008-201
Parts Inventory Pad

Time to start job

Cmdl-Cancel  Cmd9-No Delay

Enter the time that the job will be started as HHMM. Press [Cmd9] to start
the job immediately.


X36-1 PARTS INVENTORY PAD ws

A sample summary report is shown below.

Parts Inventory Pad Dace 9/29/98 age 1
BRIGGS- STRATTON 3s Time 20.42.36 3610-20

Pestor sug Dealer pate dete «= Sales
Pare mumer Description on tand Rerv List List fnternal Net cls wet = P9596 cE ky
zis PrN a so 5542 000042 P 22/97
26632 vine has 1.2290 aouooso B 32/97
26975 sean 285 2.38 A.t2 oooo17a » 12/97

27660 casxer 19516849 ont0049 » 12/97
2780 exsxer Leo 199,67 ans0006 » 12/99
27803 casxer 4540136 d0030 12/87
27826 casker “214030 c000030 » 12/97
2os6i conpensen voc 2.70 2192 so0nae2 P 12/97
1760 ey 14542130 0000000 22/97
e506 wR 6.05 $804.22 ogoue2 P 12/97
65704 PLUNGER 15 es #4 s00006a P 22/97
esrze oar Bas 410s 179 0000079 x 12/97
em Rove 192 680-60 sa00060 F 12/97

66768 ros SS ee

srces BREATHER hiss 16s 1124 0900124 P 33/07
65768 sea Luo 415 56 con00es P 12/97 {
384s puna “4540630 000090 F 1/97 \

e272 one 1194130175 0000075 p 12/97

P 12/97

P1237

 

69982 cae 2 6.28 7.00 9000555

91262 Lock? 48 40 -30 es00030
Com: suBs To 261408

s018 screw 2 4 +26 0000026 P 12/57
Cem: suas 70 93705

ane902 ENGINE

a 9036350 ® 32/97

190702 ENCINE a 0022230 2 12/97

220865 WASHER 2 : -37 0000037 p 12/97

221794 DEFLECTOR 2 0ng0026 P 12/97
Com: suas 70 399755,

222263 Leck 6 35 : 6990027 P 12/57

azar? DEFLECTOR 1 5 : osgg072 P 12/97
com: suas TO 393758

230896 ean 4 : - 50036 P 12/97

 

RELEASE 2.2 C


ASC COMPARY Parts Inventory Pad Date 9/30/97 Page}
BELLINGHAM, WA Vendor /Class Sunnary rime 9.55.36 3620-38
Sales Turn Sales
Vender Class Dealer Net Internal ugg List Dealer List YTD Rate Prev yr
as P  BRIGGS-STRATTON 851.95 852.38 1132.28 1.285.99 45.00) 4.30
OBSOLETE REFERE 2.37 2.37 3.18 3.45 06-09 -00
BRIGGS-STRATTON * Totals * 84.32 99¢.75 1,334.40 1,208. 4d 48.30 4.30

CAS POULT, CASE 1,440,97 1,260.97 1,487.12 1,603.26 00.90 208.27
ot. CASE + torals + 2,240.97 1,240.97 2487.22 1,603.26 00.00 304.2
pa LUTZ ALLIS 14.68 14.68 20.34 22.39 00-89 -00
P DEFAULT 20,690.97 7,073.45 29,498.40 32,487.58 3,743.72 1,447.5
630701, +00 eo 25 00 09.00 +00

pEUTZ ALLIS + Torats + 20,705.65 7,086.14 28,516.78 32,479.92 3,763.72 116,407.99 :
or P DIXON 2,306.54 1,104.54 1,477.89 1.624,0% eo1.71 42 766.8

 

 

### Segmentation Error Report

This report prints out segmentation and linkage errors. A sample of the
report is illustrated below.

AER EQUIPMENT SALES Parts Inventory Pad Date 10/15/97 Page 5)
LYNDEN, WA Sogmontation Error Report ‘Time 27.06.95 XQ610-18

DIV vendor Part Number

73153

74248
74295
7608
aan,

 


[ «| X36-1 PARTS INVENTORY PAD wenn
‘

TECHNICAL NOTES

Files Used

IAM
IBM
IVT
MAI
IGAIC (van code)
IGAIF (van code)
IGMIC (van code)

Field Mapping/Catculations

Detail

Dealer List Base 4 Price

Sugg List Base 3 Price

Internal Base 2 Price

Dealer Net Base 1| Price

PJ Per Job pieces required

cT Part Category

PKG Package Qty

Order Total Pieces on order

Average Average Cost = [(A*B) + (C*D)] / (B+D)
A = Current Average Cost
B = Current On Hand Qty
C = New Receipt Cost per unit
D = New Receipt Qty

RELEASE 2.2 Lo


X36-1 PARTS INVENTORY PAD [e]

Summary

Lines Number of part records in inventory
Sales YTD Pieces sold YTD * Dealer List
Tum Rate YTD Sales / Total Dealer List
Dealer List Base 4 Price * Qty on Hand

Sugg. List Base 3 Price * Qty on Hand
Internal Base 2 Price * Qty on Hand

Dealer Net —_ Base 1 Price * Qty on Hand

Data Timing

None

Data Included/Excluded

One division (or all), one vendor (or all) and one class (or all) may be
selected, and up to 6 core codes can be excluded. Dealer list, suggested
list, internal price, dealer net, or average cost may also be included in the
Pad. If multiple divisions are selected, a consolidated report that combines
the parts lists from selected divisions may be printed. The Parts Inventory
Pad prints all parts, including core parts that are not specifically excluded.
If all vendors are printed, each vendor's information will print separately
in order of vendor code. If a complete pad is not needed, a summary only
may be requested.

## X36-1 PARTS INVENTORY PAD C

OPTs/Additional Products

OPTs

Average Costing Will produce an Average cost column on the
detail report.

Additional Products

Van Code If installed, the pad can be run by Van.

Required Procedures None

Data Sorts

Vendor/Class/Division/Van

IAM is read sequentially for each part number. If the part is in the users (
division, then the number is expanded and put in sort order form. The

sortable number, the compressed number with vendor and division, and

the expanded number are all written to SORTIAM. The procedure X36101

takes this file and sorts it and runs program X36102 which prints the pad.

RELEASE 2.2 Lo

## CHAPTER X36-2

PARTS MANAGEMENT REPORT

### Introduction

Of all reports available in Parts and Point of Sale the Parts Management
Report is definitely the heavyweight. It is to the parts department what the
financial statement is to the accounting department.

The Parts Management Report can be run for any vendor and any class at
any time. Information is available for up to 36 months. Parts End of Year
purges records over 24 months.

The Parts Management Report includes only transactions involving parts
sold with sales code format "P" (no miscellaneous part sales from formats
"D," "M," or "S." The Parts Management Report:

Shows gross sales by vendor
Reports stock ordering information
Calculates turn ratios

Presents movement indicators

Plus much, much more

Its accuracy is compromised by:

Missing costs

Negative on hand quantities

Unreceived stock orders

Failure to record lost sales (at Point of Sale or in Parts
Posting & Maintenance)

. Selling inventoried parts (parts with assigned part numbers)
with miscellaneous sales codes


[2] X36-2 PARTS MANAGEMENT REPORT

Page 1
TRANSACTION SUMMARY

Historical information

= Sales and Returns

= Receipts

= Inventory Adjustments

Page 2
INVENTORY ANALYSIS

Historical information

= Orders

= Lost Sales

= Tum Rate

= Performance Indicators

Current information
= Sales Movement
= Restocking Policies

In this chapter you will find a sample Parts Management Report and
details on each section of the report. Definitions of fields and terms will be
provided. You will learn the sources of the information used to generate
the report and how information is updated. You will be given all formulas
used for ratios and percentages. Further, you will be given some hints
about how to use the report to judge the performance of your parts

department.

### Preparation

No special preparation is necessary; however, the system will check to
make sure that Parts End of Month is not running before it begins
calculations. Historical information on the Parts Management Report is
captured when transactions occur and is not affected by price changes.
Current information, Sales Movement and Restocking Policies, reflects
cv


X36-2 PARTS MANAGEMENT REPORT [2]

what is in the parts records when you run the report; therefore, the figures
in those 2 sections will be different after repricing.

Current information, which would have been captured by End of Day, is
included when the Parts Management Report is run. It is not necessary to
run Parts End of Day before the Parts Management Report.

The Parts Management Report can be run for any vendor and any class at

any time. Information is available for up to 36 months. Parts End of Year
purges records over 24 months.

### How To Run

From the Parts Report Menu (X3-6), select option 2, Parts Management
Report.

 

Calculations

First, the system does all calculations for all vendors and all classes, which
takes about as long as it takes for your parts inventory pad to start printing.
After the calculations are complete, you will receive a message at your
workstation.

Calculations are stored in a temporary files uT.PMRC and uT.PMRT (u =
User ID), which will be deleted when you take the option to Backup Data
Files (X6-1).

If Backup Data Files (X6-1) has not been cun since the inventory


[+] X36-2 PARTS MANAGEMENT REPORT c

information for the Parts Management Report was calculated, the
calculations files (uT.PMRC and uT.PMRT) will still be on the disk. You
will see this message:

Inventory information was calculated on 09/08 at 09:26

Do you wish to recalculate (¥/N)?

 

Later reports will not include transactions which have occurred since the
calculations file was created. If you want the most current transactions on
the report, type YES to recalculate the inventory information.

If the calculation files are not on disk, you will see this message: (

Inventory information has not been calculated.

Press ENTER to calculate inventory.

 

Press Enter. The following screen will display:


RELEASE 2.2 XQ

## X36-2 PARTS MANAGEMENT REPORT

PMR Calculations have been started.

A message will be sent to this workstation to notify you when the calculations
are complete.

After calculations have completed, restart the PMR option
to print the report.

Press ENTER to return to the menu.

 

Press ENTER. You will return to the menu.

After the calculations are complete, you will receive the following
message:

   

Message Display

 

From-U WSID-WL Date- 11/22/8 Time- 15:35:12
PMR calculations have completed. Restart PMR option to continue.

Press ENTER to continue

Press Enter to return to the menu.

Now that PMR calculations have been made, you may rerun the
application to print the report.


[«] X36-2 PARTS MANAGEMENT REPORT

Report

You will see the following screen:

Inventory information was calculated on 09/08 at 09:26

 

This screen indicates that the calculation files exist. If you wish to print
reports based on these calculations, type N. Press Enter.

Dates

Furnish the beginning and ending dates. Request a single month by using
the same beginning and ending month/year as illustrated below:

Beginning date (t/vy)
Ending date (MM/yy)

 

You can request as many different reports as you need from the
information calculated for the time period you specify.

RELEASE 2.2 L


 

Report Options

After the calculations have been done, you will be prompted for the level
of detail you want on the report. A consolidated report summarizes the
most information (all divisions, all vendors, all classes) and furnishes the
least amount of detail. The class code reports furnish the most detailed,
specific information.

Select Report Option: 4 1=Consolidated Report
visional Reports
3=Vendor Code Reports
4=Class Code Reports

  

Divisional Reports

If you want a summary report of parts activity for one division, you'll
receive the following prompt:

Division Code (or ALL)

 

Type the first letter of the division. This will print a summary for the
B1000 division. If you want a separate summary report for each division,
type ALL. If you have 4 divisions, you will receive 4 reports (8 pages),
whereas the consolidated report option produces 1 report for 4 divisions.

Press [Enter] when you have made your selection.


Options:

O Enter your request for another divisional report.

O Press {Cmd2] to print your selections.

O Press [Cmd1] to end the job. Remember that the calculations files will
remain on the disk until backup. If you want additional reports for the
same time period, you can request them during the day.

 

Vendor Code Reports

If you want a summary of parts activity at the vendor level, you'll receive
the following prompt:

Division Code {or ALL)

Vendor Code (cr ALL)

 

This will print a report for the Bolen vendor in division B1000. All classes
will be summarized on | report (2 pages).

Press [Enter] when you have made your selection.

Options:

O Enter your request for another vendor code report.

O Press [Cmd2] to print your selections.

Press [Cmd1!] to end the job. Remember that the calculations files will
remain on the disk until backup. If you want additional reports for the
same time period, you can request them during the day.

 

 

 

 
CO


X36-2 PARTS MANAGEMENT REPORT Ls]

Class Code Reports

To print a report with the most detail, choose the class level. You'll receive
the following prompt:

Division Code {or ALL) . .

Vendor Code (or ALL) :

Class Code {or ALL)
THxz

 

You'll recognize this selection screen from Create Suggested Stock Order
(X341-1). You can type 3 classes on the first line and 52 classes on the
second line. You can put commas or blanks between the class codes, but
they are not required. The system will ignore invalid class codes.

The request illustrated above would print 7 reports of parts in classes A, F,
S, T, W, X, and Z for each vendor in division B1000. If there are 10
vendors, there would be 70 class reports (140 pages).

 

 

Press [Enter] when you have made your selection.

Options:

O Enter your request for another report at this level.

O Press [{Cmd2] to print your selections.

Press [Cmd1] to end the job. Remember that the calculations files will
remain on the disk until backup. If you want additional reports for the
same time period, you can request them during the day.

 

 

 

 


An example of the Transaction Summary follows:

LEE‘S TRACTOR SALES, inc. PARTS MANAGEMENT REPORT Dave 12/12/97

Transaction Summacy ime 10:33:12
Division - For Period: 06/97 ce 09/97 Class - ane

cnanges . OF Cost
Transaction Type To ety Ext. Cost, Margin argin to Total
Beginning Invencory a 1696.72 109.0
SALES

counter - 49.35- 31.6
service - 36.27-
Taternal 5 90
Warranty a -08

Total sales

RETURNS
counter
Service
Internal

‘Total Revurns
RECEIPTS
Priority
stock
other

Total Receipts
INVENTORY ADJUSTHEITS
Returns te Supplier
‘Transfers In
Teansfers out
Roprice pares
Automatic Price Update
Part Adjustments
Phase outs
Initial Parts Data Entry
Spaciat

Tocal Adsustments
TOTAL CHANGES TO INVENTORY

ENDING INVENTORY 1627.25 2697.33 1970.08,

 


An example of the Inventory Analysis follows:

    

LSE'S TRACTOR SALES, INC. PARTS MANAGEHENT REPORT Date 12/12/97
inventory Analysis Time 10:32:37
Division -  b For Feriod: 06/97 to 93/97 Vendor - ALL Class - ALL

 

 

 

 

Pet. & Of Cost
Transaction Type Dealer Net Dealer List Gross wargin Margin to Total
ORDERS
Stock - Created as 43865.68 73788.14 29892.45 40.5 318.4
Stock - Adjusted by 30096.13- 51464. t4- 91954.27- 258.8

 

 

Net Stock Orders 13775.55 27294.06 8518.45
Priority - Creaced as 39 +00 +90
Priority - Adjusted by 26 08 -00

 

Net Priority orders

 

Total orders 395 32775.55 22294.00 518.45 38.2
LOST SALES 0 99 os -00 0
“INVENTORY TURN RATE PERPORMANCE INDICATORS.
(Based on 04 month period)

 

Year Te pate For Period

Cost of Sates 152465.29 CALLS - Total 14770 3805

 

Ending Inventory 119582..68 PIECES - Firat Time 59751 25150
PIECES = Acer Ordering 3

Total 25253

### “Sales Movement Movement

 

Monzhs since Lines Pet. Dealer Ket . Months on Lines et. Dealer ner
last sale system

+90 ro . -09
189858.78 to : 7448.29
0010, 89 to : 2829.49
18578. 72 : 3761.85
9861.25 . 5797.20,

0652.71

RESTOCKING POLICY

 

Service Lines pot. —bealer Net.
Auromacic 19299 99 427427.99

Combined z 11.08
manta? a 1058.10


[2] X36-2 PARTS MANAGEMENT REPORT

### Fields & Descriptions

## of Transactions

% of Cost to Total

Automatic
Beginning Inventory
Calls - Total
Combined

Cost

Dealer List

Dealer Net

This column reflects an absolute value
(neither positive or negative) since both
positive and negative #'s of transactions can
be totaled in this column. For example, if
there are 25 negative and 10 positive
transactions this column will display 35
transactions.

Cost___= Percent of Cost to Total
Total Sales
Lines ordered by DIS system under the
Automatic Ordering Method. Order code =
A.
Same as previous month's ending inventory.
Total number of calls. A request for 5 bolts
is recorded as one call; therefore, calls
correspond to lines, not pieces. Every line on
a closed, non-cloned document counts as
one call.
Lines ordered by DIS system under the
Combined Ordering Method. Order code =
Cc.
Part cost from Parts Posting & Maintenance
Information screen when the sales document
was closed.
Total of extended Dealer List from the Parts
Posting & Maintenance Information screen
at the time of the transaction.
Historical: Total of extended Dealer Net
from the Parts Posting & Maintenance
Information screen at the time of the


Ending Inventory

Gross Margin
Lines
Manual

Pct (Performance
Indicators)

Pct Margin

Pct (Restocking &
Sales Movement)
Extemded Net
Lines

Pieces

>

X36-2 PARTS MANAGEMENT REPORT [|

transaction.

Current (Sales Movement & Restocking):
Extended Dealer Net (cost) of parts in each
category. Prices are taken from current part
record which reflect the most recent reprice
or price update. The total dollars in this
column is the same as the total dollars of
ON HAND inventory on a parts pad
summary (X36-1) run at the same time.
Same as ON HAND inventory on a parts
pad summary (X36-1) (less any parts with
negative on-hand quantities).

Dealer List minus Dealer Net (dollars).
Lines are different part numbers. One part
number is one line. You may have several
pieces (individual parts) of that line on hand.
Lines ordered Manually only. Order code =
M.

## pieces - Ist time = % filled 1st time

Total # of pieces. Priority codes of blank,
"D," "Q," and "R" are included. Priority
codes of "d," "gq," "P," "p,"""S," and "s" are
not included in this total.

## pieces - after order = % filled after order

Total # of pieces with priority code="a."
Gross Margin = Percent Margin

Seliing Price

Total $ in category = Percent $ in category

Total $ in inventory

## pieces in category= % pieces in

## pieces in inventory category

One piece is one part. ("P" format line on a


Pieces - First Time

Pieces - After Ordering

Selling Price

co

Point of Sale document).

The number of pieces sold with priority
codes “blank,” "D," "Q," and "R." These
parts were not ordered.

The number of pieces ordered and sold after
receipt on any type of document. Pieces sold
with "P" order code, which progressed to "p"
then to "a."

Selling price from closed Point of Sale
document.

### Page 1 - Transaction Summary

The types of transactions are presented below in the same order as they
appear on the report. For more information on document types, see
Document Classification Maintenance, X52-2. For more information on
line types, see Point of Sale Invoicing Reference section, X5-1R.

SALES

Transaction:

Counter

Service

Source:

Parts Posting & Maintenance when a blank
transaction code is used.

Closed Point of Sale documents, type “S"
(Sales Order).

Closed Point of Sale documents, type "W"
(Work Order), line type blank (neither
Internal nor Warranty).

RELEASE 2.2 Ne


X36-2 PARTS MANAGEMENT REPORT [=]

Internal Closed Point of Sale documents, type "W"
(Work Order), line type “I” (Internal).
Warranty Closed Point of Sale documents, type "W"

(Work Order), line type "W" (Warranty),
both sales and returns (+ or - quantities).
Counter Returns Parts Posting & Maintenance when a "-"
(minus) transaction code is used.
Closed Point of Sale Documents when:
= document type is "S" (Sales order)
= line type is blank (not warranty or
= priority code is not "L" (lost sale)
= a negative quantity is entered
® transfer field is blank
Service Returns Closed Point of Sale Documents when:
= document type is "W" (Work Order)
= line type is blank (not warranty or
internal)
= priority code is not "L" (lost sale)
"= a negative quantity is entered
" transfer field is blank
Internal Returns Closed Point of Sale Documents when:
= document type "W" (Work Order)
= line type is "I" (Internal)
® priority code is not “L” (lost sale)
" a negative quantity is entered
= transfer field is blank


RECEIPTS
Transaction: Source:
Priority Receive Orders (X342-2) when a priority
order is received.
Stock Receive Orders (X342-2) when a stock order
is received.
Other Parts Posting & Maintenance when an "R"
transaction code is used.
Closed Point of Sale documents with
quantity less than zero and any character in
the "Transfer" field.
{
INVENTORY ADJUSTMENTS
Transaction Source:
Retums to Supplier Post Stock Return (X35-5).
Transfers In Parts Posting & Maintenance when a "T"

Transfers Out

Reprice Parts
Automatic Price
Update

transaction code is used.

Closed Point of Sale documents with
quantity greater than zero and any character
in the "Transfer" field.

Reprice Parts (X37-1).

Case Communications (X7-1) and

Price Tape Update (X37-2).

### X36-2 Parts Management Report [7]

   
  
    
   
  
  
  
   
   
    
   
  
  

Part Adjustments Parts Posting & Maintenance (X3-2).
Information screen: Dealer Net, Dealer List,
or class is changed.

Transaction screen:

Code: +/-
- (Delete record) -
A {Add record) +

c (Change Vendor/Part#) + &-

M (Minus to inventory) -

P (Plus to inventory) +
A high number of minus adjustments should be investigated. These parts
have not left by way of the cash register.

Parts Inventory Adjustment (X33-1).

Correct Order Before Receiving (X342-1):
Add lines, add new parts, changes to
quantity and prices.

Correct Stock Return (X35-2): Add lines,
add new parts, changes to quantity and
prices.

Reconfigure Parts (X38-3) when class code
is changed or parts are moved by demand.
Added to new class, subtracted from old
class.
Phase-outs Post Phase-out (X35-10)
Part numbers with zero on hand at phase-out
are included in the total of lines because the
part numbers are deleted.

  
 

Initial Parts


X36-2 PARTS MANAGEMENT REPORT C .

Data Entry Initial Parts Data Entry (X68-5).
Special DISMAINTs and custom code.

PAGE 2 - INVENTORY ANALYSIS

Inventory Analysis has these subsections:

C1 ORDERS

1 LOST SALES

0 INVENTORY TURN RATE

C1 PERFORMANCE INDICATORS (
SALES MOVEMENT

### Co Restocking Policy

 

 

 

 

Each subsection will be discussed and interpreted separately.

1) ORDERS
Transaction: Source:
Stock - Created as Create Suggested Stock Order (X341-1).
Stock - Adjusted by Correct Stock Order or Create Manual Order

(X341-2). A manual stock order is
considered to have been created with zero
lines and then adjusted, which means that all
lines on manual orders are counted as
adjustments.

Priority Orders (X5-3). Parts from closed

{

RELEASE 2.2 NS


X36-2 PARTS MANAGEMENT REPORT [°]

Point of Sale documents which were
assigned a priority code of "S" are placed on
a stock order, POSd (d = division code). Just
like a manual stock order, POSd is
considered to have been created with zero
lines and then adjusted.

Priority - Created as Priority Orders (X5-3). Priority orders from
Point of Sale documents are created when
you take the option X5-3. Orders which are
waiting to be processed will not be included
on this report.

Priority - Adjusted by Priority Orders (X5-3).

2) LOST

Parts Posting & Maintenance when an "L"
transaction code is used.

Closed Point of Sale documents with an “L"
priority code.


[| X36-2 PARTS MANAGEMENT REPORT co

### 3) Inventory Turn Rate

One part stocked and sold = one turn. A turn rate of 2-3 is desirable.

The formula used to calculate Inventory Turn Rate is:

Total Dealer Net for Past n Months Sales 12
x = Turns

 

Total Dealer Net of Ending Inventory n

‘The turn rate on the PMR report will always be based on an annualized

figure. An actual turn rate can be calculated by asking for a PMR report

for 12 months. If you have not been on the Parts Management Report

system (V7L4 or higher) for 12 months, and ask for a PMR report for one

year, an annualized figure for turn rate will also be given. This rate is (
based on the number of months of actual history within the system. The

number of months used for the calculation is always shown within the box.

If the turn rate is too high, the dealer may be "cherry picking" the market,
carrying only high turnover parts, or relying too much on suppliers by
making too many small orders. A very high tum rate could also indicate
that the inventory is undervalued.

If the turn rate seems too low, perhaps too many product lines are being

carried or there are too many slow turn items. Order Tesponse time may be
slow, or it may be time for a phase-out.

RELEASE 2.2 L


X36-2 PARTS MANAGEMENT REPORT [=]

### 4) Performance Indicators

Performance indicators will never be precise. They are what they are:
Indicators. The only way to have 100% fill the first time to have every part
the manufacturer has ever made in your inventory, and to have enough on
hand to supply every customer every time. Of course, no business would
attempt to do this-- think of the disastrous effect it would have on the turn
rate, not to mention the bottom line!

One way to understand this section is to think of one customer who wants
to buy 2 wheelbarrows, a ladder, and ten hammers. The document number
is CTO014 #*. You have the ladder and 6 of the hammers. When CT00145
## is closed, there are 3 lines, which are counted as 3 calls (one for the

wheelbarrows, one for the ladder, and one for the hammers). You were
able to furnish 7 pieces the first time (priority code is blank).

Assuming that the date is January 29 and nothing else has happened all
year, the deal would look like this in the Performance Indicators:

Year To Date Pet For Month Pct
CALLS - Total 3 3
PIECES - First Time 7 100.0 7 100.0

PIECES - After Ordering

Total 7 100.0 7 100.0

The wheelbarrows and 4 hammers must be ordered. They go on a clone
document, CTO0145A#*. When the hammers come in, the customer picks
them up, and the first clone document is closed. The system recognizes
that the document is a clone because of the "A", and counts 4 pieces filled
after ordering. Calls are not increased when clone documents are closed.


[2| X36-2 PARTS MANAGEMENT REPORT co

Assuming that the date is January 31 and nothing else has happened, the
deal would look like this in the Performance Indicators:

Year To Date Pet For Month Pct
CALLS - Total 3 3
PIECES - First Time 7 63.6 7 63.6
PIECES - After Ordering 4 36.4 4 36.4
Total 11 100.0 11 100.0

Another clone document, CT00145B#*, is created. The wheelbarrows are
the only things on it. When CT00145B#* is closed, 2 more pieces are
added to the Pieces - After Ordering total.

By now it is February 1. The performance indicators look like this:

Year To Date Pet For Month Pet
CALLS - Total 3 QO
PIECES - First Time 7 53.8 0 -0
PIECES - After Ordering 6 46.2 2 100.0
Total 13 100.0 2 100.0

{
RELEASE 2.2 NW


X36-2 PARTS MANAGEMENT REPORT [=]

### 5) Sales Movement

Sales Movement is divided into 6 time periods. To understand which
months are in each category, picture a calendar with a maximum of 36
months. In this example, it is currently March, 1997.

Purged at Parts End of Year 12/31/97

JAN : FEB: MAR : APR: MAY : JUN: JUL; AUG : SEP : OCT : NOV | DEC:

 

84:94 : 94 : 94 : 94 :94 : 94 : 94 : 94 : 94 : 94 94

 

[ 27
Over 24 13 - 24

 

sJAN : FEB | MAR : APR : MAY : JUN: JUL : AUG ; SEP : OCT : NOV: DEC :
79500: 95 95 2:95 : 95 : 95 : 95 :95 : 95 : 95 :95 : 95 :

 

26 25 24 23 22 21 20 19 18 17 16 15

10 - 22 | 7-9 4-6 |

 

‘JAN : FEB | MAR : APR: MAY | JUN : JUL ; AUG | SEP : OCT : Nov | DEC :
196 3 96 96 : 96 : 96 96 : 96 : 96 96 : 96 : 96 96

 

 

 

 

wqa3 a2) ato | 8 7 6 5 4 [3
: FEB : MAR :
2 37: 97

2 tO

Interpretation of Sales Movement

What you want to look for are relationships. For dealerships which carry
seasonal parts it is reasonable to expect a fairly high percentage of the
inventory lines and dollars to be concentrated in the 4 to 6 months
category.


Categories are determined by Last Sale Date. When data is entered at DIS
the Last Sale Date is blank; therefore, most inventory will be reported in
NO MOVEMENT, 0 - 3 months on system. This will gradually correct
itself.

If you have been on the DIS system for a year or more, and there is high
percentage of lines in the NO MOVEMENT section, then it may be time
for a Phase-out.

### 6) Restocking Policy

The figures in this category represent what is currently in your parts files.
This is the only report which gives you this summary.

Look for relationships. If a high percentage of the parts are ordered
automatically, and if this represents a high percentage of total inventory
dollars, then the conclusion is that the ordering methods selected are
sound. If, however, a high percentage of inventory lines and dollars have
been ordered manually, it is time to re-evaluate the ordering policy. The
goal is to have the system do as much of the work as possible.


X36-2 PARTS MANAGEMENT REPORT [=]

TECHNICAL NOTES

Files Used

PMRIP
ITSIF
OTLIF
ISFIF
JAMIP
IBMIC
ISFUC
IVTIF
MASTER
PMRUC

Field Mapping/Caiculations

Transaction Summary

Gross Margin Dealer List - Dealer Net (dollars)

Pct Margin Gross Margin / Selling Price

% of Cost to Total Cost / Total Sales

Inventory Analysis

Calls Total Total number of calls. A request for 5 bolts is
recorded as one call.

Gross Margin Dealer List - Dealer Net (dollars)

Pct Margin Gross Margin / Selling Price

% of Cost to Total Cost / Total Sales

Turn Rate (Total Dealer Net for Past "N" Months Sales X 12) /

(Total Dealer Net of Ending Inventory X "N")
Pieces First Time The number of pieces sold with priority codes


[=] X36-2 PARTS MANAGEMENT REPORT

"blank," "D," "Q," and "R."

Pieces After Ordering The number of pieces on a closed, clone

Dealer Net
Historical

Current

Pet

Lines

Pieces

document.

Total of extended Dealer Net from the Parts Posting
& Maintenance Information screen at the time of
the transaction.

Sales Movement & Restocking:

Extended Dealer Net (cost) of parts in each
category. Prices are taken from current part record
which reflect the most recent reprice or price
update. The total dollars in this column is the same
as the total dollars of ON HAND inventory on a
parts pad summary (X36-1) run at the same time.
Performance Indicators:

## pieces 1st time / Total # of Pieces = % filled

First time

Restocking & Sales Movement:

Total $ in category / Total $ in Inventory = Percent
$ in Category

Lines are different part numbers. One part

number is one line. You may have several
pieces(individual parts) of that line on hand.

One piece is one part.

First, the system does all calculations for all vendors and all classes, which
takes about as long as it takes for your parts inventory pad to start printing.
After the calculations are complete, you will receive a message at your
workstation. Calculations are stored in a temporary files uT.PMRC and
uT.PMRT (u = User ID), which will be deleted at backup.
ae


X36-2_ PARTS MANAGEMENT REPORT

 

Data Timing

Historical information on the Parts Management Report is captured when
transactions occur and is not affected by price changes. Current
information, Sales Movement and Restocking Policies, reflects what is in
the parts records when you run the report. Current information, which
would have been captured by End of Day, is included when the Parts
Management Report is run.

Data Included/Excluded

After the calculations have been done, you will be prompted for the level
of detail you want on the report. A consolidated report summarizes the
most information (all divisions, all vendors, all classes) and furnishes the
least amount of detail. The class code reports furnish the most detailed,
specific information.

 

OPTs/Additional Products

OPTs - None
Additional Products - None

Required Procedures

No special procedures are necessary; however, the system will check to
make sure that Parts End of Month is not running before it begins
calculations. It is not necessary to run Parts End of Day before the Parts
Management Report. If backup has not been run since the inventory
information for the Parts Management Report was calculated, the
calculations files (uT.PMRC and uT.PMRT) will still be on the disk.


X36-2 PARTS MANAGEMENT REPORT Co

Data Sorts

Consolidated Report, Divisional Report, Vendor Code Report, Class Code
Reports.

!

RELEASE 2.2 Nw

## CHAPTER X36-3

NET OR LIST PRICE MISSING REPORT

### Introduction

The Dealer Net or List Price Missing Report shows those parts lacking
either a net or list price. One vendor (or all) and one class (or all) may be
selected.

This report should be mun so that list prices appear at Point of Sale and
costing is correct. After running this report, make adjustments at Parts
Posting & Maintenance (X3-2) to correct list prices and costing.

PRINTING THE DEALER NET OR LIST PRICE MISSING
REPORT

 

 

 

 

Type the specific vendor code or ALL.

O Type the specific class or ALL.

O Type the number of copies (1 to 9) to be printed.
D To cancel this job, type Y (Yes).

O Press ENTER. The report will be placed on the job queue. Press
ENTER to return to a menu.

Following is an example of the report.

## X36-3 NET OR LIST PRICE MISSING REPORT

ABC COMPANY

weyNo7,
DEALER

co
suse

PART NUMBER

oon
201
oon
902
302

on
on
on,
022
012
on2
22
012
923
023
013

3368,
325M91
339091
5080
2398,
31x
com:
7B:
638x

 

SB:

42x
com:
S/B:
ala
a5
902
776
177%
690c
761
0796
0826
1420
3708
7906
4128
96x,
S3sx

x
DEALER

### Description

SECTION
‘BRAKE KIT
LINE KIT
BALL JOINT
GASKET
BOLT

suns TO 354267x1

Me 3542672
wor

SUBS TO 353437x1

ue 383437xL
BOLT

SUBS TO 35369021

“F 353690x2
WASHER

Suss TO 353442x1

we 3934¢2x1
wor

sues TO 37S122x1

a 375a22xt
WASHER

SUBS TO 383786x1

MP 383 758x2
COLLAR
ourpe
carpe
car
PIN
KEY
SPRING
OWL
TP
GaSKET

GASKET,

PI
BALL

MF -HASSEY-FERGUSON

DEALER NET OR LIST PRICE MISSING

MASSEY-
SALES

SRV BIN LOC
0-7
ane-6
ap
896-1
ec-49
835-7

 

PERGUSON

urs?

“e

LIST INTERNAL © NET CLS LOT

oooon6s
0002075
0000752
poo0aso
oanon1s
900023

de00008

ooooors

voooen2

o9o0019

oo0an08

9000150
90900090
0000079
9000199
9000035,
090049
0020078
oon0289
9000761,
000015,
0090015
0000023
0000064
9900019
0000026


x
x
x
x

MMM RCM

ayaa
area
12788
arse
185
e788

eyea
eee
erea
8784
8780
8764
area
8/84
ered
1785
avee
avae
e784
Bree
ares

9/30/86 3630-2

LS PREV YR YTD CAT PKG PY

ME MASSZY-FERGUSON

 
Cy


 

TECHNICAL NOTES

Files Used

MASTER
IAM
IBM
PXIVT

Field Mapping/Calculations

Dealer List Base 4 Price
Sugg List Base 3 Price

Internal Base 2 Price

Dealer Net Base 1 Price

cT Part Category

PKG Package Qty

PJ Per Job Pieces Required
Data Timing

None

Data Included/Excluded

Records without a Dealer List/Net are the only ones printed.


 

OPTs/Additional Products

OPTs - None

Additional Products - None

Required Procedures

None

Data Sorts

By Part Number

RELEASE 2.1 LO

## CHAPTER X36-4

BIN AVAILABILITY REPORT

### Introduction

The Bin Availability Report list those parts available and in bin location
sequence. One vendor (or all) and one class (or all) may be selected. This
report also includes the date of the last physical count of the part.

If you request that all vendors be printed, each vendor's information will
print separately in order of vendor code.

The Bin Availability report lists parts available and in bin location
sequence. Blank bin locations are printed first.

### How To Run

 

Type the specific vendor code or ALL.

 

0 Type the specific class or ALL.

 

 

 

Type Bin Order C or E.

 

C=Compress Lists in bin location order.
E= Expanded Lists in part number order.

OC Type number of copies (1 to 9) to be printed.

 

 

 

To cancel this job, type Y (Yes).

 

O Press ENTER. The report will be placed on the job queue. Press
ENTER to return to a menu.

Following is an example of the report.

## X36-4 BIN AVAILABILITY REPORT

 

ABC COMPANY BIN AVAILABILITY REPORT sya0/ea 3630-28
waynor, co DIXON pr

### Dealer Scg Dat2 Date Sales

DESCRIPTION ON HAND RSAV BIN LOC LIST LIST INTERNAL NET CLS LOT US PREV YR YIO CAT PKG PY
SWITCH KEY 0000000 F

CoM: REPL ay 4067
S/R: DE 4067
Rep eooacen P
com: suas 70 5245
S/B: BT 5245
‘SPRING eooccoa
COM: REPL BY $132
s/s: Dr 5133

oaooues
com: suas 70 6024
8/3: OF 6028
BELT ooo22¢8 P 12/97 5/988
oD: 50030925 s ORDER TOTAL:
seRocke7 0000583 P 12/97 5/98 4
wey +22 0090022 7 12/97 9/973
SPACER 0020079 P 12/97 5/97
ROD : 000063 > 12/97 8/97
‘BEARING “ o0a0ses 2 12/97 5/98 2 (
ap: 50030925 5 ORDER TOTAL:
BEARING e087 > 2/97 s/97 2
vornt cocosss Pp i2/97 s/98
SHAET cocos22 > 12/97 2/97
ROD 4 oocozs: P 12/97 5/98

0000595 Pp 22/97 8/97

aoo2s02 > 12/97 2/98

coooat1 x 22/97 8/84
cou: REPL BY 5156
s/a: Dr 5136
SHAFT 3 - 2000767 P 12/97 5/97
RoD - c000280 F 12/97 s/oa
ono: s0030925 s ORDER TOTAL:

DE DIXON 7 DY DrxoN

 

RELEASE 2.2 _


X36-4 BIN AVAILABILITY REPORT [2]

TECHNICAL INFORMATION

Files Used

IAM
IBM
PXIVT

Field Mapping/Calcs

Dealer List Base 4 Price
Sugg List Base 3 Price

Internal Base 2 Price

Dealer Net Base 1 Price

CT Part Category

PKG Package Qty

PJ Per Job Pieces Required
Data Timing

None
Data Included/Excluded

Ifall vendors are requested, each vendor's information will print separately
in order of vendor code.

OPTs/Additional Products

OPTs - None
Additional Products - None


[ «| X36-4 BIN AVAILABILITY REPORT co

Required Procedures
None
Data Sorts

Vendor, Class, Bin Order

RELEASE 2.2 WL

## CHAPTER X36-5

ON HAND QUANTITY REPORT

### Introduction

The On Hand Quantity Report indicates the status of your inventory within
the range of low on hand and high on hand which you specify. For
example, if low on hand is specified as -10 and high on hand at 0, the
report will list those parts which are zero on hand and negative on hand to
-10.

One vendor (or all) and one class (or all) may be selected.
Management Notes. The On Hand Quantity report lists all inventory that
falls in the selection criteria. For example it can be used to print all parts

with a negative on hand quantity by using a low selection of -9999 and a
high of -1.

PRINTING THE ON HAND QUANTITY REPORT

O Type the specific vendor code or ALL.

 

 

Type the specific class or ALL.

 

OO Type the low on hand quantity and press FIELD EXIT.

 

CO) Type the high on hand quantity and press ENTER.

Note:

If entering a negative on hand amount, use the FIELD - (minus) key to |
indicate the amount is negative.

 

The report will be placed on the job queue. Press ENTER to return to a
menu.

## X36-5 ON HAND QUANTITY REPORT

   

Below is an example of the report.

ABC COMPARY ON HAND QUANTITY REPORT 39/30/86 -X3650-3A
wiynor, co nN ‘ON HAND BETWEEN 00000 AND 00022 MP MASSEY-FERGUSON
DEALER SUG DBALER any
PART NUMBER DESCRIPTICN ON HAND RSRV BIN LOC LIST «LIST INTERNAL NEY CLS LCT LS PYS YTD PKG REG
RO 002327 SUITCH SP ORDER 19.02 -17.29 12.76 D0e1176 3786
us ur0023, GASKET KIT SP ORDER © 65.97 62.70 ¢0. 80 00C4950 5/85
4 980 STRIPPED SLOCK SP ORDER 1180.85 1073.50 805.00 acs05c0 4186
000 36a, SECTION 683-7 ooness x 5/684
002 325Mp1 [BRAKE KIT 884-6 0003075 x 8/8¢
001 33992 LINE KIT Bor 0090751 x 12/85
001 soay BALL gouN? BBE-2 9000450 x 8764
p02 196x xy 504-7 oooda12 e 22/65
002 2358, GASKET oo oovoe1s x 1/85
02 312% BOUT 2 eBs-7 0090023 x 6/84
02 63ex sur 2 ene-2 ooodeca x 6/84
002 784x BOLT 10 baa. oovoa1s x /6¢
MF MASSEY-PERGUSON ME MASSEY-FERGUSON MP ass2Y-FERGUSON MP MASS2Y-PERGUSON :

  

Notice the criteria chosen on the above report. The report lists
everything in the Massey Ferguson inventory between 0 and 22 on hand.

 

t
RELEASE 2.1 NK


 

TECHNICAL NOTES

Files Used

IAM
IBM
PXIVT
IGA
IGM

Field Mapping/Calculations

Dealer List Base 4 Price
Sugg List Base 3 Price

Internal Base 2 Price
Dealer Net Base 1 Price
RSRV Quantity on reserve for Work orders etc
PKG Package Qty
REQ Per Job Pieces Required
Data Timing

Should be part of dealers regular schedule (weekly or monthly).


 

Data Included/Excluded

Records are selected based on the low on hand quantity and high on hand
quantity selection criteria. Also by Vendor and/or class. For example : All
CASE Products that have an on hand quantity between 0 - 50.

OPTs/Additional Products

OPTs - None
Additional Products - None

Required Procedures
None
Data Sorts

Qty On Hand, Vendor, Class

é

RELEASE 2.1 NS

## CHAPTER X36-6

LINES BY DEMAND REPORT

### Introduction

The Lines By Demand Report lists parts in order of the number of sales
from high to low. One vendor (or all) and one class (or all) may be
selected, A recap is also printed which shows total lines sold. One use of
this report might be to obtain a list of slow moving parts.

This report is actually based on QUANTITY (or PIECES), not demand. It
uses the current month plus the last 12 months pieces starting with
January.

The report has headings for Pieces (not calls) MTD (Month-To-Date) plus
JAN-DEC. MTD reports pieces for the current month, Then the report
works back starting at last January. For example, a report run today
(12/3/96) will have the 12/96 pieces in the MTD column, 1/96 pieces in
the JAN 2/96 pieces in FEB and so forth until it reaches the DEC column
which is 12/95 pieces. So, depending on the timing of this report, it is
actually reporting pieces for 13 months. These pieces are totaled on the
recap and organized into the appropriate categories: if 342 of a part are
sold, it will appear in the 300-399 category. The net value is the pieces
sold X current net.

### Preparation

End of Day will update the history files. Before running the Lines by
Demand report, run Parts End of Day (X3-9). Refer to Chapter X3-9,
Parts End of Day for more information.

## X36-6 LINES BY DEMAND REPORT

 

### How To Run

O Type the specific vendor code or ALL.

O Type the specific class or ALL.

O Type the number of copies (1 to 9) to be printed.

Oi To select parts based on demand, type Y (Yes). If not, type N (No).

If ¥ is selected, press ENTER and specify number of calls in number of
months. Press ENTER.

 

 

 

 

Press ENTER. The report will be placed on the job queue. Press
ENTER to return to a menu. (

The Lines by Demand Report will print in two sections: the analysis and
the recap. Part numbers are listed with the description, bin location, on
hand, last sale information, last receipt information, total cost, total pieces
purchased and the month the part was purchased in.

RELEASE 2.1 LU


LZE'S TRACTOR SALES, INC.

LYNDEN, WA

PART NUMBER

w208PPES
c100

Rp1040-406
Bes
RALO?ARE
17277
213107THP
33711
GL1o2eRaB
G1L06eRRBZ
ane

RAKZ 3/16
vea17/16
20x35x7
99212
99274
GCL10¢KRRB
‘SCLIOSRRRE.
GRALOONPPE
GRALOINPPE
GRALOIRAB2
GRALOANPPB
GRALCERRE
GiiooxRan
G1103KRx8
G1103xRRB3
G110¢KRAB
G1105KRRB
1107KRAB
G1108KRAB
G1120KRAB
GI11LKRRB
Gi112cRae
Gi21aKRRB
G111sKRRB
G1z00KRan
1uM14276
ROTL34
RHPLOSS-50
PART NUMBER

 


 

An example of the Lines By Demand Report follows:

LINES BY DEMAND REPORT Date 12/03/94 Page 1
RG: BEARINGS & SEALS Tima 16.50.03 x3660-30

Th teess QUANTITY INFORMATION "e008
QTY MTD JAN FEB OMAR APR MAY JUN JUL AUG SEP OCT NOV DEC

‘
a
3
a
2
2
2
2
2
x
2
£
2
aL
L
a
1
°
8
0
0
8
®
°
°
0
©
°
°
°
°
°
°
o
°
°
o
°
°

BIN LC ON BND oct Nov DEC


   

An example of the recap follows:

ERE'S TRACTOR SALES, INC. LINES BY DEMAND REPORT - PIECES Date 12/09/34 Page 2
AINE. WA L BRG: BEARINGS & SSALS Pime 16.50.93 3660-38

TOTALS FOR BEARINGS & SEALS

DEMAND LINES NET VALUE
1000 AND OVER +00
900 - 359 00
800 - 899 0
700 - 759 00
600 - 659 +00
soo - 599 +00
400 - as9 -00
300 - 359 08
200 - 259 00
x00 - 199 +00

99 39 -00

a0 89 02

7 9 +00

60 69 +09

a %s (
30 00 .

 

The recap shows the total lines sold in a certain cost range.

RELEASE 2.1 Co


 

TECHNICAL INFORMATION

Files Used

IVTIC
IGMIC
IAM
IBM
IVT
IGAIF
LBDF

Field Mapping/Calculations

TTL Net Base 1 Price * On Hand Qty
TTL Total pieces purchased

Data Timing

 

Run Parts End of Day for up most current information.
Data Included/Excluded

One Vendor or all, one Class or all.


 

OPTs/Additional Products

OPTs - None
Additional Products - None

Required Procedures
None

Data Sorts

Parts can be selected based on demand for number of calls in number of
months, or sorted by cost. (

RELEASE 2.1 LL

## CHAPTER X36-7

ON HAND VALUE REPORT

### Introduction

The On Hand Value Report lists those parts with the largest extended net
first or in part number order. One vendor (or all) and one class (or all) may
be selected. The report will also print parts based on demand for the period
you specify.

Management Notes. The On Hand Value report lists parts with their
extended net and list. It also prints parts and their net value based on

demand. If he Average Costing Enhancement OPT (X6332-7) is on, you
can choose from Average Cost or Net cost.

### How To Run

O Type the specific vendor code or ALL.

0 Type the specific class or ALL.

 

OC If you want the report to list by extended net, type Y (Yes). If not,
type N (No). The report will print in part number order.

O Type the number of copies (1 to 9) to be printed.

CO) if you want parts selected based on demand, type Y (Yes). If not, type
N (No).

 

 

 

 

If the Average Costing OPT (X6332-7) is on, type A(Average) or
N(Net).

Press ENTER and specify number of calls in number of months.

O Press ENTER. The report will be placed on the job queue. Press
ENTER to return to a menu.


X36-7 ON HAND VALUE REPORT a

Following is a sample report:

ABC COMPANY ON HAND VALUE REPORT BY EXTENDED NET Bate 9/30/97 Page 1
wayNor, co SC: scHeroT ime 14.05.33 x3670-38,
RESERVED PART EACH OW BAND VAUOE

PART NUMBER Desc ‘counren NET ner List
836 Star 309 8.36 . $8.52 84.70

547 Sta? 410 8.7 : 49.25 71.28

980 SCREEN 9.50 47.50 68.75

821 RISER 510 8.21 32.98 47.52
ose SCREEN 10.64 31.92 26.20

760 RISER 410 7.80 30.40 44.00

782 SuAT 516 32 30.08 43.56
1284, REPAIR 360 15 22.75 -00
12seB REPAIR 415 5. - 23.75 00
1102 ‘SCREEN 2 : 196 co
125ec REPAIR 510 78 : 109 +00

anc conanr ow hao VALE REPORT 8 BETEIMED NEE pate 9/30/97 mage 2
: Ser easton ie 14.05.33 .
3670-38 rorats Fox sows (
oss umes wer atte

4900.60 ax over vee

soo.e = 939.99 “oe

soarge - 639.39 “oe

yoarae | 139.39 “oe

f00100 = 633.33 “ea

590190 = 598.33 za

qoo.ce - 433.89 “to

3oo.ce 338.98 ‘to

200.29 - 299.99 3

1oaia0 > 399.85 a

soso > 9e.s3 sss2

wo 43.93 2 ness?

oo ae 2

$327.99

 

RELEASE 2.2 WS


X36-7 ON HAND VALUE REPORT [2]

TECHNICAL NOTES

Files Used

IAM
IBM
PXIVT
IVTIC
OHVF

Field Mapping/Calculations

List Base 4 Price
Net Base 1 Price
ParteaNet Total On Hand Qty * Base 1 price
PatteaLst Total On Hand Qty * Base 4 price

Data Timing
None
Data Included/Excluded

One Vendor or all, one Class or all.


[ «| X36-7 ON HAND VALUE REPORT Cc

OPTs/Additional Products

Average Costing Enhancement (X6332-7)OPT enables you to print
average cost rather then net.
Additional Products - None

Required Procedures
None
Data Sorts

Will list by: extended net, part number, demand. (

é
RELEASE 2.2 i

## CHAPTER X36-8

INVENTORY VALUATION REPORT

### Introduction

The Inventory Valuation Report is a listing of your inventory in part
number order. The report also shows net and list prices or, if the Average
Costing OPT (X6332-7) is on, you can choose from Average Cost or Net.
This report can show negative on-hand values, like the Parts inventory
Pad. One vendor (or all) and one class (or all) may be selected.

### How To Run

O Type the specific vendor code or ALL.

O Type the specific class or ALL.

 

 

Type the number of copies (1 to 9) to be printed.

 

 

 

If the Average Costing Enhancement OPT (X6332-7) is on, type
A(Average) or N (Net).

 

O To cancel this job, type Y (Yes).

O Press ENTER. The report will be placed on the job queue. Press
ENTER to return to a menu.

## X36-8 INVENTORY VALUATION REPORT

MGR EQUIPHENT SALES
LYNDEN, WA

PART NUMBER

205756
207365
208137
posses
425623

INVENTORY VALUATION REPORT
AC : ALLIS CHALMERS

RESERVED PART SACH VALUE
ese BIN Loc COUNTER RO ner LIST

RADIO 78.96 259,00
AIR CONDITIONER 225.00 $59.60
(G20-soNAR 5008.S4 19090,10
SHOVEL BLAZE 109.60 250.00
BEARING 1.66 2.61

‘TOTALS FOR ALLIS CHALMERS $8,414.16

511,071.31

Date 9/29/97 Page 1
Time 9.17.48 3680-28

ON WANE VALUE TTL «LST 12 MTHS VALUE
ner LIST SALES ner List

78.98 259.00 +00
09 09 : +00
+09 00 -20

109.09 250,00 +00

3.32 5,22

$503.78

5178.64

Note: The Total Sales field is based on the total sales of the previous 12

months.


X36-8 INVENTORY VALUATION REPORT [2]

TECHNICAL NOTES

Files Used

1AM
IBM
IGAIF
IGMIC
IVT
IVRF

Field Mapping/Calculations

List Base 4 Price
Net Base 1 Price
TTLSales Total Sales of the Previous 12 Months
Ext Net On Hand Qty * Base 1 price
Ext List On Hand Qty * Base 4 price
Data Timing
None

Data Included/Excluded

One Vendor or ail, one Class or all.


[ «| X36-8 INVENTORY VALUATION REPORT

OPTs/Additionai Products

Average Costing Enhancement OPT (X6332-7) to print average cost rather
~ then net.
Additional Products - None

Required Procedures
None
Data Sorts

By Part Number

## CHAPTER X36-9

INVENTORY BY LAST SALE DATE REPORT

### Introduction

The Inventory By Last Sale Date Report is a listing of your inventory in
order of last sale date with most recent sale first. One vendor (or all) and
one class (or all) may be selected.

### How To Run

G Type the specific vendor code or ALL.
Ci Type the specific class or ALL.

O Type the number of copies (1 to 9) to be printed.

 

 

 

To cancel this job, type Y (Yes).

 

0 Press ENTER. The report will be placed on the job queue. Press
ENTER to return to a menu.

## X36-9 INVENTORY BY LAST SALE DATE REPORT

 

Below is a sample report:

‘LEE'S TRACTOR SALES, INC. INVENTORY BY LAST SALE DATE Date 9/30/94 Page = 1
LYNDEN, WR rE Sc ; scHurDr ‘Time 14.07.13 3660-8

LAST LAST ON EAND TTL * ++ QUANTITY INFORMATION
© pes BIN LOC ON END SALE RCPI TTL NET QTY MPD JAN FEB MAR APR MAY JUN SUL AUG SEP CCT NOV DEC
P SLaT S10 140 4005/6 00/0 30.085 1 z
SCREEN 5 10/5 00/0 47,50
AISER 410 4206/5 00/0 30.40
SLaT 410 9 00/0 00/0 49.23
RISER 520 4 00/0 90/0 32.86
SLAT 300 7 90/0 00/0 Se.52
‘SCREEN 3 00/0 00/0 31.92
SCREEN 0070 9070 00
REPAIR 300 oo7e 90/0 23,75
REPAIR 410 e070 00/0 23.75,

REPAIR 510 0070 00/0 -00
DESC LOC ON HND SALE RCPT TTL NET QTY MID JAN FEB MAR AP MAY JUN JUL AUG SEP OCT NOV DEC

P
P
P
2
P
Pe
Pe
P
Pe
By

TOTAL LINE ITEMS; nu TOTAL NET vaLE: 3327.99

 

RELEASE 2.1 Ne


 

TECHNICAL NOTES

Files Used

JAM
IBM
IGAIF
IGMIC
IVT
IVRF

Field Mapping/Calculations

On Hand TTL Net On Hand Qty * Base 1 price
TTL Quantity On Hand Qty * any reserved parts

Data Timing

None
Data Included/Excluded

One Vendor or all, one Class or all.
OPTs/Additional Products

OPTs - None
Additional Products - None


 

Required Procedures
None
Data Sorts

By Last Sale Date
Xe

## CHAPTER X36-10

PRINT PRICE LABELS

### Introduction

The Print Price Labels prints on standard address label forms. These labels
will print on address label forms that are 1,2,3 or 4 labels wide. The size to
order is 3 1/2" X 15/16. Labels are printed 6 lines per inch.

### How To Run

Oo

Q

Type the name of the vendor to appear on the printed labels.

Type the number (1 to 4) of labels wide to match your current forms.
Press [Enter].

Type the name of the vendor code.

Type the part number and part quantity. Press (Field Exit] after each
entry.

28 lines per screen are available for entering part numbers and quantity.
Parts can be entered in any order. If no quantity is specified, the default
is 1.

Press [Enter]. The parts will be edited for a valid number in your
inventory and errors will display. If errors are displayed, press [Field
Exit] to delete or re-type the correct part number.

Press [Cmd2] to print the labels.

The Price Labels will be placed on the job queue. Press [Enter] to
return to a menu.

## X36-10 PRINT PRICE LABELS

 

An example of the printed Price Labels is shown below.

ABC COMPANY ABC COMPASTY
NCA710-38 875GE9

FRD $76.06 FAD $17.48

ABC COMPANY 2c COMPANY

275¢89 E7SGES

PRD $17.49 FRD $17.48

 

RELEASE 2.1 LL


 

TECHNICAL NOTES

Files Used

IAM
IBM
IVT

IXM

Data Timing
None
Data Included/Excluded
By Vendor Code
OPTs/Additional Products

OPTs - None
Additional Products - None

Required Procedures

None


 

Data Sorts

Vendor

RELEASE 2.1 tO

## CHAPTER X36-11

LOST SALES REPORT

### Introduction

Lost sales are recorded when you use the priority code "L" on a Point of
Sale document (X5-1) or when you use the transaction code "L" at Parts
Posting & Maintenance (X3-2). Lost sales are posted to history by Parts
End of Day.

### How To Run

From the Parts Report Menu (X3-6), select option 11, Lost Sales Report.
Following the Parts security gate, the selection screen appears as
illustrated:

A & R SALES & LEASING CO LOST SALES REPORT X36B01-01

Division: a

Class (Or AL)...

Range Of Lost Sales

Summary By Part @

## X36-11 LOST SALES REPORT

 

O Make your selection. To request a report for one day, use the same date
in the fields labeled "From" and "To." If you are requesting a report for
the current day, make sure Parts End of Day has been run.

O Press [Enter] to put the report on the job queue.

RELEASE 2.1 CC


   

An example of a Lost Sales Report follows:

LEE‘S TRACTOR SALES, INC. Lost Sales Report pate 12/09/94 Page
Division: L Vendor: ALL Class: Abt Prom: 02/01/93 To: 12/32/92 Summary: N Time 26.52.08 x3@80-301

order ~-Lost. Sales
Min Max Dealer Net Dealer Lst--Dato--=+-0ty-
10.38 19.23 06/30/93 2

27.23 54.20 0@/11s93

12.57 23.26 04/01/93

03 $0.08 06/30/93,

128.64 03/10/93

43.81 09/11/93

5.84 00/11/93,

1.89 06/08/93,

103.96 06/30/93,

36.89 06/30/93,

35.25 06/08/93,

Part # Description
cepnsoogs wir
c9smiP 7338, SPRING
‘pape 494 Ring
D¢ntL73658 CABLE
DSNNB200A GRILL
ESNNSC231DB ‘cowron
E7DN915BA GASKET
$BA122990562, ‘GASKET
'§8A350200380

252499 ELT

an 6548

»
2
&

### Eeeeee Ee Eee

LEE'S TRACTOR SALES, Lost Sales Report Date 12/03/98 Pege 2 :
Division: L Vendor: ALL Class: ALL From: 01/01/93 To: 12/31/92 sumary: N Time 16.51.08 3680-302

order atest Sales: oy :

vendor Part # peseription Class Bin Code in Max Dealer Net Dealer Lst--Date-----gty- Total
Gag 99-330-227 om a 38 232 06/17/93 1 1
ecg 99-330-427 AF 30 +50 06/17/93 2 a

LEE'S TRACTOR SALES, INC. Lost Sales Report Date 12/09/94 Page 3
Division: L Vendor: ALL Chass: ALL From: 02/03/93 To: 12/31/92 Summary: N Time 16.51.08 3680-202,

order s-bost Sales
Part # Description less Bin Code Min Max Dealer Net Dealer Lst--Dace-----Oty-

1048273492 =D a 20.81 49.83 12/15/93 -
isan46mo1 FAN 22.32 $0.70 12/29/93

37042 76e1 3.03 7.91 12/09/92 :
si215e HOSE 10.98 17.79 98/09/93
5261 79M52 HOSE 12.35 20.0 08/09/93
6e7004M1 58.34 $4.36 97/09/93
831770m, 3.50 5.51 07/20/93
B3a532m, 19.90 32.19 06/30/93

 

we em

Grend yorals + 366.08 659.63

 


 

TECHNICAL NOTES

Files Used

IAM
IBM
ILS

Field Mapping/Calculations

Dealer List Base 4 Price
Dealer Net Base 1 Price

Data Timing

None
Data Included/Excluded

One Vendor or all, one Class or all, Date range.
OPTs/Additional Products

OPTs - None
Additional Products - None

{
RELEASE 2.1 Ne


 

Required Procedures

None; however, Parts End Of Day should have been run for the days
within the specified range as Lost Sales are posted in the Parts End Of Day
job.

Data Sorts

By Vendor, Part#


Notes:

## CHAPTER X36-12

LAST SALE DATE RANGE REPORT

### Introduction

This report is a listing of inventory in order of last sale date with most
recent sale first within a date range. It is similar to the Inventory by Last
Sale Date Report (X36-9) except that it can be restricted to a range of
dates. The report is printed in order by part number.

## X36-12 LAST SALE DATE RANGE REPORT

 

### How To Run

From the Parts Report Menu, select option 12, Last Sale Date Range
Report. Following the Parts security gate, the selection screen appears, as
illustrated below:

A & R SALES & LEASING CO LAST SALE DATE RANGE REPORT X36C01-01
Division: A

vendor (Or ALL)

Class (Or ALL)

Last Sale Date

 

 

 

 

 

Make your selection. To request a report for one day, type the same
date in the fields labeled "From" and "To."
O Press [Enter] to place the report on the job queue.

{
RELEASE 2.1 NS


LEE"S TRACTOR SALES,
Division: &

Vead Part ¥
GRALOON?PR.
GeaLo3RRE2
G1100KRR
G1102KRRB
GLLO6KRRB2
G1307KRRB
G1I20KRRE
G1222KRRB
RAEZ 3/16
RHE1O55-50G
32371
12458
3862
307F
asHs,


An example of a Last Sale Date Range Report follows:

asc.

Deseription
BEARING
BEARING

2 IN BRC
INSERT
RG
17/16 BRE
1 578 are
23/4 BRG
RG

BRS

SEAL

i ae

Vendor: BRC Class: ALL From: 01/92 To: 01/94

Bin

Last gale Date Range Report

Last Receipt Order

Qty Date code Min
4 4/17/89 &
5/28/88 &

2 3/07/93

a
a
a
a
a
a
a
a
A
a
A

Class A Totals :
Vendor BRG Totals +
Grand Totals +

Max Avail Hand

pate 12/12/96
Time 16.36.48

Total
Available
+00

74h
16.36

-08
00
21.60
+00
103.62
00
90
00
-00
00

 

Page
3600-302,

Tonal

bate


on Hand Ist sale

7.48
16.86
+00
95.55
00
00
21.60
-00
103.62
+00
-00
-00
00
+09

236.08
236.04
236.04

2/93
4792
9193
2794

12/93
4/92
6/33
6/93

12/93
4193

10793
5/93
9193
7193
6193


 

TECHNICAL NOTES

Files Used

TAM
IBM
IGAIF
IGMIC
IVT
IVRF

Field Mapping/Calculations

On Hand TTL Net On Hand Qty * Base I price
TTL Quantity On Hand Qty * any reserved parts

Data Timing

None
Data Included/Excluded

One Vendor or all, one Class or all. Date range.
OPTs/Additional Products

OPTs - None
Additional Products - None


Required Procedures
None
Data Sorts

By Last Sale Date


Notes:

## CHAPTER X36-13

AVAILABLE PARTS REPORT

### Introduction

The Available Parts Report lists all parts for which there is an available
quantity.

### How To Run

From the Parts Report Menu, select option 13, Available Parts Report.
Following the Parts security gate, the selection screen appears, as
illustrated below:

O Make your selections and press [Enter]. The report is placed on the job
queue.

An example of an Available Parts Report follows:

## X36-13 AVAILABLE PARTS REPORT

A & R EQUIPMENT SALES
Division: L

Vendor part #
Ag235478
ALS?
‘APNI20008
(APNI70008,
2857585
ARPSOAGSS
ARP305045
ARON
‘ABNNI22508,
ABNONL22503
‘ABNNA268a,
84222
BBd627
3B7234
BERSSe118
BMB2328
BMB23€7
3MB7256
ByBg0eL
BYCAGODOG?
BMCCK00003
BSDI338
pspeaa
Bspdadr
BspedaTs
BsZ60see
Brciocses
37¢20152
3064367
Basenoo
‘BONNI05058,
BONNL22000
‘B2NNG750R
‘BONNI7I553.
BONNS7300
BONNDATSIA
carN33018
CAPNS2008,
cani02149
caR118733
caRI18734
caR116723
can118677

AAA
AAR
AAR
AAR
AAR
BAR
AAR,
AAA
TAR
AAR
AAR
AAR
AAR
ARR
ABA
AAA
ARR
AAR
AAR
ABA
ARR
BAR
ABR
AAR
BAR
AAA
AAA
ARA
AAR
AAA
ABR
AM
BAR
AAA
ABA,
AAR
ABR
AAA,
AAR,
AMR
ABA,
ABA
AAR

Deseription
GASKET

PLUG, SPARK
KIT

KIT

ENGR

KIT SEAL

KIT CYL REPAIR
PL

RESTR

RESTR

SEAL

class

>

RRO Oe

Available farts Report
Vendor: AAA Class: A

Available Reservations

sin ay mv.

sa? 233

u 4.02

Fo 3.94

I 4.33

26.78

27.57

28.35,

1.20

30.27

9.62

6.93

5.28

“286


15.63

4.76

9.05

3.46

3.02

14.98

8.88

3023.90

3674.00

2492.00

4492.40

4.06
1.90
7.27
8.70
46.40
47.83
49.33
2.22
20.53
19.23
12.96
9.74
3h
1.10
27.16
8.18
15.72
14.68
5.19
25.99
15.33
4031.95
4898.95
5989.95
5509.95,
2.51
83.24
43.93
3.89
22.47
14.82
4.87
2.72
8.18
16.37
2.04
28.85
4.02
23.91
31

24.03
28,72

Bete 4/21/92
rime 11.17.03

W/O Dealer Net nealer Wist Ext. Net

“53
12.22
35.19
8.56
53.56
27.57
28.35
10.20
10.27
48.10
27.72
10.56
1.06
2.20
31.36
4.78
36.20
0.46
12,08
14.98
8.98
9071.70
18370.00
4292.40
2984.20
2.45
48.23
30.76
79.80
50.26
31.80
14.96
2.98
2.86
8.37
3.06
43.25
35.08
1n.s6
26

21.00
34.27

Page 1.
3600-201

Bxt, List
3.06
20.50
65.43
17.40
92.80
47.83
49.13
19.98
20.53
96.15
51.46
19.48
2.06
«49
54.32
8.18
62.88
16.68
20.76
25.99
15.33
32095.85,
24494.75
5929.95,
21979.90
2.81
e314
87.86
138.15
87.28
59.26
23.02
5.44
16.36
16.37
6.12
35.55
64.32
23,92
-32

42.09
28.72

 


 

TECHNICAL NOTES

Files Used

IVT
JAM
IBM

Field Mapping/Calculations

Dealer List Base 4 Price
Dealer Net —_ Base 1 Price
Ext. Net Dealer net X Qty
Ext. List Dealer list X Qty

Data Timing
None

Data Included/Excluded
NA

OPTs/Additional Products

OPTs - None
Additional Products - None


 

Required Procedures
None
Data Sorts

By Vendor, Part#
oe

## CHAPTER X36-14

BIN LOCATION RANGE REPORT

### Introduction

The Bin Location Range Report lists parts for a vendor/class (or all) for a
selected range of bin locations. Blank bin locations with an on hand
quantity can be omitted, if desired.

Bin locations can be requested in compressed or expanded form.
"Compressed" means left justified, dictionary order. "Expanded" means
that letters are placed on the left while numbers are right justified and
special characters are treated as blanks. For example:

Compressed Expanded
1) ABC256 A__123
2) A123 A___1218
3) A4*2B AB 42

4) 12A18 ABC__256

## X36-14 BIN LOCATION RANGE REPORT

 

### How To Run

From the Parts Report Menu, select option 14, Bin Location Range
Report. Following the Parts security gate, the selection screen appears, as
illustrated below:

A & R SALES & LEASING CO BIN LOCATION RANGE REPORT X36E01-01,
Division: A

Vendor (Or ALL)

Class (Or ALL)

Bin Location: (

Compressed or Expanded (C/E): ¢

a-+ or --+

All Blank Locations With Available Quantity: N

cmdl-End Job

 

O Make your selections. To request a report for one bin, type the same
Jocation in the fields labeled "From" and "To.”
O Press [Enter] to place the report on the job queue.

RELEASE 2.1 LO


 

 
  
    

   

### Warning!

If you answer "Y" to “All Blank Locations With Available Quantity,”
only parts with blank bin locations are listed.
ae


   

An example of a Bin Location Range Report follows:

A & R EQUIPMENT SALES ‘Bin Location Range Report. Date 4/22/92 Page 1
Division: 1 Vendor: AMA Class: M All Bin Locations Time 13.24.34 3650-301

Vendor Fart # Deseripcien Class order Code Min. «Max Qty On Hand = Qty Available Bin
NDAG2220 cop x 1
‘NDAG62ER BEARING
wACA2218, cone
93573 cone
91p12434, cup
91p12¢4A, CONE
s2G29 BEARNG
B61¢89 BEARNG
E7588 BRNG
312818 cur
322820 cons
312848

eSNP10045

CSNPIONDZA

CSNNIAAS2R

esnaeaNo41a,

csawv7No42n,

CSNNINOAEA

CSVINOABA

csmmésa

caNN71272

caN71273,

CNT 008,

cmy71182

DONN7RO6EA,

83552

connanz218

c7NN3 5528,

conaa74a,

DANNAAZ42A,

NDAG223A

wang221A

WAAA227a,

c1wvi202a

c1wi216a

e1wi217a

DSNNL2G1A

DSIN1216A,

DSNNL217A,

Baizo1B

BA1202—,

Balz17a,

KREMER ERE ERR RR RRR ERE REE REE ER ER KKK EEE EERE KK
a ed

Ana,
ann
AAA,
ARA,
ana
ABA,
BAA
2a
aA
aan
AAA
AAR
DAR
AAR
AAR
AR
AAR
AAR
AAA
AAA
BAA
AAA
AAR
AAR
AAA
AAR
AAR
AAR
AAA
AAA
AAR
AAR
BAR
BAA
AMR
AAA
AAR
BA
BRA
AAA
AM
ABA

BER PERE R ROOM RRM RRR RHA daADe

Grand Totals:

 

RELEASE 2.1 Lo :


 

TECHNICAL NOTES

Files Used

IAM
IBM
IVT

Data Timing

None
Data Included/Excluded

One Vendor or all, one Class or all.
OPTs/Additional Products

OPTs 0= Print Bin Location
1 = Print Base 4 Price instead of bin location
2 = Print Base 3 Price instead of bin location

Additional Products - None

Required Procedures

None


Notes:

RELEASE 2.1 LO

## CHAPTER X36-15

UNUSED BIN LOCATIONS REPORT

### Introduction

The Unused Bin Locations Report prints a list of parts with non-blank bin
locations and zero on hand quantity. Its purpose is to make it easy to
identify bins that are empty. If the part number is no longer stocked, the
bin location can be reassigned. The list is in order by bin locations.

Bin locations can be requested in compressed or expanded form.
"Compressed" means left justified, dictionary order. "Expanded" means
that letters are placed on the left while numbers are right justified and
special characters are treated as blanks. For example:

Compressed Expanded
bh ABC256 A___ 123
2) A123 A__1218
3) A4*2B AB___42

4) 12A18 ABC__256

## X36-15 UNUSED BIN LOCATIONS REPORT

 

### How To Run

From the Parts Report Menu, select option 15, Unused Bin Locations
Report. Following the Parts security gate, the selection screen appears, as
illustrated below:

A & R SALES & LEASING CO UNUSED BIN LOCATIONS REPORT X36F01-02
Division: A

Vendor (Or ALL)

Class (Or ALL)

Bin Locations: : (

To:

Compressed or Expanded (C/E): C

Leave blank for a list of all bins

(mdi-End Job

 

0 Make your selections. To request a report for one day, type the same
date in the fields labeled "From" and "To."
Press [Enter] to place the report on the job queue.

 

 

 

 

An example of a Unused Bin Locations Report (all bins) follows:

RELEASE 2.1 LU


 

A&R SALES & LEASING COMPANY Unused ain Lecatiens Report Dave 4/24/92 Page 1
Division: & vender: AAA Class A All Bin Locations Time 11.15.44 X36F0-302

Vendor Part & Deseriprion Class Last sale Date Bin
GEasaoa ‘TANS KIT
ang003 RADAR
987E92300 MUFELR
DONNBOSA DRABAR
DaNNeOSS DRABAR
eSNES3024

e5NE9600E CLENER
DBRNDS72BA TOBE
DOXNSASSSBA LIKE
BONNOASSGAR LINE
DONNSASSBAA, LINE
@B242007 BLADE
NCAS2558

sazeea

148122

310s

58A0S0203125

spaz2e990060

spa326990180

BUNNSASEZA,

CONNICT7OA

CSNINSS35

CSENSNSSEC

CSNNSNGEZA

CTNNSESEOR

C7NN3BSEIC

DANNSR762E

‘DENNC7S728

DaNNIBSEEBA

DBNNEZB2BA

POUNBASGACE

‘$mage0220042

eswnienso7e

‘CSNN1660SAB

CSENTBL6RF

cSNN7B2920D

c7wniensazr

PONEOSIC

DENESE4A

DRNT7021

DENYL6N78AA,

EBENLEGOSE

s2eesseas

6189
4790
4/91

32788

ayyst
6/90
4791
4788
4/9,
8/85
aan
6/81
6/90
3/91
2790
382,
5/81

20/90
1789
ans
27a8
3/92
saa
1/88

nss1
eres
8/91
9791
4/90
9790

ans91
9788
4sea
5790
5/90
9790
6/91
12/88

 

 

 

vouvuusveusoD DU RRR AA ANAANN OME ED

paEATDEL

10/52
roses

:

AKA
ABA
ana
BAA
BAA
BAR
MA
AAR
AAA
BAA
AAA,
ABA,
a
aa
Ana,
Ana,
ABA
ABA,
AAA,
ABA
ABA,
aA
aA
ABA
ABA,
AAA
AAR,
ARK
AAA,
ARR
AAR,
AAR
AAR
AAR
aA
AAR
AAR
ARN,
AAR
AAR
aA
ARK,
AAA,

POD OD wD wD


 


 

TECHNICAL NOTES

Files Used

IAM
IBM
IVT

Data Timing
None

Data Included/Exciuded (
None

OPTs/Additional Products

OPTs - None
Additional Products - None

Required Procedures
None
Data Sorts

Parts numbers can be requested either compressed or expanded.

RELEASE 2.1 Ne

## CHAPTER X36-16

QUICK CODES REPORT

### Introduction

The Quick Codes Report lists ail parts that have quick codes in order by
their quick codes.

### How To Run

From the Parts Report Menu, select option 16, Quick Codes Report.
Following the Parts security gate, the selection screen appears, as
illustrated below:

A & R SALES & LEASING CO QUICK CODES REPORT
Division: A

Vendor (Or ALL)

Class (Or ALL)

## X36-16 QUICK CODES REPORT

 

0) Make your selections.
Press [Enter] to place the report on the job queue.

 

 

 

 

An example of a Bin Location Range Report follows:

‘A @ R EQUIPWENT SALES Qvick Codes Report. Bate 4/21/92 Page 1
Divisien: L Vendor: ALL Class: ALL rime 11.06.09 x3sgo-302

Quick Code vendor Part # Description
aa7agaa = gag 347 4942m2 RIG

 

RELEASE 2.1 C.


 

TECHNICAL NOTES

Files Used

JAM
IBM
IVT

Field Mapping/Calculations
None
Data Timing
None
Data Included/Excluded
One Vendor or all, one Class or all.
OPTs/Additional Products

OPTs - None
Additional Products - None


 

Required Procedures

None
Data Sorts

By Quick Code
Co

## CHAPTER X36-17

SUPERSEDED PARTS REPORT

### Introduction

The Superseded Parts Report lists parts that have been superseded in order
by the original part numbers.

### How To Run

From the Parts Report Menu, select option 17, Superseded Parts Report.
Following the Parts security gate, the selection screen appears, as
illustrated below:

A & R SALES & LEASING CO SUPERSEDED PARTS REPORT X36H01-01
Division: A

Vendor (Or ALL)

Class (or ALL}

endl-End Job

 

O) Make your selections.
O Press [Enter] to place the report on the job queue.

## X36-17 SUPERSEDED PARTS REPORT

 

An example of a Superseded Parts Report follows:

A & R EQUIPMENT SALES Superseded Parts Report Date 4/21/92 page 3

Division: L Vendor: ABA Class: A Time 11.20.11 x36H0-302
-a~ Supersession Information ----+=

Vendor Part # Deseripcion tess Bin On Hand order Code = Min Max Code Vendor Part # ory

08121823, ROLLER s AyB121696

BECAFRDOOS ROD BMCAFRDO23

BeICAGoO00S wT BMCAGOOOaL

pecaceo007 xr BcAgoD083

BMcAG00009 xrr BMCASO0084

Bs2537070026 ENGINE 852837070326

83390303, VALVE 5399949

s391788 cans BS393410

BTc350 Brcaza

BUs4799 BLADE Bu64452

Bus4e00 BLADE Bu64a54

caR1O7555 Baa EONNGG42RA,

crPueaa7B EBPNS3373

creNea37e EBPNSI37E

cMc141036 cuciaai58

omn.16072 68221725

omv16573 389763 (

 

>
»

comm15330a ESNN1S3300A,
comm7sscoa EQNN?5S0GA,
CONNIASSOA EENNTAS39AA,
caNeezi4n, ECTNG214RA,
cSNEE303K ESUNERBOZAA,
cSNE620aN ESNING303AA
cenee37su EONNGI7SHA,
cSNES3a2R, EINN6IB4AA
CSNESPSESA ESNNSFSSSAA,
cSNES206C ESNN92QERA
CSNF110520 BENNLIK17SBA,
¢5NF121358 EANNLIK17SBA,
conp2144a2 EGnNIIKL7SBA,
cSNNAT28A, ESNNAT2SAA,
corerecion, 281170
carmmps4on, 390a03s
comn728c ESNNNTZEAA,
csra7793 FONKNT?9RA,
csrev2n099B ‘BeNN2AOIBAA,
CSNNZNOD9A BANNINO9SAA,
csmvano93n BAMNZNOSSCA,
conmani00n ‘EANNDNLOOBA,
cerm2na36a, EINNN336AR
esrmawacon BANNGnOg3BA
conE9615, BONNBOGIAA
CONW3A5908, EGENSNSO3AR
canmape24e OENSNSOJAR

ABA,
ABA,
AAA,
ABA,
ABA,
ABA,
ABA,
AAA
ABA,
BAA
AAA,
Ana,
ABA
AR
AMA,
ABA,
ABA,
ABA,
ABA,
ABA
AAA,
AAA
AMA,
ABA
ABA,
AAR
AAR
AAA,
AAA
AAA
AAR
AAA
AAA,
AAR
ABA
AAR
Bas
AAA,
AAA,
AM
AAA,
AMA,
AAA
AAA,

EEEREEEE EERE EEE ER ER EE EE ER ERE ZEEE EEE EE ER ER ERE

nonnnnonn

 

RELEASE 2.1 Lu


 

TECHNICAL NOTES

Files Used

IAM
IBM
IVT

IXM

Field Mapping/Calculations
Superseded Qty Number of new parts required to replace old
Data Timing
None
Data Included/Excluded
One Vendor or all, one Class or all.
OPTs/Additional Products

OPTs - None
Additional Products - None


 

Required Procedures
None
Data Sorts

By Vendor, Part#
CL

## CHAPTER X36-18

PARTS BY RETURN CODE REPORT

### Introduction

The Parts By Return Code Report lists parts that have return codes in order
by part number, It can be limited to 1-10 specific return codes, including
blank return codes.

### How To Run

From the Parts Report Menu, select option 18, Parts By Retum Code
Report. Following the Parts security gate, the selection screen appears, as
illustrated below:

A & R SALES & LEASING CO FARTS BY RETURN CODE REPORT 36101-01
Division: A
vendor (Or ALL)..
Class (Or ALL)
Enter ALL Or Return Codes ...

Return Codes :

For a blank return code,
enter + as return cade.

Crdi-End Job

 

 

 

 

Make your selections.

## X36-18 PARTS BY RETURN CODE REPORT

 

Note:

 

To request blank return codes, enter "+" in one of the fields provided.

 

 

 

Press [Enter] to place the report on the job queue.

 

An example of a Bin Location Range Report follows:

A & R BOUSPMENT SALES Parts By Return Coda Ropore Date 4/21/92 Pease 1

Division: L Vendor: AAA Class: A Return Code: ALL ‘Time: 12.23.22 3610-301,
qast Return.

Vendor Part ¢ Description Class Bin Total Sale Date code

AAA BANWSG518NO2OAR BRACKET. a . +90 2/90 x

maa gomgeeton GaoRee a : she xen
notals Retuen Code H : ots (
rand Tecate ae

 

RELEASE 2.1 LL


 

TECHNICAL NOTES

Files Used

IAM
IBM
IVT

Field Mapping/Calculations

Dealer Net Base 1 Price
TTL Dealer Net Dealer Net * Qty On Hand

Data Timing

None
Data Included/Excluded

One Vendor or all, one Class or all.
OPTs/Additional Products

OPTs - None
Additional Products - None


 

Required Procedures
None
Data Sorts

By Vendor, Parti
LO

## CHAPTER X36-19

PARTS BY PART NUMBER REPORT

### Introduction

This report prints a list of part numbers in order by part number. The Parts
By Part Number Report can also correctly select and sort parts with
multiple segments or segments that are right justified. This happens if you
enter a single vendor whose parts meet these criteria. This allows you to
enter partial part numbers if segment markers are used.

### How To Run

From the Parts Report Menu, select option 19, Parts By Part Number

Report. Following the Parts security gate, the selection screen appears, as
illustrated below:

A & R SALES & LEASING CO PARTS BY PART NUMBER REPORT X3601-01
Division: A

vendor (Ox ALL}

Part numbers

Cmd1-End Job


[2] X36-19 PARTS BY PART NUMBER REPORT ( .

0 Make your selections.
O Press [Enter] to place the report on the job queue.

The Parts By Part Number Report can also correctly select and sort parts
with multiple segments or segments that are right justified. This only
happens if you enter a single vendor whose parts meet these criteria. Part
numbers on the "From" and "To" lines are checked to make sure they are
valid. This allows you to enter partial part numbers if segment markers are
used. When entering part numbers, make sure that the part number "From"
is lower then the part number "To" as in the following example:

A&R SALES & LEASING CO PARTS BY PART NUMBER REPORT x36501-01
Division: A

Vendor (Cr ALL) : (

Part numbers

From: _A11507.

To: —_A5S5555,

 

If "ALL" vendors are selected, the original report, which does not check

RELEASE 2.1 CC

## X36-19 PARTS BY PART NUMBER REPORT

for segments or valid part numbers, is produced.

An example of a Parts By Part Number Report follows:

AGR EQUIPMENT SALES Parts By Part Number Report
Division: a Vendor: ALL All parts

Pate 9/30/37 page 1
Time 28.22.47 3630-301

 

 

vender Part #

FOR AEI3530A
FOR APNI2C09A,
FOR APNI7OO0R
FOR APNSE2A,
APN6O02GA,
APNSOO2HA,
APREOSSD.
APNEOSSE
ABNS6OOA
‘APNS6OOB
APN6731B
APN94
APHOSSOA
PN9S9OB
AONNLOS70A,
ORN123008
AONNESOOR,
10900
logon
aloaga
810226
810329
alg72€
10988
a1i190
11208
a11209
ali2i0
alL2at
al1222
ai1213
alng21
11423
allaad
also?
al1e12
a11e22
al1ese
aiiess
11772

Description class sin order Code

LENT © 38
Kcr aA 35
aT aA
cr ais,
arr UPSTAIRS
xrr. UPSTAIRS.
kIT m2
kor 762
ar R56
IT R45
PxLTR SP 2
STEM

xIT

xr

cave

cnpsr

TAPET.

SNAP RING

CONE OR

BEARING 5

gomNy

PALL JOINT

‘SHIELD

FUSE CAP.

‘TACHOMETER

‘GASKET

BOWL

cup war

SCREEN

BAIL

EouL

GRSKET

SEAL

BELT

‘SEAL

CLAMP

asker

asker

GASKET

WASHER

nee PD RAaNnAnANAnANAAAAD AA

woe eee ee me

Pad

 

Dealer Net

Bean
3.98
3.08
3
191.67
asa.67
109.98
107.30
19.83
19.82
1.96
2.28
18.99
81
2.84
1.22
s.13
3.63
9.57
23.42
3.68
17
1.33
1st

M4
15a
40
38
-89
6.08
1.42
2.49
5.28
aad
9.31
2.22
2.01
2.01
6.95

total

3.42
39.80
3.98
14.88
0
192.67
109.98
197.15
13.82
19,81
84,26
2.28
72,09
4.08
2.92
Lz
41.04
116.26
277,83
=98
11.97
6.05
2.66
755
+90
1.26
3.08
3.20
09
1.60
6.08
08
449
2.2
69
37.24
90
12.06
12.06
=90


[+] X36-19 PARTS BY PART NUMBER REPORT

TECHNICAL NOTES

Files Used

IAM
IBM
IVT

Field Mapping/Calculations

Dealer Net —_ Base 1 Price
Total Dealer net * Qty On Hand

Data Timing
None
Data Included/Excluded
One Vendor or all, Part# Range.
OPTs/Additional Products
OPTs - None
Additional Products

None
CU


X36-19 PARTS BY PART NUMBER REPORT |

Required Procedures
None
Data Sorts

By Part Number


Notes:

## CHAPTER X36-20

CORE INVENTORY PAD

### Introduction

The Core Inventory Pad is similar to the Parts Inventory Pad except that it
lists only parts that have non-blank core codes. It can be requested for all
vendors/classes or restricted to a single vendor/class. Up to 6 core codes
can be excluded from the report. For more information about core codes,
see CHAPTER X3-2, PARTS POSTING & MAINTENANCE,


X36-20 CORE INVENTORY PAD on

 

### How To Run

From the Parts Report Menu (X3-6), select option 20, Core Inventory Pad.
Following the Parts security gate, the following selection screen appears:

Core Inventory Pad X36K0-001

vendor (Or ALL)
Class (Or ALL)

Number of copies (1-9)

For summary only, enter "Y*

Enter core codes to exclude

Grd1-cancel

 

‘

RELEASE 2.1 Ne

## X36-20 CORE INVENTORY PAD

 

A Core Inventory Pad is illustrated:

Core taventory Pad pate 5/04/32 Page
‘CASE/TH cas ‘Time 9.30.32 236K0-28,

Dealer Sugg, Dealer Cis Date Date Sales

Part Nunber Bescription On Hand Rsrv gin Lee List List Internal Net CC Lets Prev Yr Yed Cat Pkg PY
100789 3/8" SCREW 250 BIN 42 38 -28 9000025 Ac

con: DEWO FOR CORES
10329 BALL JOINT 5 5B67 3.25 2.95 4.77 0000177 ac aac.

Com: 10726
Evectty Bow, sB8s 30.30 9.36 08 DODDEOE RE 9/86

com: A12421 :
a1is07 SEAL 5083 1.67 1.52 0900124 Re 9/86 :

com: n21822
a2sén1 BEARING 1.19 1.08 -76 0000076 RC .

com: A25612 :
A060 FRAME, AAR 1.95 3.78 1.38 6000225 aP

Com: A82687 RACKETS POR PRAME + & RECUIRED
AS2659 BAETERY writer «120.00 is9.00 55.00 0905000 Ac

com: AS2655C aN FOR CORES
AS2687 BRACKET Be 6.38 5.80 4,40 apg0s00 ac

com: aLOO729 DEMO FOR CORES

 

CAS CASE/IH CAS CASE/TH AS cASE/IE

 


 

TECHNICAL NOTES

Files Used

IAM
IBM

IVT
VENCLS

Field Mapping/Calculations

Dealer List - Base 4 Price
Sugg List - Base 3 Price
Internal - Base 2 Price

Dealer Net - Base I Price

Cat - Part Category

PKG ~ Package Qty

PJ - Per Job Pieces Required
Data Timing

None

Data Included/Excluded

One Vendor or all, one Class or all. Up to 6 core codes can be excluded.


 

OPTs/Additional Products

OPTs - None
Additional Products - None

Required Procedures
None
Data Sorts

By Vendor, Parti


Notes:

## CHAPTER X36-21

PARTS PAD BY COMMENT FIELD

### Introduction

The Parts Pad By Comment Field selects parts by examining the comment
field for specified characters and lists inventory by part number. It can be
used to list all parts that share the same core part number. One vendor (or
all) and one class (or all) may be selected. If all vendors are printed, each
vendor's information is printed separately in order by vendor code. A
summary report is printed at the end. To print all parts, including core
parts that are not specifically excluded, see CHAPTER X36-1, PARTS
INVENTORY PAD. To print core parts only, see CHAPTER X36-20,
CORE INVENTORY PAD.

## X36-21 PARTS PAD BY COMMENT FIELD

 

### How To Run

From the Parts Report Menu (X3-6), select option 21, Parts Pad By
Comment Field. The selection screen is illustrated below.

Parts Inventory Pad 3610-003
By Comment Field

Vendor (or ALL)

Class (or ALL)
Enter comment field character string ta search on. (
All parts with matching characters anywhere in the

comment field will be included on the report.

PARTS PAD.

 

O Type the characters (words) you want to match, and press [Enter].
An example of a Parts Pad By Comment Field is illustrated below. The
characters specified were: "PARTS PAD." Note that these characters
appear in various positions in the comment field.

Note: if no parts contain the characters you entered, the report will not
print and a message will be sent to your terminal.

~~

RELEASE 2.1 ee


ABC-AC, AUTO, CONS & TRUCK CO.

BELLINGHAM, WA

Part Ruber

ntog4

10323

ui1s9

aaa

a2708

anaes

2s6u1

26713

a1zas

ayogg2

CAS CASE/TH

ABC-AG,AUTO, CONS & TRUCK CO.

BRLLINGHAN, WA

vendor Class
cas) A DEPAUL
CASE/IE

v* Totals All Vendors *


+ gorals *


Parts Pad By Conment Field
a casz/in cas

Corment Field Search String: PARTS PAD
Dealer Sugg Dealer
hist Dist Internal Nat
34.35 31,23 23.42 0002342 A

Description
BEARING 5

on Hand Rerv Bin Loe
aus

els nee

Pate 10/04/93
Time 12.13.46

page 1

3620-20
Date pare sales
Ls Prev ve yea cat Pkg Po
1

Com: TODAY I WANT 70 TEST THE PARTS PAD BY COMMENT FIELD REPORT AS YOU CAN SEE

BALL JOINT 5 5267 3.25 2.98
Com: ANOTHER QUICK TEST OF THE PARTS PAD BY COMMENT FIELD REFORT TODAY
‘TACHOMETER 2 Tare
Com
GASKET, BF23 26 2.37
Com: WILL THE PARTS PAD BY COMMENT FIELD REGORT WORK FCR US TODAY?
‘SPRING 2 sc81 3.35 3.08
Com:
MUFFLER 30 24.60 22.36 16.77 0001677 A
Com: ‘THE PARTS PAD BY COMMENT FIELD CAN FIND ALL PARTS USING CORE AI1190
BEARING 60 123 1.08 -76 0000076 &
Com: A11190

Gear 16 -11 ge000i1 A

49.45 44.95

1.77 €000177 a 9/86

9000000 A 9786
‘THE NEW REPORT IS THE PARTS PAD BY COMMENT FIELD REPORT, WHICH IS HELPFUL
2.42 0000142 A 9/26

2.32 0000231 A 9/26
11190 THR PARTS PAD BY COMMENT FIBLD REPORT CAN LOCATE CORE PART NUMBERS FAST

ar

3/86

8/85

8785

### ‘Try The New Parts Pad By Comment Field Report

Com: A11130 HERS 1S ANOTHER PART THAT SHOULD BE ON PARTS PAD BY COMMENT FIELD REPORT

1 FILTER 19 2a. 10.15 9.00

7.23 0000620 A 5/a6 3/86

Com: DIS WANTS YOU 70 KNOW ABOUT THE PARTS PAD BY COMMENT FIELD REPORT ASAP

come ok a AKL 16.08 12.76
Com: THIS 1S A TEST OF PARTS PAD EY COMMENT FIELD REPORT
CAS CASE/TE CAS cASE/TH

9-57 0000957 A

 

A summary by vendor/class follows:

Parts pad By Coment Field
a Wendor/Class Summary
Conment Field Search String: PARTS PAD

 

ary
125
225,

Dealer Net
616.57
616.57

intemal
624.78
624.74

Dealer List
4,708.16
1,704.16

Sugg List,
1,544.63
1,844.63

125, 616.57 u4.74 1,564.63 1,704.16

 

10793

AS CASE/TH

 

Date 10/04/93
‘Time 11.13.48

Page 2.
X36L0-3A,
Sales Turn
yD

00.00
<00 00

sales
Prev Yr
+00
00

00.00 00


 

TECHNICAL NOTES

Files Used

JAM
IBM

IVT
VENCLS

Field Mapping/Calculations

Dealer List Base 4 Price
Sugg List Base 3 Price {

Internal Base 2 Price

Dealer Net —_ Base 1 Price

Cat Part Category

PKG Package Qty

PJ Per Job Pieces Required
Data Timing

None

Data Included/Excluded

One Vendor or all, one Class or all. Comment field selection criteria.


RELEASE 2.1 Ne


OPTs/Additional Products

OPTs - None
Additional Products - None

Required Procedures
None
Data Sorts

By Part#


Notes:

## CHAPTER X36.22-1

TURN & EARN™ REPORT

### Introduction

This report, which was developed in conjunction with Tim Deel and the
Profit Link, shows parts inventory (summary or detail) grouped by sales
demand categories. This report encapsulates Tim Deel's innovative parts
Management strategy. With an emphasis on age analysis, parts
obsolescence and stocking control, this report provides a powerful, easy,
and efficient way of tightening your control over your inventory. You may
select one of the following:

For ALL Divisions:

= ALL Vendors (ALL Classes are included)
= 1 Vendor (ALL Classes are included)

= No detail report is available

= A composite of all vendors is included

For 1 Division:

= ALL Vendors, ALL Classes

= 1 vendor, ALL Classes or 1 class
= Choice of detail in each category

Categories

Total sales (calls and pieces) for the current and previous years are
reported in the following categories:

= Fast moving, 7 or more calls, includes zero on-hand quantities
® Active tracking, 3-6 calls, includes zero on-hand quantities

= Slow moving, 1-2 calls, does not include zero on-hand

= Inactive, no calls, does not include zero on-hand

For fast moving and active/tracking categories, the detail report sorts by:
1. Calls for the most recent 12-months in descending order (highest first)
2. Extended net amount in descending order (highest first)

3. Vendor and part number in ascending order (lowest first)


[=| X36.22-1 TURN & EARN™ REPORT ve
oo
4

For slow moving and inactive categories, the detail report is sorted by:
1. Last receipt date in descending order (most recent first)

2, Extended net amount in descending order (highest first)

3. Vendor and part number in ascending order (lowest first)

If there are no totals in a category, it is not listed on reports.

RELEASE 2.1 CU


X36.22-1 TURN & EARN™ REPORT [=]

### Installation

Menu Option

If you are on V8LAB or V8L5

O Select Apply Enhancements (X6-9) and follow the instructions on
screen. The Turn & Earn™ Report appears as an option on the
Additional Options Menu (X8).

If you are on V8LS5A or higher
The Turn & Eam™ Report appears as an option on the Additional Parts
Report Menu (X36-22).

Security

Before you run the Tum & Earn™Report for the first time, you need to
obtain your own unique installation key from DIS. This process takes only
a minute; therefore, you can wait until you have a representative on the
line before you select the option for the report.

O When you have a customer service representative on the line, select the
Turn & Earn™ option.

O A security screen displays a 12-digit number with a password below it.

Read the 12-digit number to the customer service representative and

verify it. You will receive a 6-character key.

Type the software key and verify it before you press [Enter]. The

software is permanently unlocked: you will not need to re-enter the

key. The regular DIS security gate appears.


[ X36.22-1 TURN & EARN™ REPORT co

### How To Run

If you are on V8LAB or V8LS5. From the Additional Options Menu (X8),

select the Tum & Earm™ Report. The DIS security gate is displayed.

If you are on V8LSA. From the Additional Parts Reports Menu (X36-22),
select option 1, Turn & Earm™ Report. The DIS security gate is displayed.

DIS Security Gate

SECURITY GATE x0002-001 1
Parts

Enter Division Code (
Print all divisions (/m) ..
Enter Security Code

(mdl-End job

 


X36.22-1 TURN & EARN™ REPORT [=]

C Note especially the prompt “Print all divisions (Y/N)." Your reply to
this prompt determines the next screen you will see.

Selection Screen for All Divisions

If you elect to print all divisions, the following screen is displayed:

LEE'S EQUIPMENT SALES TORN AND EARN REPORT X36M1-101
Division: a Selection

Vendor (or ALL}: ALL

Includes parts
Calls in last 12 months with 0 on-hand?

Fast moving
Active/tracking

Slow moving
Inactive

Enter-Continue

 

You can select the report for one vendor or all vendors. All classes will be
included. The categories on the left (Fast moving, etc.) are the same ones
defined by Tim Deel (see page 1). The next column (Includes parts with 0


[ «| X36.22-1 TURN & EARN™ REPORT

on-hand?) is for your information only: it cannot be changed.

Selection Screen for 1 Division

If you elect the report for 1 division (the division code used at the security
gate), the following screen is displayed:

 

LEE'S EQUIPMENT SALES TURN AND EARN REPORT x36M1-101
Division: A Selection

Vendor (or ALL): TUF
Class (or ALL): ALL

Includes parts
Calls in last 12 months with 0 on-hand? Print detail?

Fast moving
Active/tracking
Slow moving
Inactive

Enter-Continue


X36.22-1 TURN & EARN™ REPORT [7]

You can select one vendor or all vendors. If you select all vendors, all
classes are included: you cannot print a report for all vendors and just 1
class. You can select one vendor, all classes or one vendor and 1 class. See
page 1. Examples of detail and summary (recap) reports follow. Report
pages may be truncated due to space limitations of the documentation

page.


X36.22-1 TURN & EARN™ REPORT

LEE'S 2QUIPMENT SALES
WENDEN, WA

cs
lor
Ven s pC Part nunbor

Deseription

Bin

Orders avai}

‘TURN AND EARY REPORT
Detail

eneLasts Current: previous=
Receipt 02/94-02/95 02/93-02/94
Qty Oty Oty Date Calis

Pes Calls Pes et

Date 2/03/98,
Time 9.17.08

avail

Dealer extended

Noe

Fast moving: 7 calls or greater: sorted 1) current 12 month calls descending 2) extended net descending: includes 9 on-hand

TUF 17883
mF spagaiR2
Tur a0
Tur 2419CHA,
oF 12522
TUF 492653R52
uF 7605

SEAL

BOLT

Ser
SPRING

SD56
B25

ars
5P65
B27
AG

Active/tracking: 3-6 calls; sorted 1) current 12

om
35646
rsa?
11628
a1iges
487374R1
485452R2
146696
anieda
Si 7645R12
18358
49826
495032R1
asus
apn07eR2
a9sa25Ri
72276
40035

$7ir

$ 5386

‘SPRING
HOSE
FILTER
GASKET
casxzz
nor

GUARD

OIL PILTER
BELT
‘COLLAR
BIST CAP
cuaMP
PIVOT
oRING
SPRING
GEAR
CABLE
BEARING
-IN

POINT

AL
RACKD
3eroP
FILE
5057
8-26
3.26
222
BB
Pelt
vasa
BOARD
B28
6B622
cis
B28
2F86
sc22,
a
pert

4 3 336 200 2.97

ico +38
50 a3 .23
11 10 386 5.56
20 2.05
2 4 486 3.50
to 5 386 -00

Li.ee

+00
11.80
72.18
41.00
14.00

+00

calls descending 2) extended net descending; includes 9 on-hand

486 2.38
388 12.68
2.28

386 2.71
2.01


6.49

2.95

5.28

2.98

3.22

aan

1.87


1.78

15.68

10.63

13.03


2.62

Slow/moving: 1-2 calls; sorted 1) last receipe date descending 2) extended net descending: excludes 0 on-hand

495619295,
482062R92,
31843
49672102
ali219
m21
30834
10329
a90473R1
27560
mara


vex

Door umerruran

O calls: sorted 1)

522062
11e24
425476
34a
10726
73153
16792
azazie
828477
24auTr
301
41245
cea
70053

prs
BEARING
‘BREATHER
CONDERSR
CUP W/NUT
SEAL
BUSHING
BALL SOIT
BLADE

@ RING
‘SPROCKET
LINK
BUSHING

last receipt date descending 2) excended net

BUSHING
SPACER
BEARING
SPRING

OD FILTER
BATTERY D
BUSHING

B28
B27
50s2
3-28
eci62
SA52
scez
5867
B27
60518
a?
AL
AT

sP5a
7085

aa
Bazi.
SF63
m2

586 38.01,
566 6.16
386 7.00
326 le
386 40
1.56

2.32

4.77

7.51


+00

4.57

7 excludes 0 on-hand

14,10
63.40
47.25
13.55
12.06
4.08
n138
61.95,
21.12
37.55,
16.05
10,86
10.29
4.51
89.50
78,40
74.41
65.15
5.78
00

190.05
36.96
35.00
21.60

3.20
38.72
16.24

8.25

7.8L

5.83

-00
-00
-00
Page}
x36M1-302

Extended
sates

 

Se


X36.22-1 TURN & EARN™ REPORT

LEE"S EQUIPMENT SALES ‘TURN AND EARN REPORT pate 2/03/95 Page 2
Detail Time 5.27.05 x36M1-301

asters s=Current== <=Previow: Avail
Receipt 02/94-02/95 02/93-02/96 Dealer Extended Extended
Bescription ey Date Calis Fes Calls Pee wet, Net Sales

515700RS
AAOT95
10839
70523
49274881
ATE34
12056
49s197RG
34087
azses4
4gs203n91
s19819R2,
74298
ag0c74na
0563
17878
495170R2
ara79
17598
492479R2 :
6197 38 . : :
19838 702
70213 R83
allege S075
10326 6372
nasa 62331
495525R1 B28
am Ra
an24g1 SE6i
10731 5R76
49ss22R1 B28
17597 7059
30613 5A83
48769781 26 :
se929en1 B26
490475RE, 3-27
10956 ses3
17877 SE57
7623 p61
499399R BELT SE-6
49859 CLAMP =D
316682 acas
Alaa BOWE 5885
33261 GASKET opin
a9si92R3 GEAR 4-28
36642 SEAL 6c162E
246696 PILTER PIL-C5
AISS2 © RING esi
409292R1 SUPEORT B26
12778 SPRING scst
eagogaR2 BELT SE+6
33260 WASHER spsic
2a6361R1 SPRING 3-28
Alna23 ‘SEAL 5891
4961S2R2 BRACKET 3-28
A7090 OTL SEAL 313
ADSS46 sur

29341181 BAR 3-26
149 GASKET pas
16202 conan, e5i2a,
yaaa e132ic
41209 3e33
23150 68620

   

 

PDH PUMP OHM HEY EHUD HYD OHHH EUR PUD OPH POE PAH ODE OHH OY HEY DD

 


[2] X36.22-1 TURN & EARN™ REPORT

Fields & Definitions (Detail Report)

Ven
Cis
Sup

RC
Part number
Description
Bin
Order

Cc

Qty
Avail Qty
Last Receipt
Qy
Date
Current; Previous
MM/YY-MM/YY

Calls
Pes

Dealer Net
Avail Extended Net

Extended Sales

3-character vendor code.
1-character class code.

Y or blank. "Y" means the part has
been superseded and there is a
superseding part number on the
master part record.

1-character return code.
Self-explanatory.

Self-explanatory.

First bin location.

Order code. A=Automatic,
C=Combined, M=Manual.
Quantity on order.
Available quantity.

Quantity received most recently.
Date most recent order received.

Month/Year range of current and
previous years,

Number of calls for the part in the
current/previous years.

Number of pieces sold in the
current/previous years.

Dealer's cost.

Available quantity multiplied by
Dealer Net.

Pieces sold in the current year
multiplied by Dealer List.


X36.22-1 TURN & EARN™ REPORT

LBE'S RENTAL ZQUTPNENT INC.
LYNDEN, WA a

cs
1urR
5 pC Part number

aisz
71139
Pog.
491762R1
49176381
17603
A7669
Ag613
27156
49176181
a7466
26713
515¢40R1
49385,
aiiz32
499429R1
490663R1
4935¢3R1
492710R)
32995
atiz08
7075,
razae
0782
16218
71466
sogoeocn,
49258
ean
ataaeo
x7409
wage
M326
NasT

Pac
Razz
v620
vee0
2285
48350281
480922K2
405673R1
496006R2
s21752R92
7078

s
A
s
s
s
a
a
a
a
s
a
a
s
a
a
s
s
s
8
A
A
A
A
A
A
a
s
A
5
A
a
°
°
°
s
°
s
s
s
s
°
5
°
s
°

Description

WASHER
SPRING
SPRING
sacTron
SRCTION
SEAL
RING
© RING
o RING
SECTION
© RING
GEAR
RING

BOLT
BAR
GASKET
RETAINER
PACKING
GASKET
SPAL RING
‘SEAL
SNAP RING
asKer
RING
FUSE
cua

as
e162
a6
8-27
8-27
6BL3B
ecis2F
62338
602230
B27
ep21

B28
SD7s
eBan

crs

B27
FILE
B27
se76
5064
6c162E
splice
op51
easic
cae
GR-10
onan
oR-8
a1
scLiza
a6

a6

aT

Ad
AB
aT
>
as

wet

‘TORN AND EARN REPORT
Detail

enetast:
Order= Avail Receipt

e ary

Qty Date calls

Date 2/09/95
‘Dime 9.17.09

seCurrents= ==Previous=
02/94-02/95 02/93-02/94
Fes Calls Pes

Dealer

Page


x36m1-301

avail
zxcended

extended

Sales

RFI FASF 914

+00
09
00
+00
-00
-00
08
+00
+00
00
00
-00
00
00
00
90
00
-00
00.
+00
09
-00
+00
+00

co
-00
+00
00
09
00
+00
+00
+00
-00
+00
+00
-00
00.
+00
00
00
00
-00


The corresponding recap, which is illustrated below, always follows the detail report. If you do not request

detail, only the recap, or summary, is printed.

Fast moving = 7 calls or greater:

vendor

TUP SALES ‘BR:

Vendor totals

TUF

cals

Fast moving
Active/tracking
Siow moving
Inactive

Vendor totals

Past moving
Ackive/tracking
Slow moving
anactive

Grand torais

‘TURK AND EARN
Bivieion: A

ext. Nee

150.59
681.39
333.96

3,405.97

4,571.84

150.54
681.37
333.96

3,405.97

4,571.84

 

X36.22-1 TURN & EARN™ REPORT

### Report

Summary

Active/tracking = 3-6 calls:

.

3.3
14.9
7.3
7a.s
100.0

3.3
149
13
74.8
100.0

Slow moving = 1-2 calls:

Lines

3.8

Daze 2/09/95,
Time 9.17

Inactive =

ext.

sales

239.18
302.63,
185.18

-00
708.93

138.15
381.63
186.15

+90
706.33


2 calla


19.7
54.0
26.3
“0
200.0

19.7
54.0

 


X36.22-1 TURN & EARN™ REPORT [=]

TECHNICAL NOTES

Files Used

IAM
IBM

Field Mapping/Calculations

Categories :

Total sales (calls and pieces) for the current and previous years are
reported in the following categories:

= Fast moving, 7 or more calls, includes zero on-hand quantities
= Active tracking, 3-6 calls, includes zero on-hand quantities

= Slow moving, 1-2 calls, does not include zero on-hand

= Inactive, no calls, does not include zero on-hand

Data Timing

None


X36.22-1 TURN & EARN™ REPORT

Data Included/Excluded

One Vendor or all, one Class or all.

For ALL Divisions:

ALL Vendors (ALL Classes are included)
1 Vendor (ALL Classes are included)

No detail report is available

A composite of all vendors is included

For I Division:

ALL Vendors, ALL Classes

1 vendor, ALL Classes or 1 class
Choice of detail in each category

OPTs/Additional Products

OPTs - None
Additional Products - None

Required Procedures

None


X36.22-1 TURN & EARN™ REPORT

Data Sorts

For FAST moving and active/tracking categories, the detail report is
sorted by:

1) Calls for the most recent 12-months in descending order (highest first)
2) Extended net amount in descending order (highest first)

3) Vendor and part number in ascending order (lowest first)

For SLOW moving and inactive categories, the detail report is sorted by:
1) Last receipt date in descending order (most recent first)

2) Extended net amount in descending order (highest first)

3) Vendor and part number in ascending order (lowest first)


Notes: a


RELEASE 2.1 ~~

## CHAPTER X36.22-3

INVENTORY QUANTITY DROP REPORT

### Introduction

The Inventory Quantity Drop Report lists all parts that dropped below a
user-specified quantity during the past day.

Note: This report will not be valid for the current day until Parts End
of Day is completed.

### How To Run

From the Additional Parts Report Menu (X36-22), select option 3,
Inventory Quantity Drop Report. Pass through the security gate. The
following screen appears.

NW EQUIPMENT SALES Inventory Quantity Drop Report X36M3-101
Division: A Selection

This report will list all parts that had an on-hand quantity
Grop below the quantity specified below. this information is
gathered during Parts End-of-Day and is stored on the system
vnti2 the option to purge is selected below for that one day.

042696


[2] X36.22-3 INVENTORY QUANTITY DROP REPORT co

CO Enter the date that will appear in the report.

 

 

Enter a quantity. Any part that dropped below this quantity during the
past day will be included on the report.

 

 

CO To purge the information used to generate the report, enter a "Y" in the
purge field.

Nw SQUIPHENT SALES Inventory Quantity Drop Report pate 5/02/96 Page 1
BELLINGHAM WA mime 13.26.12 23608-2021
Reporting parts whose quantity dropped below on 05/02/36
Deseriptien

49147922
492082291,
7153
003738

cas
cas
cas
cas
cas
cas
cas
cas
cas
kas.

 

LL

## CHAPTER X36.22-4

PART SALES FOR WHOLESALE CUSTOMERS

### Introduction

This report has data only if you are using Part Sales History and you
identify wholesale customers by placing a "W" in any of the 10 positions
of the sort code field in Receivables Maintenance. Part Sales History is
accumulated from the time the Part Sales History OPT is turned on. If you
have been using Part Sales History for a while, you can place a "W" in one
of the sort code fields to identify customers at any time, and the report will
list information from the time when the OPT was first turned on.

For any month of the current or previous year, this report lists:

= Current Year-To-Date (YTD) Sales Total and the corresponding YTD
Sales Total from the previous year

= Last year's total sales

= Current month's total and the same month last year

‘You can exclude customers for whom there have been no sales in the
month/year requested.


[2] X36.22-4 PART SALES FOR WHOLESALE CUSTOMERS

### How To Run

From the Additional Parts Report Menu (X36-22), select option 4, Part
Sales for Wholesale Customers.

Selection Screen

BOB'S TRACTOR COMPANY Wholesale Parts Sales Summary X36MO1
Division: A Selection Parameters

Select Data for Wholesale Parts Sales Report

Any month of the current or previous year can be specified.

Month/Year (MM/Y¥) : 8/96

Include customers with Zero Sales? : N (Y/N)

Output Queue : PRTOL

 

If you want a month/year other than current, enter a 2-digit month and
year.

If you want to include customers regardless of whether there were any

## X36.22-4 PART SALES FOR WHOLESALE CUSTOMERS

sales, change the default to Y (Yes).

The printer associated with the user will be used by default.

Sample Report

BOB'S TRACTOR COMPANY Monthly Parts Seles to Wholesale Cuscomers Date 8/12/96

As of: 02/96 Time 13:87:56 36ME-28

Yeor-Te-Date Corr, YTD Amt. Total Sales Same Honth
Mame Sales Total Last Year Lest Year bast Year

ADAMS, WILLIAM, 512.89 411.22 1,003 56 202.08
BELL, SUSTE 696.76 105.31 3,450.33 3,263.07
GRADY, LEROY 46.78 79.58 340.02, - 21,59
‘TaOSHORS Axe 593.48 100-01 672.04 96.72

>> Grand Totals >> 2,849.9, 696.12 5,464.94 1,522.48

 


Notes:

## CHAPTER X36.22-5

REMANUFACTURED PARTS INVENTORY PAD

### Introduction

This report works by comparing parts in inventory with parts in the price book
and listing the ones that have remanufactured (reman) information attached.
Reman parts from all classes are included. New part numbers that have reman
parts are not listed. Primary core part numbers are referenced but not listed on a
separate line. Since cores are kept in a separate class, run a Parts Inventory Pad to
get a list of them.

### Contents

ENTRANCE SCREEN...
Sample Report.


X36.22-5 ¢ REMANUFACTURED PARTS INVENTORY PAD RELEASE 2.1

### Entrance Screen

O From the Additional Parts Reports Menu (X36-22), select option 5.

Additional Parts Report Menu

 

COMMAND MENU: X36M
(c) DIS Corp.

 

1. Turn and Earn Report

2. Group Inventory Replenishment Report
3. Inventory Quantity Drop Report

4. Wholesale Customers Sales Analysis
S. Remanufactured Parts Inventory Pad

23. Return to Parts Report Menu

Ready for option number or command
=> 5

 

 

The selection screen is the same as the Parts Inventory Pad (X36-1):

Remanufactured Parts Pad Selection Screen

 

A&R EQUIPMENT SALES REMANUFACTURED PARTS PAD 3610-001
SELECT

Vendor {or ALL)

Class (or ALL).

 

Core Codes to Exclude........ 2.
PRINT
Dealer List Price............. y
Suggested List Price.......... N
Internal Price..............., N
Dealer Net...... 22... x
Cmdi-Cancel cmd2-Select Divisions Enter-Continue


1934208ca

31934212c1
1934224¢1,
193so62c2

A&R EQUIPMENT SALES
LYNDEN, WA

Part Nunber
1934206c1,

CAS CASE/TH

X36,22-5 ¢ REMANUFACTURED PARTS INVENTORY PAD 3

Sample Report

The report lists remanufactured parts only. New parts that have associated reman
parts are not included. The associated core part number is referenced but the part

number itself is not listed as a separate line. An example of the report is illustrated
below.

Sample Remanufactured Parts Inventory Pad

         
  

 

 

     
  

 

 
   
      

    

Remanufactured Parts Inventory Pad Bate 9/16/97 Page 2

CASE/TH cas! Time 14,55,36 3610-28
Dealer Dealer Date Date == Sales ==

Description On Nand Rerv Bin Lee List Net Cis Uct le F 96 97 ct Pkg PY

REN 18 1629.65, 0213779 & 9/97 rod

REAN: § 1429.65 CORE: $ 200.00 coRE # 19342071

Ord: MARKK $2 Order Total: 2

REKAN POMP. 20 1600.83 0111767 A Boa

REKAN: $ 1400.83 CORE: § 209,00 CORE # 1934209C1

Ord: MARKK Ss 3 Order Total: 3

REMAN PUMP. 10 1018.35, 0071099 a tot

REMAN: $ 968.35 CORE: $ 50.00 CORE ¥ 2934223¢1

REMAN PUMP. oars 1007, 0070329 a ,oL

REMAN: § 957.31 CORE: $ 50.00 core # 1934215¢1

REMAN-HON 16 747.81, 0047588 A. 2042

 
 
 
 
 

  
 
  

 
   

REN. MOTOR 3898.52
REMAN: § 3498.52 CORE: $ 400.00 CoRR # 1971581C1

 
     
  

CAS CASE/TH CAS CASE/TH CAS CASE/TH Page 2


X36.22-5 » REMANUFACTURED PARTS INVENTORY PAD

Notes:

## CHAPTER X37-1

REPRICE PARTS

### Introduction

Reprice Parts offers several different methods for changing the prices of
parts in your inventory. Reprice parts changes prices in one division at a
time and can be run for a specific vendor and class or all vendors or all
classes. See also, CHAPTER X3-7, AUTOMATIC PRICE UPDATE
MENU.

Note:

Parts can also be repriced from a price book. See PRICE TAPE
UPDATE, Chapter X37-2.

 

IMPORTANT: Backup your parts files before Starting this job.
The options for repricing are:

REPRICE BY FIELD-allows you to base prices in one field on a
percentage of prices in another field. For example, reprice all intemal
prices to equal 110% of dealer net. Requires “Automatic pricing"=Y in
Vendor/Class Configuration (X38-1).

REPRICE BY VALUE-allows you to price parts differently according to
their value. For example, parts with a suggested list of less than $100,
dealer list will equal 110% of suggested list. For parts over $100 dealer list
will equal 105% of suggested list. Requires "Automatic pricing"=Y in
Vendor/Class Configuration (X38-1).

REPRICE INDIVIDUAL PRICES-a fast way to changes prices on a
screenful of parts on a part-by-part basis. Parts can be repriced regardless
of setting of “Automatic pricing” field.

REPRICE BY DIRECT SHIP-reprice parts for a particular direct ship
pricing program. Parts can be repriced regardless of setting of "Automatic
pricing” field.


[| X37-1 REPRICE PARTS Co

### How To Run

From the Automatic Price Update Menu, select option 1, Reprice Parts.
On the entrance screen, type the number of the option you want to use to
reprice your parts.

REPRICING BY FIELD (option 1)

This job reprices only parts in classes where "Automatic pricing"=Y in
Vendor/Class Configuration (X38-1). The screen below is an example of
the Reprice By Fields screen.

ABC-AG,AUTO,CONS & TRUCK CO. Reprice Parts x3710-301 1 (
All Price Fieids

vendor Or ALL :
Class Or ALL :

New Price number or old price X / percentage

Dealer List (4) =
Suggested List (3)=
Internal (2
Dealer Net aye

11000
10000

goo
10000

x
x
x

Cmd1-End job Cmd3-Return to reprice options.

 

LL


X37-1 REPRICE PARTS [2]

 

Type the vendor code or ALL.

O Type the class or ALL.

O When you first see this screen, the fields are set to 100% of themselves:
no change will take place even if you press [Enter] by mistake.

To reprice a field change the bases, the operator (either an "X" for
multiplication or a "/" for division), or the percentage of the old price.

 

 

 

 

 

If the Average Costing OPT (X6332-7) is on, Reprice by Field enables
you to reprice the average cost for 1 or all vendors and 1 or all classes.

In the example shown above, the Dealer List field and the Internal field
will be repriced. Dealer List prices will change to equal 110% of
Suggested List (field 3) and Internal prices will be repriced to equal 90%
of Dealer Net (field 1). Dealer Net and Suggested List will not be repriced.

O After making the desired changes you must press ENTER to start the
feprice parts job. CMD 3 will return you to the repricing options
screen, without starting the job. All fields on the screen must be filled
out before pressing [Enter].

When the job completes, the Reprice Exception Report prints. The report
shows the percentages and bases used to reprice parts.


a | X37-1 REPRICE PARTS

REPRICING BY VALUE (option 2)

This job reprices only parts in classes where "Automatic pricing"=Y in
Vendor/Class Configuration (X38-1). Repricing by value allows you to
price parts differently according to their value.

The screen below shows an example of the reprice by value screen.

A & R EQUIPMENT SALES Reprice Parts x3710-201
Based On Value

Vendor Ox ALL : ALL
Class Or ALL : ALL

Enter price field to be used as base for repricing. Enter 4 for Dealer List,

3 for Suggested List, 2 for Internal, or 1 for Dealer Net. (
Base Field: 3

Enter price field to be repriced. Enter 4 for Dealer List, 3 for Suggested

List, 2 for Internal, or 1 for Dealer Net.

Reprice Fiela : 4
Enter dollar values (eg. 1234 = $1234} and percentages (eg. 12500 = 125%)
mark up/down prices. The reprice table must be in increasing value order. Any

unused entries should be at the end of the table and filled with ‘9's.
Range From Less Percent
or Equal Than xX /
300 10000
300 500 10000
500 1000 10000
1000. 99999 10000
39999 99999 10009

Cmal-End job cmd3-Return to reprice options

 

 

 

 

Type the vendor or ALL.
O Type the class or ALL.

 

RELEASE 2.2 LL


X37-1 REPRICE PARTS [=]

O Type the number of the field to be used as a base for repricing.
QO Type the number of the field to be repriced.
O Fill in the ranges of base price values to be changed.

Ranges are defined as From or Equal to a dollar value but, Less Than a
second dollar value. Do not use decimal places. Ranges must be in order
of increasing value. Unused ranges should be at the end of the table and be
filled in with ‘9's.

 

C1 If you want to divide a value by the percentage, replace the
multiplication symbol ("X") with the division symbol ("/").

O For each range of prices, type the percentage of the base field you
want the reprice field to equal.

O When all fields are filled out correctly, press ENTER to start the job.

When the job completes, the Reprice Exception Report prints. The report

shows the vendor and class, base and reprice fields, and the ranges and
percentages of the reprice.

REPRICE INDIVIDUAL PARTS (option 3)


his job reprices parts regardless of the setting of the "Automatic pricing”
field in Vendor/Class Configuration (X38-1).

O Type a division code or ALL.

Type a vendor or leave blank and system will default to your first
vendor.

O Type a part number or leave biank and system will default to first part
number for specified vendor.

 

 

 

 

## X37-1 REPRICE PARTS

 

O Press ENTER.

The following screen is an example of the Change Individual Prices
screen.

 
  

    

ABC COMPANY REPRICE PARTS
Division E CHANGE INDIVIDUAL PRICES

x3710-402

       
   
    
     
      
      
     
     
     
    
   
      
      
    
    
    
   
 
 

vendor part Part Dealer Suggested Internal Dealer

Code Number Description bist List Price Net

BHS sP008 GIB 274 249 157 174

BHG sP009 BOTTOM SLIDE 277 252 188 176

BHG SP010 PUSHER WELDMENT 3638 3307 2084 2315

BHG SP044 CLEVIS PIN 1185 1050 662 735

BHG SP050 FRAME WELDMENT 26358 23962 15096 16773 (
BHG SP105, HYD C¥L VENDOR L 20306 «= 18460 11630-12922 .
BHG SPi16 SHAFT ,VICTOR FL 10885 9895 6234 6927

BEG SP166 PUMP,7 GPM 29688 © 26989-17003 18892

### Beg Sp172 Spider Coupling 611 585 350 389

BEG $P188 FRAME WELDMENT 37310033918 = 21369-23743,

BHG SP191 PRAME WELDMENT 32436731243 -19683 21870

BHG 12345 WIDGET 1100 2000 630 700

wos 100 1-3/8 FRT SET 2 19250-17800 181313125

wos 10003 $0 ETC END GEAR 21780 «19800 «= 1336514850

  

Begin Next Page with Vendor Code WDS Part Number 10050
Press Cmdl to end job Cmd2 for previous screen md? for repricing options

     
 

 

 

 

Displayed on this screen is a list of parts, beginning with the vendor
and part number you specified. Move the cursor to any price field you
wish to change and type the new price. Press FIELD EXIT.

CO Change the vendor and or part number to start the next page if you
wish. To change vendor, type new vendor code and leave the starting
part number blank. The next page will begin with the first part number

 


 

for that vendor. You must press ENTER when finished making changes
on each page. When you have finished making all changes press
ENTER and then CMD 1 to end the job.

REPRICE BY DIRECT SHIP (option 4)

Note:

Before repricing by direct ship you must build a Direct Ship Price

Book when running a Price Tape Update (X37-2). Additionally ali

parts qualifying for a specific direct ship program must have the same
class code.

 

This job reprices parts regardless of the setting of the "Automatic pricing"
field in Vendor/Class Configuration (X38-1).

O On the first screen type the vendor. ALL is not allowed.
OO Type the class that has parts for this direct ship program.


—

| 3 | X37-1 REPRICE PARTS

The following screen is an example of the Inquire/Reprice Screen.

ABC COMPANY REPRICE BY DIRECT SHIP X3710-701
Division: E INQUIRE/REPRICE

Part number: MA22670

Level Description Dir.Net Sug. List Current prices
o1 ory prise 40.63 54.17 Dlr.net
Internal 40.63
Sug. List 59.59
Diz.bist : 119.18

Ord3-Reprice Options Home-Top of List Roll-Page

Reprice(¥/N) Percent Base
L-Dir.Net N iooces0 1. (
2-Internal N 1¢00000 1
3-Sug List N i90c900 3
4-Dir. List N 1060000 3

 

Do not overwrite part information if the Direct Ship pricing record has
blanks in the respective fields. Also, leave the Description field intact on
the part unless the part already has a blank description.

### Fields & Descriptions

Part Number

Level

Description

Dir.Net
Sug.List

Current prices


When the screen appears the first part in the
direct ship price book and the selected
vendor/class is displayed,

Identifies different levels in different direct
ship programs,

Direct Ship Program level. If this class of
Parts is eligible for more than one direct ship
program, all the Programs will display. If the
first program has 3 levels (like on the
example screen) then the first level of the
Second program wil] be level 04. The
description of the Second program will
identify the Program and the level.

Dealer net for each level of each Program.
Suggested List for each level of each
program.

How this Patt is priced in your inventory,

REPRICING BY DIRECT SHIP


 

 

 

To view all program levels for a part (if more than one page is
available) use the roll key to page and the home key to return to the top
of the list.

 

If you inquire about a part number that js not in both the vendor/class
and Direct Ship price book, you will get an informational message.

0 When you decide at what level to reprice parts jn this class, fill in the
options on the lower half of the screen. You cannot reprice individual
parts. The choice you make will affect all parts in the class.

Level - Type the number indicating the level of repricing.

Reprice (Y/N) - type Y (yes) or N {no) to reprice current fields.

Percent - If repricing 4 field type the percent of the direct ship field the
repriced field will equal.

Base - Type | to rep ice based on a percentage of Dir.Net. Type 3 to
reprice based on a percentage of Sug.List.

 

(1 Press ENTER when the options are complete. If you are not repricing
any fields you will receive a message to that effect.

‘When the job completes, the Reprice Exception Report is printed. The
report shows the vendor and class that were repriced, the level of
repricing, and the bases and percentages for each field that was repriced.
The exception report also lists parts that were not repriced.

## CHAPTER X37-2

PRICE TAPE UPDATE

### Introduction

Price Tape Update allows you to update part prices and other part
information with the most current data from the manufacturer. The term
“price tape" applies whether the update is furnished on diskettes or on tape
cartridges. An alternative is to create (or update) a price book first, then
use Price Tape Update to update your inventory from it.

The price tape updates parts company-wide. If you have more than one
division, you only need to run the price tape one time.

Only parts in classes where "Automatic pricing"=Y will be updated. If the
update tape carries supersession information, then parts updated by the
Price tape will be updated with supersession information.

See also, CHAPTER X3-7, AUTOMATIC PRICE UPDATE MENU.

FYI - The system proceeds with the Price Tape Update in the following
order:

1. Looks at the class assigned to the part in Parts Posting & Maintenance
(X3-2).

2. Looks at the pricing information for that class in Vendor/Class
Configuration (X38-1).

3. Uses the percentages and base codes from Vendor/Class Configuration
to calculate new prices for the part. If a base for a price used in
Vendor/Class Configuration is not on the Price Tape, the corresponding
price is set to zero.

4. Moves the bases assigned in Vendor/Class Configuration to the part
record in Parts Posting & Maintenance. It is possible to assign different
bases on the part master record (X3-2) from those used by the part's
class in Vendor/Class Configuration (X38-1); however, the system
relies on X38-1. In this step the system actually forces the part master
record to conform to the Vendor/Class setup.


[=] X37-2 PRICE TAPE UPDATE

### Direct Ship

If the price tape you are using carries Direct Ship program information, the
Price Tape Update will give the option of building a Direct Ship Price
Book. This Price book cannot be displayed or printed.

The Direct Ship Price Book will contain records only for parts you have in
your inventory. This will limit the amount of space needed to store the
price book. Direct Ship records will be in a file named, DIRu.ven (u is
your user ID and "ven" is the vendor code of the price book.)

The Direct Ship Price Book includes the following fields:

- Weight

+ Retum Code

¢ Package guantity

- Part category

+ Multiple

The system will overwrite whatever is in these fields regardless of the
OPT setting for price update fields. The description is also overwritten.

### Quantity Break Price Tapes

If your price book contains quantity break records, you will be provided
with two price tapes. One will be the standard price tape. It will be labeled
with the Manufacturers Name. The other price tape will specifically
reference quantity break records.

Apply the standard price tape first. The tape referencing quantity break


X37-2 PRICE TAPE UPDATE [2]

records should be applied over the first price tape. It will automatically
update your inventory with quantity break records. The rest of this chapter
tells how to run the Price Tape Update.

RUNNING THE PRICE TAPE UPDATE :

IMPORTANT: Before starting this job, backup your parts files.

From the Automatic Price Update Menu (X3-7), select option 2, Price
Tape Update. The entrance screen is displayed.

Automatic Price Update 3720-001

 

Device to be used (S1/M1/TC/PB) :

$1 - first diskette slot
Mi - first magazine drive
TC - tape cartridge

PB - existing price book

 

From diskettes or tape:

O If you are using a machine with one slot, type S1.
If you are using a magazine drive, type M1.
If you are using a tape cartridge, type TC.

## X37-2 PRICE TAPE UPDATE

 

O Insert the diskette, magazine, or tape cartridge and press [Enter].

OD You will see a message that the RESTORE procedure is running. On
the next screen, the title of the price tape, the date the prices are
effective and the release level of the tape are displayed.

If this price tape contains direct ship records, you will have the option
of building a direct ship price book. The number of adjacent blocks
required for the price book will be displayed.

1 Type the vendor code for this price tape. If the option is presented, type

¥ (yes) or N (no) to build a direct ship price book. Choosing Y will

delete any existing direct ship price book for this vendor. Press ENTER
two times,

Each diskette will be processed sequentially. If you do not have a

magazine drive you will be prompted to insert diskettes as required.

 

 

 

 

Note:

AS/400 only. You may receive a system message, SYS-3777 with
options 0123, regarding diskette file @.PRC. This simply means the

file could continue to the next diskette, and the message is repeated for }
all but the last diskette in the set. The message occurs about 2 minutes
after the diskette is loaded. Take option 0 (zero) to continue the price
tape update.

 

From price book:

If you are updating from a price book, type PB and press [Enter]. A vendor
code prompt appears, which will be followed by a message, "Automatic
price update from price book is running."


X87-2 PRICE TAPE UPDATE [=]

### Reports

Whether the update is from diskette, tape, or price book, Price Tape
Update produces four reports:

 

 

No Update Record Found For Part Record

Parts on this report are in your parts file, but the number is not on the price
update tape. Parts listed here are not updated. Parts manufacturers do not
carry all their parts on every update tape.

 

 

C1 Parts in Non-Update Class

Parts on this report are in your parts file and on the price tape. However,
they are in a class configured with an N for no automatic update. If you
want these prices to be updated, change the configuration and run the tape
again.

 

C] Invalid Class or Vendor Default Class Missing

The parts on this report are either in a class that has been deleted or no
default class is configured for this vendor. Check parts appearing on this
report for repricing. Make necessary changes in vendor/class
configuration.

 

 

 

 

Parts Supersession

The Parts Supersession Report provides information on parts that
supersede or are superseded by another part or parts. The supersession
indicators for single (S) and multiple supersession (M) appear on this
report,

S means that the part supersedes or is superseded by one part. M means
the part supersedes or is superseded by more than one part.

### 87-2 Price Tape Update

 

The price update tape does not set up new records for superseding or
superseded parts that are not in your inventory. If you have part A in
inventory, and on the price tape it is superseded by part B which is not in
your inventory, the price tape will add the supersession indicator to part A.
No information will be available on part B. To add information on part B,
add it to inventory in Parts Posting and Maintenance. Then nun the price
tape again and description and prices will be added.

On the Parts Supersession Report, you may find the following listing:

Part wunber Superseded By Supersedes
derzizen3 16321204

renz2izMd enzazan2

 

The part numbers in column 1 are already in your inventory files. The part
numbers in columns 2 and 3 may or may not be in your inventory files;
however, if they are, they are also listed in column 1.

In the progression above, M2 was the original part number. It is no longer
in your inventory files (it is not listed in column 1). M3, which is in your
inventory files, has been superseded by M4. M4 is also listed in column 1;
therefore, it is also in your inventory files. You only need to add part
numbers that are in column 2 but not in column 1.

## CHAPTER X37-3

DISPLAY/PRINT/CHANGE PRICE BOOK

### Introduction

Display/Print/Change Price Book allows you to display any price books
loaded onto the computer (X37-4). Also, you can print out a copy of the
price book or make changes to current prices. Customers that request
pricing of parts frequently can have their own copy.

Core information is displayed and printed. New parts reference
remanufactured (reman) parts. Reman parts show prices of the reman part
and its primary core and reference the primary core part number. Primary
cores reference alternate cores, if any. For more inofmration about reman
parts see Configure Vendor/Class (X38-1).

Before the price book can be printed or displayed, it must be loaded onto
the computer. See Chapter X37-4 CREATE/UPDATE PRICE BOOK for
details.


X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK fo

 

### How To Run

From the Automatic Price Update Menu (X3-7), select option 3,
Display/Print(Change Price Book. The Price Book Selection screen
appears, as illustrated below.

ARR EQUIPMENT RENTALS | DISPLAY/PRINT/CHANGE PRICE BOCK 3730-101 1
Division: A Price Book Selection
Price Book Name Description
ACASEIH CASE IH W/DIRECT SHIP PRICES-DISK #1/16
cUOMMINS cuMmrNs

THERMO ‘THERMO
Z.HARLEY HARLEY DAVIDSCN TEST BOOK (

To select a Price Book enter any character in front of the book name.

Gmdl-End jos = Cmd2-Display © Cmd3-Print © Cmd4-Set options  cmd5-Change

 

Place any character next to the price book you want to work with. DO
NOT PRESS ENTER. You have the following options:

Cmd2 To Display
Cmd3 To Print

oe


X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

Cmdé4 To Set Options
Cmd5 To Change

Each option is discussed on this and the following pages.
Cmd2-Display

When you press [Cmd2], the first page of the price book is displayed.
Direct ship records, as well as weight and category, will also display for
price books with two 2 prices. A sample screen from a price book is
illustrated below.

ASR EQUIPMENT SALES DISPLAY PRICE BOOK 3730-301

Division A
Part Number
AL0000
10001
10006
10007
410031
a1¢040
Aloogs
10058
10059
10060
10061
10062
10063
A10066
10094
410222
A10223
ALO124
10143

Case test book
Description
SNAP RING 4.84
CONE R 12.76
NUT 18.46
GEAR 33
GASKET 50
GASKET 50
ROLLER -50
HYDR HOSE 65
ELEMENT 95
SHAFT 54
SPIDER-PTO 48
OIL SEAL 53
SNAP RING -12
SPACER 46
BEARING 8 +23
PIN 55
PIN “7
GEAR 39.88
CABLE 10.29

Enter part number to begin next page; A10143

mdi-End Job

Sug.List Dlr.Net Rtn Pkg Mlt Weight
3.
9%.
12.


22.
13.
1.

342.

zi.
5.
3.
a
23.

s7
08

cat
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q
Q


X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

 

The first part number from the next page displays in the "Enter part
number to begin next page" field.

O To display the next page, press [Enter].

O To skip pages and display a particular part, type the part number at the
“Enter part number to begin next page” prompt, and press [Enter].

O To return to the Price Book Selection screen, press [Cmd1].

Cmd3-Print

You can print a copy of the price book for the parts counter or for
customers who frequently request part price information.

C1 To print the price book, press [Cmd3]. The Set Print Options screen
appears, as illustrated below. Defaults for Display/Print/Change are
established using Cmd4-Set options. The options entered on this screen
will only be good for this print.


X37-3_ DISPLAY/PRINT/CHANGE PRICE BOOK

ABR EQUIPMENT SALES PRINT PRICE BOOK 3730-201
Division: a Set Print Options

Name of Price Book MANEOOK
Description MANUFACTURER'S PRICE BOOK
Title Quality is our business.

% Adjust = Print = Title

Dnr.List 120 list
Sug.List Sug List
Internal

Dir.wet. cost.

Lines per Page (1 to 112). .
Lines per Inch (4/6/8) . . .

Chars per Inch (10/25) . . .
Nurber of Copies (1 to 99}

Enter options for this print ONLY.

Qmdi-return to the menu Enter-print price book

For example, ABC Company has a customer, DEF Company, that is
charged at 105% of Manufacturer's suggested list. When the price book is
printed for DEF Company, suggested list is printed with the 105% mark
up in the suggested list column. This way, the DEF Company knows what
the cost of the part is to them, and list price is available for the customers
of DEF Company. DEF Company sells parts to their customers at 110% of
List. The above screen reflects these choices.

If the price book is to print on the system printer, you may leave the other
defaults unchanged.


[ «| X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

Cmd4-Set Options

When a price book is created, Display/Prin/Change options are set up.
You select the prices you want to display/print, the percentage markup on
the prices and what you want to call them (titles). These selections are
used as defaults in Display/Print/Change until they are changed by using
Cmd4-Set Options; however, they can be changed temporarily each time
you use Cmd3-Print.

O To change the Display/Print/Change defaults, press [Cmd4]. The Set
Price Book Options screen appears, as illustrated below.

A&R EQUIPMENT SALES DISPLAY/PRINT/CHANGE PRICE BOOK 3730-401
Division: A Set Price Book Options

Name of Price Book  MANBOOK
Description MANUFACTURER'S PRICE BOOK
Title Quality is our business.

adjust Display Title
Dir List 100 List
Sug List 105 Sug List

Internal 100
Dir Net 100 Cost

Cmdi-return to Selection screen

 


X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK [7]

As many as 4 prices may be provided by the manufacturer's price tape.
You may only view those prices that are provided. If Sug.List and Dlr.Net
are the only two prices in the book, only those columns can be considered
for display or print. If there are four prices in the book, all four can be
printed or displayed.

Decide how many prices are to be displayed when viewing or printing the
price book. In the example, ABC Company decided on the following
options.

Dir.List: We'd like it to be displayed or printed at
100% of what is in the dealer list column
of the price book. When viewing or printing
the book, we want the column to be called
"List". This is a term the customer
understands.

Sug.List: We would like to mark this column up 5%
of what is in the price book. We will call it
“Sug List". Making it display at 105% of
what is in the book makes it appear a smaller
mark up to list.

Dir.Net: We will make this display or print at 100%
of what is in the price book. Let's title it
"Cost".

Fill in the screen. Press Enter. The options for display and print are
changed.


[ «| X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

Cmd5-Change

When you place a character beside a price book and press Cmd5-Change,
the following prompt is displayed:

AGR EQUIPMENT SALES CHANGE PRICE BOOK X3730-501 2

Division: A Price book: ACASEIH

 

O Type the first part number you want to change, and press [Enter]. The

part number's description and prices are displayed, as illustrated on the
next screen.


X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

A&R EQUIPMENT SALES CHANGE PRICE BOOK

X3730-502 2
Division: a

Price book: ACASEIE

Part Number: AC148939 Description: CORE-HEAD

Dir Net 12500
Sug List 12500

Enter-bpdate Cmd3-Return without update

 

 

0 Make changes by typing over the current prices.

To record your change(s) and return to the part number prompt, press
{Enter].

O To exit without making a change, press Cmd3-Retum without update.
You'll return to the part number prompt.

O Press Cmdi-End job to return to the entrance screen (list of price
books).

O Press Cmd1-End job to retum to the Price Update/Part List Menu.

 

 

 


X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

### Core And Reman Information

When Include Core Information=Y in Configure Vendor/Class (X38-1),
core information is present in Display/PrinChange Price Book. New part

numbers show the remanufactured part number and its primary core. The
Primary core points to one or more alternate cores if there are any.

New part # —> Reman part #

Reman part # —> Reman Price/Primary Core Price/Primary core #
Primary core # —> Alternate core # (if any)

On the next few screens a complete chain will be illustrated. Note that
there is not necessarily any correlation between the new part number and

the reman part number or their associated core part numbers,

The following screen illustrates a new part number and reman part number
with a reference to the primary core.


AGR EQUIPMENT SALES

Division A
Part Number
2958078C1
1958078c1
19se079c1
1g9sgo7sc1
1958080C1
19se0gici
1958082C1,
1gse0s2cl
1gsg0a3c1
1958085c1
igss0asc1
1g9saogsc1
1958120c1
1958159¢2
2958164C1
19581651
1958166C1
1958167¢1
1958268C1

X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

DISPLAY PRICE BOOK ¥3730-301

Case Price Book with Core Info 9-15-97
Description Sug.List Dir.Net Rtn Pkg Mlt

PUMP/A, 2381.20
REMAN: 1958079C2
REMAN-PUMP 1817.20
REMAN: $ 1517.20 coRE: $
CORE-PUMP 390.00
REMAN: 1958082C1
REMAN-MTR 1358.45
REMAN: § 1088.45 CORE: $
‘CORE-MOTOR 300.00
REMAN-MTR 2404.54
REMAN: § 2104.54 CORE: $
CORE-MOTOR 300.00
VALVE 79,88
VALVE 138.03
PULLEY 23.19
FITTING 2.96
BLADE, 22.32
BLADE 35.98
BRACKET 3.30

1785.90 % 2

139926 1
300.00 # 1979636C1
300.00 1

1074.26 1
300.00 # 1958083C1
300.00 1
1851.74 2
300.00 # 1958086cL
300.00 1

85.96
103.51.

15.07

1.63

15.63

25.18

1.99

Enter part number to begin next page: 1958168C1

Cmd1-End Job


X37-3_ DISPLAY/PRINT/CHANGE PRICE BOOK

The following screens show a primary core with reference to an alternate

core.

AGR EQUIPMENT SALES

Division A
Part Number

1979636¢L

197964c1
26.53
1979640¢2
1979642c1
1979644c1
1g7965Ci
1979655ci
1979658C1
1979666C1
1979667C1
1979669¢2
1979669¢3
1979670C1
1g79672c1
1979674c1
1979682C1
1979683¢1

Enter part number to begin next page:

cmdi-End Job

DISPLAY PRICE BOOK
Case Price Book with Core Info 9-15-97

Description Sug. List
Dir.Net Ren Pkg Mit

ALT CORe: 195e0g0cz

STRIPPER

PLATE
PLATE,

cure
STRIPPER
TES

‘TUBE
TUBE/A
CABLE/A
STRAP
STRAP

TEE

TEE
SUPPORT
PROD GRAPH
PROD GRAPH

27,


5.50
6.33
2.36


28.
42.


60.
1s.


28.
23.
-98
245
37.
1979663c1


a7
39
67
95
95
70
13


3730-301,

BE eee eee

 


X37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

AGR EQUIPMENT SALES DISPLAY PRICE BOOK ‘X3730-301
Division A Case Price Book with Core Info 9-15-97

Part Number Description Sug.List Dlxr.Net Rtn Pkg

Mit

19se0s0c. CORE- FUME 300.00 300.00 1 —| Alternate

Core

1958081¢1 REMAN: 1958082C1

1958082¢c1 REMAN-MTR 1358.45 1074.26 Q
1958082c1 REMAN: § 1058.45 CORE: $ 300.00 # 1958083C1
1958083c1 CORE-MOTOR 300.00 300.00 1
19sg08sci REMAN-MTR 2404.54 1851.74 1
1958085¢1 REMAN: § 2104.54 CORE: $ 300.00 # i958086C1
1958086c1 CORE-MOTOR, 300.00 300.00 1
1958120¢1 VALVE, 79.88 55.94

1958159c2 VALVE 138.03 103.51 &
1958264c1 PULLEY 23.19 15.07

1958265¢3, FITTING 2.96 1.63

19581661 BLADE 22.32 15.63

1958167C1, BLADE 35.98 25.18

19sg16ec1 BRACKET. 3.30 1.99 %
1958169C1 WASHER 1.72 86

1958170C1 PULLEY 28.17 19.73

1958172¢1 ARM 29.95 19.47

1958173¢2 BUSHING 2.26 1.25

Enter part number to begin next page: 1958173C1

Cndl-End Job

 


37-3 DISPLAY/PRINT/CHANGE PRICE BOOK

   

In the example below, you can see another example of the links from a
new part number to its remanufactured part number and the primary core.
This example will be used throughout the rest of the guide because the part
numbers are close together which makes it easier to follow.

A&R EQUIPMENT SALES DISPLAY PRICE BOOK X3730-301
Division A Case Price Bock with Core Info 9-15-97
Part Number Description Sug.List Dix.Net Rtn Pkg Mt
1971579¢2 ‘MOTOR ASSY $197.56 3898.17 % 4
is71s79c2 REMAN: 1971580c2

197158c2 SHEET RH 121.28 82.48 1
1971580c2 REM. MOTOR 3544.21 2752.71 1
1971ss0c2 REMAN: $ 3144.11 CORE: $ 400.00 # 1971581¢1
1971581¢1 CORE MOTOR 400.00 400.00 1
1971582c1 VALVE ASSY 1774.40 1330.80 1
1971582c1 REMAN: 1971583c1 {
19715831 REM VALVE 1567.03 1220.25 % 1
1971583¢2 REMAN: $ 1267.03 CORE: $ 300.00 # 1971584c1
1971584c1 CORE-VALVE 300.00 300.00 1
1971585¢1 KIT/SEAL 104.27 78.43

1971586c1 PUMP KIT 1934.27 +70

4971588c2 GASKET 4.27 -29

1971589¢2 PUMP KIT 1934.81 2

197159a1 PLATE 6.40 4.47

197159¢2 SHEET 175.91 119.62

1971590c2 GASKET 24.230 18.17

1971592c1 PACKAGE 138.91 104.18

Enter part number to begin next page: 1971592C1

Cmdi-End Job

 

For more information about reman parts, see Configure Vendor/Class
(X38-1).

## CHAPTER X37-4

CREATE/UPDATE PRICE BOOK

### Introduction

Create/Update Price Book allows you to load manufacturer's price books
onto the computer system. The price books can be used to add part
numbers to your computer inventory, look up prices, or find supersession
information. In addition, you can use a price book to update and reprice
your inventory (see Price Tape Update, X37-2). Parts and Point of Sale
can be running at the same time you create or update a price book.

Price books are furnished on:

= diskettes

™ tapes

= shared folders (New Holland only)

Time Considerations

Updating an existing price book takes a lot longer than creating a new
price book. Even if the price book already exists on the computer, use
Create instead of Update. Use Update only when it is the only option
available to you, such as when you need to add quantity break pricing or
supersession records,

 
 

Note:

 
    

    

| If you anticipate the need to update large price books frequently, call

DIS about a special price book diskette #1 that allows you to build the
initial price book large enough to accommodate future updates.


[2] X37-4 CREATE/UPDATE PRICE BOOK

### Overview

Price books are provided to DIS by the manufacturers, DIS in turn, places
the price books on diskettes or tape in a format that can be used by the
Business System and ships them to the dealer. Using this job, you can load
the price books on the computer.

The price book on the computer will be the same as the hard copy of the
price book that is kept on the parts counter. It can provide pricing
information, return information, price break information, and supersession
information. If the information is provided to DIS by the manufacturer, it
will be displayed in the price book that is loaded onto the computer.

Sometimes, the amount of information provided by the manufacturer
cannot be provided on one tape or set of diskettes. For example,
supersession information may be provided on different tapes or diskettes
from the regular price book. If you receive two tapes or sets of price book
diskettes for the same manufacturer, you would use this job to apply both.
The procedure would be:

 

 

 

Apply the price book using Create/Update Price Book.

 

O Update the price book using the same job.


X37-4 CREATE/UPDATE PRICE BOOK [=]

Once the price book is loaded using this job, it can be accessed in several

places:
X3-1 Parts Inquiry
X3-2 Parts Posting and Maintenance

X341-2 Correct Order Before Receiving

X35-2 Correct Stock Return

X36-2 Correct Phase Out

X37-3 Display/Print/Change Price Book

X5-1 Additional Options, option 9, Display/Print Price Book

The price book is loaded using this job. You will assign a name to the
Price book while it is being loaded. To access price books during Point of
Sale invoicing, you must attach the name of the price book to the
manufacturer's vendor code set up in X38-1 Configure Vendor/Class.

In Configure Vendor/Class, type the name of the Price book in the "Price
Book assignment” field on the Vendor/Class Configuration screen for the
Vendor.

At Point of Sale Invoicing, the vendor code is typed in the "Ven" field
when selling parts. See the example below:

PARTS COUNTER
TDI/W Pty Line SC Ven Qty Part number Price Base

. 0010 PC MAN 4
Standard line code No demand = Warranty

 

The price book attached to the vendor code in the "Price Book
assignment" field at Configure Vendor/Class (X38-1) will be accessed
during invoicing. See the section Price Book in CHAPTER X5- 1, POINT
OF SALE INVOICING.


[+] X37-4 CREATE/UPDATE PRICE BOOK

### Preparation

AS/400 New Holland Dealers Only

O Use the OPTDIS Library to set the New Holland Price Book option, or
at a menu, type:
X00081 PBFLRO1,1 [Enter]

O Ata menu, type:
X37703 FN 970101 NHPB (Enter]

Space Considerations

Only a small number of parts on the Price tapes are in your data files
normally. The price tape contains all of that vendor's Pparts--so you create a
price book even more current than the one on your parts counter.

There are 18,880 parts on each 8 inch diskette. General rule of thumb is
that it takes approximately 500 blocks for one diskette. To find out how
many blocks you have available on your disk, run a compress. Then run a
catalog and check for space available. Compare the number of diskettes X
500 to the blocks available. If you do not have enough room, warning
Inessages will be displayed.

Time Considerations

It takes a lot longer to update a price book than to create a new one (see
page 1).
cC


X37-4 CREATE/UPDATE PRICE BOOK [=]

Quantity Break Price Books

if your price book contains quantity break records, you will be provided
with two price books. One will be the standard price book. It will be
labeled with the manufacturer's name. The other price book will
specifically reference quantity break records.

Note:

 

Apply the standard price book first. The book referencing quantity break
records should be applied over the first price tape. You will have to
Update the main price book. See Updating a Price Book.

Supersession Information

Some vendors also provide supersession on separate tapes (or diskettes)
from the price book. The main price book will be labeled as the
Manufacturer's price book. The supersession tape (or diskettes) will be
labeled as supersession.


| You should definitely obtain the special price book diskette #1 that
allows you to build the initial price book large enough to accommodate
| the supersession records.

 

Use Create to apply the standard price tape and Update to add the
supersession information to it. See Updating a Price Book.


X37-4 CREATE/UPDATE PRICE BOOK 7 |

### How To Run

Creating a Price Book

From the Automatic Price Update Menu (X3-7), select option 4,
Create/Update Price Book. The following screen appears:

CREATE PRICE BOOK 3740-001

Enter the name for the price book file

This procedure creates a permanent disk file from your price tape diskettes.
The Price Book Display procedure is used to display the price tape on your
terminal. A separate price beck can be created for different vendors. The

number of price hooks that you keep on your computer will be limited by the
amount of disk space you have available.

Before you rua this procedure, you need to select the file name you want to use :
for this price book

emdi-cancel

 

How to choose a name:

The name may be up to 8 letters. It must not contain blanks, commas,
apostrophes, question marks, slashes, greater than signs, equal signs,
hyphens, or numbers. /t may have a period in the second Position, such as
u.PRICBK. If u=the character associated with your file set, the price book
will be backed up during daily backup.


X37-4 CREATE/UPDATE PRICE BOOK

The description shows up at Point of Sale if you have more than one price
book. The title prints on the price book. You may have the same word(s)
for the name and description.

If you select a Price Book file name that already exists on the disk you will
have the choice of either updating the existing Price Book or creating a
new Price Book to replace the existing one. See Updating a Price Book.

After selecting the name, press [Enter]. At the next screen, select the
device: $1=Slot | (default); M 1=Magazine 1; TC=Tape Cartridge, or
FL=Folder. Press [Enter] to continue. The Set Up Options screen appears.

The name selected on the first screen defaults in the Price Book Name
field. Fill in the Description and Title.

Now it's decision time. First you must know how many prices are
provided in the price book by the vendor. You may only view those prices
that are provided. If Sug. List and Dir. Net are the only two prices in the
book, only those columns can be considered for display. If there are four
prices in the book, all four can be displayed or printed.

Decide how many prices are to be displayed when viewing or printing the
price book. For now, say you wanted to display three of the four prices,
Dir.List, Sug.List, and Dlr.Net. Decide what percentage of the price you
want to display or print. For example:

Dir.List: We'd like it to be displayed or printed at
100% of what is in the dealer list column
in the price book. When viewing or printing
the book, we want the column to be called
“List”. This is a term the customer will
understand.


X37-4 CREATE/UPDATE PRICE BOOK

Sug.List: We would like to mark this column up 5%
of what is in the book. We will call it "Sug.
List". Marking it up 5% will show less mark
up to selling price.

Dir.Net: We will make this display or print at 100%
of what is in the price book. Let's title it "Dir
Net".

The Set Up Options screen, which is illustrated below, has been filled out
according to the example:

ABC COMPANY Create/Update Price Book *3740-401
Division: E Set Up Options

Price Book Name MANBOOX
Description MANUFACTURER'S PRICE BOOK
Title Manufacturer as of 12/01/91

S Adjust Display Title
Dir.List i100 List
Sug List 105 Sug List

Internal 2190 Internal,
Dir.Net 100 cost.

Enter-Set up price book options

 


X37-4 CREATE/UPDATE PRICE BOOK ( .

When the set-up options have been selected, press [Enter] to create the
price book.

Note:

AS/400 with diskette drives only. You may receive a system message,
SYS-3777 with options 0123, regarding diskette file @.PRC. This

| simply means the file could continue to the next diskette, and the
message is repeated for all but the last diskette in the set. The message
occurs about 2 minutes after the diskette is loaded. Take option 0
(zero) to continue the price tape update.

 

Updating a Price Book

Since it takes much longer to update a price book than to create a new one,
the Update option is only appropriate for Quantity Break Pricing and
Supersession records, which are described earlier in this chapter.

     

Note:

    

If you anticipate the need to update large price books frequently, call
DIS about a special price book diskette #1 that allows you to build the
initial price book large enough to accommodate future updates.

 

 
 
   

 

  

From the Automatic Price Update Menu (X3-7), select option 4,
Create/Update Price Book. The following screen appears:


X37-4 CREATE/UPDATE PRICE BOOK

CREATE PRICE BOOK x3740-001

Enter the name for the price beok file

This procedure creates a permanent disk file from your price tape diskettes.
‘The Price Book Display procedure is used to display the price tape on your
terminal. A separate price book can be created for different vendors. ‘The
number of price Books that you keep on your computer will be limited by the
amount of disk space you have available.

Before you run this procedure, you need to select the file name you want to use
for this price book

(mdi -Cancel

 

Type the name of the price book you want to update. You will see the
following message: "The price book MANBOOK already exists on disk.”

To switch from Update to Create, press [Cmd3], Create New Price Book.
The old price book will be deleted, and a new Price book will be created.

If you are adding quantity break pricing or supersession, press [Cmd2] to
update the existing price book.

If you are updating an existing price book with a price tape that has an
older date than the existing price book, you will see a warning message.
To continue, press [Enter]. You may want to update an existing book with
an older tape when, for example, you are adding supersession information
to a current price book.


Notes: C ~

C

## CHAPTER X37-5

REMOVE PRICE BOOK

### Introduction

Remove Price Book will allow you to:
™ remove or delete a price book from your files.

### Removing A Price Book

Make a backup of your parts file before running this job. After selecting
the option to Remove Price Book, you will see a screen similar to the one
shown in Figure X3750-101.

ABC COMPANY 3750-101
Division: E REMOVE PRICE BOOK

Price Book Name Description

x BUSHHOG BUSHHOG PRICE TAPE
woons WOODS PRICE TAPE

To REMOVE a Price Book enter any character in front of the book name.

Cmdl-Retuxn to menu Cm4--Remove price book

## X37-5 REMOVE PRICE BOOK

 

### Options

O To remove the price book, type any character in front of the book
name. Press CMD 4. Then press CMD 4 once again to confirm the
delete (or press CMD | to cancel).

0) Press CMD | to end the job and return to the menu.

LC

## CHAPTER X37-6

AS/400 PART LISTS

### Introduction

This job is designed to be used in Conjunction with an external parts
catalog system on CD-ROM linking it with DIS Point of Sale; however,
Part lists can be used without an external system.

Part Lists are lists of parts (and related information) that are required to do
specific jobs. The parts are not necessarily in inventory. Lists can be added
manually or uploaded from the parts catalog system. A list can be copied,
and individual parts can be added or deleted from any list. In addition,
some part information can be changed.

From the detail screen at Point of Sale, pressing [Cmd24] takes you
directly to Part Lists, where you can select lists and/or individual parts.
The Copy Lines function is evoked automatically to transfer them to an
invoice or work order.

Before you use Part Lists for the first time, set up the default information,
which is needed by Point of Sale, in Part Lists/P.0.S. Default Table. See

## CHAPTER X37-7.

If you are using an external parts catalog, set the appropriate OPT switch
in the OPTDIS Library and configure as directed in the installation
instructions for the manufacturer.

  

Technical Note:

     

Part lists are stored by date and time in files u.IIH (list header
information) and u.IID (parts detail information). An alternate index
file, u.HA, streamlines list maintenance,


X37-6 AS/400 PART LISTS

### How To Run

 

 

 

 

From the Price Update Menu (X3-7), select option 6, Part Lists. Or,

from the detail screen at Point of Sale, press [Cmd24]. The entrance
screen, Review Part Lists, appears, as illustrated below.

Reviewing Part Lists (Entrance screen)

ABC-AG, AUTO, CONS & TRUCK CO. PART LISTS

Division A Review Part Lists

(Options: 1=Select 2=Change 3=Copy 4=Delete 5=View)

List Name

HYDRAULIC

2-32 FIELD BOSS ALTERNATOR
DATE: 10/20/93 TIME: 12:49:56
WHI 16 / INJECTION NOZZLE
DATE: 10/25/93 TIME: 10:46:01
RANDY'S LIST

STEVE'S LIST

DATE: 10/21/93

DATE: 10/21/93

DATE: 16/21/93

DATE: 10/21/93

THERMO KING / MISC FILTERS
THERMO KING / UPTIME DECALS

Gmdl-End job cmd5-Add new list Roll~Page

Last Used
10/25/93
10/25/93
10/25/93
10/25/93
10/25/93
10/25/93
10/25/93
10/21/93
10/23/93
10/21/93
10/21/93
10/21/83
10/21/93

Created
10/25/93
10/25/93
10/20/93
21/29/93
10/25/93
10/25/93
10/25/93
10/21/93
10/21/93
10/21/93
10/21/93
10/21/93
09/23/93

Home-Top of list

3760-202 1

 

First, the options on this screen are discussed with the exception of
1=Select, which is covered in the section at the end of the chapter, USING
PART LISTS FROM POINT OF SALE. Options 2-5 are followed by


X37-6 AS/400 PART LISTS [2]

screens related to Cmd5-Add new list.

© To use one of the options, type its number in the column labeled "Opt"
and press [Enter].

 
 

Note:

  
     

Option 1=Select is not valid except when you enter this job by
pressing [Cmd24] from Point of Sale.

 

 

Parts Search Window

A Parts Search Window is also available on this screen. To use it, enter a
“?" on either or both sides of a string of characters in the part number field.
The Parts Search Window will display positioning at the beginning of the
string you entered. If you enter a "*" before a string of characters, the
parts search window is displayed with ail part numbers that contain the
String of characters following the asterisk. When the correct part number
is found in the window, the user may select it by placing a "1" beside it
and the complete part number will be returned to the part number field.
Refer to Parts Inquiry (X3-1) and Parts Posting and Maitenance (X3-2) for
more information on the Part Search Window.

Bearing Interchange

By using a pound sign in the part number field along with any bearing
number (such as #689), you can search for a replacement in the Bearing
Interchange Catalog. Screens are illustrated in CHAPTER X7-9, Bearing


[+] X37-6 AS/400 PART LISTS

Interchange Menu.

Renaming a Part List (2@=Change)

O To rename a part list, type 2 in the column labeled "Opt" on the
Entrance screen (Review Part Lists). The Change List Name screen

appears.

ABC-AG,AUTO,CONS & TRUCK CO. PART LISTS %3760-103 3
Division A Change List Name

List: 2-32 FIELD BOSS ALTERNATOR

Enter-Continue  Cmd3-Previous screen

 

 

 

 

To return to the entrance screen without making any changes, press
Cmd3-Previous screen.

 


X37-6 AS/400 PART LISTS [=]

O To change the name, simply type over the current name and press

[Enter].
Copying a Part List (3=Copy)

To copy a part list, type 3 in the column labeled "Opt" on the Entrance
screen (Review Part Lists). The Copy List screen appears.

ABC-AG, AUTO, CONS & TRUCK CO. PART LISTS 3760-104 4
Division A Copy List

Copy from List: 2-32 FIELD BOSS ALTERNATOR

To List: DATE: 11/29/93 TIME: 12:03:16

 

Entex-Continue Cmd3-Previous screen

 

 

 

 

 

To return to the entrance screen without making any changes, press
Cmd3-Previous screen.


[ «| X37-6 AS/400 PART LISTS a

OU To make a copy, simply type a name for the copy at the "To List:"
prompt, which defaults to the current date and time, and press [Enter].

Deleting a Part List (4=Delete)

O To delete a part list, type 4 in the column labeled "Opt" on the Entrance
screen (Review Part Lists). The Delete List screen appears.

ABC-AG, AUTO, CONS & TRUCK CO. PART LISTS 3760-105 5
Division A Delete List

ist: 2-32 FIELD BOSS ALTERNATOR

Enter-Continue Cnd3-Previous screen

 

O To retum to the entrance screen without deleting the list, press [Cmd3].

0 To proceed with the deletion, press [Enter].

‘
RELEASE 2.1 “~


X37-6 AS/400 PART LISTS 7 |

Reviewing Parts on a List (5=View)

O To look at a part list, type 5 in the column labeled "Opt" on the
Entrance screen (Review Part Lists). The Review Parts screen appears.

ABC-AG,AUTO,CONS & TRUCK CO. PART LISTS X3760-106 6
Division A Review Parts

List: WHI 16 / INJECTION NOZZLE
(Options: 1=Select 2=Change d=Delete}

Part Number Description
33-0116025 NOZZLE
33-0116122 NOZZLE > I
33-0117722 PIN
33-0127730 SPRING
33-0117749 SPACER
33-0217757 WASHER
33-0117765 WASHER
33-0117773 WASHER
33-0117782 WASHER
33-0117803 WASHER
33-0117811 WASHER
33-0117838 WASHER
33-0117846 WASHER

Cmd3-Previous screen Cmd5-Add new part Roll-Page Home-Top of list

 

This screen serves the same purpose for individual parts as the entrance
screen serves for lists. On the following pages, the options on this screen
are discussed with the exception of 1=Select, which is covered in the
section at the end of the chapter, USING PART LISTS FROM POINT OF
SALE. Options 2 and 4 are followed by screens related to Cmd5-Add new
part.


X37-6 AS/400 PART LISTS

 

Ci To use one of the options, type its number in the column labeled “Opt”
and press [Enter].

Note:

Option 1=Select is not valid except when you enter this job by
pressing [Cmd24] from Point of Sale.

 

Changing Part Information (2=Change)

O To change part information, type 2 in the column labeled "Opt" on the
Review Parts screen. The Change Part Information screen appears.


X37-6 AS/400 PART LISTS [2]

ABC-AG, AUTO,CONS & TRUCK CO. PART LISTS x3760-108 8
Division A Change Part Information

List: WHI 16 / INJECTION NOZZLE

Description

Bin Location

Enter-Continue cnd3-Previous screen

 

O To retum to the Review Parts screen without making any changes,
press [Cmd3].

O To make a change, simply type over the current information and press
[Enter]. Vendor code and part number cannot be changed.

Note:

To change vendor code or part number, first delete the part by using
option 4 from the Review Parts screen. Then add the new part number
by using Cmd5-Add new part.

 


[=| X37-6 AS/400 PART LISTS (

Deleting a Part from a List (4=Delete)

 

 

 

 

To delete a part from a list, type 4 in the column labeled "Opt" on the

Review Parts screen. The Delete Part screen displays the part's current
information.

ABC-AG,AUTO,CONS & TRUCK CO.
Divisien A

PART LISTS
Delete Part

¥3760-103 9

List: WHI 16 / INJECTION NOZZLE

Description

Bin Location

Enter-Continue  Cmd3-Previous screen

 

 

 

To return to the Review Parts screen without making any changes,
press [Cmd3].

 

 

 

 

To delete the part, press [Enter].

C


X37-6 AS/400 PART LISTS [*]

Adding a Part to a List (Cmd5-Add new Part)

 

 

 

To add a part to a list, press Cmd5-Add new part from the Review Parts
screen. The Add Part screen appears.

 
      
  
    
  

    

ABC-AG, AUTO, CONS & TRUCK co. PART LISTS

X3760-107 7
Division A

Add Part

Description

Bin Location. 2...

 

    
 

Enter-Continue  Cmd3-Previous screen

O1 To return to the Review Parts screen without making any changes,
press Cmd3-Previous screen.

 

 

 

 

To add a part, furnish the relevant information, and press [Enter].


[| X37-6 AS/400 PART LISTS (~

Adding a New Part List (Cmd5-Add new list)

0D To add a new part list press [Cmd5] from the Review Part Lists
(entrance) screen. The Add Part List screen appears. The current date
and time are used as the default name.

ABC-AG,AUTO,CONS & TRUCK CO. PART LISTS 3760-102 2
Division A Add Part List

List: DATE: 11/23/93 TIME: 11:41:49

Enter-Continue  Cmi3-Previous screen

 

O To return to the Review Part Lists (entrance) screen without making
any changes, press Cmd3-Previous screen.

CO To accept the default name, press [Enter].

O To establish a more meaningful name, simply type over the date and
time, and press [Enter].


X37-6 AS/400 PART LISTS [>]

Note:

The name of any list can be changed at any time by using option

2=Change on the Review Part Lists (entrance) screen. See the section,
Renaming a Part List (2=Change), which appears earlier in this
chapter.

 

### Using Part Lists From Point Of Sale

Although you can copy more than one part (lists and/or individual parts) to
an invoice or work order at Point of Sale, you must press [Enter] after
each selection.

O Press [Cmd24] from the detail screen to go directly to the Review Part
Lists (entrance screen). A list can be selected from the Review Part

Lists screen, or an individual part can be selected from the Review
Parts screens.


X37-6 AS/400 PART LISTS

Selecting a Part List (1=Select)

 

 

 

 

On the Review Part Lists (entrance) screen, select a part list by typing /

in the column labeled "Opt" and press [Enter]. A message that the list
has been selected is displayed at the bottom of the screen. Repeat this

process to select other lists.

Every time you type 1, you must press [Enter]. You cannot select 2
lists, even on the same screen, and then press [Enter]--if you do so, the

second list will not be copied.

ABC-AG, AUTO,CONS & TRUCK CO

PART LISTS

Division A Review Part Lists

(Options: isSelect 2=Change 3=Copy 4=Delete S-View)

bist Name
HYDRAULIC

Last Used

2-32 FIELD ROSS ALTERNATOR

DATE: 10/20/93 TIME:

12:49;

WHI 16 / INJECTION NOZZLE

DATE: 10/25/93 TIME:
RANDY'S LIST

STEVE'S LIST

: 10/21/93
10/21/93
10/21/93

2 10/21/93

 

10:46;

 

THERMO KING / MISC FILTERS
THERMO KING / UPTIME DECALS

Qmdi-End job md5-Add new list

List has been selected for copy to current Point of sale invoice.

Roll-Page

10/25/93
20/23/93
10/25/93
10/25/93
20/25/93
10/25/93
20/25/93
10/21/93
10/21/93
40/21/93
20/21/93
10/21/93
10/21/93

Created
10/25/93
10/25/93
10/20/93
11/29/93
10/25/93
10/25/93
10/25/93
10/21/93
10/21/93
10/21/93
10/21/93
10/21/93
09/23/93

Home-Top of list

x3760-101 1

cmé12-Inpert

 
LL


X37-6 AS/400 PART LISTS |

Copying Parts to Point of Sale

O To initiate the Copy-Lines procedure after you have selected the lists
(or individual parts) you want, go back to the Review Part Lists screen
by pressing [Cmd3].

C) Press (Cmd1] to end the Part Lists job. Look for the word "Copying" in
the top right comer of the screen and the first part on the detail line.
Parts are copied by the "Preview" Process.

 

ABC-AG, AUTO, CONS & TRUCK co. SALES ORDER Copying x5100-106
COUNTER TICKET ¥# croo1i9 For GRADO1 CHARGE OPEN = 11/29/93

?
TDP Line # Qty vnd Part Number Description Bin Ext Price 7
TP 0010 PC 2 wHE 33-0c17698 4

Spec order parts +00 Avail total

FARTS CUSTOMER

FDI/W Pty Line SC Ven ty Part nunber

v P0020 PC war 2 33-0017949

Standard line code host sale No demand

Available C/T Res. R/O Res. On Order Super .
a 2 0 0

 

D Press [Enter] to place each part line on the document or [Cmd22]
([Shift]+{F10]) to bypass it.


16 | X37-6 AS/400 PART LISTS C

Selecting a Part (1=Select)

 

 

 

Select an individual part from a list by first typing 5 in the column
labeled "Opt" to display the parts associated with the list. The Review
Parts screen appears.

C Type / in the column labeled "Opt" to select a part and press [Enter]. A
message that the part has been selected is displayed. Repeat this process
to select other parts.

 

Every time you type I, you must press [Enter]. You cannot select 2
parts, even on the same screen, and then press [Enter]--if you do so, the
second part will not be copied.

ABC-AG,AUTO,CONS & TRUCK CO. PART LISTS X3760-106 6 {
Division A Review Parts

List: WHI 16 / INJECTION NOZZLE
(options: 1=Select 2-Change 4=Delete)

Part Number Description
33-0116025 NOZZLE
33-0116122 NOZZLE - I
33-0117722 PIN
33-0117730 SPRING
33-0117749 SPACER
33-0117757 WASHER (aS
33-02137765 WASHER (AS
33-0217773 WASHER (AS
33-0117781 WASHER (AS
33-0117803 WASHER (AS
33-0117811 WASHER (aS
33-0117838 WASHER (AS
33-0117846 WASHER (AS

d
1
1
1
1
1
1
1
2

cnd3-Previous screen CndS-Add new part Reil-Page Home-Top of list
part has been selected for copy to current Point of Sale invoice.

 

LL


X37-6 AS/400 PART LISTS

 

 

 

 

Press [Cmd3] to return to the Review Part Lists (entrance) screen.
O Press [Cmd1] to start the Copy-Lines procedure.


Notes: Cc ~

L

## CHAPTER X37-7

PART LISTS/P.O.S DEFAULT TABLE

### Introduction

To use Part Lists (X37-6) with or without an external parts catalog system,
set up default codes in this job. If you are using an external system, this
job also records the code associated with the catalog.

Technical Notes. The P.O.S. Default Table is stored in u.IIM. Part lists are
stored by date and time in files u.IIH (list header information) and u.IID
(parts detail information). An alternate index file, u.IIHA, streamlines list
maintenance.


X37-7 PART LISTS/P.O.S. TABLE a

 

### How To Run

From the Price Update Menu (X3-7), select option 7, Part Lists/P.O.S.
Default Table.

ABC-AG,AUTO,CONS & TR PARTS CATALOG MANUFACTURER TABLE X3770-101 1
Division: A

Enter the manufacturer code from your parts catalog
system and the corresponding parts vendor code along
with the default parts sales code for this vendor.

Manufacturer code . . .
DIS vendor code... . (

Sales code

Enter '¥' to delete . .

 

OD To exit without making changes, press [Cmd1]-End job.

0 To delete the codes, enter Y at the prompt in the bottom right corner,
“Enter 'Y' to delete."

To set up the table, provide the codes, which are described below, and
press [Enter].

 

 

 

 

RELEASE 2.1 LU


X37-7 PART LISTS/P.O.S. TABLE

 

O Press {Cmd1] to end the job. The values are written to file, u.JIM and a
copy of the table is produced.

Note: Although the values have been entered, they are not displayed on
screen when you re-enter this job. Don't panic! If you need to review the

table, simply press [Cmd1] to end the job and print another copy of the
table.

### Fields & Descriptions

Manufacturer code 7 characters. Optional. The code associated
with your parts catalog system. This code is
assigned by the catalog. Leave it blank if
you are not using an external system. The
code associated with New Holland PAL is
"EN."

DIS vendor code 3 characters. Required. The vendor code you
assigned to this manufacturer in Configure
Vendor/Class (X38-1). For example, you
may have assigned "FOR" or "FNH" for
Ford/New Holland.

Sales code 2 characters. Required. Default sales code
for this vendor. Sales codes are set up in
Sales Code Maintenance (X52-3).

Note: If the cross-reference between the parts catalog manufacturer code
and the DIS vendor code you set up in Vendor/Class Configuration
(X38-1), the following error will be sent to the PC Interface screen when
you attempt to close a transaction list (TLIST):

Vendor ###### in Division # has not been cross referenced.

Notes:

## CHAPTER X37-8

AGCO CREATE PRICE BOOK

### Introduction

AGCO Create Price Book allows you to load up to six different product
lines from a tape cartridge to the computer system. The price books can
be used to add part numbers to your computer inventory, look up prices, or
find supersession information. In addition, you can use a price book to
update and reprice your inventory (see AGCO Price Tape Update, X37-9).

The create price book involves 2 tapes: pricing and supersession. The
following lines are included on the combined tapes.

1. AGCO ALLIS

2. GLEANER

3. HESSTON

4. MASSEY FERGUSON
5. NEW IDEA

6. WHITE

Time Considerations

Agco Create Price Book may be slower than you'd expect for a price book
for a single vendor. The reason is that a price book is created only for the
first line you select. For the second and subsequent lines, the first price
book is being updated, which is a slower process.


[2] X37-8 AGCO CREATE PRICE BOOK C

### Overview

Price books are provided to DIS by the manufacturers. DIS in turn, places
the price books on tapes in a format that can be used by the Business
System. The tapes are shipped to the dealer. Using this job, you can load
the price books on the computer.

The price book on the computer will be the same as the hard copy of the
price book that is kept on the parts counter. It can provide pricing
information, return information, and supersession information. If the
information is provided to DIS by the manufacturer, it will be displayed in
the price book that is loaded onto the computer.

 
 

NOTE: Backward supersession records are not added to the price book
automatically in order to avoid erroneous multiple supersession records. If
you want backward supersession information later, type the following at a
command line: X37802 nnnnnonn {Enter] (nnnnonnn=name of your

price book).

 
    
        

Once the price book is loaded using this job, it can be accessed in several

places:
X3-1 Parts Inquiry
X3-2 Parts Posting and Maintenance

X341-2 Correct Order Before Receiving

X35-2 Correct Stock Return

X36-2 Correct Phase Out

X37-3 Display/Print Price Book

XS5-1 Additional Options, option 9, Display/Print Price Book

Price Books can also be accessed during Point of Sale Invoicing. To

f
Ne


X37-8 AGCO CREATE PRICE BOOK [2]

access price books at Point of Sale, you must perform an additional
preparation step.

The price book is loaded using this job. You will assign a name to the
price book while it is being loaded. To access price books during Point of
Sale invoicing, you must attach the name of the price book to the
manufacturer's vendor code set up in X38-1 Configure Vendor/Class.

In Configure Vendor/Class, type the name of the price book in the "Price
Book assignment" field on the Vendor/Class Configuration screen for the
Vendor.

At Point of Sale Invoicing, the vendor code is typed in the "Ven" field
when selling parts. See the example below:

PARTS COUNTER
TDIsw Pty Line sc ven ty Part number
+ 0010 PC TAN

Standard line code No demand Warranty

 

‘The price book attached to the vendor code in the “Price Book
assignment” field at Configure Vendor/Class (X38-1) will be accessed
during invoicing. See the section Price Book in CHAPTER X5-1, POINT
OF SALE INVOICING.

### Preparation

Before making any significant changes to parts files, make sure you have a


[ «| X87-8 AGCO CREATE PRICE BOOK

good backup.

O From the Security & Configuration Menu (X6), select option 1,
Backup Data Files.

O Optional. Select the option to run End of Day jobs for all divisions.
(1 Save the backup for at least 1 week.

O Check the user board to make sure no other Parts or Point of Sale jobs
are running.

### How To Run

Creating a Price Book

O From the Price Update/Part Lists Menu (X3-7), select option 8, Agco
Create Price Book.

C1 Insert the combined inventory tape cartridge as prompted. Press
[Enter]. You are prompted for an 8-character name.

O Key in the name of the combined price book and press [Enter]. The
following screen appears.


X37-8 AGCO CREATE PRICE BOOK [=]

ABC-AG, AUTO, CONS & TRUCK C AGCO CREATE PRICE BOOK 3780-003
Price book: HARLEY

Please select the lines and types of information to
be included in the price book.

Line Pricing?  Supersession?

AGCO ALLIS
GLEANER
HESSTON

MASSEY FERGUSON
NEW IDEA

WHITE

Omd2-End job

 

From this list, select pricing and supersession for the lines you are
authorized to use by changing the N to Y and press [Enter]. The job is
evoked with the message, "Press Enter to return to a menu.”

C Press [Enter]. Although most of the time it doesn't matter whether you
press [Enter] right away, it does matter for this particular job.

Messages regarding its progress are sent to the $/36 console or the AS/400
System Operator's message queue. The book is created for the first line,
and updated for subsequent lines, which makes the process significantly
slower than simply creating a book for a single line. When the price book
is done, you are prompted to insert the combined supersession tape.


Notes:

## CHAPTER X37-9

AGCO PRICE TAPE UPDATE

### Introduction

AGCO Price Tape Update allows you to update part prices and other part
information with the most current data from tape cartridges. An
alternative is to create (or update) a price book first, then use Price Tape
Update to update your inventory from it (see X37-8 Agco Create Price
Book).

‘Two cartridge tapes are used in this procedure. One tape includes pricing
information; the other includes supersession information.

The price tape updates parts company-wide. If you have more than one
division, you only need to run the price tape one time.

Only parts in classes configured Y for automatic pricing will be updated.
If you are using a supersession tape, parts updated by the price tape will be
updated with supersession information.

See also, CHAPTER X3-7, AUTOMATIC PRICE UPDATE MENU.

FYI - The system proceeds with the Price Tape Update in the following
order:

 

QO Looks at the class assigned to the part in Parts Posting &
Maintenance (X3-2).

QO Looks at the pricing information for that class in Vendor/Class
Configuration (X38-1).

O Uses the percentages and base codes from Vendor/Class
Configuration to calculate new prices for the part. If a base for a
price used in Vendor/Class Configuration is not on the Price Tape,
the corresponding price is set to zero.

 

 

 

Moves the bases assigned in Vendor/Class Configuration to the
part record in Parts Posting & Maintenance. It is possible to assign
different bases on the part master record (X3-2) from those used by
the part's class in Vendor/Class Configuration (X38-1); however,


[2] X37-9 AGCO PRICE TAPE UPDATE oO

the system relies on X38-1. In this step the system actually forces
the part master record to conform to the Vendor/Class setup.

### Running The Price Tape Update

IMPORTANT: Before starting this job, backup your parts files.

 

From the Parts Report Menu (X3-6), select option 1, Parts
Inventory Pad. Request a summary only. Label the report,
“BEFORE PRICE TAPE UPDATE."

 

 

 

 

 

Optional Step. NO PARTS OR POINT OF SALE JOBS CAN i
BE RUNNING. From the Parts Inventory Adjustment Menu (X3-

3), select option 4, Parts Inventory Freeze. This creates a snapshot

of your parts inventory before any prices are changed. Later, you

can request an Inventory Variation Report, which will enumerate

the changes. Repeat for each division. Please be aware of

potential disk space problems, particularly if you have more than 1
division: the file, u.IFZd, is quite large. Also, the freeze takes a

lot more time than a parts pad summary.

Agco Price Tape Update

 

 

 

From the Automatic Price Update Menu (X3-7), select option 9,
Agco Price Tape Update. This job produces 4 reports, which are
described in the section, PRICE TAPE UPDATE REPORTS.

 

Insert the combined inventory tape cartridge as prompted. Press
[Enter]. The following selection screen appears.


X37-9 AGCO PRICE TAPE UPDATE [=]

ABC-AG,AUTO,CONS & TRUCK C AGCO PRICE TAPE UPDATE x3790-101 1

Please select the lines by specifying a DIS vendor code
for each one desired. Also specify whether or not to
update supersession for cach line.

Line Supersession?

AGCO ALLIS
GLEANER

HESSTON

MASSEY FERGUSON
NEW IDEA

WHITE

 

O For each authorized line you want to update, furnish your 3-
character vendor code, and change the N to Y if you want to update
supersession. Press [Enter] to continue. The job is evoked with
the message, "Press Enter to return to a menu."

1 Press [Enter]. Although most of the time it doesn't matter whether
you actually press [Enter] right away. It does matter for this
particular job.

Messages regarding its progress are sent to the S/36 console or the AS/400


Ls] X37-9 AGCO PRICE TAPE UPDATE

System Operator's message queue. The program updates inventory for all
selected lines first, then prompts you to insert the supersession tape.
When the job is complete, the following message is sent to the S/36
console or AS/400 System Operator message queue: "The AGCO price
tape update has completed.”

QO From the Parts Report Menu (X3-6), select option 1, Parts
Inventory Pad. Request a summary only. Label the report,
"AFTER PRICE TAPE UPDATE."

O Ifyou created an inventory freeze file earlier, run the Parts
Inventory Variation Report. From the Parts Inventory Adjustment
Menu (X3-3), select option 5.

QO Verify a successful price update. On a representative parts at Parts
Inquiry (X3-1), select option 5.

© Prices
@ Supersession Indicators
© History Information

®@ Package Quantities

This concludes Price Tape Update where there is no price book.


X37-9 AGCO PRICE TAPE UPDATE [=]

### Reports

Agco Price Tape Update produces four reports:

CO No Update Record Found For Part Record

Parts on this report are in your parts file, but the number is not on the price
update tape. Parts listed here are not updated. Parts manufacturers do not
carry all their parts on every update tape.

 

 

 

Parts in Non-Update Class

Parts on this report are in your parts file and on the price tape. However,
they are in a class configured with an N for no automatic update. If you
want these prices to be updated, change the configuration and run the tape
again.

 

0 Invalid Class or Vendor Default Class Missing

The parts on this report are either in a class that has been deleted or no
default class is configured for this vendor. Check parts appearing on this
report for repricing. Make necessary changes in vendor/class
configuration.

D Parts Supersession

The Parts Supersession Report provides information on parts that
supersede or are superseded by another part or parts. The supersession
indicators for single (S) and multiple supersession (M) appear on this
report.

S means that the part supersedes or is superseded by one part. M means
the part supersedes or is superseded by more than one part.

The price update tape does not set up new records for superseding or


[«] X37-9 AGCO PRICE TAPE UPDATE

superseded parts that are not in your inventory. If you have part A in
inventory, and on the price tape it is superseded by part B which is not in
your inventory, the price tape will add the supersession indicator to part A.
No information will be available on part B. To add information on part B,
add it to inventory in Parts Posting and Maintenance. Then run the price
tape again and description and prices will be added.

On the Parts Supersession Report, you may find the following listing:

Part. Nunber Superseded By Supersedes
361212403 Leizi2ne

ne122i2Ma 2612224M2

 

The part numbers in column | are already in your inventory files. The part
numbers in columns 2 and 3 may or may not be in your inventory files:
however, if they are, they are also listed in column 1.

In the progression above, M2 was the original part number. It is no longer
in your inventory files (it is not listed in column 1). M3, which is in your
inventory files, has been superseded by M4. M4 is also listed in column 1;
therefore, it is also in your inventory files. You only need to add part
numbers that are in column 2 but not in column 1.

## CHAPTER X38-1

CONFIGURE VENDOR/CLASS

### Introduction

In Configure Vendor/Class, define characteristics of vendors and classes,
establish criteria for suggested stock orders, define sorting specifications
for the vendor's parts on the parts pad, setting up a class for
remanufactured (reman) parts, and define pricing structures and markup
for classes of parts.

In the sections that follow, you will learn how to add change or delete a
vendor and class. The fields on the screens are briefly described in the
sections. A complete description of concepts is provided in CHAPTER
X3-8, PARTS CONFIGURATION MENU.

### How To Run

From the Parts Configuration Menu (X3-8), select option 1, Configure
Vendor/Class. A vendor prompt appears, as illustrated below:

ABC COMPANY Parts Configuration X3810-101

vendor/Class Configuration
Vendor


[2] X38-1 CONFIGURE VENDOR/CLASS (

### Configuring Or Updating Vendor Codes

Parts are added by part number and vendor code. Both must be supplied
when adding parts to the system. A vendor code is assigned to define the
vendor whose parts you are selling. You may assign up to three characters
to a vendor code. Some examples may be:

MAN = Manufacturer
HON = Honda
CAS = Case

Type the three character code to be used as the vendor code. Press Enter.
The following screen appears.

L


X38-1 CONFIGURE VENDOR/CLASS

A&R EQUIPMENT SALES Parts Configuration 3610-101
vendor/Class Configuration
Enter ¥ to delete
Vendor Information
System address# ¢ Automatic ordering option
Part Number Special Process code
Segment. sizes Price Book assignment
Sort justification
Segment sort order Include Core Information
Sort method Dealer Number
Vendor's ID Default class

Cmdl-End job Cmd2-vendor List cmd3-Special Process Codes  Cmdd-Restart
Cmd5-Frice Book list

 

If the first vendor code you type is a new vendor, all fields will be blank. If
you have looked at or updated another vendor, the information from the
previous vendor will default in the fields. Defaults make it easier to add
several vendor codes at once.


[ «| X38-1 CONFIGURE VENDOR/CLASS

### Fields & Descriptions

Vendor

Name

System address#

Automatic ordering
option

3 characters. Required.

The code used to define the vendor. If you
are adding a vendor, the word NEW will
display next to the code. If updating, the
word CURRENT will display.

16 characters. Required.

Name of the vendor.

6 characters. Optional.

Vendor code set up in payables (X12-2).
Used for reference.

C, D, or A. Required.

The quantity of the part that will be ordered (
is determined by the Automatic Ordering
Option, the Order Method, and the part
Tecord.

A= Annualized. The annualized order
option will work with the Automatic (A) and
Combined (C) order codes.

Under the Automatic order code, the
annualized option will require the part to
Meet the minimum number of calls assigned
for that part's class.

Under the Combined order code, the
annualized option will consider the
minimum and/or maximum stocking
quantity (see Chapter X3-8 Parts
Configuration Menu for more information).


X38-1 CONFIGURE VENDOR/CLASS Ls]

This method will order enough parts to
equal the amount of parts sold in the last
twelve months prorated to the days supply.

The Minimum (X3-2) equals = — (number
of sales in last 12 months / 365 * Days
Supply) - (quantity onhand+ quantity
ordered).

The “Days Supply" is entered in Create
Suggested Stock Order, X341.

C= Case. More parts will be ordered if you
choose this method. The amount ordered
will equal:

The Maximum (X3-2), adjusted for per job
and package quantity, minus what's On hand
plus Available (X3-2),

D=DIS. Less parts will be ordered if you
choose this method. The amount ordered
will equal:

The Minimum (X3-2), adjusted for per job
and package quantity, minus what's On hand
plus Available (X3-2).

For either method, C or D, if the Economic
Order Quantity (EOQ X38-1) is greater, the
amount calculated by the EOQ will be
ordered,


[ «| X38-1 CONFIGURE VENDOR/CLASS

Special Process
Code

Segment sizes

    

   

Sort justification
Segment sort
order

Sort method

Price Book

Once the vendors are configured, and parts have been added to the
system, DO NOT MAKE ANY ONE SEGMENT SMALLER than it
| was. You can only make segments bigger. If there is a need to make
| Seaments, contact the DIS Response line for assistance.

5 characters. Optional.

Only valid if a HONDA of America or
CASE communicating dealer. Use the code
that matches your communications software.
4 fields of 2 digits each. Required.

Part numbers can be up to 18 characters
long. They can be divided into four
segments. You can use only one segment or
all four.

Note:

 

     

    

4 fields of 1 character each. Required. R=
Right, L = Left. Use a sort justification for
each segment. You may change the sort
justification anytime you choose.

4 fields of 1 digit each. Required.
Determines which segment will sort first,
second, third and fourth. You may change
the sort justification anytime you choose.
1 character. Required.

A=all vendors except Ford.

B = Ford. Sort method B ignores alpha
characters when it sorts.

8 characters. Optional.


Assignment

Include Core Information
Dealer Number

Vendor's ID

Default class

X88-1 CONFIGURE VENDOR/CLASS [7]

Name assigned to the vendor's price book in
X37-4 Create/Update Price Book. The price
book typed here will be used at Point of Sale
(X5-1), when selling a part for this vendor.

2 characters. Y/N.

10 characters. Optional.

Number assigned by the vendor to the
dealership. Used with some communications
packages. If the number is required, the
details will be provided in the
Communications Manual.

5 characters. Optional.

Vendor ID used in some communications
packages. If the number is required, details
are provided in the Communications
Manual.

1 character. Required.

Parts can be added quickly at Point of Sale.
When parts are added, they must be placed
in a class. Any parts added at Point of Sale
will be placed in the Default class. If you
want to move parts from this class, see Parts
Posting and Maintenance.

When parts are added to the inventory in
other jobs, this class will be the default. It
can be changed to any configured class (See
Adding a Class) while adding parts.

Below is a sample of ABC Company adding the vendor Manufacturer:


Fs | X38-1 CONFIGURE VENDOR/CLASS

ABC COMPANY Parts Configuration 3810-201
Vendox/Class Configuration

Vendor MAN ~ NEW

Enter Y to delete

Vender Information

System address# Automatic ordering option D
Special Precess code
Price Book assignment MANBOOK

Segment sizes 0g 0 07 06
Sort justification L R ROL
Segment sort order 2 1 4 3
Sort method aA

Qmdl-End job  cmd2-Vendor List
OmdS-Price Book list

 

 

 

 

Command Key Options
Cmd1-End job
Cmd2-Vendor List

Cmd3- Special Process Codes

Cmd4-Restart

Dealer Number
Vendor's ID
Default class

Cmd3-Special Process Codes  cmdd-Restart

 

When the fields are complete, press [Enter] to add the vendor.

End the job.

Displays the current vendor codes
already set up.

Gives a current list of available
special process codes. Currently
HONDA = Honda of America and
CASE = Case, THERM = Thermo
King.

Allows you to restart at the vendor
~~,


X38-1 CONFIGURE VENDOR/CLASS |

code screen without exiting the job.
If you press Cmd4- Restart without
pressing Enter, the information typed
on the screen will be ignored.
Changes will not be made and new
vendors will not be added.

Cmd5-Price book list Displays the list of price book
currently on the computer. Used in
the Price Book assignment field.

### Configuring Or Updating Classes

Classes are used to combine parts that have the same characteristics. For
example, parts can be classed as fast moving, by demand, by pricing, by
order method. The rules governing a class are defined in this job. Parts are
added in other jobs. The characteristics of the parts are defined on a part
by part basis, Certain information entered here will default at when adding
parts. This makes adding parts easier. The same rules apply whether you
are adding or updating a class code.

Classes are defined on a vendor by vendor basis. You can use the same
classes for all vendors. For example, ABC Company has two vendors.
They are Manufacturer and Distributor. The vendor codes are MAN =
Manufacturer and DIS = Distributor.


pos

10 | X38-1 CONFIGURE VENDOR/CLASS ff

The same classes of parts are assigned to each vendor. They are:

D = Default

F = Fast Moving
S = Slow Moving
O = Obsolete

Each class will be added to each vendor. At the vendor Prompt, type the
vendor code that the class code is assigned or will be assigned to. ABC
Company has entered MAN = Manufacturer. The following screen

appears:

Parts Configuration x3810-101
Vendor/Class Configuration
Enter Y to delete {
Vendor Information
System addresst Automatic ordering option D

Special Process code
Segment sizes 04 04 07 06 Price Book assignment MANECOK
Sort justification Lb RR L ----Division Information:
Segment sort order 2 2 4 3 Dealer Number POG3s
Sort method aR Vendor's ID

Default class

Cmdl-End job Cmd2-Vendor List cCmé3-special Process Codes cndé-Restare
Grd5-Price Book list

 


X38-1 CONFIGURE VENDOR/CLASS

To add or update a class, press Enter. The class prompt appears, as
illustrated below:

ABC COMPANY Parts Configuration 3810-101
Vendor/Class Configuration
Vendor MAN - CURRENT Enter Y to delete
Vendor Information -
System address# Automatic ordering option D
--- Part Number Special Precess code
Segment sizes 04 04 07 06 Price Book assignment MANBOOK
Sort justification Lb R RL ----Division Information:
Segment sort order 2 1 4 3 Dealer Number P0435
Sort method A Vendor's 1D .
Default class

 

 

 

DIS-3200 Vendor updated - enter Class Code if desired
Cmdl-End job Cnd2-vendor List Cmd3-Special Process Codes  cmdd-Restart
Cmd5-Price Book list

Note:

When configuring vendors, a Default Class is selected. Parts added in

classes are configured, you MUST configure the Default class - no
exceptions.


[| X38-1 CONFIGURE VENDOR/CLASS

D Type the code for the class you want to configure or update. Press Enter.

The following screen is displayed:

Parts Configuration x3810-101
Vendor/Class Configuration

Enter ¥ to delete
Vendor Information ~
System address Automatic ordering option D
Special Process code
Segment sizes 04 04 07 06 Price Book assignment MANBOOK
Sort justification 4 R RL ---*Division Information
Segment sort order 2 2 4 3 Dealer Number P0435
Sort methed A Vendor's 1D
Default class A
Enter ¥ to delete
Class Information
Name FAST MOVING Order code A
Automatic pricing ¥ #Days supply 054
Price Percent Base Update -- Minimom -- Factor = 1
4-Dlr. List 1050000 3 ¥ Number #Months Acq cost 050
3-Sugg. List 1000000 3 Calls 0902 008 inv ovhd 040
2-Internal 1000000 2 Calls 0003 015
2-Dir. Net 10co000 And/Or for minimum 0 Last Receipt ¥

Gmdi-End job  Cmd2-Vendor List cmdd-Restart

 

If the class is being added, the word NEW will display next to the class
code selected. If this is the first class you have worked with or are adding,
all the fields will be blank. If you have looked or updated a class
previously, information from the previous class will default in the fields.
Default information makes adding several classes easier and faster.

If the class is to be updated and not new, the word CURRENT will display

next to the class code selected. The above screen displays the fast moving
class for Man at ABC Company. The fields are defined below:


X38-1 CONFIGURE VENDOR/CLASS [=]

### Fields & Descriptions

Name 22 characters. Required.
Name of the class.

Order Code 1 characters. Required.
A= Automatic
C= Combined
M= Manual.
For details, see X3-8 PARTS
CONFIGURATION MENU.

Automatic Pricing 1 characters. Required.
Y= Yes, N=No. If Y (Yes) is selected,
prices for parts in this class can be updated
automatically by Reprice Parts (X37-1) or
Price Tape Update (X37-2). If N (No) is
selected, neither job will affect the parts in
the class.

Note:

Individual price fields are restricted by Y/N in the column labeled
"Update."

 

#Days Supply 3 digits. Required.
Used in Create Suggested Stock Order
(X341-1). Order quantity will be adjusted
for number days of supply entered here.


X38-1 CONFIGURE VENDOR/CLASS

E0Q

A system generated stock order is created using X341-1 Create Suggested
Stock Order. A formula is used to calculate the order quantity of parts
based on the Order Code selected in this job. At the same time the order
quantity is figured, the EOQ, Economic Order Quantity is also calculated.
This figure illustrates the most economic quantity of the part to order.

The greater of the calculated order quantity or EOQ will display on the

suggested Stock Order.

The formula for the EOQ, economic order quantity is:

The square root of: (Last 12 months pieces sold) X (EOQ Factor)

(Inv Ovhd)

E0Q Factor

ACQ Cost

Inv Ovhd

X (Acq Cost)

i digit. Optional.

Use 1 if using Automatic Order Option = C.
Use 2 if using Automatic Order Option = D.
3 digits. Optional.

Acquisition cost of the part. What
percentage of the cost of the part does it take
to order the parts. Use percentage from 0 to
100% Example: At ABC Company, 50% is
used. If the part costs $6.00, ABC Company
is saying that $3.00 of the cost is in
ordering. Enter 50% as 050.

3 digits. Optional.

Amount of dollars it costs to stock the parts.
What percentage of the inventory dollars
does it cost to keep the part on the shelf. Use
percentage from 0 to 100%.


X38-1 CONFIGURE VENDOR/CLASS |

ABC Company feels that 12% of each
inventory dollar is the cost to them to stock
the part. Enter 12% as 012.

Example. ABC Company sells Manufacturer
parts. Manufacturer estimates 40% of every
dollar of inventory is acquisition cost.
Industry standard also states that 12% of
every inventory dollar is overhead cost. The
Automatic Order Option chosen when
configuring the vendor is D. The fields
would be filled in like this:

Factor 2
Acq cost 040
Inv ovhd 012


X38-1 CONFIGURE VENDOR/CLASS

REMANUFACTURED PARTS

Warning!

Include Core Information=Y

As of 9/97, Case is the only vendor who provides core information;
however, as other manufacturers make it available on their price tapes, it
will be included in your DIS price book automatically. Ail you need to do
is set a flag in Configure Vendor/Class, “Include Core Information" to
"Y." Then you can take full advantage of the reman parts and core features
immediately.

The conversion, which runs automatically when the reman software is
installed, sets this flag to "Y" for Case (CAS), "N" for all other
vendors.

  
 
 
 

 
  
  

Note:
If you don’t want to change the way you have been handling cores and|
prefer Case’s pricing the reman part and core separately, you should
change "Include Core Information” to "N" for the Case vendor.

    

Identifying Parts with Core Codes

If you have previously used core codes and you plan to use DIS's method
for handling cores, you will need te remove the existing core codes. If
you fail to do so, the cores will be sold twice. New users can use regular
core codes and then switch. To identify these parts, run the Core Inventory
Pad (X36-20), and remove the core codes in Parts Posting & Maintenance
(X3-2).

Identifying Reman Parts

To identify remanufactured parts in your inventory, run the report,
Remanufactured Parts Inventory Pad (X36.22-5). This report compares


X38-1 CONFIGURE VENDOR/CLASS

parts in your inventory with the price book and lists parts that have reman
information attached to them in the price book.

Separate Classes for Reman Parts & Cores

In addition to the "Include Core Information” flag, you need to establish
separate classes for reman parts and for cores. For Case, reman parts must
be in a class where "Case comm. update” is set to "N,” because Case
prices reman parts and cores separately while DIS prices the reman part at
the total cost including its core. If you plan to use the features of reman
parts, you want to use the DIS pricing method. Reman parts are ordered
just as any other part.

Price Tape Updates

You need to keep in mind that Dealer Net and Suggested List include the
price of the core. When a price tape update is run and prices are bumped
up according to the values set in Vendor/Class Configuration (X38-1),
many dealers reprice from Suggested List to Dealer List at 110%. Core
values are repriced right along with the reman part. While this will not
make a big difference for many reman parts, it could make a significant
difference for items with very expensive cores. Furthermore, core values
have no consistent relationship to the prices of reman parts, so you can’t
reprice all reman parts by a fixed percentage or based on the value of its
core.

Repricing Cores

For example, a reman part whose suggested list is $200 (including its $50
core) is repriced by 110%. Now its dealer list is $220. The $220 represents
$165 for the reman part ($150*110%) and $55 ($50*1 10%) for the core;
however, the core value is still only $50. On the customer’s invoice, the
reman part will be sold at $170 and the core at $50. This $5 difference
may make no difference at all. However, suppose the reman part was
$1280 and its core cost, $200. Now there will be a $20 difference. You


[| X38-1 CONFIGURE VENDOR/CLASS

Just need to be aware and, if you are concerned about the larger value
Cores, reprice the parts manually in Parts Posting & Maintenance (X3-2).

On Hand Quantities

A reman part has an on hand quantity which includes its core. The core
has no on hand quantity until it is retuned. The price of the reman part
includes the cost associated with the core. If you order 1 reman part and
receive it through Case Automatic Order Receive (8713-5), it will be
received with an on hand quantity of 1. The associated core number will
not be added to your inventory, and you won’t need to add it unless it is
returned.

Selling Reman Parts

When you sell the part at Point of Sale, the system will sell the reman part
and its core. The total price will be the same as the dealer list associated
with the reman part; however, it will be listed on 2 separate lines: the
reman part and the core. The system will look up the cost associated with
the core in the price book and sell the core at that price. Then it calculates
the price of the reman part by subtracting the cost of the core from dealer
list. For example, if the dealer list of the reman part is $2,500 and its core
cost is $500, the invoice will show the reman part at $2,000 and the core at
$500.

Dirty Cores

When the customer returns the dirty core, you’ll add the core part number
to your inventory. You'll need to do this through Parts Posting &
Maintenance before you accept the return so you can make sure it is
assigned to the special class you set up for cores. You will "sell" a quantity
of -1 on the invoice and only then will the core have an on hand quantity
of 1. (If you add the core part number from the detail line, make sure you
sell it at base 1 or 3 so it won’t be marked up, and re-assign the part to the
core class ASAP.)


X38-1 CONFIGURE VENDOR/CLASS |

Core Costs

On Case’s price tape, dealer net (cost) and suggested list prices are the
same for cores. By keeping cores in a separate class, you can price them at
100% of Case’s prices. That way you'll be sure that retums are not given
at a markup price. When a dirty core is returned, the credit will be at the
same price as it would be sold today. The price could be slightly different
than its selling price if Case changes core prices, but it would not be at
your usual dealer net.

Cores are Ordering - NOT!

never All that will ever be in the core class are dirty cores, and they can be

ordered. returned to the manufacturer. Unless a customer returns a dirty core and
you give them credit, you will never have an on hand quantity for a core.
Cores are never ordered.

Returning Cores

Also, by keeping cores in a separate class, you can run a parts pad to see
how many dirty cores you have. When you’re ready to return the cores,
use Create Stock Return (X35-1) for that class and leave minimum and
maximum values blank.

A flag indicates whether you want core information to be included in the
price book. The flag, "Include Core Information” must be set to "Y" to
enable several features. The conversion, which runs automatically when
the remanufactured (reman) software is installed, sets this flag to "Y" for
Case (CAS), "N" for all other vendors.

Even though the core information flag is already set for Case, you need to
go into Configure Vendor/Class to set up separate classes for reman parts
and cores. Core part numbers with an on hand quantity represent dirty
cores, which can be returned to the manufacturer.


X38-1 CONFIGURE VENDOR/CLASS _

 

Setting Up a Class for Reman Parts

O From the Parts Configuration Menu, select Configure Vendor Class
(X38-1).

C At the vendor prompt, type CAS and press [Enter]. The Vendor/Class
Configuration screen is displayed, as illustrated below:

A&R EQUIPMENT SALES Parts Configuration 3810-101
Vendor /Class Configuration

Vendor Information
System address# Automatic ordering option a
Special Process code cASE
Seoment sizes 10 90 09 00 Price Book assignment —_W.CASEMK
Sort justification u --Division Information
Segment sort order 1 9 0 0 Include Core Information (
Sort method a Dealer Number 0022385800 .
Vendor's ID Default class A

Cmd1-End job Cmd2-Vendor List Cmd3-Special Process Codes  Cmd4-Restart
Cnd5-Price Book list

 

O Make sure the prompt "Include Core Information" is "Y."

Press [Enter].

OD At the Class prompt, type the default class code and press [Enter]. The
default class information is displayed. The purpose for doing this is just

 

 

 

 

CL


X38-1 CONFIGURE VENDOR/CLASS

to establish some of the values for the new class so you don't have to
enter them all from a blank screen.

C1 Press [Enter] again. Now you'll have another blank class prompt.

C1 Type the class code you want to use for reman parts, such as R.

ASR EQUIPMENT SALES Parts Configuration x3810-101
Vendor/Class Configuration
Vendor CAS - CURRENT

Vendor Information --~ aan eea nn

 

System address# Automatic ordering option A
Special Process code CASE
Segment sizes 10 00 ¢0 00 Price Book assignment W.CASEMK .
Sort justification L
Segment sort order i ¢ 0 0 Include Core Information
Sort method A Dealer Number 0022385800
Vendor's ID Default class A

Class R - NEW Enter ¥ to delete

- Class Information

Name REMAN PARTS Order code A .
Automatic pricing ¥ #Days supply 054

Price Percent Base Update ++ Minimum ~-

4-Dly. List 1100000 3 ¥ Number #Months Acq cost 050 F

 

3-Sugg. List 1000000 300 ¥ Calls 0002 006 Inv ovad 022
2-Internal 1050000 1 ¥ Calls 00003 012
A-Dlr. Net 1000000 1 oy And/Or for minigum 0 Last Receipt ¥

Cmai-End job md2-Vendor List cmdd-Restart

 

### Very Important

Make sure the "CASE comm. update" flag is set to "N." You will be
relying on price tape updates to reprice reman parts, so you'll probably
want "Automatic pricing" set to "Y." You can set the order method and
pricing for this class any way you want.

 

 

 

 


X38-1 CONFIGURE VENDOR/CLASS

O When you are done, press [Enter]. You'll have another blank class code.
Now you'll need to set up a class for cores,

Setting Up a Class for Cores

O Type the class code you want to use for cores, such as "C," and press

[Enter].

A&R EQUIPMENT SALES

Part Number

Segment sizes

Segment sort order
Sort method

class ¢
Name DIRTY CORES
Automatic pricing ¥

4-Dlx. List 1000000
3-Sugg. List 1000000
2-Internal 1000000
i-Diz. Net 1090000

Parts Configuration X3820-201

Vendor/Class Configuration

vendor Information
System address# Automatic ordering option A

Special Process code CASE

10 06 00 00 Price Book assignment W.CASEMK
Sort justification L
1000 Include Core Information


Dealer Number 0022385800
Vendor's ID Default class A
Enter ¥ te delete

- Class Information

Order code M

“Days supply 054 77 BOQ ----
Price Percent Base Update -- Minimum -- Factor 1


¥
x
¥

Nunber #Months Acq cost 050
Calls 00002 006 Inv ovhd 012
Calls 00003 12
And/Or for minimum 0 Last Receipt ¥

Cmdl-End job Cmd2-vendor List Cmd4-Restart

 

0 The fields that really matter are:
- Order code = M. You will never order cores.
+ Case comm. update = Y. This is really your choice. If you want to
have the latest price for the core from Case, enter "Y"; otherwise, "N."


X38-1 CONFIGURE VENDOR/CLASS [2]

- Percent fields for all prices should be 100%. On Case's price tape
Dealer Net and Suggested List are the same. You don't want to bump
them up by the percentages you use for other classes. Doing so would
result in giving the customer more credit for a dirty core than they paid
for it when they bought the reman part.

O When you are done, press [Enter].

O Press [Cmd1] to end the job.

### Core Information In The Price Book

When Include Core Information=Y in Configure Vendor/Class (X38-1),
core information is present in Display/Print/Change Price Book (X37-3).
New part numbers show the remanufactured part number and its primary
core. The primary core points to one or more alternate cores if there are
any.
New part # E>) Reman part #
Reman part #E) Reman Price/Primary Core Price/Primary core #
Primary core tHE) Alternate core # (if any)
On the next few screens a complete chain will be illustrated. Note that

there is not necessarily any correlation between the new part number and
the reman part number or their associated core part numbers.


X38-1 CONFIGURE VENDOR/CLASS

 

AGR EQUIPMENT SALES
Division a
Part Number

DISPLAY PRICE BOOK
Case Price Book with Core Info 9-15-97
Description. Sug.List Dlr.Net Rtn Pkg mit

¥3730-301

1958078C2
19ss078c1
2958079¢2
19580791
1958080Cc1
1956081c1
1958082¢1
1958082c1
19580831
asssosser,
1958085¢1
195a086ci
1958120¢1
1958159¢2
1958164C1
jgseissci
1958166c1
1988167¢2
195816ac1

PUMP/A, 2381.20
REMAN: 1958079C1
REMAN-PUMP 1817.20
REMAN: $ 1517.20 CORE: §
CORE-PUMP 300.00
REMAN; 1958082c1
REMAN-MTR 2358.45
REMAN: § 1058.45 CORE: §
‘CORE-MOTOR, 300.00
REMAN-MTR 2404.54
REMAN: § 2104.54 CORE: ¢
CORE-MOTOR 300.00
VALVE 79,88
VALVE 138.03

23,19
2.96
BLADE 22.32
BLADE 35.98
BRACKET 3.30

1788.90 % = 2

1399.26 2
300.00 # 1979636C1
300.00 1

1074.26 1
300.00 4 1958083C1
300.00 1
1851.74 1
300.00 # 1958086c1
300.00 1

55.96
103.51,

15.07

1.63

15.63

25.18

1.99

Enter part number to begin next page: 1958i68C1

Qmdi-End Job

 


X38-1 CONFIGURE VENDOR/CLASS

The following screen shows an example of a Primary Core:

ABR EQUIPMENT SALES DISPLAY PRICE BOOK X3730-301
Division A Case Price Book with Core Info 9-15-97

Part Number Description Sug.List Dlr.Net Rtn Pkg Mit

1979636c2 ALT CORE: i9ssosoci

1979641 STRIPPER 27.55 16.53
1979640c2 PLATE 5.50 3.29
19796a2c1 PLATE 6.31 3.79
a979644cr CLIP 2.36 1.30
197965¢C1 STRIPPER 27.58 16,83
19796551 TSE 28.30 16.98
2979658¢1 TUBE 42.87 28.29
19796661 TUBE/A 42.39 27,97
1979667C1 CABLE/A 60.67 45.50
1979669C2 STRAP 19.95 13.95
1979668C3, STRAP 19.95 13.95
1979670¢C1 TEE 28.70 27.22
1979672c1 TEE 23.13 13.88
1979674CL SUPPORT 5.98 3.88
1979680c1 PROD GRAPH 37.99 28.48
1979681¢1 PROD GRAPH 33.82 25,16
1979682C1 PROD GRAPH 37.45 28.10
1979683¢1 PROD GRAPH 37.90 28.43
Enter part number to begin next page: 1979683C1
(mdl-End Job

PEP RP eee eee ee

 


26 | X38-1 CONFIGURE VENDOR/CLASS

The next screen is an example of an Alternate Core:

A&R EQUIPMENT SALES

Division A
Part Number
assBo80ci
495B081C1
19580821
1gss0e2c1
1958083¢1
195808S¢1
1958085C1
19580861
1988120c1
gseisec2
1958164c1
1958165CL
1gsei66c1
1958167¢1
2958168C1
1958169C1
1958170c1
2958172C1
1958173C1

DISPLAY PRICE BOOK

3730-301

Case Price Book with Core Info 9-15-97
Deseziption Sug.bist Dlr.Net Ren Pkg wit

CORE-PUMP 300.00
REMAN: 195808201
REMAN-MTR 1358.45
REMAN: $ 1058.45 CORE: §

CORE-MOTOR

BLADE
BRACKET
WASHER
PULLEY
ARM
BUSHING

300.

1074.

oo


300.60 # 1958083C1

1851.

7%


300.00 # 195g086c1

300.
55.
-52

15.
1.
15.
25.

Enter part number to begin next page: 1958173C1

cmdi-End Job

Gmdl-End Job


+86
1g.
19.

1.

a7
25


%

 

In the example below, you can see another example of the links from a
new part number to its remanufactured part number and the primary core.

This example will be used throughout the rest of the guide because the part

numbers are close together which makes it easier to follow.
NU


A&R EQUIPMENT SALES

Division A
Part Number
1971579¢2
1971579¢2
1971582
is71ssoca
ag7issoca
1971582¢1
1971582c1,
1972582cL
1971583c.
1971583C1
19715841
1972585c1
1971586C1
1971588c1
1971589¢2
197259A1
197159¢2
1971590¢1
1971592c1

X38-1 CONFIGURE VENDOR/CLASS [=]

DISPLAY PRICE BOOK x3730-301
Case Price Book with Core Info 9-15-97
Description Sug-List Dlr.Net Rtn Pkg mit
MOTOR ASSY 5197.56 3898.17 % 1

REMAN: 1971580¢2
SHEET RH 222
asad,

REMAN: § 3144.11 Co?
400.
1774

REMAN: 1972583CL
REM VALVE 1567

REMAN: $ 1267.03 CORE:
CORE-VALVE 300.
KIT/SEAL 104.
PUMP RIT 1934.
GASKET a.

PUMP KIT 1934

PLATE 6.
SHEET 175.

GASKET 24
PACKAGE 138

+28
1d

$
00
40


§
00
17
27
27
-81
40
91
23
91

82.48 1
2752.74 2
400.00 # 1971581¢1

400.00 a
1330.80 1

1220.28 # 1
300.00 # 1971584c1
300.00 i

78.13
1450.70

3.20
1451.21

4.17
119.62

18.17
104.18

Enter part number to begin next page: 1971592C1

(mdi-End Job

### Core Information At Parts Inquiry

 

Price books are selected automatically, which is also true for Parts Posting
& Maintenance but not for Point of Sale. The core code field can be used
to exclude part numbers from the Parts inventory Pad; however, it is not
necessarily related to remanufactured parts.


28 | X38-1 CONFIGURE VENDOR/CLASS

When you inquire on the new part number for the motor assembly, the
remanufactured part number is displayed at the bottom of the screen:

AER EQUIPMENT SALES PARTS INQUIRY 3200-102
Division: a INFORMATION

Vendor: CAS Part Number: 1971579c2 Description: MOTOR ASsY
Class.: A Quick code.+ Location...:

Available..: Part category. Order code: A Return code: %
Reserve R/O: Supersede code: Stock code: Qty. Break : N
Superseded by.: Core code
Supersede aty.:
Base Weight..: 246.0
4-Dlx. List: 5717.32 3
3-Sug. List: 5457.44

2-Internal.: 3898.27
1-Dir. Net.: 0389817
Non-PTY aty: i oty req: Last xept gty.:
PTY qty. ...: Package: 1 hast rept dat
Returns... : Mult. . Dealer order #:
Last count
Last sale..:
Date added. :

REMAN: 1971580C2
‘DIS-3303 Paxt was found in price book, not in inventory.
Fl-End Fi-Hist Fd-Orders F5=Division F7=Supersession F8=Index F9=Source supply
FlisxRef F12=Comms F13=Notebook F16=0rd.Hist

 

When you inquire on the remanufactured part, the primary core number is
displayed at the bottom of the screen.


X38-1 CONFIGURE VENDOR/CLASS | 20 |

AGR EQUIPMENT SALES PARTS INQUIRY 3100-101
Division: A INFORMATION
CAS Part Number; 1971580c2 Description: REM. MOTOR
Quick code.: Location...:

Available. .: Part category. : Order code: A Return code:
Reserve R/O: Supersede cod: Steck code: Qty. Break : N
Reserve C/T: Superseded by. Core code

On hand,...: Supersede cty

Price upd..: Base Weight..: 235.9

4-Dlr. List: 3898.52

3-Sug. List: 3721.32

2eInternal,; 2752.71

1-Dle. Net.: 0275271

Non-PTY gty: ins: Qty req: Last rept qty.:

PTY qty....: Package: 1 Last rcpt date:
Returns....: Male... Dealer ordex #:

Last count.:

Last sale
Date added.:

 

REMAN: $ 3498.52 CORE: $ 400.00 # 2971581¢1
DIS~3303 Part was found in price book, not in inventory.
Fisind F3-Hist Fé=Orders F5=Division F7=Supersession FéeIndex F9=Source Supply
Fil-XRef Fl2=Comms Fi3=Notebook F16=Ord.Hist

Dealer list for the remanufactured part is calculated from the percentages
specified in Configure Vendor/Class (X38-1). Note that the total list price
of the remanufactured part is separated to show its list price minus the cost
of the core.

An inquiry on the primary core part number is illustrated below. If there
were an associated alternate core, its information would be displayed at the
bottom of the screen.


AGR EQUIPMENT SALES PARTS INQUIRY %3100-101
Division: A INFORMATION

Vendor: CAS Part Number: 1971581C1 Description: CORE MOTOR
Class.: A Quick code.; Location... :

Available..: Part category.: 3 Order code: A Return code:

Reserve R/O: Supersede code: Stock code: Qty. Break : N
Reserve C/T; Superseded by.: Core code
On hand.. Supersede qty.:

Price upd

4-Dlr. List: 440.00

3-Sug. List: 420.00

Q-Internal.: 400.00

i-plr. Net.: 0040000

Non-PTY aty: Mins: oty rea: Last rept qty:

PTY qty....: Package: Last rept date:
Returns. Mult...: Dealer order #:

Last count.:

Last sale.,:

Date added.:

DIS-3303 Part was found in price book, not in inventory.
Fi-End FisHist F4=Orders F$=Division F7=Supersession Fé=Index F9=Source Supply
Pll=xRef F1l2=Comms F13=Notebook F1é=0rd.Hist

  


X38-1 CONFIGURE VENDOR/CLASS

Searching for Reman Parts

The most accurate way to list the remanufactured parts in your inventory is
by printing the Remanufactured Parts Inventory Pad; however, most
remanufactured parts are identified as such in their description fields. You
can search for reman parts by typing a question mark (2) in the part
number field. The search screen displays a list of part numbers beginning
with the first number in your inventory. On the input line, type *REMAN,
and press F5=Search by description. A list of parts that have "REMAN" in
their description fields is displayed.

AGR EQUIPMENT SALES PARTS INQUIRY 3100-101,
Division: A INFORMATION
Vendor: CAS Part Number: ? Description:
Class.:
Search Parts for Division A x30020
Availab | Change search field and press Enter to search
Reserve | by part# or FS to search by description.
Reserve { Enter 1 to select pact#.
on hand ‘REMAN
Price u | Opt vVendor/Part Number Description
4-Dix. cas 1934206¢1 REMAN PUMP
3-Sug. 1934208C1 REMAN PUMP
2-Inter cas 1934212c1 REMAN PUMP
i-Dir. cAS 1934214C1 REMAN PUMP
Non-PTy CAS 1935062c2 ‘REMAN-MON
PTY qty cas 1958076C1 REMAN-MTR
Returns
Last co
Last sa
Date ad FS=Search by description Roll

FlsEnd xce Supply
Fll=xRef F12=Comns F13=Notebcok Fl6=0rd.Hist

 


38-1 CONFIGURE VENDOR/CLASS

### Core Information In Parts Posting & Maintenance

If the same part numbers are in inventory, the same information is
displayed as in Parts Inquiry. The following screens show the same parts
as they were added from the price book.

Parts Posting and Maintenance ¥3200-101
Part Information
Vendor: CAS Part number: 1971579¢2 Description: MOTOR ASSY
Class.: A Quick code.: Location...:

Available..: Part category Order code: A Return code: %
Reserve R/O; Supersede code: Stock code: Qty.Break:
Reserve C/T: Superseded by.: Core code:
On hand. . Supersede aty.
Price upd..: / / Base Weight.
A-Dlr. List: 571732 3
3-Sug. List: 545744 3
2-Internal.; 389817
1-Dir. Net.: 0389817
Non-PTy gry: ine: Qty rad: Last rept gty.;
Pry qty ot Package: 1° Last rept date:
Returns. weet Dealer order #:
Last count.: 00/00
uast sale..: 00/00
Date added.: 09/97
REMAN: 19715802

Fistnd F2-Information F3=History F4=Transactions F5=Source Supply
FllsxRef Fi3=Notebook

 


A&R EQUIEMENT SALES
Division: A

X38-1 CONFIGURE VENDOR/CLASS

Parts Posting and Maintenance x3200-201
Part Infermation

Vendor: CAS Part number: 1971580c2 Description: REM. MOTOR
Class.: R Quick code.: Location.

Available.
Reserve R/
Reserve ¢/'
on hand a

Part category.: 3 Order code: A Return code:
Supersede code: Stock code: Qty Break: WN
Superseded by.: core code:
Supersede qty.:

Price upd..: 00/00/00 Base Weight 2359

4-Dlr. List: 389852
3-Sug. List; 372132
2eInternal.: 275272
1-Dir. Net.: 0275271
Non-PTY qty:

PIY qty

Returns...

Last count.:

Last sale..:

Date added. :

Qty xqd: Last rept aty.: 2
Package: Last rept date: 09/16/97
Male. Dealer order #; MANUAL

REMAN: $ 3498.52 CORE: $ 400.00 ¥ 19715B1C1

FisEné F2-Information F3=History F4=Transactions F5=Source Supply
Fll=XRef F13=Notebook


| sa X38-1 CONFIGURE VENDOR/CLASS

You don't need to add the core part number to inventory until it is
returned. Add it through Parts Posting & Maintenance, make sure it is
Te-assigned to the class set up for cores, and make sure its dealer list is the

same as Case's cost and

AGR EQUIPMENT SALES
Division: A
CAS Part number:
Quick code. :

Available. .
Reserve R/O:
Reserve C/T:
On hand.

Price upd..:  / 7
4-Dir. List
3-Sug. List:
2-Internal.
i-Dir. Net.
Non-PTy aty:
Last rept gty.:
PIY qty....:
Returns
Last count.:
Last saie..;
Date added. :

Bas
40000 3
40000 3
400002.

9040000

00/00
covoo
09/97

suggested list.

Parts Posting and Maintenance

x3200-101

Part Information

1971581¢2

Part category.: 3
Supersede code:
Superseded by.
Supersede gty.:

2 Weight..: 2000

Description: CORE MOTOR
Location. ..:

Order code: M Return code:
Stock code: Qty.Break: N
Core code:

Remove core codes
so cores will not be
sold twice!

2 bast rept date: /
Dealer order #;

FisEnd FasInformation P3-History Fé=Transactions FS=Source supply
FllsxRef F13=Notebook

 

Re-assign cores to the class set up for cores. Filed exit through Dealer List
and Internal to allow the system to reprice them.

Cores will have no on hand quantity until they are retumed as dirty cores.


X38-1 CONFIGURE VENDOR/CLASS

Searching for Reman Parts

The most accurate way to list the remanufactured parts in your inventory is
by printing the Remanufactured Parts Inventory Pad; however, most
remanufactured parts are identified as such in their description fields. You
can search for reman parts by typing a question mark (7) in the part
number field. The search screen displays a list of part numbers beginning
with the first number in your inventory. On the input line, type *REMAN,
and press F5=Search by description. A list of parts that have "REMAN" in
their description fields is displayed.

AGR EQUIPMENT SALES Parts Posting and Maintenance 3200-101
Division: A Part Information
Vendor: CAS Part number: ? Description:
Class.:
Search Parts for Division A x30020
Availab [Change search field and press Enter to search
Reserve [by part# or FS to search by description.
Reserve |Enter 1 to select part#.
on hand *REMAN
Price u opt Vendor/Part Number Description
4-Dix. CAS 1934206C1 REMAN PUMP
3-sug. CAS 1934208C1 REMAN PUMP
2-Inter cas i934212c1 REMAN PUMP

1-Dir. CaS 1934214c1 REMAN PUMP
Non-Pry cas 1935062c2 REMAN-MON
PTY aty cas 1958076C1 REMAN-MTR
Returns

Last co

Last sa

Date ad = F3=Exit FSeSearch by description Roll

Fisind
Fll=XRef F13«Notekook

 


X38-1 CONFIGURE VENDOR/CLASS a

 

### Core Information On The Parts Inventory Pad

In the core field , you can assign and exclude up to 6 core codes from the
parts pad; however, core codes are not necessarily related to
remanufactured parts.

A&R EQUIPMENT SALES PARTS INVENTORY PAD 3610-001
SELECT

Core Codes to Exclude. .

PRINT
Dealer List Price
Suggested List Price
Internal Price...

Dealer Net..

Qrdl-Cancel Cmd2-Select Divisions

Enter-Continue

 

The portion of the report that includes the motor assembly and its reman
part and core is illustrated on the next page.

LO


ABR EQUIPMENT SALES
LYNDEN, WA

Fert Nonber
19835
31429
11624
1us28
26187
16202

17596
17603
1924206c1

igaazeacr

t9se2uzc1
aspazaser
19342sa1

383506202

19380722
2972578c2

as7isacez

as7aseacs
23119
23150
2aur

30623
30634
31843

31682
32995,
33260
23261
24a,

34487
35648

AS cASE/TE

Remanufactured Parts tnventery Pad

case,

aH cas

Dealer

Description Cn Wand Rsrv Bin Loc List.

GAUGE z
GASKET z
SPACER 4
GASKET 5
BLADE 2
oamNG 7
oré: sopesons 5
PACKING, 2
SEAL a
REMAN POMP n
REMAN: § 1429.65 CORE: §
Ord: MARKK OS?
REMAN PUMP

EWAN; § 1400.83 CORE: ¢
ord: MARKK $3
REMAN PUMP 20
REMAN: $ 968.35 CORE: 5
REMAN PUMP. Fry
REMAN: § 957.33 CORE: $
BOLT-PAN

Ord: WARRK os 5.
REMAN-HON 10

REMAN: S$ 697.81 CORE: $
20

wOTOR ASSY
Rew: 1971500¢2
REM, MOTOR

7A92
oR,

3 7055
FILE
jada
sBL2A

sese

37.50
2.62
ag.ad
4.97
9.34
78

33.50

65138 3.30

200.09

200.00

3629.65
CORE + 193420702

1690.23,
CORE # 293420901

1018.35
CORE 4 1934213C1
1007.34,
cone # 192azrse1

743.8,
conz # 193506302

$727.32

3098.52

REO: § 3498.52 CORE: $ 600.00 coRE # 1971581c1,

CORE MOTOR

oRING ah

WASHER, ac
2

key

ausHING

BUSHING

BREATHER

Ord: sooteser s

PACKING

PACKING

WASHER

Gaseer

SPaING

ELEMENT

HOSE

cas case/TH

430.00

S862 83
68620 a7

SR
a6

5A63
sc62
5082

4039
5076
essic
6allA
a2
xer01
‘RACED

3.42
3.28
aaa
10.26

22.43
37
1.28
4.28
5.34
9.80
18.59

CAS CASEVIR

X38-1 CONFIGURE VENDOR/CLASS

Deeler
Net
9001193
esooa79
092305
090271,
0200637
9900046

occ0625
cocozes
0113779

0211767

2071099,

0076329,

oo0ei00

oce7se8

0200000
0389827

0275271

9040000
090081
ooo00s¢
002650
ooocaes:
oooo2ze
sooo2s2
000700

9900621
000066
000076
6000076
ecocz91
pocossa
9901268

Date 9/16/97
Time 14.37.14

Date Date == Sales ««
a7 ce ekg

els Lee
9786
9786
9786
9/86
9136
9726

9/86
gras

9786
9786
r0re6
10/86
9/86
9786
9786

9na6
9786
9786

loves
9086
9786

is P 96
10/86

3786

3786

5/88

5/85
18618
order Total:
ares

4285

3197

order Total:

order etal:

1786
1/86
vas
3/86
4/86
12/85
286 2
order Tera
ares
12785
1/86
878s
3186
aves
2788

cASEVIH

°

eoneo eo UD OO

Page


3619-28


PO

 


X38-1 CONFIGURE VENDOR/CLASS

 

### Remanufactured Parts Inventory Pad

This report is the Additional Parts Reports Menu (X36-22), It lists
remanufactured parts only. New parts that have associated reman parts are
not included. The associated core part number is referenced but the part
number itself is not listed as a separate line.

commanD
{c} DIS Corp.

+ Turn and Earn Report

- Group Inventory Replenishment Report
+ Inventory Quantity Drop Report

- Wholesale Customers Sales Analysis

- Remanufactured Parts Inventory Pad

Return te Parts Report Menu

Ready for option number or command
see 5

 

The selection screen is the same as the Parts Inventory Pad (X36-1):


X38-1 CONFIGURE VENDOR/CLASS

AGR SQUIPMENT SALES REMANUFACTURED PARTS PAD x3610-001
SELECT

Vendor (or ALL)

Class (or ALL)

Omd2-Cancel Cmd2-Select Divisions

Enter~Continue

 

The following is a sample Remanufactured Parts Inventory Pad


X38-1 CONFIGURE VENDOR/CLASS

 

ASR EQUIPMENT SALES Remanvfaccured Parts inventezy Pad Date 9/16/97 Pege 1
Lynpen, wa CASE/IN cas ‘Time 14.55.36 x3619-28

Dealer Desier Date Date == Sales

Part Number escription On Hand Rsv Bin tec List Net cls Let Le P 96 © 97 Ct Pkg PY
iezazoeca REMAN PUMP 2788 1625.65 0113779 a, 3/97 a4

REMAN: $ 1429.65 CORE: § 206.00 coRE « 193420701

Ord: MARKK S02 order Total:
1934z08c1 RERAN PUMP ao 1890.83 0211787 a

REMAN: § 1400.83 CORE: $ 200.09 » 193420901,

Ord: MAREK 33

193422203 REYAN POMP io 1028.38 vo7io93 &

REMAN: $968.38 CORE: 5 CORE + 1934213c1

a93a214e1 REMAN PUMP 10 2007.31 0070325 A,
REMAN: $ 957.31 CORE: $ core # 1934215¢2

1935062¢2 REMAN-HON 10 77a 0047588
REMAN: $ 687.81 CORE: $ CORE » 1938063¢2

197158002 EM, MOTOR 3898.52 0275271 a
RMON: $ 3498.52 cont: § cone # 2972S81c1,

 

CAS casesIH GAS CASE/TR AS CASE/IH

 


X38-1 CONFIGURE VENDOR/CLASS at |

CORE INFORMATION AT POINT OF SALE

Reman Parts at the Detail Screen

At Point of Sale, when the new part number is entered, the reman. part
number is immediately displayed to alert you to the possibility of selling it
instead of the new part number.

A&R EQUIPMENT SALES SALES ORDER x5100-106
COUNTER TICKET # CT00133 For FRANOL CHARGE OPEN 9/26/97

TDP Line # Qty Vnd Part Number Description Bin Ext Price

Spec order parts .00 Avail tetal : 00

PARTS CUSTOMER REMAN: 1971580C2

TD Pty Line SC Ven Qty Part number Price Base

A P 0010 PC cas 1 i971579¢2 571732, 4

Standard line code No demand

Available C/T Res. R/O Res. On Order Super. Bin Dir. List
o 0 0 0 8717.32

 

O Press [F6] to delete the line.


X38-1 CONFIGURE VENDOR/CLASS

SALES ORDER
For FRANO1

AGR EQUIPMENT SALES
COUNTER TICKET # CT00133 CHARGE OPEN

TDP Line # Qty vnd Part Number Description Bin

-00 Avail total
REMAN: 197158062
SC Ven  oty
PC CaS

Spec order parts
PARTS CUSTOMER

TD Pty Line Part number
A oo10
Standard line code No demand
Available C/T Res. R/O Res. on Order Super.

o ° 0 0

Bin

 

5100-106
9/16/97

Ext Price

00 (

Price Base

Enter the reman part number. Note: The reman part number remains on

the screen so that you can easily enter it on the detail line.

wo


X38-1 CONFIGURE VENDOR/CLASS

The following illustrates a Detail Screen with Reman Part on Invoice:

### Agr Equipment Sales Sales Order 5100-106

COUNTER TICKET # cT00134¢ For FRANOL CHARGE OPEN 9/16/97

TDP Line # Qty vnd Pazt Number Description Bin Ext Price
A 0010 PC 2 CAS 1971580C2 REM. MOTOR 3898.52


The core number will not be listed with the reman part as a
line on the ticket. If you see a core line here, it means you
have not removed the core code and it will be sold twice.

Spec order parts -00 Avail total 4202.62 Total 4202.61

PARTS CUSTOMER REMAN: $ 3498.52 CORE: $ 400.00 CORE # 1971581¢1

TD Pty Line sc Ven Qty Part number Price Base

A 0020 PC CAS 4

Standard Line code No demand .

Available C/T Res. R/O Res. On Order Super. Bin Dlr. List
1 1 oO 0 3898.52

Note that the reman part is placed on the invoice at its dealer list price.
Above the detail line, the cost of the core is subtracted and listed
separately along with the core part number. This is how it will appear on
the invoice.


a4 | X38-1 CONFIGURE VENDOR/CLASS

Reman Parts at Part Availability

The same features are available at Part Availability. If you enter the new
part number, the reman part number is displayed.

The screen below shows a new part number on the Part Availability
Screen.

AGR EQUIPMENT SALES PART AVAILABILITY crao134 =—-x$107-¢02

Sold by: FAL = Cust. Address: FRANO1 FRAN'S FARM Dec. Type: ¢
Sales code: PC Tax: A Discount: Price code: 4 Default vendor: cas
Part Number Qty Ven Description Avail Resrv Price Conments
1971579¢2 1 CAS MOTOR ASsY 0 a -00 NOT OK

REMAN: 1972580C2

avail Total +00 Document Total -00 Page Total

Help-Command Keys

 


X38-1 CONFIGURE VENDOR/CLASS, a5 |

This screen shows a reman part on the Part Availability Screen.

A&R EQUIPMENT SALES

Sold by: HAL Cust. Address: FRANO] FRAN'S FARM

PART AVATLABILITY c700134 = x5107-001

Doc. Type:

Sales code: PC Tax: A Discount: Price code: 4 Default vendor: CAS

Part Number
1971580c2

Avail Total <00

Help-Command Keys

 

Q@tv Ven Description avail Resrv Price Comments
1 CAS REM. MOTOR 1 0 -00 OK

REMAN: $ 3498.52 CORE: $ 600.00 # 1971581¢1

The cost of the core and its part number are

displayed. The price of the reman part is its
dealer list minus the cost of the core.

Document Total -00 Page Total

OC Press Cmd5-Add to Invoice.

 

 

 

 

When the invoice or work order is complete, press [Cmd2] to close and

print. A sample document showing 2-line invoicing for reman parts is

illustrated below:


X38-1 CONFIGURE VENDOR/CLASS

A&R EQUIPMENT SALES
Birch Bay - Lynden Road
Lynden, WA 360 354-5833
RENTALS --- SERVICE --- SALES
“We rent just about everything”
This month's special- 15% off scaffolding
Return Policy: Parts returned after 5 days are subject to a 10%
restocking fée.

FRANOL BRON, 'S FARM
P.O. BOX 89
BELLINGHAM WA 98227

Seid By: HAL PO #: Date 9/16/97 COUNTER TICKET CT00134

ip By: Tax #;
TD Qty Description Price Amount
AP ARTS CUSTOMER

CAS 1971580C2 REM. MOTOR 3498.52 3498.52
A 1 CAS 1971581CL CORE 400.00 400,00

** SUBTOTAL 3898.52
** SALES TAX 304.09
arge Sal

Beage (360)6 be 9002
$4202.61

 


X38-1 CONFIGURE VENDOR/CLASS

 

Accepting Dirty Cores at Point of Sale

When a customer retums a dirty core, it is handled like any other return;
however, it is important to make sure that you don't sell it at a markup. If
you add the core part number to inventory from the detail line at Point of
Sale, it will be assigned to your default class and marked up accordingly.
If this happens, make sure you sell the part at base 1 (dealer net) or base 3
(suggested list), not at base 4 (dealer list). The best practice is to press
[Cmd11] for Additional Options and use option 4, Parts Posting &
Maintenance, to add the core part number so you can make sure the class
and pricing are correct.

O On the detail line, "sell" a quantity of -1, as illustrated below:

A&R EQUIPMENT SALES SALES ORDER x5100-106
COUNTER TICKET # CT00138 For FRANO1 CHARGE OPEN 9417/97

TDP Line # = Qty Vnd Part Number Description Bin Ext Price

Spec order parts -00 avail coral
PARTS CUSTOMER

TD Pty Line sC ven ty Part number
A 0010 FC cas 1- 197158101
Standard line code No demand

 

OD Press [Enter] to put the returned core on the invoice.


as | X38-1 CONFIGURE VENDOR/CLASS

 

A&R EQUIPMENT SALES SALES ORDER xS100-106
COUNTER TICKET 4 CT00139 For FRANO1 CHARGE OPEN 9/17/97

TDP Line # Qty vnd Part Number Description Bin Ext Price
A 0010 PC d-cas 1971581¢1 CORE MOTOR 400,.00-

Spec order parts 00 Avail total 431.20- Total 432.20-
PARTS CUSTOMER

TD Pty Line $C Ven Qty Part number Price Base (
a 9020 PC CAS 4

Standard line code No demand

Available C/T Res. R/Q Res. On Order Super. Bin Dir. List

0 0 ° o 400.00

 

O Make sure the price of the core is not marked up. If it is, bring the line
down and change the Base to 3 or 1. It should correspond to the cost
listed on the original invoice; however, if the price has been changed by
Case in the meantime, it may be slightly different.

‘When the return is complete, the core part number will have an on hand
quantity of 1, which can be returned to the manufacturer.

Co


X38-1 CONFIGURE VENDOR/CLASS

 

    
      

Note:

 
 

If a customer returns a reman part that has not been used, "sell" a quantity]
of -1 of the reman part number, not the core. The reman part will be put
back into inventory where it can be resold.


X38-1 CONFIGURE VENDOR/CLASS C~

Pricing

Using this job, pricing is established on a class by class basis. The
"Percent" and "Base" fields are used to set defaults that will be used when
adding parts. When adding parts at Parts Posting and Maintenance (X3-2)
the defaults will display. You can change them.

There are four possible prices:

4= Dealer List The list selling price to customers

3 = Suggested List Manufacturer's suggested selling price

2 = Internal Dealer defined price fieid

1 = Dealer Net Dealer's cost of the part
(
i
NL


X38-1 CONFIGURE VENDOR/CLASS [*]

### Fields & Descriptions

Percent 7 digits. Required.
Percent of the base.

Example: ABC Company sells Manufacturer Parts.
When viewing the Price Book for Manufacturer,
two prices are displayed. They are suggested list
and dealer net.

ABC Company is configuring the class for fast
moving parts. When adding parts to inventory, they
want to set up three prices, Dealer List, Suggested
List and Dealer Net. Dealer List is to be "based" on
Suggested List. ABC Company marks up the fast
moving parts 5%. When viewing suggested list on
the computer, they want to see suggested list as
displays in the price book. Dealer net is cost and
should be the same figure as is in the price book.


[=| X38-1 CONFIGURE VENDOR/CLASS

Base

Update

Minimum
Calls

1 digit. Required.
Which price is the price to be based. Choose 4=Dir
List, 3=Sugg List, 2=Internal, 1=Dlr Net.

The screen would look like this:

Price PercentBase

4-Dir. List 1050000 3
3-Sugg. List 1000000 3
2-Internal 1000000 2
1-Dlr. Net 1000000 1

1 character (Y/N). This field controls
automatic updating by Reprice Parts (X37-1)
and Price Tape Update (X37-2). Use "Y"
(Yes) if you want the price to be updated;
otherwise, "N."

Calls = 5 digits, Months = 3 digits.
Optional. Used with Order Code of A.
Determines demand criteria for the part.
Before a part can be considered for
Suggested Stock Order, it must meet the
demand criteria established for the class.
"Number" of calls for the part during the
number of months placed in the "#Months"
field. If the part reaches the demand criteria,
the rest of the formula associated with Order
Code A will be used to determine how many
of the part should be ordered. You can
establish two different demand criteria.


X38-1 CONFIGURE VENDOR/CLASS [=]

And/Or for I character. Required.

Minimum If 2 demand criteria are established, whether both
must be met to order or one. Use A (And) if both
criteria must be met. Use O (Or) if one or the other
criteria must be met for stock order.

Example: ABC Company is configuring the fast
moving parts class. They are using an Order Code
of A. They have a busy season and a slow season.
During the busy season, three months, they figure
the part must be purchased 9 times to qualify for
reorder. During the slow season, three calls for the
part in 9 months is enough to qualify the part for
reorder. As long as either criteria is reached, they
want the part to be ordered. The screen is filled in
like this:
-- Minimum --

Number #Months

Calls 00009 003

Calls 00003 009
And/or for minimum 0

Last Receipt 1 character. Required.
Y (Yes) or N (No). Choose Y (Yes) and the record
of the last order number and receipt date will be
recorded at PARTS INQUIRY (X3-1) on a part by
part basis. Use N (No) and no record is maintained.

Below is the completed screen of the fast moving class for Manufacturer
parts:


sa | X38-1 CONFIGURE VENDOR/CLASS

ABC COMPANY Parts Configuration %3810-103
Vendor/Class Configuration
Vendor MAN - CURRENT
Vendor Information anes.
System address# Automatic ordering option D
Part Number Special Process code
Segment sizes 04 04 07 06 Price Book assignment MANBOOK
Sort justification L R R & ----Division Information:
Segment sort order 2 1 4 3 Dealer Number POd35
Sort method R Vendor's ID
Default class A
Enter ¥ to delete
Class Information
Name FAST MOVING Order code A
Automatic pricing ¥ #Days supply 054 --- BOQ ----
Price Percent Base Update -- Minimum -~ = Factor 1
4-Dir. List 1050000 3 ¥ Number #Months Acg cost 050
3-suga. List 1000000 30 ¥ calls c0g09 003 Inv ovhd 040
2-Internal 1000000 20 ¥ Calls 00003 009
1-Dlr. Net 1000000 2 ¥

And/Or for minimum 0 Last Receipt ¥

Cmdl-End job  Cmd2-Vendor List Cmd4-Restart

 

O When the fields are complete, press [Enter] to add or update the class.

Command Key Options

Cind1-End job End the job.

Cmd2-Vendor List Displays the current vendor codes already
set up.

Cmd4-Restart Allows you to restart at the vendor code

screen without exiting the job. If you press
Cmd4- Restart without pressing Enter, the
information typed on the screen will be
ignored. Changes will not be made and new
vendors will not be added.


X38-1 CONFIGURE VENDOR/CLASS [=]

### Deleting A Class Or Vendor

Before deleting a class, make sure there are not parts in the class. Run a
Parts Inventory Pad (X36-1) requesting the vendor and class to be deleted.
Move any parts in the class to another class using Reconfigure Parts
(X38-3).

All classes must be deleted before you can delete a vendor.

If the goal is to delete all classes and then the vendor, you would:
Make sure there are no parts in any classes.

Delete the regular classes.

O Delete the default class.

Oi Delete the vendor code.

 

 

 

 

 

 

Deleting the regular classes. All classes can easily be deleted. There is an
extra step that must be performed before deleting the Default class. See
Delete the default class.

On the class screen you will see a field "Enter Y to Delete". Place a Y in
the field and press Enter. The class is deleted.

Deleting the default class. Deleting the "Default" class requires an extra

step. On the Vendor/Class Configuration Screen, field exit through the
class entered in the "Default class" field:


ss | X38-1 CONFIGURE VENDOR/CLASS

ABC COMPANY Parts Configuration *3820-101
Vendor/Class Configuration

Vendor Information
system address Automatic ordering option >
Part Number - “+ Special Process code
Segment sizes 04 04 07 06 Price Bock assignment MANBOOX
Sort justification L RR L ----Division Information
Segment sort order 2 1 4 3 Dealer Number PO43S
Sort method a Vendor's ID

Default class

Cmdi-End job Cmd2-Vendor List Cmd3-Special process Codes
cnd5-Price Book list

omd4-Restart

O Press Enter. In the Class field, type the class code that use to be the
Default class. Press Enter. You will see "Enter Y to Delete". Type Yin
the field and press Enter. The class is deleted.

Deleting the Vendor Code. From the class screen, press Cmd4- Restart.
Type the vendor code for the vendor to be deleted. If all classes have been
deleted, the following screen is displayed:
Lo


X38-1 CONFIGURE VENDOR/CLASS

ABC COMPANY Paxts Configuration 3810-101
Vendor/Class Configuration

vendor MAN - CURRENT Enter ¥ to delete

Vendor Information =
System address# Automatic erdering optien D
Special Process code

Segment sizes 04 04 07 06 Price Book assignment MANBOOK

Sort justification L RR OL ----Division Information

Segment sort order 2 1 4 3 Dealer Number P0435

Sort method A Vendor's ID

Default class

Cmdi-End job Cmd2-Vendor List  Cmd3-Special Process Codes Cmdd-Restart
(ma5-Price Book list

 

O Type Y in the "Enter Y to delete" field. Press Enter. The vendor is
deleted. If all classes have not been deleted, the field "Enter Y to
delete" will not display. Print a Configuration Report (X38-2). The
classes will display on the report. Delete the remaining classes. You
can then delete the vendor code.


Notes:

## CHAPTER X38-2

CONFIGURATION REPORT

### Introduction

Vendor and classes are defined in X38-1 Configure Vendor/Class. This
report is a list of the configuration of vendors and classes.

### How To Run

From Menu X38, select option 2. The Configuration Report will be sent
to the Job Queue.

The report is divided into two sections, Configured Vendors Report and
Configured Classes Report.

A sample report is on the next page. For fields and the definitions, see
X38-1 CONFIGURE VENDOR/CLASS.

ABC COMPANY - BELLINGHAM Configuration Report- Cenfigured vendors 5/09/88 Page 1
BELLINGHAM, WA A 3820-18,

systen DElt Segnent Size Justified Sort Order Sere Auro Ord Vendors Special Price
Code vendor Nane 1203 4 12 3 4 method method 1D Proc ¢D Book

ALLIS CHALMERS ALLIO 1234567890

ALLIS CHALMERS

Beat 0060600082

canco

case:

FARMHAND

## X38-2 CONFIGURATION REPORT

ABC COMPANY - BELLINGHAK
BELLINGHAM, WA a

Ord upd Dealer
cD Class Nane cD CD List tof

Vendor: AC - ALLIS CHALMERSKE
A DEFAULT 100.0000/3
© ossoLens 100. c000/3
§ sTockine 1100..0000/3

Vendor: ALC ~ ALLIS CHALMERS

A DEFAULT 119.0000/3
S STOCKING 319.0000/3

vendor: CAM ~ CALICO

A GENERAL 400-0000/1
2% TEST CRDER CODE 400.0000/4

Vendor: CAS ~ CASE
A DEFAULT 110.9000/3
© opsoLErs 110.0000/2
S$ STOCKING 120.0000/3

vendor: PAR

A DEFNGLT 120.0900/3
5 STOCKING 120.0900/3

Vendor: wax

A DEFAULT 210. c000/3
S STOCKING 4119, 0000/3

Vendor: mrs
A DEFAULT 110.0000/3
8 STOCKING 110.0000/3

Configuration Report - Configured Classes Date 5/09/88

Suggested
List 8/of

100.0000/3
100.0000/3
100.0000/3,

190.0000/3
190.0000/3

300.0000/2
300.9009/1.

400.0000/3
106.0000/3
100.0000/3

209.0000/3
200.0000/3

390.0000/3,
100.0000/3

190.9000/2
190.9000/3,

Internal,
ot

100.0000/%
100. 0000/2
100.2005/1,

100..6000/1
100. 0000/2

200.0000/1
200..0000/1

100.0000/1
100.0000/1
100,0000/1

100.0000/1
200.0000/1

100. 0000/2.
100. 0009/3.

100.0000/1
100.00090/1

Time 8.37.48
Dealer ays Min Nunber Min Number E09 Acq
Nee 8/0£ Supp Cails/Mes A/0 Calls/Mos Fac Cost.

100.000072
100.0000/1
100.9000/2

100.0000/2
100, 0000/2

100.0900/2
109.0000/1

100.0000/2
200.0000/3
00 .0000/%

100.0000/1
100.0000/1

100.0090/2
100.0000/1

100.0000/1
100.0000/1

Page 2
43820-28,

Iyntry bast
ovheag Rept

 

## CHAPTER X38-3

RECONFIGURE PARTS

### Introduction

Reconfigure Parts allows you to:
= reconfigure an entire class/vendor or all parts.

= change the order code, class code, minimums & maximums, or other
specific fields.

™ move parts from one class to another based on demand (user-defined
performance criteria) or by value

### Entrance Screen

From the Parts Configuration Menu (X3-8), select option 3, Reconfigure
Parts. The Entrance screen appears, as illustrated below.

NW EQUIPMENT SALES 3830-101
Division A

Vendor or “ALL*
Class or "ALL"

Options values

Delete class
Change class code ? New class code _

Change order code ? New order code _ (Ac or Mm

Calculate min ? Days Supply (0-365)
Calculate max ? Days Supply (0-365)
Force min ? Quantity
Force max ? Quantity

Change bases ? 4- Dir List _3- Sug List _ (1,2,3,4)
2- Internal _ 1- Dir Net

Cmdl-Cancel © Cmd2-Move parts based on demand ¢mé5-Reconfigure Parts by Value

## X38-3 RECONFIGURE PARTS

 

### Fields & Descriptions

Vendor 3 characters. Vendor code or ALL for all
vendors.

Class 1 character. Class code or ALL for all
classes.

(Y/N) 1 character. Type Y in any of the options

you want to change.

### Options

Q Press Cmd1 to cancel the job.

O Press Cmd2 to move parts based on demand.

O Press Cmd5 to move parts based on value.

1 Change the options and values as described below.

IF CHANGING: ENTER:
Delete class If deleting, enter Y for YES.
Change class code Y, and the new class ID.

Class codes cannot be changed if there are
any parts from the original class on current

orders.

Change order code Y, and A (automatic), M (manual), C
(combined).

Calculate min YY, and minimum stocking quantity.

Calculate max Y, and maximum stocking quantity.

Force min Y, and minimum stocking quantity to force
to be a specific number.

Force max Y, and maximum stocking quantity to force

to be a specific number.


Change bases Y, and 4,3,2,1 for the new base price.

0 When you finish entering the changes you want to make, press [Enter].
A verification message or screen (for "Delete class=Y) is displayed.

Verification Screen

Division: E VERIFICATION SCREEN

Vendor or "ALL" ALL
Class or "ALL" ALL

Options Values
can)

Delete class 7

Enter "YES" to confirm delete option

Ceution: this job immediately changes all parts in the selected vendor/class,
make sure you have made a backup of your files.

Gmdl-cancel job; Cma3-Previous Screen; Enter to begin job

 

### Options

O Verify the options and values you changed. Press ENTER to accept and
retum to a menu.

O Press Cmd1 to cancel the job and return to a menu.

O Press Cmd3 to return to the Reconfigure Parts screen.


Note:

}| If this job is terminated abnormally while in progress (for example, in

|| the event of a power failure), it can be run again and the Summary will }
| accurately show that only those lines that were not changed during the
first job are changed in the second job.

### Fields & Descriptions

Function Description of option selected.
Change Class Changing class information.
New Class New class ID.
Class codes cannot be changed if there are
any parts from the original class on current
orders.
Total Dir. List Total dealer list dollars.
Dir Net Total dealer net dollars.
Vendor Vendor name.
Class Class code.
Number of Lines Number of lines changed.
Change order code Changing order code.
New order code New order code ID.
Calculate min Calculating minimum order quantity.
Days Supply Minimum number of days of stocking
quantity.
Force max Maximum number of stocking quantity
Quantity days to force.
Change Bases New base prices.


Reconfigure Parts Summary Report

NW EQUIPMENT SALES
Division : A
vendor: CAS Class: $

Date 11/05/95 Page 1
‘Time 15.49.03 x3630-5a

Function Vender Class Number of Lines

Change class New class: N Total Dir. List: 1588.26 Dlx Ret: cas s


 

An Exception Report will follow the Summary if exceptions were found.
For example, if "ALL" is entered in the Vendor field, an exception is
noted if a vendor is not configured for the new class or if no parts are
found in the selected class.


 

### Move Parts Based On Demand

O Press [(Cmd2] to move parts based on demand. Parts on current orders
cannot be moved to a new class.

BELLINGHAM CAR & TRUCK CO. RECONFIGURE PARTS x3830-301 1
Division: A MOVE PARTS BASED ON DEMAND

Vendor or "ALL" ALL
Class or "ALL" ALL

Move to class (valid class code)

if denand hes been (GE.L) (
this number of calls (0-999)

in this mumber of months (1-23),

and paxt has been in

inventory at least this
number of months

cmdi-cancel job  Cmd3-Previous Screen

 

### Fields & Descriptions

Vendor or ALL Specific vendor code for the move parts

CO


 

or ALL vendors to be considered.

Class or ALL Specific class or ALL classes.

Move to class Valid class code.

If demand has been GE (greater than or equal to) or LT (less
than).

this number of calls Number of requests for the parts (0-999).

in this number of months = From 1 month to 23 months.

and part has been in Minimum number of months that part has

been in inventory at least this inventory
(1-999). number of months.

OPTIONS:

O Press Cmd1 to cancel the job.

0 Press Cmd3 to go back to the parameter screen.

O Press ENTER to accept the move parts based on demand values.

The Move Based On Demand Summary report will be placed on the job
queue and the Reconfigure Parts screen will return.


NW EQUIPMENT SALES
Division : A

Vendor 4: CAS Class: ALL
Conpare : UT Calls: 100

Months on System: 3

Function

Change class

New class: v Total Dir.

Move Based on Demand Summary Report

Months: 23

5101.66
oral Dir. List: 195.40
Total Diz. List: 1876.46
‘Total Dir,

Toral Dir. List: 25.95

### Fields & Descriptions

Vendor

Class

Compare

Calls

Months

Function

Change Class
New Class

Total Dir. List

Dir Net

Vendor

Class

Number of Lines

Date 11/06/96
Time 15.53.42

Page 1
x3830-55

jendor = Class. Munber of Lines

2900.12
601.50
858.24

14.10

Vendor name or ALL.
Class code ID or ALL.

2s.
a
39
23
2

 

Greater than or equal to, or less than.

Number of calls.
Number of months.

Description of option selected.

Changing the class.

New class code.

Total dealer list dollars.
Total dealer net dollars.
Vendor name.

Class code ID.

Number of lines changed.

The Move Based On Demand Exception Report will follow the Summary


 

if exceptions were found. For example, if "ALL" was entered in the
Vendor field, an exception is noted if:

= the move to class is invalid,

"no parts are found in the selected class

= some parts were on current orders.

The Parts Management Report (X36-2) will reflect changes made by this
job for parts that were deleted or that had Vendor or Class codes changed.
These changes will show as "Part Adjustments".


 

### Move Parts Based On Value

O To move parts to a different class based on any one of the base price
fields (Dealer Net, Internal, Suggested List, or Dealer List), press
[Cmd5] from the entrance screen. The Based on Value screen appears.

Based on Value Screen

NW EQUIPMENT SALES Reconfigure Parts X3830-701 2
Based on Value

Base Price Fields

1s Dealer Net

2= Internal

3= Suggested List.

4= Dealer List Enter Base Price Field : _

vendor: From Class (or ALL):

Cmdl-End job Cmd3-Previous Screen Cmdd-Save Options cma5-Reset

 

O Select one of the base price ranges, which are listed in the upper left
corner of the screen.

Q Select the vendor (or ALL) and class (or ALL) for the changes.

0D In the column labeled "From or Equal,” type the beginning amount or

CL


the exact value of the parts you want to move. Use whole dollar
amounts only. For example, type $3.00 as 3 and press [Field Exit].

0 In the coiumn labeled “Less Than," type the end of the range and press
[Field Exit]. Use whole dollar amounts only.

O In the column labeled "To Class," type the new class.

### Options

O Press Cmd1 to end the job.

O Press Cmd3 to return to the entrance screen.

O Press Cmdé to save the options, start the move, and return to the menu.
The selections you have typed on this screen are saved and used as the
defaults the next time you decide to move parts based on value. After
defaults have been saved, you can change them for one session only by
typing over them or for future sessions by pressing Cmd4 to save the
new ones.

0 Press Cmd5 to reset if you have typed over the defaults saved by
Cmd4-Save Options and want to retum to the selections you saved
earlier.

O Press [Enter] to start the move without saving the current options
(selections).

A Reconfigure Parts by Value report, which lists the parts that were
moved, is printed.


X38-3 RECONFIGURE PARTS C ~

 

Reconfigure Parts by Value Report

Reconfigure Parts by value 12/06/96
AS CASE/IH Pose 3

Ranges ©
Ranges - 2. 0
Ranges -3. 00 0
Ranges °
Base Price code -
Partt Description Price Old Class New Class
24a:

246695
0246695
255562
25615,
aged
20
M806
Poe
Post
Pas
ns2
0677
ona
vaan

38a,
asasozRi.
eseo3iR2
484033R1
44035R
98445SR1,
a4879R1
494881R1
495259R91
435834R1
495672R91,
435673R1

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
v
v
v
¥
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

 

Note that the price of each part is reported in whole dollars only. The
selection criteria are printed at the top of the report.

## CHAPTER X38-4

PARTS LOCATOR CONFIGURATION

### Introduction

The purpose of this job is to match your vendor codes with the numerical
codes used by the Parts Locator. It is not necessary to repeat configuration
unless you want to change the vendors you send.

Only the vendors that are assigned numerical codes in this job will be used
to create the Parts Locator file: NO CODE, NO GO. Since there is no
further selection of vendors when the file is created, all vendors assigned
here will be included.

Vendors configured in all divisions are listed in Parts Locator
Configuration, and they appear in order by division. Although you'll use
the same numerical codes for the vendors in each division, it is necessary
to enter the codes for each occurrence.

Technical Note: Parts Locator Configuration is saved in u.IVT.

## X38-4 PARTS LOCATOR CONFIGURATION

NUMERICAL CODES FOR PARTS LOCATOR

WWOIDUARWNHH

Agco

Alamo

Alfa Laval

Allied Steel
Armstrong Tools
Badger Northland
Bayliner

Blaw Knox
Bomag
Bombardier
Briggs & Stratton
Bush Hog
Caterpillar
Champion
Chrysler

Claas of America
Clark VME,

Club Car

Crown Lift

Cub Cadet
Cummins Engine
Cushman

C, Itoh

Dresser

Dynapac

Eagle Engineering
Farmhand

Fiat Allis/Tractor
Force

Ford New Holland

SL
52
53
54
55
56
37
58
359
60

Garden Way

Gehl

GM

Gorman-Rupp
Gradall

Gravely

Hitachi

Homelite

Honda

Howard Price Turf Equip
Hyster

Ingersoll Rand
Ingersoll Equipment
JICase
Jacobsen/Textron
ICB

John Deere

J. A. Freeman
Kawasaki

Kobelco

Koehring

Kohler

Komatsu

Kubota

Kuhn Farm Machinery
Kysor Westran
Liebherr America
Mack Truck

Massey Ferguson
Melroe


 

61 Mercury Marine 92 Yamaha
62 Minn Par 93 Other
63 Navistar

64 Nissan Forklift
65 OMC/Evinrude

66 Polaris

67 Ransomes/Bobcat
68 Raymond

69 Red Dot

70 Rexworks

71 Rhino

72 Simplicity
73 Stanley Hydraulic

74 Suzuki

15 Tecumseh
76 Temco

77 Terex

78 Thermo King

719 Timberjack

80 Tisco

81 Toro

82 Toyota Auto & Forklift
83 Trojan Industries

84 True Value

85 Vermeer

86 Vicon

87 Volvo Marine

88 Volvo GM Heavy Truck

89 Wagner
90  White-New Idea
91 Woods


X38-4 PARTS LOCATOR CONFIGURATION _

 

### How To Run

From the Parts Configuration Menu (X3-8), select option 4: Parts Locator
Configuration. The assignment screen is illustrated below.

ABC COMPANY PARTS LOCATOR CONFIGURATION %3840-101

Division Vendor Name Locator Code Manufacturer
A CASE Unassigned
VERSATILE Unassigned
FORD TRACTOR Unassigned
ALLEN Unassigned
NEW HOLLAND Unassigned
BRABER EQUIPMENT Unassigned
CASE Unassigned
‘TISco Unassigned (
CUSHMAN Unassigned
DANDL Unassigned
DAVE'S DEALS Uaassigned
BOMFORD Unassigned
HOWARD Unassigned
STARLINE Unassigned
‘TAARUP Unassigned
HARSH Unassigned
PITTSBURG Unassigned
SERVIS Unassigned
oso M&W TURBO & DUAL Unassigned

(mdl-End job Roll-Page

 

CO In the column labeled "Locator Code," type the appropriate code from
the list on the previous page. Press [Field Exit].

O After making the assignments, press [Enter]. A screen with assignments
is illustrated on the next page.

 

CU


 

Note:

You must press [Enter] on each screen to register your entries before
rolling to the next screen; otherwise, the assignments are lost.

 

 

O Roll to the next screen of vendors.
O Repeat as necessary.
O Press [Cmd1] to end the job.

Remember, all assigned vendors will be included in the Parts Locator file.


 

ABC COMPANY:

Division Vendor Name


ec
HAR
BHH
TIE
Rang


LOCATOR CONFIGURATION

CASE
VERSATILE

FORD TRACTOR
ALLEN

‘NEW HOLLAND.
BRABER EQUIPMENT
CASE

TISco

CUSHMAN

DANDL

DAVE'S DEALS
‘BOMFORD

HOWARD

STARLINE

TAARUP

HARSH

PITTSBURG

SERVIS

MGW TURBO & DUAL

Qmdl-End jch Roll-Page

Locator Code

Manuzacturer
oT Case
<---+ Unassigned
Ford New Holland
<---- Unassigned
Ford New Holland
<---- Unassigned
oT Case
Tisco
Cushman
Unassigned
Unassigned
- Unassigned
Howard Price Turf Equip
<---> Unassigned
<---- Unassigned
< Unassigned
<---~ Unassigned
<---- Unassigned
<---+ Unassigned

 
x3840-101 1

 

to

## CHAPTER X38-5

CREATE/SAVE PARTS LOCATOR FILE

### Introduction

This job creates a file of parts from the vendors assigned to numerical
codes in Parts Locator Configuration (X38-4). No selection of vendors is
possible in this job. All vendors with numerical codes and only vendors
with numerical codes are included in the file: NO CODE, NO GO.

If a disk drive is present in the system, the file is saved to a diskette.
Otherwise, it is saved to a tape. After had has been saved, it is then
shipped to Parts Voice where it will be included in a computer data base.
Only parts with a positive available quantity are included in the file.

This job can be run at Parts End of Month from the menu option, X3-10,
or during Combined End of Month Procedures (X10-2) by setting the Parts
Locator OPT in Parts on OPT DIS Master Menu (X63-3).

You'll need to have an initialized tape ready before you begin this job.
This job is not particular about the tape label as long as there are no active
files on the tape. You can use tapes prepared by Prepare Tape for
Immediate Backup (X61-6).

Technical Note: Configuration is saved in u.IVT. The Parts Locator file is
WAL, which is deleted automatically after it is saved to diskette, In the
file, the part number is followed by 8 digits, such as 00504401, where 005
= available quantity; 044 = numerical vendor code; 01 = store number.


X38-5 CREATE/SAVE PARTS LOCATOR FILE oo

 

### How To Run

From the Parts Configuration Menu (X3-8), select option 5: Save/Create
Parts Locator File. The file is created, and system messages will prompt
you to insert an initialized tape cartridge.

Lo.

## CHAPTER X38-8

MANUFACTURE PARTS LOCATOR DOWNLOAD

### Introduction

Use this option to prepare a parts locator file, which will be transferred by DIS
Electronic Commerce to the PC where the manufacturer’ s communications
software is installed. Only parts with a positive available quantity are included in
the file.

The following communications packages support DIS Electronic Commerce
transfers of parts locator (inventory) files:

- AGCO Solutions™ On-Line

" New Holland DCS

To learn more about DIS Electronic Manager and Client, see Chapters X6-15 and
X6.15-1, which include configuration and troubleshooting instructions.

### Contents

2 X38-8 « MANUFACTURE PARTS LOCATOR DOWNLOAD RELEASE 2.2

 

### Submit Part Locator Screen

O From the Parts Configuration Menu, select option 8, Manufacture Parts
Locator Download. The Submit Part Locator screen is displayed.

Submit Part Locator Screen

 

AGR EQUIPMENT SALES Submit Part Locator X38801
Division A

Ven
1sSelect
Opt Ven Name Com Description

FAR FARMHAND AGC AGCO SOLUTIONS ON-LINE

MAS MASSEY FERGUSON AGC AGCO SOLUTIONS ON-LINE
i NHD New Holland DCS NHD New Holland pcs
WHT WHITE FARM EQUIP AGC AGCO SOLUTIONS ON-LINE

Bottom
F3sExit F5=Refresh Roll

 

 

The Submit Part Locator screen displays the vendors that were configured in
Configure DIS Electronic Commerce Manager (X6.15-1).

C Select one or more vendors with 1=Select and press [Enter]. The job is
submitted. You will receive a message confirming successful completion.


PARTS INVENTORY X38-8 ¢ MANUFACTURE PARTS LOCATOR DOWNLOAD 3

PARTS LOCATOR FILES FOR AGCO SOLUTIONS ON-LINE

The vendors associated with AGCO are:

AGCO Allis Hesston
AGCOSTAR Landini

Black Machine Massey Ferguson
Farmhand Tye

Gleaner White

Glencoe White-New Idea

O Select one or more of the AGCO vendors with 1=Select and press [Enter]. The
job is submitted. The system looks at all vendors attached to the AGCO
Solutions On-Line communications package and merges the part information
together for 1 transmission to AGCO. When this process is done, the
following message will be sent to your workstation: “DIV- A aAGCO
Vendor WHT Return R0010721 Successfully Sent”


4 X38-8 e MANUFACTURE PARTS LOCATOR DOWNLOAD RELEASE 2.2
OC ermh.U_I_ I CRELEASE 2.2

Notes:

## CHAPTER X52-1

CUSTOMER INDEX SETUP

### Introduction

Point of Sale cannot be running when this option is selected.

Customer Index Setup should be run from time-to-time to rebuild the
Receivables, Vendors, and Marketing indexes., even though new names
are included in indexes immediately.

Customer Index Setup rebuilds the following indexes:
® Receivables

= Point of Sale

= Vendor

® Marketing

The Customer Index Setup applies to the AS/400 when the AS/400 users
schedule automatic IPLs.

### How To Run

Before running Customer Index Setup, make sure there are no Accounting,
Marketing, or Point of Sale jobs running. From the Point of Sale Table
Maintenance Menu (X52), select option 1, Customer Index Setup. The
following warning message will be displayed:


[| X52-1 CUSTOMER INDEX SETUP c

8/36 PROGRAM MESSAGES

x52100

This procedure will rebuild the customer index files.

It is critical that point of sale is not running
on the system while the indexes are rebuiit.

Have you checked that this is the case? (Y/N)

ster missing soranezer {

 

O Type in Y if you have checked to make sure that Point of Sale is not
running.
C Press [Enter].

‘When the menu returns, the job is complete.

If Customer Index Setup is run while Point of Sale is active, a temporary
file, u.@SNT, is created and remains on the disk. You'll see it among the
temporary files on a catalog; however, it is not necessary to contact the
Response Line. Simply delete the file and re-run Customer Index Setup
after Point of Sale is terminated.

Ata menu, type: DELETE u.@SNT,F1 [Enter].
(a = the I-character ID associated with your data files)

RELEASE 2.2 Co

## CHAPTER X52-2

DOCUMENT CLASSIFICATION MAINTENANCE

### Introduction

This job allows you to establish the types of documents that will be used
in Point of Sale Invoicing. All sales at Point of Sale can be handled on two
basic documents, counter tickets and repair orders. You'll need to set upa
code for each type of document and establish the first number that will be
used.

Document Classification Maintenance is divisional. Set up document
codes for each division that will be performing Point of Sale (X5-1).
Although the number of document types is limited only by available
characters, it is best to keep the choice as simple as possible.

At Point of Sale or Rental Invoicing, you furnish the document type. The
system assigns the number that corresponds to the numbering system set
up in this job, and increments the number automatically so that the next
number will be in sequence.

You can file copies of the documents numerically for easy access in the
event of audit.

To get a copy of current document classification codes:

From the Table Maintenance Menu (X52-2), select option 2, Document
Classification Maintenance. After passing through the security gate,
press [Cmd1]. A listing of the current document classification codes
will print.


[| X52-2 DOCUMENT CLASSIFICATION MAINTENANCE

### How To Run

From the Point of Sale Table Maintenance Menu, select option 2,
Document Classification Maintenance.

The following screen appears:

ABC COMPANY DOCUMENT CLASSIFICATION 5220-101
Maintenance

Enter classification code

 

Enter either a letter or a number as the document code for the document (
type you want to set up.

Enter the document code you have chosen.

ABC COMPANY DOCUMENT CLASSIFICATION X5220-101,
Maintenance

Enter classification code C

 

When the code is typed, press Enter. If the words “Current Code" appear
in the lower right hand corner of the screen, the code already exists;
otherwise you see "NEW Classification code." The following screen
appears:

RELEASE 2.2 CU

## X52-2 DOCUMENT CLASSIFICATION MAINTENANCE

A&R EQUIPMENT SALES DOCUMENT CLASSIFICATION 5220-101
Maintenance
Enter classification code &

Description Printer ID P4

Document type W Valid document types:
"Q' + quote ‘P' - purchase order
sales order ‘M’ - sales credit memo
work order ‘D' - work credit memo

Posting option M valid options:
‘A‘ ~ automatic posting
manual posting
‘= quote

Pricing detail Y valid options:

- pricing on each line
‘N' - pricing on final total only

Sequence # RO 00118
CURRENT Classification code:
Enter ¥ to DELETE

There is a prompt for a printer ID at the top of the screen. The Printer ID
must be set up in X52-10 first. If the Printer ID is left blank, no change
will be made and documents will be printed at the printer associated with
the workstation (unless the printer is changed while entering Point of Sale
Invoicing). Only printer IDs that have already been set up in Point of Sale
Devices are accepted on this screen. If a valid Printer ID is entered,
documents will be printed at the printer associated with the document
code. This applies to documents printed from the following options:

™ Point of Sale Invoicing

@ Periodic Invoicing

™ Service Management Sysiem


® Part Pick Lists (from P.O.S. Additional Options Menu)
™ Work Order Lists (from P.O.S. Additional Options Menu)

NOTE
The printer associated with the document classification code takes
precedence over the printer assigned to the workstation or selected when
entering Point of Sale.

An example of completed screen for the document type Repair Order
follows:

ABR EQUIPMENT SALES DOCUMENT CLASSIFICATION %5220-101
Maintenance
Enter classification code R

Description REPAIR ORDER Printer ID Pa

Document type W Valid document types:
"Qt - quote ‘p+ - purchase order
‘s' - sales order ‘M' = sales credit memo
‘wt - work order "D! - work credit memo

Posting option M Valid options:
‘AY > automatic posting
‘M' - manual posting
"= quote:

Pricing detail Y Valid options:
ty ~ pricing on each line

‘N’ + pricdag on final total only

Sequence # RO 00115
CURRENT Classification cede:
Enter ¥ to DELETE

 

RELEASE 2.2 to


X52-2 DOCUMENT CLASSIFICATION MAINTENANCE [=]

In defining the fields, C = character {letter or number). D = digit (number).
All decimals are assumed. Do not type the decimal point. Example: 5.2 D
five places in the field with two assumed decimal places.

### Fields & Descriptions

Description 15C
Description of the document.
Document type 1c

Defines the document type.

S$ = Sales order: Used for any document that
is not a repair order (work order). On the
sales order, the equipment description fields
such as make, model and serial number are
not accessible.

W = Work order: Repair order. On a work
order the equipment description fields such
as make, model, and serial number are
accessible.

Q= Quote: Quote can be used for quotes,
however, if the customer decides to accept
the bid, you must void the quote and place
the same information on either a sales order
or work order. You may want to present
quotes on sales or work orders. If the
customer does not accept the bid, the sales
order or work order can be voided.


[ «| X52-2 DOCUMENT CLASSIFICATION MAINTENANCE

Pricing detail Y = Pricing on each line
N = Pricing on final total only
Posting option Ic

Use M for manual. The other options are not
available now. If setting up quotes leave the
field blank.

Sequence # 2C for prefix and 5D for numbers.
Numbering system assigned to the document
type.

When the screen is filled in, press Enter. Enter another code or press
[Cmd1] to end the job.

When [Cmd1] is pressed, a list of all valid document codes prints. Tape
the document codes to the terminals that will perform Point of Sale
Invoicing. If more lists are necessary, see the What Happens Next section
in X5-2 Table Maintenance Menu.

An example of a Document Classification Table follows.

DOCUMENT CLASSIFICATION TABLE 10/05/97 PAGE 3.

5220-24
besexiption Type Cption Sequence Pricing Detail

RECD ON ACCOUNT 5 ARoo100

COUNTER TICKET a cr0a08

SALES QUOTE oros198

REPAIR ORDER * RO0D10S

UIT SALE " ysoa199

 

RELEASE 2.2 A


X52-2 DOCUMENT CLASSIFICATION MAINTENANCE [7]

### How To Change A Code

From the Table Maintenance Menu, select option 2. Press Enter. Type in
the Document Classification Code to be changed. Press Enter. Make the
change on the screen. Press Enter.

Press [Cmd1] to end the job. A Document Classification Table will print.

### How To Delete A Code

From the Table Maintenance Menu, select option 2. Press Enter. Type in
the Document Classification Code to be deleted. Press Enter. Enter Y in
the field labeled "Enter Y to Delete." Press Enter. The code is deleted.

Press [Cmd1] to end the job. A Document Classification Table will print.


Notes:

## CHAPTER X52-3

SALES CODE MAINTENANCE

### Introduction

Sales Code Maintenance is used to set up the codes that determine
automatic accounting transactions from Point of Sale. Sales Code
Maintenance is a divisional job. Sales codes must be set up for each
division that will be running Point of Sale Invoicing (X5-1).

If you only want to print a list of current sales codes, follow these steps:
From the Table Maintenance Menu, select option 3, Sales Code
Maintenance. After passing through the security gate, press CMD1.
When you see the following prompt:

Print Sales Code Report (Y/N)....N
Type ¥, and press [Enter]. The current Sales Code Table is printed.

For your convenience, sales code formats are illustrated at the end of this

chapter as they appear on the Point of Sale detail line (see SALES CODE

FORMATS AT POINT OF SALE); otherwise, the discussion is restricted

to basic "How to Run" information. For more information about sales
codes, see CHAPTER X5-2, TABLE MAINTENANCE MENU.

Note:

Journal IDs must be set up for zo sales codes or alll sales codes. For
more information, see Journal Menu chapters (X1-11, X1.11-1, 2, 3,
and 4).

## X52-3 SALES CODE MAINTENANCE

### How To Run

 

 

 

From the Point of Sale Table Maintenance menu, select option 3, Sales
Code Maintenance.

 

O At the sales code prompt, type a 2-character code and press [Enter].
The following screen is displayed:

A & R SALES SALES CODE MAINTENANCE 5230-101 1
Sales Code TC
Description New Sales Code

Format ‘L! - Labor 2 (
= Misc. Description ‘c’ - Prepayments
‘M! + Misc. Quantity ‘At - Received on Account:
‘Ul + Misc. Units ‘W' - Unit Sales
'N' + Notes ‘S* - Misc. Cost
“T' ~ Cost Misc Quantity

 

Debit Credit Discount ‘wild card’ account #'s:
Customer Document. ‘AUTO = - any format
Internal Decument “SALE =~ 'P! or ‘WH!
Warranty Document J format only
Journal 1d *ERROR - any format
Override Tax Code
Override Discount Code
Vendor for Parts —— (optional)
GST Rate
GST Account

Gmdi-End job Cmd3-Go back Cmd19-Delete this sales code

 

RELEASE 2.2 LO


X52-3 SALES CODE MAINTENANCE [2]

### Fields & Descriptions

Description 15-characters. Recommended. This
description is displayed at Point of Sale and
printed on the invoice or work order.

Format 1-character. The various formats are
illustrated later in this chapter. See the
section, "SALES CODE FORMATS AT
POINT OF SALE.”

| The following fields pertain to general ledger accounts. Leave all

account fields blank for sales code format “N" (Note). In addition,
jeave the warranty accounts blank for the following sales code formats:
| A, C, U, and W.

 

Customer Document

Debit 8-characters. Required (except Notes
format). General ledger account that is
debited when the document is opened to a
customer. Except for format "AA"
(Received on Account), *AUTO is
suggested.

Credit 8-characters. Required (except Notes
format). General ledger account that is
credited when the document is opened to a
customer. This is usually a sales account.


[+] X52-3 SALES CODE MAINTENANCE

Discount

Internal Document
Debit

Discount

Warranty Document
Debit

Credit

8-characters. Required (except Notes
format). General ledger account that is
debited for discounts when the document is
opened to a customer. This may be a sales
account or a special account for discounts.

8-characters. Required (except Notes
format). General ledger account that is
debited when a document is opened to a
unit, and for other lines marked "I." Credit
8-characters. Required (except Notes
format). General ledger account that is
credited when the document is opened to a
unit, and for other lines marked "I."
8-characters. Required (except Notes
format). General ledger account that is {
debited for discounts when the document is
opened to a unit. Since discounts are not
usually allowed on internal documents, use
the *ERROR wild card.

8-characters. Required for the following
sales code formats: D, L, M, P, and S. Leave
blank for sales code formats: A, C, N, U,
and W. General ledger account that is
debited for lines marked "W." (Document
may be opened to a customer or to a unit.)
8-characters. Required for the following
sales code formats: D, L, M, P, and S. Leave
blank for sales code formats: A, C, N, U,
and W, General ledger account that is
credited for lines marked "W." (Document

Revease22  \_


Discount

Journal id

Override Tax Code

X52-3 SALES CODE MAINTENANCE [=]

may be opened to a customer or to a unit.)
8-characters. Required for the following
sales code formats: D, L, M, P, and S. Leave
blank for sales code formats: A, C, N, U,
and W. General ledger account that is
debited when a discount is given on a line
marked "W." This may be a sales account, a
special account for discounts, or the
*ERROR wild card.

1-character. Optional; however, if a Journal
ID is entered for 1 sales code, an ID is
required for every sales code.

1-character. Optional. Tax code that is used
with this sales code regardless of the
customer's tax code.

Tax codes are entered on a line-by-line basis
at Point of Sale Invoicing, which means that
you can tax parts sales but not tax labor
sales. Point of Sale Invoicing uses tax codes
in the following order:

1) Standard Line
2) Sales Code
3) Customer

Subsequent lines use the tax code
established by a standard line or sales code.
Using a new standard line or sales code that
carries a non-blank tax code resets the
default; however, you'll need to [Field Exit]
through the default if you want to return to


L«] X2-3 SALES CODE MAINTENANCE

Override Discount Code
Vendor for Parts

GST Rate

GST Account

the customer's tax code.

1-character. Optional. Discount code that is
used with this sales code regardless of the
customer's discount code like override tax
code described above.

3-characters. Optional. Vendor code that is
used as the default with this sales code, if
applicable. The vendor code can be changed
at Point of Sale.

5 digits. Type 7% as 07000 and press [Field
Exit]. Canada only. The GST rate associated
with this sales code.

8-characters. Canada only. The general
ledger account where GST is accumulated
for this sales code.
io


SAMPLE SALES CODES

X52-3 SALES CODE MAINTENANCE | 7 |

A Miscellaneous Quantity sales code is illustrated below:

ABC COMPANY

Sales Code PM

Description MISC PARTS
Format u u
‘De
we
o
in

Debit
Customer Document.
Internal Document
Warranty Document
Journal id

Credit
*AUTO
13220
*ERROR

Override Tax Code
Override Discount Code
vendor for Parts

GST Rate

GST Account,

Qmdi-End job  Cmd3-Go hack

~ Labor

- Mise. Description
- Misc. Quantity

- Misc. Units

- Notes

Discount
43320 15500
13220 *ERROR
*ERROR © *ERROR

(optional)

xS230-101 2

current Sales Code

Parts
Prepayments
Received on Account
Unit Sales
Mise. Cost
Cost Misc Quantity

‘Wild Card’ account #'s:

‘AUTO - any format
*SALE 0 - ‘PS or 'W
format only

*ERROR - any format

Gmdi9-Delete this sales code

 

Fill in the information from the table you have created. Press [Enter]. Add

the next sales code.

At ABC Company, the discount given is debited back to the sale general
ledger. If you keep track of discounts given in a separate general ledger
account number, enter that number in the “Discount on Sales” field.


Ls | X52-3 SALES CODE MAINTENANCE

A Received on Account sales code is illustrated below:

ABC COMPANY SALES CODE MAINTENANCE 5230-201

Sales Code AA

Description RECD ON ACCT Current Sales Code

Format a ‘Lt - Labor ‘Br - Parts
"DY - Misc, Description ‘C' - Prepayments
'M* = Misc. Quantity - Received on Account
‘Ut + Misc. Units - Unit Sales
‘Wt - Notes Misc. Cost
Cost Misc Quantity

Credit Discount ‘Wild Card* account #'s:

Customer Document al1i0 ERROR ‘agro ~~ any format

Internal Docunent *ERROR ‘ERROR *SALE © = 'P! or ‘Wt

warranty Document format. only (
Journal Id YERROR - any format

override Tax cede

Override Discount

Vendor for Parts (optional)

GsT Rate

GST Account

Gmdi-End job cmd3-Go back Cmd19-Delete this sales code

 

Do not use the *AUTO wild card on AA sales code!

Use Cash on Hand as the debit account. Use the general ledger account
number for customer receivables on the credit side of the customer
document, not *AUTO. The address number for Cash, which is set up in
Receivables Maintenance (X11-2), is CASHd (_ =a space and d = your
division code), and it is attached to the G/L Cash on Hand account. If a
payment were accepted on a cash document, *AUTO would search on the

RELEASE 2.2 Lo


X52-3 SALES CODE MAINTENANCE [2]

’

 
 


 

address number used (_CASH4) and credit its general ledger account A
number, which is Cash on Hand. In this case, Cash on Hand would be

debited and credited for the same amount. Not only would the payment not

be credited to the customer who made the payment, it would not even be
traceable because there would be no net transaction.

 
 

Note:

 
  
   
 

If you will be accepting payments at Point of Sale on more than one
receivable account, set up a separate sales code for each account.

 

 

 

When all sales codes are entered, press [Cmd1]. Print a Sales Code Table
by changing the prompt "Print Sales Code Report (Y/N)" to Y.


X52-3 SALES CODE MAINTENANCE .

### Sample Sales Code Table

Current Sales Code Tables should be taped to all the terminals
convenience during Point of Sale Invoicing. NOTE: If you want to print
several copies, take the printer off-line while you request the report.
Change the number of copies before you place the printer on-line and the
report begins printing (at a menu, type: D P [Enter]). See the Quick
Reference Guide if you need more information.

To print a list of current sales codes:
O From the Table Maintenance Menu, select option 3, Sales Code
Maintenance. Add or change sales codes, if desired.

O Press [Cmd1] to end the job. The following prompt appears:

Print Sales Code Report (Y/N).... N
Type Y, and press [Enter]. The current Sales Code Table is printed.

 

 

 

 

a
RELEASE 2.2 Qe


Na 2QUIPMENT SALES SALES CODE TABLE Pate 5/23/96 Page 1
‘SELLINGHAN WA Tine 23-21.46 5230-203,

customer Warranty ~ +
Description Prt credit Discounc Discount credit Discount T D ven

RevD ON ACCOUNT:
cus? pezosrts
UNIT TRADE
EQUIPMENT SALE
RENTAL UXIT.
msc cost

cost Mrsc gry
MESC SALES

ERROR

PARTS CUSTORER
PES cusT sisc
PARTS INYEREAL
PARTS INT MISC
‘TIRES & TUBES
PARTS SHOP
PARTS SHOP MISC
PARTS WHOLESALE
PARTS WHOLE MIS
PAID OUTS
RENTAL UIT
SUBLET LAZOR
LABOR CUSTOMER
LBEOR CUST MISC
LABOR INTERNAL
LABOR INT MISC
FREIGHT

“ERROR
“agro
sauTo
TERROR
sERHOR
“ERROR

snuTo
“aur

FOURS eGUEU KD UENRUERHHMCECOKE

 

### Changing A Sales Code

Enter the sales code to be changed. Change any fields you want. Press
[Enter].


[=] X52-3 SALES CODE MAINTENANCE .

—,

### Deleting A Sales Code

Never delete a sales code if it appears on an open or
unposted document. To make sure the sales code are not on open

documents, run a Held Documents Report (X56-2). Review the
documents.

If the code is not on any open documents not posted, enter the code to be
deleted at the prompt. Press [Cmd19] to delete this sales code.

SALES CODE FORMATS AT POINT OF SALE {
A = Received on Account:

RCVD ON ACCOUNT

ine sc Description:

oo1e aR CHECK #2345
Standard line code

 

C = Prepayments:

CUSTOMER DEPOSITS
7D Copy Line sc Description:

oc10 cD
Standard line code

 

RELEASE 2.2 CC


D = Miscellaneous Description:

FREIGHT
TD I/W Copy Line sc

0010 ZF
Standard line code

 

L = Labor:

LABOR Job Date of
TD IW Line SC Employee Cede Work Report
0010 Tc sR o1¢ = 120686 400
Standard line code

 

M = Miscellaneous Quantity:

MISC PARTS SHOP
TD IW Line $C Qty Deseription--.

colo Pr 13/4" BOLT
Standard line code

 


14 Co

N = Notes:

Std. Line I/W Line sc

oo10 No :
Note 12345678901234567890123456789012345678901234567890123456789 012345678901234

 

P = Parts:

PARTS COUNTER
TDI Pty Line Sc ven Part number

0019 PC MAN F26451.
Standard line code No demand Warranty

 

S = Miscellaneous Cost:

### Miscellaneous

TD IW Line §¢ Description-

- = = ~— 0010 zs
Standard line code

 

{
RELEASE 2.2 NK


T= Miscellaneous Cost Quantity:

MISC CST QUANT
ToOIM Line sc

Qty Description:
ALL 0050 MQ
Standard line code

 

U = Miscellaneous Unit:

MISC, UNIT

To Iw Line SC Unitt Description:

9010 UN FT0002 RENTAL OUT
Standard line code

 

W = Units (Wholegoods):

EQUIPMENT SALE Warranty

code Date Price
i 120686 400000

TD Line sc Stock#

0010 ES UNTT26
Standard line code

 

If a unit is sold or returned with a "W" format, the system checks the sales
code. If it finds *SALE or an actual general ledger account number in the
customer credit account field, it checks the amount field. If the amount is
positive (the unit is being sold), the unit must not have been sold

previously. If the amount is negative (the unit is being retumed), the unit
must have been sold earlier.


Notes:


---