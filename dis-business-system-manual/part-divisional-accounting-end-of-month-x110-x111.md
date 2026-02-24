---
title: "PART: DIVISIONAL ACCOUNTING - END OF MONTH (X1.10, X1.11)"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about PART: DIVISIONAL ACCOUNTING - END OF MONTH (X1.10, X1.11)."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on PART: DIVISIONAL ACCOUNTING - END OF MONTH (X1.10, X1.11)."
---

---

## Scanned Document - OCR Extracted Text

*This document was extracted using OCR from a scanned PDF.*

## CHAPTER X1.10-1

DIVISIONAL ACCOUNTING END OF MONTH

### Introduction

Divisional Accounting End of Month allows you to:

close the oldest open General Ledger month for one division.
print the following reports:

- Depreciation Register.

- General Ledger Register for the month you choose to close.

- Aged Payables Report and Recap as of the end of the month you
close.

- Aged Receivables Report and Recap as of the end of the month you
close.

- Inventory List current as of the end of the month you close.

- Journal printout (if Journals OPT switch is on).

- Trial Balance (if Journals OPT switch is on).

delete transactions from file for month to be closed.

update General Ledger history balances.

calculate depreciation for your fixed assets if you have specified a
method in Units Maintenance.

### Important

Before running this job, make sure that no other jobs are running.


[2] X1.10-1 DIVISIONAL ACCOUNTING END OF MONTH

### Preparation

0) Make sure the accounting month is in balance before closing it. Before
running End of Month, request a financial statement. Verify that assets
equal liabilities and net worth.

QO Run Subledger Balance Report (X14-5) to make sure that subledgers
are balanced to the General Ledger.

O Make sure that Monthly Billing has been run for the month you're
closing.

CO If you use the Sales Tax Report (X16-3), run it before you close the
month. Detail sales tax transactions, which are used to create the Sales
Tax Report, are lost when the month is closed.

O Back up your data files BEFORE running End of Month. Instructions
for doing BACKUP are in the Security and Configuration Chapter,
X6-1.

No other job(s) may run while the End of Month job is running. Check the
User Board to be sure no other job(s) are running.
LL

## X1.10-1 DIVISIONAL ACCOUNTING END OF MONTH

### How To Run

From Menu X1-10 select option 1 to run Divisional Accounting End of
Month.

#10901 TESTING FILES X1A00-300

End of Month Procedure

Executing this procedure will
close the month of January
for the division shown above!

Do not continue unless you have been
authorized to run this procedure.

It is recommended that you

do a "back-up" before running
this End of Month Procedure.

cmd1-Cancel job Cmd2-Continue

 

You are required to select [Cmd2] to continue. This safeguards you from
accidently proceeding if you did not intend to.

The procedure is placed on the job queue. Press [Enter] to return to a
menu.


[+] X1.10-1 DIVISIONAL ACCOUNTING END OF MONTH

Notes:

RELEASE 2.2 LU

## CHAPTER X1.10-2

COMBINED END OF MONTH FOR ACCOUNTING, POS, &

### Introduction

Combined End of Month combines:

ACCOUNTING END OF MONTH to:
= close the oldest open General Ledger month.
= print the following reports:
- Depreciation Register.
- General Ledger Register for the month you choose to close.
- Aged Payables Report and Recap as of the end of the month you
close.
- Aged Receivables Report and Recap as of the end of the month you
close.
_ Inventory List current as of the end of the month you close.
- Journal printout (if Journals OPT switch is on).
_ Trial Balance (if Journals OPT switch is on).
= delete transactions from file for month to be closed.

   
 
  

  
  
   

Note:

Run the Sales Tax Report before you run Accounting End of Month.

    

s update General Ledger history balances.
» calculate depreciation for your fixed assets if you have specified a
method in Units Maintenance.

POS END OF MONTH (based on closed POS documents) to:
= remove ali documents that are closed and posted from your document
file. All voided quotes will also be deleted.


[2] X1.10-2 COMBINED END oF MONTH FoR ACCOUNTING, Pos, a PARTS

 

™ reorganize all Point of Sale files and tables,

" close out month-to-date utilization into year-to-date accumulator for
Tentals. This is done by division.

" can run POS End of Month (X54) more than once a month. If you find
the response time at Point of sale slowed, it may be due to the large size

closed and posted documents and Speed up response time at point of
Sale. After End of Month is run, only the open documents remain.

PARTS END OF MONTH to:

™ rebuild and compress the Parts and master files which Organizes part
Tecords into a more efficient structure,

 
   
     
 

### Important

   

Any combination of End of Month jobs may be run from this menu

option. You can run the same job (e.g. Accounting End of Month) for
all divisions, one division, or a Combination of several divisions. THE
DIVISIONS ARE PROCESSED IN THE SAME ORDER AS THEY
APPEAR ON THE MASTER SECURITY SCREEN IN SECURITY
MAINTENANCE (X6-6). The order can be changed at any time. See

## CHAPTER X6-6

## , SECURITY MAINTENANCE

 
      
     

 

RELEASE 2.2 LL


X4.10-2 COMBINED END oF MONTH FOR ACCOUNTING: pos, & PARTS (2 \

REMEMBER: Accounting End of Month closes General Ledger months
and should only pe done once per division for that month. Tf you have any
doubt as to what month is open, check Security Maintenance (%6-6) for
the oldest open General Ledger month. Be sure that Monthly Billing has
been run for the month you are closing. If it hasn't, you won't be allowed
to close the month.

Jf you use the Sales Tax Report (X16-3); run it before you close the
month. Detail sales tax transactions, which are used to create the Sales Tax
Report, are Jost when the month is closed. Also. since POS End of Month
removes the detail of closed, posted documents, it iS important to run the
Salesperson and Labor Analysis Reports (56-3 & 4).

Jt is also important to packup your data files BEFORE running End of
Month. Instructions for doing BACKUP are in the Security and
Configuration Chapter,

No other jobs may run while the End of Month job is running- Check the
User Board to be sure no other jobs are running.

Accounting End of Month has safe-guards in it to protect your system's
data from. joss OF corruption if it is interrupted by a power outage OF some
other accident. Hf Accounting End of Month is interrupted, contact DIS for
help on restoring your system S data.


Tun Combine End

OW:

 
 
  

of Month, Follow

X2A200-993

“Month for all
1.

Before Turning this Proce,

dure ;
x files,

Backup You
Make sure

RELEASE 9 > CO


xi


0-2 COMBINED END OF MONTH FOR ACCOUNTING, pos, & PARTS

After you have completed all of the steps. press ENTER. The following

screen 1S displayed:

  
 
  
 

    

 
 
 

  

ABC COMPANY COMBINED END-OF -MONTHS x1A20~ 102

  
 

s POS? N

 
 

ALL divisions accounting? WN ALL division

  
  

ALL div? sions parts?

 
 

s by entering > y for that division pelow-

 
 

ox, select ynaividual division

  
  

pivision accounting? POs? pivision accounting? POs?

EB N
R N N

 
   
    

 

 

  
  

 

 

 
 

enter tame if you want delayed execution: pHMMSS

    

cmd. 4-End yop cmaa-continve

   

NOTE:
The time entered must be after the current time put before midnight.

Type in:

y (Yes) for All Accounting Divisions

N (No) for only the division you signed onto
(and any others you designate below)

y for All Parts Divisions
N for no parts End of Month
(This job is not divisional.


X1.10-2 COMBINED END oF MONTH FOR ACCouNTING, POs, & PARTS

Run it Once for alj divisions )
Y for All POS Divisions
for Only the division You signed onto

If you Say Yes to POS End of Month, YOu Will neeg to enter g
Purge date (see Chapter X5-4, Pos End of Month for More
i ion

the system iS not in use, However, the time €ntered must be after the
00),

al screen

If you Choose the time-delayeq Option, the following information
Will be Shown:

   

 

 


X1.10-2 COMBINED END OF MONTH FOR ACCOUNTING, POS, & PARTS

It warns you that there can’t be any active Create Source Documents or
Point of Sale batches when the procedure begins. This is only a warning
and it’s up to you to make sure these jobs are not active.

Press [Cmd2] to continue. This safeguards you from accidently proceeding
if you didn’t intend to. If you are performing POS End of Month, the
following screen appears.

   
 

  

 
 

NW EQUIPMENT SALES Combined End of Months ¥1A20-101

     

ALL div Point Of gale End of Month for Division A x54900
ALL div Amend purge dates by document type
or, sel dype/Description Purge date ‘Type/Description Purge date

  
       
  
   
 

A RECD ON ACCOUNT 9/01/98
C COUNTER TICKET 9/01/98
Division J TEST QUOTE 9/01/98
A L RENTAL/ LEASING 9/01/98
B Q REQUISITION 9/01/98
D R REPAIR ORDER 9/01/98
E § UNIT SALE 9/01/98
M U UNIT RENTAL 9/01/98

Bottom

  
  
   

Enter=Validate F3<Exit F10=Proceed Roll
cmdl-End job emd2-Continue

This screen allows you to set the purge date for each type of Purchase
Order Document. Type in dates as numbers only (without slashes) and
press [Enter]. The dates will now display with slashes. Confirm that they
are correct and press (F10].

RESULT: The procedure is placed on the job queue. Press [Enter] to


X1.10-2 COMBINED END OF MONTH FOR ACCOUNTING, POS, & PARTS

return toa menu,

### Important

You should NOT run an’

Y other jobs until this procedure is off the User
Board.

 
(

## CHAPTER X1.11-1

JOURNAL ID MAINTENANCE

### Introduction

Use Journal ID Maintenance to add, change, or delete journal [Ds.

### How To Run

From the Journal Menu (X1-11), select option 1, Journal ID Maintenance.
Following the Accounting security gate, a Journal ID prompt appears:

A & R SALES & LEASING CO JOURNAL ID MAINTENANCE X1B101-01
All Divisions

Enter Journal ID: _

Cmdl-End job

 

O Type a 1-character Journal ID, and press [Enter]. A description line
appears, as illustrated on the following page.

## X1.11-1 JOURNAL ID MAINTENANCE

 

Note:
Journal Ds can be any character, letter, or number except: ?, *, /, =, >,
+, -, comma, blank, or apostrophe (’).

A & R SALES & LEASING CO JOURNAL ID MAINTENANCE X1B101-02
All Divisions

Journal ID: E

Description 2

To delete enter ‘Y': _

Cma3-Go Back

 

RELEASE 2.1 LO


 

 

C) If it is anew code, type the description (up to 40 characters). To change
an existing code, type over the current description. To record your

changes, press [Enter].

0 To delete a code, type Y at the prompt "To delete enter "Y'."

0 To go back to the Journal ID prompt, press [Cmd3].

O To end the job, press [Cmd1] at the Journal ID prompt. The following

message is displayed: "Enter "Y' to print the ID report: N" If you want

to print the Journal ID Report, change the default, "N," to Y.

 

 

 

 

An example of a Journal ID Table follows:

A & R EQUIPMENT SALES

Journal ID Table Date ; 4/21/92
All Divisions

Page : 2

Time ; 14:59:16 X1B10-2A
Description:

B BILLING JOURNAL
EQUIPMENT JOURNAL
GENERAL JOURNAL


3 GTM'S JOURNAL
L LAURA'S JOURNAL

 


Notes:

RELEASE 2.1 CC

## CHAPTER X1.1

## 1-2

AUTOMATIC POSTING ID MAINTENANCE

### Introduction

automatically. This has the effect of posting automatic transactions to the
Specified journal.

### How To Run

  
 
   

 
 
  
  

   

A&R SALES & LEASING co AUTOMATIC POSTING Ip MAINTENANCE X1B201-02
All divisions

  

  
  
  
 


fons 2...

 

  

mdi-End Job

## X1.11-2 AUTOMATIC POSTING ID MAINTENANCE

 

C1 Type the Journal ID you want to use for each of the automatic

transactions listed on the screen. To record your changes, press [Enter].

C1 To end the job without recording your changes, press [Cmd1}.

(1 The following message is displayed: “Enter "Y’ to print the Automatic
Assignments Report : N." If you want to print the report, change the

default, "N," to Y.

An example of the Automatic Assignments Report follows:

   

    

 
 
  
  
  
  
 
  

automatic Posting Assignments table pate : 4/21/92 Page =
mime : 15:00:00 1320-24

a---x ID Journal 1D Description <-----7777 777 Xx

L LAURA'S JOURNAL

L LAURA'S JOURNAL

G GENERAL JOURNAL

= EQUIPMENT JOURNAL


 
  
 
   
  
  
  
   

A & R EQUIPMENT SALES
All Divisions

Automatic posting option ---79 TT


~ posting Checks Transactions ---

xia-1 Accounting End Of Month (Units Depreciation)

yii-8 Monthly Billing ---++" .
xi2-8 Print Payables checks
yic-1 Accounting End of Year -

  
  
 
 

  
   

 
  

gUST A JOURNAL
gUST A JOURNAL

    
   
  

 

RELEASE 2.1 L

## CHAPTER X1.11-3

JOURNAL INQUIRY

### Introduction

Use Journal Inquiry to look at transactions grouped by Journal ID. You
can roll through transactions or skip directly to any ID or document
number.

### How To Run

From the Journals Menu (X1-11), select option 3, Journal Inquiry.
Following the Accounting security gate, a list of transactions appears, as
illustrated below:

A & R SALES & LEASING CO JOURNAL X1B301-01
Division A

ID Date Mth Document D/C Account E Description Addr # Unit#

5/01/92 CASK
5/01/92 CASH
5/01/92 CK#1208
5/01/92 CK#1208
5/01/92 CK#7800
5/01/92 CK#7800
5/01/92 CK#921,
5/01/92 CK#921
5/30/92

6/20/92

5/30/92

5/01/92 PAY 051586
5/01/92 PAY 051586
5/01/92 PAY 0515
5/01/82 PAY 0515
5/01/92 PAY 0515-2

A1100 . ROA ADAMO1

A1000 . ROA ADAMO1

Al110 . ROA GRADO1 BH1000
A1000 . ROA GRADO1 BH1000
A1100 . ROA KLUCOL

A1000 . ROA KLUCOL

A1100 . ROA SEREO1

A1000 - ROA SEREO1

A1020


A1020 . BANK TRANSF

A1320 : §0010501

A2400 18s. $0010501 CASEO1

A6840 99. OFF. SUPPLY

A2400 99. OFF. SUPPLY WESTO1

A6S90 66. SHOP SUPPLY

vouanvavvsnoaeasa

----> Start Next Page With: Id _ Document
Cmd1-End job, Cmd6-More Fields, Roll-Page

## X1.11-3 JOURNAL INQUIRY

 

O Roll to see the next page or go directly to a particular ID or Document
by using the line above the command keys, "Start Next Page With: Id

Document."

O To see more fields, press [Cmd6]. Other fields are displayed as

illustrated on the screen that follows.

A & R SALES & LEASING CO
Division A

Description Addr # Unit# Name

ROA ADAMO1 WILLIAM ADAMS

ROA ADAMO1 WILLIAM ADAMS

ROA GRADO1 BH1000 LEROY GRADY

ROA GRADO1 BH1000 LEROY GRADY

ROA KLUCO1 KLUCKITOOT COUNTY

ROA KLUCOL KLUCKITOOT COUNTY

ROA SEREO1 SERENE VALLEY FARMS, INC
ROA SEREOL SERENE VALLEY FARMS, INC


BANK TRANSF

$0010501

s0010501 CASE0O1 CASE IH

OFF. SUPPLY

OFF. SUPPLY WESTO1 WESTERN SUPPLY CO
SHOP SUPPLY

Start Next Page With: Id Document
Cmdi-End job, Cmd6-More Fields, Roll-Page

X1B301-02

Due Date Discount

5/30/92
5/30/92

5/02/92

5/02/92

 
C.

## CHAPTER X1.11-4

PRINT JOURNALS

### Introduction

Use this job to print a report of all journals or select up to 10 journals. The
report can be for one General Ledger month, for a date range or for a
reporting sequence by either date or document number. The security gate
allows you to specify one division or request the same report for all
divisions.

### How To Run

From the Journals Menu (X1-11), select option 4, Print Journals. The
following security gate appears:

Enter Division Code
Print all divisions (¥/N) .. .

Enter Security Code

 

CL] Type the code of the division you want. To print all divisions, change
the default, "N," to Y. Type your security code and press [Enter]. The
selection screen appears.

## X1.11-4 PRINT JOURNALS C

A&R SALES & LEASING CO PRINT JOURNALS X1B401-01
Division A

G/L Month 1 (01 to 12)
or
From Posted Date : (MMDDYY)

To Posted Date : {MMDDYY }

Reporting Sequence : (*D’ate or Document)
‘N’umber Sequence)

Cmdl-End Job

 

0 To print all journals type ALL and field exit to select G/L month or
date range. To restrict the report to one or more journals, field exit to
the 2nd line where you can specify up to 10 Journal IDs.

QO) You can request either a G/L month, a date range or a sequence by date
or document number for the report. Select a G/L month by typing 01
for January, 02 for February, etc. or select a date range, such as 010198
to 060198. To sort reports by date or document number sequence, type
‘D’ for date or ‘N’ for document number.

D To cancel your request, press [Cmd1].

0 To process your request, press [Enter]. The following message appears:
"This procedure has been evoked. You may continue with other work
while this job is running. Press ENTER to return to a menu."

RELEASE 2.2 Se


X1.11-4 PRINT JOURNALS [=]

This is an example of the detail portion of a Print Journals Report:

A & R EQUIPMENT SALES CATHERINE'S JOURNAL Date 4/21/98 Page 1
All Divisions Selection : ID: C G/L Month: 11 Time 15.02.48 x1B40-30

Edit code overrides: 1 - ignore edit code. 2 - ignore edit code and adjust 13th month

Id Date Mth Document# Account# Edit Amount Description addr# Name- -' Due Date Discount Stock
11-04-97 Nov 13330 L102 2625.00 BTC LEASING C 11-04-97 Nov 13330 D L664 2625.00
11-04-97 Nov 13336 L102 2100.00 PSB
11-04-97 Nov 13336 L280A 558.96
11-04-97 Nov 13336 L680 1541.04
11-04-97 Nov 13337 L102 3000.00
11-04-97 Nov 13337 L238 1861.81
11-04-97 Nov 13337 L680 3336.19
11-04-97 Nov 13338 L102 500.00 DON BRIM
11-04-97 Nov 13338 1261 500.00 ADVANCE B00236 BILL BRONSON 11-01-97
11-04-97 Nov 13339 L102 425.00 TONY CURTIS
11-04-97 Nov 13339 L260A, 340.15
11-04-97 Nov 13339 L680 84.85
11-04-97 Nov 13340 L102 100.00 DAN BRIM
11-04-97 Nov 13340 L682 100.00 DAN BRIM
21-04-97 Nov 13342 L192 100.00 HENRY SUITER
21-04-97 Nov 13341 L682 100.00 HENRY SUITER
11-12-97 Nov 16901 Lioz 141.22 vorp
11-12-97 Nov 16901 Lil 141.22 CREDIT-A/P $02544 SMITH EQUIPMENT
11-18-97 Nov 13296 L102 04
11-18-97 Nov 13296 L220 +04 FL6687 FORD MOTOR CREDIT COMPANY = 11-18-97 PES927
11-18-97 Nov 13361 L102 DON BRIM
11-18-97 Nov 13361 L261 ADVANCE. 200236 BILL BRONSON 11-15-97
11-18-97 Nov 16777 L102
11-18-97 Nov 16777 L699
11-19-97

AV9VA9nFAVVAMONVGBAVADE ANDO

 

This is the recap of the Print Journals Report illustrated above.

## X1.11-4 PRINT JOURNALS

A & R EQUIPMENT SALES CATHERINE’S JOURNAL Date 4/21/98 Page 1
All Divisions Selection: ID: ¢ G/L Month: 11 Time 15.02.54 x1Bd0-4a
CASH IN BANK - PSB L102 Debit 6419.90 Credit 65864.89
ACCOUNTS RECEIVABLE Linn Debit Credit 141.22
USED TRACTORS & EQUIPMENTL125 Debit 109.20 Credit
NOTES PAYABLE - FORD L220 Debit 64393.01 Credit 58382.36
NOTES PAYABLE-MF 1221 Debit 219.80 Credit
NOTES PAYABLE - PSB L238 Debit =: 1861.81 Credit
EMPLOYEE SAVINGS ACCOUNTSL239 Debit 2889.00 Credit
ACCRUED FICA 1263 Debit 1473.74 Credic
ACCRUED WITHHOLDING-FED. L264 Debit 926.17 Credit
NOTE - PSB REAL ESTATE 280A Debit = 215.49 Credit
FORD TRACTORS & EQUIPMENTL420 Debit 9112.68 Credit 9112.68
EMPLOYEE MEDICAL L657 Debit 109.55 Credit
BUILDING LEASE LeéS Debit 2625.00 Credit
INTEREST - FLOORING L680 Debit 5437.36 credit
TRAINING L682 Debit 300.00 Credit
TAXES - STATE EXCISE L683 Debit 36.00 Credit
‘TRAVEL & ENTERTAINMENT L665 Debit 300.00 Credit
CONTRIBUTIONS L689 Debit 700.00 Credit
MISCELLANEOUS 1699 Debit 01 Credit
Total 2133501,25 133501.15

 

RELEASE 2.2 LO

## CHAPTER X1.12-1

ACCOUNTING END OF YEAR

### Introduction

Accounting End of Year will close the books for the fiscal year. The
accounts on the Operating Statement will be debited or credited
automatically and the offsetting entry to Retained Earnings will be made.
Accounting End of Year is divisional and must be run for each division.

Do not close any months in the new year until you have run End of Year.
For example, if the year ends in December, do not close January. January's
Retained Earnings will not contain the profit or loss for the previous year.
Also the totals on the Operating Statement will contain the Year to Date
balances for last year.

### Checklist

If you have no questions on how Accounting End of Year is run, refer to
the checklist below to run the job. If you are unsure about the steps
involved read the rest of the chapter carefully.

0 All twelve months of the previous fiscal year must be closed.

O The first month of the new year should be open.

 

 

 

 

O Backup your files. Save this backup as End of Year 19--.

O Run a Financial Statement and file with subledger reports for the
12th month of the previous year.

QO From the End of Year menu, select option 1, Accounting End of Year.
A. Post the batch to the first day of the first month of the current

year.
B. Enter your Retained Earnings account number.


[2] X1.12-1 ACCOUNTING END OF YEAR cc

C. Select option 2 when screen X1700-001 displays informing you
that a batch already exists.

D. Check the batch. Correct any errors.

E. Post the batch.

O Run a Financial Statement on the first month of the current year to
check the results. File the statement with the year end reports.

RELEASE 2.1 Ne


X1.12-1 ACCOUNTING END OF YEAR [2]

### Preparation

WARNING!

Read this section very carefully before you
begin end of year.

 

Below are the steps that must be taken before running Accounting End of
Year:

O Make sure all the months of the current fiscal year are closed. You
can not run Accounting End of Year unless your oldest open month
equals the month your fiscal year starts in Security Maintenance
(X6-6). Do not change the month. The system changes the month when
the end of month job is run.

O Backup your files. This is very important. Make sure you label the
backup and that no one uses the diskettes for any other backup. Make
sure you keep these diskettes.

O Runa financial statement and store it with copies of the subledger
reports: Current Inventory Report, Aged Receivables, and Aged
Payables, both flooring and trade. Run a Parts Inventory Pad Summary
report. If the accountant needs copies of these subledgers for
adjustments, they will be readily available. The subledgers are
current reports. Compare the financial statement to the reports that
were run on the last day of month of the financial statement.

After all of the above have been done, you may proceed to Accounting
End of Year (X1.12-1).


[+] X1.12-1 ACCOUNTING END OF YEAR Cc

### Running Accounting End Of Year

After passing through the security gate at Accounting End of Year, the
following screen will display:

SECURITY GATE x0001-001
Accounting

Enter Division Code
Enter Security Code

