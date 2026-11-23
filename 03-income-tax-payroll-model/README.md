# Income Tax Lookup & Payroll Automation (Excel)

A formula-driven payroll and income tax calculation model built in Microsoft Excel under the **Indian New Tax Regime (FY 2024–25 / AY 2025–26)**, utilizing dynamic lookup functions, progressive tax slab logic, and conditional aggregations.

## Project Files
- **`IncomeTax_Advanced_Blank.xlsx`**: Starter template containing assignment guidelines (`Instructions`), a 12-employee payroll dataset alongside tax slab, surcharge, department directory, and city classification reference tables (`Tax Worksheet`), and 18 dynamic lookup prompts (`Questions`).
- **`Income Tax Solved.xlsx`**: Completed workbook with fully automated formulas (zero hardcoded values) across all payroll calculations and lookup tasks.

## Key Implementations

### Part A: Automated Payroll Tax Engine (`Tax Worksheet`)
Built dynamic row-level formulas across 12 employees (`E101`–`E112`) using absolute cell references (`$`) tied to statutory constants and progressive tax tables:
- **Taxable Income**: Deducted the ₹75,000 Standard Deduction from Gross Salary using `MAX` to prevent negative taxable balances.
- **Marginal Slab Rate & Label**: Retrieved applicable tax rates (`Nil` to `30%`) and slab labels using approximate-match `VLOOKUP` and `INDEX` + `MATCH`.
- **Progressive Income Tax**: Calculated tiered tax liability (`Tax at Band Start + Excess Income × Marginal Rate`) via nested `VLOOKUP` lookups.
- **Section 87A Rebate & Net Tax**: Applied `IF` + `MIN` logic to grant up to ₹25,000 tax rebate for employees with taxable income ≤ ₹7,00,000, computing final post-rebate tax.

### Part B: Dynamic Lookup & Query Model (`Questions`)
Constructed formula-based answers driven by interactive input cells (`EmpID`, `Department`, `City`, `Income`, `Name`):
- **Exact & Reverse Lookups**: Used `XLOOKUP`, `VLOOKUP`, and `INDEX` + `MATCH` to retrieve employee records and perform reverse ID lookups by employee name.
- **Horizontal & Two-Way Lookups**: Queried department HR emails and heads via `HLOOKUP` and built dynamic cross-table lookups.
- **Approximate-Match Tax & Cess Calculations**: Computed progressive tax and 4% Health & Education Cess on test incomes and employee records.
- **Departmental Aggregations**: Used `COUNTIF` and `SUMIF` to summarize department headcounts and pre-rebate tax collections.

## Payroll Summary & Highlights
- **Total Gross Payroll**: ₹2,96,70,000 across 12 employees (`Engineering`, `Sales`, `Marketing`, `Finance`, `HR`).
- **Total Taxable Income**: ₹2,87,70,000 (after ₹75,000 standard deduction per employee).
- **Tax & Rebate Impact**: ₹57,46,500 gross income tax generated; 3 employees qualified for Section 87A tax relief totaling ₹41,750, resulting in **₹57,04,750** net tax payable.
- **Departmental Tax Leader**: **Finance** generated ₹32,37,750 in pre-rebate income tax across 3 employees (led by highest earner **Aditya Menon** at ₹1,15,00,000 gross salary).

## Tools & Excel Functions Used
- **Lookup & Reference**: `XLOOKUP`, `VLOOKUP` (Exact & Approximate Match), `HLOOKUP`, `INDEX`, `MATCH`
- **Logical & Math**: `IF`, `MIN`, `MAX`, nested progressive slab arithmetic
- **Conditional Aggregation**: `COUNTIF`, `SUMIF`
