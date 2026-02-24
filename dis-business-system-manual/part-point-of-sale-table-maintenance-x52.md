---
title: "PART: POINT OF SALE - TABLE MAINTENANCE (X52)"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about PART: POINT OF SALE - TABLE MAINTENANCE (X52)."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on PART: POINT OF SALE - TABLE MAINTENANCE (X52)."
---

---

## Page 1

## CHAPTER X52-4

VENDOR/CLASS MAINTENANCE

### Introduction

The Vendor/Class table is used when the parts sales are divided by vendor
on the Chart of Accounts. The Vendor/Class Table allows you to affect all
of the individual part sales accounts using only one sales code.

Set up the Vendor/Class Table before setting up your sales codes (X52-3).
When setting up the sales codes, X52-3, use the *CLASS “wild card” as
the credit for the customer and internal side for the documents. The
Vendor/Class Table will only work for parts that are in inventory. For
miscellaneous sales (parts sold without part numbers in inventory) the
Vendor/Class Table is not applicable. See Chapter X52-3, Sales Code
Maintenance.

To get a list of the current Vendor/Class Table:

From the Table Maintenance Menu, select option 4, Vendor/Class
Maintenance. After passing through the security code, press Cmd1.

The Vendor/Class Table wiil print.

### How It Works At Point Of Sale

The format used when creating a sales code for parts is a P. When the sales
code is entered, the following line appears on a document:

PARTS COUNTER
Tax Disc Pty ine $C Ven Qty Part number Price Base

0010 PC MAN 4
Standard line code No demand = Warranty


X52-4 VENDOR/CLASS MAINTENANCE

 

You are required to enter the vendor, quantity and part number of the part
to be sold. When the document is closed, the computer will search the
vendor entered and find the correct sale account to credit.

If you are selling a part not in inventory, the vendor and part number
entered do not mean anything to the computer. Therefore, a Vendor/Class
Table only works for parts with numbers listed in the computer's
inventory.

RELEASE 2.1 C.


X52-4 VENDOR/CLASS MAINTENANCE

 

### How To Run

From the Point of Sale Table Maintenance screen, select option 4,
Vendor/Class Maintenance. Enter a parts vendor code. The following
screen will display:

ABC COMPANY VENDOR/CLASS MAINTENANCE. x5240-101

Entex vendor code STI
Enter class

NEW Vendor/Class

Enter ¥ to CANCEL

 

Enter vendor code:
The vendor name will display under the Vendor code.
Enter class:

Parts are separated into classes on the parts pad. They are assigned to


X52-4 VENDOR/CLASS MAINTENANCE

 

aclass at the time they are entered into your inventory. For example,

you may have fast moving parts in class "F" for fast moving. You may list
obsolete parts in class “O" for obsolete. You will enter a sales account
general ledger number. Decide which classes of parts sold will affect the
parts sale account for this vendor. If all classes of parts sold are credited to
the same general ledger, leave the field blank.

If different classes of parts sales are credited to different general
ledger sales accounts, type the first class. Type the general ledger account

number credited for the sale of the class of parts. Press Enter. Enter the
Vendor code again, and repeat the steps using another class code.

Account

Enter the general ledger sales account number that is credited when the (
parts from the vendor are sold.

‘When the fields on the screen are filled in, press Enter. Repeat the steps
for all of your vendors.

Below is the screen displayed with the STI vendor, class A being credited
to account D3320:

RELEASE 2.1 CU.


X52-4 VENDOR/CLASS MAINTENANCE

 

ABC COMPANY VENDOR/CLASS MAINTENANCE x5240-101

Enter vender code STI
Enter class A

Account 03320

NEW Vendor/Class
Enter ¥ to CANCEL

 

### Changing A Code

To change a sales general ledger account number for a vendor, type over
the general ledger account number and press Enter.

The sale of different classes of parts from vendors can be changed to credit
a different general ledger sale account number. Enter the vendor, change,
type the class. Change the general ledger sale account number. Press
Enter.


X52-4 VENDOR/CLASS MAINTENANCE

 

DELETING A VENDOR FROM THE VENDOR/CLASS
TABLE

Do not delete the vendor from the Vendor/Class Table if the vendor is on
an open document.

Run a Held Documents Report, (X56-2). Review the documents listed on
the report. Close and post any documents using the Vendor to be deleted
from the Vendor/Class Table.

When all the documents with the vendor code to be deleted have been

posted, enter a Y in the filed "Enter Y to Delete". The vendor will be
deleted from the table. (

### What Happens Next

When the Vendor/Class Table is set up or all changes have been made,
press Cmd1 to end the job. The following report will print.

RELEASE 2.1 Co


X52-4 VENDOR/CLASS MAINTENANCE

 

VENDOR /CLASS TABLE 10/01/86 PACE)
x5240- 28

‘VENDOR

CODE Crass ACCOUNT

ae 33390
23395
3350
2395
p3aio
320
2380
3390
23370
3330
33393
23360
29365,
3360
02365
3398

 

### Repeat For Each Division

Vendor/Class Maintenance is divisional. Set up a Vendor/Ciass table for
each division that will run Point of Sale Invoicing (X5-1).


Notes:

RELEASE 2.1 \U

## CHAPTER X52-5

STANDARD LINE MAINTENANCE

### Introduction

Standard Line Maintenance allows you to set up frequently sold parts or
services they do not need to be re-keyed in every time during invoicing.
Only the standard line code needs to be entered. This is a real
convenience, especially when you offer a special and will sell large
volumes of a part or service. For more information on Standard Lines, See
X5-2 Table Maintenance Menu.

Before setting up standard lines, you might want print a list of current
codes. From the Table Maintenance Menu, select option 5, Standard Line
Maintenance. From the Standard Line Maintenance screen, press Cmd1.
The Standard Line Table is printed on the system printer.

### How To Run

From the Point of Sale Table Maintenance Menu (X5-2), select option 5,
Standard Line Maintenance. At the first prompt, type the code that will be
used at Point of Sale, in this case "LABOR." Press Enter. The following
screen appears.

A & R SALES STANDARD LINE MAINTENANCE 5250-202

Enter standard line code LABOR
Creating new standard line
Format _ Valid formats:
‘'M! + Misc. Quantity
Parts
units

Misc. Description
" ~ Labor
"= Received on Account
| - Prepayments
' = Misc. Units

Notes

' + Misc. Costs

## X52-5 STANDARD LINE MAINTENANCE

 

Use the same format as the sales code, which is "L" in our example. If you
have questions regarding the sales codes and their formats, see Chapter
52-3, Sales Code Maintenance. Fields that appear on the next screen
depend on the line format, and are defined in the next section.

A&R SALES STANDARD LINE MAINTENANCE 5250-201 1

Enter standard line code LABOR
Line format L Laker

Sales Code __
Discount Code _
1 -

‘Tax Code - E/C Switch _ {

Job Code

Employee #

Date of Work

Report Hours ____

Bill Hours

NEW standard line code,
Rate per Hour Enter Y to CANCEL _

 

E/C Switch

All formats, except "N" (Note) include a 1- character field labeled "E/C
Switch" as illustrated above.

RELEASE 2.1 LO


‘When using a P (parts) format, a valid priority order code can be used in
the E/C Switch field. The valid priority order codes are P, $8, D, R, Q, and
L. See Priority Orders in the Reference section of Chapter X5-1, Point of
Sale Invoicing for explanation of Priority order codes.

The code entered in the field is used as the default in the Pty field on the
detail line at Point of Sale Invoicing.

When using a D (miscellaneous description) format, enter a C in the field.
The C will display in the Copy field on the line at Point of Sale when the
standard line is used. The information from the standard line will be
copied to Clone documents.

Changing a Code

Enter the code to be changed. Press Enter. Change the fields required.
Press Enter.

Deleting a Code

Type in the Standard Line Code to be deleted. Press Enter. Enter Y in the
field labeled "Enter ¥ to Cancel." Press Enter.

### Field Definitions

Fields that may be displayed are defined below. C = character (letter or
number). D = digit (number). All decimals are assumed. Do not type the


decimal point. Example: 5.2 D = five places in the field with two assumed

decimal places.

### Fields & Descriptions

Sales Code

Discount Code

yw

Tax Code

2C

A valid sales code must be entered. Use the
same sales code that you would enter at
Point of Sale Invoicing if the Standard Line
Code did not exist. The same general ledger
accounts will be debited and credited as
when using the sales code. For more
information on sales codes, see Chapter
X52-3, Sales Code Maintenance.

1c

Type in the discount code that is used most
often. When the Standard Line Code is
entered on a document at Point of Sale
invoicing, the discount code entered will be
the default. You can override the discount
code at Point of sale. The discount code
must be valid. You are not required to fill in
the field. For information on setting up
discount codes, see Chapter X52-6, Discount
Code Maintenance.

In the example, N is the discount code. It
means no discount. Since no discount is ever
given on labor at ABC company, N is
entered.

1 C (or W). Identifies the line as an
Internal or Warranty charge.

1c

NL


Job Code

E/C Switch

Employee #


Type in the tax code that is used most often.
When the Standard Line Code is entered on
a document at Point of Sale, the tax code
entered will be the default. You can override
any information entered. The tax code must
be a valid code. For information on setting
up tax codes, see Chapter X52-7, Tax
Configuration Maintenance.

Jn the example, there is no tax on labor. N is
the tax code.

6C

As set up in optional Service Management.
The code used to define the job being done.
1c

Emergency Order Switch. Enter the code
used for parts priority ordering. If a part
entered at Point of Sale invoicing is not
available for sale, the code used here will
determine the order status of that part. For a
list of Emergency (Priority) order codes for
parts, see Chapter X5-1, Point of Sale
Invoicing. This field is not a consideration
when setting up a Labor Standard Line
code-- leave the field blank.

6c

Number of the employee doing the work.
For the ABC Company, Stanley is the only
employee doing labor for customers.
Stanley's initials are set up as his Employee
#. They are easy to remember. The
Employee # entered must be a valid

Date of Work

Report Hours

Bill Hours

Rate per Hour

employee number as set up in Employee

This is not a required field at Standard Line
Maintenance. If one more than one
mechanic is performing the work, leave the
field blank. The number of the mechanic can
be supplied at Point of Sale Invoicing.

6D

The date the work is completed. This is not a
required field. Since the work Stanley does
is all completed on different days, the field
is left blank. The Date of Work will be filled
in during Point of Sale Invoicing.

5D

Hours it took to complete the work. It takes
Stanley a different amount of hours for each
job he does. Leave the field blank. Fili in the
hours reported during Point of Sale
Invoicing.

5D

Hours you can bill to the customer.
Sometimes Stanley has problems. For
example, he breaks a windshield he is
installing. You cannot bill the customer for
the hours Stanley works cleaning up the
glass. There is no way to predict the billable
labor hours. Leave the field blank and fill it
in at Point of Sale Invoicing.

9D

Rate charged per hour for labor. Type in the
rate used most often. When the Standard


 

Line code is entered, the rate entered will be
the default. You can always

type over the default on a document at Point
of Sale Invoicing.

In the example, the ABC Company charged
$42.00 per hour for Stanley's work. Type
4200 and press the Field Exit key.

An example of a Standard Line Table follows:


STANDARD LINE MAINTENANCE

A&R SMES STANDARD LINE TABLE
BELLINGHAN, WA

P
code,

paces
Line
code

RERERR

ZRREES


e
Pa

ware
Wareanty reac cope

Labor Standard a le To io mergency pate-Tine-werer/

ed ad sd Back 7 Vondor-Parti/ Price

se xe ce Order _W Description code
AAA 9613385

AKA BDPNSRO74AA

ABA 2N6O9
MISCELLANEOUS
MISC HARDWARENB
LBS NOTS AND BOLTS
BAR ETNNGTLGAA,
SHIPPING AND HANDLING a
‘THANK YOU FOR LETTING US SERVICE 109

INCHES 4100 ROLLER CHAT
#100 CONNECTOR LINK

£100 OFFSET LINK

KKK QUARTS 134

KKK  QUARTS 15/40

YOUR EQUIPMENT DURING OUR 1991 3

WINTER SERVICE PROGRAM.
you may 30

RK QUARTS 3007

DepocT
FROM THIS INVOICE, 40

INCHES 440 ROLLER CHAIN

#40 CONNECTOR LINK

#40 OFFSET LINK

INCHES 441 ROLLER CHAIN

#42 CONNECTOR LINK

#41 OFFSET LINK

IF PAID BY S134 P
ABA 9612301

AA 9613292

INCHES 450 ROLLER CHAIN
#50 CONNECTOR LINK

#50 OFFSET LINK

INCHES 160 ROLLER CHAIN
£60 CONNECTOR LINK
ENCHES 46CH ROLLER CHAIN

units
Stock#

coder codes
‘aber ate
Employeet Quantity
2

pate 6/12/92 Page, 1
Time 9.25.30 5250-2

Rate
Rate Key/

Amount
Price
3.99
uP

we

7F

vob Rental
aber Rate/
Report Bill
Hours Hours BP

 
{
NU

## CHAPTER X52-6

DISCOUNT MAINTENANCE

### Introduction

Discount codes allow subtraction of a percentage of the sale on a
line-by-line basis at Point of Sale. The discount code can also function as a
surcharge. A percentage of the sale can be added to the invoice on a
line-by-line basis.

Even if you do not offer customer discounts, you must set up one discount
code. You can set up a "blank" code. We recommend that you use the
blank for the discount offered most often at your dealership. If you do not
offer discounts, use the blank to mean no discount.

Point of Sale Invoicing information is required when setting up a
receivables customer. The fields that must be filled in are discount and tax
code. A "blank" code will register as a valid code. You will not be able to
get off the Receivables Maintenance screen, or close an invoice without
the code.

When the discount codes are set up, assign them to receivables customers
in Receivables Maintenance (X11-2), When a document is opened to a
customer, the discount code will be the default at Point of Sale Invoicing.
This will save the people performing Point of Sale Invoicing typing
strokes. If you decide not to give the discount, the code can be changed at
Point of Sale, line-by-line.

For more information on discounts, see Chapter X52 TABLE
MAINTENANCE.

## X52-6 DISCOUNT MAINTENANCE

 

### Print Current Discount Codes

Before you set up additional discount codes, print current discount codes.
From the Table Maintenance Menu, select option 6, Discount Table
Maintenance. Do not enter a code on the Discount Maintenance screen.
Press Cmd1. The Discount Table will print on the system printer.

### Setting Up Discount Codes

From the Point of Sale Table Maintenance screen, select option 6,
Discount Table Maintenance. The following screen will display: {

RELEASE 2.1 CO


 

DISCOUNT MAINTENANCE X5260-103

Two DISCOUNT CONFIGURATION tables are available.

1. Division D

2. Company

Point of Sale checks the Divisional table first.

Maintain Division or Company table (D/C)? D

cmdi-cancel job

If you have only one division, no decision is necessary. Entering either a D
for divisional or C for company wide table will have the same result.

If you have more than one division, you must decide which table to use.

The computer will search for a divisional table first. If one is not found, a
company table will be searched.

If you have the same discount rates for all divisions, choose a company
table. You will only have to set up the discount codes in one division.
Enter C to maintain a company wide table.


 

If you have one or more divisions that differ in discount rates offered,
select D to maintain a divisional table. Set up the discount codes in each
separate division.

When the decision is made, press Enter. The discount code field is one
character (number or letter). Write the discount codes to be used in the
company's operations.

Below is a suggested list of discount codes. Each dealership is different.
Discount code needs will vary. The table below is just a suggestion:
""(Blank) Make the blank code your most frequently used
discount code. If you do not give very many
discounts, use the blank as no discount.
10%
15% (
20% .
05%
-10% (10% surcharge raises the price of the item
on the document at Point of Sale by 10%.)

URW Ne

RELEASE 2.1 WL


 

Enter the discount code to be set up. The following screen displays:

ABC COMPANY X5260-101

Enter discount code 1

Discount 00000

NEW Discount code,
Enter Y to CANCEL

Supply the rate of the discount. The field is five digits (numbers) long.
Following is an example, the rate of discount is 10%. Type 10% as 10000.


 

AEC COMPANY DISCOUNT MAINTENANCE 5260-102

Enter discount code 1

Discount 10000

NEW Discount code,
Enter Y to CANCEL

 

Press Enter.

### Changing A Discount Code

Type in the code. Press Enter. Change the percentage. Press Enter.


 

### Deleting A Discount Code

Type in the code. Press Enter. Enter Y in the "Enter Y to Cancel” field.
Press Enter.

### Opening A Blank Discount Code

Even if you do not offer discounts, a blank discount code must be set up.
All lines entered at Point of Sale invoicing require a valid discount code.
You will not be able to close a Point of Sale document without a valid
discount code. Use a blank. It means if the discount code field is blank, no
discount is given.

The blank code should be used as the code for the discount code most
frequently used at Point of Sale Invoicing. If the discount you give most
often is 10%, set up the blank code to mean 10%, If you do not usually
give discounts, set up the blank code to mean no discount.

On the Discount Maintenance screen, do not type anything in the field
titled "Enter discount code". Press Enter. The Discount Maintenance
screen will display with an additional field "Discount". Do not type
anything in the field. Press Enter. A "blank" discount code with no
discount rate is set up.


 

ABC COMPANY 5260-104

Enter discount code

Discount 00000

NEW Discount code,
Enter ¥ to CANCEL

 

Press Enter and the blank discount code is set up.

### Setting Up A Surcharge

Many dealerships offer special pricing to businesses that are in the same
business as they are. For example, often there will be an agreement
between part houses to only charge each other 10% above cost of the parts.

You can set up a discount code to reflect a 10% markup on the price. On


the Discount Maintenance screen, type the discount code to be used as the
surcharge. In the suggested Discount Codes Table, we have chosen 5.
Press Enter. On the Discount Maintenance screen, enter 10000 and use the
Field Minus key to show a negative amount. The screen will look like
this:

 

ABC COMPANY 5260-101

Enter discount code 5

Discount 10000-

NEW Discount code,
Enter ¥ to CANCEL

When the discount code is added to the document at Point of Sale
invoicing, it will create a charge of 10% to the document. The figure will
be added to the cost of the parts on the invoice. See the example below:


 

300080 J R SCHUGEL TRUCKING co.

BOX 334

NEW ULM, YN

SOLD BY: PO #: DATE 11/12/86 COUNTER TKT er0a365
SHIP BY:

TD QUAN DESCRIPTION: AMOUNT:

PARTS COUNTER *

### 5 2 Man A104367 Filter

 

On the above document there is a line that lists two fields, T and D. The T
field lists the tax code entered on the line at Point of Sale and the D field
lists the discount code.

In the above example, the D field contains the 5 entered at Point of Sale.
The cost to ABC Company of the filter being sold is $16.00. By using the
"5" discount code, 10% is added to the invoice, charging the J R Schugel
Trucking Company 10% above the cost of the part to the ABC Company.

When a Sales Code is set up in Sales Code Maintenance (X52-3), the
discount account to be credited for the surcharge or debited for the
discount is selected. ABC Company has set up the sales code using the
parts sales account as the discount account to be debited or credited

RELEASE 2.1 tO


when the sales is entered. The accounting for the document created above
would be:

DR _ D1110 (Accounts Receivable) for $17.60
CR 3320 (Parts Sales Customer) for 16.00
CR D3320 (Parts Sales Customer) for 1.60

If you have a separate discount account on your Chart of Accounts that is
debited when customers are given a discount, the sales codes you set up
will contain the discount account from your Chart of Accounts. The sales
code would be entered at Point of Sale, a surcharge code entered and the
accounting would not be correct:

DR D1110 (Accounts Receivable) for $17.60
CR D3320 (Parts Sales Customer) for 16.00
CR D5680 (Discounts Given) for 1.60

When setting up surcharges for documents created at Point of Sale, you
must consider what the accounting will be if a surcharge is created in
Discount Maintenance. There are other ways to set up a customer to be
charged 10% above the cost to the dealership of parts. See Chapter X52-9,
Price Table Maintenance.

When reviewing the Point of Sale batch in X55- 2, the discount code will
display in the third position of the Description field on the credit line to
the sales account. If the figure is not correct, check the Description field.
The wrong code was probably used at Point of Sale.


 

### What Happens Next

When all the discount codes have been created, press Cmd1 to end the job.
A list of all discounts will print. Tape the valid discounts to the terminal
that will be operating Point of Sale Invoicing.

ff more than one machine is used for Point of Sale Invoicing, make
another copy of the discount code. See the What Happens Next section of
ChapterXS-2 Table Maintenance Menu for details.

Below is a sample of the Discount Table:

DISCOUNT TABLE toso1se6 = PAGE 1
x5260- 2a
cope prscounr (

+0000
-10000

-15000
+20000
05000
-10000-

 

RELEASE 2.1 KL

## CHAPTER X52-7

TAX CONFIGURATION MENU

### Introduction

Tax Authorities have different rates for different types of customers and products
within same geographic area. Within the same zip/postal code, a customer might
pay different tax rates depending on the type of business/organization. For
example: the sale of gasoline in Mississippi is taxed at the rate of 18 cents per
gallon for everyone (certain counties may charge an additional 3 cents) except for
Government (US, state, county, city, school district, etc), who pays 5.4 cents per
gallon. Other specific products like diesel fuel and compressed gas are handled
the same way. Some taxes are applied only up to a set limit. Sometimes the limit
applies to the Point of Sale document; other times it is applied line-by-line.

It’s easy to see that you need a computer to keep up with all this complexity. The
DIS/400 Business System handles taxes with the flexibility you need to collect
and report them accurately. All you need to do is the basic setup work; after that,
the system will determine the appropriate tax and accrue it in the general ledger
account you designate. The Tax Maintenance Menu is illustrated below:

COMMAND MENU: X527
(c) DIS Corp.

. Tax Code Maintenance
. Tax Type Maintenance
- Tax Rule Maintenance
. Tax Code Rate Change
. Tax History Maintenance

- Return to Table Maintenance Menu

Ready for option number or command
===>

 

X527.doc 7/29/99 1


2 X52-7 ¢ TAX CONFIGURATION MENU

### Options

1. Tax Code Maintenance

2. Tax Type Maintenance

3. Tax Rule Maintenance

4. Tax Code Rate Change

5. Tax History Maintenance
Use this option to add, change, and delete
tax codes, view the history of changes to tax
codes and print a list of all current tax codes.
If you plan to use Tax Types, set them up in
Tax Type Maintenance (X527-2) first.

Use this option to add, change, delete, and
print a list of all current tax types . Charge
customers can be identified with a tax type
in Receivables Maintenance (X11-2), cash
customers in Address Maintenance (X4-2).
Use this option to create and maintain tax
rules, which are used to determine which tax
code is used at Point of Sale. Rules are
based on zip or postal codes.

Use this option when you want to make a
change that affects several tax codes.
Changes can be made by tax code or
description and restricted by tax type and/or
sales code. For State, County, City, District,
and Other taxes, you can change:

" Base Rate

G/L Account

Limit

Over Limit Rate

Limit Type (D/L)

This option was designed to correct errors
associated with the initial file conversion;
however, it can be used at any time to
correct errors on the Sales Tax Report (X16-
3) or Sales Tax Report by State/County
(X16-4). Only the following fields can be
changed:

= City

= State or province

= Zip or postal code.

la


X62-7 « TAX CONFIGURATION MENU 3

### Overview

Briefly, the features of the DIS’s tax system are:

For each line on a Point of Sale document, the appropriate tax rates will be

determined by a combination of:

— Tax code (expanded to 3 characters)

— Tax type (new 1-character field, used to describe the type of customer,
such as exempt, farm, government, etc.)

— Sales code

Tax codes are no longer divisional.

Tax code groups have been increased to 5 from 4: State, County, City, District

and Other.

Tax codes can be selected automatically at Point of Sale according to the zip

or postal code of the Ship To address or selling division using rules set up in

Tax Rule Maintenance (X527-3).

You can review the history of a tax code (Tax Code Maintenance, X527-1).

A utility, Tax Code Rate Change (X527-4), allows changes to tax codes and

makes the changes on open POS documents only. Rates can be changed on a

range of tax codes, selected by code or description. Changes can be restricted

to a single tax type and/or sales code combination.

The Sales Tax Report (X16-3) has been enhanced to provide different sort

options. A new report, Sales Tax Report by State/County (X16-4) is prepared

from the same data as the Sales Tax Report (X16-3). If you use the same

selection criteria, the totals will be the same, but the reports are sorted

differently. Sorting by County depends on setup in the Tax Rule Maintenance

(X52-7).

A field has been added to General Ledger Account Maintenance (K14-2) to

indicate whether the account should be included on tax reports.

A field has been added to Security Maintenance (X6-6) to determine how

many months of tax history to keep after a general ledger month is closed. the

default value is 3 months. The purge takes place at Accounting End of Month

(X1.10-1 or 2) and clears transactions as well as changes to tax codes and

rates.


4 X52-7 « TAX CONFIGURATION MENU RELEASE 2.3

SETUP

Tax rules can be used to determine which tax code is used at Point of Sale. C
Because the tax rate is determined by where the item is delivered to the customer,

the Ship To address can be used to determine the tax code; otherwise, the system

assumes the customer is taking possession of the item at the dealership and uses

the zip or postal code of the selling division if it is set up in the Tax Rule Table.

Here’s how a tax code is selected:

1. Ifthe customer’s tax rate (in X11-2) is zero, use zero.

2. Use the rate associated with the Ship To address (from Multiple Ship To
addresses), if any.

3. Use the rate associated with the Ship To address entered on the Sold To
screen, if any.

4. Use the rate associated with the selling division’s zip code in Tax Rule
Maintenance, if it is present there.

5. Use the tax code associated with the customer’s record (X11-2) unless it is
overridden by a tax code on a standard line or from Price Table Maintenance

(X52-9).

 

Note
If you want to use tax rules that apply at the selling division’s location, make sure
you enter its zip or postal code in the Tax Rule Table. Canadian dealers must
enter postal codes into the Tax Rule Table exactly the same as they are entered in {
Receivables Maintenance.

 

There is no setup if you are satisfied with the tax codes you had before and want
to keep using the software the same way without taking advantage of the new
features.

To use the tax programs most efficiently, follow these steps.

1. Create tax types in Tax Type Maintenance (X527-2). Tax types can be used
to identify the type of customer, such as Exempt, Farm, Government.
Optional.

2. Create as many tax codes as you need for each tax scenario encountered at
your dealership. Tax codes are created and maintained in Tax Code
Maintenance (X527-1). The same tax types can be associated with multiple
tax codes. The same tax code can be associated with multiple rated depending
on the tax type and sales code.

3. Enter the appropriate tax codes and types for customers in Receivables
Maintenance (X11-2). {


POINT OF SALE X52-7 ¢ TAX CONFIGURATION MENU 5

 

4. In Security Maintenance (X6-6), indicate how many months of tax history to
keep after a general ledger month is closed. The default value is 3 months.
The purge takes place at Accounting End of Month (X1.10-1 or 2) and clears
transactions as well as changes to tax codes and rates.

5. In Account Maintenance (X14-2), indicate which non-sale accounts to use on
the Sales Tax Report (X16-3). Optional.

NW EQUIPMENT SALES GENERAL LEDGER ACCOUNT MAINTENANCE X14201-01
Division: A

Account #: A2220
Title: FLOORING NEW OTHER EQMNT
Edit Code: F
Account #1: A2220
Account #2: A2220
Factor:
Type: L
Cash account? (¥):

You may key "R" to place the account in a restricted

Restrict account: state. Further posting is prohibited but account
balances will be reported. Restricted accounts will
appear on the rolodex.

General Schedule:
Months to keep:

| | Use on Tax Report(¥) _

Cmd3~Return without Save, Enter-Continue

 

6. Create tax rules based on zip or postal codes. If you want to charge tax
according to the location of the selling division to customers who pick up their
items, make sure you enter the zip or postal code of each division in Tax Rule
Maintenance (X527-3). If you want to print the Sales Tax Report by
County/State (X16-4) and have it sorted by County, make sure each county is
associated with a zip code range; otherwise, all cities will be reported under a
blank county within each state. Optional


52-7 ¢ TAX CONFIGURATION MENU

Notes:

## CHAPTER X52-7

TAX CONFIGURATION MAINTENANCE

### Introduction

Tax Configuration Maintenance is used to set up tax codes for use at Point
of Sale. If you store sales tax in different liability accounts, you can charge
up to four different tax rates and store the money in four different general
ledger liability accounts for each tax code.

Many dealerships want to capture tax exempt information on sales. Some
State governments provide a form that must be separated into tax exempt
sales for resale, government, out of state customers, agricultural etc. If you
set up tax codes for all these tax exempt reasons, you can obtain a report
using Transaction Report Writer, (X16-2) or the Sales Tax Report
(X16-3), which will provide this separation for you.

Once tax codes are set up, assign the tax codes to the customers at
Receivables Maintenance (X11-2). The correct tax information will
default on the document created at Point of Sale Invoicing. If the
customer's tax rate is different, the code can be changed on the document
at Point of Sale.

Tax codes are entered on a line-by-line basis at Point of Sale Invoicing.
This way you can tax parts sales but not tax labor sales.

How Tax Codes Work at Point of Sale

Point of Sale Invoicing uses tax codes in the following order:
1) Standard Line

2) Sales Code

3) Customer

Subsequent lines use the tax code established by the standard line or sales
code. Using a new standard line or sales code that carries a non-blank tax
code resets the default; however, you'll need to [Field Exit] through the
default if you want to return to the customer's tax code.

## X52-7 TAX CONFIGURATION MAINTENANCE

 

Printing Current Tax Codes

Before setting up tax codes, get a print of the tax codes already set up. If
no tax codes have been set up, skip this step.

To get a print, proceed into the job. On the Tax Configuration screen, you
will be prompted to enter the tax code. Do not enter a tax code. Press
[Cmd1]. A list of tax codes is printed.

### Determine The Necessary Tax Codes

For more information on Tax Codes and how they work at Point of Sale,
see Chapter X5-2, Table Maintenance Menu.

ABC Company is located in a State that taxes sales on parts but does not
tax labor sales of any type to any customer. Sales are tax exempt if sold for
resale, sold to governmental organizations, for agricultural use or to out of
state customers. The State also requires that sales be reported along with
reasons for exemptions from sales tax for all exempt sales.

The tax rate for the State is 7.3%. The county that ABC Company is
located in charges a sales tax of 2.4% above the State tax rate.

RELEASE 2.1 Lo


The tax code field is one character (letter or number) long. ABC Company
has defined their tax table like this:

CODE DESCRIPTION RATE
1 Normal Tax Rate 9.7%
L Labor 0.0%
G Government 0.0%
R Resale 0.0%
A Agricultural use 0.0%
oO Out of State 0.0%

When one of the exempt codes is used at Point of Sale Invoicing, there is
no tax charged to the customer. The computer records the tax code. At the
end of the month, ABC Company pulls a sales tax code report in
Transaction Report Writer (X1-6) which lists the total of sales, and the
total sales associated with each tax code.

This gives them all the tax reporting information they need to satisfy the
State's reporting requirements.

Based on your State's sales tax reporting requirements, decide what codes
you will need to set up for Point of Sale Invoicing.


 

### How To Run

From the Point of Sate Table Maintenance Menu, select option 7, Tax
Configuration Maintenance. The following screen will display:

TAX CONFIGURATION MAINTENANCE, 5260-103
Two TAX CONFIGURATION tables are available.
1. Division D

2, Company

Point of Sale checks the Divisional table first.

Maintain Division or Company table (D/C)? D

 

 

If you have only one division, no decision is necessary. Entering either a D
for divisional or C for company wide table will have the same result.

If you have more than one division, you must decide which table to use.

The computer will search for a divisional table first. If one is not found, a
company table will be searched.

Tf you have the same tax rates for all divisions, and keep the tax dollars
collected in one general ledger account, choose a company table. You will
only have to set up the tax codes in one division. Enter C to maintain a
company wide table.

f
RELEASE 2.1 Noe


 

If you have one or more divisions that differ in tax rates charged or each
division has its own sales tax liability general ledger account, select D to
maintain a divisional table. Set up the tax codes in each separate division.

When your selection is made, press [Enter]. The tax code prompt appears.
Creating a Tax Code

At the tax code prompt, type the code you want to create, and press
[Enter]. The accounting portion of the screen appears. In the example
below, ABC Company charges 7.3% tax for the state and 2.4% for the
county. Most customers are required to pay sales tax. The following tax
code (1) is set up:

ABC COMPANY TAX CONFIGURATION MAINTENANCE, 5270-101
Enter tax code 1

Tax #1
Tax rate 07300
Account D2250

Tax #2
Tax rate 02400
Account D2270

Tax #3
Tax rate
Account

Tax #4
Tax rate
Account

NEW Tax code,
Enter Y to CANCEL

 


 

ABC Company has two liability accounts for sales tax, D2250 for the
State, and D2270 holds the sales tax payable to the County. 7.3% of the
tax collected is payable to the State, and 2.4% payable to the County. The
customer is charged 9.7%, the total on the Point of Sale document is 9.7%,
but the accounting is correct.

When the tax code "1" is used, the sales tax liability account for the state
will be credited 7.3% of the tax collected, and the County sales tax
account will be credited 2.4%

When the information is filled in, press [Enter]. The tax code prompt is
presented. You can set up another code, or press [Cmd1] to end the job.

Tax Exempt Codes

Looking again at the table used by the ABC Company, there are five tax
exempt tax codes. They need to track sales totals and tax exempt reasons
for labor, government, resale, out of state customers and agricultural
customer.

Following is an example of the labor tax exempt code set up by the ABC
Company:

¢
RELEASE 2.1 Ne


 

ABC COMPANY ‘TAX CONFIGURATION MAINTENANCE 5270-102

Enter tax code L

Tax #1
Tax rate
Account
Tax #2
Tax rate
Account,
Tax #3
Tax rate
Account,
Tax #4
Tax rate
Account

NEW Tax code,
Entex Y to CANCEL

The tax code L was entered. Nothing was entered in the Rate field or in the
account number field. No tax is charged when the L code is used at Point
of Sale and no account is credited.


 

### Changing A Tax Code

From the Point of Sale Table Maintenance Menu, select option 7. Type in
the code to be changed. Change the rate or the account number.

### Deleting A Tax Code

Do not delete a tax code that is on an open or unposted document. Review
a Held Documents Report (X56-2), When all the documents containing the
tax code are closed and posted, delete the code.

From the Point of Sale Table Maintenance Menu, select option 7. Type in

the tax code to be deleted. Enter Y in the "Enter Y to Cancel” field. Press
[Enter].

/
RELEASE21 \_-


 

### What Happens Next

When all the tax codes are set up, press [Cmd1] to end the job. The Tax
Configuration report is printed. Cut out the tax codes and tape them on the
machines where Point of Sale Invoicing is run. If more than one copy is
needed, see "What Happens Next" in CHAPTER X5- 2, Table
Maintenance Menu.

Below is a sample of the ABC Company's Tax Table:

‘TAX CONFIGURATION TASLE woyorses PAGE.
x5270- 28

00000
00000
00000

 


Notes:

{

RELEASE21 = \_.

## CHAPTER X52-8

INVOICE HEADING MAINTENANCE

### Introduction

Invoice Heading Maintenance allows you to print your company logo at
the top of the Point of Sale invoice. It also allows you to print messages.
This job is divisional. If you have more than one division, each division
must have an invoice heading set up.

If you have invoices that have your heading printed at the top, do not set

up a heading in this job. It will print over the pre-printed heading. You can
still set up a message to print at the bottom of the pre-printed heading.

### How To Run

From the Point of Sale Table Maintenance menu, select option 8, Invoice
Heading Maintenance. The following screen displays:


[=| X52-8 INVOICE HEADING MAINTENANCE

ABC COMPANY INVOICE HEADING MAINTENANCE 5280-101
Division: A

Type in the text that is to be
Printed on the top of the invoice:

Press Cmdl to cancel job; Cmd4 to delete.

 

There are twelve lines of typing available from the top of the screen to the
bottom. The screen is 72 spaces wide. To find the center of the line, use
the space bar. Move in 36 spaces. Count the number of spaces for the first
line of typing. Divide by 2. Back up that number of spaces.

ABC Company typed their heading like this:
There are eleven spaces in ABC Company including the space between
the two words. Using the space bar, they moved over 36 spaces. Eleven
divided by 2 is 5.5. They moved back 6 spaces and typed ABC
Company.

They skipped a line and typed the address. They skipped a line and

RELEASE 2.1 (


X52-8 INVOICE HEADING MAINTENANCE [2]

typed the City and State. Next they typed the telephone number. This
week, they are having an equipment sale. They skipped two more lines
and entered the advertising for the equipment sale.

The screen looks like this:

ABC COMPANY INVOICE HEADING MAINTENANCE 5280-102
Division: a

Type in the text that is to be
printed on the top of the invoice:

ABC COMPANY
1dth and Quince Streets
Whynot, Colorado 83247

303-404-5678

DON'T MISS OUR BIG EQUIPMENT SALE
FEBRUARY 25th

Press Cmdl to cancel job; Cmd4 to delete.

 

Below is a sample screen for a company that has pre-printed invoices.
They do not need the name, address and phone number of the dealership.
‘They want to advertise a special. They skipped 9 lines to allow enough
room for the heading to print. The lines wili print on the document below
their pre-printed heading.


[ «| X52-8 INVOICE HEADING MAINTENANCE

ABC COMPANY INVOICE HEADING MAINTENANCE 5280-101
Division: A

‘Type in the text that is to be
printed on the top of the invoice:

OPEN HOUSE IS THE 14th OF THIS MONTH.

HOPE YOU ALL CAN COME.

Press Cmdl to cancel job; Cmdd to delete.

 

### How To Delete The Heading

If you decide to order pre-printed invoices, you will need to delete the
heading you have set up. When the Invoice Heading screen displays, move
the cursor to the first line of the heading. Press the Field Exit key. Move to
the next line and press the Field Exit key. Repeat the process until the
heading is gone. Press Enter. The heading is deleted.

RELEASE 2.1 A

## CHAPTER X52-9

PRICE TABLE MAINTENANCE

### Introduction

The Price Table is used to establish pricing for selected customers, both
cash and charge, and for internal units. The pricing applies only to parts
and can be restricted to certain vendors and/or classes. The special pricing
is used automatically at Point of Sale Invoicing.

A wild card, *STOCK, allows you to specify pricing and a tax and
discount code for all internal units, after which different pricing and codes
can be assigned to individual units.

Example

ABC Company performs warranty work on the major unit lines they sell.
Warrantors are charged 12% above cost for all parts used in warranty
work. The warrantors are:

Vendor: Address #:
MANUFACTURER WARMAN
HONDA WARHON
DETROIT DIESEL WARDET

### Cummins Engines Warcum

When Point of Sale documents are opened to warrantors, they are charged
12% over cost. Without the price table, it would be necessary to remember
who gets special pricing and exactly what that pricing is.


[| X52-9 PRICE TABLE MAINTENANCE

### How To Run

From the Table Maintenance Menu, select option 9, Price Table
Maintenance. The following prompts are displayed:

AEC COMPANY

Address #

Vendor Code
Class Code

Address# or
Unit#

Vendor code:

PRICE TABLE MAINTENANCE x5290-10

or Unit # *STOCK (*STOCK = wild card for all unit#s)

 

Address#. Enter the address number of a
customer who will receive special pricing.
ABC Company wants to tie their warranty
customers to cost plus 12%. They would
enter one of the warranty customer numbers.

Unit#. Enter a unit# that will receive special
pricing. To establish defaults for all units,
use the wildcard *STOCK.

Enter a 3-character vendor code that is
eligible for the special pricing. ABC
Company does warranty work for
Manufacturer, Honda, Detroit Diesel and
Cummins Engine.

When they are doing warranty work for
Manufacturer, only Manufacturer parts
would be sold at the special price. When
working for Honda, Honda parts are sold to
Honda at a special price, and so on, Other


X52-9 PRICE TABLE MAINTENANCE [:]

parts would be charged to the warranty
customer at full dealer list price.

A blank vendor code means that the special
price applies to all vendors.

Class code: Enter a class of parts that will be sold at the
special price. ABC Company offers all
classes of Manufacturer parts to the
corresponding warranty customer at the
special price.

Leave the Class code blank and all classes
will be sold at the special price.

 

 

 

When the fields are filled in, press [Enter].

## X52-9 PRICE TABLE MAINTENANCE

When you enter the the Price Table Maintenance screen , the Price Rate
field will contain all zeros. If you do not change the zero rate, the
following message will be displayed at the bottom of the screen:

AGR EQUIPMENT SALES PRICE TABLE MAINTENANCE 5290-101
Address # WARMAN Or Unit # *STOCK (*STOCK = wild card for all units)

Vendor Code
Class Code

Price Rate...

Price Code... Price codes:
= Dealer List
Tax Code... - Suggested List
- = Internal (
Discount Code. - + = Dealer Net
+ = No Code Entered

New Address/Vendor/Class
Entex ¥ to cancel

DIS-0004 Warning: Price rate equals zero. Presa enter to confirm.

 

‘You can press enter to confirm the zero rate or change it now.

RELEASE 2.1 Co


X52-9 PRICE TABLE MAINTENANCE [=]

ABC COMPANY PRICE TABLE MAINTENANCE x5290-101

Address # WARMAN Or Unit # *STOCK (*STOCK = wild card for all unit#s)
Vendor Code
Class Code

Price Rate. . .

Price Code... Valid price codes:
‘4° - Dealer bist
"3' - Suggested List
Internal
Dealer Net
- = No Code Entered

New Address/Vendor/Class
Enter ¥ to cancel

 

The screen illustrated above is an example of the warranty address
number, WARMAN, set up to charge the warranty customer 112% of

cost.

Price rate: Percentage. ABC Company is charging 12%
over cost (112%) to WARMAN. Enter
112% as 11200 and press [Enter].

Price code: You will recognize the four price codes as


[ «| X52-9 PRICE TABLE MAINTENANCE .

set up in Configure Vendor/Class (X38-1).
The cost of the part is called the dealer net
price. The dealer net price code is 1.

If you are selling parts at a percentage of
dealer list price, the price code would be 4.
If selling parts at a percentage of suggested
list, the price code would be 3.

ABC Company is charging 112% of cost to
WARMAN. The Price code is 1.

 

 

 

Press [Enter] to add the customer's special pricing to the Price Table.

 

### Deleting An Entry From The Price Table

When you first enter Price Table Maintenance, the Price Rate field will
contain all zeros. The Price Code will be blank. Jf you bring up an address
or unit number that does not belong on the Price Table, you must delete it.
If you press [Enter], the following message will be displayed at the bottom
of the screen, “Warning: Price rate equals zero. Press enter to confirm." If
you press enter, the customer or unit will be charged the percentage of the
price rate and the price code displayed on the screen, which are:

Price rate: 00000
Price code:

To delete the customer, enter Y in the "Enter Y to Cancel" field.

(
RELEASE 2.1 NL

### Examples

ABC Company offers special pricing to three competitors which purchase
parts from them, 90% of the dealer list price or 10% discount on all parts.
The three competitors give ABC Company the same price break when
ABC Company purchases parts from them. They are:

Company: Address #:
JR Shlagel Trucking JRSH96
Anderson Parts & Service ANPA90
Crenshaw Glass CRGL86

Below is a sample of how this would be set up in Price Table
Maintenance:
ABC COMPANY PRICE TABLE MAINTENANCE *5290-101
Address # ORSH96 or Stock # ("STOCK = wild card for all unit#s)
Vendor code
Class code
Price rate 09000

Price code 4 Valid price codes:
‘4° - dealer list

‘3’ - suggested list

‘2' - internal
‘1’ - dealer net
- no code entered

NEW Address/Vendor/Class
Enter ¥ to CANCEL

 


ABC Company works on their rental units as necessary. They replace
belts, change the oil and wash the units. They want only the cost of parts
to be charged to the inventory account that is tied to the rental unit. The

rental units are:

Unit:

UC5320
UH7654
UK4921

Following is an example of how a unit would be tied to the Price Table:

 

ABC COMPANY

Address &

vendor code

Class code

Price rate .

Price code. . .

Tax code... .

Discount code

Unit (Stock) #:

Used Case Backhoe

A rental 1984 Honda Sedan
Used Kubota Rotatiller

  

PRICE TABLE MAINTENANCE x5290-101,

or Stock # C5320 (*STOCK = wild card for all unitts)

Valid price codes:

"a! + dealer list

‘3! - suggested list
2) ~ internal
"1! - dealer net

- ~ no code entered

NEW Address/Vendor/Class
Enter ¥ to CANCEL

RELEASE 2.1 a


ABC COMPANY
BELLINGHAM, WA

CUSTOMER NAME

ANDERSON PARTS & SERVICE

CRENSHAW GLASS
JR SHLAGEL TRUCKING

WARRANTY MANUFACTURER
WARRANTY CUMMINS
WARRANTY DST DIESEL
SABRANTY HONDA
sTocKe


When the Price Table has been set up, press Cmd1 to end the job. The
following prompt is displayed:

PRICE TABLE MAINTENANCE x5290-102

For a listing of the customer price table enter ‘y'

 

Enter ¥ for a list of the Price Table. The Price Table Listing which follows
is for the ABC Company.

PRICE TABLE LISTIRG 2172/97 PAGEL.
POINT OF SALE INVOICING SYSTEM 5220-28,

STOCK #/ VENDOR CLASS aK
ADDRESS # © CODE CODE

aNpago
cRGLES
JRSHSE
ARAN
waRcuH
WaRDET
‘WARHON
stock
ucs326
wH76s4
uxeg21


Notes:

{
RELEASE 2.1 Ne

## CHAPTER X52-10

POINT OF SALE DEVICES

### Introduction

The purpose of this job is to simplify and speed up printing at Point of Sale by
defining printer characteristics. Each workstation is assigned to a specific printer.
It is possible to allow the user to change printers, if necessary.

These steps must be completed before you attempt to use Point of Sale.

### Contents

ENTRANCE SCREEN .......ccccssssessssssssorssecnssesssessscsonesosecseesneescereusoueseseaseene 2

POINT OF SALE PRINTERS.
Reprinting archived documents ..
How to delete the printer from the Point of Sale .

 
 
 
 

 

POINT OF SALE WORKSTATIONS


2 CHAPTER X52-10 ¢ POINT OF SALE DEVICES RELEASE 2.2

### Entrance Screen

From the Table Maintenance Menu, select option 10. The Select Type screen
appears, as illustrated below:

  
    

  
 
   
 

  

ABC COMPANY

 

POINT OF SALE DEVICES
Select Type

XS2A0-101

    

1. Point of Sale Printers
2, Point of Sale Workstations

Enter option:

 

 
 

Gmd1-End job

The process involves the following steps:

1, Point of Sale Printers. Describe POS printers in the same way they were
described on the Point of Sale Options screen: heading lines and left margin.
2. Point of Sale Workstations. Assign printers to workstations and specify
whether the printer can be changed at the Point of Sale Options screen.

NL


POINT OF SALE CHAPTER X52-10 « POINT OF SALE DEVICES 3
—— Oe eee rr oe ree ee

### Point Of Sale Printers

This option allows you to describe Point of Sale printers. From the Printer screen,
you can specify the length of the forms you are using at Point of Sale, whether
you want to use the printer as the default for unassigned workstations, and the
number of lines to allow for the preprinted footer (disclaimer or other information
at the bottom of the invoice).

From the Select Type screen, select option 1, Point of Sale Printers. A prompt for
the printer ID appears, as illustrated below.

ABC COMPANY POINT OF SALE DEVICES X52A0-102
Printers

printer:

cmd3-Return

 

Type the first printer ID and press [Enter]. The second part of the screen appears.


4 CHAPTER X52-10 » POINT OF SALE DEVICES RELEASE 2.2

 

 

ABC COMPANY POINT OF SALE DEVICES X52A0-105
Printers

Printer: P4

Length of forms in inches. . 2... 22... 01. a.
Number of invoice heading lines {0-12) ....... —
Number of spaces left of normal to print (0,5)... . 0
Use this printer for unassigned workstations? (¥/N) . N
Is there a preprinted footer on the invoice? (¥/N). . ¥

Tf so, enter # of footer lines (1 inch = 6 lines) . 9

Enter-Continue Cmd19-Delete printer

 

 

For "Number of invoice heading lines (0-12)" and “Number of spaces left of (
normal to print (0,5)" use the following table: :

 

  
   
  
  

Printer Invoice heading lines | Spaces left of normal
IBM Model 5256 9
IBM Model 4214 i2
IBM Model 4224 1
IBM PRO 12
Okidata (320,321, & 8
320 Turbo)

 

 

 

 

 

Alafulolo

 
 

 

 

 

Default printer
If you change the default of "N" at "Use this printer for unassigned workstations?
Y/N," the printer will be used for all workstations that have no assigned printer.

Only one printer can serve as the default; therefore, the printer where you change
“Use this printer for unassigned workstations?" = "Y" most recently will be used.


POINT OF SALE CHAPTER X52-10 « POINT OF SALE DEVICES 5
ee Or SE eee

Workstation
Workstation
Workstation
Workstation
Workstation
Workstation
Workstation

 

The default printer has been added to the report that is printed when you leave this
job.

POINT OF SALE DEVICES Date 4/02/99 Page 2
Time 9.33.57 X52A0-201

## Spaces Left Default Printer Allow Change

x
x
x
u
y
x
a
zg
¥
¥
x
y
N
N
x
¥
x
N
x
N
¥
N

How to determine the number of footer lines

To determine the number of footer lines, measure the box at the bottom of the
invoice where the disclaimer or other information is Printed. There are 8 lines per
inch. If your footer is 1 '/g", the nurnber of lines will be 5/g x 8 = 9 lines {use
whole numbers only).

 
 

Header: Company Name, etc.

  

‘You may have to experiment by
reprinting a couple of invoices to
get the alignment just right. If the
signature line is printed too low,
increase the number of footer lines.

 

 

Total $

=


6 CHAPTER X52-10 « POINT OF SALE DEVICES RELEASE 2.2

Reprinting archived documents C ,
Archived documents retain the printer information that was current at the time

they were archived; therefore, if you have changed form length or footer lines,

you'll want to send the archived documents to a printer that has the same values as

the original printer. Or, you can change the change forms on the original printer

long enough to reprint the archived document, and the values associated with the

original document will temporarily override the values assigned in Point of Sale

Devices (X52-10).

When you reprint an archived document in Work with Archived Documents
(X.12-1), you can determine the length of the original form from the Lines Per
Inch (LPI) and Lines Per Page (LPP) values. For example, on the screen
illustrated below, LPJ=8 and LPP=56, which means that the original form was 56
+8 or 7 inches long. You can ignore CPI, which refers to the number of
Characters Per Inch, measured horizontally. See the screen below.

 
 
   
 
    
    
    
  
    
 

 

A&R EQUIPMENT

 

Work with Archived Documents

 

Enter Printer

Print Archive Document

Date Time Type Description a :
Divide LPP by LPI
2/11/98 9:25:37 POS DIV A CTQ0282 000001 CLOSED . i
to determine the
length (in inches)
Document LPI: 8 Document CPI: 10 Document LPP: 56 a i
of the original
form. :

AS/400 Printer... t
. 56 +8=7 inches.

Page range to print: 3

Starting Page . 1 (Number)

Ending Page . . *END (Number or *END)

F3sExit F4=Prompt F12=Previous

 

 

The table below shows the relationship of the most popular form lengths and
Lines Per Page (LPP). Point of Sale documents are printed at 8 Lines Per Inch.


POINT OF SALE CHAPTER X52-10 « POINT OF SALE DEVICES 7
———— To Ore rr Creole

How to delete the printer from the Point of Sale

1. To delete the printer from the Point of Sale printer list, press [Cmd19]. This
action does not delete the printer from your AS/400 configuration.

2. Repeat for other Point of Sale printers.
3. Press [Cmd3] to retum to the Select Type screen.

### Point Of Sale Workstations

This option assigns workstations to Point of Sale IDs and allows you to specify
whether the user can use a different ID if necessary.

From the Select Type screen, select option 3, Point of Sale Workstations. A
prompt for a workstation address appears:

ABC-COMPANY POINT OF SALE DEVICES X52K0-104 4
Workstations

Workstation: __

 

Type the first workstation address and press [Enter]. The remainder of the screen
is displayed.


8 CHAPTER X52-10 » POINT OF SALE DEVICES RELEASE 2.2
SS Ee remee

ABC COMPANY POINT OF SALE DEVICES XS52A0-107 7 {
Workstations

Workstation: A8

Default printer

Allow user to change assignment (¥/N) .

Enter-Continue Cmd19-Delete Workstation

 

To delete the workstation assignment, press [Cmd19].

- To add or change, type the printer ID that will be assigned to the workstation. (
3. Answering "Y" at the next prompt allows the user at this workstation to select
a different default printer at the Point of Sale Options screen. Answering "N"
means that no choice is possible and the Point of Sale Options screen is
bypassed altogether.

Repeat for other workstations.

Press [Cmd3] to return to the Select Type screen.

When your choices are complete, press [Cmd1] at the Select Type screen to
return to the Table Maintenance Menu. A list of Point of Sale devices is
printed automatically. An example follows.

Nr

aak

PODNT OF SALE DEVICES Date 10/16/97 Page
‘Time 16.22.23 XS2A0~101

i Heading Lines 4 Spaces Left Default Printer

Workstacion
Workstaric

Workst

Workstation

Workstation YA PL

- This printer will be used for any workstation net liste in this table.

x
¢
¥
y
Nu
x
x
N


POINT OF SALE CHAPTER X52-10 « POINT OF SALE DEVICES 9
oa OOo

### Point Of Sale Options Screen

If you answered "Y" at the prompt, "Allow user to change assignment," which
appears on the Point of Sale Devices-Workstations screen, a prompt for the
printer ID appears on the Point of Sale Options screen.

If "Allow user to change assignment" = "N,” the user proceeds directly to the
Price Book Selection Screen.


10 CHAPTER X52-10 * POINT OF SALE DEVICES RELEASE 2.2

Notes:

## CHAPTER X52-11

SELF SERVICE INVOICING DEFAULTS

### Introduction

Use this job to identify the document classification code and part sales
code that are used as defaults in Self Service Invoicing (X5-9).
Instructions for setting up a User Profile for a remote user are included at
the end of this chapter.

### Preparation

0 In Document Classification Maintenance (X52-2), set up a document
code. An example is illustrated below.

A GR SALES & SERVICE DOCUMENT CLASSIFICATION *5220-101
Maintenance
Enter classification code E

Description SELF SERVICE

Document tyre S Valid document types:
"Q' - quote
‘S' - sales order
‘W! - work order

Posting option A Valid options:
'A' = automatic posting
‘M' - mapual posting
"= quote

Pricing detail ¥ Valid options:
'¥' + pricing on each line
'N' - pricing on final total only

Sequence # 8$ 01001
NEW Classification code:
Enter ¥ to CANCEL

## X52-11 SELF SERVICE INVOICING DEFAULTS

 

 

 

 

("P").

An example is illustrated below.

A & R SALES & SERVICE

Sales Code EE

SALES CODE MAINTENANCE

Description SELF SERVICE

Format

Customer Document
Internal Document
Warranty Document
Journal Id
Override Tax Code
Qverride Discount
Vendor for Parts
GST Rate

GST Account

Grdl-End job  ¢md3-Go back

‘ye
D
an
uw
‘Ne

cred:

3320
*ERRO!

lopt:

(md1§-Delete this sales code

Labor

Misc, Deseription
Misc. Quantity
Mise. Units
Notes

© Discount
3320
R “ERROR,

*ERROR © "ERROR

ional)

In Sales Code Maintenance, set up a sales code with a parts format

X5230-201

New Sales Code

Parts
Prepayments
Received on Account
Unit Sales
Misc. Cost
Cost Misc Qty
Card‘ account #'s:
- any format
- Pt or ‘w
format only
- any format

 
LL


X52-11 SELF SERVICE INVOICING DEFAULTS [=]

AS/400 Users. In Point of Sale Devices (X52-10), select option 2, Point of
Sale IDs. Set up a unique Point of Sale ID for Self Service Invoicing and
link it to a printer. An example is illustrated:

A & R SALES & SERVICE POINT OF SALE DEVICES xS2A0-106
Tas

Point of Sale Id: E

Default printer
Work order log printer .

 

Also in Point of Sale Devices, select option 3, Point of Sale Workstations.
Link the new ID to a workstation, as illustrated below:

A & R SALES & SERVICE POINT OF SALE DEVICES X52A0-107
Workstations

Workstation: x3

Point of sale id assignment
Allow user to change assignment (¥/N} .

 

5/36 Users. Decide on a unique Point of Sale ID, one that is not used for
Standard invoicing. Use it at the Point of Sale Option Screen.

AS/400 Users. It is possible to set up a user profile that will allow a
customer (probably at a remote site) to enter directly into Self Service
Invoicing and exit back to the sign on screen. Follow the instructions at
the end of the chapter.


[+] X52-11 SELF SERVICE INVOICING DEFAULTS

### How To Run

 

 

 

From the Table Maintenance Menu (X5-2), select option 11, Self
Service Invoicing Defaults.

 

 

(Nvi EQUIPMENT SALES Self Service Invoicing Defaults *52B01-01
Division: A

Decument Code : C COUNTER TICKET

Sales Code : PC PARTS CUSTOMER (
Allowed Options

CMD2-Print & Clese wan

Priority Orders from inventory (yan

Priority Orders from Price Book can)

 

O Type the document and sales codes you want to use for Self Service

Invoicing,

0 Configure allowed options.

Cmd2 - Print and Close Y/N. If Y, customers will be allowed
to print and close tickets; otherwise,
invoices are printed and held as open
documents.

RELEASE 2.1 ‘oe


X52-11 SELF SERVICE INVOICING DEFAULTS [=]

Priority Orders from Inventory Y/N. If Y, customers will be allowed
to create priority orders from
inventoried parts; otherwise, they
must enter a different part number.

Priority Orders from Price Book Y/N. If Y, customers will be allowed
to create priority orders from parts in
the price book; otherwise, they must
enter a different part number.

O Press [Enter]. Press [Cmd1] to end the job.


Setting Up a Remote User Profile

AS/400 Users. It is possible to set up a user profile that will allow a
customer (probably at a remote site) to enter directly into Self Service
Invoicing and exit back to the sign on screen.

Q Sign on as QSECOFR.
O At acommand line, type: CRTUSRPRF and press [F4]=Prompt. The
create User Profile screen prompts for the ID:

Create User Profile (CRTUSRPRF)
Type choices, press Enter.

User profile SSTBATLEY Name (
User password $813953 Name, *USRPRF, *NONE
Set password to expired... .  *NO *NO, *YES
Status *ENABLED *ENABLED, *DISABLED
User class... - . +USER, *USER, *SYSOPR, *PGMR...
Assistance level *SYSVAL *SYSVAL, “BASIC, *INTERMED.
Current library LIBRARY Name, *CRTDFT
Initial program to cali. . . . > x59SSID Name, *NONE

Library LIBRARY Name, *LIBL, *CURLIB
Initial menu - MAIN Name, *SIGNOFF

Library *LIBL Name, *LIBL, *CURLIB
Limit capabilities *No *NO, *PARTIAL, *YES

Text ‘description’ ‘Self Service Invoicing - J.R. Bailey’

More...
F3-Exit Fd=Prompt F5sRefresh F12=Cancel F13=How to use this display
F24=More keys

 

RELEASE 2.1 Co


 

 

 

 

Fumish or change the following values only:

User profile (your choice)

User password (your choice)

Current library LIBRARY

Initial program to call X59SSID
Library LIBRARY

Limit capabilities *YES

Text ‘descriptions’ (your choice)

Your screen should look like the screen illustrated above.
O Press F10=Additional parameters. Press [PgDn].

Create User Profile (CRTUSRPRF}

Type choices, press Enter.

Additional Parameters

Special authority >*jobet1 *USRCLS, *NONE, *ALLOB...
+ for more values >*savsys
Special environment *SYSVAL, *NONE, *S36
Display sign-on information ..  *SYSVAL *SYSVAL, *NO, “YES
Password expiration interval . *SYSVAL 1-366, *SYSVAL, *NOWAX
Limit device sessions . . . SYSVAL *SYSVAL, *YES, *NO
Keyboard buffering *SYSVAL *S¥SVAL, *NO, *TYPEAHEAD,..
Maximum allowed storage . . . .  *NOMAX Kilobytes, *NOMAX
Highest schedule priority ... 3 0-9
Job description QRPTJOED Name
Library *LIBL Name, *LIBL, *CURLIB
*NONE Name, *NONE
*USRPRE *USRERF, *GRPPRE
More...

F3sExit F4=Prompt FS5=Refresh Fi2=Cancel F13=How to use this display
F24sMore keys

 


c
Change the following values only:
Special authority *JOBCTL
+ for more values *SAVSYS
Special environment *836
O Press [PgDn].
Create User Profile (CRTUSRPRF)
Type choices, press Enter.
Group authority *NONE, *ALL, “CHANGE, *USE...
Accounting code
Document password Name, *NONE
>ssibailey Name, *USRPRF
Library ....- >qusrsys: Name, *LIBL, *CURLIB
*NOTIFY, "BREAK, *HOLD, *DFT {

Severity code filter 0-99
Print device Name, ‘*WRKSIN, *SYSVAL
Output queue Name, *WRKSTN, “DEV

Library Name, *LIBL, *CURLIB
Attention program >x59attnel Name, *NONE, *SYSVAL, ‘ASSIST

Library plibrazy Name, "LIBL, *CURLIB
Sort sequence *SYSVAL Name, *SYSVAL, *HEK...

Library Name, *LIBL, *CURLIB
Language ID ~SYSVAL *SYSVAL.
Country ID *SYSVAL *SYSVAL...

More...

F3-Exit F4=Prompt F5-Refresh F12=Cancel  Fi3=How to use this display
F24=More keys

 

O Change the following values only:

Message queue (same as user profile)
Library LIBRARY
Attention program XS9ATTNCL
Library LIBRARY

RELEASE 2.1 LL

### X52-11 Self Service Invoicing Defaults [2]

O Wher the 3 screens have been completed, press [Enter].
O Sign off, then sign on with the new profile and set the environment.


Notes:

## CHAPTER X52-12

CASH INVOICE HEADING MAINTENANCE

### Introduction

This job is like Invoice Heading Maintenance (X52-8) except that it is for
a 40-character strip printer. Both headings and footings can consist of 12
lines of 40 characters each. A function key (Cmd6) toggles from heading
to footing maintenance screens.

### How To Run

From the Table Maintenance Menu (X5-2), select option 12, Cash Invoice
Heading Maintenance. The Maintain Heading screen appears.

PACIFIC BOQULEMENT CASH INVOICE HEADING MAINTENANCE x52c0-101 1
Division: A Maintain Heading

‘Type in the text that is to be printed
on the top of your cash invoices

1234567890123456789012345678901234557890
HANK YOU FOR SKOPPING AT.
PACIFIC EQUIENENT CO.
SALES & SERVICE.

Cmdi-End Job cmad-Delete cmdé-Heading/Footing

## X52-12 CASH INVOICE HEADING MAINTENANCE

 

O Type the heading and press [Enter].

0 To delete both heading and footing and return to the Table Maintenance
Menu, press [Cmd4].

O To end the job press [(Cmd1].

O To type a footing, press [Cmd6]. The Maintain Footing screen appears.

RELEASE 2.1 LO


 

Maintain Footing Screen

 
  

  

   
 

PACIFIC EQUIPMENT CASH INVOICE HEADING MAINTENANCE x52C0-102 2
Division: A Maintain Footing

     

Type in the text that is to be printed
on the bottom of your cash invoices

         


 

Y'ALL COME BACK SOON!
1234567890123456789012345678901234567890

 

    

an

    
  

oo @


 

ne

 

Cmal-End Job Cmd4-Delete Cmé6-Heading/Footing

O Type the footing and press [Enter].

 

 

 

 

To end the job, press [Cmd1].

O To return to the Maintain Heading screen, press [Cmd6].

0 To delete both heading and footing and return to the Table Maintenance
Menu, press [Cmd4].


Notes:

i
RELEASE 2.1 ee

## CHAPTER X52-13

CASH TENDERING MENU

### Introduction

When Cash Tendering is installed, a special screen, which records cash
dispensation, is displayed when a Point of Sale document is closed or
re-opened. Multiple payment types can be included on a single invoice.
Invoices may be printed on the standard store printer or on a special cash
printer, which uses continuous-roll paper that accommodates 40
characters.

Tickets cannot be voided unless they are re-opened first. As a ticket is
re-opened, the cash tendering screen is displayed (if appropriate) and the
cash drawer will open (if drawers are installed).

When the Point of Sale batch is created, a cash tendering audit report is
printed. The report is sorted by drawer or by workstation (if multiple
drawers are not installed). Parts End of Day reorganizes the Cash
Tendering files. See Technical Notes.

The foliowing options are available:

0. No cash tendering.

1. Cash tendering with no cash drawers.

2. Cash tendering with one drawer, no security.

3. Cash tendering with multiple drawers (maximum is 8), full security for
each drawer.

With options 2 and 3, the drawer opens any time it is necessary at Point of
Sale, and at any other time by typing "OPEN" at the bottom of any menu.
The drawer can also be opened using Open Cash Drawer (X52.13-4).

Screens in this chapter illustrate Option 3 for multiple drawers and full
security.

## X52-13 CASH TENDERING MENU

 

} DIS will set the switches on the cash drawers before they are shipped.
Each drawer has a unique signal that opens it. Cash drawers are

physically cabled as if they were PC printers. They should be
configured on the S/36 and AS/400 as printers even though no printer
is physically attached to the drawers. Two or more drawers can be
hooked in series and open independently even though they share the
same printer ID.

 


RELEASE 2.1 Ne

### How To Run

From the Table Maintenance Menu (X5-2), select option 13, Cash
Tendering Menu. The menu is illustrated below:

COMMAND. : INQUIRY x3
{e) DIS Corp.

: Cash Drawer Configuration

- Gash Drawer Security

. Cash Tendering Sales Code Maintenance
- Open Cash Drawer

. Return to Table Maintenance Menu

Ready for option number or command

ze=>

 

OVERVIEW OF CASH TENDERING MENU OPTIONS

X52.13-1. Cash Drawer Configuration
Cash drawers are configured as printers on the $/36 and
AS/400. Use this job to identify the corresponding printer
IDs. If two or more drawers are cabled in series from the


X52.13-2.

same PC, they share the same printer ID. The drawers
operate independently even in series.

Cash Drawer Security

Full security is available when there is more than 1 cash
drawer. Use this job to enter security codes for 1-8 cash
drawers.

Note:

| No security code is necessary for a single cash drawer.

 

X52.13-3.

X52.13-4,

Cash Tendering Sales Code Maintenance (
Use this job to list sales codes that will cause the Cash

Tendering screen to be displayed at Point of Sale. The

screen will be displayed for both cash and charge sales

when one of these sales codes appears on the document.

You may enter up to 30 sales codes for each division.

Open Cash Drawer

Use this job to open a cash drawer. Another way to do the
same thing is to type "OPEN" at any menu and press
(Enter]. In both cases, you are prompted for a security code
if there is more than 1 cash drawer.

RELEASE 2.1 Ke

### Cash Tendering Screens At Point Of Sale

When you press [Cmd2] to print and close a document that includes 1 of
the sales codes entered in Cash Tendering Sales Code Maintenance
(X52.13-2), the following screen is displayed:

A-PACIFIC EQUIPMENT CLOSE INVOICE 10/01/93 X510$-901 1

INVOICE # CT00101 For 000056
Subtotal... |. 112.32
Tex ee ee 8.76
Amount Due 121.08
Payment, Amount Expiration
Method Received Date

1-cash
2-Check
3-Bank Card

 

 

O Type 1, 2, or 3 in the column labeled "Payment Method."

O Type the amount received and press [Field Exit].

C1 If the customer is using a bank card, an expiration date (MMYY) is
required.

O Repeat until the payment is equal to or greater than the amount due,

then press [Enter] to display the rest of the screen.


 

A-PACIFIC EQUIPMENT CLOSE INVOICE 10/01/93
INVOICE # CTOO101 For 000056

112.32

Expiration

Change Due . .
Drawer Code. .

cmd3-Go Back

 

 

 

 

Tf you recognize a mistake, press Cmd3-Go Back.

O Press [Enter] to return to the Point of Sale Entrance screen.
x5105-901 1

 

‘


 

GETTING STARTED

Installation

Cash Tendering is an option in the OPTDIS Library. See the Appendix for
details concerning installation.

Before Cash Tendering can be used, the following setup work is required:

O Set up printer addresses in Cash Drawer Configuration (X52.13-1).

O Ifyou are using multiple cash drawers, set up security codes for each
drawer in Cash Drawer Security (X52. 13-2).

O Set up sales codes that should always trigger the cash tendering screen,

even for charge tickets in Cash Tendering Sales Code Maintenance

(X52.13-3).

If you are using a cash printer, set up its ID in Security Maintenance

(X6-6). In addition, set up its header and footer lines in Cash Invoice

Heading Maintenance (X52-12).


Notes:

RELEASE 2.1 LL

## CHAPTER X52-14

CREDIT CARD MAINTENANCE

### Introduction

This option is used to set up codes for the credit cards used by each division after
the receivables address and corresponding general ledger account have been
established. Even if you don’t have a DataTran device, you can set up the credit
cards accepted at your dealership—just be sure to set EDC Capable=N.

You can use Receivables Maintenance to store credit card information, including
a default card, for each customer. Only Case Credit and Farm Plan card numbers
can be captured from Point of Sale.

### Contents

CREDIT CARD SET UP...
ENTRANCE SCREEN......
Credit Card Maintenance/Card Lis!


2 X52-14 e CREDIT CARD MAINTENANCE RELEASE 2.1

### Credit Card Set Up

Two credit cards will be set up by the system the first time you select Configure
Credit Cards after their respective OPTs are turned on:

1. Case Credit. The credit code is “CC.” You will have to furnish a receivables
address and, if you have a DataTran device, make EDC Capable=Y; otherwise
“N.” It is a private card.

2. Farm Plan. The credit code is “FP.” You will have to furnish a receivables
address and make EDC Capable=N. It is a private card.

You can set up all major credit cards, such as MasterCard, Visa, Discover,
American Express. If you have a DataTran device, just be careful to set EDC
Capable=N for the cards that are not associated with FDR. If you don’t have a
DataTran device, set EDC Capable=N for all cards.

### Entrance Screen

CO From the Point of Sale Table Maintenance Menu (X5-2), select option 14,
Credit Card Maintenance. The entrance screen is illustrated below.

Credit Card Maintenance/Card List

     
 

  

A-AGR CASE EQUIP

 

Credit Card Maintenance
Card List

     
 
 
 
 
   
    
 
   
   
  
 
  

EDC Capable =Y
only if you have

 

        
     
 

       

 
 
  
 
  
  

  
  
 

a DataTran Name Receivables Wournal| EDC Private
device and then Address # Capable? Card?
_ AG Agline AGLINE Ez
only for cards = cc case credit CASCRE E ¥ ¥
that will be _ FP Farm Plan FARMOL z
— omc Master Card MASTER = x
processed by — VI VISA VISA E
FDR.

 

 

 

This column is not visible
unless the Journals OPT
is on.

     

F3=Exit | F6=Add  F12=Previous

   

When the credit card software is installed, 2 card types will be pre-configured if
their respective OPTs are on: CC for Case Credit and FP for Farm Plan if you are
in the U.S., AG for Agline if you are in Canada (the system determines what
country you’re in by the postal code in Security Maintenance).

t.


POINT OF SALE X52-14 » CREDIT CARD MAINTENANCE 3
oe rr eeEeETEE eee

EDC Capable=Y means that you have arranged with FDR to authorize and send
transactions for this credit card electronically. If you have a DataTran device, you
can accept credit cards that don’t use it; however, you must set EDC Capable=N.

Private Card=Y means the card is proprietary and not one of the major credit
cards. Private cards are Case Credit, Farm Plan (or Agline), and New Holland.

O To add new credit cards to the table, press F6=Add. A blank list appears, as
illustrated below.

A-AER CASE EQUIP Credit Card Maintenance
Card List

a
5
a
2
g
@

Receivables Journal EDC Private
Address # Capable? card?

Pbterrrttrinag
Prretrrartera
Prirrerraaedga

F3=Exit  F6=Change =F 12=Previous

 

C1 Add the credit card code that will be used at Point of Sale, the name of the
card, and its receivables address.

1 If you're using journals, enter the journal ID.

C1 Use Y/N in the “EDC Capable?” and “Private Card?” fields (these prompts
are defined on the previous page).

O Repeat for as many credit cards as necessary.
O Press [Enter] to add cards to the Card List. A new blank list will be presented.
1 To return to the Card List screen, press F6=Change.

After credit cards have been set up, you’re ready to attach credit card information
to your customers’ master records in Receivables Maintenance (X11-2).


4 X52-14 « CREDIT CARD MAINTENANCE RELEASE 2.1
Te

Notes:

## CHAPTER X52-15

EDC CONFIGURATION

### Introduction

This option is used for the initial setup for FDR and the DataTran device,
including Merchant Ids, Promotion Codes, and Settle Times and for changes in
configuration, and manual command entry. Configuration has been done by DIS,
and, in most cases, it will not need to be changed. If you do need to change
settings or phone numbers, you will probably do so with the help of a customer
service representative. If you don’t have a DataTran device, you don’t need to be
concerned with this option.

### Contents

CONNECTING THE DATATRAN DEVICE TO THE AS/400
Type 6152.
Type 2609.

DATATRAN STALLATION INSTRUCTIONS

DETERMINE YOUR AS/400 OPERATING SYSTEM LEVEL.

INITIAL CONFIGURATION...
Sign on to the DIS Library as QSECOFR .
Determine the Resource Name ..............

AS/400 Operating System V3R2MO or Lower.
AS/400 Operating System V3R6MO or Higher
Create the DataTran Device.
Assign Divisions ..............
Enter Merchant IDs and Settle Times
Change Program Network Phone Numbers
ENTRANCE SCREEN..
Options..........
Function Keys

OPTION 2=CHANGE
Set Up DataTran Communication Parameter:
Select Media Types, Networks, and Capture Flags ..

Example 1 (Dumb terminal)
Example 2 (PC).....

   
  
 
  
   
 
  
 
 
  
   
 
 

 

 

wSoUNNOn Aw


2 X52-15 « EDC CONFIGURATION RELEASE 2.1

Program Network Terminal ID Fields 1 to 9.0.0.2...
Program Network Terminal ID Fields 10 to 18..
Program Network Terminal ID Fields 19 to 27..
Program Network Phone Numbers...
Example 1 (Dumb terminal) .
Example 2 (PC)... esses

List Installed Networks by Numeric ID.
OPTION 5=ASSIGNMENTS.
F6=CREATE wesc
F10=PROMOTION CODES.
Promotion Codes Screen........
Default Values .........cccce
Adding a New Promotion Code
F14=MERCHANT ID..
Merchant Id Screen...
DATATRAN ERROR RECOVERY ..
500-LEVEL ERROR MESSAGES..
CONSTANT ERROR CODE 997 OR 998
CONSTANT ERROR CODE 998
POWER LOSS OR -999...
How to Detect Error Mode ...
Resetting the DataTran Device.
PROBLEMS RESETTING OR VARYING ON THE DATATRAN DEVICE40
TIME-OUT ERRORS.
Checking the Configuration Status
Ending the DataTran Job ..


POINT OF SALE X52-15 « EDC CONFIGURATION 3

### Setting Up The Datatran Device

This section includes initial configuration, plus diagrams showing how to connect
the DataTran device. If your DataTran device is already connected, skip to the
entrance screen in this chapter on page 19.

CONNECTING THE DATATRAN DEVICE TO THE AS/400

The card positions on the back of an AS/400 are arranged in a 3x4 grid. Older
machines number the slots 1-4; newer machines number them 5-8.

 

 

DataTran devices may be attached in 2 ways:

1) Via a modem cable, which is attached directly into a slot (type 6152). See
page 4.

2) Via a box with 2 ports (type 2609), which is plugged into a slot on the
AS/400. See page 5.


X52-15 « EDC CONFIGURATION RELEASE 2.1

Type 6152
Method 1
Type 6152
Dataftran Attached Directly
1 2 3 4

5 6 7 8

 

 

Cc
5B |
Mark the card slot
where you attached the
B DataTran device on this
diagram.


POINT OF SALE X52-15 ¢ EDC CONFIGURATION

Type 2609

Method 2
Type 2609
Datatran Attached to Port 1 or 2

1 2 3 4
5 6 7 8

 

 

 

c
Mark the card slot and port
where you attached the
7B DataTran on this diagram.
B

 

 

 

 

 

 

Datatran

 


6 X52-15 « EDC CONFIGURATION RELEASE 2.1

DATATRAN 162 ND INSTALLATION INSTRUCTIONS

DATATRAN 162ND
INSTALLATION INSTRUCTIONS

Hardware List

a DataCap financial transaction processor with
integrated 2400 baud modem

Telephone cable

9-pin data cable

25-pin female to 9-pin male adaptor

a DataCap Qv power adaptor

In addition, you'll need a V.24 Communications Adapter Card,
which comes with an AS/400 data cable.

oao

 

Top rear view Back of
AS/400

 
 
  
  

Plug in power adaptor here
Plug other erid into wall outiet

    

 

   

To modem
or satellite

 
 

Ingert telephone cable here
Plug other end into telephone jack

    
   
      

v.24 ———»
Communications
Adapter Card in

Next availabie slo

1) Make connections shown in this diagram. Piug the
power adaptor into the electrical wall outlet last.

2) See Credit Card Guide to learn how to vary on the
DataTran line.

 
       
   
 
 
 
   
 

2-pin —»
data
cable

Never unplug the DataTran from the computer with
the power on. Do not place coffee cups, cash, or other
z objects on the DataTran unit.

   

Note: on some
AS/400s, slots
are on the left.

      
  
 
  
 

OM <=>25F
adaztor

 

 

Attach the other end
to the ¥24 Comm,
Adapter Card on the
AGI4Z00

DAIATRANIS.COR

WS


POINT OF SALE X52-15 « EDC CONFIGURATION 7

DETERMINE YOUR AS/400 OPERATING SYSTEM LEVEL

O Take a print key of any screen or menu.

Print Key Output Page 1

 

5763SS1| V3R2M0 |960517 s1011024 10/28/97 14:35:01

Display Device

 

 

On the second line, look for the version level. Keep the printout handy. You'll
need this for "Determine the Resource Name," which begins on page 8.

### Initial Configuration

A dedicated system is required for this step. The password for QS9ECOFR is
required.

Sign on to the DIS Library as QSECOFR

Sign off of the DIS Business System.

Sign on as QSECOFR.

Start the S/36 environment. At a command line, type: STRS36 [Enter]
Change to the DIS Library. At a command line, type: SLIB LIBRARY
[Enter].

Go to the Table Maintenance Menu by typing: MENU X52 [Enter].

Sign onto your data files. At a command line, type: ENV [Enter]. Furnish
your file set and division code.

oo oon00


8 X52-15 « EDC CONFIGURATION
Determine the Resource Name

This is a value you'll need to create the device in configuration. Before you start,
you need to know which slot (card position) on the AS/400 the DataTran has been
plugged into. Follow the instructions that correspond to your AS/400 operating
system level, which is on the print key you took (page 7).

AS/400 Operating System V3R2MO0 or Lower

O Atacommand line, type: DSPHDWRSC *CMN [Enter]. An example of the
Display Communication Resources screen is shown below. Your screen will

be different.

Type options, press Enter

Display Communication Resources

System: $1011024

S=Display configuration descriptions

Resource
CMBOL
LINOL
LINO12
ceo
LINOZ
LING21
eco3
LINOS
LINOS52

F3sExit F5=Refresh
F12=Cancel

Type
2615
6152
6152
2626
2626
2626
2623
6152
6152

Text

Combined function IOP
Com Adapter

V.24 Port Enhanced
comm Processor

LAN Adapter
Token-Ring Port

Comm Processor

Comm Adapter

‘V.24 Port Enhanced

Bottom

F6=Print Fll=Display resource addresses/statuses

 

O Find any V.24 ports listed under text and note their names.

O Press F11 twice.


POINT OF SALE X52-15 « EDC CONFIGURATION 9

Display Communication Resources
System: §1011024
Type options, press Enter.
S=Display configuration descriptions

Serial Frame EIA card
Resource Type Number ID Location Position
MBO 2615 10-4375047 ss 2
LINO1 6152 10-8905133 ss 23
LINC11 6152 10-8905133 ss 23
eco 2626 10-4381010 ss 4
LINO2 2626 10-4381020 ss 4
LINO21 2626 10-4381010 ss 4
cco3 2623 10-3164013. 8S 5
LINOS 6152 10-3157123 ss sc
LINO51 6152 10-3157123 ss sc

F3-Exit  F5=Refresh Fé=Print Fll=Display text F1Z=Cancel

 

O1 Look at the lines that correspond to the V.24 ports. Find the card position the
device is plugged into. In this example, the card is in position SC, and LINO51
is the resource name. Write the Resource name that corresponds to your
device here:: .


10 X52-15 ¢ EDC CONFIGURATION RELEASE 2.1

 

AS/400 Operating System V3R6MO or Higher

O Atacommand line, type: DSPHDWRSC *CMN [Enter]. An example of the
Work with Communication Resources screen is shown below. Your screen
will be different.

 

Work with Communication Resources
System: $100276G6
Type options, press Enter.
ScWork with configuration descriptions 7?=Display resource detail

Opt Resource Type Status Text
~  CMBOL 918B Operational Combined function IOP
- LINOL 2609 Operational Comm Adapter
7 CMNOL 2609 Operational v.24 Port Enhanced
7 CMNOZ 2609 Operational V.24 Port
_ LINO2 260% Operational Comm Adapter
7 Cuno 2609 Operational v.24 Port Bnhanced
7 CMNOd 2609 Operational V.24 Port Enhanced
Bottom
P3-Exit FS=sRefreshFé=Print F12=Cancel

 

1 Select each of the V.24 ports (CMNO1, CMNO2, etc.) with 7=Display
resource detail, and press [Enter]. The first Display Resource Detail screen

will appear.

Display Resource Detail (
system:  $100276G

 

Resource name CMNO4
Text... ee v.24 Port Enhanced
Type-Model 2609
Serial Number 10-4377044
Part Number cooog2iF4s67
Physical location:

Frame ID 1

Card position 4n +
Logical address:

SPD bus:

System bus 1

System board °

System card 8
Communications:

I/O bus 14

Adapter 0

More...
Press Enter to continue.

F3=Exit FS=Refresh Fé=Print F12=Cancel

 

 

 

©) Look for the card position. Press [Enter] to go to the next resource. When you
find the card position you're looking for, press [PgDn] to display the resource
name, as illustrated below.

LO


POINT OF SALE X52-15 « EDC CONFIGURATION 1

The AS/400
uses Ports 0
& 1, which

Display Resource Detail

cunod = <¢——_
v.24 Port Enhanced
2609

10-4377044
000002174867

Port ° ee

System: $1002766
Resource name

correspond
to P1 & P2
on the box

Serial Number
Part Number

   

O1 In this example, the card is in position 4A, and CMNO4 is the resource name.
Write the Resource name that corresponds to your device here:
O Write the Port number here:


X52-15 » EDC CONFIGURATION RELEASE 2.1

Create the DataTran Device

O From the Table Maintenance Menu (X5-2), select option 15, EDC
Configuration. The Configured DataTran Devices screen is displayed. Since
this is the first device, the screen will be empty.

 
      
   
    
    
 

Case Credit Configuration DSP9DFR
configured DataTran Devices

 

A-AKR CASE EQUIP

Name

 

2sChange 4=Delete 5=Assignments 7=Reset 9=Configuration Status

F3-Exit Fé=Create F10=Promotion Codes F12=Previous Fi4=Merchant ID
No data to display.

 
 

O Press F6=Create. The Configure DataTran Device screen is displayed.

  
 
   
    
  
   

 

A-A&R CASE EQUIP Configure DataTran Device

     

 

DataTran Name . . . | DPROL
DataTran Description . DataTran #1

< This is only an example.
Resource Name... . LINOS1 ¥ Pp

Use the resource name
you determined earlier.

 

Fi2=Previous

 

F3SBxit

  

O Enter the following values:
DataTran Name 5 characters. Enter a unique name for the device, such as
DTRO1.


POINT OF SALE X52-15 » EDC CONFIGURATION 13
ee OOO Eee revere

DataTran Description 25 characters.
Resource Name 10 characters. Enter the resource name for the port on the
AS/400 where the device is attached.

O Press [Enter]. If the device is created successfully, it will appear on the list of
configured devices.

Assign Divisions

O Start at the Configured DataTran Devices screen where the device you set up
is now listed.

A-A&R CASE EQUIP Case Credit Configuration DSP9DFR

Configured DataTran Devices
Name

2=Change 4=Delete 5=Assignments 7=Reset 9=Configuration Status

Opt Name Description Divisions Assigned?
5 DPRO1 DataTran #1

F3sExit F6=Create F10=Promotion Codes F12=Previous Fl4=Merchant ID
Datatran Device DTRO1 was configured successfully.

 

 

C Select the DataTran device with S=Assignments. The DataTran Assignment
screen is displayed, as illustrated below.


14 X52-15 « EDC CONFIGURATION RELEASE 2.1

 

Qo

       
  
  
  
      
 

Oo
o
o

F3-Exit 6=add = #12=Previous
No data to display.

A-A&R CASE EQUIP

F3=Exit F6=Change F12=Previous

A-AGR CASE EQUIP Case Credit Configuration DSQ8EFR C
DataTran Assignment

DataTran Name : DTROL

4=Delete

If there are no current assignments, press
F6=Add to assign divisions to this device.

To add a division, press Fo=Add. The following screen is displayed.

 

Case Credit Configuration DSQSEFR
DataTran Assignment

DateTran Name : DP?ROL (

Division Name

brrrrarrrrrda

 

Type the division codes that you want to assign to the device, which is named
at the top of the screen.

Press [Enter] to record the assignments and get another blank list. Add more
divisions, if necessary.

To return to the DataTran Assignment screen where the divisions will be
listed, press F6=Change.

To return to the Configured DataTran Devices list, press F12=Previous.


POINT OF SALE X52-15 « EDC CONFIGURATION 15
ae ee eeeeeeeeeeeEeeeeaes

Enter Merchant IDs and Settle Times
D From the Configured DataTran Devices screen, press Fl4=Merchant IDs.

Case Credit Configuration DSQ6DFR
Merchant ID

Division Name Merchant ID

A&R CASE EQUIPMENT SALES 504393000000034
DEALER SALES & SERVICE, LTD. 8B.
ABC COMPANY D.
EQUIPMENT RENTALS Ee
MOTORCYCLE CITY M
THERMOKING FE.

F12=Previous

 

O Enter the Merchant ID, which is assigned by FDR, to each division.

O Enter a Settle Time for each division that coincides with 6:00 P.M. Central.
Use military time. For example, If the dealership is on Eastern time, the local
settle time should be 7 P.M., which should be entered as 1900. The table
below lists the time zones and the corresponding military time that should be
entered for local settle times.

O Press [Enter] to record the information entered on this screen.

Settle Time (Milita

 
 
  

   
  

   
 

  

Time Zone Local Time

 
   
 

Hawaii
Alaska 3:00 P.M.

 
   
 

Pacific

[Pacific [16:00 CSC*dzd
Mountain 5:00 P.M.

    
 

      

Central 6:00 P.M.
Eastem 7:00 P.M.

     

 

[19:00
20:30

 

Atlantic
Newfoundland

 

 

   

O Sign off.

O Sign on again with your usual ID.

O Please refer to Chapters 1-3 for information about how to complete the setup
work and use credit cards at Point of Sale. In Chapter 4, you’ll find


16 X52-15 « EDC CONFIGURATION RELEASE 2.1

instructions for transmitting transactions that have been manually authorized
in case the FDR network is down or there is a problem with the DataTran
device. Refer to Appendix C for error recovery procedures.

For most dealers, this concludes the initial configuration. An additional step is
required if your telephone system requires you to dial one or more digits to get an
outside line, such as “9” or “O*,”

Change Program Network Phone Numbers
D Start at the Configured DataTran Devices screen.

 

A Case Credit Configuration DSP9DFR
Configured DataTran Devices
Name

 

2=Change 4=Delete S=Assignments 7=Reset 9=Configuration Status

Opt Name Description Divisions Assigned?
2  DTROL DataTran #1 Y

F3sExit  F6=Create Fl0=Promotion Codes Fl2=Previous Fid=Merchant ID

 

O Select the device with 2=Change. The DataTran Command Configuration
screen is displayed.

~~


» EDC CONFIGURATION 17

Ay DataTran Command Configuration DSQEDFR
DataTran Name DTRO1 DataTran #1

Network . . 004

2=Change

Opt Configurations

— Set Up DataTran Communication Parameters
Select Media Types, Networks, and Capture Flags
Program Network Terminal ID Fields 1 to 9
Program Network Terminal ID Fields 10 to 18
Program Network Terminal ID Fields 19 to 27
Program Network Phone Numbers
List installed Networks by Numeric ID

F3sExit  F12=Previous

 

O1 Select Program Network Phone Numbers with 2=Change. You will be
prompted for a password.

DataTran Command Configuration DTRCHGRP
Program Network Phone Numbers AT&UPE

Type choices, press Enter.

Network . 2...

Main Phone Number

Main Access Metho : Enter Password

Alternate Phone N :

Alternate Access

F3=Exit F12=Previous

 

O Type the password, which is 11111111. Do not press [Enter]. The next
screen is displayed automatically as soon as the complete password is entered.
If you return to the menu, it’s because you pressed [Enter]. (I got caught, too!)


18 X52-15 « EDC CONFIGURATION RELEASE 2.1

DataTran Command Configuration DIRCHGRP
Program Network Phone Numbers AT&UPE

Type choices, press Enter.

Network
Main Phone Number . . . . 918002289074
Main Access Method... . N  F4 for options

Alternate Phone Number . . 912159973964

Alternate Access Method . N 4 for options

F12=Previous

 

O Add the digit required by your telephone system, usually “9,” as illustrated on
the screen above. Some systems may require also an asterisk (*).

O Press [Enter] to record your changes. You will return to the DataTran
Command Configuration screen.

O Repeat F3=Exit until you return to the Table Maintenance Menu.

Now you’re ready to go to work.


ENTRANCE SCREEN

### X52-15 « Edc Configuration 19

O From the Table Maintenance Menu (X5-2), select option 15, EDC
Configuration. The entrance screen lists configured DataTran devices, if any.
DataTran devices are not associated with any particular file set: any file set
can be configured to any device, and any number of devices can be created.

BDC Configuration DSPIDFR
Configured DataTran Devices

2=Change 4=Delete 5=-Assignments 7=Reset 9=Configuration Status

Opt Name Description
DTROL DataTran #1

Divisions Assigned?

F3sExit F6=Create F10=Promotion Codes Fl2=Previous F14=Merchant ID

 

1 Use the position prompt, Name, to search for the device you want.

Options
2=Change

4=Delete
5=Assignments

7=Reset

9=Configuration Status

Function Keys
F3=Exit

Changes settings for a configured DataTran device.
See page 20.

*IOSYSCFG authority required. Deletes the line,
controller, and device. Ends any job associated with
the DataTran device.

Assigns divisions to use the DataTran device. See
page 29.

Resets the DataTran device after a failure, varies the
line off and back on, ends and restarts the
command-server job. See DataTran Error Recovery
at the end of this chapter.

Displays the configuration status of the line,
controller, and device allocated. See DataTran Error
Recovery at the end of this chapter.

Exits to the Table Maintenance Menu.


20 X52-15 ¢ EDC CONFIGURATION RELEASE 2.1
—— OI AE

F6=Create *IOSYSCFG authority required. Sign on as
QSECOFR. Initial configuration for a DataTran
device. See page 31.

F10=Promotion Codes Create and maintain promotion codes. See page 32.

F12=Previous Returns to the previous screen.

F14=Merchant ID Maintain merchant IDs for divisions. See page 34.
OPTION 2=CHANGE

O From the Configured DataTran Devices screen, select a device with
2=Change.

DataTran Command Configuration DSQEDFR
DataTran Name DTRO1 DataTran #1

Network. . 004

2=Change

Configurations

Set Up DataTran Communication Parameters

Select Media Types, Networks, and Capture Flags
Program Network Terminal ID Fields 1 to 9
Program Network Terminal ID Fields 10 to 18
Program Network Terminal ID Fields 19 to 27
Program Network Phone Numbers

List installed Networks by Numeric ID

F3=Exit F12=Previous

 

1 To change the description of this device, type over the current description.
C1 If you are unsure of the Network, select List installed Networks by Numeric
ID, which appears at the bottom of the list.
0 To change one of the configuration settings, select it with 2=Change. Each
screen is illustrated on the following pages. Briefly, the options are:
1, Set Up DataTran Communication Parameters
Change dial mode, maximum attempt count, modem reset flag, and carrier
connect time. See page 21.
2. Select Media Types, Networks, and Capture Flags
Enable/disable capture of different media types, such as Activate EDC
Network, Checks, American Express, Visa, etc. See page 22.


POINT OF SALE X52-15 e EDC CONFIGURATION 21

3. Program Network Terminal ID Fields 1 to 9
Network number required. Change terminal ID fields unique to the each
network. FDR uses only fields 1 to 9. See page 24.

4, Program Network Terminal ID Fields 10 to 18
Network number required. Change terminal ID fields unique to the each
network. FDR uses only fields 1 to 9. See page 25.

5. Program Network Terminal ID Fields 19 to 27
Network number required. Change terminal ID fields unique to the each
network. FDR uses only fields 1 to 9. See page 25.

6. Program Network Phone Numbers
Change main and alternate phone numbers and access techniques. See
page 26.

7. List installed Networks by Numeric ID
Display installed networks and their IDs, statuses, and numeric IDs. See
page 29.

Set Up DataTran Communication Parameters

DataTran Command Configuration DTRCHSRP
Set Up DataTran Communication Parameters AT&UP2

Type choices, press Enter.

Dial Mode P=Pulse T=Tone

Maximum Attempt Count . 1 to 2 recommended

Hodem Reset Flag .. . O=Reset the modem after failed communication
1sNever reset the modem
2=Reset the modem before each use

Carrier Connect Time . 035 20 te 40 seconds recommended

F3=Exit  F12=Previous

 

O1 Change the settings as necessary.

O Press [Enter] to record your changes and return to the DataTran Command
Configuration screen.

O To return to the DataTran Command Configuration screen without making
any changes, press F3=Exit or F12=Previous.


22 X52-15 » EDC CONFIGURATION RELEASE 2.1
See EE EEE ee ASE

Select Media Types, Networks, and Capture Flags

DataTran Command Configuration DTRCHGRP
Select Media Types, Networks, and Capture Flags ATKUP2

Type choices, press Enter.

Media Type

Network
Activate EDC Network
Checks
American Express
Visa
MasterCard
Discover
Other charge cards
Diner's/Carte Blanche
JCB

F12=Previous

F3=Exit F12=Previous

 

The following media types are required:
Y Activate EDC Network .
Y Other charge cards (

The appearance of the Select Media Type window will depend on your
workstation.

Example 1 (Dumb terminal)

Select Media Type
i. Activate EDC Network
2. Checks
3. American Express
4. Visa
5. MasterCard
6. Discover
7. Other charge cards
8. Diner'’s/Carte Blanche
9. JCB

F12=Previous

O For this type of window, type the option number of the media type and press
[Enter]. The input field for all options is immediately to the left of option 1.


POINT OF SALE X52-15 e EDC CONFIGURATION 23

Example 2 (PC)

  

Fa2=Previous

 

O For this type of window, do one of the following:
— Type the underlined letter for the media type, such as “x” for American
Express, or
— Use the mouse and click the appropriate button, or
— Use the arrow keys to highlight the media type, and press the space bar.
Ci Select Activate EDC Network. When you have made your choice according to
Example | or 2, the following screen is displayed:

DataTran Command Configuration DPRCHGRP
Select Media Types, Networks, and Capture Flags AT&UP2

Type choices, press Enter.

Other charge cards

Network

Capture Flag . . Enable authorization only
Enable draft capture

P3=Exit F12=Previous

 

v The Capture Flag is basically an on/off switch. When it is on (1), it enables
the DataTran device to dial out and have the network “capture” a transaction.
The device allows captures for every media type where Capture Flag is set to
“1.” The Capture Flag be set to “1” for both “Activate EDC Network” and


24 X52-15 « EDC CONFIGURATION
“Other charge cards.” For media types with Capture Flag set to 0 (zero), you
must manually dial for authorization of each transaction.

ooo

Program Network Terminal ID Fields 1 to 9

FDR uses fields 1 to 9 only.

To enable the capture of this media type, change the Capture Flag to 1.
Press [Enter] to record your change.
Repeat this process to select “Other charge cards.”

DataTran Command Configuration DIRCHGRP
Program Network Terminal ID Fields 1 to 9 AT&UP3

‘Type choices, press Enter.

Network . . 004

- NOTE - Check
the layout for
the network
carefully before
changing any
settings.
Incorrect data
length will cause
data loss in some
fields.

F3sExit F12=Previous

Terminal
Terminal
Terminal
Terminal
Terminal
Terminal
Terminal
Terminal

Terminal

RX.

504393000000034.
000,
001,
601,
001,

020,

 

co


POINT OF SALE X52-15 e EDC CONFIGURATION 25

Program Network Terminal ID Fields 10 to 18

FDR does not use fields 10 to 18; therefore, the following screen is displayed
when this option is selected,

DataTran Command Configuration DTRCHGRP
Program Network Terminal ID Fields 10 to 18 ATEUDS

Type choices, press Enter.

Network . . Terminal ID Field

Terminal ID Field
- NOTE - Check

Incorrect data
length will cause = Terminal ID Field
data loss in some .
fields. Terminal ID Field . .

 

Terminal ID Field

Terminal ID Field

F3=Exit F12=Previous

 

Program Network Terminal ID Fields 19 to 27

FDR does not use fields 19 to 27; therefore, the following screen is displayed
when this option is selected.

 

DataTran Command Configuration DTRCHGRP
Program Network Terminal ID Fields 19 to 27 AT&UPS

Type choices, press Enter
Network . . Terminal ID Field

Terminal ID Field
- NOTE - Check

Incorrect data

length will cause Terminal ID Field
data loss in some

fields. Terminal ID Field

Terminal ID Field

Terminal ID Field

F3=Exit F12=Previous


26 X52-15 e EDC CONFIGURATION RELEASE 2.1

 

Program Network Phone Numbers

To change network telephone numbers and access methods, a password is
required,

DataTran Command Configuration DTRCHGRP
Program Network Phone Numbers ATaUPS

Type choices, press Enter.

Network 2... 1 1 1 000
Main Phone Number
Main Access Metho

Alternate Phone N

 

Alternate Access

F3sExit F12=Previous

 

O Type the password, which is 11111111. Do not press [Enter]. The next screen
is displayed automatically as soon as the complete password is entered.

DataTran Command Configuration DTRCHGRP
Program Network Phone Numbers AT&UP6

Type choices, press Enter.

Network 2... 2... . 004

Main Phone Number . . . . 9*18002289074
Main Access Method . . . . N Fd for options
Altexnate Phone Number . . 9*12159973964
Alternate Access Method N Fda for options

F3=Exit F12=Previous

### Point Of Sale X52-15 » Edc Configuration 27

O To select from a list of valid access methods, press [Tab] to reach the “Main
Access Method” field, and press F4=Prompt. The appearance of the Select
Access Method window will depend on your workstation.

Example 1 (Dumb terminal)

 

elect Access
. Canadian Datapac - dial access

. DDOV

- ISDN

. Leased line access

. Normal dial-up access

. Canadian Datapac - dedicated access
- Telenet access

   

lw

AAR wNHE

F12=Previous

O Por this type of window, type the option number of the access method and
press [Enter]. The input field for all options is immediately to the left of
option 1.

Example 2 (PC)

Select Access Method

   
 

F42=Previ ous

 

O For this type of window, do one of the following:
— Type the underlined letter for the access method, such as “n’” for Normal
dial-up access, or
— Use the mouse and click the appropriate button, or
— Use the arrow keys to highlight the media type, and press the space bar.


28 EDC CONFIGURATION RELEASE 2.1

 

DataTran Command Configuration DTRCHGRP (
Program Network Phone Numbers ATRUPE

Type choices, press Enter.

Network 2... 01. » + 004
Main Phone Number . . . 9*12159973963
Main Access Method... . N F4 for options

Alternate Phone Number . . 9*8002289074

Alternate Access Method . N F4 for options

F3=Exit Fi2=Previous

 

The underlined jetter for the access method will be highlighted in the Main
Access Method field.


POINT OF SALE X52-15 « EDC CONFIGURATION 29

List Installed Networks by Numeric ID

Select this option to see the networks installed on the DataTran device, their
numeric codes, and statuses. This screen is display oniy—no input is allowed.

DataTran Command Configuration DTRCHGRP
Installed Networks

Network ID. . FDR CHK --- ---
Numeric Code . 004 005 000 000
Status . . . . ON OFF OFF OFF

Press ENTER to continue.

 

OPTION 5=ASSIGNMENTS

Use this option to assign divisions within the same file set to a DataTran device.
After divisions have been assigned, you'll see “Y” in the column labeled
“Divisions Assigned” in the list of configured devices. To assign divisions in a
different file set, exit and change to it with an “ENV” command.

O On the Configured DataTran Devices screen, select a DataTran device with
5=Assignments. The DataTran Assignment screen is displayed as illustrated


X52-15 s EDC CONFIGURATION

EDC Configuration
DataTran Assignment

DataTran Name :
4=Delete
Opt Division Name

- A A&R CASE EQUIPMENT SALES
- B DEALER SALES & SERVICE, LTD.

F3=Exit Fé=add F12=Previous

O To delete an assignment, select the division with 4=Delete.
DSQSEFR

 

O To add an assignment, press Fé=Add. The following screen is displayed.

EDC Configuration
Datafran Assignment

DataTran Name :

Division Name

FisExit Fé=Change F12=Previous

at the top of the screen.
divisions, if necessary.

listed, press Fé=Change.

oOo a0

### Dsqbefr

 

Type the division codes that you want to assign to the device, which is named
Press [Enter] to record the assignments and get another blank list. Add more
To return to the DataTran Assignment screen where the divisions will be

To return to the Configured DataTran Devices list, press Fl12=Previous.

io


POINT OF SALE X52-15 « EDC CONFIGURATION 31
——_ §§ - ue rr eeeeeeeeeeeeese_eeeea

O To return to the Table Maintenance Menu, press F3=Exit.
F6=CREATE

*IOSYSCFG authority is required to create a new DataTran device.

O To create a new DataTran device on the system, press Fé=Create from the
Configured DataTran devices screen.

  
  
 
   
  
  

Configure DataTran Device DSQAPVR

DataTran Name .
DataTran Description .

Resource Name

  
 

F3sExit F12=Previous

 

 

O Enter the following values:

DataTran Name 5 characters. Enter a unique name for the device.
DataTran Description 25 characters.
Resource Name 10 characters. Enter the resource name for the port on the

AS/400 where the device is attached.

O) Press [Enter]. If the device is created successfully, it will appear on the list of
configured devices.

How to determine the resource name

O At acommand line, type: DSPHDWRSC *CMN [Enter].

O Find any V.24 ports listed under text and note their names.

O Press F11 twice.

C1 Find the card position the device is plugged into. This is the resource name.


32 X52-15 « EDC CONFIGURATION RELEASE 2.1

 

F10=PROMOTION CODES

Promotion Codes Screen

To add or change a promotion code, or to mark one of the codes as the default,
press F10-Promotion Codes from the Merchant Id Screen.

EDC Configuration DSOLEFR
Fromotion Codes

isMark/Unmark as default 4=Delete

Code Description
0010 Open Account Transfer

6060 €0 days no interest, no payment
0080 90 days no interest, no payment
0120 120 days no interest, no payment
6150 150 days no interest, no payment
0180 180 days no interest, no payment
@210 210 days no interest, no payment
0240 240 days no interest, no payment
0270 270 days no interest, no payment
9999 Regular Purchases

F3sExit F6=Add f12=Previous Fl4=Default values

 

O To mark a code as the default to be used on the Credit Authorization screen at
Point of Sale Invoicing, select it with ]=Mark/Unmark as defauit.

O To delete a code, select it with 4=Delete.

O To change one of the current codes, type over the existing information.

Default Values

Default values refer only to codes and their descriptions that are supplied by the

system, which are illustrated on the screen above. If you have deleted or changed

system codes, they will be restored. Codes that you add will not be lost.

© To restore default codes and descriptions supplied by the system, press
F14=Default Values.


POINT OF SALE X52-15 « EDC CONFIGURATION 33

Adding a New Promotion Code
O To add new promotion codes, press Fé=Add. A blank list for new codes is
presented, as illustrated below.

EDC Configuration DSOLEFR
Promotion Codes

o
a

Description

F3=Exit Fé=Change F12=Previous Fi4=Default Values

 

O Type one or more codes and their descriptions.

D Press [Enter] to add them to the list of promotion codes.
OD To retur to the list of codes, press Fé=Change.


34 X52-15 « EDC CONFIGURATION RELEASE 2.1
Oe eee eNOS

F14=MERCHANT ID

Merchant Id Screen

EDC Configuration DSQ6DFR
Merchant ID

Division Name Merchant ID

A&R CASE EQUIPMENT SALES 504393000000034
DEALER SALES & SERVICE, LTD.

ABC COMPANY

EQUIPMENT RENTALS

MOTORCYCLE CITY

THERMOKING

FlZ=Previous

 

0 Enter the Merchant ID, which is assigned by FDR to each division.

O Enter a Settle Time for each division that coincides with 6:00 P.M. Central.
Use military time. For example, If the dealership is on Eastern time, the local
settle time should be 7 P.M., which should be entered as 1900. The table
below lists the time zones and the corresponding military time that should be
entered for local settle times.

0) Press [Enter] to record the information entered on this screen.

15:00

      
  
 
 
 

 
 
     
  
    
 
  

20:00
20:30


X52-15 « EDC CONFIGURATION 35

### Datatran Error Recovery

In this section you’ll find error recovery procedures for the DataTran device and
program.

### 500-Level Error Messages

The following error messages are generated by the network (FDR) when
transactions cannot be approved. Sometimes the message will indicate a solution;
however, if it fails, you can do the following:


Call FDR to determine a solution

Try a different credit card

Press F12=Previous to return to the detail screen, then [F7] to return to the
Sold To screen where you can remove the credit card code and proceed with a
cash or regular charge sale.

The transaction was not approved by the network. This message is
variable and may suggest solutions. If the error persists, contact the
network to determine a solution.

The transaction was not approved by the network due to problems at
the network. This message is variable and may suggest solutions. Try
again. If the error persists, contact the network for assistance.

The transaction contains erroneous data, and was not approved by
the network. This message is variable and may suggest solutions. Try
again. If the error persists, contact the network for assistance.

The transaction was not approved by the network because of a
possible duplication. Verify that the transaction was not duplicated. Try
again. If possible, bypass the error message. If the error persists, contact
the network for assistance.

The transaction was not approved by the network. This message is
variable and may suggest a solution. If the error persists, contact the
network for assistance.


36 X52-15 e EDC CONFIGURATION RELEASE 2.1
SS SE ET

### Constant Error Code 997 Or 998 -

Check data area DTRnnnnnDA (where nnnnn=name assigned to the device) for
an object lock using the command WRKOBJLCK OBJ (DTRnnnnnDA)
OBJTYPE (*DTAARA). A lock on this data area is normal during communication
for an authorization, which lasts about 25 seconds.

If something went wrong with the DataTran, or if the user ended a communication
improperly (for example, doing a System Request and taking a “2” during
communication), the data area may become locked by a display job. If any locks
on this display don’t go away after 25 seconds (press F5=Refresh), have the user
sign off from the locked terminal and check the object locks again. Once the lock
is gone, check the configuration status and make sure the DataTran is
communicating (using the terminal program).

It is important that users understand that when there is a problem with
communication and their terminal locks up during a transmission, they must wait
for the program to time out, which takes up to 3 minutes. If they don’t the lock
condition described above can occur.

CONSTANT ERROR CODE 998 : {

Error code 998: A timeout occurred. Check DataTran configuration status.

At acommand line, type: WRKACTJOB [Enter]. Look for a job that begins
“DISD” followed by the name of the DataTran device, such as DT1 in the
example below:

Opt Subsystem/Job User Type CPU % Function Status

DISDDT1 gsys SBS 0 DEQW
_— DISDDTi DUANEP BCH -Q  PGM-DATRANCL DEQW

 

O Check the Status column for MSGW (Message Waiting).
O1 To display the message, select the job with 7=Display message and take
appropriate action.


POINT OF SALE X52-15 » EDC CONFIGURATION 37

### Power Loss Or -999

Error code 999: An error has occurred with the DataTran device and it must
be reset.

If the DataTran device has a power loss or one of the cables is disconnected, the
DataTran command job will go into error mode.

How to Detect Error Mode

¢ Iflogging was turned on, display the log file. The last few lines will show that
the DataTran program ended due to a communication error. The last entry on
the log file should say “Shutting down due to communication error.”

- If logging was not turned on, take the option to start the DataTran terminal
program. Issue a command, such as AT&UT99. If the response is *ER, the
program is in error mode.

¢ If you receive an error message, “An error has occurred with the DataTran
device and it must be reset. - 999” while a batch is being closed or during an
authorization, the program is in error mode.

O To confirm that the program is in error mode, go to EDC Configuration (X52-
15) where DataTran devices are listed.

AsABR CASE EQUIP EDC Configuration DSPSDFR
Configured DataTran Devices

Name

2=Change 4=Delete S=Assignments 7=Reset 9=Configuration Status

Opt Name Description Divisions Assigned?
DTRO1 DataTran #1 ¥

F3=Exit  F6=Create Fi0=Promotion Codes Fi2=Previous F14=Merchant ID

 

1 Select the device with 9=Configuration Status. The Work with Configuration
Status screen showing the DataTran device will be displayed.


38 X52-15 * EDG CONFIGURATION RELEASE 2.1
SE

Work with Configuration Status s1021024
05/19/97 14:06:15
Position to ..... Starting characters

Type options, press Enter
isVary on 2=Vary off SsWork with job 8sWork with description
9=Display mode status ...

Opt Description Status
DISDDTROLL ACTIVE
DISDDTROIC ACTIVE
DISDDTROiID = ACTIVE DISDDTROl ALANB 199466

 

This job will not be here.

Bottom

Parameters or command

F3sExit Fd=Prompt F12=Cancel F23=More options F24=More keys

 

When the DataTran program is in error mode, the DataTran job, DISDn (n=name
of DataTran device, such as DTRO1) will not show up on the configuration status
screen because the device will not be acquired by the ICF file.


POINT OF SALE X52-15 e EDC CONFIGURATION


 

Resetting the DataTran Device

If the DataTran job is missing, follow these steps to recover:

O Restore power to the device or re-connect its cable.

O From the Table Maintenance Menu (X5-2), select option 15, EDC
Configuration. The list of configured DataTran devices is displayed.

A-A&R CASE EQUIP EDC Configuration DSP9DER
Configured DataTran Devices
Name

2=Change 4=Delete S=Assignments 7=Reset 9%=Configuration Status

Opt Name Description Divisions Assigned?
7 DTROL DataTran #1 Y

F3sExit Fé=Create Fi=Promotion Codes Fl2=Previous F14=Merchant ID

 

 

O Select the device with 7=Reset. Look for the message, “Reset was successful”

at the bottom of the screen.


40 X52-15 « EDC CONFIGURATION RELEASE 2.1

PROBLEMS RESETTING OR VARYING ON THE DATATRAN DEVICE

O Make sure the DataTran is powered on (red light).

C Vary the device off from the configuration status display.
1 Vary the device back on.

If the line, controller and device do not all go active:
O Turn the DataTran device off and back on.
O Vary the device off and back on.

If the line, controller, and device go active:
C1 Reset the device (option 7, EDC Configuration).
O Test communications with the device from the terminal program.


POINT OF SALE X52-15 «e EDC CONFIGURATION 41

### Time-Out Errors

Tf you receive time-out errors while trying to get an authorization or close a batch,
the DataTran program may have failed.

Checking the Configuration Status

O To confirm that the program failed, go to EDC Configuration (X52-15) where
DataTran devices are listed.

A-AK&R CASE EQUIP EDC Configuration DSPSDFR
Configured DataTran Devices
Name

 

2=Change 4=Delete 5=Assignments 7=Reset 9=Configuration Status

Opt Name Description Divisions Assigned?
9  DTRO1 DataTran #1 x

P3=Exit F6=Create F10=Promotion Codes F12=Previous Fi4=Merchant ID

 

O) Select the device with 9=Configuration Status. The Work with Configuration
Status screen showing the DataTran device will be displayed.


42 X52-15 « EDC CONFIGURATION RELEASE 2.1
a eeeeeeeeeeeeSSSFSFSFSFSFSST ASE ET

 

Work with Configuration status §1011024 C
05/19/97 14:00:15
Position to Starting characters

Type options, press Enter.
l=Vary on 2=Vary off S-Work with job  8=Work with description
S=Display mode status ...

Opt Description Status

DISDDTRO1L ACTIVE

DISDDTRO1C ACTIVE
DISDDTROID = ACTIVE 199466

Bottom
Parameters or command
Bee>

F3-Exit F4sPrompt Fl2=Cancel F23=More options F24=More keys

 

If you see the DataTran job, DISDn (n=name of DataTran device, such as
DTRO1), it is likely that the program failed.

Ending the DataTran Job

If the DataTran job is present, follow these steps to recover: {

O Make sure everyone is out of Point of Sale (X5-1).

O Make sure no one is using Transmit Credit Card Transactions (X55-4).

O Atacommand line, type: WRKACTJOB [Enter].

O Look under “Function” and make sure there are no X51* programs running,
such as PGM-X51001. If you find one, locate the user and sign the program
off at the workstation. Do not end this job manually.

O Look under “Function” and make sure there are no X71* programs running,
such as PGM-X71F00CL. If you find one, locate the user and sign the
program off at the workstation. Do not end this job manually.

1 When you are sure the X51* and X71* jobs have ended, look for a job that
begins “DISD” followed by the name of the DataTran device, such as DT] in
the example below:

Opt Subsystem/Job user Type CPU % Function Status

DISDDT1 gsys SBS 0 DEQW
a DISDDT1 DUANEP BCH -0  PGM-DATRANCL DEQH

 

Q End the DataTran background job by selecting it with 4=End, as illustrated.
O Press F5=Refresh until you see that it is ended. The background job will
testart as soon as someone goes into Point of Sale.

## CHAPTER X52.13-1

CASH DRAWER CONFIGURATION

### Introduction

Cash drawers are configured as printers on the $/36 and AS/400. Use this
Job to identify the corresponding printer IDs. If two or more drawers are
cabled in series from the same PC, they share the same printer ID. The
drawers operate independently even in series.

### How To Run

From the Cash Tendering Menu (X52-13), select option 1, Cash Drawer
Configuration.

PACIFIC EQUIPMENT CASH DRAWER CONFIGURATION XS52D1-101 1
Division: *

Enter the printer id to which each of
your cash drawers are assigned.

Drawer A. |.
Drawer B. .
Drawer ¢ . |.
Drawer D
Drawer EB. .
Drawer F .
Drawer GG...
Drawer B . ,

## X52.13-1 CASH DRAWER CONFIGURATION

 

(0 Enter printer IDs for all cash drawers.

 

Press [Cmd1] to end the job and return to the Cash Tendering Menu.

 

 

 

RELEASE 2.1 Co

## CHAPTER X52.13-2

CASH DRAWER SECURITY

### Introduction

Full security is available when there is more than 1 cash drawer. Use this
job to enter security codes for 1-8 cash drawers.

Note:
No security code is necessary for a single cash drawer.

## X52.13-2 CASH DRAWER SECURITY

 

### How To Run

From the Cash Tendering Menu (X52-13), select option 2, Cash Drawer
Security. First, you are prompted for the code, which may be up to 8
characters. Press [Enter] to display the full screen, as illustrated below:

PACIFIC EQUIPMENT CASH DRAWER SECURITY x5202-102 2
Division: *

Code: CASH

Cash Drawer Id (A - H): A

Code Description: GENERAL

Enter '¥' To Delete

Cm@i-End job  Cmd3-Return

O Furnish the Cash Drawer Id and a description of the code (up to 8
characters, and press [Enter]. Repeat for all cash drawers.

 

 

 

 

To remove a code, enter "Y“ at the prompt in the bottom right corner of
the screen.
Lo


 

O To return to the prompt, press Cmd3-Return

0) To end the job, press Cmd1-End.


Notes:

RELEASE 2.1 LL

## CHAPTER X52.13-3

CASH TENDERING SALES CODE MAINTENANCE

### Introduction

Use this job to list sales codes that will cause the Cash Tendering screen to
be displayed at Point of Sale. The screen will be displayed for both cash
and charge sales when one of these sales codes appears on the document.
‘You may enter up to 30 sales codes for each division.

### How To Run

From the Cash Tendering Menu (X52-13), select option 3, Cash Tendering
Sales Code Maintenance.

PACIFIC EQUIPMENT CASH TENDERING XS203-102 1
Division: A Sales Code Maintenance

Cash tendering sales codes on charge documents:

3. a. 6.

22. 13. ia, 35.

21. 22. 23. 24.

## X52.13-3 CASH TENDERING SALES CODE MAINTENANCE

 

O Enter the sales codes that will trigger the Cash Tendering screen and
press [Enter].

 

To remove a sales code, simply [Field Exit] through it.

 

O To end the job, press Cmd1-End job.

 

 

 

Repeat for each division.

 

RELEASE 2.1 Ko

## CHAPTER X52.13-4

OPEN CASH DRAWER

### Introduction

Use this job to open a cash drawer. Another way to do the same thing is to
type "OPEN" at any menu and press [Enter]. In both cases, you are
prompted for a security code if there is more than 1 cash drawer.

Note:

Typing OPEN password at a menu eliminates the security screen. For
password, use your own security code.

## X52.13-4 OPEN CASH DRAWER

 

### How To Run

From the Cash Tendering Menu (X52-13), select option 4, Open Cash
Drawer,

OPEN CASH DRAWER X52D4-201

Enter-Open drawer Cmdi-End job

 

 

 

Type the security code. It is not displayed on the screen.

OO Press [Enter] to open the drawer.

 

 

 

 

To end the job, press Cmd1-End job.

RELEASE 2.1 LO

## CHAPTER X55-1

CREATE POINT OF SALE POSTING BATCH

### Introduction

When an invoice is created at point of sale, accounting transactions are
captured. The next step is to create a batch from all the invoices. Before a
batch can be posted, it must be created.

### How To Run

From the Point of Sale Posting Menu, select option 1. Press [Enter]. After
proceeding through the security gate, you will see a screen requesting the
transaction date and the general ledger month for posting the batch.
Today's date and the current month will be the defaults. You may change
the date and month for posting. Press [Enter].

A screen displays requesting verification of the information just entered. If
the posting date and month are correct, press Enter. If not, Cmd3 back a
screen and make any changes you want. When the date and month are
correct, press [Enter]. If you went back to change the date or month, press
[Enter] twice.

The Point of Sale Posting Create Posting Batch screen appears.

## X55-1 CREATE POINT OF SALE POSTING BATCH

### Lee'S Rental Company 5510-102

This procedure creates a posting batch from closed Point of Sale
documents. You may elect to post all closed documents or those of
specified types or a single document.

Post all closed decuments:
Post all closed documents with the following decument type(s) :
To post enly one closed document, enter the document number and
either the customer address or stock number

Document number:

Customer address; Or Stock number:

Post all closed purchase orders Y/N : N
Post all closed purchase orders within date range 090196 to 100196
To post only one closed purchase order, enter the purchase order number (
and the vendor address number

Purchase order:

 

Vendor address:

Fi=Cancel

 

© Decide which POS documents will be posted and make your selection
in the Enter document selection field. To post an individual document,
specify the document number and the customer address.

By default, all closed purchase orders within the current month will
also be posted. To post only one purchase order, specify it and its
vendor address in the fields at the bottom of the screen.

Press [Enter] and the following screen appears.

RELEASE 2.2 Lo


X55-1 CREATE POINT OF SALE POSTING BATCH [=]

LEE'$ RENTAL COMPANY TIME DELAY X0008-201 1
Create ».0.$. Batch

Time to start job

mdi-cancel Cmd9-No Delay

 

O Enter the time when the posting batch will be created in the form of
HHMM. Press [Cmd9] to begin creating this batch immediately.

Generally, you will want to post all closed documents. This is the default.
If you want to post all closed documents, press [Enter]. The batch takes a
few minutes to create and you choose to have it made at any time. The
following message will be sent to your work station when it is created:

Point of Sale Posting batch is created for div a@ (d= the
division you created the batch for)

There may be an occasion when you will want to post only one document.

### [+] X55-1 Create Point Of Sale Posting Batch

For example, suppose you have a large work order on a piece of your
equipment which should have been closed and expensed last month.
Somehow it was overlooked and you don't want to recognize that large of
an expense this month.

If the month is still open, you can post the work order into last month.
Make sure the posting date and month are the ones you want. In the Post
all closed documents field, enter V. Type the work order number in the
Document number field. Type the stock number in the Stock number field.
Let's look at one more example. Suppose you sold a piece of equipment
and took in a trade on the same invoice. Then you sold the trade in the
same day to someone else. If a batch is created with both invoices, an error
will occur. You can't post both sale and cost transactions for the same
stock number in the same batch. First post the

invoice for the trade in, then post the invoice with the sale transaction in (
the regular batch.

Type N in the "Post all closed documents" field. Type the invoice number
in the document number field and the customer address number in the
Customer address field. Press [Enter].

It takes a few minutes to create a batch. You may proceed with other work.
A message is sent to your workstation when the batch is ready.

RELEASE 2.2 Lo


X55-1 CREATE POINT OF SALE POSTING BATCH [=]

P.O.S. POSTING SUMMARY REPORTS

While the batch is being created, 3 P.O.S. Posting Summary Reports will
print.

1. VOIDED DOCUMENTS: This report shows the documents that were
voided, who the salesperson was, who the customer was, the void date,
void time, and the total amount of the invoice.

All point of sale documents that were voided will show up on this
report. These are lost sales. This report may be helpful in determining
why certain sales were lost.

If Cmd10 is pressed to void a closed document, then the document will
not show up on this report. This type of document is called a
"cancelled" document.

IF A DOCUMENT IS VOIDED WHILE OPEN, THIS IS THE ONLY
AUDIT TRAIL OF THE NUMBER YOU WILL HAVE. BE SURE YOU
KEEP IT.

2. PARTS SOLD WITH ZERO COST: This report will list any parts that
were sold at point of sale and have zero cost in the part file. The report
lists the sales price. You will have to look up the cost of the part and
enter the cost in Parts Posting and Maintenance (X32).

If the parts sales account has a "D” edit code and a factor is applied in
X14-2 General Ledger Maintenance, percentage costing is applied. The
factor is multiplied by the sale. The result is credited to inventory and
debited to cost of sales.

If the parts sales account does not have a "D" edit code or factor, you


Le] X55-1 CREATE POINT OF SALE POSTING BATCH

will have to correct the general ledger. To correct the general ledger, go
to Create Source Documents (X17) and make an adjustment to
inventory and cost of sales. The parts were sold at 100% profit unless
the adjustment is made.

3. PARTS COSTING SUMMARY: This report will list all the
documents that were created at point of sale. It will show the customer
and who made the sale. It breaks down the parts sales into gross sales
price, cost of the part, discount given to the customer, the percentage of
discount, gross profit in dollars, and the percent of profit margin. The
report is divided by Document Number. This report sorts on the first
two characters of the numbering sequence for documents chosen in
Document Classification Maintenance (X52- 2).

The gross sales price of non-part sales, such as labor or miscellaneous (
parts, and final totals are listed on the report at the end of each
document section.

The following legend in the Parts Costing Summary explains which sales
code formats are included in the part sales and non-part sales totals.

Note: The Part Sales total includes all lines with formats P
and M. The Non-Part Sales total includes all lines with
formats D and L. Lines with formats S and T are included in
the Part Sales total if the credit general ledger account of
the line has a D edit code, otherwise they are included in
the Non-part Sales total.

This feature concerns the factox that is used to cost parts that have been
split out of a customer document as internal or warranty lines; in
particular, it involves sales codes of the following formats:

D Miscellaneous description

L Labor

M Miscellaneous quantity

RELEASE 2.2 A.


X55-1 CREATE POINT OF SALE POSTING BATCH | 7 |

S Miscellaneous cost
T Cost miscellaneous quantity

Unless the document is opened to a unit, when the system encounters an
internal or warranty line, the program will use the factor from the general
ledger account on the internal or warranty line for the sales code. Refer to
the Sales Code Maintenance screen (X52-3), which is illustrated below.
Customer lines will use the factor associated with C5459, internal lines
will use the factor associated with G/L account C5710, and warranty lines
will use the factor associated with C5460.

ANW EQUIPMENT SALES

Sales Code PM

Description
Format

Customer Document
nternal Document
Warranty Document

Override Tax Code
Override Discount
vendor for Parts

Cmd2-End job Crrd3~Go back

PARTS

Code

SALES CODE MAINTENANCE

- MISC
‘be

Labor
Misc.
Mise.
Misc.
Notes

eredic

$459
5710
5460

Description
quantity
Units

(optional?

5230-101

Current Sales Code
Parts

Prepayments
Received on Account
Unit Sales

Misc. Cost

Cost Misc oty

‘wild Card’ account #'s:
*aUTO © - any format
*SALE 0 = 'P' or 'W!

format only
*ERROR - any format

Crdl9-pelere this sales code


 

### Posting The Batch

When the batch is created, the following message is sent to the work

Station: Point of Sale Posting batch is created for div 4
(d = the division you created the batch for)

From the Point of Sale Posting Menu, select option 2, Review and Post
Point of Sale Documents.

If you select option 1 to create the batch again for the same division, the
following screen displays.

Point of Sale Posting 5510-003
Create Posting Batch

A Point of Sale posting batch for this division is ready to be posted. Complete.

this batch by taking the second option on this menu before
creating another batch.

Please press enter.

 

Press [Enter] to return to the Point of Sale Posting Menu for the correct
selection, Review and Post Point of Sale Documents (X55-2).

‘
RELEASE 2.2 XL

## CHAPTER X55-2

REVIEW AND POST POINT OF SALE DOCUMENTS

### Introduction

A batch is created from all closed Point of Sale documents. First the batch
must be created. After the batch is created, it can then be posted.

### How To Post A Batch

From the Point of Sale Posting Menu, select option 2. Press Enter. After
the security gate, the Post Source Documents Check for Errors screen
displays.

For information on editing and posting a batch, see Chapter X1-7, Create
Source Documents.


Notes:

f
RELEASE 2.1 KL

## CHAPTER X55-3

PERIODIC INVOICING

### Introduction

Periodic Invoicing generates and prints invoices for customers who are
billed periodically. The invoices are not posted--they must be reviewed
and posted just like any other Point of Sale documents. When creating
documents for Point of Sale, the tax rate for each line is recalculated from
the current tax table. If necessary, the batch can be cancelled, and Periodic
Invoicing can be run again.

Note:

Before running Periodic Invoicing, it's a good idea to run the Rental

Status Report (X2-10). Make changes in Rental Status as appropriate,
then run the Periodic Invoicing Report (X56-6). Make notes that will

expedite Periodic Invoicing, such as invoices to bypass or delete and

lines that should be changed or deleted.

 

There are 3 Periodic Types and related Periodic Frequencies.
Periodic Type Periodic Frequency _ Is Invoiced:

I 1-99 At set intervals, specified by
the frequency. Example:
Type "I" with Frequency= 28
is eligible for invoicing every
28 days.

M 1-31 Every month on the day
specified by the frequency.
Example: Type "M" with
Frequency= 28 is eligible for
invoicing on the 28th of each
month .


[| X55-3 PERIODIC INVOICING -

Ww 1-7 Every week on the day
specified by the frequency.
1=Monday, 2=Tuesday, etc.
Type "W" with Frequency= 5
is eligible for invoicing each
Friday.

The invoice is presented for invoicing whenever it is eligible. For
example, if you want to invoice a group of customers on the third day of
each month, use "M" as the type with a frequency of "3." Any time you
get around to running Periodic Invoicing on or after the 3rd day of the
month, this invoice will be eligible.

i
RELEASE 2.1 NL

## X55-3 PERIODIC INVOICING

### How To Run

From Menu X55, select option 3 to run the Periodic Invoicing. After the
security gate, the printer option screen is displayed.

### Periodic Invoicing Option Screen 5530-002

Enter printer ID for printing Point of Sale invoices:

Enter the number of invoice heading lines to print (0-12);

For the okidata printer, use 8.

For the IBM 5256 printer, use 9.
For the IBM 4214 printer, use 12.
For the IBM PRO printer, use 12.

Enter the number of spaces left of normal to print(0,5): 5

For the IBM 5256 and 4214 printer, use 0.
For the IBM PRO printer, use 5.
For the Okidata printer, use 5.

cmal-Cancel

 

O Type the numbers for the printer you will use, and press (Field Exit].

 

 

 

Press [Enter].
The Periodic Invoicing screen appears.

 


Fa | X55-3 PERIODIC INVOICING

Periodic Invoicing x5530-101

Invoice/PIF/Last Date/New Date
Name/Adar#
DB Unit# Qty Beseription Net Extended TD
CFOO1G3 M27 11/27/97 11/27/97
RACHEL PARKER PARKOL
METER OUT 3459.2 NO ACCESORIES 25000

(mdl-Cancel Cmd2-Print/close invoices Roll-forward

 

 

 

 

To delete or bypass an entire document, type "D" or "B" in the column
labeled "DB." Deleted documents are removed from the Periodic
Invoicing process and cannot be recovered. Bypassed documents will
show up next time.

O To delete a detail line, type "D" beside the line.

C1) To change a detail line, type over the current information. The first 2
lines, which contain document information, cannot be changed.

 

 

 

To record your changes, press [Enter].

 


X55-3 PERIODIC INVOICING |

O To print and close the designated invoices, press [Cmd2]. Two
messages are displayed:

Processing selected periodic invoices.
then:

Periodic invoicing has completed. Press enter to return to a menu.

CO Look over the printed invoices carefully. If you need to make a change, .
teopen the document in Point of Sale Invoicing, then close and reprint
it.

O From the Post POS Documents Menu (X5-5), select option 1 to Create
Point of Sale Posting Batch (X55-1).

O When the system notifies you that the batch has been created, select :
option 2 from the Post POS Documents Menu (X5-5) to Review and '
Post Point of Sale Documents.

 


[=| X55-3 PERIODIC INVOICING

### Fields & Descriptions

The fields on the Periodic Invoicing screen are described below.

DB
Unit#
Quy

Invoice

PIF

Last Date
New Date

Delete/Bypass.

Stock number of the rental unit.

Quantity of miscellaneous part. Applies to
sales codes with miscellaneous quantity
("M") format.

The original invoice number. The Periodic
Billing job can assign the next available
document number, or it can generate a
“clone” document number--the original
document number plus a letter (A-Z). In the
example above, the original document
number was CT00103. The first periodic
invoicing produces a document number of
CT00103<A, as illustrated below.

The choice between the next available
document number and a clone document
number is controlled by an OPT switch in
the OPTDIS Library. The default is a clone
document number.

Periodic type/Periodic Frequency. In the
example the type is "M" or Monthly, and the
frequency is "27," which means that the
document is eligible on or after the 27th day
of each month.

Most recent invoicing date.

Next date the document is eligible for
Periodic Invoicing.
é

Co


Name/Addr#
Description

Net
Extended


 

Customer's name and system address
number.

Description on the miscellaneous part or unit
line.

Sales price for one part.

Quantity X Net. Total price for parts on
current line, or rental amount charged to the
customer.

Tax code for the current line.

Discount code for the current line.


A sample invoice is shown below:

WHOEVER - AG, AUTO, CONSTRUCTION & TRUCK COMPANY
288 west Kellogg Road
Bellingham, WA 206 733-7616

SALES == SERVICE ---_ RENTALS.

wwe sell just about everyching™

This month's special- 188 off manufacturers AM/F¥ radios
Return Policy: Parts returned after 5 days are subject to a 108
restocking fee.

PARKO] RACHEL PARKER
(704y
4092 WINDWARD DR 373-€258

TeGA cay, SC 29605
Sold By: PARKOL FO #3 Date 11/27/97 COUNTER TICKET
Ship By: Tax
TD Qty Description -+-~+ eee price
MISC. UNIT

fA5798 FORD 770-5 M-LOADER,

METER OUT 3459.2 NO ACCESORTES

SER#: 17653

s+ SUBTOTAL
+? SALES TAK
charge sale x,

erocio3a,

amount,

250.90

$269.50

 

## CHAPTER X55-4

RECLAIM POINT OF SALE DOCUMENTS

### Introduction

This option allows you to reclaim Point of Sale documents. Accounting
transactions are not reversed by this option. Its purpose is to reclaim 1 or more
Point of Sale documents in case a P.O.S. batch is deleted because the batch was
canceled or the files were accidentally deleted - in these cases, normal recovery
does not work. After a Point of Sale batch is created, each document in it is
flagged as closed and “posted,” even though the transactions have not yet been
posted to the general ledger. This option (X55-4) removes the “posted” flag to
reclaim the document and make it available again so that it is eligible for the next
Point of Sale batch.

When a batch has been accidentally deleted, accounting transactions have not
been posted; therefore, you can re-create the batch and proceed with posting as
usual. If you use this option to reclaim a batch that had been posted normally,
make sure you reverse the accounting transactions before you re-create and re-
post the batch.


2 X55-4 ¢ RECLAIM POINT OF SALE DOCUMENTS RELEASE 2.2
oe mee AE EE

### Entrance Screen

O1 From the Point of Sale Posting Menu (X55), select option 4. After passing
through the security gate, the Reclaim Point of Sale Documents screen
appears with a warning. The screen is ijlustrated below.

Reclaim Point of Sale Documents X5540-012

### Warning!

Running this job will reclaim selected documents from the
Point of Sale and Parts files. Accounting transactions
associated with these documents, however, cannot be reversed
automatically. These transactions must be reversed manually
through Create Source Documents. To continue with this job
press ENTER; or, press Cmdl to end this job now.

Cmdl-End Job  ENTER-Continue

 

O) Press {Enter] to continue.

The following screen appears.


POINT OF SALE X65-4 » RECLAIM POINT OF SALE DOCUMENTS 3
——_—_ J OO OOo ere Eee

 
   
   
  
   
 
 

 

AER EQUIPMENT SALES
Division: A Selection

 

Reclaim Point of Saie Documents x5S401-01

Enter a valid document number

OR

Enter a posting date range

From: 100297

    

  

To: 100297

 

Enter-Continue Cmdl-End job

 
 

0 Type in either a document number or a posting date range.

Furnishing a document number will reclaim that document only. Furnishing a date
will result in reclaiming all documents posted on that date for the division, which

could mean more than 1 batch.
O Press [Enter] to continue.

A series of messages appear on the screen:
— “Selecting documents to reclaim...”
- “Removing posted flag from documents
— “Removing invoices from Periodic Invoicing...”
— “Adjusting Customer Sales Summary...”
— “Printing a list of reclaimed documents...”

 

A list of reclaimed documents is printed. If you are reversing accounting
transactions, make sure this list matches the edit list(s) you’re working from.

For documents that are reclaimed:

© The indicator that marks it as having been included in a Point of Sale batch is
removed.

« Parts are not returned to inventory, but part sales history information is
removed.-it will be re-created when the document is reposted.


4 X55-4 # RECLAIM POINT OF SALE DOCUMENTS. RELEASE 2.2

 

Service history is removed.

The invoice is removed from periodic invoicing.

Sale totals are reduced for the customer sales summary.

The document is returned to the document index as closed but reclaimed.

A message appears onscreen to let you know when the documents have been
successfully reclaimed. A sample screen is illustrated below.

Reclaim Point of Sale Documents X5540-011,

Selected Point of Sale documents have been successfully reclaimed. Accounting
transactions associated with these documents, however, cannot be reversed

automatically. These adjustments must be made manually through Create Source

Documents. Press ENTER to return to the menu.

ENTER-Return to menu

 

O Press [Enter] to return to the Point of Sale Posting Menu.

## CHAPTER X55-5

TRANSMIT EDC CREDIT CARD TRANSACTIONS

### Introduction

This option is used when you are transmitting transactions to First Data Resources
(FDR) using a DataTran device for transmitting credit card sales that were
manually authorized, reviewing, printing, and recalculating batches of
transactions and moving transactions to a different batch. In addition, this option
can be used to review, print, recalculate, and move transactions within a batch. if
you don’t have a DataTran device, you don’t need to be concerned with this
option.

### Contents

ENTRANCE SCREEN
Options .....eseeeseeeeeeeee
Open Batch...
Closed Batches
Function Keys....
OPTION 5=Display..
OPTION 7=Move to another
Select Batch Window.
OPTION 6=PRINT.......
F1O=MANUALLY AUTHORIZED TRANSACTIONS .....cesscccseesssessceseessesenee

  
  
 
 
 
  
 

Nokona vibra


2 X55-5 « TRANSMIT EDC CREDIT CARD TRANSACTIONS RELEASE 2.1

ENTRANCE SCREEN

1 From the Post P.O.S. Documents Menu (X5-5), select option 5, Transmit
Credit Card Transactions.

Transmit Credit Card Transactions DSPBDFR
Batch List

Current Open Batch:
1sSettle S=Display 6=Print 9=Recale
Opt Batch # Date Total Lines

2 8/08/97 00 0

Closed Batches:

4=Delete S=Display 6=Print 9=Recalc

opt Batch # Date Total
1 8/06/97 -00

F3sExit  F20=Manually Authorized Transactions F12=Previous {

 

Options

Open Batch

The open batch is made up of all credit card transactions that have been
automatically authorized and transmitted to FDR via the DataTran device since
the most recent settle time. As manually authorized transactions are transmitted,
they are also added to the open batch. FDR settles the transactions it has received
at 6:00 P.M. Central time; therefore, the batch on the DIS system should be set to
close at the same time in EDC Configuration. See Appendix B.

1=Settle Not currently available on the DIS System. Settlement is done
automatically by FDR at 6:00 P.M. Central time.

5=Display Displays transactions within the selected batch. See page 4. Once
displayed, transactions can be moved to a different batch. See page

5.
6=Print Prints a list of the transactions included in the selected batch.
9=Recalc Recalculates the transactions within the batch. This option, which

will rarely be needed, is provided in case a batch is out of balance. Co


POINT OF SALE X65-5 « TRANSMIT EDC CREDIT CARD TRANSACTIONS 3
see eee ARRAY ILI

Closed Batches

4=Delete Deletes a batch.

5=Display _ Displays transactions within the selected batch. See page 4. Once
displayed, transactions can be moved to a different batch. See page

6=Print Prints a list of the transactions included in the selected batch.
9=Recalc Recalculates the transactions within the batch. This option, which
will rarely be needed, is provided in case a batch is out of balance.

Function Keys

F3=Exit
Return to the Post P.O.S. Documents Menu

F10=Manually Authorized Transactions
Go to the list of manually authorized transactions, where individual transactions
can be selected for transmission.

F12=Previous
Return to the Post P.O.S. Documents Menu


4 X55-5 « TRANSMIT EDC CREDIT CARD TRANSACTIONS RELEASE 2.1

 

OPTION 5=DISPLAY (

Oo

  
      
     

FRSExit

To display the detail lines in an open or closed batch, select it with 5=Display.
You can use the position prompt line to search for a particular transaction.
Note: F21=Print generates the same report as if you selected the batch with
6=Print. See page 6.

 

Transmit Credit Card Transactions DSO8DFR
Transaction Detail

  

Line addr # Doc. # Cd Number Amount Auth # Prom TR

 

J=Move to another batch

Opt Line Addr # Doc. # Cd Number Amount Auth # Prom TR
- 3 ADAMO] SP00208 Cc 5432167890CCCC 107.80 111211 9999 RS
2 ADAMO1 SP90209 cc 5432167890CCCC 53.90- 333333 9999 RC

Fl2=Previous F2l=Print

 

 

Definitions

Cd Credit card code.
Auth # Authorization number.
Prom Promotion code.

TR Transaction code.

RS=Regular Sale

RC=Regular Credit

VS=Void Sale (document is voided after authorization, before
posting)

VC=Void Credit


POINT OF SALE X55-5 * TRANSMIT EDC CREDIT CARD TRANSACTIONS 5
oO —X-00EEeemeSree EA ERANSAU TIONS

OPTION 7=MOVE TO ANOTHER BATCH

From time-to-time, a transaction that is in process at the automatic cutoff time
may fall into a different batch on the DIS system from the FDR system. As you
reconcile your FDR statement, you may find it helpful to move a transaction to a
different batch.

1 Select the transaction with 7=Move to another batch. The Select Batch
window allows you to select the batch you want to move it to.

Select Batch Window

DSOSDFR

Line addr: : Promo TR
00000 :

lsSelect

T=Yove te ano :
Opt Batch # Date

48 5/15/97

4? 5/14/97

46 5/13/97

45 5/10/97

44 5/09/97

43 5/07/37

42 5/06/97

41 5/05/97

a0 §/05/97

39 5/05/97

Opt Line

A:
A:
A:
A:
A:
A:
A:
A:
A:
A:

#12=Previous

 

O Select the target batch with 1=Select. The transaction is moved to new batch
and is no longer listed in the displayed batch (previous screen).


6 X55-5 « TRANSMIT EDC CREDIT CARD TRANSACTIONS, RELEASE 2.1

OPTION 6=PRINT

O To print transactions within a batch, select it with 6=Print. A printed list is
illustrated below. This report is the same whether it is printed with 6=Print or
F21=Print when you are viewing a batch.

Print Batch Detail 6/95/97 15:16:14 Page

Division Code A
Batch # 18

Line Addr # Doc. # Card Number Amount Auth # Promo Type Date Time

1 ADAMO] SPO0208 CC 5432167890CCcC 107.80 111111 9999 RS 4/10/97 12:00:00
2 ADAMO] SP00203 cc 5432167a90CCCC 53.90- 333333 9999 RC 4/10/37 13:00:00

Total 53.90

** END OF REPORT **

 

 

i


POINT OF SALE X55-5 » TRANSMIT EDC CREDIT CARD TRANSACTIONS 7

F10=MANUALLY AUTHORIZED TRANSACTIONS

When transactions have been manually authorized, they must be manually
transmitted to FDR. You will be notified by a message on the entrance screen
(Batch List) that manually authorized transactions exist.

O From the Batch List, press F10=Manually Authorized Transactions. The list
of transactions that were manually authorized is displayed.

Transmit Credit Card Transactions DSRQDFR
Manually Authorized Transactions

Doc. # Card card # Amount Auth # Promo

 

1=Transmit

Opt Addr# Doc. # Card Number Auth # Promo
ADAMOL SP00272 cc 5432167890cCCC : ASDF 9999
ADAMO]! SP00274 CC $432167890CCCC : ASDF 9999
ADAMOl SP00276 cc 5432167890CCCC : ASDF g9s9
ADAMO1 SP00277 cc 5432167890CCCC : ASDFG 9999
ADAMOl SP00278 CC 5432167890CCCC : ASFD 9999
ADAMO1l SP00279 cc 5432167890CCCC : QWER 9999
ADAMO1 SP00288 CC  5432167890CCCC : ADSFG 9399
ADAMO1l SP00390 cc  5043930000000253 : 348994 9999
BELLO1 AGO0527 CC 12368768 : 2278 9999
BRADOL AGOOS31 CC  5043930000000162 . 2287 9999
900004 sP00340 cc 4500-9877-4255-3409 : skW 9999

F3=Exit P12=Previous

 

O Use the position prompts at the top to locate transactions, if necessary.

Select the transaction(s) you want to transmit with 1=Transmit. The DataTran
device will dial out and transmit the transaction(s). As transactions are transmitted
to FDR, they are added to the current open FDR batch.

If you should need to delete the transaction(s), place an “R” in front of the
transaction(s) you want to remove. Press [Enter]. A verification screen will
display to confirm that is what you want to do.


X55-5 « TRANSMIT EDC CREDIT CARD TRANSACTIONS

Notes:

## CHAPTER X56-1

RESERVATION REPORT

### Introduction

Reservation Report will list all reservations of parts for customers in
customer order and part number order.

### How To Run

From the Report Menu, select option 1. The Reservations by Customer
Number will print first.

RESEAVATICNS BY CUSTOMER NUMBER Dace 10/01/86 Page 1
Time 7.53.59 5610-40

Part nusber Description Quantity Type Date = Documenté POF

MIKE BORG 907/354-5990

028987 GASKET x17 1 6/04/86 WoOL03§ = MF SUPER 90

730095 SPRING 6/04/86 WOOI09§ = MP_-SUPER 90

31431154
31431672 VRE
32526307 srup

6/04/86 woO1086 «= MP. SUPER $0
6/04/86 woo1096 MF SUPER 50
6/08/86 © WOOL096. «ME SUPER 90

 

### Fields & Descriptions

The fields are described below:

Reservations by Customer Number in the first column, then name and
telephone number.

Vendor Vendor code of the part on reservation.
Part Number Part number of the part on reservation. If the
part is on order, the order number follows.

## X56-1 RESERVATION REPORT

Description Description of the part on reservation.

Quantity Number of the part on reservation.

Type Type of order: S for Sales or W for Work
Order.

Date Date of the reservation.

Document # Document identifying number.

P.O.# Purchase order number, user defined.

The Reservations by Part Number will then print.

ABC COMPANY ‘RESERVATIONS BY PART NOMBER Pate 10/01/85 Page 1.
weer, co B Tine 7.54.12 5610-58,
addresse custoner name Quantity Type pate Document
AMF 088997 GASKET KIT
00060 MIKE BORG 1 s 6704786 wo01096
Totals: Reserved 1 on hand 1 Available on order (

AMF iasosoms2 wines
su343 Reserved for shop work 1 s/307e6 = wo01067
Totals: Reserved on hand 2 avaliable on order

 

Reservations by Part Number Vendor Code and Part Number listed, then

description.

Address# Customer's address# who reserved the part.

Customer Name Customer's name and phone who reserved
the part.

Quantity Number of the part on reservation.

Type Type of order: S for Sales or W for Work
Order.

Date Date of the reservation.

Document# Document number for the reservation.

{
RELEASE 2.1 Qe

## CHAPTER X56-2

P.O.S. DOCUMENTS REPORT

### Introduction

The P.O.S. Documents Reports allows you to print a listing of P.O.S. documents
based upon document status. You may select, in any combination, documents
with a status of Open, Closed, Reopened, Canceled or Voided.

Note: Case requests that dealerships use “a process to record and manage the time
to complete repairs”, comprised of the date the customer requested the work and
the actual time required to complete the repairs. This report includes Days to
Completion, calculated as the number of days from the Open Date through the
Posted Date, inclusive.

1. From the Point of Sale Report Menu, select option 2, P.O.S. Documents
Report. The following screen will display:

 

NORTHWEST EQUIPMENT P.O.S. DOCUMENTS REPORT 5620-101
Division: A SELECTION SCREEN

Include the follewing documents:

 
 
 

 

 

Open documents... .... x (x7)
Closed documents... . . . N (¥/N)
Reopened documents. N (x/N)
Canceled documents. N (xn)
Voided documents. . N (sm)
Open Date: Beginning Month... .. . 0399 (mmyy)
Ending Month... 2... . 0399 (mmyy)
Closed Date: Beginning Month... ... (mmyy}
Ending Month... ..... (amyy)
Document types (blank=-include all) .. .
Sort Options: Address or Document... . A {A/D}

Cmd1-Cancel Job

 

 

 

X562.doc 7/26/99


2 CHAPTER X56-2 ¢ P.O.S. DOCUMENTS REPORT RELEASE 2.3

 

2. Select the document categories, Open, Closed, Reopened, Canceled, Voided, C
you wish to include on the report. You must answer Y=Yes for at least one
category of documents. Note: A voided document is one that is open when
[Cmd10]=Cancel/Void is pressed. If, however, the document is closed and
then canceled, it is considered canceled.

3. Choose an open date range (mmyy) and/or a closed date range (mmyy). If no
dates are supplied, the report will print all documents in the category you have
selected.

4. Select the document types you wish to include. To include all types, leave this
field blank.

5. Choose whether you want the report sorted by A=Address or D=Documents.

6. Press [Enter]. The report is placed on the job queue.

The following is a sample report for Open and Closed documents within the date
range of 08/98 to 03/99.

P.0.S. DOCUMENTS REPORT Date 3/16/99 Page 2
POINT OF SALE INVOICING SYSTEM Time 9.28.32 x5620-2
Docunents Listed: Open Closed
Opened: 12/98 - 03/99 Closed: 12/98 - 03/99 Sorted by: Custoner
Open Printing Bays to + Sold By
Customer Name Status Date Date Posted Completicn sold By
Address # AD0SO BILL BRADLEY CLOSED 8/28/98 8/26/98 8/28/98 z
GRADO? LEROY GRADY CLOSED 2/10/99 2/10/98
PRLMO2 RUTH PALMER OPEN 1/22/98
PALMO2 ROTH PALMER coszp 1/22/99 1/22/98 2/1/39
PALMOL RUTH PALMER open 1/22/99
PALMOL ROTH PALMER cLoszD 1/22/99 1/22/99 2/1/39
PALMOL ROTH PALMER 000102 OPEN © 2/07/98

Report Low:
Report High:
Report Average:
90% Average:

+ Days to Comptetion = ClosedDate-OpenDate for closed docs only. If dates are the same,Days=1.
90% Average omits the 10% of closed docs that have the highest number of Days to Completion.

 

The Days to Completion column shows the number of days each listed ticket was
in the service department, if any. Days to Completion is calculated by subtracting
the open date from the closed date of each ticket. This means that a ticket closed
the day after it is opened is considered to have taken one day to complete. A ticket
that is closed the same day that it is opened is also defined to have taken one day.

Report Low and Report High show the shortest and longest times that jobs were
open, with the Report Average showing a simple average time open for all tickets
in the time period reported.

Because there may be a few unusual jobs that require an inordinate number of
days to complete, the report shows a 90% Average, which provides the best
measurement of the zsual efficiency of the service department.

## CHAPTER X56-2

POS DOCUMENTS REPORT

### Introduction

The POS Documents Reports allows you to print a listing of POS
documents based upon document status. You may select, in any
combination, documents with a status of either Open, Closed, Reopened,
Canceled or Voided.

Note:

A voided document is one that is open when [Cmd10]=Cancel/Void is
pressed. If, however, the document is closed and then canceled, it is
| considered canceled.


[2] X56-2 P.O.S. DOCUMENTS REPORT Cc

### How To Run

From the Point of Sale Report Menu, select option 2, Held Documents
Report.

The following screen will display:

AGR EQUIPMENT SALES P.0.S. DOCUMENTS REPORT 5620-101
Division: A SELECTION SCREEN

Include the following Documents:

Open documents cen. (
Closed documents aan...
Reopened documents wm...
Canceled documents (W/m) wee
Voided documents (Y/N)...

€mdi-Cancel job

 

Type the letter Y for each type of document status you wish reported. Press
Enter.

RESULT: The report will print and the Point of Sale Report Menu will

RELEASE 2.1 LU


X56-2 P.O.S. DOCUMENTS REPORT

return to the screen.

ABC COMPANY P.0.5. DOCUMENTS REPORT Date 10/26/97 Pace
BELLINGHAM, WA POINT OF SALE INVOICING sysTet Tame 13-59-04 5620-28
Pocunent, Open Printing
Custorer Name Number Status Date. Posted Sold By
Address * ADAMO WILLIAM ADAHS ysoo107 © OPEK 8/31/97 ROGER
ADAMO] WILLIAM ADAMS vs00118 © OPEN «9/61/97
ADAMO WILLIAM ADAMS 700181 REOPENED
ADAMO] WILLIAM ADAMS 085013! vOKRED.
BEAUO1 H BEAUREGARD AROCII3. OPEN 10/26/97
BEAUO1 H BEAUREGARD TVO0932 CLOSED 9/13/97 9/3/97 9/23/97
BERUO? H BEAUREGARD FVDOS3LA OPEN 9/13/97 9/13/97 :
BELL? SUSIE BELL ROOO2I6 CLOSED 9/23/97 9/23/97 6/23/97 :
BELLO SUSTE BELL RO0G237 CLOSED 9/23/97 9/23/97 8/23/97
OULO2 STEVE BOULNAN 90012 OPEN 9/16/97
DARNG2 DARNGOOD FOORS ARDOIOIA OPEN 9/27/97 9/27/97
DRAZOa THOMAS DRATN ROVOZ21 OPEN 9/92/37
FLOYO1 FLOYD FLOYD ANO0195 CLOSED 9/27/97 9/27/97
PLOYO1 FLOYD FLOYD AROOLOSA OPEN 9/27/97 9/27/97 .
HALSO1 WALLACE HALSTON amgo1o4 = OPEN 9/27/97
INTRNL INTERNAL CHARGES RON0Z3S CLOSED 9723/97 9/23/97 9/23/97
ISTRNL DEALER INTERNAL EXPENSE RO90223 CLOSED 9/23/97 9/23/97 9/23/97
KRUCOL BRAD KLUCUM TV90S33A OPEN 9/39/99 9/19/97
MRMOL KENT JAMES 0015 REOPENED 10/19/97 10/19/97
(028001 OLSON'S COMMERCIAL AROOLI2 CLOSED 9/2797 9/27/97 h
SEREG1 SERENE VALLEY FARMS, INC qv00932A CPEN 9/13/97 9/13/57
‘SHAWOL SHAW PAPER SUPPLY ARI0110 CLOSED 9/27/97 9/27/97
SHAMOL SHAW PAPER SUPPLY ARUOLIOA OPEN 9/27/97 9/27/97

   

 


[+] X56-2 P.0.S. DOCUMENTS REPORT

### Fields & Descriptions

The fields are described below:

Address#
Or Stock #
Customer Name

Document Number

Status

Open Date
Printing Date
Posted

Sold By

Address number for the customer.

Stock number, if an internal work order.
Customer name with the held or closed
document.

Held or closed document number.

Either OPEN, CLOSED, REOPENED
CANCELED OR VOIDED.

Date the document was originally opened.
Date the document was printed.

Date document was posted.

Employee number entered as the salesperson
on the document.

Every document that is open or closed since the last time Point of Sale
End of Month was run will appear on this list. If you find the system
slowing down, run Point of Sale End of Month (X5-4) to clear out the
posted document numbers. This will help to speed up the system.
(
Ne

## CHAPTER X56-3

SALESPERSON ANALYSIS REPORT

### Introduction

The Salesperson Analysis Report shows which salesperson sold parts to
customers and internal units. It lists cost and margin on each sale. You can
select the time period you want and the sales codes that you want included
or excluded on the report.

The detail used for this report and for the Labor Analysis Report
(X56-4) is removed by Point of Sale End of Month.

## X56-3 SALESPERSON ANALYSIS REPORT

 

### How To Run

From the Point of Sale Report Menu, select option 3, Salesperson Analysis
Report. The selection screen is displayed, as illustrated below:

SALESPERSON ANALYSIS REPORT x5630-301

Enter Transaction Dates

Beginning Date .: 100294 (mMpDyy) (

Ending Date : 101394 (MMDDyy)

Include/Exclude

Sales Codes

Crdl-End Job Enter-Continue

 

The Point of Sale Report Menu returns to the screen. The report is printed
unless the information you requested has been removed by Point of Sale
End of Month.

RELEASE 2.1 Cu


A & R QUIPHENT SALES
BELLINGHAN, WA

Selesperson
Customer Name

+ DAVID STROH
‘WILLIAM amaxs

DAVID STROM

- AL HARFOLD
AMY TWOSHOES
AMY TWOSHOES
AMY TWOSHOES
AMY TWOSHOES
‘SERENE VALLEY FARMS, INC
SERENE VALLEY FARMS, INC
WALLACE HALSTON

ae

ae

HAL HARPOLD

+ WILLTAN ADAMS.
AMY THOSHOES
LARRY ‘TRUMAN
SHAW PAPER SUPPLY

ae

WILLIAM ADAMS

ae
+ Totals for

not

ae


This is a sample Salesperson Analysis Report.

SALESPERSON ANALYSIS REPORT Beginning vate
Reporting for Division A

Excludes Sales Codes

Y
>
¢ Pocument
pavip
‘aR00101,
Customer Totals

Employee Totals

AL
Ro00212
000213
ROOOLLE
ReCO1I5
R000106
Reo0107
er00127

Custemer Terals

employee Tozals
WILL
700238
cr00135,
700141
customer Totals

Employee Totals

Division R seeesrterenrstennereereennneeeeeey

Customer Totals
Invernal Totals
Wacranty Totals

Grand Torais

Gross.

Amount,

3813.75
3813.75

3813.75

2.50
3.50
3.50
3.90
10.00
50.00
28.00
93.69

93.60
20.00
1000.00
+20

1020.20

1020.20

4527.55

4927.55,

Ending Dave
PC PS

Discount
sot

Buployee amount

301.39
381.39

10.00
100.99 10.09 100,00

100,09 «382.39 10.00 100.00
+00
00
-00
+00
+00
-00
00
00

-90

-0
209,00 -00

200.00 -00

200.00

-00
00 -00

381.39 7.74

10701793,
2 10/13/94

Date 10/13/94
Pime 15.21.35

Net:

amount

3432.36
3432.36

3452.36

3.30
3.30
3.90
3.90
10.00
50.00
18.00
93.60 2.

93.60
20.00
1900.00
20
1020.20 22.44
1020.20 22-44
4846.16 100.00
+00

-00

4546.16

Page 1
xS630-2A,

Margin

100.00
100.09 *

100.00 *=

242424.24 906.15-
242424.24 906.15-
262424.24 906.15»
262424.24 906.15~
300.00
100.00
121212.12 300,67-
xoso9ce.08 402,15-+

2090909.08 401.15-:

290.00
200.00
100.00
100.00 +

100.00

190909.08 @56.28-

00+

3090509.08 896,28-*+

### Fields & Descriptions

Salesman
Customer Name

#

Type

Document

Gross Amount
Gross % of Employee
Discount Amount %
Discount % of Total
Net Amount

Net % of Total

Cost

% Margin
Customer Totals

Internal Totals
Employee Totals
Totals for the Division
Customer Totals
Internal Totals

Grand Totals

Name of the salesperson, taken from SOLD
BY field.

Name of the customer or business, if
customer. Or Stock

Stock #, if internal work order.

Type of document.

Document identifying number.

Gross amount sold per document.
Percentage of the employee sales.

Percent of discount.

Percent of total amount.

Net amount of sales on document.

Net percentage of total sales. (
Cost of the sold item(s) or transaction.
Percentage of profit on the sale.

$ and cents totals of all customer
transactions.

$ and cents totals of all internal work orders.
Totals of all employees transactions.

Totals from the division or ALL for
customers.

Totals from the division or ALL for internal
wo.

Total from both internal and customer totals.

LO

## CHAPTER X56-4

LABOR ANALYSIS REPORT

### Introduction

For closed and posted documents, the Labor Analysis Report:

Can be printed for 1 or all divisions

Can be requested for a time period -

Lists customer, internal, and warranty totals

Counts each type of document

Includes hours reported and hours billed

Hlustrates margins achieved in the shop by calculating percentages
of totals in each category

 
   

Note:

    

The detail used for this report and for the Salesperson Analysis Report
(X56-3) is removed by Point of Sale End of Month.

 

 

### How To Run

From the Point of Sale Report Menu (X5-6), select option 4, Labor
Analysis Report. At the security gate, you can indicate whether you want
ail divisions. The date range screen follows.

The default range is from the first day of the current month to the current
day.


[2] X56-4 LABOR ANALYSIS REPORT .

LABOR ANALYSIS REPORT 5640-301

Enter Transaction Dates

Beginning Date .: 70198 (MMDDYY)

Ending Date : 72198 QamDYY)

cmai-End Job

 

 

 

To change the range, simply furnish beginning and ending dates in the
format MMDDYY.

O Press [Field Exit) after each entry.

 

 

 

 

Press [Enter] to print the report, which is placed on the job queue.

An example of the Labor Analysis Report follows.


ASCWAG.AUTO,CORS & TRICK CO.
BELLINGHAM, WA

Employee
customer Name

+ BILL P. COOKE
GRECIAN ARTIPACT COMPAKY
JBMES E, MET2LER
JAMES E, MET2LER
LEROY GRADY
LEROY GRADY
LEROY GRADY
LEROY GRADY
MELISSA MCCONAUGHEY
'THERMC KING WARRANTY
THERMO KING WARRANTY

X56-4

BABOR ANALYSIS REPORT Beginning cace : 3/01/98
Reporting for Division a ending nate ...: 7/21/98

Hours----*
Reported Billed

eroose6 © 3/22/98 5.00 10.08
Pyo109g 5/07/98 250 2.59
Feooog2 12/98 hao t.08.
craosss 406/98 5.00-  ¢.0a
e7aa3s9 4/06/98 = 30.00 36.60
woogese 3/05/98 s.00 5.09
wo0de72 4/22/98 2.00
901007 5/07/98 3.50
woou0ss = 5/14/98 2.50
woosoes © 5/15/58 1.50

Scock# Bw1000 000075 423/58 1.00

WARRANTY CASE

BILL 2. COOKE

+ AMY TWOSHOES
CASE WARRANTY
LEROY GRADY

Totals for


700378 © 6/11/98 20.00

- Customer Totais 32.00
S$ * Internal Totals 13.09
2 warranty Totals 4.00

12" Employee Totals 49.00 55.75

any
wvosons6 = 6/11/98 5.05 5.06
Tcrgo379 6/11/98 10.06, 10.98

Lov Internal Tocals 19.00 16.96
Lov Warranty Totals 5.00

prployee Totals 15.09 15.06

Division A! a7
7 + Customer Torals 44.00 45.66
9 + Internal Totals 21.08 “99
5 + warranty Totals 14.25 14.25
24+ Grand Totals 49.28 96.00

fours Mours
Reported Billed
As tof as tof
urs Hours
Bilted xeporeed

st.co
106.36
100.00
- 160.98
100.85,
390.08
300.59

359.09
190.09

uis.a0
156.45
190.00,
107.56

LABOR ANALYSIS REPORT

Pate 7/21/98 Pa
‘Time 19.59.21 x5

*-Hours Reported-*
as taf ast of ‘Gros:
anployee Shop

Total Total, Anoune

200.00
137.50
35.00
5.00:
10.90:
275.00
64.00
178.78
437.50
82.50
96.00
980.00
1551.25
420.00
220.00

2191.25

49.30 a7in.28
34.73 555.00
18.97 768.75
100.00 3435.00

we 1
640-28,

of
Total

11.69
8.06
3.24
82
105+
28.89
6.70
20.45
27.89
30.73,
10.05
37.27
90.65 ¢
43.98 +
28.62 ¢

63.79

49.82
27.80
22.38
190.00

 

If the Thermo King OPT (X63B-6) is on, the Labor Analysis Report is

subtotaled by job code.


[+] X56-4. LABOR ANALYSIS REPORT

### Fields & Descriptions

The fields are described below:

Employee

Customer Name

Or Stock #

Type

Document

Work Date

Hours Reported
Hours Billed

Hours Reported as %
of Hours Billed
Hours Billed as %
of Hours reported
Hours Reported as %
of Employee Total

Hours Reported as %
of Shop Total

Gross Amount

Gross % of Total

Person who worked the hours for the
customer. (Taken from the Employee# on
the invoice.)

Person billed for the labor, if labor for
customer.

Stock number, if labor performed on internal
WG.

Document type includes any type you have
entered through Document Classification
Maintenance (X52-2).

Document identifying number.

Date the labor was performed.

Number of hours worked, in decimals.
Number of hours billed, in decimals.
Number of hours worked divided by

hours billed, expressed as percentage.
Number of hours billed divided by hours
reported, expressed as percentage.

Hours reported divided by total employee
hours for the month since the last POS End
of Month, expressed as percentage.

Hours reported divided by total shop hours
since last POS End of Month, expressed as
percentage.

Number of hours multiplied by the charge
per hour (total dollar amount).

Total dollar amount divided by division
total, expressed as percentage.
CL


Customer Totals
Employee Totals
Totals for Division
Customer Totals
Intemal Totals
Warranty Totals

Grand Totals

X56-4 LABOR ANALYSIS REPORT [=]

Totals for all fields applying to the
customer.

Totals of all fields except the shop total and
gross % of total.

Customer totals, preceded by count of
customer documents.

Internal totals, preceded by count of internal
documents.

Warranty totals, preceded by count of
warranty documents.

Grand totals of all items in fields.


Notes:

## CHAPTER X56-5

WORK-IN-PROCESS REPORT

### Introduction

The Work-In-Process Report provides cost and profit margin information
for open Point of Sale documents. The report allows the user to estimate
pending income from these open documents. Work-In-Process can be run
for one, all, or a selection of documents. If a single document is requested,
and only one division is selected, the report is evoked and processes only
the single document in order to speed performance. The user can also
select line by line detail or summary information. A Work-In-Process
Recap gives subtotals by sales code of ali documents in the report and also
provides extended cost, extended price, discount and tax totals for all
documents. Parts flagged with priority code “L" to indicate lost sales are
not included on this report.

### How To Run

From the Point of Sale Reports Menu (X56-5), select option 5,
Work-In-Process Report. The security gate includes a selection for all
divisions. The selection screen is illustrated below:

### X56-5 Work-In-Process Report

A & R EQUIPMENT SALES WORK~IN-PROCESS REPORT xS650-101
Division * Selection

Enter Document Numbers iup to 10, separated by commas}, and/or

xange of Decuments (show range with hyphen, separate ranges

with commas), ox ALL (for all Documents). See example:
1¥00382, S000001-S000100, #000647A, wo00893

ALL

Repair Orders (¥/N)

Counter Tickets (¥/N)

Document detail {¥/N)

Sales Code totals by Document (Y/N) . . -
: Sold-by Address

cmd1-End Job

 

O Choose the document(s) to be included. For a selection of documents,
you may combine single documents and ranges. For example,

### In11223A, In10995A, So00001- $000010,W000893

When asking for two or more ranges, separate the ranges with a
comma.

If a single document is requested, and only one division is selected, the
report is evoked and processes only the single document in order to

{
RELEASE 2.2 XL


X56-5 WORK-IN-PROCESS REPORT |

speed performance.
Type Y (Yes) or N (No) to include Repair Orders on the report.

Type Y (Yes) or N (No) to include Counter Tickets on the report.

Type Y (Yes) or N (No) for line by line detail to print for each
document.

Type Y (Yes) or N (No) to print Sales Code totals by document. Type
Y (Yes) if you want the report to include a sales code summary for each
document. The summary will provide total extended price, extended
cost and profit margin per sales code for each document.

Type Y (Yes) or N (No) to print in order of Sold-by address.

Press ENTER. The report will be placed on the job queue. Press
ENTER to return to a menu.


X56-5 WORK-IN-PROCESS REPORT

 

### Fields & Descriptions

ELISABETH’S Q.A. FILES WORK-IN-PROCESS REPORT pate 2/20/98 Page 1
BY THE FIRE EXIT: . Tire 8.25.11 x5680-3a
Seleczion: 111762,R02S801 Print: Repair Orders... ¥ Pocument Setail. 2... 2. ¥
Counter tickets . . ¥ Sales Code totals by Document . . ¥
Addr Num/nane/adéress/Pnone Do¢ Nur/ Sales Profit
Unit Nun/Make/Modei/Serial ate/pox Code TOP gty Description extended Price Extended Cost Margin

 

swo0a7 11762
190244 FORD oD 129.00 20.00 8
SC WILDLIFE & HARINE
G01 § aRPt2530 13.60- 32.07
P.O. BOX 12553 arigse
091 § Bs392300 2.78 54.30
CHARLESTON, SC
RUBBER HOSE : so 25.00
(803) 795-6350
RECEIVED GN ACCOUNT 300,00
MECD «1/25/98 5.50 86.00 23.60
LABOR 82.06 23.60
REC'D ON ACCT 269.09 (
MISC PARTS SHOP 4.50 25.00
PARTS COUNTER 10.84 22.46
FORD RENTAL 120.90 20.00
Document subteral 201.56
> Discount
= Subrotal 201.86
+ Tax
- Prepayments

= Total
300338 Ro1S801
1 001 5 muuwaee

FORD

5.00 MECD 2/12/98 5.00
cosi2x 5/30/85,
714796

LABOR

PARTS INTERKAL

Document Subcocal 159.24
+ Discount,

= subtotal, 159.24
+ Tax 7.96
+ Prepayments

etal

 

RELEASE 2.2 to


X56-5 WORK-IN-PROCESS REPORT [=]

Addr Num/Name/Address/

Phone For a customer document, this field contains
the address number and customer
information.

Unit Num/Make/Model/

Serial For an internal document, this field contains
the unit number and unit information.

Doc Num/Date/PO# Document number, date the document was
opened and purchase order number, if
applicable.

Note:

 

The following fields are used only when document detail is requested.

Sales Code Sales code for this line.
When totals. by document is requested, this
field wil] also contain a sales code summary
printed below the line detail. The summary
will print each sales code used on the
document, followed by a description of the
sales code, extended price, extended cost
and profit margin information per sales

code.
TDP Tax, discount and priority order codes for
this line.
Qty Quantity of items sold on this line. For
labor, number of hours billed.
Description Description as it appears on the document.
Extended Price For parts, this field contains quantity


[ «| X56-5 WORK-IN-PROCESS REPORT

Profit Margin

multiplied by price of each part.

For labor, this field contains hours billed
multiplied by rate charged.

For everything else, this field contains
whatever appears in the amount column on
the invoice. Extended Cost Source of
information in this field varies according to
format of the line's sale code.

M format Misc. Quantity: If this sales code
credits a sales account with a factor,
extended price multiplied by factor equals
extended cost.

P format Parts: Actual cost of part times
quantity.

W format Units: Actual cost of the unit.

D format Misc Description: This field will
be blank.

L format Labor: Hours reported times pay
rate of employee doing the labor.

A format: Received on account. This field
will be blank.

R format Units Rental: If sales account for
this sales code has a factor, extended price
times factor equals extended cost.

C format Prepayments: This field will be
blank.

Extended Price minus Extended cost divided
by Extended Price.
CL


X56-5 WORK-IN-PROCESS REPORT [7]

Note:

|| If you do not request document detail only, the document subtotal
section will print for each document on the report.

 

Document Subtotal Total extended price, extended cost and
profit margin for all lines on this document.
Received on account and prepayment lines

are not included.

Discount Total discount.

Subtotal Total extended price minus discount;
extended cost and revised profit margin.

Tax Total tax.

Prepayment Total prepayment.

Total Subtotal for extended price plus tax minus
prepayment.


| a X56-5 WORK-IN-PROCESS REPORT

BLISAEETHS Q.A. PILES
BY THE FIRE EXIT
Selection: 1N11762,R015601

sales
Division Code

Cc

WORK-IN- PROCESS REPORT Pate 2/20/98 Page 1

Recap mime 9.75.11 XS650- 38
Princ: Repair orders. , . ¥ Document detail . -

Counter tickets . . ¥ Sales Code totals by Document . . ¥

Profit

Description extended Price Extended Cost Margin

 

Pa
a
RA
0s
Pe
FR

Division

Sales Code

Description
Extended Price
Extended Cost
Profit Margin

 

PARTS INTERNAL 9.24 6.30 31.82
LABOR 188.00 34.64
RECV'D ON AccT

MISC PARTS SHOP

PARTS COUNTER

FORD RENTAL

Decument Subcotal 307.96 28.
= Discount

= Subtotal “ 397.96 27,
+ Tax

~ Prepayments

= Total,

The Recap sorts by division and provides a
separate sales code summary and subtotal
section for each division.

List of every sales code appearing on the
report.

Description of each sales code.

Total extended price per sales code.

Total extended cost per sales code.

Profit margin per sales code.

The document subtotal section provides information for all documents
included in the report.

RELEASE 2.2 LO

## CHAPTER X56-8

LABOR SALES CODE REPORT

### Introduction

For closed documents that have not yet been removed by Point of Sale End
of Month (X5-4), the Labor Sales Code Report provides a perspective on
sales activity for all or 1-10 selected labor sales codes (format "L"). This
Teport is divisional. The report is sorted by salesperson (from the "Sold
by" field on the Point of Sale Invoicing screen). See also Salesperson
Analysis (X56-3) and Labor Analysis Reports (X56-4).

### How To Run

From the Point of Sale Report Menu, select option 8, Labor Sales Code
Report. Following the Parts security gate, the selection screen appears, as
illustrated below:

A & R SALES & LEASING LABOR SALES CODE REPORT x56801-01
Division: A

Enter ALL -0..........
Or Some Sales Codes ...:

From Posting Date .... :

To Posting Date ...... :

Enter '¥' For Summary .: N

Cndi-End Job

## X56-8 LABOR SALES CODE REPORT

O Make your selections. To request a report for one day, type the same
date in the fields labeled "From Posting Date" and “To Posting Date."
Press [Enter} to place the report on the job queue.

 

 

 

 

An example of a Labor Sales Code Report follows:

A&R SALES & LEASING Labor Sales Code Report Date $/22/97

Division: From: 1/91/97 Te: $/22/97 Sales Codes: ALL vine 6.56.29

Job Hours --s--- Billed
SC Dacument Date Employee code Reported = Billed Rate Mazgin
Bur BUD WILKINS

Te LABOR CUSTOMER

te 008103
te ROO
te RON103

39/16/97
5/16/97
20/97

Sales Code Totals
> Sold-by sud Totals :
- Sold-by su Totals =
ss SAY SWENSON

LABOR CUSTOMER

Te
Te R000307
re R000162
re Ro0s302
Te Roasi02
Te Rooo1a2

8721797
5416/97
5716/97
8716/97
8720/97

Sales Cade Totals TC :
+ Sold-by ss Totals :
- Sold-by $8 Totals =

Grand Totals :
Grand Totals

 
‘
NO

## CHAPTER X56-6

PERIODIC INVOICING REPORT

### Introduction

The Periodic Invoicing Report, which is similar to the Aged Payables
Report, lists documents that are eligible for periodic invoicing. Documents
are selected for invoicing by the presence of a Periodic Type and Periodic
Frequency on the Sold-To screen. Documents on which the Periodic Type
is blank are not included. Only lines with formats of "U" (Miscellaneous
Unit), “D" (Miscellaneous Description), and "M" (Miscellaneous
Quantity) are processed.

Invoices are scheduled for periodic billing based on their posting dates.
You can choose to list all documents or restrict the report to “only invoices
scheduled for today," which means documents eligible on or before the
current session date. Documents or lines can be bypassed or deleted in
Periodic Billing (X55-3).

## X56-6 PERIODIC INVOICING REPORT

### How To Run

From the Rental Report Menu (X56), select option 6, Periodic Invoicing
Report. After the security gate, the selection screen appears.

ABC COMPANY PERIODIC INVOICING REPORT X5660-001
Division: * Report Options

Invoice Selection

1. All invoices on file
2. Only invoices scheduled for today

Enter option: 1

Cmdi-Ead job Enter-Continue

 

Make your selection, and press [Enter]. The report is put on the job queue.
An example of the report follows:

ABC COMPANY POREODIC INVEICING REPORT DATE 11/27/90 Pace 1

BELLINGHAH, A ALL Invoices on File Tine 19.57.48 x5660-262
Naw extended +

Price Amount ~

 

Invoices 1/# Dete Unie

PARKS2 RACHEL PARKER OTOOLOIA M27 10/27/90 11/27/90 FAS?28 METER OUT 3459.2 NO ACCESORIES 250.00

 
LL


X56-6 PERIODIC INVOICING REPORT [2]

### Fields & Descriptions

The fields on the report are described below.

- Division code.

Addr# Customer address number.

Customer Name Self-explanatory.

Invoice## Document number. A new document is

created each time. The system assigns the
original document number with the
appropriate letter of the alphabet. Example:
The original document for the listing above
was CT00103. At the first periodic billing,
the document number is CTO0103A.

THF Type/Frequency. In the example above, the
Periodic Type is "M," and the Periodic
Frequency is "27," which means that this
document is eligible for invoicing on the

27th day of each month.

Last Date Most recent invoicing date.

New Date Next date the document is eligible for
Periodic Invoicing.

Uniti Stock number of the unit.

Qty Quantity of the miscellaneous part (lines
with "M" format only).

Description The descriptive entry on the miscellaneous
units or miscellaneous description parts line.

Unit Price Applies to miscellaneous parts lines only.
Sales price for one part.

Extended Amount Quantity X Unit Price. Total price for this
line.


Notes:

!

RELEASE 2.1 QL

## CHAPTER X56-7

PART SALES CODE REPORT

### Introduction

The Part Sales Code Report provides a perspective on sales activity
summarized by sales code. The report can include parts sales code with >)
format or it can be restricted to 1-10 specific sales codes. This type of
information is available only for closed documents that have not been

removed by Point of Sale End of Month Procedure (X5-4).

## X56-7 PART SALES CODE REPORT

 

### How To Run

From the Point of Sale Report Menu, select option 7, Part Sales Code
Report. Following the Parts security gate, the selection screen appears, as
illustrated below:

  
      

PART SALES CODE REPORT

  

A & R SALES & LEASING
Division: A

 

*86701-01

  
  
  
   

Or Some Sales Codes ...:

From Posting Date .... : Qmmpyy)

To Posting Date ...... :__ (Meppyy)

  

enter 'Y' For Summary .; N

 

Make your selections. To request a report for one day, type the same
date in the fields labeled "From Posting Date" and "To Posting Date.”
Press [Enter] to place the report on the job queue.

 

 

 

 

 

f
RELEASE 2.1 \


 

 

 

An example of a Part Sales Code Report follows.

A&R SALES & LEASING Part Sales Code Report, 4/22/92 Page 1
Division: A From: 1/01/80 To: 4/22/32 Sales Codes: ALL 28.55.32 5670-202

SC Pocu.# Ar? vea Part + ry description Bin Deoler List E Coss Margin Marg.
PC PAR?S CUSTOMER

xvo0025 5096
rvo0925 49838
rvo0025 73183
000107 70091,
000107 71468
000107 7353
00120 a1i208
Rooo12s 12674
Roo0129, aliigo
000120, aiiiso
eroo109 Poet .
Ro00105, 25623, BEARING

 

Sales Code Torals PC :

RO00103 FT0888 CAS 35646 2 HOSE.
ROOO103 FT05BE CAS 491479R2 8 CLIP

Sales Code Totals PI :
PARTS SHOP

000107 35846 Rose 12.68 5.91
000102 17578 PACKING 24.75 -00
000102 sosogoci FUSE 26 +52 00
090102 17578 PACKING 29.50 34.75 14.75
000102 35646 HOSE 18.59 32.68 S92
000102 70091 BUSHING 35.29 24.05 31.23
000102 71466 Ring 1.67 1.74 1.20
000102, 73183 BRS 7.86 3.43 2.53
000103 17578 PACKING 29.50 14.75 24.75
000103 39646 HOSE 38.59 32.68 5.91

Sales Code Totals PS + 174.50 114.08 62.09
Grand Totals 284.02 229.98 128.50

  


Notes:

f
RELEASE 2.1 NU

## CHAPTER X56-9

DOCUMENT ANALYSIS REPORT

### Introduction

The Document Analysis Report provides a different perspective on Point
of Sale transactions. It can be requested for all or 1-5 selected document
types as defined in Document Classification Maintenance (X52-2). The
report can include all Point of Sale users or it can be restricted to a single
employee (Sold By). The information for this report is available only for
closed documents that have not been removed by Point of Sale End of
Month Procedure (X5-4).

### How To Run

From the Point of Sale Report Menu (X5-6), select option 9, Document
Analysis Report. Following the Parts security gate, the selection screen
appears, as illustrated below:

A & R SALES & LEASING DOCUMENT ANALYSIS REPORT x56901-03
Division: A

Enter ALL

Or Some Document Types ...:

Sold-by (or ALL) ..... +

From Posting Date .... :

To Posting Date ...... :

## X56-9 DOCUMENT ANALYSIS REPORT

   

O Make your selections. To request a report for one day, type the same
date in the fields labeled "From Posting Date" and "To Posting Date."
O Press [Enter] to place the report on the job queue.

An example of a Document Analysis Report follows:

A & R EQUIPMENT SALES Documant Analysis Roport Dace 4/22/32 Page 1
Divisien: L From: 1/02/31 To: 4/22/92 Doc Types: ALL Time 9.12.45 5690-201

Doc # Addr # sold-by
Date Houzs Hours ff, Labor

crployen sock code seport nitiea 8 cose
rws2003_aovisa_ he P Inntcanion co vovaz?
petals HSI oo cad Ok “00
rvs3007 105086. TARE Pais, soot
fetie svsi007 doa “oo
rvs3000 0501, BER seodst
svss0eo. f03668 Les, saaexson vood3i {
rotaie 83080 000k
svssoet R016 ot YACHDIER 60.
woeels Wsi0er oo 608
wvsscey 102738 a HEN
otis site oo ett

Totals Customer .00 008
‘Totals Internal 100.00
‘Totals Warranty 100008

6 Grand Totals .00 00s

 

t
RELEASE 2.1 \.

## CHAPTER X56-10

CUSTOMER SALES SUMMARY

### Introduction

Customer Sales Summary provides period-to-date (starting and ending
MMYY) totals for customers who fall into Parts, Service or Unit
categories. Other divisions can be included, if desired. The report can be
run for numerous periods without changing the session date. When an
ending period that is older than the current month is requested, the Life-
To-Date (LTD) fields will accumulate up to and including the ending
period. Since totals are not purged from the system, cumulative totals are
reported as Life-To-Date.

Categories are defined by user-selected document types and sales codes.

NOTE
Sales figures are added to customers’ totals
when a Point of Sale batch is created. Totals

begin accumulating as soon as sales codes
have been assigned. No prior totals are
included in the summary.


[2 | X56-10 CUSTOMER SALES SUMMARY a

### How To Run

At the Point of Sale Report Menu (X5-6), select option 10, Customer
Sales Summary. Enter your division and password at the security gate, if
any. Press [Enter]. The following screen appears.

A&R EQUIPMENT SALES CUSTOMER SALES SUMMARY X56A01-01
Division: A Division Selection

Place a '¥' beside divisions you wish to include on summary.

NB DEALER SALES & SERVICE, LID. ND ABC COMPANY
NE ABC COMPANY NM MOTORCYCLE CITY -
NT THERMOKING {

Gndi-Cancel job

 

G To include divisions in addition to the one you specified at the security
gate [Tab] over to the appropriate division(s) and enter a "Y."
O Press (Enter).

Cc

## X56-10 CUSTOMER SALES SUMMARY

AGR EQUIPMENT SALES CUSTOMER SALES SUMMARY XS6A01-02
Division: M Selection

report by:

Descending period-to-date total sales
Descending life-co-date total sales
Descending period-to-date part sales
Descending life-to-date part sales
Descending period-to-date service sales

 

Descending life-to-date service sales
Descending period-to-date unit sales
Descending life-to-date unit sales
Descending receivable total balance
Ascending customer address number

Sort option: 1

Beginning Month/Year for report? 0198
Ending Month/Year for report? 1298

cmdi-Cancel job Cmd2-Assign Codes

 

O If you want to assign specific sales codes to be included in the report,
press [Cmd2]. Refer to the Assign Codes section in this chapter for
more information.

0 If you want period-to-date calculations, select the beginning
Month/Year and ending Month/Year. The default is the current year.

O Determine the method that will be used to sort and calculate. Press
[Enter]. The report will be generated and sent to the system printer.

An example of the report follows:


LEE‘S TRACTOR SALES, INC.
LYNDEN, WA a

Addr Name AVR Balance
SHITO2 DAVE SMITA

HENNOL PRANK HENNENEY

Customer Sales &

Last Sale PTD/
First Sale 7D Parte Sales
10/15/38 4e76
10/15/98 “a
10/15/28

10/5/98 5

pay
LID Service Sales

REMEMBER
Sales figures are added to customers’ totals
when a Point of Sale batch is created. Totals
begin accumulating as soon as sales codes
have been assigned. No prior totals are
included in the summary.

pate 19/16/98
Time 16.27.55

pry
LTO units Sales

Page
XSERO-24

pry
LTD Tetal seles
44.76
44.76
6.00
6.00

59.76
59.75

 
\.


X56-10 CUSTOMER SALES SUMMARY |

Assign Codes —Entrance Screen

O To include specific sales codes in the report, press [Cmd2]. The
Entrance Screen, which is Assign Sales Codes appears.

CUSTOMER SALES SUMMARY X56A03-01 1
Assign Sales Codes

Division.
Document Type
Sales Code

Cmd3-Return  Cmdd-Print List

cma5-Enter Funct Codes Enter-Continue

 

0 By default, the division you specified at the security gate appears in the

“division” field. To change it, enter another division in its place. Press
[Tab] to move on to the next field.

O To print a list of sales codes assignments, press [Cmd4]. See the
section, Print List.

O To Enter Function Codes, press [Cmd5]. Function Codes do not apply
to most dealers.


Le] X56-10 CUSTOMER SALES SUMMARY .

O Enter a document type in the "document type" field. Document types
are set up in Document Classification Maintenance (X52-2). Only
transactions of the document type you specify will figure into the
teport. Press [Tab] to move on to the next field.

O Enter a sales code in the “sales code" field. Sales codes are set up in
Sales Code Maintenance (X52-3). Only transactions of the sales code
you specify will figure into the report.

O Press [Enter]. Prompts for Category and Plus/Minus Code are added to
the screen, as illustrated below:

LEE'S TRACTOR SALES CUSTOMER SALES SUMMARY X56A03-02 2
Assign Sales Codes

Division wR
Document Type - © COUNTER TICKET (
Sales Code........... PC PARTS CUSTOMER

Category (PsParts, S-Service, U=Unit)... P
Plus/Minus Code (P=Plus, M=Minus)

Cna3-Return Without Save  Cmd19-Delete Sales Code Enter-Save

 

The Plus/Minus code (P/M) lets the system know whether the data should
be added to or subtracted from the total. It is particularly helpful in the

RELEASE 2.2 LO


 

case of unit sales for items that should not be counted in the total, such as
fees.

O To cancel the assignment, press (Cmd3}-Return Without Save.

0 To delete the assignment, press [Cmd19], which is the same as
[Shift]+[Cmd7].
O To save the sales code assignment, press [Enter].

Print List

From the Entrance Screen, press [Cmd4] to print a list of sales code
assignments.

Return to the Division Selection Screen

Press [Cmd3] to return to the Division Selection screen.


Notes:

## CHAPTER X56-11

PRICE OVERRIDE REPORT

### Introduction

The Price Override Report lists point of sale documents where default
prices have been changed. It can be printed for a range of dates; therefore,
DIS advises running it at least once a week.

## X56-11 PRICE OVERRIDE REPORT

 

### How To Run

From the Report Menu (X5-6), select option 11, Price Override Report.
The date range selection screen appears.

ABC-AG,AUTO, CONS & TRUCK CO PRICE OVERRIDE REPORT 5680-101
Division: A

Select part sales to include on the override report:

From: 121994 To: 121594

Enter-Continue Cmdl-End jeb

 

0 Make your selection of dates and press [Enter]. The job is placed on the
job queue. Press [Enter] again to return to the menu.

RELEASE 2.1 LU


An example of the Price Override Report follows:

LEE'S TRACTOR SALES, INC. PRICE OVERRIDE REPORT

LYNDEN, WA

cr00101

cro0101
ervo1o1
er90102
crea102
crso1o2
700102

apsiss9a
12/18/94
22/18/94
22/15/94
32/15/94
22/15/94
32/15/98

B 12/25/94 to 12/25/94

Fart number

19726
at1190
11190
10835
31543
41245
7634

Date 12/25/24
Time 9.41.17

 

 

Page 1
1x5680-201


Notes:

‘

RELEASE 2.1 \

## CHAPTER X56-12

POS DOCUMENTS BY GROUP REPORT

### Introduction

This job produces a report that breaks down all POS documents by group.
The user is able to specify which documents are included in the report by
group and by date. Each transaction included in the report is totalled and
broken down into six separate categories.

### How To Run

From the Point of Sale Reports Report Menu (X5-6), select option 12,
POS Documents By Group Report. Enter your division and password at
the security gate and press (Enter]. The following screen appears.

POS Documents by Group X56C0-101 1

++ 000000
 0000c0

If Group Codes are plank, then All Group Codes will be included.

### [2] X56-12 Pos Documents By Group Report

O Enter a range of dates in the From Date and To Date fields in the form
of MMDDYY. April 1, 1995, for example, would be entered as
"040195." Documents posted within this range will be included in the
report.

O In the Group Codes fields, enter any group codes to be included in the
report. If these fields are left blank, the report will include all groups.
Press [Enter]. The report will be generated and sent to the system
printer.

An example of a POS Documents by GroupReport follows.

‘URE'S RENTAL COMPANY POS DOCUMENTS BY GROUP AND DOCUMENT & BATE 3/22/95 PAGE
LYNDEN. WA From Dae 1/01/90 Thru 1/01/96 TIME 20.00 5400-302
GC Document Addr¥ Name Discount Sales Tax Total

oi rooite cael samor car {
oa ertoiea tasoot Zener ent

01 GT00103 GRADO1 LEROY GRADY
83 Croo104 GRADO1 LEROY GRADY

91 RLOOLOZ CASHA ‘THANK YOU FOR YOUR BUS
02 RLOG103 © CASHA THANK YOO FOR YOUR BUS
01 ROGO100 SHAHOL SHAW PAPER SUPPLY

50 RLOOLOL 009005 Bommie Pennerton Const

 

RELEASE 2.1 Le

## CHAPTER X61-1

IMMEDIATE BACKUP

### Introduction

An immediate backup is appropriate if you want to do a critical job, such
as monthly billing, in the middle of the work day. If a critical job is
already underway, immediate backup cancels itself; if not, the system
checks for active jobs and gives you a chance to ask people to sign off or
cancel the jobs manually. Although you may select immediate backup to
tape and initialize the tape at the same time, you will probably want to
request backup to disk and move it to tape later. A dedicated system is
required only during the backup to disk. Work can continue while backups
are moved to tape.

You can initialize a tape for immediate backup in option 6, Prepare a Tape
for Immediate Backup, at any time and have it ready. Immediate Backup
expects volume ID, “IMMEDIATE.”

Active Jobs

The Immediate Backup program checks for active jobs. If any of the
following critical jobs are active, backup is canceled and you are advised
again later:

— Monthly Billing

any terminal).

— Post Source Documents

—- Accounting End of Month

— Payables File Maintenance

~ General Ledger File Maintenance

~ Price Tape Update

— Parts End of Month Procedures

— Point of Sale End of Month Procedure

— Restore Bearing Interchange

Tf the system finds other active jobs, they are listed and you can decide
whether to wait, contact users, or cancel the jobs.

## X61-1 IMMEDIATE BACKUP

 

Note: Don't forget that data may be lost when a job is canceled.

 

CASE Communications & Backup

No jobs that use data files can be running during the DIS Business System
backup. The SupportPRO business system interface (BSI) is such a job
and it cannot be left active overnight or backup will fail. There is a BSI
job active for each SupportPRO client. Every night before you leave,
follow these instructions to allow backup to complete.

O Onecach Rumba-DIS session, obtain a sign-on screen.

O Stop Case Communications.

O Exit the SupportPRO application. This cancels the BSI job so backup
will complete.

O Tum off the monitor, but leave the PC running. If you want to turn off
the PC at the end of the day, follow the instructions for exiting
Windows.

O To restart SupportPRO in the morning, find the SupportPRO CD icon
in the ABC group, and double-click on it. The SupportPRO application
will start.

RELEASE 2.1 Lo


 

### How To Run

From the Backup & Restore Files Menu, select option 1, Immediate
Backup.

Select File Set Screen

Immediate Backup

1sSelect

Opt File Description

Set
1k Created from Conversion
- 2 Created from Conversion

F3-Exit F12=Previous

 

On this screen, select one or more file sets for immediate backup. On
the next screen, you will specify disk or tape backup.

SECURITY & CONFIGURATION


 

Select Device Screen

Immediate Backup

File Set E Created from Conversion

dsSelect

Opt Device
1 Disk

_ Tape TAPOL Initialize (y/N) N

F3=Exit F12=Previous

 

Disk

Tf you select “Disk,” the file set is backed up to disk only. The backup may
be moved to tape later. A dedicated system is required while the file set is
backed up to disk, but work can proceed as usual while the backup is
moved to tape.

RELEASE 2.1 oe


 

Tape

If you select “Tape,” the file set is first backed up to disk, then saved to
tape, after which the disk backup is deleted. A dedicated system is
required for the entire process.

Initialize Y/N '
You may initialize tapes for immediate backups using option X61-6,

Prepare Tape for Immediate Backup, which will save some time, or you

may select the option to initialize the tape at the time of the backup. The

system uses the Volume ID, “IMMEDIATE.”

 

SECURITY & CONFIGURATION


Notes:

to

## CHAPTER X61-2

WORK WITH AUTOMATED BACKUP SCHEDULES

### Introduction

Use this option to schedule backups for each file set and end of day jobs
for each division. It is not necessary to repeat this initial setup work unless
you want to change the schedule or you add another division and need to
schedule end of day jobs for it.

Backup Schedule for File Set

A backup schedule consists of the following information:

The day's work you want to back up.

1. The tape device and a time for backup to begin.

2. A time for reminder messages about inserting the backup tape and 1 or
2 people to send it to.

3. The time that should be allowed before the system cancels active, non-
critical jobs and a time interval between warning messages.

End of Day Jobs by Division

The following End of Day jobs, which are run after backup, can be
scheduled by division:

= Accounting End of Day. A S/36 printer ID can be designated.

= Parts End of Day. A S/36 printer ID can be designated.

= Index Rebuild. Indexes are rebuilt for the file set. If they have already
been run when the system processes a division, they will not be run
again. The following indexes are rebuilt: Marketing, Point of Sale,
Receivables, Vendor.

Active Jobs

You can configure backup to cancel active, non-critical jobs after a certain
waiting period. In addition, the system can send warning messages to


X61-2 WORK WITH AUTOMATED BACKUP SCHEDULES.

 

active users at the time intervals you select. Users should be informed
about the possibility of losing data if active jobs are canceled.

Critical Jobs

Backup will not proceed if one of the following critical jobs is active:

o Monthly Billing

any terminal).

o Post Source Documents

o Accounting End of Month

o Payables File Maintenance

o General Ledger File Maintenance

o Price Tape Update (
o Parts End of Month Procedures

o Point of Sale End of Month Procedure

o Restore Bearing Interchange

If critical jobs remain after 5 hours, backup is canceled.

CASE Communications & Backup

No jobs that use data files can be running during the DIS Business System
backup. The SupportPRO business system interface (BSI) is such a job
and it cannot be left active overnight or backup will fail. There is a BSI
job active for each SupportPRO client. Every night before you leave,
follow these instructions to allow backup to complete.

0 On each Rumba-DIS session, obtain a sign-on screen.

RELEASE 2.1 LU

## X61-2 WORK WITH AUTOMATED BACKUP SCHEDULES

 

O Stop Case Communications.

O Exit the SupportPRO application. This cancels the BSI job so backup
will complete.

O Turn off the monitor, but leave the PC running. If you want to turn off
the PC at the end of the day, follow the instructions for exiting
Windows.

O To restart SupportPRO in the morning, find the SupportPRO CD icon
in the ABC group, and double-click on it. The SupportPRO application
will start.

 

SECURITY & CONFIGURATION

### How To Run

O From the Backup & Restore Files Menu, select option 2, Work with
Automated Backup Schedules. The file set selection screen is
displayed.

File Set Selection Screen

A-DIS TEST Work with Automated Backup Schedules

File
Set

2sChange S=Edit Description 12=Work with EOD Jobs
Opt File Deseription MTWTFSS Time £OD
Set Jobs

z Created from Conversion YY YY YNN 23:00
z Created from Conversion YY Y¥YNN_ 23:00

F3=Exit  F12=Previous

 

In the column labeled “EOD Jobs,” you will see a “Y” if any End of Day


 

job has been scheduled in any division.

O Select the file set with 1 of the options: 2=Change, 5=Edit Description,
or 12=Work with EOD Jobs. Each option is described on the following
pages. If you are setting up an automated schedule for the first time,
you will probably want to use each option.

2=CHANGE

Use this option to change the schedule and designate the person(s) who
receive the reminder to insert the backup tape. In addition, you can specify
the amount of time you want to allow active jobs to continue.

SECURITY & CONFIGURATION


 
 

Work with Automated Backup Schedules

  
   
  
  
   
   

2eChange S=Edit Description 12=wWork with OD Jobs

Opt File Description MTWTESS Time EOD
Set Jobs
2 = Created from Conversion YY YYYNN 23:00
z Created frem Conversion YY YYYNN 23:00

   

F3=Exit  Fl2=Previcus

  

 

O On the file selection screen, select the file set with 2=Change. The
schedule screen is displayed.


X61-2 WORK WITH AUTOMATED BACKUP SCHEDULES [:

  

Change Automated Backup Schedule Screen

A-DIS TEST change automated Backup schedule DSDLEIR

File Set = Created from Conversion

Save files from M T WoT F S$ §
YY ¥ ¥ ¥ NN

Tape Device . TAP01
Time (umm 2300

Tape Reminder Message:
Time (HHMM) . 1630
To User... QSYSOPR
Or User . . . QSYSOPR

Cancel active jobs after . 10 Minutes
Warn active users every .. 2 Minutes

F3=Exit F12=Previous

 

The values illustrated on the screen above are the defaults. Press FI=Help
in any field to find out more about it. The prompts are described below.
‘When you are done, press [Enter], then F12=Previous to return to the file
selection screen or F3=Exit to return to the Backup & Restore Files Menu.

Save files from M T W T F § §

M=Monday, T=Tuesday, W=Wednesday, etc. Each of these fields requires
Y (Yes) or N (No).

SECURITY & CONFIGURATION


 

 

 

O To schedule a backup of Monday's data, type “Y” in the column labeled
“M.” Repeat for other days of the week.

Example: Y=Yes, backup of Monday's data is scheduled. Backup of the
selected file set is scheduled to begin at the time specified on this screen.
N=No, backup of Monday's data is not scheduled. AY" in Monday’s
field and a time of 0145 means that a backup of Monday's data is
scheduled Tuesday morning at 1:45 a.m.

Military time is used. The clock runs from 8:01 A.M. on the first day until
8:00 A.M. on the second day. If backup begins at 8:00 Monday morning,
the system expects the tape labeled “Monday.” If backup begins at 8:01, it
expects Tuesday's tape. If backup is scheduled after work begins on
Tuesday, it will contain work from both days.

Tape Device . TAPOL
10 characters. Required. System name of the backup device, such as
"TAPOI."

Time (HHMM) . 2300

4 digits. Time (hhmm). Required. Time when backup is scheduled to
begin. The system cancels active, non-critical jobs after the time interval
specified on this screen. Jf critical jobs, which cannot be canceled, are still
active after 5 hours, backup is canceled.

Tape Reminder Message:

Time (HHMM) . 1630

4 digits. Time (hhmm). Required. Tape reminder messages are included to
make sure a tape is in the drive before backup starts. Messages may be
sent at any time of day to | or 2 people. Ifa tape is not present, a message
is sent to the system operator's queue.

To User ... QSYSOPR
Or User ... QSYSOPR


 

10 character user [Ds. Required. Press F4=Prompt to select from a list. At
the specified time, the first person receives a message reminding them to
insert the backup tape. If the message cannot be delivered to the first user,
it is sent to the second user.

Cancel active jobs after . 10 Minutes

2 digits. Time (mm). Required. If the system finds one or more active jobs
that may cause the backup to fail, messages are sent to the workstation.
Enter the total number of minutes you want to allow before non-critical
jobs are canceled. Critical jobs, which are listed in the Introduction of this
chapter, are not canceled.

Warn active users every... 2 Minutes

2 digits. Time (mm). Required. If the system finds one or more active but
non-critical jobs, messages are sent to the workstations warning the users
that backup is scheduled. Enter the number of minutes between warnings.

SECURITY & CONFIGURATION


 

5=CHANGE DESCRIPTION

A-DIS TEST Work with Automated Backup Schedules

File
Set

2=Change §=Edit Description 12sWork with EOD Jobs

Opt File Description MTWTFSS$ Time EOD
set Jobs

5 o£ Created from Conversion YYNYYNN 1:45

z Created from Conversion YY YYYNN 23:00

F3-Exit F12=Frevious

O From the file selection screen, select a file set with 5=Edit Description.
The following window opens:
LO


 

Edit File Set Description Window

 
      

Edit File Set Description

 

Created fram Conversion

   
  

File Set E

    

F12=Previous

 

FRsExit

  

O Type over the current description.
O Press [Enter] to accept the description and return to the file selection

screen,

SECURITY & CONFIGURATION


X61-2 WORK WITH AUTOMATED BACKUP SCHEDULES C .

 

12=WORK WITH EOD JOBS

A-DIS TEST Work with Automated Backup Schedules

File
Set

2=Change 5=Edit Description 12=Work with EOD Jobs

Opt File Description MTWTFSS Time EOD
Set Jobs

Equipment Sales & Rentals YYNYYNN 1:45
Created from Conversion YY ¥YYYNN 23:00

F3=Exit Fi2=Previous
Record changed.

 

0 From the file selection screen, select a file set with 12=Work with EOD
Jobs. The division selection screen is displayed.

RELEASE 2.1 LO


 

Division Selection Screen

A-DIS TEST work with End of Day Jobs DSGODFR

File Set E Equipment Sales & Rentals
MTWTFSS
Backup schedule: YY NY YNN

Division

2=change

Opt Division name

NW EQUIPMENT SALES
DEALER SALES & SERVICE, LTD.
ABC RENTALS COMPANY

PisExit F12=Previous

 

O Select a division with 2=Change. The End of Day Scheduling screen is
displayed.

SECURITY & CONFIGURATION


X61-2_ WORK WITH AUTOMATED BACKUP SCHEDULES

End of Day Scheduling Screen

A-DIS TEST End of Day Scheduling

File set & Equipment Sales & Rentals
MTWTFSS
Backup schedule: YYNYYNN

Division A NW EQUIPMENT SALES

End of Day Job MTWTFSS $/36 Printer
Accounting End of Day NNNNNNW

Parts End of Day NNNNNNW

Index Rebuild NNNNNNN

F3sExit Fl2=Previous

Accounting & Parts End of Day. On the top line, the backup schedule for
the file set is displayed. To schedule an End of Day job, simply enter a
“Y” in a corresponding day.

8/36 Printer IDs. Each printer attached to your system has an AS/400
name and a S/36 name. On this screen, you need to know the S/36 names.
Here’s how you can find a table of AS/400 and S/36 printer IDs:

O Ata menu, type: DSPS36 and press [Enter].
CC


 

O Select the option for S/36 printer IDs.
O Find the AS/400 printer ID and its corresponding S/36 printer ID.

Index Rebuild. To schedule Index Rebuild, which takes place after
backup, enter a “Y” in the corresponding day. The following indexes are
rebuilt:

1, Marketing

2. Point of Sale

3. Receivables

4, Vendors

Note: Index rebuild is done for ali divisions at the same time. If it has

been scheduled and run for one division, it is not run again even though it
is scheduled for other divisions within the same file set.

SECURITY & CONFIGURATION


Notes: oo

J
RELEASE 2.1 NL

## CHAPTER X61-3

CREATE DAILY BACKUP TAPES

### Introduction

Use this option to initialize and label tapes that will be used for daily
backups. You may create tapes for as many days as you need. You will be
prompted to insert the next day's tape. You may use this option to create
backup tapes to replace ones you want to keep, such as the backups that
follow Monthly Billing, Accounting End of Month, or End of Year.

The backup system uses the same tapes on a daily basis: Monday's data is
backed up to Monday's tape, which is labeled and recognized as
MONDAY. A different tape is needed for every day you want to schedule
backup. To prepare tapes for immediate backups, use option 6 (see

## CHAPTER X61-6

## ).

Backup uses a 24-hour clock (military time). Noon is 12:00; midnight is
24:00. Backup time is from 8:01 on the first day until 8:00 the next day.
The system expects Monday's tape from 8:01 AM. on Monday until 8:00
A.M. on Tuesday.

Files on backup tapes are active for 7 days. If active files are found,
backup will append (add to the end) the next backup. After 7 days, the
system will re-initialize the tape with the same label.

Examples. If backup time is scheduled for 23:59 on Monday, the system
expects Monday's tape and backs up Monday's data at one minute until
midnight. If backup is scheduled for 2:00, the system expects Monday's
tape and backs up Monday's data at 2:00 Tuesday morning. At 8:01
Tuesday morning, the system expects Tuesday's tape. If backup is
scheduled for 14:00 and it is Tuesday, the system expects Tuesday's tape.

## X61-3 CREATE DAILY BACKUP TAPES

 

oo
\
O From the Backup & Restore Files Menu, select option 3, Create Daily
Backup Tapes. The following screen is displayed:
Create Daily Backup Tapes DSF3PVR

Using Tape Device... .
Initialize Backup Tapes for
Monday Tuesday Wednesday Thursday Friday Saturday
(ya)

¥ ‘ y x x x (

F3eExit F12=Previous

 

© Furnish the name of your tape device, usually TAPO1.

G To create a backup tape for Monday's data, type “Y” in the column
labeled “Monday.”

O Repeat for other days of the week.

O When you are done, press [Enter]. The following window opens:

RELEASE 2.1 CO


 

Insert Tape

In Tape Device TAPO1

Place tape labeled Monday

Tape will be initialized!

Press Enter to continue

F3=Exit F12=Previous

 

O Clearly label a tape as Monday’s backup, and insert it into the tape
drive.
O Press [Enter] to proceed with the initialization.

SECURITY & CONFIGURATION


Notes:

## CHAPTER X61-4

RESTORE FROM BACKUP

### Introduction

Use this option to restore a file set from disk or tape. The DIS Backup
system keeps a log of all backups that have ever been done and what
happened to them, whether they are on disk, tape, or have been deleted and
are unavailable. If the backup you want is on disk or tape, it can be
restored.

Altention! Customers who have used previous versions of the DIS
Business System: Restoring data files no longer involves deleting the file
set you are currently using; in fact, the option to Delete Data Files has
been disabled. If you need to remove a file set, such as Z-files
permanently, the Response Line can help you.

Restoring a file set is as simple as selecting the backup from a list in
Restore from Backup.

WARNING!
If a backup appears in the list with a blank
File Location (neither On Tape nor On Disk),
it could be incomplete and should not be
restored.
|

What if I Restore the Wrong Backup?

As long as you find out before the next backup, you can "undo" the
restore. Before a file set is restored, the system backs up the current file
set as an “Undo” save file and leaves it on the disk until the next regularly
scheduled automated backup. If you have restored the wrong backup or if
you simply want to return to the current data after running some reports
from an old backup, all you do is press a function key. See F10-Undo
Restore.


X61-4 RESTORE FROM BACKUP Co

 

### How To Run

O From the Backup & Restore Files Menu, select option 4, Restore from
Backup. The file set selection screen is displayed.

File Set Selection Screen
Restore from Backup

Backup
bate

Backup
Date File Location

7/47/96 on Disk
T17/96 on Tape
T/01/96 *Deleted-Unavailable

Fi=Exit Fl0=Undo Restore F12=Previous

 

Q Select the file set you want to restore with 1=Select. In this example, a
backup that is on tape has been selected. The Restore from Backup
screen is displayed.

RELEASE 2.1 \

## X61-4 RESTORE FROM BACKUP

 

Restore from Backup Screen

Restore from Backup

Imsert Backup tape labeled: WEDNESDAY
7/27/96

Tape Device... .

Press Enter to continue.

F3cExit F12=Previous

 

1 Verify the backup and tape device before you press [Enter].

Restoring a file set includes the following steps:

1. The file set you are currently using is backed up to disk and kept until
the next regular backup. Until the next regular backup, you can “Undo”
the restore and return to the current file set simply by pressing
F10=Undo Restore from the file selection screen. During this phase, the
Status message at the bottom of the screen is: "Copying current
condition of file set E before continuing restore..."

SECURITY & CONFIGURATION


 

2. The backup you requested is restored. The status message is:
"Restoring File set E ..."

RELEASE 2.1 LC


 

F10=UNDO RESTORE

‘When you restore a file set, the current file set is backed up to disk to have
on hand as an “extra copy.” The extra copy is deleted ar the next regularly
scheduled automated backup. Meanwhile, you can “undo” the restore. The
extra copy can be put back in place as your current file set, replacing the
file set you restored earlier. This feature makes it more convenient to
restore a file set simply to run a report you may have forgotten.

O To “undo” a restore, start at the file set selection screen:

    
    

 

A-DIS TEST Restore from Backup DSIODFR

  
   
   
  
  

 

Opt File Backup

Set Date Time By Tape Id File Location
-~ & T1T/96 14:33 EBS On Disk
- &£ 7/17/96 10:34 EBS WEDNESDAY On Tape
- & 7/01/96 9:21 EBS *Deleted-Unavailable
F3=Exit Fl0sUndo Restore F12=Previous

       

 

SECURITY & CONFIGURATION


O Press Fi0=Undo Restore. You'll see a list of file sets that have been
saved temporarily because of a Restore operation.

A-DIS TEST Undo Restore

i=Select.

Opt File Set Date Restored at
1 06& 082096 1:14
2 062096 17:22

FISExit  Fi2=Exit

O Select the file set you want to reinstate with 1=Select and press [Enter].
During the "undo" operation, you'll see status messages at the bottom
of the screen, such as: "Deleting File set E in preparation for restore... "

## CHAPTER X61-5

WORK WITH BACKUPS

### Introduction

Work with Backups maintains a log of all backups and where they are
(disk, tape, deleted, etc.). From this log, you can select any backup on disk
and delete it or move it to tape.

### How To Run

From the Backup & Restore Files Menu, select option 5, Work with
Backups. The file set selection screen appears.

File Set Selection Screen

work with Backups

4=Delete 7=Move to Tape

Opt File Backup
Date Time By Tape Id File Location
7/17/96 10:34 EBS On Disk
7/01/96 9:21 EBS *Deleted-Unavailable

F3eExit F12=Previous

## X61-5 WORK WITH BACKUPS

 

O Selecta file set with 4=Delete or 7=Move to Tape.

RELEASE 2.1 LL


 

7=MOVE TO TAPE

On the file selection screen, select a file set with 7=Move to Tape. The
Move Saved File Set to Tape screen is displayed.

Move Saved File Set to Tape Screen

 
 

Move Saved File Set to Tape

 
  
  
 
 
   
   
 

 

Fileset 2... ..-0: 5
Backed up on... 7/17/96
at ee : 10:34:33
to Tape device ..... TAPOL

Tape Volume... | -
Initialize Tape (y/N) . .

F3=Exit F4=Prompt Fi2=previous

 

 

 

O Furnish the name of your tape device, which is usually TAPO1.
O Furnish the tape volume ID. Press F4=Prompt to select from a list of

SECURITY & CONFIGURATION


X61-5 WORK WITH BACKUPS:

 

IDs.

O If you want to initialize the tape before moving the backup, answer "Y"
(Yes) to "Initialize Tape (Y/N).

O Press [Enter]. A prompt similar to the one illustrated below is
displayed:

Insert Tape

In Tape Device TAPO2

Place tape labeled WEDNESDAY

Press Enter to continue

it FL2=P:

 

Q Insert the requested tape, and press [Enter]. (

RELEASE 2.1 LO

## CHAPTER X61-6

PREPARE TAPE FOR IMMEDIATE BACKUP

### Introduction

You can save time by using this option to initialize tapes to have on hand
when you need to do an immediate backup. The label for an immediate
backup tape is IMMEDIATE.

### How To Run

From the Backup & Restore Files Menu (X6-1), select option 6, Prepare
Tape for Immediate Backup.

Prepare Tape for Immediate Backup X6160-101

Tape Device . . .

 

O Provide the name of the tape device, usually TAPO1.
1 Press [Enter]. You'll see a status message:
61600
Preparing tape for immediate backup in TAPO] . ..


Notes:

RELEASE 2.1 LO

## CHAPTER X61-7

RELOAD DATA FILES

### Introduction

This menu option is used to relo,
has been reloaded. It can be use
reload since the file that keeps t

‘d anytime, but is especialh
he

ad data from a backup tape after a entire system
'y helpful after an entire
le status of backups will not be current.

If it is used at any other time, make sure

the backup is readable because this

 

option deletes the current set of data files, if any.

To verify that a backup is readable, follow these steps:
1. Atacommand line, type: DSPTAP and press F4=Prompt.

Display Tape (DsPTap)

Type choices, press Enter.

tap0l <@— name

Volume identifier ©. | *MOUNT=D Character value, -mounTep
File label *ALL .
Sequence number 2 2 | 1 1-9999
Data type ‘savest “+— *LABELS, *SAVRST
Outpue . *, “PRINT
End of tape option. 2 | | *REWIND *REWIND, *UNLOAD
Bottom
F3-Exit  F4=Prompt FS=Refresh Fl2=cancel F13=How to use this display

F24=More keys

2. Enter the name of your tape device, such as: tapo1.


2 CHAPTER X61-7 © RELOAD DATA FILES RELEASE 2.2
3. For "Data type," enter: *savrst.
4. Press [Enter]. A list of your saved data files is displayed.
Display Saved Objects - Tape
Library - ttt Qs3é6F Release level V3R2M0
BSP 2 ee ee tt FE 1 File sequence L
Volume ID - eet IMMED Data compressed Yes
Expiration date .- +? LA/i7/97 Data compacted . No
Save command. - - + = SAVOBT Objects displayed 6
Save active ---- i *NO
File label ID. - - * Qs36F
Save date/time - . + = 1i/a1/97 16:20:53
type options, press Enter.
S=Display saved data pase file members
opt Object Type Attribute Owner size Data
E.ANT *FILE PF QSECOFR 29184 YES
E.ANTLO *PILE LF QSECOFR 20992 YES
B.ATM *FILE PF QSECOFR 23040 YES
‘E.BAA *PILE PF QSECOFR 32800 YES
E.BAH *FILE PF QSECOFR 12800 YES
E. BAHL *FILE LF QSECOFR 10752 YES +
F3=Exit. Fl2=Cancel

 

5. If the tape is OK, press F3=Exit and go to the Security & Configuration

Menu.

6. Make sure all users are signed off and no

other jobs are running.


SECURITY & CONFIGURATION CHAPTER X61-7 ¢ RELOAD DATA FILES 3

 

COMMAND MENU: X61 BO
{c) DIS Corp.

 

+ Imnediate Backup
- Work with Automated Backup Schedules
. Create Daily Backup Tapes

4. Restore from Backup
5. Work with Backups

6. Prepare Tape for Immediate Backup
7

+ Reload Data Files

23, Return to Security & Configuration Menu

Ready for option number or command
=> 7

 

 

 

—!

From the Back Up & Restore Files Menu, select option 7, Reload Data Files. The
following screen appears.

 

RELOAD DATA FILES 6170-001

tne rt ee WARNING ere en beans
This job will DELETE ALL DIS data files on the disk including
multiple file sets before reloading from your backup tape.

Make sure to insert the correct backup tape before continuing.

Also make sure all users are signed off and no other jobs are
running before you continue!

 

NOTE: You may want to display the contents of the backup tape
to confirm it is readable befere running this procedure!

Cmdi-Cancel job Cmd2-Continue

 

 

If you're sure you're ready to continue, press Cmd2-Continue; otherwise, press
[Cmd1} to cancel the job.

## CHAPTER X61-7

## ¢ RELOAD DATA FILES

Notes:

## CHAPTER X63-1

OPT GENERAL LEDGER MENUS

OPT GENERAL LEDGER MENU ONE (X631)

‘conaeaND
(c) DIS Corp

### Opt General Ledger Menu

Automatic Costing 1. Do not split "D' edit code automatic
transactions by document number
Split 'D’ edit code automatic transactions by
document number at the end of the batch
Split 'D' edit code automatic transactions by
documen: number sorted in the batch

 

Accounting Print the Subledger Balance Report during end of day
End of Day Do mot print the Subledger Balance Report during
end of &

23. Return to OPTDES Master Menu
24. OPT General Ledger Menu Two

Ready for option number or command

  

SECURITY & CONFIGURATION

## X63-1 OPT GENERAL LEDGER MENUS

Automatic Costing

Parts and labor automatic costing transactions are normally grouped by
general ledger account in order to create as few as possible in each batch.
This option allows you create a set of automatic transactions for each
document number instead.

Menu option #1: Do not split 'D' edit code transactions (parts and labor)
by document number .

Menu option #2: Split ‘D' edit code transactions (parts and labor) by
document number, These automatic transactions sort to
the bottom of the batch.

 

Menu option #3: Split 'D’ edit code transactions (parts and labor) by
document number. These automatic transactions sort
in the middie of the batch by document.

Accounting End of Day

‘The Subledger Balance Report prints all subledger and general ledger
balances side-by-side for easy comparison. ‘This report is helpful to
identify posting problems which have thrown the subledgers cut of balance
with the general ledger. It is normally printed during each accounting
end of day,

Menu option #3: Print the Subledger Balance Report during accounting end
of day.

Menu option #4: Do not print the Subledger Balance Report during accounting
end of day. (it is can still be requested from the menu.)
LO


OPT GENERAL LEDGER MENU TWO (X6312)

COMMAND
ic} DIS Corp

MENU: X6312

GENERAL LEDGER MENU TWO

Restricted
Accounts

Formatted Fin,
Report

Bnd of Month

23.


- Do not include restricted accounts on

the chart of Accounts

. Include restricted accounts on the Chart

of accounts

Unit sales counters include all sale documents
Unit sales counters only include #* sale documents

Do not page break register when account # changes
. Page break register when account # changes

Return to OPT General Ledger Menu One
OPT General Ledger Menu Three

Ready for option number or command

SECURITY & CONFIGURATION


X63-1 OPT GENERAL LEDGER MENUS.

 

Restricted Accounts

Restricted accounts are not valid for future postings. If restricted
accounts contain historical balances they are included in financial

reports as necessary. ‘This option allows the choice of whether these
restricted accounts are included on the x14-3 Chart of Accounts,

Menu option fl: Do not include restricted accounts on the Chart of Accounts.

Menu option #2: Include restricted accounts on the Chart of Accounts.

 

 

Formatted Financial Reporting

‘Some formatted financial reports print totals of sale units for
each general ledger account number. This option controls whether
general transactions in the unit sale accounts increment the sales
counter

Menu option #3: Include all unit sale transactions when determining
unit sale counters.

 

Menu option #4: Only include a unit sale transaction in the unit sale
counter if the ninth and tenth characters of the document
number are equal to '#*'.

 

LU


Accounting End of Month

‘This option allows the choice of whether the general ledger register which
prints during accounting end of month should begin 2 new page every time
the account number changes

Menu option #7: Do not begin a new page when the account number changes.

Yienu option #8: Begin a new page when the account mumber changes.

 

 

 

SECURITY & CONFIGURATION


OPT GENERAL LEDGER MENU THREE (X6313)

COMMAND
{c) DIS Corp

OPT GENERAL LEDGER MENU THREE

Subledger
Balance
Report

Journals EOw
(Journals
Installed}

23.

Do not include scheduled accounts on the
Subledger Balance Report

Include scheduled accounts on the Subledger
Balance Report

Accounting journals are not instatled
Account ‘ournals are instalied

Aecting End of Month, Journals print in Date order
Aecting End of Month, Journals print by Document#
Accting End of Month, NO journals print automatically

Return to OPT General Ledger Menu Two

Ready for option number or command

 
LL


Subledger Balance Report

‘General Ledger Accounts that are scheduled using one of the special schedule edit
sedes of V, U, N, 7, ox L may want to be excluded from appearing on the Subledger
Balance Report. This option allows you the choice as to whether scheduled
accounts are included on this report

Menu option #2; Do not include scheduled accounts on the Subledger Balance
Report.
Menu option #2: Include scheduled accounts on the Subledgez Balance Report

 

Journals

‘The DIS accounting system allows for opticnal journal posting. If accounting
journals are installed, the "id" portion of each transaction is used to
identify the journal to which the transaction is pested. Both the accounting
end of day reports and the general ledger register will print in journal id
order

NOTE: This is a major change to the accounting system (and affects both posting :
and reporting.) Please cali the Response Line and discuss this option
before installing.

Menu option #5: Accounting journals are not installed.

Accounting journals are installed

 

SECURITY & CONFIGURATION


 

Journals EOM

If the option to do JOURNALS is installed (option #4], these options
will determine the format by which journals will print at the close
ef Accounting End of Month.

Menu option #5: Journals will print in Transaction Date order during EOM

Menu option #6: Journals will print in Document Number order during EOM

Menu option #7: Journals will NOT print automatically during End of Month

 

CO

## CHAPTER X63-2

OPT MARKETING MENU

OPT MARKETING MENU (X632)

‘COMMAND: MENU: X632
(c) DIS Corp

 

OPT MARKETING

Letter Writer Print the name and the salutation
Do not print the name nor the salutation
Print the name but not the salutation

Address Labels - print extended name after standard name
Extended Name Print extended name before standard name

Target Marketing . Target Marketing has not been installed
7. Target Marketing has been installed

Return to OPTDIS Master Menu

Ready for option number or command

TNQUIRY WH

## X63-2 OPT MARKETING MENUS

 

Letter Writer

The Letter Writer automatically produces form letters which can contain
the customer's name as well as a salutation. (e.g. DEAR LEROY GRADY)
This option allows you to decide whether or not the name and/or the
salutation should print.

Menu option 1: Print the customer name and the salutation.

Menu option 2: Do not print the customer name and do not print the salutation.

nu option 3: Print the customer name but not the salutation.

 

Address Labels - Extended Name

This option will allow you to choose whether the extended name will print
after the regular name or before the regular name.

The U. S. Postal Service prefers the extended name or "attention" line to be
the first line of the address block. They also prefer the extended address
to print on the same line as the normal address.

Menu option 4: GRADY CONSTRUCTION Menu option 2: LEROY GRADY
LEROY GRADY GRADY CONSTRUCTION
1234 STH AVE sO 1234 5TH AVE SO SUITS 101
SUITE 102 SPRINGDALE WA 98226
SPRINGDALE WA 98226

 

{
RELEASE 2.1 WW


Target Marketing

‘Target Marketing is an application available from the X4 Marketing Menu that
will enhance your sales department’s ability to update and track potential
customers.

Memu option #6: ‘Target Marketing has not been installed.

anu option #7: Target Marketing has been installed.

 

SECURITY & CONFIGURATION


Notes:

## CHAPTER X63-3

OPT PARTS MENUS

OPT PARTS MENU ONE (X633)

COMMAND
(s) DIS corp

PARTS MENU ONE

 

2MR Turn COS is not reduced by priority orders
Rate 2. COS is reduced by priority orders

Superseded Do not include superseded parts on a suggested stock order
Parts 4. Include superseded parts on a suggested stock order
Process supersession chain on a suggested stock order

Reservation Fill reservations in date/time order

Priority Fill reservations in customer, warranty, internal order
All priority orders are filled before stock orders
Like #8 only in cust, warr, int order within those groups
Like #7 only in priority, stock order within those groups

23. Return to OPIDIS Master Menu 24. OPT Parts Menu Two

Ready for option number or command

 

PMR Turn Rate

The Parts Management Report calculates an inventory turn rate by dividing
the net price of total part sales hy the net price of ending inventory.
This option allows you to decide whether or not to reduce the net price of
tota? parts sales by the total priority orders for the period.

Menu option 1: Do not reduce the total parts sales net by the total of the
priority orders.

Meny option 2: Reduce the total parts sales net by the total of the priority

orders

## X63-3 OPT PARTS MENUS

Superseded Parts

‘The suggested stock order process selects parts which should be ordered
based upon past sales information. This option allows you to decide whether
er not to include superseded parts on suggested stock orders

Menu option 3: Do not include superseded parts on suggested stock orders.
Menu option #4: Include superseded parts on suggested stock orders.

Menu cpticn #5: Process supersession chain on a suggested stock order and
use all sales history from all parts within the supersession
chain to determine the order quantity; then order the most
recent part in the chain,

 

Reservation Priority

farts reservations are filled according to a reservation fill priority number
of 1 - 6 that is assigned when an order is processed. This option allows you
to cheose which types of reservations get which fill priority number.

Menu option #6: All reservations get 2 fill priority of 1 and are therefore
filled in date/time order

Menu option #7: Customer reservations get a fill priority of 2, warranty
reservations get a 3, and internal reservations get a 4.

Menu option 48; Priority reservations get a 1, and stock reservations get a 2.

Menu option #9: Cust res with a 'P' get al; warr res with a 'P' get a 2;
int res with a get a3; cust res with an 'S' get a 4;
warr ree with an ‘S' get a 5; int res with an ‘S' get a 6.

Menu option #10: Cust res with a ‘P’ get al; cust res with an 'S' get a 2;
warz res with a 'P* get a3; warr res with an ‘S' get a 4;
int res with a 'P' get a5; int res with an get a 6.

 
CL


OPT PARTS MENU TWO (X633-2)

‘COMMAND
ic) DIS Corp

Supersession
Reservation

Parts Posting
and Maintenance

Average Costing

24.

MENU: %6332 INQUIRY WH

PARTS MENU

Do not fill reservations from superseded parts
Fill reservations from superseded parts

3. Do not use a part transaction security code
. Use a part transaction security code for

every quantity adjustment

. Use a security code for the first gty adjustment

Average costing for parts inventory is not installed
Average costing for parts inventory is installed

Return to OPT Parts Menu One
OPT Parts Menu Three

Ready for option number or command

 

SECURITY & CONFIGURATION


Supersession Reservations —

‘when you correct an order before receiving it, you can specify a supersession
part number as receipted instead of the original number. If this is done

the system will not normally “fill* reservations of the original part number
using quantities of the new superseding part number. This option allows you

to fill these reservations using the superseding part quantities.
Menu option 1: Do not fill reservations from superseded part quantities.

lenm option 2: Fill reservations from superseded part quantities.

  

Parts Posting and Maintenance Security

‘@n option is available to add an extra level of security at Parts Posting and . (
Maintenance. This new security code can restrict certain individuals from
changing the quantity of a part (using transaction codes M, , R, T, and blank.)

When this option is installed, the new security code (which can be up to four
characters in iength) can be set up using Menu X6 option 6.

Menu option #3: De not use a part transaction security code at Parts Posting
and Maintenance.

Menu option #4: Use a part transaction security cede to contrel part quantity
adjustments at Parts Posting and Maintenance. The security
code will be needed for each transaction.

Menu option #5: The security code will be needed for the first transaction.

 


Security Maintenance Screen
When the security option is installed, a 4-character security code is set up
in Security Maintenance (X6-6), as illustrated below.

 

Division cod

Name. .
Extended Name
Address

Extended Address
City State

Security Codes:
Communications COMM,
Parts . .

Stock Orders

Other Information:
Transfer Acct . A1800
Internal addr .

POS Printer . . Pi
Receivable Mon 6
Parts Hist Days 060
GST Num

Enter-Continue

SECURITY & CONFIGURATION

. BELLINGHAM, WA

SECURITY MAINTENANCE
A & R SALES & LEASING Co

. 288 WEST KELLOGG RD

Accounting
Configuration .
Parts Trans . .
Receivables -
units .

Interest Rate . 1800
Mos Pay Hist
Warranty Addr

Inv Head Lines

G/L Month -
Cancelled acct

Log Printer .

Postal 98226___

X6600-103

Enter ¥ to delete

Phone 206 733 7610

Backup
Financial .
Payables
Service .

Minimm Finance 100
Last Bill Date 031092
Default vender CAS
Spaces Left . . 5
Fiscal start. 1
Cancelled ID


Parts Posting & Maintenance Screen

When a security code has been set up, it is used on the Transaction screen
in Parts Posting & Maintenance, as illustrated below.

A & R SALES & LEASING CO Parts Posting and Maintenance X3200-103
Division: A Price book Transaction
Transaction cede: R Quantity: 5 Receipt cost: 10000
Vendor: CAS Part number: A52659 Descriptio
Class.: A Quick code.: BT Location. .
DEMO FOR AVERAGE COSTING
New vendor: New number: (For add or change only)
Transaction Codes
Available. .:
Reserve R/O: : Post sales
Reserve C/T: : Post sales returns
: Delete record
: Add record
Price upd: 00/00/00 : Chenge vendor/part#
Dir. List: 11000 + Post lost sale
Sug. List: 10000 + Minus to inventory
Internal: 5500 : Plus te inventory
Dir. Net: 0005000 : Receipt to inventory
: Receipt of transfer

Security Code: <----

Gmdi-End job cnd2-Info cmd3-History Cmd4-Trans Cmd5-Source of Supply
cmdl0-New Price Book

If option 5, "The security code will be needed for the first transaction," is
selected, the code is required for the first transaction only. The security
check is not repeated if you change screens, only if you press [Cmd1] and
re-enter Parts Posting & Maintenance.
om


X63-3 OPT PARTS MENUS [7 |

Average Costing

‘The DIS system can optionally maintain an average cost for each part which is
recalculated when a new part receipt is recorded on the system (either through
Parts Posting and Maintenance or through an order receipt.)

When this option is selected the average cost will be used when creating
costing transactions in your Point of Sale batch.

Menu option 6: Average costing for parts inventory is not installed.

lenu option 7: Average costing for parts inventory is installed.

 

The DIS Business System has traditionally used dealer net (replacement
cost) and will continue to do so unless average costing is installed (the
OPT switch is on). When average costing is installed, the system
calculates Average Cost of each part as it is received, displays Average
Cost in Parts Inquiry, and uses Average Cost instead of Dealer Net on
selected reports and for automatic transactions.

The decision to use average costing will depend on cost flow assumptions
made by your dealership. There is no problem switching from Dealer Net

to Average Cost and then back to Dealer Net. If the Average Costing OPT
is then turned back on at a later date, Average Cost is recalculated to equal
the current net price.

Most of the time parts received on orders cost more than parts already in
inventory: the current Dealer Net is usually jess than the Receipt Cost of
the incoming parts. Among the factors you should consider in deciding
which method to use are inventory valuation and its tax consequences,
gross margins, and disk space.

Inventory Valuation. Until new parts are received, inventory value is

SECURITY & CONFIGURATION


X63-3 OPT PARTS MENUS pe

 

calculated at Dealer Net and there won't be any change. As new parts are
received and average costs are calculated, inventory value changes.

Changes in inventory valuation may have an impact on your taxes
depending on whether you pay taxes on inventory or income, or both.

The following tables illustrate what happens to a single part line under
each method when costs are increasing.

INCREASING COSTS--REPLACEMENT COST METHOD
Qty Dealer Net Inventory Valuation

Before Order 5 $50 $ 250
Received on Order 5 $100

—

Total On Hand 10 $100 $1,000

INCREASING COSTS.--A VERAGE COST METHOD

Qty Dealer Net Average Cost Inventory Valuation
Before Order 5 $50 $50 $ 250
Receipt Cost
Received on Order 5 $100 Recalculated
Total On Hand 10 $75 $ 750

Gross Margins. Since average cost will usually be lower than Dealer Net,
gross margins will be higher.

INCREASING COSTS--REPLACEMENT COST METHOD
Dealer List Gross Margin Margin %

RELEASE 2.2 nae


X63-3 OPT PARTS MENUS [2]

$110 $10

INCREASING COSTS--AVERAGE COST METHOD
Dealer List Gross Margin Margin %
$Hio $35

Disk Space. An extra record is required for each part that has an average
cost. If, in Vendor/Class Configuration (X38-1), the field labeled "Last
Receipt” is already set to “Y," the record has already been added, and no
additional disk space is required for Average Costing.

If "Last Receipt" is set to "N" when Average Costing is installed, there
will be some increase in the size of your parts files. The amount of
increase depends on how many part lines you have and how many of them
are received after average costing is initiated. The record is not added until
average cost is calculated.

Timing & Recommendations

Because Average Costing affects your dealership's accounting, we
recommend installing it on the last day of a month. In addition, we
recommend running a Parts Inventory Pad (X36-1) immediately after
Average Costing is installed so both dealer net and average cost will be
listed. Save the parts pad with other documents that form your audit trail.

Although it takes only a second to set the switch for Average Costing in
the DIS OPT Library, file changes that follow may take 1-2 hours,
depending on the size of your parts files.

Calculations

Average Cost is calculated only when a part is received into inventory
through Receive Order (X342-2) and when an "R" transaction code is used
in Parts Posting & Maintenance (X3-2), The system calculates Average

SECURITY & CONFIGURATION


X63-3 OPT PARTS MENUS Co

Cost by the following formula:
((A *B)+(C*D)]/(B+D)=E

Parts EOD Audit Report where:

A = Current average cost per unit (OLD)

B = Current on hand quantity (ONHAND)
C = New receipt cost per unit (REC.COST)
D = New receipt quantity (REC.QTY)
E = New average cost per unit (NEW)

The labels used on the Parts End of Day Audit Report are listed in
parentheses--(OLD), (ONHAND), etc.

Where Average Costing is Used {
X3-1 PARTS INQUIRY. Average Cost is displayed. In the example

illustrated below, the Average Costing feature has just been

installed, and the system is using the price from the field labeled

"1-Dlr. Net."

RELEASE 2.2 C


A & R SALES & LEASING CO
Division: A Price book:
Vendor: CAS Part number:
Class.: A Quick code.:
DEMO FOR AVERAGE COSTING

Available. .: 5
Reserve R/O:
Reserve C/T:
On hand... : 5

Price upd.,: 00/00/00 Base

4-Dir. List: 11600
3-Sug. List: 10000
2-Internal.: 5500
1-Dlr. Net.: 9005000
Non-PTY gty:

PIY gty..

Returns.

Last count.: 00/00
bast sale..: 00/00
Date added.: 01/92
Avg Cost... 0005000


Parts Posting and Maintenance x3200-102

A52659

Part Informat:

Part category.: B
Supersede code:
Superseded by.:
Supersede aty
Weight.


Max. :


Oty ra
Package:
Malt..

5-Dir. Net:

Cmdl-End job Cmé2-Info cmé3-History cmdd-Trans

Cmd10-New Price Book

SECURITY & CONFIGURATION

 

on
Description: BATTERY
Lecation...: MT1101

Order code: A Return code: R .
Stock code: Qty.Break: WN
Core code:
Range Price

Last rept qty.: 5
Last rept date: 03/21/92
Dealer order #: 300231092

cma5-Source of Supply


X63-3 OPT PARTS MENUS a

X3-2 PARTS POSTING & MAINTENANCE. When a part is received
using an "R" transaction code, average cost is calculated from the receipt
cost. Each change is reported on the Parts End of Day Report (X3-9).

Note the field labeled “Receipt cost" on the screen below. If you do not fill
in the “Receipt cost," the system uses the cost that is currently in the field
labeled "Dir. Net."

A & R SALES & LEASING CO Parts Posting and Maintenance 3200-103
Division: A Price kook: Transaction

Transaction code: R Quantity: 5 Receipt cost: 10000

Vendor: CAS Part number: A52659 Description: BATTERY
Class.: A Quick code.: BT Location...: wr1101

DEMO FOR AVERAGE COSTING

New vendor: New number: {Fox add or change only)

Transaction Codes
available... (
Reserve R/O: : Post sales
Reserve C/T: : Post sales returns
On hand....: : Delete record

: Add record
Price upd: 00/00/00 : Change vendor/part#
1000 : Post lost sale
20000 Minus to inventory
5500 i Plus to inventory
9005000 Receipt to inventory
: Receipt of transfer

 

Gmd1-End job Cmd2-Info Cmd3-History Cméd-Trans Cmd5-Source of Supply
emd10-New Price Book

 

Average Cost is displayed and can be changed on the Part Information
screen, illustrated below. Changes are listed on the Parts End of Day Audit
Report. In the example illustrated below, 5 batteries have been received at

L.


a Receipt Cost of $100.00 each. Note the Average Cost, which has been
recalculated and is now $75.00.

In this example, the battery was received through Receive Order (X342-2)
and “Last rept gty," “Last rept date,” and "Dealer order #" have been
updated. These fields are updated every time a part is received when you
are using Average Costing. When parts are received through Parts Posting
& Maintenance, the “Dealer order #" is "MANUAL."

‘A & R SALES & LEASING CO Parts Posting and Maintenance 3200-101

Division: A Price book: Part Information .

Vendor: CAS Part number: A52659 Description: BATTERY

Class.: 8 Quick code.: BT Location...: MT1101

### Demo For Average Costing

Available..: 10 Part category.: B Order code: A Return code: R

Reserve R/O: Supersede code: Stock code: Qty.Break: oN

Reserve C/T: Superseded by.: Core code:
Supersede qty.: Range Price

: 00/00/00 Base = weight. :

4-Dlr, List: 11000

3+Sug, List: 19000

2-Internal.: 5500

1-Dlr. Net.: 0005000

Non-PT¥ gty: in: Oty rad: 1 bast rept qty.: 5

PIY gty...-: o Package: 1 Last rept date: 04/02/92

Returns....: Male... Dealer order #: s0010¢02

Last count.: 00/90

Last sale..: 00/00

Date added.: 61/92 S-plr. Net.:

Avg Cost...: 0007500

 

(mdi-End job cmd2-Info Cnd3-History Cmdé-Trans Gmd5-Source of Supply
Cmdi0-New Price Bock

 

X342-1 CORRECT ORDER BEFORE RECEIVING. If average
costing is installed, Receipt Cost can be modified.

SECURITY & CONFIGURATION


a | X63-3 OPT PARTS MENUS

Since the system recalculates Average Cost
using Receipt Cost, it is important for you
to enter the actual cost of the part if it is
different from Dealer Net.

On the screen illustrated below, note the new command key (Cmd9) at the
bottom of the screen. Use it to toggle the column labeled "Quick Code" to
“Receipt Cost."

‘A & R SALES & LEASING CO CORRECT ORDER BEFORE RECEIVING x3412-201 1

Division: A
Current mode:

Price book: CAS $0010402 Lines. . sees 1
SCROLL AND CHANGE LINES Extended Amt.. 250.00

Quick cty Qty A Supersession Qty

Paxt Number /Quick Code Code Ordered Revd C Part Number Revd

1 A52659

a
12
13
14
15

Br 5 3

Cmdi-End ¢mé2-scroll and change lines Cmd3-add lines
Cmd4-randomiy change lines Cmd5-add new parts Cmd6-receive © Cmd9-Rec. Cost.

 

When you use Cmd9-Rec. Cost, the Quick Code column is toggled to
display Receipt Cost, and the command key changes to Cmd9-Quick
Code. Receipt Cost defaults to Dealer Net.
Lo


X63-3 OPT PARTS MENUS.

To continue with the example, Receipt Cost has been changed from
$50.00 to $100.00 on the screen illustrated below. Although this change
causes Average Cost to be recalculated, it does not change Dealer Net on
the parts record. If the Receipt Cost reflects a permanent change in Dealer
Net, you can make the change in Parts Posting & Maintenance. Usually,
prices are updated routinely by Price Tape Update (X37-2).

A & R SALES & LEASING CO CORRECT ORDER BEFORE RECEIVING x3412-201
Division: A Price book: CAS s0010402 Lines....
Current mode: SCROLL AND CHANGE LINES

Rec. Qty Qty A Supersession
Part Number /Quick Code Cost Ordered Revd C Part Number
1 452659 20000 5 5

omdi-End cmd2-scroll and change lines cmd3-ad¢ lines
cndd-randomly change lines CmdS-add new parts Cmdé-receive  cma9-Quick Code

 

To change Receipt Cost, press [Shift][Tab] to position the cursor in the
correct column. Press [Enter] to record your changes.

SECURITY & CONFIGURATION


| X63-3 OPT PARTS MENUS co
{

X342-2 RECEIVE ORDER. When an order is received, average cost is
calculated and updated. Last Receipt Date is also updated. The order is
received at Receipt Cost (Dealer Net is used if the Receipt Cost is blank or
zero). Changes to order cost are listed on the Parts End of Day report (X3-
9).

X35-9 PRINT/FINALIZE STOCK PHASE-OUT. Average Cost is
used instead of Dealer Net.

X36-1 PARTS INVENTORY PAD. Average Cost is printed on the
detailed Parts Inventory Report. An Average Cost Summary is
included in the Vendor/Class Summary.

X36-7 ON HAND VALUE REPORT. Average Cost is used instead of (
net.

X36-8 INVENTORY VALUATION REPORT. Average Cost is used
instead of Dealer Net.

X37-1 REPRICE PARTS. If the Average Costing OPT is on, Reprice
Option 1, Reprice by Field (change price fields by a fixed
percentage), enables you to reprice average cost for 1 or all
vendors and 1 or all classes. The selection screen is illustrated
below.

RELEASE 2.2 -


AGR EQUIPMENT SALES Reprice Parts X3710-301
All Price Fields

Vendor Or ALL :
Class Or ALL :

New Price = number or old price X / percentage

Average Cost (5}= 10000
Dealer List 19000
Suggested List ( 10000
Internal 10000
Realer Net 10006

 

Cmdi-End job Cmd3-Return to reprice options.

 

X37-2 PRICE TAPE UPDATE. Price Tape Update does not change the
average cost of a part.

X3-9 PARTS END OF DAY. Changes to Average Cost are reported as

part of the audit trail. See "Calculations" for descriptions of the
labels on the report.

SECURITY & CONFIGURATION


| X63-3 OPT PARTS MENUS Cc

X3.12-1 TRANSFER PARTS. Average costing can be recalculated when
parts are transferred.

A&R EQUIPMENT SALES TRANSFER PARTS xaci01-01
Division: a Should transfers generate sales history? N Recalc Avg Cost ¥
From: A A&R EQUIPMENT SALES To: B
Quantity Part Number Ven Cls Error Messages Salesman Id: HAL

2 10326 cas

2 ato329 cas

1 al1423 cas

Cmdl-End job

 

X5-1 POINT OF SALE INVOICING. Average Cost is used for
automatic cost of sale transactions. The Point of Sale (SAM) file
carries Average Cost instead of Dealer Net.

X52-9 PRICE TABLE MAINTENANCE. Average cost can be used as
a valid price code (A).


X63-3 OPT PARTS MENUS [=]

X5-3. PRIORITY ORDERS. Average Cost is used for priority orders.
X56-3 SALESPERSON ANALYSIS REPORT. Average Cost is
reported. Same as Salesperson Analysis Report from End of Month
Procedure (X5-4).

X56-5 WORK-IN-PROCESS REPORT. Average Cost is used to
calculate margins.

X5-7 PART SALES HISTORY. Average Cost is displayed.

SECURITY & CONFIGURATION


 

OPT PARTS MENU THREE (X6333)

COMMAND MENU; 6333
(c) DIS Corp

oPT PARTS MENU

Automatic Price - Update master fields when tape fields are blank
Tape Update 2. Do not update master fields when tape fields are blank

Inventory 3. Inventory Interface System is not installed
Interface system Inventory Interface System is installed with the
HES EPIC electronic parts catalog
Inventory Interface System is installed with the
PartSmart electronic parts catalog

Create/Update 6. Create/Update Price Book from folder is not available (
Price Book 7. Create/Update Price Book from folder is available

23. Return to OPT Parts Menu Two 24. OPT Parts Menu Four

Ready for option number or command
see>

 


 


Automatic Price Tape Update

en a price tape is run against the parts master information, standard fields
are normally updated with current manufacturer information. This option
allows you to decide whether "blank" manufacturer information will overlay
the existing parts fields which currently exist.

Menu option 1: Update master fields when the manufacturer fields are blank.

Menu option 2: Do not update master fields when the manufacturer fields
are blank

 

Inventory Interface System

‘DIS will interface with other manufacturers electronic parts catalogs on

   

CD ROM. This option allows you to select which electronic parts catalog
system you have so that the DIS Inventory Interface System can pull
information from it. :

Menu option Inventory Interface system is not installed.

Mema option Invencory Interface System is installed with the EBS EPIC :
electronic parts catalog.

Menu option 5: Inventory Interface System is installed with the PartSmart
electronic parts catalog. :

SECURITY & CONFIGURATION


 

Create/Update Price Book

With this opt set on. the user will be allowed to create or update a price
book from a shared folder on the AS/400.

Menu option #6: Creating or updating a price book froma folder is not
available.

option #7: Creating or updating a price book from a folder is available.

 

c.


OPT PARTS MENU FOUR (X6334)

coMmaND MENU: x6334
{c} DIS Corp

### Parts Menu

Reprice Changed Do not reprice changed part numbers from price book
Part Numbers Reprice changed paxt numbers from price book

Taven. Adjustment Parts with the same bin sort by vendor and part number
Report by Bin Parts with the same bin sort by part number

Create Suggested . Prorate annual sales if there were no sales during the

Stock Order-DIs supply pericd last year

Method De not prorate annual sales if there were no sales
during the supply period last year

23. Return to OPT Parts Menu Three
24. OPP Parts Menu Five

Ready for option number or command
=>

 

SECURITY & CONFIGURATION


Reprice Changed Part Numbers

when changing a part number using the ‘C’ transaction code in Parts Posting
and Maintenance, the system can automatically read the price book for the
new number and change the price of the part.

Menu option 1: Do not reprice changed parts from the price book.

Menu option 2: Reprice changed parts from the price book

 

Inventory Adjustment Report by Bin

‘nen an inventory adjustment report is requested in sorted order by bin
location, further sorting options are available. ‘This option changes the
default secondary sort of this report.

Menu option 3: Sort parts with the same bin location by vendor and
part number.

Menu option 4: Sort parts with the same bin location by part number
ignoring the vendor code.
tO


Create Suggested Stock Orders-DIS Method

en creating a Suggested Stock Order using the DIS method, if there were
no sales during the supply period last year, you may choose to have the

sales for the entire year prorated and use that figure in calevlating the
order.

 

Menu option #5: Prorate annual sales if there were no sales during the
supply period last year.

Menu option #6: Do not prorate annual sales if there were no sales during
the supply pericd last year.

 

SECURITY & CONFIGURATION


OPT PARTS MENU FIVE (X6335)

COMMAND
tc) DIS Corp

MENU: X6335

OPT PARTS MENU FIVE

Reservation
Priority

Parts Posting
and Maintenance

23.
24.

- Reservations are filled only according to the
priorities from OPT Parts Menu One options 6 thru 10.
. Priority orders fill priority reservations and stock
orders fill stock reservations before any other
£111 pricrities from OPT Parts Menu One options

6 thru 20 are considered.

. Enable the $,0.S, feature.

Disable the $.0.$. feature.

Return to OPT Parts Menu Four
OPT Parts Menu Six

Ready for option number or command

 
XL


Reservation Priority

1. Reservations are filled only according to the priorities from OPT Parts
Menu One options 6 thru 10.

Reservations are filled according to the Reservation Priority OPT on OPT
Parts Menu One as illustrated below.

COMMAND

Reservation Priority

Parts reservations are filled according to a reservation fill priority number

of 1 - 6 that is assigned when an order is processed. This option allows you
to choose which types of reservations get which fill priority number.

Menu option #6:
Menu option #7:
Menu option #8:

Menu option #9:

option #10:

All reservations get a fill priority of 1 and are therefore
filled in date/time order.

Customer reservations get a fill priority of 2, warranty
reservations get a 3, and internal reservations get a 4.
Priority reservations get a 1, and stock reservations get a 2.
Cust res with a 'P' get ai; warr res with a ‘P’ get a 2;
int res with a 'P’ get a 3; cust res with an ‘S' get a 4;
warr res with an 'S' get a 5: int res with an ‘s* get a 6.
Cust zes with a ‘P* get a 1; cust res with an ‘s' get a
warr res with a ‘'P’ get a3; warr res with an ‘S* get a 4;
int xes with a ‘Pt get a5; int res with an 'S* get a 6.

Press ENTER to return to the menu.
F3=Exit  P12=Cance2

SECURITY & CONFIGURATION

 


| 28 | X63-3 OPT PARTS MENUS

2. Priority orders fill priority reservations and stock orders fill stock
reservations before any other fill priorities from OPT Parts Menu One
options 6 thru 10 are considered.

When this OPT is on, reservations are filled according to their origin:
priority reservations are filled by priority orders, and stock reservations are
filled by stock orders. After all reservations have been filled in this
manner, remaining reservations are filled according to the Reservation
Priority OPT on Menu One.

COMMAND
Reservation Priority

Parts reservations are normally filled according to the fill priority selected
from OPT Parts Menu One options 6 through 19. With this option, priority
reservations will be filled by priority orders and stock reservations will be
filled by stock orders before any of the fill priorities selected from OPT
Parts Menu One options 6 through 10 are considered.

Menu option 1: Reservations will be filled according to the £ill priority
selected from OPT Parts Menu One options 6 through 10.

Menu option 2: Priority reservations will be filled by priority orders and
stock reservations will be filled by stock orders. Only after
pricrity and stock order reservations are all filled, will
reservations be filled according to the fill priority selected
from OPT parts Menu One options 6 through 10.

Press ENTER to return to the menu.
F3-Exit F12=Cance)

Nae


Parts Posting and Maintenance

‘The $.0.5. feature allows you to change information that is usually handled by
the system, Fill in ‘ALL’ in the ‘New vendor’ field, and the $.0.S. code,

(3 periods, 3 underbars, and 3 more periods), in the ‘New number’ field. Then,
press Cmd2 twice. the following fields will be highlighted and available to be
changed: ‘Available’, ‘Reserve R/O', ‘Reserve C/T‘, ‘On hand’, ‘Stock code’,
“Last count', ‘Last sale’, &@ ‘Date added'. USE EXTREME CAUTICN, This is an
emergency measure. 5e sure you have all of the information you need before
changing Availability and Reservations. Is it part of an open document? Check

the Reservations Report. Is the part on a priority order? Check the Priority
Turnaround Report. ‘Tvpe the Vendor and Part number you want to change. when
you have changed the information, press Enter, Type another vendor and Part
number or Cmdl to end.

Menu option #3: Enable the $.0.S. feature.
Menu option 44: Disable the $.0.5. feature.

 

SECURITY & CONFIGURATION


 

OPT PARTS MENU SIX (X6336)

Command MENU: X6336
(ce) DIS corp

### Opt Parts Menu Six

LIFO . Do not allow selection of classes to be excluded.
End of Year Allow up to 15 selected classes to be excluded.

Parts Changed . Do not print Parts Master File change report at EOD
Report 4. Print report at EOD for Parts with Changes

. Return to OPT Parts Menu Five

Ready for option number or command

 

RELEASE 2.2 i


LIFO End of Year

‘With this option you may specify whether or not you want to allow the
selection of up to 15 classes to be excluded.

Menu option #1: Do not allow the selection of classes to be excluded

Menu option #2: Allow the selection of up to 15 classes to be excluded.

 

Parts Changed Report

This option determines whether this report will print automatically
with Parts End of Day or not. ‘The report is a list of parts that have
any change to their "master" information since the last time the report
was printed. “Master” information refers to most of the informational
fields which may be updated at Parts, Posting, and Maintenance (x3-2).
Fields such as: Description, Bin location, Weight, Prices, Price Bases,
Part Class, Minimum and Maximum Stocking Qty, Vendor Multiple... ete.
With this option turned on, ANY change to one of these informational
fields would cause that part to be included on the report.

Menu option #3: Do not print this report during Parts End of Day

Menu option #4: Print this report during Parts End of Day

 

SECURITY & CONFIGURATION


Notes:

## CHAPTER X63-4

OPT PAYABLES MENUS

OPT PAYABLES MENU ONE (X634)

COMMAND
(c) DIS corp

Payables Checks 1.
Extended Name 2.

Payables Checks 3.
. Avoid prompt for alignment on Payables Checks

Alignment Message

Invoice Entry/
Manual Checks

Payables 2.
Alignment Check a.

Print extended name after standard name
Print extended name before standard name

Prompt for alignment on Payables Checks

. Clear prior invoice description
. Keep prior invoice description

Do not print an alignment check for Payables
Print an alignment check for Payables

23. Return to OPIDIS Master Menu 24. OPT Payables Menu Two

Ready for option number or command

se=>

## X63-4 OPT PAYABLES MENUS

Payables Checks - Extended Name

‘This option will allow you to choose whether the extended name will print
after the regular name or before the regular name.

The U. S. Postal Service prefers the extended name or “attention line to be
the first line of the address block. They also prefer the extended address
to print on the same line as the normal address.

Menu option 1: GRADY CONSTRUCTION Menu option 2: LEROY GRADY
LEROY GRADY GRADY CONSTRUCTION
1234 STH AVE so 1234 STH AVE SO SUITE 101
SUITE 101 SPRINGDALE WA 98226
SPRINGDALE WA 98226

 

Payables Checks Alignment Message (

‘this option wili allow you to choose whether or not the check alignment
message will come up during Payables checks printing.

Menu option #3: Prompt for alignment on Payables checks.

ent option #4: Avoid the prompt for alignment on Payables checks.

 

RELEASE 2.1 LC


Payables Invoice Entry and Manual Checks

when entering in new invoices in Invoice Entry or Manual Checks, you can have

the invoice description default from the previously entered invoice if you set
this option.

Menu option #5: Clear prior invoice description.

enu option #6: Keep prior invoice description.

 

Payables Alignment Check

‘This option will allow you te choose whether or not an alignment check will
print prior to the first real Payables check.

Menu option #7: Do not print an alignment check.

jenu option #8: Print an alignment check.

 

SECURITY & CONFIGURATION


 

OPT PAYABLES MENU TWO (X6342)

‘COMMAND
(ce) DIS Corp

PAYABLES MENU

Payables Checks Print date on Payables checks
Print Format of . Print date on Payables checks
Date . Print date on Payables checks

. Purchase orders will print at
. Purchase orders will print at

23, Return to OPT Payabies Menu One

Ready for option number or command

 

Payables Checks Print Format of Date

option will allow you to choose the format you want the date to print
om your Payables Checks.

option #1: Print date on Payables checks like MMDDYY (01/31/95).

option #2: Print date on Payables checks like ¥YMMDD (95/01/31).

option #3: Print date on Payables checks like DDMMYY (31/01/95).

 

{
RELEASE 2.1 NS


X63-4 OPT PAYABLES MENUS.

Purchase Order Print

‘This option will allow purchase orders, which are part of an additional
purchased application of Payables, to print at different lines per inch.

Menu option #4: Purchase orders will print at 56 lines per inch.

Menu option #5: Purchase orders will print at 88 lines per inch.

 

SECURITY & CONFIGURATION


Notes:

## CHAPTER X63-5



COMMAND
(co) Dis corp


Accrued 1. Do not print accr vac on chk stub
vacation 2. Print accr vacation on chk stub

General Ledger - Bo not create detailed gl trans
fransactions 4. Create detailed gl transactions

Salaried Pay Rate 5. Print the pay rate on check stub
Do not print the pay rate on check stub

W-2 and T4 forms 7, Printer will double strike W+2/T4 forms
8. Printer will single strike W-2/T4 forms

23. Return to OPTDIS Master Menu 24, OPT Payrol! Menu Two

Ready for option number or command

 

Accrued Vacation

accrued for each employee. This option allows you to decide whether or

check stubs.


## CHAPTER X63-6

OPT POINT OF SALE MENUS

OPT POINT OF SALE MENU ONE (X636)

COMMAND:
(co) DIS Corp

Bin Location

C/I/W Invoices

cash Customers

é
;


24.

. Print bin locarion on part lines

- Print price 4 instead of bin loc
. Print price 3 instead of bin loc

+ Do not force C/I/W invoices to print

together

. C/E/t invoices will print together

Cash customers are not tracked
Cash customers are tracked

Return to OPIDIS Master Menu
OPT Point of Sale menu Two

Ready for option number or command

## X63-6 OPT POINT OF SALE MENUS

 

Bin Location

The standard Point of Sale Invoice prints the bin location of the parts being
sold to the left of the selling price. This option allows you to choose not

te print the bin location, but to print price 3 or price 4 of that part instead.
The price selected will print to the left of the selling price.

Menu option 1: Print the bin location in its normal location.

Menu option 2: print price 4 of the part instead of its bin location.

Menu option 3: Print price 3 of the part instead of its bin location.

 

C/W Invoices

Tf Point of Sale detail lines are flagged with an ‘I’ or a ‘W’, and the invoice

is closed, internal and/or warranty invoices will automatically print. It is

possible that, given the number of people invoicing, other invoices could slip

into the print sequence between 'C', ‘I’, and ‘w' invoices which would normally

Print together. This option allows you to specify that these 'C', ‘I', and ‘Ww (
invoices must always print together, even though it may slightly slow down the

printing process.

Menu option 4: It does matter if the ‘C', ‘I’, and ‘W' invoices print
sequentialiy. Do not force them te print together

Menu option 5: Make sure that ‘C’, ‘I', and ‘W' invoices always print
sequentially. No other invoice will print in between them.

 

CL


Cash Customers

Cash Customers

Typically, all Point of Sale cash invoices are created under one account. This
account is established in Receivable Maintenance X11-2 even though it is not
actually a receivable customer. ‘The address number for this account is

-CASH@, where _ = a space, and d=the first letter of your division.

This option allows the system to establish unique address numbers for each
customer who normally pays cash. These address numbers will appear in the Point
of Sale rolladex and will be accessible through the Marketing Menu

 

Menu option 6: Cash customers will not be tracked individually. All cash sales
will track under CASHd address number.

Menu option 7: Cash customers will be tracked individually. Address numbers
will be established for each customer.

 

SECURITY & CONFIGURATION


 

OPT POINT OF SALE MENU TWO (X636-2)

COMMAND MENU: X6352
(c} DIS Corp

opt

Labor Hours . Print labor hours on invoice
2. Do not print labor hours on invoice

Office Copy . Never print an office copy

Always print an office copy
Print office copy only if closed

 

Time card 6. Billable hours are calculated when enter is pressed
Entry 7. Billable hours must be entered manually

Billable hours are not required and Tk job code
ield will display

 

23. Return to CPT Point of Sale Menu One 24. OPT Point of Sale Menu Three

Ready for option number ox command (

see

 

RELEASE 2.2 os


Labor

 

Office


Hours

This option lets you decide whether or not the total number of labor hours
should print on your Point of Sale inveices.

Menu option 3: Print the total number of labor hours on the Point of Sale

invoice.

Menu option 4: Do not print the total number of labor hours on the Point of
Sale invoice.

when a Point of Sale invoice containing labor iines is printed, a second,
internal invoice (office copy) can be printed which will list all of

the labor detail by mechanic. This option aliows you te decide when this
office copy is printed.

 

Menu opticn §: Never print an office copy.

Menu option €: Always print an office copy every time the original invoice
is printed.

Menu option 7: Only print an office copy if the original invoice is closed
and printed (cmd2).

 

SECURITY & CONFIGURATION


 

Time Card Entry

Time Card Entry

When entering service time in Time Card Entry, this option allows you to
have the program automatically calculate billable hours, or require the
manual entry of billable hours, or not require them at all and display the

‘Thermo King job code field.
Menu option 6: Billable hours are caiculated automatically when enter pressed.

Menu opticn 7: Billable hours must be entered manually.

Menu option @: Billable hours are not required and Thermo King job cede field
will display.

  

L.


OPT POINT OF SALE MENU THREE (X6363)

CommaND MENU: X6363
(c) DIS Corp

OPT POINT OF SALE MENU THREE

 

Negative Discount 1. SURCHARGE COUNTY TAX
blank . CITY TAX

3. FED. TAX 7, PROV. TAX

4. EXCISE TAX @. STATE TAX

Signature Line 9. Print signature line on charge documents
10. Print signature line on all documents

11. Never print signature line

Open Decument 22. Do not warn if open document(s) exist
Warning 13. Warning message if open document(s) exist

23, Return to OPT Point of Sale Menu Two 24. OFT Point of Sale Menu Four

Ready for option number or command

 

SECURITY & CONFIGURATION


63-6 OPT POINT OF SALE MENUS ( >

Negative Discount

Discount codes can be attached to Point of Sale lines and a discount amount
will be automatically subtracted from the line total. when a discount code

is set up with a negative percentage, the calculated discount is actually added
to the line total instead of subtracted. This option will let you decide which
description will print to describe these negative discounts.

option 1: Print "SURCHARGE" to descrihe a negative discount total.
option 2: Do not print a description for a negative discount total.
option 3: Print "FED. TAX" to describe a negative discount total.

option 4: Print “EXCISE TAK” to describe a negative discount total.
option 5: Print “COUNTY TAX” to describe a negative discount total.
option 6: Print “CITY TAX” to describe a negative discount total.

option 7: Print “PROV. TAX" to describe a negative discount total.
option 8: Print “STATE TAK" to describe a negative discount total.

 

  

Signature Line

This option allows you determine when a signature line should be printed at the (
bottom of @ Point of Sele invoice.

Menu option 9: Only print a signature line on charge documents

Menu option 10: Print a signature line en all Point of Sale documents.

Menu option 11: Never print a signature line on a Point of Sale document.

 

tO


Open Document Warning

‘This option allows you determine whether the system provides a warning at the
time a new document is open that other open documents exist for the same
customer.

Menu option 12: Do not provide an open document warning

Menu option 13: Provide an open document warning.

 

SECURITY & CONFIGURATION


OPT POINT OF SALE MENU FOUR (X6364)

COMMAND
(e} DIS Corp

Labor Costing

Transfer Parts

Update History

Point of Sale
Lockout Feature

OF SALE MENU FOUR

1. Use the reported hours
2. Use the billed hours

3. Update parts history for transferred parts

4.

Do not update parts history for transferred parts

+ Lockous
+ Lockout i
. Lockour i
. Lockout i
+ Lockout

not installed
installed manually

installed automatic based on credit limit
installed automatic based on aging buckets
installed automatic based on 7 or &

23. Return to OPT Point of Sale Menu Three 24. OPT Point cf Sale Menu Five

Ready for option number or command

> §

Labor Costing

 

The system can automatically calculate labor cost. Use this option to select
whether the system should use the reported hours or the billed hours during
Point of Sale batch calculations

Menu option 4: Use the reported hours to calculate the labor cost.

Menu option §: Use the billed hours to calculate the labor cost.

 
LC


Transfer Parts Update History

On the "Sold-to" screen of Point of Sale, a field is available to indicate that
the invoice is not a normal sale, but is actually an inter-store transfer. This
option allows you to decide whether such part transfers should update the sales
history of the parts.

Menu option 6: Update the sales history for transferred parts

Menu option 7: Do not update the sales history for transferred parts

 

SECURITY & CONFIGURATION

## X63-6 OPT POINT OF SALE MENUS C

Point of Sale Lockout Feature

This option allows you to install Lockout at Point of sale.
5. Lockout is not installed.

6. Lockout is installed (manual). You determine who should be locked out from
charging at Point of Sale and assign a “Z" credit code in the second credit code
position on their record in Accounts Receivable.

7. Lockout is installed {automatic based on credit limit). "Z" credit codes are
added and removed during Accounting End of Day. The "Z" credit code is added if a
customer’s balance is greater than or equal to their credit limit. If their
credit limit is blank and their balance is zero, accounting End of Day will put
in a "2" credit code. NOTE: If a "Z" credit code is added, you can wait until the
following day and select option 8 to remove the code.

 

8. Lockout is installed (automatic based on past due balances). "z" credit codes

are added and removed during Accounting End of Day. The "Z" credit code is added

if a customer has a balance in 1 or more of the 30, 66, 90, 120 day categories.

The *Z" credit code is removed if they have no balance in the 30, 60, 90, 120 day
categories. A report is generated listing the changes to customers’ records. (

9. Lockout is installed (automatic based on credit limit and past due balances).
"2" eredit codes are added and removed during Accounting End of Day. The *Z"
credit code is added if a customer's total balance is over their credit limit or
they have a balance in 1 or more of the 30, 60, 90, 120 day categories. The "2"
credit code is removed if there the total balance falls below their credit limit
and they have no balance in the 30, 60, 90, 120 day categories. A report is
generated listing the changes to customers’ records.

 

t
RELEASE 2.2 NS


OPT POINT OF SALE MENU FIVE (X6365)

coMMAND:
(©) DIS Corp

MENU: X6365

 

OPT POINT OF SALE MENU FIVE

Security Gate
Cmdli option 4

Phone Number
Print

Periodic

Invoicing

23.
24.

 

Display security gate at POS Cmdli Option 4
Do not display security gate at POS Cmdil Option 4

Print customer phone number on invoice

4. De not print customer phone number on invoice

Use same document cumber with letter suffix
Use next document number in sequence

Return to Point of Sale Menu Four
OPT Point of Sale Menu Six

Ready for option number or command

 

>

Security Gate

Security Gate

 

Normally, when Cméli option 4 (Parts Posting and Maintenance) is selected
during Point of Sale, a parts security gate is displayed. This option allows
you te suppress this security gate if desired.

Menu option i: Display a

security gate when Cmdii option 4 is selected.

\ Menu option 2: ve not display a security gate when Cmdli option 4 is selected.

SECURITY & CONFIGURATION


Phone Number

Use this option to determine whether customer phone numbers will print
om your Point of Sale invoices.

Menu option #3: Print customer phone numbers on your Point of Sale
invoices.

Menu option #4: De not print customer phone numbers on your Point of

 

Periodic Invoicing

 

When periodic invoices are created for repeat billings, the system will
either use the same document number with a letter suffix at the end
(similar to priority order invoices,) or will use the next invoice number
in sequence.

Menu option §: Use the same invoice number with a letter suffix, (

Menu option 6: Use the next invoice number in sequence

 

RELEASE 2.2 CO


OPT POINT OF SALE MENU SIX (X6366)

‘COMMAND
{cl DIS Corp

### Of Mend Six

Canadian GST 1. Do not print Canadian GST Registration
Registration . Print Canadian GST Registration

Invoice - 3. Print extended name after standard name
Extended Name 4. Print extended name before standard name

Log Printer - A Cmd4 log printer is not installed
A Cmd4 leg printer is installed

23. Return to Point of Sale Menu Five
24. OPT Point of Sale Menu Seven

Ready for option number or command

 

Canadian GST Registration Number

This option allows a Canadian GST registration number to be printed on
Point of Sale invoices adjacent to the GST subtotal.

Menu option #1: Do

 

ot print the Canadian GST registration number on the POS

invoices.

Memu option #2: frint the Canadian GST registration number on the POS invoices.

 

SECURITY & CONFIGURATION


 

Invoice - Extended Name

This option will allow you to choose whether the extended name will print
after the regular name or before the regular name.

The U. S. Postal Service prefers the extended name or “attention" line to be
the first line of the address block. ‘they also prefer the extended address
to priat cn the same line as the normal address.

Menu option 3: GRADY CONSTRUCTION Menu option 4: LEROY GRADY
LEROY GRADY GRADY CONSTRUCTION
1234 STH AVE so 1234 STH AVE So SUITE 101
SUITE 102 SPRINGDALE WA 98226
SPRINGDALE WA 96226

 

Log Printer

The DIS system optionally provides for a log printer which is used
whenever a document is placed on hold with the emd4 key. Such a log is (
useful when reconstructing work order activity

When this option is selected, the printer id to be used for this cmd4 log
is entered using Menu Xé option 6.

Menu option §: A leg printer is not installed.

Menu option 6: A log printer is installed.

 

CC


OPT POINT OF SALE MENU SEVEN (X6367)

COMMAND MENU: 26367 INQUIRY WH
(c) DIS Corp

### Oint Of Sale Menu Seven

Invoice - Print the discount emount at the bottom of the
Discount invoice
De net print a discount amount at the bottom of the
invoice; "net" the discount amounts on each line

Point of Sale : Point of Sale security is not installed

Security 4. Point of Sale security is installed
Only the Point of Sale security report is installed

23. Return to Point of Sale Menu Six
24. OPT Point of Sale Menu Eight

Ready for option number or command

SECURITY & CONFIGURATION


X63-6 OPT POINT OF SALE MENUS ~
18 C

Invoice - Discount

Discount codes cen be added to each invoice line to adjust the selling price
of the item. Usually the dollar total of the discount for the entire invoice

is printed at the bottom of the invoice.

This option allows the discount to be automatically subtracted from the
selling price with the new adjusted price printing on each detail line (with no
discount amount printing at the bottom of the invoice.)

Menu option #i: Print the discount amount at the bottom of each invoice.

Menu option #2: Print a selling amount on each detail line which is already
adjusted by the discount

 

 

Point of Sale Security

The DIS system provides an optional security system which can report and
control which individuals add, delete, or change line items on documents. (

This feature can be implemented with just an audit trail report, or in its
complete form with on-line checking of user security for each document function
requested.

When security is active, special Point of Sale user ids and passwords must be

set up using Menu XS option 12.

Menu option 43: Point of Sale security is not instalied.

Meau option #4; Point of Sale security is completely installed.

Menu option #5: Only the audit trail security report is installed.

 


 


OPT POINT OF SALE MENU EIGHT (X6368)

COMMAND
(c) DIS Corp

If Point of Sale
Security is
Installed .

OF SALE MENU EIGHT

Print line additions on the security report
Do not print line additions on the security report
Print line modifications on the security report

Do not print line modifications on the security report
Print line deletions on the security report

Do not print line deletions on the security report

. Print document reopenings on the security report
+ Do not print document reopenings on the security rpt

Print document cancellations on the security report

. Do not print document cancellations on the sec rpt

23.
24.

Return to Point of Sale Menu Seven
OPT Foint of Sale Menu Nine

Ready for option number or command

SECURITY & CONFIGURATION


 

Point of Sale Security Report

If Point of Sale security is installed {see OPT Point of Sale Menu Seven)

@ report prints during parts end of day which can list every change to a
Point of Sale document. The options on this menu allow you to choose which
type of lines you would like to see on this daily report.

Menu option #1: Print line additions
Menu option # 2: Do net print line additions
Menu option #3: Print line modifications

Menu eption # 4; Do not print line modifications
Menu option Print line deletions

Menu option Do not print line deletions

Meau option Print document reopenings

Menu option De net print document reopenings
int document cancellations

Menu option #10: Do not print document cancellations

Menu option # 9: P:

  

o


OPT POINT OF SALE MENU NINE (X6369)

‘command
{ce} DIS Corp

Invoice -
Print Counter

Invoice -
Print Date

invoice -
Time of Day

Part Sales
History

23. Return to OF"

OF SALE MENU NINE

Do not print a counter on the iavoice

2. Print a counter on the invoice

Print either the session or the close date
4, Always print the creation date

Do not print the time of day on the invoice
Print the time of day on the invoice

Part Sales History is not installed
Part Sales History is installed

Sale Menu Eight 24. OPT Point of Sale Menv

Ready for option number or command

Invoice - Print Counter

 

The DIS system can optionally include the number of times a document has been
printed on the actual printed copy of each invoice.

Menu option #1: Do not include a print counter on the invoice

Menu option #2: Include a print counter on the invoice.

 

SECURITY & CONFIGURATION


X63-6 OPT POINT OF SALE MENUS C ~

Invoice - Print Date

When a document is printed, the DIS system normally prints the current session
date if the ticket is still open, or the date the ticket was closed. This
option allows for the printing of the creation date instead, no matter when the

document is closed.
Menu option #3: Print the session/close date on each document.

Mem option #4: Print the creation date on each document.

 

Invoice - Time of Day

 

‘The DIS system can optionally print the time of day on each document.

Menu option #5: Do nct print the time of day on each document.

Menu option #6: Print the time of day on each document

 

Part Sales History

‘The DIS system can optionally track detail part sale information for each
customer. If this option is installed the syscem will capture this
information every time a Point of Sale watch is created. The sale information
can be inquired either by customer, vendor/part number, or document aumber.

If this option is installed the system will keep the sale information for
the number of days specified at Menu X6 option 6.

Menu option #7: Part Sales History is not installed.

Menu option #8: Part Sales History is installed.

 


OPT POINT OF SALE MENU TEN (X636A)

COMMAND: MENU: X636A
(c) DIS corp

### Of Sale Menu Ten

Iavoiciag - 1. Find supersession by checking price book first
Supersession . Find supersession by checking local supersession

information first

Default 3. Default the priority code to 'P’
Priority Code Default the priority code to ‘x*

POS Entrance 5. Display the ‘Print backordered lines’ prompt
Suppress the ‘Print backordered lines' prompt
23, Return to OPT Point of Sale Menu Nine

24. OPT Point of Sale Menu Eleven

Ready for option number or command

 

Invoicing - Supersession

Supersession can be maintained locally on the master records for each part.
‘This may differ from supersession information that is provided by the
manufacturer in the price book. This option determines whether the system
will first check che price book or local supersession information for use at
Point of Sale and Part Availability.

Menu option #1: Check the price book first for supersession information.

 

| Monu option #2: Check the locsl master records first fox supersession

information.

SECURITY & CONFIGURATION


 

Defauit Priority Code

When a part is placed on an inveice at Point of Sale and there is not enough
of that part available to sell, the priority code will come up on the line
with a 'P'. If put on the ticket that way, the part will be put on a priority
order. With this option, you may select to have the priority code default to
an 'X'. This code will not allow the line to be placed on the ticket as is.

it will force the counter perscn to determine the most appropriate order method

fox that particular situation. ‘he pricrity code must be changed to a valid
code such as 'P', 'S', ‘DY, etc.

Menu option #6: The default priority ecde will be 'P’.

Menu option #7: The defaule priority code will be °x".

  

POS Entrance

With this option you may specify whether or not you would like to have the
“Print backordered lines* prompt appear on the screen.

Menu option #1: Display the ‘rrint backordered lines’ prompt.

Menu option #2: Suppress the ‘Print backordered lines‘ prompt

 

RELEASE 2.2 \


OPT POINT OF SALE MENU ELEVEN (X636B)

 
   
 

COMMAND MENU: X636B x6
fe) DIS Corp

  
   
   

    

OPT POINT OF SALE MENU ELEVEN

    
 

 

   

cash i, Cash Printer feature is not installed
Printer 2. Cash Printer feature is installed

      
  
  
   
   
  
 
 

Self Service 3. Self Service Invoicing is not installed
Invoicing 4. Self Service Invoicing is installed
Print voided 5. Print voided documents

Documents 6. Do not print voided documents

Credit card 7. Print legal text on credit card invoice
Invoices @. Do not print legal text on credit card invoice

    
     
  
  
 
 

 

 

23. Return to OPT POS Menu Ten 24, OPT Point of Sale Menu Twelve

      

  

Ready for option number or command

SECURITY & CONFIGURATION


Cash Printer

The Cash Printer Feature is a special receipt style printer that can be used
at Point of Sale to print cash tickets. The invoice that prints out is a
narrow receipt that still contains all of the necessary invoice information
but is for those quick cash sale customers that do not require the larger

invoice print.

Menu option #1: Cash Printer Feature is not installed.

Menu option #2: Cash Printer Feature is installed.

 

Seif Service Invoicing

 

Self Service Invoicing

Self Service Invoicing is specially written Point of Sale application that can

be set up for high volume customers to invoice themselves. Many of the

features in regular Point of Sale that are not appropriate for a customer to (
have access to have been eliminated.

Menu option 43: Self Service Invoicing is not installed

Menu option #4: Self Service Invoicing is installed.

 

LO


Print Voided Documents

With this option you may specify whether or not you would like your voided
Point of Sale documents to print.

Menu option #5; Print voided point of sale documents.

Menu option #6: Do not print voided point of sale documents.

If the invoice is closed when cmd10 is pressed, the system cancels
the document and prints a copy of it regardless of how this option
is set. If you do not want a copy of the document to print, set
this option using #6 and them make sure all closed documents are
xeopened (cmd9) before they are voided (cmdi0).

 

Credit Card Invoices

bith this option you may specify whether or not you would like to print
the legal text ac the bottom of a credit caxd invoice.

Menu option #7: Print the legal text on credit card invoices.

Menu option #8: De not print the legal text on credit card invoices.

 

SECURITY & CONFIGURATION


 

OPT POINT OF SALE MENU TWELVE (X636C)

COMMAND MENU: x636C INQUIRY WH
(c} DIS Corp
OPT POINT OF SALE MENU TWELVE

Cash 1. Cash Tendering feature is not installed
Tendering 2. Cash Tendering w/o cash drawers is installed
3. Cash Tendering with one cash drawer is installed
4. Cash Tendering with multiple cash drawers and
cash drawer security is installed

Point of Sale Display only the division code in the POS roladex
Roladex Display all edit codes in the POS roladex

 

7. Display ail divisions on the 70S reladex
Display only your division on the POS roladex

23. Return to CPT POS Menu Eleven 24. Opt Point of Sale Menu Thirteen

Ready for option number or command {

 

Lo


Cash Tendering Feature

 
     
         
     

  

cash Te:

  

ing is a custom Point of Sale feature that will allow you to better
monitor cash ticks

3 and your cash box on the Point of Sale counter. You may
also use this feature to signal the cpening ci cash drawers. An End of Day

report wilt help you reconcile the cash drawer at the end of each business day.
Use this opticn to choose the feature that fits your individual needs.

 

Menu option #1: Cash Tendering is not installed
Menu option #2: Cash Tendering is installed with no automatic cash drawers.
Menu option #3: Cash Tendering is installed with one automatic cash drawer.

Menu option #4: Cash Tendering is installed with multiple automatic cash
drawers and with cash drawer security.

 

 

Point of Sale Roladex

The Point of Sale roladex will display the custeomer#, the customer name,

the customer telezhonet, with either the customer‘s division code or all of the
the customer edit codes. The edit codes can tell you whether a customer is 2
receivable customer, a payable vendor, an employee, 2 whole goods customer, and
what division they are in. Use this feature to decide whether to display only
the division code or all edits codes on the Point of Sale roladex.

Menu option #5: Display only the division code on the Point of Sale roladex.

Menu optioa #6: Display all customer edit codes on the Point of Sale roladex.

 

Point of Sale Roladex

Use this cotion to select whether the Point of Sale roladex will display all
customers from all divisions or whether it will only display the customers from
the security gate division.

Menu option #7: Display all divisions on the Point of Sale roladex.

Menu option #8: Display only the customers from the division entered at the
security gate.

 

SECURITY & CONFIGURATION


X63-6 OPT POINT OF SALE MENUS Cc

OPT POINT OF SALE MENU THIRTEEN (X636D)

COMMAND INQUIRY WH
(ce) BIS Corp
SALE MENU THIRTEEN

Labor Detail - No labor detail lines on invoice

Print labor detail lines on invoice

3. Combine labor lines with matching TK job codes
-and do net print employee#
Combine labor lines with matching TK job codes
but print only freon#, job code, and description
Combine labor lines with matching TK job codes
but print only job code and description

Labor Analysis Oniy include closed/posted documents on report
Reporc Enelude open, reopen, and closed documents on report

Return to OPT Point of Sale Menu Twelve

Ready for option number or command (

 

oe


Labor Detail


Point of Sale labor information can be entered on a line by line basis for each
mechanic. This option determines whether the line by line detail will print on
che invoice, or whethex the labor will be summarized into one line per sales

code.

Menu option

option
option

option

eption

he


 

Do not print detailed labor lines. Print summary labor
information by sales code

Print all of the detail labor lines.

Print ali of the detail labor lines except combine matching
Thermo King job codes and do not print employees.

Print all of the detail labor lines except combine matching
Thermo King job codes and only print freon#, job code, and
job code description. :

Print all of the detail labor lines except combine matching
hermc King job codes and only print job code and description.

Labor Analysis Report

 
   
  

     
 
     
  
 
 
     
   
 

Menu option

SECURITY & CONFIGURATION

Labor Analysis Report

This option allows you to include only closed/posted documents on the Labor
Analysis Report and use the posted date for the date compare, or to include
open, reoven, and closed documents and use the work date from the detail labor
line for the date compare.

6:

Menu option 7:

Analysis Report and use the work date on the detail labor line.

 

Qnly include closed/posted documents on the Labor Analysis
Report and use the posted date.

Include open, reopen, and closed documents on the Labor


X63-6 OPT POINT OF SALE MENUS (~

OPT POINT OF SALE MENU FOURTEEN (X636E)

 
   
 

COMMAND.
(¢) DIS Corp

 
    
   

   

  

POINT oO

 

### F Sale Menu Fourteen

 

  
   
  
   
  
 
 
 
 
 
 
  
  
 
 

 

 

 

 

 

Parts Sales 1, Changing divisions requires a security gate
History 2. Changing divisions does not require a security gate
priority Orders 3, Drop ship ‘D' priority parts are included on priority

oxders if they are from an open or closed document
4, Drop ship ‘D’ priority parts are included on priority
orders only if they are from a closed document

 

Invoice - 5. Print ‘GST‘ on every sales code that is subject to GsT
ost §. Do not print ‘GST’ on any sales code description

23. Return to OPT Point of Sale Menu Thirteen
24. OPT Point of Sale Menu Fifteen

Ready for option number or command

  


Parts Sales History

Within the Parts Sales History application, you may hit a Cmdl2 key to change
divisions. With this option you may choose whether or not changing divisions
will require you to pass a security gate.

Menu option #1: Changing divisions requires a security gate.

Menu option #2: Changing divisions does not require a security gate.

 

Priority Orders

This option allows you te choose whether drop ship 'D‘ priority parts from
both open and closed documents or just closed documents are included on
priority orders

Menu option 43: Drop ship ‘D’ priority parts from open or closed documents
are included on priority orders.

Wenu option #4: Only drop ship 'D' priority parts from closed documents are
included on priority orders.

 

### Warning

If you select option #4 while there are drop ship parts on the priority order i
queue, they will remain on the queue until they are processed. :

 

Invoice - GST

 
  

  
     
  
  

When items sold at Point of Sale with a sales code that is subject to ost
print on the invoice, you may choose to have the word ‘GST’ print along with
description for that sales code.

Menu option #5: Pr:

  

% ‘GST on every sales code that is subject to osT.

       

 

Menu option #6: Do rot print ‘GST' on any sales code description.

SECURITY & CONFIGURATION


OPT POINT OF SALE MENU FIFTEEN (X636F)

command
(c) DIS Corp

### Cpt Point Of Sale Menu Fifteen

Salesperson - if labor cost = $0, use payroll rate for costing
Analysis Report, If labor cost = $0, do not use payroll rate

23. Return to OPT Point of Sale Menu Fourteen

Ready for option number or command

Salesperson Analysis Report

With this option you may specify whether or not you would like to use the
payroll rate for costing on the report when the labor cost is $¢.

Menu option #1: If labor cost = $0, use payroll rate for costing.

Menu option #2: If labor cost = $0, do not use the payroll rate for costing.

 
{
XW

## CHAPTER X63-7

OPT RECEIVABLES MENUS

### Introduction

The following OPT’s apply to receivables.

### Contents

OPT RECEIVABLES MENU ONE.
Statement Length..........
Balance Forward Credits...
Accounting End of Month ...

 
 
  
 

OPT RECEIVABLES MENU TWO.
Statement - Zero Balance.....
Default Canadian GST Method

 

 
 
 
 
  
   
 
  
 
 
 

OPT RECEIVABLES MENU THREE
Interest Aging...
Aging at EOD
Interest Calculation

Corporate Address
Zero Amount Transactions
Receivables Inquiry ...........

OPT RECEIVABLES MENU FIVE.
Enter Payments .....
Enter Payments .
Enter Payments .
Enter Payments .

OPT RECEIVABLES MENU SIX
Statements


X63-7 e OPT RECEIVABLES MENUS RELEASE 2.2

Statements...
Statements...

 

OPT RECEIVABLES MENU SEVEN..
Statements...
Statements...
Statements...
Statements...

 
 
 
 
 
 

OPT RECEIVABLES MENU EIGHT.

Statements..... 2
Enter Payments . 2
Distribute Payments .. 3

OPT RECEIVABLES MENU NINE .
Statement 0.0.00... teen
Multiple Ship To Addresses...

 
 
 
  
 
  

Setting Up Multiple Ship To Addresses in Receivables Maintenanc: 4
Using Multiple Ship To Addresses at Point of Sal 9
Interest and Credit Entries ........ ‘0
Aging vs. “Days Until Interest” .... .20


SECURITY & CONFIGURATION X63-7 « OPT RECEIVABLES MENUS 3

 

OPT Receivables Menu One

COMMAND MENU: X637 ws
(c} DIS Corp

 

Statement Length 1. Standard billing statements
2. Long form billing statements with titles
3. Long form billing statements without titles

Balance Forward 4. Apply to 120 day bucket first
Credits 5. Apply to service charge bucket first
Accounting BOM 6. Do not print Aged Receivables Detail Report at EOM

7, Print Aged Receivables Detail Report at EOM

23. Return to OPTDIS Master Menu
24. OPT Receivables Menu Two

Ready for option number or command

 

se=>

Po

Statement Length

DIS currently supports three different sizes and styles of monthly billing

Statements. This option allows you to specify which one you require.
Menu option #1: 8.5" statements with pre-printed column titles
Menu option #2: 11" statements with pre-printed column titles
Menu option #3: 11" statements without pre-printed column titles

 

Balance Forward Credits
This option will allow you to choose the order in which receivable aging balances
will be affected by a credit to a balance forward receivable account.
Menu option #4: Apply balance forward credits in the following order; 90
days, 60 days, 30 days, service charge, and current.
Menu option #5: Apply balance forward credits in the following order;
service charge, 90 days, 60 days, 30 days, and current.

Accounting End of Month
This option will allow you to choose whether the Aged Receivables Report will
print during Accounting End of Month.
Menu option 6: Do not print the Aged Receivables Detail Report as part of
Accounting End of Month.

### 4 X63-7 « Opt Receivables Menus

Menu option 7: Print the Aged Receivables Detail Report as part of
Accounting End of Month.

OPT Receivables Menu Two

COMMAND
(c) DIS Corp

Statement -
Zero Balance

Default Canadian
GST Method

 

 

aawe

23.

MENU: 6372

- Default new customers to a GST
- Default new customers to a GST
- Default new customers to a GST
. Default new customers to a GST

Return to OPT Receivables Menu
OPT Receivables Menu Three

Ready for option number or command

Statement - Zero Balance
This option will allow you to choose whether or not to print billing statements for
customers with a zero balance.
Menu option #1: Do not print a statement if the customer has a zero balance.
Menu option #2: Print a statement if the customer has had activity during the
month even if there is a zero balance.
Menu option #3: Print a statement if customer has zero balance and whether
or not they have had activity this month.

Default Canadian GST Method

This option will change the Canadian GST method that new customers will

default to in Receivables Maintenance, Marketing Maintenance, and when adding

a new cash customer through Point of Sale.
Menu option #4: Default new customers to a GST method of 3 - GST and
PST will each calculate independently from the invoice subtotal.

. Do not print zero balance statements

- Print all zero balance statements

method
method
method
method

one

 

 

. Print zero balance statements if activity

of 3
of 1
of 2
of 0


SECURITY & CONFIGURATION X63-7 * OPT RECEIVABLES MENUS 5
eee ee ee eee ee OY

Menu option #5: Default new customers to a GST method of 1 - GST will be
calculated 1st and then added back in before PST is calculated.

Menu option #6: Default new customers to a GST method of 2 - PST will be
calculated ist and then added back in before GST is calculated.

Menu option #7: Default new customers to a GST method of 0 - No GST.

OPT Receivables Menu Three

 

COMMAND MENU: X6373 ws
(c) DIS Corp

Interest 1. Allow interest transactions to be aged
Aging 2. Keep interest transactions as current
Aging at EOD 3. Calculate Receivables Aging during End of Day

4. Do not Calculate Receivables Aging during End of Day

Aging Date §. Calc Aging based on current session date
Calculation 6. Calc Aging based on day following the session date
Interest 7. Calculate interest on interest

Calculation 8. Do not calculate interest on interest

23. Return to OPT Receivables Menu Two 24. OPT Receivables Menu Four

Ready for option number or command

ses>

 

 

 

Interest Aging
This option will allow you to choose whether Interest transactions will age or
remain as current entries in Accounts Receivable.
Menu option 1: Allow interest transactions to age from Current, to: 30, 60,
90, and 120+ days old.
Menu option 2: Do not allow interest transactions to age. Always have them
report as Current entries.

Aging at EOD
This option will allow you to choose whether the Calculate Receivables Aging
programs will run as part of the Accounting End of Day job.
Menu option 3: Run the Calculate Receivables Aging programs as part of
Accounting End of Day.


6 X63-7 ¢ OPT RECEIVABLES MENUS. RELEASE 2.2
————————— SSSA 008

 

Menu option 4: Do not run the Calculate Receivables Aging programs as part
of Accounting End of Day.

Interest Calculation

This option will allow you to choose whether to have the system calculate new

interest on all charges including past interest or not including past interest.
Menu option 7: Calculate interest on all charges including past interest.
Menu option 8: Do not calculate interest on past interest.

OPT Receivables Menu Four

>_>

COMMAND: MENU: X6374 uN

{c} DIS Corp

 

OPT RECEIVABLES MENU FOUR

 

Aging 1. Do not age credits
2. Age credits

Corporate 3. Corporate Receivables Address function is not active

Address 4. Corporate Receivables Address function is active (
Zero Amount 5. Do not post zero amount transactions to receivables

Transactions 6. Post zero amount transactions to receivables

Receivables 7. Print payment detail on X11-1 Inquiry printout

Inquiry 8. Do not print payment detail on 11-1 Inquiry printout

23. Return to OPT Receivables Menu Three 24. OPT Receivables Mem Five

Ready for option number or command

se=>

 

 

 

Aging
This option will allow you to choose whether or not receivables credits are aged
along with debits which are always aged.

Menu option 1: Do not age credits.

Menu option 2: Age credits.

Corporate Address
This option will allow you to activate the Corporate Receivables Address
function.
Menu option 3: Corporate Receivables Address function is not active. C)


SECURITY & CONFIGURATION X63-7 « OPT RECEIVABLES MENUS 7

 

Menu option 4: Corporate Receivables Address function is active.

Zero Amount Transactions
This option will allow you to choose whether or not transactions with a zero
amount will be posted to the receivables subledger.
Menu option 5: Zero amount transactions will not be posted to receivables.
Menu option 6: Zero amount transactions will be posted to receivables.

Receivables Inquiry
This option will allow you to choose whether or not payment detail will be printed
on the Receivables Inquiry printout.

Menu option 7: Print payment detail on the X11-1 Inquiry printout.

Menu option 8: Do not print payment detail on the X11-1 Inquiry printout.

OPT Receivables Menu Five

es
COMMAND MENU: X6375 WN
(ce) DIS Coxp

 

Enter i, Do not retain doc# from preceding payment during entry
Payments 2. Retain doc# from preceding payment during entry

3. Do not retain desc from preceding payment during entry
4. Retain desc from preceding payment during entry

5. Do not retain doc# from preceding receipt during entry
6. Retain doc# from preceding receipt during entry

7. Do not retain desc from preceding receipt during entry
8. Retain desc from preceding receipt during entry

23. Return to OPT Receivables Menu Four 24. OPT Receivables Menu Six

Ready for cption number or command

  

 

 

Enter Payments
This option will allow you to choose whether or not, when entering new
payments, the document# from the preceding payment will be retained in the
document# field for the current payment you are entering.

Menu option 1: Do not retain the document# from the preceding payment.

X63-7 ¢ OPT RECEIVABLES MENUS RELEASE 2.2

Menu option 2: Retain the document# from the preceding payment.

Enter Payments
This option will allow you to choose whether or not, when entering new
payments, the description field from the preceding payment will be retained in the
description field of the current payment you are entering.
Menu option 3: Do not retain the description from the preceding payment.
Menu option 4: Retain the description from the preceding payment.

Enter Payments
This option will allow you to choose whether or not, when entering new receipts,
the document# from the preceding receipt will be retained in the document# field
for the current receipt you are entering.
Menu option 5: Do not retain the document# from the preceding receipt.
Menu option 6: Retain the document# from the preceding receipt.

Enter Payments
This option will allow you to choose whether or not, when entering new receipts,
the description field from the preceding receipt will be retained in the description
field of the current receipt you are entering.
Menu option 7: Do not retain the description from the preceding receipt.
Menu option 8: Retain the description from the preceding receipt.


SECURITY & CONFIGURATION X63-7 » OPT RECEIVABLES MENUS 9
ee EE ee MENS

OPT RECEIVABLES MENU SIX

 

COMMAND MENU: X6376 WN
(c) DES Corp

Statements 1. Print the date on statements with the format MMDDYY
2. Print the date on statements with the format YYMMDD
3. Print the date on statements with the format DDMMYY

4. Print statements on the old original style forms
5. Print statements on the new style forms

6. Print an alignment statement
7. Do not print an alignment statement

23. Return to OPT Receivables Menu Five
24. OPT Receivables Menu Seven

Ready for option number or command

Fes>

EO

Statements
This option will allow you to choose what date format you want to print to print
on your receivables statements.
Menu option 1: Print date on receivables statements with the format
MMDDYY.
Menu option 2: Print date on receivables statements with the format
YYMMDD.
Menu option 3: Print date on receivables statements with the format
DDMMYY.

 

 

Statements

This option will allow you to choose the type of form you would like your
receivables statements to print on. You may print on the original style form, or
you may print on the new style form that prints current, 30, 60, 90, and 120+
aging buckets along with a payment stub on the right that tears off for easy
customer payment identification.
Menu option 4: Receivables statements will print on the old style form.
Menu option 5: Receivables statements will print on the new style form.


10 X63-7 e OPT RECEIVABLES MENUS RELEASE 2.2
eee een

Statements

This option will allow you to choose whether or not you would like the first
statement that prints to be an alignment statement to assist you in aligning your
forms on the printer.

Menu option 6: Print an alignment statement.

Menu option 7: Do not print an alignment statement.

OPT Receivables Menu Seven

 

COMMAND MENU: X6377 ww
{c) DIS Corp

 

### Opt Receivables Menu Seven

 

Statements 1. Do net print your company information on statments
2. Print your company information on statments

3. Do not print customer's home phone# on statements
4. Print customer's home phone# on statements

5. Do not print customer's work phone# on statements
6. Print customer's work phone# on statements

7, Do not print monthly GST on statements
8. Print monthly GST on statements

23. Return to OPT Receivables Menu Six 24. OPT Receivables Menu Eight

Ready for option number or command

 

 

 

 

Statements

This option will allow you to choose whether or not you want your company
name and address to print at the top of each statement. If you are running
statements on pre-printed forms, this information may already be printed on the
statements for you. In that case you would not want this information to print. If,
however, your statements do not have this information pre-printed on them, you
would want the program to print it there for you.

Menu option 1: Do not print your company information on the statements.

Menu option 2: Print your company information on the statements.


SECURITY & CONFIGURATION X63-7 « OPT RECEIVABLES MENUS

 

Statements
This option will allow you to choose whether or not you want the customer's
home phone number to print on their statement.
Menu option 3: Do not print the customer's home phone# on the statement.
Menu option 4: Print the customer's home phone# on the statement.

Statements

This option will allow you to choose whether or not you want the customer's work
phone number to print on their statement.
Menu option 5: Do not print the customer's work phone# on the statement.
Menu option 6: Print the customer's work phone# on the statement.

Statements

This option is for Canadian businesses only. With this option, you may choose to
print each customer's monthly GST (Goods & Services Tax) on their statement.
With this option tumed on, a line will print on the statement with the total GST
for the month. Without this option turned on, the individual GST transactions will
still print but will not be separated out and totaled for the month.

Menu option 7: Do not print monthly GST amount on the statement.

Menu option 8: Print the monthly GST amount on the statement.


12 X63-7 * OPT RECEIVABLES MENUS RELEASE 2.2
eee ee eee ASE

OPT Receivables Menu Eight

 

    
   
   
    
 
    
 
  
   
 
 

COMMAND MENU: X6378
{c) DIS Corp

 

### Opt Receivables Menu Eight

Statements 1. Do not print monthly PST on statements
2. Print monthly PST on statements

Enter Payments 3. Print Payment Report and GL Trans Report when
entering payments
4. Print only the Payment Report when entering payments
5. Print only the GL Trans Report when entering payments

Distribute 6. Do not auto distribute payments to oldest unpaid
Payments invoices
7. Auto distribute payments to oldest unpaid invoices

23. Return to OPT Receivables Menu Seven 24. OPT Receivables Menu Nine

Ready Zor option number or command

  

 

Statements

This option is for Canadian businesses only. With this option, you may choose to
print each customer's monthly PST (Provincial Sales Tax) on their statement.
With this option tured on, a line will print on the statement with the total PST for
the month. Without this option turned on, the individual PST transactions will
still print but will not be separated out and totaled for the month.

Menu option 1: Do not print monthly PST amount on the statement.

Menu option 2: Print the monthly PST amount on the statement.

Enter Payments
This option will allow you to choose which reports print out automatically when
entering payments. You may print both the Receivables Payments Report and the
GL Transactions Report, or you may print only one or the other of these two
reports.
Menu option 3: Print both the Receivables Payments Report and the GL
Transactions Report when entering payments.
Menu option 4: Print only the Receivables Payments Report when entering
payments.


SECURITY & CONFIGURATION X63-7 « OPT RECEIVABLES MENUS 13

Menu option 5: Print only the GL Transactions Report when entering
payments.

Distribute Payments
This option allows you to choose whether or not to have payments distributed
automatically to debits against your balance forward type customer accounts.
With the option set on, payments will automatically be applied to the oldest debits
and work their way forward until the payment amount has been used up. With
this option set off, payments will not be applied automatically and must be
merged out manually through Apply Credits.
Menu option 6: Do not automatically distribute payments to balance forward
customers.
Menu option 7: Automatically distribute payments to balance forward
customers.

OPT Receivables Menu Nine

 

[ comauno MENU: X6379 ws
(¢} DIS Corp

Statements 1. Print total outstanding interest on statement
2. Print only current interest charges on statement

Multiple Ship To 3, Multiple Ship To Addresses is not installed

Addresses 4. Multiple Ship To Addresses is installed

Interest and 5. Calculate interest based on individual transactions
Credit entries 6. Calculate interest on the customers account balance
Aging vs. “Days 7. Age transactions based on date posted

until Interest” 8. Begin aging transactions based on delayed interest

23. Return to OPT Receivables Menu Eight

Ready for option number or command

seep

 

 

Statements

This option will allow you to choose whether the total outstanding interest
charges will print in the interest box at the bottom of the statement, or whether
only the current months interest charges will print in that box. All of the interest


14 X63-7 « OPT RECEIVABLES MENUS RELEASE 2.2
eee ELEASE 2.2

transactions from past months that are unpaid will still print on the statement (
regardless of how this option is set.

Menu option 1: Print total outstanding interest charges in the interest box at

the bottom of the statement.

Menu option 2: Print only the current month's interest charges in the interest

box at the bottom of the statement.

Multiple Ship To Addresses

This option will allow you set up multiple Ship To address numbers for each
receivables address in Receivables Maintenance. Once an address number is set
up with additional Ship To address numbers, any one of these address numbers
may be selected from Point of Sale when opening an invoice to the original
receivables customer. If selected from Point of Sale, the name and mailing
address information of the new Ship To address number will display and print in
the Ship To fields on the Sold By screen and on the invoice.

Menu option #3: Multiple Ship To Addresses is not installed.

Menu option #4: Multiple Ship To Addresses is installed.

Setting Up Multiple Ship To Addresses in Receivables Maintenance

 

NOTE
If a customer had an assigned "Ship To" address before the OPT is turned on, and {
you're adding other Shipping Addresses, the original "Ship To" must be added to
the list of shipping addresses so it can be selected at Point of Sale. It will not
default. Shipping addresses are not required to be valid system addresses. They
are stored in a new file, u.ADS.

 

 

When the OPT is on, a command key, Cmd11-Shipping Addresses is available on
the first screen of Receivables Maintenance, as illustrated below:


SECURITY & CONFIGURATION X63-7 e OPT RECEIVABLES MENUS 15

 

 

 

 

 

 

   
    

 

A&R EQUIPMENT SALES RECEIVABLES MAINTENANCE X11201-02
Division: a

Address # PARKOL

Wame .......--.55 GERRY/ PARKER Total Balance .. 3,245.50-
Name (Ext) ...... ** Age as of : 2/09/98
Address 1022 COTTONWOOD DR Current .... 3,245.50~
Address (Ext) ... 30 days past

City, State ..... BELLINGHAM WA 60 days past

Zip Code ........ 98225 90 days past

Telephone # - - 360 650 9987 120 days past

Work Phone # - 360 676 1251 Ext. 45 Interest /Balance 454.50
Fax # -...... - 360 676 5644 Peak Balance ... 70,101.50
Tax Number .....- PARK*78G Account # . Al110

Ship To Address # BADGO1 . it [Limit ... 9999999

Sort Codés .. we Cust Rank

Edit Codes - WOR A Dise code Statement Type . 0 Print? ¥
Credit Estab... N State/Co. FIP Credit Codes (1) (2)
Duns No. & Rating Tax/SIC Code ... A

Note CREDIT LIMITS UP TO $9,999,999 PLUS UP TO 9,999 SHIP TO ADDRESSES
Cmd3-Return Cmd6-Note Cmd?-Print Note Cmd8-Credit Cards Enter-Next pace
Cmd10-Calculate Age Cmdll-Shipping Addresses

 

C1 To assign more than 1 Ship To address, press Cmd11-Shipping Addresses.


16 X63-7 « OPT RECEIVABLES MENUS RELEASE 2.2
ee SSSI EASE 2.02

Shipping Addresses for: PARKOl - GERRY PARKER x11s02

Type option, press Enter - or ~ position by name, city er zip code
isSelect 2=Change 4=Delete

 

Opt Name City/State Zip Code

### Warning!

If the customer had a "Ship To" address assigned before
you turned on the Multiple Shipping Addresses OPT and
you add other Shipping Addresses for that customer, you
must add the original "Ship To" address to the list so it can
be selected at Point of Sale.

There is no change for customers with 1 "Ship To" address.

F3sExit FS5=Refresh Fé=Add Roll

 

 

O To add a new address, press Fé=Add.


SECURITY & CONFIGURATION X63-7 ¢e OPT RECEIVABLES MENUS 17

Shipping Addresses for: PARKO1 - GERRY PARKER x11S02

Type option, press Enter - or - position by name, city or zip code
isSelect 2=Change — 4=Delete

 

Add new address
Cpt Name Name.
Extended name...

Name, City, and Address... 2. .

 

Zip Code are Extended address
required when City/State. 2...

"Validate Zip code... 1.

blanks=Y"; jalidate blanks . . ¥ (¥ for name, city and zip)
otherwise,

blanks are FasPrompt = F2=Return

allowed in 1 or
more of these
fields.

  

For example, you might want to use the name & address
fields tor a note that will always be printed in the Ship To
fields on the document but leave City/State & Zip code fields
blank.

FisExit FS5=Refresh Fé=Add Roll

 

(1 If you are adding a brand new address, which is not in the system, type the
information and press [Enter]. You do not have to use a slash (/) between an
individual's first and last names.

O To select from a list of valid system addresses (from u.ADM), place the cursor
in the Name field and press F4=Prompt address. Make sure to add the
previous "Ship To" assignment, if any.


X63-7 « OPT RECEIVABLES MENUS RELEASE 2.2

 
   
 
 

Shipping Addresses for: PARKO1 - GERRY PARKER

: Select Address 01000

    
   
    
       
  
  
    
  
   

 

 

 

Edit codes. : *ALL

sSelect Division . : *ALL
: Opt Name City/State Zip Code Addr # D:
— A-] PLUMBING MT.VERNON, WA. 87599 APLUOL A:
: _ ADAMS, WILLIAM ARLINGTON, WA 98223 ADAMOL A :
+ _ ADAMS, WILLIAM ARLINGTON, WA 98223 WILL oA:
_ AILINGS,A B FERNDALE, WA 98248 AILIO! B:
ALLBRIGHT COMPANY DALLAS, TX 78222 ALLBOL A:

More... +
: F3sExit Roll :

 

 

F3=Exit  FS=Refresh Fé=Add new address Roll

  

 

O Select a name with 1=Select. You don't have to press [Enter]. The name is
retrieved to the previous screen.
O Press [Enter] to accept it. The name is added to the list.


SECURITY & CONFIGURATION X63-7 » OPT RECEIVABLES MENUS 19
——eEe——e—e=erorrm' ''Or>s sO OE TEeEeE——EEEE_E_T— OTOH

 

Shipping Addresses for: PARKO1 ~ GERRY PARKER 11802

Type option, press Enter - or - position by name, city or zip code
isSelect 2=Change 4-Delete

 

The original
opt Name City/State Zip Code "Ship To"
- BELLINGHAM address
_ CASH N CARRY BELLINGHAM WA 99226 must be on
— LYNDA MORGAN BELLINGHAM WA 99225 this list
— MINHARO WAREHOUSE a“
_ Robin Badger Builders Bellingham, WA 98226

Option 1=Select is not allowed when you use this screen from
Receivables Maintenance. This same screen is presented
immediately after the Entrance screen at Point of Sale.

Bottom
F3sExit F5=Refresh F6=Add Roll
DIS-9902 Shipping address added
aaa

 

 

O To change Shipping Addresses, select 1 or more with 2=Change. Type over
the existing information and press [Enter] to record your changes.

O To delete Shipping Addresses, select 1 or more with 4=Delete. A confirmation
screen is presented. Press [Enter] to delete the name.

O To return to Receivables Maintenance Screen 1, press F3=Exit.

Using Multiple Ship To Addresses at Point of Sale

For customers with multiple Shipping Addresses, the Shipping Address screen
illustrated above is presented immediately after the Entrance screen. This is true
whether or not there is a Ship To system address assigned on the customer's
master record (Screen 1 at Receivables Maintenance).

O To use one of the shipping addresses from the list, choose it with 1=Select,
and press [Enter]. You'll proceed to the Sold To screen where the selected
shipping address information will be filled in automatically.

 

NOTE
To change the Shipping Address after you're on the Sold To screen, type over the
information in the "Ship to" section. There is no way to go back to the list of
Shipping Addresses.


20 X63-7 » OPT RECEIVABLES MENUS RELEASE 2.2
oO Oem EL EASE 200

Interest and Credit Entries
This option will allow you to choose how interest charges are calculated. Will
unmerged credits be ignored and interest calculated on the individual unpaid
balances of past due charges?
Will the calculation include unmerged credit entries along with charges that are
past due, therefore calculated on the "net" balance of the account?
Menu option 5: When considering how much interest to charge, ignore the
fact that the account may have unmerged credits and charge interest on the
past due debits.
Menu option 6: When considering how much interest to charge, subtract
unmerged credits from the overage debits and charge interest on the net
difference regardless of the age of the credits.

Aging vs. "Days Until Interest"
This option changes the date a transaction will begin aging versus the date the
transaction becomes subject to interest being charged against it.

Leroy Grady buys a tractor on June 10, 1998 and the dealership gives him 90 days
free interest. His account does not have anything in the days interest default in
X11-2, but the dealership has 30 days defined as the default in X6-6 (Security
Maintenance). The dealer uses apply credits to change this transaction to 90 days
until interest. When the aging program looks at this transaction (with the opt on)
the "calculated transaction date" would be:

90 - 30 + 06/10/98 or 60+06/10/98 or 08/09/98

The rest of the aging would work normally using the 8/9/98 calculated date and it
would show as current until 30 days has passed since 8/9/98 -----> which is
9/8/98, the date 90 days from the original purchase.

Based on the example above ... (the interest calculation being the same)
Menu option 7: The transaction would age to 30 days as of 7/10/98.
Menu option 8: The transaction would age to 30 days as of 9/08/98.

## CHAPTER X63-8

OPT SERVICE MANAGEMENT MENUS

OPT SERVICE MANAGEMENT MENU (X638)

COMMAND
(c) DIS corp

Inquire/update . When adding additional jobs, do not use the model
Service Units as the default group code
- When adding additional jobs, use the medel as the
default group code

Standard Jeb - Do not page break for each standard job
Report . Page break for each standard job

. Return to OPTDIS Master Menu

Ready for option number or command

ase>


X63-8 OPT SERVICE MANAGEMENT MENUS:

 

Inquire/Update Service Units

During reconmended maintenance, additional jobs can be added to the initial
repair order, When this is done a group code is identified to locate the
correct job code. With this option the model of the unit can be used as a
default for the group code.

Menu option 3: Do not use the model as a default for the group code when
adding additional jobs during recommended maintenance.

Menu option 4: Use the model as a default for the group code when adding
additional jobs during recommended maintenance.

  

Standard Job Report {

This option allows you to determine whether the standard job report
should print each job code on a new page.

Memu option 3: Do not page break for each standard job.

Menu option 4: Page break for each standard job.

 

L

## CHAPTER X63-9

OPT UNITS MENUS

OPT UNITS MENU ONE(X639)

COMMAND:
, (c) DIS Corp

Flooring/Inventory 1. Print ‘Color’ as heading fer color code field
Report 2. Print ‘Mfg#' as heading for color code field

Ingaire/Update Display transactions w/o security ccde entered

Units De net display transactions w/e security code entered

Flooring Update Flooring Due Date when unic is sold
Due Date - Do not update Flooring Due Date when unit is sold

23. Return to OPTDIS Master Menu
24. OPT Units Menu Two

Ready for option number or command

 

Flooring/Inventory Report-Color Code

Many dealers have used the color code field to enter a manufacturer
floozing invoice mumber. The Flooring/Inventory report prints the color code

field. This option allows you to select the wording of the heading for this
column

Menu option #1: Print the word "Coler" as the title of the color code field.

Yienu option #2: Print the word "Mfg#" as a title of the color code field.

## X63-9 OPT UNITS MENUS

Inquire/Update Units - Security Code for Transactions

‘You may go into X2-2 Inquire/Update Units without entering a security code at

the security gate. If no security code is entered, you are in INQUIRY mode and
may not update any fields. The cost fields on the Units Information screen
will also not display. With this option you may decide whether to display the
transaction screen when someone is in this INQUIRY mode.

Menu option #3: Display transactions even without the security code entered.

lenu option #4: Do not display transactions without the security cede entered.

  

Flooring Due Date

option will allow the user to choose whether or not the Flooring Due (
is automatically when a particular unit is sold.

option #5: Automatically update Flooring Due Date when unit is sold.

option #6: Do not update Flooring Due Date when unit is sold.

 


OPT UNITS MENU TWO(X6392)

COMMAND MENU: X6392
{c) DIS Corp

Depreciation , Do Not Subtract 1st ¥r/179 Depreciation field
from Past Depr when calculating batch
Subtract 1st ¥r/179 Depreciation field from
Past Depr when calculating batch

Advanced Rental . Standard 7" invoice
Contract/Invoice . Long 11" inveice
Form Length - Extra long 14" invoice

23. Return to OPT Units Menu One
24. OPT Units Menu Three

Ready for option number or command

  

SECURITY & CONFIGURATION


 

Depreciation

When a business depreciates their fixed assets they may elect to use the
Section 179 first year depreciation. A field has been designated on the
information screen of Inquire/Update Units as ‘First yr/179' for this purpose.
When a depreciation batch is calculated, a user may want to have the amount in
this field subtracted from the amcunt in the ‘Past Depr’ field before using
that field to calculate the current depreciation.

Menu option #1: Do not subtract First Yr/179 Depr field from Past Depr when
calculating a depreciation batch.

Menu option #2: Subtract First ¥r/179 Depr field from Past Depr when
calculating a depreciation batch.

 

Advanced Rental Contract/Invoice Form Length

The Advanced Rentals application allows the dealer to print Rental

contracts onto POS invoice forms instead of formal contract forms.

If this option has been selectei (Advanced Rentals Menu X96-9), you
will need to further define the PS invoice forms length.

 

Use this option to select the size of invoice you will be using...

Menu option #3: 7" invoice

Menu option #4: 11" invoice

Menu option #5: 14" invoice

 

RELEASE 2.2 S


OPT UNITS MENU THREE(X6393)

‘COMMAND MENU: X6393
{c) DIS Corp

MENU THREE
unit Sales Do not restrict sale of RE status rental units
Restrict sale of RE status rentai units

Rentals ~ . Do not remove Rental Start Date when sold
Start Date Remove the Rental Start Date upon sale of Unit

Sold Units . Include only customers who have purchased a unit
Inquiry Index Include ALL customers from the Address Master file

. Return to OPT Units Menu Two

 

Ready for option number

 

SECURITY & CONFIGURATION


Unit Sales

Units which are currently on-rent ere marked with a rental status of RE.
This option determines whether the system allows a sale of a unit which
has a rental status of RE.

Menu option #1: Do not restrict the sale of rental units waich have a
rental status of RE

Menu option #2: Restrict the sale of rental units which have a rental

status of RE

### Warning

You must be using a sale account with an "S" edit code. Rental income
accounts typically have "R" edit codes, while sales accounts have "S" (

 

Rentals - Start Date

Units which are in a rental stetus are marked with a Rental Start Date.
This option determines whether th= system allows the date to be blanked
out during the sale of a rental unit.

Menu option #3: Do not remove the Rental Start Date in Units Maintenance
during the Sale of a rental unit. Leave the date intact.

Menu option #4: Remove the Rental Start Date in Units Maintenance during
the sale of 2 uniz.

 

RELEASE 2.2 LL


Sold Units Inquiry Index

This option will determine the apzearance of the Sold Units Inquiry -
“Customer Index* (Units Menu X2 - option 3). The content of the customer
index will be based on the selected option below.

Menu option 45: Only include customers who have purchased a unit.

Menu option 46: Include ALL customers from the Address Master file in
the customer index.

 


 

SECURITY & CONFIGURATION


Notes:

## CHAPTER X63-10

OPT SYSTEM MENUS

OPT SYSTEM MENU (X63A)

COMMAND MENU: X638
{e] DIS Corp

IPL Startup . Automatically ran startup procedures during

2. Do not run startup procedures during IPL
Automatically run startup including cache

Executive 4. The Executive System is not insralied
System 5. The Executive System is installed

Return to OPTDIS Master Menu

Ready for option number or command

## X63-10 OPT SYSTEM MENUS

 

IPL Startup

Puring the IPL process the systet

 

can automatically update the Point of Sale
customer index, prepare the sold units inquiry files, run a compress, and
start memory caching.

This option allew you to decide whether or not these jobs should be
automatically triggered during system IPL

Menu option 1: Automatically run the IPL startup programs except for cache.

 

Menu option 2: Do not run the IPL startup programs.

nu option 3: Automatically run the IPL startup programs including cache.

 

Executive System

The Executive System is an advanced reporting and data management tool
available from DIS. It uses the iatest °C technology to present inventory
and financial information from the AS/¢00 in a easy-to-use graphical
interface on the PC.

Please call DIS for more information about the Executive System.

Menu cption #4: The Executive System is not installed

Menu option #5: The Executive System is installed.

 

 

 

## CHAPTER X63-11

OPT MANUFACTURER MENUS

OPT MANUFACTURERS MENU ONE (X63B)

COMMAND
(ce) DIS Corp

MANUFACTURERS

‘Thermo King features in P.0.S. are not installed
Features - Thermo King features in P.O.S. are installed

Canadian Thermo nip is not a Canadian TX dealer

King Dealers @ Canadian TK dealer that uses
part category to calculate landed cost
Deale’ is 2 Canadian TK dealer that uses
part class to calculate landed cost

23. Return to OPTDIS Master Menu
24. OPT Manufacturer Menu Two

Ready for option number or command

## X63-11 OPT MANUFACTURERS MENUS

 

Thermo King Features

Thermo King dealers have a number of special features available in Point of
Sale if this option is set on

Menu option #1: Thermo King features in P.O.$. are not installed.

Menu option #2: ‘Thermo King features in P.O.S. are installed.

 

 

Canadian Thermo King Deaiers

‘This menu option allows you to specify whether your dealership is a
Canadian Thermo King dealership and whether you want the system to
calculate a landed cost for parts based on part category or part class. (

Menu option 3: Dealership is not a Canadian Thermo King dealership.

Menu option 4: Dealership is a Canadian Thermo King dealership using
the part category to calculate landed cost.

Menu option §: Dealership is a Canadian Thermo King dealership using

the part class tc caiculate landed cost.

 


RELEASE 2.2 Ww


OPT MANUFACTURERS MENU TWO (X63B2)

coKaND
(c) DIS Corp

DIS Ltd.
F & I Package

1H
Communications

Parts Voice

John Deere
Financial

. DIS Ltd. F & I Package is not installed
. DIS Ltd. F & I Package is installed

IH Communications is not installed
TH Communications is installed

Parts Voice is not installed
Parts Voice is installed

. John Deere Financial Download is not installed
. John Deere Financial Download is installed

23. Return to OPT Manufacturers Menu One 24. OPT Manufacturers Menu Three

Ready for option number or command

DIS Ltd. F & 1 Package

DIS Ltd. has an F & I Package £

 

eC that many of their auto dealers

use in conjuction with the AS/49b oz $/36. Those dealers need to have this

option set on.

Menu option #1: DIS Ltd. F & I Package is not installed

feru option #2: DIS Ltd. F & I Package is installed.

SECURITY & CONFIGURATION


tH Communications

‘Dealers that communicate their parts orders to IH need to have this option
set on.

Menu option #3: IH Communications is not instalied.

Yienu option #4: IH Comminications is installed.

Parts Voice

Dealers who send parts locator information to Parts Voice need to have
this option set on.

Menu option #5: Parts Voice is not installed.

enu option #6: Parts Voice is installed

John Deere Financial

‘John Deere dealers have the option of automatically downloading
financial information to the PC.

Menu option #7: John Deere Financia) powmload is not installed.

Menu option #8: John Deere Financial Download is installed

 
CC


OPT MANUFACTURERS MENU THREE (X63B3)

COMMAND
(c) DIS Corp

Case Credit
Communications

Credit card
Payment.

Electronic
Commerce

Ready for option number

SECURITY & CONFIGURATION

MENU: X63B3

. Case Credit Communications is not installed
. Case Credit Communications is installed

+ Total invoice amount paid by C/c will print the total
. Total invoice amount paid by C/C will print as zero

» Electronic Commerce Communications is not installed
6, Electronic Commerce Communications is installed

- Return to OPT Manufacturers Menu Two
. OPT Manufacturer Menu Four

or command


X63-11 OPT MANUFACTURERS MENUS a ~

Case Credit Communications

  

  

With this opticn set on, Case dealers will be able to set up their Case
credit card customers using the new credit card application and process the
credit card data directly through the system with Case Corporation.

 
   
  

  

Menu option #1: Case Credit Communications is not instailed.

  
 
  

    
 

Menu option #2: Case Credit Communications is installed,

Credit Card Payment

This menu option allows you to alter the way a Point of Sale invoice
prints the “Total Amount" at the bottom. This option is only considered (
for invoices which were completely paid by a credit card.

Menu option 3: Print the total amount of the invoice at the bottem when
the total amount is paid by credit card payment.

Menu option 4: Print a zero amount at the bottom of the inveice when the
total amount is paid by credit card payment.

 

Electronic Commerce

This menu option allows you to install the Electronic Commerce
Cormunications application to process various manufacturers communication
transactions,

Menu. option 5: Electronic Commerce Communications is not installed.

Menu option é: Electronic Comm Communications is installed.

 

tC


OPT MANUFACTURERS MENU FOUR (X63B4)

COMMAND MENU: X63B4
(<) DIS corp

UFACTURERS MENU FOUR

Case Order Case Order Fulfillment is not installed
Fulfillment Case Order Fulfillment is installed

Farm Plan . Farm Plan Communications is not installed
Communications . Farm Plan Communications is installed

Farm Plan 5. The Farm Plan offset entry is a batch total
Transactions 6. Create detail Farm Plan offset entries

23. Return to OP? Manufacturers Menu Three

Ready for option number ox command

 

Case Order Fulfillment

Case Order Fulfillment is a program that allows Case to create suggested parts
orders, returns, and transfers for dealers. The goal of Order Fulfillment is
to help you manage your inventory =o achieve the fill and turn rates you want.
The program must be set up throug Case Corporation and then will work in

conjunction with the DI§ Business System once this option has been set on.

Menu option #1: liment is not installed.

Menu option #2; Case Order Fuliiliment is installed

 

SECURITY & CONFIGURATION


Farm Plan Communications

Dealers that use Farm Plan for their receivables and download that
information through Farm Plan Communications need to set this option.

 

Mema option #3: Farm Plan Communications is not installed.

Menu option #4: Farm Plan Communications is installed.

 

Farm Plan Transactions

option will alter the Farm Plan offsetting transaction entry{s)
are created for the POS posting batch in Create Source Documents.

option #5: A single offsetting transaction entry will be created
which will accumulate the batch total.

option #6: A detail offsetting transaction will be created for each
individual farm plan entry in the batch.

 
LL

## CHAPTER X68-1

CREDIT CODE MAINTENANCE

### Introduction

Credit Code Maintenance allows you to:

= add credit codes with messages assigned to Receivable Customers.
= update or add credit messages shown on the Customer Credit List and

displayed at Point of Sale.

 
 

### Warning!

Point of Sale Lockout, which is an OPT, uses a "Z" credit code; i
therefore, don't use "Z,"

## X68-1 CREDIT CODE MAINTENANCE

 

### How To Run

From the Initial Data Entry Menu, select option 1, Credit Code
Maintenance.

The list of current credit codes is displayed.

Credit Code Maintenance
List

Opt Code Message
- Never Charge
- Cash only
No Interest Charged
Credit Not Established (
30 Days Past Due
60 Days Past Due
90 Days Past Due

120 Days Past Due
Aredit limit

F3sExit F6=Add P12=Previous

 

Messages associated with the system-assigned codes cannot be changed.

O To change user-defined messages, place the cursor in the message field
you want to change. Type over the old message. Press [Enter] to record

f
RELEASE 2.1 Ve


the change.
O To delete a user-defined code and message, select it with 4=Delete and
press [Enter].
O To add a code and message, press Fo=Add.

F3=Exit

F12=Previous

 


 

Credit Code Maintenance
List

Cede Message

brrarred

O Type codes and their associated messages. Press [Enter] to record them
and receive a new, blank list. When you are done, press F12=Previous
to return to the full list or press F3=Exit to end the job.

SECURITY & CONFIGURATION


Notes: ey
(

RELEASE 2.1 Ne

## CHAPTER X68-2

RECEIVABLES AGING ENTRY

### Introduction

Receivables Aging Entry allows you to:

= change the Aging Receivables balances for balance forward customers.

### How To Run

From the Initial Data Entry menu, select option 2, Receivables Aging
Entry.

Select the address number for the balance forward customer that needs
correcting.

The following screen will display:

RECEIVABLES AGING ENTRY

Receivables balance ... 26516.78

2633430
30 days past due :
60 days past due ...... 6796
90 days past due

## X68-2 RECEIVABLES AGING ENTRY

 

Type in the dollar and cents amount into each field:

CURRENT

30 DAYS PAST DUE
60 DAYS PAST DUE
90 DAYS PAST DUE
SERVICE CHARGE

Press ENTER.

If the amounts keyed in do not equal the RECEIVABLES BALANCE
listed on the screen, a message will appear. Simply enter the correct
figures in each field so they add up to the Receivables Balance. Press
ENTER.

OPTIONS:
O Continue to enter Customer's Address Numbers to age their
Receivables balances.

 

 

 

 

Press Cmd1 to end the job and return to the Initial Data Entry Menu.

RELEASE 2.1 C “

## CHAPTER X68-3

GENERAL LEDGER HISTORY ENTRY

### Introduction

General Ledger History Entry allows you to:
- enter history for your General Ledger Accounts after being installed on
the DIS system.

= change history balances for all but the most recently closed General
Ledger month.

### How To Run

From the Initial Data Entry Menu, select option 3, General Ledger History
Entry. Enter the general ledger account number to be updated.

Note:

After you press ENTER, the General Ledger Title and Past 25 Months’
history appears on the screen.

 

Type in the dollar and cents account balances for each of the previous 24
months in the fiscal year. Start with History #2, which is the second to the
jast closed month. Notice on the screen that only the CLOSED General
Ledger months are shown. Press ENTER.

## X68-3 GENERAL LEDGER HISTORY ENTRY

 

GENERAL LEDGER HISTORY ENTRY 6830-101 1

Account #: A1110
Title: ACCOUNTS RECEIVABLE
Past 25 month's history (previous month first)
1662068 2 48526 3 412767 4 1736786
6 7 8
10 a 12
14 15 16
18 29 20
22 23 24

Month #1 (previous month) cannot be updated and is shown for information only.

Month #2 refers to the month before last with month #25 being the oldest month
listed.
CC

## CHAPTER X68-4

FINANCIAL STATEMENT FORMAT MAINTENANCE

### Introduction

Financial Statement Format Maintenance allows you to:

= establish subtotals of General Ledger accounts for financial statements.

 

| Financial statements for all divisions share the same subtotals.

### Preparation

O Locate or run a Chart of Accounts (X14-2). Current subtotal numbers
are listed at the end of the Chart of Accounts.

O Locate or run a Financial Statement (X15-2). Study the current format
to decide what you want to change.

 

 

 

 

Read the discussion at the end of this chapter, "HOW TO ADD A
SUBTOTAL."

## X68-4 FINANCIAL STATEMENT FORMAT MAINTENANCE

 

### How To Run

From the Initial Data Entry menu, select option 4, Financial Statement
Format Maintenance. A prompt for a subtotal number appears. Eight
characters are available.

ABC COMPANY FINANCTAL STATEMENT FORMAT MAINTENANCE X6840-001 1
Division: a

Subtotal number:

 

 

 

0 Enter a subtotal number. Do not use a division letter. {
O Press [Enter}.
The full screen is displayed.

RELEASE 2.1 Lo


 

ABC COMPANY FINANCIAL STATEMENT FORMAT MAINTENANCE X6840-001 2
Division: A

Subtotal number; ** New subrotal **

Title: **TOTAL CASH*## THR ER nee
Level Number: 2
General Ledger Type: A

Eater ‘Y' to delete:

 

O Type the Title, and press [Field Exit].

 

 

 

 

Type the Level Number, and press [Field Exit].

O Type the General Ledger Type, and press [Enter].
The subtotal is added, and the prompt is redisplayed.

D Repeat as desired.
0 Press [Cmd1] to end the job and return to the Initial Data Entry menu.

O Check the results by running a financial statement (X15-2).

SECURITY & CONFIGURATION


(

### Fields & Descriptions

The fields are described below.
Account Title 25 characters. Description of the subtotal.
Level Number 1 digit: 1-4. One of four possible levels.
Status No input. New Account#, blank if Current,
or Deleted Accountit.
General Ledger Type 1 character.
A= Asset
L = Liability
S = Sales
C=Cost of Sales
I= Income {
E = Expense
Possible Action Y or blank. “Enter Y to delete" allows you

to delete a current account.
Y or blank. "To reinstate, enter Y" allows
you to use an account which was canceled.

ADDING A SUBTOTAL

Subtotal Number

Subtotal numbers correspond to General Ledger account numbers without
the division code as the first character. Remember that financial

RELEASE 2.1 CO


 

statements for all divisions share the same format.

For example, consider the following General Ledger accounts:
A1000 CASH ON HAND

A1020 CASH IN BANK.

A1030 PETTY CASH

A1040 CERTIFICATE OF DEPOSIT
A1100 WHOLE GOODS RECEIVABLE
A1110 ACCOUNTS RECEIVABLE
A1120 WARRANTY RECEIVABLE

To set up a subtotal for cash, select a subtotal number that is higher than
the last general ledger account number for cash and lower than the first
account number for receivables. Account number 10999 is appropriate,
and is illustrated on the screens above. General Ledger accounts for cash
can be inserted easily without changing the financial statement format.

Title

The convention is to use asterisks before the title to visually indicate the
level of the account. For example, Total Inventory is usually a Level 2
account. Enter the title like this:

**TOTAL INVENTORY ####*
(25 character field)

It is quickly identified as a Level 2 account and also is spotted quickly on
your financial statement due to the row of asterisks following the title.

SECURITY & CONFIGURATION


Level Number

The level number is a single digit: 1, 2, 3, or 4. Examples of the 4 different
levels of accounts are:

### Level 1 Level 2 Level 3 Level 4

Buildings Total Inventory Current Assets Total Assets
Depreciation Total Cash Fixed Assets _ Total Liabilities
Trucks Total Sales Depreciation

*Other Income

*Only one subtotal is allowed for OTHER INCOME accounts, and it must
be set at Level 3.

ALL General Ledger Accounts are Level 1. Then, the Level 1 accounts
which are subtotaled are considered Level 2 accounts. Each higher level
subtotals the preceding level. You can see that Level 2 accounts are
subtotaled by Level 3 accounts. Level 3 accounts are subtotaled by Level 4
accounts.

Assign the levels so that each higher level subtotals the lower level. Level
1 is the lowest and Level 4 is the highest level.
t
XL


 

There are 5 computer-generated totals which you don't post to directly.
The subtotal numbers must be the highest in your chart of accounts. In the
example below, 99999 is used. ( __ signifies 2 blanks).

Subtotal Level
Number Title Number

99999 5 Operating Profit

99999__6 Other Income

99999__7 Net Profit Before Tax
99999 _ 8 Profit or Loss Current Year
99999_9 Total Liabilities and Net Worth

wee

The Subtotal Numbers for the generated totals must be 8 characters. In the
last available space for the subtotal number (position 8), type the
appropriate digit (5-9) as indicated above.

Note:

 

Any General Ledger type is valid for generated totals.

SECURITY & CONFIGURATION


Notes:

RELEASE 2.1 Lo

## CHAPTER X68-5

INITIAL PARTS DATA ENTRY

### Introduction

Initial Parts Data Entry allows you to:

™ enter new part numbers. This job is used instead of Parts Posting and
Maintenance when you have large quantities of

= parts to add. For example, when you add a new vendor, use Initial Parts
Data Entry.

= enter sales history, prices and parts information on a single screen.

= maintain vendor/class default values.

### How To Run

From the Initial Data Entry Menu, select option 5, Initial Parts Data Entry.

## X68-5 INITIAL PARTS DATA ENTRY

 

The following screen will display:

INITIAL PARTS DATA ENTRY X68S0-101

Division. A
Vendor... Class...
Part number. . Description. .

On hand. Location... order code..
Diz List Based on...

Sug List Based on...

Internal Based on...

Dir Net.

Package. i Multiple qty
Weight. . wee Return code.

Moye Demand
13,

1 6.
Ig. (

Cmdl-End job.

 

 
 

Note:

Press FIELD EXIT to advance to the next field if you do not use the
entire character/digit limit of the field.

  
  

     

(
RELEASE 2.1 WS

### Fields & Descriptions

Vendor

Class
Part Number

Description
On hand

Location
Order Code

Dir List

Based on
Sug List
Based on

Internal

Based on

SECURITY & CONFIGURATION


 

3 characters. Vendor Code for the
manufacturer.

1 character. Classification code.

22 characters. Identifying part number. Enter
the part number in segments. Each vendor
has been configured with 1 to 4 segments. If
you've forgotten, request a Configuration
Report at X382. Then check the part number
to see where its segments are. Between each
segment and after the number typea .

16 characters. Brief description of the part.

5 digits. Number of the part you have on
hand.

8 characters. Bin location of the part.

1 character. A for Automatic, M for Manual,
or C for Combined.

7 digits. Selling price, in dollars and cents
no decimals.

I digit. Base price (1-4) to figure Dealer
List. Usually 3 for Suggested List.

7 digits. Manufacturer's suggested list price.
Type in dollars and cents, no decimal.

1 digit. Base price (1-4) to use as Suggested
List. Use 3 for Suggested List.

7 digits. Field used for any reference price,
dealer-defined; sometimes used for
competitor's price. Type in dollars and cents,
no decimal.

1 digit. Base price (1-4) to figure Internal


Dir Net
Based on
Package

Per job
Multiple

Weight
Disc Qty
Return Code

Sales History

Moyr
Qty
Demand
Memo

Press ENTER.

from. Usually 1 for cost or Dealer Net.

7 digits. Cost of the part, in dollars and
cents, no decimal.

1 digit. Field to base the Dealer Net on.
Use 1.

5 digits. Package quantity, how many per
vendor package.

3 digits. Number needed per job.

5 digits. Amount in a bulk package (i.e., 55
gallons of oil, enter 55).

5 digits. Weight of the part.

5 digits. Quantity to order for a discount.

1 character. Optional field to note whether
the part is returnable or non- returnable.
Start with the oldest month. Don't

bother to enter those months without any
sales history.

2 digits each. Month and year for sales
history.

2 digits. Number of parts sold in that month.

2 digits. Number of people requesting the

part in that month.
80 characters. Comment line.


 

OPTIONS:

Continue to enter parts numbers.

Note the defaults on the screen after the entry of the first part:
Vendor/class, order code and base prices default. To change the
defaults, type in the new information in the field over the default. Press
FIELD EXIT.

 

 

 

 

O Press CMD 1 to end the job and return to the Initial Data Entry Menu.
You will receive an Initial Parts Data Entry Log from the printer. Keep
this report as an audit trail of changes made to your parts inventory.
Transactions made to your parts with this job do not appear on your
Parts End of Day report.

INITIAL PARTS DATA ENTRY Loc Date 10/01/86 Page 1
‘Time 15.27.06 6850-14

WORKSTATION WL

VEXDOR PART NUMBER
035722 Pm ca-4177
035723 PM 4 1455999
035723 Pm a2ss2e

038920 Pa asoaess |

 

### Fields & Descriptions

Counter Sequentially numbers your entries.

Time Two digits of hours, minutes, seconds; PM
: or AM.

Vendor Vendor code of the entry.

Part Number Part number entered.

Description Description of the part entered.

SECURITY & CONFIGURATION


Notes:

é

RELEASE 2.1 Na

## CHAPTER X68-6

POS CODES REPORT

### Introduction

This job prints the following DIS codes for the division selected at the
security gate:

 

 

Credit Messages (X68-1)

Price Tables (X52-9)

O Tax Codes (X52-7)

O Discount Codes (X52-6)

UO) Document Classification Codes (X52-2)
Sales Codes (X52-3)

O Standard Line Codes (X52-5)

 

 

 

 

 

 

These codes can also be printed from the individual jobs; however, the
purpose of the POS Codes Report is provide lists to attach to workstations
for easy reference.

### How To Run

From the Initial Data Entry Menu (X6-8), select option 6, POS Codes
Report. At the security gate, select the division. The report is sent to the
job queuc. The report is illustrated on the pages that follow.

## X68-6 POS CODES REPORT

 

CREDIT MESSAGE TABLE
ce Message
+ wever charge
cash only
No Interest Charged
Credit Not Established
30 Days Past Due
60 Days Past Due
90 Days Past Dua
credit Limit

mnsce cot tas
Sek/Aact Vad Cle dave Base
sua 300
menue? cas anne
arisen cad 5 1000
pear Laon
femaoo; eas 30008
sev tates
zante

ea)

zeroes

dencnon

zones

toes: (
onroc:

sores

remctt

rennet

neue

anor

neue

zemsent

mates

ctoet

mene:

 

SALES TAX TABLE

cd Rate Bese
A 7.80% ACCRUED SALES TAK
e s
8 a
@ a
7 10.00 % ACCRUED SALES TAX
x 2
5 5.00 & ACCRUED SALES TAX

 


ca piscoune,

90.00 %
18.00
32.50
5.00
5.00
5.09
-50
30.00
5.00
1,00

DOCUMENT CLASS TABLE
Description
Change Now
© document,
SELF SERVICE
INVOICE
REPATR ORDER
ONTT SALE
nines

UNIT RENTAL
WORK ORDER

x Bee

pes

ca
a
¢
zg
1
R
s
.
v
w
x
2


X68-6 POS CODES REPORT e

 

beak

CODE TARLE
Description
RCVD oN ACCOUNT
MISC DESC.


UNI? RADE

PAID OUTS
TABOR CUST MISC
LASOR INT MISC
UNITS TRADE IN
FREIGHT

EABOR CUSTOMER
LASOR INTERNAL
TASOR WARRANTY

MISC SALES
PTS CUST MISC

PARTS INT MISC
PARTS SHOP MISC
PARTS WHOLE MIS

ER SSSHRRAAAESHS2dRB es
ReEZEE EOE rr UUU ese oe

nove 1
NOPE #2

NOTE 93,

NOTE 44

SELP SERVICE
PARTS CUSTOMER
PARTS INTERNAL

REESSE

TIRES & TUBES
PARTS SHOP
PARTS WHOLESALE
cus? Deposzts
SUBLET SALE
TEST TCODE
TEST °T!

RENTAL OTHER
RENTAL DEFAULT
RENTAL
EQUIPMENT SALE

Secesanavvvs eee eZee

Beeesaaas

 

RELEASE 2.1 LC


 

STD LINE - Isc DESC
ca Sis-ce Description
Testa 7 eeco0c
STD LINE - LABOR

ca Sis-ca I/#  Enplyce
REGLAR TC

TESTS Tr HAL
STD LINE - MISC OTY

ca Sis-cé tescription
OIL = MS OOTL, FTUTER AND
Testl wm rest?

TRSTIO wm TEST

97D LINE - PART

ca peser

REBATE CASREBATEOL
TEST? SOME PART

STD LINE -COST/MISC PART
ca Sis-ca Description
ss ss TEST oe
STD LINE - WHOLE GooDs
Ca sistockkescription
ss SS TEST testes
Tests AEC

 


Notes: C ~

(.

## CHAPTER X68-7

RENAME CUSTOMER NUMBERS

### Introduction

Use this option to change one or more customer or other system address
numbers, such as vendors, employees, marketing. Address numbers are
changed in all DIS Business System files.

 

### How To Run

Q From the Initial Data Entry Menu (X6-8), select option 7, Rename
Customer Numbers. You are prompted for the original customer
address:


[2] X68-7 RENAME CUSTOMER NUMBERS c

LEE'S RENTAL COMPANY Rename Address Numbers %6870-101
Selection Screen

Address number to change from +++ 009004

Cmdl-cancel  Cmd6-Continue

 

O Enter the first customer address number and press [Enter]. The address
number is confirmed.


RELEASE 2.1 NN


X68-7 RENAME CUSTOMER NUMBERS [2]

Rename Address Numbers 6870-102
Selection Screen

Address number to change from

Pat Rose Construction Co.

Address number to change to

cmd3-Previous Screen

 

C Press [Enter] to confirm and return to the prompt.
O Enter another customer address number, or press [Cmd6] to continue
with the changes.

SECURITY & CONFIGURATION

## X68-7 RENAME CUSTOMER NUMBERS

 

During the changes, you will see the following system messages:

X68700

ConRELEASE 2.1

Converting: DAAT, EAAT, CUA, PAA, REA, REH, WGA, WGG, CUH
Converting: DAMT, ATM, SNT, SPA, VHM

Converting: EDT

Converting: EET

Converting: SCA

Converting: SEA

Converting: MOM

Converting: PSH

Converting: PTD

Converting: RAT

Converting: SAC

Converting: SPN

Converting: SSM

Converting: AECP,AEMP,AENP, LJCP,LPPP, LOHP, LUSP,LOTP PASS1
Converting: AECP,AEMP,LOEP,LUSP, PASS2

Converting: ISH

Converting: IAH

Converting: IDH

Converting: SAP

Converting: SAM, SHM, and SUM

DIS-6022 Receivables Files are being reorganized. (
DIS-6023 Payables Files are being reorganized.

Rebuilding Marketing index .

Rebuilding Payable index...

Rebuilding Point of Sale index .

 

RELEASE 2.1 C

## CHAPTER X68-8

RENAME GENERAL LEDGER ACCOUNT NUMBERS

### Introduction

Use this option to change up to 16 general ledger account numbers for all
divisions.

 

Warning!

A dedicated system is required.
Make sure you have a good backup before you begin.

 

### How To Run

From the Initial Data Entry Menu (X6-8), select option 8, Rename General
Ledger Account Numbers. The following screen is displayed:


X68-8 RENAME GENERAL LEDGER ACCOUNT NUMBERS a

LEE'S RENTAL COMPA RENAME GENERAL LEDGER ACCOUNT NUMBERS x6880-001 1
Division: ALL Map Accounts

This job allows the renaming of general ledger account numbers. Since
the DIS system requires all divisions to have the same general ledger
account structure, any changes will be made to all divisions at the
same time

Specify up to 16 different accounts to be renamed. Specify the current
account number(s) and the new account number(s). Do not include the
division code with the account numbers.

From To Title
1110__ 112¢0__

LTT

Enter-Verify accounts Cmdl-Cancel job cma2-Continue Cmdl9-Erase input

 

O To cancel this job and return to the Initial Data Entry Menu without
making any changes, press Cmd1-Cancel job.

1 Type the "From" account number in the 7 spaces provided. Do not type

the division code. Type the "To" account number in the next 7 spaces,

again without the division code. All divisions will be changed at once.

OC To erase your input in al! "From" and "To" fields, press Cmd19-Erase

input.

To verify the "From" account number, press [Enter].

 

 

 

 

L

### X68- 8 Rename General Ledger Account Numbers

LEE'S RENTAL COMPA RENAME GENERAL LEDGER ACCOUNT NUMBERS: X€880-001 1
Division: ALL Map Accounts

This job allows the renaming of general ledger account numbers. Since
the DIS system requires all divisions to have the same general ledger
account structure, any changes will be made to all divisions at the
same time

Specity up to 16 different accounts to be renamed. Specify the current
account number(s} and the new account number(s). Do not include the
division code with the account numbers.

From = To Title From To Title
1110 11190 ACCOUNTS RECEIVABLE 1200-12000 NEW TRACTORS

Enter-Verify accounts Cmdl-Cancel job Cmd2-Continye cmal9-Erase input

 

© To continue with the renaming procedure, press [Cmd2]. The Obtain

dedicated System screen appears. A sample screen is illustrated.

SECURITY & CONFIGURATION


X68-8 RENAME GENERAL LEDGER ACCOUNT NUMBERS C .

A&R EQUIPMENT SALE RENAME GENERAL LEDGER ACCOUNT NUMBERS X6880-002
Division: ALL Obtain Dedicated System

This job requires a dedicated system,

Make sure that no cther jcbs are running on the system and press
Cmd2 te continue

 

Gmdi-Cancel jeb Cmd2-Continue Cmd3-Return to Map Accounts

 

KO

## CHAPTER X71-11

DOCUMENTS FILL RATIO REPORT

### Introduction

This option, from the Case Corporation Menu (X7-1), produces the Documents
Fill Ratio Report. The same option is available from the Case Advanced
Communications Menu (X7-2). The report supplies a means of measuring and
reviewing how many documents have their parts needs completely filled at
initiation. A series of six queries is used to pull this information from POS to
create the report.

PARTS FILL RATE BY DOCUMENT

1. From the Case Corporation Menu (X7-1), select option 11, Documents Fill
Ratio Report.

COMMAND MENU: X71 G4
(c) DIS Corp. Lease/Dial,

 

Lease/Dial Communication Certification Requirements

. Start/Sstop 11. Documents Fill Ratio Report
. Case Returns Menu

. Case Order Menu

. Batch Entry Menu

» Configure

. Batch Status

. Retail Tracking

. Review Case Responses

warnneuvne

. Review Log

23. Return to Manufacturers Menu

Ready for option number or command
sss>ll

 

 

X71B.doc 8/23/99

## CHAPTER X71-11

## * DOCUMENTS FILL RATIO REPORT RELEASE 2.3

2. Press [Enter]. The Documents Fill Ratio Report entrance screen appears.

 

XT1F0-101
Decuments Fill Ratio Report

Date Range: Seginning Month. .... . 0399 (mmyy)

Ending Month. ......, 0399 (mmyy)
Document classifications: Sales types. . ACLSU

Work Order types. . R

Include Warranty Customers? .. . .. . x (yn)
Include Warranty Lines?. . 2 2... 1. ¥ (een)
Include Internal Customers? ...... ¥ (ys)
Include Internal Lines? .. 2. 2... Y Ax /N)
Detail or Summary... -.. 2.2.24. D (D/s)
Cmd@i-End Job

 

 

3. Select a date range for the documents you want on the report. Type a
beginning month (mmyy) and ending month (mmyy). The report will select
documents posted within the date range entered. Lost Sales and Drop Ship
lines are ignored. Clone documents are treated as individual documents,
unrelated to their parents.

4. Choose which document classifications are to be included in the report. A list
of the existing classification codes is presented. You can delete those codes
that should be excluded. It is possible to produce a Sales-only report, for
example, by completely emptying the work order types on the screen.

5. Choose whether or not to include Warranty Customers, Warranty Lines,
Internal Customers and/or Internal Lines.

6. Select whether you want a detail or summary report. For Case reporting
purposes, it may be that only the summary report is necessary.

7. After selecting the parameters you want for the report, press [Enter]. The
procedure is placed on the job queue. Press [Enter] again to return to a main
menu.

When this report is produced, it will likely be with the same parameters every
time. The system stores the parameters of the most recent running of this report
and presents them as the default the next time the report is requested. The
selection criteria and certain other explanatory remarks will appear in the heading
of the report, centered on each line. A sample report is illustrated on the following
page.


MANUFACTURERS

Nut EQUIPMENT SALES
TYNDEN, WA. .
Included:
Lest Sales and
Doc nate
Class Posted = Document
¢ 8/28/98 croo1e2
er90105
cr00107
cro0108
creo.
Subtotals for ¢ 8/28/98:
Subtotals for C:
8/28/98 usooLoc
Subsotals for s 8/28/98:

 

Ro00100
R 8/28/98:

Report Totals:

The data is sorted, printed, and subtotaled by date within classification code,

## CHAPTER X71-11

## e DOCUMENTS FILL RATIO REPORT

Doruments Fill Ratio Report
Dates: 01/28 - 03/99 Dec Class, Sales: ACLSU W/O: R
warzanty customers. warranty lines, internal customers, internal lines.
ip li excluded: Clone decunents are counted as individual docunents.
Lines
Filled
-0%

Lines

Bee ene SB uw ae

Date 3/15/99
Tine 14:42:39

Docs
Filled


x7AF0-
Page 2

Ave. bines
Filled

 

showing all sales classifications first, followed by all work order classifications.
Subtotals are also printed for each classification, for sales and work orders
separately, and for the rest of the report.

## CHAPTER X71-11

## ¢ DOCUMENTS FILL RATIO REPORT

Notes:

## CHAPTER X76-1

DOWNLOAD NH PARTS ORDERS & RETURNS

### Introduction

Use this job to transfer finalized orders, including drop ships, and returns
from the DIS System to a PC. Orders and returns are then transmitted to
New Holland using the New Holland Dealer Communications System
(DCS) programs.

This chapter covers only the transfer from the DIS System to the PC.
Please refer to the DCS manual for instructions about what to do after the
download.

‘You can download only | order or 1 return at a time; however, you can
download as many orders and-returns as necessary before transmitting ~
them to New Holland. Each order or return is limited to 1,000 lines.

Drop Ship Features

= Drop ship orders can now be processed from open invoices (previously
they were accessible from closed invoices only). Priority code "D"
signifies parts that will be drop shipped.

= In addition, Priority Orders (X5-3) has been modified to add a prompt
at the bottom of the Drop Ship Header screen: "Retain Drop Ship Order
for Download? (Y/N). If this prompt is answered "Y," order
information is stored in 2 new order files, ODA and ODM, which are
similar to the regular order files, OAA and OAM. The order number
defaults to the invoice number; it can be changed as long as it is unique.

= After drop ship orders have been processed in Priority Orders, the
priority code "D" changes to "d" on the point of sale invoice, which
remains open for additional charges. Drop ships are downloaded like
any other order.

= Downloaded files are placed in the \DCSDATA directory.

™ On the Collect Parameters screen, you'll find new order types: nye
(Unit Down Drop) and "G" (Fill In Drop).


Ban ae

[2] 76-1 DOWNLOAD NH PARTS ORDERS & RETURNS ,

### Preparation

0 Create the order or return. You can transfer stock, critical, unit down, or
drop ship orders. For more information, refer to the table below, which
lists the function and its corresponding chapter in the DIS HOW TO

RUN MANUAL.
7 TO CREATE: SEE CHAPTER:
Computer generated stock order X341-1 Create Suggested Stock
, Order
Manual stock order 341-2 Correct Stock order or
Create Manual Order
Critical order X5-3 Priority Orders
Unit down order X5-3 Priority Orders i
Drop Ship order X5-3 Priority Orders *
Computer generated stock return § _X35-1 Create Stock Return
Manual stock return X35-2 Correct Stock Return

O Finalize orders in Print/Finalize Order (X341-3), returns in
Print/Finalize Return (X35-4). Only finalized orders and returns can be
transferred. Exception: Drop ship orders come from invoices, which

- may remain open for further charges.

O Make a note of the order, return, or drop ship number, which will be
transferred. If you forget the number, you can find orders (not drop
ships) and returns through Order Inquiry (X34-4).

(
RELEASE 2.1 Nee


X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS [-]

### How To Run

Signing On
Turn on the PC. The PC starts as a DIS System terminal.

Q Sign ON to the DIS system as usual.

O From the DIS Master Meni, select option 7 for the Manufacturers
Menu. Select option 6, New Holiarid Menu. Note that option 1.is
initiated from the PC, which means’that you don't-select it from the DIS
menu. .

Follow the steps that correspond to your equipment.

Emulating PC without a printer or PC with hard disk
- Press {Alt]+[Esc] to hot key to the PC.

Emulating PC with a printer
- Press [Alt]+[Esc] to hot key to the PC.
- Hotkey again.

Emulating PC acting as a console on the 5364 (S/36.only)
- Press [Alt]+[Esc] to hot key to the PC.

- From the Session Selection Menu, select option 1, DOS, and press

[Enter].

MANUFACTURER


[+] X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS

Orders

Q At the DOS prompt, type: orders [Enter]. The following message is
displayed: Pause... waiting for the DIS System
security gate.

O Wher the security gate appears, enter the division code that you use on
the DIS System. Press [Enter]. The following message is displayed:
Checking division code. The NEW HOLLAND
COMMUNICATIONS Collect Order Parameters screen appears.
4
Me™

## X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS

Collect Order Parameters Screen

MANUFACTURER

 

NEW HOLLAND COMMUNICATIONS
Collect Order Parameters

DIS Order # ROGO143A DIS Vendor
Transmit Order # Special Ship to Name/Address +
Sales Program Name Ship to Name THIS DATA WILL COME FROM THE
Special ship to #@ = __ Ship to Addr aS/490.
order Type City, St, Zip
Ship Code Attention ne
--Ship Codes- -
H=Bus Q=Pony Express
FeFill In JsSurface/ ReNebraska Land Exp
S=Stock Prem Air;Next Day © Best way S-Film Transit
AsAnnual jon-Prem;2nd Day KeOcean Freight TePriority Post
DeDirect Ship track/LTL L=Federal Express U=UPS SATURDAY
arcel Post. M=Fed Ex SATURDAY —- VeCardinal
‘VeUnit Down Drop G=Parcel Post/ NeNormal weCanadian Air =x
G+Fill In Drop Special Handling P=Purolator SATURDAY X=Direct Systems

The fields on the Collect Order Parameters screen follow on page 9.
Except for order numbers, the system uses the information that was used
most recently. Changes may be necessary--always check each field
carefully.

O Type the information for each field. To reach the next field, press
[Enter].


[«| X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS

O When all fields are complete, press [Enter] through all fields to create
the order file on the PC diskette. The following message is displayed:
Preparing to download your order from the DIS
System. The order is downloaded. An example of the message is
illustrated below:

Your Order is being downloaded from the DIS System

6 lines have been dowloaded

 

RELEASE 2.1 Senet


MANUFACTURER

 


 

The message is followed by a screen like this:

Your Order is being downloaded from the DIS System

6 lines have been downloaded

Downloaded Order # C:\DCSDATA\U143.p$x is ready to transmit

== Number of lines = 7 ==

Press Enter to continue

You can download as many orders as necessary before transmitting them
to New Holland. The file-naming scheme is d: \DCSDATA\ t####.pSr,
where d = drive, \DCSDATA = directory, t = order type, ##### = Transmit
Order #, p = parts and r = ready to send (see the example illustrated
above).

Technical note: After the PC file has been transmitted, it is renamed to
t####.p$s, where s = sent.


[=] X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS _.

O Follow the instructions for transmitting the order(s) to New Holland,
which are in the New Holland Dealer Communications System
documentation.

O Press [Alt]+[Esc] to hot key to the DIS System where you may
continue your work. Follow the instructions that correspond to your
equipment.

Emulating PC with or without a printer and PC with hard disk

- Press [Alt]+[Esc] to hot key to the DIS System.

Emulating PC acting as console for the 5364 (S/36 only)

- Press [Alt]+[Esc] to hot key to the DIS System.
- From the Session Selection Menu, select option 2, DIS System
display station, and press [Enter]. (

RELEASE 2.1 Mo


X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS [|

The fields on the Collect Order Parameters screen are described below.

Field: Description:

DIS Order # 8 characters. Required. DIS System
order number. Stock order numbers
are usually SOOnMMDD, where n =

number, MM = month, DD = day.
Example: 0020428.

Priority orders are usually
MMDDYYnd, where MM = month,
DD = day, YY = year, n = number,
and d = your division code.
Example: 0526860H.

Drop ship orders are usually the
same as the Point of Sale invoice
number.

If you are not sure of the DIS order
number, confirm it through Order
Inquiry (X34-4). This does not apply
to drop ship orders.

DIS Vendor 3 characters. Required. DIS System
vendor code.

Dealer Number 5 characters. Required. The dealer
number assigned to your dealership
by New Holland.

Transmit Order # 4 digits. Required. The number New

MANUFACTURER


[| X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS

Sales Program Name
Special Ship to #

Order Type

Ship Code

Holland will use to refer to this
order. Also used in the PC filename.

6 characters. Optional.

2 characters. Optional.

1 character. Required. Valid order
types are listed on screen. Also used

in the PC filename.

1 character. Required. Valid ship
codes are listed on screen.

The following fields are appropriate for unit down orders only:

Ship to Name 30 characters.

Ship to Addr 30 characters.

City 20 characters.

St 2 character abbreviation for state.

Zip 10 character postal code.

Attention 30 characters. Special instructions
regarding this order.
Lo


X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS In]

Returns

0 Foliow the steps presented in the section, "Signing On."

D At the DOS prompt, type: returns [Enter]. The following message is
displayed: Pause... waiting for the DIS System
security gate.

O When the security gate appears, enter the division code that you use on
the DIS System. Press [Enter]. The following message is displayed:
Checking division code. The NEW HOLLAND
COMMUNICATIONS Collect Return Parameters screen appears.

MANUFACTURER


[| X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS

Collect Return Parameters Screen

NEW HOLLAND COMMUNICATIONS
Collect Return Parameters
DIS Return# R1119920 DIS Vendor
Transmit Returné
--Return Types--

A = Annual
| = Initial

L = Leveling
? = Termination

 

The fields on the Collect Return Parameters screen are defined on page 14.
Except for return numbers, the system uses the information that was used

most recently. Changes may be necessary—always check each field
carefully.

© Type the information for each field. To reach the next field, press

[Enter].

RELEASE 2.1 Lo


MANUFACTURER


O When all fields are complete, press [Enter] through all fields to create

the order file on the PC diskette. The following message is displayed:
Preparing to download your return from the DIS
System.

O The order is downloaded and the following message displayed:

Your Return is being downloaded from the DIS System

128 lines have been downloaded

 

The message is followed by a screen like this:

Your Retum is being downloaded from the DIS System

128 lines have been downloaded

Downloaded Return # C:\DCSDATA\RI234.x$r is ready to transmit

Press Enter to continue.

 

You can download as many returns as necessary before transmitting them
to New Holland. The file-naming scheme is d: \DCS\t####.r$r,


[+] X76-1 DOWNLOAD NH PARTS ORDERS & RETURNS

where d = drive, \DCS = directory, t = return type, ###H# = Transmit
Return#, r = return and r= ready to send (see the example illustrated
above).

Technical note: After the PC file has been transmitted, it is renamed to
t##E Ss, where s = sent,

O Follow the instructions for transmitting the return to New Holland,
which are in the New Holland Dealer Communications System
documentation.

1 Press [Alt]+[Esc] to hot key to the DIS System where you may
continue your work. Follow the instructions that correspond to your

equipment.

Emulating PC with or without a printer and PC with hard disk
- Press [Ait}+[Esc] to hot key to the DIS System.

Emulating PC acting as console for the 5364 (S/36 only)
- Press [Alt}+{Esc] to hot key to the DIS System.
- From the Session Selection Menu, select option 2, $/36 display

station, and press [Enter].

RELEASE 2.1 ae


The fields on the Collect Return Parameters screen are described below.

DIS Retum #

DIS Vendor

Dealer Number

Transmit Return#

Return Type

8 characters. Required.
DIS System return number. The
return must be finalized.

If you are not sure of the DIS return
number, confirm it through Order
Inquiry (X34-4).

3 characters. Required. DIS System
vendor code.

5 characters. Required. The dealer
number assigned to your dealership
by New Holland.

4 digits. Required. The number New
Holland will use to refer to this
return. Also used in the PC filename.

1 character, Required. Valid return
types are listed on screen. Also used
in the PC filename.


Notes:

## CHAPTER X76-2

NH PART LOCATOR DOWNLOAD

### Introduction

Use this job to download parts inventory from the DIS System to a PC.
The resulting file is placed in the \DCSDATA directory from which it is
later transmitted to New Holland using the New Holland Dealer
Communications System (DCS) programs.

This chapter covers only the transfer from the DIS System to the PC.
Please refer to the DCS manual for instructions about what to do after the
download.

For the division used at the security gate, the following information is
transferred:

= Part number
= Quantity on hand (negative quantities are transferred as zero)

### How To Run

Signing On
© Turn on the PC. The PC starts as a DIS System terminal.

O Sign ON to the DIS system as usual.

O From the DIS Master Menu, select option 7 for the Manufacturers
Menu. Select option 6, New Holland Menu.

Q From the New Holland Menu, select option 2, Part Locator Download.

O At the security gate, use the division you want to transfer from.


[2] X76-2 NH PART LOCATOR DOWNLOAD we
(

O At the Select Vendor screen, type the 3-character code you use on the
DIS System.

O At the Download Utility screen, follow the steps that correspond to
your equipment:

Emulating PC without a printer or PC with hard disk
- Press [Alt]+[Esc] to hot key to the PC.

Emulating PC with a printer
- Press [Alt]+[Esc] to hot key to the PC.

- Hot key again.

Emulating PC acting as a console on the 5364 (S/36 only)
- Press [Alt]+[Esc] to hot key to the PC.

- From the Session Selection Menu, select option 1, DOS, and press
Enter].

O Atthe DOS prompt, type: loctope [Enter]. When the download is
complete, a message is displayed: Transfer is complete. You
will be at a DOS prompt.

Technical notes: The PC file created by download is
d:\DCSDATA\inventr.dat, where d= drive, \DCSDATA = the DCS
data directory. If parts from another division are downloaded, the file is
overwritten.

O Follow the instructions for transmitting the inventory data to New

Holland, which are in the New Holland Dealer Communications
System documentation.

RELEASE 2.1 LL


X76-2 NH PART LOCATOR DOWNLOAD [=]

0 Press [Alt]+[Esc] to hot key to the DIS System where you may
continue your work. Follow the instructions that correspond to your

equipment.

Emulating PC with or without a printer and PC with hard disk
- Press [Alt]+[Esc] to hot key to the DIS System.

Emulating PC acting as console for the 5364 (S/36 only)

- Press [Alt]+[Esc] to hot key to the DIS System.
- From the Session Selection Menu, select option 2, DIS System

display station, and press [Enter].

MANUFACTURER


Notes:

RELEASE 2.1 LU

## CHAPTER X79-1

RESTORE BEARING INTERCHANGE INFORMATION

### Introduction

Use this job to load Bearing Interchange information onto your hard disk.
It is stored in an independent file, BIX, which is similar to a price book.
This step is required before you can complete option 2, Bearing
Interchange Mfr Name/Vendor Code Table.

### How To Run

O From the Manufacturers Menu (X7), select option 9, Bearing
Interchange Menu.

Select option 1, Restore Bearing Interchange Information. You are
prompted to load the tape cartridge, as illustrated below:

 

 

 

 

RESTORE BEARING INTERCHANGE INFORMATION X7910-001

Insert the bearing Interchange tape into TAPO1.

Enter-Continue


[=| X79-1 RESTORE BEARING INTERCHANGE INFORMATION

O Follow the instructions on screen. When the menu returns, the job is
done.

O Use Bearing Interchange Mfr Name/Vendor Code Table (X79-2) to
assign DIS vendor codes to the manufacturers on the tape.

RELEASE 2.1 (

## CHAPTER X79-2

BEARING INTERCHANGE MFR NAME/VENDOR CODE
TABLE

### Introduction

Load Bearing Interchange Information (X79-1) enters the names of all
manufacturers into the Bearing Interchange Manufacturer Name/Vendor
Code Table. Then you can use this job to build a table that
cross-references manufacturers to your DIS vendor codes. Up to 10 DIS
vendor codes can be assigned to a single manufacturer.

This table is accessible to all divisions; however, if you have more than 1
set of dealer files, you'll need to make it available by following the steps
below. If the other set of files uses the same DIS vendor codes, do these
steps after the table is complete and you won't have to enter the DIS
vendor codes more than once.

O Delete the empty file from the second file set. For u2, substitute the 1-
character ID associated with the second set of files.

Ata DIS menu, type: DELETE u2.BMV,F1 [Enter].

O Copy the file that holds the table from the first set of files to the second.
For ul, substitute the 1-character ID associated with the first set of
files. For u2, substitute the 1-character ID associated with the second
set of files.

Ata DIS menu, type: COPYDATA u1.BMV, ,u2.BMV [Enter].


[2] X79-2 BEARING INTERCHANGE MFR NAME/VENDOR CODE TABLE

### How To Run

From the Manufacturers Menu (X7), select option 2, Bearing Interchange
Mfr Name/Vendor Code Table. A list of manufacturers' names is
displayed.

ABC-AG,AUTO,CONS & T MFR NAME/VENDOR CODE TABLE

‘THERMO KIN
‘THERMOID
‘THERMOKING
‘THESMAN
THEW SHOV
‘THICK. CHEM
‘THIOKOL
THO HDW
THOMAS
THOMAS BUS
‘THOMP .GRND
‘THOMPSON

 

PETTITTE TT abl
PEL PLE ETE TH
PIPL Ett dir
PlTid tidied
PIPETTE I Ete
PrTT Edt tht
PETELE tid
PEP TEEEL IEE
PET EPT Ett tt
PETIT G bd tba

Position to...

Gmdl-End Job Roll-Page

 

O Assign your 3-character DIS vendor codes to manufacturers. Press
[PgDn] to roll to another screen of names. These assignments can be
done at any time.

RELEASE 2.1 LO

## CHAPTER X114-2

AUTOMATIC MERGE

### Introduction

The purpose of this job is to allow you to automatically merge payments (credits)
with their corresponding invoices (debits).

If you have entered receivables credits in Create Source Documents (X1-7) or
Point Of Sale Invoicing (X5-1), you will merge them with the corresponding
debits. If you enter all your payments from the Enter Payments (X11-5), you will
use this option to merge the debits and credits.

Note: The merge applies to all customers regardless of their “Statement Type”
(“O” = Open Item, or “B” = Balance Forward). This code determines how
transactions display on the statement. Credit and debit processing is exactly the
same for these two statement types.

### Contents

ENTRANCE SCREEN...
Parameter Selection........
Select By General Ledger Account
Select By Group Codes ....
Select By Address Number .
Regular Merge..............
Merge in Balance Forward le.
Execution of Automatic Merge...

   
 
 
 
 
  

 

 
 
  

AYAAUERYNND


2 X114-2 « AUTOMATIC MERGE RELEASE 2.3

 

### Entrance Screen

O From the Receivables Apply Credits Menu (X11-4), select option 2,
Automatic Merge, press [Enter]. If the Receivables Security Gate appears,
enter your division code and security code and press [Enter]. The “Automatic
Merge” screen will appear:

NW EQUIPMENT SALES APPLY CREDITS %11401-02
Division A Automatic Merge

: i-Regular Merge
2-Merge In Balance Forward Mode

: i-General Ledger Account
2-Group Code
3-aAddress Number

 

Merge Type: Select I for Open Item statements
Select 2 for Balance Forward statements

 

 

 

Q To exit the procedure and return to the Receivables Apply Credits Menu
(X11-4) without applying credits, press [Cmd1] - End. .

Parameter Selection

This screen allows you to select the automatic merge type that you prefer.

— “Regular Merge” merges all eligible transactions for all customers by the
selected category. To be eligible for the regular merge, the first 8 characters of
the document number of the debit (invoice) have to be identical to first 8
characters of the credit description (payment). You can omit the #* at the end
of the document number that was generated in Point of Sale.

— “Merge Jn Balance Forward Mode” merges oldest debits with oldest credits
for all customers in the selected category.

You can select customers by general ledger account, group code, or by address

number for all automatic merge types.

O Select options in the “Merge Type” and “Select by” fields and press [Enter] to
continue.

O  Toexit the procedure without applying credits, press [Cmd1] - End.


ACCOUNTING X114-2 « AUTOMATIC MERGE 3
eS ee eee

Select By General Ledger Account

If you have entered “1” the “Select by” field in the “Automatic Merge” screen, the
“Selection by G/L Accounts” screen appears:

NW EQUIPMENT SALES APPLY CREDITS X11401-03
Division A Selection by G/L Accounts

Enter : ALL = All Receivables Accounts
or

Specific General Ledger Accounts

Qm@l-End md3-Previous Screen

 

O1 Type ALL to select all customers, or enter up to ten different general ledger
account numbers. If you enter specific general ledger accounts, the selected
accounts must be included in the division displayed in the upper left corner of
the screen. Accounts must also be valid and active in the general ledger chart
of accounts and they have to have an edit code of “A” (accounts receivable).

 

O To continue, press [Enter].

O To return to the parameter “Selection” screen, press [Cmd3] - Previous
Screen.

O To exit the procedure and return to the Receivables Apply Credits Menu
(X11-4), press [Cmd1] - End.


X114-2 e AUTOMATIC MERGE RELEASE 2.3

 

Select By Group Codes

If you have entered “2” the “Select by” field in the “Automatic Merge” screen, the
“Selection by Group Codes” screen appears:

 

NW EQUIPMENT SALES APPLY CREDITS X11401-04
Division A Selection by Group Codes

Enter Group Codes

Cméi-End cmdé3-Previous Screen

© Enter up to ten different group codes. Group codes are configured under the
option Group Code Maintenance (X11-3).

O To continue, press [Enter].

O To return to the Automatic Merge parameter “Selection” screen, press [Cmd3]
- Previous Screen.

O To exit the procedure without applying credits and return to the Receivables
Apply Credits Menu (X11-4), press [Cmd1] - End.


ACCOUNTING X114-2 e AUTOMATIC MERGE 5

 

Select By Address Number

If you have entered “3” the “Select by” field in the “Automatic Merge” screen, the
“Selection by Address Numbers” screen appears:

 

NW EQUIPMENT SALES APPLY CREDITS X11401-05,
Division A Selection by Address Numbers

Enter Address Numbers ..

 

Cmdl-End Cmd3-Previous Screen

 

 

1 Enter up to ten different address numbers. Address numbers must be valid
customer address numbers set up in Receivables Maintenance (X11-2), and
must be included in the division displayed in the upper left corner of the
screen.

 

O To continue, press [Enter].

O To return to the Automatic Merge parameter “Selection” screen, press [Cmd3]
- Previous Screen.

O To exit the procedure without applying credits and return to the Receivables
Apply Credits Menu (X11-4), press [Cmd1] - End.


6 X114-2 e AUTOMATIC MERGE -RELEASE 2.3

 

Regular Merge

In the “Automatic Merge” screen, if you select “1” in the “Merge Type” field,
complete the “Select by” field and press [Enter], the merge will begin and the
following messages will display on your screen:

Step 1 of 4 ~ Creating Files To Be Merged

Step 2 of 4 - Receivables Transactions Merging Is Running
Step 3 of 4 - Receivables Aging Calculation Is Running
Step 4 of 4 - Average Payments Age Update Is Running

Merge in Balance Forward Mode

In the “Automatic Merge” screen, if you select “2” in the “Merge Type” field,
complete the “Select by” field and press [Enter], a confirmation screen will
appear:

NW EQUIPMENT SALES APPLY CREDITS *31401-06
Division A Automatic Merge

Merge In Balance Forward Mode
Confirm : N (¥/N)

cmé3-Return Enter-Confirm

 

 

O To continue with the merge, type ¥ and press [Enter].

### Warning!

If you continue, the system will merge all credits of the selected receivable

according to the balance forward mode. Oldest debits will be merged with oldest
credits. If you merge accidentally, the only way to correct your receivables
transactions is to delete your files and to restore from your backup.


ACCOUNTING X114-2 e AUTOMATIC MERGE 7

 

Execution of Automatic Merge

‘When you press [Enter] to confirm the automatic merge, the merge will begin and
the following messages will display on your screen:

Step 1 of 4 - Creating Files To Be Merged

Step 2 of 4 - Receivables Transactions Merging Is Running
Step 3 of 4 - Receivables Aging Calculation Is Running
Step 4 of 4 - Average Payments Age Update Is Running

The Automatic Merge procedure is completed. The Receivables Apply Credits
Menu appears.


8 X114-2 ¢ AUTOMATIC MERGE RELEASE 2.3

Notes:

## CHAPTER X147-1

GENERAL SCHEDULE

### Introduction

A General Schedule can be printed for up to 7 General Ledger accounts.
You can specify the sort order you prefer, and a date range for the report.
Only transactions for open months are available, however, General
Ledger Maintenance (X14-2) allows you to specify a number of "Months
to Keep" if you need to print general schedules pertaining to closed G/L
months.

## X147-1 GENERAL SCHEDULE

   

### How To Run

General Ledger Account Maintenance Screen

If you want to keep transactions for closed months, enter the number of
"Months to Keep" in General Ledger Account Maintenance. Be aware that
keeping a lot of transactions around for a long time will consume a lot of
disk space, the same as keeping a lot of months open.

GENERAL LEDGER ACCOUNT MAINTENANCE x1421~101 1

Account #: 2400
vitle PAYABLES (
Edit Code P

Debit Code M

Account #1

Account #2

Factor

Type

cash acct? (¥)

General Schedule:
Months to keep 06 <

 


RELEASE 2.1 LL


General Schedule Selection Screen

A & R SALES & LEASING
Division: A

G/L Accounts:

G/L from mon. :

from year:

to mon.
to year:

cmdi-End job

x14701-02

2-By unit #

2-By Document #

3-By Address #

4-By ‘Transaction Date

01-12, Blank = All Months
For 1 month, fill in
From-month only, leave
the rest blank


   

A & R SUES & LEASING GENERAL SCHEDULE ace 4/24/92 Page 1.
Division: A From: 0100 Te: 1299 Sort By Unit # Time 9.28.19 1470-30,

Pate <é Decument# Addr # onic Account © amount ALD A1200.«A270«—a8 900

050186 © cKR7800 © KLUCUI atiog 300.00-
50186 © CKNS21 «= SEREO? alto 3500.90-
250186 CASH ADAMOL 1100 500.00-
4900.00-

052091 F RCOO203 Fr a1z00 109.52
109.52
osoige P C6277 atz00©-«-25235.28
050186 + Eso0203, aizoc—15235.28-
050286 F c6z9362 atzoo = 27532.32,
050286 W 0952 1200 89.63,
050186 W 32258 1200 $5.00

aneee.94
asoi8s p ssetsi2 nitov ovre7s atz70——_s0co,0 (
seae.o0

os01e6 P =S00632 T32EAR AL270 4000.05

2000.00,
Grand Totals : ¢900,00- 27796.45 9000.00

 

RELEASE 2.1 Lo

## CHAPTER X147-2

UNIT SCHEDULE

### Introduction

The Unit Schedule summarizes transactions for sold units from General
Ledger accounts related specifically to units: Units Inventory, Units Cost
of Sale, and Flooring accounts ("W" and "F" edit codes). The schedule
may include up to 7 different accounts for a particular month/year.

Transactions involving inventory and cost of sale accounts are accessible
even for closed months. Flooring transactions are not available for closed
months if they have been merged through Correct Due Dates and
Discounts (X12-7) or Print Payables Checks (X12-9) unless payables
history is retained through the "Months of Payables History” field in
Security Maintenance (X6-6).

## X147-2 UNIT SCHEDULE

 

### How To Run

From the General Ledger Menu (X 1-4), select option 6, Unit Schedule.
Following the Accounting security gate, the selection screen appears as
illustrated below:

A&R SALES & LEASING UNIT SCHEDULE x14601-01
Division: A

G/L Accounts:

Sales Period:

Cndl-End job

O Make your selections.
O Press [Enter] to place the report on the job queue.


 

An example of a Unit Schedule Report follows:

A & R EQUIPMENT SALES UNIT SCHEDULE wate 4/21/92 Page

Division: 1 asa ‘Time 14.5934 1.4603-01
unite Td Date Docunent adart 1320

Prseaa ansiss1 woo7213

Frseea 1/31/91 007213

rsea3 2/01/91 woO7213 #

KEs879 1/21/91 36808 2097.27-
Kese79 231/91 Lucy. 1964.93,
Kese73 2/31/91 ORK HARBOR 237.48
xese79 1731/91 Lucky 108.43-
xesa79 2708791 007202 143.25

‘rotel
1731/9) 38808
2/12/92 MITCHELL .

 

op2000 33485 157.94 -
onz000 430785 105.27

092000 5yanses 78.60
ooz000 e 416/86 300.00-
opz000 24/91 1669.90-

2632.09- :
anzes 3288 453.82

anaes 1560 59.00 .
4/737e5 9201 4782.25
aroses 15234 30.52
4388 VARS 2.25
22/91/89 WRITEDOWms 2827.84-
3431/90 WOOSEIE + 200.23 :
azrasea 1 2600.23-

1/25/91 38397

on9149,
ona249
ouaies
on3149
on2149
on3149,
oxs1e9,
on3149
ona149

rogyw sawn

oRSsS6 PF 2/20/90
onsssé Pp 2/27/50
orsssé = 3/24/91

 


Notes:

RELEASE 2.1 Lo

## CHAPTER X147-3

SCHEDULED ACCOUNT REPORTING

### Introduction

Scheduled account reporting lists all of the transactions posted to accounts
marked with an N, U, T, V, or L edit code. Depending on the account's
edit code, transactions may be indexed by Address#, Unit#, Description,
VIN# or DOC#. Transactions that occurred prior to the edit code being
added to the account will not appear on this report.

### Preparation

Prior to running the report, you must assign one of the following edit
codes to the G/L account you wish to schedule.

N Schedule by Address#
U Schedule by Unit#

T Schedule by Description
Vv Schedule by VIN#

L Schedule by DOC#

Once you assign one of these edit codes to a G/L account, transactions
posted to that account will be recorded by the system. Refer to the
Schedule Menu Overview (X14-7) for more information on this process.

### How To Run

From the Schedule Menu (X14-7), select option 3, Scheduled Account
Reporting. The following screen will appear

## X147-3 SCHEDULED ACCOUNT REPORTING

ABC-AG,AOTO,CONS & TRUCK CO. PRINT SCHEDULED ACCOUNT x14731-02 1
Division A REPORT

G/L Account #......
Detail or Aged... ve. D (D/A)

Purge $0.00 Balances N o(x/N)

O Type the account you want to see included in the report in the "G/L
Account#" field.
C1 Select a detail or aged report.

A detailed report lists all the transactions posted to the account along
with an address#, unit#, description, VIN#, or DOC# for each. This
report is sorted according to the contents of the selected account's edit
code. For example, an account with edit code N (schedule by
Address#) will sort by Address#.

An aged report summarizes all the transactions to the account according
to Address#, Unit# Description, VIN#, or DOC#. These transactions
CC


 

are spread out over three ranges of days that the user specifies. By
default, the aged report is spread over periods of 30 days, 60 days, and
90 days. Negative balances are listed in the most recent aging category.

© Decide if you want to purge $0.00 balances. Jf "Y,” all groups of

transactions associated with a particular Address#, Unit#, Description,
VIN#, or DOC# (depending on the edit code you used) that have a
balance of zero will be deleted from the schedule and not be included in
the report. As this job purges debit and credit transactions that are
equal to one another, it is good for merging payments with invoices.
Purged transactions are only deleted from the files involved with
scheduling; they are not deleted from any other files.

A sample report follows.

ADERESS 4 SCHEDULE Pate 11/11/94 Pege
ACCOUNT # A15¢0 ‘Tie 19.45.07 14734-01
Gocument ‘Transaction
Description Number

aasasssa . raveao122
33/22/84 wzwv5i262

Total
aisiassa asc. EQUIP #2006

Total
qaass¢ rves2ad2

‘Total
aasaas9g rwvs2000

‘otal

Grand Total


Notes:

RELEASE 2.1 LU

## CHAPTER X147-4

AUTOMATED SCHEDULED ACCOUNT PURGE

### Introduction

Scheduled Account Purge allows you to set up a table that will purge
selected scheduled accounts. Any account can be bypassed before the
purge is submitted.

### How To Run

From the Schedule Menu (X14-7), select option 4, Automated Scheduled
Account Purge. Pass through the security gate. The following screen
appears.

‘iti EQUIPMENT SALES AUTOMATED SCHEDULED ACCOUNT PURGE X14740-01
Division Setup Screen

Account Pes/Neg. Writeoff |
B Number variance accounté |

Account Pos. /Neg. WriteOff |
Number Variance Accounté |

 

 

 

 

 

 

 

 

 

 

|
l
I
|
I
t
i

i
|
I
!
|
!

I
i
1
|
]
|
!

| i
| I
|
) |
i j
I 1
1
l |
i |
i I
| '
| '

 

Bottom
HELP Cm@i~Bné Job CmdS-Refresh Cmd7-Submit Purge  Cmd8-Accounts
Amounts are to be entered in cents, without decimal. {c) DIS, 1996.

 

O For each entry in the table supply the Account Number, the Plus/Minus
maximum for write-offs, and the unscheduled G/L account# to which to
post the write-off amount.

Note: Enter the amount in cents, without a decimal.

## X147-4 AUTOMATED SCHEDULED ACCOUNT PURGE

0 To select the account# or the write-off account# from a list, position the

cursor in one of these two fields and press [Cmd8]. If the cursor was in
the Account# field, a list of scheduled account numbers will appear. If
the cursor was in the write-off account# field, a list of unscheduled

account numbers will appear.

Note: To display a list of account numbers, the field the cursor is in
(cither account# or write-off account#) must be empty or contain the
number of a valid account.

The following screen appears.

‘Sw EQUIPMENT SALES

NW EQUIPMENT SALES
Division: A

Subset: Scheduled
IsSelect

AUTOMATED SCHEDULED ACCOUNT PURGE

Select G/L Account

Position to Account:

Opt Account Ed Description
1200 NEW TRACTORS
A1240 ‘NEW EQUTPMENT
1250 USED TRACTORS & EQUIPMENT 3250
A1260 NEW AUTOS
A1265, NEW TRACTORS

1270 USED

F9=sPage-Up

Gméi-End Job

AUTOS

F10=Page-Down

cnd5-Refresh

Acct. #1
23200
a3240
3260

3270

F12=Cancel Loo!

cmé7-Submit Purge

Acct.
A4200
A420
A4250
a4260

A4270

kup

x14740-01
x01901

£
#

#20 Type


i
l
i
i
|
1
i

ce

Bottom

Cmd§-Accounts

 
CO

### 147-4 Automated Scheduled Account Purge [2]

O Use the Page Up and Page Down keys and the Position To Account
field to display different accounts. Select an account by placing a "1" in
the opt field and pressing [Enter]. The account you selected will appear
in the setup screen.

O Once you have selected a list of scheduied accounts to be purged, the
screen will look like the following:

set! EQUIPMENT SALES AUTOMATED SCHEDULED ACCOUNT PURGE *14740-01
Division A Setup Screen


I
|
i
I
I
i
!
1


 

Account Pos/Neg. writeogé |
Number Variance Accounté |
Al200 100.00 A1320 |
A1240 100.00 A1320
Al260 100.00 A1320
1273 50.00 A1320

Account Pos. /Neg. Writeoff |
B Number = variance Account# |

l
I
1
[
!

i

|
!
|
1
1

I
[


!

!
!

|
Bottom
Cmdi-End Job CmdS-Refresh Cmd7-Submit Purge  cma8-Accounts


[+] X147-4 AUTOMATED SCHEDULED ACCOUNT PURGE

1 To bypass the purging of an account, place a "B" in the B field. This
will bypass that account for this pass only. The next time this job is
started, this account will appear on the table but will not be flagged
with a "B."

O To purge the accounts you have selected, press [Cmd7]. The purge job
will be submitted to the job queue. You will receive a message when
the purge is completed.

O Press [Cmd1] to return to the Schedule Menu (X14-7). The accounts in
this table will reappear when this job is started in future sessions.

RELEASE 2.1 Lo

## CHAPTER X147-5

SCHEDULED ACCOUNT INQUIRY

### Introduction

Scheduled Account Inquiry allows you to view individual transactions
posted to a scheduled account.

### How To Run

From the Schedule Menu (X14-7), select option 5, Scheduled Account
Inquiry. The following screen will appear.

ABC-AG,AUTO,CONS & TRUCK CO. SCHEDULED ACCOUNT INQUIRY x14751-01 1

Division: a Transaction Display

G/L Posting

ID Mth Date Description Document # addr #

Cmdi-End job Omd2-Print Cmd3~Purged only Roll-Page Page

 

2 Enter the Account# for the postings you want to display.

Enter the Schedule for the posting you want to display. Ef the account
is scheduled by unit number, for example, you would have to enter a
unit number in this field.

O Press [Enter]. Transactions will appear on screen.

## X147-5 SCHEDULED ACCOUNT PURGE

 

Commands Available

[Cmd1] End job.
[Cmd2] Print transactions displayed on screen.
[Cmd3] Toggle between current transactions and purged

transactions. Note: purged transactions cannot be printed.

RELEASE 2.1 Co

## CHAPTER X159-1

FORMATTED FINANCIAL STATEMENT

### Introduction

Certain vendors require that financial information be submitted to them in
specific forms. Formatted Financial Statement allows you to runa
financial statement in the format Tequired by the vendor.

### Preparation

O Make sure the Formatted Financial Statement diskette has been applied.
See Chapter X159-3 APPLY FINANCIAL STATEMENT FORMAT.

O Assign all general ledger accounts to standard account numbers
matching the account numbers on the form required by the vendor. See
Chapter X159-2 ACCOUNT ASSIGNMENT MAINTENANCE.

If either of the above steps is omitted, you will not be able to runa
Formatted Financial Statement. Screens will display informing you of the
problem and how to correct it.


[=] X159-1 FORMATTED FINANCIAL STATEMENT

### How To Run

Jf more than one Financial Format diskette has been applied in Apply
Financial Statement Format (X159-3), the following screen will display:

ABC COMPANY Formatted Financial Statement x159a-401,
Division: D Format Selection

Date
Format Title Effective Applied

Manufacturer's Financial Format 12/17/96 1/05/97
XvZ'S Financial Format - Another Format 1/17/97 2/05/97

To select, type any character beside the desired format.

eméi-cancel job

 

Place any character next to the financial format you want to work with. Do
not press Enter. The Financial Statement Month Selection screen will be
displayed automatically.

If only one Financial Format Diskette has been applied, the Financial

Statement Month Selection screen will display after passing the security
gate:

RELEASE 2.1 LL

## X159-1 FORMATTED FINANCIAL STATEMENT

AGR EQUIPMENT SALES Formatted Financial Statement x1591-101
Division: A Month Selection
DCS Financial Statement

Enter the month for which a Financial statement is desired (1-13) :
Is this statement for an cpen or closed month? Enter '0' or ‘C! :
Is this statement for a fiscal or calendar year? Enter 'F' or 'C' :
Round all numbers on financial statement? Enter '¥' or 'N' :
Is statement used for down Loading? Enter ‘¥‘ or ‘Nt ;

Examples: Open/Closed
1. Statement for most recently closeé month c
2. Statement for current month °
3. Statement for oldest open month °
4. Statement for the "thirteenth"* month c

- The "thirteenth" month statement is your fiscal year end month plus
adjusting entries.

cmdi-Cancel job cmd3-Select. by division

 

Enter the month for which a Financial Statement is desired (1-13):

The default will be the most recently closed month. Choose the month
desired. 1 = January, 2 = February and so on.

The 13th month is used for year end adjustments. See Accounting End of

Year Adjustments (X1.11-2). You can only choose the thirteenth month if
you are running a financial statement for the fiscal year.


[ «| X159-1 FORMATTED FINANCIAL STATEMENT

Is this statement for an open or closed month?

The default will be C for closed. Enter a C if the month desired is closed
and O if it is open.

Is this statement for a fiscal or calendar year?

Fiscal year:
If running a financial statement for the fiscal year, type F.

Calendar year:
To mn a calendar year statement, type C.

How Calendar Year works:

You may only run a calendar year financial statement for a month of the
previous calendar year while January of the current year is open.

For example, we will say it is January 1997. All the months in the
previous year are closed. You want a calendar financial statement for June,
1996. You would request the following:

Enter the month for which a Financial Statement is desired (1-13) :

Is this statement for an cpen or closed month? Enter "0" or
Is this statement for a fiscal or calendar year? Enter ‘Fi or 'C* :

  

Once January of 1997 is closed, you cannot run a calendar year financial
statement for any month in 1996, the previous calendar year. If you select:

RELEASE 2.1 Lo


X159-1 FORMATTED FINANCIAL STATEMENT [=]

Enter the month for which a Financial Statement is desired (1-13) :

Is this statement for an open or closed month? Enter "O" or
Is this statement for a fiscal or calendar year? Enter ‘F' or ‘C

 

You will receive the calendar financial statement for January 1997.
Selecting any other closed month will result in a message:

A Calendar statement cannot be run for this month. See documentation.

There is no other closed month in the current year. Choosing a closed
month other than January would be an attempt to mn a statement for the
previous year. You cannot run a calendar financial statement for the
previous year once January of the current year is closed.

If the fiscal year begins in January, the financial statement would contain
the same figures whether fiscal or calendar is selected. Select F for fiscal.
If C for Calendar is selected, the following message will display:

Fiscal and Calendar statements for this division are the same, so select
Fiscal.

Round all numbers on financial statement?
Answer Y (Yes) if you want the figures rounded and balanced; otherwise,

there may be some discrepancies and the financial statement may be out of
balance by a small amount.


[«| X159-1 FORMATTED FINANCIAL STATEMENT

Note:

 

The Command keys are at the bottom of the screen.

Cmd1 to cancel job: If you do not want to run a Formatted Financial
Statement, press Cmd1 to cancel the job.

Cmd3 select by division: If you have more than one division, you can
combine the divisions for a financial statement containing all
divisions.

Tf you have more than one division, you can select any of or all of the
divisions and combine them on one financial statement. (

The Formatted Financial Statement will not run unless all general ledger
numbers in all selected divisions have been assigned standard account
numbers. Standard account numbers match the account numbers on the
financial format required by the vendor. See Chapter X159-2 Account
Assignment Maintenance.

Rules for Selecting Combined Divisional Statements

O When selecting a financial statement, all divisions must be operating in
the same general ledger month. In Security Maintenance X6-6, there is
a field called General Ledger month. The month changes each time a
month is closed. All divisions must display the same month in this
field.

O You can only request a combined calendar statement if the fiscal year
for all divisions selected starts in the same month.

RELEASE 2.1 LL


X159-1 FORMATTED FINANCIAL STATEMENT | 7 |

Press Cmd3 to select divisions to be included in the statement. The
following screen displays:

ABC COMPANY Formatted Financial statement. 1591-103
Division: D Division Selection

To include other divisions in a composite Financial statement, place any
character beside the divisions and press Enter.

### X B Ever Available Rental L

Enter-Verify selections Cmd6-Return to Month Selection screen

 

Place any character next to the divisions to be included on the Financial
Statement.

When the selection is made, Cmd6 back to the Month Selection screen.


[8 | X159-1 FORMATTED FINANCIAL STATEMENT c

On the Financial Statement Month Selection screen, press Enter. The final
verification screen will display:

ABC COMPANY Formatted Financial Statement x1591-104
Division: D Final Verification
Manufacturer's Financial Format

If you have completed making your selections, press Enter to continue.
However, if you want te change your month or division selection, press omd6.

You have selected:
August,

Closed

With divisions B
For a fiscal year

(mdi-Cancel job Qrd6-Return to Month Selection Enter-Continue

 

Verify the choices made. If they are correct, press Enter. The Financial
Statement will be placed on the job queue.

Tn the above example, the choice is for a Financial Statement for the
closed 8th fiscal month, to include divisions D and B.

If the choices displayed are not the ones you want, press Cmd6 to return to

the Financial Statement Month Selection screen. You can begin the
selection process again.

RELEASE 2.1 CO


When final verification is made, press Enter to continue. The following
screen will display:

Formatted Financial Statement x1591-104
Final Verification
Manufacturer's Financial Format

Account Assignments are now being checked

 

 

If ail the general ledger accounts have not been assigned standard account .
numbers as appear on the form supplied by the vendors, the following
screen will display: :

Formatted Financial Statement X1591-104
Final Verification
Nanufacturer’s Financial Format

One or moxe General Ledyer Accounts are not assigned.

 

See the Report of Unassigned Accounts for details.

To assign G/L Accounts to Standard Format Accounts,
use Option 2 te do Account Assignment Maintenance.

Enter-Return to menu

 


[| X159-1 FORMATTED FINANCIAL STATEMENT

The following screen will display:

Formatted Financial Statement x1591-204
Final Verification
Manufacturer's Financial Format

Dealer Value records are now being prepared.

 

Press Enter to return to the menu. The Unassigned Accounts Report will
print. Select option 2, Account Assignment Maintenance. Assign standard
account numbers te the general ledger accounts that appear on the report.
See Chapter ¥159-2 Account Assignment Maintenance.

If all general ledger account numbers have been assigned to standard (

account numbers, you will proceed to the Formatted Financial Statement
Update Dealer Values screen.

RELEASE 2.1 LC


ABC COMPANY Formatted Financial Statement X1590-201
Division: D Update Dealer values
Manufacturer's Financial Format Screen 01

Enter City & State: WHYKOT, co Length: 25
Eater Dealer Number: 123456 Length: 25
Enter Dealer Code: Da2631 Length: 08
Enter Bank Authorization: 1000000 Dec pl: 2

New Statement (Adjust values) Next screen to show: 02

Gmdl-Cancel job Omd4-Continue with statement Enter-More dealer values

Each vendor requires different information be provided on the financial
statement. Some require dealer numbers, address, name and location of the
dealership and so on. Since each vendor's requirements are different, the
Formatted Financial Statement Update Dealer Values screen will be
different.

The above screen is an example of the values that must be provided by
ABC Company to satisfy the requirements of the vendor Manufacturer. On
the left of the screen, the information required displays.

If the field is alpha-numeric such as dealer address, the information is
filled in at the center of the screen. The length of the field will display on
the right of the screen. The length indicates the maximum of characters


[=| X159-1 FORMATTED FINANCIAL STATEMENT

that can be typed in the field.

If the field is numeric, the amount is typed in on the right of the screen.
Type the number and press the Field Exit key. The decimal places in the
number display to the right of the field. In the example, the Bank
authorization for ABC Company is $10,000.00.

Once the screen has been filled in, the information will be on the screen
the next time the job is run.

There are a maximum of 16 fields to a screen. If more than 16 fields are
required, or all the information has been entered, press Enter to advance to
the next screen. Some formats require several screens.

Tf you know the number of a desired Dealer Value screen, you may change {
the Screen number in the Next Screen to show: field to advance or go
back to that screen.

When ail the information is typed in the fields, press Cmd4 to continue
with the statement.

The statement is placed on the job queue.

LO


X159-1 FORMATTED FINANCIAL STATEMENT |

Special Forms for the Financial Statement

System messages tell you when to load special forms, such as statements,
and when to reload regular standard paper; however, it must depend on
your answers to the messages to "know" what kind of forms are currently
in the printer. In addition, when your answer indicates that forms have
been changed, the system provides a message to facilitate alignment. In its
own clunky mechanical way, it is trying to make your job easier.

For additional help with alignment, please refer to the forms alignment
documentation in the APPENDIX that pertains to your printer.

When statements are ready to be printed the Load Forms message will be
generated to prompt you to load the statements. Do not load the statements
until prompted to do so. An error report prints before statements. If
statements are loaded, the report will print on the statements.

Before you answer the message, place the first form for the financial
statement in the printer. When the forms are properly aligned, answer the
Load Forms message with a G. The first line is printed and the Alignment
message is generated,

If a minor adjustment is needed use the roll wheel to move up or down.

If you want to reprint the 1* line on the same statement to verify the
alignment before Jetting all your statements print, answer this message
with an R. The first line of the statement will be printed again on the same
check. At the bottom of the screen, you'll see: "Reply sent to message."
The Alignment message will be generated again.

When you are satisfied with the alignment, answer the message with an
I, which will print the 2™ line on the same statement and continue printing


[+] X159-1 FORMATTED FINANCIAL STATEMENT

without further messages.

If the alignment needs more than a minor adjustment, press the On Line
button to stop the printer. See the section titled TROUBLESHOOTING in
the appendix chapter for your printer.

After statements have been printed and the first printout is requested, the

Load Forms message will be generated again to prompt you to change
forms back to standard paper.

No Special Forms for the Financial Statement

Answer the load STD forms message with a G. Then answer the message
with an I. The financial statement will print.

Tf you are not happy with the way the financial statement looks on the
paper, adjust the paper and run the job again.

Statement Requires More Than One Page

If the Formatted Financial Statement requires more than one page, it is
necessary to align each page. The same messages will display. Repeat the
process for each page.

RELEASE 2.1 LO

## CHAPTER X159-2

ACCOUNT ASSIGNMENT MAINTENANCE

### Introduction

In this job, you will assign your general ledger account numbers to
standard account numbers matching the account numbers provided by the
vendor on the required form. Account assignments must be made before a
Formatted Financial Statement (X159-1) can be run.

Previously, the balances from your general ledger have been manually
written in the standard account number spaces provided on the required
financial form.

Once your general ledger numbers are assigned to the vendor's standard
account numbers, the computer will automatically place the balances of
your general ledger accounts into the standard account numbers required
by the vendor when a formatted financial statement is run.

Before a formatted financial statement can be run, all general ledger
account numbers must be assigned to a standard account number provided
by the vendor. Before Account Assignment Maintenance can be
performed, the Financial Format diskette must be applied. See Chapter
X159-3 APPLY FINANCIAL STATEMENT FORMAT.

Account Assignment is divisional and wili have to be performed for each
division that will be included on a formatted financial statement.

### How To Run

To complete this job, you will need a copy of the required financial form
provided by the vendor. You will be asked to supply a standard account
number listed on the form for each general ledger account number on the
system.

## X159-2 ACCOUNT ASSIGNMENT MAINTENANCE

 

If more than one Financial Format diskette has been applied in Apply
Financial Statement Format (X159-3), the following screen will display:

ABC COMPANY Account Assignment Maintenance X159A-401
Division: D Format Selection
Date
Format Title Effective applied

Mamufactuxer's Financial Format 12/17/86 1/05/87
XYZ'S Financial Format - Another Format, 117487 2/05/87

To select, type any charactex beside the desired format.

Cmd-Cancel job

 

Place any character next to the financial format you want to work with. Do
not press Enter. The Account Assignment Maintenance Assign G/L
Accounts screen will display automatically.

If only one format was loaded on the computer, the Account Assignment

Maintenance Assign G/L Accounts screen will display automatically after
the security gate is passed.

RELEASE 2.1 LO


 

ABC COMPANY Account Assignment Maintenance x1592-201
Division: D Assign G/L Accounts

Manufacturer's Financial Format
G/L assign to
Recount = Title Standard Acct
p1010 CASH ON HAND
1020 CASH IN BANK
pLii10 ACCOUNTS RECEIVABLE
pi11s WHOLEGOODS RECEIVABLE
pi1i7 BALANCE-CONTRACTS
1118 WARRANTY RECEIVABLE
p1129 DOUBTFUL ACCOUNTS
1200 NEW INVENTORY
pi2io NEW LAWN & GARDEN
1220 USED INVENTORY
1230 PARTS INVENTORY
1250 PREPAID TAX & LICENSE
Di260 PREPAID OTHER


1110 Acct. Rec.-parts & Service

1200 New Ford Tractors & Equipment 2

1220 Used Equipment Inventory
1230 Parts Inventory

1250 Prepaid Taxes & License
1260 Prepaid Other


Begin next page with Account ¥: 51260

cmi1-End job

General ledger account numbers are set up in General Ledger

Maintenance(X14-2). When they are set up, account number, account title, E
debit code, edit code, account 1, account 2, factor and account type are

selected.

On the left of the above screen are the general ledger account numbers,
account titles, and account types as set up in General Ledger Maintenance.


 

Standard Account numbers are the numbers assigned by the vendor on the
standard financial format form. All of the general ledger accounts
displayed on the left must be assigned to a standard account number from
the financial form supplied by the vendor. All the general ledger account
numbers assigned to a standard account will be used to provide the balance
of the standard account when the formatted financial statement is
requested.

If a standard account number from the form provided by the vendor
matches a general ledger number set up in General Ledger Account
Maintenance, the standard account number and its description will be
supplied automatically on the screen. Using the financial form, type the
standard account number to be assigned from the form under the columa
“Assign to Standard Acct".

If a standard account displays and you want to change it, type over the
standard account number with a different number. You must choose a
standard account that is on the form. Only the accounts on the form are
valid.

It is possible that some standard account numbers may not be exactly the
same as those printed on the Manufacturer's form. For example, for some
manufacturers the standard account numbers have extra zeros. If you are
having difficulty assigning Standard Account numbers, press Cmd1.
Request the Standard Accounts and Assignments report. This report will
list every valid standard account number and title. Refer to the report when
assigning standard account numbers.

RELEASE 2.1 tO


 

Below is a sample Account Assignment Maintenance Assign G/L
Accounts screen when all standard accounts are filled in:

ABC COMPANY Account Assignment Maintenance x1592-101
Division: D assign G/L Accounts
Manufacturer's Financial Format
s/L Assign to
Account ‘Title Standard Acct


p1o10 CASH ON HAND

1020 CASH IN BANK

D1110 ACCOUNTS RECEIVABLE
piiis WHOLEGOODS RECEIVABLE
plii7 BALANCE-CONTRACTS
pli WARRANTY RECEIVABLE
pig DOUBTFUL ACCOUNTS
Di200 NEW INVENTORY

pi2io NEW LAWN & GARDEN
1220 USED INVENTORY

1230 PARTS INVENTORY
pi2zs0 PREPAID TAX & LICENSE
p1260 PREPAID OTHER

1000-2 Cash On Hand & In Bank

1000-2 Cash On Hand & In Bank

1000-2 Cash On Hand & In Bank

1110 Accts Rec.-Parts & Service
1310 Accts Rec.-Parts & Service
1110 Accts Rec.-Parts & Service
1115 Accts. Rec. -Warranty

1110 Accts Rec.-Parts & Service
1200 New Ford Tractors & Equipment
1200 New Ford Tractors & Equipment
1220 Used Equipment Inventory
1230 Parts Inventory

1250 Prepaid Taxes & License
1260 Prepaid Other

A
A
B
A
A
A
A
A
A
A
A
A
A

Begin next page with Account #: D1260
cmd1-End job

On the above screen, there is more than one cash general ledger account
number. The standard account number on the form provided by
Manufacturer for all cash accounts is 1000- 2. If the standard account
number to be placed on one line is the same as the previous line, you can
use the Dup key to duplicate the standard account number. This will save
typing strokes.

When the screen is filled in, press Enter. At the bottom of the screen, the
account number that will be on the top of the next page is listed in the field


 

“Begin next page with Account #". If there are no errors on the screen, the
next screen will display. Repeat the process until ali general Jedger
accounts are assigned to a standard account.

Tf you are unsure of the standard account number to be used, or can not
determine from looking at the form the correct standard account numbers,
you can skip the account and return to it later. However, all general ledger
accounts must be assigned to a standard account before a formatted
financial statement will be run.

To determine the valid standard account numbers, press Cmd]1 to end the
job. The following screen displays:

ABC COMPANY Account Assignment Maintenance x1592-104
Division: D Select Reports (
Manufacturer's Financial Format

Enter 'Y' for a report of
Standard Accounts and Assignnents N

Enter 'Y' for a report of
Unassigned Accounts N

Cmdl-End job  Cmd3-Go back

 

RELEASE 2.1 LO


 

To obtain a printed report of the Standard Accounts and Assignments,
place a Y (Yes) in the field next to the Standard Accounts and
Assignments report. Press Enter. The report will print on the system
printer. Select option 2 and finish the account assignments. All valid
standard account numbers will be listed on the report. You cannot use any
standard account number that does not appear on the report.

Possible Errors

There are two possible errors that can occur:

O Ifa general ledger account number is assigned to a standard account
that does not exist on the vendor's form, a message will display next to F
the standard account number: .

® not a Standard Acct

 

Type over the standard account number with the correct number. Press
Enter. If there are no other errors on the screen, the next screen will
display.

 

O The standard account numbers assigned must match the account type of
the general ledger account number. An expense general ledger account
number must be assigned to an expense standard account number. If,
for example, an asset general ledger account number is assigned to a
liability standard account number, the following message will display
next to the standard account number:

™ types do not match

To correct the error, type a standard account number that matches the
account type over the standard account number that displays. Press


 

Enter. If no other errors exist on the screen, you will advance to the
next screen.

### Enter Must Be Pressed On Each Screen

The standard account numbers typed on the screen are not registered until
Enter is pressed. When all general ledger account numbers have been

assigned to standard account numbers, press Cmd1 to end the job.

The following screen displays:

ABC COMPANY Account Assignment Maintenance X1592-104
Division: D Select Reports

Manufacturer's Financial Format

saver "V" foe a vesect of {
Standard Accounts and Assignments

@nter "Y' for a report of
Unassigned Accounts

(mdl-Ead job crd3-Go back

 

If Cmd1 was pressed in error, press Cmd3 to go back. You will return to
the Account Assignment Maintenance Assign G/L Accounts screen.

RELEASE 2.1 Lo


 

It is recommended that you request both reports listed on the screen above.
To request the reports, change the N (No) to Y (Yes).


 

The following report prints:

ABC COMPANY ACCOUNT ASSIGNMENT MATNTENANCE Dace 1/05/87 Page 1
BELLINGHAM, A Standard Accounts and Assignmente Time 9.52.39 1598-08,
Manufacturer's Financial Format

Standard Assigned
Account Title Account ‘Title
1900-2 cash on Band & In Bank

pioo2 ‘CASH ON HAND

seco costa
some cere
ST as
vem ceva (
cee cm

 

Review the account assignments carefully. Make any changes necessary in
ACCOUNT ASSIGNMENT MAINTENANCE (X159-2).

The following screen will display:

Account Assignment Maintenance 1592-204
Select Reports
Manufacturer's Financial Format

Account Assignments are now being checked

 

RELEASE 2.1 LO


If all general ledger accounts have been assigned a standard account
number, the following screen will display:

Account Assignment Maintenance ‘x1592-104
Select Reports
Manufacturer's Financial Format

All G/L Accounts are properly assigned.

Enter-Return to menu

 

The Unassigned Accounts report will not print. Press Enter to return to the
menu. If all general ledger accounts have not been assigned to standard
account numbers, the following screen will display:


 

Account Assignment Maintenance x1592-104
Select Reports
Manufacturer's Financial Format

One or more General Ledger Accounts are not assigned.
See the Report of Unassigned Accounts for details.

To assign G/L Accounts to Standard Format Accounts,
use Option 2 to do Account Assignment Maintenance.

Enter-Return to menu

 

Press Enter to return to the menu. The Unassigned Accounts Report will
print. Assign all unassigned general ledger account numbers to standard
account numbers using Account Assignment Maintenance. All valid
standard account numbers are listed on the Standard Accounts and

Assignments report. Below is a sample of the Unassigned Accounts
Report:

RELEASE 2.1 LO


 

ABC COMPANY ACCCUND ASSIGNMENT ATNTENANCE Date 1/06/87 Page i
WaYNOT, CO Unassigned Accounts Time 9.59.38 X159A-5A

Account title Type

21330 ACCUM DEPR-FURNITURE
1349 ‘VEHICLES

p2i29 ‘CUSTOMER DEPOSITS
p2135 BANK NOTES

p21as LOANS -OTHER

paaze SHOP PARTS

paasg RESALE EXEMPT PARTS
peoze COs? OF SALE-USED
peaig COST OF SALE PTs MISC
ps221 INCOWE OTHER,

225, DISCOUNTS EARNED
ps2to VEHICLE MAINTENANCE
5239 DATA PROCESSING

 

ACCOUNTING .


 

### Changing A Standard Account Assignment

Tf a general ledger account number is added in General Ledger
Maintenance, you must assign it to a standard account number before a
Formatted Financial Statement can be run.

If you decide that a general ledger account number is assigned to an
incorrect standard account number, change the standard account number.

From the Financial Report Menu, select option 9, Formatted Financial
Statement Menu. Select option 2, Account Assignment Maintenance.

If more than one Financial Format diskette is loaded onto the system,

select the format you want to work with by placing any character next to {
the format you want to work with. Do not press Enter. The first Assign .
G/L Accounts screen will display automatically. If only one Financial

Format diskette has been loaded onto the system, the first Account

Assignment Maintenance Assign G/L Accounts screen will display after

passing through the security gate.

i
RELEASE 2.1 \


ABC COMPANY.
Division: D

G/L
Account
pio10
p1020
1030
pl110
pl115
DILL7
pis
1119
1200
1210
1220
1230
i250
1260

Type the general ledger number that was added or the general ledger

title
CASH ON HAND
CASH IN BANK

ACCOUNTS RECEIVABLE
WHOLEGOODS RECETVABLE
BALANCE-CONTRACTS
WARRANTY RECEIVABLE
DOUBTFUL ACCOUNTS

NEW INVENTORY

NEW LAWN & GARDEN
USED INVENTORY
PARTS INVENTORY

PREPAID TAX &
PREPAID OTHER

 


 

Account Assignment Maintenance ‘1592-101
Assign G/L Accounts
Manufacturer's Financial Format
Assign to
Standard Acct
1000-2 Cash Cn Hand & In Bank
1000-2 Cash On Hand & In Bank
1000-2 Cash On Hand & In Bank
1110 Accts Rec.-Parts & Service
1110 Acets Rec.-Parts & Service
1110 Accts Rec.-Parts & Service :
12115 Accts. Rec.-wWarranty
1110 Accts Rec.-Parts & Service
1200 New Ford Tractors & Equipment 2
3200 New Ford Tractors & Equipment
122¢ Used Equipment Inventory
1230 Parts Inventory .
1250 Prepaid Taxes & License
1260 Prepaid Other

LICENSE

poe a yaya mem eg

Begin next page with account #: D1260

account number to have the standard account number changed in the :
"Begin next page with Account #" field as illustrated on the screen:


 

ABC COMPANY Account Assignment Maintenance ¥1592-101
Division: D Assign G/L Accounts
Manufacturer's Financial Format

Assign to

Title Standard Acct


CASH ON HAND
CASH IN BANK

ACCOUNTS RECEIVABLE
WHOLEGOODS RECEIVABLE
BALANCE-CONTRACTS
WARRANTY RECEIVABLE
DOUBTFUL ACCOUNTS

NEW INVENTORY

NEW LAWN & GARDEN
USED INVENTORY

PARTS INVENTORY
PREPAID TAX & LICENSE
PREPAID OTHER

1000-2 Cash On Hand & In Bank
1000-2 Cash On Hand & In Bank
1000-2 Cash On Hand & In Bank

1110 Accts Rec.-Parts & Service
1110 Accts Rec.-Parts & Service
1110 Accts Rec.-Parts & Service
1115 Accts. Rec.-warranty

1110 Accts Rec.-Parts & Service
1200 New Ford Tractors & Equipment
1200 New Ford Tractors & Equipment
1220 Used Equipment Inventory

1230 Parts Inventory (
1250 Prepaid Taxes & License

1260 Prepaid Other


Begin next page with Account #: D6850

 

Press Enter. The Account Assignment Maintenance Assign G/L Accounts
screen will display with the account number that was typed at the top of
the screen:

i
RELEASE 2.1 \N


 

ABC COMPANY Account Assignment Maintenance 1592-101
Division: D Assign G/L Accounts

Gi
Account

Dé8s0
6860
6870
p6s80
6890

 

Manufacturer's Financial Format

Assign to
Title Standard Acct

VEHICLE EXPENSE


 

Begin next page with Account #:

Type in the standard account to be assigned to the new general ledger
account number or change the standard account number assigned to any i

general ledger number. Press Enter to register the change.

 

You may type a partial general ledger number in the "Begin next page
with Account #" field. When Enter is pressed, the general ledger number
closest to what was typed will be the beginning account number on the
Account Assignment Maintenance Assign G/L Accounts screen.


 

When all changes have been made, press Cmd1! to end the job. The
following screen displays:

ABC COMPANY Account Assignment Maintenance X1592-104
Division: D Select Reports
Manufacturer's Financial Format

‘Y' for a report of
Standard Accounts and Assignments N

Enter ‘¥’ for a report of
Unassigned accounts N

md1-End job  Cmd3-Go back

 

Change the N to ¥ beside the report listed on the screen if you want to
receive either report. Press Enter. If you do not want either the report,
press Enter to return to the menu.

RELEASE 2.1 LO

## CHAPTER X159-3

APPLY FINANCIAL STATEMENT FORMAT

### Introduction

The form required by the vendor has been placed on diskette or tape. In
this job you apply the financial format on the diskette or tape to your files.
This is the first step in the process.

If changes are made to the required format by the vendor, a new diskette or
tape will be supplied. You will need to replace the financial format with
the new information. Replacing the old format with the new one provided
on the diskette or tape saves the account assignments made in ACCOUNT
ASSIGNMENT MAINTENANCE (X159-2). The Dealer Values are
erased. Dealer Values must be entered again when a format is replaced.

If your main vendor requires financial information be supplied in one
format and a short line vendor requires another format, apply both formats.

Check with DIS for a list of available formats.

MATERIALS

You should have one diskette or tape labeled:

GTM Formatted Financial Statement $/36 1 of 1 Vendor
Name/Format Type

Effective Date: mm/dd/yy

## X159-3 APPLY FINANCIAL STATEMENT FORMAT

cc

 

### How To Run

When using this job, one of three possible conditions exist:

CO You are applying a financial format diskette or tape for the first time
and have never applied a financial format diskette or tape before.

 

 

 

You are applying a financial format diskette or tape for a vendor that is
different from the formats previously applied.

 

O Changes have been made to a financial format that has already been
applied. The financial format needs to be replaced with new
information.

Applying a Financial Format Diskette or Tape for the First
Time

After passing the security gate, the following screen displays:

RELEASE 2.1 (OO


 

Apply Financial Statement Format x1593-101

Insert the Financial Statement Format diskette or tape
and specify either $1 for diskette or TC for tape. --

Qmdi-End job Enter-Continue

Select diskette or tape and press [Enter]. The following screen appears.


 

Apply Financial Statement Format x1593-101

Insert the Financial Statement Format diskette into slot i

emdi-End job —_ Enter-Continue

 

Place the Financial Format diskette sent by DIS into slot 1. Press Enter to
continue.

A confirmation screen displays:


‘AEC COMPANY Apply Financial Statement Format X1593-103
Division: D Verification
Date
Format Title Effective Applied

Manufacturer's Financial Format 12/17/86 1/05/87

will be applied as a new format.

(mdi-Cancel job — Enter-Continue

 

If the name of the format is not the one desired, press Cmd1 to cancel the
job.

If the format is correct, press Enter to continue. The following screen will
display:

ABC COMPANY Apply Financial Statement Format 1593-103
Division: D verification
Date
Format Title Effective Applied

Manufacturer's Financial Format 12/17/86 =: 1/05/87

will be applied as a new format.

This format is now being applied.
Remove the diskette from Slot i and store it in a safe place.

 


 

The format may take several minutes to apply. During this time, you can
remove the diskette and store it in a safe place.

When the format has been applied, the following screen will display:

‘ABC COMPANY apply Financial Statement Forrat 1593-103
Division: D Verification
Date
Format Title Effective applied

Manufacturer's Financial Format 12/17/86 = 1/05/87

This format has been successfully applied.
gnter-Return to menu

When Enter is pressed, the Formatted Financial Statement Menu will
display.

Applying a Different Financial Format than was Previously
Applied

After passing through the security gate, the following screen displays:
LU


 

Apply Financial Statement Format X1593-102

Insert the Financial Statement Format diskette or tape
and specify either $1 for diskette or TC for tape. -~

(mdl-End job —_ Enter~Continue

 

Select tape or diskette and press [Enter] the following screen appears.


 

apply Financial statement Format 1893-101

Insert the Financial Statement Format diskette into sict 1

gmdl-End job Enter-Contimue

 

 

Insert the Financial Format Diskette into Slot 1. Press Enter to continue.
The following screen will display:

RELEASE 2.1 Lo


 

‘ABC COMPANY Apply Financial Statement Format X1593-101
Division: D Format Selection
Date
Format to Apply Eifective
XYZ‘S Financial Format - Ancther Format = 1/17/87

current Formats Effective Applied
Manufacturer's Financial Format 12/17/86 = 1/05/87

Apply as a new format

To select, type any character beside the desired format.

emdi-Cancel job

All the Financial Formats applied will be listed under Current Formats.

The cursor will be positioned in the Apply as a new format field. Place any
character in the field. Do not press Enter. The Verification screen will
display automatically.

If the cursor is moved to the field next to one of the Current Formats and
Enter is pressed on the verification screen that displays next, the financial
format that is on the diskette will replace the financial format listed under
Current Formats. See the section Replace a Financial Format that has
Already been Applied later in this chapter.


 

It is recommended that you save all your Financial Format diskettes. Do
not return them for credit. If a mistake is made, you may need the
Financial Format diskette to reapply the correct Financial Format.

The verification screen will display automatically:

   

ABC COMPANY Apply Financial Statement Format x1593-103
Division: D Verification
Date
Format Title Effective Applied

X¥Z'S Financial Fermat - Another Format 1/17/87 2/05/87

will be applied as a new format.

endl-Cancel job — Cmd3-Go back Enter-Continue

If you do not want to apply the format, press Cmd1 to cancel the job.
If the financial format named is one that was already applied, and should

be replaced, press Cmd3 to go back. See the section Replace a Financial
Format that has Already been Applied.

RELEASE 2.1 tO

### 159-3 Apply Financial Statement Format

 

If the format is correct, press Enter to continue. The following screen will
display:

‘2BC COMPANY Apply Financial Statement Format 1593-103

Division: D Verification
Date

Format Title Effective Applied
X¥Z'S Financial Format - Another Format 1/17/87 2/05/87

will be applied as a new format.

This format is now being applied.
Remove the diskette from Slot 1 and store it in a safe place.

 

  

When the format is applied, the following screen will display:

Apply Financial Statement Format 1593-103

 

verification
Date

Format Title Effective Applied

Manufacturer's Financial Format 12/17/86 1/05/87

This format has been successfully applied.

nter-Return te menu


 

Press Enter to continue. The Formatted Financial Statement Menu
displays.

Replacing a Financial Format

After passing through the security gate, the following screen displays:

Apply Financial Statement Format x1$93-101

Insert the Financial Statement Format diskette or tape
and specify either Si for diskette or TC for tape. --

cmél-End job Enter-Continue

 

Select tape or diskette and press [Enter] the followings screen appears.

RELEASE 2.1 LU


 

Apply Financial Statement Format X1593-101

Imsert the Financial Statement Format diskette into Slot 1

€rdl-End job —_ Enter-Continue

 

Insert the Financial Format diskette into slot 1. Press Enter.

The Format Selection screen will display with the cursor next to the words
Apply as a new format.


 

ABC COMPANY Apply Financial statement Format 1593-101
Division: D Format Selection
Date
Format to Apply Effective
Manufacturer's Financial Format 3/17/87

Current Formats Effective Applied

Manufacturer's Financial Format 12/17/86 = 1/05/87
X¥Z'S Financial Format - another Format 4/17/87 2/05/87

Apply as a new format

To select, type any character beside the desired format
end1-Cancel job

 

Position the cursor next to the format that is to be replaced. Place any
character in the field. Do not press Enter. The Verification screen displays
automatically.

What to do if "Apply as a new format" is used in error:

If the cursor is left next to the words "Apply as a new format," the

format on the diskette will be applied as a new format. Two _ identical
formats with the same name will display on the Format — Selection
screen when this job is selected. You can tell which —_ format is correct
by the Date Applied. The incorrect format would need to be removed.
See Chapter X159-4, REMOVE FINANCIAL STATEMENT FORMAT.

When a new format is applied, there are no account assignments. | Make
sure you remove the new format that was applied in error —_and not the
format that has account assignments already made. If _ the wrong
Financial Format is removed, new account assignments will need to be

RELEASE 2.1 CO


made. See Chapter X159-2 ACCOUNT ASSIGNMENT
MAINTENANCE.

‘REC COMPANY Apply Financial Statement Format 1593-102
Division: D Verification
Date
Format Title Effective applied
Manufacturer‘s Financial Format 3/17/87 3/24/87

will replace

Manufacturer's Financial Format 12/17/86 = 1/05/87

ndi-Cancel job ¢md3-Go back Enter-Continue

Tf the format chosen does not match the one on the diskette, press Cmd3 to
go back to the previous screen. Place any character next to the correct
format. Do not press Enter. The verification screen displays automatically.
When the correct format is displayed on the Verification screen, press
Enter to continue. The following screen appears:


 

apply Financial Statement Format *1593-103
verification

Date
Format Title Effective applied

Nanufacturer's Financial Format 3/17/87 3/24/87

will replace

Manufacturer's Financial Format

This format is now being applied.
Remove the diskette from Slot 1 and store it in a safe place.

 

The old format is replaced with the format that is on the diskette.

Any general ledger account assignments made in Account Assignment
Maintenance (X159-2) will be kept when the format is replaced.

When a format is replaced, it is possible that some standard account
numbers for the vendor have changed. You should check the account
assignments to make sure that the Standard Account assignments are still
valid. You can check account assignments by running the Standard
Accounts and Assignments Report and the Unassigned Accounts Report in
Chapter X159-2.

When the format is successfully applied, the following screen will display:

RELEASE 2.1 LL


ABC COMPANY Apply Financial Statement Format 1593-103
Division: D Verification
Date
Format Title Effective applied

Manufacturer's Financial Format 12/17/86 1/05/87

This format has been successfully applied.

Enter-Return to menu

 

Press Enter to return to the Formatted Financial Statement Menu.

os


Notes:


RELEASE 2.1 CO

## CHAPTER X159-4

REMOVE FINANCIAL STATEMENT FORMAT

### Introduction

This job removes a financial statement format.

Removing a financial format also removes all standard account number
assignments set up in ACCOUNT ASSIGNMENT MAINTENANCE
(X159-2). Make sure this is what you want to do.

Ifa financial format has been changed, you may wish to replace the format
loaded on the computer rather than remove it altogether. To replace the
Financial Format, see X159-3 APPLY FINANCIAL STATEMENT
FORMAT.

## X159-4 REMOVE FINANCIAL STATEMENT FORMAT

 

### How To Run

After passing the security gate, the following screen will display:

ABC COMPANY Remove Financial Statement Format XIS9A-401
Division: D Format Selection
Date

Format Title Effective Applied

Manufacturer's Financial Format 12/17/86 = 1/05/87

X¥Z'S Financial Format - Another Format 1/17/87 2/08/87

fo select, type any character beside the desired format.

cmd1-Cancel job

 

Place any character next to the format to be removed. Do not press Enter.
The Remove Financial Statement Format Verification screen displays
automatically:

RELEASE 2.1 LS


ABC COMPANY Remove Financial Statement Format X159A-402
Division: D Verification
Date
Format Title Effective applied

Manufacturer's Financial Format 12/17/86 1/05/87

Press Enter to remove this format.

Cmdi-cancel job  cmd3-Go back

 

If you do not wish to remove a financial format, press Cmd1 to cancel the
remove. If you chose the wrong format to be removed, press Cmd3 to go
back.

When the correct format is displayed on the Remove Financial Statement
Format Verification screen, press Enter.


 

The following screen will display:

ABC COMPANY Remove Financial Statement Format XI59A-402
Division: D Verification
Date

Format Title Effective Applied

Manufacturer's Financial Format 12/17/86 1/05/87

This format is now being removed. Please wait.

 

RELEASE 2.1 LU


It may take several minutes for the format to be removed. When the
format is removed, the following screen displays:

ABC COMPANY Remove Financial Statement Format X159A-402
Division: D Verification
Date
Format Title Effective Applied

Manufacturer‘s Financia) Format 12/17/86 = 1/05/87

‘This format has been removed.

Enter - Rerurn to menu

Press [Enter] to return to the menu,


Notes:

## CHAPTER X159-5

FFS MONTHLY INVENTORY & SALES REPORT

### Introduction

FFS Monthly Inventory & Sales Report generates a report that summarizes
unit inventory counts and sales counts. The first part of the report, Units
Inventory Counts, lists the number of units in the inventory. The second
part of the report, Sales Counts, lists the number of sales posted to all G/L
sales accounts.

### How To Run

From the Formatted Financial Statement Menu (X15-9), select option 5,
FFS Monthly Inventory & Sales Report. Enter your division and
password at the security gate and press [Enter]. A report is generated and
sent to the system printer. A sample report follows.

## X159-5 FFS MONTHLY INVENTORY & SALES REPORT

LEE'S TRACTOR SALES, INC.
Division: &
Units Inventory Counts

Recount #

P.P.S, MONTHLY INVENTORY AND SALES COUNTS
December, 1994

ary in stock
1 + 30 days

NEW TRACTORS

NEW BQUIPHENT

USED TRACTORS & EOUIPHENT

NeW AUTOS

USED AUTOS

‘TRUCKS:

MOTORCYCLES

RENTAL SQUIP

NEW MOTORCYCLES

USED MOTORCYCLES

Nunber of sales
current month

NEW TRACTORS
NEW BOUIPHENT

OSED TRACTORS-2QUIP
NEW ABTOS

USED AUTOS

‘TRUCKS

MOTORCYCLES

RENTAL EQUIP REVENUE
RENTAL EQUIP SALES
PARTS-WHOLESALE
PARTS- INTERNAL
PARTS-COUNTER
PARTS-SHOP

‘TIRES AND TUBES

ise SALES

SERVICE LABOR-CUSTOMER
SERVICE LABOR-INTERNAL
SUBLET REPAIRS

FREIGH? SALES
‘SALBS-NEW HONDA
‘SALES-USED HONDA
SALES-NEW KRAASAKI
SALES-USED KAWASAKI
SALES-NEW SUZOKI
SALES-USED SUZUKI
SALES-NEW YAMAHA
‘SALES-USED YANARA,
‘SALES-NEW HARLEY-DAVIDSON
‘SALES-USED HARLEY-DAVIDSN
SALES-NEW BMG
SALES-USED BM
SALES-PARTS.
SALES-TIRES & TUBES

Pate 12/29/94
Time 8.29.18

ary in stock
over 30 days

Number of sales
91/94 thru 12/94

Page 2
215950-92

 

V8L5A

## CHAPTER X341-1

CREATE SUGGESTED STOCK ORDER

### Introduction

Create Suggested Stock Order allows you to:
™ request a system-generated stock order based on your specifications.
= view two years of history for parts on the suggested order.
® opt to print comments for parts on the suggested order.
® opt to automatically create separate orders for your different sources
of supply.
= mun the suggested order at a time when the system is not busy or run with
no delay.

## X341-1 CREATE SUGGESTED STOCK ORDER

 

### How To Run

From the Create Stock Order Menu (X34-1), select option 1, Create
Suggested Stock Order. The prompts, which are presented sequentially,
are described below.

ABC COMPANY Create Suggested Stock order x3411-101
Division: E

From the given information a suggested stock order will be printed:

vendor or All
Class(es) or All
12c5700z

Order Start Date

Create source of supply orders? (¥/N)

Source of supply vendor (or All)

Primary or all sources (P/Al1) .
Split order into separate orders by source of supply? (Y/N)

Days Supply (1 to 365} : . 120
Order Number ......... : eee : - $0010909
print on order location, class, comments, and weight? (¥/N)

Print stock transfer report? (¥/N)

Enter character to select by part category sees

Use available/on order quantities to calevlate order? (¥/N)

cmd1-End job Cmd2-Page back

 

RELEASE 2.2 Co


X341-1 CREATE SUGGESTED STOCK ORDER [2]

 

 

 

 

Vendor Code or ALL
Class Code(s) or ALL To request an order for more than
one class, but not all classes, type up
to 3 class codes on the first line and
up to 52 more on the second line.
Press ENTER.
Order Start Date. Type the beginning date of your

stocking period. A future start date
will change the sales history period
the system considers when selecting
parts for the order.

Create Source of Supply Orders? —_—-Y/N. Y displays the next 3 options
for generating orders for parts from
alternate sources. Up to 3 alternate
sources can be set up in Parts Posting
& Maintenance (X3-2). See

## CHAPTER X3-2.

*Source of Supply Vendor (or ALL) Name the specific vendor or ALL to
be considered for source of supply.

*Primary or ALL Sources

(P or ALL) P includes only those parts for which
the vendor is the primary source (1).
ALL includes all parts where the
alternate source is listed as 1, 2, or 3.

O Press FIELD EXIT.

*Split Order into separate orders

PARTS INVENTORY


[ «| X341-1 CREATE SUGGESTED STOCK ORDER

by source of supply?

Days Supply (1 to 365)

O Press FIELD EXIT.

Order Number

Y produces final printed orders
separated by source of supply. Order
numbers are incremented from the
original order number automatically.

Nis OK for manual orders of small
quantities (1 or 2 parts), The result is
a single suggested order sorted by
the source of supply.

The number of days supply this order
will cover. Between 1 - 365.

You may change it to an order name
or number of up to 8 characters.
Order number defaults to
S001MMDD (MM is 2 digits for the
month, DD is 2 digits for the day.)


X341-1 CREATE SUGGESTED STOCK ORDER [=]

Print on order location, class, Y/N, Enter Y to have the specified
comments, and weight? information printed on the order.
Print Stock Transfer Report? ¥ allows for the creation of a stock

transfer report on this order. The
report prints available parts at other
divisions available for transfer.
(X3414 also creates the report. See
the section at the end of this chapter
for more explanation of the stock
transfer report.)

N doesn't print a stock transfer
report.

Enter character to select This prompt refers to the part
category by part category field on the
Parts Posting & Maintenance screen.
It is furnished by some price tapes;
otherwise, it is user-defined. If you
don't want to select a particular class
category, leave this prompt blank.

Use available/on order quantities Enter Y to have available and on
order to calculate order? (Y/N)
quantities considered in the ordering
calculations.

O Press ENTER.

= If you have requested to create a source of supply order, you will see the
three asterisked fields. If you type an N in the Create Source of Supply

PARTS INVENTORY


[ «| X341-1 CREATE SUGGESTED STOCK ORDER co

Orders? (Y,N) you will not see these three fields.

 
   
 

Note:

 
 
 

The demand criteria you specified by class as well as the EOQ formula
will be used in creating the suggested stock order parts. The part(s)
with a C order code will be considered for the order based on the
minimum or maximum stocking levels you specified. If the stocking
levels are missing, the system will automatically calculate them.

 
   
   
 

 

 

RELEASE 2.2 LO


 

### Time Delay

After you fill out the bottom half of the Create Suggested Order screen and
press [Enter], the following screen is displayed:

AGR EQUIPMENT TIME DELAY 0008-201 1
Suggested Stock Order

Time to start job

Cmdl-Cancel Cmd9-No Delay

 

O Fumish a later time for the report to run or, if you want to run it
immediately, press [Cmd9] for no delay.

PARTS INVENTORY


 

A Suggested Stock Order is illustrated below:

ABC COMPARY SUGGESTED S70CK ORDER VENDOR ENG BUSHHOG Pate 9/25/38 Paget
BELLINGHAM, WA 90 DAYS SUPPLY Order + 30930825 ‘Time 16.25.95 3411-58
Classtes): ALL

Sales History sales order
Pazt Number Order Diz Net Current 12 Menths ¢ Previous 12 Monchs To Date OnHand Oty Req Min Eoq Method
Quick Cd Cat Rescription Qty Extended Sep Avg Jul Jun May Apr Mar Feb Jan Dec Nov Cct Prev Yr Avail Pkg/Mult Max Disc SRA

2149 2 2.80 a lL
5.00 ‘ io
5038 a 6.96
27.84
5156 2.45
7432
6085 6.08
13.22
ent 12.46
37.44

st++ VENDOR Tomas NUMBER OF LINES: NuMBER OF PIECES; a5 TOTAL KexGK: (

DEALER LIST: 240,93 SUGGESTED LIST: 127.62, INTERNAL: 95.72 DEALER NET:

NUMBER OF LINES: NUMBER CF PIECES: 15 DEALER NET:

 

RELEASE 2.2 LO


The following stock order was requested for parts where BOB was listed
as the primary source of supply:

A & R SALES & SERVICE SUGGESTED STOCK ORDER VENDOR CRS CASE/IE Date 10/18/98 Page 4

BELLINGHAM. WA
Class(es): &

Part Number
Quick cd cae

SOURCE BOE
13812

19 SOURCE TOTALS NUMBER OF LINES: NUMBER OF PIECE!

365 DAYS SUPPLY order * 50062018 ‘ime 11.33.53 x3421-5A,

Sales History Sales order
order Diz Net Current 12 Months / Previous 12 Months To Date Oniland Qty Req Min Eoq Method
Description Qty Extended Oct Sep Aug Jul Jun May Apr Mar Feb Jan Dec Nov Prev vr Avail Phe/Mult Max Disc SRA

+ UNRROHN
48
CLAMP
Source of Supply #1 11812
Source ef Supply #2 11822
source of supply #3 niisi2
soois1a s 48
16
NUPPLER
Source ef Supply #1 w2aais
Source of Supply #2 24314
Source of Supply #2 reaats
sooiidie $ 16

 

6 TOTAL WEYGHT: 128.0

DEALER LIST: 1212.96 SUGGESTED LIST: 1162.72 INTERNAL; 715.20 DEALER NET:

‘+++ VENDOR TOTALS NUMBER OF LINES: NUMBER OF PIECE:

 

357 TOTAL WEIGHT: 135.3

DERLER LIST: 3087.83 SUGGESTED LIST: 2506.91 INTERNAL: 2225.13 DEALER NET: 1925.13

+147 ORDER TOTALS NUMBER OF LINES: NUMBER OF PIECES: 64 DEALER NET: 725.20

 

PARTS INVENTORY

### Field Descriptions

Part Number
Quick Code
Description

Ext. Part Infor
Order Qty

Dir Net
Extended

Sales History
Sales to date
Prev yr
Onhand Avail
Per job
Pkg/mult
Min

Max

EOQ

Disc
Order Method
SRA(Return Code)

Source totals

Identifying part number.

Identifying code for the part.

Brief description of the part. (Above CLASS
& LOC.)

Comment line information.

Number suggested for ordering.

Cost of the part.

Number on hand multiplied by the cost of
the part.

Each month listed with number of sales of
part, current year, then previous year.

Year to date sales, doesn't include current
month.

Previous year's sales.

Number of part on hand and available.
Number of this part required to complete a
job.

The amount in a package from the vendor.
Minimum to keep in stock at all times.
Maximum to keep in stock at all times.
Economic Order Quantity or the amount it is
most economical to order--calculated by
system using class configured formula.
Number to order for a discount.

Order code: A=Automatic, M=Manual,
C=Combined.

Dealer defined code noting whether
returnable.

Totals for source of supply including
number of lines, pieces, and dollar amount.

### X341-1 Create Suggested Stock Order [J

Vendor totals Number of lines on the suggested order for
the (for each vendor) manufacturer. Number
of pieces, or amount of parts ordered.

Dollar value of the order to the vendor.

Grand totals Number of lines on the entire suggested
order. Number of pieces on the entire
suggested order. Dollar value or amount of
the entire suggested order.

Note:

If you selected the transfer report, you will get the printout. See the
final section in this chapter for a detailed look at the Stock Transfer

 

PARTS INVENTORY


Notes:
LL

co

## CHAPTER X341-2

AS/400 CORRECT STOCK ORDER OR
CREATE MANUAL ORDER

### Introduction

Create Stock Order or Create Manual Order allows you to.

= correct to add to the suggested stock order.
™ create a manual stock order.

CORRECTING EXISTING OR CREATING MANUAL
STOCK ORDERS

From Menu X341 select option 2, Correct Stock Order or Create Manual
Order. The Stock Order Correction entrance screen appears.

AUSTIN TRACTOR & EQUIPMENT STOCK ORDER CORRECTION x3412-101 2
Division: A

Vendor Code .... CAS
Order Number ... 80031113
Enter ‘c' or 'N' C

‘C' = Change existing Order
'N' - Create new Order

For new orders, you may enter a source of supply vendor:

Grdi-Cancei job


[2] X341-2 CORRECT STOCK ORDER OR CREATE MANUAL ORDER

O1 Type the vendor code, if different from the default.

Press [Field Exit].

Type the order number.

O Press [Field Exit].

O To change an existing order, type: C [Field Exit].

© To establish a new order, type: N [Field Exit].

Ci For a new order, type the vendor code for a source of supply if desired.

 

 

 

 

 

 

Note:

 

Source of Supply vendors do not have to be configured in X38-1,
Configure Vendor/Class.

O Press [Enter].
The Stock Order Correction screen will appear in the SCROLL AND
CHANGE LINES mode.
_~


X341-2 CORRECT STOCK ORDER OR CREATE MANUAL ORDER [=]

### Abc Company Stock Order Correction 3412-201

Division: E Price book: BUSHHOG © BHG S0010911 Lines
Current mode: SCROLL AND CHANGE LINES

Quick Qty
Code ordered

€mdi-End Cmd2-serell and change lines cmé3-add lines
cmd4-randomly change lines Cmd5-add new parts

 

Parts Search Window

A Parts Search Window is also available on this screen. To use it, enter a
"2" on either or both sides of a string of characters in the part number field.
The Parts Search Window will display positioning at the beginning of the
string you entered. If you enter a '"*" before a string of characters, the parts
search window is displayed with all part numbers that contain the string of
characters following the asterisk. When the correct part number is found
in the window, the user may select it by placing a'"1" beside it and the
complete part number will be returned to the part number field. Refer to
Parts Inquiry (X3-1) and Parts Posting and Maitenance (X3-2) for more


“s,

[+] X341-2 CORRECT STOCK ORDER OR CREATE MANUAL ORDER a

information on this feature.
Bearing Interchange

By using a pound sign in the part number field along with any bearing
number (such as #689), you can search for a replacement in the Bearing
Interchange Catalog. Screens are illustrated in CHAPTER X7-9, Bearing
Interchange Menu.

In the upper right-hand corner, LINES gives you the number of part
lines in this order and EXTENDED AMOUNT gives you the dollar
amount.

 

### Fields & Descriptions

Part Number Identifying part number.
Quick Code Identifying part code.
Order Quantity Amount of the part ordered.

Press [Enter].

### Options

O To scroll and change lines, press [Cmd2].

RELEASE 2.1 LO


X341-2 CORRECT STOCK ORDER OR CREATE MANUAL ORDER l=]

15 lines will appear on the screen in a sorted sequence. You may only
change the QUANTITY in this mode. Press [Enter] to display the next
14 lines of the order.

Note:

The last part will display as the first on the next screen. A message will!
| display if quantity is negative or greater than 100. Press [Enter] if the
quantity is correct.

 

 

 

 

 

To add lines already in inventory to the order, press [Cmd3]. 15 blank
lines will become available for addition. Type in the parts and
quantities desired. Press [Enter] to add them to the order.

If there are any errors, the screen will clear the parts up to the part with
errors. If error-free, a new screen will display.

If a part number does not exist in your inventory and you try to order
it, you will need to segment the part number as if you were adding it to
your inventory. Type in a less than symbol between segments and at the
end of the part number. This puts the part on the order and put the part
in the default class for the vendor. To add all of the part information
now, use [Cmd5] instead of this [Cmd3] to add the new part to
inventory (explained below). Or go to X32, Parts Posting and
Maintenance, to add the part information later .

O To randomly change lines, press [Cmd4]. 15 lines are available on the


Ls] X341-2 CORRECT STOCK ORDER OR CREATE MANUAL ORDER

screen at one time for changing. The changes may be arranged in any
order on the screen. Type in part number and quantity.

If a part number does not exist in your inventory and you try to order it,
or you enter a part wrong, the message at the bottom of the screen will
say the new part number has an invalid format. This means that how
the part is set up needs to be changed.

Check how the vendor is configured: how many segments or sections
per part number. Then create or change the format by putting < (less
than symbol) between each segment and at the end of the number.

Press [Enter]. This will add the part to inventory with the default class
code, order code, and base codes.

 

 

To DELETE a part from the order, enter a zero for the quantity.
[Press ENTER].

 

 

 

 

Press [Cmd5] to add new part(s) to inventory and to the order. Type a
less than symbol between the segments and at the end of the part #.
You can add all of the part information here. Be sure to enter the part
number before the Order Quantity information. For instance, when
receipting an order with new part numbers, type the part number with
the less than symbol between segments and at the end of the # and
press [Enter]. Add Order Quantity if the part is being added to the
order. Add Suggested List and Dealer Net prices and press [Enter]. The
other prices will be adjusted according to the class configuration in
X38.


X341-2 CORRECT STOCK ORDER OR CREATE MANUAL ORDER [7]

### Fields & Descriptions

Division Division code. Default ©
Order Qty Amount of the new part on order. on
If you leave this field blank, the c
part will be added to inventory but ° Y
will NOT be ordered.
Vendor Vendor code of the new part. 3 characters oO
Part Number Identifying part number. 22 characters 9
Description Brief description of the new part. 16 characters v
Class Dealer-defined classification code
on part. 1 character
Quick Code Alternate method of calling up part.
Location Location of the new part in your
dealership. 8 characters
Order Code Code noting whether manual (M),automatic (A), or
combined manual and automatic (C) ordering used.
1 character
Return Code Notes whether part is return able: 1 character
R = Retumable, N = Not returnable.
Part Category Code from price tape noting the

account type: A = Accessory,
P = Part, or O = Other. 1 character
Weight Weight of the part. 5 digits
Price Four prices on the part: 7 digits
DLR LIST = Selling price, based on 3.
SUG LIST = Manufacturer's suggested
list, based on 3.
INTERNAL = Optional fieid, usually
for competitor's price.
DLR NET = Cost of part, based on 1.

## X341-2 CORRECT STOCK ORDER OR CREATE MANUAL ORDER C

Base Base of the four pricing fields,
listed above. 1 character
Minimum Minimum you want to stock or
best reorder point. 5 digits
Maximum Maximum stocking level. 5 digits
Qty Rqd Quantity of this part required to
do a job. 5 digits.
Package Quantity per package (e.g., spark plugs
4 per package, enter 4 here).
Multiple Order quantity reflects vendor multiple.

Oil in a 55 gallon drum would be ordered
as 1. Enter 55 here. 5 digits
Discount Quantity to order to get a discount. 5 digits

### Options

0 Press [Cmd3] to add these new parts to the order.

O Press {Cmd1] to end the job, return to the entrance screen. Process
another order, or press [Cmd1] again to return to the Create Stock
Order Menu.

Press [Cmd2] to change the vendor.

 

 

 

 

 
   
 

Note:

 
 
 

For all of these operations, ensure that you press [Enter] before taking
a [(Cmd1] to end the job or change modes. Otherwise the changes or
additions will not be made. Then press {Cmd1].

 

 
   

 

RELEASE 2.1 —

## CHAPTER X341-3

PRINT/FINALIZE ORDER

### Introduction

Print Final Order allows you to.

= Print your suggested or manual stock order,

= Finalize (close) and print your Suggested or manual order.

= Transmit orders via the DIS Electronic Commerce Manager to a PC or
directly to a host computer, such as Case.

You cannot make changes to orders after they are finalized; therefore, you
should make sure they are complete before you select the option to
finalize.

 
    

If there is a problem, lines can be moved into a different order number
by using Move Order Lines (X34-6).

 

All orders are printed when they are finalized. Two copies are printed
side-by-side so you can separate the form, send one to the vendor, and
keep the other for your records.

An additional screen, is presented when an order for the following vendors
is finalized:

- AGCO Solutions™ On-Line (see page 8)

Case (see page 12)

Clarknet Till (see page 13)

Kubota (see page 19)

New Holland (see page 20)

Its purpose is to capture information Tegarding the order before the DIS
Electronic Commerce Manager and Electronic Commerce Client transfer it
to the PC and subsequently to a vendor. For Case, orders are transferred
directly to the Case host computer. To learn more about DIS Electronic
Commerce Manager and Client, see Chapters X6-15 and X6.15-1, which
include configuration and troubleshooting instructions.


[2] X341-3 PRINT/FINALIZE ORDER

### How To Run

From the Create Stock Order Menu (X341), select option 3, Print/Finalize
Order. The Print/Finalize prompts are displayed, as illustrated below.

LRB SALES & SERVICE PRINT FINAL STOCK ORDER ¥3413-101 1

Vendor Code MAN

order Number 50010306

Finalize (¥/N) N

(mdi-Cancel job

Type the vendor code and order number.

O To print a stock order without finalizing it, leave the default of N in the
Finalize (Y/N) prompt. Press Enter. The order is printed.

 

O To finalize a stock order, change the default to Y in the Finalize (Y/N)
prompt. Press [Enter]. Additional prompts are displayed as illustrated
below.
Cc


X341-3 PRINT/FINALIZE ORDER

LRB SALES & SERVICE PRINT/FINALIZE ORDER x3413-101 1

Vendor Code MAN
Order Number 0010306

Finalize (Y/N) ¥

Dealer Number 123456

Special Shipping Instructions

UPS GROUND

md1~Cancel job

 

QO Type your Dealer Number and any special shipping instructions. Press
[Enter].

PARTS INVENTORY


X341-3 PRINT/FINALIZE ORDER

 

An example of an order printout follows.

LRS SALES & SERVICE LAB SALES & SERVICE

StH ST AND VINE STH 7 AND VINE

wiywor, co 63204 weno, co e3204
ORDER NUMBER O407860N ORDER NUMBER 0407860"
DEALER NUMBER 22257 DEALER NUMBER 22257


MASSEY-PERGUSON 9/30/97 MASSEY-FERGUSON 9730/97

or mare » osenzrien hwoan tscann me 28 te # + pescrvesa
we wa voor as oe var wea
we cont “os n-ne a come 0

rem, . rem
355m . 3550
saa . nase
sem . . sem
456n92 - ésono1
60n91 - : a60N91

197N92 - - a97m91 STOP CABLE

sehv+ ORDER TOTALS teat

+ 8 oF Lines .

 


X341-3 PRINT/FINALIZE ORDER [=]

The following stock order was requested for parts where BOB was listed
as the primary source of supply. Note that the manufacturer's part numbers
are listed on the left and the alternate source's part numbers are listed on
the right. The order is received as if the manufacturer's part numbers had
been ordered and received.

 

PARTS INVENTORY


X341-3 PRINT/FINALIZE ORDER

 

URB SALES & SERVICE
288 Wes? KELLOGG RD 288 WEST KELLOGG RD
BELLINGHAM, WA 98225, BELLINGHAM, WA

Order Nuxher 0061018 order Number  $0061018

Dealer Number Dealer Number

Special Shipping Tastructions: Specia) Shipping instructions:

BEST KAY BEST WAY

cASE/IH 30/22/93 10/18/93 Page

aty Part # + neseriprion cost Amount Leeation Pack S-S Part "Description
rea 9.31 446.88 6242 2M BOB NI1612 CLAMP
aa 16.77 268.32 2m Bop 824314

LRA SALES & SERVICE
order munber 50061018
Dealer Nusber
cASE/IH 10/18/93 Page
order Totals *****
+ 4 Of Lines :

+ 8 Of parts

 

LU


X341-3 PRINT/FINALIZE ORDER

 

### Fields & Descriptions

The fields on the report are described below:

Co. & address ‘Your company name and address.

Order # Number assigned to the order by the dealer.

Dealer # Number assigned by the vendor to your
dealership.

X----------- Authorization signature area.

Ship via Notes how you would like order shipped.

Qty Quantity of the part to be ordered.

Part number Identifying part number.

Description Brief description of the part on order.
You may divide the report here; send one and
keep one.

Cost Cost to the dealership of this part.

Extended amount Quantity of the part ordered times the cost.

Location Location of the part in your dealership.

Pack If a packaged part, the number per package is
listed.

S/S Source of Supply. If this part has a source of

supply, your inventory number is listed in the
PART# field and the source of supply part
number is listed under the CODE field.

Code Quick code or source part number.
Description Description of part.

Qty Quantity of the part on order.

Order totals Includes the number of lines, parts and dollars.

PARTS INVENTORY


X341-3 PRINT/FINALIZE ORDER

 

### Agco Order Information Screen

If you’re using DIS Electronic Commerce to transfer files to and from a
PC, the following screen will be displayed after an order for a configured
AGCO vendor has been finalized:

LRB SALES & SERVICE AGCO Solutions On-Line AGC1O0ORDi
Division A Ordex Information WHT CT00132

Miscellaneous VIP Information

order Class Brand

Discount /Terms Model

Promotion Code Serial Number
Customer Name

Shipping Information Drop Ship

Carrier Code Name Pat Rose Construction Co.
Alternate Carrier Code Address (1) 1708 High Noon Rd.
PDC Code Address (2)
Ship To Location Address (3)
city Bellingham
State WA,
Zip Code 98226
Phone

F2=Continue

Note
VIP fields are available for Order Class 06 only. Drop Ship fields are
available for drop ship orders (Ship to Location 01) only.

 


X41-3 PRINT/FINALIZE ORDER [2]

When this screen is complete, press F2=Continue. The order will be
picked up by DIS Electronic Commerce Client within 10 minutes (or the
polling time you selected) and transferred to the appropriate directory for
AGCO Solutions On-Line.

The default order class is "03" for a stock order, but it can be changed on
this screen. Order classes are:

Priority Order

Daily Order

Dealer Mid-Week Fill-In Order

Dealer Weekly Stock Order

New Dealer/Product Initial Order

Promotional Order

VIP Order

NYAWERWHH

F4=Prompt is valid in the following fields:
= Order Class

= Carrier Code

= Alternate Carrier Code

= PDC Code

= Ship To Location

= Brand (VIP Information)

Miscellaneous Fields

Order Class 2 digits. Press F4=Prompt in this field to
select from a list.

Discount/Terms 1 character. 0=Discount, 1=Terms.

Promotion Code 4 characters. No specific value required.

PARTS INVENTORY


[>] X341-3 PRINT/FINALIZE ORDER

Shipping Information Fields

Carrier Code
Alternate Carrier Code
PDC Code

Ship To Location

4 characters. Press F4=Prompt in this field
to select from a list.

4 characters. Press F4=Prompt in this field
to select from a list.

1 character. Press F4=Prompt in this field to
select from a list.

2 characters. Press F4=Prompt in this field
to select from a list. When this field is "01,"
the Drop Ship fields will be available.

Note: For most AGCO dealers, 00 and 01

are the only valid values for this field;

however, some AGCO dealers may have (
valid Ship To Locations of 00-05. Since 02-

05 are not defined for all AGCO dealers, use

01 here and change it to 02-05 in AGCO

Solutions On-Line.

VIP Information (Order Class 06 only)

Brand

Model
Serial Number
Customer Name

30 characters, case specific. Press
F4=Prompt in this field to select from a list.
30 characters.

30 characters.

30 characters.

Drop Ship Fields (Ship To Location 01 only)

Name

Address (1) ~ (3)
City

30 characters. The first 2 characters of the
extended name, if any, will appear in the last
2 positions of this field.

30 characters.

19 characters.

(


X341-3 PRINT/FINALIZE ORDER Le]

State 2 characters,

Zip Code 9 characters. This field accepts 5-digit U.S.
zip codes or 9-digit U.S. zip codes. In
addition, it accepts 6-character Canadian
postal codes.

Phone 3-3-4 digits for area code and telephone
mumber.

PSO# Update

Finalized orders are listed on the Order Inquiry screen as usual. After they
have been transmitted using AGCO Solutions On-Line, DIS Electronic
Commerce Client (ECC) monitors AGCO orders for a change in the PSO
field on the PC. When AGCO updates this field, ECC updates the PSO #
on the DIS Business System.

PARTS INVENTORY


[2] X341-3 PRINT/FINALIZE ORDER co

### Case Order Information Screen

LRB SALES & SERVICE PRINT/FINALIZE ORDER CASLODORDI
Division: T Order Information cas 0010324

Shipping Information

Order Type 2
Routing

If the Case computer is down,
you can bypass communications (
and fax the printed order.

Bypass communications (N/y) _

F2=continue F4=Prompt.

 

To select from a list of valid Order Types, place the cursor in the Order
Type field and press F4=Prompt. You will be able to choose from:

[1 | Unit Down, Air_]

 
 
   
   
     

 
 

Lo


X341-3 PRINT/FINALIZE ORDER |

### Clarknet Order Information Screen

If you’re using DIS Electronic Commerce to transfer files to and from a
PC, the following screen will be displayed after an order for the
configured Clarknet III vendor has been finalized:

LRB SALES & SERVICE Clarknet, CyT1oooRDL

Division A Order Information MEL S0010616

Miscellaneous

Order Class

Shipping Information

Mode of Transportation __
Carrier Code

priority

Back Order Mode

Back Order Carrier Code
Back Order Priority

 

The default order class is "3" for priority orders and "4" for stock orders,
but there are 4 order classes in all:

1 Break down order under warranty

2 Break down order not under warranty

PARTS INVENTORY


X341-3 PRINT/FINALIZE ORDER Co

3 Break down not under warranty (ships within 24 hours)
4 Weekly stock order

Different prompts are presented for each order class; for example, a serial
number (up to 21 characters) is required for order classes 1 and 2.

### Warning

Tf the serial number contains a tilde (~), substitute a period or a dash for
the tilde.

 

If the order class is 1, 2, or 3, "Ship To Flag" is available. When the "Ship
To Flag” is "Y," name and address fields are available. For drop ships, the
"Ship To Flag" is automatically set to “Y," and the name and address are {
transferred to the Order Information screen, as illustrated below: .


X341-3 PRINT/FINALIZE ORDER

LRB SALES & SERVICE Clarknet,
Division A order Information
Miscellaneous

Order Class
Ship to Flag

Shipping Information Drop Ship

Mode of Transportation ATR Name RICHARD BURKIN
Carrier Code FEDX Address (1) 1101 MONTPELIER DR
Priority NEA Address (2)
Back Order Node AIR Address (3)
Back Order Carrier Code FEDX Address (4)
Back Order Priority KA city

state

zip Code

 

Shipping Information Fields

Mode of Transportation 3 characters,
Carrier Code 4 characters.
Priority 3 characters.
Back Order Mode 3 characters.
Back Order Carrier Code 4 characters.
Back Order Priority 3 characters.

Valid shipping options are listed in the table on page 14.

PARTS INVENTORY


[3] X341-3 PRINT/FINALIZE ORDER

Drop Ship Fields
Name

Address (1) - (4)
City

State

Zip Code

30 characters. The first 2 characters of the
extended name, if any, will appear in the last
2 positions of this field.

30 characters.

19 characters.

2 characters.

9 characters. This field accepts 5-digit U.S.
zip codes or 9-digit U.S. zip codes. In
addition, it accepts 6-character Canadian
postal codes.

### Warning

Enter Canadian postal codes without a space; for example, enter V8V
2K2 as V8V2K2. Leaving a space will render your order irretrievable!

 


X341-3 PRINT/FINALIZE ORDER

 

Clarknet Shipping Options

For descriptions of the shipping options (explanations of the
abbreviations) in the following table, see next page.

    

CARRIER EXTENSION | PRIORITY
EXTENSION

[i

Z|
a

   

clefcicicic anfaiaia
RISIS UIs mimjm
oOo

ie) gQizls Olziz oyZ wn
z bn >

   

XXXX
BUS Cs
TAK Ce
TRK XXXX

    

PARTS INVENTORY


X341-3 PRINT/FINALIZE ORDER

 

Descriptions of Shipping Options

    
 

 
 

[Option | Description
AIR, BUS, TRK, SEA | Mode of transportation to air in delivery of order

CARRIER UPS=United Parcel Service

FEDX=Federal Express
PRIORITY

    

  
   
     
 
  

EMER=Emery

XXXX=4-character abbreviation of carrier, such as
RDWY=Roadway or UAL=United Air Lines
EAM=Early AM.
HTG=Hot Tail Gate
NXA=Next day A.M.
NXP=Next day P.M.
NS=Not specified
SAT=Saturday deliver
SD=Same day
2ND=Second day
3RD=Third day select
4HR=Pick up in 4 hours

  
  
     
     
   
   
   
   
   

  
CC


X341-3 PRINT/FINALIZE ORDER

### Kubota Order Information Screen

If you’re using DIS Electronic Commerce to transfer files to and from a
PC, the following screen will be displayed after an order for the
configured Kubota vendor has been finalized:

LRB SALES & SERVICE KUBOTA, KUB1000RD2

Division A order Information KUB CT00146

Valid order types are:

2=Emergency

4=Regular
6=Stock

F2=Continue

 

O Press F2=Continue. If you have started the DIS Electronic Commerce
Client The order will be picked up within 10 minutes (or the polling
time you selected) and transferred to the appropriate directory for
KubotaLink.

PARTS INVENTORY


[>] X341-3 PRINT/FINALIZE ORDER

### New Holland Order Information Screen

If you’re using DIS Electronic Commerce to transfer files to and from a
PC, the following screen will be displayed after an order for the
configured New Holland vendor has been finalized:

LRB SALES & SERVICE New Holland NHDLOOORD?
Division A Order Information FOR CT00183
Miscellaneous

Order Class
Sales Program Name

Shipping Information Drop Ship

Ship Code A Name Pat Rose Construction Co.
Special Ship to Number Address (1) 1708 High Noon Rd.

city Bellingham

State WA

Zip Code 98226

Attention

F2=Continue Fa=Prompt

 

The default order class is U for priority orders and S for stock orders, but
there are 5 order classes in all:
A=Annual


X341-3 PRINT/FINALIZE ORDER [2]

D=Direct (maximum=50 lines)
F=Fill-In (maximum=50 lines)
S=Stock

U=Unit Down (maximum=50 lines)

Technical note: Parts order filenames are 8 characters plus a 3-character
extension, such as Nxxxxxxx.P$R, where N represents the type of order,
such as S=Stock, "P" signifies a parts order, and R=Ready to Send. When
the file has been successfully sent the extension is renamed to P$S, which
prevents the file from being sent again but retains it for future use.

Miscellaneous Fields

Order Class 1 character. Press F4=Prompt to select from
a list of valid classes.

Sales Program Name 6 characters. Optional.

Shipping Information Fields

Ship Code 1 character. Press F4=Prompt to select from

a list of valid shipping codes.
Special Ship to Number 2 characters.

Drop Ship Fields (Available tor Fill-in (F) and Drop Ship (U) orders only)

Name 30 characters. The first 2 characters of the
extended name, if any, will appear in the last
2 positions of this field.

Address (1) 30 characters.

City 20 characters.

State 2 characters.

Zip Code 9 characters. This field accepts 5-digit U.S.

zip codes or 9-digit U.S. zip codes without a
space or dash. In addition, it accepts
Canadian postal codes.

PARTS INVENTORY


[2] X341-3 PRINT/FINALIZE ORDER

Attention

30 characters. Use for the customer’s name
when an order is being picked up at the PDC
(Parts Distribution Center).

## CHAPTER X341-3

PRINT/FINALIZE ORDER

### Introduction

Print Final Order allows you to.
= Print your suggested or manual stock order.
= Finalize (close) and print your suggested or manual order,

You cannot make changes to orders after they are finalized; therefore, you
should make sure they are complete before you select the option to
finalize.

Note

If there is a problem, lines can be moved into a different order number
by using Move Order Lines (X34-6).

 

All orders are printed when they are finalized. Two copies are printed
side-by-side so you can separate the form, send one to the vendor, and
keep the other for your records.

An additional screen, is presented when an order for the following vendors
is finalized:

= AGCO (see page 7)

= Clarknet (see page 11)

= Kubota (see page 16)

" New Holland (see page 17)

Its purpose is to capture information regarding the order before the
Electronic Commerce Manager and Electronic Commerce Client transfer it
to the PC. On the PC, the vendors programs will be able to pick it up and
eventually transfer it to the vendor. To lear more about DIS Electronic
Manager and Client, see Chapters X6-15 and X6.15-1, which include
configuration and troubleshooting instructions.


[2] X341-3 PRINT/FINALIZE ORDER Co

### How To Run

From the Create Stock Order Menu (X341), select option 3, Print/Finalize
Order. The Print/Finalize prompts are displayed, as illustrated below.

PRINT FINAL STOCK ORDER X3413-101 1

Vendor Code MAN
Order Number $0010306

Finalize (¥/N) N

Cmdi-Cancel job

 

O Type the vendor code and order number.

O To print a stock order without finalizing it, leave the default of N in the
Finalize (Y/N) prompt. Press Enter. The order is printed.

C To finalize a stock order, change the default to Y in the Finalize CY/N)

prompt. Press [Enter]. Additional prompts are displayed as illustrated
below.

RELEASE 2.1 LL


X341-3 PRINT/FINALIZE ORDER

ABC COMPANY PRINT/FINALIZE ORDER X3413-101 1

Vendor Code MAN
Order Number 0010306

Finalize (¥/u) ¥

Dealer Number 123456

Special Shipping Instructions

UPS GROUND

Grdi-cancel job

 

O Type your Dealer Number and any special shipping instructions. Press
[Enter].

PARTS INVENTORY


X341-3 PRINT/FINALIZE ORDER

An example of an order printout follows.

ABC COMPANY AOC COMPANY
STH ST AND vine STH ST AND VINE
waYNOT, CO 83206 WOT, co ex2ca
ORDER NUMBER 04072608 cape2 NUMBER 94078608
DEALER NUMBER 22757 DEALER NUKBER 72257
Hee - Xe
MASSEY-FERGUSON 9730797 pace MASSEY-PERGUSON 9/30/97 PAGE
Ory paar a. DESCRIPTION COST AMOUNT LOCATION PACK $-5 PART #-. + DESCRIPTION
O15 8428 wasHER heae 3.54 $52-3 035 Baan WASHER
020 092491 KIT MOUNT: 43.75 43,78 220 992491 KIT MOUNT
022 327K & RING 236 5aa-7 922 327% E RING
254 iBama BOLT 7 73 ated 254 igem Pour
260 r03Me1 caane 322.00 322.00 sw coRNE 260 103M92 CHAIN
388 74542 ree 16.93 358 745K1 tee

726m 7 72682
355e1 5. 235K
aa3ea 6 . 24362

ésamea . : esau
a5eHo1 : 4seyo1
Beong2 e60ns2

97mg ‘STOP CRELE . 197892 STOP CABLE

ORDER TOTALS ***++

4 OF LINES 2B

4 OP PARTS 24

DOLLARS

 

RELEASE 2.1 Lo


X341-3 PRINT/FINALIZE ORDER

The following stock order was requested for parts where BOB was listed

as the primary source of supply.

Note that the manufacturer's part numbers

are listed on the left and the alternate source's part numbers are listed on
the right. The order is received as if the manufacturer's part numbers had

been ordered and received.

AG R SALES & SERVICE
288 WEST KELLOGG RD
BELLINGHAM, WA 98226

order Number
Dealer Nunber

9062618

Kenn

Special Shipping Instructions:
BEST way
casusTH 19/18/93
---* Description Amount Location
246.88 sc142
268,32

A&R SALES & SERVICE
Order Number  sogsio1a
Desier Nunber
caserta

20/18/59 page 2

268 WEST KELLOGG RD
BELLINGHAM, WA

Order Number
Deeler Number

soosteie

x eee

Speciel Shipping tnstruccions:
BEST WAY
10/36/93,

Pack S-8 Pare #---
2w BOR Wi2E22
2m BoE B26314

s--* Description
CLAMP:

seees oxder Totals *er*

v4 Of Lines

+ 8 Of Parts

Dolvers

PARTS INVENTORY

nas.


Le] X341-3 PRINT/FINALIZE ORDER

### Fields & Descriptions

The fields on the report are described below:

Co. & address
Order #
Dealer #

XKennn-------
Ship via
Qty

Part number
Description

Cost

Extended amount
Location

Pack

S/S

Code
Description

Qty

Order totals

Your company name and address.

Number assigned to the order by the dealer.
Number assigned by the vendor to your
dealership.

Authorization signature area.

Notes how you would like order shipped.
Quantity of the part to be ordered.
Identifying part number.

Brief description of the part on order.

You may divide the report here; send one and
keep one.

Cost to the dealership of this part.

Quantity of the part ordered times the cost.
Location of the part in your dealership.

If a packaged part, the number per package is
listed.

Source of Supply. If this part has a source of
supply, your inventory number is listed in the
PART# field and the source of supply part
number is listed under the CODE field.
Quick code or source part number.
Description of part.

Quantity of the part on order.

Includes the number of lines, parts and dollars.


X341-3 PRINT/FINALIZE ORDER [7 |

### Agco Order Information Screen

If you’re using DIS Electronic Commerce to transfer files to and from a
PC, the following screen will be displayed after an order for a configured
AGCO vendor has been finalized:

AGR EQUIPMENT SALES AGCO Solutions On-Line AGC1OCORDA
Division a Order Informaticn WHT CT00132

Miscellaneous VIP Information

Order Class Brand

Discount/Terms Model

Promotion Code Serial Number
Customer Name

Shipping Information Drop Ship

Carrier Code Name Pat Rose Construction Co.
Alternate Carrier code Address (1) 1708 High Noon Rd.

PDC Code Address (2)

Ship To Location Address (3)
city Bellingham

State wa,
zip Code 98226
Phone

F2=Continue F4=Prompt

Note
VIP fields are available for Order Class 06 only. Drop Ship fields are
available for drop ship orders (Ship to Location 01) only.

 

PARTS INVENTORY


X341-3 PRINT/FINALIZE ORDER : C s

When this screen is complete, press F2=Continue. The order will be
picked up by DIS Electronic Commerce Client within 10 minutes (or the
polling time you selected) and transferred to the appropriate directory for
AGCO Solutions On-Line.

The default order class is "03" for a stock order, but it can be changed on
this screen. Order classes are:

NAUDUAwWNE

Priority Order

Daily Order

Dealer Mid-Week Fill-in Order
Dealer Weekly Stock Order

New Dealer/Product Initial Order
Promotional Order

VIP Order

F4=Prompt is valid in the following fields:

Order Class

Carrier Code

Alternate Carrier Code
PDC Code

Ship To Location

Brand (VIP Information)

Miscellaneous Fields
Order Class 2 digits. Press F4=Prompt in this field to

select from a list.

Discount/Terms 1 character. 0=Discount, 1=Terms.
Promotion Code 4 characters. No specific value required.

CO


PARTS INVENTORY

X341-3 PRINT/FINALIZE ORDER [2]

Shipping Information Fields

Carrier Code
Alternate Carrier Code
PDC Code

Ship To Location

4 characters. Press F4=Prompt in this field
to select from a list.

4 characters. Press F4=Prompt in this field
to select from a list.

1 character. Press F4=Prompt in this field to
select from a list.

2 characters. Press F4=Prompt in this field
to select from a list. When this field is "01,"
the Drop Ship fields will be available.

Note: For most AGCO dealers, 00 and 01
are the only valid values for this field;
however, some AGCO dealers may have
valid Ship To Locations of 00-05. Since 02-
05 are not defined for all AGCO dealers, use
01 here and change it to 02-05 in AGCO
Solutions On-Line.

VIP Information (Order Class 06 only)

Brand

Model
Serial Number
Customer Name

30 characters, case specific, Press
F4=Prompt in this field to select from a list.
30 characters.

30 characters.

30 characters.

Drop Ship Fields (Ship To Location 01 only)

Name

Address (1) ~ (3)
City

30 characters. The first 2 characters of the
extended name, if any, will appear in the last
2 positions of this field.

30 characters.

19 characters.


X341-3 PRINT/FINALIZE ORDER co

State 2 characters.

Zip Code 9 characters. This field accepts 5-digit U.S.
zip codes or 9-digit U.S. zip codes. In
addition, it accepts 6-character Canadian
postal codes.

Phone 3-3-4 digits for area code and telephone
number.

PSO# Update

Finalized orders are listed on the Order Inquiry screen as usual. After they

have been transmitted using AGCO Solutions On-Line, DIS Electronic

Commerce Client (ECC) monitors AGCO orders for a change in the PSO

field on the PC. When AGCO updates this field, ECC updates the PSO # (
on the DIS Business System.

RELEASE 2.1 C


X341-3 PRINT/FINALIZE ORDER [vy

### Clarknet Order Information Screen

If you’re using DIS Electronic Commerce to transfer files to and from a
PC, the following screen will be displayed after an order for the
configured Clarknet III vendor has been finalized:

AgR EQUIPMENT SALES Clarknet CNTLOCORDI,

Division a Order Information MEL $0010616

Miscellaneous

Order Class

Shipping Information

Mode of Transportation
Carrier Code

Priority

Back Order Mode

Back Order Carrier Code
Back Order Priority

  

The default order class is “3" for priority orders and "4" for stock orders,
but there are 4 order classes in all:

1 Break down order under warranty

2 Break down order not under warranty

3 Break down not under warranty (ships within 24 hours)
4 Weekly stock order

PARTS INVENTORY


[2] X341-3 PRINT/FINALIZE ORDER CO

Different prompts are presented for each order class; for example, a serial
number (up to 21 characters) is required for order classes 1 and 2.

### Warning

If the serial number contains a tilde (~), substitute a period or a dash for
the tilde.

 

If the order class is 1, 2, or 3, "Ship To Flag” is available. When the "Ship
To Flag” is "Y," name and address fields are available. For drop ships, the
"Ship To Flag" is automatically set to "Y," and the name and address are
transferred to the Order Information screen, as illustrated below:

ASR EQUIPMENT SALES Clarknet CNTIO00RDI (
Division A Order Information MEL CT00333
Miscellaneous

order Class
Ship to Flag

Shipping Information Drop Ship

Mode of Transportation AIR Name RICHARD BURKIN
Carrier Code FEDX Address (1) 1102 MONTPELIER DR
Priority NAA Address (2)
Back Order Mode AIR Address (3)
Back Order Carrier Code FEDX Addxess (4)
Back Order Priority NRA city GREENSBORG

state NC

Zip Code 27420

 

RELEASE 2.1 LL


PARTS INVENTORY

X341-3 PRINT/FINALIZE ORDER

Shipping Information Fields

Mode of Transportation 3 characters.
Carrier Code 4 characters.
Priority 3 characters.
Back Order Mode 3 characters.
Back Order Carrier Code 4 characters.
Back Order Priority 3 characters.

Valid shipping options are listed in the table on page 14.

Drop Ship Fields

Name 30 characters. The first 2 characters of the
extended name, if any, will appear in the last
2 positions of this field.

Address (1) - (4) 30 characters,

City 19 characters.

State 2 characters.

Zip Code 9 characters. This field accepts 5-digit U.S.

zip codes or 9-digit U.S. zip codes. In
addition, it accepts 6-character Canadian
postal codes.

### Warning

Enter Canadian postal codes without a space; for example, enter V8V

2K2 as V8V2K2. Leaving a space will render your order irretrievable!


X341-3 PRINT/FINALIZE ORDER

 

      
 

     
   
 
 

Cc
Clarknet Shipping Options

For descriptions of the shipping options (explanations of the

abbreviations) in the following table, sce next page.

| MODE EXTENSION | ARRIER EXTENSION | PRIORITY

EXTENSION

[AIR FEDX

LAR

LAR Psp

[AR [ano (

[EAM

zZ
|

=
Ba]

ARE
>[al7|
cicic nay
SSE |salalalaya gale} &
se >< PK DX

TRK
RK

ale jolzl2 a
x > >

ala
z

TRK
TRK
TRK

x{Cic]yv Zylo
z[slalalaialals
Rg 5 ryo

   

   

>

XXX HTG

 

RELEASE 2.1 LL


X341-3 PRINT/FINALIZE ORDER Le]

Descriptions of Shipping Options

AIR, BUS, TRK, SEA | Mode of transportation to air in delivery of order

CARRIER UPS=United Parcel Service

FEDX=Federal Express
PRIORITY

 
 
  
 
 

 
  

    

 

   

EMER=Emery

XXXX=4-character abbreviation of carrier, such as
RDWY=Roadway or UAL=United Air Lines
EAM=Early A.M,

HTG=Hoet Tail Gate

NXA=Next day A.M.

NXP=Next day P.M.

NS=Not specified

SAT=Saturday deliver

SD=Same day

2ND=Second day

3RD=Third day select

4HR=Pick up in 4 hours

     
   

     
    

  
 

   
      
   
   
      

PARTS INVENTORY


[=] X341-3 PRINT/FINALIZE ORDER co

### Kubota Order Information Screen

If you’re using DIS Electronic Commerce to transfer files to and from a
PC, the following screen will be displayed after an order for the
configured Kubota vendor has been finalized:

AGR EQUIPMENT SALES KUBOTA KUBLOOORDI

Division A order Information KUB CT00146

Valid order types are: (
2=Emergency

4=Regular
6=Stock

F2=Continue

 

C Press F2=Continue. If you have started the DIS Electronic Commerce
Client The order will be picked up within 10 minutes (or the polling
time you selected) and transferred to the appropriate directory for
KubotaLink.

RELEASE 2.1 LO


X341-3 PRINT/FINALIZE ORDER

 

### New Holland Order Information Screen

If you’re using DIS Electronic Commerce to transfer files to and from a
PC, the following screen will be displayed after an order for the
configured New Holland vendor has been finalized:

AGR EQUIPMENT SALES New Holland NHD1OGORD1
Division A order Information FOR CTC0183
Miscellaneous

Order Class
Sales Program Name

Shipping Information Drop Ship

ship Code A Name Pat Rose Construction Co.
Special Ship to Number __ Address (1) 1708 High Noon Rd.

city Bellingham

State

Zip Code

Attention

 

F2=Continue

 

The default order class is U for priority orders and S for stock orders, but
there are 5 order classes in all:

A=Annual

D=Direct (maximum=50 lines)

F=Fill-In (maximum=50 lines)

S=Stock

U=Unit Down (maximum=S0 lines)

PARTS INVENTORY


| X341-3 PRINT/FINALIZE ORDER

Technical note: Parts order filenames are 8 characters plus a 3-character
extension, such as Nxxxxxxx.P$R, where N represents the type of order,
such as S=Stock, “P” signifies a parts order, and R=Ready to Send. When
the file has been successfully sent the extension is renamed to P$S, which
prevents the file from being sent again but retains it for future use.

Miscellaneous Fields

Order Class 1 character. Press F4=Prompt to select from
a list of valid classes.

Sales Program Name 6 characters. Optional.

Shipping information Fields

Ship Code 1 character. Press F4=Prompt to select from

a list of valid shipping codes.
Special Ship to Number 2 characters.

Drop Ship Fields (Available for Fill-in (F) and Drop Ship (U) orders only)

Name 30 characters. The first 2 characters of the
extended name, if any, will appear in the last
2 positions of this field.

Address (1) 30 characters.

City 20 characters.

State 2 characters.

Zip Code 9 characters. This field accepts 5-digit U.S.

zip codes or 9-digit U.S. zip codes without a
space or dash. In addition, it accepts
Canadian postal codes.

Attention 30 characters. Use for the customer’s name
when an order is being picked up at the PDC
(Parts Distribution Center).

## CHAPTER X341-4

STOCK TRANSFER REPORT

### Introduction

This report provides availability information from your other divisions on
parts on an existing Ptiority, stock or special merchandising order.

PRINTING A STOCK TRANSFER REPORT (X3414)

From screen: Type in: Press:
Stock Transfer Vendor Code or ALL
Report Days Supply
Order Number ENTER
(The order number of
the existing priority,
stock, or special

merchandising order.)

## X341-4 STOCK TRANSFER REPORT

 

### Result

The job is placed on the job queue. Press ENTER to return to a menu.

STOCK TRANSFER REPORT ‘VENDOR 9/30/86 PAGE
61 DAYS SUPPLY ORDER # 0627860 13.33.46 x341g-3A
ORDER QUANTITY CAN BE DECREASED EY THE TRANSFER AMOUNT IN THES DIVZSZONS

PRAT NUMBER ORDERED DIVISION TRANSFER ON HAND ON ORDER ESV DEUND JAN FER MAR APR MAY JUN Ub AUG SEP OCT NOV
E75GE9 2 a 2 3 a x 2

 

The fields on the report are described below:

Part Number Identifying part number that can be
transferred from another division instead of
ordered.

Ordered Amount of part on order.

Division Division with the part number.

Transfer Amount of the part possible to transfer from
that division.

On Hand Amount of the part on hand at the division.

On Order Amount of the part on order at that division.

Resv Amount of the part on reservations at the
division.

Demand The demand quantity for the part in each

Jan-Dec month for that division. Check here to see to
seasonal needs.

RELEASE 2.1 LU

## CHAPTER X341-5

REPRINT SUGGESTED STOCK ORDER

### Introduction

The purpose of this option, Reprint Suggested Stock Order, is to allow you to
reprint suggested orders, You will need to know the order number, which can be
determined in Order Inquiry (X34-4).

 

NOTE
The parts history printed on this report is as of the time you run the report, which
"| probably will not be the same as the history used to create the order.

 

### Contents

CREATE STOCK ORDER MENU SCREEN ..........csccssssccssesssessnseesseserseneees 2

ENTRANCE SCREEN
Sample Report.


2 CHAPTER X341-5 ¢ REPRINT SUGGESTED STOCK ORDER RELEASE 2.2

### Create Stock Order Menu Screen

From the Create Stock Order Menu screen, illustrated below, select option 5,
Reprint Suggested Stock Order.

 

‘COMMAND
({c} DIS Corp.

. Create Suggested Stock Order

. Correct Stock Order Or Create Manual Order
. Print/Finalize Order

. Stock Transfer Report

. Reprint Suggested Stock Order

. Return Te Stock Order Menu

Ready for option number or command
see> 5


PARTS INVENTORY CHAPTER X341-5 *« REPRINT SUGGESTED STOCK ORDER 3

### Entrance Screen

Selecting the option leads to the following prompts:

A&R EQUIPMENT SALES Reprint Suggested Stock Order 3415-101
Division: A

Print on order location, class, comments, and weight? (Y/N) ...

 

1. Reply to the prompts, and press [Enter]. A screen for time delay is displayed.
2, Furnish the time you want to print the report, or press [Cmd9] for no delay.


4 CHAPTER X341-5 » REPRINT SUGGESTED STOCK ORDER RELEASE 2.2
SS ESE Eee CELEEAASE €-e

Sample Report
A sample report with location, class, comments, and weight is illustrated below:

A&R EQUIPMENT SALES SUGGESTED STOCK ORDER VENDOR CAS Date 12/18/97 Page i
EXNDER, WA Order # 0001370 ‘pime 10.17.46 ¥3418-52

Sales History Sales order
Fart Number Order Diz Net Current 12 Months / Previous 12 Months To Date Oniand Qty Req Min Eoq Method
Quick Cd Cat Description Qty Extended bee Nov Oct Sep Aug Jul Jun May Apr Mar Feb Jan Prev ¥r Avail Pkg/Hult Max Dice SRA
Location Clg Ext Part Info Weight Extended we

A Lago an 0 $ 5 5 5 a
‘TACHOMETER, 000245 5 8 5
Tad A Comment ~
- 000137R0 § 22
A 11209. ise
Bow 33.88
Comment -
<12i2230a £2
> 000137RO § 22
auzae 40
CUP A/NUT 10180
A” Comment —
- 900137RO $27
uaz 80
Q BAIL
A “Conment -
- 0001370 S21
11213
@ Bom,
sas A” Comment =
- 00013780 S$ 22
10000
@ SAP RING
A Comment -
- 900137RO S 2a

+++ VENDOR TOTALS NUMBER OF LINES: 6 NUMBER OF PIECES: 137
DEALER LIST: 462.34 SUGGESTED LIST: 420.24 INTERNAL,

MUMBER OF PIECES: 137

## CHAPTER X342-1

CORRECT ORDER BEFORE RECEIVING

### Introduction

Sometimes when parts orders arrive at the dealership, there are
discrepancies between what was ordered and what was shipped. If the
inventory was received as ordered, the count would be off. The orders
must be corrected before they are receipted. Orders can be received
directly from this job (see Cmd6-receive order).

If order counts are not corrected before the order is received, corrections
must be made through Parts Posting and Maintenance (X3-2).

In Correct Order Before Receiving, you may also add superseding parts to
your inventory.


[| X342-1 CORRECT ORDER BEFORE RECEIVING a

### How To Run

After passing the security, the following screen displays:

ABC COMPANY CORRECT ORDER BEFORE RECEIVING x3412-102
Division: D

Vendor Code .... MAN
Order Number ... 80010911
Enter ‘C' or 'N'C

“C’ - Change existing Order
oN’ - Create new order

€mdl-Cancel job

 

Enter the vendor code and order number to be corrected. The order already
exists. It is being changed. Use C in the Enter "C” or "N" field. If more
than one price book is loaded on the system, the Select Price Book screen
displays. Select a price book if appropriate. Press Enter.

RELEASE 2.1 LL

## X342-1 CORRECT ORDER BEFORE RECEIVING

The following screen is displayed:

AUSTIN TRACTOR & EQUIPMENT CORRECT ORDER BEFORE RECEIVING x3412-201 1
Division: A Price book: 2.MANEIH MAN S0021113 Lines.. ...
Current mode: SCROLL AND CHANGE LINES Extended amt.

Quick ty Qty A Superses sion
Part Number /Quick Code Code Ordered Revd C Part Number
2 A11208 1 1
2 A11210 1 1
3 allada 1
4 A24314 1

Cmdl-End Cmd2-Scroll/change lines Cmd3-Add lines Cmd4-Random Cmd5-Add new parts
Omd6-Receive ordex Cmd6-Backorder Cmd9-Receipt cost <---Average Costing OPT =

 

The screen displays the part number ordered, the quick code, and the
quantity ordered. The quantity received will match the quantity ordered. If
the quantity received is not the same as the quantity ordered, enter the
number received. Press Field Exit.

If four parts are ordered and three received, one remains unaccounted for.
Decide the disposition of the remaining parts. The column listed in the
center of the screen, A C, is referred to as Action Code. There are three


[ «| X342-1 CORRECT ORDER BEFORE RECEIVING _

valid Action Codes:
Action Codes

B = Back Order. If the part is on back order with the vendor, type B. When
the order is received (X342-2), all parts with a B Action Code will be back
ordered. View all parts on back order by requesting a Back Order Parts
Report (X34-5). Back Order parts will not show on the report until the
order is received (X342-2).

C=Cancel. If you will not be receiving the part, cancel it off the order. To
cancel the part, type C in the Action Code field. When the order is
received, the part will be deleted from the order.

S = Supersession. If you order four parts, receive three of the ordered part (
and one of a part superseding the ordered part, type a S in the Action Code
field.

You must supply the Supersession Part Number and the quantity received.
The part number must be properly segmented. Type a < at the end of each
part segment. If you have questions on part segmentation, see Parts
Posting and Maintenance (X3-2). When this information is entered, the
part will be added to the computer inventory.

Supersession with a Price Book:

If you chose a price book when entering the job that contains the
part number information such as price and description will be
supplied by the price book.

Supersession without a Price Book:

If the price book is not available, proceed to Parts Posting and
Maintenance X3-2. Supply information about the superseding part

RELEASE 2.1 LU


number such as prices and description.

When all the fields are filled in on the screen, press Enter. If you do not
press Enter, no changes made on the screen will register. If a second page

exists, Enter will roll you to the next page. When you are finished with the
job, press Cmd1 to end the job.

Below is a screen with changes made:

ABC COMPANY CORRECT ORDER BEFORE RECEIVING x3412-201
Division: D Price book: MANBOOK © MAN $0010911 Lines
Current mode: SCROLL AND CHANGE LINES Extended Amt..

Quick gry Qty A Supersession
Code Ordered Revd C Part Number
c

### S Sp234<

Cmd1-End Cmd2-scroll and change lines cmd3-add lines
Cmd4-randomly change lines Cmd5-add new parts Cmd6-receive order


[ «| X342-1 CORRECT ORDER BEFORE RECEIVING

### Options

There are seven valid command keys listed at the bottom of the screen.
Cmd2 Scroll and Change Lines

When entering the job, it is as though Cmd2 was pressed. In the upper left
hand corner, the current mode displays: Scroll and Change Lines. Notice
that the Cmd2 key listed at the bottom of the screen says scroll and change
lines.

Cmd3 Add Lines

If you received parts in your computer inventory that are not on the order,
press Cmd3 to add lines. Type the part number you received and the
quantity received. You can add up to 15 parts per screen. Add an Action
Code if appropriate. Press Enter when the parts are added. If you do not
press Enter, additions will not register.

Cmd4 Randomly Change Lines

If there are several pages of order and you only have to make a change to
one of two parts, this is the mode you would use. Type the part number to
be changed. Type the quantity received. Press Field Exit. If the amount
received is less than the amount ordered, type the action code. Press Enter
to register the change. If Enter is not typed, the changes will not register.

RELEASE 2.1 LO


X342-1 CORRECT ORDER BEFORE RECEIVING [7 |

Cmd5 Add Parts

If parts are not in your computer inventory and not on the order, use Cmd5
to add parts. When Cmd5 is pressed, the following screen displays:

ABC COMPANY CORRECT ORDER BEFORE RECEIVING X3412-202
Division: & Price beck: BUSHHCG ADD NEW PARTS

order Qty..:
Vendor: MAN Part number: Description:
Class.: C Quick code.: Loca tion. ..:

Order code: > Return code: Part category: Weight:

Dlr. List Sug. List Internal Dlr. Net
Price...:
Base... .: 3 3 3 3

Minimum: Maximum. : Qty. rad.:

Package: Moltiple: Discount. :

Cmdl-End cmd2-seroll and change lines Cmd3-add lines
(mé4-randomly change lines Cmd5S-add new parts Cmd6-receive order

 

Information is supplied from the default class set up at Configure
Vendor/Class (X38-1). To add the part, type the Part number with
segmentation. A < should be placed at the end of each part segment. For
more information see Parts Posting and Maintenance (X3-2). Press Enter.


| a | X342-1 CORRECT ORDER BEFORE RECEIVING

The following screen will display:

AEC COMPANY CORRECT ORDER BEFORE RECEIVING X3412~202
Division: D Price book: MANEOOK ADD NEW PARTS

order Oty
Vendor: MAN Part number: 43521 Description:
Class.: ¢ Quick code.: Location, ..:

order code: A Return code: Part category: Weight:

Dir. List Sug. List Internal Dir. Net
3 3 3

Maximum, : Qty. rad:
Package: Multiple: Discount. :

DIS-3089 New part number. Add part information and ENTER to update file. (
Cmdi-End md2-scrol2 and change lines cmd}-add lines
Cmd4-randomly change lines cmdé5-add new parts Cmd6-receive order

 

Type the necessary information. A Class, Order code and Bases are
required. Add an Order quantity, Description and pricing information. If a
price book is used, information such as description and pricing will be
provided for you. You may enter or change as much information as you
want. When all the information is typed, press Enter. DO NOT SKIP THIS
STEP. If you do not press Enter, the part is only half added. This will
cause file problems.

When Enter is pressed, the part is added to the order. If the quantity
ordered is not the quantity received, press Cmd2 or Cmd4. Type the
quantity received and action code.

tO


X342-1 CORRECT ORDER BEFORE RECEIVING [*]

Parts Search Window

A Parts Search Window is also available on this screen. To use it, enter a
"2" on either or both sides of a string of characters in the part number field.
The Parts Search Window will display positioning at the beginning of the
string you entered. If you enter a "*" before a string of characters, the parts
search window is displayed with all part numbers that contain the string of
characters following the asterisk. When the correct part number is found
in the window, the user may select it by placing a "1" beside it and the
complete part number will be returned to the part number field. Refer to
Parts Inquiry (X3-1) and Parts Posting and Maitenance (X3-2) for more
information on this feature.

Bearing Interchange

By using a pound sign in the part number field along with any bearing
number (such as #689), you can search for a replacement in the Bearing
Interchange Catalog. Screens are illustrated in CHAPTER X7-9, Bearing
Interchange Menu.


 

Cmd6-Receive Order

When all the corrections have been made, make sure all changes have
registered by pressing Enter on each screen. You are ready to receive the
order,

If you want to receive the order immediately, press Cmd6. The Correct
Order Before Receiv ing entrance screen retums with the following
message at the bottom of the screen:

AUSTIN TRACTOR & EQUIPMENT CORRECT ORDER BEFORE RECEIVING *3412-102 1
Division: A

Vendor Code ....
Order Number ...
Enter 'C' or "N' C

"Ct - Change existing Order
‘MN - Create new order

DIS-0001 Receive request for MAN S0021113 has been placed on the job queue.
Cndi-Cancel job

 

Enter another order number or press Cmd! to cancel the job and return to
the Receive Stock Order Menu.

CU


X342-1 CORRECT ORDER BEFORE RECEIVING [~]

Cmd 8-Backorder

Applies the backorder action code to all parts on the order. Refer to the
action code section above for more information on the backorder code.

Cmd9-Receipt Cost

This command key is displayed only when the Average Costing OPT is
on. It toggles between displaying the quick code and the receipt cost for
the order. The receipt cost is determined when the order is received.

Cmd1-End

When all the corrections have been made, make sure all changes have
registered by pressing Enter on each screen. You are ready to receive the
order. To receive the order immediately, see Cmd6-receive order.

If you don't want to receive the order immediately, press Cmd1 to end the
job. The Correct Order Before Receiving entrance screen returns. Enter
another order for corrections, or press Cmd1 again to cancel the job and
return to the Receive Stock Order menu. You may use option 2, Receive
Stock Order, to receive the order.


Notes: vee

## CHAPTER X342-2

RECEIVE ORDER

### Introduction

After all corrections have been made to the order, the order is received to
update on hand inventory. If the order is received before corrections are
made, corrections to inventory must be made in Parts Posting and
Maintenance (X3-2).

All orders are received through Receive Order. This includes Stock and
Priority Orders.

‘When Receive Order is run, certain reports print:

= Receipt Order Report
= Receipt to Reservations Report

The following two reports are optional:
= Stocking List

= Price Labels
This job uses standard 3 1/2" x 5/16" labels (1 across).


[2] X342-2 RECEIVE ORDER la

### How To Run

After passing the security gate, the following screen is displayed.
LEE'S TRACTOR SALES, INC. Receive Order ‘X3422-101

vendor AAA

Order Number 0912980L

Stocking List (Y/N) WN
Print Price Labels? (y/™) (

Grdi-cancel job

 

Enter the vendor code and order number of the order to be received.

A Stocking List will list the parts received in bin number order. This
makes putting away the parts easier. If you want a Stocking List to print,
change the Stocking List (Y/N) field from N to Y.

Price Labels will print for the items received. You will be prompted to
change forms. If you want price labels to print, change the Print Price

RELEASE 2.2 LO

### X342-2 Receive Order [2]

Labels? (Y/N) field from N to Y. If you are printing price labels, see
Optional Report 4, Price Labels.

Press Enter. The job is placed on the job queue.

Standard Reports

Receive Order Report

This gives you a breakdown of all the inventory received. Below is a
sample report.

EEE'S TRACTOR SALES, INC. Receive Order Report, 09/12/98 = Page
Division: L AAR FORD TRACTOR 3422-28,
orgs 09229801

ain on order Recvd over(-) A nealer Extended
Location Hand avail Qty ary under Cost cost

2 5.04 20.08
2.98
at

Tovals

 

If average costing is installed, the extended cost on the Receive Order
Report will be based on the receipt cost if it is supplied.

Receipt to Reservations

During Point of Sale invoicing, reservations are created for parts and
customers if parts are not in stock. The parts are ordered through


[ «| X342-2 RECEIVE ORDER c

priority Orders. See Priority Orders in the Reference Section of

Point of Sale and Chapter X5-3 PRIORITY ORDERS. When the order
is received, all reservations that can be filled or partially filled are
printed on the Receipt to Reservations Report.

If the reservation was filled, the letter F will display by the Reserve
amount. If the entire reservation was not filled, the Priority Order
section of the Point of Sale Reference Section will explain how to sell a
partially received priority order.

The leftmost column, labeled "F," is the reservation priority fill code.

For more information about how to use this code before a reservation | (
is filled, please see Chapter X342-3, INQUIRE/UPDATE
RESERVATION PRIORITIES.

 

RELEASE 2.2 C


Division:

Parc
adder
T33150
s008s0
apeai3sct
sooese
2309336e1
sogsso
132767602,
800850
1230323¢2
800859
196s97c1
soceso
186599092


¥

Customer Name

oie SHITH

STM SMITH

JIM SHITE

OIM surTH

ane SHITE

ouH surTH

WARRANTY ~ cA!

Fi2sCancel,

## X342-2 RECEIVE ORDER

Receipt To Reservations 9/01/98 Page
GAS CASEIK x3422-3,
ord# eo21098

Description ~ Quantity Document: Date. customer

Cntand Reserve avail Phone & Number Reserved Purchase Ozder  Soldby

BEARING 3

260-838-2972 WWN2363A 1/30/92 COMBINE SPECIAL KC
COLLAR-BRG
360-638-2973 W912363A 1/30/98 COMBINE SPECIAL KC

BAR (cH)

360-838-2973 w712362A 1/30/98 COMBINE SPECIAL KC

ANCLE

260-838-2973 W512363A 1/39/98 COMBINE SPECZAL
BUSHING

360-838-2973 W312363A 1/30/98 COMBINE SPECTAL
BUSHING

360-€38-2973 WI12363A 1/30/98 COMBINE SPECIAL
‘SUPPORT/A
SE 123-656-8011 12395 2/06/98 2188 WARRANTY

FI9<Left  P20sRighe  F24=More keys

 

The report shows all outstanding reservations for parts for both Truck/Van
Inventory and non-van code customers.


 

Optional Reports

Stocking List

If Y was selected to print a stocking, a list of parts received will print in
bin number location.

DEE'S TRACTOR SALES, INC. RECEIVE ORDER - ORDER NO. 0912980L Bate 09/12/98 Paget
Division: 2 STOCKING REPORT FOR AAA - FORD TRACTOR Time 14.54.52 1422-5

PART DESCRIPTION ON HAND RECEIVED RESERVE C/T RESERVE R/O QUICK CODE
APN9158A, kit 4 a

aw BEARING CONE 1 1

ciw cur 1

 

Price Labels
The labels size to order is 3 1/2” x 5/16" (1 across).

If ¥ was selected to Print Labels, the following screen is displayed:

RELEASE 2.2 LU


X342.2 RECEIVE ORDER 7 |

 
   

      

USE'S TRACTOR SALES, inc, RECEIVE ORDER x3422~101

   

 
 

Vendor AAA

  

Order number 09129801,

 
    
    

Stocking list (ym) y

 
 

Print Price Labels 2(y/m)

 

Name to appear on label: ABC COMPANY

 

  
 
 

Number ef labels wide on form (1-4);

Press CHD 1 to cancel job

 
 

Change the following information if it is not correct:
= Name to appear on label:
= Number of labels wide on form (1-4):

Press ENTER when information is Correct. The printing of the Price labels
will be placed on the Job queue. Press ENTER to retum to a menu.


342-2 RECEIVE ORDER co

Il the APPENDIX, for
the Change Forms and Align Forms

 

Ci When the job is ready to print, you are prompted to change forms.
Place the label forms on the printer.
(0 When the forms are loaded, answer the message. The first line of the
Jabel is printed. The first alignment message is generated.
CO Check the alignment of the labels, and answer the message. (
CU When the next print job is selected, the system prompts you to change
forms back to standard. Place the regular paper pack in the machine.
Answer the message.

L

## CHAPTER X342-3

INQUIRE/UPDATE RESERVATION PRIORITIES

### Introduction

Use this job to review or change the order in which reservations will be
filled. Valid priority codes are 1-5 (1 highest, 5 lowest). Priority codes are
printed on the Receipt to Reservations report, which accompanies the
Receive Order job (X342-2).

Standard

The standard procedure is to fill reservations in the order in which they
were made (date/time order). In this case, all reservations are assigned a
priority code of "1," which can be changed before parts are received.

Reservation Priority OPT Switch

An OPT switch, Reservation Priority, allows you to fill customers’
reservations first. With this switch, the system assigns the following
priority codes automatically:

Code Reservation
2 Customer
3 Warranty
4 Internal

When you choose this option, customers’ reservations are filled first (in
date/time order). If you want to further specify the order in which
particular reservations should be filled, use this job.


X342-3 INQUIRE/UPDATE RESERVATION PRIORITIES

### How To Run

From Menu X342 select option 3 to view or update reservation priorities.
The Parts security gate appears, followed by the Inquire/Update
Reservation Priorities screen, which is illustrated below.

AUSTIN EQUIPMENT CO Inquire/Update Reservation Priorities

Division: A

Ven Part
50908
70091
70091
70316
70316
71466
71466
73183
73153
73153

vendor

Date
C1 5/16/91
5/16/91
5/21/92
5/16/93
5/20/92
5/16/91
5/22/91
1/86/05
5/16/91
5/21/91

Partt

Addr®
CURROL
CURROL
BURKOL
FTO888
Fr0888
‘CURROL
BURKO1
ADAMOL
CURROL
BURKOL

Invoice Name
ROOOL02 CARL CURRY
ROO0102 CARL CURRY
RO00107 LAURA P BURKIN
RO00103 ¢642972
ROOOLOZA C642972
ROOOL02 CARL CURRY
ROO0107 LAURA P BURKIN
1v00025A WILLIAM ADAMS
RO00102 CARL CURRY
RO00107 LAURA P BURKIN

to begin next screen

Enter-Update priority Cmdl-fnd job

x3423-102

 

NL


X342-3 INQUIRE/UPDATE RESERVATION PRIORITIES

 

As you change priority codes, press [Enter] to record your changes.

To go to the next screen of reservations, press [Enter].

O To begin the next screen at a particular vendor or part number, use the
line at the bottom of the screen.

When you have made all of your changes, press [Cmd1] to end the job.

 

 

 

 

 

 

 

The fields on the Inquire/Update Reservation Priorities screen are
described on the next page.

_ Leftmost position is 1 digit (unlabeled),
which is the reservation priority fill code.
Valid codes are 1-5 (1 high).

Ven 3-character vendor code.

Part Part number.

Date Date of reservation.

Addr# 6-character address number of the customer
or stock number of the unit (internal work
order).

Invoice Document number of the invoice or work
order.

Name Customer's name or unit's serial num ber.

Qty Quantity of parts reserved.

P Priority order code:

Code: Description:

Pors The part is on a priority or
stock order.

pors The priority/stock order has
been finalized.

a The part has been received.


Notes:

## CHAPTER X342-4

UNCLAIMED PART RECEIPTS REPORT

### Introduction

Print the Unclaimed Part Receipts Report to see a list of Parts that have
been reserved, ordered, and Teceived, but not yet claimed: parts on open
Point of Sale documents where the priority code has changed to "a",

REMINDER: Priority codes "P" and "S" change to “p" and "s" when parts
are ordered, to "a" when the parts are received. For more information
about priority codes, see CHAPTER X5-3, PRIORITY ORDERS.


X342-4 UNCLAIMED PART RECEIPTS REPORT (

 

### How To Run

(X34-2), select option 4, Unclaimed Part

From the Receive Order Menu
Parts security gate, the selection screen

Receipts Report. Following the
appears, as illustrated below:

x34241-01

Unclaimed Part Receipts Report

A & R SALES & LEASING
Division: A

vendor (Or ALL)

(mdi-End Job

 

CO Make your selection and press [Enter] to place the report on the job

queue.

RELEASE 2.1 Lo.

## X342-4 UNCLAIMED PART RECEIPTS REPORT

 

An example of an Unclaimed Part Receipts Report follows:

    
 
 
   

    
     
   
     
      
        
   
  
  
   

   
 

A & R SALES & LEASING Uncleined Part Receip:s Report pate 4/22/92 Page 1
Division: a Vendor :Auh Moe 8.53.37 x342¢2-01
Address # customer Name Phone Phone #2
vate
Eevoiced opened —P. 0. Vendor/parct Descziption Bin 1m oaty. Price etal
ADAMO] WILLIAM ADAMS 206-212-7364 206-212-7388
rvoucasa syo1/92 cas 12824 SPACER 7e85 3 26.29 70.87
Tvoo0z5a 5/01/92 cas 49036 cuAMP BOARD 2 3.07 3.07
tvoo02sa 5/01/92 cas 73153 BRC 5F63 2 7.96 7.96
Customer Totals ; 5 89.90

 

. PARTS


Notes: {(-

Lo

## CHAPTER X527-1

TAX CODE MAINTENANCE

### Introduction

Use this option to add, change, and delete tax codes, view the history of changes
to tax codes and print a list of all current tax codes. If you plan to use Tax Types,
set them up in Tax Type Maintenance (X527-2) first.

 

NOTE
Only one person can use Tax Code Maintenance at the same time.

 

 

### Contents

 

X5271.doc 7/29/99 J


2 X527-1 « TAX CODE MAINTENANCE
ENTRANCE SCREEN

1. From the Point of Sale Menu (X5), select option 2, Table Maintenance Menu.
2. Select option 7, Tax Configuration Menu.
3. Select option 1, Tax Code Maintenance. The current tax codes are listed.

NW EQUIPMEN’

Tax Code

2=change
Tax Ti

Opt Code Tf:
aA

AL

Alo
All
Al2
Al3
Ald
ALS
ALG
Al?
Ale
A1g
a2

F3"Exit

 

'T SALES, INC.

Tax Code Maintenance

Description

4=Delete History

ax Sales

ype Code Rate
06875
04625
06625
06625
06625
06625
- 06875
- 06875
06875
+ 06875
07228
07125
05625

Description

ARK
ARK
ARK
ARK
ARK
ARK
ARK
ARK
ARK
ARK
ARK
ARK

F5=Refresh F6rAdd

STATE SALES TAX
TX-CITY 2%
TX-CO 18-CITY 1%
TX-CO 0.5%-CITY
TX-CO 2%

TX-CO 0.25%-CITY
TX-CO 2%-CITY 0.
TX-CITY 2.253
TX-CO 1.5%-CITY
TX-CO 18-CITY 2.
@X-CO 1.5%-CITY
EX-CITY 16

F9=Print Rpt

Changed by
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA
VIRGINIA

Roll

Date Chgd
4/15/1999
4/08/1999
4/08/1999
4/08/1999
4/08/1999
4/08/1999
4/08/1999
4708/1999
4/08/1999
4/08/1999
4/08/1999
4/08/1999
4/08/1999

 

X52711

Time Chg
15:22:32
12:22:04
12:41:17
12:45:56
12:47:18
12:48:52
12:50:10
12:51:17
12:52:11
12:53:35
12:55:04
13:45:35
12:25:49

More...


POINT OF SALE X527-1 « TAX CODE MAINTENANCE 3

 

### Adding A New Tax Code

To add a new tax code, press F6=Add on the Entrance screen. The Add Tax Code
Info screen is displayed.
NW EQUIPMENT SALES, INC. Tax Code Maintenance XS2711
Add Tax Code Info
_— Tax Type: _ SC: __ Desc:
Base OverLimit Limit

Rate G/L Acct Limit Rate Type(D/L) - Changed -
State :

4/08/1999
County: _ 12:25:49

City
Dist

Other :

Total Effective Date: WARNING!
Decimals are used on
this screen. Enter 7% as
-07000. Enter $500 as
F3sExit  F5=Refresh F6=Add F9=Print Rpt Roll 500.00.

F4=Prompt. F12=Previous

 

Furnish the information and press [Enter]. You will return to the Entrance screen.
Press F5=Refresh to see the entire list of codes.

G/L Account Defaults

If you press F6=Add and you have not changed or added a tax code during the
current session, the screen will be blank as illustrated above. However, if you
have already changed or added a tax code, the same G/L accounts will be used as
defaults. In other words, as long as you are in Tax Code Maintenance, the system
uses the G/L accounts from the tax code you worked on most recently.

### Fields & Descriptions

Top Line

Tax Code Required. 3-characters.

Tax Type Optional. 1-character. User-defined code set up in Tax
Type Maintenance (X527-2). To select from the list of
current tax codes, place the cursor in this field and press
F4=Prompt.

sc Optional. 2-character sales code set up in Sales Code

Maintenance (X52-3). To select from the list of current


4 X527-1 » TAX CODE MAINTENANCE RELEASE 2.3

 

sales codes, place the cursor in this field and press (
F4=Prompt.
Desc Optional. 30 character description of the tax code. The
Sales Tax Report can be selected by description; therefore,
you may want to establish standards for this field.

Tax Group Information

Base Rate Required. The rate that is applied first. Enter 7% as .07000.

G/L Acct Required, The general ledger account used to accrue the
tax.

Limit Optional. Dollar limit, if any, the base rate is applied to.

Two decimals are assumed. Enter $500 as 500.00.

OverLimit Rate Rate, ifany, that is applied to the dollar amount that is over
the limit. Enter 7% as .07000.

Limit Type (D/L) | D=Document. The limit applies to all lines on the
document. L=Line. The limit applies to each line. This field
is required only if the limit is not zero.

Changed No input. System generated. ID of the person who changed
the tax code most recently. If the rate is changed through
Tax Code Rate Change (X527-7), the ID of the person who
ran the job is applied to each tax code, and 2 asterisks (**)
are displayed in the last 2 positions of the Changed field.

Total No input. System generated.Total tax rate for the current (
code,
Effective Date Optional. Date (mm/dd/yy). Date on which the tax code is

effective. If the current date is before the effective date, the
system looks for the same tax code in the history file,
which tracks changes to tax codes. If the same tax code is
not found in history, the current tax code will be used
tegardless of the effective date.


POINT OF SALE X527-1 « TAX CODE MAINTENANCE

### Changing A Tax Code

To change an existing tax code, select it with 2=Change on the Entrance screen.
The Change Tax Code Info screen is displayed.
NW EQUIPMENT SALES, INC. Tax Code Maintenance B52711
Change Tax Code Info
Tax Code: AlS Tax Type: sc: Desc: ARK TX-CO 2%-CITY 0.25%
Base OverLimit Limit
Rate G/L Acct Limit Rate Type(D/L) - Changed =
State : +04625 M22410 VIRGINIA
4/08/1999
County: ~02000 M22410 2500.00 42:51:17
City : 00250 M22410 2500.00

Dist

Other :
Total -06875 Effective Date:

F4=Prompt F12=Previous

F3=Exit FS=Refresh F6=Add F9=Print Rpt Roll

1. Type over any information you want to change. See Fields & Definitions on
page 3.

2. Press [Enter] to record the change. You will return to the Entrance screen.

3. Press F5=Refresh to see the entire list of codes.


 

 

NOTE
If there are closed, not posted documents that include the tax code you are trying
to change, you will receive this message when you retum to the Entrance screen:

DIS-9073 Code not changed - Closed/Not Posted documents exist.
(F9 for list)

Press [F9] to print a list of the closed, not posted documents.


é X527-1 » TAX CODE MAINTENANCE RELEASE 2.3

 

### Deleting A Tax Code

To delete a tax code, select it with 4=Delete on the Entrance screen. A
confirmation window pops up, as illustrated below.

NW EQUIPMENT SALES, INC. Tax Code Maintenance xS2711

Tax Code Description

2=Change 4=Delete #=History
Tax Tax Sales

 

Opt Code Type Code Rate Description Changed by Date Chgd Time chg
A 06875 VIRGINIA = 4/35/1999 15:22:32
Al
ALO : Delete Tax Code Info
All Confirm Delete
Al2
Al3
Ald . Tax Code .

ALS : Tax Type .
Al6 . Sales Code
aly . Description . ARK TX-CO 1.58-CITY 18
alg
4 alg
a2 . Press ENTER to Delete F12=Cancel

 

F3-Exit FS5=Refresh F6=Add F9=Print Rpt Roll

 

 

 

1. To cancel the request, press F12=Cancel.
2. To delete the code, press [Enter].

 

NOTE
If there are closed, not posted documents that include the tax code you are trying
to delete, you will receive this message when you return to the Entrance screen:

DIS-9074 Code not deleted - Closed/Not Posted documents exist.
(F9 for list)

 

 

Press [F9] to print a list of the closed, not posted documents.


POINT OF SALE X527-1 « TAX CODE MAINTENANCE


 

### Viewing Tax Code History

The system keeps history on all tax codes. To see the history of a tax code, select
it with H=History on the Entrance screen.

NW EQUIPMENT SALES, INC. Tax Code History XS2712

Tax Code
Als

l=Show Details
Tax Tax Sales

Opt Code Type Code Rate Description Changed by Date Chgd Time Chg
ALo +07125 ARK TX-CO 1.58-CITY VIRGINIA 19/99/0408 13:45:35

F3-Exit F5-Refresh F6=Add F9=Print Rpt Roll

To see the details, select the code with 1=Show Details.

NW EQUIPMENT SALES, INC. Tax Code History x52712
Display Tax Code Detail
Tax Code: Al9 Tax Type: sc: Desc: ARK TX-CO 1,.5$-CITY 1%

Base OverLimit Limit
Rate G/L Acct Limit Rate Type (D/L) - Changed -
State : .04625 M22410 VIRGINIA
49/99/0408
County: 01500 M22410 2500.00 13:45:35

city : 01000 M22410 2500.00

Dist

Other :
Total .07125 Effective Date:

Pl2=Previous

F3sExit Roll


8 X527-1 « TAX CODE MAINTENANCE RELEASE 2.3

### Printing A List Of Tax Codes

To print a list of all current tax codes, press F9=Print Rpt on the Entrance screen.
The Tax Code List Selection screen is displayed.

NW EQUIPMENT SALES, INC. TAX CODE LIST %52712
Division: A Selection

Sort by D(Description} or T(Tax Code) _

Starting value . . :
Ending value... :

cmdl-Cancel

 

1, Ifyou want the report to be sorted by description, enter D at the “Sort by”
prompt and furnish the starting and ending values for the description.

2. Ifyou prefer to have the report sorted by tax code, enter T at the “Sort by”
prompt, and furnish the starting and ending tax codes.

3. To cancel the request, press Cmd1-Cancel; otherwise, press [Enter] to print
the report.

A sample report, sorted by tax code, is illustrated below.


X527-1 « TAX CODE MAINTENANCE

 

Sample Sales Tax Table —

NW EQUIPMENT SALES, INC.
ABBOTSFORD, BC z

Starting value: A
Tax Tax Sales Total
Code Type code Rate Description
B 6.875
BaseRate GL Accounr Limit
6.875 M22435 0

ARK STATE SALES TAX ONLY
BaseRate GL Account Limit
4.625 wz2420 a

ARK TX-CITY 22
BaseRate GL Account Limit
4.625 MZ2410 0
2.000 Mzzsi0 2800

ARK TK-CO Le-c7TY 12
BaseRate Gi Account Limit
4.625 w22ai0 3
1,000 22410 2500
1/000 22410 2500

ARK TX-CO 0.5%-CITY 1.5%
BaseRate GL Account Limit
4.625 22610 °
+500 622410 2500
1.500 22410 2500

ARK TX-CO 2%
BaseRate GL Account Limit
4.625 22410 0
2,000 22410 2800

ARK TX-CO 0.252%-cITy 2%
BaseRate GL Account Limit
4.625 22410 0
+250 22410 2500
2.000 22420 2500

ARK TX-co 25-cITY 0.25%
BaseRate GL Account Limit
4.625 M2z410 °
2.000 22410 2500
+250 22410 2500

ARC TK-CITY 2.253
BaseRate GL Account Limit
4.625 422410 9
2.250 22410 2500

ARK TX-cO 1,5%-cITY 6,752,
BaseRate GL account Limit
4.625 22410 °
3.509 H22410 200
1750 M22e10 2500

ARK TX-CO La-CITY 1.52

By Tax Code

Sales Tax Table Date 6/04/99
Report by: TAX cous Time 18:09:41

Ending value: 222
pate Time Dace
Changed By Changed Changed Effective
VIRGINIA 6/25/1999 15.22.32
OverRate Limtype
000

VIRGINIA 4/09/1999
OverRate LimType
090

VIRGINIA 4/08/1999 12.41.17
OverRate LimType

+000

:000 «BC DOCUMENT

VIRGINIA 4/08/1998 12.45.56
OverRate LimType
+000
1000 =D (OcMENT
-009 =D DOCUMENT

VIRGINIA 4/08/1999 12.47.18
Overkate LinType
900
1000 =D (DOCUMENT
+000 DOCUMENT

VIRGINIA 4/08/1999 12.48.$2.
OverRate Lintype

+900

9000) Documenr

VIRGINIA 4/08/1999 12.30.10
OverRate LinType
090
1000 BS DocuMENT.
+900 B Document

VIRGINIA 4/08/1999 32.51.17
OverRate LimType
000
+000 DOCUMENT
7000 = (DOCUMENT:

VIRGINIA 4/08/1999 12.82.11
OverRate LirType

+000

3000 BD DOCUMENT

VIRGINIA 4/08/1999 12.53.35
OverRate Lintype
+000
-000 =D (DOcuMENT.
7000 8B DOCOMENT.

VIRGINIA 4/08/1399 12.55.04

Page 1
X52713-01

## CHAPTER X527-2

TAX TYPE MAINTENANCE

### Introduction

Tax authorities have different rates for different type customers within same
geographic area. Because of this need, the tax rate can be determined by using a
combination of tax code, sales code and the customer’s tax type. Tax type is a 1-
character, user-defined code. A blank tax type is furnished by the system and
automatically assigned until it is replaced by a user-defined tax type. Tax types
are optional.

Use this option to add, change, delete, and print a list of all current tax types .
Charge customers can be identified with a tax type in Receivables Maintenance
(X11-2), cash customers in Address Maintenance (X4-2).

### Contents

ENTRANCE SCREEN .....cscsscssscssssssssessssssessessstnucossosenesatsenentsaesnesvesessversesne 2
ADDING A TAX TYPE....csssessssserensnseee sonsssentsnsoeoneneneceensontersusnsoesneneateeraneas 3
CHANGING A TAX TYPE........ccsssssssessssssnessssssacsnssnsssssnsansassaseasenseaseeesernes 4
DELETING A TAX TYPE.........scssssssssssscrnssssesessnsoesusnsssessanenssseesnsnessesseneense 5
PRINTING A LIST OF TAX TYPES. ..cscsssscussssssssessssneseesersesesersersensenaesantee 6

X5272.doc 7/29/99 1


2 X527-2 « TAX TYPE MAINTENANCE RELEASE 2.3

 

ENTRANCE SCREEN

1. From the Point of Sale Menu (X5), select option 2, Table Maintenance Menu.
2. Select option 7, Tax Configuration Menu.
3. Select option 2, Tax Type Maintenance. The current tax types are listed.

NW EQUIPMENT SALES, INC. Tax Type Maintenance X52721

Tax Type

2=Change 4=Delete

Opt Tax Type Description Changed by Date Chgd
EXEMPT ROBMC 11/04/1998
FEDERAL GOVERNMENT ROBMC 11/04/1998
GOVERNMENT ~ OTHER THAN FED ROBMC 11/04/1998
OUT OF STATE ROBMC 11/04/1993
FOR RESALE ROBMC. 12/04/1998
SC STATE SALES TAX EBS 6/03/1999
NATIVE AMERICAN BARB 4/26/1999
AGRICULTURAL ROBMC 11/04/1998

F5=Refresh F6=Add F9=Print Rpt Roll


POINT OF SALE X527-2 ¢ TAX TYPE MAINTENANCE 3

### Adding A Tax Type

To add a tax type, press Fé=Add on the Entrance screen. The Add Tax Type Info
window is displayed.

NW EQUIPMENT SALES, INC. Tax Type Maintenance XS2721

Add Tax Type Info

Tax Type Description

Fi2=Previous

 

F3sExit F5=Refresh F6=Add F9=Print Rpt Roll

 

 

1. Enter a 1-character tax type code and its description (up to 30 characters).
2. Press [Enter] to record the code. You will return to the Entrance screen.
3. Press F5=Refresh to see the entire list of codes.


4 X527-2 © TAX TYPE MAINTENANCE RELEASE 2.3

 

### Changing A Tax Type

To change a tax type, select it with 2=Change on the Entrance screen. The Change
Tax Type Info screen is displayed.

NW EQUIPMENT SALES, INC. Tax Type Maintenance X52722

Change Tax Type Info

Tax Type Descriptien
E EXEMPT

F12=Previous

 

F3-Exit FS=Refresh F6=Add F9=Print Rpt Roli

1. Type over any information you want to change.
2. Press [Enter] to record the change. You will return to the Entrance screen.
3. Press F5=Refresh to see the entire list of codes.

 

”)


POINT OF SALE X527-2 « TAX TYPE MAINTENANCE 5

 

### Deleting A Tax Type

To delete a tax type, select it with 4=Delete on the Entrance screen. A
confirmation window pops up, as illustrated below.

NW EQUIPMENT SALES, INC. Tax Type Maintenance 52721
Tax Type

2=Change 4=Delete

 

Opt Tax Type Description Changed by Date Chgd
E EXEMPT EBS 6/07/1998
F FEDER
G GOVER Delete Tax Type Info
° ouT Oo Confirm Delete
R FOR R
4 s Sc ST
1 NATIV Tax Type .. §
2 AGRIC Description . §C STATE SALES TAX
Fl2=Cancel

 

F3sExit  FS=Refresh F6=Add F9=Print Rpt Rell

 

1. To cancel the request, press F12=Cancel.
2. To delete the code, press [Enter].


6 X527-2 © TAX TYPE MAINTENANCE RELEASE 2.3

PRINTING A LIST OF TAX TYPES

1. To print a list of all current tax types, press F9=Print Rpt on the Entrance
screen. The job will be placed on the job queue.

2. Press [Enter] to return to the Tax Type Maintenance screen. A sample report
is illustrated below.

NW EQUIEMENT SALES, INC. Tax Type Listing Date 6/04/99 Page 1
BELLINGHAM, WA A Time 14.38.47 %52780-01

Tax Type Deseription Changed By Date

ROBNC 2/12/1939
EXEMPT 31/04/1998
FEDERAL GOVERNMENT 11/04/1998
GOVERNMENT OTHER THAN FED 21/04/1998
ov? oF STATE 21/94/1998
FOR RESALE 11/04/1398
3¢ STATE SALES TAX 6/03/1399
NATIVE AMERICAN 4/26/2999
AGRICULTURAL 41/04/2996


POINT OF SALE X527-2 » TAX TYPE MAINTENANCE 7

Notes:

## CHAPTER X527-3

TAX RULE MAINTENANCE

### Introduction

Use this option to establish the tax rules by which tax codes will be determined at

Point of Sale, Because it matters where the item is delivered to the customer, the

Ship To address is used if it is present; otherwise, the system assumes the

customer is taking possession of the item at the dealership and uses the zip or

postal code of the selling division. Here’s how a tax code is selected:

1. Ifthe customer’s tax rate (in X11-2) is zero, use zero.

2. Use the rate associated with the Ship To address (from Multiple Ship To
addresses), if any.

3. Use the rate associated with the Ship To address entered on the Sold To

screen, if any.

Use the rate associated with the selling division’s zip code in Tax Rule

Maintenance, if it is present there.

5. Use the tax code associated with the customer’s record (X11-2) unless it is
overridden by a tax code on a standard line or from Price Table Maintenance
(X52-9).

 

Use this option to identify the tax codes that apply within certain zip/postal codes,
change and delete rules, and to the list of all current rules. You can furnish the
county if you’re interested in printing the Sales Tax Report by County/State (X16-
4). An optional user-defined field is available to record the code used by your tax

 

Teporting form.

### Contents

ENTRANCE SCREEN .w.sssssssssssssesssesssserssessesssesessssesnssaeensesnarsesaseesersnseseess 2
ADDING A TAX RULE..
CHANGING A TAX RULE .......sssssssssessssessssnsseatssreeseesnssnssorsenesseeneesneeaeensens 4
DELETING A TAX RULE.........c.sssssssssessessesesssessessestecseseessseasentensesesssesatees 5
PRINTING A LIST OF TAX RULES .....ccssssssssssesserseesnnssetsessneesesensenansenesens 6

X5273.doc 7/29/99 1


2 X527-3 e TAX RULE MAINTENANCE RELEASE 2.3

 

ENTRANCE SCREEN

1. From the Point of Sale Menu (X5), select option 2, Table Maintenance Menu.
2. Select option 7, Tax Configuration Menu.
3. Select option 3, Tax Rule Maintenance. The current tax rules are listed.

NW EQUIPMENT SALES Tax Rule Maintenance X52731
Zip/Postal Code

2=Change 4=Delete
Opt Starting Ending Tax County Rpt Code Changed by / Date
38302 T2 MADISON VIRGINIA 4/14/1999
38302 12 MADISON VIRGINIA 4/14/1999
38303 T2 MADISON VIRGINIA 4/14/1999
38305 72 MADISON VIRGINIA 4/14/1999
38308 12 MADISON VIRGINIA 4/14/1999
38313 MADISON VIRGINIA 4/14/1999
38314 T2 MADISON VIRGINIA 4/14/1999
38356 MADISON VIRGINIA 4/14/1999
38362 MADISON VIRGINIA 4/14/1999
38366 MADISON VIRGINIA 4/14/1999
38378 MADISON VIRGINIA 4/14/1999
38391 MADISON VIRGINIA 4/14/1999
38392 MADISON VIRGINIA 4/14/1999
More...

F3sExit F5=Refresh F6=Add F9-Print Rpt Roll

 

 

 

Note
If you want to use tax rules that apply at the selling division’s location, make sure
you enter each division’s zip or postal code in the Tax Rule Table with the correct
tax code for that location.


POINT OF SALE X527-3 ¢ TAX RULE MAINTENANCE 3

 

### Adding A Tax Rule

To add a tax rule, press F6=Add on the Entrance screen. The Add Tax Rule Info
window is displayed.

  

Canadian Postal
Codes must be
entered with or
without a space
exactly like they
entered in
Receivables
Maintenance, su

  
    
    
  

V4Ww2H8.

as V4W 2H8 or .

   

    

Nw EQUIPMENT SALES

 

   

Tax Rule Maintenance X$2731

  
 

Add Tax Rule Info

 
    
  
    
         

Zip/Postal Code Range

    

Starting Ending

 

Tax code County


   

 

 
     
      
 
  
 

Furnish the County

Press F4=Prompt in the for the Sales Tax by
“Tax code” field to select County/State Report
from the list of valid tax {X16-4).

are codes.

 

 
   

    
 
  

   

ich

  

F4=Prompt F12=Previous

 

   
      

        

it,

 

F5-Refresh FésAdd FQ=Print Rpt Roll

   

Enter the information. See Fields & Descriptions below.
Press [Enter] to record the code. You will return to the Entrance screen.
Press F5=Reftesh to see the entire list of codes.

1.
2.
3.

### Fields & Descriptions

Starting 9 characters. Required. Beginning Zip/Postal code.
Canadian Postal Codes must be entered with or without a
space exactly like they are entered in Receivables
Maintenance, such as V4W 2H8 or V4W2H8.

Ending 9 characters. Optional. Ending Zip/Postal code.

Tax code 3 characters. Required. Press F4=Prompt to select from a
list of valid tax codes. Tax codes are set up in Tax Code
Maintenance (X527-1).

County 20 characters. Optional. If you want to print the Sales Tax
Report by County/State (X16-4) and have it sorted by
County, make sure each county is associated with a zip
code range; otherwise, all cities will be reported under a
blank county within each state.


4 X527-3 ¢ TAX RULE MAINTENANCE RELEASE 2.3

 

Rpt code 8 characters. Optional code from your tax reporting form. C

### Changing A Tax Rule

To change a tax rule, select it with 2=Change on the Entrance screen. The Change
Tax Rule Info screen is displayed.
NW EQUIPMENT SALES Tax Rule Maintenance x52731
Change Tax Rule info
Zip/Bostal Code Range

Starting Ending Tax code County Rpt code
38313 12 MADISON

F4=Tax Codes F12=Previous

F3-Exit FS-Refresh F6=Add F9=Print Rpt Roll

 

1. Type over any information you want to change.
2. Press [Enter] to record the change. You will return to the Entrance screen.
3. Press F5=Refzesh to see the entire list of codes.


POINT OF SALE X527-3 * TAX RULE MAINTENANCE 5

### Deleting A Tax Rule

To delete a tax type, select it with 4=Delete on the Entrance screen. A
confirmation window pops up, as illustrated below.

NW EQUIPMENT SALES Tax Rule Maintenance X52731

Zip/Postal Code

2=Change 4=Delete

Opt Starting Ending Tax County Rpt Code Changed by / Date
71601 All JEFFERSON 35-01 «VIRGINIA 4/14/1999
71602 :
71603 Delete Tax Rule Info :
71631 Confirm Delete
71613
71630
71631 Starting
71634 Ending .
71635 Tax Code
71638 County
71639 Rpt Code
71640
71642 F12=Cancel

 

 

F3=Exit F5=Refresh

 

1. To cancel the request, press F12=Cancel.
2. To delete the code, press [Enter]. :


6 X527-3 © TAX RULE MAINTENANCE RELEASE 2.3

### Printing A List Of Tax Rules

To print a list of all current tax rules, press F9=Print Rpt on the Entrance screen.
The Tax Code List Selection screen is displayed.

NW EQUIPMENT SALES TAX RULE LIST X52732
Division: A Selection

Sort by C(County), P(Zip/Postal), R(Rpt Code), or T(Tax Code)

Starting value. .:
Ending value. .:

 

Cmd1-Cancei

Select the sort option.

Fumish the starting (optional) and ending (required) values.

Press [Enter]. The job will be placed on the job queue.

Press [Enter] to return to the Tax Rule Maintenance screen. A sample report,
sorted by postal code, is illustrated on the next page.

RYN


POINT OF SALE X527-3 « TAX RULE MAINTENANCE 7

 

Sample Sales Tax Table — By Postal Code

Na EQUIPMENT SALES Tax Rule List Date 6/04/99 Page 2
‘BELLINGHAM, WA Report by: POSTAL CODE Time 14.40.52  x$2760-02

Starting value: 90000 Ending valve: 99999

Code-start Code-fnd Tax Code county Changed by / Date
38301 72 MADISON VIRGINIA 4/14/1999
38302 12 MADISON VIRGINIA 4/14/1959
38303 12 MADISON VIRGINIA 4/14/1999
30308 12 ‘MADISON VIRGINIA 4/14/1993
38308 12 YADISOK VIRGINIA 4/24/1999
30223 12 MADISON VIRGINIA 4/14/1999
30324 12 MADISON VIRGINIA 4/14/2999
30356 12 MADISON VIRGINIA 4/14/1999
38362 12 MADISON VIRGINIA 4/14/1899
33366 12 waDIsoN VIRGINIA 4/14/1999
38378 72 MADISCH VIRGINIA 4/14/1998
33391 72 MADISON VIRGINIA 4/14/1999
38392 72 MADISON VIRGINIA. 4/14/1398
33801 M2 EE TABATHA 4/14/1399
38802 M2 LEE VIRGINIA 4/14/1399
38803 M2 LEE VIRGINIA 4/14/1999
38804 Me LEE VIRGINIA ¢/20/1999
71601 All JEFFERSON VIRGINIA 4/14/1999
n1602 AlL JEFFERSON VIRGINIA 4/14/1999
71603 All JEFFERSON VIRGINIA 4/14/1999
neat All JEFFERSON VIRGINIA 4/14/1999
71613, All JEFFERSON VIRGINIA 4/14/1999
71630 A31  DESHA VIRGINIA 4/24/3899
71631 A31 BRADLEY. VIRGINIA 5/03/1599
73634 Al3 DREW VIRGINIA 4/14/1939
71635 AZ6 0 ASHLEY. VIRGINIA 4/14/1999
nese 30 © CHICOT VIRGINIA 4/14/1999
Ties R27 ESHA, VIRGINIA 4/14/1989
71640 424 CHICOT VIRGINIA 4/14/1999
Tew 4260 ASHLEY VIRGINA 4/14/1999,
71633 LINCOLN VIRGINIA 4/14/1999
nese LINCOLN VIRGINIA 4/14/1989
7646 A260 ASHLEY VIRGINIA 4/14/1999
71647 BRADLEY VIRGINIA 5/03/1999
ness a3 cHICOT VIRGINIA 4/14/1999
71650 DREW VIRGINIA 4/14/1999
71651 Aj] BRADLEY VIRGINIA 5/03/1999
71652 aa CLEVELAND VIRGINIA 4/34/1999
71653 A260 CHICOT VIRGINIA 4/24/1989
71654 DESRA VIRGINIA 4/24/1939
71655 DREW VIRGINIA 4/24/1999
71656 DREW VIRGINIA 4/14/1999
nese ASHLEY VIRGINIA 4/14/1999
71659 SEEFERSON VIRGINIA 4/14/1999
73660 CLEVELAND VIRGINIA 4/14/1999
71661 ASHLEY VIRGINIA 4/14/2999
mesa DESEA VIRGINIA 4/14/1999
71663 ASHLEY VIRGINIA 4/14/1999
71665 CLEVELAND VIRGINIA 4/14/1989
71866 DESRA VIRGINIA 4/14/1999
71687 LINCOLN TABATHA 5/27/1989
71670 DESHA, VIRGINIA 4/14/1999
71673 BRADLEY VIRGINIA 5/03/1993


X527-3 » TAX RULE MAINTENANCE

Notes:

## CHAPTER X527-3

TAX RULE MAINTENANCE

### Introduction

Use this option to establish the tax rules by which tax codes will be determined at
Point of Sale. Because it matters where the item is delivered to the customer, the
Ship To address is used if it is present; otherwise, the system assumes the
customer is taking possession of the item at the dealership and uses the zip or
postal code of the selling division. Here’s how a tax code is selected:
1. Ifthe customer’s tax rate (in X11-2) is zero, use zero.
2. Use the rate associated with the Ship To address (from Multiple Ship To
addresses), if any.
3. Use the rate associated with the Ship To address entered on the Sold To
. screen, if any.
Use the rate associated with the selling division’s zip code in Tax Rule
Maintenance, if it is present there.
5. Use the tax code associated with the customer’s record (X11-2) unless it is
overridden by a tax code on a standard line or from Price Table Maintenance

(X52-9).

 

Use this option to identify the tax codes that apply within certain zip/postal codes,
change and delete rules, and to the list of all current rules. You can furnish the
county if you’re interested in printing the Sales Tax Report by County/State (X16-
4). An optional user-defined field is available to record the code used by your tax
reporting form.

### Contents

ENTRANCE SCREEN...

 

ADDING A TAX RULE........c.secsssesussessseesssensasseesserssesermtensverstssersnnearenentoees 3
CHANGING A TAX RULE ...cscsessstssessscssssanssssnsssersnenesatecsnensnneatieecsavenenssens 4
DELETING A TAX RULE.

 

PRINTING A LIST OF TAX RULES .....sscsssusssssssssssssstossassssoenersensosssareeesess 6


2 X527-3 « TAX RULE MAINTENANCE RELEASE 2.3

 

 

ENTRANCE SCREEN

1, From the Point of Sale Menu (X5), select option 2, Table Maintenance Menu.
2. Select option 7, Tax Configuration Menu.
3. Select option 3, Tax Rule Maintenance. The current tax mules are listed.

NW EQUIPMENT SALES Tax Rule Maintenance X52731
Zip/Postal Code

2=Change 4=Delete

Opt Starting Ending Tax County Rpt Code Changed by / Date
— 38301 12 MADISON VIRGINIA 4/14/1999
_ 38302 12 MADISON VIRGINIA 4/14/1999
_ 38303 72 MADISON VIRGINIA 4/14/1999
_ 38305 72 MADISON VIRGINIA 4/14/1999
_ 38308 12 MADISON VIRGINIA 4/14/1999
_ 38313 72 MADISON VIRGINIA 4/14/1999
_ 38314 T2 MADISON VIRGINIA 4/14/1999
_ 38356 T2 MADISON VIRGINIA 4/14/1999
_ 36362 T2 MADISON VIRGINIA 4/14/1999
_ 38366 T2 MADISON VIRGINIA 4/14/1999
_ 38378 712 MADISON VIRGINIA 4/14/1999
_ 38391 72 MADISON VIRGINIA 4/14/1999
_ 38392 72 MADISON VIRGINIA 4/14/1999

More...

F3-Exit  FS=Refresh Fé=Add F9=Print Rpt Roll

 

 

Note
If you want to use tax rules that apply at the selling division’s location, make sure
you enter each division’s zip or postal code in the Tax Rule Table with the correct
tax code for that location.

### Adding A Tax Rule

To add a tax rule, press F6=Add on the Entrance screen. The Add Tax Rule Info
window is displayed.

  

 

Canadian Postal
Codes must be
entered with or
without a space
exactly like they
entered in
Receivables

Maintenance, such

as V4W 2H8 or
V4W2H8.

      
 
 
  
  

NW EQUIPMENT SALES

Zip/Postal Code Range

Starting Ending Tax code County Rpt code

X527-3 e TAX RULE MAINTENANCE 3

Tax Rule Maintenance X$2731

 

 

Add Tax Rule Info

 

  
    
  

Press F4=Prompt in the for the Sales Tax by
“Tax code” field to select County/State Report
from the list of valid tax {X16-4).

are codes.

   
  

 

   
    

Ixit  FS=Refresh

F4=Prompt  F12=Previous

 

 
       
     

 


Furnish the County

 

Fe=Add 9 F9=Print Rpt Roll.

    

 

1. Enter the information. See Fields & Descriptions below.

2. Press [Enter] to record the code. You will return to the Entrance screen.

3. Press F5=Refresh to see the entire list of codes.

### Fields & Descriptions

Starting 9 characters. Required. Beginning Zip/Postal code.
Canadian Postal Codes must be entered with or without a
space exactly like they are entered in Receivables
Maintenance, such as V4W 2H8 or V4W2H8.

Ending 9 characters. Optional. Ending Zip/Postal code.

Tax code 3 characters. Required. Press F4=Prompt to select froma
list of valid tax codes. Tax codes are set up in Tax Code
Maintenance (X527-1).

County 20 characters. Optional. If you want to print the Sales Tax

Report by County/State (X16-4) and have it sorted by
County, make sure each county is associated with a zip
code range; otherwise, all cities will be reported under a
blank county within each state.


4 X527-3 « TAX RULE MAINTENANCE RELEASE 2.3
NE ENSE 2

Rpt code 8 characters. Optional code from your tax reporting form. f

### Changing A Tax Rule

To change a tax rule, select it with 2=Change on the Entrance screen. The Change
Tax Rule Info screen is displayed.
NW EQUIPMENT SALES tax Rule Maintenance X52731
Change Tax Rule Info
Zip/Postal Code Range

Starting Ending Tax code County
38313 T2 MADISON

F4é=Tax Codes F12=Previous

F3=Exit FS<Refresh F6=Add F9=Print Rpt Roll

 

1. Type over any information you want to change.

2. Press [Enter] to record the change. You will return to the Entrance screen.
3. Press F5=Refresh to see the entire list of codes.


POINT OF SALE X527-3 « TAX RULE MAINTENANCE §

### Deleting A Tax Rule

To delete a tax type, select it with 4=Delete on the Entrance screen. A
confirmation window pops up, as illustrated below.

NW EQUIPMENT SALES Tax Rule Maintenance X52731

Zip/Pestal Code

2=Change 4=Delete
Opt Starting Ending Tax County Rpt Code Changed by / Date
71602 All JEFFERSON 35-Ci «VIRGINIA 4/14/1989
71602
71603 Delete Tax Rule Info
71611 Confirm Delete
71613
71630
71631 Starting
71634 Ending . .
71635 Tax Code
71638 county
71639 Rpt Code
74.640
71642 F12=Cancel

 

F3=Exit F$=Refresh

 

 

1. To cancel the request, press F12=Cancel.
2. To delete the code, press [Enter].


6 X527-3 ¢ TAX RULE MAINTENANCE RELEASE 2.3

### Printing A List Of Tax Rules

To print a list of all current tax rules, press F9=Print Rpt on the Entrance screen.
The Tax Code List Selection screen is displayed.

NW EQUIPMENT SALES TAX RULE LIST X52732
Division: A Selection

Sort by C(County), P(Zip/Postal), R(Rpt Code), or T(Tax Code)

Starting value. . :
Ending value. . :

 

Cm@1-Cancel

Select the sort option.

Furnish the starting (optional) and ending (required) values.

Press [Enter]. The job will be placed on the job queue.

Press [Enter] to return to the Tax Rule Maintenance screen. A sample report,
sorted by postal code, is illustrated on the next page.

BY

## CHAPTER X527-4

TAX CODE RATE CHANGE

### Introduction

Use this option when you want to make a change that affects several tax codes.
Changes can be made by tax code or description and restricted by tax type and/or
sales code. For State, County, City, District, and Other taxes, you can change:

Base Rate

G/L Account
Limit

Over Limit Rate
Limit Type (D/L)

Changes made with this utility can be identified in Tax Code Maintenance where
affected codes will display the ID of the person who made the change and 2
asterisks in the last positions of the ID field.

### Contents

SELECTION SCREEN........0:cesssssssesssssosssssssssssonsosseesseousseesasseeneeneenesseaneese 2

X5274.doc 7/29/99


2 X527-4 e TAX CODE RATE CHANGE RELEASE 2.3

SELECTION SCREEN

1. From the Point of Sale Menu (X5), select option 2, Table Maintenance Menu.

2. Select option 7, Tax Configuration Menu.

3. Select option 4, Tax Code Rate Change. The selection screen is displayed as
illustrated below.

SAMPLE DEALER TEST FILES TAX CODE RATE CHANGE 52740
Division: A Selection

Change by T(Tax code) or D(Desc) . . . .
Restrict to Tax type (blank=none)
Restrict to Sales Code (blank-none)

Starting value . .

Ending value. .

Fill in only the fields you want changed !
OverLimit Limit
G/L Acct imi Rate Type (D/L)

2100=$100.00)

When this screen is complete, press
cmdi-Cancel Cnd2-Continue —____ [Cmd2] to continue.

 

Change by T (Tax code) or D (Desc) 1 character. This is where you
indicate whether the text in the fields
labeled “Starting value” and “Ending
value” is a tax code or description.

Restrict to Tax type (blank=none) 1 character. Enter the only tax type
that will be affected by these
changes.

Restrict to Sales Code (blank=none) 2 characters. If you are changing tax
tates associated with one sales code,
type it here.

Starting value If you are changing by Tax code (T),
type the first tax code here. If you
are changing by Description (D),
type the first description here.


POINT OF SALE X527-4 ¢ TAX CODE RATE CHANGE 3

Ending value If you are changing by Tax code (T),
type the last tax code here. If you are
changing by Description (D), type
the last description here.

The following fields pertain to the 5 different taxing entities: State, County, City,
District, and Other. Fill in only the values you want to change and leave the others

blank.

Base Rate Required. The rate that is applied first.

G/L Acct Required. The general ledger account used to accrue the
tax.

Limit Dollar limit, if any, the base rate is applied to.

OverLimit Rate Rate, if any, that is applied to the dollar amount that is over
the limit.

Limit Type (D/L) Required. D=Document. The limit applies to all lines on
the document. L=Line. The limit applies to each line.


4 X527-4 ® TAX CODE RATE CHANGE RELEASE 2.3

Notes:

## CHAPTER X527-5

TAX HISTORY MAINTENANCE

### Introduction

This option was designed to correct errors associated with the initial file
conversion; however, it can be used at any time to correct errors on the Sales Tax
Report (X16-3) or Sales Tax Report by State/County (X16-4).

Only the following fields can be changed:
" City

" State or province

" Zip or postal code.

### Contents

X5275.doc 7/29/99 1


2 X527-5 ¢ TAX HISTORY MAINTENANCE RELEASE 2.3

ENTRANCE SCREEN
1. From the Point of Sale Menu (X5), select option 2, Table Maintenance Menu.
2. Select option 7, Tax Configuration Menu.
3.

Select option 2, Tax History Maintenance. The following prompts are
displayed.

SAMPLE DEALER TEST FILES TAX HISTORY MAINTENANCE X52750-01
Division: A

Address #
Document #

Month (MM)

Year (YYYY)

cmdi-End Job


X527-5 « TAX HISTORY MAINTENANCE

 

TAX HISTORY MAINTENANCE SCREEN

SAMPLE DEALER TEST FILES

Division: A

Customer Address:
Document number :
Description
Transaction Dat:
G/L Period

Debit /Credit

G/L Account
Transaction Amt
Stock aumber
City name
State/Prov Code
Zip/Postal code

GL2483

cT4g032ny+

PCB

5/02/98

199805


43203
182.64

‘ABBOTSFORD
BC
v2s ana

Cmd3-Return without Save, Enter-Update

TAX HISTORY MAINTENANCE %52750-01

These fields can be
changed to make
the Tax Report
accurate.


X527-5 * TAX HISTORY MAINTENANCE

Notes:


CHAPTER x1 14-1
MANUAL MERGE

### Introduction

The purpose of this job is to allow you to manually merge Payments (credits) with
their Corresponding invoices (debits) and to change the number of days for
calculating interest for a Particular invoice,

Note: The Merge applies to al] Customers regardless of their “Statement Type”
(“O” = Open Item, or “B” = Balance Forward). This code determines how
transactions display on the Statement, Credit and debit Processing is exactly the
Same for these two Statement types.

 
 
 

### Contents

ENTRANCE SCREEN... ceeee -2
Customer Index... 3
Change Days of Interest 4
Merge... 5
Verify Merge 7


2 Xt14-1e MANUAL MERGE RELEASE 2.3 |
(6
ENTRANCE SCREEN

1 From the Receivables Apply Credits Menu (X11-4), select option 1, Manual
Merge, press [Enter]. If the Receivables Security Gate appears, enter your
division code and security code and press [Enter]. The “Change Days of

Interest” screen will appear:

  
  
  

   
     

 

  
  

RGR EQUIPMENT SALES APPLY CREDITS 11402-2114
Division A Change Days of Interest By Invoice Date
address * Alpha gransaction -

  
 
  
 

Days Interest

 
  
 

G/L acct + Bal.
qrans Date Tavoice # pescription Addr * 1 bys Amount. unpaid

 

     

 

 
  
  

position to :
(emal-End cmd2-Change cmd3-Merge cmd9-Invoice Number Roll-Page

 
  

 
 

OO To exit the procedure and return to the Receivables Apply Credits Menu
(X114), press [Cmd1] - End.

1 If you know the address number of the customer, type the number in the
“Address #” field and press {Enter]. The information on the receivable will
appear. To change receivables type a new number in the “Address #” field and
press {Enter}.

0 To look up the customer in the Customer Index, type the first letters of the
name of the company OF the name of a receivable customer in the “Alpha”
field and press {Entes]. A Customer Index appears.


X114-1 « MANUAL MERGE 3

 

 

Customer Index
NW EQUIPMENT SALES APPLY CREDITS %11402-93
Division: A Customer Index
Name ---~--- 22 Address # Edit Codes Telephone
12345678901
a sHaw PAPER SUPPLY SHAWO1 R A 3337777
— SHOP EXPENSE SHOPOl R A
— SMITH, Dave SMITOL R A 675 3344
— SWEDELIUS . STEVE SWEDOL R B
— TEXAS NATURAL GAS TEXAQ1 WOR A 555 1111
— TExas NATURAL GAS-- GARAGE ‘TEXAO2 R A 555 5555
— THANK you FOR YouR BUSINESS CASHA VR A
_ TRUMAN, JACK MTRUOL R uM 555 1537
— TRUMAN, LARRY MTRUO2 R M 555 1356
_ TWOSHORS, amy TWOSO1 WoR A 333 2222
= UMPQUA, JAMES UMPQO1 R B 872 6763
~ USA, ANTHONY USAAOL R B
- VAN PELT, wes ‘VANPO? R A 856 1998
= VANDER BOAT, Wes VANDOi R B 354 9973
- WALTER , WALTER WALTOI R A 788 1233

Cmd3-Retuzn Ro11- Page

 

The Customer Index is listed in alphabetical order Starting with the letter(s) you
have typed in the “Alpha” field.

O Press the roll keys to scroll through the Pages of the screen. To select a
teceivable on the list, type any character on the line at the left of the
Teceivable’s name, Information on the receivable will display in the “Change
Days of Interest” screen automatically,

System. The user can not modify them,

Position Letter Means
Ww Units customer

Vv Vendor

E Employee

R Receivable customer

L Leasing customer

Cc Cash customer

T Employee Technician

d Division code (blank=all)

MD Bw DOL

™ co


4 X114-1 « MANUAL MERGE


Change Days of Interest

  
   
 
  

 
  
   

 

  
  
      
    
       
      
  
    
 

A&R EQUIPMENT SALES APPLY CREDITS x21402-11
Division A Change Days Of Interest By Invoice Date
address # SHAWO1 Alpha Transaction -
SHAW PAPER SUPPLY Days Interest
G/L Acet > Al110 Bal.: 7.63
prans Date Invoice F Description Addx # T Dys Amount. unpaid
1 01/20/99 TROOOT TIRES 240.00 240.00
2 02/01/99 TVO0018 4° INVOICE 195.43 195.43
3 02/15/99 ROA FEB 240.00- 240.00-
4 03/15/99 ROA MAR 100.00- 100.00-
s* END **

  
 

 

Position to !
qmal-End ¢m42-Change Cmé3-Merge emd9-Invoice Number Roll-Page

      

 
 

This screen allows you to change the number of days used for calculating the
interest for a particular invoice. When you calculate the interest from the option
Calculate And Post Interest (X11-9), the system will determine the number of
days for calculating interest in the following order:
1. Transaction, as specified in the “Days Interest” field in Apply Credits,
Manual Merge (X1 14-1)
2. Customer, as specified in “Number Of Days To Charge Interest” field in
Receivables Maintenance (X11-2)
3. Division, as specified in “Days Before Int” field in Security Maintenance
(X6-6) for all the receivables
4, Tfall these fields are blank, the default will be 30 days.

Transactions set to not charge interest for 999 days will be considered
"permanently current" and will never age regardless. The number of days until
interest begins can be set. for the division in Security Maintenance, for the
customer in Receivables Maintenance, and for a particular transaction in Apply
Credits. See also Receivables OPTS. Otherwise, even though interest charges are
postponed, transactions age normally. You might want to keep this in mind when
you compose messages that appear on statements. Aging cannot be changed.

co

### Accounting X114-16 Manual Merge 5

G To change the number of days of interest, enter the transaction number in the
“Transaction” field and the number of days desired in the “Days Interest” field

and press [Enter]. The number that you have entered will appear in the “Dys”
field.

O Ifyou never want to calculate the interest for Particular invoice, enter the
transaction number in the “Transaction” field and “999 in the “Days Interest”
field and Dress [Enter}.

oa Transactions are displayed by invoice number. To display transactions b
invoice date, press [Cmd9}. Invoice Number.

QD To Scroll] through the Pages of the Screen, press the Toll keys,

If you have Pressed [Cmd3] - Merge, in the “Change Days of Interest” Screen, the
“Merge” Screen wil] appear:

   

    
   

       
   
     
      
  
  
  

  
  

 
 
 
 

 

NW EQUIPMENT? SALES APPLY CREDITS %21402-92
Division a Merge By Invoice pate
Address SHAWOL Alpha Transaction #1
SHAW PAPER syppry Transaction g2
G/L Acct : a1ii19 Bal.;
Trans Date Invoice ¢ Description Addr# r pys Amount Unpaid
1 91/20/99 tRoog7 TIRES 240.00 240.00
2 02/01/99 rvo901g #* INVotcE 195.43 195.43
3 02/15/99 Ro, FEB 240.00- 240.00~
4 03/15/99 Rox MAR 100.00~ 100.00-

  
  

** END +x

      

Position to :
—_—_—
Cmdl-Eng md2-Change Cmd3 -Merge Cma$-Invoice Number Roll~page

  

 

This screen allows you to merge transactions entered in Create Source Documents
(X1-7) or Point OF Sale Invoicing (X5-1). Each line that appears in this screen


X114-1 « MANUAL MERGE. RELEASE 2.3

 

represents a transaction that is a debit (invoice), OF is a credit (payment) posted to
the account of the selected receivable. Credits appear as negative numbers.

Amounts to be merged display inthe “Unpaid” column.

O To merge a debit and a credit, enter the line number of the first transaction in
the “Transaction #4” field and the line number of the second transaction in the
“Transaction #2” field and press {Enter}.

C1 To return to the “Change Days of Interest” screen, press {Cmd2}.
0 To display transactions by invoice number, press [Cmd9}.

1 To scroll through the pages of the screen, press the roll keys.

1 To exit the procedure without applying credits, press {Cmdl]} - End.


ACCOUNTING X114-1 « MANUAL MERGE 7

Verify Merge

When you select two transactions to be merged and press [Enter], the screen will
Teappear displaying only the two transactions to be merged:

 

NW EQUIPMENT SALES APPLY CREDITS X11402-02
Division A Merge By Invoice Date
Address # SHAWC1 Alpha Fransaction #1 2
SHAW PAPER SUPPLY Transaction #2 4
G/L Acct : a2110 Bal:
Trans Date Invoice # Description addr# t Dys Amount Unpaid
2 02/01/98 rvoooig #+ INVOICE 195.43 195.43
4 03/15/99 ROA MAR 100.00- 100.00~-

Position to ;

——__
Cmd1-End Cmd2-Change cma3 “Merge Cnd9-Invoice Number Roll-Page

DIS-1185 You can Stop this merge by pressing Cmd2, cmd3 or Roll.

O To stop the merge, press [Cmd2], [Cmd3}] or one of the roll keys.

O To continue with the merge, Press [Enter]. After the Merge, transaction 4 wil]

no longer appear because itis completely merged, transaction 2 wil] appear
with its new unpaid amount,


X114-1 « MANUAL MERGE RELEASE 2.3

NW EQUIPMENT SALES APPLY CREDITS ¥11402-02
Division A Merge By Invoice Date
address # SHAWOL Alpbe — qransaction #1
SHAW PAPER SUPPLY transaction #2
G/L Acct : ALL10 Bal.:
trans Date Invoice F Description  Addr# I Dys Amount Unpaid
4 01/20/99 TROOOT TIRES 240.00 240.00
2 02/01/99 Iv00018 #* INVOICE 195.43 95.43
3 02/15/99 ROA FEB 240.00- 240.00-
*«* END **

Position to : ——___——
emdi-End Cmd2-Change Cnd3-Merge emd9—Inveice Number Rol1-Page

 

(1 From here you can continue merging transactions or you can exit the
procedure by pressing (Cmd1] - End.

When you have completed all your changes, press [Cmd1] - End, to exit the
procedure. The following messages will appear:

Step 1 of 2 - Receivables Aging Calculation Is Running
Step 2 of 2 - Average Payments Age Update Is Running

The Manual Merge procedure is completed. The Receivables Apply Credits Menu
appears.


FLEET MANAGEMENT GUIDE

CUSTOMER SERVICE & UNIT HISTORY

### Introduction

This guide describes enhancements to the DIS Service Management System,
which have been made for Fleet Management. In it, you'll find examples of
screens and reports, plus step-by-step instructions for installation and use.

Fleet Management is compatible with the Truck/Van Inventory Additional
Product. Its primary focus is the management of scheduled maintenance for
customers who own fleets of equipment located at different sites. Fleet
Management makes it possible to schedule maintenance by date or hourmeter and
to charge against a pre-established contract for maintenance.

The Fleet Management System was designed with the following objectives in
mind:

" Easy access to customer service information, unit information, and unit history
from Point of Sale.

= Improved efficiency for dispatcher to obtain a monthly customer list for
customers on Schedule Maintenance.

" Quick access to unit history for parts installed on a specific unit for warranty.

" Capture of unit repair cost for marketing service, parts, new equipment sales.

" Marketing analysis of unit population by age, cost of repair, etc. for service,

 

parts, and sales.
NOTICE
As in Service Management, unique serial numbers are required for Fleet
Management.

 

 

Fleet Management Guide.doc 5/17/2000


2 FLEET MANAGEMENT GUIDE * CUSTOMER SERVICE & UNIT HISTORY

ENHANCEMENTS

Very briefly, the enhancements include:

On Point of Sale work orders, all users are warned when a part is still on
warranty for any unit that bas been set up in Fleet Management. A pop-up
window allows you to change the billing to Internal (I) or Warranty (W). After
a part line is changed to Warranty, subsequent lines default to "W," which is
the same way Point of Sale works without Fleet Management. See page 17.
All new parts are warrantied for the number of days set as the default in
Maintain Parts Warranty.

Each part with a different warranty period must be entered in Maintain Parts
Warranty (X10.3-13).

To determine whether a part is still under warranty, the system checks the
install date, then the Maintain Parts Warranty table.

A new command key, Cmd8-Unit Index on the Inquire/Update Service Units
entrance screen. After a customer's ID (system address) is entered, you can
select the appropriate unit from a list. The list includes all units that can be
handled in the Service Management System. See UNIT INDEX, page 22.

Command keys from SMS View/Update screen to:

— Ship To Location Information, which includes notes, contacts, and
purchase orders (P/O's). Two main types of P/O's are displayed on the
information screen: Breakdown (BKD) and Scheduled Maintenance (SM).
Other types of P/O's can be entered. The remaining balance on SM and
BKD P/O's is updated when a work order is posted for the unit. See
CUSTOMER SERVICE INFORMATION, page 24.

- Unit Service Information, which pertains to the individual units in a flect
and includes relevant dates and records pertaining to the unit's service
contract and schedule. Units can be associated with existing contracts,
which are entered in Inquire/Update Service Contracts (X10.3-20). A
Scheduled Maintenance Summary report (X10.2-8) and Scheduled
Maintenance List (X10.2.9) can be printed for a specific (or all) contract
number.

A new field on the Sold To screen at Point of Sale records a "Work Date,"
from which the date of the next scheduled maintenance is calculated. In
addition, function keys provide access to notes, a record of parts installed
on the unit, and costs associated with the unit.

Parts and costs for the current owner and previous owners provide a
complete history. In addition, the system keeps track of the date parts are

-


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

installed and their warranty period. See UNIT SERVICE
INFORMATION, page 38.

= Each customer address may have multiple Ship To addresses associated with
it. Units within the fleet may be assigned to different Ship To addresses,
which correspond to their locations. The initial conversion process establishes
each customer address as a Ship To address for itself. As new addresses are

entered, this process must be done manually.

= The following reports have been added to the Service Report Menu (X10-2):

— Scheduled Maintenance Due (Divisional)

~ Scheduled Maintenance Overdue (Divisional)

-— Scheduled Maintenance Contracts Ending (Divisional)
— Scheduled Maintenance Summary (Divisional)

— Scheduled Maintenance List (Divisional)

— Parts History Report

— Unit Cost Report

— Options File List

— Warranties File List

See CHAPTERS X10.2-5 - X10.2-13.

= The following utilities have been added to the Service Utilities Menu:

- Maintain Service Options

— Maintain Parts Warranty

— Purge Repair Parts History

~ Purge Unit Repair Cost History
— Maintain Ship to Location

— Maintain Unit Service Info

— Assign Units to Ship to Location
— Maintain Hourmeters

—  Inquire/Update Service Contracts

See CHAPTERS X10.3-12 - X10.3-20.


4 FLEET MANAGEMENT GUIDE ¢ CUSTOMER SERVICE & UNIT HISTORY

### Overview

Most features in Fleet Management are concentrated within Inquire/Update
Service Units (X10-1) and can be handled on a case-by-case basis. There are
shortcuts on the Service Utilities Menu, and these will be pointed out but not
illustrated in this section.

To illustrate the features, we'll follow an example of a customer, Coleman
Forklift Corp., who has a fleet of 6 forklifis. The concepts can be illustrated in a
table, which will expand. Let’s start with the owner and the 6 forklifts.

 

 

OLEMAN FORKLIFT:COR

 

 

 

 

 

 

 

 

 

 

 

 

 

By pressing Cmd8-Unit Index at the Inquire/Update Service Units entrance
screen, you can see the units listed by serial number.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 5

 

Unit Index

AGR SALES & RENTALS Inquire/Update Service Units XA100-101 1
Division: A View/Update Search Only

Address # COLEO1 or
License # .
Serial# .

C Unit #

Unit Search

1=Select

Opt Serial + Make

FOOL AMAZON
F002 AMAZON
F003 AMAZON
F004 AMAZON
F005 AMAZON,

F3sExit F12=Previous

cma5-Service History Cmd6-Recommended Maintenance Cmd8-Unit Index

 

Coleman Forklift’s units were not purchased from the dealership; they were
entered in Service Management by serial number.

Since Coleman Forklift Corp. owns the fleet, it is billed for repairs; therefore, at
Point of Sale, Coleman will always be the “Sold To” address. Associated with the
billing address may be many “Ship To” addresses, which represent the various
locations of the customer’s units. The “Ship To” addresses may be any valid DIS
system address, they can be set up in Address Maintenance (X4-2) or on the fly.
The 6 Coleman forklifts are located in 3 different warehouses: 2 at Minharo
Wholesale in Burlington, 2 in Anacortes, and 2 in Sedro Wooley. To handle the 3
locations, 3 “Ship To” addresses are needed.

Two associations are needed:
= The “Ship To” addresses must be associated with the “Sold To” address
«Each unit must be associated with a “Ship To” address.


FLEET MANAGEMENT GUIDE ¢ CUSTOMER SERVICE & UNIT HISTORY

 

Assigning “Ship To” Addresses

For this step, we need one of the utilities on the Service Utilities Menu (X10-3),
which is illustrated below:

 

COMMAND MENU: XA3 WH
(c) DIS Corp.

1. Inquire/Update Service Tables 12. Maintain Service Options

2. Inquire/Update Make Model Assignments 13. Maintain Parts Warranty

3. Service Note Distribution 14. Purge Repair Parts History

4. Standard Job Rename 15. Purge Unit Repair Cost History
5. Serial Number Rename 16. Maintain Ship to Location

6. Service Divisional Profile 17. Maintain Unit Service Info

7. Update Standard Job Parts Prices 18. Assign Units to Ship to Location
8. Update Labor Rate for a Group 19. Maintain Hourmeters

9. Delete a Standard Job
10. Load Manufacturer Standard Jobs
11. Correct Service History

23. Return to Service Menu

Ready for option number or command
as=> 16

 

 

 

Select option 16, Maintain Ship to Location. In this job, we’ll be able to associate
3 “Ship To” addresses with Coleman Forklift Corporation.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 7

First, we’re prompted for an address:

 

A A&R SALES & RENTALS Maintain Ship To Location

Enter Sold to Address #. ... COLEOI

 

At this prompt, we'll enter Coleman Forklift’s address, which is the “Sold To”
address, and press [Enter]. The first time you see this screen, the only “Ship To”
address will be the same as the “Sold To.” That is because the conversion assigns
customers’ own addresses as their “Ship To” address in Receivables Maintenance.

On the screen illustrated below, 3 “Ship To” addresses have been assigned.
Select Customer Ship To Screen

 

A A&R SALES & RENTALS Maintain Ship To Location VSOQPVR
Select Customer Ship to

Sold to  COLEO1
COLEMAN FORKLIFT CORP.
2300 IOWA ST
BELLINGHAM WA 98226
Ship
To

1sSelect 2=Edit 4=Delete

Opt Ship Name Address

To
_ MINHO1 MINHARO WHOLESALE BURLINGTON

Open 8:00 Close 17:30 BURLINGTON WA 98233
_ MINHO2 MINHARO WHOLESALE ANACORTES

Open 7:30 Close 18:00 ANACORTES WA 98221

MINHO3 MINHARO WHOLESALE SEDRO WOOL
Open 6:00 Close 16:00

F3=Exit F6=Add Fi2=Previous

 

 

To assign more “Ship To” addresses, press F6=Add. You can select from a list of
all system addresses or press F6=Add again to add a new address, which. would be
the same as adding a new address in Address Maintenance (X4-2).


8 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

 

 

Now the 3 Minharo warehouses are associated with Coleman Forklift
Corporation. This step can be illustrated with the following diagram:

 

 

Here’s what we have so far:
= Coleman Forklift Corporation owns F001-F006.
= The 3 Minharo warehouses are “Ship To” addresses for Coleman Forklift.

‘The last step is to assign FO01-F002 to the Minharo warehouses. This can be done
from Inquire/Update Service Units, which will be illustrated in this section, or by
using another utility, Assign Units to Ship To IDs (X10.3-18). To use the utility,
see CHAPTER X10.3-18.

Assigning Units to a “Ship To” Address
For this step, we'll start on the View/Update screen in Inquire/Update Service

Units (X10-1). One of the Coleman Forklift units will be displayed on the detail
screen, in this case, F001:


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 9

 

ASR SALES & RENTALS Inquire/Update Service Units XAL00-102
Division: A View/Update Current Equipment
Address # COLEO1 or Name ..... COLEMAN FORKLIFT CORP.

   

License +

 
 
 
 

   

Serial# FOOL 2300 IOWA ST
Unit # . c Unit #
Series.: BELLINGHAM WA 98226
Make .. AMAZON: Phone 360 714 8578
Model ..
Year ...e-.eee22 97 Warranty code .. N
Description .... FORKLIFT Exp. date - 999999
Purchase date 10197 Engine # ...
Hourmeter .... 100 Key code ......-
Reminder date .. 30197
BIC eee ee eee N Job code .....

 

 

cmdi-End ¢md3-Go back Cmd5-Service History Cmd6-Recommended Maint
cma?-Cust Service Info Cmd8-Next Cmd10-Unit Service Info Cmd19-Delete :

 

 

You can press Cmd8-Next to cycle through the 6 units belonging to Coleman
Forklift Corp. When you get to the one you want, press either F7-Cust. Service
Info or Cmd10-Unit Service Info. Either command key will cause the following
window to pop up so that a “Ship To” address can be selected.

Select Ship To Window

A&R SALES & RENTALS
Division: A Select Ship To
Ship To
Address # Address #
License # .
Serial# .

 

1=Select

Ship To Name
Address #
: MINHO1 MINHARO WHOLESALE BURLINGTON
Description : MINHO2 MINHARO WHOLESALE ANACORTES

Purchase date .. MINHO3 MINHARO WHOLESALE SEDRO WOOL
Hourmeter ....

A/C...

F12=Previous


 

FLEET MANAGEMENT GUIDE ¢ CUSTOMER SERVICE & UNIT HISTORY

Select the appropriate “Ship To” location, and press [Enter] to proceed to the next
screen, which will be either Cust Service Info Details or Display Unit Service
Info. Both of these screens will be illustrated to help you understand the type of
information they record.

After each of the 6 forklifts have been associated with a “Ship To,” our table
looks like this:

 

Sedro Wooley

 

 

 

Coleman Forklift Corporation has a contract with A&R Sales & Rentals for
scheduled maintenance and breakdown repairs. Purchase orders are issued for
each warehouse to cover the units located there. Purchase orders are entered on
the Customer Service Information screen, which is reached from the
Inquire/Updates detail screen by Cmd7-Shipto Location Info.

On the following page, you'll see the Customer Service Info Details screen.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY W

Customer Service Information Details

 

A&R SALES & RENTALS Inquire/Update Service Units VSNA4DER
Cust Service Info Details

Sold To COLEO1 Ship To MINHO1
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233
HRS:..Open: 8:00 Close: 17:30 Map Location 28 Metro A
Contact: #1 RAE BARNES #2
Phone #: #1 360 650 - 5489 #2
Fax #: #1 360 738 - 7885 #2 -
SM: ¥ CFPM: ¥
BKD P/O #: 10100 Amount : 500.00
Ending Date: 12/31/97 Remaining Balance: 122.94
SM P/O #: Po 100800 Amount : 3900.00
Ending Date: 7/31/97 Remaining Balance: 3000.00

Note: Renews annually - contact in June

F2=Units F3=Exit F6=Edit F9=Note F10=Contacts FilsP/0's F12=Previous

 

 

Note that the information on this screen docs not pertain to an individual unit: it is
for the “Ship To” address although some information is updated from the Unit
Service Info screen, such as SM (Scheduled Maintenance) and CFPM (Contract
for Preventive Maintenance), which indicates that one or more units at this
location are under a service agreement. The purchase order remaining balances
are updated by Point of Sale. The information on the first line under the addresses,
opening & closing hours, map location, and metro, pertain to the “Ship To”
location and are entered via F6=Edit.

 

Look at the command keys at the bottom of the screen to get an idea of what you
can do here. The most important one is F11-P/O’s.


12 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

Once you have entered P.O. information for the 6 forklifts, the table looks like
this:

 

 

 
 
 

  

Bcaeowa (BKD) P.O. # & Amt.
SM (Scheduled Maint) P.O. # & Amt.

 
 
 

 

Breakdown (BKD) P.O. # & Amt.
SM (Scheduled Maint) P.O. # & Amt.

 
   
 
  
 

 

 

  

F005 Breakdown (BKD) P.O. # & Amt.
Sedro Wooley SM (Scheduled Maint) P.O. # & Amt.

FLEET MANAGEMENT GUIDE * CUSTOMER SERVICE & UNIT HISTORY 13

Unit Service Information

A&R SALES & RENTALS Inquire/Update Service Units VSOLDFR
Display Unit Service Info

Sold To COLE01 Ship To MINHO1
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233
Make Model Yr Serial # Hourmeter Div Group Option
AMAZON 2000 97° FOOL 10.0 A 2

Inst Date 90 Day i Year 3 Years 5 Years CREM End
1/01/97 4/01/97 1/01/98 12/31/97

SM Begin . : 1/01/97 SMEnd. .: 12/31/97 SM... 2:
SM Type ..: FSM SM Freq . 30 SM Due Type:
SM Rate . . 55.00 Cons Rate 36.00 Labor Hours:
sM Due . . 4/01/97 SM Prev. 1/01/97
SM Due Hr . :0 SM Prev Hr : <0

¥

 

Note :

F3=Exit F6=Edit F9%=Note Fi12=Previous Fi5=Parts F16=Costs

 

 

This screen applies to the unit displayed under the address fields, in this case,
F001. This is where the record-keeping is done concerning maintenance dates,
parts installed, and repair costs.

The most recent work date from a SM work order is stored as “SM Previous” on.
the Unit Service Information screen. “SM Due” is calculated by adding
“Frequency” to the most recent work date.

This screen is discussed in more detail later in this chapter.


14 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

After maintenance schedules have been entered, the table is nearly complete. All
that remains is for the system to track parts and costs, which are recorded on the
Unit Service Information screen (or through one of its function keys).

tr E COLEMAN FORKLIFT CORP: e
i MINHOL FOOL Breakdown (BKD) P.O. # & Amt.
Burlington Schedule & {SM (Scheduled Maint) P.O. # & Amt.
Records
F002
Schedule &
Records
MINHO02 F003 Breakdown (BKD) P.O. # & Amt.
Anacortes Schedule & | |SM (Scheduled Maint) P.O. # & Amt.
Records
F004
Schedule &
Records
MINH03 FO0S Breakdown (BKD) P.O. # & Amt.
Sedro Wooley |Schedule & |SM (Scheduled Maint) P.O. # & Amt.
Records

F006
} Schedule &
Records |

 


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 15

 

Scheduled Maintenance Due Report

After the initial setup work has been done, the service manager will run the
Scheduled Maintenance Due Report to see which units need to be serviced in the
next month. From this report, a plan can be developed whereby all units in the
same geographical area can be scheduled and the service manager can determine
how many technician hours will be required.

Point of Sale Work Orders

At Point of Sale, a work order is opened to the “Sold To” address, in this case,
Coleman Forklift Corporation. From the Sold To screen, pressing [Cmd18] takes
you directly to Inquire/Update Service Units for Coleman Forklift. You can look
on the Customer Service Information screen to determine the P.O. number the
service should be charged against. An example of the completed Sold To screen is
illustrated below:


16 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

Sold To Screen

ALR SALES & RENTALS INVOICING-SOLD TO 5100-105 4
Document classification
WORK ORDER # wo00045 CHARGE OPEN 3/26/97
Sold to: COLEOL Freon#: Ship to:
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
360 714 8578

   

2300 IOWA ST

BELLINGHAM WA 98226 98233
Credit Not Established
User ID HAL Password HAL = C Unit: TK Warr:
Ship By Sold By HAL P.0.# PO 109800 Add Date 3/26/97
Sales Code PC Transfer Quantity Break Pricing N Print Date
Tax Number Trans Date
Periodic Type Periodic Frequency Rental Start Date Group 3.
Std Job Desc: Std Job Flat Rate: om oY
Make Model Year Serial] Number Hourmeter Warranty
AMAZON 2000 97 FOO 250.8 N
Balance current 31-60 90 + WORK DATE
377.06 377.06 -00 : -00 032897
Internal Address #:
Credit Limit Peak Bal Beg Date Or Unit #:
099999 .00 3/19/97 Warranty Address #:

 

On this screen, the following fields are important to Fleet Management:

P.0.# Purchase order number from the Customer Service
Information screen in Inquire/Update Units (X10-
1).

Group Group code. Fleet Management is fully compatible

with the Truck/Van additional product. If it is not
being used, the number entered in the group field
will still be used on reports.

SM Y/N. Scheduled maintenance. Regardless of the
setting of this flag, the following fields are updated
by Create Point of Sale Posting Batch (X55-1):
hourmeter, parts repair cost, unit cost information.
In addition, parts warranty is always checked.

If this field is “Y,” the following fields are updated
by Create Point of Sale Posting Batch (X55-1):

If the unit has a SM Due Type of “D,” the SM
Previous and SM Due Dates are updated.

If the unit has a SM Due Type of “H,” the SM
Previous Hour, and SM Due Hour are updated.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 17

Hourmeter Hourmeter is always updated regardless of setting
of SM flag. If SM=Y, the SM Previous and SM Due
Hour fields are updated.

Warranty Y/N. This field pertains to internal warranty
documents only. It is not specifically for Fleet
Management.

Work Date Date on which work was actually done. The system
stores the work date for parts & cost history. If
SM=Y and maintenance is scheduled by date, the
work date is used to calculate “SM Due” by adding
“Frequency” to the most recent work date.

Warranty Parts

On Point of Sale work orders, all users are warned when a part is still on warranty

for any unit that has been set up in Fleet Management. A pop-up window allows

you to change the billing to Internal (I) or Warranty (W).

 

### A&R Sales & Rentals Work Order 5100-106

REPAIR ORDER # wo0004s For COLEO1 CHARGE OPEN 7/07/99
TDP Line t Price

  

Part Under Warranty

Part # Days Under Warranty
cas A10094 365

Unit Install Date Warranty Exp. Date
1/01/99 1/01/00

Specify who will pay for the part _ (blank/I/W)

Spec ord 00
PARTS CU

TD Isa Pty Line SC Ven Qty Part number Price Base
EN 0010 PC CAS 1 10094 4
Standard line code No demand

 

 

After a part line is changed to Warranty, subsequent lines default to "W," which is
the same way Point of Sale works without Fleet Management.


18 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY
SETUP

Service Info Maintenance—Link “Sold To” with “Ship To’s”

C1 Link "Sold To" customers with one or more "Ship To" names in Service Info
Maintenance (X10.3-16). See CHAPTER X10.3-16, MAINTAIN SHIP TO

LOCATION.

Customer Service Info—Purchase Orders (by “Ship To”)

(1 Optional. Enter purchase order information. See Purchase Orders in
CUSTOMER SERVICE INFORMATION, page 32. Purchase orders are
entered for the “Ship To” address.

Option Table

(1 Optional. Set up a list of options in Maintain Service Options (X10,3-12). See
can be associated with a unit on the Edit Unit Service Information screen.
Service options are user-defined and may pertain to any aspect of scheduled
maintenance. This is an optional step and can be done later. If the options are
entered, they can be associated with a unit in the Scheduled Maintenance

Information step below.

Enter Contracts
O Optional. Use Inquire/Update Service Contracts (X10.3-20) to enter contract
information. If the contracts are entered, units can be assigned to them in the
next step.

Scheduled Maintenance Information

O Enter scheduled maintenance information and associate options, if any, and
contracts with each unit in Inquire/Update Units Cmd10-Unit Service Info. To
process a lot of units at a time, use the shortcut utility, Maintain Unit Service
Info (X10.3-17). See CHAPTER X10.3-17, MAINTAIN UNIT SERVICE

INFO.


FLEET MANAGEMENT GUIDE * CUSTOMER SERVICE & UNIT HISTORY 19

 

Contacts

O Optional. Assign contacts. This step can be done later.

This concludes the overview of Fleet Management. What follows are step-by-step
instructions for using the Customer Service Information and Unit Service
Information screens. Separate chapters describe the reports (X10.2-5 - X10.2-13)
and utilities (Chapters X10.3-12 - X10.3-20).

 
   
 
     
  
  
 
 
 
 
 
 
    

### Warning!

  

The code combines both S/36 and AS/400 conventions, which handle decimal
places differently. On S/36 screens, decimal places are assumed: they are not
entered on the screen. On AS/400 screens, decimals are entered directly into
fields. If you enter 3600 on an AS/400 screen, the system records 3600.00.

When you deal with numbers with decimal places, look for the screen name in the
upper right corner. S/36 screens are numbered according to the menu map and
include the option number, such as X51000-106. AS/400 screen names are 7-
character combinations of letters and numbers, such as VSMAE1R, which don't
mean much to most of us.

In addition, S/36 screens refer to command keys, such as Cmdl-End job, while
AS/400 screens refer to function keys, such as F3=Exit. On all AS/400 screens,
press F3=Exit to end the job and return to a menu. If you just want to go back one
screen, press F12=Previous.


20 FLEET MANAGEMENT GUIDE e CUSTOMER SERVICE & UNIT HISTORY

### Adding A New Unit

In this section, you'll find step-by-step instructions for adding new units. The
process is different for a new customer as opposed to a customer that has already
been set up in the system.

New Customer

Qa
Oo

Set up the customer in Receivables Maintenance (X11-2).
From the Service Management Menu (X10), select option 1, Inquire/Update
Service Units.

On the entrance screen for Inquire/Update Service Units, type the customer
address number, and press [Enter]. You'll receive a message that equipment
does not exist.

© Type the serial number of the new unit, and press [Enter]. The View/Update

oo

oo

oo

screen displays blank fields to record unit information.

When the information is complete, press [Enter].

When the screen is complete, press [Enter] to record the information. The
customer's name and the new serial number remain on the entrance screen.
Add other equipment as necessary.

Press [Cmd1] to end the job.

From the Utilities Menu, select Maintain Ship to Location (X10.3-16). For
details, please see CHAPTER X10.3-16. The Maintain Ship To screen appears
with a prompt for the “Sold to” address number.

At the “Enter Sold to Address #” prompt, press F4=Prompt or key in the
address number of the equipment owner. The purpose of this job is to set up
Ship To addresses for the equipment owner.

Press F6=Add. A list of receivables and marketing addresses is displayed.
Select an address by typing "1" beside it, or press F6=Add to add a new Ship
To address.

O You may add as many Ship To addresses as needed Press F3=Exit. After each

one, you can enter the corresponding Open Time, Closing Time, Map
Location, and Metro Flag.

From the Utilities Menu, select Assign Units to Ship To Location (see

## CHAPTER X10.3-18

## ). You will be prompted for a “Sold to Address#.” The

Assign Ship To Address screen lists all units belonging to the customer. Select
a unit with 2=Change to add or change a Ship To assignment.

You can also assign the unit to a Ship To address by pressing Cmd7-Customer
Service Information or Cmd10-Unit Service Information. A window opens to
allow you to select a Ship To address. Select a Ship To address by placing a
"1" beside it and pressing [Enter].

Co


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 21

Existing Customer

O Type a few characters of the customer's last name, and press [Enter]. The

customer index displays the closest match. If you choose to type an existing

customer's address number, press {Enter] to allow the system to find the

record.

Select the customer's name by typing any character beside it. If the customer

already owns equipment, the first unit is displayed on the View/Update

screen.

Press [Enter] to return to the entrance screen.

Type the serial number of the new unit, and press [Enter]. The View/Update

screen displays blank fields to record unit information.

When the screen is complete, press [Enter] to record the information. The

customer's name and the new serial number remain on the entrance screen.

Press [Enter] again. The View/Update screen displays the information you just

entered.

You can assign the unit to a Ship To address by pressing Cmd7-Customer

Service Information or Cmd10-Unit Service Information. A window opens to

allow you to select a Ship To address. Select a Ship To address by placing a

"1" beside it and pressing [Enter].

1 If you prefer, you can also assign a Ship To address from the Service Utilities
Menu in Assign Units to Ship To Location (X10.3-18). For details,

## CHAPTER X10.3-18.

Oo

o6Oo 6 0 OO


22 FLEET MANAGEMENT GUIDE * CUSTOMER SERVICE & UNIT HISTORY

### Unit Index

On the entrance screen for Inquire/Update Service Units:

A&R SALES & RENTALS Inquire/Update Service Units XA100-101 2
Division: A View/Update Search Only

Address # .. + COLEO1 or
License #

Serial# .

Unit # ... see C Unit #

1sSelect

Opt Serial #
FOOL
F002
F003
FOO4
FOOS

F3sExit ¥F12=Previous

 

cmd5-Service History Cmd6-Recommended Maintenance Cmd8-Unit Index

 

C1 Type a customer address number.

O) Press Cmd8-Unit Index. A list of units belonging to the customer is displayed:

O Select a unit for service with 1=Select, and press [Enter]. The View/Update
screen displays information about the unit:


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 23

 

View/Update Screen

 

A&R SALES & RENTALS
Division: A

Inquire/Update Service Units
view/Update

XA100-102
Current Equipment

Address # ..
License #
Serial#
Unit # .

Make ..

Year

Description ....
Purchase date ..

. COLEQ1 or

. FOO6

Cc unit #
Series.:
AMAZON

COLEMAN FORKLIFT CORP.
2300 IOWA ST

BELLINGHAM WA 98226
Phone 360 714 8578

Warranty code ..
Exp. date .... 21098
. 20994A-08763

Engine # .
Key code .
Reminder date
alc . : Job code

Hourmeter ....

(mdl-End Cmd3-Go back Cmd5-Service History Cmd6-Recommended Maint
(md7-Cust Service Info Cmd8-Next Cmdl0-Unit Service Info Cmd19-Delete

 

On this screen, you can see the new command keys, which are discussed on the
following pages. See CUSTOMER SERVICE INFORMATION, page 24, and
UNIT SERVICE INFORMATION, page 38.

 

   
   
     

NOTE

To delete a unit and all of its service history, press [Cmd19] on this screen. The
unit cannot be reinstated; therefore, you should delete equipment only when it is
incorrect or when you are short of disk space.


24 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

### Customer Service Information

On the Customer Service Information screen, which has no security gate, users
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
from the system), and a function key allows the user to purge all P/O's with zero
balances at one time.

1 From the SMS Inquire/Update screen, press Cmd7-Cust Service Info to reach
the Cust Service Info Details screen. The same screen is available from the (
Entrance, Sold To, and detail screens at Point of Sale Invoicing (see

## CHAPTER X5-1

## , POINT OF SALE). The Customer Service Info Details

screen is displayed first in Inquiry mode, as illustrated below.

Cc


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 25

Cust Service Info Details Screen

ASR SALES & RENTALS Inquire/Update Service Units VSNSDFR

Cust Service Info Details

Sold To COSTO1 Ship To CosT02

COST CUTTER FOODS
4111 GUIDE MERIDIAN
BELLINGHAM WA 98225

Cost Cutter Limited-Sumas
944 Cherry St
Sumas, WA 98341

LEE REECE EEGEE CSS CHEE HEISE GGUS IES SISO IEEE ISDE ING EG OEE
HRS:..Open: 4:00 Close: 21:00 Map Location 460 Metro ¥

Contact: #1 Meredith Curry #2 DOUGLAS A/WILLIAMS

Phone #: #1 206 398 - 1145 42 206 734 - 0567

Fax #: 0 #1 - #2 -

SM: ¥ CEPM:
BKD P/O #:

Y
666-666
Ending Date: 9/30/94

Amount: 1000.00
Remaining Balance:
Amount: 3000.00
Remaining Balance:

1000.00
SM P/O #: 235-2409
Ending Date: 12/31/94 3000.00
Note: Notes are displayed by date, with the most

date first. Notes entered on the same date

remain in order. Press F9=Note to sce more.

F2<Units ¥F3=Exit Fé=Edit F9=Note F10=Contacts F1l=P/O's F12=Previous

 

 

O To work with Unit Service Information, press F2=Units. See F2-Units, page
26.

O To change the Customer Service Information screen, press F6—Edit. See
F6=Edit, page 27.

0 To maintain notes about the customer, press F9=Note. See F9=Notes, page 28.

D To maintain contacts for the customer, press F10=Contacts. See
F10=Contacts, page 30.

CO To maintain purchase orders for the customer, press F1 1=P/O's. See
F11=Purchase Orders, page 32.

O To go back one screen, press F12=Cancel.

1 To end the job and exit to the Service Management Menu, press F3=Exit.


26 FLEET MANAGEMENT GUIDE e CUSTOMER SERVICE & UNIT HISTORY

F2=Units

O To work with Unit Service Information, press F2=Units. The Unit Search
screen appears with a list of units assigned to the Ship To address.

A&R SALES & RENTALS Inquire/Update Service Units
Unit Search
Sold To COSTO1 Ship To COSTO2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341

Make Serial #

C=Cost NsNotes P=Parts 5=Display

Opt Model Make Serial # Equip # Options
— 2000 RAYMOND — 1G8ZH1576RZ211704 wa
— 2000 RAYMOND —- 1G8ZH1576RZ211705 we

F3sExit F12=Previous

 

C Use any combination of the position prompts or scroll by pressing [PgDn] to
locate the unit you want.

O To see costs associated with a unit, type C beside it in the column labeled
"Opt," and press [Enter].

O To record notes about a unit, type N beside it and press [Enter].

O To see parts that have been installed on a unit, type P.

O To display a unit, type 5.

See UNIT SERVICE INFORMATION, page 38.


FLEET MANAGEMENT GUIDE e CUSTOMER SERVICE & UNIT HISTORY 27

Fé=Edit

To change the location information, press F6=Edit. The Edit Customer Location
Details screen is displayed:

A&R SALES & RENTALS inguire/Update Service Units VSNADFR
Cust Service Info Details

Sold To cosT01 Ship To CosTo2
COST CUTTER FOODS Cost Cutter Limited~Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341
FORE E EEE G GEST OI SIH UG EIS UEO EO IUOISODNEUOUE AISI G EEA IIE
Open Time . . - 400
Closing Time . . 2100
Map Location . . 460
Metro Flag. .- ¥

F3=Exit F12=Previous

 

0 For "Open Time" and "Closing Time" use 24-hour military time. For example,
for 6 P.M., type: 1800 and press [Field Exit].
O To return to the Details screen, press F12=Previous.


28 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

 

F9=Notes

O To maintain notes about the customer, press F9=Note on the Edit Customer
Service Info Details screen. The Edit Customer Notes screen is displayed in
CHANGE mode if there are current notes; otherwise, it is displayed in ADD
mode.

CHANGE Mode

ASR SALES & RENTALS, Inquire/Update Service Units CHANGE VSLSEFR
Edit Customer Notes

Sold To PARKO1 Ship To PARKOL
AUSTIN PARKER AUSTIN PARKER
3149 ELLIS 3149 ELLIS
BELLINGHAM WA 98225 BELLINGHAM WA 98225
Note Date

4=Delete request

Opt Note Date Note
3/10/94 The 3 most recent notes are displayed at Inquiry.
3/10/94 To see other notes, press F9=Note.
3/10/94 There is no limit to the number of note lines.

F3=Exit Fé=Add F12=Previous

 

© Use the position prompt or scroll by pressing [PgDn] to locate the note you
want.

O To change a note line, simply type over the existing line. The system records
the most recent User ID in the column labeled "Changed by"; however, the
date is not changed.

O To delete 1 or more note lines, type 4 in the column labeled "Opt" and press
[Enter].

O Toggle to ADD mode by pressing F6=Add. A screen of blank note lines is
displayed.


FLEET MANAGEMENT GUIDE e CUSTOMER SERVICE & UNIT HISTORY 29

 

ADD Mode

 

A&R SALES & RENTALS Inquire/Update Service Units VSLSEFR
Edit Customer Notes

PARKOL Ship To PARKO1

AUSTIN PARKER AUSTIN PARKER

3149 ELLIS 3149 ELLIS
BELLINGHAM WA 98225 BELLINGHAM WA 98225

F3=Exit Fé=Change F12=Previous

 

O Type as many note lines as you need and press [Enter] to record them.
O Toggle to CHANGE mode by pressing F6=Change.

O To go back to the detail screen, press F12=Previous.

O To end the job and return to the menu, press F3=Exit.


30 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

F10=Contacts

A contact is simply a record of one or more persons who can be contacted in
regard to contracts, maintenance, and units. Each customer can be associated with
as many contacts as needed. Only the first 2 contacts are displayed on the
Customer Service Information screen.

O To maintain contacts, press F10=Contacts. The Edit Contacts screen displays a
list of current contacts, if any.

A&R SALES & RENTALS Inquire/Update Service Units VSLTDFR
Edit Contacts

Sold To cosTdi Ship To CosT02
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341

4=Delete

First Name Last Name

Meredith, curry. —-—_____
Phone 206 733 - 0243 Ext 4571 Fax 206 733 - 5106
Steve___ Garrett.
Phone 206 734 - 2514 Ext 1134 Fax 206 671 ~ 9706

F3=Exit F6=Add F12=Previous

O To change information on this screen, type over the existing data and press
[Enter].

Ci To delete a contact, type 4 beside the name in the column labeled "Opt" and
press [Enter]. The contact is deleted without confirmation.

O To add new contacts, press F6=Add. A blank list for contact information is
displayed, as illustrated below.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 31

 

AGR SALES & RENTALS

Sold To cosTol

Inquire/Update Service Units VSOSEFR
Edit Contacts

COST CUTTER FOODS
4111 GUIDE MERIDIAN
BELLINGHAM WA 98225

First Name
Phone
Phone

Phone

Phone

F3=Exit F6=Change

 

Phone __. ___

F12=Previous

Ship To

cosTo2

Cost Cutter Limited-sumas
944 Cherry St

Sumas, WA 98341

 

D Add as many contacts as necessary. Press [Enter] to add the names or press
[PgDn] for another blank list.
O To toggle to CHANGE mode, press F6=Change.


32 FLEET MANAGEMENT GUIDE ¢ CUSTOMER SERVICE & UNIT HISTORY

F11=Purchase Orders

The first 2 types of purchase orders are displayed on the Customer Information
screen; however, there is no limit to the number of purchase order numbers that
can be stored. Purchase order numbers must be unique.

I To maintain purchase orders for the customer, press F11=P/O's on the Edit
Customer Info Details screen. The list of current P/O's, if any, is displayed.

AGR SALES & RENTALS Inquire/Update Service Units VSLXDFR
Purchase Orders

Sold fo COSTO1 Ship To cCosTo2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341
Type End Date Number

2=Edit P/O 4=Delete 5=Invoices

Opt Type End Date Number Amount Balance
_ so 12/31/94 118145 750.00 750.00

Purchase Order balances reflect tax and discounts. They may differ from
amounts seen in F16=Costs, which are before tax and discounts.

Only P/O's with zero balances can be deleted.

F3-Exit F6=Add F12=Previous F13=Purge Records

 

O To change a purchase order, type 2 beside it in the column labeled "Opt" and
press [Enter]. See Add Purchase Orders, page 34. (same screen).

O To delete a particular purchase order, type 4 beside it in the column labeled
"Opt" and press [Enter]. A confirmation message is displayed. Only P/O's
with zero balances can be deleted.

O To review invoices (or work orders) associated with a purchase order, type 5
beside it in the column labeled "Opt" (Purchase Orders screen) and press
[Enter]. See Invoices, page 33.

0 To add purchase orders, press Fo=Add. See Add Purchase Orders, page 34.

O To remove zero balance P/O's from the system, press F13=Purge Records. See
F13=Purge Records, page 35.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 33

Invoices

D To review invoices (or work orders) associated with a purchase order, start at
the Purchase Orders screen. Type 5 beside the purchase order in the column
labeled "Opt," and press [Enter]. A list of invoices, if any, is displayed.

 

A&R SALES & RENTALS

Sold To cosTo1

Inquire/Update Service Units VSLODFR

COST CUTTER FOODS
4111 GUIDE MERIDIAN
BELLINGHAM WA 98225

Purchase Order
235-2409

Invoice Invoice
Number Date

Invoice Invoice
Number Date
§M09026 9/23/94

F3sExit F12=Previous

Type
SM

Invoice
Amount.
142.36

Invoices

Ship To

Date
12/31/94

cosTo2

Cost Cutter Limited-Sumas

944 Cherry st

Sumas, WA 98341

Amount Balance
3000.00 2857.64


34 FLEET MANAGEMENT GUIDE * CUSTOMER SERVICE & UNIT HISTORY

Add Purchase Orders

0 To add purchase orders, press Fé=Add. The Add Purchase Order screen
appears.

A&R SALES & RENTALS Inquire/Update Service Units
Add Purchase Order

Sold To CosTo1 Ship To COsTo2
COST CUTTER FOODS Cost Cutter Limited-sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341

P/O Number . .
P/O Type. . ~
P/O End Date -
P/O Amount . .

F3sExit  F12=Previous

 

O Type the requested information. This is an AS/400 screen: don't forget to type
the decimal in the P.O. Amount field.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

F13=Purge Records

O To remove zero balance P/O's from the system, press F13=Purge Records.

A&R SALES & RENTALS Inquire/Update Service Units
Purchase Orders

cosTo1 Ship To COSTOZ
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98342
Type End Date Number

Purge P/O Invoices

Purge all invoices for zero Balance

balance Purchase Orders _ 1000.00
2500.00

F3-Exit F12=Previous

F3=Exit F6=Add F12=Previous F13=Purge Records

O To confirm your request to remove the P/O's, type y (Yes) and press [Enter].
O To cancel your request, press F12=Previous.


36 FLEET MANAGEMENT GUIDE ¢ CUSTOMER SERVICE & UNIT HISTORY

 

 

Customer Service Information Screen: Field Definitions

BKD
P/O#
Ending Date

Amount
Remaining Balance

CFPM
Changed by

Closing Time
Contact

HRS
Open Time
Closing Time

Map Location
Metro
Note

Note Date

Open Time
Option

SM

SM
P/IOF#
Ending Date
Amount

Purchase Order Number

Date (mmddyy). End of purchase order
authorization period.

Dollar amount of purchase order.

Amount of original P/O minus cost of repairs to
date. Purchase Order balances reflect tax and
discounts. They may differ from amounts seen in
F16=Costs, which are before tax and discounts.
Y/N, Extended maintenance contract. Will be "Y" if
there are any units on service maintenance.

User ID of the person who entered a note line for a
customer or unit.

See HRS.

6 characters. Person's name and phone number at
the Ship To address.

Time (hhmm). Use 24-hour military time.

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
date, the 3 most recent note lines are displayed for
customers and the 3 oldest lines are displayed for
units.

See HRS.

8 characters. Option code. Options are set up in
Unit Service Options Table (X10.3-7)

Y/N. Scheduled Maintenance. Will be "Y" if there
are any units on service maintenance.

Purchase Order number
Date (mmddyy)
Dollar amount of original P/O


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 37

Remaining Balance Amount of original P/O minus cost of repairs to
date. P/O balances reflect tax and discounts.


38 FLEET MANAGEMENT GUIDE * CUSTOMER SERVICE & UNIT HISTORY

### Unit Service Information (

CO From the SMS Inquire/Update screen, press Cmd10-Unit Service Info to reach
the Unit Service Info screen. The same screen is available from the Sold To
screen at Point of Sale Invoicing (see CHAPTER X5-1, POINT OF SALE).
After a unit serial number is entered, the Unit Service Info screen is displayed
in Inquiry mode, as illustrated below. If a serial number is not entered, the
Customer Service Information screen is displayed instead.

 

   

AGR SALES & RENTALS Inquire/Update Service Units VSOLDFR
Sold To ADAMOL Ship To ADAMOL

WILLIAM ADAMS WILLIAM ADAMS

RT 2, BOX 933 RT 2, BOX 933

ARLINGTON, WA 98223 ARLINGTON, WA 98223
Make Mode. vr serial # Hourmeter Div Group Option
1% 1. 90 11112567777 0 A 0
Inst Date 30 Day 2 Year 3 Years 5 Years CFPM End
3/01/99 6/01/99 3/01/00
SM Begin 5/01/99 SMEnd..: 5/01/00 SM... 1: N
SM Type . bsm SM Freq .: 60 SM Due Type: D Date
SM Rate - $5.00 Cons Rate : 5.00 Labor Hours: 3.6
SM Due 8/01/99 SM Prev. : Contract Number 789 {
Note

F3sExit F6=Edit F9=Note F12=Previous F15=Parts F16=Costs

 

(0 To change or add service information, press F6=Edit. See F6=Edit, page 39.

1 To add notes, press F9=Note. See F9=Notes, page 44.

UO To review parts that have been installed on this unit, press F15=Parts. See
F15=Parts, page 42.

O To review costs associated with this unit, press F16=Costs. See F6=Costs,
page 45.

O To go back to the Inquire/Update Units screen, press F12=Previous.

D To go back to the Service Management Menu, press F3=Exit.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 39

F6=Edit

O To change or add service information, press F6=Edit. The Unit Service Info
screen appears in edit mode.

  
       
     
    
     

A&R SALES & RENTALS Inquire/Update Service Units VSMAEIR

 

     
    

Sold To ADAMO1 Ship To ADAMO1
WILLIAM ADAMS WILLIAM ADAMS
RT 2, BOX 933 RT 2, BOX 933
ARLINGTON, WA 98223 ARLINGTON, WA 98223
Make Model Yr Serial # Hourmeter Div Group Option

an 90 11112567777 0 A 9

  

 

  

        
 
    
  
   

Inst Date 90 Day 1 Year 3 Years 5 Years CFPM End
3/01/99 6/01/99 3/01/00 99999999

   
 

       

F4=Prompt
to select
from a list.

                  
    
  
 
   
  

   

SM Begin 5/01/99 SM End . 5/01/00 SM. ...: N
SM Type...  bsm SM Freq . - 60 SM Due Type D
SM Rate... 55.00 Cons Rate .- 5.00 Labor Hours 3.6
sM Due... 6/01/99 SM Prev . - Contract Number
SM Due Hr SM Prev Hr .

    

  

   

Note

   

      

F9=Note

   
 

F4=Prompt Fl2=Previous F15=Parts F16=Costs

 

O To start a Scheduled Maintenance contract, enter a date in the field labeled
"SM Begin." See Fields and Definitions, page 49.
1 When you are done, press [Enter] to record the changes.


40 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY.

F9=Notes

The 3 most recent note lines are displayed on the Edit Unit Service Info screen;
however, there is no limit to the number of note lines that can be stored. When
multiple lines are entered on the same day, they are maintained in the order in
which they were entered.

O To add or change notes about a unit, press F9=Note from the Edit Unit Service
Information screen. The Edit Vehicle Notes screen is displayed in CHANGE

mode if there are existing notes; otherwise, blank note lines are displayed in
ADD mode.

CHANGE Mode

AGR SALES & RENTALS Inquire/Update Service Units CHANGE VSL6EFR
Edit Unit Notes

COLEO1 . Ship To MINHO1
COLEMAN PORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233
Serial # Make Model ID
FOOL AMAZON —- 2000
Note Date

4=Delete request

Note Date Note Changed by
10/22/97 The most. recent note lines are displayed first.

10/22/97 Press F9=Note to see more notes or add notes.

10/22/97 There is no limit to the number of note lines.

10/22/97 ‘Type as many as you want.

10/22/97 Line 5

10/22/97 Line 6

F3=Exit F6=Add F12=Previous

 

0 Use the position prompt or scroll by pressing [PgDn] to locate the note you
want,

C1 To delete a note line, type 4 beside it in the column labeled "Opt" and press
[Enter].

O To change a note, simply type over the current line. The system records the
most recent User ID in the column labeled "Changed by;" however, the date is
not changed.

O Toggle to ADD mode by pressing F6=Add. A screen of blank notes is
displayed.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 4i

 

ADD Mode

 

A&R SALES & RENTALS Inquire/Update Service Units VSL6EFR
Edit Unit Notes

Sold To COLEO1 Ship To MINHO1
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233
Serial 4 Make Model ID
FOO AMAZON 2000

Note
Deaier prep 3/19/97 OK-Luke,

F3=Exit F6=Change F12=Previous

 

0 Type as many note lines as you need and press [Enter] to record them.
O Toggle to CHANGE mode by pressing F6=Change.

O To go back to the detail screen, press F12=Previous.

O To end the job and return to the menu, press F3=Exit.


42 FLEET MANAGEMENT GUIDE ¢ CUSTOMER SERVICE & UNIT HISTORY

F15=Parts

 

NOTE
To purge parts history from the following series of screens, use Purge Repair
Parts History (X10.3-14).

 

 

To review the parts that have been installed on the unit, press F15=Parts. A list of
parts that have been installed for this customer are displayed. The parts are
displayed in order first by part number, then by labor date (most recent first).

A&R SALES & RENTALS Inquire/Update Service Units VSL9DFR
Customer's Unit Repair History

Sold To cOsTO1 Ship To cosTo2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341
Make Model Serial # Hourmeter
RAYMOND 2000 1GBZH1576RZ211704 3011.0
Part Number
Part Part Vendor Hour Labor Invoice
Qty Number Meter Date W/O Number
1 1150-065 RAY 254.0 3/21/94 sm09024
1 1150-065 RAY 21.0 3/15/94 sMo9022
2 154-010-210 RAY 1501.0 9/23/94 sMo9026
1 590-096 RAY 1007.0 6/30/94 sMo9025
1 632-043-001 RAY 2467.0 12/21/94 sM09027
1 632-043-001 RAY 1007.0 6/30/94 sM09025
1 632-043-001 RAY 21.0 3/15/94 smo9022

F2-Unit History F3=Exit F1l2=Previous F21=Print

 

1 Use the position prompt or scroll by pressing [PgDn] to locate the part you are
interested in.

CO To print a list of parts that have been installed since this customer purchased
the unit, press F21=Print. See F2/=Print Unit Repair History, page 43.

O To review all parts that have been installed on this unit (for all owners), press
F2=History. See F2=History, page 44.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 43

 

F21=Print Unit Repair History

O To print a list of parts that have been installed since this customer purchased
the unit, press F21=Print on the Customer's Unit Repair History screen.

1 To print a list of all parts that have been installed on this unit (for all owners),
press F21=Print on the Unit Repair History screen.

In either case, a prompt for Printer ID is displayed.

A&R SALES & RENTALS Inguire/Update Service Units VSL9DFR
Customer's Unit Repair History

Sold To cOsTO1 Ship To cosTo2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry St
BELLINGHAM WA 98225 Sumas, WA 98341

Model Serial # Hourmeter
2000 1G8ZH1576R2211704 3011.0

Enter Printer Id nvoice
70 Number
: MO9024
M09022
M09026
M09025
MO9027

: = MO9025
632-043-001 +0 3/15/94 smM09022

Num :

115 : Printer Id

115:

184: F3=Exit F12=Previous
590 :

632 :

 

F2=Unit History F3=Exit Fl2=Previous F21=Print

 

 

O Enter a printer ID, or leave the prompt blank and the report will be printed on
the default printer for your User ID.


44 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

F2=History

O To review all parts that have been installed for all owners, press F2=History.

A&R SALES & RENTALS Inquire/Update Service Units VSNODFR
Unit Repair History

Make Model Serial # Hourmeter
RAYMOND 2000 1G8ZH1576RZ211704 3011.0
Part. Number

Part Vendor Hour Labor Invoice
Number Meter Date w/O Number
1150-065 254. 3/21/94 sm09024
1150-065 21. 3/15/94 sM09022
154-010-210 1801. 9/23/94 sMos026
590-096 1007. 6/30/94 sMo9025
632-043-001 2467.0 12/21/94 sMo9027
632-043-001 1007. 6/30/94 sM09025
632-043-001 21. 3/15/94 smo9022

F3=Exit  F12=Previous F2i=Print F3=Exit  F12=Previous F21=Print

 

O To print this list, press F21=Print. See previous page.


FLEET MANAGEMENT GUIDE e CUSTOMER SERVICE & UNIT HISTORY 45

 

F16=Costs

 

NOTES

Unit cost amounts are before taxes and discounts; therefore, purchase order
balances, which reflect taxes and discounts may be different.

To purge cost history from the following series of screens, use Purge Unit Repair
Cost History (X10.3-15).

 

 

O To review costs associated with a unit, press F16=Costs on the Unit Service
Information screen. The Select Sales Code window is displayed.

Select Sales Codes

Sales Sales Code NHOL
Code Description NHARO WHOLESALE BURLINGTON
RLINGTON WA 96233
isSelect Meter Div Group option
0.0 A 2 OVER
Opt Sales Sales Code
Code Description 5 Years CFP End
“ 12/31/97
RCVD ON ACCOUNT
cD CUST DEPOSITS :
UNIT TRADE H  Hourmeter
EQUIPMENT SALE Labor Hours = 1.5

JOHN'S SALES

F2=All F3=Exit Fi2=Previous ed.
otes.
lines.
=Parts F16=Costs

 

Select Sales Code Window

D To review costs associated with all sales codes, press F2=All.

1 To select 1 or more sales codes, type 1 beside them in the column labeled
"Opt" as illustrated above, and press [Enter]. The costs associated with the
selected sales codes are displayed.


46 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

Unit Repair Cost for Customer

A&R SALES & RENTALS Inquire/Update Service Units VSMRDFR
Unit Repair Cost for Customer

Sold To cosTo1 Ship To cosTo2
COST CUTTER FOODS Cost Cutter Limited-Sumas
4111 GUIDE MERIDIAN 944 Cherry st
BELLINGHAM WA 98225 Sumas, WA 98341
Make Model Serial # Hourmeter
RAYMOND 2000 1GBZH1576RZ211704 +0
Inst Date 90 Day 1 Year 3 Years 5 Years
3/21/94 6/21/94 3/21/95
Code Month Year Life
Total 106.68 685.16 685.16

Sales Code Current Year to Life
Month Date to Date
PS - PARTS SHOP 67.73 158.83 158.83
TC - LABOR CUSTOMER 38.95 136.33 136.33
TD - LABOR CUST MISC -00 390.00 390.00

F2sUnit History F3=Exit F12=Previous F21=Print

 

O To print the costs incurred by the current owner, press F21=Print. A prompt for
Printer ID is displayed.


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 47

 

F21=Print Unit Repair Cost

A&R SALES & RENTALS Inquire/Update Service Units
Unit Repair Cost for Customer

   

cosToi Ship To CosTo2
COST CUTTER FOODS Cost Cutter Limited-sumas
4111 GUIDE MERIDIAN 944 Cherry st
BELLINGHAM WA 98225 Sumas, WA 98341
Make Model Serial # Hourmeter
RAYMOND 2000 1G82ZH1576R2211704 0
Inst Date 90 Day 1 Year 3 Years 5 Years
3/21/94 6/21/94 3/21/95
Code Month Year Life
Total 106.68 685.16 685.16

 

Life
: to Date
Printer 1d : 8. 158.83
: 6. 136.33
FP3=Exit F12=Previous 3 0. 390.00

Enter Printer Id

 

 

revious F21=Print

O Enter a printer ID, or leave the prompt blank and the report will be printed on
the default printer for your User ID.


48 FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY

Unit Repair Cost History

A&R SALES & RENTALS Inquire/Update Service Units ‘VSNSDFR
Unit Repair Cost History

Make Model Serial # Hourmeter

RAYMOND 2000 1G8ZH1576RZ211704 -0

Inst Date 90 Day 1 Year 3 Years 5 Years

3/21/94 6/21/94 3/21/95

Code Month Year Life

_— Total 106.68 685.16 685.16
Sales Code current Year to Life

Month Date to Date

PS - PARTS SHOP 67.73 158.83 158.83

TC - LABOR CUSTOMER 38.95 136.33 136.33

TD - LABOR CUST MISC +00 390.00 390.00

F3=Exit F12=Previous F21=Print

 

 

O To print the unit's repair cost history for all owners, press F21=Print. See
previous page.


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

Labor Date
Labor Hours

Note Date

Note

FLEET MANAGEMENT GUIDE ¢ CUSTOMER SERVICE & UNIT HISTORY 49

Unit Service Information Screen: Field Definitions

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
Point of Sale Posting Batch (X55-1) if SM=¥ on
the Sold To screen at Point of Sale (X5-1) and SM
Due Type=H.

Dates (mmddyy)

90 Day

1 Year

3 Years

5 Years

10 characters. The document number is stored each
time parts are installed on a unit. It is displayed on
the Customer's Unit Repair History (F15=Parts
from Display Unit Service screen) and on the Unit
Repair History (F2=Unit History). It is displayed on
the Customer's Unit Repair History (F15=Parts
from Display Unit Service screen) and on the Unit
Repair History (F2=Unit History).

Date (mmddyy). Work date from the Sold To screen
at Point of Sale Invoicing (X5-1).

3.1 digits. Number of hours for maintenance. Unit
Service Information screen.

Date (mmddyy). Unit Service Information screen.
Date a note line was originally entered. Does not
change when the note is updated.

60 characters. Unlimited. The oldest 3 note lines are
displayed.


FLEET MANAGEMENT GUIDE * CUSTOMER SERVICE & UNIT HISTORY

Option

SM Begin

SM Due

SM Due Hr.

SM Due Type

Type the
number here

8 characters. Optional. User-defined option code. C
Options are set up in Unit Service Options Table
(X10.3-7). Press F4=Prompt for a list of valid
options.

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
(X55-1) if SM=Y on the Sold To screen at Point of
Sale (X5-1) and SM Due Type=H. Accepts 1
decimal place or enter 750 hours as 750 and press
[Field Exit]. Screen will display 750.0.

1 character. Indicates how service is scheduled. {
H=Hourmeter. Requires hours in SM Due Hr. field.
D=Date. Requires date in SM Due field.

The display depends on the type of workstation you
use. Ifyou work at a “green screen” or dumb
terminal, you will see the following selection:

 
     
   
 

2 1. Hourmeter
2. Date
. Blank

Type the number of the option you want in the
column to the left of Hourmeter, as illustrated.

Ifyou work at a PC, you will get the following
selection:

Highlight the
one you want
& press the
space bar

 


FLEET MANAGEMENT GUIDE « CUSTOMER SERVICE & UNIT HISTORY 51

SM End

SM Frequency

SM Prev

SM Prev Hr

SM Rate

SM Type

Use your mouse to click on the selection, or
move the highlighted bar with an arrow key, and
press the space bar to make your selection.

Date (mmddyy). Date scheduled maintenance
contract ends.

3.0 digits. Number of days between scheduled
maintenance daies, typically 30, 60, 90. The system
calculates the next date for scheduled maintenance
(SM Due) by adding the frequency to work date
from the most recent work order (SM Prev).

Date (mmddyy). Work date from the most recent
(Previous) work order. Updated by Create Point of
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
or ISM (inspection Service Maintenance).


52 FLEET MANAGEMENT GUIDE CUSTOMER SERVICE & UNIT HISTORY

Notes: