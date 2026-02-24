---
title: "PART: POINT OF SALE - PRIORITY ORDERS (X5)"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about PART: POINT OF SALE - PRIORITY ORDERS (X5)."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on PART: POINT OF SALE - PRIORITY ORDERS (X5)."
---

---

## Page 1

## CHAPTER X5-3

PRIORITY ORDERS

### Introduction

Use this option to:

= make changes to any part placed on priority order
= add parts to the priority order

= add parts to the order that are not in inventory

In Point of Sale Invoicing (X5-1), parts with no available quantity are
frequently encountered. These parts can be handled in different ways:
1) deleted from the document

2) recorded as lost sales

3) placed on priority order

4) placed on a stock order

5) robbed and not reordered (provided there is some on hand quantity)
6) robbed and reordered

Drop ship parts and actions 2-6 are aiso covered. See also Recovering a
Priority Order, which is at the end of this chapter.

The system will pick up and order parts, including, drop ship parts from
both open and closed documents. You can go back later and add freight
before you close the ticket.

An OPT X636E-3,4 allows you to decide whether you want to drop ship
parts from both open and closed documents to be included in the priority
order queue (default) or whether you prefer to have only those from closed
documents in the queue.

A separate priority order is created at Point of Sale Invoicing for each
vendor. The order is then accepted or finalized. A copy of the order prints
for submission to the manufacturer. This job allows you to process priority
orders from multiple vendors at the same time and will remember the
special instructions entered for each one.


[2] X5-3 PRIORITY ORDERS 0 .

### Overview

At Point of Sale, if a customer wants to purchase a part that is not in stock
or inventory, the part can be priority ordered. The part number entered is
checked for quantity available for sale. This does not mean the quantity on
hand. There may be 3 parts on hand, but if other documents at Point of
Sale have created reservations for two of the parts, only one is available
for sale. If an attempt is made to sell two of the parts at Point of Sale, 1
will be placed on the Priority Order Queue.

When a part number is added to a document a "P" is displayed in the Pty

field on the line. The “P" is a Priority order code. It means, order the part.

There are three reasons that a part is placed on the Priority Order Queue:

= The part is reserved on another Point of Sale document. (
= The part is not in stock and must be ordered.

= The inventory count is off.

The part is not placed on the Priority Order Queue until the document is
either closed or placed on hold.

When a part is priority ordered, the job of finalizing the priority orders is
done in this job, Priority Orders (X5-3). All parts that are priority order
queued by Point of Sale documents will display. They will remain on
priority order until the order is accepted.

For more details on priority orders, see Priority Orders in the Reference
Section of Chapter X5-1 Point of Sale Invoicing.

RELEASE 2.2 Ne


X5-3 PRIORITY ORDERS [=]

Definitions of Priority Order Codes

When the part is available, the priority code is blank. The "P" means
Priority Order the part. Parts with a priority code of "P" are counted as
"Filled after ordering" on the Parts Management Report. In addition to the
"P" action code, "1," "2," "3," and "4" may also be used for priority orders.
All of these order codes are treated by the computer in the same way; the
advantage of having multiple priority order codes is that you can organize
your priority orders in five separate categories. Once a part that has a
priority code is ordered, it will have an "a" code regardless of its original
priority code.

There are other Priority codes that can be used in place of the large "P" on
a Point of Sale document.

R =Rob the reservation and do not order.
Q =Rob the reservation and order the part.
S = Place the part on a stock order.

L =Lost sale.

D = Dropship.

Uses of the code are explained below:

R= __ Rob the reservation and do not order
When you change the "P" to "R", you are robbing a reservation
created by another document at Point of Sale. The computer has
determined that there is not enough inventory available to fill the
reservation created by the document. Using "R" will allow the part
to be sold; however, no Priority order will be created for the part
and it will be counted filled "First Time" on the Parts Management
Report.

### [+] X5-3 Priority Orders

There are two reasons you might rob the reservation:

1. The inventory count is off. There are really 3 parts in the part
bin. The computer shows 2 parts in the bin. Selling 3 parts creates
a-] available. Back the cursor to the Pty field. Change the "P" to
“R" to rob the reservation. When the customer leaves, go to Parts
Posting and Maintenance (X3-2) and correct the quantity. Plus (P)
in one of the parts. Make sure you correct your inventory. Control
becomes a large problem if inventory is not corrected.

2. The part is really reserved for an internal work order. You would
rather sel] the part at a profit to a customer than place it on a piece
of your equipment. It may be cheaper to order the part on a regular
stock order than on priority order. Change the "P" in the Pty field
to "R". After the customer leaves, recall the internal document.
Remove the part from the document. Do not skip this step. It
corrects the inventory.

Rob the reservation and order the part

This would be used to sell a part reserved on a ticket to someone
else. For example a part was ordered for a customer (Mr. Smith). It
arrives and he will not be using it right away. Another customer
(Mr. Jones) needs the part now. When the part is typed onto the
document opened to Mr. Jones, a "P" appears indicating that the
part is not available for sale.

In reviewing the Reservations Report, you see a reservation for Mr.
Smith. Mr. Smith does not need the part now. On the document for
Mr. Jones, change the "P" to a "Q". You can then sell the part to
Mr. Jones and another part will be ordered for Mr. Smith. The
reservation is retained for Mr. Smith. His name will show on the
Reservations Report. The part is counted as filled "First Time" on
or,


X5-3 PRIORITY ORDERS [=]

the Parts Management Report.

When the part is received in Receive Order (X342-2,) no name or
customer address number will be displayed for the part on the
Receipt to Reservations Report. Run a Reservations by Part
Number Report. Determine who should receive the part and
process that customer's document.

S= Place the part on a stock order
Freight and UPS charges are usually higher on a Priority order than
on a regular stock order. If a customer is in no hurry to receive a
part, the part can be placed on a stock order to be ordered with the
regular stock order.

Change the "P" that appears on the part line to a "S". The part will
display on the Priority Order Queue in this job. Parts sold with
priority codes of "S" are counted as filled "After Ordering" on the
Parts Management Report when the "S" changes to "a" to signify
that they have been received.

When the order is accepted, a stock order is created, which is
named MMDDHHnd, where:

MM=Current month

DD=Current day

HH=Current hour in military time (4 P.M. is 16)

n=0-9 (orders for the same MMDDHH are numbered sequentially
from zero to 9)

d=division code

The parts are placed on MMDDHHnd. When you create a regular

stock order (X341-1 or X341-2), the parts can be moved from
order MMDDHHnd to the regular stock order with Move Order


(«| X5-3 PRIORITY ORDERS

Lines (X34-6).

Lost sale

When a part needs to be ordered, there is always a chance that the
customer will not want to wait until the part is received. The
customer may be able to go somewhere else to purchase the part.
Lost sales mean lost revenue. If there are not enough parts to meet
customer needs, something may be wrong with the dealership's
stocking levels.

When [Enter] is pressed on a part line, change the "P" to "L" to

indicate Lost Sale. The "L" increases the demand history for the

part. The demand history is used in the calculation formula for

Creating a Suggested Stock Order (X341-1). Parts with priority

codes of "L" are counted as Lost Sales on the Parts Management (
Report.

Dropship

Dropship means that the part ordered will be shipped directly to the
customer. The dealership will not receive the part. If this is the
case, change the "P" to "D". The Priority Order is processed as
usual. Parts sold with priority codes of "D" are counted as filled
"First Time" on the Parts Management Report. Processing the
order is explained in the section How to Run, later in this chapter.
Once the order is processed, there is no more tracking of the part
by the system.

An OPT (X636-14) allows you to decide whether you want
dropship parts from open and closed documents to be inciuded in
the priority order queue (default) o r whether you prefer to have
only those from closed documents in the queue. If a document is
opened to a dropship customer, place the Ship To address in the

{
RELEASE 2.2 \


Ship to field on the Point of Sale Sold to Screen. The document
must be closed to bill the customer.

Processing a Priority Code Document

When [Enter] is pressed on a part sale line, if the part is not available for
sale, a large "P” displays in the Pty field on the line. At that point, the
decision must be made as to which priority code is to be used.

Once the code is entered, the part is added to the document by pressing
[Enter] again. There are three fields at the top of the document. TDP.
T =tax code used, D = discount code used and P = priority code used.

The P field at the top of the document will display the priority order code.
For example, say the "P" remains as a Large "P". "P" means order the part.
The part is sent to the Priority Order queue to be ordered only when the
document is closed or placed on hold.

Only documents containing the priority order codes listed below will be
visible in the Priority Orders job (X5-3).

P = Priority order (1,2,3, or 4 will also work)

Q = Rob the reservation and order the part

D = Drop ship

S = Place the part on a stock order

You can see a field called Typ when reviewing a priority order. This field
holds the Priority Order code used at Point of Sale. P, D and S$ will be
visible as typed. If a Q was used, it will display as a P.

The codes L = Lost Sale and R = Rob the reservation and do not order,
will not display on the priority order.


X5-3 PRIORITY ORDERS oe

When the Priority order is accepted, (X5-3), the large "P" (or the 1,2,3, or
4) on the document in the P field at the top of the document becomes a
small "p". The small "p" indicates that the part has been ordered. If you are
reviewing the document, and the "P" is still large, the Priority Orders
(X5-3) job has not been run and the parts have not been ordered.

‘When the part has been received in (X34-2), the small "p" will change to a
small "a". The small "a" indicates the document can be closed and the
customer billed. The small "a" means available for sale. Parts sold with
priority codes of “a” are counted as filled "After Ordering" on the Parts
Management Report.

If the priority order code was changed to an S = place on stock order, an
"S" will display until the priority order is accepted in this job. When the
order is accepted, a stock order is created, which is named MMDDHHnd, (
where:
MMs=Current month
DD=Current day
HH=Current hour in military time (4 P.M. is 16)
n=0-9 (orders for the same MMDDHH are numbered sequentially from
zero to 9)
d=division code

The parts are placed on MMDDHHnd. When you create a regular stock
order (X341-1 or X341-2), the parts can be moved from order
MMDDHHnd to the regular stock order with Move Order Lines (X34-6).

Accepting the order changes the large "S" to a small "s" on the Point of
Sale document. When the order is received (X342-2), the smal] "s"

becomes small “a". The document can be closed and the customer billed.

RELEASE 2.2 LL


X5-3 PRIORITY ORDERS [2]

OTHER FACTS ABOUT PRIORITY ORDERS

Codes that display at Priority Order

Only Parts with priority codes listed below will display on the priority
order queue until the order is accepted.

P = Priority order (or 1,2,3, or 4)

Q = Rob the reservation and order the part
D = Dropship

S = Place the part on a stock order

Parts sold with priority codes of "Q," and "R" are counted as filled "First
Time" on the Parts Management Report.

Changing Priority Orders

In this job, you will have the opportunity to make changes to parts already
on the priority order. You will also be able to add parts to the order or add
parts to inventory and the order.

Parts are placed on Priority Order Queue by selling parts not available at
Point of Sale. When you enter the Priority Orders job, the computer
checks Point of Sale documents for priority order codes.

Any changes made to the priority order are not tied back to documents at
Point of Sale. Changes or additions to the order will not register until the
Priority Order is accepted or finalized. Do not go into the job to make
changes or add parts until you are ready to accept (finalize) the order.


If you leave the priority order without accepting the order, the program
assumes that any changes made were not valid. When you go back into the
priority order the second time, it will look like it did the first time you
reviewed it. The changes will have to be made again.

Receiving Priority Orders

When the parts are received, the order must processed in Receive
Order(X342-2). For information on this job, See Chapter X34-2, Receive
Order Menu.

If you have questions on how to sell partially received priority orders,see
Sell a Partially Received Priority Order in the Reference Section of Point
of Sale Invoicing (X5-1).

{
RELEASE 2.2 Le

### How To Run

You may review a Priority Order at any time in this job, however, do not
add parts or make changes until you are ready to accept the order. Changes
to priority orders do not register until the order is accepted. You will have
to repeat the work.

Selecting a Priority Order

After passing the security screen, the following screen displays:

LEE’S RENTAL COMPANY Price Book List x5108-591 1
Division : A Select Price Book

CASE TEST BOOK

CUB CADET TEST BOOK

FORD TEST BOOK

HARLEY DAVIDSON TEST BOOK

1 price book may be selected.

To select a Price Book enter any character in front of the name and press enter.

Cmdl-End job

 


O Place any character next to a price book and press [Enter].

The price book you select will be referred to when a non-inventoried part
is added to a priority order. Information will be copied from the price
book entry for that part into that line of the priority order.

LEE'S RENTAL COMPANY Priority Orders X$300-301 2
Acceptance

Accept?
(yam) Vendor: Lines
N CAS CASE/IH 2
N FRD FORD 55
N WHT WHITE 33

MAS MASSEY FERGUSON 5

Update priority order for vendor:
Include order types P: ¥ 1: ¥

(mdi-End job

O Specify which order types wiil be included in the priority order by
placing a "Y" or "N" in the seven fields at the bottom of the screen.
om


X5-3 PRIORITY ORDERS [=]

Accepting Priority Orders

On the screen above, there is an N (No) displayed under the Accept?
column. The order should not be accepted before it is reviewed. You may
want to make changes or additions to the order. Leave the N for No. This
will give you the opportunity to review the order before accepting it.

Accepting the order has the same result on priority orders as Print Final
Order (X341-3) has on stock orders. The result is that the order is finalized
and the order is printed.

When a part order is received at the dealership, you update computer
inventory by receiving the order in Receive Order (X342-2). An order
cannot be received in Receive Order (X342-2) until it has been finalized.
Once the order is accepted, the word Final will display in the Status field
in Order Inquiry (X34-4). Only when the word Final is displayed can the
order be received.

There is ne requirement as to the order in which you review Priority

orders. To review an order, type the Vendor Code for the priority order in
the Update Priority order for vendor: field. Press [Enter].


14 X5-3 PRIORITY ORDERS C

Valid Priority Order Options

Cmd3 Update Lines
After selecting the vendor, the Priority Orders Update Lines screen
displays. This is [Cmd3] Update Lines:

“ABC COMPANY PRIORITY ORDERS 5300-302
UPDATE LINES Page lof 2
Vendor MAN Lines 13 Amount 967.54 Accept? (Y/N) W
D-elete
Bypass = Part # Quick Customer Name Cost
Typ D/B Qty —Deseription Cede Addr # Document Sold by R/B Extend
2 a24140 WALTER CROME ow 89
STUD CRWAS9 CTOOSO1A N 1.78 (
a24314 WALTER CROME mw 12.61
MUFFLER cRWAS9 CTODSO1A N 12.62
825416 WALTER CROME 12.42
HOUSING CRWAB9 CTOOSO1A 12.42
25430 WALTER CROME 71.12
SWITCH CRWASD CTOOSOLA 71.12
A25541 LEROY GRADY 10.40
SHAFT GRLE25 CT00222 10.40
25552 JAMES UMPQUA 2.42
CLT UMJA91 40000034 2.42
425573 WALTER CROME 1.54
SPRING CRWAB9 CTOOSO1A x 1.54
25579 ALTER CROME 5.99
RETAINER CRWAB9 CTOOSO1A N 11.98

fress Cmal-End job; Cmd2-Change vendor: Cmd4-Add lines; Cmd5-Add new parts

 

At the top of screen the total number of pages in the order will display.
The Vendor code, the number of lines in the order and the total cost
(Amount) of the order is displayed.


RELEASE 2.2 XL


X5-3 PRIORITY ORDERS |

The Accept? (Y/N) field will display a N (No) just as the previous screen
did. You will change the N (No) to Y (Yes) when the order has been
reviewed and you are ready to accept or finalize the order.

The screen displays all the detail of the orders. The fields are described
below. Each part on the priority order takes up two lines on the screen:

### Fields & Descriptions

The fields on the first line are:
Typ This field will hold the Priority Code chosen
during Point of Sale Invoicing.

P will display if either a P = Priority Order
or a Q= Rob and place on priority order was
used at Point of Sale Invoicing.

D = Dropship will display if a D was used.
Tracking of parts with a D code stops with
the acceptance of the Priority Order. After
the order is accepted, it is up to the
manufacturer to ship the parts. The customer
was billed for the parts when the document
was closed.

S = Place on stock order. When the order is
accepted, all parts displaying S in the field
will be placed on a system-created stock
order, MMDDHHnd, where:

MM=Current month

DD=Current day


D/B

HH=Current hour in military time (4 P.M. is
16)

n=0-9 (orders for the same MMDDHH are
numbered sequentially from zero to 9)
d=division code

When you create a regular stock order
(341-1 or X341-2), the parts can be moved
from order MMDDHHnd to the regular
stock order with Move Order Lines (X34-6).

For more information on these codes, see the
Overview section of this chapter or Priority
Orders in the Reference section of X5-1
Point of Sale Invoicing.

When changing the Typ code, only S =
Place on stock order and P = Priority order
can be used. You may not change a code to
or from D = Dropship.

Delete or Bypass.

Type a D to delete a part from the priority
order. When the priority order is accepted,
the document will display a small "p" as if
the part has been ordered. The "p" indicates
the order has been accepted. Deleting the
part off the priority order does not eliminate
the reservation created by the Point of Sale
document.

Tf enough of the part is received on a
suggested stock order, the reservation is


X5-3 PRIORITY ORDERS [7]

filled. The small "p" becomes a small "a" at
Point of Sale. You can fill the order, close
the document and bill the customer. If the
reservation is filled, the customer will be
listed on the Receipt to

Reservations Report that is printed with
Receive Order (X32-2).

If you deleted the part because the customer
does not want the part, you must go to Point
of Sale and delete the part from the
document. The reservation will remain until
the part is deleted off the document or the
part is received on a stock order and the
document is closed.

Type B to bypass the part on the order. The
part will not be placed on this priority order.
The part will remain on the Priority Order
Queue until it is accepted with the order or
deleted off the order.

Qty Quantity of the part ordered. Quantity can be
changed. Type the quantity and press Field
Exit.

To register changes to any of the above fields, press [Enter]. The other
fields listed below are informational only. They cannot be changed in
Priority Orders. The information is generated by documents from Point of
Sale. If the information on the document is changed at Point of Sale, the
information will be different in Priority Orders.


Part #
Quick Code

Customer Name

Sold by

Cost

The fields on the second line:

Description
Addr #

Document

Part to be ordered.

Identifying code for the part as set up in
X3-2 Parts Posting and Maintenance.

The name of the customer as entered in
Receivables Maintenance (X11-2).
Employee Address Number of the employee
making the sale. The Employee Address
entered on the Point of Sale Sold To screen
in the Sold by field.

The cost per part of the item on priority
order.

Description of the part.

Customer's address number from
Receivables Maintenance (X11-2).
Document number from Point of Sale
containing the part for priority order.

If a document is closed with priority order
parts on it, a clone document is created. All
information about the parts is carried
forward to the clone document.

You can recognize a clone document by the
number of the document. When a document
is closed, an "A" is added to the end of the
document number.

A new clone document is created each time
.


X5-3 PRIORITY ORDERS |

a document is closed that has priority order
parts on it, the letter at the end of the
document number increases by one. A
becomes B, B becomes C and so on.

The document number will not be cloned if
the document is placed on hold. If the

document number does not have a letter
after it, the document was placed on hold.

RB Replaced by. Contains the Supersede code
entered at Parts Posting and Maintenance
(X3-2).

Extend Extended cost of the part. Cost times the
quantity ordered.

To see the next page of the order, press [Enter].

Cmd1-End job

If you are just reviewing the order, press [Cmd1] to end the job. You will
return to the Point of Sale Menu. After the order is accepted, [Cmd1] is
used to proceed to the next step in the job.


| 20 | X5-3 PRIORITY ORDERS

Cmd2-Change vendor

[Cmd2] will return you to the Priority Orders Acceptance screen. You may
choose another vendor by typing the Vendor code for the priority order. If
you choose a different set of order types for the same vendor, the
following screen appears.

Priority Orders x5300-305

Vendor CAS has previously been updated in this Prioxity Orders
session with different order type selections. Please enter ene
of the folowing options: 1

1. Retain previous selections and return to the Acceptance screen.

2. Retain previous selections and continue to the Update Lines screen.

3. Delete previous selections and continue to the Update Lines screen.

The selections this screen is referring to are the settings for the order types
at the bottom of the Acceptance Screen. At any time, the system can only
use one set of selections for each vendor. Once you change a set, this

screen appears to give you a choice between accepting the old or new
settings.

Ne


X5-3 PRIORITY ORDERS [=]

Cmd4-Add lines
To add parts not reserved on a document at Point of Sale, use [Cmd4].
When [Cmd4] is pressed, the following screen will display:

‘ABC COMPANY Priority orders 5300-303
add Lines
Vendor MAN Lines Amount 967.54 Accept? (¥/N) N

emdl-End  Cmd2-Change vendor —cmd3-Update lines

 

Cmd5-Add new parts
Enter P to place the part on the Priority Order or S to place the part on a
stock order. If S is used, the part will be placed on a system-created stock
order, MMDDHHnd, where:

MMz=Curtent month

DD=Current day

HH=Current hour in military time (4 P.M. is 16)

n=0-9 (orders for the same MMDDHH are numbered sequentially from

zero to 9)

d=division code


[=] X5-3 PRIORITY ORDERS

When you create a regular stock order (X341-1 or X341-2), the parts can
be moved from order MMDDHHnd to the regular stock order with Move
Order Lines (X34-6).

Enter the quantity of the part to be ordered in the Qty field. Press Field
Exit.

Part Number to be ordered.

If the part number is in inventory:
Type the part number to be ordered in the Part # field. Press [Enter].

If the part number is not in inventory:

Type the part number to be ordered in the Part # field. Parts must be
segmented to match configuration for the vendor in Configure
Vendor/Class (X38-1). See Parts Posting and Maintenance (X3-2) or
Adding Parts in the Reference section of Point of Sale Invoicing
(X5-1) for more information on segmentation. Place a < at the end of
each part segment.

Only the part number has been added. To add information about the
part, proceed to Parts Posting and Maintenance (X3-2). If you have a
price tape for the vendor, information from the price tape can be
supplied to parts by running Price Tape Update (X37-2). The price tape
would contain information such as part description and price. Part
information can be supplied if the part is added to inventory _ using
[Cmd5] Add new parts. With [Cmd5], the part is added to the

ptiority order and to inventory along with information.

Press [Enter]. If no errors are on the screen, the screen will clear. Press

Cmd3-Update lines to return to the Priority Orders Update Lines screen.
The parts added will display with the other part on the Priority Order
Co.


X5-3 PRIORITY ORDERS [=]

Update Lines screen.

Reservations are created by Point of Sale documents. Parts added to a
priority order with [Cmd4] are not reserved.

Cmd5-Add new parts

When [Cmd5] is pressed, the following screen displays:

‘REC COMPANY Priority Orders x5300-304
Store: D add New Parts

Order gty..:
Vendor: MAN Part number:
Class.: F Quick code.:

Order code: A Return code:

sug.

Order type.:
Description:
Location...:

Part category: Weight:

Internal Dir. Net

1 1
Maximum, : Qty. rqd.:
Multiple: Discount. :

cmd2-Change vendor © Cmd3-Update lines  Cmdd-Add lines

 

When Cmd5-Add new parts is used, the part will be placed in inventory
and placed on the order. If the part is already in your inventory, [Cmd5] is
not a valid option. Use Cmd4-Add lines to add parts if parts are already in
inventory.


[=] X5-3 PRIORITY ORDERS

### Fields & Descriptions

In defining the fields, C = character (letter or number). D = digit(number).
All decimals are assumed. Do not type the decimal point. Example: 5.2 D
= five places in the field with two assumed decimal places.

Order qty

Order type

Vendor

Part Number

5.0 D (required)

Quantity to be placed on the order. Type the number
and press Field Exit.

1 C (required)

Type P for Priority order and S for Stock Order. If P
is used, the part will be placed on the priority order
you are currently working with. If S is used, the part (
will be placed on an order called MMDDHHnd,
where:

MM=Current month

DD=Current day

HH=Current hour in military time (4 P.M. is 16)
n=0-9 (orders for the same MMDDHH are
numbered sequentially from zero to 9)

d=division code

When you create a regular stock order (X341-1 or
X341-2), the parts can be moved from order
MMDDHHnd to the regular stock order with Move
Order Lines (X34-6).

3 C (required)

Vendor code for the order.

18 C (required)

Enter the part number to be placed on the order and

RELEASE 2.2 Ne


X5-3 PRIORITY ORDERS [=]

in inventory. The part number must be segmented to
match the configuration for the vendor. Use the < to
signify the end of each segment. For more
information on segmentation, see X3-2 Parts
Posting and Maintenance. Only 18 characters can be
entered, however, 22 spaces are available to display
the part in expanded form.

Description 16 C (recommended)
Description of the part. If a price tape for the vendor
is available, description can be updated later by
running Price Tape Update (X37-2)

Class 1 C (required)
The field will contain the class entered in the
Default class field in Configure Vendor/Class
(X38-1). You may change the code to any valid
class.

Quick code 7 C (optional)
Part identifying code as set up in Parts Posting and
Maintenance (X3-2).

Location 8 C (optional)
Bin location of the part
Order code 1 C (required)

A = Automatic, C = Combined, M = Manual
Default is from Default Class information in
Configure Vendor/Class (X38-1). The order code
may be different for individual parts within a class.
If the class code is changed, check the order code,
too. It will not change automatically, and the order
code on the part record is what rules ordering.
Return code 1 C (optional)
Code designating vendor's return policy. Furnished
on some price tapes. R = Returnable, N = Not


Part Category

Weight

Price. . .

Price
Base

Minimum

returnable. You may use this field as desired.

1 C (optional)

Option is furnished on some price tapes as: A =
Accessory, P = Part, or O = Other or a preseason
indicator. You may use this field as desired.

5.1 D (optional)

Weight is required by some vendors. May be
supplied on some price tapes.

5.0 D (recommended)

Fill in all four prices to match the pricing
configuration set up in Configure Vendor/Class
(X38-1). See Pricing Information in Chapter X3-2
Parts Posting and Maintenance.

Dir. List - Selling price of the part. (
Sug. List - Manufacturer's suggested selling price.

Internal - Dealer defined. May be used to display
competition's price.

Dir. Net - Cost of the part.

If a price tape is available for the vendor, pricing
can be added later by running Price Tape Update
(X37-2). If pricing is not added when the part is
added, the amount (cost of the parts on the order) of
the order will not reflect the cost of parts added.
1.0 D (required)

Base fields will contain the defaults from the
Default Class of the vendor set up in Configure
Vendor/Class (X38-1). See Pricing Information in
Chapter X3-2, Parts Posting and Maintenance.

5.0 D (optional)

Field is used by the C Combined order code. It is

f
RELEASE 2.2 NL


X5-3 PRIORITY ORDERS [=]

the minimum quantity you wish to keep on hand or
the best reorder point.

Maximum 5.0 D (optional)
Field used by the C Combined order code. It is the
maximum quantity you wish to keep on hand or the
best restocking level.

Qty rqd 3.0 D (optional)
Quantity required. The quantity of this part which is
required to do one job, sometimes referred to as
“Per Job". May be furnished on some price tapes.

Package 5.0 D (optional)
The number of parts in a package. May be furnished
on some price tapes.

Multiple 5.0 D (optional)
Vendor Multiple. The number of units in the part
number. Example: 55 gallons of oil come in one
drum. The vendor multiple is 55.

Discount 5.0 D (optional)
Quantity which must be ordered to receive a
discount from the manufacturer.


28 | X5-3 PRIORITY ORDERS C

Below is an example of a screen with the fields filled in:

‘ABC COMPANY Priority Order %53000-304
Stexe: D Add New Parts

order gty. 3 Order type.: P
Vendor: MAN Part Number: <Q<43629¢< Description: FILTER
Class.: F Quick Code. : Location...; F312

Order code: A Return code Part category: Weight:

Dir, List Sug. List Internal Dlr. Net
379 349 391 269
3 3 1 z

Maximum: Qty. rqd.:
Package: 2 Multiple: Discount.: 40

€mdl-End  Cmd2-Change vendor Cmd3-Update lines Cmid-Add lines

 

When the information is typed, press [Enter]. The following message is
displayed at the bottom of the screen:

DIS-5159 New part number. Press ENTER to update parts file

If you fail to press [Enter], the part is not completely added to inventory.
This type of error can create serious part file errors.

MAKE SURE YOU PRESS ENTER.

When the part has been added successfully, the following message is
displayed:

DIS-5156 Part file has been updated

i
RELEASE 2.2 —


X5-3 PRIORITY ORDERS [=]

Add more parts, as necessary. When all parts have been added to the order
and inventory, press [Cmd3] to return to the Priority Orders Update Lines
screen where changes and additions can be seen.

Reservations are created only on Point of Sale documents. Parts added to
the Priority Order with [Cmd5] will not show as reserved.


20 | X5-3 PRIORITY ORDERS

 

### Accepting The Order

Below is an example of the Priority Orders Update Lines screen after all
changes have been made:

S20 COMPANY PRIORITY ORDERS x5300-302
UPDATE LINES Page lof 2

Vendor MAN Lines 14 Amount, 980.99 Accept? (Y/N) N

Drelete

Brypass Part # Quick Customer Name cost

Typ D/B Qty Description Code Addr # Document Sold by R/B Extend
1 Azdi40 WALTER CROME 89

sTuD CRWABS CTO0SO1A Jw N -89

Aza31d WALTER CROME 12.61

MUFFLER CRWABS CTO0SO1A ow N 12.61

AZ54i6 WALTER CROME 12.42

HOUSING CRWABI CTOOSC1A 12.42

A25430 WALTER CROME 71.12

SWITCH cRWAgS CTOOSOLA 71.12

A25541 LEROY GRADY 10.40

SHAFT GRLE2S CT00222 10.40

25552 JAMES UMPQUA 2.42

BOLT UMJA91 WOOCO0IA 2.42

A25573 WALTER CROME 1.84

SPRING CRNAB CTOCSO1A 1.54

425579 WALTER CROME 5.99

RETAINER, CRWA89 CTOOSO1A N 11.98

943629 2.69

FILTER N 13.45

 

Press Cmdl-End job; Cmd2~Change vendor; Cad4-Add lines; Cmd5-Add new parts

 

When the order is complete, move the cursor up to the field in the upper
tight hand comer of the screen Accept (Y/N). A N (No) currently displays.
Change the N to ¥ (Yes). Press [Enter] to register the change to the field.

{
RELEASE 2.2 Ke


X5-3 PRIORITY ORDERS [=]

The same screen will be redisplayed. press Cmd1-End job. You will
advance to the next step in the job.

Processing Dropship Orders

The Priority Orders Drop Ship Header screen will display:

LEE‘S RENTAL COMPANY Priority Orders 45300-5011
Store: A Drop Ship Header

Vendor Code MAS order Date 3/16/95
Order Number CT00102 Dealer Number
Special Instructions

Drop ship to: LEROY GRADY

$692 BRITT RD

MT VERNON, WA 98273

Retain Drop Ship Order for Download? (¥/M) N

Cmdi-Cancel

 

The Vendor Code and Order date will display. The document number will
be visible in the Order Number field for reference.


[=] X5-3 PRIORITY ORDERS —

The Dealer Number field will contain the information in the Dealer
Number field at Configure Vendor/Class (X38-1). If a Dealer Number is
not displayed, one may be typed. You may also change the dealer number.

Special Instructions field can be filled in as you see fit. Some dealerships
type special shipping instructions.

The "Drop ship to" field will contain the information entered in the Ship
To field on the Sold to Screen of Point of Sale (X5-1). If nothing was
entered, the field will be blank.

The "Retain drop ship order for download" field at the bottom of the
screen allows you to save this dropship to a file. This file will be referred
to when the file is downloaded.

To advance to the next screen, press [Enter].

There will be a separate Drop Ship Header screen for each customer who
is to receive a dropship order.

When all the dropship orders have been processed, the Priority Orders
Order Header screen will be displayed.

Processing Priority Orders

Dropship orders are processed first. See the previous section. If no
dropship orders are on the Priority Order Queue, the Priority Orders Order
Header screen will be the first screen displayed.

RELEASE 2.2 LL


X5-3 PRIORITY ORDERS [=]

Below is an example of the Priority Orders Order Header screen:

ABC COMPANY PRIORITY ORDERS x5300-502
Store: D ORDER HEADER

Vendor code MAN Order date 9/17/96
Order number 0917860A Dealer number 03426
Special instructions

Press Cmal to cancel job

 

The Vendor code and Order date will be displayed. An order number is
assigned, which is the system date, mmddyy0A, which may be changed.
The Dealer number will contain what is typed in the Dealer number field
at Configure Vendor/Class (X38-1). If one is not displayed, or the one
displayed is not correct, you may correct the field.

You may enter any information you want in the Special instructions field.

The field should refer to special shipping instructions for the
manufacturer.


ae | X5-3 PRIORITY ORDERS .

### Sample Report

When the screen is complete, press [Enter]. The order is finalized and a
copy of the order will be printed.

ABC COMPANY
288 W. KELLOGS RD
BELLINGHAM, WA 93226

Order Number 01126700

ee.
MANUFACTURER azi9a
Oty Pare t—- -++ Description ost amount Locatice Pack

a2ano step 89 wee sane (

24314 MUFFLER - F409

25426 HOUSING . F4-93

a25830 SurTcH

425573 SPRING

28579 RETAINER

43260

363891

spoz0ce

 

RELEASE 2.2 LO


X5-3 PRIORITY ORDERS [=]

ABC COMPANY

Order Number 01128708
Dealer Nunber

MANUPACTURER, asi2sge

+ 4 Of Lines

+ # 0€ Pacts

+ pollars

 

The report is divided into two sections.

The first section lists the order detail. The part numbers, descriptions and
quantities ordered will be printed twice. You can split the report and send
the order information to the vendor.

The second section of the report is a recap of the number of part lines, the
number of parts and cost of the parts on the order.


[=] X5-3 PRIORITY ORDERS C

### Recovering Priority Orders

The command key recovery [Cmd24], which was used in previous releases
(prior to Release 2.1), has been eliminated and replaced by a more reliable
method. The rules for working with priority orders are the same:

= Only one workstation in each division can be using a priority order
option.

= Until the first workstation has completed its priority order option
successfully, no other workstation can use any of the priority order
options.

It wasn't always possible to know for sure which workstation had been (
using which priority order job; therefore, a screen has been added to

clarify what needs to be done to recover successfully. If any other

workstation in Division A selects any one of the four priority order options
before the first workstation has ended the job normally, the following

message, which is explained on the next page, is displayed:

f
RELEASE 2.2 We


‘Nit EQUIPMENT SALES Priority Orders X5300-B01,
Division: A

Only one workstation per division may process priority orders at the
same time.

Workstation AF is either currently running this job from Menu X53 or
was interrupted before the job covld complete.

If workstation AF is not currently running this job from Menu x53,
xestart this job from Menu X53 at workstation AF to either cancel or
finish the priority orders.

Press Enter to return to the menu.

 

For example, if workstation AF enters Priority Orders from the Point of
Sale Menu in Division A, no other workstation in Division A can start any
of the other priority order jobs (Case, Viscom, or Navistar) until
workstation AF has ended its job normally. If workstation AF is still using
Priority Orders, it must complete the job normally. If workstation AF was
interrupted while it was processing priority orders, it must re-enter the
same menu option, which will resume at the point of interruption, and
complete it normally.


Notes:

## CHAPTER X5-4

END OF MONTH PROCEDURE

### Introduction

Point of Sale End of Month Procedure is a job that should be run at least
once a month. It can be run more than once a month to improve
performance at Point of Sale.

This procedure takes care of necessary file maintenance and file
reorganization for Point of Sale Invoicing. It cleans up the main Point of
Sale file, u.SAM (u = your user ID). All documents that were closed and
posted before the cutoff date you designate are removed from the
document index.

Why is this helpful to you? Since all documents are listed in a customer's
document index, it can become a chore to find the one you want. The list
can be very long and the process time-consuming. Running End of Month
Procedures decreases the size of each customer's document index by
removing closed, posted documents.

Before document detail is removed, run the Salesperson and Labor
Analysis Reports (X56-3 and X56-4).


[2] X5-4 END OF MONTH PROCEDURE

### Preparation

Before running Point of Sale End of Month:

O Run Priority Orders (X5-3) to process any dropship parts.

O Run the Salesperson and Labor Analysis Reports (X56-3 and X56-4).
O Backup your data files (X6-1).

O Make sure no Point of Sale or Rental Invoicing jobs are running.

### How To Run

Point of Sale End of Month Procedures is divisional. The job can be run
for the division used at the security gate only; however, the first screen
allows you to indicate whether you want to include other divisions. The
following screens are presented:

O CAUTION and Division information

D Cutoff date

Division selection (if you indicate on screen 1 that other divisions
would be included).

 

 

 

 

From the Point of Sale Menu (XS), select option 4. After passing the
security gate, screen | appears.

RELEASE 2.1 LL


Point Of Sale End Of Month x5400-102

CAUTION! You are about to begin the Point Of Sale End Of Month Procedure.
There must be no P.0.S. jobs xunning until this job is finished.

Check to see that no jobs: invoicing, maintenance, posting or
reports are running before you continue.

1. Division L only.
2. Select other Divisions.

Enter option number

Please enter "1" {current division), or *2" (select division).
Gmd1-Cancel

 

To run the job for the division selected at the security gate, select option 1;
to run the job for selected divisions, select option 2. The cutoff date
prompt (screen 2) appears.


[ «| X5-4 END OF MONTH PROCEDURE ;

POINT OF SALE END OF MONTH X$400-501

Enter Date + 52892 (empyy)

All documents closed and posted from this date and prior will be deleted.

 

O The system uses the current date as the default. Type the cutoff date
(MMDDYY) you prefer, and press [Field Exit]. Documents that were
closed and posted before and including this date will be deleted.
Documents closed and posted after this date are retained.

O Press [Enter]. If you indicated on the first screen that you wanted to
select other divisions, a modified Combined End-Of-Months screen
appears.

RELEASE 2.1 LL


A & R EQUIPMENT Combined End-Of-Months 5420-101
All divisions’ Pos? W Printer

Ox, select individual divisions by entering a ¥ for that division below.
Note: Tf a printer is not specified, the system printer will be used.

Division Pos? Division POS?
Y
N
¥

Enter time if you want delayed execution: HEMMSS

(mdi-Cancel  Enter-Continue

 

To run Point of Sale End of Month Procedures, type a Y (Yes) next to the
divisions you want under the POS? column.

You may set the job up to run at a later time. Type the military time in the
field Enter time if you want delayed execution. The job will run at the time
entered. If the time chosen is after dealership hours, make sure you leave
the machine on so the procedure can run.


Notes:

RELEASE 2.1 Lo

## CHAPTER X5-7

PART SALES HISTORY

### Introduction

### Warning

Tracking this information takes a lot of disk space. To track 150

invoices a day, each with an average of 4 part lines, requires 7.2-8.5
MB per month on an AS/400 or 2800-3300 blocks per month on a

| S/36.

L__—

 

Use Part Sales History to review sales and returns by any combination of
the following items:

= Customer or Unit Number

= Vendor or Vendor and Part Number
= Date range

= Document number

Quick codes may, also, be used to access part information. Results are
always displayed on screen first, and you can Tequest printouts, if desired.

Part Sales History is installed from the OPTDIS Library (X636-9), The
default is not installed. The detail displayed by this job is usually removed
from the system by the End of Month Procedure (X5-4). After the Part
Sales History OPT has been installed, go to Security Maintenance (X6-6).
Look for the field labeled "Part Hist Mos" and enter the number of months
you want to keep (up to 999). The system begins tracking part sales
history the next time a Point of Sale Posting Batch (X55-1) is created.

Although detail is retained only as long as specified in Security
Maintenance, the history summary is maintained as long as the customer
or unit number remains in the system. If customers are deleted, their part
sales history is deleted the next time Parts End of Month Procedures (X3-
9) are run, regardless of whether their history falls within the specified
number of months.


[2] X5-7 PART SALES HISTORY c

Since this job deals with history files, it is possible that one or more items
may have been deleted since the document was created, such as the
division, customer, unit number, vendor, or part number. Even so, it is
possible to look up the history.

RELEASE 2.2 tO


X5-7 PART SALES HISTORY [2]

### How To Run

From the Point of Sale Menu (X5), select option 7, Part Sales History, or
from Point of Sale Invoicing, press [Cmd11] for the Additional Options
Menu where Part Sales History is option 10. The Part Sales History
selection screen is displayed, as illustrated below.

A & R EQUIPMENT PART SALES HISTORY

xS7002-02
Division L

Parameter Selection

Verdor/Paxt Nunber .;
Beginning Date .. —

Ending pate : aompry)
Document Number .

Gndi-End  Cmd5-History Summary  Crdi2-Change Division

 

O Type your selection criteria, and press [Enter]. You may search using
one or more of the fields described below.

Customer or Unit Number _If the customer number is not known, type a
few characters of the last name in the field
labeled "Name," and press [Enter] to select
from the customer index.


Vendor
Vendor and Part Number
Date range

Document Number

3-character code associated with a parts

vendor.

To select a particular part number, both the
vendor code and part number are required.
To select one day, use the same date for the

beginning and ending dates.

If more than 1 document was associated
with a document number, all documents are

displayed for selection.

The default is for the division that was selected at the security gate;
however, you can change the division by pressing [Cmd12] on the
selection screen. The following screen is an example of the Customer
Index displayed after entering information on the "Name" field.

PART SALES HISTORY

‘SHAW PAPER SUPPLY
SHOP EXPENSE
SMETH, DAVE

SOME CREDIT CARD
SHBDELIUS, STEVE
‘TERRIER, TEDDY
‘TSKRS NATURAL GAS

‘TEXAS NATURAL GAS--GARAGE
THANK YOU FOR YOUR BUSINESS

‘TRUMAN, JACK
‘TRUMAN, LARRY
‘THOSHOES, ANY
UMPQUA, JAMES
USA, ANTHONY

Cndi-End Cmd3-Return  Rell-Page

Baie codes
22345678901

Ce

mH
RM
RN
RK
aod
Rt
RX
mH

RN
RM
vg
BS
Re

 
Cc

\


X5-7 PART SALES HISTORY [=]

Command Key Options

Cmd1-End Ends the job and returns to the menu or to
the Point of Sale document if Part Sales
History was requested from the Additional
Options Menu.

Cmd5-History Summary Displays a summary of the current request,
which can be printed, if desired. Does not
apply to searches by document number. See
History Summary.

Cmd12-Change Division Displays the Parts security gate.


[ «| X5-7 PART SALES HISTORY co

### History Summary

Individual part sales documents and lines are retained for the number of
months specified in Security Maintenance; however, history summary is
available as long as the customer or unit number remains in the DIS
system. If customers are deleted, their part sales history is removed the
next time Parts End of Month Procedures (X3-9) are run, regardless of
whether their history falls within the specified number of months.

Q Press [F5] on the selection screen to see a summary of the current
request. There is no history summary when a document number is
requested.

History Summary Screen (

A&R EQUIPEENT PART SALES HISTORY x57003-09
Division L History summary
CAINOO CATE CONSTRUCTION CO. INC.

Part Total Discounts
‘11997"* Lines quantity Subtotal Surcharge

ganwary..
February. 4,961.12 2,561.22

March...
April...
may.

yely.
August...
September
October.
November.
December.

Totals... sa a 2,962.22 1,581.12

cmdl~End Cnd3-Return Crd6-Prine R011-Page

 

RELEASE 2.2 LL


On the history summary screen you can roll to the next or previous year.

Command Key Options

Cmd1-End Ends the job and returns to the Point of Sale
Menu or to the Point of Sale document if
Part Sales History was requested from the
Additional Options Menu.

Cmd3-Retum Returns to the selection screen.

Cmdé6-Print Prompts you for the number of copies and
prints the results of the current search. See
History Summary Report.

Roll-Page Roll to the summary of the next or previous
year.

History Summary Report

A & R EQUIPMENT
Division:

Part Sales #iscory Repore Date + 8/02/97 Page: 2
History Summary PS1:08 xS709~-a,

CAINOS CAIN CONSTRUCTION CO. INC.

Part Toca,
ory

october...
Novenber.
December.

Totals...

Discount/
Subtotal ‘surcharge

2,561.12 2,963.12

1,562.12


|e | X5-7 PART SALES HISTORY

### Transactions Screens

The screens in this section show the results of searches using various
combinations of selections. Note the position prompt at the top which you
can use to list transactions on or after a certain date. Purchase order
numbers are on the transaction screen and the transaction report. Each
transaction is listed on 2 lines in order to include ail pertinent information.
Column headings are displayed on lines 4 and 5. A negative quantity and
total indicates a return.

Address Number

You may search by either customer address number or by unit number. If
the customer's address number is not known, enter a few characters of the (
last name and press [Enter] to select from the customer index.

A&R ZQUIPHENT PART SALES HISTORY x57001-02

Division % Transactions Position to + campy)
Selection : HOL0d0 Dates : 00/00/00 To 99/99/99

ven Pare Nuaber Deseription ise gty price votal
Addrk Customer Name Document Date POR

cas 121629¢3 2 13.50 13.50
HO1040 HONEY LAKE WILDLIFE TR17175 4/20/97

cas 1967094C1, a 6.16 24.64
401040 © HONEY LAKE WILDLIFE K20741 8/01/97

KRS 62-263 4 6.26 24.64
HOL040 «HONEY LAKE WILDLIFE 3K20741 8/01/97

ME 1901234m1 L 3.78 3.78
Ho1040 © HONEY LAKE WILDLIFE 1K20862 4/07/97

MIS  MTP-24 L 78.95 78.98
H01040 HONEY LAKE WILDLIFE 1K25312 3/11/98

MIS MTP-24 t 78.95 74.95
HO1040 HOMEY LAKE WILDLIFE 1K25312 3/11/98

cas 1272956C92 z 249.00 249.00
HC1040 HONEY LAKE WILDLIFE 1K262398 8/01/98 HYD CYLINDER
Cmdl-End Cnd3-Retura Gnd6-Print Cndl0-Totals

Rell-Page Home-Top of List

Transactions are in
order by:

1) Date
2) Vendor
3) Part Number

  

RELEASE 2.2 LO


Unit Number


The following screen illustrates a search by unit number:

‘ASR EQUIPMENT

Division
Selection

Ven Part Number

Addr

HON ¢R65700
190003
RON cASSaE6
1690003
HON ¢A65927
90003
HON cAss940
190003
HON cA65379
90003

cnél-ena
Roli-Pase

PART SALES HISTORY
Transactions

= MOLogo Dates :

Description

Disc ory
custoner Nane Document
PRELUDE MAT BIAC
BRIAN BOCHET

CHROME RUOP RACK
KI CORVETTE

BLOCK HEATER BRK
woooeas

wooocea

woo00ee

wooooss

wooooes

Cnd3-Return — Crd6-Print
Home-Tep of List

(néi¢-Totals

Position to

¥57001-02
gamer)
Te 99/99/95
Price Total
Dace Pot

90/00/00

15.50
5/04/98

38.22
5/04/98

5704/98
6.34
soars
14.20
5/04/98 WARRANTY


Vendor or Vendor & Part Number

Searches can be made using only a vendor code, which lists all parts for
that vendor, or, if you're interested in a particular part, using a vendor code

and part number.

A&R EQUIPMENT
Division

Selection + cas
Ven Pare Number

Addr# Customer Name
cAS BSTASIA

RO0625 —-ROBERT ROBERTS
cas 1316563c2

ROO625 —-ROBERT ROBERTS
CAS 223-20
700625
cas 223-31
ROD625 ROBERT ROBERTS.
cas 90-11SeTL

ROOLIL RAMSEY & BECKETT
AS 90-710272

ROO11] «RAMSEY & BECKETT
cas 90-7636T1

ROOLIL RAMSEY & BECKETT
cas A77470

ROO2i0 «MARTIN ROGERS

Omdi-Ené  cmd3-Retura  cmd6-Print
Roll-Page Home-Top of List

Description

ROBERT ROBERTS

PART SALES HISTORY
‘Transactions

Dates :
Disc ty
Document

T1564,

IRL66¢3

s
TeL66aa

TKL66¢4

IK16696

Tx16646

TK16646

2K26703
cndi0-Totals

Position to :
09/00/00

Price
Date POW
26.25
4/09/97
26.25
4709/97
56
4/09/97
+60
4/09/97
29.81
4/09/97
29.52
4709/97
29.
4/09/97
23.
4/20/97

 

B x57001-02
camry)
To 99/99/99

Toral
52.50
52.50

2.80

3.00


Beginning & Ending Dates

Searches can be made over a date range. To find transactions for one
particular day, use the same beginning and ending dates.

A & R EQUIPMENT PART SALES HISTORY B x57001-02,
Division 1 Transactions Position te : ameDry)
Selection : Dates : 09/09/1995 To 09/09/1998
Ven Part Mumber Description Diss gry Price Total
Adért Customer Nane Document Date Ow

MF 1751670M91 2 37.69 37.68
100040 COUNTRY COOP IK21779A 9/11/97 M/F 135

MF 19012162 a 3.77 15.08
P0080 = DRAKER CONSTRUCTION ws0g771 9/11/97

MP 1902217". 20.92
POOC8O © —-DRAKER CONSTRUCTION wsos771 9/11/97

MF 1901232M1. 2.01 -02
DO0360 JAMES DEN K21849 9/11/97

MP 29012¢em1 5.46 92
00080 © DRAKER CONSTRUCTION wgos771 9/11/97

MF 19028591. 2.08 36
00360 GAMES DEW reales 9/11/97

MF 5052371 L 6.28 6.28
TEMP : IK2i590A 9/11/97 JOHNNY TURNER

MF $05236n1 4 1.85 7.40
Temp : IK21$90R 9/11/97 JOHNNY TURNER
Cmdl-Ead Cmd3-Return cmd6-Print cmdl0-Torals

Roll-Page Home-Top of List

 


[| X5-7 PART SALES HISTORY °

Document Number

Searches can be restricted to one document. If the original document
included internal or warranty lines, which generated separate documents, a
document index is displayed; otherwise, the Document Detail screen,
illustrated below, is displayed immediately.

Each line from each invoice containing the part number displayed above
will be listed. If the part number was sold twice on the same document,
both transactions will be displayed.

A & R SQUIPHENT PART SALES HISTORY X57001-96
Division Document Petail

Document | 0977, address # + #00080 B  FAREER cousmerten
fess syns (

ene | poss evo0rea

Ven eet mater = eriocion sige @ty Pade at

190320me 2 5.46 10.92
3

ATE 1.75 5.25

Cmdl-End CadJ-Return Cmd6-Print  Cnd2O~Totals
Roll-Page Home-Top of List

 

Note: The vehicle line shows the make, model, year, serial number,
hourmeter (or odometer) reading, and type of warranty.

RELEASE 2.2 Lo


X5-7 PART SALES HISTORY |

Document Details Report

Ak R ZOUIPHENT Port Sales History Report pace: 4/08/98
Division M Lecument Details ime: 14:16:40

Document : #308771 Address ¢ ; POUOG] DRAXER CONSTRUCTION
PO # : a9-s500921, Add: 15/11/97
Sold By Ship To + suRKO2 Print: 19/12/97

Vehicle + rans: 19/12/97
ven Pare Number Description Diss Qty Price otal
cas 11624 26.29 78.87
cas 49536 3.07 3.07
cas 73153 7.36 7.96

 

Command Key Options

Cmd1-End Ends the job and returns to the Point of Sale
Menu or to the Point of Sale document if
Part Sales History was requested from the

Additional Options Menu.
Cmd3-Return Returns to the selection screen.
Cmd6-Print Prompts you for the number of copies and

prints the results of the current search. See
Transactions Report.

Cmd10-Totals Displays totals of part lines, quantity, etc. of
the current search. See Selection Totals
Screen.

Roll-Page Roll to the next or previous page.

Home-Top of List Returns to the top of the current search.


Transactions Report

A&R EQUIPHENT
Division: 4

Selection + 39003
Fare Number

cass700
cases
cass927
cass920
cass979,

Part Lines ..
Total Quantity .

Press [Cmd6] to print the current search. The results which correspond to
the part sales history for the customer in the previous example are shown

below.

PRELUDE MAT SLAC
CHROME ROOF RACK
BLOCK HEATER BRK
ACC/CIVIC SWITCH
TAN DRV-GLOVE $

Part Seles History Report Date : 8/02/97 Page +
‘Transactions Time: €:93:30 XS700+2a

Dates : 0/90/00 To 93/99/99
Price Total Addr ¥ Customer Name

N9c093 © Befan Bochet = WOUD044. 5/04/94
w90G03 Kim Corverce —woucnad « SyaKyaa
99993 Barb Pretty wooega4 — s/0cr9a
N90003 Kristina Engine woogoad 5/04/94
N90303—Incernal wonoge, §/04/94 785 Pin

Subtotal... 145.54
Discount /Surcharge

148.54

 


X5-7 PART SALES HISTORY Ls]

Selection Totals Screen

Press [Cmd10] to see totals of the current search. The results which
Correspond to the part sales history for the customer in the previous
example are shown below. The Same screen is also available for any other
selection criteria, such as vendor or date range.

A&B EQUIPMENT PART SALES HISTORY ¥57001-06
Division 4 Selection Totals
Selection + cazNOG Dates : 00/00/00 To 99/9/99

Part Lines ...,

Total Quantity .

Subtotal ...., ce 1,562.12

Discount/surcharge ...:

4,561.22

Press any Key

Crdl-End — Cnd3-Return

 

You may press any key to return to the previous screen.


X5-7 PART SALES HISTORY Cc

### Fields & Descriptions

Fields on screens and reports in Part Sales History are listed in

alphabetical order.

Add Date (or Add) System-generated. Date on which the
document was added to the system
(originally opened).

Addr# or Addr # See Address Number.

Address Number 6-character customer address number.

Searches can be made by customer number
or by unit number.
Beginning Date Searches can be made based on a date range.
Transactions on and after this date will be
listed. See also, Ending Date.

Closed Date Date the document was closed.

Customer Name Customer's name as entered on their master
record.

Date Transaction date. Date on which document
was posted.

Description Description as entered in Parts Posting &
Maintenance.

Discount/Surcharge Discount or surcharge allowed.

Discount or Disc See Discount/Surcharge.

Document # See Document Number.

Document Number Point of Sale document number. Searches
can be made by document number.

Document See Document Number.

Ending Date Transactions up to and including this date
will be listed.

RELEASE 2.2 LU


X5-7 PART SALES HISTORY L7]

Name Customer's last name. Use this field on the
selection screen to access the customer
index.

Part Lines Quantity of different part numbers.

Part Number 18-characters.

PO Contents of the purchase order number field

on the Point of Sale Invoicing - Sold to
Screen. Internal and Warranty documents
contain the name of the customer to whom
the original document was opened.

Price Sales price of each part.

Print Date (or Print) System-generated. Date on which the
document was closed.

Qty Quantity of parts sold or returned.

Ship To System address of entity to ship parts to, if
different from Sold To.

Sold By System address of salesperson on the
document.

Subtotal Dollar amount of sales before discount or
surcharge.

Total Quantity multiplied by sales price.

Total Quantity The total quantity of parts (all part lines).
Negative quantities indicate retums at Point
of Sale.

Totals Dollar amount of sales.

Trans Date System-generated transaction date. Date on
which the document was posted.

Vehicle Make and model, year, serial number,

hourmeter ( or odometer), and warranty code
are displayed on this line.
Ven See Vendor/Part Number.


[| X5-7 PART SALES HISTORY

Vendor/Part Number

3-character vendor code plus a part number.
Searches made by vendor list all parts for
that vendor. To search for a specific part,
both vendor code and part number are
required.

## CHAPTER X5-8

RETAIL TRACKING

### Introduction

This is the sarne as Send Retail Tracking (X721-9). Use this option to transmit
retail tracking information to Case. The information collected includes quantity
on-hand, pieces sold, and quantity on order for each Case part you have in
inventory. In addition, the total dollar sales of Case and non-Case parts is
collected,

Before retail tracking information can be sent to Case successfully, you must use
Configure Vendor/Class (X38-1) to establish a Case vendor (CAS) in each
division. Jn addition, there must be a dealer number entered for the Case vendor in
each division (X38-1).

### Entrance Screen

A&R EQUIPMENT SALES CASE CORPORATION END OF MONTH C1ORT1-01
Division: A RETAIL TRACKING

Parts Retail Tracking data will be collected for the month displayed below.
Please ensure that this is the correct MMYY before continuing.

      
 

Month & Year (MMYY) 2. 2...

Do not change this
default unless

{ N - Send ali case part records )}) instructed by Case
{ Select N only if told to by Case ) to do so

Send only changed Case part records? (¥ or N) .. .

Cmal-Cancel job = Enter-Continue

X58.doc 3/29/99 1


2 X5-8 ¢ RETAIL TRACKING RELEASE 2.3

1. Change the current month year (mmyy) if necessary. C
2. Do not change the default on the prompt “Send only changed Case part

records=Y unless you are instructed to do so by Case.
3. Press [Enter]. The system will extract information from your parts files. This

process takes from 20 to 60 minutes per 10,000 parts, depending on how

many other jobs are running on the AS/400. The workstation where this job is

initiated will not be released until the data has been collected. You'll see the

following status messages:

Collecting Retail Tracking data
Adding Retail Tracking data to the Communications file
Retail Tracking data being sent to Case. Press Enter.

4. Press [Enter] to return to the Work with Communications Menu.

## CHAPTER X5-9

SELF SERVICE INVOICING

### Introduction

Self Service Invoicing enables customers with minimal knowledge of
Point of Sale Invoicing to create invoices. All sales are charge.

This job is designed to work closely with bar coding. You may want to
make up a card for each self service customer and print the customer's
receivable address as a bar code. In addition, each part can be labeled with
a bar code, which is one of its cross-references. The system uses the cross-
reference to find the vendor code and manufacturer's part number. The
cross-reference number is set up with a forced rob--obviously the part is
available if its bar code is being wanded. (Forced rob is an option when
the bar coding option is installed.)

Call DIS if you're interested in using bar coding at Point of Sale. A label
can be printed with the bar code that includes the vendor code and part
number.

Self Service Invoicing uses the normal Point of Sale program; however,
the screen looks different to the customer because most fields are hidden.
To limit the amount of information needed by the customer, Self Service
Invoicing relies on the following defaults:

 

 

 

Document Classification Code
0 Parts Sales Code (format "P")
QO Unique Point of Sale ID (not used for standard invoicing)

 

Except for the POS ID, you could use codes that are already in use;
however, you'll probably want to track self service sales better by setting
up new document and sales codes, which are identified in Self Service
Invoicing Defaults (X52-11).


 

 

RELEASE 2.1 Co


 

### How To Run

O From the Point of Sale Invoicing Menu (X5), select option 9, Self
Service Invoicing. The Entrance screen, which is the equivalent to the
POS Entrance screen, prompts for a customer number.

A & R SALES & SERVICE SELF SERVICE x5100-104
INVOICING-ENTRANCE

 

O The customer wands the bar code on her card or types her system
address number, which is not displayed on the screen, and presses
[Enter]. The verification screen, which is the equivalent of the POS
Sold To screen, is displayed.


A & R SALES & SERVICE INVOICING-VERIFICATION 5100-105,

SOLD TO

AUSTIN PARKER

ROUTE 2 BOX 588

‘LYNDEN

Purchase Order Number

=- OR --
Press Enter te Continue

CMD-10 Cancel/Void Sale

 

 

 

 

 

To void the sale and return to the Customer Number prompt, the
customer presses [Cmd10].

O To proceed with the invoice, the customer enters a purchase order
number, if any, and presses [Enter]. The detail screen appears.

RELEASE 2.1 a


 

Self Service Detail Screen

A & R SALES &
SELF SERVICE

TDP Line #

AP 0010 BE
AP 0020 EE
A 0030 BE
A 0040 BE

SERVICE SALES ORDER 5100-106
## 3301002 For PARKO1 CHARGE OPEN 10/13/93

Qty vVnd Part Number Description Bin Ext Price
2 ATE aioooo SNAP RING 5.32
5 API A11421 GASKET BF23 13,05
7 ATI adi24s OIL FILTER = _2A21 71.05
3 ATI A25611 BEARING 3.87

Spec order parts 19.80 Avail total 60.44 Total

SELF SERVICE

CMD-2 Close

Ven Qty Part number

CMD-6 Delete Last Part CMD-7 Return To Previous Screen

 

Part is not available
Settings established in X52-11, Self Service Invoicing Defaults, determine
what happens when a part is not available.

If Priority Orders from Inventory = Y, the customer will be allowed to
priority order parts that are normally part of your inventory; otherwise,
they must enter a different part number.

If Priority Orders from Price Book = Y, the customer will be allowed to
priority order parts from the price book; otherwise, they must enter a


 

different part number.
Valid command keys are listed at the bottom of the screen.

Buying parts
O The customer wands the bar code on the part label, which furnishes the
vendor code, a quantity of 1, and the part number, then presses [Enter].

C If bar coding is not used, customers must learn to press [Shift]+[Tab] to
reach the quantity field and [Field Exit] to reach the part number field.
Then press [Enter] to place the line on the invoice.

C1 When the invoice is complete, the customer presses [Cmd2]. What
happens next depends on the default established in X52-11, Self
Service Invoicing Defaults, Jf CMD2-Print & Close = Y, the invoice (
will be closed and printed; otherwise, the invoice will be printed and
held as an open document.

Note:

If "forced rob" has not been specified or bar coding is not active, and a

part is unavailable, the quantity and part number remain on the detail
line just as they do in normal invoicing. The customer can press
[Enter] to order the part (if allowed to priority order parts) or type in a
different part.

 

RELEASE 2.1 to

## CHAPTER X5-10

TECHNICIAN TIME CARD ENTRY

### Introduction

Technician Time Card Entry (TTCE) is a modified program from Time Clock
(Review by Technician). This program can be used as a punch-out system (just
like Time Clock); however, its purpose is not to account for every minute of a
technician’s time. The purpose of Technician Time Card Entry is to record

 

 

 
  
 

billable hours.

### Contents

OVERVIEW.........s:csssssesecsvessorseesavensuensesnescssansecausuenecssssacsseseatansrensasesesesseees 2
OPTIONS WINDOW .......cssssssssessesscsesssesseessentessatsnsrseeseeneessensacassnssssesessenss 3
ENTRANCE SCREEN .

DETAIL SCREEN

Standard Line Prompt

New Line...........

Work Order Index .. a

Crd 1 L-Options ......c..cesccceesssecssescessesseeceesersenseesseesesseeanessaeesaesaeeaenaeesaseasenseeases 8
SAMPLE TIME CARD ENTRY ..ssccsesesesessssssesssecassecsssscrsnesatsesersessesessenes 10
FIELDS ON THE TIME CARD ENTRY SCREEN. .........:ssssscsesssssesseeeesesee ah]

OPTS RELATED TO TIME CARD...

 

TIME CARD ENTRY SCREEN FOR THERMO KING DEALERG............ 15
AUTOMATIC RECOVERY.......csccsssssessetsstestsaseseseessessnssctssensnesssansansasansan 17


2 X5-10 # TECHNICIAN TIME CARD ENTRY RELEASE 2.3 Co

### Overview

Labor lines added in TTCE update Point of Sale documents immediately, and
lines can be changed as long as you don’t end the job. The price for this is that
there is no provision for deleting a batch; rather, lines must be deleted
individually. After the job is ended, existing labor lines can be modified only on
the work order. New labor lines can be entered in Technician Time Card Entry or
at Point of Sale. With Time Clock, on the other hand, labor lines cannot be added
or modified at Point of Sale.

An Options window, which can be displayed at the beginning of each session,
retains Time Card settings.

If a batch ends abnormally, simply re-select the Time Card option (X5-10) and
the previously entered data will be recovered automatically. See Automatic
Recovery on page 17.

 

### Warning!

Technician Time Card Entry will always assign the maximum billable hours to (
a job code every time it is used; therefore, on the work order, you may find the
job has been over-billed and will have to be adjusted.

 

 

Technician Time Card Entry has no reporting capability of its own, but the Labor
Analysis Report can be used to check technicians’ hours. It is not connected with

Technician Time Card Entry and Time Clock are mutually exclusive; that is, if
Time Clock has been installed, Technician Time Card Entry is not available and
vice versa.

If the Thermo King dealer OPT (X63B-6) is on, Thermo King job codes are
available and work the same as in Point of Sale. Because of its enhanced features
and reporting ability, Thermo King dealers are encouraged to use Time Clock
instead of Technician Time Card Entry.


POINT OF SALE X5-10 e TECHNICIAN TIME CARD ENTRY 3

### Options Window

If, in this window, “Display options at startup” = Y, this window is displayed
whenever you select Technician Time Card Entry from the Point of Sale Menu
(X5). These settings can be changed by pressing Cmd11-Options from the detail
screen. For more information on this screen, see Cmd11-Options on page 3.

Standard rounding or Start/stop time, enter in
always round Up (S/U) Minutes or Decimal (M/D)...
Round to Print time card (¥/N)
Display options at startup (Y/N!
Tenths
Quarters
Hundredths
106 min (1/6 hr)
30 min (1/2 hr)
5 min (1/12 hr)

If “Display options at startup” =
Y, this window is displayed every
time Technician Time Card Entry
is selected.

UePHoOR san

Omd3-Return without changing


X5-10 ¢ TECHNICIAN TIME CARD ENTRY RELEASE 2.3

### Entrance Screen

 

O From the Point of Sale Menu (X5), select option 10, Technician Time Card
Entry. You are prompted for a technician ID and date. During the session, you
can enter times for different technicians on any number of work orders. To
change technicians or dates, simply return to the entrance screen, illustrated
below.

         
 
 
 
    
   
 
  
 

A A&R EQUIPMENT SALES TIME CARD ENTRY X5B40-101

To change an Employee ID or date, you
must return to this screen.

Enter a Technician ID.. HAL

and a Date (mmddyy).... 061599

The information you enter during this session is lost to
Technician Time Card Entry after you press [Cmd1] to end
this job. Point of Sale is updated immediately each time
you press [Enter] on a detail line; therefore, the
information is available and can be changed on the work
order after you end this job.

¢mdl-End

  

C1 Type a valid employee address number. Since it doesn’t use profiles to record
employees’ rates, normal start/stop times, etc., Technician Time Card Entry
accepts employees and technicians. An employee is any system address in the
master file with an edit code of “E” in 3rd position and a technician has a “T”
in the 8th position. Just as in Time Clock, there is no index feature for
technicians’ IDs.

O  Fumish the date on which the work was done.
Press [Enter] to proceed to the detail screen.


POINT OF SALE X5-10 » TECHNICIAN TIME CARD ENTRY

DETAIL SCREEN

Standard Line Prompt

A A&R EQUIPMENT SALES TIME CARD ENTRY 06/16/1999 HAL HARPOLD X5B40-102
Ln W/O # o¢ =D-in sc Time Report Billed Rate or

Technician’s full name
is displayed.

Press [Cmd11] to bring up
the Options window.

Cmd3-Return Cmdl0-Totals cmdii“options Page Down Home
Enter a Line # to change, or press ENTER to add a new line.

Line # std Line Code
00

O Enter a labor standard line code or press [Enter] to add a new line. Standard
lines are set up in Standard Line Maintenance (X52-5).


 

X5-10 ¢ TECHNICIAN TIME CARD ENTRY RELEASE 2.3
New Line
A A&R EQUIPMENT SALES = TIME CARD ENTRY 06/16/1999 HAL BARPOLD xSB40~-103
Ln W/O # oc D-Ln sc Time Report Billed Rate TDI Comment

  
 

  

lf the Thermo King OPT
(X63B-6) is not on, the
Time Card detail screen
does not display job
code fields.

 
   
     
    
 

Cmd3-Retuzn Cmdid-Totals Cmdil-options cmd19-Delete Line
Ln W/o # D Addr Date oc P/O # Customer or Uni
oo

W/O Line SC Punch Start Stop

 

 

 

 

Report Billed Rate T D I/W Comment
o0000

 

 

To record a punch-in time:

In the field labeled W/O, type: IN and press [Enter]. After an “IN” punch,
subsequent punch times are considered punch-outs: the system will calculate
reported and billed hours from the previous punch time.

 

Co


POINT OF SALE X5-10 « TECHNICIAN TIME CARD ENTRY 7

 

Work Order Index

To look up a work order, place a few characters of its number in the field labeled
“Work Order” and press [Enter]. A list of open work orders is displayed, as
illustrated below.

  
     
   
   

 

 

TIME CARD ENTRY 06/16/1999 HAL HARPOLD X5B40-104
— R000101 0 BELLO1 SUSIE BELL
— 000103 0 000004 Pat Rose Constructi
— RooC104 Oo 090001 Carolynn Cain Const
Work
Order #
Cmd3-Return (no select} Page Down Home

     

 

O Place any character beside the work order you want. You do not need to press
[Enter]. The work order number will be placed on the detail line.


8 X5-10 ¢ TECHNICIAN TIME CARD ENTRY RELEASE 2.3
eee eS ES


Cmd11-Options

You can change the way the system rounds. In Point of Sale, you’re allowed only
2 decimals (hundredths); however, in Time Card, you can round time to whole
hours, or to the nearest tenth, quarter, or hundredth of an hour plus 10 min. (1), 30
min. (3), and 5 min. (5). It is not necessary to select the rounding method each
time—the method you select will remain as the default until you change it again.
If lines have already been entered when you change the rounding method, they
will not be re-edited and re-rounded until you bring them down to the detail line.

 

### Notice

DIS recommends that you select a rounding option before entering any lines and
stick with it. Although it’s possible to change the way rounding is done, even
mid-session, it is not a good idea. Changing rounding methods may confuse the
customers and make the resulting work orders and reports difficult to reconcile.

 

O To change rounding, press Cmd11-Options. The rounding options are
presented in the following window: (

Standard rounding or Start/stop time, enter in

always round Up (S/U)... Minutes or Decimal (M/D)...
Print time card (¥/N) os
Display options at startup (Y/N)... ¥

M

Quarters
Hundredths

10 min (1/6 hr)
30 min (1/2 hr)
5 min (1/12 hr}

cmd3-Return without changing

 

1 Select the options you prefer and press [Enter], or press [Cmd3] to return
without making any changes.


POINT OF SALE X5-10 ¢ TECHNICIAN TIME CARD ENTRY g

S=Standard, U=Up.

 

### Fields & Descriptions

Standard rounding or always round Up (S/U)
Round to
Whole WwW
Tenths T

 

Quarters C )
Hundredths H

 

10 min. (1/6 br)

 

30 min. (1/2 hr)

 

 

Start/stop time, enter in minutes/decimal (M/D)
Print time card (Y/N)
Display options at startup (Y/N)

 


5 min. (1/12 br)

 

M=Minutes, D=Decimal
Y=Yes, N=No

Y=Display options window
every time Technician Time
Card Entry is selected. N=Do
not display the options
window every time
Technician Time Card Entry
is selected. This setting can
be changed from the detail
screen by pressing Cmd1I-

Options.


X5-10 « TECHNICIAN TIME CARD ENTRY RELEASE 2.3

### Sample Time Card Entry

 

A A&R EQUIPMENT SALES TIME CARD ENTRY 06/16/2999 Carolynn Cain Co X5B40-102

 

 

Ln W/O # oc -D-Ln scprime Report( Billed] Rate TDI Comment

01 IN 08:00 N

02 ROOD104 Oo 0020 Tc]10:00 200 200 | 3995 A PREP MOTOR

03 ROO0103 0 0020 Tc/22: 280 280 | 3995 A TEAR DOWN

04 ROOO104 Oo 0030 TC}17:00 430 430 | 3995 A REPAIRS TO COMPR

 

 

 

a \

Punch time will not change after line is first entered.
When you change a line, watch the Billed column to
make sure entries are correct. Line can be deleted and
re-entered if you want “Time” column to be correct
(optional).

Cmd3-Return Cmdl0-Totals cmdll-Options Page Down Home
Enter a Line # to change, or press ENTER to add a new line.

Line # Std Line code
00

 

Since the purpose of Time Card is to record billable hours, you can use start/stop
times instead of punch-out times (you can mix punch-out times and start/stop
times).

On the first line, you can use a punch-in time by typing “IN” in the work order
field.

On the first line that is not a punch-in line, the following information is required:

- Work Order #

= Sales Code

= Start/Stop times. If this is the first line or the first line following a punch-in,
both start and stop times are required; otherwise, the system can calculate
from the previous stop time. Start/stop times are not allowed to span midnight
(24:00).

«Rate (Rate is not required if LABORJOB, Orton's custom code OPT, is on.

la


X5-10 ¢ TECHNICIAN TIME CARD ENTRY 1

### Fields On The Time Card Entry Screen

Across the top of the screen, the following fields are displayed:

La

W/O #

OC
D-Ln

sc
Time

Report
Billed
Rate
TDI

Comment

Line number. Lines are renumbered by time;
therefore, this line number may not have been the
original line number.

Work Order #. You can enter a portion of the work
order and press [Enter] to select from a list of open
work orders. Put any character beside the work
order you want. You do not need to press [Enter]:
the work order number will be placed on the detail
line automatically.

Status of the document: O=Open; R=Reopened.
Document Line #. Corresponding line on the work
order.

Sales Code.

Punch-out time. Same as Stop time for this line
unless the line has been changed. Punch time is one
of the keys to the record and does not change after
it is entered and displayed at the top of the screen.
Tf the line is brought down and changed, the original
Stop/Start times will be available and can be
changed. When the line is entered, the repor/billed
times will be changed (if appropriate), but the
“Time” field will remain the sarne throughout the
session. The best way to proceed is to watch the
“Billed” time. If this is too confusing, you can
always bring the line down, delete it, and re-enter it
with the correct start/stop times.

Hours reported.

Hours billed.

Hourly rate for this technician.
Tax/Discount/Billing codes. Billing codes are:
I=Internal, W=Warranty, N=Not Billed,
blank=same as work order.

Truncated version of the 30-character comment
field--only 7 characters can be displayed if the
Thermo King OPT is on because of the job code
field. This field is informational only. It will not be
carried over to the work order; however, it will be
printed on the time card if you select to print the
time card (Options screen).


12 X5-10 ¢ TECHNICIAN TIME CARD ENTRY RELEASE 2.3 C
_  eeeeaeaeSsSeo—_ eee eee _ sm ESE 209

At the bottom of the screen, the following fields, which are defined from left to

right, are displayed:
Ln

WO#

D
Addr
Date
oc

P/IO#
Customer or Unit

W/O Line
SC (Sales Code)

a Punch

Use either
Punch
time or
Start/Stop

or
Start

Next available line number for this session. Lines
are renumbered by time; therefore, this line may not
retain its number after it is entered.

8 characters. Work Order Number. Required.

To record a punch-in time of 8:00 A.M. (hard-coded,
cannot be changed), simply enter IN into this field
and press [Enter] (no further information is required
for a punch-in line); otherwise, enter an open work
order number. You can only post to open and
reopened work orders. The system reports closed,
voided, and canceled documents as not found.

No input. Division code.

No input. Customer address # from the work order.
No input. Date work order was opened.

No input. Status of work order. O=Open;
R=Reopened.

No input. Purchase order # from work order. (
No input. Customer name or Unit
Make/Model/Serial#.

No input. Next available line on the work order.

2 characters. Sales Code. Required. This must be a
labor sales code (format=L).

6 digits. Time (HHMMSS). The system does not
require leading or trailing zeros even though this
field will accommodate HHMMSS. If you enter
830, the system will assume you mean 083000.
After an “IN” punch, subsequent punch times are
considered punch-outs: the system will calculate
reported and billed hours from the previous punch
time. If a punch time is used after a start/stop time,
the system will calculate reported and billed hours
from the previous stop time.

4 digits. Time (HHMM). “Start time=0000” and

“Stop time=2400,” which makes a full 24-hours of

work time available. If technicians work past

midnight, enter the hours worked on the day they

started, then open new timecards for the day they

finished and enter the remaining hours. The system !
does not require leading or trailing zeros. If you X\


Stop

Report

Billed

Rate

YW

Comment

X5-10 « TECHNICIAN TIME CARD ENTRY 13

enter 830, the system will assume you mean 0830.
Start/stop times are not allowed to span midnight
(24:00).

4 digits. Time (HHMM). The system does not
require leading or trailing zeros. If you enter 830,
the system wili assume you mean 0830. If a start
time is omitted, the system calculates from the most
recent stop time. Start/stop times are not allowed to
span midnight (24:00).

5 digits. Number of hours reported. Two decimal
places are assumed. Hours are rounded according
the method selected in Cmd11-

5 digits. Number of billable hours. Two decimal
places are assumed. The billed hours are assumed to
be the same as reported hours, but they can be
changed.

5 digits. Two decimal places are assumed. The
hourly rate charged for this technician.

1 character. The customer’s tax code, which can be
changed here, will be used when you press [Enter].
Changes remain in effect for subsequent lines until
the code is changed again.

1 character. The customer’s discount code, which
can be changed here, will be used when you press
{Enier]. Changes remain in effect for subsequent
lines until the code is changed again.

1 character. Billing code. I=Internal, W=Warranty,
N=Not Billed, blank=same as work order.

30 characters. The comment field is truncated on
the top half of the screen. Only 7 characters can be
displayed when the Thermo King OPT is on
because of the job codes field.


14 X5-10 ¢ TECHNICIAN TIME CARD ENTRY RELEASE 2.3 a

OPTS RELATED TO TIME CARD

Menu X636D

Labor Analysis
Report

Menu X63B

Thermo King
Features

6. Only include closed/posted documents on report
7. Include open, reopen, and closed documents on report

5. Thermo King features in P.O.S. are not installed
6. Thermo King features in P.O.S. are installed


POINT OF SALE X5-10 ¢ TECHNICIAN TIME CARD ENTRY 15

### Time Card Entry Screen For Thermo King Dealers

In this section, only the aspects of the Time Card Entry screen that pertain to
Thermo King are discussed. Please read the previous sections to get a full
understanding of this screen, how it works, and the fields on it.

If the Thermo King OPT is on (X63B-6), the Time Card Entry screen displays job
code fields, as illustrated below.

 

A A&R EQUIPMENT SALES TIME CARD ENTRY 12/09/1997 HAL X5B40-103
Ln W/o # oc D-Ln sc Time Report Billed Rate TDI JobCd Comment

Job Code fields are present for all work orders if the TK Dealer
OPT is on. If TK Warr=T on the work order and /W=W on the
labor line, a job code is required.

Cmd3-Return Cmdl0-Totals Cmdli-Options cmd19-Delete Line
Ln w/o # D Addr Date oc P/O # Customer or Unit
00

W/O Line SC Punch Start Stop Jobed Job Code Description

 

 

Report Billed Rate T D I/W Comment

 

 

 

 

 

 

Technician Time Card Entry follows the same specifications and limits for

creating Thermo King warranty claims as in Point of Sale Invoicing, which are:

» One claim per work order

» Each claim can contain multiple segments (one segment only for a “Service
Parts Only Claim”)

» One cause of failure (COF) per segment

Up to 27 part lines per segment (one part line only for a “Service Parts Only

Claim”)

Up to 9 Misc. parts per claim

Up to 3 outside invoices per claim

Up to 10 comment lines per claim

Up to 18 serialized parts per claim

No labor lines on “Service Parts Only Claims”

vrvr y


X5-10 ¢ TECHNICIAN TIME CARD ENTRY. RELEASE 2.3

Note that the restriction of only 14 job codes per claim has been removed. You
may need to combine job codes on the work order because the restriction still
applies for Thermo Komm. Adjusting the job codes on the work order is also
necessary because Technician Time Card Entry will always assign the
maximum billable hours to a job code every time it is used; therefore, on the
work order, you may find the job has been over-billed.

The expectation is that you will be using job codes; therefore, you'll go into
“lookup” mode when you press [Enter] on the Time Card Entry screen. If TK
Warr=T on the work order and I/W=W on the labor line, a job code is
required.

To skip a job code, the following conditions must be true:
1) TK Warr=blank on the work order
2) No job code is entered

3) Billed hours are entered

Also, if you don’t want to use a job code, you can press F3=Exit after you enter
the series of Thermo King related screens.

  

Reminder
The "TK Warr" flag on the Sold To screen at Point of Sale cannot be changed if
there is a warranty line on the work order.

 

 

 


POINT OF SALE X5-10 « TECHNICIAN TIME CARD ENTRY 17

### Automatic Recovery

If Technician Time Card Entry is ended abnormally, the temporary files it uses
temain on the disk. To recover previously entered data, simply select the Time
Card option (X5-10) again.

Technical notes

When the Time Card option, X5-10, is selected, the following files are created
and used for the duration of the procedure instead of the standard files:
» wTCDws

> uTCSws
> uTCTws
> wuTCWws
(u=dealer’s file set, ws=S/36 workstation ID)


18 X5-10 e TECHNICIAN TIME CARD ENTRY RELEASE 2.3

Cc

Notes:

## CHAPTER X5-10

TECHNICIANS TIME CARD ENTRY

### Introduction

Technician Time Card Entry (TTCE) is a modified program from Time Clock
(Review by Technician). It requires no setup and retains no permanent
information other than what is recorded on the Point of Sale documents. Labor
lines added in TTCE update Point of Sale documents immediately, and lines can
be changed as long as you don’t end the job. The price for this is that there is no
provision for deleting a batch; rather, lines must be deleted individually. After the
job is ended, existing labor lines can be modified only on the work order. New
labor lines can be entered in Technician Time Card Entry or at Point of Sale. With
Time Clock, on the other hand, labor lines cannot be added at Point of Sale.

   
   
     

 

### Warning!

Technician Time Card Entry will always assign the maximum billable hours to
a job code every time it is used; therefore, on the work order, you may find the
job has been over-billed and will have to be adjusted.

Technician Time Card Entry has no reporting capability of its own, but the Labor
Analysis Report can be used to check technicians” hours. It is not connected with

Technician Time Card Entry and Time Clock are mutually exclusive; that is, if
Time Clock has been installed, Technicians Time Card Entry is not available and
vice versa.

If the Thermo King dealer OPT (X63B-6) is on, Thermo King job codes are
available and work the same as in Point of Sale. Because of its enhanced features
and reporting ability, Thermo King dealers are encouraged to use Time Clock
instead of Technician Time Card Entry.


2 X5-11 ¢ TIME CLOCK MENU

### Contents

### Time Clock Menu

 
   

Includes an option to print one Time Clock audit report at Accounting End of
Day

Protects integrity of reports by disabling labor lines at Point of Sale, but
provides access if necessary See CHAPTER X5.11-3, CONFIGURATION.
Provides access to Thermo King job codes just like in Point of Sale provided
the Thermo King dealer OPT (X63B-6) is on.

 

Point of Sale...
Thermo King Job Code!

 
 
  
  
 
 
 
 
 

 

PUNCh-OUL ......seeseesserereee
Review by Technician or Work Order...
Work Status Codes & Work Type Codes
Service Management.
Reports ..
History...

ARDAUNUUNA RD

TCLOCK User Profile...
oo


POINT OF SALE X5-10 « TECHNICIANS TIME CARD ENTRY 3
——— EE eS MI PARDO ENTRY OS

### Entrance Screen

O From the Point of Sale Menu (X5), select option 10, Technician Time Card
Entry. You are prompted for a technician ID and date. During the session, you
can enter times for different technicians on any number of work orders. To
change technicians or dates, simply return to the entrance screen, illustrated
below.

     
 
   
 
   
 
   
   

A A&R EQUIPMENT SALES TIME CARD ENTRY XSB40-101

To change an Employee ID or date, you
must return to this screen.

Enter a Technician ID.. HAL

ang a Date (mmddyy).... 120897

The information you enter during this session is lost to
Technician Time Card Entry after you press [Cmd1] to end
this job. Point of Sale is updated immediately each time
you press [Enter] on a detail line; therefore, the
information is available and can be changed on the work
order after you end this job.

  

 

C1 Type a valid employee address number. Since it doesn’t use profiles to record
employees’ rates, normal start/stop times, etc., Technician Time Card Entry
accepts any employee as a technician. An employee is any system address in
the master file with an “E” in 3rd position of Edit Code field. Just as in Time
Clock, there is no index feature for technicians’ IDs.

O Fumish the date on which the work was done.

O Press [Enter] to proceed to the detail screen.


4 X5-10 ¢ TECHNICIANS TIME CARD ENTRY RELEASE 2.2 —

### Time Card Detail Screen

A A&R EQUIPMENT SALES TIME CARD ENTRY 12/12/1997 HAL X5B40-203
in w/o # oC D-Ln SC Time Report Billed Rate ‘DB Comment

If the Thermo King OPT (X63B-6) is
not on, the Time Card Entry screen
does not display job code fields.

(md3-Return Cmdl0-Totals cmd11-Change Rounding Cmd19-Delete Line

in w/o # DB Addr Date OC P/O # Customer or Unit

00 (
W/O Line SC Punch start stop

Report Billed Rate T D Bill Comment

 

Cmd11-Change Rounding

As in the previous release of Technician Time Card Entry, you can change the
way the system rounds. In Point of Sale, you’re allowed only 2 decimals
(hundredths); however, in Time Card, you can round time to whole hours, or to
the nearest tenth, quarter, or hundredth of an hour (rounding options 1/2, 1/6, and
1/12 are no longer offered). It is not necessary to select the rounding method each
time—the method you select will remain as the default until you change it again.
If lines have already been entered when you change the rounding method, they
will not be re-edited and re-rounded until you bring them down to the detail line.

   
 

 
 

### Notice

DIS recommends that you select a rounding option before entering any lines and
stick with it. Although it’s possible to change the way rounding is done, even
mid-session, it is not a good idea. Changing rounding methods may confuse the
customers and make the resulting work orders and reports difficult to reconcile.


POINT OF SALE X5-10 + TECHNICIANS TIME CARD ENTRY 5
SS OEE ees ee

0 To change rounding, press Cmd11-Change Rounding. The rounding options
are presented in the following window:

 

Rounding... T whole
Tenths
Quarters
Hundredths

Cma3-Return without changing

 

1 Select the option you prefer and press [Enter], or press [Cmd3] to return
without changing the current option.


6 X5-10 « TECHNICIANS TIME CARD ENTRY RELEASE 2.2

### Sample Time Card Entry

 

A A&R EQUIPMENT SALES TIME CARD ENTRY 12/15/1997 HAL X5B40-102
Ln W/O # oc p-tn sf
o1 IN
02 R000108 Oo 0020 Tq
03 RO00108 0 0030 Tq
04 ROO0103 oO o0se tq

Rate TDB Comment
N
03850 A PREP MOTOR
03850 A TEAR DOWN
03850 A REPAIRS TO COMPR

Punch time will not change after line is ~

entered. When you change a line, watch the Billed
column to make sure entries are correct. Line can

 
     
  
 

be deleted and re-entered if you want “Time” Total Hours
column to be correct (optional). orted Billed
6.80 6.80

Cmd3-Return Cmdl0-Totals cm@li-Change Rounding Page Down Home

Enter a Line # to change, or press ENTER to add a new line.

Line #
00

 

 

This program can be used as a punch-out system (just like Time Clock); however,
its purpose is not to account for every minute of a technician’s time. The purpose
of Technician Time Card Entry is to record billable hours; therefore, you can use
start/stop times instead of punch-out times (you can mix punch-out times and
start/stop times).

Because there is no setup or configuration for this job (no stored values), all
relevant information is required on the first detail line. These values are then
stored in temporary files and used as defaults for subsequent lines and retrieved
when you need to change lines. When you press [Cmd1] to end the job, the
temporary files are deleted.


POINT OF SALE X5-10 » TECHNICIANS TIME CARD ENTRY. 7

 

On the first line that is not a punch-in line, the following information is required:

= Work Order #

= Sales Code

= Start/Stop times. If this is the first line or the first line following a punch-in,
both start and stop times are required; otherwise, the system can calculate
from the previous stop time. Start/stop times are not allowed to span midnight
(24:00).

= Rate (Rate is not required if LABORJOB, Orton's custom code OPT, is on.

a” & Cc
Ss Ea %
ce: %
BWR TS


8 X5-10 ¢ TECHNICIANS TIME CARD ENTRY RELEASE 2.2 os
TEASE, 2

### Fields On The Time Card Entry Screen

Across the top of the screen, the following fields are displayed:

La

W/O #
oc
D-Ln

sc
Time

Report
Billed
Rate
TDB
Comment

Line number. Lines are renumbered by time;
therefore, this line number may not have been the
original line number.

Work Order #.

Status of the document: O=Open; R=Reopened.
Document Line #. Corresponding line on the work
order.

Sales Code.

Punch-out time. Same as Stop time for this line
unless the line has been changed. Punch time is one
of the keys to the record and does not change after
it is entered and displayed at the top of the screen.
If the line is brought down and changed, the original
Stop/Start times will be available and can be
changed. When the line is entered, the report/billed
times will be changed (if appropriate), but the
“Time” field will remain the same throughout the {
session. The best way to proceed is to watch the
“Billed” time. If this is too confusing, you can
always bring the line down, delete it, and re-enter it
with the correct start/stop times.

Hours reported.

Hours billed.

Hourly rate for this technician.

Tax/Discount/Bill codes.

Truncated version of the 29-character comment
field--only 7 characters can be displayed if the
Thermo King OPT is on because of the job code
field.

At the bottom of the screen, the following fields, which are defined from left to

right, are displayed:
Ln

WO#

Next available line number for this session. Lines

are renumbered by time; therefore, this line may not

retain its number after it is entered.

8 characters. Work Order Number. Required.

To record a punch-in time of 8:00 A.M. (hard-coded,

cannot be changed), simply enter IN into this field

and press [Enter] (no further information is required \


X5-10 ¢ TECHNICIANS TIME CARD ENTRY 9

 

D
Addr
Date
oc
P/IO#
Customer or Unit
W/O Line
SC (Sales Code)
a Punch
Use either
Punch
time or
Start/Stop
or
Start
Stop

for a punch-in line); otherwise, enter an open work
order number. You can only post to open and
reopened work orders. The system reports closed,
voided, and canceled documents as not found.

No input. Division code.

No input. Customer address # from the work order.
No input. Date work order was opened.

No input. Status of work order. O=Open;
R=Reopened,

No input. Purchase order # from work order.

No input. Customer name or Unit
Make/Model/Serial#.

No input. Next available line on the work order.

2 characters. Sales Code. Required. This must be a
labor sales code (format=L).

6 digits. Time (HHMMSS). The system does not
require leading or trailing zeros even though this
field will accommodate HHMMSS. If you enter
830, the system will assume you mean 083000.
After an “IN” punch, subsequent punch times are
considered punch-outs: the system will calculate
reported and billed hours from the previous punch
time. If a punch time is used after a start/stop time,
the system will calculate reported and billed hours
from the previous stop time.

4 digits. Time (HHMM). “Start time=0000” and
“Stop time=2400,” which makes a full 24-hours of
work time available. If technicians work past
midnight, enter the hours worked on the day they
started, then open new timecards for the day they
finished and enter the remaining hours. The system
does not require leading or trailing zeros. If you
enter 830, the system will assume you mean 0830.
Start/stop times are not allowed to span midnight
(24:00).

4 digits. Time (HHMM). The system does not
require leading or trailing zeros. If you enter 830,
the system will assume you mean 0830. If a start
time is omitted, the system calculates from the most
recent stop time. Start/stop times are not allowed to
span midnight (24:00).


10 X5-10 ¢e TECHNICIANS TIME CARD ENTRY RELEASE 2.2
——e=rowuwuwHU“ a G S37 TW vkbe Oe EES 6

Report

Billed

Rate

Bill

Comment

5 digits. Number of hours reported. Two decimal
places are assumed. Hours are rounded according
the method selected in Cmd11-

5 digits. Number of billable hours. Two decimal
places are assumed. The billed hours are assumed to
be the same as reported hours, but they can be
changed.

5 digits. Two decimal places are assumed. The
hourly rate charged for this technician.

1 character. The customer’s tax code, which can be
changed here, will be used when you press [Enter].
Changes remain in effect for subsequent lines until
the code is changed again.

1 character. The customer’s discount code, which
can be changed here, will be used when you press
[Enter]. Changes remain in effect for subsequent
lines until the code is changed again.

1 character. Billing code. C=Customer, I=Intemal,
W=Warranty, blank=same as work order.

30 characters. The comment field is truncated on
the top half of the screen. Only 7 characters can be
displayed when the Thermo King OPT is on
because of the job codes field.


X5-10 ¢ TECHNICIANS TIME CARD ENTRY u

OPTS RELATEDTO TIME CARD

Menu X636D

Labor Analysis
Report

Menu X63B
Thermo King
Features

6. Only include closed/posted documents on report
7. Include open, reopen, and closed documents on report

5. Thermo King features in P.O.S. are not installed
6. Thermo King features in P.O.S. are installed


12 X5-10 « TECHNICIANS TIME CARD ENTRY RELEASE 2.2

### Time Card Entry Screen For Thermo King Dealers

In this section, only the aspects of the Time Card Entry screen that pertain to
Thermo King are discussed. Please read the previous sections to get a full
understanding of this screen, how it works, and the fields on it.

If the Thermo King OPT is on (X63B-6), the Time Card Entry screen displays job
code fields, as illustrated below.

 

A A&R EQUIPMENT SALES TIME CARD ENTRY 12/09/1997 HAL x5B40-103
Ln w/o # oc D-Ln SC Time Report Billed Rate TDB Jobcd Comment

Job Code fields are present for all work orders if the TK Dealer
OPT is on. If TK Warr=T on the work order and Bill=W on the
labor line, a job code is required.

Cmd3-Return Cmdl0-Totals Cmd19-Delete line

In W/O # DAddr Date OC P/O # Customer or Unit
00

W/O Line SC Punch Start Stop Jobtd Job Code Description

 

 

Report Billed Rate T D Bill Comment

 

 

 

 

 

 

Technician Time Card Entry follows the same specifications and limits for
creating Thermo King warranty claims as in Point of Sale Invoicing, which are:
> One claim per work order
» Each claim can contain multiple segments (one segment only for a “Service
Parts Only Claim”)
» One cause of failure (COF) per segment
> Upto 27 part lines per segment (one part line only for a “Service Parts Only
Claim”)
Up to 9 Misc. parts per claim
Up to 3 outside invoices per claim


POINT OF SALE X5-10 ¢ TECHNICIANS TIME CARD ENTRY 13
oor

> Upto 10 comment lines per claim
> Upto 18 serialized parts per claim
» No labor lines on “Service Parts Only Claims”

Note that the restriction of only 14 job codes per claim has been removed. You
may need to combine job codes on the work order because the restriction still
applies for Thermo Komm. Adjusting the job codes on the work order is also
necessary because Technician Time Card Entry will always assign the
maximum billable hours to a job code every time it is used; therefore, on the
work order, you may find the job has been over-billed.

The expectation is that you will be using job codes; therefore, you’ ll go into
“Jookup” mode when you press [Enter] on the Time Card Entry screen. If TK
Warr=T on the work order and Bill=W on the labor line, a job code is
required.

To skip a job code, the following conditions must be true:
1) TK Warr=blank on the work order
2) No job code is entered

3) Billed hours are entered

Also, if you don’t want to use a job code, you can press F3=Exit after you enter
the series of Thermo King related screens.

 

Reminder
The "TK Warr" flag on the Sold To screen at Point of Sale cannot be changed if
there is a warranty line on the work order.


X5-10 « TECHNICIANS TIME CARD ENTRY

Notes:

## CHAPTER X5-11

TIME CLOCK MENU
locke

Opr Xxpy | TMeLk-’91, |

Sct v0 TEL '
INTRODUCTION CC® PSO file,

Time Clock is a software solution for tracking time and billing charges. It is
available as an additional product, which can be purchased separately from DIS.
If the Thermo King dealer OPT (X63B-6) is on, Thermo King job codes are
available and work the same as in Point of Sale. Because of its enhanced features
and reporting ability, Thermo King dealers are encouraged to use Time Clock
instead of Technician Time Card Entry.

Time Clock is a punch-out system with full reporting capabilities. To make it easy
to upgrade, Technician Time Card Entry looks and feels like Time Clock’s
Review by Technician except that it does not use work type codes, status codes,
or technicians’ profiles. Technician Time Card Entry and Time Clock are
mutually exclusive; that is, if Time Clock has been installed, Technicians Time
Card Entry is not available and vice versa.

By simulating a time clock on the AS/400, it provides the following functions:

=  Validates and accumulates job information

= Keeps an unlimited amount of history making it easy to compare productivity
in Different years

= Requires minimal disk space: 5 MB per year for 10 technicians, each with 5
work orders and 4 miscellaneous punches, working 6 days/week

- Describes work by status codes and work type codes, both of which are
completely user-defined and can be tailored to your work environment

= Automatically charges overtime on selected work types (optional)

= Start/end of day can be customized for each technician's schedule

= Provides a "window" or grace period during which a punch is the same as the
start/end time of day

- Directly linked with Point of Sale Invoicing with command key that goes to
Review by Work Order

- Places billable labor lines on Point of Sale work orders when you press
[Enter] in Time Clock

= Allows management to review charges by technician/date or by work order

® Provides excellent management reports


2 X5-11 ¢ TIME CLOCK MENU RELEASE 2.2

- Includes an option to print one Time Clock audit report at Accounting End of
Day

= Protects integrity of reports by disabling labor lines at Point of Sale, but
provides access if necessary See CHAPTER X5.11-3, CONFIGURATION.

= Provides access to Thermo King job codes just like in Point of Sale provided
the Thermo King dealer OPT (X63B-6) is on.

### Contents

TIME CLOCK MENU

 
 
  
 

Point of Sale..
Thermo King Job Codes

 
 
 
 
 
 
 

Review by Technician or Work Order...
Work Status Codes & Work Type Codes
Service Management.
Reports


POINT OF SALE X5-11 ¢ TIME CLOCK MENU 3

 

TIME CLOCK MENU

 

COMMAND MENU: X5B WH
(c) DIS corp

 

» Time Clock

+ Table Maintenance

» Configuration
Review by Technician

+ Review by Work order

. Audit Reports

Aum we

23. Return to Point of Sale Menu

Ready for option number or command

 

seep

 

—_—__|

Technicians will log on with an AS/400 User ID, TCLOCK, which will take them
directly into Time Clock. They will not have access to any of the other setup,
reporting, or reviewing options that appear on the Time Clock Menu.

 

 

### Warning

An initial punch-in at the start of each day is Tequired. At least one punch-out is
expected before the next punch-in. After midnight, a new punch-in is tequired.


Time Clock is not connected to payroll in any way, nor are data accumulated by
‘Time Clock availabie to payroll jobs.


X5-11 » TIME CLOCK MENU RELEASE 2.2

Point of Sale

Billable Time Clock entries are placed directly on Point of Sale documents when
[Enter] is pressed in Time Clock, Review by Technician and by Work Order.

Because the integrity of Time Clock Reports will be compromised if labor lines
are entered through Point of Sale, they are disabled when Time Clock is installed.
From time-to-time, it may be necessary for someone to enter a labor line from
Point of Sale; therefore, a process has been provided whereby Point of Sale access
can be unlocked for one or more users. See POS Access Lock in CHAPTER
X5.11-3, CONFIGURATION.

 

### Warning

To ensure the accuracy of Time Clock reports, make sure all labor lines that are
entered at Point of Sale are duplicated in Time Clock. Better yet, don't use labor
lines at Point of Sale at all.

Thermo King Job Codes

Time Clock follows the same specifications and limits for creating Thermo King

warranty claims as in Point of Sale Invoicing, which are:

> One claim per work order

» Each claim can contain multiple segments (one segment only for a “Service
Parts Only Claim”)

» One cause of failure (COF) per segment

Up to 27 part lines per segment (one part line only for a “Service Parts Only

Claim”)

Up to 9 Misc. parts per claim

Up to 3 outside invoices per claim

Up to 10 comment lines per claim

Up to 18 serialized parts per claim

No labor lines on “Service Parts Only Claims”


yurveyr

Note that the restriction of only 14 job codes per claim has been removed.


POINT OF SALE X5-11 e TIME CLOCK MENU §

Command key option from Point of Sale

From the detail screen at Point of Sale Invoicing (X5-1), [Cmd14] takes the user
directly to the labor lines for that work order in Time Clock's Review by Work
Order option, where lines can be changed (for a more thorough discussion, see the
heading Review by Technician or Work Order). Pressing [Cmd1] returns to Point
of Sale.

Punch-out

Time Clock is a “punch out" system. After an employee "punches" in,
subsequent entries describe the activity (work, lunch, break, etc.) that has just
been completed. Time Clock automatically calculates the time that has elapsed
since the previous entry. In the review options, Time Clock will calculate the
punch-out time of day if the time reported is furnished, or hours reported if the
punch-out time of day is furnished.

Review by Technician or Work Order

Jn Review by Technician, new time data can be added to a technician's day ora
whole day can be entered; however, in Review by Work Order, labor lines cannot
be added or deleted--they can only be changed to billable or non-billable. Lines
can also be changed to internal or warranty provided there is an internal or
warranty address on the Sold To screen at point of sale.

Review by Technician is for a specified date. All punches made by the technician
for that date are displayed; therefore, the reviewer is working with consecutive
time periods for the technician's day.

By contrast, Review by Work Order shows all labor lines for all dates and all
technicians on a selected work order. Lines are displayed in the same order as
they appear on the point of sale detail screen. Additions, deletions, or changes to
time would affect the technician's time on other, unidentified work orders;
therefore, they are not allowed. Lines can be changed from billable to
non-billable, which deletes them from the work order, but does not delete the time
from the technician's day, and the lines can still be seen in Review by Technician.


6 X5-11 » TIME CLOCK MENU RELEASE 2.2

Work Status Codes & Work Type Codes

Technicians' work is described by work status codes, such as Break, Lunch,
Repair, Diagnostics, Waiting for Parts, Job Complete. It is further defined by
work type, such as Regular, Welding, etc. These codes are completely
user-defined and should be tailored to your work environment.

### Warning

Once work status codes and work type codes
have been set up and are in use, they should not
be changed, because to do so alters historical
data.

 

 

Overtime

Automatic overtime can be specified for any work type, such as Regular or

Welding. When this type of work is done outside of normal working hours, the

default start/end of day or the individual technician's start/end of day, the

technician's overtime rate is charged automatically. It is possible to designate a

"window" during which a punch is considered the same as the start/end of day. a
For example, you can specify a window of 10 minutes, which means that if the

normal start of day is 8:00 a.m., any punch from 7:50 to 8:10 would be the same

as 8:00 a.m. The window prevents many small overtime charges due to slight

variations in punch-in and punch-out times.

Service Management
Only the time and billing charges that are posted to work orders become part of
service history.

Reports
An audit report is printed at Accounting End of Day. In addition, audit

reports, which focus on technicians, work orders (same as the End of Day
Report), or date and time, can be requested at any time.

History

Time Clock entries accumulate indefinitely, but it requires minimal disk i


POINT OF SALE X5-11 * TIME CLOCK MENU 7

 

SETUP

space: 5 MB per year for 10 technicians, each with 5 work orders and 4
miscellaneous punches, working 6 days/week.

The following setup is required:

O1 Install the AS/400 software using Apply Enhancements (X6-9).

1 Set up a user profile: TCLOCK. This step involves signing on as QSECOFR,
so the appropriate password is required. This is explained later in this chapter.

O Configuration of default time clock values, including starting and ending

times for a typical day. Company configuration is required. The company

values are used unless a division is configured individually. See CHAPTER

X5.11-3, CONFIGURATION.

Table maintenance to furnish the following information:

Work type codes, such as REGULAR, WELDING, etc. and whether they get

overtime automatically.

Status codes for lunch, break, waiting for parts, etc.

Technician profiles, including their usual start/stop times, and rates charged in

each work type category. Any valid address number in the DIS Business

System can be used.

00 oa

See CHAPTER X5.11-2, TABLE MAINTENANCE.

TCLOCK User Profile

If you have only | file set, the user profile can be simply TCLOCK. If you have
more than 1 file set, you will need to create a user profile for each. You can use a
naming convention, such as TCLOCKu where « is the character associated with
your dealer files. Example: TCLOCKH for the H-files and TCLOCEM for the
M-files.

O Sign off.

CO Sign on as QSECOFR.

{J Ata menu, type: ertusrprf [Enter]. The Create User Profile screen
appears.


8 X5-11 « TIME CLOCK MENU RELEASE 2.2

 

Create User Profile (CRTUSRPRF)

Type choices, press Enter.

User profile. ........ . > telock Name
User password... ..... .  *USRPRF Name, *USRPRF, *NONE
Set password to expired . ... ‘*NO *NO, *YES
Status... ..-....-... + *BNABLED *ENABLED, *DISABLED
User class... ....... + > *PGMR *USER, *SYSOPR, *PGMR...
Assistance level... ..... *SYSVAL *SYSVAL, “BASIC, *INTERMED...
Current library > library Name, *CRTDFT
Initial program to call > x5b000c1 Name, *NONE

Library > library Name, *LIBL, *CURLIB
Initial menu > *signoff Name, *SIGNOFF

Library ...-..-.--- Name, *LIBL, *CURLIB
Limit capabilities ...... .|> *yes *NO, *PARTIAL, *YES
Text ‘description’... . . .°. > 'Time Clock’

Bottom

F3=Exit F4=Prompt FS5=Refresh F10=Additional parameters F12=Cancel
F13=How to use this display F24=More keys

 

 

 

O Complete the screen as illustrated above.
O) Press F10=Additional parameters.

\8T | THC AO |
eco _
TCLOckAD

| \p
Frases


Type choices, press Enter

Special authority

Special environment
Display sign-on information
Password expiration interval
Limit device sessions
Keyboard buffering .
Maximum allowed storage
Highest schedule priority
Job description

Library
Group profile
Owner

F3=Exit
F24=More keys

F4=Prompt,

 

O Complete the screen as illustrated above.

O Press [PgDn].

+ for more values

F5=Refresh

Additional Parameters

*usrels

*536
*SYSVAL
*SYSVAL
*SYSVAL
*SYSVAL
*NOMAX
3
adftjobd
*1ibl
*NONE
*USRPRF

F12=Cancel

X5-11 ¢ TIME CLOCK MENU 9

Create User Profile (CRTUSRPRF)

*USRCLS, *NONE, *ALLOBJ...

*SYSVAL, *NONE, *S36
*SYSVAL, *NO, *YES

1-366, *SYSVAL, *NOMAX
*SYSVAL, *YES, *NO

*SYSVAL, *NO, *TYPEAHEAD. ..
Kilobytes, *NOMAX

o-9

Name

Name, *LIBL, *CURLIB

Name, *NONE

*USRPRF, *GRPPRF

More...

F13=How to use this display


X5-11 « TIME CLOCK MENU

Create User Profile

Type choices, press Enter.

Group authority
Accounting code

Document password

Message queue
Library

Delivery .

Severity code filter -
Print device .
Output queue
Library
Attention program
Library
Sort sequence
Library
Language ID
Country ID .

*NONE
*BLANK
*NONE
tusrprt
*libl
*NOTIFY
°
*WRKSTN
*WRKSTN

*SYSVAL

*SYSVAL

*SYSVAL
*SYSVAL

(CRTUSRPRF)

*NONE,

Name,
Name,
Name,
*ALL, *CHANGE, *USE...

*NONE
*USRPRE
*LIBL, *CURLIB

*NOTIFY, *BREAK, *HOLD, *DFT

0-99

Name,
Name,
Name,
Name,
Name,
Name,
Name,

*WRKSTN, *SYSVAL
*WRKSTN, "DEV

*LIBL, *CURLIB

*NONE, *SYSVAL, *ASSIST
*LIBL, *CURLIB
*SYSVAL, *HEX

*LIBL, *CURLIB

*SYSVAL...
*SYSVAL...

More...
F3=Exit
F24=More keys

 

F4=Prompt Fl2=Cancel F13=How to use this display

 

O Complete the screen as illustrated above.
O Press [PgDn].


POINT OF SALE X5-11 « TIME CLOCK MENU a

 

Create User Profile (CRTUSRPRF)

Type choices, press Enter.

Coded character set ID... . . *SYSVAL *SYSVAL, *HEX...
User options... ..... -  *NONE *NONE, *CLKWD, *EXPERT...
+ for more values
Authority 2.2... 22... *ALL *ALL, *CHANGE, *USE, *EXCLUDE

Bottom
F3sExit Fé=Prompt FS=Refresh F12=Cancel F13=How to use this display
F24=More keys

 

 

 

O Complete the screen as illustrated above.
1 Press [Enter].
O Press F3=Exit.

Associating the User ID with the File Set

After the user profile has been created, it must be associated with the file set

(same as setting the environment).

O Ata menu, type: COPYDATA userid,,?CLOCK [Enter]. For userid use any
existing user ID on your system that is currently used to access the desired file
set.

1 If necessary, repeat this process for other file sets. As a shortcut, you can type:
WRKUSRPRF TCLOCKu and select TCLOCKu with 3=Copy.

O Sign off, then sign on as usual.


X5-11 « TIME CLOCK MENU
Notes:

co

## CHAPTER X5.11-1

TIME CLOCK

### Introduction

Technicians will use this option to punch in each day and throughout the day to
punch out as they change to a different activity, which may be work on a different
work order, lunch, etc. Time Clock automatically calculates the time that has
elapsed since the previous entry. If the Thermo King dealer OPT (X63B-6) is on,
Job code fields are included on the detail screen. Thermo King dealers are
encouraged to use Time Clock instead of Technician Time Card Entry.

### Contents

### How To Run

Technician Prompt..
Work Order & Customer/Unit# Prompts

 

  

PUNCHING IN...
After Midnight

 

 

PUNCHING OUT.........ccsssessessrees
Punching Out After Breaks Or Lun
Punching Out Before Breaks Or Lunch..
Punching Out To Change Jobs............

WORK ORDER INDEX.

SALES CODE & W/W FIELDS ......sccssscsssscssssessssssnesssensesssssneesnersneseatersesaneene 7

STATUS PROMPT.

  
 
 

 

 

 

FIELD PROMPT..........::csssssssssesnescnsssvessssessessossseessesssecusesseesstsasesseceeseeenesss 11


X5.11-1 « TIME CLOCK RELEASE 2.2

THERMO KING JOB CODES.

  
  

Multiple Punches to the Same Job Code 14
Multiple Job Codes wees 15
Multiple Job Codes with Overtime. 17
Miscellaneous Job Codes ........:scccsssessessecsseesssesssesseesseeanseateeseesnecanssnscanecsaeennsesces 18
TIME PROMPT .......s:s:ccssessncensssesessrarensteersseensassesoranensosstees soaenenenensyenenenees 19

VERIFICATION... .ccsssessessrsscessnssnerseessseturorersaessesrscssnsanatarsusenarssnensansssnressees 20


POINT OF SALE X5.11-1 « TIME CLOCK 3
ee SSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSeseSeesesessssSESA ET ME SIR

### How To Run

O From the Time Clock Menu (X5-11), select option 1, Time Clock. The
technician prompt is displayed.

Technician Prompt

A NW EQUIPMENT SALES 3/31/98  X5B10-101

Technician:

 

cmdl-End

 

Only address numbers that have been entered in the Technician Table (option ! in
Table Maintenance) are valid at this prompt.

It is not necessary to press [Enter] after typing a valid technician ID. The timeout
period entered in Configuration applies to the time it takes to type a valid ID
when signed on as User ID TCLOCK.


4 X5.11-1 » TIME CLOCK RELEASE 2.2

Work Order & Customer/Unit# Prompts

A NW EQUIPMENT SALES TIME CLOCK 3/31/98 X5B10-102
Technician: BONNIE BONNIE PEMBERTON
Use customer
Work Order: Cust /Unit #: << .
on Orese meromensens address# or unit# to
narrow the search for
work orders.

Use partial work
order number to
select from a list
of work orders.

 

cmdi-cancel Cmd3-Return to Technician

 

 

 

### "Warning

An initial punch-in at the start of each day is required. At least one punch-out is
expected before the next punch-in. After midnight, a new punch-in is required.

 

 

### Punching In

When a technician arrives, their first action is to punch in by typing IN at the
Work Order prompt. For User ID TCLOCK, a verification message follows. For
other User IDs, a time prompt, which defaults to the current system time, is
presented before the verification message.


POINT OF SALE X5.11-1 ¢ TIME CLOCK 5

After punching IN, a technician is expected to punch out at least once before
another punch-in will be accepted. After midnight, a new punch-in is required.
See below.

After Midnight

If technicians work past midnight, they need to punch out before midnight or ask
management to make a correction on the following day.

Technicians will not be allowed to punch out after midnight without first
punching IN for the new day.

PUNCHING OUT

Punching Out After Breaks Or Lunch

When technicians return from breaks or lunch, they do not use a work order
number or unit number. They should simply press [Enter] at this prompt and to
proceed to the next prompts to record the break or lunch time, which has just been
completed.

y% Punching Out Before Breaks Or Lunch

When technicians stop working to go on breaks or to lunch, they will use a work
order number or unit number. After entering the work order or unit number for the
job they have been working on, they press [Enter] to proceed to the next prompts
to record the type of work they have been doing. Work orders can be selected
from the Work Order Index, which is described below.

Punching Out To Change Jobs

When technicians go from one job to the next, they enter the work order or unit
number for the job that has just been completed. Work orders can be selected
from the Work Order Index, which is described below.


6 X5.11-1 ¢ TIME CLOCK RELEASE 2.2

 

### Work Order Index

Enter a partial work order number, press [Enter], then select from a list of current
work orders. [Page Down] and [Home] enable you to page through the work
orders looking for the one you want. You can enter a customer address number or
a unit number to narrow the search. A work order is selected by placing any
character beside it. If only one document matches the request, it is assumed to be
the one you want.

 

A NW EQUIPMENT SALES TIME CLOCK 3/31/98  X5B10-103
Technician: BONNIE BONNIE PEMBERTON
Work order: Customer/Unit #:
— W042043 0 FORD 8830 26833 WARRANTY-NEW ROLLAN
— Wo42044 oO FORD 8830 G08280 WALTER OR MASEL GRO
— W042117_ 0 WHITE 6124 625058 W2684d WARRANTY-AGCO
— wo4q2944 0 #32 SKNR 529 1PTFZ1THXKS0 M15228 MCFARLANE MFG, MOTO
— 4043026 0 WHITE 6125 622307 W26844 WARRANTY-AGCO
— WO43045 0 KNOWLES RUNNING GEAR HO8980 HATZ FARMS, INC. (
— Wo43291 0 #17 PRAILER M15228 MCFARLANE MFG. MOTO
— W043770 0 FORD 8340 G07907 GOLDEN VALLEY FARMS
— wo44204 0 N.HOLLAND L785 CASHS THANK YOU
— 4044219 0 CASHS THANK YOU
— wo44225 0 NH Lx885 W26833 WARRANTY-NEW HOLLAN
~ woda318 0 FORD 8830 CASHS THANK YOU
— W044325 oO FORD 8830 926279 CASHS THANK YOU
— WO44396 0 W30225 W.C.C. FLATS
— W044575 0 WHITE 6195 682017 W26844 WARRANTY-AGCO
— Wo44a95 0 WHITE, 2-110 302153 M15232 MCFARLANE CO. WARRA

emdl-Cancel cmd3~-Return to Technician Page Down Home


POINT OF SALE X5.11-1 « TIME CLOCK 7
SEE EE

SALES CODE & I/W FIELDS

These fields take their default values from Configuration (X5.11-3). Both fields
can be changed on the Time Clock screen. The rules governing the sales code and
YW field are summarized in the 3 tables below. For further clarification, see the
text that follows.

Step
Document opened to customer:
Int/Warr=Blank
Int/Warr=1

1: How the Default Sales Code is Determined in Time Clock

Step 2: How the Default I/W Field is Determined in Time Clock

    
 
 
 

 

   
 
 

 
    
 
 
  

  

  

Document opened to unit

 

 

 

 

If "Default for war docs" is: YW in Time Clock is:
Blank Blank
Ww W (Warranty Addr# required on POS doc.)

 

Step 3: How the Billing Code Affects the I/W field

 

 

 

 

 

 

 

If status code's billing code (Bill) is: | /W. changes to:

Y No change

N No change

I I dnternal Addr# required on POS doc.)

Ww. W (Warranty Addr# required on POS doc.)

 

 

= Sales Code. If, in the customer's master record, the Int/War field is blank, the
customer sales code default is used; if "I," the internal sales code default is
used; if "W,” the warranty sales code default is used. For customer addresses
that are Internal or Warranty (Int/Warr="I" or "W" in Receivables
Maintenance (X1 1-2), the YW field may be blank, in which case
corresponding addresses are not required on the Point of Sale document.
Individual lines are not marked "I" or "W" on the document; therefore,
separate Internal and Warranty documents are not generated.

= I/W field. If “Default for lines on war docs" is blank, the I/W field on the
Time Clock screen will be blank; if it is "W," the I/W field on the Time Clock
screen will be "W." Any time the //W field is "I" or "W," the corresponding
address numbers must be present on the Sold To screen of the Point of Sale
document.

= Changing. Both fields can be changed on the Time Clock screen.


8 X5.11-1 © TIME CLOCK RELEASE 2.2

- Status Code Billing. If a status code with a billing code of "I" or "W" is
selected, the I/W flag will be changed to match it automatically, and the
corresponding Internal or Warranty address is required to be on the Point of
Sale document (Sold To screen). Labor lines will be entered as "I" and "W”
lines on the document.

= Document Opened to a Unit. The default internal sales code from Time
Clock Configuration is used.

= Document Opened to Internal or Warranty Customer. If the customer is a
warranty or internal customer (Int/War field on the customer's master record.
in Receivables Maintenance has a value of "I" or "W"), system addresses are
not required on the Sold To screen unless the I/W field in Time Clock is set to
'T" or "W."

= Thermo King Warranty Documents. Even if the Point of Sale document is a
Thermo King warranty document, which is indicated by setting the TK field
on the Sold To screen to "I", system addresses are required on the Sold To
screen in order to mark lines as internal or warranty.

See also, CHAPTER XS.11-3, CONFIGURATION.


POINT OF SALE X5.11-1 « TIME CLOCK 9
SE a

 

STATUS PROMPT
A NW EQUIPMENT SALES TIME CLOCK 3/31/98 X5B10-104
Technician: BONNIE BONNIE PERMBERTON
Work Order: wo43770 Customer: G07907 GOLDEN VALLEY FARMS, LLC
Sales Code: 40 I/wW: unit: FORD 8340
Status:
Status Codes W/O Bill Status Codes W/O Bill
10 PRELIMINARY DETERMINATION ¥ Y 35 ASSIST 5 YoY
12 PRELIM 2 YoY 40 WORK COMPLETE Yoy
13 PRELIM 3 Yow 50 TEST yoy
14 PRELIM 4 yor 52 TESTING AGAIN yoy
20 WAITING FOR PARTS/INFO N oN 54 TESTING AGAIN AND AGAIN ¥ ¥
22 WAITING 2 YoY 55 COURT N oN
23 WAITING 3 yow S6 TESTING UNTIL IT WORKS yoy
24 WAITING 4 yor 58 TESTING, WHAT ELSE TO DO? Y ¥
30 ASSISTANCE YoY 60 RESEARCH NON
32 ASSIST 2 y ¥ 70 LUNCH N oN
33 ASSIST 3 Y Ww 71 LUNCH 1 yoy
34 ASSIST 4 yo. 72 LUNCH 2 y o¥
More...
Cmdl-Cancei © Cmd3-Return to Work Order Page Up Page Down Home

 

 

re

Status codes are set up in Table Maintenance. [Page Down], [Page Up], and
[Home] enable you to page through status codes, as illustrated above. From the
list, type a 2-digit status code. If it is a billable code, a type of work prompt
follows; otherwise, the time prompt is presented next.

Status Code Billing. If a status code with a billing code of "I" or "W" is selected,
the I/W flag will be changed to match it automatically, and the corresponding
Internal or Warranty address is required to be on the Point of Sale document (Sold
To screen). Labor lines will be entered as "I" and “W" lines on the document.


10 X5.11-1 * TIME CLOCK RELEASE 2.2

TYPE OF WORK PROMPT

A NW EQUIPMENT SALES TIME CLOCK 3/31/98  X5B10-105

Technician: BONNIE BONNIE PEMBERTON

Work Order: W045295 Customer: PARKOL AUSTIN PARKER
Sales Code: 40 I/W: Unit:

Status: 32 ASSIST 2

Type of Work:
Work Type Codes Overtime?
0 STANDARD ¥
1 SHOP N
2 CLEAN/PAINT ¥

Cmdi-Cancel Cmd3-Return to Work Order

 

Work type codes and descriptions are set up in Table Maintenance. From the list,
type a 1-digit work type code. The field prompt follows.


POINT OF SALE X5.11-1 « TIME CLOCK VW
oS EME EUR

FIELD PROMPT

 
       
   
   
   
   
  
 

A NW EQUIPMENT SALES

 

TIME CLOCK 3/31/98 = X5B10-106

Technician: BONNIE BONNIE PEMBERTON
Work Order: W045235 Customer: PARKOi AUSTIN PARKER
Sales Code: 40 I/W: Unit:
Status: 32 ASSIST 2
Type of Work: 0 STANDARD

Field? (¥ or N): N

  

 

   
 

 

Cmdi-Cancel

   

Cmd3-Return to Work Order

The field prompt refers to whether the work was done in the field and is billable at
field rates as opposed to in-house regular charges. The field accepts only Y=Yes
or N=No (default). If Field=Yes, billing is calculated using the per hour Fieid
Rate entered in the Technician Table (Table Maintenance). The punch-out time
prompt follows. If the punch-out time indicates that overtime is appropriate, the
field rate is used. Field rates override overtime rates.


12 X5.11-1 « TIME CLOCK

### Thermo King Job Codes

If the Thermo King OPT (X63B-6) is on, the following sequence of screens is
presented. If it is not on, these screens are omitted and the time prompt is

displayed.

 

 

 

### Warning

Job codes can be used on non-warranty lines. This is true regardless of whether
TK War=T or not. If you suspect that a job code has not been processed correctly,
make sure the line is a warranty line or that TK Warr=T on the work order.

 

 

A NW EQUIPMENT SALES

Technician: BONNIE

Work Order: WO45295

Sales Code: 40 I/w:

Status: 32

Type of Work: 0

Field? (Y¥ or N): N

Job Code/Desc.:

TIME CLOCK 3/31/98 = XSB10-111

BONNIE PEMBERTON

Customer: PARKO2 AUSTIN PARKER
unit:

ASSIST 2

STANDARD

cmdél-Cancei Cmd3-Return to Work Order

 

O Enter a job code on the first line and press [Enter]. The job code is processed.
If it is not valid, you are taken through the same series of Thermo King
screens relating to job codes as in Point of Sale, beginning with Select
Group/Category, then Job Codes. If it is a valid Thermo King Job Code, its
description is returned to this screen, and the time prompt is displayed. See

page 19.


POINT OF SALE X5.11-1 » TIME CLOCK 13
———— SN eee

THERMO KING JOB CODES XTEQOP-02
Select Group/Category

Model: 062 AMD
isSelect Serial#:

Opt — Group/Category

_ ENGINE - FUEL

_ ENGINE - COOLING

~ ENGINE - EXHAUST

= ENGINE - INTAKE

- ENGINE - CYLINDER HEAD

- ENGINE - LUBRICATION

- ENGINE - BLOCK
ENGINE - MISC. OPERATION
COMPRESSOR - INTERNAL
COMPRESSOR - EXTERNAL
COMPRESSOR - MISC. OPERATION
ELECTRICAL - STARTER
ELECTRICAL - THERMOSTAT
ELECTRICAL ~ CHARGING
ELECTRICAL - CONTROL

F3=Exit Fl2=Return to Model Selection Roli

 

O1 Select a Group/Category with 1=Select, and press [Enter]. The Job Code
screen is displayed.


14 X5.11-4 » TIME CLOCK RELEASE 2.2

 

THERMO KING JOB CODES X7E90P-03
Select Job Code

Grp/Cat: REFRIGERATION - MISC. OPERATION
Model: 062 AMD
i=select Serial#:

Opt Job Code Description
2 04000 RECVY-LEAK CHK-EVAC-CHG (R&R
- 04002 RECVRY-REPAIR-L CHA-DRIER-EVA
04002 ‘LOW CHG-LEAK CHK-ADD CHG
04003 INCORRECT CHG-RECOVERY-EVAC-R
04009 RECVRY-LBAK CHK-EVAC-CHG (NO
04010 RECVRY-L CHK RPR-EVAC-CHG (NO
04040 CLEANUP PROCED. #1
o4cal CLEANUP PROCED. #2
04042 CLEANUP PROCED. #3
06999 MISC LABOR

F3=Exit  F12=Return to Group/Category Selection Roll

 

© Select a job code with 1=Select and press [Enter]. The job code is returned to
the Time Clock screen.

O) Press [Enter]. The Punching OUT time is displayed.

O Press [Enter]. The confirmation message is displayed.

C1) Press any key to return to the Technician prompt.

 

NOTE
Depending on the situation, there may be other screens where you are asked to
make selections relating to Thermo King jobs. No attempt has been made to
illustrate all Thermo King screens.

 

Multiple Punches to the Same Job Code

Thermo King’s flat rate is intended to apply to the entire work order, regardless of
how many times it is necessary to use the same job code when the work is done
over several days. For each new entry, Time Clock searches the work order for
other occurrences of the same job code. Then the billed hours of each line are
adjusted so the total billed hours exactly equal the flat rate for the job code. The


POINT OF SALE X5.11-1 © TIME CLOCK 18

calculation uses each line’s reported hours and assigns billed hours based on its
percentage of total reported hours.

Multiple Job Codes

Sometimes job codes cover very small tasks, and it is inefficient to punch out for
each one; for example, a task may actually be made up of several individual steps,
each with its own job code, but it is impossible to separate them into their own
time segments. In this case, Time Clock Entry (X5.11-1) allows up to 5 job codes
per punch.

There is no way for Time Clock to “know” how many job codes you want to
combine; therefore, it is necessary to “reserve” the lines. To indicate that there
will be 5 job codes, enter a character on each line, as illustrated below.

A NW EQUIPMENT SALES TIME CLOCK 3/31/98  XSBi0-111
Technician: BONNIE BONNIE PEMBERTON
Work Order: w045286 Customer: BURKO1 © RICHARD BURKIN
Sales Code: 40 I/W: W Unit: TK 2001 4S6PHA098745
Status: 50 TEST Non-standard job codes are
allowed on non-warranty
Type of Work: 0 STANDARD lines (/W=blank or “I."

Field? (¥ or N): N

Job Code/Desc.: ARAAA

2.

——_» 2

06051__

The characters that reserve lines for job codes
do not have to be uniaue.

 

 

 

€md1-Cancel Cmd3-Return to Work Order

 

 

When you press [Enter], the program will loop through 5 times to allow you to
select 5 unique Thermo King job codes for these lines. You will see a box that
displays the line number and job code being processed.


16 X5.11-1 « TIME CLOCK RELEASE 2.2

 

Processing Job Code

Line number Job code

 

Watch this box to know which job code is being
edited. Valid job codes are accepted. Invalid job
codes lead you to the Thermo King determination
screens to select a valid job code.

 

 

When the system encounters an invalid job code, it will proceed to the Thermo
King Job Codes screen. If you press F3=Exit on one of the Thermo King Job
Code screens, you will return to the list of "Job Code/Desc." Press [Enter] again
to resume. The system will re-edit each non-blank line beginning with line 1.

~~


POINT OF SALE X5.11-1 ¢ TIME CLOCK 7
——— EEE LOUK

A NW EQUIPMENT SALES TIME CLOCK 3/31/98  X5B10-107
Technician: BONNIE BONNIE PEMBERTON
Work Order: WO045287 Customer: BURKO1 RICHARD BURKIN
Sales Code: 40 I/w: Unit:
Status: 50 TEST
Type of Work: 0 STANDARD

Field? (¥ or N): N

Job Code/Dese.: 02036 R&R FRONT SEAL (INCL R&R) 50
05039 R&R T-STAT/THERMOMETER RELAY
06028 ADJUST BELTS
06051 R&R EVAP FAN BLADES ALL
04004 R&R DRIER

Punching OUT at 13 : 31:55 on 12/15 / 1997

Cmdl-Cancel Cmd3-Return to Work Order

 

 

After the punch-out process is complete, Time Clock must assign hours reported
to each job code. The assumption is that the job code with the largest number of
billed hours should have the largest number of reported hours. The flat rates of all
job codes are added and each job code is assigned a percentage based on the total
elapsed time. Then Time Clock checks the work order. If it finds the same job
codes already on the work order, billed hours are adjusted so the total billed hours
exactly equal the flat rate for the job code. The calculation uses each line’s
reported hours and assigns billed hours based on its percentage of total reported
hours.

Muitiple Job Codes with Overtime

When a technician punches out using multiple job codes after the end of their
normal day, Time Clock records regular time first, then uses overtime on the last
job code. Billed hours are allocated as described in the previous section, Multiple
Job Codes.

 

 

NOTE


18 X5.11-1 ¢ TIME CLOCK RELEASE 2.2
SSE AE Ee

 

Since the last job code may not always be the best one to use for overtime, the
service manager should be alert to the possibility that adjustments need to be
made for this situation.

 

Miscellaneous Job Codes

If a miscellaneous job code is selected (last 3 digits are 999), a window will pop
up, which allows you to enter a description and a rate.

THERMO KING JOB CODES X7ESOP-03
Select Job Code
Grp/Cat: ENGINE - MISC. OPERATION
Model:

1sSelect Serial#:

Opt Job Code Description
1 o1999 MISC LABOR

gobCode: 01999 Desc

JEnter desired Description and/or Flat Rate (nnn.n} and press ENTER.

Miscellaneous Job Codes on Point of Sale Document. Since miscellaneous job
codes do not have a flat rate, Time Clock does not search for the occurrence of the
same miscellaneous job codes on the same work order or attempt to combine
them or prorate their billed times.

Miscellaneous Job Codes Included in Punch Out. If a miscellaneous job code is
included in a punch out along with other job codes, their reported times are
determined as described in the previous section.


POINT OF SALE X5.11-1 ¢ TIME CLOCK 19

 

### Time Prompt

A NW EQUIPMENT SALES TIME CLOCK 3/31/98 = XSBL0~107
Technician: BONNIE BONNIE PEMBERTON
Work Order: wo45295 Customer: PARKO1 AUSTIN PARKER
Sales Code: 40 I/W: unit:
Status: 32 ASSIST 2
Type of Work: 0 STANDARD

Field? (¥ or N): N

Job Code/Desc-: 04000 RECVY-LEAK CHK-EVAC-CHG (R&R

Punching OUP at 09 : 25 : 41 on 063 / 31 / 1998

 

Cmdl-Cancel cmd3-Return to Work Order

 

1 Press [Enter].

The time/date stamp is displayed for User ID TCLOCK but no input

is allowed. Other users receive a prompt where the current system time
(hhmmss) and date (mmddyyyy) are used as defaults. Enter the time and/or date,
if different. Military time is used: enter 5:15 P.M. as 171500.


20 X5.11-1 ¢ TIME CLOCK RELEASE 2.2
VERIFICATION
A NW EQUIPMENT SALES TIME CLOCK 3/31/98 -X5B10-108
Technician: BONNIE BONNIE PEMBERTON
Work Order: wW045295 Customer: PARKO] © AUSTIN PARKER
Sales Code: 40 I/w: unit:
Status: 32 ASSIST 2
Type of Work: 0 STANDARD
Field? (¥ or N): N
Job Code/Desc.: 04000 RECVY-LEAK CHK-EVAC-CHG (R&R
Punching OUT at 09:25:41 on 03/31/1998 (

md1-Cancel

Press any key to complete *

cmé3-Return to Work Order

 

O The verification message requires any keystroke to continue. If the
information on screen is correct, press any key; otherwise, press [Cmd3] to
return to the work order prompt or [Cmd1] to cancel this entry and return to
the technician prompt.

NL

## CHAPTER X5.11-2

TABLE MAINTENANCE

### Introduction

Use this job to set up the following information for Time Clock:

= Work type codes, such as REGULAR, WELDING, etc. and whether they get
overtime automatically.

= Status codes, such as lunch, break, waiting for parts, etc.

= Technician profiles, including their usual start/stop times, and rates charged in
each work type category. Any valid address number in the DIS Business
System can be used.

### Warning

Once work type codes and status codes have been set up and are in use, they
should not be changed, because to do so alters historical data.

 

### Contents

INTRODUCTION..

 

### How To Run

Work Type Codes
Status Codes........
Print Tables

 

 
 
 

YARN


2 X5.11-2 « TABLE MAINTENANCE RELEASE 2.2
ee SeSSeSeSSSSSSSSSSSSSeeeeSeseSSESEEIRASE

### How To Run

From the Time Clock Menu (X5-11), select option 2, Table Maintenance. The
following options are displayed:

A NW EQUIPMENT SALES TC Table Maintenance X5B20-101

i. Technician Table
2. Status Codes
3. Work Type Codes

Select a Table: _

For setup, the options are taken in reverse order

Cmdi-End cmd$-Print Tables

 

 

la


POINT OF SALE X5.11-2 © TABLE MAINTENANCE 3

 

Work Type Codes
O From the TC Table Maintenance entrance screen, select option 3, Work Type
Codes Screen.
Work Type Codes Screen
A NW EQUIPMENT SALES TC Table Maintenance X5B20-106
Work Type Codes
Automatic
Code Description Overtime
Q REGULAR ¥
i STEAM CLEANING N
2 WELDING N
3 PAINTING N
4
5
6
7
8
9
Cmd3-Return

 

 

 

 

    
 
 

### Warning

Once work type codes have been set up and are in use, they should not be
changed, because to do so alters historical data.

 
    

Each punch-out will prompt technicians for a work type. In the Technician Table,
each work type is associated with regular, overtime, and field labor rates for each
individual technician.

Code 1-character code that will be associated with the type of
work described on this line.
Description 25 characters.

Automatic Overtime Y/N. "Yes" means that the technician's overtime rate is
automatically billed if the hours are outside the technician's


X5.11-2 © TABLE MAINTENANCE RELEASE 2.2

co

normal starting and ending times for the day (with
allowance for window, if any). "No" means that the
technician's regular rate will be used. Rate changes can be
made in Review by Technician or Work Order.

Status Codes

O From the TC Table Maintenance entrance screen, select option 2, Status
Codes.

Status Codes Screen

 

S MCGILL MANUFACTURING TC Table Maintenance XSB20~105
Status Codes
Code Description : W/O Required Billable
10 PRELIMINARY DETERMINATION ¥ ¥
12 PRELIM 2 Y ¥
13 PRELIM 3 Y w Up to 99
1a PRELIM 4 x Z status codes
20 WAITING FOR PARTS/INFO N N can be used (
22 WAITING 2 Y ¥
23 WAITING 3 ¥ w
24 WAITING 4 x I
30 ASSISTANCE ¥ ¥
32 ASSIST 2 Y ¥
33 ASSIST 3 Y W
34 ASSIST 4 ¥ I
35 ASSIST 5 Y Y
40 WORK COMPLETE Y ¥
50 TEST ¥ ¥
52 TESTING AGAIN ¥ x

 

cma3-Return Page Down Page Up Home (& Sort}

    

### Warning

Once status codes have been set up and are in use, they should not be changed,
because to do so alters historical data.

 

Here's how it works. If you add a new code or change an existing one, press

[Enter] to record what you've done. If the screen is full (16 codes), the next screen

is displayed; otherwise, the same screen is displayed. You can press [Page Up]

and [Page Down] to look at the next or previous screen. Pressing [Home] takes .


X5.11-2 * TABLE MAINTENANCE 5

 

you to the top of the list and sorts the codes in numerical order. The maximum
number of status codes is 99.

The codes, descriptions, and other information displayed on this screen will also
be displayed at the prompt for a status code during time clock entry.

Cd
Description
W/O Req.

Bill

2-digit code.

25 characters.

Work Order Required. Y=Yes, N=No. If W/O Req.=Y, a
work order is required. Whether a work order is required
depends on your own policies and how you want to track
technicians’ time. A work order is required for all billable
codes. A work order may not be required for lunch or
breaks. A work order may be required for non-billable time
for a status such as Waiting for Parts.

"Y" (Yes), "N" (No), "I" (internal), and "W" (Warranty). If
Bill=N, a work order is not required. For any other code, a
work order is required and time with this status code will
be charged to it. A billing code of "I" uses the default
Internal sales code from Time Clock Configuration; "W"
uses the default Warranty sales code. In addition, the IW
flag on the Time Clock screen is changed automatically to
"I" or “W," which means that the corresponding Internal or
Warranty addresses are required on the Point of Sale
document (Sold To screen).


X5.11-2 ¢ TABLE MAINTENANCE RELEASE 2.2

Technician Table Screen

A NW EQUIPMENT SALES & TC Table Maintenance X5B20-104
Technician Table

Technician ++. BONNIE BONNIE PEMBERTON

Start of Day (hhmmss).. 063000
End of Day (hhmmss).... 153000

Regular Overtime Field
Work Type Labor Rate Labor Rate Labor Rate
REGULAR 03750 05625 07500
STEAM CLEANING 4100 4100 6200
WELDING 4800 7200 8500
PAINTING 00900 0000 90000
ce000 00000 o9000
06000 00000 09000
00000 00000 99000
o¢o00 00000 00000
oco00 09000 00000
oco00 90000 00000

cmd3-Return

 

Any valid DIS address can be entered in the technician table. Only addresses
entered in this table will be valid in Time Clock. The rates entered for each type
of work are used to calculate billing charges for work orders. Overtime should be
entered as a dollar amount, not a percentage.

Start of Day (hhmmss) Normal starting time for this technician. For
automatic overtime work types, overtime is charged
for hours outside of the start time except for
window allowed in Configuration.

End of Day (hhmmss) Normal ending time for this technician. For
automatic overtime work types, overtime is charged
for hours outside of the end time except for window
allowed in Configuration.

Work Type Work type codes and their descriptions are entered
in Work Type Codes (Table Maintenance).
Regular Labor Rate The per hour charge billed for this work type for

this technician during regular hours. Enter $37.50 as
3750 and press [Field Exit}.


POINT OF SALE X5.11-2 « TABLE MAINTENANCE 7

 

Overtime Labor Rate The per hour charge billed for this work type for
this technician during overtime hours. Enter $37.50
as 3750 and press [Field Exit].

Field Labor Rate The per hour charge billed for this work type for
this technician if the work is done in the field. Enter
$37.50 as 3750 and press [Field Exit]. Overrides
overtime rate.

Print Tables

O From the Table Maintenance Menu, press Cmd9-Print Tables.

Example of Technician Table

‘TIME CLOCK TABLES LIST Date 4/30/96
‘TECHNICIAN ‘TABLE Time 13:22:23

START
Te

08:30:00
05:30:00
06:30:00

08:00:00

07:00:00

WW EQUIPMENT SALES & RENTALS (TIME CLOCK TABLES LIST Date 4/20/96 Page 3
BELLINGHAK, WA a STATUS CODES Time 13:22:23 X$n20-2
:EQUIRED

### Description

LUNCH
sREAK

a
WAITING FOR PARTS
REPAIR

ee ED


8 X5.11-2 e TABLE MAINTENANCE RELEASE 2.2

 

Notes:

## CHAPTER X5.11-3

### Configuration

### Introduction

Use this option to configure default values for Time Clock to use, including
starting and ending times for a typical day, and selection of a Time Clock report
that will be printed when Accounting End of Day is run. Configuration can be at a
company level or customized for individual divisions.

This ‘option is also used to grant or remove access to Point of Sale labor lines.
Because the integrity of Time Clock Reports will be compromised if labor lines
are entered through Point of Sale, they are disabled when Time Clock is installed.
From time-to-time, it may be necessary for someone to enter a labor line from
Point of Sale; therefore, a process has been provided whereby Point of Sale access
can be unlocked for one or more users.

Usually, a particular user will be granted permission enter labor lines at Point of
Sale to meet an emergency, and then it will be revoked. See POS ACCESS
LOCK.

 

### Warning

To ensure the accuracy of Time Clock reports, make sure all labor lines that are
entered at Point of Sale are duplicated in Time Clock. Better yet, don't use labor
lines at Point of Sale at all.


2 X5.11-3 » CONFIGURATION RELEASE 2.2

### Contents

HOW TO RUN........ccsscsssnsscsnssestensoesersnsscettessetscansesnsuesntassnenesaesneatenenensensneens 3
COMPANY CONFIGURATION........c:scsscsserensssssesssesnentersensouocstescuesssensneonane 4

### Divisional Configuration

 

POS ACCESS LOCK.......ccccsssssessssesssessesssssnsesssocsnsneesssconsarsnsvenvevouseesnenss 11


POINT OF SALE X5.11-3 e CONFIGURATION

### How To Run

O From the Time Clock Menu (X5-11), select option 3, Configuration. The
entrance screen prompts you for a division.

Division Prompt

A NW EQUIPMENT SALES & TIME CLOCK CONFIGURATION X5B30-102

Division (or blank for Company configuration)

Cméi-Cancel Cmd2-POS Access Lock

C1 If this is the first time you have used Time Clock or if you want to configure


 

Time Clock for the entire company, leave the division prompt blank and press

{Enter]. Values configured for the company will be used for each division,

including brand new divisions as they are set up in Security Maintenance (X6-

6). See COMPANY CONFIGURATION.
C1 If you want to configure Time Clock for a particular division, type the
division code and press [Enter]. See DIVISIONAL CONFIGURATION.
C1 If you want to grant or remove access to Point of Sale labor lines, press
Cmd2-POS Access Lock. See POS ACCESS LOCK.


4 X5.11-3 « CONFIGURATION

### Company Configuration

When the division prompt is left blank, the company configuration screen is

displayed.

Company Configuration Screen

 

 

 

 

 

Cmd3-No Change

 

Default Start of Day (hhmmss)

Default End of Day (hhmmss)

Window for start/end of day

A A&R EQUIPMENT SALES TIME CLOCK CONFIGURATION for Company X5B30-102
Default Start of Day (hhmmss)... 070000
Default End of Day (hhmmss) . 163000
Window for start/end of day. 10 Minutes + or - in which punch=default
Hours Rounding (W,T,Q,H)........ 7 Whole, Tenths, Quarters, Hundredths
Sales Code, Customer Docs... TC
Sales Code, Internal Docs. Tr
Sales Code, Warranty Docs... ™w
Timeout (seconds) 060
End of day report (T,W,N). T Technician, Work order, or No report
Overall Default Division ... A
Default Division by Workstation
WS Div WS Div ws Div WS Div
cK OA

The default starting time can be changed
later for any individual technician in the
Technician Table (Table Maintenance).
Military time is used: enter 5:15 P.M. as
171500.

The default ending time can be changed
later for any individual technician in the
Technician Table (Table Maintenance).
Military time is used: enter 5:15 P.M. as
171500.

Minutes for window or grace period during
which any punch is considered the same as
the default start/end time or the technician's

 

cC

io


Hours Rounding (W,T,Q,H)

Sales Code, Customer Docs

Sales Code, Internal Docs

Sales Code, Warranty Docs

Timeout (seconds)

End of day report (T,W,N)

X5.11-3 e CONFIGURATION 5

 

start/end time. Prevents many small
unnecessary overtime charges due to minor
variations in punch-in or punch-out times.
W=Whole, T=Tenths, Q=Quarters,
H=Hundredths. Applies to how time is
rounded for Point of Sale. Time is calculated
in hours, minutes, and seconds. Hours can
be rounded to the nearest whole hour (W),
the nearest tenth of an hour (T), the nearest
quarter hour (Q), or the nearest hundredth of
an hour (H). For example, if the time spent
on a job is 05:25:30, it is billed as 5 hours
(whole), 5.4 (tenths), 5.25 hours (quarters)
or 5.42 (hundredths).

The defauit sales code for placing charges
on customer documents. The sales code
moust be of format "L." Tax codes follow the
same rules as at Point of Sale.

The default sales code for placing charges
on internal documents. The sales code must
be of format "L." Tax codes follow the same
tules as at Point of Sale.

The default sales code for placing charges
on warranty documents. The sales code must
be of format "L." Tax codes follow the same
tules as at Point of Sale.

Timeout applies only to the User ID
TCLOCK and refers to the time interval
allowed for entering a valid employee ID in
Time Clock. All activity is logged;
therefore, it is important to monitor the end
of day report for suspicious activity and
possible security breaches. To disable the
timeout feature, enter 999.

Review by Technician, Review by Work
Order, or No audit report to be printed
automatically at Accounting End of Day. If
Accounting End of Day is not run, this
report will not be printed automatically, but
it can be run from Audit Reports (X5.11-3).
A printers can be selected on the divisional
configuration screen.


X5.11-3 » CONFIGURATION RELEASE 2.2

Overall Default Division 1-character division code. Enter the division
that is used most often for service jobs. See
Default Division by Workstation below.

Default Division by Workstation This table records workstation IDs and the
divisions where User ID TCLOCK is used.
If User ID TCLOCK is used at a workstation
that is not in this table, the overall default
division (above) is used.

DIVISIONAL CONFIGURATION

A A&R EQUIPMENT SALES

 

Timeout (seconds) ....

Cmd3-No Change

 

When a division code is provided on the entrance screen, the configuration screen
for that division is presented. In this section, you'll learn how the sales codes and
the I/W flag on the Time Clock screen are determined. The interrelationships
between the customer record, Time Clock Configuration, and billing codes
associated with each status code are explained.

Divisional Configuration Screen

 
   

X5B30-103

  

  
  

TIME CLOCK CONFIGURATION for Division A

Default Start of Day (hhmmss)... 070000
Default End of Day (hhmmss)..... 163000
Window for start/end of day.
Hours Rounding (W,T.Q,8)
Salas Code, Customer Doc
Sales Code, Internal Doc

10 Minutes + or ~ in which punch=default
Whole, Tenths, Quarters, Hundredths

 

   
  

 

 

 

End of day report (7,W,N)....... v Technician, Work order, or No report
Printer for end of day report .. Pl
Default for lines on war docs .. W Wedefault all lines to W & use war SC

Note: The default for documents opened to a customer
address where I/W=l (or W) will be the sales code for
Internal (or Warranty) documents. The default sales code
for internal documents is always used when the POS
document is opened to a unit.


POINT OF SALE X5.11-3 e CONFIGURATION

 

Most prompts on the Division screen are the same as the company screen.
Definitions begin on page 4. The following prompts are unique to the Division
screen.

Printer for end of day report
The $/36 printer ID where the End of Day report should be printed.

Default for lines on war docs
You can specify the default value for the I/W field in Time Clock. This field can
be blank or "W." The corresponding field in Time Clock is illustrated below:

§ A&R EQUIPMENT SALES TIME CLOCK 3/26/98 XSB10-104
Technician: BUBBA BUBBA JONES

Work Order: w045295 Customer: PARKO1 AUSTIN PARKER
Sales Code

Status: __
Status Codes Status Codes
10 PRELIMINARY DETERMINATION Y 35 ASSIST 5
12 PRELIM 2 ¥ 40 WORK COMPLETE
13 PRELIM 3 50 TEST
14 PRELIM 4 52 TESTING AGAIN
20 WAITING FOR PARTS/INFO 54 TESTING AGAIN AND AGAIN
22 WAITING 2 55 COURT
23 WAITING 3 56 TESTING UNTIL IT WORKS
24 WAITING 4 58 TESTING, WHAT ELSE TO DO?
39 ASSISTANCE 60 RESEARCH
32 ASSIST 2 70 LUNCH
33 ASSIST 3 71 LUNCH 1
34 ASSIST 4 72 LUNCH 2

 

¥
yx) Ww
¥] or
wi oN
yl] ox
vy] ow
yi or
xy o¥
xy] ¥
y|ow
y| 1

Woe eB BM
HBA KR Be

omdl-Cancel Cmd3-Return to Work Order Page Up Page Down Home

 

The default values of the sales code and I/W field depend on the value of the /W
field in Receivables Maintenance. The value of the I/W field may be changed by
the billing code.


 

 

 

X5.11-3 « CONFIGURATION RELEASE 2.2
(
A&R EQUIPHENT SALES RECEIVABLES MAINTENANCE x11201-02
Division: $
Address # ....... PARKO2
Name........ ... RACHEL/ PARKER
Extended Name....
Address ....... :
Extended Address.
City, State ..... Zip code .
Phone
Ph #2 Ext Sort code
Fax Edit code R s
Account # S124 Cust type 0 Statement? ¥
Credit limit Int /War ¥
Insurance agent
Policy number Insurance phf
Expiration
Note
Tax code t Discount code
Credit code (1) (2) Qty break N Ship to addr#
Tax number Freon Certification #
cmd3-Return Cmd6-Note Cmd8-Credit cards To delete enter 'Y' (

The rules governing the sales code and I/W field are summarized in the 3 tables
below. For further clarification, see the text that follows.

Step 1: How the Default Sales Code is Determined in Time Clock

 

Document opened to customer:

Time Clock Uses the Default Sales Code for:

 

 

 

 

Int/Warr=Blank Customer docs
Int/Warr=I Internal docs
Int/Wan=W Warranty docs
Document opened to unit Internal docs

 

 

Step 2: How the Default I/W Field is Determined in Time Clock

 

If "Default for war docs" is:

Y/W in Time Clock is:

 

 

blank

blank

 

Ww __|

W (Warranty Addr# required on POS doc.)

 

Step 3; How the Billing Code Affects the I/W field
Hf status code’s billing code (Bill) is: | /W. changes to:

 

 


 

 


 

No change
[No change :


X5.11-3 «e CONFIGURATION 9

 

_

I Gnternal Addr# required on POS doc.)

 

 

 

 

W (Warranty Addr# required on POS doc.)

 

 

Sales Code. If, in the customer's master record, the Int/War field is blank, the
customer sales code default is used; if "I," the internal sales code default is
used; if "W," the warranty sales code default is used. For customer addresses
that are Internal or Warranty (Int/Warr="I" or "W" in Receivables
Maintenance (X11-2), the /W field may be blank, in which case
corresponding addresses are not required on the Point of Sale document.
Individual lines are not marked "I" or "W" on the document; therefore,
separate Internal and Warranty documents are not generated.

I/W field. If "Default for lines on war docs" is blank, the I/W field on the
Time Clock screen will be blank; if it is "W," the I/W field on the Time Clock
screen will be “W." Any time the I/W field is "I" or "W," the corresponding
address numbers must be present on the Sold To screen of the Point of Sale
document.

Changing. Both fields can be changed on the Time Clock screen.

Status Code Billing. If a status code with a billing code of "I" or "W" is
selected, the I/W flag will be changed to match it automatically, and the
corresponding Internal or Warranty address is required to be on the Point of
Sale document (Sold To screen). Labor lines will be entered as "I" and "W"
lines on the document.

Document Opened to a Unit. The default intemal sales code from Time
Clock Configuration is used.

Document Opened to Internal or Warranty Customer. If the customer is a
warranty or internal customer (Int/War field on the customer's master record
in Receivables Maintenance has a value of "I" or "W"), system addresses are
not required on the Sold To screen unless the I/W field in Time Clock is set to
'T" or "W."

Thermo King Warranty Documents. Even if the Point of Sale document is a
Thermo King warranty document, which is indicated by setting the TK field
on the Sold To screen to "T", system addresses are required on the Sold To
screen in order to mark lines as internal or warranty.

 

### Warning

Job codes can be used on non-warranty lines. This is true regardless of whether
TK War=T or not. If you suspect that a job code has not been processed correctly,
make sure the line is a warranty line or that TK Warr=T on the work order.


10 X5.11-3 «e CONFIGURATION RELEASE 2.2

POS ACCESS LOCK

‘You can give permission to selected individuals to enter labor lines on work
orders at Point of Sale although this practice is not recommended and
compromises the integrity of Time Clock's Audit Reports.

O On the Configuration entrance screen, press Cmd2-POS Access Lock. The
configuration security gate is displayed. Upon passing the gate successfully,
the following screen is presented.

List of User Profiles with Access to Labor Lines

 

A A&R EQUIPMENT SALES TIME CLOCK CONFIGURATION X5B30-105
User Profiles with POS Labor Lines Access
BARB EBS SUE LINDA

 

 

 

 

 

 

 

 

 

 

cmd3-Return Enter-Save & page down Page Up Home

 

 

### Warning!

After access has been unlocked, users must exit Point of Sale and POS Access
Lock for the entries to take effect.

 

O) To remove a profile from the list, simply [Field Exit] through it, and press
[Enter].

## CHAPTER X5.11-4

REVIEW BY TECHNICIAN

### Introduction

This option, which is similar to Review by Work Order, is used to review billing
and make sure that charges accurately reflect the work technicians have done
before work orders are closed and posted. This function is not available to most
technicians—usually only the parts manager or accounting staff are allowed to
review or change Time Clock data. If the Thermo King OPT is on (X63B-6), the
Review by Technician screen displays job code fields, which are illustrated on
page 12.

In this job, as opposed to Review by Work Order, one technician's time is
displayed for a selected date for all the work orders that technician works with on
that day. Consecutive time periods that make up the technician's entire day are
displayed in order by punch-out time to make it easy to see how the day was
spent. Lines can be added, deleted, and changed.

Charges are placed on the point of sale documents directly from this job;
however, nothing is posted to the general ledger until the document is closed and
posted.

Changes can be made to individual punch-out lines, or a day's entries can be
created. The default labor sales codes set up in Configuration for customer,
intemal, or warranty labor are used. Shortcuts expedite the process. For example:
if you enter the elapsed time, the system can calculate the punch-out time, or if
you enter the punch-out time, the system can caiculate the elapsed time. The
following fields can be changed without deleting and re-entering lines in this job:
= Time Clock status code

Time Clock work type code

Field (Y/N)

Hours Reported and Hours Billed

Rate

Tax and discount codes

Billing entity (Customer, Internal, Warrantor, or Non-billable)

Comment
Thermo King job code (available only if the Thermo King dealer OPT (X63B-
6) is on).


2 X5.11-4 « REVIEW BY TECHNICIAN RELEASE 2.2

### Contents

INTRODUCTION .........ccscessesrsrersscesssesssnssnsnerensessesenearanensesneasseenseneassnsestnens 1

HOW TO RUN.
Adding a Line
Changing a Line.

 
 
 
   
 
 

THERMO KING SCREENS. ....
Miscellaneous Job Codes

### Fields & Descriptions

POINT OF SALE X6.11-4 » REVIEW BY TECHNICIAN 3

### How To Run

O From the Time Clock Menu (X5-1 1), select option 4, Review by Technician.
Technician and Date prompts are presented.

Technician/Date Prompts

A NW EQUIPMENT SALES & 1 REVIEW BY TECHNICIAN XSB40-101

Enter a Technician ID.. HAL

and a Date (mmédyy).... 033198

cmd1-End

 

 

1 Enter a technician's system address and the date the work was done, and press
{Enter].


Detail Screen

A A&R EQUIPMENT SALES

Ln w/o #
ol IN

62 ROOb143
03 RO00143
04 RO00143
0S RO00143

cmd3-Return

REVIEW BY TECHNICIAN

SC Time St W

Te 08:59 17 0
TC 09:01 60 9

 

cmd10-Totals

RY TECHNICIAN 04/02/1998 BAL
F Report Billed Rate TDS Jobcd

N
00150 02500 A 04000
28760 02500 A 02999
N
14000 92500 A 01999

Enter a Line # to change, or press ENTER to add a new line.

Line #
co

Note the technician's ID in the upper right corner.


POINT OF SALE X5.11-4 « REVIEW BY TECHNICIAN 5
Ss meee

Adding a Line

Adding a line affects all the lines below it.

O To add a line, press [Enter] on an empty line (00). A new line is displayed.

 
  

    
 

A NW EQUIPMENT SALES & 3 REVIEW BY TECHNICIAN 04/30/1996 BONNIE X5B40-103
in W/o # Oc D-Ln SC Time St WF Report Billed Rate TDB Comment
01 IN 07:02 N

    
       
    
   
   
    
   
   
    
  
 
  
   
   
    
  
  
  
  
 

02 RODCI1SE O 0020 Tc 09:33 70 0 N 00250 00250 03750 a
03 RO00158 oO 0020 TC 11:15 40 0 N 00170 00170 03750 A
04 ROOD1SS 12:00 20 0 N 00080 N
05 ROO0156 oO 0030 FC 13:20 31 0 N 00140 00140 03750 a
06 ROOD156 14:42 10 0 N 00140 N
07 ROO0156 oO 0040 fC 15:30 60 0 N 00080 OoDsC 03750 aA
08 ROOOISE oO 0050 TC 17:00 60 0 N 00150 001S¢ 05625 A

If the Thermo King OPT (X63B-6) is
not on, job code fields are not

 

displayed.
Cmd3-Return Cmdi0-Totais Cmd19-Delete line
Ser Work w/o Sales Punch Out -------~ Work Order Information -------
Ln Order # Line Code Time Dv Addr Date oc P/O #
oo _ _—
Work Hours Hours ROSE CONSTRUCTION CO. 7
Stat Type Fld Report Billed Rate T D Bill Comment BONNIE 04301996

 

0 N

 

 

 

 

 

O Fill in the W/O#, Status, Work Type, Field (Y/N), and either elapsed time or
hours reported/billed. Other fields are optional.

©) Press [Enter]. The system assigns a line number and adds the line to the Time
Clock Review screen in order by punch-out time. At the same time, the labor
line is added to the P.O.S. work order if it is a billable line.

 

Tip
If you furnish the elapsed time, the system will calculate hours reported/billed and
punch-out time. If you furnish the hours reported/billed, the system will calculate
elapsed time and punch-out time.


X5.11-4 » REVIEW BY TECHNICIAN RELEASE 2.2

Changing a Line
Changing a line has no effect on the lines below it.

1 To change a line, enter its screen line number (columns 1-2). The line is
displayed as illustrated below:

 

A A&R EQUIPMENT SALES REVIEW BY TECHNICIAN 03/31/1998 HAL X5B40-103
Ln w/o # oc D-Ln SC Time St WF Report Billed Rate TDB Comment

01 ROOO142 Oo 0030 Tc 09:00 12 0 N 02500 A WORKED WITH JOE
02 ROOO142 10:15 35 0 N N INSPECTION

03 ROCO142 9 0040 TC 14:00 40 0 N 02500 A FIXED IT

cmd3-Return Cmdl0-Totals Cmd19-Delete Line
Ln W/O # D Addr Date oC P/O # Customer or Unit
02 ROO0142 A 000004 033198 0 Pat Rose Construction Co.
w/O Line SC Punch
101500
Stat Type Fld Report Billed Rate T D Bill Comment
35° 0 N N INSPECTION

 

1 Make the necessary changes and press [Enter]. The next line number is
displayed (see screen below). You can roll through the lines by pressing
[Enter].


POINT OF SALE X5.11-4 « REVIEW BY TECHNICIAN 7

 

A A&R EQUIPMENT SALES REVIEW BY TECHNICIAN 03/31/1998 HAL X5B40-102
La W/o # OC D-Ln SC Time St WF Report Billed Rate DB Comment

G1 ROOO142 O 0030 Tc 09:00 12 0 N 02500 A WORKED WITH JOE
02 ROO0142Z 10:15 35 0 N N INSPECTION

03 ROOO142 Oo 0040 TC 14:00 400 N 02500 A FIXED IT

Cmd3-Return Cmdl0-Totals Page Down Home

Enter a Line # to change, or press ENTER to add a new line.

Line #
03

 

Making a Line Non-billable

Any updateable field can be changed; however, lines billed cannot be changed to
zero. Instead, the line should be changed from billable to non-billable.

O1 To change a line to non-billable, type its screen line number (columns 1 & 2)
and press [Enter].

O Move the cursor to the field labeled "Bill," and change its value to "N," and
press [Enter]. A confirmation message is displayed as illustrated on the screen
below.


X5.11-4 « REVIEW BY TECHNICIAN RELEASE 2.2

   
   

ANW EQUIPMENT SALES & 8 REVIEW BY TECHNICIAN 04/30/1996 BONNIE X5540-108
Ln W/O # oC D-Ln SC Time St WF Report Billed Rate TDB Comment

    

 

   
  
  
 
  
     
   
  
    
      

Press ENTER to confirm delete.

(Record is now non-billable;
its POS line will be deleted.)

cmd3-Return without deleting

 

 

Scr Work W/O Sales Punch Out -~------ Work Order Information --
In Order # Line Code Time Dy Addr. Date oc P/O 4
02 R000156 e020 TC 093333 A ROSEQ1 4/30/96 0
Work Hours Hours ROSE CONSTRUCTION Co.
Stat Type Fld Report Billed Rate T D Bill Comment BONNIE 19960430 A

70 o N 250 90000 03750 N CHANGED TO NON-BILLABLE LMP

 

 

 

© Press [Enter] to confirm. The POS line will be deleted. It will remain on this
screen, as illustrated below.

      

 

Lo

### Review By Technician

 

A NW EQUIPMENT SALES & REVIEW BY TECHNICIAN 04/30/1996 BONNIE XS5B40-102
Ln w/o # oC D-Ln SC Time St WF Report Billed Rate TDB Comment

o1 IN 07:02 N

02 ROO0156 09:33 70 0 N 09250 N CHANGED TO NON-B
03 ROGO158 Oo 0020 TC 11:15 40 9 N 00170 00170 03750 a

04 ROO0156 12:00 20 0 N 09080 N

05 ROOCISE 0 0030 Tc 13:20 31 0 N 00240 00140 03750 a

06 ROO0I5SE 14:42 10 0 N 00140 N

07 ROO015E Oo 0040 Te 15:30 69 0 N 00080 00080 03750 A BILL'S SUPERVIST
08 ROODIS6 O 0050 TC 17:00 60 0 N 09150 00150 05625 A

Cmd3-Return Cmé10-Totals Page Down Home

Enter a Line # to change, or press ENTER to add a new line.

 

Line #
02

 

 

FYI. There is no way to get Time Clock to keep a labor line in Point of Sale that
has zero hours billed.


10 X5.11-4 « REVIEW BY TECHNICIAN RELEASE 2.2
ee Ee

Deleting a Line
Deleting a line affects all the lines below it.

O To delete a line, type its screen line number (columns 1 & 2) and press [Enter].
fl Press Cmd19-Delete. A confirmation message appears, as illustrated below.

A NW EQUIPMENT SALES & 8 REVIEW BY TECHNICIAN 04/30/1996 BONNIE XS5B40-108
Ln w/o # oc D-Ln SC Time St WF Report Billed Rate TDB Comment
Press ENTER to confirm delete.

Deleting a Time Clock record
also deletes its POS line.

cmd3-Return without deleting

Ser Work W/O Sales Work Order Information
Ln Order # Line Code Time Dy Addr Date oc P/O #
08 ROOOLSE 0050 TC 170009 A ROSEO1 °
Work Hours Hours ROSE CONSTRUCTION co.
Stat Type Fld Report Billed Rate T D Bll Comment BONNIE 19960430 A
60 ° N 150 150 05625

O Press [Enter] to delete the line. The corresponding line on the Point of Sale
document is also deleted.


Totals

Ln
02
02
03
04
oS
06
907
08


 

O To check totals, press [Cmd10]. A window pops up, which shows the total
hours that have been reported and billed for the date, which was selected at

the entrance screen.

w/o F
IN
ROO0LS6
ROOO1SS
ROOO1SE
ROOO1SE
ROO015S6
ROO0156
ROOCLSE

cma3-Return

Line #

oc

A NW EQUIPMENT SALES & 2

D-in sc

0020 TC
0020 TC

0030 Tc

0040 Tc
00s0 FC

Cmd10-Totals

REVIEW

Time

07:02
09:33
11:15
12:00
13:20
14:42
15:30
47:00

st


ceo 0coe

azz

Page Down

X5.11-4 » REVIEW BY TECHNICIAN

BY TECHNICIAN 04/30/1996 BONNIE XS5B40-102
F Report Billed Rate DB Comment

N 00250
N 00170
N 00080
N 00240
90240
09080
00150

00250
06170

00140

90080
90150

Home

N
03750 A
03750 A
N
03750 A
N
03750 A BILL'S SUPERVISI
os625 A
: Total Hours
2 Reported Billed
z 10.10 7.90

Enter a Line # to change, or press ENTER to add a new line.

O1 When ail changes have been made, press [(Cmd3].


12 X5.11-4 « REVIEW BY TECHNICIAN RELEASE 2.2

 

### Thermo King Screens

In this section, only the aspects of the Review by Technician screen that pertain to
Thermo King are discussed. Please read the previous sections to get a full
understanding of this screen, how it works, and the fields on it.

Time Clock follows the same specifications and limits for creating Thermo King
warranty claims as in Point of Sale Invoicing, which are:

>

»


yvurwwy

One claim per work order

Each claim can contain multiple segments (one segment only for a “Service
Parts Only Claim’)

One cause of failure (COF) per segment

Up to 27 part lines per segment (one part line only for a “Service Parts Only
Claim”)

Up to 9 Misc. parts per claim

Up to 3 outside invoices per claim

Up to 10 comment lines per claim

Up to 18 serialized parts per claim

No labor lines on “Service Parts Only Claims”

If the Thermo King OPT is on (X63B-6), the Review by Technician screen
displays job code fields, as illustrated below.


POINT OF SALE X5.17-4 « REVIEW BY TECHNICIAN 13

 

 

A A&R EQUIPMENT SALES REVIEW BY TECHNICIAN 04/02/1998 HAL X5B40-103
in w/o # oC D-Ln SC Time St WF Report Billed Rate TDB JobCd Comment
01 IN 07:58 N

02 RO00143 0 0020 TC 08:59 17 0 N 60100 00150 02500 A 04000

93 RO00143 oO 0030 TC 09:01 60 ON 28760 02500 A 02999

04 ROO0143 09:15 30 0 N GO0z2 N

95 R000143 0040 TC 09:32 16 0 N 00030 14000 02500 A 01999

Job Code fields are present for all work orders if the TK Dealer
OPT is on. If TK Warr=T on the work order and Bill=W, a job
code is required.

Cmd3-Return Cmdl0-Totals cmdl9-Delete Line
In W/O# D Addr Date oc P/o # Customer or Unit
00 ROO0143
W/O Line SC Punch Jobed Job Code Description =
to 815 02999 12345678901234567890223456789 :
Stat Type Fld Report Billed Rate T D Bill Comment
0 N

 

The expectation is that you will be using job codes; therefore, you'll go into
“lookup” mode when you press [Enter] on the Time Card Entry screen. If TK
Warr=T on the work order and Bill=W on the labor line, a job code is
required.

 

To skip a job code, the following conditions must be true:
1) TK Warr=blank on the work order
2) No job code is entered

3) Billed hours are entered

Also, if you don’t want to use a job code, you can press F3=Exit after you enter
the series of Thermo King related screens.

  
  

 

Reminder
The "TK Warr" flag on the Sold To screen at Point of Sale cannot be changed if
there is a warranty line on the work order.


14 X5.11-4 » REVIEW BY TECHNICIAN

Miscellaneous Job Codes

When a miscellaneous job code is entered, the following message appears at the

bottom of the screen:

 

A B&R EQUIPMENT SALES

REVIEW BY TECHNICIAN 04/02/1998 HAL

Ln W/O # oc

ol IN

02 ROOO143
03 ROOO143
04 ROO0143

D-Ln SC Time St WF Report Billed Rate TDB Jobcd
07:58 N
0 0020 TC 08:59 17 0 N 00100 00150 92500 aA
0 0030 TC 09:01 600 N 28760 02500 A
09:15 30 0 N 00022 N

04000
023999

‘X5B40-103
Comment.

omd3-Return

In W/o #

00 RO00143

W/o Line Sc Punch
0080 TC 133000

Stat Type Fld Report Billed Rate T D Bill Comment

16 0 oN 250 250 02500 A

Verify Miscellaneous Job Code hours, then change or accept as is.

(md10-Totals  Cmd19-Delete Line (
DAddr Date o¢ P/O ¥
A 000004 021298 © TCLOCK
Jone
01999

Customer ox Unit
Pat Rose Construction Co.
Job Code Description

 

 

This message gives you a chance to enter the description and the rate (there is no
flat rate for miscellaneous job codes) rather than requiring you to bring the line
down again to change it after it is added. The message is necessary at least for
new operators since they do not normally see the whole line again unless there is
an error. Without a message, they will wonder what they did wrong. This also
gives them a change to review the whole line together to see if their choice of a
miscellaneous job code requires further refinement of other fields.

### Fields & Descriptions

X5.11-4 « REVIEW BY TECHNICIAN 15

The following labels appear at the top of the screen.

La
W/O#

oc

D-Ln
sc
Time

St

Report

Billed

Rate

Line number.

Work order number or "IN" for the first punch of the day.
Division code.

Point of Sale Status:

C=Closed
N=No document found

R=Reopened

 

 

Line number on the point of sale work order.

Sales code.

Time of day (hh:mm). Punch-out time (without seconds).
Time Clock status code.

Time Clock work type code.

Time Clock field (Y/N), indicating whether work was done
in the field.

Time reported in decimal equivalent. Two decimal places
assumed; for example, 3.50 means 3 hours and 30 minutes.
Can be negative.

Time billed in decimal equivalent. Two decimal places
assumed; for example, 3.50 means 3 hours and 30 minutes.
Can be negative.

Dollar amount. Rate at which work will be billed. Two
decimal places assumed; for example, 3750=$37.50.

Tax/Discount/Bill. Tax and discount codes plus the billing
entity. The document defaults are used. The billing entity


16 X5.11-4 » REVIEW BY TECHNICIAN RELEASE 2.2

for individual lines, which may be different from the
document default are coded:
C or blank=Customer
I=Internal
W=Warrantor
N=Non-billable.

 

 

 

 

 

Lines can be designated as Internal or Warrantor only if the
respective addresses have been entered on the Sold To
screen of the work order.

JobCd Thermo King job code.
Comment Comments are entered in review only. They cannot be
entered in Time Clock Entry.

The following fields are available for input only while working on a brand new
line. To change them after they are entered, it is necessary to press Cmd19-Delete
and re-enter the line.

Ln 2 digit. Screen line number (columns 1-2). Abbreviated as
“Ln" on the top line. If you are changing a line, enter its
number here. If you are adding a line, simply press [Enter].
You cannot insert a line number. The system assigns a line
number after you furnish the information and press [Enter]

to add it.
W/0# Work order number or "IN" for the first punch of the day.
‘W/O Line Line number on the point of sale work order. If there is a

prefix associated with the line number, it is displayed in the
space immediately on the left.

sc 2 characters. Sales code. The default sales code for the type
of line (CIW) is used. Default sales codes are set up in
Configuration.

Punch Punch OUT time (hhmmss). Seconds are optional. Furnish

the time reported and leave this field blank and the system
will supply the time elapsed since the most recent
punch-out of the day.

JobCd 5-digit Thermo King job code.

Job Code Description 29-characters. Except for miscellaneous job codes, the
description is furnished by Thermo King.

cr


POINT OF SALE X5.11-4 « REVIEW BY TECHNICIAN 7
—_ re errr errr NE

The following informational fields are furnished from the work order. No input or
changes are allowed.

 

 

 

D 1 character. Division code.
Addr 6 character address number of the customer.
Date Date (mmddyy). Date on which work order was opened.
oc 1 character. Open/Closed Status of P.O.S. Document.
C=Closed
O=Open
R=Reopened
V=Voided
P/IO# Purchase order number.
Customer or Unit Customer name or unit make, model, & serial
number.

These fields are from Time Clock Entry and can be changed on this screen:

Stat (Input) 2 digits. Time Clock status code. Abbreviated as "St" on
the top line. Status codes are set up in Table Maintenance.
Example: 10=Lunch, 20=Break, 99=Job Complete, etc.

Type (Input) 1 digit. Time Clock work type code. Abbreviated as “W"
on the top line. Work type codes are set up in Table
Maintenance. Example: 0=Regular, 1=Steam Cleaning, etc.

Fld (Input) Field (Y/N). Abbreviated as "F" on the top line. "Y" means
the work was done in the field and will be charged at field
rates.

Report (Input) Number of hours reported in decimal equivalent; for

example, enter 3 hours and 30 minutes as 350 and press
[Field Exit}. Same as "Report" on the top line. If elapsed
time is entered, the system will calculate hours reported and
use the same amount for hours billed.

Billed (Input) Number of hours billed in decimal equivalent; for example,
enter 3 hours and 30 minutes as 350 and press [Field Exit].
Same as "Billed" on the top line. If elapsed time is entered,
the system will calculate hours reported and use the same
amount for hours billed.


18 X5.11-4 « REVIEW BY TECHNICIAN RELEASE 2.2

Rate (Input)

T (Input)

D (Input)

Bill (Input)

Comment (Input)

If hours billed are not entered, the number of hours
reported is used by default. Hours billed are rounded
according to the configuration option only when the hours
reported default is used. If hours billed are entered directly,
the number is stored exactly as entered.

Dollar amount at which hours will be billed. Leave this
field blank to use the default from the technician's table,
which is set up in Table Maintenance. Enter $35.25 as 3525
and press [Field Exit].

Tax code. Tax codes follow the same rules as Point of Sale
Invoicing. If a tax code is entered on the Time Clock detail
line, it takes precedence. If not, the tax code associated
with the sales code is used. If there is none, the tax code
associated with the customer is used.

Discount code. Discount codes follow the same rules as
Point of Sale Invoicing. If a discount code is entered on the
Time Clock detail line, it takes precedence. If not, the
discount code associated with the sales code is used. If
there is none, the discount code associated with the
customer is used.

Billing entity. The document default is used. Individual
lines, which may be different from the document default
are coded:

N=Non-billable.

To make a line non-billable, enter "N" in this field. The
corresponding POS line is deleted. See Making a Line
Non-Billable on page? .

 

30 characters.

## CHAPTER X5.11-5

REVIEW BY WORK ORDER

### Introduction

This option, which is similar to Review by Technician, is used to review billing
and make sure that charges accurately reflect the work that was done. This
function is not available to most technicians—usually only the parts manager or
accounting staff are allowed to review or change time clock data. It can be
accessed by way of the Time Clock Menu or by pressing [Cmd14] from the detail
screen at Point of Sale Invoicing (X5-1), which takes you directly to the detail
screen of labor lines for the current work order.

Charges are placed directly on point of sale documents directly from this job.
Nothing is posted to the general ledger until the work order is closed and posted.
Default labor sales codes set up in Configuration for customer, internal, or
warranty labor are used.

Lines cannot be added or deleted in Review by Work Order; however, some
changes can be made to individual punch-out lines. Lines can be changed to
billable or non-billable. Lines can be charged to internal or warranty provided the
respective internal or warranty addresses are entered on the Sold To screen of the
work order. Hours Reported cannot be changed because doing so would impact
technicians' time on other, unidentified work orders.

The following fields can be changed without deleting and re-entering lines in this
job:

Time Clock status code

Time Clock work type code

Field (Y/N)

Hours Billed

Rate

Tax and discount codes

Billing entity (Customer, Internal, Warrantor, None)
Comment

Thermo King job code (available only if the Thermo King dealer OPT (X63B-
6) is on).

r+ eee ooo


2 CHAPTER X5.11-5 e REVIEW BY WORK ORDER RELEASE 2.2

TIP : ES beg
To.add or delete a'line, bring it down as if to change it, then press Cind14-Review
by Technician, Make additions or changes or delete the. line. When you press

[Cmd}] to end Review by Technician, you will-eturn to. Review by Work Order.

### Contents

ENTRANCE SCREEN ..

 

CHANGING A LINE..........:cccesssorssesssssecessesssnsonsneesenesesssarssseesorontnesenenenteosers 5
TOTALS... ..sesscecnsseeree doesegnroennen sueverensqvevensecavenssuaveueesvevensssevesavevorsvenevossese 1nar2 6


POINT OF SALE CHAPTER X5.11-5 « REVIEW BY WORK ORDER 3
Se eee OO OSs ee

### Entrance Screen

O From the Time Clock Menu (X5-11), select option 5, Review by Work Order.
A work order prompt is presented.

A NW EQUIPMENT SALES & 1 REVIEW BY WORK ORDER X5B50-101,

Enter a Work Order .... ROO0156

 

Work Order Prompt

O Enter a valid work order and press [Enter].


La D-in
ol
02
03
oa 0020
O5 0030
06 9040
0? oaso
8 0060

cmd3-Return

Line #
00

 

Detail Scre

 

A NW EQUIPMENT
sc

rc
oC
vc
C
biel

en

 

 

 

®

e200 0000

REVIEW BY WORK ORDER

ZAAZwA~Zzsaezwyan

SALES & 2 REVIEW BY WORK
Tech Date st
BONNIE 04/24/98 0 20
BONNIE 04/25/98 742 10
BUTCH 04/26/98 5 10
BONNIE 04/21/98 3 70
BONNIE 04/18/98 320 31
BONNIE 04/28/98 15:30 60
BONNIE 04/30/98 17:00 60
BUTCH 04/23/98 15:08 40
cmdl0-Totals Page Down

Enter a Line # to change.

ORDER
Report.
00080
00140
00100
00250
00140
00080
00150
06240

Home

ROOOLSE
Billed Rate

06250
00440
00080
oc1se0
00240

03750
03750
03750
05625
03750
X5B50-102

TDB Comment

bebe bee be

N
N

### Bill'S Supe

POINT OF SALE CHAPTER X5.11-5 e REVIEW BY WORK ORDER 5
Oo  SFeFSFSSSSSSSSsSS Oe eee

Changing a Line

O To change a line, enter its line number. The line is displayed as illustrated

below:

A A&R EQUIPMENT SALES REVIEW BY WORK ORDER ROGO143 X5B50-103
In D-Ln SC Tech Date Time St WF Report Billed Rate TCB Jobed
on HAL 04/02/98 09:15 30 0 N 00022 N
02-0020 TC HAL «04/02/98 08:59 17 0 N 00100 00150 02500 a 04000
03 «0030 TC HAL =©——«-0.4/02/98 09:01 60 0 N 28760 02500 A 02999
04 0040 TC HAL «04/02/98 09:32 16 G N 00030 14000 02500 a 01999
05 0060 TC HAL 04/02/98 11:00 16 0 N 00050 00150 02500 A 01999
06 0070 TC HAL 04/02/98 10:30 16 0 N OG1l00 00100 02500 A 01999
Cmd3-Return Cmdl0-Totals C¢mdld4-Review by Technician
In WO# D Addr Date 0c P/O # Customer or Unit
00 RO00143 A 000004 040298 Oo Pat Rose Construction Co.
W/O Line SC Punch Jobe Job Code Description

9030 Tc 090136 02999
Stat Type Fid Report Billed Rate TP D Bill Comment
60 co oN 28760 02500

 

 

C1 Make the necessary changes and press [Enter]. The next line is displayed. You
can roll through the lines by pressing [Enter].


6 CHAPTER X5.11-5 e REVIEW BY WORK ORDER RELEASE 2.2

 

### Totals (~

O To check total hours reported and billed, press Cmd10-Totals.

 

   
    
    
  
    
  
  
   
  
 
 

A A&R EQUIPMENT SALES REVIEW BY WORK ORDER RO00143 X5B590-103

Ln D-Ln SC Tech Date WF Report Billed Rate TCB Jobed
ol HAL 04/02/98 ON 00022 N

02 0020 TC HAL 04/02/98 ON 06100 00150 02500 A 04000
03 0030 TC HAL 04/02/98 oN 28760 02500 A 02999
o4 0040 TC HAL 04/02/98 ON 00030 14000 62500 A 01999
05 0060 TC HAL 04/02/98 9 N 00050 00150 02500 A 01999
06 0070 TC HAL 04/02/98 ON 00100 00100 02500 A 01999

 

Total Hours
Reported Billed
3.02 431.60

 

Cmd3-Return Cmd10-Totals Cmdi4-Review by Technician

Ln W/O # D Addr Date oC P/O # Customer or Unit

00 ROO0143 A OC0004 040298 O Pat Kose Construction Co.

W/O Line sc Punch Joba Job Code Description (
0030 TC 090136 02999

Stat Type Fld Report Billed Rate T D Bill Comment
60 0 N 99999 28760 02500

 

O When all changes have been made, press [Cmd3).
01 Press [Enter] or [Cmd3] to return to the Work Order prompt.


 

The following labels appear at the top of the screen:

Ln
D-Ln

sc
Tech
Date
Time
St

Ww


Report

Billed

Rate

Jobed

Line number.
Document line. Line number on the point of sale
work order. On the Review by Work Order screen,
lines are displayed in order by document line.
Sales code.
Technician's 1D.
Date (mmddyy). Date on which work order was
opened.
Time of day (hh:mm). Punch-out time (without
seconds).
Time Clock status code.
Time Clock work type code.
Time Clock field (Y/N), indicating whether work
was done in the field.
Time reported in decimal equivalent. Two decimal
places assumed; for example, 350 means 3 hours
and 30 minutes. Can be negative.
Time billed in decimal equivalent. Two decimal
places assumed; for example, 350 means 3 hours
and 30 minutes. Can be negative.
Dollar amount. Rate at which work will be billed.
Two decimal places assumed; for example,
3750=$37.50.
T=Tax code
D=Discount code
Billing entity. The document default is used.
Individual lines, which may be different from the
document default are coded:

C or blank=Customer

EE Internal

 

 

W=Warrantor

 

 

 

N=Nop-billable.

Thermo King Job Code.

Fields on the detail lines are described below. Fields that can be changed are
designated as "Input." No other fields can be changed on the detail screen. Lines

cannot be deleted.

Ln

2 digit. Screen line number (columns 1-2).
Abbreviated as "Ln" on the top line. If you are
changing a line, enter its number here.


8 CHAPTER X5.11-5 ¢ REVIEW BY WORK ORDER RELEASE 2.2

W/O #

 

Work order number or "IN" for the first punch of C -
the day.

The following informational fields are furnished from the work order. No input or
changes are allowed in Time Clock.

D
Addr
Date

oc

P/IO#
Customer or Unit

1-character. Division code.

6 character address number of the customer.
Date (mmddyy). Date on which work order was
opened.

1 character. P.O.S. Status

 

 

V=Voided

Purchase order number.
Customer name or unit make, model, & serial
number.

W/O Line Line number on the point of sale work order. If
there is a prefix associated with the line number, it
is displayed in the space immediately on the left.

These fields are from Time Clock Entry: (

Sc 2 characters. The default sales code for the type of
line (CIW) is used. Default sales codes are set up in
Configuration.

Punch Elapsed time (hhmmss).

JobCd Thermo King job code

Job Code Description 29 characters.

Stat (Input) 2 digits. Time Clock status code. Abbreviated as
"St" on the top line. Status codes are set up in Table
Maintenance. Example: 10=Lunch, 20=Break,
99=Job Complete, etc.

Type (Input) 1 digit. Time Clock work type code. Abbreviated
as "W" on the top line. Work type codes are set up
in Table Maintenance. Example: 0=Regular,
1=Steam Cleaning, etc.

Fid (Input) Field (Y/N). Abbreviated as "F" on the top line. "Y"
means the work was done in the field and will be
charged at field rates.

Report (No input) Number of hours reported in decimal equivalent: for
example, 3 hours and 30 minutes is displayed as
350.

Billed (Input) Number of hours billed in decimal equivalent; for

example, enter 3 hours and 30 minutes as 350 and C


POINT OF SALE CHAPTER X5.11-5 « REVIEW BY WORK ORDER 9

press [Field Exit]. If hours billed are not entered,
the number of hours reported is used by default.
Hours billed are rounded according to the
configuration option only when the hours reported
default is used. If hours billed are entered directly,
the number is stored exactly as entered.

Rate (Input) Dollar amount at which hours will be billed. Leave
this field blank to use the default from the
technician's table, which is set up in Table
Maintenance. Enter $35.25 as 3525 and press [Field
Exit].

T (nput) Tax code. Tax codes follow the same tules as Point
of Sale Invoicing. If a tax code is entered on the
Time Clock detail line, it takes precedence. If not,
the tax code associated with the sales code is used,
If there is none, the tax code associated with the
customer is used.

D caput) Discount code. Discount codes follow the same
Tules as Point of Sale Invoicing. If a discount code
is entered on the Time Clock detail line, it takes
precedence. If not, the discount code associated
with the sales code is used. If there is none, the
discount code associated with the customer is used.

Bill Gnput) Billing entity. The document default is used,

Individual lines, which may be different from the
document default are coded:

C or blank=Customer

N=Non-billable.

Lines can be designated as Internal or Warrantor

only if the respective addresses have been entered

on the Sold To screen of the work order.
Comment (Input) 30 characters,


10 CHAPTER X5.11-5 « REVIEW BY WORK ORDER

Notes:

## CHAPTER X5.11-6

AUDIT REPORTS

### Introduction

In Configuration, you may select one audit report to be ran when Accounting End
of Day is run. You can also specify a printer for the Time Clock report to be
printed on. This may or may not be the same as the End of Day printer. Audit
Reports will be helpful to the Service Managers as they prepare to review the
day's work and make any necessary adjustments.

If the Thermo King dealer OPT (X63B-6) is on, Thermo King job codes are
included on the audit reports, but, due to space constraints, job code descriptions
are truncated to 24 characters on the By Technician report and 26 characters on
the By Work Order report. No subtotals or summaries by job codes have been
provided since this information is produced by Thermo Komm.

### Contents

ENTRANCE SCREEN ........csscsscossssssssstssessessesssssacsersaesocsonsrssssssassacsnesaneoens 2
BY TECHNICIAN ........s:ssssssssssctsssssssesssseesensnserscescessesseeeseentestenssneseaeseeasssons 3


2 CHAPTER X5.11-6 * AUDIT REPORTS RELEASE 2.2
oo
ENTRANCE SCREEN

O From the Time Clock Menu (X5-11), select option 6, Audit Reports. The
following menu is displayed.

A NW EQUIPMENT SALES & Time Clock Audit Reports 0 XBO15-000

1. By Technician
2. By Work Order

Select a Report:

Cmdi-cancel


POINT OF SALE CHAPTER X5.11-6 « AUDIT REPORTS 3

 

### By Technician

    

A NW EQUIPMENT SALES & Time Clock Audit Reports X5B60-001

By Technician

  
  
   
    
  

 

Technician ID (blank for all)...

Beginning Date (mmddyy).........

Ending Date (mmddyy) ..

  

 

    
 

Cmdl-Cancel Cmd3-Return to Menu

This report can be printed automatically at Accounting End of Day

(Configuration), and it can be requested at any other time. A sample report i
illustrated below.

Sample Time Clock Audit Report by Technician

ABR EQUIPMENT SALES ‘TOME CLOCK AUDIT REPORT Date 12/12/97
IPSWICH, SD s BY TECHNICIAN Time 23:44:26

OCUMENT/ DATE To JOB BILL FLD cIW coments
LINE JO CODE:

>>> TECHNICIAN: BONNIE BONNIE
In 32/17/1997

woes291 12/17/1997 8» PRELIMINARY DETERMINATION
9020 ‘STANDARD
WO4s291 12/17/1997 ASSISTANCE

9030 ‘STANDARD. RGR T-STAT/THERMOMETER REL
wOdS291_ 12/17/1997 9:10: ASSISTANCE

‘0040 ‘STANDARD . CHECK &/OR ADJUST CALTBRAT

CHECK OUT THERMOSTAT

wO%s291 12/17/1997 10:38: ASSTSTANCE. w
9050 ‘STANDARD. RER ULE. T-SPAT (INCL CALI
WOdS291 12/17/1997 11:35: ASSISTANCE w

‘0060 ‘STANDARD RGR T-STAT CONTROLLER,
Wo4s291 12/17/1997 LUNCH N

woa5291 12/27/1997 ‘TEST 4
9070 ‘STANDARD 01095 PRESSURE TSST COOL SYS.
WOaS291 12/27/1997 14:35: ASSISTANCE

w
3080 ‘STANDARD. 02002 RAR COMPR. SEAL ( INCL. R
WO4S291 12/27/1997 16:40:14 30 ASSISTANCE w

2030 ‘STANDARD 02009 R&R COMPRESSOR
wWoa5291 12/27/1997 16:30:00 90 BREAK No BREAK


4 CHAPTER X5.11-6 e AUDIT REPORTS. RELEASE 2.2

wo4s291 12/17/1997 17:00:03 40 WORK COMPLETE. . 1.00 $1.00 w
0120 0 STANDARD $81.00 02010 ER COMPR. SO/PE (INCL. AD

TECHNICIAN SUMMARY: Bi

‘JOB

DOCUMENT HOURS % OF ERS NOT cD DESCRIPTION
BILLED REPORT BILLED

ONNIE BONNIE PEMBERTON <<<

woas7s1 «8.60 86.5% 2.58 : 10 PRELIMINARY DETERMINATION : : 0 STANDARD 9.94 200,00
TOTAL «= «8.60 86.58 2.58 : 30 ASSISTANCE : ee 9.94

 

The fields at the bottom of the report are:

Hours Billed Total number of hours billed.

% of Report Hours Billed as a percentage of Hours Reported

Hours Not Billed Total of time differences when Billed is less than
Reported, including non-billable status codes.

Hours Gained Total of time differences when Billed is greater than
Reported; that is, time billed that was not actually
worked.


POINT OF SALE CHAPTER X5.11-6 e AUDIT REPORTS 5

 

### By Work Order

A NW EQUIPMENT SALES & Time Clock Audit Reports X5B60-002
By Work Order

Work Order (blank for all)

Beginning Date (mmddyy) ..

Ending Date (mmddyy)

Cmdl-Cancel Cmd3-Return to Menu

 

This report is run for the current day. It can be printed automatically at
Accounting End of Day (Configuration), and it can be requested at any other time.
A sample report is illustrated below.


6 CHAPTER X5.11-6 « AUDIT REPORTS RELEASE 2.2

 

Sample Time Clock Audit Report by Work Order C ‘

MCGILL MANUFACTURING ‘TIME CLOCK AUDIT REFORT Date 12/17/97 Page 1
IPSWICH, SD s WORK ORDER: WO<529T. Time 13:44:50 xSB60~-2

LINE TECH PATE TH JOB BILL FLD HOURS HOURS RATE/ CI COMMENT/
REPCRT BILLED AMOUNT Jos CODE

WO: WOe5292  CUSTOMBA DOCUMENT
BORNIEL2/17/1997 12:45:31
BONNIEL2/17/1997 16:30:00


0020 BONNIEI2/17/1997 8:09:16
CHECK OUT THERMOSTAT
0030 BONNTEI2/27/1997 8:31:28
ReR T-STAT/THERMOMBTER R
0060 BONNTEI2/17/1997 9:10:48
CHECK £/OR ADJUST CALTBR
0050 BONNZEI2/11/1997 10:38:37
ReR ULE. T-STAT (INCL CA
0050 BONNZE12/17/1997 11:38:56

R&R T-STAT CONTROLLER
0070 BONNTEL?/17/1997 13:10:30

PRESSURE TES? COOL SYS

0080 BONNEEI2/17/1997 14:35:43

R@R COMPR, SEAL { INCL.
0030 BONNZEI2/17/1997 15:40:14
RER COMPRESSOR
0120 BOMNTE12/27/1997 17:00:03 WORK COMPLETE.
‘STANDARD
LABOR SUMMARY CUSTOMER: 00” WARRANTY: 8.60 INTERNAL:
$0200 $309.40

Raeaugeeeseuexsesszzge

RAR COMPR. 50/PE (INCL.

## CHAPTER X6-1

BACKUP & RESTORE FILES MENU

### Introduction

Options on the Backup & Restore Files Menu enable you to back up your
dealership's files and run divisional end of day jobs at night after everyone
is off the system. The automated backup runs Communications End of
Day for Case, during which the prices of Case/IH parts that were inquired
on during the day are updated (if they are in an updatable class).

Backup & Restore Files Menu

COMMAND
{c) DIS Corp.

RESTORE FILES

. Immediate Backup

- Work with Automated Backup Schedules
. Create Daily Backup Tapes

. Restore from Backup

+ Work with Backups

. Prepare Tape for Immediate Backup

. Return to Security & Configuration Menu

Ready for option number or command

Bee>


[| X6-1 BACKUP & RESTORE FILES MENU

Overview of Menu Options

Immediate Backup

An immediate backup is appropriate if you want to do a critical job, such
as monthly billing, in the middle of the work day. If a critical job is
already underway, immediate backup cancels itself; if not, the system
checks for active jobs and gives you a chance to ask people to sign off or
cancel the jobs manually. Although you may select immediate backup to
tape and initialize the tape at the same time, you will probably want to
request backup to disk and move it to tape later. A dedicated system is
required only during the backup to disk. Work can continue as backups are
moved to tape.

Work with Automated Backup Schedules

Use this option to schedule backups for each file set and end of day jobs
for each division. It is not necessary to repeat this initial setup work unless
you want to change the schedule or you add another division and need to
schedule end of day jobs for it.

Create Daily Backup Tapes

Use this option to initialize and label tapes that will be used for daily
backups. You may create tapes for as many days as you need. You will be
prompted to insert the next day's tape. You may use this option to create
backup tapes to replace ones you want to keep, such as the backups that
follow Monthly Billing, Accounting End of Month, or End of Year.

Restore from Backup

Use this option to restore a file set from disk or tape. The DIS Backup
system keeps a log of all backups that have ever been done and what
happened to them, whether they are on disk, tape, or have been deleted and
are unavailable. If the backup you want is on disk or tape, it can be


X6-1 BACKUP & RESTORE FILES MENU [= |

restored.

Altention! Customers who have used previous versions of the DIS
Business System: Restoring data files no longer involves deleting the file
set you are currently using; in fact, the option to Delete Data Files has
been disabled. If you need to remove a file set, such as Z-files
permanently, the Response Line can help you.

Restoring a file set is as simple as selecting the backup from a list in
Restore from Backup.

As long as you find out before the next backup, you can "undo" the
restore. Before a file set is restored, the system backs up the current file
set as an "Undo" save file and leaves it on the disk until the next regularly
scheduled automated backup. If you have restored the wrong backup or if
you simply want to return to the current data after running some reports
from an old backup, all you do is press a function key. See F10-Undo
Restore.

 

Work with Backups

Work with Backups maintains a log of all backups and where they are
(disk, tape, deleted, etc.). From this log, you can select any backup on disk
and delete it or move it to tape. Backups to disk are not deleted until they
are moved to tape or manually deleted. /t is important to be aware of
backups on disk and deal with them in a timely manner to prevent
problems with disk space.

Prepare Tape for Backup

You can save time by using this option to initialize tapes to have on hand
when you need to do an immediate backup.

SECURITY & CONFIGURATION


[«] X6-1 BACKUP & RESTORE FILES MENU c

### Case Communications & Backup

No jobs that use data files can be running during the DIS Business System
backup. The SupportPRO business system interface (BSI) is such a job
and it cannot be left active overnight or backup will fail. There is a BSI
Job active for each SupportPRO client. Every night before you leave,
follow these instructions to allow backup to complete.

O On each Rumba-DIS session, obtain a sign-on screen.
Q Stop Case Communications.
O Exit the SupportPRO application. This cancels the BSI job so backup
will complete.
0 Turn off the monitor, but leave the PC running. If you want to turn off
the PC at the end of the day, follow the instructions for exiting (
Windows.
To restart SupportPRO in the morning, find the SupportPRO CD icon
in the ABC group, and double-click on it. The SupportPRO application
will start.

RELEASE 2.2 LL


X6-1 BACKUP & RESTORE FILES MENU [=]

### Online Help

Online help is available throughout backup (except for option 6, Prepare
Tape for Immediate Backup).

Field Level

Online help is available for each field and for the screen. Field level help
is also called context-sensitive help. To find out more about a particular
field, place the cursor in the field you are interested in and press Fl=Help.
You can even get help about display fields, such as column headings, by
placing your cursor over the field and pressing Fl=Help. To close the field
help window, press [Enter] or F3=Exit or F12=Previous.

The following screen illustrates field level help on the Tape Volume field
in X61-5, Work with Backups.

SECURITY & CONFIGURATION


Online Help for Tape Volume

Move Saved File Set to Tape

File Set -t
Backed up on st 8/20/96

10:59:23

to Tape device
Tape Volume .
Initialize Ta ..

WSR.Backup Vol Id {sts} - Help

Tape Volume REQUIRED

Press F4=Prompt to select from a list of valid tape volume

IDs.

If you are working at a dumb terminal, the values are

More...

F2-Extended help  F10=Move to top F12=Cancel

F3sExit Fae +

Fl3=Information Assistant F20=Enlarge F24=More keys

 

O The presence of more text is indicated by the text, "More...," in the

bottom right corner. To see more text, press [PgDn].
O To read the text on the full screen, press F20=Enlarge.
© To retum to the application screen, press [Enter].


Enlarged View of Field Heip

A-DIS TEST Move Saved File Set to Tape DSIGPVR

USR.Backup Vol Id (sts) - Help

Tape Volume REQUIRED
Press F4é=Prompt to select froma list of valid tape volume IDs. :

If you are working at a dumb terminal, the values are displayed in a
numbered list with the cursor at the top. without moving the cursor, : .
type the number that corresponds to the item you want. The value is

retrieved automatically without your pressing Enter

 

T£ you are working at a PC, the values are displayed with selection

“muttons.* If you have a mouse, click on the button you want; otherwise,

use the arrow keys to move the bar to your selection and press the space :

bar. The value is immediately retrieved to the screen. :

Valid tape volumes are:

 

F2=Extended help F3=Exit help F10=Move to top Fl2=Cancel
Fl3=Information Assistant FidsPrint help : :

 

SECURITY & CONFIGURATION


|e | X6-1 BACKUP & RESTORE FILES MENU C

Screen Level

Hf you need more information about the screen, press F2=Extended help
while the field help window is open.

Extended Help

A-DIS TEST Move Saved File Set to Tape
Move Saved File Set to Tape - Extended Help
Further information

Position your cursor on one of the following topics and press the
Enter key.
Introduction : {
Detail screen
Function keys for Detail Screen
Screen fields for Detail Screen
Checks against other files

 

Introduction

This function allows you to enter fields for processing.

This screen is used to identify the tape device and tape volume
More...

F3sExit help Fl0=Move to top Fl2sCancel Fl3=Information Assistant
Fid=Print help

 

OD Note the presence of the text "More..." in the bottom right corner. You
can press [PgDn] to read the text, or press [Tab] to place the cursor
before "Introduction," then press {Enter].

LO


X6-1 BACKUP & RESTORE FILES MENU Le]

O To leave extended help, press F3=Exit to return to the application
screen.

F4=Prompt

In many places, you can press F4=Prompt to select from a list of valid
values for a particular field. In most cases, you will use 1=Select on
standard AS/400 lists. On a few fields, such as Tape Volume, which is
illustrated below, the process is different. Furthermore, the method of
selection is slightly different. Depending on the equipment and
configuration you're using, you will see one of the following displays.

. Tuesday :
. Wednesday :
Thursday

Friday
Saturday :
Sunday
Immediate :

 

Display 1 Display 2

Display 1 The items are numbered and the cursor is at the top of the
list. Without moving the cursor, find the value you want
and type its number to select it.

Display 2 If you have a mouse, click on the value you want;
otherwise, use the arrow keys to move the bar, then press
the space bar to select a value. In either case, the value is
retrieved immediately.

SECURITY & CONFIGURATION


[| X6-1 BACKUP & RESTORE FILES MENU

Position Prompts

AS/400 screens often present items in a list for your selection. Position
prompts are available on most screens to help you search for what you

want quickly and avoid paging through screen after screen of irrelevant
items in a list. Occasionally, they don't serve a real useful purpose, and
may be confusing until you realize what they are. See the screen below:

Select File Set Screen

A-DIS TEST Immediate Backup DSF8DFR

Position prompt

1sSelect

Opt File Description
Set
1 o£ Created from Conversion

- 2 Crested from Conversion

Fi=Exit F12=Previous

Usually, a dealer has only 1 or 2 file sets. To select | of them does not
require a search, but a position prompt is a standard part of the screen.
LC


X6-1 BACKUP & RESTORE FILES MENU ["]

### Security & Setup

The Backup security code is required for all options on the Backup &
Restore Menu. Since daily backups are automated, no security is required.

Setup work is minimal and consists of the following steps:

1) Use option 3, Create Daily Backup Tapes, to initialize and label tapes
that will be used for daily backups. Tapes are labeled MONDAY
through SUNDAY.

2) Use option 2, Work with Automated Backup Schedules, to select the

file set(s) you want to backup, a time, persons who will be notified to
insert the backup tapes, etc.

3) Also, in Work with Automated Backup Schedules, you will schedule

End of Day jobs by division. End of Day jobs are done after backup
and include:

Accounting End of Day. A S/36 printer ID can be designated.
Parts End of Day. A S/36 printer ID can be designated.

Index Rebuild. Indexes are rebuilt for the file set. If they have
already been run when the system processes a division, they will
not be run again. The following indexes are rebuilt: Marketing,
Point of Sale, Receivables, and Vendor.

4) If you want to initialize and label a tape to have on hand for immediate
backups, use option 6, Prepare Tape for Immediate Backup. Tapes can
be initialized at the time you do an immediate backup; however, it
makes the backup less immediate.

SECURITY & CONFIGURATION


[| X6-1 BACKUP & RESTORE FILES MENU co

COMMON QUESTIONS & ANSWERS

What's the Best Thing About Backup?

Backup is always done to disk first, provided there is enough space. An
immediate backup to disk takes about 10-20 minutes for an average file
set, and this is the only time you need a dedicated system. After that, the
backup can be moved to tape manually, which takes longer but does not
interfere with other work.

L


X6-1 BACKUP & RESTORE FILES MENU |

What Happens to Active Jobs?

Backup does not proceed as long as there are active jobs. Since there is
always a possibility that somebody will forget to sign off, you can set up
backup to warn users every 2 minutes and cancel active jobs after 10
minutes. Bear in mind that there is always a danger of losing valuable
data when jobs are canceled. See also the section on Case
Communications & Backup, which appears earlier in this chapter.

Backup will not cancel the following critical jobs:
= Monthly Billing

any terminal).

Post Source Documents

Accounting End of Month

Payables File Maintenance

General Ledger File Maintenance

Price Tape Update

Parts End of Month Procedures

Point of Sale End of Month Procedure

Restore Bearing Interchange

If critical jobs remain active, backup is canceled after 5 hours.

a
NOTE
The Point of Sale print job, DISPSPPnu (Pn=S/36 printer ID and u=file set
ID) is automatically canceled by a regularly scheduled backup; however, it is
often active at the time of an immediate backup. It can be canceled safely as
long as no one is using Point of Sale Invoicing.


SECURITY & CONFIGURATION


X6-1 BACKUP & RESTORE FILES MENU co

What's the Most Important Thing to Remember?

Put the right tape in the tape drive every night.

Reliable backups are your best insurance against disaster. Several
conditions govern successful backups. Assuming that critical jobs have
ended, the following conditions must be true for a successful backup:
i) A tape must be placed in the drive.

2) It must have the correct label.

3) The tape drive must be working.

If even one of these conditions is not true, the system backs up to disk,
provided there is enough room.

Are Backups to Disk OK?

Yes and no. Backups on disk are condensed and disk space will not
normally be a problem; however, old backups are not deleted
automatically. If backups are allowed to accumulate on your disk,
performance may suffer. At 90% of disk capacity, the system skips the
disk backup and attempts to back up to tape. If for any reason, the tape
backup is unsuccessful, you are left with no backup at all.

It is your responsibility to move disk backups to tape as soon as possible.

Backups are deleted as soon as they are successfully moved to tape or
when you manually delete them using the option, Work with Backups.

RELEASE 2.2 LL


X6-1 BACKUP & RESTORE FILES MENU [=]

If Backup Fails, What Do | Do?

Backup fails completely only when there is no available disk Space and no
tape or the wrong tape in the drive. First, move all old backups to tape in
Work with Backups. As they are moved to tape, backups are deleted from
the disk. If there are no backups on disk, find out what's wrong and free
space somehow. Make sure the correct tape is placed in the tape drive
before the next scheduled backup.

Which Tape Do | Use?

Backup uses a 24-hour clock (military time). Noon is 12:00; midnight is
24:00. Backup time is from 8:01 on the first day until 8:00 the next day.
The system expects Monday's tape from 8:01 A.M. on Monday until 8:00
A.M. on Tuesday. Files on backup tapes are active for 7 days. If active
files are found, backup will append (add to the end) the next backup.
After 7 days, the system will re-initialize the tape with the same label.

Examples. If backup time is scheduled for 23:59 on Monday, the system
expects Monday's tape and backs up Monday's data at one minute until
midnight. If backup is scheduled for 2:00, the system expects Monday's
tape and backs up Monday's data at 2:00 Tuesday morning. At 8:01
Tuesday morning, the system expects Tuesday's tape. If backup is
scheduled for 14:00 and it is Tuesday, the system expects Tuesday's tape.

SECURITY & CONFIGURATION


X6-1 BACKUP & RESTORE FILES MENU Co

What If I Forget the Tape?

Provided there is enough room, the DIS Backup System always backs up
to disk first. The disk backup is deleted only after backup to tape is
successful. If you fail to put in the tape, or if it is the wrong one, a backup
will be done to disk; however, you should move it to tape as soon as
possible.

How Will | Know If Backup is Not Successful?

When backups fail, messages are sent only to the 2 user profiles set up in
Work with Automated Backup Schedules (X61-2) and not to all
workstations. Messages received alert you to the following conditions: (

1) The wrong tape was in the drive and the system backed up to disk only.
Move the backup to tape ASAP using option 5, Work with Backups.

2) The system could not back up to disk, but backup to tape was
successful. This means your disk is over 90% full, and you need to free
some space ASAP. Failure to do so may impact performance. In
addition, if the system cannot back up to disk or tape in the future,
backup will fail completely.

3) Backup failed completely: no room for a backup to disk and no tape or
the wrong tape in the drive (or the tape drive is not operating).

How Do | Delete & Restore?

The option to Delete Data Files has been disabled. If you need to remove a
file set, such as Z-files permanently, the Response Line can help you. With
the new backup, restoring a file set is as simple as selecting the backup

RELEASE 2.2 LU


 

from a list in Restore from Backup. The DIS Backup system keeps a log
of all backups that have ever been done and what happened to them,
whether they are on disk, tape, or have been deleted and are unavailable.
If the backup you want is on disk or tape, it can be restored.

WARNING! If a backup appears in the list with a blank File Location
(neither On Tape nor On Disk), it could be incomplete and should not be
testored.

What if | Restore the Wrong Backup?

As long as you find out before the next backup, you can "undo" the
testore. Before a file set is restored, the syste backs up the current file
set as an "Undo" save file and leaves it on the disk until the next regular
backup. If you have restored the wrong backup or if you simply want to
return to the current data after running some reports from an old backup,
all you do is press a function key.

SECURITY & CONFIGURATION

### Technical Notes

Work with Backups is a log which lists all backups with the most
recent first. The list is maintained indefinitely, and there is currently no
way to remove items.

When backups are saved to disk, dealer files are saved in a special
library, DISSAVLIB. The files are deleted when they are moved to
tape; otherwise, they accumulate until the disk is full.

When a file set is restored, the current file set is saved temporarily in
DISSAVLIB but the files are deleted at the next backup.

The major job steps involved in a regularly scheduled backup occur in the
following order:

3)
2)
3)

4)
5)
6)

8)
9)

Hold the job queue (QBATCH)

Stop DISPOSPRT subsystem.

Check for critical jobs. Stop the backup process if critical jobs remain
active after 5 hours.

Check for active, non-critical jobs. Issue warnings and cancel them
after the specified time.

Allocate (lock) all files to be saved.

Run Backup in QCTL: Save current file set in DISSAVLIB. Save the
backup to tape, then delete it from DISSAVLI. If no tape is present,
issue warning message.

Delete the "Undo" save file from DISSAVLL, if any.

Deallocate (unlock) files.

Run End of Day Jobs.

10) Release the job queue (QBATCH).

## CHAPTER X6-3

OPT DIS MASTER MENU

### Introduction

DIS provides several options for some applications. These options have
been combined and grouped by application on the OPT DIS Master Menu.
When you select an application, such as Receivables, the options that are
available are listed on the screen.

To find out more about an option, type the number of the option, and press
the [Help] key. To return to the menu, press [Enter]. In this chapter you'll
find each menu followed by the help screens for each option.

When option switches are set in the DIS Library, they apply to all
divisions. In every case, the first option is the default: the standard
configuration for the DIS Library. You do not need to set any switches if
you prefer the first option. To print a list of your switch settings, use the
OPT Report (X6-13) in the DIS LIBRARY.

### How To Run

From the Security & Configuration Menu (X6), select option 3, OPT DIS
Master Menu. If you know exactly where you want to go, you can “menu
hop” by typing the nearest menu, such as X631, which is the General
Ledger Menu.


OPT DIS MASTER MENU (X6-3)

‘COMMAND
{c) DIS Corp

OoPTDIS MASTER MENU

. General Ledger 7. Receivables

. Marketing . Service Management
Parts . Units

- Payables + system


. Point of Sale

23. Return te Security and Configuration Menu

Ready for option number or command Cmdl-Resume job

 

RELEASE 2.1 LC


HELP KEY


Pressing the [Help] key at the Master Menu displays the following screen.

Help Text

COMMAND INQUIRY WH

OPT Master Menu

Various DIS program option can be permanently set for your dealership.
These options are grouped by application category.

1}
2)
3)
4)

Press ENTER to return to the menu.
Select the application you desire to change and press ENTER.
Options that are available to be changed will be listed on the screen.
Help text is available for each option and can be obtained by
a. selecting the mema option and

b. pressing the HELP key.

Press ENTER to return to the menu. Gmdl-Resume job
FJ=Exit F12=Cancel

 

SECURITY & CONFIGURATION


Notes:

## CHAPTER X6-4

LIST OF FILES ON DISK

### Introduction

List of Files on Disk shows you:

= all the files currently on the disk.
= all of the free space available on the disk.

For more information, see the CATALOG procedure in IBM's System
Support Reference Manual.

### How To Run

From the Security and Configuration menu, select option 4, List of Files
on Disk. The following screen displays:

Input-Output

64000

LIST OF FILES ON DISK ... DEFAULT IF BY LOCATION
TO LIST FILES ON DISK BY LOCATION, TYPE IN...

TO LIST FILES ON DISK BY NAME, TYPE IN

Enter missing parameter
NAME

 

Type NAME for an alphabetical list of files and libraries.

Type LOCATION for a list of files and libraries according to their location
on the disk.


X6-4 LIST OF FILES ON DISK a

 

Press ENTER.
RESULT:

A message will display naming the manner of listing, by name or location.
It also says the Catalog procedure is executing. The list will print.

Note:
Other methods for creating the same information include:
1. Type CATALOG and press ENTER.

2. Type SYSLIST CRT and press ENTER to put the data to CRT. {

Then type CATALOG and press ENTER. The result is a display of
the files on screen (saving you time and paper). The @ files list
before any other. (For example, within the Q files Q.@ lists before
Q.ADM.) When you have viewed the files and want to wrap up the
job, type in 0 (zero) in the number of lines to review question on
screen. Then to get the system output back to your printer, type
SYSLIST and press ENTER.

 

RELEASE 2.1 C

## CHAPTER X6-5

SECURITY AUDIT REPORT

### Introduction

This report identifies which users have correctly passed through the security gates
for Accounting, Payables, Receivables, Financial, Parts, Stock Order, Backup,
Communications, Configuration, Units, and Services since the jast time the
security code was changed. DIS recommends that security codes be changed often
using Security Maintenance (X6-6).

ENTRANCE SCREEN

1 At the Security and Configuration menu (X6), choose Option 5, Security
Audit Report. A message is displayed to let you know the report is being
printed. A sample screen is illustrated below.

 

$/36 PROGRAM MESSAGES

%65000

Printing the security audit report . . .


2 X6-5 « SECURITY AUDIT REPORT RELEASE 2.2

The printed report includes an informative legend of users and the security gates
they have used, An example of the report is illustrated below.

AGR EQUIPMENT Sales SECURITY AUDIT REPORT Date 10/07/37

Page 2
LYNDEN, WA A

Time 19.58.22 6500-202

An ‘x’ is @ column indicates that the user has correctly passed that security gate since the last time the security code
was changed using Menu X6 option &

supply the correct Security code each time that they are run. As a result, this chart does not indicate which users
have run these twe jobs.

DIS recommends that security codes be changed frequently.


x


require the user to correctly pass the security gate. Therefore, these options are
not included on this report.

## CHAPTER X6-6

SECURITY MAINTENANCE

### Introduction

A Division is usually a store. Security Maintenance allows you to add or
delete a division. Information associated with each division such as name
and address, security, etc is changed or supplied in Security Maintenance.
Master Security for the entire system can be changed in Security
Maintenance.

     

Note:

 
 
 

  

The master security screen, where division codes are established, also
controls the order in which divisions are processed by jobs which
affect more than one division, such as End of Day (X1-9) and
Combined End of Month Procedure (X1.10-2).

   
   

 
 

 

### Setting Up Master Security

Master Security is used to gain access to the division code information.
This is the main security code. With use of this code, any other
security information becomes available. Only persons with the highest
security level should be given this code.

THE MASTER CODE WILL BE @ UNTIL IT IS CHANGED THE
FIRST TIME

Since we have just informed all readers that the master security code
is @, it would be a good idea to change it.

At the Security Maintenance screen, type @ in the Division Code field.
The @ will not display until Enter is pressed. Press Enter.


[2] X6-6 SECURITY MAINTENANCE C .

The Security Maintenance screen will display with @ in the Master Code
field. The Division Code field will be blank.

The Master Code field is five characters long. You must use the @ in the
first position of the field. There are no exceptions. Select up to 4
characters, letters, or numbers for the rest of the code.

Take two print screens of the Master Code. They should be placed in a
safe place. We suggest the dealer principal's home or perhaps in a lock box
off the premises.

When the print keys have been made, press Enter. Your code is changed.

CO


ADDING A DIVISION

X6-6 SECURITY MAINTENANCE [=]

At the Security Maintenance screen, type the master code in the Division
Code field. Press Enter. The following screen displays:

Division code .
Master Code

Number of Stores .....

Store Codes:
1. Lieoo 2.
7. 8.
13. a.
19. 20.

### Security Maintenance X€600-101 1

 

The division codes are listed under Store codes. In the above example, we
have two divisions. To add a division, change the Number of Stores to 3
and press Field Exit. Type the new division code beside the number 3

under Store Codes.

The first letter of the division code is the bridge that ties all numbering
systems and parts to the division. For example, A in the division A1000, is
the first letter of all general ledger accounts. Cash is A100 and so on. The
first letter of the division code you choose must be the first letter of your
general ledger accounts. Use up to five characters.

SECURITY & CONFIGURATION


[| X6-6 SECURITY MAINTENANCE co

Note:

The order in which divisions are processed by jobs that affect more

than one division, such as End of Day (X1-9) and Combined End of
| Month Procedure (X1.10-2), is established on this screen. The order

can be changed at any time.

 

Take two print screens of this screen and put them in a safe place.

When Enter is pressed, the division is added.

### Changing A Division Code

At the Security Maintenance screen, type the master code in the Division
Code field. Press Enter.

To change a division code, type over the old division code. You cannot
change the initial alpha character. It must still be the first letter of your
general ledger accounts. For example, change B1000 to B. You do not
have to use all the spaces. The first letter is the bridge to your general
ledger accounts and parts. If you change the letter, the bridge is broken.

When the change is made, take two print screens of the screen and put
them in a safe place. Press Enter. The division code has been changed.

o


SETTING UP OR CHANGING INFORMATION FOR A
DIVISION

From the Security Maintenance screen, supply the Division Code for the
division to be accessed. Press Enter. The Security Maintenance screen
displays current information.

Division code: A SECURITY MAINTENANCE X6600-103 3

Name... LEE'S RENTAL COMPANY Enter Y¥ to delete
Extended Name

Address . . . . BIRCH BAY-LYNDEN RD

Extended Address

City State . . . LYNDEN, WA Postal 98264 Phone 360 354 S841

Security Codes: Accounting . . P Backup :
Communications ? Configuration . P Financial . |.

Parts Trans . . Payables
Steck Orders . Units .

Other Information: Interest Rate . Minimum Finance 100
Transfer Acct . A1800 Pay Check Prt . Last Bill Date 032295
Internal Addr . Warranty Addr . Default Vendor CaS

Receivable Mon 6 G/L Month... 5 Fiscal start
Parts Hist Days 000 Cancelled Acct A4970 Cancelled 1D

Payables Purge Date. 0194 (‘mry)

Enter-Continue

 

In field definitions, all decimals are assumed. Do not type the decimal
point. Example: 5.2 digits = five places in the field with two assumed

SECURITY & CONFIGURATION


[ «| X6-6 SECURITY MAINTENANCE

decimal places, such as 123.45.

### Fields & Descriptions

Name

Extended Name
Address
Extended Address
City, State

Postal

Phone #
Security codes

Interest Rate

Minimum Finance

28 characters.

15 characters.

20 characters.

20 characters.

20 characters.

9 characters. Some communications
software use the first position of the postal
(zip) code to determine whether yours is a
U.S. or Canadian dealer (a digit indicates a
U.S. dealer; a letter indicates a Canadian
dealer. This character is also used by vendor
to determine cost of the parts and by Service
Management to show distance in kilometers
or miles. If first character is blank, miles
will be the default.

10 characters.

5 characters each. Each security gate will
indicate which security code is necessary.
For example "Accounting" will appear in the
center of the screen when the accounting
security code is required. A security code
may be blank if no security is necessary.

5.2 digits. Type 18% as 01800. Field Exit is
required.

5.2 digits. Type $1.00 as 100. Field Exit is
required. This is the minimum service
charge on a receivables account. For
example, if $1.00 and calculated interest =
Co


Transfer Acct

Mos Pay Hist

Last Bill Date

Internal Addr

Warranty Addr

Default Vendor

Receivable Mon

SECURITY & CONFIGURATION


$.53, then $1.00 will be charged.
8 characters. General ledger account used
for transferring between divisions.
2.0 digits. Number of months of history to
be displayed on screen for each payables
vendor in Vendor Inquiry.
Date (MMDDYY). Most recent date on
which Monthly Billing (X11-8) was run.
Consult your support representative before
changing this field.
6 characters. Address # used at POS to
charge internal expense for courtesy service
charges. See the section Internal Charges in
INVOICING.
6 characters. Address # used at POS to
charge warranty portions of work orders.
See the section on Warranty Charges
INVOICING.
3 characters. Used as the default in most
parts jobs.
1 character. The current receivables month
or the month that billing will be run for.

1 - 9 for January - September

O = October

N= November
D = December

Z = Dealership does not use

Accounts Receivable


G/L Month

Fiscal Start

Parts Hist Days

1 character. Oldest open general ledger
month. Do not alter this character if you
have already posted balances to the general
ledger.

1 - 9 for January - September

O = October

N= November

D = December
1 character. Month in which the dealership's
fiscal year starts.

1 - 9 for January - September

O = October

N= November

D = December
3.0 digits. Optional field. You do not have to (
track this information. You can track sales
and retums on parts in inventory sold at
point of sale.

This is the number of days you wish to
track. Tracking this information takes a lot
of disk space. For example, say you ran 150
invoices a day with an average of 4 part
lines on each invoice. Tracking sales and
return information for 30 days would take
approximately 1100 blocks of disk space.
This is just an estimate.

If you do not have enough room to track this
information, leave this field blank. Filling in
this field will automatically start tracking the
information with the creation of your next


Cancelled Acct

Cancelled ID

GST Num
Cash Printer

Payables Purge Date

X6-6 SECURITY MAINTENANCE [2

Point of Sale batch.

8 characters. This field is displayed only
when the Journals OPT is on. General ledger
account for point of sale invoices that have
been cancelled. The invoice can be tracked.
A debit for zero dollars will be posted.

1 character. ID (document number) to be
used for cancelled documents.

14 characters. Canadian GST Number.

2 characters. This field is displayed only
when the OPT for Cash Printer is on. It is
not displayed when the OPTs for Cash
Tendering and Self Service Invoicing are on.
Printer ID for the strip printer that uses
continuous roll 40-character paper. May be
used for self service invoicing or cash
tendering.

4 characters. This field is copied from the
field of the same name in Payables File
Maintenance (X1.12-6). It indicates the date
at which payables history begins.

Before pressing Enter, take two print screens of the information on the
screen. Put them in a safe place. When the print screens have been made,

press Enter.

Cmd1 to end the job.

SECURITY & CONFIGURATION


X6-6 SECURITY MAINTENANCE ac

### Deleting A Division

From the Security Maintenance screen, fill in the division code of the
division to be deleted. Press Enter.

Type Y in the “Enter Y to delete field". Press Enter. The division is
deleted.

Tf the division was deleted in error, enter Y in the same field to
reinstate the division.

Cmd1 to end the job.

CC

## CHAPTER X6-7

INITIAL FILE SETUP

### Introduction

Initial File Setup allows you to:

= Create missing files. Initial File Setup adds missing files to an
existing file set. Data in existing files are preserved.

= Create all data files required for DIS programs, which includes: 0
Setting up Master Security and configuration for each division.

Note:

 

 

 

 

Restoring ACRS information, which is maintained in the
WFT and WIT files, from diskette or existing disk file, if
desired.

 

### How To Run

If you are supplementing an existing file set, use the corresponding User
ID at the Sign On screen. If you are building a new file set, use the
1-character ID you want to associate with the files at the Sign On screen.

From the Security and Configuration Menu (X6), select option 7, Initial
File Build. The following message is displayed:

### Initial File Build %6700-001

This job will build all necessary files for the DIS system.
Press ENTER to continue.


O To cancel the job, press [Cmd1].

O To continue, press [Enter]. If a partial file set, including u. MASTER
(u=your User ID, the 1-character identifier associated with your
company files), is on the disk, missing files are set up, and the menu
returns. The job is complete.

If there are no files on disk, the remainder of the screen is displayed:

### Initial File Build 6700-001

This job will build all necessary files for the DIS system.

You must first setup the master security code and assign the number of
stores and division codes. Then, setup your divisional information.

If you are unsure about how to do this, press Cmdi to cancel job and refer to
your documentation before proceeding.

If you are ready, press ENTER to contimue.

Press Cmdl to cancel job

O To continue, press [Enter]. A division code prompt appears.

 

 

 

For the division code, type an "at" symbol (@) and press [Enter]. The
"@" symbol is the original Master code, which may be changed here.

 
-


 

0 If you want to change the Master code, simply type the new code over
the existing code and press [Enter]. For no changes, simply press
[Enter]. The System Setup screen is displayed.

System Setup Screen

x6600-101

Division code
Master Code ....

Number of Stores

Store Codes:
1, bl000 62. aloco 3. Ln

cB 8. 9. 10.
1B. 14. 15, 16.

29. 20. 2. 22.

 

 

O) Type the number of stores or divisions you have, and press FIELD
EXIT.

Note:

To add a store later, use Security Maintenance (X6-6), which uses the
same screen.

 

O In the "Store codes” section, type codes for each division. The division
code must begin with a unique letter from A to Z. After the first letter,

SECURITY & CONFIGURATION


 

you may use from zero to 4 characters or numbers. Do not leave any
blanks in the code.

The first letter of the division code is the bridge that ties all numbering
systems and parts to the division. For example, A in the division
A1000, is the first letter of all general ledger accounts. The first ietter
of the division code entered on this screen must be the first letter of
your general ledger accounts, such as Accounts Receivable (A1110 and
11110). Use up to five characters.

Note:

| The order in which divisions are processed by jobs that affect more

} than one division, such as End of Day (X1-9) and Combined End of (
} Month Procedure (X1.10-2), is established on this screen. The order
| can be changed at any time.

 

O Press FIELD EXIT to go to the next field.

 

O When you have typed in all of your divisions’ codes, take two print
screens of this screen and put them in a safe place.

O Press [Enter]. The “Division code" prompt is re-displayed.

 

Ci At the prompt, type one of the division codes you entered on the
previous screen. The Security Maintenance screen for that division is
displayed.

RELEASE 2.1 LU


 

Division code:

A & R SALES & LEASING CO

Extended Name
Address

Extended Address
City State . .

Security Codes:
Commnications CcOMM_


. aX
Stock Orders

other Information:

Transfer Acct .
Internal addr .
POS Printer . . Pi
Receivable Mon 6
Parts Hist Days 060
GST Num

aiB00

Enter-Continue

+ BELLINGHAM, WA

SECURITY MAINTENANCE

. 288 WEST KELLOGG RD

Accounting

Configuration .
Parts Trans . .

Postal 98226,

Receivables . .

Interest Rate .
- 03
Warranty Addr .

Mos Pay Hist

Inv Head Lines

G/L Month . . .

Cancelled Acct
Log Printer .

1800

4970

x€600-103

Enter ¥ to delete

Phone 206 733 7620

Backup
Financial . . .
Payables
Service... .

Minimum Finance

Last Bill Date 031092
Default Vendor CAs
Spaces Left . . 5
Fiseal start . 1
Cancelled ID

 

 

 

O Furnish the information for the fields, which are defined below. Before
pressing [Enter], take two print screens of the information on the
screen. Put them in a safe place. When the print screens have been
made, press [Enter].

O System files are created, and the Initial File Build screen for WFT is
displayed.

SECURITY & CONFIGURATION


 

### Fields & Descriptions

In field definitions, all decimals are assumed. Do not type the decimal
point. Example: 5.2 digits = five places in the field with two assumed
decimal places, such as 123.45.

Name 28 characters.
Extended Name 15 characters,
Address 20 characters.
Extended Address 20 characters.
City, State 20 characters.
Postal 9 characters. Some communications
software use the first position of the postal
(zip) code to determine whether yours is a (

U.S. or Canadian dealer (a digit indicates a
U.S. dealer; a letter indicates a Canadian
dealer. This character is also used by vendor
to determine cost of the parts and by Service
Management to show distance in kilometers
or miles. If first character is blank, miles

will be the default.
Phone # 10 characters.
Security codes 5 characters each, Each security gate will

indicate which security code is necessary.
For example "Accounting" will appear in the
center of the screen when the accounting
security code is required. A security code
may be blank if no security is necessary.

Interest Rate 5.2 digits. Type 18% as 01800. Field Exit is
required.
Minimum Finance 5.2 digits. Type $1.00 as 100. Field Exit is

RELEASE 2.1 LO


Transfer Acct

Mos Pay Hist

Last Bill Date

Internal Addr

‘Warranty Addr

Default Vendor

POS Printer

SECURITY & CONFIGURATION


required. This is the minimum service
charge on a receivables account. For
example, if $1.00 and calculated interest =
$.53, then $1.00 will be charged.

8 characters. General ledger account used
for transferring between divisions.

2.0 digits. Number of months of history to
be displayed on screen for each payables
vendor in Vendor Inquiry.

Date (MMDDYY). Most recent date on
which Monthly Billing (X11-8) was run.
Consult your support representative before
changing this field.

6 characters. Address # used at POS to
charge internal expense for courtesy service
charges. See the section Internal Charges in
6 characters. Address # used at POS to
charge warranty portions of work orders.
See the section on Warranty Charges
3 characters. Used as the default in most
parts jobs.

2 characters. Point of Sale Printer. Use the
printer identification from a system
configuration report.


Inv Head Lines

Number Left

Receivable Mon

G/L Month

2.0 digits. Number of lines of heading that
will print after each invoice. Allows the
perforation of the invoice to be high enough
to tear off. The rest of the heading prints as
part of the next invoice. Field Exit is
required. See the table below.

1.0 digits. Number of spaces the invoice
needs to be moved to the left. Depends on
the printer being used. See the table below:
For printer. Heading: Lines Left:

IBM 5256 9 0
IBM 4214 12 0
IBM Pro 12 5
Okidata 320 8 5

1 character, The current receivables month
or the month that billing will be run for.
1- 9 for January - September
O = October
N= November
D= December
Z = Dealership does not use
Accounts Receivable
1 character. Oldest open general ledger
month. Do not alter this character if you
have already posted balances to the general
ledger.
1-9 for January - September
O = October
N = November
D = December

RELEASE 2.1 nail


Fiscal Start

Parts Hist Days

Canceled Acct

Canceled ID

GST Num

SECURITY & CONFIGURATION


 

1 character. Month in which the dealership's
fiscal year starts.

1 - 9 for January - September

O = October

N=November

D = December
3.0 digits. Optional field. You do not have to
track this information. You can track sales
and returns on parts in inventory sold at
point of sale.

This is the number of days you wish to
track. Tracking this information takes a lot
of disk space. For example, say you ran 150
invoices a day with an average of 4 part
lines on each invoice. Tracking sales and
return information for 30 days would take
approximately 1100 blocks of disk space.
This is just an estimate.

If you do not have enough room to track this
information, leave this field blank. Filling in
this field will automatically start tracking the
information with the creation of your next
Point of Sale batch.

8 characters. General ledger account for
point of sale invoices that have been
canceled. The invoice can be tracked. A
debit for zero dollars will be posted.

1 character. ID (document number) to be
used for canceled documents.

14 characters. GST Number.


X6-7 INITIAL FILE SETUP : _

Log Printer 2 characters. Printer ID for the printer where
Point of Sale documents are printed when
they are held (Cmd4).

Initial File Build Screen (WFT)

The following screen pertains to the file, WFT, which is furnished on a
diskette from DIS. The WFT file is necessary for calculating fixed asset
depreciation.

### Initial File Build 6700-003

This job will build all necessary files for the DIS system.

Copy file "wrt" for fixed asset depreciation. You may copy from diskette or
fixed disk, (

If you do not have a copy of this file you may press Cmd2 to skip
this step and continue building other files.

Copy from diskette or disk
1 - diskette (put diskette into slot Sl}
2 - disk

Name of file to copy from

Press Cmd2 to skip this step

 

If you do not want to install WFT at this time, press [Cmd2] to skip this
step; otherwise, complete the screen as follows:


 

Copy from diskette or disk If you have a diskette containing WFT,
jeave the default of "1." If you are setting
up an additional user ID and a WFT file for
the original user ID is on your disk, type "2."

Name of file to copy from _If you have a diskette containing WFT,
leave the default of "WFT." If you are
setting up an additional user ID and a WFT
file for the original user ID is on your disk,
type: "u.WFT" where u=original user ID.

 

 

 

When the screen is complete, press [Enter]. The WFT file is copied. A
similar screen pertaining to the file, WIT, is displayed.

 

Initial File Build Screen (WIT)

The following screen pertains to the file, WIT, which is furnished on a
diskette from DIS. The WIT file is necessary for calculating fixed asset
depreciation.

SECURITY & CONFIGURATION


X6-7 INITIAL FILE SETUP —

 

### Initial File Build X6700-004

This job will build all necessary files for the DIS system.

Copy file “WIT” for fixed asset depreciation. You may copy from diskette or
fixed disk.

Tf you do not have a copy of this file you may press cmd2 to skip
this step and continue building other files.

Copy from diskette or disk
1 - diskette (put diskette inte slot si)
2 - disk

Name of file to copy from

Press Cmd2 to skip this step

 

O If you do not want to install WIT at this time, press [(Cmd2] to skip this
step; otherwise, complete the screen as follows:

Copy from diskette or disk If you have a diskette containing WIT, leave
the default of "1." If you are setting up an
additional user ID and a WIT file for the
original user ID is on your disk, type "2."

Name of file to copy from _ If you have a diskette containing WIT, leave
the default of "WIT." If you are setting up
an additional user ID and a WIT file for the
original user ID is on your disk, type:
“u.WIT" where u=original user ID.

L


 

C) When the screen is complete, press [Enter]. The file is copied and the
Security and Configuration Menu is displayed.

SECURITY & CONFIGURATION


Notes:

RELEASE 2.7 LO

## CHAPTER X6-9

APPLY ENHANCEMENTS

### Introduction

Apply Enhancements allows you to:

= modify your DIS System with the most recent PTF (Program
Temporary Fix) updates from DIS.

= apply a Communications and other modules.

= apply custom code.

Run this job from the system console. Make sure no one else is signed on
to the DIS library. Store the diskette(s) or tape carefully in case you need
them again.

Communications MODs can often be used for the next release of the DIS
Library. You can avoid unnecessary charges by keeping them where you
can find them. Always check the product number to make sure they are
compatible with new releases.

When a PTF is applied through this option, the system will automatically
sign the session off when it is completed. When you sign back on, you will
be ENV’d to the file set you were using when you applied the PTF.


X6-9 APPLY ENHANCEMENTS C .

### How To Run

From the Security and Configuration menu, select option 9, Apply
Enhancements. After the Security Gate, the Apply Enhancements screen
appears with the device prompt.

x6900-C01

This job will place new programs into your DIS library,

No other user should be signed on to the system.
There should be no active jobs on the user board.

This procedure should be run from the system console.

Carefully respond to all messages.

Keep all diskettes and tapes organized and properly labeled. {

Please specify device (S1/TC): $1 $1 - diskette slot 1
WW - tape cartridge

Cmdi-End job Enter-Continue

 

O Type SJ if you are using diskettes, or TC if you are using a tape
cartridge. Press [Enter].

CO Follow the prompts on screen, which will guide you through the job.
When the modifications are complete, store the diskette(s) or tape in a
safe place.

=

## CHAPTER X6-9

APPLY ENHANCEMENTS

### Introduction

Apply Enhancements allows you to:

= modify your DIS System with the most recent PTF (Program
Temporary Fix) updates from DIS.

= apply a Communications and other modules.

= apply custom code.

Run this job from the system console. Make sure no one else is signed on
to the DIS library. Store the diskette(s) or tape carefully in case you need
them again.

Communications MODs can often be used for the next release of the DIS
Library. You can avoid unnecessary charges by keeping them where you
can find them. Always check the product number to make sure they are
compatible with new releases.

When a PTF is applied through this option, the system will automatically
sign the session off when it is completed.

### How To Run

From the Security and Configuration menu, select option 9, Apply
Enhancements. After the Security Gate, the Apply Enhancements screen
appears with the device prompt.

APPLY ENHANCEMENTS x6200-001

This job will place new programs into your DIS library.

No other user should be signed on to the system

There should be no active jobs on the user board.

This procedure should be run from the system console

Carefully respond to all messages.

Keep ail diskettes and tapes organized and properly labeled. (

Please specify device (S1/TC): 51 $1 ~ diskette slot 1
TC - tape cartridge

Cmdl-End job Enter-Continue

 

 

(3 Type SJ if you are using diskettes, or TC if you are using a tape
cartridge. Press [Enter].

O Follow the prompts on screen, which will guide you through the job.

When the modifications are complete, store the diskette(s) or tape in a

safe place.

CO

## CHAPTER X6-10

PREPARE PARTIAL PROCEDURE

### Introduction

Prepare Partial Procedure is used to recover certain jobs that did not
complete. For example, you may be in the middle of a job and the
electricity goes off. Most jobs now have recovery procedures that display
when they fail.

DO NOT ATTEMPT THIS JOB WITHOUT CALLING DIS. THIS IS
NOT A JOB FOR YOU TO RUN WITHOUT OUR TECHNICAL
SUPPORT.


Notes:
Cc

CO

## CHAPTER X6-11

DIS BUSINESS SYSTEM SETUP

### Introduction

The DIS Business System Setup can perform the following tasks:

Reload the DIS Library

Load a fresh copy of the Query dictionary

Convert a new file set, such as a newly acquired dealership
Load an auxiliary PTF (Apply Enhancements could be used as
well)

= Load the sample company files (Z-files)

The setup option can do all this without much help from you. It is so
self-sufficient that it comes with an Express setup. For more complicated
and unusual situations, there is a Custom setup.

Note: Screen illustrations in this chapter apply to Release 1.4. Screens will
be slightly different for each release.

### How To Run

A dedicated system is not required for the following steps.

O Sign on as QSECOFR.

 

 

 

From the Security and Configuration Menu (X6), take option 11, DIS
Business System Setup. Pass through the security gate. The following
screen appears.


X6-11 DIS BUSINESS SYSTEM SETUP c

DIS BUSINESS SYSTEM SETUP
Welcome to the DIS Business System Setup program.

This program allows you to install all or some of the components
which make up the AS/400 V9L0/1.4 DIS Business System.

You will be prompted to make a decision regarding each aspect of the
installation. In most cases, the system will choose the correct

option for you. If you change your mind about one of the questions,
press Cmd3 to step backwards through the setup screens.

Press Enter to continue.

emdi-Cancel setup

 

The purpose of the screens that follow is to create a list of tasks that the
setup program will run. No changes will be made until you have a chance
to review the list. Press [Enter] to continue.

L.


Selecting a Setup Method

### Dis Business System Setup Setup-002

Two options are available for DIS Business System Setup.

Express Setup During express setup, the system will automatically
make most of the 1.@ setup decisions for you. After
the system has made its recommendations, you will be
presented with 2 list of setup tasks to be performed.
This option is ideal for a routine upgrade from an
earlier version of the system.

Custom Setup During custom setup, the system will present a series
of questions in order for you to customize which
modules will be affected by the 1.4 setup programs.
Use this option if you desire greater control over
the setup process

1. Express setup
2. Custom setup

Enter setup option: 2

 

Enter-Continue Cmdl-Cancel setup

 

Select the method you want to use. DIS recommends the Express setup,
which requires fewer decisions on your part.

What happens next depends on the type of setup you choose and the
version of the DIS Library and file set(s) on your disk. If you choose
Express, the setup makes decisions for you and displays the list of
proposed tasks. All complete file sets will be scheduled for conversion.
Replacement sample company files (Z-files) will be loaded. You will be
prompted only if the program needs information that pertained to a
previous version, such as a tax code to replace a blank tax code, which is

SECURITY & CONFIGURATION


X6-11 DIS BUSINESS SYSTEM SETUP co

no longer valid. If you are upgrading from V8LSA for the AS/400, there
are no additional prompts.

If you choose Custom, you'll step through a series of screens. On the left,
you'll see the list of selected tasks; on the right, a statement or question
pertaining to the next task.

DIS BUSINESS SYSTEM SETUP SETUP-102
Selected setup tasks

As you work through the questions Tae existing DIS software
on the right half of the screen, library on this machine is
the setup tasks you have chosen an earlier release than 1.4.
will be listed here on the left.
The 1.4 library will be
loaded from tape and will (
replace the existing library.

Press Enter to continue.

€mdi-Cancel setup Cmd3-Back

 

Co


The Completed Task List

Both Express and Custom setup methods end with a screen like the one
below, where the proposed tasks are listed on the left and exit options are
presented on the right.

DIS BUSINESS SYSTEM SETUP SETUP-CO1

Selected setup tasks NW

It
Replace old library with 1.4 library [| The setup tasks listed on
Convert ¢ files from V8LSA i the left side of the screen
Change AS/400 values for 1.¢ and up || have been selected to perform.
Load auxiliary tape into 1.4 It
Load QRYi.4 data dictionary i Select one of the following
Relcad 2 files i options:

i 1 - Exit the setup program

li but retain all selected
tl tasks information for

l running at a future time.
Il 2 - Proceed with the disk
il space analysis (may take
ti up to 30 minutes.)
iI
i Option: 2
I
Wt Press Enter to continue.
il
Cmil-Cancel setup Cmd3-Back

 

You may step backwards in the task list by pressing Cmd3-Back. For
example, if you prefer to convert your Z-files instead of reloading new
ones, press Cmd3-Back, which will allow you to select the option to
convert rather than reload. By pressing [Enter] to continue, you can move
forward and return to the screen illustrated above.

SECURITY & CONFIGURATION


[«] X6-11 DIS BUSINESS SYSTEM SETUP Co

Exit Options

1 - Exit the setup program but retain al] selected tasks information for
running at a future time.

Signs off as QSECOFR. Preserves the task list. To re-enter, use the
LODRUN command.

2 - Proceed with the disk space analysis (may take up to 30 minutes)

DIS recommends this option as a preliminary assessment of disk space. At
the end, you will have another opportunity to save the task list and exit.

Descriptions of Task List Options (

Replace old library with 1.4 library
For the setup, this is not an option. It is the goal.

Convert C files from VnLn
Complete file sets, which have not been converted to 1.4 are listed. Again,
this is what the setup is designed to do.

Change AS/400 values for 1.4 and up

For each release, beginning with V8L4B, some system values have had to
be changed. The setup will elect to change values beginning with the
release you are currently using plus those up to and including Release 1.4.

Load auxiliary tape into 1.4
Last minute changes and bug fixes are included on auxiliary tapes. If you
have an auxiliary tape, make sure this task is on the list.

Lu.


X6-11 DIS BUSINESS SYSTEM SETUP.

 

Load QRY1.4 data dictionary

If you have a catalog of files on your disk, look at the Q section for aQRY
entry. Or, maybe you know that your dealership uses Query to create
reports. The Query dictionary is small, and it can be deleted later. If you're
unsure and disk space is not a problem, go ahead and load it.

Reload Z files
The Z-files are for a sample company. Some dealers don't use the Z-files at
all; others depend on them and enter their own data to experiment with.

The setup program will put loading or reloading Z-files on the task list. If
there were no existing files, you may go back and choose not to load them.
If Z-files were found, you may go back and decide to do one of the
following:

1) Delete the files and restore a fresh set

2) Convert the existing files to 1.4
3) Ignore the files. If you do so, they will not function properly with 1.4.

Disk Space Analysis

 

You are encouraged to proceed with the disk space analysis at this time.
The system analyzes your current disk usage and estimates what you'll
need for Release 1.4 features. The goal is to keep disk usage under 85%.
The feature in the new release that uses the most disk space is Part Sales
History. The next screen will let you know that one of the following
conditions has been found:

Thumbs down. There is not enough disk space to install all of the selected

features. You can press Cmd3-Back to remove tasks, such as the Query
dictionary and Z-Files.

SECURITY & CONFIGURATION


Le] X6-11 DIS BUSINESS SYSTEM SETUP C~

Maybe. There is enough disk space to install all features, but you need to
lower the number of months of part sales history. You will be presented
with a screen that allows you to select the number of months of part sales
history. You can change the number until the 85% capacity has been
reached.

Thumbs Up! There is enough disk space to install all features, including
part sales history, and keep disk usage under 85%.

CC


Thumbs Down

### Dis Business System Setup

You are currently using 83.7% (6586M) of the total disk space.

The DIS Business System Setup program has estimated that the tasks you
have selected to perform will result in a utilization of 91.38 (7184M)
ef your total disk space

This is in excess of the acceptable disk space utilization limit of

85.08 (6689M). The DIS Business System Setup programs cannot complete
at this time.

It is probably a good time to begin thinking about purchasing more disk
space for your system. In the meantime, please fax a cataicg to the
Response Line who will try to help you find cbjects which can be
deleted from your system.

Press Crdi to cancel setup or press Cm? to return to the selection
of tasks to be performed.

€mdi-Cancel setup Cmd3-Return to task selections

 

Depending on how much the estimate exceeds 85%, you may cancel or
press Cmd3-Return to task selections. After you have revised the task list
by omitting items, such as loading the Query dictionary or Z-files, the
system will recalculate the utilization percentage and display one of the 3
utilization screens.

SECURITY & CONFIGURATION


 

Maybe

### Dis Business System Setup Setup~Z03

You are currently using 83.7% (6586M) of the total disk space.

The DIS Business System Setup program has estimated that the tasks you
have selected to perform will result in a utilization of 91.3% (7184M)
of your total disk space.

This is in excess of the acceptable disk space utilization limit of
85.0% (6689m) .

Disk space utilization can be altered by reducing the number of months

of part sales history to be converted for 1.4. Bach month of part

sales history will affect your disk space utilization by

approximately 4.2% (0330M}. (

Number cf months of parts sales history to convert for 1.4 (0-36): 24

Press Enter to revise the disk space utilization estimate.

Enter-Revise estimate Cmd3-Return to task selections

 

Type a number of months and press [Enter] to allow the system to
recalculate. Repeat until you receive the Thumbs Up screen illustrated
below.

CL


Thumbs Up!

DIS BUSINESS SYSTEM SETUP SBTUP-z02

You are currently using 64.7% (5091M) of the total disk space.

The DIS Business System Setup program has estimated that the tasks you
have selected to perform will result in a utilization of 73.0% (5744M)
of your total disk space.

This is below the acceptable disk space utilization limit of 85.0%
(8689M). To proceed with the performing of the setup tasks, make sure
that no one else is using the system, and press Cmd2.

Cmdl-Cancel setup Cmd2-Perform setup tasks

 

   
 
  

WARNING! Do not press Cmd2-Perform setup tasks now unless you
have backed up your data files and DIS Library and have a dedicated
system.

 
    

O Press Cmd1-Cancel setup. This will not cancel the task list, but it will
allow you to exit and do the following tasks:

= Make sure you have a dedicated system.
= Backup your data files.

SECURITY & CONFIGURATION


| X6-11 DIS BUSINESS SYSTEM SETUP co

= Backup your DIS Library.

O Initialize a tape just as you do for daily backup.

O Ata menu, type: SAVLIB and press [F4]. Furnish the name of the
Library, which is LIBRARY; and the device, which is TAPO1. The
other defaults are OK. Press [Enter].

Save Library (SAVLIB)

Type choices, press Enter.

Name, *NONSYS, *ALLUSR, *IBM

Name, *SAVF
+ for more values

Bottom
F3sExit Fa=Prompt FS5=Refresh F10=Additional parameters F12sCancel
Fl2-How to use this display F24=More keys

Parameter LIB required.

 

O When you have completed the backups, sign on as QSECOFR.

 

 

 

 

Select option 2 to repeat the disk analysis. When the following screen
appears, press Cmd2-Perform setup tasks.

Lo

### Dis Business System Setup

You are currently using 64.7% (5091M) of the total disk space.

The DIS Business System Setup program has estimated that the tasks you
have selected to perform will result in a utilization of 73.0% (5744M)
of your total disk space.

This is below the acceptable disk space utilization limit of 85.0%
(8689™). To proceed with the performing of the setup tasks, make sure
that no one else is using the system, and press Cmd2.

Cndi-cance? setup Cmd2-Perform setup tasks

  

No further input will be necessary. When the installation and conversion
are complete, the system will sign off as QSECOFR.

SECURITY & CONFIGURATION


Notes:

## CHAPTER X6-12

POINT OF SALE SECURITY

### Introduction

Point of Sale Security is installed through the DIS OPT Library (Point of
Sale Menu 7, option 4). It is used to set up User IDs and passwords that
control what the user is allowed to do on a Point of Sale document. A
report, which can be used without POS Security, is printed at Parts End of
Day. Controlled functions are:

= Reopening documents
= Cancelling documents
= Using all sales codes

The first option within Point of Sale Security, Users Maintenance,
provides for the setup of User IDs and passwords and specifies which of
the controlled functions are allowed.

Users who are not allowed to use all sales codes can be restricted to
specified sales codes. See "Sales Codes By User Maintenance."

User IDs are required on the Point of Sale "Sold To" screen, which is
illustrated below. The User ID and Password are required to gain access to
the detail screen.


X6-12 POINT OF SALE SECURITY ey

A & R SALES & LEASING CO INVOTCING-SOLD 70 X5100-105 4
Document classification
REPAIR ORDER # R000108 CHARGE OPEN, 4/07/92
Sold to: CURRO2 Ship te:
MEREDITH § CURRY
919 273 2812
2508 TIMBER LANE

GREENSEOR, NC 27408

User ID, Password,

Ship By________ Sold By STAROI ?.0.4, Add Date 4/07/92
Sales Code__ ‘Transfer _ Quantity Break Pricing N Print Date

Tax Number, GST Method © ‘Trans Date
Periodic Type __ Periodic Frequency 99

Make Model Year Serial Number Warranty

Balance current 31-66 61-90 {
00 00 00 -00
Internal address
Cregit Limit Peak Bal Beg Date or unit #2

900000 2000 5/15/91 Warranty Address #:

 

LL


X6-12 POINT OF SALE SECURITY [=]

### How To Run

From the Security & Configuration Menu (X6), select option 12, Point of
Sale Security. Following the Configuration security gate. the Point of Sale
Security menu appears.

A & R SALES & LEASING co POINT OF SALE SECURITY X8C00-101
Division A

1. Users Maintenance

2. Sales Codes By User Maintenance

Enter An Option : _

Cmdl-End Job

 

SECURITY & CONFIGURATION


[ «| X6-12 POINT OF SALE SECURITY Cc

### Users Maintenance

 

C] To set up user IDs, select option 1, Users Maintenance. A User prompt
appears, as illustrated on the following page.

 
  

       

A & R SALES & LEASING CO POINT OF SALE SECURITY
Division A Users Maintenance

x6C00-102

     
   
 

User :

 

 

Gmd1-End Job,

  
 

cmd3-Return,

 

0 Type a User ID (up to 8 characters) and press [Enter]. The Users
Maintenance screen appears.

o


X6-12 POINT OF SALE SECURITY [=]

A&R SALES & LEASING CO POINT OF SALE SECURITY x6C00-103
Division A Users Maintenance

User : EBS
Password :
Reopening Of Documents .. :

Cancellation Of Documents :

All Sales Codes

Enter 'Y' To Delete

cmd3-Retura

 

OQ Assign a password (up to 4 characters).

 

 

 

Type ¥ to allow the user to reopen or cancel documents or use all sales
codes. To restrict the user from one or more of these functions, type N.
If the user is not allowed to use all sales codes, use option 2, Sales
Codes By User Maintenance, on the Point of Sale Security Menu to
specify the ones that can be used.

 

O Press [Enter] to record your selections or press [Cmd3] to return to the
User prompt.

CO To end the job, press [Cmd1] from the User prompt. The following

SECURITY & CONFIGURATION


[ «| X6-12 POINT OF SALE SECURITY Cc

message is displayed: “Enter "Y' to print the P.O.S. security report." If
you want the report, change the default of 'N' to "Y'. An example of the
report follows:

ASR SALES & LEASING
Division a
ser open Canc. all

SC Resczipsion

7.0.8. Securizy Report Pate: 4/24/92 Page 1
Tine: 3 X6C00-2A,

 

yoy

yoy
ROVE ON ACCOUNT
PARTS CUSTOMER
MESCELLANEOUS

 

LO


X6-12 POINT OF SALE SECURITY [7]

### Sales Codes By User Maintenance

 

 

 

For users who are not allowed to use all sales codes, select option 2,
Sales Codes by User Maintenance to assign the sales codes they are
allowed to use. A User prompt appears, as illustrated below.

 

Ag R SALES & LEASING CO POINT OF SALE SECURITY XECOO-1046
Division A Sales Codes By User

User :

Sales Code : __

Cmdl-End Job, Cmd3-Return

 

oO

Type the User ID, which was assigned in option 1, Users Maintenance.

 

 

 

 

Type the first sales code that will be allowed, and press [Enter]. The
description of the sales code is displayed.

SECURITY & CONFIGURATION


X6-12 POINT OF SALE SECURITY oe

 

A & R SALES & LEASING CO POINT OF SALE SECURITY X6C0O-105
Division & Sales Codes By User

User : EBS

Sales Code : 2S

Description . : MISCELLANEOUS

Enter ‘¥' to Delete

cmd3-Return

 

 

 

Press [Enter] to complete the assignment.

O Repeat the process for other sales codes.

 

 

 

To end the job, press [Cmd1] from the User prompt. The following
message is displayed: "Enter "Y' to print the P.O.S. security report." If
you want the report, change the default of 'N' to 'Y". The report is
illustrated in the section, "Users Maintenance."

 

LL

## CHAPTER X6-13

OPT REPORT

### Introduction

The OPT report lists the current option settings from the DIS OPT Library.
All options are listed including those which retain their default settings.
For a complete description of all options, refer to OPT DIS Master Menu
(X6-3).

### How To Run

From the Security and Configuration Menu (X6), select option 13, OPT
Report. Following the Configuration security gate, the report is placed
directly on the job queue.

An example of an OPT Report follows. The number of the OPT menu and
the number of the selected option are printed on the right side of the
report. For example, the following option is on the second Parts menu
where it is option 4 (Parts, 2-4):


Notes:

## CHAPTER X6-15

ELECTRONIC COMMERCE MENU

### Introduction

Transfers between the AS/400 and the PC are handied by DIS Electronic
Commerce Manager (ECM) on the AS/400 and DIS Electronic Commerce Client
(ECC) on the PC. The options on this menu pertain to DIS Electronic Commerce
Manager; however, instructions for configuring the Client for the following
manufacturers’ communications software are included in CHAPTER X6.15-1:

= AGCO Solutions™ On-Line

= Clarknet III

= KubotaLink

= Ingersoll-Rand

= New Holland DCS)

The table below shows the transactions supported by each manufacturer:

Manufacturer’s . Parts
Communications ‘inan. Locator
Package . File

AGCO Sol'ns On-Line es

Clarknet III es.
Ingersoll-Rand
KubotaLink

New Holland DCS
Triad (Custom Code’


2 X6-15 « ELECTRONIC COMMERCE MENU RELEASE 2.1

 

OVERVIEW OF MENU OPTIONS

Electronic Commerce Menu

 

COMMAND
{c) DIS Corp.

. Electronic Commerce Configuration
Backup EC Configuration Files
. Restore EC Configuration Files

- Return To Security & Configuration Menu

Ready for option number or command
===>

 

X6.15-1 Electronic Commerce Configuration

Use this option to configure the DIS Electronic Commerce Manager. Transfers
between the AS/400 and the PC are handled by DIS Electronic Commerce
Manager (ECM) on the AS/400 and DIS Electronic Commerce Client (ECC) on
the PC. Configuration for DIS Electronic Commerce Client is also covered in this
chapter. The configuration done here is also applied to Manufacture Parts Locator
Download (X38-8).

X6.15-2 Backup Electronic Commerce Configuration Files

Use this option to back up your Electronic Commerce configuration files. DIS
Electronic Commerce Manager 400 runs in Library DISFILES, so it doesn’t
interfere with DIS Backup. Since the configuration is not included in DIS Backup,
this option is used for backing the configuration up to tape.

 

### Warning

Make sure the correct tape is in the drive. There is no selection screen. The
system initializes the tape and proceeds to back up the EC files immediately.

X6.15-3 Restore Electronic Commerce Configuration Files

Use this option to restore your Electronic Commerce configuration files in case of
emergency.

## CHAPTER X6.15-1

ELECTRONIC COMMERCE CONFIGURATION

### Introductio!

Use this option to configure the DIS Electronic Commerce Manager (ECM),
which handles communications on the AS/400. Transfers between the Business
System and another host computer, such as Case, use only ECM. The
configuration for ECM is also applied to Manufacture Parts Locator Download
(X38-8).

For other vendors, transfers are made between the DIS Business System and the

vendor’s software running on a PC. These transfers require 3 components:

= DIS Electronic Commerce Manager (ECM) on the AS/400

= DIS Electronic Commerce Client (ECC) on a PC. Configuration for ECC is
also covered in this chapter.

= Mannfacturer’s Software, such as New Holland DCS, on the same PC as
ECC. The following vendor packages may be installed on the PC:

AGCO Solutions™ On-Line

The table below shows the transactions supported

  
   

   
 

Manufacturer's
Communications
Package

   

Clarknet Hi

Farm Plan CheckF™ 4.0 for Windows® 95 (No configuration is required,
but the Farm Plan OPT for Farm Plan 95 communications must be on).

KubotaLink

Ingersoll-Rand
New Holland DCS
Triad (This is custom code for McFarlane, not covered in this chapter.)

ECC | Win
3.11

   
 

Orders
Priority

 

  
 

Farm Plan

 

    
 
 

 
     

Yes

 
 
 

  

   

Yes

by each vendor:

Stock & | Locator

  
      
  

 

 

AGCO Sol'ns On-Line _| Yes [Yes _| Yes
Case Communications | No N/A_ [N/A
Clarknet IIT Yes__| Yes No Yes

Yes

    

No

   

No

 

ale Credit Card Transactions onh

     

 

 

  

  

  

  

 

   

   
 

 

 

 

        

 

     

     

 

 

 

Ingersoll-Rand Yes_ | No Yes | Yes No No
KubotaLink No. Yes Yes No No No
New Holland DCS Yes Yes Yes Yes No

 

   

Triad (Custom Code}

X6.15-1.doc 3/24/99


2 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

 

### Contents

PREPARATION.
AS/400 System Name ..
AS/400 Workstation Name...
Enabling 16-bit Client Access Support..

 
 
  
  
 
  
  
 
  
 
 
  
 
  
 
 
 
 
 
 
 
 

CONFIGURATION — DIS ELECTRONIC COMMERCE CLIENT...
General Configuration...
AGCO Configuration
Clarknet Configuration.
Ingersoll-Rand Configuration .
Kubota Configuration.......
New Holland Configuration.
Triad Configuration

CONFIGURATION — DIS ELECTRONIC COMMERCE MANAGER.
General Configuration...
Case Configuration...
Ingersoll-Rand Configuration .
New Holland Configuration...
Parameters ..
Security...

STARTING COMMUNICATIONS PROGRAMS
AS/400 Program: Electronic Commerce Manager.
DIS Electronic Commerce Client (ECC)

TROUBLESHOOTING.
Verifying Transfers ...
Check AS/400 Now! Doesn’t Display Data...
Client Access Crashes During Print & Finalize
Corporate Order Error Messages.
Manufacturer’s Communications So
Missing Order Files «0.0... ceesessseerseeseerserreeneerenee
Print & Finalize Fails to Display Order Information Screens.
Ship To Address Information Missing
Problems Caused by Multipie AS/400s .

 
 
 
 
 
 
 
 
  
 
  

 

 

TECHNICAL NOTES. .-ERROR! BOOKMARK NOT DEFINED.
Uninstalling ECC... Error! Bookmark not defined.
Debugging ECC Error! Bookmark not defined.

Variable Definitions for File: DIS.INI Error! Bookmark not defined.


SECURITY & CONFIGURATION X6.15-1 ¢ ELECTRONIC COMMERCE CONFIGURATION 3

### Preparation

If you are configuring Case Communications, you can skip this section.

In this section, you'll find instructions for gathering information you’ll need to
make sure the AS/400 and the PC can find each other. In addition, there are
instructions for enabling 16-bit Client Access Support.

To complete the configuration, you will need to have the following information

handy:

1. The name of your AS/400 system.

2. The name of the PC (AS/400 workstation) where the manufacturer’s software
is installed.

Follow the instructions in this section to find these 2 names.

AS/400 System Name

O1 At the PC you are using for the manufacturer’s communications software,
start an AS/400 session. Look at the Sign On screen.


4 X6.15-1 ¢ ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

 

  
    
  
    
 
 
   
     

 

 

AS/400 Sign On Screen
Sign on
System... ..: si011024
Subsystem... . : OINTER
Display... .. : CLEMOISL
User 2... ee ee ee - -
Password . 2. 2 ee eee eee
Program/procedure ........
Menu. ee wee ee ee ee
Current library... ......-
This AS/400 System
Name is $1011024.
Your system name will
be different.
{C) COPYRIGHT IBM CORP. 1980, 1996.

 

   

O Write the System name on your Sign On screen here:


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 5

AS/400 Workstation Name

The AS/400 Workstation Name is the name of the PC where the manufacturer’s
communications software is installed. You can give it any name you want, up to
10 characters. DIS prefers that you use your computer name. The important thing
to remember is to use the same name during configuration on the AS/400 and the
PC. Follow the steps in Windows 3.x or Windows 95 sections to find your
computer name.

Windows 3.x

1 From Program Manager, double click on the Main icon.
O) Double click on the Contro! Panel icon.
O1 Double click on the Network icon.

Microsoft Windows Network

Computer Name:
Workgroup: PCGROUP

Comment: DIS Network Server

 

 

 

Logon Status
Currently logged on as CARENP

Default Logon Name: carenp

 

 

 

O Look at the value in the Computer Name field, such as PCQAO1 in the
example illustrated above.

O Write the value from your screen here: . Use this as
your AS/400 Workstation Name in configuration for DIS Electronic
Commerce Manager and Electronic Commerce Client.

O Click on Cancel.


6 X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Windows 95

0 On the PC where the manufacturer’s communications software is installed,
select Start | Settings | Control Panel.

O Double click on Network. The Network dialog box opens.
O Select the Identification tab.

 

lisabeth Stames

 

G Use the value in Computer name:, such as ElisabeS in the example
illustrated above. Write the value from your screen here.

Use this as your AS/400 Workstation Name in configuration for DIS
Electronic Commerce Manager and Electronic Commerce Client.

O Click on Cancel.
O1 Close the Control Panel window.


SECURITY & CONFIGURATION X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION 7
ee E—SEEeeeeeeeEEE—_————e—T Oe

Enabling 16-bit Client Access Support

This step is for PCs running Windows 95. If you are running Windows 3.x, skip
this section.

O Select Start | Settings | Control Panel.

O Double click on the Client Access icon. The Client Access Properties window
opens.

O Click on the Other tab as illustrated below.

 

 

O Check the Enable 16-bit Client Access support box as illustrated above.
O Click on OK. Close the Control Panel window.


8 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

 

### Configuration — Dis Electronic Commerce Client

The Electronic Commerce software is installed on the client PC that is designated
for communications to and from the AS/400. Specifically, it is the PC where the
manufacturer’s software, such as AGCO Solutions On-Line or New Holland
DCS, is installed.

Windows 3.11

— From Program Manager, double click on the DIS Applications icon to open
the group.

-— Within the DIS Applications group, double click on the DIS Electronic
Commerce Client icon. The DIS Electronic Commerce Client window opens.
See General Configuration.

Windows 95

~ Select Start | Programs | DIS Applications | DIS Electronic Commerce
Client. The DIS Electronic Commerce Client window opens.

— Select Edit.

— Select Configuration. The General tab is active.

cc


SECURITY & CONFIGURATION X6.15-1 ¢ ELECTRONIC COMMERCE CONFIGURATION 9

General Configuration

General configuration is required for all communications that use DIS Electronic
Commerce Client (ECC). In addition, manufacturers other than Farm Plan have
individualized configuration tabs, which are explained in this section.

t G Configuration - DIS Electronic Commerce Client

 

 

CRITICAL STEP.

Use the AS/400
Workstation Name
from page 5
(Windows 3.11) or
page 6 (Windows
95).

 

 

Check AS/400 every minutes

The suggested polling frequency is 10 minutes, which means the PC will look for
data, such as a finalized order or a part locator file, on the AS/400 every 10
minutes, and, if it finds something, transfer it to the designated directory on the
PC’s hard drive. Destination directories are configured within the different
Manufacturer tabs.


10 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

 

AS/400 Workstation Name

Use the computer name determined on page 6-the PC that will be used for
transfers (where the manufacturer’s communications software, such as AGCO
Solutions On-Line or Clarknet III, is installed, orders and returns will be printed
and closed, and parts locator files wili be created and downloaded). Make sure the
AS/400 Workstation Name is the same as the Workstation Name used on the
Configure Communication Devices screen. See page 30.

### Warning!

These names must match. If they don't, failure is guaranteed!

 

AS/400 System Name

Use the name, determined on page 4, found on the top right comer of the AS/400
Sign On screen. It is 8 characters long and usually begins with an “S.”

Logging Detail

The log file contains exactly what is displayed in the DIS Electronic Commerce
Client log window during transfers between the AS/400 and PC. One log file is
created for each day. If the download is ran more than once during the day, the

record of activity is added (appended) to the day’s log.

The level of detail may be brief, informational, or detailed (see page 11). The
amount of detail selection can be changed at any time. Log files can be viewed or
deleted by selecting File | Log File Management from the DIS ECC window.
When you select a log file to view, it is displayed in Notepad.

O Click on the Logging Detail down arrow to display the logging detail options.
O Click on the one you want. Detailed information is helpful if you're having
problems. For every day use, DIS recommends the Informational level.

Enable Timer

O Make sure the Auto Enable feature is selected.

O When General Configuration is done, click on a manufacturer tab or click on
OK to close the Configuration window.


SECURITY & CONFIGURATION X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION 11
ee NNsweeRe.vw__—_—eeyeyeeeeeeee —E——yeEOEeeeeeeA

Logging Detail

‘You can select from 3 logging detail records: Brief, Informational, and Detailed.
Below are examples of each type as generated by the same stock order. DIS
recommends the Informational log because it furnishes enough information for
you to get a pretty good idea of what has happened. The brief log doesn’t even let
you know that the destination file was closed, which is how you know that data
was transferred successfully. The detailed log omits nothing and is usually more
information than you need unless you are having problems.

Brief

ing.
4 11:25:18 AM: Connection enabled.
#11:25:12 AM: Connection disabled.

25:08 AM: Sending 23 bytes to queue: DISSYSOBJ/DISMFG.
25:08 AM: Connected to host $1011024; to= 2
125.05 AM: Create data queue: DISSYSOBJ/DISMFG400 on $ a

waiting 18 minutes.
18:37 AM: Check complete
18:37 AM: Checking AS400 for commands.

37 AM: Sending 74 bytes to queue: DISSYSOBJ/DISM.
37 AM: Connected to host $1011024: re= 2
18:37 AM: Create data queue: DISSYSOBJ/DISMFG400 oi
8:37 AM: Bulk data received; Qlines: c= 0

‘AM: Data teceived, len= 700
:36 AM: Data received, len= 700


12 X6.15-1 ¢ ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Detailed (Best for problems)

Fed Lae Cae

     

30 PM: Bulk data received: 9 fines; re= 0 5
0 PM: Received: 00163100008011475x O000003PLU
(0 Pi: Data received, len= 700
0 PM: Receive complete, rc =0
10 PM: Receive from data queue: DISSYSOBJ/MFGO0O
0 PM: Received: 00163100007011277% noDacSwASs

}0 PM: Data received, len= 700

(0 PM: Receive complete, rc = 0

0 PM: Receive from data queue: DISSYSOBJ/MFGOGO
(0 PM: Received: 00163100006010593x O000005R

(0 PM: Data received, fen= 700

(0 PM: Receive complete, rc = 0

0 :


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 13

AGCO Configuration

De ees

 

 

Ci On the Configuration window, select the AGCO Solutions tab.

O Check the Activated checkbox.

CG. If you accepted the default directories during your installation of AGCO
Solutions On-Line, click on Defaults to restore the directories used by AGCO
Solutions On-Line. If you did not accept the default directories when you
installed AGCO Solutions On-Line, enter the directories you selected during
installation.

O Enter the number of days you want to archive, Click on OK.

Activated Checkbox

f the Activated checkbox is checked:
The Defaults button is enabled.

= You can enter data into the text boxes.

"The text boxes cannot be empty.

= The pathnames (directories) furnished in the text boxes must exist; otherwise,
you'll be presented with a series of dialog boxes asking if you want to create
them.

If the Activated checkbox is not checked:

= ECC will not check for PC files for that manufacturer to see if any data needs
to be sent back up to the AS/400.


14 X6,15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Clarknet Configuration

 

O On the Configuration window, select the Clarknet tab.

O Check the Activated checkbox.

© If you accepted the default directories during your installation of Clarknet fi,
click on Defaults to show the directory used by Clarknet IfI for orders. If you
did not accept the default directory when you installed Clarknet III, enter the
directory you selected for orders during installation.

O Click on OK.

Activated Checkbox

ci the Activated checkbox is checked:
The Defaults button is enabled.

= You can enter data into the text boxes.

= The text boxes cannot be empty.

= The pathnames (directories) furnished in the text boxes must exist; otherwise,
you'll be presented with a series of dialog boxes asking if you want to create
them.

If the Activated checkbox is not checked:

= ECC will not check for PC files for that manufacturer to see if any data needs
to be sent back up to the AS/400.


SECURITY & CONFIGURATION X6.15-1 e ELECTRONIC COMMERCE CONFIGURATION 15

 

Ingersoll-Rand Configuration

ono00

Qo

Configuration - DIS Electronic Commerce Client

 

On the Configuration window, select the Ingersoll-Rand tab.

Check the Activated checkbox.

If you accepted the default directories during your installation of Ingersoll-
Rand, click on Defaults to show the directory used by Ingersoll-Rand for
orders. If you did not accept the default directory when you instalied
Ingersoll-Rand, enter the directory you selected for orders during installation.
Click on OK.

Activated Checkbox
If the Activated checkbox is checked:

The Defaults button is enabled.

You can enter data into the text boxes.

The text boxes cannot be empty.

The pathnames (directories) furnished in the text boxes must exist; otherwise,
you'll be presented with a series of dialog boxes asking if you want to create
them.

If the Activated checkbox is not checked:

ECC will not check for PC files for that manufacturer to see if any data needs
to be sent back up to the AS/400.


16 X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Kubota Configuration

ooo

Oo

 

Cem aot rtm Beer ee sg

BIC:AKTCEPC\OUTBOUNDS

On the Configuration window, select the Kubota tab.

Check the Activated checkbox.

If you accepted the default directories during your installation of KubotaLink,
click on Defaults to show the directory used by KubotaLink for orders. If you
did not accept the default directory when you installed KubotaLink, enter the
directory you selected for orders during installation.

Click on OK.

Activated Checkbox
if the Activated checkbox is checked:

The Defaults button is enabied.

You can enter data into the text boxes.

The text boxes cannot be empty.

The pathnames (directories) furnished in the text boxes must exist; otherwise,
you'll be presented with a series of dialog boxes asking if you want to create
them.

If the Activated checkbox is not checked:

ECC will not check for PC files for that manufacturer to see if any data needs
to be sent back up to the AS/400.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 17

New Holland Configuration

Configuration - DIS Electronic Commerce

 

 

 

On the Configuration window, select the New Holland tab.

Check the Activated checkbox.

If you accepted the default directories during your installation of New Holland
DCS for Windows, click on Defaults to show the directories used by New
Holland DCS. If you did not accept the default directories when you installed :
New Holland DCS, enter the directories you selected during installation. i
O Enter the Dealer Code assigned by New Holland.

O Click on OK.

ooo

 

 

Activated Checkbox

t the Activated checkbox is checked:
The Defauits button is enabled.

= You can enter data into the text boxes.

"The text boxes cannot be empty.

= The pathnames (directories) furnished in the text boxes must exist; otherwise,
you'll be presented with a series of dialog boxes asking if you want to create
them.

If the Activated checkbox is not checked:

» ECC will not check for PC files for that manufacturer to see if any data needs
to be sent back up to the AS/400.


18 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Triad Configuration

This is custom code for McFarlane, not covered in this guide.

### Configuration — Dis Electronic Commerce Manager

A dedicated system is not required for the configuration. This step must be
repeated for each division in all file sets. Don’t forget to go through the
configuration for each AGCO vendor you carry:

= AGCO Allis

= AGCOSTAR

= Black Machine
= Farmhand

= Gleaner

= Glencoe

= Hesston

= Landini

= Massey Ferguson
= Tye

= White

= White-New Idea

DIS Electronic Commerce Manager 400 runs in Library DISFILES, so it doesn’t
interfere with DIS Backup. The configuration provided on the following screens
is also applied to a new option on the Parts Configuration Menu, Manufacture
Parts Locator Download (X38-8).


SECURITY & CONFIGURATION X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION 19

Security & Configuration Menu

 

COMMAND
(c} DIS Corp.

- Backup and Restore Files Menu - Initial Data Entry menu
9. Apply Enhancements

. OPTDIS Master Menu . Prepare Partial Procedure

. List Of Files On Disk 11. DIS Business System Setup
12. Point of Sale Security

. Security Maintenance 13. OPT Report
. Initial File Setup
15. Electronic Commerce Menu

23. Return To Master Menu

Ready for option number or command
a> 15,

 

0 From the Security & Configuration Menu (X6), select option 15, Electronic
Commerce Menu.

Electronic Commerce Menu

COMMAND
(c) DIS Corp.

. Electronic Commerce Configuration
- Backup EC Configuration Files
. Restore EC Configuration Files

Except for Case, do not configure Electronic Commerce
until you have installed the manufacturer’s communications
software on a PC.

23. Return To Security & Configuration Menu

Ready for option number or command

ss=>

 

Since the Electronic Commerce Manager configuration is not included in DIS
Backup, there are also options for backing it up to tape and restoring it in case of
emergency.


20 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

1 From the Electronic Commerce Menu, select option 1, Electronic Commerce
Configuration. After the configuration security gate, if any, the following
screen is displayed.

Electronic Commerce Configuration Screen

AGRE Electronic Commerce Configuration MFGCFG
Division A
ven

2=Change 4=Delete P=Parameters S=Security
Opt Ven Name Com Description

Bottom
F3=Exit F5=Refresh F6=Add Roll

 

General Configuration

O On the Electronic Commerce Configuration screen, press Fo=Add.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 21
Se —eeeeaaaaaaeeeeeeeeeeeeeeeeeeeeee~xeeeeeEO—eeeeeeueeeeeeeeee

Add Vendor/Comm Package Window

 

 

A&R E Electronic Commerce Configuration MEGCFG
Division A

2=Change 4=Delete P=Parameters S=Security
Opt Ven Name Com Description

Add vendor/Comm Package

vendor Id... . .
: Manufacturer Id .
: Communication Pkg .
: Version...

F4=Prompt F12=Previous

 

Fi=Exit F5=Refresh

 

 

O1 With the cursor in the Vendor Id field, press F4=Prompt to select from a list
of valid vendor codes that you set up in Configure Vendor/Class (X38-1).

 

 

 

Select Vendor List
A&R EQUIPMENT SALES Electronic Commerce Configuration MFGCFG
Division A
: Select Vendor MFGVND
: Vendor : PC software is
: _ + curity not required for
: # Aon Case. Do not add
2 1=Select > TIL oth d
Opt Vendor = Name Bobet eee eeeeeeeeeee jer vendors
foo FAR FARMHAND : or/Comm Package unless you have
: 1 FOR FORD : installed their
roo GEH GEHL : communications
Z _ HDC HARLEY DAVIDSON 2 software on the
z _ HES HESSTON : ndor Id. . PC.
3 More... : nufacturer Id. . *
: : munication Pkg .
: F3-Exit Roll : rsion .
Bec e ee eee cece eee eee ress eeeeeecseeeed SPrevious :
F3=Exit F5=Refresh Beee eae


X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

O Press [PgDn] to display more vendors.

O Select the vendor code you use for the manufacturer, such as FOR in the
illustration, with 1=Select. The display returns to the Add Vendor/Comm
Package window.

O) Press [Tab] to place the cursor in the Manufacturer Id field.
O) Press F4=Prompt in the Manufacturer Id to select from a list.

Select Manufacture Id List

 

  
  
    
    
 
  
  
   
    
   
 

AGR EQUIPMENT SALES Electronic Commerce Configuration
Division A

 

Select Manufacturers Id For Farm Plan,

Mig select any vendor

—_ that is not used
deselect for another —
: communications
: Opt Mfg Name package,suchas ......
+ _ AGC AGCO a Miscellaneous

CAS CASE CORPORATION vendor {MIS).

— CNT Clarknet
1 NHD New Holland North America, INC.

: Bottom :
: F3sExit Roll 3

P3sExit FSsRefresh ieee eee eee eee cece eee een ner e eee eee ened

   

 

O Press [PgDnj to display more manufacturers.

O Select manufacturer’s ID, such as NHD (New Holland), with 1=Select. The
display returns to the Add Vendor/Comm Package window. The Case vendor
must be “CAS.” The Farm Plan vendor code is not used: select any vendor
that is not used by another communications package, such as a Miscellaneous
vendor (MIS).

O Press [Tab] twice to place the cursor in the Communication Pkg Field.

O Press F4=Prompt in the Communication Pkg field to select from a list.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 23

 

 

Select Communication Package List

 

 

A&R EQUIPMENT SALES Electronic Commerce Configuration MFGCFG
Division A

: Opt Ven Ver Name bosses
— AGC 100 AGCO SOLUTIONS ON-LINE : :
— CAS 100 CASE VSAT/LEASE COMMUNICATIONS
— CNT 100 Clarknet IIT

1 WHD 100 New Holland pcs

: Bottom :
: F3=Exit Roll

F3sExit FSsRefresh 12.0.2... e eevee eet ece eee sere cence eset teeter en eeed

 

O Press [PgDn] to display more communications packages.

O Select Communication Package, such as NHD (New Holland DCS), with
1=Select. The display returns to the Add Vendor/Comm Package window.

O1 Press [Enter]. If you are configuring Case, Ingersoll-Rand or New Holland,
there is an additional screen; otherwise, you will return to the Electronic
Commerce Configuration screen, which displays the Vendor/Communications
package.


X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

 

Case Configuration

Hf you are configuring Case Communications, the following screen is displayed:

 

AGR EQUIPMENT SALES CASE COMMUNICATIONS cASLOOCFG1
Division A Configure

### Common Communication Information

Temporary File Library . . . DISTEMP Case User ID... 1... 2. AHI98.
Leased or Vsat (Lor V}. . . L Case Dealer # 2... 2... 22385800
Keep Sugg Part Transfers . . 30 Keep Retail Parts Activity . 10

Keep Incoming Case Data, . . 08 LU-ID #10. ..-.2.022. SNUFOS
Keep Cross Reference Data . 08 LU-ID #2... SNUFOS
Keep CASENET Data... ... 10 8NA3270 or TN3270 (S or T) . $

Configure the communications to 1N3270

DIVISIONAL INFORMATION (P) when the connection to CASE uses
an ethernet card. Otherwise it

Dealer Number... 2... 22385800 © should always be SNA3270 (S).

Order Sequence Number. . . 00012

Retail Tracking Sequence . 00000

 

COMMON COMMUNICATION INFORMATION

Temporary File Library

This library stores log files for SNUFO5, SNUFO06, and the CASECOM file.
Leased or Vsat (L or V)

Type of communications line used.

Keep Sugg Part Transfers

Number of days that suggested part transfers are stored.

Keep Incoming Case Data

Number of days that incoming data is stored.

Keep Cross Reference Data

Number of days that cross reference data is stored.

Keep CASENET Data

Number of days until read CaseNets are removed.

Case User ID

User identification used when connecting to Case (assigned by Case).
Case Dealer #

Case-assigned dealer number for the entire company

Keep Retail Parts Activity

Number of days to store retail parts activity.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 25

LU-ID #1

Device used to communicate. Usually SNUFOS.

LU-ID #2

Device used to communicate. Usually SNUFO6.

SNA32700r TN3270 (S or T)

Select TN3270 if you have an Ethermet connection with Case--it can be used in
VSAT and Frame connections only; otherwise, select SNA3270.

DIVISIONAL INFORMATION

Dealer Number

Case-assigned dealer number for the current division. Each division should also
have its dealer number set up in Configure Vendor/Class (X38-1).

Order Sequence Number

Sequence number (1-99999) used for next Case order. This number is increased
after each transmission. For new dealers, start with 1. For existing dealers, check
for current number using 3270 communications.

Retail Tracking Sequence

Sequence number (1-99999) used for next retail tracking. This number is
increased after each transmission. For new dealers, start with 1. For existing
dealers, check for current number using 3270 communications.


26 X6,15-1 ¢ ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Ingersoll-Rand Configuration

If you are configuring Ingersoll-Rand, the following screen is displayed:

AGR EQUIPMENT SALES CONFIGURE COMMUNICATIONS INGRANDSOi.
INGERSOLL-RAND VER 1.00

Manufacturing Plant or Distribution Warehouse

Account Number

Invoice Type

Date Last Weekly order oo0000 «——- No input

 

Manufacturing Plant or Distribution Warehouse 30 characters.

Account Number 11 characters.

Invoice Type 3 characters.

Date Last Weekly Order Date (MMDDYY). No input.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 27

New Holland Configuration

O Ifyou are configuring New Holland, the following screen prompts you for a
Valid Dealer Number (required) and User Code, which are provided by New
Holland. When you press [Enter], you will return to the Electronic Commerce
Configuration screen, which displays the Vendor/Communications package.

Dealer Number Prompt

 

A&R EQUIPMENT SALES Electronic Commerce Configuration MFGCFG
Division A

Enter Valid Dealer Number

Dealer Code . . 01234

user Code... :ers $=Security

Description
AGCO SOLUTIONS ON-LINE

Change vendor/Comm Package

Vendor Id
Manufacturer Id . .
Communication Pkg .

F3sExit F5=Refresh


28 X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Parameters

If you are configuring Case Advanced Communications, you can skip this section.
All others are required to enter the workstation name and library associated with
the various transactions that will be transferred to the manufacturer’s software on
the PC.

Electronic Commerce Configuration Screen

A&R E Electronic Commerce Configuration
Division A
Ven

2=Change 4=Delete P=Parameters S=Security
Opt Ven Name Com Description
P FOR New Holland DCS NED New Holland DCs

Bottom

F3sExit F5sRefresh F6=Add Roll
DIS-9913 Vendor FOR has been added

 

O From the Configure Communications screen (X6.15-1), select the
manufacturer with P=Parameters. The Configure Communication Devices
screen is displayed with a list of the types of transactions that can be
transferred. Not all vendors support all transaction types. The types are:

FIN Financial Statement
INV Part Locator Information
ORD Stock Order

ORD-CORP Corporate Stock Order
ORD-DROP Drop Ship Order
ORD-EMERG — Emergency (Priority) Order
ORD-UP PSO# Upload

RTN Return


SECURITY & CONFIGURATION X6.15-1 ¢ ELECTRONIC COMMERCE CONFIGURATION 29

The table below shows the transactions, which will be supported by each
manufacturer:

Manufacturer's Format. | Orders | Orders | Parts
Communications Finan. Priority | Stock & | Locator
Package State. Drop Corp. File
Ship

AGCO Sol'ns On-Line
Clarknet III

Farm Plan/Ag Line
Ingersoll-Rand
KubotaLink

New Holland DCS

Triad (Custom Code

 

 

 

 

 

 

 

 

Configure Communication Devices Screen

 

A&R EQUIPMENT SALES Configure Communication Devices MFGPRM
Division
Transaction
Your screen
2-Change may look
opt Transaction Workstation Name Library different. Not
2 FIN _ DISSYSOB
2 INV —_—__ DISSYSOBI all vendors
2 orp DISSYSOBZ will have the
2 ORD-CORP —_— DISSYSOBT same
2 ORD-DROP DISS¥SOBI transaction
2 ORD-EMERG _ DISSYSOBI list.
2 RIN DISSYSOBI
Bottom
Fi=Exit FS5sRefresh Roll

 

 

O To change a parameter, select a transaction with 2=Change. You can select
more than | transaction before you press [Enter]. The Change Device Parms
window opens.


 

 

X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3
Change Device Parms Window
ARR E Configure Communication Devices MFGPRM
Division
Transaction
2-Change po Change Device parms :
Opt ‘Transactio :
2 FIN Transaction... . PIN Use the AS/400
2 INV Workstation Name . ELISABES— Workstation
2 ORD Library. 2... DISSYSOBT Name from page
2 ORD-CORP 5 (Windows
2 ORD-DROP
3 ORD-EXERG 3.11) or page 6
2 RIN F12=Retuxn {Windows 95).
Bottom
F3sExit F5=Refresh Roll

 

 

 

O For “Workstation Name,” enter the name determined on page 5 (Windows

3.11) or page 6 (Windows 95)--the PC where the manufacturer’s

communications software is installed. Make sure the Workstation Name is the
same as the AS/400 Workstation Name used in the General Configuration of
DIS Electronic Commerce Client (see page 9). The name of the library
remains DISSYSOBJ, which is the default.
O Press [Enter] to record the information. If you selected more than 1
transaction type, the next one will be presented.
O When all transactions have been processed, you’l] return to the Configure
Communication Devices screen.
O To return to the Electronic Commerce Configuration screen, press F3=Exit.


SECURITY & CONFIGURATION X6,15-1 » ELECTRONIC COMMERCE CONFIGURATION 31

Security

In this section, you’ ll establish a security key and expiration date for each type of
transaction. Until security is fully implemented, everyone will use the same

security key and expiration date. Don’t worry—your transactions will be perfectly
safe.

Electronic Commerce Configuration Screen

A&R EQUIPMENT SALES Electronic Commerce Configuration MFGCFG
Division A

ven

2=Change 4=Delete P=Parameters S=Security
Opt ven Name Com Description
S FOR New Holland DCS NHD New Holland Docs

F3-Exit PS=Refresh F6=Add Roll

 

O From the Electronic Commerce Configuration screen (X6.15-1), select the
manufacturer with S=Security.


32 X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION

Configure Security Screen
A&R EQUIPMENT SALES Configure Security
Division
Transaction

2=Change

Your screen may
Opt Transaction Security Key look different. Not

2 ed all vendors will

ORD have the same

ORD-CORP transaction list.

ORD-DROP

ORD-EMERG

RIN

F3=Exit F5=Refresh Roll

Expiration

Date
000000
990000
000000
ooco00
ooco00
900000
000000

Bottom

 

0 To add or change a security key, select each transaction type with 2=Change.
You can select more than | transaction type before you press [Enter]. The

Change Transaction Security window opens.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 33

 

Change Transaction Security Window

 

 

A&R EQUIPMENT SALES Configure Security MEGSEC
Division
Transaction
2s: Change Transaction Security
op Transaction . . . . FIN
2 Security Key. . . . NED.
2: Expiration Date . . 123139
2:
2
2 F12=Return
2
2

Bottom
F3sExit  FS5=Refresh Roll

 

O For the Security Key, type:
Acc for AGCO Solutions On-Line
CASE for Case
ent for Clarknet II
FPA for Farm Plan/Agline
ING for Ingersoll-Rand
KUB for Kubota
NuD for New Holland DCS

O For the expiration date, type: 123139, which is December 31, 2039, the most
future date in the DIS Business System.

C. Press [Enter]. If you selected more than 1 transaction type on the previous
screen, the next one will be presented.

O When all transaction types have been processed, you’ll return to the Configure
Security screen. To return to the Electronic Commerce Configuration screen,
press F3=Exit.

O Repeat this process, Configuration — DIS Electronic Commerce Manager,
which begins on page 8, for each vendor you have communications software
for. In the case of AGCO, repeat for every vendor associated with AGCO.
Select the same Manufacturers Id for each AGCO vendor. Don’t forget the
Parameters and Security screens!

Repeat this process for each division in all file sets.


34 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

 

STARTING COMMUNICATIONS PROGRAMS

AS/400 Program: Electronic Commerce Manager

O Normally, the DIS Electronic Commerce Manager (DISECM400) runs 24-
hours a day except when it is stopped by an IPL. It will be restarted after the
IPL. The jobs that use the Electronic Commerce Manager will start it if it is
not active: finalizing an order or return, or downloading a formatted financial
statement or parts locator file. You can verify that the job is running by typing
the following command at an AS/400 command line: WRKACTJOB [Enter].
Look for the job illustrated below:

 

Subsystem/Job User Type CPU % Function Status

DISECM400 Qsys SBS 0 DEQW
DISECM400 QPGMR BCH -0 PGM-MFG400ENGO DEQW

 

DIS Electronic Commerce Client (ECC)

The programs that process data on the PC are shut down whenever the PC is
rebooted or powered off; therefore, they must be restarted afterwards. Follow this
procedure every morning. Repeat it any time the PC is rebooted or Client Access
is restarted.

1, Start the PCs where the manufacturer’s communications software and ECC is
installed.

2. Start the DIS Business System on the PCs. This starts the Client Access
connection between the AS/400 and the PCs.

3. Start ECC. ECC starts the data queue on the AS/400 and the polling process.
It must be running for information to be transferred successfully to and from
the AS/400 and the PCs.

Windows 3.17

—- To start DIS ECC from Program Manager, double click on the DIS
Applications icon. Within the DIS Applications group, double click on the
DIS Electronic Commerce Client icon.

Windows 95

— To start DIS ECC, select Start | Programs | DIS Applications | DIS
Electronic Commerce Client.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 35

### Troubleshooting

Verifying Transfers

To verify that a file has been successfully downloaded and is ready for
transmission to the manufacturer, look in the DIS Electronic Commerce Client
window on the PC where the log is displayed. Look for the line: “Destination file
closed,” which means the file has been transferred from the AS/400 to the PC in
the format requested by the manufacturer.

37 AM: Data received, lene
‘37 AM: Data received, ler
18:36 AM: Data received, ler

  
  

If you don’t see the line, you can wait for the next polling time—the DIS
Electronic Commerce Client polls the AS/400 every 10 minutes (or the number
you set in Configuration).


X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

 

Tf you are in a hurry, you can click on More Detail>> to expand the dialog box, C
then click on Check AS/400 Now! to poll the AS/400 immediately.

imer enabled.
nding 23 by

 

Check AS/400 Now! Doesn’t Display Data

Tf you click on Check AS/400 Now! and don’t see any data, verify the Electronic
Commerce Configuration (X6.15-1) on the AS/400.

1. Verify the Parameters configuration and repeat for all manufacturers in all
divisions. Make sure the workstation name is the same as the AS/400
workstation name configured in ECC on the PC. Make sure the library name
is DISSYSOBJ. See page Error! Bookmark not defined..

2. Verify the Security configuration. See page 31.

Client Access Crashes During Print & Finalize

If Client Access crashes while you are printing and finalizing an order on the
Order Information screen, go back into the Print & Finalize screens.


SECURITY & CONFIGURATION X6.15-1 «e ELECTRONIC COMMERCE CONFIGURATION 37

 

ECM has the same recovery feature currently in the DIS Business System
product. If the Print and Finalize process is interrupted, the next time the you
start that process you will return to the screen you were using.

Corporate Order Error Messages

When you are using Electronic Commerce and create a corporate order, the
system checks to see whether the sub-order vendors have been set up in Configure
Electronic Commerce.

If none of the vendors have been set up in Configure Electronic Commerce, the
order is finalized as usual.

if all of the vendors are set up in Configure Electronic Commerce for the same
communications package and they all pass security, the order is finalized and the
appropriate Order Information screen for Electronic Commerce is presented.

If one or more of the vendors are not set up in Configure Electronic Commerce,
the following error codes may be displayed:

ERR: Invalid sub-order found verify EC configuration.

This error code indicates that not all orders passed security, not all orders are of
the same communication package, or an order was encountered that was not
configured.

ERR: Invalid vendor verify EC configuration.
This error code indicates that the vendor code selected was not set up in the main
division’s EC 400 configuration.

The order is then submitted under the first vendor code encountered. For example,
if MAS, HES, and GLE orders have been combined into a corporate order, the
first vendor encountered, MAS, will be used.

 

Manufacturer’s Communications Software Problems

If you encounter problems while using the manufacturer’s software, such as
AGCO Solutions On-Line or Clarknet II, other than missing order files
(described below), please call the manufacturer. DIS cannot provide support for
these packages.


38 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Missing Order Files

When your manufacturer’s communications software, such as AGCO Solutions
On-Line or Clarknet Il, does not find the order files it was expecting, follow
these steps to find out what is wrong.

ECC was not running

Assuming that configuration has been done correctly (previous orders have been
transferred successfully), it is most likely that ECC was not running on the PC
when Print & Finalize was done on the AS/400. All order types will remain on the
WRKACTIOB screen until ECC is started and the transfer occurs. Check the
ECC log for the "Destination file closed” message. Follow these steps to resolve
the issue:

Stock Order. Select Print/Finalize Order (X341-3) again.

Priority Order. The AS/400 will think the priority order was closed and
transmitted just fine. Do not attempt to back it out of the DIS Business System,
which will only waste a lot of time and totally mess up your reservations. Instead,
use the printout and re-create the order manually in the manufacturer’s software.
Receive it in the usual way when it comes in.

Verify Electronic Commerce Configuration

If ECC was running when the order was finalized, verify Electronic Commerce
Configuration (X6.15-1) on the AS/400. See Parameters on page Error!
Bookmark not defined., Security on page 31. In particular, verify the AS/400
Workstation Name on the AS/400 and PC match exactly.

Check Configuration of PC directories

Verify that the manufacturer’s software and ECC on the PC are configured for the
same PC directory.

In the manufacturer’s software, check the configuration. This will be different for
each manufacturer. Please refer to the manufacturer’s documentation. Make sure
the drive/directory combination matches what is in ECC.

To check ECC configuration on the PC, follow these steps:

(1 Start ECC. See page 34.

(1) Select Edit | Configuration.

C) Click on the manufacturer’ s tab.

O Verify the drive/directory combination for each type of order.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 39

Print & Finalize Fails to Display Order Information Screens

If you don’t get the new Order Information screens illustrated in this Guide, verify
the Electronic Commerce configuration on the AS/400.

Make sure the order was for one of the vendors configured in Electronic
Commerce Configuration (X6.15-1).

Make sure the Electronic Commerce Manager OPT switch is set.

If it is for a configured vendor, check the configuration carefully. Make sure the
Parameters and Security sections are configured correctly. See pages Error!
Bookmark not defined. and 31.

Ship To Address Information Missing

If the last part of your ship to address information was present on the AS/400 but
is missing when you open the order in the manufacturer’s communications
software, you probably used a tilde (~) somewhere on the Order Information
screen.

For the current order, simply add the information to the order in the
manufacturer’s software and process it as usual. To prevent this from happening
again on future orders, do not use a tilde (~) anywhere in the Order Information
screens. The tilde is used to indicate the end of the data in the data transfer
process.

Problems Caused by Multiple AS/400s

The problems described in this section are seldom encountered at a dealership.
They occur occasionally at DIS where there are multiple AS/400s.

AS/400 System Name Must Be Changed

If ECC is running when you decide to change the AS/400 System Name:

OQ Select File | Close Connection.

O Select Edit | Configuration.

(1 Change the AS/400 System Name. You must use all CAPS in this field.
OG Click on More Detail >>>.

1 Click on Check AS/400 Now! to connect to the new AS/400.

If ECC is not running when you decide to change the AS/400 System Name:
Method 1: Open ECC and follow the steps above.


40 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.3

Method 2: This is the easiest if you are not configured at the Client Access
Workstation level for this AS/400. Verify ECC is closed and manually edit the
CAWINDOWSUIS.INI file. The cleanest way is to change the AS/400 System
Name to the install default value of $0000001, then start ECC. This will open the
dialog box with no further challenges. You may then modify the data in the field.

System Security Dialog Box

‘You may get a System Security dialog box, requesting a Userid and Password, as
illustrated below, when you start ECC or when there is no Client Access sessions
Or connections at the time ECC is started.

 

When ECC is configured for a specific AS/400, ECC automatically connects to

that AS/400 when it is started. If, for some reason, you have it configured for an {
AS/400 that you are not currently connected to, you will see a Client Access

System Security dialog box.

Example. My ECC is configured for $100008G as that is where I was last using
it. lam currently only logged onto $100276G. When I open ECC I will see a
Userid/Password dialog box with S100008G on the title bar.

## CHAPTER X6.15-1

ELECTRONIC COMMERCE CONFIGURATION

### Introduction

Use this option to configure the DIS Electronic Commerce Manager. Transfers
between the AS/400 and the PC are handled by DIS Electronic Commerce
Manager (ECM) on the AS/400 and DIS Electronic Commerce Client (ECC) on
the PC. Configuration for DIS Electronic Commerce Client is also covered in this
chapter. The configuration done here is also applied to Manufacture Parts Locator
Download (X38-8).

The Electronic Commerce programs are used to transfer information between the
DIS Business System and the PC where one or more of the following vendor
packages is installed:

AGCO Solutions™ On-Line

Clarknet IIT

KubotaLink

Ingersoll-Rand

New Holland DCS

Triad (This is custom code for McFarlane, not covered in this chapter.)

The table below shows the transactions supported by each vendor:

Manufacturer’s i Orders | Orders
Communications . Priority | Stock
Package

AGCO Sol'ns On-Line
Clarknet III
Ingersoll-Rand
Kubota ink TYes_[ No
New Holland DCS Yes | Yes


X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1

 

 

### Contents

PREPARATION ......sssssssessocsssessesenrerssoesereseesrarsnserseasenenteensensentarenenentecseaters
AS/400 System Name
AS/400 Workstation Name...

 

 

CONFIGURATION -— DIS ELECTRONIC COMMERCE CLIENT.
General Configuration .
AGCO Configuration
Clarknet Configuration
Ingersoll-Rand Configuration .
Kubota Configuration ..
New Holland Configuration.
Triad Configuration

 
 
  
  
 
  
 
 

CONFIGURATION - DIS ELECTRONIC COMMERCE MANAGER

Parameters

 

STARTING COMMUNICATIONS PROGRAMS ...
AS/400 Program: Electronic Commerce Manager
DIS Electronic Commerce Client (ECC)...

 
 

TROUBLESHOOTING........:ecssssscssssansssnnssssrensarssnensevensensvenoresansesensessensare 29


SECURITY & CONFIGURATION X6.15-1 »« ELECTRONIC COMMERCE CONFIGURATION 3

### Preparation

Have the following information handy:

1. The name of your AS/400 system.

2. The name of the PC (AS/400 workstation) where the manufacturer’s software
is installed.

Follow the instructions in this section to find these 2 names.

AS/400 System Name

O Atthe PC you are using for the manufacturer’s communications software,
Start an AS/400 session. Look at the Sign On screen.

 

AS/400 Sign On Screen
Sign on

System 2... $1011024
Subsystem... : QINTER
Display... . t CLEM01S1

User 2 ee -

Password - 2...

Program/procedure . .. 2... 1. .

Menu. www Le

This AS/400 System
Name is $1011024.

Your system name will
be different.

 

(C) COPYRIGHT IBM CORP. 1980, 1996.

 

O Write the System name on your Sign On screen here:


4 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1
ee een em eIELEASE 21

AS/400 Workstation Name

The AS/400 Workstation Name is the name of the PC where the manufacturer's
communications software is installed. You can give it any name you want, up to
10 characters. DIS prefers that you use your computer name. The important thing
to remember is to use the same name during configuration on the AS/400 and the
PC. Follow the steps in Windows 3.x or Windows 95 sections to find your
computer name.

Windows 3.x

O From Program Manager, double click on the Main icon.
O Double click on the Control Panel icon.
© Double click on the Network icon.

yy Microsoft Windows Network

+ | conpiterWane:
Workgroup: PCGROUP [3]
Comment: DIS Network Server (

‘Logon Status
Currently logged on as CARENP

Default Logon Name: carenp

Log Off

   

 

 

 

Options:

re. | GR.
Startup | Password Event Log

 

O Look at the value in the Computer Name field, such as PCQAO1 in the
example illustrated above.

O Write the value from your screen here: . Use this as
your AS/400 Workstation Name in configuration for DIS Electronic
Commerce Manager and Electronic Commerce Client.

O Click on Cancel.


SECURITY & CONFIGURATION X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION 5
eee oO O— UUme UME UNERMALON OY

Windows 95

O On the PC where the manufacturer’s communications software is installed,
select Start | Programs | NS Router | NS Administrator. The
NS/Administrator dialog box is displayed, as illustrated below:

 

 

O Right click on NS/Router.


é

X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION
C1 Select Properties.

7 Use.a shared value: | —- :

© Use alocal specific value: | j Oe

OD Select the Local LU tab.


SECURITY & CONFIGURATION X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION 7

 

O Look at the section, PC Location Name. Use the value in Use computer

name:, such as ELISABES in the example illustrated above. Write the value
from your screen here: . Use this as your AS/400
Workstation Name in configuration for DIS Electronic Commerce Manager
and Electronic Commerce Client..

C1 Select Cancel.
O Close the NS/Administrator window.

### Configuration — Dis Electronic Commerce Client

The Electronic Commerce software is installed on the client PC that is designated
for communications to and from the AS/400. Specifically, it is the PC where the
manufacturer’s software, such as AGCO Solutions On-Line or New Holland
DCS, is installed.

Don’t forget to go through the ECC configuration for each AGCO vendor you
carry such as: AGCO Allis, AGCOSTAR™, Black Machine, Farmhand®,
Gleaner®, Glencoe®, Hesston®, Landini, Massey Ferguson®, Tye®, White, or
White-New® Idea.

Windows 3.11

From Program Manager, double click on the DIS Applications icon to open
the group.

Within the DIS Applications group, double click on the DIS Electronic
Commerce Client icon. The DIS Electronic Commerce Client window opens.
See General Configuration.

Windows 95

Select Start | DIS Applications | DIS Electronic Commerce Client. The
DIS Electronic Commerce Client window opens.

Select Edit.

Select Configuration. The General tab is active.


8 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1
ee ——eee_O_50"T TS eee eee RELEASE 2.1

General Configuration

     
 

ecu ye ate re,

  

(faint ta

Receive Poling Frequency {minutes} [T0

    

Use the AS/400 ea .

Workstation > ~A8/400 Workstation Name: [ELISABES

Name from page te pd : CR
8 (Windows AS/400 System Nome: [STI
3.11) or page 12 AO System Name |S20T 024
(Windows 95).

   
 

 
 

Logging Detait

  
 

© Defauits’ j we Cancel :

 

Receive Polling Frequency (minutes)

The suggested polling frequency is 10 minutes, which means the PC will look for
data, such as a finalized order or a part locator file, on the AS/400 every 10
minutes, and, if it finds something, transfer it to the designated directory on the
PC’s hard drive. Destination directories are configured within the different
manufacturer tabs.

AS/400 Workstation Name

Use the name determined on page 7-the PC that will be used for transfers (where
the manufacturer’s communications software, such as AGCO Solutions On-Line
or Clarknet II, is installed, orders and returns will be printed and closed, and
parts locator files will be created and downloaded). Make sure the. AS/400
Workstation Name is the same as the Workstation Name used on the Configure
Communication Devices screen. See page 25.

AS/400 System Name

Use the name, determined on page 3, found on the top right corner of the AS/400
Sign On screen. It is 8 characters Jong and usually begins with an “‘S.”


SECURITY & CONFIGURATION X6.15-1 * ELECTRONIC COMMERCE CONFIGURATION 9

Logging Detail

The log file contains exactly what is displayed in the DIS Electronic Commerce
Client log window during transfers between the AS/400 and PC. One Jog file is
created for each day. If the download is run more than once during the day, the
record of activity is added (appended) to the day’s log. The level of detail may be
brief, informational, or detailed. The amount of detail selection can be changed at
any time. Log files can be viewed or deleted by selecting File | Log File
Management from the DIS ECC window. When you select a log file to view, it is
displayed in Notepad.

O Click on the Logging Detail down arrow to display the logging detail options.

O Click on the one you want.

Enable Connection

O Make sure the Auto Enable feature is selected.


10 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1

AGCO Configuration

DIS Electronic Commerce

Clarknet
Ingersoll-Rand

White orders to: |C:\AGCO\On-Line\orders\ :|

Wie Patt Locator data to: [C8500 \Orr Linens " :

"White retuins to: [OAGCO\On Line\anvetumy 4

 

On the Configuration window, select the AGCO Solutions tab.

If you accepted the default directories during your installation of AGCO
Solutions On-Line, click on Defaults to restore the directories used by AGCO
Solutions On-Line. If you did not accept the default directories when you
installed AGCO Solutions On-Line, enter the directories you selected during
installation.

Enter the number of days you want to archive. Click on OK.

If you receive messages concerning directories not found, such as illustrated
below, click on Yes to create them: otherwise you will receive these messages
every time you come into Configuration.

oo

oo


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION i

Clarknet Configuration

Re eR ec en | (id
He hen —

 

C1 On the Configuration window, select the Clarknet tab.

1 Ef you accepted the default directories during your installation of Clarknet II,
click on Defaults to show the directory used by Clarknet III for orders. If you
did not accept the default directory when you installed Clarknet III, enter the
directory you selected for orders during installation.

O Click on OK.

C1 If you receive messages concerning directories not found, such as illustrated
below, click on Yes to create them; otherwise you will receive these messages
every time you come into Configuration.

Directory not found xi

CZ) CATRIADXFRV dows rot exist.
Create it? vos,


12 X6.15-1 ¢e ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1
ee eeeeeeeaeles=<~_ S eEeeee ee ELEASE 6.7

Ingersoll-Rand Configuration

nfiguration - DIS Electronic Commerce Client

 

£1 On the Configuration window, select the Ingersoll-Rand tab.

1 If you accepted the default directories during your installation of Ingersoll-
Rand, click on Defaults to show the directory used by Ingersoll-Rand for
orders. If you did not accept the default directory when you installed
Ingersoll-Rand, enter the directory you selected for orders during installation.

O Click on OK.

C1 If you receive messages concerning directories not found, such as illustrated
below, click on Yes to create them; otherwise you will receive these messages
every time you come into Configuration.

Crm C a eure x]

~ (C\TRIADXFRV does


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 13

Kubota Configuration

 

 

O On the Configuration window, select the Kubota tab.

1 If you accepted the default directories during your installation of KubotaLink,
click on Defaults to show the directory used by KubotaLink for orders. If you
did not accept the default directory when you installed KubotaLink, enter the
directory you selected for orders during installation.

Click on OK.

If you receive messages concerning directories not found, such as illustrated
below, click on Yes to create them; otherwise you will receive these messages
every time you come into Configuration.

oo

       
   

Piece Cite) <j
3 CATRIAD XFR" does notiesist: -
Create it? we

ef


14 X6.15-1 * ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1
So ee eeoeOer eC ELEASE 2.7

New Holland Configuration

     
 

- = Configuration - DIS Electronic Commerce Client Bee
Fle Help " :

[Berea Y_Ingereot and __ABCO Solitons “Heer ofiand)
: | Wit orders to [ES idesy — 7 - j
| wite at Lecter deta te [EWEGER
[oo Wt tart [ER
"Dealer Code: [123455 mr

      

    
      
 
    
 

On the Configuration window, select the New Holland tab.

If you accepted the default directories during your installation of New Holland
DCS for Windows, click on Defaults to show the directories used by New
Holland DCS. If you did not accept the default directories when you installed
New Holland DCS, enter the directories you selected during installation.
Enter the Dealer Code assigned by New Holland.

Click on OK.

If you receive messages concerning directories not found, such as illustrated
below, click on Yes to create them; otherwise you will receive these messages
every time you come into Configuration.

oO

oo00

      
 

rH

 

OT es

‘CATRIAD XFRV does not Git
Create i? ne

 

 
 
 
 

 

[xe] No

Triad Configuration

This is custom code for McFarlane, not covered in this chapter.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 18
eee Eee MIME UE CONFIGURATION IO

### Configuration - Dis Electronic Commerce Manager

A dedicated system is not required for the configuration. This step must be
Tepeated for each division in all file sets. Don’t forget to go through the
configuration for each AGCO vendor you carry:

AGCO Allis
AGCOSTAR
Black Machine
Farmhand
Gleaner
Glencoe
Hesston

Landini

Massey Ferguson
Tye

White
White-New Idea

DIS Electronic Commerce Manager 400 runs in Library DISFILES, so it doesn’t
interfere with DIS Backup. To configure it, you’l! use a new option on the
Security & Configuration Menu, Electronic Commerce Menu (X6-15). The same
configuration is also applied to a new option on the Parts Configuration Menu,
Manufacture Parts Locator Download (X38-8).


ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.4

Security & Configuration Menu

 

COMMAND
(c} DIS Corp

. Backup and Restore Files Menu . Initial Data Entry Menu

9. apply Enhancenents
OPTDIS Master Menu - Prepare Partial Procedure

. List Of Files On Disk ll. DIS Business System Setup
12. Point of Sale Security

. Security Maintenance 13. OPT Report

. Initial File Setup
15. Electronic Commerce Menu

23. Return To Master Menu

Ready for option number or command
ses> 15

 

O From the Security & Configuration Menu (X6), select option 15, Electronic
Commerce Menu.

Electronic Commerce Menu

 
      
 
   
 
 
   
 
 

COMMAND 5 E6
({c) DIS corp.

 

1. Electronic Commerce Conéiguration
2. Backup EC Configuration Files
3. Restore EC Configuration Files

Do not configure Electronic Commerce until you have
instalied the manufacturer’s communications software.

23. Return To Security & Configuration Menu

 
 

Ready for option number or command

 

Since the Electronic Commerce Manager configuration is not included in DIS
Backup, there are also options for backing it up to tape and restoring it in case of
emergency.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 17

 

O From the Electronic Commerce Menu, select option 1, Electronic Commerce
Configuration. After the configuration security gate, if any, the following
screen is displayed.

Electronic Commerce Configuration Screen

 

 
    
    
  
   
  
 

AGRE Electronic Commerce Configuration MFGCFG
Division A

Ven

2=Change 4=Delete P=Parameters S=Security
Opt Ven Name Com Description

Bottom
F3sExit FS=Refresh Fé=Add Roll

O Press F6é=Add.

Add Vendor/Comm Package Window

   
  
    
  
   
  
   
 
 
 
 
  

 

AGRE Electronic Commerce Configuration MFGCFS
Division aA

 

ven

2=Change 4=Delete P=Parameters s=Security
cpt Ven Name Com Description

Add vendor/Comm Package :

Vendor Id --
Manufacturer Id. .
Communication Pkg .
Version...

 

Fa=Prompt F12=Previous

        
 

F3sExit F5=Refresh

 

O With the cursor in the Vendor Id field, press F4=Prompt to select from a list
of valid vendor codes that you set up in Configure Vendor/Class (X38-1).


X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION

Select Vendor List

AgR EQUIPMENT SALES
Division A

Vendor

1=Select.

opt Vendor
FAR
FOR
GEH
HDC
HES

F3-Exit
Electronic Commerce Configuration

FARMHAND
FORD

GEHL

HARLEY DAVIDSON
KESSTON

F3=Exit  FS=Refresh

: curity
: ion

: or/Comm Package

: ndor Id
: Mufacturer Id. .
: mmunication Pkg .

O Press [PgDn] to display more vendors.

Do not add
vendors unless
you have
installed their
communications
software on the
Pc.

 

£1 Select the vendor code you use for the manufacturer, such as FOR in the
illustration, with 1=Select. The display returns to the Add Vendor/Comm
Package window.

C1 Press [Tab] to place the cursor in the Manufacturer Id field.

O Press F4=Prompt in the Manufacturer Id to select froma list.


SECURITY & CONFIGURATION X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION 19

Select Manufacture Id List

 

A&R EQUIPMENT SALES Electronic Commerce Configuration MFGCEG

Select Manufacturers Id

: IsSelect

Mig

AGC AGCO

CAS CASE CORPORATION

CNT Clarknet

NHD New Holland North America, INC.

Bottom :

+ F3sExit Roll

F3sExit FS5=Refresh

 

O Press [PgDn] to display more manufacturers.

O Select manufacturer’s ID, such as NHD (New Holland), with 1=Select. The
display returns to the Add Vendor/Comm Package window.

O Press [Tab] twice to place the cursor in the Communication Pkg Field.
0 Press F4=Prompt in the Communication Pkg field to select from a list.


20 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION

Select Communication Package List

A&R EQUIPMENT SALES Electronic Commerce Configuration

Division

Ven
AGC
cas
cnr
NED

2 F3sExit

F3=Exit

BR

Select Communication Package

Name

AGCO SOLUTIONS ON-LINE

CASE VSAT/LEASE COMMUNICATIONS
Clarknet III

New Holland Des

Roll

FS=Refresh

O Press [PgDn] to display more communications packages.

O Select Communication Package, such as NHD (New Holland DCS), with
1=Select. The display returns to the Add Vendor/Comm Package window.

O Press [Enter]. If you are not configuring Ingersoll-Rand or New Holland,
you will return to the Electronic Commerce Configuration screen, which
displays the Vendor/Communications package.

O Ifyou are configuring New Holland, the following screen prompts you for a
Valid Dealer Number (required) and User Code, which are provided by New
Holland. When you press [Enter], you will return to the Electronic Commerce
Configuration screen, which displays the Vendor/Communications package.
MFGCFG

Bottom :


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION

Dealer Number Prompt

A&R EQUIPMENT SALES
Division A

Dealer Code . . 01234
User Code .

F3sExit  F5=Refresh

Electronic Commerce Configuration

Description
AGCO SOLUTIONS ON-LINE

vendor Id . se
Manufacturer Id. .
Communication Pkg .
Version . :

Fl2=Previous


22 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1

If you are configuring Ingersoll-Rand, the following screen is displayed:

A&R EQUIPMENT SALES CONFIGURE COMMUNICATIONS INGRANDSO1
INGERSCLL-RAND VER 1.00

Manufacturing Plant or Distribution Warehouse
Account Number

Invoice Type

Date Last Weekly Order 000000 <——— No input

 

Manufacturing Plant or Distribution Warehouse 30 characters.

Account Number 11 characters. (
Invoice Type 3 characters.
Date Last Weekly Order Date (MMDDYY). No input.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 23

Parameters

Electronic Commerce Configuration Screen

AGRE Electronic Commerce Configuration
Division A

ven

2=Change 4=Delete P=Parameters S=Security
Opt ven Name Com Description
P FOR New Holland DCS NHD New Holland pcs

Bottom

FisExit PS5=Refresh Fé=Add = Roll
DIS-9913 Vendor FOR has been added

 

O From the Configure Communications screen (X6.15-1), select the
manufacturer with P=Parameters. The Configure Communication Devices
screen is displayed with a list of the types of transactions that can be
transferred. Not all vendors support all transaction types. The types are:

FIN Financial Statement
INV Part Locator Information
ORD Stock Order

ORD-CORP Corporate Stock Order
ORD-DROP Drop Ship Order
ORD-EMERG _ Emergency (Priority) Order
ORD-UP PSO# Upload

RIN Return


24 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION
The table below shows the transactions, which will be supported by each
manufacturer:

Manufacturer’s
Communications
Package

AGCO Sol'ns On-Line
Clarknet Hl

 

Ingersoll-Rand
KubotaLink

New Holland DCS
Triad (Custom Code

 

 

Configure Communication Devices Screen

   

 

A&R EQUIPMENT SALES

Division

2-Change
Opt

NYNNAND

F3sExit

Transaction

Transaction
PIN

Inv

ORD
ORD-CORP
ORD-DROP
ORD-EMERG
RIN

FS=Refresh

Configure Communication Devices

Workstation Name

Library

DISSYSOBI
DISSYSOBI
DISSYSOBI
DISSYSOBI
DISSYSOBI
DISSYSOBT
DISsysozg

MFGPRM

Your screen
may look
different. Not
all vendors
will have the
same
transaction
list.

Bottom

 

O To change a parameter, select a transaction with 2=Change. You can select
more than 1 transaction before you press [Enter]. The Change Device Parms
window opens.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 25
ee ecco eee

Change Device Parms Window

ARR E Configure Communication Devices
Division
Transaction

Change Device Parms :
Transactio
PIN Transaction... . FIN Use the AS/400
INV Workstation Name . ELISABES<— Workstation
ORD : Library DISSYSOBI
ORD-CORP SC; Name from page

ORD-DROP: 9 (Windows

ORD-EMERG : 3.11) or page 12

RIN : Fl2=Return

(Windows 95).

Bottom
F3=Exit FS=Refresh

 

1 For “Workstation Name,” enter the name determined on page 4 (Windows
3.11) or page 7 (Windows 95)--the PC where the manufacturer’s
communications software is installed. Make sure the Workstation Name is the
same as the AS/400 Workstation Name used in the General Configuration of
DIS Electronic Commerce Client (see page 8). The name of the library
remains DISSYSOBJ. which is the default.

1 Press [Enter] to record the information. If you selected more than 1
transaction type, the next one will be presented.

O) When all transactions have been processed, you'll return to the Configure
Communication Devices screen.

O To return to the Electronic Commerce Configuration screen, press F3=Exit.

Security

In this section, you’ll establish a security key and expiration date for each type of
transaction. Until security is fully implemented, everyone will use the same
security key and expiration date. Don’t worry—your transactions will be perfectly
safe.


26 X6.15-1 ¢ ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1
eee OELEASE 2.1

 

Electronic Commerce Configuration Screen

 

A&R EQUIPMENT SALES Electronic Commerce Configuration MFGCFG
Division A
ven

2sChange 4=Delete P=Parameters $=Security
Opt ven Name Com Description
S FOR New Holland DCS NHD Wew Holland pcs

Bottom
F3=Exit  FS5sRefresh Fé=Add Roll.

 

O From the Electronic Commerce Configuration screen (X6.15-1), select the
manufacturer with S=Security.

 

Configure Security Screen (
A&R EQUIPMENT SALES Configure Security MPGSEC
Division

Transaction
2=Change
Expiration

Opt Transaction Security Key Your screen may Date

2 FIN look different. Not 000000
2 INv all vendors will 000000
2 ORD oo0cce
2 ORD-CORP have the same 000000
2 ORD-DROP transaction list. 060000
2) ORD-EMERG o00000
2 RIN 000000

Bottom

F3sExit FS=Refresh R011

 

 

O To add or change a security key, select each transaction type with 2=Change.
You can select more than 1 transaction type before you press [Enter]. The
Change Transaction Security window opens.


SECURITY & CONFIGURATION X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION 27

 

 

Change Transaction Security Window

 

A&R EQUIPMENT SALES Configure Security MFGSEC
Division

u
"

 

weunnnnd

Transaction

Change Transaction Security

FIN

Transaction .
Security Key.
Expiration Dal

  

F12=Return

  

Bottom

F3sExit  FS=Refresh Roll

 

0 For the Security Key, type:

AGC for AGCO Solutions On-Line
cnt for Clarknet II

ING for Ingersoll-Rand

KUB for Kubota

NHD for New Holland DCS

For the expiration date, type: 123199.

Press [Enter]. If you selected more than 1 transaction type on the previous
screen, the next one will be presented.

When all transaction types have been processed, you’ll return to the Configure
Security screen. To return to the Electronic Commerce Configuration screen,
press F3=Exit.

Repeat this process, Configuration — DIS Electronic Commerce Manager,
which begins on page Error! Bookmark not defined., for each vendor you
have communications software for. In the case of AGCO, repeat for every
vendor associated with AGCO. Select the same Manufacturers Id for each
AGCO vendor. Don’t forget the Parameters and Security screens!

Repeat this process for each division in all file sets.


28 X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1

STARTING COMMUNICATIONS PROGRAMS

AS/400 Program: Electronic Commerce Manager

O Normally, the DIS Electronic Commerce Manager (DISECM400) nuns 24-
hours a day except when it is stopped by an IPL. It will be restarted after the
IPL. The jobs that use the Electronic Commerce Manager will start it if it is
not active: finalizing an order or return, or downloading a formatted financial
statement or parts locator file. You can verify that the job is running by typing
the following command at an AS/400 command line: WRKACTJOB [Enter].
Look for the job illustrated below:

 

Subsystem/Job User Type CPU % Function Status
DISECM400 ess SBS +0 DEQW
DISECN400 QPGMR BCH -0 PGM-MFGSOCENGG © DEQW

 

DIS Electronic Commerce Client (ECC)

The programs that process data on the PC are shut down whenever the PC is
rebooted or powered off; therefore, they must be restarted afterwards. Follow this
procedure every morning. Repeat it any time the PC is rebooted or Client Access
is restarted.

1. Start the PCs where the manufacturer’s communications software and ECC is
installed.

2. Start the DIS Business System on the PCs. This starts the Client Access
connection between the AS/400 and the PCs.

3. Start ECC. ECC starts the data queue on the AS/400 and the polling process.
It must be running for information to be transferred successfully to and from
the AS/400 and the PCs.

Windows 3.11

— Tostart DIS ECC from Program Manager, double click on the DIS
Applications icon. Within the DIS Applications group, double click on the
DIS Electronic Commerce Client icon.

Windows 95

— Tostart DIS ECC, select Start | Programs | DIS Applications | DIS
Electronic Commerce Client.


SECURITY & CONFIGURATION X6.15-1 « ELECTRONIC COMMERCE CONFIGURATION 29

 

### Troubleshooting

To verify that an itern (order, parts locator file, return, etc.) has been successfully
downloaded and is ready for transmission to the manufacturer, look in the DIS
Electronic Commerce Client window on the PC where the log is displayed. Look
for the line: “Destination file closed,” which means the order has been transferred
from the AS/400 to the PC in the format requested by the manufacturer.

If you don’t see the line, you can wait for the next polling time—the DIS
Electronic Commerce Client polls the AS/400 every 10 minutes (or the number
you set in Configuration).

Tf you are in a hurry, you can click on More Detail>> to expand the dialog box,
then click on Check AS/400 Now! to poll the AS/400 immediately.


30 X6.15-1 » ELECTRONIC COMMERCE CONFIGURATION RELEASE 2.1

Notes:

## CHAPTER X6.15-2

BACKUP ELECTRONIC COMMERCE
CONFIGURATION FILES

### Introduction

Use this option to back up your Electronic Commerce configuration files. DIS
Electronic Commerce Manager 400 runs in Library DISFILES, so it doesn’t
interfere with DIS Backup. Since the configuration is not included in DIS Backup,
this option is used for backing the configuration up to tape, use option 3 to restore
it in case of emergency.

Before you start, please make sure that you are using TAPO] and that you have

removed your DIS backup tape.

 

### Contents

ENTRANCE SCREEN

Electronic Commerce Mem


2 X6.15-2 » BACKUP ELECTRONIC COMMERCE CONFIGURATION FILES RELEASE 2.1

ENTRANCE SCREEN

Electronic Commerce Menu

 

COMMAND MENU: X6F
({c; DIS Corp.

2. Electronic Commerce Configuration

2. Backup EC Configuration Files
3. Restore EC Configuration Files

23. Return To Security & Configuration Menu

Ready for option number or command
==>_2.

 

 

  

 

O From the Electronic Commerce Menu, (X6-15) select option 2, Backup EC
Configuration Files. Press [Enter]. At the bottom of your screen, the following
messages will appear:

Checking tape drive TAPO1.
Initializing TAPO1.

Saving MFG400 configuration data...
Backup of DIS Manufacture configuration data completed.

The Electronic Commerce configuration files are backed up.

Label your tape “Electronic Commerce configuration files” and store it in a safe
place off-site.

## CHAPTER X6.15-3

RESTORE ELECTRONIC COMMERCE
CONFIGURATION FILES

### Introduction

Use this option to restore your Electronic Commerce configuration files in case of
emergency.

Before you start, please make sure that you are using TAPO1 and that you have
removed your DIS backup tape.

### Contents

   

ENTRANCE SCREEN............
Electronic Commerce Menu...

  

iv bo


2 X6.15-3 « RESTORE ELECTRONIC COMMERCE CONFIGURATION FILES RELEASE 2.1
ee eee A IN TS CRIELEASE 2.7

ENTRANCE SCREEN

Electronic Commerce Menu

COMMAND
(c) DES Corp.

cTRONIC COMME

- Electronic Commerce Configuration
» Backup EC Configuration Files
» Restore EC Configuration Files

+ Return To Security & Configuration Menu

Ready for option number or command
==>_3

 

 

 

O From the Electronic Commerce Menu, (X6-15) select option 3, Restore EC
Configuration Files. Press [Enter]. At the bottom of your screen, the following
messages will appear:

Checking tape drive TAPO1.
Restoring MFG400 Configuration...

Restoring configuration data for AGCO SOLUTIONS ON-LINE.
Restore of MFG400 Communications completed.

The Electronic Commerce configuration files are restored.

## CHAPTER X6

SECURITY AND CONFIGURATION MENU

### Introduction

commaND:
(¢) DIS corp.

. Backup and Restors Files Menu - Initial Data mnery Menu
. Apply Enhancements
OPTDIS Master Menu . Prepare Partial Procedure
. List Of Files On Disk . DIS Business System Setup
. Security Audit Report : Point of Sale Security

. Security Maintenance OPT Report
. Initial File Setup

23. Return To Master Menu

Ready for option number or command

=s=>

 

X6-1 Backup & Restore Files Menu

Options on the Backup & Restore Files Menu enable you to back up your
dealership's files and run divisional end of day jobs at night after everyone
is off the system. The automated backup runs Communications End of
Day for Case, during which the prices of Case/IH parts that were inquired
on during the day are updated (if they are in an updatable class).

X6-3 OPT DIS Master Menu

Set options for the DIS Library. These options have been combined and
grouped by application on the OPT DIS Master Menu. When you select an
application, such as Receivables, the options that are available are listed
on the screen, When option switches are set in the DIS Library, they apply


[2] X6 SECURITY AND CONFIGURATION MENU

to all divisions. In every case, the first option is the default: the standard
configuration for the DIS Library. You do not need to set any switches if
you prefer the first option.

X6-4 List of Data Files on Disk

List of Files on Disk shows you all the files currently on the disk and all of
the free space available on the disk.

X6-5 Security Audit Report |

This printed report identifies which users have correctly passed security
gates since the last time a security code was changed.

X6-6 Security Maintenance

A Division is usually a store. Security Maintenance allows you to add or
delete a division. Information associated with each division such as name
and address, security, etc is changed or supplied in Security Maintenance.
Master Security for the entire system can also be changed in Security
Maintenance.

X6-7 Initial File Setup

Initial File Setup allows you to create missing files. Initial File Setup adds
missing files to an existing file set. Data in existing files are preserved.

!

RELEASE 2.1 W


X6 SECURITY AND CONFIGURATION MENU [2]

X6-8 Initial Data Entry Menu

The Initial Data Entry Menu includes jobs that are used to manually add
information to the DIS System after it has been installed.

X6-9 Apply Enhancements

Apply Enhancements allows you to modify your DIS System with the
most recent PTF (Program Temporary Fix) updates from DIS, apply
Communications and other modules, and apply custom code.

X6-10 Prepare Partial Procedure

Prepare Partial Procedure is used to recover certain jobs that did not
complete. For example, you may be in the middle of a job and the
electricity goes off. Most jobs now have recovery procedures that display
when they fail.

X6-11 DIS Business System Setup

The DIS Business System Setup can perform the following tasks:

Reload the DIS Library

Load a fresh copy of the Query dictionary

Convert a new file set, such as a newly acquired dealership
Load an auxiliary PTF (Apply Enhancements could be used as
well)

= Load the sample company files (Z-files)

The setup option can do all this without much help from you. It is so

‘ SECURITY AND CONFIGURATION


[«] X6 SECURITY AND CONFIGURATION MENU

self-sufficient that it comes with an Express setup. For more complicated
and unusual situations, there is a Custom setup.

X6-12 Point of Sale Security

Point of Sale Security is used to set up User IDs and passwords that
control what the user is allowed to do on a Point of Sale document.
Controlled functions include reopening documents, cancelling documents,
using all sales codes.

X6-13 OPT Report

The OPT report lists the current option settings from the DIS OPT Library,
which is located at X6-3. All options are listed including those which (
retain their default settings.


X6 SECURITY AND CONFIGURATION MENU [=]

### Restoring Data Files

It may be necessary to restore your data files from a backup when your
system has encountered an unrecoverable error. Please consult with the
Response Line to determine if this is the best solution for you.

When this procedure is performed, all of the data that is currently on your
system is replaced with data that was on your system before the error
occurred. The critical elements of this procedure are a current backup of
your data files and an exact audit trail to help you recover to the current
day and time.

O First, find your most current backup. It is a good idea to CATALOG it
to make sure your backup files are complete.

G If you have an AS/400 with a tape backup, find the last backup tape
created before the error occurred. Put that tape in the drive and type:
DSPTAP and press [Cmd4]. The following screen appears.

 

SECURITY AND CONFIGURATION


Le] X6 SECURITY AND CONFIGURATION MENU

Display Tape (DSPTAP)

Type choices, press Enter.

Tape device | - : Name

File label . + TALL

Sequence number . 1 21-9999
Datatype . | fe *LABELS *LABELS, *SAVRST.
ourput pee *, *PRINT

End of tape option... . *REWIND *REWIND, *UNLOAD

Bottom
F3sExit  F4=Prompt  F5=Refresh Fl2=Cancel  F13=How to use this display
F24sMore keys

 

O In the "Tape Device" field enter the name of your tape drive (usually
TAPO1). Change the "Output" field to read *PRINT and press [Enter].
Review the printout to verify that it contains your user files.

D Alert other departments and divisions that the delete and restore is
imminent.


COLLECT INFORMATION TO RECREATE THE DATA

O Run acurrent financial statement (X15-2).


O Gather all edit lists from posting since last backup.

### Parts And Point Of Sale

QG Run an Open Documents Report (X56-2) and gather those invoices.
Note any new parts added to currently open documents.

Q Gather all invoices ciosed since the backup.

O Gather all orders created and received since the backup.

 

Q Run an inventory summary (X36-1) for all vendors.

### Restore The Backup

Once all the information is gathered for each department and division, do
the following:

0 Advise all users to sign off.

O Run Accounting End of Day (X1-9) and Parts End of Day (X3-9).
O Do an Immediate Backup (X61-1) to tape.

SECURITY AND CONFIGURATION


Le] X6 SECURITY AND CONFIGURATION MENU

O When this job is complete, take option X61-4 to Restore From Backup.
Remember to use the backup tape that you identified earlier as the most
current backup before the unrecoverable error. This is the data you
want to restore in order to have a fresh start at the job that caused your
error.

O When the restore is complete, you may begin recreating your old
records and bring your system back up-to-date.

### Bringing The System Back Up To Date

Note: This section is concerned with bringing your restored libraries up-

to-date by adding transactions that occurred subsequent to the last backup.

While adding this information, it is important that no new work be added (
to system.


0 Using Accounting End of Day (X1-9), re-create new address numbers
and G/L account numbers.

O Re-post transactions using edit lists or the Accounting End of Day (X1-
9).

O When you think that you have completed your recovery work, run a

new financial statement and subledger balance report and compare to
the one just prior to the delete and restore.

RELEASE 2.1 Lu


X6 SECURITY AND CONFIGURATION MENU [2]

UNITS
O Set up any new units.

PARTS AND POINT OF SALE.

O Using the Parts End of Day report and invoice copies, carefully recreate
Point of Sale tickets in the exact order as the originals.

O Re-receive parts orders.

OD Re-create stock and priority orders.

0 Using the open documents report, put parts back on open workorders.

G Review the Changes to Quantity Report from Parts End of Day. If the
program field says X32001, look in the Transaction field for changes
made to your parts inventory through Parts Posting and Maintenance.

Re-create those changes now.

O Run the new inventory summary pads and compare to those run just
prior to the delete and restore.

### Restore Daily Work

Once all your data is reconciled, you may continue to work on your
system as you normaily would.

SECURITY AND CONFIGURATION


Notes:

RELEASE 2.1 CU

## CHAPTER X7-9

BEARING INTERCHANGE MENU

### Introduction

‘COMMAND
(c) BIS corp.

BEARING INTERCHANGE MENU

i. Restore Bearing Interchange Information
2. Bearing Interchange Mfr Name/Vendor Code Table

23. Return to Manufacturers Menu

Ready for option number or command

ss=>

 

The Bearing Interchange Menu, illustrated above, consists of 2 jobs.
Option 1 loads Bearing Interchange information onto the hard disk. It is
stored in Library QS36F in file BIX. In addition, the following alternate
index files are used: BIXLO, BIXL1, and BIXL2.

Option 2 is a table that cross-references manufacturers from the tape to
your 3-character DIS vendor codes. Up to 10 DIS vendor codes can be
assigned to a single manufacturer. The table must be completed before the
Bearing Interchange information will be available in programs that use the
parts search feature:

= Parts Inquiry (X3-1)


[2] X7-9 BEARING INTERCHANGE MENU

Parts Posting & Maintenance (X3-2)

Correct Stock Order or Create Manual Order (X341-2)
Correct Order Before Receiving (X342-1)

Part Lists (X37-6)

Point of Sale Invoicing (X5-1)
{
NU


X7-9 BEARING INTERCHANGE MENU [=]

### How To Use

When the Bearing Interchange Manufacturer Name/Vendor Code table has
been completed, you can locate a part in your inventory that corresponds
to a Bearing Interchange part number by using the parts search feature.
The following example is from Point of Sale; however, the process is the
same in other jobs. In some cases, fewer selection screens are required.

CASE POWER & EQUIPMENT SALES ORDER
COUNTER TICKET # CT00234 For DEMEQL

X5100-106
CHARGE OFEN 4/06/95
v
Ext Price

TDP Line # Qty Vnd Part Number Description Bin

Spec order parts 00 avail total

PARTS CUSTOMER

TDI/W Pty Line SC Ven Qty Part number
5 0010 PC CAS #896
Standard line code Lost sale No demand

 

 

 

 

 

Type a pound sign followed by the part number (no blank after the #),
such as #896, and press [Enter]. A list of Interchange groups is
displayed.

MANUFACTURER


List of Interchange Groups

CASE POWER & EQUIPMENT SALES ORDER %X5100-106
COUNTER TICKET # CT00234 For DEMEQI 4/06/95

Ext Price
+ Search Interchange for Division A x30090 :
: Select Interchange xp
+ Type option, press Enter
=Select Search For
: 896
: Opt Manufr. Part Number In/chg No.
1 PEUGEOT 896 12456
UNTROYAL 896 70659
GENBEARCO 70795
CCELCANADA 896 73812
CROSLAND 896 F1312 :
BIG A F2290 : (
DELUXE 896 F2652 : -00

Bottom: ice Base
F3eExit Roll 4
ode

 

O Select the group you want by typing "1" beside it in the column labeled
"Opt" and press [Enter]. A list of manufacturers is displayed.

RELEASE 2.1 LU


List of Manufacturers

CASE POWER & EQUIPMENT 5100-106
COUNTER TICKET # CTO0234 4/06/95

: Search Interchange for Division A
Select Manufacturer
Type option, press Enter
1=Select

: Opt Manufr
ce
CARLTON
CASE-18

F3=Exit Roll

 

O Select the manufacturer with a 1=Select, and press [Enter]. A list of
equivalent part numbers appears.

MANUFACTURER


List of Replacements

CASE POWER & EQUIPMENT 5100-106
COUNTER TICKET 4 CT00234 CHARGE OPEN 4/06/95

Ext Price
: Search Interchange for Division A «30092 :
: Select Part Interchy Grp
: Type option, press Enter 12456
IsSelect Part orig Number
: cASE-In as
: Opt Replacement avail Bin Loc
040007
0410375
11761081
31238
323465991 :
: 3148966R91 2 {
Spec or : 3216466R91
PARTS ¢ : 380129291
rDIMW:
5 + F3sEeie Roll
Standar :

 

 

 

 

Select the part number with 1=Select, and press [Enter]. The part
number is placed on the Point of Sale document.

 

RELEASE 2.1 Lo


CASE POWER & EQUIPMENT SALES ORDER XxS5100-106
COUNTER TICKET # CT00234 For DEMEO] CHARGE OPEN 4/96/95

v
DP bine # Qty Vnd Part Number Description Bin Ext Price 5
5 o010 B= 1 CAS 70523 WASHER, 6863 9.64

Spec order parts +00 Avail total 20.12 Total
PARTS CUSTOMER
TDIswW Pty Line SC Ven Qty Part number
5 0020 PC CAS
Standard line code Bost sale No demand
Available C/T Res. R/O Res. On Order Super. Bin
4 1 0 4 N «B63

 

MANUFACTURER


Notes:

## CHAPTER X7-15

FARM PLAN MENU

### Introduction

This chapter shows how Farm Plan/Agline Communications allows you to
process credit card sales and describes options on the Farm Plan/Agline Menu.
For more information on Credit Cards, see Credit Cards in Point of Sale (XS-1).

 

Farm Plan/Agline transactions are manually authorized and transmitted to
Farm Plan/Agline, not First Data Resources (FDR).

### Contents

CREDIT CARD SETUP OVERVIEW...
AUTHORIZATION OF FARM PLAN/AGLINE SALES
POINT OF SALE POSTING BATCH......c.csscssssecesseeees


2 X7-15 » FARM PLAN RELEASE 2.1
——— oe eSSSSFSSSSFSSSFFSESEFEFSEIELEEADSE 27

### Entrance Screen

The Farm Plan/Agline Communications Menu is illustrated below,

COMMAND
{c) DIS Corp.

. Transfer/Transmit
« Configuration

. Return To Manufacturers Menu

Ready for option number or command

Note If the postal code in Security Maintenance (X6-6) is U.S., the menu and
screens show “Farm Plan”; if Canadian, they are labeled “Agline.”

After Farm Plan/Agline transactions have been posted in Point of Sale, you'll use
Transfer/Transmit (X7.15-1) to transfer the batches to Farm Plan/Agline. Posted
Farm Plan transactions are stored in a file called "u.FPA" on the DIS Business
System. The Transfer/Transmit option transfers the file from the AS/400 to the
PC, then calls Farm Plan's Communication program which transmits the
information to Farm Plan. An authorization code is required for a transaction
when the total is $500 or more. This limit is in the software and can be changed
by DIS only. On a single transaction, an authorization code is entered at the time
the point of sale document is closed and is not required in Transfet/Transmit. If
the transaction is entered through Create Source Documents and is $500 or more,
an authorization code will be required in Transfer/Transmit.

In addition, the following configuration step is required:

Farm Plan/Agline Configuration (X7.15-2). Farm Plan assigns information to
the dealership for communications. It is the information that the Farm Plan
computer will be expecting. In the Configuration option, you configure the
computer to match the computer at Farm Plan. You must configure before you
can communicate with Farm Pian. Once the information is entered, do not change
it without consulting DIS or Farm Plan.

### Manufacturers X7-15 * Farm Plan 3

If it is necessary to post Farm Plan/Agline transactions through Create Source
Documents, use FP or AG in the last 2 positions of the debit to the customer’s
account.


4 X7-15 » FARM PLAN RELEASE 2.1

 

### Installing Farm Plan Communications On The Pc

The following procedure will place the software on the hard disk of the PC. You
will not need any diskettes when you communicate.

O Hot Key to the PC.

Use this diskette:
PC - EXECUTABLE
FARMPLAN COMMUNICATIONS

O1 Insert the program diskette into drive A.
C1 At the A:\> prompt, type: setup[Enter]

Tf you are asked to enter your hard disk drive:

Enter Your Hard Disk Drive (B-J}:

O Type: ¢ [Enter]

if you are already using Farm Plan, the following message will be displayed:

Unable to create directory

This is normal. It means that a FARMPLAN directory already exists on your hard
disk. The program will continue. The following messages will be displayed:
Creating your Farm Plan Batch program
DIS Farm Plan Setup Has Completed

C: \FARMPLAN>

The Farm Plan setup is completed
CREDIT CARD SETUP OVERVIEW

Here are the steps to setup a Credit Card:

1) Account Maintenance (X14-2). Decide on a general ledger account for Farm
Plan.

2) Receivables Maintenance (X11-2). Create a receivables address number for
Farm Plan.

3) Farm Plan Communications (Menu X63B). When this OPT is on and you
go into Credit Card Configuration, a credit card code of “FP” is automatically


MANUFACTURERS X7-15 » FARM PLAN 5

set up. You are required to furnish a receivables address and set EDC
Capable=N and Private Card=Y. If you are a Farm Plan dealer, this OPT is
already on. When this OPT is on you can go to Credit Card Maintenance
(X52-14) to verify that EDC Capable=N.

4) Receivables Maintenance (X11-2). Optional. Enter credit card information
for each customer and select a default to be used at Point of Sale Invoicing.

5) Credit Code Maintenance (X68-1). Optional. Set up a credit code to flash a
message at Point of Sale alerting salespeople that a customer needs to fill out a
credit card application.

AUTHORIZATION OF FARM PLAN/AGLINE SALES

1 Enter the Farm Plan/Agline credit card code (FP) on the Sold To screen in
Point of Sale.

O Process the document and close it by pressing [F2]. The Credit Card
Authorization screen is displayed, as illustrated below.

Credit Card Authorization

FP Farm Plan Invoice Amount

Card Number Exp. Date

Capture card number? ¥

Enter Y to store a new card number in
customer’s record for future use.

Enter to continue F4=Prompt Fé=Use Card Reader /Manval Entry
Fl0=Auto/Manual Authorization Fl2=Previous F1d=Re-Authorize

 

 

 

If necessary, enter the card number (without dashes) and expiration date.
Press [Enter] to continue. Farm Plan/Agline card numbers are checked for
validity, and if an invalid card number is encountered, an error message is
displayed at the bottom of the screen.

O To return to the document detail screen, press F12=Previous.

oo

The card number and expiration date are taken from the default specified on the
customer’s master record if they are present there. Both can be changed on this
screen. If no default has been specified, the first card number for the card code
from the customer’s list is used. If no card numbers have been set up for this


6 X7-15 » FARM PLAN RELEASE 2.1
oo SSeS oT

customer, the card number field will be blank, and the cursor will be positioned
there; otherwise, the cursor will be in the amount field.

C Press F4=Prompt in the following fields to select from a list of valid values:
© Card Code
e¢ Card Number

Authorization Field
Farm Plan sales of $500 or more require an authorization code before you can
leave this screen. This limit can be changed in the software by DIS only.

Capture Card Number?

To save the credit card number or an updated expiration date, make sure the
prompt “Capture card number” is answered “Y,” which is the default.

F6=Use Card Reader/Manual Entry

Press [F6] to toggle between manual entry (default) and swiping the credit card
through the reader to allow the system to read the card number.

F10=Auto/Manual Authorization & F14=Re-Authorize
Automatic authorization for Farm Plan sales is not available.

### Point Of Sale Posting Batch

The DIS Point of Sale posting batch will include all closed credit card
transactions at the time it is created. Charges to the customer’s account are
automatically reversed in the posting batch and charged to the credit card
receivable. Charges to the customer’s account are identified by the characters
“SC” in the last 2 positions of the description field.

Example:

Dalllo A COUNTER TI$C 000001 Carolynn Cain Construction
2 TICK

‘COUNTER
MSA, 000001 Carolynn Cain Construction

 

Automatic transactions, identified by *AUTO, are generated to reverse the debit
to the customer’s account. On the debit to the customer’s account, the original
document number is placed in the document number and description fields. On
the debit to the credit card account, the original document number is placed in the
document number field. The customer’s address is placed in the description field
with the 2-character code for the Farm Pian (FP) credit card in the last 2 Positions.


MANUFACTURERS X7-15 » FARM PLAN 7

Example
AUTO + 3-18-97 CTOUI7 #* C AlLIO |= A467 CTOOLE7 #*_ VANPOL WES VAN PELT
duro = 3-18-97 Tove? HD ALLLO = -R«6¢167 VANPOL-#P FARNFL FARM PLAN RECEIVABLES

For more information about using credit cards at Point of Sale, see Credit Cards
X5-1.

### Entering Transactions In Create Source Documents

If necessary, Farm Plan/Agline, credit card sales can be entered through Create
Source Documents. These transactions will be reversed automatically and can be
transmitted to Farm Plan. Since there is no way to associate a credit card number
with a customer in Create Source Documents, you will be asked for the credit
card number at the time the transaction is transmitted.

Make sure that:

= The 2 characters “FP” (or “AG” for Canadian dealers) are in the last 2
positions of the debit to the customer’s account.

= The same document number is used for all lines.

Example:

   

A&R EQUIPMENT SALES POST SOURCE DOCUMENTS 3/18/97 %1700-102
Division A Document Entry June
ID Document# Account# Amount Description Addr# Date Discount Stock#

© eroosce D A1120 80000 FP VANPOL
¢ croosce c A3360 gc000 VANPO1

Current Line 60

Cmdi-End job Cmd2-recurrent transactions Cmd3-Show Line# cCmd4-Show stock#

X7-15 ¢ FARM PLAN

Notes:

## CHAPTER X7-22

GENERAL LEDGER DOWNLOAD

### Introduction

The General Ledger Download prepares a file of account numbers, names,
and Year-To-Date (YTD) balances for any G/L month you choose. It uses
familiar Financial Statement screens, which means that you can download
data for a single division or any combination. If you have
departmentalized your general ledger, you can run a download by
department. The download is a standard procedure, which is used in many
of DIS's communications packages.

The download creates an ASCII (text) file, GLD.DIS on the PC, which can
be used with an Excel Spreadsheet. If you ever need Month-To-Date
figures, it will be necessary to download 2 months and subtract account
totals. For example, to calculate what happened in March, it would be
necessary to download figures for February and March and calculate the
difference. Since each download overwrites the GLD.DIS file, it is
necessary to rename the first download, such as GLDmm.DIS, where
"mm" is the month.

### Installation

Materials

DIS provides the following materials:

For the AS/400 1 PTF Tape for V8LAB and higher
For the S/36 1 PTF Diskette for V8L4B and higher

For the PC 1 PC Diskette with the download program


[2] X7-22 GENERAL LEDGER DOWNLOAD Cc

DIS Business System Software

O From the Security & Configuration Menu (X6), select option 9, Apply
Enhancements. insert the AS/400 tape or S/36 diskette and follow the
instructions on screen. When the menu returns, the Business System
software has been installed. You will find the new program on the
Additional Options Menu (X8).

PC Software

 

 

 

Press [Alt]+[Esc] to toggle (hot key) to the PC.

 

‘You may make a new directory for the download or use an existing (
directory. The name of the directory is not critical.

C To make a new directory, type: ed c= \ [Enter].

At the C:\> prompt, type: md gi1down [Enter].

Insert the PC diskette into drive a.

1) Change to the download directory:
At the c:\> prompt, type: c@ g1down [Enter]. Substitute the name of
the directory you want to use.
From the download directory, type: copy a:*.* [Enter].

 

 

 

 

This concludes the installation of the software.

RELEASE 2.1 LO

### How To Run

### Manufacturer

 

From the Additional Options Menu (X8), select General Ledger
Download. After passing a financial security gate, the Month Selection
Screen is displayed:

LBE'S RENTAL COMPANY GENERAL LEDGER DOWNLOAD x7M00-201 2
Division: A Month Selection

Enter the month for which a GL Download is desired (1-13)
Is this download for an open or closed month? Enter '0' or
Select either current or previous year Enter 'C' or

 

Examples: Month Open/Closed
Download for most recently closed month 4 c
Download for current month 4 °
Download for oldest open month 5 °
Download for the “thirteenth” month*

- The -thirteenth* month download is your fiscal year end month plus
adjusting entries.

Cmdi-End job Cmd2-Select by department Cmd3-Select by division

The screen defaults to the oldest closed month. Select the month by the
calendar year, such as August = 8, September = 9, and October = 10 in the
example above. Figures on the General Ledger Download are based on the
fiscal year-to-date. If your fiscal year begins April 1, and you request a


[+] X7-22 GENERAL LEDGER DOWNLOAD c

download for month 8, you will get year-to-date figures for April -
August.

O Enter the month for the General Ledger Download. If the month is
open, enter O. If the month is closed, enter C. On the next line enter C
if you want the download for the current year or P if you want it for the
prior year.

Command Keys

Cmd2 Select by department. If you have departmentalized your
Sales, Cost of Sales, Income and Expense accounts as
explained in General Ledger (X1-4), you may select the
department by pressing [Cmd2].

Cmd3 Select by division. If you have more than one division and {
have similar account numbers, you can combine the
divisions for a General Ledger Download containing all
divisions.


X7-22 GENERAL LEDGER DOWNLOAD [=]

Select By Department

We will assume you have departmentalized all Sales, Cost of Sales,
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

Also, we will say our goal was to have each department receive credit for
the sales they made. This will help the shop offset their high expenses for
electricity with income generated by parts sales for equipment they are
working on. See a sample chart below:

PARTS-WHOLESALE A33001

PARTS-INTERNAL A33103
PARTS-COUNTER A33201
PARTS-SHOP A33302
OTHER INCOME-PARTS AS50501
OTHER INCOME-SERVICE A50502
OTHER INCOME-SALES A50503
OTHER INCOME-ADMIN. AS50504

MANUFACTURER


Le] X7-22 GENERAL LEDGER DOWNLOAD cC

TELEPHONE EXP.-PARTS A67101
TELEPHONE EXP.-SERV. A67102

TELEPHONE EXP.-SALES A67103
TELEPHONE EXP.-ADMIN. A67104

To find out if the goal has been reached, we want to run a General Ledger
Download for the service department. The department code is 2.

O To select by departments, press [Cmd2]. The Department Selection
screen appears.

RELEASE 2.1 CO


MANUFACTURER

 

X7-22 GENERAL LEDGER DOWNLOAD | 7 |

Department Sefection Screen

LEE'S RENTAL COMPANY GENERAL LEDGER DOWNLOAD X7M00-102 2
Division: A Department Selection

Department selection mask: XXKXK2RK

To select all departments and all accounts, the mask must be all ‘x'.

To select all departments and summarize on a major portion of the account

number, enter a '*' in the mask where the minor (department) portion of the
account numbers begin.

To select a specific department, enter the character(s) that identify that
department. Be sure to place them in the mask exactly where they appear in
the account numbers.

Examples:
Assume general ledger accounts A100A and 1008 which represent cash accounts
for departments ‘A' and 'B' respectively.

All accounts saoonocn:

Summarized OKO

Specific department secounear

Cmd6-return to Month Selection screen

 

Note the prompt, Department selection mask: "XXXXXXXX."

The "XXXXXXXX" represent the eight possible characters in a General
Ledger account number. Select the character representing the department
you want and enter it in over the "X" that is in that position. For example,
Parts Shop has an account number of A33302. The 2 in the last position of
the account number is the department code. It is in the sixth position of the


X7-22 GENERAL LEDGER DOWNLOAD cm

account number.

On the Department Selection screen, we have entered a "2" in the sixth
position of the "mask". This tells the computer to search all General
Ledger account numbers and report those that have a "2" in the sixth
position of the General Ledger account number. In this way, a General
Ledger Download is created for the service department, department 2.

If you want to download a composite of all departments, enter "*" in the
sixth position of the "mask". This tells the computer include all accounts
with anything in the sixth position of the General Ledger account number
on the General Ledger Download.

O When the department selection is made, press [Cmd6] to return to the
Month Selection screen. {

RELEASE 2.1 Le


X7-22 GENERAL LEDGER DOWNLOAD [2]

Select By Division

If you have more than one division, you can select any of or all of the
divisions and combine them on a single General Ledger Download. For
the comparison to be valid, you must have the same General Ledger
account numbers in all divisions.

O To select by division, press [{Cmd3]. The Division Selection Screen
appears.

LEE’S RENTAL COMPANY GENERAL LEDGER DOWNLOAD X7M00-203 3
Division: A Division Selection

To include other divisions in a composite GL Download, place any
character beside the divisions to include.

— B DEALER SALES & SERVICE, LTD, _ D ABC COMPANY
— E ABC COMPANY — M MOTORCYCLE CITY
= T THERMOXING

emd6-xetura to Month Selection screen

 

MANUFACTURER


X7-22 GENERAL LEDGER DOWNLOAD c

O Place any character next to the divisions to be included on the General
Ledger Download.

O When the selection is made, press [Cmd6] to go back to the Month
Selection screen.

On the General Ledger Download Month Selection screen, press Enter.
The final verification screen is displayed.

LEE'S RENTAL COMPANY GENERAL LEDGER DOWNLOAD x7MO0-104 4
Division: A Final Verification

I£ you have completed making your selections, press Enter to continue.
However, if you want to change your month, department or division selection,
press Cnd6.

You have selected: (
Month 4

Open/Closed

Year CURRENT

Department KKK

Division

Qndil-Bnd job Cmdé-return to Month Selection screen Enter to continue

 

In the above example, the choice is for the closed 4th fiscal month, for the
current year.

RELEASE 2.1 Co.


X7-22 GENERAL LEDGER DOWNLOAD |

 

 

 

 

Verify the choices made, and if they are correct, press Enter. If the
choices displayed are not the ones you want, press [Cmd6] to return to
the Month Selection screen. You can begin the selection process again.
The G/L Download is not placed on the job queue. Instead, you'll see
this message:

"The requested General Ledger Download is being
processed.

Please wait..."

When the file is ready to be transferred to the PC, the following screen
appears:

DOWNLOAD UTILITY x7000-E01
Business System to PC

To complete the data transfer to the FC:

- Hot-Key to the PC

- Type in DISTOPC to start the job on the PC side

cmdi-cancel

 

MANUFACTURER


[7] X7-22 GENERAL LEDGER DOWNLOAD laa

0 Hot key to the PC, as directed.

CO) Change to your download directory.

Type: distopc [Enter]. The file is transferred to the PC. Its name on
the PC is GLD. DIS. It is a standard ASCII (text) file 80 characters
long. The file is illustrated below.

 

 

 

 

RELEASE 2.1 LO


Sample Download File

ASH ON HAND 1000.00 s4o4
CAS ON HAND 9408
CASH ie BANK 10090.77 s4oa
PETTY CASH-CHANGE FUND 9408
WHOLE GOODS RECEIVABLES 9404
ACCOUNTS RECEIVABLE 1620.68 9400
WARRANTY RECEIVABLE 9404
CONTRACTS IN TRANSIT 9404
DOUBTFUL RECEIVABLES 9404
NEW TRACTORS 4467.00 9408
NEW EQUIPHENT 6978.00 9404,
USED TRACTORS & EQUIPMENT 1000.00 940%
NEW AcTOS 9a
USED AUTOS 2404
‘TRUCKS 9404
MOTORCYCLES, save
RENTAL SQUIPHENT s4oe
PARTS & ACCESSORIES 22801,75 9404
TIRES & TUBES 8750.90 9404
PREPAID INSURANCE sacs
PREPAID OTHER 9404

 

 

MoD eee ee

 

MANUFACTURER


Notes:

## CHAPTER X7.15-1

TRANSFER /TRANSMIT

### Introduction

This option is used to transfer batches to Farm Plan/Agline after Farm
Plan/Agline transactions have been posted. An authorization code is required for a
transaction when the total is $500 or more. This limit is in the software and can be
changed by DIS only. On a single transaction, an authorization code is entered at
the time the point of sale document is closed and is not required in
Transfer/Transmit. If the transaction is entered through Create Source Documents
and is $500 or more, an authorization code will be required in Transfer/Transmit.

Posted Farm Plan transactions are stored in a file called "u.FPA” on the DIS
Business System. The Transfer/Transmit option transfers the file from the DIS
Business System to the PC, then calls "CheckF” which transmits the information
to Farm Plan.

You can communicate with Farm Plan 24 hours per day, 7 days per week, and as
many times a day as desired.

DO NOT RUN THIS JOB FROM A PC ACTING AS A CONSOLE ON
THE 5364.

### Preparation

You must always perform the following steps before you communicate:

«Post all batches containing Farm Plan sales.
- Turn on the modem.


2 CHAPTER X7.15-1 ¢ TRANSFER/TRANSMIT RELEASE 2.1

ENTRANCE SCREEN

Tip

O From the Farm Plan/Agline Communications Menu (X7-15), select option 1,
Transfer/Transmit. Farmplan/Agline transactions are collected when a Point
of Sale Batch is posted. Transactions are identified “FP” or “AG” in the last 2
positions of the description field on the *AUTO debit transactions. For
example, here is the original debit to the customer:

 

 

Line# Date Document# Account # © Amount Description Addr#
10 ¢ 5-21-97 CT00280 #* D A1110 BR 170.80 FARM PLAN $C BECKCL

 

Here are the automatic transactions associated with it:

    

 

 

   
  
   

Line# Date Document# Account # E Amount Description Addr#
*AUTO * 5-21-97 CT00280 #* Cc A1110 A 170.80 CT00280 #*  BECKO1
*AUTO * 5-21-97 CTO0280 #* D A111 A 170.80 BECKOl FP FARMPL

       
 

The following screen is displayed only if an authorization code is required or a
credit card number is needed. It presents one transaction at a time.

A&R EQUIPMENT SALES FARM PLAN TRANSFER XTF10-101 1
Division: A Transaction Authorization

Authorization is required for Debit transactions greater than § 500.00

Authorization Division adéress# Reference Amount
oo0000 A DEVOOL FPOO005 00003504

Please enter your authorization code for this transaction.
cmdl-End Job


MANUFACTURERS CHAPTER X7.15-1 « TRANSFER/TRANSMIT 3
<< OOO —e—rr er ee eer OEorrerroroee

O Fumish the necessary information, in this case, an authorization code, and
press [Enter]. An authorization code is required for any transaction $500 or
more. This limit is in the software can be changed by DIS only. On a single
transaction, an authorization code is entered at the time the point of sale
document is closed and is not required in Transfer/Transmit. If the transaction
is entered through Create Source Documents and is $500 or more, an
authorization code will be required in Transfer/Transmit.

1 Process all transactions. When you are done, the next screen asks you to hot
key to the PC and start the download program for Farm Pian.

A&R EQUIPMENT SALES FARM PLAN TRANSFER XTFLO-303 1
Division: A

To complete the Farm Plan transfer:

Hot Key to the PC, type FARMPLAN, then press Enter.

cmdl-End Job

  

 

O Hot Key to the PC.
1 Change to the Farm Plan directory by typing: cd\farmplan[Enter]
O Atthe C:\FARMPLAN> prompt, type: £armplan [Enter]

During the transfer, the following screen appears:


4 CHAPTER X7.15-1 » TRANSFER/TRANSMIT RELEASE 2.1
eS ee

 
    
  
 
  

### Farm Plan Transfer

Transferring Farm Plan data from the DIS Business System

Records transferred: 1784

 
 

Omdi-End Job

When the transfer is complete, the following screen appears:

### Farm Plan Transfer Farmplan

Transferring Farm Plan data from the DIS Business System

Transfer is complete, press [Enter] to continue

(mdl-End Job

 

 

O Press PC-Enter to continue.

The transmitting process begins automatically.


MANUFACTURERS CHAPTER X7.15-1 ¢ TRANSFER/TRANSMIT 5

### Transmit

When PC-Enter is pressed from the previous screen, the transferred file is copied
to the CHECKF directory and the CheckF program is started. CheckF will prompt
you for additional information before transmitting the file to Farm Plan via
FPComm. If you have any difficulty with this, please consult your CheckF
manual.

The following message will be displayed:

Farm Plan file successfully transmitted.
Press enter to return to DOS.

O Press PC-Enter to exit. You will return to the C:\FARMPLAN> prompt.
O Hot Key back to the DIS Business System.

How to Restart

1 Ifa problem occurs during the transfer of data to the CHECKF directory, at
the prompt, type: restart [Enter]

The transferred file will be recopied to the CHECKF directory. The CheckF
program will begin. Please consult your CheckF manual for additional
information on CheckF.


Notes:

## CHAPTER X7.15-2

### Configuration

### Introduction

Farm Plan assigns information to the dealership for communications. It is the
information that the Farm Plan computer will be expecting. In the Configuration
option, you configure the computer to match the computer at Farm Plan. You
must configure before you can communicate with Farm Plan. Once the
information is entered, do not change it without consulting DIS or Farm Plan. For
additional information on Configuration see Credit Card Maintenance (X52-14)
and Credit Card in Point of Sale (X5-1).

### Entrance Screen

O From the Farm Plan/Agline Communications Menu (X7-15), select option 2,
Configuration. The configuration screen is illustrated below.

 

FARM PLAN COMMUNICATIONS XTF20-104
CONFIGURATION
WARNING: Do not change Farm Plan Configuration unless you have authorization
Transmission Site 4. . 9999 Transmit File Name . . FPA
Farm Plan Dealer # . . Next Transmission # . . 1
Farm Plan Bank #

cmd1-End job Enter-Continue


X7.15-2 » CONFIGURATION RELEASE 2.1

Fill in the Configuration Screen

D Enter the Device #, Transmit File Name, Transmission Site #, Farm Plan
Dealer #, and Farm Pian Bank # from the information received from Farm
Plan. Next Transmission # will be | unless otherwise specified by Farm Plan.
The number increases by one each time you transmit to Farm Plan.

O Press [Enter].

The following screen appears:

FARM PLAN COMMUNICATIONS X7F20-102
CONFIGURATION
WARNING: Do not change Farm Plan Configuration unless you have authorization
Transmission Site # - 09999 Transmit File Name . , FPA
Farm Plan Dealer 4 . . 999 Next Transmission # . . 000001
Farm Plan Bank # . . . 99999 Device # 2... 2...

Division Division

ee

Cmdl-Previous screen emd2-Delete Enter-Continue

O Enter the Device # assigned by Farm Plan.

O Enter the Next Batch #. The number increases each time you transmit to Farm
Plan.

O Assign the division codes associated with the dealer/bank numbers now on the
screen. For the divisions, assign the document classification code set up to
identify Farm Plan Sales and the Farm Plan address number.

Once configuration is complete, do not change it without assistance from DIS or
Farm Plan. If you make a change to the "Transmit File Name" on the
Configuration screen, the Setup procedure on the PC must be run again.

O Press [Enter] to accept the entries on the screen. You will return to the first
screen. Press [Cmd1] to return to the first screen without accepting the entries.
The fields at the top of the screen can only be changed on the first screen.

O To delete the configuration currently on the screen, press [Cmd2]


MANUFACTURERS X7.15-2 « CONFIGURATION 3

If all divisions have not been configured for Farm Plan Communications, the
following screen will appear:

FARM PLAN COMMUNICATIONS X7F20-001

WARNING:

Divisions exist which were not configured...

Be sure and configure all divisions before doing any

Farm Plan transactions.

Enter-Continue

 

Make sure all divisions making Farm Plan Sales are configured before you

Transfer/Transmit to Farm Plan (X7.15-1).

O Go back into the Configuration job. Add the omitted divisions to the
appropriate dealer/bank number combination.

There may be no Farm Plan sales in some divisions. If this is the case, you can
ignore the warning message and press [Enter] to continue.


X7.15-2 © CONFIGURATION RELEASE 2.1

Notes:

## CHAPTER X10-1

INQUIRE/UPDATE SERVICE UNITS
FOR FLEET MANAGEMENT

### Introduction

With this option, you can view and update information about equipment serviced
and sold to customers. You can add units and cash customers. A complete service
history is kept on each unit. Inquire/Update Service Units is also available from
the Additional Options Menu--[Cmd1 1] from Point of Sale Invoicing. In addition,

- you can access Inquire/Update Units from Point of Sale by pressing [Cmd1 8],
which goes directly to Recommended Maintenance. From Recommended
Maintenance, you can select command keys that take you to all screens in
Inquire/Update Units, including the View/Update screen.

In this chapter, you'll find instructions for using this option. For more information
about the features of the Service Management System and the Fleet Management
System including overviews, see CHAPTER X10, SERVICE MANAGEMENT
MENU FOR FLEET MANAGEMENT.

xa1_fleet.doc 11/27/00 1


2 X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3
SS ee ee ee ere CRIELEASE 2.9

### Contents

 
   
 
 
  


Command Keys on the View/Update Screen.. 5
Fields on the View/Update Screen.. 6
Add Equipment and Customers ... 9
How to Add Equipment....... 9
How to Add a Cash Customer 10

CMD5-SERVICE HISTORY
Fields on the Service History Screen..

 

 

CMD6-RECOMMENDED MAINTENANCE .........s.secessscossceenessesen id

Fields on the Recommended Maintenance Screen

"Drop In" Equipment - Not on File.
Cmd9-Add other jobs.......

’ Definitions of Print Options.

 
 
 
  
 
 
 
 

CMD7-SHIP TO LOCATION INFO
Select Ship To Screen
F2=Units .
F6=Edit

 
 
 
 
 
  

CMD8-UNIT INDEX ....

 

CMD10-UNIT SERVICE INFORMATION
F6=Edit ...
F9=Notes...
F15=Parts
F21=Print Unit Repair History
F2=History ..
F16=Costs

Unit Service Info Screen: Field Definitions.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 3

 

 

### Entrance Screen

From the Service Units Menu (X10), select option 1, Inquire/Update Service
Units. After the service security gate, the View/Update prompts appear.

 

 

 

  

 

A&R SALES & RENTALS Inquire/Update Service Units XA100-101
Division: A View/Update Search Only
Address # Name .....
License #
Serial¥
unit #. Cc Unit #

 

As in Service Management, unique serial
numbers are required for Fleet Management.

(m@i-End Cmd5-Service History Cmd6-Recommended Maintenance Cmd8-Unit Index
cmdi0-Add Cash Customer Add Equipment-Enter new Serial number

 

 

 

You can use any one of the following methods to proceed:

« Enter a customer's system address and press [Enter]. The first unit (by Unit #)
belonging to the customer is displayed.

= Enter a license number.

= Enter a unique serial number (existing or new).

= Enter a unit number.

= Enter a customer's system address and the customer's unit number (C Unit #).

« Enter a customer's system address and press Cmd8 to select from a list of the
units belonging to the customer. :

= Enter a few characters of the customer's last name and press [Enter] to select
from the customer index.


4 X10-1 » INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

Command Keys on the Entrance Screen

Cmd1-End

Press [Cmd1] to end the job and return to the Service Management menu. If you
entered Service Management from Point of Sale, you will return to Point of Sale.

Cmd5-Service History

Press [Cmd5] to see a listing of all repair orders on a particular piece of
equipment. See page 12.

Cmd6-Recommended Maintenance

This option displays the recommended service jobs that should be performed at
certain time or hourmeter intervals. Job codes can be added to the recommended
list, and an initial repair order with an estimate can be printed. See page 15.

Cmd8-Unit Index

Press [Crd] to see a list of a customer's units listed by serial number. See page
36.

Cmd10-Add Cash Customer
Press [Cmd10] to add a cash customer. See page 10.

A&R SALES & RENTALS Inquire/Update Service Units XA100~102
Division: A View/Update Current Equipment

Address # ...... COLEQL or COLEMAN FORKLIFT CORP.
License # :
Serial# + FOOL 2300 IOWA sT
Unit #. see Cc Unit # FL
po BELLINGHAM WA 98226
Make ... wee Phone 360 714 8578
Model
Year . . Warranty code .. N
Description .... Exp. date ....
Purchase date .. Engine # ..
Hourmeter .... Key code .. :
Reminder date .. 30197
A/C .. cee Job code

 

Cmdl-End Cmd3-Go back Cmd5-Service History Cmd6-Recommended Maint
Cmd7-Shipto Location Info Cmd8-Next Cmd10-Unit Service Info cmd19-Delete


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT §

From this screen you can select a particular piece of equipment and/or see each
piece of equipment for a given customer. The selection of equipment depends
upon which ficld you enter or change. The screen is processed from top to bottom
(i.e. Address #, Name, License #, Serial #, Unit# , C Unit #). The first field that
has been changed to a new value will be used to find the piece of equipment.
Typing more than one field will not narrow the search further.

 

Tips

When a unit is traded, sold, exchanged, or transferred, it can easily be reassigned
to a different customer. Simply display the current owner's record for the unit,
type over the customer address number, and press [Enter].

[When a customer changes their C Unit# and assigns it to a different unit, it can be
changed on the View/Update screen by replacing the current C Unit#. If the new
C Unit# is already assigned to a unit, you'll need to remove it from the first unit
before reassigning it, because the same customer cannot use a C Unit# more than
once. However, the same C Unit# can be used by different customers.

 

C1 Fill in the fields, and press [Enter] to update the information and return to the
top part of screen. If [Enter] is not pressed, the fields will not be updated. You
may change the equipment information displayed on the screen.

These updates remain in Service Management. The records in Inquire/Update
Units will not be affected. This allows you to maintain the integrity of the
washout tree and Sold Units report yet transfer equipment if it is resold to a
new customer.

 

NOTE
If you want to make changes in fields that are held in common, it will be
necessary to make the same changes in Inquire/Update Units.

 

Command Keys on the View/Update Screen

Cmd1-End

Press [Cmd1] to end the job and return to the Service Management menu. If you
entered Service Management from Point of Sale, you will return to Point of Sale.

Cmd3-Go back

Press [Cmd3] to go back to the top part of the screen and select another customer
or unit. Any changes you made on the screen without pressing [Enter] will be
ignored. You do not need to erase all fields at the top of the entrance screen. Just


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

 

change the field you're interested in, the system will use the field that was
changed for the search.

Cmd5-Service History

Press [Cmd5] to see a listing of all repair orders on a particular piece of
equipment. See page 1212.

Cmd6-Recommended Maintenance

This option displays the recommended service jobs that should be performed at
certain time or hourmeter intervals. Job codes can be added to the recommended
list, and an initial repair order with an estimate can be printed. See page 15.

Cmd7-Shipto Location Info
Press [Cmd7] to go to the Ship To Location Information screen. See page 22.

Cmd8-Next

Ifa customer owns more than | unit, press [Cind8] to see the service information
for the next unit (by Unit #). If you made changes on the previous unit, it will be
updated when you press [Cmd8].

Cmd10-Unit Service Info
Press [Cmd10] to go to the Unit Service Information screen. See page 36.

Cmd19-Delete
Press [Cmd19] to delete the unit and all of its history.

 

### Warning

Once a unit has been deleted, it can not be reinstated. You should only delete a
unit if it is in error or you are very short on disk space.

 

Fields on the View/Update Screen

The fields on the View/Update screen are described below in the order in which
they appear from left to right.

 

In defining the fields, a character is any character on your keyboard, usually
letters A-Z and numbers 0-9, but special characters such as "!" "@" "#" can be
used. Do NOT use the following characters: "" (blank) "," (comma), "*"
(asterisk), "/" (forward slash), "-" (dash or minus sign), "+" (plus sign), ">"
(greater than sign), "=" (equal sign), or "2" (question mark).

A digit is any number from 0-9. Example: 5.2 D digits means 5 digits with 2
fixed decimal places. 12345.67 is typed as 1234567.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 7

Address #

Name

License #

Serial #

Unit #

C Unit #

Series

Make

Model

Phone
Year

Warranty Code

6 characters

Set up at Service Management, Receivables
Maintenance (X11-2), or Point of Sale Entrance
(X5-1). The address # can be changed on a unit by
displaying the current owner's record at
Inquire/Update Units, typing over the customer
address number and pressing [Enter].

28 characters

Set up at Service Management, Receivables Main-
tenance, or Point of Sale Entrance. May use partial
last name to display index for selection.

7 characters

License number. Used only in Service Management.
17 characters

Serial number (or VIN). From Service Management
or the Serial Number from Inquire/Update Units
(X2-1). Must be unique. Duplicate serial numbers
can not be handled by Service Management or Fleet
Management.

6 characters

Unit number assigned by your dealership. If used,
must have been previously set up in Inquire/Update
Units (X2-1).

6 characters

Unit number used by the customer. This number
must be unique for the customer; however, the same
unit number may be used by different customers.
The C Unit# can be changed on a unit by typing
over the current number and pressing [Enter]. If a
customer is reassigning a C Unit#, it may be
necessary to remove the C Unit# from its previous
assignment first in order to avoid duplicates.

3 characters.

Set up and used in Service Management only.

9 characters

From Service Management or Inquire/Update Units
(X2-1).

9 characters

From Service Management or Inquire/Update Units
(X2-1).

3, 3, 4 digits. Area code and phone number.

2.0 digits

From Service Management or Inquire/Update Units
(X2-1).

1.0 digit


8 X10-1 * INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

 

Exp date

Description

Purchase Date

Hourmeter

Engine #

Key code

Reminder date

Job Code

AIC

A/T

Service Note

Warranty code as set up in Inquire/Update Units
(X2-1) or when sale was posted in Create Source
Documents (X1-7). These codes are user-defined.
Date (mmddyy)

Date the warranty expires.

12 characters

From Service Management or Inquire/Update Units
(X2-1).

Date (mmddyy)

From Service Management or Create Source
Documents.

6.1 digits

Number of hours equipment was used for at the
time it was purchased. In Service Management
only. Enter 1500.0 hours as 15000.

12 characters

Engine serial number.

6 characters

Ignition key number.

Date (mmddyy)

May be entered to remind customer to come in for
service on a certain date, Not used for regular
recommended maintenance, but for special
reminders. Used by Service Customer Target List
(X10.2-1).

6 characters

Used by Service Customer Target List. The service
job the customer should be reminded of.

1 character (Y/N)

Does the equipment have air conditioning? Set up
and used in Service Management only.

1 character (Y/N)

Does the equipment have automatic transmission?
Set up and used in Service Management only.

62 characters.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 9

Add Equipment and Customers

Here are a few situations that would require you to add a piece of equipment or
customer to your service files:

New customer and equipment you have never seen .
Add customer as a receivable or as a cash customer Then add equipment by
serial number.

New customer and equipment, but not in service file
Add customer as a receivable or as a cash customer. Then add equipment by
serial number or unit number.

New customer, equipment you have serviced

Add customer as a receivable or as a cash customer. Access equipment by
serial number, license number or unit number. Change address number to new
owner,

Previous customer, equipment you have never seen

Add equipment by serial number. If the equipment is for a different customer
than is displayed, [Field Exit] through the address number or type in the
address number of the customer you are adding the equipment to.

Previous customer, equipment you sold, but not in service file

Add equipment by serial number or unit number. If equipment is different
customer than displayed, [Field Exit] through the address number or type in
the address number of the customer you are adding the equipment to.

How to Add Equipment
01 To add equipment to Service Management, go back to the top portion of the

screen and type in the new serial number. Press [Enter]. The blank equipment
information fields appear. Fill in the fields and press [Enter] when complete.
This piece of equipment and its service information will now be stored within
your service files.


10 X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3
reer errr KX Eee RELEASE 6.9

How to Add a Cash Customer

O Go back to the top of the screen. To add a cash customer, press [Cmd10]. The
cash customer window will appear:

A&R SALES & RENTALS Inquire/Update Service Units XA100~101
Division: A View/Update Search Only

Address # ..

License #

Serial# .

Unit #. . Cc Unit #

Add New Cash Customer

(Example: John H./Doe)
Extended name .
Address
Extended addr
City, State . ——___________ Zip code
Phone # .. — Phone #2 ___
Fax Number . _
Tax Number . GST Method 0
Tax Code ... + — Discount Cede _ Quantity Break Pricing N

Cmd1-End Cmd3-Go back

D Fill in the fields for the new customer. Remember to put a slash before the last
name. The system uses the slash to put names in alphabetical order. You don't
need a slash for a business name, such as BEST EQUIPMENT. This is an
example of a new cash customer:

Add New Cash Customer

STEWART /HENDRICK (Example: John H./Doe)
Extended name ... C/O ACE MOTORS
Address .... 1715 LAKEWAY DR

City, State BELLINGHAM WA Zip code . +++ 982252456
360 733 2515 Phone #2 360 676 4500 Ext 4571
360 650 1000
ACE*1715 GST Method 0
1 Discount Cede Quantity Break Pricing N

Cmdl-End  Cmd3-Go back

Address# Assignment

An address number will be assigned to the customer automatically. The address
number will be the first four letters of the last name plus two numbers. Example:
The first customer named Smith will be assigned SMITOO, the next, SMITOL, etc.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT VW

Point of Sale Index
The customer's name will appear in the Point of Sale index immediately.

Edit Code

The customer created is a cash customer. The customer will be made into a charge
customer if you bring up the address number in Receivables Maintenance (XL1-
2). A C (cash) will display in the seventh position of the edit code.

Delete a Cash Customer
Cash customers can be deleted using Address Maintenance (X4-2),_


12 X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT

### Cmd5-Service History

A service history is kept for each piece of equipment under Service Management.
It tracks the date of the repair order, each service job performed, the technician
and length of time it took to finish each job. The service history is displayed but

cannot be changed here.

Show All Repair Orders

Select a piece of equipment by filling in one or more fields at the top of the
screen. Refer to the section titled "Cmd4-View/Update.”

Press [Enter] and the service history for that equipment is displayed with the most
recent service date first. If the history extends beyond one screen, press [Enter] to

 

see more.

ARR SALES & RENTALS Inquire/Update Service Units XA100-103 3
Division: L Service History

Address # .. BURKOO or Name .... RICHARD BURKIN

License # BLG483

Serial# 6901A-89034-55pP Make/Model COASTLINE 5400 Year 92

 

 

Date RO#/HrM/Service Note

11/06/92 wo08798
RCM:1048BR 5000
RCM:10480IL 5000
RCM: WINTER 5000
JOB:1048BR 5000
vv v52409
JOB:10480IL 5000
vv v26018
vv v34890

cmdl-End  Cmd4-View/Update

 

Unit # . C Unit # TRKOD

Job/Description/Ven/Part# Qty/Mech/Price/Hrs

1.50 replace bracket
+75 041 change
1.75 WINTERIZATION
1.50 replace bracket
1

110.00

-75 oi1 change
2 2.02
1 6.39

TOTAL R/O AMT

Ext. Price

110.00

4.04
6.39
129.82

Cmd6-Recommended Maintenance Cmd8-Next

 

At the end of each repair order, the dollar amount for that repair order is shown.
Press [Cmd8] to display the recommended maintenance for this customer's next

piece of equipment, if any.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 13

Fields on the Service History Screen

The fields on the Service History screen are described below in the order in which

they appear from left to right.

 

In defining the fields, a character is any character on your keyboard, usually
letters A-Z and numbers 0-9, but special characters such as "!" "@" "#" can be
used. Do NOT use the following characters: " " (blank) "," (comma), "*"
(asterisk), "/" (forward slash), "-" (dash or minus sign), "+" (plus sign), ">"
(greater than sign), "=" (equal sign), or "2" (question mark).

A digit is any number from 0-9. Example: 5.2 D digits means 5 digits with 2
fixed decimal places. 12345.67 is typed as 1234567.

Make/Model

Year

Date

R/O#/HrM/Service Note

R/O#

HrM

Service Note

Job/Description/Ven/Part#
Job

Description

Ven

Part#
Oty/Mech/Price/Hrs
Qty

9 characters

Equipment's make and model as set up in Service
Management or Inquire/Update Units (X2-1).

2.0 digits

Year unit was made. Set up in Service Management
or Inquire/Update Units.

mmddyy

The date the repair order was initially opened at
Point of Sale (X5-1).

Repair order number used to record the service at
Point of Sale.

5.1 digits

Number of hours the piece of equipment was used
for as entered in Point of Sale at the time of the
transaction. 1500.0 hours is entered as 15000.
Note from the View/Update screen, which may
originate there or from Service Note Distribution.

11 characters.

Point of Sale document number for the standard job.
Description of standard job as entered in
Inquire/Update Service Tables (X10.3-2).
3-character vendor code.

Part number.

Quantity of part.
If labor, mechanic's employee ID appears in this
field.


14 X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

 

Mech 6 characters.
Mechanic's employee ID.

Price/Hrs 7.2 digits.
Price of labor or part. If hours, 450 = 4 and 1/2
hours.

Ext. Price Extended price. Quantity of part or number of hours
multiplied by the price.

Total R/O AMT The dollar amount for the repair order.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 15

### Cmd6-Recommended Maintenance

Recommended maintenance can be displayed for a particular piece of equipment
or for a general make and model. The display shows each service job
recommended, the time or hour interval between each service, estimated price for
parts and labor, and estimated length of time required for each service job. Jobs
can be added to and deleted from the list.

Existing Equipment

OQ Select a piece of equipment by filling in one or more fields at the top of the
screen. Refer to the section titled "Cmd4-View/Update."

1 Press [Enter] and the recommended maintenance for that equipment is
displayed. If the display extends beyond one screen, press [Enter] to see more.

 

A&R SALES & RENTALS Inquire/Update Service Units XALOO-104 4
Division: L Recommended Maintenance

Address # .. BURKOO or Name .... RICHARD BURKIN
License # .. BLG483 Make COASTLINE Model 5400 Year 92
Serial? .... 6901A-89034-5S5DF Hourmeter .... Series
€ Unit # TRKO? Access COASTLINE 5400 90 92 5000
i Interval Price Time
‘D' W Group Code Description Mo Hours Labor = Hrs
5000 1048BR replace bracket 60.00 1.50
5000 104801L oil change 30.00 75
Total 90.00 2.25

Cmdl-End cmd4-View/Update | cmd5-Service History
Cmdé-Next Cma9-Add other jobs Cmd12-Print new R/O

oO
Qa
Oo
Oo

 

To delete a job from the recommended list, type D in the 'D' column. Press
[Enter]. °

To mark a job as internal or warranty, type J or W in the I/W column.

To display the recommended maintenance for this customer's next piece of
equipment (if more exist), press Cmd8-Next.

To add jobs, standard jobs (Group:Job combinations) or brand new jobs, press
Cmd9-Add other jobs (see [Cmd9]-Add other jobs), following field
descriptions.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

 

 

Fields on the Recommended Maintenance Screen

The fields on the Recommended Maintenance screen are described below in the
order in which they appear from left to right.

 

In defining the fields, a character is any character on your keyboard, usually
letters A-Z and numbers 0-9, but special characters such as "!" "@" "#" can be
used. Do NOT use the following characters: "" (blank) "," (comma), "*"
(asterisk), "/" (forward slash), "-" (dash or minus sign), "+" (plus sign), ">"
(greater than sign), "=" (equal sign), or "2" (question mark).

A digit is any number from 0-9. Example: 5.2 D digits means 5 digits with 2

 

fixed decimal places. 12345.67 is typed as 1234567.


Job
Group

Code

Description

Interval
Mo
Hours

Price Labor

Time Hrs

‘D' = Delete. Type D in this column to delete the job
from the recommended list.

{= Intemnal, W= Warranty. Tags the job as an
internal charge or a warranty transaction. When the
initial Repair Order prints, the Z or W will print
beside the job. Assists shop employees to correctly
charge for parts and service. See "Warranty and
Internal" in Point of Sale (X5-1).

Group code assigned in Inquire/Update Service
Tables (X10.3-1).

Document number of the job assigned at Point of
Sale (X5-1).

Description of the job code from the Sold To screen
at Point of Sale (X5-1).

Recommended number of months between service.
Set up in Inquire/Update Service Tables (X10.3-1).
Recommended number of hours between servicing.
4 and 1/2 hours is entered as 450.

Default labor hourly rate from Divisional Profile
(X10.3-6) multiplied by the Standard Job Flat Rate
(time) at Point of Sale (X5-1).

Standard Job Flat Rate from Point of Sale, usually
the Manufacturer's flat rate time.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 17

"Drop In" Equipment - Not on File

If it's a "drop-in" unit you have never serviced, you may not have a recommended
maintenance schedule set up for the exact make, model and year. There are
different ways equipment can be assigned to service tables:

" Specific make, model and year (or range of years). Example: Ford 7610 '83- .
‘87.

- Make and model are given with no year. Example: New Holland 680 (leave
year blank to indicate all years of model number 680).

- Make and year (or range of years) with no model. Example: Ford '64-'68
(leave mode! blank to indicate all models of Ford equipment from 1964
through 1968). ,

"Make is specified with no model or years. Example: New Holland (model and
year are blank to indicate all models and years of New Holland equipment).

When you want to display the recommended maintenance for a particular piece of
equipment, the program does the following to determine which service table to
use:

1) First, it tries to find the actual make, model and year of the equipment. If that
fails,

2) It tries to find the make and model (with a blank year). If that fails,

3) It tries to find the make and year (with a blank model). If that fails,

4) It tries to find the make (with blank model and year). If that fails,

5) It will use the default service table (refer to Set up Default Table). If no
default table is found,

6) Anerror message is displayed.

 

NOTE
Setting up service tables and assigning equipment to them is discussed in more
detail in CHAPTERS X10.3-1, INQUIRE/UPDATE SERVICE TABLES, and
X10.3-2, INQUIRE/UPDATE MAKE MODEL ASSIGNMENTS.


18 X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

Cmd9-Add other jobs

To add other jobs to the recommended maintenance, press [Cmd9]. The "Add
Recommended Maintenance" screen will then appear on the lower half of the
display.

A&R SALES & RENTALS Inquire/Update Service Units XA100-104 4
Division: L Recommended Maintenance

Address # .. BURKOO or Name .... RICHARD BURKIN
License # BLG483 Make COASTLINE Model 5400 Year 92
Serial# 6901A-89034-S5DF Hourmeter .... Series
Unit # . “ @ Unit # TRKO9 Access COASTLINE 5400 90 92 5000
i Interval Price Time
‘D' W Group Code Description Mo Hours Labor = Hrs
5000 1048BR replace bracket 60.00 1.50

 

Add Recommended Maintenance 8
Job

I/W Group Code Description
5000 WINTER WINTERIZATION

Cmdi-End Cmd3-Go back cCmd9-Accept jobs and return

 

 

 

NOTE
Jobs appear on the POS detail screen in the same order as on the Recommended
Maintenance screen. Since all established standard jobs can be expanded at Point
of Sale, they should be listed first. New jobs, which apply only to the new R/O
and cannot be expanded, should be placed last.

6nd 2-Print new R/O —_
From Inquire/Update Service Units, you can establish a repair order that includes
the recommended maintenance or work to be done. Parts and labor are added as
note lines, as is the estimated total. You may want to print the repair order for the
customer to sign before s/he leaves.

O To print a copy of the invoice showing the recommended maintenance and
additional jobs requested, press [Cmd12]. You will see the print options.

The printer information provided at Point of Sale will default. When you select

the options the first time, they will remain until you change them or end the job
[Cmd1].


X10-1 » INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 19

 

A&R SALES & RENTALS Inguire/Update Service Units A100-107 7
Division: L Option Screen
Enter document type to use
Enter sold by address number
Enter sales code of the note line to use
Enter printer ID for printing invoices
Enter the number of invoice heading lines to print (0-12) . .
For the Okidata printer, use 8.
For the IBM 5256 printer, use 9.

For the IBM 4214 printer, use 12.
For the IBM PRO printer, use 12.

Enter the number of spaces left of normal to print (0,5)
For the IBM 5256 and 4214 printer, use 0.
For the IBM PRO printer, use 5.
For the Okidata printer, use 5.

cmdl-End  Cmd3-Go back

 

O Furnish the document type, employee address number, and the sales code of
the note line that will precede the recommended maintenance jobs (header
line).

O1 Press [Enter]. You'll return to the Recommended Maintenance screen.

C1 Press [Cmd1] to end the Inquire/Update Service Units job. If you reached
Recommended Maintenance by pressing [Cmd18] from Point of Sale, you'll
return to Point of Sale; otherwise, you'll return to the Service Management
Menu.

Definitions of Print Options

Enter document type to use ...............25 w
The document code must have a Type of 'W' for Repair Order as set up in
Document Classification Maintenance (X52-2).

Enter sold by address number ............. ++. JIM
Type a valid employee address number on this line.

Enter sales code of the note line to use .......... AA
Use a sales code with line type "N.”

 

### Suggestion

Set up a sales code of type "N" (Note) especially for this purpose. Use its 15-
character description to signal that the lines that follow are suggestions and
estimates, such as: "WORK TO BE DONE" or "RECOMMENDED WORK."


20 X10-1 » INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3
em ANAEEMENT RELEASE 2.3

Enter printer ID for printing invoices ........... P2
Use the ID of the printer with R/O forms, usually your store printer set up in
Security Maintenance (X6-6).

C1 Fill out the other lines according to the type of printer you are using.
O1 After you press [Enter], an open document will be printed.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 21

Sample Repair Order

An example of a repair order created and printed using this option is illustrated
below.

A&R SALES & RENTALS
288 West Kellogg Road
Bellingham, WA 206 733-7610
SALES --- SERVICE --- RENTALS
"We sell just about everything”
This month's special- 15% off manufacturers AM/IM radios

Return Policy: Parts returned after 5 days are subject to a 10%
restocking fee.

BURKOO RICHARD BURKIN
1101 MONTPELIER DR
GREENSBORO, NC 27410
FORD 2000 90 S/N: C642972 HRS: -0 WAR: 4

Sold By: AUSTIN PO #: Date 1/14/93 REPAIR ORDER RO00119

Ship By: Tax d: --Open-~

TD Qty Description Amount
RCM:1048BR 5000 = 40.00 REPLACE BRACKET
RCM:10480IL 5000 1.00 OIL CHANGE

Cash Sale
Phone: (919)492-5050

 

For information about completing work orders created by this process, see


22 X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

### Cmd7-Ship To Location Info

On the Ship To Location Information screen, which has no security gate, users
can view and update customer address, ship-to information, hours open and
closed, map location (by ship-to), metro (by ship-to), contacts (as many as
needed) and contact titles, phone number (as many as needed), fax # (as many as
needed), BKD PO#, date of BKD PO#, SM PO#, and the date of SM PO#. Both
SM (y/n) and CFPM (y/n) are view only fields: the values in these 2 fields are
updated automatically by the system when the Unit Information Screen is
updated. Users can enter an unlimited number of notes (60-characters each) for
each customer. The system records their ID, date, and time of the note. Only the
three most current notes are displayed.

A function key provides access to each customer's purchase orders: type,
beginning and ending dates, and amount. Totals (charges and credits) of all posted
work orders that reference corresponding purchase order numbers on the P.O.S.
Sold To screen are displayed. Individual purchase orders can be purged (deleted
from the system), and a function key allows the user to purge all P/Os with zero
balances at one time.

O From the SMS Inquire/Update screen, press Cmd7-Ship To Location Info to
reach the Cust. Service Info Details screen. The same screen is available from
the Entrance, Sold To, and detail screens at Point of Sale Invoicing (sec
displayed first in Inquiry mode, as illustrated below.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 23

 

Select Ship To Screen

 

A&R SALES & RENTALS Select Ship To VSYXSRR

Sold To COLEMAN FORKLIFT CORP. Mode 2000 Make AMAZON
2300 IOWA ST. Serial# Fo002
BELLINGHAM WA 98226 © Unit#

1sSelect
Opt Ship To Name City, State
MINHARO WHOLESALE BURLINGTON WA

MINHARO WHOLESALE ANACORTES WA
MINHARO WHOLESALE SEDRO WOOLEY WA

F3=Exit F12=Previous

 

0 Select the appropriate “Ship To” location, and press [Enter] to proceed to the
next screen, which will be the Ship to Location Info screen, as illustrated
below.

AGR SALES & RENTALS Ship to Location Info VSYODFR

Sold To COLEO1 Ship To MINHO1
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233
JESSE EINE SSSI ISOC OU UO IOUS IEG GTO IGOR EERO SERRA EEE
HRS:..Open: 8:00 Close: 17:30 Map Location 28 Metro A
Contact: #1 RAE BARNES #2
Phone #: #1 360 650 - 5489 42
Fax #: #1 360 738 - 7885 #2
SM: ¥ CFPM: ¥
BRD P/O #: 10200 Amount : 500.00
Ending Date: 12/31/97 Remaining Balance: 122.94
SM P/O #: PO 100800 Amount: 3000.00
Ending Date: 7/31/97 Remaining Balance: 3000.00

Note: Renews annually - contact in June

F2=Units F3sExit Fé=Edit F9=Note Fi0=Contacts Fll=P/0's F12=Previous

 

Note that the information on this screen does not pertain to an individual unit: it is
for the “Ship To” address although some information is updated from the Unit
Service Info screen, such as SM (Scheduled Maintenance) and CFPM (Contract
for Preventive Maintenance), which indicates that one or more units at this
location are under a service agreement. The purchase order remaining balances
are updated by Point of Sale. The information on the first line under the addresses,


24 X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

opening & closing hours, map location, and metro, pertain to the “Ship To”
location and are entered via F6=Edit.

Look at the command keys at the bottom of the screen to get an idea of what you
can do here. The most important one is F11-P/O’s.

O To work with Unit Service Information, press F2=Units. See F2=Units, page
50.

Oi To change the Customer Service Information screen, press F6=Edit. See
F6=Edit, page 50.

O To maintain notes about the customer, press F9=Note. See F9=Notes, page 50.

G To maintain contacts for the customer, press F10=Contacts. See
F10=Contacts, page 50.

1 To maintain purchase orders for the customer, press F11=P/O's. Sce
F11=Purchase Orders, page 50.

O To go back one screen, press F12=Cancel.

O To end the job and exit to the Service Management Menu, press F3=Exit.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 25

F2=Units

O To work with Unit Service Information, press F2=Units. The Unit Search
Screen appears with a list of units assigned to the Ship To address.

 

 
   
 
  
 
    
  

A&R SALES & RENTALS Unit Search VSMBDFR
Sold To COLE Ship To
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE
2300 Iowa st.
BELLINGHAM WA 98226 BURLINGTON WA
Model Make Serial #

i=Select C=Cost N=Notes P=Parts

Opt Model Make Serial # Cc Unit # Options
— 2000 AMAZON FOOOL 7
— 2000 AMAZON FOO06

F3SExit

  

F12=Previous

 

O Use any combination of the position prompts or scroll by pressing [PgDn] to
locate the unit you want.

O To see costs associated with a unit, type C beside it in the column labeled
"Opt," and press [Enter].

O To record notes about a unit, type N beside it and press [Enter].

O To see parts that have been installed on a unit, type P.

O To display a unit, type 5.

See UNIT SERVICE INFORMATION, page 36.


26 X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

F6=Edit

To change the ship to location information, press F6=Edit. TheShip To Location

Info screen is displayed:

AER SALES & RENTALS Ship to Location Info VSYODFR

Sold to COLEO1 Ship To
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE
2300 IOWA sT.
BELLINGHAM WA

whe neadewnrnenenenient Edit Ship To Location

HRS:..Open: 8:00 Clo| Name... - - MINHARO WHOLESALE

Contact: #1 Extended Name

Phone #: #1 - Address we

Fax #: #1 - Extended Address

SM: ¥ CFPM: N City/State . . BURLINGTON WA

BKD P/O #: 87-09325 Zip Code... 98233 Open 800

Ending Date: 12/31/00 Salesman... Close 1730

SM P/O #: 130-9045 Tax Code... TA Map Loc AB13

Ending Date: 12/31/00 Discount Code Metro Y

Note: F12=Previous

F2=-Units F3=Exit F6=Edit F9=Note Fid=Contacts F11=P/O0's F12=Previous (

 

© For "Open Time" and "Closing Time" use 24-hour military time. For example,
for 5:30 P.M., type: 1730 and press [Field Exit].
CQ To return to the Info screen, press F12=Previous.

co


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 27

F9=Notes

O To maintain notes about the customer, press F9=Note on the Edit Ship To
Location Info screen. The Edit Customer Notes screen is displayed in
CHANGE mode if there are current notes; otherwise, it is displayed in ADD
mode.

CHANGE Mode

A&R SALES & RENTALS Inquire/Update Service Units VSYSEFR
Edit Ship To Notes
Sold To COLEO1 Ship To
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE
2300 IOWA ST.
BELLINGHAM WA 98226 BURLINGTON WA
Note Date

4=Delete

Opt Note Date Note

11/20/00 The 3 most recent notes are displayed at Inquiry.
21/20/00 To see other notes, press F9=Note.
11/20/00 There is no limit to the number of note lines.

F3=Exit F6sAdd F12=Previous

 

O1 Use the position prompt or scroll by pressing [PgDn] to locate the note you
want.

O To change a note line, simply type over the existing line. The system records
the most recent User ID in the column labeled "Changed by"; however, the
date is not changed.

0 To delete 1 or more note lines, type 4 in the column labeled "Opt" and press
[Enter].

O Toggle to ADD mode by pressing F6=Add. A screen of blank note lines is
displayed.


28 X10-1 » INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3
S$ ec e—e—c—C egwswnw_c eee ELAS 2.9

ADD Mode

AGR SALES & RENTALS Inquire/Update Service Units VSLSEFR
Edit Customer Notes

Sold To  PARKOL Ship To PARKO1
AUSTIN PARKER AUSTIN PARKER
3149 ELLIS 3149 ELLIS
BELLINGHAM WA 98225 BELLINGHAM WA 98225

 

 

 

 

 

 

 

 

 

F3=Exit F6=Change F12=Previous

 

O Type as many note lines as you need and press [Enter] to record them.
O Toggle to CHANGE mode by pressing F6=Change.

O To go back to the detail screen, press F12=Previous.

O To end the job and return to the menu, press F3=Exit.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 29

F10=Contacts

A contact is simply a record of one or more persons who can be contacted in
regard to contracts, maintenance, and units. Each customer can be associated with
as many contacts as needed. Only the first 2 contacts are displayed on the Ship To
Location Info screen.

O To maintain contacts, press F10=Contacts. The Edit Contacts screen displays a

list of current contacts; if any.

AGR SALES & RENTALS Inquire/Update Service Units VSLTDFR
Edit Contacts

Sold To COSTOL Ship To costTo2z

COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry st
BELLINGHAM WA 98225 Sumas, WA 98341

4=Delete
First Name Last Name
Meredith, Curry
Phone 206 733 - 0243 Ext 4571 Fax 206 733 ~ 5106

Steve. Garrett_____ —__
Phone 206 734 - 2514 Ext 1134 Fax 206 671 - 9706

F3-Exit F6=Add F12=Previous

 

O) To change information on this screen, type over the existing data and press
[Enter].

O To delete a contact, type 4 beside the name in the column labeled "Opt" and
press [Enter]. The contact is deleted without confirmation.

O To add new contacts, press F6=Add. A blank list for contact information is
displayed, as illustrated below.


30 X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

 

ABR SALES

Sold To

First

& RENTALS Inquire/Update Service Units VSOSEFR

cosTo1

COST CUTTER FOODS
4111 GUIDE MERIDIAN
BELLINGHAM WA 98225

Name

Phone

Phone

Phone

Phone

Phone ___

F3sExit

Edit Contacts

Ship To cosTo2
Cost Cutter Limited-sumas
944 Cherry st
Sumas, WA 96341

F6=Change F12=Previous

 

O Add as many contacts as necessary. Press [Enter] to add the names or press
[PgDn] for another blank list.
O To toggle to CHANGE mode, press F6=Change.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 3t

F11=Purchase Orders

The first 2 types of purchase orders are displayed on the Purchase Orders screen;
however, there is no limit to the number of purchase order numbers that can be
stored. Purchase order numbers must be unique.

0] To maintain purchase orders for the customer, press F11=P/O's on the Edit
Customer Info Details screen. The list of current P/O’s, if any, is displayed.

A&R SALES & RENTALS Inquire/Update Service Units VSLXDFR
Purchase Orders

Sold To COSTOL Ship To CosTo2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341
Type End Date Number

2-Edit P/O 4=Delete 5=Invoices

Opt Type End Date Number
- 12/31/94 118145

Purchase Order balances reflect tax and discounts. They may differ from
amounts seen in F16=Costs, which are before tax and discounts.

Only P/O's with zero balances can be deleted.

 

F3-Exit F6=Add F12=Previous F13=Purge Records

 

O To change a purchase order, type 2 beside it in the column labeled "Opt" and
press [Enter]. See Add Purchase Orders, page 50. (same screen).

O To delete a particular purchase order, type 4 beside it in the column labeled
"Opt" and press [Enter]. A confirmation message is displayed. Only P/O's
with zero balances can be deleted.

O To review invoices (or work orders) associated with a purchase order, type 5
beside it in the column labeled "Opt" (Purchase Orders screen) and press
[Enter]. See Invoices, page 50.

O To add purchase orders, press F6=Add. See Add Purchase Orders, page 50.

U To remove zero balance P/O's from the system, press F13=Purge Records. See
F13=Purge Records, page 50.


32 X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

Invoices

O To review invoices (or work orders) associated with a purchase order, start at
the Purchase Orders screen. Type 5 beside the purchase order in the column
labeled "Opt," and press [Enter]. A list of invoices, if any, is displayed.

ARR SALES & RENTALS Inquire/Update Service Units VSLODFR

Invoices
Sold To

cosTo1 Ship To cosT0o2

COST CUTTER FOODS
4111 GUIDE MERIDIAN
BELLINGHAM WA 98225

Cost Cutter Limited-sumas
944 Cherry St
Sumas, WA 98341

Purchase Order Type
235-2409 SM
Invoice Invoice

Number Date

Date
12/31/94

Amount Balance
3000.00 2857.64

Invoice
Number
sM09026

Invoice
Amount
142.36

Invoice
Date
9/23/94

F3sExit F12=Previous


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 33

Add Purchase Orders

O To add purchase orders, press F6=Add. The Add Purchase Order screen
appears.

A&R SALES & RENTALS

Inquire/Update Service Units
Add Purchase Order

Sold To COSTO1L Ship To cosTo2
COST CUTTER FOODS Cost Cutter Limited-sumas
4311 GUIDE MERIDIAN 944 Cherry st
BELLINGHAM WA 98225 Sumas, WA 98341

P/O Number . .

P/O Type...

P/O End Date .

P/O Amount . .

F3=Exit

 

Fl2=Previous

1 Type the requested information. This is an AS/400 screen: don't forget to type
the decimal in the P.O. Amount field.


34 X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

Fi3=Purge Records

O To remove zero balance P/O's from the system, press F13=Purge Records.

A&R SALES & RENTALS Inquire/Update Service Units
Purchase Orders

Sold To  CosTo1 Ship To costo2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry st
BELLINGHAM WA 98225 Sumas, WA 98341
Type End Date Number

Purge P/O Invoices

Purge all Invoices for zero Pe Balance
balance Purchase Orders _ + 00.00 1000.00
: 00.00 2500.00

F3sExit F12=Previous

FP3=Exit F6=Add Fi2=Previous F13=Purge Records

 

1 To confirm your request to remove the P/O's, type y (Yes) and press [Enter].
Oi To cancel your request,press F12=Previous.

Ship To Location info Screen: Field Definitions

BKD
P/O# Purchase Order Number
Ending Date Date (mmddyy). End of purchase order
authorization period,

Amount Dollar amount of purchase order.

Remaining Balance Amount of original P/O minus cost of repairs to
date. Purchase Order balances reflect tax and
discounts. They may differ from amounts seen in
F16=Costs, which are before tax and discounts.

CFPM Y/N. Extended maintenance contract. Will be "Y" if
there are any units on service maintenance.

Changed by User ID of the person who entered a note line for a
customer or unit.

Closing Time See HRS.

Contact 6 characters. Person's name and phone number at
the Ship To address.

HRS

Open Time Time (bhmm). Use 24-hour military time.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 35

 

Closing Time

Map Location
Metro
Note

Note Date

Open Time
Option
SM

SM
P/IO#
Ending Date
Amount
Remaining Balance

Time (hhmm). Use 24-hour military time. For
example, type 6:30 P.M. as 1830.

6 digits.

Y/N. Within Metro area (Yes/No).

60-character line. Unlimited. Maintained for
customers and units. The 3 most recent note lines
are displayed for customers and the 3 oldest lines
are displayed for units.

Date (mmddyy). Date on which a note for a
customer or unit was entered. This date does not
change when the note is changed. Based on this
date’, the 3 most recent note lines are displayed for
customers and the 3 oldest lines are displayed for
units.

See HRS.

Y/N. Scheduled Maintenance. Will be "Y" if there
are any units on service maintenance.

Purchase Order number

Date (mmddyy)

Dollar amount of original P/O

Amount of original P/O minus cost of repairs to
date. P/O balances reflect tax and discounts.


36 X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

### Cmd8-Unit Index

On the entrance screen for Inquire/Update Service Units:

1 Type a customer address number.
DO Press Cmd8-Unit Index. A list of units belonging to the customer is displayed:

A&R SALES & RENTALS Inguire/Update Service Units XA100-101
Division: A View/Update Search Only

Address # COLEO1 or
License # . .

Serial# .

Unit # ....

unit Search

1=Select

Opt Serial # Make

— F001 AMAZON
F002 AMAZON
F003 AMAZON
FO04 AMAZON
FOOS AMAZON:

F3=Exit F12=Previous

 

O) To select a unit for service, type 1 beside it in the column labeled "Opt," and
press [Enter]. The View/Update screen displays information about the unit:


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 37

### Cmd10-Unit Service Information

O From the SMS Inquire/Update screen, press Cmd10-Unit Service Info to reach
the Unit Service Info screen. The same screen is available from the Sold To
screen at Point of Sale Invoicing (see CHAPTER X5-1, POINT OF SALE).
After a unit serial number is entered, the Unit Service Info screen is displayed
in Inquiry mode, as illustrated below. [fa serial number is not entered, the
Unit Service Information screen is displayed instead.

 

A&R SALES & RENTALS Display Unit Service Info VSO1DFR

Sold To  COLEOL Ship To

COLEMAN FORKLIFT CORP. MINHARO WHOLESALE

2300 IOWA ST.

BELLINGHAM WA 98226 BURLINGTON WA 98233
Make Model Yr Serial # Hourmeter Div Group Option
AMAZON 2000 97 F001 Oo A 0 7

Inst Date 90 Day 1 Year 3 Years 5 Years CFPM End
8/24/00 11/24/00 8/24/02 8/24/03 8/24/04

SM Begin . : 8/24/97 SM End . 8/24/03

SM Type. . 2: bsm SM Freq 60

SM Rate. 2: 55.00 Cons Rate 5.00 Labor Hours:
SM Due . .: 8/01/99 SM Prev . : Contract Number

F3sExit Fé=Edit F9=Note Fl2=Previous FiS=Parts F26=Costs

  

O To change or add service information, press F6=Edit. See F6=Edit, page 38.

O To add notes, press F9=Note. See F9=Notes, page 3939. To review parts that
have been installed on this unit, press F15=Parts. See F15=Parts, page 41.

C1 To review costs associated with this unit, press F16=Costs. See F/6=Costs,
page 44.

O To go back to the Inquire/Update Units screen, press F12=Previous.

O To go back to the Service Management Menu, press F3=Exit.


38 X10-1 » INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

F6=Edit c

O To change or add service information, press F6=Edit. The Unit Service Info
screen appears in edit mode.

A&R SALES & RENTALS Inquire/Update Service Units

Sold To  COLEO1 Ship To

COLEMAN FORKLIFT CORP. MINHARO WHOLESALE

2300 IOWA ST.

BELLINGHAM WA 96226 BURLINGTON WA 98233
Make Model Yr serial # Hourmeter Div Group Option
AMAZON 2000 97 FOOOL Oo oA 7

      
 

Inst Date 90 Day 1 Year 3 Years 5 Years CFPM End
8/24/00 11/24/00 8/24/01 8/24/03 8/24/04 F4=Prompt

SM Begin . . 8/24/97 SMEnd. .. 8/24/03 SM... . to select
SM Type...  bsm SM Freq . . 60 SM Due Type from a list.
SM Rate . . 55.00 Cons Rate . 5.00 Labor Hours

SM Due. . 8/01/99 SM Prev. . Contract Number

SM Due Hr . SM Prev Hr .

Note :

F3=Exit F4=Prompt F9=Note F12=Previous Fl15=Parts ¥F16=Cests

O To start a Scheduled Maintenance contract, enter a date in the field labeled (
"SM Begin." See Fields and Definitions, page 47.
O When you are done, press [Enter] to record the changes.


X10-1 » INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 39

F9=Notes

The 3 most recent note lines are displayed on the Edit Unit Service Info screen;
however, there is no limit to the number of note lines that can be stored. When
multipie lines are entered on the same day, they are maintained in the order in
which they were entered.

Oj To add or change notes about a unit, press F9“Note from the Edit Unit Service
Information screen. The Edit Unit Notes screen is displayed in CHANGE
mode if there are existing notes; otherwise, blank note lines are displayed in
ADD mode.

CHANGE Mode

A&R SALES & RENTALS Inquire/Update Service Units CHANGE VSL6EFR
Edit Unit Notes

Sold To COLEOi Ship To

COLEMAN FORKLIFT CORP. MINHARO WHOLESALE
2300 IOWA ST.
BELLINGHAM WA 98226 BURLINGTON WA 98233
Serial # Fake Model ID
FOOOL AMAZON: 2000

Note Date

99999999

4=Delete

Note Date Note

11/20/00 The most recent note lines are displayed first.
11/20/00 Press F9=Note to see more notes or add notes.
11/20/00 There is no limit to the number of note lines.
11/20/00 Tupe as many as you want.

11/20/00 Line 5

11/20/00 Line 6

F3-Exit F6=Add F12=Previous

 

O Use the position prompt or scroll by pressing [PgDn] to locate the note you
want.

O To delete a note line, type 4 beside it in the column labeled "Opt" and press
[Enter].

O To change a note, simply type over the current line. The system records the
most recent User ID in the column labeled "Changed by;" however, the date is
not changed,

D Toggle to ADD mode by pressing F6=Add. A screen of blank notes is
displayed.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

ADD Mode

 

A&R SALES & RENTALS Inquire/Update Service Units VSLG6EFR
Edit Unit Notes

Sold To COLEO1 Ship To MINHO1
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233
Serial # Make Model ID
FOOL AMAZON. —- 2000

Note
Dealer prep 3/19/97 OK-Luke.

F3=Exit F6=Change Fi2=Previous

C1 Type as many note lines as you need and press [Enter] to record them.
O Toggle to CHANGE mode by pressing F6=Change.

O To go back to the detail screen, press F12=Previous.

O To end the job and return to the menu, press F3=Exit.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 41

F15=Parts

 

NOTE
To purge parts history from the following series of screens, use Purge Repair
Parts History (X10.3-14).

 

 

To review the parts that have been installed on the unit, press F15=Parts. A list of
parts that have been installed for this customer are displayed. The parts are
displayed in order first by part number, then by labor date (most recent first).

A&R SALES & RENTALS Inquire/Update Service Units VSLODER
Customer's Unit Repair History

Sold To COSTO1 Ship To cosTo2
COST CUTTER FOODS Cost Cutter Limited-sumas
4111 GUIDE MERIDIAN 944 Cherry st
BELLINGHAM WA 98225 Sumas, WA 98341

Make Model Serial # Hourmeter
RAYMOND 2000 1G8ZH1576R2Z211704 3011.0
Part Number

Part Vendor Hour Labor Invoice
Number Meter Date W/O Number
1150-065 RAY 254. 3/21/94 smMog024
1150-065 RAY 21. 3/15/94 sM09022
154-010-210 RAY 1501. 9/23/94 SM09026
590-096 RAY 1007. 6/30/94 $m09025
632-043-001 RAY 2467.0 12/21/94 $M09027
632-043-001 RAY 1007. 6/30/94 sM09025
632-043-001 RAY 21. 3/15/94 smo9022

F2=Unit History F3=Exit F12=Previous F21=Print

 

O Use the position prompt or scroll by pressing [PgDn] to locate the part you are
interested in.

O To print a list of parts that have been installed since this customer purchased
the unit, press F21=Print. See F21=Print Unit Repair History, page 42.

O To review all parts that have been installed on this unit (for all owners), press
F2=History. See F2=History, page 43.


42 Xi0-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

F21=Print Unit Repair History

O To print a list of parts that have been installed since this customer purchased
the unit, press F21=Print on the Customer's Unit Repair History screen.

O1 To print a list of all parts that have been installed on this unit (for all owners),
press F21=Print on the Unit Repair History screen.

In either case, a prompt for Printer ID is displayed.

 

Inquire/Update Service Units VSL9DFR
Customer's Unit Repair History

Sold To COSTO1 Ship To cosTo2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341

Model Serial # Hourmeter
2000 1GB2ZH1576R2231.704 3011.0

Par Enter Printer Id + nvoice
Num : : /O Number
115: Printer Id OU > M09024
15: x M9022
154: F3sExit F12=Previous + MO9026
590 : + M09025
632 : : M09027
632 : : MO9025
632-043-001 21.0 3/15/94 smM09022

F2:Unit History F3=Exit Fl2=Previous ¥F21=Print

 

O Enter a printer ID, or leave the prompt blank and the report will be printed on
the default printer for your User ID.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 43

F2=History

D To review all parts that have been installed for all owners, press F2=History.

 

A&R SALES & RENTALS Inquire/Update Service Units VSNODER
Unit Repair History .

Make Mode? Serial 4 Hourmeter
RAYMOND 2000 1G82H1576RZ211704 3011.0
Part Number
Part Part Vendor Hour Labor Invoice
Qty Number Meter Date W/O Number
1 1150-065 RAY 254.0 3/21/94 sM09024
1 1150-065 RAY 21.0 3/15/94 smo9022
2 154-010-210 RAY 1501.0 9/23/94 sm09026
1 590-096 RAY 1007.0 6/30/94 sM09025
1 632-043-001 RAY 2467.0 12/21/94 S$H09027 .
1 632-043-001 RAY 1007.0 6/30/94 sM09025 :
1 632-043-001 RAY 21.0 3/15/94 sM09022 :

F3=Exit Fl2=Previous F21=Print F3=Exit Fl2=Previous F21=Print

 

O To print this list, press F21=Print. See previous page.


X10-1 e INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

 

F16=Costs

 

 

   
  
    

NOTES

Unit cost amounts are before taxes and discounts; therefore, purchase order
balances, which reflect taxes and discounts may be different.

To purge cost history from the following series of screens, use Purge Unit Repair
Cost History (X10,3-15).

O To review costs associated with a unit, press F16=Costs on the Unit Service
Information screen. The Select Sales Code window is displayed.

 

its
Select Sales Codes

Sales Sales Code NHOL
Code Description NHARO WHOLESALE BURLINGTON

RLINGTON WA 98233
1=Select Meter Div Group Option
0.0 A 2 OVER
Opt Sales Sales Code
Code Description 5 Years CFPM End
+e 12/31/97
AA RCVD ON ACCOUNT
cD CUST DEPOSITS
DU UNIT TRADE H Hourmeter
ES EQUIPMENT SALE Labor Hours 1.5
Er
JG JOHN'S SALES

F2=All F3=Exit F12=Previous ed.
otes.
lines -
=Parts F16=Costs

 

Select Sales Code Window

1 To review costs associated with all sales codes, press F2=All.

O To select 1 or more sales codes, type 1 beside them in the column labeled
"Opt" as illustrated above, and press [Enter]. The costs associated with the
selected sales codes are displayed.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 45

Unit Repair Cost for Customer

 

A&R SALES & RENTALS Inquire/Update Service Units VSMRDFR
Unit Repair Cost for Customer
Sold To cosTo1 Ship To cosT02
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry st
BELLINGHAM WA 98225 Sumas, WA 98341
Make Model Serial # Hourmeter
RAYMOND 2000 1G8ZH1576R2Z211704 -0
Inst Date 90 Day 1 Year 3 Years 5 Years
3/21/94 6/21/94 3/21/95
Code Month Year Life
Total 106.68 685.16 685.16
Sales Code Current Year to Life
Month Date to Date
PS - PARTS SHOP 67.73 158.83 158.83
TC - LABOR CUSTOMER 38.95 136.33 136.33
TD - LABOR CUST MISC 00 390.00 390.00

F2=Unit History F3=Exit F12=Previous F21=Print

 

O To print the costs incurred by the current owner, press F21=Print.'A prompt for
Printer ID is displayed.


46 X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

F21=Print Unit Repair Cost

 

A&R SALES & RENTALS Inquire/Update Service units
Unit Repair Cost for Customer

Sold To COSTO1 Ship To COsTO2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341
Make Model Serial # Hourmeter
RAYMOND 2000 1G82ZH1576R2211704 0
Inst Date 90 Day 1 Year 3 Years 5 Years
3/21/94 6/21/94 3/21/95
Month fear Life
685.16 685.16
Enter Printer Id Life
to Date
Printer Id : 8. 158.83
: 136.33
F3=Exit F12=Previous : 0. 390.00

 

nit History F3=Exit Fi2=Previous ¥F21=Print

 

O Enter a printer ID, or leave the prompt blank and the report will be printed on
the default printer for your User ID.

Unit Repair Cost History

A&R SALES & RENTALS Inguire/Update Service Units VSNSDFR
Unit Repair Cost History

 

   

Model Serial # Hourmeter
2000 1G8ZH1576RZ211704 .
Inst Date 90 Day 1 Year 3 Years 5 Years
3/21/94 6/21/94 3/21/95
Code Month Year Life
— Total 106.68 685.16 685.16

Sales Code Current Year to Life
Month Date to Date

PS - PARTS SHOP 67.73 158.83 158.83
TC - LABOR CUSTOMER 38.95 136.33 136.33
TD - LABOR CUST MISC .00 390.00 390.00

F3=Exit F12=Previous F21=Print

C To print the unit's repair cost history for all owners, press F21=Print. See
previous page.


X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 47

Unit Service Info Screen: Field Definitions

Changed by
CFPM
CFPM End
Cons Rate

Contract Number

Division
Group

Group Number

Hourmeter

Inst Date

Invoice W/O Number

6 characters. User ID of person who entered or
changed note line.

Y/N. Extended maintenance contract.

Date (mmddyy). Date CFPM contract ends.

2.2 digits. Consumables rate. Dollar amount
allotted.

9 digits. Contract for the unit. Press F4=Prompt to
select from a list of contracts. A unit can be
associated with only one contract; however, more
than one unit can be associated with the same
contract.

Division code associated with the unit.

2 digits (01-99). Service truck's group code, which
is assigned in Van Inventory System.

Group number that the service truck is assigned to.
See Group.

5.1 digits. The hourmeter field is updated by Create
Point of Sale Posting Batch (X55-1) if SM=Y on
the Sold To screen at Point of Sale (X5-1) and SM
Due Type=H.

Dates (mmddyy)

90 Day

1 Year

3 Years

35 Years

(F2=Unit History). It is displayed on the Customer's Unit Repair History
(F15=Parts from Display Unit Service screen) and on the Unit Repair History

(F2=Unit History).
Labor Date

Labor Hours

Note Date

Note

Option

Date (mmddyy). Work date from the Sold To screen
at Point of Sale Invoicing (X5-1).

3.1 digits. Number of hours for maintenance. Unit
Service Information screen.

Date (mmddyy). Unit Service Information screen.
Date a note line was originally entered. Does not
change when the note is updated.

60 characters. Unlimited. The oldest 3 note lines are
displayed.

8 characters. Optional. User-defined option code.
Options are set up in Unit Service Options Table
(X10.3-7). Press F4=Prompt for a list of valid
options.


48 X10-1 « INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

 

SM Begin

SM Due

SM Due Hr.

SM Due Type

Type the
number here

Date (mmddyy). First day of Scheduled
Maintenance contract. Entering this date on the Edit
Unit Service Information screen makes the system
aware that the unit is under contract.

Date (mmddyy). Date of next scheduled
maintenance. The system calculates the next
Scheduled Maintenance due date by adding
"Frequency" to the "Work Date" from the most
recent work order. Updated by Create Point of Sale
Posting Batch (X55-1) if SM=Y on the Sold To
screen at Point of Sale (X5-1) and SM Due
Type=D.

6.1 digits. Hourmeter reading when next service is
due. Updated by Create Point of Sale Posting Batch
(55-1) if SM=Y on the Sold To screen at Point of
Sale (X5-1) and SM Due Type=H. Accepts 1
decimal place or enter 750 hours as 750 and press
[Field Exit]. Screen will display 750.0.

1 character. Indicates how service is scheduled.
H=Hourmeter. Requires hours in SM Due Hr. field.
D=Date. Requires date in SM Due field.

The display depends on the type of workstation you
use. Ifyou work at a “green screen” or dumb
terminal, you will see the following selection:

2 1. Hourmeter

2. Date
3.

 

Type the number of the option you want in the
column to the left of Hourmeter, as illustrated.

Ifyou work at a PC, you will get the following
selection:

Highlight the
one you want

& press the
space bar

Use your mouse to click on the selection, or
move the highlighted bar with an arrow key, and
press the space bar to make your selection.


X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT 49

SM End

SM Frequency

SM Prev

SM Prev Hr

SM Rate

SM Type

Date (mmddyy). Date scheduled maintenance
contract ends.

3.0 digits. Number of days between scheduled
maintenance dates, typically 30, 60, 90. The system
calculates the next date for scheduled maintenance
(SM Due) by adding the frequency to work date
from the most recent work order (SM Prev).

Date (mmddyy). Work date from the most recent
(previous) work order. Updated by Create Point of
Sale Posting Batch (X55-1) if SM=Y on the Sold
To screen at Point of Sale (X5-1) and SM Due
Type=D.

6.1 digits. Hourmeter reading at previous service.
Updated by Create Point of Sale Posting Batch
(X55-1) if SM=Y on the Sold To screen at Point of
Sale (X5-1) and SM Due Type=H. Accepts 1
decimal place or enter 750 hours as 750 and press
[Field Exit]. Screen will display 750.0.

4.2 digits. Dollar amount of scheduled maintenance
flat rate.

3 characters. User defined. Type of maintenance
contract, such as FSM (Full Service Maintenance)
or ISM (Inspection Service Maintenance).


50 X10-1 ¢ INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT RELEASE 2.3

Notes:


---