Assign transaction date for posting (

Enter transaction date (mmddyy): 010198

Cmdl-End job Cmd3-Go back

 

Before closing the year, all twelve months of the previous fiscal year must
be closed. No months in the current fiscal year should be closed until you
close the year.

THE TRANSACTION DATE SHOULD BE THE FIRST DAY OF THE
CURRENT FISCAL YEAR.

In the above example, the year ended 12/31/97. The year is being closed in
January. The posting date is January 1, 1998.

RELEASE 2.1 CU

## X1.12-4 ACCOUNTING END OF YEAR

When the transaction date is typed, press Enter. The following screen
displays:

WEAVER'S EQUIPMENT ACCOUNTING END OF YEAR *1C10-101
Division: L

This procedure creates a posting batch to zero balances in your profit and@ loss
statement. The balance is posted to your retained earnings account.

Enter the general ledger account for retained earnings: L295

Press Cmdl to cancel job.

If you want to cancel the job, press [Cmd1].

 

To proceed, enter the number of your Retained Earnings account and press
Enter.

## X1.12-1 ACCOUNTING END OF YEAR

After typing the Retained Earnings account, press Enter. The following
confirmation screen is displayed:

WEAVER'S EQUIPMENT ACCOUNTING END OF YEAR x1C10-101
Division: L

This procedure creates a posting batch to zero balances in your profit and loss
statement. The balance is posted to your retained earnings account.

Enter the general ledger account for retained earnings: L295

Title of account: RETAINED EARNINGS
Type of account ; L
Please verify this account. If incorrect, enter another.

Press Cmdl to cancel job.

 

After confirming the Retained Earnings account, press Enter. The
following screen displays:

WEAVER'S EQUIPMENT ACCOUNTING END OF YEAR X1C10-102
Division: L

The posting batch is being created. When it is complete, the Post Source
Documents Check for Errors screen will be displayed. Complete this posting batch
as you would a regular posting batch.

 

The End of Year batch is being created through Create Source Documents
(X1-7). The debits and credits will be generated. The operating accounts

RELEASE 2.1 Lo


X1.12-1 ACCOUNTING END OF YEAR [7 |

will be zeroed out and the offset will be to the Retained Earnings account.
You will proceed through the security gate and verification gates that are
in Create Source Documents (X1- 7). When choosing the posting month,
choose the first month of the current fiscal year. For example, if the
current fiscal year began January 1, 1998, post the batch:

DATE: 010198

MONTH: 01

After passing through the security gate and verification screens, the
following screen displays:

### Create Source Documents X1700-001

A post source documents batch already exists for this workstation.

Enter one of the following options: 2

1. Return to the Accounting Menu.

2. Continue with the Check For Errors job for the existing batch.
3. Delete the existing batch and begin creating a new batch.

 

Select option 2, Continue with the Check for Errors job for the existing
Job. After selecting option 2, the Post Source Documents Check for Errors
screen will display. Choose the editing option. If you are unsure about the
editing options, refer to Create Source Documents (X1-7) for information.
After choosing the editing options, press Enter.


8 | X1.12-1 ACCOUNTING END OF YEAR

The Post Source Documents Check for Errors screen will display
containing the End of Year batch. See the example below:

WEAVER'S EQUIPMENT POST SOURCE DOCUMENTS 1/01/98 x1710~S01
Division L CHECK FOR ERRORS January

Current display: partial transactions Update line #
Line# Date Document# Account # E Amount Description Addr #
10 1-01-98 D L332 1D 150.00 YEAR END
20 1-01-98 Cc L432 1 105.00 YEAR END
1-01-98 D L600 1 600.00
Cc L295 1 645.00
of transactions

Press Cmdl to end job; Cmd2 partial transactions; Cmd3 full transactions; Cmdé
recap; Cmd5 scan for error; Cmd6 more fields; roll keys

 

Notice in the above example, the * after the "Line #" column. The
*indicates an automatic transaction. You will recall that the Retained
Earnings account number was selected before the batch was displayed.
The program looks at the balance in the operating account. It debits or
credits that balance to make the account balance for the End of the Year
zero. It then automatically debits or credits the Retained Earnings account
for the offsetting amount.

The first three lines of the batch, for example, are Operating Statement
accounts. All accounts that have a S = Sales, C = Cost of Sales, I=
Income, or E = Expense account type from General Ledger Maintenance,
(X14-2), will generate an automatic transaction at Accounting End of

RELEASE 2.1 LO


X1.12-1 ACCOUNTING END OF YEAR le |

Year. The debits and credits will display and print in account number
order by types, S,C,I, and E. This is the same order as the Financial
Statement.

The fourth line contains the offsetting entry to Retained Earnings, L295.

There will be no errors in the batch. The debits and credits will equal. You
may post the batch. However, review the batch carefully to make sure the
entries are what you want. Make any changes you choose. The batch will
have to be reedited if changes are made. If you need more information
refer to Create Source Documents (X1-7).

If no changes are to be made, press Cmd1 to end job. This advances you to
the next job step. The following screen will display:

WEAVER'S EQUIPMENT SHOP POST SOURCE DOCUMENTS 1/01/98 1710-503
Division L CHECK FOR ERRORS January

End of job option: 1
1. Return to processing -- do not end job
« End job with printed edit list

3. End job without printed edit list
4

- Create new edit list.

No errors have been detected. This batch may be posted.

 

Select option 2, End job with printed edit list. Press Enter. File the list
with the other end of year reports.


10 | X1.12-1 ACCOUNTING END OF YEAR

The following screen displays:

COMMAND
(c) DIS Corp.

Errors Have Been Detected

+ Post Source Documents

» Return To Editor Correction Menu (

Ready for option number or command

 

Run a January Financial Statement. The Retained Earnings account and
operating statement accounts will reflect the changes. If End of Year was
completed before closing or posting to the second month in the new year.
the Year to Date balance should equal the Current Month figures on the
January Statement.

?

RELEASE 2.1 LL


X1.12-1 ACCOUNTING END OF YEAR ["]

Retained Earnings will contain last year's profit or loss. For example, if the
year is from January 1, 1997 to December 31, 1997 and you close the year
in January of 1998, the Retained Earnings account will reflect the profit or
loss for 1997 and all previous years.

End of Year must be run for all divisions. Repeat the above steps as
necessary.


Notes:

## CHAPTER X1.12-10

SOLD UNITS FILE MAINTENANCE

### Introduction

Sold Units File Maintenance purges a selected unit or units sold before a
user-specified date. Units will be purged if they:

- do not have a flooring balance

- are not on a point of sale or periodic invoice

- are not linked in a washout tree without units which do not quality
to be purged

### How To Run

From the Accounting End of Year Menu (X1-C), select option 9, Sold
Units File Maintenance.

## X1.12-10 SOLD UNITS FILE MAINTENANCE

NW EQUIPMENT SALES SOLD UNITS FILE MAINTENANCE X1CA0-102
Select Units

Purge all units sold before this date: 50286 or
Purge this unit number:

Unit(s) specified will be purged provided they

- do not have a flooring balance

- are not on a point of sale or periodic invoice
- are not linked in a washout tree with other
units which do not qualify to be purged.

Enter-Continue Cmdi-End job

 

0 To purge a specific unit, enter the unit number. Otherwise, enter a date.
All units sold before that date will be purged from the system.

Press [Enter] when finished. The following screen appears.

RELEASE 2.1 LU


NW EQUIPMENT SALES SOLD UNITS FILE MAINTENANCE X1CA0-002

Continuation

A report has been printed listing all units which will be purged.

Please carefully review this list before processing.

Cmdl - Cancel job; do not purge units.
Cmd2 - Continue; purge units specified on report.

 

A sample Sold Units File Maintenance Report is displayed below.

NW EQUIPMENT SALES SOLD UNITS FILE MAINTENANCE DATE 5/02/96 PAGE 1
BELLINGHAM WA Division: A Purge Date: 5/02/86 TIME 11.29.25 X1CA08-01,
Sale Dt Addr! Serial Number Description

BH1000 © 5/01/86 GRADOL 266899F423 Unit will not be purged. *** washout tree
FES@68 2/01/86 GRADOL 80063 Unit will be purged.

fT0642 3/25/86 BOULOL 002468 Unit will be purged.

FTS492 1/03/86 TWOSO1 u700982 Unit will not be purged. *** Washout tree
PTS768 1/15/86 #00K01 0502617 Unit will not be purged. *** Flooring balance
FTS5809 5/01/86 BOULO1 637578 Unit will not be purged. *** Flooring balance
SNH281 1/05/86 TEXAOQ] NEW HOLLA 288364 Unit will be purged.

431LVS 5/01/86 TWOSO1 HONDA 1HGBAS432GA003947 Unit will be purged.

 

After reviewing the report, press [Cmd1] to cancel the job or [Cmd2] to
purge the units on the report.


Notes:

RELEASE 2.1 (O

## CHAPTER X1.12-2

ACCOUNTING END OF YEAR ADJUSTMENTS

### Introduction

Accounting End of Year Adjustments allows you to make adjustment
entries to a thirteenth month. You can then run a Thirteenth Month
Financial Statement with correct balances for current profit/loss and the
Operating Statement accounts on the Financial Statement for the previous
year after the year has been closed.

### Preparation

Before you run accounting end of year adjustments, do the following:
For example, the year closed December 31, 1986, adjustments are to be
made to 1986.

Make sure the 1985 is closed.

Make sure all adjustments have been made to 1985.

Close 1986.

Proceed with Accounting End of Year Adjustments (X1.12- 2).

oooo0

## X1.12-2 ACCOUNTING END OF YEAR ADJUSTMENT

 

### Checklist

If you have no questions about the running of the Accounting End of Year
Adjustments, follow the steps on the checklist below to perform
Accounting End of Year Adjustments. If you have questions, read all] the
documentation carefully before proceeding with this job:

D Close the 12th fiscal month of the previous year.
O Close the year (X1.12-1).
O Run a Financial Statement for the last month of the last fiscal year.

O From the End of Year menu, select option 2, Accounting End of Year (
Adjustments.

a. Supply your Retained Earnings account number.

b. For posting date and month, use the first day of the oldest open
month.

c. Make necessary adjustments and post them.

 

 

Run 13th month Financial Statement. Make sure the changes you want
are made correctly.

 

 

O Bring the subledger reports back into balance with the General Ledger.

RELEASE 2.1 LO


 

### How To Run

If you have any questions on the theory of Thirteenth Month Adjustments,
refer to the section titled What is The Thirteenth Month in Chapter X1-12,
End of Year.

Let's take an example of a possible end of year adjustment and follow it
through to see how to enter the adjustment and to see the effect of the
adjustment,

The Case of the Missing Bucket

Once upon a time there was a bucket attached to a certain backhoe. But
something happened to the bucket. It is nowhere to be found. This bucket
is going to be charged to the Sales Department (L600). The backhoe was
used as a demonstrator, and the Sales Department was responsible for the
backhoe and bucket. The bucket was missing at end of year inventory. The
accountant insists that the profit or loss for last year must show this
adjustment. You need to lower the cost in the Equipment Inventory
account (L120) by $450.00.

Retained Earnings Account

From the End of Year menu, select option 2, Accounting End of Year
Adjustments. After proceeding through the security gate, the following
Screen displays:


 

WEAVER'S EQUIPMENT ACCOUNTING END OF YEAR x1LC20-1023
Division: L ADJUSTMENTS

This procedure is used to enter a special posting batch for year end adjustments.

Enter the general ledger account for retained earnings: 1295

Press Cmdl to cancel job.

 

Enter the Retained Earnings account number. If you wish to cancel this
job, enter the Retained Earnings account number. Press Enter. On the next (
screen you will be given the opportunity to cancel the job with a Cmdl.

RELEASE 2.1 LO


 

Fill in the Retained Earnings account number and press Enter. The
following verification screen will display:

WEAVER'S EQUIPMENT ACCOUNTING END OF YEAR X1C20-101
Division: L ADJUSTMENTS

This procedure is used to enter a special posting batch for year end
adjustments.

Enter the general ledger account for retained earnings: L295

Title of account: RETAINED EARNINGS

Type of account : L
Please verify this account. If incorrect, enter another.

Press Cmdi to cancel job.

 

If the Retained Earnings account number is correct, press Enter. If not,
make another selection and press Enter. You will be given an other
opportunity to verify the account. You will pass through another
accounting security gate.


Posting Verification

Accounting End of Year Adjustments is a trip through Create Source
Documents. The following posting verification screen will display:

Cmdl-End job

SECURITY GATE
Accounting

x0001-001

Enter Division Code

Enter Security Code

Assign transaction date and G/L month for posting
Enter transaction date (mmddyy): 010187
There are 2 active months

The oldest is January
It is currently February

Enter G/L posting month (01-12): 1

Cmd3-Go back

 

CHOOSE THE FIRST DAY OF THE OLDEST OPEN MONTH FOR
THE POSTING DATE. CHOOSE THE OLDEST OPEN MONTH AS
THE G/L POSTING MONTH.

You want to see the adjustments reflected on the Financial Statement as
close to the beginning of the new year as possible.

When you press Enter, you will have the opportunity to verify the posting
month. If it is correct, press Enter. If not, [Cmd3] to choose another
LL


 

posting date and month. After the selection of posting date and month, the
Post Source Documents Document Entry screen will display just as in
Create Source Documents (X1-7).

Adjustment Lines

The Create Source Document Entry screen below contains the entries
necessary for the example referenced earlier:

WEAVER'S EQUIPMENT POST SOURCE DOCUMENTS 1/01/87 xX2700-101
Division L DOCUMENT ENTRY January ID Document#
Account# Amount Description Addr# Date Discount Stock#

J ADJUST ¢ L120 45000 MISSING BKT

J ADJUST D L600 45000 MISSING BKT

Current line 30 Next line

Press Cmdl to end job; Cmd2 recurrent trans; Cmd3 show line#; Cmd4 show stock#

 

Make any adjustments necessary. If you need help with Create Source


 

Documents, refer to Create Source Documents (X1-7).

When you are ready to move to the next job step, press Cmd1. Choose the
editing options. Refer to Create Source Documents (X1-7).

Check for Errors Screen

Below is the Post Source Documents, Check for Errors screen identical to
the one in Create Source Documents (X1-7).

WEAVER'’S EQUIPMENT POST SOURCE DOCUMENTS 1/01/87 X1710-501

Division L CHECK FOR ERRORS January

Current \display: partial transactions Update line #

Line# Date Document# Account # E Amount Description Addr #
10 J 4-01-87 ADJUST ¢ L120 2w 450.00 MISSING BKT {
20 3 1-01-87 ADJUST D L600 2 450.00 MISSING BKT

*AUTO * 1-01-87 ADJUST © L600 1 450.00 MISSING BKT

*AUTO * 1-01-87 ADJUST D L295 1 450.00

Press Cmdl to end job; Cmd2 partial transactions; Cmd3 full transactions;
cmd4 recap; Cmd5 scan for error; Cmd6 more fields; roll keys

 

In the above example, there is a credit to L120 and a debit to L600. Note
the line crediting L120. Column "E" is the edit code column. It will tell

RELEASE 2.1 LL


 

you what Edit Code was entered for the General Ledger

account number in General Ledger Maintenance (X14-2). L120 has a W
Edit Code. It is an Equipment Inventory account.

Normally you would be required to enter a stock number, indicating which
piece of equipment was missing the bucket. However, notice the 2 in the
same column. The 2 means that the Edit Code was overridden. This
override means the general ledger can be affected without using a Unit
Number.

The Unit Numbers appear on a subledger report called Current Inventory
(X2-6). The total on the subledger report should equal the general ledger
account balance. Because we are posting to the general ledger without
affecting the subledger, the subledger and general ledger will be out of
balance.

Accounts with Subledgers

Accounts that have subledgers are:

Subledger Report
Receivables Aged Receivables Report
Payables Aged Payables Report - Trade
Flooring Aged Payables Report - Flooring
Inventory Current Inventory Report

Accounting End of Year Adjustments will always override any Edit Codes
on the general ledger accounts. The subledgers and general ledger
accounts will always be out of balance. If you are making an Accounting
Year End Adjustment to any general ledger account that has a subledger,
refer to the section Bringing the Subledger Reports Back Into Balance


 

with the General Ledger.

The same transaction information will be on the End of Day report and on
the General Ledger Register, which prints when you run End of Month. A
perfect audit trail.

The 2 in Column "E" on the line crediting L120 and the 2 on the line
debiting L600 also have another meaning. Not only will the 2 override the
Edit Code but the transaction will be posted to the Thirteenth month. This
will correct the End of Year balances.

Only line # 10 and line # 20 were entered. That transaction generated an
automatic transaction. The "*AUTO *" indicates an automatic transaction.
You supplied the Retained Earnings account number earlier in this job.
The Retained Earnings account contains the profit or loss for the previous
fiscal years. Since the balance was not correct at the beginning of the year,
the account balance must be adjusted to reflect the change made using the
Accounting End of Year Adjustment.

Again looking at the *AUTO transaction, the 1 under the column "E"
means override the Edit Code. The transaction will be posted to the
selected posting month. If there was an Edit Code on the general ledger
account, it will be displayed next to the 1. In our example, there was no
Edit Code. There is no subledger to bring back into balance. The
transaction is correcting the Retained Earnings account balance, L295, and
the operating statement account, L600.

Provided the debits and credits balance, there should be no errors in the
batch because the Edit Codes are overridden. You are not required to
provide normal information like an address number, due date, discount, or
unit numbers. Review the batch carefully to make sure you are affecting
only the accounts you need to.


 

If you need help in correcting errors, refer to Chapter X1-7, Create Source
Documents.

Edit List

When you are ready to proceed to the next job step, press Cmd1 to end
job. The following screen will display:

WEAVER'S EQUIPMENT SHOP POST SOURCE DOCUMENTS 1/01/87 + x1710-503
Division L CHECK FOR ERRORS January

End of job option: 1
1. Return to processing -- do not end job
End job with printed edit list

2.
3. End job without printed edit list
4. Create new edit list.

No errors have been detected. This batch may be posted.

 

Select option 2, End job with printed edit list. Press Enter. Save this edit
list and file it with other End of Year reports. The edit list will also print in
the End of Day report for your daily report file.


 

Posting the Batch

The following screen displays:

COMMAND
(c) DIS Corp.

No Errors Have Been Detected

1. Post Source Documents

23, Return To Editor Correction Menu

Ready for option number or command

 

Select option 1, Post Source Documents. Press Enter. The Accounting End
of Year batch is posted.

RELEASE 2.1 CO


 

### Checking Results Of Adjustments

Run the financial statement for the last fiscal month of last year (X15-2).
In the example we are using, the year ended in December.

Month: 12
Open/Closed: C

Then run a financial statement for:

Month: 13
Open/Closed: C
(Thirteenth month always displays as closed)

Compare the Thirteenth Month to the December statement. You will see
the changes. The Equipment Inventory account will be $450.00 less, the
Sales Department Expense account will $450.00 more. Current Profit/Loss
will have a decrease of $450.00 because expenses went up $450.00.

Run the financial statement for the month you posted to in the current
year. In the example we are using, we had not closed any months since
closing the year. This will allow adjustments to be visible on the January
financial statement. The Retained Earnings account, which contains the
profit/loss for last year and all previous years, will show a decrease of
$450.00. The Equipment Inventory account will show a decrease of
$450.00. The Sales Department Expense account will show no change.
There was a debit and credit of $450.00 to the account. The year-to-date
total for this account is not affected.


va

 

BALANCING SUBLEDGERS WITH THE G/L

Still using the case of the missing bucket example, we would run a Current
Inventory Report. The Current Inventory Report will contain all activity
on Unit numbers up to the present date. The totals are current and should
balance to the current months Financial Statement. Run a Financial
Statement for the current open month.

In the example we are using, the Current Inventory Report balance will be
$450.00 more than the General Ledger. The General Ledger was credited
$450.00 but the subledger, Current Inventory Report, was never affected

by $450.00. The Unit Number of the Backhoe that should have contained

the bucket was UC4502. We now have to lower the cost associated with

UC4502 by $450.00. (

From the Accounting Menu, select option 7. Create Source Documents.
The task of bringing the subledger back into balance is performed in
Create Source Documents, not Accounting End of Year Adjustment.

After passing through the security gate, you will be asked to choose a
transaction date and posting month. Use the first day of the oldest open
month. For more information on Create Source Documents, see Chapter
X1-7, Create Source Documents.

Below is the transaction as it would be entered on the Create Source
Documents Document Entry screen:

RELEASE 2.1 LO


X1.12-2_ ACCOUNTING END OF YEAR ADJUSTMENT

 

WEAVER'S EQUIPMENT POST SOURCE DOCUMENTS 1/01/87 =X1700-101
Division L DOCUMENT ENTRY January ID
Decument# Account# Amount Description Addr# Date Discount Stock#

J ADJUST SUB C L120 45000 SUB- EOY uc4so2
J ADJUST SUB L120 45000 SUB -EOY


Current line 30 Next line

Press Cmdl to end job; Cmd2 recurrent trans; Cmd3 show line#; Cmd4 show stock#

 

Notice on the two lines, we have used the same general ledger account
number. The general ledger balance is correct. What you want to do is
affect the unit number only, UC4502.

On the first line the Equipment Inventory account has been credited
$450.00 on Unit Number UC4502. The second line uses the "override
symbol" to debit back the $450.00, leaving the general ledger account with
the original balance.

The symbol ">" is used to debit the account instead of D. The D would
require you to use a Unit Number as usual. However, the ">" allows you to
make an entry to the General Ledger account without affecting the
subledger.


 

The symbols look like this:

>
<

D for debiting
C for crediting

When you are ready to move to the next job step, press Cmd1. Choose the
editing options. The following screen will display:

WEAVER'S EQUIPMENT POST SOURCE DOCUMENTS 1/01/87 1710-501
Division L CHECK FOR ERRORS January
Current display: partial transactions Update line #
Line# Date Document # Account # E Amount Description Addr #
10 J 1-01-87 ADJUST SUB C L120 w 450.00 SUB- EOY
20 J 1-01-87 ADJUST SUB D L120 lw 450.00 SUB -EOY
End of transactions

Press Cmdl to end job; Cmd2 partial transactions; Cmd3 full transactions;
cmd4 recap; Cmd5 scan for error; Cmdé more fields; roll keys

Notice the "E" column in the above example. On line 10, the column
contains a W. There is no 1 or 2 next to the W edit code. The account has
been affected normally. The subledger containing the stock number has
been credited the $450.00.
{

LL


 

On line 20, the column "E" contains a 1 next to the W edit code. This
means that the Edit Code was ignored. The subledger was ignored but the
General Ledger account was debited $450.00. When this batch is posted,
the subledger will be in balance with the General Ledger.

Looking at the Recap, (Cmd4) may help you with this concept:

WEAVER'S EQUIPMENT POST SOURCE DOCUMENTS 1/01/87 X1710-501
Division L CHECK FOR ERRORS January
Current display: recap

**** RECAP **** Account# Title Debit Credit
L120 NEW INVENTORY 450.00 450.00
Recap Totals 450.00
End of recap

Press Cmdl to end job; Cmd2 partial transactions; Cmd3 full transactions;
Cmd4 recap; roll keys

Notice that the General Ledger account has been debited and credited
$450.00. The net effect is zero dollars posted to the Equipment Inventory
account. The subledger containing the Unit number has been credited
$450.00, decreasing the cost of the Unit. When the entry is posted, the
subledger will be back in balance with the General Ledger.


 

You may apply these rules to any other subledgers that were affected by
year end adjustments.

If there are any errors in the batch, they will have to be corrected. If you
have questions on correcting errors, refer to Chapter X1-7, Create Source
Documents.

When all errors have been corrected, Cmd1 to end job. The following
screen will display:

WEAVER'S EQUIPMENT SHOP POST SOURCE DOCUMENTS 1/01/87 1720-503
Division L CHECK FOR ERRORS January

End of job option: 1
1. Return to processing ~- do not end job
- End job with printed edit list (

3. End job without printed edit list
4. Create new edit list.

No errors have been detected. This batch may be posted.

 

Select option 2, End job with printed edit list. Press Enter. Save this edit
list and file it with other End of Year reports. The edit list will also print in
the End of Day report for your daily report file.

RELEASE 2.1 LO


 

The following screen displays:

COMMAND
(c) DIS Corp.

No Errors Have Been Detected

1. Post Source Documents

23. Return To Editor Correction Menu

Ready for option number or command

 

Select option 1, Post Source Documents. Press Enter.

### Adjustments Between Divisions

Adjustments between divisions may involve more work. The Retained
Earnings account is tied to the Income Statement on the Financial
Statement. Income statement accounts are Sales, Cost of Sales, Expense
and Income accounts. If cross divisional adjustments involve income
statement accounts, follow the directions on the following page:


 

Income Statement Accounts, One Division

If you are adjusting an income statement account in one division and a
balance sheet account in another division, make the adjustment in the
division where the correction is to the income statement account.

For example, Weaver's Equipment has two divisions A and B. All of the
receivable accounts are in division A. However, a sale was made in
division B that cannot be collected. Weaver's Equipment needs to write off
the bad debt, charging B division the expense. The accounting would look
like this:

Credit A111 Accounts Receivable $150.00
Debit B685 Bad DebtExpense $150.00

At Accounting End of Year Adjustment, Weaver's Equipment selects
division B. The retained earnings account they select would be B295.
Follow the directions in the chapter to process the batch.

Income Statement Accounts, Two Divisions

The retained earnings general ledger account can only be affected in the
division containing the income statement account. If you must make an
adjustment to income statement accounts in both divisions, you will have
to post two Accounting End of Year Adjustment batches, one in each
division.

For example, Weaver's Equipment has two divisions, A and B. Division B
purchased a new time clock for the service department. The expense was
accidentally charged to division A. This must be corrected. The accounting
would look like this:

RELEASE 2.1 LU


 

Credit A693  ShopExpense $2385.00
Debit B693 ShopExpense $2385.00

The work must be performed in two batches, one in each division.

Division A: Weaver's Equipment selects division A at Accounting End of
Year Adjustments. The retained earnings account number is A295.
Division A was charged the expense in error. Weaver's Equipment will
credit the expense A693 and debit the division's transfer account A180. On
the screen, they enter:

WEAVER'S EQUIPMENT POST SOURCE DOCUMENTS 1/01/87 1700-101
Division A DOCUMENT ENTRY January

ID Document# Account# Amount Description Addr# Date Discount Stock#
J ADJUST Cc A693 238500 WRONG DIVIN

J ADJUST D A180 238500 WRONG DIVIN

Current line 30

Press Cmdl to end job; Cmd2 recurrent trans; Cmd3 show line#; Cmd4 show stock#


 

The batch is posted. See previous sections in this Chapter.

Division B, in Accounting End of Year Adjustments, division B is
selected at the security gate. The retained earnings selected is for division
B, B295. The expense account B693 is debited, and the transfer account is
credited.

On the screen, the following is entered.

WEAVER'S EQUIPMENT POST SOURCE DOCUMENTS 1/01/87 X1700-101
Division A DOCUMENT ENTRY January

ID Document# Account# Amount Description Addr# Date Discount Stock#
J ADJUST D B693 238500 WRONG DIVIN

J ADJUST c B180 238500 WRONG DIVIN

Current line 30

Press Cmdl to end job; Cmd2 recurrent trans; Cmd3 show line#; Cmd4 show stock#

 

The batch is then posted. See the directions in this chapter.

RELEASE 2.1 L.

## CHAPTER X1.12-3


### Introduction

cleared from the u.EMH file and the u.EGT file, which holds the event
log. Employee entries, however, will never be purged and they will remain
on the system forever.

### Preparation

O) Make sure you have paid the last payroll for the previous calendar
year. The Year to Date fields and hours posted for each employee will

CO) Make sure you have printed W-2 forms. Again the fields needed to run

O Backup your data files.


### How To Run

Select option 3 from the Accounting End of Year Menu. After passing
through the security gate, press Enter. When the job is complete, you will
return to the Accounting End of Year Menu.

Make sure the job clears the User Board before Tunning any other
accounting jobs.

## CHAPTER X1.12-4

DEPRECIATION END OF YEAR

### Introduction

Depreciation End of Year is for dealers who are using the system to
depreciate units automatically. This job moves the figures in the "Current
Depr" field in Inquire/Update Units to the "Past Depr" field and sets
"Current Depr" to zero. This job should be run at Fiscal Year End. The job
is divisional and must be run for each division individually.

### Preparation

CO Run a depreciation report for the closed month (X27-3).

NO OTHER JOBS CAN BE RUNNING.
You will have a record of what was in the Current Year Depreciation. This
is important because Units End of Year will transfer this balance into Prior
Years Depreciation. This report can be used for tax purposes.

QO) Backup your data files.

O Make sure no other accounting jobs are running.

### How To Run

From the End of Year menu, select option 4. When the job is compete, you
will return to the End of Year menu.

For example, we will say that the fiscal year ended in December.
December was closed before you closed your year. January is still open.


[| X1.12-4 DEPRECIATION END OF YEAR

After running Units End of Year, run a Depreciation Report (X27-3) for
January. The "Year-to-Date Depr" should be the same as "This Month
Depr". This is an easy way to check the results. File the reports with your
End of Year information.

RELEASE 2.1 Lo

## CHAPTER X1.12-5

RECEIVABLES FILE MAINTENANCE

### Introduction

Receivables File Maintenance will remove all deleted receivables address
numbers from the ADM, Address Master file, and REM, Receivables
Master file where they are stored. Also, deleted customer transactions are
removed from REA, Receivables Transaction file and REH, Receivables
History Transaction file. This job will make more room on the disk of the
computer. The files will be smaller.

### The Result Of This Job On The System

When a customer is deleted, you have the option of reinstating that
customer. When the customer is reinstated, all history and information for
that customer is available for review. If you were to print a Receivables
Master Report, for example, all customer information and transactions
would be printed on the Master Report. Once a customer if purged, all
record of that customer is gone. Be sure that this is what you want to do.

Below is a suggested schedule for Receivables File Maintenance. Run the
job at fiscal year end. It will clean your files for the new year.

O Run a Receivables Master Report (X1.1-10). All information and
transactions for all receivable customers that have not been deleted
will be on the Masters Report.

 

O Delete the receivable customers you want to be purged (X11-2).
O Backup your data files.
O Run this job.

Having a Receivable Master Report will make history on the customer
readily available if questions should arise.

## X1.12-5 RECEIVABLES FILE MAINTENANCE

 

### How To Run

Before running this job, make sure no other Accounting jobs are running.

From the End of Year Menu, select option 5, Receivables File
Maintenance. The security gate gives you the opportunity to run the job
for all divisions or each division individually.

After passing through the security gate, the following screen will display:

***WARNING*** This job may not be run while any other accounting jobs are
running. Also, make sure you have made a backup of your files.

If there are any accounting jobs running or you need to make a

backup, press CMD1 to cancel.

This program will list those addresses that you have deleted
in Receivables Maintenance. The next screen will give you the
option of purging these addresses.

Press CMD1 to cancel CMD2 to continue

 

RELEASE 2.1 LO


1.12-5 RECEIVABLES FILE MAINTENANCE

 

Press Cmd2 to continue. A report of all the address numbers that will be
purged will print. A report containing all address numbers that cannot be
purged and the reason will also print. See the following samples.

WEAVER'S EQUIPMENT RECEIVABLES FILE MAINTENANCE DATE 1/27/86 PAGE 1
BELLINGHAM WA LIST OF DELETED RECEIVABLES CUSTOMERS WHICH WILL BE PURGED X1C50-4A
ADDRESS #

BUHWAR

DLDWAR

HOWWAR

### Dyrwar

WEAVER'S EQUIPMENT RECEIVABLES PILE MAINTENANCE. DATE 1/27/86 PAGE = 2
BELLINGHAM WA L EXCEPTION REPORT x1C50-4B
ADDRESS # DELETED CUSTOMER WILL NOT BE PURGED FROM YOU PILES POR THE FOLLOWING REASON

RECEIVABLES FILE MAINTENANCE, x1050-002

### Purge Addresses

 

When the report is printing the following screen displays:

***WARNING*** This program will PURGE all addresses from your files that were
listed on the preceding printout.

If you do not want to PURGE these addresses, press CMD1 to cancel. Then run
Receivables Maintenance to remove the delete and rerun this program.

If you are sure you want to PURGE these addresses press CMD2 to continue.

Press CMD1 to cancel CMD2 to continue

 


 

Press Cmd2 to continue. Three reports will print:

O RECEIVABLES FILE MAINTENANCE
LISTED CUSTOMERS HAVE BEEN DELETED FROM YOUR
RECEIVABLES MASTER FILE: The first report will contain the
address numbers of all the customers that have been purged from your
Receivable Master File.

QO RECEIVABLES FILE MAINTENANCE
PURGED FROM RECEIVABLE TRANSACTION FILES:
The second report contains the transactions that have been purged for
each purged customer.

QO RECEIVABLES FILE MAINTENANCE
PURGED OR MODIFIED IN CUSTOMER MASTER FILE:
The third report will list all the information: Name, Address,
Extended Name, Extended Address, City, State and Zip Code for each
purged customer.

Make sure the job clears the user board before starting any other
accounting jobs.

File all the reports with your end of year reports. They will help as an
audit trail should questions arise.

If only one division was purged, repeat the steps above for all other
divisions.

RELEASE 2.1 LL

## CHAPTER X1.12-6

PAYABLES FILE MAINTENANCE

### Introduction

Payables File Maintenance will purge records from PAA (the Payables
Transaction file). It is a divisional job. This will make more room on the
computer disk. The files will be smaller.

### The Result Of This Job On The System

When a vendor address number is deleted, it can be reinstated. When the
address number is reinstated, transaction history is available for review on
that vendor. Once the vendor address and transactions are purged, there
will be no record of the vendor. Make sure this is what you want to do.
You may do this job anytime during the year. If you perform this job at

fiscal year end, your files are clean for the new year. This may help with
disk space.

### What To Do Before Running The Job

C Delete any Vendor Address Numbers (X12-2) you want purged.
O) Make a backup of your data files.

O No other accounting jobs can be running.


[2 | X1.12-6 PAYABLES FILE MAINTENANCE

### How To Run

From the End of Year menu, select option 6, Payables File Maintenance.
At the security gate, decide if you want to run the job for all divisions. The
following screen displays:

ABC TRACTOR CO. PAYABLES FILE MAINTENANCE X10601-01
Division A

*** All History transactions prior to the period entered will be Purged ***

Purge Period

Leave period blank to not purge History Transactions. {

*** Enter ‘Y' to purge Information ***

Purge Deleted Vendors

 

If you want to purge transactions, enter a month and year in the Purge
Period field. All transactions prior to that month will be purged. You can
also opt to purge deleted vendors from the system. To run this job, at least
one of these two fields must be completed. Press [Enter] to continue. The
following screen appears.

RELEASE 2.1 LU


X1.12-6 PAYABLES FILE MAINTENANCE [2 |

ABC TRACTOR CO. PAYABLES FILE MAINTENANCE X1C601-02
Division A

Confirmation

Purge Period

Purge Deleted vendors

Confirm ..: N  (¥/N)

Cmd3~-Return, Enter-Continue

 

To continue with the purge, place a "Y" in the Confirm field and press
[Enter]. Three reports will be sent to the system printer.

O) PAYABLES FILE MAINTENANCE
LISTED VENDORS HAVE BEEN DELETED FROM YOUR
PAYABLES MASTER FILE
The report lists the address numbers of the vendors that have been
deleted from the master file.


[+ | X1.12-6 PAYABLES FILE MAINTENANCE a

O PAYABLES FILE MAINTENANCE
PURGED FROM PAYABLES TRANSACTION FILES
The report lists all transactions purged from the payables _ transactions
files.

O PAYABLES FILE MAINTENANCE
PURGED FROM PAYABLES TRANSACTION FILES
This report lists the information for the purged vendors including
address number, name and address, extended name and address, City
and State, and zip code.

File these reports with your payables information or end of year file. These
audit trails will be available if questions arise.

Make sure the job clears the user board before proceeding with any other {
accounting jobs.

RELEASE 2.1 oe

## CHAPTER X1.12-8

RENTALS END OF YEAR

### Introduction

Rentals End of Year sets Year-To-Date (YTD) figures to zero for Rental
Status and the Utilization Report. Run it at the end of the calendar year.
The job is divisional and must be run for each division individually.

### Preparation

O Backup your data files.

O Make sure no other accounting jobs are running.

### How To Run

From the End of Year menu, select option 8. When the job is complete,
you will return to the End of Year menu.


Notes:

RELEASE 2.1 LU

## CHAPTER X1

ACCOUNTING OVERVIEW

### Introduction

The DIS Accounting Menu is a major functional area of the integrated DIS
System. As part of an integrated system, transactions which occur in Point
Of Sale can automatically be posted to the General Ledger. It is also
integrated with the Parts Inventory Control System through the posting of
actual costing on part sales. Some of the major features of the Accounting
System include an unlimited number of subsidiary journals and automatic
error checking to ensure balanced and valid entry of transactions.

MENU SUMMARIES

X1-1

X1-2

Receivables Menu

The accounts receivable applications are designed to assist you to manage
one of the most important assets of your business - the money owed by
your customers. These applications provide timely information to help
improve cash flow and reduce bad debt losses. Invoice transactions from
Point Of Sale are automatically posted directly to the General Ledger and
the Receivables Subsidiary Ledger. There are no limits to the number of
accounts receivable sub-ledgers on the DIS System. For more information
on Accounts Receivable, see the introduction in the Accounts Receivables
Menu ( X1-1).

Payables Menu

The accounts payable applications are designed to assist you to control the
outflow of cash and maintain accurate records of liabilities to trade,
flooring and other vendors. Payable items are handled on an accrual basis.


[| X1 ACCOUNTING OVERVIEW

X1-3

X1-4

X1-5

X1-6


Computations are posted automatically to appropriate General Ledger

General Ledger Menu

The General Ledger is the key to the DIS Accounting System. Options on
this menu allow you to setup General Ledger accounts and subsidiary
journals. The General Ledger overview will explain the way to setup the
general ledger. The instructions provided will help you to create a chart of
accounts that will be easy to use.

Financial Reports Menu

The financial reports applications provide current and historical financial
information that is available whenever, and as frequently as you wish.

Transaction Menu

Options on the Transaction Menu allow you to inquire on previously
posted accounting transactions. This information is available in the form
of simple inquiries or user defined reports.


X1 ACCOUNTING OVERVIEW [= |

X1-7 Create Source Documents

Create Source Documents is used to post manual transactions to the
General Ledger and to the subsidiary ledgers. With this job, you post all
types of transactions. All sub-ledgers are posted at the same time the
posting occurs to the General Ledger. Consequently, the two should
always remain in balance. The transactions entered will be edited to ensure
balanced and valid entry of transactions. If there are any errors, the
transactions cannot be posted.

X1-8 Compute Hours For Time Cards

Compute Hours For Time Cards allows you to convert, compute, and add
payroll hours.

X1-9 End of Day Procedures

Accounting End of Day allows you to print an audit trail of all changes to
your accounting files since the last time End of Day was run.

Reports will list changes made to information, a log of transaction entries,
and a recap summary of General Ledger posting totals.

X1-10 End of Month Menu

Options on this menu allow you to close the oldest open General Ledger
month, run audit trail reports, and perform file maintenance to increase the
efficiency of your system.


[ «| X1 ACCOUNTING OVERVIEW _
/

X1-11 Journals Menu

Journals, which can be activated or de-activated at any time, are installed
using the DIS OPT Library (see APPENDIX). On the Journals Menu there
are options for creating and describing as many Journal IDs as you need
and for assigning Journal IDs to automatic transactions such as Monthly
Billing. Transactions from Point of Sale are directed to specific journals
through sales codes.

X1-12 End of Year Menu

Accounting End of Year jobs close your accounting year and open a
thirteenth month to which you can post year- end adjusting entries.
Additional jobs allow the purging of inactive information from your files. (

RELEASE 2.1 LL


X1 ACCOUNTING OVERVIEW [=]

ESTABLISHING ACCOUNTING PROCEDURES

### Introduction

This section provides some suggestions on establishing procedures for use
by your company's accounting department.

System procedures are an important, but often neglected area in the
operations of any computer system. Installing a computer system often
brings integration to many companies operations for the first time.

With a manual system, departments usually work almost independently of
one another. The individual departments are only responsible for providing
other departments with certain bits of information at certain times. A
computer system brings a requirement for integration of information. One
department becomes responsible for the input of certain information before
another department can proceed with its responsibilities.

Benefits from establishing procedures include:

= Eliminating conflicts on the usage of the system.

= Reducing the time it takes to perform jobs.

= Establishing clear responsibilities so jobs are sure to be performed.


[ «| X1 ACCOUNTING OVERVIEW es
{

### Establishing Responsibilities

Establishing responsibilities allows for defining clear-cut lists of duties for
each person who uses the system. These lists aid in improving the
efficiency of each department's operations.

The primary concern for establishing responsibilities is to make sure that
certain jobs will be performed on the system. Without having
responsibilities defined, you may have duplication of duties or, worse yet,
certain duties for which nobody is responsible.

The first step in establishing responsibilities is to identify what everyone's

current responsibilities are. This can be done by creating a list of each

person's current duties on the system. Once you have created these lists, (
any overlaps or gaps in responsibilities will become evident. Correcting

these gaps or overlaps will give you a new list of assigned responsibilities

for each person.

### Establishing Procedure Checklists

The primary purpose of establishing procedure checklists is to document
what people have learned about operating the system. Each person who
works with the computer knows certain details of the system operation that
are very valuable to the operations of the company. Documenting the way
you perform certain jobs helps when someone is away due to vacation or
illness and when it comes time to train new employees.

co

## X1 ACCOUNTING OVERVIEW

Individuals are sometimes reluctant to share the knowledge they have about
operating the computer. They mistakenly believe that by keeping this
information to themselves, they will enhance or secure their own positions
within the company. This idea is detrimental to both the individual and the
company. For the individual, this means that they can never be ill or go on
vacation without their work back- logging on their desks. It also means that
they lock themselves into one position within the company. For the
company, it means that they are entirely dependent on one person to
perform certain functions. What if that person becomes ill or wishes to
retire? It also does not allow for any growth paths for people within the
company.

After having established responsibilities from the previous section, you can
now create checklists of all of the identified accounting functions on the
system. Each person who has the most experience running certain jobs
should write down each detailed key stroke and decision that they make
when they run a job. After writing down the steps needed to run a job, the
checklist should be checked for accuracy and then given to a person
inexperienced to see if they can actually run the job without error. Collect
these checklists into confidential binders. Access to this information may
have to be controlled if each procedure contains passwords.


X41 ACCOUNTING OVERVIEW Le

### Scheduling Jobs

Developing a calendar schedule of jobs to be performed ensures that jobs
will always be run on time and in the proper sequence.

After having examined your individual responsibilities and checklists of
procedures, you can now incorporate all of this information into calendars
of events for your department. This process should be done for each
department using the DIS System. This will ensure that each department
will have a schedule which specifies when jobs need to be run that affect
the schedules of other departments.

Create a schedule calendar by marking a large sheet of paper with blocks

for seven days and four weeks. Within the blocks, write down procedures (
on the days that they should be performed along with a primary and

secondary person responsible for running the jobs. You should consider

how certain jobs affect other departments and the sequence in which jobs

should be run.

The critical procedures table and the suggested schedules on the following
pages will help in developing your calendar of jobs.

RELEASE 2.1 LU


X1 ACCOUNTING OVERVIEW [2]

SUGGESTED ACCOUNTING SCHEDULES

Daily

IPL (Initial Program Load)
Alerts you to disk problems

Backup
Cheapest insurance you can buy

Run Accounting End of Day as option at backup or choose X1-9.

No other accounting jobs can be running at this time.

 

Accounting End of Day is a report. It does not DO anything, but it is your
AUDIT trail. If you skip a day, everything will pile up.

When it is printed is not critical. If you are tired and want to go home, call

for Accounting (and Parts) End of Day at backup, but let them print next
morning (see How to Backup).

Note:

Parts End of Day MUST be run daily, preferably at backup. It does DO
something. It updates parts history.

 


On Accounting End of Day be sure to look for:

Unequal debits and credits. This is a BIG DEAL.

Do not attempt to "fix" this problem. Contact DIS immediately. It
will be just as well not to do a lot of work until this is straightened
out. It may be time to delete and restore.

Edit code overrides. Look for a "1" beside the edit code.
Example: 1A, 1W, 1P. This means the bridge between the general
ledger and its subsidiary account has been broken. Know why.

Extraordinary amounts.
Review the recap, particularly accounts affected by automatic
transactions.

Zero amounts. OK if intentional -- such as to add a comment to a
transaction line in Create Source Documents.

Daily, at a Regular Time

Create Point of Sale Posting Batch (X55-1)
The Point of Sale batch seals off one business day from another. It
is the time to count the till.

Here are three acceptable procedures:
O Create the batch at the end of the business day when you are
through using Point of Sale. Review it the next moming.

This will leave u.@dSAE and u.@dSA7 on your disk (u =
your user ID, d = your division code).
Lo


X1 ACCOUNTING OVERVIEW In]

O Create the batch first thing in the morning before Point of
Sale is begun. Review the batch whenever it's convenient.

O Create and review the batch before backup.

Review and Post Point of Sale Documents (X55-2)

Daily, as Needed

Enter new Receivables, Vendors, Employees, and Whole Goods
Post Received on Accounts (Create Source Documents or POS)
Create and post source documents (X1-7)

Approved vendor invoices

Manually written checks

Journal entries
Bank deposits


[| X1 ACCOUNTING OVERVIEW Cc

Weekly


Run reports as desired

Aged Payables Summary Report (X12-5)
Sales Price Book (X2-11)

For Open Item billing, run Receivables Credits List (X1.14-6)

__ Apply Credits (X11-4) or run Auto-Merge

Bi-weekly

Run Aged Payables Report (X12-4)

Merge manual checks with related invoices through
Correct Due Dates and Discounts (X12-7)

Run Payables Due Today Report (X12-6) and Print Payables
Checks (X12-8)


RELEASE 2.1 LU


X1 ACCOUNTING OVERVIEW [3]

Monthly

Run statements.

Close General Ledger Month.

Try to be prompt in closing General Ledger months. The file which
holds current transactions gets too large to be efficient when there
are many open months.

On last day of the month run:

Financial Statement (X15-2)

Subledger Balance Report (X14-5)

The Subledger Balance Report prints a list of General Ledger accounts that
have edit codes of A (Receivables), P (Payables), W (Units), and F
(Flooring). It prints the balance of each General Ledger account and
compares it to the total of its subledger balances, which should be equal. It
is the same as if you ran all of the following reports and compared them to
the balances on the Financial Statement:

Aged Receivables Report (X1.14-1)

Aged Payables Report (X12-4)

Current Inventory Report (X2-6)

Floored Units Report (X2-12)

Resolve any discrepancy between a General Ledger account and its
subledger at once.


X1 ACCOUNTING OVERVIEW _
{

### Integrating Departments

Certain procedures on the system affect other departments within your
company. Identifying critical jobs allows you to schedule jobs in sequences
that minimizes disruptions and conflicts.

The Critical Procedures Table in this section lists jobs that require special
attention. The applications listed on the left require that the jobs listed
under exclusions not be run at the same time. When running Monthly
Billing, there can be no postings to Accounts Receivable, and Point of Sale
cannot be running from the time you take the option for billing until you
get back to a menu (monthly billing has been put on the job queue).

{
RELEASE 2.1 Ne


File
Application Update

End Of Day No
End Of Month
Mo. Billing
P/R Checks
Checks

UNITS

Create Depr. Batch
Depr. Batch
Report

End Of Day

End Of Month

End Of Year
Reprice Parts
Create Price Book
Reconfigure Parts
Inven. Adjustment

Cust. Index Setup

Create Post. Batch
End Of Month


Prerequisite

None

Backup
Backup
Backup
Backup

None

Backup
Backup
Backup
None

Backup
Backup

None

Close Docu.
Backup

CRITICAL PROCEDURES TABLE

Exclusions

Dedicated System
Dedicated System
Dedicated System
No X1

No X12 or X17

Dedicated System

No Cmd2 at POS
No POS activity

Frequency

Daily
Monthly
Monthly

As Needed A/P
As Needed

As Needed Post
As Needed Depr.
As Needed

Daily
Monthly
End of Year
As Needed
As Needed
As Needed
As Needed

Daily or As
Needed

Daily

Monthly

 

The most common problem people have with critical procedures is with the
Point Of Sale Posting Batch. We can see from the Critical Procedures Table
that certain jobs must be excluded from the system when this job is run.
Since the posting batch is taking information from all the closed but not
posted documents from the Point Of Sale SAM file, other jobs that use the
SAM file must be excluded. These jobs


include Point Of Sale End of Month, which clears all closed and posted
documents and the Cmd2 - Print and Close procedure from the Point Of
Sale Invoicing program.

Since the Print and Close function of Point Of Sale needs to be excluded,
you either have to train your people not to close documents during the
creation of the posting batch or you need to shut down Point Of Sale
completely. The safest thing to do is to shut down Point Of Sale
completely. Someone may accidentally Print and Close during the batch
creation. If you create the posting batch during the middle of the day, you
may be greatly inconveniencing the parts counter. You need to decide on
the time of day that would least interrupt Point Of Sale activities. Most
users shut down the parts counter right before doing back-up for the
evening. This may be at 4:30 or 5:00.

Some suggested procedures are listed below:
ae


Point of Sale Posting Batch

 

[1 Shut down the parts counter at 4:30 or 5:00. Write invoices by hand if
necessary.

O Count the till.

 

O Run back-up without End-of-Day (runs faster).

 

(J Run End-of-Day Procedures (parts and accounting).

 

(1 Hold the print spool for printing the next morning.
OQ Run Create Point Of Sale Posting Batch.
CO] Review and Post the batch the next morning.

O Next morning, have the parts counter recreate manual tickets on the
system if necessary.

Monthly Billing

This sequence of steps will ensure that your statement run will include all
possible work orders and invoices. The Parts and Service departments will
know that it is their responsibility to close all possible documents before
statements are run. This often speeds up a considerable amount of cash
flow.

O Run Work in Process Reports separately for the shop and parts
departments. Have each department close appropriate documents.


X1 ACCOUNTING OVERVIEW .

O Run Aged Receivables Report (X1.14-1). Review it for payments which
have not been posted.

OO For Open Item billing, run Receivables Credits List. Apply Credits or
Auto-Merge.

O Backup on monthly billing diskettes (2 sets - even and odd months)
DO NOT SKIP THIS STEP. YOU WILL BE SORRY IF YOU DO
Hint: Get this far by regular backup time. Finish first thing the next
morning.

Note:

### No Create Source Documents (X1-7), Accounts


 

CO) Print Statements (X11-10) can be run at the end of the month or any
other time. You may also want to Print Interim/Past Due Statements
(X11-11) and Calculate and Post Interest (X11-9).

RELEASE 2.1 LO


X1 ACCOUNTING OVERVIEW 19 |

O Skip the option for Receivables Master Report. This is a very long
report. It should be run quarterly; however, it is the same as Receivables
Master Report on the Receivables Menu (X11.14-12), and it's easier to
run from there at some other time.

Keep this report on file for at least one year.

WATCH THE USER BOARD!!!
ou DU DU DU DU DU DU DU DU DU DU DU

FEISS III IIIT ICI IO RR IIR ER ETI EER RR Ee

### Caution

There are 9-10 job steps involved in monthly billing.
Statements print before billing job is complete.

Do NOT run any receivables jobs until ALL x118__
procedures have cleared user board.

FOSS UIISIIGIIOIISISIISIISIS ISIS III EIS ISIC OIIOI EE

DY DU dU DU DU DU DU DU DU DU DU DU

 

O Run Aged Receivables Report.
KEEP THIS COPY AS PART OF YOUR AUDIT TRAIL.


Notes:

RELEASE 2.1 ae

## CHAPTER X2-1

INQUIRE/UPDATE UNITS

### Introduction

Use Inquire/Update Units to:

= add new units into inventory
= maintain unlimited specifications
= update existing units
## delete units from inventory

= select units by
color
description
horsepower
location
make/model
new/used code
product code
product type
serial number
status
year
= browse through units inventory
= display a summary of selected units
= print condensed and detailed reports on one or more selected units
= view and update rental/leasing and fixed asset information on units
® view transactions pertaining to a unit


[2 X2-1 INQUIRE/UPDATE UNITS _
(

### Security

If the units security code is entered at the security gate, both Inquiry and
Update are allowed. Inquiry is allowed on units in all divisions. Update is
allowed on units in the division requested at the security gate. Without a
security code only Inquiry is available.

Summary:

With Units Security Code: Inquire all divisions. Update division
requested at security gate.

Without Units Security Code: Inquire all divisions. No update.

RELEASE 2.2 LO


X2-1 INQUIRE/UPDATE UNITS

### How To Run

From the Units Menu (X2-1), select option 1, Inquire/Update Units. The

entrance screen appears. The entrance screen is also called the Options
screen.

Entrance - Options Screen

A-A&R EQUIPMENT SALES INQUIRE/UPDATE UNITS 10/15/97 =. K21001
Unit Prod N

## Number Cd Make Model Yr Description Color U Le Serial Number st

cmdl-gnd cmd3-Restart Home-Top of list Roll-Page

. Define Search . Transfer Unit
. Inquire Unit » Print Unit
- Update Unit . Print Report of Selected Units

. Add Unit . Display Summary of Selected Units
- Delete Unit

Enter option number:

item number: or unit number: or serial number:
DIS-2059 Roll to display units.

 

The top half of the screen is blank except for the options which are
available throughout Inquire/Update Units.

Option: Description:
Cmd1-End End the job, return to the Units Menu.

UNITS


[| X2-1 INQUIRE/UPDATE UNITS

Cmd2-Open W/O

Cmd3-Restart

Home-Top of List
Roll-Page

Inquire mode only. Displays a list of open
internal work orders for the current unit. To
see work orders for a different division,
press [Cmd3] to return to the entrance screen
and define a search based on that

Return to the entrance screen. Blank out the
list of units.

Go to the first unit in the current selection.
Roll up to see the previous unit. Roll down
to see the next unit.

Note the message at the bottom of the screen: "Roll to display units." You

can press [PgDn] to display all units in the division used at the security

gate; however, you may prefer to start by using one of the options listed at

the bottom of the screen. Brief descriptions of the items on the Options {
screen follow. In this chapter, a full section is devoted to each of the :

options listed below.

Option:
1. Define Search

2. Inquire Unit
3. Update Unit

4. Add Unit
5. Delete Unit

Description:

Select units by division, make/model,
horsepower range, description, etc. Define
Search limits the list to the ones you want to
process.

View unit information. No changes allowed.
Change unit information. Allowed only if
the Units password is used at the security
gate.

Add a new unit to inventory.

Remove a unit from your inventory files.
Restricted to units whose cost is zero. A
warning message is given when you try to
delete a sold unit.

RELEASE 2.2 CC “


UNITS

X2-1 INQUIRE/UPDATE UNITS [= |

6. Transfer Unit Designates units which have been
transferred to other dealerships. Units can
only be marked as transferred if they have a
status of ‘A’ (available) and have zero
inventory and flooring amounts.

7. Print Unit Print detailed information on one unit.
8. Print Report of Print a report (detailed or summary only)
Selected Units of units selected by Define Search.

9. Display Summary of Display a summary of units selected by
Selected Units Define Search.

### Fields & Descriptions

You can always return to this screen by pressing [Cmd3]-Restart. The
fields on the Options (entrance) screen are described below.

## Item number identifying the unit's location

on the screen.

Unit Number Unit's identifying number or stock number.

Prod Cd Product Code. User-defined.

Make Name of the manufacturer.

Model Manufacturer's model type.

Yr Year the unit was manufactured or model
year.

Description Brief description; for example, TRACTOR
or A- TRACTOR. Used to organize the
Sales Price Book.

Color A code indicating the color of the unit.

NU New/Used code. N = New, U = Used.

Le Location. User-defined.


[ «| X2-1 INQUIRE/UPDATE UNITS

Serial Number Unit's serial number or VIN (vehicle identification
number) issued from the manufacturer.
St Unit Status.

A = Available for sale

F = Fixed Asset Unit (established by Start
Date)

R = Rental Unit (established by Rental Start
Date)

S = Sold

T = Transfer

Note:

Entering a Start Date in Fixed Asset Information establishes a unit as a
Fixed Asset with Status = F. Entering a Start Date in Rental

Information establishes a unit as a Rental with Status = R. A Fixed
Asset which is also a Rental is assigned Status = R. When a unit is
sold, the status changes to "S." To establish a status of Transfer=T, a
unit first have a status of ‘A’ (available) and have zero inventory and
flooring amounts.

### Define Search

Use Define Search when you want to work with a limited number of
similar units. You can base the search on one or more of the foliowing
items:

® color


UNITS

X2-1 INQUIRE/UPDATE UNITS

= description

= horsepower range

= location

= make/model (make and model must be used together)
= new/used code

® product code

® product type

- rental status

® serial number

® year

You can use a partial field, such as the first 2 characters only. Don't be
afraid to try any kind of search. The worst thing that can happen is that no
units match your definition- -you can adjust the search criteria and try
again.

From the Options screen (Cmd3-Restart), select option 1, Define Search.
The bottom half of the screen displays the search criteria.


| 8 | X2-1 INQUIRE/UPDATE UNITS

A-AUSTIN TRACTOR & EQUI
Unit Prod

Number Cd
FES798
FE5868
FT0642
FTO781
FTO888
FTS492
FT5539
PTS768

Cmd1-End

Unit Status
Color Code
Location
Description

Make
FORD
FORD
FORD
FORD
FORD
FORD
FORD
FORD

Horsepower Range . .

Model
770-S
758
6600
6600
7700
1700
TW10
1500

INQUIRE/UPDATE UNITS
N
Yr Description Color U
00 M-LOADER
00 O-BACKHOE
00 A-TRACTOR
00 A-TRACTOR
00 A-TRACTOR
A-TRACTOR
00 A-TRACTOR
00 A-TRACTOR
cmd3-Restart Home-Top
mos mansessossssces:

Define Search

New/Used Code
Product Code... .
Serial Number
Division Code
Rental Status

11/04/97 X21001

Serial Number

17853
80063
c002468
621249
642972
U700982
C6é16601
US02617
list


APHY PHYO

Roll-Page

 

The limits of the fields on the Define Search screen are listed below. 5.2 D
means 5 digits including 2 decimal places (123.45).

Unit Status
Color code
Location . .
Description

6characters Model.......

2.0 digits

New/Used code...

lcharacter Product code ...

5 characters

2 characters Division code.
12 characters Rental status . .
Horsepower Range .. 3 digits each field

Valid rental status codes are:

Null Status
Available
Demo

7K

AV
DE

Serial Number .

9 characters
1 character
2 characters
17 characters
1 character
2 characters

Ne


UNITS

X2-1 INQUIRE/UPDATE UNITS [°]

Light Service LS
Major Service MS
Rented RE
Sold So
Waiting for Delivery WD

Waiting for Light Service WL
Waiting for Major Service WM
Waiting for Pickup WP

Remember:

O Make and model must be used together.

O You can use part of a field, such as the first 2 characters.

O To see the units in all divisions, leave the division code blank.


[| X2-1 INQUIRE/UPDATE UNITS

The following example illustrates a search from Division A for Fords in
Division B.

A-AUSTIN TRACTOR & EQUI INQUIRE/UPDATE UNITS
11/13/97 X21001 Unit Prod N
## Number Cd Make Model Yr Description

Color U Le Serial Number St

1 FES798 FORD. 770-5 00 M-LOADER MO 17853
2 FES868 FORD 758 00 O-BACKHOE MO 80063

3 FT0642 FORD 6600 00 A-TRACTOR LO €002468
4 FTO781 FORD 6600 00 A-TRACTOR LO C621249
5
6
7
8

FTO888 FORD 7700 00 A-TRACTOR LO C642972

FT5492 FORD 1700 00 A-TRACTOR MO 0700982

FT5539 FORD 00 A-TRACTOR LO C616601

FT5768 00 A-TRACTOR MO U502617

Cm@l-End Cmd@j-Restart Home-Top of list Roll-Page
sessesseses: seees: a8

Define Search

Orurran vy

Make. - 6. 1 we Model

Year. 2 2 ee New/Used Code
Unit Status .... Product Code .
Color Code... . . Serial Number
Location. ..... Division Code
Description .... Rental Status
Horsepower Range .

 


X2-1 INQUIRE/UPDATE UNITS

The next screen illustrates the result of the search. Note that the division is
now "B- Dealer Sales & Service."

B-DEALER SALES & SERVIC INQUIRE/UPDATE UNITS 11/13/97
X21001 Unit Prod N

Number Cd Make Model Description Color U Le Serial Number
FES778 FORD S~-MISC MO

FES330 FORD 105-2 I-ROTAVATOR MO 1154

FE5788 FORD 770-4 M-LOADER MO 17732

FES438 FORD 770-5 M-LOADER MO 16438

FES475 FORD 771-1 M-LOADER MO 19386

PES739 FORD 781-2 L-BLADES MO 4300

PES751 FORD 782-3 L-BLADES MO 19999


rrr pry pa

Cmd1-End Cmdl-End Cmd3-Restart Home-Top of list Roll-Page
= Seseeee serscsess:
Define Search

Make...) 1 ww. Model .
Year. 2. ee New/Used Code
Unit Status .... Product Code .
Color Code. .... Serial Number
Location. ..... Division Code
Description .... Rental Status
Horsepower Range .

 

UNITS


[=| X2-1 INQUIRE/UPDATE UNITS Cc

### Inquire Unit

Use Inquire Unit when you want to look at (without changing) information
pertaining to one or more units. If you know the stock number of one unit,
you can request it directly without a search. Or, you can begin by defining
a search to restrict the display to the units you are interested in. Then you
can access the unit you want by its item number on the list or by its stock
number.

No security code is required at the security gate. From the Options screen
(Cmd3-Restart), select option 2, Inquire Unit. The Unit Information screen

and the Information Options appear. The fields on the Unit Information

screen the information options are exactly the same as what you'll see

when you choose option 3, Update Unit, or option 4, Add Unit. See the (
section "Add Unit."

### Update Unit

Use Update Unit when you want to change information on units that are
already in the system. If you know the stock number of one unit, you can
request it directly without a search. Or, you can begin by defining a search
to restrict the display to the units you are interested in. Then you can
access the unit you want by its item number on the list or by its stock
number.

Use the units password at the security gate. From the Options screen

(Cmd3-Restart), select option 3, Update Unit. The Unit Information screen
and the Information Options appear. The fields on the Unit Information

é
RELEASE 2.2 KL


X2-1 INQUIRE/UPDATE UNITS [3]

screen the information options are exactly the same as what you'll see
when you choose option 2, Inquire Unit, or option 4, Add Unit. See the
section "Add Unit."

ADD UNIT (Inquire/Update/Add)

Use Add Unit to add new units to inventory. To add or change
information, the units password is required at the security gate. The fields
and options are exactly the same as what you see when you choose option
2, Inquire/Update Units, or option 3, Update Unit. Because of the
similarity, all 3 options are discussed in this section.

Begin at the Options screen (Cmd3-Restart). Look closely at the last 2
lines on the screen. Besides the option number, 3 other fields are available:
item number, unit number, and serial number. The fields are described
following the screen.

UNITS


14 | X2-1 INQUIRE/UPDATE UNITS

A-A&R EQUIPMENT SALES
Unit Prod
## Number Cd Make

Cmd1-End

Cmd3-Restart

- Define Search
. Inquire Unit
. Update Unit

- Add unit

- Delete Unit

Enter option number:

item number:

Fields & Screens

Enter option number

item number

or unit number

ox unit number:
DIS-2059 Roll to display units.

 

INQUIRE/UPDATE UNITS 10/15/97 X21001

Yr Description Color U Le Serial Number st

Home-Top of list
Soneenesseeseese ees!

Options

Roll-Page

. Transfer Unit

» Print Unit

- Print Report of Selected Units

. Display Summary of Selected Units

or serial number: (

1 digit. Required. Use "2" if you want to
inquire only. Use "3" to update units already
in the system. Use "4" to add new units to
the system.

1 digit. Get this number from the column
labeled "#." For Inquire and Update, use
one of the numbers: item, unit, or serial.
There is no item number when you are
adding new units.

6 characters. The stock number you assigned

{

RELEASE 2.2 Ne


X2-1 INQUIRE/UPDATE UNITS [5]

to the unit. For Inquire and Update, use one
of the numbers: item, unit, or serial. You can
enter the new stock number when you are
adding, but it is not required.

or serial number 17 characters. For Inquire and Update, use
one of the numbers: item, unit, or serial.

After you have selected an option and entered one of the numbers (if
appropriate), press [Enter]. The Unit Information screen appears with the
Information Options. The Information Options are presented in numerical
order.

UNITS


16 | X2-1 INQUIRE/UPDATE UNITS va

1. Unit Information

The Unit Information screen is illustrated below.

A-AGR EQUIPMENT SALES INQUIRE/UPDATE UNITS 11/04/97 X21001
Inquire Unit Information

Unit Number/Status . BH1000 / S Location... .. . ¥0
Description .. . . O-BACKHOE In Date/Warr Code. . 50184 /
Make... .... . CASE wee 18231.84
Model ...... , 440 Original Cost.

Flooring Due Date . 5/01/86 Added Cost

Year / Color Code . 00 / Flooring Amount . . 18216.00
Sold-by ..... Suggested List . . .

Horsepower/Prod Code __ / __ Discount Pct . +
New/Used Code .. . Dealer List ... . 4400000

Serial Number . . . 266899F423 G/L Account .. . . A1l620

Engine Number .. . Traded On Unit . .

Cmdl-End Cmd2-Open W/O Cmd3-Restart Home-Top/List Roll-Page

= Seeeeescscesss seeeeeesnccs (

Information Options
1. Unit Information 4. Specification Information
2. Unit Transactions 5. Rental Information

3. Flooring Transactions 6. Fixed Asset Information

Enter option number:

 

Inquire/Update Unit
To update information on this screen, press [Enter]. The following
message is displayed: "Unit has been updated."

If you used an item number on Inquire/Update, you can roll down or press
[PgDn] to see the next unit. Roll up or press [PgUp] to see the previous
unit.

{
RELEASE 2.2 LU


UNITS

X2-1 INQUIRE/UPDATE UNITS

 

TIP
To inquire/update another unit without rolling, enter its unit number,
then backspace twice to the field labeled "Enter option number" at the
bottom of the screen. Select option 1 and press [Enter]. Information for
the unit requested is displayed.
ES

Only units in the division selected at the security gate can be updated. To
change divisions, Cmd1-End to return to the Units Menu. Re-enter with
the new division and security codes.

Add Unit
To add the first unit, press [Enter]. The following message is displayed:
"Unit has been added. Press Roll key to add another unit."

If you want to add another unit, roll down or press [PgDn]. Information
from the previously added unit is redisplayed at the next Add screen
except for items that are unique to any unit, such as stock number. This
feature makes it easy to add several similar units at one time.


X2-1 INQUIRE/UPDATE UNITS

### Fields & Descriptions

The fields on the Unit Information screen are described below.

Unit Number

Description

Make
Model

Year

Color Code

Horsepower
Product Code

New/Used Code
Serial Number

Engine Number

6 characters. User-defined unit identification
number.

12 characters. Recommended. Brief
description of unit; for example, LOADER.
The Sales Price Book sorts in order by this
description. Unlimited lines of specifications
can be entered by using Information Option
3, Specification Information.

9 characters. Required. Name of (
manufacturer.

9 characters. Required. Manufacturer's
model type.

2.0 digits. Optional. Use the last 2 digits of
the year the unit was manufactured, for
example, 1991 = 91.

5 characters. Optional. User-defined. Not
used by the system except for searches.

3.0 digits. Optional. Horsepower of unit.

2 characters. Optional. User- defined. Not
used by the system.

1 character. Optional. N = New, U = Used.
17 characters. Optional. Serial number
assigned by the manufacturer.

12 characters. Optional. Engine number
assigned by the manufacturer.

RELEASE 2.2 Vo


UNITS

Location

Warranty Code

Cost

Suggested List

Discount Pct

Dealer List

X2-1 INQUIRE/UPDATE UNITS

2 characters. Optional. User- defined code
indicating the physical location of the unit.
In DateDate (mm/dd/yy). Required. Date the
unit was received into inventory. Defaults to
current date.

1.0 digits. Required. Valid digits are 1-9
only. User-defined code indicating the type
of warranty that applies to the unit.
Suggested warranty codes are:

1=1 year

2 =2 years

3 = 30 days

4=

5 = 50/50 used warranty

6 = 60 days

7 = No warranty - as it is, where it is
8 = Special

9 = 90 days

9.2 digits. Cannot be entered or changed in
Inquire/Update Units. Cost of the unit
(999999999) is posted in Create Source
Documents only.

9.2 digits. Optional. Manufacturer's
suggested list price (9999999.99).

2.1 digits. Optional. Discount percentage
allowed on the sale, such as 7 1/2 % = 075.
Must be a positive number.

9.2 digits. Recommended. List price used by
Sales (9999999.99). Must be a positive
number.


X2-1 INQUIRE/UPDATE UNITS

G/L Account

Trade-On Unit

Unit Status

8 characters. Required. General Ledger units
inventory account number. For company
vehicles which have been set up as fixed
assets, this G/L account may be an expense
account with an edit code = "C".

6 characters. The stock number of the unit
that was sold when this unit was traded in.

1 character. System-assigned. Status of unit.
Status codes are:

S=Sold

A = Available For Sale

R = Rental Unit (established by Rental Start
Date)

F= Fixed Asset Unit (established by Start
Date on the Fixed Assets Information
screen)

T = Transferred Units

Note:

Units that are both rentals and fixed assets are assigned status "R."

 


UNITS

2. Transaction Information

X2-1 INQUIRE/UPDATE UNITS

From the Information Options screen, select option 2, Transaction
Information. Transactions from Create Source Documents and Point of
Sale that pertain to the current unit are displayed. No additions or changes

can be made on this screen.

A~A&R EQUIPMENT SALES
Inquire

1 BH1O000 CASE 440

Mth ID Date Invoice #
May P 5/01/86 ES00512

--> Sold To: LEROY GRADY
Jan 1/20/86 Iv00009 #* RE
Jan 1/20/86 IVO0009 #* RE
Jan 1/20/86 IV00009 #* RE
Jan 1/20/86 TROOO4
May 5/01/86 ES00512
May 5/01/86 ES00S12

INQUIRE/UPDATE UNITS

11/04/97 = X21001

Unit Transactions

00 O-BACKHOE

Description D/C G/L Acct
440 BACKHOE C

440 BACKHOE

D
Cc
Cc
BACKHOE D
D
440 BACKHOE C¢

Cmdl-End Cmd2-Open W/O Cmd3-Restart

Information

1. Unit Information
2. Unit Transactions
3. Flooring Transactions

Enter option number:

YO 266899F423 s

Amount Type Addr # Code
A290 29995.00 S  GRADO1 s
Warranty Code: 1 Expires: 9/01/86
4280 1s. FLOYO1
33280 39. FLOYO1
Ai620 15. FLOYO2
A1620 18216.
A4290 18231.
AlL620 18231. 84-
Home-Top of list Roll-Page

GRADO1

Options

. Specification Information
. Rental Information
. Fixed Asset Information


[2] X2-1 INQUIRE/UPDATE UNITS

### Fields & Descriptions

Fields on the Transaction Information screen are described below.

MTH

ID

Date
Invoice
Description

D/C

G/L Acct
Amount

Type

Addr#

Code

The month in which the transaction occurred; for
example, JAN, FEB, MAR.
ID from Create Source Documents. Automatic
transactions are marked with an asterisk (*).
The date of the transaction (mm/dd/yy).
#Invoice number.
Description of the transaction.
Type of General Ledger transaction. D = Debit; C =
Credit.
General Ledger account number.
Amount of General Ledger transaction.
Type of transaction. The edit code of the G/L
Account.

C = Cost of Rental

R = Rental Revenue

W = Units Inventory/Cost of Sales
Address number of the customer who purchased the
unit.
See Type field.
NU


UNITS

X2-1 INQUIRE/UPDATE UNITS

3. Flooring Transactions

Select option 3, Flooring Transactions, to display the transactions posted
to flooring accounts (edit code = F) for the current unit.

 
  

  

  

A-LEE'S RENTAL COMPANY INQUIRE/UPDATE UNITS 11/04/97 = -X21001
Inquire Flooring Transactions

       
 
  

    

     

1 BHIO00 CASE 440

  

### 00 O-Backhoe Yo 266899F423

      
   
  

 

     

  

Mth ID Date Invoice # Description D/C G/L Acct Amount Type Addr #
Jan J 1/20/86 TROOO4 BACKHOE Cc A2260 18216 .00 CASEQ
Nov 11/04/97 666 Check X12-7 D A2260 18216 .00-

eode

   

     

    
  

 

  

Cmd1-End Cmd2-Open W/O Cmd3-Restart Home-Top of list Roll-Page

 
 

   

Information Options

 
 
  

    
 

- Unit Information . Specification Information

   

2. Unit Transactions 5S. Rental Information

       

3. Flooring Transactions 6. Fixed Asset Information

    
   
 

Enter option number:

The last character of each transaction to shows either a "C” for current or
an "H" for history.


24 | X2-1 INQUIRE/UPDATE UNITS

4. Specification Information

From the Information Options screen, select option 4, Specification
Information. The Specification Information screen appears.

A-AUSTIN TRACTOR & EQUI INQUIRE/UPDATE UNITS 11/13/97 X21001
Update Specification Information


7 FTS539 FORD 00 A-TRACTOR LO C616601

Specifications
26" X 48" bucket, enclosed cab, heater, AM/FM stereo

Cmd3-Restart Kome-Top of list Roll-Page

Information Options

- Unit Information 4. Specification Information
. Transaction Information 5. Rental Information
3. Flooring Transactions 6. Fixed Asset Information

Enter option number:

 

Each screen holds 8 lines of specifications. Press [Enter] to add/update the
information and go to the next screen. Use all the lines you need. There is
no limit to the number of specification lines that can be attached to one
unit.


RELEASE 2.2 Qe


X2-1 INQUIRE/UPDATE UNITS

5. Rental Information

From the Information Options screen, select option 5, Rental Information.
The Rental/Leasing Information screen appears.

 

A PACIFIC NORTHWEST REN INQUIRE/UPDATE UNITS 09/24/93 %21002

Update Rental/Leasing Information
5

 

## BUO1OO SCOOPKING 390C 92 BUCKET

Current Rental Status: “*

Rental Start Date . . 61592 Rental Revenue

New Rental Status . . __ Rental Cost .

Meter. ...... . 999999 Fuel Type..........
Unit Class. .....w20—s Fuel Capacity. .......
Replacement Value (2) Non-Serialized Quantity .
Damage Waiver (Y/N) . N Attachment (Y/N).

cmd1-End Cmd3-Restart Roll-Page

Information Options t
1. Unit Information 4, Specification Information
2. Transaction Information 5. Rental Information

3. Flooring Transactions 6. Fixed Asset Information

Enter option number:

 

### Fields & Descriptions

The fields on the Rental Information screen are described below.

Current Rental Status Valid rental status codes are:

UNITS


X2-1 INQUIRE/UPDATE UNITS

Rental Start Date
New Rental Status
Meter

Rental Revenue

4£— Rental Cost

nga
eo

AV = Available

DE = Demo

LS = Light Service

MS = Major Service

RE = Rented

SO = Sold

WD = Waiting for Delivery

WL = Waiting for Light Service

WM = Waiting for Major Service

WP = Waiting for Pickup
Date (mm/dd/yy). This date establishes the
unit as a Rental/Leasing unit, and changes
the type code to "R."
2 characters. See the rental status codes
listed above. Rental Status cannot be
changed to the null category.
7.1 digits. Current or most recent meter
reading.
Cannot be changed in Inquire/Update Units.
Dollar amount of revenue posted to this unit
through Create Source Documents (X1-7) or
Point of Sale (X5-1).
Cannot be changed in Inquire/Update Units.
Dollar amount of cost posted to this unit
through Create Source Documents (X1-7) or
Point of Sale (X5-1).

?
4 The following fields are available if you have Advanced Rentals:

Fuel Type
Unit Class

8 characters. Optional.
10 characters. Must be a valid class as set up
in Work with Rates (X9-5).


UNITS

Fuel Capacity
Replacement Value
Non-serialized Quantity

Damage Waiver?
Attachment?

X2-1 INQUIRE/UPDATE UNITS

3 digits. Optional.

7.2 digits. Example: 1234567.12.

3 digits. Defaults to zero. If there is no serial
number, this quantity can be any number. A
non-zero number is required here to rent
more than | unit on the same line. If there is
a serial number, the system automatically
furnishes a quantity of one.

Y/N. Required.

Y/N. Defaults to "N." "Y" means the unit is
an attachment. It cannot have its own
attachments in Work with Rentals (X9-1).


28 | X2-1 INQUIRE/UPDATE UNITS

6. Fixed Asset Information

From the Information Options screen, select option 6, Fixed Asset
Information. The Fixed Asset Information screen appears. An example of
a fixed asset set up for ACRS depreciation is illustrated.

A-AUSTIN TRACTOR & EQUI INQUIRE/UPDATE UNITS 11/13/97 =x21001
Update Fixed Asset Information 6

7 FT5539 FORD TW10 00 A-TRACTOR LO C616601 A

Start Date Starting Cost ... 1300000

Method Invest Credit

Life... Past Depr .....

Vehicle Flag.... Frst Yr/179 Depr . . {
Expense Account . . Current Depr..- .

Contra Account . . . Salvage

Unit Cost . . Total Depr. . Book Value . .

Cmd3-Restart Home-Top of list Roll-Page

Information Options
1. Unit Information . Specification Information
2. Transaction Information . Rental Information

3. Flooring Transactions . Fixed Asset Information

Enter option number:

 

Fixed assets can be set up to depreciate automatically when Accounting
End of Month (X1-10) is run. The program looks at the Start Date for
depreciation. If necessary, Starting Cost of the fixed asset is adjusted for
past and current depreciation.

RELEASE 2.2 Xen


X2-1 INQUIRE/UPDATE UNITS

The adjusted cost is used for depreciation calculations based on the
depreciation method. The amount is divided by 12 to figure the
depreciation to be debited to the Expense Account number entered and
credited to the Contra Asset Account entered when Accounting End of
Month is run. This Contra Asset Account (accrued depreciation) must be
set up with a 'X’ edit code in General Ledger Maintenance (X14-2).

### Fields & Descriptions

The fields on the Fixed Asset Information screen are described below.

Start Date Date (mm/dd/yy). Date on which unit
becomes a fixed asset and depreciation
begins.

Note:
Entering a Start Date causes the status to change from A = Available to

| F = Fixed Asset. A Fixed Asset which is also a Rental is assigned
| status = R.

 

Method 3 characters. Depreciation method.
ACR = ACRS (Accelerated Cost Recovery
Syst em) Depreciation calculations for
ACRS on units placed into service before
12/31/86 are different than for units placed
into service after that date.

UNITS


X2-1 INQUIRE/UPDATE UNITS

Life

Vehicle Flag

Expense Account

Contra Account

SLN = Straight Line

MAN = Manual. No depreciation is
calculated by the system. Debits and credits
for depreciation must be posted in Create
Source Documents (X1-7).

3 digits = Declining Balance. Example: 200
= 200%.

3.0 digits. Life of the unit in years (99.9).
Must be a positive number.

1 character. Y = Yes, N = No. "Y" indicates
that the fixed asset is a vehicle. Used in
figuring depreciation on vehicles with a
Start Date greater than 12/31/86.

When the system encounters a "Y" in this
field, NEW ACRS is examined. There is a
yearly ceiling on depreciation on vehicles
defined as Luxury Vehicles by the IRS. The
Life for Luxury Vehicles must be 5 years.
Depreciation may extend beyond 5 years.
Depreciation will be calculated until the
depreciation amount equals the starting cost.
8 characters. General Ledger account
number debited for depreciation expense on
the unit.

8 characters. General Ledger account
credited for the depreciation charged to
units. This account must have an edit code
of "X."
—


X2-1 INQUIRE/UPDATE UNITS [>|

Starting Cost 9.2 digits. The original cost of the unit prior
to depreciation (9999999.99). Must be a
positive number.

Invest Credit 9.2 digits. Amount of investment credit
claimed. This field is not valid if Start Date
is greater than December 31, 1986.

Past Depr 9.2 digits. Amount of depreciation taken in
previous years. Should not include the
depreciation to be in the Frst Yr/179 Depr
field.

Frst Y1/179 Depr 9.2 digits. Amount of depreciation taken on
this unit during its first year. If you are using
ACRS for units in service before 12/31/86,
the amount of depreciation depends on when
the vehicle is placed in service. See section
179 of the IRS code. For example: 1983 - 87
Cannot be over 5,000.00 1988 - 89 Cannot
be over 7,500.00 1990/over Cannot be over
10,000.00 If you are using ACRS for units
placed in service later than 12/31/86, the
field is not valid unless your business is less
than one year old.

Current Depr 9.2 digits. Amount of depreciation taken in
the current year. Example: If it is June,
enter the amount of depreciation for January
through May. June's depreciation would be
calculated when Accounting End of Month
is run.

Salvage 9.2 digits. The dollar value of the unit when
it is fully depreciated.

UNITS


[=| X2-1 INQUIRE/UPDATE UNITS

Unit Cost

Total Depr

Book Value

DELETE UNIT

9.2 digits. Current cost of the unit (current).
Cannot be entered or changed in
Inquire/Update Units. Cost of the unit
(9999999.99) is posted in Create Source
Documents only.

System-generated. Total amount of
depreciation to date. Total of past and
current depreciation.

9.2 digits. System-generated. Book value of
the unit. Total Depreciation subtracted from
Unit Cost.

From the Options Screen, select option 5, Delete Unit. Type the item
number, unit number or serial number. Press [Enter]. The unit is displayed
on the Unit Information Screen with a message asking if you want to
delete this unit. Press [Cmd1] to cancel the request, or press [Enter] to

delete the unit.

Note:

Units cannot be deleted unless their cost is zero. Cost may be changed
in Create Source Documents.

 
LL


X2-1 INQUIRE/UPDATE UNITS

### Print Unit

Print Unit and Print Report for Selected Units work the same way. The
only difference is you begin Print Unit by using an item number, a unit
number, or a serial number to request information about a single unit.

From the Options Screen, select option 7, Print Unit. Type the item
number, unit number, or serial number. Press [Enter]. The Print Options
Screen appears. The print options are described in the next section, Print
Report of Selected Units.

An example of a report with transactions for Unit BH1000 follows.

A&R EQUIPMENT SALES INQUIRE / UPDATE UNITS Date 9/24/97 Page 1
LYNDEN, WA Selected Units Report Time 11.08.47 x2100-4a

Sug List Dir lise

Unit Make PC Color Loc Engine # cost
s YO 16,232.84 44,000.00

### Bh1600 Case 440

Serial # Description Indate Warr Trade G/L Acct Disc
2668997423 O-BACKEOE, 0$/01/84 A1620
--Sale Information--
Sold To Date Document # Sold by Sold for Gr Profit Margin & Warr Date Warr
LEROY GRADY $/G1/86 ESOOS12 29995.00  11763.16 39.22 8 9/01/86 = 1
=-Rental Information--
Start Dt Revenue Cost Rental Status Meter Class Fuel Type Capacity N/S Qty Dam Wr Attachment Repl value
1/10/86 39.60 15.84 ™ N N
+2-Unit Trans-~
Month ID Date Invoice # Description
RE

G/L Acct Amount Type Addr # Code
Jan * 1/20/86 TVO000S #* too

A4280 15.84 C FLOYO
Subtotal

Subtotal
Jan 1/20/86 Iv00009 #* RE

Jan 1/20/86 ‘TROOOS BACKHOE
May 5/01/86 £S00512 440 BACKHOE
May $/01/86 ES00512 440 BACKHOE

A1629 15, FLOYO1
A1620 18216,
Ad290 28232. GRADOL
A1620 16233.

pe

Jan 1/20/86 Tv00009 #* RE Cc A3280 39, FLOYOL
c
D
D

Subtotal 8200.16
-Flooring Trans-
Jan J 1/20/86 ‘TROOOS BACKHOE Cc A2260 16226. CASEO2
Subtotal 18216.00
--Washout Tree--
Unit = Make Model Description In Days Sale De Sold for Cost Margin $ Trade washout Tree
BHI000 CASE O-BACKHOE, 730° 5/01/86 = 29995.00 18:

 

UNITS


X2-1 INQUIRE/UPDATE UNITS a
(

### Print Report Of Selected Units

Before selecting this option, define a search for the units you want. If a
search is not defined, all units in inventory will be summarized printed.

Example:

A customer buys 3 units and trades in one unit. If the color code field is

not being used, use it in this case to tie these 4 units together. Enter the

same 5 characters in the color code of each of the 4 units. You might

choose the last 5 characters of the invoice number which recorded the

transaction. Then define a search on the color code. The 4 units are

displayed. Now you can print a report which will show all of the costs (
related to this deal.

From the Options Screen select option 8 to Print Report of Selected Units.
The Print Options Screen is displayed.

RELEASE 2.2 CO


X2-1 INQUIRE/UPDATE UNITS

A-A&R EQUIPMENT SALES INQUIRE/UPDATE UNITS 10/15/97 X21001
Unit Prod N
Number Cd Make Model Yr Description Color U Le Serial Number st
BH1000 CASE 440 00 O-BACKHOE YO 266899F423
BU3010 THOR 7700 95 BUCKET STONE LY 898565639
BU3020 THOR 7700 35 BUCKET STONE LY 9903020
BU3030 THOR 7700 95 BUCKET STONE LY 9903030
BU3040 THOR 7700 95 BUCKET STONE LY 9903040
BU3050 THOR 7700 95 BUCKET STONE LY 9903050
BU3060 THOR 7700 95 BUCKET STONE LY 9903060
BU3070 THOR 7700 95 BUCKET STONE OY 9903070
cCmdl-End Cmd3-Restart Home-Top of list Roll-Page
senesss See eeaSesssse=sesscss:

Print Options

i i i i )

Print Unit Trans? (Y/N)... Printer ID .
Print summary only? (Y/N). . Forms Number . woe ee
Print Flooring Trans? (Y/N). . Priority (0-hold/l to 5)... *
Print unit list only? (Y/N). . Lines per Page (1 to 112)

Lines per Inch (4/6/8)

Chars per Inch (10/15)... . r

Number of Copies (1 to 99) . .

  

If the fields are left blank, the print options default to those set for your
workstation. If you have no reason to change the defaults, press [Enter].
The report is printed.

   

   

Note:
Subtotals are calculated for each Make and/or Model of the selected

unit(s).

UNITS


X2-1 INQUIRE/UPDATE UNITS

Print Options

The print options for Print Unit and Print Report of Selected Units are

described below.

Print Unit Trans? (Y/N)
Print summary only? (Y/N)
Print Flooring Trans? (Y/N)

Print unit list only? (Y/N)

Printer ID

Forms Number
Print Priority

Lines Per Page
Lines Per Inch
Characters Per Inch

Number of Copies

Y = Yes, print detail transactions for the
unit. N = No, do not print transactions. The
default is Y.

Y = Print summary only. N = Print detail
and summary. The default is N.

Y = Yes, print flooring transactions. N = No,
do not print transaction. The default is Y.

Y = Yes, print a list of units and Unit (
Information. If ‘Y’ is entered on this report,
all other report options will be ignored and
only this one will print out. N = No, do not
print a list of units. The default is N.

2 characters. Identifying number of the
printer where the report is to be printed.

4 characters. Number identifying form used.
1 digit. Valid numbers are 0 - 5. Priority = 0
will place the print on hold.

3.0 digits. Valid numbers are 1 - 112.
Maximum number of lines per page.

1.0 digits. Number of lines per inch. Valid
numbers are 4, 6, and 8.

2.0 digits. Number of characters per inch.
Valid numbers are 10 and 15.

2.0 digits. Number of copies to be printed.
Valid numbers are i - 99.
ye


A&R EQUIPMENT SALES

LYNDEN, WA

Make/Model:

“* Make:

Make/Model:

Make/Model:

INQUIRE / UPDATE UNITS
Selected Units Report

: units Cost
‘THOR 7700

New Units .

Used Units

Rental Units fe

Non-rental Fixed Assets .
Totel Units Available for Sale .

Total Units Sold or Transferred

THOR
New Units .
Used Units
Rental Units ......
Non-rental Fixed Assets .
Total Units Available for Sale .

Total Units Sold or Transferred

Woops MPC
New Units...
Used Units ........
Rental Units .......
Non-rental Fixed Assets .
Total Units Available for sale .

Total Units Sold or Transferred

woops usec
New Units .
Used Units
Rental Units bee
Non-rental Fixed Assets . .
Total Units Available for Sale .

Total Units Sold or Transferred

woops
New Units .
Used Units
Rental Units Le
Non-rental Fixed Assets .
Total Units Available for Sale .

Total Units Sold or Transferred

Report Totals

UNITS

New Units .
Used Units
Rental Units tee
Non-rental Fixed Assets . .
Total Units Available for Sale .

90,924,
10,000.
103,198.

204,123.

Total Units Sold or Transferred

An example of a report without transactions is illustrated.

X2-1 INQUIRE/UPDATE UNITS

Date 11/04/97
Time 11.49.28

Page 10
X2100-SA

Sale
Amount.

%
Margin

Gross
Profit

Dealer
List

1,805.00

1,805.00

227,573.50
20,412.00
131,709.90

379,694.50
154,268.00

40,398.68 26.19


X2-1 INQUIRE/UPDATE UNITS

An example of a Unit List follows.

AER EQUIPMENT SALES
LYNDEN, WA A
Options: make...

Product Code
unit Product

INQUIRE/UPDATE UNITS
Unit List
Model. . Year
Color code Sert

New/Used
Location

Date 10/15/37
Time 11.41.56
Unit Status

Division . A

Page 1
¥2100-601

 

BH1000
TRLOOG
‘TR2000
CREVO1
UNIT?73

CASE 440 00
CASE S86C 00
CASE s80c 86
CHEV C65 79
CORVETTE HOT ce
LGT125, 76

O-BACKHOE,
O-BACKHOE
O-BACKHOE
TRUCK

73 VETTE
RIDING MOWER

FE2228 FORD
UTSS76 FORD TLB 00 TLE

FTSssi9 FORD TWIG 00
FTS8S1 FORD TW1O 00
101 FORD 101 97
PTS768 FORD 1500 00
FTS492 FORD 1700 00
UTS5334 FORD 5000 00

A-TRACTOR
A-TRACTOR
UNIT 161
A-TRACTOR
A-TRACTOR
A-TRAC-FORD
F3=Exit  Fl2-Cancel F29=Left

F20-Right F24=More keys

266899F423
AGS4RESE4L
266589F245
CCEESOV137810
NIJW1950
16063
765444
6166021
639362
101
U502617
700982
OT6949

 


UNITS

 

X2-1 INQUIRE/UPDATE UNITS 39 |

### Display Summary Of Selected Units

Before selecting this option, define a search for the units you want. If a
search is not defined, all units in inventory will be summarized and
displayed.

From the Options Screen, select option 9, Display Summary of Selected
Units. The message "Summary is being calculated" appears, and the
summary of units selected at the Define Search option is displayed.

A-AUSTIN TRACTOR & EQUI INQUIRE/UPDATE UNITS 21/13/97 X21001

Unit Prod N

Number Cd Make Model Yr Description Color U Le Serial Number st

FT5539 FORD TW1O 00 A-TRACTOR LO C616601

FTS851 FORD TW10 00 A-TRACTOR MO C639362

FTO0002 TR FORD 97 A-TRACTOR BLUE N UB01273

FTS768 FORD 00 A-TRACTOR MO U502617

FT5492 FORD 00 A-TRACTOR MO 0700982

UTS439 FORD 00 A-TRACTOR LO C787666

FA0642 FORD 00 A-TRACTOR 30 C002468A

FAO781 FORD 00 A-TRACTOR 30 C621249A R

md1l-End cmd3-Restart Home~Top of list Roll-Page
Display Summary of Selected Units

Summary Totals Cost Sugg List Dir List

72,409.39 7,529.00 151,186.50

Rental 18,425.00 45,897.00
Fixed Assets...

Available 90,834.39 7,529.00 197,083.50

Sold/Transferred . . 51,500.28 59,643.00

DIS-0026 Press Enter to continue.


X2-1 INQUIRE/UPDATE UNITS

Press [Enter] to return to the Define Search screen.

### Fields & Descriptions

The fields on the summary are described below:

Summary Totals
Units
Cost
Sugg List
Dir List
New

Used

Rental

Fixed Assets

Available

Sold/Transferred

Total number of selected units in summary.
Total cost of summary of selected units.
Total suggested list price of summary of
selected units.

Total dealer list price of summary of
selected units.

Summary of selected new units based on
New/Used code = "N."

Summary of selected used units based on
New/Used code = "U."

Summary of selected rental units, based on
presence of a Rental Start Date and Unit
Status of "R."

Summary of selected fixed asset units based
on the presence of a Start Date and Unit
Status of "F."

Summary of selected units available for sale
based on Unit Status of "A."

Summary of sold selected units and
transferred selected units. Based on Unit
Status = "S" and/or "T".

## CHAPTER X2-3

SOLD UNITS INQUIRY

### Introduction

Sold Units Inquiry provides:
= ascreen display of any customer's unit purchase record.

### How To Run

From Menu Name: Type in: Press:
Sold Units Inquiry Customer
Address # or
Customer
Name ENTER
RESULT:

If a customer name was entered, the Sold Units Inquiry screen
(X2300-301) will appear.

## X2-3 SOLD UNITS INQUIRY

Below is a sample of the Sold Units Inquiry screen:

ABC COMPANY

Division:

Address #

SOLD UNITS INQUIRY

ADAMS, WILLIAM
GRADY, LEROY
LIGHTFOOT, CARL
MCINTOSH, ERNEST
MEYER, THAD

MUDD, JASON
PICKLEHOUSE, PAUL
SERENE VALLEY FARMS
SHAW PAPER SUPPLY
SMITH, DAVID
SWEDELIUS , STEVE
TEXAS NATURAL GAS
TEXAS PLUMBING
TWOSHOES ,, AMY
WHOEVER COMPANY

Press Cmdl to end job Cmd2 to reset

ADAMO1
650525
150840
MS1645
M00710
MUDDO1
PICKO1L
SEREO1L
SHAWO1
SMITOL
SWEDO1
TEXAOL
TEXA03
TWwOSOL
WHOEO1

### X2300-301

 

Move the cursor to the name you want and type in any character next to

that name.

The Sold Units Inquiry screen (X2300-101) will display the customer

information.

Ne


UNITS


Below is a sample of the Sold Units Inquiry screen:

ABC COMPANY SOLD UNITS INQUIRY %2300-301

Division: E

Address # ADAMO1

Name WILLIAM ADAMS (555) 111-1111
RT 1 BOX 999
ARLINGTON, WA 98223

Document Stock # Make Model Serial # Description
8/15/86 NEW1 RED CO. BIG €12345678 NEW UNIT 1
123456 Air conditioning, cab, 7 1/2 x 15 inch tires, radio

35618.00

8/15/86 NEW2 BLUE CO. SMALL F789456
123456 Radio, 7 x 14 inch tires
8768.75

9/23/86 NEW3 GREEN CO. MEDIUM %457812
45678
24300.00

Press CMD1 to end job

Warranty
8/15/87


[ «| X2-3 SOLD UNITS INQUIRY

### Fields & Descriptions

The fields found on the Sold Units Inquiry screen are described below in
the order in which they appear from left to right:

Customer
Message

Document

Stock #

Make
Model
Serial #
Description
Warranty
Specs

Name, address, and telephone number of
address number entered.

If no units have been sold to the customer,
the screen displays a message to that effect.
Date of sale document.

Document number.

Dollar amount of sale.

Number you assigned this unit item.

Specs on the item. (
Name of the manufacturer.

Manufacturer's model number.
Manufacturer's serial number for the unit.
Brief description of the unit.

Date warranty expires.

Up to two lines of specs appear to the right
of the invoice number and price.

Note:

If the customer has multiple purchases, they will be listed. If the
purchases are more than what will fit on one screen, you may roll the

 

next screen up by using the ROLL key.

f
RELEASE 2.1 \


X2-3 SOLD UNITS INQUIRY [=]

### Options

O Take a print of the screen by pressing the PRINT key.

C] Enter a new customer address number for Sold Units Inquiry, or press
FIELD EXIT to bypass address and enter portion of last name.

( Press CMD 1 to end the job and return to the Units Menu.

UNITS


Notes:

RELEASE 2.1 LO

## CHAPTER X2-4

RENTAL STATUS INQUIRY

### Introduction

Rental Status Inquiry allows you to select units by unit number, or by:
= make/model = year
® serial number ® location
= rental status code = description
= Address number from = six user-defined fields from Rental
Point of Sale Status Maintenance (X2-5)

or any combination of these items. The information displayed includes:

= unit # " serial number

= make * location

= model ™ product code

= year = hour meter

= description = current rental status & related
fields

The units are displayed in order by unit number. This job is for inquiry
only--no changes can be made to unit information, Status, or comments.

### How To Run

From the Units Menu (X2), select option 4, Rental Status Inquiry. The
Select Units screen appears.


[2 | X2-4 RENTAL STATUS INQUIRY os
(

Select Unit Screen

ABC COMPANY RENTAL STATUS INQUIRY X2400-101 1
Select Units
S044a3
or select a combination of the following:

Rental Status Code. .

Location . .
Serial number
Description

Address number... .

Cmdl-End job Enter-Continue

 

You may use the unit number or a combination of the other fields. Unit
number cannot be used in conjunction with any of the other fields. Make
and model must be requested together. You can use a partial serial
number; however, all other fields must be complete and exact matches.

The fields RnVLPO, Attch, ITEM, WarrEXp, PM pgm, YY/MM, are
examples of user defined fields which were created in Rental Status
Maintenance (X2-5). You can search on any combination of these fields,
as well as the Address number created in Point of Sale.

RELEASE 2.1 Ne


X2-4 RENTAL STATUS INQUIRY [=]

Type your request, and press [Enter] to continue. The first screen of units
matching your request is displayed on the Display Units screen.

The list of valid status codes follows:

Null Status **
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
[Enter] Completes your request for the units. The

system locates and displays the units.

UNITS

## X2-4 RENTAL STATUS INQUIRY

Display Units Screen

Unit information and comments are available. Unit information, which is
on the "left" side, is displayed first.

ABC COMPANY RENTAL STATUS INQUIRY X2400-102 2
Display Units

Unit# Make Model Description Serial# Le Yr PC Meter RS
5044Aa3 CASE D52642 CE-BUCKET RE

Cmdi-End job Cmd3-Reselect units Cmd4-Display comments Enter-page

 

To see the comments, which are on the right side, press [Cmd4]. The
Display Comments screen appears.

i
RELEASE 2.1 —


X2-4 RENTAL STATUS INQUIRY [=]

Display Comments Screen

ABC COMPANY RENTAL STATUS INQUIRY X2400-103 3
Display Comments

Unit# RS HEADER] HEADER2 HEADER3 HEADER4 HEADERS HEADER6 HEADER? HEADERSHEADER
$044A3 RE JAMES C 8/30/90 54321x

Cmdl-End job Cmd3-Reselect units Cmd4-Display units Enter-page

 

Press [Cmd4] again to return to unit information.

### Options

[Cmd1] End this job. Return to the Units Menu.

([Cmd3] Return to the selection screen.

[Cmd4} Shift screen to display comments. {Cmd4] is
a toggle which alternately displays the left
(unit information) and right side (comments)
of the list of units.

[Enter] See another screen of these units, if any.

UNITS


Notes:

## CHAPTER X2-5

RENTAL STATUS MAINTENANCE

### Introduction

Rental Status Maintenance allows you to change the status of a unit
quickly, and to add or change one or all of the comments. As you do so,
the system records the status code and date of change for history. Use
Rental Status Maintenance to establish headings for 9 comment fields.

At the time a unit is placed on the detail screen of a Point of Sale invoice,
you can press [Cmd1i1] for the Additional Options menu. Option 12 is
Rental Status Maintenance. The system "remembers" the unit most
recently put on the detail screen and uses it as the default. This is a quick
way to change Rental Status and Job Site on a timely basis.

## X2-5 RENTAL STATUS MAINTENANCE

 

### How To Run

From the Units Menu, select option 5, Rental Status Maintenance. The
Select Unit screen appears.

Select Unit Screen

ABC COMPANY RENTAL STATUS MAINTENANCE 2500-101 1
Select Unit

Unit#: 5044A3

Qmdi-End job Cmd9-Set field titles Enter-Continue

 

Type the Unit# and press [Enter]. The Change Unit screen appears.

### Options

(Cmd1] End this job. Return to the Units Menu.

[Cmd9] Establish or change titles for the 9 comment
fields associated with each unit.

[Enter] Completes your request for a unit. The

RELEASE 2.1 LO


 

system locates and displays the unit on the
Change Unit screen.

Change Unit Screen

ABC COMPANY RENTAL STATUS MAINTENANCE X2500-102 2
Change Unit

Unit#: 5044A3 8/27/90 AV Available
Status YTD % LID &

2.1 5
New Status Information: 97.9 639

Status code RE 100

HEADERL JAMES C 80
HEADER2

HEADER3

HEADERS 8/30/90

HEADERS

HEADER6

HEADER?

HEADERS 54321xx

HEADERS

Job Site BELLIS FAIR MALL

Cmai-End job Cmd3-Return without update Enter-Update new status

 

The current status of the unit is displayed at the top of the Change Unit
screen. The list of status codes and the unit's year-to-date (YTD) and
life-to-date (LTD) history are displayed. The system calculates and
displays the percentage of time the unit has been assigned to each status.

UNITS

### Warning!

The system records a change of status when you press [Enter]. It does

not check to see whether a change has actually been made. If you don't
want to record a change, press [Cmd3] to return to the selection screen
without an update.

 

The list of valid status codes follows:

Null Status

Available

Rented

Waiting for pickup
Waiting for light service
Waiting for major service
Light Service

Major Service

Sold

Demo

2h

AV

RE

WP (
WL

WM

LS

MS

sO

DE

Job Site is a 52-character field.

### Options

[Cmd1]
[Cmd3]

{Enter]

End this job. Return to the Units Menu.
Return to the selection screen without

. updating the unit's status or comments. The

system does not record a change on the Unit
Status Report.
Record a change in unit status, which will be

RELEASE 2.1 L.


 

noted on the Rental Status Report. The new
Status, if any, will be seen in Rental Status
Inquiry.

Set Field Titles Screen

There are 9 fields associated with each unit. Each field may contain up to
7 characters. These fields are displayed in Rental Status Inquiry. Comment
fields are available for your convenience. Dealers may use them for items
such as estimated in/out dates, insurance certificate numbers, etc.

To establish or change the titles you want to use, press [Cmd9] from the

Select Unit screen. The Set Field Titles screen appears, which is a list of
titles, 1-9.

UNITS


 

ABC COMPANY RENTAL STATUS MAINTENANCE X2500-103 3
Set Field Titles

Comment
Comment
Comment
Comment
Comment:
Comment
Comment
Comment
Comment

Cmdi-End job Enter-Continue

 

Type the titles you want to use. Press [Field Exit] to go to the next title.
When you are done, press [Enter] to enter them into the system. The Select
Unit screen reappears.

RELEASE 2.1 LL.

## CHAPTER X2-6

RENTAL STATUS HISTORY MAINTENANCE

### Introduction

Rental Status History Maintenance allows you to redistribute the rental
status history of a unit. Rental status history is updated by End of Day at
which time the system records the current rental status. Since history is
accumulated by days, you may occasionally want to redistribute history to
the status the unit held for most of the day. For example, if a unit was
returned in the last hour and its status was changed from REnted to
AVailable, the system records the entire day as A Vailable. Future reports
will be more accurate if its history reflects REnted for that day.

When you assign a Rental Start Date, the system calculates the number of
days to the current date and places the total in the null status.
Redistributing the days in the various categories will preserve some
history that would otherwise be lost.

## X2-6 RENTAL STATUS HISTORY MAINTENANCE

 

### How To Run

From the Units Menu (X2), select option 6, Rental Status History
Maintenance. The Select Unit screen appears.

Select Unit Screen

RENTAL STATUS HISTORY MAINTENANCE X2600-101 1
Select Unit

Unit#: 5044A3

Qmdl-End job Enter-Continue

 

Type the unit number, and press [Enter]. The Change Unit screen appears.

### Options

[Cmd1] End this job. Return to the Units Menu.
[Enter] Completes your request for a unit. The

system locates and displays the unit's status
history on the Change Unit screen.

f
RELEASE 2.1 Ne


 

Change Unit Screen - BEFORE

ABC COMPANY RENTAL STATUS HISTORY MAINTENANCE X2600-102 2
Change Unit

Unit#: 504403 8/30/90
Status YTD %

Null Status 5 2.1
Available 236 97.9

Waiting for pickup
Waiting for delivery

Waiting for light service .
Waiting for major service .
Light Service
Major Service

History Totals

Cmdl-End job Cmd3-Select new unit

 

To change the unit's status history, first [Field Exit] through the status you
are redistributing. Type the changes in the appropriate fields, and press
[Field Exit]. When you are done, press [Enter] to record your changes. If
the total number of days is less than the original total, the difference is
added to the Null Status, as illustrated on the next screen.

UNITS


 

If the total number of days is more than the original total, you will receive
an error message, and you will not be able to exit. When the total number
of hours is acceptable, you can press [Cmd3] to return to the Select Unit
screen reappears.

Change Unit Screen - AFTER

RENTAL STATUS HISTORY MAINTENANCE X2600-102 2
Change Unit

Unit#: 5044A3 8/30/90 RE Rented
Status

Null Status : : (
Available :

Waiting for pickup
Waiting for delivery

Waiting for light service .
Waiting for major service .
Light Service
Major Service

History Totals

Cmdl-En@ job Cmd3-Select new unit

 

t
{

RELEASE 2.1 Me


UNITS


 

The list of valid status codes follows:

Null Status **
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

[Cmd1} End this job. Return to the Units Menu.
[Cmd3] Return to the Select Unit screen.


Notes:

é

RELEASE 2.1 Ne

## CHAPTER X2-7

UNITS DEPRECIATION MENU

### Introduction

Depreciation is the loss in the value of property over the time the property
is being used. Depreciation can be caused by wear and tear, age,
deterioration, and obsolescence. You can recover the cost of certain
property, such as equipment you use in your business or property used for
the production of income, by taking deductions for depreciation.

There are a number of elements that any machine computation of
depreciation must have in order to be accurate and within the laws outlined
by the U.S. government. What follows is an examination of how these
elements should be handled, as described in IRS Publication 534, and how
they are actually handled by the DIS Business System.

### What Can Be Depreciated

Each piece of business property must be evaluated to determine whether it
is depreciable or not. For property to be depreciable, it must meet the
following basic requirements:

CO The property must be used in business or held to produce income.
O The property must have a determinable useful life longer than one year.

0 The property must be something that wears out, decays, gets used up,
becomes obsolete, or loses its value from natural causes.

If property does not meet all of the above requirements, it is not
depreciable. Land, for instance, although used in a business or held to
produce income, can never be depreciated because it does not wear out or
become obsolete. On the other hand, a vehicle that was purchased for use
in a business, does have a useful life of over a year, and yet also

## X2-7 UNITS DEPRECIATION MENU

 

becomes worn out and obsolete over an extended period of time, can be
depreciated.

Each business owner must evaluate whether property is depreciable or not
and if it is, it can be assigned a Unit# in the DIS system and set up as a
fixed asset. As long as certain elements are set up for that unit correctly,
the system will automatically run depreciation for it.

DEFINITIONS

Life

For a piece of property to be depreciable, there must be a period of time
during which it serves a useful purpose for your business. After this period
of time has passed, the property is no longer useful, is worn out, or is
obsolete. This period of time is known as the life of the property. It is only
during the life of the property that it may be depreciated. The DIS system
defines the life of a unit on the Fixed Asset Information screen in a field
labeled "Life." This field must be filled with the number of years that
equals the life of the depreciable unit.

Placed-in-Service Date

Depreciation begins on the date the property is placed in service for
business use. In order to determine what the life of a piece of property is,
this date must be defined. On the DIS system, the date that a unit is placed
in service is defined as the "Start Date" on the Fixed Asset Information
Screen.


 

Conventions

To figure depreciation deductions for a depreciable piece of property, a
convention must be used. A convention is a standard method, which is
used to determine the depreciation for the property in the first year that
property is placed in service. This is necessary because property is usually
placed in service for business use on some date during the year other than
January Ist. In other words, the first year that property is eligible for
depreciation is not necessarily a complete year. Because of this, three
different conventions have been established to prorate this first year of
depreciation. A business must choose one of the following three
conventions based on the type of property being depreciated:

1. The Half-Year Convention
This convention is generally used for property other than non-
residential real and residential rental property. Under the half-year
convention, property is treated as if it were placed in service at the
midpoint of the year. This means that no matter when in the year the
property was placed in service, it is treated as if it were placed in
service in the middle of the year. This is the most common convention.

2. The Mid-Month Convention
Under this convention, property is treated as if it were placed in service
at the midpoint of a month. This convention is used for non-residential
real property or residential rental property.

3. The Mid-Quarter Convention
This convention can apply to other than non-residential real property or
residential rental property in certain specific circumstances. Under this
convention, property is treated as if it were placed in service at the
midpoint of a quarter.

UNITS


 

The DIS system is set up to use the half-year convention when a unit is
depreciated using the ACRS method described in the next section. A
convention must also be used when calculating depreciation on a unit
using the straight line method or the declining balance method. The DIS
system currently does not use any convention for the latter two methods.
This change will need to be made to make our software correctly calculate
depreciation.

Method

The appropriate depreciation method depends on the type of property or

class each piece of property falls into. These classes are defined in detail in

the IRS depreciation publication. The DIS system defines a field on the

Fixed Asset Information screen labeled "Method." This field must be

filled in with the method of depreciation for each depreciable unit. The

methods that may be chosen are as follows: {

1. ACRS or MACRS Method
ACRS stands for the Accelerated Cost Recovery System. This method
is used for property placed in service before 1987. MACRS stands for
Modified Accelerated Cost Recovery System. This method is used for
property placed in service during or since 1987. On the DIS system this
method is chosen by filling in the method field with "ACR." The
system then determines whether to use the ACRS calculations or the
MACRS calculations based on the year portion of the start date.

2. Straight Line Method
The straight line method is chosen on the DIS system by filling in the
method field with "SLN.”

3) Declining Balance Method
The declining balance method is specified on the DIS system by filling
in the method field with three digits between 0 and 9. These three digits

i
RELEASE 2.1 QU


UNITS


 

are usually 200 or 150, which are defined as either the 200% declining
balance method or the 150% declining balance method.

Section 179 Deduction

As a business, if you purchase certain business property, you may be able
to recover all or part of its cost by taking a section 179 deduction. Section
179 of the Internal Revenue Code permits certain taxpayers to elect to
deduct all or part of the cost of certain qualifying property in the year that
property was placed in service, instead of taking depreciation deductions
over a specified recovery period. Certain costs that are not recovered by
the section 179 deduction can be recovered through depreciation with one
of the methods described above. The total cost of section 179 property that
you can elect to deduct for any year cannot be more than $10,000. You are
only allowed to deduct the actual amount paid for a piece of property in
cash. The section 179 deduction is purely elective and does not have to be
taken.

The DIS system defines the section 179 deduction on the Fixed Asset
Information screen as the 'Frst Yr/179 Depr' field. The section 179
deduction is not defined as actual depreciation. It is merely an optional
deduction that may be taken by a business on the cash paid for a piece of
property. This deduction must be taken during the first year the property is
placed in service. If the entire cost of the unit is not taken with the section
179 deduction, the remaining amount, including any additional value that
was added to the cost of the unit because of a trade-in, may be depreciated
through one of the methods described above.

Currently, the DIS system takes into account the section 179 deduction
when straight line, declining balance, or ACRS (units placed in service
before 1987) is used.


 

Basis

Basis is the original cost value placed on a piece of property when that
property is placed in service for business use. Basis includes any cash paid
for property plus the accumulated value of other pieces of property used as
trade when a depreciable property was purchased. Basis is the dollar
amount used to figure yearly depreciation that may be taken on a piece of
property. When calculating depreciation using any of the methods
described above, any section 179 deduction that was taken during the first
year the property was placed in service must first be subtracted from the
basis. The DIS system is set up to use the correct basis once a few changes
to the calculator have been made. The basis is described on the Fixed
Asset Information screen in the Starting Cost field.

Vehicle Limits {
In addition to the rules for all listed property, a passenger automobile is

also subject to other special limits. For passenger automobiles, the total
depreciation deduction (including the section 179 deduction) that can be

claimed is limited for each year. These yearly limits are different

depending upon what year a vehicle was placed in service and what year in

the life the depreciation is currently being calculated for. Each year the

limits for vehicles placed in service that year may change. These changes

are reflected the I-R.S. depreciation publication.

The DIS system has a field on the Fixed Asset Information screen called
Vehicle Flag. When a 'Y' is placed in this field, that unit will have its
yearly depreciation checked against the limits set up in the depreciation
calculator for MACRS depreciation. The only problem with the current
limits in the DIS calculator is that they only reflect the laws for vehicles
placed in service during 1986 through 1988. Since that time, there are a
different set of limits set up for each of the succeeding years. This part of
the DIS depreciation calculator will need to be updated.

RELEASE 2.1 LU


 

Add:
0 Sale of Assets
« Mid-year convention
= Accounting entries required

O Reporting for depreciation

= Audit trail (for internal use)
= Conformance & report format for IRS

UNITS


Notes:

RELEASE 2.1 Ne

## CHAPTER X2-9

CHANGE UNIT ACCOUNT#

### Introduction

Change Unit Account# makes it easy to transfer a unit from one general
ledger account to another. Units can also be transferred between divisions.
All transactions associated with the transfer proceed automatically:

1. Post Unit Cost: Credit Unit Account and Debit Holding Account.
2. Changes Unit Account Number.
3. Post Unit Cost: Credit Holding Account and Debit New Account.

Note:

To transfer a unit between divisions, a valid holding account must be
assigned for each division. Holding accounts are assigned in X6-6,
Security and Maintenance.


X2-9 CHANGE UNIT ACCOUNT#

### How To Run

From the Units Menu (X2), select option 9, Change Unit Account. The
following warning screen is displayed:

CHANGE UNIT ACCOUNT#

### + * *Warning***

This job may not be run while any other Accounting/Posting
Jobs are running. If any Accounting/Posting Jobs are running
press Cmdi to Cancel

This program performs the following functions:

1. Post Unit Cost: Credit Unit Account and Debit Holding Account.
2. Changes Unit Account Number.
3. Post Unit Cost: Credit Holding Account and Debit New Account.

Cmd1-Cancel Cmda2-Continue

 

C1 If you are sure there are no accounting or posting jobs running, press
[Cmd_2] to continue; otherwise, press [Cmd1] to cancel. The Change
Unit Account# screen appears.

X2-9 CHANGE UNIT ACCOUNT# |= |

List of Unit#s Screen

ABC-AG,AUTO,CONS & TRUCK CO. CHANGE UNIT ACCOUNT# X29001-01 1
Division: A
G/L Holding Account: A1800

Unit # From Acct # To Acct #
FES798

Cmd1-End@ Job Enter-Continue

 

O Key in the Unit #s of the units you want to transfer. When your list is
complete, press {Enter] to continue.

UNITS


[+] X2-9 CHANGE UNIT ACCOUNT# co ’

From Account to Account Screen

When you press [Enter] on the List of Unit#s screen, the system retrieves
the current account number and cost of each unit and displays them as
illustrated below.

ABC-AG,AUTO,CONS & TRUCK CO. CHANGE UNIT ACCOUNT# %29001-02 2
Division: A
G/L Holding Account: A1800

Unit # From Acct # Cost
FES798 A1240 1,837.00

Cmdl-End Job Cmd2-Previous Screen Enter-Continue

 

© Key in the account numbers you want to transfer each unit fo. When the
lists is complete, press [Enter]. The unit is transferred automatically.

RELEASE 2.1 LC


---