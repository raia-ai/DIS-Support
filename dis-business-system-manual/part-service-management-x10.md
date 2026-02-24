---
title: "PART: SERVICE MANAGEMENT (X10)"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about PART: SERVICE MANAGEMENT (X10)."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on PART: SERVICE MANAGEMENT (X10)."
---

---

## Page 1

- CHAPTER X10.2-1
SERVICE CUSTOMER TARGET LIST

### Introduction

With this option, you can selectively print a report or mailing labels for
service customers who:

Have a unit of a certain make, model or year

Purchased the unit during a certain time period

Need service by a particular date

Have a unit whose serial number is part of a recall or special
program

= Need a reminder to come in for a certain service job


[2] X10.2-1 SERVICE CUSTOMER TARGET LIST co

### Printing Service Customers

From the Service Reports Menu (X10-2), select option 1, Service
Customer Target List.

NW EQUIPMENT SALES Service Customer Target List XA210-101
Division: A Display Setup

Last Service Date .
Needs service
Needed Job

Service odometer ..

 

### Fields & Descriptions

The fields on the Setup for Report screen are described below in the order
in which they appear from left to right.

In defining the fields, a character is any character on your keyboard,

usually letters A-Z and numbers 0-9, but special characters such as "!"
*@" "#" can be used. Do NOT use the following characters: " " (blank)

RELEASE 2.3 LL


X10.2-1 SERVICE CUSTOMER TARGET LIST [2]

"," (Comma), "*" (asterisk), "/" (forward slash), "-" (dash or minus sign),
"+" (plus sign), ">" (greater than sign), "=" (equal sign), or "?" (question
mark).

A digit is any number from 0-9. Example: 5.2 D digits means 5 digits
with 2 fixed decimal places. 12345.67 is typed as 1234567.

Make 9 characters
Equipment make. See Inquire/Update Units
(X2-1).

Model 9 characters
Equipment model. See Inquire/Update Units
(X2-1).

Year 2.0 digits
Type range of years to search for. If only the
first year is entered that date will be used for
search.
1988 is entered as 88. Equipment year is set
up in Inquire/Update Units (X2-1).

Sale Date mmddyy
Type range of dates to search for. If only the
first date is entered that date will be used for
search. The date the unit was purchased sold
is automatically entered during posting, and
can be changed in Inquire/Update Units
(X2-1).

Last Service Date mmddyy
Type range of dates to search for. If only the
first date is entered that date will be used for
search. Date of last service is from most
recent repair order performed on this unit.

Needs service by mmddyy

SERVICE MANAGEMENT


[ «| X10.2-1 SERVICE CUSTOMER TARGET LIST

Needed job

Reminder date

Reminder job

Serial #

VIN
Address number
C Unit #

Odometer
Service Odomoter

Based on time since last service.

6 characters

Job code. If blank, will print if any job is
needed.

minddyy

Type range of reminder dates to search for.
If only the 1st date is entered that date will
be used for search. Must include this field if
reminder job is used. This date is entered in
Inquire/Update Service Units (X10.1-1).
mmddyy

Job code. Typed as reminder job code at
Inquire/Update Service Units (X10.1-1). If
blank, will include all reminders that fall
into the Reminder Date range.

17 characters

Type range of serial numbers to search for.
Set up in Units as serial number, or added in
Inquire/Update Service Units (X10.1-1).
Type range of VINs to search for. If only the
first VIN is entered, that VIN will be used
for search.

Type range of Address numbers to be
searched for. If only the first Number is
entered, that unit will be used for the search.
Type range of Customer Unit numbers to be
searched for. If only the first number is
entered, that unit will be used for the search.
Enter the range of miles to be used for.
Enter a mininum number of miles at the time
of service to be searched for.
CO


X10.2-1 SERVICE CUSTOMER TARGET LIST [=]

Any fields left blank will not be checked for the search. All fields with
values must match the unit's information to be included in the report. In
other words, each field you enter will further narrow the search to include
only those units that meet all selection criteria.

You may enter a partial name in the "Make" and "Model" fields. Typing
an "F" in the "Make" field will find Ford and Ferguson. An "FO" will find
only Ford. Similarly, if you type "76" in the "Model" field, you will find
7610, 7625 and 7636. As you type more characters, the search becomes
narrower.

If you need to cancel the job before printing, press [Cmd1] to retum to the
Service Marketing Menu.

Labels Setup

You may wish to run a report initially to verify your search, and then
switch to Labels Setup and press [Enter] again. This will eliminate the
possibility of wasting labels on incorrect searches.

When you enter the Print Service Customer option, the Report Setup

screen is displayed first. Press [Cmd4] to switch to the Labels Setup
screen. A sample follows shown below:

SERVICE MANAGEMENT


[ «| X10.2-1 SERVICE CUSTOMER TARGET LIST Cc

A & R SALES & LEASING CO Service Customer Target List ¥A310~102 2
Division: A Setup for Labels

Regular or Compressed Print Density (Ryc)
Number of Labels across Page a-4a
Number of Copies of Each Address Label (1-999)
Alphabetical or Zip Code Sort Order (az)
Print serial# on each label (ean)

Make ..
Model.
Year ..

Needs service by
Needed Job ...
Reminder Date
Reminder Job -

 

Cmd4-Setup for Report

 

### Fields & Descriptions

The fields on the Setup for Labels screen (XA300-102) are described
below in the order in which they appear from left to right.

In defining the fields, a character is any character on your keyboard,
usually letters A-Z and numbers 0-9, but special characters such as "!"
"@" "#" can be used. Do NOT use the following characters: “" (blank)
*," (comma), "*" (asterisk), "/" (forward slash), "-" (dash or minus sign),
"+" (plus sign), ">" (greater than sign), "=" (equal sign), or "?" (question
mark).

A digit is any number from 0-9. Example: 5.2 D digits means 5 digits
with 2 fixed decimal places. 12345.67 is typed as 1234567.

RELEASE 2.3 Cu


X10.2-1 SERVICE CUSTOMER TARGET LIST [7]

Regular or 1 character

Compressed Print Type R (regular - 10 CPI) or C Density
(compressed-15 CPI). If 4 labels wide is
selected, you must specify C. NOTE: Not
all printers support 15 CPI print density.
Please refer to your printer manual.

Number of labels 1.0 digit

Across page The number of labels wide to match your
current forms.

Number of Copies 3.0 digits

of Each Label Amount of times each label is to be copied.

Alphabetic or 1 character

Zip Code Order Type A to sort alphabetically by customer

name. If you have a Canadian postal code, a
‘P' will appear. Type P to select postal code

sort, Z to select zip code sort.
Print serial # 1 character
on each label Type ¥ to print serial numbers on each label.

Useful for fleet customers. Type N to
suppress printing of serial number.

Make 9 characters
Equipment make as set up in Inquire/Update
Units (X2-1).

Model 9 characters
Equipment model as set up in
Inquire/Update Units.

Year 2.0 digits
Type range of years to search for. If only the
first year is entered that date will be used for
search. 1988 is entered as 88. Equipment
year is set up in Inquire/Update Units.

SERVICE MANAGEMENT


Sale Date

Last Service Date

Needs Service by
Needed Job

Reminder Date

Reminder Job

Serial #

tomddyy

Type range of years to search for. If only the
first date is entered that date will be used for
search. The date the equipment was
purchased sold is automatically entered
during posting and can be changed in In-
quire/Update Units (X2-1).

minddyy

Type range of years to search for. If only the
first date is entered that date will be used for
search. Date of last service is from most
recent repair order performed on this unit.
mmddyy

Last day for service.

3 characters

If blank, will print label if any job is needed.
mmddyy

Type range of reminder dates to search for.
If only the first date is entered that date will
be used for search. Must include this field if
reminder job is used. This date is entered in
Inquire/Update Service Units (X10.1-1).

3 characters

Typed as reminder job code at
Inquire/Update Service Units (X10.1-1).

17 characters

Type range of serial numbers to search for.
Set up in Units as serial number, or added in
Inquire/Update Service Units (X10.1-1).
CL


X10.2-1 SERVICE CUSTOMER TARGET LIST [2]

Any fields left blank will not be checked for the search. All fields with
values must match the unit information to be included when the labels are
printed. In other words, each field you enter will further narrow the search
to print labels for only those units that meet all selection criteria.

You may enter a partial name in the "Make" and "Model" fields. Typing
an “F" in the "Make" field will find Ford and Ferguson. An "FO" will find
only Ford. Similarly, if you type "76" in the "Model" field, you will find
7610, 7625 and 7636. As you type more characters, the search becomes
narrower.

If you need to cancel the job before printing, press [Cmd1] to return to the
Service Management menu.

Running the Job

Press [Enter] after filling in the fields you want included in the search. The
labels or report will be sent to the job queue. You may then change your
selection fields and request another report or set of labels, or press [Cmd1]
to end the job.

You will receive a message at your work station telling you:

a) Your report or label run is complete and has been sent to the
print spool,

OR

b) No unit was found that matched all of your selection fields.

SERVICE MANAGEMENT


Notes: oo

RELEASE 2.3 LL

## CHAPTER X10.2-2

SERVICE LABOR ANALYSIS

### Introduction

Service Labor Analysis includes only labor lines that have been placed on
a work order in connection with a standard job. By contrast, the Labor
Analysis Report on the Point of Sale Report Menu (X56-4) includes all
labor lines. Both reports use figures that are available since the last cutoff
date used for Point of Sale End of Month (X5-4).

Service Labor Analysis helps you compare the performance of the
mechanics relative to flat rates, By scanning the column labeled
"Reported" and "% Flat" for percentages greater than 100%, you can spot
times that are consistently more than the flat rate provides for.

### How To Run

From the Service Reports Menu (X10-2), select option 2, Service Labor
Analysis. After the service security gate, the report is placed on the job
queue,


An example of the Service Labor Analysis Report follows:

A&R SRLZS & LEASING COMPAHY SERVICE LABOR ANALYSTS REPORT nate 11/05/92
BELLINGHAM, WA . ‘Time 11.53.47

Employee seseeens Hours serceee ae: ise Reported =-=~ Bilas

Customer Name pate Plat Report Billed € Bill ft Flac § Spl % Shop Plat
+ gEM TROUTHRN
AINEKSON COUNTY © wo08795 10/20/92 3. . 50 109.09
JACKSON COUNTY © woos795 11/02/92
JACKSON COUNTY © woos79s 10/21/92

JACKSON COUNTY © woon797 10/20/92

= customer Teta?
‘+ Employee eral

Totals for Division & * Customer Totals
+ ancerna? Totate

s+ Grand toral

### Fields & Descriptions

The fields on the Service Labor Analysis Report are described below.

Employee * Mechanic's name.

Customer Name For internal documents, the unit number is
used in this field.

Document Repair order number. The number is
CC


Date

Hours
Flat
Report
Billed

Reported
% Bill

% Flat

% Empl

% Shop

Bill/Plat

SERVICE MANAGEMENT

X10.2-2 SERVICE LABOR ANALYSIS. [2]

preceded by a “C" for customer repair
orders, by "I" for internal repair orders.
mm/dd/yy. Date repair order was opened.

Flat rate hours from the job code table.
Actual hours reported.
Actuai hours billed.

Percentage of hours reported that were
billed. Calculated by dividing "Hours
Report" by "Hours Billed.”

Percentage of hours reported that were
allowed by the flat rate. Calculated by
dividing "Hours Report" by "Hours Flat."
Look for over 100%, which means more
time was spent on the job than is covered by
the flat rate.

Percentage of mechanic's time that was
spent on this job. Calculated by dividing
“Employee Total Reported" by "Hours
Report."

Percentage of total shop hours for the
division that were contributed by this
mechanic. Calculated by dividing
“Employee Total Report" by "Division Total
Report."

Percentage of hours billed that were allowed
by the flat rate. Calculated by dividing
“Hours Billed” by "Hours Flat." Look for
less than 100%, which means that fewer
hours were billed than were allowed. More


