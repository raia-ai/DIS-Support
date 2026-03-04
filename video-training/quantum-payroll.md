---
title: "Quantum — Payroll"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — Payroll** module within the DIS (Dealer Information System) platform is a comprehensive solution designed to manage employee time tracking, payroll processing, and labor cost allocation for automotive dealerships. It integrates tig..."
long_description: "This document provides a comprehensive overview of the Quantum — Payroll module within the DIS platform, derived from internal training sessions."
---

# Quantum — Payroll

**Source Sessions**: 24, 33, 34, 35, 36

### Overview

The **Quantum — Payroll** module within the DIS (Dealer Information System) platform is a comprehensive solution designed to manage employee time tracking, payroll processing, and labor cost allocation for automotive dealerships. It integrates tightly with the **Time Clock** and **Service/Work Order** modules to ensure accurate labor tracking and billing, while the Payroll module handles employee setup, tax calculations, deductions, benefits, and general ledger (GL) accounting.

This module is critical for dealerships to maintain precise labor cost accounting, comply with tax regulations, and streamline payroll operations. By linking technician time punches directly to work orders and payroll records, Quantum Payroll provides real-time visibility into labor productivity and automates complex payroll calculations, including overtime, deductions, and employer contributions.

### Core Concepts

- **Time Clock Integration**: The Time Clock system records technician work hours and links them to service work orders for accurate labor billing. Time punches flow from the Time Clock to work orders, but manual labor entries on work orders do not update the Time Clock.

- **Technician View**: A specialized mode enabled by the `X00081` command that requires technicians to clock into specific work orders upon starting their shift. This provides service managers with a live dashboard of technician activity and job assignments.

- **Payroll Employee Setup**: Technicians and other employees must be configured in the Payroll module before using the Time Clock, even if payroll processing is handled externally. Employee records include department assignments, pay rates, tax information, and deduction/benefit codes.

- **Departmentalization**: Payroll expenses are allocated by department to enable detailed financial tracking. Departments are linked to GL accounts for payroll taxes and expenses. Employees can be assigned to single or multiple departments, with salary expenses distributed by percentage if needed.

- **Wage, Deduction, and Benefit Codes**: Wage codes define pay types (hourly, salary, bonus, commission) and rates. Deduction codes represent employee-paid deductions (e.g., health insurance, 401k contributions), while benefit codes track employer-paid contributions. Taxability and GL accounts are configured per code.

- **Overtime Handling**: The system supports automatic overtime billing based on configured workday hours but often dealerships disable this to manually control overtime charges, avoiding billing customers for non-chargeable overtime.

- **Payroll Processing Workflow**: Payroll runs include selecting employees, applying deductions, entering pay data (including bonuses and commissions), printing checks, and posting to the GL. Accrued transactions are created if payroll is started but not completed and must be reversed before reprocessing.

### System Architecture & Data Model

- **Employee Records**: Stored in the Payroll module, employee records include personal details, department assignment (`DEPT` field), pay frequency, wage codes, deduction codes, benefit codes, and tax withholding information.

- **Department Codes**: Departments link employees to specific GL accounts for payroll expenses and employer tax liabilities. Department codes are distinct within payroll and may differ from other DIS departmental codes.

- **Work Orders and Time Clock Data**: Time punches are linked to work orders, enabling labor hours to be reviewed and billed directly from the work order screen. Non-work order statuses track non-billable time such as training or vacation.

- **GL Account Structure**: Payroll-related GL accounts are structured by division, base account, and department. Liability accounts for payroll taxes require a 'G' edit code in the Chart of Accounts. Departmentalized companies must carefully manage account numbering to avoid misclassification.

- **Tax Calculators**: State-specific tax calculators are loaded into the system to handle payroll tax computations according to jurisdictional requirements.

### Key Procedures

**1. Enabling Technician View for a Division**

1. Ensure all technicians in the division are clocked out.
2. Access the AS/400 command line.
3. Enter the command: `X00081 [Division Code],1` (e.g., `X00081 K,1`) to enable Technician View.

**2. Technician Clock-In with Technician View**

1. Technician logs into the Time Clock screen.
2. Enters their technician number and clocks in.
3. System prompts for a work order or non-work order status selection.
4. Technician selects the appropriate work order or status; time is assigned accordingly.

**3. Configuring Automatic Shop Supply Fees**

1. Navigate to `Point of Sale > Point of Sale Parameters > Automatic Point of Sale Charges`.
2. Select the division to configure.
3. Define the sales code for the shop supply fee (e.g., `SS`).
4. Specify the percentage charge.
5. Add included sales codes (e.g., labor `S1`, parts `P1`) that the fee applies to.

**4. Adding a New Employee in Payroll**

1. Access `Accounting > Payroll > Full Access > Inquire/Update Payroll Employee`.
2. Create a new employee record with personal and employment details.
3. Assign the employee to a department.
4. Link applicable wage, deduction, and benefit codes.
5. Set pay frequency and tax withholding information.

**5. Processing Payroll**

1. Navigate to the Process Payroll screen.
2. Select one or multiple employees for payment.
3. Choose "Use deductions selected above" to apply deductions.
4. Enter the pay date.
5. Review and edit employee timesheets, adding bonuses or commissions as needed.
6. Run the payroll register and print checks.
7. Post payroll to the general ledger.

**6. Reversing Accrued Payroll Transactions**

1. Start a new payroll run for the affected employee.
2. Access the "Accrual" tab.
3. Reverse each accrued line item from the previous incomplete payroll.
4. Confirm reversal lines appear in the "Current" tab.
5. Process a new payroll check (can be zero-dollar) to clear accruals.
6. Complete payroll processing by printing the check.

**7. Adding Bonus or Commission Pay**

1. On the employee’s timesheet, select a blank line.
2. Enter the dollar amount of the bonus or commission.
3. Specify the appropriate wage code (e.g., "Bonus" or "Commission").
4. Save the entry.

**8. Splitting a Salaried Employee’s Pay**

1. On the timesheet, adjust the percentage of the default salary line (e.g., 50%).
2. Add a new line with a different salary wage code.
3. Set the percentage for the second salary line (e.g., 50%).
4. The system calculates total pay based on the split percentages.

### Menu Navigation

- **Time Clock Configuration**:  
  `Point of Sale > Time Clock > Configuration`

- **Technician View Setup**:  
  `Point of Sale > Time Clock > Technician View`

- **Technician Setup and Payroll Employee Maintenance**:  
  `Accounting > Payroll > Full Access > Inquire/Update Payroll Employee`

- **Work Order Management**:  
  `Point of Sale > Work Order > Inquire/Update/Post`

- **Automatic Fee Setup**:  
  `Point of Sale > Point of Sale Parameters > Automatic Point of Sale Charges`

- **Payroll Processing**:  
  Accessed via the Payroll module’s Process Payroll screen (exact path varies by installation)

### Business Rules & Constraints

- All technicians must be clocked out before enabling Technician View for a division.
- Employees must be set up in the Payroll module before using the Time Clock.
- Manual labor entries on work orders do not create time clock punches and should be used sparingly.
- The same labor sales code should be used consistently across customer, internal, and warranty work orders for accurate accounting.
- Only one user can modify the Field Configuration at a time.
- Child support deductions must be configured as after-tax (`Tax Type = N`) and are automatically invoiced to the appropriate vendor.
- Payroll pay periods must be consistent across all employees within a company.
- Negative net pay checks cannot be processed; such employees must be bypassed.
- Accrued payroll transactions must be reversed and cleared before reprocessing payroll for an employee.
- Wage codes should not be modified for raises; instead, create new wage codes to preserve historical pay data.
- Salaried employees cannot have bonuses added directly to their salary line; bonuses require separate wage code entries.
- Departmentalized companies must carefully manage GL account numbering to avoid misallocation of payroll liabilities.

### Configuration Options

- **Technician View (`X00081` command)**: Enable or disable mandatory clock-in to work orders.
- **Hours Rounding**: Choose to bill actual hours or round to nearest tenth, quarter, or whole hour.
- **End of Day Reports**: Configure automatic printing of daily time reports, with options to group by technician or work order.
- **Page Break by Technician**: Option to print each technician’s daily summary on a separate page.
- **Automatic Point of Sale Charges**: Define fees such as shop supplies or environmental fees as a percentage of selected sales codes.
- **Payroll Field Configuration**: Setup tax departments, GL distributions, and tax calculators.
- **Wage Codes**: Define pay types, rates, and taxability.
- **Deduction Codes**: Configure deduction types, tax treatment (pre-tax, after-tax), GL accounts, and AP invoice integration.
- **Benefit Codes**: Track employer-paid contributions.
- **Bank Account Maker Setting**: Automate check numbering for payroll checks.
- **Overtime Rate Multiplier**: Configure the multiplier for overtime pay (e.g., 1.5 for time and a half).
- **Unemployment Insurance (UI) Rates**: Set globally or per dealership to accommodate state-specific requirements.

### Common Pitfalls & Warnings

- Forgetting to clock out technicians before enabling Technician View can cause system errors.
- Manual labor entries on work orders bypass the Time Clock, leading to inaccurate labor hour reporting.
- Switching to Technician View after technicians are trained on the older method is difficult; it is best to enable Technician View at implementation.
- Missing employee mailing addresses can delay paycheck delivery.
- Users often overlook pressing "Enter" to view multiple deductions on an employee record.
- Incorrect department assignment or pay distribution can misallocate labor costs.
- Duplicate pay type entries in employee distributions require cleanup.
- Failing to select "use deductions selected above" during payroll processing results in deductions not being applied.
- Incomplete Field Configuration setup prevents successful payroll processing.
- Incorrect tax type assignment on deductions (e.g., child support) causes tax calculation errors.
- Attempting to modify existing wage codes for raises compromises payroll history.
- Bonuses must be entered as separate wage code line items, not added to salary lines.
- Payroll runs started but not completed create accrued transactions that must be reversed before reprocessing.

### Key Terminology

- **Technician View**: A Time Clock mode requiring technicians to clock into specific work orders, enabling real-time monitoring of technician activity.
- **Punch**: A single clock-in or clock-out time entry in the Time Clock system.
- **Non-Work Order Status**: Codes used to track non-billable time such as vacation (`VAC`), training (`TRN`), or cleaning.
- **Field Configuration**: The payroll setup area where tax departments and GL accounts are defined.
- **Departmentalization**: Assigning employees and payroll expenses to specific departments for detailed financial tracking.
- **Wage Code**: A code representing a pay type and rate, such as hourly, salary, bonus, or commission.
- **Deduction Code**: A code representing an employee-paid deduction, with taxability and accounting settings.
- **Benefit Code**: A code representing employer-paid benefits or contributions.
- **Tax Type**: A setting on deduction codes indicating tax treatment: 'C' for Cafeteria (pre-tax), 'P' for Pension (pre-tax), and 'N' for None (after-tax).
- **Accrued Transactions**: Payroll entries created when payroll processing is started but not completed, requiring reversal before reprocessing.
- **Maker**: A bank account setting that enables automatic check numbering.
- **Distributed Employee**: An employee whose salary expenses are allocated across multiple departments or profit centers.
- **FUTA**: Federal Unemployment Tax Act, an employer-paid tax.
- **Cafeteria Plan**: A pre-tax benefit plan allowing employees to select from various benefits.
- **Pension Plan**: A retirement plan, such as a 401(k), tracked as employer benefits in the system.

---