[| X10.2-2 SERVICE LABOR ANALYSIS

than 100% would mean that more time was
billed than was allowed by the flat rate.

Gross
Amount Extended amount of labor charge.
Calculated by multiplying the billed hours
by the labor rate.
%Total Calculated by dividing the extended amount

of labor charge on the current line by the
Grand Total of extended labor for the
division.

Note:

Remember that the Gross Amounts and Grand Totals for the Division
represent only labor lines that are associated with job codes. For more
comprehensive, more accurate figures, see the Labor Analysis Report

(X56-4).

Also keep in mind that the report is based on figures that have
accumulated since the last cutoff date used for Point of Sale End of
Month (X5-4).

 

## CHAPTER X10.2-3

STANDARD JOB REPORT

### Introduction

The Standard Job Report makes it possible for you to review a range of
groups and/or jobs. The report can be displayed on screen or printed on the
system printer. You can request full detail or a summary only.

### How To Run

From the Service Reports Menu (X10-2), select option 3, Standard Jobs
Report. The following prompt is displayed: "Display the standard job
teport (Y/N)?"

C1 To display the report on screen, accept the default Y, or to print the
report on the system printer, change the default to N. A selection screen
appears, as illustrated:

ABC-AG,AUTO,CONS & TRUCK CO. STANDARD JOB REPORT ¥A230-001
Division: ALL Display options

Group code
Job code

Print detail (y/N). ¥

Cndl-End job

 

O To display or print all standard jobs, leave the fields blank; otherwise,


[| X10.2-3 STANDARD JOB REPORT Cc

select a range of groups and/or jobs.
If you want all detail, accept the default of Y; otherwise, type N to
receive a summary only.

 

 

 

 

Examples of the Standard Job Report with and without detail follow.
First, the report with detail is illustrated:

RELEASE 2.3 CU


ABC-AG.AUTO,CONS & TRUCK CO.

CRSHA Name: THANK YOU FOR YOUR BUSINESS

Group code: @RADOL Name: BILL BRADLEY
TD Qty Description -

PARTS CUSTOHER
a 3 cRS A25623,

Group code: BRADO1 Name:
>
Growp code: BRAD1 Name:
oD

Group code: PALHO1 Name: RUTH PALMER
TD Qty Description

Group code: 5000

Name: GROUP CODE FOR Sto JOBS
TD Gy Description ---~
‘PARTS. SHOP
? 4 cas 11429
t 2 CAS A2se1a
. @ CAS anLBi2 sc1a2
‘* oral PART:
PARTS SHOP MISC
1 BRACKET
Group code: 5000 Name: GROUP CODE FOR STD JOBS
7D Qty Description
PARTS SHOP
r 1 CAS Ag1245, OTL Fluren 2n21
T 2 cas aniez3 SEAL 5B92


‘STANDARD JOB REPORT

Jab code: JEFF
Price Amount
JOBCODEA Job code a
‘Amount,

2.61 7.83
Subcotal 7.83
Sales tax

Job code: JoRconE3
Price

Price
Job code: 1048BR
Price Anount

2.62 10.48
119 2.38

17.07 68.28

'3. SHOP eid

104.67 104.67

Subtotal 285.81

Sales tax 18.58

‘Total $204.39

Job code: 1048012 OX CHANGE
Price amount

19.98 19.96
6.59 13,18

+* moral parts sor 33.36

PARTS SHOP MISC
? 6 QUARTS PEMZOZL

 

SERVICE MANAGEMENT

2.58 15.48
‘subtotal 48.64
Sales tax 4.86
Tozal $53.50

REPLACE BRACKET

Pate 1/24/93
Time 9.42.28

racer

Flat rate:

 

Page 1
xa2302-01

39.00

1.00


An example of the same Standard Job Report without detail follows.

ABC-AG,AUTO,CONS & TRUCK CO. Date 1/14/93 Page 1
BELLINGHAM, WA mime 9.42.30 xA2302-01

Job code: JEFF
Meme: BILL BRADLEY gob code: JOBCODEA Job cade A Plat rate:
+ qotal PARTS CUSTOMER 7.83

Flat rate:
Flat rate:

Plae rate:
Group code: 5000 Name: GROUP CODE FOR STD JOBS Plat rate
#8 Total PARTS SHOP
‘+ motel PARTS SHOP MISC 104.67
** subtotal 185.82 -
++ gales tax 18.58 {
+ Total $204.39
‘Group CODz FOR STD TORS dob code: 1048072 OTL CHANGE
s+ Total PARTS SHOP 33,18
‘+ gotal PARTS SHOP MISC 15.48
+ subcoral, 48.66
s+ sales tax 4.06
+ gorat $53.50

 

RELEASE 2.3 CO

## CHAPTER X10.2-4

SERVICE HISTORY REPORT

### Introduction

The Service History Report is especially helpful for reviewing
maintenance for a fleet customer. If you want to review the service history
of one unit in a fleet, it is easier and quicker to take a printkey [Cmd5]-
Service History from Inquire/Update Units (X10.1-1), which displays the
same information. The report can be displayed or printed.

### How To Run

From the Service Reports Menu (X10-2), select option 4, Service History
Report. After the service security gate, the Report Options screen appears.

ABC-AG,AUTO,CONS & TRUCK C SERVICE HISTORY REPORT ‘¥a240-101 2
Division: A Display Report Options

Unit Make
Selection:
Year
Sale Date
Serial# ..
¢ unit# ..
Hourmeter ...

Last Service Date .

Needs service
Needed Jab ..

Historical
Service Job code group
Selection: Job code

Print detail lines? ¥

Gmdl-End Job

 

To cancel your request, press [Cmd1]; otherwise, make your selections
and press [Enter]. The report is placed on the job queue. An example of
the Service History Report follows:


asc Company
BELLINGHAM,

SEAVICE HISTORY REPORT Dare 11/06/92

Time 12.58.03

Closed: 11/06/92 By: oIM
Hourmeter:

BURKOO Name: RICHARD BURKIN
6901A-69034-SS0F Make: COASTLINE Mode):

w008798

cy Description
STANDARD CODE
ROM: 10498
ROM: 1049071,

$000
3000
3000
JOB:1048BR 5000
PARTS.

1 vw vs2aoe
STANDARD CODE
30B:1048012 5000
PARTS.

2 ww v26018

1 “Ww v34890

acy peseription
MISC PARTS

1 OIL FILTER
LABOR-OTHER

o 400

Address#: 306341 Name:

Serial#: 1266xA

CASE,
IN? PARTS-SHOP

Vw APART
STANDARD CODE,
yoa:30n19 230
misc. cost

nate 11/03/92

2.50 replace bracket
-78 oi change

1.75 WINTERIZATION
1.50 replace bracket

BRACKET.
.75 of change

GASKET 2.02
6.39
s+ gotal PARTS
++ subtoral
“+ sales rax
++ total

Price
$7.20
Employee oT 80.00

Subtotal
++ total

JACKSON COUNTY

004.00 = STD JoB DESC FOR CASB/cOBOL*

APART ‘srace

OTL - 8 QUARTS

4.04
6.39
10.43
120.43
9.39
$229.82

grood10

Amount,
57.20
20.00

137.20
$137.20

woo8764

Warrant:

Clesed:
Hourmeres:

ay: JIM PO: Summary Decument
3200.5 warranty:

Closed: 11/02/92 By: JH
Hourmeter! Warranty:

 

## CHAPTER X10.2-5

SCHEDULED MAINTENANCE DUE

### Introduction

Use this report to print a list of units that have scheduled maintenance due
by a selected date or within a selected hourmeter reading. The report is
divisional and uses the division code entered at the security gate.

### How To Run

O From the Service Report Menu (X10-2), select option 5, Scheduled
Maintenance Due.

‘A ARR EQUIPMENT SALES Fleet Management Report
Schedule Maintenance Due

Mt yy
Units Due By ____ Month/Year
or
units within __ —_ Hourmeter

Printer 1D

F3=Exit  F12=Previous


Sample Report

AER EQUIPMENT SALES MAINTENANCE DCE 12/29/97 Page
LYNDEN, WA 14:14:25 VSMSPFR

UNITS DUE BY: January OR WITHIN 100 HOURS

HIMHARO WHOLESALE BURLINGTON

sensor

KeY HAP ASE
BURLINGTON WA 98233 RAE BARNES 360 650 = S409
OPEN 7:00 CLOSE 6:30

SPECINL INSTRUCTIONS: Renews annually - contact in June

SH DUE SH DUB LABOR ¢ ANOMtT OPTrON
MEER DATE HOURS
4701/97
2.5 55.00 TECH?

1.8 CUSTOMER'S § AMOUNT 58.00

 
CC

## CHAPTER X10.2-6

SCHEDULED MAINTENANCE OVERDUE

### Introduction

Use this report to print a list of units that have scheduled maintenance
overdue. The report is divisional and uses the division code entered at the
security gate.

‘HOW TO RUN

5 From the Service Report Menu (X10-2), select option 6, Scheduled
Maintenance Overdue.

A AGR EQUIPMENT SALES Fleet Management Report

Print Schedule Maintenance overdue

Printer ID PRTOL <-- Use AS/400 name
or output queue

F3=Exit  F12=Previous


Sample Report

A&R EQUIPMENT SALES 12/30/97 Page
MINHARO WHOLESALE BURLINGTON

BURLINGTON WA 98233 360 650 - 5489
OPEN 7:00 CLOSE 18:30

SPECIAL INSTRUCTIONS: Renews annually - contact in June

SM DUE SM DUE LABOR $ AMOUNT OPTION
METER =‘ DATE HOURS
4/01/97
55.00 TECH2

CUSTOMER'S # UNITS 1 CUSTOMER LBR HRS 1.5 CUSTOMER'S $ AMOUNT 55.00

+++ Report interrupted to show total line ***

TOTAL # OF UNITS 9 TOTAL LABOR HOURS 27.8 TOTAL $ AMOUNT 1091.23

 

RELEASE 2.3 LU

## CHAPTER X10.2-7

SCHEDULED MAINTENANCE CONTRACTS ENDING

### Introduction

Use this option to print a list of contracts that will end in a selected month.

### How To Run

O From the Service Report Menu (X10-2), select option 7, Scheduled
Maintenance Contracts Ending.

Selection Screen

Fleet Managment Report
Contracts Ending

MM YY
Contracts Ending _ __

Printer ID . . <-- Use AS/400 name

Or output queve

F3eExit F2=Previous


Sample Report

AER SALES @ RENTALS
BELLINGHAM, WA

WILDTAM ADAMS

Rr 2, BOK 933,
ARLINGTON, WA 98223,

DIV SERIAL 4

‘A 11112567777

‘TOTAL NUMBER OP UNITS


Scheduled Maine znd 4727799 Page 1
12:08:49 VSNIPFR

CONTRACTS ENDING IN May

ApaMO.

JOE CONTACT 360 211 = 1278

EQUIPE OPTION GRE

SCH MAINT $M RATE PREQ
END DATE
0 8701700 © 55.0060

## CHAPTER X10.2-8

SCHEDULED MAINTENANCE SUMMARY

### Introduction

The purpose of this report, which is divisional, is to calculate the annual
value and number of labor hours represented by contracts in a selected
time period.

 

NOTE
To be included on this report, the scheduled maintenance must begin on or
before the first date and end on or after the second date. In other words,
the report lists contracts that are in force throughout the entire date range
ou specify.

In the example below, any contract that began in 1996 and ends in 1998
will be included. A contract that began in March 1997 and ends in March
1998 will not be included.

If you enter the same date in both fields, the report will show all contracts
valid on that date, regardless of beginning and ending dates.


[| X10.2-8 SCHEDULED MAINTENANCE SUMMARY Co

### How To Run

O From the Service Report Menu (X10-2), select option 8, Scheduled
Maintenance Summary.

Selection Screen

A-A&R EQUIPMENT SALES Print Scheduled Maintenance Summary

Include units with Service Maintenance Contracts valid
throughout the following range: to (

Contract Number . {Leave blank for All)

Printer Id <-- Use AS/400 name
Or output queve

F3=Exit F12=Previous

 

Units can be listed using only a date range or a date range plus a contract
number. To include all contracts, leave the Contract Number blank, To be
included on this report, the scheduled maintenance must begin on or
before the first date and end on or after the second date.

CL


X10.2-8 SCHEDULED MAINTENANCE SUMMARY [2]

Sample Report
A&R SALES & RENTALS Maintenance Summary 4/27/99 Page 1
BELLINGHAM, WA 11:19:56 VSNLPFR

Begin Date 1/01/98 End Date 1/01/99
Contract Number 123

MODEL ANNUAL VALUE ANNUAL LABOR HOURS

1 800.00 20.0

1 800.00 20.0

 

Note that if a Contract Number is specified, it is printed on this report.

Calculations:

Units Quantity of each model on Scheduled Maintenance list.
Model Model number.

Value (SM Rate + Consumables) X Frequency

Frequency = (365/Days) rounded to nearest whole number
Labor Hours Labor Hours X Frequency
Frequency = (365/Days) rounded to nearest whole number

SERVICE MANAGEMENT


Notes:

## CHAPTER X10.2-9

SCHEDULED MAINTENANCE LIST

### Introduction

This report, which is divisional, lists units that have current contracts for
scheduled maintenance along with terms, options, etc.

### How To Run

O From the Service Report Menu (X10-2), select option 9, Scheduled
Maintenance List.

Selection Screen

Scheduled Maintenance List
print Scheduled Maintenance List

Leave contract number blank for ALL
Contract Number .
Printer Id <-- Use AS/400 name
or output queve

F3-Exit F12=Previous


Sample Report

Schedule Maint List

WILLIAM ADAMS

RT 2, BOK 933
ARLINGTON, WA 98223

SERIAL # EQUIP # DUE METER DUE DATE OPTION

11112567777 8/01/99

1HDLDBL19GY502347 10/01/99

SERIAL @ EQUIP # DUE METER DUE DATE OPTION

343434 9/01/98

we
123456 11/03/98

ar

4/29/99 Page
12:59:22 VSNXPER

360 111 - 1278

SM RATE LABOR CONS
HOURS RATE

$5.00 3.6 5.00

45.00 4.5 5.00

360 67L - 1234

SM RATE LABOR CONS
HOURS RATE

:0  -00

5.5

 

## CHAPTER X10.2-10

PARTS HISTORY REPORT

### Introduction

This report lists parts installed on a particular unit for a single owner or for
all owners.

### How To Run

© From the Service Report Menu (X10-2), select option 10, Parts History
Report.

Selection Screen

A ARR SALES & RENTALS Print Unit Repair History

Enter a Customer Address Number to report for only one customer

Serial # — 1G82H1576Rz211704
Address # cosTo1
Printer ID PRTO1 <-- Use AS/400 name

Or output queue

F3-Exit Fd=Prompt F12=Previous

 

O Enter a serial number and customer address number, or, to get a report
of costs that includes all owners, leave the Address # prompt blank.

DB Enter a printer ID, or leave the prompt blank to allow the report to go to
the printer or output queue associated with your User ID.

© Press [Enter]. The following message is displayed: “Unit Repair
History submitted to print."

Sample Report

The report illustrated below is for a single owner only: the title is "UNIT
REPAIR HISTORY." The title of the report for all owners is: "UNIT
REPAIR HISTORY TOTAL."

AAGR SALES & RENTALS unit Repair History pate 3/22/94
BELLINGHAM. WA B ‘mime 40:53:22 .
Heke Model -Sexial # our veter Install 90 Day 1 Year 3 Years 5 Years ¢
Date
RavMaND — 2000 1g82H1576R2211708 03/21/94 6/21/94 3/22/95
‘Vendor Wour Laner ‘Invoice
Meter Date W/o Number

2 1is¢-065 pay ‘254.0 3/21/94 sMOsO2e

4 1150-065 RAY 21.0 3/15/94 suo9022

2 454-010-210 1501.0 9/23/94 sv99026

1 590-096 1907.0 6/30/94 SK09025
2 632-043-004 2467-0 12/21/94 SM09027
1. 632-043-001 1007-¢ 6/30/94 sH09025
1 632-043-001 Bild 3/25/94 sm09022

+ BND OP REPORT **

 

RELEASE 2.3 LU

## CHAPTER X10.2-11

UNIT COST REPORT

### Introduction

This report lists costs associated with a particular unit for all sales codes or
up to 12 selected sales codes, which will be “remembered” and defaulted
the next time the report is run. It can be printed for a single owner only or
for all owners.

### How To Run

0 From the Service Report Menu (X10-2), select option 11, Unit Cost
Report.

Selection Screen
‘A CLARKLIFT OF WA Print Unit Cost

Serial # 1G8ZH1576R2211704
Address # COSTOL

Sales code 1
Sales code 2
Sales code 3
Sales code 4
Sales code 5
Sales code 6
Sales code 7
Sales code 8
Sales code 9
Sales code 10
Sales code 11
Sales code 12

TPIT FFF

Printer ID PRTO1, <-- Use AS/400 name
Or output queue

Fi=Exit Fd=Prompt F2=Previous


[2 | X10.2-11 UNIT COST REPORT Cc

O Enter a serial number and customer address number, or leave the
customer address blank to print costs associated with all owners.

© To select from a list of customer address numbers and serial numbers,
press F4=Prompt from either field.

0 Enter 1-12 sales codes or leave blank for all sales codes.

O To select from a list of sales codes, press F4=Prompt.

O Enter a printer ID, or leave the prompt blank to allow the report to go to
the default printer associated with your User ID.

Press [Enter]. The following message is displayed: “Unit Cost Report
submitted to print." The Print Unit Cost screen remains so you can
request other reports as desired.

© When you are done, press F3=Exit or F12=Previous to return to the
Service Reports Menu.

RELEASE 2.3 LC


Sample Report

The report illustrated below is for a single owner. Its title is "UNIT
REPAIR COST." The report for all owners is "UNIT COST HISTORY
TOTAL."

AER SALES & RENTALS unit Repair Cost Date 3/21/94 Page 1

   

BELLINGHAM, WA a Time 11:43:59 USMGPR
veke Model_——sSerial # Moar Meter Install 90 ney 1 Year 3 Years 5 Years
pace
Rarwond 2000 «© LG8ZH1576R2211704 a avaiy9a 6/2as94 3/21/95
Sales Seles code current Life
Description Month to pate
PARTS SHOP 67.93 158.83

LABOR CUSTOMER 38.95 136.33

LABOR CUST MISC : 390.00

Final Totals 685,16

+ END OP REPORT **

SERVICE MANAGEMENT


Notes:

## CHAPTER X10.2-12

OPTIONS FILE LIST

### Introduction

The Options File List is a printout of current service options, which are
user-defined. Options are set up in Maintain Service Options (X3.10-12).
They are assigned to units on the Unit Service Information Screen, where
a list of valid options is available by pressing F4=Prompt. See CHAPTER
X3.10-12, MAINTAIN SERVICE OPTIONS.

### How To Run

O From the Service Report Menu (X10-2), select option 12, Options File
List.

Selection Screen

Options Table Dump
Print Options File

Printer Id PRTC1. <-- Use AS/400 name
Or output queue

F3-Exit Fi2=Previous


[| X10.2-12 OPTIONS FILE LIST C

Sample Report

CLARKLIFT OF WASHINGTON options List Dete a/iisse
BELLINGHAM, WA a Pime 8:31:19

Option Option Peseription
code

INTSLL2 Intelligent Machine
wo Wire Guidance

 

Lo

## CHAPTER X10.2-13

WARRANTIES FILE LIST

### Introduction

The Warranties File List is a printout of current part numbers that carry a
warranty different from the default number of days. These are the parts
that have been entered in Maintain Parts Warranty (X10.3-13). The default
is also set in Maintain Parts Warranty.

### How To Run

G From the Service Report Menu (X10-2), select option 13, Warranties
File List.

Selection Screen

ANORTHWESTTRUCK = Warranty Table Dump
Print Warranty File

Printer Id PRTO!___<-- Use AS/400 name
Or output queue

F3=Exit F12=Previous


Sample Report

CLARKLIFT OF WASHINGTON INC. wazranty File pate 2/08/94 Page

BELLINGEN, WA a Time 14:16:40 VENEPFR
Vendor Part # piv Warranty
## of bays,

10726 370
at1i90 370
ATG 500
0369 500
30613, 500
aass3 500
34057 500
01s 500
72376 800
Rms so -

 

RELEASE 2.3 LL

## CHAPTER X10.3-1

INQUIRE/UPDATE SERVICE TABLES

### Introduction

A service table is an intermediate device that combines standard jobs (the
Group:Job created at Point of Sale) before they can be assigned to a
particular Make/Model and available for automatic inclusion in
recommended maintenance. The most straightforward technique is to
name your tables the same as your groups, although this is not required.

Group:Jobs can be deleted from recommended maintenance, and other
Group:Jobs can be added; however, service tables make it possible to
make sure jobs are added accurately and on schedule.

The steps are:

O Create standard jobs at Point of Sale. When you select Standard Jobs
mode, the address number used on the entrance screen is the group
name and the document number you assign is the job name. Every
standard job can then be referred to as a Group:Job.

 

Assign Group:Jobs to tables, usually with the same names as the groups
Cnquire/Update Service Tables, X10.3-1).

 

 

 

 

Link equipment to tables according to make, model, years or series
code. (Inquire/Update Make Model Assignments, X10.3-2).

 

U1 Tables of Group:Job combinations are automatically included in
recommended maintenance, which is available from Inquire/Update
Service Units (X10-1) or from Point of Sale (X5-1, [Cmd18]).

For more information, see CHAPTERS X10 and X10.3-2, SERVICE
MANAGEMENT MENU and INQUIRE/UPDATE MAKE MODEL
ASSIGNMENTS, and CHAPTER X5-1, POINT OF SALE INVOICING.


[| X10.3-1 INQUIRE/UPDATE SERVICE TABLES c

### How To Run

From the Service Utilities Menu (X10-3), select option 1, Inquire/Update
Service Tables. The Service Table prompt and a list of current tables

appear.

ABC COMPANY Inquire/Update Service Tables xA310-101 1
Division: L

Service Table: Enter name or select from list

Current Service Tables

“x! to Select
‘c! to Copy

default
T0642
7000

 

RELEASE 2.3 LL


X10.3-1 INQUIRE/UPDATE SERVICE TABLES [=]

Adding a Service Table

Type the name (up to 6 characters) for the new service table in the
"Service Table" field. Press [Enter]. The words "New Table" will display
in the upper right hand comer of the detail jobs screen.

 

In this example, a new service table named "5000" is started. The detail
jobs screen is illustrated below:

ABC COMPANY Inquire/Update Service Tables XA310-102
Division: L New Table

Service Table: 5000

Del Interval
D Group Job Description Mo ur

cmdi-End © cmd3-Go back cCmd8-Get job codes Cmd19-Delete this table

 

SERVICE MANAGEMENT


[ «| X10.3-1 INQUIRE/UPDATE SERVICE TABLES

[Cmd8}-Get Job Codes

To add standard jobs to the table, press [Cmd8]-Get Job Codes to display
jobs in a window at the right of the screen. Jobs associated with the default
group are displayed first. The standard alphanumerical sort order is used:
1) Special characters, 2) Letters, 3) Numbers.

ABC COMPANY Inquire/Update Service Tables XA310-102
Division: L New Table

Service Table: 5000

Del Interval Est. Price
DGroup Job Description Mo Rr Labor Hours

Group Job Description 4
% 5000 1048BR replace bracket
% 5000 10480IL oii change (
580C  JOBOZ
580¢ JoB10
soc gopéd = 15 Hr tune
S92C JOBXX OIL, & FILTER CHANGE.
7777 32137 exhaust pipe blowout
7777 44011
KOS5149 TVS3091 ¢371008418

Next page> Group: *JOBS Job: JoBY
(md8-Include selected job codes

qm@i-End © Cmd3-Go back Cmd8-Get job codes Cmdl9-pelete this table

 

O Place any character next to the job codes to be included in the service
table. An '"X" is used in the example illustrated above. Press [Enter] to
register your choice.

O To display the next page of jobs, if any, press [Enter].

 

 

 

If your list of jobs is long, you may change "Next page>" to the group

 

RELEASE 2.3 CO


X10.3-1 INQUIRE/UPDATE SERVICE TABLES |

and job you want, and press [Enter].

[Cmd8]include selected job codes
Press [Cmd8] to include the marked job codes in the service table. The
following screen is displayed:

ABC COMPANY Inquire/Update Service Tables XA310-102
Division: L New Table

Service Table: 5000

Del Interval Est. Price

DGroup Job Description Mo Hr nabor Hours
5000 1048BR replace bracket 6 60.00 1.50
5000  104801L oil change 3 30.00 78

cmd3-Go back Cmd8-Get job codes Cmdl9-pelete this table

 

1 Complete the service table by filling in the service intervals.

 

 

 

To add another table, press [Cmd3]-Go back. The table that was just
completed is added to the columns of existing service tables in
alphabetical order under "Current Service Tables." The name of the
service table set up most recently is displayed in the "Service Table"
field. Type the name of the table to be created over the name of the

 

SERVICE MANAGEMENT


[ «| X10.3-1 INQUIRE/UPDATE SERVICE TABLES ~

previous table. Press [Enter]. Fill in the appropriate fields.

### Fields And Descriptions

The fields on the Inquire/Update Service Tables screen are described
below in the order in which they appear from left to right:

In defining the fields, a character is any character on your keyboard,
usually letters A-Z and numbers 0-9, but special characters such as "!"
“@" "#" can be used. Do NOT use the following characters: "" (blank)

"\" (comma), "*" (asterisk), "/" (forward slash), "-" (dash or minus sign), (
"+" (plus sign), ">" (greater than sign), "=" (equal sign), or "?" (question
mark).

A digit is any number from 0-9. Example: 5.2 D digits means S digits
with 2 fixed decimal places. 12345.67 is typed as 1234567.

Del 1 character
D To delete a job, enter D.
Group 6 characters

Group name: the address number used at
Point of Sale when the standard job was

created.
Job 10 characters
The document number used at Point of Sale when
the standard job was created.
Description 30 characters

Description of the standard job furnished on the
Sold To screen at Point of Sale when the standard

RELEASE 2.3 LO


X10.3-1 INQUIRE/UPDATE SERVICE TABLES [7]

job was created.
Interval

Mo 2.0 digits
Recommended interval (in months) after which this
type of vehicle is to have the service job. 14 months
is entered as 14.

Hr 5.0 digits
Recommended interval in operating hours for this
piece of equipment. Unlike the hourmeter entry on
the Point of Sale Sold-to screen (which has a place
for 10ths of hours), do NOT assume any decimal
places for this field. For example, if you wished to
enter a maintenance interval of 125 hours, you
would simply enter "125" into this column.

Est. Price

Labor 7.2 digits
Price of the labor caiculated by multiplying the
Default Labor Hourly Rate from the Divisional
Profile by the Standard Job Flat Rate that was
furnished on the Sold To screen at POS when the
standard job was created.

Hours 7.2 digits
The Standard Job Flat Rate, usually the same as the
manufacturer's flat rate time, that was furnished on
the Sold To screen at POS when the standard job
was created. Four and a half hours is displayed as
450.

SERVICE MANAGEMENT


X10.3-1 INQUIRE/UPDATE SERVICE TABLES C

### Changing A Service Table

O Start at the Service Table prompts. From the Inquire/Update Service
Tables screen, press [Cmd3]-Go Back to return to the Service Table
prompts.

O Type the name of the table you want to change, or type a character next
to the table you want to work with. The table is displayed. The words
"Current Table" are displayed in the upper right hand corner.

 

 

 

Make any changes or additions necessary. Press [Enter] to update. To
delete job codes from the table, place a "D" in the Delete column next
to the codes. Press [Enter].

 


X10.3-1 INQUIRE/UPDATE SERVICE TABLES [>]

### Copying A Service Table

You may have different types of equipment that require almost the same
maintenance. For example, tractors may have the same service schedule as
backhoes with the exception of Oil and Filter change intervals. Rather than
type a new table for tractors, copy the codes from the tractor table to the
backhoe table. Then customize the new backhoe table to fit the needs of
backhoes.

Type "C" next to the name of the table you want to copy at the list of
Current Service Tables on the Inquire/Update Service Tables screen. The
following screen appears:

ABC COMPANY Service Schedules XA200-113
Division A Copy Tables

Copy From Table TRACTOR
To Table BACKHOE Updating existing Job Codes? (¥/N) N

Current Service Tables

 

To Table
Fill in the name of the new table which will contain the codes from the
Tractor table.

SERVICE MANAGEMENT


X10.3-1 INQUIRE/UPDATE SERVICE TABLES CC

Updating existing Job Codes? (Y/N)
If you want to copy only the codes on the "From Table” that do not exist
on the "To Table," type N (No).

If both tables have codes that are the same, and you want to update the
codes on the "To Table" with the codes on the "From Table", type Y
(Yes).

Press [Enter]. If you used the name of an existing "To table," it will be

updated with information contained on the From Table. If you used a new
name in the "To Table" field, a new table is created.

### Deleting A Service Table

 

 

 

Select the table and display it on the Inquire/Update Service Tables
screen.

 

O Press [Cmd19]-Delete this table.

Note

 

The service table will not be deleted if any vehicles have been assigned
H} to it.

RELEASE 2.3 oe


X10.3-1 INQUIRE/UPDATE SERVICE TABLES [“]

### Setting Up A Default Table

Sometimes a customer brings in a piece of equipment that you do not sell
or usually service. This vehicle may not match any make, model, or year
assignments in the service tables. But, it would be nice to be able to show
some kind of recommended maintenance schedule to the customer.

Think of the default service table as a "catch-all" which will be used when
no others match. The information in the default table will be general
maintenance guidelines that apply to most equipment.

To create the default table, place an X next to "default" in the table list.
Press [Enter]. Fill in the fields on the default service table.

SERVICE MANAGEMENT


Cc

[| X10.3-1 INQUIRE/UPDATE SERVICE TABLES

### Printing Service Tables

To print a list of service tables, press [Cmd1] to end the job. The following
screen is displayed:

AUSTIN TRACTOR & EQUIPMENT Service Schedules XA220-107 7
Division: A print Reports

Print Service Tables (Y/N)... N

Cmdl-fnd cmd3-Go back Enter to continue

 

If you want to:

= end the job and return to the Service Utilities Menu, press [Cmd1].
™ go back to the Service Tables prompt, press [Cmd3].

= return to the Service Utilities Menu without printing, press [Enter].
= print the service tables and return to the Service Schedules Menu,
type: Y, and press [Enter].

RELEASE 2.3 Lo


INQUIRE/UPDATE SERVICE TABLES

An example of a Service Tables printout follows.

ABC COMPANY Service Tables Date 11/04/92 Page 1
Division: L ‘Pime 11.05.50 XA310-24,

Service Bst. Price

Table Code-. Description Labor Hours

5000 10sasR $000 replace bracket 60.00 1.50
104601L 5000 of1 change 30.00 -15

s80c JOBS) “JOBS winterization 130.00 3.25
CASTROL OILCHG oil & grease job 40.00 1.00
PENNZ —OTLCHG of} & grease 60.00 1.50
SEARS OTLCHG of] & grease 50.00 2.25
yoss4  980C «15 Mr tune 100.00 2.50
goB26 306341 standard 50 br tune 130.00 3.25

 

SERVICE MANAGEMENT


Notes:

## CHAPTER X10.3-2

INQUIRE/UPDATE MAKE MODEL ASSIGNMENTS

### Introduction

Use this job to assign vehicles to service tables according to make, model,
year or range of years (or series codes). This is necessary to enable the
system to furnish jobs for recommended maintenance automatically.

The steps are:

 

C1 Create standard jobs at Point of Sale. When you select Standard Jobs
mode, the address number used on the entrance screen is the group
name and the document number you assign is the job name. Every
standard job can then be referred to as a Group:Job.

C1 Assign Group:Jobs to tables, usually with the same names as the groups
(Inquire/Update Service Tables, X10.3-1).

 

 

Link equipment to tables according to make, model, years or series
(nquire/Update Make Model Assignments, X10.3-2).

 

 

 

 

Tables of Group:Job combinations are automatically included in
recommended maintenance, which is available from Inquire/Update
Service Units (X10-1) or from Point of Sale (X5-1, [Cmd18]).

For more information, see CHAPTERS X10 and X10.3-1, SERVICE
MANAGEMENT MENU and INQUIRE/UPDATE SERVICE TABLES,
and CHAPTER X5-1, POINT OF SALE INVOICING.

Equipment can be assigned to service tables in the following ways (a
series code may be used instead of year):

= Specific make, model and year (or range of years or series).
Example: Ford 7610 '83-'87.

= Make and model are given with no year (or series). Example: Ford
7610 (leave year/series blank to indicate all years/series of New
Holland 680).


[| X10.3-2 INQUIRE/UPDATE MAKE MODEL ASSIGNMENTS _

= Make and year (range of years or series) with no model. Example:

Ford '64-'68 (leave model blank to indicate all models of Ford
vehicles from 1964 through 1968).

Make is specified with no model or years (or series). Example:
New Holland (model and year/series are blank to indicate all
models and years/series of New Holland vehicles)

When you want to display the recommended maintenance for a particular
piece of equipment, the program does the following to determine which
service table to use:


Oo

 

 

 

 

First, it tries to find the actual make, model and year (or series) of
the equipment. If that fails,

It tries to find the make and model (with a blank year and series). If (
that fails,

It tries to find the make and year (with a blank model and series). If
that fails,

It tries to find the make (with blank model and year and series). If
that fails,

It will use the default service table (refer to SETTING UP A
DEFAULT TABLE in CHAPTER X10.3-1, INQUIRE/UPDATE
SERVICE TABLES). If no default table is found,

An error message is displayed.

:

RELEASE 2.3 NS


X10.3-2 INQUIRE/UPDATE MAKE MODEL ASSIGNMENTS [2]

### How To Run

From the Service Utilities Menu (X10-3), select option 2, Inquire/Update
Make Model Assignments.

Add Assignments

The two modes in Inquire/Update Make/Model Assignments are: ADD
and UPDATE. If you have never assigned makes and models to service
tables, the screen is displayed in ADD mode. If assignments have been

made, the screen is displayed in UPDATE mode. Use [Cmd8] to switch
between the ADD and UPDATE modes.

The first time equipment is assigned to a service table, the word “Add”
appears in the upper corner of the screen, as illustrated below:

ABC COMPANY Make/Model Assignments ‘XA320-101.

O You can add 16 makes and models on each screen. Press [Enter]. A
new screen will be displayed.

Note:

Once you press [Enter], changes must be made in Update Mode. Press

{Cmd8] to update the assignments. |

 

SERVICE MANAGEMENT


[ «| X10.3-2 INQUIRE/UPDATE MAKE MODEL ASSIGNMENTS a

### Fields & Descriptions

The fields on the Make/Model Assignments screen are described below in
the order in which they appear.

In defining the fields, a character is any character on your keyboard,
usually letters A-Z and numbers 0-9, but special characters such as "!"
"@" "#" can be used. Do NOT use the following characters: "" (blank)
"." (comma), "*" (asterisk), "/" (forward slash), “." (dash or minus sign),
"+" (plus sign), ">" (greater than sign), "=" (equal sign), or "2" (question
mark).

A digit is any number from 0-9. Example: 5.2 D digits means 5 digits

with 2 fixed decimal places. 12345.67 is typed as 1234567. {
Make 9 characters
Make of piece of equipment.
Model 9 characters
Model of piece of equipment.
Year 4.0 digits

Use either a year range or a series code
(below). Type the years of the makes and
models to be assigned to the service table.
Use 2 digits. for the beginning year and 2
digits for the ending year. For example, if
the service schedule covers the makes and
models made from 1985 to 1987, enter:
85 (to) 87
A make and model for the years specified
can only be linked to one service table.

RELEASE 2.3 LO


X10.3-2 INQUIRE/UPDATE MAKE MODEL ASSIGNMENTS L:]

Series 3 characters
Use either a year range (above) or a series
code.

Service Table 6 characters

Type the name of the appropriate Service
Table for the make and model listed.

Update Assignments

If makes and models have been assigned to service tables, you can press
[Cmd8]-Update assignments to change them. On the update screen, the
word “Update” is displayed in the upper right hand corner, as illustrated:

ABC COMPANY Make/Model assignments 4320-101

Oi Make changes by typing over the existing information. Press [Enter] to
register the change and to see more screens.

SERVICE MANAGEMENT


[ «| X10.3-2 INQUIRE/UPDATE MAKE MODEL ASSIGNMENTS a

### Print Assignments

To print a list of assignments, press [Cmd1] to end the job. The following
screen is displayed:

ABC COMPANY Make/Model Assignments KA230~104 4

If you want to:

= end the job and return to the Service Utilities Menu, press [Cmd1].

= go back to the Make/Model Assignment screen, press [Cmd3].

= return to the Service Utilities Menu without printing, press [Enter].

= print the job codes and return to the Service Schedules Menu, type: Y, {
and press [Enter].

A list of assignments is illustrated below:

Service Schedules Date 11/05/92 Page 1
Assignments Time 11.34.51 xA320-20

Year Series Service Table
Jos = 506341
85 to sac
86 to 89 580¢
BS to a7 5000,
86 to 89 5000
90 co 92 5000
co. seer
80 co 92 secc
85 to 92 000

 

RELEASE 2.3 Lo

## CHAPTER X10.3-3

SERVICE NOTE DISTRIBUTION

### Introduction

Use Service Note Distribution to distribute notes, such as special programs
or recall notices, to a range of units.

### How To Run

From the Service Utilities Menu (X10-3), select option 3, Service Note
Distribution. After the service security gate, the Service Note Distribution
screen appears:

A & R SALES & LEASING CO Service Note Distribution %A330-101
Division: a

cmdi-End job

 

‘Type the make and model of the units. Leave the year fields blank to affect
all years, or type the range of years the note pertains to. Also, leave the
serial number blank to place the note on all selected units, or type the
range of serial numbers the note pertains to.

When the selection criteria are complete, press [Enter].


[=| X10.3-3 SERVICE NOTE DISTRIBUTION co

A & R SALES & LEASING CO Service Note Distribution XA33-102
Division: A

Service Note:

REPLACE CAM BELTS ASAP - RECALL NOTICE 05/21/91

print selected equipment? N

00002 items selected - £i11 in Service Note and Enter to update selected items
cmdl-End job Cnd3-Previous

 

Note the message that is displayed at the bottom of the screen giving a
count of the number of units that will be affected by this service note.
Type the service note (up to 62 characters), and press [Enter] to send it.

If the note is incorrect, send the correct version to the same units. The
incorrect note will replaced and moved to history, where it can be deleted.

If you send the note to the wrong units, you can send a blank note to the
same units. The incorrect note is replaced by the blank note and moved to
history, where it can be deleted.

To request a list of the units that received this service note, type Y in the
field labeled "Print selected equipment?"

LU

## CHAPTER X10.3-4

STANDARD JOB RENAME

### Introduction

This job allows you to change the name of a standard job and assign it to a
different group, if desired.

### How To Run

From the Service Utilities Menu (X10-3), select option 4, Standard Job

Rename. The following prompt asks you for the current Job:Group
names.

ABC-AG, AUTO, CONS & TRUCK CO. Job Code Rename 1 XA340-101,
Division: A

Job Code to Rename 1048BR
Group 5000


[| X10.3-4 STANDARD JOB RENAME a

CO Fumish the current job and group, and press [Enter]. Prompts for the
new job and group names are displayed.

ABC-AG, AUTO,CONS & TRUCK CO. Job Code Rename 4 XA340-101

Division: A

Job Code to Rename 1048BR
Group 5000

Job/Group Description
1048BR REPLACE BRACKET
5000

Cmdi-mmd job Cmd3-Go back

 

(C0 Fumish the new job code and group, and press [Enter]. You return to
the first prompt.

C When you are done, press [Cmd1] to end the job.

LL.

## CHAPTER X10.3-5

SERIAL NUMBER RENAME

### Introduction

Equipment serial numbers are part of the information stored in service
history. Use this job to change the serial number on a piece of equipment.
Only the serial number can be changed. This new serial number will then
be updated throughout service history.

### How To Run

From the Service Utilities Menu (X10-3), select option 5, Serial Number
Rename. The Serial# prompt is displayed:

AUSTIN TRACTOR & EQUIPMENT Serial #/VIN Rename XA500-103,
Division: A Rename Equipment

Serial to Rename:

 

Enter the serial number you want to change. Press [Enter]. Information
about the piece of equipment and its owner will display.

To complete the change, type the new serial number. Press [Enter].


[| X10.3-5 SERIAL NUMBER RENAME

Below is a sample of the Rename Equipment screen:

AUSTIN TRACTOR & EQUIPMENT Serial #/VIN Rename XA500-301
Division: A Rename Equipment

Serial # to Rename BB7685S

+ ADAMOL

FORD

7610

All Purpose Tractor
5/24/88

 

Description . . .

New Serial # BB89798

(md3-Go back

If you want to:
™ end the job and retum to the Service File Maintenance Menu, press

[Cmd1].
® go back to the Serial# prompt, press [Cmd3].

## CHAPTER X10.3-6

SERVICE DIVISIONAL PROFILE

### Introduction

This required setup job records defaults for Service Management, such as
sales codes, hourly rate for labor, and a schedule for "collapsing" history
documents in order to preserve disk space.

### How To Run

O From the Service Management Menu (X10), select option 3, Service
Utilities Menu.

Oi From the Service Utilities Menu, select option 6, Service Divisional
Profile.

ABC COMPANY SERVICE DIVISIONAL PROFILE XA360-101 1
Division: L

Default miscellaneous description sales code (D)
Default labor sales code (u)
Default miscellaneous quantity sales code — (M)
Default note sales code
Default part sales code

Default internal tax code
Default internal discount code

Default labor hourly rate 4000

Collapse history to the document level if older than month(s)
Collapse history to the job code level if older than month(s)
Collapse history to the customer/unit level if older than month(s)

Enter-Continue Cmdl-End job


[=| X10.3-6 SERVICE DIVISIONAL PROFILE C .

The prompts are described below.

The first prompts are for sales codes. The required format is presented in
parentheses. For example, the miscellaneous description sales code must
be of line type "D."

Default miscellaneous description sales code (D)
Used during conversion of history.

Default labor sales code (L)
Used for default labor line.

Default miscellaneous quantity sales code (M)
Used during conversion of history.

Defauit note sales code (N)
Used for the Standard Job Header at Point of Sale. Also used during
conversion of history.

Default part sales code (P)
Used during conversion of history.

The following prompts pertain to the tax and discount lines that are
charged, not to the customer, but to "Internal,"

Default internal tax code
Tax code used for lines charged to "Internal."

Defauit internal discount code
Discount code used for lines charged to "Internal."

The default labor hourly rate is the dollar amount that is multiplied by the

i


X10.3-6 SERVICE DIVISIONAL PROFILE [=]

standard job flat rate (time entered on the standard job Sold To screen) to
calculate the estimated price of labor. The estimated price of labor appears
first in Inquire/Update Service Tables, then in Recommended
Maintenance.

Defauit labor hourly rate
Dollar amount charged for 1 hour of labor. Two decimals are assumed.

As you may suspect, storing a lot of document detail consumes a lot of
disk space. To help you conserve disk space while, at the same time,
preserving enough information to be helpful, DIS has provided a way for
you to delete some detail. Based on the schedule entered below, history
documents are collapsed during Point of Sale End of Month (X5-4).
Collapsed documents are listed on the Service History Report as
"Summary Documents.”

Collapse history to the document level
Job header lines are deleted; individual document remains intact.

Collapse history to the job code level
Lines with the same sales code format, such as "P" (parts format), are
combined into 1 line and | total. Individual documents remain intact.

Collapse history to the customer/unit level
At this level, documents lose their identity as identical job codes are
combined onto a common document. The remaining summary
documents, lacking detail, indicate only jobs done and totals spent.

SERVICE MANAGEMENT


Notes:

## CHAPTER X10.3-7

UPDATE STANDARD JOB PARTS PRICES

### Introduction

Use this option after a price update to change the prices of standard job
parts that are also in your inventory. You can change one group at a time
or all groups.

### How To Run

C From the Service Management Menu (X10), select option 3, Service
Utilities Menu.

Service Utilities Menu

COMMAND
{e) DIS Corp.

. Inquire/Update Service Tables

. Inquire/Update Make Model Assignments
. Service Note Distribution

. Standard Job Rename

. Serial Number Rename

. Service Divisional Profile

. Update Standard Job Parts Prices
. Update Labor Rate for a Group

. Delete a Standard Job

. Load Manufacturer Standard Jobs
. Correct Service History

23. Return to Service Menu

Ready for option number or command

soe> 7

 

CI Select option 7, Update Standard Job Parts Prices. You are prompted
for a group code.


[| X10.3-7 UPDATE STANDARD JOB PARTS PRICES os

Update Parts Prices Screen

ASR EQUIPMENT SALES Update Parts Prices xA370-101
Division: A

Part prices and bin locations will be updated from your inventory
for all job codes that belong to the selected group. Enter the group
number to update or enter *ALL to update job codes for all groups.

cmdl-End Cmd4-List of Groups  Enter-Update

 

O To update all job codes in all groups, type: *ALL at the group prompt,
and press [Enter]. Since there are over 500 groups, about 228,485
standard jobs for Case Ag and 88,503 for Case construction equipment,
the job will take a long time.

O If you know the group code, type it and press [Enter]. The following
message will be displayed at the bottom of the screen: “Part prices and
bin locations were updated for the selected group.”

CO To select from the list of group codes, press [Cmd4]. Case job codes
are grouped by unit model numbers. You can type a partial model


number, then press [F4] and the list will start with the closest match.

List of Group Codes

A&R EQUIPMENT SALES LIST OF GROUPS
Division: A
Place any character next to a Group to select.

Position
Group Name -
6200
621
6218
6213
s21¢
6300
6388
65L
650
6505
6506
6500
e588
6590
660

cmdi-End  Enter-Page

 

SERVICE MANAGEMENT


[| X10.3-7 UPDATE STANDARD JOB PARTS PRICES

O Place any character beside the group you want to update. The code is
retrieved to the group prompt.

CO Press [Enter] to start the update. When it is complete, the following
message appears at the bottom of the screen: “Part prices and bin
locations were updated for the selected group.” Select another group
and repeat the process, or press [Cmd1!] to end.

## CHAPTER X10.3-8

UPDATE LABOR RATE FOR A GROUP

### Introduction

Use this option to change the labor rates on a group. Updates are done for
all standard jobs in a group. Since only flat rates are provided by Case
Corporation, there are no labor rates unless you have added them. Only
one group can be updated at a time.

### How To Run

O From the Service Management Menu (X10), select option 3, Service
Utilities Menu.

Service Utilities Menu

COMRIAND
(c) DIS Corp.

. Inquire/Update Service Tables

. Inquire/Update Make Model Assignments
+ Service Note Distribution

. Standard Job Rename

. Serial Number Rename

. Service Divisional Profile

. Update Standard Job Parts Prices

- Update Labor Rate for a Group

. Delete a Standard Job

. Load Manufacturer Standard Jobs

. Correct Service History

. Return to Service Menu

Ready for option number or command
===> 8

 

O Select option 8, Update Labor Rate for a Group. You are prompted for
a group code.


[=| X10.3-8 UPDATE LABOR RATE FOR A GROUP Co

Update Parts Prices Screen

A&R EQUIPMENT SALES Update Labor Rate XA380-101
Division: A

@mal-End Cmd4-List of Groups

 

O Ifyou want to update labor lines on one or more groups, type the first
group number, or to select from the list of groups, press [Cmd4].

RELEASE 2.3 LO


X10.3-8 UPDATE LABOR RATE FOR A GROUP [2]

List of Groups

AGR EQUIPMENT SALES LIST OF GROUPS XA2100-701
Division: A
Place any character next to a Group to select.

Position

— 621
— 6218
— 621B xX
~ 621¢
— 6300
— 6388
— 65L

~ 650

— 650E
~ 6506
— 6500
— 6588
— 6590
— 660

— 6650

Cmdl-End  Enter-Page

 

Q Place any character beside the group you want to update. You do not
need to press [Enter]. The group code is retrieved and appears at the
prompt.

O To update the labor rate for the group, press [Enter]. The Update Labor
Rate screen is displayed with the current rate.

SERICE MANAGEMENT


[ «| X10.3-8 UPDATE LABOR RATE FOR A GROUP

Update Labor Rate Screen

A&R EQUIPMENT SALES Update Labor Rate XA380-102
Division: A

cmdi-End  Entex-Update

 

C Furnish a new rate, if desired. Press [Enter]. The following message is
displayed at the bottom of the Entrance screen: “Labor lines were
updated for the selected group.”

O Repeat as necessary.

## CHAPTER X10.3-9

DELETE A STANDARD JOB

### Introduction

Use this option to delete a standard job from a group. WARNING! There
is no confirmation message.

### How To Run

O From the Service Management Menu (X10), select option 3, Service
Utilities Menu.

Service Utilities Menu

COMMAND
(c) DIS Corp.

. Inquire/Update Service Tables
. Inquire/Update Make Model Assignments
. Service Note Distribution
. Standard Job Rename
Serial Number Rename
. Service Divisional Profile
. Update Standard Job Parts Prices
. Update Labor Rate for a Group
. Delete a Standard Job
. Load Manufacturer Standard Jobs
. Correct Service History

. Return to Service Menu

Ready for option number or command
za 9

 

O Select option 9, Delete a Standard Job. You are prompted for a job code
and a group code.


[| X10.3-9 DELETE A STANDARD JOB C

Update Parts Prices Screen

AGR EQUIPMENT SALES Delete a Standard Job XA390-101
Division: A

cmdi-fnd _Enter-Delete

 

O There is no F4=Prompt on this screen. Enter the exact job code and its

group code.
CO Press [Enter]. A deletion notification message similar to the following
appears at the bottom of the screen: “Deleted standard job - nnnnnnnn.”

LC

## CHAPTER X10.3-10

LOAD MANUFACTURER STANDARD JOBS

### Introduction

In this chapter, you'll learn how to load manufacturer standard jobs and how to
use them at Point of Sale. In addition, you'll learn how to change standard jobs
and how to prevent their being overwritten during an update. After standard jobs
have been loaded, a Standard Job Exception Report lists the jobs that you have
specified for no update.

Standard jobs are available in Inquire/Update Units (X10-1) in Recommended
Maintenance, and they are displayed in Service History. Descriptions of job codes
on labor lines are listed on the Standard Jobs Report (X10.2-3) and Service
History Report (X10.2-4).

You can change standard jobs in Point of Sale in Standard Jobs mode. You can
access standard jobs in Active Document mode from the detail line by using
Copy-Lines [F20].

Case Standard Jobs

Over 500 Case model numbers are used as group codes, and they are added to the
master file as cash customers; therefore, they will not appear in the Point of Sale
index unless you track cash customers. As of October 1999, there were about
228,485 standard jobs for Case Agriculture and 88,503 for Case Construction
Equipment.

Thermo King Standard Jobs

Thermo King standard jobs are uploaded from Thermo Komm automatically
according to the schedule specified in Set Time for Daily TKOMM Updates
(X7.14-10), or you can use Get Updates from TKOMM Immediately (X7.14-11).
Because the labor hours vary by model number, you will need to remember that
the group code will be *TKJOB, the job code will be TK job code (5 characters)
with the model number suffixed (3 characters).

xaSa.doc 12/8/00 1


2 X10.3-10 e LOAD MANUFACTURER STANDARD JOBS. RELEASE 10.1

### Contents

ENTRANCE SCREEN..
Service Utilities Menu .
Load Mfg Standard Jobs Screen .
Enter Document Type Screen......
Update Sales Code Cross-Reference Screen.
Update Vendor Cross-Reference Screen
Update Default Tax-Disc Codes.....
Update Flat Rate Mark-up Factors...
Program Messages - Rebuilding Indexe:
Program Messages - Customer Index Set-up.

 
  
 
 
 
 
  

CHANGING STANDARD JOBS...
Point of Sale Sold To Screen

 
 

USING STANDARD JOBS AT POINT OF SALE... 215
Copy-Lines Options Screen
Select Service Job Index...
Point of Sale Detail Screen ..


SERVICE MANAGEMENT X10.3-10 « LOAD MANUFACTURER STANDARD JOBS 3

SETUP

During the loading process, you will be asked for setup information, which
includes:

1. The document type you use for Service Management.

2. Cross-references for sales codes. Your sales codes must be of the same format
as the sales codes on the tape.

3. Cross-references for vendor codes. Your 3-character vendor codes for Case
and Allied will be required.

4. Default tax and discount codes for:
Part lines
Labor lines
Miscellaneous quantity lines
Miscellaneous description lines

5. Updates to flat rate mark-up factors, if applicable. Since only flat rates are
provided with the job codes furnished by Case Corporation, there are no labor
rates unless you add them to the standard jobs.

After the initial load, subsequent updates to standard jobs will print a list of
standard jobs that you don’t want updated automatically because of changes you
have made. You can use the list to decide whether you need to update the part
prices manually.

To be better prepared for the questions, take a look at the screens, which are
illustrated in this chapter, before you begin. To print the standard jobs after they
have been loaded, use Standard Job Report (X10.2-3).

Technical Notes:

Case’s group codes correspond to model numbers, and they are added to ADM as
cash customers. All standard jobs are added to u.SJM (u=User ID, the character
associated with the file set). The following files are used: u.CRS (cross-reference
for sales codes), u.CRT (cross-reference for tax and discount codes), u.CRV
(cross-reference for vendor codes).


4 X10.3-10 e LOAD MANUFACTURER STANDARD JOBS RELEASE 10.1

### Entrance Screen C

A dedicated system is not required to Load Standard Jobs; however, it will run
faster if you’re not using Point of Sale at the same time.

O From the Service Management Menu (X10), select option 3, Service Utilities
Menu.

Service Utilities Menu

 

COMMAND
{e) DIS Corp.

. Inquire/Update Service Tables

. Inquire/Update Make Model Assignments
. Service Note Distribution

. Standard Job Rename

. Serial Number Rename

. Service Divisional Profile

. Update Standard Job Parts Prices

. Update Labor Rate for a Group

- Delete a Standard Job (
. Load Manufacturer Standard Jobs

. Correct Service History

. Return to Service Menu

Ready for option number or command

seep

 

O Select option 10, Load Manufacturer Standard Jobs. You are prompted to
insert the Tape or CD.


SERVICE MANAGEMENT X10,3-10 ¢ LOAD MANUFACTURER STANDARD JOBS

Load Mfg Standard Jobs Screen


 

LOAD MFG STANDARD JOBS XA3A0-001
Specify Media

Place the Manufacturer Standard Jobs tape or CD-ROM into the proper
device, specify your choice below, and press [Enterj to continue.

Installation media: 1
1 - Tape
2 - CD-ROM

Enter-Continue F3-Exit

C1 Insert the CD or tape, and press [Enter].

You are prompted for the document type you use for Service Management.


6 X10.3-10 e LOAD MANUFACTURER STANDARD JOBS RELEASE 10.1

Enter Document Type Screen

A&R EQUIPMENT SALES LOAD MFG STANDARD JOBS XA3A0-801
Division A Enter Document Type

Service Management Document Type... -

Enter-Continue F3-Exit

 

O Enter the document type you use for Service Management and press [Enter].
The Update Sales Code Cross-Reference screen is displayed.


SERVICE MANAGEMENT X10.3-10 « LOAD MANUFACTURER STANDARD JOBS

Update Sales Code Cross-Reference Screen

A&R EQUIPMENT SALES LOAD MFG STANDARD JOBS XA3A0-301
Division A Update Sales Code Cross-Reference

Incoming Data: Your Dealership
Sales Code Format Description Sales Code Format Description
- NOTES NN NOTES
FIELD LABOR Te LABOR CUSTOMER
PARTS SERVICE PC PARTS CUSTOMER
SERV OTHER PTS PC PARTS CUSTOMER
SERV PARTS CASE PC PARTS CUSTOMER
SHOP SUPPLIES ss SUBLET SALE
MILEAGE PK PARTS WHOLE MIS
LABOR SERVICE Te LABOR CUSTOMER
EPA ss SUBLET SALE

FR
PS
SA
sc
ss
™
TS
2B

vPsxovUNE Ss
UNE UUs

Enter-Continue F3-Exit

The first time you encounter this screen, the sales codes on the right will be
exactly the same as the ones on the left; however, after you provide cross-
references to your own sales codes, the system will display your changes on the

right.

O Change the sales codes on the right to the corresponding sales codes used at
your dealership. The formats, such as P=Parts or D=Miscellaneous
Description, must be the same.

O When you're sure all the sales codes correspond, press [Enter]. The vendor
cross-references are presented next.


8 X10.3-10 « LOAD MANUFACTURER STANDARD JOBS RELEASE 10.1

Update Vendor Cross-Reference Screen

 

AGR EQUIPMENT SALES LOAD MFG STANDARD JOBS MA3A0-401
Division A Update Vendor Cross-Reference

Incoming Data ~--- Your Dealership ----
Vendor Code Deseription Vendor Code Description
AL ALLIED MAS MASSEY FERGUSON
cAS CASE CORPORATION cAS CASE/IH

Enter-Continue F3-Exit

This table works like the sales code table: the first time the vendor codes on the
right will be exactly the same as those on the right. On subsequent occasions, the
table on the right will reflect your changes.

1 Fumish the 3-character vendor codes you use for Case and Allied, and press
[Enter]. Tax and discount updates follow.


SERVICE MANAGEMENT X10.3-10 e LOAD MANUFACTURER STANDARD JOBS 9

Update Default Tax-Disc Codes

AGR EQUIPMENT SALES LOAD MFG STANDARD JOBS
Division a Update Default Tax/Disc Codes

wees Tax ---- - Discount --

code Rate Code Rate

Part Lines 07800 coo
Labor Lines 07800 00000
Misc Quantity Lines 07800 00000
Mise Description Lines 07800 00000

Enter-Continue P3-Exit

 

 

O Fumish the tax and discount codes that will be associated with the types of
lines listed. In addition, furnish the corresponding rates for each code. When
you are done, press [Enter].


10 X10.3-10 » LOAD MANUFACTURER STANDARD JOBS RELEASE 10.1

Update Flat Rate Mark-up Factors

A&R EQUIPMENT SALES LOAD MFG STANDARD JOBS
Update Flat Rate Mark-up Factors

Manufacturer: CASE CORPORATION

to 05 Hours - Multiply by a factor of 1.0000
to 15 Hours - Multiply by a factor of 1.0000
Hours and up - Multiply by a factor of 1.0000

A mark-up factor of 125% would be entered as 1.2500)

Enter-verify F2-Continue F3-Exit

 

This table lets you change the flat rate markup factors.

O Specify the hour range and change the percentage factor, to either increase or
decrease the job code rate, to match the rate used at your dealership.
Example: A mark-up factor of 150% would be entered as 1.5000.

O When you are done, press [Enter] to verify and then [F2] to continue.


SERVICE MANAGEMENT X10.3-10 « LOAD MANUFACTURER STANDARD JOBS V1

Program Messages - Rebuilding Indexes

 

8/36 PROGRAM MESSAGES

### Xa3A00

Adding Case Corporation CE Jobs to the Standard Jobs file,
DELETE procedure is running

DELETE procedure is running

DELETE procedure is running

DELETE procedure is running

Rebuilding Marketing index . . |

Rebuilding Payable index...

Rebuilding Point of Sale index...

Rebuilding Receivable index...

 

1 Ifyou are running Point of Sale when loading the job codes, you will need to
tun Customer Index Set-up (X5.2-1).


12 X10.3-10 « LOAD MANUFACTURER STANDARD JOBS RELEASE 10.1

Program Messages - Customer Index Set-up

Tf Point of Sale is active at the time you are loading the job codes, you will see the
Customer Index Setup Screen. You can choose to end Point of Sale at this time
and press enter to continue or press F3=Skip Customer Index Setup and run this
job from the menu (X52-1) at a later time.

 

LOAD MFG STANDARD JOBS XA3A0-002
Customer Index Setup .

In order to complete this job, an attempt was made to run a Customer
Index Setup. Customer Index Setup could not pe run, however, because
the index files are in use by other jobs.

No Point of Sale jobs may be running in order to complete a Customer
Index Setup. After ending all Point of Sale jobs, press enter to
continue with the Customer Index Setup. If you cannot end all Point
Sf Sale jobs now, you may press F3 to skip this step. If you do skip
thig step now, you must run a Customer Index Setup at a later time
from Menu X52 option 1.

Enter-Continve F3-Skip Customer Index Setup

 

0 Press [Enter] after ending Point of Sale jobs, or to bypass Customer Index Set-
up and run it later press F3=Customer Index Setup from the menu option.

After the indexes are rebuilt, you will return to the Service Utilities Menu.

O To print the standard jobs, you may use Standard Job Report (X10.2-3) at any
time.


SERVICE MANAGEMENT X10.3-10 e LOAD MANUFACTURER STANDARD JOBS 13

### Changing Standard Jobs

To change a standard job, start at the Point of Sale Entrance screen.

 

A&R EQUIPMENT SALES POINT OF SALE Std Jobs 5100-104
INVOICING-ENTRANCE

Tf a new document, enter document type:

Enter customer name or address number 6218

If internal document Document # 0402700
enter stock number

Do you want back order lines to print?

Use Cmdl4 to switch mode:

Active Documents
=> Standard Jobs
History Documents

 

1 Ifyou don’t know the group or job code and cash customers are tracked, place
a model number in the name field. Standard jobs will be listed in the Point of
Sale index along with all the other cash customers.

1 Ifyou don’t know the group or job code, place a question mark (?) in the
name field and press [Enter] to go directly to the Select Service Jobs screen.

0 Ifyou know both the group and job codes, type the group code in the address
number field, and type the standard job code in the Document # field. In this
case, you will go directly to the Sold To screen, where the standard job
description will be displayed, as illustrated on the screen below.


14 X10.3-10 ¢ LOAD MANUFACTURER STANDARD JOBS RELEASE 10.1

 

Point of Sale Sold To Screen

 

 

 

 

 

 

 

—
A&R EQUIPMENT SALES INVOICING-SOLD TO Std Jobs x5100-105
UNET SALE #040170A CASH = OPEN 1/13/00
Sold to: 621B Freon#: Ship to:
6213 —
_—
_
_
¢ Unit:
ship By Sold By 6218 P.O. Add Date 8/27/98
Sales Code Transfer Quantity Break Pricing N_ Print Date
Tax Number _ GST Method O ‘Trans Date
Periodic Type ___Periodic Frequency Rental Staxt Date
Sta Job Desc: JUNCTION STUD FOR CAB POWER, R Std Job Flat Rate: 00100 Update:N
Make Model Year Serial Number Hourmeter Warranty
Balance Current 31-60 61-90 90 +
Internal address #:______
credit Limit Peak Bal Beg Date Or Unit #:
Warranty Address #:_______

 

 

0 To preserve changes to standard jobs and prevent their being overwritten
during a future load or update, you must set “Update=N” on the Point of Sale

Sold To screen (see example above). T
which is printed after standard jobs are

‘he Standard Jobs Exception Report,
loaded, lists jobs flagged “Update=N.”

You may want to update the part prices on these jobs manually.

(1 Proceed to the detail screen, where you can remove or add lines to the
standard job. When you are done, press [F4].

O Following a price tape update, you can

change prices on parts with Update

Standard Job Parts Prices (X10.3-7). Ifyou add labor lines to standard jobs,
you can change group labor rates with Update Labor Rate for a Group (X10.3-

8). You can eliminate a standard job wi

ith Delete a Standard Job (X10.3-9).


SERVICE MANAGEMENT X10.3-10 e LOAD MANUFACTURER STANDARD JOBS 18

### Using Standard Jobs At Point Of Sale

OD At Point of Sale Invoicing (X5-1), press [Cmd14] until you’re in Active
Documents mode.

C1 Open a work order as usual. Go to the detail screen.

 

### A&R Equipment Sales Work Order 5100-106

REPAIR ORDER # _ROO0169 For 000004 CHARGE OPEN 1/13/00

TDP Line # Qty vVnd Part Number Description Bin Ext Price
Spec order parts -00 Avail total 00 Total 00
TDI/W Copy Line sc Description-----------~--------~ * Amount
A go10  +*

 

Standard line code

 

 

C1 Press [F20] (same as [Shift]+[F8]) for Copy-Lines. The copy-lines options
screen is displayed.


16 X10.3-10 e LOAD MANUFACTURER STANDARD JOBS RELEASE 10.1

 

Copy-Lines Options Screen

 

AGR EQUIPMENT SALES POINT OF SALE X5100-108
Enter options for copy-lines function
Source of lines. eet ttt customer 621B
Defaults to previous document... +--+ + or Unit
wee .. . Document ?
source file; active, standard job, ox history . choice = J_ A\g|H

Default tax code cs wo
Default discount code - - s+ seer


 

Process options
1. Preview each line before adding - - +--+ + - 7 enter
2. Copy all lines... ee ee et tte . choice ior 2

iy

Reprice options
1. Reprice parts from current inventory. - + - + 5° - enter
2. Keep pricing of source document -- - - - . choice itor 2
Tax and discount codes will also be kept
if copying from same customer.

ir

Disposition of source document (quotes only)
1. Do not void automatically -- - +--+ ert enter
2. Void quote automatically .- +--+ + 1. choice Lor2

\r

 

C1 To position the list at a specific group, enter a partial or full group code in the
Customer field and place a question mark (?) in any position of the Document
field. Or, if you don’t know the group code at all, enter a “?” in any position
of the Customer or Document.

1 Change the Source file to "J" to indicate a standard job.

DB Select other options as desired. You will not come back to this screen after
you select the job code. For more information on these options, see

1 Press [Enter] to go to the Standard Jobs index.


SERVICE MANAGEMENT

X10.3-10 ¢ LOAD MANUFACTURER STANDARD JOBS

Select Service Job Index

 

Division:

Group
6218

__Group
6213
6218
“6218
6213
“6218
“e218
“e21n
__ 6218
__ 6218
“e21B
76218
6218
_ 6218
__621B

 


A&R EQUIPMENT SALES

dob Code
040140a,

Job Code
020301A
0203018
020301¢
020302
0203028
020302c
020302D
020302E
020302F
020302G¢
020303
020303B
020303
020311A

Select Service Job

Description

FILTER ELEMENT FOR ENGINE OIL,
FILTER ELEMENT FOR AIR CLEANER
FILTER ELEMENT FOR COOLING SYS
RUN ENGINE UNTIL IT REACHED OP
STALL SPEED TEST

LOOSEN INJECTOR LINE FITTING T
CHECK INTAKE SYSTEM FOR AIR RE
COOLING SYSTEM PRESSURE TEST
OPERATION OF THERMOSTAT, TEST
TROUBLESHOOT ENGINE

ENGINE ASSEMBLY, R&I

SHORT BLOCK ASSEMBLY, R&I
ENGINE ASSEMBLY, OVERHAUL
RADIATOR CAP, R&I

Cmdi-End Enter-Page Down

Hours
30
+20
-30
~30
+30
50
~50
.30
+40
80

15.00

26.10

33.60
+20

### Xa100-401

 

O Type all or part of the group code (Case’s model number) and part or all of the

job code at the Job Code prompt and press [Enter].
O Place any character beside the job code you want. The copy-lines function

starts immediately. Lines are copied to the Point of Sale detail screen
according to the other options you selected on the Copy-Lines Option screen.


18 X10.3-10 « LOAD MANUFACTURER STANDARD JOBS RELEASE 10.1

 

Point of Sale Detail Screen

 

 

 
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

### A&R Equipment Sales Work Order ¥5100-106

REPAIR ORDER # RO00172 For 000004 CHARGE CLOSED 1/13/00

TDP Line # Qty Vnd Part Number Description Bin Ext Price
01 0010 %% JOB:040170A 6218 001.00 JUNCTION STUD FOR CAB POWER, R
01 0020 NN JUNCTION STUD FOR CAB POWER, R&I
01 0030 NN - INCLUDES REPLACING SEAL
01 0040 NN - INCLUDES CHECK ALL SPECIFICATIONS AND TOLERANCES
01 0050 NN - INCLUDES FILTER ELEMENTS, REPLACE
01 0060 NN - INCLUDES DO RUN-IN PROCEDURES & ADJUSTMENTS
01 0070 NN - INCLUDES CLEANING & PAINTING

A 01 0080 PC = - 1 CAS A187523 4 17.55
A 01 0090 PC = 2 CAS 56698RL 4 17.34
A 01 0100 TC HAL 10/21/99 1.00 = 1.00 42.00
Spec order parts .00 Avail total 82.89 Total 82.89
LABOR CUSTOMER

TDI Line sC¢ Date Tech. Report Billed Rate
A 01 0110 TC 01130

Standard line code

 

On the screen illustrated above, you can see that the standard job had been
modified to add a labor line.

## CHAPTER X10.3-11

CORRECT SERVICE HISTORY

### Introduction

Use this option to make corrections to serial numbers that have been
entered by mistake. Usually these are typographical errors that cause
variations of a serial number to be set up as separate units. For example,
serial number 2P4FH5531LR621529 may also be entered as
2P4FH5531LR621528 and 2P4FH5531LR621592. You can use this job to
eliminate the incorrect serial numbers and combine service history records
under the correct serial number.

During Correct Service History, no parts or point of sale jobs should be
running. In addition, the Point of Sale Print program (DISPSPPnu) must
be ended by running backup, Point of Sale End of Month, or manually
ending it in Work with Active Jobs. Instructions are included in this
chapter.


[2 | X10.3-11 CORRECT SERVICE HISTORY c .

### How To Run

From the Service Utilities Menu (X10-3), select option 11, Correct Service
History. The job is preceded by the following warming, which indicates
when it can be run:

Warning Screen

CORRECT SERVICE HISTORY xA400-002

This job showld only be run when there are no other Parts or Point of
Sale jobs ruaning on the system.

Usually there is a dedicated invoice printing program running on the {
system which will prevent this job from starting. Performing an

automatic backup or running Point of Sale end of month will end this

printing program.

Press Enter to continue or Cmdi to end.

 

The dedicated invoice printing program is DISPSPPnu, where
DIS=DIS
PSP=Point of Sale Printer
Pn=S/36 printer ID of the Point of Sale printer, such as P2
u=File set, such as Z

If the Point of Sale print program is not running, you will go directly to the
Correct Service History screen; otherwise, you will see the Display
Program Messages screen when you press [Enter].

Display Program Messages Screen

RELEASE 2.3 LL


Display Program Messages

Job 140717/EBS/ELISABESS1 started on 09/05/96 at 08:31:08 in subsystem QINTE
This job cannot be run. File E.SAM is being used by another job,

Press Enter to continue.

F3=Exit F12=Cancel

 

O Press [Enter] to return to the Service Utilities Menu.

SERVICE MANAGEMENT


[ «| X10.3-11 CORRECT SERVICE HISTORY C

Ending the Point of Sale Print Program

To end the Point of Sale print program, follow these steps.

O Make sure there are no active Point of Sale sessions.

O At acommand line, type: WRKACTJOB [Enter]. The Work with
Active Jobs screen is displayed.

Work with Active Jobs Screen

Work with Active Jobs 1011024
05/05/96 08:44:49
CPUs: 10.4 Elapsed time: 00:11:53 Active jobs: 98

Type options, press Eater.
2-Change 3-Hold 4=End 5=Work with 6=Release 7=Display message
8-Work with spooled files 13=Disconnect ... (

Type CPU % Function Status
SBS : DEQ
BCH .0 POM-DISARCHTVE DEQW
BCH -0 PGM-DISARCHTVE  DEQW
SBS : DEQW
BCH «0 PGN-DISPOSPRT —§ DEQW
SBS ‘ DEQW
DISPSPPIE BCH .0 PGM-DISPOSPRT — DEQW
DISPOSPRTT SBS : DEQ
DESPSPP2L BCH .0 PGH-DISPOSPRT — DEQW

s
5

=Pxit F5=Refresh Fl0=Restart statistics Fll-Display elapsed data
Fl2=Cancel  F23=More options F24=More keys

 

Q Select each DISPSPPnu with 4=End. There will be a Point of Sale Print
program for each Point of Sale printer. The Confirm End of Active Jobs
screen is displayed.

Confirm End of Active Jobs Screen

RELEASE 2.3 LO


X10.3-11 CORRECT SERVICE HISTORY is |

Confirm End of Active Jobs $1011024
09/05/96 08:44:49
cpu: 10.4 Elapsed time: 00:11:53 Active jobs: 98

Press Enter to confirm your choices for 4=End.
Press F12 to return to change your choices.

Opt sSubsystem/Job User Type CPU $ Function
4 DISPSPP9E EBS BCH -0 PGM-DISPOSPRT

F12=Cancel

 

Press [Enter]. The following message appears at the bottom of the
Work with Active Jobs screen: ENDJOB started for job
140724/EBS/DISPSPP9E.

OQ Press F5=Refresh until the job DISPSPPnu disappears from the list of
active jobs.

Q Press [F3]=Exit to return to the Service Utilities Menu.

O Select option 11, Correct Service History, again.

SERVICE MANAGEMENT


[ «| X10.3-11 CORRECT SERVICE HISTORY cc

Correct Service History Screen

CORRECT SERVICE HISTORY %R400-001

   

: Correct Service Histoxy

: Enter the correct serial number:

: Serial Number Make Model Description
1 2PAFHSS31LR621529

: Up to ten incorrect serial numbers can be corrected:
: Serial Number Make Model Description
: 2P4FHS5311LR621528

2 2PAFHSS31LR621592

; Enter=validate F3sExit F10=Proceed

O Type the correct serial number on the first line.
O On the following lines, type the incorrect serial numbers.
O Press [Enter] to validate the incorrect serial numbers.

RELEASE 2.3 LU


Validation Screen
CORRECT SERVICE HISTORY xaAd00-001

: Correct Service History

i Enter the correct serial number:

: Serial Number Make Model Description
: 2PSFHSS31LR621529 AMAZON 4800 LOADER

: Up to ten incorrect serial numbers can be corrected:
: Serial Number Make Model Description
+ 2PAFHS5S31LR621528 AMAZON 4800 LOADER

: 2PAFHSS31LR621592 AMAZON 4800 LOADER

: Entersvalidate F3=Exit F10=Proceed

 

Q To transfer service history from the incorrect serial numbers to the
correct one, press F10=Proceed. The following message is displayed
below the command line on the Service Utilities Menu: Job
140717/EBS/XA4003 submitted to job queue QBATCH
in library QGPL. When the transfer is done, a message will be
sent to your terminal.

O To see the message, type: MSG [Enter] at a command line.

SERVICE MANAGEMENT


X10.3-11 CORRECT SERVICE HISTORY a

Display Messages Screen

Display Messages

System:  §1011024

Queue . . Program... . *DSPMSG
Library... QusRsYs Library...

Severity . Delivery .. - *NOTIFY

Type reply (if required), press Enter.
Correct Service History has completed.
Job 140729/EBS/XA4003 completed normally on 09/05/86 at 08:4

F3=Exit FllsRemove a message Fl2=Cancel
F13=Remove all F16=Remove all except unanswered F24=More keys

 

RELEASE 2.3 Lo

## CHAPTER X10.3-12

MAINTAIN SERVICE OPTIONS

### Introduction

Use this job to enter a table of service option codes and their descriptions.
The codes may be up to 8 characters each; the descriptions, 30 characters.
To print the list of options, press F21=Print on the Maintain Service
Options screen, or select option 11, Options File List, from the Service
Reports Menu (X10-2).

One service option can be associated with a unit on the Edit Unit Service

Information screen, which is illustrated below. This screen is accessed

from the Inquire/Update Service Units screen by pressing Cmd10-Unit

Service Info, then F6=Edit. Service options are user-defined and may .
pertain to any aspect of scheduled maintenance.

Edit Unit Service Info Screen

Inquire/Update Service Units
Edit Unit Service info

COLEOL Ship To MINHOL
COLEMAN FORKLIFT CORP. ‘INHARO WHOLESALE BURLINGTON
2300 Iowa sP
BELLINGHAM WA 98226 BURLINGTON WA 98233
Make Model Ye Serial # Hourmeter Div Group Option
AMAZON 2000 97 FOOL 10.0 A 2

 

Inst Date 90 Day 1 Year 5 Years  CFPM End
1/01/97 4/01/97 1/01/98 12/31/97

SM Begin .. 1/01/97 SM End... 12/31/97 SM :

SM Type... FSM SM Freq . . 30 SM Due Type
SM Rate . 5 - 55.00 Cons Rate . 36.00 Labor Hours = 2.5
SM Due... SM Prev... 1/01/97

SM Due Hr. . 50.0 SM Prev Hr . 8.0

Note : The 3 most recent note lines are displayed.
Press F9<Note to see more notes or add notes.
There is no limit to the number of note lines.
F4=Prompt F9=Note Fl2=Previous F15=Parts F16=Costs

 

On this screen, you can select from a list of valid service options by
pressing F4=Prompt. Follow the steps below to create the list.


[=| X10.3-12 MAINTAIN SERVICE OPTIONS oc

### How To Run

© From the Service Management Utilities Menu (X10-3), select option
12, Maintain Service Options. The Maintain Service Options screen is
displayed in CHANGE mode (illustrated below) if you have current
options; if not, it is displayed in ADD mode:

A ARR EQUIPMENT SALES Maintain Service Options

Option
cede
TECH

4=Delete request

Opt Option Option Description
code {
TECH? ‘Technician 2 job .
HCH ‘Technician 3 only

wiRE wire grade

F3-Exit F6=Add  F12=Previous  F21=Print

 

© Change as many option codes and their descriptions as needed.

© Press [Enter] to record your changes.

Q To add new codes, you can press F6=Add to toggle to ADD mode. A
blank list for new codes and descriptions will be displayed. Enter as
many codes and their descriptions as you want. Press [Enter] to add.
them to the list and get another blank list. Press Fé=Change to return to
CHANGE mode, where you can view and change the entire list.

LL


X10.3-12 MAINTAIN SERVICE OPTIONS [=]

O To print the list of current option codes, press F21=Print from the Edit
Option Table in either ADD or CHANGE mode or select Options File
List (X10.2-11).

C To go back to the Service Utilities Menu, press F12=Previous or
F3=Exit from the Edit Option Table in either ADD or CHANGE mode.

SERVICE MANAGEMENT


Notes:

## CHAPTER X10.3-13

MAINTAIN PARTS WARRANTY

### Introduction

Use this option to stipulate the default number of days parts will be
warrantied and to maintain a list of parts that have different warranty
periods. To print the list of parts, press F21=Print on the Maintain Parts
Warranty screen, or select option 12, Warranties File List, from the
Service Reports Menu (X10-2).

### How To Run

0 From the Service Management Utilities Menu (X10-3), select option
13, Maintain Parts Warranty. The screen is displayed in CHANGE
mode if you have current options; if not, it is displayed in ADD mode,
as illustrated below:

Maintain Parts Warranty List

Default Days Warranty 00365

Part Number Of
Number Days Warranty
alo0g1 12
£10006 30
A10008 120
10094 60
Al111 30
Al1211 360
AL1212 60
12004 60
A23456 360

FisExit F6=Add F12=Previous F21=Print


[2] X10.3-13 MAINTAIN PARTS WARRANTY

© In Add mode, enter part numbers. Press [PgDn] for another blank
screen. Press [Enter] to add the parts to the list.

0 To toggle to CHANGE mode, press F6=Change.

OD To print a list of the part numbers with different warranty periods, press
F21=Print or select Warranties File List (X10.2-12).

O To return to the Utilities Menu, press F3=Exit or F12=Previous.
(
Ne

## CHAPTER X10.3-14

PURGE REPAIR PARTS HISTORY

### Introduction

Use this option to delete parts history through a selected date. This
pertains only to a customer’s unit repair history and the parts that have
been installed on the unit for the current and previous owners. It does not
apply to Part Sales History (5-7).

### How To Run

O From the Service Utilities Menu (X10-3), select option 14, Purge
Repair Parts History. You are prompted for a cut-off date:

A LINDA FLEET Parts History Maintenance
Purge Parts History

Delete all part history records
prior to and including: 4/05/97

F3=Exit F12=Previous
CONFIRM: N (¥/N)

 

OD Enter a date and press [Enter]. A confirmation message appears at the
bottom right corner of the screen, as illustrated above.

C1 Type Y to proceed with the deletion or N to cancel your request. You
don't need to press [Enter] again.


[| X10.3-14. PURGE REPAIR PARTS HISTORY Co

0 To return to the menu, press F3=Exit or F12=Previous.

## CHAPTER X10.3-15

PURGE UNIT REPAIR COST HISTORY

### Introduction

Use this option to delete unit cost records through a selected date. A unit’s
repair cost for the current owner or all owners can be reviewed and printed
by pressing F16=Costs on the Unit Service Information screen.

### How To Run

 

 

 

 

From the Service Utilities Menu (X10-2), select option 15, Purge Unit
Repair Cost History. The following prompt for a cut-off date is
presented:

A LINDA FLEET Purge Unit Repair Cost History

Delete all unit cost records
prior to and including: 6/21/97

F3cExit F12=Previous
CONFIRM: N (Y/N)

 

O Enter a date and press [Enter]. A confirmation message appears at the


[2 X10.3-15 PURGE UNIT COST REPAIR HISTORY Cc

bottom right comer of the screen.
O Type Y to proceed with the deletion or N to cancel your request. You
don't need to press [Enter] again.
O To return to the menu, press F3=Exit or F12=Previous.

LC

## CHAPTER X10.3-16

MAINTAIN SHIP TO LOCATION

### Introduction

Use this option to associate multiple "Ship to" addresses with a customer's
address. During the file conversion that accompanied this enhancement, all
customers were assigned their own address as a "Ship to." Additional assignments
for current customers and new customers must be made manually.

In Fleet Management, the customer is the billing address and the “Ship To”
address is where the unit is physically located. “Ship To” is not the same as a
contact. A contact is simply a record of one or more persons who can be
contacted in regard to contracts, maintenance, and units. However, the same name
may be both a “Ship To” and a contact, in which case, it must be set up both here
and in Customer Service Information.

### Contents

ENTRANCE SCREEN ......sssssssssosscsssssserenrnesnnessrsesseeensstetaneauansntenencensneaenensorensanasoes 2
SHIP TO LOCATION SCREEN ......:sscssssssssssseneorssssestssensnessnarecsnsnanoneneatnssssenenenencen 3
ADD NEW ADDRESS

 

xa3g.doc 1/16/01 1


2 X10.3-16 « MAINTAIN SHIP TO LOCATION RELEASE 10.1 c

### Entrance Screen

D From the Service Utilities Menu, select option 16, Maintain Ship To Location.
A prompt for a “Sold to” address is presented, as illustrated below.

 

Maintain Ship To Location

Enter Sold to Address #. - - -

F3=Exit F4=Prompt F12=Previous

 

1 Type the address or press F4=Prompt to select from a list of system addresses.
Press [Enter].


SERVICE MANAGEMENT X10,3-16 « MAINTAIN SHIP TO LOCATION 3

 

### Ship To Location Screen

 

Ship To Locations for: FOURO1 - FOURTH CORNER FORKLIFTS x11802

Type option, press Enter - or - position by name, city or zip code
1=Select 2=Change 4=Delete

 

Opt Name City/State Zip Code Open Close
— BILL BRADLEY ARLINGTON, WA 98223 6:30 20:30
— .M. BURKIN BELLINGHAM WA 98226 8:00 17:30

F3=Exit F5=Refresh F6=Add new address Fi2=Previous Roll

 

Option 1=Select is not used in Maintain Ship To Location.

O To change an address in the list, select it with 2=Change.
O To delete a ship to address, select it with 4=Delete.
O To add anew address, press F6=Add new address.


4 X10.3-16 ¢ MAINTAIN SHIP TO LOCATION RELEASE 1
eee SSeS ive

 

### Add New Address

Ship To Locations for: FOURO1 - FOURTH CORNER FORKLIFTS x11802

Type option, press Enter - or - position by name, city or zip code
1=Select 2=Change 4=Delete

Name, . 2...

Extended name .

Address . ae

Extended address.

City/State. 2...

Zip code. . 2. 2. Open
Salesman. . . . . . Close .

Tax code... 2. . __ Map Loc
Discount code . . . _ Metro . _
Validate blanks . . ¥ (¥ fox name, city and zip)

Fa=Prompt address F12=Return Add new address

F3sExit F5=Refresh F6=Add new address F12=Previous Roll

 

O With the cursor in the Name field, press F4=Prompt address to select from a
list of system addresses (may be cash customer, vendor, etc).

Ship To Locations for: FOURO1 - FOURTH CORNER FORKLIFTS

Select Address x01000
Edit codes. : *ALL
=Select Division . ; *ALL

 

 

Opt Name City/state Zip Code Addr #
BRADLEY, BILL ARLINGTON, WA 98223 BRADO1
BRANDT, BILL RENTON, WA. 999999999 BRANOL
BRINE, JEREMY LYNDEN, WA 98264 BRINO1
BURPEE, ALFRED BELLINGHAM, WA 98225 BURPOL

1 CAIN CONSTRUCTION C,CAROLYNN Bellingham, WA 000001

F3=Exit Roll

F3-Exit F5=Refresh F6=Add new address F12=Previous Roll


SERVICE MANAGEMENT X10.3-16 » MAINTAIN SHIP TO LOCATION 5

O Select the customer with 1=Select. The customer’s information will be
retrieved to the Ship To box.

Ship To Locations for: FOURO1 - FOURTH CORNER FORKLIFTS xX11802

Type option, press Enter - or - position by name, city or zip code
1=Select 2=Change 4=Delete

Opt Name Name. . . . . . . . Carolynn Cain Construction ¢
BILL BRADLEY Extended name .

L.M. BURKIN Address . . . . . . 858 Timberlake Way
Extended address. .
City/State. . . . . Bellingham, WA
Zip code. . . . . . 98225 Open .
Salesman... . . - Close .
Tax code... -.- A Map Loc
Discount code... Metro .
Validate blanks . . ¥ (¥ for name, city and zip)

F4=Prompt address F12=Return Add new address

F3=Exit F5=Refresh Fé=Add new address F12=Previous Roll

 

O Press [Enter] to return to the Ship To Locations screen. Press F5=Refresh to
sec the entire list of Ship To Locations.


X10.3-16 » MAINTAIN SHIP TO LOCATION

Notes:

## CHAPTER X10.3-17

MAINTAIN UNIT SERVICE INFO

### Introduction

Use this option when you need to enter contracts for a lot of units at once and
want a more direct path to the Edit Unit Service Information screen, especially
during initial setup.

### Contents

ENTRANCE SCREEN ovessesseccsssssssssseronerserenneesenserssacsssernenssnenesunepsvenentnsnsaratsegraneaen
UNIT SERVICE INFO .....sccsessessessssserssssnsseserssnessarenesestansosaunerssnsesaeauararesonenssersntoeee

xa3h.doc 1/16/01


2 X10.3-17 « MAINTAIN UNIT SERVICE INFO RELEASE 10.1 Cc .

### Entrance Screen

O From the Service Utilities Menu, select option 17, Maintain Unit Service Info.
All current “Ship To” addresses arc listed with the units assigned to them.

A A&R EQUIPMENT SALES Maintain Unit Service Info List VSOZDER

Address # Model Make Serial #

1sSelect C=Cost N=Notes P=Parts


Address # Model Make Serial # © Unit # Option
AAROOL 3366 KAWASA, 2002

ADAMOL 2010R uD LHDLDBL19GY502347 2222 TECH2
ADAMOL 8870 CASE 68888 WIRE
BODAOL 6600 FORD 621249

BOULO1 6600 FORD 002468 TECH
BOULO1 7600 FORD 637578 TECH?
COLEOL 2000 AMAZON FOO TECH
COLEOL 2000 AMAZON F002

COLEOL 2000 AMAZON FOO3 (
COLEOL 2000 AMAZON FOO4

COLEOL 2000 AMAZON F005

COLEOL 2000 AMAZON F006

COLEO1 2001 AMAZON F009

F3-Exit F12=Previous

 

 

1 Use the position prompts at the top of the screen or scroll by pressing [PgDn]
to locate the name you want, which appears in the first column. In the second
column are the units that belong to the customer.

The cost, notes, and parts function keys are accessible from the Unit Service
Information screen in Edit mode or they can be accessed directly by using
the options “C,” “N,” and “P.” These options are covered in the section, Unit
Service Information, in both the Fleet Management Guide and CHAPTER
X10-1, INQUIRE/UPDATE SERVICE UNITS FOR FLEET
MANAGEMENT.

O To display unit service information, select 1 or more customer addresses/units
with 1=Select and press [Enter]. See Unit Service Info.
CO To maintain costs, select 1 or more customer addresses/units with C=Cost.
O To maintain notes, select 1 or more customer addresses/units with N=Notes.
O. To maintain parts, select 1 or more customer addresses/units with P=Parts. C


SERVICE MANAGEMENT X10.3-17 « MAINTAIN UNIT SERVICE INFO 3

 

### Unit Service Info

Selecting a customer address/unit from the Entrance screen displays the Unit
Service Info List. To edit values on this screen, press Fo=Edit.

 

A A&R EQUIPMENT SALES Maintain Unit Service Info

Sold To COLEO1 Ship To MINHOL
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233
Make Model yr Serial # Kourmeter Div Group option
AMAZON 2000 97 F001 20.0 A 20 TECH

Inst Date 90 Day 1 Year 3 Years 5 Years  CFPM End
1/01/97 4/01/97 1/01/98 12/31/97

SM Begin .. 1/01/97 SM End... 12/31/97 !

SM Type... SM Freq. . 30 SM Due Type D
SM Rate... Cons Rate . 36.00 Labor Hours = 1.5
sw Due... SM Prev .. 1/01/97 Contract Number
SM Due Hr. . SM Prev Hr .

Note : The 3 most recent note lines are dispiayed.
Press F9=Note to see more notes or add notes.
‘There is no limit to the number of note lines.

FisExit F4sPrompt F9=Note Fl2=Previous F15=Parts F1é=Costs

 

O) Enter a date in the field labeled "SM Begin."

To enter notes pertaining to the unit, press F9=Note. Or, you can select the
customer with N=Notes at the Unit Search All Customers screen. See Nofes in
Unit Service Information in the Fleet Management Guide or CHAPTER X10-
1, INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGEMENT.
To review parts that have been installed on the unit, press F15=Parts. Or, you
can select the customer with P=Parts at the Unit Search All Customers screen.
See Parts in Unit Service Information in the Fleet Management Guide or
MANAGEMENT.

O To review costs on the unit, press F16=Costs. Or, you can select the customer
with C=Costs at the Unit Search All Customers screen. See Costs in Unit
Service Information in the Fleet Management Guide or CHAPTER X10-1,
INQUIRE/UPDATE SERVICE UNITS FOR FLEET MANAGMENT.


X10.3-17 « MAINTAIN UNIT SERVICE INFO

Notes:
-_

## CHAPTER X10.3-18

ASSIGN UNITS TO SHIP TO LOCATIONS

### Introduction

Use this job to change a unit to a different Ship To location from the original
owner. Before a Ship To address can be assigned to a unit in this job, it must be
associated with the customer's address in Maintain Ship To Location (X10.3-16).
The conversion process assigns each customer address to itself; however, future
additions must be assigned manually. There is no limit to the number of “Ship
To” addresses that can be assigned to the same “Sold To” customer (owner)
addressi#.

 

### Warning

All customers must have their own address as a Ship To address, regardless of
whether any units are assigned to it.

### Contents

ENTRANCE SCREEN

ASSIGN UNITS TO SHIP TO LOCATION

SELECT SHIP TO ADDRESS SCREEN

xaSi.doc 1/16/01


2 X10.3-18 « ASSIGN UNITS TO SHIP TO LOCATIONS RELEASE 10.1

### Entrance Screen

From the Service Utilities Menu (X10-3), select option 18, Assign Units to Ship
to Locations. The following prompt for a “Sold to” address is presented.

A-A&R EQUIPMENT SALES Change Unit Ship to for Customer

Enter Sold to Address #. . . . COLEQ1

F3=Exit F4=Prompt F12=Previous

0 At the prompt, enter a “Sold to” address number, and press {Enter]. A list of
the customer's units appears on the Assign Ship To Address screen.

 

an


SERVICE MANAGEMENT X10.3-18 « ASSIGN UNITS TO SHIP TO LOCATIONS 3

### Assign Units To Ship To Location

A A&R EQUIPMENT SALES Assign Units to Ship to Location VSO5DFR

Sold To COLEO1
COLEMAN FORKLIFT CORP.
2300 IOWA sT

Make Serial #

2=Change

Opt Model Serial # ¢ Unit# Ship To Name

2000 FOOL MINHARO WHOLESALE BURLINGTON
2000 F002 MINHARO WHOLESALE BURLINGTON
2000 F003 MINHARO WHOLESALE ANACORTES
2000 Fo04 MINHARO WHOLESALE ANACORTES
2000 FOS MINHARO WHOLESALE SEDRO WOOL
2000 FO06 MINHARO WHOLESALE BURLINGTON
2001 F009

F3=Exit F12=Previous

 

O To assign 1 or more units to a different Ship To address, select them with
2=Change and press [Enter]. You can select more than 1 unit at a time.


4 X10.3-18 ¢ ASSIGN UNITS TO SHIP TO LOCATIONS RELEASE 10.1 C 7

 

SELECT SHIP TO ADDRESS SCREEN

AS Select Ship To

Sold To COLEO1
COLEMAN FORKLIFT CORP.
2300 IOWA ST

1sSelect

Opt Name City/State Open Close

L.M. BURKIN BELLINGHAN WA 8:00 17:30
CAROLYNN CAIN CONSTRUCTION BELLINGHAM, WA 7:30 19:30

F3=Exit F12=Previous

 

CO Select the new Ship To address with 1=Select and press [Enter]. The Assign
Units to Ship To Location screen will be re-displayed. The new Ship To name
will be listed for the unit.

## CHAPTER X10.3-19

MAINTAIN HOURMETERS

### Introduction

The purpose of this option is to enable you to reset hourmeter readings on all
units at a particular “Ship to” location at the same time. From the same screen,
you can investigate cost, maintain notes, review parts, or display the Unit Service

Information screen.

### Contents

ENTRANCE SCREEN .......ccssscssesnesearennscrorseesssrsssnesnenesentonessnrecersnanenneosnnneranecera ones 2
SELECT SHIP TO SCREEN.........s:scssecsessarsssessnsssessentsnensnsnsnesseseasaversenssnnsortonsen sees 3

 

MAINTAIN HOURMETERS SCREEN

xa3j.doc 1/16/01


2 X10.3-19 « MAINTAIN HOURMETERS RELEASE 10.1

### Entrance Screen

O From the Service Utilities Menu (X10-3), select option 19, Maintain
Hourmeters. The following prompt for a “Sold to” address is presented.

A A&R EQUIPMENT SALES Maintain Hourmeters

Enter Sold to address #

F3<Exit F4=Prompt F12=Previous

O Atthe prompt, enter a “Sold to” address number, and press [Enter]. A list of
“Ship To” Jocations currently associated with the customer's units is displayed
in the Select Ship To window.

 

{


SERVICE MANAGEMENT X10.3-19 e MAINTAIN HOURMETERS

SELECT SHIP TO SCREEN

A- Select Ship To VSYXSRR

Sold To COLEO1
COLEMAN FORKLIFT CORP.
2300 IOWA ST

1=Select

Opt Name City/State Open Close
— uM. BURKIN BELLINGHAM WA 8:00 17:30
_ CAROLYNN CAIN CONSTRUCTION BELLINGHAM, WA 7:30 19:30

F3sExit F12=Previous

O Select a “Ship to” address with 1=Select, and press [Enter]. A list of the units
currently assigned to the “Ship to” address is displayed on the Maintain
Hourmeters screen.


 

X10,3-19 « MAINTAIN HOURMETERS RELEASE 10.1 C~

MAINTAIN HOURMETERS SCREEN

A A&R EQUIPMENT SALES Maintain Hourmeters VSQSDFR
Sold To COLEO1 Ship To MINHOL
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233

Make Serial ¢ c Unit #

i=Select C=Cost NsNotes P=Parts

Opt Model Make Serial # Cc Unit # Hourmeter
2000 AMAZON FOOL 10.0
2000 AMAZON Fo02 20.0
2000 AMAZON FO06 6000.0

 

© To change the hourmeter readings, simply type in the new number and press (
[Field Exit]. Decimals are allowed on this screen: enter 7150.8 as 7150.8. If
you enter 71508, the system will assume you mean 71,508.0.

Note that from this screen, you can also investigate cost, maintain notes, and
review parts directly. Or, you can select a unit with 1=Select, and display the Unit
Service Information screen. From the display screen, the same options, Cost,
Notes, and Parts, are available, or you can press F6=Edit to maintain fields on the
Unit Service Information screen.

## CHAPTER X10.3-20

INQUIRE/UPDATE SERVICE CONTRACTS

### Introduction

Use this option to record details about service contracts including the
contract number, a customer address number, which could be a billing or
ship to address, a short description, and terms. Thermo King dealers
should use the customer address number field for a billing address.

After a contract is entered, one or more units can be associated with it on
the Unit Service Info screen in Inquire/Update Service Units. Each unit
can be associated with only one contract.

### Entrance Screen

From the Service Utilities Menu (X10-3), select option 20, Inquire/Update
Service Contracts. A list of service contracts is displayed.

A-AER EQUIPMENT SALES  Inquire/Update Service Contract
Contract
Number

QeEdit 4=Delete 7-Display Units on Contract

Opt Contract Contract Description
Number
- 123 service contract
- 456 Service Contract
789 Breakdown contract

FisExit Fé=Add Fl2=Previous

 

Adding a Service Contract


[| X10.3-20 INQUIRE/UPDATE SERVICE CONTRACTS

To add a service contract, press F6=Add on the Entrance Screen. The
Inquire/Update Service Contract screen is displayed.

A-AGR EQUIPMENT SALES  Inquire/Update Service Contract ADD

Contract Number . . . Customer Address # .
Contract Description -
Contract Terms... .

F3=Exit F12=Previous

Enter the information. Press [Enter] to record it and return to the Entrance

screen.

Contract Number 9 digits. Required.

Customer Address # 6 characters. Required. Press F4=Search to
select from a list of customers. This field can
be used for a billing or ship to address.
Thermo King dealers should use it for a

billing address.

Contract Description 30 characters. Displayed on the Entrance
screen.

Contract Terms 4 lines of 50 characters.
Le


X10.3-20 INQUIRE/UPDATE SERVICE CONTRACTS |

Changing a Service Contract

To change a service contract, select it with 2=Edit. The Inquire/Update
Service Contract screen is displayed in change mode.

A-AGR EQUIPMENT SAKES Inquire/Update Service Contract CHANGE VSTSE1R

contract Number. . : 123 Customer Address # -
Contract Description . Service Contract. —
Contract Terms . . . . Annual contract:payment due 5-1-99.

F3=Exit F12=Previous

 

Make the necessary changes. Press [Enter] to record your changes and
return to the Entrance screen.

Deleting a Service Contract

Make sure you want to delete a contract, because there is no confirmation
screen. On the Entrance screen, select the item you want to delete with

SERVICE MANAGEMENT


[| X10.3-20 INQUIRE/UPDATE SERVICE CONTRACTS om

4=Delete, and press [Enter]. The item is immediately deleted from the list.
Displaying Units on a Service Contract

To display the units on a service contract, select it with 7=Display Units
on Contract. The Display Contract Units screen lists the units for which
there are contracts.

A-A&R EQUIPMENT SALES Display Contract Units
Contract Number 123

Serial #
0128813R0B

F3=Exit  F12=Previous

 

This connection is made on the Unit Service Info screen in Inquire/Update
Service Units (X10-1), which is illustrated on the next page.

RELEASE 2.3 a


X10.3-20 INQUIRE/UPDATE SERVICE CONTRACTS

A AGR EQUIPMENT SALES

Inquire/Update Service Units

000001,

Carolynn Cain Construction ¢
858 Timberlake way
Bellinghan, WA 96225

sold To Ship To 000001
Carolynn Cain Construction
858 Timberlake way

Bellingham, WA 98225

Make
CASE

Model Ye
600c 96

Inst Date
$/26/96

90 Day
8/26/96

8/26/96

SM Begin . -
SM Type .
SM Rate .
su tue . .
SM Due Hr .

Note +

F3=pxit  Fa=Prompt

F9=Note

Serial #
450089ST-098

1 Year
8/26/97

SM End .
SM Freg
Cons Rate
SM Prev

SM Prev Hr .

F12=Previous

3 Years
8/26/00

8/26/00

F15=Parts

Hourmeter Div Group option

347.900 A

5 Years = CFPM End

re
SM Due Type
Labor Hours = ___
Contract Number

Plé=Costs

 

With the cursor in the Contract Number field, press F4=Prompt to select

from a list of contracts.

SERVICE MANAGEMENT


X10.3-20 INQUIRE/UPDATE SERVICE CONTRACTS a

A-AGR EQUIPMENT SALES Select Service Contracts
Contract

‘Number

999999999

1=Select

Contract Contract Description Customer Number
Number

123 Service Contract GRADOL

456 Service Contract ADAMOL

789 Breakdown contract ADAMOL

F3eExit Pd=Prompt F12=Previous {

 

Select the appropriate contract with 1=Select. Press [Enter] to retrieve the
contract number and return to the Unit Service Info screen.

Lo

## CHAPTER X10

SERVICE MANAGEMENT MENU
FOR FLEET MANAGEMENT

### Introduction

The Service Management System (SMS) is an additional product, which is
available for purchase. With it, you can create service work orders and
automatically record and track detailed service history for each unit. You can
store standard jobs, with parts, labor, and description, ready to add to a customer's
service work order as a complete job. In the most advanced usage, the system will
compare the service history of a unit to the recommended service table, and
recommend tasks that should be performed. You may then add other jobs to the
list to be performed, all of which are recorded in detail, to the unit service history.

Fleet Management is compatible with the Truck/Van Inventory Additional
Product. Its primary focus is the management of scheduled maintenance for
customers who own fleets of equipment located at different sites. Fleet
Management makes it possible to schedule maintenance by date or hourmeter and
to charge against a pre-established contract for maintenance. .

 

NOTE
L Unique serial numbers are required for both SMS and Fleet Management.

xa_fleet.doc 1/16/01 1


X10 © SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

 

### Contents

 

SERVICE MANAGEMENT SYSTEM FEATURES
FLEET MANAGEMENT FEATURES

 
  
 
 

SUMMARY OF MENU OPTIONS...

Service Management Menu

Service Reports Menu...

Service Utilities Menu ..
OVERVIEW OF SERVICE MANAGEMENT .........:-:-----ssecsrsnerevenessentensonetsstsnenenee 13
OVERVIEW OF FLEET MANAGEMENT .. 24

 
 

  
  
  

Unit Index o..eseecscstesneseseneerneneee
Assigning “Ship To” Addresses
SHIP TO LOCATION SCREEN .......c.scccssssscssssessessnsseseessersasanecensnersensesneneasnesseoeae 17
ADD NEW ADDRESS .......cersescssrssnsscerernereneoen 18
Assigning Units to a “Ship To” Address . .20
Ship To Location Info Screen.. 23

Unit Service Info Screen.......
Scheduled Maintenance Due Report.
Point of Sale Work Orders

 
 
 

   
 
 
 
 

 

Service Info Maintenance—| with “Ship To’s”.

Ship To Location Info—Purchase Orders (by “Ship To”). 30
Option Table...... 30
Enter Contracts. 30

Scheduled Maintenance Information ..
COMtACHS..... ee eercessenesseneracessneeeacenecseaneensessesesnees


X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 3

### Service Management System Features

Your Service Management System is fully integrated with Point of Sale, Parts,
Accounts Receivable and the General Ledger. SMS provides 2 sessions at Point
of Sale. A command key toggles back and forth between 2 documents.

At Point of Sale, the following types of documents (modes) are available, all
with the same "look and feel":
— Active documents (work orders)
— Standard jobs
— History documents, including:
a) Closed & posted work orders with serial numbers (former active
documents)
b) Documents created expressly for history records, created at POS in
"History documents" mode

Standard jobs

Standard jobs can be created directly or copied from work orders and
accumulated over time. Standard jobs, each identified as a Group:Job, can be
added to Service Tables and Recommended Maintenance. As the Group:Job
identifier is expanded to its actual detail lines on a work order, the usual
checks are made for special pricing, supersession, availability, etc. (same as
Copy-Lines).

Labor lines shortcut

When a standard job is used on a work order, a job code entered on the POS
Entrance screen takes you directly to a labor line on the detail screen. From
there you can add labor and other types of lines, and then close the work
order.

Customer's unit number

You can use the customer's unit number to locate the unit more quickly at
POS or Inquire/Update Service Units. It is also printed on the work order.
Series code

Equipment can be identified by a 3-characier series code, which may often be
more helpful than organizing service tables strictly by make/model and year.
Reports on the Service Reports Menu can be displayed on screen or printed.
Equipment searches by:

— Customer name

License number

Unit number

Serial number (same as VIN). Must be unique.

— Customer's unit number

Service history tracking including all work performed on equipment. Detail
can be preserved as long as you need it (or disk space permits), then collapsed
in stages.

Equipment is automatically added to the service system when it is sold.


4 X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

= Recommended service maintenance displays:
Each service job

Real or metered time interval between service
Estimated prices for labor, based on flat sate
— Standard flat rate time for each service job

= Add or delete jobs from recommended list, create & print initial repair order.
= Print service customer information:
— Mailing labels for service sales and follow up on any combination of:

a) Make e) Model
b) Year f) Last service date
c) Purchase date g) Needed service

d) Reminder for a service job on a certain date
— Run report printing any combination of above information
= Update service history information:

— Add previous service history
— Update history when changing a serial number (VIN)


X10 e SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 5

### Fleet Management Features

The Fleet Management System was designed with the following objectives in
mind:

= Easy access to ship to location information, unit information, and unit history
from Point of Sale.

= Improved efficiency for dispatcher to obtain a monthly customer list for
customers on Schedule Maintenance.

® Quick access to unit history for parts installed on a specific unit for warranty.

= Capture of unit repair cost for marketing service, parts, new equipment sales.

" Marketing analysis of unit population by age, cost of repair, etc. for service,

 

parts, and sales.
NOTICE
As in Service Management, unique serial numbers are required for Fleet
Management.

 

Very briefly, the enhancements made to the Service Management System for
Fleet Management include:

= On Point of Sale work orders, all users are warned when a part is still on
warranty for any unit that has been set up in Fleet Management. A pop-up
window allows you to change the billing to Internal (I) or Warranty (W). After
a part line is changed to Warranty, subsequent lines default to "W," which is
the same way Point of Sale works without Fleet Management. See page 29.

® All new parts are warrantied for the number of days set as the default in
Maintain Parts Warranty (X10.3-13).

«= Each part with a different warranty period must be entered in Maintain Parts
Warranty (X10.3-13).

= To determine whether a part is still under warranty, the system checks the
install date, then the Maintain Parts Warranty table.

« Anew command key, Cmd8-Unit Index on the Inquire/Update Service Units
entrance screen. After a customer's ID (system address) is entered, you can
select the appropriate unit from a list. The list includes all units that can be
handled in the Service Management System.

= Command keys from SMS View/Update screen to:

Rel. 10.1 — Ship To Location Information, which includes notes, contacts, and
purchase orders (P/O's). Two main types of P/O's are displayed on the
information screen: Breakdown (BKD) and Scheduled Maintenance (SM).
Other types of P/O's can be entered. The remaining balance on SM and
BKD P/O's is updated when a work order is posted for the unit. See Ship
To Location Info Screen in CHAPTER X10-1.


6 X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

Rel. 10.1

- Unit Service Information, which pertains to the individual units in a fleet
and includes relevant dates and records pertaining to the unit's service
contract and schedule. Units can be associated with existing contracts,
which are entered in Inquire/Update Service Contracts (X10.3-20). A
Scheduled Maintenance Summary report (X10.2-8) and Scheduled

Maintenance List (X10.2.9) can be printed for a specific (or all) contract
number.

= Point of Sale Enhancements
— Anew field on the Sold To screen at Point of Sale records a "Work Date,"
from which the date of the next scheduled maintenance is calculated. In
addition, function keys provide access to notes, a record of parts installed
on the unit, and costs associated with the unit.
— The command key [F16] to scroll through units has been enhanced so that
you can select from a list instead of scrolling through the customer’s units.

Parts and costs for the current owner and previous owners provide a

complete history. In addition, the system keeps track of the date parts are
installed and their warranty period.

= Each customer address may have multiple Ship To addresses associated with
it. Units within the fleet may be assigned to different Ship To addresses,
which correspond to their locations. The initial conversion process establishes
each customer address as a Ship To address for itself. As new addresses are
entered, this process must be done manually.

The following reports have been added to the Service Report Menu (X10-2):
5. Scheduled Maintenance Due (Divisional)

6. Scheduled Maintenance Overdue (Divisional)

7. Scheduled Maintenance Contracts Ending (Divisional)

8, Scheduled Maintenance Summary (Divisional)

9. Scheduled Maintenance List (Divisional)

10. Parts History Report

11. Unit Cost Report

12. Options File List

13. Warranties File List

See CHAPTERS X10.2-5 - X10.2-13.

= The following utilities have been added to the Service Utilities Menu:
— Maintain Service Options
— Maintain Parts Warranty

— Purge Repair Parts History
~— Purge Unit Repair Cost History


X10 e SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 7

— Maintain Ship to Location

— Maintain Unit Service Info

— Assign Units to Ship to Location
- Maintain Hourmeters

— Inquire/Update Service Contracts

See CHAPTERS X10.3-12 - X10.3-20.

SUMMARY OF MENU OPTIONS

Service Management Menu

The Service Management Menu (X10) is illustrated below:

 

COMMAND
(c) DIS Corp.

1. Inquire/Update Service Units
2. Service Report Menu
3. Service Utilities Menu

23. Return to Master Menu

Ready for option number or command

—

 

The options are discussed below.

1. Inquire/Update Service Units

With this option, you can view and update information about units serviced and
sold to customers. Units and cash customers can be added. A complete service
history is kept on each unit. Recommended maintenance, which is determined by
the service table the unit is assigned to, can be displayed. In addition, a new work
order can be created with the recommended maintenance jobs already on it.

2. Service Reports Menu
See page 8.


8 X10 e SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

3. Service Utilities Menu
See page 10.

Service Reports Menu

‘COMMAND
{e) DIS Corp.

. Service Customer Target List . Scheduled Maintenance Summary
. Service Labor Analysis . Scheduled Maintenance List

. Standard Job Report . Parts History Report

. Service History Report . Unit Cost Report

. Scheduled Maintenance Due - Options File List

. Scheduled Maintenance overdue . Warranties File List

. Scheduled Maintenance Contracts Ending

23. Return to Service Menu

Ready for option number or command

ses?

 

1. Service Customer Target List

With this option, you can print a report or labels for mailings to customers who:
= Have equipment of a certain make, model or year

= Purchased their equipment during a certain time period

= Need service by a particular date

= Own equipment that is part of a recall or program

2. Service Labor Analysis Report

This report is similar to the Labor Analysis Report (X56-4) except that it analyzes
only labor lines associated with job codes. It can help you assess the performance
of individual mechanics relative to flat rate times.

3. Standard Job Report

The Standard Job Report makes it possible for you to review a range of groups
and/or jobs. The report can be displayed on screen or printed on the system
printer. You can request full detail or summary only.

4, Service History Report

This report can be requested for one customer, making it especially helpful for
reviewing maintenance for a fleet customer.


X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 9

 

5. Scheduled Maintenance Due

This report can be requested for all units whose service is due by a selected
month/date or within a selected hourmeter reading. Units serviced by date and by
hourmeter are included on the same report.

6. Scheduled Maintenance Overdue

This report lists all units whose service is overdue and includes units serviced by
date as well as by hourmeter.

7. Scheduled Maintenance Contracts Ending

The purpose of this report, which is divisional, is to calculate the annual value and
number of labor hours represented by contracts in a selected time period. To be
included on this report, the scheduled maintenance must begin on or before the
first date and end on or after the second date. In other words, the report lists
contracts that are in force throughout the entire date range you specify.

8. Scheduled Maintenance Summary

This report, which is divisional, lists units that have current contracts for
scheduled maintenance along with terms, options, etc.

9. Scheduled Maintenance List

This report, which is divisional, lists units that have current contracts for
scheduled maintenance along with terms, options, etc.

10. Parts History Report

This report lists parts installed on a particular unit for a single owner or for all
owners.

11. Unit Cost Report

This report lists costs associated with a particular unit for up to 12 selected sales
codes or all sales codes. It can be printed for a single owner only or for all
owners. You can select from a list of valid address numbers and serial numbers.

12, Options File List

The Options File List is a printout of current options, which are user-defined.
Options are set up in Unit Service Options Table (X3.10-12). They are assigned to
units on the Unit Service Information Screen, where a list of valid options is
available by pressing F4=Prompt. See CHAPTER X3.10-12, OPTION TABLE.

13. Warranties File List

The Warranties File List is a printout of current part numbers that carry a
warranty different from the default, which is set in Maintain Parts Warranty
(X10.2-13). These parts are also entered in Maintain Parts Warranty.


10 X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

Service Utilities Menu

COMMAND
(c) DIS Corp.

. Inquire/Update Service Tables . Maintain Service Options

. Inguire/Update Make Model Assignments . Maintain Parts Warranty

. Service Note Distribution . Purge Repair Parts History

. Standard Job Rename . Purge Unit Repair Cost History

. Serial Number Rename . Maintain Ship to Location
Service Divisional Profile . Maintain Unit Service Info

. Update Standard Job Parts Prices . Assign Units to Ship to Location
. Update Labor Rate for a Group . Maintain Hourmeters

. Delete a Standard Job . Inquire/Update Service Contracts
. Load Manufacturer Standard Jobs

. Correct Service History

RENE

6.
7
8
9
oO
1

Be

23. Return to Service Menu

Ready for option number ox command

sEE>

 

1. Inquire/Update Service Tables

A service table is an intermediate device that combines standard jobs (the
Group:Job created at Point of Sale) before they can be assigned to a particular
Make/Model and available for automatic inclusion in recommended
maintenance. The most straightforward technique is to name your tables the same
as your groups, although this is not required.

 

Group: Jobs can be deleted from recommended maintenance, and other
Group:Jobs can be added; however, service tables make it possible to make sure
jobs are added accurately and on schedule.

 

 

2. Inquire/Update Make Model Assignments

Use this job to assign vehicles to service tables according to make, model, year or
range of years (or series codes). This is necessary to enable the system to furnish
jobs for recommended maintenance automatically.

3. Service Note Distribution

Use Service Note Distribution to distribute notes, such as special programs or
tecall notices, to a range of units.

4. Standard Job Rename

Use this job if you want to rename the 6-character job code. All associated
information is transferred to the new job code.


X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT a

5, Serial Number Rename

Use this job if you want to change a unit's serial number or VIN. All associated
information is transferred to the new serial number or VIN (Vehicle Identification
Number)

6. Service Divisional Profile

This is a one-time setup job where defaults are established for other Service
Management jobs.

7. Update Standard Job Parts Prices

Use this option after a price update to change the prices of parts on standard jobs
according to the new prices in inventory for all standard jobs in a group.

8. Update Labor Rate for a Group

Use this option to change the labor rates on standard jobs. Updates are done for all
standard jobs in a group.

9. Delete a Standard Job
Use this option to delete a standard job from a group.

10. Load Manufacturer Standard Jobs
In this chapter, you'll learn how to load manufacturer standard jobs and how to
use them at Point of Sale. In addition, you'll learn how to change standard jobs;

however, changes are lost the next time you take this option to load manufacturer
standard jobs.

11. Correct Service History

Use this option to make corrections to serial numbers that have been entered by
mistake. Usually these are typographical errors that cause variations of a serial
number to be set up as separate units. For example, serial number
2P4FH5531LR621529 may also be entered as 2P4FH5531LR621528 and
2P4FH5531LR621592. You can use this job to eliminate the incorrect serial
numbers and combine service history records under the correct serial number.

12. Maintain Service Options

Use this job to enter a table of service option codes and their descriptions. The
codes may be up to 8 characters each; the descriptions, 30 characters. To print the
list of options, press F21=Print on the Maintain Service Options screen, or select
option 11, Options File List, from the Service Reports Menu (X10-2).

One service option can be associated with a unit on the Edit Unit Service
Information screen, which is illustrated below. This screen is accessed from the
Inquire/Update Service Units screen by pressing Cmd10-Unit Service Info, then


X10 * SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 70.1

F6=Edit. Service options are user-defined and may pertain to any aspect of
scheduled maintenance.

13. Maintain Parts Warranty

Use this option to specify the default number of days that parts are warrantied and
to maintain a list of parts with warranty periods that are different. To print the list
of parts, press F21=Print on the Maintain Parts Warranty screen, or select option
12, Warranties File List, from the Service Reports Menu (X10-2).

14. Purge Repair Parts History

Use this option to delete parts history through a selected date. This pertains only
to a customer’s unit repair history and the parts that have been installed on the
unit for the current and previous owners. It does not apply to Part Sales History

(X5-7).

15. Purge Unit Repair Cost History

Use this option to delete unit cost records through a selected date. A unit’s repair
cost for the current owner or all owners can be reviewed and printed by pressing
F16=Costs on the Unit Service Information screen.

16. Maintain Ship To Location

Use this option to associate multiple "Ship to" addresses with a customer's
address, During the file conversion that accompanied this enhancement, all
customers were assigned their own address as a "Ship to." Additional assignments
for current customers and new customers must be made manually.

17. Maintain Unit Service Info

Use this option when you need to enter contracts for a lot of units at once and
want a more direct path to the Edit Unit Service Information screen, especially
during initial setup for Ship To Location Info and Unit History enhancement.

18. Assign Units to Ship to Location

Use this job to change a unit to a different Ship To location from the original
owner. Before a Ship To address can be assigned to a unit in this job, it must be
associated with the customer's address in Service Information Maintenance
(X10.3-16). The conversion process assigns each customer address to itself;
however, future additions must be assigned manually. There is no limit to the
number of “Ship To” addresses that can be assigned to the same “Sold To”
customer (owner) address#.

 

### Warning!

All customers must have their own address as a Ship To address, regardless of
whether any units are assigned to it.


X10 » SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 13

 

19. Maintain Hourmeter

The purpose of this option is to enable you to reset hourmeter readings on all units
at a particular “Ship to” location at the same time. From the same screen, you can
investigate cost, maintain notes, review parts, or display the Unit Service
Information screen.

20. Inquire/Update Service Contracts

Use this option to record details about service contracts including the contract
number, a customer address number, which could be a billing or ship to address, a
short description, and terms. Thermo King dealers should use the customer
address number field for a billing address.

After a contract is entered, one or more units can be associated with it on the Unit
Service Info screen in Inquire/Update Service Units. Each unit can be associated
with only one contract.

### Overview Of Service Management

The steps involved in successful Service Management are:

1) Create standard jobs at Point of Sale. When you select Standard Jobs mode,
the address number used on the entrance screen is the group name and the
document number you assign is the job name. Every standard job can then be
referred to as a Group:Job.

2) Assign Group:Jobs to tables, usually with the same names as the groups
(Inquire/Update Service Tables, X10.3-1).

3) Link equipment to tables according to make, model, years or series code.
(Inquire/Update Make Model Assignments, X10.3-2).

Tables of Group:Job combinations are automatically included in recommended
maintenance, which is available from Inquire/Update Service Units (X10-1) or
from Point of Sale (X5-1, [Cmd18}).

Please refer to the SMS Diagrams, which precede this chapter and illustrate the
integration of SMS and Point of Sale. In particular, see diagram #2, How to
Use Standard Jobs.


14 X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

### Overview Of Fleet Management

Most features in Fleet Management are concentrated within Inquire/Update
Service Units (X10-1) and can be handled on a case-by-case basis. There are
shortcuts on the Service Utilities Menu, and these will be pointed out but not
illustrated in this section.

To illustrate the features, we'll follow an example of a customer, Coleman
Forklift Corp., who has a fleet of 6 forklifts. The concepts can be illustrated in a
table, which will expand. Let’s start with the owner and the 6 forklifts.

 

 

 

 

 

 

 

By pressing Cmd8-Unit Index at the Inquire/Update Service Units entrance
screen, you can see the units listed by serial number.


X10 *® SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 15

 

Unit Index

 

A&R SALES & RENTALS Inquire/Update Service Units ¥A100-101 4
Division: A View/Update Search Only -

Address # . - COLEOL or
License #

Serial#

unit # .. c Unit #

Unit Search
1=Select.
Opt Serial # Make
FOOL AMAZON
F002 AMAZON
FOO3 AMAZON
FOO AMAZON
FOOS AMAZON

F3=Exit F12=Previcus

tmds—-Service History cmde-Recommended Maintenance Cmd8-Unit Index

 

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
"The “Ship To” addresses must be associated with the “Sold To” address
= Each unit must be associated with a “Ship To” address.


16 X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 40.1

Assigning “Ship To” Addresses

For this step, we need one of the utilities on the Service Utilities Menu (X10-3),
which is illustrated below:

COMMAND
{c) DIS Corp.

. Inquire/Update Service Tables 12. Maintain Service Options
. Inquire/Update Make Model Assignments 13. Maintain Parts Warranty
Service Note Distribution 14. Purge Repair Parts History
Standard Job Rename 15. Purge Unit Repair Cost History
Serial Number Rename 16. Maintain Ship to Location
. Service Divisional Profile 17. Maintain Unit Service Info
. Update Standard Job Parts Prices 18. Assign Units to Ship to Location
. Update Labor Rate for a Group 19. Maintain Hourmeters
Delete a Standard Job 20. Inquire/Update Service Contracts
. Load Manufacturer Standard Jobs
. Correct Service History

23. Return to Service Menu

Ready for option number or command
6

=Re>

Select option 16, Maintain Ship to Location. In this job, we'll be able to associate
3 “Ship To” addresses with Coleman Forklift Corporation.

 


X10 e SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 7

 

First, we’re prompted for an address:

 

A A&R SALES & RENTALS Maintain Ship To Location VSOQPVR

Enter Sold to Address #. . - . COLEO1

 

At this prompt, we’ll enter Coleman Forklift’s address, which is the “Sold To”
address, and press [Enter]. The first time you see this screen, the only “Ship To”
address will be the same as the “Sold To.” That is because the conversion assigns
customers’ own addresses as their “Ship To” address in Receivables Maintenance.

On the screen illustrated below, 2“Ship To” addresses have been assigned.

SHIP TO LOCATION SCREEN

Select Ship To Locations

Ship To Locations for: COLEQ1 - COLEMAN FORKLIFT CORP. 11802

Type option, press Enter - or - position by name, city or zip code
l=Select 2=Change 4=Delete

 

Opt Name City/State Zip Code Open Close
— MINHARO WHOLESALE BURLINGHTON WA 98233 8:30 17:30
_ MINHARO WHOLESALE ANACORTES WA 98221 7:30 18:00

F3=Exit FS=Refresh F6=Add new address F12=Previous Roll

 

O To select an address as the Ship To location, select it with 1=Select.
O To change an address in the list, select it with 2=Change.

O To delete a ship to address, select it with 4=Delete.

1 To add a new address, press F6=Add new address.


18 X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

### Add New Address

Ship To Locations for: FOUROi - FOURTH CORNER FORKLIFTS x11802

Type option, press Enter - or - position by name, city or zip code
isSelect 2=Change 4=Delete

Name. 2... -

Extended name .

Address... .

Extended address.

City/State. -

zip code... . - Open .
Salesman. ... Close .

Tax code. 2... Map Loc

Discount code... _ Metro . _
validate blanks . . ¥ (¥ for name, city and zip)

F4=Prompt address ¥F12=Return Add new address

F3=Exit F5=Refresh F6=Add new address F12=Previous Roll

 

O With the cursor in the Name field, press F4=Prompt address to select from a
list of system addresses (may be cash customer, vendor, etc).

Ship To Locations for: COLEO1 - COLEMAN FORKLIFT CORP. 11502

x01000
Edit codes.
Select, Division

Opt Name City/state Zip Code
MARTIN, BILL ARLINGTON, WA 98223
MASON, BILL RENTON, WA. 99203
MINHARO WHOLESALE ANACORTES WA 98221
MINHARO WHOLESALE BURLINGTON WA 98233

1 MINHARO WHOLESALE SEDRO WOOLEY WA

 

: B3sExit Roll

F3-Exit F5=Refresh F6=Add new address F12=Previous

 

Oi Select the customer with 1=Select. The customer’s information will be
retrieved to the Ship To box.


X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 19

 

 

Ship To Locations for: COLEQi - COLEMAN FORKLIFT CORP. 11802

Type option, press Enter - or - position by name, city or zip code
1=Select 2=Change 4=Delete

. MINHARO WHOLESALE
Extended name . . -
Address 858 Timberlake Way
Extended address. .
Sedro’ Wooley WA

Open

Close -

Map Loc
Discount code . . Metro .
Validate blanks . . ¥ {¥ for name, city and zip)

F4=Prompt address Fil2=Return Add new address

F3=Exit F5<Refresh F6=Add new address F12=Previous Roll

 

1 Press [Enter] to return to the Ship To Locations screen. Press F5=Refresh to
see the entire list of Ship To Locations.

To assign more “Ship To” addresses, press F6=Add. You can select from a list of

all system addresses or press F6=Add again to add a new address, which would be

the same as adding a new address in Address Maintenance (X4-2).


20 X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

Now the 3 Minharo warehouses are associated with Coleman Forklift
Corporation. This step can be illustrated with the following diagram:

MINH03
Sedro Wooley

 

 

 

 

 

Here’s what we have so far:
« Coleman Forklift Corporation owns F001-F006.
- The 3 Minharo warehouses are “Ship To” addresses for Coleman Forklift.

The last step is to assign F001-F002 to the Minharo warehouses. This can be done

from Inquire/Update Service Units, which will be illustrated in this section, or by (
using another utility, Assign Units to Ship To IDs (X10.3-1 8). To use the utility,

see CHAPTER X10.3-18. .

Assigning Units to a “Ship To” Address

For this step, we'll start on the View/Update screen in Inquire/Update Service
Units (X10-1). One of the Coleman Forklift units will be displayed on the detail
screen, in this case, F001:


X10 » SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 21

 

 

  
  

 

  

 

A&R SALES & RENTALS Inquire/Update Service Units XA100-102
Division: A View/Update Current Equipment
Address # . + COLE02 or Name ..... COLEMAN FORKLIFT CORP.
License # .
Serial¥ FOO? 2300 IOWA ST
Unit # . c unit #
Series: BELLINGHAM WA 98226
- AMAZON Phone 360 714 8578
2000
Year . teeeee 97 Warranty code .. N
Description .... FORKLIFT Exp. date .. 100100
Purchase date .. 10197 Engine # .......
Hourmeter .... 100 Key code .......
Reminder date .. 91000
A/c. ~N Job code

 

 

 

Cmdi-End Cmd3-Go back Cmd5-Service History Cmd6-Recommended Maint
Cmd7-Shipto Location Info Cmd8-Next Cmdl0-Unit Service Info cmd19-Delete

 

You can press Cmd8-Next to cycle through the 6 units belonging to Coleman :
Forklift Corp. When you get to the one you want, press either F7-Shipto Location

Info or Cmdi0-Unit Service Info. Either command key will cause the following

window to pop up so that a “Ship To” address can be selected.

 

Select Ship To Window
A Select Ship To VSYXSRR
Sold To COLEMAN FORKLIFT CORP. Model 2000 Make AMAZON
2300 IOWA ST. Serial# Fo002
BELLINGHAM WA 98226 c unité :
1=Select
Opt Ship To Name Address City, state
MINHARO WHOLESALE BURLINGTON WA
MINHARO WHOLESALE ANACORTES WA
MINHARO WHOLESALE SEDRO WOOLEY WA

F3sExit F12=Previous

 

Select the appropriate “Ship To” location, and press [Enter] to proceed to the next
screen, which will be either Ship To Location Info or Display Unit Service Info.


X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT
Both of these screens will be illustrated to help you understand the type of C
information they record.

After each of the 6 forklifts have been associated with a “Ship To,” our table
looks like this:

 

 

 

 

 

 

 

 

 

 

 

Coleman Forklift Corporation has a contract with A&R Sales & Rentals for
scheduled maintenance and breakdown repairs. Purchase orders are issued for
each warehouse to cover the units located there. Purchase orders are entered on

the Select Ship To Location screen, which is reached from the Inquire/Updates (
detail screen by Cmd7-Shipto Location Info.

On the following page, you’ll see the Ship To Location screen.


X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 23

Ship To Location Info Screen

 

A&R SALES & RENTALS Ship to Location Info VSYODFR
Sold To COLEO1 Ship To MINHOL
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 YOWA ST
BELLINGHAM WA 98226 BURLINGTON WA 98233
AA ESTRUASTSS ESE ORT ASE SUSE EDEN CURATED ELL cnt ANE ELEAEISatERHAEtaE ST etaneAnanesE
ERS:..Open: 8:00 Close: 17:30 Map Location 28 Metro A
Contact: #1 RAE BARNES #2
Phone #: #1 360 650 - 5489 #2 -
Fax #: #1 360 738 - 7885 #2 -
SM: ¥ CPPM: ¥
BKD P/O #: 10100 Amount: 500.00
Ending Date: 12/31/97 Remaining Balance: 122.94
SM P/O 4: Po 100800 Amount: 3000.00
Ending Date: 7/31/97 Remaining Balance: 3000.00

Note: Renews annually ~ contact in June

F2<Units F3=Exit F6sEdit F9=Note F10=Contacts F11=P/0's F12=Previous

 

Note that the information on this screen does not pertain to an individual unit: it is
for the “Ship To” address although some information is updated from the Unit
Service Info screen, such as SM (Scheduled Maintenance) and CFPM (Contract
for Preventive Maintenance), which indicates that one or more units at this
location are under a service agreement. The purchase order remaining balances
are updated by Point of Sale. The information on the first line under the addresses,
opening & closing hours, map location, and metro, pertain to the “Ship To”
location and are entered via F6-Edit,

Look at the command keys at the bottom of the screen to get an idea of what you
can do here. The most important one is F11-P/0’s,


24 X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

Once you have entered P.O. information for the 6 forklifts, the table looks like C
this:

 

 

 

 

 

 

 
 

 

   
 
  
 
 
 
 
 
 

Breakdown (KE) P. 0. # & ‘Amt.
SM (Scheduled Maint) P.O. # & Amt.

 

Breakdown (BKD) P.O. # & Amt.
SM (Scheduled Maint) P.O. # & Amt.

 

Breakdown (BKD) P.O. # & Amt.
SM (Scheduled Maint) P.O. # & Amt.

X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 25

Unit Service Info Screen

 

    
  
   
 
 
 
 
 
 
 
 
 
 
 
 
 

 

ae Display Unit Service Info VSOLDFR
Sold To  COLEOL Ship To MINHO1
COLEMAN FORKLIFT CORP. MINHARO WHOLESALE BURLINGTON
2300 IOWA sv
BELLINGHAM WA 98226 BURLINGTON WA 98233
Make Model Yr Serial # Hourmeter Div Group Option
AMAZON 2000 97 Foo2 10.0 A 2
Inst Date 90 Day 1 Year 3 Years 5 Years CFPM End
1/01/97 4/01/97 1/01/98 12/31/97
SM Begin . : 1/01/97 SMend. .: 12/31/97 SM... sy .
SM Type. .: Fem SM Freq . : 30 SM Due Typ
SM Rate . . ; 55.00 Cons Rate : 36.00 Labor Hour 1.5
SM Due ..: 4/01/97 SM Prey .: 1/01/97
SM Due Hr . : -0 SM Prev Hr : +0 -
Note :

F3-Exit| F6=Edit F9=-Note Fi2=Previous F15-=Parts F16=Costs

 

This screen applies to the unit displayed under the address fields, in this case,
F001. This is where the Tecord-keeping is done concerning maintenance dates,
parts installed, and repair costs.

The most recent work date from a SM work order is stored as “SM Previous” on
the Unit Service Information screen. “SM Due” is calculated by adding
“Frequency” to the most recent work date.


26 X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

After maintenance schedules have been entered, the table is nearly complete. All
that remains is for the system to track parts and costs, which are recorded on the
Unit Service Information screen (or through one of its function keys).

 

 

 

 

 

 
  

  

ILEMAN FORKLIFT COR
Breakdown (BKD) P.O. # & Amt.
SM (Scheduled Maint) P.O. # & Amt.

  

FOO1
Schedule &
Records
F002
Schedule &
Records
F003
Schedule &
Records
F004
Schedule &
Records
F005

Sedro Wooley | Schedule &
Records
F006
Schedule &

Records

        
    
     
 

   

Breakdown (BKD) P.O. # & Amt.
SM (Scheduled Maint) P.O. # & Amt. |

 
       
    
      
  
  
 

   

Breakdown (BKD) P.O. #& Amt.
SM (Scheduled Maint) P.O. # & Amt. |

   
 
 

 

 
 

 

 

 

 

 

—— —— —

 

Scheduled Maintenance Due Report

After the initial setup work has been done, the service manager will run the
Scheduled Maintenance Due Report to see which units need to be serviced in the
next month. From this report, a plan can be developed whereby all units in the
same geographical area can be scheduled and the service manager can determine
how many technician hours will be required.

Point of Sale Work Orders

At Point of Sale, a work order is opened to the “Sold To” address, in this case,
Coleman Forklift Corporation. Immediately after the Entrance screen, the Select
Ship To Location screen is displayed.


X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 27

Select Ship To Location Screen

 

Ship To Locations for; COLE01 - COLEMAN FORKLIFT CoRP. 411802

Type option, press Enter - or - position by name, city or zip code
1=Select 2=Change 4=Delete

 

Opt Name City/State Zip Code Open Close

1 MINHARO WHOLESALE BURLINGTON WA 98233 8:00 17:30

— MINHARO WHOLESALE ANACORTES WA 98221 7:30 18:00

~ MINHARO WHOLESALE SEDRO WOOLEY WA 98214 7:00 19:00
Bottom

F3-Exit F5-Refresh F6=add new address F12=Previous Roll

 

 

Select a Ship To location with 1=Select and press [Enter]. The Sold To screen
is displayed.
O Press [F16] to select a unit.

Select Vehicle Screen

 

A Select Vehicie LRYISR

Address # COLE] COLEMAN FORKLIPT CORP.

 

Serial # Make Model Yx Description
1=Select
Opt Serial # Make Model. Yr Description
1 -F0001 AMAZON 2000 97
~  Fo002 AMAZON 2000 97
~  F0003 AMAZON 2000 97
~ ¥Fo0004 AMAZON 2000 97
~  F0005 AMAZON 2000 97
— ¥F0006 AMAZON 2000 97

F3sExit  P12=Previous

 

CO Select a unit with 1=Select and press [Enter]. Press F12=Previous.


28 X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

 

Sold To Screen

### A&R Sales & Rentals Invotcing-Sold To 5100-105

 

WORK ORDER # SP00229 CHARGE OPEN 11/16/00 Credit Card
Sold to: COLE01 Freon#: Ship to:
COLEMAN FORKLIFT CORP. MINKARO WHOLESALE

2300 IOWA sT.

BELLINGHAM WA 98226 BURLINGTON WA. 98233
Credit not established
¢ Unit: TK Warr Work Date 111600
Ship By Sold By HAL P.O.# 87-09325 Add Date 11/16/00
Sales Code PS Transfer Quantity Break Pricing N Print Date
Tax Number COL334-98657*S GST Method 3° Prans Date
Periodic Type = Periodic Frequency Rental Start Date Group 0

Make Model Year Serial Number Hourmeter Warranty SM
AMAZON 2000 97 FO001 1562. 4 00 Y
Balance Current 31-60 90 +
00 00 -00 . 00
Internal Address #: JOBJOE
Credit Limit Peak Bal Beg Date Or Unit #:
0900000 00 11/14/00 Warranty Address #: BELLO1

 

On this screen, the following fields are important to Fleet Management:

P.O.# Purchase order number from the Ship To Location
Info screen in Inquire/Update Units (X10-1). To
find this number, press [F18] to go to
Inquire/Update Units. At the Recommended
Maintenance screen, press F4-View/Update. At
the View/Update screen, press F7-Shipto
Location Info, where BKD & SM POs are
displayed. To see all POs, press F11-P/Os.

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

Uf the unit has a SM Due Type of “D,” the SM
Previous and SM Due Dates are updated.


X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 29

 

 

If the unit has a SM Due Type of “H,” the SM
Previous Hour, and SM Due Hour are updated.

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
for any unit that has been set up in Fleet Management. The warranty period for a
part is set up in Maintain Parts Warranty (X10.3-13). A pop-up window allows
you to change the billing to Internal (1) or Warranty (W). The default is blank,
which means the customer will be billed.

 

 

### A&R Sales & Rentals Work Order 5100-106

WORK ORDER # sP00230 For COLEO1 CHARGE OPEN 11/16/00
TaxDP Li t Price
Part Under Warranty
Part # Days Under Warranty

MAS 010146a94 180
Unit Install Date Warranty Exp. Date
8/24/00 2/20/01

Specify who will pay for the part W (blank/I/W)

 

Spec ord 00
PARTS SH

Tax DI/W Pty Line sc ven Qty Part number © Price Base
7 0010 Ps Mas 1 o10146a94 4
Standard line code No demand

 

After a part line is changed to Warranty, subsequent lines default to "W," which is
the same way Point of Sale works without Fleet Management.

 

NOTE
From the Entrance, Sold To, and detail screens at Point of Sale Invoicing, you can
press [Cmd18] to go to Recommended Maintenance then [Cmd7} to go to the
Ship To Location Info screen.


30 X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

SETUP

Service Info Maintenance—Link “Sold To” with “Ship To’s”

O Link "Sold To" customers with one or more "Ship To" names in Service Info
Maintenance (X10.3-16). See CHAPTER X10.3-16, MAINTAIN SHIP TO
LOCATION.

Ship To Location Info—Purchase Orders (by “Ship To”)

01 Optional. Enter purchase order information. See Purchase Orders in SHIP TO
LOCATION INFO SCREEN, page 17. Purchase orders are entered for the
“Ship To” address.

Option Table

O Optional. Set up a list of options in Maintain Service Options (X10.3-12). See
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


X10 « SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT 31

 

Contacts
O Optional. Assign contacts. This step can be done later.

This concludes the overview of Flect Management. What follows are step-by-step
instructions for using the Ship To Location Info and Unit Service Info screens.
Separate chapters describe the reports (X10.2-5 - X10.2-13) and utilities
(Chapters X10.3-12 - X10.3-20).

 

 

 

### Warning!

   

The code combines both S/36 and AS/400 conventions, which handle decimal
places differently. On $/36 screens, decimal places are assumed: they are not
entered on the screen. On AS/400 screens, decimals are entered directly into
fields. If you enter 3600 on an AS/400 screen, the system records 3600.00.

When you deal with numbers with decimal places, look for the screen name in the
upper right comer. 8/36 screens are numbered according to the menu map and
include the option number, such as X51000-106. AS/400 screen names are 7-
character combinations of letters and numbers, such as VSMAEIR, which don't
mean much to most of us.

 

 

In addition, $/36 screens refer to command keys, such as Cmd1-End job, while
AS/400 screens refer to function keys, such as F3=Exit. On all AS/400 screens,
press F3=Exit to end the job and return to a menu. If you just want to go back one
screen, press F12=Previous.


32 X10 ¢ SERVICE MANAGEMENT MENU FOR FLEET MANAGEMENT RELEASE 10.1

Notes:


---